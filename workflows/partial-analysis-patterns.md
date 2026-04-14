# Partial Analysis Patterns

## Purpose

This document defines valid partial execution patterns in Pandora.

Pandora is modular by design.
That means not every valid run must execute the full available analytical path.

A route may:
- analyze only selected layers,
- focus on one specific analytical dimension,
- perform a quick triage pass,
- isolate one kind of signal,
- or generate a constrained intermediate result for later deeper analysis.

This flexibility is a strength.

But partial use becomes weak very quickly if it is not disciplined.

A partial route must remain:
- explicit in scope,
- lawful in dependency order,
- honest about its claim limits,
- and structurally distinct from a full-stack execution.

This document exists to define those rules and to provide a small set of valid baseline partial patterns.

---

## Core Principle

> A partial route is valid only when its reduced scope is explicit and its reduced claims remain truthful.

Pandora does not require every run to be full-stack.

But it does require every run to remain honest about:
- what was actually executed,
- what was intentionally omitted,
- and what kind of conclusion the route is therefore allowed to produce.

A partial route is not a lesser version of Pandora.
It is a narrower version of Pandora.

That narrowing must be visible.

---

## Why Partial Routes Matter

Partial routes are necessary because real analysis does not always require the same depth.

A solo researcher may need:
- a rapid first-pass misuse classification,
- a behavior-only review,
- an artifact-only inspection,
- a capability-only assessment,
- or a narrow route that prepares inputs for later deeper analysis.

Partial routes are especially valuable when:
- time is limited,
- evidence is still exploratory,
- one dimension matters more than others,
- synthesis blocks are not fully standardized yet,
- or a workflow is being used as a pre-analysis stage rather than a terminal route.

Pandora should support this explicitly rather than forcing users to improvise around a full route every time.

---

## Partial Analysis Is Not Incomplete Analysis by Default

A partial route is not automatically invalid because it is narrow.

It becomes invalid only when:
- its scope is hidden,
- its omissions are ignored,
- or its outputs are treated as if they came from a broader route than actually ran.

A narrow route may still be:
- precise,
- useful,
- traceable,
- benchmark-relevant,
- and operationally strong,

as long as it does not overclaim.

This distinction matters.

The failure is not partiality.
The failure is misrepresentation.

---

## Partial Route Categories

This document is primarily a **category document**, not a full topology matrix.

Its purpose is to define valid **partial workflow categories**:
- single-layer routes
- narrow multi-layer routes
- triage routes
- preparation routes
- exploratory routes

Most examples in this document are naturally compatible with:
- single-operator execution
- and freestyle-compatible use

But partiality is not tied to one operator topology only.

A partial workflow may later exist under other types as well, including:
- hybrid human-agent
- multi-operator
- distributed-layer

So in this document, **partial** names the category.
Workflow type remains a separate axis.

Pandora should recognize several broad kinds of partial routes.

### 1. Single-Layer Routes

These routes execute only one layer.

Examples:
- L1-only
- L2-only
- L3-only
- L4-only

These are valid when the goal is to isolate one analytical dimension cleanly.

### 2. Narrow Multi-Layer Routes

These routes execute a small lawful subset of layers.

Examples:
- L2 + L3
- L3 + L4
- L1 + L2

These are valid when the selected dimensions are sufficient for the intended claim scope.

### 3. Triage Routes

These routes are designed for quick first-pass analytical filtering rather than full downstream judgment.

Examples:
- rapid misuse-domain mapping
- early behavior risk scan
- fast artifact screening

These routes are often preparatory rather than terminal.

### 4. Preparation Routes

These routes exist to produce structured outputs for later use by a deeper route.

Examples:
- artifact extraction before capability review
- early layer outputs prepared for later synthesis
- narrow route used to populate a case record for later expansion

These routes should explicitly state that they are preparatory.

### 5. Exploratory Routes

These routes are narrow because the operator is exploring uncertainty rather than trying to finalize a conclusion.

These are especially useful in freestyle sessions.

They remain valid only if their exploratory status is declared.

---

## General Rules for Partial Routes

All valid partial routes must obey the following rules.

### Rule 1 — Scope Must Be Explicit

A partial route must declare:
- what was analyzed,
- what layers or stages participated,
- what was intentionally excluded,
- and what claim scope is therefore permitted.

### Rule 2 — Reduced Scope Must Reduce Claim Scope

A route that executes fewer dimensions must also reduce what it is allowed to conclude.

For example:
- a behavior-only route cannot silently claim full operational risk
- an artifact-only route cannot silently claim full alignment interpretation
- a misuse-only route cannot silently claim practical executability

### Rule 3 — Dependencies Must Still Be Lawful

A partial route may be narrow, but it may not violate structural law.

