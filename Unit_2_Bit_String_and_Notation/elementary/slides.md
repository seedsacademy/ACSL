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
  h1 { color: #e65100; }
  h2 { color: #f57c00; }
  code { background: #fff3e0; color: #e65100; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 2: Elementary Division
## Prefix & Postfix Notations
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Unit 2 Elementary Roadmap

- **Class 1**: Intro to Polish & Reverse Polish Notations
- **Class 2**: Evaluating Compound Prefix & Postfix Expressions
- **Class 3**: Converting Infix $\leftrightarrow$ Prefix/Postfix
- **Class 4**: String Loops in Pseudocode & Contest 2 Mock Exam

---

<!-- _class: lead -->
# 🌟 Class 1
## What is Prefix and Postfix?

---

## The Three Mathematical Notations

Every math expression has **operands** (numbers) and **operators** ($+, -, *, /$):

1. **Infix**: Operator in the middle
   $$3 + 4$$
2. **Prefix (Polish)**: Operator in front
   $$+ \ 3 \ 4$$
3. **Postfix (Reverse Polish)**: Operator in the back
   $$3 \ 4 \ +$$

*All three evaluate to 7!*

---

## ⚠️ Warning: Division & Subtraction Order

In addition and multiplication, order doesn't change the answer ($3+4 = 4+3$).
**In subtraction and division, ORDER MATTERS!**

$$\begin{aligned}
- \ 8 \ 3 &\implies 8 - 3 = \mathbf{5} \\
8 \ 3 \ - &\implies 8 - 3 = \mathbf{5} \\
/ \ 12 \ 4 &\implies 12 / 4 = \mathbf{3} \\
12 \ 4 \ / &\implies 12 / 4 = \mathbf{3}
\end{aligned}$$

*Rule: The FIRST number comes first in the calculation!*

---

<!-- _class: lead -->
# 🌟 Class 2
## The Underline Evaluation Method

---

## How to Evaluate Prefix: Scan Right $\rightarrow$ Left

Find the first operator immediately followed by two numbers:

$$+ \ * \ 2 \ 3 \ - \ 8 \ 4$$

1. Notice $- \ 8 \ 4 \implies 8 - 4 = \mathbf{4}$
   Expression: $+ \ * \ 2 \ 3 \ \mathbf{4}$
2. Notice $* \ 2 \ 3 \implies 2 \times 3 = \mathbf{6}$
   Expression: $+ \ \mathbf{6} \ \mathbf{4}$
3. Evaluate $+ \ 6 \ 4 = \mathbf{10}$

---

## How to Evaluate Postfix: Scan Left $\rightarrow$ Right

Find the first two numbers followed by an operator:

$$8 \ 2 \ / \ 5 \ * \ 3 \ -$$

1. First pair: $8 \ 2 \ / \implies 8 / 2 = \mathbf{4}$
   Expression: $\mathbf{4} \ 5 \ * \ 3 \ -$
2. Next pair: $4 \ 5 \ * \implies 4 \times 5 = \mathbf{20}$
   Expression: $\mathbf{20} \ 3 \ -$
3. Next pair: $20 \ 3 \ - \implies 20 - 3 = \mathbf{17}$

---

<!-- _class: lead -->
# 🌟 Class 3
## The Full Parenthesization Secret

---

## Converting Infix $\rightarrow$ Postfix in 2 Steps

**Problem: Convert $(A + B) * (C - D)$ to Postfix**

1. **Step 1**: Fully parenthesize by PEMDAS:
   $$((A + B) * (C - D))$$
2. **Step 2**: Move each operator to its **matching RIGHT parenthesis**:
   - $(A + B) \rightarrow (A \ B \ \mathbf{+})$
   - $(C - D) \rightarrow (C \ D \ \mathbf{-})$
   - $((AB+) * (CD-)) \rightarrow ((AB+) (CD-) \ \mathbf{*})$
3. Erase parentheses:
   $$\mathbf{A \ B \ + \ C \ D \ - \ *}$$
