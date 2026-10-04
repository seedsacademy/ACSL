# Unit 4: Intermediate Division (4 Classes × 90 Minutes)

This curriculum prepares high school competitors (Grades 10–12) for **ACSL Contest 4** at the Intermediate/Senior Division level, covering matrix powers for path counting, planar graphs, advanced digital hardware (adders/multiplexers), official ACSL Assembly Language emulation, and contest programming strategies.

---

## 📅 Class 1: Advanced Graph Theory (Matrix Powers, Planarity & DAGs)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: Adjacency matrix construction and matrix multiplication review.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - **The Matrix Power Theorem**: If $A$ is the adjacency matrix of a graph, then the $(i, j)$-th entry of the matrix power $A^k$ is **the exact number of walks of length $k$** from vertex $i$ to vertex $j$.
  - **Planar Graphs & Euler's Formula**:
    $$V - E + F = 2$$
    - Face degree theorem: $2E \ge 3F \implies E \le 3V - 6$ (for simple planar graphs with $V \ge 3$).
    - Non-planar test: Kuratowski's theorem ($K_5$ and $K_{3,3}$).
  - **Directed Acyclic Graphs (DAGs)** & Topological Sorting (Kahn's in-degree algorithm).
- **0:45 – 0:70 (25 min)**: Guided Practice: Calculating walks of length 2 and 3 using $A^2$ and $A^3$; solving planar graph face/edge equations.
- **0:70 – 0:85 (15 min)**: Timed Speed Challenge: 3 contest-grade graph theory problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Compute the number of walks of length $k$ between two vertices by calculating $(A^k)_{ij}$.
2. Apply Euler's Planar Formula $V - E + F = 2$ and the planarity inequality $E \le 3V - 6$.
3. Perform topological sorts on Directed Acyclic Graphs.

### 📘 Core Content & Worked Examples

#### Example 1: Walks of Length 2 Using $A^2$
Given adjacency matrix $A$ for vertices $\{1, 2, 3\}$:
$$A = \begin{pmatrix} 0 & 1 & 1 \\ 1 & 0 & 1 \\ 1 & 1 & 0 \end{pmatrix}$$
Find the number of walks of length 2 from vertex 1 to vertex 1 ($A^2_{11}$):
$$A^2_{11} = \sum_{k=1}^3 A_{1k} A_{k1} = A_{11}A_{11} + A_{12}A_{21} + A_{13}A_{31} = (0)(0) + (1)(1) + (1)(1) = 0 + 1 + 1 = \mathbf{2}.$$
*(The two walks are $1 \rightarrow 2 \rightarrow 1$ and $1 \rightarrow 3 \rightarrow 1$.)*

#### Example 2: Euler's Planar Formula
A connected planar graph has 12 vertices and divides the plane into 8 faces/regions. How many edges does the graph have?
- Use $V - E + F = 2$:
  $$12 - E + 8 = 2 \implies 20 - E = 2 \implies E = \mathbf{18} \text{ edges}.$$

---

## 📅 Class 2: Advanced Digital Electronics (Adders & Combinational Logic)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick logic gate truth table check.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - **Half-Adder**:
    - Sum: $S = A \oplus B$
    - Carry: $C = A \cdot B$
  - **Full-Adder**:
    - Adds three bits: $A$, $B$, and Carry-in $C_{in}$.
    - Sum: $S = A \oplus B \oplus C_{in}$
    - Carry-out: $C_{out} = A B + B C_{in} + A C_{in} = A B + C_{in}(A \oplus B)$
  - Multiplexers (MUX 2:1 and 4:1) and Decoders.
  - Universal Gates: Implementing any Boolean function using *only* NAND gates or *only* NOR gates.
- **0:45 – 0:70 (25 min)**: Guided Practice: Tracing cascaded adders and multi-level combinational circuits.
- **0:70 – 0:85 (15 min)**: Timed Contest Drill: 3 circuit analysis problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. State the exact Boolean formulas and circuit schematics for Half-Adders and Full-Adders.
2. Trace ripple-carry adder outputs given multi-bit inputs.
3. Synthesize circuits using NAND/NOR universal logic gates.

---

## 📅 Class 3: Official ACSL Assembly Language Masterclass

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: What is machine code and assembly? The accumulator model.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Official ACSL Assembly Instruction Set:
    - `LOAD X`: ACC $\leftarrow$ value of X
    - `STORE X`: memory[X] $\leftarrow$ ACC
    - `ADD X`: ACC $\leftarrow$ ACC + value of X
    - `SUB X`: ACC $\leftarrow$ ACC - value of X
    - `MULT X`: ACC $\leftarrow$ ACC $\times$ value of X
    - `DIV X`: ACC $\leftarrow$ ACC $/$ value of X (integer division)
    - `BG LABEL`: Branch to `LABEL` if ACC $> 0$
    - `BE LABEL`: Branch to `LABEL` if ACC $= 0$
    - `BL LABEL`: Branch to `LABEL` if ACC $< 0$
    - `BU LABEL`: Branch unconditionally to `LABEL`
    - `READ X`: Read next input into memory location X
    - `PRINT X`: Output value of X
    - `END`: Halt execution
    - `DC N`: Declare Constant with integer value N
- **0:45 – 0:70 (25 min)**: Guided Practice: Step-by-step tracing of an ACSL Assembly program with memory register tables.
- **0:70 – 0:85 (15 min)**: Timed Assembly Tracing Sprint: 2 contest questions.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Trace the accumulator (ACC) and memory variables across ACSL assembly instructions.
2. Correctly execute conditional branching (`BG`, `BE`, `BL`) based on the current ACC value.
3. Translate loops and conditionals between assembly and high-level pseudocode.

### 📘 Worked Example: ACSL Assembly Trace

```assembly
      LOAD  A
LOOP  SUB   B
      BL    DONE
      STORE A
      LOAD  C
      ADD   ONE
      STORE C
      LOAD  A
      BU    LOOP
DONE  PRINT C
      END
A     DC    14
B     DC    4
C     DC    0
ONE   DC    1
```

#### Step-by-Step Execution Trace:
- Initial state: $A = 14, B = 4, C = 0, \text{ONE} = 1$.
- `LOAD A` $\implies \text{ACC} = 14$.
- **Iteration 1**:
  - `SUB B` $\implies \text{ACC} = 14 - 4 = 10$.
  - `BL DONE`: Is $\text{ACC} < 0$? No ($10 \not< 0$).
  - `STORE A` $\implies A = 10$.
  - `LOAD C` $\implies \text{ACC} = 0$.
  - `ADD ONE` $\implies \text{ACC} = 0 + 1 = 1$.
  - `STORE C` $\implies C = 1$.
  - `LOAD A` $\implies \text{ACC} = 10$.
  - `BU LOOP`
- **Iteration 2**:
  - `SUB B` $\implies \text{ACC} = 10 - 4 = 6$.
  - `BL DONE`: No.
  - `STORE A` $\implies A = 6$.
  - $C$ becomes $1 + 1 = 2$.
  - `LOAD A` $\implies \text{ACC} = 6$.
  - `BU LOOP`
- **Iteration 3**:
  - `SUB B` $\implies \text{ACC} = 6 - 4 = 2$.
  - `BL DONE`: No.
  - `STORE A` $\implies A = 2$.
  - $C$ becomes $2 + 1 = 3$.
  - `LOAD A` $\implies \text{ACC} = 2$.
  - `BU LOOP`
- **Iteration 4**:
  - `SUB B` $\implies \text{ACC} = 2 - 4 = -2$.
  - `BL DONE`: Is $\text{ACC} < 0$? **YES ($-2 < 0$)!** Jump to `DONE`.
- `DONE PRINT C`: Value of $C$ is **3**.
- `END`: Halts.
- *Notice*: This assembly program implements integer division: $14 // 4 = 3$! Output: **3**.

---

## 📅 Class 4: Contest 4 Programming Challenge & Final Mock Contest

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick assembly instruction trace.
- **0:15 – 0:45 (30 min)**: Contest Programming Deep Dive:
  - Typical Contest 4 problems: "Graph Path Finding", "Logic Circuit Evaluator", "Connected Components Finder".
  - Implementing BFS / DFS and adjacency list graphs in Python / Java.
- **0:45 – 0:75 (30 min)**: **Full Timed ACSL Contest 4 Mock Exam (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Final contest review, awards, and complete curriculum celebration!

### 💻 Contest 4 Programming Blueprint (Graph Path Counting in Python)

```python
# Sample Contest 4 Solution: Counting Paths of Length K
import numpy as np

def count_walks_of_length_k(adj_matrix, k, start_node, end_node):
    # Raise adjacency matrix to power k
    A = np.array(adj_matrix, dtype=int)
    A_k = np.linalg.matrix_power(A, k)
    return int(A_k[start_node][end_node])
```

---

### 🏆 Unit 4 Intermediate Division Mock Contest
1. In a simple connected planar graph with 9 vertices, what is the maximum possible number of edges? (*Answer: $E \le 3V - 6 = 3(9) - 6 = 21$*)
2. Let $A$ be the adjacency matrix of a 4-vertex graph. If $(A^3)_{2, 4} = 5$, what does this 5 represent? (*Answer: There are exactly 5 distinct walks of length 3 from vertex 2 to vertex 4*)
3. A Full-Adder has inputs $A=1, B=1, C_{in}=1$. What are the values of Sum ($S$) and Carry-out ($C_{out}$)? (*Answer: $S = 1, C_{out} = 1$*)
4. In ACSL Assembly Language, what is printed by the following program?
   ```assembly
         LOAD  X
         MULT  Y
         DIV   Z
         ADD   ONE
         STORE RES
         PRINT RES
         END
   X     DC    15
   Y     DC    4
   Z     DC    7
   ONE   DC    3
   RES   DC    0
   ```
   (*Answer: $(15 \times 4) // 7 + 3 = 60 // 7 + 3 = 8 + 3 = 11$*)
5. What does the following pseudocode print?
   ```basic
   DIM DEG(5)
   FOR I = 1 TO 4
     FOR J = I + 1 TO 5
       IF (I * J) MOD 2 = 1 THEN
         DEG(I) = DEG(I) + 1
         DEG(J) = DEG(J) + 1
       END IF
     NEXT J
   NEXT I
   PRINT DEG(1) + DEG(3) + DEG(5)
   ```
   (*Answer: $I \times J$ is odd only when both $I$ and $J$ are odd. Odd vertices in $1..5$ are $\{1, 3, 5\}$ (3 vertices). They form a $K_3$ triangle! Each has degree 2. Sum $= 2 + 2 + 2 = 6$*)
