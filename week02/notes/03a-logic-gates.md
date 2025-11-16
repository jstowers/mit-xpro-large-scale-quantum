# Logic Gates

Saturday, November 8, 2025

## AND Gate

To compute $A \cdot B$, follow this simple rule:

  - If both inputs are 1, output 1.

  - Otherwise, output 0.

### AND Truth Table

| Input A | Input B | Output ($A \cdot B$) |
| ------- | ------- | ----------------- |
| 0       | 0       | 0                 |
| 0       | 1       | 0                 |
| 1       | 0       | 0                 |
| 1       | 1       | 1                 |

## NOT Gate

The bar over a variable means __logical NOT__.  It inverts the value.

### NOT Truth Table

| $A$  | $\overline{A}$ |
| --   | -------------- |
| 0    | 1 |
| 1    | 0 |

## NAND Gate

A NAND gate (__NOT-AND__) is a fundamental logic gate in digital electronics and computer engineering.

Boolean expression:

  - $\text{A NAND B} = \overline{A \cdot B} = \overline{A} + \overline{B}$

  - Output = NOT(A AND B) 

### NAND Truth Table

| Input A | Input B | Output (A NAND B) |
| ------- | ------- | ----------------- |
| 0       | 0       | 1                 |
| 0       | 1       | 1                 |
| 1       | 0       | 1                 |
| 1       | 1       | 0                 |

NAND is one of the __universal gates__, meaning that any _boolean_ function can be built using only NAND gates.

| Gate     | NAND Implementation |
| -------- | ------------------- |
| NOT A    | A NAND A            |
| A AND B  | (A NAND B) NAND (A NAND B) |
| A OR B   | (A NAND A) NAND (B NAND B) |

### NAND Uses

NAND is the dominant logic gate (~70-90% of logic cells):

• Complementary Metal-Oxide Semiconductor (__CMOS__): the foundation for smartphones, AI accelerators, CPUs, GPUs, and quantum control hardware.

• Fastest and smallest to implement in transistors.

• Its speed is derived from transistor sizing, stacking, and drive strength.

## Universal Gate

A __universal gate__ is a single logic gate (or a small set) that can __implement any Boolean function__:

  1. AND

  2. OR

  3. NOT

  4. NAND

  5. NOR

  6. XOR, etc

and thus any digital circuit, using only that gate.

There are ony __two__ logic gates that are individually universal:

 1. NAND

 2. NOR

## What makes a gate universal?

It can produce:

1. NOT (inversion)

2. AND or OR (conjunction/disjunction)

## What this means?

Any digital circuit, from adders to AI chips, can be built using only NANDs or only NORs.



