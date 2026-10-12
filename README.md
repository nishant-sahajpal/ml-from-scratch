# ml-from-scratch

ML algorithms implemented from first principles in NumPy — no scikit-learn for the core logic — each with tests that check it against a known-good reference. The point is to understand the mechanics, not to build a library.

## Approach

- One algorithm per module under `src/ml_from_scratch/`.
- Every algorithm has tests in `tests/` that assert it matches a reference (closed-form solution, or scikit-learn's output within a tolerance).
- Write the test first where it makes sense, then the implementation.
- A short note at the top of each module: the intuition, the maths, and where it breaks down.

## Planned (in rough order)

| Algorithm | Note |
| --- | --- |
| Linear regression (closed form) | Normal equation, then gradient descent |
| Logistic regression | Gradient descent, sigmoid, cross-entropy |
| k-NN | Distance metrics, the curse of dimensionality |
| k-means | Lloyd's algorithm, initialisation matters |
| Decision tree | Gini / entropy splits |
| Neural net (1 hidden layer) | Forward + backprop by hand |

## Layout

```
src/ml_from_scratch/    # the implementations (installable package)
tests/                  # pytest, one file per algorithm
```

## Status

Phase 0 setup. First implementation (linear regression, closed form + tests) lands in Week 3 of the plan.
