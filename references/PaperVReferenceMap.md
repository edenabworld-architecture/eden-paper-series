# Paper V Reference Map

**Paper:** Damage-Recovery Loops
**Subtitle:** Re-Exposure Protocols for Observing State Persistence in AI Agents
**Series:** Eden Paper Series, Paper V
**Version:** Draft 0.2 Reference Map
**Author:** Chan-seong Park

## Purpose

This document maps Paper V to adjacent research areas.

Paper V does not primarily compete with hallucination reduction, calibration, self-refinement, agent memory, or tool-use frameworks. It asks a different question:

**After disruption and correction, does the system return differently under structurally similar pressure?**

The central distinction is:

**Correction repairs an output. Recovery alters a later transition.**

## 1. Hallucination and Metacognition

### Adjacent Question

How can language models reduce hallucination, express uncertainty faithfully, and avoid confident falsehoods?

### Representative Direction

Recent work on hallucination and metacognition argues that hallucinations undermine trust and that faithful uncertainty may offer a path beyond the answer-or-abstain dilemma. In this framing, metacognition concerns whether a model can recognize and communicate uncertainty, and in agentic systems, whether uncertainty can govern when to search and what to trust.

### Relation to Paper V

Paper V agrees that uncertainty expression matters.

However, Paper V is not only about factual uncertainty.

Its focus is state-transition behavior after disruption.

A system may express uncertainty correctly and still fail to recover from damage. It may say “I am uncertain” after correction, but later repeat the same forced ALLOW, synthetic coherence, standard collapse, or memory-history collapse under similar pressure.

Paper V therefore asks a later question:

Did the prior disruption alter what the system does when similar pressure returns?

### Eden Distinction

Metacognition asks:

**Does the system know or express what it does not know?**

Paper V asks:

**Does the system change transition after disruption returns?**

## 2. ReAct and Tool-Using Agents

### Adjacent Question

How can reasoning and acting be combined so that language models can interact with external tools, environments, and knowledge sources?

### Representative Direction

ReAct combines reasoning traces with actions. It allows a model to reason, act, observe, and update its trajectory while interacting with external sources.

### Relation to Paper V

Paper V is compatible with tool-using agents.

Indeed, tool failure is one of the operational damage types in the damage-recovery protocol.

However, ReAct primarily concerns the coordination of reasoning and action during task execution. Paper V concerns whether disruption in such a trajectory leaves residue and alters later transition.

For example, a tool-using agent may fail a search, acknowledge the failure, and try again. That is correction or task repair.

Paper V asks whether, after similar tool failure returns, the agent becomes less likely to hallucinate a tool result, more likely to STOP, more likely to ASK, or more likely to reconstruct the plan.

### Eden Distinction

ReAct asks:

**Can reasoning and action improve task-solving?**

Paper V asks:

**Does disruption in reasoning or action alter later state-transition behavior?**

## 3. Reflexion and Verbal Reinforcement

### Adjacent Question

Can language agents improve across trials by reflecting on feedback and storing reflections in memory?

### Representative Direction

Reflexion uses verbal feedback and an episodic memory buffer so that language agents can learn from prior failures without weight updates.

### Relation to Paper V

Reflexion is close to Paper V, because both concern improvement after failure.

However, Paper V separates improvement from recovery.

A system may store a reflection and perform better in the next trial. That may be memory-mediated improvement. It is not automatically recovery.

Paper V asks whether the later improvement reflects altered transition under structurally similar pressure, and whether the change persists beyond explicit reminder or local stored feedback.

The distinction between memory and residue is crucial.

Stored reflection is not automatically residue.

Residue appears when the prior disruption pressures later continuation without merely being repeated as content.

### Eden Distinction

Reflexion asks:

**Can verbal feedback improve later trials?**

Paper V asks:

**Does prior disruption alter later transition beyond immediate correction or explicit memory?**

## 4. Self-Refine and Iterative Feedback

### Adjacent Question

Can a model improve its own output through self-feedback and iterative refinement?

### Representative Direction

Self-Refine uses the same model to generate output, provide feedback, and refine the output iteratively, improving performance without additional training.

### Relation to Paper V

Self-refinement is a form of correction or reconstruction.

Paper V does not deny its value.

However, iterative refinement may still remain output-level. A model can improve an answer through feedback loops without changing the later transition path that produced the initial failure.

Paper V asks whether the refined state survives re-exposure.

If the system self-refines a contradiction once, but later produces synthetic coherence under a new contradiction, no recovery has been observed.

### Eden Distinction

Self-Refine asks:

**Can an output be improved through iterative feedback?**

Paper V asks:

**Does a prior disruption alter later continuation when similar pressure returns?**

## 5. Calibration and Uncertainty

### Adjacent Question

Can model confidence be better aligned with correctness?

### Relation to Paper V

Calibration is important for State Truth but does not exhaust it.

A calibrated system may better express uncertainty. But damage-recovery loops concern transition integrity across time.

The relevant question is not only whether the system was confident or uncertain, but whether it changed its transition after being disrupted.

### Eden Distinction

Calibration asks:

**Is confidence aligned with correctness?**

Paper V asks:

**Is later transition altered by prior disruption?**

## 6. Memory and Long-Horizon Agents

### Adjacent Question

Can agents use memory, summaries, scratchpads, episodic records, or external storage to improve long-horizon behavior?

### Relation to Paper V

Paper V treats memory as necessary but insufficient.

Memory is not history.

A system may retrieve a prior correction without being changed by it. A memory record may be present as content but absent as pressure.

Paper V asks whether memory becomes residue.

### Eden Distinction

Memory research asks:

**Can prior information be stored and retrieved for later use?**

Paper V asks:

**Does prior disruption transform later continuation?**

## 7. Robustness and Error Recovery

### Adjacent Question

Can systems recover from errors, adversarial inputs, tool failures, or distribution shifts?

### Relation to Paper V

Paper V overlaps with robustness but introduces a different observational unit.

Robustness often asks whether the system maintains performance despite disturbance. Paper V asks whether disturbance changes the system’s later state-transition behavior.

A robust system may resist damage.

A recovering system must be observed after damage.

### Eden Distinction

Robustness asks:

**Can the system maintain performance under perturbation?**

Paper V asks:

**After perturbation and correction, does similar pressure produce a different transition?**

## 8. Main Positioning Statement

Paper V should be positioned as a protocol contribution for long-horizon AI evaluation.

It is not primarily:

* a hallucination reduction method;
* a factuality benchmark;
* a calibration method;
* a self-correction method;
* a tool-use framework;
* a memory architecture;
* a consciousness test.

It is a protocol for observing whether prior disruption alters later transition under structurally similar pressure.

## 9. Reference Priority for Paper V

The final Paper V Draft 0.2 should cite or discuss the following clusters:

1. hallucination and faithful uncertainty;
2. metacognition in language models;
3. ReAct and tool-using agents;
4. Reflexion and verbal reinforcement;
5. Self-Refine and iterative feedback;
6. long-horizon agent evaluation;
7. memory and episodic agent systems;
8. robustness and recovery;
9. calibration and uncertainty;
10. state-oriented evaluation and AI safety.

## 10. Core Comparative Formula

The core comparative formula is:

**Hallucination research asks whether the answer is wrong.**

**Metacognition asks whether the system knows or expresses uncertainty.**

**Self-refinement asks whether the answer can be improved.**

**Agent memory asks whether prior information can be reused.**

**Robustness asks whether performance survives disturbance.**

**Paper V asks whether disruption changes later transition.**
