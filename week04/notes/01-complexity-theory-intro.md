# Introduction to Complexity Theory

Saturday, November 22, 2025

## Lecturer

Prof. Aram Harrow

Associate Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@d74eb092f4c942e0a78f9e2db830f52c/block-v1:xPRO+QCRx2+R13+type@vertical+block@b95c2d3417d2428580e611a97dfce771)

## What does it mean to compute something?

### Functions

Usually, we are computing a function, $f$, that has some input and some output.

The  input is a binary string of some length and the output is a binary string of some length.

We can encode anything into bits.

This includes problems like:

- matrix multiplication

- shortest path in a graph

- integer factorization

- halting problem

Even though the inputs to these problems don't look like bits, they can all be encoded to bits in some way.

## Complexity Theory

Some problems are harder than others.

### Languages (L)

A special case of functions that outputs one bit: 

$ f:\{0,1\}^* \rightarrow \{0,1\}$

You can describe the whole function by specifying the set that gets mapped to 0, and a set that gets mapped to 1.

The function is just determining membership in a set.

- If you are in the set $L$, you accept the input.

- If you are _not_ in the set $L$, you reject the input.

Essentialy, you can phrase any general problem as a __yes/no__ problem.

