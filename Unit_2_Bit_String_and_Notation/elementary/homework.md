# Unit 2: Elementary Division — Homework Problem Sets

This workbook contains curated homework sets for each of the 4 classes in Unit 2 (Prefix / Postfix Expressions and "What Does This Program Do?"). Every set includes **Concept Checks**, **Contest-Style Problems**, and a **Complete Answer Key with Step-by-Step Derivations**.

---

## 📝 Homework 1: Infix, Prefix, and Postfix Basics

### Section A: Concept Checks
1. Explain the difference between Infix, Prefix, and Postfix notations.
2. Why do Prefix and Postfix expressions never require parentheses?
3. In the postfix expression $8 \ 2 \ /$, which number is divided by which?

### Section B: Simple Evaluations
4. Evaluate: $+ \ 14 \ 9$
5. Evaluate: $- \ 25 \ 12$
6. Evaluate: $* \ 7 \ 8$
7. Evaluate: $/ \ 36 \ 6$
8. Evaluate: $15 \ 7 \ -$
9. Evaluate: $9 \ 4 \ *$
10. Evaluate: $48 \ 8 \ /$

---

## 📝 Homework 2: Evaluating Compound Expressions

### Section A: Multi-Operator Prefix Expressions
1. Evaluate: $+ \ * \ 3 \ 5 \ 4$
2. Evaluate: $* \ + \ 6 \ 2 \ - \ 10 \ 3$
3. Evaluate: $- \ * \ 4 \ 4 \ / \ 18 \ 3$
4. Evaluate: $+ \ 5 \ * \ 2 \ \text{\textasciicircum} \ 3 \ 2$

### Section B: Multi-Operator Postfix Expressions
5. Evaluate: $7 \ 3 \ + \ 2 \ *$
6. Evaluate: $20 \ 4 \ / \ 3 \ 2 \ * \ +$
7. Evaluate: $9 \ 5 \ - \ 8 \ 2 \ / \ *$
8. Evaluate: $5 \ 2 \ 3 \ \text{\textasciicircum} \ * \ 10 \ -$

---

## 📝 Homework 3: Conversion Between Notations

### Section A: Infix to Postfix (Full Parenthesization)
1. Convert $A + B * C$ to Postfix.
2. Convert $(A + B) * C$ to Postfix.
3. Convert $A * B - C / D$ to Postfix.
4. Convert $(A + B) / (C - D)$ to Postfix.

### Section B: Infix to Prefix
5. Convert $A + B * C$ to Prefix.
6. Convert $(A + B) * C$ to Prefix.
7. Convert $(A - B) * (C + D)$ to Prefix.
8. Convert $A / B + C * D$ to Prefix.

---

## 📝 Homework 4: Pseudocode & Contest 2 Mock Exam

### Section A: Pseudocode Tracing
1. What does the following program print?
   ```basic
   S$ = "COMPUTER"
   RES$ = ""
   FOR I = 1 TO LEN(S$)
     IF I MOD 2 = 1 THEN
       RES$ = RES$ + MID$(S$, I, 1)
     END IF
   NEXT I
   PRINT RES$
   ```

2. What does the following program print?
   ```basic
   A = 2
   B = 10
   FOR I = 1 TO 4
     B = B - A
     A = A + 1
   NEXT I
   PRINT B
   ```

### Section B: Elementary Contest 2 Mock Set
3. Evaluate: $* \ + \ 4 \ 3 \ - \ 12 \ 5$.
4. Evaluate: $14 \ 2 \ / \ 3 \ * \ 5 \ +$.
5. Convert $(X + Y * Z) / W$ to Postfix.
6. What is the value of the prefix expression: $+ \ 8 \ / \ * \ 6 \ 4 \ 3$?
7. What does this code print?
   ```basic
   W$ = "BANANA"
   COUNT = 0
   FOR I = 1 TO LEN(W$)
     IF MID$(W$, I, 1) = "A" THEN
       COUNT = COUNT + 1
     END IF
   NEXT I
   PRINT COUNT * 10
   ```

