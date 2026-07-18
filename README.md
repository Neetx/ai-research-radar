# AI Radar

![trends](https://img.shields.io/badge/trends-18-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-4-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-25-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--07--18-2f9e44?style=flat-square)

Tracking AI-ecosystem trends (frontier research → engineering) for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-07-18, weekly W29):**
- Reactivated: **[MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks)** 💤 dormant → 🚀 accelerating (confidence → high) — the weekly sweep of the (un-swept) MCP blog captured two interim primaries: [EMA-stable auth](https://blog.modelcontextprotocol.io/posts/enterprise-managed-auth/) (06-18, adopted by Okta + Anthropic + Microsoft + 8 servers) and [four Tier-1 SDK betas](https://blog.modelcontextprotocol.io/posts/sdk-betas-2026-07-28/) (06-29) for the 07-28 stateless-core spec.
- Coverage fix: the MCP blog was a named reactivation-watch but in no swept list (~3–4-week capture lag) → promoted to the swept registry; amendment **W28-P1 applied** (Meta AI + Together AI re-tiered to low-cadence).
- Anchoring warning (2nd consecutive — all daily evidence on pre-existing trends), partially mitigated by the non-arXiv MCP capture. Daily dormancy marks confirmed (rl-env / agent-sandbox / multi-agent-eng / low-bit quant). Capture-leak 20/0.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-15](https://arxiv.org/abs/2607.13491) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 5 · 📈 4 · 🚀 4 · 🌊 1 · 🏔 0 · 📉 0 · 💤 4

| trend | stage | latest signal |
|---|---|---|
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-16](https://www.kimi.com/blog/kimi-k3) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-07-07](https://arxiv.org/abs/2607.05722) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-07-01](https://arxiv.org/abs/2607.00466) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-29](https://blog.modelcontextprotocol.io/posts/sdk-betas-2026-07-28/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-15](https://arxiv.org/abs/2607.13491) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-30](https://arxiv.org/abs/2606.31227) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🌱 seed | [2026-07-16](https://arxiv.org/abs/2607.14777) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌱 seed | [2026-07-14](https://arxiv.org/abs/2607.13285) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-07-09](https://arxiv.org/abs/2607.08964) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-02](https://arxiv.org/abs/2607.02512) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-06-30](https://arxiv.org/abs/2606.32034) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-07-16](https://www.kimi.com/blog/kimi-k3) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 💤 dormant | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 💤 dormant | [2026-06-22](https://sakana.ai/fugu-release/) |

## Worth studying

- [MCP goes stateless: the 2026-07-28 spec, four SDK betas, and Enterprise-Managed Auth](https://blog.modelcontextprotocol.io/posts/sdk-betas-2026-07-28/) — the biggest MCP revision since launch: stateless core (no init handshake/session, round-robin-scalable), MRTR, routable headers, four Tier-1 SDK betas + now-stable zero-touch OAuth (Okta/Anthropic/Microsoft).
- [Kimi K3: the first open 3T-class model (KDA + Attention Residuals + Stable LatentMoE)](https://www.kimi.com/blog/kimi-k3) — Moonshot's 2.8T-param flagship; delta/linear attention + a new depth-wise residual pathway as the native substrate of a frontier open model (weights due 07-27).
- [Inkling: a ~1T-param multimodal open-weights model with relative attention](https://huggingface.co/thinkingmachines/Inkling) — Thinking Machines' first open model (952B/41B, image+audio+text, 1M ctx); drops RoPE for learned relative attention + interleaved local/global layers.
- [Bonsai 27B: the first 27B-class model to run on a phone](https://prismml.com/news/bonsai-27b) — PrismML: a Qwen3.6-27B-based multimodal model shipped low-bit end-to-end (1-bit 3.9 GB / ternary 5.9 GB), fits an iPhone.
- [Direct-OPD: Weak-to-Strong Generalization via Direct On-Policy Distillation](https://arxiv.org/abs/2607.05394) — run RL on a small cheap model, transfer only the RL-induced policy shift (log-ratio dense reward) to the strong target.
- [Flash-MSA: open-source training kernels for MiniMax Sparse Attention](https://nanduruganesh.github.io/flash-msa/) — a rare open artifact on the *training* side of sparse attention (block-sparse, GQA, group-wise proxy heads) on Hopper/Blackwell.
- [Colibri: run GLM-5.2 (744B MoE) on a 25 GB-RAM machine in pure C](https://github.com/JustVugg/colibri) — zero-dependency engine streaming MoE experts from disk; existence proof for extreme CPU-first expert-offloading.
- [UniClawBench: capability-driven eval of proactive agents in live containers](https://arxiv.org/abs/2607.08768) — live Docker containers scored by step-by-step checkpoints, tasks decomposed by five foundational capabilities.
- [Nemotron-Labs-Diffusion: a tri-mode AR + diffusion + self-speculation LM](https://arxiv.org/abs/2607.05722) — one model, joint AR-diffusion objective, mode-switching by deployment regime; open at 3B/8B/14B.
- [OmniOpt: Taxonomy, Geometry, and Benchmarking of Modern Optimizers](https://arxiv.org/abs/2607.04033) — a unified survey + benchmark cookbook for 100+ optimizers as a five-stage meta-pipeline.
- [Bridging Latent and Explicit Reasoning with Looped Transformers](https://arxiv.org/abs/2606.31779) — names why latent CoT underperforms beyond ~1B params and gives a looped-transformer recipe that closes the gap.
- [AI-Infra-Guard: Multi-Layer Agent Red Teaming](https://arxiv.org/abs/2606.31227) — open-source blueprint matching a detection paradigm to each layer of the agent attack surface (infra/protocol/behavior/model).

## Community pulse

_Unverified sentiment from social/community channels — intake only, never trend evidence, no individuals named._

- Frontier open models topped Hacker News two weeks running: Moonshot's [Kimi K3](https://www.kimi.com/blog/kimi-k3) (#1, ~1390 pts) and Thinking Machines' [Inkling](https://huggingface.co/thinkingmachines/Inkling) (#1, ~840 pts) — both captured as verified evidence above.
- On-device demo: a community post running [Gemma 4 26B at ~5 tok/s on a 13-year-old Xeon, no GPU](https://hn.algolia.com/?query=Gemma%204%20Xeon) (small-CPU-adjacent, no new artifact).
- Local-agent tooling: [LM Studio "Bionic"](https://hn.algolia.com/?query=LM%20Studio%20Bionic) — an agent runtime for open models (queued as intake).
- Platform security: Hugging Face posted a [security incident disclosure](https://huggingface.co/blog) for July 2026 (field news, no model artifact).

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (25)](TRENDS.md#observation_queue) · [reports/](reports/) ([2026-07-17](reports/2026-07-17.md)) · weekly: [2026-W29](reports/weekly/2026-W29.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
