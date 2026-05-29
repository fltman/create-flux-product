---
description: End the evolution and pick the winner.
---

# /select

End the active evolution and select the winner. Optional argument names the evolution: $ARGUMENTS

1. Read every living timeline's latest generation. Identify the highest fitness survivor.
2. Before committing, sanity-check against gaming: high fitness with suspicious signals (perfect tests but low coverage, zero errors but empty catch blocks, minimal code that does little) means the score may be gamed. Surface the suspicion and let the human confirm. user_satisfaction is the tiebreaker and it cannot be gamed.
3. Archive the winning genome to `.claude/flux/winners/` with the problem, the final genome, the generation count, the origin (fresh or crossover), and what made it win.
4. Present the result:

```
WINNER: Timeline-{label}
Fitness: {score}
Generations: {n}
Origin: {fresh | crossover of X + Y}
Final genome: {traits and skills}

No one designed this agent. It evolved through:
  {k} parallel explorations
  {d} extinctions
  {c} crossovers
  {g} total generations
```

5. Offer to materialize the winner's work product as the real deliverable.

The winning genome already existed as a possibility. Forking and selection found it. You navigated to the solution, you did not design it.
