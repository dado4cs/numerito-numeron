## Definition
Multiplexers are a [[Combinational Logic|combinational circuits]], that choose an input from among several possible inputs based on the value of a *select* signal. A multiplexer is called a *mux*.
## 2:1 Multiplexer
Have two data inputs: $D_0$ and $D_1$, a select input, $S$, and the output $Y$. The multiplexer chooses betwen the two data inputs based on the select: if $S=0, Y=D_0$ , and if $S=1,Y=D_1$. S is also called a *control signal* because it controls what the multiplexer does.
### Symbol
![[21mux.png]]
### Truth table
![[21muxtruthtable.png]]
## Schematic
With the truth table, we can build the circuit using [[Karnaugh Map|K-Maps]].
![[21mux_kmaps.png]]
The multiplexer implementation uses a [[Multilevel Combinational Logic|two-level design]]:
![[21muxschematic.png]]