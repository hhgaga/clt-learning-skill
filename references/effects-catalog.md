# Effects Catalog

Each effect below is presented as: **statement → mechanism → conditions → bad example → good example → source**. Apply these as design rules, not laws — the **expertise reversal effect** at the end shows why every other effect inverts for advanced learners.

---

## 1. Worked-example effect

**Statement.** Novices learn problem-solving better by studying complete worked examples than by attempting the equivalent problems.

**Mechanism.** Solving an unfamiliar problem forces a means-ends search (compare current state to goal, find operators to close the gap). This depletes WM with non-schema-building work. Studying a worked solution lets all WM go to recognizing the structure.

**Conditions.** Effective for novices on tasks with a learnable solution structure (math, physics, programming, well-defined procedures). Less useful for ill-structured creative tasks. Reverses for experts (see effect 10).

**Bad example.** "Solve: differentiate f(x) = x² · sin(x) using the product rule." (Novice has no schema for the product rule yet — solving this trains search, not the rule.)

**Good example.** "Here is f(x) = x² · sin(x) differentiated step by step:
- u = x², v = sin(x)
- u' = 2x, v' = cos(x)
- (uv)' = u'v + uv' = 2x·sin(x) + x²·cos(x)

Notice how each factor is differentiated once, then combined."

**Source.** Sweller & Cooper (1985); Sweller, van Merriënboer & Paas (1998).

---

## 2. Completion-problem effect

**Statement.** Partially solved problems where the learner completes the remaining steps work as well as worked examples and force engagement.

**Mechanism.** Pure worked examples can be skimmed without processing. A completion problem requires the learner to study the given partial solution to finish it correctly — embedding self-explanation.

**Conditions.** Bridge between worked examples (full solution) and conventional problems (no solution). Strong for design-oriented domains (programming, circuit design, architecture).

**Bad example.** Asking a beginner to design a binary search from scratch.

**Good example.**
```
Complete this binary search. The structure is given; fill the three blanks.

def binary_search(arr, target):
    lo, hi = 0, len(arr) - 1
    while lo <= hi:
        mid = (lo + hi) // 2
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            lo = ___        # blank 1
        else:
            hi = ___        # blank 2
    return ___              # blank 3
```

**Source.** van Merriënboer (1990); Paas (1992).

---

## 3. Goal-free effect

**Statement.** Replacing "solve for X" with "find as many quantities as you can" reduces extraneous load and improves schema construction.

**Mechanism.** A specific goal triggers means-ends analysis (work backward from goal, set subgoals). A non-specific goal lets the learner just apply any operator they know to the current state, which is exactly the schema-building activity.

**Conditions.** Works well for math, physics, geometry. Less applicable when tasks have a single canonical answer (e.g., proof exercises).

**Bad example.** "A car accelerates from rest for 60 s reaching 120 km/h. What distance did it travel?"

**Good example.** "A car accelerates from rest for 60 s reaching 120 km/h. Calculate any other quantities you can about this motion."

**Source.** Sweller (1988); Ayres (1993).

---

## 4. Split-attention effect

**Statement.** When two information sources must be mentally integrated to be understood, **physically integrate them** (place them spatially or temporally together) instead of separating them.

**Mechanism.** Holding source A in WM while searching source B for a referent burns WM capacity that should go to integration itself.

**Conditions.** Applies when neither source is self-contained. Most relevant for diagram + explanatory text, code + commentary, formula + variable definitions.

**Bad example.**
> See Figure 3 for the geometry. Triangle ABC has angle A equal to 30°, side b equal to 5, and we need to find side a.

(Reader must scroll/glance to Figure 3, hold the diagram in WM, return to the text, etc.)

**Good example.**
Place the labels and known values directly on the diagram:
```
       A (30°)
      /\
   c /  \ b = 5
    /    \
   B------C
       a = ?
```
Followed immediately by the working — no separate figure reference.

**Source.** Tarmizi & Sweller (1988); Chandler & Sweller (1992).

---

## 5. Modality effect

**Statement.** When two visual sources must be integrated, present one in audio (narration) instead of text. This recruits both visual and phonological WM channels.

