# Unit 4: Junior Division (4 Classes × 90 Minutes)

This curriculum prepares middle school students (Grades 7–9) for **ACSL Contest 4** (Graph Theory, Digital Electronics, and "What Does This Program Do?").

---

## 📅 Class 1: Graph Theory (Adjacency Matrices & Eulerian Paths)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: Vertex degrees and handshaking lemma review.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Adjacency Matrices: $A_{ij} = 1$ if edge $(i, j)$ exists, else $0$.
  - Undirected matrices are symmetric ($A = A^T$); row sum = degree of vertex $i$.
  - **Eulerian Circuits**: A closed walk traversing every edge exactly once $\iff$ graph is connected and **all vertices have EVEN degrees**.
  - **Eulerian Trails/Paths**: An open walk traversing every edge exactly once $\iff$ graph is connected and **exactly TWO vertices have ODD degrees** (must start at one odd vertex and end at the other!).
  - Hamiltonian Paths vs. Eulerian Paths (Hamiltonian visits vertices; Eulerian visits edges).
- **0:45 – 0:70 (25 min)**: Guided Practice: Identifying Eulerian circuits/paths and building adjacency matrices.
- **0:70 – 0:85 (15 min)**: Timed Speed Challenge: 3 Eulerian & matrix problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Construct and read adjacency matrices for directed and undirected graphs.
2. Determine instantaneously whether a graph possesses an Eulerian Circuit, an Eulerian Trail, or neither.
3. Identify valid Eulerian sequences of edges.

### 📘 Core Content & Worked Examples

#### Example: Eulerian Path Theorem
Determine if the following graph has an Eulerian Circuit, an Eulerian Path, or neither:
- Vertices: $A, B, C, D, E$
- Edges: $(A, B), (A, C), (B, C), (B, D), (C, D), (C, E), (D, E)$

1. Calculate degrees of each vertex:
   - $\text{deg}(A) = 2$ (edges to $B, C$) $\rightarrow$ **EVEN**
   - $\text{deg}(B) = 3$ (edges to $A, C, D$) $\rightarrow$ **ODD**
   - $\text{deg}(C) = 4$ (edges to $A, B, D, E$) $\rightarrow$ **EVEN**
   - $\text{deg}(D) = 3$ (edges to $B, C, E$) $\rightarrow$ **ODD**
   - $\text{deg}(E) = 2$ (edges to $C, D$) $\rightarrow$ **EVEN**
2. Count odd vertices:
   - Exactly **two** odd vertices ($B$ and $D$).
3. Conclusion:
   - Has an **Eulerian Path** (must start at $B$ and end at $D$, or start at $D$ and end at $B$).
   - Does **not** have an Eulerian Circuit.

---

## 📅 Class 2: Digital Electronics (The 7 Logic Gates & Schematics)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick logic gate symbol flashcards.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - The 7 Gates:
    1. **AND** ($A \cdot B$): Flat back, rounded front.
    2. **OR** ($A + B$): Curved back, pointed front.
    3. **NOT** ($\overline{A}$): Triangle with bubble.
    4. **XOR** ($A \oplus B$): Double curved back, pointed front.
    5. **NAND** ($\overline{A \cdot B}$): AND gate with an inversion bubble.
    6. **NOR** ($\overline{A + B}$): OR gate with an inversion bubble.
    7. **XNOR** ($\overline{A \oplus B}$): XOR gate with an inversion bubble.
- **0:45 – 0:70 (25 min)**: Guided Practice: Tracing circuit schematics step-by-step from left inputs to right output.
- **0:70 – 0:85 (15 min)**: Timed Circuit Tracing: 3 schematic evaluation problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Recognize the standard ANSI graphic symbols for all 7 digital logic gates.
2. Label intermediate wire outputs sequentially through a multi-gate circuit.
3. Write the exact unsimplified Boolean output expression for any given circuit schematic.

### 📘 Core Content & Worked Examples

#### Example: Circuit Tracing
Given a circuit with inputs $A, B, C$:
1. $A$ and $B$ enter a `NAND` gate $\implies W_1 = \overline{A \cdot B}$.
2. $B$ and $C$ enter an `OR` gate $\implies W_2 = B + C$.
3. $W_1$ and $W_2$ enter an `XOR` gate $\implies \text{Output } F = W_1 \oplus W_2$.
- Find the output $F$ when $A = 1, B = 1, C = 0$:
  - $W_1 = \overline{1 \cdot 1} = \overline{1} = 0$.
  - $W_2 = 1 + 0 = 1$.
  - $F = 0 \oplus 1 = \mathbf{1}$.

