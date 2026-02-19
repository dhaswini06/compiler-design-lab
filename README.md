# 📘 Compiler Design Laboratory (Lab 1 – Lab 8)

## 👩‍💻 Course: Compiler Design Lab

This repository contains the complete implementation of Compiler Design laboratory experiments from **Lab 1 to Lab 8** using Python.
All programs are designed according to academic syllabus requirements and implemented with clear logic, proper input format, and step-by-step outputs suitable for lab record, viva, and GitHub submission.

---

# 📂 Repository Structure

```
COMPILER-DESIGN-LAB/
│
├── Lab1_Lexical_Analyzer.py
├── Lab2_RE_to_NFA.py
├── Lab3_NFA_to_DFA.py
├── Lab4_LeftRecursion_LeftFactoring.py
├── Lab5_FIRST_FOLLOW.py
├── Lab6_Predictive_Parsing_Table.py
├── Lab7_Shift_Reduce_Parsing.py
├── Lab8_Leading_Trailing.py
└── README.md
```

---

# 🧪 List of Experiments (Lab 1 – Lab 8)

## 🔹 Lab 1 – Implementation of Lexical Analyzer

### Objective:

To design and implement a lexical analyzer that identifies tokens such as:

* Keywords
* Identifiers
* Operators
* Numbers
* Special Symbols

### Description:

This program scans the input source code and breaks it into tokens. It simulates the first phase of a compiler (Lexical Analysis) and classifies each token based on its type.

---

## 🔹 Lab 2 – Conversion from Regular Expression to NFA

### Objective:

To convert a given Regular Expression into an equivalent NFA using Thompson’s Construction.

### Features:

* Supports concatenation (.)
* Supports union (|)
* Supports Kleene star (*)
* Displays NFA states and transitions

Example Input:

```
a.b
a|b
a*
```

---

## 🔹 Lab 3 – Conversion from NFA to DFA

### Objective:

To convert a Non-Deterministic Finite Automaton (NFA) into a Deterministic Finite Automaton (DFA) using Subset Construction Algorithm.

### Description:

This program:

* Accepts NFA transitions
* Computes ε-closure
* Generates DFA states
* Displays transition table

---

## 🔹 Lab 4 – Elimination of Left Recursion and Left Factoring

### Objective:

To eliminate immediate left recursion and perform left factoring on a given grammar.

### Description:

* Detects left recursion in grammar
* Removes left recursion using standard transformation
* Applies left factoring for common prefixes

Example Input:

```
A->Aa|b
A->ab|ac
```

---

## 🔹 Lab 5 – FIRST and FOLLOW Computation

### Objective:

To compute FIRST and FOLLOW sets of a given context-free grammar.

### Features:

* Handles epsilon (ε) productions
* Recursive FIRST computation
* FOLLOW set generation using grammar rules

Example Grammar:

```
E->TR
R->+TR|ε
T->FY
Y->*FY|ε
F->(E)|i
```

---

## 🔹 Lab 6 – Predictive Parsing Table (LL(1))

### Objective:

To construct a Predictive Parsing Table using FIRST and FOLLOW sets.

### Description:

* Generates LL(1) parsing table
* Checks grammar suitability for predictive parsing
* Displays table format for parsing process

---

## 🔹 Lab 7 – Shift Reduce Parsing

### Objective:

To implement Bottom-Up Parsing using Shift Reduce technique.

### Features:

* Stack-based parsing simulation
* Shows Shift and Reduce operations
* Step-by-step parsing output
* Accepts input string and grammar

---

## 🔹 Lab 8 – Computation of LEADING and TRAILING

### Objective:

To compute LEADING and TRAILING sets for operator precedence grammar.

### Description:

* Finds leading symbols of non-terminals
* Finds trailing symbols of non-terminals
* Useful for operator precedence parsing

Example Input:

```
E->E+T|T
T->T*F|F
F->(E)|i
```

---

# 🛠️ Technologies Used

* Python 3.x
* Standard Python Libraries
* Command Line Interface (CLI)
* GitHub for version control

---

# ▶️ How to Run the Programs

## Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/COMPILER-DESIGN-LAB.git
cd COMPILER-DESIGN-LAB
```

## Step 2: Run Any Lab File

Example:

```bash
python Lab1_Lexical_Analyzer.py
```

```bash
python Lab2_RE_to_NFA.py
```

```bash
python Lab4_LeftRecursion_LeftFactoring.py
```

---

# 🧾 Input Format Guidelines

## 🔹 For Regular Expressions (Lab 2)

Operators to use:

```
.  → Concatenation
|  → Union
*  → Kleene Star
```

Valid Examples:

```
a.b
a|b
a*
a.b*
```

---

## 🔹 For Grammar-Based Labs (Lab 4, 5, 6, 8)

Use standard production format:

```
A->Aa|b
E->E+T|T
S->iEtS|a
```

⚠️ Important Rules:

* Do NOT use spaces
* Use `->` for production
* Use `|` to separate alternatives

---

# 📊 Sample Test Inputs

### Lab 1:

```
int a = 10;
float b = a + 5;
```

### Lab 2:

```
a.b
a|b
a*
```

### Lab 3:

Predefined NFA transitions inside the program

### Lab 4:

```
A->Aa|b
A->ab|ac
S->Sa|b
```

### Lab 5:

```
E->TR
R->+TR|ε
T->FY
Y->*FY|ε
F->(E)|i
```

### Lab 6:

Same grammar as FIRST & FOLLOW

### Lab 7:

```
Input String: id+id*id
Grammar: E->E+E|E*E|id
```

### Lab 8:

```
E->E+T|T
T->T*F|F
F->(E)|i
```

---

# 🎯 Learning Outcomes

After completing this lab, students will be able to:

* Understand phases of a compiler
* Implement lexical analysis
* Convert RE to NFA and NFA to DFA
* Transform grammars (Left Recursion & Factoring)
* Compute FIRST and FOLLOW sets
* Construct Predictive Parsing Tables
* Perform Shift Reduce Parsing
* Compute LEADING and TRAILING sets

---

# 📚 Reference Books

1. Alfred V. Aho, Monica S. Lam, Ravi Sethi, Jeffrey D. Ullman – *Compilers: Principles, Techniques, and Tools*
2. Aho & Ullman – *Principles of Compiler Design*
3. K. Muneeswaran – *Compiler Design*
4. John E. Hopcroft – *Introduction to Automata Theory, Languages and Computation*

---
