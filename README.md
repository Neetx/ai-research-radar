# AI Radar

![trends](https://img.shields.io/badge/trends-11-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-3-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-10-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--13-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-13):**
- Weekly recalibration 2026-W24: [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) and [latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) → **dormant** (27 and 24 days without qualifying evidence).
- [MCP](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) gained verified adoption data: Stacklok survey — [50% experimenting / 11% in production](https://stacklok.com/blog/the-enterprise-it-security-guide-to-claude-and-mcp) (secondary "41–45% production" claim was wrong).
- [LT2](https://arxiv.org/abs/2605.20670) (linear-time looped transformers) added to latent reasoning — the field stays active even while the trend is dormant.

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-05](https://arxiv.org/abs/2604.02029) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 💤 dormant | [2026-05-20](https://arxiv.org/abs/2605.20670) |

## Trends

🌱 0 · 📈 6 · 🚀 3 · 🌊 0 · 🏔 0 · 📉 0 · 💤 2

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-11](https://learn.microsoft.com/en-us/agent-framework/) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) | 📈 emerging | [2026-06-08](https://huggingface.co/deepseek-ai) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-05](https://arxiv.org/abs/2604.02029) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 emerging | [2026-06-10](https://arxiv.org/abs/2606.12191) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 💤 dormant | [2026-05-20](https://arxiv.org/abs/2605.20670) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 💤 dormant | [2026-05-17](https://arxiv.org/abs/2605.17634) |

## Worth studying

- [PPD Disaggregation for Multi-turn LLM Serving](https://arxiv.org/abs/2603.13358) — ICML 2026; the "append-prefill is an order of magnitude cheaper than full prefill" insight reframes prefill/decode routing for chat and agent workloads
- [LT2: Linear-Time Looped Transformers](https://arxiv.org/abs/2605.20670) — looped reasoning at linear cost; keeps the latent-reasoning line practical
- [Agentic Environment Engineering: A Survey](https://arxiv.org/abs/2606.12191) — 63-page systematization of the environment lifecycle; the map to read before building or buying RL-environment infrastructure
- [On Subquadratic Architectures](https://arxiv.org/abs/2606.12364) — clean head-to-head of xLSTM vs Mamba-2 vs Gated DeltaNet on code-model pretraining, distillation and time-series pretraining
- [vLLM `turboquant` module](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) — KV-cache vector quantization inside a mainstream serving engine; read next to the TurboQuant paper
- [RecursiveMAS](https://github.com/RecursiveMAS/RecursiveMAS) — reference implementation of latent-space multi-agent computation, reproducible on modest hardware (Qwen/Llama/Gemma checkpoints)
- [Cache-to-Cache (C2C)](https://arxiv.org/abs/2510.03215) — the cleanest formulation of direct KV-cache communication between different LLMs (ICLR'26)
- [bitnet.cpp](https://github.com/microsoft/BitNet) — the official ternary-LLM inference stack; the practical entry point to 1-bit models on CPU

## Community pulse

No community pulse sampled yet — first social/repo sample due on the next daily run.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (10)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-12](reports/2026-06-12.md) · weekly: [2026-W24](reports/weekly/2026-W24.md) · conventions: [AGENTS.md](AGENTS.md)
