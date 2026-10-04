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
  h1 { color: #004d40; }
  h2 { color: #00796b; }
  code { background: #e0f2f1; color: #004d40; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
---

# 🚀 ACSL Contest 4: Junior Division
## Eulerian Graphs & Digital Logic Circuits
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Junior Syllabus Matrix

- **Class 1**: Adjacency Matrices & Eulerian Circuits / Paths
- **Class 2**: The 7 Standard Digital Logic Gates & Circuit Tracing
- **Class 3**: Circuit Minimization with Boolean Algebra
- **Class 4**: Graph Pseudocode & Contest 4 Mock Exam

---

<!-- _class: lead -->
# 🌟 Class 1
## Euler's Famous Graph Theorems

---

## Eulerian Circuit vs. Eulerian Path

| Type | Definition | Condition (Connected Graph) |
| :--- | :--- | :--- |
| **Eulerian Circuit** | Traverses every edge once; **starts & ends at same vertex** | **ALL** vertices have **EVEN** degree |
| **Eulerian Trail/Path** | Traverses every edge once; **starts & ends at different vertices** | Exactly **TWO** vertices have **ODD** degree |

*Tutor Tip: The path MUST start at one of the odd vertices and terminate at the other!*

---

<!-- _class: lead -->
# 🌟 Class 2
## The 7 Digital Logic Gates

---

## Logic Gate Symbol Recognition

- **AND**: Curved front, flat back ($A \cdot B$)
- **OR**: Pointed front, curved back ($A + B$)
- **NOT**: Triangle with inversion bubble ($\overline{A}$)
- **XOR**: Pointed front, double curved back ($A \oplus B$)
- **NAND**: AND gate with bubble ($\overline{A \cdot B}$)
- **NOR**: OR gate with bubble ($\overline{A + B}$)
- **XNOR**: XOR gate with bubble ($\overline{A \oplus B}$)
