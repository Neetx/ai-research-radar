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

## Lab & big-tech AI blogs (Phase 1 — TIERED, prefer RSS/Atom)

Method: `radar-lab-sweep` skill. Open only posts newer than the last scan.

TIERING (W26-P1, applied 2026-07-04 W27; motivated by the W26 coverage-honesty
finding that ~12 low-cadence blogs were listed "swept every run" yet absent from
all 7 days' rotation logs — a coverage lie). Two tiers:
- **Tier (i) — EVERY-RUN high-cadence:** the big labs/vendors below + the
  open-weight HF orgs. These post frequently and on-axis; a daily sweep is
  realistic and OWED — a tier-(i) source silently absent from a run's log is a
  coverage lie.
- **Tier (ii) — LOW-CADENCE (weekly + 1/day rotation):** the "Research labs /
  independents" and "Hardware" lists below. These post infrequently; the DAILY
  rotates ONE per day (logged), and the WEEKLY run owns a full sweep of the tier.
  They are NOT promised every run — this keeps the registry honest.

### Tier (i) — Big labs / vendors (EVERY run):
- OpenAI — https://openai.com/news/ (RSS https://openai.com/news/rss.xml — works; mostly business/policy, scan titles for model/open-weight items)
- Anthropic — https://www.anthropic.com/news (no public RSS as of 2026-06-13: /rss.xml and /news/rss both 404 — extract the HTML index via Tavily)
- Google DeepMind — https://deepmind.google/blog/rss.xml (RSS — confirmed working 2026-06-13; the old /discover/blog/ path is the HTML index)
- Google Research — https://research.google/blog/ (RSS)
- Microsoft Research — https://www.microsoft.com/en-us/research/blog/ (RSS); also Microsoft Security blog https://www.microsoft.com/en-us/security/blog/ for agent-security advisories
- NVIDIA — https://developer.nvidia.com/blog/ (HEALED 2026-06-14: the bare `/blog/feed` returns empty; use https://developer.nvidia.com/blog/feed/ (trailing slash) for the full Atom feed, or the on-axis category feed https://developer.nvidia.com/blog/category/generative-ai/feed/ — titles are CDATA in <entry>. RE-HEAL 2026-06-22: the `/blog/feed/` Atom URL now intermittently returns an EMPTY body too (curl 200 but 0 bytes, seen across 06-21/06-22 passes); reliable fallback is `tvly extract "https://developer.nvidia.com/blog/recent-posts/" --format text` which lists dated post titles + blurbs — use it to triage newest posts when the Atom feed is empty. HEALED AGAIN 2026-07-28: `curl https://developer.nvidia.com/blog/feed/` now returns a full, real Atom feed with dated `<entry>` items again (tested after weeks of the empty-body failure) — surfaced "Six Agent Harness Capabilities for Higher Model Performance" (07-27, NOOA → agent-runtime-015 promotion evidence). Try the direct Atom feed FIRST each run; fall back to the tvly recent-posts extract only if it 0-bytes again) + https://research.nvidia.com/
- Mistral — https://mistral.ai/news/
- Qwen — https://qwenlm.github.io/blog/ (RSS /index.xml STALE: newest post Sep 2025 as of 2026-06-13 — Qwen likely posts elsewhere now; verify qwen.ai + Qwen HF org instead)
- DeepSeek — https://api-docs.deepseek.com/news/ + deepseek-ai HF org
- Hugging Face — https://huggingface.co/blog (RSS /blog/feed.xml)
- Z.ai / GLM — https://z.ai/blog + zai-org HF org
- Model Context Protocol — https://blog.modelcontextprotocol.io/ (PROMOTED to swept 2026-07-18 W29 via source-discovery — cleared the ≥2-on-axis-primary bar in one sweep: EMA-stable 06-18 + four Tier-1 SDK betas 06-29, both dated after mcp-standard-001's 06-11 last_evidence and MISSED for ~3–4 weeks because the blog was only a "watch it late July" note, not a swept source. Working method: `tvly extract "https://blog.modelcontextprotocol.io/"` for the index; individual posts at /posts/<slug>. The primary source for mcp-standard-001 — sweep it every run through the 07-28 final-spec cycle. Also the repo github.com/modelcontextprotocol for the spec itself)

### Tier (ii) — Research labs / independents (LOW-CADENCE: weekly sweep + 1/day rotation; agent: verify feeds on first sweep):
- Meta AI — https://ai.meta.com/blog/ (RE-TIERED to low-cadence 2026-07-18 W29, amendment W28-P1: 0/6 in W28 daily logs + 0/5 in W29, freshest on-axis post infrequent — genuinely low-cadence, mis-placed in tier-(i) "every run". No RSS exists (/blog/rss/, /blog/feed/, /blog/rss.xml all 404); working method `tvly extract "https://ai.meta.com/blog/" --extract-depth advanced`. Recent posts are media-gen/CV/neuro — Muse Image/Video 07-07, Brain2Qwerty 06-29 — mostly OFF the tracked axes; llama releases are also caught via the meta-llama HF org in the daily open-weight recheck)
- Together AI — https://www.together.ai/blog (RE-TIERED to low-cadence 2026-07-18 W29, amendment W28-P1: JS-degraded/empty on the 07-15 + 07-17 daily attempts, infrequent + rarely on-axis; the blog index returns no dated on-axis content via `tvly extract` — treat as low-yield, verify a working extraction method on the next sweep)
- Allen Institute (AI2) — https://allenai.org/blog + https://allenai.org/research (verified-swept 2026-07-04 W27: top posts DiScoFormer / hybrid-token analysis / EMO MoE-for-emergent-modularity — off-axis or already-intake, nothing new on-axis)
- EleutherAI — https://blog.eleuther.ai/ (RSS)
- Sakana AI — https://sakana.ai/blog/
- Nous Research — https://nousresearch.com/
- Berkeley AI Research (BAIR) — https://bair.berkeley.edu/blog/ (RSS)
- Stanford CRFM / Hazy Research — https://crfm.stanford.edu/ + https://hazyresearch.stanford.edu/blog
- PrismML — https://prismml.com/blog + https://prismml.com/news (VERIFIED-SWEPT 2026-07-04 W27 — first actual sweep; `tvly extract https://prismml.com/blog` lists dated posts, `tvly map` gives post URLs at prismml.com/news/<slug>. On-axis ternary/1-bit line: Ternary Bonsai [true 1.58-bit 8B/4B/1.7B, 04-16, → small-cpu-models-008 evidence], 1-bit Bonsai [03-31, prismml.com/news/bonsai-8b], Ternary Bonsai Image 4B [05-26, local-device image gen]. Directly on the small/CPU + low-bit pinned axes — a coverage win the low-cadence tier now captures.)
- Liquid AI (LFM) — https://www.liquid.ai/blog (RE-HEAL 2026-07-21: the RSS `https://www.liquid.ai/blog/rss.xml` now returns "Page not found" (404) — working method is `tvly extract "https://www.liquid.ai/blog"`, whose index lists dated posts; newest LFM2.5-230M unchanged as of this heal) + LiquidAI HF org — the Liquid Foundation Models line ships a steady stream of on-device / small / MoE / GGUF-ONNX releases (LFM2.5-230M, -350M, -8B-A1B, VL, retrievers) — squarely on the small/CPU axis; announced on the blog, NOT arXiv, so the lab sweep is the only lane that catches it.
- LMSYS / SGLang — https://lmsys.org/blog/ (use RSS, JS index fails extraction)
- Cohere — https://cohere.com/blog (RSS)
- GSAI-ML (Renmin University, the LLaDA / iLLaDA diffusion-LM group) — HF org https://huggingface.co/GSAI-ML — added 2026-06-27 (W26 source-discovery): recurring on the diffusion-lm-013 axis (3rd independent open diffusion base model, iLLaDA-8B). Check the HF org for new open diffusion base models; announces via arXiv + HF card, not a blog.

### Tier (ii) — Hardware (LOW-CADENCE: weekly sweep + 1/day rotation) — technical
only, coupled to the small/CPU, low-bit-quant and serving axes; scan for
capability changes, NOT chip-business/macro news. agent: verify feeds on first sweep:
- NVIDIA technical blog — https://developer.nvidia.com/blog/ (also in big-labs above)
- Apple Machine Learning Research — https://machinelearning.apple.com/research (on-device / ANE / small models)
- AMD ROCm Blogs — https://rocm.blogs.amd.com/index.html (serving on non-CUDA)
- Modular (MAX / Mojo) — https://www.modular.com/blog (inference engine + HW abstraction)
- Qualcomm AI Research — https://www.qualcomm.com/developer/blog (edge NPU / on-device). VERIFIED-SWEPT 2026-07-27 (first real sweep of this hardware-tier source, tier-ii daily rotation): `tvly extract` lists dated posts directly, no heal needed. Captured GenieX (07-07) — an open-source on-device Gen AI runtime (NPU/GPU/CPU, GGUF support) — as small-cpu-models-008 evidence.
- Google Cloud TPU / JAX — via research.google + cloud.google.com/blog/products/ai-machine-learning
- Inference-chip startups (agent discretion — technical perf posts only, skip PR): Groq, Cerebras, SambaNova, Etched, Tenstorrent
- Venue: arXiv cs.AR is the standing exploration listing for hardware-aware serving / low-bit kernels (already yielded SPEAR, TileFuse)

## Discovered-source candidates (auto-staged by the daily — NOT yet swept; the weekly verifies & promotes)

The source-discovery loop's staging area. The radar grows its OWN source coverage the way it
finds papers and curators: when any daily lane NAMES an on-axis primary whose publishing
org/domain is NOT already in a swept list above, the daily APPENDS/increments it here — a tally
only, NO extra fetch (you already hold the URL). The weekly VERIFIES the recurring ones (opens
the feed / HF org / repo — never from memory) and PROMOTES them into the swept registry as
`[candidate]`, pruning one-off noise. This closes the gap where an on-axis lab/vendor that
announces only on its own blog (not arXiv) goes untracked because no swept list points at it.
Promotion bar: ≥2 on-axis primary artifacts OR recurrence across ≥2 runs, AND it survives
verification (real feed, on-axis, not SEO). Line format:
`domain/org — times seen — last on-axis artifact (date) — first seen YYYY-MM-DD`.

- aws.amazon.com/blogs/aws — 1 — AWS Lambda MicroVMs, Firecracker agent/AI-code sandbox primitive (2026-06-22) — first seen 2026-06-27 (surfaced via HN front page → agent-sandbox-007 evidence; the cloud vendors' own blogs — AWS, and by extension GCP/Azure — aren't in any swept list, yet the agent-sandbox category now includes a hyperscaler. Weekly: verify the AWS "What's New"/compute-blog feed and consider promoting an AWS-AI-infra feed for agent-sandbox / serving announcements)
- kimi.com/blog — 1 — Kimi K3 announcement, 2.8T "world's first open 3T-class model" (2026-07-16) — first seen 2026-07-17 (surfaced via HN #1 → open-weight-003 + subquad-attn-012 evidence. Moonshot is currently covered ONLY via its HF org recheck, but K3 was announced on the org's own blog with weights/tech-report deferred to 07-27 — so the announcement blog is a high-signal pointer the HF-org lane misses at announcement time. Weekly: verify kimi.com/blog has a usable feed/index and consider promoting it as a Moonshot announcement source, esp. ahead of the 07-27 weights drop)
- enklypesalt.com — 1 — "Context Collapse, Part 3 — AI Worming through Word" (2026-07-28), an MSRC-coordinated prompt-injection-worm disclosure → agent-security-004 evidence — first seen 2026-07-29 (Håkon Måløy's independent security-research blog; discovered via Simon Willison's blog, which pointed to it the same day it published. A named individual's personal research blog, not a lab/vendor — but produces primary-grade, vendor-coordinated (MSRC) security disclosures on the agent-security axis; this is Part 3 of a series, so Parts 1-2 may hold earlier on-axis material. Weekly: check whether the blog has a feed/archive worth a recurring sweep, or whether Simon Willison's blog (already a swept curator) is a sufficient pointer)

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
- Latent.Space / AINews (news.smol.ai) — daily AI news digest. DEGRADED (recurring, first flagged W27): the index is JS-rendered marketing copy with no dated post list via `tvly extract` — heal candidate, not yet fixed.
- Ahead of AI (Sebastian Raschka, magazine.sebastianraschka.com) — LLM architecture / ML research roundups. DEGRADED 2026-07-27 (first real sweep): Substack index returns only a 412-char JS shell via `tvly extract`, no post titles — same shape as Interconnects below; heal candidate (try a direct post-URL guess or an RSS path like `/feed`). **HEALED 2026-07-29**: the author's OWN blog, `sebastianraschka.com/blog/` (distinct domain from the Substack magazine index), is directly `tvly`-extractable with a full dated post archive going back months — surfaced "Kimi K3 Architecture Notes" (07-28, via HN 358pts) with genuinely new architecture detail (NoPE everywhere instead of RoPE, attention-residuals connecting layers via an attention-weighted score) on top of the already-cited K3 tech report. Sweep `sebastianraschka.com/blog/` going forward as the working access path for this author's technical notes; the Substack magazine index stays degraded/redundant.
- Interconnects (Nathan Lambert, interconnects.ai) — post-training, RLHF, open-model dynamics (high signal). DEGRADED 2026-07-27 (first real sweep): Substack index returns only a 429-char JS shell via `tvly extract`, no post titles; same Substack-JS-index shape as Ahead of AI — heal candidate.
- Import AI (Jack Clark, jack-clark.net) — weekly research + policy summary, candid commentary. PARTIALLY WORKING 2026-07-27 (first real sweep): `tvly extract` returns a full issue (good — not JS-blocked) but the returned issue (#462, dated 2026-06-22) reads as a cached/older snapshot, not necessarily the newest; verify against the site's own archive/issue-number index on next sweep to confirm freshness before treating extract results as current.
- AlphaSignal (alphasignal.ai) — research-grade weekly: trending papers, repos, coding breakdowns. VERIFIED-SWEPT 2026-07-27 (first real sweep): `tvly extract` works well, returns a live "N days/hours ago" feed of items with source attribution — a genuinely productive lane (led to the vLLM AFD Plugin + Kimi K3 preview blog posts this run via its vLLM-tagged items). Sweep every run.
- Lilian Weng's blog (lilianweng.github.io) — deep technical surveys. VERIFIED-SWEPT 2026-07-27 (first real sweep): `tvly extract "https://lilianweng.github.io/"` lists post titles/summaries directly (not JS-blocked); post URLs follow `/posts/YYYY-MM-DD-slug/` — grep `href="https://lilianweng.github.io/posts/..."` from a raw `curl` of the index if tvly's summary doesn't give the exact slug. Surfaced "Harness Engineering for Self-Improvement" (07-04), directly on the agent-runtime-015 axis — a real find from a source that had been listed-but-never-swept.
- Simon Willison's blog (simonwillison.net) — LLM practitioner notes/releases. VERIFIED-SWEPT 2026-07-27 (first real sweep): `tvly extract` works well, dated entries readable directly.
- alphaXiv (alphaxiv.org) — community-discussed/trending arXiv papers. VERIFIED-SWEPT 2026-07-27: `tvly extract` of the homepage lists dated trending items directly (no JS issue) — surfaced HOPE (2607.21366, DeepMind) this run.
- Papers with Code (paperswithcode.com) — trending papers + SOTA leaderboards. VERIFIED-SWEPT 2026-07-27: readable via `tvly extract`, but the "Trending Papers" list looked generic/stale (same items across checks) — treat as a weak signal, cross-check against HF daily papers / alphaXiv rather than relying on it alone.
- emergentmind.com — topic/paper tracker that surfaces emerging work. VERIFIED-SWEPT 2026-07-27: readable, but the date-filtered "Trending Papers" query returned empty ("no papers found") on this attempt — the "Explainer Videos" list below it is static/unfiltered and showed nothing new on-axis; may need a different date-range param, revisit.
- **Practitioner-discourse blogs (where PRACTICES GET NAMED)** — this sub-lane serves the
  VOCABULARY-capture step in `routines/daily.md`: these authors coin or popularise the umbrella
  terms the field then adopts (the "<X> engineering" class of paradigm label). Such a naming
  ships no paper, release or changelog, so every artifact lane is blind to it — this is the only
  lane that can see it. Intake-only, NEVER evidence: follow to a primary when one exists,
  otherwise capture the NAME as an `also-called:` alias on the trend it renames. Sweep + log
  every run like the rest of this lane.
  - Addy Osmani — https://addyosmani.com/blog/ · RSS `https://addyosmani.com/rss.xml` **[verified 2026-07-29; both 200]**
  - Louis Bouchard ("What's AI") — https://www.louisbouchard.ai/ · RSS `https://www.louisbouchard.ai/rss/` **[verified 2026-07-29; both 200]**
- alphamatch.ai — explainer blog (curator-seeded; added after it surfaced a
  serious paper the radar had missed). Intake-only: follow to the named primary,
  verify it, cite the primary — NEVER the blog. ACCESS METHOD (healed
  2026-06-22): it has NO RSS (`/rss`, `/feed`, `/rss.xml` all 404); the index
  `https://alphamatch.ai/blog` returns 200 — fetch it with `tvly extract
  https://alphamatch.ai/blog` (or built-in fetch of that URL) to list posts. Sweep
  it EVERY run as part of the mandatory curator lane and log it as opened OR as
  `degraded: <reason>` — do NOT silently omit it (it was listed-but-never-fetched
  for days precisely because no access method was recorded). NAVIGATION TRAP
  (confirmed 2026-07-29): the bare domain `https://alphamatch.ai/` (and
  `www.alphamatch.ai`) now redirects to an UNRELATED AI-consulting/agency
  homepage sharing the domain — do NOT check the bare domain and conclude the
  source is dead or off-topic; the `/blog` path is a distinct, correctly-scoped
  index and is the only URL that should ever be fetched for this source.
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
  rate-limiting, not a channel_id change.
- HEAL UPDATE (2026-06-25, after the 3rd consecutive failure 06-23/06-24/06-25):
  youtube.com is IP-BLOCKED end-to-end from this datacenter — BOTH access paths
  now confirmed dead: (a) `feeds/videos.xml?channel_id=UC…` returns HTTP 404, and
  (b) the previously-proposed heal path `tvly extract ".../@<handle>/videos"`
  returns "Error fetching content". DO NOT keep re-attempting both every run (wasted
  budget). Working BEST-EFFORT fallback until the block lifts or a Reddit/YT API key
  is provisioned: (1) `tvly search "<channel> latest video 2026"` surfaces recent
  upload TITLES (not descriptions) — use a title→arXiv search to try to recover the
  named primary, and if it can't be pinned, log it and rely on (2) the HF-daily-papers
  + HN overlap, where code4AI/bycloud's picks recur (the exploration slot already
  covers these). Re-test the Atom feed roughly weekly; restore the feed method if
  the IP block lifts.
- **HEAL RESOLVED 2026-07-27 (daily, W31)**: the IP-block LIFTED — `feeds/videos.xml?channel_id=UC…`
  returned HTTP 200 with real entries for code4AI, bycloud AND AI Explained on
  re-test (the direct Atom-feed method from before the block, not a new heal).
  Restore this as the primary method going forward; only fall back to the
  best-effort `tvly search` path above if a future run hits 404s again (re-flag
  a fresh block rather than assuming this one).
- **RE-DEGRADED 2026-07-28**: the very next run's re-test 404'd again for all
  three channels — the 07-27 lift did not hold (intermittent, not a stable heal).
  Logged as a fresh single-run failure, NOT yet a repeat-failure pattern (that
  needs the SAME failure twice before spending heal budget on it again per
  `radar-source-heal`) — re-test next run before concluding the block is back
  for good; if it 404s a second consecutive time, treat as re-blocked and fall
  back to the `tvly search` method above.
- **CONFIRMED RE-BLOCKED 2026-07-29**: 2nd CONSECUTIVE 404 (07-28 + 07-29) for
  all three channels — per the rule above this is now a repeat-failure pattern,
  not a one-off. The `tvly search "<channel> latest video 2026"` fallback was
  attempted this run too and returned no usable upload titles (generic/irrelevant
  results). Treat the direct Atom-feed method as blocked again until further
  notice; keep relying on HF-daily-papers + HN overlap for code4AI/bycloud's
  picks; re-test the Atom feed on the weekly cadence rather than every daily run
  (it just proved itself unstable even after a real lift, so daily re-tests are
  low-yield until there's a reason to expect it changed).
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

Hugging Face — org/user activity for tracked accounts (below), PLUS the GLOBAL trending/new-models lane (this is the reliable, complete version of what X reposter accounts like "HuggingModels" relay — the X account is just a derivative pointer to HF, and X is unreadable via code anyway, so query the primary directly, never the pointer):
- **HF GLOBAL trending / new (intake + discovery, every run)** — key-less JSON, no scraping:
  `https://huggingface.co/api/models?sort=trendingScore&limit=30` (what is hot now), plus
  `…?sort=createdAt&direction=-1&limit=30` (brand-new drops) and `…?sort=likes30d&direction=-1` (recent traction).
  Read top items significance-first; filter for on-axis (small/CPU, low-bit quant, new architectures, agent/serving).
  For each on-axis hit, follow to the model card / linked paper and route per the daily §4 (intake until the primary is opened).
  DISCOVERY HOOK (feeds the source-discovery loop): any trending org/author NOT already in a swept list is a candidate lab → stage it in "Discovered-source candidates". A new org trending on HF is exactly a source to track.

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

ACCESS NOTE (2026-07-02, daily — GitHub scope block, self-heal): as of this run
GitHub is proxy-SCOPED to only the radar's own repo — every EXTERNAL GitHub
endpoint (the watched-repo `releases.atom` feeds AND `api.github.com/repos/...`
for vllm-project, sgl-project, ggml-org, modelcontextprotocol, etc.) returns
HTTP 403 `"GitHub access to this repository is not enabled for this session"`.
This is a CHANGE from earlier runs, which fetched these feeds directly. WORKING
METHOD until scope is restored: route the GitHub-watch lane through `tvly`
(search the repo/release name + version + month; extract the release page if a
non-github primary mirrors it) — lower fidelity (no diff of commit/PR turbulence)
but catches new release tags and version bumps. If the block persists, the
weekly should ask the curator to enable broader GitHub read scope (restores the
direct `releases.atom` lane and fork-tree analysis, which tvly cannot replicate).

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

### Engine BLOGS (swept every run ALONGSIDE the release feeds — added 2026-06-27)
Lesson (2026-06-27, daily Pass 2): watching only the GitHub `releases.atom` feeds
MISSED the gate-firing engineering posts that live on the serving engines' own
BLOGS — vLLM announced day-0 native MiniMax-M3 (MSA kernel), DiffusionGemma
(native diffusion sampler) and a benchmarked TurboQuant KV-quant study on its
blog weeks before any of it surfaced in release notes, so three pre-registered
serving-engine promotion gates sat "unfired" for weeks. Fetch these blog feeds
every run (RSS/Atom; fall back to `tvly extract` of the index):
- vLLM — https://blog.vllm.ai/ (HEALED 2026-07-27: no RSS exists — `/feed.xml` and `/rss.xml` both 404. The blog index IS `tvly`-extractable and lists recent post titles/dates directly, but post URLs are NOT in that summary; the site is Next.js so a raw `curl` of `/` doesn't expose `<a href>` either in most tools — the working method is `curl -sL https://blog.vllm.ai/ | grep -oE 'href="/blog/[0-9]{4}-[0-9]{2}-[0-9]{2}-[a-z0-9-]+"'` which DOES surface the slugs from the embedded Next.js payload, then `tvly extract` each `https://blog.vllm.ai/blog/YYYY-MM-DD-slug` directly. This is how the AFD-plugin (07-23) and Kimi-K3-preview (07-22) posts were found this run.)
- SGLang — https://lmsys.org/blog/ (already in Phase 1; the same posts cover SGLang)
- NVIDIA Dynamo / TensorRT-LLM — developer.nvidia.com technical blog (already swept)
A serving-engine post that natively supports a tracked model/operator OR
benchmarks a tracked method is a PRIMARY engineering artifact (citable), not intake.

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
