# Case Study:  The Surface Code and How It Works

Friday, November 21, 2025

## Lecturer

Austin Fowler

Quantum Hardware Engineer, Google, 2014 - 2025

[LinkedIn]((https://www.linkedin.com/in/austin-fowler-16031071/))

## Goal

Build a reliable quantum computer.

## Need

A way to detect and handle errors.

## Circuit Churn

Generic way to detect errors.

Test the __parity__ of a set of qubits and note when the value of the parity changes.

### Detection Events

A change in value is called a __detection event__.

Detection events indicate the _nearby_ presence of errors.

## Surface Code

The surface code applies the circuit churn principle in two dimensions.

## Why Use a Surface Code?

1. Only __nearest neighbor__ interactions are required.

2. Only __about 6 gates__ are required to generate a bit of information about local errors.

The bits are very likely to be _reliable_.  This means a high error rate of around 1% is tolerable.


## Physical Qubits vs. Logical Qubits

### Physical Qubit

A single, real, noisy qubit made of a specific piece of quantum hardware:

  - superconducting loop

  - trapped ion

  - spin

  - photon

A physical qubit flips or decoheres quickly, typically within 10 to 500 microseconds.  It typically has gate error rates of 0.1 - 1% today.

### Logical Qubit

It is _not_ a single physical qubit.

It is a __large, collective object__ made from _many_ physical qubits.  This could be 100s to tens of thousands.  Together, these qubits behave as _one_ extremely high-quality qubit.

## Surface Code

### Purpose

To make the logical qubit __vastly more reliable__ than _any_ individual physical qubit.

### How it Works

This _active_ error correction happens many times per second:

1. Monitor all physical qubits inside the surface code patch

2. Measure the stabilizer checks (X and Z plaquettes/vertices)

3. Detect where errors have occurred

4. Run a decoder, like MWPM

5. Apply corrective X or Z gates to physical qubits that were _inferred_ to have flipped.

Need sub-10 microsecond latency processing between custom CPUs and FPGAs.

## Qubit Types

### Data Qubits

Sometimes called _bulk_ qubits, these physical qubits carry the actual encoded information of the logical qubit.  They hold the protected quantum state and sit on the lattice sites or edges in the standard checkerboard layout.

### Measure (Ancilla) Qubits

They are only used to read out the stabilizers.  They do not store any logical information.