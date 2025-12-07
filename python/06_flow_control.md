# 📘 **Sub-Topic 6: Flow of Control in Python**

**Flow of control** refers to the order in which statements are executed.

Python follows three types of flows:
- **Sequential**
- **Conditional**
- **Iterative (Loops)**

---

## ⭐ **1. Introduction**

A program’s flow decides:
- Which statements run
- When a decision is made
- How often a piece of code repeats

Python uses **indentation** instead of braces `{}` to structure control flow.

---

## ⭐ **2. Indentation in Python**

### **Concept**
- **Indentation** = spaces at the beginning of a line → defines code blocks.
- Python requires **consistent indentation**.
- Default style: **4 spaces** (recommended but not mandatory).

### **✔ Valid Example**
```python
if x > 10:
    print("Large")
    print("Done")
```

### **❌ Invalid Example**
```python
if x > 10:
  print("Large")
    print("Done")  # inconsistent
```
**Error:** `IndentationError`

---

### **MCQ Notes**
- Python uses **indentation** to define blocks.
- Indentation errors are **syntax errors**.
- **Mixing tabs & spaces** can cause errors.

---

## ⭐ **3. Sequential Flow**

### **Concept**
Statements execute **one after another** in order.

**Example:**
```python
print("Start")
x = 10
y = x * 2
print("Result =", y)
print("End")
```

---

## ⭐ **4. Conditional Flow (Decision-Making)**

Used to execute certain statements based on **conditions**.

### **Keywords:** `if`, `if-else`, `if-elif-else`

#### **✔ Example 1: Simple if**
```python
if x > 0:
    print("Positive")
```

#### **✔ Example 2: if-else**
```python
if n % 2 == 0:
    print("Even")
else:
    print("Odd")
```

#### **✔ Example 3: if-elif-else**
```python
if marks >= 90:
    print("A")
elif marks >= 75:
    print("B")
elif marks >= 60:
    print("C")
else:
    print("D")
```

### **❌ Common Mistakes**
- Missing colon `:`
- Using `=` instead of `==`
- Incorrect indentation
- Not realizing that **only first True condition** in an `elif` chain executes

---

## ⭐ **5. Iterative Flow (Loops)**

Used to execute a block **multiple times**.

### **Types:**
- **for loop**
- **while loop**

---

### **✔ A. for loop**
**Example:**
```python
for i in range(1, 6):
    print(i)
```

**How `range()` works:**
- `range(n)` → 0 to n-1
- `range(start, stop)` → start to stop-1
- `range(start, stop, step)` → step increments

---

### **✔ B. while loop**
**Example:**
```python
i = 1
while i <= 5:
    print(i)
    i += 1
```

**Using break:**
```python
for i in range(10):
    if i == 5:
        break
```

**Using continue:**
```python
for i in range(10):
    if i % 2 == 0:
        continue
```

---

### **❌ Common Human Errors**
- Infinite loops due to missing updates in `while`
- Off-by-one errors
- Using `range(1,10)` expecting it to include 10
- Indentation mistakes

---

## ⭐ **6. Full Demonstration Code**
```python
# Sequential
x = 10
y = x + 5
print("y =", y)

# Conditional
if y > 10:
    print("Greater")
else:
    print("Smaller or equal")

# Iterative
for i in range(5):
    print("i =", i)

# While loop
count = 3
while count > 0:
    print(count)
    count -= 1
```

---

## ⭐ **7. Exceptions & Error Scenarios in Flow Control**

| Error Type | Example | Reason |
|-------------|----------|---------|
| **IndentationError** | ```python
if x > 0:
print("Positive")
``` | Missing indentation |
| **Infinite Loop** | ```python
while x > 0:
    print(x)  # missing x -= 1
``` | Condition never changes |
| **NameError** | ```python
if value > 10:  # value not defined
``` | Undefined variable |

---

## ⭐ **8. Exam-Focused Notes Summary**

| Concept | Key Point |
|----------|------------|
| **Syntax Errors** | Occur **before** program runs |
| **Runtime Errors** | Occur **while running** |
| **Logical Errors** | Program runs but output is wrong |
| **Indentation** | Required to define code blocks |
| **Sequential Flow** | Default order of execution |
| **Conditional Flow** | Runs based on condition |
| **Iterative Flow** | Repeats code block |
| **range()** | Stops **one before** stop value |
| **IndentationError** | Common mistake in exams |

---

📚 *These notes comprehensively explain Python’s flow of control — Sequential, Conditional, and Iterative — with syntax, examples, and common EMRS exam traps.*

