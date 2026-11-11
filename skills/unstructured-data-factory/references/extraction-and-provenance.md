# Extraction and provenance

Use this workflow for ingestion, repair, segmentation, normalization, deduplication, and source verification. Keep the existing pipeline when it already preserves the necessary information.

## Define the record before transforming it

Record the source identity and version separately from each derived unit. Typical identity fields are source ID, original filename or URL, content hash, title, publication/retrieval dates, source role, service or organization, reporting cycle, language, and document-family ID. Unknown fields stay unknown. Do not infer a document's legal status from its filename.

Choose identifiers that survive reruns. A source version plus a stable span anchor can identify a unit. If segmentation changes, version the unit map and record predecessor/successor relationships; do not silently attach old annotations to new text.

Preserve raw text and a normalized view. An offset must say which view it indexes and whether its units are Unicode code points, UTF-16 code units, bytes, PDF glyphs, or another representation. Record mappings when normalization changes addresses. PDF evidence can use page and bounding-box coordinates where text offsets alone are unreliable.

## Inspect source-specific failure modes

| Source | Check in the original | Preserve |
|---|---|---|
| PDF/report | Reading order, column crossings, headers, page continuations, table captions | Pages, boxes, table structure, section hierarchy |
| Web/policy snapshot | Navigation, repeated boilerplate, publication versus capture date, moved content | Snapshot date/version and canonical source |
| Interview/transcript | Speaker turns, interruptions, transcript corrections, consent scope | Pseudonymous speaker IDs and approved quotation scope |
| Scientific result | Units, confidence intervals, group definitions, endpoint and comparator | Full event, methods context, treatment direction |
| Table/list | Merged headers, row/column scope, qualifiers in notes | Cell/header associations and row context |

Use a deliberately varied pilot: normal documents, long and short units, scans, tables, page joins, and previously troublesome source types. Report its denominator and sampling rule. A bounded pilot supports a bounded claim.

Separate exclusion from uncertainty. A navigation menu may be excluded as non-content. An ambiguous scientific claim remains unresolved. A reported failure or nonimplementation can be substantive evidence. Keep reasons for exclusions and retain originals.

## Units and context

Do not assume sentence splitting yields complete claims. A sentence can need its preceding actor, a following exception, a table header, or a methods definition. Conversely, a paragraph can combine several actors and claims. Split only when each new unit retains its meaning; store wider source context separately from text embedded or classified.

For a changed segmentation, compare the old and proposed units on the same source sample. Review retained qualifiers, source coverage, split/merge errors, and downstream behavior. If unit change is the research variable, isolate it from codebook and model changes.

## Reuse and invalidation

Cache using a dependency fingerprint: source version, extraction/normalization version, unit text, model revision, preprocessing and relevant settings. Reuse only artifacts whose dependencies match. Do not re-normalize already validated cached vectors merely to enforce a cosmetic convention; numerical transformations can change downstream outputs. Recompute changed units and their dependent artifacts, and preserve the prior release.

Use content hashes to detect duplicate uploads, while retaining separate bibliographic or temporal identities when identical content belongs to distinct records. Avoid counting mirrors, repeated passages, or report revisions as independent evidence.

## Delivery checks

- Sample final records and follow their source pointers all the way to the original.
- Account for source and unit counts before and after cleaning, exclusions, deduplication, and splitting.
- Review affected cross-page and table evidence after a citation-map repair.
- Verify that a rerun reuses unchanged artifacts only when their dependencies match.
- Name remaining extraction uncertainty; do not describe the entire corpus as clean because a sample passed.

Keep audit detail in the methods record. Put only limitations that change interpretation into the audience-facing result.
