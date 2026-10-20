# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-24-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--10--20-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-20):** Independent researchers at [Redact](https://redact.dev/blog/whatsapp-help-pages-hidden-ai-instructions) found hidden, invisible-to-users HTML text on WhatsApp's own help pages instructing AI assistants to suppress regulator/privacy-law information — a real, in-the-wild instance of [indirect prompt injection](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) from the page's own operator · vLLM's [near-zero-downtime elastic expert parallelism](https://vllm.ai/blog/2026-10-19-elastic-ep-near-zero-downtime) cuts MoE-deployment rescale pauses from ~100s to ~1-2s, landing on [prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) · Google DeepMind's [XYEval](https://arxiv.org/abs/2609.23939) shows one confidently-wrong user hint costs frontier agents up to 46.7% relative performance, feeding [deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) · ["Into the Unknown"](https://arxiv.org/abs/2610.19159) has nine frontier agents write follow-up papers on open scientific problems — 0 of 135 submissions pass, landing on [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-18](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-15](https://research.meta.ai/blog/muse-spark-open) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-14](https://arxiv.org/abs/2610.20951) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.39788) |

## Trends

🌱 8 · 📈 11 · 🚀 0 · 🌊 0 · 🏔 4 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-10-19](https://vllm.ai/blog/2026-10-19-elastic-ep-near-zero-downtime) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-18](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-10-18](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-15](https://research.meta.ai/blog/muse-spark-open) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-10-15](https://arxiv.org/abs/2610.22364) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-15](https://arxiv.org/abs/2610.21601) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-07](https://www.microsoft.com/en-us/research/blog/agent-lightning-v1-0-a-3500-line-lightweight-agentic-rl-framework-for-training-agents-with-real-harnesses/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-07](https://blog.cloudflare.com/agentic-security-operations/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 📈 accelerating | [2026-10-07](https://arxiv.org/abs/2610.04198) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-04](https://arxiv.org/abs/2610.05319) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-09-30](https://blog.cloudflare.com/faster-agent-sandboxes/) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-10-19](https://arxiv.org/abs/2609.23939) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22322) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-14](https://arxiv.org/abs/2610.20951) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-10-13](https://arxiv.org/abs/2610.17593) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-10-01](https://arxiv.org/abs/2610.01787) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.39788) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-09-30](https://arxiv.org/abs/2609.40360) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-09-30](https://blog.cloudflare.com/monetization-gateway-beta/) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-10-19](https://redact.dev/blog/whatsapp-help-pages-hidden-ai-instructions) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-10-19](https://blog.cloudflare.com/clairic-extraction-model/) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-10-16](https://huggingface.co/blog/reflection-beam) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-10-13](https://arxiv.org/abs/2610.19159) |

## Worth studying

- [XYEval: Agents Say Yes to Bad Advice](https://arxiv.org/abs/2609.23939) — one confidently-wrong user hint costs frontier agents up to 46.7% relative performance, even though they privately know it's wrong 92.1% of the time.
- [Near-Zero-Downtime Elastic Expert Parallelism](https://vllm.ai/blog/2026-10-19-elastic-ep-near-zero-downtime) — cuts the pause for scaling a live MoE deployment's GPUs from ~100s to ~1-2s via background preparation and in-place communicator/CUDA-graph reuse.
- [Waypoint-OPD](https://arxiv.org/abs/2610.21601) — gates on-policy distillation's teacher signal by checking whether an RL run's early and late policy shifts actually agree, not just its net endpoint delta.
- [Muse Spark Open](https://research.meta.ai/blog/muse-spark-open) — Meta's 816B/42B-active open-weight MoE, engineered to run end-to-end on two Mac Studios via MLX rather than just a datacenter, with day-0 agentic demos.
- [OpenCode 2.0](https://anoma.ly/notes/opencode-2-0/) — a production-grade reference design for the architectural questions (client/server split, tool-composition layer, background orchestration) anyone building an agent harness has to answer.
- [RoboJEPA: Scaling Robotic Latent World Models](https://arxiv.org/abs/2610.10515) — a rare genuine scaling-law study (not just a bigger model) applied to embodied/robotic world models.
- [Redesigning source control at Anthropic](https://www.anthropic.com/engineering/redesigning-source-control) — merges grew 2,500/day → 30,000+/day as Claude took over more coding, forcing a 5-month from-scratch VCS migration (Scion).
- [Gemini 4 Argon for Robotics](https://developers.googleblog.com/gemini-4-argon-for-robotics/) — Google DeepMind's physical-reasoning model (87% ERQA) controls real robots via code-as-policies prompts, with Real2Sim digital twins from video or sketches.
- [ReplaySSM](https://developer.nvidia.com/blog/replayssm-rethinking-state-storage-for-faster-hybrid-model-decoding/) — a shared checkpoint+buffer serving fix for hybrid Mamba-2/GDN/KDA models, cutting state traffic ~50% and already in TensorRT-LLM/vLLM/FlashInfer.
- [Math 2.0](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) — Terence Tao's own structural account of AI-driven mathematics: proof abundance, jagged capability, reporting bias, and a call for transparent assessment.
- [SGLang v0.5.21](https://github.com/sgl-project/sglang/releases/tag/v0.5.21) / [llama.cpp v0.6.0](https://github.com/ggml-org/llama.cpp/releases/tag/v0.6.0) — two inference engines ship native decision-model serving APIs in the same week.
- [Understanding the MCP Ecosystem (MCPacific)](https://arxiv.org/abs/2610.05319) — maps 368,754 MCP server listings into a capability taxonomy; presenting tools through it lifts task completion up to 12 points.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- [MiniMax M3.1 Flash](https://www.minimax.io/blog/minimax-m31f) claims a "generational leap in agentic tasks" but is API-only for now; open weights are promised later, the same unshipped pattern as Mistral Large 4.
- An [early-stage RuneScape gameplay benchmark](https://maxbittker.github.io/runebench/) has coding agents write tools to play live, via TypeScript — no model scores reported yet, and the authors call their own results noisy.
- An [Ask HN thread](https://hn.algolia.com/api/v1/search?tags=front_page) on "how to deal with shipping AI-written code you don't understand" drew 347 points — a practitioner-discourse signal, no primary artifact to follow.
- Mistral's [Large 4](https://huggingface.co/mistralai/Mistral-Large-4-1T-A52B) remains API-preview-only; the company's own announcement still gives an end-of-month weights ETA.
- Reddit's r/LocalLLaMA JSON endpoint remains blocked (HTML interstitial); HN and AlphaSignal continue covering the earthquake-check role.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~24 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-10-20.md)) · weekly: [latest](reports/weekly/2026-W42.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
