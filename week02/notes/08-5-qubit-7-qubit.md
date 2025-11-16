# 5-Qubit and 7-Qubit Codes

Tuesday, November 11, 2025

## 5-Qubit Code

Stabilizers:

  1. XZZXI

  2. IXZZX

  3. XIXZZ

  4. ZXIXZ

Memorize the first pattern (XZZXI) and then cyclically shift them to the _right_ to get the other three.

These stabilizers generate the 5-qubit code.

### Normalizers


Hadamard gates do not commute on the normalizers.


## Hamming Codes

Richard Hamming (1950) used seven bits to encode a four-bit message.  The extra three bits in each codeword served the purpose of _redundancy_, allowing for any _single-bit_ error to be detected and corrected.  

This 7-bit message is called the _logical codeword_.

To correct one error, the code must have a minimum Hamming distance of $d = 3$.

### Code Generation Matrix, $G$

Any four-bit message multipled by $G$ will result in a column vector of length 7.

### Parity-Check Matrix, $H$

The encoded message is transmitted and, potentially, incur errors.

Multiply the seven-bit vector by $H$ to yield a three-bit vector, referred to as the _syndrome vector_.

### Syndrome Vector

This vector can be used to determine which of the seven bits in the logical codeword have been flipped.

If the logical codeword is uncorrupted, the syndrome vector will be a zero vector for _all_ logical codewords.

## 7-Qubit Steane Code

The Steane code is capable of correcting a _single_ arbitrary error.

The subscript, $L$, stands for the logical codeword state.

### Notation

$[[7, 1, 3]]$

where:

  7 = number of _physical_ qubits

  1 = number of encoded _logical_ qubits

  3 = number of qubits containing information on the errors

  [[ ]] = quantum error correction code

## Clifford Gates

Clifford gates are gnerated by $H$, $S$, and $CNOT$.

Any product of 