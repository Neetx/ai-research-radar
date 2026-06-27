# AI Radar

![trends](https://img.shields.io/badge/trends-15-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-6-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-43-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--27-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-27) — daily Pass 2:**
- **Two promotions from a serving-engine BLOG sweep the radar had been missing.** Chasing the vLLM gate through [blog.vllm.ai](https://blog.vllm.ai/) (not just release notes) surfaced three official posts firing pre-registered gates: [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) **seed → emerging** (vLLM ships a [native MiniMax Sparse Attention kernel](https://blog.vllm.ai/2026/06/12/minimax-m3-vllm.html)) and [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) **emerging → accelerating** ([DiffusionGemma natively served in vLLM](https://blog.vllm.ai/2026/06/10/diffusion-gemma.html) with a native sampler + benchmarks).
- **[⭐ Low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) — benchmarked-release gate fired (no stage move).** vLLM's [comprehensive TurboQuant study](https://blog.vllm.ai/2026/05/11/turboquant.html) benchmarks KV-quant vs BF16/FP8 — honest finding: it's a memory-capacity lever (~5× burst-TTFT), *not* a throughput win.
- **[Open-weight frontier MoE](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) absorption gate fired for its first model** (M3 now first-class native in vLLM); stays accelerating, not mainstreaming (GLM-5.2 native serving still unfired).
- **Capture-leak closure:** UltraQuant ([2606.20474](TRENDS.md#observation_queue)) was called "queued" in notes but never actually in the queue — queued for real. `capture-leak: 89 ids checked / 1 queued`.

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-26](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |

## Trends

🌱 2 · 📈 7 · 🚀 6 · 🌊 0 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-06-24](https://arxiv.org/abs/2606.25331) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🚀 accelerating | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-26](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-22](https://sakana.ai/fugu-release/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 emerging | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌱 seed | [2026-06-23](https://arxiv.org/abs/2606.24775) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-06-23](https://arxiv.org/abs/2606.24530) |

## Worth studying

- [A First Comprehensive Study of TurboQuant (vLLM)](https://blog.vllm.ai/2026/05/11/turboquant.html) — the vLLM team's honest production benchmark of TurboQuant KV-cache quantization vs BF16/FP8 on 2×H100: low-bit KV-quant is NOT a throughput/latency win (FP8 matches BF16 at negligible cost); TurboQuant only pays off as a memory-CAPACITY lever, cutting burst TTFT ~5×. Read before reaching for KV-quant in serving — it tells you exactly when the trade is worth it
- [DiffusionGemma: The First dLLM Natively Supported in vLLM](https://blog.vllm.ai/2026/06/10/diffusion-gemma.html) — vLLM's engineering writeup of integrating a discrete-diffusion LM into an autoregressive-first engine via a native `DiffusionSampler` + reusable `ModelState`, with `vllm bench serve` throughput on H100/H200; the reference for what serving a non-autoregressive LM actually requires, and the first sign diffusion decoding is becoming a first-class serving mode
- [Accelerating Gemini Nano with frozen Multi-Token Prediction](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) — Google Research's practical on-device acceleration: retrofit MTP onto a FROZEN production model (Gemini Nano v3) so one model both generates and self-drafts — speculative-decoding-style speedups WITHOUT a separate drafter, now on Pixel 9/10; the clearest sign that speculative decoding is becoming a drafter-free on-device default
- [AWS Lambda MicroVMs](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) — the first hyperscaler-native agent-sandbox primitive: per-session Firecracker microVMs (VM-level isolation) with image-then-launch snapshot resume for user/AI-generated code; the reference for what an agent-code execution layer needs (isolation, fast resume, statefulness)
- [The Verification Horizon: No Silver Bullet for Coding Agent Rewards](https://arxiv.org/abs/2606.26300) — a 12-author (Alibaba/Qwen-line) result inverting a load-bearing assumption of agentic RL: "verifying is easier than producing" is breaking down for coding agents — generating complex solutions outpaces our ability to verify them, so reward *verification* becomes the bottleneck; read before trusting any verifiable-reward / RLVR pipeline
- [iLLaDA-8B (Improved Large Language Diffusion Models)](https://huggingface.co/GSAI-ML/iLLaDA-8B-Base) — RUC/GSAI-ML's open-weights (Apache-2.0, paper 2606.25331) 8B fully-bidirectional masked-diffusion LM trained from scratch on 12T tokens: the clearest "diffusion LM at autoregressive quality" datapoint — its card ties autoregressive Qwen2.5-7B (63.9 vs 63.3); the third independent open diffusion base model on the diffusion-lm-013 line
- [Thinking to Recall: How Reasoning Unlocks Parametric Knowledge in LLMs](https://research.google/blog/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms/) — Google Research: why a reasoning trace helps an LLM recall even *simple* single-hop facts — a *computational buffer* (reasoning tokens as latent computation) and *factual priming* — so reasoning expands the parametric-knowledge boundary; the hook is process rewards on factually-supported steps to cut hallucination
- [Qwen-AgentWorld (35B-A3B language world model)](https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B) — Alibaba/Qwen's open-weights (paper 2606.24597) "native language world model": a 35B-A3B MoE where *predicting the next environment state* from an agent's action+history IS the objective from CPT onward; a runnable bridge between world models and agent infrastructure — a learned *simulator of agentic environments*
- [Prompt Injection as Role Confusion](https://arxiv.org/abs/2603.12277) — Ye/Cui/Hadfield-Menell (MIT, ICML 2026): the cleanest mechanistic *theory* of why prompt injection works — LLMs infer who is speaking from how a span *sounds*, not its labeled `<user>`/`<tool>` role; study it (with role-confusion.github.io) for "role probes", why label-based defenses are brittle, and as the underpinning of the architectural/least-privilege turn
- [Sakana Fugu: A Multi-Agent Orchestration System as a Foundation Model](https://sakana.ai/fugu-release/) — Sakana AI's product: a small LM TRAINED to orchestrate a pool of frontier LLMs (choosing/switching models, recursive self-calls for test-time scaling) behind one API; the clearest example of "orchestration-as-a-model" vs orchestration-as-a-framework. Benchmarks are vendor-claimed.
- [Looped World Models (LoopWM)](https://arxiv.org/abs/2606.18208) — the first looped-transformer architecture for *world modelling*: a parameter-shared block iteratively refines the latent environment state with adaptive compute (~100× parameter efficiency, less long-horizon drift); the looped/recursive-computation idea crossing into world simulation
- [DiffusionGemma (26B-A4B discrete-diffusion MoE)](https://huggingface.co/google/diffusiongemma-26B-A4B-it) — Google DeepMind's open-weights (Apache-2.0) discrete-diffusion LM: an encoder-decoder Gemma-4 MoE that denoises whole blocks of tokens ("canvases") instead of decoding left-to-right for ~4× faster generation; pair with Sumi + iLLaDA for the diffusion-lm-013 line

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named. (Latest daily intake: 2026-06-27.)

- **The earthquake is closed-model + policy:** OpenAI previewed [GPT-5.6 "Sol"](https://news.ycombinator.com/) (a next-gen model) and the [U.S. government will vet who can use it](https://news.ycombinator.com/) (top HN, ~1000 pts), while the U.S. [allowed Anthropic to release Mythos to "trusted" U.S. organizations](https://news.ycombinator.com/) — a partial reopening of the 06-12 export-control shutdown. Government-gated frontier-model access is hardening into a pattern (off every tracked axis; recorded so the ledger reflects that the ground moved).
- On-axis on the [HN](https://news.ycombinator.com/) front page: ["AWS Lambda introduces microVMs"](https://news.ycombinator.com/) (~328 pts → routed to agent-sandbox-007 as evidence) and a "gap between open-weight and closed LLMs" discussion (~202 pts, intake).
- Degraded: the [code4AI](https://www.youtube.com/@code4AI) YouTube curator lane remains IP-blocked end-to-end (not re-attempted per the standing heal note); coverage falls back on the HN/HF-papers overlap. Pointer/digest blogs (Interconnects, Simon Willison, alphamatch) swept and clean.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (43)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-27](reports/2026-06-27.md) · weekly: [2026-W26](reports/weekly/2026-W26.md) · conventions: [AGENTS.md](AGENTS.md)
