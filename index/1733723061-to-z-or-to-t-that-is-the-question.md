---
id: 1733723061-to-z-or-to-t-that-is-the-question
aliases:
  - To Z or to T, That is the Question
tags:
  - statistics
---

# To Z or to T, That is the Question

## Z distributions

Used when the sample size is large ($n \geq 30$) or population standard deviation ($\sigma$) is known. Assumes normality.

## T Distributions

Used for smaller sample sizes ($n < 30$) or unknown $\sigma$. Has heavier tails to account for additional uncertainty.

## Degrees of Freedom

Degrees of Freedom (df) are the number of independent values in a calculation that can vary while still satisfying a constraint.

**For example:**

In a dataset of $n$ values, if you're calculating the sample mean, one value becomes dependent because the sum of the differences from the mean must equal zero. This reduces the degrees of freedom to
$$
  df = n - 1
$$

- **Key Formula for T or Z Testing**:
$$
  t = \frac{\bar{X} - \mu}{s / \sqrt{n}}, \quad z = \frac{\bar{X} - \mu}{\sigma / \sqrt{n}}
$$
$s$: sample standard deviation, $\sigma$: population standard deviation).  

- The T and Z distributions converge as $n$ increases.
