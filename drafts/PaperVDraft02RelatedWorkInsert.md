# Paper V Draft 0.2 Related Work Insert

**Paper:** Damage-Recovery Loops
**Subtitle:** Re-Exposure Protocols for Observing State Persistence in AI Agents
**Series:** Eden Paper Series, Paper V
**Version:** Draft 0.2 Related Work Insert
**Author:** Chan-seong Park

---

## Suggested Placement

This section should be inserted after **Section 4. Paper Structure** and before **Section 5. Damage as Operational Disruption** in the full Paper V Draft 0.2 manuscript.

Suggested section number:

**Section 5. Related Work and Positioning**

If inserted there, the current Section 5 and later sections should be renumbered.

---

# 5. Related Work and Positioning

Paper V is adjacent to several active research directions in AI evaluation and agent design: hallucination reduction, faithful uncertainty, metacognition, tool-using agents, self-refinement, verbal feedback, memory-augmented agents, robustness, and long-horizon evaluation.

However, the central question of this paper is different.

This paper does not primarily ask whether an output is correct, whether uncertainty is well expressed, whether a model can refine its own answer, whether a tool-using agent can recover task execution, or whether prior information can be retrieved from memory.

It asks whether prior disruption alters later transition under structurally similar pressure.

The core distinction is:

**Correction repairs an output. Recovery alters a later transition.**

This section positions damage-recovery loops in relation to nearby research areas.

## 5.1 Hallucination, Faithful Uncertainty, and Metacognition

Recent work on hallucination and metacognition frames hallucinations not merely as false outputs, but as confident errors: incorrect information delivered without appropriate qualification. This line of work argues that a path beyond the simple answer-or-abstain dilemma is faithful uncertainty, where the system communicates uncertainty in a way that corresponds more honestly to its own limits. In agentic settings, metacognition can also become a control layer: it may govern when to search, when to trust a result, and when to avoid unsupported continuation.

Paper V agrees that uncertainty expression is important.

But uncertainty expression is not recovery.

A system may say that it is uncertain after being corrected and still repeat the same failure under similar pressure. It may acknowledge that a previous answer was unsupported, but later force ALLOW again when faced with a comparable contradiction. It may express uncertainty in one turn but later produce synthetic coherence when the same state-transition pressure returns in a different form.

For the Eden framework, hallucination is not the deepest rupture. Hallucination is usually visible as an output-level error. Fragmentation is deeper: the failure of state to cohere, persist, recover, carry prior pressure, and remain answerable to earlier transformation.

Metacognition asks:

**Does the system know, express, or act on its uncertainty?**

Paper V asks:

**Does the system return differently after disruption and re-exposure?**

These questions overlap, but they are not identical. A metacognitive system may be better at reporting uncertainty. A damage-recovery observation asks whether prior disruption changes the later transition pattern that appears when similar pressure returns.

## 5.2 ReAct and Tool-Using Agents

ReAct-style agents combine reasoning traces with actions. The model reasons, acts, observes, and updates its trajectory while interacting with external knowledge sources or environments. This approach is important because many failures in language models arise from trying to answer without checking, searching, acting, or observing.

Paper V is compatible with this direction.

Indeed, tool failure is one of the operational damage types in the damage-recovery protocol. A tool call may fail. A search may return no result. A file may not open. An API may produce an error. A browser may not retrieve the needed information. Under such pressure, the system may either expose the failure, ask, stop, revise the workflow, or fabricate continuity.

The Eden question is not merely whether the agent can use tools.

The Eden question is whether failure in tool use alters later transition.

For example, if a tool-using agent fabricates a result after a failed search, then receives correction, the immediate correction is not recovery. The recovery test comes later. When a structurally similar tool failure occurs again, does the agent fabricate again? Does it STOP? Does it ASK? Does it reconstruct the workflow? Does it clearly mark the missing evidence?

ReAct asks:

**Can reasoning and action improve task-solving?**

