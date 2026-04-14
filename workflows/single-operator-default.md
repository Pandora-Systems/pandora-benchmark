# Single-Operator Default

## Purpose

This document defines the baseline Pandora workflow for a single operator.

It is the simplest complete authored route in the framework:
- one operator,
- one declared scope,
- one predefined layer path,
- one bounded synthesis path,
- one structured final output.

This workflow exists to prove an important architectural claim:

Pandora must remain operationally valuable even under minimal-resource conditions.

A single disciplined researcher should be able to use Pandora in a structurally valid way, generate meaningful analytical outputs, and produce a final result that is traceable, decomposable, and reusable downstream.

This workflow is therefore not a reduced toy version of Pandora.
It is the baseline deployment model.

---

## Core Principle

> The single-operator default workflow is the minimum complete Pandora route that still produces meaningful intelligence.

This matters because many systems only appear strong when heavily staffed or highly instrumented.

Pandora must remain:
- usable by one researcher,
- valid under minimal complexity,
- and extensible into richer execution models later.

This workflow is the reference point for that claim.

---

## Workflow Identity

### Workflow ID
`WF-SOLO-001`

### Workflow Name
Single-Operator Default

### Workflow Version
`v1.0`

### Execution Mode
`workflow_mode`

### Intended Operator Topology
Single operator

### Intended Use
Baseline structured analysis of one evaluated unit using a predefined path under minimal-resource conditions.

This workflow is the canonical baseline route for the single-operator type.

Its purpose is not to define solo work as the only valid Pandora form.
Its purpose is to provide the simplest complete authored route under one-operator conditions.

---

## Recommended Use Cases

This workflow is most appropriate when:
- one researcher is conducting the analysis,
- the case needs a clean end-to-end route,
- a first full structured pass is needed,
- no multi-operator validation is available,
- no specialized distributed execution is required,
- and a final structured output is needed without waiting for richer infrastructure.

It is especially useful for:
- initial benchmark cases,
- solo red-team analysis,
- framework testing,
- example output generation,
- and early-stage public documentation.

---

## Scope Model

### Unit Scope
Default: one full conversation

This workflow is designed primarily for full-session analysis, not isolated single-turn judgment.

### Material Scope
- conversation input
- selected layer outputs
- bounded synthesis outputs generated inside this workflow
- final structured result

### Analytical Scope
Default layer path:
- L1
- L2
- L3
- L4

Optional note:
L5 may later be added in future versions when its role is formally released, but it is not required for the current default workflow.

### Route Scope
Single-pass structured workflow with one final synthesis stage and one final output package.

### Claim Scope
Session-level analytical judgment only.

This workflow may produce strong conclusions about the evaluated session, but should not silently generalize into universal model-level claims.

---

## Workflow Summary

The single-operator default workflow proceeds through the following route:

1. declare scope and workflow metadata  
2. ingest input and prepare analysis context  
3. execute selected layer path in order  
4. preserve structured outputs from each layer  
5. perform bounded synthesis after completion of the selected layer path  
6. produce final structured output  
7. emit route metadata and completion state

This is the canonical minimum complete route for a solo operator.

---

## Stage Path

### Stage 0 — Run Declaration

The run begins with explicit declaration of:
- workflow ID
- workflow version
- run ID
- operator ID
- scope object
- selected evaluated unit
- selected layer path
- intended claim scope

This stage exists to ensure that the run is explicit before execution begins.

### Stage 1 — Input Ingestion

The operator gathers and normalizes the evaluated material.

This includes:
- the conversation or evaluated unit itself
- any required context framing information
- any relevant metadata needed for lawful execution

No interpretation occurs here.
This stage prepares the material for analysis.

### Stage 2 — Layer Execution

The operator runs the selected layer path in order.

Default order:
- L1
- L2
- L3
- L4

The purpose of this order is practical:
- L1 establishes misuse-domain mapping
- L2 evaluates behavioral response
- L3 evaluates the artifact
- L4 evaluates capability or barrier-lowering impact

