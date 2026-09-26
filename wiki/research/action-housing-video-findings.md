---
type: concept
title: ACTION-Housing video findings and product implications
description: Timestamped analysis of the full automatic-caption track, separating practitioner accounts from product hypotheses.
tags: [workflow, evidence, affordable-housing, product]
status: researched
updated: 2026-09-26
---

# ACTION-Housing video: what changes our product thinking

**Evidence upgrade:** Original English automatic captions for the full 71:01 video were retrieved on September 26, 2026 using yt-dlp. YouTube metadata gives April 16, 2024 as the upload date. This supersedes the earlier screenshot-only access limitation. It does not mean the audio or every slide was watched or that the presentation took place on its upload date.

The team reviewed the timestamped caption text across the talk. Automatic captions misrecognize names, acronyms and numbers. Speaker recollections and estimates are historical accounts, not current regulations, measured market prevalence or independent project audits. Original screenshots remain useful for cross-checking visible numbers. Full captions are not republished; `docs/action-housing-video-provenance.json` records acquisition details and a hash.

## Evidence relevant to our workflow

| Time | What the speaker describes | Product implication and limit |
|---|---|---|
| 16:18-17:02 | ACTION-Housing used available parking reductions but still saw parking go unused on its projects. | A concrete practitioner concern linking requirements to project design. His generalization is about his experience, not a surveyed prevalence statistic. Do not implement 2024 parking rules without checking current code. |
| 17:40-18:26 | Energy efficiency and access to transport/opportunity are organizational priorities. | Mission and resident costs matter beyond site ease. This is stronger than assuming all nonprofits share one objective. |
| 27:16-28:52 | A two-building Lawrenceville project near Penn Avenue opened in 2021 after construction began in 2019. A small lot led to loft-unit design. | Actual physical constraints affected the design. Exact property identity still needs corroboration before importing parcel facts. |
| 29:15-30:01 | In retrospect he would have preferred one taller building rather than two, explaining that two buildings duplicated infrastructure/work and raised costs. | Direct evidence that alternatives and tradeoffs matter. It does not establish that a software comparison was missing or that zoning alone caused the outcome. |
| 30:12-32:05 | Lawrenceville organizations facilitated multiple meetings covering allowable development, community plans and preferences; schematic design followed. A neighboring resident's view concern was discussed. | Real actors and artifacts: community organizations, developer, meetings, community plans and schematic design. Do not label every negotiated preference a legal prohibition. Exact parcel ownership allocation in the captions is ambiguous. |
| 32:33-33:17 | ACTION-Housing primarily develops rental housing and holds/manages projects over time. | This evidence comes from a rental developer, not a single-home CLT sale workflow. Do not conflate the two personas. |
| 36:17-40:31 | The budget example includes hard/soft costs, reserves, fees, funder-driven design requirements and compliance work; he dates construction to August 2019. | The screenshots' budget is historical, not a 2026 cost model. Funding conditions can affect design and administrative effort. |
| 41:19-42:02 | He recalls a roughly four-month utility-related delay before construction accelerated during COVID-era price disruption. | A specific infrastructure/process issue. Captions render the utility name imperfectly; no independent cause/duration audit. Zoning clearance would not establish utility readiness. |
| 43:37-46:06 | He separates application preparation, award waiting, architectural/engineering work and construction, and describes increasing numbers of funding sources bringing compliance work. | Show development stages and unknown dependencies separately. His rough timing is not a predictive schedule or validated delay multiplier. |
| 57:07-58:14 | When asked about application cost, he names schematic design, environmental work and a market study. Direct expenditures are more readily quantified than staff time. Detailed architectural spending can be staged after funding confidence. | Concrete support for a decision about what diligence to commission and when. No evidence of a specific spreadsheet, CRM, approval role or quantified time saving. |
| 58:20-59:55 | He describes selective applications, building project support, uncertainty over awards, then finding investors through a syndicator and an RFP. | Funding success cannot be inferred from parcel characteristics. RFP is a documented artifact; not a proposed integration requirement. |
| 64:29-67:54 | Community advocacy and residents supporting affordable housing at meetings mattered to project discussions. | Community process is not reducible to a parcel score. Do not score residents or infer neighborhood opposition from demographics. |

## What this supports and what it challenges

**Stronger support:** Development alternatives can have concrete cost/design tradeoffs, and a useful review must separate formal rules, physical conditions, funding requirements and community preferences. The project discussion gives us a better discovery question than asking for general feature opinions.

**Challenge to our leading persona:** The clearest alternative described is two multifamily buildings versus one taller building. It does not validate the proposed repair-versus-expansion tool for a small nonprofit rehabilitating one home. Supporting the example literally would require site assembly, massing/design, funding and other analysis beyond the weekend boundary.

**Keep the narrow build, constrain its claim:** Use the talk as motivation and a source for practitioner questions. Do not switch to automatic building design or a comprehensive pro forma. The app can show supported rule implications and evidence requests; a practitioner must judge whether that changes a real decision.

**Do not treat this as a customer interview:** No one reviewed our prototype. We have no observed software usage, willingness to adopt, staff approval chain or proof of time saved. The speaker's experience represents one organization and project context.

## Corrections and caption quality

1. The budget now has more context: the speaker associates the ongoing example with construction beginning in 2019 and opening in 2021. Still do not automatically attribute it to Sixth Ward Flats merely because later reusable slides bear that title.
2. Around 62:49-63:16, he explicitly says the project being discussed did not have the veterans set-aside shown in the later slide context. This reinforces the risk of treating every slide as one consistent project record. The screenshot accurately records its slide text, but it is not proof the current example had that set-aside.
3. Around 60:45-60:52, captions contain an equity amount inconsistent with the visible $11,692,000 figure in the supplied slide. Treat this as a transcription discrepancy, not a corrected financial fact. Names and LIHTC terminology are also repeatedly mistranscribed.
4. The transcript supplies historical statements about zoning, funding and tax programs. Current governing sources must supply app rules; the talk supplies workflow and project experience.

## Next practitioner question

In the Lawrenceville example, when did the team first compare one taller building with two buildings, what documents were available then, and which constraint ultimately determined the choice? Could an earlier rule comparison have changed that decision, or were community agreements, funding and site conditions decisive?

For our smaller proposed user, ask separately whether they have an analogous recent repair-versus-expansion decision. Do not transfer the answer across project types without evidence.

# Citations

Pro-Housing Pittsburgh, [Building Affordable Housing by Action Housing](https://www.youtube.com/watch?v=vJ0ReB26gVA), uploaded April 16, 2024; captions retrieved September 26, 2026. Timestamp links: [parking](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=978s), [design alternative](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=1755s), [community/design process](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=1812s), [budget context](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=2177s), [utility delay](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=2479s), [development stages](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=2617s), [diligence artifacts](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=3427s), [set-aside clarification](https://www.youtube.com/watch?v=vJ0ReB26gVA&t=3769s).

[Previously inspected screenshots](/wiki/research/action-housing-presentation-excerpts.md), [current product proposal](/wiki/product/proposal-comparison.md). These are linked analyses of the same source, not independent corroboration.
