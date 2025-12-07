# 📘 **Sub-Topic 5: Errors in Python**

Errors indicate problems in a program. Python categorizes errors mainly as:

- **Syntax Errors**  
- **Runtime Errors (Exceptions)**  
- **Logical Errors**

These types appear frequently in **MCQs and debugging questions** in EMRS exams.

---

## ⭐ **1. Syntax Errors (Compile-Time Errors)**

### **Concept**
- Occur **before execution**, during the parsing stage.  
- Caused by incorrect **Python syntax**.
- Python **cannot run the code** until they are fixed.

### **Examples:**

#### ❌ Missing colon
```python
if x > 10
    print("OK")
```
**Error:**  
`SyntaxError: invalid syntax`

#### ❌ Incorrect indentation
```python
print("Hello")
 print("World")
```
**Error:**  
`IndentationError: unexpected indent`

#### ❌ Missing parentheses in Python 3
```python
print "Hi"
```
**Error:**  
`SyntaxError: Missing parentheses in call to 'print'`

#### ❌ Unbalanced quotes
```python
msg = "hello'
```
**Error:**  
`SyntaxError: EOL while scanning string literal`

---

### **Common Causes (Exam Focus)**
- Missing `:` after `if`, `for`, `while`, `else`, `elif`
- Using **Python 2 print syntax**
- Using `=` instead of `==` inside conditions
- Wrong indentation
- Invalid identifiers (e.g., `2name`, `class`)

---

## ⭐ **2. Runtime Errors (Exceptions)**

### **Concept**
- Occur **during execution**, after the program starts running.
- Python **stops execution** and raises an **exception**.

### **Common Runtime Errors:**

| Error Type | Example | Description |
|-------------|----------|--------------|
| **ZeroDivisionError** | `x = 10 / 0` | Division by zero not allowed |
| **ValueError** | `int("abc")` | Invalid literal for conversion |
| **TypeError** | `10 + "5"` | Operation between incompatible types |
| **IndexError** | `lst = [1,2]; print(lst[5])` | Index out of range |
| **KeyError** | `d = {"a":10}; print(d["b"])` | Missing dictionary key |
| **NameError** | `print(x)` | Variable not defined |
| **FileNotFoundError** | `open("abc.txt", "r")` | File does not exist |

---

### **MCQ Traps (Runtime Errors)**
- Using incorrect types → **TypeError**
- Accessing missing dictionary key → **KeyError**
- Dividing integers by zero → **ZeroDivisionError**

---

## ⭐ **3. Logical Errors**

### **Concept**
- Program runs **without crashing**, but produces **incorrect output**.
- Hardest to detect — **no error message displayed.**

### **Examples:**

#### Example 1 – Wrong formula
```python
# Mistake: dividing by 2 instead of 3
avg = (a + b + c) / 2
```
✅ Program runs → ❌ Output is wrong.

#### Example 2 – Off-by-one error
```python
for i in range(1, 10):   # prints 1 to 9, not 10
    print(i)
```

---

### **MCQ Traps (Logical Errors)**
- Logical errors **do not stop program execution**.
- **No exceptions** are raised.
- Output is **incorrect or unexpected**.

---

📚 *These notes summarize all key error types and examples commonly asked in EMRS Python exams — Syntax, Runtime, and Logical errors.*

