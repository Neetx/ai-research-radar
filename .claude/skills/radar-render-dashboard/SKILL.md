---
name: radar-render-dashboard
description: |
  Regenerate DASHBOARD.md, the compact widget-style summary derived from TRENDS.md (badges, a 3-4 line "since last scan" digest, stage strip, compact trend table, footer links). Use after every change to TRENDS.md, in the same commit. DASHBOARD.md is never edited by hand: if it disagrees with TRENDS.md, TRENDS.md wins — regenerate.
---

# Render the dashboard

`DASHBOARD.md` is a derived view. `TRENDS.md` stays the single source of truth.
Regenerate the whole file from scratch on every run — never patch it. The design
goal is a widget: everything visible in one screen, no diagrams, no walls of text.

## Layout (exactly these blocks, in this order)

1. **Title** — `# AI Radar`, nothing else.
2. **Badge row** — four shields.io static badges, style `flat-square`:
   `trends-<total>-3266ad`, `accelerating-<n>-e8590c`,
   `watchlist-<queue count>-6c757d`, `updated-<YYYY--MM--DD>-2f9e44`
   (escape `-` in dates as `--`). One line, space-separated.
3. **Digest** — `**Since last scan (YYYY-MM-DD):**` followed by 3–4 bullets MAX,
   distilled from today's ledger changes in priority order: stage moves first,
   then queue promotions/drops, then the single strongest new evidence. Bold the
   one keyword that matters per bullet. If nothing changed, one bullet: "Quiet
   scan — no ledger changes."
4. **Stage strip** — one line, all seven stages with counts:
   `🌱 n · 📈 n · 🚀 n · 🌊 n · 🏔 n · 📉 n · 💤 n`
   (seed, emerging, accelerating, mainstreaming, saturated, declining, dormant).
5. **Trend table** — columns `trend | stage | last evidence`. All trends, sorted:
   accelerating → emerging → seed → mainstreaming → saturated → declining →
   dormant, then by `last_evidence` descending within each stage. The trend
   column uses a SHORT label (≤5 words): reuse the labels already in the previous
   DASHBOARD.md for existing trends (stability matters), invent one only for new
   trends. Stage column: emoji + word.
6. **Footer** — one line of links: `[Ledger](TRENDS.md)`, watchlist count linking
   to `TRENDS.md#observation_queue`, `[study shelf](LIBRARY.md)`, newest daily
   report, newest weekly report ("weekly: none yet" if absent).

## Checks before commit

- Badge counts = stage-strip counts = table row counts = number of `### [id:`
  blocks in TRENDS.md.
- Every table date equals that trend's `last_evidence` field exactly.
- No Mermaid, no images other than the four badges, no sections beyond the six
  blocks above.
- Commit DASHBOARD.md together with the TRENDS.md change that triggered it.
