# MTL-XF-027 — Acceptance criteria and domain tests

**Business decision owner:** Director of International Trade & Regional Economic Strategy. **Decision:** Which English regions and broad product sections warrant export-support investigation, and what additional individual-market evidence is needed before targeted diversification recommendations?

## Delivery sign-off

| ID | Deliverables | Required pass evidence | Acceptance owner |
| --- | --- | --- | --- |
| AC1 | D1 | Eight user requirements cover the commissioned questions, named stakeholder actions and core/extension boundary. | Business Analyst / Director of International Trade & Regional Economic Strategy |
| AC2 | D2 | 100% of used source files have approved provenance, version/coverage, licence, retrieval UTC and SHA-256. Required fields and reference versions are checked. | Data Governance Analyst |
| AC3 | D3 | Every input row is accounted for; keys and all many-to-many/hierarchy effects have explicit checks and no unexplained duplication. | Data Engineer / independent reviewer |
| AC4 | D4 | Five source cells reconcile within a declared rounding tolerance; all material differences and non-additive totals are explained. | Domain specialist |
| AC5 | D5 | All 9 metric contracts are classified core/conditional and have tested definitions; no unsupported fields or fabricated unavailable values. | Data Governance Analyst / BI Developer |
| AC6 | D6 | Five findings cover all business questions or evidence gaps; period, eligible population, magnitude, comparison and limitation are visible. | Domain analyst |
| AC7 | D7 | The project-specific baseline and alternative below are implemented; eligibility, scenario changes, reason codes and evidence requests are visible. | Director of International Trade & Regional Economic Strategy |
| AC8 | D8 | Five BI measures reconcile to curated outputs; all filters/reset/export retain the scope, units and limitations. | BI Developer / operational UAT user |
| AC9 | D9 | DT1–DT10 have actual execution evidence and expected/actual outcomes; no unresolved critical/high defect. | Independent reviewer |
| AC10 | D10 | A distinct member's clean rerun reproduces equivalent core outputs with documented environment and checks. | Independent rerun reviewer |
| AC11 | D11 | Two-page maximum briefing and 15–20 minute presentation answer the decision and assign investigation owners without unsupported outcomes. | Director of International Trade & Regional Economic Strategy / Mettelo panel |
| AC12 | D12 | Every member links substantive authored and reviewed work, including handover or presentation contribution. | Delivery Lead |

## Project-specific business success

1. Regional outputs use S2 or an approved equivalent; S1 is explicitly England context.
2. Every concentration metric declares category level, complete denominator and suppressed/unallocated treatment.
3. The final brief distinguishes SITC-section concentration, partner-group exposure and unavailable individual-country concentration.

## Required prioritisation and sensitivity

Compare regional export weakening and broad product-section concentration as separate review dimensions. Compute section HHI/top-three shares only from a complete non-overlapping section partition that reconciles to its parent. Partner-group exposure is labelled at its actual aggregation level. Compare latest-quarter and trailing-four-quarter scenarios where the frozen tables provide sufficient contiguous history.

Record each case's entity/segment, valid period, supporting measures, reason code, scenario position, missing evidence, responsible operational role, next review and manual-review trigger. Fewer than ten cases is valid; padding unsupported cases fails acceptance.

## DT1–DT10 — minimum executed domain tests

| Test | Input / action | Expected pass evidence |
| --- | --- | --- |
| DT1 | Reconcile five S2 region/period/flow values and confirm currency units. | Five selected published values reproduce within declared source precision, with explicit source coordinates and scope. |
| DT2 | Test missing-quarter handling or reject unsupported rolling calculations. | The invalid comparison, join or denominator is rejected or flagged according to the documented rule; no silent fallback. |
| DT3 | Block country-level metrics when only broad partner groups are supplied. | The edge case produces an explicit unavailable/exclusion result or a supported calculation, with affected rows quantified. |
| DT4 | Quantify any residual between available regional/component sums and a compatible parent. | The domain boundary remains visible in the analytical output and BI product; no unsupported inference. |
| DT5 | England aggregate Figure 1 is loaded without S2 | Regional comparisons are blocked; no invented regional rows. |
| DT6 | Section shares are 0.5, 0.3 and 0.2 in a complete toy partition | HHI = 0.38 on 0–1 scale, or 3,800 on 0–10,000 scale; scale is labelled. |
| DT7 | Only the top three products are supplied without the remainder | Do not calculate full-distribution HHI or imply complete market coverage. |
| DT8 | EU/non-EU shares are available but individual countries are not | Label broad-group exposure; country-level concentration remains unavailable. |
| DT9 | Region components omit unallocated trade | Reconcile to a compatible parent or show the residual explicitly. |
| DT10 | Quarterly history spans a methodology break | Flag or exclude incompatible changes; document the affected comparison. |

Worked values are **synthetic test fixtures**, not claims about the public data or simulated client. For each test retain requirement ID, source/input or fixture, expected result, actual result, evidence link, tester, independent reviewer and date. DT1–DT4 additionally require the documented project-specific rule; their general evidence descriptions do not waive the named domain condition. Add dashboard/filter tests as needed beyond these ten.

## Scope gate and unresolved issues

**Mandatory core:** Retain agreed England Figure 1 as contextual source S1. Add the official Q2 2026 accompanying ODS as required regional source S2 to support the repository's regional scope; freeze its actual historical coverage and use only matching periods. Core delivery includes English ITL1 comparisons, available mutually exclusive SITC-section exposure and EU/non-EU or other valid partner-group splits. If S2 cannot support a required dimension, the Week 2 gate blocks that output until a registered official replacement is approved.

**Optional extensions:** Individual-country HHI/top-three-market shares require an exhaustive compatible country extract and are optional until registered. Detailed product-by-country interactions, services trade and causal export-support impact are outside core. An England aggregate is never relabelled an English region.

A mandatory source/field gap blocks the affected deliverable and must be resolved by a registered official replacement or approved, versioned scope change. An explicitly optional result may be unavailable with a reason and a useful evidence request. Neither missing raw data nor unexecuted tests may be marked passed.

A critical/high defect materially changes a headline value, cohort, recommendation, provenance or reproducibility and blocks release. Lower-impact issues require a named acceptance owner and disclosed impact. All panel feedback and approvals must be recorded honestly as simulated where applicable.
