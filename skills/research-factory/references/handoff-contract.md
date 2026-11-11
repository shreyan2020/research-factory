# Handoff contract

Use a compact record for work spanning multiple stages or agents. Reuse the project's existing notebook, manifest, issue, or report. Do not make the user complete a form when the inputs are already available.

## Minimum useful record

```yaml
objective: null
requested_deliverables: []
audience_and_use: null
current_artifact_version: null
sources_and_versions: []
research_question: null
unit_and_population: null
scope_and_exclusions: []
permissions_and_compute_bounds: null
evaluation_exposure: null
acceptance_conditions: []
stages:
  - stage: null
    owner: null
    inputs: []
    output_paths: []
    status: planned
    evidence_of_completion: []
    unresolved_dependencies: []
```

Keep unknown fields null. Fill only fields relevant to the task. Link to a full experiment protocol rather than copying it into this record.

## Evidence packet carried downstream

Every substantive finding passed to a writer or presenter should include:

- A stable claim ID and exact bounded wording.
- Source IDs, locators, versions, and roles, with enough context to check the claim.
- The corpus, time period, unit, numerator/denominator, and exclusions when quantitative.
- Its status: source assertion, model suggestion, assistant interpretation, independently reviewed interpretation, measured result, or proposed hypothesis.
- Contradictory evidence and unresolved material uncertainty.
- Run/report provenance for computed values, including model or method revisions as needed.
- Which audience-facing wording the evidence permits.

A missing field should constrain the downstream claim rather than invite invention. When no original sources were inspected, say what was actually checked.

## Handoff-specific checks

| Transition | Check before proceeding |
|---|---|
| Raw sources → analysis | Extraction fidelity and source pointers; source roles and unit definitions |
| Analysis → unsupervised experiment | Versioned units, duplicate/family groups, features/context boundaries, exclusions |
| Experiment → paper | Baselines, exposure, raw metrics, semantics, coverage, uncertainty, actual execution status |
| Paper → presentation | Current manuscript version, exact numbers, contribution boundaries, audience need |
| Presentation → delivery | Requested format, notes, rendering, export status, interaction dependencies |

## Completion vocabulary

Use clear, distinct states such as planned, running, executed, reviewed, delivered, and blocked with reason. A single green check should not conflate them. A protocol file may be delivered while its experiment is unexecuted. A software check may pass while a semantic claim fails. An artifact can be ready while a user-controlled sign-in remains pending.
