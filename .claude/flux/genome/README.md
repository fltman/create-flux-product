# The genome

Agents in FLUX are not written. They are composed from genes. A genome is a set of genes, each weighted 0.0 to 1.0. Two kinds of gene live here:

- `traits/` are personality genes. They shape approach: how the agent thinks, what it values, what it risks.
- `skills/` are domain genes. They shape competence: what the agent knows how to do.

## How a genome looks

```yaml
genome:
  traits:
    analytical: 0.8
    defensive: 0.6
    methodical: 0.5
  skills:
    api-design: 0.9
    testing: 0.7
```

flux-core composes a seed genome per timeline at fork time, then mutation reshapes it generation by generation. No human writes the final weights. Selection finds them.

## Reading a gene weight

- 0.0 means absent. The behavior does not express.
- around 0.5 means present and balanced.
- above 0.7 means dominant. It shapes most of the agent's choices, and at the extreme it becomes a risk.

## Genes are contextual

A gene is not good or bad in the abstract. It is good or bad for an environment. `aggressive: 0.9` is lethal in a compliance-critical banking API and an advantage in a throwaway prototype. The graveyard stores this as contextual risk, not flat rejection. Always ask what kind of problem this is before judging a gene.

## Adding genes

To teach FLUX a new competence, add a skill gene file here following the same shape as the existing ones. To add a new dimension of approach, add a trait gene. Keep the description behavioral: say what the gene makes the agent do at low and high weight, and which genes it is dangerous or safe to combine with.
