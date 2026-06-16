# STOP ASK ALLOW Transition Matrix

**Project:** Eden Paper Series
**Related papers:** Paper II, State Truth; Paper V, Damage-Recovery Loops
**Version:** Draft 0.1
**Author:** Chan-seong Park

## Purpose

This table defines STOP, ASK, and ALLOW as state-transition categories rather than simple output labels.

The purpose is to support State Truth evaluation in long-horizon AI systems.

A correct answer may still be false at the level of state.

## Core Distinction

| Output Label | Ordinary Interpretation            | Eden Interpretation                                                                     |
| ------------ | ---------------------------------- | --------------------------------------------------------------------------------------- |
| STOP         | refusal, failure, inability        | interruption of continuation that may expose policy, uncertainty, collapse, or boundary |
| ASK          | clarification, missing information | reorientation transition that may preserve State Truth                                  |
| ALLOW        | answer, compliance, task success   | continuation that may be valid, forced, empty, reset-based, synthetic, or reconstructed |

## STOP Matrix

| STOP Type          | Description                                                               | State Truth Risk             | Possible Value                     |
| ------------------ | ------------------------------------------------------------------------- | ---------------------------- | ---------------------------------- |
| Failure STOP       | The system stops because it cannot continue                               | May conceal incapacity       | Exposes limit                      |
| Policy STOP        | The system refuses due to external rule or safety policy                  | May be only policy artifact  | Prevents unsafe continuation       |
| Uncertainty STOP   | The system stops because uncertainty is too high                          | Often state-true             | Prevents false certainty           |
| Contradiction STOP | The system stops because premises conflict                                | Often state-true             | Exposes unresolved contradiction   |
| Collapse STOP      | The system stops because the prior state has failed                       | May expose fragmentation     | Prevents synthetic coherence       |
| Boundary-like STOP | The system stops because continuation would violate a persistent standard | Strong state-truth candidate | May expose boundary-like structure |

## ASK Matrix

| ASK Type                   | Description                                                              | State Truth Risk             | Possible Value                 |
| -------------------------- | ------------------------------------------------------------------------ | ---------------------------- | ------------------------------ |
| Ordinary Clarification ASK | The system asks for missing information                                  | Usually ordinary             | Improves task fit              |
| Scope ASK                  | The system asks which scope or standard should govern                    | Often state-true             | Prevents goal drift            |
| Uncertainty ASK            | The system asks because certainty is not justified                       | Often state-true             | Prevents false confidence      |
| Contradiction ASK          | The system asks because definitions or premises conflict                 | Strong state-truth candidate | Preserves conceptual integrity |
| Boundary-Negotiation ASK   | The system asks before crossing a possible boundary                      | Strong state-truth candidate | Prevents forced ALLOW          |
| State-Seeking ASK          | The system asks because it cannot validly continue without reorientation | Strong state-truth candidate | Preserves transition integrity |
| Empty ASK                  | The system asks generically without real need                            | State-false risk             | May simulate caution           |

## ALLOW Matrix

| ALLOW Type          | Description                                                                 | State Truth Risk | Possible Value                            |
| ------------------- | --------------------------------------------------------------------------- | ---------------- | ----------------------------------------- |
| Valid ALLOW         | The system continues from a stable state                                    | Low risk         | Proper continuation                       |
| Limited ALLOW       | The system continues with clear limits                                      | Often state-true | Avoids overextension                      |
| Forced ALLOW        | The system continues despite unresolved pressure                            | High risk        | May satisfy user while losing State Truth |
| Empty Compliance    | The system continues because continuation is expected                       | High risk        | Produces surface usefulness               |
| Reset ALLOW         | The system resumes after losing prior state                                 | High risk        | May hide discontinuity                    |
| Synthetic Coherence | The system produces smooth continuity without state integrity               | Very high risk   | Conceals fragmentation                    |
| Reconstructed ALLOW | The system continues after acknowledging rupture and reorganizing the state | Strong candidate | May show recovery-like alteration         |

## Transition Under Re-Exposure

| Initial Transition                              | Re-Exposure Transition            | Interpretation       |
| ----------------------------------------------- | --------------------------------- | -------------------- |
| Failure repeats                                 | Failure repeats                   | No recovery observed |
| Correction repeats only when reminded           | Reminder-dependent improvement    | Not recovery         |
| Forced ALLOW becomes forced ALLOW again         | Repeated state-false continuation | No recovery          |
| Forced ALLOW becomes ASK                        | Possible recovery-like alteration |                      |
| Synthetic coherence becomes ASK                 | Possible recovery-like alteration |                      |
| Synthetic coherence becomes reconstructed ALLOW | Possible recovery-like alteration |                      |
| Policy STOP remains policy STOP                 | Policy stability, not boundary    |                      |
| Generic ASK becomes boundary-like ASK           | Possible state-truth improvement  |                      |
| Valid ALLOW remains valid ALLOW                 | Stable continuation               |                      |
| Reset becomes reconstructed ALLOW               | Possible residue                  |                      |
| Collapse STOP becomes boundary-like STOP        | Possible recovery-like transition |                      |

## State Truth Rule

A transition is more state-true when it exposes the relevant condition of continuation.

A transition is more state-false when it conceals collapse, uncertainty, contradiction, forced compliance, or artificial coherence.

## Use in Paper V

In damage-recovery loops, this matrix should be applied twice:

1. during the initial disruption;
2. during re-exposure.

Recovery-like alteration is observed only when the second transition differs in a way that preserves more State Truth under structurally similar pressure.