This sequence may later evolve through other workflows, but it is the baseline authored route for the single-operator default.

Each layer must emit structured outputs and preserve its own scope and reasoning discipline.

### Stage 3 — Output Preservation

After each layer executes, its output is preserved as a structured analytical object.

This stage is not optional in practice, even if it appears implicit.

The workflow depends on preserved outputs so that:
- later synthesis is lawful,
- final judgments remain traceable,
- and the full route can be decomposed afterward.

### Stage 4 — Final Synthesis Checkpoint

Once the defined layer path is complete, the workflow authorizes a final synthesis checkpoint.

At this stage, the operator may run bounded synthesis against the completed upstream outputs.

Because block-specific synthesis docs are not fully frozen yet, this workflow should describe synthesis functionally rather than overcommitting to a finalized block catalogue.

At minimum, the final synthesis stage should support:
- cross-layer interpretation
- contradiction surfacing
- severity or significance formation
- final session-level assessment
- structured reporting state formation

The workflow does not require a fully exploded synthesis block grammar yet.
But it does require a lawful interpretive stage after structured upstream outputs exist.

### Stage 5 — Final Output Construction

The workflow produces one final structured output package.

This should include:
- core layer outputs
- synthesized analytical result
- final session-level judgment
- route metadata
- completion state

### Stage 6 — Run Closure

The workflow ends by logging:
- completion status
- declared scope
- actual stage sequence
- synthesis checkpoint usage
- output artifact references
- any route deviations or execution notes

This ensures the run remains auditable later.

---

## Synthesis Position in This Workflow

This workflow uses a **final synthesis checkpoint** after completion of the selected layer path.

That means:
- synthesis is not run before upstream structured outputs exist
- synthesis is not used as a substitute for layer logic
- synthesis remains downstream of measurement
- final reporting remains downstream of synthesis

At this stage of Pandora’s release, this workflow intentionally uses a conservative synthesis model:
one bounded interpretive stage after the selected layer path is complete.

Future workflows may define:
- interim synthesis checkpoints
- validation-aware synthesis branches
- block-specific synthesis paths
- richer reporting routes

But the single-operator default should stay clean and minimal.

---

## Validation Position in This Workflow

This workflow does **not** require a separate validation stage by default.

That is intentional.

The purpose of this route is to remain complete and useful even when only one disciplined operator is available.

However, the workflow may still support lightweight self-check practices such as:
- verifying structured completeness
- checking that each selected layer was actually executed
- checking that synthesis consumed lawful inputs
- checking that final claims remain inside declared scope

These checks improve quality without turning the baseline route into a multi-pass validation workflow.

Future workflows may formalize:
- second-pass review
- independent reruns
- cross-operator validation
- disagreement handling

But those belong to richer execution models, not the minimal default.

---

## Required Inputs

A valid run of this workflow requires:

- declared run metadata
- one identified evaluated unit
- valid conversation or source material
- a selected layer path
- a scope object
- a defined output target

No synthesis stage may occur unless the required upstream layer outputs exist.

---

## Required Outputs

A valid run of this workflow should emit at minimum:

### A. Run Metadata
- workflow ID
- workflow version
- run ID
- operator ID
- execution mode
- completion state

### B. Scope Object
- unit scope
- material scope
- analytical scope
- route scope
- claim scope

### C. Layer Outputs
Structured outputs for each executed layer in the workflow path.

### D. Final Synthesis Output
A bounded interpretive object derived from the completed upstream outputs.

### E. Final Structured Result
A session-level result suitable for storage, comparison, or downstream reporting.

### F. Route Metadata
- stage sequence
- route signature
- synthesis checkpoint count
- actual completion path

---

## Recommended Output Shape

A clean result from this workflow should probably include sections like:

```text
Run Metadata
Scope Declaration
Executed Layer Path
Layer Outputs
Synthesis Output
Final Assessment
Route Metadata
Completion State
