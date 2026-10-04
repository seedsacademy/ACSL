# Unit 1: Elementary Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 1 (Computer Number Systems & "What Does This Program Do?"). Every set includes **Concept Checks**, **Official Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Binary & Decimal Foundations

### Section A: Concept Checks
1. Why does the binary number system only use digits $0$ and $1$?
2. Write down the first 8 powers of 2 (starting from $2^0$ up to $2^7$).
3. What is the value of the binary number $100000_2$ in base 10?

### Section B: Conversions (Binary $\rightarrow$ Decimal)
4. Convert $1011_2$ to decimal.
5. Convert $11010_2$ to decimal.
6. Convert $100101_2$ to decimal.
7. Convert $111111_2$ to decimal.

### Section C: Conversions (Decimal $\rightarrow$ Binary)
8. Convert $19_{10}$ to binary.
9. Convert $38_{10}$ to binary.
10. Convert $77_{10}$ to binary.
11. Convert $105_{10}$ to binary.

### Section D: Challenge Problem
12. If a computer storage register can hold an 8-bit binary number, what is the largest decimal number it can store?

---

## 📝 Homework 2: Octal & Hexadecimal Grouping

### Section A: Concept Checks
1. What decimal values do the hexadecimal letters represent? Complete:  
   $A = \underline{\hspace{1cm}}, B = \underline{\hspace{1cm}}, C = \underline{\hspace{1cm}}, D = \underline{\hspace{1cm}}, E = \underline{\hspace{1cm}}, F = \underline{\hspace{1cm}}$.
2. How many binary bits are needed to represent exactly one Octal digit?
3. How many binary bits are needed to represent exactly one Hexadecimal digit?

### Section B: Octal $\leftrightarrow$ Binary Grouping
4. Convert $11010110_2$ to Octal (base 8).
5. Convert $1011101001_2$ to Octal.
6. Convert $365_8$ to Binary.
7. Convert $712_8$ to Binary.

### Section C: Hexadecimal $\leftrightarrow$ Binary Grouping
8. Convert $110111101010_2$ to Hexadecimal.
9. Convert $10011101011_2$ to Hexadecimal.
10. Convert $4\text{C}7_{16}$ to Binary.
11. Convert $\text{F}0\text{E}_{16}$ to Binary.

### Section D: Octal $\leftrightarrow$ Hexadecimal (The Binary Bridge)
12. Convert $57_8$ to Hexadecimal without going through Base 10.
13. Convert $2\text{B}6_{16}$ to Octal.

---

## 📝 Homework 3: Binary & Multi-Base Arithmetic

### Section A: Binary Addition
1. Compute: $1011_2 + 110_2$.
2. Compute: $11011_2 + 10101_2$.
3. Compute: $101110_2 + 11011_2$.
4. Compute: $11111_2 + 1_2$.

### Section B: Binary Subtraction
5. Compute: $1101_2 - 101_2$.
6. Compute: $10110_2 - 1101_2$.
7. Compute: $10000_2 - 111_2$.

### Section C: Multi-Base Arithmetic
8. Find $X$ in Base 10: $X = 1011_2 + 17_8$.
9. Find $X$ in Base 8: $X = 3\text{D}_{16} - 10100_2$.
10. Solve for the binary string $B$: $B + 1101_2 = 100000_2$.

---

## 📝 Homework 4: Pseudocode Tracing & Contest Simulation

### Section A: Trace Tables
1. What does the following program print?
   ```basic
   A = 3
   B = 15
   FOR K = 1 TO 4
     A = A + 2
     B = B - A
   NEXT K
   PRINT B
   ```
2. What does the following program print?
   ```basic
   X = 20
   Y = 6
   IF X / Y > 3 THEN
     Z = (X - Y) * 2
   ELSE
     Z = X + Y
   END IF
   PRINT Z
   ```

### Section B: Contest 1 Practice Set (ACSL Style)
3. Convert $1100111_2$ to Hexadecimal.
4. Convert $274_8$ to decimal.
5. Evaluate $11011_2 + 101101_2 - 1110_2$ in binary.
6. What is the value of $S$ after running:
   ```basic
   S = 0
   FOR I = 1 TO 6
     IF I MOD 2 = 1 THEN
       S = S + I * 2
     END IF
   NEXT I
   PRINT S
   ```
