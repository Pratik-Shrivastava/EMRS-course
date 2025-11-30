# 📘 Python Basics – Structured Notes (EMRS-Oriented)

## 1. Introduction to Python
Python is a **high-level**, **interpreted**, **general-purpose**, **object‑oriented** programming language created by **Guido van Rossum (1991)**.

### Where Python is used?
- Web development
- Data science & ML
- Automation & scripting
- Application development
- School/college programming
- EMRS/TGT CS exams

---

## 1.1 Key Features of Python
### ✔ 1. Easy & Readable
- English‑like syntax
- No braces `{}`
- Uses **indentation** to define blocks

### ✔ 2. Interpreted Language
- Executes code **line‑by‑line**
- No compilation needed

### ✔ 3. Dynamically Typed
No need to declare data type:
```python
x = 10      # int
x = "abc"   # now string
```

### ✔ 4. High-Level
- Programmer doesn’t manage memory manually.

### ✔ 5. Portable & Cross‑Platform
- Same code runs on **Windows, Linux, Mac**.

### ✔ 6. Large Standard Library
- Modules like: `math`, `csv`, `random`, `statistics`, etc.

---

## 2. Executing a Simple “Hello World” Program
### **Example:**
```python
print("Hello World")
```
### Explanation
- `print()` → built-in function
- Parentheses required in Python 3
- Prints output on the console

---

## 3. Execution Modes in Python
Python provides **two modes**:

---
###  A. Interactive Mode (REPL)
**REPL = Read → Evaluate → Print → Loop**

**Used for:**
- Quick tests
- Trying functions
- Evaluating expressions

**Example:**
```
>>> print("Hello")
Hello
>>> 10 + 5
15
```
**Exam Points (MCQs):**
- “Which mode executes one statement at a time?” → **Interactive Mode**
- “Which mode uses prompt `>>>`?” → **Interactive Mode**

---
### B. Script Mode
Code written in a **.py file** and executed.

**Example:**
```python
# File: hello.py
print("Hello World from Script")
```
Run using:
```
python hello.py
```
**Used for:**
- Full programs
- Assignments
- EMRS “Write a Python script” questions

---

## 4. Python Character Set
Python uses:
- **Letters** → A–Z, a–z
- **Digits** → 0–9
- **Whitespace** → space, tab, newline
- **Special Symbols** → `+ - * / = ( ) [ ] { } : , . ' " @ # % ^ &`

Character set helps define: **tokens, identifiers, keywords**.

---

## 5. Python Tokens
Smallest units of a Python program.

### Types of Tokens:

---
### 1️⃣ Keywords
Predefined meaning.

Examples:
`if, else, for, while, True, False, None, import, class, return`

**Exam Note:**
- Keywords are **case‑sensitive** → `True ≠ true`
- Cannot be used as identifiers: ❌ `for = 10`

---
### 2️⃣ Identifiers (Names)
Used for variables, functions, classes.

**Rules:**
- Must start with **letter or underscore**
- Cannot start with digit
- Case‑sensitive
- Cannot use keywords
- No spaces allowed

**Valid:**
```
name
_age
roll2
```
**Invalid:**
```
2name
my name
class
```

---
### 3️⃣ Literals (Fixed values)
- Integer → `10`
- Float → `10.5`
- String → "hello"
- Boolean → `True, False`
- None → `None`
- List → `[1,2,3]`
- Dictionary → `{"a":10}`

---
### 4️⃣ Operators
- **Arithmetic** → `+ - * / % // **`
- **Relational** → `< <= > >= == !=`
- **Logical** → `and or not`
- **Assignment** → `= += -=`
- **Membership** → `in, not in`
- **Identity** → `is, is not`

---
### 5️⃣ Punctuators
```
() [] {} : , . ; ' '
```
Used in: functions, lists, dictionaries, strings.

---

## 6. Variables
A variable is a **name referring to a value** stored in memory.
```python
x = 100
name = "Pratik"
```
Python is **dynamically typed** → type assigned at runtime.

---

## 7. l-value and r-value
- **l-value** → left side of `=` (location)
- **r-value** → right side of `=` (value)

```python
x = 10
```
x → l-value
10 → r-value

❌ Invalid:
```python
10 = x   # SyntaxError
```

---

## 8. Comments
Interpreter ignores comments.

### Single-line:
```python
# This is a comment
```
### **Multi-line:**
```python
"""
This is a
multi-line comment
"""
```
Used for documentation, logic explanation.

---

## 9. Code Example (Covers All Concepts)
```python
# Single-line comment
"""
This program demonstrates
basic Python features
"""

# Variables and tokens
name = "EMRS"      # identifier + string literal
year = 2025        # integer literal

# l-value and r-value
x = 10

y = x + 5          # operator and literal

print("Hello World")
print("Value of y:", y)
```

---

## 10. Exception / Error Scenarios
### ❌ 1. Invalid Identifier
```python
2name = "abc"
```
→ SyntaxError

### ❌ 2. Keyword as Identifier
```python
for = 10
```
→ SyntaxError

### ❌ 3. Missing Parentheses
```python
print "Hello"
```
→ SyntaxError

### ❌ 4. Indentation Error
```python
print("Hi")
 print("Hello")
```
→ IndentationError

### ❌ 5. Wrong Quotes
```python
msg = 'Hello"
```
→ EOL while scanning string literal

---

## 11. Common Human Errors (EMRS Important)
❌ Using spaces in variable names
```python
my name = "Pratik"
```

❌ Confusing `=` with `==`
```python
if x = 5:   # wrong
```
✔ Correct:
```python
if x == 5:
```

❌ Assuming Python is case-insensitive → `Print` ≠ `print`

❌ Using Python 2 syntax → `print "hello"`

❌ Using keywords as identifiers → `None = 5`

❌ Forgetting `input()` returns string
```python
x = input()   # x is string
```

