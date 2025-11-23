# Models of Computing: Circuits

Saturday, November 22, 2025

## Lecturer

Prof. Aram Harrow

Associate Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@d74eb092f4c942e0a78f9e2db830f52c/block-v1:xPRO+QCRx2+R13+type@vertical+block@187cf9fc507e4990a56ecc83eb0823ce)

## Circuit Model

### Classical Circuits

You have bits, $x_1$ to $x_n$.

You combine bits via gates like AND, NOT, and OR.

Classical circuits can have _unbounded_ fan-in AND/OR fan-out.

  - You can take the `AND` of many different bits.

  - You can take the output of an `AND` gate and feed it to many, many other gates.

### Quantum Circuits

#### Unitary

Quantum circuits are _unitary_ because:

1. quantum gates are perfectly reversible, and 

1. no information is lost

In math, a matrix, $U$, is unitary if:

  $U \dagger U = I$

Its adjoint times itself is the identity.

#### Adjoint

The adjoint of a matrix can be determined by:

1. Taking the _complex conjugate_ of every entry (replace $i$ with $-i$)

1. Transposing the matrix (swap rows and columns)

The identity matrix has 1s on the diagonal and 0s everywhere else.

#### Translation

If you take the quantum gate, reverse it (dagger $\dagger$), and then apply the original gate again, you get exactly the "do nothing" operation.

Quantum gates do not create any extra data:

  - if two qubits go into a NOT gate, two qubits come out.

  - if three qubits go into a Toffoli gate, three qubits go out.

Any extra data must be created in ancilla bits and initialized to state $\ket{0}$ at the start.

## Circuit Complexity

How hard is it to compute the circuit?

How much time does it take?

How much effort is required?

## How do you measure circuit complexity?

#### 1. Circuit Width

The __number of bits__ in the circuit.  It represents the memory required to run the circuit.

#### 2. Circuit Depth

The __amount of time__ it takes to run a circuit.

Imagine the gates are in layers.  If two gates happen on disjoint pairs of qubits, I can run them in parallel.

The depth measures the number of layers in this kind of decomposition.

#### 3. Circuit Size

The __number of gates__.

## Pros and Cons of Circuit Model

### Pros

1. Concrete model of computation

### Cons

1. Dependence on the input size, $n$

  - Every quantum circuit has a _definite_ number of inputs and a _definite_ sequence of operations.

  - n = |x| where x is the input string

  - n = number of bits of input

  - For every value of $n$, I have to specify a circuit.

  - Example:  Does the nth Turing machine halt?

    - There is no algorithm that will compute this for all inputs.

2. No loops

  - No infinite loops, but you give up some powerful features of programming.
