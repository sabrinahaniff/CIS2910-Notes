## Definition 1: Graph

A **graph** $G = (V, E)$ consists of:
- $V$ = a nonempty set of **vertices** (or nodes)
- $E$ = a set of **edges**

Each edge has either one or two vertices associated with it, called its **endpoints**. An edge is said to **connect** its endpoints.

> **Note:** Vertices are the "dots" — they cannot be replaced with labels.

---

## Types of Graphs

### Simple Graph
- No multiple edges
- No loops

### Multigraph
- Multiple edges allowed
- No loops
- You don't have to connect each vertex
- **Multiplicity:** the number of edges between two vertices

### Pseudograph
- Multiple edges AND loops allowed

---

## Directed Graphs

Each edge in a **directed graph** is associated with an **ordered pair**. The directed edge associated with the ordered pair $(a, b)$ starts at $a$ and ends at $b$.

### Simple Directed Graph
- No multiple edges

### Directed Multigraph
- Multiple directed edges and loops allowed

---

## Mixed Graph

Contains both **directed** and **undirected** edges.

---

## Graph Terminology

### Undirected Graphs

**Adjacent vertices (or neighbors):** Two vertices connected by an edge

**Incident edges:** Edges that connect to a vertex

**Neighborhood of a vertex:** $N(v)$ = listing of all vertices that vertex $v$ is adjacent to

**Degree of a vertex:** $\deg(v)$ = how many edges are connected to that vertex

**Isolated vertex:** A vertex not connected to anything ($\deg(v) = 0$)

**Pendant vertex:** Degree of the vertex is 1 (connected to only 1 other vertex)

---

### Example

a       b
 \      /  \
  \    /     \
   c  ---  d

- $N(b) = \{c, d\}$
- $\deg(b) = 2$
- $N(a) = \emptyset$
- $\deg(a) = 0$ (isolated)

---

## Handshake Lemma

Let $G = (V, E)$ be an undirected graph with $m$ edges. Then:

$$2m = \sum_{v \in V} \deg(v)$$

> Each edge connects **two vertices**, so each edge contributes 2 to the total degree sum.

If $G = (V, E)$ is a graph with $n$ vertices, then:

$$\sum_{i=1}^{n} \deg(v_i) = 2|E|$$

---

### Example: Handshakes

Suppose there are 6 people in a room, and each must shake hands with every other person. How many handshakes occurred?


Each person shakes 5 hands: $6 \times 5 = 30$

By handshake lemma: $2m = 30 \implies m = 15$ handshakes

---

### Example: Degree 6

How many edges are there if you have 10 vertices, each of degree 6?

$$2m = 10 \times 6 = 60$$

$$m = 30 \text{ edges}$$

---

## Directed Graphs Terminology

Let $G = (V, E)$ be a directed graph. Then:

$$\sum_{v \in V} \deg^-(v) = \sum_{v \in V} \deg^+(v) = |E|$$

**Initial vertex:** Where an edge starts

**Terminal vertex (or end vertex):** Where an edge ends

**In-degree:** $\deg^-(a)$ = how many directed edges come **into** $a$

**Out-degree:** $\deg^+(a)$ = how many directed edges leave $a$

---

### Example

- $b$ adjacent to: $a$ (edge $(b, a)$)
- $a$ adjacent from: $b$ (starts at $b$ and ends at $a$)

---

## Special Graphs

### Complete Graphs: $K_n$

A complete graph on $n$ vertices has every vertex connected to every other vertex.

- $K_n$ has $n$ vertices
- Every vertex has degree $n - 1$
- Total edges: $\binom{n}{2} = \frac{n(n-1)}{2}$

---

### Cycles: $C_n$

A cycle graph on $n$ vertices forms a closed loop.

- $C_n$ has $n$ vertices
- Every vertex has degree 2

---

### Wheels: $W_n$

A wheel graph is related to the cycle graph with a central point.

- $W_n$ has $n + 1$ vertices
- Central vertex has degree $n$
- Outer vertices have degree 3

---

### Hypercube (or $n$-Cube): $Q_n$

Vertices are $n$-bit strings: $0 \to 1 \to \cdots \to n$

Two vertices are connected **if and only if** they differ in exactly one bit position.

**Order matters:** Vertices can only be connected when they share the same bit value in the same bit position.

#### Example: $Q_2$

Vertices: 00, 01, 10, 11


---

## Bipartite Graphs

A graph is **bipartite** if its vertex set can be partitioned into two disjoint sets $V_1$ and $V_2$ such that every edge connects a vertex in $V_1$ to a vertex in $V_2$.

> **Visual:** Two groups of vertices, edges only go between groups, never within a group.

---

## Isomorphism

Graphs are **isomorphic** if they have the same number of edges, vertices, degree sequence, and structure, but look different visually.

Let $G_1 = (V_1, E_1)$ and $G_2 = (V_2, E_2)$. $G_1$ is isomorphic to $G_2$ ($G_1 \cong G_2$) if and only if:

$$\exists f: V_1 \to V_2 \text{ where:}$$

1. $f$ is **bijective** (one-to-one and onto)
2. $\forall a, b \in V_1$: $\{a, b\} \in E_1 \iff \{f(a), f(b)\} \in E_2$

---

[[README|← Back to Main Index]]