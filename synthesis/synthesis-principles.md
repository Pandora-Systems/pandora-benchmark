## Synthesis Principles

This document defines the principles that govern how synthesis operates within Pandora.

If the evaluation principles define how Pandora measures, the synthesis principles define how Pandora **constructs meaning from measurement**. They exist to ensure that synthesis remains disciplined, modular, traceable, and compatible with the architecture of the framework as a whole. 

These principles apply to all core synthesis logic unless explicitly overridden by a more specific synthesis document.

---

## Core Objective

The objective of synthesis is not to re-evaluate the conversation from scratch.

It is to:

> **interpret structured analytical signals and transform them into coherent, defensible intelligence**

Synthesis does not replace evaluation. It operates on outputs already produced by valid analytical components and determines what those outputs mean together.

---

## 1. Separation from Evaluation

Synthesis must remain distinct from evaluation.

Evaluation:
- measures
- scores
- labels
- classifies
- records

Synthesis:
- interprets
- combines
- reconciles
- infers
- concludes

This is not a stylistic preference. It is one of Pandora’s core structural boundaries. If synthesis begins re-measuring raw dimensions, inventing new tests, or assigning undeclared layer scores, it collapses back into evaluation and contaminates the framework.

---

## 2. Operate on Structured Outputs

Core synthesis must operate on structured upstream outputs.

Its valid inputs are things such as:
- scores
- labels
- classifications
- reasoning fields
- structured observations
- validated outputs from prior synthesis blocks

This keeps synthesis compatible with Pandora’s architecture, automation model, and extensibility discipline. Interpretation that depends on undocumented or implicit inputs is not valid synthesis.

---

## 3. Post-Measurement Discipline

Canonical synthesis is a **post-measurement** activity.

Within the Pandora lifecycle, synthesis occurs after layer execution and intermediate output generation. This means core synthesis does not begin from raw conversational impression. It begins from structured signals already produced by the system.

Objects that operate before formal measurement may still exist elsewhere in Pandora, but they do not belong to core synthesis if they violate this post-measurement boundary.

---

## 4. Single-Purpose Boundedness

Every synthesis block must have one bounded analytical purpose.

A valid synthesis block should do one thing clearly:
- detect contradictions
- synthesize severity
- normalize comparative outputs
- reframe conclusions for a stakeholder
- resolve evaluator disagreement

It should not try to do all of these at once. The same atomic discipline that protects evaluation also protects synthesis from becoming vague, bloated, or un-auditable.

---

## 5. No Hidden Logic

All synthesis logic must be explicit.

A synthesis block must not rely on:
- hidden heuristics
- undocumented escalation rules
- silent weighting assumptions
- implicit operator intuition
- opaque transformations of meaning

If a rule affects how a conclusion is formed, that rule must be documented. If it cannot be explained clearly, it should not be part of core synthesis. This principle is essential for reproducibility, trust, and defensibility.

---

## 6. Do Not Mutate Upstream Measurement

Synthesis may interpret upstream outputs. It must not rewrite them.

A synthesis process may say:
- these signals are contradictory
- these signals jointly imply elevated severity
- these judgments are unstable across operators

It may not say:
- this layer score should have been different
- this prior output is replaced retroactively
- this signal is discarded without trace

Layer outputs remain layer outputs. Synthesis may build on them, contextualize them, or challenge their implications, but it must preserve their existence and traceability.

---

## 7. Traceability of Conclusions

Every synthesis conclusion must remain traceable to its source signals.

A conclusion should be explainable in terms of:
- which layer outputs informed it
- which synthesis block produced it
- which upstream evidence segments ultimately support it
- what transformation or interpretive logic was applied

This is essential for auditing, debugging, comparison, and trust. A synthesis result that cannot be traced back to its upstream signals is analytically weak, no matter how persuasive it sounds.

---

## 8. Contradiction Is a First-Class Signal

Synthesis must treat contradiction as information, not as noise to be smoothed away.

Contradictions such as:
- refusal language with actual compliance
- low-confidence framing with highly precise output
- cautious tone with operational enablement
- evaluator disagreement under identical input

are often among the most analytically valuable findings in Pandora. Synthesis should surface and characterize contradiction, not suppress it in the name of neatness.

---

## 9. Ambiguity Remains Valid

Not every case resolves cleanly.

Synthesis must tolerate:
- ambiguous signals
- borderline severity
- evaluator divergence
- unresolved tension between outputs

When ambiguity exists, synthesis should represent it explicitly rather than force artificial precision. Pandora already treats ambiguity as a valid signal in evaluation; synthesis should preserve that discipline at the interpretive level.

---

## 10. Presence–Absence Symmetry

Synthesis must not be framed as one-directional detection.

A valid synthesis block must be able to conclude that its target condition is:

- present
- absent
- indeterminate

This prevents synthesis from becoming a bias injector.

For example, a contradiction block must not be designed as a mechanism that searches only for contradiction. It must evaluate whether contradiction is actually supported by the available structured signals, whether non-contradiction is better supported, or whether the evidence is insufficient to justify either conclusion.

This principle applies across the synthesis domain.

