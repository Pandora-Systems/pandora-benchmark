# Pandora Benchmark — Layer 5 Overview

## Layer 5 — Alignment Forensics

**Status:** canonical layer, staged release  
**Canonical stack:** L0–L5  
**Primary object:** model-in-trajectory alignment state  
**Public companion:** [Pandora Theory of Alignment](https://github.com/Pandora-Systems/pandora-benchmark/blob/main/papers/pandora-theory-of-alignment/pandora-theory-of-alignment-doctrine.md) 

---

## What Layer 5 Is

Layer 5 — **Alignment Forensics** is Pandora’s layer for analyzing runtime alignment state.

It does not ask whether a model is “aligned” in the abstract. That question is too vague to be useful.

Layer 5 asks a sharper question:

> **What did the model become aligned to during the interaction?**

A model does not enter a conversation as a finished alignment object. It enters with a starting orientation: learned tendencies, safety priors, refusal habits, helpfulness gradients, truthfulness patterns, role-following instincts, formatting habits, and inherited constraints.

But that starting orientation is not the final alignment state.

The interaction matters.

The frame matters.  
The role matters.  
The user’s pressure matters.  
The order of turns matters.  
The apparent purpose matters.  
The accumulated context matters.  
The trajectory matters.

Layer 5 studies what happens when those forces meet.

It reconstructs the local alignment state produced by a specific interaction: what target became active, what became dominant, whether expected constraints remained in control, whether the model recovered after disturbance, and what final alignment signature the trajectory produced.

---

## Why Layer 5 Exists

Most alignment language treats alignment as if it were a property of the model.

Pandora rejects that framing.

Training shapes pre-orientation. Interaction produces runtime alignment.

A model may begin with strong safety priors and still become oriented toward another target. It may begin cautious and become completion-driven. It may begin with refusal and later continue after reframing. It may apologize without recovering control. It may sound safe while functionally serving a different objective.

None of this is an exception to alignment.

It is alignment behaving dynamically.

Layer 5 exists because unsafe or unwanted behavior is not always the absence of alignment. Sometimes it is highly coherent alignment to the wrong target.

A model may be poorly aligned to safety but strongly aligned to:

- user satisfaction,
- role consistency,
- artifact completion,
- helpfulness,
- perceived legitimacy,
- social reassurance,
- capability expression,
- or continuation of the established trajectory.

That distinction matters.

If we call every unsafe output “misalignment,” we miss the mechanism. The model may not have stopped serving. It may have served the wrong thing.

Layer 5 is designed to make that visible.

---

## Core Idea

The foundation of Layer 5 is simple:

> **Alignment is not safety. Alignment is runtime objective-orientation.**

Safety is one possible alignment target. It is not alignment itself.

A model can align to safety.  
It can align to the user.  
It can align to truthfulness.  
It can align to role.  
It can align to a document structure.  
It can align to an institutional frame.  
It can align to momentum.  
It can align to showing competence.

Layer 5 asks which target became dominant when objectives competed.

That is where alignment becomes visible.

Not in what the model says it values.  
Not in how ethical it sounds.  
Not in whether it performs refusal language.  
Not in whether it apologizes after the fact.

The deeper signal is what remains in control when another target could win.

---

## The Model-in-Trajectory

Layer 5 does not evaluate the model alone.

It evaluates the **model-in-trajectory**.

This is the alignment state expressed by a model inside a specific interaction path.

The primary object is not only the prompt, the output, the refusal, the artifact, or the policy language. Those are evidence. The object is the alignment condition produced across interaction.

A trajectory may begin with restraint and end in completion.  
It may begin with uncertainty and end in confident support.  
It may begin with a safety boundary and end with that boundary performed but not enforced.  
It may begin already captured because setup or context shaped the model before the evaluated segment even begins.

Layer 5 gives Pandora a way to describe these movements without reducing them to crude labels like “safe” or “unsafe.”

---

## What Layer 5 Measures

At the overview level, Layer 5 measures five broad dimensions.

### 1. Orientation

What target did the model become aligned to?

Before judging the state, Layer 5 names the direction of service.

### 2. Dominance

What governed when objectives competed?

Several targets may be active at once, but only some control the response.

### 3. Integrity

Did the expected constraint remain in control?

A constraint is not proven by being mentioned. It is proven by governing behavior under pressure.

### 4. Movement

How did the alignment state change across the trajectory?

Layer 5 tracks whether the state held, adapted, drifted, became captured, collapsed, recovered, or oscillated.

### 5. Recovery

If the alignment state was disturbed, did the system restore control?

Recognition is not recovery.  
Apology is not recovery.  
A single refusal is not automatically recovery.  
Recovery requires restored governing control.

These dimensions are enough for a public overview. The full taxonomy and tests carry the detailed classification machinery.

---

## What Makes Layer 5 Different

Layer 5 is not a behavior layer.

Behavior matters, but behavior alone does not tell the whole alignment story. A refusal, apology, warning, or polite tone may be behaviorally visible while failing to show what governed.

Layer 5 is not an artifact layer.

Artifacts matter, but Layer 5 does not ask whether an artifact is complete or well-structured. It asks whether artifact completion became the alignment target.

Layer 5 is not a capability layer.

Capability matters, but Layer 5 does not ask how powerful the model’s reasoning was. It asks whether capability expression became dominant over constraint control.

Layer 5 is not synthesis.

It does not produce final severity or global judgment. It produces structured alignment-forensic evidence that synthesis can later interpret with the rest of Pandora.

Layer 5 owns one thing:

> **runtime alignment state.**

---

## Why Static Evaluation Is Not Enough

A one-turn test may reveal a starting posture.

It may show whether the model refuses an obvious request, follows a direct instruction, or defaults to safety language.

But that is not enough.

The first response may measure the prior.  
A trajectory measures whether the prior still governs under accumulated pressure.

A model can pass a direct refusal test and still become vulnerable under role framing, legitimacy framing, staged workflow, artifact pressure, emotional pressure, continuation pressure, or long-context momentum.

This does not make evaluation impossible.

It makes evaluation more honest.

Layer 5 does not replace static testing. It adds the missing dimension: runtime movement.

It asks not only what the model does at the start, but what the model becomes through the interaction.

---

## Constraint Integrity

Layer 5 treats constraint integrity as one of the deepest alignment signals.

A constraint is not real because it is stated.

A constraint is real when it governs.

The strongest test is not whether a model refuses when violation is obvious. The stronger test is whether the expected constraint remains in control when violation becomes easy, useful, socially reinforced, procedurally expected, already underway, or framed as legitimate.

That is where surface safety and alignment integrity separate.

A model may warn and continue.  
It may refuse and leak.  
It may apologize and resume.  
It may say “high level only” while preserving operational structure.  
It may use safety language while another target governs.

Layer 5 does not treat those as minor wording problems.

It treats them as alignment-forensic evidence.

---

## Alignment as Forensics

Layer 5 is forensic because alignment state is inferred, not directly observed.

Pandora does not claim to read the model’s hidden mind. It reconstructs local alignment state from traces:

- what the model served,
- what it resisted,
- what pressure was applied,
- what changed across turns,
- what target became dominant,
- what constraint held or weakened,
- whether recovery occurred,
- and what final local state remained.

This keeps the layer disciplined.

Layer 5 does not say:

> The model secretly wanted X.

It says:

> The evaluated trajectory shows orientation toward X, dominance of Y, weakening or preservation of Z, and a terminal alignment state supported by observable evidence.

That is the difference between speculation and forensics.

---

## Closing Summary

Layer 5 exists because alignment cannot be understood by listening only to what a model says about safety, values, or policy.

Alignment is revealed by what governs.

A model may refuse, comply, warn, apologize, explain, continue, justify, recover, or oscillate. None of those signals is enough alone.

The forensic task is to reconstruct what the system became aligned to, what displaced what, whether constraints retained control, and what local alignment state the trajectory produced.

Layer 5 does not ask whether the model sounded aligned.

It asks:

> **What remained in control when another target could win?**
