# Methods and results

## Freeze the scope before describing it

Start with the manuscript's actual analysis, not the newest or largest dataset in the repository. Establish study ID, corpus version, unit of analysis, period, inclusion/exclusion rule, and completed review state. A prospective expansion can be a future direction without becoming the evidence for current findings.

Record source coverage by relevant strata, such as service × reporting cycle × document role. Distinguish unavailable, not collected, collected but unprocessed, processed but unreviewed, excluded by design, and source-reviewed with no relevant evidence found. Missing outputs cannot support absence findings. Uneven coverage limits comparison even when every parser completed.

## Describe a reproducible final design

Use only elements needed to assess this study:

- **Sampling and rationale:** Why these cases, periods, source types, or participants answer the question; whether sampling supports population inference.
- **Source preparation:** Retrieval dates/versions, deduplication, extraction, segmentation, context expansion, and consequential exclusions. Quantify relevant losses and failures.
- **Operationalization:** Definitions, coding scheme or task specification, units, ambiguous cases, and decision rules.
- **Analysis:** Transformations, model/configuration revisions, comparison conditions, selection process, and role of automated tools.
- **Review:** Who or what reviewed which material, how disagreement was handled, and what remains unreviewed. Assistant-generated review is not independent human validation.
- **Evaluation:** Exposure state, split construction, reference provenance, baseline, metric/denominator, uncertainty where justified, and protocol changes.
- **Reproducibility:** Data/code versions, run records, access limits, and which results have actually been replayed.

Do not force this order as a fixed section template. Use the order that explains the final study with the least backtracking. Move exploratory iterations to a notebook or appendix unless they explain a consequential design choice or selection bias.

When a methods statement lacks a source, inspect code/configuration/protocol/receipts. Keep retrospective reconstruction labeled as such. An executable script's default does not prove the reported run used it. A results file does not prove a job completed successfully.

## Connect results to the question

Report effect or performance with its denominator, coverage, comparison, and scope. Keep failed and null results that change the scientific conclusion. Separate descriptive patterns from hypotheses about their cause. Do not use a method's complexity as evidence of improvement.

For model comparisons, distinguish changes in method from changes in evidence, supervision, fallback rules, compute, and evaluation exposure. A development improvement requires fresh evaluation before a generalization claim. For clustering or topic discovery, report stability, coverage, semantic review, and sensitivity rather than treating visually separated groups as validated categories.

Use tables or figures when they let the reader inspect a pattern or comparison more directly than prose. Captions should identify the unit, measure, population/scope, and material caveat. Do not interpret an omitted card, unrun analysis, or unreported value as zero.

## Separate four kinds of verification

| Check | Supports | Does not establish |
|---|---|---|
| Parse/schema/integrity checks | The pipeline handled expected files and shapes | Correct semantics or complete evidence |
| Numerical replay | Reproduction of a specified computation within stated tolerance | Valid labels, interpretations, or causal inference |
| Source and semantic review | Support for a bounded interpretation | Independent human validation unless performed |
| External or human outcome evaluation | The tested outcome under the observed design | Untested populations, deployments, or periods |

A reproducibility report must state its boundaries: cached replay, new encoding, generative inference, interpretation, and human adjudication are different activities. Preserve original outputs when fixing scoring or preprocessing, and explain whether published conclusions change.

## Limitations that change interpretation

Discuss coverage, selection, measurement, model/annotation validity, and inference limits where they affect a claim. Avoid a generic disclaimer paragraph repeated in every section. State what the reader can conclude and the specific additional evidence needed for a stronger claim. Do not describe an unapproved or unrun future study as the fix already in place.
