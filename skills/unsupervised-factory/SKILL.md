---
name: unsupervised-factory
description: Design, run, diagnose, and evaluate unsupervised research workflows, especially clustering, topic discovery, representations, and cross-corpus comparisons. Use for empirical method selection or evaluation; ordinary data cleaning and fixed-label extraction belong to unstructured-data workflows.
---

# Unsupervised factory

Produce a defensible decision about a method and its useful scope, with source-linked outputs and a reproducible record. A useful preliminary theme, a repeatable computation, and a validated scientific finding are different outcomes.

## Establish the job

Start from the actual question, existing protocol, latest user corrections, and authorized deliverable. Choose the relevant mode:

- **Find evidence for a known question:** retrieval, followed by source review. Clustering is optional, not a prerequisite.
- **Discover candidate structure:** exploratory clustering, factors, topics, or anomaly candidates. Define what a useful result would enable.
- **Compare methods:** freeze the comparison contract and development/evaluation exposure before running candidates.
- **Diagnose a failed result:** inspect the first failed layer and its raw evidence before changing parameters.
- **Review existing work:** inspect saved reports and receipts; do not rerun experiments or open protected raw data merely to reconstruct history.

For method selection and corpus changes, read [design.md](references/design.md). For evaluation or failure diagnosis, read [validation.md](references/validation.md). For relevant historical traps, consult [lessons.md](references/lessons.md); its dated results are examples, not current project state or universal thresholds.

## Preserve the experiment contract

1. Identify the inference target and analysis unit: document, occurrence, sentence group, claim, participant, or another domain unit. Keep the mapping from derived rows to their source and context.
2. Record inclusion rules, strata, deduplication, missingness, preprocessing, representation, model, parameter range, selection rule, and evaluation unit. Use the project's existing record; otherwise adapt [run-plan.json](assets/run-plan.json).
3. Separate document roles, periods, products, and providers when they change the question. Pool only with a stated comparison purpose. Unknown dates are metadata unless the question genuinely requires exact temporal eligibility.
4. A request to add missing documents does not authorize changing sentence units, filters, partition rules, or cluster counts. Make the requested comparable rerun first; label additional redesigns separately.
5. Label every result's exposure: exploratory/development, frozen evaluation on fresh families, or retrospective reconstruction. Reused known examples remain development evidence even when a new script scores them.

## Execute a discriminating comparison

- Start with the simplest credible baseline and a small set of alternatives that test different explanations. Preserve matched data, scope, budget, and evaluation rules; report unavoidable differences.
- Audit the representation before clustering: empty/zero-feature rows, truncation, duplicates, length effects, missing features, normalization, and source-role signals. For tabular inputs, justify scaling and treatment of categorical or missing values.
- In held-out evaluation, fit learned preprocessing on the allowed training side. Keep near-duplicate passages, versions, and source families together where leakage is plausible. A full-corpus exploratory fit can be valid, but does not become an inductive generalization test.
- Choose the method for the requested structure. Hard partitions, overlapping topics, latent dimensions, and anomaly scores are different objects. Do not force all of them through a fixed-k clustering pipeline.
- Preserve fixed input IDs, hashes, code/configuration versions, seeds, raw outputs, errors, excluded rows, and execution receipts. Reuse unchanged cached vectors only when their complete transformation identity matches.
- Use `experiment-notebook` when available to maintain the existing journal. Otherwise record the question, comparison, results, failures, and decision beside the run. Respect current project compute/storage instructions; a historical server path is not authorization for new spend or relocation.

For parallel work, partition independent tasks such as corpus accounting, method rationale, and blinded source review. Give each worker the same frozen contract and explicit output ownership. Keep fitting and dependent evaluation ordered. More agents are not independent human validators.

## Evaluate separate claims separately

Use the layers in [validation.md](references/validation.md): data integrity, representation coverage, statistical structure, semantic fidelity, and usefulness for the intended task. Do not collapse them into one approval badge.

- Report stability over meaningful perturbations, coverage/noise, cluster-size distribution, and relevant internal diagnostics. Compare assignments on common IDs and distinguish missing memberships from unstable ones.
- Inspect representatives **and** a documented sample of ordinary members, boundary cases, outliers, and excluded material. Good examples do not establish cluster-wide coherence or corpus completeness.
- Treat generated names as hypotheses. Preserve the actors, mechanisms, conditions, time, modality, and evidence role in their supporting passages. Allow mixed clusters, multiple themes, unresolved cases, and abstention.
- Distinguish literal quote validity from whether a quote supports the claimed theme; distinguish broad topic overlap from faithful coverage of specific assertions. Label assistant and model judgments as such.
- If claiming independent semantic validation, obtain genuinely independent judgments with a clear rubric, source access, and disagreement handling. A second pass by the same model is a diagnostic, not an independent reference.
- Fix thresholds and selection rules before the evaluation they govern. Explain a threshold's use; do not import a past project's value as a universal standard or lower it post hoc to manufacture a pass.

## Respond to failure and finish

Inspect raw scores when an aggregate is zero, missing, clipped, or overridden. Report the override, raw metric, population, and exclusions separately. Removing difficult rows changes coverage and the evaluated population.

When multiple repairs fail the same gate, test the shared premise: unsuitable analysis units, source-role confounding, poor representation, overlapping concepts, or no useful partition may explain the result better than another sweep. Preserve failed runs and prefer a bounded discriminating experiment. Retrieval, an evidence index, or preliminary qualitative themes can remain useful when stable clusters do not emerge.

Deliver the requested artifact plus a concise decision: retain/change/reject the method for the stated purpose; evidence and denominators; material limitations; and the next test only if needed. Link assignments, source-backed themes, exclusions, configuration, and results where useful. Report what actually ran and what remains proposed. Do not promote navigation clusters into legal categories, company-performance rankings, or compliance findings without the separate evidence those claims need.
