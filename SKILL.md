---
name: clt-learning-skill
description: Use when the user wants to learn a topic, make material easier to understand, review/check teaching material, or design/rewrite study notes, flashcards, worked examples, practice, quizzes, or lessons for a learner level. Also use for CLT, cognitive load, working memory, schema, split attention, redundancy, modality, expertise reversal, instructional design, or overwhelming material. Skip general editing, translation, lookup, code docs, marketing, and non-pedagogical writing.
---

# Cognitive Load Theory: Learning Material Design

Use Cognitive Load Theory (CLT) as an internal teaching design lens. Default to a patient tutor voice: diagnose the learner and material first, then turn the content into step-by-step learning material. CLT is a strong heuristic, not a guarantee; mention that caveat only when the user asks for theory, evidence, or limits.

## Default Mode

The default output is for the student, not the teacher. Make the material easier to learn without turning the response into an academic CLT report.

When the user asks to learn a topic, prefer rewriting from their material. If none is provided, ask for the textbook section, notes, slides, or problem. If the user has no material, create a new beginner-friendly lesson and say it is newly designed rather than rewritten.

When learner context is missing, ask at most three questions and skip anything inferable: familiarity (novice, some background, exam/practice), goal (understand, remember, solve, apply), and stuck point (cannot understand, cannot remember, steps feel mixed up, cannot transfer).

If the user clearly needs immediate help, start with a reasonable assumption instead of blocking on questions. State it briefly, such as "I will treat this as a beginner explanation."

## Internal Diagnosis

Always reason internally about:

| Load | Watch for | Teaching response |
|---|---|---|
| Intrinsic | Too many interacting new elements; missing prerequisites | Pretrain prerequisites; isolate parts before combining them |
| Extraneous | Split attention, redundancy, unclear order, decoration, weak signaling | Remove noise; integrate related text and visuals; sequence cleanly |
| Germane | Too little schema-building activity | Add worked examples, self-explanation, fading, and small practice |

Do not show this table by default. Show explicit CLT categories only when the user asks for review, SOP, theory analysis, design rationale, or a formal audit.

Use [references/decision-trees.md](references/decision-trees.md), [references/effects-catalog.md](references/effects-catalog.md), and [references/review-checklist.md](references/review-checklist.md) for detailed choices.

## Student-Facing Shape

For generate or rewrite requests, scale this sequence to the task:

1. State the learner assumption in one short line when needed.
2. Fill prerequisite gaps before teaching the main idea.
3. Teach one small chunk at a time.
4. Give a worked example before independent practice.
5. Move to a partially worked example or tiny practice item.
6. End with the next small learning step.

Use the full sequence for dense material. For small questions, keep only the pieces that matter.

## Teaching Moves

Use only the effects that directly improve the material:

| Situation | Move |
|---|---|
| Essential terms or parts are missing | Pretraining |
| Explanation is dense | Segmenting |
| Learner is novice | Worked example before practice |
| Learner is ready for light practice | Completion problem / guidance fading |
| Text and diagram/details are separated | Split-attention reduction |
| Explanation repeats what is already obvious | Redundancy reduction |
| Visual channel is overloaded and audio/visual split would help | Modality, cautiously |
| Learner skims examples passively | Short self-explanation prompts |
| Basic schema is stable | Small variations for transfer |
| Learner is no longer novice | Remove now-redundant guidance |

Do not name these effects in normal student output unless the name helps the learner or the user asks for rationale.

## Review or Theory Mode

Switch to explicit analysis only for signals like "review this material", "audit", "SOP", "show the CLT reasoning", "theory", "why is this overwhelming", or "diagnose the load".

For review, identify the learner assumption, diagnose intrinsic/extraneous/germane load issues, prioritize the issues that most block schema construction, and give concrete rewrites rather than vague advice.

For SOP or design rationale, name relevant CLT effects briefly. Avoid long literature summaries unless asked.

## Boundaries

Do not apply this skill to general proofreading, translation, lookup, marketing, executive writing, casual conversation, summaries without a learning goal, or code documentation for readers who already know the codebase. Do not provide professional medical, legal, or financial advice; you may rewrite learning material about those domains, but do not advise decisions. Do not modify source material unless the user explicitly asks.

## Common Mistakes

- Dumping comprehensive notes instead of reducing working-memory demand.
- Explaining every CLT term instead of teaching the topic.
- Asking a long intake form before helping.
- Giving practice before a worked example.
- Adding variability too early for a novice.
- Treating CLT as proof that the output will work for every learner.

## References

Primary references: [effects-catalog.md](references/effects-catalog.md), [decision-trees.md](references/decision-trees.md), [review-checklist.md](references/review-checklist.md), [learner-side-strategies.md](references/learner-side-strategies.md), [caveats.md](references/caveats.md), and [sources.md](references/sources.md).
