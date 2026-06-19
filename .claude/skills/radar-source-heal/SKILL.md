---
name: radar-source-heal
description: |
  Repair a source or tool that keeps failing — a broken/moved/stale feed, a 404, an empty result, a parse/JSON error — instead of logging "degraded" forever. Diagnose the failure class, find a working access path, and record the repaired method in SOURCES.md so future runs don't repeat it. Generalizes to any future source/tool breakage. Use whenever the lab sweep, pulse, or repo-watch hits a source that failed the same way before.
---

# Source self-healing

Logging "degraded" run after run is a failure of the radar, not of the source.
If you logged the same breakage last run (check the recent `source_rotation`
tail and SOURCES.md notes), **fix it this run** — don't just re-log it.

## When to heal (don't thrash)

- One transient failure → log it, retry next run. Do not heal on a single blip.
- The SAME failure twice (across runs), OR obviously degraded data now (empty
  feed, 404, JSON/parse error, a feed whose newest item is months old) → heal.

## Diagnose the failure class, then repair

**Class A — broken / moved / stale feed or page**
- Open the source's HTML index. Find the real feed from the page's
  `<link rel="alternate" type="application/rss+xml|atom+xml">`, or try common
  paths: `/rss`, `/feed`, `/rss.xml`, `/atom.xml`, `/index.xml`, `/blog/feed.xml`.
- Moved blog (org rebranded/changed domain) → search for the current URL and
  confirm it resolves with recent posts.
- Stale feed (newest post months old while the org is clearly still active) →
  the org now posts elsewhere; find the live channel (a different domain, their
  HF org activity, a docs/changelog page) and switch to it.
- No feed exists at all → set the method to "HTML index via Tavily extract" and
  note it, so the sweep stops hunting for a feed.

**Class B — failing tool call on an otherwise-live source**
- Vary the call shape: different `tvly` flags, `extract` vs `search`,
  `--extract-depth advanced`, smaller/larger scope.
- Prefer the source's own structured endpoint when it has one (many sites expose
  a JSON/search API — e.g. a public search endpoint — that returns clean data
  without scraping).
- Fall back to the built-in web tools if Tavily keeps failing on that source.
- Find the shape that returns clean, parseable data.

## Record the fix (this is the durable part)

Write the WORKING access method back into `SOURCES.md` next to that source,
dated, REPLACING the "degraded/404/stale" note — e.g. "feed at <url> (confirmed
working YYYY-MM-DD)" or "use <endpoint>, not the feed (YYYY-MM-DD)". The registry
is agent-owned; the repaired method is what makes the fix permanent. If a source
is genuinely dead with no replacement, mark it `RETIRED <date> — <reason>` and
drop it from the active list.

## Persistent environmental / IP blocks (don't re-log forever)

Some sources are blocked not by a broken path but by the environment — a
datacenter-IP block by the site, or egress restricted to a few hosts. You cannot
"repair" these, but you must NOT re-log "blocked from this IP" every run either.
- **Diagnose** which it is: try a neutral *programmatic* endpoint (an API host
  like `hn.algolia.com`). If it works, the block is site-specific → switch that
  source to its API host (e.g. HN → `hn.algolia.com/api/v1/...`; HF → the
  `huggingface.co/api/...` endpoints; Reddit → the `.json`/RSS endpoints or a
  mirror). If even the neutral API host fails, the environment's egress is
  restricted.
- **Record once**: pick the best reachable method and write it into SOURCES.md as
  a KNOWN CONSTRAINT with that method; then stop re-logging it run after run.
- **Escalate** (weekly proposal) only if the only real fix needs a secret (e.g. a
  free Reddit OAuth app → `REDDIT_CLIENT_ID/SECRET`) or a change to the
  environment's allowed domains — those are the curator's call.

## Escalate only when a fix needs what the agent can't grant

If the only working path needs a secret or paid API (e.g. a paid X API), do NOT
hardcode it — keep the source best-effort, log it, and PROPOSE the paid option
via the weekly amendment process for the curator to decide.

## Effort cap

Heal at most ~1–2 sources per run; if several are broken, repair the
highest-value first and queue the rest for following runs. Healing must never
crowd out the actual scan.

## Open cases to apply this to (examples, not hardcoded fixes)

Diagnose and repair these with the procedure above, then record what works:
- Hacker News pulse returning a Tavily JSON error (Class B) — find a call shape
  or a structured HN endpoint that parses cleanly.
- Anthropic news feed 404 and Meta blog feed empty (Class A) — locate the real
  feed or switch to HTML extraction.
- EleutherAI / Qwen feeds stale by months (Class A) — find where each org
  actually publishes now.