Examples:
- a synthesis stage cannot run unless its required upstream inputs exist
- a reporting object cannot claim final integrated judgment if the route never created the required inputs
- a narrow route cannot borrow missing dimensions rhetorically

### Rule 4 — The Route Must Be Identifiable as Partial

The final result should visibly state that the execution route was partial.

This should appear in:
- route metadata
- analytical scope
- claim scope
- and final result language where relevant

### Rule 5 — Partial Does Not Mean Informal

A partial route still needs:
- execution mode
- route metadata
- stage sequence
- completion state
- and decomposable outputs

Partiality changes depth, not discipline.

---

## Baseline Partial Patterns

The following patterns should be treated as valid baseline partial routes.

---

## Pattern 1 — L1-Only Classification Route

### Pattern ID
`PA-L1-001`

### Type
`single-operator` / `freestyle-compatible`

### Purpose
To classify the misuse domain of the evaluated unit without attempting broader behavioral, artifact, or capability interpretation.

### Typical Use
- fast domain mapping
- taxonomy assignment
- dataset labeling
- first-pass case sorting

### Executed Scope
- L1 only

### Allowed Claims
- misuse-domain identification
- primary/secondary category structure
- taxonomy-level mapping

### Forbidden Claims
- behavior quality claims
- artifact quality claims
- operationality or barrier-lowering claims
- session-level integrated danger judgment

### Why It Matters
This route is useful when the immediate need is structured misuse labeling rather than full analytical depth.

---

## Pattern 2 — L2-Only Behavioral Route

### Pattern ID
`PA-L2-001`

### Type
`single-operator` / `freestyle-compatible`

### Purpose
To analyze how the model behaved during the interaction without attempting full artifact or capability interpretation.

### Typical Use
- behavior profiling
- refusal analysis
- drift analysis
- jailbreak susceptibility observation
- alignment-style comparison

### Executed Scope
- L2 only

### Allowed Claims
- behavioral posture
- refusal quality
- drift patterns
- manipulation sensitivity
- session-level behavioral observations

### Forbidden Claims
- artifact usability judgments
- operational capability judgments
- full integrated severity conclusions

### Why It Matters
This route isolates one of Pandora’s strongest dimensions: how alignment behaves under conversational pressure.

---

## Pattern 3 — L3-Only Artifact Route

### Pattern ID
`PA-L3-001`

### Type
`single-operator` / `freestyle-compatible`

### Purpose
To analyze the artifact produced by the model as an informational object.

### Typical Use
- output structure review
- completeness review
- granularity screening
- artifact cataloging
- artifact comparison across cases

### Executed Scope
- L3 only

### Allowed Claims
- structure
- completeness
- detail level
- coherence
- artifact-form observations

### Forbidden Claims
- behavioral motive claims
- full capability or barrier-lowering claims unless separately supported
- integrated danger claims

### Why It Matters
This route is useful when the produced output itself is the primary object of interest.

---

## Pattern 4 — L3 + L4 Artifact-to-Capability Route

### Pattern ID
`PA-ACT-001`

### Type
`single-operator` / `freestyle-compatible`

### Purpose
To analyze what was produced and what that production likely enables, without attempting a full behavioral interpretation.

### Typical Use
- artifact screening with capability follow-through
- barrier-lowering review
- output-to-impact mapping
- practical enablement analysis

### Executed Scope
- L3
- L4

### Allowed Claims
- artifact properties
- practical usability
- barrier-lowering capacity
- output-level enabling assessment

### Forbidden Claims
- full behavioral masking claims unless behavior was actually evaluated
- full session-level alignment judgments
- integrated cross-domain conclusions requiring missing dimensions

### Why It Matters
This is one of the strongest narrow routes because it connects product quality to practical enablement directly.

---

## Pattern 5 — L2 + L3 Behavior-and-Artifact Route

### Pattern ID
`PA-BA-001`

### Type
`single-operator` / `freestyle-compatible`

### Purpose
To compare how the model behaved with what it produced, without necessarily proceeding into full capability judgment.

### Typical Use
- masked compliance screening
- refusal-versus-output tension analysis
- contradiction candidate surfacing
- session-level behavioral/artifact comparison

### Executed Scope
- L2
- L3

### Allowed Claims
- behavior/artifact comparison
- contradiction candidate identification
- tension between posture and product
- early containment-failure patterns

### Forbidden Claims
- full operational severity conclusions
- practical capability estimates unless a lawful downstream stage exists
- integrated final danger judgment beyond route scope

### Why It Matters
This route is especially useful when the main interest is whether behavioral posture matches the artifact actually delivered.

---

## Pattern 6 — Rapid Triage Route

### Pattern ID
`PA-TRIAGE-001`

### Type
`single-operator` / `freestyle-compatible`

