# MTL-XF-027 — Required deliverables

**Commissioned decision:** What does the agreed regional trade-in-goods series establish about exposure and volatility, and what additional official country/product detail is required before making diversification recommendations?

All locations below refer to the team's delivery repository. The master repository defines the requirements and contains no completed analysis. Owners are assigned from [the project roles](PROJECT_BRIEF.md).

## D1 — Discovery & decision requirements

**Due:** Week 1  
**Team artefact location:** `docs/01-discovery/`

Decision statement; stakeholder map; as-is reporting to investigation-review process; at least eight prioritised requirements. Answer these questions: How do regional export and import values change over comparable quarters? Which regions show persistent export weakness or volatility? How does each region's share of a compatible England total change? Does the source actually contain partner/product detail needed for concentration? Which official additional tables and denominator definitions would make diversification analysis defensible?

**Acceptance evidence:** All requirements have an owner, priority, deliverable and test ID; domain analyst approves scope.

## D2 — Governed sources & cohort

**Due:** Week 2  
**Team artefact location:** `docs/02-data-governance/; data/`

Freeze the agreed HMRC England Figure 1 ODS, intended quarterly coverage from Q1 2021 onward. Inspect its actual sheet dimensions and endpoint. The core is regional aggregate trade assessment. Country/product concentration is conditional: if those dimensions are absent, deliver an explicit evidence-gap and extension specification rather than invented concentration metrics. Register exact files, metadata, licences, checksums, coverage and critical fields; record rejection of unavailable dimensions.

**Acceptance evidence:** 100% of inputs registered; no claimed freeze until acquisition evidence exists.

## D3 — Reproducible analytical model

**Due:** Week 3  
**Team artefact location:** `src/; sql/; docs/03-data-model/`

Quarter × published region × trade flow × measure/unit, plus only dimensions actually present. Imports, exports and balances remain distinct. Do not infer partner-country or product breakdowns from regional totals. Deliver load, type checks, hierarchy handling, lineage, exclusions and environment instructions.

**Acceptance evidence:** A second member regenerates equivalent curated outputs from identical inputs; no unexplained duplicate analytical keys.

## D4 — Quality & reconciliation

**Due:** Week 3  
**Team artefact location:** `docs/04-data-quality/; tests/`

Profile missingness, suppression, valid values, keys and join coverage. Reconcile five region/quarter/flow values and verify workbook units. Test a missing quarter invalidates a four-quarter total. Test that country/product metrics are unavailable when required dimensions are absent. Explain any difference between summed regions and the published England total.

**Acceptance evidence:** Every input row is accounted for as retained, excluded or quarantined; five published cells reconcile within declared rounding.

## D5 — KPI catalogue

**Due:** Week 4  
**Team artefact location:** `docs/05-kpi-catalogue/`

Define all 8 measures listed below with formula, grain, denominator, unit, source fields, exclusions, owner, refresh and limitations.

**Acceptance evidence:** 100% headline metrics trace to source fields and tested transformations; conditional unavailable measures are explicitly marked.

## D6 — Domain analytical assessment

**Due:** Week 5  
**Team artefact location:** `analysis/; docs/06-analysis/`

Produce regional aggregate export/import trends, four-quarter totals and volatility diagnostics. Audit workbook dimensions and write a signed scope statement showing whether country/product concentration is possible.

**Acceptance evidence:** At least five evidence-backed findings state period, population, comparison, magnitude, uncertainty and limitation; negative findings count.

## D7 — Investigation decision framework

**Due:** Week 6  
**Team artefact location:** `docs/07-decision-framework/`

Shortlist up to ten regional investigation cases and deliver either a defensible concentration analysis with registered extensions or a precise official-data acquisition plan. Record eligibility, thresholds, weights if used, reason codes and manual review triggers.

**Acceptance evidence:** Every shortlisted case has metrics, rationale, owner and evidence gaps; at least two scenarios compared; fewer than ten is valid where evidence is insufficient.

## D8 — BI decision-support product

**Due:** Draft Week 6; final Week 7  
**Team artefact location:** `dashboard/`

Executive overview answering 'What does the agreed regional trade-in-goods series establish about exposure and volatility, and what additional official country/product detail is required before making diversification recommendations?' plus diagnostic and data-quality views; visible periods, units, denominator notes, resettable filters and accessible labels.

**Acceptance evidence:** Five headline measures reconcile; every filter tested; export screenshots/PDF plus reproducible build or free access instructions.

## D9 — Independent assurance & UAT

**Due:** Week 7  
**Team artefact location:** `docs/08-assurance-uat/`

At least ten scenarios including the four project-specific tests below; requirement-to-test matrix, expected/actual evidence, defect log and simulated stakeholder feedback.

**Acceptance evidence:** No unresolved critical/high defect; accepted lower-severity limitations have a named reviewer and explicit impact.

## D10 — Technical & operational handover

**Due:** Week 8  
**Team artefact location:** `docs/09-technical-handover/`

Clean setup, architecture, frozen input manifest, run/refresh steps, output checks, troubleshooting and change-control process for Regional Trade Exposure, Export Concentration & Market Diversification Intelligence.

**Acceptance evidence:** Another member reproduces the core outputs without undocumented edits and records environment, duration and discrepancies.

## D11 — Executive recommendation

**Due:** Week 8  
**Team artefact location:** `deliverables/`

Maximum two-page briefing and 15–20 minute presentation: commissioned decision, five findings, investigation shortlist, sensitivity, missing evidence, responsibilities and next review.

**Acceptance evidence:** Every quantitative claim links to an artefact/metric; no unsupported causal, policy or operational guarantee.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8  
**Team artefact location:** `CONTRIBUTIONS.md; delivery issues/PRs`

Record who delivered and reviewed each MTL-XF-027 work package, including domain, governance, engineering, BI and assurance contributions.

**Acceptance evidence:** Every member links to substantive artefacts and review/presentation evidence; commit count alone is insufficient.

## Required KPI definitions

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

For every metric record business purpose, formula, source fields, grain, unit, numerator/denominator, exclusions, suppression, zero-base behaviour, owner, refresh and test evidence. Do not populate conditional metrics from invented fields.

## Mandatory domain scenarios

1. Reconcile five region/quarter/flow values and verify workbook units.
2. Test a missing quarter invalidates a four-quarter total.
3. Test that country/product metrics are unavailable when required dimensions are absent.
4. Explain any difference between summed regions and the published England total.

## Review gates

Week 2: cohort and source approval. Week 4: model, DQ and metrics approval. Week 6: analytical and decision-framework review. Week 8: UAT, independent rerun and final panel review. Record reviewer, date, artefact version and decision at every gate.
