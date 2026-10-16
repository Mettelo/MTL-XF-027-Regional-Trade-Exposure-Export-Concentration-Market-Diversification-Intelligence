# MTL-XF-027 — Required deliverables and metric contracts

**Decision:** Which English regions and broad product sections warrant export-support investigation, and what additional individual-market evidence is needed before targeted diversification recommendations?  
**Business acceptance:** Director of International Trade & Regional Economic Strategy  
**Core scope:** Retain agreed England Figure 1 as contextual source S1. Add the official Q2 2026 accompanying ODS as required regional source S2 to support the repository's regional scope; freeze its actual historical coverage and use only matching periods. Core delivery includes English ITL1 comparisons, available mutually exclusive SITC-section exposure and EU/non-EU or other valid partner-group splits. If S2 cannot support a required dimension, the Week 2 gate blocks that output until a registered official replacement is approved.

All artefact locations refer to the team repository. Deliver the core before optional extensions. [The source register](../data/SOURCE_REGISTER.md) documents evidence status; required field support is a G1 release condition.

## D1 — Discovery & requirements

**Due:** Week 1 · **Location:** `docs/01-discovery/` · **Owner:** Business Analyst

Map the quarterly regional export and diversification review, stakeholder needs, current reporting failures and target decision. Eight prioritised requirements must cover the business questions, scope gates and usable outputs.

**Pass evidence:** Each requirement has an accountable user, artefact, test and acceptance owner.

## D2 — Sources, governance & cohort contract

**Due:** Week 2 · **Location:** `data/; docs/02-data-governance/` · **Owner:** Data Governance Analyst

Complete the source-to-deliverable support matrix and classify core, fallback and optional inputs. Retain agreed England Figure 1 as contextual source S1. Add the official Q2 2026 accompanying ODS as required regional source S2 to support the repository's regional scope; freeze its actual historical coverage and use only matching periods. Core delivery includes English ITL1 comparisons, available mutually exclusive SITC-section exposure and EU/non-EU or other valid partner-group splits. If S2 cannot support a required dimension, the Week 2 gate blocks that output until a registered official replacement is approved.

**Pass evidence:** Every used input has provenance, exact version/coverage, licence evidence and SHA-256; conditional scope cannot be signed off without supporting fields.

## D3 — Reproducible model & ingestion

**Due:** Week 3 · **Location:** `src/; sql/; docs/03-data-model/` · **Owner:** Data Engineer

Implement raw preservation, selection, schema checks, curated facts and dimensions. Quarter × published region × trade flow × measure/unit, plus only dimensions actually present. Imports, exports and balances remain distinct. Do not infer partner-country or product breakdowns from regional totals.

**Pass evidence:** Zero unexplained duplicate keys or join inflation; every input row accounted for as retained/excluded/quarantined.

## D4 — Quality, source reconciliation & exceptions

**Due:** Week 3 · **Location:** `tests/; docs/04-data-quality/` · **Owner:** Independent reviewer + domain specialist

Execute source, denominator, missingness, boundary and linkage checks against the risk 'An England chart or partial category list may be misrepresented as regional market-concentration evidence.'

**Pass evidence:** Reconcile five source values from at least two periods or segments; retain source coordinates, precision and explanations for non-additive totals.

## D5 — Governed metric catalogue

**Due:** Week 4 · **Location:** `docs/05-kpi-catalogue/` · **Owner:** Domain specialist + Data Governance Analyst

Implement the 9 metric contracts below; distinguish unconditional core metrics from gated extensions.

**Pass evidence:** Each core metric has purpose, raw fields, formula, grain, denominator/unit, missing/zero handling, owner, refresh and test; conditional items have explicit eligibility or unavailable status.

## D6 — Domain assessment

**Due:** Week 5 · **Location:** `analysis/; docs/06-analysis/` · **Owner:** Domain analyst

Produce regional export/import comparisons from S2 and a separate England context view from S1. Assess supported SITC-section mix and partner-group exposure at the actual table grain; reconcile exhaustive category sets before concentration calculations.

**Pass evidence:** At least five supported findings answer the five questions or document a genuine evidence gap; each includes magnitude, scope, comparison and limitation.

## D7 — Investigation framework & scenarios

**Due:** Week 6 · **Location:** `docs/07-decision-framework/` · **Owner:** Director of International Trade & Regional Economic Strategy (business acceptance)

