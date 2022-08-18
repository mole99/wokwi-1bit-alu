![](../../workflows/wokwi/badge.svg)

# 1bit ALU

This design is based on the 1bit ALU from `Structured Computer Organization: Andrew S. Tanenbaum`.

![1bit ALU](./img/1bit-alu.png)

## Pin list

| Pin | Function |
|---|------|
| 1 | CIN  |
| 2 | INVA |
| 3 | A    |
| 4 | ENA  |
| 5 | B    |
| 6 | ENB  |
| 7 | F0   |
| 8 | F1   |

## Functions

The following functions are supported:

| F1 | F0 | Operation |
|----|----|---------|
| 0  | 0  | A AND B |
| 0  | 1  | NOT B   |
| 1  | 0  | A OR B  |
| 1  | 1  | ADD     |

`ENA` and `ENB` enable/disable the respective input.
`INVA` inverts A before applying the operation.
`CIN` is used as input for the full adder.

## Results

The 7-segment display shows either a "0" or a "1" depending on the output.
If the ADD operation is selected, the dot of the 7-segment display represents the COUT.
