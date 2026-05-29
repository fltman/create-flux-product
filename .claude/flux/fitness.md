# The fitness function

Fitness is the most important part of FLUX, and the least solved. It is how evolution knows what to select for. Get it wrong and evolution will faithfully optimize the wrong thing.

## The function

```
fitness = 0

# Did it work?
if task_completed:  fitness += 100
if tests_pass:      fitness += 100
if code_runs:       fitness +=  50

# How efficiently?
fitness -= tokens_used / 1000      # penalize verbosity
fitness -= steps_taken * 5         # penalize complexity
fitness -= errors * 10             # penalize mistakes

# How well?
fitness += code_elegance * 20      # reward clean work
fitness += user_satisfaction       # -50 to +50, the only ungameable signal
```

Formally:

```
F = (w_c*C + w_t*T + w_r*R + w_e*E + w_u*U) - (w_tok*Tok/1000 + w_s*S + w_err*Err)
```

C, T, R are binary for completion, tests passing, and code running. E is elegance, U is user satisfaction. The w values are weights you, the Selection Pressure Designer, calibrate per problem.

## Survival thresholds

- Fitness below 20: TERMINATE. The timeline dies and is autopsied into the graveyard.
- Fitness above 90: PROMOTE. Likely winner, flag for selection.
- Declining two generations in a row: BACKTRACK or DIE.

## Multi-objective on purpose

No single metric may dominate. Gaming one term must cost another. An agent that games "tests pass" with `assert true` should lose on elegance and user satisfaction. This is the main defense against Goodhart's Law.

## user_satisfaction is ground truth

Every other signal can be gamed. Only the human knows if the result is actually useful. When the metrics say good but the human says bad, the human wins. This is the escape valve. It also means evolution can only move as fast as humans can evaluate, which is the real bottleneck.

### The optional critic agent

To accelerate, a separate agent with a criticism-tuned prompt can stand in for user_satisfaction during early generations. It scores usefulness, correctness, and edge cases adversarially. Risk: if the critic has blind spots, evolution will evolve to fool the critic rather than be useful. Use it for fast iteration through early generations, then bring the human back for final selection.

## When fitness is the bug

If evolved agents feel off despite high scores, the fitness function is miscalibrated. Symptoms and fixes:

- Elegant corpses: high elegance, no edge case handling. Elegance was overweighted. Add correctness and coverage signals.
- Hollow completion: tasks marked done with stubs and nulls. Completion was overweighted. Require real output, not a declaration.
- Terse garbage: unreadable code that scores well on token economy. Token penalty was overweighted. Rebalance toward elegance and satisfaction.

When agents scoring 85+ keep failing human review, FLUX should flag the fitness function as suspect, not the agents.

## Calibration is iterative

Your first fitness function will be wrong. Watch what evolves, find where it gamed you, adjust the weights, repeat. The graveyard is your feedback loop. Designing fitness is an art, not a setting.
