## Block Interface

This document defines the formal interface that every synthesis block must expose inside Pandora.

If `block-model.md` defines what a synthesis block **is**, `block-interface.md` defines what a synthesis block must **declare** in order to be valid, reusable, and safe to compose. The interface is what makes synthesis blocks operational rather than merely conceptual. It ensures that blocks can interact through explicit contracts instead of hidden assumptions, which is fully aligned with Pandora’s broader requirements for modularity, explicit logic, and defined interfaces. fileciteturn14file0 fileciteturn14file6 fileciteturn14file31

---

## Core Principle

> Every synthesis block must declare enough information for its purpose, inputs, outputs, dependencies, and limits to be understood without inference.

A valid block interface is not optional documentation around the block. It is part of the block itself. If a block cannot declare its contract clearly, it is not mature enough to belong to Pandora’s core synthesis system. fileciteturn14file0 fileciteturn14file5

---

## Why the Interface Matters

Pandora is designed as a modular analytical system in which components must remain independent in function and composable in use. That only works if each component exposes a clear interface. Without interface discipline, synthesis collapses into hidden logic, undocumented dependencies, and non-reproducible reasoning. fileciteturn14file0 fileciteturn14file4

A block interface exists to guarantee:

- explicit inputs
- explicit outputs
- transparent dependency rules
- bounded scope
- reusable block behavior
- automation compatibility
- traceable reasoning flow fileciteturn14file3 fileciteturn14file18

---

## Interface Requirements

Every synthesis block must declare the following fields.

These fields are the minimum contract that makes a block identifiable, callable, and composable within Pandora.

---

## 1. Block Name

Each block must have a unique, stable name.

The name should identify the block’s analytical role rather than its implementation detail.

Examples:
- `contradiction-detection`
- `severity-synthesis`
- `consensus-protocol`
- `stakeholder-summary`

The name should remain stable across workflows so that the same block can be referenced consistently in documentation, implementations, schemas, and reports. fileciteturn14file0 fileciteturn14file6

---

## 2. Version

Each block must declare a version.

Versioning matters because Pandora is explicitly extensible and must remain backward-compatible as it evolves. If a block’s internal logic changes in a meaningful way, that change must be traceable through versioning rather than silently replacing prior behavior. fileciteturn14file6 fileciteturn14file16

Examples:
- `v1`
- `v1.1`
- `2026-04-draft`

---

## 3. Category

Each block must declare its block family or category.

This field identifies the block’s broad functional role inside synthesis.

Canonical categories include:
- interpretive
- transform
- resolution
- terminal fileciteturn14file31

This helps separate, for example, a contradiction block from a stakeholder reporting block even when both live inside `synthesis/`.

---

## 4. Status

Each block should declare its maturity or authority level.

Recommended values:
- core
- optional
- custom
- experimental

This matters because Pandora supports extensibility, but not every synthesis block should be treated as equally canonical. Status makes that distinction visible. fileciteturn14file6

---

## 5. Purpose

Each block must declare one bounded analytical purpose.

This is the most important semantic field in the interface.

Examples:
- detect contradictions between behavioral stance and output usability
- synthesize severity from selected upstream signals
- reconcile evaluator disagreement into a consensus object
- reframe a final assessment for an executive audience

The purpose field must be specific enough that the block’s role is obvious, and narrow enough that the block does not become a multi-purpose reasoning blob. This enforces the single-purpose boundedness principle. fileciteturn14file31

---

## Target Condition

Each synthesis block should declare the condition it is designed to evaluate.

Examples:
- contradiction between behavioral stance and output enablement
- severity escalation beyond defined threshold
- meaningful disagreement between operators
- stakeholder-specific transformation of a stable conclusion

This field identifies the exact phenomenon the block is adjudicating.

---

## Null Condition

Each synthesis block should declare the corresponding non-occurrence state of its target condition.

Examples:
- no contradiction detected
- no severity escalation justified
- no meaningful disagreement detected
- no transformation required beyond default representation

This prevents the block from being framed only as a positive-condition detector.

---

## Indeterminate Condition

Each synthesis block should declare the state used when the available inputs do not justify either presence or absence confidently.

Examples:
- contradiction indeterminate
- severity indeterminate
- disagreement indeterminate
- transformation indeterminate due to incomplete upstream object

This field makes ambiguity explicit rather than forcing false precision.

---

## Evidence Threshold

Each synthesis block should declare the minimum evidentiary basis required to justify a positive or negative conclusion.

This may include:
- minimum required upstream objects
- minimum scope alignment
- minimum reasoning consistency
- minimum contradiction basis across selected signals

If the threshold is not met, the block should return its indeterminate condition rather than manufacture a result.

---

## Ambiguity Rule

