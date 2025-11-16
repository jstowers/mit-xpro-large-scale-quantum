# Threshold Theorem

Saturday, November 8, 2025

## Threshold: Classical Computation

We start with a _uniform_ family of circuits of size $N$ error-free gates.

Goal: error-free circuit

Probability of error: $< \epsilon$

Number of gates needed:

  ${O\left(\mathrm{Poly}\left(\log\frac{N}{\epsilon}\right) \cdot N \right)}$

The size of the simulating circuit must grow only logarithmically as 1 over the desired error, $\epsilon$.  It must also grow as the size of the circuit $N$.

1. A gate will fail with probability, $P$, provided that $P < P_{th}$

2. ${P_{th}}$ is independent of $N$ and $\epsilon$

### What does this mean?

${P_{\text{th}}}$ is independent of the size of the circuit, $N$.  This means that the circuit is scalable.

${P_{\text{th}}}$ is independent of $\epsilon$ means that the gate-error threshold required to demonstrate quantum advantage _does not shrink_ as you demand higher accuracy (smaller $\epsilon$) in the output distribution.

## Quantum Advantage

Assume you want to improve accuracy and reduce error by a factor of 10:

$\epsilon \to \epsilon/10$

You would need to lower the errors per gate by 10x.  

It appears that $P_{th}$ would depend on $\epsilon$.

But the quantum advantage proves otherwise.



