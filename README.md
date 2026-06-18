# AI Radar

![trends](https://img.shields.io/badge/trends-11-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-32-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--18-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-18):**
- **Quiet scan — no stage moves, no new trend evidence.** The lab sweep, GitHub watch and open-weight recheck turned up nothing newer than yesterday; the native-serving watch items (vLLM/SGLang support for [MiniMax-M3](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) / GLM-5.2, benchmarked [turboquant](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache)) have not fired.
- **Exploration find — diffusion LMs strengthening:** the 06-13 watch item fired twice — [Sumi](https://arxiv.org/abs/2606.19005) (open uniform diffusion LM pretrained from scratch) and [Diffusion-Proof](https://arxiv.org/abs/2606.19315) (diffusion LLMs for theorem proving) join Google's DiffusionGemma. Logged to the [watchlist](TRENDS.md#observation_queue); still below the trend bar.
- **Watchlist +3 intake** ([32](TRENDS.md#observation_queue)): the diffusion-LM consolidation, a Mistral "new open-weight family in July" rumor (unverified), and agent-harness/long-horizon-eval datapoints ([Xcientist](https://arxiv.org/abs/2606.18874), [CEO-Bench](https://arxiv.org/abs/2606.18543)). No promotions, no drops.
- **Study pick:** [Sumi](https://arxiv.org/abs/2606.19005) — a clean open reference uniform-diffusion LM trained from scratch at scale, for studying diffusion-LM scaling behavior.

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |

## Trends

🌱 0 · 📈 5 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) | 🚀 accelerating | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-10](https://arxiv.org/abs/2606.12191) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-11](https://learn.microsoft.com/en-us/agent-framework/) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 💤 dormant | [2026-05-17](https://arxiv.org/abs/2605.17634) |

## Worth studying

- [Sumi: Open Uniform Diffusion Language Model from Scratch](https://arxiv.org/abs/2606.19005) — the first uniform-diffusion LM pretrained from scratch at both large parameter scale and token budget, released as a clean open reference point; study it to understand diffusion-LM scaling firsthand as the architecture line (DiffusionGemma, dLLMs) keeps recurring
- [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) — Z.ai's new flagship open MoE (~753B, MIT) and the first GLM at a full 1M-token context, via a `GlmMoeDsa` sparse-attention operator (the "index share" trick); study the card's openly-reported benchmarks (vs Claude Opus 4.8 / GPT-5.5 / Gemini 3.1 Pro) and the sparse-attention design as the current open-weight route to cheap long context
- [LoopCoder-v2](https://arxiv.org/abs/2606.18023) — a 7B Parallel Loop Transformer coder family trained from scratch (18T tokens) that treats loop count as a first-class design knob (extra-loop refinement vs cross-loop positional-mismatch cost); the clearest "looped transformers, trained not bolted-on" datapoint, and why two loops tends to be the sweet spot
- [NVIDIA Nemotron 3 Ultra (550B/55B "LatentMoE")](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) — a US lab's frontier open-weight MoE on a Mamba-2 + MoE + Attention hybrid with MTP, 1M context, shipped natively in NVFP4 (open OpenMDW-1.1 license + open datasets); study how hybrid-linear-attention MoE and low-bit-native distribution converge at frontier scale
- [Qwen3.6-35B-A3B](https://huggingface.co/Qwen/Qwen3.6-35B-A3B) — Alibaba's newest open MoE on a Gated-DeltaNet (linear attention) + Gated-Attention + MoE backbone with MTP and 256K context; a clean, documented example of a production frontier model using subquadratic attention, plus a "thinking-preservation" option for agentic coding
- [Skip a Layer or Loop It? (PoLar)](https://arxiv.org/abs/2606.06574) — training-free dynamic depth: pretrained layers become modules you skip or loop per input, so shorter "programs" match full-depth accuracy and looping fixes some errors — inference-time compute control without retraining
- [Kimi-K2.7-Code](https://huggingface.co/moonshotai/Kimi-K2.7-Code) — a frontier coding/agentic open MoE (1T/32B, MLA + MoonViT) shipped *natively in INT4*; study how a top lab now treats low-bit as the default distribution format, plus its interleaved-thinking + multi-step-tool-call design
- [Deploy MiniMax-M3 on NVIDIA (TensorRT-LLM/SGLang/vLLM/Dynamo)](https://developer.nvidia.com/blog/deploy-long-context-reasoning-and-agentic-workflows-with-minimax-m3-on-nvidia-accelerated-infrastructure/) — how a frontier 1M-context open-weight MoE actually gets served (disaggregated prefill/decode, MXFP8, MSA at 1/20th per-token compute); the research→production map for long-context serving

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- The open-weight conversation is still centered on [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) — [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) flags it as the first open-weights model to cross 80% on Terminal-Bench; the weights were followed to the primary HF card and verified.
- A forward-looking rumor that [Mistral](https://huggingface.co/mistralai) will ship "a new family of open-weight models in July" is circulating — intake only, no primary artifact yet; queued and being watched.
- Direct Reddit / HN JSON remains blocked from this run's IP; sampled via Tavily — logged for the source-heal trail.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (32)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-18](reports/2026-06-18.md) · weekly: [2026-W24](reports/weekly/2026-W24.md) · conventions: [AGENTS.md](AGENTS.md)
