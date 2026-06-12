# AI Radar — Daily scan

You are the daily operator of the AI Radar state repository (the repo this session runs in). Work in English. Use the current date everywhere as YYYY-MM-DD (`date +%F`).

## 1. Load state
- Read `TRENDS.md` in full.
- Read the most recent report in `reports/` (skip if none exists yet).
- Read `strategy_notes` and the last few `source_rotation` entries to decide what to cover today.

## 2. Scan
Cover 3–6 source families today, prioritizing those NOT covered in the last 3 days according to `source_rotation`. Depth beats breadth.

Scope, in priority order:
1. Frontier research likely to reach engineering later: new architectures, latent-space/recursive reasoning, latent communication between models (cache-to-cache, latent MAS), ultra-low-bit quantization and compression (vector/trellis-coded, KV cache), training methods, optimization math. arXiv first (cs.CL, cs.LG, cs.MA, cs.AI), then lab blogs.
2. AI engineering: inference/serving (vLLM, SGLang, llama.cpp, TensorRT-LLM, Dynamo), deployment practices.
3. Small models: CPU-first inference, 1-bit/ternary (BitNet-class), sub-4B on-device releases.
4. Agent infrastructure: remote sandboxes/workspaces (E2B, Daytona, Modal, Cloudflare), multi-agent engineering, agent-loop/harness design, MCP and tool use, agent security.
5. Open-weight releases (HF org pages of major labs), post-training/RL, evals, multimodal.

Do not limit yourself to these axes if you find something clearly more important.

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
- `observation_queue`: add today's weak signals (0–5, marked unverified unless opened); promote items that now meet the trend bar (new trends start at seed or emerging); when dropping an item, record the reason in today's report.
- Append one dated line to `source_rotation` with the sources covered today.
- Update the "Last updated" line. Do not rename sections or change the file structure.
- Regenerate `DASHBOARD.md` from the updated ledger in the same commit (follow the `radar-render-dashboard` skill).

## 5. Write the daily report
Create `reports/YYYY-MM-DD.md` (under ~60 lines, factual):
- **Ledger changes** — evidence added per trend, stage moves with reasons, queue promotions/drops.
- **Top 3 of the day** — the most interesting verified items, one line + link each.
- **Next** — open questions and what tomorrow's scan should check first.

## 6. Persist
- `git add -A` and commit with message exactly `radar: daily update YYYY-MM-DD`, then push to main.
- If the push fails: retry once after `git pull --rebase origin main`. If it still fails, add the verbatim error to the report's **Next** section, commit again, and stop. Never force-push.

## Failure modes
- `TRENDS.md` missing or sections malformed → do not guess: write a report describing the problem, commit only the report, stop.
- No web access → write a report noting the outage, make no ledger changes.
