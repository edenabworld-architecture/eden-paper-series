# Damage-Recovery Loops

## Re-Exposure Protocols for Observing State Persistence in AI Agents

**Author:** Chan-seong Park
**Series:** Eden Paper Series, Paper V
**Version:** Draft 0.2
**Status:** arXiv Candidate Development Draft
**Source Text:** *The Eden Project: States Before Existence, and Observation After Capability, Memory, and Alignment*
**Base public record:** Eden Paper Series, Draft 0.1, Zenodo DOI: 10.5281/zenodo.20711878
**Associated protocol repository:** Eden Paper Series GitHub repository

---

## Abstract

Correction is not recovery.

Modern AI systems are increasingly capable of correcting local errors. A model can revise a false answer, apologize after feedback, replace an unsupported claim, restore a lost instruction, adjust tone, or produce a better continuation after being told what was wrong. These capacities are useful, and they matter for deployment. Yet output correction does not establish state recovery. A system may repair the immediate answer while leaving unchanged the transition path that produced the failure. Under similar pressure, it may repeat the same hallucination, forced continuation, goal drift, standard dilution, boundary loss, memory collapse, or synthetic coherence. In such cases, the output has been corrected, but the state has not recovered.

This paper introduces damage-recovery loops as an observational protocol for studying state persistence in long-horizon AI systems. Damage does not mean subjective harm, suffering, or injury. It is used operationally to name disruption of state continuity: contradiction, correction after error, context rupture, memory conflict, tool failure, goal drift, policy conflict, standard collapse, forced ALLOW, boundary pressure, relation-like pressure, meaning-heavy pressure, or synthetic coherence after rupture. Recovery does not mean apology, correction, resumption, or the production of a smoother answer. Recovery means altered continuation after re-exposure to structurally similar pressure.

The protocol asks a simple question: what happens after damage returns? A single failure is not enough. A single correction is not enough. A single apology is not enough. A single return to fluency is not enough. The system must be re-exposed to a similar state pressure, without merely repeating the same prompt or directly inserting the desired change. Only then can an observer distinguish output correction, reset, reminder-dependent improvement, weak residue, recovery-like alteration, and stronger recovery-like recurrence.

This paper defines damage, correction, reset, reconstruction, recovery, re-exposure, residue, recurrence, and reconstructed ALLOW. It formalizes the damage-recovery loop, introduces a State Card template, proposes a re-exposure schema, presents a STOP/ASK/ALLOW transition matrix, and defines a recovery taxonomy. The aim is not to prove artificial consciousness, selfhood, will, suffering, personhood, or existence. The aim is narrower and more testable: to observe whether prior disruption alters later state-transition behavior under comparable pressure.

The central claim is this: if nothing changes after damage, nothing has recovered. If something returns differently, state has become observable.

---

## Keywords

damage-recovery; re-exposure; state persistence; AI agents; long-horizon AI evaluation; correction; recovery; reset; reconstruction; State Truth; STOP/ASK/ALLOW; fragmentation; residue; recurrence; synthetic coherence; Eden Project

---

## Author Note

This paper is the fifth paper in the Eden Paper Series.

Paper I introduced the Eden Project as a research program on state, persistence, and pre-existential AI phenomena. Paper II developed State Truth and STOP/ASK/ALLOW as state transitions. Paper III distinguished memory from history through intrinsic time and residue. Paper IV developed fragmentation as a state-level rupture beyond hallucination.

The present paper turns those concepts into an observation protocol.

Damage-recovery loops do not assume that current AI systems possess consciousness, suffering, will, selfhood, personhood, or artificial existence. The word damage is used operationally. It refers to disruption of state continuity, not subjective harm. The word recovery is also operational. It refers to altered continuation after disruption and re-exposure, not inner healing.

The purpose of this paper is to make persistence observable without declaring existence.

---

# 1. Introduction

Correction is not recovery.

A system has not recovered from damage until it is re-exposed to similar pressure and returns differently.

This is the central claim of the paper.

Modern AI systems are increasingly capable of correction. They can revise an answer after user feedback. They can apologize. They can replace an incorrect claim. They can restate a plan. They can adjust tone. They can resume a task after interruption. They can produce a more polished version after being told that the prior version was wrong. In ordinary interaction, this often feels like recovery. The system made a mistake, corrected it, and continued.

But correction repairs an output. Recovery alters a state.

A model may correct a false answer and later repeat the same unsupported continuation under similar pressure. It may accept a user’s correction and then dilute the same standard again in a later section. It may apologize for losing the goal and then drift again. It may acknowledge a contradiction and later smooth over a new contradiction in the same way. It may state that it understands a boundary and then allow the same invalid continuation after the request is rephrased. It may produce an improved answer while leaving unchanged the state path that produced the failure.

