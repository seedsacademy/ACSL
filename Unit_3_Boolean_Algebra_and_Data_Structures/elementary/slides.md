---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #ffffff
color: #1a1a2e
style: |
  section {
    font-family: 'Segoe UI', Arial, sans-serif;
    padding: 40px;
  }
  h1 { color: #283593; }
  h2 { color: #3949ab; }
  code { background: #e8eaf6; color: #283593; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
---

# 🚀 ACSL Contest 3: Elementary Division
## Boolean Logic & Binary Search Trees
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Unit 3 Elementary Roadmap

- **Class 1**: True, False, NOT, AND, OR & Truth Tables
- **Class 2**: Evaluating Compound Boolean Expressions
- **Class 3**: Intro to Binary Search Trees (BST Rules)
- **Class 4**: Logic in Pseudocode & Contest 3 Mock Exam

---

<!-- _class: lead -->
# 🌟 Class 1
## The 3 Logic Gates

---

## Truth Tables: NOT, AND, OR

| $A$ | $B$ | $\text{NOT } A$ | $A \text{ AND } B$ ($A \cdot B$) | $A \text{ OR } B$ ($A + B$) |
| :---: | :---: | :---: | :---: | :---: |
| 0 | 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 0 | 0 | 1 |
| 1 | 1 | 0 | 1 | 1 |

- **NOT**: The opposite flipper!
- **AND**: Both must be 1.
- **OR**: At least one must be 1.

---

<!-- _class: lead -->
# 🌟 Class 3
## Binary Search Trees (BST)

---

## The BST Golden Rule

When inserting a new node:
- If **Smaller** than current node $\rightarrow$ go **LEFT**
- If **Larger** than current node $\rightarrow$ go **RIGHT**

```text
Insert [50, 30, 70, 20, 40]

         50 (Root)
       /    \
     30      70
    /  \
  20    40
```
- **Root**: 50
- **Leaves**: 20, 40, 70
