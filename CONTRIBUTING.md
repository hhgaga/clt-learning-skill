# Contributing

Thanks for considering a contribution. This skill is small and opinionated; that's by design.

## What's in scope

- **Counter-examples** — places where a recommended CLT effect produced a worse result than the alternative. These are the most valuable bug reports.
- **Domain worked examples** — well-marked, easy to read, with a one-line note on which effects were applied.
- **Citation fixes** — wrong page, wrong year, misattributed claim. Open a PR with the correct primary source.
- **Trigger description tightening** — cases where the skill fires for the wrong task or fails to fire for the right one.

## What's out of scope (for v0.x)

- Adding more learner-side strategies without primary-literature backing — see `references/learner-side-strategies.md` for the bar.
- Domain-specific reference packs as part of this repo. Ship them as a sibling skill (e.g. `clt-learning-skill-pt`) and link from `ROADMAP.md`.
- Tooling, build systems, CI. A skill is just markdown.

## Workflow

1. Open an issue first for anything beyond a typo or citation fix. Describe the problem, not the proposed wording.
2. PRs should touch one concern at a time.
3. New claims need a citation in `references/sources.md`. No claim, no merge.
4. Match the existing voice: terse, falsifiable, no marketing language.

## Code of conduct

Be civil. Disagree about pedagogy, not people. Maintainer reserves the right to close threads that aren't going anywhere.

## License

By contributing you agree your contribution is licensed under the MIT license, same as the rest of the repo.
