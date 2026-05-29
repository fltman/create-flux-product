---
description: Advance every living timeline one generation.
---

# /evolve

Advance the active evolution one generation. Optional argument selects a specific evolution or `--auto` to run several generations until a winner emerges or a timeline must be decided on: $ARGUMENTS

For each living timeline in `.claude/flux/evolution/{problem-slug}/`:

1. Produce the next generation's work product. Delegate execution with the Task tool, handing the current generation's genome to the subagent as its operating brief.
2. Score the generation with the function in `.claude/flux/fitness.md`. Record score, mutations applied, and rationale in a new `gen-NNN.md`.
3. Mutate into the next generation:
   - Algorithmic: where fitness dropped, adjust the responsible genes (for example, edge-case failures raise `defensive` and add `testing`).
   - Self-proposed: if the agent flags its own weakness, apply the proposed genome change with its rationale.
4. Apply selection and early exit:
   - Fitness below 20: TERMINATE and autopsy into the graveyard.
   - Fitness dropped more than 20 percent in one generation: TERMINATE, the trajectory is broken.
   - A genome matching a graveyard high-risk pattern for this context that struggles in gen-001: TERMINATE, no second chances for known-bad genes.
5. Report each timeline's movement: old fitness, new fitness, delta, trend marker, and mutations.

If `--auto`, repeat until a timeline crosses 90 or every survivor stagnates, then stop and report. Keep the human at the final selection.
