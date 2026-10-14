# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-20-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--10--14-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-14):** a Princeton/Felix-Heide-line paper on [generalist embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) rescues that trend from the 21-day dormancy line with a 5th independent group — a VLM self-distillation policy deployed across 13 real-world navigation tasks · vLLM ships bi-directional KV transfer, extending [prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) to multi-turn agentic workloads (up to 3.3x faster time-to-first-token) · a new hidden-state self-distillation signal ([PR-OPD](https://arxiv.org/abs/2609.36642)) extends [on-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) into agentic settings · Anthropic's from-scratch VCS rewrite (Scion) and Google DeepMind's Gemini 4 Argon for Robotics join the [study shelf](#worth-studying) · queue burndown drops 8 stale, never-recurring 10-08 items.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-07](https://arxiv.org/abs/2610.06833) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-06](https://arxiv.org/abs/2610.07767) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.39788) |

## Trends

🌱 8 · 📈 11 · 🚀 0 · 🌊 0 · 🏔 4 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-10-12](https://vllm.ai/blog/2026-10-12-bidirectional-kvxfer-multiturn-agentic-workload) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-10-12](https://developer.nvidia.com/blog/replayssm-rethinking-state-storage-for-faster-hybrid-model-decoding/) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-14](https://arxiv.org/abs/2609.36642) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-07](https://www.microsoft.com/en-us/research/blog/agent-lightning-v1-0-a-3500-line-lightweight-agentic-rl-framework-for-training-agents-with-real-harnesses/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-07](https://blog.cloudflare.com/agentic-security-operations/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 📈 accelerating | [2026-10-07](https://arxiv.org/abs/2610.04198) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-10-07](https://arxiv.org/abs/2610.03607) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-06](https://arxiv.org/abs/2610.07767) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-04](https://arxiv.org/abs/2610.05319) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-09-30](https://blog.cloudflare.com/faster-agent-sandboxes/) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-10-12](https://pub.sakana.ai/mass/) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-10-08](https://www.anthropic.com/news/anthropic-cyber-mission) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-10-07](https://github.com/openai/math) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-09-27](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-MOPD) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-07](https://arxiv.org/abs/2610.06833) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-10-06](https://portal.nousresearch.com/bench) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-10-01](https://arxiv.org/abs/2610.01787) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.39788) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.40360) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-09-30](https://blog.cloudflare.com/monetization-gateway-beta/) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-10-13](https://arxiv.org/abs/2610.17593) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 seed | [2026-09-29](https://arxiv.org/abs/2609.38482) |

## Worth studying

- [Redesigning source control at Anthropic](https://www.anthropic.com/engineering/redesigning-source-control) — merges grew 2,500/day → 30,000+/day as Claude took over more coding, forcing a 5-month from-scratch VCS migration (Scion).
- [Gemini 4 Argon for Robotics](https://developers.googleblog.com/gemini-4-argon-for-robotics/) — Google DeepMind's physical-reasoning model (87% ERQA) controls real robots via code-as-policies prompts, with Real2Sim digital twins from video or sketches.
- [ReplaySSM](https://developer.nvidia.com/blog/replayssm-rethinking-state-storage-for-faster-hybrid-model-decoding/) — a shared checkpoint+buffer serving fix for hybrid Mamba-2/GDN/KDA models, cutting state traffic ~50% and already in TensorRT-LLM/vLLM/FlashInfer.
- [Math 2.0](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) — Terence Tao's own structural account of AI-driven mathematics: proof abundance, jagged capability, reporting bias, and a call for transparent assessment.
- [SGLang v0.5.21](https://github.com/sgl-project/sglang/releases/tag/v0.5.21) / [llama.cpp v0.6.0](https://github.com/ggml-org/llama.cpp/releases/tag/v0.6.0) — two inference engines ship native decision-model serving APIs in the same week.
- [Understanding the MCP Ecosystem (MCPacific)](https://arxiv.org/abs/2610.05319) — maps 368,754 MCP server listings into a capability taxonomy; presenting tools through it lifts task completion up to 12 points.
- [Whistle](https://cactuscompute.com/blog/whistle) — a 16.9MB open speech-to-text model, dependency-free on CPU, beating Whisper base.
- [Agent Lightning v1.0](https://www.microsoft.com/en-us/research/blog/agent-lightning-v1-0-a-3500-line-lightweight-agentic-rl-framework-for-training-agents-with-real-harnesses/) — trains an agent through the same harness it runs in deployment.
- [Multimodal open d1 decision models](https://huggingface.co/blog/LiquidAI/open-d1) — Liquid AI's d1-3B/d1-omni-600M beat AWS Decider at a quarter of the parameters, under 50ms on edge hardware.
- [Building an agentic security operations harness on Cloudflare](https://blog.cloudflare.com/agentic-security-operations/) — a concrete case study on why and how to split one agent into several specialized ones.
- [Sharing AI progress in mathematics](https://openai.com/index/sharing-ai-progress-in-mathematics/) — OpenAI's mass math-results release, now with externally-governed disclosure norms.
- [openTPU](https://github.com/FeSens/openTPU) — a complete open-source AI accelerator, built largely by AI coding agents.
- [Dust: Pretraining Transformers Without Backpropagation](https://qlabs.sh/research/dust) — the first zeroth-order method reported competitive with backprop at scale.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- Anthropic's [Scion rewrite](https://www.anthropic.com/engineering/redesigning-source-control) and Google DeepMind's [Gemini 4 Argon for Robotics](https://developers.googleblog.com/gemini-4-argon-for-robotics/) both topped today's HN/AlphaSignal front pages.
- HN discussion of an [openai/codex GitHub issue](https://github.com/openai/codex/issues/48195) on a silently-installed, self-updating background daemon (515 points) — still unresolved, below the evidence bar.
- [Agent37](https://www.ycombinator.com/launches) launched on HN claiming low-cost agent sandboxes at under 10% of other providers' cost — too new to verify.
- Mistral's [Mistral Large 4](https://mistral.ai/news/mistral-large-4/) and Reflection AI's [Beam](https://reflection.ai/blog/introducing-beam) both remain weights-unshipped, over a week after their announcements.
- Reddit was unreachable via both direct JSON and the proxy fallback this scan — no fresh r/LocalLLaMA signal today; HN and AlphaSignal covered the earthquake-check role.

## Output map

[Full ledger](TRENDS.md) · [watchlist (28 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-10-14.md)) · weekly: [latest](reports/weekly/2026-W41.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
