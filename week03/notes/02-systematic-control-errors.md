# Correcting Systematic Control Errors

Sunday, November 16, 2025

## Lecturer

Isaac Chuang

Professor of Electrical Engineering and Computer Science

Professor of Physics, MIT

[Video lecture](https://courses.xpro.mit.edu/learn/course/course-v1:xPRO+QCRx2+R13/block-v1:xPRO+QCRx2+R13+type@sequential+block@9affab3cccb347b29b95f4fedafc0737/block-v1:xPRO+QCRx2+R13+type@vertical+block@c11fa2c117b742308dff7e9ed5f20656)

## Correcting Quantum Errors

Quantum errors can be corrected simply by __changing the control sequence__, as long as the errors are systematic and not random.

  - __systematic__ - predictable mistakes that happen the same way every time

  - __random__ - different error each time; can't predict

### Example

A quantum gate is supposed to rotate a qubit by 90°.  

Due to a calibration flaw, the qubit rotates 95° (systematic over-rotation).

  - Bad fix: add complicated error-correction circuits requiring extra qubits and measurements

  - Good fix: tell cubit to rotate by 85°.  85° + 5° (systematic error) = 90° (perfect rotation)

Gate as implemented: $M_x$

Ideal rotation: $R_x(\theta)$

Error caused by over-rotation: $\epsilon$

$M_x(\theta) = R_x(\theta(1 + \epsilon))$

## Quantum Response

The error is unknown but fixed.  

The __quantum response function__ quantifies the effect of this error as the transition probability between 0 and 1 for the implemented $\pi$ pulse:

Quantum response = $|\bra{1}|M_x(\pi)\ket{0}|^{2}$

The error can be removed by __composite pulse sequences__, or composite quantum gates.

  - replaces a single pulse with multiple rotation pulses aobut different axes of rotation

Examples: 

  - Levitt 90° - 180° - 90°

  - 90° - 360° - 90°

  - BB1

## Review Question

Which pulse sequence implements a $\pi$-pulse about the $\x$-axis with the _smallest_ net error in the system response?


