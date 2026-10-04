# Unit 1: Junior Division (4 Classes × 90 Minutes)

This curriculum prepares middle school students (Grades 7–9) for **ACSL Contest 1** (Computer Number Systems, Recursive Functions, and "What Does This Program Do?").

---

## 📅 Class 1: Arbitrary Base Conversions & Fractional Bases

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: Powers of bases ($2^n, 8^n, 16^n, 3^n, 5^n$).
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Base $b$ positional representation: $N = d_k b^k + \dots + d_0 b^0 + d_{-1} b^{-1} + d_{-2} b^{-2}$.
  - Converting Base $A \rightarrow$ Decimal $\rightarrow$ Base $B$.
  - Fractional base conversions (e.g., $0.1011_2$, $0.625_{10} \rightarrow$ base 2).
- **0:45 – 0:70 (25 min)**: Guided Problem Solving: Base $b$ algebraic equations (e.g. $42_b = 30_{10}$, find $b$).
- **0:70 – 0:85 (15 min)**: Timed Practice: 5 mixed conversion problems.
- **0:85 – 0:90 (5 min)**: Homework assignment & common trap warnings.

### 🎯 Learning Objectives
1. Convert numbers between any arbitrary base $b \in [2, 16]$ and decimal.
2. Convert terminating fractions between binary/hexadecimal and decimal.
3. Solve for an unknown base $b$ given equivalent representations.

### 📘 Core Content & Worked Examples

#### Example 1: Arbitrary Base Conversion
Convert $243_5$ to Base 7.
- Step 1: Base 5 to Base 10:
  $$2 \times 5^2 + 4 \times 5^1 + 3 \times 5^0 = 2(25) + 4(5) + 3(1) = 50 + 20 + 3 = 73_{10}$$
- Step 2: Base 10 to Base 7 (Repeated division):
  $$73 \div 7 = 10 \text{ R } 3$$
  $$10 \div 7 = 1 \text{ R } 3$$
  $$1 \div 7 = 0 \text{ R } 1$$
- Read remainders bottom-to-top: $133_7$.

#### Example 2: Fractional Conversions
Convert $0.6875_{10}$ to Binary and Hexadecimal.
- Binary (Repeated multiplication by 2):
  $$0.6875 \times 2 = 1.375 \rightarrow \mathbf{1}$$
  $$0.375 \times 2 = 0.75 \rightarrow \mathbf{0}$$
  $$0.75 \times 2 = 1.5 \rightarrow \mathbf{1}$$
  $$0.5 \times 2 = 1.0 \rightarrow \mathbf{1}$$
  Result: $0.1011_2$.
- Hexadecimal conversion via 4-bit grouping from the radix point:
  $$0.1011_2 = 0.\text{B}_{16} \quad (\text{since } 1011_2 = 11 = \text{B}).$$

#### Example 3: Finding an Unknown Base
If $34_b + 25_b = 62_b$, find the base $b$.
- Express in powers of $b$:
  $$(3b + 4) + (2b + 5) = 6b + 2$$
  $$5b + 9 = 6b + 2 \implies b = 7.$$

### 📝 In-Class Exercises
1. Convert $101.11_2$ to decimal. (*Answer*: $4 + 1 + 0.5 + 0.25 = 5.75_{10}$).
2. Solve for $b$: $121_b = 100_7$. (*Answer*: $b^2 + 2b + 1 = 49 \implies (b+1)^2 = 49 \implies b = 6$).
3. Convert $0.\text{A}8_{16}$ to Octal. (*Answer*: $0.1010\ 1000_2 = 0.101\ 010_2 = 0.52_8$).

---

## 📅 Class 2: Arithmetic Operations in Bases 2, 8, and 16

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Rapid recall: Addition and borrowing rules across bases.
- **0:15 – 0:45 (30 min)**: Core Concept: Multi-base column addition, subtraction with non-10 borrowing, and multiplication.
- **0:45 – 0:70 (25 min)**: Guided Practice: Hexadecimal addition/subtraction, dealing with letter carries ($\ge 16$).
- **0:70 – 0:85 (15 min)**: In-Class Speed Round: 4-minute contest problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Q&A.

