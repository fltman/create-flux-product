---
description: Breed two timelines into a hybrid.
---

# /cross

Breed two timelines. The two labels are in: $ARGUMENTS

1. Read the latest generation of both parent timelines in `.claude/flux/evolution/{problem-slug}/`.
2. Build the hybrid genome by unioning the strongest genes of each parent. Where both carry the same gene, take the higher weight. Resolve trait tension toward the combination the graveyard has not flagged for this context.
3. Set the hybrid's starting fitness to an inherited baseline near the higher parent, acknowledging it begins with proven genes.
4. Create a new timeline subdirectory (`timeline-delta`, then `timeline-epsilon`, ...) with `gen-001.md` holding the hybrid genome, the combined approach, and both parents named as origin.
5. Announce it in the CROSSOVER format.

The hybrid reimplements from the combined genome rather than literally merging code. It inherits the traits and skills, not the text. Crossover often produces a solution better than either parent. That is the point.