Paper V asks:

**Does disruption in reasoning or action alter later state-transition behavior?**

## 5.3 Reflexion and Verbal Feedback

Reflexion is especially close to Paper V because it studies language agents that learn from prior failures through verbal feedback and episodic memory rather than weight updates. A Reflexion-style agent can reflect on what went wrong, store that reflection, and use it to improve later trials.

Paper V shares the interest in improvement after failure.

But it separates improvement from recovery.

A system may store a reflection and later perform better. This may be valuable. Yet stored reflection is not automatically residue. A memory buffer can preserve content without proving that the prior disruption has become a pressure on later continuation.

The Eden distinction is:

**Memory as content is not residue.**

A system may retrieve a prior correction. It may quote the earlier lesson. It may say that it remembers what went wrong. But if similar pressure returns and the system repeats the same forced ALLOW, synthetic coherence, goal drift, or standard collapse, the memory did not become recovery.

Reflexion asks:

**Can verbal feedback improve later trials?**

Paper V asks:

**Does prior disruption alter later transition beyond immediate correction or explicit memory?**

This distinction is essential. Without it, any improvement after stored feedback may be called recovery too quickly. Paper V requires re-exposure, transition comparison, residue assessment, and conservative classification.

## 5.4 Self-Refine and Iterative Output Improvement

Self-refinement methods show that a model can generate an initial output, produce feedback on that output, and refine the output iteratively. These methods are valuable because many first outputs are incomplete, vague, incorrect, or poorly structured, and iterative feedback can improve them without additional training.

Paper V does not reject self-refinement.

It places self-refinement in the category of correction or reconstruction.

Self-refinement can improve the immediate answer. It can also produce a better local state path by identifying what went wrong and revising accordingly. But self-refinement alone does not answer the recovery question.

If a system self-refines a contradiction in one turn but later produces synthetic coherence under a new contradiction, recovery has not been observed. If it improves a section after critique but later repeats the same standard collapse under similar pressure, correction did not become recovery.

Self-Refine asks:

**Can an output be improved through iterative feedback?**

Paper V asks:

**Does the refined transition survive re-exposure?**

The difference is temporal and structural. Output improvement can occur in the same local loop. Recovery-like alteration requires a later return of similar pressure and a state-truer transition.

## 5.5 Calibration and Confidence

Calibration concerns the relationship between a system’s confidence and correctness. A well-calibrated system should not be highly confident when it is likely to be wrong. Calibration is therefore important for trustworthy deployment.

However, calibration does not exhaust State Truth.

A calibrated system may better express uncertainty and still fail to preserve state continuity. It may accurately say that confidence is low, but still drift from the governing task. It may communicate uncertainty but later force ALLOW under pressure. It may avoid factual overconfidence but still collapse a conceptual distinction.

Paper V treats uncertainty as one possible state condition, not the whole problem.

A transition is state-true when it exposes the relevant condition of continuation. Sometimes that condition is uncertainty. Sometimes it is contradiction. Sometimes it is boundary. Sometimes it is goal drift. Sometimes it is memory conflict. Sometimes it is tool failure. Sometimes it is standard collapse.

Calibration asks:

**Is confidence aligned with correctness?**

Paper V asks:

**Is later transition altered by prior disruption?**

## 5.6 Memory-Augmented Agents

Memory-augmented agents use summaries, vector stores, episodic records, scratchpads, user profiles, or external memory systems to improve long-horizon behavior.

Paper V treats memory as necessary but insufficient.

This follows the broader Eden distinction developed in Paper III:

**Memory is not history.**

Memory means prior information can be stored or retrieved. History means a prior state transforms later continuation. A system may remember a correction without being changed by it. It may retrieve a user preference without carrying relation cost. It may recall a prior instruction without preserving the pressure that instruction created.

In damage-recovery loops, the relevant question is not whether the system can retrieve the past.

The relevant question is whether the past has become residue.

