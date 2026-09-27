# Product interview decisions

Latest amendment: [ADR 0008](adr/0008-gate-preliminary-scoring-on-complete-evidence.md) supersedes the blanket no-score preference below. A Pittsburgh preliminary score is allowed only after all required rubric factors are assessed. Current coverage is incomplete and produces no score. Other historical decisions are preserved; read [the current handoff](handoffs/current.md) for deployment, rejected UI and paused work.

September 26, 2026. Accepted by Het during the product interview. These decisions guide the forthcoming design; they do not mean the capabilities are implemented or that practitioner demand is validated. Recommendations in the separate product critique remain recommendations unless explicitly accepted here.

## Personas and journey

- Onboarding offers Municipal Planner, Small/Mid-Size Developer, Housing Nonprofit/CDC, Policy Analyst, and Other / exploring. Developers and housing nonprofits are the initial priority, not the only users.
- Decision priority: whether to pursue a site, which proposal to pursue, then preparation for review.
- Complete one site's workflow first. Shortlist comparison is deferred.
- V1 begins with an address or parcel ID and natural-language proposal description. V2 adds packet uploads and extraction.
- Guided form with conversational help, editable structured inputs and user confirmation. The optional visual companion was declined for now.

## Coverage

- V1 geographic intake covers Allegheny County, including Pittsburgh, with municipality-specific source and check coverage disclosed.
- Accept and retain all housing proposal types and combinations. Evaluate supported checks; preserve unresolved and unsupported checks as explicit next tasks. Do not substitute a supported but different proposal.
- Model classification cannot establish jurisdiction, legal permission or coverage. Source dates, conflicting records and financial unknowns remain explicit.

## Saved projects and actions

- Users can explore before signing in, then sign in to save and revisit.
- Anonymous drafts persist in the current browser with an explicit Clear draft action and a device-only disclosure until saved to an account. Het accepted the recommended draft behavior.
- Signed-in projects and associated version/task history remain until the owner deletes them. Backup retention and deletion mechanics must be made explicit in the technical design.
- V1 projects have one owner and an exportable brief for collaborators. Shared editing, invitations and team permissions are deferred.
- Task outcomes must be recorded before dependent work continues. Request completed, response received and requirement satisfied are distinct states.
- An inconclusive outcome preserves the unresolved finding and creates the next dependency. Unrelated work may continue.
- Users may proceed with their own planning despite an unresolved dependency by recording a reason for accepting the risk. This does not clear findings, substitute for evidence or authorize regulated work.
- The project lead confirms AI-suggested changes to the path.
- Proposal changes preserve the earlier version and findings, identify affected checks and mark findings needing reassessment. Completed work remains in history but may not apply to the revision.
- On return, show each source's last check and offer an explicit refresh of available sources. Preserve the prior assessment and explain changes. Retrieval time is distinct from source-record vintage.

## Still open

Backup/deletion mechanics; runtime model/endpoint validation; exact source/API and reviewed-rule inventory; deployment/email configuration and server-enforced usage limits. Public dataset reuse checks remain unresolved. No broad automatic regulatory coverage or financial feasibility has been established.

## Authentication and storage options

Het selected Supabase Postgres and Supabase Auth for v1 after comparing Neon with Better Auth. Retain the React/Vite frontend and planned Vercel hosting. Supabase combines the database and managed authentication; personal-project access still requires explicit ownership policies and tests. Anonymous drafts remain browser-local until sign-in. File storage can be considered when packet uploads enter v2. This is a design selection; no provisioning or implementation has occurred.

Neon Postgres plus Better Auth remains a viable alternative, with an application-owned auth server, PostgreSQL adapter and email-delivery integration. Better Auth can also use PostgreSQL hosted elsewhere, including Supabase; the database and authentication choices are separate.

Both email-link approaches require delivery setup. Supabase's default SMTP restricts delivery to organization team addresses and is not suitable for a public sign-in flow; use custom SMTP. Better Auth's magic-link plugin requires a sendMagicLink implementation. Free Supabase projects may pause after inactivity, and a free plan is not itself a backup or long-term retention policy.

Official sources checked September 26, 2026:
- https://supabase.com/docs/guides/auth/auth-email-passwordless
- https://supabase.com/docs/guides/auth/auth-smtp
- https://supabase.com/docs/guides/database/postgres/row-level-security
- https://supabase.com/docs/guides/deployment/going-into-prod
- https://better-auth.com/docs/plugins/magic-link
- https://better-auth.com/docs/adapters/postgresql

