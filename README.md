# AI Radar — state repository

Persistent state for **AI Radar**, a tracker of trends across the AI ecosystem
(research + AI engineering). The ledger holds what is being watched; reports are
point-in-time snapshots derived from it.

## File map

| Path | Contents |
|---|---|
| `TRENDS.md` | The ledger: active trends (stage, confidence, evidence), `observation_queue`, `source_rotation`, `strategy_notes` |
| `ARCHIVE.md` | Archived trends, one-line post-mortem each |
| `reports/YYYY-MM-DD.md` | Daily reports |
| `reports/weekly/YYYY-Wnn.md` | Weekly reports |

## Conventions

- `TRENDS.md` is the single source of truth; reports are derived from it.
- Evidence items cite only primary sources that were actually opened (papers,
  changelogs, repos, official lab blogs). No SEO sites, no model comparators.
- Stages are promoted conservatively; see the legend at the top of `TRENDS.md`.
- Manual edits to state files should be explicit, clearly-messaged commits.
