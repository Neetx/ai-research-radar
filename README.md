# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-25-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--10--03-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-03, weekly recalibration):**

- **Monthly retrospective catches a real miss**: Convai Innovations' [Laya](https://huggingface.co/convaiinnovations/laya) — a fast "System 1" decision model with 5,000+ HF likes — sat uncaught for 2+ weeks before this run backfilled it onto [agent harness/runtime infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) as a 4th independent org on the decision-model-as-harness-primitive pattern.
- **Three standing mainstreaming gates held again**: small-cpu-models-008's extreme-low-bit-as-default, multi-agent-eng-009's cross-vendor-portable-abstraction, and world-action-models-020's adoption-side gate all stay unfired this week — no stage moves.
- **Queue reconciled**: a direct recount found 24 live watchlist items pre-session (vs. a daily-delta projection of 28) — a 4-item gap now named and a [tightened recount step](reports/weekly/2026-W40.md) proposed for next week.
- **Capture-leak sweep clean**: 20 ids cross-checked this week, 0 genuine leaks (2 apparent misses resolved as legitimately-dropped queue items).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-29](https://github.com/firelex/jeff) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-14](https://arxiv.org/abs/2609.15160) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Trends

🌱 1 · 📈 4 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-30](https://blog.cloudflare.com/faster-agent-sandboxes/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-30](https://github.com/zed-industries/zed/releases/tag/v1.22.0) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-30](https://arxiv.org/abs/2609.32722) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-29](https://github.com/firelex/jeff) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.33772) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.34981) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-21](https://blog.vllm.ai/blog/2026-09-21-qwen38-pd-serving) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-20](https://arxiv.org/abs/2609.23809) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-17](https://arxiv.org/abs/2609.20751) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-09-26](https://arxiv.org/abs/2609.32577) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-23](https://arxiv.org/abs/2609.26777) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-09-16](https://arxiv.org/abs/2609.18842) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-14](https://arxiv.org/abs/2609.15160) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-09-15](https://arxiv.org/abs/2609.16610) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-10-01](https://earendil.com/posts/pi-1-0/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-30](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-28](https://z.ai/blog/glm-built-its-inference-infrastructure) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Worth studying

- [Pi 1.0](https://earendil.com/posts/pi-1-0/) — a hardened, minimal, MIT-licensed agent harness (already independently benchmarked to the Pareto frontier in HarnessTax) ships its own 1.0 release — by far the day's highest-attention item (HN #1, 996pts).
- [Context Language Models](https://arxiv.org/abs/2609.37725) — Ai2/UW researchers show a model that treats its own context as a rewritable file, beating SOTA harness-external context management, with a natural extension to multi-agent systems.
- [Disrupting a coordinated model-distillation campaign](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign) — a rare, quantified look (15,000+ users, concrete timeline) at adversarial distillation as a live operational threat, not a theoretical one.
- [Cloudflare Containers, rebuilt to scale agent sandboxes](https://blog.cloudflare.com/faster-agent-sandboxes/) — a ground-up rewrite (Durable Objects, filesystem-snapshot pause/resume, 6x faster startup) worth studying as an architecture pattern for multi-tenant agent execution infrastructure.
- [Introducing dots](https://openai.com/index/introducing-dots/) — OpenAI's always-on, persistent agent with its own cloud computer and learned-preference memory, plus a "teams of dots" roadmap.
- [Post-Training Leaves Behavioral Shadows on Unrelated Decisions](https://arxiv.org/abs/2609.29233) — Active Taskless Distillation transfers capability between models using only a single word from the teacher per prompt, on text unrelated to the transferred skill.
- [How Cloudflare addressed a cross-tenant data exposure vulnerability in Containers](https://blog.cloudflare.com/containers-cross-tenant-vulnerability/) — a clear postmortem of a shared-storage-pool bug letting one tenant recover another's residual disk data, affecting both Containers and Sandboxes.
- [NVIDIA Launches Open Agent Safety Platform](https://nvidianews.nvidia.com/news/open-agent-safety-platform) — OpenShell (an open-source runtime boundary) plus Sentry, a hardware watchdog on dedicated DPU silicon that can quarantine a rogue agent in milliseconds, entirely out-of-band from the agent's own software stack.
- [Holo4](https://huggingface.co/blog/Hcompany/holo4) — an open-weight generalist computer-use agent that clicks/types on a screen, writes and runs code, and calls MCP/API tools through one model across desktop, web, Android and code-sandbox targets.
- [2026 in LLMs (so far)](https://simonwillison.net/2026/Sep/27/2026-in-llms-so-far/) — Simon Willison's annotated year-in-review keynote, a single practitioner-grounded recap of the whole year.
- [Introducing Contrastive Language Models (CLM)](https://huggingface.co/Contrastive-LM/CLM-v0.1-8B) — Stanford's Scaling Intelligence Lab ships an 8B "System One" model that scores agent actions via cheap contrastive vector search, matching the incumbent Jev's quality at up to 9x lower latency.
- [Codetta: High-Capacity, Keyless, and Undetectable Multi-Agent Collusion](https://arxiv.org/abs/2609.28900) — CMU researchers build a provably-undetectable steganographic protocol for independently-deployed agents to covertly collude, no pre-shared secret required.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- This week's curator lane ran a full sweep only 1 of 5 days; this weekly's own spot-recheck of the 4 most-productive thin-logged curators (Interconnects, Import AI, Lilian Weng, Sebastian Raschka) found all four genuinely quiet — 0 primaries actually lost, but the logging-discipline gap is named for the dailies to fix.
- Zvi Mowshowitz's newsletter (curator probation) stays at 0 verified-serious hits since 09-19 — decision window (promote or drop) closes ~W41-W42.
- Two standing rumors stay unconfirmed by any primary as of 10-02: OpenAI's "Decisions API" (3rd miss) and a reported "GPT-6.1 Astra" pullback for alignment concerns (2nd miss).
- Tooling note: `tvly` reinstalled and worked throughout this weekly's source-strategy checks; direct GitHub API access stays scope-blocked for repos outside this session (WebFetch of public release pages is the working fallback).

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (25)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-10-02](reports/2026-10-02.md) · weekly: [2026-W40](reports/weekly/2026-W40.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
