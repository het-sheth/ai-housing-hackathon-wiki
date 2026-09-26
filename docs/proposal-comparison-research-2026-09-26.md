# Independent check: proposal comparison on one Pittsburgh parcel

Date: 2026-09-26. This is a public-source research note, not a practitioner interview or product decision. It tests whether proposal comparison is plausible and distinct enough to validate. It does not establish demand, Pittsburgh coverage in commercial tools, or a scoring rubric.

## Findings

| Question | Public evidence | What follows |
|---|---|---|
| Does project scope affect Pittsburgh review? | The City says review depends on location and scope. Its planning guidance puts most single-family renovations, additions and new homes in Basic Zoning Review, while some locations and environmentally sensitive cases receive Site Plan Review. Its current Building and Development Application asks for work type and scope. | The proposed work must be an input. A repair-to-expansion change does not automatically change the review level. The exact site and plans matter. |
| Can a scope change alter the applicable rule check? | Current City Code section 921.03.A.1 addresses maintenance, remodeling and repair of a lawful nonconforming structure when nonconformity does not increase. Section 921.03.D.1 separately addresses enlargement and expansion, including compliance and non-increase conditions. | The proposed comparison has a real rule distinction. It is conditional, not evidence that either Lanark scenario is approved or needs a variance. Lawful status, nonconformity and dimensions remain unresolved. |
| Do practitioners consider alternatives? | In a public ACTION-Housing talk, the speaker retrospectively compared one taller building with two and discussed duplicated work/costs. The talk also described community discussions, utility delay and paid schematic, environmental and market-study work. | Alternatives and staged diligence occur in at least one local development account. This multifamily rental example does not validate a repair-versus-expansion product or show that software would have improved the decision. See `wiki/research/action-housing-video-findings.md`. |
| Is comparison already available elsewhere? | TestFit advertises side-by-side scheme comparison with design and financial measures, site constraints and reports. Rescope advertises source-cited parcel zoning and site constraints. Pittsburgh's public tools provide local zoning, parcel and process information. | Neither scenario comparison nor a cited parcel report is a unique feature. The reviewed product pages do not verify Pittsburgh rule accuracy or whether they answer the proposed small-project handoff question. |

## Assessment

The strongest supported claim is narrow: a Pittsburgh housing proposal's scope can change which rules must be checked, and a tool can explain that conditional difference alongside stable parcel facts. Existing products substantially overlap. We have not shown that a small developer or nonprofit needs this comparison, that it changes a real decision, or that the Lanark repair-versus-expansion pair produces a useful changed outcome beyond "more details needed."

To test the current prototype, hold all other assumptions constant and change only the work scope. Trace one changed rule with its missing inputs, identify one unchanged constraint, and show whether the next authority or evidence needed actually changes. If both scenarios lead to the same next action, say so and reconsider whether comparison is the right first interaction. Keep financial feasibility unassessed rather than converting absent inputs into ease. Ask a practitioner for one recent scope change and the artifact used to decide it. A public-source review cannot replace that test.

## TestFit comparison, checked again September 26

TestFit's Site Solver advertises scheme comparison, site massing, zoning metrics, cost inputs and PDF reports. Those are stronger than this prototype's current design and financial coverage. Its zoning help says parcel zoning comes from Zoneomics, can be unavailable, and user-edited setbacks are marked separately. Its zoning profile rates user-selected numerical metrics pass/fail. The documentation reviewed does not establish rule-by-rule Pittsburgh legal-use, repair-versus-expansion or variance interpretation. This is a documentation gap, not proof those capabilities are absent.

TestFit's Site Intelligence help says its major utility layer excludes water and sewer data. Its export help says mapped data layers, including topography, wetlands, flood and parcel information, do not export from a TestFit deal. The local prototype's brief carries its own source URLs, dates, conflicts and missing checks, but it does not verify utility capacity or most hazards either. No hands-on TestFit trial or direct report comparison has been completed. The proposed distinction is therefore a hypothesis about a local decision handoff, not a claim of overall superiority.

The local app currently defaults to two scenarios that differ only in work scope and conservatively leaves overall ease unrated. Its rule explanation changes, but both scenarios can still say review required and direct the user to confirm the pathway with the City. The interface should distinguish a changed explanation from a changed review outcome or next action before using the comparison as the central demo claim. The current app is described in `/home/het/personal/ai-housing-navigator/docs/current.md`; app work remains separate from this research repo.

## Evidence limits

- Vendor pages describe claimed capabilities; no account, Pittsburgh parcel trial, report comparison or paid feature check was performed.
- The City's general process pages do not decide an individual project's review route. The code sections do not establish Lanark's lawful use, current condition or full rule dependencies.
- The ACTION-Housing account is a historical public talk reviewed through automatic captions, not a prototype interview or a current code source.
- No product decision, scoring weights, financial assumptions or competitor gap is established here.

# Citations

1. City of Pittsburgh, [Zoning](https://www.pittsburghpa.gov/Business-Development/City-Planning/Zoning) and [Planning Application and Process](https://www.pittsburghpa.gov/Business-Development/City-Planning/Zoning/Planning-Applications-and-Processes), accessed 2026-09-26.
2. City of Pittsburgh, [Building and Development Application](https://www.pittsburghpa.gov/Business-Development/Permits-Licenses-and-Inspections/Permitting/Building-Development-Application), accessed 2026-09-26.
3. City of Pittsburgh, [Title 9, section 921.03](https://ecode360.com/45478965), accessed 2026-09-26.
4. [TestFit Site Solver](https://www.testfit.io/product/site-solver) and [Rescope Rezone](https://www.rescope.co/products/rezone/), vendor pages accessed 2026-09-26.
5. Pro-Housing Pittsburgh, [Building Affordable Housing by Action Housing](https://www.youtube.com/watch?v=vJ0ReB26gVA), video uploaded 2024-04-16; existing caption analysis in `wiki/research/action-housing-video-findings.md`.
6. TestFit, [Using Zoning Information](https://support.testfit.io/knowledge/using-zoneomics-information), [Zoning Profile and Deal Metrics](https://support.testfit.io/knowledge/getting-started/zoning-profile), [Site Intelligence Add-On](https://support.testfit.io/knowledge/the-site-intelligence-add-on-) and [Exporting Data](https://support.testfit.io/knowledge/getting-started/exporting-data), accessed 2026-09-26.
