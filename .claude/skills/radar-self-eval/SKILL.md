---
name: radar-self-eval
description: |
  Compute the radar's self-calibration: weekly funnel metrics (queue dynamics, exploration compliance, off-axis rate), a monthly hit/miss retrospective against what actually became big, and up to 3 curator proposals. Use during every weekly recalibration, after the source-strategy review; results go into the append-only `calibration` section of TRENDS.md and into the weekly report.
---

# Self-evaluation

The radar must measure whether it is winning, not assume it. Three parts:
metrics (every week), retrospective (monthly), curator proposals (every week).

## 1. Weekly metrics

Compute from the week's daily reports (primary source — they list ledger
changes) and, where needed, `git log -p -- TRENDS.md` since the previous weekly
commit:

- **queue funnel**: items added / promoted to trend / dropped / older than 14
  days and still unverified (stale)
- **ledger**: evidence items added, stage moves (up and down)
- **exploration compliance**: daily runs whose `source_rotation` line contains a
  venue-exploration entry ÷ daily runs executed
- **off-axis rate**: share of new queue items that do NOT match any axis in
  `strategy_notes` (judgment call — name them)

Append ONE dated line to `## calibration` in TRENDS.md:
`- YYYY-MM-DD — W<nn>: queue +a/→p/−d/stale s · evidence +e · moves m · exploration c/r · off-axis o/a`
and include the same numbers, readable, in the weekly report.

Interpretation thresholds (act, don't just log):
- exploration compliance < 100% → call it out; two weeks running → propose a
  daily prompt/skill refinement.
- stale > half the queue → scanning breadth exceeds verification capacity:
  propose narrowing or a verification-only day.
- off-axis = 0 for two consecutive weeks → anchoring warning, even if the
  tunnel-vision check passed.

## 2. Monthly retrospective (first weekly run of the month: `date +%d` ≤ 7)

Goal: ground truth — did the radar see early what later became big?

1. Pick 2–3 items that clearly became big in the past month by BROWSING venues
   (open the pages — evidence rules apply): HF papers trending, two major lab
   blog indexes, one arXiv listing. Pick what is everywhere, not what is
   interesting.
2. For each, find the radar's earliest mention:
   `git log -S"<term>" --oneline -- TRENDS.md` plus the queue and reports.
3. Classify: **HIT-early** (tracked ≥7 days before it was everywhere),
   **HIT-late**, **MISS**.
4. For every MISS: add it to `observation_queue` now, and name the venue or
   axis that would have caught it — feed that into the proposals.

Log in `## calibration`:
`- YYYY-MM-DD — retro M<mm>: <item> — HIT-early|HIT-late|MISS (first seen <date or never>), …`

## 3. Curator proposals (every week, max 3)

The mission — scope axes, trend bar, prompts — belongs to the curator; the radar
may question it but never change it. Close the weekly report with up to 3
proposals the radar cannot apply alone: drop/merge a scope axis, change a
routine prompt (give the exact replacement text), adjust the exploration budget.
Each proposal must cite the metric or retrospective result that motivates it.

Tracking: an unanswered proposal may be re-raised once, then dropped. An adopted
proposal will appear later as a dated curator entry in `strategy_notes` —
written by the curator, never by the radar.

## Boundaries

- Evidence rules apply to the retrospective: cite only opened pages.
- `## calibration` is append-only: never edit or delete existing lines.
- If a metric shows the same procedural failure twice, trigger a skill
  refinement per the maintenance policy in AGENTS.md (dedicated commit,
  explained in the report).
