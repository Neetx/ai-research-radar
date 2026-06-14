# AI Radar

![trends](https://img.shields.io/badge/trends-11-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-15-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--14-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-14):**
- [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) **broadens from four to six Chinese labs**: two queued intake items were verified against primary HF cards and promoted — Xiaomi [MiMo-V2.5-Pro](https://huggingface.co/XiaomiMiMo/MiMo-V2.5-Pro) (1.02T/42B MoE, hybrid attention + MTP, 1M ctx) and Alibaba [Qwen3.5](https://huggingface.co/Qwen/Qwen3.5-397B-A17B) (multimodal MoE up to 397B-A17B). Stays 🚀 accelerating.
- A fresh Moonshot drop verified from the pulse: [Kimi-K2.7-Code](https://huggingface.co/moonshotai/Kimi-K2.7-Code) (06-12, 1T/32B MoE, MLA + MoonViT) — coding/agentic, shipped *natively in INT4*. Newer than the K2.6 already cited.
- Sub-pattern across the new drops: frontier open weights increasingly ship **natively in low-bit/MX formats** (Kimi INT4, MiMo FP4-DFlash, MiniMax-M3 MXFP8) — logged under the hardware↔low-bit [watchlist](TRENDS.md#observation_queue) note, not yet its own trend.
- Earlier today: [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) gained a fifth cluster ([Dense Latent Communication](https://arxiv.org/abs/2606.13594)); M3 serving-adoption watch fired ([NVIDIA guide](https://developer.nvidia.com/blog/deploy-long-context-reasoning-and-agentic-workflows-with-minimax-m3-on-nvidia-accelerated-infrastructure/)) — vLLM still serves M3 recipe-only (v0.23.0 unchanged this pass).

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 💤 dormant | [2026-05-20](https://arxiv.org/abs/2605.20670) |

## Trends

🌱 0 · 📈 4 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 2

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
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 💤 dormant | [2026-05-20](https://arxiv.org/abs/2605.20670) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 💤 dormant | [2026-05-17](https://arxiv.org/abs/2605.17634) |

## Worth studying

- [Kimi-K2.7-Code](https://huggingface.co/moonshotai/Kimi-K2.7-Code) — a frontier coding/agentic open MoE (1T/32B, MLA + MoonViT) shipped *natively in INT4*; study how a top lab now treats low-bit as the default distribution format, plus its interleaved-thinking + multi-step-tool-call design
- [Deploy MiniMax-M3 on NVIDIA (TensorRT-LLM/SGLang/vLLM/Dynamo)](https://developer.nvidia.com/blog/deploy-long-context-reasoning-and-agentic-workflows-with-minimax-m3-on-nvidia-accelerated-infrastructure/) — how a frontier 1M-context open-weight MoE actually gets served (disaggregated prefill/decode, MXFP8, MSA at 1/20th per-token compute); the research→production map for long-context serving
- [Dense Latent Communication Across Heterogeneous Agents](https://arxiv.org/abs/2606.13594) — pushes KV-cache communication past duplicate-model setups to cross-model latent alignment between different model families
- [MiniMax-M3](https://huggingface.co/MiniMaxAI/MiniMax-M3) — frontier open-weight native-multimodal MoE (~428B/23B-active, 1M context); its MiniMax Sparse Attention (MSA) claims 9× prefill / 15× decode speedup at 1M tokens — study the operator + tech report (arXiv:2606.13392)
- [OpenEnv (Meta-PyTorch + Hugging Face)](https://huggingface.co/blog/openenv) — the emerging standard interface (`step()`/`reset()`/`close()` + Hub) for agentic RL environments, already wired into TRL/Unsloth/verl/SkyRL/TorchForge
- [EchoLeak: First Real-World Zero-Click Prompt Injection (AAAI 2025)](https://arxiv.org/abs/2509.10540) — the canonical production exploit (CVE-2025-32711, M365 Copilot, CVSS 9.3) behind the "move security into the architecture" thesis
- [LT2: Linear-Time Looped Transformers](https://arxiv.org/abs/2605.20670) — looped reasoning at linear cost; keeps the latent-reasoning line practical
- [PPD Disaggregation for Multi-turn LLM Serving](https://arxiv.org/abs/2603.13358) — ICML 2026; "append-prefill is an order of magnitude cheaper than full prefill" reframes prefill/decode routing for chat and agent workloads

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) open-weight "value wars" now compare frontier MoE that the radar has since verified — Xiaomi **MiMo-V2.5-Pro** and Alibaba **Qwen3.5** were opened on their primary HF cards and promoted to evidence (the post is intake; the model card is the evidence).
- A curated AI-news digest flagged **Kimi-K2.7-Code**; following the link to the [official Moonshot HF card](https://huggingface.co/moonshotai/Kimi-K2.7-Code) verified it (06-12) — the intake-lane → primary-artifact path working as designed.
- Direct Reddit / HF-papers JSON is blocked from this run's IP; sampled via Tavily search instead (logged for the source-heal trail).

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (15)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-14](reports/2026-06-14.md) · weekly: [2026-W24](reports/weekly/2026-W24.md) · conventions: [AGENTS.md](AGENTS.md)
