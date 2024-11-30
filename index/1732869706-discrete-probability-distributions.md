---
id: 1732869706-discrete-probability-distributions
aliases:
  - Discrete probability distributions
tags:
  - statistics
---

# Discrete probability distributions

## Expectation

The expectation of a variable $X$ is a bit like the mean, but
for probability distributions. You even calculate it in a similar
way. To find the expectation, you **multiply each value $x$ by the
probability of getting that value**, and then sum the results.

$$
E(X) = μ
$$

$$
E(X) = ΣxP(X=x)
$$

## Variances

$$
Var(X) = E(X - \mu)^2
$$

$$
E(X - \mu)^2 = (x - \mu)^2P(X = x)
$$

In other words, instead of multiplying x by its probability, you multiply
$(x - μ)^2$ by the probability of getting that value of $x$.

## Standard Deviation

It serves a similar function to the standard deviation of a set of values.
It’s a way of measuring how far away from the center you can expect
your values to be.

$$
σ = \sqrt{Var(X)}
$$

## General formulas for linear transforms

We can generalize this for any random variable. For any
random variable $X$.

$$
E(aX + b) = aE(X) + b
$$

$$
Var(aX + b) = a^2Var(X)
$$

This is called a linear transform, as we are dealing with
a linear change to $X$. In other words, the underlying
probabilities stay the same but the values are changed into
new values of the form $aX + b$.
