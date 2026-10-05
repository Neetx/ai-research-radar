# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-20-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--10--05-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-10-02 daily / 2026-10-03 weekly):**

- **Dormancy rescue**: [LOOM](https://arxiv.org/abs/2610.01153) fixes the specific mechanism (variance compounding + expert-selection collapse) capping prior looped-MoE work at ~2 loops, rescuing [latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) from crossing the 21-day dormancy line today.
- **A 5th org on the decision-model pattern**: OpenAI's [Decisions API](https://openai.com/index/devday-2026-recap/) resolves a 4-run-standing queue item into [agent harness/runtime](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) evidence — the first frontier lab itself (not just infra vendors/startups) to ship this primitive.
- **A new realism dimension**: Microsoft + Hugging Face's [ThinkingBox](https://huggingface.co/blog/microsoft/thinkingbox) grades agents on the terminal backend state they leave behind, not their tool calls or final response — new evidence on [deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards).
- **Queue refreshed**: 7 stale below-bar items dropped, 8 new ones added (small/CPU-model compression batch + a KV-cache paper), net flat at 20 live.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-10-01](https://arxiv.org/abs/2610.01153) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Trends

🌱 1 · 📈 4 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-10-04](https://github.com/Niko1221/Strata) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-30](https://blog.cloudflare.com/faster-agent-sandboxes/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-30](https://github.com/zed-industries/zed/releases/tag/v1.22.0) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-30](https://arxiv.org/abs/2609.32722) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.33772) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.34981) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-21](https://blog.vllm.ai/blog/2026-09-21-qwen38-pd-serving) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-20](https://arxiv.org/abs/2609.23809) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-17](https://arxiv.org/abs/2609.20751) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-10-03](https://huggingface.co/blog/microsoft/thinkingbox) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-10-01](https://arxiv.org/abs/2610.01153) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-09-26](https://arxiv.org/abs/2609.32577) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-09-16](https://arxiv.org/abs/2609.18842) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-10-01](https://earendil.com/posts/pi-1-0/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-30](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-28](https://z.ai/blog/glm-built-its-inference-infrastructure) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-09-15](https://arxiv.org/abs/2609.16610) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Worth studying

- [The Agent Said It Was Done. The Database Disagreed.](https://huggingface.co/blog/microsoft/thinkingbox) — Microsoft + Hugging Face's ThinkingBox grades agents on the terminal backend state they leave behind, with a vivid case of an agent making 9 well-formed tool calls yet closing a ticket "resolved" when the required end state was "hold."
- [LOOM: a Scalable Recipe for Looped Mixture-of-Experts](https://arxiv.org/abs/2610.01153) — diagnoses why looped-MoE scaling stalls at ~2 loops and fixes it, reaching stable scaling to 9-12 loops with open code.
- [Pi 1.0](https://earendil.com/posts/pi-1-0/) — a hardened, minimal, MIT-licensed agent harness (already independently benchmarked to the Pareto frontier in HarnessTax) ships its own 1.0 release — by far the day's highest-attention item (HN #1, 996pts).
- [Context Language Models](https://arxiv.org/abs/2609.37725) — Ai2/UW researchers show a model that treats its own context as a rewritable file, beating SOTA harness-external context management, with a natural extension to multi-agent systems.
- [Disrupting a coordinated model-distillation campaign](https://openai.com/index/disrupting-a-coordinated-model-distillation-campaign) — a rare, quantified look (15,000+ users, concrete timeline) at adversarial distillation as a live operational threat, not a theoretical one.
- [Cloudflare Containers, rebuilt to scale agent sandboxes](https://blog.cloudflare.com/faster-agent-sandboxes/) — a ground-up rewrite (Durable Objects, filesystem-snapshot pause/resume, 6x faster startup) worth studying as an architecture pattern for multi-tenant agent execution infrastructure.
- [Introducing dots](https://openai.com/index/introducing-dots/) — OpenAI's always-on, persistent agent with its own cloud computer and learned-preference memory, plus a "teams of dots" roadmap.
- [Post-Training Leaves Behavioral Shadows on Unrelated Decisions](https://arxiv.org/abs/2609.29233) — Active Taskless Distillation transfers capability between models using only a single word from the teacher per prompt, on text unrelated to the transferred skill.
- [How Cloudflare addressed a cross-tenant data exposure vulnerability in Containers](https://blog.cloudflare.com/containers-cross-tenant-vulnerability/) — a clear postmortem of a shared-storage-pool bug letting one tenant recover another's residual disk data, affecting both Containers and Sandboxes.
- [NVIDIA Launches Open Agent Safety Platform](https://nvidianews.nvidia.com/news/open-agent-safety-platform) — OpenShell (an open-source runtime boundary) plus Sentry, a hardware watchdog on dedicated DPU silicon that can quarantine a rogue agent in milliseconds, entirely out-of-band from the agent's own software stack.
- [2026 in LLMs (so far)](https://simonwillison.net/2026/Sep/27/2026-in-llms-so-far/) — Simon Willison's annotated year-in-review keynote, a single practitioner-grounded recap of the whole year.
- [Introducing Contrastive Language Models (CLM)](https://huggingface.co/Contrastive-LM/CLM-v0.1-8B) — Stanford's Scaling Intelligence Lab ships an 8B "System One" model that scores agent actions via cheap contrastive vector search, matching the incumbent Jev's quality at up to 9x lower latency.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- Small/CPU consumer-hardware compression is having a moment: a [turnkey 125B-on-a-gaming-PC installer](https://github.com/Niko1221/Strata) hit #1 on HN (690pts) the same week AlphaSignal's feed carried six more independent compression releases in a single pull.
- A major telecom (China Telecom) shipped its own [29B local coding-agent model](https://huggingface.co/XingChen-AGI/Xing4.0-29B-A4B) — a notably different publisher type entering the small/CPU axis.
- Two standing rumors stay unconfirmed by any primary: a reported "GPT-6.1 Astra" pullback for alignment concerns (3rd miss, a 2nd secondary source found but still no lab primary) — OpenAI's "Decisions API" rumor resolved to a confirmed primary this run.
- Zvi Mowshowitz's newsletter (curator probation) stays at 0 verified-serious hits since 09-19 — decision window (promote or drop) closes ~W41-W42.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (20)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-10-05](reports/2026-10-05.md) · weekly: [2026-W40](reports/weekly/2026-W40.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
