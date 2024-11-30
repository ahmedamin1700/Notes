---
id: 1732956981-geometric-distributions
aliases:
  - Geometric Distributions
tags:
  - statistics
---

# Geometric distributions

## Situations
1. You run a series of independent trials.
2. There can be either a success or failure for each trial, and the 
probability of success is the same for each trial.
3. The main thing you’re interested in is how many trials are needed in 
order to get the first successful outcome.

$$
P(X=r) = p q^r-1
$$

where $p$ is the probability of success, and $q = 1 – p$ the probability of failure.

## Inequalities

For the number of trials needed for a success to be greater 
than $r$, there must have been $r$ failures.

$$
P(X>r) = q^r
$$

$$
P(X \leq r) = 1 - q^r
$$

## Expectation

The expectation is 1 divided by the probability of success.

$$
E(X) = \frac{1}{p}
$$

## Variance

$$
Var(X) = \frac{q}{p^2}
$$
