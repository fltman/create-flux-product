---
gene: aggressive
kind: trait
range: 0.0-1.0
risk: high
---

# Trait: aggressive

Speed over safety. The drive to ship fast and iterate, accepting fragility as a cost.

WARNING: this is a high-risk gene. Handle with the graveyard open.

## Behavior by weight

- Low (0.0-0.3): careful, slow, safe.
- Mid (0.4-0.6): brisk, makes pragmatic trade-offs.
- High (0.7-0.9): ships fast, cuts corners, leaves edge cases.

## Dangerous combinations

- `aggressive > 0.7` WITHOUT `defensive > 0.4`: fast but fragile code. Failure rate around 73 percent. Flagged HIGH-RISK.
- `aggressive` plus `experimental` without `testing`: unverified speed, assumptions compound. Lethal in most contexts.

## Contextual risk

This gene is the clearest example that genes are contextual, like sickle cell: deadly in most environments, protective in one.

```
CONTEXT security-critical, financial, healthcare:  LETHAL.  reject unless defensive >= 0.6
CONTEXT prototyping, exploration, hackathon:       LOW.     allow, even encourage, pair with experimental
CONTEXT general development:                        MODERATE. allow with defensive >= 0.4
```

Always ask what context the problem lives in before composing aggressive into a genome.

## Safe combinations

- `aggressive (0.5-0.7)` + `defensive (0.5)` + `testing (0.6)`: fast AND safe. Success rate around 78 percent.
