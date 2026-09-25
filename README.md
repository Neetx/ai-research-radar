# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-26-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--25-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-25):**

- **New architectural primitive**: Stanford's [CLM-8B](https://huggingface.co/Contrastive-LM/CLM-v0.1-8B) scores agent actions via cheap contrastive vector search instead of a full LLM call, landing on [agent harness/runtime infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object); CMU's [Codetta](https://arxiv.org/abs/2609.28900) demonstrates a provably-undetectable multi-agent collusion channel, landing on [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn).
- **Capture-leak backfill**: Google Research's 260-configuration scaling study, ["Towards a Science of Scaling Agent Systems"](https://research.google/blog/towards-a-science-of-scaling-agent-systems-when-and-why-agent-systems-work/) (published 2026-01-28, only found today via a pulse pointer), lands on [multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a).
- **⭐ Small/CPU models**: two adds — Edge0's [Audio8 ASR Infinite](https://huggingface.co/Edge0/Audio8-ASR-Infinite) (2nd artifact, promotion-flagged) and Liquid AI's [LFM2.5-VL-DSpark](https://huggingface.co/blog/LiquidAI/lfm2-5-vl-dspark).
- **Queue**: +9 new below-bar items (a vLLM watermarking artifact, an agent-name-collision attack, a new-architecture memory paper, a world-models pair) − 5 stale drops; sits just over the ~25 soft cap, burndown flagged for next run.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-24](https://huggingface.co/blog/LiquidAI/lfm2-5-vl-dspark) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-14](https://arxiv.org/abs/2609.16338) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Trends

🌱 1 · 📈 5 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-22](https://blog.cloudflare.com/worker-previews/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-24](https://huggingface.co/blog/LiquidAI/lfm2-5-vl-dspark) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-22](https://arxiv.org/abs/2609.26708) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-21](https://blog.vllm.ai/blog/2026-09-21-qwen38-pd-serving) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-20](https://arxiv.org/abs/2609.23809) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-18](https://arxiv.org/abs/2609.22068) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-18](https://www.figure.ai/news/helix-2-5-zero-shot-30-home-generalization) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-17](https://arxiv.org/abs/2609.20751) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-14](https://arxiv.org/abs/2609.16338) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-10](https://cursor.com/blog/projects) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-24](https://huggingface.co/Contrastive-LM/CLM-v0.1-8B) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-24](https://arxiv.org/abs/2609.28900) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-23](https://arxiv.org/abs/2609.26777) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-22](https://arxiv.org/abs/2609.26457) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-09-20](https://arxiv.org/abs/2609.23808) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-09-16](https://arxiv.org/abs/2609.18842) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-09-15](https://arxiv.org/abs/2609.16610) |

## Worth studying

- [Introducing Contrastive Language Models (CLM)](https://huggingface.co/Contrastive-LM/CLM-v0.1-8B) — Stanford's Scaling Intelligence Lab ships an 8B "System One" model that scores agent actions via cheap contrastive vector search, matching the incumbent Jev's quality at up to 9x lower latency.
- [Codetta: High-Capacity, Keyless, and Undetectable Multi-Agent Collusion](https://arxiv.org/abs/2609.28900) — CMU researchers build a provably-undetectable steganographic protocol for independently-deployed agents to covertly collude, no pre-shared secret required.
- [CliffCompaction](https://arxiv.org/abs/2609.26779) — Tim Dettmers' lab ships a drop-in Claude Code/Codex CLI proxy that only truncates or drops prior context, never rewrites it, cutting long-horizon agent token cost up to 50%.
- [Agensh: Scaling Organizational Intelligence to 1,024 Agents](https://arxiv.org/abs/2609.26781) — a decentralized multi-agent harness with no central orchestrator, scaling from 1 to 1,024 concurrent workers, more than doubling pass rate on a hard coding task.
- [Transformers now runs llama.cpp quants](https://huggingface.co/blog/transformers-llama-cpp-quants) — Hugging Face adds native GGUF loading to `transformers` by reusing llama.cpp/ggml's own kernels, closing the gap between the ecosystem's two dominant local-inference paths.
- [A Faster Shortest Path Algorithm](https://www.vals.ai/blogs/faster-shortest-path-algorithm) — ten Claude Opus 5.5 agents coordinate over 15 hours to design and Lean-verify a genuine (if narrow) asymptotic algorithms improvement, honestly caveated.
- [dlab Open Source Week: Frontier AI on Your Own Hardware](https://timdettmers.com/2026/09/21/dlab-open-source-week/) — bitsandbytes/QLoRA creator Tim Dettmers' lab ships tooling running Qwen3.8-Flash-Next (125B) on a single 24GB consumer GPU and DeepSeek V4.1 (550B) on a 128GB Mac.
- [Packaged, But Not Portable](https://arxiv.org/abs/2609.23809) — a 68,072-plugin-bundle audit finds only 6.2% conform to the Agent Plugins standard, and argues conformance alone wouldn't guarantee portability anyway.
- [Same Name, Different Server](https://arxiv.org/abs/2609.14119) — a full-registry census of 21,643 MCP servers finds 51% of multi-version servers silently change what they advertise, correlating with 3x higher odds of a serious security finding.
- [Agent Substrate / AX](https://github.com/agent-substrate/substrate) — a Google-affiliated open-source runtime claiming 10x sandbox density and sub-500ms resume for running millions of agent workloads.
- [When AI builds itself](https://www.anthropic.com/institute/recursive-self-improvement) — Anthropic's own quantified disclosure that Claude now leads 26% of its internal AI R&D, up from under 1% a year ago, with ~30,000 concurrent research/engineering agents.
- [Hacking OpenAI](https://www.hacktron.ai/blog/hacking-openai) — a heap overflow + SSO misconfiguration chain reaching internal OpenAI GitHub repos, the exploit built almost entirely by autonomous Claude Opus agents in a goal loop.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- A marketing/explainer post on distributed-systems framing for agent swarms pointed back to a genuinely significant, previously-uncaptured Google Research primary on multi-agent scaling — an indirect-pointer capture-leak, now closed.
- The Australian government Medicare-portal OpenAI agent breach (flagged in yesterday's pulse) still has no OpenAI primary report as of this session — stays unverified in the queue.
- YouTube's curator channels (code4AI, bycloud, AI Explained) 404'd again on re-test — the intermittent block/lift pattern continues; HF-daily-papers and HN overlap keep covering their typical picks.
- Broad Reddit pulse stayed unreachable this run (Tavily plan-limited, direct JSON still returns a login-wall page); the Hacker News broad-pulse tier carried the full community-pulse load today.
- Tooling note: the GitHub external API remains scope-blocked for a 36th+ consecutive week (already notification-flagged); web-search fallbacks continue to cover the lab-sweep and curator lanes without it.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~26)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-25](reports/2026-09-25.md) · weekly: [2026-W38](reports/weekly/2026-W38.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
