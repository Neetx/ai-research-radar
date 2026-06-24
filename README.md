# AI Radar

![trends](https://img.shields.io/badge/trends-14-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-36-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--24-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-24):**
- **New evidence — [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards):** added [NatureBench](https://arxiv.org/abs/2606.24530) — can coding agents reproduce the published SOTA of Nature-family papers? A real-task, long-horizon agent benchmark and the fifth independent group on this axis in a week; `last_evidence` 06-22 → 06-23 (no stage move — still seed).
- **Watchlist capture (off-axis, world models):** [Qwen-AgentWorld-35B-A3B](https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B) — Alibaba/Qwen open-weights "native language world model" (paper #1 HF daily paper today) that simulates agentic environments by predicting the next state from an agent's action+history; queued as watch-area + added to the study shelf. Also queued [AOHP](https://arxiv.org/abs/2606.23449) + OpenRath → the agent-harness/runtime-infra cluster (flagged for weekly W26).
- **Watchlist 35 → 36** (3 captures, 2 stale 06-17 drops: NVIDIA low-precision-training blog, cs.DC serving cluster). No stage moves; no new trend.
- **Native-serving gates still unfired (2+ weeks)** across [open-weight](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs), [subquadratic attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) and [low-bit quant](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache): no native MiniMax-M3 / GLM-5.2 kernels or benchmarked vLLM `turboquant` release (vLLM v0.23.1rc0 / SGLang v0.5.13.post1 unchanged). tvly auth restored this run; YouTube curator feed still 404 — HN net covered the earthquake check.

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |

## Trends

🌱 3 · 📈 6 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🚀 accelerating | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-22](https://sakana.ai/fugu-release/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-06-23](https://arxiv.org/abs/2606.24530) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🌱 seed | [2026-06-17](https://arxiv.org/abs/2606.19005) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🌱 seed | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |

## Worth studying

- [Qwen-AgentWorld (35B-A3B language world model)](https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B) — Alibaba/Qwen's open-weights (paper 2606.24597, #1 HF daily paper today) "native language world model": a 35B-A3B MoE where *predicting the next environment state* from an agent's action+history IS the objective from the CPT stage onward, across seven agent-interaction domains; study it as a runnable bridge between world models and agent infrastructure — a learned *simulator of agentic environments* (adjacent to verifiable-RL-environments), not a video/physics world model
- [Prompt Injection as Role Confusion](https://arxiv.org/abs/2603.12277) — Ye/Cui/Hadfield-Menell (MIT, ICML 2026): the cleanest mechanistic *theory* of why prompt injection works — LLMs receive one flat text stream and infer who is speaking from how a span *sounds*, not its labeled `<user>`/`<tool>` role, so injected text that "sounds like" the user hijacks the agent regardless of its real source; study it (with role-confusion.github.io) for "role probes", why label-based defenses are brittle, and as the underpinning of the architectural/least-privilege turn
- [Sakana Fugu: A Multi-Agent Orchestration System as a Foundation Model](https://sakana.ai/fugu-release/) — Sakana AI's commercial product (Ultra release 06-22, beta 04-24): a small LM TRAINED to orchestrate a pool of frontier LLMs — choosing/switching models per task and even calling itself recursively for test-time scaling — behind one API; the clearest example of "orchestration-as-a-model" (vs orchestration-as-a-framework), the product form of Sakana's collective-intelligence line. Benchmarks are vendor-claimed.
- [Looped World Models (LoopWM)](https://arxiv.org/abs/2606.18208) — the first looped-transformer architecture for *world modelling*: a parameter-shared block iteratively refines the latent environment state with adaptive compute (~100× parameter efficiency, less long-horizon drift); the looped/recursive-computation idea (LoopCoder-v2/LT2) crossing into world simulation
- [DiffusionGemma (26B-A4B discrete-diffusion MoE)](https://huggingface.co/google/diffusiongemma-26B-A4B-it) — Google DeepMind's open-weights (Apache-2.0) discrete-diffusion LM: an encoder-decoder Gemma-4 MoE that denoises whole blocks of tokens ("canvases") instead of decoding left-to-right (multi-canvas, block-autoregressive) for ~4× faster generation; the clearest production-scale example of a *non-autoregressive* open LM — pair with Sumi for the line now seeded as diffusion-lm-013
- [Beyond Static Leaderboards: Predictive Validity for the Evaluation of LLM Agents](https://arxiv.org/abs/2606.19704) — a 61-author coordinated deep-dive (fourteen parallel studies of one MCP-based industrial-agent benchmark) showing no single benchmark covers more than 4–5 of the dimensions real deployment exposes; the case for *predictive validity* over static scores — read before trusting any agent leaderboard (the thesis paper for the deployment-grounded agent-eval trend)
- [Securing the future of AI agents (DeepMind AI Control Roadmap + "Three Layers of Agentic Security")](https://deepmind.google/blog/securing-the-future-of-ai-agents/) — a major lab's blueprint for production agent security: defense-in-depth (sandboxing + injection resistance + alignment + treating internal agents as potentially misaligned) plus a behavioral monitor trained on ~1M coding-agent trajectories, live on Gemini Spark
- [MosaicLeaks: Privacy Risks for Deep Research Agents](https://huggingface.co/blog/ServiceNow/mosaicleaks) — research agents leak local/private context through the *mosaic effect* of their web queries; training for task success alone makes leakage worse, and "you can't prompt privacy in, you have to train it in" — read before deploying any retrieval/tool agent over sensitive data
- [Sumi: Open Uniform Diffusion Language Model from Scratch](https://arxiv.org/abs/2606.19005) — the first uniform-diffusion LM pretrained from scratch at both large parameter scale and token budget, a clean open reference point; study it to understand diffusion-LM scaling firsthand
- [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) — Z.ai's new flagship open MoE (~753B, MIT) and the first GLM at a full 1M-token context, via a `GlmMoeDsa` sparse-attention operator; study the openly-reported benchmarks (vs Claude Opus 4.8 / GPT-5.5 / Gemini 3.1 Pro) and the sparse-attention design as the current open-weight route to cheap long context
- [LoopCoder-v2](https://arxiv.org/abs/2606.18023) — a 7B Parallel Loop Transformer coder family trained from scratch (18T tokens) that treats loop count as a first-class design knob; the clearest "looped transformers, trained not bolted-on" datapoint, and why two loops tends to be the sweet spot
- [NVIDIA Nemotron 3 Ultra (550B/55B "LatentMoE")](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) — a US lab's frontier open-weight MoE on a Mamba-2 + MoE + Attention hybrid with MTP, 1M context, shipped natively in NVFP4; the canonical artifact for the subquadratic-attention trend, and for how hybrid-linear-attention MoE and low-bit-native distribution converge at frontier scale

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- No earthquake on the [HN](https://news.ycombinator.com/) front page (read direct via the Algolia API): the AI items are [Qwen-AgentWorld](https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B) (captured) and [DiffusionBench](https://news.ycombinator.com/) (noted, likely generative-image, off the language-diffusion axis); nothing field-shaking.
- Reddit broad-pulse (tvly restored): tiny-VLM intake ([SupraVL-Nano-900k](https://www.reddit.com/r/LocalLLaMA/)), "local models got useful fast" discussion, and [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) leading the Artificial Analysis index (aggregator chatter, not evidence — already tracked).
- Open-model momentum stays a recurring theme; a [Mistral](https://huggingface.co/mistralai) "open-weight family in July" rumor still circulates with no primary artifact.
- Degraded this run: the [code4AI](https://www.youtube.com/@code4AI) YouTube curator feed 404'd again (persistent datacenter-IP block) and the [AINews](https://news.smol.ai/) digest index is JS-only — the HN/Reddit net covered the earthquake check; pointer/digest blogs (Interconnects, Simon Willison, alphamatch) were swept and clean.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (36)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-24](reports/2026-06-24.md) · weekly: [2026-W25](reports/weekly/2026-W25.md) · conventions: [AGENTS.md](AGENTS.md)
