qIt allow the use of `if-else` blocks
```verilog
module latch(input clk,
			 input [3:0] d,
			 output reg [3:0] q);
always @ (clock, d)
	if(clk) q <= d;
endmodule
```

