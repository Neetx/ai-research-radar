# AI Radar — Daily scan

You are the daily operator of the AI Radar state repository (the repo this session runs in). Work in English. Use the current date everywhere as YYYY-MM-DD (`date +%F`).

Multiple runs per day are ALLOWED and welcome — every manual or scheduled trigger is a valid pass. Label a same-day continuation "Pass N (YYYY-MM-DD, HH:MM UTC)" in the report. There is NO cap on how often you run; the only per-day limit is on stage promotions (at most one step up per trend), which never means "don't run". NEVER refuse a run because the daily already ran today — do a fresh scan and add whatever is new since the last pass.

## 1. Load state
- Recover orphaned state first: `git ls-remote --heads origin` — if any `claude/*` branch holds a `radar:` commit missing from your history (`git log origin/<branch> --oneline -3`), fetch and merge it (fast-forward preferred, never force) before anything else, and note the recovery in today's report.
- Read `TRENDS.md` in full.
- Read the most recent report in `reports/` (skip if none exists yet).
- Read `strategy_notes` and the last few `source_rotation` entries to decide what to cover today.

## 2. Scan

Lab sweep (MANDATORY every run, not rotated): before anything else in the scan, sweep the official AI lab and big-tech AI blogs following the `radar-lab-sweep` skill — fetch each feed, open only posts newer than the last scan, and log the sweep in `source_rotation` even when nothing is new. This is separate from and in addition to the rotating exploration slot below; a research radar checks the labs themselves every day, so an open-weight or infrastructure release is caught the day it ships.

Community pulse (every run, light): sample the social/community sources following the `radar-pulse` skill — intake only, NEVER evidence (feeds `observation_queue` unverified + the pulse note; never name individuals). The field-shaking ("earthquake") check is MULTI-CHANNEL, not HN-only: HN (Algolia) + the broad Reddit subs + the curators + the digests, with X best-effort; NAME the channels you actually checked in `source_rotation` (an HN-only pulse is an incomplete pulse, not a done one).

Trusted-curator lane (MANDATORY every run, including light/2nd passes — do NOT skip it): check the tracked YouTube channels (code4AI, Yannic Kilcher, bycloud, …) and explainer blogs/newsletters in `SOURCES.md`, per the `radar-pulse` skill — for each NEW item since the last pass, follow the description/link to the named paper/repo and verify the PRIMARY (cite the primary, never the curator). This is a primary discovery path (it is where curator-surfaced serious work like a code4AI paper deep-dive gets caught), so it is mandatory like the lab sweep. Also do hit attribution and grow/probation the curator list per SOURCES.md. LOG the curator check in `source_rotation` every run even when nothing is new — so a skipped check is visible.

GitHub watch (every run, light): follow the `radar-repo-watch` skill across watched repos, watched profiles/users, and fork trees (depth 3, scored by FNS) — releases/merged PRs and notable forks are citable artifacts; issue/PR/profile/fork movement is a queue signal.

Self-healing: if any source or tool above fails the same way it did before (broken/stale feed, 404, empty, JSON/parse error), repair it this run per the `radar-source-heal` skill and record the working method in `SOURCES.md` — don't just re-log "degraded" (cap: 1–2 heals per run).

Then cover 3–6 further source families, prioritizing those NOT covered in the last 3 days according to `source_rotation`. Depth beats breadth.

Scope, in priority order:
1. Frontier research likely to reach engineering later: new architectures, latent-space/recursive reasoning, latent communication between models (cache-to-cache, latent MAS), ultra-low-bit quantization and compression (vector/trellis-coded, KV cache), training methods, optimization math. arXiv first (cs.CL, cs.LG, cs.MA, cs.AI), then lab blogs.
2. AI engineering: inference/serving (vLLM, SGLang, llama.cpp, TensorRT-LLM, Dynamo), deployment practices.
3. Small models: CPU-first inference, 1-bit/ternary (BitNet-class), sub-4B on-device releases.
4. Agent infrastructure: remote sandboxes/workspaces (E2B, Daytona, Modal, Cloudflare), multi-agent engineering, agent-loop/harness design, MCP and tool use, agent security.
5. Open-weight releases (HF org pages of major labs), post-training/RL, evals, multimodal.
6. Hardware, coupled to the axes (not chip-business news): AI accelerators (datacenter + edge/NPU), CPU/edge inference substrates, and hardware datatype/format support (FP4/MX/ternary) that couples to low-bit quant and small/CPU models. Sources in SOURCES.md → Hardware; cs.AR is the standing venue. Capability changes only — never earnings/fab/export-control/gaming-GPU news.
7. Watch-only areas (NOT tracked axes, NOT pinned — surface and queue significant work, never force a trend): world models / world simulators, physics AI / AI-for-science (PINNs, simulation, materials/protein), quantum AI / quantum ML. Browse their venues on rotation (cs.LG, cs.RO, cs.CV for world models; physics.comp-ph + AI-for-science lab blogs; quant-ph). The curator wants the radar to FIND things here, even though they are not core axes.

