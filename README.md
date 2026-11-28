# AI Radar

![trends](https://img.shields.io/badge/trends-24-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-12-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-9-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--28-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-11-28):** [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) promoted accelerating → mainstreaming — now documented across five hardware vendors and both major open-source serving engines, via [Cerebras's production launch](https://cerebras.ai/blog/cerebras-launches-disaggregated-inference). [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) raised confidence low → medium on a converging "weight-space programming" cluster, via [WeightCode](https://arxiv.org/abs/2611.25476). Applied [amendment W47-P1](routines/daily.md) making the daily's tier-ii source rotation deterministic and mandatory; archived 10 [study-shelf](TRENDS.md#study_shelf) picks older than 30 days, queue holds steady at [9 live lines](TRENDS.md#observation_queue).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-24](https://prismml.com/news/bonsai-2-5-27b) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 accelerating | [2026-11-25](https://arxiv.org/abs/2611.34923) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-19](https://arxiv.org/abs/2611.26157) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-25](https://arxiv.org/abs/2611.34278) |

## Trends

🌱 4 · 📈 12 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 3

| trend | stage | latest signal |
|---|---|---|
| [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 accelerating | [2026-11-25](https://arxiv.org/abs/2611.34923) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-11-25](https://arxiv.org/abs/2611.34051) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-11-24](https://blog.modelcontextprotocol.io/posts/mcp-turns-two/) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-24](https://prismml.com/news/bonsai-2-5-27b) |
| [Decision models](TRENDS.md#id-decision-models-024-system-1-decision-models-single-forward-pass-calibrated-classifiers-as-a-distinct-benchmarked-model-category) | 📈 accelerating | [2026-11-24](https://arxiv.org/abs/2611.32100) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-11-19](https://developer.nvidia.com/blog/reducing-rollout-bottlenecks-in-reinforcement-learning-with-nvidia-dynamo/) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-19](https://arxiv.org/abs/2611.26157) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-11-19](https://arxiv.org/abs/2611.25595) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-11-18](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-11-18](https://huggingface.co/blog/rumble-2-flash) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-11-13](https://blog.cloudflare.com/kitesurf-open-source/) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 📈 accelerating | [2026-11-09](https://aaif.io/blog/when-good-agents-make-bad-systems) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-25](https://arxiv.org/abs/2611.34278) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-11-23](https://huggingface.co/blog/agentic-evals) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-11-19](https://arxiv.org/abs/2611.25476) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-11-09](https://arxiv.org/abs/2611.12587) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-11-25](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-11-21](https://facebookresearch.github.io/RAM/blogs/self_improving_memory/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🏔 mainstreaming | [2026-11-17](https://cerebras.ai/blog/cerebras-launches-disaggregated-inference) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-11-17](https://huggingface.co/tencent/Hy4-flash) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-11-17](https://www.vals.ai/blogs/autonomous-warfare) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 💤 dormant | [2026-11-03](https://arxiv.org/abs/2611.05129) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 💤 dormant | [2026-11-03](https://www.fireblocks.com/?p=32426) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 💤 dormant | [2026-10-30](https://huggingface.co/Diffuspace/Clover-35B-A3B-Preview) |

## Worth studying

- [Swarms, Flocks, Gangs: How to build, train, and evaluate multi-agent systems](https://huggingface.co/blog/training-swarms) — a directly-runnable TRL recipe (shared-policy agents, a shrinking-token-budget team reward) that takes a team from 6.6% to 82.3% success while cutting tokens/attempt ~37%.
- [The matrix multiplication exponent is nine fourths](https://github.com/openai/math/tree/main/preprints) — OpenAI's internal model claims a matching lower bound for ω=9/4, the first non-trivial unconditional lower bound of this kind ever proved, if it survives scrutiny.
- [Cogentic](https://github.com/google-research/google-research/tree/master/cogentic_research_papers) — Google's multi-agent proof-discovery harness (prover populations, adversarial verification, a persistent verified ledger), worth studying as an architecture independent of whether every individual claim holds up.
- [Rewirable Circuits in Transformers with Loom Attention](https://arxiv.org/abs/2611.30634) — a genuinely new point in the attention design space: splitting control (a per-token matrix memory) from content (ordinary token attention) into two residual streams.
- [Ternary Bonsai 2.5 27B](https://prismml.com/news/bonsai-2-5-27b) — a 5.9GB ternary 27B model that closes much of the agentic/coding gap to its full-precision base (SWE-bench Verified 75.6 vs. 80.6).
- [How to build and maintain an agentic evaluation](https://huggingface.co/blog/agentic-evals) — an 8-step, directly-reusable methodology for building a deployment-grounded agent eval, plus a release checklist most teams skip.
- [VP ≠ VNP over Every Field](https://github.com/anthropics/formal-math/tree/main/vp-vnp) — a complexity-theory separation result whose paper and Lean proof were both written by an Anthropic research model, with no human mathematician check yet.
- [Perplexity and Intelligence](https://openai.com/index/perplexity-and-intelligence) — OpenAI Chief Scientist Jakub Pachocki's case for perplexity as a shared cross-lab metric and policy trigger, including the honest admission that chain-of-thought gains are invisible to it.
- [Introducing harness adapters](https://huggingface.co/blog/harness-adapters-at-scale) — RL-trained, harness-specific LoRA adapters on a frozen base model lift Terminal-Bench 2.1 pass@1 from ~39% to 55% at lower token cost.
- [Claude solves two open problems in the physics of black holes](https://www.anthropic.com/research/claude-black-hole-physics) — a ~6-week, many-agent Claude side project with an unusually rigorous verification chain (independent double-checking, two Lean kernels, a human physicist's full review).
- [SenseNova-Loop-9B](https://huggingface.co/sensenova/SenseNova-Loop-9B) — a real, open-weight looped-transformer model reaching near-Qwen3.8-27B parity at roughly a third the parameters via loop-depth plus a novel residual-stream-mixing mechanism.
- [180B Parameters, 32GB of RAM: Pushing MoE Inference to the Limit with Transformers](https://huggingface.co/blog/moe-expert-streaming) — a reproducible `transformers` recipe (3-bit expert quantization + SSD streaming) that runs a ~180B-parameter MoE on a 32GB Mac within 6% of a specialized inference engine.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- A sprawling, independently-unverified cluster of same-day AI-authored math/CS claims — [a matrix-multiplication-exponent lower bound](https://github.com/openai/math/tree/main/preprints), [a new unconditional subexponential factoring algorithm](https://github.com/google-research/google-research/tree/master/cogentic_research_papers), and [a quantum-complexity result](https://arxiv.org/abs/2611.31236) — drew the loudest reaction of the week on Hacker News ("Holy shit holy shit...", 1195pts).
- A looped-transformer coding model, [GLM-5.4](https://z.ai/blog/glm-5.4), remains inaccessible to this radar's tools (JS-rendered shell) across several days of re-attempts; its open-weight status stays unconfirmed.
- A disputed 940-page draft claiming a proof of [the Riemann Hypothesis](https://johncarlosbaez.wordpress.com/2026/11/22/masullo-on-the-riemann-hypothesis/) remains under heavy community scrutiny, including an AI-agent-assisted Lean-formalization effort.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~9 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-27.md)) · weekly: [latest](reports/weekly/2026-W48.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
