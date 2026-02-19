# 🧪 Lab 5 – FIRST and FOLLOW Computation

## 🎯 Aim
To write a Python program to compute FIRST and FOLLOW sets for a given Context-Free Grammar (CFG).

## 📚 Description
FIRST and FOLLOW sets are essential in compiler design for constructing predictive parsing tables and checking whether a grammar is suitable for LL(1) parsing.  
This program takes grammar productions as input and calculates FIRST and FOLLOW sets using standard compiler design algorithms.

## 🛠️ Algorithm

### FIRST Set:
1. If X is a terminal, FIRST(X) = {X}
2. If X → ε, then ε is in FIRST(X)
3. If X → Y1Y2...Yn
   - Add FIRST(Y1) to FIRST(X)
   - If FIRST(Y1) contains ε, add FIRST(Y2) and so on

### FOLLOW Set:
1. Add `$` to FOLLOW(Start Symbol)
2. If A → αBβ, then FIRST(β) is in FOLLOW(B)
3. If A → αB or FIRST(β) contains ε, add FOLLOW(A) to FOLLOW(B)

## ▶️ How to Run
```bash
python Lab5_FIRST_FOLLOW.py
🧾 Input Format

Enter number of productions

Use format: A->aB|b

Do not use spaces

Use ε for epsilon (if needed)

📊 Sample Input
5
E->TR
R->+TR|ε
T->FY
Y->*FY|ε
F->(E)|i

📤 Sample Output
FIRST Sets:
FIRST(E) = { (, i }
FIRST(R) = { +, ε }
FIRST(T) = { (, i }
FIRST(Y) = { *, ε }
FIRST(F) = { (, i }

FOLLOW Sets:
FOLLOW(E) = { $, ) }
FOLLOW(R) = { $, ) }
FOLLOW(T) = { +, $, ) }
FOLLOW(Y) = { +, $, ) }
FOLLOW(F) = { *, +, $, ) }

🎓 Learning Outcome

Understand grammar analysis

Compute FIRST and FOLLOW sets

Apply concepts in LL(1) parsing