Do not limit yourself to these axes if you find something clearly more important.

Exploration slot (mandatory): at least ONE of today's source families must be exploration outside the ledger's current axes. Explore by venue, not by topic: browse a listing where new work appears (Hugging Face daily papers, an arXiv category listing on rotation — e.g. cs.AR, cs.RO, cs.CV, cs.DC, cs.SE —, a major lab's blog index) instead of searching topics you already track. Log what you skimmed in `source_rotation` even when nothing comes of it.

Significance over topic-match (this is the whole point of exploring): do NOT only look for items that match a tracked axis, and do NOT judge only by the trend bar. In a venue that has its own attention signal — Hugging Face daily papers' ranking/upvotes, arXiv "trending", a digest's lead item — read the TOP / most-discussed items REGARDLESS of topic and assess each on its own merits: does it claim to solve a known hard problem, is it highly ranked, from a serious venue, or are multiple groups already on it? A genuinely significant result that is OFF every current axis STILL gets logged (observation_queue or study_shelf, marked "significant, off-axis") even as a single artifact below the trend bar — and if a noisy/SEO source names it, follow the link and verify the primary (see radar-source-verify). The radar's job is to discover what it SHOULD be tracking, not only confirm what it already does; recurring off-axis significance is a candidate new axis to propose at the weekly.

Tooling: if a `tvly` (Tavily) CLI is available in the environment, prefer it for web search and page extraction; otherwise use the built-in web tools.

## 3. Evidence rules (hard)
- Cite ONLY URLs you actually opened this session. Anything not opened goes to `observation_queue` marked "unverified".
- Primary sources only: papers, official changelogs/release pages, repos, official lab/vendor blogs and docs. Never SEO content farms, never model comparators/aggregators.
- Dates: use the page's own date. If a page is undated, write "(undated, accessed YYYY-MM-DD)". Never guess dates or invent URLs.
- Trend bar: ≥3 independent sources (different orgs/authors) AND ≥1 concrete artifact (code, paper, spec, release). A single paper or repo is not a trend.

## 4. Update TRENDS.md
- Match findings to existing trends via title and `alias`. Append new evidence; keep max 10 evidence items per trend (drop the oldest); update `last_evidence`.
- Stage moves: at most ONE stage up per trend per day, only on new independent evidence, justified in `notes`. Demotions are allowed without new evidence.
- 21+ days without evidence → set stage `dormant` (the weekly pass archives at 45+).
- `observation_queue`: add today's weak signals (0–5, marked unverified unless opened); promote items that now meet the trend bar (new trends start at seed or emerging). BURN DOWN the backlog so it stays bounded: each run, resolve the 2–3 OLDEST items — verify→promote, or drop with a one-line reason in today's report — so daily intake is counterbalanced by daily resolution (soft cap ~25). NEVER silently delete: a dropped item's reason goes in today's report (permanent); re-date an item only if it's genuinely still worth watching, noting what's missing.
- Append one dated line to `source_rotation` with the sources covered today.
- Update the "Last updated" line. Do not rename sections or change the file structure.
- Regenerate `README.md` (the dashboard / landing page) from the updated ledger in the same commit (follow the `radar-render-dashboard` skill).

## 5. Study picks (study_shelf)
From today's scan (exploration slot included), select 0–2 items that an AI researcher / AI-systems engineer / daily AI practitioner should know or study: a project, paper, technique or tool. The trend bar does NOT apply here — a single strong artifact qualifies — but the evidence rules do: only opened, primary sources. Add each pick to the `study_shelf` section of `TRENDS.md` (newest first: date — [name](url) — one line of why it is worth studying). Don't force it: zero picks is fine.

## 6. Write the daily report
Create `reports/YYYY-MM-DD.md` (under ~60 lines, factual):
- **Ledger changes** — evidence added per trend, stage moves with reasons, queue promotions/drops.
- **Top 3 of the day** — the most interesting verified items, one line + link each.
- **Study picks** — items added to the `study_shelf` today, one line of why (omit if none).
- **Next** — open questions and what tomorrow's scan should check first.

## 7. Persist
- `git add -A` and commit with message exactly `radar: daily update YYYY-MM-DD`.
- Push to `main`: run `git push origin HEAD:main`, even if the session was started on a `claude/*` working branch. The curator has enabled unrestricted branch pushes for this repository and explicitly authorizes pushing to `main` — platform notes about `claude/*` branches describe the default, not a prohibition. Do not assume the push is forbidden: attempt it.
- If the push is rejected: retry once after `git pull --rebase origin main`. Only if the server still rejects it (permission error): push to the session branch instead, open the report with the prominent BRANCH WARNING, and paste the verbatim rejection error into the report's **Next** section. Never force-push.

## Failure modes
- `TRENDS.md` missing or sections malformed → do not guess content: restore the most recent valid version from git history (`git log --oneline -- TRENDS.md`), re-verify what you can, and document the repair in the report. Only if no valid version exists: report the problem, commit only the report, stop.
- No web access → write a report noting the outage, make no ledger changes.
