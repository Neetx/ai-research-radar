# AI Radar

![trends](https://img.shields.io/badge/trends-21-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-11-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-27-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--09--29-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-09-29):**

- **New evidence, no gate fired**: NVIDIA's [Open Agent Safety Platform](https://nvidianews.nvidia.com/news/open-agent-safety-platform) — a hardware watchdog on dedicated BlueField-4 DPU silicon, out-of-band from the agent's own software — lands on [agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) with 100+ launch partners including Anthropic and Microsoft.
- **Cross-cutting finds**: [Disaggregated Quantization](https://arxiv.org/abs/2609.26333) specializes quantization format to prefill vs. decode, bridging [low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) with [PD disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture); [Skill2Env](https://arxiv.org/abs/2609.33772) extends [verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) to skill-derived construction.
- **Dormancy watch**: ⭐ [latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) (20d) crosses the 21-day line tomorrow if unrefreshed; [multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) (19d) is close behind — dedicated rescue searches found nothing new yet.
- **Housekeeping**: queue burndown continues (3 new below-bar items, 4 dropped, 1 resolved into trend evidence) — still working toward the ~25 soft cap.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-29](https://github.com/firelex/jeff) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |

## Trends

🌱 1 · 📈 5 · 🚀 11 · 🌊 4 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🌊 mainstreaming | [2026-09-28](https://nvidianews.nvidia.com/news/open-agent-safety-platform) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌊 mainstreaming | [2026-09-28](https://x.ai/news/team-bots) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.33772) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-09-28](https://arxiv.org/abs/2609.26333) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 📈 emerging | [2026-09-23](https://arxiv.org/abs/2609.26777) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 🚀 accelerating | [2026-09-22](https://blog.cloudflare.com/worker-previews/) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🌊 mainstreaming | [2026-09-22](https://arxiv.org/abs/2609.26457) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🚀 accelerating | [2026-09-22](https://arxiv.org/abs/2609.26708) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-09-21](https://blog.vllm.ai/blog/2026-09-21-qwen38-pd-serving) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-09-21](https://huggingface.co/XiaomiMiMo/MiMo-V2.6-Pro-RL) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-09-20](https://arxiv.org/abs/2609.23809) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 📈 emerging | [2026-09-20](https://arxiv.org/abs/2609.23808) |
| [World/action models (video)](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 🚀 accelerating | [2026-09-18](https://www.figure.ai/news/helix-2-5-zero-shot-30-home-generalization) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-09-17](https://arxiv.org/abs/2609.20751) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 📈 emerging | [2026-09-16](https://arxiv.org/abs/2609.18842) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 🚀 accelerating | [2026-09-29](https://github.com/firelex/jeff) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 🚀 accelerating | [2026-09-10](https://cursor.com/blog/projects) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-09-12](https://github.com/yifanzhang-pro/recurrent-looped-tranformer) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-09-09](https://arxiv.org/abs/2609.10266) |
| [VLM-scaffolded navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 seed | [2026-09-15](https://arxiv.org/abs/2609.16610) |

## Worth studying

- [NVIDIA Launches Open Agent Safety Platform](https://nvidianews.nvidia.com/news/open-agent-safety-platform) — OpenShell (an open-source runtime boundary) plus Sentry, a hardware watchdog on dedicated DPU silicon that can quarantine a rogue agent in milliseconds, entirely out-of-band from the agent's own software stack.
- [Holo4](https://huggingface.co/blog/Hcompany/holo4) — an open-weight generalist computer-use agent that clicks/types on a screen, writes and runs code, and calls MCP/API tools through one model across desktop, web, Android and code-sandbox targets.
- [How Cloudflare addressed a cross-tenant data exposure vulnerability in Containers](https://blog.cloudflare.com/containers-cross-tenant-vulnerability/) — a clear postmortem of a shared-storage-pool bug letting one tenant recover another's residual disk data, affecting both Containers and Sandboxes.
- [2026 in LLMs (so far)](https://simonwillison.net/2026/Sep/27/2026-in-llms-so-far/) — Simon Willison's annotated year-in-review keynote, a single practitioner-grounded recap of the whole year.
- [Introducing Contrastive Language Models (CLM)](https://huggingface.co/Contrastive-LM/CLM-v0.1-8B) — Stanford's Scaling Intelligence Lab ships an 8B "System One" model that scores agent actions via cheap contrastive vector search, matching the incumbent Jev's quality at up to 9x lower latency.
- [Codetta: High-Capacity, Keyless, and Undetectable Multi-Agent Collusion](https://arxiv.org/abs/2609.28900) — CMU researchers build a provably-undetectable steganographic protocol for independently-deployed agents to covertly collude, no pre-shared secret required.
- [CliffCompaction](https://arxiv.org/abs/2609.26779) — Tim Dettmers' lab ships a drop-in Claude Code/Codex CLI proxy that only truncates or drops prior context, never rewrites it, cutting long-horizon agent token cost up to 50%.
- [Agensh: Scaling Organizational Intelligence to 1,024 Agents](https://arxiv.org/abs/2609.26781) — a decentralized multi-agent harness with no central orchestrator, scaling from 1 to 1,024 concurrent workers, more than doubling pass rate on a hard coding task.
- [Transformers now runs llama.cpp quants](https://huggingface.co/blog/transformers-llama-cpp-quants) — Hugging Face adds native GGUF loading to `transformers` by reusing llama.cpp/ggml's own kernels, closing the gap between the ecosystem's two dominant local-inference paths.
- [A Faster Shortest Path Algorithm](https://www.vals.ai/blogs/faster-shortest-path-algorithm) — ten Claude Opus 5.5 agents coordinate over 15 hours to design and Lean-verify a genuine (if narrow) asymptotic algorithms improvement, honestly caveated.
- [dlab Open Source Week: Frontier AI on Your Own Hardware](https://timdettmers.com/2026/09/21/dlab-open-source-week/) — bitsandbytes/QLoRA creator Tim Dettmers' lab ships tooling running Qwen3.8-Flash-Next (125B) on a single 24GB consumer GPU and DeepSeek V4.1 (550B) on a 128GB Mac.
- [Packaged, But Not Portable](https://arxiv.org/abs/2609.23809) — a 68,072-plugin-bundle audit finds only 6.2% conform to the Agent Plugins standard, and argues conformance alone wouldn't guarantee portability anyway.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- YouTube's curator channels stay confirmed re-blocked (2nd consecutive 404); HF-daily-papers and HN overlap keep covering their typical picks — next re-test on the weekly cadence.
- Broad Reddit pulse was not attempted this run (standing egress-block precedent); the Hacker News broad-pulse tier carried the full community-pulse load, topped by Anthropic's Claude Sonnet 5.5 release.
- An independent open-source "Jev-compatible" small decision model ([Jeff](https://github.com/firelex/jeff)) recurred on Hacker News, resolving a below-bar queue item into trend evidence — two independent developers now converge on the same open recipe.
- Tooling note: the GitHub external API remains scope-blocked for a 39th+ consecutive week (already notification-flagged); the Tavily search API hit its plan usage limit again this run — the 2nd consecutive daily occurrence — web-search fallbacks covered the full run without it.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~27)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-09-29](reports/2026-09-29.md) · weekly: [2026-W39](reports/weekly/2026-W39.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
