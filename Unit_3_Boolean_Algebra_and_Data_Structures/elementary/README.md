# Unit 3: Elementary Division (4 Classes × 90 Minutes)

This curriculum prepares elementary students (Grades 3–6) for **ACSL Contest 3** (Boolean Logic, Simple Trees, and "What Does This Program Do?").

---

## 📅 Class 1: Introduction to Boolean Logic (NOT, AND, OR)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: True or False questions from daily life. Introduction of George Boole.
- **0:15 – 0:45 (30 min)**: Core Concept: The 3 fundamental operators:
  - $\text{NOT}$ ($\sim$ or overline): Flips True $\leftrightarrow$ False.
  - $\text{AND}$ ($\cdot$ or $\land$): Only True if BOTH are True.
  - $\text{OR}$ ($+$ or $\lor$): True if AT LEAST ONE is True.
- **0:45 – 0:70 (25 min)**: Guided Practice: Filling out 2-variable Truth Tables.
- **0:70 – 0:85 (15 min)**: Timed Game: "Human Truth Table" or rapid-response cards.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Define the truth values for `NOT`, `AND`, and `OR`.
2. Construct and complete 2-variable truth tables (4 rows).
3. Evaluate statements like: If $A = 1$ and $B = 0$, what is $A \cdot B$?

### 📘 Truth Table Reference:
| $A$ | $B$ | $\text{NOT } A$ | $A \text{ AND } B$ ($A \cdot B$) | $A \text{ OR } B$ ($A + B$) |
| :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 1 |
| 1 | 1 | 0 | 1 | 1 |

### 📝 In-Class Exercises
1. If $A = \text{TRUE}$ and $B = \text{FALSE}$, evaluate $\text{NOT}(A) \text{ OR } B$. (*Answer*: $\text{FALSE} + \text{FALSE} = \text{FALSE} = 0$).
2. If $X = 1, Y = 1, Z = 0$, what is $X \cdot Y \cdot Z$? (*Answer*: $1 \cdot 1 \cdot 0 = 0$).
3. Which operator is like multiplying? (*Answer*: AND, because $1 \times 1 = 1$, $1 \times 0 = 0$).

---

## 📅 Class 2: Compound Boolean Expressions & Truth Tables

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: 5 rapid boolean flashcards.
- **0:15 – 0:45 (30 min)**: Core Concept: Compound expressions and Operator Precedence:
  1. Parentheses `(...)`
  2. $\text{NOT}$
  3. $\text{AND}$ ($\cdot$)
  4. $\text{OR}$ ($+$)
- **0:45 – 0:70 (25 min)**: Guided Practice: Building full truth tables for expressions like $\overline{A} \cdot B + A \cdot \overline{B}$.
- **0:70 – 0:85 (15 min)**: In-Class Contest Simulation: 4 boolean evaluation questions.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Apply the precedence rule: $\text{NOT} > \text{AND} > \text{OR}$.
2. Determine how many rows are in a truth table ($2^n$ where $n$ is number of variables).
3. Count how many combinations make an expression TRUE (1).

### 📘 Worked Example: Build Truth Table for $F = \overline{A} \cdot B + A \cdot B$
- Step 1: List all 4 combinations of $A$ and $B$:
- Step 2: Calculate sub-columns:

| $A$ | $B$ | $\overline{A}$ | $\overline{A} \cdot B$ | $A \cdot B$ | $F = \overline{A} \cdot B + A \cdot B$ |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 1 | 0 | 0 | **0** |
| 0 | 1 | 1 | 1 | 0 | **1** |
| 1 | 0 | 0 | 0 | 0 | **0** |
| 1 | 1 | 0 | 0 | 1 | **1** |

*Notice*: The column for $F$ is identical to $B$! Thus $\overline{A} \cdot B + A \cdot B = B$.

---

## 📅 Class 3: Introduction to Trees & Binary Search Trees

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Family tree diagramming.
- **0:15 – 0:45 (30 min)**: Core Concept: What is a Tree?
  - Root node, Parent, Child, Leaf node (no children).
  - **Binary Search Tree (BST) Rule**:
    - Numbers/letters **smaller** than current node go to the **LEFT**.
    - Numbers/letters **larger** than current node go to the **RIGHT**.
- **0:45 – 0:70 (25 min)**: Guided Practice: Inserting lists of numbers and letters into a BST step by step.
- **0:70 – 0:85 (15 min)**: Timed Tree Building Drill: Draw the BST for given sequences.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Identify the Root, Leaves, and Height of a binary tree.
2. Insert a list of numbers or words into a Binary Search Tree in given order.
3. Count how many leaves or nodes are at each level.

### 📘 Worked Example: Build BST for Sequence: [50, 30, 70, 20, 40, 80]
- Step 1: **50** is the Root.
- Step 2: **30** $< 50 \implies$ left child of 50.
- Step 3: **70** $> 50 \implies$ right child of 50.
- Step 4: **20** $< 50 \rightarrow < 30 \implies$ left child of 30.
- Step 5: **40** $< 50 \rightarrow > 30 \implies$ right child of 30.
- Step 6: **80** $> 50 \rightarrow > 70 \implies$ right child of 70.

```text
       50
     /    \
   30      70
  /  \       \
 20   40      80
```
- **Root**: 50
- **Leaves** (nodes with no children): 20, 40, 80 (Total = 3 leaves).
- **Depth/Level of 40**: Level 2 (Root is level 0).

---

## 📅 Class 4: "What Does This Program Do?" & Contest 3 Mock Test

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Rapid BST insertion challenge.
- **0:15 – 0:45 (30 min)**: Pseudocode Focus: Nested `IF-THEN` statements and boolean flag variables.
- **0:45 – 0:75 (30 min)**: **Full Timed Contest 3 Mock Test (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Detailed review and celebration!

### 📘 Pseudocode Tracing Example

```basic
A = 10
B = 20
C = 15
FLAG = 0
IF (A < B) AND (C > A) THEN
  FLAG = 1
  A = A + 5
END IF
IF (B > C) AND (FLAG = 1) THEN
  C = C + A
END IF
PRINT C
```
- Line 5: $(10 < 20)$ is TRUE, $(15 > 10)$ is TRUE $\implies$ Condition TRUE.
- Line 6: `FLAG` becomes 1. `A` becomes $10 + 5 = 15$.
- Line 9: $(20 > 15)$ is TRUE, $(1 = 1)$ is TRUE $\implies$ Condition TRUE.
- Line 10: $C$ becomes $15 + 15 = 30$.
- Output: **30**.

---

### 🏆 Unit 3 Mock Contest (Elementary Division)
1. For $A=1, B=0, C=1$, evaluate: $\overline{A} + B \cdot C$. (*Answer: $0 + 0 \cdot 1 = 0$*)
2. How many combinations of $A, B, C$ make $(A + B) \cdot \overline{C}$ equal to 1? (*Answer: 3 combinations: (1,0,0), (0,1,0), (1,1,0)*)
3. Insert the letters `[M, G, T, B, H, Z]` into an empty BST in that order. What letter is the root? (*Answer: M*)
4. In the BST created in Question 3, what are the leaves? (*Answer: B, H, Z*)
5. What does the following program print?
   ```basic
   COUNT = 0
   FOR I = 1 TO 10
     IF (I MOD 2 = 0) OR (I MOD 3 = 0) THEN
       COUNT = COUNT + 1
     END IF
   NEXT I
   PRINT COUNT
   ```
   (*Answer: Multiples of 2 or 3 in 1..10 are: 2, 3, 4, 6, 8, 9, 10 $\implies$ Count = 7*)
