# Challenges with Large-Scale Systems

Saturday, November 22, 2025

## Challenge

In 2018, you could not execute _physical_ gates with sufficiently low error to successfully implement the surface code.

## Current State of Art

As of early 2025, Google Quantum AI showed that physical gate fidelities operate below the surface code's error threshold.

This breakthrough enables __exponential suppression__ of logical errors as code distance increases.

The surface code's theoretical error threshold is around __1% per gate (or cycle)__.  Google's Willow processor achieved two-qubit gate fidelities exceeding 99.9%.  This represents an error rate of around __0.1% or better__.

See ["Quantum error correction below the surface code threshold"](https://www.nature.com/articles/s41586-024-08449-y), Nature, December 9, 2024.

## Minimum Weight Perfect Matching (MWPM) Algorithm

The MWPM algorithm is the most widely-used _classical_ decoding method for the surface code.

Given a lattice with detection events, you can:

1. Choose paths connecting detection event pairs, or

2. Connect detection event pairs to the nearest boundary such that the total path length is minimal

## How it works

The decoder builds a complete graph where every __defect__ is a vertex, and the weight of each edge is the estimated __probability__ that an error chain actually occurred between those two defects.

The pairing tells us which chain or errors most likely happened.  From there, we apply the corresponding correction operators to the _data_ qubits, thereby removing the inferred errors and protecting the logical qubit.
