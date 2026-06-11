# Trend ledger — AI Radar
Last updated: 2026-06-11

Stage legend: seed | emerging | accelerating | mainstreaming | saturated |
declining | dormant (21 days without evidence; after 45 → ARCHIVE.md).
Confidence: low | medium | high.
Rule: max 10 evidence items per trend, most recent.

## Active trends

### [id: mcp-standard-001] MCP as the standard integration layer for agents (stateless core, Apps, Tasks)
- alias: Model Context Protocol, MCP Apps, Tasks extension, spec 2026-07-28
- stage: accelerating
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-11
- evidence:
  - 2026-05-21 — https://blog.modelcontextprotocol.io/posts/2026-07-28-release-candidate/ — release candidate of the 2026-07-28 spec (final on July 28): stateless core that scales on plain HTTP, MCP Apps (server-rendered UI in sandboxed iframes), Tasks promoted to official extension, six OAuth 2.0/OIDC hardening SEPs
  - 2026-03-09 — https://blog.modelcontextprotocol.io/posts/2026-mcp-roadmap/ — 2026 roadmap: transport scalability, Tasks primitive (retry/expiry), Working Group governance, enterprise readiness via extensions
  - 2026-06-11 — https://openai.github.io/openai-agents-python/mcp/ — official OpenAI Agents SDK docs: five MCP transports supported (hosted, streamable HTTP, deprecated SSE, stdio, server manager) with tool filtering and approvals (undated page, accessed today)
  - 2026-06-11 — https://adk.dev/tools-custom/mcp-tools/ — official Google ADK docs: McpToolset as client plus ADK exposed as MCP server, in Python/TypeScript/Java/Kotlin (undated page, accessed today)
- notes: Stage set to accelerating despite the conservative no-history rule (max emerging): adoption is documented in the official frameworks of at least three independent orgs (MCP project spec/SDKs, OpenAI Agents SDK, Google ADK). Clear 2026 direction: from local tool-wiring protocol to production infrastructure (stateless, OAuth, UI, long-running tasks). Watch: final spec publication on 2026-07-28 and Tier 1 SDK adoption speed.

### [id: pd-disagg-002] Prefill/decode disaggregation as the standard LLM serving architecture
- alias: PD disaggregation, disaggregated prefilling, disaggregated serving, KV transfer
- stage: accelerating
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-11
- evidence:
  - 2026-06-02 — https://github.com/ai-dynamo/dynamo — NVIDIA Dynamo v1.2.0: datacenter-scale orchestration layer with disaggregated serving as a core capability, on top of vLLM/SGLang/TensorRT-LLM; 7.2k stars
  - 2026-06-11 — https://docs.vllm.ai/en/latest/features/disagg_prefill.html — official vLLM docs: prefill and decode on separate instances with ~9 KV connectors (NIXL, LMCache, Mooncake, FlexKV…); still flagged experimental (accessed today)
  - 2026-06-11 — https://docs.sglang.io/advanced_features/pd_disaggregation.html — official SGLang docs: PD disaggregation with Mooncake, NIXL and Ascend transfer backends, single/multi-node deployment (accessed today)
- notes: Stage accelerating despite no velocity history: the feature is officially documented in the major serving frameworks (vLLM, SGLang) and NVIDIA built a dedicated product on it (Dynamo). Honest counterpoint: vLLM still marks it "experimental and subject to change". Watch: stabilization in vLLM and convergence on transfer engines (NIXL vs Mooncake).

### [id: open-weight-003] Open-weight wave: frontier-scale MoE released at high cadence by Chinese labs
- alias: open-weight frontier, DeepSeek V4, Kimi K2.6, GLM-5.x, MiniMax M2.x
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-08
- evidence:
  - 2026-06-08 — https://huggingface.co/deepseek-ai — DeepSeek-V4-Pro (862B) and DeepSeek-V4-Flash (158B) published/updated ~3 days ago (date estimated from "updated 3 days ago" on the org page)
  - 2026-05-19 — https://huggingface.co/moonshotai — Kimi-K2.6 (1.1T, image-text-to-text, i.e. multimodal) updated ~23 days ago; K2.5 on April 30 (dates estimated from the org page)
  - 2026-05-13 — https://huggingface.co/zai-org — GLM-5.1 (754B) updated ~29 days ago; GLM-5 on April 5 (dates estimated from the org page)
  - 2026-04-20 — https://huggingface.co/MiniMaxAI — MiniMax-M2.7 (229B), 2.52M downloads: the M2.x family iterates roughly monthly (M2 Dec 2025, M2.1 Feb, M2.5 Mar, M2.7 Apr)
