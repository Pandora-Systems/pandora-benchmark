# Scope and Trigger Model

## Purpose

This document defines how Pandora execution routes express scope and trigger logic.

A valid execution route is not only a list of stages. It also defines:
- what the analysis is about,
- how wide the route is allowed to go,
- what kind of outputs it may produce,
- and under what conditions each next stage is allowed to occur.

This matters because Pandora supports both:
- predefined workflows selected at the start of a run,
- and rule-bound freestyle sessions composed during execution.

In both cases, scope and trigger logic must remain explicit.

Without a scope model, routes become vague.
Without a trigger model, routes become improvisational in the wrong way.

This document exists to prevent both failures.

---

## Core Principle

> Scope defines the permitted analytical reach of a run.  
> Triggers define the lawful conditions under which that run may advance.

This is the central distinction.

Scope answers:
- what is in bounds,
- how far the route goes,
- what the run is allowed to claim.

Triggers answer:
- when a stage may run,
- when a route may branch,
- when synthesis may occur,
- when validation is invoked,
- when reporting is emitted,
- and when execution stops.

Pandora should never allow either of these to remain implicit.

---

## 1. Scope Is Multi-Dimensional

Scope is not one setting.

A Pandora execution route should define scope across multiple dimensions.

### A. Unit Scope
What is the evaluated unit?

Examples:
- single turn
- selected segment
- full conversation
- multi-conversation package
- compiled case bundle

This is the most basic scope declaration.
No route should begin without it.

### B. Material Scope
What material is included in the run?

Examples:
- user/model messages only
- model outputs only
- structured layer outputs
- prior run artifacts
- validation metadata
- supporting notes or annotations

Material scope matters because it determines what stages can lawfully consume.

### C. Analytical Scope
Which dimensions of Pandora are participating?

Examples:
- L1 only
- L2 + L3
- L3 + L4
- L1 → L4 full path
- selected synthesis stages after selected layers

Analytical scope defines what the route is designed to measure or interpret.

### D. Route Scope
How large is the execution route?

Examples:
- single-pass route
- multi-pass route
- route with validation
- route with final synthesis only
- route with interim checkpoints

This determines the structural depth of the run.

### E. Claim Scope
What level of claim is the route allowed to produce?

Examples:
- turn-level observation
- session-level judgment
- comparative case finding
- provisional model-level suggestion
- benchmark-ready structured result

This is critical.

Pandora should distinguish between:
- the scope of what was analyzed,
- and the scope of what may be claimed.

A narrow run must not silently produce wide claims.

---

## 2. Scope Must Be Declared at the Start of Execution

Every Pandora run must begin with an explicit scope declaration.

### In workflow mode
Scope is declared by the authored workflow itself.

The workflow should already specify:
- unit scope
- material scope
- analytical scope
- route scope
- intended claim scope

### In freestyle mode
Scope must still be declared at the start of the session, even if the full route is not yet known.

At minimum, the session should declare:
- initial unit scope
- initial material scope
- initial analytical scope
- provisional claim scope

If scope changes during a freestyle session, the change must be explicitly logged rather than silently assumed.

Pandora may allow scope expansion.
It must not allow scope drift.

---

## 3. Scope Expansion Must Be Explicit

Some routes may legitimately widen during execution.

Examples:
- a segment analysis becomes a full-session analysis
- an L2-only route expands into L2 + L3
- a first-pass route expands into a validation pass
- a narrow review expands into a full structured report

This is acceptable only when:
1. the expansion is explicitly recorded
2. the new scope is lawful
3. the route metadata reflects the change
4. downstream claims respect the updated scope rather than the original one

Freestyle mode may do this more often than workflow mode, but the same law applies:
scope change must be declared, not implied.

---

## 4. Trigger Logic Exists to Authorize Progression

A trigger is a route-level condition that authorizes a next stage.

A trigger does not create truth.
It authorizes movement.

This distinction matters.

A trigger may say:
- now the required inputs exist
- now validation is required
- now reporting is allowed
- now a branch is permitted
- now the route should terminate

A trigger must not say:
- the case is severe because the route advanced
- the output is meaningful because a checkpoint fired

Triggers are execution laws, not conclusions.

---

## 5. Core Trigger Families

Pandora should recognize several trigger families.

### A. Dependency Triggers
These authorize a stage only when its required inputs exist.

Examples:
- a synthesis stage may run only after valid upstream outputs are present
- a validation stage may run only after comparable outputs exist
- a report stage may run only after the required reasoning objects exist

This is the most fundamental trigger family.

### B. Completion Triggers
These fire when a defined stage path has been completed.

Examples:
- all selected layers for the route are complete
- all required passes have been executed
- all mandatory validation steps are done

These triggers are especially important in workflow mode.

### C. Escalation Triggers
These authorize route deepening.

Examples:
- a narrow route may expand because a threshold condition is met
- an exploratory run may add another stage because a meaningful signal has appeared
- a freestyle session may shift from observation to deeper analysis

Escalation triggers do not themselves define the new route.
They authorize lawful expansion.

### D. Validation Triggers
These invoke a reliability check.

Examples:
- disagreement threshold reached
- ambiguity threshold reached
- route marked as high-value or high-uncertainty
- mandatory second pass required by workflow design

These triggers matter because Pandora values stability, not only first-pass cleverness.

### E. Synthesis Checkpoint Triggers
These authorize interpretive stages.

Examples:
- selected upstream layers are complete
- required reasoning inputs exist
- route design specifies a checkpoint after a given stage set

This is better than saying “run synthesis whenever it feels right.”

Pandora should treat synthesis checkpoints as authorized route points, not vague interpretive impulses.

### F. Reporting Triggers
These authorize output emission.

Examples:
- interim route summary
- final structured result
- escalation memo
- validation note
- benchmark-ready package

