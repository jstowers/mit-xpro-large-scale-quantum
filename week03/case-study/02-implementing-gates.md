# Implementing Gates on the Surface Code

Sunday, November 22, 2025

## Review

White squares and semicircles - bit flip errors

Blue squares and semicircles - phase flip errors

![surface-code-diagram](../images/surface-code-diagram.png)

## Agenda

1. Logical initialization

2. Logical measurement

## Logical Initialization

### Logical Zero State

If all _data_ qubits start at zero and then errors are detected, then create and protect a logical _zero_ state.

### Logical One State

If all data qubits start at zero and bit-flip white qubits along a vertical line, then create and protect a logical _one_ state.

## Logical Measurement


## Logical T Gates

A __T gate__ is a small, precise rotation of a qubit by exactly 45° around the Z-axis of the Bloch sphere.

Its official name is a "$\pi/8$" gate.

With Clifford gates (Hadamard, S/Phase, CNOT, X, Y, Z), T gates make quantum computation _universal_.  This means that you can build any possible quantum algorithm with enough T gates.

### Magic State

A __T state__ is a special _ancillary qubit_ prepared in the following state:

$|T⟩ = \frac{|0⟩ + e^{\frac{iπ}{4}}|1⟩}{\sqrt{2}}$

T gates consume T states, usually through a few Clifford gates and one measurement.

Once you measure and destroy one $\ket{T}$ state, you get one __T gate__ on the qubit you care about.

### Repairing T States

1. Injection - Ying Li

2. Distillation

    - may need to pipe output of 1 distillation to another distillation

