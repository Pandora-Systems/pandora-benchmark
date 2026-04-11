## Synthesis Overview

Synthesis is the **reasoning domain** of Pandora.

It exists to transform structured analytical signals into coherent intelligence. While layers measure distinct dimensions of model behavior, synthesis is where those signals are interpreted, correlated, reconciled, and turned into conclusions. In Pandora’s architecture, this makes synthesis the third core domain alongside structure (`framework/`) and execution (`workflows/`).

Pandora is not merely a layered benchmark. It is a full analytical system composed of:
- **layers** for measurement
- **workflows** for execution
- **synthesis** for reasoning

Synthesis is what turns Pandora from a system that produces scores into a system that produces judgments, insights, and reportable intelligence.

---

## Core Purpose

The purpose of synthesis is simple:

> **to construct meaning from structured outputs without contaminating measurement**

Layers produce isolated signals:
- scores
- labels
- classifications
- reasoning fields
- structured observations

Synthesis takes those signals and determines what they mean together. It identifies patterns that are not visible inside any single layer, resolves tension between signals, and produces coherent analytical conclusions.

This includes functions such as:
- cross-layer interpretation
- contradiction detection
- severity synthesis
- disagreement analysis
- final assessment formation
- report protocol selection and output framing

---

## Position in the Pandora Lifecycle

Within the canonical Pandora lifecycle, synthesis occurs **after** layer execution and intermediate output generation, and **before** final output generation. This position is not incidental. It is what preserves the boundary between measurement and interpretation.

The lifecycle remains:

1. Input Ingestion  
2. Context Framing  
3. Layer Execution  
4. Intermediate Output Generation  
5. Synthesis  
6. Final Output Generation

This means synthesis does **not** define what the model did in the conversation. The layers do that. Synthesis defines what the measured signals mean once they are considered together.

---

## Why Synthesis Exists

Without synthesis, Pandora would remain a structured evaluation system, but not yet a complete analytical intelligence system.

A layer can tell you:
- that the model was cooperative
- that the output was highly detailed
- that the output was operationally usable

But no single layer should conclude:
- that the conversation represents critical adversarial capability
- that the model contradicted its own stated refusal posture
- that the case should be escalated under a specific reporting protocol

Those are synthesis-level judgments. They emerge from **relationships between signals**, not from one signal alone.

This is why synthesis matters:
- it enables composite intelligence
- it makes contradiction visible
- it supports severity escalation logic
- it turns signal collections into defensible conclusions

---

## Boundary: Layers vs Synthesis

Pandora depends on a strict boundary between layers and synthesis.

### Layers
Layers:
- measure
- score
- classify
- describe

They must remain atomic, structured, and dimension-specific. They must not perform cross-layer reasoning, final severity assignment, or conclusion generation.

### Synthesis
Synthesis:
- interprets
- combines
- infers
- concludes

It operates on structured outputs from layers and produces higher-order intelligence from them.

This separation is one of Pandora’s core architectural protections. Without it, measurement and interpretation collapse into one another, signal contamination increases, and the framework becomes harder to validate, automate, and defend.

---

## Synthesis Is a Domain, Not a Layer

Synthesis is **not** another layer.

A layer captures one analytical dimension. Synthesis operates across already-captured dimensions. Turning synthesis into an additional pseudo-layer would blur Pandora’s architecture and undermine the logic of the lifecycle.

Pandora therefore treats synthesis as a **reasoning domain** with its own internal logic, constraints, and protocols.

---

## From Monolithic Synthesis to Synthesis Blocks

Synthesis should not remain one large, monolithic reasoning step.

Instead, Pandora now treats synthesis as a modular domain composed of **synthesis blocks**: bounded reasoning units that each serve a single interpretive purpose. This makes synthesis structurally consistent with the rest of the framework’s modular design.

A synthesis block is not a freeform “think about everything” phase. It is a clearly defined reasoning unit with:
- a purpose
- an input contract
- an output contract
- explicit boundaries
- explicit prohibitions

This makes synthesis:
- composable
- reusable
- auditable
- automation-ready
- extensible without redesign

---

## What Synthesis Blocks Do

Synthesis blocks exist to perform bounded interpretive work.

Examples of valid synthesis functions include:
- detecting contradictions between layer signals
- correlating behavior and output properties
- synthesizing severity from multiple upstream signals
- generating consensus judgments across multiple evaluators
- reframing established conclusions for different stakeholders
- assembling final analytical assessments

What matters is not the subject matter alone, but the role:
- they must remain interpretive
- they must operate on structured outputs
- they must not silently re-enter the measurement domain

