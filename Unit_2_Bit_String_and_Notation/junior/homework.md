# Unit 2: Junior Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 2 (Bit-String Flicking, Shifts/Circs, Prefix/Postfix Expressions, and Junior Pseudocode). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Bit-String Logic & Precedence

### Section A: Bitwise Operators
1. Complete the truth table values for inputs $A=1, B=0$:
   - $\text{NOT } A = \underline{\hspace{1cm}}$
   - $A \text{ AND } B = \underline{\hspace{1cm}}$
   - $A \text{ OR } B = \underline{\hspace{1cm}}$
   - $A \text{ XOR } B = \underline{\hspace{1cm}}$
2. What is the official ACSL order of operations among: `OR`, `AND`, `NOT`, `XOR`?

### Section B: Bit-String Expressions (Length 5)
3. Evaluate: $\text{NOT } 10110 \text{ AND } 11001$.
4. Evaluate: $11010 \text{ XOR } 01101 \text{ OR } 00111$.
5. Evaluate: $\text{NOT } (10011 \text{ OR } 01100) \text{ XOR } 11100$.
6. Evaluate: $10101 \text{ AND } 01110 \text{ OR } \text{NOT } 11000 \text{ XOR } 00101$.

---

## 📝 Homework 2: Shifts, Circular Rotates & Bit Equations

### Section A: Shift & Rotate Operations
1. Given $S = 10110$:
   - (a) $\text{LSHIFT-2 } S = \underline{\hspace{2cm}}$
   - (b) $\text{RSHIFT-3 } S = \underline{\hspace{2cm}}$
   - (c) $\text{LCIRC-2 } S = \underline{\hspace{2cm}}$
   - (d) $\text{RCIRC-1 } S = \underline{\hspace{2cm}}$
2. Evaluate: $\text{RCIRC-2 } (\text{LSHIFT-1 } 10101)$.
3. Evaluate: $\text{NOT } (\text{LCIRC-3 } 11001) \text{ AND } \text{RSHIFT-2 } 10111$.

### Section B: Solving for Unknown String $X$
4. Solve for the 5-bit string $X$: $(\text{LSHIFT-1 } X) \text{ OR } 01011 = 11111$.
5. Solve for all 5-bit strings $X$: $(\text{RCIRC-1 } X) \text{ AND } 10101 = 10001$.
6. Find the 5-bit string $X$ with the minimum number of 1s such that:  
   $(\text{NOT } X) \text{ XOR } 10100 = 01011$.

---

## 📝 Homework 3: Prefix & Postfix Mastery

### Section A: Infix to Prefix & Postfix
1. Convert $(A + B) * (C / D) - E$ to Postfix.
2. Convert $(A + B) * (C / D) - E$ to Prefix.
3. Convert $A \text{\textasciicircum} B * C + D / E$ to Postfix.

### Section B: Evaluation
4. Evaluate the postfix expression: $12 \ 3 \ / \ 4 \ 2 \ \text{\textasciicircum} \ * \ 10 \ -$.
5. Evaluate the prefix expression: $- \ * \ + \ 5 \ 3 \ 2 \ / \ 16 \ 4$.
6. Evaluate: $4 \ 2 \ 3 \ \text{\textasciicircum} \ \text{\textasciicircum} \ 2 \ /$ (assuming right-associative exponentiation).

---

## 📝 Homework 4: Junior Pseudocode & Contest 2 Mock Exam

### Section A: Pseudocode Tracing
1. What does the following program print?
   ```basic
   S$ = "INTERNATIONAL"
   COUNT = 0
   FOR I = 1 TO LEN(S$)
     CH$ = MID$(S$, I, 1)
     IF CH$ = "A" OR CH$ = "E" OR CH$ = "I" THEN
       COUNT = COUNT + 1
     END IF
   NEXT I
   PRINT COUNT
   ```

2. What does this program print?
   ```basic
   A$ = "10110"
   B$ = "01101"
   RES$ = ""
   FOR I = 1 TO 5
     CA = VAL(MID$(A$, I, 1))
     CB = VAL(MID$(B$, I, 1))
     IF CA = CB THEN
       RES$ = RES$ + "0"
     ELSE
       RES$ = RES$ + "1"
     END IF
   NEXT I
   PRINT RES$
   ```

