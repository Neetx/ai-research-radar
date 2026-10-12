# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-23-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--10--12-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-12):** three serving/inference engines in one week now treat decision-model routing as a first-class primitive — [SGLang v0.5.21 and llama.cpp v0.6.0](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) ship native decision-model APIs, resolving that trend's own standing watch item · [vLLM's Vera Rubin NVL72 preview](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) reports 7.8x throughput/GPU over GB200 NVL72, and the same engine's [DeepSeek-V4.1-Flash kernel work](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) lands 5x agentic throughput · Anthropic launched the [Cyber Mission](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) (critical-infrastructure defense + free OSS vulnerability scanning) · Terence Tao's [Math 2.0](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) gives the field's most authoritative outside read on AI-driven mathematics, and Sakana AI/UC Berkeley's [MASS](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) ships a new recursive-self-improvement mechanism.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-06](https://arxiv.org/abs/2610.07767) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-07](https://arxiv.org/abs/2610.06833) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.39788) |

## Trends

🌱 8 · 📈 11 · 🚀 0 · 🌊 0 · 🏔 4 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-04](https://arxiv.org/abs/2610.05319) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-10-09](https://blog.vllm.ai/blog/2026-10-09-vera-rubin-preview) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-07](https://www.microsoft.com/en-us/research/blog/agent-lightning-v1-0-a-3500-line-lightweight-agentic-rl-framework-for-training-agents-with-real-harnesses/) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-09-30](https://blog.cloudflare.com/faster-agent-sandboxes/) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-07](https://blog.cloudflare.com/agentic-security-operations/) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-06](https://arxiv.org/abs/2610.07767) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-10-07](https://blog.vllm.ai/blog/2026-10-07-deepseek-v41-flash) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 📈 accelerating | [2026-10-07](https://arxiv.org/abs/2610.04198) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-06](https://arxiv.org/abs/2610.08448) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-10-07](https://arxiv.org/abs/2610.03607) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-09-27](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-MOPD) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-10-08](https://www.anthropic.com/news/anthropic-cyber-mission) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-10-12](https://pub.sakana.ai/mass/) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-10-07](https://github.com/openai/math) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-07](https://arxiv.org/abs/2610.06833) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-10-06](https://portal.nousresearch.com/bench) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.39788) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.40360) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-10-01](https://arxiv.org/abs/2610.01787) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-09-24](https://arxiv.org/abs/2609.29861) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-09-30](https://blog.cloudflare.com/monetization-gateway-beta/) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 seed | [2026-09-29](https://arxiv.org/abs/2609.38482) |

## Worth studying

- [Math 2.0](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) — Terence Tao's own structural account of AI-driven mathematics: proof abundance, jagged capability, reporting bias, and a call for transparent assessment.
- [SGLang v0.5.21](https://github.com/sgl-project/sglang/releases/tag/v0.5.21) / [llama.cpp v0.6.0](https://github.com/ggml-org/llama.cpp/releases/tag/v0.6.0) — two inference engines ship native decision-model serving APIs in the same week.
- [Understanding the MCP Ecosystem (MCPacific)](https://arxiv.org/abs/2610.05319) — maps 368,754 MCP server listings into a capability taxonomy; presenting tools through it lifts task completion up to 12 points.
- [Whistle](https://cactuscompute.com/blog/whistle) — a 16.9MB open speech-to-text model, dependency-free on CPU, beating Whisper base.
- [Agent Lightning v1.0](https://www.microsoft.com/en-us/research/blog/agent-lightning-v1-0-a-3500-line-lightweight-agentic-rl-framework-for-training-agents-with-real-harnesses/) — trains an agent through the same harness it runs in deployment.
- [Multimodal open d1 decision models](https://huggingface.co/blog/LiquidAI/open-d1) — Liquid AI's d1-3B/d1-omni-600M beat AWS Decider at a quarter of the parameters, under 50ms on edge hardware.
- [Building an agentic security operations harness on Cloudflare](https://blog.cloudflare.com/agentic-security-operations/) — a concrete case study on why and how to split one agent into several specialized ones.
- [Sharing AI progress in mathematics](https://openai.com/index/sharing-ai-progress-in-mathematics/) — OpenAI's mass math-results release, now with externally-governed disclosure norms.
- [openTPU](https://github.com/FeSens/openTPU) — a complete open-source AI accelerator, built largely by AI coding agents.
- [Memory and dreaming: how Devin learns from working with you](https://devin.ai/blog/memory-and-dreaming) — persistent Git-backed agent memory plus a daily background consolidation pass.
- [Dust: Pretraining Transformers Without Backpropagation](https://qlabs.sh/research/dust) — the first zeroth-order method reported competitive with backprop at scale.
- [The Agent Said It Was Done. The Database Disagreed.](https://huggingface.co/blog/microsoft/thinkingbox) — a sharp argument for grading agents on backend state, not self-report.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- Hacker News discussion of [Terence Tao's "Math 2.0" talk](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) was the day's clear significance-first catch (368 points).
- [Karpathy's tweet](https://twitter.com/karpathy/status/2109361546505966046) on the widening gap in shared understanding of LLM capability drew heavy HN discussion (371 points) — commentary, no primary artifact to route.
- r/LocalLLaMA discussion of a community quantization tool for GLM-5.3 Flash ("Project Maya," ~118 tok/s on 4x RTX 4090) — below this radar's evidence bar, watch for a technical writeup.
- Mistral's [Mistral Large 4](https://mistral.ai/news/mistral-large-4/) announcement (API-only preview, weights promised "by the end of the month") was the day's top HN story a week ago and remains a live watch item.
- Reflection AI's [Beam](https://reflection.ai/blog/introducing-beam) (501B-total MoE, "advancing the Western open-weight frontier") still has no shipped weights as of this scan.

## Output map

[Full ledger](TRENDS.md) · [watchlist (23 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-10-12.md)) · weekly: [latest](reports/weekly/2026-W41.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
