# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-10-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-15-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--10--24-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-24, weekly recalibration):** this week's low-cadence source sweep closed a 9-day capture gap on [small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) — PrismML's own blog had quietly shipped [Bonsai 2 in 2B/4B/9B sizes](https://prismml.com/news/prismml-expands-bonsai-2-family-with-2b-4b-and-9b-models-for-on-device-ai), phone-class ternary models extending the already-tracked 27B · no trend crossed the 21-day dormancy line this week ([multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) is closest, 17 days) · the study shelf's ≤09-23 tail was pruned to the archive (nothing lost, see [the weekly report](reports/weekly/2026-W43.md)).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-21](https://alphasignal.ai/news/recursive-si-s-flint-runs-a-40b-coding-model-on-your-laptop) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-18](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-21](https://arxiv.org/abs/2610.27628) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-10](https://arxiv.org/abs/2610.15095) |

## Trends

🌱 8 · 📈 10 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-22](https://huggingface.co/blog/microsoft/thinkingbox-training) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-22](https://arxiv.org/abs/2610.31563) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-21](https://blog.cloudflare.com/webmcp-commerce/) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-21](https://alphasignal.ai/news/recursive-si-s-flint-runs-a-40b-coding-model-on-your-laptop) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-10-21](https://arxiv.org/abs/2610.26855) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-10-19](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-10-19](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-18](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-10-14](https://vercel.com/blog/findings-from-the-1-million-dollar-vercel-sandbox-challenge) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-07](https://blog.cloudflare.com/agentic-security-operations/) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-10-22](https://arxiv.org/abs/2610.31544) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-21](https://arxiv.org/abs/2610.27628) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-10-19](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents/blob/main/benchmarking-new-models-on-slop-code-bench.md) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22070) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22322) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-10-14](https://www.chainalysis.com/blog/north-america-crypto-adoption-2026) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-10-13](https://arxiv.org/abs/2610.17593) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-10](https://arxiv.org/abs/2610.15095) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-10-22](https://arxiv.org/abs/2610.28577) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-10-22](https://www.anthropic.com/research/formal-verification) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-10-21](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-19](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-10-16](https://huggingface.co/blog/reflection-beam) |

## Worth studying

- [LLMs are making formal software verification feasible at a much larger scale](https://www.anthropic.com/research/formal-verification) — Anthropic + Theorem have Claude prove 239 open-source libraries crash-free via machine-checked proofs, with an honest account of what "verified" does not mean.
- [Cache Engineering for Agents](https://arxiv.org/abs/2610.28577) — lets an agent directly drop or reposition pieces of its own KV cache instead of re-prefilling after every context trim.
- [Compromised LiteLLM 1.107.0 on PyPI Installs a Credential Stealer and Backdoor](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) — a real supply-chain attack on the widely-used LiteLLM gateway, targeting AI-tool and LLM-provider credentials specifically.
- [Patch the Planet: global response coordination as agents uncover critical vulnerabilities](https://openai.com/index/coordinated-disclosure-of-critical-vulnerabilities/) — what agentic vulnerability-discovery at internet scale actually requires operationally, not just technically.
- [DeepInfer](https://github.com/deepseek-ai/DeepInfer) — DeepSeek open-sources its own in-house production inference framework, confirmed official by the lab itself and today's #1 Hacker News story by a wide margin.
- [Findings from the $1M Vercel Sandbox challenge](https://vercel.com/blog/findings-from-the-1-million-dollar-vercel-sandbox-challenge) — a public bug bounty found a real production host-memory-leak zero-day in a major agent-sandbox vendor's microVM isolation.
- [XYEval: Agents Say Yes to Bad Advice](https://arxiv.org/abs/2609.23939) — one confidently-wrong user hint costs frontier agents up to 46.7% relative performance, even though they privately know it's wrong 92.1% of the time.
- [Near-Zero-Downtime Elastic Expert Parallelism](https://vllm.ai/blog/2026-10-19-elastic-ep-near-zero-downtime) — cuts the pause for scaling a live MoE deployment's GPUs from ~100s to ~1-2s via background preparation and in-place communicator/CUDA-graph reuse.
- [Waypoint-OPD](https://arxiv.org/abs/2610.21601) — gates on-policy distillation's teacher signal by checking whether an RL run's early and late policy shifts actually agree, not just its net endpoint delta.
- [Muse Spark Open](https://research.meta.ai/blog/muse-spark-open) — Meta's 816B/42B-active open-weight MoE, engineered to run end-to-end on two Mac Studios via MLX rather than just a datacenter, with day-0 agentic demos.
- [OpenCode 2.0](https://anoma.ly/notes/opencode-2-0/) — a production-grade reference design for the architectural questions (client/server split, tool-composition layer, background orchestration) anyone building an agent harness has to answer.
- [RoboJEPA: Scaling Robotic Latent World Models](https://arxiv.org/abs/2610.10515) — a rare genuine scaling-law study (not just a bigger model) applied to embodied/robotic world models.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- [xAI's Grok gains OS-permissioned access](https://alphasignal.ai/news/xai-s-grok-reaches-into-your-phone-s-calendar-and-contacts) to phone Calendar, Reminders and Contacts data, broadening its already-tracked persistent-agent identity's data surface.
- A same-day HF-daily-papers cluster on embodied/world-model agents — [SpatialScout](https://arxiv.org/abs/2610.26659), [Right Screen, Wrong Transition](https://arxiv.org/abs/2610.11942) and [Agent World Model in the Wild](https://arxiv.org/abs/2610.26828) — watching for a third independent group to converge.
- Cloudflare's own account of [cutting an internal agent's inference bill by 68%](https://blog.cloudflare.com/obsessive-inference-optimization/) via agent-directed cost/latency optimization of its own harness.
- A candidate 14th cluster on cross-model latent communication, [CacheBack](https://arxiv.org/abs/2609.32046), prunes up to 94% of redundant multi-agent KV-cache via a receiver-conditioned attention mask.
- Reddit's direct JSON endpoints remain blocked; the YouTube curator Atom feed is re-confirmed re-blocked; HN and AlphaSignal continue covering the earthquake-check role.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~15 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-10-23.md)) · weekly: [latest](reports/weekly/2026-W43.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
