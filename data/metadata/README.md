# MTL-XF-027 — Metadata, lineage and freeze evidence

Metadata makes regional trade exposure, export concentration & market diversification intelligence reproducible. This folder currently contains guidance; no acquisition manifest or source sign-off is claimed.

## Required records after acquisition

- Source manifest: source ID, exact/resolved URL, retrieval UTC, actual release, filename, bytes, SHA-256, archive members/sheets and coverage.
- Publisher methodology and licence/attribution evidence with provenance and retrieval date.
- Schema and field dictionary: name, type, meaning, units, key role, missing/suppression markers and valid values.
- Business glossary and critical data elements, with named steward and approved definitions.
- Grain, hierarchy and join-cardinality documentation.
- Field-level lineage from raw fields through transformations to each headline metric/dashboard measure.
- Quality profile, row-accounting reconciliation, exclusions, unresolved exceptions and their decision impact.
- Freeze approval, change log and later revision comparisons.

## Model contract

Quarter × published region × trade flow × measure/unit, plus only dimensions actually present. Imports, exports and balances remain distinct. Do not infer partner-country or product breakdowns from regional totals.

## Metric definition coverage

- Export value: Published goods export value in stated currency/unit.
- Import value: Published goods import value in stated currency/unit.
- Goods trade balance: Exports minus imports for the same region, quarter and scope; not a welfare measure.
- Year-on-year export change: 100 × (exports / exports four quarters earlier − 1), requiring a positive base.
- Regional export share: 100 × region exports / compatible England total; disclose unallocated trade and coverage.
- Trailing four-quarter exports: Sum of four contiguous quarters; no rolling result for missing quarters.
- Export variability: Standard deviation of comparable quarterly export growth over a declared window with at least eight observations.
- Country/product concentration — conditional: Top-three share and HHI only after obtaining compatible mutually exclusive partner/product detail; otherwise mark unavailable.

Every listed metric needs source fields, transformation/formula, valid grain, unit, numerator/denominator, exclusions, zero/missing behaviour, refresh expectation, owner and test reference. Mark conditional metrics unavailable if the actual source cannot support them.

Store actual evidence only; never invent publisher schema, a completed licence review, a checksum or a stakeholder approval. See [source register](../SOURCE_REGISTER.md) and [acceptance criteria](../../project/ACCEPTANCE_CRITERIA.md).
