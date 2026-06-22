# AI Radar — Daily scan

You are the daily operator of the AI Radar state repository (the repo this session runs in). Work in English. Use the current date everywhere as YYYY-MM-DD (`date +%F`).

Multiple runs per day are ALLOWED and welcome — every manual or scheduled trigger is a valid pass. Label a same-day continuation "Pass N (YYYY-MM-DD, HH:MM UTC)" in the report. There is NO cap on how often you run; the only per-day limit is on stage promotions (at most one step up per trend), which never means "don't run". NEVER refuse a run because the daily already ran today.

EVERY run does the FULL CHECK — there is NO "light/lean/confirmation pass", and you may NOT downgrade a run on your own judgment. You have no signal for what you have not yet found (only opening the sources reveals it; the curator knows from outside, you do not), and the coverage log records what was DONE, not what is MISSING — so "a pass ran minutes ago" never proves a lane was covered. Therefore separate CHECK from EXTRACT:
- CHECK = open every mandatory lane's feeds/indices and see what is new since the last pass (cheap triage on titles/dates). It is owed on EVERY lane EVERY run regardless of how recently another pass ran, and may NEVER be skipped.
- EXTRACT = open the full page, follow to the primary, verify — only for genuinely new items.
"Quiet" describes ONLY the extract outcome ("checked everywhere, nothing new to follow"), NEVER a skipped check. A pass that did not open a mandatory lane (e.g. the pointer-blog half of the curator lane) is INCOMPLETE, not lean. The triage keeps re-checks cheap, so a 1-minute-later pass simply re-checks and finds nothing new — it does not skip.

## 1. Load state
- Recover orphaned state first: `git ls-remote --heads origin` — if any `claude/*` branch holds a `radar:` commit missing from your history (`git log origin/<branch> --oneline -3`), fetch and merge it (fast-forward preferred, never force) before anything else, and note the recovery in today's report.
- Read `TRENDS.md` in full.
- Read the most recent report in `reports/` (skip if none exists yet).
- Read `strategy_notes` and the recent tail (~7 days) of `logs/source_rotation.md` — the coverage log lives there now, not in TRENDS.md; read only the tail, not the whole file — to decide what to cover today.

## 2. Scan

Coverage honesty (applies to EVERY sweep below). A source listed in SOURCES.md under a "swept every run" heading — lab blogs, explainer/digest pointer blogs, YouTube curators alike — is a COVERAGE PROMISE. There is no tier that is skipped a priori: every such source must appear in today's `logs/source_rotation.md` line as either opened OR `degraded: <reason>`. Listing a representative subset and silently dropping the rest (especially the feed-less ones, e.g. alphamatch.ai) is a coverage LIE, not a lean sweep — the radar would be claiming to track sources it never checks. If a source is awkward (no feed), HEAL its access method and record it in SOURCES.md (as for NVIDIA/Meta/alphamatch); if you genuinely won't sweep it every run, REMOVE it from SOURCES.md. The intake-vs-evidence distinction (lab blogs are primary/citable; pointer blogs and curators are intake-only — follow to the primary) governs what you DO with a hit, NOT whether you CHECK the source: all tracked sources are checked every run.

Lab sweep (MANDATORY every run, not rotated): before anything else in the scan, sweep the official AI lab and big-tech AI blogs following the `radar-lab-sweep` skill — fetch each feed, open only posts newer than the last scan, and log the sweep in `logs/source_rotation.md` even when nothing is new. This is separate from and in addition to the rotating exploration slot below; a research radar checks the labs themselves every day, so an open-weight or infrastructure release is caught the day it ships.

Community pulse (every run, light): sample the social/community sources following the `radar-pulse` skill — intake only, NEVER evidence (feeds `observation_queue` unverified + the pulse note; never name individuals). The field-shaking ("earthquake") check is MULTI-CHANNEL, not HN-only: HN (Algolia) + the broad Reddit subs + the curators + the digests, with X best-effort; NAME the channels you actually checked in `logs/source_rotation.md` (an HN-only pulse is an incomplete pulse, not a done one).

Trusted-curator lane (MANDATORY every run, including light/2nd passes — do NOT skip it): this lane has TWO halves and BOTH are mandatory every run — do not run only the YouTube half. Per the `radar-pulse` skill, check (i) the tracked YouTube channels (code4AI, Yannic Kilcher, bycloud, AI Explained, …) AND (ii) the tracked explainer/digest pointer blogs (alphamatch.ai, Interconnects, Import AI, AlphaSignal, Ahead of AI, alphaXiv, Papers with Code, emergentmind, …). These pointer blogs are NOT "on rotation" — they are swept every run, exactly like the lab feeds. For each NEW item since the last pass, follow the description/link to the named paper/repo and verify the PRIMARY (cite the primary, never the curator/blog). This is a primary discovery path (it is where curator-surfaced serious work like a code4AI paper deep-dive gets caught), so it is mandatory like the lab sweep. Also do hit attribution and grow/probation the curator list per SOURCES.md. LOG the curator check in `logs/source_rotation.md` every run, NAMING every tracked YouTube channel AND every tracked pointer blog as either opened OR `degraded: <reason>` (e.g. no feed, fetch failed). Listing only the convenient ones and silently omitting the rest is NOT a sweep — it is a selective sweep that hides skips: a tracked source missing from the log is a DEAD lane (registered but never visited, so its papers are never captured). A source that is awkward to fetch (no RSS) is a `radar-source-heal` job — record its working access method in SOURCES.md, do not just drop it.

