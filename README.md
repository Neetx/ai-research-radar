# AI Radar

![trends](https://img.shields.io/badge/trends-24-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-12-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-7-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--18-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-11-18):** [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) added a 27,280-run study, [FrontierHarness Eval v1.1](https://runta.com/blog/introducing-frontierharness-eval-v1-1/), finding the model (not the harness) drives ~93% of agent cost variance · [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) added a rigorous follow-up, [Weight-Space Programming Doesn't Need Transformers](https://arxiv.org/abs/2611.22055), showing an LLM-designed sparse lookup table beats a Transformer the same LLM wrote with ~1,800x fewer parameters.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-16](https://huggingface.co/papers/2611.20404) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-12](https://edge0.ai/blog/introducing-edge0-145b-frontier-ai-capabilities-on-your-own-computer) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08483) |

## Trends

🌱 7 · 📈 12 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-11-16](https://developer.nvidia.com/blog/nvidia-vera-rubin-nvl72-leads-agentic-inference-performance-on-mlperf-endpoints-v1-0/) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-11-13](https://blog.cloudflare.com/kitesurf-open-source/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-11-13](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-12](https://edge0.ai/blog/introducing-edge0-145b-frontier-ai-capabilities-on-your-own-computer) |
| [Decision models](TRENDS.md#id-decision-models-024-system-1-decision-models-single-forward-pass-calibrated-classifiers-as-a-distinct-benchmarked-model-category) | 📈 accelerating | [2026-11-12](https://arxiv.org/abs/2611.16321) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-11-11](https://huggingface.co/blog/qvac/botpsy) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-11-10](https://blog.modelcontextprotocol.io/posts/exploring-file-uploads-and-downloads-in-mcp/) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 📈 accelerating | [2026-11-09](https://aaif.io/blog/when-good-agents-make-bad-systems) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-11-06](https://huggingface.co/blog/allenai/toyblocks) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-11-03](https://arxiv.org/abs/2611.04671) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-11-02](https://developer.nvidia.com/blog/build-world-models-for-interactive-simulation-with-nvidia-cosmos/) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-11-18](https://runta.com/blog/introducing-frontierharness-eval-v1-1/) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-11-18](https://arxiv.org/abs/2611.22055) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-16](https://huggingface.co/papers/2611.20404) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-11-09](https://arxiv.org/abs/2611.12587) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08483) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05129) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-11-03](https://www.fireblocks.com/?p=32426) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-11-16](https://www.microsoft.com/en-us/research/blog/tokeneconomizer-learning-from-experience-to-make-ai-coding-agents-more-efficient/) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-11-13](https://blog.cloudflare.com/adapting-to-ai-penetration-testing-orchestrators/) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-11-10](https://deepmind.google/blog/introducing-alphaproof-code/) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-11-05](https://ernie.baidu.com/release/ernie-5-5-flash-base/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-30](https://huggingface.co/Diffuspace/Clover-35B-A3B-Preview) |

## Worth studying

- [FrontierHarness Eval v1.1](https://runta.com/blog/introducing-frontierharness-eval-v1-1/) — 27,280 agent runs across 22 harnesses x 5 models find model choice drives ~93% of cost variance to the harness's ~2%, yet the cheapest harness flips completely depending on which model it's paired with.
- [Weight-Space Programming Doesn't Need Transformers](https://arxiv.org/abs/2611.22055) — three frontier LLMs independently asked to design a network's weights directly all converge on the same sparse-lookup-table architecture, beating the Transformer the same LLM wrote with ~1,800x fewer parameters.
- [TokenEconomizer: Learning from Experience to Make AI Coding Agents More Efficient](https://www.microsoft.com/en-us/research/blog/tokeneconomizer-learning-from-experience-to-make-ai-coding-agents-more-efficient/) — an open-source, model-agnostic plugin (micro-skills, tool pruning, a failure-loop judge) that cuts coding-agent cost 18-31% across three benchmark suites by learning from a repo's own completed sessions.
- [SwarmEvolve: Latent Agent Swarms for Evolutionary Discovery and Optimization](https://arxiv.org/abs/2611.08483) — 450 agents per round reason in latent space and share ideas by passing KV caches, beating established evolutionary-coding frameworks on throughput by 5-9x on one GPU.
- [Advancing science & engineering with Antigravity's /teamwork](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) — a dense, cross-domain accounting of what a verified multi-agent team produces (Lean-checked proofs, a 95%-accurate chemistry pipeline, 60-90x graph throughput, Rust rewrites, scheduler tuning), each result checked by an automated verifier.
- [llama.cpp v1.0.0: A stronger foundation for the local AI ecosystem](https://huggingface.co/blog/ggml-org/llama-cpp-v1) — the local-inference substrate most of the small/CPU-model ecosystem builds on adopts semantic versioning and expands its CI/distribution footprint across six major hardware vendors.
- [A Lean Proof of the Thomson Problem for Seven Electrons](https://www.vals.ai/blogs/thomson-n7-lean-proof) — ten Claude Sonnet 5.5 agents produced a 17,895-line, two-kernel-verified Lean proof in ~15 hours, extending a prior N=8 proof to the next case.
- [LLMON: An LLM-Native Markup Language](https://huggingface.co/blog/ibm-granite/llmon-an-llm-native-markup-language-now-in-granite) — a reserved-token markup that keeps context structure in a separate part of the vocabulary than content, so injected text can't fake a boundary.
- [Top Chinese Frontier AI Models Carry the Fingerprint of Export-Controlled NVIDIA Blackwell GPUs](https://unemploymentlabs.com/checkpoint-forensics) — recovers a model's training-hardware fingerprint directly from its own published weights, confirmed on physical chips for two of six models.
- [My AI Agents Found an Unmapped Maya Site](https://pietromiotti.com/latest/maya-site) — a first-hand diary of 48 agents triaging public lidar strips with no classifier, flagging a real unregistered archaeological site.
- [Decision Models in Hugging Face](https://huggingface.co/blog/decision) — a concise introduction to a model category every practitioner building routing/classification/guardrail logic should know.
- [Introducing AlphaProof Code](https://deepmind.google/blog/introducing-alphaproof-code/) — a multi-LLM agentic framework that formally verified Signal's cryptographic protocol down to compiled-code depth (6M+ lines of machine-checked Lean) in four weeks, a task that historically took expert teams years.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- OpenAI's [GPT‑6.2 Astra and Sol](https://openai.com/index/introducing-gpt-6-2-astra-sol) topped today's Hacker News front page, but the announcement page was unreachable this run — not yet verified or routed.
- Microsoft AI introduced [MAI Code 2 and Code 2 Flash](https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/), proprietary coding models shipping in GitHub Copilot.
- A new paper, [TeleChat to Xing4](https://arxiv.org/abs/2611.22115), details a 285B-parameter model trained on Huawei Ascend hardware.
- Per AlphaSignal, Cognition's Devin now runs parallel coding sessions at [2,000 pull requests a week](https://alphasignal.ai/).
- Per AlphaSignal, Google's [Gemini Tasks](https://alphasignal.ai/) makes calls, shops, and runs apps on a user's behalf.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~7 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-18.md)) · weekly: [latest](reports/weekly/2026-W46.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
