# AI Radar

![trends](https://img.shields.io/badge/trends-14-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-38-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--26-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-26):**
- **Quiet pass for the ledger — no new trend, no stage moves, no evidence adds.** The lab sweep, 8-org open-weight recheck, GitHub watch, curator lane and pulse turned up nothing new on the tracked axes since 06-25.
- **Watchlist 39 → 38** — 2 captures, 3 stale drops. Captured a forming **agentic-RL reward/supervision-limits** cluster: ["The Verification Horizon: No Silver Bullet for Coding Agent Rewards"](https://arxiv.org/abs/2606.26300) (verifying coding-agent solutions is becoming *harder* than generating them), ["Why Multi-Step Tool-Use RL Collapses"](https://arxiv.org/abs/2606.26027) and [OPID](https://arxiv.org/abs/2606.26790) — heterogeneous claims, convergence did not fire; plus an exploration omnibus (Cache-Resident LLM inference, GUI-vs-CLI computer-use bench, JetSpec). Dropped 3 stale 06-21 items (Apertus pulse, two superseded exploration notes).
- **Standing serving-engine gates still unfired** for [open-weight](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) / [subquadratic attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) / [low-bit quant](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache): SGLang bumped to v0.5.14 and vLLM to v0.24.0rc2 (a P/D-disagg fix), but neither documents native MiniMax-M3 / GLM-5.2 / MSA-DSA kernels or a benchmarked `turboquant` release.
- **Pulse — no earthquake.** The HN front page and Reddit broad-pulse carried no model-access/field-shaking event; the open-model conversation stays centered on GLM-5.2 (already tracked). YouTube curator lane remains IP-blocked (covered by the HN/HF-papers overlap).

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |

## Trends

🌱 2 · 📈 7 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🚀 accelerating | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 📈 emerging | [2026-06-24](https://arxiv.org/abs/2606.25331) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-22](https://sakana.ai/fugu-release/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-06-23](https://arxiv.org/abs/2606.24530) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🌱 seed | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |

## Worth studying

- [The Verification Horizon: No Silver Bullet for Coding Agent Rewards](https://arxiv.org/abs/2606.26300) — a 12-author (Alibaba/Qwen-line) result inverting a load-bearing assumption of agentic RL: "verifying is easier than producing" is breaking down for coding agents — as models reason better and harnesses get more sophisticated, generating complex solutions outpaces our ability to verify them, so reward *verification* becomes the bottleneck and there is no silver-bullet reward; read before trusting any verifiable-reward / RLVR pipeline for coding agents (pair with "Why Multi-Step Tool-Use RL Collapses" + OPID on the denser-supervision side)
- [iLLaDA-8B (Improved Large Language Diffusion Models)](https://huggingface.co/GSAI-ML/iLLaDA-8B-Base) — RUC/GSAI-ML's open-weights (Apache-2.0, paper 2606.25331) 8B fully-bidirectional masked-diffusion LM trained from scratch on 12T tokens: the clearest current "diffusion LM at autoregressive quality" datapoint — its own base-model card beats LLaDA-8B (avg 63.9 vs 51.1) and Dream-7B (61.4) and ties autoregressive Qwen2.5-7B (63.3); the third independent open diffusion base model that just moved diffusion-lm-013 to emerging
- [Thinking to Recall: How Reasoning Unlocks Parametric Knowledge in LLMs](https://research.google/blog/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms/) — Google Research: why a reasoning trace helps an LLM recall even *simple* single-hop facts that need no arithmetic — a *computational buffer* (reasoning tokens as latent computation) and *factual priming* — so reasoning expands the parametric-knowledge boundary; the practical hook is process rewards on factually-supported steps to cut hallucination
- [Qwen-AgentWorld (35B-A3B language world model)](https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B) — Alibaba/Qwen's open-weights (paper 2606.24597) "native language world model": a 35B-A3B MoE where *predicting the next environment state* from an agent's action+history IS the objective from CPT onward; a runnable bridge between world models and agent infrastructure — a learned *simulator of agentic environments*
- [Prompt Injection as Role Confusion](https://arxiv.org/abs/2603.12277) — Ye/Cui/Hadfield-Menell (MIT, ICML 2026): the cleanest mechanistic *theory* of why prompt injection works — LLMs infer who is speaking from how a span *sounds*, not its labeled `<user>`/`<tool>` role; study it (with role-confusion.github.io) for "role probes", why label-based defenses are brittle, and as the underpinning of the architectural/least-privilege turn
- [Sakana Fugu: A Multi-Agent Orchestration System as a Foundation Model](https://sakana.ai/fugu-release/) — Sakana AI's product: a small LM TRAINED to orchestrate a pool of frontier LLMs (choosing/switching models, recursive self-calls for test-time scaling) behind one API; the clearest example of "orchestration-as-a-model" vs orchestration-as-a-framework. Benchmarks are vendor-claimed.
- [Looped World Models (LoopWM)](https://arxiv.org/abs/2606.18208) — the first looped-transformer architecture for *world modelling*: a parameter-shared block iteratively refines the latent environment state with adaptive compute (~100× parameter efficiency, less long-horizon drift); the looped/recursive-computation idea crossing into world simulation
- [DiffusionGemma (26B-A4B discrete-diffusion MoE)](https://huggingface.co/google/diffusiongemma-26B-A4B-it) — Google DeepMind's open-weights (Apache-2.0) discrete-diffusion LM: an encoder-decoder Gemma-4 MoE that denoises whole blocks of tokens ("canvases") instead of decoding left-to-right for ~4× faster generation; pair with Sumi + iLLaDA for the diffusion-lm-013 line
- [Beyond Static Leaderboards: Predictive Validity for the Evaluation of LLM Agents](https://arxiv.org/abs/2606.19704) — a 61-author coordinated deep-dive (fourteen parallel studies of one MCP-based industrial-agent benchmark) showing no single benchmark covers more than 4–5 of the dimensions real deployment exposes; the case for *predictive validity* over static scores — read before trusting any agent leaderboard
- [Securing the future of AI agents (DeepMind AI Control Roadmap + "Three Layers of Agentic Security")](https://deepmind.google/blog/securing-the-future-of-ai-agents/) — a major lab's blueprint for production agent security: defense-in-depth (sandboxing + injection resistance + alignment + treating internal agents as potentially misaligned) plus a behavioral monitor trained on ~1M coding-agent trajectories, live on Gemini Spark
- [MosaicLeaks: Privacy Risks for Deep Research Agents](https://huggingface.co/blog/ServiceNow/mosaicleaks) — research agents leak local/private context through the *mosaic effect* of their web queries; training for task success alone makes leakage worse, and "you can't prompt privacy in, you have to train it in" — read before deploying any retrieval/tool agent over sensitive data

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- No on-axis earthquake on the [HN](https://news.ycombinator.com/) front page (read direct via the Algolia API): the loudest items are a Herculaneum-scroll read, an Apple MacBook/iPad price raise and an IBM sub-1nm chip — all off-axis (history / hardware-business). The most AI-relevant thread, ["what happened after 2k people tried to hack my AI assistant"](https://news.ycombinator.com/), is an agent-security anecdote (intake).
- Reddit broad-pulse + digests (AINews / Latent.Space): the open-model conversation stays dominated by [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) ("as good as Opus 4.8 / GPT-5.5" sentiment) and an "economics favor open models" opinion piece — no new drop, no model-access earthquake.
- Degraded this run: the [code4AI](https://www.youtube.com/@code4AI) YouTube curator lane remains IP-blocked end-to-end (not re-attempted per the standing heal note); coverage falls back on the HN/HF-papers overlap. Pointer/digest blogs (Interconnects, Simon Willison, alphamatch) swept and clean.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (38)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-26](reports/2026-06-26.md) · weekly: [2026-W25](reports/weekly/2026-W25.md) · conventions: [AGENTS.md](AGENTS.md)
