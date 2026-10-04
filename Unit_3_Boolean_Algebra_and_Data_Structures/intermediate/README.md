# Unit 3: Intermediate Division (4 Classes × 90 Minutes)

This curriculum prepares high school competitors (Grades 10–12) for **ACSL Contest 3** at the Intermediate/Senior Division level, covering Karnaugh Maps (K-Maps), advanced binary tree properties, priority queues, intermediate pseudocode, and contest programming strategies.

---

## 📅 Class 1: Karnaugh Maps (K-Maps) & Boolean Minimization

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: Minterm notation ($\sum m(0, 1, 4, \dots)$) vs Maxterm notation ($\prod M(\dots)$).
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - The Gray Code sequence ($00, 01, 11, 10$) ensuring single-bit hamming distance between adjacent cells.
  - 3-Variable K-Map ($2 \times 4$) and 4-Variable K-Map ($4 \times 4$).
  - Grouping rules: Groups must be sizes of $2^k$ ($1, 2, 4, 8, 16$), rectangular, wrap around edges and four corners.
  - Handling "Don't Care" conditions ($d$ or $X$): include only if they enlarge groups.
- **0:45 – 0:70 (25 min)**: Guided Practice: Minimizing 4-variable expressions to minimal Sum-of-Products (SOP) and Product-of-Sums (POS).
- **0:70 – 0:85 (15 min)**: Timed Speed Challenge: 3 K-map minimization problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Construct 3-variable and 4-variable K-Maps with correct Gray Code coordinates.
2. Group adjacent 1s into maximal rectangular blocks of size $2^k$, including torus/wrap-around groups.
3. Extract the simplified minimal SOP equation by identifying invariant variables.

### 📘 Core Content & Worked Examples

#### Example: 4-Variable K-Map Minimization
Minimize: $F(A, B, C, D) = \sum m(0, 2, 5, 7, 8, 10, 13, 15)$.

#### K-Map Grid ($AB$ rows, $CD$ columns):
```text
           CD
       00  01  11  10
    +-----------------
 00 |  1   0   0   1   (m0, m2)
AB   |
 01 |  0   1   1   0   (m5, m7)
 11 |  0   1   1   0   (m13, m15)
 10 |  1   0   0   1   (m8, m10)
```

#### Grouping Analysis:
1. **Group 1 (The Four Corners)**:
   - Cells: $m_0 (0000), m_2 (0010), m_8 (1000), m_{10} (1010)$.
   - Row comparison: $AB = 00$ and $10 \implies B$ is constant $0$ ($\overline{B}$).
   - Column comparison: $CD = 00$ and $10 \implies D$ is constant $0$ ($\overline{D}$).
   - Term: **$\overline{B} \cdot \overline{D}$**.
2. **Group 2 (The Center $2 \times 2$ Block)**:
   - Cells: $m_5 (0101), m_7 (0111), m_{13} (1101), m_{15} (1111)$.
   - Row comparison: $AB = 01$ and $11 \implies B$ is constant $1$ ($B$).
   - Column comparison: $CD = 01$ and $11 \implies D$ is constant $1$ ($D$).
   - Term: **$B \cdot D$**.
- Minimal SOP: **$F = \overline{B} \ \overline{D} + B \ D$** (which is also $B \odot D$ or $\overline{B \oplus D}$!).

---

## 📅 Class 2: Advanced Data Structures (Binary Trees & Priority Queues)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Tree terminology review (height, depth, internal vs external).
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Mathematical Properties of Binary Trees:
    - In any full binary tree (every node has 0 or 2 children): $L = I + 1$ (Leaves = Internals + 1).
    - Maximum nodes at level $k$ is $2^k$; Maximum nodes in tree of height $h$ is $2^{h+1}-1$.
  - BST Node Deletion:
    - Case 1: Leaf node (simply remove).
    - Case 2: One child (bypass node).
    - Case 3: Two children (replace with inorder predecessor or inorder successor).
  - Priority Queues & Binary Heaps:
    - Min-Heap and Max-Heap property.
    - Array representation: Root at index 1, left child at $2i$, right child at $2i+1$, parent at $\lfloor i/2 \rfloor$.
- **0:45 – 0:70 (25 min)**: Guided Practice: Simulating BST deletion and Heap insertions/extractions.
- **0:70 – 0:85 (15 min)**: Timed Contest Drill: 3 problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Calculate the exact number of internal and external nodes using tree formulas.
2. Delete nodes from a BST and draw the resulting valid BST structure.
3. Map binary trees and heaps to 1D arrays and compute index offsets.

### 📘 Core Content & Worked Examples

