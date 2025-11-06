# Detecting Single Errors

Sunday, November 2, 2025

## Encoding a Single Qubit State

The logical qubit state, $\ket{\psi_L}$, is realized by implementing two CNOT gates.

How can we detect if a _bit flip_ occurred on one of the three qubits?

-  Use a majority voting scheme

-  A set of measurments called __parity checks__ between neighboring qubits

    - Qubits in the same state have the same parity.

    - Qubits in different states have different parities.

The _outputs_ of parity measurements are called a __syndrome__.

- The syndrome tells us _if_ and _where_ a single error occurred.

## Parity Checks

1. To check the parity of $q_1$ and $q_2$, apply an XOR gate between them.  Store the answer on ancilla qubit, $S_A$.

    $\ket{S_A} = \ket{q_1 \oplus q_2}$

1. To check the parity of $q_2$ and $q_3$, apply an XOR gate between them.  Store the answer on ancilla qubit, $S_B$.

    $\ket{S_B} = \ket{q_2 \oplus q_3}$

1. Measure the ancilla qubits to get the values of $S_A$ and $S_B$.

    ${S_A = q_1 \oplus q_2}$

    ${S_B = q_2 \oplus q_3}$

1. Check the parities 

    | ${q_i}$ | ${q_j}$ | ${S_m}$ | Parity     | Error  |
    | ------- | ------- | ------- | ---------- | ------ |
    | 0       | 0       | 0       | same       | No     |
    | 0       | 1       | 1       | different  | Yes    |
    | 1       | 0       | 1       | different  | Yes    |
    | 1       | 1       | 0       | same       | No     |

    If the parities are the same, there is _no_ error.

    If the parities are different, there is an error.

## Bit-Flip Code

Use _redundancy_ to encode information.

Instead of encoding information in a single _physical_ qubit, we encode this information in a single _logical_ qubit comprising several physical qubits.

### Physical Qubits

Fragile, error-prone, individual hardware-level qubits.  Either trapped ion or superconducting loop.

### Logical Qubits

Robust, error-corrected, abstract units made from _many_ physical qubits.

In the 3-qubit repetition code, 3 physical cubits are used to encode 1 logical qubit and correct 1 bit-flip error.

### Three-Qubit Repetition Code

1. These two states are called _codewords_, and they are both chosen to have parity 0:

    $\ket{0} \rightarrow \ket{0}_{q_1}\ket{0}_{q_2}\ket{0}_{q_3} \rightarrow \ket{000}$

    $\ket{1} \rightarrow \ket{1}_{q_1}\ket{1}_{q_2}\ket{1}_{q_3} \rightarrow \ket{111}$

2. Consider a single-qubit superposition state mapped onto the codewords:

    $\alpha\ket{0} + \beta\ket{1} \rightarrow \alpha\ket{000} + \beta\ket{111}$

3. If a single bit-flip error occurs, the quantum state will change causing a change in parity.

4. The two parity checks, one between ${q_1}$ and ${q_2}$, and the other between ${q_2}$ and ${q_3}$, will be stored on the ancillary qubits, ${S_A}$ and ${S_B}$, respectively.

5. The measured values, ${S_A}$ and ${S_B}$, form a __syndrome__, and can uniquely identify on what qubit the error occurred.

6. The syndrome measurements project the logical states onto the codeword states while preserving the quantum information on the data qubits.
