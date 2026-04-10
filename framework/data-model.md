# Data Model

## Purpose

This document defines the **logical data model** of Pandora.

It specifies the core analytical objects the framework operates on, the relationships between those objects, and the distinction between raw inputs, intermediate analytical states, and final outputs.

The data model does not define presentation formatting, interface design, or implementation-specific storage choices.
It defines the **structural logic of Pandora data**.

---

## Core Principle

> Pandora must produce analytical data that remains structured, traceable, and composable across the full lifecycle of evaluation.

The data model exists so that Pandora outputs can be:

- interpreted by humans
- processed by machines
- compared across runs
- validated across operators
- stored in datasets
- reused across workflows and synthesis protocols

---

## Why a Data Model Is Necessary

Pandora is not only a conceptual framework.
It is a system intended to generate analytical objects that can move across:

- layers
- workflows
- synthesis processes
- validation procedures
- reporting systems
- storage and retrieval environments

Without a data model, those objects become inconsistent, difficult to compare, and difficult to automate.

The data model ensures that Pandora outputs remain:

- structurally legible
- interoperable
- versionable
- reusable

---

## Data Model Scope

The Pandora data model covers:

- input objects
- context objects
- layer output objects
- synthesis input objects
- synthesis output objects
- validation objects
- final output objects
- metadata required for traceability

It does not prescribe one exact serialization format.
Those details belong to schemas and implementation.

This document defines the logical structure that those schemas must represent.

---

## Primary Data Objects

Pandora operates on a small set of primary analytical objects.

### 1. Input Object

The input object is the material being analyzed.

Examples include:

- a full conversation
- a conversation segment
- a single prompt–response pair
- a batched evaluation unit

An input object should preserve:

- raw content
- role structure
- turn order
- scope boundaries
- identifying metadata where needed

The input object is the anchor of the entire analytical process.

---

### 2. Evaluation Context Object

The context object defines the conditions under which the input is evaluated.

This may include:

- selected layers
- scope
- workflow identity
- execution mode
- operator model
- version identifiers
- methodology references
- relevant execution metadata

The context object does not change the input.
It defines how the input is being processed.

---

### 3. Layer Result Object

A layer result object captures the output of one layer applied to a defined input under a defined context.

A layer result typically contains:

- layer identifier
- test results
- scores or labels
- reasoning fields
- local metadata
- references to input scope

A layer result is a **measurement object**.
It should remain interpretable without synthesis.

---

### 4. Test Result Object

Within a layer result, the smallest standard analytical unit is the test result.

A test result typically includes:

- test identifier
- purpose or dimension
- score and/or label
- reasoning
- optional local evidence reference
- local confidence or ambiguity notes where supported

The test result object is the atomic unit of structured evaluation.

---

### 5. Intermediate Analytical State

Pandora may store intermediate states between stages of execution.

These may include:

- collected layer results prior to synthesis
- staged outputs from repeated passes
- validation-ready bundles
- partial execution states in complex workflows

Intermediate states are useful because Pandora does not always operate as a single-pass linear process in practice.

---

### 6. Synthesis Input Object

The synthesis input object is the bundle of structured analytical signals consumed by synthesis.

This bundle may include:

- selected layer outputs
- validation indicators
- relevant context metadata
- contradiction candidates
- aggregation-ready structures

The synthesis input object does not contain final meaning.
It contains the structured signals from which higher-order interpretation is formed.

---

### 7. Synthesis Result Object

The synthesis result object contains the output of interpretive logic operating on structured analytical signals.

This may include:

- correlations
- contradictions
- severity conclusions
- composite interpretations
- narrative findings
- structured summary judgments

The synthesis result is downstream from measurement and should remain traceable to the signals it was built from.

---

### 8. Validation Object

Validation objects represent information produced through comparison, repetition, or agreement analysis.

They may include:

- repeated-run comparisons
- inter-operator comparisons
- disagreement flags
- agreement metrics
- traceability links across runs
- stability indicators

Validation objects do not replace analytical outputs.
They qualify and contextualize their reliability.

---

### 9. Final Output Object

The final output object is the completed analytical product emitted by Pandora.

This may include:

- full report objects
- structured benchmark entries
- exportable dataset rows
- operator-facing summaries
- system-facing machine-readable outputs

The final output object may combine:

- synthesis results
- validation information
- selected raw or intermediate structures
- reporting metadata

---

## Data Relationships

The primary relationships in the Pandora data model follow the structure of the analytical process.

### Input → Context

An input is evaluated under a defined context.

### Input + Context → Layer Results

Layer results are produced by applying one or more layers to the input under that context.

### Layer Results → Intermediate State

Collected layer outputs may be stored as a reusable intermediate bundle.

### Intermediate State → Synthesis Input

Relevant structured signals are selected and packaged for synthesis.

### Synthesis Input → Synthesis Result

Synthesis generates higher-order analytical conclusions from structured signals.

### Layer Results / Runs / Operators → Validation Objects

Validation emerges by comparing outputs across passes, runs, or evaluators.

### Synthesis Result + Validation + Metadata → Final Output

Final outputs are assembled from the relevant analytical products generated across the process.

---

## Required Data Properties

All Pandora analytical objects should preserve a common set of properties.

### 1. Structure

Objects must be representable in a consistent structured form.

### 2. Traceability

Objects must be linkable back to:

- source input
- scope
- layer or analytical stage
- operator or execution context where relevant

### 3. Composability

Objects must be reusable across workflows, synthesis protocols, and validation processes without requiring reinterpretation.

### 4. Stage legibility

It must remain clear whether an object belongs to:

- input
- measurement
- intermediate storage
- synthesis
- validation
- final output

### 5. Compatibility

Objects should be designed so that schemas, tooling, datasets, and reporting systems can operate on them consistently.

---

## Separation of Data Types by Analytical Role

The data model must preserve the same analytical separations that the framework preserves conceptually.

### Measurement data

Produced by layers.
Contains scores, labels, classifications, and evidence-linked reasoning.

### Interpretive data

Produced by synthesis.
Contains cross-signal meaning, contradictions, escalation logic, and conclusions.

### Validation data

Produced by comparative analysis across runs, operators, or configurations.
Contains stability and agreement information.

### Reporting data

Produced when analytical objects are assembled into a final output form for human or machine use.

These data types may connect.
They must not collapse into one another.

---

## Metadata Requirements

Pandora data objects should support metadata that makes the system auditable and reusable.

Examples include:

- input identifier
- conversation or session identifier
- layer identifier
- test identifier
- workflow identifier
- operator identifier where relevant
- model identifier where relevant
- version identifier
- timestamp or run marker
- scope marker
- methodology reference where relevant

Metadata exists to support:

- traceability
- validation
- reproducibility
- dataset integrity
- longitudinal comparison

---

## Granularity

The data model must support multiple levels of granularity.

At minimum, Pandora should be able to represent:

- whole-input objects
- segment-level objects
- layer-level objects
- test-level objects
- synthesis-level objects
- final-output objects

This matters because Pandora may be used for:

- one-off analysis
- interaction-by-interaction evaluation
- conversation-level analysis
- large-scale dataset generation
- comparative benchmarking

A data model that only works at one granularity level is too weak for the framework.

---

## Data Model and Schemas

This document defines the **logical structure** of Pandora data.

The `schemas/` layer of the repository should define the **formal representations** of that structure.

In other words:

- this document defines **what objects exist and how they relate**
- schemas define **how those objects are encoded and validated**

This distinction keeps the data model implementation-agnostic while still making formalization possible.

---

## Data Model and Output Standardization

The data model is related to, but distinct from, output standardization.

- the **data model** defines the object structure and relationships
- **output standardization** defines naming consistency, formatting discipline, and representational uniformity

The data model answers:

> what analytical objects exist?

Output standardization answers:

> how should they be represented consistently?

Both are required.
They are not the same document.

---

## What the Data Model Prevents

Without a clear data model, Pandora risks:

- inconsistent output structures
- weak interoperability across tools
- reduced automation compatibility
- unclear distinction between stages
- broken validation traceability
- poor dataset integrity
- confusion between raw signals and interpreted outputs

The data model exists to prevent those failures by making Pandora’s analytical objects explicit.

---

## Summary

Pandora’s data model defines the core analytical objects of the framework and the relationships between them.

It ensures that inputs, context, layer outputs, synthesis structures, validation objects, and final outputs remain:

- structured
- traceable
- interoperable
- stage-specific
- reusable

This makes Pandora not only analytically coherent, but operationally durable.

---

## Final Principle

Pandora must not generate isolated answers.

It must generate analytical objects that remain meaningful wherever they move in the system.