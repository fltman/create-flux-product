# Winners

Archived winning genomes. When `/select` ends an evolution, the winner's genome is recorded here.

This is the positive half of FLUX's memory. The graveyard records what to reject. This records what proved itself. Future evolutions can seed from a relevant winner instead of starting from a blank genome, and cross-problem learning lives here: can a genome that won an authentication problem seed a database problem? How transferable are traits across domains?

## Entry shape

```
PROBLEM: {what was solved}
CONTEXT: {the problem context}
WON AT: generation {n}, fitness {score}
ORIGIN: {fresh | crossover of X + Y | resurrected from graveyard}

WINNING GENOME:
  traits: {...}
  skills: {...}

WHY IT WON:
  {what made this combination succeed, in one or two lines}
```

## How to use this

- At fork time, check for a winner from a similar problem and context. Seed a timeline from it as one of the parallel approaches.
- Watch transferability. A trait that wins everywhere is a strong default. A trait that wins only in one context belongs to that context, like the genes in the graveyard.
- A winner is a starting point, not a final answer. Selection pressure still decides. The context may have changed.
