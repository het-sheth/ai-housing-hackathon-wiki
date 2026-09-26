# ADR 0004: Keep decisions and handoffs in Git

- Status: Accepted
- Date: 2026-09-26
- Decision owner: Het
- Approval evidence: Request for local and Git-versioned ADRs plus handoff files for fresh sessions

## For Humans

Maintain a short current handoff, ADRs for consequential choices, and selectively loaded Markdown research. All live in the local checkout and are versioned in Git for collaboration and session continuity.

This reduces dependence on a long chat transcript. It preserves why decisions were made and distinguishes accepted choices from proposals.

## For Agents

Start with root AGENTS.md, `docs/handoffs/current.md`, then `docs/adr/README.md`. Follow only the relevant research links. Never load every source automatically or load the same research report in both PDF and Markdown form.

Update the current handoff when the stage, decisions, branches, verification, blockers or next actions change. Archive a dated snapshot before a significant session transition. Record exact commands and outcomes when relevant, but never include tokens, credentials, private conversations or unnecessary personal details.

The handoff is current state; ADRs are decision history. The handoff must identify research still running, unresolved questions and unapproved scope. Do not mark proposed decisions accepted merely to simplify the handoff.

Alternative: rely on chat summaries alone. Rejected because Rushi and later sessions need the same context without the original transcript. Alternative: reload all source documents each session. Rejected because it wastes context and hides priorities.

Before committing documentation, run `npm run check`. Run applicable tests for tooling changes. Publish through branch and PR under the repository's Git rules.
