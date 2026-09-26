# Current handoff: first local prototype

Updated September 26, 2026. Stage: first usable local app built; final verification and app handoff are recorded in the app repository.

## Current work

Het explicitly selected React + TypeScript + Vite and authorized creating the separate local application. The new repository is `/home/het/personal/ai-housing-navigator`, branch `feat/first-prototype`. No app remote, push, deployment or external message was authorized or performed. The research branch remains `docs/proposal-comparison`; prior remote PR #3 status was not rechecked this session.

The app supports selecting 1623 Lanark, inspecting its real projected parcel outline, editing two hypothetical proposals, comparing conditional findings and downloading a Markdown brief. Browser print is also available. The comparison retains the September 26 evidence snapshot, with assessment as of September 1. A fresh whitelisted exact-parcel assessment request succeeded during browser verification, while failures remain explicit. It is a separate live observation, not silent replacement of snapshot evidence.

## Resume

Read `/home/het/personal/ai-housing-navigator/AGENTS.md`, `README.md` and `docs/current.md`. Start with the running app at http://127.0.0.1:5173/ or run `npm run dev -- --port 5173 --strictPort` in the app repository. Iterate on the demonstrated flow with Het; do not restart research or recreate the app.

## Boundaries and remaining gaps

Assessment and PLI conflicts persist. Unknown legal use, slope impact and unchecked hazards never become permission. Full code dependency/effective-date review, practitioner validation, runtime AI integration and organizer acceptance of component-only scoring remain open. Overall ease is not rated and finances are unassessed. No final submission completeness claim is made. Resolve dataset reuse terms before publication. ADR 0005's detailed research scope remains proposed beyond the narrow authorized prototype.

## Verification

App checks passed: 27 tests, typecheck, ESLint, production build and local Chromium smoke flow. Research documentation check passed with 79 concepts and zero problems. The known sandbox subprocess failure recurred; all 40 wiki tests passed outside the sandbox.

App verification results and exact commands are recorded in `ai-housing-navigator/docs/current.md`. Browser interaction, actual Markdown download, mobile overflow, simulated request failure and one actual live assessment request were exercised. See that handoff for final counts and fixes.

The pre-build research context is preserved in [the dated handoff](2026-09-26-before-local-prototype.md). The original execution prompt remains [start-prototype-session.md](../start-prototype-session.md), but its statement that no app exists is now historical.
