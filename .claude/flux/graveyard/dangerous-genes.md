# Dangerous genes

Seed patterns the graveyard already knows kill agents. Check this before composing a genome. These emerged from evolutionary pressure, not human design. The patterns that survive do not need to be flagged, they prove themselves.

## High-risk combinations

```
! aggressive > 0.7  WITHOUT  defensive > 0.4
  result: fast but fragile code
  failure rate: ~73%

! experimental > 0.6  WITHOUT  testing > 0.4
  result: unverified assumptions compound into silent failure
  failure rate: ~68%

! creative > 0.8  WITHOUT  methodical > 0.3
  result: never converges, endless exploration
  failure rate: ~54%
```

## Safe combinations

From winner analysis. Not guarantees, but proven baselines.

```
+ analytical (0.7-0.9) + defensive (0.4-0.6) + testing (0.6-0.8)
  success rate: ~89%

+ creative (0.5-0.7) + methodical (0.4-0.6)
  success rate: ~82%   innovative but ships

+ aggressive (0.5-0.7) + defensive (0.5) + testing (0.6)
  success rate: ~78%   fast AND safe
```

## How to use this

- At fork time, avoid the high-risk combinations for the problem context.
- Remember contextual risk. The same gene can move from LETHAL to encouraged when the context changes. A high-risk pattern in a banking API may be exactly right in a hackathon prototype.
- As real evolutions run, append newly discovered patterns here so the immune system grows.
