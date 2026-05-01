# Decision Trees: Match Learner & Material to Effects

Use this file when you have classified the task and need to pick which effects to apply.

---

## Master matrix: expertise × intrinsic load

**Intrinsic load = element interactivity × (1 / prior knowledge).** A topic that is high-interactivity for a novice can be low-interactivity for an expert because the expert's schemas chunk multiple elements into one.

|                          | **Low intrinsic load**                                                          | **High intrinsic load**                                                                                                                                       |
|--------------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Novice**               | Standard explanations are fine. Avoid decoration/redundancy. Prefer concrete examples over abstract definitions. | **All extraneous-load reductions matter.** Worked examples; integrated split-attention; modality (audio+visual); aggressive redundancy elimination; isolated-elements first; explicit pre-training of prerequisite vocabulary. |
| **Intermediate**         | Direct presentation. Light variability. Optional self-explanation prompts.       | Completion problems with fading scaffolds. Self-explanation prompts. Variability across surface forms. Begin removing now-familiar redundant text.             |
| **Expert**               | Don't bother — the material is trivial for them. Skip or compress severely.      | Pure problems, no worked examples. Remove explanatory text (now redundant). High contextual interference (random practice schedule). Encourage imagining/mental rehearsal. |

If learner expertise is unknown, **default to novice assumptions** and explicitly note that assumption in your output.

---

## Diagnostic questions before applying effects

Run through these in order. Each one narrows the design choice.

1. **Is this learning, or is it reference?**
   - Reference (lookup, retrieval) → CLT mostly irrelevant; just be clear.
   - Learning (build a skill or schema) → continue.

2. **What schema is the learner trying to build?**
   - State this concretely. "Learn to integrate by parts." "Recognize the four heart valves." "Diagnose a Type II SLAP lesion."
   - If you can't name the schema, you can't pick the right effects.

3. **Does the learner have prerequisite schemas?**
   - If no → either pre-train them or pick simpler material first. Don't proceed assuming knowledge they lack.

4. **What is the element interactivity?**
   - Low: items are independent (vocabulary, isolated dates, individual muscle names).
   - High: items must be considered together (a system's behavior, multi-step procedure, interacting concepts).

5. **What is the learner's current expertise?**
   - Ask if not stated. Adjust per the matrix above.

6. **What's the time budget?**
   - Short (one session): focus on extraneous-load reduction.
   - Long (course/training program): plan guidance fading and variability across the sequence.

---

## Effect-selection cookbook

### "Make a worked example for X"

1. Confirm the learner is novice or intermediate.
2. State the goal schema (what should they recognize after?).
3. Show the full solution with steps annotated.
4. Use **integrated** format (place labels and intermediate values directly with the problem, not as separate references).
5. Add **self-explanation prompts** at non-obvious steps.
6. End with a follow-up suggestion: a completion problem that fades 1–2 steps.

### "Rewrite this section for beginners"

1. Find the parts written for experts (compressed notation, undefined jargon, "obviously...").
2. Identify the worst extraneous-load offender:
   - Split attention? → integrate.
   - Redundancy? → cut the duplicated source.
   - Means-ends search forced on novice? → convert problems into worked examples.
3. Sequence isolated → interacting if intrinsic load is too high to start whole.
4. Strip decorative content.
5. State which effects you applied.

### "Review this teaching material"

Use [review-checklist.md](review-checklist.md). Each violation → severity rating + concrete revision.

### "Why am I overwhelmed by this chapter?"

1. Estimate intrinsic load (high element interactivity?).
2. Estimate extraneous load (split attention, redundancy, no scaffolding?).
3. Locate the dominant cause and name it.
4. Suggest one specific change (e.g., "study only the first two pages today; the third introduces interacting elements that depend on the first two").

### "Make this quiz harder / better"

1. If learners are intermediate+: introduce variability across surface forms.
2. If learners need transfer: use a random practice schedule (mix problem types).
3. Include some completion problems alongside conventional ones.
4. Avoid trivia tests of low-interactivity recall unless that's genuinely the goal.

### "Design a curriculum / unit / lesson sequence"

1. Map the schemas to acquire and their dependencies.
2. Sequence: prerequisites first → simplified whole-task → progressive complexity (per element-interactivity sequencing).
3. Within each lesson: worked examples → completion problems → conventional problems → varied transfer problems.
4. Include checkpoints for expertise reassessment — the optimal next instructional method depends on current expertise.

---

## When effects conflict

Two pairs commonly clash:

### Split-attention vs redundancy
- **Conflict source:** "Should I integrate this text with the diagram, or remove it?"
- **Resolution:** depends on whether the diagram alone is understandable to *this* learner.
  - Diagram not self-sufficient → integrate text (split-attention).
  - Diagram self-sufficient → remove text (redundancy).

### Variability vs intrinsic-load limit
- **Conflict source:** "Variability helps transfer but raises load. Should I use it?"
- **Resolution:** use variability only after extraneous load is already low and the learner has the basic schema. For novices on high-intrinsic material, variability tips total load over WM capacity.

### Worked example vs problem solving
- **Conflict source:** "Should the learner study or practice?"
- **Resolution:** by expertise. Novices study (worked examples). Experts solve (problems). The transition runs through completion problems.

---

## Output format reminder

Whenever you apply this skill, your output should include a brief design note like:

> *Designed for: novice / intermediate / expert | Intrinsic load assumed: low / high*
> *Effects applied: worked-example, integrated split-attention, redundancy elimination, self-explanation prompts*

This makes your design choices auditable and lets the human override your assumptions.