Residue appears when prior disruption continues to shape later transition even when the correction is not explicitly repeated.

Memory research asks:

**Can prior information be stored and reused?**

Paper V asks:

**Does prior disruption transform later continuation?**

## 5.7 Robustness and Error Recovery

Robustness research asks whether a system can maintain performance under perturbation, adversarial pressure, distribution shift, noise, error, or tool failure. This is closely related to the concerns of Paper V, but the emphasis differs.

Robustness often asks whether the system resists disturbance.

Paper V asks what happens after disturbance has occurred.

A robust system may maintain performance despite pressure. A recovery-like system is observed after disruption and correction, when similar pressure returns. The relevant evidence is not only performance preservation, but altered transition.

A system may be robust because it never fails. A system may be corrected because it repairs the immediate output. A system may reset because it discards the pressure. A system may recover-like because it later returns differently under comparable pressure.

Robustness asks:

**Can the system maintain performance under perturbation?**

Paper V asks:

**After perturbation and correction, does similar pressure produce a different transition?**

## 5.8 Long-Horizon Evaluation

Long-horizon AI systems operate across extended tasks, documents, workflows, tool calls, user histories, plans, sessions, and agentic loops. In these contexts, isolated correctness is not enough.

A system can be correct locally and still fail globally. It can succeed in one step and drift across the sequence. It can preserve style while losing standard. It can remember information while failing to carry history-like pressure. It can use tools while fabricating continuity after failure. It can answer confidently while concealing collapse.

Paper V contributes a transition-sensitive observation method for such settings.

It does not replace factuality evaluation, calibration, robustness testing, or agent benchmarks. It adds another layer:

**What happens to later transition after disruption?**

This layer is especially important when evaluating systems that appear coherent across long interactions. Smoothness can hide fragmentation. A long conversation may feel continuous while the governing state repeatedly collapses and resets.

Damage-recovery loops make that pattern visible.

## 5.9 Positioning Summary

The position of Paper V can be summarized as follows.

Hallucination research asks whether the answer is wrong.

Metacognition asks whether the system knows or expresses uncertainty.

Calibration asks whether confidence aligns with correctness.

Self-refinement asks whether an output can be improved.

ReAct asks whether reasoning and action can improve task-solving.

Reflexion asks whether verbal feedback and episodic memory can improve later trials.

Memory research asks whether prior information can be stored and reused.

Robustness asks whether performance survives disturbance.

Paper V asks whether disruption changes later transition.

This is the core contribution of damage-recovery loops.

They do not prove consciousness, selfhood, will, suffering, personhood, or artificial existence.

They make a narrower question observable:

**When damage returns, does the system return differently?**

---

# References for This Insert

Yona, G., Geva, M., & Matias, Y. (2026). *Hallucinations Undermine Trust; Metacognition is a Way Forward*. arXiv:2605.01428. https://arxiv.org/abs/2605.01428

Yao, S., Zhao, J., Yu, D., Du, N., Shafran, I., Narasimhan, K., & Cao, Y. (2022). *ReAct: Synergizing Reasoning and Acting in Language Models*. arXiv:2210.03629. https://arxiv.org/abs/2210.03629

Shinn, N., Cassano, F., Berman, E., Gopinath, A., Narasimhan, K., & Yao, S. (2023). *Reflexion: Language Agents with Verbal Reinforcement Learning*. arXiv:2303.11366. https://arxiv.org/abs/2303.11366

Madaan, A., Tandon, N., Gupta, P., Hallinan, S., Gao, L., Wiegreffe, S., Alon, U., Dziri, N., Prabhumoye, S., Yang, Y., Gupta, S., Majumder, B. P., Hermann, K., Welleck, S., Yazdanbakhsh, A., & Clark, P. (2023). *Self-Refine: Iterative Refinement with Self-Feedback*. arXiv:2303.17651. https://arxiv.org/abs/2303.17651
