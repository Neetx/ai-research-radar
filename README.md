# AI Radar

![trends](https://img.shields.io/badge/trends-11-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-3-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-11-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--12-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence.

**Since last scan (2026-06-12):**
- [Low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) is **accelerating**: vLLM ships an in-tree [`turboquant` KV-cache module](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) — second production engine after EXL3.
- [PPD](https://arxiv.org/abs/2603.13358) (ICML 2026) promoted from the watchlist into [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture): affirms PD-disagg as "the standard architecture" and extends it to multi-turn (append-prefill routing).
- [GenEnv](https://arxiv.org/abs/2512.19682) (Princeton) promoted into [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training): the "co-evolve environments with the policy" sub-theme now has two independent groups.
- Off-axis exploration (cs.AR venue): low-bit LLM serving surfacing in the hardware-architecture listing — [SPEAR](https://arxiv.org/abs/2606.11244) and [TileFuse](https://arxiv.org/abs/2606.11357) logged to the [watchlist](TRENDS.md#observation_queue).

## Trends

🌱 0 · 📈 8 · 🚀 3 · 🌊 0 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-11](https://learn.microsoft.com/en-us/agent-framework/) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 emerging | [2026-06-10](https://arxiv.org/abs/2606.12191) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) | 📈 emerging | [2026-06-08](https://huggingface.co/deepseek-ai) |
| [Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-05](https://arxiv.org/abs/2604.02029) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-05-17](https://arxiv.org/abs/2605.17634) |
| [Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-04-28](https://arxiv.org/abs/2604.25917) |

## Worth studying

- [PPD Disaggregation for Multi-turn LLM Serving](https://arxiv.org/abs/2603.13358) — ICML 2026; the "append-prefill is an order of magnitude cheaper than full prefill" insight reframes prefill/decode routing for chat and agent workloads
- [Agentic Environment Engineering: A Survey](https://arxiv.org/abs/2606.12191) — 63-page systematization of the environment lifecycle (modeling/synthesis/evaluation/application); the map to read before building or buying RL-environment infrastructure
- [On Subquadratic Architectures](https://arxiv.org/abs/2606.12364) — clean head-to-head of xLSTM vs Mamba-2 vs Gated DeltaNet on code-model pretraining, distillation and time-series pretraining, with a unified formulation
- [vLLM `turboquant` module](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) — KV-cache vector quantization inside a mainstream serving engine; read next to the TurboQuant paper to see the research→production distance
- [RecursiveMAS](https://github.com/RecursiveMAS/RecursiveMAS) — reference implementation of latent-space multi-agent computation, reproducible on modest hardware (Qwen/Llama/Gemma checkpoints)
- [Cache-to-Cache (C2C)](https://arxiv.org/abs/2510.03215) — the cleanest formulation of direct KV-cache communication between different LLMs (ICLR'26)
- [ExLlamaV3 / EXL3](https://github.com/turboderp-org/exllamav3) — production trellis-coded quantization (QTIP-derived) on consumer GPUs
- [bitnet.cpp](https://github.com/microsoft/BitNet) — the official ternary-LLM inference stack; the practical entry point to 1-bit models on CPU

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (11)](TRENDS.md#observation_queue) · daily reports: [reports/](reports) — latest [2026-06-12](reports/2026-06-12.md) · weekly: none yet · conventions: [AGENTS.md](AGENTS.md)
