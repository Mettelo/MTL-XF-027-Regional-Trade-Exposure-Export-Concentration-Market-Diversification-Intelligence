# MTL-XF-027 — Project brief

This is a **simulated confidential-client engagement using official public/open data**. Client and stakeholder role labels describe a fictional engagement; do not claim a real external Mettelo customer, employment, endorsement or privileged data access. No raw data is uploaded by this specification update.

**Client:** Confidential Regional Economic Development & Trade Board. **Decision owner:** Director of International Trade & Regional Economic Strategy. **Team:** 6–8. **Duration:** 8 weeks. **Review:** quarterly regional export and diversification review.

## Business problem and commission

The board wants to target export support where dependence or weakening activity may be concentrated, but an England-wide EU/non-EU chart cannot tell it which English region or product section is driving exposure. A regional trade total also cannot reveal whether a few individual destination countries dominate. The project must provide the appropriate regional evidence and make the level of aggregation visible.

> Which English regions and broad product sections warrant export-support investigation, and what additional individual-market evidence is needed before targeted diversification recommendations?

## Core deliverable boundary

Retain agreed England Figure 1 as contextual source S1. Add the official Q2 2026 accompanying ODS as required regional source S2 to support the repository's regional scope; freeze its actual historical coverage and use only matching periods. Core delivery includes English ITL1 comparisons, available mutually exclusive SITC-section exposure and EU/non-EU or other valid partner-group splits. If S2 cannot support a required dimension, the Week 2 gate blocks that output until a registered official replacement is approved.

**Optional / out of core:** Individual-country HHI/top-three-market shares require an exhaustive compatible country extract and are optional until registered. Detailed product-by-country interactions, services trade and causal export-support impact are outside core. An England aggregate is never relabelled an English region.

File availability does not prove dimensional support. Before analytical build, the team completes the source→field→metric→deliverable matrix in [data guidance](../data/README.md). Missing mandatory support blocks the gate and requires an approved official replacement or scope decision.

## Analytical model

Quarter × published region × trade flow × measure/unit, plus only dimensions actually present. Imports, exports and balances remain distinct. Do not infer partner-country or product breakdowns from regional totals.

The source contract above controls where a general grain description is conditional. Do not create dimensions absent from the approved input.

## Objectives

1. Regional outputs use S2 or an approved equivalent; S1 is explicitly England context.
2. Every concentration metric declares category level, complete denominator and suppressed/unallocated treatment.
3. The final brief distinguishes SITC-section concentration, partner-group exposure and unavailable individual-country concentration.

## Business questions

1. How do regional export and import values change over comparable quarters?
2. Which regions show persistent export weakness or volatility?
3. How does each region's share of a compatible England total change?
4. How concentrated are complete SITC-section partitions, and what partner-group exposure is supported?
5. What individual-country detail is still needed before selecting specific export markets?

## Cross-functional delivery model

| Delivery role | Required project contribution |
| --- | --- |
| Business Analyst / Delivery Lead | Map the quarterly regional export and diversification review, document eight prioritised user requirements and maintain requirement→deliverable→test links; Director of International Trade & Regional Economic Strategy owns business approval. |
| Data Governance Analyst | Own the MTL-XF-027 source/metadata register, cohort decision, licence evidence and 100% headline-measure lineage; resolve the specific risk: An England chart or partial category list may be misrepresented as regional market-concentration evidence. |
| Data Engineer | Implement the declared facts, keys, hierarchy and join controls; account for every source row and deliver a second-member reproducible run at the chosen MTL-XF-027 scope. |
| BI Developer | Implement the quarterly regional export and diversification review overview, diagnostic and quality pages; reconcile five measures and ensure cohort/extension warnings survive filters and export. |
| Trade & Regional Economy Analyst | Validate region/flow definitions and interpret at least five reconciled values. |
| Trade Data Governance Analyst | Own the dimension audit and register each additional partner/product source before concentration work. |
| Trade Policy & Risk Analyst | Write the regional investigation shortlist and test whether diversification claims exceed the available evidence. |

Assign named team members and review partners at kickoff; roles may be combined, but a distinct member must review critical calculations and perform the final clean rerun. The executive and operational stakeholder roles are specified in [business context](BUSINESS_CONTEXT.md).

## Required investigation approach

Compare regional export weakening and broad product-section concentration as separate review dimensions. Compute section HHI/top-three shares only from a complete non-overlapping section partition that reconciles to its parent. Partner-group exposure is labelled at its actual aggregation level. Compare latest-quarter and trailing-four-quarter scenarios where the frozen tables provide sufficient contiguous history.

## Milestones and acceptance

| Gate | Reviewers | Evidence / decision |
| --- | --- | --- |
| G1 — scope/source, end Week 2 | Business Analyst + Data Governance Analyst + domain specialist | Approve actual period, geography, grain, required input and field support in a source-to-deliverable matrix. Official regional scope, S2 link and explanatory notes verified; workbook sheets, contiguous period coverage, partitions, suppression and checksums pending. Unsupported mandatory outputs remain blocked, not quietly reclassified as completed. |
| G2 — model/metrics, end Week 4 | Data Engineer + domain specialist + independent reviewer | Approve row accounting, keys, hierarchy, join cardinality, five source reconciliations and all core metric definitions. |
| G3 — analytical decision review, end Week 6 | Director of International Trade & Regional Economic Strategy + operational stakeholders | Compare regional export weakening and broad product-section concentration as separate review dimensions. Compute section HHI/top-three shares only from a complete non-overlapping section partition that reconciles to its parent. Partner-group exposure is labelled at its actual aggregation level. Compare latest-quarter and trailing-four-quarter scenarios where the frozen tables provide sufficient contiguous history. Retain an evidence-insufficient case and a manual review route. |
| G4 — release, end Week 8 | Simulated Mettelo panel + independent reviewer | Accept D1–D12 only after ten executed domain tests, five BI reconciliations, clean rerun evidence and resolution of all critical/high defects. |

D1–D12 are defined in [deliverables](DELIVERABLES.md). AC1–AC12 and DT1–DT10 are defined in [acceptance criteria](ACCEPTANCE_CRITERIA.md). No real production deployment, automatic funding/service allocation, private-client data or paid-source dependency is required.