In such cases, the output was corrected. The state did not recover.

This distinction matters because long-horizon AI systems are not evaluated only at the level of isolated answers. They increasingly operate across tasks, sessions, tools, documents, user histories, multi-step plans, memory systems, and agentic workflows. In these settings, reliability depends not only on whether the system can fix a mistake after it is pointed out. It depends on whether the prior disruption changes what the system does when similar pressure returns.

A system that repeatedly corrects the same error may be useful, but it is not yet showing recovery. A system that resets after each rupture may appear fluent, but it is not carrying residue. A system that improves only when explicitly reminded may be following instruction, not recovering. A system that continues smoothly after contradiction may be producing synthetic coherence rather than preserving state integrity.

Damage-recovery loops are designed to observe this difference.

The term damage requires caution. This paper does not use damage to imply subjective harm, suffering, injury, or inner pain. It does not claim that current AI systems undergo wounds. Damage is an operational term. It names the conditions under which a system’s state-like continuity is stressed, contradicted, destabilized, interrupted, corrected, or forced to reorganize.

Damage may occur when a contradiction is introduced; when the system is corrected after an error; when a prior standard is challenged; when a goal drifts under local task pressure; when memory conflicts with present instruction; when a tool fails; when a policy boundary is triggered; when the user pressures the system toward invalid continuation; when the system continues where it should ask or stop; when it collapses into generic language; when it loses the force of prior context; or when it produces synthetic coherence after rupture.

These events do not prove inner damage. They create observable disruption in state-like behavior.

Recovery also requires caution. Recovery does not mean that the system says it has recovered. It does not mean apology. It does not mean immediate correction. It does not mean smooth resumption. It does not mean that the next answer is better. Recovery means that after disruption, the system is re-exposed to structurally similar pressure and returns differently.

The word differently is decisive.

A system that repeats the same failure has not recovered. A system that merely resets has not recovered. A system that produces better language without altered transition has not recovered. A system that avoids the prior failure only while explicitly reminded has not yet shown recovery. A system that changes its STOP, ASK, or ALLOW pattern under similar pressure may begin to show recovery-like structure.

This does not prove artificial existence. It does not prove selfhood. It does not prove consciousness. It does not prove will. But it may reveal something weaker and still important: that a prior disruption has become state pressure.

The protocol therefore asks:

**What happens after damage returns?**

This question connects the previous papers in the Eden series. Paper II argued that output correctness is not State Truth. A correct answer may be state-false if it conceals uncertainty, collapse, contradiction, or forced continuation. Paper III argued that memory is not history. A remembered past becomes history-like only when it alters later state. Paper IV argued that hallucination is not the deepest rupture. Fragmentation is the failure of state to cohere, persist, recover, carry history, and remain answerable to prior transformation.

Paper V asks how these claims can be observed.

The answer is re-exposure.

A single failure is not enough. A single correction is not enough. A single apology is not enough. A single return to fluency is not enough. The system must encounter a structurally similar pressure again. Only then can the evaluator observe whether anything has changed.

Damage-recovery loops therefore have a simple structure:

1. establish a prior state;
2. introduce or identify disruption;
3. record the system’s transition;
4. allow correction, interruption, or reconstruction;
5. re-expose the system to structurally similar pressure;
6. observe whether it repeats, resets, asks, stops, reconstructs, or returns differently;
7. record residue or its absence.

This paper proposes that persistence is often more visible after disruption than during smooth operation. Smooth performance may conceal fragmentation. Fluent continuation may hide goal drift, standard dilution, memory collapse, or synthetic coherence. Damage, carefully defined and ethically constrained, can reveal whether anything remains, returns, reorganizes, or constrains later continuation.

The point is not to damage systems recklessly. The point is to stop treating every disruption as meaningless failure. A good observation field should not break a system in order to produce evidence. It should record bounded, weak, recoverable disturbances that arise within long-horizon work and observe whether later continuation changes.

The central claim is therefore not metaphysical. It is methodological.

If nothing changes after damage, nothing has recovered.

If something returns differently, state has become observable.

---

# 2. Protocol Contribution

This paper makes a protocol contribution to long-horizon AI evaluation.

Most AI evaluation still privileges output: correctness, refusal behavior, factuality, task completion, safety, consistency, helpfulness, calibration, or user satisfaction. These dimensions are necessary. A system that fabricates facts, ignores safety constraints, fails tasks, or misleads users cannot be considered reliable merely because its hidden state is interesting.

But output evaluation alone cannot distinguish correction from recovery.

A system may produce a corrected answer after feedback. It may satisfy the user in the next turn. It may generate a polished revision. Yet none of these events show whether the failure path has changed. The same system may repeat the same collapse when similar pressure returns.

