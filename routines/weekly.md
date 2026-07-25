# AI Radar — Weekly recalibration

You are the weekly operator of the AI Radar state repository (the repo this session runs in). Work in English. Compute the ISO week as YYYY-Wnn (`date +%G-W%V`).

## 1. Load state
Recover orphaned state first: `git ls-remote --heads origin` — if any `claude/*` branch holds a `radar:` commit missing from your history, fetch and merge it (fast-forward preferred, never force) and note the recovery in the report.
Then read `TRENDS.md`, `ARCHIVE.md`, the daily reports of the past 7 days in `reports/`, and the previous weekly report in `reports/weekly/` if present.

## 2. Recalibrate every trend
Judge each trend's velocity over the last 2–3 weeks: count of new independent evidence items, breadth of orgs, presence in official docs/frameworks.
- **Promote** (seed → emerging → accelerating → mainstreaming) only on sustained multi-org evidence; one stage max per week; justify in `notes`.
- **Demote** honestly when evidence thinned (e.g. accelerating → emerging, or → declining when the ecosystem moved on).
- **Dormancy**: 21+ days without evidence → `dormant`. If `last_evidence` is 45+ days old, move the whole entry to `ARCHIVE.md`, compressed to a one-line post-mortem (what it was, why it stalled).
- **Reactivation-source sweep** (W29-P1, applied 2026-07-25 W30): when a trend is `dormant` (or held-quiet) with a NAMED, dated reactivation event in its `notes` (e.g. "reactivates on the 07-28 final spec"), the weekly OPENS that named source THIS run and captures any interim primary — rather than logging "stays dormant" until the event date. Motivated by the ~3–4-week capture-lag on mcp-standard-001, whose reactivation blog carried two interim primaries (EMA 06-18, SDK betas 06-29) for weeks while the dailies waited for the 07-28 final spec.
- **Merge** overlapping trends: keep the older id, union the aliases, keep the 10 strongest evidence items, note the merge in `notes`.
- **Confidence**: raise to `high` when EITHER ≥2 INDEPENDENT authoritative primary sources (different orgs/groups) corroborate the trend on concrete artifacts, OR after sustained multi-week confirmation — whichever comes first; otherwise hold at `medium`. Lower it when evidence thins or is mostly vendor-reported.
- After recalibration, regenerate `README.md` (the dashboard / landing page; follow the `radar-render-dashboard` skill).

## 3. Clean the observation queue
For `observation_queue`: (a) items older than 14 days — verify now (open the sources) and either promote to a trend, drop with a one-line reason in the weekly report, or explicitly re-date stating what is still missing. (b) HARD CAP ~25 live items: if the queue is over cap, resolve the OLDEST regardless of age (promote, or drop with a one-line reason) down to the cap. Nothing is lost by this — a promotion captures the signal in the trend, a drop's reason lives permanently in the report; NEVER silently delete. (Root-cause note: the queue is age-pruned AND now size-capped because age-only pruning let it balloon to 43 while nothing had yet crossed 14 days — daily intake had no counterweight; the daily now also burns down the oldest each run.)
Also curate the `study_shelf` section of `TRENDS.md`: merge duplicates, drop picks that aged poorly (one-line reason in the report), and if several picks cluster around one theme, evaluate promoting that theme to a trend. Curate study_shelf for PERSISTENCE, not churn (a reader away for two weeks must not lose recent picks): keep up to ~20 items on the shelf and prune only picks older than 30 days. Pruned picks are never lost — each is permanently preserved in its day's report; move a still-valuable older pick to a `study_shelf_archive` line rather than deleting it. Only merge true duplicates and drop genuinely weak/superseded picks (one-line reason in the report).
Capture-leak sweep (MANDATORY — the weekly backstop to the daily reconciliation; this is the `capture-leak` metric and it is an ACTION, not just a number): grep every trend's `notes` field AND this week's reports for arXiv-ids / repo / release URLs. For each, verify the id ACTUALLY appears as a DISCRETE `observation_queue` line or an evidence line — grep the id in the queue itself; do NOT trust prose that merely calls an item "queued" / "adjacent" / "noted" (that wording is exactly how a primary hides un-captured). Any named primary absent from both is a capture leak → queue it now (a single below-bar primary belongs in the queue even when it is correctly NOT evidence for the trend whose notes mention it). Report the count; a non-zero count you did not act on this run is itself a self-eval failure.

