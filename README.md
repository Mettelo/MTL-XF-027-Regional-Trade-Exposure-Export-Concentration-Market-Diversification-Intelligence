# MTL-XF-027 — Regional Trade Exposure, Export Concentration & Market Diversification Intelligence

**Mettelo Project Studio** · Cross-Functional · Master specification  
**Client:** Confidential Regional Economic Development & Trade Board  
**Sector:** International Trade / Economic Development  
**Status:** Pre-launch; documentation ready, data acquisition/freeze pending  
**Recommended team:** 6–8 people · **Delivery window:** 8 weeks  
**Master repository:** `Mettelo/MTL-XF-027-Regional-Trade-Exposure-Export-Concentration-Market-Diversification-Intelligence`

> This is a **simulated confidential-client engagement** using official public/open data. The client label is fictional and intentionally anonymous. Do not imply a real external Mettelo customer, employment by that client, privileged access or confidential source data. Public source statistics remain public; the engagement framing does not make them confidential.

## Business challenge

**Regional Trade Exposure, Export Concentration & Market Diversification Intelligence.** An economic-development board needs to understand whether its regional economy is too dependent on a small number of export markets or product groups and where market-diversification support should be investigated.

Current reporting fragments the evidence needed for a repeatable management review. The team must explain which signals are reliable, which comparisons are valid and where further investigation is needed. No budget, operational failure or improvement outcome is asserted as an observed client fact.

## Commissioned decision

> What does the agreed regional trade-in-goods series establish about exposure and volatility, and what additional official country/product detail is required before making diversification recommendations?

The product supports a simulated stakeholder review. A dashboard alone is insufficient: the recommendation must be traceable to governed definitions, a reproducible model, reconciled analysis and a transparent investigation framework.

## Business questions

- How do regional export and import values change over comparable quarters?
- Which regions show persistent export weakness or volatility?
- How does each region's share of a compatible England total change?
- Does the source actually contain partner/product detail needed for concentration?
- Which official additional tables and denominator definitions would make diversification analysis defensible?

## Approved data and cohort

HMRC Regional Trade in Goods. The England file contains the regional trade series from Q1 2021 onward and is updated quarterly.

Freeze the agreed HMRC England Figure 1 ODS, intended quarterly coverage from Q1 2021 onward. Inspect its actual sheet dimensions and endpoint. The core is regional aggregate trade assessment. Country/product concentration is conditional: if those dimensions are absent, deliver an explicit evidence-gap and extension specification rather than invented concentration metrics.

Exact copyable URLs and acquisition gates are in [SOURCE_REGISTER.md](data/SOURCE_REGISTER.md). No raw data is uploaded by this build. Source coverage and size statements inherited from the agreement are expected values until controlled acquisition verifies them; current URLs are not a substitute for a frozen file manifest.

## What the team must build

1. Produce regional aggregate export/import trends, four-quarter totals and volatility diagnostics.
2. Audit workbook dimensions and write a signed scope statement showing whether country/product concentration is possible.
3. Shortlist up to ten regional investigation cases and deliver either a defensible concentration analysis with registered extensions or a precise official-data acquisition plan.

Produce the full D1–D12 delivery pack: discovery, governance, ingestion/model, quality, KPI catalogue, analysis, decision framework, BI, assurance/UAT, handover, executive briefing and contribution record. [Deliverables](project/DELIVERABLES.md) defines locations, dates and evidence for each.

## Core measures

| Metric | Required definition / calculation |
| --- | --- |
| Export value | Published goods export value in stated currency/unit. |
| Import value | Published goods import value in stated currency/unit. |
| Goods trade balance | Exports minus imports for the same region, quarter and scope; not a welfare measure. |
| Year-on-year export change | 100 × (exports / exports four quarters earlier − 1), requiring a positive base. |
| Regional export share | 100 × region exports / compatible England total; disclose unallocated trade and coverage. |
| Trailing four-quarter exports | Sum of four contiguous quarters; no rolling result for missing quarters. |
| Export variability | Standard deviation of comparable quarterly export growth over a declared window with at least eight observations. |
| Country/product concentration — conditional | Top-three share and HHI only after obtaining compatible mutually exclusive partner/product detail; otherwise mark unavailable. |