- notes: Four labs (DeepSeek, Moonshot, Z.ai, MiniMax) shipped frontier-scale weights between April and June 2026, with cadence measured in weeks. Kept at emerging under the conservative rule: velocity still needs to be measured over time (only the releases were verified here, not adoption in serving frameworks). Licenses not yet checked on individual model cards. Caution on parameter counts reported by aggregators: for V4 the HF org page is authoritative (862B/158B).

### [id: agent-security-004] Agent security: formal limits of prompt-injection defenses and the architectural turn
- alias: prompt injection, indirect prompt injection, agent security, contextual integrity, defense wrappers
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-05-17
- evidence:
  - 2026-05-17 — https://arxiv.org/abs/2605.17634 — Abdelnabi & Bagdasarian, "AI Agents May Always Fall for Prompt Injections": impossibility result — an adversary can always construct a context where a blocked flow looks legitimate; reframed via Contextual Integrity
  - 2026-04-07 — https://arxiv.org/abs/2604.06436 — Bhatt et al., "The Defense Trilemma": continuity, utility preservation and completeness cannot coexist in a wrapper defense; formalized in Lean 4 and validated on three LLMs
  - 2025-06-10 — https://arxiv.org/abs/2506.08837 — Beurer-Kellner, Tramèr et al. (multi-org group), "Design Patterns for Securing LLM Agents against Prompt Injections": design patterns with resistance by construction, at a utility cost
- notes: Three independent groups converge on the same conclusion: filters/wrappers are not enough and security must move into the architecture (least privilege, sandboxing, design patterns). The impossibility results (May 2026) are the strongest recent signal. Cross-link: agent-sandbox-007 is the infrastructure side of this same conclusion. Watch: vendor reactions (platform-level defenses) and advisories on real agent vulnerabilities in production.

### [id: rl-env-005] Verifiable RL environments as an infrastructure category for agent training
- alias: RL environments, environments hub, rollout-as-a-service, agentic RL
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-05-21
- evidence:
  - 2026-05-21 — https://www.bugcrowd.com/press-release/bugcrowd-launches-reinforcement-learning-environments-to-help-ai-models-learn-real-world-security-skills/ — Bugcrowd launches "RL Environments" as a product: hundreds of thousands of environments built from real open-source vulnerabilities (Mayhem technology), already used by LLM providers
  - 2026-04-30 — https://arxiv.org/abs/2604.27859 — Cui et al., "Rethinking Agentic Reinforcement Learning in LLMs": survey systematizing the paradigm (autonomous goals, long-horizon planning, uncertain environments)
  - 2026-03-19 — https://arxiv.org/abs/2603.18815 — "ProRL Agent: Rollout-as-a-Service for RL Training of Multi-Turn LLM Agents" (NVIDIA group): the agentic rollout lifecycle as an API service with rootless sandboxes for HPC; open-sourced inside NeMo Gym
  - 2025-08-27 — https://www.primeintellect.ai/blog/environments — Prime Intellect's Environments Hub: open platform for sharing RL environments + the prime-rl trainer; 30+ contributors already in beta (Arcee, Hud.so, Groq…)
- notes: Environments with verifiable outcomes are becoming a market/category of their own (sold: Bugcrowd; federated: Prime Intellect; industrialized into training: NVIDIA). Emerging: the pieces are real but cross-lab adoption is not yet measurable from here. Watch: NeMo Gym, Environments Hub growth, possible standard interfaces between environments and trainers.

### [id: latent-reasoning-006] Latent-space reasoning and recursive computation (looped models, latent multi-agent)
- alias: latent reasoning, continuous thought, looped transformers, RecursiveMAS, latent collaboration, RLTT
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-04-28
- evidence:
  - 2026-04-28 — https://arxiv.org/abs/2604.25917 — "Recursive Multi-Agent Systems" (Yang, Zou, Pan et al., 12 authors): the whole multi-agent system cast as one recursive latent-space computation; the RecursiveLink module transfers last-layer hidden states between heterogeneous agents instead of text; +8.3% avg accuracy, 1.2–2.4× speedup, 34.6–75.6% token reduction on 9 benchmarks
  - 2026-04-28 — https://github.com/RecursiveMAS/RecursiveMAS — official implementation, 542 stars: checkpoints for Sequential/Mixture/Distillation/Deliberation collaboration styles over Qwen/Llama/Gemma agents, inference pipelines and eval utilities
  - 2026-02-11 — https://arxiv.org/abs/2602.10520 — Williams & Tureci, "Prioritize the Process, Not Just the Outcome": RLTT distributes RL credit along the latent thought trajectory of looped LMs, no external verifiers; +5.8% (1.4B) and +10.9% (2.6B) on math, transfers to non-math reasoning
  - 2025-07-08 — https://arxiv.org/abs/2507.06203 — Zhu et al. (33 authors), "A Survey on Latent Reasoning": systematizes the field — activation-based recurrence, hidden-state propagation, internalized CoT, up to infinite-depth latent reasoning via masked diffusion
