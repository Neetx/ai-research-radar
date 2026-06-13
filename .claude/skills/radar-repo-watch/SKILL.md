---
name: radar-repo-watch
description: |
  Watch a curated set of important GitHub repos every daily run for behind-the-scenes movement — new releases/tags, notable merged PRs, and high-activity issues/discussions — to catch the build-up before the big merge, not just the release. Releases and merges are citable artifacts; issue/PR turbulence is a queue signal. Use during the daily scan, after the lab sweep.
---

# Repo watch — catch the turbulence before the merge

In big projects, important changes show up as PR/issue activity well before the
headline release. Watching the repos directly surfaces that early.

## Method

For each repo in `SOURCES.md` → "Watched GitHub repos", check activity since the
last scan (use the previous `source_rotation` date). Prefer the GitHub REST API
via curl (the routine has GitHub access), or `tvly`/web as fallback:

- **Releases / tags**: `https://api.github.com/repos/<owner>/<repo>/releases` —
  a new release is a citable artifact (evidence-eligible against a trend).
- **Recently merged PRs**: `…/pulls?state=closed&sort=updated&direction=desc` —
  filter to `merged_at` after the last scan; a notable merged PR (new feature,
  format, kernel, model support) is a citable artifact.
- **Hot issues / discussions**: `…/issues?sort=comments&state=open` — a
  suddenly high-activity thread is a QUEUE signal (unverified turbulence), not
  evidence, until it lands.

Keep it light: headline-level, only items newer than the last scan. Log the
watch in `source_rotation` every run, even when quiet ("repo-watch: no movement").

## Classification

- Release / merged PR → evidence rules apply; match to a trend or `study_shelf`.
- Issue/PR turbulence → `observation_queue`, marked unverified, with the repo +
  thread link; promote only when it results in a merged artifact.

## Self-maintenance (agent owns this)

Add repos that become central to a tracked trend; drop repos that go silent or
off-scope (one-line reason in the report). Keep the list in `SOURCES.md`.
