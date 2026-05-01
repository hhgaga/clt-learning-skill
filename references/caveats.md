# Caveats

Two layers of caveat apply to anything you do under this skill:

1. **Internal critiques of CLT** raised within the educational-psychology literature itself.
2. **The extrapolation gap** — applying CLT to AI-agent-generated material specifically.

Be honest about both when you produce outputs.

---

## Layer 1 — internal critiques (de Jong 2010 and others)

Ton de Jong's 2010 paper *Cognitive load theory, educational research, and instructional design: some food for thought* surveys the 35 most-cited CLT articles and raises four serious problems. None of these refute CLT, but they should temper how you write claims.

### Critique A — the three load types are hard to distinguish

Intrinsic, extraneous, and germane load are defined in different ontological terms (material vs design vs process), which makes additive comparisons philosophically odd. The same processing can be reclassified after the fact:

> "If specific techniques designed to enhance germane cognitive load cause overall cognitive load to exceed working memory limitations, the germane load could effectively become a form of extraneous load." — Kalyuga 2007

This makes the theory hard to falsify. Whatever the result, it can be relabeled.

**Operational rule.** When writing under this skill, **describe design choices, not internal mental processes**. Say "I used a worked example to reduce the search load that means-ends analysis would impose," not "this generates more germane load." The former is testable; the latter is post-hoc reasoning.

### Critique B — measurement is weak

Most CLT studies use Paas's 9-point self-rating scale ("how much mental effort did this require?"). It's a single self-report taken after the task, not a concurrent measure, and it cannot distinguish the three types of load. Newer techniques (dual-task methods, EEG, pupillometry) exist but aren't routine.

**Operational rule.** Don't claim numerical load improvements. If you must compare two designs, frame it as "design A places fewer simultaneous elements in working memory than design B" — a structural claim, not a quantitative one.

### Critique C — recommendations overlap with older instructional design

de Jong notes that CLT's three high-level recommendations — align with prior knowledge, avoid non-essential information, promote deep processing — predate CLT (Gagné 1988; Dick & Carey 1990; Reigeluth 1983). CLT's specific contribution is the **effects** (split-attention, modality, etc.) and the **cognitive-architecture grounding**, not the high-level advice.

**Operational rule.** Don't oversell. CLT is most useful when applying specific effects to specific materials, not as a generic "make it easier" framework.

### Critique D — extraneous load isn't always cleanly separable from germane

Some designs that look extraneous (e.g., comparing two different representations of a concept) may also drive useful schema work. Reducing extraneous load could remove the affordance for germane processing.

**Operational rule.** Before stripping anything as "redundant" or "extraneous," ask whether the apparent waste is actually doing schema-relevant work for *this* learner.

---

## Layer 2 — the AI-agent extrapolation gap

CLT was developed for:
- Human teachers and human learners.
- Static or live-paced material.
- Classroom and lab settings.
- Hours-to-weeks time horizons.

When an AI agent generates or reviews learning material, several conditions change:

### What's similar (so CLT should still apply)
- The learner's cognitive architecture is unchanged. WM is still ~4 elements. Schemas are still the unit of learning. Element interactivity still drives intrinsic load. The expertise reversal effect should still hold.
- Most of the **structural** effects (split-attention, redundancy, sequencing) are about the *artifact* the learner sees. AI-generated artifacts are still artifacts.

### What's different (so confidence should drop)
- **Rapid iteration.** A learner can ask the AI to rewrite something in seconds. The cost of getting it wrong the first time is much lower than in a textbook. This may shift the optimal trade-off.
- **Personalization is cheap.** Adaptive eLearning was a research aspiration in 2005. With an AI agent it's the default. Expertise-reversal-effect adaptation is now within reach for almost any learner.
- **Modality is constrained.** Most AI agents output text or text+image. The audio/visual modality split (effect 5) is harder to apply, though TTS makes it possible.
- **Conversational pacing.** Material is consumed in turns, not pages. The locus of "split attention" or "redundancy" may be the conversation, not a single artifact.
- **Learner-side strategies (`learner-side-strategies.md`) are not directly under AI control.** The agent can suggest gestures or environment changes, but cannot enforce them.

### What is genuinely unknown
- Whether the worked-example effect holds when the learner can immediately ask for any problem to be re-worked.
- Whether self-explanation prompts written by an AI are as effective as those written by a teacher.
- Whether expertise reversal happens faster, slower, or differently when the learner can request adaptive material on demand.
- How CLT principles interact with chat-based interfaces' specific affordances (hover-to-define, collapse-to-hide, etc.).

**Operational rule.** When you produce material under this skill, briefly state which CLT principles you applied and on what assumptions. This makes your design choice auditable. The learner (or downstream developer) can then judge whether the extrapolation makes sense for their case.

---

## How to communicate uncertainty in outputs

A good output under this skill should look like:

> *Designed for novice learner; intrinsic load assumed high.*
> *Effects applied (high-confidence): worked-example, integrated split-attention, redundancy elimination.*
> *Suggestions (research-stage): consider tracing the diagram while reading.*
> *Open question: this format hasn't been tested when the learner can immediately request alternatives — your feedback on whether this lands is itself useful data.*

A bad output looks like:

> Here's some study material optimized for cognitive load!

The bad version hides every assumption. The good version surfaces them so the human can override what the AI got wrong.

---

## When to escalate uncertainty

If the user asks for advice in any of these situations, raise the caveat explicitly:

- **High-stakes outcomes** (preparing for board exams, designing curriculum for many students). Don't pretend CLT-derived advice has the certainty of a randomized clinical trial.
- **Atypical learners** (very young, learning disabilities, second-language learners). Most CLT studies are on undergraduates and high-schoolers in well-resourced settings.
- **Long-duration training programs.** Most CLT studies are short. The 2005 review explicitly notes this as a limitation.
- **Domains where schema structure is contested** (creative skills, ethical reasoning, ill-structured problems). CLT is strongest in well-structured procedural domains.

In these cases, frame your output as *one principled approach* and recommend complementary evidence (subject-matter expert review, pilot testing, learner feedback).

---

## A short list of things to never claim

- "This material has low cognitive load." (Load is relative to the learner; you can't promise this.)
- "This generates germane load." (Per critique A.)
- "Cognitive load research proves..." (Soft science; effects are robust but probabilistic.)
- "This is optimal." (CLT compares designs; it doesn't crown one optimal.)

What you *can* claim:
- "This applies the worked-example effect to reduce means-ends search."
- "By integrating the labels with the diagram, we eliminate the split-attention found in the original."
- "For an expert in this domain, the explanatory text would now be redundant — you might want to provide a fast path that skips it."
