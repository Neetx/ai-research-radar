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
- Meta AI — https://ai.meta.com/blog/ (HEALED 2026-06-14: no RSS exists — /blog/rss/, /blog/feed/, /blog/rss.xml all 404 and the HTML index has no feed <link>. Working method: `tvly extract "https://ai.meta.com/blog/" --extract-depth advanced`. As of 2026-06-14 the blog's freshest post is April 2026 — Meta posts infrequently)
- Microsoft Research — https://www.microsoft.com/en-us/research/blog/ (RSS); also Microsoft Security blog https://www.microsoft.com/en-us/security/blog/ for agent-security advisories
- NVIDIA — https://developer.nvidia.com/blog/ (HEALED 2026-06-14: the bare `/blog/feed` returns empty; use https://developer.nvidia.com/blog/feed/ (trailing slash) for the full Atom feed, or the on-axis category feed https://developer.nvidia.com/blog/category/generative-ai/feed/ — titles are CDATA in <entry>. RE-HEAL 2026-06-22: the `/blog/feed/` Atom URL now intermittently returns an EMPTY body too (curl 200 but 0 bytes, seen across 06-21/06-22 passes); reliable fallback is `tvly extract "https://developer.nvidia.com/blog/recent-posts/" --format text` which lists dated post titles + blurbs — use it to triage newest posts when the Atom feed is empty) + https://research.nvidia.com/
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

Reddit (subreddits — verified active; organized by axis so coverage gaps are
visible. Ensure every pinned axis has at least one channel):
- **Broad AI pulse / breaking news** (HIGH traffic, high noise — intake only;
  where field-shaking events surface first and loudest, and the layer whose
  absence let the radar miss the Anthropic Fable/Mythos shutdown 2026-06-12):
  r/singularity, r/artificial, r/ClaudeAI, r/OpenAI, r/Anthropic, r/LocalLLaMA.
  Read these for "what is the field consumed by right now", not just on-axis topics.
- Local / small / CPU models + quant: r/LocalLLaMA (the canonical pulse), r/LocalLLM
- Research / papers: r/MachineLearning
- Agents / agentic engineering: r/AI_Agents, r/LLMDevs, r/LangChain
- MCP / tool use: r/mcp
- RAG / retrieval: r/RAG
- Multimodal / diffusion: r/StableDiffusion
- Serving/inference has no dedicated active sub — that discussion lives in r/LocalLLaMA
- (agent: add/prune by signal; latent-reasoning & latent-comm have no strong sub
  yet — those surface on X/newsletters, watch for an emerging community)

Rationale for the broad-pulse tier: the technical subs maximise on-axis signal
but are blind to field-shaking events outside the tracked axes. Big news breaks
in the generalist/vendor communities first — include them (intake only) so the
pulse never misses an earthquake. See the "Don't miss the earthquake" rule in
the `radar-pulse` skill.

Hacker News — via the Algolia API host `https://hn.algolia.com/api/v1/search?tags=front_page` (and `query=<term>` searches): programmatic, CDN-fronted, not IP-blocked — use this, don't scrape the HTML front page.

