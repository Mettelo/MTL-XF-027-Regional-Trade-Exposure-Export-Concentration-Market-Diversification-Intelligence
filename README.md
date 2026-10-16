# MTL-XF-027 — Regional Trade Exposure, Export Concentration & Market Diversification Intelligence

**Mettelo Project Studio** · Cross-Functional · Master project specification  
**Client:** Confidential Regional Economic Development & Trade Board  
**Accountable simulated executive:** Director of International Trade & Regional Economic Strategy  
**Sector:** International Trade / Economic Development  
**Team:** 3–5 people · **Window:** 8 weeks  
**Status:** documentation revised; file acquisition and cohort freeze pending  
**Review cadence:** quarterly regional export and diversification review

> This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

## Business setting

The simulated regional economic-development and trade board reviews export-support priorities each quarter. Its programme team must decide which English regional/product-section exposures deserve outreach scoping and which requests need more detailed market evidence.

## Business problem

The Director of International Trade & Regional Economic Strategy needs to explain why a region or broad product section should receive export-support investigation. An England-wide goods chart cannot locate a regional issue, and an EU/non-EU split cannot identify individual destination-market dependency. Nominal export movement alone also does not distinguish a broad volume story from price or product-mix effects.

Without the correct regional evidence, outreach priorities can follow the loudest headline rather than a supported exposure. The commission is a quarterly regional review using the required HMRC accompanying tables, with a separate England context panel and a clear route from broad exposure to a specific further market enquiry.

## Commissioned decision

> Which English regions and broad product sections warrant export-support investigation, and what additional individual-market evidence is needed before targeted diversification recommendations?

## Practical use

At the quarterly board meeting, the Regional Economist selects an English ITL1 region and compares its goods-export movement and supported SITC-section mix with the England context. The Export Support Programme Lead checks whether a proposed case is robust to latest-quarter versus trailing-four-quarter comparison where compatible history exists.

The Director commissions a regional/section outreach-scoping enquiry or requests a detailed country extract before discussing destination diversification. The case records the exact broad exposure, programme owner and next evidence request. A partner-group split is never used to name a destination country, and goods evidence is not presented as the whole regional economy.

**Management handover:** A quarterly trade review pack with separate England and regional views, supported section/partner-group exposure, period sensitivity and an outreach-scoping register. Every proposed diversification enquiry must state whether country-level evidence is available or still required.

The full [business context](project/BUSINESS_CONTEXT.md) sets out stakeholders, decisions, evidence limits and proposed benefit measures.

## What must be delivered

1. Produce regional export/import comparisons from S2 and a separate England context view from S1.
2. Assess supported SITC-section mix and partner-group exposure at the actual table grain; reconcile exhaustive category sets before concentration calculations.
3. Compare latest-quarter and trailing-four-quarter review scenarios where history permits, then deliver up to ten regional/section investigation cases with individual-market evidence gaps.

The complete D1–D12 pack includes discovery, source governance, ingestion/model, quality, metric catalogue, analysis, investigation scenarios, BI, assurance/UAT, independent handover, executive briefing and contribution evidence. A dashboard by itself does not satisfy the commission.

## Fixed core and optional work

**Core:** Retain agreed England Figure 1 as contextual source S1. Add the official Q2 2026 accompanying ODS as required regional source S2 to support the repository's regional scope; freeze its actual historical coverage and use only matching periods. Core delivery includes English ITL1 comparisons, available mutually exclusive SITC-section exposure and EU/non-EU or other valid partner-group splits. If S2 cannot support a required dimension, the Week 2 gate blocks that output until a registered official replacement is approved.

**Extensions:** Individual-country HHI/top-three-market shares require an exhaustive compatible country extract and are optional until registered. Detailed product-by-country interactions, services trade and causal export-support impact are outside core. An England aggregate is never relabelled an English region.

Source support is checked at the Week 2 gate. A required output is blocked until its fields and cohort are verified; it cannot pass acceptance through a generic “data unavailable” disclaimer. An explicitly optional extension may remain unavailable with a reason. See [exact source URLs and verification evidence](data/SOURCE_REGISTER.md).

## Measurable project outcomes

1. Regional outputs use S2 or an approved equivalent; S1 is explicitly England context.
2. Every concentration metric declares category level, complete denominator and suppressed/unallocated treatment.
3. The final brief distinguishes SITC-section concentration, partner-group exposure and unavailable individual-country concentration.

All headline metrics require field lineage; five source values and five BI measures must reconcile. DT1–DT10 must be executed, a second member must reproduce the core outputs, and no critical/high defect may remain. These assess delivery quality; real-world savings or service improvement are not claimed.

## Investigation rules

Compare regional export weakening and broad product-section concentration as separate review dimensions. Compute section HHI/top-three shares only from a complete non-overlapping section partition that reconciles to its parent. Partner-group exposure is labelled at its actual aggregation level. Compare latest-quarter and trailing-four-quarter scenarios where the frozen tables provide sufficient contiguous history.

- S1 is an England aggregate; regional comparisons require S2. Grouped partners and SITC sections do not establish individual-country/product-market concentration.
- Goods trade excludes services; nominal values do not directly measure real growth or regional prosperity.
- Use complete non-overlapping category partitions; preserve allocation, revision and methodology-break caveats.

## Team and stakeholder ownership

Director of International Trade & Regional Economic Strategy approves business scope and the investigation recommendation. The Business Analyst, Data Governance Analyst, Data Engineer and BI Developer work with the specialist roles in the [project brief](project/PROJECT_BRIEF.md). Assign individual owners at kickoff and record substantive work and independent reviews in `CONTRIBUTIONS.md`.

## Delivery plan

Weeks 1–2: decision requirements and verified cohort. Weeks 3–4: model, reconciliation and metric definitions. Weeks 5–6: analytical findings, alternative investigation scenarios and BI draft. Weeks 7–8: simulated UAT, independent rerun, executive briefing and handover.

## Start here

1. [Project brief](project/PROJECT_BRIEF.md) and [business context](project/BUSINESS_CONTEXT.md).
2. [D1–D12 deliverables and metric contracts](project/DELIVERABLES.md).
3. [AC1–AC12 and DT1–DT10 acceptance tests](project/ACCEPTANCE_CRITERIA.md).
4. [Governance and sign-off](project/GOVERNANCE.md).
5. [Data workspace](data/README.md), [source register](data/SOURCE_REGISTER.md), [raw](data/raw/README.md), [reference](data/reference/README.md) and [metadata](data/metadata/README.md) guidance.
6. [Team repository standard](submission/TEAM_REPOSITORY_STANDARD.md), [submission guide](submission/SUBMISSION_GUIDE.md) and [final template](submission/FINAL_SUBMISSION_TEMPLATE.md).

## Master and team repositories

This master repository holds the Mettelo-controlled specification. Create `MTL-XF-027-<team-name>` under the **Mettelo GitHub organisation** and add every member's individual account. Delivery analysis, code, tests, BI and contribution evidence belong in that team repository. Use issues, branches, meaningful commits, PRs and reviews where practical.

The required master areas are `project/`, `data/` (including raw/reference/metadata guidance) and `submission/`; [the documentation index](project/README.md) explains their authority and current revision.

**Mettelo — Built for What’s Next**
