# Unit 3: Intermediate Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 3 (Karnaugh Maps, Advanced Binary Tree Properties, Priority Queues / Heaps, Intermediate Pseudocode, and Contest Programming). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Karnaugh Maps (K-Maps) Minimization

### Section A: 3-Variable K-Maps
1. Minimize to Sum-of-Products (SOP) using a K-Map:
   $$F(A, B, C) = \sum m(0, 1, 4, 5, 6)$$
2. Minimize:
   $$G(A, B, C) = \sum m(1, 3, 5, 7)$$

### Section B: 4-Variable K-Maps
3. Minimize to minimal SOP:
   $$F(A, B, C, D) = \sum m(0, 2, 8, 10, 5, 7, 13, 15)$$
4. Minimize with "Don't Care" conditions ($d$):
   $$F(A, B, C, D) = \sum m(1, 3, 7, 11, 15) + d(0, 2, 5)$$

---

## 📝 Homework 2: Tree Formulas, BST Deletion & Heaps

### Section A: Tree Mathematical Theorems
1. In a strictly binary tree with 21 internal nodes, how many leaf (external) nodes are there?
2. If a binary tree has height $h = 4$ (root is level 0), what is the maximum number of nodes it can contain?
3. A complete binary tree has 63 nodes. What is its height?

### Section B: BST Deletion
4. Given the BST with keys `[50, 30, 70, 20, 40, 60, 80]`:
   - (a) Delete node 30 by replacing it with its **Inorder Successor**. What key replaces 30?
   - (b) What key would replace 30 if using its **Inorder Predecessor**?

### Section C: Binary Heaps (Priority Queues)
5. A Min-Heap is stored in an array: `[0, 10, 15, 30, 40, 50, 60, 70]`.
   - What is the parent of node 60?
   - What are the children of node 15?

---

## 📝 Homework 3: Intermediate Pseudocode Tracing

### Section A: Tree & Stack Simulation
1. What does the following program print?
   ```basic
   DIM VAL(7), L(7), R(7)
   DATA 0, 10, 20, 30, 40, 50, 60, 70
   DATA 0,  2,  4,  0,  0,  0,  0,  0
   DATA 0,  3,  5,  0,  0,  0,  0,  0
   FOR I = 1 TO 7 : READ VAL(I) : NEXT I
   FOR I = 1 TO 7 : READ L(I) : NEXT I
   FOR I = 1 TO 7 : READ R(I) : NEXT I
   
   FUNCTION COUNT_LEAVES(NODE)
     IF NODE = 0 THEN RETURN 0
     IF L(NODE) = 0 AND R(NODE) = 0 THEN RETURN 1
     RETURN COUNT_LEAVES(L(NODE)) + COUNT_LEAVES(R(NODE))
   END FUNCTION
   
   PRINT COUNT_LEAVES(1)
   ```

---

## 📝 Homework 4: Contest 3 Programming & Mock Exam

### Section A: Programming Blueprint
Implement a Python function `build_bst_and_inorder(values: list[int]) -> list[int]` that inserts values into a BST and returns its Inorder traversal.

### Section B: Intermediate Contest 3 Mock Set
1. Minimize using a 4-variable K-Map: $F(A, B, C, D) = \sum m(4, 5, 6, 7, 12, 13, 14, 15)$.
2. A binary tree has 35 total nodes where every node has either 0 or 2 children. How many internal nodes are there?
3. Find the Inorder Successor of 45 in the sequence: `[45, 20, 60, 10, 35, 55, 75, 50]`.
4. How many prime implicants are in the K-Map for $F(A, B, C) = \sum m(0, 2, 4, 6)$?

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. Group $m(0,1,4,5) \implies \overline{B}$. Group $m(4,6) \implies A \overline{C}$. Minimal SOP: $\mathbf{\overline{B} + A \overline{C}}$.
2. Group $m(1,3,5,7) \implies \mathbf{C}$.
3. Group corners $m(0,2,8,10) \implies \overline{B} \ \overline{D}$. Group center $m(5,7,13,15) \implies B D$. Minimal SOP: $\mathbf{\overline{B} \ \overline{D} + B D}$.
4. Including $d(0, 2, 5)$ allows forming an 8-cell group $m(0,1,2,3) + d + m(5,7) \dots$ Minimal: $\mathbf{\overline{A} + C D}$ (or $\overline{A} D + C D$).

### Homework 2 Solutions
1. For strictly binary trees: $L = I + 1 = 21 + 1 = \mathbf{22 \text{ leaves}}$.
2. Max nodes $= 2^{h+1} - 1 = 2^5 - 1 = \mathbf{31 \text{ nodes}}$.
3. $2^{h+1} - 1 = 63 \implies 2^{h+1} = 64 \implies h+1 = 6 \implies h = \mathbf{5}$.
4. (a) Inorder successor of 30 is smallest in its right subtree $\implies \mathbf{40}$.  
   (b) Inorder predecessor is largest in its left subtree $\implies \mathbf{20}$.
5. Node 60 is at index 6. Parent is at $\lfloor 6/2 \rfloor = 3 \implies$ Node 30.  
   Node 15 is at index 2. Children at $2(2)=4$ (Node 40) and $2(2)+1=5$ (Node 50).

### Homework 3 Solutions
1. Leaves are nodes where $L(i)=0$ and $R(i)=0$: Node 3, Node 4, Node 5. Total $= \mathbf{3}$.

### Homework 4 Solutions
1. Group covers rows $01$ and $11$ for all columns $\implies \mathbf{B}$.
2. Total $N = 2I + 1 \implies 35 = 2I + 1 \implies 2I = 34 \implies I = \mathbf{17 \text{ internal nodes}}$.
3. Right subtree of 45 has root 60, left child 55, left child 50 $\implies$ smallest in right subtree is $\mathbf{50}$.
4. Group covers all 4 corners of 3-variable map ($m_0, m_2, m_4, m_6$) $\implies$ 1 prime implicant ($\overline{C}$).
