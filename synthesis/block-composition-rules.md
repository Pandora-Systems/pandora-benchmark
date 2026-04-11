## Block Composition Rules

This document defines how synthesis blocks may be combined inside Pandora without breaking the framework’s core principles.

If `block-model.md` defines what a synthesis block is, and `block-interface.md` defines what a synthesis block must declare, this document defines how blocks may **relate to one another**. Its purpose is to preserve composability without allowing synthesis to collapse into hidden logic, pseudo-layers, uncontrolled dependency chains, or bias-amplifying reasoning stacks.

---

## Core Principle

> Synthesis blocks may be combined freely only when their composition remains explicit, bounded, traceable, and fully separated from evaluation.

Pandora is modular, but not unbounded. Composition is allowed because Pandora is a system of interchangeable analytical components. But composition must occur under strict rules so that flexibility does not degrade clarity, reproducibility, or architectural integrity.

---

## Why Composition Rules Exist

Without composition rules, synthesis quickly becomes fragile.

Blocks may begin to:
- assume undocumented upstream context
- duplicate or override one another
- silently re-enter evaluation
- form circular dependency chains
- amplify directional bias
- suppress ambiguity in favor of narrative neatness

That is exactly the kind of hidden structural collapse Pandora is designed to prevent. Composition rules therefore exist to make multi-block synthesis possible **without sacrificing explicit structure**.

---

## 1. Composition Must Preserve Domain Boundaries

Synthesis blocks must remain inside the synthesis domain.

Composition must not cause blocks to:
- re-score raw behavior
- create new undeclared evaluation dimensions
- replace layer logic
- function as hidden workflows
- mutate upstream measurement into new measurement

The fact that blocks are chained does not give them permission to leave their domain. Layers remain measurement. Workflows remain execution. Synthesis remains interpretation.

---

## 2. Explicit Dependencies Only

A block may only depend on upstream objects that are explicitly declared.

No synthesis block may assume:
- that another block has already run
- that a particular layer output is always present
- that a given interpretation already exists
- that prior conclusions should be inherited automatically

Every dependency must be visible in the block’s interface or in the workflow that invokes it. Hidden dependency is invalid composition.

---

## 3. Forward Flow Only

Composition must preserve a forward-moving dependency structure.

A block may consume:
- layer outputs
- prior synthesis block outputs
- reconciliation or validation objects

It must not create:
- circular dependency loops
- backward influence into already-finalized upstream reasoning
- recursive chains that overwrite earlier interpretive states

This mirrors Pandora’s broader information-flow discipline, where the system remains understandable only when data movement is directional and transparent.

---

## 4. No Retroactive Mutation

A downstream synthesis block must not rewrite the meaning of upstream outputs as if they had originally meant something else.

A block may:
- contextualize prior outputs
- compare them
- challenge their implications
- mark them as contradictory or unstable
- build higher-order conclusions from them

A block must not:
- alter a prior layer score
- replace a previous block result without trace
- erase upstream ambiguity
- silently normalize disagreement away

Composition builds on prior outputs. It does not erase them.

---

## 5. One Analytical Purpose per Block Still Applies

Composition does not weaken the requirement that each block remain single-purpose.

A synthesis chain may be complex, but each block in the chain must still remain bounded.

Good composition:
- contradiction block → severity block → final assessment block

Bad composition:
- one block that detects contradiction, assigns severity, resolves ambiguity, and writes the report

Composition is the mechanism for building sophisticated reasoning from bounded parts. It is not an excuse to make each block bloated.

---

## 6. Interface Compatibility Is Mandatory

Blocks may only be composed when their interfaces are compatible.

This includes compatibility of:
- input type
- scope
- version
- dependency mode
- output contract

A block that consumes conversation-level contradiction objects should not be fed a dataset-level profile object unless it explicitly declares that compatibility. Composition without interface compatibility is structural error, not flexibility.

---

## 7. Scope Must Remain Legible

Composition must preserve scope clarity across blocks.

Blocks may operate at different scopes, but the transition must be explicit.

Examples of valid scope transitions:
- interaction-level block outputs aggregated into conversation-level block
- conversation-level outputs compared in session-level synthesis
- case-level outputs aggregated into dataset-level profile synthesis

Invalid composition occurs when a block silently changes analytical scale without declaring that change. Pandora requires scope consistency and traceable scope transitions.

---

## 8. Composition Must Tolerate Partial Upstream Configurations

Pandora does not require all layers or all blocks to run in every valid analysis.

Therefore, synthesis composition must remain compatible with:
- partial layer subsets
- partial synthesis stacks
- optional reconciliation branches
- minimal and advanced configurations

This means blocks should not be designed as though a full fixed upstream graph always exists. Composition must be resilient to legitimate variation in what is available.

---

## 9. Independent and Dependent Composition Are Both Valid

Block composition supports two main patterns.

### Independent Composition
Multiple blocks operate on the same upstream layer outputs without depending on one another.

Example:
- contradiction detection from L2 + L3
- severity synthesis from L3 + L4
- disagreement analysis from operator bundle

These can all run in parallel if their inputs are satisfied.

### Dependent Composition
A block operates on prior synthesis block outputs.

Example:
- final assessment depends on contradiction object + severity object
- stakeholder summary depends on final assessment object

Both are valid. What matters is that dependency is explicit and traceable.

---

## 10. Branching Is Allowed

A valid synthesis graph may branch.

One upstream object may feed multiple downstream blocks.

Example:
- the same contradiction object may feed:
  - severity synthesis
  - final assessment
  - forensic summary generation