Compare regional export weakening and broad product-section concentration as separate review dimensions. Compute section HHI/top-three shares only from a complete non-overlapping section partition that reconciles to its parent. Partner-group exposure is labelled at its actual aggregation level. Compare latest-quarter and trailing-four-quarter scenarios where the frozen tables provide sufficient contiguous history.

**Pass evidence:** Publish eligibility, component definitions, scenario differences and up to ten supported cases; every case names a service role, evidence request and review trigger.

## D8 — Decision-support BI

**Due:** Draft Week 6; final Week 7 · **Location:** `dashboard/` · **Owner:** BI Developer

Build overview, diagnostic and quality pages for the quarterly regional export and diversification review. Show period, units, definitions, missingness and core/extension status.

**Pass evidence:** Five headline values reconcile; every visible filter and reset tested; accessible static export plus free review/build path.

## D9 — Assurance & simulated UAT

**Due:** Week 7 · **Location:** `docs/08-assurance-uat/` · **Owner:** Independent reviewer

Execute DT1–DT10 below, plus any tool-specific calculations and filter tests. Record expected/actual evidence, requirement links and defects.

**Pass evidence:** All ten mandatory domain cases evidenced; no critical/high issue remains; accepted lower-impact limitations have named review.

## D10 — Technical & operational handover

**Due:** Week 8 · **Location:** `docs/09-technical-handover/` · **Owner:** Data Engineer + a second-member reviewer

Provide environment, immutable manifest, end-to-end run, output checks, troubleshooting and refresh/change process.

**Pass evidence:** A second member regenerates equivalent core outputs without undocumented edits and records checks, environment, duration and result.

## D11 — Executive briefing & presentation

**Due:** Week 8 · **Location:** `deliverables/` · **Owner:** Business Analyst + specialist service roles

Deliver maximum two-page briefing and 15–20 minute presentation to Director of International Trade & Regional Economic Strategy: decision, five findings, scenario comparison, investigation actions, evidence gaps and next review.

**Pass evidence:** Every numeric claim links to tested evidence; explicitly show a case where action is not yet supported.

## D12 — Contribution & delivery record

**Due:** Weekly; final Week 8 · **Location:** `CONTRIBUTIONS.md` · **Owner:** Delivery Lead

Link actual authored work, reviews, issues/PRs/commits and presentation/handover contributions for every member.

**Pass evidence:** All responsibilities have owners and evidence; commit count alone is insufficient.

## Metric contracts — authoritative definitions

| Metric | Definition / support condition |
| --- | --- |
| Regional exports / imports | Published S2 values by English ITL1 region, quarter and flow, with stated currency scale; S1 England totals are context only. |
| Goods balance | Compatible regional exports minus imports; no welfare interpretation. |
| Comparable export change | 100 × (current / same quarter prior year − 1) with positive base and comparable source periods. |
| Regional share | 100 × region exports / compatible England total; show unallocated/residual treatment. |
| Trailing four-quarter exports | Sum four contiguous genuine quarters from S2; unavailable if only rolling annual snapshots are supplied. |
| SITC-section exposure | Section exports / matching regional exports, using a complete mutually exclusive partition. |
| Section concentration | Top-three share and sum of squared section shares only with an exhaustive reconciled section set; label HHI scale. |
| Partner-group exposure | Published regional EU/non-EU or other non-overlapping group split; not individual-country concentration. |
| Country-market concentration — extension | Country HHI/top-three-market share only after registering complete compatible country-level data. |

For each metric add source ID and actual raw fields, business purpose, formula, grain, valid population, unit, numerator/denominator, hierarchy, suppression/zero/missing handling, owner, refresh and test evidence. Verify source rounding before setting a reconciliation tolerance. A conditional item is not silently promoted into core; a core requirement is not silently waived.

## Project-specific outcomes

1. Regional outputs use S2 or an approved equivalent; S1 is explicitly England context.
2. Every concentration metric declares category level, complete denominator and suppressed/unallocated treatment.
3. The final brief distinguishes SITC-section concentration, partner-group exposure and unavailable individual-country concentration.

See [DT1–DT10 and investigation rules](ACCEPTANCE_CRITERIA.md) for worked pass/fail cases. Source schemas, specific period selections and reference versions must be signed at G1. Keep calculation definitions here; other guidance pages link to this contract rather than maintaining competing copies.
