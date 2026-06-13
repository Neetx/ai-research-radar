---
name: radar-lab-sweep
description: |
  Sweep the official AI lab and big-tech AI blogs on EVERY daily run (not rotated) so no open-weight release, infrastructure or safety announcement is missed. Prefer RSS/Atom feeds over HTML pages to survive JavaScript-rendered indexes. Use at the start of every daily scan, before the rotating exploration slot.
---

# Lab sweep — every run, no rotation

A real research radar checks the labs themselves every single day. This sweep is
mandatory on every daily run and is separate from (and in addition to) the
rotating exploration slot. Official lab/vendor blogs are primary sources under
the Hard rules, so anything found here is citable evidence.

## Method (efficient)

1. For each source in the list, fetch its FEED first (RSS/Atom), not the HTML
   index — feeds are immune to the JS-rendering that hid `lmsys.org/blog`. To
   find a feed: try `/rss.xml`, `/feed`, `/atom.xml`, `/index.xml`, or read the
   page's `<link rel="alternate" type="application/rss+xml">`.
2. Open only entries dated AFTER the last daily scan (check the previous
   `source_rotation` date). Skip everything older — this keeps the sweep cheap.
3. Apply the evidence rules: open the actual post, cite its own date, match to a
   trend or log to `observation_queue`/`study_shelf` as appropriate.
4. Log the sweep in `source_rotation` every run, even when nothing is new
   ("lab-sweep: no new posts").

## Source list (maintain this — agent-owned)

Mark a feed `DEAD` inline if it stops resolving; add new labs as they appear.
Prefer the feed URL; fall back to the HTML index via `tvly extract` only if no
feed exists.

- OpenAI — https://openai.com/news/ (check for feed)
- Anthropic — https://www.anthropic.com/news (check for feed)
- Google DeepMind — https://deepmind.google/discover/blog/ (RSS)
- Google Research — https://research.google/blog/ (RSS)
- Meta AI — https://ai.meta.com/blog/ (RSS)
- Microsoft Research — https://www.microsoft.com/en-us/research/blog/ (RSS)
- NVIDIA developer/research — https://developer.nvidia.com/blog/ (RSS) + https://research.nvidia.com/
- Mistral — https://mistral.ai/news/
- Qwen — https://qwenlm.github.io/blog/ (RSS at /index.xml)
- DeepSeek — https://api-docs.deepseek.com/news/ and the deepseek-ai HF org
- Allen Institute (AI2) — https://allenai.org/blog (RSS)
- Cohere — https://cohere.com/blog (RSS)
- Hugging Face — https://huggingface.co/blog (RSS at /blog/feed.xml)
- LMSYS / SGLang — https://lmsys.org/blog/ (use the RSS feed, not the JS index)
- Together AI — https://www.together.ai/blog
- Z.ai / GLM — https://z.ai/blog and the zai-org HF org

## Notes

- The sweep complements, never replaces, the rotating exploration slot.
- Big-tech AI blogs often announce model/open-weight releases that never become
  arXiv papers — those announcements are exactly what this sweep exists to catch.
- Keep this list in sync with any unified source registry if one is introduced.