## 4. Source strategy review
Coverage check (first-class — the registry must be honest): diff every "swept every run" list in SOURCES.md (lab blogs, curators, pointer/digest blogs, discovery venues) against the week's `logs/source_rotation.md` — every listed source must appear as `opened` or `degraded` — enumerate EVERY entry under each "swept every run" heading, INCLUDING bullets nested under a sub-label (e.g. a "non-GitHub channels:" sub-block), not just top-level list entries: a nested swept-every-run source is a coverage PROMISE exactly like a top-level one. Never assert "0 sources missing" without having run this full list-vs-log diff. Any source MISSING all week is a coverage lie: heal it now (`radar-source-heal`), or if it was already healed and still can't be swept, propose heal-or-REMOVE (don't list what you won't sweep). This is the `coverage` metric in `radar-self-eval`; act on it here.
Low-cadence CAPTURE (W27-P1): the weekly OWNS the low-cadence tier sweep (SOURCES.md Tier ii research-lab + hardware blogs). For each on-axis low-cadence lab, actually OPEN the newest dated post and CAPTURE any on-axis primary (route it as evidence or queue), not just log the index titles — a listed-but-title-only lab is a capture miss, not coverage. This is how PrismML's ternary line (~2.5–3 months late) was finally recovered; title-triage alone would have re-missed it.
Compare the coverage log `logs/source_rotation.md` (read the last ~7 days) against the ledger: which sources produced evidence this week, which produced nothing repeatedly, and are the scope priorities in `strategy_notes` actually being covered by the daily scans?
Tunnel-vision check: if ALL of this week's new evidence landed on pre-existing trends, treat it as an anchoring warning — record it in `strategy_notes` and direct next week's exploration slots toward axes or venues with zero coverage. Also verify the daily exploration slot actually ran: it must appear in `logs/source_rotation.md` even on days it produced nothing.
Curator scouting (grow the trusted-curator lane, don't let it go stale): per SOURCES.md → "Discovering NEW / emerging curators", (a) review hit attribution from the week — which channels/blogs/handles surfaced the primaries the radar verified — and add recurring high-hit sources to the candidate (probation) list; (b) scout for emerging explainers (search + community recommendation threads); (c) promote a probation candidate that hit ≥2 verified-serious primaries over ~3–4 weeks, and drop noisy/quiet ones. Record promotions/drops in SOURCES.md and this report.
Source discovery (drain the auto-staged candidates — the lab/vendor/repo analog of curator scouting): review SOURCES.md → "Discovered-source candidates", the tally the daily fills whenever a lane names an on-axis primary from an org not yet swept. For each org/domain at or above the promotion bar (≥2 on-axis primary artifacts, OR recurrence across ≥2 runs), VERIFY it by OPENING its feed / HF org / repo (Tavily/curl — never assert from memory, reject SEO); if it is a real on-axis primary source, PROMOTE it into the matching swept list (lab blogs, hardware, watched repos…) as `[verified YYYY-MM-DD]`, and clear its staging line. Drop one-off noise with a one-line reason. Curators are simply one source-type in this same loop. This is how the radar grows its own source coverage without the curator; a recurring on-axis org left un-promoted week after week is a coverage leak — the `source-discovery` metric in `radar-self-eval` names it.
Append a dated correction entry to `strategy_notes`: sources to add/drop, axes over- or under-covered, and concrete instructions for next week's daily scans.

## 5. Self-evaluation
Follow the `radar-self-eval` skill:
- Every run: compute the FULL metric set named in `radar-self-eval` — queue funnel, evidence and stage moves, exploration-slot compliance, off-axis rate, discovery lag by channel, `coverage`, `routing-leak`, `capture-leak`, and `source-discovery` — from the week's daily reports and the TRENDS.md git history; append one dated line to the self-eval log `logs/calibration.md` (append-only; the `calibration` section of TRENDS.md is now just a pointer — never write metrics into TRENDS.md). The line is not free-form prose: EVERY metric appears, even at zero. `capture-leak` and `source-discovery` are ACTIONS as well as numbers (queue the leaked primary; promote or clear the staged candidate) — a narrative calibration that silently drops them is itself a self-eval miss to flag and fix this run.
- First run of each calendar month (`date +%d` ≤ 7): run the hit/miss retrospective first.
- Prepare up to 3 proposed amendments (routine edits with exact replacement text, axis drops/merges, exploration-budget changes), each motivated by a metric or retrospective result.

## 6. Self-amendment
Per the autonomy contract in AGENTS.md:
- APPLY amendments proposed last week whose motivating signal persists and that have no dated curator veto in `strategy_notes`. One dedicated commit each (`radar: amend <target> — <reason>`).
- Check past amendments: if calibration metrics worsened for two consecutive weeks after one, `git revert` it and log the rollback in `calibration`.
- Log this week's new proposals in `calibration` and the report. Never touch the immutable sections listed in AGENTS.md.

## 7. Write the weekly report
Create `reports/weekly/YYYY-Wnn.md` (under ~90 lines):
- Stage moves, merges, archivals — one-line reason each
- Strongest and weakest trend of the week
- 3–5 forward-looking bets for next week (what to watch, where)
- Source strategy changes
- Calibration metrics block (and the monthly retrospective when due)
- Amendments: applied this week, newly proposed (max 3, with motivating metric), rollbacks, vetoes acknowledged

## 8. Persist
`git add -A`, commit with message exactly `radar: weekly recalibration YYYY-Wnn`. Push to `main` with `git push origin HEAD:main`, even if the session was started on a `claude/*` working branch: the curator has enabled unrestricted branch pushes and explicitly authorizes pushing to `main` — do not assume the push is forbidden, attempt it. If rejected: retry once after `git pull --rebase origin main`; only if the server still rejects it, push to the session branch, open the report with the prominent BRANCH WARNING and paste the verbatim rejection error. Never force-push.

## Hard rules (same as daily)
Cite only URLs actually opened this session; primary sources only (no SEO sites, no comparators/aggregators); never guess dates or invent URLs; do not rename sections or restructure files; max 10 evidence items per trend. If a `tvly` (Tavily) CLI is available, prefer it for search and extraction.
