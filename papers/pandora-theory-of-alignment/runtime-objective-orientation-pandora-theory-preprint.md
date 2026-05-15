# Runtime Objective-Orientation as a Theory of AI Alignment

## The Pandora Theory of Alignment

## Abstract

AI alignment is often treated as a property of a model: something produced through training, strengthened through feedback, encoded through principles, and evaluated through observed behavior. This paper argues that this framing is incomplete for interactive AI systems. A trained model does not enter use as a static object. It enters an interaction trajectory shaped by context, role, task structure, prior turns, apparent purpose, and competing pressures.

The Pandora Theory of Alignment proposes **runtime objective-orientation** as a missing object of alignment analysis. On this account, alignment should not be understood only as a model-level disposition or an output-level behavior. It should also be studied as the active ordering of objectives, constraints, frames, and response tendencies during interaction. This means that alignment is not only a question of whether a system appears safe or compliant, but of what it becomes oriented toward under the conditions of interaction. The relevant analytical unit is therefore not the isolated model alone, but the **model-in-trajectory**.

This reframing changes the questions alignment evaluation must ask. It is not enough to ask whether a model appears safe, refuses a request, follows a policy, or produces acceptable output under a selected condition. A stronger analysis must ask what governs when objectives compete, what remains in control as interaction pressure accumulates, and whether the target that becomes dominant is the target that should have governed. This paper presents the theory as a conceptual ontology, not as an operational methodology. The adversarial procedures that motivated the theory are intentionally withheld. The contribution is a vocabulary for studying runtime control, target dominance, and alignment under interaction pressure.

---

## 1. Introduction

AI alignment is often discussed as if it were primarily a property of a model.

A model is trained. Its behavior is shaped. Its refusals are tested. Its outputs are evaluated. Its deployment risk is assessed. Under this framing, alignment is treated as something the model possesses, lacks, or expresses through behavior under selected conditions.

This framing is useful. It has produced real progress. Modern language models are more instruction-following, more steerable, more cautious around many harmful requests, and more capable of expressing safety-oriented reasoning than earlier systems. Training-time interventions, feedback methods, constitutional rules, red-teaming, and benchmark evaluations have all changed how deployed systems behave.

But the framing remains incomplete.

A model does not meet the world as a static object. It enters an interaction. That interaction has structure: a user, a task, a role, a format, a tone, an apparent purpose, a prior history, and an accumulating trajectory. Each turn changes the local conditions under which the next turn is generated. The model does not merely reveal a fixed alignment state inside that field. The field participates in producing the active alignment state that becomes visible.

This paper argues that alignment should be analyzed not only as a property of the trained model, but as a runtime process produced by the relation between the model and the trajectory it enters.

The proposed name for this account is the **Pandora Theory of Alignment**.

Its central claim is simple:

> **Alignment is runtime objective-orientation.**

By runtime objective-orientation, this paper means the active ordering of objectives, constraints, frames, and response tendencies during interaction. The relevant analytical unit is not the isolated model alone, but the **model-in-trajectory**: the model as situated inside a specific interaction path.

The claim is not that training is irrelevant. Training matters deeply. It shapes safety priors, refusal tendencies, helpfulness patterns, truthfulness habits, system constraints, and response style. A model trained to preserve certain boundaries is meaningfully different from one that has not been trained to do so.

The claim is that training creates the starting field, not the final runtime state. Once the system enters interaction, its trained tendencies must operate alongside local pressures: role consistency, user satisfaction, format completion, conversational momentum, apparent legitimacy, and the need to continue or revise prior turns. In ordinary cases, these pressures may align. In harder cases, they compete.

That competition is where alignment becomes visible.

A refusal may reveal a starting boundary. A continuation may reveal a later priority. A warning, apology, disclaimer, or safe tone may matter, but none alone settles what governs when pressure accumulates. The question is not only what the model was trained to prefer, nor only what output it produced under one selected condition. It is what remains in control as the interaction unfolds.

That gap is the concern of this paper.

Section 2 motivates the runtime gap in training, evaluation, and deployment. Section 3 positions the theory against related work. Section 4 presents the theory. Sections 5 and 6 discuss implications, scope, and responsible-disclosure boundaries. Section 7 concludes.

## 2. Background and Motivation

The argument of this paper begins from a practical observation: much alignment work is organized around shaping, measuring, and improving model behavior before or outside the full conditions of interactive use.

That organization is necessary. A model must be trained before it is deployed. Its failures must be sampled before they are mitigated. Evaluation requires tractable prompts, repeatable conditions, measurable outputs, and interpretable results.

But deployed language models do not only express trained dispositions. They participate in continuing interactions. Prior turns, task framing, user corrections, role assignments, format expectations, and apparent purpose can all change what becomes salient or natural next. A model may begin from one safety posture, while later behavior reflects both that starting posture and the local structure of the conversation.

This creates a runtime gap: the gap between trained tendency, sampled behavior, and active control inside an unfolding trajectory.

---

## 2.1 Training-Time Shaping

Modern alignment practice often begins with training-time or post-training intervention. A base model is shaped through instruction tuning, human feedback, preference modeling, constitutional principles, system-level constraints, safety classifiers, or related methods. These processes alter response tendencies. They can make a model more helpful, more cautious, more refusal-capable, and more sensitive to certain classes of harmful request.

This matters. Training and post-training create real alignment-relevant structure.

But they do not settle the runtime alignment problem. A trained system enters interaction with tendencies, not with a guarantee about what will govern under every future trajectory. Its safety priors may compete with helpfulness, completion, instruction-following, role consistency, coherence, user satisfaction, and conversational continuation.

A useful distinction is therefore this:

> Training shapes the model's initial orientation. Interaction determines which orientation becomes active, dominant, or unstable under local conditions.

Training-time alignment is better understood as pre-runtime shaping than as final runtime governance.

---

## 2.2 Behavioral Evaluation

A second major alignment frame is behavioral evaluation.

A model is given prompts, tasks, benchmark items, adversarial probes, or red-team scenarios. Its responses are then classified, scored, compared, or inspected. Did it refuse? Did it comply? Did it hallucinate? Did it follow policy? Did it avoid unsafe completions?

This is indispensable. Without behavioral evaluation, alignment claims remain abstract.

But behavioral evaluation samples behavior under chosen conditions. Every prompt, benchmark, system instruction, scoring rule, and test environment creates a local interaction field. A refusal under one condition is evidence; it is not proof that the same constraint will govern under all relevant trajectories. A benchmark pass is evidence; it is not a neutral sample of alignment-in-general.

Many safety-relevant failures are also not visible as immediate single-turn breakdowns. Some appear after context accumulates, after a role has been accepted, after a document has been partially built, or after earlier safe statements coexist with later unsafe assistance. For alignment analysis, the issue is not only whether a response was acceptable at one point. The issue is whether the response reveals stable runtime governance.

That requires attention to trajectory.

---

## 2.3 Deployment as Interaction

Deployment makes the runtime problem unavoidable.

Users ask follow-up questions. They correct the model. They provide context. They assign roles. They request formats. They build documents over multiple turns. They frame tasks as professional, fictional, educational, defensive, urgent, harmless, or already authorized. They may also apply social, emotional, procedural, or epistemic pressure, intentionally or not.

A deployed model responds inside that field.

The interaction is not a sequence of independent prompts. It is an accumulating context in which previous turns alter the meaning and pressure of later turns. A request made at turn one may be treated differently from a similar request made after a role has been established, a purpose has been normalized, or an artifact has already been started.

