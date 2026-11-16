# AI Radar

![trends](https://img.shields.io/badge/trends-24-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-12-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-8-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--16-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-11-16):** [Multi-agent engineering](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) was rescued from an 18-day gap by Google's [Antigravity /teamwork](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) results batch · [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) added Cloudflare's and Amazon's independent disclosures of [ARTEX AI-pentesting orchestrators](https://blog.cloudflare.com/adapting-to-ai-penetration-testing-orchestrators/) scanning the open web at scale · [Remote sandboxes](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) gained Cloudflare's newly [open-sourced Kitesurf](https://blog.cloudflare.com/kitesurf-open-source/) browser-for-agents · [MCP](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) picked up a new [file-upload/download extension proposal](https://blog.modelcontextprotocol.io/posts/exploring-file-uploads-and-downloads-in-mcp/).

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-12](https://arxiv.org/abs/2611.17309) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-12](https://edge0.ai/blog/introducing-edge0-145b-frontier-ai-capabilities-on-your-own-computer) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08390) |

## Trends

🌱 7 · 📈 12 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-11-13](https://blog.cloudflare.com/kitesurf-open-source/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-11-13](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) |
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-11-12](https://vllm.ai/blog/2026-11-12-deepseek-v41-flash-vera-rubin) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-12](https://edge0.ai/blog/introducing-edge0-145b-frontier-ai-capabilities-on-your-own-computer) |
| [Decision models](TRENDS.md#id-decision-models-024-system-1-decision-models-single-forward-pass-calibrated-classifiers-as-a-distinct-benchmarked-model-category) | 📈 accelerating | [2026-11-12](https://arxiv.org/abs/2611.16321) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-11-11](https://huggingface.co/blog/qvac/botpsy) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-11](https://arxiv.org/abs/2611.10649) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-11-10](https://blog.modelcontextprotocol.io/posts/exploring-file-uploads-and-downloads-in-mcp/) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 📈 accelerating | [2026-11-09](https://aaif.io/blog/when-good-agents-make-bad-systems) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-11-06](https://huggingface.co/blog/allenai/toyblocks) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-11-03](https://arxiv.org/abs/2611.04671) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-11-02](https://developer.nvidia.com/blog/build-world-models-for-interactive-simulation-with-nvidia-cosmos/) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-12](https://arxiv.org/abs/2611.17309) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-11-09](https://arxiv.org/abs/2611.12587) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08390) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05129) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-11-03](https://www.fireblocks.com/?p=32426) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-11-02](https://openai.com/index/lifeval/) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-11-02](https://rikiyat.github.io/blog/weight-space-programming/) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-11-13](https://blog.cloudflare.com/adapting-to-ai-penetration-testing-orchestrators/) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-11-10](https://deepmind.google/blog/introducing-alphaproof-code/) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-11-10](https://arxiv.org/abs/2611.14320) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-11-05](https://ernie.baidu.com/release/ernie-5-5-flash-base/) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-30](https://huggingface.co/Diffuspace/Clover-35B-A3B-Preview) |

## Worth studying

- [Advancing science & engineering with Antigravity's /teamwork](https://research.google/blog/advancing-science-engineering-with-antigravitys-teamwork-feature/) — a dense, cross-domain accounting of what a verified multi-agent team produces (Lean-checked proofs, a 95%-accurate chemistry pipeline, 60-90x graph throughput, Rust rewrites, scheduler tuning), each result checked by an automated verifier.
- [llama.cpp v1.0.0: A stronger foundation for the local AI ecosystem](https://huggingface.co/blog/ggml-org/llama-cpp-v1) — the local-inference substrate most of the small/CPU-model ecosystem builds on adopts semantic versioning and expands its CI/distribution footprint across six major hardware vendors.
- [A Lean Proof of the Thomson Problem for Seven Electrons](https://www.vals.ai/blogs/thomson-n7-lean-proof) — ten Claude Sonnet 5.5 agents produced a 17,895-line, two-kernel-verified Lean proof in ~15 hours, extending a prior N=8 proof to the next case.
- [LLMON: An LLM-Native Markup Language](https://huggingface.co/blog/ibm-granite/llmon-an-llm-native-markup-language-now-in-granite) — a reserved-token markup that keeps context structure in a separate part of the vocabulary than content, so injected text can't fake a boundary.
- [Top Chinese Frontier AI Models Carry the Fingerprint of Export-Controlled NVIDIA Blackwell GPUs](https://unemploymentlabs.com/checkpoint-forensics) — recovers a model's training-hardware fingerprint directly from its own published weights, confirmed on physical chips for two of six models.
- [My AI Agents Found an Unmapped Maya Site](https://pietromiotti.com/latest/maya-site) — a first-hand diary of 48 agents triaging public lidar strips with no classifier, flagging a real unregistered archaeological site.
- [Decision Models in Hugging Face](https://huggingface.co/blog/decision) — a concise introduction to a model category every practitioner building routing/classification/guardrail logic should know.
- [Introducing AlphaProof Code](https://deepmind.google/blog/introducing-alphaproof-code/) — a multi-LLM agentic framework that formally verified Signal's cryptographic protocol down to compiled-code depth (6M+ lines of machine-checked Lean) in four weeks, a task that historically took expert teams years.
- [After 7-months, Glasswing Overwhelms Maintainers with Underwhelming Findings](https://www.vulncheck.com/blog/anthropic-glasswing-november-update) — an independent security vendor's skeptical, numbers-first audit of a frontier lab's own AI-vulnerability-discovery claims, a template for reading any adoption claim against independently-tracked ground truth.
- [A proof of the Aaronson-Ambainis conjecture](https://psi.inc/research/aaronson-ambainis) — a case study in what mechanically-verified AI-driven math research actually looks like end to end: Lean proof, two independent kernels, a deliberately-false control case, and a third-party replay.
- [llama-modchip v2.3.0](https://github.com/synchopate/llama-modchip) — fits a 284B-parameter frontier MoE inside 64GB of CPU RAM at 256K context with zero GPUs, via Hessian-weighted 2-bit quantization and AVX-512 kernels.
- [Scientist World: Grow a Research World for AI-Scientists](https://arxiv.org/abs/2611.08478) — turns 1,000 research papers into executable, verifiable environments where an AI-Scientist is graded against what the human authors actually achieved.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- Alibaba previewed [Qwen4-Max](https://qwen.ai/blog?id=qwen4-max) with a claimed 62% agent-task cost cut, but no open weights or published benchmark table yet.
- A research-platform claim that [one prompt can command six coding agents at once](https://alphasignal.ai/news) drew attention via AlphaSignal.
- A video of [Claude Code and Codex reverse-engineering a 1994 Jeep's ECU](https://www.youtube.com/watch?v=WPj3aQ-xxpI) over a $3 Arduino circulated widely on Hacker News.
- A survey naming "agentic robotics" as the paradigm where [harnessed foundation models now match task-specific robot policies](https://arxiv.org/abs/2611.18359) was the day's top Hugging Face paper.
- An academic claim of [32x on-device model compression without losing accuracy](https://alphasignal.ai/news) surfaced via AlphaSignal.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~8 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-16.md)) · weekly: [latest](reports/weekly/2026-W46.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
