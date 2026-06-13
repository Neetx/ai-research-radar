# Sources registry — AI Radar

Agent-owned registry of monitored sources. The radar maintains and evolves this
file itself (add/remove/mark-dead entries, with a one-line reason in the day's
or week's report) — no curator sign-off needed. Skills describe the *method*;
this file is the *data*.

Hard-rule reminder: lab blogs and GitHub artifacts are PRIMARY sources (citable
evidence). Social/community sources are an INTAKE LANE ONLY — never evidence;
see the `radar-pulse` skill and the social carve-out in AGENTS.md.

---

## Lab & big-tech AI blogs (Phase 1 — swept EVERY run, prefer RSS/Atom)

Method: `radar-lab-sweep` skill. Open only posts newer than the last scan.

- OpenAI — https://openai.com/news/
- Anthropic — https://www.anthropic.com/news
- Google DeepMind — https://deepmind.google/discover/blog/ (RSS)
- Google Research — https://research.google/blog/ (RSS)
- Meta AI — https://ai.meta.com/blog/ (RSS)
- Microsoft Research — https://www.microsoft.com/en-us/research/blog/ (RSS)
- NVIDIA — https://developer.nvidia.com/blog/ (RSS) + https://research.nvidia.com/
- Mistral — https://mistral.ai/news/
- Qwen — https://qwenlm.github.io/blog/ (RSS /index.xml)
- DeepSeek — https://api-docs.deepseek.com/news/ + deepseek-ai HF org
- Allen Institute (AI2) — https://allenai.org/blog (RSS)
- Cohere — https://cohere.com/blog (RSS)
- Hugging Face — https://huggingface.co/blog (RSS /blog/feed.xml)
- LMSYS / SGLang — https://lmsys.org/blog/ (use RSS, JS index fails extraction)
- Together AI — https://www.together.ai/blog
- Z.ai / GLM — https://z.ai/blog + zai-org HF org

## Social & community channels (Phase 2 — INTAKE ONLY, never evidence)

Method: `radar-pulse` skill. Best-effort via Tavily (no paid APIs / no secrets).
Log degradation when a platform can't be reached. Never name/quote individuals
in the repo — link the thread/profile, summarise.

Reliable (free, clean via Tavily):
- Reddit — r/LocalLLaMA, r/MachineLearning, r/LocalLLM
- Hacker News — front page + Algolia search for AI/LLM/serving terms
- YouTube — per-channel RSS (`/feeds/videos.xml?channel_id=…`) for named channels
- Hugging Face — org/user activity for tracked accounts

Best-effort (unreliable in 2026 — log when degraded):
- X / Twitter — specific researcher/lab profiles via Tavily on profile URLs
- Instagram — public posts only; low feasibility, drop if it never yields

Tracked profiles/handles (agent maintains — start empty, add as discovered):
- (none seeded yet — agent adds researcher/lab handles it finds worth watching)

## Watched GitHub repos (Phase 5 — behind-the-scenes activity)

Method: `radar-repo-watch` skill. Each run, check since the last scan: new
releases/tags, notable merged PRs, high-activity issues/discussions. Releases &
merges are citable artifacts; issue/PR turbulence is a queue signal.

- vllm-project/vllm
- sgl-project/sglang
- ggml-org/llama.cpp
- huggingface/transformers
- turboderp-org/exllamav3
- microsoft/BitNet
- ai-dynamo/dynamo
- modelcontextprotocol/modelcontextprotocol
- ggml-org/ggml
