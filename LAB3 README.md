# 🔬 Lab 3 – Conversion of NFA to DFA (Subset Construction)

## 📘 Subject
Compiler Design Laboratory

## 👩‍🎓 Experiment Name
Conversion of Non-Deterministic Finite Automaton (NFA) to Deterministic Finite Automaton (DFA)

---

## 🎯 Objective
To write a program to convert a given NFA into an equivalent DFA using the Subset Construction Algorithm.

---

## 🧠 Theory
A Non-Deterministic Finite Automaton (NFA) is a finite automaton where multiple transitions are allowed for a single input symbol and it may also include epsilon (ε) transitions.

A Deterministic Finite Automaton (DFA) is a finite automaton in which for every state and input symbol, there is exactly one transition.

The Subset Construction Algorithm is used to convert an NFA into an equivalent DFA by representing each DFA state as a set of NFA states.

---

## ⚙️ Algorithm
1. Read the NFA states, input symbols, transitions, start state, and final states.
2. Compute ε-closure of the start state.
3. Treat ε-closure as the initial DFA state.
4. For each DFA state and input symbol:
   - Find the move of the state set.
   - Compute ε-closure of the result.
5. Repeat until no new DFA states are generated.
6. Mark DFA states containing NFA final states as DFA final states.
7. Display DFA transition table.

---

## 💻 Program Description
This Python program converts a given NFA into an equivalent DFA using the Subset Construction Method.  
It supports epsilon (ε) transitions and dynamically generates DFA states and transition tables.

---
Lab3_NFA_to_DFA.py # Main Python program
README.md # Documentation for Lab 3


---

## ▶️ How to Run the Program

### Step 1: Install Python
Make sure Python 3.x is installed.

### Step 2: Run the Program
```bash
python Lab3_NFA_to_DFA.py

🧪 Sample Input
States: q0 q1 q2
Input Symbols: a b
Transitions:
q0 ε q1
q1 a q1
q1 b q2
q2 b q2
Start State: q0
Final State: q2

📊 Output

DFA States (as sets of NFA states)

DFA Transition Table

DFA Start State

DFA Final States

🛠️ Requirements

Python 3.x

No external libraries required (only built-in modules)

## 📂 File Structure
