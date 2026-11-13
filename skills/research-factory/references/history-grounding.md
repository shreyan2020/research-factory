# Learning from the actual work

Use this reference when creating or revising workflows from the user's history, or auditing claims of personalization.

## Establish the source of each rule

- **Explicit user decision:** read the original request or correction, its target artifact, and later revisions. Preserve its scope and any superseding decision.
- **Observed artifact behavior:** inspect the relevant input, output, or execution evidence. An assistant saying it succeeded is not enough.
- **External guidance:** read the supplied source and adapt it to the task. Attribute it as guidance, not as the user's preference or a validated effect.
- **Design inference:** label it as a proposed generalization with a reason and limits. Do not present it as something the user previously asked for.

Use memory summaries to find the relevant conversation and files, then read the consequential turns. Reconstruct the sequence of correction, attempted remedy, further correction, and latest decision. A summary of the final export can miss the decisions that made the result useful.

## Audit before adding more instructions

Compare the existing skill with the original evidence. Mark a requirement as already covered, present but too vague or difficult to discover, missing, contradicted, or unsupported. Retain useful existing instructions. Prefer replacing an abstract rule with a concrete decision procedure over accumulating repeated warnings.

Record source-to-rule mappings locally, with exact turns or artifact locations. Keep private conversations and unpublished findings out of public skills. Publish only the transferable procedure and permitted source attribution. Do not reintroduce public testing narratives the user removed.

## Separate packaging from usefulness

Valid metadata, working links, successful compilation, and reproducible execution establish specific technical properties. They do not establish that a skill reflects the user's workflow or that an artifact is coherent, visually useful, semantically correct, or accepted. Review the actual requested outcome against the recovered decisions. If only an audit or instruction edit was performed, say so; do not claim the corrected workflow has been demonstrated in a new real task.
