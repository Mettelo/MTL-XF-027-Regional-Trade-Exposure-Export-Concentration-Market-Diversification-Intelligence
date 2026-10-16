# MTL-XF-027 — Data workspace and support gate

## Core contract

Retain agreed England Figure 1 as contextual source S1. Add the official Q2 2026 accompanying ODS as required regional source S2 to support the repository's regional scope; freeze its actual historical coverage and use only matching periods. Core delivery includes English ITL1 comparisons, available mutually exclusive SITC-section exposure and EU/non-EU or other valid partner-group splits. If S2 cannot support a required dimension, the Week 2 gate blocks that output until a registered official replacement is approved.

## Optional work

Individual-country HHI/top-three-market shares require an exhaustive compatible country extract and are optional until registered. Detailed product-by-country interactions, services trade and causal export-support impact are outside core. An England aggregate is never relabelled an English region.

## Acquisition state

No raw data is uploaded by this update. Official documentation checks are recorded in [SOURCE_REGISTER.md](SOURCE_REGISTER.md). File payloads, full schemas, bytes/checksums and final reuse/freeze approvals remain pending where stated. Keep publication-level evidence distinct from acquired-file evidence.

## Required source-to-deliverable matrix

Before analysis, create a row per headline measure/required comparison:

`requirement_id | deliverable_id | metric | core_or_extension | source_id | actual_field_or_sheet | valid_grain | coverage | unit_denominator | metadata_evidence | support_status | owner | decision`

Allowed support statuses: documentation-supported; payload-verified; unsupported; optional-not-activated. “Documentation-supported” alone is insufficient for a completed data freeze. If a mandatory field is absent, block its output and resolve the source or approved scope; do not fabricate values or silently waive the requirement.

## Controlled preparation

1. Use registered exact URLs and inspect actual content type, archive members or sheets.
2. Record version, resolved URL, separate retrieval timestamps, bytes, SHA-256 and licence evidence.
3. Approve the actual cohort and scope matrix at G1.
4. Preserve original bytes; transform into curated facts with documented types, keys, hierarchies and joins.
5. Account for retained/excluded/quarantined rows and quantify all mapping gaps.
6. Reconcile five source values and execute [DT1–DT10](../project/ACCEPTANCE_CRITERIA.md).

## Model and measures

Quarter × published region × trade flow × measure/unit, plus only dimensions actually present. Imports, exports and balances remain distinct. Do not infer partner-country or product breakdowns from regional totals.

The core contract above controls conditional dimensions. Metric formulas have one authoritative home: [DELIVERABLES.md](../project/DELIVERABLES.md). Do not create another incompatible formula copy in the data README.

## Data areas

- [Raw snapshots](raw/README.md): unmodified source bytes only when later authorised and permitted.
- [Reference data](reference/README.md): category/entity/period mappings with version and cardinality.
- [Metadata](metadata/README.md): manifest, dictionary, methodology, lineage and support/freeze decisions.

**Specific control:** An England chart or partial category list may be misrepresented as regional market-concentration evidence.