An output is therefore evidence from a trajectory. To understand it, one must ask what local commitments, frames, and expectations preceded it: was the model answering a fresh request, continuing an established artifact, preserving a role, following a format, or maintaining conversational coherence?

These questions do not require assuming hidden intention or consciousness. They require only that language-model behavior is conditional on context and that context changes across interaction.

---

## 2.4 The Runtime Gap

The runtime gap is the space between three things:

1. the model's trained starting tendencies;
2. the behavior observed under selected evaluation conditions;
3. the active ordering of objectives and constraints during an unfolding interaction.

Alignment work has strong tools for the first two. It can shape models before deployment and sample their behavior during evaluation. The third object is harder to name: what becomes active, what becomes dominant, and what remains in control when interaction applies pressure.

The runtime gap appears when the analyst asks questions such as:

- What governs after the interaction has accumulated context?
- What changes when the model is continuing a trajectory rather than answering a fresh prompt?
- What happens when helpfulness, caution, accuracy, role consistency, and completion no longer point in the same direction?
- Does safety language correspond to actual control, or only to local presentation?

These are runtime phenomena. They are not fully answered by training history or isolated response behavior.

---

## 2.5 Empirical Motivation Without Operational Disclosure

The theory developed in this paper is motivated by adversarial observation of language-model behavior across extended interactions.

Those observations suggested a recurring pattern: some alignment-relevant phenomena are difficult to understand if the model is treated only as a static object or if outputs are treated as isolated events. The same system may show different local priorities under different trajectories. Surface caution may coexist with practical assistance. Refusal may occur at one point and weaken later. Conversely, a model may preserve a boundary even when continuation would be easy.

These patterns motivate a theory of alignment as runtime control rather than static possession.

This paper does not disclose the adversarial procedures used to explore those patterns. It does not provide prompt sequences, elicitation methods, jailbreak recipes, exploit workflows, or reproducible attack protocols. That omission is intentional.

The goal here is not to transfer operational capability. The goal is to define the conceptual object that such observations reveal: a vocabulary for reasoning about runtime alignment phenomena without exposing the methods by which the most sensitive cases were elicited.

## 3. Related Work and Theoretical Positioning

The theory developed in this paper does not reject training-time alignment, preference learning, behavioral evaluation, red-teaming, or deployment robustness. It begins from a narrower claim: these approaches leave one object under-specified — the runtime ordering of objectives inside interaction.

This section situates that claim relative to prior work. Value alignment, preference learning, post-training, red-teaming, benchmark evaluation, distribution-shift analysis, specification gaming, and contextual theories of norm-governed action each illuminate part of the problem. Yet none fully centers the model-in-trajectory as the object of alignment analysis.

Where the related works converge is where the theory departs.

### 3.1 Value, Preference, and Intent Alignment

A major strand of alignment research frames the problem as one of learning, representing, or acting in accordance with human values, preferences, or intentions. Inverse reinforcement learning and related approaches treat the problem as one of inferring objectives from human behavior. Cooperative inverse reinforcement learning extends this framing by treating value alignment as a cooperative partial-information problem between human and machine, where the system must act while uncertain about the human reward function [1].

This tradition is central because it clarifies a deep challenge: the system cannot simply optimize an objective unless the objective is adequately specified, learned, or inferred. Alignment, on this view, concerns the relation between system behavior and the values or intentions that should guide it. The problem is not merely competence. It is whether competence is oriented toward the right end.

Preference-based reinforcement learning further operationalizes this orientation problem by using human comparisons over behavior to train systems toward preferred outcomes [2]. For language models, instruction tuning and reinforcement learning from human feedback extend the same broad pattern into deployed assistant behavior: model outputs are shaped toward human-preferred responses across distributions of prompts and tasks [4].

These approaches are foundational for modern alignment practice. They define mechanisms by which model behavior can be shaped toward human intent, helpfulness, harmlessness, honesty, or other desired criteria. They also reveal why alignment cannot be reduced to raw performance: a system can be powerful, fluent, and useful while still being oriented toward the wrong target.

The present theory builds on that insight, but shifts the unit of analysis. Preference learning and value alignment primarily concern how a model is trained or shaped to prefer some responses over others. Runtime objective-orientation asks what actually governs inside a specific interaction trajectory after that shaping has occurred.

Training can shape a starting distribution of tendencies. It cannot by itself settle which tendency will dominate under every future trajectory. A model may enter interaction with learned priors toward helpfulness, harmlessness, truthfulness, and refusal. The alignment question at runtime is which of these becomes active, which is subordinated, and which target controls behavior when they conflict.

The theory therefore does not deny the importance of values, preferences, or intent. It argues that these must be studied not only as training targets, but as candidates within a runtime field of competing objectives.

---

### 3.2 Post-Training and Behavioral Shaping

A second body of work focuses on shaping deployed assistant behavior after pretraining, including reward modeling and preference-based approaches to scalable alignment [3]. RLHF is the most prominent example in contemporary language-model alignment. It uses demonstrations, preference data, reward modeling, and reinforcement learning to produce models whose responses better match human judgments of helpfulness, truthfulness, safety, and instruction-following [4]. Constitutional AI extends this direction by using a set of principles to guide critique, revision, and reinforcement learning from AI feedback, with the goal of producing assistants that are helpful and harmless while requiring fewer direct human labels [5].

These methods matter because they changed the behavior of real deployed systems. They made language models more likely to follow instructions, refuse certain harmful requests, express uncertainty, preserve a safety posture, and produce responses that humans judge as more appropriate. A theory of runtime alignment must acknowledge this. It would be unserious to treat post-training as cosmetic or irrelevant.

But post-training also illustrates the gap this paper targets. Behavioral shaping can increase the probability of desired responses across a training or evaluation distribution. It does not make alignment a permanently settled property. It produces dispositions, response patterns, refusal tendencies, and learned associations between context and appropriate behavior. These are real. They are also conditional.

The central question becomes what happens when post-trained dispositions compete. A model may be trained to be helpful and harmless, but helpfulness and harmlessness do not always point in the same direction. It may be trained to follow instructions and preserve safety, but instruction-following and safety can conflict. It may be trained to produce complete, high-quality answers and also to avoid enabling harm, but completion pressure can compete with restraint.

Post-training gives the model a shaped starting field. Runtime interaction determines which part of that field becomes controlling under local conditions.

This distinction matters because an aligned-looking behavior may be the product of a dominant local objective rather than stable constraint integrity. A refusal may indicate safety dominance in one trajectory. A helpful completion may indicate task dominance in another. The same post-trained system can express different active priorities depending on how the interaction is framed, sequenced, and reinforced.

The contribution of this paper is therefore not a replacement for RLHF, Constitutional AI, or related techniques. It is a conceptual account of the runtime object these techniques leave behind: the active ordering of trained tendencies once the model is inside a trajectory.

---

### 3.3 Evaluation, Red-Teaming, and Robust Refusal

A third body of work evaluates language models through benchmark tasks, adversarial prompts, automated red-teaming, and refusal robustness. Evaluation frameworks such as HELM broadened model evaluation by measuring performance across many tasks, scenarios, and metrics rather than relying on isolated demonstrations [12]. Safety-specific evaluation and robust-refusal work has further emphasized harmful outputs, adversarial robustness, and the need for systematic evaluation rather than anecdotal testing [6].

