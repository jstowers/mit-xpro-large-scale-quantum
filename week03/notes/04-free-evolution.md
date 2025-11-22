# Dynamical Decoupling: Free Evolution

Monday, November 17, 2025

## Lecturer

Prof. William Oliver, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@9affab3cccb347b29b95f4fedafc0737/block-v1:xPRO+QCRx2+R13+type@vertical+block@03c8f0d0b58e4411b09aa2db4eae3a09)

## Pennylane

[Quantum computing with superconducting qubits](https://pennylane.ai/qml/demos/tutorial_sc_qubits) by Alvaro Ballon



## Introduction

When a qubit is placed into a 50/50 superposition, the state is:

  $\frac{\ket{0} + \ket{1}}{\sqrt{2}}$

The current is no longer definitely clockwise or counterclockwise.

Instead the current in the loop __oscillates back and forth__ at the qubit frequency.

The oscillating current is exactly like a tiny _radio wave_.

## $\pi$-pulse

A $\pi$-pulse is a very strong, very short microwave/laser/voltage pulse that rotates the qubit exactly 180° on the Bloch sphere.

It _perfectly flips_ the qubit state:

  $\ket{0} \rightarrow \ket{1}$

  $\ket{1} \rightarrow \ket{0}$




## Ramsey Experiment

A $\pi/2$ pulse along the y-axis of the Bloch sphere brings the qubit Bloch vector down to the equator, pointed along the x-axis.



## Spin Echo Experiment

A $\pi$-pulse is applied during the free evolution period.

The $\pi$-pulse _inverts_ the phase diffusion along the equator:

  - Spins move away from x-axis
  
  - Apply $\pi$-pulse
  
  - Spins move _towards_ x-axis.

For a pulse located precisely in the middle, the Bloch vector refocues and coalesces right when the second $\pi$-pulse occurs.

This takes the Bloch vector down to the south pole and state $\ket{1}$. 

Adding the $\pi$-pulse divides the evolution into half periods of free evolution.

The $\pi$-pulse is an example of dynamically decoupling the qubit from its flux noise environment.


## CPMG Sequence

Carr, Purcell, Meiboom, and Gill (__CPMG__) developed equally-spaced $\pi$-pulses.

As the number of $\pi$-pulses, $n$, is increased, the filter function shifts to higher and higher frequencies.

This _reduces_ the dephasing rate even more.

As dephasing improves, the decoherence time, $T_2$, approaches the ideal value of $2T_1$

## Pulses Sequences and Noise Filters

Pulse sequences in the _time_ domain can be viewed as _noise_ filters in the frequency domain.

- __passband__ - the range of frequencies where the filter lets noise through almost unattenuated.  In this range, the qubit still strongly feels the noise and, therefore, decoheres.

_ __stopband__ - frequencies where the filter is very small.  Noise is cancelled and the qubit is protected.

In spin echo and CPMG, the passband is the set of _high_ frequencies where the sequence failes to protect the qubit.

The stopband region runs from near 0 to 0.8/$\tau$.  This is why CPMG kills low-frequency and 1/f noise well.