### 🎯 Learning Objectives
1. Perform multi-digit addition and subtraction directly in Octal and Hexadecimal without converting to Decimal.
2. Perform binary multiplication.
3. Solve complex multi-base arithmetic expressions.

### 📘 Core Content & Worked Examples

#### Example 1: Hexadecimal Subtraction
Evaluate: $4\text{A}3_{16} - 1\text{C}7_{16}$.
- Column 0 (units): $3 - 7$. Must borrow from $\text{A}$.
  - Borrow 16 from $\text{A}$ ($10 \rightarrow 9$):
  - $16 + 3 = 19$. Now $19 - 7 = 12 = \text{C}$.
- Column 1: $9 - \text{C} = 9 - 12$. Must borrow from 4.
  - Borrow 16 from 4 ($4 \rightarrow 3$):
  - $16 + 9 = 25$. Now $25 - 12 = 13 = \text{D}$.
- Column 2: $3 - 1 = 2$.
- Result: $2\text{DC}_{16}$.

#### Example 2: Octal Addition
Evaluate: $756_8 + 467_8$.
```text
  1 1 1   (carries)
  7 5 6
+ 4 6 7
-------
1 4 4 5  in Base 8
```
- $6 + 7 = 13 = 1 \times 8 + 5$ (write 5, carry 1)
- $1 + 5 + 6 = 12 = 1 \times 8 + 4$ (write 4, carry 1)
- $1 + 7 + 4 = 12 = 1 \times 8 + 4$ (write 4, carry 1)
- Result: $1445_8$.

### 📝 In-Class Exercises
1. Calculate in Hex: $\text{B}9\text{F}_{16} + 7\text{E}4_{16}$. (*Answer*: $1383_{16}$).
2. Calculate in Octal: $602_8 - 345_8$. (*Answer*: $235_8$).
3. Multiply in Binary: $1101_2 \times 101_2$. (*Answer*: $1000001_2 = 65_{10}$).

---

## 📅 Class 3: Recursive Functions

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: What is recursion? Base cases vs. recursive step.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive: Tracing recursive calls with Call Stacks and Tree Diagrams.
- **0:45 – 0:70 (25 min)**: Guided Practice: Single recursion, multi-branch recursion ($f(n) = f(n-1) + f(n-2)$), conditional branches.
- **0:70 – 0:85 (15 min)**: Timed Drill: 3 tricky recursive function evaluations.
- **0:85 – 0:90 (5 min)**: Wrap-up & recursion shortcuts (memoization table).

### 🎯 Learning Objectives
1. Trace linear and branching recursive functions accurately without losing state.
2. Identify base conditions and termination criteria.
3. Draw recursion trees to evaluate expressions like $f(5)$ in 2 minutes or less.

### 📘 Core Content & Worked Examples

#### Example 1: Multi-Branch Recursive Function
Given the function:
$$f(x) = \begin{cases} x - 2 & \text{if } x \le 2 \\ f(x - 1) + f(x - 3) & \text{if } x > 2 \end{cases}$$
Find the value of $f(6)$.

#### Execution Tree:
```text
                   f(6)
                 /      \
             f(5)        f(3)
            /    \      /    \
         f(4)    f(2)  f(2)  f(0)
        /   \     |     |     |
      f(3)  f(1)  0     0    -2
     /   \   |
   f(2) f(0) -1
    |    |
    0   -2
```
Evaluating from bottom up:
- $f(0) = 0 - 2 = -2$
- $f(1) = 1 - 2 = -1$
- $f(2) = 2 - 2 = 0$
- $f(3) = f(2) + f(0) = 0 + (-2) = -2$
- $f(4) = f(3) + f(1) = -2 + (-1) = -3$
- $f(5) = f(4) + f(2) = -3 + 0 = -3$
- $f(6) = f(5) + f(3) = -3 + (-2) = -5$

