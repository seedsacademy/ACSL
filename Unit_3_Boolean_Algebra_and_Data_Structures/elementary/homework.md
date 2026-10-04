# Unit 3: Elementary Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 3 (Boolean Logic, Truth Tables, Binary Search Trees, and Pseudocode). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: NOT, AND, OR Truth Tables

### Section A: Concept Checks
1. If $A = 1$ (True) and $B = 0$ (False), evaluate:
   - (a) $\text{NOT } A$
   - (b) $A \text{ AND } B$
   - (c) $A \text{ OR } B$
2. In English, what does an AND statement require for the result to be True?
3. In English, what does an OR statement require for the result to be True?

### Section B: 2-Variable Truth Table Construction
4. Complete the truth table for $F = \text{NOT}(A) \text{ AND } B$:
   | $A$ | $B$ | $\text{NOT } A$ | $F$ |
   | :-: | :-: | :-: | :-: |
   | 0 | 0 | | |
   | 0 | 1 | | |
   | 1 | 0 | | |
   | 1 | 1 | | |

5. Complete the truth table for $G = A \text{ OR } \text{NOT}(B)$.

---

## 📝 Homework 2: Compound Boolean Expressions

### Section A: Evaluating with Given Values
Given $A = 1, B = 0, C = 1$, evaluate:
1. $A \cdot B + C$
2. $\overline{A} + B \cdot \overline{C}$
3. $(A + B) \cdot (B + C)$
4. $\overline{A + B} + \overline{C}$

### Section B: Counting True Combinations
5. For how many of the 4 combinations of $(A, B)$ is the expression $A + \overline{B}$ equal to 1?
6. For how many of the 8 combinations of $(A, B, C)$ is $(A \cdot B) + C$ equal to 1?

---

## 📝 Homework 3: Binary Search Tree (BST) Basics

### Section A: BST Definitions
1. In a tree diagram, what is the top node called?
2. What are nodes called that have no children?
3. If a new number is **smaller** than the current node in a BST, does it go to the left or right?

### Section B: Constructing BSTs
4. Insert the numbers `[40, 20, 60, 10, 30, 70]` into an empty BST in that order.
   - (a) What is the root?
   - (b) What is the left child of 40?
   - (c) List all the leaf nodes.
5. Insert the letters `[D, B, F, A, C, E, G]` into an empty BST.
   - (a) How many levels does this tree have (counting root as level 0)?
   - (b) What are the children of node B?

---

## 📝 Homework 4: Pseudocode & Contest 3 Mock Exam

### Section A: Pseudocode Tracing
1. What does the following program print?
   ```basic
   FLAG = 0
   FOR I = 1 TO 5
     IF I > 2 AND I < 5 THEN
       FLAG = FLAG + I
     END IF
   NEXT I
   PRINT FLAG
   ```

2. What does this program print?
   ```basic
   A = 12
   B = 18
   IF A > 10 OR B < 15 THEN
     C = A + B
   ELSE
     C = A * B
   END IF
   PRINT C \ 2
   ```

### Section B: Elementary Contest 3 Mock Set
3. If $A = 1, B = 1, C = 0$, evaluate $\overline{A \cdot B} + C$.
4. Insert `[50, 25, 75, 10, 30, 90]` into an empty BST. What is the value of the node with the largest value?
5. How many leaves are in the tree from Question 4?
6. For how many combinations of $(A, B)$ is $\overline{A} \cdot \overline{B} = 1$?

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. (a) 0, (b) 0, (c) 1.
2. Both inputs must be True.
3. At least one input must be True.
4. $F$ values: Row 0: 0, Row 1: 1, Row 2: 0, Row 3: 0.
5. $G$ values: Row 0: 1, Row 1: 0, Row 2: 1, Row 3: 1.

### Homework 2 Solutions
1. $1 \cdot 0 + 1 = 0 + 1 = \mathbf{1}$.
2. $0 + 0 \cdot 0 = \mathbf{0}$.
3. $(1 + 0) \cdot (0 + 1) = 1 \cdot 1 = \mathbf{1}$.
4. $\overline{1+0} + 0 = 0 + 0 = \mathbf{0}$.
5. Combinations: $(0,0) \rightarrow 1$; $(0,1) \rightarrow 0$; $(1,0) \rightarrow 1$; $(1,1) \rightarrow 1 \implies \mathbf{3 \text{ combinations}}$.
6. $C=1$ gives 4 combinations. When $C=0$, $A \cdot B = 1$ gives 1 combination $(1,1,0)$. Total $= 4 + 1 = \mathbf{5 \text{ combinations}}$.

### Homework 3 Solutions
1. Root.
2. Leaves (or leaf nodes).
3. Left.
4. (a) Root = **40**. (b) Left child of 40 = **20**. (c) Leaves = **10, 30, 70**.
5. (a) Levels: Level 0 (D), Level 1 (B, F), Level 2 (A, C, E, G) $\implies \mathbf{3 \text{ levels}}$ (Height 2). (b) Children of B = **A and C**.

### Homework 4 Solutions
1. $I > 2$ and $I < 5$ matches $I=3$ and $I=4$. `FLAG` $= 3 + 4 = \mathbf{7}$.
2. Condition: $12 > 10$ is True $\implies C = 12 + 18 = 30$. $30 \setminus 2 = \mathbf{15}$.
3. $\overline{1 \cdot 1} + 0 = \overline{1} + 0 = 0 + 0 = \mathbf{0}$.
4. Largest value is always the rightmost node $\implies \mathbf{90}$.
5. Leaves are nodes with no children: 10, 30, 90 $\implies \mathbf{3 \text{ leaves}}$.
6. Only when $A=0$ and $B=0 \implies \mathbf{1 \text{ combination}}$.
