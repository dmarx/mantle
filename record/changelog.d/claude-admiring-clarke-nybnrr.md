### Added

- A Luria record for mantle: `luria.yaml`, the decisions, principles,
  changelog and devlog directories, and the Docs and Pages workflows from
  Luria's template, with `architecture` and `product` decision tags.
- Retrospectives, adopted from nucleation ([ADR-002](record/decisions.d/ADR-002.md)): RETRO and POSTMORTEM
  schemes, devlog notes tagged `retro`, earmarks, and triggers the assistant
  checks when a batch closes. nucleation's decisions are citable as `NU-…`.
- Standard operating procedures ([ADR-003](record/decisions.d/ADR-003.md)): an SOP scheme in
  `record/procedures.d/` for step-by-step processes, scaffolded with
  purpose, preconditions, checked steps, done-when and pitfalls, and linked
  to the decisions it carries out. [SOP-001](record/procedures.d/SOP-001.md): closing a batch of work.

### Documentation

- [ADR-001](record/decisions.d/ADR-001.md) (Proposed): mantle publishes a markdown tree described by a
  manifest, rendered in the visitor's browser, with its requirements drawn
  from the CI history of Quartz-published Luria records.