#### Example: BST Node Deletion
Given the BST with elements `[50, 30, 70, 20, 40, 60, 80]`:
Delete node `50` (the root) by replacing it with its **Inorder Successor**.
- Step 1: Find Inorder Successor (smallest node in the right subtree):
  - Right subtree is rooted at 70. Go left: node 60.
  - Inorder Successor = **60**.
- Step 2: Replace value 50 with 60.
- Step 3: Remove the original node 60 from its position.
- Resulting Tree:
```text
         60
       /    \
     30      70
    /  \       \
   20   40      80
```

---

## 📅 Class 3: "What Does This Program Do?" (Intermediate Level)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick recursive tree traversal function.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Simulating trees and linked lists using parallel arrays (`LEFT(i)`, `RIGHT(i)`, `VAL(i)`).
  - Recursive depth-first search (DFS) pseudocode tracing.
  - Two-dimensional matrix manipulation.
- **0:45 – 0:70 (25 min)**: Guided Practice: Tracing a 20-line recursive array traversal.
- **0:70 – 0:85 (15 min)**: In-Class Contest Simulation: 2 challenging pseudocode traces.
- **0:85 – 0:90 (5 min)**: Wrap-up & Q&A.

### 📘 Pseudocode Tracing Example (Tree Traversal via Arrays)

```basic
DIM V(7), L(7), R(7)
' Tree encoded: V is value, L is left child index, R is right child index
V = [0, 50, 25, 75, 10, 30, 60, 90]
L = [0,  2,  4,  6,  0,  0,  0,  0]
R = [0,  3,  5,  7,  0,  0,  0,  0]

FUNCTION TRAVERSE(N)
  IF N = 0 THEN RETURN 0
  IF L(N) = 0 AND R(N) = 0 THEN
    RETURN V(N)
  ELSE
    RETURN TRAVERSE(L(N)) + TRAVERSE(R(N))
  END IF
END FUNCTION

PRINT TRAVERSE(1)
```
- Analysis:
  - This function checks if node $N$ is a leaf (`L(N) == 0 AND R(N) == 0`).
  - If it is a leaf, it returns the value of the leaf.
  - Otherwise, it recursively sums the leaf values of the left and right subtrees!
  - Leaves in this tree are:
    - Node 4: Value 10
    - Node 5: Value 30
    - Node 6: Value 60
    - Node 7: Value 90
- Sum of leaves: $10 + 30 + 60 + 90 = \mathbf{190}$.

---

## 📅 Class 4: Contest 3 Programming Challenge & Mock Contest

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick tree building algorithm.
- **0:15 – 0:45 (30 min)**: Contest Programming Deep Dive:
  - Contest 3 typical problems: "Binary Search Tree Reconstruction", "Expression Tree Evaluation", "Boolean Logic Minimizer".
  - Object-Oriented Node definitions vs. Array-based trees in Python/Java.
- **0:45 – 0:75 (30 min)**: **Full Timed ACSL Contest 3 Mock Exam (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Score debrief, answer key walk-through, and celebration.

### 💻 Contest 3 Programming Blueprint (Binary Search Tree in Python)

```python
class Node:
    def __init__(self, val):
        self.val = val
        self.left = None
        self.right = None

def insert(root, val):
    if not root:
        return Node(val)
    if val <= root.val:
        root.left = insert(root.left, val)
    else:
        root.right = insert(root.right, val)
    return root

def get_leaves(root):
    if not root:
        return []
    if not root.left and not root.right:
        return [root.val]
    return get_leaves(root.left) + get_leaves(root.right)
```

---

### 🏆 Unit 3 Intermediate Division Mock Contest
1. Minimize the boolean function using a K-Map: $F(A, B, C) = \sum m(1, 3, 4, 5, 7)$. (*Answer: $C + A \overline{B}$*)
2. In a strictly binary tree with 14 internal nodes, how many leaf (external) nodes are there? (*Answer: $L = I + 1 = 14 + 1 = 15$*)
3. A Max-Heap is stored in an array: `[0, 90, 70, 80, 40, 50, 60, 30]`. What is the value of the right child of node 70? (*Answer: Node 70 is at index 2. Right child is at $2i+1 = 5 \implies$ Value is 50*)
4. Insert elements `[40, 20, 60, 10, 30, 50, 70]` into a BST, then delete node 20 using its **inorder successor**. What is the new left child of 40? (*Answer: 30*)
5. What does the following program print?
   ```basic
   S = 0
   FOR I = 1 TO 3
     FOR J = 1 TO 3
       IF I <> J THEN
         S = S + (I * J)
       END IF
     NEXT J
   NEXT I
   PRINT S
   ```
   (*Answer: Total sum of all pairs minus diagonal: Total = $(1+2+3)(1+2+3) = 36$. Diagonal $I=J$: $1^2+2^2+3^2 = 14 \implies 36 - 14 = 22$*)
