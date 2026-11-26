### Changed

- Units of work ([ADR-005](record/decisions.d/ADR-005.md)) merge into a session pull request instead of
  stacking into `main`. Each unit's pull request is squash-merged into the
  session branch, and the owner reviews the session as one commit per unit,
  merged with a merge commit. A convention already in use in a sibling
  project counts as applied. Steps: [SOP-002](record/procedures.d/SOP-002.md).
