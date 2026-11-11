# Delegation and learning

## Assignments that add value

| Pattern | Good use | Avoid |
|---|---|---|
| Partitioned production | Independent source families or sections with explicit ownership | Several agents rewriting the same manuscript |
| Independent checking | A reviewer checks raw evidence against a candidate claim | Giving the reviewer the desired verdict |
| Bounded alternatives | Two plausible methods or layouts tested under shared conditions | Many variations without a decision criterion |
| Failure diagnosis | One worker traces source extraction; another checks scoring | Agents all repeating the same speculative explanation |

Provide each worker this brief in a form suited to the tools available:

```text
User objective:
Your exact subtask:
Skill path and relevant reference:
Authoritative input paths/versions:
Permitted actions and protected resources:
Owned output path:
Observable acceptance evidence:
Return artifacts, checks performed, unresolved issues, and source pointers.
```

Do not use model names or agent types copied from another product. Use available capabilities and current user/project constraints. If delegation is unavailable, execute the same distinct roles sequentially without claiming independent review.

## Integrate, do not concatenate

Inspect worker artifacts. Resolve contradictory counts, source roles, terms, units, and manuscript versions. Choose a supported interpretation when evidence permits it; retain disagreements when it does not. Keep one owner for the final scientific claim and one owner per shared output file.

## Turn outcomes into lessons

Record in the current project journal when useful:

```text
Observed event and artifact:
What worked:
What failed:
Cause supported by evidence (or unresolved hypothesis):
Condition under which the lesson applies:
Smallest process or tool change:
Check that would show the change helped:
```

Keep observations separate from interpretations and proposed fixes. Prefer a narrow source-locator repair, schema constraint, cache rule, or focused checklist over adding a universal prohibition.

When the user asks to improve these skills, review the relevant event, update the owning skill, validate its references and metadata, and run a realistic case if behavior changed substantially. Preserve user edits and explain the change briefly. Do not silently modify global memory or installed skills during unrelated work. Recording a project lesson is not the same as changing the user's persistent instructions.

## Forward-test meaningful behavior

Give an evaluator a realistic request, the skill, and minimum raw artifacts. Do not supply the expected answer. Use an isolated directory and bounded, authorized actions. Inspect the resulting artifact, not only the evaluator's self-report. Check decisions such as refusing to equate a quote with support, preserving requested format, or retaining a failed baseline comparison. Do not write a test suite that only asserts skill headings or phrases.
