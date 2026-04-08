# SR Latch
The Set-Reset (SR) latch is one of the simplest sequential logic circuits. It has two inputs, Set ($S$) and Reset ($R$), and two complementary outputs, $Q$ and $\bar{Q}$.

## Truth Table
| $S$ | $R$ | $Q_{next}$ | Description |
|---|---|---|---|
| 0 | 0 | $Q$ | Hold (no change) |
| 0 | 1 | 0 | Reset |
| 1 | 0 | 1 | Set |
| 1 | 1 | Undefined | Forbidden State |

## Forbidden State
The state $S=1, R=1$ is generally forbidden because it leads to an unpredictable outcome ($Q$ and $\bar{Q}$ both become 0, which violates the complementary property).

## Implementation
An SR latch can be implemented using two cross-coupled NOR gates or two cross-coupled NAND gates.
