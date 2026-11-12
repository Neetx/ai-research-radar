# AI Radar

![trends](https://img.shields.io/badge/trends-24-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-12-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-7-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--12-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-11-12):** New trend — [Decision models](TRENDS.md#id-decision-models-024-system-1-decision-models-single-forward-pass-calibrated-classifiers-as-a-distinct-benchmarked-model-category) seeded from Google's [Gemini Decisions API](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/) and Hugging Face's own ["decision" pipeline](https://huggingface.co/blog/decision), pulling together a pattern this radar had tracked piecemeal for months · [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) added Huawei's [MACaQ](https://arxiv.org/abs/2611.10649), a cross-modal W4A4 quantizer · [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) added vLLM's own [encoder-disaggregation engineering post](https://blog.vllm.ai/blog/2026-11-11-encoder-disaggregation-epd) · [Agent harness/runtime](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) added KAIST's [WikiTrace](https://arxiv.org/abs/2611.14320), an evidence-linked-memory primitive.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-11](https://huggingface.co/blog/qvac/botpsy) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08390) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05150) |

## Trends

🌱 7 · 📈 12 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-11](https://huggingface.co/blog/qvac/botpsy) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-11-11](https://huggingface.co/blog/qvac/botpsy) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-11-11](https://blog.vllm.ai/blog/2026-11-11-encoder-disaggregation-epd) |
| [Decision models](TRENDS.md#id-decision-models-024-system-1-decision-models-single-forward-pass-calibrated-classifiers-as-a-distinct-benchmarked-model-category) | 📈 accelerating | [2026-11-11](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-11-10](https://developer.nvidia.com/blog/agent-substrate-advancing-kubernetes-for-agents-at-scale/) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 📈 accelerating | [2026-11-09](https://aaif.io/blog/when-good-agents-make-bad-systems) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-11-06](https://huggingface.co/blog/allenai/toyblocks) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-11-03](https://arxiv.org/abs/2611.04671) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-11-02](https://aws.amazon.com/about-aws/whats-new/2026/10/connect-flows-mcp-tools) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-11-02](https://developer.nvidia.com/blog/build-world-models-for-interactive-simulation-with-nvidia-cosmos/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-29](https://cursor.com/blog/agent-sdk) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08390) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05150) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05129) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-11-03](https://www.fireblocks.com/?p=32426) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-11-02](https://openai.com/index/lifeval/) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-11-02](https://rikiyat.github.io/blog/weight-space-programming/) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-10-29](https://arxiv.org/abs/2610.35013) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-11-10](https://www.microsoft.com/en-us/research/blog/lazare-veni-foras-reprogramming-dormant-neurons-to-backdoor-ai-agents/) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-11-10](https://deepmind.google/blog/introducing-alphaproof-code/) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-11-10](https://arxiv.org/abs/2611.14320) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-11-05](https://ernie.baidu.com/release/ernie-5-5-flash-base/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-30](https://huggingface.co/Diffuspace/Clover-35B-A3B-Preview) |

## Worth studying

- [My AI Agents Found an Unmapped Maya Site](https://pietromiotti.com/latest/maya-site) — a first-hand diary of 48 agents triaging public lidar strips with no classifier, flagging a real unregistered archaeological site.
- [Decision Models in Hugging Face](https://huggingface.co/blog/decision) — a concise introduction to a model category every practitioner building routing/classification/guardrail logic should know.
- [Introducing AlphaProof Code](https://deepmind.google/blog/introducing-alphaproof-code/) — a multi-LLM agentic framework that formally verified Signal's cryptographic protocol down to compiled-code depth (6M+ lines of machine-checked Lean) in four weeks, a task that historically took expert teams years.
- [After 7-months, Glasswing Overwhelms Maintainers with Underwhelming Findings](https://www.vulncheck.com/blog/anthropic-glasswing-november-update) — an independent security vendor's skeptical, numbers-first audit of a frontier lab's own AI-vulnerability-discovery claims, a template for reading any adoption claim against independently-tracked ground truth.
- [A proof of the Aaronson-Ambainis conjecture](https://psi.inc/research/aaronson-ambainis) — a case study in what mechanically-verified AI-driven math research actually looks like end to end: Lean proof, two independent kernels, a deliberately-false control case, and a third-party replay.
- [llama-modchip v2.3.0](https://github.com/synchopate/llama-modchip) — fits a 284B-parameter frontier MoE inside 64GB of CPU RAM at 256K context with zero GPUs, via Hessian-weighted 2-bit quantization and AVX-512 kernels.
- [Scientist World: Grow a Research World for AI-Scientists](https://arxiv.org/abs/2611.08478) — turns 1,000 research papers into executable, verifiable environments where an AI-Scientist is graded against what the human authors actually achieved.
- [The Agent Economy by the Numbers: 2026 Data, Trends, and Blind Spots](https://www.fireblocks.com/?p=32426) — a payments vendor's own honest accounting: ~196M x402 transactions sound impressive until you learn over half trace to a 2025 memecoin arbitrage-bot loop, not genuine agentic commerce.
- [GPT‑6 Cyber: Advancing the frontier of aligned cybersecurity agents](https://openai.com/index/introducing-gpt-6-cyber) — a named model release with quantified capability AND alignment gains, already fixing 81 real Firefox 0-days with patches Mozilla has shipped.
- [Agents aren't humans (but they kinda are)](https://blog.cloudflare.com/trusted-agent-delegation/) — Cloudflare's proposal for cryptographic agent identity/delegation on the open web, launching an IETF-track coalition — worth knowing before it's a de facto standard.
- [A thousand fewer paths to root](https://openai.com/index/a-thousand-fewer-paths-to-root/) — an autonomous Linux-kernel vulnerability-discovery/exploitation/patching pipeline that validated and patched 948 real bugs in one run, and a concrete dual-use capability benchmark in its own right.
- [Use NVIDIA NeMo to Turn Agent Failures into Tests and Harness Fixes](https://developer.nvidia.com/blog/use-nvidia-nemo-to-turn-agent-failures-into-tests-and-harness-fixes/) — a reproducible trace→eval→harness-fix optimization loop with a held-out generalization check, a template for self-improving agent harnesses.
- [Agensh: A Decentralized, Scalable Multiagent Harness](https://github.com/microsoft/Agensh) — Microsoft Research's open-source harness scaling self-organized coding-agent teams to 1,024 workers with no central orchestrator.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- Google's [Gemini Decisions API launch](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/) landed the same week as Hugging Face's own "decision models" explainer, pushing a months-old scattered pattern into a tracked trend.
- An individual's account of [48 AI agents finding an unmapped Maya site](https://pietromiotti.com/latest/maya-site) via lidar triage drew the day's #2 Hacker News slot.
- An open-source quantization method, [MACaQ](https://github.com/huawei-csl/MACaQ), drew independent corroboration on r/LocalLLaMA the same day it shipped.
- [United Airlines banning AI agents from booking flights](https://www.cbsnews.com/news/united-airlines-bans-ai-agents-booking-flights/) on travelers' behalf circulated on Hacker News.
- A session-sync tool for coding agents, [Atuin Threads](https://blog.atuin.sh/threads-agent-sessions/), surfaced on Hacker News as a harness-infrastructure discussion point.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~7 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-12.md)) · weekly: [latest](reports/weekly/2026-W45.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