### Section B: Junior Contest 2 Mock Set
3. Evaluate: $\text{LSHIFT-1 } (\text{NOT } 01101 \text{ XOR } \text{RCIRC-2 } 10011)$.
4. How many 5-bit strings $X$ satisfy: $(X \text{ AND } 11100) \text{ OR } 00011 = 10111$?
5. Evaluate the prefix expression: $+ \ * \ 5 \ - \ 8 \ 3 \ / \ 24 \ 6$.
6. Convert $A + (B - C) * D \text{\textasciicircum} E$ to postfix.

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. $\text{NOT } A = 0$, $A \text{ AND } B = 0$, $A \text{ OR } B = 1$, $A \text{ XOR } B = 1$.
2. $\text{NOT} > \text{AND} > \text{XOR} > \text{OR}$.
3. $\text{NOT } 10110 = 01001$. Then $01001 \text{ AND } 11001 = \mathbf{01001}$.
4. XOR before OR: $11010 \oplus 01101 = 10111$. Then $10111 \lor 00111 = \mathbf{10111}$.
5. Inside (): $10011 \lor 01100 = 11111$. $\text{NOT } 11111 = 00000$. $00000 \oplus 11100 = \mathbf{11100}$.
6. Precedence:
   - $\text{NOT } 11000 = 00111$.
   - $10101 \text{ AND } 01110 = 00100$.
   - Next XOR: $00111 \oplus 00101 = 00010$.
   - Finally OR: $00100 \lor 00010 = \mathbf{00110}$.

### Homework 2 Solutions
1. (a) $11000$, (b) $00010$, (c) $11010$, (d) $01011$.
2. $\text{LSHIFT-1 } 10101 = 01010$. $\text{RCIRC-2 } 01010 = \mathbf{10010}$.
3. $\text{LCIRC-3 } 11001 = 01110 \implies \text{NOT} = 10001$.
   $\text{RSHIFT-2 } 10111 = 00101$.
   $10001 \text{ AND } 00101 = \mathbf{00001}$.
4. Let $X = x_1 x_2 x_3 x_4 x_5$. $\text{LSHIFT-1 } X = x_2 x_3 x_4 x_5 0$.
   $(x_2 x_3 x_4 x_5 0) \lor 01011 = 11111 \implies x_2 \lor 0 = 1 \implies x_2 = 1$.
   $x_4 \lor 0 = 1 \implies x_4 = 1$. $x_1, x_3, x_5$ can be $0$ or $1$.
   $X = *1*1*$.
5. $\text{RCIRC-1 } X = x_5 x_1 x_2 x_3 x_4$.
   $(x_5 x_1 x_2 x_3 x_4) \text{ AND } 10101 = 10001$.
   $x_5 \land 1 = 1 \implies x_5 = 1$.
   $x_2 \land 1 = 0 \implies x_2 = 0$.
   $x_4 \land 1 = 1 \implies x_4 = 1$.
   $x_1, x_3$ can be any value ($0$ or $1$).
   $X = *0*11 \implies 4$ solutions: $00011, 00111, 10011, 10111$.
6. $\text{NOT } X \oplus 10100 = 01011 \implies \text{NOT } X = 01011 \oplus 10100 = 11111$.
   $X = \text{NOT } 11111 = \mathbf{00000}$.

### Homework 3 Solutions
1. $\mathbf{A \ B \ + \ C \ D \ / \ * \ E \ -}$.
2. $\mathbf{- \ * \ + \ A \ B \ / \ C \ D \ E}$.
3. $\mathbf{A \ B \ \text{\textasciicircum} \ C \ * \ D \ E \ / \ +}$.
4. $12/3 = 4$, $4^2 = 16$, $4 \times 16 = 64$, $64 - 10 = \mathbf{54}$.
5. $+ \ 5 \ 3 = 8$, $* \ 8 \ 2 = 16$. $16/4 = 4$. $16 - 4 = \mathbf{12}$.
6. $2^3 = 8$, $2^8 = 256$, $256/2 = \mathbf{128}$.

### Homework 4 Solutions
1. Matches: I (idx 1), E (idx 4), A (idx 6), I (idx 8), O (idx 9), A (idx 12) $\implies$ total matching A, E, I is $1 + 1 + 2 + 1 = \mathbf{5}$.
2. Computes bitwise XOR: $10110 \oplus 01101 = \mathbf{"11011"}$.
3. $\text{NOT } 01101 = 10010$. $\text{RCIRC-2 } 10011 = 11100$.
   $10010 \oplus 11100 = 01110$.
   $\text{LSHIFT-1 } 01110 = \mathbf{11100}$.
4. $(X \land 11100) \lor 00011 = 10111$.
   $x_1 \land 1 = 1 \implies x_1 = 1$.
   $x_2 \land 1 = 0 \implies x_2 = 0$.
   $x_3 \land 1 = 1 \implies x_3 = 1$.
   $x_4, x_5$ can be anything ($0$ or $1$) because $00011$ forces the last two bits to 1.
   Number of strings $= 2^2 = \mathbf{4}$.
5. $8 - 3 = 5$, $5 \times 5 = 25$. $24/6 = 4$. $25 + 4 = \mathbf{29}$.
6. $\mathbf{A \ B \ C \ - \ D \ E \ \text{\textasciicircum} \ * \ +}$.