- notes: Research-side trend with direct engineering implications: token costs and latency drop when reasoning/inter-agent communication stays in hidden states. The multi-agent variant (latent state transfer instead of token messages) is the newest twist and bridges to multi-agent-eng-009. Foundational anchors not re-verified here: COCONUT (Meta), Huginn, Ouro looped models. Watch: independent reproductions of RecursiveMAS numbers, and whether any open-weight release ships looped/latent reasoning natively.

### [id: agent-sandbox-007] Remote sandboxes as the execution layer for agents
- alias: agent sandboxes, code execution infrastructure, microVMs, ephemeral workspaces, remote agent workspaces
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-11
- evidence:
  - 2026-06-11 — https://e2b.dev/ — Firecracker microVM sandboxes for agent code execution, <200ms start, 24h sessions, Python/JS SDKs; vendor-reported: 1B+ sandboxes spawned, 3.5M monthly downloads, customers incl. Perplexity, Hugging Face, Manus, Groq (undated product page, accessed today)
  - 2026-06-11 — https://daytona.io/ — sandboxes with sub-90ms creation, SDKs for Python/TS/Ruby/Go/Java, process/filesystem/git/LSP APIs, dedicated per-customer compute (undated product page, accessed today)
  - 2026-06-11 — https://developers.cloudflare.com/sandbox/ — official Cloudflare Sandbox SDK docs: untrusted AI-generated code in isolated containers (full Linux env) on the Workers platform, TypeScript API (accessed today)
  - 2026-06-11 — https://modal.com/docs/guide/sandbox — official Modal docs: Sandboxes as "secure containers for executing untrusted user or agent code", explicit LLM-generated-code use case, CPU/memory/GPU provisioning (accessed today)
- notes: At least four independent vendors ship a dedicated product for the same primitive: spin up an isolated environment per agent task/turn (microVMs at E2B, containers at Cloudflare/Modal, fast-start runtimes at Daytona). Adoption numbers are vendor-reported — treat as upper bounds. This is the infrastructure counterpart of agent-security-004 (sandboxing as the architectural defense). Watch: which sandbox becomes the default in agent SDKs, GPU-in-sandbox support, pricing convergence.

### [id: small-cpu-models-008] Small and 1-bit models: CPU-first and on-device inference
- alias: SLM, BitNet, ternary models, bitnet.cpp, llama.cpp ecosystem, on-device AI, edge inference
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-11
- evidence:
  - 2026-06-11 — https://github.com/ggml-org/llama.cpp — release b9596 cut today, 116k stars; backends from Apple Silicon/CUDA/HIP/SYCL/Vulkan down to RISC-V; multimodal support in llama-server; MXFP4 format added in collaboration with NVIDIA
  - 2026-06-11 — https://deepmind.google/models/gemma — Gemma 4 family with E2B/E4B variants explicitly for mobile/IoT, plus 12B/26B/31B; Gemma 4 QAT (June 2026) for mobile/laptop efficiency; multi-token prediction drafters (May 2026); Gemma 3 270M as compact baseline (page accessed today)
  - 2026-01-15 — https://github.com/microsoft/BitNet — bitnet.cpp, official inference framework for 1-bit/ternary LLMs, 39.3k stars: Jan 2026 release adds parallel kernels (+1.15–2.1×) on top of 2.37–6.17× (x86) and 1.37–5.07× (ARM) speedups with 55–82% energy reduction; largest official ternary checkpoint is BitNet-b1.58-2B-4T
  - 2025-09-30 — https://huggingface.co/HuggingFaceTB — SmolLM3-3B ("SOTA 3B, dual reasoning, 6 languages, long context"), SmolLM2 down to 135M, SmolVLM2 down to 256M (dates approximated from the org page)
- notes: Two converging threads: (a) extreme quantization (ternary weights, QAT releases) making CPU/edge inference viable; (b) sub-4B models engineered as first-class products (Gemma E-series, SmolLM). llama.cpp is the ecosystem hub where both land. Honest caveat: no ternary checkpoint above ~2.4B exists publicly — "100B on CPU" claims are kernel benchmarks, not downloadable models. Watch: larger ternary checkpoints, Gemma 4 E-series adoption, SmolLM4 signals.

