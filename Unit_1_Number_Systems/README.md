# Unit 1: Computer Number Systems & Recursive Functions

## 📌 Unit Overview
Unit 1 corresponds to **ACSL Contest 1**. The core focus is mastering how computers store, convert, and calculate numbers in different bases, understanding recursive function evaluation, and deciphering program control flow in "What Does This Program Do?".

---

## 🎯 Division Specific Focus & Matrix

| Feature / Topic | Elementary Division | Junior Division | Intermediate Division |
| :--- | :--- | :--- | :--- |
| **Number Bases** | Binary (2), Octal (8), Decimal (10), Hexadecimal (16) | Bases 2, 8, 10, 16, and arbitrary base $b$ | Bases 2 to 16, fractional bases, negative representations |
| **Base Conversions** | Direct positional expansion, 3-bit / 4-bit grouping | Multi-step conversions, base $A \rightarrow 10 \rightarrow B$, fractions | Signed Two's Complement, floating-point approximations |
| **Base Arithmetic** | Binary addition & subtraction | Addition & subtraction in Bases 2, 8, 16 | Arithmetic in arbitrary bases, signed overflow |
| **Recursion** | Not in Elementary Contest | Single recursive functions, base case identification | Nested recursion, multiple parameters, memoization |
| **Pseudocode** | Sequential statements, IF-THEN-ELSE, simple FOR loops | Loops with step, nested conditionals, 1D arrays | Multi-dimensional arrays, string functions, nested loops |
| **Programming Contest** | N/A (Short answers only) | 1 problem (HackerRank) | 1 problem (Advanced HackerRank) |

---

## 📁 Subfolders & Level Curricula

- **[Elementary Division Curriculum (4 × 90 Mins)](./elementary/README.md)**
  - Resources: **[Homework Sets & Solutions](./elementary/homework.md)** | **[Markdown Slides](./elementary/slides.md)** | **[PowerPoint Deck (.pptx)](./elementary/slides.pptx)**
  - Class 1: The Magic of Base 2: Binary Counting, Powers of 2 & Decimal-Binary Conversions.
  - Class 2: Octal & Hexadecimal: The 3-Bit and 4-Bit Grouping Shortcuts.
  - Class 3: Computer Arithmetic: Binary Addition, Subtraction & Carry Operations.
  - Class 4: "What Does This Program Do?" (Trace Tables & Flow Control) + Contest 1 Mock Test.
- **[Junior Division Curriculum (4 × 90 Mins)](./junior/README.md)**
  - Resources: **[Homework Sets & Solutions](./junior/homework.md)** | **[Markdown Slides](./junior/slides.md)** | **[PowerPoint Deck (.pptx)](./junior/slides.pptx)**
  - Class 1: Base Conversions in Arbitrary Bases ($b=2 \dots 16$) & Fractional Conversions.
  - Class 2: Arithmetic Operations in Bases 2, 8, and 16.
  - Class 3: Recursive Functions: Tracing Call Stacks and Tree Diagrams.
  - Class 4: "What Does This Program Do?" (Junior Pseudocode) & Contest 1 Mock Exam.
- **[Intermediate Division Curriculum (4 × 90 Mins)](./intermediate/README.md)**
  - Resources: **[Homework Sets & Solutions](./intermediate/homework.md)** | **[Markdown Slides](./intermediate/slides.md)** | **[PowerPoint Deck (.pptx)](./intermediate/slides.pptx)**
  - Class 1: Advanced Number Systems: Fractional Bases, Two's Complement & Signed Representation.
  - Class 2: Complex Recursion: Nested Calls, Double Recurrence & Execution Tracing.
  - Class 3: Intermediate Pseudocode Tracing (Strings, Arrays & State Machines).
  - Class 4: Contest 1 Programming Problem Strategies (Python/Java) + Timed Mock Contest.

---

## 💡 Key Teacher Tips & Speed Strategies for Contest 1
1. **The Power-of-2 Memory Bank**: Make students memorize $2^0$ through $2^{10}$ ($1, 2, 4, 8, 16, 32, 64, 128, 256, 512, 1024$).
2. **The Hex Table**: Have students immediately write down `A=10, B=11, C=12, D=13, E=14, F=15` on their scrap paper at the start of the contest.
3. **Grouping Strategy**: Never convert Octal to Hex through Decimal! Always use Binary as the stepping stone: $\text{Octal} \leftrightarrow \text{Binary (3 bits)} \leftrightarrow \text{Hex (4 bits)}$.
