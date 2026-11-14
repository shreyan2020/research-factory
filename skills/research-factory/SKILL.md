---
name: research-factory
description: Coordinate a research workflow across document analysis, unsupervised methods, paper writing, and presentations. Use when asked for a research factory or an end-to-end, multi-stage research deliverable. For one bounded task, use the matching specialist directly; do not activate a full pipeline for a small edit.
---

# Research factory

Turn the user's research objective into checked, source-linked deliverables. Coordinate only the stages the task needs. Preserve the user's chosen method, audience, format, scope, and existing work.

This is a workflow layer. It uses available specialist skills and tools; it does not create a background service or authorize new experiments, publication, spending, or external messages by itself.

## Route the work

The specialist skills are sibling directories. Pass their absolute paths to delegated workers. Read only the skills and references needed for the current assignment.

| Request | Owner | Handoff |
|---|---|---|
| Extract, code, retrieve, or compare documentary evidence | [unstructured-data-factory](../unstructured-data-factory/SKILL.md) | Versioned units, source pointers, candidate claims, review status |
| Discover topics, compare representations, or test unsupervised methods | [unsupervised-factory](../unsupervised-factory/SKILL.md) | Protocol, baselines, raw and derived metrics, semantic review, decision |
| Choose a paper framing or connect planned questions, results, and claims | [research-narrative](../research-narrative/SKILL.md) | Commitments coverage, argument tree, rival interpretations, section/figure sequence |
| Plan, draft, revise, or shorten a research paper | [paper-factory](../paper-factory/SKILL.md) | Claim-evidence map, revised manuscript, citations and artifact checks |
| Create or revise a talk, workshop, or deck | [presentation-factory](../presentation-factory/SKILL.md) | Story, slides, notes, checked requested delivery format |

Typical chains are documents → evidence → manuscript, or existing paper → talk. Clustering is optional. Existing results do not need to be rerun merely to make slides. A method proposal is not permission to launch a research program.

For requests to learn from past work or audit these skills, read [history grounding](references/history-grounding.md). Separate explicit user decisions, artifact observations, external guidance, and design inferences before calling a workflow personalized.

## Start from what exists

State the intended outcome and the first concrete action briefly. Read current project instructions, latest user-edited artifacts, relevant source records, and active experiment status. Use history to identify lessons, then check the owning evidence for consequential claims. Do not treat an old server status, corpus count, or manuscript version as current.

Infer routine choices and proceed. Ask only about missing information that changes the scientific question, access, required format, audience, or consequential scope. While waiting, do work that does not depend on that answer. Never ask the user to settle a fact the available files or a small authorized check can establish.

For a multi-stage task, keep a compact work record using [the handoff contract](references/handoff-contract.md). Reuse existing project records; do not introduce a parallel documentation system. For a small edit, retain the necessary facts in the task context.

Match checks to the requested artifact and available evidence. Supplied excerpts, saved run diagnostics, slide text, and complete editable files need different completion checks. Reuse the upstream evidence record and route only the remaining work; missing inputs for an unrequested full build should not block a useful bounded deliverable.

## Run the production loop

1. **Frame.** Identify the question, requested artifact, audience, available evidence, exposure/access boundaries, and observable completion conditions.
2. **Plan the dependency chain.** Separate work that can run in parallel from work that requires a completed upstream result. Choose the simplest relevant baseline and a bounded pilot when a method or integration is uncertain.
3. **Produce a checked unit.** Create one representative extraction batch, experiment, manuscript section, slide sequence, or other meaningful slice. Verify the actual output before scaling.
4. **Evaluate the right claim.** Check source fidelity, semantic validity, empirical performance, rendering, or delivery as applicable. Passing one dimension does not imply passing the others. Use [quality and recovery](references/quality-and-recovery.md).
5. **Revise or stop the unsuccessful branch.** Diagnose the first failing assumption. Preserve failed attempts and null results. Change one consequential mechanism at a time when attribution matters. Do not lower a failed gate after seeing results and call the same experiment successful.
6. **Integrate.** Carry source IDs, run IDs, corpus boundaries, claim status, and denominators into the next stage. Reconcile inconsistent worker outputs rather than merging their prose blindly.
7. **Deliver.** Verify the exact requested artifact, destination, and version. Report the result, material verification limits, and any genuinely pending dependency. Update the project's research record where applicable.

Use available experiment-notebook for experimental comparisons, concise-artifacts for audience-facing editing, and the relevant presentation/document/PDF runtime skill for file mechanics. Use writing-style guidance when drafting on the user's behalf. If an optional companion is unavailable, apply the needed local guidance and state only material limitations; do not invent unavailable tools or dependencies.

## Delegate with purpose

Parallelize when it saves time or adds a distinct check: source families, independent literature roles, alternative candidate methods under a frozen protocol, or an independent audit. Give each worker the objective, exact inputs, permitted actions, output location, acceptance evidence, and boundary of ownership. Use [delegation patterns](references/delegation-and-learning.md).

Keep shared file ownership explicit. A reviewer should receive raw evidence and the candidate artifact without the author's intended verdict when independent evaluation matters. The coordinator remains responsible for inspecting output, correcting conflicts, and reporting accurately. Agreement among agents is not independent human validation.

## What completion means

- A proposed method is described as proposed; an executed run has a receipt and results.
- A reproducible pipeline is not automatically semantically sound.
- A source-backed finding states its actual corpus, time, unit, and status.
- A paper's claims match its evidence; a deck's numbers match the paper or saved results.
- A rendered preview and a local editable export are distinct deliverables.
- Unavailable access or missing independent review remains an explicit pending dependency. Finish unaffected work without filling the gap with invented evidence.

Read [design rationale](references/design-and-lessons.md) when adapting this factory. Preserve the small entry point and put new specialized detail in the owner skill rather than expanding every workflow.
