# Unit 4: Intermediate Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 4 (Matrix Powers, Planar Graphs, Adders & Multiplexers, ACSL Assembly Language, and Contest Programming). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Matrix Powers, Planarity & DAGs

### Section A: Walks of Length $k$ via $A^k$
1. Given adjacency matrix $A$ for vertices $\{1, 2, 3\}$:
   $$A = \begin{pmatrix} 0 & 1 & 1 \\ 1 & 0 & 1 \\ 1 & 1 & 0 \end{pmatrix}$$
   - (a) Compute $A^2$.
   - (b) How many walks of length 2 exist from vertex 1 to vertex 2?
   - (c) How many walks of length 3 exist from vertex 1 to vertex 1?

### Section B: Planar Graphs & Euler's Formula
2. A connected planar graph has 10 vertices and 15 edges. How many faces/regions does it divide the plane into?
3. A simple connected planar graph has 8 vertices. What is the maximum number of edges it can have?
4. Explain why $K_5$ (complete graph on 5 vertices) is non-planar using the inequality $E \le 3V - 6$.

---

## 📝 Homework 2: Half-Adders, Full-Adders & Hardware Logic

### Section A: Arithmetic Logic Units
1. Write the Boolean equations for the Sum ($S$) and Carry ($C$) of a **Half-Adder**.
2. Write the Boolean equations for the Sum ($S$) and Carry-out ($C_{out}$) of a **Full-Adder** with inputs $A, B, C_{in}$.
3. A Full-Adder has inputs $A=1, B=0, C_{in}=1$. What are the values of $S$ and $C_{out}$?
4. How many Half-Adders and OR gates are needed to construct one Full-Adder?

---

## 📝 Homework 3: ACSL Assembly Language Emulation

### Section A: Tracing Assembly Programs
1. Trace the accumulator and print output:
   ```assembly
         LOAD  A
         ADD   B
         MULT  C
         DIV   D
         STORE RES
         PRINT RES
         END
   A     DC    5
   B     DC    7
   C     DC    4
   D     DC    6
   RES   DC    0
   ```

2. What does the following program print?
   ```assembly
         LOAD  N
         STORE COUNT
         LOAD  ZERO
         STORE SUM
   LOOP  LOAD  COUNT
         BE    DONE
         ADD   SUM
         STORE SUM
         LOAD  COUNT
         SUB   ONE
         STORE COUNT
         BU    LOOP
   DONE  PRINT SUM
         END
   N     DC    4
   ONE   DC    1
   ZERO  DC    0
   COUNT DC    0
   SUM   DC    0
   ```

---

## 📝 Homework 4: Contest 4 Programming Challenge & Final Mock Contest

### Section A: Programming Challenge Blueprint
Implement a Python function `count_walks(adj_matrix: list[list[int]], k: int, start: int, end: int) -> int` that returns the number of walks of length $k$ between `start` and `end` vertices.

### Section B: Intermediate Contest 4 Mock Set
1. A connected planar graph with 14 vertices has every face bounded by 3 edges ($2E = 3F$). How many edges does it have?
2. If $A$ is an adjacency matrix and $(A^2)_{3, 3} = 4$, what does this tell you about vertex 3?
3. What is printed by this ACSL Assembly program?
   ```assembly
         LOAD  X
         BG    POS
         LOAD  NEG_ONE
         BU    FINISH
   POS   LOAD  POS_ONE
   FINISH PRINT ACC
         END
   X     DC    -15
   POS_ONE DC  1
   NEG_ONE DC -1
   ```
4. How many distinct topological orderings exist for a DAG with vertices $\{A, B, C\}$ and edges $(A, B), (A, C)$?

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. (a) Matrix multiplication:
   $$A^2 = \begin{pmatrix} 2 & 1 & 1 \\ 1 & 2 & 1 \\ 1 & 1 & 2 \end{pmatrix}$$
   (b) $(A^2)_{1, 2} = \mathbf{1 \text{ walk}}$ ($1 \rightarrow 3 \rightarrow 2$).  
   (c) $A^3 = A \cdot A^2$: $(A^3)_{1, 1} = 0(2) + 1(1) + 1(1) = \mathbf{2 \text{ walks}}$ ($1 \rightarrow 2 \rightarrow 3 \rightarrow 1$ and $1 \rightarrow 3 \rightarrow 2 \rightarrow 1$).
2. $V - E + F = 2 \implies 10 - 15 + F = 2 \implies -5 + F = 2 \implies F = \mathbf{7 \text{ faces}}$.
3. $E_{max} = 3V - 6 = 3(8) - 6 = \mathbf{18 \text{ edges}}$.
4. For $K_5$: $V = 5, E = \frac{5 \times 4}{2} = 10$.
   Max edges for planarity: $3V - 6 = 3(5) - 6 = 9$.
   Since $10 > 9$, $K_5$ violates the planar inequality and cannot be planar!

### Homework 2 Solutions
1. $S = A \oplus B$, $C = A \cdot B$.
2. $S = A \oplus B \oplus C_{in}$, $C_{out} = A B + C_{in}(A \oplus B)$.
3. Inputs: $A=1, B=0, C_{in}=1$:
   $S = 1 \oplus 0 \oplus 1 = 0$.
   $C_{out} = (1)(0) + 1(1 \oplus 0) = 0 + 1 = 1$.
   $S = \mathbf{0}, C_{out} = \mathbf{1}$ (Binary sum of $1+0+1 = 2 = 10_2$).
4. **2 Half-Adders** and **1 OR gate**.

### Homework 3 Solutions
1. $\text{ACC} = 5 + 7 = 12 \implies 12 \times 4 = 48 \implies 48 // 6 = 8$. Output: **8**.
2. Sum of numbers from $N$ down to 1! For $N=4$: $4 + 3 + 2 + 1 = 10$. Output: **10**.

### Homework 4 Solutions
1. $2E = 3F \implies F = \frac{2}{3}E$.
   $V - E + F = 2 \implies 14 - E + \frac{2}{3}E = 2 \implies 12 = \frac{1}{3}E \implies E = \mathbf{36 \text{ edges}}$.
2. The degree of vertex 3 is 4! In an undirected graph with no self-loops, $(A^2)_{i, i} = \text{deg}(v_i)$.
3. $X = -15 \le 0$, so `BG POS` does not jump. Loads `NEG_ONE` ($-1$) and jumps to `FINISH`. Output: **-1**.
4. $A$ must come first. $B$ and $C$ can be in either order: $A, B, C$ or $A, C, B \implies \mathbf{2 \text{ orderings}}$.