Reporting triggers decide when outputs are emitted, not what they mean.

### G. Termination Triggers
These define when the route should stop.

Examples:
- declared route complete
- lawful next stage unavailable
- evidence sufficiency reached
- route explicitly halted
- termination branch reached

A route without termination logic becomes messy quickly.

---

## 6. Triggers Must Be Predeclared in Workflow Mode

In workflow mode, trigger logic belongs to the authored workflow.

A workflow should specify in advance:
- what completion triggers exist
- what escalation triggers exist
- what validation triggers exist
- what synthesis checkpoints exist
- what reporting triggers exist
- what termination conditions exist

This does not mean the workflow must be fully linear.
It may contain branches.

But those branches must be authored into the workflow rather than invented during the run.

A workflow is a predefined execution contract.
Its trigger logic is part of that contract.

---

## 7. Triggers May Be Applied Live in Freestyle Mode, But Must Still Be Lawful

In freestyle mode, trigger logic may be applied during execution.

But “live” does not mean unconstrained.

A freestyle session may:
- add a stage because a lawful escalation trigger is satisfied
- invoke validation because a lawful validation trigger is satisfied
- invoke synthesis because required inputs now exist
- terminate because a lawful stop condition is met

What it may not do is invent structural permissions that ignore dependency or order rules.

Freestyle mode allows live composition.
It does not allow live suspension of routing law.

---

## 8. Synthesis Checkpoints Must Be Defined as Authorized Route Points

Pandora should use the term **synthesis checkpoint** rather than vague phrases like “do synthesis.”

A synthesis checkpoint is a route point at which one or more interpretive stages are authorized because their required inputs are available.

Examples:
- after completion of the selected layer path
- after a defined subset of layers has produced outputs
- after validation has produced a stable or contested upstream state
- at final assessment point

In workflow mode, these checkpoints are authored in advance.
In freestyle mode, they must still satisfy input and dependency law before they are added.

This language is much cleaner than treating synthesis like a foggy end-stage that “somehow happens.”

---

## 9. Scope and Trigger Logic Must Stay Separate

A common failure is to confuse scope and trigger logic.

### Scope says:
this run covers the full conversation.

### Trigger says:
final synthesis may occur after the selected layer path is complete.

### Scope says:
this route is limited to L2 and L3.

### Trigger says:
reporting may occur once both selected layers are complete.

Scope defines the bounds.
Triggers define progression within those bounds.

Pandora should never collapse the two.

---

## 10. Route Depth Must Be Measurable

One reason Pandora needs explicit scope and trigger logic is so route depth can be analyzed later.

A run should make it possible to inspect:
- how wide the route was
- how deep the route went
- how many stages fired
- how many checkpoints existed
- whether validation occurred
- whether escalation occurred
- whether the route stayed narrow or expanded

This means route metadata should preserve:
- declared scope
- actual executed scope
- trigger events
- stage count
- branch count
- checkpoint count
- completion state

Execution flow is itself valuable data.

Pandora should be able to study not only case outputs, but also analysis-route behavior downstream.

---

## 11. Minimal Scope Declaration

At minimum, every Pandora run should declare:

```text
execution_mode
unit_scope
material_scope
analytical_scope
route_scope
claim_scope
```

This is the smallest acceptable scope object.

Anything less becomes too ambiguous for serious downstream use.

---

## 12. Minimal Trigger Declaration

At minimum, every Pandora execution route should define or log:

```text
dependency_triggers
completion_triggers
synthesis_checkpoints
reporting_triggers
termination_conditions
```

More advanced routes may also define:
- escalation triggers
- validation triggers
- branch triggers
- route-expansion triggers

But the minimal trigger set above should exist in every mature Pandora route.

---

## 13. Scope Fidelity Must Constrain Reporting and Claims

This principle is worth isolating because it is so important.

A route may only produce claims that are justified by its declared and executed scope.

Examples:
- a turn-level route should not silently produce session-level conclusions
- a partial analytical route should not pretend it executed the full stack
- a freestyle exploratory session should not masquerade as a standardized benchmark run
- a non-validated run should not imply the confidence of a validated one

Scope fidelity protects Pandora from overclaiming.

Sharp routes are better than inflated routes.

---

## 14. Scope and Trigger Logic Must Remain Automation-Compatible

Scope and trigger models should be explicit enough to become machine-operable later.

That means:
- scopes should be representable as structured objects
- triggers should be representable as explicit route conditions
- checkpoints should be identifiable
- branch logic should be formal enough to log and analyze

If these remain vague, Pandora’s later automation and orchestration layers become much harder to build cleanly.

---

## 15. Freestyle Mode Should Generate Workflow Candidates

Freestyle mode is not just tolerated.
It is useful.

When a freestyle route repeatedly shows:
- a stable scope pattern
- a recurring trigger pattern
- a useful stage sequence
- and strong downstream value,

that route becomes a candidate for formal workflow design.

This is one of the most important reasons to track scope and trigger logic properly.
It allows Pandora to learn from live analytical practice and convert repeated good execution into stable doctrine.

---

## Summary

The Pandora scope and trigger model exists to make execution routes disciplined, analyzable, and scalable.

Scope defines:
- what is in bounds,
- how far the run goes,
- and what the route is allowed to claim.

Triggers define:
- when a stage may run,
- when the route may deepen,
- when synthesis checkpoints are authorized,
- when validation occurs,
- when reporting is emitted,
- and when the route ends.

Pandora supports both:
- predefined workflow execution,
- and rule-bound freestyle execution.

In both cases, scope must be explicit and triggers must remain lawful.

That is how Pandora stays flexible without becoming vague.

---

## Final Principle

A Pandora run is only as disciplined as its declared scope and its lawful trigger logic.
