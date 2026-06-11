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
- notes: Three independent groups converge on the same conclusion: filters/wrappers are not enough and security must move into the architecture (least privilege, sandboxing, design patterns). The impossibility results (May 2026) are the strongest recent signal. Watch: vendor reactions (platform-level defenses) and advisories on real agent vulnerabilities in production.

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

## observation_queue
Signals not yet promoted to seed. Format: date — description — link if available.
- 2026-06-11 — "MiniMax M3" (frontier coding + 1M context + native multimodality) cited by aggregators as a June 2026 release, but NOT present on the MiniMaxAI Hugging Face org page as of today — unverified, check MiniMax official channels
- 2026-06-11 — vendor report "Stacklok State of MCP in Software 2026" reportedly claims 41–45% production MCP use — unverified (source not opened), find the original report
- 2026-06-11 — paper "Not All Prefills Are Equal: PPD Disaggregation for Multi-turn LLM Serving" (arXiv 2603.13358): disaggregation pushed beyond the prefill/decode pair for multi-turn — unverified (not opened)
- 2026-06-11 — "GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators" (arXiv 2512.19682): environment generation itself becomes a training target — unverified (not opened)
- 2026-06-11 — series of real agent vulnerabilities disclosed in Q1 2026 (EchoLeak, GeminiJack, Reprompt…) cited only by secondary sources — unverified, trace the original advisories

## source_rotation
Log of which sources were covered on which dates.
- 2026-06-11 — blog.modelcontextprotocol.io; openai.github.io/openai-agents-python (OpenAI Agents SDK docs); adk.dev (Google ADK docs); docs.vllm.ai; docs.sglang.io; github.com/ai-dynamo/dynamo; huggingface.co (orgs: deepseek-ai, moonshotai, Qwen, MiniMaxAI, zai-org); arxiv.org (2605.17634, 2604.06436, 2506.08837, 2603.18815, 2604.27859); bugcrowd.com (press release); primeintellect.ai (blog). Attempted lmsys.org/blog: index not readable via fetch (JS rendering) — use direct post URLs for SGLang/LMSYS posts.

## strategy_notes
Corrections to the source-coverage strategy.
