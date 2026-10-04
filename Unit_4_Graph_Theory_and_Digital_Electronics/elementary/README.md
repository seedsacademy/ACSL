# Unit 4: Elementary Division (4 Classes × 90 Minutes)

This curriculum prepares elementary students (Grades 3–6) for **ACSL Contest 4** (Graph Theory, Simple Logic Circuits, and "What Does This Program Do?").

---

## 📅 Class 1: Introduction to Graphs (Vertices & Edges)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Map of subway stations / airline flight routes.
- **0:15 – 0:45 (30 min)**: Core Concept:
  - What is a Graph? Set of **Vertices** (dots/nodes) and **Edges** (lines/connections).
  - Undirected graphs (two-way streets) vs. Directed graphs (one-way arrows).
  - Parallel edges and self-loops.
- **0:45 – 0:70 (25 min)**: Guided Practice: Counting vertices ($V$) and edges ($E$) from diagrams. Drawing graphs given edge lists.
- **0:70 – 0:85 (15 min)**: In-Class Graph Drawing Challenge.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Identify the number of vertices and edges in any given graph.
2. Differentiate between directed and undirected graphs.
3. Translate a list of edge pairs into a clear visual diagram.

### 📘 Core Content & Worked Examples

#### Example 1: Graph Vocabulary
Consider a graph with vertices $V = \{A, B, C, D\}$ and edges $E = \{(A,B), (B,C), (C,D), (D,A), (A,C)\}$.
- Number of Vertices $V = 4$.
- Number of Edges $E = 5$.
- Is it directed? No arrows are given, so it is **undirected**.

---

## 📅 Class 2: Vertex Degrees & The Handshaking Lemma

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Counting edges flashcards.
- **0:15 – 0:45 (30 min)**: Core Concept:
  - **Degree of a Vertex**: The number of edges connected to that vertex.
  - In directed graphs: In-degree (arrows coming in) and Out-degree (arrows going out).
  - **The Handshaking Lemma**:
    $$\sum \text{deg}(v) = 2 \times E$$
    *Why? Every edge connects two vertices, so each edge contributes 2 to the sum of degrees!*
- **0:45 – 0:70 (25 min)**: Guided Practice: Solving for unknown edge counts or degrees using the Handshaking Lemma.
- **0:70 – 0:85 (15 min)**: Timed Degree Sprint: 4 contest problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Calculate the degree of every vertex in a graph.
2. Use the Handshaking Lemma to find the total number of edges without counting manually.
3. Understand why the sum of all degrees in any undirected graph is **always an even number**.

### 📘 Worked Example: The Handshaking Lemma
A graph has 5 vertices with degrees $4, 3, 3, 2, 2$. How many edges does the graph have?
- Step 1: Add all degrees:
  $$\text{Sum} = 4 + 3 + 3 + 2 + 2 = 14$$
- Step 2: Use $\sum \text{deg} = 2 \times E$:
  $$14 = 2 \times E \implies E = \mathbf{7} \text{ edges}.$$

*Can a graph have 5 vertices with degrees $3, 3, 3, 2, 2$?*
- Sum $= 3 + 3 + 3 + 2 + 2 = 13$ (Odd!).
- **Impossible!** A graph can never have an odd sum of degrees.

---

## 📅 Class 3: Walks, Paths, Cycles & Adjacency Tables

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick handshaking calculation drill.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - **Walk**: A sequence of alternating vertices and edges.
  - **Path**: A walk where no vertex is repeated.
  - **Cycle**: A path that starts and ends at the same vertex.
  - **Adjacency Table / Matrix**: A table where row $i$ and column $j$ has a 1 if connected by an edge, else 0.
- **0:45 – 0:70 (25 min)**: Guided Practice: Finding all paths of length 2 or 3 between two vertices.
- **0:70 – 0:85 (15 min)**: Timed Path Finding Drill: 3 problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Trace paths of specified length between two vertices.
2. Identify cycles in a graph.
3. Read and construct simple $0/1$ adjacency tables.

### 📘 Worked Example: Finding Paths of Length 2
In the graph with edges $(A, B), (B, C), (A, C), (B, D), (C, D)$:
Find all simple paths of length 2 from $A$ to $D$.
- A path of length 2 must visit 1 intermediate vertex: $A \rightarrow X \rightarrow D$.
- Check possible vertices $X$:
  - If $X = B$: Edge $(A, B)$ exists? Yes. Edge $(B, D)$ exists? Yes. $\implies A - B - D$.
  - If $X = C$: Edge $(A, C)$ exists? Yes. Edge $(C, D)$ exists? Yes. $\implies A - C - D$.
- Total simple paths of length 2 from $A$ to $D$: **2 paths** ($A-B-D$ and $A-C-D$).

---

## 📅 Class 4: "What Does This Program Do?" & Contest 4 Mock Test

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick path tracing puzzle.
- **0:15 – 0:45 (30 min)**: Pseudocode Focus: 2D array grid search representing connections.
- **0:45 – 0:75 (30 min)**: **Full Timed Contest 4 Mock Test (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Scoring, detailed review, and course graduation!

### 📘 Pseudocode Tracing Example (Graph Connection Count)

```basic
DIM G(4, 4)
' G(i, j) = 1 if edge exists
FOR I = 1 TO 4
  FOR J = 1 TO 4
    IF I <> J AND (I + J) MOD 2 = 0 THEN
      G(I, J) = 1
    ELSE
      G(I, J) = 0
    END IF
  NEXT J
NEXT I
TOTAL = 0
FOR K = 1 TO 4
  TOTAL = TOTAL + G(1, K)
NEXT K
PRINT TOTAL
```
- Line 5: Connected if $I \ne J$ and $I + J$ is even.
- When $I = 1$:
  - $J = 1$: $I = J \implies 0$
  - $J = 2$: $1 + 2 = 3$ (odd) $\implies 0$
  - $J = 3$: $1 + 3 = 4$ (even) and $1 \ne 3 \implies 1$
  - $J = 4$: $1 + 4 = 5$ (odd) $\implies 0$
- Row 1 values: $0, 0, 1, 0$.
- `TOTAL` $= G(1, 1) + G(1, 2) + G(1, 3) + G(1, 4) = 0 + 0 + 1 + 0 = \mathbf{1}$.

---

### 🏆 Unit 4 Mock Contest (Elementary Division)
1. A graph has 6 vertices with degrees $3, 2, 4, 1, 2, 4$. How many edges are in the graph? (*Answer: Sum = 16, Edges = $16 / 2 = 8$*)
2. In a directed graph, vertex $A$ has 3 arrows pointing to other vertices, and 2 arrows pointing into it. What is the out-degree of $A$? (*Answer: 3*)
3. How many cycles are in a complete graph $K_3$ (a triangle with vertices A, B, C)? (*Answer: 1 cycle of 3 vertices*)
4. Given vertices $A, B, C, D$ with edges $(A, B), (B, C), (C, D), (D, A)$. What is the length of the shortest path from $A$ to $C$? (*Answer: 2 edges*)
5. What does the following program print?
   ```basic
   E = 0
   FOR I = 1 TO 5
     E = E + I
   NEXT I
   PRINT E * 2
   ```
   (*Answer: $E = 1+2+3+4+5 = 15 \implies 15 \times 2 = 30$*)
