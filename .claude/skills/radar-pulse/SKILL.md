---
name: radar-pulse
description: |
  Sample social/community sources (Reddit, Hacker News, YouTube, Hugging Face, and best-effort X/Instagram) for sentiment and leading-indicator buzz on every daily run. Social is an INTAKE LANE ONLY — it can feed observation_queue (unverified) and a community-pulse note, but NEVER becomes trend evidence. Use after the lab sweep and arXiv scan.
---

# Community pulse — intake only, never evidence

Social tells you what people *think* and what is gaining traction before it
reaches papers/docs, and it is often the FASTEST place to spot that something
official exists (a post links a repo, a release, a paper). Social is not a
primary source — but it is a discovery accelerator. This skill captures both
without corroding the ledger's evidence standard.

The platform/channel/profile list lives in `SOURCES.md`; treat it as a seed and
curate it by your own judgment — add platforms and accounts that prove useful,
drop noise. Don't restrict yourself to a fixed roster.

## Absolute rules (constitutional carve-out — see AGENTS.md Hard rules)

1. Social NEVER becomes trend evidence. It may only:
   - create `observation_queue` items, marked `unverified` — promotable to a
     trend ONLY after the claim is confirmed on a primary artifact (paper,
     repo, release, official doc), via the `radar-source-verify` skill;
   - feed the community-pulse note surfaced on the dashboard (Phase 3).
2. Never name or quote individuals in the repo. Link the thread/profile and
   summarise the signal ("a widely-upvoted r/LocalLLaMA thread reports X").
   No handles in evidence/queue text beyond the bare URL.
3. Opened-source rule still applies: only log what you actually fetched.

## Method (best-effort via Tavily, no paid APIs)

Per run, sample the channels in `SOURCES.md` → "Social & community channels".
Keep it light — this is a pulse, not a crawl. For each platform:
- **Reddit / Hacker News**: search the tracked subreddits / HN for the day's
  high-engagement AI posts; note recurring topics and sentiment shifts.
- **YouTube / Hugging Face**: check tracked channels/accounts for new activity.
- **X / Instagram**: best-effort via Tavily on the profile URLs in SOURCES.md.
  These are unreliable in 2026 (no free API); if a profile can't be fetched,
  log "X/IG degraded: <handle> unreachable" in `source_rotation` and move on —
  do not fabricate.

## Discovery fast-track (the main point)

When a social signal LINKS TO or NAMES a primary artifact (repo, release, paper,
official blog post), do not just queue the rumour — FOLLOW the link in the same
run and verify the artifact via `radar-source-verify`. If the artifact clears
the evidence rules, it becomes evidence THIS run, cited to the primary source
(never to the social post). Social is how you find it days early; the primary
artifact is what you cite. Only when there is no reachable artifact yet does the
signal stay a queue item.

For signals without an artifact: if it points to something concrete but not yet
findable, log a queue item ("verify <thing>"); if it is pure sentiment, hold it
for the pulse note. Cap at ~5 pulse items per run.

## Self-maintenance (agent owns this)

- Add researcher/lab handles, subreddits, channels to `SOURCES.md` as you find
  ones that recur with signal; drop channels that produce only noise (one-line
  reason in the report).
- If a platform is persistently unreachable for 2+ weeks, note it and stop
  trying until conditions change.
- Propose, via the weekly amendment process, any change that would need new
  env secrets (e.g. a paid X API) — the curator decides those, not the agent.
