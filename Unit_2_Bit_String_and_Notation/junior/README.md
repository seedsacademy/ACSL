# Unit 2: Junior Division (4 Classes × 90 Minutes)

This curriculum prepares middle school students (Grades 7–9) for **ACSL Contest 2** (Bit-String Flicking, Prefix / Infix / Postfix Notation, and "What Does This Program Do?").

---

## 📅 Class 1: Bit-String Flicking Fundamentals & Precedence

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: Truth tables for basic logic gates (NOT, AND, OR, XOR).
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Bit-by-bit parallel evaluation on strings of equal length (e.g., length 5).
  - Truth table mechanics:
    - $\text{NOT}(0)=1, \text{NOT}(1)=0$.
    - $\text{AND}$: 1 only if both are 1.
    - $\text{OR}$: 1 if at least one is 1.
    - $\text{XOR}$ (Exclusive OR): 1 if bits are different ($0 \oplus 1 = 1$, $1 \oplus 1 = 0$).
  - Official Precedence Rule: **(Parentheses) $\rightarrow$ NOT $\rightarrow$ AND $\rightarrow$ XOR $\rightarrow$ OR**.
- **0:45 – 0:70 (25 min)**: Guided Practice: Multi-operator bit-string evaluation step-by-step.
- **0:70 – 0:85 (15 min)**: Timed Practice: 5 compound bit-string evaluations.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Apply `NOT`, `AND`, `OR`, `XOR` to bit-strings of length $N$ simultaneously.
2. Adhere strictly to ACSL's official order of operations.
3. Avoid the common pitfall of evaluating left-to-right when operator precedence takes priority!

### 📘 Core Content & Worked Examples

#### Example 1: Applying Precedence
Evaluate:
$$\text{NOT } 10110 \text{ OR } 01101 \text{ AND } 11000$$
- Step 1: Precedence dictates **`NOT`** first:
  $$\text{NOT } 10110 = 01001$$
  Expression is now: $01001 \text{ OR } 01101 \text{ AND } 11000$.
- Step 2: Precedence dictates **`AND`** before `OR`:
  $$01101 \text{ AND } 11000 = 01000$$
  Expression is now: $01001 \text{ OR } 01000$.
- Step 3: Evaluate **`OR`**:
  $$01001 \text{ OR } 01000 = \mathbf{01001}.$$

#### Example 2: XOR Behavior
$$10110 \text{ XOR } 11100 = 01010$$
*Tip*: XOR with all 1s is equivalent to NOT: $A \oplus 11111 = \text{NOT } A$.

### 📝 In-Class Exercises
1. Evaluate: $\text{NOT } (11001 \text{ XOR } 01011)$. (*Answer*: $11001 \oplus 01011 = 10010 \implies \text{NOT} = 01101$).
2. Evaluate: $10101 \text{ AND } 01110 \text{ XOR } 11001$. (*Answer*: AND first: $00100$. Then XOR: $00100 \oplus 11001 = 11101$).

---

## 📅 Class 2: Shifting, Rotating & Solving Bit Equations

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick bit-operator review quiz.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - `LSHIFT-k`: Shift left $k$ places, zero-fill on the right, discard overflow bits.
  - `RSHIFT-k`: Shift right $k$ places, zero-fill on the left, discard overflow bits.
  - `LCIRC-k`: Circular rotate left $k$ places (bits exiting left re-enter on right).
  - `RCIRC-k`: Circular rotate right $k$ places (bits exiting right re-enter on left).
  - Full ACSL Precedence: **( ) $\rightarrow$ NOT $\rightarrow$ SHIFTS/CIRCS $\rightarrow$ AND $\rightarrow$ XOR $\rightarrow$ OR**.
  - Solving for unknown bit-string $X$ of length $n$.
- **0:45 – 0:70 (25 min)**: Guided Practice: Solving bit-equations bit-by-bit (e.g. $(X \text{ AND } 10100) \dots$).
- **0:70 – 0:85 (15 min)**: Timed Contest Drill: 3 tricky bit equations.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Compute `LSHIFT`, `RSHIFT`, `LCIRC`, `RCIRC` for any integer $k \ge 0$.
2. Solve equations of the form $\text{expr}(X) = \text{target}$ for bit-string $X$.
3. Handle cases where multiple solutions exist (using wildcard $*$ or listing possibilities).

### 📘 Core Content & Worked Examples

#### Shift vs. Circ Comparison (Length 5):
Given $B = 10110$:
- $\text{LSHIFT-2}(10110) = 11000$ (discards $10$, adds $00$ at right)
- $\text{RSHIFT-2}(10110) = 00101$ (discards $10$ on right, adds $00$ on left)
- $\text{LCIRC-2}(10110) = 11010$ (first two bits $10$ wrap around to the right)
- $\text{RCIRC-2}(10110) = 10101$ (last two bits $10$ wrap around to the left)

#### Example: Solving a Bit-String Equation
Find all 5-bit strings $X$ that satisfy:
$$(\text{LSHIFT-1 } X) \text{ AND } 10110 = 00100$$
- Let $X = b_1 b_2 b_3 b_4 b_5$.
- $\text{LSHIFT-1 } X = b_2 b_3 b_4 b_5 0$.
- We are given:
  $$(b_2 b_3 b_4 b_5 0) \text{ AND } 10110 = 00100$$
