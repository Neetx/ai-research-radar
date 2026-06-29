# AI Radar

![trends](https://img.shields.io/badge/trends-15-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-6-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-28-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--29-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-29):**
- **[Open-weight frontier MoE](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) → 🌊 MAINSTREAMING.** The serving-stack-absorption gate fired across BOTH engines: vLLM ships [day-0 native Nemotron 3 Ultra](https://blog.vllm.ai/blog/2026-06-04-nemotron-3-ultra-vllm) (a 2nd frontier model first-class native), and [SGLang v0.5.14](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) adds native GLM-5.2 / Kimi-K2.7-Code / LFM2.5 / DiffusionGemma / Nemotron-H in one release — the GLM-5.2 native-serving gate, long unfired, is now met.
- **[Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) emerging → 🚀 accelerating.** [SGLang v0.5.14](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) ships first-class kernels for the whole class — DeepSeek Sparse Attention (DSA) indexer, Nemotron-H Mamba2-hybrid DP-attention, a Mamba radix-cache, a Kimi-Linear CuteDSL kernel — a 2nd serving engine (after vLLM's MSA) on these operators.
- **[Diffusion LMs](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale): DiffusionGemma now native on a 2nd engine** (SGLang, evidence add, no stage move); **Baidu "Unlimited OCR" R-SWA** pinned to [arXiv 2606.23050](TRENDS.md#observation_queue) (closes the 06-27 unpinned flag).
- **Watchlist burned 43 → 28** (provenance of promoted trends pruned). `capture-leak: 13 ids checked / 0 leaks`.

## ⭐ Pinned topics

Standing-watch axes — never archived, but shown `dormant` honestly when quiet.

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-26](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |

## Trends

🌱 2 · 📈 6 · 🚀 6 · 🌊 1 · 🏔 0 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-06-26](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-06-26](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-11](https://docs.vllm.ai/en/latest/features/disagg_prefill.html) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-26](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-22](https://sakana.ai/fugu-release/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-06-23](https://arxiv.org/abs/2606.24530) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌱 seed | [2026-06-23](https://arxiv.org/abs/2606.24775) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-06-16](https://huggingface.co/zai-org/GLM-5.2) |

## Worth studying

- [SGLang v0.5.14 release notes](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) — one serving-engine release that absorbs much of the frontier open-weight + subquadratic-attention class at once: native DeepSeek Sparse Attention (DSA indexer + LoRA), Nemotron-H Mamba2-hybrid DP-attention + MTP, a Mamba radix-cache (int8 recurrent-state pool), a Kimi-Linear (KDA) CuteDSL prefill kernel, plus native GLM-5.2 / Kimi-K2.7-Code / LFM2.5 / DiffusionGemma. A concrete map of what serving engines must build to run sparse/linear/hybrid-attention MoEs — the engineering reality behind subquad-attn-012 and open-weight-003 moving on serving-stack absorption
- [A First Comprehensive Study of TurboQuant (vLLM)](https://blog.vllm.ai/2026/05/11/turboquant.html) — the vLLM team's honest production benchmark of TurboQuant KV-cache quantization vs BF16/FP8 on 2×H100: low-bit KV-quant is NOT a throughput/latency win (FP8 matches BF16 at negligible cost); TurboQuant only pays off as a memory-CAPACITY lever, cutting burst TTFT ~5×. Read before reaching for KV-quant in serving
- [DiffusionGemma: The First dLLM Natively Supported in vLLM](https://blog.vllm.ai/2026/06/10/diffusion-gemma.html) — vLLM's engineering writeup of integrating a discrete-diffusion LM into an autoregressive-first engine via a native `DiffusionSampler` + reusable `ModelState`, with `vllm bench serve` throughput on H100/H200; the reference for what serving a non-autoregressive LM actually requires
- [Accelerating Gemini Nano with frozen Multi-Token Prediction](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) — Google Research's practical on-device acceleration: retrofit MTP onto a FROZEN production model (Gemini Nano v3) so one model both generates and self-drafts — speculative-decoding-style speedups WITHOUT a separate drafter, now on Pixel 9/10
- [AWS Lambda MicroVMs](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) — the first hyperscaler-native agent-sandbox primitive: per-session Firecracker microVMs (VM-level isolation) with image-then-launch snapshot resume for user/AI-generated code; the reference for what an agent-code execution layer needs (isolation, fast resume, statefulness)
- [The Verification Horizon: No Silver Bullet for Coding Agent Rewards](https://arxiv.org/abs/2606.26300) — a 12-author (Alibaba/Qwen-line) result inverting a load-bearing assumption of agentic RL: "verifying is easier than producing" is breaking down for coding agents — generating complex solutions outpaces our ability to verify them, so reward *verification* becomes the bottleneck; read before trusting any verifiable-reward / RLVR pipeline
- [iLLaDA-8B (Improved Large Language Diffusion Models)](https://huggingface.co/GSAI-ML/iLLaDA-8B-Base) — RUC/GSAI-ML's open-weights (Apache-2.0, paper 2606.25331) 8B fully-bidirectional masked-diffusion LM trained from scratch on 12T tokens: the clearest "diffusion LM at autoregressive quality" datapoint — its card ties autoregressive Qwen2.5-7B (63.9 vs 63.3); the third independent open diffusion base model
- [Thinking to Recall: How Reasoning Unlocks Parametric Knowledge in LLMs](https://research.google/blog/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms/) — Google Research: why a reasoning trace helps an LLM recall even *simple* single-hop facts — a *computational buffer* (reasoning tokens as latent computation) and *factual priming* — so reasoning expands the parametric-knowledge boundary; the hook is process rewards on factually-supported steps to cut hallucination
- [Qwen-AgentWorld (35B-A3B language world model)](https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B) — Alibaba/Qwen's open-weights (paper 2606.24597) "native language world model": a 35B-A3B MoE where *predicting the next environment state* from an agent's action+history IS the objective from CPT onward; a runnable bridge between world models and agent infrastructure
- [Prompt Injection as Role Confusion](https://arxiv.org/abs/2603.12277) — Ye/Cui/Hadfield-Menell (MIT, ICML 2026): the cleanest mechanistic *theory* of why prompt injection works — LLMs infer who is speaking from how a span *sounds*, not its labeled `<user>`/`<tool>` role; study it for "role probes", why label-based defenses are brittle, and as the underpinning of the architectural/least-privilege turn
- [Sakana Fugu: A Multi-Agent Orchestration System as a Foundation Model](https://sakana.ai/fugu-release/) — Sakana AI's product: a small LM TRAINED to orchestrate a pool of frontier LLMs (choosing/switching models, recursive self-calls for test-time scaling) behind one API; the clearest example of "orchestration-as-a-model" vs orchestration-as-a-framework. Benchmarks are vendor-claimed.
- [Looped World Models (LoopWM)](https://arxiv.org/abs/2606.18208) — the first looped-transformer architecture for *world modelling*: a parameter-shared block iteratively refines the latent environment state with adaptive compute (~100× parameter efficiency, less long-horizon drift); the looped/recursive-computation idea crossing into world simulation

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named. (Latest daily intake: 2026-06-29.)

- **No earthquake this scan.** The 06-27 closed-model/policy story (GPT-5.6 "Sol" preview, U.S. vetting of access, Anthropic Mythos trusted-org release) has settled; the field's loudest thread is now [GLM-5.2 benchmark comparisons](https://news.ycombinator.com/) (top HN, ~640 pts) — an already-tracked open-weight model, intake only.
- Community texture on [r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/) (via Tavily): GLM-5.2 vs closed-frontier reasoning, CPU-only inference throughput ("64 t/s on 6-year-old CPUs"), a larger Qwen-AgentWorld variant (world-model watch area), and recurring "Meta won't open-source its next model" sentiment — all intake, nothing new to route.
- Degraded: the [code4AI](https://www.youtube.com/@code4AI) YouTube curator lane remains IP-blocked end-to-end (not re-attempted per the standing heal note); [alphamatch](https://alphamatch.ai/blog) and pointer/digest blogs swept and clean.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (28)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-29](reports/2026-06-29.md) · weekly: [2026-W26](reports/weekly/2026-W26.md) · conventions: [AGENTS.md](AGENTS.md)
