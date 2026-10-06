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
  h1 { color: #311b92; }
  h2 { color: #4527a0; }
  code { background: #ede7f6; color: #311b92; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 3: Junior Division
## Boolean Laws, Stacks, Queues & BST
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Junior Syllabus Matrix

- **Class 1**: Boolean Laws, De Morgan's & Factoring
- **Class 2**: Boolean Simplification & 3-Variable Truth Sets
- **Class 3**: Stacks, Queues & Binary Search Tree Traversals
- **Class 4**: Pseudocode Data Structures & Contest 3 Mock Exam

---

<!-- _class: lead -->
# 🌟 Class 1
## The Essential Boolean Laws

---

## Must-Memorize Boolean Laws

- **De Morgan's**:

  $\displaystyle \overline{A \cdot B} = \overline{A} + \overline{B} \quad \text{and} \quad \overline{A + B} = \overline{A} \cdot \overline{B}$

- **Absorption**:

  $\displaystyle A + A B = A \quad \text{and} \quad A(A + B) = A$

  $\displaystyle \mathbf{A + \overline{A} B = A + B}$

- **The Secret Distributive Law**:

  $\displaystyle \mathbf{A + B C = (A + B)(A + C)}$

---

<!-- _class: lead -->
# 🌟 Class 3
## BST Traversals: Inorder, Preorder, Postorder

---

## 3 Ways to Traverse a Tree

```text
         F
       /   \
      B     G
     / \     \
    A   D     I
```

1. **Inorder (Left - Root - Right)**:

   $\displaystyle \mathbf{A, B, D, F, G, I} \quad \text{(Always Alphabetical!)}$

2. **Preorder (Root - Left - Right)**:

   $\displaystyle \mathbf{F, B, A, D, G, I}$

3. **Postorder (Left - Right - Root)**:

   $\displaystyle \mathbf{A, D, B, I, G, F}$
