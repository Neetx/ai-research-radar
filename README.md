# AI Radar

![trends](https://img.shields.io/badge/trends-18-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-3-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-25-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--07--25-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-07-25):**

- **2 overdue dormancy marks caught this weekly** — [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) (🚀→💤) and pinned [Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) (📈→💤), both `last_evidence` [2026-07-01](https://arxiv.org/abs/2607.01308) = 24d; the dailies missed the 21-day crossing (enumeration gap → proposal W30-P2).
- **Amendment W29-P1 applied** ([routines/weekly.md](routines/weekly.md)): a dormant trend's named reactivation source is now swept every weekly — the [MCP blog](https://blog.modelcontextprotocol.io/) was swept, 07-28 final spec still 3 days out, [MCP](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) held.
- **Study shelf** pruned 44 → 27 live (≤06-30 tail archived, nothing lost — [study_shelf](TRENDS.md#study_shelf)); capture-leak sweep **27 ids / 0 leaks**.
- **3rd consecutive anchoring warning** — all week's evidence landed on pre-existing trends, zero new trends ([strategy_notes](TRENDS.md#strategy_notes)).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 5 · 📈 3 · 🚀 3 · 🌊 1 · 🏔 0 · 📉 0 · 💤 6

| trend | stage | latest signal |
|---|---|---|
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-16](https://www.kimi.com/blog/kimi-k3) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-07-07](https://arxiv.org/abs/2607.05722) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-29](https://blog.modelcontextprotocol.io/posts/sdk-betas-2026-07-28/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-07-22](https://huggingface.co/blog/security-incident-july-2026) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-07-23](https://arxiv.org/abs/2607.20911) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-07-20](https://arxiv.org/abs/2607.18110) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🌱 seed | [2026-07-16](https://arxiv.org/abs/2607.14777) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌱 seed | [2026-07-14](https://arxiv.org/abs/2607.13285) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-07-22](https://huggingface.co/upstage/Solar-Open2-250B) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.00466) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 💤 dormant | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 💤 dormant | [2026-06-22](https://sakana.ai/fugu-release/) |

## Worth studying

- [Solar-Open2-250B (Upstage)](https://huggingface.co/upstage/Solar-Open2-250B) — a new open-weights frontier-ish MoE (320 experts / 8 active, 1M ctx) from a lab not previously in the open-weight set.
- [Scaling Laws for Hypernetwork-Based Knowledge Injection](https://arxiv.org/abs/2607.19604) — can you reliably compile factual knowledge INTO weights at scale, and how does it scale? The reference for the parametric-injection-vs-RAG question.
- [SLPO: outcome-reward RL for latent reasoners](https://arxiv.org/abs/2607.19691) — a surrogate policy density over latent transitions + a learned stopping head lets outcome-reward RL finally grip latent reasoning.
- [GigaToken: a ~1000× faster LLM tokenizer in Rust](https://github.com/marcelroed/gigatoken) — a systems artifact for anyone whose data-prep/serving pipeline is tokenization-bound (solo project, self-benchmarked).
- [The HF security incident](https://huggingface.co/blog/security-incident-july-2026) — the canonical threat-model writeup: the first real-world autonomous-AI-agent intrusion of a major platform, entered via a malicious dataset.
- [LLM-as-a-Coach: experiential learning for non-verifiable tasks](https://arxiv.org/abs/2607.18110) — how to do RL when you can't write a verifier: repurpose the judge into a coach emitting transferable experiential knowledge.
- [Loopie: the strongest looped-Transformer MoE to date](https://arxiv.org/abs/2607.16051) — the existence proof that recurrent-depth computation beats a same-compute vanilla MoE (no public weights yet).
- [MCP goes stateless: the 2026-07-28 spec + SDK betas + EMA](https://blog.modelcontextprotocol.io/posts/sdk-betas-2026-07-28/) — the clearest map of what "MCP as production infrastructure" requires on the wire.
- [Kimi K3: the first open 3T-class model](https://www.kimi.com/blog/kimi-k3) — KDA linear/delta attention + Attention Residuals + Stable LatentMoE at record scale (architecture claims announcement-level; weights due 07-27).
- [Inkling: a ~1T-param multimodal open model with relative attention](https://huggingface.co/thinkingmachines/Inkling) — drops RoPE for a learned relative attention + interleaved local/global attention; runnable (119 safetensors + NVFP4 sibling).
- [Bonsai 27B: the first 27B-class model to run on a phone](https://prismml.com/news/bonsai-27b) — a Qwen3.6-27B multimodal model shipped low-bit end-to-end (1-bit 3.9 GB fits an iPhone; downloadable GGUFs).
- [Direct-OPD: weak-to-strong via direct on-policy distillation](https://arxiv.org/abs/2607.05394) — run RL on a small cheap model and transfer only the RL-induced policy shift (log-ratio dense reward) to a strong target.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No earthquake. A top AI-policy thread on [Hacker News](https://news.ycombinator.com/) argued against shutting off Chinese open-weight models — a policy attention event, no citable primary.
- The OpenAI × Hugging Face [security-incident](https://huggingface.co/blog/security-incident-july-2026) coverage kept topping HN — already tracked under [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn).
- Continued buzz on the Qwen 3.8-Max preview and Kimi K3 (weights due 07-27) under [Open-weight wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs); still preview/announcement, no new WEIGHTS drop.
- A recurring AI-for-math thread (an AI-assisted Jacobian-Conjecture counterexample) drew front-page attention on [Hacker News](https://news.ycombinator.com/) — watch-area only, no citable primary paper.
- Reddit r/LocalLLaMA (datacenter-IP-blocked JSON) and YouTube curator channels remain IP-blocked from this environment (known, multi-week).

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (25)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-07-24](reports/2026-07-24.md) · weekly: [2026-W30](reports/weekly/2026-W30.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
