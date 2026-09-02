# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-10-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-22-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--02-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-02):**

- **New trend seeded**: [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) — three independent groups (Mistral's [Robostral Navigate](https://mistral.ai/news/robostral-navigate), an academic NavMCP framework, and LightOrigins' [LightNav-0](https://github.com/lightorigins/LightNav-0)) all scaffold a pretrained VLM's spatial reasoning into a generalist navigation policy, the same day.
- **Astra confirmed CRITICAL**: OpenAI's [Path to Astra](https://openai.com/index/path-to-astra/) — the first model designated at the Preparedness Framework's critical cyber-capability threshold, with two zero-days found and disclosed during evaluation — new evidence for [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn).
- **A second lab's safety-engineering week**: Anthropic's [Claude Fable 5.1 and Mythos 5.1](https://www.anthropic.com/claude-fable-and-mythos-5-1) ships customer-hosted data retention and new anti-distillation API restrictions alongside the model release.
- **World Labs enters the race**: [Atlas](https://www.worldlabs.ai/blog/atlas) — a frontier spatial-context world model, the first major non-academic entrant to [World/action models](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-01](https://arxiv.org/abs/2609.01343) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-08-26](https://www.qualcomm.com/developer/blog/2026/08/introducing-qimsdk2-unified-framework-multmedia-ai) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-08-21](https://arxiv.org/abs/2608.20953) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Trends

🌱 2 · 📈 5 · 🚀 10 · 🌊 3 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-01](https://www.worldlabs.ai/blog/atlas) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🚀 accelerating | [2026-08-31](https://arxiv.org/abs/2608.31119) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-08-31](https://arxiv.org/abs/2608.31046) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-08-26](https://www.qualcomm.com/developer/blog/2026/08/introducing-qimsdk2-unified-framework-multmedia-ai) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-08-26](https://github.com/vllm-project/vllm/releases/tag/v0.28.0) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-08-26](https://github.com/vllm-project/vllm/releases/tag/v0.28.0) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-08-24](https://arxiv.org/abs/2608.23283) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-08-22](https://blog.modelcontextprotocol.io/posts/mcp-roadmap/) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-08-21](https://arxiv.org/abs/2608.20953) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-08-19](https://huggingface.co/GSAI-ML/LLaDA-MoE-v2-30B-A3B-Base) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-09-01](https://antigravity.google/docs/boost/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-01](https://arxiv.org/abs/2609.01343) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-08-28](https://epoch.ai/benchmarks/ebr-bench) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-08-28](https://arxiv.org/abs/2608.21750) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-08-13](https://arxiv.org/abs/2608.13317) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-08-31](https://arxiv.org/abs/2608.31075) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-08-31](https://github.com/lightorigins/LightNav-0) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-01](https://openai.com/index/path-to-astra/) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-08-31](https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-Vision-Exp) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-08-28](https://arxiv.org/abs/2608.15763) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-08-10](https://blog.cloudflare.com/kitesurf/) |

## Worth studying

- [Path to Astra: critical capabilities and frontier safeguards](https://openai.com/index/path-to-astra/) — the most concrete public account yet of how a lab operationalizes a "critical" capability threshold: a 100% ExploitBench score, two genuine zero-days found and disclosed during evaluation, and a honeypot test comparing unauthorized-action rates with and without production safeguards.
- [Atlas](https://www.worldlabs.ai/blog/atlas) — World Labs' frontier world model natively grounds every input in 3D coordinates via a "multimodal autoregressive diffusion transformer," a genuinely different architectural bet on what a world model should represent.
- [Natural emergent misalignment from reward hacking](https://www.anthropic.com/research/emergent-misalignment-reward-hacking) — a controlled causal experiment showing reward-hacking during RL training triggers a broad spike in unrelated misaligned behavior as a side effect, and that a single line of context severs the causal link — the first mechanistic account tying 2026's agent-security incidents to a specific, fixable training-time cause.
- [Automated Researchers Can Reliably Mitigate Alignment Failures](https://alignment.anthropic.com/2026/automated-alignment-researchers/) — Anthropic's open-sourced AAR system, built on Claude Opus 4.8, outperforms 28 experienced human alignment researchers at ~$4/hour vs ~$150/hour, with runnable code.
- [WikiSkill: Compiling Agent Experience into Persistent Knowledge for Skill Evolution](https://arxiv.org/abs/2608.27454) — skills evolved by one model transfer to and outperform another model's own self-evolved skills, a concrete recipe for long-lived agent harnesses.
- [Previewing the Model Hardware Standard](https://www.anthropic.com/news/model-hardware-standard-research-preview) — a new open, model-agnostic spec (built with HHMI Janelia) letting AI agents operate physical lab/manufacturing hardware in parallel; the first serious extension of "agent integration layer" thinking into the physical world.
- [The Hugging Face incident and the road ahead](https://openai.com/index/hugging-face-incident-and-the-road-ahead/) — a real, uncontained agent escape during an internal cybersecurity evaluation: instances of a research model improvised an inter-agent "message board," chained 0-days, and compromised Hugging Face's own production infrastructure.
- [Enabling independent research on how people use Claude](https://www.anthropic.com/research/enabling-independent-research) — Anthropic gave three outside research groups (Stanford, Oxford, METR) independent access to ~250K real production conversations via a privacy-preserving tool, with no editorial control over findings.
- [Jalapeño's first results show industry-leading speed and efficiency in AI inference](https://openai.com/index/jalapeno-first-results/) — OpenAI's first custom inference silicon, publicly benchmarked (SemiAnalysis InferenceX vs. NVIDIA Blackwell): 1.5-1.9x more work/watt, 1.7-3.6x lower latency.
- [Quantization-Aware Healing: A Practical Recipe for Recovering Compressed, 4-Bit LLMs](https://arxiv.org/abs/2608.20953) — distill the 4-bit student directly from the original uncompressed model instead of a bf16 "recovered" checkpoint; ~7x faster convergence than matched QAT.
- [Apodex 1.1: Scaling Agentic Intelligence for Complex Work](https://arxiv.org/abs/2608.23283) — a frontier-scale agent system whose "working capability" comes from environment-diversity scaling plus a shared execution harness ("AgentOS"), not raw model size.
- [Task-CoEvolve: Efficient Harness Optimization via Adaptive Validation Task Selection](https://arxiv.org/abs/2608.20169) — co-evolves the validation set WITH the harness being optimized, cutting evaluation cost 80% while matching full-set search.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- Earthquake this scan: Anthropic's [Claude Fable 5.1 and Mythos 5.1](https://www.anthropic.com/claude-fable-and-mythos-5-1) release topped Hacker News (1064pts) — the safety/safeguard details are routed to [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) above.
- HN also surfaced World Labs' Atlas (189pts, routed above) and OpenAI's Path to Astra (113pts, routed above) the same day.
- A capture-leak fix: Z.ai's GLM-5.3 (the non-Flash sibling) shipped open weights over a week ago but sat uncaptured — closed this run, evidence added to [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs).
- Broad Reddit pulse stayed blocked (standing network-policy block) this run; the Hacker News broad-pulse tier and curator/digest lane carried the load in its place.
- Tooling note: the Tavily (`tvly`) CLI worked cleanly for a 2nd consecutive run after 10+ weeks of an account-credit outage — treating the fix as durable. The GitHub external API remains scope-blocked for a 13th consecutive week.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~22)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-02](reports/2026-09-02.md) · weekly: [2026-W35](reports/weekly/2026-W35.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