## Cross-functional ownership

| Accountable role | Project responsibility and evidence |
| --- | --- |
| Business Analyst / Delivery Lead | Own the commissioned decision for Confidential Regional Economic Development & Trade Board; record at least eight prioritised requirements, each linked to a deliverable and test; maintain weekly scope and decision logs. |
| Data Governance Analyst | Register every 027 input and critical field; approve the frozen cohort, licence evidence, glossary and 100% headline-KPI lineage before analysis. |
| Data Engineer | Implement the stated 027 analytical grain, ingestion and exclusions; deliver a clean rerun with row-count/checksum evidence and no unexplained key duplicates. |
| BI Developer | Build executive, diagnostic and quality views for the commissioned decision; reconcile at least five 027 dashboard measures and test every visible filter. |
| Trade & Regional Economy Analyst | Validate region/flow definitions and interpret at least five reconciled values. |
| Trade Data Governance Analyst | Own the dimension audit and register each additional partner/product source before concentration work. |
| Trade Policy & Risk Analyst | Write the regional investigation shortlist and test whether diversification claims exceed the available evidence. |

Roles may be combined by a smaller team, but each responsibility needs a named owner. A different member reviews critical calculations and final evidence wherever practical.

## Interpretation rules

- Regional aggregate data cannot reveal partner-country or product concentration.
- Goods trade excludes services; nominal trade values do not directly measure real growth or regional prosperity.
- Avoid summing overlapping regions, flows or incompatible allocation methods.

## Measurable success

- All source files and transformations have provenance and licence evidence; approved inputs have SHA-256 manifests.
- All headline metrics have tested definitions and source-field lineage.
- At least five published values and five dashboard measures reconcile with declared source rounding.
- At least five findings address the business questions and quantify materiality.
- Up to ten investigation cases have evidence, reason codes, owners and limitations; at least two priority scenarios are compared.
- At least ten UAT scenarios pass or have explicitly accepted low-impact limitations; no critical/high defect remains.
- A second member reproduces the core outputs from the same frozen inputs.

These are delivery acceptance thresholds, not promises of real-world service improvement. See [acceptance criteria](project/ACCEPTANCE_CRITERIA.md).

## Delivery sequence

Weeks 1–2: decision requirements, source inspection and freeze approval. Weeks 3–4: model, reconciliation and KPI definitions. Weeks 5–6: analysis, investigation framework and BI draft. Weeks 7–8: UAT, independent rerun, briefing and handover.

## Start here

1. Read the [project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. Review [deliverables](project/DELIVERABLES.md), [acceptance criteria](project/ACCEPTANCE_CRITERIA.md) and [governance](project/GOVERNANCE.md).
3. Inspect the [data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw guidance](data/raw/README.md), [reference guidance](data/reference/README.md) and [metadata guidance](data/metadata/README.md).
4. Create `MTL-XF-027-<team-name>` under the **Mettelo GitHub organisation**, add each member's individual account and follow the [team repository standard](submission/TEAM_REPOSITORY_STANDARD.md).
5. Use the [submission guide](submission/SUBMISSION_GUIDE.md) and [final submission template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master holds the challenge specification. Teams deliver their analysis and artefacts in their own Mettelo organisation repository. Do not submit team work by replacing this master specification. Use issues, branches, meaningful commits, PRs and reviews to demonstrate actual collaboration.

## Specification map

```text
README.md
project/README.md
project/PROJECT_BRIEF.md
project/BUSINESS_CONTEXT.md
project/DELIVERABLES.md
project/ACCEPTANCE_CRITERIA.md
project/GOVERNANCE.md
data/README.md
data/SOURCE_REGISTER.md
data/raw/README.md
data/reference/README.md
data/metadata/README.md
submission/README.md
submission/TEAM_REPOSITORY_STANDARD.md
submission/SUBMISSION_GUIDE.md
submission/FINAL_SUBMISSION_TEMPLATE.md
```

**Mettelo — Built for What’s Next**
