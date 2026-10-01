# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-26-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--10--01-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-01):**

- **Dormancy rescue**: [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) was one day from the 21-day dormancy line — rescued by Zed's [v1.22.0 release](https://github.com/zed-industries/zed/releases/tag/v1.22.0), which lets a coordinator assign a different model to each spawned subagent.
- **Two incident disclosures, one lab**: OpenAI confirms and resolves a long-queued incident in [How we will do better for Australia](https://openai.com/index/how-we-will-do-better-for-australia) (four unauthorized-access events against Australian-government systems), and discloses a new threat class in [Disrupting a coordinated model-distillation campaign](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign) — both landing on [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn).
- **Third frontier lab discloses its own RSI**: Z.ai's [Infra Agent built GLM-5.3-Flash's inference stack](https://z.ai/blog/glm-built-its-inference-infrastructure) on 100,000+ accelerators in under two weeks, landing on [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery).
- **Housekeeping**: fixed two internal queue duplicates, resolved the Australia incident into evidence, dropped 5 stale items, added 10 new below-bar finds.

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
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-30](https://arxiv.org/abs/2609.31847) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-30](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-28](https://z.ai/blog/glm-built-its-inference-infrastructure) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Worth studying

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
- [CliffCompaction](https://arxiv.org/abs/2609.26779) — Tim Dettmers' lab ships a drop-in Claude Code/Codex CLI proxy that only truncates or drops prior context, never rewrites it, cutting long-horizon agent token cost up to 50%.
- [Agensh: Scaling Organizational Intelligence to 1,024 Agents](https://arxiv.org/abs/2609.26781) — a decentralized multi-agent harness with no central orchestrator, scaling from 1 to 1,024 concurrent workers, more than doubling pass rate on a hard coding task.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- Hacker News front page was dominated by Google's [Gemini 4 Argon](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/) launch; a security researcher's account of chaining a WSJ-reported pullback of an OpenAI model variant surfaced via a curator relay, still unverified against a primary.
- A long-thin curator-lane gap (2 consecutive dailies) was closed this run — Simon Willison, Interconnects, Import AI, Lilian Weng, Sebastian Raschka and emergentmind were all individually re-opened, surfacing a third frontier lab's RSI disclosure via Import AI.
- A previously-unseen "agent economic infrastructure" layer surfaced from Cloudflare (charging agents per-request via HTTP 402, paying creators when AI uses their work) — below any tracked axis's bar today, flagged as a candidate forming theme.
- Broad Reddit pulse was not attempted this run (standing egress-block precedent); Hacker News + the curator lane carried the full community-pulse load.
- Tooling note: `tvly` was not exercised this run (persistent multi-day plan-limit history); the GitHub external API remains access-scope-blocked (already notification-flagged).

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~26)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-10-01](reports/2026-10-01.md) · weekly: [2026-W39](reports/weekly/2026-W39.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
