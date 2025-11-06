# Three-Qubit Phase-Flip Error Correction Code

Monday, November 3, 2025

## Lecturer

Peter Shor, MIT

## Introduction

Assume we have a dephasing channel:

| Probability | Apply |
| ----------- | ----- |
| 1 - $q$     | nothing (${I}$) |
| $q$         | ${\sigma_z}$ |   


A phase-flip ($\sigma_z$) in the computational basis becomes a bit-flip ($\sigma_x$) in the Hadamard ($X$) basis.

## Hadamard Gate

A Hadamard gate is a __single-qubit__ gate and cannot entangle two qubits.

It also can't encode a single-qubit state into a three-qubit entangled state.


## Process

1. Start with initial quantum state:

    $\alpha\ket{0} + \beta\ket{1}$


2. Apply $H$ to data qubit:

    $\alpha\ket{+} + \beta\ket{-}$

3. Encode using __bit-flip code in X-basis__:








Hadamard cubed puts a `-1` in front of any state with an odd number of ones.


## Code Conjugation

By applying Hadamard gates _before_ and _after_, you transform $\sigma_z$ errors into $\sigma_x$ errors.

The bit-flip code transforms into the phase-flip code.

This is called __code conjugation__ or __basis change__, and it is a core technique in quantum computing.



## Pauli Operators

The Pauli operators, $\sigma_x$ and $\sigma_z$, are the basic building blocks of quantum errors:

| Operator| Matrix     | Name       | Action on $\ket{0}$, $\ket{1}$ |
| ------- | ---------- | ---------- | -------------------------------------- |
| $\sigma_x = X$ | $\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$ | X (bit-flip) |"X∣0⟩=∣1⟩X\ket{0} = \ket{1}X∣0⟩=∣1⟩, X∣1⟩=∣0⟩X\ket{1} = \ket{0}X∣1⟩=∣0⟩" |
| $\sigma_x = Z$ | $\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$ | Z (phase-flip) | |



σz=Z\sigma_z = Zσz​=Z,(100−1)\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}(10​0−1​),Z (phase-flip),"Z∣0⟩=∣0⟩Z\ket{0} = \ket{0}Z∣0⟩=∣0⟩, Z∣1⟩=−∣1⟩Z\ket{1} = -\ket{1}Z∣1⟩=−∣1⟩"