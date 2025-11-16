# Codes

## What is a Code in Computing?

In information theory and computing, a code is:

  _A systematic way to represent (encode) information using redundancy so that errors can be detected or corrected._

A code is a mapping from __logical__ data to __physical__ data.

### Classical Codes

1. Hamming (7,4) Code

Richard W. Hamming at Bell Labs became frustrated by punch card machines that crashed on single bit errors.

So he invented the first "error-correcting code" as we know it.  His paper "Error Detecting and Error Correcting Codes" was published in 1950.

Hamming introduced several key error correction principles:

  - Parity checks

  - Codewords

  - Minimum distance

  - Syndrome decoding

This code encodes 4 logical bits into 7 physical bits.  It can correct 1 bit flip error.  It add 3 parity bits.

Used in RAM (ECC memory), satellite communications, hard drives.

