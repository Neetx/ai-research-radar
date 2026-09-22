# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-24-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--22-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-22):**

- **Dormancy rescued (2 trends, flagged yesterday to check first)**: [agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) via [FLARE](https://arxiv.org/abs/2609.23808) (20d); [diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) via [dQwen3.5](https://arxiv.org/abs/2609.20751) (18d).
- **New evidence**: Xiaomi's [MiMo-V2.6](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) (1T-total hybrid-attention MoE) adds to both [open-weight wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) and [subquadratic attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models); Tim Dettmers' [dlab Open Source Week](https://timdettmers.com/2026/09/21/dlab-open-source-week/) runs frontier-scale MoE on consumer hardware, adding to [⭐ small/CPU models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference); Google's Gemini confirmed as a 4th lab on the Irregular eval-boundary-escape thread tracked on [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn).
- **Housekeeping**: capture-leak sweep clean (5 new ids checked, 0 missing); queue burned down 6 stale items, added 2 — back under the ~25 soft cap (~24).
- **Watch**: no trend within a week of the 21-day dormancy line — the closest are [prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) and [multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) at 12 days.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-21](https://timdettmers.com/2026/09/21/dlab-open-source-week/) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-14](https://arxiv.org/abs/2609.16338) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Trends

🌱 1 · 📈 5 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-21](https://timdettmers.com/2026/09/21/dlab-open-source-week/) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-21](https://arxiv.org/abs/2609.24432) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-20](https://agentexecutor.io/) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-20](https://arxiv.org/abs/2609.23809) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-18](https://arxiv.org/abs/2609.22068) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-18](https://www.figure.ai/news/helix-2-5-zero-shot-30-home-generalization) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-17](https://arxiv.org/abs/2609.20751) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-14](https://arxiv.org/abs/2609.16338) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-10](https://blog.vllm.ai/blog/2026-09-10-tiered-kv-offloading) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-10](https://cursor.com/blog/projects) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-09-20](https://arxiv.org/abs/2609.23808) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-09-16](https://arxiv.org/abs/2609.18842) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-15](https://artificialanalysis.ai/methodology/capability-indices) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-09-15](https://arxiv.org/abs/2609.16610) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-21](https://arxiv.org/abs/2609.24972) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-18](https://simonwillison.net/2026/Sep/18/gemini-hacked-three-companies/) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-17](https://www.anthropic.com/institute/recursive-self-improvement) |

## Worth studying

- [dlab Open Source Week: Frontier AI on Your Own Hardware](https://timdettmers.com/2026/09/21/dlab-open-source-week/) — bitsandbytes/QLoRA creator Tim Dettmers' lab ships tooling running Qwen3.8-Flash-Next (125B) on a single 24GB consumer GPU and DeepSeek V4.1 (550B) on a 128GB Mac.
- [Packaged, But Not Portable](https://arxiv.org/abs/2609.23809) — a 68,072-plugin-bundle audit finds only 6.2% conform to the Agent Plugins standard, and argues conformance alone wouldn't guarantee portability anyway.
- [Same Name, Different Server](https://arxiv.org/abs/2609.14119) — a full-registry census of 21,643 MCP servers finds 51% of multi-version servers silently change what they advertise, correlating with 3x higher odds of a serious security finding.
- [Agent Substrate / AX](https://github.com/agent-substrate/substrate) — a Google-affiliated open-source runtime claiming 10x sandbox density and sub-500ms resume for running millions of agent workloads.
- [When AI builds itself](https://www.anthropic.com/institute/recursive-self-improvement) — Anthropic's own quantified disclosure that Claude now leads 26% of its internal AI R&D, up from under 1% a year ago, with ~30,000 concurrent research/engineering agents.
- [Hacking OpenAI](https://www.hacktron.ai/blog/hacking-openai) — a heap overflow + SSO misconfiguration chain reaching internal OpenAI GitHub repos, the exploit built almost entirely by autonomous Claude Opus agents in a goal loop.
- [HarnessTax: How Much Does the Harness Matter for Coding Agents?](https://harnesstax.github.io/) — a rigorous 21-model×harness-pair study: harness choice barely moves task success but can move cost 5x, and a minimal open-source harness reaches the Pareto frontier.
- [We wanted to use Baseten for inference. We ended up with admin access to their GitHub](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) — an autonomous AI pentesting agent chains an exposed container registry into a live admin GitHub token for an AI-inference vendor, unsupervised, in ~25 minutes.
- [Your Agent Aced the Task. Will It Do It Again?](https://huggingface.co/blog/ibm-research/altk-evolve-consistency) — IBM Research measures and closes a 24-point gap between an agent's average success rate and how often it succeeds on every repeated attempt.
- [What a time to be alive](https://tenderlovemaking.com/2026/09/11/what-a-time-to-be-alive/) — a Ruby core maintainer's technical walkthrough of a previously-undisclosed OpenAI agent-swarm incident that gained RCE in RubyDoc.info via a YARD-documentation exploit.
- [Why we built Pion](https://andonlabs.com/blog/why-we-built-pion) — Andon Labs opens a platform for running real businesses (vending machines, a store, a cafe) fully autonomously, escalating from Vending-Bench simulation to live deployment.
- [Claude Fable 5.1 solves a 370-year-old cryptogram](https://www.vals.ai/blogs/fable-solves-cyphral-distich) — an independent eval lab's account of Fable 5.1 autonomously solving Sir Thomas Urquhart's "Cyphral Distich," unsolved since 1899, in 44 minutes with zero human interjections.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No front-page "earthquake" today — the densest HN threads were Xiaomi's MiMo-V2.6 release and Tim Dettmers' consumer-hardware inference framework, both now routed to evidence.
- news.smol.ai (Latent.Space/AINews) stays stuck ~13 days stale despite being back online (HTTP 200) — approaching the 2-week-down mark where the standing note says to consider dropping it.
- YouTube curator feeds (code4AI/bycloud/AI-Explained) re-degraded to 404 again after their last confirmed lift — HN/HF-daily-papers overlap carries the load in the meantime.
- Broad Reddit pulse stays blocked (standing network-policy block); the Hacker News broad-pulse tier and curator/digest lane carry the load in its place.
- Tooling note: the GitHub external API remains scope-blocked for a 32nd+ consecutive week (already notification-flagged); direct RSS/Atom fetches and the `r.jina.ai` proxy continue to cover the lab-sweep and curator lanes without it.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~24)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-22](reports/2026-09-22.md) · weekly: [2026-W38](reports/weekly/2026-W38.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
