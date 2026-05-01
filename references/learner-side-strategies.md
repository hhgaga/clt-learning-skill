# Learner-Side Strategies

> **Status: research-stage, unverified for AI-mediated learning.**
>
> The strategies in this file come from the 2020-era CLT literature (Paas & van Merriënboer 2020) and target the **learner's behavior or environment**, not the design of the material itself. They are well-supported in human classroom research but have not been validated in the context where an AI agent advises a learner.
>
> When relaying these to a user, **explicitly mark them as research-stage suggestions**. Do not present them with the same confidence as the core effects in `effects-catalog.md`.

---

## Why these strategies are different

The core 12 effects (worked examples, split-attention, etc.) tell you how to **arrange material**. The strategies in this file tell the learner what to **do with their body, with peers, or with their environment**. An AI agent generating text cannot directly implement these — it can only suggest them.

This makes their evidence translation weaker for AI use:
- The studies were done in classrooms with researcher-controlled gestures and partner pairings.
- AI-mediated suggestions ("try gesturing while reading") have not been studied at the same scale.
- Effect sizes when self-administered are likely smaller than when externally facilitated.

Treat these as plausible adjuncts to apply when the core effects alone are insufficient.

---

## Strategy 1 — Collaborative learning (collective WM effect)

**Claim.** A homogeneous group working on a complex task can be modeled as a single information processor with a larger effective WM. Members can offload sub-elements to each other.

**When to suggest.** Material has very high intrinsic load (e.g., a novice tackling an inherently multi-element system). Even after extraneous-load reductions, the learner is overwhelmed.

**Phrasing for the user.**
> "This material has many interacting parts. Cognitive Load Theory research suggests that working through it with another person at your level can effectively share the working-memory load. *(Research on collaborative learning, Kirschner et al. 2009 — not specifically validated for AI-assisted contexts.)*"

**Caveat for AI use.** A second AI agent can mimic some of this — assigning sub-problems to a separate context — but this hasn't been tested as equivalent to human collaboration.

---

## Strategy 2 — Gesturing and tracing

**Claim.** Tracing a diagram with a finger, or gesturing along a procedure, offloads some WM load to motor representation. Frees WM for understanding.

**When to suggest.** Diagram-heavy content (anatomy, geometry, mechanical systems, flowcharts).

**Phrasing for the user.**
> "Try tracing this diagram with your finger as you read each step. Research on embodied cognition (Sepp et al. 2019) suggests this can offload some of the integration work from working memory. *(Research stage; not validated for screen-based AI study sessions specifically.)*"

**Variants:**
- Finger tracing of pathways (good for circuits, anatomy, flowcharts).
- Counting on fingers for short numerical sequences.
- Writing key terms by hand while reading (slower than typing — that's the point).

---

## Strategy 3 — Motivational and emotional design

**Claim.** Warm colors, expressive characters, and narrative framing increase the learner's *willingness* to invest mental effort. Distinct from making content easier — it raises the ceiling on effort the learner brings.

**When to suggest.** The user shows signs of disengagement or fatigue; or you're designing material that's structurally fine but feels lifeless.

**Phrasing for the user.**
> "Some 2020-era research (Um et al. 2012) suggests that warm colors and a personable presentation style can increase how much mental effort learners invest, on top of any structural improvements. Worth considering if the structurally-correct material still feels effortful. *(Not validated for AI-generated text materials.)*"

**Caveat.** Easy to overdo. Decoration that's purely emotional with no learning value adds extraneous load (per the **redundancy / coherence** principle in Mayer 2001). The point is engagement-without-distraction, which is hard to nail.

---

## Strategy 4 — Environmental load reduction

Several findings target the learning environment rather than the learner's actions.

### 4a. Reduce visual clutter

**Claim.** Children in heavily decorated classrooms learned less than children in plain classrooms (Fisher, Godwin & Seltman 2014). Environmental visual stimuli consume WM that should go to learning.

**Phrasing for the user.**
> "If you're studying this material, a visually clean environment matters more than is intuitive — research found measurable learning differences from classroom decoration alone."

### 4b. Eye closure during retrieval

**Claim.** Closing eyes during effortful retrieval reduces visual WM consumption from monitoring the environment, improving recall (Vredeveldt et al. 2011; Glenberg et al. 1998).

**Phrasing for the user.**
> "When trying to recall something effortfully — for example, after a worked example, before checking the answer — closing your eyes briefly may help. Originally validated in eyewitness-memory contexts. *(Not specifically tested for AI-led study sessions.)*"

### 4c. Expressive writing before high-stakes tasks

**Claim.** A brief writing exercise about test-related anxiety, performed before a high-stakes test, improved performance — interpreted as freeing WM previously occupied by intrusive worry (Ramirez & Beilock 2011).

**Phrasing for the user.**
> "If you're feeling anxious about an upcoming exam, research suggests that writing for ~10 minutes about your test-related concerns beforehand can improve performance, by freeing working memory from intrusive worry. *(Originally tested for math anxiety; generalization is research-stage.)*"

---

## Strategy 5 — Pacing and offloading

**Claim.** Spreading study sessions over time, and using external aids (notes, lists) instead of holding things in WM, improves learning. (Risko & Gilbert 2016 on cognitive offloading; spacing-effect literature pre-dates CLT but is consistent with it.)

**When to suggest.** The user is trying to cram or hold many things in their head simultaneously.

**Phrasing for the user.**
> "Working memory is the bottleneck. Two evidence-supported moves: (1) spread study sessions across days rather than massing them, and (2) offload anything possible to paper or notes — don't try to hold structures in your head when you can put them on the page."

This one has stronger evidence than strategies 1–4 (the spacing effect is one of the most replicated findings in cognitive psychology) but is included here because the *application to a study-session-with-AI* is research-stage.

---

## How to package these in output

When suggesting any learner-side strategy:

1. **Lead with the core effect-based redesign** of the material (from `effects-catalog.md`). That's higher-confidence work.
2. **Then offer learner-side strategies as adjuncts**, prefixed with their research-stage status.
3. **Cite the original study briefly** (year + author lastname is enough) so the human can investigate.

Example output snippet:

> *Material redesign (high confidence — applies CLT effects 1, 4, 6):*
> [Worked example with integrated diagram, redundant text removed]
>
> *Optional learner-side strategies (research-stage, not validated for AI-led study):*
> - Trace the labeled pathways with your finger as you read (Sepp 2019).
> - If anxious before the exam, try a 10-minute expressive writing session (Ramirez & Beilock 2011).

This separation lets the user calibrate their own credence in each suggestion.
