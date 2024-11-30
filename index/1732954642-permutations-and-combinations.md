---
id: 1732954642-permutations-and-combinations
aliases:
  - Permutations and Combinations
tags:
  - tatistics
---

# Permutations and Combinations

## Generalize a formula for arranging duplicates

To find the number of arrangements, start off by calculating the number of
arrangements for the n objects as if they were all unique. Then divide by
the number of ways in which the k objects (the ones that are alike) can be
arranged.

$$
\frac{n!}{k!}
$$

Imagine you want to arrange n objects, where k of one type are alike, and j of
another type are alike, too. You can find the number of possible arrangements by
calculating:

$$
\frac{n!}{j!k!}
$$

## Permutations

A permutation is the number of ways in which you
can choose objects from a pool, and where the order in
which you choose them counts. It's a lot more specific
than a combination as you want to count the number
of ways in which you fill each position.

$$
^nP_r = \frac{n!}{(n-r)!}
$$

## Combinations

A combination is the number of ways in which you
can choose objects from a pool, without caring about
the exact order in which you choose them. It's a lot
more general than a permutation as you don't need to
know how each position has been filled. It's enough to
know which objects have been chosen.

$$
^nC_r = \frac{n!}{r!(n-r)!}
$$
