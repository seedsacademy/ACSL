# Unit 2: Bit-String Flicking & Prefix / Infix / Postfix Notation

## 📌 Unit Overview
Unit 2 corresponds to **ACSL Contest 2**. This unit covers two distinct fundamental computer science concepts:
1. **Bit-String Flicking**: Low-level bitwise manipulation using logic operators (`NOT`, `AND`, `OR`, `XOR`) and shifting/rotating operations (`LSHIFT`, `RSHIFT`, `LCIRC`, `RCIRC`).
2. **Prefix / Infix / Postfix Notation**: Expression representation and stack-based parsing (Polish Notation and Reverse Polish Notation).
3. **"What Does This Program Do?"**: Contest 2 pseudocode questions focusing on string manipulation, loops, and conditional logic.

---

## 🎯 Division Specific Focus & Matrix

| Topic / Feature | Elementary Division | Junior Division | Intermediate Division |
| :--- | :--- | :--- | :--- |
| **Prefix & Postfix** | Simple binary operators (`+`, `-`, `*`, `/`), basic stack evaluation | Full arithmetic expressions (`^`, `*`, `/`, `+`, `-`), Infix $\leftrightarrow$ Postfix/Prefix | Expressions with unary minus, relational operators, full parse trees |
| **Bit-String Operations** | Concept of bits, simple `AND` / `OR` / `NOT` | `NOT`, `AND`, `OR`, `XOR`, `LSHIFT-k`, `RSHIFT-k`, `LCIRC-k`, `RCIRC-k` | Complex bit equations with unknown variable $X$, masks, length constraints |
| **Order of Operations** | Parentheses first, left-to-right | `NOT` $\rightarrow$ Shifts/Circs $\rightarrow$ `AND` $\rightarrow$ `XOR` $\rightarrow$ `OR` | Strict formal precedence, associativity, bit-equation systems |
| **Pseudocode** | String length, character extraction, simple count loops | String functions (`MID$`, `LEFT$`, `RIGHT$`), character replacement | Substring search, multi-array index mapping, nested string algorithms |
| **Programming Contest** | N/A | 1 problem (HackerRank) | 1 problem (Advanced HackerRank) |

---

## 📁 Subfolders & Level Curricula

- **[Elementary Division Curriculum (4 × 90 Mins)](./elementary/README.md)**
  - Resources: **[Homework Sets & Solutions](./elementary/homework.md)** | **[Markdown Slides](./elementary/slides.md)** | **[PowerPoint Deck (.pptx)](./elementary/slides.pptx)**
  - Class 1: Introduction to Prefix and Postfix: Why Order Matters.
  - Class 2: Evaluating Prefix & Postfix Expressions (The Visual Underline / Tree Method).
  - Class 3: Converting Between Infix, Prefix, and Postfix.
  - Class 4: "What Does This Program Do?" (String Concatenation & Loops) + Contest 2 Mock Test.
- **[Junior Division Curriculum (4 × 90 Mins)](./junior/README.md)**
  - Resources: **[Homework Sets & Solutions](./junior/homework.md)** | **[Markdown Slides](./junior/slides.md)** | **[PowerPoint Deck (.pptx)](./junior/slides.pptx)**
  - Class 1: Bit-String Flicking Fundamentals: `NOT`, `AND`, `OR`, `XOR` & Precedence Rules.
  - Class 2: Shifting & Rotating: `LSHIFT`, `RSHIFT`, `LCIRC`, `RCIRC` & Solving Bit Equations.
  - Class 3: Prefix/Postfix Mastery: Infix Conversion & Stack Evaluation.
  - Class 4: "What Does This Program Do?" (String Functions) & Contest 2 Mock Exam.
- **[Intermediate Division Curriculum (4 × 90 Mins)](./intermediate/README.md)**
  - Resources: **[Homework Sets & Solutions](./intermediate/homework.md)** | **[Markdown Slides](./intermediate/slides.md)** | **[PowerPoint Deck (.pptx)](./intermediate/slides.pptx)**
  - Class 1: Advanced Bit-String Equations: Solving for Unknown Strings of Length $n$.
  - Class 2: Advanced Prefix/Postfix: Unary Operators, Exponents & Relational Expressions.
  - Class 3: Intermediate Pseudocode Tracing (String Parsing & Dynamic Encodings).
  - Class 4: Contest 2 Programming Problem (String Parsing / Expression Evaluators) + Timed Mock Contest.

---

## 💡 Official ACSL Precedence Hierarchy (Must Memorize!)

### Bit-String Flicking Precedence:
1. Expressions inside parentheses `(...)`
2. `NOT`
3. `LSHIFT-k`, `RSHIFT-k`, `LCIRC-k`, `RCIRC-k` (evaluated left-to-right if multiple)
4. `AND`
5. `XOR`
6. `OR`
