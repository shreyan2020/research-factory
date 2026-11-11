# Semantic analysis and evaluation

Use for coding, event extraction, cross-source comparisons, evidence retrieval, and evaluation of model-derived claims.

## Make the inferential chain inspectable

Write the chain in ordinary language before implementation. Example: source documents → complete claim units → legal-theme retrieval → candidate cross-source relations → source review → bounded findings. Record the input, output, and source of supervision at each stage.

For an LLM parent classifier followed by within-parent clustering, the parent classifier uses the codebook; the clustering receives its selected pool. Positive examples and exclusions can therefore change membership without directly constraining the clustering algorithm. Call the method what it actually does. Settle a consequential mismatch with the user's intended methodology before expanding it.

For deductive qualitative coding, anchor each code to a definition and inclusion/exclusion boundary. Allow multiple codes when warranted and retain ambiguous/context-insufficient states. For inductive qualitative interpretation, preserve analytic memos and contrasting cases; do not relabel automated clusters as human-developed themes. For mixed methods, show where automated candidate discovery ends and interpretive coding begins.

## Source-role matrix

Before asserting a relationship, check:

| Question | Example of an invalid shortcut |
|---|---|
| Who is making the claim? | Treating a provider description as an auditor's finding |
| What was actually tested? | Treating an audit criterion as a demonstrated outcome |
| What time/cycle does it concern? | Treating a later response as evidence of earlier implementation |
| What authority/status applies? | Presenting preliminary regulatory findings as a final ruling |
| What relationship is supported? | Treating co-occurrence or similar wording as a causal link |
| What does a missing item mean? | Treating retrieval failure as proof of absence |

In documentary comparisons, retrieve by the substantive research theme before applying secondary tags. Use those tags as secondary dimensions unless the study explicitly defines them as the primary frame. Recheck the active corpus and question: a completed bounded analysis and a prospective broader corpus are not interchangeable.

## Complete events and semantic binding

Keep actor/entity, intervention, comparator, outcome/property, value or direction, time, conditions, attribution, and source scope together when the task needs them. Some fields legitimately remain unknown. A support span must justify their relationship, not just contain their words.

Typical checks:

- Does the answer concern the requested endpoint rather than a nearby total score or subgroup?
- Is the effect direction oriented to the question's intervention and comparator?
- Is a within-group change being mistaken for a between-group effect?
- Are aliases or group A/B definitions available in the evidence shown to every method?
- Do all arguments belong to the same event, including table or cross-sentence references?
- Is an omitted retained tuple an annotation fact or a separately established scientific negative?

Do not force a decisive answer when context is insufficient. If aggregation converts abstentions into answers, evaluate those transitions explicitly.

## Evaluation contract

Before a comparison, define the unit of sampling and splitting, exposure ledger, corpus version, baseline, frozen scoring rule, review sample, and stopping condition. Split at document/family level when related passages would leak across sets. Unknown historical exposure is not fresh evaluation.

If comparing categorical relation labels, freeze a common codebook first. When only label names were supplied and analysts independently operationalized them, assess the supported claim and explain definition differences; label-string disagreement alone is not an error rate.

Report the relevant dimensions separately:

1. Structural validity: parsing, schema, references resolve.
2. Extraction fidelity: original source content and scope survived.
3. Quotation validity: quoted text exists at the cited location.
4. Semantic support: that evidence supports this specific interpretation.
5. Reference-label agreement: performance against a named, versioned reference.
6. Coverage and retrieval: what eligible cases were found, missed, or abstained on.
7. Downstream usefulness: whether the research or audience task improved.

Select metrics to match the claim. Precision over accepted cases alone hides abstention and retrieval misses. Recall needs an independently defined eligible set or a clearly bounded estimate; do not invent it from retrieved candidates. Keep denominators and sampling weights visible. Use uncertainty estimates appropriate to correlated source units; do not imply independent observations for many excerpts from one paper.

Inspect wins and losses, not only average scores. Hold source evidence, retrieval budgets, annotation policy, and realized compute comparable where attribution requires it. A benefit caused by repaired quote formatting does not establish better reasoning. Equal maximum output lengths are not equal realized compute.

## Independent review

Use a predeclared review sample that includes typical, boundary, contradictory, rejected, and potentially missed cases. Blind reviewers to method labels where feasible. Supply enough original context to judge the claim. Record reviewer identities/roles, source quotations, decisions, and disagreements without exposing private identities in public artifacts.

If human validation is required but unavailable, prepare the review instrument and report review pending. An agent review can identify errors and improve a draft; it cannot be relabeled human validation or independent expert adjudication. If references appear wrong, preserve frozen results and create a separate adjudication/version record.

## Recovery

Malformed output: retain the failed attempt; simplify the schema or output mechanism; create a versioned retry and account for reused responses and compute.

Unsupported labels: repair source roles, scope, and evidence selection before adding another unconstrained reviewer. Use deterministic span selection when exact quotation is the problem.

Repeated baseline losses: keep improvements to infrastructure, reject the unsupported method claim, identify the premise causing failure, and define one discriminating next test. A proposal remains a proposal until run.
