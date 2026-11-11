---
name: unstructured-data-factory
description: Extract, organize, code, compare, and validate evidence from unstructured documents, PDFs, interviews, reports, and scientific papers. Use for corpus-to-evidence workflows and semantic extraction audits; route clustering or representation experiments to unsupervised-factory. Skip ordinary summarization of a short supplied passage.
---

# Unstructured data factory

Produce source-linked evidence that another reader can check. Optimize the representation for the research question before selecting a model. A parsed corpus, valid JSON, exact quotation, and supported interpretation are different achievements.

## Establish the task

Read the current project instructions, corpus manifest, and nearest existing analysis before changing the pipeline. Recover the question, deliverable, sources, unit of analysis, intended population, access constraints, and what counts as a supported result. Inspect available material before asking for facts it contains. Ask only about a consequential unresolved research choice; continue independent work meanwhile.

Choose the relevant branch:

| Need | Workflow |
|---|---|
| Repair or build a document corpus | [Extraction and provenance](references/extraction-and-provenance.md) |
| Code claims, extract events, or compare sources | [Semantic analysis](references/semantic-analysis.md) |
| Evaluate or improve an extractor | Semantic analysis plus the available experiment-notebook skill |
| Discover clusters/topics or compare representations | Hand verified units to unsupervised-factory; do not label a classification pipeline unsupervised |
| Write up findings | Pass the bounded evidence to paper-factory or presentation-factory |

For an already supplied excerpt or comparison packet, start at the analysis and verification stages. Preserve its IDs, source roles, schema, and any supplied codebook; do not re-ingest a corpus or build a new notebook unless needed. If only label names are supplied, state any provisional operational definitions rather than silently treating them as an established taxonomy. Verify quotations against the available excerpts and distinguish that check from inspecting the original documents.

Use relevant format tools for PDF, Word, spreadsheet, and connected files. Use the current tool documentation rather than copied API recipes. Do not send private interview text or restricted corpora to external services unless that processing is authorized.

## Production workflow

1. **Inventory.** Pin source versions, dates, roles, document families, inclusion criteria, and extraction status. Distinguish complete documents, retained excerpts, duplicate versions, and supporting references. Read-only retrospective work does not require opening sealed evaluation material.
2. **Choose units.** Preserve the smallest complete claim, turn, event, or table entry that answers the question. Keep qualifiers, negation, attribution, temporal scope, and comparison direction. Store neighboring context separately. Use the project's existing unit when changing it would change the study.
3. **Pilot extraction.** Inspect a bounded, diverse set of hard source layouts and ordinary cases. Compare extracted text with originals, including page boundaries, tables, footnotes, lists, OCR, and speaker attribution. Fix upstream defects before treating downstream noise as a model problem.
4. **Build provenance.** Retain immutable original files and source-addressable spans. Keep normalized model text linked to original offsets or bounding boxes; do not let cleaning silently invalidate citations. Use [the evidence record](references/evidence-record.yaml) as a field guide, adapting to an existing schema.
5. **Analyze.** Declare each operation: retrieval, classification, extraction, relation proposal, or interpretation. For codebook analysis, record definitions, boundary examples, ambiguous cases, and revisions. For scientific extraction, preserve the complete event and its shared source scope. For comparisons, distinguish provider claims, audit tests, responses, implementation evidence, and observed outcomes.
6. **Verify meaning.** Check source attribution, entities, outcome, polarity, time, conditions, and comparison orientation. A quotation can be exact while supporting a different claim. Use representative, boundary, negative, and missed cases; do not only inspect model-selected successes.
7. **Evaluate the change.** When comparing methods, use the same source evidence, exposure state, units, annotation policy, and compute accounting where possible. Retain a strong simple baseline. Separate software checks, extraction fidelity, reference-label agreement, semantic support, coverage, and practical usefulness. Record failures and post-hoc changes.
8. **Deliver and reconcile.** Save the requested evidence table, coded corpus, comparison packets, or report with source pointers, denominators, unresolved cases, and a concise method record. Update the existing experiment record when applicable. Report what is complete and which substantive checks remain unperformed.

## Decisions that prevent repeated failures

- Repairing quotations or citations can be worth retaining even if the proposed reasoning method loses to the baseline. Retain the infrastructure benefit without asserting a scientific improvement.
- Pairwise links do not establish a complete event. Do not join material–property and property–value edges into every possible triple without shared source support. Missing retained annotations are not automatically semantic negatives.
- A second pass by the same model is an internal check, not independent validation. A source audit by an exposed assistant must be named as such.
- Zero parser errors do not establish complete extraction or sound coding. Fix status displays that imply semantic validation from execution checks.
- A missing retrieved passage or missing comparison card is not evidence that a practice is absent. Define what was searched and the ascertainment limits.
- Freeze a review or evaluation policy before examining evaluation outputs. Keep original labels and scores when recording a possible reference error; adjudication is a separate, versioned activity.
- If source roles or claim units explain repeated errors, test that premise before adding another review agent or elaborate decoder.

## Scale the work sensibly

For a one-document repair, make the repair and inspect affected sources. For a research corpus, save the manifest and transformation record. For a comparison experiment, record the protocol and results. A short analysis of supplied comparison numbers can keep its evidence and missing-information record in the answer; it does not need a separate notebook or a paper-writing handoff unless that work is requested. Do not create a large tracking system for a small edit.

Parallelize independent source families or blinded reviews with disjoint output ownership. Give every worker the question, permitted sources, unit definition, schema, and evidence standard. The coordinator checks cross-worker consistency and owns the final interpretation. Agent agreement does not replace independent human judgment where that is part of the study.

Read [historical lessons](references/lessons.md) when an extraction or semantic failure resembles the prior work. These are bounded observations, not universal performance claims or permission to rerun old experiments.
