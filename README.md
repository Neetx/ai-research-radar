# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-10-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-12-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--10--26-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-26):** [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) was rescued from its closest-ever approach to the 21-day dormancy line by [DoorDash's real industrial multi-agent LLM deployment](https://arxiv.org/abs/2610.31351) · [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) (pinned) gained a 14th independent cluster, [J-Comm's Jacobian-lens interface](https://arxiv.org/abs/2610.32871) · a dense vLLM-blog catch added fresh evidence to [prefill/decode disaggregation](https://vllm.ai/blog/2026-10-23-deepseek-v41-flash-pd-wide-ep), [subquadratic/sparse attention](https://vllm.ai/blog/2026-10-23-glm53-part2-pcp-dcp-hisparse), and resolved [MiniMax-M3.1-Flash's shipped-weights watch](https://vllm.ai/blog/2026-10-23-minimax-m31-flash) on the [open-weight wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) · a 1-release GitHub-watch coverage gap closed with [llama.cpp v0.7.0](https://github.com/ggml-org/llama.cpp/releases/tag/v0.7.0) on [ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) (pinned).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-23](https://arxiv.org/abs/2610.32871) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-21](https://alphasignal.ai/news/recursive-si-s-flint-runs-a-40b-coding-model-on-your-laptop) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-18](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-21](https://arxiv.org/abs/2610.27628) |

## Trends

🌱 8 · 📈 10 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-10-23](https://vllm.ai/blog/2026-10-23-deepseek-v41-flash-pd-wide-ep) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-10-23](https://vllm.ai/blog/2026-10-23-glm53-part2-pcp-dcp-hisparse) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-22](https://arxiv.org/abs/2610.31351) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-22](https://huggingface.co/blog/microsoft/thinkingbox-training) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-22](https://arxiv.org/abs/2610.31563) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-21](https://blog.cloudflare.com/webmcp-commerce/) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-21](https://alphasignal.ai/news/recursive-si-s-flint-runs-a-40b-coding-model-on-your-laptop) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-10-21](https://arxiv.org/abs/2610.26855) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-18](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-10-14](https://vercel.com/blog/findings-from-the-1-million-dollar-vercel-sandbox-challenge) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-23](https://arxiv.org/abs/2610.32871) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-10-22](https://arxiv.org/abs/2610.31544) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-21](https://arxiv.org/abs/2610.27628) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-10-19](https://github.com/humanlayer/advanced-context-engineering-for-coding-agents/blob/main/benchmarking-new-models-on-slop-code-bench.md) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22070) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22322) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-10-14](https://www.chainalysis.com/blog/north-america-crypto-adoption-2026) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-10-13](https://arxiv.org/abs/2610.17593) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-10-22](https://arxiv.org/abs/2610.28577) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-10-22](https://www.anthropic.com/research/formal-verification) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-10-21](https://safedep.io/litellm-pypi-compromise-credential-stealer-backdoor/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-19](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-10-23](https://vllm.ai/blog/2026-10-23-minimax-m31-flash) |

## Worth studying

- [Automating Feature Flag Cleanup at Scale with Multi-Agent LLM Systems: An Industrial Experience at DoorDash](https://arxiv.org/abs/2610.31351) — a real production multi-agent pipeline cleaned up 56,000 feature flags across 623 repos with a 90% engineer-approved removal rate.
- [GLM 5.3 Part 2: Prefill/Decode Context Parallelism and Hybrid HiSparse](https://vllm.ai/blog/2026-10-23-glm53-part2-pcp-dcp-hisparse) — splitting a prompt's tokens across GPUs for prefill and sharding the KV cache by token for decode is the only tested way to serve a real 1M-token request on 16 H200s.
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

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- "Context engineering" keeps relabeling itself — [a practitioner's account](https://www.dbreunig.com/2026/10/24/the-state-of-context-engineering.html) traces prompt engineering → context engineering → "harness engineering," naming this radar's own agent-runtime axis directly.
- A thin HF-daily-papers day surfaced a handful of agent-eval/embodied/agent-evolution candidates — [UserArena](https://arxiv.org/abs/2610.30932), [HiSTEVE 1.0](https://arxiv.org/abs/2610.31162), [RSIHub](https://arxiv.org/abs/2610.32253) — none yet crossing any trend's bar.
- NVIDIA's own account of [serving a 753B model across 8 linked DGX Spark nodes](https://developer.nvidia.com/blog/running-frontier-class-ai-models-across-8-nvidia-dgx-spark-nodes/) — multi-node tensor parallelism, not disaggregated serving.
- A candidate 14th cluster on cross-model latent communication, [CacheBack](https://arxiv.org/abs/2609.32046), prunes up to 94% of redundant multi-agent KV-cache via a receiver-conditioned attention mask.
- Reddit's direct JSON endpoints remain blocked; the YouTube curator Atom feed is re-confirmed re-blocked; HN and the lab/engine blogs continue covering the earthquake-check role.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~12 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-10-26.md)) · weekly: [latest](reports/weekly/2026-W43.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
