# `workflows/` — Document Map

## Purpose

`workflows/` defines the execution routes of Pandora.

If `framework/` defines what Pandora is, and `synthesis/` defines how Pandora forms higher-order conclusions, `workflows/` defines how an analysis actually runs in practice: what happens, in what order, at what scope, and with which reporting or validation handoffs.

A workflow is not the same thing as the canonical analysis lifecycle.

The lifecycle defines the structural stages that all Pandora analyses follow at a system level. A workflow defines one valid route through that lifecycle under specific operational conditions. This allows Pandora to support multiple execution patterns without changing its underlying architecture.

At this stage, the `workflows/` folder focuses on the core execution doctrine needed for a solo researcher or early operator to use Pandora in a structurally valid way. More specialized workflow documents—especially those tied to finalized synthesis blocks, richer operator topologies, or advanced automation patterns—can be added later without changing the role of the folder.

---

## 1. `workflow-principles.md`

Defines the governing rules for all Pandora workflows. This document explains what workflows are allowed to do, what they are not allowed to do, how they preserve framework boundaries, and how they remain compatible with synthesis, validation, and future automation.

---

## 2. `scope-and-trigger-model.md`

Defines how workflows express execution scope and route-level triggers. This includes partial vs full analysis, selected vs full layer stacks, single-pass vs multi-pass execution, and the conditions that trigger synthesis, validation, or reporting.

---

## 3. `single-operator-default.md`

Defines the simplest complete Pandora workflow. One operator evaluates selected material, applies the chosen layer path, performs bounded synthesis at the appropriate stage, and produces a structured output. This is the baseline deployment model for the initial public framework.

---

## 4. `partial-analysis-patterns.md`

Defines valid partial workflows. This document explains how Pandora can be used selectively—such as through reduced layer paths, quick triage routes, or constrained analysis modes—without losing analytical integrity or collapsing architectural boundaries.

---

## 5. `workflow-template.md`

Defines the reusable structure for future workflow specifications. Every new workflow should be describable through a shared template so the execution layer remains modular, auditable, and extensible as Pandora grows.

## 6. `single-vs-multiplayer.md`

Document explaining the practical differences between single and multiplayer operator modes in Pandora, including core principles, workflow distinctions, and their implications for downstream processing, validation, and provenance.
---

## Core Idea

## Workflow Classification

Pandora workflows should be understood along two dimensions:

### Category
The analytical purpose of the route.

Examples:
- baseline
- partial
- validation
- consensus
- distributed
- hybrid
- exploratory

### Type
The operator topology through which the route is executed.

Examples:
- single-operator
- hybrid human-agent
- multi-operator
- distributed-layer
- freestyle-compatible

This distinction matters.

A workflow is not defined only by what stages it runs.
It is also defined by who or what runs them.

Operator models live at the framework level as evaluation topologies.
Workflows turn those topologies into concrete execution routes.

So:
- **category** tells you what the route is trying to do
- **type** tells you under which operator model it runs

A workflow is a route, not a reasoning engine.

It decides:
- what runs,
- in what order,
- at what scope,
- and when outputs move forward.

It does not reinterpret layer findings, replace synthesis logic, or smuggle evaluation into routing.

That separation is one of the reasons Pandora can remain coherent across different execution realities, from a single researcher using a basic route to more advanced future configurations involving richer validation, distributed execution, or agent-assisted analysis.

---

## Release Logic

The initial `workflows/` release is intentionally narrow.

It is designed to provide:
- a clear execution boundary,
- a valid baseline workflow,
- a disciplined model for partial use,
- and a stable template for future growth.

Documents that depend on finalized synthesis block orchestration, richer multi-operator resolution logic, or more mature automation patterns are better added after real block experimentation and applied workflow testing. This keeps the folder sharp, truthful, and aligned with the current maturity of the framework.

---

## Summary

`workflows/` is Pandora’s execution domain.

It exists to define how valid analyses move through the system without confusing:
- measurement with interpretation,
- structure with route,
- or reporting with truth.

The first release of this folder focuses on the minimum workflow doctrine needed to make Pandora usable, publishable, and structurally coherent in practice.
