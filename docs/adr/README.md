# Decision records

ADRs explain consequential choices, their evidence, alternatives and tradeoffs. They are versioned in this repository and available in the local checkout. They record actual decisions; proposals must remain labeled proposed.

## For Humans

| ADR | Status | Decision |
|---|---|---|
| [0001](0001-select-track-one.md) | Accepted | Enter Track 1 and continue workflow discovery |
| [0002](0002-separate-research-and-application.md) | Accepted | Keep research and application repositories separate |
| [0003](0003-stack-candidate.md) | Superseded by selected foundation | Historical stack candidate; React/Vite and Supabase were later selected |
| [0004](0004-context-and-handoffs.md) | Accepted | Use selective Markdown context, ADRs and a current handoff |
| [0005](0005-propose-project-comparison.md) | Proposed | Evaluate two housing proposals on one Pittsburgh parcel |
| [0006](0006-select-action-led-v1.md) | Partially superseded by 0008 | Lead with proposal assessment and next actions |
| [0007](0007-propose-persisted-workflow-architecture.md) | Proposed | Extend the prototype with owner-scoped persisted workflows |
| [0008](0008-gate-preliminary-scoring-on-complete-evidence.md) | Accepted | Withhold preliminary score until required evidence is complete |

## For Agents

Create an ADR when a choice materially affects user workflow, scope, data authority, scoring, architecture, integration, deployment or evaluation. Use sequential IDs and the template. Include the source of approval, status, context, considered alternatives, rationale, consequences and revisit conditions. Do not infer acceptance from a discussion or a research suggestion.

Preserve historical rationale. When a decision changes, add a superseding ADR and update the old record's status and link. Keep this index current. Minor edits and routine findings belong in the handoff or topic pages, not a new ADR.
