#sequential #circuit #architecture #bistable
## Definition
A D Latch Is a [[Sequential Logic|sequential circuit]] with two inputs. The *data* input, D, controls what the next state should be. The *clock* input, CLK, controls when the state should change. To implement a D Latch, using a SR Latch, we drive the S input with D and the R input with $\bar{D}$ .
## Schematic

![[D Latch schematic.png]]

## Symbol
![[D Latch symbol.png]]
## Truth table

| $CLK$ | $D$ | $\bar{D}$ | $S$ | $R$ | $Q$        | $\bar{Q}$        |
| ----- | --- | --------- | --- | --- | ---------- | ---------------- |
| 0     | $X$ | $\bar{X}$ | 0   | 0   | $Q_{prev}$ | $\bar{Q}_{prev}$ |
| 1     | 0   | 1         | 0   | 1   | 0          | 1                |
| 1     | 1   | 0         | 1   | 0   | 1          | 0                |
D Latchs are important to implement [[D Flip-Flop]]
## Verilog code
```verilog
module dlatch(D,CLK,Q);
	input D,CLK;
	output Q;
	always @ (CLK)
		if(CLK) Q <= D;
```
