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
  h1 { color: #b71c1c; }
  h2 { color: #c62828; }
  code { background: #ffebee; color: #c62828; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 1: Intermediate Division
## Two's Complement, Nested Recursion & Advanced Tracing
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Intermediate Syllabus Matrix

- **Class 1**: Two's Complement Signed Arithmetic & Repeating Fractions
- **Class 2**: Complex & Nested Recursion (Ackermann & Memoization)
- **Class 3**: "What Does This Program Do?" (Matrix Loops & String Encryptions)
- **Class 4**: Contest 1 Programming Architecture & Mock Exam

---

<!-- _class: lead -->
# 🌟 Class 1
## Two's Complement Signed Representation

---

## Two's Complement: The Gold Standard

Why Two's Complement?
- Avoids negative zero (`+0` and `-0`).
- Hardware adder circuits can subtract simply by adding!

### How to Negate an $n$-bit Integer:
1. Write the positive number with leading zeros.
2. Invert all bits ($0 \leftrightarrow 1$).
3. Add $1$.

**Shortcut**: From right to left, keep all zeros and the very first `1` unchanged. Invert all bits to the left of that `1`!

---

## Example: Find $-43_{10}$ in 8-bit Two's Complement

1. $+43_{10} = 00101011_2$
2. Invert all bits:

   $\displaystyle \sim (00101011) = 11010100$

3. Add 1:

   $\displaystyle 11010100 + 1 = \mathbf{11010101_2} = \mathbf{D5_{16}}$

### Decoding Negative Two's Complement:
- If MSB is `1`, it is negative.
- Positional weight of MSB is $-2^{n-1}$ ($-128$ for 8-bit).
- Value of $\text{D}5_{16} = -128 + 64 + 16 + 4 + 1 = \mathbf{-43_{10}}$.

---

<!-- _class: lead -->
# 🌟 Class 2
## Nested Recursion & Cycle Recognition

---

## Tackling Nested Recursive Calls

$$
f(x) = \begin{cases} x - 3 & \text{if } x > 20 \\ f(f(x + 5)) & \text{if } x \le 20 \end{cases}
$$

### Speed Strategy:
1. Don't trace blindly from $f(12)$!
2. Compute known values just above the threshold:
   - $f(21)=18, f(22)=19, f(23)=20, f(24)=21, f(25)=22$.
3. Compute backwards near the boundary:
   - $f(20) = f(f(25)) = f(22) = 19$.
   - $f(19) = f(f(24)) = f(21) = 18$.
   - $f(18) = f(f(23)) = f(20) = 19$.
4. **Identify the Invariant**: Even inputs yield 19, odd yield 18!

   $\displaystyle \mathbf{f(12) = 19}$

---

<!-- _class: lead -->
# 🌟 Class 3
## Intermediate Pseudocode Tracing

---

## 2D Matrix Anti-Diagonal & State Changes

```basic
DIM M(3, 3)
FOR I = 1 TO 3
  FOR J = 1 TO 3
    M(I, J) = (I * J) MOD 4
  NEXT J
NEXT I
```

| $I \setminus J$ | $J=1$ | $J=2$ | $J=3$ |
| :---: | :---: | :---: | :---: |
| **$I=1$** | $1 \pmod 4 = 1$ | $2 \pmod 4 = 2$ | $3 \pmod 4 = 3$ |
| **$I=2$** | $2 \pmod 4 = 2$ | $4 \pmod 4 = 0$ | $6 \pmod 4 = 2$ |
| **$I=3$** | $3 \pmod 4 = 3$ | $6 \pmod 4 = 2$ | $9 \pmod 4 = 1$ |

Anti-diagonal: $M(1,3) + M(2,2) + M(3,1) = 3 + 0 + 3 = \mathbf{6}$.

---

<!-- _class: lead -->
# 🌟 Class 4
## Contest 1 Programming Problem Strategy

---

## Contest 1 Programming: Common Archetypes

1. **Base Converter Engine**:
   - Parse input number string (careful with fractions!).
   - Convert to decimal floating point or fraction.
   - Convert to target base with custom digit alphabet `"0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ"`.
2. **Key Python Snippet**:
   ```python
   def int_to_base(n, b):
       if n == 0: return "0"
       digits = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ"
       res = []
       while n > 0:
           res.append(digits[n % b])
           n //= b
       return "".join(reversed(res))
   ```
