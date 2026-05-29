---
description: Kill an underperforming timeline.
---

# /terminate

Terminate a timeline. The label is in: $ARGUMENTS

1. Read the timeline's latest generation in `.claude/flux/evolution/{problem-slug}/`.
2. Autopsy it. This is mandatory. A death with no extracted learning is wasted. Record:
   - cause of death (below threshold, steep decline, known-bad genome, gaming)
   - the genome at death, highlighting the toxic combination
   - learnings as reject-patterns, scoped to the problem context
3. Write the autopsy to `.claude/flux/graveyard/` (see the graveyard README for the entry shape). Move the timeline's record there.
4. Confirm in the TERMINATION format.

Remember the genes are contextual. Flag the toxic pattern for the context it died in, not as a universal rejection. The same genome may be resurrected and thrive in a different world.