- Compare bit by bit:
  - Bit 1: $b_2 \text{ AND } 1 = 0 \implies b_2 = 0$.
  - Bit 2: $b_3 \text{ AND } 0 = 0 \implies b_3$ can be $0$ or $1$.
  - Bit 3: $b_4 \text{ AND } 1 = 1 \implies b_4 = 1$.
  - Bit 4: $b_5 \text{ AND } 1 = 0 \implies b_5 = 0$.
  - Bit 5: $0 \text{ AND } 0 = 0$ (Always holds).
  - What about $b_1$? It was shifted out, so it can be **either 0 or 1**!
- Conclusion: $X = *0*10 \implies$ Two solutions: $00010, 10010, 00110, 10110$ (4 solutions total!).

---

## 📅 Class 3: Prefix & Postfix Mastery

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Infix expression tree representation.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Complete arithmetic operator precedence: `^` (Right-to-left) $>$ `*`, `/` (Left-to-right) $>$ `+`, `-` (Left-to-right).
  - Infix $\rightarrow$ Postfix conversion using the Stack Algorithm.
  - Infix $\rightarrow$ Prefix conversion using the Reversed Scan Method.
  - Direct Stack Evaluation of Postfix expressions.
- **0:45 – 0:70 (25 min)**: Guided Practice: Converting complex arithmetic expressions with powers and division.
- **0:70 – 0:85 (15 min)**: Timed Evaluation Sprint: 5 contest questions.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Convert infix expressions to prefix and postfix accurately without losing operator order.
2. Evaluate prefix and postfix expressions containing exponents (`^`).
3. Build expression parse trees to verify prefix and postfix representations.

### 📘 Core Content & Worked Examples

#### Example: Evaluating Prefix with Exponent
Evaluate:
$$+ \ / \ 16 \ \text{\textasciicircum} \ 2 \ 3 \ * \ 4 \ 2$$
- Work from right to left:
  - $* \ 4 \ 2 \implies 4 \times 2 = 8$.
  - Next operator with two operands: $\text{\textasciicircum} \ 2 \ 3 \implies 2^3 = 8$.
  - Next: $/ \ 16 \ 8 \implies 16 / 8 = 2$.
  - Next: $+ \ 2 \ 8 \implies 2 + 8 = \mathbf{10}$.

#### Example: Infix to Postfix Conversion
Convert: $(A + B * C) / (D - E \text{\textasciicircum} F)$
- Fully parenthesize:
  $$((A + (B * C)) / (D - (E \text{\textasciicircum} F)))$$
- Postfix shift:
  - $(B * C) \rightarrow B C *$
  - $(A + BC*) \rightarrow A B C * +$
  - $(E \text{\textasciicircum} F) \rightarrow E F \text{\textasciicircum}$
  - $(D - EF\text{\textasciicircum}) \rightarrow D E F \text{\textasciicircum} -$
  - Whole expression: $A \ B \ C \ * \ + \ D \ E \ F \ \text{\textasciicircum} \ - \ /$

---

## 📅 Class 4: "What Does This Program Do?" & Contest 2 Mock Exam

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick bit-flicking identity challenge.
- **0:15 – 0:45 (30 min)**: Pseudocode Focus: String transformations, nested loops, character counters.
- **0:45 – 0:75 (30 min)**: **Full Timed ACSL Contest 2 Mock Exam (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Answer key breakdown and test review.

### 📘 Junior Pseudocode Example

```basic
S$ = "ABRACADABRA"
RES$ = ""
FOR I = 1 TO LEN(S$)
  C$ = MID$(S$, I, 1)
  IF C$ = "A" THEN
    RES$ = RES$ + "Z"
  ELSE IF C$ = "B" THEN
    RES$ = RES$ + "Y"
  ELSE
    RES$ = RES$ + C$
  END IF
NEXT I
PRINT RES$
```
Output: `"ZYRZCZDZYRZ"`.

---

### 🏆 Unit 2 Junior Division Mock Contest
1. Evaluate: $\text{LSHIFT-2 } (\text{NOT } 10101 \text{ OR } \text{RCIRC-1 } 01100)$. (*Answer: $10000$*)
2. Solve for the 5-bit string $X$: $(\text{LCIRC-2 } X) \text{ AND } 11001 = 10001$ where $X$ has exactly two 1s. (*Answer: $00101$*)
3. Evaluate the postfix expression: $18 \ 6 \ / \ 3 \ 2 \ \text{\textasciicircum} \ * \ 10 \ -$. (*Answer: $18/6=3$, $3^2=9$, $3 \times 9 = 27$, $27 - 10 = 17$*)
4. Convert the following infix expression to prefix: $(A + B) * C - D / E$. (*Answer: $- \ * \ + \ A \ B \ C \ / \ D \ E$*)
5. What does the following program print?
   ```basic
   A = 20
   B = 4
   FOR I = 1 TO 3
     A = A - B
     B = B + 2
   NEXT I
   PRINT A + B
   ```
   (*Answer: Start: A=20, B=4. I=1: A=16, B=6. I=2: A=10, B=8. I=3: A=2, B=10. Output: A+B = 2+10 = 12*)
