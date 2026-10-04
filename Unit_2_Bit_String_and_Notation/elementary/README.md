# Unit 2: Elementary Division (4 Classes × 90 Minutes)

This curriculum prepares elementary students (Grades 3–6) for **ACSL Contest 2** (Prefix / Postfix Expressions and "What Does This Program Do?").

---

## 📅 Class 1: Introduction to Prefix and Postfix Notation

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Arithmetic order of operations (PEMDAS) review. Why do regular expressions need parentheses?
- **0:15 – 0:45 (30 min)**: Core Concept: Infix vs. Prefix (Polish) vs. Postfix (Reverse Polish). Where does the operator live?
- **0:45 – 0:70 (25 min)**: Guided Practice: Simple 3-token expressions ($+ \ 3 \ 4$ vs. $3 \ 4 \ +$ vs. $3 + 4$).
- **0:70 – 0:85 (15 min)**: In-Class Matching Game: Matching Infix expressions with their Prefix and Postfix pairs.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework assignment.

### 🎯 Learning Objectives
1. Understand the 3 notation styles:
   - **Infix**: Operator between operands ($A + B$)
   - **Prefix**: Operator before operands ($+ \ A \ B$)
   - **Postfix**: Operator after operands ($A \ B \ +$)
2. Recognize that Prefix and Postfix **never need parentheses**!
3. Evaluate simple single-operation Prefix and Postfix expressions.

### 📘 Core Content & Worked Examples

#### The Three Notations:
| Notation | Position of Operator | Example | Calculation |
| :--- | :--- | :--- | :--- |
| **Infix** | In the middle | $8 - 3$ | $8 - 3 = 5$ |
| **Prefix** | In the front | $- \ 8 \ 3$ | $8 - 3 = 5$ |
| **Postfix** | At the back | $8 \ 3 \ -$ | $8 - 3 = 5$ |

> ⚠️ **Critical Trap for Beginners**:
> In subtraction and division, order matters!
> $- \ 8 \ 3$ means $8 - 3 = 5$ (First number minus second number).
> $/ \ 12 \ 4$ means $12 / 4 = 3$.
> In Postfix: $8 \ 3 \ -$ means $8 - 3 = 5$, NOT $3 - 8$!

### 📝 In-Class Exercises
1. What is the value of the prefix expression $+ \ 7 \ 9$? (*Answer*: 16)
2. What is the value of the postfix expression $15 \ 3 \ /$? (*Answer*: $15 / 3 = 5$)
3. What is the value of the postfix expression $4 \ 2 \ \text{ \textasciicircum } $? (*Answer*: $4^2 = 16$)

### 🏠 Homework Assignment
- Evaluate: (a) $- \ 20 \ 8$, (b) $* \ 6 \ 7$, (c) $18 \ 6 \ -$, (d) $9 \ 3 \ /$.
- Write in Postfix: (a) $5 + 2$, (b) $10 \times 4$, (c) $7 - 3$.

---

## 📅 Class 2: Evaluating Compound Prefix & Postfix Expressions

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: 5 rapid single-operator prefix/postfix flashcards.
- **0:15 – 0:45 (30 min)**: Core Concept: The "Underline / Pair Finding" technique for evaluating multi-operator expressions.
- **0:45 – 0:70 (25 min)**: Guided Practice: Step-by-step reduction of 5-token and 7-token expressions.
- **0:70 – 0:85 (15 min)**: Timed Evaluation Relay: Students solve in teams.
- **0:85 – 0:90 (5 min)**: Review common missteps (order of operands in division/subtraction).

### 🎯 Learning Objectives
1. Evaluate multi-operator **Prefix** expressions by scanning right-to-left for `operator operand operand` patterns.
2. Evaluate multi-operator **Postfix** expressions by scanning left-to-right for `operand operand operator` patterns.

### 📘 Step-by-Step Reduction Technique

#### Evaluating Prefix:
Scan from **right to left** (or find the first operator immediately followed by two numbers):
Evaluate: $+ \ * \ 2 \ 3 \ - \ 8 \ 4$
1. Find right-most operator followed by two numbers:
   - Notice $- \ 8 \ 4 \implies 8 - 4 = 4$.
   - Expression becomes: $+ \ * \ 2 \ 3 \ \mathbf{4}$
2. Find next operator with two numbers:
   - Notice $* \ 2 \ 3 \implies 2 \times 3 = 6$.
   - Expression becomes: $+ \ \mathbf{6} \ \mathbf{4}$
3. Evaluate $+ \ 6 \ 4 \implies 6 + 4 = \mathbf{10}$.

#### Evaluating Postfix:
Scan from **left to right**. Find the first two numbers followed immediately by an operator:
Evaluate: $8 \ 2 \ / \ 5 \ * \ 3 \ -$
1. Find two numbers followed by operator:
   - $8 \ 2 \ / \implies 8 / 2 = 4$.
   - Expression becomes: $\mathbf{4} \ 5 \ * \ 3 \ -$
2. Next: $4 \ 5 \ * \implies 4 \times 5 = 20$.
   - Expression becomes: $\mathbf{20} \ 3 \ -$
