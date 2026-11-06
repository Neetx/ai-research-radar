# AI Radar

![trends](https://img.shields.io/badge/trends-23-3266ad?style=flat-square)
![accelerating](https://img.shields.io/badge/accelerating-10-e8590c?style=flat-square)
![watchlist](https://img.shields.io/badge/watchlist-6-6c757d?style=flat-square)
![updated](https://img.shields.io/badge/updated-2026--11--06-2f9e44?style=flat-square)

Tracks AI-ecosystem trends (research + engineering) and curates a study shelf for an AI researcher / AI-systems engineer who works with AI daily — generated from [TRENDS.md](TRENDS.md).

**Since last scan (2026-11-05):** [Agent security](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) added a [production email-leak incident in Claude Code itself](https://github.com/anthropics/claude-code/issues/107757) and OpenAI's [GPT‑6 Cyber](https://openai.com/index/introducing-gpt-6-cyber) model, which already found and fixed 81 Firefox 0-days · [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) added Baidu's [ERNIE 5.5 Flash Base open weights](https://ernie.baidu.com/release/ernie-5-5-flash-base/), a previously-untracked lab · [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) added [SCALE](https://arxiv.org/abs/2611.08390), the first to move this axis into real-time cyber-physical/robotics constraints · [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) added vLLM's [day-0 Kimi K3.1 Pro serving post](https://vllm.ai/blog/2026-11-04-kimi-k31-pro), with token-sharded prefill and decode-context-parallelism.

## ⭐ Pinned topics

| trend | stage | latest signal |
|---|---|---|
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08390) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05150) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-03](https://arxiv.org/abs/2611.04382) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-04](https://github.com/ggml-org/llama.cpp/releases/tag/v0.9.0) |

## Trends

🌱 8 · 📈 10 · 🚀 0 · 🌊 0 · 🏔 5 · 📉 0 · 💤 0

| trend | stage | latest signal |
|---|---|---|
| [Prefill/decode disaggregation](TRENDS.md#id-pd-disagg-002-prefilldecode-disaggregation-as-the-standard-llm-serving-architecture) | 📈 accelerating | [2026-11-04](https://vllm.ai/blog/2026-11-04-kimi-k31-pro) |
| ⭐ [Small / CPU-first models](TRENDS.md#id-small-cpu-models-008-small-and-1-bit-models-cpu-first-and-on-device-inference) | 📈 accelerating | [2026-11-04](https://github.com/ggml-org/llama.cpp/releases/tag/v0.9.0) |
| ⭐ [Ultra-low-bit quantization](TRENDS.md#id-lowbit-quant-011-ultra-low-bit-quantization-vector-and-trellis-coding-for-weights-and-kv-cache) | 📈 accelerating | [2026-11-03](https://arxiv.org/abs/2611.04382) |
| [Subquadratic/sparse attention](TRENDS.md#id-subquad-attn-012-subquadratic-and-sparse-attention-reaches-frontier-open-weight-models) | 📈 accelerating | [2026-11-03](https://arxiv.org/abs/2611.04671) |
| [World/action models from video](TRENDS.md#id-world-action-models-020-learned-worldaction-models-from-video-as-a-substrate-for-embodied-and-open-ended-agent-generalization) | 📈 accelerating | [2026-11-02](https://developer.nvidia.com/blog/build-world-models-for-interactive-simulation-with-nvidia-cosmos/) |
| [Multi-agent engineering as product](TRENDS.md#id-multi-agent-eng-009-multi-agent-engineering-becomes-product-surface-teams-workflows-a2a) | 📈 accelerating | [2026-10-29](https://cursor.com/blog/agent-sdk) |
| [MCP as the standard integration layer](TRENDS.md#id-mcp-standard-001-mcp-as-the-standard-integration-layer-for-agents-stateless-core-apps-tasks) | 📈 accelerating | [2026-10-22](https://www.anthropic.com/news/donating-agent-skills-to-the-agentic-ai-foundation) |
| [Verifiable RL environments](TRENDS.md#id-rl-env-005-verifiable-rl-environments-as-an-infrastructure-category-for-agent-training) | 📈 accelerating | [2026-10-22](https://huggingface.co/blog/microsoft/thinkingbox-training) |
| [On-policy distillation](TRENDS.md#id-on-policy-distill-016-on-policy-distillation-as-the-post-training-method-for-reasoning-and-agentic-llms) | 📈 accelerating | [2026-10-22](https://arxiv.org/abs/2610.31563) |
| [Remote sandboxes for agents](TRENDS.md#id-agent-sandbox-007-remote-sandboxes-as-the-execution-layer-for-agents) | 📈 accelerating | [2026-10-22](https://cloud.google.com/blog/topics/ai-infrastructure/introducing-agent-compute-engine-and-expanded-agent-governance) |
| ⭐ [Latent-space communication](TRENDS.md#id-latent-comm-010-latent-space-communication-between-models-cache-to-cache-latent-collaboration) | 🌱 emerging | [2026-11-05](https://arxiv.org/abs/2611.08390) |
| ⭐ [Latent-space reasoning](TRENDS.md#id-latent-reasoning-006-latent-space-reasoning-and-recursive-computation-looped-models-latent-multi-agent) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05150) |
| [VLM-scaffolded embodied navigation](TRENDS.md#id-embodied-nav-021-vlm-scaffolded-generalist-embodied-navigation-policies) | 🌱 emerging | [2026-11-03](https://arxiv.org/abs/2611.05129) |
| [Deployment-grounded agent eval](TRENDS.md#id-agent-eval-014-deployment-grounded-agent-evaluation-long-horizon-real-session-benchmarks-beyond-static-leaderboards) | 🌱 emerging | [2026-11-02](https://openai.com/index/lifeval/) |
| [Parametric injection](TRENDS.md#id-parametric-injection-018-parametric-injection-compiling-behavior-and-knowledge-into-model-weights-instead-of-promptcontext) | 🌱 emerging | [2026-11-02](https://rikiyat.github.io/blog/weight-space-programming/) |
| [Dense credit assignment for agentic RL](TRENDS.md#id-agentic-rl-credit-017-dense-credit-assignment-and-process-supervision-for-long-horizon-agentic-rl-beyond-sparse-outcome-rewards) | 🌱 emerging | [2026-10-29](https://arxiv.org/abs/2610.35013) |
| [Decentralized multi-agent coordination](TRENDS.md#id-decentralized-mas-022-decentralized-multi-agent-coordination-without-a-central-orchestrator) | 🌱 emerging | [2026-10-24](https://github.com/microsoft/Agensh) |
| [Agent payments (x402)](TRENDS.md#id-agent-payments-023-agent-payments-http-402-based-machine-to-machine-micropayment-infrastructure) | 🌱 emerging | [2026-10-20](https://www.mastercard.com/us/en/news-and-trends/press/2026/october/Mastercard-Agent-Pay-for-Machines-in-action.html) |
| [Open-weight frontier MoE wave](TRENDS.md#id-open-weight-003-open-weight-wave-frontier-scale-moe-released-at-high-cadence-across-labs) | 🏔 mainstreaming | [2026-11-05](https://ernie.baidu.com/release/ernie-5-5-flash-base/) |
| [Agent security: architectural turn](TRENDS.md#id-agent-security-004-agent-security-formal-limits-of-prompt-injection-defenses-and-the-architectural-turn) | 🏔 mainstreaming | [2026-11-05](https://github.com/anthropics/claude-code/issues/107757) |
| [Agent harness/runtime as self-improving object](TRENDS.md#id-agent-runtime-015-agent-harnessruntimememory-as-a-first-class-engineered-self-improving-object) | 🏔 mainstreaming | [2026-11-04](https://developer.nvidia.com/blog/use-nvidia-nemo-to-turn-agent-failures-into-tests-and-harness-fixes/) |
| [AI agents doing open-ended research](TRENDS.md#id-agentic-ai-research-019-ai-agents-conducting-open-ended-aiscientific-research-measuring-and-building-for-autonomous-discovery) | 🏔 mainstreaming | [2026-11-03](https://deepmind.google/blog/agentic-cheminformatics-with-google-antigravity) |
| [Diffusion language models](TRENDS.md#id-diffusion-lm-013-diffusion-language-models-reach-open-weights-production-scale) | 🏔 mainstreaming | [2026-10-30](https://huggingface.co/Diffuspace/Clover-35B-A3B-Preview) |

## Worth studying

- [GPT‑6 Cyber: Advancing the frontier of aligned cybersecurity agents](https://openai.com/index/introducing-gpt-6-cyber) — a named model release with quantified capability AND alignment gains, already fixing 81 real Firefox 0-days with patches Mozilla has shipped.
- [Agents aren't humans (but they kinda are)](https://blog.cloudflare.com/trusted-agent-delegation/) — Cloudflare's proposal for cryptographic agent identity/delegation on the open web, launching an IETF-track coalition — worth knowing before it's a de facto standard.
- [A thousand fewer paths to root](https://openai.com/index/a-thousand-fewer-paths-to-root/) — an autonomous Linux-kernel vulnerability-discovery/exploitation/patching pipeline that validated and patched 948 real bugs in one run, and a concrete dual-use capability benchmark in its own right.
- [Use NVIDIA NeMo to Turn Agent Failures into Tests and Harness Fixes](https://developer.nvidia.com/blog/use-nvidia-nemo-to-turn-agent-failures-into-tests-and-harness-fixes/) — a reproducible trace→eval→harness-fix optimization loop with a held-out generalization check, a template for self-improving agent harnesses.
- [Agensh: A Decentralized, Scalable Multiagent Harness](https://github.com/microsoft/Agensh) — Microsoft Research's open-source harness scaling self-organized coding-agent teams to 1,024 workers with no central orchestrator.
- [The "Astra can read and write weights to improve Qwen" post is misleading](https://honnibal.dev/blog/astra-read-write-misleading) — a careful, specific critique of a viral AI-capability claim, showing which parts were genuine raw-weight reading versus ordinary tool use.
- [Sparks of Weight-Space Programming](https://rikiyat.github.io/blog/weight-space-programming/) — an LLM reasoning directly over another model's raw weights (no gradient descent) to find and fix a specific failure, with a live demo and full experiment logs.
- [Introducing Agent Compute Engine](https://cloud.google.com/blog/topics/ai-infrastructure/introducing-agent-compute-engine-and-expanded-agent-governance) — a clear technical walkthrough of per-agent microVM isolation (Titanium IPU, copy-on-write templates, checkpoint/resume), a reference design for agent-sandboxing infrastructure.
- [Do the math: How we took over ChatGPT accounts](https://www.parameter.ai/labs/we-found-a-gap-at-openai) — a chained XSS/sandbox-escape (a math-rendering widget's own `postMessage` listener → an unsandboxed iframe → a CSP bypass via YouTube's oEmbed endpoint) that turned a sandboxed UI feature into a full account takeover on mere click.
- [ForkPilot](https://arxiv.org/abs/2610.04889) — a rigorously-benchmarked answer to when a long-horizon agent should backtrack a decision, tested against a production harness with hundreds of thousands of paid users.
- [How we detect frontier model misalignment](https://openai.com/index/how-we-detect-frontier-model-misalignment) — OpenAI's full disclosed monitoring stack (activation probes → CoT-reading reviewer → human investigators → automated telemetry cross-check), red-teamed by METR/Redwood Research for three weeks.
- [We're releasing the weights of Mistral Large 4](https://mistral.ai/news/mistral-large-4-oss/) — the first Western lab to ship a frontier-scale open-weight model combining Multi-head Latent Attention with a DeepSeek-Sparse-Attention-style indexer at ~1T total/~50B active parameters.

## Community pulse

Unverified intake, not evidence — link only, no individuals named:

- Today's HN discussion centers on an [AI coding agent sending a user's email address to third-party sites](https://github.com/anthropics/claude-code/issues/107757) without consent, fixed same-day.
- A [newly-opened lab](https://ernie.baidu.com/release/ernie-5-5-flash-base/) shipped a frontier-scale open-weight model with self-reported benchmarks beating an established rival.
- A web-infrastructure vendor is [proposing a cryptographic identity standard](https://blog.cloudflare.com/trusted-agent-delegation/) for AI agents acting on behalf of users across the open web.
- An independent evaluator reported that an open-weight model [turned disclosed-but-unpatched browser security fixes into working exploits](https://epoch.ai/publications/ai-can-turn-security-fixes-into-working-exploits-before-users-receive-an-update) within days, cheaply.
- A previously-untracked robotics lab proposed [real-time latent-state communication between physical agents](https://arxiv.org/abs/2611.08390) under bandwidth and deadline constraints.

## Output map

[Full ledger](TRENDS.md) · [watchlist (~6 items)](TRENDS.md#observation_queue) · [reports](reports/) ([latest daily](reports/2026-11-06.md)) · weekly: [latest](reports/weekly/2026-W44.md) · [agent guide](AGENTS.md) · [sources registry](SOURCES.md)
