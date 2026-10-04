# Unit 1: Intermediate Division (4 Classes × 90 Minutes)

This curriculum prepares high school competitors (Grades 10–12) for **ACSL Contest 1** at the Intermediate/Senior Division level, covering advanced number representations, nested recursion, complex pseudocode, and contest programming strategies.

---

## 📅 Class 1: Signed Number Representations & Fractional Bases

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Diagnostic warm-up: Signed magnitude vs. One's Complement vs. Two's Complement.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Two's Complement: Form, range of $n$ bits ($-2^{n-1} \dots 2^{n-1}-1$), negation trick (invert bits and add 1, or preserve bits up to and including the first 1 from right).
  - Fractional base conversions in arbitrary bases ($b_1 \rightarrow b_2$).
  - Detecting signed overflow in addition.
- **0:45 – 0:70 (25 min)**: Guided Problem Solving: Signed hex arithmetic, overflow flags, base $b$ repeating fractions.
- **0:70 – 0:85 (15 min)**: Timed Speed Challenge: 5 contest-grade questions.
- **0:85 – 0:90 (5 min)**: Wrap-up & Homework.

### 🎯 Learning Objectives
1. Convert signed negative integers to 8-bit and 16-bit Two's Complement binary/hex representation.
2. Decode Two's Complement bit patterns with negative leading bits.
3. Detect arithmetic overflow in two's complement addition ($C_{in} \oplus C_{out}$ of MSB).
4. Convert repeating fractions in base $b$ to rational fractions ($p/q$).

### 📘 Core Content & Worked Examples

#### Example 1: 8-Bit Two's Complement
Find the 8-bit Two's Complement representation of $-43_{10}$, and express it in Hexadecimal.
- Step 1: Write $+43$ in 8-bit binary:
  $$43 = 32 + 8 + 2 + 1 \implies 00101011_2$$