**Mechanism.** Baddeley's WM model has partially independent visual-spatial and phonological subsystems. Splitting load across both channels effectively expands capacity.

**Conditions.** High element interactivity material. The explanatory text must be short enough for working auditory memory. Useless for low-complexity material (no overload to relieve).

**Bad example.** Animation playing while a paragraph of text scrolls beside it. Both compete for visual WM.

**Good example.** Animation playing with a synchronized voiceover narrating the steps.

**For text-only AI agents:** the modality lever is unavailable — but you can suggest the human read narration aloud, or recommend a text-to-speech setup for diagram-heavy content.

**Source.** Mousavi, Low & Sweller (1995); Tindall-Ford, Chandler & Sweller (1997).

---

## 6. Redundancy effect

**Statement.** When one source is self-sufficient, **remove the second source** — even if the second seems "helpful." Redundant material adds load because learners cannot easily ignore it.

**Mechanism.** Integrated/adjacent material is hard to filter out. Processing redundant content competes with processing the source you actually need.

**Conditions.** When either source alone conveys the full information. Most often: a labeled diagram + paragraph re-describing the diagram.

**Bad example.**
> *(Diagram showing arrows from Heart → Lungs → Heart with chambers labeled.)*
>
> The right ventricle pumps deoxygenated blood through the pulmonary artery to the lungs. From the lungs, oxygenated blood returns through the pulmonary veins to the left atrium...

**Good example.** Diagram with arrows and one-word labels per arrow ("deoxygenated", "oxygenated"). No paragraph.

**Conflict with split-attention.** If the diagram alone is *not* understandable (novice), keep the text and integrate (split-attention). If the diagram alone *is* understandable (intermediate+), drop the text (redundancy). The boundary is the learner's expertise — see effect 10.

**Source.** Chandler & Sweller (1991); Kalyuga, Chandler & Sweller (1998).

---

## 7. Variability effect

**Statement.** Practising a skill across **varied surface contexts** (different stories, settings, parameter ranges) builds more transferable schemas than blocked practice with the same surface form.

**Mechanism.** Variability forces the learner to identify what stays constant (the underlying structure) versus what varies (surface). This is exactly schema abstraction.

**Conditions.** Useful once extraneous load is already low — variability raises load during practice but pays off in transfer. Use after worked examples have introduced the schema.

**Bad example.** Five practice problems all about projectile motion with cannons.

**Good example.** Five practice problems about: cannon, basketball free throw, water from a hose, kicked football, dropped object from a plane — all using the same kinematic equations.

**Source.** Paas & van Merriënboer (1994); Sweller, van Merriënboer & Paas (1998).

---

## 8. Self-explanation effect

**Statement.** Prompting learners to explain *why* each step of a worked example is correct increases germane processing and transfer.

**Mechanism.** Learners often skim worked examples passively. Explicit "why" prompts force the learner to connect the step to a general rule, building the schema rather than memorizing the trace.

**Conditions.** Pairs with worked examples and completion problems. Even simple prompts ("which rule was applied here?") suffice.

**Bad example.** A worked derivation followed by "Now solve these problems."

**Good example.** A worked derivation interleaved with prompts: "**Why does the chain rule apply here, but not in the previous step?**"

**Source.** Renkl (1997); Stark et al. (2002).

---

## 9. Imagining effect

