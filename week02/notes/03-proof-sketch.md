# Classical Threshold Theorem:  Proof Sketch

Saturday, November 8, 2025

## Discussion

• Compute on encoded data.  Do no decode data as you go along.

• The circuit construction is composed of two parts:

  1. Logical gate - a gate acting on the encoded data

  2. Error correction - based on majority votiing

## What is the probability of failure?

Output is incorrect only if __two__ or more gates fail.

  - number of gates = 6

  - number of failures = 2

## Binomial Coefficient

In combinatorics, "6 choose 2" refers to the binomial coefficient.

Here, $n$ = 6 and $k$ = 2:

$\binom{n}{k} = \frac{n!}{k!(n-k)!}$

15 $P^2$ < P

The failure probability is often expanded as a series in powers of $p$:

$P_{fail} = a_1p + a_2 p^2 + a_3 p^3 + \cdots$

"To the leading order in $p$" means keep only the lowest-power, non-zero term in $p$.

This is the __dominant__ contribution when $p$ is very small (e.g. $p = 10^{-3}$), because higher powers like $p^2$ or $p^3$ become negligible.


## Binomial Theroem

The binomial theorem describes the algebraic expansion of powers of a binomial expression $(x + y)^n$.

$\boxed{(x + y)^n = \sum_{k=0}^{n} \binom{n}{k} x^{n-k} y^k}$


## Level 1 Encoding

You can recurse on this encoding and build a fault-tolerant circuit of arbitrary size.

