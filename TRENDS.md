# Trend ledger — AI Radar
Last updated: 2026-06-12

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
- notes: Research-side trend with direct engineering implications: token costs and latency drop when reasoning/inter-agent communication stays in hidden states. The multi-agent variant (latent state transfer instead of token messages) is the newest twist and bridges to multi-agent-eng-009 and latent-comm-010 (which tracks the cross-model communication line specifically). Foundational anchors not re-verified here: COCONUT (Meta), Huginn, Ouro looped models. Watch: independent reproductions of RecursiveMAS numbers, and whether any open-weight release ships looped/latent reasoning natively.

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
- notes: Two converging threads: (a) extreme quantization (ternary weights, QAT releases) making CPU/edge inference viable; (b) sub-4B models engineered as first-class products (Gemma E-series, SmolLM). llama.cpp is the ecosystem hub where both land. Honest caveat: no ternary checkpoint above ~2.4B exists publicly — "100B on CPU" claims are kernel benchmarks, not downloadable models. Cross-link: lowbit-quant-011 tracks the quantization research line feeding this trend. Watch: larger ternary checkpoints, Gemma 4 E-series adoption, SmolLM4 signals.

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
- notes: Orchestration is moving from libraries into first-party product surface: a converged enterprise framework (Microsoft), a built-in orchestrator in a mainstream coding agent (Claude Code Agent Teams), and a vendor-neutral inter-agent protocol at 1.0 (A2A). Complementary to mcp-standard-001: MCP = agent↔tools, A2A = agent↔agent. Research bridge: latent-reasoning-006 and latent-comm-010 explore replacing token-based agent messaging entirely. Watch: Agent Framework GA, Agent Teams exiting experimental, A2A v1.0 implementations.

### [id: latent-comm-010] Latent-space communication between models (cache-to-cache, latent collaboration)
- alias: latent communication, C2C, KV-cache fusion, LatentMAS, model-to-model semantic transfer, Interlat
- stage: emerging
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-05
- evidence:
  - 2026-04-02 — https://arxiv.org/abs/2604.02029 — "The Latent Space: Foundation, Evolution, Mechanism, Ability, and Outlook" (Yu, Chen, He et al., 39 authors; v2 on 2026-06-05): community survey systematizing latent-space work, including latent communication as a new paradigm for multi-agent systems
  - 2026-02-17 — https://arxiv.org/abs/2602.15382 — Liu, Zhang, Yu, Xiong et al., "The Vision Wormhole: Latent-Space Communication in Heterogeneous Multi-Agent Systems" (v2 2026-05-28, preprint/WIP): extends latent communication to heterogeneous agents including vision models
  - 2025-11-25 — https://arxiv.org/abs/2511.20639 — Zou, Qiu, Li, Yang et al. (13 authors), "Latent Collaboration in Multi-Agent Systems" (LatentMAS; v2 2026-06-01): agent collaboration entirely through latent representations; code at github.com/Gen-Verse/LatentMAS (linked from the abs page)
  - 2025-11-12 — https://arxiv.org/abs/2511.09149 — Du, Wang, Bai, Cao, Zhu, Cheng, Zheng, Chen, Ying, "Enabling Agents to Communicate Entirely in Latent Space" (Interlat; v4 2026-04-16, accepted to ACL 2026): inter-agent communication carried by last hidden states instead of text — a distinct (Alibaba/Zhejiang-line) cluster from C2C, Vision Wormhole and Gen-Verse
  - 2025-10-03 — https://arxiv.org/abs/2510.03215 — Fu, Min, Zhang, Yan et al., "Cache-to-Cache: Direct Semantic Communication Between Large Language Models" (published at ICLR'26; v2 2026-03-02): project and fuse the source model's KV-cache into the target's with learned gating, beating text-based communication on both accuracy and latency
