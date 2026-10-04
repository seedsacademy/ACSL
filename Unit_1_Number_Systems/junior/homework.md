# Unit 1: Junior Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 1 (Arbitrary Number Bases, Fractions, Recursive Functions, and "What Does This Program Do?"). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Arbitrary Base Conversions & Fractional Bases

### Section A: Arbitrary Bases ($b \in [2, 16]$)
1. Convert $342_5$ to decimal (base 10).
2. Convert $1202_3$ to decimal.
3. Convert $189_{10}$ to Base 6.
4. Convert $254_7$ to Base 9.
5. Solve for base $b$: $45_b = 37_{10}$.
6. Solve for base $b$: $132_b = 30_{10}$.

### Section B: Fractional Bases
7. Convert $0.1101_2$ to decimal.
8. Convert $0.625_{10}$ to binary.
9. Convert $0.\text{C}4_{16}$ to binary and octal.
10. Convert $12.375_{10}$ to binary and hexadecimal.

---

## 📝 Homework 2: Multi-Base Arithmetic Operations

### Section A: Octal & Hexadecimal Arithmetic
1. Evaluate in Octal: $563_8 + 274_8$.
2. Evaluate in Octal: $702_8 - 345_8$.
3. Evaluate in Hexadecimal: $3\text{A}9_{16} + 7\text{C}5_{16}$.
4. Evaluate in Hexadecimal: $\text{A}14_{16} - 3\text{E}7_{16}$.

### Section B: Multi-Base Equations
5. Find $X$ in Base 16: $X = 35_8 \times 11_2$.
6. Solve for $N$ in Base 8: $N = 1\text{F}_{16} + 10110_2$.
7. Evaluate in Base 2: $1101_2 \times 1011_2$.

---

## 📝 Homework 3: Recursive Functions

### Section A: Single & Branching Recursion
1. Given:
   $$f(n) = \begin{cases} 4 & \text{if } n \le 1 \\ 2 \cdot f(n-1) + 3 & \text{if } n > 1 \end{cases}$$
   Find $f(4)$.

2. Given:
   $$g(x) = \begin{cases} x & \text{if } x \le 2 \\ g(x-1) + g(x-2) & \text{if } x > 2 \end{cases}$$
   Find $g(6)$.

3. Given:
   $$h(n) = \begin{cases} n - 1 & \text{if } n \le 3 \\ h(n-2) + 2 \cdot h(n-3) & \text{if } n > 3 \end{cases}$$
   Find $h(7)$.

### Section B: Multi-Parameter Recursion
4. Given:
   $$F(x, y) = \begin{cases} x + y & \text{if } x \le 0 \text{ or } y \le 0 \\ F(x-1, y) + F(x, y-1) & \text{otherwise} \end{cases}$$
   Find $F(2, 2)$.

---

## 📝 Homework 4: Junior Pseudocode & Contest 1 Simulation

### Section A: Pseudocode Tracing
1. What is the value of `TOTAL` after running:
   ```basic
   DIM A(5)
   FOR I = 1 TO 5
     A(I) = I * I - I
   NEXT I
   TOTAL = 0
   FOR J = 1 TO 4
     TOTAL = TOTAL + (A(J+1) - A(J))
   NEXT J
   PRINT TOTAL
   ```

2. What does this program print?
   ```basic
   N = 45
   C = 0
   WHILE N > 0
     IF N MOD 2 = 1 THEN
       C = C + 1
     END IF
     N = N \ 2
   END WHILE
   PRINT C
   ```

### Section B: Junior Contest 1 Mock Test Set
3. Convert $312_4$ to base 8.
4. What is the value of $X$ in Base 16: $7\text{A}_{16} + 65_8 = X_{16}$?
5. Given:
   $$f(x) = \begin{cases} 2 \cdot x & \text{if } x \le 3 \\ f(x-2) + f(x-1) & \text{if } x > 3 \end{cases}$$
   Find $f(6)$.