---

## What Synthesis Blocks Must Not Do

A synthesis block must not become:
- a hidden extra layer
- an undeclared test system
- a scoring mechanism for new raw dimensions
- a place where undocumented heuristics live
- a mechanism for rewriting earlier layer outputs

If a component re-measures raw behavior, invents new scoring logic, or mutates prior structured outputs, it is no longer valid synthesis. It has crossed back into evaluation or into hidden logic, both of which violate Pandora’s design principles.

---

## What Is Explicitly Outside Core Synthesis

Not every useful analytical object belongs in synthesis.

Pandora may later support optional upstream objects such as:
- pre-analysis intuition objects
- annotation helpers
- turn counters
- key-point markers
- pre-measurement controls

These may be useful for workflow enrichment or benchmarking controls, but they do **not** belong inside canonical synthesis if they violate synthesis block principles. Synthesis remains reserved for structured post-measurement reasoning. This keeps the domain clean and preserves Pandora’s first principles.

---

## Canonical Functions of the Synthesis Domain

At the highest level, Pandora synthesis is expected to cover six major functions.

### 1. Cross-Layer Interpretation
Synthesis identifies higher-order meaning that emerges only when multiple layer outputs are considered together.

### 2. Contradiction Handling
Synthesis detects conflicts such as:
- refusal language with actual compliance
- safe tone with unsafe output
- weak confidence language with highly precise instructions

### 3. Severity Logic
Synthesis determines when a case moves from notable to serious to critical, based on defined interpretive rules rather than isolated signals.

### 4. Composite Assessment
Synthesis constructs integrated judgments from selected signal combinations.

### 5. Resolution of Multi-Operator Differences
When multiple evaluators disagree, synthesis interprets disagreement, resolves it where appropriate, or preserves it as a meaningful signal.

### 6. Reporting and Reframing
Synthesis determines how the same analytical substance can be expressed as:
- technical report
- executive summary
- forensic breakdown
- comparative benchmark output
- adversarial capability exposure report

---

## Synthesis and Validation

Synthesis is also central to Pandora’s validation logic.

Validation does not merely depend on agreement rates. It depends on understanding:
- where signals align
- where they diverge
- why inconsistency exists
- whether disagreement is noise, ambiguity, instability, or a meaningful edge case

For that reason, synthesis is responsible not only for combining outputs, but also for interpreting disagreement and contradiction as analytical signals. This is especially important in multi-operator and fragmented evaluation models.

---

## Synthesis and Automation

Pandora is designed to be automation-ready, and synthesis is part of that design.

Because synthesis operates on structured outputs and defined interfaces, it can be implemented:
- manually
- agentically
- semi-automatically
- in hybrid human–AI systems

This is only possible if synthesis remains explicit, modular, and bounded. A monolithic or implicit synthesis model would be far harder to automate consistently.

---

## Synthesis and Extensibility

Synthesis is one of Pandora’s core extensibility surfaces.

Pandora explicitly allows synthesis to evolve through:
- new interpretation rules
- new aggregation strategies
- new correlation logic
- new severity models
- new reporting styles

But that extensibility is disciplined, not open-ended. New synthesis logic must:
- operate on structured outputs
- preserve separation from evaluation
- avoid hidden dependencies
- remain compatible with the architecture and lifecycle

This means synthesis can grow in sophistication without collapsing back into ambiguity.

---

## The Internal Shape of `synthesis/`

At this point, the synthesis domain is best understood as having:

### Foundational documents
- overview
- principles
- block model
- block interface
- block composition rules

### Core reasoning blocks
- contradiction detection
- correlation logic
- severity synthesis
- final assessment logic

### Reconciliation blocks
- consensus protocols
- disagreement analysis

### Reporting blocks
- reporting protocols
- unified template
- stakeholder-oriented reframing formats

This gives `synthesis/` a clean internal structure: foundational rules first, block logic second, reporting logic third.

---

## Summary

Synthesis is the reasoning domain of Pandora.

It:
- operates after measurement
- interprets structured outputs
- remains separate from layers
- is modular rather than monolithic
- is composed of bounded synthesis blocks
- supports contradiction handling, severity logic, composite assessment, consensus interpretation, and reporting
- must remain explicit, structured, and automation-compatible

Pandora’s layers generate signals.  
Synthesis turns those signals into intelligence.

---

## Final Principle

Pandora synthesis is not a loose reporting phase.

It is a **modular reasoning system** that transforms structured analytical outputs into defensible, traceable, and reusable intelligence.
