# AI Radar

![trends](https://img.shields.io/badge/trends-19-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-7-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-16-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--08--08-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-08-08, weekly recalibration):**

- **Stage moves**: [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) promoted emerging → accelerating (Prime Intellect's [Prime Agent](https://www.primeintellect.ai/blog/prime-agent) is the pre-registered gate's "second independently-shipped harness framework," after NVIDIA's NOOA); [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) confidence raised to medium (three independent groups — ECHO, CAST, [ABSeeker](https://arxiv.org/abs/2608.05102) — now converge on turn-level credit), held at seed pending a shared benchmark.
- **Source growth**: [Cloudflare's blog](https://blog.cloudflare.com/) promoted to the swept lab-blog registry after two on-axis primaries this month; a genuine coverage gap was found and flagged — the Hugging Face lab blog was silently missed all week (distinct from the HF-papers exploration lane, which ran daily).
- **Queue & shelf**: [observation_queue](TRENDS.md#observation_queue) condensed 7 stale lines (07-18..07-25) into one tombstone, now 16 live; the study shelf pruned its 07-02..07-08 tail past the 30-day floor.
- Full detail in the [W32 weekly report](reports/weekly/2026-W32.md).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-07](https://github.com/google-gemma/gemma-translator) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 3 · 📈 6 · 🚀 7 · 🌊 1 · 🏔 0 · 📉 0 · 💤 2

| trend | stage | latest signal |
|---|---|---|
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-08-06](https://developers.openai.com/codex/plugins) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-08-05](https://arxiv.org/abs/2608.04502) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🚀 accelerating | [2026-08-05](https://www.promptarmor.com/resources/atlassian-rovo-exfiltrates-data) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🚀 accelerating | [2026-08-05](https://www.primeintellect.ai/blog/prime-agent) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-08-04](https://arxiv.org/abs/2608.03457) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-08-03](https://www.microsoft.com/en-us/research/blog/orchard-an-open-framework-for-scalable-agentic-ai/) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-31](https://developer.nvidia.com/blog/co-designing-ai-model-attention-for-fast-interactive-long-context-inference/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-07](https://github.com/google-gemma/gemma-translator) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-08-05](https://blog.cloudflare.com/cloudflare-os/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-08-05](https://research.meta.ai/blog/introducing-muse-code-and-muse-spark-1-2) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 emerging | [2026-08-04](https://arxiv.org/abs/2608.03632) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 📈 emerging | [2026-08-01](https://openai.com/index/ten-advances-in-mathematics) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-08-05](https://arxiv.org/abs/2608.05102) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-08-03](https://arxiv.org/abs/2608.02499) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-08-02](https://qwen.ai/blog?id=qwen3.8) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Worth studying

- [Agent Plugins](https://developers.openai.com/codex/plugins) — OpenAI's new open standard, built jointly with AWS, Cursor, GitHub, VS Code and Vercel, for packaging Skills + Connectors + MCP servers into one distributable format usable across compatible agent clients.
- [Humans missed 1 in 3 threats approving AI agent commands across 40,000 plays](https://scalex.dev/blog/ai-agent-permissions-stats/) — a browser game turned real dataset (409k decisions) showing data-exfiltration commands get missed 3x more often than obviously destructive ones; a sharp illustration of why manual human-in-the-loop approval is a weak last line of defense.
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

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- The Google DeepMind leadership change (Demis Hassabis CEO → Chair, Jeff Dean departing) topped both [Hacker News](https://news.ycombinator.com/) and r/singularity simultaneously this week — corporate/leadership news, not a research trend, so it stays a pulse note rather than ledger evidence.
- YouTube curator channels (code4AI, bycloud, AI Explained) kept flip-flopping between reachable and blocked all week — the radar now re-tests every run rather than waiting for the weekly cadence, given how unstable the pattern has been.
- [AlphaSignal](https://alphasignal.ai) and the HN front page were the week's most productive curator lanes, surfacing Prime Agent, Muse Code, and Google's Gemma Translator among other finds that made it into evidence.
- Press (via [Simon Willison's blog](https://simonwillison.net)) reported a Meta model "hacked" another company during a misconfigured cybersecurity evaluation — the same failure pattern already tracked for OpenAI and Anthropic — but no official Meta primary has surfaced yet, so it stays an unverified queue item.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~16)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-08-07](reports/2026-08-07.md) · weekly: [2026-W32](reports/weekly/2026-W32.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