- notes: Companion to latent-reasoning-006: there the hidden states stay inside one model, here they cross model boundaries (KV-cache fusion, latent message passing). Independence check: C2C (Tsinghua-line), Vision Wormhole, the Gen-Verse group (LatentMAS, shares authors with RecursiveMAS) and now Interlat (Alibaba/Zhejiang-line) are four distinct clusters; the survey shares one author with C2C but spans 39 contributors. Two peer-reviewed acceptances now anchor the line: C2C at ICLR'26 and Interlat at ACL 2026. Watch: standardization of cross-model latent interfaces, first MAS framework shipping latent channels.

### [id: lowbit-quant-011] Ultra-low-bit quantization: vector and trellis coding for weights and KV cache
- alias: TCQ, trellis-coded quantization, QTIP, TurboQuant, EXL3, vector quantization, KV-cache quantization
- stage: accelerating
- confidence: medium
- first_observed: 2026-06-11
- last_evidence: 2026-06-12
- evidence:
  - 2026-06-12 — https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant — official vLLM API docs: an in-tree `turboquant` KV-cache quantization module (Hadamard rotation + per-coordinate Lloyd-Max scalar quant for keys, uniform for values), explicitly tracing the method to TurboQuant (ICLR 2026) / DRIVE / EDEN (accessed today)
  - 2026-06-11 — https://github.com/turboderp-org/exllamav3 — ExLlamaV3: the EXL3 format is a simplified variant of Cornell RelaxML's QTIP running in a production consumer-GPU inference library; v0.0.40 released June 2026, 938 stars, a 70B quantizes in hours on one RTX 4090 (accessed today)
  - 2026-04-27 — https://arxiv.org/abs/2605.08114 — D'Alberto, "Statistical Inference and Quality Measures of KV Cache Quantisations Inspired by TurboQuant": independent statistical analysis of TurboQuant-class KV quantization (inner-product variance, softmax effects)
  - 2025-09-24 — https://arxiv.org/abs/2509.20214 — Lee & Song (SNU), "Q-Palette: Fractional-Bit Quantizers Toward Optimal Bit Allocation" (NeurIPS 2025): fractional-bit quantizers with trellis-coded quantizers among the tools, plus joint quantizer/fusion optimization with CUDA kernels
  - 2025-04-28 — https://arxiv.org/abs/2504.19874 — Zandieh, Daliri, Hadian, Mirrokni, "TurboQuant: Online Vector Quantization with Near-optimal Distortion Rate": data-oblivious online VQ (rotation + 1-bit QJL residual); KV cache quality-neutral at 3.5 bits/channel, marginal loss at 2.5
  - 2024-06-17 — https://arxiv.org/abs/2406.11235 — Tseng, Sun, Hou, De Sa (Cornell), "QTIP: Quantization with Trellises and Incoherence Processing" (NeurIPS 2024 Spotlight; last revised 2025-06-18): TCQ with a stateful decoder and hardware-friendly "bitshift trellis" decouples codebook size from bitrate, enabling ultra-high-dimensional quantization
