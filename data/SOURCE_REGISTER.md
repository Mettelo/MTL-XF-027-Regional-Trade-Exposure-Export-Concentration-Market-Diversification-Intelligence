# MTL-XF-027 — Source register and verification record

**Project:** Regional Trade Exposure, Export Concentration & Market Diversification Intelligence  
**Documentation review:** 16 October 2026  
**State:** official documentation checked; acquired-file validation and freeze approval pending.  
**Steward:** Data Governance Analyst, with the project domain specialist.

## Source/cohort decision

Retain agreed England Figure 1 as contextual source S1. Add the official Q2 2026 accompanying ODS as required regional source S2 to support the repository's regional scope; freeze its actual historical coverage and use only matching periods. Core delivery includes English ITL1 comparisons, available mutually exclusive SITC-section exposure and EU/non-EU or other valid partner-group splits. If S2 cannot support a required dimension, the Week 2 gate blocks that output until a registered official replacement is approved.

**Outside core:** Individual-country HHI/top-three-market shares require an exhaustive compatible country extract and are optional until registered. Detailed product-by-country interactions, services trade and causal export-support impact are outside core. An England aggregate is never relabelled an English region.

## Official publication and methodology references

| Official reference | URL |
| --- | --- |
| Q2 2026 regional accompanying tables | https://www.gov.uk/government/statistical-data-sets/uk-regional-trade-in-goods-statistics-second-quarter-april-to-june-2026-accompanying-tables |
| Q2 2026 explanatory notes | https://www.gov.uk/government/statistics/uk-regional-trade-in-goods-statistics-second-quarter-april-to-june-2026/uk-regional-trade-in-goods-statistics-second-quarter-april-to-june-2026-explanatory-notes |
| Official regional release | https://www.uktradeinfo.com/trade-data/regional/2026/uk-regional-trade-in-goods-statistics-second-quarter-2026/ |
| Figure 1 description in official commentary | https://www.gov.uk/government/statistics/uk-regional-trade-in-goods-statistics-first-quarter-january-to-march-2026/uk-regional-trade-in-goods-statistics-first-quarter-january-to-march-2026-commentary |

References above were inspected for this revision. They establish only the evidence described below; they are not a completed file acquisition, licence clearance or signed freeze.

## Verification findings

HMRC describes Figure 1 as England's export/import series split by EU/non-EU. The Q2 accompanying tables are advertised as ITL1 data with SITC sections and country groupings, so S2 is added to resolve the regional scope gap. Explanatory notes describe nominal values, allocation caveats and changes in data collection; confirm sheet coverage and exhaustive category partitions in the acquired workbook.

**Field/reference mapping and acquisition instructions:** Required S2 download: https://assets.publishing.service.gov.uk/media/6aa2aaa2c5796a7a179c665c/RTS_Accompanying_tables_2026_Q2.ods . Register the release as Q2 2026 and inspect actual region, period, flow, units, section and partner-group fields. Avoid assuming a full country×product×quarter cube.

**Remaining status:** Official regional scope, S2 link and explanatory notes verified; workbook sheets, contiguous period coverage, partitions, suppression and checksums pending.

## Exact copyable file URLs

Original agreed URLs are retained. Entries labelled required supplement/reference or fallback are explicit changes from the initial pack. Do not silently replace an input with a newer release.

### S1 — England Figure 1 — context only

```text
https://assets.publishing.service.gov.uk/media/6a9fe44f62ec7fe7bedf5129/Figure_1-Englands_trade_in_goods_first_quarter_January_to_March_2021_onwards.ods
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Use for England context only; regional analysis uses S2.

### S2 — Required regional accompanying tables — Q2 2026

```text
https://assets.publishing.service.gov.uk/media/6aa2aaa2c5796a7a179c665c/RTS_Accompanying_tables_2026_Q2.ods
```

**Acquisition:** pending; no source bytes uploaded. Record actual version, coverage, schema and licence before approving use. Core source reference; actual file identity remains to be verified.

## File validation and licence record

For every actually used input record:

`source_id, role_core_reference_fallback_extension, original_url, resolved_url, retrieved_utc, actual_release, filename, bytes, sha256, format, sheets_or_members, rows, geography, period_start, period_end, grain, schema_version, methodology_evidence, licence_notice, attribution, redistribution_conditions, approved_by, approval_date`

Retain the relevant publication/file notices, including exceptions and third-party conditions. Do not assume all publishers use the same licence. A stated publication licence does not remove the need to check file-specific terms. Keep unverified values pending; never invent a hash or approval.

## Support and freeze decision

Complete the [source-to-deliverable matrix](README.md). The domain specialist verifies actual grain, units, period comparability and supported metrics; the steward verifies identity and reuse terms. Required missing fields block dependent core outputs. Every activated extension is separately registered. Where a fallback is used, record why, which original it replaces, overlap handling and impact on outputs.

If an agreed URL fails, seek the same official archived release and record evidence. A browser format limitation does not prove a file is unavailable, and a successful page fetch does not prove payload integrity. Preserve the frozen version and metadata in the approved location so future website changes do not silently alter the cohort.
