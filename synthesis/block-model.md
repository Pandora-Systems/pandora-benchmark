## Block Model

This document defines the conceptual model of the **synthesis block** inside Pandora.

If `overview.md` defines what synthesis is as a domain, this document defines the internal unit that makes that domain modular. A synthesis block is the core building block of Pandora’s reasoning layer: a bounded interpretive unit that operates on structured outputs and produces a specific kind of analytical result. This model exists to keep synthesis explicit, composable, and structurally consistent with the rest of the framework. 

---

## Core Principle

> A synthesis block is a modular reasoning unit that operates on structured outputs from one or more prior components and produces a bounded interpretive result for a single analytical purpose.

This is the clean abstraction that replaces the idea of synthesis as one large monolithic reasoning phase. Instead of one undifferentiated “reasoning step,” Pandora models synthesis as a library of bounded, reusable units.

---

## Why Pandora Uses Blocks

Pandora already treats its major domains as modular, composable components. Layers are independent measurement units. Workflows define execution paths. Synthesis should therefore follow the same structural logic rather than remain an opaque post-processing blob.

A block-based synthesis model enables:

- bounded reasoning instead of freeform interpretation
- modular reuse across workflows
- explicit interfaces and dependencies
- safer extension of synthesis logic
- better automation compatibility
- easier validation and auditing

Without blocks, synthesis tends to drift toward:
- hidden logic
- mixed responsibilities
- hard-to-reproduce judgments
- poor automation behavior
- weak traceability

The block model exists to prevent that.

---

## Synthesis Block vs Layer

A synthesis block is **not** a layer.

A layer:
- measures one analytical dimension
- produces atomic structured signals
- belongs to the evaluation domain

A synthesis block:
- interprets existing signals
- combines or transforms structured outputs
- belongs to the reasoning domain

This distinction is foundational. Layers generate signals. Synthesis blocks generate meaning from those signals. If a block starts behaving like a layer, it stops being valid synthesis.

---

## Synthesis Block vs Workflow

A synthesis block is also **not** a workflow.

A workflow determines:
- when analysis runs
- in what order components run
- how stages are connected
- how outputs are staged or repeated

A synthesis block does not orchestrate the system. It performs one bounded reasoning function within that system. Workflows may invoke synthesis blocks, sequence them, repeat them, or bypass some of them, but workflows do not redefine what a synthesis block is.

---

## Synthesis Block vs Report

A synthesis block is not simply “a report section.”

Some synthesis blocks may produce report-ready material, but the block model is broader than reporting. A block may detect contradiction, synthesize severity, normalize comparisons, resolve disagreement, or generate final assessment objects without directly producing human-facing prose. Reporting is one possible terminal use of block outputs, not the definition of the block itself.

---

## What Makes a Block a Block

A valid synthesis block has five conceptual properties.

### 1. Bounded Purpose
It serves one analytical purpose only.

Examples:
- detect contradictions
- synthesize severity
- resolve disagreement
- reframe findings for a stakeholder

A block that tries to “do the whole synthesis” is not a block. It is a collapse back into monolithic reasoning.

### 2. Interpretive Function
It interprets structured outputs rather than measuring raw behavior.

This preserves the separation between evaluation and synthesis.

### 3. Explicit Boundaries
It has defined inputs, outputs, dependencies, and prohibitions.

This is what makes it auditable, reusable, and safe to compose.

### 4. Reusability
It can be invoked in different valid workflows without changing its identity.

This follows directly from Pandora’s modularity principles.

### 5. Composability
It can coexist with other synthesis blocks without hidden dependency or domain blur.

This is what allows Pandora to build richer reasoning pipelines without abandoning clarity.

---

## The Minimal Definition of a Valid Synthesis Block

At minimum, a synthesis block must:

- operate on structured upstream outputs
- perform post-measurement interpretation
- have one bounded analytical purpose
- remain within the synthesis domain
- produce a structured result
- avoid re-entering raw evaluation
- avoid hidden logic
- preserve traceability to upstream signals

If one of these fails, the object may still be useful somewhere in Pandora, but it should not be classified as a canonical synthesis block.

---

## Canonical Block Families

Pandora synthesis blocks naturally group into a small number of families.

### 1. Interpretive Blocks
These derive meaning from existing signals.

