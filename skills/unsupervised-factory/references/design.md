# Design the smallest informative experiment

Read this when selecting a method, changing a corpus, or setting up a comparison. The choices below are general methodological guidance; historical evidence is separately identified in [lessons.md](lessons.md).

## Start from the decision, not the algorithm

Write one sentence naming the object to recover and what the user will do with it. Examples: retrieve claims about a provision; discover recurring mechanisms within reports; compare their occurrence across services; compress a measurement matrix; flag unusual records for review. These require different outputs and evaluation.

| Needed object | Candidate starting point | Check before proceeding |
| --- | --- | --- |
| Evidence relevant to a known issue | Lexical retrieval, then an embedding or hybrid alternative | Recall of relevant passages, scope matching, and source review; no need to invent themes first |
| A navigable partition | K-means or a suitable hierarchical baseline | Geometry, distance, scaling, cluster-size imbalance, and assignment to new cases |
| Variable-density groups with unassigned points | Density-based clustering | Parameter sensitivity and coverage/noise; excluding most data is not automatically a quality gain |
| Overlapping textual themes | Factor/topic models or multi-label qualitative coding | Whether components have coherent support and preserve meaningful mixed membership |
| Latent dimensions for compression | PCA or another justified factorization | Reconstruction/variance objective and domain interpretation; a factor need not be a real-world construct |
| Candidate anomalies | An anomaly score matched to the population | False-alarm burden, contamination assumptions, subgroup effects, and source review |

Use current official documentation for implementation details and estimator assumptions. The [scikit-learn clustering overview](https://scikit-learn.org/stable/modules/clustering.html) compares geometry and scalability; its [decomposition guide](https://scikit-learn.org/stable/modules/decomposition.html) distinguishes component objectives. These are starting points, not evidence that a particular method fits the user's corpus.

For a named method outside this guide, read its primary paper/documentation, describe the needed assumptions, and establish a simple baseline. Do not claim our past topic-modelling work validates unrelated unsupervised methods.

## Corpus and unit contract

Keep a compact inventory with source ID, family/version, role, period/scope, eligibility decision/reason, raw location/hash, extraction version, derived unit IDs, and inclusion count. Separate unique texts from their occurrences; deduplication should not erase meaningful differences in speaker, context, period, or document role.

Before a rerun, produce a configuration difference: requested change, expected changed inputs, and every additional methodological change. A comparable rerun keeps the other settings fixed where possible. If corpus size makes a prior setting infeasible, explain the consequence and preserve a matched subset comparison rather than silently substituting a new experiment.

Keep structured records, navigation, and substantive prose distinguishable. Including all relevant documents does not require admitting every extracted fragment. If filtering is changed, report coverage and error changes, not just the final number of rows.

## Representation and split design

- Evaluate at the unit and dependency level that supports the claim. Source-family or temporal splits may be needed; random passage splits can leak repeated boilerplate and document context.
- Identify learned transforms, including vocabulary, IDF, scaling, feature selection, dimensionality reduction, and clustering. Fit them on allowed training data for inductive tests. A fixed external embedding model still needs version and exposure documentation.
- Count zero vectors and out-of-vocabulary rows in each evaluation direction. Inspect whether short text, language, OCR damage, or special document roles explain them.
- Compare one representation change while holding clustering fixed, then one clustering change while holding representation fixed, when the question is attribution. Do not interpret a wholesale pipeline replacement as evidence for one component.
- Treat two-dimensional maps as exploratory displays. If clustering uses reduced features, evaluate that complete pipeline and compare against unreduced or simple linear-reduction alternatives where feasible; visual islands alone are insufficient evidence.
- For longitudinal/cross-company comparisons, separate actual changes in content from changing document mix, extraction, vocabulary, prevalence, and labels. Independent fits need a documented alignment method; identical cluster numbers do not establish topic identity.

## Bounded selection

State the credible baseline, candidate mechanisms, permitted parameter ranges, sampling/seed plan, primary selection criterion, minimum useful coverage, semantic-review plan, and resource limit. Use pilot failures to refine a development protocol; freeze the revised protocol before fresh evaluation. Keep all searched candidates in the record so the chosen result is interpretable.

One fixed seed tests repeatability of that run. Multiple seeds test one source of sensitivity. Neither replaces source-family resampling, corpus perturbations, semantic review, or downstream usefulness. Repeatedly producing the same interpretation may merely reproduce the same mistake.

## Explain where guidance actually enters

For seeded or semi-supervised work, show the actual chain: who reads the codebook, whether positive and negative examples select inputs or constrain an objective, what the clustering algorithm receives, and when themes are inferred. An LLM assigning parent classes before ordinary clustering is not equivalent to seed-constrained clustering. Settle that distinction before interpreting a pilot as the requested method.

Expose the run's model, prompt/template version, configuration, assignment files, representative texts, and theme outputs. The user should be able to trace a theme to the code and source samples without guessing which script produced it. Leave deliberately unseeded categories unseeded; do not invent examples to fill a schema.

For corpus additions, reconcile changes in unit counts and cluster counts against the prior run. Explain effects of changed eligible documents, grouping, and settings separately. An unexpected count change is a reason to inspect the run contract, not to defend a redesigned pipeline merely because it completed.