---

## 📅 Class 3: Circuit Minimization & Logic Simplification

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Rapid gate output drill.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Converting a circuit diagram into a Boolean expression.
  - Applying Boolean laws (De Morgan's, Absorption) to simplify physical circuits.
  - Finding how many input combinations $(A, B, C)$ yield output $1$.
  - Equivalent circuits: Recognizing that `NAND` with inputs tied together is `NOT`.
- **0:45 – 0:70 (25 min)**: Guided Practice: Reducing a 5-gate circuit to a single gate!
- **0:70 – 0:85 (15 min)**: Timed Contest Drill: 3 problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Express logic circuits as algebraic expressions and reduce them to minimal literal form.
2. Determine input combinations that activate circuit outputs.
3. Replace complex sub-circuits with functionally identical simpler gates.

### 📘 Worked Example: Minimizing a Circuit
A circuit produces:
$$F = \overline{(A + B)} + (A \cdot \overline{B})$$
- Simplify algebraically:
  $$F = \overline{A} \cdot \overline{B} + A \cdot \overline{B}$$
- Factor out $\overline{B}$:
  $$F = (\overline{A} + A) \cdot \overline{B} = 1 \cdot \overline{B} = \mathbf{\overline{B}}.$$
- Remarkable conclusion: The entire circuit with inputs $A$ and $B$ is equivalent to just a single `NOT` gate on input $B$! Input $A$ has zero effect on the output.

---

## 📅 Class 4: "What Does This Program Do?" & Contest 4 Mock Exam

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick Eulerian circuit condition question.
- **0:15 – 0:45 (30 min)**: Pseudocode Focus: Graph traversal simulation (Counting connected neighbors, degree calculations).
- **0:45 – 0:75 (30 min)**: **Full Timed ACSL Contest 4 Mock Exam (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Detailed review and end-of-unit celebration.

### 📘 Pseudocode Tracing Example (Vertex Degree Calculator)

```basic
DIM M(4, 4)
' Adjacency Matrix
DATA 0, 1, 1, 0
DATA 1, 0, 1, 1
DATA 1, 1, 0, 1
DATA 0, 1, 1, 0

MAX_DEG = 0
FOR I = 1 TO 4
  DEG = 0
  FOR J = 1 TO 4
    READ M(I, J)
    DEG = DEG + M(I, J)
  NEXT J
  IF DEG > MAX_DEG THEN
    MAX_DEG = DEG
  END IF
NEXT I
PRINT MAX_DEG
```
- Row 1 sum: $0 + 1 + 1 + 0 = 2$
- Row 2 sum: $1 + 0 + 1 + 1 = 3$
- Row 3 sum: $1 + 1 + 0 + 1 = 3$
- Row 4 sum: $0 + 1 + 1 + 0 = 2$
- `MAX_DEG` = **3**.

---

### 🏆 Unit 4 Junior Division Mock Contest
1. In a connected graph with vertices $A, B, C, D, E$, the degrees are $\text{deg}(A)=4, \text{deg}(B)=2, \text{deg}(C)=3, \text{deg}(D)=3, \text{deg}(E)=2$. Does an Eulerian path exist? If so, which vertices could be the start of the path? (*Answer: Yes; must start at $C$ or $D$*)
2. How many edges are in a tree graph with 19 vertices? (*Answer: $E = V - 1 = 19 - 1 = 18$*)
3. For what input values of $(A, B, C)$ does the gate expression $\overline{(A \text{ XOR } B)} \text{ AND } C$ equal 1? (*Answer: $C=1$ and $A=B$, so $(0,0,1)$ and $(1,1,1)$*)
4. What single logic gate is equivalent to $\overline{\overline{A} \cdot \overline{B}}$? (*Answer: By De Morgan's: $A + B$, which is an OR gate!*)
5. What does the following program print?
   ```basic
   A = 5
   B = 12
   C = 0
   WHILE B > 0
     IF B MOD 2 = 1 THEN
       C = C + A
     END IF
     A = A * 2
     B = B \ 2
   END WHILE
   PRINT C
   ```
   (*Answer: Binary Russian Peasant Multiplication: computes $5 \times 12 = 60$*)
