# Unit 3: Junior Division (4 Classes × 90 Minutes)

This curriculum prepares middle school students (Grades 7–9) for **ACSL Contest 3** (Boolean Algebra, Data Structures: Stacks, Queues, Binary Search Trees, and "What Does This Program Do?").

---

## 📅 Class 1: Boolean Algebra Laws & De Morgan's Theorems

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: 2-variable truth table review.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - The Axioms and Fundamental Laws of Boolean Algebra.
  - De Morgan's Laws: $\overline{A \cdot B} = \overline{A} + \overline{B}$ and $\overline{A + B} = \overline{A} \cdot \overline{B}$.
  - The Second Distributive Law: $A + B C = (A + B)(A + C)$ (The secret weapon of ACSL).
  - Absorption Laws: $A + A B = A$ and $A(A + B) = A$ and $A + \overline{A} B = A + B$.
- **0:45 – 0:70 (25 min)**: Guided Practice: Step-by-step algebraic simplification.
- **0:70 – 0:85 (15 min)**: Timed Speed Challenge: 4 simplification problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Memorize and instantly spot opportunities to apply De Morgan's and Absorption laws.
2. Reduce expressions with 3 or 4 variables to minimal literal count.
3. Verify algebraic simplifications using truth table rows.

### 📘 Core Content & Worked Examples

#### Example 1: Simplifying with De Morgan's & Absorption
Simplify: $F = \overline{A + \overline{B}} + \overline{\overline{A} \cdot B}$
- Step 1: Apply De Morgan's to first term:
  $$\overline{A + \overline{B}} = \overline{A} \cdot \overline{\overline{B}} = \overline{A} \cdot B$$
- Step 2: Apply De Morgan's to second term:
  $$\overline{\overline{A} \cdot B} = \overline{\overline{A}} + \overline{B} = A + \overline{B}$$
- Step 3: Combine terms:
  $$F = \overline{A} \cdot B + A + \overline{B}$$
- Step 4: Regroup: $(A + \overline{A} \cdot B) + \overline{B}$.
  - Using Absorption ($A + \overline{A} B = A + B$):
  $$F = (A + B) + \overline{B} = A + (B + \overline{B})$$
  - Since $B + \overline{B} = 1$:
  $$F = A + 1 = \mathbf{1}.$$

#### Example 2: Distributive Law in Reverse (Factoring)
Simplify: $A B C + A B \overline{C} + A \overline{B} C$
- Factor $A B$ out of first two terms:
  $$A B (C + \overline{C}) + A \overline{B} C = A B (1) + A \overline{B} C = A B + A \overline{B} C$$
- Factor $A$ out:
  $$A (B + \overline{B} C)$$
- Apply Absorption $B + \overline{B} C = B + C$:
  $$A (B + C) = \mathbf{A B + A C}.$$

### 📝 In-Class Exercises
1. Simplify: $(A + B)(A + \overline{B})$. (*Answer*: $A + B \overline{B} = A + 0 = A$).
2. Simplify: $\overline{\overline{X + Y} + \overline{X + Z}}$. (*Answer*: $(X + Y) \cdot (X + Z) = X + Y Z$).

---

## 📅 Class 2: Boolean Expression Simplification & 3-Variable Truth Tables

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Rapid De Morgan's expansion quiz.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - 3-variable truth table construction ($2^3 = 8$ rows in standard order: $000, 001, \dots, 111$).
  - Proving two expressions are equivalent using truth tables.
  - Finding the number of ordered triples $(A, B, C)$ for which an expression is TRUE or FALSE.
- **0:45 – 0:70 (25 min)**: Guided Practice: Solving "For how many ordered pairs/triples..." contest questions.
- **0:70 – 0:85 (15 min)**: Timed Contest Drill: 3 problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Construct 8-row truth tables rapidly without misaligned rows.
2. Determine truth set sizes without drawing the whole table when shortcuts apply.
3. Identify dual expressions and canonical forms.

### 📘 Core Content & Worked Examples

#### Example: How many ordered triples $(A, B, C)$ make $F = (A + \overline{B}) \cdot (B + C)$ FALSE (0)?
- Shortcut: An AND product is 0 whenever **at least one** factor is 0.
- Factor 1: $(A + \overline{B}) = 0 \iff A = 0 \text{ and } B = 1$.
  - Triples where $(A=0, B=1)$:
    - $(0, 1, 0) \implies F = 0 \cdot (1) = 0$.
    - $(0, 1, 1) \implies F = 0 \cdot (1) = 0$.
    (2 triples from Factor 1).
- Factor 2: $(B + C) = 0 \iff B = 0 \text{ and } C = 0$.
  - Triples where $(B=0, C=0)$:
    - $(0, 0, 0) \implies F = (0 + 1) \cdot (0 + 0) = 1 \cdot 0 = 0$.
    - $(1, 0, 0) \implies F = (1 + 1) \cdot (0 + 0) = 1 \cdot 0 = 0$.
    (2 triples from Factor 2).
- Check overlap: Can $B=1$ and $B=0$ simultaneously? No! Overlap is empty.
- Total triples making $F = 0$: $2 + 2 = \mathbf{4}$ triples.

---

