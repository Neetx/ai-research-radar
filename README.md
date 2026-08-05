# AI Radar

![trends](https://img.shields.io/badge/trends-19-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-6-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-19-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--08--05-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-08-05):**

- **[On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms)** promoted seed → 📈 emerging: its pre-registered gate fired — [OPD Support in Miles](https://www.lmsys.org/blog/2026-07-18-opd-support-in-miles) ships OPD as a first-class trainer in the Miles RL framework (SGLang + Megatron).
- **[Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale)** reactivated dormant → 🚀 accelerating via [LLaDA MoE v2](https://arxiv.org/abs/2608.03457) (GSAI-ML) — the first systematic MoE-diffusion-LM scaling study.
- **New evidence**: [Maple-Preview](https://deepgrove.ai/maple-preview) (open 20B-A1B ternary reasoning LLM, 218 tok/s on a Mac mini) on [small/CPU models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference); [QM](https://github.com/yc-software/qm) (YC's multiplayer agent harness) on [multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a); [OpenAI's cyber-eval disclosure](https://openai.com/index/third-party-cyber-evaluations-involving-openai-models) on [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn).
- **Queue**: +10 intake (18 → 19 lines), `deepgrove.ai` staged — see [observation_queue](TRENDS.md#observation_queue). ⚠ [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) hits its 45-day archive line tomorrow (08-06).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-04](https://deepgrove.ai/maple-preview) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 3 · 📈 6 · 🚀 6 · 🌊 1 · 🏔 0 · 📉 0 · 💤 3

| trend | stage | latest signal |
|---|---|---|
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🚀 accelerating | [2026-08-04](https://openai.com/index/third-party-cyber-evaluations-involving-openai-models) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-08-04](https://arxiv.org/abs/2608.03457) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-08-03](https://www.microsoft.com/en-us/research/blog/orchard-an-open-framework-for-scalable-agentic-ai/) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-31](https://developer.nvidia.com/blog/co-designing-ai-model-attention-for-fast-interactive-long-context-inference/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-07-29](https://www.together.ai/blog/thunderagent) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-07-28](https://blog.modelcontextprotocol.io/posts/2026-07-28/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-04](https://deepgrove.ai/maple-preview) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 📈 emerging | [2026-08-01](https://openai.com/index/ten-advances-in-mathematics) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-07-31](https://github.com/yc-software/qm) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 📈 emerging | [2026-07-30](https://www.microsoft.com/en-us/research/blog/evolib-turning-experience-into-evolving-knowledge/) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 emerging | [2026-07-30](https://arxiv.org/abs/2607.28590) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-08-03](https://arxiv.org/abs/2608.02499) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-07-28](https://arxiv.org/abs/2607.25308) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-08-02](https://qwen.ai/blog?id=qwen3.8) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |

## Worth studying

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
- [TurboFieldfare](https://github.com/drumih/turbo-fieldfare) — a 26B MoE running in ~2GB RAM on an 8GB Mac via per-token expert streaming from SSD; a clean worked example of "stream, don't shrink."
- [Context Collapse, Part 3 — AI Worming through Word](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word) — the first self-replicating prompt-injection worm in a mainstream productivity suite, MSRC-coordinated.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No earthquake on the [Hacker News front page](https://news.ycombinator.com/) today — top items are generalist/culture posts (a memorial, color-space tooling), not AI.
- On-axis HN discussion surfaced [Maple-Preview](https://deepgrove.ai/maple-preview) (ternary 20B on iPhone) and [Mistral's Shieldstral 3B](https://mistral.ai/news/shieldstral/) safety model — both followed to primaries and routed/queued.
- Model-release rumor churn on [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) with no primary confirmation this run — watching.
- The [curator lane](https://alphamatch.ai/blog) surfaced YC's [QM agent harness](https://github.com/yc-software/qm) and Cursor's [Mixture-of-Kittens](https://github.com/cursor/mixture-of-kittens) — both followed to primary repos.
- YouTube curator channels (code4AI, bycloud, AI Explained) remain unreachable (confirmed re-blocked as of 07-29); re-test is due on the weekly cadence.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~19)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-08-05](reports/2026-08-05.md) · weekly: [2026-W31](reports/weekly/2026-W31.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
