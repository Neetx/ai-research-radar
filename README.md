# AI Radar

![trends](https://img.shields.io/badge/trends-15-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-6-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-25-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--06--30-2f9e44?style=flat-square)

Tracks research and engineering trends across the AI ecosystem, for an AI researcher / AI-systems engineer. This page is generated from [TRENDS.md](TRENDS.md), the ledger of record — click a trend for its full evidence. ⭐ marks pinned standing-watch topics.

**Since last scan (2026-06-30):**
- **[Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards): a 7th group, the day's top paper.** Added [Agentic Abstention](https://arxiv.org/abs/2606.28733) (109 up on HF) — a 28K-task / 13-system study of *when* an agent should stop acting under uncertainty (not just whether it can abstain); last_evidence 06-26 → 06-27, stays seed.
- **[Agent harness/runtime/memory](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) refreshed.** Added [Experience Graphs / Trellis](https://arxiv.org/abs/2606.29823) — agent experience/state as first-class queryable database state; the memory-as-managed-data facet now spans ≥3 independent groups (last_evidence 06-23 → 06-29), but no shared interface yet → stays seed.
- **[Open-weight frontier MoE](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs): an 8th lab.** [LongCat-2.0](https://huggingface.co/meituan-longcat/LongCat-2.0) (Meituan, 1.6T/48B, trained entirely on non-NVIDIA AI ASIC superpods) — weights still "coming soon" (re-checked this pass); stays mainstreaming.
- **Watchlist 25 (at cap).** Dropped MosaicLeaks (06-19 agent-privacy, no recurrence in 11d). `capture-leak: 11 ids checked / 0 leaks`. Dormancy watch: MCP & latent-comm (both last_evidence 06-11, 19d) cross the dormant line ~07-02 absent a new primary.

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
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-06-29](https://github.com/vllm-project/vllm/releases/tag/v0.24.0) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-06-26](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-06-26](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 🚀 accelerating | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 🚀 accelerating | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 🚀 accelerating | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-06-26](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 emerging | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 emerging | [2026-06-22](https://sakana.ai/fugu-release/) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-16](https://deepmind.google/blog/securing-the-future-of-ai-agents/) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-06-16](https://arxiv.org/abs/2606.18023) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-06-11](https://arxiv.org/abs/2606.13594) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌱 seed | [2026-06-29](https://arxiv.org/abs/2606.29823) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-06-27](https://arxiv.org/abs/2606.28733) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-06-30](https://huggingface.co/meituan-longcat/LongCat-2.0) |

## Worth studying

- [Agentic Abstention: Do Agents Know When to Stop Instead of Act?](https://arxiv.org/abs/2606.28733) — the day's top HF paper (109 up): agentic abstention is sequential (answer / abstain / gather-more per turn), so the metric that matters is not WHETHER an agent can abstain but WHEN. Across web-shopping, terminal and QA (28K+ tasks, 13 systems), some agents never stop when they should, others burn many wasted tool calls — study it before trusting any long-horizon agent loop in production
- [Experience Graphs / Trellis: The Data Foundation for Self-Improving Agents](https://arxiv.org/abs/2606.29823) — a 25-author argument that long-horizon agentic work is a database WORKLOAD: the "experience graph" an agent produces (artifacts, tool outputs, rewards, sibling comparisons, causal lineage over hundreds of steps) is thrown away as JSON checkpoints today; Trellis treats it as first-class, governed, queryable state. The systems lens on agent memory consolidating the agent-runtime-015 axis
- [LongCat-2.0 (Meituan, 1.6T/48B MoE)](https://huggingface.co/meituan-longcat/LongCat-2.0) — an 8th lab's frontier open-weight MoE announcement, notable for its TRAINING substrate: the full 1.6T run (>35T tokens, "no rollbacks or irrecoverable loss spikes") was done ENTIRELY on AI ASIC superpods (non-NVIDIA) — an existence proof that frontier-scale pretraining is now viable off the CUDA stack, plus "LongCat Sparse Attention" for 1M ctx. Caveat: weights "coming soon", so an announcement to track
- [Agents-A1: Scaling the Horizon, Not the Parameters](https://arxiv.org/abs/2606.30616) — a 35B MoE agentic model reaching "trillion-parameter-level" agent performance by scaling the AGENT HORIZON (45K-token-avg trajectories) instead of parameters, via a 3-stage recipe ending in multi-teacher domain-routed on-policy distillation; study it for the thesis that horizon/data infrastructure + distillation can substitute for raw scale in agents
- [SGLang v0.5.14 release notes](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) — one serving-engine release that absorbs much of the frontier open-weight + subquadratic-attention class at once: native DeepSeek Sparse Attention (DSA indexer + LoRA), Nemotron-H Mamba2-hybrid DP-attention + MTP, a Mamba radix-cache (int8 recurrent-state pool), a Kimi-Linear (KDA) CuteDSL prefill kernel, plus native GLM-5.2 / Kimi-K2.7-Code / LFM2.5 / DiffusionGemma. A concrete map of what serving engines must build to run sparse/linear/hybrid-attention MoEs
- [A First Comprehensive Study of TurboQuant (vLLM)](https://blog.vllm.ai/2026/05/11/turboquant.html) — the vLLM team's honest production benchmark of TurboQuant KV-cache quantization vs BF16/FP8 on 2×H100: low-bit KV-quant is NOT a throughput/latency win (FP8 matches BF16 at negligible cost); TurboQuant only pays off as a memory-CAPACITY lever, cutting burst TTFT ~5×. Read before reaching for KV-quant in serving
- [DiffusionGemma: The First dLLM Natively Supported in vLLM](https://blog.vllm.ai/2026/06/10/diffusion-gemma.html) — vLLM's engineering writeup of integrating a discrete-diffusion LM into an autoregressive-first engine via a native `DiffusionSampler` + reusable `ModelState`, with `vllm bench serve` throughput on H100/H200; the reference for what serving a non-autoregressive LM actually requires
- [Accelerating Gemini Nano with frozen Multi-Token Prediction](https://research.google/blog/accelerating-gemini-nano-models-on-pixel-with-frozen-multi-token-prediction/) — Google Research's practical on-device acceleration: retrofit MTP onto a FROZEN production model (Gemini Nano v3) so one model both generates and self-drafts — speculative-decoding-style speedups WITHOUT a separate drafter, now on Pixel 9/10
- [AWS Lambda MicroVMs](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) — the first hyperscaler-native agent-sandbox primitive: per-session Firecracker microVMs (VM-level isolation) with image-then-launch snapshot resume for user/AI-generated code; the reference for what an agent-code execution layer needs (isolation, fast resume, statefulness)
- [The Verification Horizon: No Silver Bullet for Coding Agent Rewards](https://arxiv.org/abs/2606.26300) — a 12-author (Alibaba/Qwen-line) result inverting a load-bearing assumption of agentic RL: "verifying is easier than producing" is breaking down for coding agents — generating complex solutions outpaces our ability to verify them, so reward *verification* becomes the bottleneck; read before trusting any verifiable-reward / RLVR pipeline
- [iLLaDA-8B (Improved Large Language Diffusion Models)](https://huggingface.co/GSAI-ML/iLLaDA-8B-Base) — RUC/GSAI-ML's open-weights (Apache-2.0, paper 2606.25331) 8B fully-bidirectional masked-diffusion LM trained from scratch on 12T tokens: the clearest "diffusion LM at autoregressive quality" datapoint — its card ties autoregressive Qwen2.5-7B (63.9 vs 63.3); the third independent open diffusion base model
- [Thinking to Recall: How Reasoning Unlocks Parametric Knowledge in LLMs](https://research.google/blog/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms/) — Google Research: why a reasoning trace helps an LLM recall even *simple* single-hop facts — a *computational buffer* (reasoning tokens as latent computation) and *factual priming* — so reasoning expands the parametric-knowledge boundary; the hook is process rewards on factually-supported steps to cut hallucination

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named. (Latest daily intake: 2026-06-30.)

- **No earthquake this scan.** The loudest AI threads on the [HN front page](https://news.ycombinator.com/) are "Ornith-1.0: self-improving open-source models for agentic coding" (~232 pts) and "[LongCat-2.0](https://huggingface.co/meituan-longcat/LongCat-2.0), a 1.6T/48B MoE" (~205 pts) — both already captured/routed; nothing new on-axis.
- Intake captured and routed this pass: [Ornith-1.0](https://huggingface.co/deepreinforce-ai/Ornith-1.0-397B) (deepreinforce-ai; card opened — a self-improving *agentic-coding specialist* family, below the frontier-general bar → watchlist), and the cs.MA exploration tops (Agentic Abstention, Experience Graphs/Trellis → routed to trends).
- Degraded: the [code4AI](https://www.youtube.com/@code4AI) YouTube curator lane remains IP-blocked end-to-end (not re-attempted per the standing heal note); HF-daily-papers + HN overlap carried discovery this run.

## Output map

Ledger: [TRENDS.md](TRENDS.md) · unverified signals: [watchlist (25)](TRENDS.md#observation_queue) · sources: [SOURCES.md](SOURCES.md) · daily reports: [reports/](reports) — latest [2026-06-30](reports/2026-06-30.md) · weekly: [2026-W26](reports/weekly/2026-W26.md) · conventions: [AGENTS.md](AGENTS.md)
</content>
</invoke>
