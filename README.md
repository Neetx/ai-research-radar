# AI Radar

![trends](https://img.shields.io/badge/trends-11-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-3-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-10-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--13-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence.

**Since last scan (2026-06-12):**
- 💤 [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) and [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) → **dormant** (27 and 24 days without qualifying evidence); [LT2](https://arxiv.org/abs/2605.20670) (May 2026) added to latent-reasoning — field is active, would reactivate quickly
- 📊 Stacklok "State of MCP 2026" vendor survey verified: 50% of orgs experimenting with MCP, only 11% in production — [mcp-standard-001](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks)
- 🚀 [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) confirmed accelerating: vLLM's in-tree [`turboquant`](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) + EXL3 = two independent production stacks carrying vector/trellis quant
- 🌍 W24 retrospective: bootstrap week — 11 trends seeded, 51 evidence items added, cs.AR venue newly in rotation

## Trends

🌱 0 · 📈 6 · 🚀 3 · 🌊 0 · 🏔 0 · 📉 0 · 💤 2

| trend | stage | latest signal |
|---|---|---|
| [Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-12](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-11](https://learn.microsoft.com/en-us/agent-framework/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 emerging | [2026-06-10](https://arxiv.org/abs/2606.12191) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-by-chinese-labs) | 📈 emerging | [2026-06-08](https://huggingface.co/deepseek-ai) |
| [Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-05](https://arxiv.org/abs/2604.02029) |
| [Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 💤 dormant | [2026-05-20](https://arxiv.org/abs/2605.20670) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 💤 dormant | [2026-05-17](https://arxiv.org/abs/2605.17634) |

## Worth studying

- [LT2: Linear-Time Looped Transformers](https://arxiv.org/abs/2605.20670) — looping uniquely synergizes with subquadratic attention; Ouro-hybrid-1.4B beats industry 1B models at linear-time cost — practical path to scalable looped LMs
- [PPD Disaggregation for Multi-turn LLM Serving](https://arxiv.org/abs/2603.13358) — ICML 2026; "append-prefill is an order of magnitude cheaper than full prefill" — required reading for anyone running PD-disaggregated serving
- [Agentic Environment Engineering: A Survey](https://arxiv.org/abs/2606.12191) — 63-page systematization of the environment lifecycle; the map to read before building or buying RL-environment infrastructure
- [On Subquadratic Architectures](https://arxiv.org/abs/2606.12364) — head-to-head xLSTM vs Mamba-2 vs Gated DeltaNet with unified formulation; orientation for anyone weighing attention alternatives
- [vLLM `turboquant` module](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) — KV-cache vector quantization inside a mainstream serving engine; read alongside TurboQuant paper to see the research→production gap
- [RecursiveMAS](https://github.com/RecursiveMAS/RecursiveMAS) — reference implementation of latent-space multi-agent computation, reproducible on modest hardware (Qwen/Llama/Gemma checkpoints)
- [Cache-to-Cache (C2C)](https://arxiv.org/abs/2510.03215) — the cleanest formulation of direct KV-cache communication between LLMs (ICLR'26)
- [ExLlamaV3 / EXL3](https://github.com/turboderp-org/exllamav3) — production trellis-coded quantization (QTIP-derived) on consumer GPUs; the format to study to understand where weight quantization is heading

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (10)](TRENDS.md#observation_queue) · daily reports: [reports/](reports) — latest [2026-06-12](reports/2026-06-12.md) · weekly: [2026-W24](reports/weekly/2026-W24.md) · conventions: [AGENTS.md](AGENTS.md)