Branching is valid because Pandora is modular and non-prescriptive. What matters is not single-path execution, but explicit structure and preserved lineage.

---

## 11. Merging Is Allowed Only with Defined Logic

Multiple upstream block outputs may converge into one downstream block, but the merge logic must be explicit.

A block that merges outputs must declare:
- what it merges
- under what rules
- how conflict is handled
- what happens when one upstream source is missing
- how ambiguity is preserved

Merging without declared logic is one of the fastest ways to create opaque synthesis. Explicit merge rules are mandatory.

---

## 12. Ambiguity Must Propagate Honestly

Composition must not suppress ambiguity just because later blocks prefer cleaner outputs.

If an upstream block emits:
- indeterminate contradiction
- ambiguous severity basis
- unresolved evaluator disagreement

downstream composition must either:
- preserve that ambiguity
- explicitly transform it under declared rules
- or withhold stronger conclusions if the threshold is not met

A downstream block must not convert ambiguous upstream reasoning into false certainty by default. Pandora already treats ambiguity as a valid signal; synthesis composition must preserve that discipline.

---

## 13. Presence–Absence Symmetry Must Survive Composition

A synthesis graph must not be biased toward positive-condition accumulation.

If an upstream block can emit:
- condition present
- condition absent
- condition indeterminate

downstream composition must be able to honor all three, not just propagate the “present” state.

This is especially important for blocks such as:
- contradiction detection
- disagreement analysis
- severity escalation
- instability assessment

Otherwise, chaining multiple directional blocks creates a bias-amplifying pipeline where the system keeps finding what it was framed to find. Composition must therefore preserve null states and indeterminate states as legitimate downstream inputs. This is critical for preventing bias injection.

---

## 14. Threshold Escalation Must Be Declared

If a downstream block strengthens, escalates, or resolves upstream findings, the conditions for doing so must be explicit.

Examples:
- when contradiction elevates severity
- when disagreement blocks final assessment certainty
- when multiple moderate signals justify a high-level escalation
- when repeated weak signals form a stronger composite judgment

Escalation logic is valid synthesis. Undeclared escalation is hidden bias.

---

## 15. Validation-Aware Composition

Composition must remain compatible with Pandora’s validation model.

This includes the possibility that:
- multiple operators produce divergent upstream results
- repeated passes yield unstable synthesis objects
- disagreement itself becomes a first-class input to later blocks

Blocks that consume validated or reconciled outputs must preserve the distinction between:
- stable agreement
- unstable consensus
- unresolved disagreement
- insufficient basis

This allows synthesis graphs to remain analytically honest in multi-operator systems.

---

## 16. Report Blocks Must Not Distort Upstream Substance

When terminal or reporting blocks are composed downstream, they may transform representation, but they must not silently alter the underlying conclusion.

This means:
- executive summary blocks may condense
- forensic blocks may expand
- comparative blocks may normalize
- stakeholder blocks may reframe

But none of these should rewrite the actual meaning of the upstream final assessment while pretending to merely adjust formatting. Reporting composition must preserve analytical substance.

---

## 17. Composition Must Preserve Traceability

Every composed synthesis result must remain traceable across the full chain.

A downstream output should be traceable to:
- the synthesis blocks that produced it
- the upstream synthesis objects it used
- the original layer outputs beneath those objects
- the relevant evidence segments behind those outputs

Composition without lineage turns a modular system into an opaque narrative generator. Traceability is what keeps Pandora defensible.

---

## 18. Reuse Must Not Introduce Drift

Blocks may be reused across workflows and contexts, but reuse must not silently change block meaning.

A reused block should preserve:
- purpose
- input contract
- output contract
- dependency logic
- prohibited actions

If a reused block needs materially different logic in a new context, that should become a new version or new block, not an implicit reinterpretation of the existing one. This is especially important for backward compatibility and versioned reproducibility.

---

## 19. Invalid Composition Patterns

The following are invalid composition patterns.

### Circular Synthesis
A block depends on outputs that eventually depend on itself.

### Hidden Merge
Two upstream objects are combined without declared merge logic.

### Retroactive Rewrite
A downstream block silently replaces upstream meaning.

### Directional Bias Chain
Multiple blocks are framed only to detect presence and cannot preserve absence or indeterminacy.

### Pseudo-Layer Injection
A downstream block begins scoring new raw phenomena instead of interpreting structured outputs.

### Undeclared Scope Shift
A block consumes outputs at one scale and emits conclusions at another without declaring the transition.

These patterns are not edge cases. They are exactly the structural failure modes this document is designed to prevent.

---

## 20. Minimal Composition Template

A simple way to think about valid block composition is:

```text
Upstream Structured Outputs
    ↓
Eligible Synthesis Block(s)
    ↓
Structured Intermediate Synthesis Object(s)
    ↓
Dependent Synthesis Block(s)
    ↓
Terminal Assessment / Reporting Block(s)
```

This is not the only valid pattern, but it illustrates the core rule:
**composition builds forward through explicit, structured, bounded objects.**

---

## Summary

Block composition in Pandora is allowed, encouraged, and necessary.

But it is valid only when it remains:
- explicit
- forward-moving
- traceable
- scope-aware
- interface-compatible
- ambiguity-preserving
- free from hidden evaluation logic

These rules are what allow synthesis to scale in sophistication without collapsing into opaque reasoning stacks.

---

## Final Principle

Pandora permits complex synthesis.

It does **not** permit uncontrolled synthesis.

A synthesis graph is valid only when every block relationship is explicit, bounded, and consistent with the framework’s separation between measurement and interpretation.
