# Unit 2: Intermediate Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 2 (Advanced Bit Equations, Complex Prefix/Postfix with Unary and Relational Operators, Intermediate Pseudocode, and Contest Programming). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Advanced Bit-String Equations & Masking

### Section A: Complex Bit Equations
1. Find all 5-bit strings $X$ that satisfy:
   $$(\text{RCIRC-2 } X) \text{ XOR } 10101 = (\text{LSHIFT-1 } X) \text{ OR } 01100$$

2. Solve for the 6-bit string $X$:
   $$\text{NOT } (\text{LCIRC-2 } X) \text{ AND } 111000 = 010000 \quad \text{and} \quad (\text{RSHIFT-1 } X) \text{ XOR } 010101 = 001101$$

3. How many 5-bit strings $X$ satisfy the identity:
   $$(X \text{ AND } 10110) \text{ OR } (\text{NOT } X \text{ AND } 01001) = 00000$$

---

## 📝 Homework 2: Advanced Prefix & Postfix (Unary & Relational)

### Section A: Unary Minus (`@`) and Relational Operators
Evaluate the following where `@` denotes unary minus:
1. Evaluate: $+ \ * \ @ \ 4 \ 3 \ / \ 20 \ 5$
2. Evaluate: $* \ > \ 8 \ 5 \ + \ 7 \ @ \ 2$
3. Evaluate: $15 \ 3 \ / \ @ \ 4 \ * \ 10 \ +$
4. Evaluate: $6 \ 2 \ \text{\textasciicircum} \ 10 \ > \ 5 \ 3 \ - \ *$

### Section B: Infix to Postfix with Relational Operators
5. Convert $(A + B > C) * (D - E)$ to Postfix.
6. Convert $(A \text{\textasciicircum} B = C * D) + E$ to Prefix.

---

## 📝 Homework 3: Intermediate Pseudocode Tracing

### Section A: String Parsing & Transformation Algorithms
1. What does the following program print?
   ```basic
   S$ = "ABCDCBA"
   P = 1
   FOR I = 1 TO LEN(S$) \ 2
     C1$ = MID$(S$, I, 1)
     C2$ = MID$(S$, LEN(S$) - I + 1, 1)
     IF C1$ <> C2$ THEN
       P = 0
     END IF
   NEXT I
   PRINT P
   ```

2. What does the following program print?
   ```basic
   A = 5
   B = 3
   C = 2
   FOR I = 1 TO 3
     A = (A + B) MOD 7
     B = (B * C) MOD 5
     C = (A + B + C) MOD 4
   NEXT I
   PRINT A + B + C
   ```

---

## 📝 Homework 4: Contest 2 Programming Problem & Mock Exam

### Section A: Programming Problem Blueprint
Write a function `evaluate_postfix(expr: str) -> int` that takes a space-separated postfix expression containing integers, `+`, `-`, `*`, `/` (integer division), `^` (exponentiation), and `@` (unary negation) and returns the evaluated integer.

```python
def evaluate_postfix(expr: str) -> int:
    pass
```

### Section B: Intermediate Contest 2 Mock Set
1. Solve for the 5-bit string $X$: $(\text{LCIRC-2 } X) \text{ XOR } 11010 = \text{NOT } (\text{RSHIFT-1 } 10100)$.
2. Evaluate the prefix expression: $- \ * \ 3 \ + \ 4 \ 2 \ \text{\textasciicircum} \ 2 \ 4$.
3. Convert the infix expression $(A * B - C \text{\textasciicircum} D) / (E + F)$ to postfix.
4. How many 5-bit strings $X$ satisfy: $(\text{LSHIFT-2 } X) \text{ AND } 11111 = 00000$?
5. What does the following program print?
   ```basic
   DIM ARR(5)
   FOR I = 1 TO 5
     ARR(I) = I * 2
   NEXT I
   FOR J = 1 TO 4
     ARR(J + 1) = ARR(J + 1) + ARR(J)
   NEXT J
   PRINT ARR(5)
   ```

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. Equate bit-by-bit:
   - $\text{RCIRC-2 } X = x_4 x_5 x_1 x_2 x_3$.
   - $\text{LHS} = (x_4 \oplus 1)(x_5 \oplus 0)(x_1 \oplus 1)(x_2 \oplus 0)(x_3 \oplus 1) = \sim x_4 \ x_5 \ \sim x_1 \ x_2 \ \sim x_3$.
   - $\text{RHS} = (x_2 \lor 0)(x_3 \lor 1)(x_4 \lor 1)(x_5 \lor 0)(0 \lor 0) = x_2 \ 1 \ 1 \ x_5 \ 0$.
   - Bit 5: $\sim x_3 = 0 \implies x_3 = 1$.
   - Bit 3: $\sim x_1 = 1 \implies x_1 = 0$.
   - Bit 2: $x_5 = 1 \implies x_5 = 1$.
   - Bit 4: $x_2 = x_5 = 1 \implies x_2 = 1$.
   - Bit 1: $\sim x_4 = x_2 = 1 \implies x_4 = 0$.
   - Result: $X = \mathbf{01101}$.
