# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-24-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--23-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-23):**

- **New evidence across 9 trends** from a dense cs.AI exploration batch + tier-i sweep: [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) gets [A2M](https://arxiv.org/abs/2609.26761), a 93.6%-success MCP-agent-hijacking attack; [agent harness/runtime](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) gets ["Growing Harness"](https://arxiv.org/abs/2609.26760); Hugging Face ships [native GGUF support in transformers](https://huggingface.co/blog/transformers-llama-cpp-quants), adding to [⭐ small/CPU models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference).
- **Three independent instances of AI-driven open-ended discovery land the same day** on [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery): [Vals AI's Lean-verified shortest-path algorithm](https://www.vals.ai/blogs/faster-shortest-path-algorithm), [AIDE²'s self-improving research agent](https://arxiv.org/abs/2609.26457), and GPT-6 Astra's autonomous break of a WWII Enigma message unsolved since 2005.
- **Queue resolution**: Epoch AI's full "Benchmark Reviews" documentation, unverified for citation since 09-18, is confirmed and promoted to [deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) evidence.
- **Watch**: news.smol.ai now 14 days stale, one day short of the standing drop-consideration mark; no trend within a week of the 21-day dormancy line.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-22](https://huggingface.co/blog/transformers-llama-cpp-quants) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-14](https://arxiv.org/abs/2609.16338) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Trends

🌱 1 · 📈 5 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-22](https://blog.cloudflare.com/worker-previews/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-22](https://huggingface.co/blog/transformers-llama-cpp-quants) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-22](https://arxiv.org/abs/2609.26708) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-21](https://blog.vllm.ai/blog/2026-09-21-qwen38-pd-serving) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-20](https://arxiv.org/abs/2609.23809) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-18](https://arxiv.org/abs/2609.22068) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-18](https://www.figure.ai/news/helix-2-5-zero-shot-30-home-generalization) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-17](https://arxiv.org/abs/2609.20751) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-14](https://arxiv.org/abs/2609.16338) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-10](https://cursor.com/blog/projects) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-21](https://developer.nvidia.com/blog/how-to-evaluate-ai-agents-from-tool-calls-to-task-completion/) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-09-20](https://arxiv.org/abs/2609.23808) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-09-16](https://arxiv.org/abs/2609.18842) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-09-15](https://arxiv.org/abs/2609.16610) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-22](https://arxiv.org/abs/2609.26761) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-22](https://arxiv.org/abs/2609.26760) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-22](https://arxiv.org/abs/2609.26457) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |

## Worth studying

- [Transformers now runs llama.cpp quants](https://huggingface.co/blog/transformers-llama-cpp-quants) — Hugging Face adds native GGUF loading to `transformers` by reusing llama.cpp/ggml's own kernels, closing the gap between the ecosystem's two dominant local-inference paths.
- [A Faster Shortest Path Algorithm](https://www.vals.ai/blogs/faster-shortest-path-algorithm) — ten Claude Opus 5.5 agents coordinate over 15 hours to design and Lean-verify a genuine (if narrow) asymptotic algorithms improvement, honestly caveated.
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

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- Today's biggest HN threads were proprietary flagship model launches (Claude Opus 5.5, GPT-6 Sol/Luna) — neither has an open-weight or research-axis fit, so neither is routed as evidence.
- news.smol.ai (Latent.Space/AINews) stays stuck 14 days stale despite being back online (HTTP 200) — one day short of the standing 2-week-down drop-consideration mark.
- YouTube curator feeds (code4AI/bycloud/AI-Explained) re-degraded to blocked/empty again after their last confirmed lift — HN/HF-daily-papers overlap carries the load in the meantime.
- Broad Reddit pulse stays blocked (standing network-policy block); the Hacker News broad-pulse tier and curator/digest lane carry the load in its place.
- Tooling note: the GitHub external API remains scope-blocked for a 33rd+ consecutive week (already notification-flagged); direct RSS/Atom fetches and web-search fallbacks continue to cover the lab-sweep and curator lanes without it.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~24)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-23](reports/2026-09-23.md) · weekly: [2026-W38](reports/weekly/2026-W38.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
