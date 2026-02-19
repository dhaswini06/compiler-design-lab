# 🔷 Compiler Design Lab 4
## Left Recursion Removal & Left Factoring

### 📌 Objective
To implement a program that eliminates Left Recursion and performs Left Factoring on a given Context Free Grammar (CFG) to make it suitable for predictive (LL(1)) parsing.

---

## 📖 Description
In Compiler Design, grammars with left recursion cannot be parsed using top-down parsers like Recursive Descent Parsers. Similarly, grammars with common prefixes cause ambiguity during parsing.  

This program:
- Eliminates Immediate Left Recursion
- Performs Left Factoring
- Accepts grammar from user input
- Displays transformed grammar clearly

The implementation follows standard algorithms used in Syntax Analysis.

---

## 🧮 Features
- Removes Immediate Left Recursion
- Performs Left Factoring automatically
- Supports multiple productions
- User-friendly input format
- Clean and readable output
- Single file implementation (as required for lab submission)

---
A -> Aα | β

Example:


E -> E+T | T
A -> aB | aC | d


---

## ▶️ How to Run

### Step 1: Clone Repository
```bash
git clone https://github.com/your-username/COMPILER-DESIGN-LAB.git
cd COMPILER-DESIGN-LAB

Step 2: Run the Program
python Lab4_LeftRecursion_LeftFactoring.py

💻 Sample Input
Enter number of productions: 1
Enter production (Example: A->Aa|b): 
A->Aa|b

📤 Sample Output
After Removing Left Recursion:
A -> bA'
A' -> aA' | ε

After Left Factoring:
(No Left Factoring needed)

🎯 Applications

Compiler Design (Syntax Analysis)

LL(1) Parser Construction

Grammar Optimization

Programming Language Processing
## 🧾 Input Format
Enter productions in the format:
