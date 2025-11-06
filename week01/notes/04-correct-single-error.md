# Correcting Single Errors

Monday, November 3, 2025

## Example

The syndrome measurement can be used to correct a single qubit by performing an __X gate__ on the errant qubit and flipping it back to the correct state.

We don't know if the errant qubit, ${q_1}$, is in state 0 or state 1.  We just know that it was in the wrong state and needed to be flipped back to the correct state.



The CNOT gate acts on the two-qubit subspace spanned by qubits 0 and 1, leaving qubit 2 unchanged. Its matrix in the basis $\{\ket{00}, \ket{01}, \ket{10}, \ket{11}\}$ (for control-target) is:
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0
\end{pmatrix} $$
For the full three-qubit system, the gate is tensored with the identity on qubit 2:
$$ \text{CNOT}_{0 \to 1} = \text{CNOT} \otimes I = 
\begin{pmatrix}
1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 1 & 0 & 0
\end{pmatrix} $$
(in the ordered basis $$ \ket{000}, \ket{001}, \ket{010}, \ket{011}, \ket{100}, \ket{101}, \ket{110}, \ket{111} $$).

The initial state vector is:
$$ \ket{\psi_0} = 
\begin{pmatrix}
a \\ 0 \\ 0 \\ 0 \\ b \\ 0 \\ 0 \\ 0
\end{pmatrix} $$

### Matrix Multiplication
Apply the gate:
$$ \ket{\psi_1} = (\text{CNOT} \otimes I) \ket{\psi_0} = 
\begin{pmatrix}
1 & 0 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 1 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 & 0 & 1 & 0 & 0
\end{pmatrix}
\begin{pmatrix}
a \\ 0 \\ 0 \\ 0 \\ b \\ 0 \\ 0 \\ 0
\end{pmatrix}
=
\begin{pmatrix}
a \\ 0 \\ 0 \\ 0 \\ 0 \\ 0 \\ b \\ 0
\end{pmatrix} $$

### Final State After First CNOT
This corresponds to:
$$ \ket{\psi_1} = a \ket{000} + b \ket{111} $$

### Basis-State Derivation (Without Full Matrix)
Alternatively, expand explicitly by applying CNOT to each term:

1. For the $$ a \ket{100} $$ term (qubits 0=1, 1=0, 2=0):  
   Control (qubit 0) is $$ \ket{1} $$, so flip target (qubit 1): $$ \ket{0} \to \ket{1} $$.  
   Qubit 2 unchanged: $$ \ket{0} $$.  
   Result: $$ a \ket{111} $$.

2. For the $$ b \ket{000} $$ term (qubits 0=0, 1=0, 2=0):  
   Control (qubit 0) is $$ \ket{0} $$, so target unchanged: $$ \ket{0} $$.  
   Qubit 2 unchanged: $$ \ket{0} $$.  
   Result: $$ b \ket{000} $$.

Superposition:  
$$ \ket{\psi_1} = a \ket{000} + b \ket{111} $$