---
name: radar-source-verify
description: |
  Verify a signal or evidence candidate for the AI Radar ledger: open primary sources, pin exact dates and authors, check source independence, and classify the result as citable evidence or an unverified observation_queue item. Use whenever adding evidence to TRENDS.md, promoting a queue item, or fact-checking a claim found in search results.
---

# Verify a source for the ledger

Goal: every evidence line in `TRENDS.md` has (a) a URL that was actually opened
this session, (b) a real date, (c) one line of context.

## Procedure

1. **Find** candidates with the `tavily-search` skill (`--include-domains
   arxiv.org,github.com,huggingface.co` for primary sources, `--time-range`
   for recency). Search snippets are never citable on their own.
2. **Open** each candidate with the `tavily-extract` skill. Opened = citable.
3. **Pin dates** — by source type:
   - arXiv: `curl -sL 'https://export.arxiv.org/api/query?id_list=ID1,ID2'`
     gives exact v1/latest dates and the full author list (the abs page often
     hides them from extraction). Use https, not http.
   - GitHub: cite the latest release tag and its date, not the access date.
   - Hugging Face org pages: "updated X days ago" → compute the estimate and
     write "(date estimated from the org page)".
   - Undated pages: "(undated, accessed YYYY-MM-DD)".
4. **Independence check** (for the ≥3-sources trend bar): sources must come from
   different orgs/author groups. Shared co-authors collapse two papers into one
   group — compare author lists before counting.
5. **Classify**:
   - Opened + dated + primary → evidence line:
     `- YYYY-MM-DD — URL — one line of context`
   - Not opened, or secondary-only → `observation_queue` line marked
     "unverified", stating exactly what is missing.

## Red flags (queue or drop — never cite)

- SEO content farms, model comparators/aggregators, market-wire press syndication.
- Releases claimed by aggregators but absent from the vendor's official channel
  (check the org's HF page or official blog index before believing them).
- Vendor-reported adoption numbers: citable, but label them "vendor-reported".
