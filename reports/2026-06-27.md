# Daily report — 2026-06-27

Daily run (first of the day; the W26 weekly recalibration also ran earlier today — this is the
daily scan on top of it). FULL CHECK across all mandatory lanes. Focus: the W26 DORMANCY-WATCH
priority (mcp/pd-disagg/sandbox/small-cpu/latent-comm all at last_evidence 06-11) and the
Liquid AI small-models gap.

## Ledger changes
- **small-cpu-models-008** (pinned, dormancy refresh, last_evidence 06-11 → 06-26; no stage move):
  added TWO independent on-axis primaries. (1) Google Research **"Accelerating Gemini Nano with
  frozen Multi-Token Prediction"** (research.google, 06-26) — retrofits MTP onto a FROZEN Gemini
  Nano v3 for drafter-free on-device speculative decoding, shipped on Pixel 9/10. (2) **Liquid AI
  LFM2.5-230M** (HF, 06-26) — a sub-1B hybrid on-device model with native GGUF/ONNX/MLX edge
  distribution (closes the W26-flagged Liquid AI gap). Dormancy threat (was ~07-02) cleared.
- **agent-sandbox-007** (dormancy refresh, last_evidence 06-11 → 06-22; no stage move): added
  **AWS Lambda MicroVMs** (official AWS blog, 06-22; resurfaced on HN today, 323 pts) — a new
  serverless Firecracker-microVM primitive for "user- or AI-generated code", per-session VM
  isolation + snapshot resume. A FIFTH vendor and the FIRST hyperscaler on the agent-sandbox
  primitive — validates the category beyond startups/platform-SDKs.
- **observation_queue** (intake added): (a) PULSE/earthquake note — OpenAI GPT-5.6 "Sol" preview +
  U.S.-gov vetting of GPT-5.6 users + U.S. allowing Anthropic Mythos to "trusted" US orgs
  (closed-model + policy, off-axis, never evidence); (b) DeepSeek-V4-DSpark capture — card says
  "not a new model" (a speculative-decoding module on the existing V4 checkpoint), so NOT
  open-weight-003 evidence; (c) exploration intake CARVE linear attention (2606.27229) + curator-named
  Baidu Unlimited OCR R-SWA (constant-KV sliding-window attention, primary id unpinned) — both
  below-bar subquad-attn-012 corroboration.
- Source-discovery: staged `aws.amazon.com/blogs` (1 hit) for the weekly to verify.

## Top 3 of the day
1. **AWS Lambda MicroVMs** — a hyperscaler ships a first-party Firecracker agent-sandbox primitive
   for user/AI-generated code: https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/
2. **Gemini Nano frozen-MTP** — drafter-free on-device multi-token prediction now on Pixel 9/10:
   https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/
3. **Liquid AI LFM2.5-230M** — sub-1B hybrid on-device model, native GGUF/ONNX/MLX:
   https://huggingface.co/LiquidAI/LFM2.5-230M

## Study picks
- Gemini Nano frozen-MTP (Google Research) — the practical face of edge speculative decoding without
  a separate drafter; pairs with small-cpu-models-008.
- AWS Lambda MicroVMs — reference design for an agent-code execution layer (isolation, fast resume,
  statefulness) now first-party at a hyperscaler.

## Next
- **vLLM v0.24.0 GA gate** is UNCONFIRMED this run (release page JS-only, GitHub API body null, atom
  content unparsed) — re-read the v0.24.0 notes next run for turboquant-benchmark / native M3 / GLM-5.2
  support (the standing lowbit-quant-011 + open-weight-003 + subquad-attn-012 gates).
- **Remaining dormancy watch** (last_evidence 06-11, cross ~07-02): mcp-standard-001, pd-disagg-002,
  latent-comm-010 (pinned) — refresh or honestly mark dormant.
