---
name: radar-render-dashboard
description: |
  Regenerate DASHBOARD.md, the derived visual summary of TRENDS.md (stage pipeline in Mermaid, per-stage tables, watchlist, latest reports). Use after every change to TRENDS.md, in the same commit. DASHBOARD.md is never edited by hand: if it disagrees with TRENDS.md, TRENDS.md wins — regenerate.
---

# Render the dashboard

`DASHBOARD.md` is a derived view. `TRENDS.md` stays the single source of truth.
Regenerate the whole file from scratch on every run — never patch it.

## Stage badge map (fixed)

🌱 seed · 📈 emerging · 🚀 accelerating · 🌊 mainstreaming · 🏔 saturated · 📉 declining · 💤 dormant

Badges appear ONLY in DASHBOARD.md and reports — never inside TRENDS.md
(the ledger's `stage:` field stays plain text; tooling greps it).

## Generation rules

Parse every trend block from TRENDS.md (`id`, title, `stage`, `confidence`,
`last_evidence`), count `observation_queue` items, find the newest daily and
weekly reports. Then emit, in this order:

1. **Header** — title, generation date, and the warning line:
   `Generated from [TRENDS.md](TRENDS.md) on YYYY-MM-DD — derived view, do not edit by hand.`
2. **Stage pipeline (Mermaid)** — flowchart LR with one node per stage showing
   `badge stage · count` (include zero-count stages), the dormancy dotted edge
   labeled "21d no evidence" and the archive dotted edge labeled "45d → ARCHIVE.md".
   Quote all node labels.
3. **One section per non-empty stage**, ordered accelerating → emerging → seed →
   mainstreaming → saturated → declining → dormant. Each is a table
   `| id | trend | confidence | last evidence |`, rows sorted by `last_evidence`
   descending. Heading: `## 🚀 Accelerating (N)`.
4. **Watchlist** — total `observation_queue` count linking to TRENDS.md, then the
   3 newest items as one-line bullets (date + short description).
5. **Latest reports** — link the newest file in `reports/` and in
   `reports/weekly/` ("none yet" if absent).

## Checks before commit

- Counts in the Mermaid nodes equal the table row counts per stage and the total
  number of `### [id:` blocks in TRENDS.md.
- Every table date matches the trend's `last_evidence` field exactly.
- Commit DASHBOARD.md together with the TRENDS.md change that triggered it.
