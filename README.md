# AI Radar

![trends](https://img.shields.io/badge/trends-13-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-35-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--22-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-22):**
- **Quiet scan — no new trend evidence, no stage moves.** A full first-run of the day with nothing new across the lab sweep, the 8-org open-weight recheck, the GitHub watch, the curator lane (both halves) and the community pulse; arXiv is still in its weekend-quiet zone (newest cs.* listings are the same 06-18/06-19 batch already mined).
- **Watchlist +1 / −2.** Closed a capture leak by queuing [MAA — Marginal Advantage Accumulation for Memory-Driven Agent Self-Evolution](https://arxiv.org/abs/2606.20475) (named in the 06-21 log but never captured; joins [FinAcumen](https://arxiv.org/abs/2606.17642) on a forming *self-evolving-memory* sub-theme), and burned down two stale isolated [watchlist](TRENDS.md#observation_queue) items (cs.SE file-based agent protocol, cs.AR lossless weight compression).
- **Native-serving gates still unfired (2+ weeks)** across [open-weight](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs), [subquadratic attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) and [low-bit quant](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache): no native MiniMax-M3 / GLM-5.2 kernels or benchmarked vLLM `turboquant` release ([vLLM](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) v0.23.1rc0 / SGLang v0.5.13.post1 unchanged).

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |

## Trends

🌱 2 · 📈 6 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🚀 accelerating | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-10](https://arxiv.org/abs/2606.12191) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-11](https://learn.microsoft.com/en-us/agent-framework/) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🌱 seed | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🌱 seed | [2026-06-17](https://arxiv.org/abs/2606.19005) |

## Worth studying

- [Looped World Models (LoopWM)](https://arxiv.org/abs/2606.18208) — the first looped-transformer architecture for *world modelling*: a parameter-shared block iteratively refines the latent environment state with adaptive compute (~100× parameter efficiency, less long-horizon drift); the looped/recursive-computation idea (LoopCoder-v2/LT2) crossing into world simulation, and the canonical example of work the trusted-curator lane (code4AI) catches on the pinned latent-reasoning axis
- [DiffusionGemma (26B-A4B discrete-diffusion MoE)](https://huggingface.co/google/diffusiongemma-26B-A4B-it) — Google DeepMind's open-weights (Apache-2.0) discrete-diffusion LM: an encoder-decoder Gemma-4 MoE that denoises whole blocks of tokens ("canvases") instead of decoding left-to-right (multi-canvas, block-autoregressive) for ~4× faster generation; the clearest production-scale example of a *non-autoregressive* open LM — pair with Sumi for the line now seeded as diffusion-lm-013
- [Beyond Static Leaderboards: Predictive Validity for the Evaluation of LLM Agents](https://arxiv.org/abs/2606.19704) — a 61-author coordinated deep-dive (fourteen parallel studies of one MCP-based industrial-agent benchmark) showing no single benchmark covers more than 4–5 of the dimensions real deployment exposes; the case for *predictive validity* over static scores — read before trusting any agent leaderboard
- [Securing the future of AI agents (DeepMind AI Control Roadmap + "Three Layers of Agentic Security")](https://deepmind.google/blog/securing-the-future-of-ai-agents/) — a major lab's blueprint for production agent security: defense-in-depth (sandboxing + injection resistance + alignment + treating internal agents as potentially misaligned) plus a behavioral monitor trained on ~1M coding-agent trajectories, live on Gemini Spark
- [MosaicLeaks: Privacy Risks for Deep Research Agents](https://huggingface.co/blog/ServiceNow/mosaicleaks) — research agents leak local/private context through the *mosaic effect* of their web queries; training for task success alone makes leakage worse, and "you can't prompt privacy in, you have to train it in" — read before deploying any retrieval/tool agent over sensitive data
- [Sumi: Open Uniform Diffusion Language Model from Scratch](https://arxiv.org/abs/2606.19005) — the first uniform-diffusion LM pretrained from scratch at both large parameter scale and token budget, a clean open reference point; study it to understand diffusion-LM scaling firsthand
- [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) — Z.ai's new flagship open MoE (~753B, MIT) and the first GLM at a full 1M-token context, via a `GlmMoeDsa` sparse-attention operator; study the openly-reported benchmarks (vs Claude Opus 4.8 / GPT-5.5 / Gemini 3.1 Pro) and the sparse-attention design as the current open-weight route to cheap long context
- [LoopCoder-v2](https://arxiv.org/abs/2606.18023) — a 7B Parallel Loop Transformer coder family trained from scratch (18T tokens) that treats loop count as a first-class design knob; the clearest "looped transformers, trained not bolted-on" datapoint, and why two loops tends to be the sweet spot
- [NVIDIA Nemotron 3 Ultra (550B/55B "LatentMoE")](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) — a US lab's frontier open-weight MoE on a Mamba-2 + MoE + Attention hybrid with MTP, 1M context, shipped natively in NVFP4; the canonical artifact for the subquadratic-attention trend, and for how hybrid-linear-attention MoE and low-bit-native distribution converge at frontier scale

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- No earthquake today. The [HN](https://news.ycombinator.com/) front page (read direct via the Algolia API) is led by product/policy items (identity verification on a vendor product) — nothing field-shaking.
- [Apertus](https://huggingface.co/swiss-ai) ("Open Foundation Model for Sovereign AI") keeps high [HN](https://news.ycombinator.com/) attention — the Swiss EPFL/ETH fully-open model (8B/70B from 2025 + a 2026 v1.1 sub-4B line); queued as a sovereign/EU on-device datapoint, not frontier-scale, so not open-weight evidence.
- Open-model momentum is a recurring [HN](https://news.ycombinator.com/) theme ("minimal downside to switching to open models"; local fine-tunes of sub-1B Qwen) — sentiment, not a primary artifact.
- A [Mistral](https://huggingface.co/mistralai) "new open-weight family in July" rumor still circulates with no primary artifact (would be a 2nd non-Chinese lab on the open-weight wave). Direct HF / HN endpoints work from this run's IP; Reddit-direct stays egress-blocked (tvly fallback).

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (35)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-22](reports/2026-06-22.md) · weekly: [2026-W25](reports/weekly/2026-W25.md) · conventions: [AGENTS.md](AGENTS.md)
