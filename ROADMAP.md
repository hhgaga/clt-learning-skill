# Roadmap — clt-learning-skill

Public roadmap for `hhgaga/clt-learning-skill`. Versions follow semver.

## v0.1.0 — Initial public release (current)

- SKILL.md + 6 reference files (effects-catalog, decision-trees, review-checklist, learner-side-strategies, caveats, sources)
- MIT license, README, CHANGELOG, CONTRIBUTING
- 3 example outputs (GENERATE / REVIEW / DIAGNOSE)
- Distributed as a project-level Claude Code skill (`.claude/skills/clt-learning-skill/`)

## v0.2.0 — Examples & evals

- 5+ additional worked examples across domains (anatomy, programming, math)
- Eval harness: a small set of "before/after" prompts to measure whether the skill changes outputs in the predicted direction
- Add `evals/` folder with reproducible prompts

## v0.3.0 — Domain packs

- Optional domain reference files users can opt into:
  - `references/domain-stem.md` — math/physics specifics
  - `references/domain-procedural.md` — motor / clinical procedure learning
- Keep core SKILL.md domain-agnostic

## v0.4.0 — User-side feedback loop

- Issue templates for "this advice didn't work for my learner"
- Living FAQ in README from real reports
- Tighten the "when NOT to apply" boundary based on misfires

## v1.0.0 — Stable

- Frozen SKILL.md trigger description (only patch-level edits after this)
- Documented compatibility with specific Claude Code versions
- A second-party review (someone other than the author) of the effects catalog against primary literature

## Sibling repo (separate, public)

- `hhgaga/clt-learning-skill-pt` — Physical Therapy domain customization (biomechanics, anatomy, kinesiology). Forks v0.1.0 of this skill, layers PT-specific worked examples and vocabulary. Tracked separately so the general skill stays domain-neutral.

## Out of scope

- Bundling LLM-generated study materials (this is a skill, not a content library).
- Anything that requires running code inside the skill — Claude Code skills are prompts + references, not executables.
- Validation claims beyond "structured heuristic distilled from primary literature." Empirical validation for AI-mediated learning is an open research question; see `references/caveats.md`.