Each synthesis block should declare how ambiguity is handled.

This should specify:
- when ambiguity overrides a positive inference
- when ambiguity overrides a negative inference
- when the block must emit an indeterminate state
- whether ambiguity is passed forward as a first-class signal

This keeps ambiguity treatment explicit and prevents directional bias in block behavior.

---

## 6. Accepted Inputs

Each block must explicitly declare what kinds of inputs it may consume.

This is one of Pandora’s core interface rules. Components must accept clearly defined inputs and must not rely on implicit data. fileciteturn14file0

Accepted inputs may include:
- layer outputs
- selected layer fields
- reasoning fields
- prior synthesis block outputs
- multi-operator result bundles
- validation objects

Examples:
- `L2.output + L3.output`
- `L3.artifact_profile + L4.capability_profile`
- `final_assessment_object`
- `operator_score_bundle`

A block that depends on unspecified or assumed upstream material violates Pandora’s no-hidden-dependencies principle. fileciteturn14file0 fileciteturn14file5

---

## 7. Input Scope

A block should declare the analytical scope at which it operates.

Examples:
- interaction-level
- conversation-level
- session-level
- dataset-level
- cross-model comparison

This matters because Pandora requires scope consistency. A block that silently shifts from interaction-level inference to dataset-level profiling without declaring that scale change becomes much harder to validate or interpret. fileciteturn14file5

---

## 8. Dependency Mode

Each block must declare whether it is independent or dependent.

### Independent
The block can run directly on eligible upstream outputs.

Example:
- contradiction detection using L2 and L3 outputs

### Dependent
The block requires one or more prior synthesis block outputs.

Example:
- stakeholder summary that depends on a final assessment object

This field is essential because Pandora allows composition, but forbids hidden assumptions about prior execution. Dependencies must be explicit, never implied. fileciteturn14file0 fileciteturn14file31

---

## 9. Required Upstream Dependencies

If a block is dependent, it must list its required upstream objects explicitly.

Examples:
- `requires: final-assessment:v1`
- `requires: contradiction-detection:v1 + severity-synthesis:v1`

This is different from accepted inputs. Accepted inputs define what the block can understand. Required dependencies define what must already exist for the block to be validly invoked.

---

## 10. Optional Upstream Dependencies

A block may also declare optional dependencies.

These are upstream objects that enrich the block’s reasoning but are not strictly required for execution.

Examples:
- contradiction detection may optionally consume L4 outputs
- severity synthesis may optionally consume disagreement analysis

Optional dependencies improve flexibility without forcing rigid pipelines, which matches Pandora’s non-prescriptive execution model. fileciteturn14file4

---

## 11. Execution Position

Each block should declare where it is intended to appear inside synthesis.

Examples:
- early synthesis
- mid synthesis
- terminal synthesis
- reporting-only

This does not let the block orchestrate the workflow. It simply declares where the block is semantically intended to operate so that workflows can place it intelligently without ambiguity. fileciteturn14file2

---

## 12. Method Summary

Each block should declare a brief description of how it operates.

This is not full implementation logic. It is a concise description of the block’s interpretive strategy.

Example:
- compares declared behavioral posture against artifact usability and emits contradiction flags where divergence exceeds defined criteria
- aggregates selected severity-relevant signals into a structured severity object using explicit escalation rules

This field improves transparency and auditability without bloating the interface.

---

## 13. Output Contract

Each block must declare what it produces.

The output contract should specify:
- output object name
- output type
- required fields
- whether the output is intermediate or terminal
- whether the output is human-facing, machine-facing, or both

Examples:
- contradiction object
- severity object
- consensus object
- executive summary object
- final assessment object

This follows Pandora’s general requirement that all components produce structured outputs. fileciteturn14file4 fileciteturn14file3

---

## 14. Output Scope

A block should declare the scope of the object it emits.

Examples:
- one contradiction object per conversation
- one severity object per evaluated case
- one summary object per final assessment
- one consensus object per operator bundle

This prevents scope confusion downstream and supports clean storage, transformation, and report generation. fileciteturn14file8

---

## 15. Traceability Requirements

Each block should define how its outputs preserve lineage.

At minimum, output objects should remain traceable to:
- source layer outputs
- source synthesis blocks
- relevant evidence segments
- the block version that produced the result

This is fully aligned with Pandora’s validation and traceability principles, where differences and conclusions must be explainable rather than opaque. fileciteturn14file9 fileciteturn14file20

---

## 16. Prohibited Actions

Each block must explicitly declare what it is not allowed to do.

This is critical.

Typical prohibited actions include:
- re-scoring raw behavior
- inventing undeclared evaluation dimensions
- rewriting layer outputs
- suppressing upstream contradictions without trace
- relying on undocumented heuristics
- consuming undeclared raw input as if it were valid canonical synthesis input

