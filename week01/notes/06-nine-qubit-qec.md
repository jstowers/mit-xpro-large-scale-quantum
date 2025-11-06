# Nine-Qubit Quantum Error Correction Code

Wednesday, November 5, 2025

## Lecturer

Prof. Peter Shor, MIT

## Shor Code

Peter Shor introduced the first error-correcting code in 1995.  

The __Shor code__ encodes __1 logical qubit__ into __9 physical qubits__.

It can correct any single-qubit error:

| Error | Name | Flips Bit? | Flips Phase | Corrected by 3-qubit code |

- $\sigma_x$

- $\sigma_z$ -> 

- $\sigma_y$ -> bit + phase flip



## Concatenation

When you apply a $\sigma_x$ error on a logical qubit, the phase errors blow up.

When you apply a code that corrects $\sigma_z$ errors, it causes the $\sigma_x$ bit errors to increase 3x.

How do you fix this?


Shor code applies a phase-flip code (outer) of the bit-flip code (inner)

## Toffolli Gate

The __Toffoli Gate__ is a conditional gate that applies a $\sigma_X$ bit-flip on the target qubit when both control qubits are in the $\ket{1}$ state.  Otherwise, it leaves the state the same.