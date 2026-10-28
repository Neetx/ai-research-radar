# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-10-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-6-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--10--28-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-28):** [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) gained its most authoritative entrant yet — DeepMind's own [Genie 4](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/), a natively multimodal, real-time-steerable world model · [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) added Anthropic's [drug-development case-study program](https://www.anthropic.com/research/early-progress-drug-development) across six external biotech/pharma partnerships · ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) jumped a full model generation with Liquid AI's [LFM3](https://www.liquid.ai/blog/lfm3) · the observation queue's oldest cohort (the 10-21 batch) was burned down with no recurrence found.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-27](https://www.liquid.ai/blog/lfm3) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-26](https://arxiv.org/abs/2610.34824) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-26](https://arxiv.org/abs/2610.35556) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-23](https://arxiv.org/abs/2610.32871) |

## Trends

🌱 8 · 📈 10 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-10-27](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-27](https://www.liquid.ai/blog/lfm3) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-27](https://arxiv.org/abs/2610.34467) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-10-26](https://blog.cloudflare.com/kv-cache-exposure-remediation/) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-26](https://arxiv.org/abs/2610.34824) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-10-23](https://vllm.ai/blog/2026-10-23-glm53-part2-pcp-dcp-hisparse) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-22](https://huggingface.co/blog/microsoft/thinkingbox-training) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-22](https://arxiv.org/abs/2610.31563) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-21](https://blog.cloudflare.com/webmcp-commerce/) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-10-14](https://vercel.com/blog/findings-from-the-1-million-dollar-vercel-sandbox-challenge) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-26](https://arxiv.org/abs/2610.35556) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-23](https://arxiv.org/abs/2610.32871) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-10-22](https://arxiv.org/abs/2610.31544) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-10-19](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents/blob/main/benchmarking-new-models-on-slop-code-bench.md) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22070) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22322) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-10-14](https://www.chainalysis.com/blog/north-america-crypto-adoption-2026) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-10-13](https://arxiv.org/abs/2610.17593) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-10-27](https://www.anthropic.com/research/early-progress-drug-development) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-10-23](https://vllm.ai/blog/2026-10-23-minimax-m31-flash) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-10-22](https://arxiv.org/abs/2610.28577) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-10-21](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-19](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) |

## Worth studying

- [Genie 4: A new generation of world simulation](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) — DeepMind's newest world model generates audio, dialogue and visuals simultaneously and lets you steer the evolving simulation in real time via natural language.
- [Early progress on accelerating drug development with Claude](https://www.anthropic.com/research/early-progress-drug-development) — a frontier lab's own candid account of where an LLM actually helps (and doesn't yet) across the full drug-development pipeline, from six simultaneous external biotech/pharma partnerships.
- [Working with academic communities to build scientific understanding](https://openai.com/index/building-scientific-understanding-with-academic-communities/) — three AI-produced discoveries across math, CS and physics, released under a novel per-result external-governance experiment chosen by independent expert shepherds.
- [Cross-request KV cache exposure in the GLM-5.3 Workers AI model, and our remediation with SGLang](https://blog.cloudflare.com/kv-cache-exposure-remediation/) — a real cross-tenant data leak traced to an exact context-window/KV-pool-size mismatch combined with a disaggregated-serving bug, published as a coordinated disclosure with the engine itself.
- [Automating Feature Flag Cleanup at Scale with Multi-Agent LLM Systems: An Industrial Experience at DoorDash](https://arxiv.org/abs/2610.31351) — a real production multi-agent pipeline cleaned up 56,000 feature flags across 623 repos with a 90% engineer-approved removal rate.
- [GLM 5.3 Part 2: Prefill/Decode Context Parallelism and Hybrid HiSparse](https://vllm.ai/blog/2026-10-23-glm53-part2-pcp-dcp-hisparse) — splitting a prompt's tokens across GPUs for prefill and sharding the KV cache by token for decode is the only tested way to serve a real 1M-token request on 16 H200s.
- [LLMs are making formal software verification feasible at a much larger scale](https://www.anthropic.com/research/formal-verification) — Anthropic + Theorem have Claude prove 239 open-source libraries crash-free via machine-checked proofs, with an honest account of what "verified" does not mean.
- [Cache Engineering for Agents](https://arxiv.org/abs/2610.28577) — lets an agent directly drop or reposition pieces of its own KV cache instead of re-prefilling after every context trim.
- [Compromised LiteLLM 1.107.0 on PyPI Installs a Credential Stealer and Backdoor](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) — a real supply-chain attack on the widely-used LiteLLM gateway, targeting AI-tool and LLM-provider credentials specifically.
- [Patch the Planet: global response coordination as agents uncover critical vulnerabilities](https://openai.com/index/coordinated-disclosure-of-critical-vulnerabilities/) — what agentic vulnerability-discovery at internet scale actually requires operationally, not just technically.
- [DeepInfer](https://github.com/deepseek-ai/DeepInfer) — DeepSeek open-sources its own in-house production inference framework, confirmed official by the lab itself and today's #1 Hacker News story by a wide margin.
- [Findings from the $1M Vercel Sandbox challenge](https://vercel.com/blog/findings-from-the-1-million-dollar-vercel-sandbox-challenge) — a public bug bounty found a real production host-memory-leak zero-day in a major agent-sandbox vendor's microVM isolation.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- A disputed [r/LocalLLaMA thread](https://www.reddit.com/r/LocalLLaMA/) debunking a claim that an open-weight model uploads data to a remote URL — not independently verified this session.
- AlphaSignal's ["Backplane" PCB/CAD agent-editing tool](https://alphasignal.ai/news/backplane-lets-ai-agents-directly-edit-pcb-and-cad-hardware-designs) — surfaced but not opened in full (subscriber-gated).
- A dense HF-daily-papers world-model cluster (StreamVibe, InteractiveWorld, ChronoReplay, Hy-Nomas) is forming — watched for a 3rd-independent-group convergence.
- Reddit's direct JSON endpoints remain blocked; HN and the lab/engine blogs continue covering the earthquake-check role.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~6 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-10-28.md)) · weekly: [latest](reports/weekly/2026-W43.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
