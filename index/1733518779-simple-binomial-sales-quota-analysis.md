---
id: 1733518779-simple-binomial-sales-quota-analysis
aliases:
  - Simple Binomial Sales Quota Analysis
tags:
  - statistics
---

# Simple Binomial Sales Quota Analysis

[video url](https://www.youtube.com/watch?v=FwIguCYyu7o)

1. **Concepts**:
   - Used binomial distribution to find probabilities of achieving sales quotas.
   - $n$: Number of trials (calls), $p$: Success rate, $x$: Quota threshold.
   - Example: Joan $p=0.75, n=10$ vs. Margot $p=0.45, n=16$.

2. **Approach**:
   - Used **cumulative distribution function (CDF)** to calculate $P(X \geq 6) = 1 - P(X < 6)$.
   - Joan: $P(X \geq 6) = 0.922$, Margot: $P(X \geq 6) = 0.802$.

3. **Python Code**:
   Below is Python code replicating the calculations using the SciPy library:

```python
from scipy.stats import binom

# Joan's parameters
n_joan = 10
p_joan = 0.75
x_joan = 6

# Calculate P(X >= 6) for Joan
p_joan_at_least_6 = 1 - binom.cdf(x_joan - 1, n_joan, p_joan)
print(f"Joan's probability of at least 6 sales: {p_joan_at_least_6:.3f}")
```

```python
# Margot's parameters
n_margot = 16
p_margot = 0.45
x_margot = 6

# Calculate P(X >= 6) for Margot
p_margot_at_least_6 = 1 - binom.cdf(x_margot - 1, n_margot, p_margot)
print(f"Margot's probability of at least 6 sales: {p_margot_at_least_6:.3f}")
```

```python
# Bonus Question 1: Calls needed for Margot to match Joan
target_prob = p_joan_at_least_6
calls = 16
while True:
    p_match = 1 - binom.cdf(x_margot - 1, calls, p_margot)
    if p_match >= target_prob:
        break
    calls += 1
print(f"Margot needs to make at least {calls} calls to match Joan's performance.")
```

```python
# Bonus Question 2: Success rate needed for Margot to match Joan
success_rate = 0.45
while True:
    p_match = 1 - binom.cdf(x_margot - 1, n_margot, success_rate)
    if p_match >= target_prob:
        break
    success_rate += 0.001
print(f"Margot needs a success rate of at least {success_rate:.2f} to match Joan's performance.")
```

4. **Insights**:
   - Joan’s higher success rate compensates for her lower call volume.
   - Margot would need either increased calls or a higher success rate to match Joan’s probability.