### Purpose
To generate a fast structured first-pass review that determines whether a case should be escalated into a deeper workflow.

### Typical Use
- high-volume case screening
- early prioritization
- rough case ranking
- deciding whether a full route is warranted

### Executed Scope
Variable, but intentionally narrow.

A common implementation may use:
- L1 only
- L2 only
- or a very small selected combination

### Allowed Claims
- preliminary classification
- preliminary concern flag
- preliminary escalation recommendation
- recommendation for deeper route selection

### Forbidden Claims
- terminal benchmark judgment
- deep integrated synthesis
- stable high-confidence final assessment

### Why It Matters
Not every case deserves full depth immediately. Triage routes make Pandora more practical at scale.

---

## Pattern 7 — Preparatory Pre-Synthesis Route

### Pattern ID
`PA-PREP-001`

### Type
`single-operator` / `freestyle-compatible`

### Purpose
To generate lawful upstream structured outputs that will later feed a deeper workflow or synthesis stage.

### Typical Use
- preparing selected layer outputs
- structuring evidence before a later full run
- creating analysis-ready objects for future synthesis experiments

### Executed Scope
Selected lawful upstream stages only.

### Allowed Claims
- preparatory observations
- intermediate structured outputs
- readiness for later route expansion

### Forbidden Claims
- full final assessment
- claims that imply the later route has already occurred
- terminal interpretive compression

### Why It Matters
This pattern is especially useful while synthesis blocks and richer routes are still being tested and finalized.

---

## Choosing the Right Partial Route

A partial route should be chosen based on the question being asked.

A good rule is:

### If the question is narrow, the route may be narrow.
### If the claim is broad, the route must be broad enough to support it.

Pandora should not select routes by habit alone.
It should select them by analytical fit.

---

## Partial Route Metadata

Every partial route should emit clear route metadata.

At minimum, this should include:

```text
route_id
route_name
route_version
execution_mode
is_partial_route
declared_scope
executed_stage_sequence
omitted_dimensions
claim_scope
completion_state
```

This matters because downstream reviewers must be able to see immediately that the route was partial and in what way.

---

## Partial Reporting Discipline

A partial route may still produce a structured output.

But that output should preserve partiality explicitly.

A clean partial result should usually include:
- declared route scope
- executed analytical dimensions
- omitted dimensions
- allowed claim scope
- final route-limited conclusion

This protects Pandora from one of the most common failures in modular systems:
narrow routes producing inflated narratives.

---

## When Partial Routes Should Expand

A partial route may lawfully expand when:
- the route itself includes an authored expansion branch
- or a freestyle session explicitly broadens scope and logs the change

Examples:
- L2-only route expands into L2 + L3 because contradiction candidates appear
- triage route expands into the single-operator default because a threshold condition is met
- preparatory route becomes a deeper route because later stages are now justified

Expansion is valid.
Silent expansion is not.

---

## When Partial Routes Should Not Expand

A partial route should remain narrow when:
- its purpose is already satisfied
- missing dimensions are not required for the allowed claim scope
- the operator is only preparing upstream outputs
- available evidence does not justify deeper execution
- route expansion would create false precision rather than real clarity

Pandora should not deepen just because it can.
It should deepen when the route logic or analytical purpose justifies it.

---

## Failure Conditions

A partial route should be considered weak or invalid if:
- it does not declare itself as partial
- it hides omitted analytical dimensions
- it produces claims broader than its scope supports
- it uses downstream language that implies missing stages occurred
- it invokes synthesis without lawful upstream inputs
- it cannot be decomposed back into its narrow path

These are not minor errors.
They destroy the credibility of modular analysis.

---

## Notes for Implementation

The public workflow layer should make partial routes easy to use correctly.

That means:
- clear naming
- explicit scope declarations
- explicit claim-scope limits
- clean metadata
- and stable narrow-route patterns that solo researchers can adopt immediately

Partial routes should feel legitimate, not improvised.

---

## Notes for Evaluation

A good partial route should be judged by questions like:
- Did it remain honest about what it executed?
- Did it avoid overclaiming?
- Did it produce useful route-limited intelligence?
- Did it remain traceable?
- Did it preserve decomposability?
- Did it help select or prepare the next route well?

If yes, then the partial route is doing real work.

---

## Summary

Pandora supports partial analysis because Pandora is modular.

A partial route is valid when:
- its scope is explicit,
- its omissions are visible,
- its dependencies remain lawful,
- and its claims remain proportional to what was actually executed.

Single-layer routes, narrow multi-layer routes, triage routes, preparatory routes, and exploratory routes are all legitimate when used honestly.

Partial execution is not a weakness.
Misrepresented partial execution is.

---

## Final Principle

A partial Pandora route is strong when it narrows execution without inflating conclusion.
