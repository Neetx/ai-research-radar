# AI Radar

![trends](https://img.shields.io/badge/trends-11-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-25-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--16-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-16):**
- [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) broadens beyond Chinese labs: [NVIDIA Nemotron 3 Ultra](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) (550B/55B open "LatentMoE" Mamba-2 hybrid, NVFP4-native) is the **first US lab** in the set; and the radar backfilled [Qwen3.6](https://huggingface.co/Qwen/Qwen3.6-35B-A3B) (Alibaba's newest open MoE, Gated-DeltaNet hybrid), a April drop it had missed. Breadth/backfill → stage unchanged (accelerating).
- A forming architecture signal: both new entries use **hybrid / subquadratic-attention MoE** backbones (Mamba-2; Gated DeltaNet), echoing MiMo — [queued](TRENDS.md#observation_queue) as a sub-theme; both also ship **natively low-bit** (NVFP4), reinforcing the native-low-bit-distribution note.
- Watchlist +8 intake (KV-cache compression [Tangram](https://arxiv.org/abs/2606.06302), agent context cache [TokenPilot](https://arxiv.org/abs/2606.17016), small-reasoning [VibeThinker-3B](https://arxiv.org/abs/2606.16140), lossless [weight compression](https://arxiv.org/abs/2606.15789), NVIDIA [MoE fusion kernels](https://developer.nvidia.com/blog/) …) — all single-group, below the trend bar. No promotions/drops; no stage moves.

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-04](https://arxiv.org/abs/2606.06574) |

## Trends

🌱 0 · 📈 5 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) | 🚀 accelerating | [2026-06-13](https://huggingface.co/MiniMaxAI/MiniMax-M3) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-10](https://arxiv.org/abs/2606.12191) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-11](https://learn.microsoft.com/en-us/agent-framework/) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-04](https://arxiv.org/abs/2606.06574) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 💤 dormant | [2026-05-17](https://arxiv.org/abs/2605.17634) |

## Worth studying

- [NVIDIA Nemotron 3 Ultra (550B/55B "LatentMoE")](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16) — a US lab's frontier open-weight MoE on a Mamba-2 + MoE + Attention hybrid with MTP, 1M context, shipped natively in NVFP4 (open OpenMDW-1.1 license + open datasets); study how hybrid-linear-attention MoE and low-bit-native distribution converge at frontier scale
- [Qwen3.6-35B-A3B](https://huggingface.co/Qwen/Qwen3.6-35B-A3B) — Alibaba's newest open MoE on a Gated-DeltaNet (linear attention) + Gated-Attention + MoE backbone with MTP and 256K context; a clean, documented example of a production frontier model using subquadratic attention, plus a "thinking-preservation" option for agentic coding
- [Skip a Layer or Loop It? (PoLar)](https://arxiv.org/abs/2606.06574) — training-free dynamic depth: pretrained layers become modules you skip or loop per input, so shorter "programs" match full-depth accuracy and looping fixes some errors — inference-time compute control without retraining
- [Kimi-K2.7-Code](https://huggingface.co/moonshotai/Kimi-K2.7-Code) — a frontier coding/agentic open MoE (1T/32B, MLA + MoonViT) shipped *natively in INT4*; study how a top lab now treats low-bit as the default distribution format, plus its interleaved-thinking + multi-step-tool-call design
- [Deploy MiniMax-M3 on NVIDIA (TensorRT-LLM/SGLang/vLLM/Dynamo)](https://developer.nvidia.com/blog/deploy-long-context-reasoning-and-agentic-workflows-with-minimax-m3-on-nvidia-accelerated-infrastructure/) — how a frontier 1M-context open-weight MoE actually gets served (disaggregated prefill/decode, MXFP8, MSA at 1/20th per-token compute); the research→production map for long-context serving
- [Dense Latent Communication Across Heterogeneous Agents](https://arxiv.org/abs/2606.13594) — pushes KV-cache communication past duplicate-model setups to cross-model latent alignment between different model families
- [MiniMax-M3](https://huggingface.co/MiniMaxAI/MiniMax-M3) — frontier open-weight native-multimodal MoE (~428B/23B-active, 1M context); its MiniMax Sparse Attention (MSA) claims 9× prefill / 15× decode speedup at 1M tokens — study the operator + tech report (arXiv:2606.13392)
- [OpenEnv (Meta-PyTorch + Hugging Face)](https://huggingface.co/blog/openenv) — the emerging standard interface (`step()`/`reset()`/`close()` + Hub) for agentic RL environments, already wired into TRL/Unsloth/verl/SkyRL/TorchForge

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- The open-weight conversation this week centers on NVIDIA's big drop — [Nemotron 3 Ultra](https://huggingface.co/nvidia/NVIDIA-Nemotron-3-Ultra-550B-A55B-BF16)/Super and the [Cosmos 3](https://huggingface.co/nvidia) multimodal line — surfaced via an AINews digest and [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/); the Nemotron 3 Ultra weights were followed to the primary HF card and verified.
- Lingering background chatter: the Chinese-lab "value wars" (DeepSeek-V4, Gemma 4, Qwen) already in the ledger — nothing new the radar hadn't verified.
- Direct Reddit / HN JSON is blocked from this run's IP; sampled via Tavily (tvly reinstalled this session) — logged for the source-heal trail.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (25)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-16](reports/2026-06-16.md) · weekly: [2026-W24](reports/weekly/2026-W24.md) · conventions: [AGENTS.md](AGENTS.md)
</content>
</invoke>
