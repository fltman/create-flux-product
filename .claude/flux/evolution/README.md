# Active evolutions

Each problem that FLUX explores gets a directory here, named by a slug of the problem. Inside it, each parallel timeline gets its own subdirectory, and each generation is a file.

```
evolution/
  build-auth-system/
    timeline-alpha/
      gen-001.md
      gen-002.md
    timeline-beta/
      gen-001.md
    timeline-delta/      # a crossover of alpha and beta
      gen-001.md
```

A generation file follows `_TEMPLATE-generation.md`. It carries the genome, the approach, the fitness breakdown, and the mutations that produced the next generation. Reading a timeline top to bottom is reading its evolutionary history.

Timelines do not share a workspace during exploration. Keep each timeline's real work product isolated (its own folder under the timeline directory) so fitness can be measured on real output, not plans. Only the selected winner materializes into the main project.
