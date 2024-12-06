---
id: 1732960194-binomial-distribution
aliases:
  - Binomial Distribution
tags:
  - statistics
---

# Binomial Distribution

## Situations

1. You’re running a series of independent trials.
2. There can be either a success or failure for each trial, and the 
probability of success is the same for each trial.
3. There are a finite number of trials.

$$
P(X=r) = ^nC_r p^r q^n-r
$$

## Expectation

$$
E(X) = np
$$

## Variance

$$
Var(X) = npq
$$

## Standard Deviation

$$
Std(X) = \sqrt{n \cdot p \cdot q}
$$

1. **Using PMF (Probability Mass Function):**
   Calculate the probability of exactly $r$ successes.

   Example:
   A coin is flipped 5 times ($n = 5$) with $p = 0.5$.
   What is the probability of getting exactly 3 heads ($r = 3$)?

   ```python
   from scipy.stats import binom

   n, p, r = 5, 0.5, 3
   pmf_result = binom.pmf(r, n, p)
   print(f"P(X = {r}) = {pmf_result:.4f}")
   ```

   Output:
   $P(X = 3) = 0.3125$

2. **Using CDF (Cumulative Distribution Function):**
   Calculate the probability of at most $r$ successes ($P(X \leq r)$).

   Example:
   A die is rolled 10 times ($n = 10$) with $p = \frac{1}{6}$.
   What is the probability of getting at most 2 sixes ($X \leq 2$)?

   ```python
   n, p, r = 10, 1/6, 2
   cdf_result = binom.cdf(r, n, p)
   print(f"P(X <= {r}) = {cdf_result:.4f}")
   ```

   Output:
   $P(X \leq 2) = 0.9302$

### Summary of Functions:
- **PMF:** $P(X = r)$ gives the probability of exactly $r$ successes.
- **CDF:** $P(X \leq r)$ gives the cumulative probability up to $r$ successes.
