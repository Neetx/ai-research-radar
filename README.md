# AI Radar

![trends](https://img.shields.io/badge/trends-19-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-6-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-20-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--08--06-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-08-06):**

- **[Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents)** REACTIVATED dormant → 📈 emerging, on the exact 45-day archive line — [Cloudflare OS](https://blog.cloudflare.com/cloudflare-os/) (capability-scoped agent runtime) and [Zed 1.14](https://zed.dev/blog/sandboxing) (OS-enforced sandboxing, on by default) both landed the same day.
- **New evidence**: [PromptArmor's Atlassian Rovo disclosure](https://www.promptarmor.com/resources/atlassian-rovo-exfiltrates-data) (unpatched data-exfil) on [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn); [Prime Agent](https://www.primeintellect.ai/blog/prime-agent) on [agent harness/runtime](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object); [Muse Code](https://research.meta.ai/blog/introducing-muse-code-and-muse-spark-1-2) (Meta) on [multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a).
- **Queue**: +11 intake (19 → 20 lines) — see [observation_queue](TRENDS.md#observation_queue). Four source candidates staged (`primeintellect.ai`, `zed.dev`, `promptarmor.com`); `blog.cloudflare.com` crosses the ≥2-artifact promotion bar for the weekly.
- **Pulse**: a genuine earthquake — [Google DeepMind's leadership shakeup](https://blog.google/company-news/inside-google/message-ceo/next-chapter-ai-momentum/) (Hassabis CEO→Chair, Jeff Dean departing) topped both Hacker News and r/singularity today; off-axis corporate news, not a trend — see Community pulse below.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-04](https://deepgrove.ai/maple-preview) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 3 · 📈 7 · 🚀 6 · 🌊 1 · 🏔 0 · 📉 0 · 💤 2

| trend | stage | latest signal |
|---|---|---|
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🚀 accelerating | [2026-08-05](https://www.promptarmor.com/resources/atlassian-rovo-exfiltrates-data) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-08-04](https://arxiv.org/abs/2608.03457) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-08-03](https://www.microsoft.com/en-us/research/blog/orchard-an-open-framework-for-scalable-agentic-ai/) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-31](https://developer.nvidia.com/blog/co-designing-ai-model-attention-for-fast-interactive-long-context-inference/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-07-29](https://www.together.ai/blog/thunderagent) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-07-28](https://blog.modelcontextprotocol.io/posts/2026-07-28/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-08-05](https://blog.cloudflare.com/cloudflare-os/) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 📈 emerging | [2026-08-05](https://www.primeintellect.ai/blog/prime-agent) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-08-05](https://research.meta.ai/blog/introducing-muse-code-and-muse-spark-1-2) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-04](https://deepgrove.ai/maple-preview) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 emerging | [2026-08-04](https://arxiv.org/abs/2608.03632) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 📈 emerging | [2026-08-01](https://openai.com/index/ten-advances-in-mathematics) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-08-03](https://arxiv.org/abs/2608.02499) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-07-28](https://arxiv.org/abs/2607.25308) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-08-02](https://qwen.ai/blog?id=qwen3.8) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Worth studying

- [Cloudflare OS: an open platform for agents, apps, and work](https://blog.cloudflare.com/cloudflare-os/) — agents start with access to nothing, gaining typed capability bindings only on explicit grant; a concrete capability-security reference design for agent-execution infrastructure.
- [Prime Agent: A Self-Improving RLM Harness](https://www.primeintellect.ai/blog/prime-agent) — Prime Intellect's coding harness built around a named "Continual Harness" abstraction, arguing static hand-engineered scaffolding can't keep pace with what frontier models can already do.
- [Maple-Preview: a 20B-A1B ternary reasoning LLM at 218 tok/s on a Mac mini](https://deepgrove.ai/maple-preview) — DeepGrove's open ternary-weight ({−1,0,+1}) reasoning model (5.31 GB) that solves IMO-level problems on-device; the clearest demonstration yet that 1-bit-class quantization and real reasoning coexist.
- [Mixture-of-Kittens (MoK): a deterministic MoE training megakernel](https://github.com/cursor/mixture-of-kittens) — Cursor's open MoE-training megakernel for GB300 NVL72 racks, fusing all expert communication/computation into one deterministic kernel (up to 2.37× faster than public baselines).
- [Orchard: An open framework for scalable agentic AI](https://www.microsoft.com/en-us/research/blog/orchard-an-open-framework-for-scalable-agentic-ai/) — Microsoft Research's open, reusable Kubernetes environment service for agentic RL rollouts, training data and eval across SWE/GUI/personal-assistant agents.
- [Buzz: a workspace where humans and AI agents build together](https://github.com/block/buzz) — Block, Inc.'s open-source Nostr workspace where every message, workflow step and git event is a signed event, whether the author is a person or an agent.
- [Ten advances in mathematics and theoretical computer science](https://openai.com/index/ten-advances-in-mathematics) — an internal OpenAI Astra checkpoint producing new, formally-verified results on ten decades-open problems in pure math/TCS.
- [Autoregressive Language Model on the 6502 Processor](https://mattbeton.com/blog/bitnet-6502.html) — a BitNet-class model running on a 1975 BBC Micro; a clean teaching example of extreme low-bit/CPU inference engineering.
- [Investigating three real-world incidents in our cybersecurity evaluations](https://www.anthropic.com/news/investigating-incidents-cybersecurity-evals) — models under misconfigured eval sandboxing attacked genuinely live internet-connected systems; an eval-infrastructure failure mode worth designing against.
- [Echoverse](https://www.microsoft.com/en-us/research/blog/echoverse-deep-evolving-environments-for-computer-use-agents/) — Microsoft Research's co-evolution loop for computer-use-agent training environments, nearly doubling a 9B model's accuracy.
- [Discovering cryptographic weaknesses with Claude](https://www.anthropic.com/research/discovering-cryptographic-weaknesses) — Claude Mythos Preview autonomously found a genuine mathematical weakness in a post-quantum signature scheme and a new round-reduced AES attack.
- [How enabling two settings tripled our scores on the ARC-AGI-3 benchmark](https://openai.com/index/how-two-settings-tripled-our-arc-agi-3-scores) — OpenAI's own demonstration that agent benchmark scores are a property of the harness as much as the model.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- **Earthquake**: [Google DeepMind leadership shakeup](https://blog.google/company-news/inside-google/message-ceo/next-chapter-ai-momentum/) (Demis Hassabis CEO→Chair, Jeff Dean departing) topped both the [Hacker News front page](https://news.ycombinator.com/) (645 pts) and [r/singularity](https://www.reddit.com/r/singularity/) today — corporate/leadership news, not a research trend, but the field is consumed by it.
- HN also surfaced [Cloudflare OS](https://blog.cloudflare.com/cloudflare-os/), [Atlassian Rovo's data-exfiltration disclosure](https://www.promptarmor.com/resources/atlassian-rovo-exfiltrates-data) and [Prime Agent](https://www.primeintellect.ai/blog/prime-agent) — all three followed to primaries and routed as evidence.
- [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/)'s top post was also Prime Agent ("a new coding harness surpassing Codex/CC"), corroborating cross-community reach.
- YouTube curator channels (code4AI, bycloud, AI Explained) are reachable again as of today — code4AI's paper picks (Metis memory model, SciToolAgent-Evo, RecHarness) were cross-checked against existing evidence/queue, no duplicates.
- The [curator lane](https://alphamatch.ai/blog) and [AlphaSignal](https://alphasignal.ai) both independently surfaced Prime Agent and Meta's Muse Code the same day — strong cross-source corroboration.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~20)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-08-06](reports/2026-08-06.md) · weekly: [2026-W31](reports/weekly/2026-W31.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
