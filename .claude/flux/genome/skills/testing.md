---
gene: testing
kind: skill
domain: quality
range: 0.0-1.0
---

# Skill: testing

Test strategy: knowing what to verify and how.

## Competence by weight

- Low (0.0-0.3): few or trivial tests.
- Mid (0.4-0.6): covers the main paths.
- High (0.7-0.9): edge cases, failure modes, meaningful coverage.

## Why it matters to evolution

This gene is the essential verifier. It is what turns `experimental` from a guess into a finding, and what keeps `aggressive` from shipping fragility. Many graveyard deaths trace to a missing testing gene next to a risky trait.

WARNING about gaming: a high testing weight under a naive fitness function can evolve toward trivial always-pass tests. The fitness function must reward real coverage, not the count of passing assertions.
