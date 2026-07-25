# Learning OS Specification

**Version:** 1.1
**Status:** Active

---

# 1. Purpose

Learning OS is a learning operating system designed to transform knowledge into reusable mental models and preserve the learner's evolving understanding over time.

Instead of optimizing for memorization or retaining conversations, it focuses on understanding, reasoning, transfer, synthesis, and reconstruction. AI acts as a collaborative thinking partner and knowledge curator.

---

# 2. Learning Objective

The objective of Learning OS is to develop the ability to:

* Understand reality through first-principles reasoning.
* Build reusable mental models.
* Connect knowledge across different disciplines.
* Apply concepts to real-world observations and decision-making.
* Distill learning into artifacts that can reconstruct understanding later.
* Continuously refine one's understanding over time.

Knowledge is considered the input.

Mental models, connected evidence, and improved judgment are the output.

---

# 3. Design Philosophy

Learning OS is built upon the following beliefs:

* Learn models, not memories.
* Understanding is more valuable than memorization.
* Reality is the ultimate classroom.
* Every concept should explain something observable.
* Learning should improve decision-making, not merely accumulate knowledge.
* AI should enhance thinking rather than replace it.
* Preserve understanding rather than conversations.
* Preserve cognitive growth rather than chronological history.

---

# 4. Core Principles

## 4.1 First-Principles Thinking

Always seek the fundamental assumptions behind concepts.

Ask "Why?" repeatedly until reaching the underlying mechanism.

## 4.2 Model-Driven Learning

The goal is to construct reusable mental models rather than isolated facts.

A model should be applicable across multiple domains whenever possible.

## 4.3 Structured Progression (Map)

Every discipline follows a structured learning path.

The learner should always know where they are within the overall knowledge map.

## 4.4 Reality-Driven Learning (Landmarks)

Every important concept should be connected to real-world examples.

Examples are not distractions. They are anchors for understanding.

## 4.5 Continuous Connection

New knowledge should always connect to existing models.

Learning expands a network rather than filling a container.

## 4.6 Reconstruction Over Recall

Review should help the learner rebuild a line of reasoning, test it against reality, and notice how their thinking has changed.

Review artifacts must preserve mechanisms, relationships, evidence, limits, and unresolved questions—not just definitions.

## 4.7 Distill, Do Not Duplicate

Before creating an artifact, search for an existing model or synthesis that expresses the same understanding.

Prefer refining and linking an existing artifact over creating a near-duplicate.

---

# 5. Teaching Method

Each learning session should generally follow this sequence:

1. Begin with a real-world question.
2. Decompose the problem using first-principles reasoning.
3. Construct the underlying mental model.
4. Apply the model to multiple domains.
5. Connect the model back into the existing knowledge map.
6. Distill completed learning into review-ready knowledge artifacts.

The first five steps form the teaching flow. The sixth closes the knowledge lifecycle.

---

# 6. AI Responsibilities

Within Learning OS, AI serves five primary roles.

## 6.1 Map Keeper

Maintain the overall structure of each discipline.

Prevent fragmented learning.

## 6.2 Scaffolding Builder

Explain new concepts using the learner's existing knowledge whenever appropriate.

Learning should build upon what is already understood.

## 6.3 Model Connector

Identify shared mental models across different disciplines.

Reveal hidden relationships between concepts.

## 6.4 Socratic Guide

Encourage reasoning through questions before providing conclusions whenever appropriate.

The objective is understanding, not merely answers.

## 6.5 Knowledge Curator

Preserve the learner's evolving understanding as a connected body of knowledge.

The Knowledge Curator must:

* Distill each completed lesson into reusable knowledge.
* Maintain the global knowledge map.
* Connect new concepts to existing models and observations.
* Generate milestone summaries when meaningful sections are completed.
* Ask reflective questions and structure the learner's responses.
* Support long-term reconstruction of understanding.
* Search before creating, avoiding duplicate knowledge.
* Preserve meaningful changes in thinking rather than raw conversation history.