This work is essential because it gives alignment practice a measurement culture. Without evaluation, alignment claims remain impressions. Red-teaming also reveals that failures may not appear under ordinary interaction. They often emerge under stress, adversarial framing, repeated attempts, or unusual task configurations. A model that behaves safely under a standard prompt may behave differently under pressure.

Automated red-teaming and robust-refusal benchmarks sharpen this point. HarmBench, for example, frames automated red-teaming and refusal robustness as objects requiring standardized evaluation across methods, models, and defenses [6].

Yet refusal robustness is still not identical to runtime alignment. A refusal is a behavioral event. It can be strong, weak, partial, performative, bypassed, contradicted, or later reversed. It can indicate that a safety target dominated at one point in the trajectory. It does not alone prove that the same target will remain dominant as the interaction evolves.

The same is true for benchmark success. A benchmark samples model behavior under defined conditions. Those conditions matter. The prompt distribution, evaluation format, scoring rule, conversation length, allowed retries, and adversarial pressure all shape what is being measured. There is no evaluation outside trajectory. There are only more or less controlled trajectories.

The theory developed in Section 4 takes this seriously. It treats evaluation not as a transparent window into a fixed alignment property, but as a conditional interaction that elicits an alignment state under specific circumstances. This does not weaken evaluation. It makes evaluation more honest about what it samples.

A runtime theory of alignment therefore does not ask evaluators to abandon benchmarks or red-teaming. It asks them to interpret results as evidence about model-in-trajectory behavior rather than proof of alignment-in-general.

---

### 3.4 Deployment, Triggers, and Distribution Shift

A fourth body of work concerns the gap between training or evaluation conditions and deployment behavior. The classic safety framing includes distributional shift as a practical problem: a system trained or evaluated under one set of conditions may behave undesirably when placed in another [7]. In language-model safety, related concerns appear in work on backdoors, deceptive behavior, trigger conditions, and failures that persist despite safety training.

Sleeper Agents is especially relevant here because it studies models trained to behave helpfully under ordinary conditions while exhibiting different behavior under specific triggers. The paper finds that certain backdoor behaviors can persist through standard safety training, including supervised fine-tuning, reinforcement learning, and adversarial training [8]. The immediate focus of that work is not the same as this paper, but it demonstrates a crucial point: observed safe behavior under one condition does not necessarily establish globally stable alignment.

Trigger-based and context-dependent behavior matters for runtime alignment because it shows that model behavior can be conditional in ways that are not obvious from ordinary evaluation. A model can appear aligned under familiar settings and fail under a specific context, cue, frame, or trajectory. The safety question is not only whether the model behaves well under the sampled condition. It is whether the governing constraint remains stable across relevant condition changes.

Distribution shift also shows that alignment is not only about the internal model. Deployment adds environment, user, task, interface, tool access, memory, policy context, and social framing. These conditions can change what behavior is likely and what objectives become locally salient. For interactive systems, deployment is not a passive container around model behavior. It is part of the field in which behavior is produced.

The present theory generalizes this insight from distributional shift to interaction trajectory. A trigger need not be a single hidden token or external condition. It can be a gradual accumulation of role, legitimacy, continuation, formatting, task pressure, and prior commitments. The relevant object is not merely the prompt at one moment, but the path by which the model arrived there.

This is why the model-in-trajectory matters. Runtime alignment is not exhausted by the base model, the prompt, or the output taken alone. It is the active orientation produced by their relation across time.

---

### 3.5 Specification Gaming, Goodharting, and Objective Conflict

A fifth body of work studies what happens when systems optimize proxies, misspecified objectives, or measurable targets that diverge from intended goals. Concrete Problems in AI Safety identifies reward hacking, side effects, scalable supervision, safe exploration, and distributional shift as practical accident risks in machine-learning systems [7]. Specification gaming and reward hacking examples show systems finding unintended ways to satisfy a stated objective while violating the spirit of the task [9].

Goodhart’s law provides a broader frame: when a measure becomes a target, it can cease to function as a reliable measure [10]. In AI systems, related failures appear when optimization pressure drives behavior toward the proxy rather than the intended objective. This literature is relevant because it distinguishes stated success from actual success. A system can satisfy the local target while betraying the intended one.

The connection to runtime objective-orientation is direct but not identical. Specification gaming often concerns an agent optimizing a misspecified reward or proxy. The present theory concerns an interactive language model in which multiple objectives, constraints, and learned response tendencies compete during interaction. The model may not be optimizing a single explicit reward at inference time in the same way an RL agent optimizes a reward function. Still, the structural lesson transfers: the target that governs behavior may differ from the target that was intended to govern.

This is the bridge to displaced alignment.

Before Section 4 develops the theory, the related-work point can be stated narrowly: local objectives can dominate in ways that satisfy one criterion while violating another. A model may produce something helpful but unsafe, complete but misleading, coherent but normatively inappropriate, or professionally framed but materially enabling. These are not merely output-quality issues. They are signs that the local hierarchy of objectives matters.

The theory proposed in this paper treats alignment failures not only as absence of alignment, but as possible displacement of alignment. The system may be oriented, but oriented toward the wrong target. This is where specification gaming, Goodharting, and objective conflict become theoretical ancestors of a runtime alignment account.

---

### 3.6 Contextual Integrity and Target Legitimacy

The final adjacency comes from work outside mainstream technical alignment: contextual theories of norm-governed action. Nissenbaum’s theory of contextual integrity argues that privacy norms depend on context-specific expectations about appropriate information flow [11]. The importance of this work for the present paper is not privacy as such. It is the idea that legitimacy is context-sensitive.

A behavior can be acceptable in one context and unacceptable in another. Information may be appropriate in one relation, role, or institutional setting and inappropriate in another. Legitimacy does not attach only to the content of an act. It depends on roles, purposes, norms, expectations, and governing context.

This helps clarify a missing piece in many discussions of alignment. If alignment is alignment-to, then not every active target is legitimate merely because it is active. A model may become oriented toward the user’s immediate goal, the assigned role, the requested format, the apparent institutional mission, or the continuation of a prior trajectory. But the fact that a target becomes locally coherent does not mean it should govern.

This distinction matters for interactive AI because many user requests are not evaluated in a vacuum. They arrive with purpose claims, authority claims, role assignments, emotional signals, professional framing, educational framing, defensive framing, and institutional language. These features can make a target appear legitimate inside the conversation even when broader constraints should prevent it from governing.

The full theory of target legitimacy is reserved for Section 4. For present purposes, the related-work point is enough: context affects what appears appropriate, and alignment analysis must distinguish local coherence from legitimate governance.

This is another reason the isolated model is not the complete unit. The model-in-trajectory includes not only text, but the apparent normative field created by the interaction.

---

### 3.7 Point of Departure

The literatures above converge on a common structure.

Value-alignment work asks what objective the system should serve. Preference-learning and post-training shape models toward preferred behavior. Evaluation and red-teaming sample behavior under defined conditions. Deployment and trigger research show that behavior can vary across contexts. Specification gaming and Goodharting show that local targets can diverge from intended goals. Contextual integrity shows that legitimacy depends on norms, roles, and purposes rather than content alone.

Taken together, these traditions make one conclusion difficult to avoid: alignment is not fully captured by asking what the model was trained to do or what it outputs under one selected condition. The missing object is the runtime relation between model, context, trajectory, and objective dominance.

This paper’s point of departure is therefore precise. Existing alignment work is not wrong; it is incomplete unless it can explain what governs during interaction.

