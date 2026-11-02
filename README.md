# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-10-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-6-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--02-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-31):** [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) added the [Ruby SDK's Tier-1 promotion](https://blog.modelcontextprotocol.io/posts/ruby-sdk-tier-1/), closing a ~5-week coverage gap · [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) added Parameter.ai's [ChatGPT account-takeover disclosure](https://www.parameter.ai/labs/we-found-a-gap-at-openai), a chained XSS/sandbox-escape fixed by OpenAI · [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) was rescued from the 21-day dormancy line by [ACE-Brain-0.6](https://arxiv.org/abs/2610.27040) · Microsoft Research's own [ForkPilot](https://arxiv.org/abs/2610.04889) and [TeleTune](https://www.microsoft.com/en-us/research/publication/teletune-evolving-agent-skills-from-offline-telemetry/) landed as evidence on [dense credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) and [agent harness/runtime](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) respectively.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-30](https://arxiv.org/abs/2610.41822) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-30](https://arxiv.org/abs/2610.42030) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-30](https://arxiv.org/abs/2610.41751) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-27](https://www.liquid.ai/blog/lfm3) |

## Trends

🌱 8 · 📈 10 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-10-30](https://arxiv.org/abs/2610.41822) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-29](https://cursor.com/blog/agent-sdk) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-10-29](https://vllm.ai/blog/2026-10-29-mistral-large-4) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-10-27](https://www.liquid.ai/blog/lfm3) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-10-27](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-10-26](https://blog.cloudflare.com/kv-cache-exposure-remediation/) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-22](https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-22](https://huggingface.co/blog/microsoft/thinkingbox-training) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-22](https://arxiv.org/abs/2610.31563) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-10-15](https://www.perplexity.ai/hub/blog/open-sourcing-space) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-10-30](https://huggingface.co/blog/ibm-granite/granite-switch-4-1-1) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-10-30](https://arxiv.org/abs/2610.42030) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-10-30](https://arxiv.org/abs/2610.41751) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-10-29](https://arxiv.org/abs/2610.35013) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-10-27](https://surgehq.ai/blog/dayjob-tax) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-10-19](https://arxiv.org/abs/2610.27040) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 emerging | [2026-10-15](https://arxiv.org/abs/2610.22322) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-10-14](https://www.chainalysis.com/blog/north-america-crypto-adoption-2026) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-10-29](https://mistral.ai/news/mistral-large-4-oss/) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-10-29](https://openai.com/index/how-we-detect-frontier-model-misalignment) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-10-29](https://arxiv.org/abs/2610.36077) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-10-27](https://www.anthropic.com/research/early-progress-drug-development) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-19](https://github.com/sgl-project/sglang/releases/tag/v0.5.22) |

## Worth studying

- [Do the math: How we took over ChatGPT accounts](https://www.parameter.ai/labs/we-found-a-gap-at-openai) — a chained XSS/sandbox-escape (a math-rendering widget's own `postMessage` listener → an unsandboxed iframe → a CSP bypass via YouTube's oEmbed endpoint) that turned a sandboxed UI feature into a full account takeover on mere click.
- [ForkPilot](https://arxiv.org/abs/2610.04889) — a rigorously-benchmarked answer to when a long-horizon agent should backtrack a decision, tested against a production harness with hundreds of thousands of paid users.
- [How we detect frontier model misalignment](https://openai.com/index/how-we-detect-frontier-model-misalignment) — OpenAI's full disclosed monitoring stack (activation probes → CoT-reading reviewer → human investigators → automated telemetry cross-check), red-teamed by METR/Redwood Research for three weeks.
- [We're releasing the weights of Mistral Large 4](https://mistral.ai/news/mistral-large-4-oss/) — the first Western lab to ship a frontier-scale open-weight model combining Multi-head Latent Attention with a DeepSeek-Sparse-Attention-style indexer at ~1T total/~50B active parameters.
- [Qwenputer](https://divagr.com/blog/qwenputer) — a deterministic RISC-V CPU compiled directly into Qwen 3.5 4B's weights with no training, by exploiting its linear-attention state as addressable RAM.
- [Gemini 4 Carbon: Our next frontier model](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-carbon/) — a frontier lab publishing a quantified before/after number (prompt-injection success 0.7%→0.0%) for an architectural safety mechanism rather than a qualitative claim.
- [Genie 4: A new generation of world simulation](https://deepmind.google/blog/genie-4-a-new-generation-of-world-simulation/) — DeepMind's newest world model generates audio, dialogue and visuals simultaneously and lets you steer the evolving simulation in real time via natural language.
- [Early progress on accelerating drug development with Claude](https://www.anthropic.com/research/early-progress-drug-development) — a frontier lab's own candid account of where an LLM actually helps (and doesn't yet) across the full drug-development pipeline, from six simultaneous external biotech/pharma partnerships.
- [Working with academic communities to build scientific understanding](https://openai.com/index/building-scientific-understanding-with-academic-communities/) — three AI-produced discoveries across math, CS and physics, released under a novel per-result external-governance experiment chosen by independent expert shepherds.
- [Cross-request KV cache exposure in the GLM-5.3 Workers AI model, and our remediation with SGLang](https://blog.cloudflare.com/kv-cache-exposure-remediation/) — a real cross-tenant data leak traced to an exact context-window/KV-pool-size mismatch combined with a disaggregated-serving bug, published as a coordinated disclosure with the engine itself.
- [Automating Feature Flag Cleanup at Scale with Multi-Agent LLM Systems: An Industrial Experience at DoorDash](https://arxiv.org/abs/2610.31351) — a real production multi-agent pipeline cleaned up 56,000 feature flags across 623 repos with a 90% engineer-approved removal rate.
- [GLM 5.3 Part 2: Prefill/Decode Context Parallelism and Hybrid HiSparse](https://vllm.ai/blog/2026-10-23-glm53-part2-pcp-dcp-hisparse) — splitting a prompt's tokens across GPUs for prefill and sharding the KV cache by token for decode is the only tested way to serve a real 1M-token request on 16 H200s.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- Moonshot's [Kimi K3.1 Pro](https://www.kimi.com/blog/kimi-k3-1-pro) is API-only for now, with open weights promised "by Nov 4" — a watch item, not yet shipped.
- Yann LeCun and Randall Balestriero's [Platonic Representation Theorem](https://arxiv.org/abs/2610.39302) — a proof that JEPAs trained on different modalities converge to the same representation up to rotation — is drawing attention on both Hacker News and alphaXiv.
- NVIDIA's [NemoClaw blueprint](https://developer.nvidia.com/blog/build-specialized-agents-on-a-stack-you-control-with-nvidia-nemoclaw/) names a third-party open-source harness, "OpenClaw," not yet independently verified or sourced.
- A secondary crypto-industry report argues real x402 agent-payment client adoption is smaller than headline transaction counts suggest — the primary analysis wasn't located this session.
- Ubicloud's [vLLM tool-call-accuracy fix](https://www.ubicloud.com/blog/fixing-tool-call-accuracy-in-vllm) (a config change, not a new mechanism) raised schema accuracy from 92% to 100% for Kimi/DeepSeek deployments.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~6 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-02.md)) · weekly: [latest](reports/weekly/2026-W44.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
