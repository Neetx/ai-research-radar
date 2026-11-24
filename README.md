# AI Radar

![trends](https://img.shields.io/badge/trends-24-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-13-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-10-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--24-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-11-24):** [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) and [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) both moved emerging → dormant on an empty dormancy probe. [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) added Anthropic's AI-authored ["VP ≠ VNP" proof](https://github.com/anthropics/formal-math/tree/main/vp-vnp) — no human mathematician has checked it yet. [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) added [Cerebras's disaggregated-inference launch](https://cerebras.ai/blog/cerebras-launches-disaggregated-inference), a fourth hardware vendor reaching production. Queue: dropped a 12-day-stale cohort, added one new below-bar bundle (net 10 live lines).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 accelerating | [2026-11-20](https://vllm.ai/blog/2026-11-20-inkling2-mini) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-19](https://arxiv.org/abs/2611.26157) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-18](https://huggingface.co/blog/moe-expert-streaming) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08483) |

## Trends

🌱 4 · 📈 13 · 🚀 0 · 🌊 0 · 🏔 4 · 📉 0 · 💤 3

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 accelerating | [2026-11-20](https://vllm.ai/blog/2026-11-20-inkling2-mini) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-11-19](https://developer.nvidia.com/blog/reducing-rollout-bottlenecks-in-reinforcement-learning-with-nvidia-dynamo/) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-19](https://arxiv.org/abs/2611.26157) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-18](https://huggingface.co/blog/moe-expert-streaming) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-11-18](https://huggingface.co/blog/rumble-2-flash) |
| [Decision models](TRENDS.md#id-decision-models-024-system-1-decision-models-single-forward-pass-calibrated-classifiers-as-a-distinct-benchmarked-model-category) | 📈 accelerating | [2026-11-18](https://blog.cloudflare.com/open-clairic/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-11-18](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-11-18](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-11-17](https://cerebras.ai/blog/cerebras-launches-disaggregated-inference) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-11-17](https://developer.nvidia.com/blog/co-designing-sparse-attention-for-efficient-long-context-inference/) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-11-13](https://blog.cloudflare.com/kitesurf-open-source/) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-11-10](https://blog.modelcontextprotocol.io/posts/exploring-file-uploads-and-downloads-in-mcp/) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 📈 accelerating | [2026-11-09](https://aaif.io/blog/when-good-agents-make-bad-systems) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-11-23](https://huggingface.co/blog/agentic-evals) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-11-19](https://arxiv.org/abs/2611.25476) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-11-09](https://arxiv.org/abs/2611.12587) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08483) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-11-24](https://github.com/anthropics/formal-math/tree/main/vp-vnp) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-11-21](https://facebookresearch.github.io/RAM/blogs/self_improving_memory/) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-11-17](https://huggingface.co/tencent/Hy4-flash) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-11-17](https://www.vals.ai/blogs/autonomous-warfare) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 💤 dormant | [2026-11-03](https://arxiv.org/abs/2611.05129) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 💤 dormant | [2026-11-03](https://www.fireblocks.com/?p=32426) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 💤 dormant | [2026-10-30](https://huggingface.co/Diffuspace/Clover-35B-A3B-Preview) |

## Worth studying

- [How to build and maintain an agentic evaluation](https://huggingface.co/blog/agentic-evals) — an 8-step, directly-reusable methodology for building a deployment-grounded agent eval, plus a release checklist most teams skip.
- [VP ≠ VNP over Every Field](https://github.com/anthropics/formal-math/tree/main/vp-vnp) — a complexity-theory separation result whose paper and Lean proof were both written by an Anthropic research model, with no human mathematician check yet.
- [Perplexity and Intelligence](https://openai.com/index/perplexity-and-intelligence) — OpenAI Chief Scientist Jakub Pachocki's case for perplexity as a shared cross-lab metric and policy trigger, including the honest admission that chain-of-thought gains are invisible to it.
- [Introducing harness adapters](https://huggingface.co/blog/harness-adapters-at-scale) — RL-trained, harness-specific LoRA adapters on a frozen base model lift Terminal-Bench 2.1 pass@1 from ~39% to 55% at lower token cost.
- [Claude solves two open problems in the physics of black holes](https://www.anthropic.com/research/claude-black-hole-physics) — a ~6-week, many-agent Claude side project with an unusually rigorous verification chain (independent double-checking, two Lean kernels, a human physicist's full review).
- [SenseNova-Loop-9B](https://huggingface.co/sensenova/SenseNova-Loop-9B) — a real, open-weight looped-transformer model reaching near-Qwen3.8-27B parity at roughly a third the parameters via loop-depth plus a novel residual-stream-mixing mechanism.
- [180B Parameters, 32GB of RAM: Pushing MoE Inference to the Limit with Transformers](https://huggingface.co/blog/moe-expert-streaming) — a reproducible `transformers` recipe (3-bit expert quantization + SSD streaming) that runs a ~180B-parameter MoE on a 32GB Mac within 6% of a specialized inference engine.
- [Evolving Agent Teams](https://arxiv.org/abs/2610.36848) — a central supervisor that detects when a coding-agent team converges to a local optimum and restructures the team, writing a CUDA kernel that beats production FlashInfer by 1.2x average.
- [FrontierHarness Eval v1.1](https://runta.com/blog/introducing-frontierharness-eval-v1-1/) — 27,280 agent runs across 22 harnesses x 5 models find model choice drives ~93% of cost variance to the harness's ~2%, yet the cheapest harness flips completely depending on which model it's paired with.
- [Weight-Space Programming Doesn't Need Transformers](https://arxiv.org/abs/2611.22055) — three frontier LLMs independently asked to design a network's weights directly all converge on the same sparse-lookup-table architecture, beating the Transformer the same LLM wrote with ~1,800x fewer parameters.
- [TokenEconomizer: Learning from Experience to Make AI Coding Agents More Efficient](https://www.microsoft.com/en-us/research/blog/tokeneconomizer-learning-from-experience-to-make-ai-coding-agents-more-efficient/) — an open-source, model-agnostic plugin (micro-skills, tool pruning, a failure-loop judge) that cuts coding-agent cost 18-31% across three benchmark suites by learning from a repo's own completed sessions.
- [SwarmEvolve: Latent Agent Swarms for Evolutionary Discovery and Optimization](https://arxiv.org/abs/2611.08483) — 450 agents per round reason in latent space and share ideas by passing KV caches, beating established evolutionary-coding frameworks on throughput by 5-9x on one GPU.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- A 940-page draft claiming a proof of [the Riemann Hypothesis](https://johncarlosbaez.wordpress.com/2026/11/22/masullo-on-the-riemann-hypothesis/) is under heavy community scrutiny, including an AI-agent-assisted Lean-formalization effort still in progress; disputed, unverified.
- A looped-transformer coding model, [GLM-5.4](https://z.ai/blog/glm-5.4), drew heavy Hacker News attention today; its full post is currently inaccessible to this radar's tools (JS-rendered), so its open-weight status is unconfirmed.
- A corporate-governance story (NVIDIA's CEO reinstated) topped Hacker News today; off every tracked axis, noted here only as the earthquake check's catch, not routed anywhere.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~10 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-24.md)) · weekly: [latest](reports/weekly/2026-W47.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
