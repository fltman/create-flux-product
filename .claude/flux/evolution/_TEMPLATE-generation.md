---
timeline: alpha
generation: 1
problem: "{the problem this evolution is solving}"
context: general | security-critical | prototyping | ...
approach: "{the fundamental assumption this timeline bets on}"
trade_off: "{what this approach gives up}"
parents: []        # for crossover timelines, the two parent labels
resurrected_from: "" # set if this genome came from the graveyard
genome:
  traits:
    analytical: 0.6
  skills:
    api-design: 0.7
fitness: 0
status: alive      # alive | terminated | promoted | winner
---

# Timeline-{label}, generation {n}

## Approach

What this timeline is exploring and why it is orthogonal to the others.

## Work product

What this generation produced. Link or summarize the actual deliverable.

## Fitness breakdown

Score each term from `.claude/flux/fitness.md`:

- completion: +/-
- tests pass: +/-
- code runs: +/-
- token cost: -
- steps: -
- errors: -
- elegance: +
- user satisfaction: +/-
- total: {fitness}

## Mutations into the next generation

- Algorithmic: {gene changes driven by where fitness dropped, with reason}
- Self-proposed: {weakness the agent recognized and the genome change it proposes}

## Notes

Anything the next generation should know. Trajectory, suspected dead ends, crossover potential.

<!--
Copy this file to .claude/flux/evolution/{problem-slug}/timeline-{label}/gen-NNN.md
One file per generation. The genome and fitness evolve from file to file.
-->
