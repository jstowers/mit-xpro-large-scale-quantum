# Models of Computing:  Random, Quantum, and Non-Determinism

Saturday, November 22, 2025

## Lecturer

Prof. Aram Harrow

Associate Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@d74eb092f4c942e0a78f9e2db830f52c/block-v1:xPRO+QCRx2+R13+type@vertical+block@34d83759ea4e4129bb74044385103cad)

## Basic Models

1. Circuits

2. Turing machines

These are good ways of describing _deterministic_ computations.

## Randomness

Two ways:

1.  Extra inputs are random bits, or

2.  Gates / Turing machine rules can be random

## Quantum Models

### Characteristics

1. Unitaries

2. Ancillas in state $\ket{0}$

3. Depth, width, and size

### Drawback

Uncontrolled dependence on input size, $n$

Ways around this:

1. Quantum Turing machine - rarely used

2. Classical Turing machine outputs a _quantum_ circuit

## Non-Determinism

Think of __NP__ problems

A classical computer takes the __OR__ of two branches of a computation.

Physically unreasonable form of computation.  

  - Useful in math for thinking of proof systems.

  - Your computer can go into two branches and those branches can branch.

### What does non-determinism mean?

- In the end, if any of those branches _accept_, the overall computer will accepts.

- If all branches _reject_, then the overall computer will reject.