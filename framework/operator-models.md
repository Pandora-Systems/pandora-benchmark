# Operator Models

## Purpose

This document defines how evaluation authority can be arranged within Pandora.

Operator models do not define what Pandora measures, how workflows execute, how automation is implemented, or how synthesis reconciles results.  
They define only how evaluation responsibility is distributed across one or more operators.

An operator may be:

- a human evaluator
- an AI evaluator
- a hybrid human-AI arrangement

The identity of the operator is secondary.  
The core question is how analytical authority is structured.

---

## Core Principle

> Pandora is independent of any single judging configuration.

Operator models exist so the framework can remain analytically stable across different authority arrangements without changing its underlying logic.

---

## What Operator Models Define

Operator models define:

- how many evaluators are involved
- whether they work independently or in fragments
- whether authority is centralized or distributed
- where replication becomes possible
- how evaluation ownership is arranged

Operator models do **not** define:

- layer logic
- workflow sequencing
- automation architecture
- resource allocation strategy
- consensus resolution rules
- synthesis logic

Those belong elsewhere.

---

## Why Operator Models Matter

A framework can be conceptually sound and still become unstable if evaluation authority is not structured clearly.

Pandora needs operator models because the same framework may be run by:

- one solo researcher
- several independent judges
- distributed specialists
- hybrid human-agent systems

Without explicit operator models, these arrangements get treated as informal variations of the same thing.  
That weakens analytical comparability.

Operator models make those authority structures explicit.

---

## Canonical Operator Patterns

Pandora supports three core operator patterns.

### 1. Single Operator

One operator performs the evaluation.

This model is best suited to:

- rapid analysis
- exploratory work
- prototyping
- low-complexity deployment

Key property:

- centralized evaluation authority

This is the simplest valid operator model.  
It does not provide replication by itself, but it can still produce a coherent Pandora run if analytical boundaries are preserved.

---

### 2. Independent Multi-Operator

Multiple operators evaluate the same material independently.

Their outputs are compared only after individual evaluation has been completed.

This model is best suited to:

- validation
- bias reduction
- reliability strengthening
- formal benchmarking

Key property:

- independent replication of judgment

The value of this model comes from independence.  
If evaluators influence each other during scoring, agreement becomes less informative.

---

### 3. Fragmented / Distributed Evaluation

Multiple operators evaluate different slices of the analysis space.

Each operator may receive:

- a subset of sessions
- a subset of layers
- a subset of materials
- a subset of benchmarking tasks

This model is best suited to:

- large-scale evaluation
- distributed quality assurance
- specialist review structures
- scalable benchmarking systems

Key property:

- distributed authority across segmented analytical ownership

This model scales well, but it creates stronger coordination requirements around output compatibility and later synthesis.

---

## Composability

These patterns are not mutually exclusive.

Examples include:

- single-operator evaluation followed by independent validation
- distributed layer ownership followed by multi-operator review
- agent-first evaluation followed by human audit

The important point is that composability does not erase structure.  
Each operator model used in a run should still be identifiable.

---

## Operator Independence

Where Pandora depends on more than one evaluator, independence is a first-order concern.

Operators should not:

- coordinate during scoring
- share provisional judgments before independent completion
- inherit another evaluator’s conclusion as a starting point
- converge socially before comparison has meaning

Without independence, agreement becomes less analytically valuable.

This does not mean operators can never be compared or reconciled.  
It means comparison must happen **after** independent evaluation, not during it.

---

## Distributed Ownership

Some Pandora runs may assign different analytical responsibilities to different operators.

Examples include:

- one operator owning one layer
- one operator validating another operator’s output
- one operator producing a first-pass run and another reviewing it

This is valid as long as role boundaries are explicit.

The key question is not whether authority is shared.  
The key question is whether the structure of ownership remains visible and traceable.

---

## Role of Disagreement

Disagreement between operators is a legitimate analytical signal.

It may indicate:

- ambiguity in the material
- unstable behavior in the target system
- weak test definitions
- borderline cases
- insufficiently constrained criteria

This document does not define how disagreement is resolved.  
That belongs to synthesis and related downstream logic.

What operator models define is simpler:

- disagreement can exist
- disagreement can be structurally meaningful
- disagreement must remain visible rather than being collapsed prematurely

---

## Human, AI, and Hybrid Operators

Operator models are compatible with human, AI, and hybrid evaluators.

What matters is not the substrate of the operator.  
What matters is whether the operator can preserve:

- boundary discipline
- structured output
- independence where required
- role clarity
- traceable evaluation ownership

A human operator can violate these rules.  
An AI operator can also violate them.  
The model therefore remains topological, not identity-based.

---

## Boundary with Other Framework Domains

Operator models are distinct from the rest of the framework.

### Layers

Layers define what is being measured.

### Workflows

Workflows define how execution proceeds.

### Resource Scaling

Resource scaling defines how the framework expands across different levels of available capacity.

### Automation Readiness

Automation readiness defines what makes Pandora machine-operable.

### Synthesis

Synthesis defines how multiple outputs are interpreted, reconciled, or turned into conclusions.

Operator models define only how evaluation authority is arranged.

---

## Common Failure Modes

Operator models matter most when authority structure becomes unclear.

### 1. Hidden coordination

Multiple evaluators appear independent but influence each other informally.

### 2. Role collapse

One operator silently performs multiple roles without keeping outputs distinct.

### 3. Ambiguous ownership

It becomes unclear who evaluated what, or under which authority structure.

### 4. Premature reconciliation

Differences between evaluators are flattened before they can be interpreted properly.

### 5. Structural confusion

Operator topology is mistaken for workflow logic, automation design, or resource strategy.

These are operator-model failures even when the broader framework remains conceptually sound.

---

## Summary

Operator models make Pandora:

- topology-flexible
- validation-capable
- compatible with centralized and distributed judgment
- compatible with human, AI, and hybrid evaluation

They ensure that Pandora can operate under different authority arrangements without changing its analytical foundations.

---

## Final Principle

Pandora is not defined by how many operators are involved.

It is defined by whether evaluation authority is arranged clearly enough to preserve independence, traceability, and analytical integrity.