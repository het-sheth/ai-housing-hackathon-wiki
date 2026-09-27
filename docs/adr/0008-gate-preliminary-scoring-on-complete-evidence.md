# ADR 0008: Gate preliminary scoring on complete evidence

- Status: Accepted
- Date: 2026-09-26
- Decision owner: Het
- Approval evidence: Het selected Pittsburgh-first preliminary explainable scoring, then required withholding every number until all required information is available.
- Supersedes: The blanket no-overall-score preference in ADR 0006 only. Other evidence, action and permission boundaries remain.

## For Humans

### Decision

Allow a preliminary Development Ease Score for a defined Pittsburgh proposal only when every required factor in a published, explainable rubric is assessed. Until then, show sourced findings, missing information and useful next actions without any score, range or numeric contribution. Countywide property lookup remains available with municipality-specific check coverage.

### Why

The user explicitly requested a score aligned with the track goal but rejected broad partial intervals. An incomplete evidence set must not appear favorable merely because unknown factors were omitted or guessed.

### Tradeoffs

Current integrations leave required factors unassessed and therefore cannot produce a complete score. A rubric and complete evidence do not establish financial feasibility, legal permission or calibrated approval probability. Provisional weights require review before being treated as a stable product standard.

## For Agents

### Context and evidence

The app has a provisional deterministic rubric and bounded public-record adapters. Mapped undermining is now a supplementary observation, while zoning requirements, site-level risk review, process, utilities and financial evidence remain incomplete. A model does not fill these gaps. The deployed API returns pending with null score and no numeric check contributions. User feedback also rejects the unrun results page; generic tasks must not masquerade as completed assessment findings.

### Alternatives considered

Keep no overall score indefinitely; show a partial min/max interval; or use a model probability as the final number. The user superseded the first and rejected the second. The third has not been authorized or validated.

### Consequences and constraints

Jev is not integrated. Its Noul primitive reports probability of a yes/no proposition; its Score primitive rates against ordered criteria. Multiplying Noul by 100 does not turn it into development ease. No Jev trial, paid request, model replacement or missing-evidence inference is authorized by this decision. Preserve string parcel IDs, source dates, independent failures and conflicts.

The separate property-explorer branch contains a proposed AI-confirmed candidate search and one-parcel proposal comparison. This direction does not mean citywide search or a 3D parcel explorer is implemented. Preserve the original guided layout while repairing the current flow.

### Revisit when

The required factor inventory, source/rule versions, practitioner review and rubric calibration can support an actual number, or the user changes the completeness requirement.

### Related material

- [ADR 0006](0006-select-action-led-v1.md)
- [Current handoff](../handoffs/current.md)
- [TypeSafe primitives](https://docs.typesafe.ai/primitives)