3. Next: $20 \ 3 \ - \implies 20 - 3 = \mathbf{17}$.

### 📝 In-Class Exercises
1. Evaluate the prefix expression: $* \ + \ 3 \ 4 \ - \ 9 \ 7$.  
   *Step 1*: $+ \ 3 \ 4 = 7$ and $- \ 9 \ 7 = 2$.  
   *Step 2*: $* \ 7 \ 2 = 14$. (*Answer*: 14)
2. Evaluate the postfix expression: $12 \ 4 \ / \ 3 \ 2 \ * \ +$.  
   *Step 1*: $12 \ 4 \ / = 3$ and $3 \ 2 \ * = 6$.  
   *Step 2*: $3 \ 6 \ + = 9$. (*Answer*: 9)

---

## 📅 Class 3: Converting Between Infix, Prefix, and Postfix

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick postfix evaluation puzzle.
- **0:15 – 0:45 (30 min)**: Core Concept: The "Full Parenthesization Method" for converting Infix to Prefix and Postfix.
- **0:45 – 0:70 (25 min)**: Guided Practice: Parenthesizing standard expressions according to PEMDAS and moving operators.
- **0:70 – 0:85 (15 min)**: In-Class Speed Conversion Challenge.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Fully parenthesize any arithmetic expression according to standard precedence.
2. Convert Infix to Prefix by moving each operator to the left of its opening parenthesis.
3. Convert Infix to Postfix by moving each operator to the right of its closing parenthesis.

### 📘 The "Full Parenthesization" Conversion Secret

#### Problem: Convert $(A + B) \times (C - D)$ to Prefix and Postfix
- Step 1: Fully parenthesize according to PEMDAS:
  $$((A + B) * (C - D))$$
- Step 2: **For Prefix (Move operators to left parenthesis)**:
  - $(A + B) \rightarrow (+ \ A \ B)$
  - $(C - D) \rightarrow (- \ C \ D)$
  - $((+ A B) * (- C D)) \rightarrow * (+ A B) (- C D)$
  - Erase parentheses: $* \ + \ A \ B \ - \ C \ D$.
- Step 3: **For Postfix (Move operators to right parenthesis)**:
  - $(A + B) \rightarrow (A \ B \ +)$
  - $(C - D) \rightarrow (C \ D \ -)$
  - $((A B +) * (C D -)) \rightarrow ((A B +) (C D -) *)$
  - Erase parentheses: $A \ B \ + \ C \ D \ - \ *$.

### 📝 In-Class Exercises
1. Convert $A * B + C$ to Postfix.  
   Parenthesize: $((A * B) + C) \implies A \ B \ * \ C \ +$.
2. Convert $A * B + C$ to Prefix.  
   Parenthesize: $((A * B) + C) \implies + \ * \ A \ B \ C$.
3. Convert $(A + B * C) / D$ to Postfix.  
   Parenthesize: $((A + (B * C)) / D) \implies A \ B \ C \ * \ + \ D \ /$.

---

## 📅 Class 4: "What Does This Program Do?" & Contest 2 Mock Test

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick prefix conversion drill.
- **0:15 – 0:45 (30 min)**: Pseudocode Focus: String loops, counting specific characters, string length.
- **0:45 – 0:75 (30 min)**: **Full Timed Contest 2 Mock Test (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Mock test debrief and celebration!

### 📘 Pseudocode Tracing Example

```basic
S$ = "KANGAROO"
COUNT = 0
FOR I = 1 TO LEN(S$)
  CH$ = MID$(S$, I, 1)
  IF CH$ = "A" OR CH$ = "O" THEN
    COUNT = COUNT + 1
  END IF
NEXT I
PRINT COUNT * 3
```
- `LEN(S$)` is 8.
- Letters at indices: K, A, N, G, A, R, O, O.
- Vowels matching "A" or "O": index 2 (A), index 5 (A), index 7 (O), index 8 (O).
- Total matches = 4.
- Output: $COUNT * 3 = 4 \times 3 = \mathbf{12}$.

---

### 🏆 Unit 2 Mock Contest (Elementary Division)
1. Evaluate the prefix expression: $+ \ * \ 4 \ 3 \ 8$. (*Answer: $4 \times 3 + 8 = 20$*)
2. Evaluate the postfix expression: $16 \ 4 \ 2 \ / \ -$. (*Answer: $4 / 2 = 2 \implies 16 - 2 = 14$*)
3. Convert the infix expression $(A + B) / (C * D)$ to postfix. (*Answer: $A \ B \ + \ C \ D \ * \ /$*)
4. Evaluate the prefix expression: $* \ - \ 10 \ 4 \ + \ 2 \ 3$. (*Answer: $(10 - 4) \times (2 + 3) = 6 \times 5 = 30$*)
5. What does the following program print?
   ```basic
   A = 3
   B = 10
   FOR I = 1 TO 3
     B = B - A
     A = A + 1
   NEXT I
   PRINT B
   ```
   (*Answer: Start: B=10, A=3. I=1: B=7, A=4. I=2: B=3, A=5. I=3: B=-2, A=6. Output: -2*)
