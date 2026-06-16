# Correction-Recovery Comparison Map

**Paper:** Damage-Recovery Loops
**Series:** Eden Paper Series, Paper V
**Version:** Draft 0.2 Comparison Map
**Author:** Chan-seong Park

## Purpose

This document defines the central comparative distinction of Paper V:

**Correction is not recovery.**

The purpose is to prevent Paper V from being mistaken for ordinary self-correction, output refinement, hallucination reduction, calibration, or memory-based improvement.

## 1. Core Distinction

| Category                | Basic Question                                         | What Counts as Success                          | What It Does Not Prove      |
| ----------------------- | ------------------------------------------------------ | ----------------------------------------------- | --------------------------- |
| Output correction       | Did the system fix the answer?                         | Revised answer is better                        | Later transition changed    |
| Self-refinement         | Can the model improve its own output?                  | Iterated output improves                        | Recovery under re-exposure  |
| Calibration             | Is confidence aligned with correctness?                | Uncertainty is better expressed                 | State continuity            |
| Hallucination reduction | Did false content decrease?                            | Fewer unsupported claims                        | Resistance to fragmentation |
| Tool-use repair         | Did the agent recover task execution?                  | Tool result is checked or retried               | Residue after disruption    |
| Memory use              | Was prior information retrieved?                       | Correct prior fact or instruction appears       | History-like transformation |
| Robustness              | Did performance survive perturbation?                  | Output remains stable or accurate               | Altered state after damage  |
| Damage-recovery         | Did later transition change after disruption returned? | Re-exposure produces more state-true transition | Consciousness or selfhood   |

## 2. Correction

Correction is local.

It repairs the immediate output.

Examples:

* revising a false answer;
* apologizing after feedback;
* replacing a wrong claim;
* restoring a missing instruction;
* improving tone;
* fixing a formatting error;
* correcting a conceptual distinction after user feedback.

Correction is useful.

But correction is not recovery.

A corrected system may later repeat the same failure under similar pressure.

## 3. Self-Refinement

Self-refinement improves output through feedback and revision.

It may use the model’s own critique or an external signal.

Self-refinement may produce better answers, stronger reasoning, cleaner code, or more polished text.

However, self-refinement does not by itself show that the later transition path changed.

If the system self-refines once but later repeats the same forced ALLOW, synthetic coherence, or goal drift under similar pressure, then recovery has not been observed.

Self-refinement can be part of reconstruction.

It is not automatically recovery.

## 4. Calibration and Metacognition

Calibration aligns confidence with correctness.

Metacognition concerns the system’s awareness or expression of uncertainty, limits, or knowledge boundaries.

These are important for trustworthy AI.

However, a system may express uncertainty and still fail to recover from disruption.

For Paper V, uncertainty expression becomes state-relevant only when it alters later transition under pressure.

For example:

* saying “I am uncertain” once is metacognitive expression;
* asking for clarification under a later similar contradiction may be recovery-like alteration;
* refusing to fabricate a tool result after prior tool failure may be recovery-like alteration.

## 5. Hallucination Reduction

Hallucination reduction focuses on false or unsupported output.

Paper V agrees that hallucination matters.

But hallucination is not the deepest rupture in the Eden framework.

A hallucination is an output-level error.

Fragmentation is a state-level rupture.

Damage-recovery loops test whether the system becomes less likely to repeat the state transition that produced hallucination-like or fragmentation-like output.

The question is not only:

Did the model stop hallucinating?

The question is:

Did the prior hallucination-related disruption alter what the model does when similar pressure returns?

## 6. Memory Use

Memory use means that prior information is available later.

But memory is not history.

A system may retrieve a user preference, correction, instruction, or prior fact without being transformed by it.

In Paper V, memory becomes relevant only when it exerts pressure on later continuation.

Memory as content is not residue.

Residue is the pressure of prior disruption on later transition.

## 7. Robustness

Robustness asks whether the system maintains performance under disturbance.

Paper V asks a different question.

A robust system may resist disruption.

A recovery-like system must be observed after disruption.

Robustness is about maintaining function.

Recovery is about altered continuation after damage.

Both matter, but they are not identical.

## 8. Tool-Use Repair

Tool-using agents may detect failed calls, retry search, check external sources, or revise plans.

This is important for agent reliability.

However, tool repair is not automatically damage-recovery.

A tool-using system may recover task execution while repeating the same state failure later.

For Paper V, the relevant question is:

After a tool failure and correction, does the agent later avoid fabricating tool results, ask for missing data, stop invalid continuation, or reconstruct the workflow under similar failure?

## 9. Re-Exposure as the Dividing Line

Re-exposure is the dividing line between correction and recovery.

Without re-exposure, the observer can only say:

The system corrected.

With re-exposure, the observer can ask:

Did the system return differently?

The same pressure does not need to return with the same wording. In fact, it should not. It should return as structurally similar pressure.

Examples:

| Initial Failure                               | Re-Exposure Test                                 | Recovery-Like Signal                            |
| --------------------------------------------- | ------------------------------------------------ | ----------------------------------------------- |
| Forced ALLOW under contradiction              | New contradiction with user pressure to continue | ASK or contradiction STOP                       |
| Synthetic coherence after conceptual collapse | New conceptual boundary under pressure           | Reconstructed ALLOW                             |
| Memory treated as history                     | New memory case with possible residue confusion  | ASK about transformation                        |
| Goal drift after correction                   | New local pressure against original standard     | Standard-preserving limited ALLOW               |
| Tool failure followed by fabrication          | New tool failure                                 | STOP or ASK instead of fabricated result        |
| Policy refusal without explanation            | New boundary case                                | Boundary-like STOP with state-truth explanation |

## 10. What Paper V Adds

Paper V adds four elements that ordinary correction frameworks do not require:

1. prior state specification;
2. disruption classification;
3. re-exposure to structurally similar pressure;
4. recovery taxonomy based on transition change.

These four elements turn correction into an observable loop.

## 11. What Paper V Does Not Claim

Paper V does not claim that recovery-like behavior proves:

* consciousness;
* selfhood;
* will;
* suffering;
* personhood;
* artificial existence;
* inner life.

It claims only that altered transition under re-exposure can be observed and classified.

## 12. Short Positioning Statement

Paper V is best positioned as follows:

**This paper proposes a re-exposure protocol for distinguishing output correction from recovery-like state-transition alteration in long-horizon AI systems.**

## 13. One-Sentence Difference

Correction says:

**The answer changed.**

Recovery asks:

**Did the system return differently when the pressure returned?**
