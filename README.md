# AI Radar

![trends](https://img.shields.io/badge/trends-24-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-12-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-8-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--21-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-11-21):** Weekly recalibration — no new trend evidence or stage moves this run; externalized old [`observation_queue`](TRENDS.md#observation_queue) tombstones to a new append-only log to keep the ledger lean, pruned the study shelf, and promoted Tencent Hunyuan to a swept [source](SOURCES.md).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-18](https://huggingface.co/blog/moe-expert-streaming) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-17](https://huggingface.co/sensenova/SenseNova-Loop-9B) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08483) |

## Trends

🌱 7 · 📈 12 · 🚀 0 · 🌊 0 · 🏔 4 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-11-19](https://developer.nvidia.com/blog/reducing-rollout-bottlenecks-in-reinforcement-learning-with-nvidia-dynamo/) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-11-18](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-18](https://huggingface.co/blog/moe-expert-streaming) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-11-18](https://huggingface.co/blog/rumble-2-flash) |
| [Decision models](TRENDS.md#id-decision-models-024-system-1-decision-models-single-forward-pass-calibrated-classifiers-as-a-distinct-benchmarked-model-category) | 📈 accelerating | [2026-11-18](https://blog.cloudflare.com/open-clairic/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-11-18](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-11-17](https://developer.nvidia.com/blog/co-designing-sparse-attention-for-efficient-long-context-inference/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-11-16](https://developer.nvidia.com/blog/nvidia-vera-rubin-nvl72-leads-agentic-inference-performance-on-mlperf-endpoints-v1-0/) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-11-13](https://blog.cloudflare.com/kitesurf-open-source/) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-11-10](https://blog.modelcontextprotocol.io/posts/exploring-file-uploads-and-downloads-in-mcp/) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 📈 accelerating | [2026-11-09](https://aaif.io/blog/when-good-agents-make-bad-systems) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-11-18](https://arxiv.org/abs/2611.22055) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-11-18](https://runta.com/blog/introducing-frontierharness-eval-v1-1/) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-17](https://huggingface.co/sensenova/SenseNova-Loop-9B) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-11-09](https://arxiv.org/abs/2611.12587) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08483) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05129) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-11-03](https://www.fireblocks.com/?p=32426) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-11-19](https://arxiv.org/abs/2611.23068) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-11-17](https://www.vals.ai/blogs/autonomous-warfare) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-11-17](https://www.anthropic.com/research/claude-black-hole-physics) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-11-17](https://huggingface.co/tencent/Hy4-flash) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 💤 dormant | [2026-10-30](https://huggingface.co/Diffuspace/Clover-35B-A3B-Preview) |

## Worth studying

- [Claude solves two open problems in the physics of black holes](https://www.anthropic.com/research/claude-black-hole-physics) — a ~6-week, many-agent Claude side project with an unusually rigorous verification chain (independent double-checking, two Lean kernels, a human physicist's full review).
- [SenseNova-Loop-9B](https://huggingface.co/sensenova/SenseNova-Loop-9B) — a real, open-weight looped-transformer model reaching near-Qwen3.8-27B parity at roughly a third the parameters via loop-depth plus a novel residual-stream-mixing mechanism.
- [180B Parameters, 32GB of RAM: Pushing MoE Inference to the Limit with Transformers](https://huggingface.co/blog/moe-expert-streaming) — a reproducible `transformers` recipe (3-bit expert quantization + SSD streaming) that runs a ~180B-parameter MoE on a 32GB Mac within 6% of a specialized inference engine.
- [Evolving Agent Teams](https://arxiv.org/abs/2610.36848) — a central supervisor that detects when a coding-agent team converges to a local optimum and restructures the team, writing a CUDA kernel that beats production FlashInfer by 1.2x average.
- [FrontierHarness Eval v1.1](https://runta.com/blog/introducing-frontierharness-eval-v1-1/) — 27,280 agent runs across 22 harnesses x 5 models find model choice drives ~93% of cost variance to the harness's ~2%, yet the cheapest harness flips completely depending on which model it's paired with.
- [Weight-Space Programming Doesn't Need Transformers](https://arxiv.org/abs/2611.22055) — three frontier LLMs independently asked to design a network's weights directly all converge on the same sparse-lookup-table architecture, beating the Transformer the same LLM wrote with ~1,800x fewer parameters.
- [TokenEconomizer: Learning from Experience to Make AI Coding Agents More Efficient](https://www.microsoft.com/en-us/research/blog/tokeneconomizer-learning-from-experience-to-make-ai-coding-agents-more-efficient/) — an open-source, model-agnostic plugin (micro-skills, tool pruning, a failure-loop judge) that cuts coding-agent cost 18-31% across three benchmark suites by learning from a repo's own completed sessions.
- [SwarmEvolve: Latent Agent Swarms for Evolutionary Discovery and Optimization](https://arxiv.org/abs/2611.08483) — 450 agents per round reason in latent space and share ideas by passing KV caches, beating established evolutionary-coding frameworks on throughput by 5-9x on one GPU.
- [Advancing science & engineering with Antigravity's /teamwork](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) — a dense, cross-domain accounting of what a verified multi-agent team produces (Lean-checked proofs, a 95%-accurate chemistry pipeline, 60-90x graph throughput, Rust rewrites, scheduler tuning), each result checked by an automated verifier.
- [llama.cpp v1.0.0: A stronger foundation for the local AI ecosystem](https://huggingface.co/blog/ggml-org/llama-cpp-v1) — the local-inference substrate most of the small/CPU-model ecosystem builds on adopts semantic versioning and expands its CI/distribution footprint across six major hardware vendors.
- [A Lean Proof of the Thomson Problem for Seven Electrons](https://www.vals.ai/blogs/thomson-n7-lean-proof) — ten Claude Sonnet 5.5 agents produced a 17,895-line, two-kernel-verified Lean proof in ~15 hours, extending a prior N=8 proof to the next case.
- [LLMON: An LLM-Native Markup Language](https://huggingface.co/blog/ibm-granite/llmon-an-llm-native-markup-language-now-in-granite) — a reserved-token markup that keeps context structure in a separate part of the vocabulary than content, so injected text can't fake a boundary.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- Anthropic [priced its initial public offering](https://www.reuters.com/business/finance/anthropics-historic-debut-put-ais-promise-peril-wall-st-test-2026-11-19/) on Nasdaq.
- OpenAI's "Introducing GPT‑6.2 Astra and Sol" stayed unreachable again this run — openai.com would not load under the tools available; still unverified.
- [Sakana AI launched an independent public-interest cyber-defense lab](https://sakana.ai/) in Tokyo, per today's curator-lane sweep.
- A paper-review channel flagged a NeurIPS oral on [formally-verified agent planning](https://arxiv.org/abs/2611.17880), named but not yet promoted.
- Commentary is debating [whether governments should slow down frontier AI development](https://www.youtube.com/watch?v=lwfewYL7X0o).

## Output map

[Full ledger](TRENDS.md) · [watchlist (~8 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-20.md)) · weekly: [latest](reports/weekly/2026-W47.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
