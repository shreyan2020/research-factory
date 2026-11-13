# Claims and literature

## Build an evidence map only where it earns its cost

For a short edit, source links in working notes may suffice. For a paper with interacting datasets, automated outputs, or contested interpretations, use the existing evidence ledger or start from [the claim ledger](../assets/claim-ledger.csv). Record one checkable claim per row; split bundled claims if different evidence supports them.

| Field | What it prevents |
|---|---|
| Claim ID and manuscript location | A correction that fixes one section but leaves the abstract inconsistent |
| Proposed wording and claim kind | An inference or proposal presented as an observation |
| Source/version and exact locator | A nearby citation that does not support the sentence |
| Supporting passage/result | A remembered summary replacing the actual evidence |
| Unit, population, period, denominator | A local observation becoming a general prevalence claim |
| Evidence/review status | A machine output becoming a source-reviewed finding |
| Counterevidence and unresolved scope | A selected favorable passage becoming the whole story |
| Decision and final wording | The same rejected interpretation reappearing |

Use evidence states appropriate to the project, for example `source-checked`, `computed-unreviewed`, `assistant-reviewed`, `independently-reviewed`, `disputed`, `proposed`, or `unsupported`. These are descriptions of process, not a numeric truth scale. A checked source can still be incomplete or wrong.

## Read beyond a retrieved fragment

Inspect neighboring paragraphs, headings, footnotes, table structure, definitions, exceptions, and reporting period when they can change interpretation. Preserve PDF page and printed page separately when they differ. If the source is inaccessible, retain the limited-access state and narrow the claim; do not infer that missing access proves missing evidence.

In documentary governance work, distinguish:

1. A provider's commitment or self-report.
2. An auditor's test, opinion, recommendation, and stated scope.
3. A follow-up record of implementation.
4. Evidence that the implemented change was checked.
5. Evidence of effects on affected people.

These states are not interchangeable. A verified correction to a disclosure does not establish broader effectiveness or compliance. An adverse opinion can coexist with successful sampled tests; source-specific categories may not form a simple good/bad scale. Explain the relevant issue, population, period, mechanism, and verification evidence.

For empirical AI/HCI work, similarly separate model performance against a reference, reference validity, simulated behavior, participant observations, and causal effects. Report the conclusion that the design identifies.

## Compare closest literature concretely

Use a compact comparison during a major background revision:

| Prior work | Actual question/task | Material and unit | Output and evaluation | Overlap | Defensible difference |
|---|---|---|---|---|---|

Search by the substantive problem and closest method, including sources the user names. A citation belongs because it establishes a premise, supplies a method, offers a competing explanation, or defines the closest comparison. Do not add every retrieved paper or divide the background into a catalog of tools.

Check bibliographic identity, publication status, version, and the claims in the source itself. Use primary papers and official sources for technical or legal assertions. Save the source locator needed for review. Never invent authors, titles, DOIs, quotations, page numbers, or experimental details.

Avoid “the first,” “no prior work,” and “state of the art” unless the search and comparison support that exact scope. Prefer a specific contribution such as a new source combination, unit of comparison, task definition, or empirical finding. If the closest paper already does the claimed task, revise the contribution instead of writing around it.

## Make paragraphs do work

For each paragraph, identify its claim, supporting evidence, and connection to the next step of the argument. Use author-led citations when discussing what researchers did, following the draft's citation convention; in a compatible LaTeX/natbib manuscript this may be `\citet{key}`. Use parenthetical citations for support when the author is not the sentence's subject. Do not change citation packages merely to impose this preference.

Check the background subsection by subsection: what does this literature establish, what uncertainty remains, and how does the present design address it? Avoid a final sentence that mechanically declares a gap without evidence.

## Preserve the author's argument and citation mechanics

When the user selects a narrative or supplies a final introduction, use that as the argument to develop. Do not substitute a new framing because it fits a familiar paper template. Explain how each paragraph advances the selected question and connects to the next; a sequence of individually relevant paragraphs is insufficient.

For a literature comparison, name the relevant prior study's actual task, evidence, or method and the specific difference the current design supports. Replace “we build on these concerns” with that concrete relationship. Do not invent what prior work failed to do; distinguish unreported, inaccessible, and established absence. Track user-nominated papers through inclusion, deferral, or an explained exclusion rather than silently dropping them.

Preserve existing bibliography keys when merging references. In a manuscript using textual citations, use its citation command (for example `\citet{key}`) rather than manually writing “X and colleagues” and duplicating the author name. Check the resulting sentence as well as compilation. Keep the user's final wording, retained figures, and reserved edits unless the requested revision affects them.