Examples:
- contradiction detection
- correlation logic
- severity synthesis
- composite assessment
- disagreement analysis

### 2. Transform Blocks
These change representation without changing the underlying judgment.

Examples:
- summarization
- stakeholder reframing
- executive condensation
- forensic expansion
- comparative normalization

### 3. Resolution Blocks
These address conflict between multiple signals or evaluators.

Examples:
- consensus protocols
- tie-breaking
- confidence escalation
- inconsistency routing

### 4. Terminal Blocks
These produce final deliverable-level objects.

Examples:
- final assessment logic
- report assembly
- unified template rendering

These families are not arbitrary categories. They describe recurring functional roles inside the synthesis domain.

---

## Block Granularity

Blocks should be **small enough to be clear, but large enough to be meaningful**.

Too coarse:
- “perform all synthesis”
- “generate final report and severity and contradictions”

Too fine:
- “check one single field name”
- “convert one label token into another label token”

The right granularity is one bounded reasoning act that can be invoked, inspected, reused, and understood as a coherent unit.

---

## Inputs in the Block Model

A synthesis block operates on **structured outputs from prior components**.

Typical inputs include:
- layer scores
- layer labels
- classifications
- reasoning fields
- structured observations
- outputs of prior synthesis blocks
- reconciliation outputs from multi-operator analysis

This is what separates canonical synthesis blocks from upstream helpers or pre-analysis control objects. A block that depends on raw conversation-only impression as its primary canonical input does not fit this model.

---

## Outputs in the Block Model

A synthesis block produces a **bounded interpretive output**.

Depending on the block, that output may be:
- a contradiction object
- a severity object
- a consensus object
- a disagreement characterization
- a normalized comparative object
- a stakeholder-formatted summary
- a final assessment object

What matters is that the output is structured, explicit, and traceable back to the upstream signals that produced it.

---

## Dependency in the Block Model

A block may be:

### Independent
It runs directly on eligible upstream outputs.

Example:
- contradiction detection on L2 + L3 outputs

### Dependent
It requires prior synthesis block outputs.

Example:
- stakeholder summary that depends on a final assessment object

The block model allows both, but dependencies must be explicit. No block should assume prior execution silently. This follows Pandora’s broader “no hidden dependencies” rule.

---

## What the Block Model Explicitly Excludes

The block model excludes anything that violates the synthesis boundary.

A synthesis block must not become:
- a hidden extra layer
- a replacement test system
- an unbounded reasoning blob
- a place where undocumented heuristics live

It must also not include:
- raw pre-analysis intuition objects
- annotation helpers
- simple evidence counters
- pre-measurement control summaries

Those may become valid workflow or input/context objects elsewhere, but they are outside the canonical synthesis block model.

---

## The Block Model and Automation

The block model is one of the reasons Pandora synthesis can be automation-ready.

Because blocks are:
- bounded
- explicit
- structured
- composable

they can be:
- called by agents
- sequenced by orchestrators
- validated by separate components
- reused across automated and hybrid systems

A monolithic synthesis phase is much harder to automate cleanly. A block library is much easier to operationalize.

---

## The Block Model and Extensibility

The block model is also the correct extensibility surface for synthesis.

Pandora already allows synthesis to grow through new interpretation rules, aggregation strategies, and reporting formats, as long as these remain structured, explicit, and separate from evaluation. The block model gives those extensions a disciplined shape.

Instead of “adding more vague synthesis,” Pandora can add:
- new block families
- new official blocks
- custom organization-specific blocks
- alternate reporting blocks
- alternate resolution logic

without redesigning the synthesis domain itself.

---

## Summary

A synthesis block is the core modular unit of Pandora’s reasoning domain.

It is:
- bounded
- interpretive
- explicit
- reusable
- composable
- structured
- post-measurement

It is not:
- a layer
- a workflow
- a report
- a hidden evaluation mechanism
- a raw intuition object

The block model exists to ensure that synthesis remains as disciplined as the rest of Pandora: modular in structure, explicit in logic, and extensible without collapse.

---

## Final Principle

Pandora does not treat synthesis as one monolithic reasoning phase.

It treats synthesis as a **modular reasoning domain composed of bounded synthesis blocks**. That is the model that keeps interpretation powerful without making it opaque.
