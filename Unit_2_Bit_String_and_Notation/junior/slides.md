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
  h1 { color: #00695c; }
  h2 { color: #00897b; }
  code { background: #e0f2f1; color: #00695c; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 2: Junior Division
## Bit-String Flicking & Expression Parsing
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Junior Syllabus Matrix

- **Class 1**: Bit-String Flicking Fundamentals & Precedence
- **Class 2**: Shifts, Circular Rotates & Solving Equations for $X$
- **Class 3**: Infix $\leftrightarrow$ Postfix / Prefix & Stack Evaluation
- **Class 4**: Pseudocode String Transforms & Contest 2 Mock Exam

---

<!-- _class: lead -->
# 🌟 Class 1
## The Bit-String Flicking Rules

---

## 4 Bitwise Operators

Operate bit-by-bit simultaneously on strings of the same length:

| $A$ | $B$ | $\text{NOT } A$ | $A \text{ AND } B$ | $A \text{ OR } B$ | $A \text{ XOR } B$ |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 1 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 | 1 | 0 |

🔥 **ACSL Official Precedence**:

$$
\mathbf{(Parentheses) \rightarrow NOT \rightarrow AND \rightarrow XOR \rightarrow OR}
$$

---

<!-- _class: lead -->
# 🌟 Class 2
## Shifting, Rotating & Equations

---

## Shifts vs. Circular Rotates (Length 5)

Let $B = \mathbf{10110}$:

- $\mathbf{LSHIFT-2}(10110) = \mathbf{11000}$
  *(Pushes in zeros from right; discards left 2 bits)*
- $\mathbf{RSHIFT-2}(10110) = \mathbf{00101}$
  *(Pushes in zeros from left; discards right 2 bits)*
- $\mathbf{LCIRC-2}(10110) = \mathbf{11010}$
  *(First 2 bits wrap around to the back)*
- $\mathbf{RCIRC-2}(10110) = \mathbf{10101}$
  *(Last 2 bits wrap around to the front)*

---

## Solving Bit Equations: Example

Find all 5-bit strings $X$ that satisfy:

$$
(\text{LSHIFT-1 } X) \text{ AND } 10110 = 00100
$$

1. Let $X = x_1 x_2 x_3 x_4 x_5$.
2. $\text{LSHIFT-1 } X = x_2 x_3 x_4 x_5 0$.
3. Bit comparison with $10110$:
   - Bit 1: $x_2 \land 1 = 0 \implies x_2 = \mathbf{0}$
   - Bit 2: $x_3 \land 0 = 0 \implies x_3 = \mathbf{*}$ (can be 0 or 1)
   - Bit 3: $x_4 \land 1 = 1 \implies x_4 = \mathbf{1}$
   - Bit 4: $x_5 \land 1 = 0 \implies x_5 = \mathbf{0}$
   - Bit 5: $0 \land 0 = 0$ (Holds)
   - $x_1$ was shifted away: $x_1 = \mathbf{*}$!
4. **Result**: $X = *0*10 \implies \mathbf{4 \text{ solutions}}$ ($00010, 00110, 10010, 10110$).
