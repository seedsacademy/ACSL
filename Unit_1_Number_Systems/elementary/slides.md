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
  h1 { color: #0d47a1; }
  h2 { color: #1565c0; }
  code { background: #f0f4f8; color: #d32f2f; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 1: Elementary Division
## Computer Number Systems & Program Logic
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Unit 1 Curriculum Roadmap

- **Class 1**: The Magic of Base 2 (Binary & Decimal Conversions)
- **Class 2**: Octal & Hexadecimal (3-Bit and 4-Bit Grouping Secrets)
- **Class 3**: Computer Arithmetic (Binary Addition & Borrowing)
- **Class 4**: "What Does This Program Do?" (Trace Tables & Mock Contest)

---

<!-- _class: lead -->
# 🌟 Class 1
## The Magic of Base 2 (Binary & Decimal)

---

## Why Do Computers Use Binary?

- Inside a computer CPU are billions of microscopic **transistors**.
- Each transistor acts like a **light switch**:
  - **OFF** = `0` (Low voltage)
  - **ON** = `1` (High voltage)
- A single `0` or `1` is called a **bit** (binary digit).
- A group of 8 bits is called a **byte**.

---

## Positional Notation: Base 10 vs. Base 2

### In Base 10 (Decimal):

$$
543 = 5 \times 10^2 + 4 \times 10^1 + 3 \times 10^0 = 500 + 40 + 3
$$

### In Base 2 (Binary):
Each position is a **Power of 2**!

| $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ |
| :---: | :---: | :---: | :---: | :---: | :---: |
| **32** | **16** | **8** | **4** | **2** | **1** |

---

## 💡 Converting Binary $\rightarrow$ Decimal

### Worked Example: Convert $11011_2$ to Base 10

1. Align the bits with the powers of 2:

   $\displaystyle \begin{array}{ccccc} 16 & 8 & 4 & 2 & 1 \\ \mathbf{1} & \mathbf{1} & \mathbf{0} & \mathbf{1} & \mathbf{1} \end{array}$

2. Add the numbers that have a `1` underneath:

   $\displaystyle \text{Sum} = 16 + 8 + 0 + 2 + 1 = \mathbf{27_{10}}$

🎯 *Rule: If the bit is 1, take the weight. If 0, skip it!*

---

## 💡 Converting Decimal $\rightarrow$ Binary
### The "Largest Power of 2" Subtraction Trick

**Convert $53_{10}$ to Binary:**
1. Largest power $\le 53$ is **32**: $53 - 32 = 21 \implies \text{bit } 32 = \mathbf{1}$
2. Largest power $\le 21$ is **16**: $21 - 16 = 5 \implies \text{bit } 16 = \mathbf{1}$
3. Does **8** fit into 5? No! $\implies \text{bit } 8 = \mathbf{0}$
4. Largest power $\le 5$ is **4**: $5 - 4 = 1 \implies \text{bit } 4 = \mathbf{1}$
5. Does **2** fit into 1? No! $\implies \text{bit } 2 = \mathbf{0}$
6. Largest power $\le 1$ is **1**: $1 - 1 = 0 \implies \text{bit } 1 = \mathbf{1}$

**Result: $110101_2$**

---

<!-- _class: lead -->
# 🌟 Class 2
## Octal & Hexadecimal Grouping Tricks

---

## The Hexadecimal Letters
Because base 16 needs 16 single symbols, we use letters for values 10 to 15:

$$
\mathbf{A = 10} \quad \mathbf{B = 11} \quad \mathbf{C = 12}
$$

$$
\mathbf{D = 13} \quad \mathbf{E = 14} \quad \mathbf{F = 15}
$$

⚡ *Tutor Speed Tip: Always write A=10 through F=15 at the top of your test sheet immediately!*

---

## The Magical Grouping Rule

- $2^3 = 8 \implies$ **1 Octal digit = 3 Binary bits**
- $2^4 = 16 \implies$ **1 Hexadecimal digit = 4 Binary bits**

### Converting Binary $\rightarrow$ Octal:
Group into sets of **3 bits from right to left**!

$$
11010110_2 \rightarrow (011)(010)(110)_2 = \mathbf{326_8}
$$

### Converting Binary $\rightarrow$ Hexadecimal:
Group into sets of **4 bits from right to left**!

$$
11010110_2 \rightarrow (1101)(0110)_2 = \mathbf{D6_{16}}
$$

---

## The "Binary Bridge" (Octal $\leftrightarrow$ Hex)

**Never convert Octal to Hex through Base 10!** Always use Binary in between:

$$
\text{Octal} \xleftrightarrow{\text{Group by 3}} \text{Binary} \xleftrightarrow{\text{Group by 4}} \text{Hexadecimal}
$$

### Example: Convert $75_8$ to Hexadecimal
1. Convert each octal digit to 3 bits:

   $\displaystyle 7 \rightarrow 111, \quad 5 \rightarrow 101 \implies 111101_2$

2. Regroup into 4 bits from the right:

   $\displaystyle (0011)(1101)_2 = 3 \quad \text{D} \implies \mathbf{3D_{16}}$

---

<!-- _class: lead -->
# 🌟 Class 3
## Computer Arithmetic (Binary Addition)

---

## Binary Addition Rules

$$\begin{aligned}
0 + 0 &= 0 \\
0 + 1 &= 1 \\
1 + 1 &= 10_2 \quad (\text{0 with carry 1}) \\
1 + 1 + 1 &= 11_2 \quad (\text{1 with carry 1})
\end{aligned}$$

*Think: In decimal, $9 + 1 = 10$. In binary, $1 + 1 = 10_2$!*

---

## Binary Addition: Step-by-Step

Add: $101101_2 + 11011_2$

```text
    1  1  1  1  1     <-- Carries
    1  0  1  1  0  1  (= 45)
 +  0  1  1  0  1  1  (= 27)
 --------------------
 1  0  0  1  0  0  0  (= 72)
```

**Check with Decimal:**
$45 + 27 = 72$. $64 + 8 = 72$. Perfect match!

---

<!-- _class: lead -->
# 🌟 Class 4
## "What Does This Program Do?" & Trace Tables

---

## How to Build a Trace Table

Never do code execution in your head! Always draw a **Trace Table**:

```basic
10 X = 2
20 FOR K = 1 TO 3
30   X = X * 2 + 1
40 NEXT K
50 PRINT X
```

| Step / Loop | Formula | $X$ Value |
| :---: | :---: | :---: |
| Initial | `X = 2` | 2 |
| $K = 1$ | $2 \times 2 + 1$ | 5 |
| $K = 2$ | $5 \times 2 + 1$ | 11 |
| $K = 3$ | $11 \times 2 + 1$ | **23** |

---

## Contest Day Tips for ACSL Contest 1

1. **Powers of 2 Checklist**: Write down $1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024$.
2. **Padding Zeros**: When grouping bits for Octal/Hex, always add leading zeros to the **left** of the integer.
3. **Double-Check Arithmetic**: Verify your binary addition by quickly converting to decimal and back.
4. **Trace Every Line**: In pseudocode questions, update one variable at a time on your scratch paper!
