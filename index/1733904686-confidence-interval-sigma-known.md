---
id: 1733904686-confidence-interval-sigma-known
aliases:
  - Confidence Interval Sigma known
tags:
  - statistics
---

# Confidence Interval Sigma known

- **Confidence Interval Basics**: Confidence intervals estimate a population parameter with a margin of error around a point estimate (e.g., sample mean).
- **Critical Z-Value**: For 95% confidence, the critical Z-value is ±1.96.
- **Standard Error ($SE$)**: Computed as $\frac{\sigma}{\sqrt{n}}$.
- **Example**: Calculate the margin of error and interval for a sample mean using formulas:
$$
\text{CI} = \bar{x} \pm (Z \times SE)
$$

Python Example:
```python
import math

# Inputs
sigma = 4  # Population SD
n = 75  # Sample size
x_bar = 20  # Sample mean
z = 1.96  # Z-value for 95% confidence

# Calculations
se = sigma / math.sqrt(n)
margin_of_error = z * se
lower_bound = x_bar - margin_of_error
upper_bound = x_bar + margin_of_error

# Output
print(f"95% CI: ({lower_bound:.2f}, {upper_bound:.2f})")
```
