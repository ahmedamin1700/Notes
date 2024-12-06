---
id: 1733475666-geometric-mean-and-standard-deviation
aliases:
  - Geometric Mean and Standard Deviation
tags:
  - statistics
---

# Geometric Mean and Standard Deviation

## geometric mean
  - suitable for **multiplicative processes** (e.g., growth rates).
$$
\text{Geometric Mean} = \sqrt[n]{x_1 \cdot x_2 \cdot \ldots \cdot x_n}
$$
  - used in finance (e.g., CAGR), biology, and agriculture.

## real-world applications
  - calculate growth rates accurately over time.
  - required for positive values (use growth factors).  
  - arithmetic mean gives incorrect results for growth rates.

## geometric standard deviation
  - Measures variability in logarithmic growth processes.
$$
\ln(\text{GSD}) = \sqrt{\frac{\sum_{i=1}^n (\ln(X_i) - \ln(\text{Geometric Mean}))^2}{n}}
$$

where:
  - $X_i$: individual data points
  - $\ln(X_i)$: natural log of each data point
  - $\ln(\text{Geometric Mean})$: natural log of the geometric mean
  - $n$: number of observations

To calculate GSD:
  - Compute deviations of $\ln(X_i)$ from $\ln(\text{Geometric Mean})$.
  - Square, sum, divide by $n$, and take the square root.
  - Exponentiate the result:  
$$
\text{GSD} = e^{\ln(\text{GSD})}
$$
