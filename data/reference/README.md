# MTL-XF-027 — Reference mappings

References support the approved [model and cohort](../README.md). Do not assume a mapping exists solely because entity names look similar.

Required acquisition checks: Required S2 download: https://assets.publishing.service.gov.uk/media/6aa2aaa2c5796a7a179c665c/RTS_Accompanying_tables_2026_Q2.ods . Register the release as Q2 2026 and inspect actual region, period, flow, units, section and partner-group fields. Avoid assuming a full country×product×quarter cube.

For each mapping record source/version, licence, key, definition, valid dates, uniqueness, relationship cardinality, unmatched coverage and responsible domain steward. Quantify every unmapped category/entity. Keep totals distinct from components and do not multiply fact rows through many-to-many crosswalks.

Analyst-created groupings and eligibility thresholds are labelled project assumptions. If they affect case selection, show their effect in [the scenario comparison](../../project/ACCEPTANCE_CRITERIA.md). Candidate raw field names or download references in the source register still require actual version validation.
