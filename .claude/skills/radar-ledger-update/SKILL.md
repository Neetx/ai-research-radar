---
name: radar-ledger-update
description: |
  Safely update TRENDS.md (the AI Radar ledger): append evidence, move stages, manage observation_queue, source_rotation and strategy_notes without breaking the file contract. Use every time TRENDS.md is edited, before committing radar updates, and when promoting or archiving trends.
---

# Update the ledger safely

`TRENDS.md` is the single source of truth and later sessions parse it. The
structure is a contract.

## File contract (do not change)

- Header: `# Trend ledger — AI Radar`, then `Last updated: YYYY-MM-DD`, then the
  stage legend.
- Sections, in this order: `## Active trends`, `## observation_queue`,
  `## source_rotation`, `## strategy_notes`.
- Trend block: `### [id: slug-NNN] Title` with fields `alias`, `stage`,
  `confidence`, `first_observed`, `last_evidence`, `evidence:` (list), `notes:`.
- Evidence line: `- YYYY-MM-DD — URL — one line of context`.

## Rules

- Match findings to existing trends via id and `alias` before creating a new
  trend. New trends take the next free NNN and start at `seed` or `emerging`.
- Max 10 evidence items per trend — drop the oldest. Keep `last_evidence` equal
  to the newest evidence date.
- Stage moves: at most ONE stage up per trend per day, only on new independent
  evidence, justified in `notes`. Demotions are always allowed. 21+ days without
  evidence → `dormant`; at 45+ days the weekly pass moves the entry to
  `ARCHIVE.md` as a one-line post-mortem.
- `observation_queue` items are dated and marked "unverified" unless opened.
  When dropping one, record why in the day's report.
- Append one dated line per session to `source_rotation`. Append dated
  corrections to `strategy_notes`; never delete curator entries.
- Update the `Last updated` line. Keep everything in English.

## Validate before commit

```bash
grep -n '^## ' TRENDS.md
# expected, in order: Active trends, observation_queue, source_rotation, strategy_notes
grep -c '^### \[id: ' TRENDS.md          # trend count matches expectations
grep -nE '^  - [0-9]{4}-[0-9]{2}-[0-9]{2} — ' TRENDS.md | head -3   # evidence format
grep -n '^Last updated:' TRENDS.md       # date is today
```

If a check fails, fix the file before committing. Commit and push per the
conventions in AGENTS.md.
