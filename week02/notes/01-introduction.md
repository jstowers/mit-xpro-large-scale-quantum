# Week 2: Building Reliable Classical and Quantum Machines from Unreliable Components

Prof. William Oliver

Saturday, November 8, 2025

## Introduction

Large-scale quantum computers solving larger scale problems will need to run algorithms much longer than the lifetimes of any individual physical qubits.

To do this, we need to implement quantum error correction (QEC).

QEC codes _improve_ quantum system reliability through __qubit redundancy__ and overhead.

If individual qubits are _good enough_, then the overall system performance can be improved by encoding quantum information in _larger numbers_ of such qubits.

By adding more good enough qubits, the _overall_ error rate is decreased.

## Threshold Theorem

How do we determine the __threshold__ for good enough?

How do we design an error-correcting code to handle errors that will certainly occur, but not knowing _when_ or _how many_?

What about errors that occur _during_ the QEC protocol itself?