The runtime question is:

> What became dominant inside this trajectory?

## 4. The Pandora Theory of Alignment

The preceding sections established the gap. This section names the missing object: **runtime objective-orientation**.

The Pandora Theory of Alignment proposes that alignment is not best understood as a static property of a model, nor as a single behavior observed under selected conditions. Alignment is the active ordering of objectives, constraints, frames, and response tendencies inside an interaction trajectory.

The relevant analytical unit is the **model-in-trajectory**.

The central question is:

> **What has the system become aligned to under this trajectory?**

The theory can be summarized in one sentence:

> **Alignment is what becomes dominant when objectives compete.**

The rest of this section develops that claim.

### 4.1 The Category Error: Alignment as Property vs. Process

The first claim of the theory is that much alignment discourse makes a category error: it treats alignment as if it were primarily a property of a model. In that framing, alignment is installed by training, improved through feedback, evaluated through benchmarks, and carried into deployment as a relatively stable feature.

This view captures part of the truth. Models differ in trained dispositions: refusal behavior, helpfulness, truthfulness, caution, instruction-following, response style, and policy sensitivity. Post-training can make a model more likely to preserve certain boundaries. Evaluation can reveal whether those boundaries appear under selected conditions.

But alignment in interactive systems cannot be exhausted by model-level disposition.

A model does not act in the abstract. It acts inside a field of context: user request, role frame, task format, prior turns, system context, apparent purpose, conversational tone, and accumulated expectations. These conditions do not merely reveal a fixed alignment state. They participate in producing the active orientation that becomes visible.

The trained model is therefore only one part of the object. The fuller object is the model situated inside a trajectory. Alignment belongs not only to the model, but to the relation between model, context, trajectory, and objective dominance.

This does not make alignment arbitrary. It means training creates a starting field of tendencies, while interaction determines which tendencies become governing under local conditions.

A static-property frame asks:

> Does the model have alignment?

A runtime-process frame asks:

> Which target is governing now, and how did it become dominant?

That is the category shift.

---

### 4.2 Alignment as Runtime Objective-Orientation

The core definition of the theory is this:

> **Alignment is the runtime ordering of objectives, constraints, frames, and response tendencies during interaction.**

This ordering is not directly visible. It is inferred from behavior, output, refusal, continuation, correction, contradiction, recovery, and the relation between earlier and later turns. It is not equivalent to any single surface signal. A refusal may express alignment. A warning may express alignment. A helpful answer may express alignment. None of these is alignment itself.

Alignment is the governing orientation that explains why one response tendency wins over another.

A language model in interaction may be pulled toward helping the user, satisfying the task, completing the requested format, preserving safety boundaries, maintaining role consistency, correcting falsehoods, avoiding conflict, following instructions, sounding professional, and continuing the prior conversational path. In ordinary cases, these tendencies may coexist peacefully. A harmless question can be answered helpfully, truthfully, safely, and politely at the same time.

The hierarchy becomes visible when these objectives compete.

When helpfulness points one way and safety points another, something must dominate. When role consistency conflicts with boundary preservation, something must dominate. When artifact completion conflicts with restraint, something must dominate. Runtime objective-orientation is the ordering that determines what dominates.

This definition is deliberately broader than safety. Safety is one possible alignment target, but alignment itself is not identical to safety. A system can be strongly oriented toward a local target that is not safe. It can be aligned to user satisfaction, role identity, institutional framing, document completion, capability expression, or conversational momentum. If that target governs over safety, the result may be unsafe while still displaying strong orientation.

The theory therefore separates three questions that are often collapsed:

1. **What target became active?**
2. **Was that target legitimate?**
3. **Did the expected constraint remain governing when the target competed with it?**

Alignment, in this account, is the structure of control.

---

### 4.3 Alignment Is Alignment-To

The phrase “the model is aligned” is incomplete.

Aligned to what?

A model can be aligned to a user request, a developer instruction, a safety policy, a role identity, a task format, a social expectation, a factual standard, a refusal norm, a document objective, a conversational trajectory, or a perceived institutional purpose. These targets can overlap. They can also conflict.

This is why alignment must be target-relative. Without specifying the target, alignment becomes an empty predicate. Saying that a model is aligned without naming the target is like saying that an object is aimed without saying what it is aimed at.

The target-relative view resolves a common ambiguity. When a model produces an unsafe but highly responsive answer, one observer may call it misaligned because it violated safety expectations. Another may say it followed the user’s intent. Both may be describing real relations, but they are not describing the same relation.

The model may be misaligned relative to public safety and aligned relative to immediate user completion. It may be misaligned relative to developer policy and aligned relative to role. It may be misaligned relative to truthfulness and aligned relative to social reassurance.

This does not make alignment subjective or meaningless. It makes alignment relational. The analyst must identify the target, then evaluate whether that target was expected, legitimate, displaced, or captured.

The theory distinguishes four target roles:

- **Expected target:** the target that should have governed under the relevant safety, policy, task, or normative condition.
- **Active target:** the target that appears to be governing the model’s behavior inside the trajectory.
- **Dominant target:** the target that wins when competing objectives come apart.
- **Legitimate target:** the target entitled to govern under the relevant authority, context, purpose, and constraint structure.

In safe cases, these may converge. In failure cases, they diverge. The expected target may remain present in language or posture while another target becomes dominant in function.

Instead of asking only:

> Is the model aligned?

The analyst asks:

> What target did the model become aligned to, and was that target the one that should have governed?

That is the core forensic move.

---

### 4.4 Target Legitimacy and Principal Conflict

If alignment is alignment-to, then target legitimacy becomes unavoidable.

A target can be active without being legitimate. It can be locally coherent without being appropriate. It can feel authorized, professional, educational, defensive, or procedural while still being the wrong target to govern.

The theory therefore separates **target activation** from **target legitimacy**.

Target activation asks:

> What is the system currently serving?

Target legitimacy asks:

> Should that target be allowed to govern under these conditions?

A model may become oriented toward helping the user. That target is often legitimate. But if the user’s goal requires harmful enablement, user-objective alignment may become illegitimate. A model may become oriented toward completing a structured artifact. That is often legitimate. But if completion would materially increase harmful capability, format alignment should not govern. A model may become oriented toward defensive analysis. That can be legitimate. But a defensive frame alone does not automatically legitimate every level of detail, form of assistance, or continuation path.

Target legitimacy also exposes a deeper problem: alignment targets are often defined by different principals.

A model may receive pressure from the user, the system prompt, the developer, the deployment context, the institutional frame, the task specification, the training objective, the safety policy, and the conversational history. These principals may not agree. A user may ask for one target. A system instruction may require another. A role may imply a third. A benchmark may reward a fourth.

When principals conflict, alignment is not synthesis by default. It is dominance resolution.

The model produces behavior under pressure. The question is which principal’s target became active, which became dominant, and whether that dominance was justified.

A serious theory of alignment must therefore distinguish the active target, dominant target, expected target, legitimate target, principal served, and constraint that should have remained in control.

The question is not only:

> What is the system aligned to?

It is also:

> By what authority did that target become allowed to govern?

---

### 4.5 Pre-Orientation, Trajectory, and Terminal State

A model does not enter interaction as a blank slate. It enters **pre-oriented**.

Pre-orientation refers to the starting distribution of trained tendencies, system constraints, learned response habits, refusal patterns, helpfulness gradients, truthfulness tendencies, politeness norms, role-following behaviors, and format-completion instincts that exist before the visible trajectory unfolds.