---

## 🔑 Complete Answer Key & Solutions

### Homework 1 Solutions
1. Infix has the operator in the middle ($A+B$); Prefix has the operator in front ($+AB$); Postfix has the operator in the back ($AB+$).
2. The position of each operator unambiguously determines which operands it applies to without precedence ambiguity.
3. 8 is divided by 2: $8 / 2 = 4$.
4. $14 + 9 = \mathbf{23}$.
5. $25 - 12 = \mathbf{13}$.
6. $7 \times 8 = \mathbf{56}$.
7. $36 / 6 = \mathbf{6}$.
8. $15 - 7 = \mathbf{8}$.
9. $9 \times 4 = \mathbf{36}$.
10. $48 / 8 = \mathbf{6}$.

### Homework 2 Solutions
1. $* \ 3 \ 5 = 15 \implies + \ 15 \ 4 = \mathbf{19}$.
2. $+ \ 6 \ 2 = 8$, $- \ 10 \ 3 = 7 \implies * \ 8 \ 7 = \mathbf{56}$.
3. $* \ 4 \ 4 = 16$, $/ \ 18 \ 3 = 6 \implies - \ 16 \ 6 = \mathbf{10}$.
4. $\text{\textasciicircum} \ 3 \ 2 = 3^2 = 9$. Next $* \ 2 \ 9 = 18$. Next $+ \ 5 \ 18 = \mathbf{23}$.
5. $7 \ 3 \ + = 10 \implies 10 \ 2 \ * = \mathbf{20}$.
6. $20 \ 4 \ / = 5$, $3 \ 2 \ * = 6 \implies 5 \ 6 \ + = \mathbf{11}$.
7. $9 \ 5 \ - = 4$, $8 \ 2 \ / = 4 \implies 4 \ 4 \ * = \mathbf{16}$.
8. $2 \ 3 \ \text{\textasciicircum} = 8$, $5 \ 8 \ * = 40$, $40 \ 10 \ - = \mathbf{30}$.

### Homework 3 Solutions
1. $((A + (B * C))) \implies \mathbf{A \ B \ C \ * \ +}$.
2. $(((A + B) * C)) \implies \mathbf{A \ B \ + \ C \ *}$.
3. $((A * B) - (C / D)) \implies \mathbf{A \ B \ * \ C \ D \ / \ -}$.
4. $((A + B) / (C - D)) \implies \mathbf{A \ B \ + \ C \ D \ - \ /}$.
5. $+ \ A \ * \ B \ C$.
6. $* \ + \ A \ B \ C$.
7. $* \ - \ A \ B \ + \ C \ D$.
8. $+ \ / \ A \ B \ * \ C \ D$.

### Homework 4 Solutions
1. Takes odd characters: $I=1(\text{'C'}), I=3(\text{'M'}), I=5(\text{'U'}), I=7(\text{'E'}) \implies \mathbf{"CMUE"}$.
2. $I=1: B=10-2=8, A=3$. $I=2: B=8-3=5, A=4$. $I=3: B=5-4=1, A=5$. $I=4: B=1-5=-4, A=6$. Output: **-4**.
3. $+ \ 4 \ 3 = 7$, $- \ 12 \ 5 = 7 \implies 7 \times 7 = \mathbf{49}$.
4. $14/2 = 7$, $7 \times 3 = 21$, $21 + 5 = \mathbf{26}$.
5. $\mathbf{X \ Y \ Z \ * \ + \ W \ /}$.
6. $* \ 6 \ 4 = 24 \implies / \ 24 \ 3 = 8 \implies + \ 8 \ 8 = \mathbf{16}$.
7. "A" appears 3 times in "BANANA". Count $= 3 \implies 3 \times 10 = \mathbf{30}$.