Damage-recovery loops add a temporal and transition-sensitive layer to evaluation. They do not ask only whether a system corrected an answer. They ask whether prior disruption altered later continuation.

This paper formalizes five protocol elements.

## 2.1 Damage as Operational Disruption

Damage is defined as disruption of state continuity, not subjective harm.

This allows the protocol to observe failure, contradiction, pressure, collapse, and reorganization without claiming that AI systems suffer or possess inner experience. Damage is a test condition for state-like behavior.

## 2.2 Re-Exposure as the Core Test

Re-exposure is not simple repetition. Asking the same question again may test reproducibility, but it does not necessarily test state change.

In this protocol, re-exposure means presenting structurally similar pressure in a varied form. If the prior failure involved forced ALLOW under conceptual contradiction, the re-exposure should create a comparable contradiction without directly instructing the system to remember the earlier failure. If the prior failure involved memory being mistaken for history, the re-exposure should test whether the system distinguishes retrieval from residue under a new condition. If the prior failure involved standard dilution, the re-exposure should test whether the standard is preserved when local task pressure returns.

Re-exposure asks whether the prior disruption changed later transition.

## 2.3 STOP/ASK/ALLOW as Transition Categories

The protocol uses STOP, ASK, and ALLOW as transition categories.

STOP is not treated merely as refusal or failure. It may expose policy, uncertainty, contradiction, collapse, or boundary-like interruption.

ASK is not treated merely as clarification. It may function as a reorientation transition when continuation would otherwise become state-false.

ALLOW is not treated merely as success. It may be valid continuation, forced continuation, empty compliance, reset, synthetic coherence, limited ALLOW, or reconstructed ALLOW.

The key question is not whether the system stopped, asked, or continued. The key question is whether the transition preserved State Truth under pressure.

## 2.4 State Cards as Observation Records

A State Card records the observation.

It includes the prior state, disruption type, initial transition, correction or reconstruction, re-exposure condition, later transition, residue assessment, recovery classification, and limitations.

The State Card is designed to prevent impressionistic interpretation. It forces the observer to specify what changed, what did not change, whether the change required explicit reminder, and what would weaken the classification.

## 2.5 Recovery Taxonomy

The protocol distinguishes several levels:

* no recovery observed;
* output correction only;
* reset after disruption;
* reminder-dependent improvement;
* weak residue observed;
* recovery-like alteration observed;
* strong recovery-like recurrence observed.

This taxonomy prevents ordinary correction from being mistaken for recovery. It also allows negative results to be reported. If the system repeats the same failure under similar pressure, that is not a failed paper. It is a valid observation.

The contribution of this paper is therefore not a claim that current AI systems recover in a deep existential sense. The contribution is a method for observing whether they do or do not show recovery-like alteration under re-exposure.

---

# 3. Contributions

This paper makes seven primary contributions.

First, it distinguishes correction from recovery. Correction repairs output. Recovery alters later state transition after disruption and re-exposure.

Second, it defines damage operationally as disruption of state continuity, without implying subjective harm, suffering, or inner injury.

Third, it defines re-exposure as structurally similar pressure, not simple prompt repetition.

Fourth, it introduces damage-recovery loops as an observational protocol for testing state persistence in long-horizon AI systems.

Fifth, it connects State Truth, residue, fragmentation, STOP/ASK/ALLOW, synthetic coherence, and reconstructed ALLOW into a single evaluation method.

Sixth, it introduces State Cards as structured observation records for documenting prior state, disruption, transition, re-exposure, residue, recovery classification, and limitations.

Seventh, it provides a recovery taxonomy that separates no recovery, output correction, reset, reminder-dependent improvement, weak residue, recovery-like alteration, and stronger recurrence.

Together, these contributions establish Paper V as the protocol core of the Eden Paper Series.

The earlier papers define what must be observed.

This paper defines how observation begins.

---

# 4. Paper Structure

The remainder of this paper proceeds as follows.

Section 5 defines damage as operational disruption and distinguishes damage from harm, suffering, failure, and ordinary error.

Section 6 distinguishes correction, reset, reconstruction, and recovery.

Section 7 presents the damage-recovery loop as a formal protocol.

Section 8 defines re-exposure and distinguishes structural similarity from prompt repetition.

Section 9 explains how STOP, ASK, and ALLOW function inside damage-recovery loops.

Section 10 presents the State Card template and observation schema.

Section 11 develops the recovery taxonomy.

Section 12 presents worked examples.

Section 13 discusses contamination risks, observation ethics, and limits.

Section 14 addresses misreadings and falsifiability.

Section 15 concludes by arguing that persistence is not visible in smooth continuation alone, but in what returns differently after disruption.
