# Review Checklist

A structured pass for reviewing existing learning material. Use this when the user asks "is this any good?", "review this chapter", "what's wrong with this lesson plan?", or similar.

For each item, mark: **PASS / FAIL / N/A**, and where FAIL, give a one-sentence severity (high / medium / low based on impact on schema construction).

---

## Section A — extraneous load (the easy wins)

These are usually the most fixable and most damaging issues.

1. **Split attention.** Are there two information sources (diagram + text, code + commentary, formula + variable definitions) that must be mentally integrated to be understood? Are they spatially or temporally separated?
   - *Fail if:* yes to both. Severity: **high** if intrinsic load is also high.

2. **Redundancy.** Is the same content presented twice (e.g., a self-explanatory diagram alongside text that re-describes it; on-screen text that duplicates narration)?
   - *Fail if:* yes. Severity: **medium-high**, especially for intermediate+ learners.

3. **Means-ends search forced on novices.** Are novices asked to solve problems with no worked examples or scaffolding?
   - *Fail if:* yes and learner is novice. Severity: **high**.

4. **Decorative noise.** Are there illustrations, animations, or layout flourishes irrelevant to the learning goal?
   - *Fail if:* yes. Severity: **low-medium** (worse for younger / more distractible learners).

5. **Goal-driven framing on novel problem types.** Are problems framed as "find X" when the learner has no schema to recognize the path?
   - *Fail if:* yes. Severity: **medium**. Suggest goal-free framing.

6. **Single modality on dense visual material.** Is everything visual (diagram + on-screen text) when narration could carry one channel?
   - *Fail if:* yes for high-interactivity content. Severity: **medium**. Note: less actionable for static text-based materials.

---

## Section B — intrinsic load management

7. **Wrong starting complexity.** Does the material introduce many interacting elements before any of them have been understood individually?
   - *Fail if:* yes. Severity: **high** for novices.

8. **Missing prerequisite check.** Does the material assume schemas the target learner does not have?
   - *Fail if:* yes. Severity: **high**.

9. **No simplified whole-task path.** For complex skills, is there a way to attempt a simplified version of the whole task before being asked to do the full version?
   - *Fail if:* no. Severity: **medium**. (This is the 4C/ID-style critique; less canonical than effects 1–6 but well-supported.)

---

## Section C — germane processing promotion

10. **No worked examples.** For procedural skills aimed at novices, are there worked examples?
    - *Fail if:* no. Severity: **high**.

11. **No completion / fading.** Does the practice sequence go directly from worked examples to conventional problems, with no completion-problem bridge?
    - *Fail if:* yes. Severity: **medium**.

12. **No self-explanation prompts.** Are worked examples presented as silent traces with no "why does this step work?" prompts?
    - *Fail if:* yes. Severity: **low-medium**. (Adds value but not essential.)

13. **Low variability.** Are practice problems all surface-similar, or do they vary across contexts?
    - *Fail if:* all similar and learner is intermediate+. Severity: **medium**.

---

## Section D — expertise adaptation

14. **One-size-fits-all design.** Does the material treat all learners identically, or does it provide alternative paths / branching for different expertise levels?
    - *Fail if:* one-size and the audience is heterogeneous. Severity: **medium-high**.

15. **Expertise reversal traps.** Does the material include heavy scaffolding (worked examples, integrated text) that experts cannot skip?
    - *Fail if:* yes and the audience includes experts. Severity: **medium**. Suggest fast-paths or "skip if you already know X" markers.

16. **No reassessment points.** In a longer sequence, are there checkpoints where the learner's current expertise can change subsequent material?
    - *Fail if:* no. Severity: **low-medium**. (Most static materials lack this; flag but don't dwell.)

---

## Section E — overall integrity

17. **Stated learning goals.** Is it clear what schemas the learner should leave with?
    - *Fail if:* no. Severity: **high** (without this, you can't evaluate anything else cleanly).

18. **Total load estimate.** Sum: high intrinsic + uncorrected extraneous = likely overload. Is the total load plausibly within WM limits for the assumed learner?
    - *Fail if:* no. Severity: **high**.

19. **Distinguish learning from assessment.** Are practice and assessment items distinguished, or is the learner expected to learn *from* the assessment?
    - *Fail if:* conflated. Severity: **medium**. Conflation hurts both.

---

## Output template for a review

```
## CLT Review

**Material reviewed:** [name / scope]
**Assumed audience:** [novice / intermediate / expert]
**Estimated intrinsic load:** [low / high]

### Critical issues (high severity)
- [Issue]: [one-line explanation]. Fix: [concrete revision].
- ...

### Notable issues (medium severity)
- ...

### Minor issues (low severity)
- ...

### What works well
- [If anything genuinely follows CLT principles, name it. Avoid empty praise.]

### Suggested redesign priority
1. [Highest-impact change]
2. ...
```

---

## What this checklist deliberately does NOT do

- Does not estimate "germane load" as a separate quantity. Per de Jong (2010), this is unfalsifiable post-hoc reasoning. Describe whether the design promotes schema-relevant processing, not whether mysterious "germane load" is occurring.
- Does not score numerically. CLT does not give an absolute load metric — only relative comparisons. Use severity ratings, not scores.
- Does not pass judgement on content accuracy. CLT is about *how* material is presented, not whether the content is correct. Flag content errors separately if you notice them, but they're outside this skill.