Cloud-env network note (HEALED 2026-06-20 — see the persistent-block rule in `radar-source-heal`; do NOT re-log "degraded" every run): the curator's 2026-06-19 allowlist widening (reddit.com, hn.algolia.com, huggingface.co, news.ycombinator.com) was RE-TESTED on 2026-06-20 and partially took effect. WHAT NOW WORKS DIRECT (preferred over tvly — no key, full JSON):
  - HN front page / search: `https://hn.algolia.com/api/v1/search?tags=front_page` (+ `&query=<term>`) — returns JSON, use for the broad-pulse earthquake check.
  - HF daily papers: `https://huggingface.co/api/daily_papers?date=YYYY-MM-DD` (empty `[]` until the day's list posts, usually next-day; omit `?date` for current). Sort the returned items by `paper.upvotes` for the significance-first read.
  - HF models (open-weight recheck): `https://huggingface.co/api/models?author=<org>&sort=lastModified&direction=-1&limit=N` — JSON with `id`/`lastModified`/`createdAt`.
  STILL BLOCKED (site-side / datacenter-IP, NOT egress — do not keep retrying): `reddit.com/r/<sub>/*.json` returns "Blocked by egress policy" even after the allowlist change → keep the tvly fallback for Reddit. Reliable Reddit-direct would need a free Reddit OAuth app (`REDDIT_CLIENT_ID/SECRET`), a separate curator call.
  Tooling note (2026-06-20): the `tvly` CLI flag set drifted from the `tavily-search` skill docs — use `--time-range [day|week|month|year]` (not `--days`), `--depth [ultra-fast|fast|basic|advanced]` (not `--search-depth`), and `--topic [general|news|finance]`.

Curated digests + explainer/aggregator blogs (INTAKE LANE). Like the lab blogs
above, these are SWEPT EVERY RUN; unlike them, they are intake only — NEVER cited
as evidence. Their job is to surface what is getting attention so you FOLLOW the
link to the PRIMARY artifact and verify THAT (cite the primary, never the
pointer/blog).

These are tracked SOURCES, swept with the SAME discipline as the lab blogs —
there is NO second-class "sample a few on rotation" tier. Every entry below is a
coverage PROMISE: open it (or log `degraded: <reason>`) EVERY run and NAME it in
the coverage log. A tracked source silently absent from the log is a coverage
LIE, not a lean sweep. If an entry has no feed, HEAL its access method and record
it here (as done for alphamatch / NVIDIA / Meta) — never drop a source for being
awkward to fetch. If you genuinely will not sweep an entry every run, REMOVE it
from this list: the registry must be honest about what it actually covers, with
no tier that is skipped a priori. Agent: verify each on first use.
- Latent.Space / AINews — daily AI news digest
- Ahead of AI (Sebastian Raschka) — LLM architecture / ML research roundups
- Interconnects (Nathan Lambert) — post-training, RLHF, open-model dynamics (high signal)
- Import AI (Jack Clark) — weekly research + policy summary, candid commentary
- AlphaSignal — research-grade weekly: trending papers, repos, coding breakdowns
- Lilian Weng's blog (lilianweng.github.io) — deep technical surveys (verify)
- Simon Willison's blog (simonwillison.net) — LLM practitioner notes/releases (verify)
- alphaXiv (alphaxiv.org) — community-discussed/trending arXiv papers
- Papers with Code — trending papers + SOTA leaderboards
- emergentmind.com — topic/paper tracker that surfaces emerging work
- alphamatch.ai — explainer blog (curator-seeded; added after it surfaced a
  serious paper the radar had missed). Intake-only: follow to the named primary,
  verify it, cite the primary — NEVER the blog. ACCESS METHOD (healed
  2026-06-22): it has NO RSS (`/rss`, `/feed`, `/rss.xml` all 404); the index
  `https://alphamatch.ai/blog` returns 200 — fetch it with `tvly extract
  https://alphamatch.ai/blog` (or built-in fetch of that URL) to list posts. Sweep
  it EVERY run as part of the mandatory curator lane and log it as opened OR as
  `degraded: <reason>` — do NOT silently omit it (it was listed-but-never-fetched
  for days precisely because no access method was recorded).
- (explainer/SEO blogs that REPEATEDLY surface verified primaries get ADDED here
  as tracked pointers via the discovery mechanism below — alphamatch.ai is the
  first; always pointer → primary → cite the primary, never the blog)

YouTube — TRUSTED-CURATOR POINTER LANE (check EVERY run, intake only, never
cited). High-signal channels that explain serious new papers are topic-agnostic
FILTERS for "what's worth attention" — exactly how the radar catches important
work it would otherwise miss (e.g. code4AI's "looped world model" = a
looped-transformer world model that sits on the latent-reasoning pinned axis,
missed because YouTube wasn't being worked). For each NEW video since the last
scan, FOLLOW the description to the named paper/repo and verify the PRIMARY
(radar-source-verify); cite the primary, never the video. Resolve each handle to
its `channel_id` once (open the channel page, grep `"channelId":"UC…"`), then use
`https://www.youtube.com/feeds/videos.xml?channel_id=UC…`.
- SOURCE-HEALTH note (2026-06-23): the `feeds/videos.xml?channel_id=UC…` Atom
  endpoint returned HTTP 404 intermittently from this datacenter IP for code4AI /
  bycloud / AI-Explained today (one early Yannic fetch succeeded, then all 404'd);
  the channel HTML is JS-rendered (built-in fetch returns only the footer) and a
  WebSearch for recent uploads did not surface them. So the YouTube curator lane
  was DEGRADED this run (logged in source_rotation). Likely transient YouTube
  rate-limiting, not a channel_id change. If it 404s again next run: re-resolve
  each `channel_id` from the channel page, and consider a `tvly extract` of the
  `/videos` page (once `tvly` auth is restored) as the heal path.
- @code4AI (now "Discover AI") — daily deep-dives on fresh AI papers (curator-supplied, high signal) — channel_id `UCfOvNb3xj28SNqPQ_JIbumg` (resolved 2026-06-21; NOTE: the handle's HTML lists featured side-channels first — take the canonical `channel/UC…` link, not the first `"channelId"` match)
- Yannic Kilcher — long-form, section-by-section paper readings — channel_id `UCZHmQk67mSJgfCCTn7xBfew` (resolved 2026-06-21; main channel quiet, newest 2026-03)
- bycloud — frontier research breakdowns + lab analysis (high signal) — channel_id `UCgfe2ooZD3VJPB6aJAnuQng` (resolved 2026-06-21)
- AI Explained — what new capabilities actually mean, with nuance — channel_id `UCNJ1Ymd5yFuUPtn21xtRbbw` (resolved 2026-06-21)
- Machine Learning Street Talk — long-form technical interviews with researchers
- (lower-priority / pop-sci, optional: Two Minute Papers, 3Blue1Brown for math)

### Discovering NEW / emerging curators AND explainer/aggregator blogs (grow the list)

This covers BOTH human curators (YouTube channels, researcher handles) AND
explainer/aggregator blogs & sites (the alphamatch.ai class — even SEO-ish ones,
used as intake-only pointers, never cited). The curated list must GROW on its own
— a static roster goes stale and misses the next code4AI or the next explainer
blog sitting on a great paper. Three mechanisms, all agent-owned:
1. **Hit attribution (daily, free).** Whenever you follow a signal to a primary
   you then verify as serious, note WHO surfaced it first (which channel / blog /
   handle / thread). A source that recurs as the origin of verified-serious finds
   has earned a place — add it to "Candidate curators" with the hit count.
2. **Scouting (weekly, cheap).** Periodically search for emerging explainers
   ("best AI paper YouTube/Substack 2026", new researcher blogs) AND scan the
   community recommendation threads (r/MachineLearning, HN, r/LocalLLaMA "who
   explains X / best channel for Y") for creators repeatedly praised for serious
   explanations. Add promising ones to "Candidate curators".
3. **Probation → promote / drop (weekly, measured).** A candidate rides the
   probation list; if it surfaces ≥2 verified-serious primaries over ~3–4 weeks,
   promote it to the curated list; if it's hype/noise or never hits, drop it with
   a one-line reason. Demote a curated source that goes quiet or noisy. This is
   the self-improvement loop applied to GROWING the source set, not just healing it.

Candidate curators (probation — agent fills; format: name/handle — why — hits/since):
- (none yet — populate via mechanisms 1–2 above)
- (agent: ADD a channel when it repeatedly surfaces work the radar later verifies
  as serious; drop noisy ones. conference/lab talk channels — vLLM, SGLang,
  PyTorch, NeurIPS/ICLR — by discovery.)

Hugging Face — org/user activity for tracked accounts (below) + trending models/datasets.

X / Twitter — BEST-EFFORT, never a dependency. No free API in 2026, Nitter dead,
scraping blocked → reading X is unreliable. Method: tvly on the handle/profile
URLs below + pick up the big X threads that the digests (AINews/Latent.Space)
and HN/Reddit already surface (a real X earthquake cross-posts everywhere within
hours). So the earthquake net must NOT rely on X — the reliable channels (HN +
broad Reddit + curators + digests) catch it regardless; X is a bonus. Log
"X degraded" when unreachable and move on; do not let it block the pulse. The
only reliable-X path is a paid X API (a curator call — declined for now).

Instagram — public posts only; low feasibility, drop if it never yields.

Tracked profiles/handles (candidates — agent verifies each resolves, then keeps
the ones that recur with signal; add researchers/labs as discovered):
- HF orgs/users: unsloth, bartowski, mradermacher, ggml-org, huihui, googlecs (GGUF/quant/inference + abliterated/derived model activity)
- X (verify each resolves): @ggerganov (llama.cpp), @turboderp_ (ExLlama/EXL3), @danielhanchen (Unsloth), @reach_vb (HF), @teortaxesTex (release news), @kalomaze (sampling/quant), @rasbt (research roundups)
- Agents axis (the previously-missing area): add active agent-framework/research
  accounts as discovered (LangChain, LlamaIndex, AutoGen/Microsoft, CrewAI, and
  individual agent researchers) — seed from r/AI_Agents and the MCP community.
- (agent: extend with lab/researcher accounts on the pinned axes — latent reasoning, latent comm, small/CPU models, low-bit quant)

## Discovery / exploration venues (Phase 4 — iterated EVERY run by radar-explore)

Where NEW / not-yet-tracked important work surfaces. The `radar-explore` skill
iterates this list significance-first (read the TOP / most-attention items
REGARDLESS of topic), to find what the radar SHOULD be tracking — not to confirm
the axes it already tracks. Same contract as the other sweeps: execute the list,
log venues + date range covered. A venue that recurrently surfaces serious work
gets ADDED here (so it is iterated next run); a dead one is dropped.

PRIMARY (cross-category, attention-ranked — covered EVERY run; this cross-cutting
view is what a single arXiv category cannot give):
- Hugging Face daily papers — https://huggingface.co/papers + /papers/date/YYYY-MM-DD ; API https://huggingface.co/api/daily_papers — rank by upvotes, read the top items regardless of category.
- alphaXiv (alphaxiv.org) + Papers with Code /trending — community attention signals on fresh arXiv work (cross-check; intake → follow to the arXiv primary).

SUPPLEMENT (ONE per run, rotating, with an ADVANCING date window — read newer than
the last browse of that venue per logs/source_rotation.md; never re-mine the same
batch):
- arXiv category recent listings, rotated: cs.AR, cs.RO, cs.CV, cs.DC, cs.SE, cs.LG, cs.CL, cs.MA, cs.AI (export.arxiv API or the /list/<cat>/recent page).
- Watch-area venues (off-axis — surface and queue, never force a trend): world models / world simulators (cs.RO, cs.CV), physics AI / AI-for-science (physics.comp-ph + AI-for-science lab blogs), quantum ML (quant-ph).

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
