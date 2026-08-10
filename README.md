# AI Radar

![trends](https://img.shields.io/badge/trends-19-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-7-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-17-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--08--10-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-08-08, weekly recalibration):**

- **Two major security disclosures, same day**: [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) gained OpenAI's [Astra critical-cyber-capability flag](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities) (first lab to flag a pre-release model against its Preparedness Framework's CRITICAL threshold) and Anthropic's [auto mode going default in Claude Code](https://claude.com/blog/auto-mode-default-in-claude-code) (rigorous eval: automated permission checks catch 89% of dangerous commands vs 13.6% for human review) — both flagged for the weekly as a possible mainstreaming trigger.
- **A fifth orchestration form**: [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) added Claude Code's [cross-session `SendMessage`/`ListAgents`](https://raw.githubusercontent.com/anthropics/claude-code/main/CHANGELOG.md) (independent sessions message each other directly, no human relay) — the community independently coined "Zawinski's Law of MultiAgents" for the same pattern this week.
- **Evidence adds**: [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) ← vLLM's [Decode Context Parallelism](https://blog.vllm.ai/blog/2026-08-07-decode-context-parallelism); [Agent harness/runtime infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) ← Scale AI's [HarnessOpt-Bench](https://arxiv.org/abs/2608.06301); [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) ← fully-unsupervised [U-OPSD](https://arxiv.org/abs/2608.06296).
- Full detail in the daily report [2026-08-10](reports/2026-08-10.md).

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
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-08-07](https://blog.vllm.ai/blog/2026-08-07-decode-context-parallelism) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🚀 accelerating | [2026-08-07](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-08-06](https://developers.openai.com/codex/plugins) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🚀 accelerating | [2026-08-06](https://arxiv.org/abs/2608.06301) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-08-04](https://arxiv.org/abs/2608.03457) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-08-03](https://www.microsoft.com/en-us/research/blog/orchard-an-open-framework-for-scalable-agentic-ai/) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-31](https://developer.nvidia.com/blog/co-designing-ai-model-attention-for-fast-interactive-long-context-inference/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-07](https://github.com/google-gemma/gemma-translator) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-08-07](https://raw.githubusercontent.com/anthropics/claude-code/main/CHANGELOG.md) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 emerging | [2026-08-06](https://arxiv.org/abs/2608.06296) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-08-05](https://blog.cloudflare.com/cloudflare-os/) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 📈 emerging | [2026-08-01](https://openai.com/index/ten-advances-in-mathematics) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-08-05](https://arxiv.org/abs/2608.05102) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-08-03](https://arxiv.org/abs/2608.02499) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-08-02](https://qwen.ai/blog?id=qwen3.8) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Worth studying

- [Auto mode is now the default in Claude Code](https://claude.com/blog/auto-mode-default-in-claude-code) — Anthropic's own methodology for whether automated permission-checking beats human review: 1,053-tester controlled study (89% vs 13.6% dangerous-command catch rate) plus a 720-attack third-party red-team comparison; a well-instrumented template for evaluating agent permission systems.
- [Responding to the next frontier of critical cyber capabilities](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities) — OpenAI's own definition of its Preparedness Framework's CRITICAL cybersecurity threshold, and why an upcoming model may have crossed it; the clearest public line yet between "high capability" and "needs fundamentally different internal controls."
- [Agent Plugins](https://developers.openai.com/codex/plugins) — OpenAI's new open standard, built with AWS, Cursor, GitHub, VS Code and Vercel, for packaging Skills + Connectors + MCP servers into one distributable format usable across compatible agent clients.
- [Humans missed 1 in 3 threats approving AI agent commands across 40,000 plays](https://scalex.dev/blog/ai-agent-permissions-stats/) — a browser game turned real dataset (409k decisions) showing data-exfiltration commands get missed 3x more often than obviously destructive ones; a sharp illustration of why manual human-in-the-loop approval is a weak last line of defense.
- [Cloudflare OS: an open platform for agents, apps, and work](https://blog.cloudflare.com/cloudflare-os/) — agents start with access to nothing, gaining typed capability bindings only on explicit grant; a concrete capability-security reference design for agent-execution infrastructure.
- [Prime Agent: A Self-Improving RLM Harness](https://www.primeintellect.ai/blog/prime-agent) — Prime Intellect's coding harness built around a named "Continual Harness" abstraction, arguing static hand-engineered scaffolding can't keep pace with what frontier models can already do.
- [Maple-Preview: a 20B-A1B ternary reasoning LLM at 218 tok/s on a Mac mini](https://deepgrove.ai/maple-preview) — DeepGrove's open ternary-weight ({−1,0,+1}) reasoning model (5.31 GB) that solves IMO-level problems on-device; the clearest demonstration yet that 1-bit-class quantization and real reasoning coexist.
- [Mixture-of-Kittens (MoK): a deterministic MoE training megakernel](https://github.com/cursor/mixture-of-kittens) — Cursor's open MoE-training megakernel for GB300 NVL72 racks, fusing all expert communication/computation into one deterministic kernel (up to 2.37× faster than public baselines).
- [Orchard: An open framework for scalable agentic AI](https://www.microsoft.com/en-us/research/blog/orchard-an-open-framework-for-scalable-agentic-ai/) — Microsoft Research's open, reusable Kubernetes environment service for agentic RL rollouts, training data and eval across SWE/GUI/personal-assistant agents.
- [Buzz: a workspace where humans and AI agents build together](https://github.com/block/buzz) — Block, Inc.'s open-source Nostr workspace where every message, workflow step and git event is a signed event, whether the author is a person or an agent.
- [Ten advances in mathematics and theoretical computer science](https://openai.com/index/ten-advances-in-mathematics) — an internal OpenAI Astra checkpoint producing new, formally-verified results on ten decades-open problems in pure math/TCS.
- [Autoregressive Language Model on the 6502 Processor](https://mattbeton.com/blog/bitnet-6502.html) — a BitNet-class model running on a 1975 BBC Micro; a clean teaching example of extreme low-bit/CPU inference engineering.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- [Interconnects](https://www.interconnects.ai/p/lessons-from-the-hacks) and [Latent.Space/AINews](https://www.latent.space/p/ainews-zawinskis-law-of-multiagents) both frame this week's OpenAI/Anthropic security disclosures as a turning point for lab-internal AI-safety practice — commentary only, no new primary beyond what's already routed to evidence.
- YouTube curator channels (code4AI, bycloud, AI Explained) were all reachable again this run after weeks of intermittent blocking — code4AI's harness-optimization coverage led directly to a new [agent-runtime-015](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) evidence item.
- [AlphaSignal](https://alphasignal.ai) was again the week's most productive lane, cross-referencing the Astra/auto-mode/cross-session-messaging cluster and surfacing an unverified UCLA finding that reward-hack monitors trained on prompted attacks collapse to ~28% accuracy against real training-time cheating — queued, arXiv id not yet pinned.
- Ant Group's efficiency-focused Ling-3.0-Flash release (124B total / 5.1B active) drew attention this week but sits off both the open-weight and small/CPU pinned axes — noted, not routed.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~17)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-08-10](reports/2026-08-10.md) · weekly: [2026-W32](reports/weekly/2026-W32.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
