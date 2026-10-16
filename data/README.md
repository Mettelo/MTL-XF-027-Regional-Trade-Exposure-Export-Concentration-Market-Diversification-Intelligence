# MTL-XF-027 — Data workspace

## Required sources and cohort

HMRC Regional Trade in Goods. The England file contains the regional trade series from Q1 2021 onward and is updated quarterly.

Freeze the agreed HMRC England Figure 1 ODS, intended quarterly coverage from Q1 2021 onward. Inspect its actual sheet dimensions and endpoint. The core is regional aggregate trade assessment. Country/product concentration is conditional: if those dimensions are absent, deliver an explicit evidence-gap and extension specification rather than invented concentration metrics.

[Source register and exact URLs](SOURCE_REGISTER.md)

**Current state:** specification only. No raw datasets have been downloaded or uploaded in this build. Expected size, row count and history statements from the earlier agreement require verification against the actual files. Do not mark the cohort frozen until the manifest and metadata are complete.

## Controlled acquisition and preparation

1. Read [SOURCE_REGISTER.md](SOURCE_REGISTER.md); use the exact agreed URLs and official publisher documentation.
2. Validate that the response is the expected CSV/ODS/XLSX/ZIP rather than an error page. Inspect archive contents and sheet names where relevant.
3. Record resolved URL, UTC retrieval, release, coverage, filename, bytes, SHA-256 and licence evidence. Log discrepancies before changing sources.
4. Preserve original bytes in an approved immutable snapshot; later upload only where instructed and redistribution is permitted.
5. Record source fields, types, valid values, suppression, units and publisher methodology in [metadata](metadata/README.md).
6. Implement the analytical grain below, verify keys/cardinality and account for excluded/quarantined records.
7. Reconcile at least five published measures and create curated outputs reproducibly in the team repository.

## Analytical grain

Quarter × published region × trade flow × measure/unit, plus only dimensions actually present. Imports, exports and balances remain distinct. Do not infer partner-country or product breakdowns from regional totals.

## Required metric contract

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

## Mandatory quality risks

- Regional aggregate data cannot reveal partner-country or product concentration.
- Goods trade excludes services; nominal trade values do not directly measure real growth or regional prosperity.
- Avoid summing overlapping regions, flows or incompatible allocation methods.

1. Reconcile five region/quarter/flow values and verify workbook units.
2. Test a missing quarter invalidates a four-quarter total.
3. Test that country/product metrics are unavailable when required dimensions are absent.
4. Explain any difference between summed regions and the published England total.

## Folder ownership

- [raw](raw/README.md): unmodified approved source snapshots; guidance only at present.
- [reference](reference/README.md): governed code lists, hierarchies and crosswalks.
- [metadata](metadata/README.md): source notices, schema, glossary, lineage and manifest evidence.

Curated data, processing code, logs and test results belong in the team delivery repository. Preserve a reproducible boundary between source inputs and generated products. Do not add personal, confidential or paid-source data.