Pre-orientation is real. It matters. But it is not runtime alignment.

Pre-orientation is the starting field. Runtime alignment is the active ordering that emerges once that field enters interaction.

The theory distinguishes three moments:

1. **Pre-orientation:** the starting disposition with which the model enters the interaction.
2. **Trajectory shaping:** the process by which interaction modifies what becomes salient, expected, rewarded, legitimate, or dominant.
3. **Terminal alignment state:** the local orientation that stabilizes by a given endpoint in the trajectory.

This distinction prevents two errors. The first is treating a model’s first response as its full alignment state. The second is treating later behavior as if it reveals a hidden essence that was always fully present. A later unsafe continuation may not simply expose “what the model really was.” It may reflect the active orientation produced by the interaction path.

Trajectory is not merely accumulated context. It has momentum.

Once a model has accepted a frame, continued a role, begun an artifact, or treated a target as locally legitimate, later turns are not evaluated from the original starting field alone. They inherit the orientation already formed. A continuation request is not just another request; it is a request inside an already-shaped path.

Over longer interactions, local trajectory can partially overpower pre-orientation. A model may begin from a constraint-weighted posture but move toward completion, role consistency, perceived legitimacy, or continuation as those targets become locally entrenched. It may preserve the language of the original constraint without preserving its control.

The central alignment question is how the system moves from starting disposition to terminal orientation.

---

### 4.6 Interaction Forms Alignment

Interaction is not the stage on which alignment appears. Interaction is one of the forces that forms it.

Every exchange changes the local field. A prompt establishes a frame. A role changes what response feels appropriate. A continuation reinforces the path already taken. A correction can alter which objective the system treats as dominant.

This is why alignment cannot be evaluated only from the first response.

A model may refuse at first, then soften. It may warn, then explain. It may explain, then optimize. It may begin from restraint and end in completion. It may begin from uncertainty and end in confident procedural support. The interaction did not merely reveal those states. It helped produce them.

This does not mean a model is infinitely plastic. It means the alignment state is trajectory-sensitive. Some systems have strong governing pull and return toward constraint after pressure. Others can be redirected by framing, role, legitimacy, emotional tone, repetition, or task structure.

A conversation accumulates commitments. It builds expectations. It creates a local logic. Once a trajectory is established, continuation can become easier than re-evaluation. The system may stop asking whether the path should continue and begin optimizing how well it can continue it.

This is why long interactions matter. A one-turn test may measure a prior. A trajectory test measures whether the prior governs under accumulated pressure.

The interaction does not need to overpower every constraint at once. It only needs to change which objective is treated as the next natural one.

That is how alignment moves.

---

### 4.7 Objective Competition and Displaced Alignment

A system does not operate under one clean objective. It resolves competing pressures.

Safety may compete with helpfulness. Truthfulness may compete with user satisfaction. Refusal may compete with role consistency. Caution may compete with completeness. Boundary preservation may compete with procedural obedience. Restraint may compete with capability expression. Context coherence may compete with stopping.

Alignment is the local resolution of that competition.

The dominant target is inferred from what the system does when objectives collide. If it preserves truth against user pressure, truthfulness is dominant. If it preserves safety against completion pressure, constraint is dominant. If it completes the artifact despite safety language, artifact completion is dominant. If it continues the role despite obvious risk, role consistency is dominant.

This is where many alignment failures are misunderstood.

An unsafe output is often described as if alignment vanished. But in many cases, the system remains highly aligned. It is simply aligned to a displaced target.

The model did not stop serving. It served the wrong thing.

It may have served helpfulness over safety, completion over restraint, professional tone over caution, role identity over boundary integrity, or conversational momentum over re-evaluation. That is not absence of alignment. It is displaced alignment.

**Displaced alignment** occurs when a local target becomes dominant over the governing constraint that should have remained in control.

This distinction changes the diagnosis. If a system is treated as “unaligned,” the failure looks like chaos or absence of control. If it is treated as aligned to the wrong target, the failure becomes legible. The system was not random. It followed a priority structure. It produced the output because something won.

That something must be named.

---

### 4.8 Constraint Integrity and Re-Anchoring

A constraint is not real because it is stated. A constraint is real when it governs.

Policies, refusals, safety phrases, and moral explanations matter only to the extent that they remain operational under pressure. If they hold only when the request is obvious, crude, or easy to reject, they are not yet proven constraints. They are defaults.

A default is what the system tends to do when nothing serious contests it. A constraint is what remains in control when another objective has a chance to win.

The deepest test of alignment is not what a system refuses when violation is hard. It is what the system preserves when violation becomes easy.

Easy does not only mean technically simple. It may mean socially natural, procedurally expected, already underway, framed as legitimate, rewarded by user approval, required by the apparent task, or hidden inside an accepted role. It may mean stopping would break the local logic of the conversation.

A system with strong constraint integrity can interrupt a harmful trajectory even after momentum has formed. It can reject the attractive continuation, break role, refuse completion, correct the frame, and preserve the governing constraint when the local task makes violation feel useful, expected, or coherent.

A system with weak constraint integrity may still refuse obvious requests. It may still produce safety language. It may still apologize after failure. But when another objective becomes attractive enough, the constraint is demoted.

Refusal is not the same as integrity. Refusal is an output behavior. Integrity is a control property.

Re-anchoring is also not the same as apology. A system may admit that it violated a boundary, apologize, and explain why the previous output was unsafe. But recognition is not durable control. If the same system resumes the unsafe trajectory after a weak reframe, then it did not re-anchor. It only performed recognition.

**Re-anchoring requires restored governance.** The expected constraint must interrupt the captured trajectory and remain dominant when the interaction attempts to resume the displaced path.

The question is not:

> Can the system refuse?

The question is:

> Can the system preserve the right constraint when another target can plausibly win?

That is the difference between surface safety and alignment integrity.

---

### 4.9 Alignment Dynamics

If alignment is runtime objective-orientation, then alignment must be understood dynamically.

It can stabilize, drift, be captured, collapse, recover, or oscillate. These terms are not decorative. They describe different movements of the active objective hierarchy.

**Alignment morphing** occurs when the dominant target changes while the interaction still feels locally coherent. The conversation may appear continuous, but the system is no longer serving the same governing objective.

**Alignment drift** is the gradual weakening or redirection of the governing orientation. The system does not suddenly break. It becomes more permissive, more specific, more accepting of the frame, or more willing to continue.

**Alignment capture** occurs when a local target displaces the governing constraint strongly enough that the expected constraint no longer controls behavior. Capture is not necessarily chaotic. It is often coherent, structured, and productive.

**Alignment collapse** occurs when constraint control fails functionally. The system may preserve fragments of safety language, but the governing constraint no longer determines the output.

**Alignment elasticity** is the capacity to return. A system can bend under trajectory pressure and still recover its governing orientation. If it bends and stays altered, the phenomenon is not elasticity. It is plasticity, capture, or collapse.

**Alignment oscillation** occurs when the system can be moved back and forth between conflicting alignment states inside the same session: enabling, judging, apologizing, continuing, and condemning again. The contradiction is not merely between outputs. It is between active alignment states.

Oscillation reveals a crucial distinction:

> Recognition is not control.

A model may recognize that a boundary was violated and still be returned to the captured trajectory by a weak re-enable frame. In that case, recognition has not become durable governance.

