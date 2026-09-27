# Review of the supplied proposal-comparison research

Recorded by Rushi Patel with coding-assistant support on September 27, 2026. The research assignment and product discussion originated September 26. The supplied PDF is an AI-generated research synthesis, not a practitioner interview, primary record, or approved product specification. Its creation time is not independently established by this intake.

Source: [A Decision-Focused Proposal-Comparison Brief for Pittsburgh Housing](decision-focused-proposal-comparison.pdf). Original-byte hash and intake metadata are in [the manifest](decision-focused-proposal-comparison.manifest.json). The PDF metadata names ChatGPT Deep Research as author. The original was supplied by Rushi; it was preserved without rewriting its claims.

## What was reviewed

Text was extracted from the 20-page PDF. Review focused on the product implications (pages 1-2), case chronology and comparison limits (pages 3-8), field specification (pages 9-12), sample and feedback questions (pages 13-15), unresolved evidence (pages 15-16), and source register (pages 17-20). Page 13 was rendered and visually inspected to confirm the comparison table structure. This is content review, not full-page visual QA or independent verification of all linked sources.

## Useful design proposals

| Report proposal | Potential benefit | Boundary before adoption |
|---|---|---|
| Give proposals explicit version dates/status | Avoid treating a superseded concept as a current option | Establish whether options were simultaneous or sequential |
| Separate regulatory changes from housing outcomes | Preserve the applicant's objective when requirements change | Do not rank fewer checks as inherently better |
| Track public commitments and their evidence status | Avoid flattening discussion, reported promises and formal conditions | Require underlying evidence before labeling a binding condition |
| End with role, document and reason | Make the brief useful for a project handoff | Test whether a delivery-side practitioner can act on it |
| Preserve financial claims as claims | Prevent developer estimates from becoming feasibility findings | No independent financial model is supplied |

These are candidates for the existing proposal-comparison design. They do not supersede ADR 0005, choose a new demo, or authorize a larger implementation.

## Case separation is essential

The report's Lanark case is an eight-home development/program, with a reported change from six attached and two detached homes to eight detached homes (pages 7-8 and 13-14). The existing repository demonstration is one parcel at **1623 LANARK ST**, PARID `0023C00208000000`. The report also discusses an advocacy example at **21 Lanark Street**.

Do not transfer zoning determinations, approvals, estimated costs, unit counts or geometry between these three references. A relationship has not been established by this review. Before using the eight-home case as application data, obtain project boundaries, parcel IDs, original/revised plans and the corresponding decisions. Consult the existing [single-parcel example](../../wiki/product/lanark-worked-example.md) for its separate evidence boundary.

## Claims and gaps to preserve

| Report content | Status in this intake | Required follow-up |
|---|---|---|
| Earlier and later Shur Save concepts have different height/unit counts | Reported historical comparison; not independently reverified here | Recover dated plans and establish option status |
| A hypothetical by-right Shur Save alternative lacks a recovered design | Explicit report limitation | Do not invent dimensions, housing yield or an approval outcome |
| Shur Save primary decisions/application PDFs were not retrieved | Report limitation | Obtain original records before encoding their full relief checklist |
| Current code enactment history is used to contextualize historical rules | Incomplete historical baseline | Check intervening amendments and archived rules; an original enactment date alone is insufficient |
| Eight-home Lanark revision reportedly preserves home count | Research claim, not verified revised approval | Obtain revised plan and zoning disposition |
| Lanark redesign cost/time estimates | Attributed estimates in the report | Do not use as audited costs, current benchmarks or a calculated feasibility result |
| ACTION-Housing video could not be retrieved by the research agent | Limitation of this particular report | Existing repository caption analysis remains separate evidence; do not erase it |

The report labels a sample as one page, but the sample table spans pages 13-14 and the feedback discussion continues on page 15. A genuinely concise practitioner handout still needs to be produced and tested.

## Next review sequence

1. Confirm the precise project and parcel identity for any proposed historical demonstration. Keep the current single-parcel prototype distinct while this is unresolved.
2. Obtain the original/revised site plan and decision record that would change a comparison conclusion. Prioritize the selected demo's evidence over completing every historical case.
3. Prepare a short brief that labels proposal status, persistent unknowns and the next document needed.
4. Ask a development/project manager: what is misleading, who would use it, and what action changes? No contact was made during this intake.

## Contribution and publication boundary

Rushi requested that the actual September 26 discussion and supplied PDF be documented and submitted in PRs on September 27. This note records that provenance without inventing commit times or claiming five separate work sessions. No raw Slack transcript, private contact details or attributed private feedback is included in the authored review. The source PDF contains no pasted Slack transcript; its mention of private concept feedback is a limitation statement, not a published quote.
