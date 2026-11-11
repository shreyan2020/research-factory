# Validation and failure diagnosis

Use the layers below to identify what an experiment has actually established. A prototype may be delivered with partial validation when clearly scoped; missing semantic review does not require discarding useful preliminary exploration.

| Layer | Evidence to inspect | What a pass establishes |
| --- | --- | --- |
| Corpus and output integrity | Inclusion/exclusion ledger, source IDs, joins, hashes, accounting, duplicate conflicts, completed receipts | The stated inputs and outputs are internally traceable |
| Representation coverage | Valid/zero/missing vectors, truncation, feature coverage by stratum, examples of excluded rows | Which units the representation can evaluate |
| Statistical structure | Repeatability, resampling/holdout stability, cluster sizes, distance diagnostics, appropriate nulls | Reproducibility or geometry under the specified perturbations |
| Semantic fidelity | Source-based review of labels, members, qualifiers, relations, and missed assertions | Support for the reviewed interpretation under its rubric and sample |
| Task usefulness | Retrieval relevance, faithful coverage, reviewer burden, a downstream comparison | Utility for the specific task measured |

Software checks cannot substitute for the last two layers. No single layer certifies legal, causal, or real-world effectiveness claims.

## Statistical checks with explicit populations

Report relevant metric definitions, direction, denominators, distance/space, sampled IDs, and excluded/noise treatment. A silhouette measured on an embedding space and one measured on a two-dimensional projection answer different questions. Record both if comparing them; do not substitute the more attractive one.

Trace an ambiguous metric to the code and saved configuration that produced it before naming its population. A field called `raw` may still include zero-feature or otherwise problematic rows; it is not automatically a score conditional on representable rows. Check the order of filtering, fitting, scoring, and overrides. If directional denominators or stable row IDs are unavailable, report the counts and missing information; do not invent coverage percentages or sum reused split counts as unique affected records.

Stability compares alignable objects: common observation IDs, co-memberships, or explicitly matched topics/components. Separate seed sensitivity from resampling stability and generalization to fresh source families. A stable partition may encode provider, role, language, length, or boilerplate instead of the intended subject; examine such confounds.

Prediction strength is one option for assessing whether cluster co-memberships transfer across splits. Preserve the method's definition, evaluation direction, treatment of singleton/missing clusters, and preprocessing split. Its theoretical and simulation scope does not establish legal-theme validity. See [Tibshirani and Walther (2005)](https://sites.stat.washington.edu/wxs/Stat592-w2011/Literature/tibshirani-walther-prediction-strength-2005.pdf).

Use a null or negative control only when its construction answers a clear question, such as whether observed separation exceeds an appropriate randomized structure. Explain what is preserved and destroyed; a favorable comparison to a weak null is not semantic validation.

## Source-based semantic review

Prepare a packet with stable unit IDs, source passages and necessary context, occurrence provenance, candidate label/claim, and reviewer fields. If testing independent judgments, hide model verdicts and prior adjudications while preserving source information needed to judge scope. Do not claim blinding that the reviewer did not actually have.

Sample central representatives, random ordinary members, boundary cases, and outliers separately. Keep probability samples distinct from purposive error discovery. Report the sampling frame and weighting; equal-cluster and population-weighted summaries answer different questions. Where dependence matters, uncertainty should respect source/report families rather than treating all passages as independent.

For each theme, assess:

1. **Support:** do the cited passages entail the name and description, including actors, conditions, modality, dates, and qualifiers?
2. **Membership:** do sampled members instantiate that theme, merely share vocabulary, or require multiple labels?
3. **Coverage:** which specific source assertions are faithfully represented, partly represented, or missing?
4. **Distinctiveness:** is the theme distinguishable from neighboring themes at the intended granularity?
5. **Usefulness:** does it support the intended retrieval, comparison, or interpretive work?

Record support and coverage separately. A theme can be well supported by three passages while missing most claims in its cluster. An exact quote can be real but irrelevant to the clause it supposedly supports.

Human judgments, assistant audits, and automated judgments need separate provenance. For consequential validation, specify reviewer independence, rubric, disagreement handling, and unresolved cases. Do not silently turn consensus reached after seeing predictions into an independent gold standard. A same-model critic can expose errors but shares possible failure modes.

Topic-model predictive fit and interpretability are distinct: [Chang et al. (2009)](https://papers.neurips.cc/paper/2009/hash/f92586a25bb3145facd64ab20fd554ff-Abstract.html) demonstrated human semantic evaluations that revealed properties missed by held-out likelihood. Adapt intrusion or source-matching tasks to the actual claim; a generic coherence score does not settle interpretation.

## Diagnose before expanding the search

| Observed failure | Inspect first | Candidate response |
| --- | --- | --- |
| All scores exactly zero | Raw values, exceptions, forced-zero rules, denominator, zero-feature rows | Separate representation coverage from conditional metrics; retain original scores |
| Stable but mixed clusters | Unit granularity, source roles, overlapping concepts, representative bias | Test a unit/representation hypothesis; allow multi-theme descriptions |
| High broad overlap, low faithful coverage | Missing mechanisms, negation, scope, ratings, and quantities | Refine coverage rubric and claim representation; do not call overlap completeness |
| Better scores after heavy exclusion | Which IDs disappeared and why | Report quality-versus-coverage tradeoff; compare a common evaluation population |
| Clean extraction but unchanged clustering | Matched assignments and semantic panel | Keep extraction repair as a provenance improvement; reject unsupported coherence gains |
| Reproducible LLM output with semantic errors | Fixed prompts, context, source clauses, shared judge bias | Retain repeatability evidence, revise interpretation task, obtain separate review |
| One attractive candidate after many trials | Search history and selection exposure | Report selection; evaluate a frozen candidate on fresh data if making generalization claims |

When publishing or presenting an analysis, use the result's actual status: candidate structure, reviewed sample, development result, fresh evaluation, or validated task performance. Failed validation can justify a useful change in workflow; it should not disappear from the experiment record.