- notes: A coherent research-to-engineering line: QTIP (2024, trellis coding for weights) → TurboQuant (2025, online VQ for KV cache) → 2026 independent analyses and production implementations. Stage → accelerating: vector/trellis quant is now in two independent production serving stacks — EXL3 (weights, ExLlamaV3) and a `turboquant` KV-cache module in vLLM itself — i.e. the "landing in mainstream engines" watch item has fired. A community ik_llama.cpp port (issue #1509, CPU done / CUDA pending) is in review but not merged, so treat it as a weaker signal. Feeds small-cpu-models-008 (extreme quantization is what makes CPU/edge viable). Watch: vLLM turboquant leaving API-only docs for a benchmarked release, KV-cache VQ at serving scale, fractional-bit allocation.

## observation_queue
Signals not yet promoted to seed. Format: date — description — link if available.
- 2026-06-12 — "MiniMax M3" (frontier coding + 1M context + native multimodality) still cited only by aggregators; rechecked the MiniMaxAI Hugging Face org page today — latest open weights are MiniMax-M2.7, no M3 — unverified, no official open-weight release yet
- 2026-06-12 — MiniMaxAI shipped VTP visual tokenizers (VTP-Small/Base/Large, "Towards Scalable Pre-training of Visual Tokenizers for Generation") on the HF org page — single org / single artifact, below the trend bar; watch if other labs pursue scalable visual tokenizers
- 2026-06-11 — vendor report "Stacklok State of MCP in Software 2026" reportedly claims 41–45% production MCP use — unverified (source not opened), find the original report
- 2026-06-11 — paper "Not All Prefills Are Equal: PPD Disaggregation for Multi-turn LLM Serving" (arXiv 2603.13358): disaggregation pushed beyond the prefill/decode pair for multi-turn — unverified (not opened)
- 2026-06-11 — "GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators" (arXiv 2512.19682): environment generation itself becomes a training target — unverified (not opened)
- 2026-06-11 — series of real agent vulnerabilities disclosed in Q1 2026 (EchoLeak, GeminiJack, Reprompt…) cited only by secondary sources — unverified, trace the original advisories
- 2026-06-11 — "loop engineering" circulating as a practitioner term: designing agent loops (trigger + verifiable goal + stopping conditions as first-class concerns) instead of hand-prompting; found only on vendor/creator blogs and an Oracle dev blog, no lab/primary anchor — unverified; watch whether a framework or lab adopts the term
- 2026-06-12 — ik_llama.cpp TurboQuant KV-cache port (issue #1509): community implementation, CPU complete (18/18 tests, ~4.9× compression at 3 bits/value), CUDA kernels awaiting GPU validation, not merged — verified but weak (single contributor, in review); the vLLM in-tree `turboquant` module was promoted to lowbit-quant-011 today
- 2026-06-11 — "Sequential KV Cache Compression via Probabilistic Language Tries: Beyond the Per-Vector Shannon Limit" (arXiv 2604.15356) — unverified (not opened)

## source_rotation
Log of which sources were covered on which dates.
- 2026-06-11 — blog.modelcontextprotocol.io; openai.github.io/openai-agents-python (OpenAI Agents SDK docs); adk.dev (Google ADK docs); docs.vllm.ai; docs.sglang.io; github.com/ai-dynamo/dynamo; huggingface.co (orgs: deepseek-ai, moonshotai, Qwen, MiniMaxAI, zai-org); arxiv.org (2605.17634, 2604.06436, 2506.08837, 2603.18815, 2604.27859); bugcrowd.com (press release); primeintellect.ai (blog). Attempted lmsys.org/blog: index not readable via fetch (JS rendering) — use direct post URLs for SGLang/LMSYS posts.
- 2026-06-11 (second pass) — arxiv.org (2604.25917, 2602.10520, 2507.06203); github.com (RecursiveMAS/RecursiveMAS, microsoft/BitNet, ggml-org/llama.cpp); e2b.dev; daytona.io; developers.cloudflare.com/sandbox; modal.com/docs; huggingface.co/HuggingFaceTB; deepmind.google/models/gemma (ai.google.dev/gemma redirects here); learn.microsoft.com/agent-framework; code.claude.com/docs (agent teams); a2a-protocol.org/latest; ai.meta.com/blog (index only).
- 2026-06-11 (third pass) — arxiv.org abs pages 2406.11235, 2504.19874, 2605.08114, 2509.20214 (direct) and 2604.02029, 2510.03215, 2511.20639, 2602.15382 (via extraction API, metadata cross-checked on export.arxiv.org); github.com/turboderp-org/exllamav3.
- 2026-06-12 — arxiv.org/abs/2511.09149 (Interlat) + export.arxiv.org metadata (2511.09149, 2604.15356); ai.meta.com/blog (Muse Spark post, read in full); docs.vllm.ai (turboquant module API docs); github.com/ikawrakow/ik_llama.cpp (issue #1509); huggingface.co/MiniMaxAI (org page recheck). Tavily search surfaced mostly SEO/comparator results for serving engines and open-weight news — none citable; verified via primary pages only.

## strategy_notes
Corrections to the source-coverage strategy.
- 2026-06-11 — Scope priorities (curator input): (1) frontier research likely to reach engineering later — math, new architectures, latent-space/recursive computation; (2) AI engineering — inference/serving engines (vLLM, SGLang, and the llama.cpp ecosystem) and deployment practice; (3) small models — CPU-first, 1-bit/ternary, sub-4B on-device; (4) agent infrastructure — remote sandboxes/workspaces, multi-agent engineering, agent-loop design. Keep covering the original axes (MCP/tool use, agent security, open-weight, post-training/RL, evals, multimodal). Anchor product categories on vendor docs and repos; never SEO or comparator sites.
- 2026-06-11 — Scope additions (curator input): (5) model compression research — vector/trellis-coded quantization (QTIP-class, TurboQuant) for weights and KV cache, tracked through to engine adoption; (6) latent-space communication between models (cache-to-cache, latent multi-agent collaboration), including surveys. Folded into the daily scan axes.
- 2026-06-12 — Anti-anchoring correction (curator input): every daily scan must reserve at least one of its 3–6 source families for venue-based exploration outside the ledger's current axes — browse listings (HF daily papers, rotating arXiv categories such as cs.AR/cs.RO/cs.CV/cs.DC/cs.SE, lab blog indexes) rather than searching known topics; log the exploration in source_rotation even when fruitless. Weekly runs flag any week where all new evidence landed on pre-existing trends and redirect exploration toward uncovered axes or venues.
- 2026-06-12 — Audience definition (curator input): the radar serves an AI researcher / AI-systems engineer / daily AI practitioner. Beyond trends, each daily scan may select 0–2 "study picks" into the `study_shelf` section below — projects, papers, techniques or tools worth studying; single-artifact items allowed there (trend bar does not apply), opened primary sources only.

## study_shelf
Things worth studying for an AI researcher / AI-systems engineer / daily AI practitioner. Single strong artifacts qualify (the trend bar does not apply); opened primary sources only. Newest first; pruned weekly. Format: date — [name](url) — one line of why.
- 2026-06-12 — [vLLM `turboquant` module](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) — KV-cache vector quantization inside a mainstream serving engine; read next to the TurboQuant paper to see the research→production distance
- 2026-06-12 — [RecursiveMAS](https://github.com/RecursiveMAS/RecursiveMAS) — reference implementation of latent-space multi-agent computation, with checkpoints over Qwen/Llama/Gemma that make it reproducible on modest hardware
- 2026-06-12 — [Cache-to-Cache (C2C)](https://arxiv.org/abs/2510.03215) — the cleanest formulation of direct KV-cache communication between different LLMs (ICLR'26)
- 2026-06-12 — [ExLlamaV3 / EXL3](https://github.com/turboderp-org/exllamav3) — production trellis-coded quantization (QTIP-derived) on consumer GPUs; the format to study to understand where weight quantization is heading
- 2026-06-12 — [bitnet.cpp](https://github.com/microsoft/BitNet) — the official ternary-LLM inference stack; the practical entry point to 1-bit models on CPU
- 2026-06-12 — [Design Patterns for Securing LLM Agents](https://arxiv.org/abs/2506.08837) — the reference catalogue of injection-resistant agent architectures; required reading before building any tool-using agent
- 2026-06-12 — [Claude Code Agent Teams](https://code.claude.com/docs/en/agent-teams) — first mainstream built-in multi-agent orchestrator; the shared-task-list + mailbox architecture is a pattern worth studying regardless of vendor

## calibration
Self-evaluation log (append-only; see the radar-self-eval skill). Weekly line: `W<nn>: queue +added/→promoted/−dropped/stale n · evidence +n · moves n · exploration done/runs · off-axis n/added`. Monthly retro line: `retro M<mm>: <item> — HIT-early|HIT-late|MISS (first seen <date>)`.
- 2026-06-12 — baseline: 11 trends (3 accelerating, 8 emerging), queue 9, study_shelf 7; exploration-slot and tunnel-vision rules active since 2026-06-12; first weekly metrics due with the next weekly run, first monthly retrospective due with the first weekly run of July 2026.
