# AI for Housing Hackathon research wiki

Het and Rushi's shared research context. Resume with [the current handoff](docs/handoffs/current.md), review [decision records](docs/adr/README.md), or start at [the overview](wiki/event/overview.md).

1. Read [rules and submission](wiki/event/rules.md).
2. Compare [the three tracks](wiki/tracks/comparison.md).
3. Browse [all 60 catalog entries](wiki/data/catalog.md).
4. Discuss [Rushi's direction](wiki/research/rushi-direction.md).
5. Resolve [open decisions](wiki/product/open-questions.md).

Canonical notes live in `wiki/`; immutable sources and checksums live in `raw/hackathon/`. The repository is copied from https://github.com/het-sheth/okf-wiki-template and keeps its template provenance. It is a research workspace, not the hackathon application submission. New app development needs its own repository and event-time commit history.

Run `npm ci`, then `npm run check`. Run `npm test` for template regression checks. Optional `npm run build` generates a local static site. Do not edit generated `site/` files.

Track 1 is selected. No product design or stack is approved yet. The source catalog is fully read; underlying datasets are not fully ingested. Current policy claims require independent verification before product use.
