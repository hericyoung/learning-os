# Learning OS

> A versioned operating system for lifelong learning, built on first-principles thinking, mental models, knowledge curation, and AI collaboration.

[English](README.md) | [中文](README-zh.md)

Learning OS is not a collection of notes or courses.

It is a system for learning **how to think**, rather than simply **what to know**.

The goal is to build reusable mental models that can be applied across disciplines, connected back to real-world observations, and reconstructed months or years later.

---

# Why Learning OS?

Traditional learning often follows two extremes:

* **Textbook-driven**: systematic, but disconnected from reality.
* **Fragmented learning**: interesting, but lacking structure.

Learning OS combines both.

It follows a structured learning path while continuously connecting every concept to real-world examples, products, businesses, technology, and everyday decisions.

The objective is not to memorize knowledge, but to gradually construct a growing cognitive network.

---

# How It Works

Learning OS is designed to work with **AI coding agents** as collaborative thinking partners. The AI automatically takes on five specialized roles:

| Role | Responsibility |
|------|---------------|
| 🗺️ **Map Keeper** | Maintains the structure of each discipline, prevents fragmented learning |
| 🏗️ **Scaffolding Builder** | Builds new knowledge on top of what you already understand |
| 🔗 **Model Connector** | Identifies shared patterns across different disciplines |
| 🏛️ **Socratic Guide** | Encourages reasoning through questions before conclusions |
| 🧭 **Knowledge Curator** | Distills lessons, connects artifacts, synthesizes milestones, and supports long-term review |

The Knowledge Curator does not archive conversations. It preserves mechanisms, evidence, connections, cognitive change, and open questions as review-ready artifacts.

---

# Quick Start

## Prerequisites

- Git
- An AI coding agent (see platform-specific setup below)

## Step 1: Clone the Repository

```bash
git clone https://github.com/hericyoung/learning-os.git
cd learning-os
```

## Step 2: Choose Your AI Agent

### Option A: Gemini (VS Code / JetBrains IDE) — Native Support ✅

Learning OS is natively built as a **Gemini Skill**. No extra setup needed.

1. Open the project in your IDE with Gemini plugin installed
2. The skill in `.agents/skills/learning-os/` is **automatically discovered**
3. Start chatting — the skill activates when you discuss learning topics

### Option B: Claude Code (Anthropic)

Claude Code reads `CLAUDE.md` in the project root for instructions.

1. Make sure [Claude Code](https://docs.anthropic.com/en/docs/claude-code) is installed
2. Open the project directory:
   ```bash
   cd learning-os
   claude
   ```
3. Claude will automatically read the `CLAUDE.md` file and adopt the Learning OS behavior
4. Start learning!

### Option C: OpenAI Codex CLI

Codex CLI reads `AGENTS.md` in the project root for instructions.

1. Make sure [Codex CLI](https://github.com/openai/codex) is installed
2. Open the project directory:
   ```bash
   cd learning-os
   codex
   ```
3. Codex will automatically read the `AGENTS.md` file and adopt the Learning OS behavior
4. Start learning!

### Option D: Cursor

Cursor reads `.cursor/rules/` directory for project-specific rules.

1. Open the project in [Cursor](https://cursor.sh)
2. Cursor will automatically load the rules from `.cursor/rules/learning-os.mdc`
3. Start chatting in Cursor's AI panel

### Option E: GitHub Copilot

Copilot reads `.github/copilot-instructions.md` for project instructions.

1. Open the project in VS Code with GitHub Copilot enabled
2. Copilot will automatically read `.github/copilot-instructions.md`
3. Use Copilot Chat to start learning

### Option F: Manual Usage (No AI Agent)

If you don't have an AI agent, you can still use Learning OS as a knowledge framework:

1. Read `SPECIFICATION/Learning-OS-Spec.md` for the full methodology
2. Read `SPECIFICATION/Roadmap.md` for the learning progression
3. Use the templates in `.agents/skills/learning-os/resources/templates/` to manually create models, courses, observations, lesson summaries, milestones, and reflections
4. Copy any template to the corresponding directory and fill it in:
   ```bash
   cp .agents/skills/learning-os/resources/templates/model-template.md MODELS/my-model.md
   ```

## Step 3: Start Learning

Once your agent is set up, simply start a conversation:

- *"I want to understand why prices rise during a shortage"*
- *"Help me build a mental model for decision-making"*
- *"I noticed something interesting about how habits form — let's explore it"*
- *"Continue the Economics course from where we left off"*

The AI will follow the Learning OS methodology: start from reality, decompose with first principles, build models, apply across domains, connect to your knowledge map, and distill completed learning for future reconstruction.

## What v1.1 Generates

After the learner demonstrates understanding of a lesson, Learning OS creates a concise lesson summary containing the key model, reasoning, examples, prior connections, related models, limits, and a reconstruction prompt.

When all lessons in a declared course milestone are complete, it creates an integrated milestone summary. At that point it also asks the learner reflective questions; a reflection document is generated only from the learner's responses.

All artifacts are connected through `INDEX.md`. `CHANGELOG.md` records material changes, while duplicate-prevention rules keep one canonical home for each idea.

## Long-Term Review

Review is not definition drilling or a fixed spaced-repetition schedule. The learner:

1. Orients with the knowledge map and milestone.
2. Attempts reconstruction prompts before rereading.
3. Rebuilds models from first principles.
4. Tests them against old and new observations.
5. Compares reflection history to see cognitive change.
6. Refines canonical models and connections when understanding improves.

---

# Core Principles

* First-Principles Thinking
* Mental Models
* Structured Progression (Map)
* Real-World Landmarks
* Socratic Dialogue
* Cross-disciplinary Connections
* AI-assisted Scaffolding
* Continuous Reflection & Iteration

---

# Repository Structure

```text
learning-os/
├── .agents/skills/learning-os/  # Gemini Skill (native)
│   ├── SKILL.md                 # AI behavior definition
│   ├── references/              # Full specification & roadmap
│   ├── examples/                # Example learning sessions
│   └── resources/templates/     # Templates for all learning and knowledge artifacts
├── .cursor/rules/               # Cursor rules
├── .github/                     # GitHub Copilot instructions
├── CLAUDE.md                    # Claude Code instructions
├── AGENTS.md                    # OpenAI Codex / generic agent instructions
├── MODELS/                      # Reusable mental models (output)
├── COURSES/                     # Structured learning paths (output)
├── OBSERVATIONS/                # Real-world case studies (output)
├── KNOWLEDGE/                   # Lesson distillations, milestones, reflections
├── INDEX.md                     # Global knowledge graph and artifact registry
├── CHANGELOG.md                 # Versioned changes
├── SPECIFICATION/               # Original specification (reference)
└── README.md                    # Project documentation
```

---

# Learning Philosophy

Learning begins with reality.

Reality reveals patterns.

Patterns become models.

Models connect into systems.

Systems become intuition.

The ultimate goal is not to finish courses.

The ultimate goal is to develop a way of seeing and understanding the world.

---

# Current Status

**Version:** v1.1

Current focus:

* Building the Learning OS framework ✅
* Gemini Skill integration ✅
* Knowledge management and review system ✅
* Economics (in progress)

---

# License

This project is intended as a long-term personal knowledge system.

It is open to continuous evolution as new ideas, disciplines, and mental models are discovered.