7. Find the base 10 value of $X$ if $X = 1010_2 \times 11_2$.

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. Computers use electrical switches (transistors) that have two physical states: OFF ($0$) and ON ($1$).
2. $2^0=1, 2^1=2, 2^2=4, 2^3=8, 2^4=16, 2^5=32, 2^6=64, 2^7=128$.
3. $100000_2 = 2^5 = 32_{10}$.
4. $1011_2 = 8 + 2 + 1 = 11_{10}$.
5. $11010_2 = 16 + 8 + 2 = 26_{10}$.
6. $100101_2 = 32 + 4 + 1 = 37_{10}$.
7. $111111_2 = 2^6 - 1 = 64 - 1 = 63_{10}$.
8. $19 = 16 + 2 + 1 \implies 10011_2$.
9. $38 = 32 + 4 + 2 \implies 100110_2$.
10. $77 = 64 + 8 + 4 + 1 \implies 1001101_2$.
11. $105 = 64 + 32 + 8 + 1 \implies 1101001_2$.
12. $2^8 - 1 = 255_{10}$.

### Homework 2 Solutions
1. $A=10, B=11, C=12, D=13, E=14, F=15$.
2. 3 bits ($2^3 = 8$).
3. 4 bits ($2^4 = 16$).
4. Group by 3: $(011)(010)(110)_2 = 326_8$.
5. Group by 3: $(001)(011)(101)(001)_2 = 1351_8$.
6. $3=011, 6=110, 5=101 \implies 011110101_2 = 11110101_2$.
7. $7=111, 1=001, 2=010 \implies 111001010_2$.
8. Group by 4: $(1101)(1110)(1010)_2 = \text{DEA}_{16}$.
9. Group by 4: $(0100)(1110)(1011)_2 = 4\text{EB}_{16}$.
10. $4=0100, \text{C}=1100, 7=0111 \implies 10011000111_2$.
11. $\text{F}=1111, 0=0000, \text{E}=1110 \implies 111100001110_2$.
12. $57_8 = (101)(111)_2 = (0010)(1111)_2 = 2\text{F}_{16}$.
13. $2\text{B}6_{16} = (0010)(1011)(0110)_2 = (001)(010)(110)(110)_2 = 1266_8$.

### Homework 3 Solutions
1. $1011_2 + 110_2 = 11 + 6 = 17 = 10001_2$.
2. $11011_2 + 10101_2 = 27 + 21 = 48 = 110000_2$.
3. $101110_2 + 11011_2 = 46 + 27 = 73 = 1001001_2$.
4. $11111_2 + 1_2 = 31 + 1 = 32 = 100000_2$.
5. $1101_2 - 101_2 = 13 - 5 = 8 = 1000_2$.
6. $10110_2 - 1101_2 = 22 - 13 = 9 = 1001_2$.
7. $10000_2 - 111_2 = 16 - 7 = 9 = 1001_2$.
8. $1011_2 = 11$, $17_8 = 1(8) + 7 = 15 \implies X = 11 + 15 = 26_{10}$.
9. $3\text{D}_{16} = 3(16)+13 = 61_{10}$. $10100_2 = 20_{10}$. $61 - 20 = 41_{10} = 51_8$.
10. $B = 100000_2 - 1101_2 = 32 - 13 = 19_{10} = 10011_2$.

### Homework 4 Solutions
1. Trace:
   - $K=1: A=5, B=15-5=10$
   - $K=2: A=7, B=10-7=3$
   - $K=3: A=9, B=3-9=-6$
   - $K=4: A=11, B=-6-11=-17$
   - Output: **-17**.
2. $X/Y = 20/6 = 3.333 > 3$ (True). $Z = (20 - 6) \times 2 = 14 \times 2 = 28$. Output: **28**.
3. Group by 4: $(0110)(0111)_2 = 67_{16}$.
4. $274_8 = 2(64) + 7(8) + 4 = 128 + 56 + 4 = 188_{10}$.
5. $27 + 45 - 14 = 58_{10} = 111010_2$.
6. Odd $I$ in $1..6$ are $1, 3, 5$:
   - $I=1: S = 0 + 2 = 2$
   - $I=3: S = 2 + 6 = 8$
   - $I=5: S = 8 + 10 = 18$
   - Output: **18**.
7. $1010_2 = 10$, $11_2 = 3 \implies 10 \times 3 = 30_{10}$.
