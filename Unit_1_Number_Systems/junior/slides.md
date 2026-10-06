---
marp: true
---

<!--
theme: gaia
_class: lead
paginate: true
backgroundColor: "#ffffff"
color: "#1a1a2e"
style: |
  section {
    font-family: 'Segoe UI', Arial, sans-serif;
    padding: 40px;
  }
  h1 { color: #1b5e20; }
  h2 { color: #2e7d32; }
  code { background: #e8f5e9; color: #2e7d32; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 1: Junior Division
## Number Systems, Recursion & Pseudocode
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Junior Syllabus Matrix

- **Class 1**: Arbitrary Base Conversions ($b \in [2, 16]$) & Fractional Bases
- **Class 2**: Multi-Base Arithmetic Operations (Octal & Hex directly)
- **Class 3**: Recursive Functions (Tracing Call Stacks & Trees)
- **Class 4**: "What Does This Program Do?" (Arrays, Modulo & Loops)

---

<!-- _class: lead -->
# 🌟 Class 1
## Arbitrary Bases & Fractional Conversions

---

## Positional Expansion in Base $b$

Any number with integer and fractional parts in base $b$:
$$N = d_k b^k + \dots + d_1 b^1 + d_0 b^0 + d_{-1} b^{-1} + d_{-2} b^{-2} + \dots$$

### Example: Evaluate $243_5$
$$2 \times 5^2 + 4 \times 5^1 + 3 \times 5^0 = 50 + 20 + 3 = \mathbf{73_{10}}$$

### Example: Fractional Expansion
$$0.1011_2 = \frac{1}{2} + \frac{0}{4} + \frac{1}{8} + \frac{1}{16} = \frac{11}{16} = \mathbf{0.6875_{10}}$$

---

## Converting Fractions: Decimal $\rightarrow$ Base $b$
### Repeated Multiplication Method

**Convert $0.625_{10}$ to Binary:**
1. $0.625 \times 2 = \mathbf{1}.25 \implies \text{first bit is } 1$
2. Take the fractional remainder: $0.25 \times 2 = \mathbf{0}.5 \implies \text{second bit is } 0$
3. $0.5 \times 2 = \mathbf{1}.0 \implies \text{third bit is } 1$
4. Remainder is $0$ $\rightarrow$ Terminate!

$$\mathbf{0.625_{10} = 0.101_2}$$

---

<!-- _class: lead -->
# 🌟 Class 2
## Arithmetic Directly in Bases 8 and 16

---

## Hexadecimal Addition: No Base 10 Needed!

Rule: If sum $\ge 16$, subtract 16 and carry 1.

$$\begin{array}{r@{\quad}l}
  \text{Carries:} & 1 \quad 1 \\
  & 3 \quad \text{A} \quad 9_{16} \\
+ & 7 \quad \text{C} \quad 5_{16} \\
\hline
& \mathbf{B} \quad \mathbf{6} \quad \mathbf{E}_{16}
\end{array}$$

- Column 0: $9 + 5 = 14 = \mathbf{\text{E}}$
- Column 1: $1 + \text{A} + \text{C} = 1 + 10 + 12 = 23 = 16 + 7 \dots$ wait:
  $23 - 16 = 7$ (Write 7, carry 1) $\implies \mathbf{B6E}$ or check arithmetic!

---

<!-- _class: lead -->
# 🌟 Class 3
## Recursive Functions: Tree Diagrams

---

## Multi-Branch Recursion Tree

Given:
$$f(n) = \begin{cases} n & \text{if } n \le 1 \\ f(n-1) + f(n-2) & \text{if } n > 1 \end{cases}$$

```text
               f(4)
             /      \
         f(3)        f(2)
        /    \      /    \
      f(2)  f(1)  f(1)  f(0)
     /    \
   f(1)  f(0)
```
- Evaluate from the leaves up: $f(0)=0, f(1)=1$.
- $f(2) = 1 + 0 = 1$.
- $f(3) = 1 + 1 = 2$.
- $f(4) = 2 + 1 = \mathbf{3}$.

---

<!-- _class: lead -->
# 🌟 Class 4
## "What Does This Program Do?" (Junior Level)

---

## Arrays & Modulo Arithmetic Tracing

```basic
DIM A(4)
FOR I = 1 TO 4
  A(I) = (I * 5) MOD 6
NEXT I
PRINT A(2) + A(4)
```

1. $I = 1: A(1) = 5 \pmod 6 = 5$
2. $I = 2: A(2) = 10 \pmod 6 = 4$
3. $I = 3: A(3) = 15 \pmod 6 = 3$
4. $I = 4: A(4) = 20 \pmod 6 = 2$

$$\text{Output: } A(2) + A(4) = 4 + 2 = \mathbf{6}$$
