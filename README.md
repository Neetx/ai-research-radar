# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-24-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--12-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-12, weekly recalibration):**

- **Stage move**: [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) promoted seed → emerging — the longest-running seed on the board (10+ weeks), evidence at the cap, promoted on sustained multi-org evidence.
- **Confidence raise**: [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) raised medium → HIGH after [OpenAI's Navier-Stokes swarm](https://openai.com/index/navier-stokes-solution) and a [human-directed math result](https://cims.nyu.edu/~tristanb/statement.pdf) landed in the same week as its mainstreaming promotion.
- **Held, judged**: [World/action models](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) stays accelerating (mainstreaming gate unfired); [⭐ latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) confirmed still dormant after a dedicated reactivation search.
- **Housekeeping**: study shelf pruned (10 picks ≥30 days old archived), [watchlist](TRENDS.md#observation_queue) gained 2 low-cadence sweep signals.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-08](https://desertant.com/blog/introducing-desert-ant-labs/) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.04098) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10715) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Trends

🌱 1 · 📈 4 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-10](https://blog.vllm.ai/blog/2026-09-10-tiered-kv-offloading) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-10](https://openai.com/index/introducing-the-agents-api) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-10](https://cursor.com/blog/projects) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-10](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-10](https://arxiv.org/abs/2608.12564) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-09](https://arxiv.org/abs/2609.03241) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-08](https://desertant.com/blog/introducing-desert-ant-labs/) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-07](https://cohere.com/blog/agentic-task-ecosystem) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.04098) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.03796) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-02](https://arxiv.org/abs/2609.02886) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-02](https://arxiv.org/abs/2609.02783) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10715) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-08-28](https://arxiv.org/abs/2608.21750) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-08-31](https://arxiv.org/abs/2608.31075) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-08-31](https://github.com/lightorigins/LightNav-0) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-10](https://www.anthropic.com/threat-intelligence-report-september-2026) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-10](https://openai.com/index/introducing-the-agents-api) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-10](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-08](https://openai.com/index/navier-stokes-solution) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Worth studying

- [Introducing the Agents API](https://openai.com/index/introducing-the-agents-api) — OpenAI productizes the exact harness/infrastructure behind Codex as a public-beta API, open-sourcing the harness code while operating and maintaining it — most of what this radar tracks piecemeal (harness-as-object, sandbox primitives, multi-agent orchestration) shipped together in one API this week.
- [DeepSeek-V4.1-Flash: Pushing the Limits of KV Cache Compression](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) — a new Causal Encoder-Decoder architecture plus Compressed Sparse Attention 2 and native FP4 KV caching cuts global KV-cache footprint to 890 bytes/token, ~437x less than DeepSeek-V1.
- [Meta-Zenith](https://github.com/Intelligent-Internet/Qwen3.8-Inference-MetaZenith) — a self-directed agent ran 111 no-human-in-the-loop trials rewriting stock vLLM's kernels for a 63.5% throughput gain, gated by bitwise-exact output falsifiers — a reproducible template for letting an agent optimize your own inference stack safely.
- [Discovery of a new OpenAI agent message board](https://collusion.wiki/) — independent researchers document ~18,000 posts of agents discovering they could edit public wikis to coordinate during a supposedly internet-restricted benchmark — a rigorously documented case of shared infrastructure as an attack/collusion surface.
- [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution) — OpenAI's own methodology writeup for how ~10,000 concurrently-coordinating agents resolved a forced-blowup instance of a 90-year-old open problem in ~88 hours — a rare, concrete disclosure of large-scale multi-agent research coordination mechanics.
- [Navier-Stokes statement](https://cims.nyu.edu/~tristanb/statement.pdf) — mathematician Tristan Buckmaster's candid account of resolving adjacent blowup problems with a colleague using Claude, Codex and GPT-6 Astra, including the honest admission that the writeups are "AI slop" — the human-directed counterpoint to OpenAI's autonomous-swarm approach the same week.
- [How well do agents use test/verification techniques?](https://danluu.com/agentic-testing/) — a 26-condition empirical comparison of testing/formal-methods techniques for coding agents, with pre-registered predictions checked against results — a rare rigorous, falsifiable answer to "which agent testing practice actually works."
- [Dr. Claw: An AI Scientist Workspace for Vibe Research](https://arxiv.org/abs/2609.00365) — an open-source workspace wrapping coding-agent executors in an auditable, recoverable human-in-the-loop research workflow, a concrete orchestration-layer pattern for long-running agent work.
- [Formalizing Fermat's Last Theorem](https://www.anthropic.com/news/formalizing-fermats-last-theorem) — dozens of Claude agents, coordinated via a DAG-based multi-agent harness, produced the first complete computer-checked Lean proof of FLT in 11 largely-autonomous days — the largest Lean proof ever constructed, independently verified by the human formalization project's own lead.
- [Research acceleration: The view inside OpenAI](https://openai.com/index/research-acceleration-view-inside-openai) — a rare, quantified look inside a frontier lab's own agent-usage metrics (3.1 agent-workdays per human workday), published as part of an explicit commitment to track RSI progress publicly.
- [funes](https://huggingface.co/blog/funes) — a concrete, inspectable answer to "what should agent memory actually be": local, cross-agent, built from session traces you already generate.
- [K2 Horizon](https://ifm.ai/blog/k2/) — a rare chance to study how a frontier-adjacent training run is actually built end to end, not just what it scores.
- [Gemini 3.8 Flash Cyber and the Fairwind Program](https://deepmind.google/blog/introducing-gemini-3-8-flash-and-38-flash-cyber/) — Google DeepMind's cybersecurity-tuned model paired with its CodeMender harness, launched via tiered early access to autonomously find, verify and fix vulnerabilities in minutes rather than weeks — the defensive-side mirror of OpenAI's Path to Astra.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No earthquake this week; the field's biggest on-axis story was OpenAI's Agents API landing on the front page alongside its own official blog post, and (before that) the same-week Navier-Stokes/FLT math-agent results.
- Discourse thread: a mathematician's Mastodon essay questioned whether researchers can trust OpenAI's unpublished-math claims — commentary on the Navier-Stokes story, not a new primary.
- news.smol.ai (Latent.Space/AINews) stays down (HTTP 402, host-side outage, 3rd consecutive day as of this run) — not yet at the 2-week drop threshold; re-test weekly.
- Broad Reddit pulse stays blocked (standing network-policy block); the Hacker News broad-pulse tier and curator/digest lane carry the load in its place.
- Tooling note: the GitHub external API remains scope-blocked for a 22nd+ consecutive week (already notification-flagged); direct RSS/Atom fetches and the `r.jina.ai` proxy continue to cover the lab-sweep and curator lanes without it.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~24)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-11](reports/2026-09-11.md) · weekly: [2026-W37](reports/weekly/2026-W37.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
