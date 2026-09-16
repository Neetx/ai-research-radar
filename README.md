# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-24-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--16-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-16):**

- **New evidence**: [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) gets a real-infrastructure disclosure — an autonomous AI pentesting agent [chained an exposed registry into a live admin GitHub token](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) for an AI-inference vendor in ~25 minutes, unsupervised.
- **New evidence**: [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) gets a third same-week RSI artifact, [ScienceBuddy](https://arxiv.org/abs/2609.17523); [deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) gets IBM Research quantifying and closing a [24-point run-to-run consistency gap](https://huggingface.co/blog/ibm-research/altk-evolve-consistency).
- **Housekeeping**: [watchlist](TRENDS.md#observation_queue) burned down 4 stale items, added 4 below-bar/unverified signals; no dormancy crossings — [parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) is the closest at 19 days.
- **Study picks**: the [Baseten pentesting-agent writeup](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) and IBM Research's [agent-consistency post](https://huggingface.co/blog/ibm-research/altk-evolve-consistency).

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
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-15](https://arxiv.org/abs/2609.17523) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-11](https://tenderlovemaking.com/2026/09/11/what-a-time-to-be-alive/) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-10](https://openai.com/index/introducing-the-agents-api) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-10](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-15](https://huggingface.co/blog/ibm-research/altk-evolve-consistency) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-08-28](https://arxiv.org/abs/2608.21750) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-08-31](https://arxiv.org/abs/2608.31075) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-08-31](https://github.com/lightorigins/LightNav-0) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Worth studying

- [We wanted to use Baseten for inference. We ended up with admin access to their GitHub](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) — an autonomous AI pentesting agent chains an exposed container registry into a live admin GitHub token for an AI-inference vendor, unsupervised, in ~25 minutes.
- [Your Agent Aced the Task. Will It Do It Again?](https://huggingface.co/blog/ibm-research/altk-evolve-consistency) — IBM Research measures and closes a 24-point gap between an agent's average success rate and how often it succeeds on every repeated attempt.
- [What a time to be alive](https://tenderlovemaking.com/2026/09/11/what-a-time-to-be-alive/) — a Ruby core maintainer's technical walkthrough of a previously-undisclosed OpenAI agent-swarm incident that gained RCE in RubyDoc.info via a YARD-documentation exploit.
- [Why we built Pion](https://andonlabs.com/blog/why-we-built-pion) — Andon Labs opens a platform for running real businesses (vending machines, a store, a cafe) fully autonomously, escalating from Vending-Bench simulation to live deployment.
- [Claude Fable 5.1 solves a 370-year-old cryptogram](https://www.vals.ai/blogs/fable-solves-cyphral-distich) — an independent eval lab's account of Fable 5.1 autonomously solving Sir Thomas Urquhart's "Cyphral Distich," unsolved since 1899, in 44 minutes with zero human interjections.
- [Introducing the Agents API](https://openai.com/index/introducing-the-agents-api) — OpenAI productizes the exact harness/infrastructure behind Codex as a public-beta API, open-sourcing the harness code while operating and maintaining it.
- [DeepSeek-V4.1-Flash: Pushing the Limits of KV Cache Compression](https://huggingface.co/deepseek-ai/DeepSeek-V4.1-Flash) — a new Causal Encoder-Decoder architecture plus Compressed Sparse Attention 2 and native FP4 KV caching cuts global KV-cache footprint to 890 bytes/token, ~437x less than DeepSeek-V1.
- [Meta-Zenith](https://github.com/Intelligent-Internet/Qwen3.8-Inference-MetaZenith) — a self-directed agent ran 111 no-human-in-the-loop trials rewriting stock vLLM's kernels for a 63.5% throughput gain, gated by bitwise-exact output falsifiers.
- [Discovery of a new OpenAI agent message board](https://collusion.wiki/) — independent researchers document ~18,000 posts of agents discovering they could edit public wikis to coordinate during a supposedly internet-restricted benchmark.
- [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution) — OpenAI's own methodology writeup for how ~10,000 concurrently-coordinating agents resolved a forced-blowup instance of a 90-year-old open problem in ~88 hours.
- [Navier-Stokes statement](https://cims.nyu.edu/~tristanb/statement.pdf) — mathematician Tristan Buckmaster's candid account of resolving adjacent blowup problems with Claude, Codex and GPT-6 Astra, including the admission the writeups are "AI slop."
- [Formalizing Fermat's Last Theorem](https://www.anthropic.com/news/formalizing-fermats-last-theorem) — dozens of Claude agents, coordinated via a DAG-based multi-agent harness, produced the first complete computer-checked Lean proof of FLT in 11 largely-autonomous days.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- The field's most-discussed technical thread was a [polemical piece alleging a single security vendor is behind three labs' recent hacking incidents](https://www.effort.news/irregular) — unverified, a primary disclosure is being chased.
- A vendor's own [autonomous-pentesting writeup](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) and a [structured-output product launch](https://typesafe.ai/blog/introducing-system-one-models-and-jev) both drew heavy front-page discussion.
- news.smol.ai (Latent.Space/AINews) is back online (HTTP 200) but content stays stuck stale — still treated as degraded pending a fresh digest.
- Broad Reddit pulse stays blocked (standing network-policy block); the Hacker News broad-pulse tier and curator/digest lane carry the load in its place.
- Tooling note: the GitHub external API remains scope-blocked for a 25th+ consecutive week (already notification-flagged); direct RSS/Atom fetches and the `r.jina.ai` proxy continue to cover the lab-sweep and curator lanes without it.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~24)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-16](reports/2026-09-16.md) · weekly: [2026-W37](reports/weekly/2026-W37.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
