# AI Radar

![trends](https://img.shields.io/badge/trends-22-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-23-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--10--07-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-06 daily):**

- **New evidence**: OpenAI [releases a broad batch of new math results](https://openai.com/index/sharing-ai-progress-in-mathematics/) via GitHub + Lean, governed for the first time by an independent external advisory body — reinforcing [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery).
- **Capture-leak fix**: Hugging Face's [RL Environments hub](https://huggingface.co/blog/rl-environments) (dataset-tag-based, backed day-0 by four frameworks) had sat unopened for 9 days — now [verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) evidence.
- **New facet**: Anthropic expands its [Cyber Verification Program](https://www.anthropic.com/news/cyber-verification-program) into a three-tier conditional-access system — new [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) evidence.
- **Pattern widens**: AWS/Strands ships an open-source [fast decision model](https://strandsagents.com/blog/introducing-strands-decider/), a sixth independent org on the harness-primitive pattern already tracked in [agent harness/runtime](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-10-07](https://arxiv.org/abs/2610.06833) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Trends

🌱 1 · 📈 5 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-10-07](https://arxiv.org/abs/2610.04198) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-10-02](https://arxiv.org/abs/2610.03391) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-30](https://github.com/zed-industries/zed/releases/tag/v1.22.0) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-30](https://blog.cloudflare.com/faster-agent-sandboxes/) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-30](https://arxiv.org/abs/2609.32722) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-28](https://huggingface.co/blog/rl-environments) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-21](https://blog.vllm.ai/blog/2026-09-21-qwen38-pd-serving) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-20](https://arxiv.org/abs/2609.23809) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-10-07](https://arxiv.org/abs/2610.06833) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-10-06](https://portal.nousresearch.com/bench) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-10-01](https://arxiv.org/abs/2610.01787) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-09-26](https://arxiv.org/abs/2609.32577) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 📈 emerging | [2026-09-24](https://arxiv.org/abs/2609.29861) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 seed | [2026-09-29](https://arxiv.org/abs/2609.38482) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-10-06](https://www.anthropic.com/news/cyber-verification-program) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-10-06](https://openai.com/index/sharing-ai-progress-in-mathematics/) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-10-05](https://devin.ai/blog/memory-and-dreaming) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Worth studying

- [Sharing AI progress in mathematics](https://openai.com/index/sharing-ai-progress-in-mathematics/) — OpenAI releases a broad batch of new math results (722 per third-party count) via GitHub + Lean, with release practices developed for the first time alongside an independent external advisory body.
- [openTPU](https://github.com/FeSens/openTPU) — a complete open-source AI accelerator (RTL, ISA, simulator, compiler, profiler) built largely by AI coding agents, running real quantized models bit-for-bit identically on an actual FPGA card and in simulation.
- [Memory and dreaming: how Devin learns from working with you](https://devin.ai/blog/memory-and-dreaming) — Cognition's Devin gets persistent, Git-backed memory plus a daily background "Dreaming" pass that consolidates it, shipped alongside an open "Agent Memory Repo" spec with setup docs for Claude Code and Cursor too.
- [Dust: Pretraining Transformers Without Backpropagation](https://qlabs.sh/research/dust) — the first zeroth-order method reported competitive with backprop for pretraining transformer LMs, with the counterintuitive finding that larger models are MORE population-efficient, not less.
- [The Agent Said It Was Done. The Database Disagreed.](https://huggingface.co/blog/microsoft/thinkingbox) — Microsoft + Hugging Face's ThinkingBox grades agents on the terminal backend state they leave behind, with a vivid case of an agent making 9 well-formed tool calls yet closing a ticket "resolved" when the required end state was "hold."
- [LOOM: a Scalable Recipe for Looped Mixture-of-Experts](https://arxiv.org/abs/2610.01153) — diagnoses why looped-MoE scaling stalls at ~2 loops and fixes it, reaching stable scaling to 9-12 loops with open code.
- [Disrupting a coordinated model-distillation campaign](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign) — a rare, quantified look (15,000+ users, concrete timeline) at adversarial distillation as a live operational threat, not a theoretical one.
- [Cloudflare Containers, rebuilt to scale agent sandboxes](https://blog.cloudflare.com/faster-agent-sandboxes/) — a ground-up rewrite (Durable Objects, filesystem-snapshot pause/resume, 6x faster startup) worth studying as an architecture pattern for multi-tenant agent execution infrastructure.
- [Introducing dots](https://openai.com/index/introducing-dots/) — OpenAI's always-on, persistent agent with its own cloud computer and learned-preference memory, plus a "teams of dots" roadmap.
- [Post-Training Leaves Behavioral Shadows on Unrelated Decisions](https://arxiv.org/abs/2609.29233) — Active Taskless Distillation transfers capability between models using only a single word from the teacher per prompt, on text unrelated to the transferred skill.
- [How Cloudflare addressed a cross-tenant data exposure vulnerability in Containers](https://blog.cloudflare.com/containers-cross-tenant-vulnerability/) — a clear postmortem of a shared-storage-pool bug letting one tenant recover another's residual disk data, affecting both Containers and Sandboxes.
- [NVIDIA Launches Open Agent Safety Platform](https://nvidianews.nvidia.com/news/open-agent-safety-platform) — OpenShell (an open-source runtime boundary) plus Sentry, a hardware watchdog on dedicated DPU silicon that can quarantine a rogue agent in milliseconds, entirely out-of-band from the agent's own software stack.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- Mistral's new flagship, [Mistral Large 4](https://mistral.ai/news/mistral-large-4/), topped HN (1674pts) — weights not yet shipped, promised "by the end of the month."
- An open-source AI accelerator, [openTPU](https://github.com/FeSens/openTPU), drew attention (218pts) for running real models bit-for-bit identically on actual FPGA hardware — built largely by AI coding agents.
- A reported [Anthropic chatbot-to-police escalation](https://www.techspot.com/news/114091-florida-woman-used-claude-diary-anthropic-reported-shoot.html) from last week stays unresolved — still no Anthropic primary located.
- Zvi Mowshowitz's newsletter (curator probation) stays at 0 verified-serious hits since 09-19; its promote/drop decision window closes ~W41-W42.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (23)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-10-07](reports/2026-10-07.md) · weekly: [2026-W40](reports/weekly/2026-W40.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
