# Unit 1: Elementary Division (4 Classes × 90 Minutes)

This curriculum prepares elementary students (Grades 3–6) for **ACSL Contest 1** (Computer Number Systems & "What Does This Program Do?").

---

## 📅 Class 1: The Magic of Base 2 (Binary & Decimal)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Why do computers only understand 1 and 0? (Light switch analogy).
- **0:15 – 0:45 (30 min)**: Core Concept: Place values in Base 10 vs. Base 2. Powers of 2 ($1, 2, 4, 8, 16, 32, 64$).
- **0:45 – 0:70 (25 min)**: Guided Practice: Converting Binary to Decimal (Expansion) and Decimal to Binary (Greedy Subtraction Method).
- **0:70 – 0:85 (15 min)**: Timed Speed Challenge: 5 rapid conversions.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework distribution.

### 🎯 Learning Objectives
1. Understand positional notation: place values represent powers of the base.
2. Convert any 6-bit binary string (e.g., $110101_2$) to decimal.
3. Convert any decimal number under 100 to binary using the "Largest Power of 2" subtraction method.

### 📘 Core Content & Worked Examples

#### Concept 1: Binary Place Values
In Base 10:

$$345 = 3 \times 10^2 + 4 \times 10^1 + 5 \times 10^0 = 300 + 40 + 5$$

In Base 2:

$$10110_2 = 1 \times 2^4 + 0 \times 2^3 + 1 \times 2^2 + 1 \times 2^1 + 0 \times 2^0 = 16 + 0 + 4 + 2 + 0 = 22_{10}$$

#### Worked Example 1: Convert $11011_2$ to Base 10
- Step 1: Write weights over bits:

  $$
  \begin{array}{ccccc} 16 & 8 & 4 & 2 & 1 \\ \mathbf{1} & \mathbf{1} & \mathbf{0} & \mathbf{1} & \mathbf{1} \end{array}
  $$

- Step 2: Sum the active weights: $16 + 8 + 0 + 2 + 1 = 27_{10}$.

#### Worked Example 2: Convert $53_{10}$ to Binary
- Largest power of 2 $\le 53$ is $32$: $53 - 32 = 21$ (Bit at 32 is 1).
- Largest power of 2 $\le 21$ is $16$: $21 - 16 = 5$ (Bit at 16 is 1).
- Next power is 8: $8 > 5$ (Bit at 8 is 0).
- Largest power of 2 $\le 5$ is $4$: $5 - 4 = 1$ (Bit at 4 is 1).
- Next power is 2: $2 > 1$ (Bit at 2 is 0).
- Largest power $\le 1$ is $1$: $1 - 1 = 0$ (Bit at 1 is 1).
- Result: $110101_2$.

### 📝 In-Class Exercises (with Solutions)
1. Convert $100111_2$ to decimal.  
   *Answer*: $32 + 4 + 2 + 1 = 39$.
2. Convert $75_{10}$ to binary.  
   *Answer*: $64 + 8 + 2 + 1 \rightarrow 1001011_2$.
3. What is the value of the largest 5-bit binary number?  
   *Answer*: $11111_2 = 2^5 - 1 = 31$.

### 🏠 Homework Assignment
- Convert to Decimal: (a) $10101_2$, (b) $111000_2$, (c) $1010101_2$.
- Convert to Binary: (a) 43, (b) 62, (c) 99.

---

## 📅 Class 2: Octal (Base 8) and Hexadecimal (Base 16)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Review Homework & Power-of-2 flashcards.
- **0:15 – 0:45 (30 min)**: Core Concept: Base 8 digits (0–7) and Base 16 digits (0–9, A–F). The 3-bit and 4-bit grouping trick.
- **0:45 – 0:70 (25 min)**: Guided Practice: Binary $\leftrightarrow$ Octal, Binary $\leftrightarrow$ Hex, Octal $\leftrightarrow$ Hex.
- **0:70 – 0:85 (15 min)**: In-Class Contest Simulation: Grouping speed drills.
- **0:85 – 0:90 (5 min)**: Review common errors (padding zeroes to the left).

