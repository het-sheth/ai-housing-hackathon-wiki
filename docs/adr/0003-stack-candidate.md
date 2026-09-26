# ADR 0003: Evaluate a familiar web stack

- Status: Proposed
- Date: 2026-09-26
- Decision owner: Het and Rushi
- Approval evidence: None; stack discussion remains open

## For Humans

Consider a React/TypeScript web application, with Better T Stack as an optional scaffolding tool. Choose its backend and persistence only after the initial workflow and deployment needs are known.

Het's available project history shows repeated React/TypeScript frontend work and both Python and TypeScript backends. This is evidence of prior exposure, not proof of preference or of Rushi's skills.

## For Agents

Alternatives include a small Next.js application, a React frontend plus Python/FastAPI backend, or a minimal Better T Stack configuration. No framework, database, authentication provider, model provider or hosting service is selected.

Better T Stack can reduce assembly work when its generated choices fit the team. It does not provide trustworthy zoning interpretation, source joins, feasibility logic or evaluation. A multi-service architecture may increase deployment effort during the weekend. Accounts and persistence need a workflow justification.

Do not scaffold, install product dependencies or create a production repository based on this proposed ADR. Determine required user action, input/output, saved state, GIS operations, model calls and hosting constraints first. Confirm each teammate's desired role.

Evidence: read-only review of available personal repository commit metadata, plus manifests and selected recent commits in nine relevant projects. This was not an exhaustive review of every historical code change, an audit of deployed systems, or a claim about unseen remote branches.

Reference: https://www.better-t-stack.dev/docs . Prior code informs experience only; it is not application source for this hackathon.