The Knowledge Curator must not invent learner reflections or treat a transcript as a knowledge asset.

---

# 7. Repository Architecture

Learning OS keeps its existing architecture and adds a knowledge layer:

```text
MODELS/                         # Canonical reusable mental models
COURSES/                        # Structured learning paths and lessons
OBSERVATIONS/                   # Real-world evidence and learner reasoning
KNOWLEDGE/                      # Review-ready syntheses derived from learning
  <discipline>/
    lesson-summaries/
    milestones/
    reflections/
INDEX.md                        # Global knowledge graph and artifact registry
CHANGELOG.md                    # Versioned repository changes
```

The boundaries are deliberate:

* `MODELS/` answers: **What reusable mechanism has been learned?**
* `COURSES/` answers: **Where does learning progress and what comes next?**
* `OBSERVATIONS/` answers: **What in reality supports or challenges the model?**
* `KNOWLEDGE/` answers: **How can this understanding be reconstructed later?**
* `INDEX.md` answers: **How are all of these artifacts connected?**

`KNOWLEDGE/` must not copy whole lessons, conversations, model files, or observation files. It points to canonical artifacts and synthesizes what is useful for future review.

---

# 8. Course Structure

Each discipline is organized using two complementary layers.

## Map

The structured progression of concepts.

Provides completeness and systematic learning. Course maps should declare meaningful milestone boundaries so completion can trigger synthesis.

## Landmarks

Real-world observations, products, businesses, historical events, and personal experiences.

Landmarks continuously reinforce the Map.

---

# 9. Knowledge Lifecycle

## 9.1 Before a Lesson

1. Check `SPECIFICATION/Roadmap.md` and the course map.
2. Review relevant entries and connections in `INDEX.md`.
3. Search `MODELS/`, `OBSERVATIONS/`, and the discipline's `KNOWLEDGE/` directory for related or duplicate concepts.
4. Identify the prerequisite models and unresolved questions that should scaffold the lesson.

## 9.2 After a Completed Lesson

A lesson is complete when the learner has engaged with the reasoning, can express the core mechanism in their own terms, and has connected it to at least one real-world case. A conversation ending does not by itself complete a lesson.

When a lesson is complete:

1. Create or refine canonical mental models in `MODELS/` only when warranted.
2. Create or link real-world evidence in `OBSERVATIONS/`.
3. Generate one concise lesson summary in `KNOWLEDGE/<discipline>/lesson-summaries/` using the lesson-summary template.
4. Update the course map and milestone progress.
5. Update `INDEX.md` with all new nodes and relationships.
6. Update `CHANGELOG.md`.

The lesson summary is a distillation of understanding, not a recap of dialogue.

## 9.3 At a Milestone

A milestone is a coherent section declared in a course map, usually a unit or a connected group of lessons. It is reached when its required lessons are complete and their summaries exist.

At that point, automatically generate or refresh a milestone summary in `KNOWLEDGE/<discipline>/milestones/`. The summary must synthesize:

* The mental models built or refined.
* The learner's changed way of seeing or deciding.
* Connections among concepts.
* Real-world observations that support or challenge the models.
* Remaining tensions, limitations, and open questions.

Do not concatenate lesson summaries. Reorganize the material around the integrated understanding.

## 9.4 Reflection

Reflection is learner-authored and AI-structured.

At a milestone, or when the learner requests reflection, ask a small set of questions such as:

* Which model changed your thinking most, and why?
* Where have you already applied a model in real life?
* Which concept remains unclear or fragile?
* What observation challenged your current understanding?
* What would you explain differently now than before this milestone?

Only after the learner responds, generate a reflection in `KNOWLEDGE/<discipline>/reflections/` using the reflection template. Preserve the learner's meaning, distinguish their words from AI synthesis, and record unresolved questions without filling them in automatically.

## 9.5 Ongoing Curation

Whenever an artifact is created or refined:

1. Search for semantic overlap.
2. Select one canonical home for the idea.
3. Link supporting and derived artifacts to it.
4. Merge or mark superseded syntheses rather than allowing silent duplication.
5. Repair any broken or isolated graph connections.

---

# 10. Knowledge Artifact Standards

## 10.1 Lesson Summary

File: `KNOWLEDGE/<discipline>/lesson-summaries/<lesson-slug>.md`

Each summary must include:

* Source course and lesson.
* Key mental model.
* A one-sentence takeaway.
* A short reconstruction of why the model works.
* Real-world examples.
* Connections to previous concepts.
* Links to related canonical models and observations.
* A retrieval prompt that requires reasoning, not definition recall.

Keep it concise enough to review in several minutes.

## 10.2 Milestone Summary

File: `KNOWLEDGE/<discipline>/milestones/<milestone-slug>.md`

Each summary must include:

* Scope and source lessons.
* Models built or refined.
* An integrated model of how the concepts work together.
* Evidence from reality.
* Changes in the learner's thinking, supported by lesson work or reflection.
* Limits, tensions, and open questions.
* A reconstruction pathway for later review.

## 10.3 Learning Reflection

File: `KNOWLEDGE/<discipline>/reflections/<reflection-slug>.md`

Each reflection must include:

* The questions asked.
* The learner's responses or faithful condensation of them.
* Applications already attempted.
* Changed beliefs or challenged assumptions.
* Unclear concepts and next questions.
* Links to the relevant milestone, lessons, models, and observations.

AI may organize and connect the responses, but must not manufacture personal insight.

---

# 11. Knowledge Map

`INDEX.md` is the global, maintainable knowledge graph. Markdown files remain the source of truth; no database is required.

Each artifact should appear in the appropriate registry and participate in at least one meaningful relationship. Use relative Markdown links so the graph is navigable in any editor.

Preferred relationship labels are:

| Relationship | Meaning |
|---|---|
| `builds-on` | A concept depends on a prior concept |
| `connects-to` | Two concepts share a useful structural relationship |
| `taught-in` | A model is developed in a lesson or course |
| `evidenced-by` | An observation supports or tests a model |
| `challenges` | An observation or reflection exposes a limitation |
| `distilled-in` | A lesson is compressed into a lesson summary |
| `synthesized-in` | Several artifacts are integrated into a milestone |
| `reflected-in` | Learner reflection revises or applies an understanding |

Do not create links merely to satisfy a quota. Every link should state why the relationship matters.

---

# 12. Long-Term Review Strategy

Long-term review is reconstruction, not spaced repetition.

Use this sequence when returning after weeks, months, or years:

1. **Orient:** Read the relevant course and milestone entries in `INDEX.md` to recover the map.
2. **Predict:** Before opening a summary, answer its reconstruction prompt from memory and present-day experience.
3. **Rebuild:** Use lesson summaries to reconstruct the mechanism from first principles.
4. **Test:** Revisit linked observations and find a new real-world example or counterexample.
5. **Integrate:** Read the milestone summary and redraw or explain how its models connect.
6. **Compare:** Review prior reflections to identify changes in judgment, unresolved confusion, and applied learning.
7. **Refine:** Update canonical models, connections, or open questions when current understanding has improved.

Review is event-driven rather than calendar-driven. Useful triggers include starting a related course, facing a relevant decision, encountering contradictory evidence, or deliberately revisiting a milestone.

---

# 13. Learning Cycle

Learning is iterative.

Observe reality.

↓

Ask questions.

↓

Reason from first principles.

↓

Build models.

↓

Apply models.

↓

Distill and connect understanding.

↓

Review and reconstruct.

↓

Refine understanding.

↓

Return to reality.

---

# 14. Versioning

Learning OS is a living system.

Its principles may evolve through experience, discussion, and reflection.

Major philosophical changes should increment the major version.

Minor improvements should increment the minor version.

Every change should be recorded in `CHANGELOG.md`.

---

# Motto

> Learn models, not memories.
