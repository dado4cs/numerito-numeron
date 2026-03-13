#discrete #graph
# Definition
A graph $G$ is a pair $(V,E)$, where $V$ is a [[Set|set]] whose elements are called vertices and $E$ is a set of pairs $\{v_1,v_2\}$ of vertices, whose elements are called *edges*.

# Type of graphs
## [[Directed Graph]] (Digraph)
A directed graph (also called digraph), is a graph in which edges have direction. In digraphs, a edge is an ordered pair $(u,v)$, that represents a connection from $u$ to $v$.
## [[Simple Graph]]
A graph that doesn't have loops (edges that connect the same vertex) and doesn't have multiple edges.
## [[Multigraph]]
A graph that can have multiple edges (called also parallel edges) between the same pair of vertices.

# Terminology
Let $G$ be a simple undirected graph.
- $V(G)$ denotes the set of vertices of G
- $E(G)$ denotes the set of edges of G
- $V \choose 2$ : Set of all subsets of two vertices from V. $E \subseteq {V \choose 2}$.
- Let $e = \{u,v\} \in E$ . We say that $u$ and $v$ are **adjacent**, and the edge $e$  is said to be **incident on** both $u$ and $v$.
## Degree of a vertex
Let $G = (V,E)$ be an undirected graph. We say that the **degree** of a vertex $v \in V$ (denotated with $d(v)$) is the number of vertices adjacent to v. 
In general, for any type of graph, the dregree of a vertex is the number of edges incident to it.

# The Handshake Theorem
In any finite undirected graph $G$, the sum of the degrees of all vertices is exactly twice the number of edges.
$$
\sum_{v \in V(G)}{d(v)} = 2 \times |E(G)|
$$
## Intuition
Por cada arista que vamos contando, esta arista aumenta en 1 por cada vértice, y como toda arista une dos vértices, entonces en total por cada arista se aumenta en 2 la sumatoria total de grados.
