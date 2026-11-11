# Research Factory

Five modular agent skills for turning source material into checked research outputs. Use one specialist for a bounded task, or the coordinator for work that crosses analysis, methods, writing, and presentations.

| Skill | What it does |
|---|---|
| [research-factory](skills/research-factory/SKILL.md) | Routes work and preserves evidence through handoffs |
| [presentation-factory](skills/presentation-factory/SKILL.md) | Builds research talks and workshops, with notes and delivery checks |
| [paper-factory](skills/paper-factory/SKILL.md) | Develops arguments, revises manuscripts, and shortens prose without changing claims |
| [unstructured-data-factory](skills/unstructured-data-factory/SKILL.md) | Extracts, codes, and compares evidence with source context |
| [unsupervised-factory](skills/unsupervised-factory/SKILL.md) | Designs and evaluates clustering, representations, and topic discovery |

The package contains instructions and templates, not a standalone application. It uses the tools available in your agent environment. Presentation rendering, document conversion, model inference, and data access need their own supported tools.

## Install

Clone or download this repository. Copy the five directories inside `skills/` into your Codex skills directory (normally `~/.codex/skills/`). Keep them as sibling folders so the coordinator's links resolve. Review existing folders before replacing an installed version. Start a new chat and invoke the relevant skill by name.

For other agents that support `SKILL.md`, install the directories using that agent's documented skill mechanism. The `agents/openai.yaml` files are optional Codex UI metadata; availability of companion tools varies.

## Use

```text
Use $presentation-factory to turn this paper into a 20-minute talk.
Keep the evidence readable and put detailed explanations in speaker notes.
```

```text
Use $paper-factory to shorten this methodology by about 25%.
Preserve the population, conditions, qualifiers, citations, and reported results.
```

```text
Use $unstructured-data-factory to compare these report excerpts.
Preserve their IDs and distinguish observations, interpretations, and missing evidence.
```

```text
Use $unsupervised-factory to diagnose these clustering results.
Trace each metric to its scored population before proposing a new run.
```

```text
Use $research-factory to analyze these documents and develop a findings section
and presentation from the supported claims.
```

## What is different

- Meaning is checked separately from valid files, quotations, citation counts, and successful runs.
- Evidence status, units, and denominators travel with results into manuscripts and slides.
- Small excerpt tasks stay small; they do not trigger a full corpus rebuild or manuscript compilation.
- Failed methods and simple baselines remain visible. More complex workflows must justify their added work.
- A deck is checked in the requested saved format; a preview is not an editable export or a live delivery test.

Each skill has a short entry point and detailed references loaded only when relevant. Templates cover evidence records, experiment plans, claim ledgers, and revision responses.

## Origins and adaptation

Created by Shreyan Biswas with Codex assistance. The coordinating structure was inspired by [Poteto mode](https://github.com/cursor/plugins/blob/main/pstack/skills/poteto-mode/SKILL.md); these are original research workflows, not a copy of that plugin.

Adapt the skills to your question, corpus, audience, and tools. A workflow skill does not itself authorize publication, spending, new experiments, or contacting other people.
