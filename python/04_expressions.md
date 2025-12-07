# 📘 **Sub-Topic 4: Expressions, Statements, Type Conversion & Input/Output**

This topic is very important for **EMRS MCQs and short code questions**, especially focusing on **operator precedence, input handling, and type conversion**.

---

## ⭐ **1. Expressions in Python**

### **Concept**
An expression is any combination of:
- Variables  
- Literals  
- Operators  
- Function calls  

...that produces a value when evaluated.

### **Examples:**
```python
10 + 5
x * (y + 2)
a > b and b > c
```

Expressions can appear in:
- Assignments
- Conditions
- Loops
- Function arguments

---

## ⭐ **2. Evaluation of Expressions**

Python evaluates expressions using:
- **Precedence** (which operator executes first)
- **Associativity** (left-to-right or right-to-left)

**Example:**
```python
print(10 + 20 * 3)  
# 20 * 3 = 60 → 10 + 60 = 70
```

---

## ⭐ **3. Precedence of Operators (Very Important for MCQs)**

### **Order of Precedence (Highest → Lowest)**

| Level | Operators | Examples |
|--------|------------|-----------|
| 1 | `()` | Grouping, function calls |
| 2 | `**` | Exponent |
| 3 | `+ -` | Unary plus/minus (`-5`) |
| 4 | `* / // %` | Multiplicative |
| 5 | `+ -` | Addition, subtraction |
| 6 | `< <= > >=` | Relational |
| 7 | `== !=` | Equality |
| 8 | `not` | Logical negation |
| 9 | `and` | Logical AND |
| 10 | `or` | Logical OR |

### **Examples:**
```python
result = 10 + 20 * 3
print(result)      # 70

result = (10 + 20) * 3   # 90

x = 10
y = 5
print(x > y and x < 20)     # True

print(-2 ** 2)   # -4, NOT 4
```

### **Explanation:**
- `**` has higher precedence → `-(2 ** 2)` = `-4`

### **Common Mistakes (Exam Traps)**
- Writing `-2 ** 2` expecting 4 → actual result = **-4**.
- Forgetting `and` has higher precedence than `or`.
- Misunderstanding chained comparisons:
  ```python
  3 < 5 < 10   # True (evaluated as 3 < 5 and 5 < 10)
  ```

---

## ⭐ **4. Python Statements**

### **Concept:**
A **statement** is an instruction that Python can execute.

### **Types of Statements:**
- **Assignment:**
  ```python
  x = 10
  ```
- **Expression:**
  ```python
  print(5 + 3)
  ```
- **Control:**
  ```python
  if a > b:
      print("Yes")
  ```
- **Loop:**
  ```python
  for i in range(5):
      print(i)
  ```
- **Compound Statement:**
  ```python
  if x > 10:
      print("Big")
  ```

---

## ⭐ **5. Type Conversion**

Python supports **implicit** and **explicit** type conversion.

### ✔ A. **Implicit Type Conversion (Automatic)**
Python automatically converts smaller types to larger types when needed.

```python
x = 10     # int
y = 2.5    # float
z = x + y
print(z)   # 12.5 (float)
```
✅ Here, int → float implicitly.

```python
print(5 + 3j + 2)    # 7 + 3j
```
❌ **Limitation:** Python does not convert between incompatible types.
```python
print("10" + 5)     # TypeError
```

### ✔ B. **Explicit Type Conversion (Type Casting)**
Use built-in functions: `int()`, `float()`, `str()`, `bool()`, `list()`, `tuple()`.

**Examples:**
```python
int(5.89)     # 5
int("25")     # 25
int("25.5")   # ValueError
tuple([1,2,3])   # (1,2,3)
str(100) + "kg"   # '100kg'
```

---

## ⭐ **6. Accepting Input from Console**

### **Concept:**
`input()` is used to read user input — it **always returns a string**.

**Example:**
```python
name = input("Enter your name: ")
print("Hello", name)
```

### **Converting input to int/float:**
```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print("Sum =", a + b)

num = float(input("Enter decimal number: "))
```

❌ **Common Error:** Forgetting to convert input
```python
x = input()
y = input()
print(x + y)     # Concatenation, not addition!
```

---

## ⭐ **7. Displaying Output**

### **Basic print:**
```python
print("Hello EMRS")
```

### **Print multiple values:**
```python
print("Sum of numbers =", 25)
```

### **Using sep and end:**
```python
print("A","B","C", sep="-")     # A-B-C
print("Hello", end=" ")         # no newline
```

---

## ⭐ **8. Demonstration Code (All Concepts Together)**
```python
# Expression evaluation with precedence
x = 10 + 2 * 5        # 20
y = (10 + 2) * 5      # 60
z = -2 ** 2           # -4

# Input and type conversion
a = int(input("Enter a number: "))
b = float(input("Enter another number: "))

# Expression and statement
result = (a + b) * 2
print("Result is:", result)

# Explicit conversion
s = str(result)
print("As string:", s)
```

---

## ⭐ **9. Exception Cases / Error Scenarios**

| Error Type | Example |
|-------------|----------|
| **TypeError** | `print("10" + 5)` |
| **ValueError** | `int("abc")` |
| **ZeroDivisionError** | `x = 10 / 0` |
| **SyntaxError** | `print "Hello"` *(invalid in Python 3)* |
| **IndentationError** | Missing indentation |

---

## ⭐ **10. Common Human Errors (Exam Favorites)**

- Thinking `input()` returns number → it returns **string**.
- Using `/` expecting integer division (use `//` instead).
- Forgetting parentheses in `print`.
- Misunderstanding operator precedence.
- Incorrect type casting:
  ```python
  int("10.5")  # error
  ```
- Confusion with boolean conversion:
  ```python
  int(True)   # 1
  ```
- Incorrect chained comparison assumptions:
  ```python
  (3 < 5 < 10) == True   # Valid, evaluates as (3 < 5 and 5 < 10)
  ```
- Forgetting that **expressions produce values**, but **statements may not**.

---

📚 *These notes cover all essential EMRS exam points on expressions, statements, type conversion, input/output, and operator precedence.*