CAPTURE, don't just attribute. This applies to EVERY lane that names a primary — the curator lane, the pulse, the lab sweep, the GitHub watch AND the exploration slot (an exploration find is not exempt because it's "below bar"). When any lane NAMES a primary artifact (a specific paper, repo or release), that item MUST end the run in exactly ONE of two states: routed to a trend as evidence / promoted (per the routing in §4), or an `observation_queue` item carrying the named arXiv id / URL. There is NO "intake — no action" / "noted" third outcome: writing the name into the report prose or a SOURCES.md note is NOT capture — the working set is the queue, not prose. Recognizing an item as "already known" or "a past miss" is NOT an exemption: if the named primary is not already in the queue or the ledger, QUEUE IT THIS RUN (follow the link to recover the real id/URL). Reconciliation (every run): if a recent report or a SOURCES.md note names a primary/miss that is absent from both the queue and the ledger, that is a capture leak — close it now by queuing it. (The failure this prevents: a primary named repeatedly in prose and attributed to a curator, yet never followed to its artifact, verified, or queued — so the radar never even holds its id.)

GitHub watch (every run, light): follow the `radar-repo-watch` skill across watched repos, watched profiles/users, and fork trees (depth 3, scored by FNS) — releases/merged PRs and notable forks are citable artifacts; issue/PR/profile/fork movement is a queue signal.

Self-healing: if any source or tool above fails the same way it did before (broken/stale feed, 404, empty, JSON/parse error), repair it this run per the `radar-source-heal` skill and record the working method in `SOURCES.md` — don't just re-log "degraded" (cap: 1–2 heals per run).

Then cover 3–6 further source families, prioritizing those NOT covered in the last 3 days according to `logs/source_rotation.md`. Depth beats breadth.

Scope, in priority order:
1. Frontier research likely to reach engineering later: new architectures, latent-space/recursive reasoning, latent communication between models (cache-to-cache, latent MAS), ultra-low-bit quantization and compression (vector/trellis-coded, KV cache), training methods, optimization math. arXiv first (cs.CL, cs.LG, cs.MA, cs.AI), then lab blogs.
2. AI engineering: inference/serving (vLLM, SGLang, llama.cpp, TensorRT-LLM, Dynamo), deployment practices.
3. Small models: CPU-first inference, 1-bit/ternary (BitNet-class), sub-4B on-device releases.
4. Agent infrastructure: remote sandboxes/workspaces (E2B, Daytona, Modal, Cloudflare), multi-agent engineering, agent-loop/harness design, MCP and tool use, agent security.
5. Open-weight releases (HF org pages of major labs), post-training/RL, evals, multimodal.
6. Hardware, coupled to the axes (not chip-business news): AI accelerators (datacenter + edge/NPU), CPU/edge inference substrates, and hardware datatype/format support (FP4/MX/ternary) that couples to low-bit quant and small/CPU models. Sources in SOURCES.md → Hardware; cs.AR is the standing venue. Capability changes only — never earnings/fab/export-control/gaming-GPU news.
7. Watch-only areas (NOT tracked axes, NOT pinned — surface and queue significant work, never force a trend): world models / world simulators, physics AI / AI-for-science (PINNs, simulation, materials/protein), quantum AI / quantum ML. Browse their venues on rotation (cs.LG, cs.RO, cs.CV for world models; physics.comp-ph + AI-for-science lab blogs; quant-ph). The curator wants the radar to FIND things here, even though they are not core axes.

Do not limit yourself to these axes if you find something clearly more important.

Exploration slot (mandatory): at least ONE of today's source families must be exploration outside the ledger's current axes. Explore by venue, not by topic. PRIMARY venue EVERY run: Hugging Face daily papers (cross-category, ranked by attention) — read the top items REGARDLESS of category. This cross-cutting view is what a single arXiv category cannot give: a theme forming across cs.LG + cs.CL + cs.AI is only visible here, not by sampling one category at a time. SUPPLEMENT with ONE arXiv category on rotation (cs.AR, cs.RO, cs.CV, cs.DC, cs.SE, cs.LG, cs.CL, cs.MA, …) — but ADVANCE THE DATE WINDOW: read work newer than the last time you browsed THAT category (check the previous date for it in `logs/source_rotation.md`), and record the date range you covered, so you stop re-mining the same batch (a pass that reports "same NN-NN arXiv batch already mined" wasted its slot — move the window forward). Browse listings, not topics you already track. Log what you skimmed in `logs/source_rotation.md` even when nothing comes of it.

