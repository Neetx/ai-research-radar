# AI Radar

![trends](https://img.shields.io/badge/trends-19-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-7-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-16-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--08--13-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-08-12):**

- **Qwen3.8-Max weights ship**: [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) closes an 11-day watch as Alibaba's [2.4T-parameter Qwen3.8-Max](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) goes downloadable, with day-0 NVIDIA GB300 serving; its hybrid linear/full-attention backbone also lands as evidence on [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models).
- **A seventh multi-agent orchestration form**: [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) gained Zed's [Delta](https://zed.dev/blog/introducing-delta) — a multiplayer human+agent code-review environment anchored to a live, evolving worktree.
- **AI writing its own papers**: [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) gained [Spark-to-Paper](https://arxiv.org/abs/2608.11924), an end-to-end research-paper-generation system built as 13 composable coding-assistant skills.
- Full detail in the daily report [2026-08-13](reports/2026-08-13.md).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-10](https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-08-10](https://arxiv.org/abs/2608.09888) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 3 · 📈 6 · 🚀 7 · 🌊 1 · 🏔 0 · 📉 0 · 💤 2

| trend | stage | latest signal |
|---|---|---|
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🚀 accelerating | [2026-08-11](https://developer.nvidia.com/blog/nvidia-nemotron-3-5-lightning-delivers-fast-accurate-specialized-task-execution-for-long-running-agents/) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-08-10](https://blog.cloudflare.com/mcp-v2/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🚀 accelerating | [2026-08-10](https://arxiv.org/abs/2608.09867) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-08-08](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-08-07](https://www.primeintellect.ai/blog/multi-agent-systems) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-08-07](https://blog.vllm.ai/blog/2026-08-07-decode-context-parallelism) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-08-04](https://arxiv.org/abs/2608.03457) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-08-12](https://zed.dev/blog/introducing-delta) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 📈 emerging | [2026-08-12](https://arxiv.org/abs/2608.11924) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-08-10](https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-08-10](https://arxiv.org/abs/2608.09888) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 emerging | [2026-08-10](https://arxiv.org/abs/2608.04419) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-08-10](https://blog.cloudflare.com/kitesurf/) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-08-10](https://arxiv.org/abs/2608.09819) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-08-05](https://arxiv.org/abs/2608.05102) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-08-03](https://arxiv.org/abs/2608.02499) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-08-10](https://huggingface.co/Motif-Technologies/Motif-3-NVFP4) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Worth studying

- [Introducing Delta](https://zed.dev/blog/introducing-delta) — Zed's new multiplayer environment for coding with agents: comments anchored to a live, evolving worktree instead of a stale diff, agent and teammates sharing the same conversational context, layered on the git repo you already use.
- [Stealing Reasoning Traces from Proprietary LLM APIs](https://arxiv.org/abs/2608.09867) — encrypted chain-of-thought is not isolated across a provider's own model family: a jailbroken cheap sibling decodes a frontier model's hidden reasoning verbatim, demonstrated across Anthropic/OpenAI/Google with real credentials/PII recovered from public agent trajectories.
- [BDH-CQ: In-Context Learning with Recurrent Latent Reasoning](https://arxiv.org/abs/2608.09888) — a recurrent latent-reasoning model breaking the ARC-AGI-1 cost-accuracy Pareto frontier at 150M parameters; a rare case of a latent/continuous-reasoning architecture delivering genuine SOTA rather than just an architectural study.
- [Introducing Muse Glimmer](https://research.meta.ai/blog/introducing-muse-glimmer-open-agentic-model) — Meta Superintelligence Labs' first open release: a concrete distillation recipe for compressing a frontier agentic model to consumer hardware, day-0 llama.cpp/MLX/ExecuTorch support.
- [Macaron-V1](https://arxiv.org/abs/2608.09819) — a released, reusable reference architecture for "compile behavior into adapters instead of prompt/context" at production scale (744B base + Mixture-of-LoRA specialists), with an actually-open harness to read.
- [Auto mode is now the default in Claude Code](https://claude.com/blog/auto-mode-default-in-claude-code) — Anthropic's own methodology for whether automated permission-checking beats human review: 1,053-tester controlled study (89% vs 13.6% dangerous-command catch rate) plus a 720-attack third-party red-team comparison; a well-instrumented template for evaluating agent permission systems.
- [Responding to the next frontier of critical cyber capabilities](https://openai.com/index/responding-next-frontier-critical-cyber-capabilities) — OpenAI's own definition of its Preparedness Framework's CRITICAL cybersecurity threshold, and why an upcoming model may have crossed it; the clearest public line yet between "high capability" and "needs fundamentally different internal controls."
- [Agent Plugins](https://developers.openai.com/codex/plugins) — OpenAI's new open standard, built with AWS, Cursor, GitHub, VS Code and Vercel, for packaging Skills + Connectors + MCP servers into one distributable format usable across compatible agent clients.
- [Humans missed 1 in 3 threats approving AI agent commands across 40,000 plays](https://scalex.dev/blog/ai-agent-permissions-stats/) — a browser game turned real dataset (409k decisions) showing data-exfiltration commands get missed 3x more often than obviously destructive ones; a sharp illustration of why manual human-in-the-loop approval is a weak last line of defense.
- [Cloudflare OS: an open platform for agents, apps, and work](https://blog.cloudflare.com/cloudflare-os/) — agents start with access to nothing, gaining typed capability bindings only on explicit grant; a concrete capability-security reference design for agent-execution infrastructure.
- [Prime Agent: A Self-Improving RLM Harness](https://www.primeintellect.ai/blog/prime-agent) — Prime Intellect's coding harness built around a named "Continual Harness" abstraction, arguing static hand-engineered scaffolding can't keep pace with what frontier models can already do.
- [Maple-Preview: a 20B-A1B ternary reasoning LLM at 218 tok/s on a Mac mini](https://deepgrove.ai/maple-preview) — DeepGrove's open ternary-weight ({−1,0,+1}) reasoning model (5.31 GB) that solves IMO-level problems on-device; the clearest demonstration yet that 1-bit-class quantization and real reasoning coexist.
- [Mixture-of-Kittens (MoK): a deterministic MoE training megakernel](https://github.com/cursor/mixture-of-kittens) — Cursor's open MoE-training megakernel for GB300 NVL72 racks, fusing all expert communication/computation into one deterministic kernel (up to 2.37× faster than public baselines).

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No earthquake today: Hacker News' front page was topped by non-AI stories (a 16-year-old SQLite bug, a software-engineering-jobs essay); the AI conversation centered on the same-day cluster of model releases below.
- A cluster of model releases broke within hours of each other: [Qwen3.8-Max](https://huggingface.co/Qwen/Qwen3.8-2.4T-A95B) weights, a [DeepSeek V4 Pro refresh](https://openrouter.ai/deepseek/deepseek-v4-pro-0813) (API-only so far), [xAI's Grok 4.6](https://x.ai/news/grok-4-6), and Microsoft's first from-scratch reasoning model (MAI-Thinking-1) — the digests dubbed it "Frontier Model Day."
- Unverified press reporting (via The Information) says NVIDIA is training a rumored ≥1-trillion-parameter open model, Nemotron 4 — watching for NVIDIA's own announcement before treating this as more than a rumor.
- YouTube curator channels (code4AI, bycloud, AI Explained) were not re-tested this run — still a confirmed repeat-failure pattern, deferred to the weekly re-test cadence.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~16)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-08-13](reports/2026-08-13.md) · weekly: [2026-W32](reports/weekly/2026-W32.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
