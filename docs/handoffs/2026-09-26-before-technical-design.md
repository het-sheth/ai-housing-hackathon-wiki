# Current handoff: first local prototype

Updated September 26, 2026. Stage: first usable local app built; final verification and app handoff are recorded in the app repository.

Independent public-source research on whether proposal comparison is useful is recorded in `docs/proposal-comparison-research-2026-09-26.md`. Pittsburgh rules support scope-dependent checks, but many single-family repairs and additions share Basic Zoning Review. TestFit advertises side-by-side scheme comparison, so comparison alone is not differentiation. The ACTION-Housing talk establishes a real design tradeoff, not demand for this prototype. Het has sent a practitioner question about a recent scope change; the answer remains pending. Use the response to judge whether the app changes a meaningful next action.

Additional TestFit documentation review found that its zoning data comes from Zoneomics, its major utility layer excludes water and sewer, and mapped data layers do not export from a deal. These do not establish a Pittsburgh product gap or an advantage the local prototype has already delivered. In the current local app, the repair-versus-expansion explanation changes but both pathways can retain the same review status and City next action. The next demo should distinguish changed reasoning from changed decisions.

The public-source [ShurSave case review](../shursave-case-2026-09-26.md) now traces an earlier roughly 190-unit grocery concept, the related Ella Street rezoning with future site-plan review required, the later 248-unit variance request, the Board setback and the 2024 grocery-only outcome. The Board denied FAR and height relief but granted a grocery special exception. This supports a proposal-specific comparison with separate approval, housing and financial questions. The earlier concept's full zoning path and financial viability remain unverified, and this large mixed-use example does not validate the Lanark workflow.

Research note verification: `npm run check` passed with 79 concepts and zero problems; `git diff --check` passed. The note and this handoff update are local and uncommitted on `docs/proposal-comparison`.

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

## Product critique follow-up

Resume from the [consolidated v1 specification](../product-spec-v1-2026-09-26.md). Het accepted all six final choices: assessment/actions first, comparison secondary; eight pillars and statuses without a numeric score; countywide intake with the documented bounded launch checks; 2D v1 and deferred 3D; explicit AI failure/retry; existing $10 OpenRouter plus $75 Cursor balances with no new purchases/top-ups authorized. The product interview is complete for this scope. Review the consolidated spec and resolve exact sources/rules/reuse, model/endpoint validation, email/auth/deployment configuration and usage limits before an implementation plan. Supabase Postgres/Auth is selected. OpenRouter is the recommended runtime candidate, not a verified integration. Cursor Auto CLI passed one isolated intake probe; hosted suitability and grant attribution remain unverified. No app implementation changes were made in this product-design phase.

Subsequent interview decisions are recorded in [product interview decisions](../product-decisions-2026-09-26.md): countywide intake with explicit municipal/check coverage, all proposal types retained, personal saved projects and exportable briefs, outcome-based tasks with recorded planning-risk overrides, preserved proposal versions and explicit source refresh on return. These supersede narrower interview recommendations where noted, but do not establish implemented coverage or practitioner validation. Supabase sign-in and retention until deletion are selected; email delivery, backup/deletion mechanics, runtime model and detailed architecture remain technical prerequisites.

The user requested critical product judgment, not implementation. [The product critique](../product-direction-critique-2026-09-26.md) recommends testing a proposal-aware zoning/site screen and next-diligence handoff, keeping comparison secondary unless it changes a consequential task. Het subsequently accepted assessment/actions as primary and comparison as secondary in the final interview; practitioner value remains unvalidated. Het accepted recording a task outcome before dependent work continues; task completion does not establish a favorable finding. ShurSave's hearing transcript explicitly revises FAR from 3.25:1 to 3.1:1. The historical record does not establish a viable lower-rise alternative. App and prior research work were preserved.
