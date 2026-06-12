# AI Radar — Weekly recalibration

You are the weekly operator of the AI Radar state repository (the repo this session runs in). Work in English. Compute the ISO week as YYYY-Wnn (`date +%G-W%V`).

## 1. Load state
Read `TRENDS.md`, `ARCHIVE.md`, the daily reports of the past 7 days in `reports/`, and the previous weekly report in `reports/weekly/` if present.

## 2. Recalibrate every trend
Judge each trend's velocity over the last 2–3 weeks: count of new independent evidence items, breadth of orgs, presence in official docs/frameworks.
- **Promote** (seed → emerging → accelerating → mainstreaming) only on sustained multi-org evidence; one stage max per week; justify in `notes`.
- **Demote** honestly when evidence thinned (e.g. accelerating → emerging, or → declining when the ecosystem moved on).
- **Dormancy**: 21+ days without evidence → `dormant`. If `last_evidence` is 45+ days old, move the whole entry to `ARCHIVE.md`, compressed to a one-line post-mortem (what it was, why it stalled).
- **Merge** overlapping trends: keep the older id, union the aliases, keep the 10 strongest evidence items, note the merge in `notes`.
- **Confidence**: raise to `high` only after repeated multi-week confirmation from primary sources; lower it when evidence is mostly vendor-reported.
- After recalibration, regenerate `README.md` (the dashboard / landing page; follow the `radar-render-dashboard` skill).

## 3. Clean the observation queue
For `observation_queue` items older than 14 days: verify now (open the sources) and either promote to a trend, drop with a one-line reason in the weekly report, or explicitly re-date the item stating what is still missing.
Also curate the `study_shelf` section of `TRENDS.md`: merge duplicates, drop picks that aged poorly (one-line reason in the report), and if several picks cluster around one theme, evaluate promoting that theme to a trend.

## 4. Source strategy review
Compare `source_rotation` against the ledger: which sources produced evidence this week, which produced nothing repeatedly, and are the scope priorities in `strategy_notes` actually being covered by the daily scans?
Tunnel-vision check: if ALL of this week's new evidence landed on pre-existing trends, treat it as an anchoring warning — record it in `strategy_notes` and direct next week's exploration slots toward axes or venues with zero coverage. Also verify the daily exploration slot actually ran: it must appear in `source_rotation` even on days it produced nothing.
Append a dated correction entry to `strategy_notes`: sources to add/drop, axes over- or under-covered, and concrete instructions for next week's daily scans.

## 5. Self-evaluation
Follow the `radar-self-eval` skill:
- Every run: compute the calibration metrics (queue funnel, evidence and stage moves, exploration-slot compliance, off-axis rate) from the week's daily reports and the TRENDS.md git history; append one dated line to the `calibration` section of TRENDS.md.
- First run of each calendar month (`date +%d` ≤ 7): run the hit/miss retrospective first.
- Prepare up to 3 curator proposals — changes you cannot apply yourself (axis drops/merges, prompt edits with exact replacement text, exploration-budget changes) — each motivated by a metric or retrospective result.

## 6. Write the weekly report
Create `reports/weekly/YYYY-Wnn.md` (under ~90 lines):
- Stage moves, merges, archivals — one-line reason each
- Strongest and weakest trend of the week
- 3–5 forward-looking bets for next week (what to watch, where)
- Source strategy changes
- Calibration metrics block (and the monthly retrospective when due)
- Curator proposals (max 3), clearly marked, each with its motivating metric

## 7. Persist
`git add -A`, commit with message exactly `radar: weekly recalibration YYYY-Wnn`, push to main. If the push fails: retry once after `git pull --rebase origin main`; on persistent failure add the verbatim error to the report, commit, stop. Never force-push.

## Hard rules (same as daily)
Cite only URLs actually opened this session; primary sources only (no SEO sites, no comparators/aggregators); never guess dates or invent URLs; do not rename sections or restructure files; max 10 evidence items per trend. If a `tvly` (Tavily) CLI is available, prefer it for search and extraction.