Result: $-5$.

### 📝 In-Class Exercises
1. Given $g(n) = 3$ if $n \le 1$, else $g(n) = 2 \cdot g(n-1) - 1$. Find $g(4)$.  
   (*Answer*: $g(1)=3, g(2)=5, g(3)=9, g(4)=17$).
2. Given $h(x, y) = x + y$ if $x \le 1$, else $h(x-1, y+2) - 1$. Find $h(4, 1)$.  
   (*Answer*: $h(4,1) = h(3,3)-1 = h(2,5)-2 = h(1,7)-3 = (1+7)-3 = 5$).

---

## 📅 Class 4: "What Does This Program Do?" & Contest 1 Mock Exam

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Rapid recursion tracing problem.
- **0:15 – 0:45 (30 min)**: Junior Pseudocode Masterclass: 1D Arrays, String indexing, Nested LOOPS, modulo arithmetic (`MOD`), integer division (`INT` / `DIV`).
- **0:45 – 0:75 (30 min)**: **Full Timed Mock Contest 1 (5 Short Answer Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Complete post-contest answer review & strategic exam-taking tips.

### 📘 Pseudocode Array & Modulo Tracing Example

```basic
DIM A(6)
FOR I = 1 TO 6
  A(I) = (I * 3) MOD 7
NEXT I
S = 0
FOR J = 1 TO 5
  IF A(J) < A(J + 1) THEN
    S = S + A(J)
  ELSE
    S = S - A(J)
  END IF
NEXT J
PRINT S
```

#### Trace:
- Array $A$:
  - $A(1) = 3 \pmod 7 = 3$
  - $A(2) = 6 \pmod 7 = 6$
  - $A(3) = 9 \pmod 7 = 2$
  - $A(4) = 12 \pmod 7 = 5$
  - $A(5) = 15 \pmod 7 = 1$
  - $A(6) = 18 \pmod 7 = 4$
  - $A = [3, 6, 2, 5, 1, 4]$
- Loop $J$:
  - $J=1$: $A(1) < A(2) \implies 3 < 6$ (T) $\rightarrow S = 0 + 3 = 3$
  - $J=2$: $A(2) < A(3) \implies 6 < 2$ (F) $\rightarrow S = 3 - 6 = -3$
  - $J=3$: $A(3) < A(4) \implies 2 < 5$ (T) $\rightarrow S = -3 + 2 = -1$
  - $J=4$: $A(4) < A(5) \implies 5 < 1$ (F) $\rightarrow S = -1 - 5 = -6$
  - $J=5$: $A(5) < A(6) \implies 1 < 4$ (T) $\rightarrow S = -6 + 1 = -5$
- Final Output: **$-5$**.

---

### 🏆 Unit 1 Junior Division Mock Contest
1. Convert $1101.101_2$ to decimal. (*Answer: 13.625*)
2. Calculate: $743_8 + 365_8 - 277_8$ in Octal. (*Answer: $1031_8$*)
3. For what positive integer base $b$ does $53_b = 38_{10}$? (*Answer: $b = 7$*)
4. Given:
   $$f(n) = \begin{cases} 2 & \text{if } n \le 0 \\ f(n-1) + 2 \cdot f(n-2) & \text{if } n > 0 \end{cases}$$
   Find $f(4)$ given $f(-1) = 1$.  
   (*Answer: $f(0)=2, f(1)=f(0)+2f(-1)=2+2(1)=4, f(2)=4+2(2)=8, f(3)=8+2(4)=16, f(4)=16+2(8)=32$*)
5. What does the following program print?
   ```basic
   X = 24
   Y = 36
   WHILE X <> Y
     IF X > Y THEN
       X = X - Y
     ELSE
       Y = Y - X
     END IF
   END WHILE
   PRINT X
   ```
   (*Answer: 12 — Euclid's GCD algorithm!*)
