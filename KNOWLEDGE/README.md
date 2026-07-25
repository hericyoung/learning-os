# Knowledge Layer

`KNOWLEDGE/` contains review-ready syntheses generated from completed learning. It preserves the learner's understanding without storing transcripts or duplicating canonical lessons, models, and observations.

## Structure

Create a discipline directory only when its first knowledge artifact is produced:

```text
KNOWLEDGE/
└── <discipline>/
    ├── lesson-summaries/
    ├── milestones/
    └── reflections/
```

Use lowercase kebab-case for discipline directories and filenames.

* `lesson-summaries/` distills one completed lesson into its model, reasoning, evidence, and connections.
* `milestones/` integrates a declared unit or coherent lesson group.
* `reflections/` structures the learner's answers to reflective questions; AI never writes personal reflection without those answers.

The templates live in `.agents/skills/learning-os/resources/templates/`.

## Artifact Rules

1. Link to canonical files in `COURSES/`, `MODELS/`, and `OBSERVATIONS/`; do not copy them.
2. Search existing artifacts before creating a new one. Refine an existing synthesis when the understanding is substantially the same.
3. Optimize for reconstruction: preserve mechanisms, connections, evidence, limits, and useful questions.
4. Avoid chronology unless a date is needed to compare changes in understanding.
5. Add every new artifact and meaningful relationship to `INDEX.md`.
6. Record every creation or material update in `CHANGELOG.md`.

## Long-Term Review

Review should follow this path:

1. Orient with `INDEX.md` and the relevant milestone.
2. Attempt the reconstruction prompts before rereading explanations.
3. Rebuild the models from first principles using lesson summaries.
4. Test them against linked observations and a new real-world case.
5. Compare reflection history to find changed judgment and unresolved confusion.
6. Refine the canonical model or graph when present understanding has improved.

The purpose is to recover a way of thinking, not to remember the wording of an earlier lesson.
