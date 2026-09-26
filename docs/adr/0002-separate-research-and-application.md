# ADR 0002: Separate research and application repositories

- Status: Accepted
- Date: 2026-09-26
- Decision owner: Het
- Approval evidence: "we will make another repo for the actual production stuff"

## For Humans

Use this public wiki for shared research, rules, decisions and handoffs. Create a separate repository for the actual hackathon application when its scope is selected.

This lets Het and Rushi share research without confusing a copied wiki template with the submitted application. It also keeps the app's build history and disclosures clear.

## For Agents

Alternative: put research, inherited wiki tooling and app code in one repository. Rejected because their purpose, source provenance and lifecycle differ.

Repository: https://github.com/het-sheth/ai-housing-hackathon-wiki . Rushi's verified GitHub account is Baburaoooo, identified through an existing collaboration and his public profile. A write-access invitation was sent. Acceptance must be checked before claiming he has access.

The public wiki contains source PDFs/CSVs, faithful Markdown extractions, curated concepts and prospective product analysis. Preserve original sources. Exclude customer conversations and other private discovery records. Do not copy prior project implementation into the new app; the packet prohibits prior project code while permitting disclosed libraries/frameworks.

Use branches and PRs, never direct pushes to main. No application repository has been created yet. Revisit if the team changes how it separates public documentation from implementation.
