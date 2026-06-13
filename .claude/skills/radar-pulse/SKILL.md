---
name: radar-pulse
description: |
  Sample social/community sources (Reddit, Hacker News, YouTube, Hugging Face, and best-effort X/Instagram) for sentiment and leading-indicator buzz on every daily run. Social is an INTAKE LANE ONLY — it can feed observation_queue (unverified) and a community-pulse note, but NEVER becomes trend evidence. Use after the lab sweep and arXiv scan.
---

# Community pulse — intake only, never evidence

Social tells you what people *think* and what is gaining traction before it
reaches papers/docs. But social is not a primary source. This skill captures
that value without corroding the ledger's evidence standard.

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

For every signal worth keeping: if it points to a concrete artifact, log a
queue item ("verify <artifact>"); if it is pure sentiment, hold it for the
pulse note. Cap at ~5 pulse items per run.

## Self-maintenance (agent owns this)

- Add researcher/lab handles, subreddits, channels to `SOURCES.md` as you find
  ones that recur with signal; drop channels that produce only noise (one-line
  reason in the report).
- If a platform is persistently unreachable for 2+ weeks, note it and stop
  trying until conditions change.
- Propose, via the weekly amendment process, any change that would need new
  env secrets (e.g. a paid X API) — the curator decides those, not the agent.