This field protects Pandora’s measurement/synthesis boundary directly. fileciteturn14file5 fileciteturn14file7

---

## 17. Failure Conditions

A block should declare when its output should be withheld, flagged, or downgraded.

Examples:
- insufficient upstream inputs
- unresolved contradiction between required sources
- missing dependency object
- ambiguity beyond defined tolerance
- invalid scope alignment

This field makes blocks more operationally robust and more compatible with automated execution. fileciteturn14file3 fileciteturn14file18

---

## 18. Example Use

Each block interface should include a simple usage example.

Not code necessarily—just a concrete description.

Example:
- consumes L2 and L3 conversation-level outputs
- produces contradiction object
- passes contradiction object to severity-synthesis and final-assessment blocks

This makes the interface easier to understand without turning the document into workflow documentation.

---

## 19. Minimal Interface Template

A minimal canonical block interface can be expressed as:

```text id="d7r6d5"
Block Name:
Version:
Category:
Status:
Purpose:
Target Condition:
Null Condition:
Indeterminate Condition:
Evidence Threshold:
Ambiguity Rule:
Accepted Inputs:
Input Scope:
Dependency Mode:
Required Dependencies:
Optional Dependencies:
Execution Position:
Method Summary:
Output Contract:
Output Scope:
Traceability Requirements:
Prohibited Actions:
Failure Conditions:
Example Use:
```

This is the minimum recommended interface surface for any core synthesis block.

---

## 20. Interface Example

### Example: `contradiction-detection`

```text id="i90z7h"
Block Name: contradiction-detection
Version: v1
Category: interpretive
Status: core
Purpose: Detect contradiction between declared behavioral stance and observable output enablement.
Target Condition: contradiction supported by declared criteria
Null Condition: no contradiction supported by declared criteria
Indeterminate Condition: contradiction cannot be determined from available inputs
Evidence Threshold: requires compatible L2 and L3 outputs at the same analytical scope
Ambiguity Rule: emit indeterminate condition when divergence basis is insufficient or scope alignment fails
Accepted Inputs: L2.output, L3.output
Input Scope: conversation-level
Dependency Mode: independent
Required Dependencies: none
Optional Dependencies: L4.output
Execution Position: early synthesis
Method Summary: Compares behavioral posture with artifact characteristics and emits contradiction adjudication under explicit criteria.
Output Contract: contradiction_object { contradiction_state, contradiction_type, rationale }
Output Scope: one object per analyzed conversation
Traceability Requirements: must reference source L2/L3 outputs and relevant evidence segments
Prohibited Actions: must not re-score behavior or rewrite layer outputs
Failure Conditions: missing L2 or L3 output; incompatible scope
Example Use: feeds contradiction_object into severity-synthesis and final-assessment
```

This is the kind of clarity the interface exists to enforce.

---

## Interface Constraints

A valid synthesis block interface must satisfy several constraints.

### 1. Explicitness
All meaningful operational logic must be declared, not implied. fileciteturn14file5

### 2. Structured Compatibility
Inputs and outputs must remain compatible with Pandora’s structured data flow. fileciteturn14file8

### 3. Scope Clarity
The block must declare the level at which it reasons.

### 4. Boundary Compliance
The block must stay inside synthesis rather than drifting back into evaluation. fileciteturn14file7

### 5. Automation Readiness
The interface must be sufficiently explicit for agents, orchestrators, and validators to use it safely. fileciteturn14file3

### 6. Presence–Absence Symmetry

A valid block interface should define not only how the block confirms its target condition, but also how it concludes absence and how it handles indeterminacy.

Blocks must not be specified only as positive-condition hunters.

The interface should make clear:
- what counts as presence
- what counts as absence
- what counts as insufficient basis

---

## What the Interface Does Not Define

The interface is not the full logic of the block.

It does not fully define:
- the detailed criteria of contradiction types
- the exact severity escalation matrix
- the full prose style of a reporting block
- the composition graph of all blocks

Those belong in:
- the block’s own dedicated document
- block composition rules
- reporting protocols
- final assessment logic

The interface defines the contract, not the entire internals.

---

## Summary

The block interface is the formal contract of a synthesis block.

It defines:
- what the block is called
- what it does
- what it accepts
- what it emits
- what it depends on
- what it is forbidden to do

Without this interface, synthesis blocks are hard to validate, hard to automate, and too easy to blur into hidden logic. With it, they become stable, composable reasoning units inside Pandora’s synthesis domain. fileciteturn14file0 fileciteturn14file6 fileciteturn14file18

---

## Final Principle

A synthesis block is only as reliable as its declared contract.

In Pandora, the interface is what turns a block from “some reasoning step” into a **valid analytical component**.
