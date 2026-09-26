---
type: concept
title: Write evidence-grounded housing notes
description: Add concise, sourced research without turning hypotheses into decisions.
tags: [housing, authoring, evidence]
timestamp: 2026-09-26T00:00:00Z
status: solid
---

# Write evidence-grounded housing notes

Use one clear topic per page. Add `type: concept`, a descriptive title, description, tags, status and meaningful-change timestamp in YAML frontmatter. Use a stub when the answer is unknown. Return to the [session reading guide](/wiki/getting-started/welcome.md) when deciding what to load next.

For example, a zoning-source note should distinguish the organizer catalog's claim, what the current official metadata establishes, which actual records were inspected, and what still requires a planner. Include jurisdiction, date, source and limitations. A nearby utility line does not establish service capacity; an absent record does not establish absence of a constraint.

Preserve original files in `raw/hackathon/`. Use page-marked text in `raw/markdown/` for selective source reading. Cite raw paths as inline code, with PDF page references where useful. External sources belong under `# Citations`. Link other wiki concepts through resolving Markdown links.

Place product alternatives in the relevant product concept. Record an accepted consequential choice in `docs/adr/`, including approval evidence and tradeoffs. Keep current state and next actions in `docs/handoffs/current.md`. Do not add private customer conversations or unsupported research claims.

Run `npm run check` after changes. `site/` is generated only when needed; do not edit it. Commit and publish via a branch and PR.

# Citations

Project `AGENTS.md`; `docs/adr/0004-context-and-handoffs.md`; user requirements for grounded research and session continuity.
