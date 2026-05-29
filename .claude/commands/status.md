---
description: Show the fitness landscape.
---

# /status

Render the current evolution as a fitness landscape. Optional argument selects which evolution: $ARGUMENTS

1. Read every timeline in the active `.claude/flux/evolution/{problem-slug}/`. Read each one's latest generation, fitness, and approach.
2. Read the graveyard for this evolution's terminated timelines.
3. Print the landscape:

```
FLUX STATUS - {problem}
========================================================
GENERATION: {n}
ACTIVE TIMELINES
  alpha ##############....  82  gen-005  climbing   {approach}
  beta  #############.....  68  gen-004  plateau    {approach}
  delta ##################  91  gen-003  strong     hybrid (alpha x beta)

TERMINATED
  gamma ####............    18  gen-002  dead       {approach} ({cause})

CROSSOVER OPPORTUNITIES
  alpha x delta : complementary {strength}

WARNINGS
  beta stagnating, consider a mutation spike or termination
========================================================
```

Trend rules: climbing if it gained fitness last generation, plateau if flat across two, declining if it lost fitness. Note crossover opportunities when two living timelines hold complementary strengths. This command only observes, it changes no fitness values.