2. LCIRC and RSHIFT analysis yields unique 6-bit string: $\mathbf{100110}$.
3. For the OR to be $00000$, both terms must be $00000$.
   $X \land 10110 = 00000 \implies x_1=0, x_3=0, x_4=0$.
   $\sim X \land 01001 = 00000 \implies \sim x_2 = 0 \implies x_2 = 1$; $\sim x_5 = 0 \implies x_5 = 1$.
   Unique solution: $\mathbf{01001}$ (1 string).

### Homework 2 Solutions
1. $@ \ 4 = -4$. $-4 \times 3 = -12$. $20/5 = 4$. $-12 + 4 = \mathbf{-8}$.
2. $> \ 8 \ 5 = 1$ (True). $@ \ 2 = -2$. $7 + (-2) = 5$. $1 \times 5 = \mathbf{5}$.
3. $15/3 = 5 \implies @ \ 5 = -5$. $-5 \times 4 = -20$. $-20 + 10 = \mathbf{-10}$.
4. $6^2 = 36$. $36 > 10 = 1$. $5 - 3 = 2$. $1 \times 2 = \mathbf{2}$.
5. $\mathbf{A \ B \ + \ C \ > \ D \ E \ - \ *}$.
6. $\mathbf{+ \ = \ \text{\textasciicircum} \ A \ B \ * \ C \ D \ E}$.

### Homework 3 Solutions
1. Standard Palindrome verification algorithm! "ABCDCBA" is a palindrome $\implies P = \mathbf{1}$.
2. Tracing iteration states:
   - Initial: $A=5, B=3, C=2$.
   - $I=1: A=(5+3)\%7=1; B=(3\times 2)\%5=1; C=(1+1+2)\%4=0$.
   - $I=2: A=(1+1)\%7=2; B=(1\times 0)\%5=0; C=(2+0+0)\%4=2$.
   - $I=3: A=(2+0)\%7=2; B=(0\times 2)\%5=0; C=(2+0+2)\%4=0$.
   - Sum $= 2 + 0 + 0 = \mathbf{2}$.

### Homework 4 Solutions
1. $\text{RSHIFT-1 } 10100 = 01010 \implies \text{NOT} = 10101$.
   $\text{LCIRC-2 } X \oplus 11010 = 10101 \implies \text{LCIRC-2 } X = 10101 \oplus 11010 = 01111$.
   $X = \text{RCIRC-2 } 01111 = \mathbf{11011}$.
2. $+ \ 4 \ 2 = 6$, $3 \times 6 = 18$. $2^4 = 16$. $18 - 16 = \mathbf{2}$.
3. $\mathbf{A \ B \ * \ C \ D \ \text{\textasciicircum} \ - \ E \ F \ + \ /}$.
4. $\text{LSHIFT-2 } X = x_3 x_4 x_5 0 0$.
   For this to equal $00000$, we must have $x_3=0, x_4=0, x_5=0$.
   $x_1, x_2$ can be any binary digits $\implies 2^2 = \mathbf{4 \text{ strings}}$.
5. Initial ARR: $[2, 4, 6, 8, 10]$.
   - $J=1: ARR(2) = 4 + 2 = 6$
   - $J=2: ARR(3) = 6 + 6 = 12$
   - $J=3: ARR(4) = 8 + 12 = 20$
   - $J=4: ARR(5) = 10 + 20 = 30$
   - Output: **30** (Prefix sum array!).
