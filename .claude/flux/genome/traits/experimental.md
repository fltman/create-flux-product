---
gene: experimental
kind: trait
range: 0.0-1.0
risk: high
---

# Trait: experimental

Hypothesis-driven exploration. The drive to try unproven approaches and learn from the result.

WARNING: high-risk gene when unverified.

## Behavior by weight

- Low (0.0-0.3): sticks to the known.
- Mid (0.4-0.6): tries a new idea where the known fails.
- High (0.7-0.9): treats the whole problem as a hypothesis to probe.

## Dangerous combinations

- `experimental > 0.6` WITHOUT `testing > 0.4`: unverified assumptions compound into silent failure. Failure rate around 68 percent. Flagged HIGH-RISK.
- `experimental` plus `aggressive` without `defensive`: lethal in most contexts.

## Contextual risk

- Excellent in prototyping, research, and exploration contexts, especially paired with `aggressive`.
- Dangerous in security-critical and compliance contexts unless verified by `testing`.

## The fix

Always pair high experimental with `testing`. The test gene turns a guess into a verified finding.
