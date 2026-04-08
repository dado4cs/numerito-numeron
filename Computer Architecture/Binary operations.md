## Binary Addition
Binary addition follows the same rules as decimal addition, but with only two digits: 0 and 1.

The basic rules:
- $0 + 0 = 0$
- $0 + 1 = 1$
- $1 + 0 = 1$
- $1 + 1 = 10_2$ (0 with a carry of 1)
- $1 + 1 + 1 = 11_2$ (1 with a carry of 1)

### Example
$$
\begin{array}{r@{\quad}l}
  111 & \text{(Carry)} \\
  0110 & (6_{10}) \\
+ 0111 & (7_{10}) \\
\hline
  1101 & (13_{10})
\end{array}
$$

## Binary Subtraction
Subtraction can be performed directly or by using [[Integer representation#Two's complement|Two's complement]].
To subtract $A - B$, you can calculate $A + (-B)$.
To find $-B$, invert the bits of $B$ and add 1.
