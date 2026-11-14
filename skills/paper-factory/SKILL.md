---
name: paper-factory
description: Develop, revise, shorten, or audit research papers through source-grounded arguments, reproducible methods, and verified manuscript delivery. Use for substantive manuscript and reviewer-response work; skip routine copyedits and general factual questions.
---

# Paper factory

Produce the requested manuscript change with a traceable argument: the problem matters, the evidence supports the claim, the method and its execution status are described accurately, and the delivered version works in its intended format. Preserve the user's study, latest edits, and publication decisions.

## Choose the scale

- **Focused revision:** Read the affected section, its source evidence, and the surrounding argument. Edit it directly and check downstream claims, references, and layout where affected.
- **Excerpt-only delivery:** If only revised text is requested, check that text, its local citations and dependencies. Do not reconstruct a whole manuscript, fetch venue rules without a submission requirement, or require a render to finish the excerpt. Distinguish preservation of supplied assertions from independent verification of the underlying study.
- **New paper or conceptual argument:** Establish the substantive question, available evidence or premises, closest literature, and contribution before drafting. Match the argument and evaluation to the paper type; do not invent an empirical study for a conceptual paper or imply a proposed experiment has run.
- **Substantive paper work:** Use the workflow below. Keep a compact evidence and revision record when several claims or sections interact.
- **Critical review:** Return prioritized, actionable findings with manuscript locations and supporting evidence. Do not rewrite the paper unless requested.
- **Reviewer response:** Tie each response to a completed change, a justified disagreement, or an explicitly pending action. Do not report planned experiments as completed.

Use the existing repository/document workflow and current format skill for LaTeX, Word, Google Docs, or PDF. Use `concise-artifacts` and the available writing-style skill when applicable; if unavailable, follow the user's draft and explicit preferences without claiming a retrieved style match. This skill adds research judgment, not a replacement rendering engine.

## 1. Establish the manuscript contract

Find the authoritative draft, bibliography, latest user/coauthor edits, source corpus, analysis outputs, and any submission constraints. Inspect project instructions before changing files. Record only decisions that affect the work:

- Requested change and audience; target venue/year/version when relevant.
- Research question, contribution, unit of analysis, sampling boundary, and evidence period.
- Which study and results are completed, which are proposals, and which have unresolved review.
- Material constraints: retained figures, terminology, citation style, anonymization, length, and user-edited passages.

Use available context to resolve these. Ask only for an ambiguity that changes the deliverable and cannot be settled by inspecting sources. Recheck the actual current venue rules when they govern submission; do not carry forward old deadlines, page counts, or appendix assumptions.

## 2. Build the argument from evidence

When the task is to choose a framing, reconcile a protocol with findings, or build a narrative tree, use the sibling [research-narrative](../research-narrative/SKILL.md) if available. Carry its claim IDs, alternative interpretations, and planned-item coverage into the manuscript. Routine copyedits do not need that workflow.

Read [claims and literature](references/claims-and-literature.md) when establishing claims, positioning novelty, or revising introduction/background/findings.

Write a short argument spine before expanding a major rewrite: substantive problem → what existing work establishes → unresolved question → what this study can observe → contribution supported by the results. Each section should advance this argument rather than repeat a generic motivation.

For consequential claims, connect the proposed wording to the exact source passage or result, scope, and evidence status. Separate observations, interpretations, normative arguments, and proposals. Find counterevidence and qualify the inference where it changes the conclusion. A cluster label, automated count, extraction success, or reproducible run is not by itself a validated substantive finding.

Position related work by task, source material, unit, output, and evaluation. Read the closest work before claiming a gap. Preserve partial-access and version limits: an abstract supports abstract-level statements; a newer preprint may not support a claim about the cited older version.

## 3. Write the final study, not its development diary

Read [methods and results](references/methods-and-results.md) when changing methods, results, limitations, or reproducibility claims.

Explain the final design in the order needed to reproduce and assess it. Keep experimental history in the research record or appendix when it explains a consequential choice. Describe actual inclusion criteria, source asymmetries, transformations, annotation/review roles, exposure, comparison conditions, and analysis decisions. Mark missing information instead of inventing a plausible method.

Keep a frozen distinction between the manuscript's analyzed corpus and proposed expansions. Do not silently transfer findings across services, periods, tasks, or evaluation sets. Distinguish computational assistance, assistant review, independent human review, and adjudication.

## 4. Revise coherently

Use [revision and delivery](references/revision-and-delivery.md) for shortening, reviewer responses, bibliography changes, and final checks.

For a substantial change, identify affected abstract, research questions, methods, results, tables, captions, discussion, and supplement claims. Update only the dependent material. Preserve the user's removed text and retained figures as editorial decisions; do not restore equivalent filler or remove material again without a new reason grounded in the current request.

Use connected prose, concrete subjects and verbs, and terminology the evidence can sustain. Explain necessary terms. Remove repeated scope defenses, section previews, generic novelty language, and development chronology that obscures the final design. Keep limitations where they affect interpretation; do not bury evidence needed to judge a claim in the appendix solely to meet length.

After shortening, compare each materially changed sentence with its source for actor, population, subject matter, conditions, modality, time, and evidence status. Numbers and citations can all survive while a removed phrase broadens the claim. Restore any necessary qualifier before accepting the word reduction; check the revised sentence again in context.

## 5. Review and deliver the actual artifact

For a long or consequential rewrite, delegate independent, bounded reviews when available: one for claim/source support and one for argument or reader comprehension. Give reviewers the relevant draft and raw evidence, not the conclusion they are expected to endorse. The integrating agent resolves conflicts against sources and user decisions. Do not treat agreement among agents as independent human validation.

Verify the changed artifact using its real workflow: compile or render, inspect affected pages and final pagination, check citations and cross-references, and inspect figures/tables at readable size. A successful compile is one check, not proof of scientific validity or visual quality. If a necessary check is unavailable, report the specific unchecked property.

Deliver the requested file, section, review, or response. Summarize what changed, the material checks completed, and any unresolved decision. Do not claim acceptance readiness, publication, human validation, or venue compliance beyond the evidence. Writing and editing do not authorize submission or contacting coauthors.

## Recovery and learning

When a correction exposes a stale generator, source table, bibliography key, or reused paragraph, repair the owning source within scope so the error will not regenerate. Preserve original evidence and results. If the same framing repeatedly fails, revisit the research question, source capability, or contribution claim before another prose pass.

Consult [observed lessons](references/observed-lessons.md) when a similar failure recurs or when reviewing the factory's assumptions. Those records are historical evidence, not current project status. Capture a new lesson in the existing project record with the observed failure, supported correction, and a condition that would make the lesson inapplicable; do not silently rewrite global skills or memory.
