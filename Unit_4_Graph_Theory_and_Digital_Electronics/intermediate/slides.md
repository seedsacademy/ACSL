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
  h1 { color: #bf360c; }
  h2 { color: #d84315; }
  code { background: #fbe9e7; color: #bf360c; padding: 2px 6px; border-radius: 4px; }
  .highlight { background-color: #fff9c4; padding: 2px 8px; border-radius: 4px; }
  footer { font-size: 0.5em; color: #78909c; }
-->

# 🚀 ACSL Contest 4: Intermediate Division
## Matrix Powers, Adders & ACSL Assembly
### 4-Class Master Slide Deck (4 × 90 Minutes)

---

## 📌 Intermediate Syllabus Matrix

- **Class 1**: Matrix Powers ($A^k$), Walks of Length $k$ & Planarity ($V-E+F=2$)
- **Class 2**: Half-Adders, Full-Adders & Combinational Synthesis
- **Class 3**: Official ACSL Assembly Language Emulation
- **Class 4**: Contest 4 Programming Challenge & Final Comprehensive Mock

---

<!-- _class: lead -->
# 🌟 Class 1
## The Matrix Power Walk Theorem

---

## Matrix Powers Count Walks!

If $A$ is the $0/1$ adjacency matrix of graph $G$:

$$(A^k)_{i, j} = \text{The exact number of walks of length } k \text{ from vertex } i \text{ to vertex } j$$

### Special Diagonal Property:
$$(A^2)_{i, i} = \text{deg}(v_i)$$
*(In an undirected graph with no self-loops, the diagonal of $A^2$ gives the degree of each vertex!)*

---

<!-- _class: lead -->
# 🌟 Class 2
## Digital Adders

---

## Half-Adder vs. Full-Adder

### Half-Adder (Adds 2 bits $A, B$):
- $\mathbf{\text{Sum } S = A \oplus B}$
- $\mathbf{\text{Carry } C = A \cdot B}$

### Full-Adder (Adds 3 bits $A, B, C_{in}$):
- $\mathbf{\text{Sum } S = A \oplus B \oplus C_{in}}$
- $\mathbf{\text{Carry-out } C_{out} = A B + C_{in}(A \oplus B)}$

*Physical hardware uses 2 Half-Adders and 1 OR gate to make 1 Full-Adder!*

---

<!-- _class: lead -->
# 🌟 Class 3
## Official ACSL Assembly Language

---

## The ACSL Assembly Opcodes

| Opcode | Meaning | Action |
| :--- | :--- | :--- |
| `LOAD X` | Load | $\text{ACC} = X$ |
| `STORE X`| Store | $\text{memory}[X] = \text{ACC}$ |
| `ADD X`  | Add | $\text{ACC} = \text{ACC} + X$ |
| `SUB X`  | Subtract | $\text{ACC} = \text{ACC} - X$ |
| `MULT X` | Multiply | $\text{ACC} = \text{ACC} \times X$ |
| `DIV X`  | Integer Divide | $\text{ACC} = \text{ACC} // X$ |
| `BG LABEL`| Branch if Greater | Jump if $\text{ACC} > 0$ |
| `BE LABEL`| Branch if Equal | Jump if $\text{ACC} = 0$ |
| `BL LABEL`| Branch if Less | Jump if $\text{ACC} < 0$ |
| `BU LABEL`| Branch Unconditional | Always jump |
