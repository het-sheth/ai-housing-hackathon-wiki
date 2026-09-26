# AI for Housing Hackathon: agent instructions

## For Humans

This repository is Het and Rushi's shared research and decision record for the Pittsburgh AI for Housing Hackathon. Track 1, Development Feasibility Navigator, is selected. We are still brainstorming the practitioner workflow and product scope. The application will have its own repository.

Read `docs/handoffs/current.md` to resume work. Read `docs/adr/README.md` for accepted and proposed decisions. Use `wiki/product/context-start.md` for a compact research overview.

## For Agents

### Session entry and intent

1. Read this file, `docs/handoffs/current.md`, then `docs/adr/README.md`.
2. Check the current branch and working tree. Preserve unfinished work and inspect the handoff's publication state.
3. Load only the wiki concepts or source sections needed for the current question.
4. Continue the user's active task; do not restart discovery, repeat settled questions or treat a research proposal as approval to implement.

The user wants an actionable Pittsburgh housing product that fits practitioners' existing tools and handoffs. It should be usable by people without technical expertise. A nonprofit site screen is a candidate workflow, not an approved specification. Het does not want a standalone analytics dashboard. Architecture, model provider and hosting remain open. Better T Stack is being evaluated, not selected.

The team has two people. Het has Saturday and Sunday. Build window: September 26, 2026 at 9 a.m. through September 27 at 11:59 p.m. Eastern. The full official rules are in the packet; do not replace them with assumptions. Before public claims, distinguish Pittsburgh city jurisdiction from other Allegheny County municipalities.

### Where information belongs

| Location | Purpose |
|---|---|
| `wiki/event/` | Rules, provenance and project overview |
| `wiki/tracks/` | Challenge requirements and comparison |
| `wiki/research/` | Housing concepts and interpretation of Rushi's research |
| `wiki/data/` | Catalog index, access checks and corrections |
| `wiki/datasets/` | One page per organizer catalog entry |
| `wiki/product/` | Current hypotheses, open questions, research brief and stack assessment |
| `wiki/getting-started/` | Project-specific reading and authoring guidance |
| `raw/hackathon/` | Immutable downloaded sources and original-byte manifest |
| `raw/markdown/` | Full PDF text extractions, page anchors, links and conversion manifest |
| `docs/adr/` | Consequential decisions, rationale, alternatives and approval evidence |
| `docs/handoffs/` | Current state and dated transition snapshots |
| `docs/deep-research-prompt.txt` | Copyable assignment for the separate research session |
| `site/` | Optional generated website; never edit manually |

### Evidence and context discipline

Preserve source files. Correct stale URLs or mistaken claims in a derived note rather than rewriting originals. Label official requirements, research claims, verified findings, inferences and team decisions separately. Never invent interviews, endorsements, dataset coverage, time savings, score calibration or financial assumptions.

The long PDF and original research Markdown substantially overlap. The two catalog CSVs are duplicates. Read one relevant representation. Prefer curated concepts, then page-marked text, then the original PDF when figures or table layout matter. Reading a data catalog is not equivalent to validating underlying records or joins.

Do not put Penny/customer conversations, credentials or private discovery records in this public repository. Public notes may contain only appropriate, explicitly shareable findings. Never infer access or outreach authorization from a request to brainstorm.

### ADRs and handoffs

Record consequential decisions using `docs/adr/template.md`. Include status, decision owner, approval evidence, alternatives, rationale, tradeoffs and revisit conditions. Keep proposals proposed until accepted. Supersede old decisions explicitly instead of rewriting their history.

Update `docs/handoffs/current.md` after meaningful progress and before ending a substantial work session. Include current stage, branch/publication state, outstanding work, blockers, verification and exact next actions. Archive a dated snapshot for a major transition. Provide a resume prompt that works without the original chat. Keep the current handoff concise; reference detailed notes instead of copying them.

### Markdown and validation contract

Markdown in `wiki/` is canonical. Each concept has YAML frontmatter with required `type: concept`, `pattern` or `worked-example`; include a title, description, tags, status and meaningful-change timestamp. Use `status: stub` for unresolved knowledge. Full source Markdown under `raw/` uses `type: source`.

Reserved `index.md` and `log.md` have no frontmatter. `wiki/_templates/` and `wiki/journal/` are excluded from normal concept validation and publication, but Git still tracks them unless ignored: they are not private storage.

Cross-link concepts using `[Label](/wiki/topic/slug.md)` or relative Markdown links. Every concept link must resolve. Cite raw source paths as inline code or via `resource:` rather than ordinary local Markdown links. Put external sources under `# Citations`. Use plain ASCII punctuation in authored material; preserve original source text faithfully.

`topics.json` controls topic ordering. Each named topic must exist. The optional renderer supports within-wiki links and callouts. Cross-wiki federation is not enabled for this project; do not add peer dependencies without a reason and a decision.

Run `npm run check` after documentation changes. Run `npm test` after tooling or rendering changes and before publishing a batch that affects agent guidance or wiki structure. Use `npm run build` only when a generated local site is requested or needed. In this environment, sandboxed test subprocesses have intermittently returned empty captured output. The full suite passed outside the sandbox; diagnose execution-environment failures before changing assertions.

### Collaboration and boundaries

Use branches and PRs; never push directly to main. Follow the inherited global commit conventions, with no attribution trailers. Rushi's GitHub account is Baburaoooo; verify invitation acceptance before asserting collaborator access.

This repo was derived from `het-sheth/okf-wiki-template`. That is provenance, not an active template-development task. The old template's implementation plans do not govern this project. Do not create application code here or reuse prior project implementation for the hackathon app. Broader source research does not authorize product implementation; obtain agreement on the product design first.
