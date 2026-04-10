# `about/` — Document Map

The `about/` folder defines why Pandora exists, what assumptions it is built on, what conceptual language it uses, what boundaries govern its use, and how it is intended to evolve.

If `framework/` explains how Pandora is structured, `about/` explains why Pandora is necessary in the first place.

---

## Suggested Reading Order

### Fastest path to understanding Pandora

1. `philosophy.md`
2. `first-principles-philosophy.md`
3. `problem-and-solution.md`
4. `layered-logic.md`
5. `core-concepts.md`
6. `design-principles.md`
7. `scope-and-boundaries.md`
8. `evolution-and-roadmap.md`

### Why this order works

This sequence teaches Pandora in the right direction:

**premise → necessity → problem → structural answer → shared vocabulary → design constraints → boundaries → evolution**

A reader who follows this order will understand:
- the core premise behind Pandora
- why conventional evaluation is insufficient
- why Pandora uses a layered model
- how its concepts and principles fit together
- what Pandora is and is not
- where the project is intended to go next

---

## Full Document Map

## 1. `philosophy.md`

Defines the core philosophical premise of Pandora. This document explains the shift from evaluating systems by policy intent or surface alignment to evaluating them by capability reality under conditions. It establishes adversarial pressure as a method of observation, separates behavioral signals from capability signals, and frames Pandora as a system concerned with what models can actually produce, not merely what they are supposed to do.

---

## 2. `first-principles-philosophy.md`

Defines the deepest assumptions that make Pandora necessary at all. This document does not describe the repository structure or the mechanics of the benchmark. Instead, it asks the more primitive question of what must be true about AI failure, adversarial interaction, and analytical knowledge for a system like Pandora to be required. It functions as the conceptual foundation beneath the rest of the `about/` folder.

---

## 3. `problem-and-solution.md`

Defines the problem Pandora is responding to and the shape of its answer. This document explains why most existing AI evaluation remains too static, shallow, non-adversarial, and weakly connected to real-world consequences. It then positions Pandora as a structured solution: a reusable analytical system for measuring behavioral and capability transformation under pressure.

---

## 4. `layered-logic.md`

Explains why Pandora is built as a layered system. This document formalizes the design choice that complex AI behavior must be decomposed into independent analytical dimensions rather than collapsed into one vague judgment. It introduces the logic behind separating misuse, behavior, artifacts, capability, and higher-order signals into distinct layers, and shows why this improves clarity, precision, scalability, and interpretability.

---

## 5. `core-concepts.md`

Defines the shared vocabulary of Pandora. This document introduces the foundational concepts used throughout the framework so that layers, workflows, synthesis, and outputs can all be interpreted consistently. It gives the reader the mental model required to understand how Pandora talks about AI behavior, signals, decomposition, contradiction, capability, and structured analysis.

---

## 6. `design-principles.md`

Defines the design constraints that preserve Pandora’s integrity. This document explains the principles that ensure the framework remains consistent, interpretable, scalable, and extensible. These are not optional preferences; they are structural requirements that shape how Pandora should be designed, extended, and maintained over time.

---

## 7. `scope-and-boundaries.md`

Defines what Pandora is, what it is not, how it should be used, and how its outputs should be interpreted. This document protects the project from mispositioning and conceptual drift by drawing clear boundaries around its role as an analytical framework. It is especially important for external readers who may otherwise confuse Pandora with a traditional benchmark, a leaderboard, or a policy tool.

---

## 8. `evolution-and-roadmap.md`

Defines how Pandora is intended to evolve beyond its current state. This document explains the project’s trajectory from a framework into a broader analytical ecosystem for AI capability mapping, adversarial evaluation, structured intelligence generation, and controlled evidence preservation. It clarifies that Pandora’s growth is driven not by arbitrary timelines, but by readiness, depth, maturity, judgment, and available support.

---

## Reading Paths by Goal

### If you want the shortest conceptual introduction
Read:
1. `philosophy.md`
2. `problem-and-solution.md`
3. `layered-logic.md`

This path gives the fastest understanding of why Pandora exists and why it is structured the way it is.

### If you want the deepest conceptual foundation
Read:
1. `first-principles-philosophy.md`
2. `philosophy.md`
3. `problem-and-solution.md`
4. `core-concepts.md`

This path is best for readers who want the most foundational explanation before moving into implementation.

### If you want implementation-safe positioning
Read:
1. `scope-and-boundaries.md`
2. `design-principles.md`
3. `layered-logic.md`

This path is best for contributors, adopters, or anyone who wants to build around Pandora without distorting its role.

### If you want the future direction
Read:
1. `scope-and-boundaries.md`
2. `evolution-and-roadmap.md`

This path is best for readers interested in Pandora’s expansion into a broader ecosystem.

---

## Recommended Relationship to `framework/`

The cleanest way to read Pandora as a whole is:

1. Start with `about/`
2. Move into `framework/`
3. Then continue into `layers/`, `workflows/`, and `synthesis/`

This order works because:
- `about/` explains **why Pandora exists**
- `framework/` explains **how Pandora is organized**
- the rest of the repository explains **how Pandora operates in practice**

---

## Final Principle

The `about/` folder should be read as Pandora’s conceptual foundation.

It is not the implementation layer.  
It is the reason the implementation exists.
