# Unit 4: Elementary Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 4 (Graph Theory Foundations, Handshaking Lemma, Paths, and Pseudocode). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Graph Theory Foundations

### Section A: Concept Checks
1. What is a **vertex** in a graph?
2. What is an **edge** in a graph?
3. What is the difference between a directed graph and an undirected graph?

### Section B: Counting Vertices & Edges
4. A graph has vertices $V = \{A, B, C, D, E\}$ and edges $E = \{(A,B), (B,C), (C,D), (D,E), (E,A), (A,C)\}$.
   - How many vertices are there?
   - How many edges are there?
5. Draw or describe the complete graph $K_4$ (every vertex connects to every other vertex). How many edges does it have?

---

## 📝 Homework 2: Vertex Degrees & The Handshaking Lemma

### Section A: Degree Calculations
1. In an undirected graph, what is the **degree** of a vertex?
2. State the **Handshaking Lemma** formula.
3. Can a graph have an odd sum of vertex degrees? Why or why not?

### Section B: Handshaking Problems
4. A graph has 6 vertices with degrees $4, 3, 2, 2, 2, 1$. How many edges does the graph have?
5. A graph has 5 vertices, each with degree 4. How many edges are in the graph?
6. Is it possible to draw an undirected graph with 4 vertices having degrees $3, 3, 3, 2$?

---

## 📝 Homework 3: Walks, Paths, Cycles & Adjacency

### Section A: Definitions
1. What is the difference between a **walk** and a **path**?
2. What is a **cycle**?

### Section B: Path Finding
3. In a graph with edges $(A, B), (B, C), (C, D), (A, D), (B, D)$:
   - List all simple paths from $A$ to $C$ of length 2.
   - List all simple paths from $A$ to $C$ of length 3.
4. Construct the $4 \times 4$ adjacency matrix for the graph above with vertices ordered $A, B, C, D$.

---

## 📝 Homework 4: Pseudocode & Contest 4 Mock Exam

### Section A: Pseudocode Tracing
1. What does the following program print?
   ```basic
   DEG_SUM = 0
   FOR I = 1 TO 4
     FOR J = 1 TO 4
       IF I <> J THEN
         DEG_SUM = DEG_SUM + 1
       END IF
     NEXT J
   NEXT I
   EDGES = DEG_SUM \ 2
   PRINT EDGES
   ```

### Section B: Elementary Contest 4 Mock Set
2. A graph has 8 vertices, each of degree 3. How many edges does it have?
3. In a directed graph, if vertex $A$ has 4 outgoing edges and 2 incoming edges, what is the out-degree of $A$?
4. What is the length of the shortest path from $A$ to $E$ in: $(A,B), (B,C), (C,D), (D,E), (A,C), (C,E)$?
5. How many edges are in a tree graph with 12 vertices?

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. A node or dot representing an entity/point.
2. A line or link connecting two vertices.
3. Directed graphs have one-way arrows; undirected graphs have two-way symmetric edges.
4. Vertices $= 5$; Edges $= 6$.
5. $K_4$ has 4 vertices. Each connects to 3 others: $\frac{4 \times 3}{2} = \mathbf{6 \text{ edges}}$.

### Homework 2 Solutions
1. The number of edges connected to that vertex.
2. $\sum \text{deg}(v) = 2 \times E$.
3. No, because the sum equals $2E$, which is always an even number!
4. Sum $= 4 + 3 + 2 + 2 + 2 + 1 = 14 \implies E = 14 / 2 = \mathbf{7 \text{ edges}}$.
5. Sum $= 5 \times 4 = 20 \implies E = 20 / 2 = \mathbf{10 \text{ edges}}$.
6. Sum $= 3 + 3 + 3 + 2 = 11$ (Odd!). **Impossible** by the Handshaking Lemma.

### Homework 3 Solutions
1. A walk can repeat vertices and edges; a path visits each vertex at most once.
2. A closed path that starts and ends at the same vertex.
3. Length 2: $A-B-C$ (1 path). Length 3: $A-D-B-C$ (1 path).
4. Adjacency Matrix:
   $$\begin{pmatrix} 0 & 1 & 0 & 1 \\ 1 & 0 & 1 & 1 \\ 0 & 1 & 0 & 1 \\ 1 & 1 & 1 & 0 \end{pmatrix}$$

### Homework 4 Solutions
1. Loops count all non-diagonal pairs: $4 \times 3 = 12$. $\text{EDGES} = 12 \setminus 2 = \mathbf{6}$ (Edges in $K_4$!).
2. Sum $= 8 \times 3 = 24 \implies E = 24 / 2 = \mathbf{12 \text{ edges}}$.
3. Out-degree is the number of outgoing edges $\implies \mathbf{4}$.
4. Path $A \rightarrow C \rightarrow E$ has length $\mathbf{2}$.
5. For any tree graph: $E = V - 1 = 12 - 1 = \mathbf{11 \text{ edges}}$.
