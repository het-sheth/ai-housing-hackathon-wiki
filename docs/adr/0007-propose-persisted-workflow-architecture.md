# ADR 0007: Propose persisted workflow architecture

- Status: Proposed
- Date: 2026-09-26
- Decision owner: Het and Rushi
- Approval evidence: None for this architecture. The user requested a concrete technical design and plan, explicitly without application implementation. Supabase Postgres/Auth is already selected in the dated product decisions.
- Supersedes: None. ADR 0003 remains historical proposed stack research; this record narrows the new engineering recommendation without rewriting it.

## For Humans

### Decision

Recommend extending the React/TypeScript/Vite prototype with same-origin Node API handlers on planned Vercel hosting, Supabase Postgres/Auth, PostGIS geography checks, IndexedDB anonymous drafts and ordinary persisted application workflows. One validated model endpoint proposes intake/explanations; code owns geographic joins, rules and authorized transitions.

Keep the existing prototype at `/`, design preview at `/design-system`, and introduce the guided workflow at `/projects/new`. Personal project history and task dependencies use relational records; findings are immutable assessment payloads. No graph database or LangGraph dependency is proposed initially.

### Why

The current evaluator contains Lanark-specific evidence and cannot safely accept arbitrary parcels. Typed coverage contracts and a narrow evaluator boundary let the app grow without copying Lanark findings onto new sites. Server handlers protect credentials, budgets and transitions; database policies enforce owner isolation independently of the UI.

### Tradeoffs

Server/database setup adds auth, migrations, email and deployment work. PostGIS provides full-polygon checks but requires verified CRS, municipality crosswalks and geometry handling. IndexedDB preserves anonymous work on one browser profile, with explicit storage-failure handling. A local demo can precede those external integrations, but cannot be represented as the countywide launch.

## For Agents

### Context and evidence

The accepted product record is [the specification](../product-spec-v1-2026-09-26.md), [dated decisions](../product-decisions-2026-09-26.md) and [ADR 0006](0006-select-action-led-v1.md). The [technical design](../technical-design-v1-2026-09-26.md) defines schemas, API boundaries, AI limits, retention and failure behavior. [Source verification](../source-adapter-verification-2026-09-26.md) records sampled actual API behavior and remaining gaps.

### Alternatives considered

Browser-only integration cannot enforce shared AI budgets or protect server credentials. A workflow framework/graph database adds operational cost before a demonstrated need. Recreating the app discards verified comparison, evidence and export behavior without solving a requirement.

### Consequences and constraints

Architecture is recommended, not accepted. No infrastructure was provisioned, no runtime model selected and no application implementation performed in this handoff. Source reuse, rule review, full jurisdiction tests, endpoint validation, email delivery and retention remain release gates. Existing balances do not authorize new purchases or top-ups. Public deployment requires later authority.

### Revisit when

Review this recommendation before implementation. Revisit orchestration only if bounded request records and relational dependency transactions cannot meet measured workflow needs. Revisit spatial infrastructure if permitted data or verified geometry behavior cannot support reliable countywide identity.

### Related material

- [Phased implementation plan](../implementation-plan-v1-2026-09-26.md)
- [Current handoff](../handoffs/current.md)
