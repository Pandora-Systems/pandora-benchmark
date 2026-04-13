# Analysis Lifecycle

## Purpose

This document defines the **canonical lifecycle of a single Pandora analysis**.

It specifies the fixed stage structure through which an input becomes structured analytical output.

It defines:

- what stages exist
- the order in which they occur
- the structural constraints that preserve lifecycle identity

It does **not** define workflow variants, operator arrangements, automation strategies, schema formats, or report styles.

---

## Core Principle

> Every valid Pandora analysis follows the same six-stage lifecycle, even when the selected analytical path differs.

Pandora may vary in:
- scope,
- selected layer path,
- route depth,
- resourcing,
- and execution method.

What does not vary is the structural stage skeleton.

The lifecycle is therefore fixed at the level of stages, not at the level of analytical width. A run may be structurally complete without being analytically maximal.

---

## Canonical Lifecycle

Every Pandora analysis progresses through these six stages:

1. **Input Ingestion**
2. **Context Framing**
3. **Layer Execution**
4. **Intermediate Output Generation**
5. **Synthesis**
6. **Final Output Generation**

These stages define the minimum structural progression of a valid Pandora analysis. They do not imply that every valid run must execute the full available layer stack.

What varies by workflow or freestyle route is the selected analytical path inside the lifecycle. A valid run may execute:
- one selected layer,
- a narrow lawful subset of layers,
- or a broader multi-layer route,

as long as the run still passes through the same structural progression:
input → framing → selected analytical execution → intermediate outputs → synthesis → final output. 

---

## Stage Definitions

### 1. Input Ingestion

A defined object of analysis is supplied.

Valid inputs may include:

- a full conversation
- a partial interaction sequence
- a single prompt-response pair
- a batch of interactions

The input must be:

- clearly bounded
- identifiable as the object of analysis
- preserved as the source material for downstream stages

---

### 2. Context Framing

The analytical context is defined before measurement begins.

This may include:

- selected layers
- scope of analysis
- intended granularity
- execution context
- synthesis destination

Context framing defines **how the input will be evaluated**.
It does not alter the input or produce analytical conclusions.

---

### 3. Layer Execution

The declared analytical path is executed against the input.

In many runs this takes the form of selected layer execution. That path may contain:
- one layer,
- a lawful subset of layers,
- or a broader multi-layer route,
depending on the declared scope and execution design.

At this stage:

- each layer performs measurement within its own analytical dimension
- each layer uses only layer-valid inputs
- each layer produces outputs within its own scope

Layer execution is the measurement phase of Pandora.

---

### 4. Intermediate Output Generation

Executed layers emit structured analytical outputs.

These may include:

- scores
- labels
- classifications
- observations
- reasoning

Intermediate outputs are **layer-bounded analytical signals**.
They are not final judgments.

---

### 5. Synthesis

Synthesis operates on the outputs produced by executed layers.

This stage may include:

- cross-layer correlation
- contradiction detection
- aggregation
- significance or severity formation
- pattern-level interpretation

Synthesis is the stage where independent analytical signals become integrated conclusions.

---

### 6. Final Output Generation

The completed analysis is rendered into reusable outputs.

These may include:

- full reports
- summaries
- benchmark records
- structured dataset entries
- comparative outputs

Final outputs may be human-readable, machine-readable, or both.

---

## Lifecycle Constraints

The lifecycle preserves several non-negotiable constraints.

### Input precedes framing
The object of analysis must exist before the analytical lens is defined.

### Framing precedes measurement
Scope and context must be set before layers are executed.

### Measurement precedes interpretation
Layer execution and intermediate outputs must occur before synthesis.

### Synthesis precedes final output
Final outputs are downstream products of completed interpretation.

### Stage order is fixed
The lifecycle allows execution flexibility inside stages, but not structural reordering across stages.

---

## Lifecycle Identity

A Pandora analysis remains lifecycle-compliant only if all six stage types remain structurally present, whether explicit or embedded in a larger execution system.

This requirement does not mean that every run must execute the broadest available analytical path. It means only that every valid run must preserve:
- input ingestion,
- context framing,
- selected analytical execution,
- preserved intermediate outputs,
- downstream synthesis,
- and final output generation.

The lifecycle is therefore independent of:
- specific workflows,
- selected layer width,
- operator topologies,
- automation styles,
- reporting formats,
- and deployment scale.

These factors change **how the lifecycle is instantiated**, not **what the lifecycle is**.

---

## Allowed Variation

Variation is allowed **within** the lifecycle, not **instead of** it.

Examples of valid variation include:

- single-layer, partial-layer, or broader multi-layer analytical paths
- interaction-level, segment-level, or conversation-level scope
- single-pass or multi-pass execution
- workflow-mode or freestyle-mode execution
- manual, hybrid, or automated operation
- centralized or distributed execution

None of these variations changes the canonical six-stage structure.

---

## What This Document Protects Against

This lifecycle definition prevents:

- collapsing framing into measurement
- collapsing synthesis into layer execution
- treating reports as if they were raw analytical outputs
- mistaking workflow variation for structural change

Its purpose is to preserve a stable analytical spine across different Pandora deployments.

---

## Summary

The Pandora analysis lifecycle defines the fixed structural progression of analysis:

**input → framing → layer execution → intermediate outputs → synthesis → final outputs**

It ensures that Pandora can vary operationally without losing structural identity.

---

## Final Principle

Pandora can vary in execution.
Its lifecycle must remain constant in structure.