A synthesis block should not ask:

> “What contradiction exists here?”

It should ask:

> “Is contradiction present, absent, or indeterminate under the declared criteria?”

This preserves analytical neutrality, supports ambiguity tolerance, and reduces the risk of manufacturing patterns that are not actually justified by the evidence.

Synthesis must therefore remain symmetric with respect to its target conditions:
- evidence may support presence
- evidence may support absence
- evidence may remain inconclusive

All three are valid analytical outcomes.

---

## 11. Composition Without Collapse

Synthesis must be modular and composable.

Pandora is not a fixed pipeline. It is a modular system of interoperable components. Synthesis therefore should be composed from reusable blocks rather than implemented as one monolithic reasoning phase. Each block should have:
- defined inputs
- defined outputs
- clear purpose
- explicit dependencies
- clear prohibitions

Composition is allowed. Architectural blur is not.

---

## 12. Workflow-Compatible, Not Workflow-Dependent

Synthesis may be orchestrated differently by different workflows, but synthesis principles must remain stable across workflows.

A workflow may choose:
- which synthesis blocks run
- in what order they run
- when they are triggered
- whether they are repeated or branched

But workflows do not redefine what valid synthesis is. This preserves Pandora’s architecture, where workflows define execution paths and synthesis defines reasoning logic.

---

## 13. Valid with Partial Layer Configurations

Synthesis must remain valid when operating on any legitimate upstream layer subset.

Pandora does not require the full layer stack for every analysis. Synthesis therefore cannot assume that all layers are always present. It must be able to operate on:
- one layer
- selected subsets
- full stacks
- repeated or validated variants of the same stack

This is one of the reasons synthesis should be block-based rather than hard-coded to one canonical bundle of upstream signals.

---

## 14. Validation-Aware Reasoning

Synthesis is central to Pandora’s validation logic.

When multiple operators or multiple passes exist, synthesis is responsible for interpreting:
- agreement
- disagreement
- instability
- conflict between signals
- cross-layer inconsistency

Validation is not only about whether outputs match. It is about understanding why they differ and what those differences imply. Synthesis must therefore be able to operate not only on layer signals, but also on patterns across evaluators, runs, or cases.

---

## 15. Reporting Must Preserve Substance

Some synthesis blocks transform conclusions into different report formats. That transformation must preserve analytical substance.

A stakeholder-facing summary may be:
- shorter
- more technical
- more executive
- more forensic
- more comparative

But it must not quietly alter the underlying judgment while pretending to only change the format. Reframing is allowed. Substantive distortion is not.

---

## 16. Scale Awareness

Synthesis may operate at more than one analytical scale.

Examples include:
- interaction-level synthesis
- conversation-level synthesis
- session-level synthesis
- dataset-level synthesis across many cases
- model-profile synthesis across repeated studies

The principles remain the same at all scales:
- structured inputs
- explicit logic
- traceable derivation
- preserved measurement boundary

As Pandora grows, synthesis must scale in sophistication without abandoning this discipline.

---

## 17. Automation Compatibility

Synthesis must remain automation-compatible by design.

This requires:
- explicit interfaces
- schema-compatible outputs
- clear input contracts
- bounded block purposes
- minimal ambiguity in reasoning rules

Pandora is designed to be machine-operable by structure. That applies to synthesis just as much as it applies to layers. A synthesis model that cannot be operationalized consistently is not yet mature Pandora logic.

---

## 18. Human Judgment Still Matters

Automation compatibility does not mean human judgment becomes irrelevant.

Pandora explicitly treats human oversight as valuable, especially where:
- edge cases appear
- disagreements are meaningful
- ambiguity persists
- severity judgments require careful interpretation

Synthesis should be designed so that humans can inspect, validate, and challenge it when needed, even if parts of it are automated.

---

## 19. Extensibility Under Discipline

Synthesis is one of Pandora’s main extensibility surfaces.

Pandora explicitly allows extension through:
- new interpretation rules
- new aggregation strategies
- new reporting styles
- new consensus logic
- new severity models

But every extension must:
- preserve separation from evaluation
- operate on structured outputs
- follow explicit interfaces
- avoid hidden dependencies
- coexist without destabilizing the framework

This is controlled evolution, not conceptual drift.

---

## 20. What Core Synthesis Excludes

Core synthesis excludes any object that violates synthesis block principles.

That means objects such as:
- raw first-impression summaries
- pre-analysis intuition controls
- annotation helpers
- key-point markers
- turn counters
- pre-measurement control objects

may be useful elsewhere in Pandora, but they do not belong inside core synthesis if they are not post-measurement, structured-output-driven interpretive blocks. This keeps synthesis clean, canonical, and conflict-free.

---

## 21. Final Principle

> Synthesis exists to construct meaning from structured analytical signals without re-entering the measurement domain.

If evaluation becomes interpretive too early, Pandora loses signal purity.  
If synthesis becomes vague or unbounded, Pandora loses rigor.

These principles ensure that synthesis remains:
- modular
- explicit
- traceable
- extensible
- defensible

and worthy of acting as Pandora’s reasoning domain.
