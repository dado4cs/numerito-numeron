#circuit #sequential #architecture #bistable
## Definition
A D flip-flop is a sequential circuit element that samples its input `D` at the edge of a clock (usually the rising edge) and updates its output `Q`. It stores one bit of information.

Unlike a latch, which is level-sensitive, a flip-flop is edge-sensitive.
## Schematic
![[D FlipFlop Schematic.png]]
## Symbol
![[D FlipFlop symbol.png]]
## Difference from Latch
A **latch** updates its output whenever the clock is high (level-sensitive).
A **flip-flop** updates its output only when the clock transitions (negedge or posedge, edge-sensitive).
## Verilog implementation
```verilog
module d_flip_flop(input clk,
                   input [3:0] d,
                   output reg [3:0] q);
always @ (posedge clk)
    q <= d;
endmodule
```