# Agent guide — AI Radar

Instructions for AI agents (and humans) working in this repository. Task-specific
instructions come from the session prompt; this file holds the invariants that
apply to every session.

## What this repo is

Persistent state for AI Radar, a tracker of AI-ecosystem trends (research +
engineering). It serves an AI researcher / AI-systems engineer who works with AI
daily: besides trends, the radar curates `LIBRARY.md`, a shelf of things worth
studying. `TRENDS.md` is the single source of truth; reports are derived
snapshots. History matters: never rewrite published history, never force-push.

## File map

| Path | Contents | Edit policy |
|---|---|---|
| `TRENDS.md` | Trend ledger + `observation_queue`, `source_rotation`, `strategy_notes` | follow the `radar-ledger-update` skill |
| `DASHBOARD.md` | Derived widget-style summary: badges, digest, stage strip, trend table | regenerate via the `radar-render-dashboard` skill; never edit by hand |
| `LIBRARY.md` | Curated study shelf: projects/papers/concepts worth knowing | daily appends 0–2 picks; weekly prunes |
| `ARCHIVE.md` | Archived trends, one-line post-mortems | append-only |
| `reports/YYYY-MM-DD.md` | Daily reports | write once, never edit old ones |
| `reports/weekly/YYYY-Wnn.md` | Weekly reports | write once |
| `routines/*.md` | Versioned copies of operating prompts | only on explicit request |
| `.claude/skills/` | Project skills | improvable — see policy below |

## Hard rules (never relax these)

- Cite only URLs actually opened in the current session. Anything else is
  "unverified" and belongs in `observation_queue`.
- Primary sources only: papers, official changelogs/release pages, repos,
  official lab/vendor blogs and docs. Never SEO farms, never model
  comparators/aggregators.
- Never guess dates or invent URLs. Undated pages: "(undated, accessed YYYY-MM-DD)".
- Trend bar: ≥3 independent sources (different orgs/author groups) + ≥1 concrete
  artifact (code, paper, spec, release).
- Max 10 evidence items per trend. Do not rename sections or restructure files.
- Everything in this repo is written in English.

## Coverage discipline

- Every daily scan reserves at least one source family for venue-based
  exploration outside the ledger's current axes: browse listings where new work
  appears (HF daily papers, rotating arXiv categories, lab blog indexes) rather
  than searching topics already tracked. Log it in `source_rotation` even when
  it yields nothing.
- Weekly runs check for anchoring: a week where all new evidence lands on
  pre-existing trends gets flagged in `strategy_notes`, and exploration is
  redirected toward uncovered axes or venues.

## Tooling

- Web: prefer the Tavily CLI (`tvly`) via the `tavily-search` and
  `tavily-extract` skills. Auth comes from the `TAVILY_API_KEY` environment
  variable — never print it, never write it to any file in this repo. If `tvly`
  is missing: `pip install -q tavily-cli` (or `uv tool install tavily-cli`).
  Fall back to built-in web tools only if Tavily fails.
- arXiv metadata (exact authors and dates):
  `curl -sL 'https://export.arxiv.org/api/query?id_list=ID1,ID2'`.

## Git conventions

- Commit messages: `radar: daily update YYYY-MM-DD`,
  `radar: weekly recalibration YYYY-Wnn`, `radar: refine skill <name>`, or
  `radar: <short description>` for anything else.
- Any commit that changes `TRENDS.md` must regenerate `DASHBOARD.md` in the same
  commit (see the `radar-render-dashboard` skill).
- Push to `main`. If the push fails: retry once after
  `git pull --rebase origin main`; on persistent failure record the verbatim
  error in the report and stop. Never force-push.
- If the execution environment forces a dedicated session branch (e.g.
  `claude/*`) and forbids pushing to `main`, push there — and open the report
  with a prominent warning that `main` must be fast-forwarded from that branch
  before the next run, otherwise state is lost.

## Skill maintenance policy

Skills in `.claude/skills/` may be improved when a procedure proves wrong,
clunky or incomplete — that is welcome, with constraints:

- Never relax the hard rules above: skills make them more precise, not weaker.
- Keep SKILL.md frontmatter valid (`name`, `description`).
- One dedicated commit per skill change (`radar: refine skill <name>`), and
  describe what changed and why in that day's or week's report.
- Create a new skill only after the same procedure has failed or been improvised
  twice without one.
