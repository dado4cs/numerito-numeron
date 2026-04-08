#architecture #circuit #sequential
## Definition
A N-bit register is a structure that stores n bits of data and can be read from or written simultaneously.

## Implementation
It is created using multiple [[D Latch|D Latchess]] or [[D Flip-Flop|D Flip-Flops]] in parallel.
### Control
A single **Write Enable (WE) or CLK** signal is shared across all storage elements to allow simultaneously writes.
## Example
4-bit register stores data referenced as $Q[3:0]$.
- Schematic
![[4-bit-register.png]]
- Symbol
![[4-bit-register-symbol.png]]