6. What is the decimal value of the binary fraction $101.1011_2$?

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. $3(25) + 4(5) + 2(1) = 75 + 20 + 2 = 97_{10}$.
2. $1(27) + 2(9) + 0(3) + 2(1) = 27 + 18 + 0 + 2 = 47_{10}$.
3. Repeated division by 6: $189 = 31 \times 6 + 3$; $31 = 5 \times 6 + 1$; $5 = 0 \times 6 + 5 \implies 513_6$.
4. $254_7 = 2(49) + 5(7) + 4 = 98 + 35 + 4 = 137_{10}$. In Base 9: $137 = 15 \times 9 + 2$; $15 = 1 \times 9 + 6$; $1 = 0 \times 9 + 1 \implies 162_9$.
5. $4b + 5 = 37 \implies 4b = 32 \implies b = 8$.
6. $b^2 + 3b + 2 = 30 \implies b^2 + 3b - 28 = 0 \implies (b+7)(b-4) = 0 \implies b = 4$.
7. $0.5 + 0.25 + 0 + 0.0625 = 0.8125_{10}$.
8. $0.625 \times 2 = 1.25$ (1); $0.25 \times 2 = 0.5$ (0); $0.5 \times 2 = 1.0$ (1) $\implies 0.101_2$.
9. $0.\text{C}4_{16} = 0.1100\ 0100_2$. In Octal: $0.110\ 001\ 000_2 = 0.61_8$.
10. $12_{10} = 1100_2 = \text{C}_{16}$. $0.375_{10} = 0.011_2 = 0.6_{16} \implies 1100.011_2 = \text{C}.6_{16}$.

### Homework 2 Solutions
1. $563_8 + 274_8 = 1057_8$.
2. $702_8 - 345_8 = 335_8$.
3. $3\text{A}9_{16} + 7\text{C}5_{16} = \text{B}6\text{E}_{16}$.
4. $\text{A}14_{16} - 3\text{E}7_{16} = 62\text{D}_{16}$.
5. $35_8 = 29_{10}$. $11_2 = 3_{10}$. Product $= 87_{10} = 57_{16}$.
6. $1\text{F}_{16} = 31_{10}$. $10110_2 = 22_{10}$. Sum $= 53_{10} = 65_8$.
7. $1101_2 \times 1011_2 = 13 \times 11 = 143_{10} = 10001111_2$.

### Homework 3 Solutions
1. $f(1)=4$, $f(2)=2(4)+3=11$, $f(3)=2(11)+3=25$, $f(4)=2(25)+3=53$.
2. $g(1)=1, g(2)=2, g(3)=3, g(4)=5, g(5)=8, g(6)=13$.
3. Base cases: $h(1)=0, h(2)=1, h(3)=2$.
   - $h(4) = h(2) + 2h(1) = 1 + 0 = 1$.
   - $h(5) = h(3) + 2h(2) = 2 + 2(1) = 4$.
   - $h(6) = h(4) + 2h(3) = 1 + 2(2) = 5$.
   - $h(7) = h(5) + 2h(4) = 4 + 2(1) = 6$.
4. Dynamic table for $F(x, y)$:
   - $F(0, y) = y$, $F(x, 0) = x$.
   - $F(1, 1) = F(0, 1) + F(1, 0) = 1 + 1 = 2$.
   - $F(1, 2) = F(0, 2) + F(1, 1) = 2 + 2 = 4$.
   - $F(2, 1) = F(1, 1) + F(2, 0) = 2 + 2 = 4$.
   - $F(2, 2) = F(1, 2) + F(2, 1) = 4 + 4 = 8$.

### Homework 4 Solutions
1. Telescoping sum! $\sum_{J=1}^4 (A(J+1) - A(J)) = A(5) - A(1)$.
   $A(5) = 25 - 5 = 20$. $A(1) = 1 - 1 = 0 \implies \text{TOTAL} = 20$.
2. This counts the number of 1-bits in the binary representation of 45!
   $45 = 32 + 8 + 4 + 1 = 101101_2 \implies 4$ ones. Output: **4**.
3. $312_4 = 3(16) + 1(4) + 2 = 48 + 4 + 2 = 54_{10}$. In binary: $110110_2$. Group by 3: $66_8$.
4. $65_8 = 6(8) + 5 = 53_{10} = 35_{16}$. $7\text{A}_{16} + 35_{16} = \text{AF}_{16}$.
5. $f(1)=2, f(2)=4, f(3)=6$.
   $f(4) = f(2) + f(3) = 4 + 6 = 10$.
   $f(5) = f(3) + f(4) = 6 + 10 = 16$.
   $f(6) = f(4) + f(5) = 10 + 16 = 26$.
6. $101.1011_2 = 5 + (1/2 + 0/4 + 1/8 + 1/16) = 5 + 11/16 = 5.6875_{10}$.
