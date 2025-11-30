# 📘 Sub-Topic 2: Knowledge of Data Types in Python

Python has built-in data types grouped into:

✔ Number  
✔ Boolean  
✔ Sequence (string, list, tuple)  
✔ Mapping (dictionary)  
✔ None Type  
✔ Mutability concept (mutable vs immutable)

Understanding these is heavily tested in TGT/PGT exams through MCQs.

---

## 1. Numeric Data Types
Python supports three numeric types:

### 1️⃣ Integer (int)
**Concept**
- Whole numbers without decimal.
- No limit on size (Python handles big integers automatically).

**Example**
```python
a = 10
b = -25
c = 10000000000    # Valid large integer
```

**Important Notes**
- No need to specify type (int, long, etc.) → Python has only int.
- Arithmetic operations produce int or float based on operands.

**Common Errors**
```python
x = int("10.5")  # ❌ ValueError (string has decimal point)
```

---

### 2️⃣ Floating Point (float)
**Concept**
- Numbers with decimals.

**Example**
```python
pi = 3.14
rate = -0.99
```

**Scientific notation allowed**
```python
x = 1.2e3   # 1200.0
```

**Common Issues**
Floating-point precision:
```python
print(0.1 + 0.2)  # 0.30000000000000004
```

---

### 3️⃣ Complex Numbers (complex)
**Concept**
Python natively supports complex numbers as:
```python
a + bj
```

**Example**
```python
z = 3 + 5j
print(type(z))  # <class 'complex'>
```

**Access real/imag parts**
```python
z.real   # 3.0
z.imag   # 5.0
```

**Common Error**
```python
z = 4 + 5J   # ❌ SyntaxError
```
Correct:
```python
z = 4 + 5j
```

---

## 2. Boolean Data Type
**Concept**
Boolean represents truth values:
- True
- False

**Example**
```python
x = True
y = False
```

**Boolean results from comparisons**
```python
print(5 > 3)     # True
print(10 == 2)   # False
```

**Booleans behave like integers**
- True = 1
- False = 0
```python
print(True + True)  # 2
```

**Common MCQ Trap**
- `true` and `false` (lowercase) are invalid identifiers.

---

## 3. Sequence Data Types
Sequence = ordered collection of items.
Python supports:
- String
- List
- Tuple

---

### 1️⃣ String (str)
**Concept**
A sequence of characters enclosed within quotes.
```python
s = "Hello"
```

**Characteristics**
- Ordered
- Indexed
- Immutable
- Support slicing
- Support membership (`in`)

**Examples**
```
s[0]      # 'H'
s[-1]     # 'o'
s[1:4]    # 'ell'
```

**String methods (from syllabus)**
upper(), lower(), capitalize(), title()  
count(), find(), index()  
strip(), lstrip(), rstrip()  
startswith(), endswith()  
split(), join()  
replace()  
isalpha(), isdigit(), isalnum(), etc.

---

### 2️⃣ List (list)
**Concept**
Ordered, mutable sequence of items.
```python
nums = [10, 20, 30]
mixed = [1, "abc", 3.14, True]
```

**Characteristics**
- Can modify elements.
- Supports slicing & membership.
- Nested lists allowed.

**Examples**
```python
nums[1] = 200
```

**Common Mistake**
```python
a = [1,2,3]
b = a
b.append(4)
print(a)    # [1,2,3,4]
```
Both refer to same list → mutability.

---

### 3️⃣ Tuple (tuple)
**Concept**
Ordered, immutable sequence.
```python
t = (10, 20, 30)
```

**Single-value tuple**
```python
x = (5)     # int
x = (5,)    # tuple ✔
```

**Why tuples?**
- Faster
- Safe from modification
- Used as dictionary keys

**Common Error**
```python
t[0] = 100   # ❌ TypeError
```

---

## 4. Mapping Data Type: Dictionary
**Concept**
Stores key–value pairs.
```python
emp = {"name": "Amit", "salary": 50000}
```

**Characteristics**
- Keys must be immutable.
- Values can be anything.
- Mutable.
- Ordered (Python 3.7+).

**Access**
```python
emp["name"]
```

**Add/Modify**
```python
emp["age"] = 25
emp["salary"] = 60000
```

**Common Errors**
1️⃣ Missing key:
```python
emp["address"]   # ❌ KeyError
```
Use:
```python
emp.get("address")
```

2️⃣ Using mutable keys:
```python
d = {[1,2]: "abc"}  # ❌ TypeError
```

---

## 5. None Type
**Concept**
Represents no value.
```python
x = None
```
Used in:
- Function returns nothing
- Default values
- Placeholders

**Common Confusion**
```python
None != 0
None != ""
None != False
```

---

## 6. Mutable vs Immutable Data Types

### Immutable
- int, float, complex
- string
- tuple
- bool
- NoneType
```python
s = "hello"
s[0] = 'H'   # ❌ TypeError
```

### Mutable
- list
- dictionary
- set
```python
l = [1,2,3]
l[1] = 20   # ✔
```

**Why important?**
Affects memory, assignment, identity, function arguments.

---

## 7. Code Examples
```python
# Numeric types
i = 10
f = 10.5
c = 3 + 4j

# Boolean
flag = True

# String
s = "Python"

# List
lst = [1, 2, 3]

# Tuple
tup = (10, 20, 30)

# Dictionary
d = {"name": "Amit", "age": 25}

# None type
x = None
```

---

## 8. Exception Cases / Error Scenarios
```python
# String modification
a = "abc"
a[0] = 'x'   # TypeError

# Tuple modification
t = (1,2,3)
t[1] = 50    # TypeError

# Dictionary key missing
emp["dept"]  # KeyError

# List index out of range
lst = [1,2]
lst[5]        # IndexError

# Invalid complex
z = 4 + j5    # SyntaxError

# Mutable key in dict
d = {[1,2]: "hi"}   # TypeError
```

---

## 9. Common Human Errors (Important for EMRS)
❌ Confusing immutable & mutable types  
❌ Forgetting comma in a single-value tuple  
❌ Wrong dictionary access (`d.key` instead of `d["key"]`)  
❌ Mixing numbers with strings during input  
❌ Capital `J` in complex numbers  
❌ Assuming Python mishandles large integers

