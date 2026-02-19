# Lab 7 – Shift Reduce Parser

## 📌 Experiment Title
Implementation of Shift Reduce Parser in Python

## 🎯 Objective
To design and implement a Shift Reduce Parser to check whether a given input string is accepted by a specified context-free grammar (CFG).

## 🧾 Description
Shift Reduce Parsing is a bottom-up parsing technique used in compiler design to analyze and validate input strings based on a given grammar. The parser uses a stack and input buffer to perform shift and reduce operations. During parsing, symbols are shifted onto the stack and reduced using grammar productions until the start symbol is obtained.

This program simulates the working of a basic Shift Reduce Parser. It reads grammar productions, start symbol, and input string from the user and displays each parsing step including shift, reduce, accept, or reject actions.

## 🛠️ Features
- Accepts multiple grammar productions
- Step-by-step parsing table output
- Error handling for invalid inputs
- Supports multiple RHS productions using `|`
- Suitable for Compiler Design lab submission
- GitHub ready documentation and clean code

## 📥 Input Format
- Number of productions (integer)
- Productions in format: `A->aB|b` (No spaces)
- Start symbol
- Input string

## ▶️ Sample Input 1
Enter number of productions: 1
E->E+E|E*E|i
Enter start symbol: E
Enter input string: i+i


## ▶️ Sample Input 2


Enter number of productions: 3
E->E+T|T
T->TF|F
F->(E)|i
Enter start symbol: E
Enter input string: i+ii


## 📤 Sample Output


Step Stack Input Buffer Action
1 i+i$ Shift
2 i +i$ Reduce E->i
3 E +i$ Shift
...
String Accepted by Shift Reduce Parser.


## 🧠 Algorithm
1. Initialize stack as empty and append `$` to input buffer.
2. Shift symbols from input buffer to stack.
3. Check if stack suffix matches any RHS of grammar.
4. If matched, reduce RHS to LHS.
5. Repeat shift and reduce until:
   - Stack = Start Symbol and Input = `$` → Accept
   - Otherwise → Reject

## 📚 Applications
- Syntax Analysis in Compiler Design
- Bottom-Up Parsing
- LR Parsing concept understanding
- Educational simulation of parsing process

## 💻 Language Used
Python 3

## 🧪 Lab Course
Compiler Design Laboratory
