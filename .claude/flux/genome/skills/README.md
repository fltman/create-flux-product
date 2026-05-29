# Skill genes

Domain knowledge genes. These are the competences a genome can carry. The four here are seeds, not a fixed set. Add a skill gene whenever evolution needs a competence the current genome cannot express.

To add one, copy the shape of an existing skill gene:

```
---
gene: your-skill
kind: skill
domain: backend | frontend | data | quality | ...
range: 0.0-1.0
---

# Skill: your-skill

One line on the competence.

## Competence by weight
- low / mid / high behavior

## Pairs well with
- traits and problem types this skill thrives alongside
```

Keep descriptions behavioral and weight-aware, so flux-core can reason about what a given weight will actually produce.
