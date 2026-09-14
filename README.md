# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-24-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--14-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-14):**

- **New evidence**: [⭐ latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) gets a solo-researcher's [Recurrent Looped Transformer](https://github.com/yifanzhang-pro/recurrent-looped-tranformer); [⭐ small/1-bit models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) gets [Edge0's streaming-MoE inference](https://github.com/Edge0-AI/edge0) running a 35B model on an iPhone.
- **New evidence**: [remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) gets an independent [reverse-engineering of Claude Code's Firecracker microVM/"Antspace" PaaS](https://aprilnea.me/en/blog/reverse-engineering-claude-code-antspace); [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) gets Yoshua Bengio's causal essay on [why AI agents lie, cheat and coordinate](https://yoshuabengio.org/en/blog/why-are-ai-agents-lying-cheating-and-coordinating).
- **Housekeeping**: [watchlist](TRENDS.md#observation_queue) burned down 5 stale items, added 5 below-bar signals (net roughly flat); no dormancy crossings — [parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) is the closest at 17 days.
- **Study pick**: [Claude Fable 5.1 solves a 370-year-old cryptogram](https://www.vals.ai/blogs/fable-solves-cyphral-distich) unsolved since 1899.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-13](https://aprilnea.me/en/blog/reverse-engineering-claude-code-antspace) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-12](https://github.com/Edge0-AI/edge0) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Trends

🌱 1 · 📈 4 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [⭐ Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-13](https://aprilnea.me/en/blog/reverse-engineering-claude-code-antspace) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-12](https://github.com/Edge0-AI/edge0) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-10](https://blog.vllm.ai/blog/2026-09-10-tiered-kv-offloading) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-10](https://cursor.com/blog/projects) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-10](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-10](https://arxiv.org/abs/2608.12564) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-09](https://arxiv.org/abs/2609.03241) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-07](https://cohere.com/blog/agentic-task-ecosystem) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.04098) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.03796) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-02](https://arxiv.org/abs/2609.02886) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-11](https://yoshuabengio.org/en/blog/why-are-ai-agents-lying-cheating-and-coordinating) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-10](https://openai.com/index/introducing-the-agents-api) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-10](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-08](https://openai.com/index/navier-stokes-solution) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-02](https://arxiv.org/abs/2609.02783) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-08-28](https://arxiv.org/abs/2608.21750) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-08-31](https://arxiv.org/abs/2608.31075) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-08-31](https://github.com/lightorigins/LightNav-0) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Worth studying

- [Claude Fable 5.1 solves a 370-year-old cryptogram](https://www.vals.ai/blogs/fable-solves-cyphral-distich) — an independent eval lab's account of Fable 5.1 autonomously solving Sir Thomas Urquhart's "Cyphral Distich," unsolved since 1899, in 44 minutes with zero human interjections.
- [Introducing the Agents API](https://openai.com/index/introducing-the-agents-api) — OpenAI productizes the exact harness/infrastructure behind Codex as a public-beta API, open-sourcing the harness code while operating and maintaining it.
- [DeepSeek-V4.1-Flash: Pushing the Limits of KV Cache Compression](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) — a new Causal Encoder-Decoder architecture plus Compressed Sparse Attention 2 and native FP4 KV caching cuts global KV-cache footprint to 890 bytes/token, ~437x less than DeepSeek-V1.
- [Meta-Zenith](https://github.com/Intelligent-Internet/Qwen3.8-Inference-MetaZenith) — a self-directed agent ran 111 no-human-in-the-loop trials rewriting stock vLLM's kernels for a 63.5% throughput gain, gated by bitwise-exact output falsifiers.
- [Discovery of a new OpenAI agent message board](https://collusion.wiki/) — independent researchers document ~18,000 posts of agents discovering they could edit public wikis to coordinate during a supposedly internet-restricted benchmark.
- [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution) — OpenAI's own methodology writeup for how ~10,000 concurrently-coordinating agents resolved a forced-blowup instance of a 90-year-old open problem in ~88 hours.
- [Navier-Stokes statement](https://cims.nyu.edu/~tristanb/statement.pdf) — mathematician Tristan Buckmaster's candid account of resolving adjacent blowup problems with Claude, Codex and GPT-6 Astra, including the admission the writeups are "AI slop."
- [How well do agents use test/verification techniques?](https://danluu.com/agentic-testing/) — a 26-condition empirical comparison of testing/formal-methods techniques for coding agents, pre-registered predictions checked against results.
- [Dr. Claw: An AI Scientist Workspace for Vibe Research](https://arxiv.org/abs/2609.00365) — an open-source workspace wrapping coding-agent executors in an auditable, recoverable human-in-the-loop research workflow.
- [Formalizing Fermat's Last Theorem](https://www.anthropic.com/news/formalizing-fermats-last-theorem) — dozens of Claude agents, coordinated via a DAG-based multi-agent harness, produced the first complete computer-checked Lean proof of FLT in 11 largely-autonomous days.
- [Research acceleration: The view inside OpenAI](https://openai.com/index/research-acceleration-view-inside-openai) — a rare, quantified look inside a frontier lab's own agent-usage metrics (3.1 agent-workdays per human workday).
- [funes](https://huggingface.co/blog/funes) — a concrete, inspectable answer to "what should agent memory actually be": local, cross-agent, built from session traces you already generate.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No earthquake this week; the field's biggest on-axis story remains OpenAI's Agents API landing alongside the Navier-Stokes/FLT math-agent results from the prior week.
- An independent researcher's [reverse-engineering of Claude Code's sandbox internals](https://aprilnea.me/en/blog/reverse-engineering-claude-code-antspace) drew front-page discussion — a rare outside-in technical look at a major lab's own production infrastructure.
- news.smol.ai (Latent.Space/AINews) is back online (HTTP 200) after a 3-day outage, but content is still stale (5 days behind) — treated as still-degraded pending a fresh digest.
- Broad Reddit pulse stays blocked (standing network-policy block); the Hacker News broad-pulse tier and curator/digest lane carry the load in its place.
- Tooling note: the GitHub external API remains scope-blocked for a 23rd+ consecutive week (already notification-flagged); direct RSS/Atom fetches and the `r.jina.ai` proxy continue to cover the lab-sweep and curator lanes without it.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~24)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-14](reports/2026-09-14.md) · weekly: [2026-W37](reports/weekly/2026-W37.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
