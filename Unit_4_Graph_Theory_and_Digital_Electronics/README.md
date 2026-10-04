# Unit 4: Graph Theory & Digital Electronics

## 📌 Unit Overview
Unit 4 corresponds to **ACSL Contest 4**. It covers two essential computer science pillars:
1. **Graph Theory**: Modeling networks, relationships, and connections using vertices and edges. Covers degrees, Eulerian/Hamiltonian paths, adjacency matrices, and matrix power path-counting.
2. **Digital Electronics**: Physical silicon hardware logic, logic gates (AND, OR, NOT, XOR, NAND, NOR, XNOR), circuit schematic tracing, half/full adders, and ACSL Assembly Language emulation.
3. **"What Does This Program Do?" & ACSL Assembly**: Tracing low-level assembly language registers and high-level pseudocode algorithms.

---

## 🎯 Division Specific Focus & Matrix

| Topic / Feature | Elementary Division | Junior Division | Intermediate Division |
| :--- | :--- | :--- | :--- |
| **Graph Theory** | Vertices, Edges, Directed vs Undirected, Vertex Degrees, Handshaking Lemma | Eulerian paths/circuits, Hamiltonian paths, Adjacency matrices, Tree properties | Walks of length $k$ using $A^k$ matrix powers, Planar graphs ($V-E+F=2$), DAGs, Topological sort |
| **Digital Electronics** | Basic visual gate recognition (AND, OR, NOT) | Circuit schematics with 7 gates (AND, OR, NOT, XOR, NAND, NOR, XNOR), Truth tables | Circuit minimization, Half-Adders, Full-Adders, Multi-level gate equivalence |
| **Assembly Language** | N/A | Introduction to simple accumulator concepts | Official ACSL Assembly Language (LOAD, STORE, ADD, SUB, MULT, DIV, BG, BE, BL, BU, READ, PRINT, END) |
| **Pseudocode** | Graph matrix grid lookup, loops | Path traversal counters, connected components | Graph search algorithms (BFS/DFS), complex assembly simulations |
| **Programming Contest** | N/A | 1 problem (HackerRank) | 1 problem (Advanced HackerRank) |

---

## 📁 Subfolders & Level Curricula

- **[Elementary Division Curriculum (4 × 90 Mins)](./elementary/README.md)**
  - Resources: **[Homework Sets & Solutions](./elementary/homework.md)** | **[Markdown Slides](./elementary/slides.md)** | **[PowerPoint Deck (.pptx)](./elementary/slides.pptx)**
  - Class 1: Introduction to Graphs: Vertices, Edges & Directed Arrows.
  - Class 2: Degrees of Vertices & The Magic Handshaking Lemma.
  - Class 3: Walks, Paths, Cycles & Simple Adjacency Tables.
  - Class 4: "What Does This Program Do?" (Graph Grid Tracing) + Contest 4 Mock Test.
- **[Junior Division Curriculum (4 × 90 Mins)](./junior/README.md)**
  - Resources: **[Homework Sets & Solutions](./junior/homework.md)** | **[Markdown Slides](./junior/slides.md)** | **[PowerPoint Deck (.pptx)](./junior/slides.pptx)**
  - Class 1: Graph Theory: Adjacency Matrices, Cycles & Eulerian Paths/Circuits.
  - Class 2: Digital Electronics: The 7 Logic Gates & Circuit Diagram Tracing.
  - Class 3: Circuit Minimization & Combining Digital Logic with Boolean Algebra.
  - Class 4: "What Does This Program Do?" & Contest 4 Mock Exam.
- **[Intermediate Division Curriculum (4 × 90 Mins)](./intermediate/README.md)**
  - Resources: **[Homework Sets & Solutions](./intermediate/homework.md)** | **[Markdown Slides](./intermediate/slides.md)** | **[PowerPoint Deck (.pptx)](./intermediate/slides.pptx)**
  - Class 1: Advanced Graph Theory: Matrix Powers ($A^k$), Planarity ($V-E+F=2$) & Topological Sorting.
  - Class 2: Advanced Digital Electronics: Half-Adders, Full-Adders & Multi-Level Circuit Synthesis.
  - Class 3: ACSL Assembly Language Masterclass (Accumulator, Opcodes, Branching).
  - Class 4: Contest 4 Programming Challenge (Graph Paths & Circuit Simulators) + Final Comprehensive Mock Contest.

---

## 💡 Quick Reference: Euler's Theorem for Graphs
- A connected graph has an **Eulerian Circuit** (starts and ends at the same vertex, traverses every edge exactly once) if and only if **every vertex has an EVEN degree**.
- A connected graph has an **Eulerian Trail/Path** (starts and ends at different vertices, traverses every edge exactly once) if and only if **exactly TWO vertices have an ODD degree**.
