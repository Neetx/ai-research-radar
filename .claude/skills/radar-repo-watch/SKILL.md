---
name: radar-repo-watch
description: |
  Watch GitHub every daily run for behind-the-scenes movement — across watched REPOS (releases, merged PRs, hot issues), watched PROFILES/USERS (what a key author ships next, across all their repos), and FORK TREES (notable forks up to depth 3, scored by a notability metric). Releases and merges are citable artifacts; profile/issue/fork movement is a queue signal until it lands. Use during the daily scan, after the lab sweep. Source lists live in SOURCES.md → "GitHub watch".
---

# GitHub watch — repos, profiles, and fork trees

In big projects, important changes show up as PR/issue/fork activity well before
the headline release. Watching repos, the people behind them, and their fork
trees surfaces that build-up early. Prefer the GitHub REST API via curl (the
routine has GitHub access); `tvly`/web as fallback. Use the routine's GitHub
credentials for API calls when available (authenticated = 5000 req/hr); if
unauthenticated (60 req/hr), keep it lean — batch, and shrink the fork walk
before the rest of the scan suffers. Check activity since the last scan
(previous `source_rotation` date). Log the watch every run, even when quiet
("github-watch: no movement").

## 1. Watched repositories

For each repo in SOURCES.md → "Watched repositories":
- **Releases / tags** — `…/repos/<o>/<r>/releases` — a new release is a citable
  artifact (evidence-eligible against a trend).
- **Recently merged PRs** — `…/pulls?state=closed&sort=updated&direction=desc`,
  filter `merged_at` after last scan — a notable merged PR (feature, format,
  kernel, model support) is a citable artifact.
- **Hot issues / discussions** — `…/issues?sort=comments&state=open` — a
  suddenly high-activity thread is a QUEUE signal until it lands.

## 2. Watched profiles / users

For each user in SOURCES.md → "Watched profiles/users", see where the author is
heading next: `…/users/<u>/repos?sort=pushed` and their recent public events
(`…/users/<u>/events/public`). Surface: brand-new repos, a repo suddenly getting
heavy pushes, or a new release across any of their repos. New repos/releases are
citable; early push activity on an unreleased repo is a queue signal ("watch
<user>/<repo>, pre-release").

## 3. Fork-tree analysis (depth 3) + Fork Notability Score

For each project in SOURCES.md → "Fork-tree analysis", walk the fork tree up to
depth 3 (`…/repos/<o>/<r>/forks?sort=newest`, then forks of those, then forks of
those). Prune aggressively: only descend into a fork that is itself active
(pushed in the last ~30 days) — dead forks have no live children worth chasing.

Compute the **Fork Notability Score (FNS)** per fork:

```
gate:   pushed within last 30 days           (else skip — stale)
FNS  =  commits_ahead_of_upstream            (via /compare/<upstream>...<fork>, ahead_by)
      + 2 × (fork's own stars)
      + 20 if the fork has its own releases/tags
      + 15 if the fork has an open PR back to upstream
```

**Surface a fork under the project's trend when FNS ≥ 50 AND commits_ahead ≥ 20.**
- A fork that clears the bar AND ships a release/artifact → citable evidence
  under that project's trend (cite the fork repo/release).
- A fork that clears the bar but is still pre-release (just diverging fast) →
  `observation_queue` signal ("fork <o>/<r> diverging, N commits ahead").
- Name the fork in the trend's notes/evidence ("fork X carries feature Y not yet
  upstream"). Tune the threshold over time and log changes in the report.

Rationale: in this ecosystem the real innovation often lives in an active,
far-ahead fork (performance/quant variants) months before it merges upstream —
FNS is meant to catch exactly those, not the thousands of bookmark forks.

## Self-maintenance (agent owns this)

Add repos/users/projects that become central to a tracked trend; drop ones that
go silent or off-scope (one-line reason in the report). Adjust the FNS weights
and threshold as you learn what they surface — record any change. Keep all lists
in `SOURCES.md`.
