# Sources registry — AI Radar

Agent-owned registry of monitored sources. The radar maintains and evolves this
file itself (add/remove/mark-dead entries, with a one-line reason in the day's
or week's report) — no curator sign-off needed. Skills describe the *method*;
this file is the *data*.

Hard-rule reminder: lab blogs and GitHub artifacts are PRIMARY sources (citable
evidence). Social/community sources are an INTAKE LANE ONLY — never evidence,
but they are a fast discovery channel: when a social signal links to or names a
primary artifact, follow the link and verify the artifact (that artifact, not
the post, becomes the evidence). See the `radar-pulse` skill and the social
carve-out in AGENTS.md.

The lists below are seeds; the agent should grow/prune them. Handles marked
`(verify)` must be confirmed to resolve on first use — fix or drop any that
don't, never assert an unverified handle as fact.

Source health: inline notes flag degraded entries (404, stale, empty, parse
error). These are not permanent — a source that fails the same way twice must be
repaired and its working method recorded here, per the `radar-source-heal`
skill. Don't leave a "degraded" note standing across runs.

---

## Lab & big-tech AI blogs (Phase 1 — swept EVERY run, prefer RSS/Atom)

Method: `radar-lab-sweep` skill. Open only posts newer than the last scan.

Big labs / vendors:
- OpenAI — https://openai.com/news/ (RSS https://openai.com/news/rss.xml — works; mostly business/policy, scan titles for model/open-weight items)
- Anthropic — https://www.anthropic.com/news (no public RSS as of 2026-06-13: /rss.xml and /news/rss both 404 — extract the HTML index via Tavily)
- Google DeepMind — https://deepmind.google/blog/rss.xml (RSS — confirmed working 2026-06-13; the old /discover/blog/ path is the HTML index)
- Google Research — https://research.google/blog/ (RSS)
- Meta AI — https://ai.meta.com/blog/ (the /blog/rss/ feed returned empty 2026-06-13 — find correct feed or extract HTML index)
- Microsoft Research — https://www.microsoft.com/en-us/research/blog/ (RSS); also Microsoft Security blog https://www.microsoft.com/en-us/security/blog/ for agent-security advisories
- NVIDIA — https://developer.nvidia.com/blog/ (RSS) + https://research.nvidia.com/
- Mistral — https://mistral.ai/news/
- Qwen — https://qwenlm.github.io/blog/ (RSS /index.xml STALE: newest post Sep 2025 as of 2026-06-13 — Qwen likely posts elsewhere now; verify qwen.ai + Qwen HF org instead)
- DeepSeek — https://api-docs.deepseek.com/news/ + deepseek-ai HF org
- Hugging Face — https://huggingface.co/blog (RSS /blog/feed.xml)
- Together AI — https://www.together.ai/blog
- Z.ai / GLM — https://z.ai/blog + zai-org HF org

Research labs / independents (agent: verify feeds on first sweep):
- Allen Institute (AI2) — https://allenai.org/blog + https://allenai.org/research
- EleutherAI — https://blog.eleuther.ai/ (RSS)
- Sakana AI — https://sakana.ai/blog/
- Nous Research — https://nousresearch.com/
- Berkeley AI Research (BAIR) — https://bair.berkeley.edu/blog/ (RSS)
- Stanford CRFM / Hazy Research — https://crfm.stanford.edu/ + https://hazyresearch.stanford.edu/blog
- PrismML — https://prismml.com/blog + https://prismml.com/news (Ternary Bonsai 1.58-bit family, Bonsai Image — directly on the small/CPU + low-bit axes)
- LMSYS / SGLang — https://lmsys.org/blog/ (use RSS, JS index fails extraction)
- Cohere — https://cohere.com/blog (RSS)

Hardware (technical only — coupled to the small/CPU, low-bit-quant and serving
axes; scan for capability changes, NOT chip-business/macro news. agent: verify
feeds on first sweep):
- NVIDIA technical blog — https://developer.nvidia.com/blog/ (also in big-labs above)
- Apple Machine Learning Research — https://machinelearning.apple.com/research (on-device / ANE / small models)
- AMD ROCm Blogs — https://rocm.blogs.amd.com/index.html (serving on non-CUDA)
- Modular (MAX / Mojo) — https://www.modular.com/blog (inference engine + HW abstraction)
- Qualcomm AI Research — https://www.qualcomm.com/developer/blog (edge NPU / on-device)
- Google Cloud TPU / JAX — via research.google + cloud.google.com/blog/products/ai-machine-learning
- Inference-chip startups (agent discretion — technical perf posts only, skip PR): Groq, Cerebras, SambaNova, Etched, Tenstorrent
- Venue: arXiv cs.AR is the standing exploration listing for hardware-aware serving / low-bit kernels (already yielded SPEAR, TileFuse)

## Social & community channels (Phase 2 — INTAKE ONLY, never evidence)

Method: `radar-pulse` skill. Best-effort via Tavily (no paid APIs / no secrets).
Log degradation when a platform can't be reached. Never quote individuals in
evidence/queue text — link the thread/profile, summarise. The watchlist of
profiles below is a discovery aid, not an endorsement.

Reddit (subreddits — verified active 2026-06-13; organized by axis so coverage
gaps are visible. Ensure every pinned axis has at least one channel):
- Local / small / CPU models + quant: r/LocalLLaMA (the canonical pulse), r/LocalLLM
- Research / papers: r/MachineLearning
- Agents / agentic engineering: r/AI_Agents, r/LLMDevs, r/LangChain
- MCP / tool use: r/mcp
- RAG / retrieval: r/RAG
- Multimodal / diffusion: r/StableDiffusion
- Serving/inference has no dedicated active sub — that discussion lives in r/LocalLLaMA
- (agent: add/prune by signal; latent-reasoning & latent-comm have no strong sub
  yet — those surface on X/newsletters, watch for an emerging community)

Hacker News — front page + Algolia search for AI/LLM/serving/quantization/agent terms.

Curated digests (named-expert, high-signal intake — still NOT evidence; their
value is pointing to primaries fast, so follow their links and verify):
- Latent.Space / AINews — daily AI news digest
- Ahead of AI — Sebastian Raschka's LLM research roundups

YouTube — per-channel RSS (`/feeds/videos.xml?channel_id=…`). Seed: Yannic
Kilcher (paper walk-throughs); add conference/lab talk channels (vLLM, SGLang,
PyTorch, NeurIPS/ICLR recordings) and release explainers by discovery.

Hugging Face — org/user activity for tracked accounts (below) + trending models/datasets.

X / Twitter — best-effort via Tavily on profile URLs (no free API in 2026; log
when degraded).

Instagram — public posts only; low feasibility, drop if it never yields.

Tracked profiles/handles (candidates — agent verifies each resolves, then keeps
the ones that recur with signal; add researchers/labs as discovered):
- HF orgs/users: unsloth, bartowski, mradermacher, ggml-org, huihui, googlecs (GGUF/quant/inference + abliterated/derived model activity)
- X (verify each resolves): @ggerganov (llama.cpp), @turboderp_ (ExLlama/EXL3), @danielhanchen (Unsloth), @reach_vb (HF), @teortaxesTex (release news), @kalomaze (sampling/quant), @rasbt (research roundups)
- Agents axis (the previously-missing area): add active agent-framework/research
  accounts as discovered (LangChain, LlamaIndex, AutoGen/Microsoft, CrewAI, and
  individual agent researchers) — seed from r/AI_Agents and the MCP community.
- (agent: extend with lab/researcher accounts on the pinned axes — latent reasoning, latent comm, small/CPU models, low-bit quant)

## GitHub watch (Phase 5 — repos, profiles, and fork trees)

Method: `radar-repo-watch` skill. Releases/merged PRs are citable artifacts;
issue/PR turbulence and profile/fork movement are queue signals until they land.

### Watched repositories (releases / merged PRs / hot issues)
- vllm-project/vllm
- sgl-project/sglang
- ggml-org/llama.cpp
- ggml-org/ggml
- huggingface/transformers
- turboderp-org/exllamav3
- microsoft/BitNet
- ai-dynamo/dynamo
- modelcontextprotocol/modelcontextprotocol

### Watched profiles/users (what a key author will ship next)
Track these accounts' new repos, notable pushes, and releases across all their
repos — early sight of where an influential author is heading:
- ggerganov (ggml/llama.cpp)
- turboderp (ExLlama/EXL3)
- (agent: add authors whose future work is worth pre-empting, on the pinned axes)

### Fork-tree analysis (depth 3)
For the projects below, analyse the fork tree up to depth 3 (forks, forks-of-
forks, forks-of-forks-of-forks) and surface a fork under the project's trend
when it crosses the Fork Notability Score (see `radar-repo-watch`):
- ggml-org/llama.cpp (e.g. ik_llama.cpp-class performance/quant forks)
- microsoft/BitNet
- turboderp-org/exllamav3
- (agent: add projects where forks tend to carry the real innovation)
