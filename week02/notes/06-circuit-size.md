# Circuit Size of Fault-Tolerant Procedures

Tuesday, November 11, 2025

## [Lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@f7e6c9a9cbb1446f952c4e3cde89ff62/block-v1:xPRO+QCRx2+R13+type@vertical+block@2d15f2d064d848e1a23df5ce48451516)


## Review

Quantum error correction only works if the physical error rate, $p$, is below a threshold, $p_\text{th}$.  

For the surface code, $p_\text{th} \approx 1\%$.

## Logarithm

A logarithm is the _inverse_ operation of exponentiation.

It answers the question:

"To what _power_ must a _base_ be raised to produce a _given_ number?

### Common Logarithm

  $\log_{\text{10}}(100) = 2$

  base = 10

  power = 2

  number = 100

### Natural Logarithm

  $\ln(x) = log_{\text{e}}(x)$

  $\ln(e^3) = 3$

  base = $e \approx 2.718$

  power = 3

  number = $e^3$



## What is the _cost_ of fault tolerance?

How many erroneous error-prone gates do we need in order to construst an error-free circuit system?

$d^k$ => levels of recursion, increase exponentially

### Goal

Simulate N-Gate circuit with probability of failure < $\epsilon$

each gate = $\epsilon / N$


## Necessity for Quantum Computation

In the world of quantum computation, fault tolerance is not just a _desirable_ philosophy, it is a _necessary_ philosophy.

We do not know of any other way to reduce errors in quantum systems until they are tolerable.

