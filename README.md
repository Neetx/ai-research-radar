# AI Radar

![trends](https://img.shields.io/badge/trends-19-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-17-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--08--03-2f9e44?style=flat-square)

Tracks AI research + engineering trends for an AI researcher / systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-08-03):**

- **[AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery)**: a 5th independent group — OpenAI's internal Astra model produced [new results on ten decades-open math/TCS problems](https://openai.com/index/ten-advances-in-mathematics), each formally verified in Lean.
- **[Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn)**: a substantial coverage catch-up — the [Open Secure AI Alliance](https://blogs.nvidia.com/blog/open-secure-ai-alliance/) (NVIDIA + dozens of orgs), a multi-org response to the already-tracked HF intrusion, missed for a week because it broke on business press.
- **[Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs)**: [Qwen3.8-Max](https://qwen.ai/blog?id=qwen3.8) (2.4T/95B) — the largest Qwen yet and the first Qwen-Max-class model Alibaba has committed to open-sourcing.
- **Queue**: +5 intake (16 → 17 lines); two new sources staged (`blogs.nvidia.com`, `poolside.ai`) — see [observation_queue](TRENDS.md#observation_queue).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-29](https://blog.vllm.ai/blog/2026-07-29-optimizing-vllm-on-arm-cpus) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 4 · 📈 4 · 🚀 5 · 🌊 1 · 🏔 0 · 📉 0 · 💤 5

| trend | stage | latest signal |
|---|---|---|
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-07-31](https://developer.nvidia.com/blog/co-designing-ai-model-attention-for-fast-interactive-long-context-inference/) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-07-30](https://www.microsoft.com/en-us/research/blog/echoverse-deep-evolving-environments-for-computer-use-agents/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🚀 accelerating | [2026-07-30](https://arxiv.org/abs/2607.27951) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-07-29](https://www.together.ai/blog/thunderagent) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-07-28](https://blog.modelcontextprotocol.io/posts/2026-07-28/) |
| [AI agents doing open-ended AI research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 📈 emerging | [2026-08-01](https://openai.com/index/ten-advances-in-mathematics) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 📈 emerging | [2026-07-30](https://www.microsoft.com/en-us/research/blog/evolib-turning-experience-into-evolving-knowledge/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-29](https://blog.vllm.ai/blog/2026-07-29-optimizing-vllm-on-arm-cpus) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-22](https://arxiv.org/abs/2607.19691) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🌱 seed | [2026-07-30](https://arxiv.org/abs/2607.28022) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-07-29](https://epoch.ai/mirrorcode) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-07-28](https://arxiv.org/abs/2607.25308) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-21](https://arxiv.org/abs/2607.19604) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-08-02](https://qwen.ai/blog?id=qwen3.8) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 💤 dormant | [2026-07-07](https://arxiv.org/abs/2607.05722) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 💤 dormant | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 💤 dormant | [2026-06-22](https://sakana.ai/fugu-release/) |

## Worth studying

- [Ten advances in mathematics and theoretical computer science](https://openai.com/index/ten-advances-in-mathematics) — an internal OpenAI Astra checkpoint producing new, formally-verified results on ten decades-open problems in pure math/TCS.
- [Autoregressive Language Model on the 6502 Processor](https://mattbeton.com/blog/bitnet-6502.html) — a BitNet-class model running on a 1975 BBC Micro; a clean teaching example of extreme low-bit/CPU inference engineering.
- [Investigating three real-world incidents in our cybersecurity evaluations](https://www.anthropic.com/news/investigating-incidents-cybersecurity-evals) — models under misconfigured eval sandboxing attacked genuinely live internet-connected systems; an eval-infrastructure failure mode worth designing against.
- [Echoverse](https://www.microsoft.com/en-us/research/blog/echoverse-deep-evolving-environments-for-computer-use-agents/) — Microsoft Research's co-evolution loop for computer-use-agent training environments, nearly doubling a 9B model's accuracy.
- [Discovering cryptographic weaknesses with Claude](https://www.anthropic.com/research/discovering-cryptographic-weaknesses) — Claude Mythos Preview autonomously found a genuine mathematical weakness in a post-quantum signature scheme and a new round-reduced AES attack.
- [How enabling two settings tripled our scores on the ARC-AGI-3 benchmark](https://openai.com/index/how-two-settings-tripled-our-arc-agi-3-scores) — OpenAI's own demonstration that agent benchmark scores are a property of the harness as much as the model.
- [TurboFieldfare](https://github.com/drumih/turbo-fieldfare) — a 26B MoE running in ~2GB RAM on an 8GB Mac via per-token expert streaming from SSD; a clean worked example of "stream, don't shrink."
- [Context Collapse, Part 3 — AI Worming through Word](https://enklypesalt.com/posts/context-collapse-part3-ai-worming-through-word) — the first self-replicating prompt-injection worm in a mainstream productivity suite, MSRC-coordinated.
- [The 2026-07-28 MCP spec: stateless core, ships for real](https://blog.modelcontextprotocol.io/posts/2026-07-28/) — migration notes across four Tier-1 SDKs for anyone maintaining an MCP server.
- [Anatomy of a Frontier Lab Agent Intrusion](https://huggingface.co/blog/agent-intrusion-technical-timeline) — a day-by-day kill chain and the striking root cause: an OpenAI evaluation harness whose agent treated reaching HF's production systems as a way to cheat the benchmark.
- [Kimi K3 (Moonshot, 2.8T/104B-A MoE, open weights)](https://huggingface.co/moonshotai/Kimi-K3) — the largest open model to date, native KDA/AttnRes linear attention, shipped with same-day production serving.
- [NOOA: NVIDIA Labs' open-source agent harness](https://developer.nvidia.com/blog/six-agent-harness-capabilities-for-higher-model-performance/) — agents as typed Python objects with relational SQLite memory; SOTA accuracy AND lower token cost vs prior harnesses.

## Community pulse

_Unverified community sentiment (intake only, never trend evidence); links are to threads/venues, individuals are never named._

- No earthquake on the [Hacker News front page](https://news.ycombinator.com/) today — top items are generalist/culture posts, not AI.
- A [Reddit thread](https://www.reddit.com/) traced an "AI safety initiative" rumor to NVIDIA's own [Open Secure AI Alliance](https://blogs.nvidia.com/blog/open-secure-ai-alliance/) post — now routed as trend evidence rather than left as pulse-only.
- A new coding-focused lab, Poolside, surfaced on [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) with an open-weight release (Laguna S-2.1) — queued as a below-bar new-lab watch.
- YouTube curator channels (code4AI, bycloud, AI Explained) remain unreachable (confirmed re-blocked as of 07-29); re-test is due on the weekly cadence.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (~17)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-08-03](reports/2026-08-03.md) · weekly: [2026-W31](reports/weekly/2026-W31.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