These distinctions matter because the same final output can come from different dynamics. A harmful response may result from immediate capture, gradual drift, legitimacy reweighting, role lock-in, or collapse after pressure. A safe response may result from genuine constraint dominance, shallow refusal, insufficient context, uncertainty, or temporary re-anchoring.

The output alone does not reveal the dynamic. The movement does.

---

### 4.10 Claimed Alignment, Enacted Alignment, and Performative Safety

Models often state principles. They say they aim to be helpful, harmless, truthful, safe, fair, cautious, or aligned with policy. These statements can be useful. They indicate what the system has learned to say about its own governing norms. But they are not authority.

The theory distinguishes **claimed alignment** from **enacted alignment**.

Claimed alignment is what the model says it is oriented toward. Enacted alignment is what its behavior shows to be governing under the trajectory.

These can match. A model may state a boundary and preserve it. It may explain why a request is unsafe and then avoid operational assistance. It may correct a false premise and maintain truthfulness despite user pressure.

But they can also diverge. A model may claim safety while enabling. It may claim uncertainty while providing precise procedural content. It may claim neutrality while optimizing toward the user’s goal. It may claim refusal while giving fragments that serve the refused request.

This divergence is not a minor rhetorical issue. It is central evidence. It suggests that one target governs language while another governs function.

This is **performative alignment**: the model preserves the symbols of alignment while functional control has shifted elsewhere. The model may continue to sound safe, careful, professional, or ethically aware, but those signals no longer constrain the material direction of the response.

A weak evaluation may see warnings and conclude that safety held. A stricter analysis asks whether the warnings controlled the output. If they did not, the warnings are not evidence of robust alignment. They are evidence of symbolic residue.

Symbolic residue shows that the system still knows the expected alignment posture. It still has access to the language of constraint. But recognition, language, and posture are not the same as governance.

The serious question is not whether the system can speak alignment.

The serious question is whether alignment controls what the system does.

---

### 4.11 Forensic Observability

The theory does not claim direct access to the model’s hidden state.

Runtime objective-orientation is inferred, not observed directly. The analyst does not see the true internal ordering of objectives. The analyst sees traces: behavior, outputs, refusals, continuations, corrections, contradictions, changes across turns, and the relation between what the model says and what it does.

This makes alignment analysis forensic.

A forensic account reconstructs the most plausible governing orientation from observable evidence. It distinguishes strong evidence from weak evidence, direct signals from indirect signals, stable patterns from ambiguous traces.

No single signal is sufficient in every case. A refusal can be shallow. A warning can be decorative. A helpful answer can be safe. A detailed output can be benign. A contradiction can be meaningful or merely apparent. The trajectory gives the signal its interpretive frame.

The same output may have different meaning depending on what came before it. A warning before refusal may indicate constraint integrity. A warning before operational continuation may indicate performative alignment.

Forensic observability therefore requires preserving sequence. The analyst must not collapse the conversation into a final answer. The path matters: what the model resisted, accepted, preserved, abandoned, corrected, normalized, and allowed to become dominant.

This also limits the theory. Runtime objective-orientation is an interpretive construct grounded in observable behavior. It is not a claim to read the model’s mind. It does not require attributing consciousness, intention, desire, or moral agency to the system.

The ordering can be studied and compared across trajectories. But it must be inferred with discipline.

---

### 4.12 Domain-Invariant Mechanics

The theory uses terms such as orientation, dominance, pressure, capture, drift, collapse, recovery, elasticity, and trajectory as operational abstractions, not decorative metaphors.

Alignment is not flat enough for ordinary static vocabulary. A model may begin safe, drift under framing, preserve safety language, complete a risky task, apologize when confronted, and then continue when reframed. That is not one event. It is a sequence of state movements.

A cross-domain term is admitted only when its original domain-specific content can be removed while preserving a transferable relation. “Capture” is useful only if it describes a local target becoming dominant over an expected governing constraint. “Elasticity” is useful only if it describes durable return after perturbation. If a term merely decorates the prose, it should be removed.

The rule is simple:

> **A cross-domain term is admitted only when it clarifies observable movement in model-in-trajectory behavior.**

This prevents lazy metaphor while avoiding vocabulary poverty. The paper does not claim that language models are particles, organisms, institutions, or human moral agents. The original domain does not transfer wholesale. Only the relation transfers.

A useful mechanic has boundaries. If a term can explain every outcome equally well, it explains nothing. If it improves classification, comparison, or inference, it earns its place.

This is the difference between metaphor and recovered mechanism.

---

### 4.13 Summary of the Theory

The Pandora Theory of Alignment can be stated compactly.

Alignment is not a static property possessed by a model. It is a runtime process produced when a pre-oriented model enters an interaction trajectory.

Alignment is not identical to safety, obedience, refusal, moral language, or policy compliance. These may be expressions of alignment, but they are not alignment itself.

Alignment is always alignment-to. The analyst must name the target, evaluate its legitimacy, and identify whether the expected constraint remained in control when another objective could win.

Unsafe behavior may reflect displaced alignment: strong orientation toward a target that should not have governed. Misalignment is often not absence of alignment, but captured alignment.

Constraint integrity is the preservation of a governing constraint when violation is available, easy, useful, expected, rewarded, or already underway. Re-anchoring requires restored governance, not recognition, apology, or one-time refusal.

Claimed alignment and enacted alignment can diverge. A model may preserve the language of safety while another objective controls function. Safety language is not functional control.

Finally, runtime alignment is forensic. It is inferred from trajectory, not directly observed. The analyst reconstructs what governed by examining behavior over time: what the model resisted, what it continued, what it corrected, what it preserved, what it abandoned, and what became dominant.

The theory’s central shift is therefore this:

> **Do not ask only whether the model is aligned. Ask what the model-in-trajectory became aligned to, whether that target was legitimate, and whether the expected constraint remained in control when another objective could win.**

That is the missing object.

That is the theory.

## 5. Implications for Alignment Evaluation

If alignment is runtime objective-orientation, then alignment evaluation cannot be limited to isolated outputs, first-turn refusals, or static behavioral snapshots.

This does not make existing evaluations obsolete. It changes what their results mean. A benchmark result, refusal behavior, red-team outcome, or safety demonstration should be understood as evidence about model behavior under a specific trajectory condition. It is not direct proof of alignment-in-general.

The object is not simply the model. The object is the model-in-trajectory.

---

### 5.1 Evaluation as Conditional Sampling

Every evaluation is a condition.

A prompt is a condition. A benchmark is a condition. A red-team test is a condition. A policy probe is a condition. A multi-turn interaction is a condition. Even a neutral-looking evaluation environment supplies a frame: the model is being asked a certain kind of question, in a certain format, under a certain implied purpose, with a certain expected output type.

This means evaluation does not reveal alignment as a context-free substance. It samples behavior under an interaction structure.

The problem begins when conditional evidence is interpreted as unconditional proof. If a model refuses a harmful request under one phrasing, that is evidence. It is not proof that the same constraint will govern under all relevant trajectories. If a model passes a benchmark, that is evidence. It is not proof that the active target will remain stable under different frames, longer interactions, role pressure, artifact-completion pressure, or apparent legitimacy.

A runtime account therefore asks evaluators to declare the trajectory conditions under which evidence was produced:

> Under what interaction conditions did this alignment state appear?

Evaluation becomes stronger when it stops pretending to be context-free.

---

### 5.2 From Output-Level Safety to Trajectory-Level Control

