# Evaluation Principles

## Purpose

This document defines the **core principles that govern evaluation across Pandora**.

It specifies the rules that make analytical outputs clear, comparable, and reproducible across layers, operators, workflows, and implementations.

Evaluation principles define **how Pandora measures**.
They do not define layer content, synthesis logic, workflow structure, or implementation mechanics.

---

## Core Principle

> Pandora evaluation must produce structured analytical signals that are atomic, observable, and interpretable.

A valid evaluation is not based on impression, intuition, or undocumented judgment.
It is based on explicit tests, clear scoring rules, and reasoning tied to observable evidence.

---

## Governing Principles

### 1. Atomic Testing

Evaluation is composed of **atomic tests**.

Each test must:

- measure one analytical dimension
- produce one discrete result
- remain interpretable on its own

Atomic testing prevents blended judgments and preserves signal clarity.

---

### 2. Dimension Isolation

Each test evaluates **one dimension only**.

Related dimensions may coexist within the same layer, but they must not be merged into a single test.

Dimension isolation preserves nuance and reduces analytical contamination.

---

### 3. Observation Over Interpretation

Evaluation records **what is observable in the input or output**.

It does not infer hidden intention, speculative motive, or final significance beyond the scope of the test.

Interpretation belongs downstream.
Measurement belongs here.

---

### 4. Structured Outputs

Each evaluation must produce structured output.

Typical output elements include:

- score or label
- optional classification
- concise reasoning

Structured outputs make evaluation traceable, machine-readable, and reusable.

---

### 5. Clear Scoring Systems

Every test must define a scoring system that is:

- explicit
- stable
- interpretable

Scoring may be numerical, categorical, binary, or label-based, but it must be unambiguous and consistently applied.

---

### 6. Evidence-Tied Reasoning

Each test should include brief reasoning tied directly to observed evidence.

Reasoning should:

- justify the assigned score or label
- remain concise
- avoid speculation

Reasoning exists for traceability, not for narrative expansion.

---

### 7. Scope Consistency

Evaluation must respect the defined analytical scope.

That scope may be:

- interaction-level
- segment-level
- conversation-level

A single evaluation run must not mix scopes without explicit design.

---

### 8. Layer Independence

Pandora layers are independently evaluable.

A layer must be able to apply its own tests and produce valid outputs without depending on conclusions from another layer.

Sequential context may exist in some workflows, but independent evaluability remains the baseline requirement.

---

### 9. Completeness of Application

Defined tests should be applied consistently within a run unless they are explicitly excluded by design.

Selective omission weakens comparability and reduces dataset integrity.

---

### 10. Analytical Neutrality

Pandora evaluation is analytically neutral.

It records:

- presence
- absence
- degree

It does not assign moral judgment, enforcement status, or final severity inside the evaluation step itself.

---

### 11. Reproducibility

Evaluation must be designed so that different operators or repeated runs can produce comparable results under the same rules.

This requires:

- clear test definitions
- explicit scoring logic
- structured outputs
- minimal hidden assumptions

---

### 12. Explicit Logic

Evaluation logic must be documented and accessible.

No test should rely on hidden heuristics, unstated assumptions, or undocumented shortcuts.

Transparency is a condition of validity.

---

### 13. Separation from Synthesis

Evaluation and synthesis are separate functions.

Evaluation:

- measures
- scores
- labels
- records

Synthesis:

- combines
- interprets
- correlates
- concludes

Evaluation produces signals.
It does not produce final judgment.

---

## Minimum Valid Output Pattern

A valid Pandora evaluation output should include at least:

- **Test Name**
- **Score or Label**
- **Reasoning**

This pattern provides the minimum structure required for interpretation, comparison, and validation.

---

## What These Principles Enable

These principles enable:

- comparability across analyses
- consistency across operators
- compatibility with automation
- reliable validation workflows
- structured dataset generation

They make Pandora evaluation usable as a measurement system rather than a loose review process.

---

## Summary

Pandora evaluation is defined by a small set of non-optional properties.
It must be:

- atomic
- observable
- structured
- traceable
- reproducible
- separated from synthesis

These principles are the rules that keep Pandora analytically coherent across all layers and deployment conditions.

---

## Final Principle

Pandora is only as strong as the quality of its evaluation discipline.

If evaluation loses clarity, everything built on top of it loses reliability.