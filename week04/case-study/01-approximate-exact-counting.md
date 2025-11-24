# Case Study:  How to Think About Quantum Supremacy

Monday, November 24, 2025

## Lecturer

Prof. Aram Harrow

Associate Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@0673182deb33461a8451348703d31068/block-v1:xPRO+QCRx2+R13+type@vertical+block@524802917efb4888b140251a1c8c9d23)


## Introduction

What complexity classes are harder than NP?

1. Approximate counting

1. Exact counting

## Approximate Counting

Given $\phi$ at the threshold, $T$, determine whether:

  $COUNT(\phi) \geq 2T$ 
  
  or

  $COUNT(\phi) \leq T$

You are promised one of these conditions is true.  You must determine which one it is.

### Example

$T = 1,000$

You either have more than 2,000 solutions or less than 1,000 solutions.

### Example

$T = 2^{99}$

You either have more than $2^{100}$ solutions or less than $2^{99}$ solutions.

## Exact Counting ($PP$)

Given $\phi$ at the threshold, $T$, determine whether:

  $COUNT(\phi) \geq T$
  
  or

  $COUNT(\phi) \leq T-1$

The goal of __exact counting__ is to figure out the solution _exactly_.

NP complete is trying to determine if the number is 0 or positive.

The next one is to approximate it within a factor of two.

The exact counting problem is to figure out if the solutions are above or below a threshold:

_Are there more than 1,000,000,300,042 solutions?  Or are there fewer than that?_

## Goldbach Conjecture

A program takes a _purported proof_ of the Goldbach Conjecture and fits it in a million lines.

_conjecture_ - an educated guess or proposed idea based on intuition or limited evidence.  Often mathematical or speculative in nature.

### Conjecture

The __Goldbach Conjecture__ is one of the oldest _unsolved_ problems in mathematics.  

In 1742, Christian Goldbach asserted his postulate in a letter to Leonhard Euler:

  __every even integer greater than 2 can be expressed as the sum of two prime numbers__.

