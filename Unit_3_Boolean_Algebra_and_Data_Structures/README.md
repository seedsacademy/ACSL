# Unit 3: Boolean Algebra & Data Structures

## 📌 Unit Overview
Unit 3 corresponds to **ACSL Contest 3**. It combines two major branches of theoretical computer science:
1. **Boolean Algebra**: The mathematical calculus of two-state logic (`TRUE`/`FALSE` or $1$/$0$), encompassing truth tables, algebraic laws (De Morgan's, Distributive, Absorption), and circuit minimization via Karnaugh Maps.
2. **Data Structures**: Foundational memory organizations including linear structures (**Stacks** [LIFO] and **Queues** [FIFO]) and hierarchical tree structures (**Binary Search Trees** [BST], tree traversals, and balance properties).
3. **"What Does This Program Do?"**: Contest 3 pseudocode problems involving conditional branching, loops, and data structures.

---

## 🎯 Division Specific Focus & Matrix

| Topic / Feature | Elementary Division | Junior Division | Intermediate Division |
| :--- | :--- | :--- | :--- |
| **Boolean Algebra** | Truth tables, basic gates (AND, OR, NOT), simple evaluation | Formal algebraic laws, De Morgan's, Distributive, Absorption, algebraic reduction | 3 & 4-variable Karnaugh Maps (K-Maps), Min-terms, Max-terms, Don't-cares |
| **Stacks & Queues** | Push/Pop concepts conceptually | Formal Stack (LIFO) and Queue (FIFO) pointer simulation | Implementation nuances, double-ended queues (deques), priority queues |
| **Binary Trees** | Basic tree terminology (root, leaf, parent, child) | BST insertion, Inorder, Preorder, Postorder traversals, search paths | Internal vs. external nodes, tree height/depth formulas, BST deletion |
| **Pseudocode** | Basic logic branches, accumulator loops | Array modifications, nested conditionals, stack/queue simulation | Recursion on trees/arrays, dynamic state tracking |
| **Programming Contest** | N/A | 1 problem (HackerRank) | 1 problem (Advanced HackerRank) |

---

## 📁 Subfolders & Level Curricula

- **[Elementary Division Curriculum (4 × 90 Mins)](./elementary/README.md)**
  - Resources: **[Homework Sets & Solutions](./elementary/homework.md)** | **[Markdown Slides](./elementary/slides.md)** | **[PowerPoint Deck (.pptx)](./elementary/slides.pptx)**
  - Class 1: Introduction to Boolean Logic: TRUE, FALSE, NOT, AND, OR.
  - Class 2: Compound Boolean Expressions & Truth Tables.
  - Class 3: Introduction to Trees & Binary Search Trees.
  - Class 4: "What Does This Program Do?" (Logic Conditions) + Contest 3 Mock Test.
- **[Junior Division Curriculum (4 × 90 Mins)](./junior/README.md)**
  - Resources: **[Homework Sets & Solutions](./junior/homework.md)** | **[Markdown Slides](./junior/slides.md)** | **[PowerPoint Deck (.pptx)](./junior/slides.pptx)**
  - Class 1: Boolean Algebra Laws: De Morgan's, Distributive & Absorption.
  - Class 2: Boolean Expression Simplification & 3-Variable Truth Tables.
  - Class 3: Data Structures: Stacks, Queues & Binary Search Tree Traversals.
  - Class 4: "What Does This Program Do?" & Contest 3 Mock Exam.
- **[Intermediate Division Curriculum (4 × 90 Mins)](./intermediate/README.md)**
  - Resources: **[Homework Sets & Solutions](./intermediate/homework.md)** | **[Markdown Slides](./intermediate/slides.md)** | **[PowerPoint Deck (.pptx)](./intermediate/slides.pptx)**
  - Class 1: Advanced Boolean Minimization: 3 & 4-Variable Karnaugh Maps (K-Maps).
  - Class 2: Advanced Data Structures: Priority Queues, Internal/External Nodes & BST Properties.
  - Class 3: Intermediate Pseudocode Tracing (Recursive Trees & Stacks).
  - Class 4: Contest 3 Programming Challenge (BST Traversals & Logic Parsers) + Timed Mock Contest.

---

## 💡 Essential Boolean Laws Summary Sheet
- **De Morgan's Laws**:
  - $\overline{A \cdot B} = \overline{A} + \overline{B}$
  - $\overline{A + B} = \overline{A} \cdot \overline{B}$
- **Distributive Laws**:
  - $A \cdot (B + C) = (A \cdot B) + (A \cdot C)$
  - $A + (B \cdot C) = (A + B) \cdot (A + C)$ *(Very common ACSL trick!)*
- **Absorption Laws**:
  - $A + A \cdot B = A$
  - $A \cdot (A + B) = A$
  - $A + \overline{A} \cdot B = A + B$
- **Complement Laws**:
  - $A \cdot \overline{A} = 0$
  - $A + \overline{A} = 1$
