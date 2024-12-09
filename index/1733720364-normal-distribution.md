---
id: 1733720364-normal-distribution
aliases:
  - Normal Distribution
tags:
  - statistics
---

# Normal Distribution

### Summary: **Normal Distribution Overview**

1. **Definition**: The normal distribution, or bell curve, is symmetric with probabilities under the curve summing to 1. The mean (\( \mu \)) defines its position, and the standard deviation (\( \sigma \)) determines its shape (spread).  

2. **Key Features**:
   - **Symmetry**: Left and right halves are identical.
   - **Mean, Median, and Mode**: Align at the curve's peak.
   - **Tails**: Extend infinitely but asymptotically approach zero.

3. **Standard Normal Distribution**: Has \( \mu = 0 \) and \( \sigma = 1 \).  

4. **Probabilities**:
   - **Between -1σ and 1σ**: \( 68.2\% \) of data.  
   - **Between -2σ and 2σ**: \( 95.4\% \).  
   - **Between -3σ and 3σ**: \( 99.7\% \).  

---

### Example Python Code:

#### Plot a Normal Distribution
```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import norm

# Define parameters
mean = 0
std_dev = 1
x = np.linspace(-4, 4, 1000)  # Range of values
pdf = norm.pdf(x, mean, std_dev)  # Probability density function

# Plot
plt.plot(x, pdf, label="Normal Distribution")
plt.title("Standard Normal Distribution")
plt.xlabel("X")
plt.ylabel("Probability Density")
plt.grid()
plt.legend()
plt.show()
```

#### Calculate Probabilities
```python
# Using SciPy for cumulative probabilities
prob_below_1sd = norm.cdf(1) - norm.cdf(-1)  # P(-1σ ≤ Z ≤ 1σ)
prob_below_2sd = norm.cdf(2) - norm.cdf(-2)  # P(-2σ ≤ Z ≤ 2σ)
prob_above_1sd = 1 - norm.cdf(1)  # P(Z > 1σ)

print(f"P(-1σ ≤ Z ≤ 1σ): {prob_below_1sd:.4f}")
print(f"P(-2σ ≤ Z ≤ 2σ): {prob_below_2sd:.4f}")
print(f"P(Z > 1σ): {prob_above_1sd:.4f}")
```