**Statement.** Asking advanced learners to **mentally rehearse** executing a procedure (after they've studied it) improves performance more than further studying.

**Mechanism.** Mental rehearsal exercises the schema in WM, accelerating its automation.

**Conditions.** Only for learners who already have a partial schema — novices have nothing to imagine and just become confused. Works once worked examples have been mastered.

**Bad example.** Telling a novice "imagine yourself solving this differential equation" before they've learned the rules.

**Good example.** After a learner has worked through several integration-by-parts examples: "Without writing anything down, mentally walk through how you'd integrate x·ln(x). Then check by writing it out."

**Source.** Cooper et al. (2001); van Gog et al. (2004).

---

## 10. Expertise reversal effect

**Statement.** Most CLT effects **invert as expertise grows**. Designs that help novices hurt experts, and vice versa.

**Mechanism.** Effects work by reducing WM load relative to the learner's available schemas. Once a learner has the schema, the supports become redundant material competing for WM.

**Specific reversals.**
- *Worked example → conventional problem:* experts learn more from solving than from studying.
- *Integrated text+diagram → diagram alone:* experts find the integrated text redundant.
- *Audio+visual → visual alone:* the audio narration becomes redundant once the learner can read the diagram fluently.

**Conditions.** Track learner expertise. Adjust designs as it grows. This is the single most important meta-effect for any longer learning sequence.

**Practical rule.** When in doubt, ask: "Does this learner already have a schema for this material?" If yes, **strip the scaffolding**.

**Source.** Kalyuga, Ayres, Chandler & Sweller (2003).

---

## 11. Guidance-fading effect (compound)

**Statement.** A learning sequence should start with full worked examples and gradually fade guidance through completion problems to conventional problems.

**Mechanism.** Combines the worked-example effect (helpful for novices) with the expertise reversal effect (worked examples become redundant). Fading is the operational form of "adapt to expertise."

**Conditions.** Default sequencing for any procedural skill domain.

**Bad example.** A textbook chapter with one worked example and twenty conventional problems. Most novices stall.

**Good example.**
1. Two full worked examples with self-explanation prompts.
2. Three completion problems (each fading more steps).
3. Five conventional problems.

**Source.** Renkl & Atkinson (2003); van Merriënboer & Sweller (2005).

---

## 12. Element-interactivity sequencing (intrinsic-load management)

**Statement.** When intrinsic load is too high even after extraneous load is minimized, present the **isolated elements first**, then the integrated whole.

**Mechanism.** Intrinsic load comes from elements that must be processed simultaneously. Temporarily breaking the interactions lets each element be learned serially, then integrated.

**Conditions.** Use when even a clean worked example is overwhelming. Caveat: understanding is incomplete in the isolated phase — the integration phase is essential.

**Bad example.** Teaching electrical circuit analysis by presenting Kirchhoff's voltage law, current law, and Ohm's law all at once in a multi-loop circuit.

**Good example.**
1. Phase 1 — isolated: present each law alone with single-loop circuits.
2. Phase 2 — interacting: present a multi-loop circuit and have the learner apply all three together.

**Related: whole-task vs part-task.** Modern view (van Merriënboer): present a *simplified version of the whole task* first, then expand, rather than learning isolated parts that may not integrate.

**Source.** Pollock, Chandler & Sweller (2002).

---

## Newer methods (Paas & van Merriënboer 2020)

These are less well-established than effects 1–12. Treat as candidates worth applying when standard effects are insufficient.

### Collective working-memory effect
Multiple learners collaborating on a complex task share WM load. Use for tasks too high in element interactivity for any individual.
- *Note for AI use:* not directly transferable, but suggests that for very dense material, splitting it across multiple chat turns / agents may help.

### Gesturing / tracing
Having learners trace or gesture along a diagram offloads WM to motor representation.
- *AI relevance:* you can suggest the human trace a diagram with their finger or write key terms by hand.

### Motivational and emotional design
Warm colors, expressive faces, narrative framing increase invested mental effort. Distinct from making content "easier" — it makes the learner *willing* to engage.

### Environmental load reduction
- Reduce decoration, visual noise.
- For high-stakes tests, brief expressive writing about anxiety improves performance (Ramirez & Beilock 2011).
- Eye closure during retrieval frees WM previously monitoring the visual field.

These four are **research-stage with respect to AI-mediated learning** and should be presented as suggestions, not prescriptions. See [learner-side-strategies.md](learner-side-strategies.md).

---

## Cross-effect rules of thumb

- **Effects compound.** Worked example + integrated split-attention + redundancy elimination + self-explanation prompts is a coherent stack for a novice on hard material.
- **Effects conflict at expertise boundaries.** Split-attention and redundancy give opposite advice at different expertise levels. Always check expertise first.
- **Intrinsic load is the floor.** No amount of extraneous-load engineering can make intrinsically hard material easy — only schemas can.
- **Total load matters.** Even germane-promoting techniques (variability, self-explanation) can overload novices on high-intrinsic material. Stage them after extraneous load is already low.
