# Unit 2: Intermediate Division (4 Classes × 90 Minutes)

This curriculum prepares high school competitors (Grades 10–12) for **ACSL Contest 2** at the Intermediate/Senior Division level, covering advanced bit-string algebraic equations, relational/unary prefix and postfix expressions, intermediate pseudocode, and contest programming strategies.

---

## 📅 Class 1: Advanced Bit-String Equations & Algebraic Properties

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: 5 rapid bit-string evaluation problems.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Boolean algebra identities applied to bit strings (Distributive law, De Morgan's on bit-strings, Absorption).
  - Bit-equations with multiple variables or wildcard solutions ($*$).
  - Circular shifts of arbitrary length $k$ where $k > n$ (modulus property: $\text{CIRC-}k = \text{CIRC-}(k \bmod n)$).
- **0:45 – 0:70 (25 min)**: Guided Practice: Solving system equations for 5-bit unknown strings.
- **0:70 – 0:85 (15 min)**: Timed Speed Challenge: 3 contest-grade bit equation problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Solve for unknown bit-strings $X$ with masking constraints and multiple valid configurations.
2. Apply the modulo reduction property to circular shifts ($k \pmod n$).
3. Algebraically simplify bit-string expressions before numerical substitution.

### 📘 Core Content & Worked Examples

#### Example 1: Solving Bit Equations with Unknown Variable $X$
Find all 5-bit strings $X$ that satisfy:
$$(\text{RCIRC-2 } X) \text{ XOR } 01101 = (\text{LSHIFT-1 } X) \text{ OR } 10010$$
- Let $X = x_1 x_2 x_3 x_4 x_5$.
- Compute LHS:
  $$\text{RCIRC-2 } X = x_4 x_5 x_1 x_2 x_3$$
  $$\text{LHS} = (x_4 \oplus 0)(x_5 \oplus 1)(x_1 \oplus 1)(x_2 \oplus 0)(x_3 \oplus 1) = x_4 \ (\sim x_5) \ (\sim x_1) \ x_2 \ (\sim x_3)$$
- Compute RHS:
  $$\text{LSHIFT-1 } X = x_2 x_3 x_4 x_5 0$$
  $$\text{RHS} = (x_2 \lor 1)(x_3 \lor 0)(x_4 \lor 0)(x_5 \lor 1)(0 \lor 0) = 1 \ x_3 \ x_4 \ 1 \ 0$$
- Equate bit-by-bit:
  - Bit 1: $x_4 = 1 \implies x_4 = 1$.
  - Bit 2: $\sim x_5 = x_3 \implies x_5 = \sim x_3$.
  - Bit 3: $\sim x_1 = x_4$. Since $x_4 = 1 \implies \sim x_1 = 1 \implies x_1 = 0$.
  - Bit 4: $x_2 = 1 \implies x_2 = 1$.
  - Bit 5: $\sim x_3 = 0 \implies x_3 = 1$.
  - Using $x_5 = \sim x_3$: $x_5 = 0$.
- All bits determined!
  $$X = x_1 x_2 x_3 x_4 x_5 = \mathbf{01110}.$$

---

## 📅 Class 2: Advanced Prefix/Postfix (Unary, Exponents & Relational)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick Infix-Postfix stack tracing.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Handling Unary Minus (represented as `@` or `~` or `-` in single-operand position).
  - Relational Operators in expressions ($<, \le, >, \ge, =, \ne$) returning Boolean $0$ or $1$.
  - Right-associative exponentiation in Postfix/Prefix.
- **0:45 – 0:70 (25 min)**: Guided Practice: Evaluating mixed boolean-arithmetic postfix and prefix expressions.
- **0:70 – 0:85 (15 min)**: In-Class Speed Round: 4 complex evaluation problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Q&A.

### 🎯 Learning Objectives
1. Correctly parse unary minus operators in prefix and postfix notations.
2. Evaluate expressions intermixing arithmetic operators and relational operators.
3. Build complete abstract syntax trees for complex expressions.

### 📘 Core Content & Worked Examples

#### Example: Evaluating Prefix with Relational and Unary Operators
Let `@` denote unary minus. Evaluate:
$$+ \ * \ > \ 5 \ 3 \ 4 \ @ \ - \ 8 \ 2$$
- Work from right to left:
  - $- \ 8 \ 2 \implies 8 - 2 = 6$.
  - $@ \ 6 \implies -6$.
  - Now left sub-expression: $> \ 5 \ 3 \implies 5 > 3$ is **True (1)**.
  - $* \ 1 \ 4 \implies 1 \times 4 = 4$.
  - Finally: $+ \ 4 \ (-6) \implies 4 + (-6) = \mathbf{-2}$.

#### Example: Postfix Evaluation with Exponentiation
Evaluate:
$$2 \ 3 \ 2 \ \text{\textasciicircum} \ \text{\textasciicircum} \ 5 \ -$$
- Right-to-left power rule in Postfix is handled naturally by the stack:
  - Stack after numbers: $[2, 3, 2]$.
  - Operator `^`: pop 2, pop 3 $\implies 3^2 = 9$. Stack is $[2, 9]$.
  - Operator `^`: pop 9, pop 2 $\implies 2^9 = 512$. Stack is $[512]$.
  - Push 5: Stack is $[512, 5]$.
  - Operator `-`: pop 5, pop 512 $\implies 512 - 5 = \mathbf{507}$.

---

## 📅 Class 3: "What Does This Program Do?" (Intermediate Level)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Pseudocode function trace.
- **0:15 – 0:45 (30 min)**: Intermediate Pseudocode Constructs:
  - String manipulation algorithms: Palindrome checks, anagram transforms, run-length encoding.
  - 2D Array / Matrix grid traversal.
  - Bitwise operations embedded in pseudocode (`BAND`, `BOR`, `BXOR`, `BSHL`, `BSHR`).
- **0:45 – 0:70 (25 min)**: Guided Practice: Tracing an encryption/decryption loop.
- **0:70 – 0:85 (15 min)**: Timed Pseudocode Drill: 2 past ACSL contest questions.
- **0:85 – 0:90 (5 min)**: Wrap-up & common pitfalls.

### 📘 Pseudocode Tracing Example

```basic
S$ = "ACSL2024"
FOR I = 1 TO LEN(S$)
  C$ = MID$(S$, I, 1)
  IF C$ >= "0" AND C$ <= "9" THEN
    D = VAL(C$)
    PRINT CHR$(ASC("A") + D);
  ELSE
    PRINT C$;
  END IF
NEXT I
```
- Character-by-character analysis:
  - `A`: letter $\rightarrow$ prints `A`
  - `C`: letter $\rightarrow$ prints `C`
  - `S`: letter $\rightarrow$ prints `S`
  - `L`: letter $\rightarrow$ prints `L`
  - `2`: digit $2 \rightarrow \text{ASC}('A') + 2 = 65 + 2 = 67 \implies \text{'C'}$
  - `0`: digit $0 \rightarrow \text{ASC}('A') + 0 = 65 \implies \text{'A'}$
  - `2`: digit $2 \rightarrow \text{'C'}$
  - `4`: digit $4 \rightarrow \text{ASC}('A') + 4 = 69 \implies \text{'E'}$
- Output: `"ACSLCA CE"` $\rightarrow$ **`ACSL CACE`** (without spaces: `ACSLCA CE`).

---

## 📅 Class 4: Contest 2 Programming Problem & Mock Contest

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick string tokenization challenge.
- **0:15 – 0:45 (30 min)**: Contest Programming Deep Dive:
  - Common Contest 2 problem patterns (e.g. "String Expression Evaluator", "Word Scramble", "Bit String Formula Simplifier").
  - Designing stack-based evaluators in Python / Java.
- **0:45 – 0:75 (30 min)**: **Full Timed ACSL Contest 2 Mock Exam (5 Questions, 30 Minutes)**.
- **0:75 – 0:90 (15 min)**: Comprehensive debrief and question walk-through.

### 💻 Contest 2 Programming Strategy: Postfix Evaluator

```python
# Sample Contest 2 Engine: Stack-based Postfix with Powers & Unary Minus
def eval_postfix(tokens):
    stack = []
    for token in tokens:
        if token.lstrip('-').isdigit():
            stack.append(int(token))
        elif token == '@':  # Unary minus
            val = stack.pop()
            stack.append(-val)
        else:
            b = stack.pop()
            a = stack.pop()
            if token == '+': stack.append(a + b)
            elif token == '-': stack.append(a - b)
            elif token == '*': stack.append(a * b)
            elif token == '/': stack.append(int(a / b))
            elif token == '^': stack.append(a ** b)
            elif token == '>': stack.append(1 if a > b else 0)
            elif token == '<': stack.append(1 if a < b else 0)
            elif token == '=': stack.append(1 if a == b else 0)
    return stack[0]
```

---

### 🏆 Unit 2 Intermediate Division Mock Contest
1. How many 5-bit strings $X$ satisfy: $(\text{LSHIFT-1 } X) \text{ AND } 11011 = 01000$? (*Answer: 2 strings*)
2. Evaluate: $\text{RCIRC-3 } (\text{NOT } 011010 \text{ XOR } \text{LCIRC-2 } 110001)$. (*Answer: $001100$*)
3. Evaluate the prefix expression where `@` is unary minus: $+ \ * \ @ \ 3 \ 4 \ \text{\textasciicircum} \ 2 \ 3$. (*Answer: $(-3 \times 4) + (2^3) = -12 + 8 = -4$*)
4. Convert to Postfix: $(A + B) * (C - D \text{\textasciicircum} E) / F$. (*Answer: $A \ B \ + \ C \ D \ E \ \text{\textasciicircum} \ - \ * \ F \ /$*)
5. What does the following program print?
   ```basic
   A = 5
   B = 2
   FOR I = 1 TO 3
     FOR J = 1 TO I
       A = A + J
     NEXT J
     B = B * 2
   NEXT I
   PRINT A + B
   ```
   (*Answer: Outer I=1: A=5+1=6, B=4. Outer I=2: A=6+(1+2)=9, B=8. Outer I=3: A=9+(1+2+3)=15, B=16. Output: 15+16 = 31*)
