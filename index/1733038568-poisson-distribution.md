---
id: 1733038568-poisson-distribution
aliases:
  - Poisson Distribution
tags:
  - statistics
---

# Poisson Distribution

1. **Poisson Distribution Overview**:
  - Models the probability of discrete events over a specific interval (time, space, etc.).
  - Lambda ($\lambda$) represents the mean (expected occurrences per interval).
  - Formula:
    $$
     P(X = x) = \frac{\lambda^x e^{-\lambda}}{x!}
    $$
    $X$: number of occurrences, $e$: natural constant (~2.718).

2. **Applications**:
   - Suitable for rare events or intervals like customer arrivals in a queue.
   - Assumes independence of events and constant expected occurrences.

3. **Python Code for Examples**:

```python
from scipy.stats import poisson

# Parameters
lambda_val = 10  # Expected occurrences (mean)
x_exact = 7  # Exact number of events

# Probability of exactly 7 occurrences
p_exact = poisson.pmf(x_exact, lambda_val)
print(f"Probability of exactly 7 occurrences: {p_exact:.4f}")

# Probability of more than 10 occurrences
p_more_than_10 = 1 - poisson.cdf(10, lambda_val)
print(f"Probability of more than 10 occurrences: {p_more_than_10:.4f}")

# Adjusted interval example: 10 minutes instead of 15 minutes
adjusted_lambda = (10 / 15) * lambda_val
print(f"Expected customers in 10 minutes: {adjusted_lambda:.2f}")
```

4. **Insights**:
   - Probability of $X = 7$: 9% ($P(X=7) = 0.09$).
   - Probability of $X > 10$: 41.7% ($P(X>10) = 0.417$).
   - Adjusting the interval scales $\lambda$ proportionally.
