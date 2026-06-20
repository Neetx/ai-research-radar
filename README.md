# AI Radar

![trends](https://img.shields.io/badge/trends-12-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-37-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--20-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-20 — weekly W25 recalibration):**
- **New seed trend — [Subquadratic & sparse attention in frontier models](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) (🌱 seed):** two sub-themes that had been forming in the queue for ~2 weeks are merged and promoted — frontier open weights are independently moving off dense softmax attention toward subquadratic backbones ([Nemotron](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) Mamba-2, [Qwen3.6](https://huggingface.co/Qwen/Qwen3.6-35B-A3B) Gated-DeltaNet, MiMo full+SWA) and sparse long-context operators ([GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) DSA, [MiniMax-M3](https://huggingface.co/MiniMaxAI/MiniMax-M3) MSA, DeepSeek-V4). Six labs + a [survey](https://arxiv.org/abs/2606.12364); held at seed pending first-class serving-engine kernels.
- **Retitle — [Open-weight wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs):** dropped "by Chinese labs" (NVIDIA, a US lab, has been in the set since 06-16) — the claim is lab-agnostic. No dormancy changes, no archivals, no merges this week (oldest active evidence is 10 days old).
- **Anchoring warning:** all in-week evidence landed on pre-existing trends — addressed by seeding subquad-attn-012. Exploration ran on 7/7 daily passes but venues are concentrated on HF daily papers / arXiv; next week diversifies venues and prioritises diffusion LMs, A2A implementations, and the subquad-attn serving-engine gate.
- **Housekeeping:** study shelf pruned 25 → 10 (soft cap applied — amendment W24-P2); watchlist now [37](TRENDS.md#observation_queue).

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |

## Trends

🌱 1 · 📈 6 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🚀 accelerating | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-10](https://arxiv.org/abs/2606.12191) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-11](https://learn.microsoft.com/en-us/agent-framework/) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🌱 seed | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |

## Worth studying

- [Securing the future of AI agents (DeepMind AI Control Roadmap + "Three Layers of Agentic Security")](https://deepmind.google/blog/securing-the-future-of-ai-agents/) — a major lab's blueprint for production agent security: defense-in-depth (sandboxing + injection resistance + alignment + treating internal agents as potentially misaligned) plus a behavioral monitor trained on ~1M coding-agent trajectories, live on Gemini Spark; the operational/architectural counterpart to the impossibility-result theory
- [MosaicLeaks: Privacy Risks for Deep Research Agents](https://huggingface.co/blog/ServiceNow/mosaicleaks) — research agents leak local/private context through the *mosaic effect* of their web queries; training for task success alone makes leakage worse, and "you can't prompt privacy in, you have to train it in" (credit-assigning query construction cuts leakage >3× at neutral accuracy) — read before deploying any retrieval/tool agent over sensitive data
- [Sumi: Open Uniform Diffusion Language Model from Scratch](https://arxiv.org/abs/2606.19005) — the first uniform-diffusion LM pretrained from scratch at both large parameter scale and token budget, a clean open reference point; study it to understand diffusion-LM scaling firsthand as the architecture line (DiffusionGemma, dLLMs) keeps recurring
- [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) — Z.ai's new flagship open MoE (~753B, MIT) and the first GLM at a full 1M-token context, via a `GlmMoeDsa` sparse-attention operator (the "index share" trick); study the card's openly-reported benchmarks (vs Claude Opus 4.8 / GPT-5.5 / Gemini 3.1 Pro) and the sparse-attention design as the current open-weight route to cheap long context
- [LoopCoder-v2](https://arxiv.org/abs/2606.18023) — a 7B Parallel Loop Transformer coder family trained from scratch (18T tokens) that treats loop count as a first-class design knob (extra-loop refinement vs cross-loop positional-mismatch cost); the clearest "looped transformers, trained not bolted-on" datapoint, and why two loops tends to be the sweet spot
- [NVIDIA Nemotron 3 Ultra (550B/55B "LatentMoE")](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) — a US lab's frontier open-weight MoE on a Mamba-2 + MoE + Attention hybrid with MTP, 1M context, shipped natively in NVFP4 (open OpenMDW-1.1 license + open datasets); the canonical artifact for the new subquadratic-attention trend, and for how hybrid-linear-attention MoE and low-bit-native distribution converge at frontier scale
- [Skip a Layer or Loop It? (PoLar)](https://arxiv.org/abs/2606.06574) — training-free dynamic depth: pretrained layers become modules you skip or loop per input, so shorter "programs" match full-depth accuracy and looping fixes some errors — inference-time compute control without retraining
- [OpenEnv (Meta-PyTorch + Hugging Face)](https://huggingface.co/blog/openenv) — the emerging standard interface (`step()`/`reset()`/`close()` + Hub) for agentic RL environments, already wired into TRL/Unsloth/verl/SkyRL/TorchForge; the spec to read to see where agent-training infrastructure is converging

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- The open-weight conversation is still centered on [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) — [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) flags it as the first open-weights model to cross 80% on Terminal-Bench; the weights were followed to the primary HF card and verified.
- A forward-looking rumor that [Mistral](https://huggingface.co/mistralai) will ship "a new family of open-weight models in July" is still circulating — intake only, no primary artifact yet; queued and being watched (would be a 2nd non-Chinese lab on the open-weight wave).
- Tavily search for open-weight/serving topics returns mostly SEO/comparator pages (none citable); direct Reddit / HN JSON remains blocked from this run's IP — sampled via Tavily, logged for the source-heal trail.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (37)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-19](reports/2026-06-19.md) · weekly: [2026-W25](reports/weekly/2026-W25.md) · conventions: [AGENTS.md](AGENTS.md)
