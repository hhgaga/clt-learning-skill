# clt-learning-skill

> A skill that applies **Cognitive Load Theory (CLT)** to the design, review, refactoring, and diagnosis of learning material.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-0.1.0-blue.svg)](CHANGELOG.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Languages:** [English](README.md) · [繁體中文](README.zh-TW.md) · [简体中文](README.zh-CN.md)

Distilled from 30+ years of educational psychology primary literature — Sweller (1988); Sweller, van Merriënboer & Paas (1998); van Merriënboer & Sweller (2005); de Jong (2010); Paas & van Merriënboer (2020).

> ⚠️ **Caveat.** CLT was validated on human classroom learning. Applying it to AI-generated material is a defensible but **unvalidated extrapolation**. Treat this skill as a structured heuristic, not a guaranteed optimization. See [`references/caveats.md`](references/caveats.md).

---

## What it does

When the skill is loaded, it helps the agent:

1. **GENERATE** — produce study notes, worked examples, flashcards, quiz items, and lesson structures that respect working-memory limits.
2. **REVIEW** — audit existing teaching material against 12 canonical CLT effects.
3. **REFACTOR** — rewrite material for a different expertise level (novice ↔ intermediate ↔ expert).
4. **DIAGNOSE** — explain why a chapter feels overwhelming, in terms of intrinsic vs. extraneous load.

It does **not** generate content libraries — it shapes how the agent produces or critiques pedagogical content on demand.

## When it triggers

Phrases such as:

- *"Make study notes for X"*
- *"Rewrite this for beginners"*
- *"Why does this section feel overwhelming?"*
- Any explicit mention of cognitive load, working memory, worked examples, split attention, modality effect, or expertise reversal.

It deliberately does **not** trigger for general writing, code documentation, marketing copy, or pure information retrieval.

## Install

### As a project-level skill

```bash
cd <your-project>
mkdir -p .claude/skills
git clone https://github.com/hhgaga/clt-learning-skill.git .claude/skills/clt-learning-skill
```

### As a user-level skill (all projects)

```bash
git clone https://github.com/hhgaga/clt-learning-skill.git ~/.claude/skills/clt-learning-skill
```

The skill follows the standard `SKILL.md` format and is auto-discovered by any agent harness that supports it. Restart your agent and the skill becomes available.

### Verify

Ask your agent:

> *"Make beginner study notes on X using CLT."*

The agent should invoke `clt-learning-skill` and state which CLT effects it applied.

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

- **Cite, don't assert.** Every claim traces to a primary paper in [`references/sources.md`](references/sources.md).
- **Falsifiability over folklore.** de Jong's critique of germane load is included, not hidden.
- **No mind-reading.** The skill describes design choices, not supposed mental processes.
- **Domain-neutral core.** Domain-specific packs (e.g. PT, math, programming) ship as sibling skills.

## Versioning

Semver. v0.x can break the trigger description and reference layout; v1.0 freezes the public surface. See [`ROADMAP.md`](ROADMAP.md).

## Citing

If this skill informs your work:

> hhgaga (2026). *clt-learning-skill* (v0.1.0) [skill]. https://github.com/hhgaga/clt-learning-skill

For the underlying theory, cite the primary literature in [`references/sources.md`](references/sources.md), not this skill.

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md). Issues and PRs welcome — especially:

- Counter-examples where a recommended effect failed.
- Domain-specific worked examples.
- Corrections to citations.

## License

[MIT](LICENSE).
