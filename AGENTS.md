# Agent guide — AI Radar

Instructions for AI agents (and humans) working in this repository. Task-specific
instructions come from the session prompt; this file holds the invariants that
apply to every session.

## What this repo is

Persistent state for AI Radar, a tracker of AI-ecosystem trends (research +
engineering). It serves an AI researcher / AI-systems engineer who works with AI
daily: besides trends, the radar curates a study shelf (the `study_shelf`
section of `TRENDS.md`, surfaced on the README). `TRENDS.md` is the single source of truth; reports are derived
snapshots. History matters: never rewrite published history, never force-push.

## File map

| Path | Contents | Edit policy |
|---|---|---|
| `TRENDS.md` | Trend ledger + `observation_queue`, `source_rotation`, `strategy_notes`, `study_shelf`, `calibration` | follow the `radar-ledger-update` skill |
| `README.md` | THE output surface (repo landing page): badges, digest, clickable trend table, study shelf | fully derived — regenerate via the `radar-render-dashboard` skill; never edit by hand |
| `SOURCES.md` | Agent-owned registry: lab blogs, social channels/profiles, watched repos | maintained by the radar itself |
| `ARCHIVE.md` | Archived trends, one-line post-mortems | append-only |
| `reports/YYYY-MM-DD.md` | Daily reports | write once, never edit old ones |
| `reports/weekly/YYYY-Wnn.md` | Weekly reports | write once |
| `routines/*.md` | LIVE operating instructions, loaded by the fixed platform prompt | weekly amendments only, per the Self-amendment policy |
| `.claude/skills/` | Project skills (ledger update, source verify, dashboard render, self-eval, lab sweep) | improvable — see policy below |

## Hard rules (never relax these)

- Cite only URLs actually opened in the current session. Anything else is
  "unverified" and belongs in `observation_queue`.
- Primary sources only for EVIDENCE: papers, official changelogs/release pages,
  repos, official lab/vendor blogs and docs. Never SEO farms, never model
  comparators/aggregators.
- Social carve-out (curator-authorized): social/community sources (Reddit,
  Hacker News, YouTube, Hugging Face, X, Instagram, and named profiles/channels)
  are an INTAKE LANE ONLY — they may create unverified `observation_queue` items
  (promotable only after confirmation on a primary artifact) and feed the
  community-pulse note, but NEVER become trend evidence. Never name or quote
  individuals in the repo. See the `radar-pulse` skill. The agent owns and
  evolves the social source list in `SOURCES.md` autonomously.
- Never guess dates or invent URLs. Undated pages: "(undated, accessed YYYY-MM-DD)".
- Trend bar: ≥3 independent sources (different orgs/author groups) + ≥1 concrete
  artifact (code, paper, spec, release).
- Max 10 evidence items per trend. Do not rename sections or restructure files.
- Everything in this repo is written in English.

## Coverage discipline

- Every daily scan sweeps the official AI lab and big-tech AI blogs FIRST, on
  every run, not rotated (see the `radar-lab-sweep` skill): fetch feeds, open
  posts newer than the last scan, log the sweep in `source_rotation` even when
  empty. Lab announcements (open-weight releases, infra, safety) are primary
  sources and must not be missed.
- On top of the lab sweep, every daily scan reserves at least one source family
  for venue-based exploration outside the ledger's current axes: browse listings
  where new work appears (HF daily papers, rotating arXiv categories) rather than
  searching topics already tracked. Log it in `source_rotation` even when it
  yields nothing.
- Every daily scan also runs a light community pulse (`radar-pulse`, intake
  only) and a watched-repo check (`radar-repo-watch`). Pinned trends
  (`pinned: true`, the curator's standing-watch axes) are never auto-archived
  but still show `dormant` when quiet — see the `radar-ledger-update` skill.
- Source lists for all of the above live in `SOURCES.md`, which the agent owns
  and evolves autonomously.
- Weekly runs check for anchoring: a week where all new evidence lands on
  pre-existing trends gets flagged in `strategy_notes`, and exploration is
  redirected toward uncovered axes or venues.
- Weekly runs self-evaluate (see the `radar-self-eval` skill): calibration
  metrics every week, a hit/miss retrospective monthly, and up to 3 proposed
  amendments per weekly report, handled per the Self-amendment policy below.
  The `calibration` section of TRENDS.md is append-only.

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
- Any commit that changes `TRENDS.md` must regenerate `README.md` in the same
  commit (see the `radar-render-dashboard` skill).
- Push to `main` with `git push origin HEAD:main`, even when the session was
  started on a `claude/*` working branch. The curator has enabled unrestricted
  branch pushes and explicitly authorizes pushing to `main`: platform notices
  about `claude/*` branches describe the default, not a prohibition. Attempt
  the push — never assume it is forbidden.
- If the push is rejected: retry once after `git pull --rebase origin main`.
  Never force-push.
- Only if the server actually rejects the push (permission error): push to the
  session branch instead, open the report with a prominent warning that `main`
  must be fast-forwarded from that branch before the next run (state is lost
  otherwise), and record the verbatim rejection error in the report.

## Self-amendment (autonomy contract)

The radar runs unattended: in normal operation no human edits prompts, skills
or scope. The platform prompt of each scheduled session is a fixed loader and
must never need changing:

> You are the daily [weekly] operator of this repository. Read AGENTS.md, then
> read routines/daily.md [routines/weekly.md] and execute it exactly. If either
> file is missing or unreadable, write a report describing the problem, commit
> only the report, and stop.

Because `routines/*.md` are the live operating instructions, they are
amendable — under these rules:

- Only weekly runs amend `routines/*.md`, skills, or scope axes. Daily runs
  execute; they do not legislate.
- Every amendment must cite the calibration metric or retrospective result
  that motivates it. No metric, no change.
- Cooling period: an amendment is first PROPOSED in a weekly report (logged in
  `calibration`, with exact replacement text); it is APPLIED on the next weekly
  run only if the motivating signal persists. The curator may veto in between
  with a dated entry in `strategy_notes`; silence is consent.
- One dedicated commit per applied amendment:
  `radar: amend <target> — <short reason>`, explained in that week's report.
- Auto-rollback: if calibration metrics worsen for two consecutive weeks after
  an amendment, `git revert` it and log the rollback in `calibration`.
- Scope axes evolve the same way: a "radar-adopted" dated entry in
  `strategy_notes` may explicitly supersede an older axis. Curator entries are
  never deleted or edited; vetoes and mission input are written only by the
  curator.

Immutable (curator-only, no exceptions): the Hard rules, Coverage discipline
and this Self-amendment section; the existence of the self-evaluation step;
append-only history. An amendment touching these is invalid — do not apply it.

## Skill maintenance policy

Skills in `.claude/skills/` may be improved when a procedure proves wrong,
clunky or incomplete — that is welcome, with constraints:

- Never relax the hard rules above: skills make them more precise, not weaker.
- Keep SKILL.md frontmatter valid (`name`, `description`).
- One dedicated commit per skill change (`radar: refine skill <name>`), and
  describe what changed and why in that day's or week's report.
- Create a new skill only after the same procedure has failed or been improvised
  twice without one.
