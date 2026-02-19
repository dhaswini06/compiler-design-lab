
# 📄 README.md (Lab 2 – Regular Expression to NFA)

```markdown
# 🔬 Lab 2 – Conversion of Regular Expression to NFA (Thompson Construction)

## 📘 Subject
Compiler Design Laboratory

## 👩‍🎓 Experiment Title
Conversion of Regular Expression to Non-Deterministic Finite Automaton (NFA)

---

## 📌 Objective
To design and implement a program that converts a given Regular Expression into an equivalent Non-Deterministic Finite Automaton (NFA) using Thompson’s Construction method.

---

## 🧠 Theory
A Regular Expression (RE) is a formal notation used to describe patterns in strings. In compiler design, regular expressions are used in lexical analysis to define token patterns.

An NFA (Non-Deterministic Finite Automaton) is a finite automaton where multiple transitions for a single input symbol are allowed, including epsilon (ε) transitions.

Thompson’s Construction is a standard algorithm used to convert a Regular Expression into an equivalent NFA. It works by:
- Converting infix regular expression to postfix
- Constructing small NFAs for operands
- Combining them using operators like union (|), concatenation (.), and Kleene star (*)

---

## ⚙️ Algorithm
1. Read the input regular expression.
2. Convert the infix regular expression to postfix notation.
3. Create basic NFA for each operand (symbol).
4. Apply Thompson’s Construction rules:
   - Union (|): Create new start and accept states with ε transitions.
   - Concatenation (.): Connect first NFA accept state to second NFA start state.
   - Kleene Star (*): Add ε transitions to allow repetition.
5. Display the start state, accept state, and transition table of the NFA.

---

## 🖥️ Program Description
This Python program converts a user-given regular expression into an equivalent NFA using Thompson’s Construction.  
It supports:
- Union operator (|)
- Concatenation operator (.)
- Kleene star (*)
- Parentheses ( )

The program also converts infix expressions to postfix internally for correct NFA generation.

---

## 📂 File Structure
```

Lab2_RE_to_NFA.py   # Main Python program
README.md           # Documentation for Lab 2

````

---

## ▶️ How to Run the Program

### Step 1: Install Python
Make sure Python 3 is installed on your system.

### Step 2: Clone the Repository (or download files)
```bash
git clone https://github.com/your-username/compiler-design-lab.git
cd compiler-design-lab
````

### Step 3: Run the Program

```bash
python Lab2_RE_to_NFA.py
```

---

## 🧪 Sample Inputs and Outputs

### Sample Input 1:

```
a|b
```

Output:

* Postfix Expression
* Start State
* Accept State
* NFA Transition Table

### Sample Input 2:

```
a.b
```

### Sample Input 3:

```
(a|b).c
```

---

## 📥 Valid Input Format

| Operator | Meaning       |       |
| -------- | ------------- | ----- |
| `.`      | Concatenation |       |
| `        | `             | Union |
| `*`      | Kleene Star   |       |
| `( )`    | Grouping      |       |

Example valid expressions:

```
a|b
a.b
a*
(a|b).c
a.b*
```

---

## 📊 Output

The program displays:

* Postfix Expression
* Start State of NFA
* Accept State of NFA
* NFA Transition Table with ε-transitions

---

## 🛠️ Requirements

* Python 3.x
* No external libraries required

---

## 🎯 Result

The program successfully converts a given Regular Expression into its equivalent Non-Deterministic Finite Automaton (NFA) using Thompson’s Construction method and displays the transition table correctly.
  
so your GitHub looks fully complete and professional?
```
