<!-- README.md -->
# mantle

Like Quartz but better. Designed around [Luria](https://github.com/dmarx/luria)
deployment, but usable without Luria.

mantle publishes a large tree of interlinked markdown as a static site. It
deploys a small shell and a manifest of the tree, and the visitor's browser
fetches and renders each page when it is opened. Publishing costs what the
tree's metadata costs, not what every rendered page costs. Why, and what that
has to satisfy: [ADR-001](record/decisions.d/ADR-001.md).

**Status:** design. Nothing is built yet.

## The record

This project keeps its memory in a Luria record: decisions in
`record/decisions.d/`, principles in `record/principles.d/`, changelog
fragments in `record/changelog.d/` and the devlog in `record/devlog.d/`. The
generated views under `docs/` are built by CI on `main`. See
[CLAUDE.md](CLAUDE.md) for the working rules.
