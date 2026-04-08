```verilog
module flop(input clk,
			input [3:0] d,
			output reg [3:0] q);
always @ (posedge clk)
	q <= d;
endmodule
```

```verilog
module flop(input clk,
			input [3:0] d,
			output reg [3:0] q);
always @ (clk)
	if(clk=1) q <= d;
endmodule
```
