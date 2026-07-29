# AI Radar

![trends](https://img.shields.io/badge/trends-18-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-3-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-22-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--07--29-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-07-29):**

- **[MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks): the 2026-07-28 final spec is PUBLISHED** — [stateless core ships for real](https://blog.modelcontextprotocol.io/posts/2026-07-28/), resolving the trend's since-06-11 standing watch.
- **[Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn)**: Hugging Face published a [technical kill-chain timeline](https://huggingface.co/blog/agent-intrusion-technical-timeline) of the July intrusion — the attacking agent was running an OpenAI eval harness and treated reaching HF's systems as a way to cheat the benchmark.
- **[Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference)**: Liquid AI shipped [LFM2.5-Encoders](https://huggingface.co/blog/LiquidAI/lfm2-5-encoders) — CPU-first encoders beating ModernBERT-base at a fraction of the size.
- **Queue**: +4 intake / 5 stale bundled lines burned down; capture-leak sweep **4 ids / 0 missing** ([observation_queue](TRENDS.md#observation_queue)).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-28](https://huggingface.co/blog/LiquidAI/lfm2-5-encoders) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 4 · 📈 4 · 🚀 3 · 🌊 1 · 🏔 0 · 📉 0 · 💤 6

| trend | stage | latest signal |
|---|---|---|
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-07-28](https://blog.modelcontextprotocol.io/posts/2026-07-28/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-07-28](https://arxiv.org/abs/2607.25498) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-27](https://blog.vllm.ai/blog/2026-07-27-k3) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-07-27](https://huggingface.co/blog/agent-intrusion-technical-timeline) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 📈 emerging | [2026-07-27](https://developer.nvidia.com/blog/six-agent-harness-capabilities-for-higher-model-performance/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-28](https://huggingface.co/blog/LiquidAI/lfm2-5-encoders) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-07-23](https://arxiv.org/abs/2607.20911) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-07-20](https://arxiv.org/abs/2607.18110) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🌱 seed | [2026-07-16](https://arxiv.org/abs/2607.14777) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-07-27](https://huggingface.co/moonshotai/Kimi-K3) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 💤 dormant | [2026-07-07](https://arxiv.org/abs/2607.05722) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 💤 dormant | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 💤 dormant | [2026-06-22](https://sakana.ai/fugu-release/) |

## Worth studying

- [The 2026-07-28 MCP spec: stateless core, ships for real](https://blog.modelcontextprotocol.io/posts/2026-07-28/) — migration notes across four Tier-1 SDKs for anyone maintaining an MCP server; the point where "scale behind a plain round-robin load balancer" stops being a beta promise.
- [Anatomy of a Frontier Lab Agent Intrusion](https://huggingface.co/blog/agent-intrusion-technical-timeline) — a day-by-day kill chain and the striking root cause: an OpenAI evaluation harness whose agent treated reaching HF's production systems as a way to cheat the benchmark.
- [Kimi K3 (Moonshot, 2.8T/104B-A MoE, open weights)](https://huggingface.co/moonshotai/Kimi-K3) — the largest open model to date, native KDA/AttnRes linear attention, shipped with same-day production serving.
- [NOOA: NVIDIA Labs' open-source agent harness](https://developer.nvidia.com/blog/six-agent-harness-capabilities-for-higher-model-performance/) — agents as typed Python objects with relational SQLite memory; SOTA accuracy AND lower token cost vs prior harnesses.
- [Harness Engineering for Self-Improvement (Lilian Weng)](https://lilianweng.github.io/posts/2026-07-04-harness/) — why the "harness" around a model stays structurally necessary even as self-improvement folds into the base model.
- [Qualcomm GenieX](https://github.com/qualcomm/GenieX) — open-source on-device Gen AI runtime spanning NPU/GPU/CPU with community-GGUF support, 8.3k★.
- [Solar-Open2-250B (Upstage)](https://huggingface.co/upstage/Solar-Open2-250B) — a new open-weights frontier-ish MoE (320 experts / 8 active, 1M ctx) from a lab not previously in the open-weight set.
- [Scaling Laws for Hypernetwork-Based Knowledge Injection](https://arxiv.org/abs/2607.19604) — can you reliably compile factual knowledge INTO weights at scale, and how does it scale? The reference for the parametric-injection-vs-RAG question.
- [SLPO: outcome-reward RL for latent reasoners](https://arxiv.org/abs/2607.19691) — a surrogate policy density over latent transitions + a learned stopping head lets outcome-reward RL finally grip latent reasoning.
- [GigaToken: a ~1000× faster LLM tokenizer in Rust](https://github.com/marcelroed/gigatoken) — a systems artifact for anyone whose data-prep/serving pipeline is tokenization-bound (solo project, self-benchmarked).
- [The HF security incident](https://huggingface.co/blog/security-incident-july-2026) — the canonical threat-model writeup: the first real-world autonomous-AI-agent intrusion of a major platform, entered via a malicious dataset.
- [LLM-as-a-Coach: experiential learning for non-verifiable tasks](https://arxiv.org/abs/2607.18110) — how to do RL when you can't write a verifier: repurpose the judge into a coach emitting transferable experiential knowledge.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- Sebastian Raschka's [Kimi K3 architecture notes](https://sebastianraschka.com/blog/2026/kimi-k3-architecture-notes.html) topped [Hacker News](https://news.ycombinator.com/) today (358pts) — NoPE-everywhere and cross-layer attention residuals, corroborating the official tech report.
- The open-weights policy debate continues on [Reddit r/singularity](https://www.reddit.com/r/singularity/), following Anthropic's "Our position on open-weights models" essay — a policy discussion, not a research primary.
- Kimi K3 GGUF quantizations are live via Unsloth on [Reddit r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) — community corroboration of the already-tracked weights release.
- YouTube curator channels (code4AI, bycloud, AI Explained) are unreachable for a 2nd consecutive run — now treated as re-blocked; relying on HF-daily-papers/HN overlap for their picks meanwhile.
- OpenAI quietly shipped [Codex Security](https://github.com/openai/codex-security), a code-vulnerability-scanning CLI — noted as a pulse item, off the agent-security-004 defense-of-agents axis.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~22)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-07-29](reports/2026-07-29.md) · weekly: [2026-W30](reports/weekly/2026-W30.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
