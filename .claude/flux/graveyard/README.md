# The graveyard

Failed timelines are not deleted. They are autopsied. This is FLUX's immune system.

The graveyard does not record what a good agent looks like. It records what a bad one looks like, as patterns to reject. In biology this is negative selection: the immune system does not memorize every pathogen, it memorizes what to reject. Knowing what fails is often more valuable than knowing what succeeds.

## Contextual risk, not flat rejection

A gene is not universally toxic. `aggressive: 0.9` is lethal in a banking API and an advantage in a throwaway prototype, like the sickle cell gene: deadly in most environments, protective against malaria in one. So the graveyard stores risk per context, never a blanket ban.

```
GENE: aggressive
CONTEXT security-critical, financial, healthcare:  LETHAL.   reject unless defensive >= 0.6
CONTEXT prototyping, exploration, hackathon:       LOW.      allow, even encourage
CONTEXT general development:                        MODERATE. allow with defensive >= 0.4
```

The graveyard remembers not just what died, but where it died. A buried genome can be resurrected and celebrated in a different context. See `/resurrect`.

## Autopsy entry shape

Every termination writes one entry here:

```
TIMELINE: {problem-slug} / timeline-{label}
DIED: generation {n}, fitness {score}
CONTEXT: {the problem context}
CAUSE: {below threshold | steep decline | known-bad genome | gaming}

GENOME AT DEATH:
  {the toxic combination, highlighted}

LEARNINGS (reject-patterns, scoped to context):
  ! {pattern} -> reject in {context}
```

## Seed knowledge

FLUX starts with patterns already known to kill, from prior evolutions. See `dangerous-genes.md`. Check it before composing any genome.