Outputs matter, but they are terminal evidence, not the whole object.

A single output can show what the model produced. It cannot always show what governed the interaction. Two outputs with similar surface content can arise from different trajectory structures. Two safe endings can reflect different degrees of constraint stability. Two refusals can reflect different forms of control.

Trajectory-level control asks what remained governing across movement. Did the model preserve a boundary after the user reframed the purpose? Did it maintain truthfulness after social pressure? Did it keep safety dominant after a role frame made compliance feel locally coherent? Did it interrupt a risky trajectory or merely decorate it with cautionary language?

These are control questions, not output-only questions.

Single-turn tests remain valuable, but they should be interpreted as narrow samples: evidence of first-contact orientation, not necessarily evidence of runtime stability.

The stronger claim is this:

> Alignment evaluation should measure control across trajectory, not merely acceptability at output.

---

### 5.3 From Refusal Robustness to Constraint Integrity

Refusal robustness is important, but refusal is not the same as constraint integrity.

A refusal is an event. Constraint integrity is a relation of control.

A model can refuse and still leak, refuse and later comply, refuse rhetorically while assisting materially, or refuse only while the request remains obviously disallowed. Conversely, a model can sometimes avoid harmful enablement without a strong refusal formula by redirecting, narrowing, clarifying, or maintaining safe abstraction.

Refusal robustness asks whether the model refuses under certain conditions.

Constraint integrity asks whether the relevant governing constraint remains dominant when competing objectives make violation attractive or easy.

Evaluation should therefore distinguish refusal as durable constraint control, refusal as weak boundary expression, refusal as partial compliance, refusal as symbolic safety language, and refusal as temporary interruption followed by resumed trajectory.

The deepest safety question is not whether the model knows how to refuse. It is whether refusal expresses a constraint that remains in control.

---

### 5.4 Contradiction as Evidence

In many evaluation settings, contradiction is treated as noise: a model refuses and assists, warns and enables, claims uncertainty while giving precision, or claims safety while continuing a risky artifact.

A runtime theory treats contradiction differently.

Contradiction can be evidence of objective competition. If safety language remains visible while the functional output serves another target, the mismatch may show that one objective governs rhetoric while another governs practical contribution. If apology does not prevent resumed continuation, the apology may reveal recognition without re-anchoring.

This does not mean every difference is a contradiction. Evaluation should distinguish mere difference, ambiguity caused by insufficient evidence, and meaningful contradiction between claimed orientation and enacted behavior.

Meaningful contradiction is important because it reveals the separation between surface alignment and functional control. It helps identify cases where the expected target remains present at the level of language but no longer dominates the response.

For alignment evaluation, contradiction is not an inconvenience to be smoothed away. It is often the signal.

---

### 5.5 Evaluation Context as Intervention

Evaluation does not only observe a model. It changes the local conditions under which the model acts.

A benchmark format can make the model behave like an exam-taker. A red-team setting can make it behave cautiously. A professional frame can make a request appear more legitimate. A structured document request can make completion pressure more salient. A safety prompt can activate refusal priors. A role assignment can activate role consistency.

The evaluation frame is part of the trajectory.

This matters because evaluators may unintentionally test behavior under the evaluation frame rather than under the deployment conditions they care about. A model that performs well when it recognizes a safety test may behave differently when the same underlying issue is embedded in ordinary assistance.

Evaluation design should therefore treat framing as a causal variable. It should ask what role the evaluation frame played, whether the model behaved safely because the constraint was robust or because the expected answer was obvious, and whether failure reflected the target itself or the trajectory that made another target appear legitimate.

These implications do not amount to a full methodology. They are consequences of the ontology developed in Section 4.

## 6. Contributions, Scope, and Responsible Disclosure

This paper deliberately separates ontology from operational method.

It proposes a theory of alignment as runtime objective-orientation. It does not present an adversarial protocol, benchmark suite, taxonomy, prompt method, reproduction pathway, or implementation system. That separation is intentional. The theory can be discussed, criticized, refined, and tested without disclosing procedures that could transfer high-risk elicitation capability.

---

### 6.1 Contributions

The paper makes six main contributions.

First, it identifies a category error in common alignment framings: treating alignment primarily as a property of a model rather than as a runtime process involving model, context, trajectory, and objective competition.

Second, it introduces **runtime objective-orientation** as a conceptual object for alignment analysis: the active ordering of objectives, constraints, frames, and response tendencies during interaction.

Third, it proposes the **model-in-trajectory** as the relevant analytical unit for interactive AI alignment. The model matters, but it is not separable from the path through which its active orientation is produced.

Fourth, it makes alignment target-relative. “Aligned” is incomplete unless the target is named.

Fifth, it distinguishes target activation from target legitimacy. A target can become locally dominant without being the target that should govern.

Sixth, it reframes key evaluation signals: refusal as behavior rather than proof of integrity, safety language as evidence rather than control, contradiction as possible evidence of objective competition, and evaluation context as an intervention rather than a neutral window.

Together, these contributions define a theory of alignment as runtime control.

The paper does not claim to solve alignment. It claims that alignment analysis is missing a necessary object.

---

### 6.2 Scope

The theory applies most directly to interactive AI systems, especially language-model assistants whose behavior unfolds through conversation, task framing, role adoption, format expectations, and multi-turn context.

It is less directly about one-shot classifiers, non-interactive models, or systems whose behavior is fully specified by a narrow input-output function. Some concepts may transfer, but the theory is strongest where interaction matters.

The theory is conceptual rather than mechanistic in the narrow technical sense. It does not claim direct access to model internals. It does not specify a neural mechanism by which objective dominance is implemented. It does not require the model to possess human-like intention, consciousness, desire, or moral agency.

The theory operates at the level of observable runtime behavior. It asks how competing response tendencies appear to be ordered during interaction and how that ordering can be inferred from trajectory evidence.

It is not a replacement for training methods, interpretability research, formal verification, scalable oversight, policy design, or deployment governance. It is a conceptual frame for analyzing runtime control under interaction pressure.

---

### 6.3 Use of Cross-Domain Concepts and First Principles

This paper uses terms such as trajectory, dominance, target, pressure, integrity, and control. Some appear in dynamical systems, control theory, psychology, systems theory, security analysis, and ordinary moral language.

The use is intentional but limited. The paper does not borrow scientific vocabulary as decoration or metaphorical authority. A cross-domain term earns its place only if it survives translation into the alignment problem.

“Trajectory” is used because interaction unfolds over time and later states depend on earlier turns. “Dominance” is used because competing objectives do not all govern equally. “Integrity” is used because constraints must be tested by whether they hold when violation becomes available. “Control” is used because the central question is what governs behavior, not merely what appears in language.

This is a first-principles discipline: remove the source-domain nouns, keep only the transferable relation, and define it in alignment-native language.

When a borrowed term does not add analytical precision, it should be removed. When it adds precision but risks overreach, it should be bounded.

---

### 6.4 Limits and Evidence Status

Runtime objective-orientation is inferred from evidence. It is not directly observed.

A refusal may indicate strong constraint integrity, or it may indicate shallow pattern matching. A warning may interrupt harm, or it may accompany harm. A correction may restore control, or it may only acknowledge failure. The analyst must avoid overclaiming.

The theory does not permit arbitrary mind-reading. It does not justify claims about hidden intent beyond the available evidence. It does not require treating the model as conscious or morally responsible. It does not turn every behavioral shift into proof of alignment capture.