- **Follow the Baidu Unlimited OCR R-SWA primary** (via alphamatch's link) to pin its arXiv id and
  decide subquad-attn-012 routing.
- Watch whether native speculative-decoding modules (DeepSeek DSpark) / frozen-model MTP land in a
  serving engine (serving-stack-absorption signal).

---

# Pass 2 (2026-06-27, ~09:35 UTC)

FULL CHECK ~45 min after Pass 1. Triage of all mandatory lanes found nothing new since Pass 1
EXCEPT the item that defined this pass: chasing the W26/Pass-1 "vLLM v0.24.0 GA gate" Next-item
through the vLLM ENGINE BLOG (blog.vllm.ai) — a primary lane the radar had NOT been sweeping
(it watched `releases.atom`, not the blog) — surfaced three official engineering posts that fire
long-standing pre-registered serving-engine gates. All three opened/verified this session.

## Ledger changes
- **subquad-attn-012 — PROMOTED seed → emerging.** Gate fired: vLLM ships day-0 FIRST-CLASS native
  MiniMax-M3 support **including the MiniMax Sparse Attention (MSA) kernel** (+ model parsers, EAGLE3),
  not recipe-only — "MiniMax M3 in vLLM: Day-0 Serving" (blog.vllm.ai, 2026-06-12). Added as evidence.
  One move only (kernel for ONE model's MSA, not a general abstraction); last_evidence stays 06-16
  (blog is 06-12 → gate-driven move, not recency).
- **diffusion-lm-013 — PROMOTED emerging → accelerating.** Gate fired on two conditions at once:
  vLLM natively supports DiffusionGemma via a custom `DiffusionSampler` + reusable `ModelState`
  abstraction AND publishes `vllm bench serve` throughput on H100/H200 — "DiffusionGemma: The First
  dLLM Natively Supported in vLLM" (blog.vllm.ai, 2026-06-10). Added as evidence; last_evidence
  stays 06-24 (backfill).
- **lowbit-quant-011 — evidence add (no stage move).** The named "vLLM turboquant benchmarked-release"
  gate fired: "A First Comprehensive Study of TurboQuant" (blog.vllm.ai, 2026-05-11) benchmarks 4
  turboquant KV-quant variants vs BF16/FP8 on 2×H100. **Honest finding:** TurboQuant underperforms
  both baselines on throughput/latency; its only win is memory capacity (~5× burst-TTFT improvement
  via compressed KV-cache). Backfill (05-11), no recency refresh; stays accelerating, confidence medium.
- **open-weight-003 — note (no move).** The standing serving-stack-absorption stage-gate fired for its
  first model (M3 now first-class native in vLLM). Stays accelerating, NOT mainstreaming: only one model
  (GLM-5.2 native serving still unfired — no vLLM blog post, only GLM-4.5).
- **observation_queue:** added (a) the serving-engine gate-sweep record + root-cause; (b) UltraQuant
  (2606.20474) — capture-leak closure (called "queued" in lowbit notes but never actually in queue).
  Dropped 1 redundant provenance line (06-13 DeepMind diffusion, superseded by diffusion-lm-013 evidence).
- **SOURCES.md:** added an "Engine BLOGS (swept every run)" lane — root-cause fix for the multi-week miss.

## Capture-leak sweep
capture-leak: 89 ids checked / 1 queued (UltraQuant 2606.20474; the other flag, 2606.15007, is the
Nemotron tech-report ref of an already-cited evidence item — no separate capture needed).

## Top 3 of the day (Pass 2)
1. **vLLM ships MiniMax Sparse Attention natively (day-0 M3)** — the serving-engine sparse-attention
   kernel the radar had been waiting on: https://blog.vllm.ai/2026/06/12/minimax-m3-vllm.html
2. **DiffusionGemma natively served in vLLM** — first dLLM with a native diffusion sampler in a major
   serving engine, with engine-measured throughput: https://blog.vllm.ai/2026/06/10/diffusion-gemma.html
3. **TurboQuant benchmarked in vLLM** — production numbers show low-bit KV-quant is a capacity lever,
   not a speed win: https://blog.vllm.ai/2026/05/11/turboquant.html

## Study picks (Pass 2)
- TurboQuant vLLM study — when (and when not) to reach for low-bit KV-cache quant in serving.
- DiffusionGemma-in-vLLM — what serving a non-autoregressive LM actually requires (sampler + ModelState).

## Next
- **Sweep blog.vllm.ai every run now** (new SOURCES.md lane) — and find its Atom feed (likely /feed.xml).
- **vLLM v0.24.0 GA changelog still UNREAD** (page JS-only, REST API blocked via proxy, atom CDATA
  truncated) — heal a working access path next run; confirm whether GA bundles the M3/MSA + DiffusionGemma
  + turboquant support documented on the blog.
- **GLM-5.2 native serving** — watch blog.vllm.ai for a GLM-5.2 post (would move open-weight-003 toward
  mainstreaming and add a 2nd-mechanism datapoint to subquad-attn-012's DSA side).
- **Remaining dormancy watch** (last_evidence 06-11, cross ~07-02): mcp-standard-001, pd-disagg-002,
  latent-comm-010 (pinned) — refresh or mark dormant. (Note: pd-disagg-002 may have an engine-blog
  datapoint too — check blog.vllm.ai for P/D-disaggregation posts next run.)
