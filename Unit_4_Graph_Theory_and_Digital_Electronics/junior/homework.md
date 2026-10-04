# Unit 4: Junior Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 4 (Eulerian Graphs, Digital Electronics, Circuit Minimization, and Junior Pseudocode). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Adjacency Matrices & Eulerian Graphs

### Section A: Eulerian Circuits & Trails
1. State the exact condition for a connected graph to contain an **Eulerian Circuit**.
2. State the exact condition for a connected graph to contain an **Eulerian Trail/Path**.
3. In a graph with vertices $A, B, C, D, E$, the degrees are $\text{deg}(A)=4, \text{deg}(B)=2, \text{deg}(C)=3, \text{deg}(D)=3, \text{deg}(E)=4$.
   - Does it have an Eulerian circuit?
   - Does it have an Eulerian path? If so, what are the only possible starting vertices?

### Section B: Adjacency Matrices
4. Given the adjacency matrix $M$:
   $$M = \begin{pmatrix} 0 & 1 & 1 & 0 \\ 1 & 0 & 1 & 1 \\ 1 & 1 & 0 & 0 \\ 0 & 1 & 0 & 0 \end{pmatrix}$$
   - Find the degree of vertex 2 (row 2).
   - How many total edges are in this graph?

---

## 📝 Homework 2: The 7 Digital Logic Gates & Circuit Schematics

### Section A: Logic Gate Behavior
1. Complete the table:
   | Gate | Output is 1 when... | Formula |
   | :-: | :-: | :-: |
   | **AND** | | $A \cdot B$ |
   | **OR** | | $A + B$ |
   | **XOR** | | $A \oplus B$ |
   | **NAND** | | $\overline{A \cdot B}$ |
   | **NOR** | | $\overline{A + B}$ |
   | **XNOR** | | $\overline{A \oplus B}$ |

### Section B: Schematic Tracing
2. A circuit has inputs $A, B, C$.
   - Inputs $A$ and $B$ feed into an `XOR` gate: $W_1$.
   - Input $C$ and $W_1$ feed into a `NAND` gate: Output $F$.
   - Find $F$ when $A = 1, B = 0, C = 1$.
   - Find $F$ when $A = 1, B = 1, C = 1$.

---

## 📝 Homework 3: Circuit Simplification

### Section A: Boolean Reduction of Schematics
1. Find the simplified Boolean output for a circuit with output:
   $$F = \overline{A \cdot B} + \overline{A + B}$$
2. Find the simplified Boolean output for:
   $$G = (A \text{ XOR } B) \cdot \overline{A \cdot B}$$
3. How many combinations of $(A, B, C)$ produce output $1$ for:
   $$F = (A + \overline{B}) \cdot (B \oplus C)$$

---

## 📝 Homework 4: Junior Pseudocode & Contest 4 Mock Exam

### Section A: Pseudocode Tracing
1. What does the following program print?
   ```basic
   DIM DEG(4)
   DATA 0, 1, 1, 1
   DATA 1, 0, 0, 1
   DATA 1, 0, 0, 1
   DATA 1, 1, 1, 0
   FOR I = 1 TO 4
     DEG(I) = 0
     FOR J = 1 TO 4
       READ X
       DEG(I) = DEG(I) + X
     NEXT J
   NEXT I
   ODD_COUNT = 0
   FOR K = 1 TO 4
     IF DEG(K) MOD 2 = 1 THEN
       ODD_COUNT = ODD_COUNT + 1
     END IF
   NEXT K
   PRINT ODD_COUNT
   ```

### Section B: Junior Contest 4 Mock Set
2. How many edges are in a tree graph with 15 vertices?
3. A connected graph has 7 vertices with degrees $4, 4, 3, 3, 2, 2, 2$. Does an Eulerian path exist?
4. What logic gate has the same truth table as $\overline{\overline{A} + \overline{B}}$?
5. Find the value of $F$ if $A=0, B=1, C=1$:
   $$F = \overline{(A \text{ NOR } B)} \text{ XOR } (\overline{B} \text{ NAND } C)$$

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. Connected graph and **all vertices have EVEN degrees**.
2. Connected graph and **exactly TWO vertices have ODD degrees**.
3. Vertex degrees: $A=4, B=2, C=3, D=3, E=4$. Exactly two odd vertices ($C$ and $D$).
   - Eulerian circuit? **No**.
   - Eulerian path? **Yes**, must start at $C$ or $D$.
4. Row 2 sum: $1 + 0 + 1 + 1 = \mathbf{3}$ (Degree 3).
   Sum of all rows: $2 + 3 + 2 + 1 = 8 \implies \text{Total Edges} = 8 / 2 = \mathbf{4 \text{ edges}}$.

### Homework 2 Solutions
1. AND: Both 1. OR: At least one 1. XOR: Inputs are different. NAND: Not both 1. NOR: Both 0. XNOR: Inputs are identical.
2. $W_1 = A \oplus B$. $F = \overline{W_1 \cdot C}$.
   - Case 1 ($A=1, B=0, C=1$): $W_1 = 1 \oplus 0 = 1 \implies F = \overline{1 \cdot 1} = \mathbf{0}$.
   - Case 2 ($A=1, B=1, C=1$): $W_1 = 1 \oplus 1 = 0 \implies F = \overline{0 \cdot 1} = \mathbf{1}$.

### Homework 3 Solutions
1. $F = (\overline{A} + \overline{B}) + (\overline{A} \cdot \overline{B}) = \mathbf{\overline{A} + \overline{B}}$ (by absorption).
2. $A \oplus B$ already excludes $A \cdot B = 1 \implies G = \mathbf{A \oplus B}$.
3. For $F=1$: both factors must be 1.
   $(A + \overline{B}) = 1$ and $(B \oplus C) = 1$ ($B \ne C$).
   - If $B=0$: $C$ must be 1. $A$ can be 0 or 1 $\implies (0, 0, 1), (1, 0, 1)$ (2 triples).
   - If $B=1$: $A$ must be 1. $C$ must be 0 $\implies (1, 1, 0)$ (1 triple).
   - Total $= 2 + 1 = \mathbf{3 \text{ triples}}$.

### Homework 4 Solutions
1. Rows:
   - Row 1: $0+1+1+1 = 3$ (odd)
   - Row 2: $1+0+0+1 = 2$ (even)
   - Row 3: $1+0+0+1 = 2$ (even)
   - Row 4: $1+1+1+0 = 3$ (odd)
   - Total odd vertices $= \mathbf{2}$.
2. In any tree: $E = V - 1 = 15 - 1 = \mathbf{14 \text{ edges}}$.
3. Exactly two odd vertices (the two 3s) $\implies$ **Yes**, an Eulerian path exists.
4. By De Morgan's: $\overline{\overline{A} + \overline{B}} = A \cdot B \implies$ **AND gate**.
5. $A \text{ NOR } B = \overline{0 + 1} = 0 \implies \overline{0} = 1$.
   $\overline{B} \text{ NAND } C = \overline{0 \cdot 1} = 1$.
   $F = 1 \oplus 1 = \mathbf{0}$.
