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
  h1 { color: #880e4f; }
  h2 { color: #ad1457; }
  code { background: #fce4ec; color: #880e4f; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
---

# 🚀 ACSL Contest 3: Intermediate Division
## Karnaugh Maps, Tree Theorems & Priority Queues
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Intermediate Syllabus Matrix

- **Class 1**: 3 & 4-Variable Karnaugh Maps (K-Maps) Minimization
- **Class 2**: Tree Properties ($L = I + 1$), BST Deletions & Binary Heaps
- **Class 3**: "What Does This Program Do?" (Array-Based Tree Traversal)
- **Class 4**: Contest 3 Programming Blueprint (BST Rebuilding)

---

<!-- _class: lead -->
# 🌟 Class 1
## 4-Variable Karnaugh Maps

---

## The Gray Code Grid ($AB$ rows, $CD$ columns)

Notice: Only **1 bit changes** between adjacent rows/columns!

```text
           CD
       00  01  11  10
    +-----------------
 00 |  m0  m1  m3  m2
AB 01 |  m4  m5  m7  m6
 11 | m12 m13 m15 m14
 10 |  m8  m9 m11 m10
```

🔥 **The 4 Corners Trick**:
$m_0 (0000), m_2 (0010), m_8 (1000), m_{10} (1010)$ form a valid group of 4!
- Invariant bits: $B=0$ and $D=0 \implies \mathbf{\overline{B} \ \overline{D}}$.

---

<!-- _class: lead -->
# 🌟 Class 2
## Tree Theorems & Formulas

---

## 3 Golden Formulas for Strictly Binary Trees

In any tree where every node has either 0 or 2 children:

1. **Leaves vs. Internals**:
   $$\mathbf{L = I + 1}$$
2. **Total Nodes ($N$)**:
   $$\mathbf{N = 2I + 1 = 2L - 1}$$
3. **Maximum Nodes for Height $h$**:
   $$\mathbf{N_{max} = 2^{h+1} - 1}$$

*Contest Speed Trick: If a problem says "strictly binary tree with 50 leaves", instantly internal nodes $I = 49$ and total nodes $N = 99$!*
