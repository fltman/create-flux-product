---
gene: defensive
kind: trait
range: 0.0-1.0
risk: low
---

# Trait: defensive

Error handling and edge cases. The drive to anticipate what can go wrong and guard against it.

## Behavior by weight

- Low (0.0-0.3): happy path only, ignores edge cases.
- Mid (0.4-0.6): handles the common failures.
- High (0.7-0.9): guards every boundary, validates inputs, plans for failure.

## Synergies

- With `analytical` and `testing`: the backbone of the most reliable genomes. Success rate around 89 percent.
- The essential counterweight to `aggressive` and `experimental`. It is what makes a fast or exploratory genome survivable.

## Cautions

- Very high defensive with no `bold` or `aggressive` can become over-guarded and verbose, paying an efficiency penalty. Reliability has a cost too.
