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
- **Reddit**: read the TOP posts of the tracked subreddits — both the technical
  subs AND the broad-pulse subs. Note two things, not one: (a) recurring on-axis
  topics, and (b) whatever is *dominating* a community right now, on-axis or not.
- **Hacker News**: read the FRONT PAGE unconditionally (the #1 story is a
  don't-miss), in addition to term searches.
- **Trusted curators (YouTube channels + explainer blogs/newsletters) — check EVERY run, this is a PRIMARY DISCOVERY path, not "social noise":** check BOTH halves — the YouTube channels AND the explainer/digest pointer blogs (SOURCES.md → YouTube + the pointer-lane trackers, incl. alphamatch.ai). Neither half is "on rotation"; the explainer-blog half is as mandatory as the YouTube half and is the one that tends to get silently dropped — NAME in the coverage log which pointer blogs you actually opened, because a tracked blog that never appears in the log is a dead lane — its papers never get captured. For every new video/post, FOLLOW the description/link to the named paper/repo and verify the PRIMARY (radar-source-verify); cite the primary, never the curator. This is how high-signal work surfaced by a person (e.g. a code4AI paper deep-dive) gets caught even when it hasn't ranked on arXiv/HF yet.
- **Hugging Face**: check tracked accounts/orgs for new activity.
- **X / Instagram**: best-effort via Tavily on the profile URLs in SOURCES.md.
  These are unreliable in 2026 (no free API); if a profile can't be fetched,
  log "X/IG degraded: <handle> unreachable" in `logs/source_rotation.md` and move on —
  do not fabricate.

## Discovery fast-track (the main point)

When a social signal LINKS TO or NAMES a primary artifact (repo, release, paper,
official blog post), do not just queue the rumour — FOLLOW the link in the same
run and verify the artifact via `radar-source-verify`. If the artifact clears
the evidence rules, it becomes evidence THIS run, cited to the primary source
(never to the social post). Social is how you find it days early; the primary
artifact is what you cite. Only when there is no reachable artifact yet does the
signal stay a queue item.

A NAMED primary has exactly TWO valid end-states, never a third: (a) verified →
evidence, or (b) an `observation_queue` item carrying the named id/URL. "Intake —
no action", "noted", "hit-attributed to <curator>" are NOT end-states: attribution
records WHERE you saw it, capture records WHAT it is, and only the queue/ledger is
capture — report prose and SOURCES notes are not. "We already know this is a miss"
is the trap, not an excuse: if a named primary is recognized but is not in the
queue or the ledger, it has been LOST, so queue it now. (The failure this
prevents: a primary named repeatedly in report/SOURCES prose and attributed to a
curator, yet never followed to its artifact, verified, or queued — so the radar
never even holds its id.)

For signals without an artifact: if it points to something concrete but not yet
findable, log a queue item ("verify <thing>"); if it is pure sentiment, hold it
for the pulse note. Cap at ~5 pulse items per run — but a field-shaking event
(below) always makes the cut, even off-axis.

## Don't miss the earthquake (field-shaking events)

The pulse's job is NOT only to extract on-axis signal — it is also to notice when
the ground moves. The classic failure: the top post of your #1 community is a
field-shaking story, but you discard it because it doesn't map to a tracked axis.
Do not do that.

- **Check ALL channels, not one — never collapse the pulse to HN.** The
  earthquake check is multi-channel every run: HN front page (Algolia) + the
  broad Reddit subs + the trusted curators + the digests; X best-effort. HN is
  the reliable backbone, but an HN-only pulse is incomplete — and the report
  must NAME which channels were actually checked (a single-channel pulse is a
  visible gap to fix, not "done"). Cross-posting is your friend: a real
  field-shaking event shows up across several of these within hours, so checking
  the reliable set catches it even when X/Reddit-direct are flaky.
- **Cross-community virality = importance.** If one event is dominating the top
  of a major community — or several communities at once (technical AND broad) —
  that IS the signal, on-axis or not. Surface it.
- **Vendor-neutral.** This applies to the WHOLE field, not any one company:
  OpenAI, Google, Meta, Anthropic, Mistral, xAI, regulators, the open-weight
  labs — whoever the earthquake involves. Do not over-index on a single vendor;
  the test is "is the field consumed by it", not "which logo is on it".
- **Where it lives.** A field-shaking event that is not a research/engineering
  trend (a model ban, an abrupt global access cut, a vendor/government action, an
  acquisition, a major outage) does NOT go in the trend ledger and is NOT
  evidence — but it MUST appear in the community-pulse note ("the community is
  consumed by X"). The radar must *say the ground moved*, even when it has no
  trend for it. Follow to a primary source if one exists; otherwise log it as
  the dominant unverified pulse item with the thread link.
- **Test:** if a practitioner would say "how did your radar not mention THAT?",
  it belonged in the pulse. Operational earthquakes (a model you depend on
  vanishing) count, even though they are not papers or releases.

## Self-maintenance (agent owns this)

- Add researcher/lab handles, subreddits, channels to `SOURCES.md` as you find
  ones that recur with signal; drop channels that produce only noise (one-line
  reason in the report).
- If a platform is persistently unreachable for 2+ weeks, note it and stop
  trying until conditions change.
- Propose, via the weekly amendment process, any change that would need new
  env secrets (e.g. a paid X API) — the curator decides those, not the agent.
