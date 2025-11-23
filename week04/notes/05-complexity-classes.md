# Complexity Classes: Deterministic Time

Saturday, November 22, 2025

## Lecturer

Prof. Aram Harrow

Associate Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@d88e1317c7be4690bc631827e5d1a020/block-v1:xPRO+QCRx2+R13+type@vertical+block@9d0136bb3ebb4a3aaf5a9fd3007a0ae9)

## Deterministic Time (DTIME)

A Language, $L$, belongs ($\in$) to DTIME $(f(n))$ if there exists ($\exists$) a Turing machine, $m$, such that $m(x)$ __always halts__ with the correct answer.

This means:

  __accept__ if $x$ $\in$ $L$

  __reject__ if $x$ $\notin$ $L$

in $f(|x|)$ steps

### Example

DTIME($100n^3$)

These are the languages that if my input is $n$ bits, I can solve at most $100n^3$ steps.