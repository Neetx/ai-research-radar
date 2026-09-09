# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-10-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-25-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--09-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-09):**

- **Stage move**: [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) reactivated dormant → accelerating on Meta's [Muse](https://ai.meta.com/muse/), a consumer agent built around a persistent dedicated-VM sandbox with approval-gated actions.
- **Landmark evidence**: [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) gained two contrasting primaries the same week — OpenAI's [~10,000-agent resolution](https://openai.com/index/navier-stokes-solution) of the Navier–Stokes Millennium Prize problem, and mathematician Tristan Buckmaster's own [candid account](https://cims.nyu.edu/~tristanb/statement.pdf) of a human-directed, multi-LLM-assisted proof of adjacent blowup results.
- **Evidence add**: [Small & 1-bit models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) gained a new lab — OpenBMB's [MiniCPM5-2B](https://huggingface.co/openbmb/MiniCPM5-2B) tops the sub-4B open leaderboard.
- **Watchlist**: +7 new signals, −8 cap-driven burndown drops (see the [watchlist](TRENDS.md#observation_queue)).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-06](https://huggingface.co/openbmb/MiniCPM5-2B) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.04098) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-01](https://arxiv.org/abs/2609.01343) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Trends

🌱 2 · 📈 4 · 🚀 10 · 🌊 4 · 🏔 0 · 📉 0 · 💤 1

| trend | stage | latest signal |
|---|---|---|
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-09](https://ai.meta.com/muse/) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-09](https://arxiv.org/abs/2609.03241) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-07](https://cohere.com/blog/agentic-task-ecosystem) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-06](https://huggingface.co/openbmb/MiniCPM5-2B) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.04098) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-04](https://arxiv.org/abs/2609.03796) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-02](https://arxiv.org/abs/2609.02886) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-08-26](https://github.com/vllm-project/vllm/releases/tag/v0.28.0) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-08-26](https://github.com/vllm-project/vllm/releases/tag/v0.28.0) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-08-24](https://arxiv.org/abs/2608.23283) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-09-03](https://developer.nvidia.com/blog/nvidia-pair-virtual-inference-router-expands-available-compute-on-your-local-network/) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-02](https://arxiv.org/abs/2609.02783) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-01](https://arxiv.org/abs/2609.01343) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-08-28](https://arxiv.org/abs/2608.21750) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-08-31](https://arxiv.org/abs/2608.31075) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-08-31](https://github.com/lightorigins/LightNav-0) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-09](https://ai.meta.com/muse/) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-08](https://openai.com/index/navier-stokes-solution) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-07](https://developer.nvidia.com/blog/building-a-memory-driven-agent-with-nvidia-nemoclaw/) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-03](https://ifm.ai/blog/k2/) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-08-13](https://arxiv.org/abs/2608.13317) |

## Worth studying

- [On the Navier–Stokes Millennium Prize Problem](https://openai.com/index/navier-stokes-solution) — OpenAI's own methodology writeup for how ~10,000 concurrently-coordinating agents resolved a forced-blowup instance of a 90-year-old open problem in ~88 hours — a rare, concrete disclosure of large-scale multi-agent research coordination mechanics.
- [Navier-Stokes statement](https://cims.nyu.edu/~tristanb/statement.pdf) — mathematician Tristan Buckmaster's candid account of resolving adjacent blowup problems with a colleague using Claude, Codex and GPT-6 Astra, including the honest admission that the writeups are "AI slop" — the human-directed counterpoint to OpenAI's autonomous-swarm approach the same week.
- [How well do agents use test/verification techniques?](https://danluu.com/agentic-testing/) — a 26-condition empirical comparison of testing/formal-methods techniques for coding agents, with pre-registered predictions checked against results — a rare rigorous, falsifiable answer to "which agent testing practice actually works."
- [Dr. Claw: An AI Scientist Workspace for Vibe Research](https://arxiv.org/abs/2609.00365) — an open-source workspace wrapping coding-agent executors in an auditable, recoverable human-in-the-loop research workflow, a concrete orchestration-layer pattern for long-running agent work.
- [Formalizing Fermat's Last Theorem](https://www.anthropic.com/news/formalizing-fermats-last-theorem) — dozens of Claude agents, coordinated via a DAG-based multi-agent harness, produced the first complete computer-checked Lean proof of FLT in 11 largely-autonomous days — the largest Lean proof ever constructed, independently verified by the human formalization project's own lead.
- [Research acceleration: The view inside OpenAI](https://openai.com/index/research-acceleration-view-inside-openai) — a rare, quantified look inside a frontier lab's own agent-usage metrics (3.1 agent-workdays per human workday), published as part of an explicit commitment to track RSI progress publicly.
- [funes](https://huggingface.co/blog/funes) — a concrete, inspectable answer to "what should agent memory actually be": local, cross-agent, built from session traces you already generate.
- [K2 Horizon](https://ifm.ai/blog/k2/) — a rare chance to study how a frontier-adjacent training run is actually built end to end, not just what it scores.
- [Gemini 3.8 Flash Cyber and the Fairwind Program](https://deepmind.google/blog/introducing-gemini-3-8-flash-and-38-flash-cyber/) — Google DeepMind's cybersecurity-tuned model paired with its CodeMender harness, launched via tiered early access to autonomously find, verify and fix vulnerabilities in minutes rather than weeks — the defensive-side mirror of OpenAI's Path to Astra.
- [SolarWM: Open Data and Scalable Training for Long-Horizon Video World Models](https://arxiv.org/abs/2609.02886) — a fully open, reproducible foundation for building interactive video world models end-to-end, solving the field's cross-dataset/cross-architecture reproducibility gap.
- [Path to Astra: critical capabilities and frontier safeguards](https://openai.com/index/path-to-astra/) — the most concrete public account yet of how a lab operationalizes a "critical" capability threshold: a 100% ExploitBench score, two genuine zero-days found and disclosed during evaluation, and a honeypot test comparing unauthorized-action rates with and without production safeguards.
- [Atlas](https://www.worldlabs.ai/blog/atlas) — World Labs' frontier world model natively grounds every input in 3D coordinates via a "multimodal autoregressive diffusion transformer," a genuinely different architectural bet on what a world model should represent.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- Double earthquake on Hacker News: Tristan Buckmaster's own [Navier-Stokes statement](https://cims.nyu.edu/~tristanb/statement.pdf) (#1) and [OpenAI's post](https://openai.com/index/navier-stokes-solution) (#2) both broke the front page the same day, alongside [Meta's Muse](https://ai.meta.com/muse/) agent launch (#5).
- A mathematician's Mastodon essay on AI "non-renewably mining" open math problems drew wide discussion (#9) — reflective commentary, not itself a trend signal.
- Independent-developer curiosities on the pulse: streaming a 2.8T model from four SSDs at 1 tok/s, and a third-party benchmark showing 1-bit quantization collapsing on Qwen3.8 27B where 4-bit holds up — both below-bar on the [watchlist](TRENDS.md#observation_queue).
- Broad Reddit pulse stays blocked (standing network-policy block); the Hacker News broad-pulse tier and curator/digest lane carry the load in its place.
- Tooling note: the GitHub external API remains scope-blocked for a 20th consecutive week.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~25)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-09](reports/2026-09-09.md) · weekly: [2026-W36](reports/weekly/2026-W36.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
