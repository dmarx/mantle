# CLAUDE.md

**Before anything else, read
[the design principles](docs/design-principles.md) in full.** They are the
standing values every choice in this project is judged against; the rest of
this file, and the record itself, assume you hold them. Read them
immediately after finishing this file, before any other code or
documentation in this repository.

This project keeps its memory in a Luria record — decisions, principles, a
changelog and a devlog — scaffolded, generated and linted by the `luria`
CLI. This file is a map, not a copy
([LU-ADR-037](https://github.com/dmarx/luria/blob/main/record/decisions.d/ADR-037.md)):
the doctrine lives one link away and the current command surface lives in
`luria --help`. When this file disagrees with either, this file is the one
that's wrong.

- **Run `luria --help`** for what the CLI does today; every command takes
  `--help`.
- [This project's docs](docs/README.md) — the generated views: the decision
  record, the principles, the devlog books, the status reports.
- [Project memory: how a repo thinks](https://github.com/dmarx/luria/blob/main/docs/project-memory.md)
  — the doctrine behind the layout: the four layers, what files where, how
  the record is revised.
- [Comment directives](https://github.com/dmarx/luria/blob/main/docs/directives.md)
  — the acknowledgement vocabulary (`inactive-ok:` and friends), wikilinks,
  and fixture codes.
- [Configuration](https://github.com/dmarx/luria/blob/main/docs/configuration.md)
  — every `luria.yaml` key, generated from Luria's own schema. Read this
  before assuming the record can only hold decisions: schemes, fragment
  directories, journals and remotes are families this project names, and
  `luria.yaml` is where its shape is decided.

Four ground rules, terse enough to restate:

- **Work goes to a branch and a pull request, never straight to the default
  branch** — the record is the deliverable, and it needs a chance to be read
  before it becomes what the project believes.
- **File the fragment in the same contribution as the work** (`luria new`):
  a fact filed while its context is loaded costs a paragraph; re-derived
  cold, it costs a session.
- **Never hand-write a link target.** Write the bare code and let `luria
  link --fix` spell the target: record prose is rendered into views in
  *other directories*, so a target has to resolve from where the text
  lands, not where it lives — only the fixer knows that frame. Want prose
  as the label? That's `[[FX-ADR-001|a labeled wikilink]]`, still the fixer's
  job. A hand-written target that looks right here is wrong somewhere.
- **A guard that keeps catching you is a bug report about the workflow.**
  One catch is the net working; the same catch again means the hazard is
  upstream — a practice, a missing affordance, an undocumented rule — and
  the fix is to remove what *generates* the mistake, not to keep thanking
  the net. Quiet guards are the goal; a busy one is compensating for
  something.

## Retrospectives

The process is [ADR-002](record/decisions.d/ADR-002.md), adopted from nucleation.

- `record/retrospectives.d/`: RETROs, reviews of how a change or a stretch of
  work went, including what went right. `record/postmortems.d/`:
  POSTMORTEMs, rarer, reviews of something that went wrong. Both `review`
  the decisions involved, link the pull requests, and name in `prompted` the
  decisions their recommendations become.
- **File notes as the work goes.** When something seems to be going right or
  wrong and worth revisiting, file a devlog entry tagged `retro` (`luria new
  devlog`) in the pull request it concerns. Say what happened, why it seems to
  work or not, and any wrong theory and how it was found out. Going right is
  worth a note as much as going wrong. No asking needed.
- **Earmarks.** When the owner says something is for the retro, in any
  words, file a note tagged `retro` and `earmarked` at once. Quote the
  earmark and say where it was made. The next RETRO answers each one by name.
- **When a batch closes, check the triggers** and say which are met:
  - a RETRO for a contract change that has been used, five or more pull
    requests in a session, a release, or a site moving onto mantle;
  - a POSTMORTEM for a decision revised soon after landing, or a process
    incident (CI red twice on one cause, a revert, a broken release or site,
    a standing rule broken or nearly broken).

  The owner decides whether to write it; never file one unasked. The steps
  are [SOP-001](record/procedures.d/SOP-001.md).

## Procedures

`record/procedures.d/` holds SOPs, step-by-step instructions for processes
run more than once ([ADR-003](record/decisions.d/ADR-003.md)). Each names the decisions it carries out in
`implements`.

- **When a task matches an Active SOP's `when`, follow it**, and report any
  step that didn't hold.
- **A run that shows a step is wrong fixes the SOP in the same pull
  request**: bump `version`, and add a `history` entry saying what the run
  found.
- **A new recurring process gets an SOP** (`luria new sop`). Don't write its
  steps into an ADR body or restate them here.

<!-- Optional: a hands-free regime (luria's decision on it, in its record). Uncomment once the project
     has an integration branch that only a promotion carries to the default
     branch, and a decision of its own adopting this.

- **The hands-free regime, when the owner switches it on.** It is on until
  switched off; a new session starts off. While it is on: file what the
  work develops as it goes, one commit per turn; when a turn has several
  readings, file each as an alternative; answer first, then report what was
  filed; merge into the integration branch when checks pass; revert when
  the owner interjects. Status changes, new decisions, configuration, CI,
  anything sent outside and the promotion to the default branch still wait
  for the owner. Suggest switching off when going on would be awkward.
-->
