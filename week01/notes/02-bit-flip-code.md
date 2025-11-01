# Introduction to the Bit-Flip Code

Saturday, November 1, 2025

## Failure Rate Comparison

**Classical transistor**

  $1 \times 10^{20}$

**Current qubits** 

  $1 \times 10^{3}$ ~ $1 \times 10^{4}$

## Large-Scale, Fault-Tolerant Quantum Systems

- systems are built from devices and devices can be faulty.

- whether classical or quantum, you can improve _system reliability_ by implementing error correction protocols.

## Redundancy

- assume an imperfect device that is insensitive to small input errors, but becomes less resilient with larger errors.

- if the individual devices are good enough, then adding another device can improve system reliablity.

- device redundancy can improve system reliablity, but at the expense of additional overhead.

## Bit-Flip Code

Can be implemented on classical and quantum bits.

Add redundancy by _encoding_ the physical qubit state onto 3 logical qubits.

- This encoding protects against a single bit-flip error on one of the qubits.

- The error code will fail if there 2 or more errors on the encoded qubits.

Net win if:

  $cp^{2} < p$

where:

- $c$ is a constant that conceptually incorporates the number of ways an encoding error can occur

- $p$ is the single qubit error probability.

### Threshold Condition

  $ p_{th} = p < \frac{1}{c}$

Takeaway:

- If the single qubit error rate is low enough, then introducing redundancy by adding more such qubits will reduce the overall error rate.

- The cost is the overhead, $c$, in implementing the QEC.

- The turning-point probability, $p_{th}$, is called the _threshold probability_ or _threshold_.

## Parity Checks

### Exclusive-OR (XOR) Gate

In classical computing, the _exclusive-OR gate_ (XOR) outputs 1 only if bit _a_ and bit _b_ are different:

|   a   | b     | $a \oplus b$ |
| ----- | ----- | ------------ |
| 0 | 0 | 0 |
| 1 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 1 | 0 |

### Controlled-NOT (CNOT) Gate
In quantum computing, the XOR operation is implemented using the _controlled-NOT_ (CNOT) gate:

  CNOT

Parity-check operations can detect errors without projecting and destroying the quantum information.

The parity bit, ${b_p}$, is the _exclusive-OR (XOR)_ of two data bits:

  $ b_p = b_1 \oplus b_2 $