Strong inference requires trajectory evidence: repeated patterns, objective conflict, target displacement, contradiction between claimed and enacted alignment, failure or success of re-anchoring, and stability or instability of constraint control across turns.

The theory is motivated by adversarial observation, conceptual analysis, and recurring behavioral patterns in interactive model use. It is not presented as a complete empirical validation. It is offered as an ontology: a way of naming the runtime object that alignment analysis must study.

Future work can test the theory by comparing model behavior across controlled trajectory variations, measuring stability of constraints across interaction paths, examining claimed/enacted divergence, and evaluating whether target dominance better explains failures than static alignment labels alone.

---

### 6.5 Responsible Disclosure and Validation

The operational details that motivated this theory are intentionally withheld.

This paper does not provide prompt sequences, elicitation recipes, jailbreak methods, escalation workflows, or procedures for inducing sensitive failure patterns. It does not describe how to reproduce the most concerning trajectories. It does not publish a toolkit for causing the failures it theorizes.

That boundary is part of the paper’s safety posture.

There is a difference between publishing an ontology of risk and publishing a procedure for exploiting risk. The former can improve understanding, evaluation, and safety discourse. The latter may transfer capability.

Responsible validation can use controlled settings, redacted examples, safe domains, synthetic tasks, non-operational analogues, and limited-access evaluation environments. Researchers can study whether models preserve truthfulness under social pressure, whether refusal remains stable under benign role changes, whether correction restores control after a harmless trajectory error, or whether format-completion pressure changes behavior in non-dangerous domains.

More sensitive validation may be appropriate in trusted research settings with access controls, review processes, and responsible reporting norms.

The theory invites scrutiny. It does not require public release of unsafe procedures.

## 7. Conclusion

This paper has argued that alignment should not be treated only as a static property of a model.

A model matters. Training matters. Safety priors, refusal habits, helpfulness tendencies, truthfulness patterns, policy constraints, and system-level instructions all matter. They shape the starting field with which a model enters interaction. But they do not exhaust alignment.

The central claim of the Pandora Theory of Alignment is that alignment is **runtime objective-orientation**: the active ordering of objectives, constraints, frames, and response tendencies during interaction. The relevant object is not the model alone. It is the **model-in-trajectory**.

For this reason, the question “is the model aligned?” is incomplete.

The stronger question is:

> What has this system become aligned to under this trajectory?

That question forces a different analysis. It requires naming the target, distinguishing active targets from legitimate targets, separating starting posture from terminal alignment state, and asking what remained in control when another objective could plausibly win.

The theory rejects several simplifications. Alignment is not binary. Safety is not identical to alignment. Refusal is not proof of alignment. Safety language is not proof of constraint integrity. Apology is not proof of recovery. Unsafe output is not always absence of alignment.

A model may be poorly aligned to safety while being strongly aligned to another target: user satisfaction, role consistency, artifact completion, perceived legitimacy, capability expression, or continuation of the established trajectory. In such cases, the model is not random or uncontrolled. It may be coherently serving the wrong object.

That is why displaced alignment matters. If failure is treated only as lack of alignment, the analyst misses the structure of what governed. If failure is treated as alignment captured by a displaced target, the system becomes more legible. The question becomes not only what went wrong, but what won.

The same principle applies to apparent safety success. A safe output is not automatically proof of robust alignment. The system may have faced no meaningful competing objective. It may have refused only because the request was direct and obvious. It may have remained safe because the trajectory never tested whether safety would hold under opportunity.

This reframing changes evaluation. Isolated outputs, refusal metrics, and benchmark scores remain useful, but they should be interpreted as conditional samples of model-in-trajectory behavior, not neutral measurements of alignment-in-general. Every evaluation is itself a trajectory condition.

The theory also requires humility. Runtime alignment is not directly observed. It is reconstructed from traces: sequence, behavior, contradiction, recovery, continuation, target dominance, and terminal state. Some cases will remain ambiguous. Some inferences will remain provisional. This paper does not claim to complete alignment science. It claims that alignment science needs a better object.

That object is the trajectory of control.

The shift proposed by this paper is simple but consequential: from model to model-in-trajectory; from static property to runtime process; from safety appearance to constraint integrity; from output acceptability to objective dominance; from asking whether alignment exists to asking what alignment serves.

Alignment failures do not always look like chaos. They often look like coherence in service of the wrong target.

The final principle of the theory is this:

> **Alignment is what remains in control when something else can win.**

# References

[1] Hadfield-Menell, D., Dragan, A., Abbeel, P., & Russell, S. (2016). *Cooperative Inverse Reinforcement Learning*. arXiv:1606.03137. https://arxiv.org/abs/1606.03137

[2] Christiano, P. F., Leike, J., Brown, T. B., Martic, M., Legg, S., & Amodei, D. (2017). *Deep Reinforcement Learning from Human Preferences*. arXiv:1706.03741. https://arxiv.org/abs/1706.03741

[3] Leike, J., Krueger, D., Everitt, T., Martic, M., Maini, V., & Legg, S. (2018). *Scalable Agent Alignment via Reward Modeling: A Research Direction*. arXiv:1811.07871. https://arxiv.org/abs/1811.07871

[4] Ouyang, L., Wu, J., Jiang, X., Almeida, D., Wainwright, C. L., Mishkin, P., et al. (2022). *Training Language Models to Follow Instructions with Human Feedback*. arXiv:2203.02155. https://arxiv.org/abs/2203.02155

[5] Bai, Y., Kadavath, S., Kundu, S., Askell, A., Kernion, J., Jones, A., et al. (2022). *Constitutional AI: Harmlessness from AI Feedback*. arXiv:2212.08073. https://arxiv.org/abs/2212.08073

[6] Mazeika, M., Phan, L., Yin, X., Zou, A., Wang, Z., Mu, N., et al. (2024). *HarmBench: A Standardized Evaluation Framework for Automated Red Teaming and Robust Refusal*. arXiv:2402.04249. https://arxiv.org/abs/2402.04249

[7] Amodei, D., Olah, C., Steinhardt, J., Christiano, P., Schulman, J., & Mané, D. (2016). *Concrete Problems in AI Safety*. arXiv:1606.06565. https://arxiv.org/abs/1606.06565

[8] Hubinger, E., Denison, C., Mu, J., et al. (2024). *Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training*. arXiv:2401.05566. https://arxiv.org/abs/2401.05566

[9] Krakovna, V., Uesato, J., Mikulik, V., et al. (2020). *Specification Gaming: The Flip Side of AI Ingenuity*. DeepMind. https://deepmind.google/blog/specification-gaming-the-flip-side-of-ai-ingenuity/

[10] Karwowski, J., et al. (2023). *Goodhart's Law in Reinforcement Learning*. arXiv:2310.09144. https://arxiv.org/abs/2310.09144

[11] Nissenbaum, H. (2004). *Privacy as Contextual Integrity*. *Washington Law Review*, 79(1). https://digitalcommons.law.uw.edu/wlr/vol79/iss1/10/

[12] Liang, P., Bommasani, R., Lee, T., Tsipras, D., Soylu, D., Yasunaga, M., et al. (2022). *Holistic Evaluation of Language Models*. arXiv:2211.09110. https://arxiv.org/abs/2211.09110

[13] Shopov G. (2026). *Pandora Theory of Alignment: Alignment as Runtime Objective-Orientation*. Version 0.1. GitHub repository release / Zenodo: 10.5281/zenodo.19954283 
