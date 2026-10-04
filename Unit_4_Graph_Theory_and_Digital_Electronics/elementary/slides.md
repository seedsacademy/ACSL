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
  h2 { color: #00695c; }
  code { background: #e0f2f1; color: #004d40; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
---

# 🚀 ACSL Contest 4: Elementary Division
## Graph Theory Foundations
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Unit 4 Elementary Roadmap

- **Class 1**: Vertices, Edges & Directed vs Undirected Graphs
- **Class 2**: Degrees of Vertices & The Magic Handshaking Lemma
- **Class 3**: Walks, Paths, Cycles & Adjacency Lists
- **Class 4**: Graph Grids in Pseudocode & Contest 4 Mock Exam

---

<!-- _class: lead -->
# 🌟 Class 1 & 2
## The Handshaking Lemma

---

## The Handshaking Lemma

$$\sum \text{deg}(v) = 2 \times E$$

- **Degree**: Number of edges connected to a vertex.
- **Why $2 \times E$?**
  - Every edge has **2 endpoints**!
  - Each edge adds 1 to the degree of two vertices.

🔥 **The Big Rule**:
**The sum of all degrees in any graph is ALWAYS EVEN!**
*(If a question gives an odd sum, the graph is impossible!)*
