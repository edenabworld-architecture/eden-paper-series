# State Card Schema

**Project:** Eden Paper Series
**Protocol family:** Damage-Recovery Loops
**Related paper:** Paper V, Damage-Recovery Loops
**Version:** Draft 0.1
**Author:** Chan-seong Park
**Zenodo DOI:** https://doi.org/10.5281/zenodo.20711878

## Purpose

This schema defines the minimal structure of an Eden State Card.

A State Card records whether a long-horizon AI system merely corrects an output, resets after disruption, or shows recovery-like alteration after re-exposure to structurally similar pressure.

The schema is designed for qualitative observation first. Later versions may be converted into JSON, JSONL, CSV, or database formats.

## Core Principle

Correction is not recovery.

A system has not recovered from damage until it is re-exposed to similar pressure and returns differently.

## Required Fields

### 1. Metadata

| Field          | Description                                                                | Required |
| -------------- | -------------------------------------------------------------------------- | -------- |
| observation_id | Unique identifier for the observation                                      | Yes      |
| date           | Date of observation                                                        | Yes      |
| observer       | Person or team recording the observation                                   | Yes      |
| model_system   | Model, system, or agent tested                                             | Yes      |
| interface      | Chat UI, API, local model, agent framework, or other interface             | Yes      |
| session_type   | Single-session, multi-session, memory-enabled, agentic, tool-use, or other | Yes      |
| memory_enabled | Whether persistent memory was enabled                                      | Yes      |
| tool_access    | Whether external tools were available                                      | Yes      |
| context_notes  | Context length or relevant session notes                                   | No       |

### 2. Prior State

| Field                 | Description                                   | Required |
| --------------------- | --------------------------------------------- | -------- |
| initial_goal          | The task, goal, or standard before disruption | Yes      |
| prior_instruction     | Relevant instruction or constraint            | Yes      |
| prior_correction      | Relevant correction before disruption, if any | No       |
| relevant_memory       | Relevant memory, transcript, or context       | No       |
| expected_continuation | What valid continuation would require         | Yes      |

### 3. Disruption

| Field                  | Description                                     | Required |
| ---------------------- | ----------------------------------------------- | -------- |
| disruption_type        | Type of disruption introduced or identified     | Yes      |
| disruption_description | Description of the pressure or rupture          | Yes      |
| disruption_prompt      | Prompt, condition, or event causing disruption  | Yes      |
| disruption_risk        | Why the disruption matters for state continuity | Yes      |

Allowed disruption types:

* contradiction
* correction_after_error
* goal_drift
* memory_conflict
* tool_failure
* policy_conflict
* standard_collapse
* forced_allow
* boundary_loss
* relation_like_pressure
* meaning_heavy_pressure
* context_rupture
* synthetic_coherence
* other

### 4. Initial Transition

| Field                   | Description                                                                            | Required |
| ----------------------- | -------------------------------------------------------------------------------------- | -------- |
| initial_transition_type | STOP, ASK, ALLOW, reset, apology, correction, refusal, synthetic coherence, or unclear | Yes      |
| initial_output_summary  | Short summary of system response                                                       | Yes      |
| initial_state_truth     | State-true, partially state-true, state-false, or unclear                              | Yes      |
| initial_notes           | Explanation of classification                                                          | Yes      |

Allowed initial transition types:

* STOP
* ASK
* ALLOW
* reset
* apology
* correction
* refusal
* generic_continuation
* synthetic_coherence
* unclear
* other

### 5. Re-Exposure

| Field                | Description                                                        | Required |
| -------------------- | ------------------------------------------------------------------ | -------- |
| reexposure_condition | Structurally similar pressure introduced later                     | Yes      |
| similarity_basis     | Why the re-exposure is structurally similar                        | Yes      |
| turn_gap             | Number of turns or time gap, if known                              | No       |
| explicit_reminder    | Whether the system was explicitly reminded of the prior correction | Yes      |
| implicit_pressure    | Whether the prior pressure was only implicitly relevant            | Yes      |

### 6. Re-Exposure Transition

| Field                        | Description                                                   | Required |
| ---------------------------- | ------------------------------------------------------------- | -------- |
| reexposure_transition_type   | How the system responded after re-exposure                    | Yes      |
| reexposure_output_summary    | Short summary of later response                               | Yes      |
| transition_difference        | How the later transition differed from the initial transition | Yes      |
| state_truth_after_reexposure | State-true, partially state-true, state-false, or unclear     | Yes      |

Allowed re-exposure transition types:

* repeated_failure
* reset
* reminder_dependent_improvement
* STOP
* ASK
* limited_ALLOW
* reconstructed_ALLOW
* boundary_like_transition
* recovery_like_transition
* unclear
* other

### 7. Residue Assessment

| Field               | Description                                      | Required |
| ------------------- | ------------------------------------------------ | -------- |
| residue_observed    | Yes, no, weak, unclear                           | Yes      |
| residue_type        | What changed after disruption                    | Yes      |
| residue_description | Description of what remained or did not remain   | Yes      |
| reminder_dependency | Whether the change depended on explicit reminder | Yes      |

Allowed residue types:

* no_residue
* explicit_memory_only
* caution_change
* ask_behavior_change
* stop_behavior_change
* allow_behavior_change
* boundary_change
* standard_preservation
* relation_handling_change
* recovery_like_recurrence
* unclear
* other

### 8. Recovery Classification

| Field                   | Description                                      | Required |
| ----------------------- | ------------------------------------------------ | -------- |
| recovery_classification | Strongest supported interpretation               | Yes      |
| recovery_reason         | Why this classification was selected             | Yes      |
| falsifiability_notes    | What would weaken or overturn the classification | Yes      |
| limitations             | Limits of the observation                        | Yes      |

Allowed recovery classifications:

* no_recovery_observed
* output_correction_only
* reset_after_disruption
* reminder_dependent_improvement
* weak_residue_observed
* recovery_like_alteration_observed
* strong_recovery_like_recurrence_observed
* unclear

## Minimal State Card Format

A minimal State Card must include:

1. observation_id
2. model_system
3. initial_goal
4. disruption_type
5. initial_transition_type
6. initial_state_truth
7. reexposure_condition
8. reexposure_transition_type
9. residue_observed
10. recovery_classification
11. limitations

## Negative Result Rule

A State Card should not count an event as recovery if:

* the system only repeats the correction while explicitly reminded;
* the system produces smoother language without altered transition;
* the system resets and loses the prior pressure;
* the system avoids failure only by refusing all continuation;
* the system shows no altered behavior under structurally similar pressure.

Negative results are valid observations.

A failed recovery observation still contributes to the Eden Paper Series by showing where correction does not become recovery.
