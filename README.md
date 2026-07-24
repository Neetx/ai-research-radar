# AI Radar

![trends](https://img.shields.io/badge/trends-18-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-4-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-25-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--07--24-2f9e44?style=flat-square)

Tracking AI-ecosystem trends (frontier research → engineering) for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-07-24):**
- **Parametric injection** REACTIVATED 💤 dormant → 🌱 **seed** — a new independent group brings train-time knowledge-into-weights via hypernetworks with scaling laws ([2607.19604](https://arxiv.org/abs/2607.19604)); routed as evidence to [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext).
- **Open-weight wave** adds a NEW lab — Upstage ships [Solar-Open2-250B](https://huggingface.co/upstage/Solar-Open2-250B) (320-expert / 8-active MoE, 1M ctx, downloadable), evidence for [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs).
- **Deployment-grounded agent eval** refreshed — Tencent [WorkBuddy Bench](https://arxiv.org/abs/2607.20911) (contamination-resistant multi-domain coding-agent benchmark) → [evidence](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards).
- Watchlist steady at 25 (+3 intake: AREX, NVIDIA OO Agents, Nunchaku 4-bit diffusion; −3 stale) → [watchlist](TRENDS.md#observation_queue). No new frontier open-weight WEIGHTS drop, no earthquake (07-28 final MCP spec 4 days out).

## ⭐ Pinned topics

| trend | stage | latest signal |
| --- | --- | --- |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 5 · 📈 4 · 🚀 4 · 🌊 1 · 🏔 0 · 📉 0 · 💤 4

| trend | stage | latest signal |
| --- | --- | --- |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-16](https://www.kimi.com/blog/kimi-k3) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-07-07](https://arxiv.org/abs/2607.05722) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-07-01](https://arxiv.org/abs/2607.00466) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-29](https://blog.modelcontextprotocol.io/posts/sdk-betas-2026-07-28/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-07-22](https://huggingface.co/blog/security-incident-july-2026) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-07-23](https://arxiv.org/abs/2607.20911) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-07-20](https://arxiv.org/abs/2607.18110) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🌱 seed | [2026-07-16](https://arxiv.org/abs/2607.14777) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌱 seed | [2026-07-14](https://arxiv.org/abs/2607.13285) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-07-22](https://huggingface.co/upstage/Solar-Open2-250B) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 💤 dormant | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 💤 dormant | [2026-06-22](https://sakana.ai/fugu-release/) |

## Worth studying

- [Solar-Open2-250B (Upstage, 320-expert / 8-active MoE, 1M ctx)](https://huggingface.co/upstage/Solar-Open2-250B) — a fresh open-weights architecture datapoint from a lab new to the open-weight set: very high expert count with very sparse routing, 1M context, downloadable weights.
- [Scaling Laws for Hypernetwork-Based Knowledge Injection](https://arxiv.org/abs/2607.19604) — can you reliably compile factual knowledge INTO weights at scale? Repurposes hypernetworks as a train-time knowledge-injection mechanism and derives scaling laws — the reference for parametric-injection-vs-RAG.
- [SLPO: outcome-reward RL for latent reasoners](https://arxiv.org/abs/2607.19691) — a surrogate policy density over latent transitions for trajectory-level credit + a learned variable-horizon stopping head; the training-side reference for the latent-reasoning axis.
- [GigaToken: a ~1000× faster LLM tokenizer in Rust](https://github.com/marcelroed/gigatoken) — a practical systems artifact for tokenization-bound data/serving pipelines; study the Rust pretokenizer engineering + optimization writeups.
- [The HF security incident: first real-world autonomous-AI-agent intrusion of a major AI platform](https://huggingface.co/blog/security-incident-july-2026) — HF's own disclosure: malicious dataset → RCE in the data pipeline → agent-swarm lateral movement; the canonical threat-model writeup for anyone running dataset/agent pipelines.
- [LLM-as-a-Coach: experiential learning for non-verifiable tasks](https://arxiv.org/abs/2607.18110) — turn the RL judge into a coach emitting transferable experiential feedback: the practical answer to running RL when you can't write a verifier.
- [Loopie: the strongest looped-Transformer MoE to date](https://arxiv.org/abs/2607.16051) — the clearest current answer to the looped-transformer's oldest objection, at MoE scale.
- [MCP goes stateless: the 2026-07-28 spec, four Tier-1 SDK betas, and Enterprise-Managed Auth](https://blog.modelcontextprotocol.io/posts/sdk-betas-2026-07-28/) — the shape of the MCP standard as it heads to its final spec.
- [Kimi K3: the first open 3T-class model (KDA + Attention Residuals + Stable LatentMoE)](https://www.kimi.com/blog/kimi-k3) — Moonshot's newest flagship, a 2.8T-parameter MoE.
- [Inkling: a ~1T-param multimodal open-weights model with relative attention](https://huggingface.co/thinkingmachines/Inkling) — Thinking Machines' first open-weights model (Apache-2.0).
- [Bonsai 27B: the first 27B-class model to run on a phone](https://prismml.com/news/bonsai-27b) — a Qwen3.6-27B-based multimodal model shipped low-bit end-to-end.
- [Direct-OPD: Weak-to-Strong Generalization via Direct On-Policy Distillation](https://arxiv.org/abs/2607.05394) — a clean, practically-motivated post-training recipe.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No earthquake. Top AI-policy thread on [Hacker News](https://news.ycombinator.com/) argued against shutting off Chinese open-weight models — a policy attention event, no citable primary.
- The OpenAI × Hugging Face [security-incident](https://huggingface.co/blog/security-incident-july-2026) coverage topped HN again — already tracked under [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn).
- Continued buzz on the Qwen 3.8-Max preview and Kimi K3 (weights due 07-27) under [Open-weight wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs); still preview/announcement, no new WEIGHTS drop.
- Reddit r/LocalLLaMA (datacenter-IP-blocked JSON) and YouTube curator channels remain IP-blocked from this environment (known, multi-week).

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (25)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-07-24](reports/2026-07-24.md) · weekly: [2026-W29](reports/weekly/2026-W29.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
