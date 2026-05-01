# clt-learning-skill

A Claude Code skill that applies **Cognitive Load Theory (CLT)** to learning material design, review, refactoring, and diagnosis.

Distilled from 30+ years of educational psychology primary literature (Sweller 1988; Sweller, van Merriënboer & Paas 1998; van Merriënboer & Sweller 2005; de Jong 2010; Paas & van Merriënboer 2020).

> **Caveat:** CLT was validated on human classroom learning. Applying it to AI-generated material is a defensible but **unvalidated extrapolation**. Treat this skill as a structured heuristic, not a guaranteed optimization. See [`references/caveats.md`](references/caveats.md).

---

## What it does

When loaded, the skill helps Claude:

1. **GENERATE** — produce study notes, worked examples, flashcards, quiz items, lesson structure that respect working-memory limits.
2. **REVIEW** — audit existing teaching material against 12 canonical CLT effects.
3. **REFACTOR** — rewrite material for a different expertise level (novice ↔ intermediate ↔ expert).
4. **DIAGNOSE** — explain why a chapter feels overwhelming, in terms of intrinsic vs. extraneous load.

It does **not** generate content libraries — it shapes how Claude produces or critiques pedagogical content on demand.

## When it triggers

Phrases like *"make study notes for X"*, *"rewrite this for beginners"*, *"why does this section feel overwhelming?"*, or any explicit mention of cognitive load, working memory, worked examples, split attention, modality effect, expertise reversal.

It deliberately does **not** trigger for general writing, code documentation, marketing copy, or pure information retrieval.

## Install

### As a project-level skill

```bash
cd <your-project>
mkdir -p .claude/skills
git clone https://github.com/hhgaga/clt-learning-skill.git .claude/skills/clt-learning-skill
```

Claude Code auto-discovers `.claude/skills/*/SKILL.md`. Restart Claude Code and the skill becomes available.

### As a user-level skill (all projects)

```bash
git clone https://github.com/hhgaga/clt-learning-skill.git ~/.claude/skills/clt-learning-skill
```

### Verify

In Claude Code, ask: *"Make beginner study notes on X using CLT."* Claude should invoke `clt-learning-skill` and state which effects it applied.

## Repository layout

```
SKILL.md                              # Entry point + decision flow
references/
  effects-catalog.md                  # 12 canonical CLT effects, before/after examples
  decision-trees.md                   # Expertise × intrinsic load → effects matrix
  review-checklist.md                 # 19-point structured review pass
  learner-side-strategies.md          # Gestures, collaboration — marked unverified for AI use
  caveats.md                          # de Jong critique + AI-extrapolation gap
  sources.md                          # Primary papers behind every claim
examples/
  generate-novice-notes.md            # Sample GENERATE output
  review-existing-chapter.md          # Sample REVIEW output
  diagnose-overwhelm.md               # Sample DIAGNOSE output
ROADMAP.md                            # v0.1 → v1.0
CHANGELOG.md
CONTRIBUTING.md
LICENSE                               # MIT
```

## Design principles

- **Cite, don't assert.** Every claim in the skill traces to a primary paper in `sources.md`.
- **Falsifiability over folklore.** de Jong's critique of germane load is included, not hidden.
- **No mind-reading.** The skill describes design choices, not supposed mental processes.
- **Domain-neutral core.** Domain-specific packs (e.g. PT, math, programming) ship as sibling skills.

## Versioning

Semver. v0.x can break the trigger description and reference layout; v1.0 freezes the public surface. See [`ROADMAP.md`](ROADMAP.md).

## Citing

If this skill informs your work:

> hhgaga (2026). *clt-learning-skill* (v0.1.0) [Claude Code skill]. https://github.com/hhgaga/clt-learning-skill

For the underlying theory, cite the primary literature in [`references/sources.md`](references/sources.md), not this skill.

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md). Issues and PRs welcome — especially:
- counter-examples where a recommended effect failed,
- domain-specific worked examples,
- corrections to citations.

## License

MIT. See [`LICENSE`](LICENSE).
