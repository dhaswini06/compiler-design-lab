# Lab 8 – Computation of LEADING and TRAILING

## 📌 Experiment Title
Computation of LEADING and TRAILING Sets in Compiler Design

## 🎯 Objective
To implement a Python program to compute the LEADING and TRAILING sets for a given context-free grammar (CFG).

## 🧾 Description
LEADING and TRAILING are important concepts used in Operator Precedence Parsing in Compiler Design. 
The LEADING set of a non-terminal contains the terminals that can appear at the beginning of strings derived from that non-terminal. 
The TRAILING set contains the terminals that can appear at the end of strings derived from that non-terminal.

This program accepts grammar productions from the user and automatically computes the LEADING and TRAILING sets using iterative algorithms.

## 🛠️ Features
- Supports multiple productions
- Handles terminals and non-terminals correctly
- Iterative computation until stable sets are formed
- Error handling for invalid input format
- Suitable for lab record and GitHub submission
- Clean and readable Python implementation

## 📥 Input Format
- Enter number of productions
- Enter productions in format: `A->aB|b` (No spaces)

Example:
E->E+T|T
T->T*F|F
F->(E)|i


## ▶️ Sample Input


Enter number of productions: 3
E->E+T|T
T->T*F|F
F->(E)|i


## 📤 Sample Output


LEADING Sets:
LEADING(E) = { (, i }
LEADING(T) = { (, i }
LEADING(F) = { (, i }

TRAILING Sets:
TRAILING(E) = { ), i }
TRAILING(T) = { ), i }
TRAILING(F) = { ), i }


## 🧠 Algorithm
1. Read grammar productions from user.
2. Initialize empty LEADING and TRAILING sets.
3. If first symbol is terminal → add to LEADING.
4. If last symbol is terminal → add to TRAILING.
5. If non-terminal appears, propagate its sets.
6. Repeat until no changes occur (fixed point).

## 📚 Applications
- Operator Precedence Parsing
- Syntax Analysis
- Compiler Construction
- Grammar Analysis in Parsing Techniques

## 💻 Language Used
Python 3

## 🧪 Subject
Compiler Design Laboratory
