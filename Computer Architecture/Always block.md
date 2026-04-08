It allows the use of procedural statements like `if-else` and `case` blocks.

```verilog
module latch(input clk,
             input [3:0] d,
             output reg [3:0] q);
always @ (clk, d)
    if(clk) q <= d;
endmodule
```

The sensitivity list (the part after `@`) defines when the block should execute. In the example above, the block runs whenever `clk` or `d` changes.

# Assignments
- **Blocking (=):** Used in combinational blocks. Statements execute sequentially.
- **Non-blocking (<=):** Used in sequential blocks. Statements execute in parallel at the end of the time step.
