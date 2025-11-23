# Promise Problems

Saturday, November 22, 2025

## Lecturer

Prof. Aram Harrow

Associate Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@d74eb092f4c942e0a78f9e2db830f52c/block-v1:xPRO+QCRx2+R13+type@vertical+block@f1bbab3f17ff47e5a62adc19d596f0c1)

## Promise Problems

For a __promise problem__, the input is not all strings, but only a _subset_ of strings.

You only need the correct answer for input, $x$, when it belongs to some set, $p$, which is some subset of strings.

The input is _promised_ to be in the subset of strings.

The algorithm only needs to run on strings satisfying the promise.

Promise problems __modify__ all other problems.  It could be:

1. function

2. language

3. sampling problem

## Sampling Problems

The function takes an input and outputs a bit string.

But associated with every input, $x$, there is some distribution, $D_x$, that I want to sample from.

Instead of outputting a deterministic bit string, the goal is to ouput some __distribution__ parameterized by $x$.

## Relation

Multiple correct answers.

$R$ is a subset.

Example:
Given a number, output _any_ prime factor.

For this problem, there could be multiple correct answers.