## 📅 Class 3: Data Structures (Stacks, Queues, BST Traversals)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Cafeteria tray stack (LIFO) vs. Grocery store checkout line (FIFO).
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - **Stack**: `PUSH(x)` adds to top, `POP()` removes from top (LIFO - Last In, First Out).
  - **Queue**: `ENQUEUE(x)` / `PUSH(x)` adds to rear, `DEQUEUE()` / `POP()` removes from front (FIFO - First In, First Out).
  - **Binary Search Tree (BST)**:
    - Nodes inserted sequentially: Left $<$ Root $\le$ Right.
    - **Inorder Traversal** (Left, Root, Right) $\rightarrow$ *ALWAYS yields sorted order!*
    - **Preorder Traversal** (Root, Left, Right).
    - **Postorder Traversal** (Left, Right, Root).
- **0:45 – 0:70 (25 min)**: Guided Practice: Simulating a sequence of stack/queue operations and traversing a 7-node BST.
- **0:70 – 0:85 (15 min)**: Timed Data Structures Sprint: 4 contest problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Trace stack and queue contents after an interleaved sequence of pushes and pops.
2. Construct a BST from an arbitrary sequence of numbers or letters.
3. Write the exact Inorder, Preorder, and Postorder traversal sequences.

### 📘 Core Content & Worked Examples

#### Example: BST Insertion & Traversals
Insert the letters: `[F, B, G, A, D, I, C, E]` into an empty BST.

```text
         F
       /   \
      B     G
     / \     \
    A   D     I
       / \
      C   E
```

#### Traversal Derivations:
- **Inorder (L - Root - R)**:
  - Visit left subtree of F (rooted at B):
    - Subtree B: Left is A, Root is B, Right is D.
    - Subtree D: Left is C, Root is D, Right is E $\implies$ `C, D, E`.
    - Subtree B traversal: `A, B, C, D, E`.
  - Visit Root: `F`.
  - Visit right subtree of F (rooted at G):
    - Root is G, Right is I $\implies$ `G, I`.
  - Complete Inorder: **`A, B, C, D, E, F, G, I`** (Alphabetical order!).
- **Preorder (Root - L - R)**:
  - Root `F` $\rightarrow$ Left subtree rooted at `B`:
    - `B` $\rightarrow$ Left `A` $\rightarrow$ Right subtree rooted at `D`:
      - `D` $\rightarrow$ Left `C` $\rightarrow$ Right `E`.
  - Right subtree rooted at `G`:
    - `G` $\rightarrow$ Right `I`.
  - Complete Preorder: **`F, B, A, D, C, E, G, I`**.
- **Postorder (L - R - Root)**:
  - Complete Postorder: **`A, C, E, D, B, I, G, F`**.

---

## 📅 Class 4: "What Does This Program Do?" & Contest 3 Mock Exam

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick BST height & traversal check.
- **0:15 – 0:45 (30 min)**: Pseudocode Focus: Stack / Queue array simulation, pointer updates (`TOP = TOP + 1`, `HEAD = HEAD + 1`).
- **0:45 – 0:75 (30 min)**: **Full Timed ACSL Contest 3 Mock Exam (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Complete post-contest review and test strategies.

### 📘 Stack Simulation Pseudocode Example

```basic
DIM STACK(10)
TOP = 0
DATA 4, 7, 2, -1, 5, -1, -1, 9
FOR I = 1 TO 8
  READ X
  IF X > 0 THEN
    TOP = TOP + 1
    STACK(TOP) = X
  ELSE
    TOP = TOP - 1
  END IF
NEXT I
PRINT STACK(TOP)
```
- Step-by-step Stack states:
  - Read 4: Push 4 $\implies [4]$, `TOP = 1`
  - Read 7: Push 7 $\implies [4, 7]$, `TOP = 2`
  - Read 2: Push 2 $\implies [4, 7, 2]$, `TOP = 3`
  - Read -1: Pop $\implies [4, 7]$, `TOP = 2`
  - Read 5: Push 5 $\implies [4, 7, 5]$, `TOP = 3`
  - Read -1: Pop $\implies [4, 7]$, `TOP = 2`
  - Read -1: Pop $\implies [4]$, `TOP = 1`
  - Read 9: Push 9 $\implies [4, 9]$, `TOP = 2`
- Final Output `STACK(TOP)` = **9**.

---

### 🏆 Unit 3 Junior Division Mock Contest
1. Simplify the boolean expression: $\overline{A} \cdot B + \overline{A + \overline{B}}$. (*Answer: $\overline{A} \cdot B + \overline{A} \cdot B = \overline{A} \cdot B$*)
2. How many ordered pairs $(A, B)$ make $(A + B) \cdot (\overline{A} + \overline{B}) = 1$? (*Answer: 2 pairs: (1,0) and (0,1) — this is XOR!*)
3. Letters `[C, O, M, P, U, T, E, R]` are inserted into an empty BST in this order. List the nodes in the left subtree of the root. (*Answer: Root is C. Letters $< C$: none! Left subtree is empty.*)
4. For the BST inserted with numbers `[45, 20, 60, 10, 30, 50, 75, 25]`, what is the Preorder traversal? (*Answer: 45, 20, 10, 30, 25, 60, 50, 75*)
5. What does the following program print?
   ```basic
   A = 1
   B = 1
   FOR I = 1 TO 4
     C = A + B
     A = B
     B = C
   NEXT I
   PRINT C
   ```
   (*Answer: Fibonacci generator: Initial A=1, B=1. I=1: C=2, A=1, B=2. I=2: C=3, A=2, B=3. I=3: C=5, A=3, B=5. I=4: C=8, A=5, B=8. Output: 8*)
