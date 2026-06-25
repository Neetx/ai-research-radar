# AI Radar

![trends](https://img.shields.io/badge/trends-14-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-5-e8590c?style=flat-square) ![pinned](https://img.shields.io/badge/pinned-4-7048e8?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-39-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--25-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-25):**
- **Stage move — [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) 🌱 seed → 📈 emerging:** the "third independent open diffusion BASE model" gate fired — [iLLaDA](https://arxiv.org/abs/2606.25331) (open weights [GSAI-ML/iLLaDA-8B-Base](https://huggingface.co/GSAI-ML/iLLaDA-8B-Base), Apache-2.0, 8B masked diffusion from scratch on 12T tokens) by RUC's LLaDA group joins Google DiffusionGemma + Tohoku Sumi; its own card ties autoregressive Qwen2.5-7B on average. Paper + HF card opened/verified this run.
- **New evidence — [Low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache):** added [Block-GTQ](https://arxiv.org/abs/2606.24033), a RoPE-aware KV-cache bit allocator built directly on TurboQuant-MSE — the first new evidence since 06-12, relieving the W25 demotion-risk flag (`last_evidence` 06-12 → 06-23; stays accelerating).
- **Watchlist 36 → 39** (4 captures: agent-native memory study [2606.24775](https://arxiv.org/abs/2606.24775) (W26 agent-memory-infra cluster), over-privileged tool selection [ToolPrivBench](https://arxiv.org/abs/2606.20023), Google ["Thinking to Recall"](https://research.google/blog/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms/); 2 stale 06-16/06-19 drops). No new trend.
- **Standing serving-engine gates still unfired** for [open-weight](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) / [subquadratic attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) / low-bit quant: vLLM bumped to v0.24.0rc1 but the rc notes document no native MiniMax-M3 / GLM-5.2 kernels or benchmarked `turboquant` release. YouTube curator feed IP-blocked (3rd run) — HN/Reddit net covered the earthquake check.

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |

## Trends

🌱 2 · 📈 7 · 🚀 5 · 🌊 0 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🚀 accelerating | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 📈 emerging | [2026-06-24](https://arxiv.org/abs/2606.25331) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-22](https://sakana.ai/fugu-release/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18208) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-11](https://e2b.dev/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-11](https://github.com/ggml-org/llama.cpp) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-06-23](https://arxiv.org/abs/2606.24530) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🌱 seed | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |

## Worth studying

- [iLLaDA-8B (Improved Large Language Diffusion Models)](https://huggingface.co/GSAI-ML/iLLaDA-8B-Base) — RUC/GSAI-ML's open-weights (Apache-2.0, paper 2606.25331) 8B fully-bidirectional masked-diffusion LM trained from scratch on 12T tokens: the clearest current "diffusion LM at autoregressive quality" datapoint — its own base-model card beats LLaDA-8B (avg 63.9 vs 51.1) and Dream-7B (61.4) and ties autoregressive Qwen2.5-7B (63.3); the third independent open diffusion base model that just moved diffusion-lm-013 to emerging
- [Thinking to Recall: How Reasoning Unlocks Parametric Knowledge in LLMs](https://research.google/blog/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms/) — Google Research: why a reasoning trace helps an LLM recall even *simple* single-hop facts that need no arithmetic — a *computational buffer* (reasoning tokens as latent computation) and *factual priming* — so reasoning expands the parametric-knowledge boundary; the practical hook is process rewards on factually-supported steps to cut hallucination
- [Qwen-AgentWorld (35B-A3B language world model)](https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B) — Alibaba/Qwen's open-weights (paper 2606.24597) "native language world model": a 35B-A3B MoE where *predicting the next environment state* from an agent's action+history IS the objective from CPT onward; a runnable bridge between world models and agent infrastructure — a learned *simulator of agentic environments*
- [Prompt Injection as Role Confusion](https://arxiv.org/abs/2603.12277) — Ye/Cui/Hadfield-Menell (MIT, ICML 2026): the cleanest mechanistic *theory* of why prompt injection works — LLMs infer who is speaking from how a span *sounds*, not its labeled `<user>`/`<tool>` role; study it (with role-confusion.github.io) for "role probes", why label-based defenses are brittle, and as the underpinning of the architectural/least-privilege turn
- [Sakana Fugu: A Multi-Agent Orchestration System as a Foundation Model](https://sakana.ai/fugu-release/) — Sakana AI's product: a small LM TRAINED to orchestrate a pool of frontier LLMs (choosing/switching models, recursive self-calls for test-time scaling) behind one API; the clearest example of "orchestration-as-a-model" vs orchestration-as-a-framework. Benchmarks are vendor-claimed.
- [Looped World Models (LoopWM)](https://arxiv.org/abs/2606.18208) — the first looped-transformer architecture for *world modelling*: a parameter-shared block iteratively refines the latent environment state with adaptive compute (~100× parameter efficiency, less long-horizon drift); the looped/recursive-computation idea crossing into world simulation
- [DiffusionGemma (26B-A4B discrete-diffusion MoE)](https://huggingface.co/google/diffusiongemma-26B-A4B-it) — Google DeepMind's open-weights (Apache-2.0) discrete-diffusion LM: an encoder-decoder Gemma-4 MoE that denoises whole blocks of tokens ("canvases") instead of decoding left-to-right for ~4× faster generation; pair with Sumi + iLLaDA for the diffusion-lm-013 line
- [Beyond Static Leaderboards: Predictive Validity for the Evaluation of LLM Agents](https://arxiv.org/abs/2606.19704) — a 61-author coordinated deep-dive (fourteen parallel studies of one MCP-based industrial-agent benchmark) showing no single benchmark covers more than 4–5 of the dimensions real deployment exposes; the case for *predictive validity* over static scores — read before trusting any agent leaderboard
- [Securing the future of AI agents (DeepMind AI Control Roadmap + "Three Layers of Agentic Security")](https://deepmind.google/blog/securing-the-future-of-ai-agents/) — a major lab's blueprint for production agent security: defense-in-depth (sandboxing + injection resistance + alignment + treating internal agents as potentially misaligned) plus a behavioral monitor trained on ~1M coding-agent trajectories, live on Gemini Spark
- [MosaicLeaks: Privacy Risks for Deep Research Agents](https://huggingface.co/blog/ServiceNow/mosaicleaks) — research agents leak local/private context through the *mosaic effect* of their web queries; training for task success alone makes leakage worse, and "you can't prompt privacy in, you have to train it in" — read before deploying any retrieval/tool agent over sensitive data
- [Sumi: Open Uniform Diffusion Language Model from Scratch](https://arxiv.org/abs/2606.19005) — the first uniform-diffusion LM pretrained from scratch at both large parameter scale and token budget, a clean open reference point; study it to understand diffusion-LM scaling firsthand
- [GLM-5.2](https://huggingface.co/zai-org/GLM-5.2) — Z.ai's flagship open MoE (~753B, MIT) and the first GLM at a full 1M-token context via a `GlmMoeDsa` sparse-attention operator; study the openly-reported benchmarks and the sparse-attention design as the current open-weight route to cheap long context

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named.

- No on-axis earthquake on the [HN](https://news.ycombinator.com/) front page (read direct via the Algolia API): the loudest AI items are an [OpenAI custom inference chip](https://news.ycombinator.com/) (chip-business news, off-axis) and an [Anthropic-vs-Alibaba](https://news.ycombinator.com/) model-capability-extraction dispute (industry/legal, off-axis) — notable but not field-shaking for the tracked axes.
- The diffusion-LM conversation stays hot on HN (Introspective dLLMs, Consistency dLLMs "14× faster", "dLLMs are super data learners") — intake corroboration for the [diffusion-language-models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) promotion, not evidence.
- Reddit broad-pulse (tvly): local-inference hardware chatter (RTX PRO 6000, Strix Halo, "NVFP4 KV cache in vLLM" aggregator post) and [Gemma 4 on Ollama](https://ollama.com/library/gemma4); broad news (Gemini 3.5 Pro slips to July, AI-policy items) carried no model-access earthquake.
- Degraded this run: the [code4AI](https://www.youtube.com/@code4AI) YouTube curator lane is IP-blocked end-to-end (feed 404 + page-extract failure, 3rd run); a best-effort search surfaced an agent-shared-memory ("Trajectory RAG") video but it couldn't be followed to a primary — the theme is captured via the agent-memory study. Pointer/digest blogs (Interconnects, Simon Willison, alphamatch) swept and clean; [AINews](https://news.smol.ai/) index JS-only.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (39)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-25](reports/2026-06-25.md) · weekly: [2026-W25](reports/weekly/2026-W25.md) · conventions: [AGENTS.md](AGENTS.md)
