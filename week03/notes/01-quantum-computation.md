# Quantum Computation vs. Analog Computation

Sunday, November 16, 2025

## Lecturer

Aram Harrow

Associate Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@8f2935d37d0c4e8e93ad94e8b15d30ae/block-v1:xPRO+QCRx2+R13+type@vertical+block@e747b2141ae848a6a8c092cb0dcc8195)

## Discussion

### Digital Computers

In a _digital_ computer, the voltage level represents the two binary logic states (bits) in a digital circuit:

  - __0 V__ represents __logic 0__ (low, false, or off)

  - __5 V__ represents __logic 1__ (high, true, or on)

The circuit voltage is either 0 V or 5 V.  Everything else is illegal.  If a digital computer sees 4.9 V, it knows to bump the voltage up to 5 V.

Historically, 5 V was used based on the Texas Instruments Transistor-Transitor Logic (__TTL__) 7400 chip (integrated circuit) introduced in the 1960s.  Modern systems use lower voltages (3.3 V, 1.8 V, 1.2 V, etc) for power efficiency, but the same two-state principle applies.

### Analog Computers

In an _analog_ computer, if 3.7 is a legal voltage and 3.70001 is a legal voltage, there's nothing the computer can do if there's a little drift in the voltage.  

  - Was this supposed to happen?  Or was this something that should be corrected?

Fundamentally, analog computing is _not_ error correctable!

### Quantum Computers

#### Argument

Some theorists believed that quantum computers suffered the same limitation as analog computers.  Namely that amplitudes cannot be error corrected.

Consider a unitary quantum error: 

  $e^{i \theta Z}$

where:

  - Pauli matrices: $X = \sigma_x, Y = \sigma_y, Z = \sigma_z$

  - $\theta$ = error magnitude

  - $i$ = rotation

#### Question

If $\theta$ is very small and continuously varies, I cannot distinguish all those different errors.  So how can I correct them?

This question prompted Peter Shor and others to develop error-correcting codes.

#### Solution

Today, we know that a quantum error is a linear combination of $I$ and $Z$:

 $e^{i \theta Z} = \cos{\theta}I + i\sin{\theta}Z$ 

If a code can correct $i$ and $Z$, it can also correct, for all values of $Z$, all linear combinations of $i$ and $Z$.

#### Key Point

It is a remarkable and crucial feature of _quantum_ error correction that the space of errors they correct is a __linear subspace__.

## Active Error Correction

QEC protocols typcially use __syndrome measurements__ to detect _if_ and _where_ an error occurred.

Detected errors are corrected using a __feed-forward__ approach: pulses are applied to errant qubits to correct the error.

