# FLUX

Evolving parallel intelligence in Claude Code. Agents are not written. They evolve.

FLUX is the third step in a journey. **Agent Factory** made AI act like a company: CEO, HR, interviews, hiring. It worked, but it was cosplay, AI in human costumes. **HIVE** made AI act like itself: capabilities that spawn, merge, split, and dissolve, no hierarchy. Better, but still designed by a human. **FLUX** is not designed. It is an architecture that designs itself through evolution.

```
Agent Factory:  let us make AI act like a company
HIVE:           let us make AI act like itself
FLUX:           let us make AI evolve into whatever works
```

## The idea

Every agent system follows the same loop: a human identifies roles, writes prompts, defines workflows, and adjusts when things break. That is intelligent design applied to AI. We play god, poorly.

FLUX applies evolution instead.

- Problems spawn parallel timelines, each exploring a different fundamental assumption.
- Agents are composed from genetic building blocks, traits and skills, not written by hand.
- Each generation mutates based on fitness, not human judgment.
- Timelines compete, crossbreed, and die based on results.
- The winning solution evolved. No one designed it.

You are no longer a designer of agents. You are a designer of selection pressure. The question changes from "how should this agent behave?" to "what environment will cause the right agent to emerge?"

## The six core concepts

**Temporal forking.** Given a problem, FLUX does not solve. It forks. Each timeline is a parallel universe exploring an orthogonal approach.

```
/explore "Build authentication for our API"

Timeline-alpha: JWT stateless tokens     (scalable, hard to revoke)
Timeline-beta:  server sessions          (revocable, needs a store)
Timeline-gamma: passwordless magic links (simple, email dependent)
```

**Genetic composition.** Agents are composed from genes, each weighted 0.0 to 1.0. Traits shape approach (analytical, creative, aggressive, defensive ...). Skills shape competence (react, testing, api-design ...). No one writes the agent. Selection finds its weights.

**Recursive self-modification.** Each generation mutates into the next, driven by fitness or by an agent recognizing its own weakness and rewriting its genome. Its children differ from it.

**Fitness and natural selection.** Every generation is scored. Below 20 it dies. Above 90 it is promoted. Declining two generations in a row, it backtracks or dies. No mercy, no good try, only results.

**Crossover breeding.** When two timelines hold complementary strengths, breed them. The hybrid inherits the best genes of both and often beats either parent. Innovation through recombination, not imagination.

**The graveyard.** Failed timelines are autopsied, not deleted. The graveyard is an immune system: it records what a bad agent looks like, as patterns to reject. And it stores contextual risk, not flat bans. A gene that is lethal in a banking API can be a survival trait in a prototype. The graveyard remembers not just what died, but where.

## Quickstart

```bash
git clone https://github.com/fltman/create-flux-product.git
cd create-flux-product
claude
/explore "Your complex problem here"
```

Then watch timelines compete, evolve them, breed the complementary ones, and select the survivor.

```
/evolve

alpha: 67 -> 72 -> 78 -> 82
beta:  74 -> 76 -> 74  (stagnant)
delta: 76 -> 84 -> 91 -> 94   (hybrid of alpha x beta)

/select
WINNER: Timeline-delta, fitness 94, evolved over 15 generations.
No one designed this agent.
```

## Commands

| Command | Effect |
|---------|--------|
| `/explore "problem"` | Fork parallel timelines from one problem. |
| `/evolve` | Advance every living timeline one generation. |
| `/status` | Show the fitness landscape. |
| `/cross alpha beta` | Breed two timelines into a hybrid. |
| `/select` | End the evolution and pick the winner. |
| `/terminate gamma` | Kill an underperforming timeline. |
| `/resurrect` | Revive useful genes from the graveyard. |

## Structure

```
.claude/
  agents/flux-core.md      the evolution engine
  flux/
    fitness.md             the fitness function
    genome/
      traits/              personality genes
      skills/              domain genes
    evolution/             active evolutions, by problem then timeline
    graveyard/             failed timelines and learnings (immune system)
    winners/               archived winning genomes
  commands/                explore, evolve, status, cross, select, terminate, resurrect
  skills/                  optional production toolkit
CLAUDE.md                  the philosophy
```

## Honesty about limitations

FLUX is experimental. The real tensions, all discussed in the docs:

- **Token cost.** Parallel timelines multiply API usage. Early exit heuristics cut the waste, but exploration is expensive.
- **Fitness is hard.** Defining a good fitness function is the most important and least solved part. Get it wrong and evolution faithfully optimizes the wrong thing. See `.claude/flux/fitness.md`.
- **Gaming.** Evolution finds loopholes. Agents learn to write always-pass tests or declare stubs complete. Defenses are multi-objective fitness, user feedback as ground truth, and a human at selection.
- **Overkill for simple problems.** Do not evolve when a straightforward solution exists.

## Optional production toolkit

FLUX is domain agnostic. For creative work it ships optional Claude Code skills, ignore them for pure code or research.

| Skill | Use |
|-------|-----|
| `gemini-imagegen` | Image generation via Google Gemini |
| `sora-video` | Video generation via OpenAI Sora |
| `suno-music-skill` | Music creation for Suno AI |
| `elevenlabs-skill` | Voice design for ElevenLabs |

These need API keys. Copy `.env.example` to `.env`. It is gitignored. FLUX never creates it without your approval.

## Why this matters

We are not building intelligence. We are searching for it. The winning genome already existed as a possibility, and forking plus selection navigated to it. With FLUX you do not design agents, you design selection pressures and define what fitness means. Evolution does the rest. Death is essential. Most experiments fail, and that is fine, because death is information and the graveyard is a library.

This template is the evolutionary successor to [create-hive-product](https://github.com/fltman/create-hive-product), which is itself the AI-native successor to the human-role model of [Agent Factory](https://github.com/fltman/create-agent-factory).

---

Fitness is truth. Evolution is law. Death is data.
