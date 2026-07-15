# AI Radar

![trends](https://img.shields.io/badge/trends-18-3266ad?style=flat-square) ![accelerating](https://img.shields.io/badge/accelerating-3-e8590c?style=flat-square) ![watchlist](https://img.shields.io/badge/watchlist-24-6c757d?style=flat-square) ![updated](https://img.shields.io/badge/updated-2026--07--15-2f9e44?style=flat-square)

Tracking AI-ecosystem trends (frontier research → engineering) for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-07-15):**
- 📄 One evidence add: [Bonsai 27B](https://prismml.com/news/bonsai-27b) (PrismML) — the first 27B-class 1-bit/ternary **multimodal** model to run on a phone (1-bit variant 3.9 GB fitting an iPhone 17 Pro; ternary 5.9 GB on a laptop), low-bit end-to-end on a Qwen3.6-27B base → [⭐ Small & 1-bit models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference). Refreshes last-evidence 06-26 → 07-14, clearing near-dormancy; NO stage move. Downloadable GGUFs on the prism-ml HF org partially close this trend's "no ternary >2.4B / not downloadable" caveats.
- 🌐 No new frontier open-weight LLM drop, no earthquake. HF-org recheck across 9 labs: 8-org set unchanged (new-but-off-axis: Nemotron-3-Embed embeddings, Kimi-K2.7-Code-DFlash).
- 🧹 `capture-leak: 16 ids / 0 missing`; watchlist 25→24 (dropped stale 06-27 items: GPT-5.6 "Sol" pulse note + UltraQuant 4-bit KV-quant, below-dormant-bar). Queued: [Multi-Agent-Fail-to-Explore](https://arxiv.org/abs/2607.11250), [Proxy-Guided-Post-Training](https://arxiv.org/abs/2607.11505).
- 🔭 A recurring **world-model open-release** cluster surfaced this run (Giga-World-1, lingbot-world, LeMario, Xiaomi-Robotics-U0) — watch-only, flagged for the weekly as a candidate axis.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-09](https://arxiv.org/abs/2607.08186) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |

## Trends

🌱 5 · 📈 4 · 🚀 3 · 🌊 1 · 🏔 0 · 📉 0 · 💤 5

| trend | stage | latest signal |
|---|---|---|
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🚀 accelerating | [2026-07-07](https://arxiv.org/abs/2607.05722) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 🚀 accelerating | [2026-07-01](https://arxiv.org/abs/2607.00466) |
| [Subquadratic & sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 🚀 accelerating | [2026-06-26](https://github.com/sgl-project/sglang/releases/tag/v0.5.14) |
| [⭐ Small & 1-bit models (CPU/edge)](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 emerging | [2026-07-14](https://prismml.com/news/bonsai-27b) |
| [⭐ Latent/recursive reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 📈 emerging | [2026-07-09](https://arxiv.org/abs/2607.08186) |
| [⭐ Latent inter-model communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 📈 emerging | [2026-07-01](https://arxiv.org/abs/2607.01308) |
| [Agent security (injection limits)](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 📈 emerging | [2026-06-30](https://arxiv.org/abs/2606.31227) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 seed | [2026-07-09](https://arxiv.org/abs/2607.08964) |
| [On-policy distillation (post-training)](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 🌱 seed | [2026-07-06](https://arxiv.org/abs/2607.05394) |
| [Parametric injection (behavior→weights)](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 seed | [2026-07-02](https://arxiv.org/abs/2607.02512) |
| [Agent harness/runtime/memory infra](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🌱 seed | [2026-06-30](https://www.microsoft.com/en-us/research/blog/skillopt-agent-skills-as-trainable-parameters/) |
| [Agentic-RL credit assignment](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 seed | [2026-06-30](https://arxiv.org/abs/2606.32034) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🌊 mainstreaming | [2026-07-05](https://huggingface.co/meituan-longcat/LongCat-2.0-INT8) |
| [⭐ Low-bit quantization (vector/trellis)](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 💤 dormant | [2026-06-23](https://arxiv.org/abs/2606.24033) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 💤 dormant | [2026-06-22](https://arxiv.org/abs/2606.22883) |
| [Remote agent sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 💤 dormant | [2026-06-22](https://aws.amazon.com/blogs/aws/run-isolated-sandboxes-with-full-lifecycle-control-aws-lambda-introduces-microvms/) |
| [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 💤 dormant | [2026-06-22](https://sakana.ai/fugu-release/) |
| [MCP standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 💤 dormant | [2026-06-11](https://openai.github.io/openai-agents-python/mcp/) |

## Worth studying

- [Bonsai 27B: the first 27B-class model to run on a phone](https://prismml.com/news/bonsai-27b) — PrismML: a Qwen3.6-27B-based **multimodal** model shipped low-bit end-to-end (no higher-precision escape hatches) as ternary {−1,0,+1} at 1.71 bits/weight (5.9 GB, laptop) and 1-bit {−1,+1} at 1.125 bits/weight (3.9 GB, fits an iPhone 17 Pro). The current high-water mark for extreme-quantization on-device inference: a 27B-class agent (tool calls, computer-use loops, 262K context) in a phone's memory budget, with downloadable GGUFs on the prism-ml HF org.
- [Direct-OPD: Weak-to-Strong Generalization via Direct On-Policy Distillation](https://arxiv.org/abs/2607.05394) — Shiyuan Feng et al. (10 authors): a practically-motivated post-training recipe for anyone doing RLVR. As models scale, running RL on the target is the bottleneck, so run RL on a SMALL cheap model and transfer only the RL-induced policy shift to the strong target — compare the post-RL teacher to its own pre-RL reference and use the log-ratio as a dense implicit reward, so only "what RL changed" transfers.
- [Flash-MSA: open-source training kernels for MiniMax Sparse Attention](https://nanduruganesh.github.io/flash-msa/) — a solo engineer's CuTeDSL kernels billed as "the world's first performant open-source TRAINING kernels for MiniMax Sparse Attention" on Hopper/Blackwell. The kernel engineering behind subquad-attn-012's training side — block-sparse selection, GQA-not-MLA for reproducibility, group-wise proxy-head specialization; caveat: solo project, "not an official MiniMax implementation".
- [Colibri: run GLM-5.2 (744B MoE) on a 25 GB-RAM machine in pure C](https://github.com/JustVugg/colibri) — JustVugg (72★): a pure-C, zero-dependency inference engine that streams MoE experts from disk so a 744B model runs on ~25 GB RAM at 0.05–0.1 tok/s cold. An existence proof and design reference for extreme MoE expert-offloading on CPU; caveat: barely-interactive throughput, solo/community project.
- [UniClawBench: capability-driven eval of proactive agents in live containers](https://arxiv.org/abs/2607.08768) — HKU-MMLab (7 authors): a deployment-grounded agent benchmark that runs agents in LIVE Docker containers scored by step-by-step completion checkpoints, decomposing 400 bilingual tasks by five foundational capabilities so a failure points to a capability. The current methodology for evaluating proactive / real-world agents.
- [Nemotron-Labs-Diffusion: a tri-mode AR + diffusion + self-speculation LM](https://arxiv.org/abs/2607.05722) — NVIDIA (26 authors): the clearest current case that AR and diffusion decoding are complementary rather than rival. One architecture, JOINT AR-diffusion objective, switches among AR, diffusion and self-speculation; shipped OPEN at 3B/8B/14B. Caveat: throughput vendor-reported, native diffusion serving not yet confirmed in an engine release.
- [OmniOpt: Taxonomy, Geometry, and Benchmarking of Modern Optimizers](https://arxiv.org/abs/2607.04033) — 12 authors (top HF daily paper 07-07, 67 up): a unified survey + benchmark "cookbook" for the 100+ modern optimizers, treating every update as a structured transformation through a five-stage meta-pipeline, benchmarked under matched budgets. Read it before picking an optimizer for a large training run.
- [Bridging the Gap Between Latent and Explicit Reasoning with Looped Transformers](https://arxiv.org/abs/2606.31779) — Ying Fan, Anej Svete, Kangwook Lee: the clearest answer to "why has latent chain-of-thought underperformed, and can it be fixed?" Latent CoT LOSES to explicit CoT beyond ~1B params and the gap WIDENS with scale; this argues looped / recurrent-depth Transformers are the natural substrate and gives a recipe that closes the gap.
- [AI-Infra-Guard: Multi-Layer Agent Red Teaming](https://arxiv.org/abs/2606.31227) — Yong Yang et al. (10 authors): a practical open-source blueprint for the agent-security stack. The attack surface is STRATIFIED (infrastructure, protocol/tool, behavior, model) and no single paradigm covers all layers, so it matches a technique to each. A checklist of what each layer needs tested.
- [SkillOpt: Agent skills as trainable parameters](https://www.microsoft.com/en-us/research/blog/skillopt-agent-skills-as-trainable-parameters/) — Microsoft Research: "make the skill file itself trainable." SkillOpt treats the skill file as a trainable parameter OUTSIDE a frozen model (bounded edits, validation gating, rejected-edit feedback). Best-or-tied-best in all 52 eval cells with NO weight updates, and skills transfer across model scales.
- [Memora: A Harmonic Memory Representation](https://www.microsoft.com/en-us/research/blog/memora-a-harmonic-memory-representation-balancing-abstraction-and-specificity/) — Microsoft Research: agent long-term memory that decouples WHAT is stored from HOW it is retrieved. New SOTA on LoCoMo and LongMemEval, beating Mem0, RAG and full-context inference while using up to 98% FEWER context tokens — read it before building any long-horizon agent memory layer.
- [PrismML Ternary Bonsai (true 1.58-bit LLMs at 8B/4B/1.7B)](https://prismml.com/news/ternary-bonsai) — a commercial, independent (Caltech-origin) lab shipping a ternary-throughout LLM family: {-1,0,+1} weights in EVERY layer, ~9× smaller memory than 16-bit. The clearest existence proof of true 1.58-bit models ABOVE the ~2.4B research ceiling; caveat: benchmarks vendor-claimed.

## Community pulse

> Unverified sentiment from social/community sources — intake only, never evidence. Links to threads, no individuals named. (Latest daily intake: 2026-07-15.)

- **Quiet run — no earthquake.** No frontier open-weight drop, ban or open-model access event; the ground did not move.
- On-axis lead: "[Bonsai 27B: a 27B-class model that runs on a phone](https://hn.algolia.com/?query=Bonsai%2027B&sort=byPopularity&type=story)" (515 pts) — followed to the PrismML primary and captured → small-cpu-models-008.
- World-model activity recurs: "[LeMario: Training a JEPA World Model on Super Mario Bros](https://hn.algolia.com/?query=LeMario%20JEPA&sort=byPopularity&type=story)" (72 pts) on HN, plus Giga-World-1 / lingbot-world open releases trending on [HF](https://huggingface.co/models?sort=trending) — a watch-only cluster flagged for the weekly.
- Also drawing attention (off-axis, not queued): "[Solving 20 Erdős Problems with 20 Codex Accounts in Parallel](https://hn.algolia.com/?query=Erdos%20Codex&sort=byPopularity&type=story)" (97 pts, agentic-parallelism anecdote).
- Degraded: GitHub is proxy-scoped to only this repo, so the external release-feed watch (vLLM/SGLang/llama.cpp/MCP) is 403 — healed via PyPI version signal (vLLM 0.25.1, SGLang 0.5.15.post1, notes unread); the [code4AI](https://www.youtube.com/@code4AI) YouTube lane and Reddit remain IP/datacenter-blocked. HF-daily-papers + HF-org + HN carried discovery.

## Output map

[TRENDS.md](TRENDS.md) · [watchlist (24)](TRENDS.md#observation_queue) · [reports/](reports/) → [2026-07-15](reports/2026-07-15.md) · weekly: [2026-W28](reports/weekly/2026-W28.md) · [AGENTS.md](AGENTS.md) · [SOURCES.md](SOURCES.md)
