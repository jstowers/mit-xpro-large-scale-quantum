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



