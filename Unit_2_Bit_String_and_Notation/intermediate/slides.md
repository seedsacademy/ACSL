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
  h1 { color: #4a148c; }
  h2 { color: #6a1b9a; }
  code { background: #f3e5f5; color: #4a148c; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 2: Intermediate Division
## Advanced Bit Equations & Expression Trees
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Intermediate Syllabus Matrix

- **Class 1**: Advanced Bit-String Equations & Unknown Masks
- **Class 2**: Prefix/Postfix with Unary Minus (`@`) & Relational Operators
- **Class 3**: "What Does This Program Do?" (String Parsing & Prefix Sums)
- **Class 4**: Contest 2 Programming Blueprint (Stack Evaluators)

---

<!-- _class: lead -->
# 🌟 Class 1
## Advanced Bit-String Equations

---

## Modulo Reduction for Shifts & Circs

For any string of length $n$:

$$
\text{LCIRC-}k = \text{LCIRC-}(k \bmod n)
$$

$$
\text{RCIRC-}k = \text{RCIRC-}(k \bmod n)
$$

### Example: Length 5 String

$$
\text{LCIRC-13 } (10110) = \text{LCIRC-}(13 \bmod 5) = \text{LCIRC-3 } (10110) = \mathbf{10101}
$$

---

<!-- _class: lead -->
# 🌟 Class 2
## Unary Minus & Relational Operators

---

## Unary Operator `@` and Booleans in Expressions

ACSL frequently uses `@` for **Unary Minus** (single operand) and relational operators ($<, >, =$):

$$
{}+ \ * \ > \ 5 \ 3 \ 4 \ @ \ 6
$$

1. Notice $> \ 5 \ 3 \implies 5 > 3$ is **True (1)**.
2. Notice $@ \ 6 \implies \mathbf{-6}$.
3. Expression: $+ \ * \ 1 \ 4 \ (-6)$
4. $* \ 1 \ 4 \implies 4$.
5. $+ \ 4 \ (-6) \implies \mathbf{-2}$.

---

<!-- _class: lead -->
# 🌟 Class 3 & 4
## Contest 2 Programming Problem Strategy

---

## Stack-Based Postfix Evaluator Engine

```python
def eval_postfix(tokens):
    stack = []
    for t in tokens:
        if t.isdigit():
            stack.append(int(t))
        elif t == '@':
            stack.append(-stack.pop())
        else:
            b, a = stack.pop(), stack.pop()
            if t == '+': stack.append(a + b)
            elif t == '-': stack.append(a - b)
            elif t == '*': stack.append(a * b)
            elif t == '/': stack.append(int(a / b))
            elif t == '^': stack.append(a ** b)
    return stack[0]
```
