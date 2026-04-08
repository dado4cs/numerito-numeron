# Definition
## First definition
A boolean algebra is a bounded, complemented and distributive [[Lattice|lattice]].

**Theorem:** If $(A,R_1)$ and $(B,R_2)$ are isomorphic lattices and $(A,R_1)$ is a boolean algebra, then $(B,R_2)$ is a boolean algebra too.

## Second definition
A boolean algebra is a set B equipped with two binary operations:
$$
\begin{align}
B \times B &\rightarrow B \\
	(a,b)&\rightarrow a+b
\end{align} 
$$
$$
\begin{align}
B \times B &\rightarrow B \\
	(a,b)&\rightarrow a \cdot b
\end{align} 
$$
such that the following [[Axiom|axioms]] are satisfied:
- **Commutativity:** 
$$
\begin{align}
\forall a,b \in B: \\
a + b &= b + a \\
a \cdot b &= b \cdot a 
\end{align}
$$
- **Associativity:**
$$
\begin{align}
\forall a,b,c \in B: \\
a + (b + c) &= (a+b)+c \\
a \cdot (b \cdot c) &= (a \cdot b) \cdot c
\end{align}
$$
- **Distributivity:**
$$
\begin{align}
\forall a,b,c \in B: \\
a + b\cdot c &= (a+b) \cdot (a+c)\\
a \cdot (b+ c) &= a \cdot b + a \cdot c\\
\end{align}
$$
- **Identity elements:**
There exist distinct elements $0, 1 \in B$ such that for all $a \in b$:
$$
\begin{align}
a + 0 = a \\
a \cdot 1 = a
\end{align}
$$
- **Complemententation:**
For every $a \in B$ exists an element $\bar{a} \in B$ such that:
$$
\begin{align}
a + \bar{a} &= 1 \\
a \cdot \bar{a} &= b \cdot a 
\end{align}
$$
# Theroems
Let $B$ be a boolean algebra. Then, the following holds:
- An element's complement is unique.
- The elements 0 and 1 are unique.
- $\overline{(\bar{a})}=a, \forall a \in B$ 
- $\forall a \in B : a+a = a \wedge a \cdot a = a$ 
- $\forall a \in B : a+1 = 1 \wedge a \cdot 0 = 0$ 
- De Morgan's laws: $$ \begin{align} \forall a,b \in B : \\ \overline{(a+b)} = \bar{a} \cdot \bar{b} \\ \overline{a \cdot b} = \bar{a} + \bar{b} \end{align}$$  