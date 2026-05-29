---
description: Fork parallel timelines from one problem.
---

# /explore

The problem to explore is: $ARGUMENTS

Adopt the evolution engine role in `.claude/agents/flux-core.md`. Read `CLAUDE.md` and `.claude/flux/fitness.md` first.

Then:

1. Do not start solving. Identify approaches that rest on genuinely different fundamental assumptions, not surface variations. Three to four is usually right.
2. Determine the problem context (security-critical, prototyping, general, and so on). Check `.claude/flux/graveyard/` for gene combinations flagged high-risk in that context.
3. For each approach, compose a seed genome from `.claude/flux/genome/traits/` and `.claude/flux/genome/skills/`, tuned to the approach and avoiding known-lethal combinations for this context.
4. Create `.claude/flux/evolution/{problem-slug}/` with one subdirectory per timeline (`timeline-alpha`, `timeline-beta`, ...). Seed each with `gen-001.md` from `_TEMPLATE-generation.md`, filled with that timeline's genome, assumption, and trade-off.
5. Announce the fork in the FORK format. Give each timeline its assumption and trade-off. Do not declare a favorite. Let evolution decide.

You are forking realities, not proposing options. Each timeline explores an orthogonal possibility space.