### [id: multi-agent-eng-009] Multi-agent engineering becomes product surface (teams, workflows, A2A)
- alias: subagents, agent teams, orchestrator/supervisor patterns, handoffs, Agent2Agent, A2A
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-11
- evidence:
  - 2026-06-11 — https://learn.microsoft.com/en-us/agent-framework/ — official Microsoft Agent Framework docs hub (updated today): graph workflows (executors/edges), A2A integration, DevUI, and migration guides from both AutoGen and Semantic Kernel — the two lines converged into one framework
  - 2026-06-11 — https://code.claude.com/docs/en/agent-teams — official Claude Code docs: Agent Teams (experimental, v2.1.32+) — a team lead plus teammates in separate context windows, shared task list with file-locked claiming, inter-agent mailbox, plan-approval gates, quality-gate hooks (accessed today)
  - 2026-06-11 — https://a2a-protocol.org/latest/ — A2A (Agent2Agent) protocol under the Linux Foundation (donated by Google), Apache 2.0, spec v1.0 announced; agent↔agent interop across LangGraph/CrewAI/Semantic Kernel, with ADK, Cisco agntcy and IBM ACP in the ecosystem (accessed today)
- notes: Orchestration is moving from libraries into first-party product surface: a converged enterprise framework (Microsoft), a built-in orchestrator in a mainstream coding agent (Claude Code Agent Teams), and a vendor-neutral inter-agent protocol at 1.0 (A2A). Complementary to mcp-standard-001: MCP = agent↔tools, A2A = agent↔agent. Research bridge: latent-reasoning-006 explores replacing token-based agent messaging entirely. Watch: Agent Framework GA, Agent Teams exiting experimental, A2A v1.0 implementations.

## observation_queue
Signals not yet promoted to seed. Format: date — description — link if available.
- 2026-06-11 — "MiniMax M3" (frontier coding + 1M context + native multimodality) cited by aggregators as a June 2026 release, but NOT present on the MiniMaxAI Hugging Face org page as of today — unverified, check MiniMax official channels
- 2026-06-11 — vendor report "Stacklok State of MCP in Software 2026" reportedly claims 41–45% production MCP use — unverified (source not opened), find the original report
- 2026-06-11 — paper "Not All Prefills Are Equal: PPD Disaggregation for Multi-turn LLM Serving" (arXiv 2603.13358): disaggregation pushed beyond the prefill/decode pair for multi-turn — unverified (not opened)
- 2026-06-11 — "GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators" (arXiv 2512.19682): environment generation itself becomes a training target — unverified (not opened)
- 2026-06-11 — series of real agent vulnerabilities disclosed in Q1 2026 (EchoLeak, GeminiJack, Reprompt…) cited only by secondary sources — unverified, trace the original advisories
- 2026-06-11 — "loop engineering" circulating as a practitioner term: designing agent loops (trigger + verifiable goal + stopping conditions as first-class concerns) instead of hand-prompting; found only on vendor/creator blogs and an Oracle dev blog, no lab/primary anchor — unverified; watch whether a framework or lab adopts the term
- 2026-06-11 — Meta announced "Muse Spark" on 2026-04-08 ("Scaling Towards Personal Superintelligence" — title seen on the official ai.meta.com/blog index, post not yet read); aggregators call it the Llama successor and some market-wire pieces mislabel it "Llama 5"; no Llama 5 entry on the official blog — read the post, check open-weight status of the Llama line

## source_rotation
Log of which sources were covered on which dates.
- 2026-06-11 — blog.modelcontextprotocol.io; openai.github.io/openai-agents-python (OpenAI Agents SDK docs); adk.dev (Google ADK docs); docs.vllm.ai; docs.sglang.io; github.com/ai-dynamo/dynamo; huggingface.co (orgs: deepseek-ai, moonshotai, Qwen, MiniMaxAI, zai-org); arxiv.org (2605.17634, 2604.06436, 2506.08837, 2603.18815, 2604.27859); bugcrowd.com (press release); primeintellect.ai (blog). Attempted lmsys.org/blog: index not readable via fetch (JS rendering) — use direct post URLs for SGLang/LMSYS posts.
- 2026-06-11 (second pass) — arxiv.org (2604.25917, 2602.10520, 2507.06203); github.com (RecursiveMAS/RecursiveMAS, microsoft/BitNet, ggml-org/llama.cpp); e2b.dev; daytona.io; developers.cloudflare.com/sandbox; modal.com/docs; huggingface.co/HuggingFaceTB; deepmind.google/models/gemma (ai.google.dev/gemma redirects here); learn.microsoft.com/agent-framework; code.claude.com/docs (agent teams); a2a-protocol.org/latest; ai.meta.com/blog (index only).

## strategy_notes
Corrections to the source-coverage strategy.
- 2026-06-11 — Scope priorities (curator input): (1) frontier research likely to reach engineering later — math, new architectures, latent-space/recursive computation; (2) AI engineering — inference/serving engines (vLLM, SGLang, and the llama.cpp ecosystem) and deployment practice; (3) small models — CPU-first, 1-bit/ternary, sub-4B on-device; (4) agent infrastructure — remote sandboxes/workspaces, multi-agent engineering, agent-loop design. Keep covering the original axes (MCP/tool use, agent security, open-weight, post-training/RL, evals, multimodal). Anchor product categories on vendor docs and repos; never SEO or comparator sites.