### 🎯 Learning Objectives
1. Memorize hexadecimal letters: $A=10, B=11, C=12, D=13, E=14, F=15$.
2. Convert between Binary and Octal using 3-bit grouping.
3. Convert between Binary and Hexadecimal using 4-bit grouping.
4. Convert Octal to Hexadecimal via Binary without passing through Base 10.

### 📘 Core Content & Worked Examples

#### The Grouping Rule
- $2^3 = 8 \implies$ 1 Octal digit = exactly 3 Binary bits.
- $2^4 = 16 \implies$ 1 Hexadecimal digit = exactly 4 Binary bits.

| Hex / Dec | Binary (4-bit) | Hex / Dec | Binary (4-bit) |
| :--- | :--- | :--- | :--- |
| **0** | 0000 | **8** | 1000 |
| **1** | 0001 | **9** | 1001 |
| **2** | 0010 | **A (10)** | 1010 |
| **3** | 0011 | **B (11)** | 1011 |
| **4** | 0100 | **C (12)** | 1100 |
| **5** | 0101 | **D (13)** | 1101 |
| **6** | 0110 | **E (14)** | 1110 |
| **7** | 0111 | **F (15)** | 1111 |

#### Worked Example: Convert $110101101_2$ to Octal and Hex
- **To Octal (Group by 3 from right to left)**:
  $$(110)(101)(101)_2 = 6 \quad 5 \quad 5 = 655_8$$
- **To Hex (Group by 4 from right to left, pad left with zero)**:
  $$(0001)(1010)(1101)_2 = 1 \quad \text{A} \quad \text{D} = 1\text{AD}_{16}$$

#### Worked Example: Convert $57_8$ to Hexadecimal
- Step 1: Convert to binary: $5 \rightarrow 101$, $7 \rightarrow 111 \implies 101111_2$.
- Step 2: Regroup by 4: $(0010)(1111)_2 \implies 2\text{F}_{16}$.

### 📝 In-Class Exercises
1. Convert $2\text{B}_{16}$ to binary. (*Answer*: $0010\ 1011_2 = 101011_2$).
2. Convert $73_8$ to hex. (*Answer*: $73_8 = 111011_2 = 0011\ 1011_2 = 3\text{B}_{16}$).
3. Convert $1111010_2$ to octal. (*Answer*: $001\ 111\ 010_2 = 172_8$).

### 🏠 Homework Assignment
1. Convert $3\text{E}4_{16}$ to binary.
2. Convert $101101110010_2$ to octal and hexadecimal.
3. Convert $654_8$ to hexadecimal.

---

## 📅 Class 3: Computer Number Operations (Binary Arithmetic)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: 3-bit and 4-bit grouping speed test.
- **0:15 – 0:45 (30 min)**: Core Concept: Binary addition rules ($1+1=10_2, 1+1+1=11_2$). Binary subtraction using borrowing.
- **0:45 – 0:70 (25 min)**: Guided Practice: Multi-digit binary addition and subtraction. Checking answers via decimal conversion.
- **0:70 – 0:85 (15 min)**: Timed ACSL Arithmetic Problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework check.

### 🎯 Learning Objectives
1. Add two or three binary numbers accurately with carry propagation.
2. Subtract binary numbers using place-value borrowing.
3. Solve multi-base arithmetic equations (e.g., $1011_2 + 25_8 = X_{16}$).

### 📘 Core Content & Worked Examples

#### Addition Rules
- $0 + 0 = 0$
- $0 + 1 = 1$
- $1 + 1 = 0 \text{ with carry } 1$ ($10_2$)
- $1 + 1 + 1 = 1 \text{ with carry } 1$ ($11_2$)

