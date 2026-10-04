# Unit 3: Junior Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 3 (Boolean Algebra Laws, Simplification, Stacks, Queues, Binary Search Trees, and Pseudocode). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Boolean Laws & De Morgan's

### Section A: Law Identification
1. Name the Boolean law demonstrated:
   - (a) $A + B = B + A$
   - (b) $A \cdot (B + C) = A B + A C$
   - (c) $A + A B = A$
   - (d) $\overline{A \cdot B} = \overline{A} + \overline{B}$
   - (e) $A + \overline{A} B = A + B$

### Section B: Applying De Morgan's Laws
2. Expand and simplify: $\overline{A + \overline{B \cdot C}}$
3. Expand and simplify: $\overline{\overline{X} \cdot Y + Z}$
4. Simplify: $\overline{\overline{A + B} \cdot \overline{A + C}}$

---

## 📝 Homework 2: Boolean Simplification & Truth Sets

### Section A: Algebraic Reduction
1. Simplify to minimal literals: $A B C + A B \overline{C} + A \overline{B} C + \overline{A} B C$.
2. Simplify: $(X + Y)(X + \overline{Y})(\overline{X} + Z)$.
3. Simplify: $A \overline{B} + A B + \overline{A} B$.

### Section B: Counting Ordered Triples
4. How many ordered triples $(A, B, C)$ make $F = (A + B) \cdot (\overline{B} + C)$ equal to 1?
5. How many ordered triples $(A, B, C)$ make $G = \overline{A} \cdot B \cdot \overline{C} + A \cdot \overline{B} \cdot C$ equal to 0?

---

## 📝 Homework 3: Stacks, Queues & BST Traversals

### Section A: Stacks (LIFO) & Queues (FIFO)
1. A stack is initially empty. Execute: `PUSH(5)`, `PUSH(8)`, `POP()`, `PUSH(3)`, `PUSH(7)`, `POP()`, `POP()`. What value remains on the stack?
2. A queue is initially empty. Execute: `ENQUEUE(10)`, `ENQUEUE(20)`, `DEQUEUE()`, `ENQUEUE(30)`, `ENQUEUE(40)`, `DEQUEUE()`. What is at the front of the queue?

### Section B: Binary Search Tree Traversals
3. Insert the letters `[F, B, H, A, D, G, I, C, E]` into an empty BST in that order.
   - (a) What is the Inorder traversal?
   - (b) What is the Preorder traversal?
   - (c) What is the Postorder traversal?
4. How many leaves are in the tree from Question 3?

---

## 📝 Homework 4: Junior Pseudocode & Contest 3 Mock Exam

### Section A: Pseudocode Tracing
1. What does the following program print?
   ```basic
   DIM S(10)
   TOP = 0
   DATA 3, 5, 2, -1, 4, -1, 9, -1
   FOR I = 1 TO 8
     READ X
     IF X > 0 THEN
       TOP = TOP + 1
       S(TOP) = X
     ELSE
       TOP = TOP - 1
     END IF
   NEXT I
   PRINT S(TOP)
   ```

### Section B: Junior Contest 3 Mock Set
2. Simplify the Boolean expression: $\overline{\overline{A} + B} + \overline{A + B}$.
3. How many ordered triples $(A, B, C)$ make $A \cdot (B + \overline{C}) = 1$?
4. What is the height of a BST created from inserting `[10, 20, 30, 40, 50]`?
5. For the BST with keys `[30, 15, 50, 10, 20, 40, 60]`, write the Postorder traversal sequence.

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. (a) Commutative, (b) Distributive, (c) Absorption, (d) De Morgan's, (e) Absorption.
2. $\overline{A} \cdot \overline{\overline{B \cdot C}} = \overline{A} \cdot (B \cdot C) = \mathbf{\overline{A} B C}$.
3. $\overline{\overline{X} \cdot Y} \cdot \overline{Z} = (X + \overline{Y}) \cdot \overline{Z} = \mathbf{X \overline{Z} + \overline{Y} \overline{Z}}$.
4. By De Morgan's on the outer product: $\overline{\overline{A+B}} + \overline{\overline{A+C}} = (A + B) + (A + C) = \mathbf{A + B + C}$.

