# TypeSafe Jev: bounded evaluation

Checked September 26, 2026. Documentation review only, no API call, account or key access. Het asked whether Jev/System One models can be used. Provider selection is not accepted.

Official documentation describes Choice, Score and Noul typed decisions, with probability distributions and confidence for Choice/Score. Jev does not generate narrative explanations. A Node 20+ JavaScript/TypeScript SDK and HTTP API are documented. Launch post dated September 15, 2026 describes early access; actual account access remains unverified.

Candidate use: classify a user-provided proposal description into independent bounded fields, e.g. expansion stated, added unit stated, reconstruction stated, each with explicit unknown/ambiguous outcomes and user confirmation. Code applies verified rule predicates; authored templates or a separate generative model explain results. If input is already a structured form, use it directly without redundant model calls.

Do not use Jev's Score primitive as a validated Development Ease rubric or model confidence as probability of approval. Schema validity is not factual/legal correctness. The vendor's limitations page warns about numerical precision, date comparisons, multi-step reasoning, irrelevant context and adversarial input. An evaluation must include negation, conflicting documents, missing lawful use and user instructions embedded in evidence. Measure errors on labeled examples before deciding thresholds. Access and housing-domain performance are untested; do not make the weekend depend on early-access admission.

Sources, all accessed September 26, 2026:
- https://docs.typesafe.ai/introduction : primitives and non-generative behavior.
- https://docs.typesafe.ai/introduction/quickstart : API/key setup.
- https://docs.typesafe.ai/sdk/javascript : @typesafe-ai/sdk and Node 20+.
- https://docs.typesafe.ai/confidence : confidence derives from output probability distribution; thresholds depend on domain performance.
- https://docs.typesafe.ai/model-jaggedness/jev-1.13 : limitations, last reviewed September 17, 2026.
- https://typesafe.ai/blog/introducing-system-one-models-and-jev : September 15 launch, early access and benchmark caveats. Vendor performance claims are not independently verified here.
