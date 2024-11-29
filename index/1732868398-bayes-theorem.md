---
id: 1732868398-bayes-theorem
aliases:
  - Bayes' Theorem
tags:
  - statistics
---

# Bayes' Theorem

Bayes' Theorem provides a way to calculate the conditional probability of an event based on prior knowledge of related events. Given probabilities $P(A)$, $P(B | A)$, and $P(B | A')$, the theorem helps us find $P(A | B)$, the probability of event $(A)$ given that event $(B)$ has occurred. 

The theorem can be expressed as:

$$
P(A | B) = \frac{P(A) \cdot P(B | A)}{P(A) \cdot P(B | A) + P(A') \cdot P(B | A')}
$$

Where:
- $(P(A \cap B) = P(A) \cdot P(B | A))$
- $(P(B) = P(A) \cdot P(B | A) + P(A') \cdot P(B | A'))$

This formula is invaluable for calculating reverse conditional probabilities, especially when not all probabilities are known upfront.