### Homework 2 Solutions
1. $A B (C + \overline{C}) + C(A \overline{B} + \overline{A} B) = A B + A \overline{B} C + \overline{A} B C = A(B + \overline{B} C) + \overline{A} B C = A(B + C) + \overline{A} B C = A B + A C + B C$.
2. $(X + Y)(X + \overline{Y}) = X + Y \overline{Y} = X$. Then $X \cdot (\overline{X} + Z) = X \overline{X} + X Z = \mathbf{X Z}$.
3. $A(\overline{B} + B) + \overline{A} B = A + \overline{A} B = \mathbf{A + B}$.
4. Truth set analysis:
   - When $B=0$: $(A + 0) \cdot (1 + C) = A \cdot 1 = A$. Requires $A=1$. $C$ can be 0 or 1 $\implies (1, 0, 0), (1, 0, 1)$ (2 triples).
   - When $B=1$: $(A + 1) \cdot (0 + C) = 1 \cdot C = C$. Requires $C=1$. $A$ can be 0 or 1 $\implies (0, 1, 1), (1, 1, 1)$ (2 triples).
   - Total $= 2 + 2 = \mathbf{4 \text{ triples}}$.
5. $G = 1$ for exactly 2 triples: $(0, 1, 0)$ and $(1, 0, 1)$.
   Total triples $= 2^3 = 8 \implies G = 0$ for $8 - 2 = \mathbf{6 \text{ triples}}$.

### Homework 3 Solutions
1. Operations: Push 5 $\rightarrow [5]$; Push 8 $\rightarrow [5, 8]$; Pop $\rightarrow [5]$; Push 3 $\rightarrow [5, 3]$; Push 7 $\rightarrow [5, 3, 7]$; Pop $\rightarrow [5, 3]$; Pop $\rightarrow [5]$. Remaining: **5**.
2. Operations: Enq 10 $\rightarrow [10]$; Enq 20 $\rightarrow [10, 20]$; Deq $\rightarrow [20]$; Enq 30 $\rightarrow [20, 30]$; Enq 40 $\rightarrow [20, 30, 40]$; Deq $\rightarrow [30, 40]$. Front is **30**.
3. (a) Inorder is always sorted: **`A, B, C, D, E, F, G, H, I`**.  
   (b) Preorder: **`F, B, A, D, C, E, H, G, I`**.  
   (c) Postorder: **`A, C, E, D, B, G, I, H, F`**.
4. Leaves are nodes with no children: A, C, E, G, I $\implies \mathbf{5 \text{ leaves}}$.

### Homework 4 Solutions
1. Pushes 3, 5, 2 $\implies [3, 5, 2]$. Pop $\implies [3, 5]$. Push 4 $\implies [3, 5, 4]$. Pop $\implies [3, 5]$. Push 9 $\implies [3, 5, 9]$. Pop $\implies [3, 5]$. `S(TOP)` is **5**.
2. $\overline{\overline{A}+B} = A \overline{B}$. $\overline{A+B} = \overline{A} \overline{B}$. $A \overline{B} + \overline{A} \overline{B} = (A + \overline{A}) \overline{B} = \mathbf{\overline{B}}$.
3. $A$ must be 1. $(B + \overline{C})$ is 1 for 3 pairs of $(B, C)$: $(1, 0), (1, 1), (0, 0)$. Triples: $\mathbf{3}$.
4. All nodes go to the right (degenerate linked list). Height = $\mathbf{4}$ (or 5 levels).
5. Postorder: **`10, 20, 15, 40, 60, 50, 30`**.