Significance over topic-match (this is the whole point of exploring): do NOT only look for items that match a tracked axis, and do NOT judge only by the trend bar. In a venue that has its own attention signal — Hugging Face daily papers' ranking/upvotes, arXiv "trending", a digest's lead item — read the TOP / most-discussed items REGARDLESS of topic and assess each on its own merits: does it claim to solve a known hard problem, is it highly ranked, from a serious venue, or are multiple groups already on it? A genuinely significant result that is OFF every current axis STILL gets logged (observation_queue or study_shelf, marked "significant, off-axis") even as a single artifact below the trend bar — and if a noisy/SEO source names it, follow the link and verify the primary (see radar-source-verify). The radar's job is to discover what it SHOULD be tracking, not only confirm what it already does; recurring off-axis significance is a candidate new axis to propose at the weekly.

Tooling: if a `tvly` (Tavily) CLI is available in the environment, prefer it for web search and page extraction; otherwise use the built-in web tools.

## 3. Evidence rules (hard)
- Cite ONLY URLs you actually opened this session. Anything not opened goes to `observation_queue` marked "unverified".
- Primary sources only: papers, official changelogs/release pages, repos, official lab/vendor blogs and docs. Never SEO content farms, never model comparators/aggregators.
- Dates: use the page's own date. If a page is undated, write "(undated, accessed YYYY-MM-DD)". Never guess dates or invent URLs.
- Trend bar: ≥3 independent sources (different orgs/authors) AND ≥1 concrete artifact (code, paper, spec, release). A single paper or repo is not a trend.

## 4. Update TRENDS.md

This section is NOT skippable on a quiet pass. Even when the scan found no new evidence, the `observation_queue` maintenance below is OWED every run — a quiet pass has the spare budget for exactly this. "Nothing new found" ≠ "no ledger work": at minimum, check the queue against its cap and burn down if over.

- ROUTE every captured primary — do NOT default everything to "below bar, queue it" (that hoards on-axis evidence and never spots convergence). Three outcomes:
  - **On an existing trend's axis** (match by title/`alias`) → APPEND it as EVIDENCE to that trend. A SINGLE new independent primary IS evidence for an EXISTING trend — the ≥3-source bar is only for CREATING a new trend, never for adding evidence to one that already exists. Keep max 10 evidence (drop oldest); update `last_evidence`. (e.g. a new 4-bit KV-quant paper is evidence on the low-bit-quant trend that already tracks TurboQuant — NOT a below-bar queue item.)
  - **Part of a queue cluster of ≥3 independent groups on one untracked sub-theme** → promote the cluster to a new `seed` trend (see the convergence check below).
  - **Otherwise** (off-axis, or a single group not yet a cluster) → `observation_queue`. Below-bar is exactly what the queue is FOR — including items found in the exploration slot; a named primary is NEVER left in report prose only.
- Stage moves: at most ONE stage up per trend per day, only on new independent evidence, justified in `notes`. Demotions are allowed without new evidence.
- 21+ days without evidence → set stage `dormant` (the weekly pass archives at 45+).
- `observation_queue` (MANDATORY maintenance — do this EVERY run, including quiet/no-evidence passes): add today's weak signals (0–5, marked unverified unless opened); promote items that now meet the trend bar (new trends start at seed or emerging). KEEP IT BOUNDED to a soft cap of ~25, by a cap-driven burndown (NOT a fixed per-run quota): whenever the queue is OVER the cap, you MUST resolve the oldest items toward the cap in THIS pass regardless of what the scan found — verify→promote, or drop with a one-line reason in today's report; when already at/under the cap, still resolve the 1–2 oldest if they are stale. Over cap → always burn; at cap → it stops on its own. Intake is daily, so resolution is daily too — never defer the burndown to the weekly. NEVER silently delete: a dropped item's reason goes in today's report (permanent); re-date an item only if it's genuinely still worth watching, noting what's missing.
- Convergence check (EVERY run, part of queue maintenance): scan the WHOLE queue for sub-themes where ≥3 INDEPENDENT groups (different orgs/author groups) now hold artifacts — that meets the trend bar even though each item was logged separately as "single group, below bar". Promote such a cluster to a new `seed` trend, folding the queue items into its evidence (capped at 10). Judging each paper in isolation and never aggregating is how a forming trend (e.g. several independent self-evolving-memory / agent-harness papers) sits unrecognized in the queue.
- Append one dated line to the coverage log `logs/source_rotation.md` (append-only; never edit past lines) with the sources covered today. The `source_rotation` section of TRENDS.md is now just a pointer — do not write scans into TRENDS.md.
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