#### Worked Example: Add $101101_2 + 11011_2$
```text
   1 1 1 1 1   (carries)
   1 0 1 1 0 1  (= 45)
 + 0 1 1 0 1 1  (= 27)
 --------------
 1 0 0 1 0 0 0  (= 72)
```
Check: $45 + 27 = 72$. Correct!

#### Subtraction with Borrowing
When you borrow in base 10, you borrow 10. When you borrow in base 2, **you borrow 2**!
Example: $100_2 - 1_2$:
- You borrow from the 4s place: becomes 2 in the 2s place, which leaves 1 and gives 2 to the 1s place:
- $2 - 1 = 1 \implies 011_2$ (3).

### 📝 In-Class Exercises
1. Calculate $11011_2 + 10110_2$ in binary. (*Answer*: $110001_2$).
2. Calculate $10101_2 - 110_2$. (*Answer*: $1111_2$).
3. Evaluate $14_8 + 1010_2$ and give the answer in base 10. (*Answer*: $14_8 = 12$, $1010_2 = 10 \implies 12 + 10 = 22$).

### 🏠 Homework Assignment
1. $101101_2 + 111100_2 = ?$
2. $110010_2 - 10111_2 = ?$
3. Solve for $X$ in Base 8: $2\text{A}_{16} + 1101_2 = X_8$.

---

## 📅 Class 4: "What Does This Program Do?" & Contest 1 Mock Test

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Homework review & arithmetic speed run.
- **0:15 – 0:45 (30 min)**: Core Concept: Pseudocode tracing. Understanding variables, assignment (`=`), conditionals (`IF ... THEN ... ELSE`), and loops (`FOR ... TO ...`).
- **0:45 – 0:65 (20 min)**: Step-by-step Trace Tables method.
- **0:65 – 0:85 (20 min)**: Official 5-Question Contest 1 Simulation (Timed).
- **0:85 – 0:90 (5 min)**: Score debrief and celebration of Unit 1 completion!

### 🎯 Learning Objectives
1. Read ACSL elementary pseudocode without confusion.
2. Build systematic Trace Tables tracking variable state line by line.
3. Complete a 5-question ACSL Contest 1 paper in under 30 minutes with $\ge 80\%$ accuracy.

### 📘 Pseudocode Tracing Example

```basic
10 X = 5
20 Y = 2
30 FOR K = 1 TO 4
40   IF X > Y THEN
50     X = X - 1
60     Y = Y + 2
70   ELSE
80     X = X + 2
90   END IF
100 NEXT K
110 PRINT X + Y
```

#### Trace Table:
| Loop $K$ | Condition $X > Y$? | $X$ becomes | $Y$ becomes |
| :---: | :---: | :---: | :---: |
| Initial | - | 5 | 2 |
| $K=1$ | $5 > 2$ (True) | $5 - 1 = 4$ | $2 + 2 = 4$ |
| $K=2$ | $4 > 4$ (False!) | $4 + 2 = 6$ | 4 |
| $K=3$ | $6 > 4$ (True) | $6 - 1 = 5$ | $4 + 2 = 6$ |
| $K=4$ | $5 > 6$ (False) | $5 + 2 = 7$ | 6 |

Final result: $X + Y = 7 + 6 = 13$.

---

### 🏆 Unit 1 Mock Contest (Elementary Division)
1. Convert $110101_2$ to Base 10. (*Answer: 53*)
2. Convert $3\text{F}_{16}$ to Octal. (*Answer: 77*)
3. Find the value of $X$ in Base 2: $10110_2 + X_2 = 100000_2$. (*Answer: $1010_2$*)
4. What is the value of $P$ after executing:
   ```basic
   P = 1
   FOR I = 1 TO 5
     P = P * 2
   NEXT I
   ```
   (*Answer: 32*)
5. What does the following program print?
   ```basic
   A = 12
   B = 18
   IF A + 6 = B THEN
     C = B - A
   ELSE
     C = A + B
   END IF
   PRINT C * 2
   ```
   (*Answer: 12*)