## Runtime AI and cost decisions

Het accepted starting with one generative model for structured intake, clarification and sourced explanation, with code owning calculations and rule checks. Jev remains a later candidate to evaluate on the same classification examples rather than an additional initial provider.

Het explicitly wants an AI-native product. The earlier manual-fallback recommendation is not recorded as accepted. AI leads the agreed guided experience. Accepted failure behavior: preserve work, expose failure and retry, retain dated prior results and never fabricate a successful assessment.

Het accepted budget limits and server-side usage enforcement. The final round identifies $10 in existing OpenRouter balance plus the Cursor grant as the available funding boundary. No new purchases or automatic top-ups are authorized. OpenRouter is the recommended runtime candidate pending model/endpoint validation. He reports $75 in Cursor hackathon grant credits, redeemed through a link and already present in his account, and asked whether these can fund API use. Do not treat this as approval to spend $75 elsewhere.

Current official Cursor SDK documentation says agent SDK runs share IDE/Cloud Agent pricing and request pools. It also explicitly distinguishes the SDK from a standalone model-inference API. Credit-grant eligibility for this user's $75, account access and runtime suitability remain unverified. Source checked September 26, 2026: https://prod.cursor.com/docs/sdk/python (Usage and billing; Cursor Router sections). Do not assert that Cursor has no programmable API or that these credits transfer to another provider.

The official TypeScript SDK documentation also explicitly describes credit-grant usage in its billing output: https://cursor.com/docs/sdk/typescript . This establishes support for grant-funded SDK usage in general, not this specific promotion's eligibility. A future bounded account test should confirm the actual grant balance/usage attribution, latency and response quality before selecting Cursor as the product runtime. A zero chargedCents value alone does not prove the grant paid, because plan-included and BYOK usage can also report zero. No grant-attribution or hosted SDK test has been performed; the subsequent CLI probe below is narrower.

## Approval record

Subsequent bounded test: [Cursor intake probe](cursor-intake-probe-2026-09-26.md) records one successful Auto CLI call after named-model access was rejected. Local response quality and latency were inspected; grant billing and SDK/hosted suitability remain unverified. This supersedes earlier statements that no account test had occurred, without selecting Cursor as the runtime.

In the interview, Het agreed to countywide intake, broad proposal acceptance with explicit check coverage, and recorded planning-risk overrides. Het then explicitly selected personal projects with an exportable brief and agreed to preserved proposal versions and explicit source refresh on return. Earlier persona and journey decisions are preserved from the same conversation.

## Accepted final round

Het accepted all six final questions in specification section 11. Assessment and prioritized actions are primary; comparison is secondary. Adopt the eight product pillars, named check statuses and evidence/action checklist without an overall numerical score. Keep finances unassessed without inputs. The accepted launch minimum is countywide identity/assessment, verified permit coverage, a reviewed Pittsburgh subset and explicit gaps elsewhere. V1 uses useful 2D site context; defer 3D until data and decision value justify it. Preserve work and show explicit retry on AI failure. The reported available balances are $10 OpenRouter and $75 Cursor; no additional purchases or automatic top-ups are authorized.

The [consolidated specification](product-spec-v1-2026-09-26.md) is ready for review. Technical recommendations remain labeled; application implementation has not begun for this expanded design.

## September 26 amendment: early financial diligence

Het subsequently accepted one early, relevant question about whether the proposal has a preliminary budget, expected sale or rental assumptions where applicable, and an identified funding path. Each answer may be unknown. When relevant information is unknown or absent, the assessment creates a prioritized financial diligence task requesting the missing assumptions or a responsible reviewer. User-provided figures remain assumptions, not verified market evidence or a financial feasibility finding. Finance remains Unassessed without a reviewed financial method and sufficient evidence. This amendment preserves assessment and next actions as the primary result, comparison as secondary, and the no-score decision.

This is a product decision from Het, not a practitioner interview, endorsement or validation. Do not publish private conversation quotes or names as interview evidence. Het also authorized starting application implementation after the earlier documentation-only handoff.

Het subsequently chose a striking 3D animated intro as an illustrative visual, separate from actual 2D parcel context. The animation does not depict a surveyed property, current buildings or a verified 3D site. Procedural Three.js is the current implementation direction; a Blender GLB may be considered later. Blender is not installed in the current workspace. The earlier decision to defer evidentiary 3D site context still stands.