- Step 2: Invert all bits (One's Complement):
  $$\sim 00101011 = 11010100$$
- Step 3: Add 1:
  $$11010100 + 1 = 11010101_2$$
- Step 4: Convert to Hex:
  $$1101 \quad 0101 \implies \text{D}5_{16}.$$

#### Example 2: Decoding Two's Complement Hex
What is the decimal value of the 8-bit Two's Complement number $\text{E}7_{16}$?
- Binary: $1110\ 0111_2$. MSB is 1, so it is **negative**.
- Method A (Invert and add 1):
  $$\sim (11100111) = 00011000$$
  $$00011000 + 1 = 00011001_2 = 25_{10} \implies \mathbf{-25}.$$
- Method B (Positional weight of MSB is $-2^{n-1}$):
  $$-2^7 + 2^6 + 2^5 + 2^2 + 2^1 + 2^0 = -128 + 64 + 32 + 4 + 2 + 1 = -25.$$

#### Example 3: Repeating Fractional Base Conversion
Convert $0.2\overline{3}_5$ to a simplified decimal fraction.
- Let $x = 0.2333\dots_5$.
- Multiply by base $5$: $5x = 2.333\dots_5$.
- Multiply by base $5^2$: $25x = 23.333\dots_5 = (2 \times 5 + 3) + 0.333\dots = 13 + 0.333\dots_5$.
- Subtract: $25x - 5x = 13 - 2 = 11_{10} \implies 20x = 11 \implies x = \frac{11}{20}$.

### 📝 In-Class Exercises
1. What is the range of integers representable in 12-bit two's complement? (*Answer*: $-2^{11}$ to $2^{11}-1$, i.e., $-2048$ to $+2047$).
2. Evaluate $\text{F}2_{16} + \text{1E}_{16}$ as 8-bit signed two's complement numbers. Does overflow occur?  
   (*Answer*: $\text{F}2 = -14$, $1\text{E} = +30$. Sum $= +16 = 00010000_2 = 10_{16}$. No overflow).

---

## 📅 Class 2: Complex & Nested Recursive Functions

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Quick recursion tree check.
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - Nested recursion: $f(f(x))$, Ackermann-like functions.
  - Multi-variable recurrence with state memoization.
  - Mutual recursion ($f$ calls $g$, $g$ calls $f$).
- **0:45 – 0:70 (25 min)**: Guided Problem Solving: Deconstructing nested calls without infinite loops.
- **0:70 – 0:85 (15 min)**: Timed Contest Drill: 3 tricky recursion problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & Memoization table strategy.

### 🎯 Learning Objectives
1. Safely evaluate nested recursive functions by evaluating the inner call first.
2. Track multi-argument state transitions in tabular form.
3. Solve recursive equations under tight time constraints (under 3 minutes).

### 📘 Core Content & Worked Examples

#### Example: Nested Recursive Evaluation
Given:
$$f(x) = \begin{cases} x - 3 & \text{if } x > 20 \\ f(f(x + 5)) & \text{if } x \le 20 \end{cases}$$
Find the value of $f(12)$.

#### Step-by-Step Evaluation Table:
Work backwards from values near 20:
- For $x \ge 21$: $f(x) = x - 3$.
  - $f(21) = 18$
  - $f(22) = 19$
  - $f(23) = 20$
  - $f(24) = 21$
  - $f(25) = 22$
  - $f(26) = 23$
- Now evaluate for $x \le 20$:
  - $f(16) = f(f(21)) = f(18) = \dots$
  Let's compute sequentially from $x=20$ downwards:
  - $f(20) = f(f(25)) = f(22) = 19$
  - $f(19) = f(f(24)) = f(21) = 18$
  - $f(18) = f(f(23)) = f(20) = 19$
  - $f(17) = f(f(22)) = f(19) = 18$
  - $f(16) = f(f(21)) = f(18) = 19$
  - Notice the alternating pattern: for $x \le 20$:
    - If $x$ is even: $f(x) = 19$.
    - If $x$ is odd: $f(x) = 18$.
- Therefore, since 12 is even: **$f(12) = 19$**!

*Teaching Tip*: ACSL loves patterns! When students see recursion with large numbers, encourage finding the periodic cycle rather than expanding 50 branches.

---

## 📅 Class 3: "What Does This Program Do?" (Intermediate Pseudocode)

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: String functions review (`MID$`, `LEFT$`, `RIGHT$`, `LEN`).
- **0:15 – 0:45 (30 min)**: Theoretical Deep Dive:
  - 2D arrays / Matrices indexing.
  - String manipulation and ASCII transformations.
  - Subroutine / function calls within pseudocode.
- **0:45 – 0:70 (25 min)**: Guided Practice: Tracing a 25-line nested algorithm with string accumulators.
- **0:70 – 0:85 (15 min)**: Timed Pseudocode Drill: 2 challenging past ACSL problems.
- **0:85 – 0:90 (5 min)**: Wrap-up & error analysis.

### 📘 Pseudocode Tracing Example

```basic
S$ = "ACSL2024CONTEST"
OUT$ = ""
N = LEN(S$)
FOR I = 1 TO N STEP 2
  CH$ = MID$(S$, I, 1)
  IF CH$ >= "A" AND CH$ <= "Z" THEN
    K = ASC(CH$) - ASC("A")
    IF K MOD 2 = 0 THEN
      OUT$ = OUT$ + CH$
    END IF
  END IF
NEXT I
PRINT OUT$
```

#### Step-by-Step Trace:
- `S$` length is 14.
- `I` steps by 2: values are $1, 3, 5, 7, 9, 11, 13$.
- Characters at odd indices (1-indexed):
  - $I=1: \text{'A'} \implies \text{ASC}('A') - \text{ASC}('A') = 0$. $0 \pmod 2 = 0 \implies \text{Append 'A'}$.
  - $I=3: \text{'S'} \implies 18 \pmod 2 = 0 \implies \text{Append 'S'}$.
  - $I=5: \text{'2'} \implies$ Not between 'A' and 'Z'.
  - $I=7: \text{'2'} \implies$ Not letter.
  - $I=9: \text{'C'} \implies 2 \pmod 2 = 0 \implies \text{Append 'C'}$.
  - $I=11: \text{'N'} \implies 13 \pmod 2 = 1 \implies$ Skip.
  - $I=13: \text{'E'} \implies 4 \pmod 2 = 0 \implies \text{Append 'E'}$.
- Final Result: `"ASCE"`.

---

## 📅 Class 4: Contest 1 Programming Problem & Timed Mock Contest

### ⏱️ 90-Minute Lesson Timeline
- **0:00 – 0:15 (15 min)**: Warm-up: Rapid review of input parsing (Python `sys.stdin.read().split()` or Java `Scanner`).
- **0:15 – 0:45 (30 min)**: Contest Programming Deep Dive:
  - Architecture of typical ACSL Contest 1 programming problems (Base transformations, numeral systems, transformational rules).
  - Common pitfalls: string indexing out of bounds, large base overflows, formatting output.
- **0:45 – 0:75 (30 min)**: **Full Timed ACSL Contest 1 Mock Exam (5 Short Answer Questions)**.
- **0:75 – 0:90 (15 min)**: Detailed review, scoring rubric, and individual feedback.

### 💻 Typical Contest 1 Programming Task Blueprint
**Problem (Sample: "Base Transposer")**:
Given a series of lines where each line contains a number $N$, its current base $B_1$, and a target base $B_2$, convert $N$ to base $B_2$. If $N$ has fractional parts, round to 3 decimal places.

```python
# Sample Contest 1 Solution Pattern (Python 3)
def convert_base(num_str, b1, b2):
    # Split integer and fractional parts
    parts = num_str.split('.')
    int_val = int(parts[0], b1)
    
    # Convert integer part to target base
    digits = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    if int_val == 0:
        res = "0"
    else:
        res = ""
        while int_val > 0:
            res = digits[int_val % b2] + res
            int_val //= b2
            
    if len(parts) == 1:
        return res
        
    # Convert fractional part
    frac_str = parts[1]
    frac_val = sum(digits.index(ch) * (b1 ** -(i + 1)) for i, ch in enumerate(frac_str))
    
    frac_res = ""
    for _ in range(3):  # 3 decimal places
        frac_val *= b2
        d = int(frac_val)
        frac_res += digits[d]
        frac_val -= d
        
    return res + "." + frac_res
```

---

### 🏆 Unit 1 Intermediate Division Mock Contest
1. What is the value of 8-bit Two's Complement number $\text{B}4_{16}$ in decimal? (*Answer: $-76$*)
2. Convert $0.3\overline{6}_7$ to a simplified decimal fraction. (*Answer: $\frac{27}{42} = \frac{9}{14}$*)
3. Given $F(a, b)$:
   $$F(a, b) = \begin{cases} a + 1 & \text{if } a = b \\ F(a-1, b) + F(a, b+1) & \text{if } a > b \\ 2 \cdot F(b, a) & \text{if } a < b \end{cases}$$
   Find $F(3, 1)$. (*Answer: 36*)
4. Find the base $b$ such that $144_b = 64_{10} + 36_{10}$. (*Answer: $b^2 + 4b + 4 = 100 \implies (b+2)^2 = 100 \implies b = 8$*)
5. What is the output of the following pseudocode?
   ```basic
   A = 1
   FOR I = 1 TO 4
     FOR J = I TO 4
       A = A + (I * J)
     NEXT J
   NEXT I
   PRINT A
   ```
   (*Answer: 71*)
