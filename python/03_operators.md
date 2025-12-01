# 📘 Sub-Topic 3: Operators in Python

(Arithmetic, Relational, Logical, Assignment, Augmented Assignment, Identity, Membership)

Operators perform operations on variables and values.
Python operators are heavily tested in EMRS exams through MCQs.

---

## ⭐ 1. Arithmetic Operators
| Operator | Meaning | Example |
|---------|---------|---------|
| `+` | Addition | `10 + 5` |
| `-` | Subtraction | `10 - 5` |
| `*` | Multiplication | `10 * 5` |
| `/` | Division (float result) | `10 / 4 = 2.5` |
| `//` | Floor division | `10 // 4 = 2` |
| `%` | Modulus (remainder) | `10 % 4 = 2` |
| `**` | Exponentiation | `2 ** 3 = 8` |

### ✔ Concepts & Examples
**1. True Division `/`**
- Always produces float, even if evenly divisible.
```python
print(10 / 2)   # 5.0
```

**2. Floor Division `//`**
- Removes decimal digits → gives the floor value.
```python
print(10 // 3)  # 3
print(-10 // 3) # -4
```

**3. Modulus `%`**
- Returns remainder.
```python
print(10 % 3)   # 1
print(-10 % 3)  # 2
```

**4. Exponent `**`**
```python
print(2 ** 5)   # 32
print(9 ** 0.5) # 3.0
```

### ❌ Common Mistakes (MCQ Traps)
- `10 / 3 = 3.333...` (float)
- `10 // 3 = 3` but `-10 // 3 = -4`
- `%` differs for negative numbers
- `2 ^ 3` is NOT exponent → bitwise XOR

---

## ⭐ 2. Relational (Comparison) Operators
Used to compare values; return True/False.

| Operator | Meaning |
|----------|---------|
| `<` | Less than |
| `>` | Greater than |
| `<=` | Less than or equal |
| `>=` | Greater than or equal |
| `==` | Equal to |
| `!=` | Not equal to |

### ✔ Examples
```python
print(5 < 10)    # True
print(5 == "5")  # False (different types)
print(5 != 5.0)  # False (equal in value)
```

### ❌ Common Mistakes
- Using `=` instead of `==`
```python
if x = 5:   # Wrong
```
- Comparing incompatible types:
```python
"abc" < 5   # TypeError
```

---

## ⭐ 3. Logical Operators
| Operator | Meaning |
|----------|---------|
| `and` | True if both are True |
| `or` | True if at least one is True |
| `not` | Negates Boolean |

### ✔ Examples
```python
print(True and False)   # False
print(True or False)    # True
print(not True)         # False
```

**Using in comparisons**
```python
a = 10
print(a > 5 and a < 20)      # True
print(a < 5 or a == 10)      # True
print(not (a == 10))         # False
```

### ❌ Common Errors / Traps
- `and` has higher precedence than `or`
- `and/or` sometime returns **values**, not booleans:
```python
print(5 and 10)   # 10
print(0 or 20)    # 20
```

---

## ⭐ 4. Assignment Operator
### Basic assignment
```python
x = 10
name = "Python"
```

### Multiple assignment
```python
a = b = c = 5
x, y = 10, 20
```

### Swap
```python
a, b = b, a
```

---

## ⭐ 5. Augmented Assignment Operators
| Operator | Equivalent to |
|----------|----------------|
| `+=` | `x = x + value` |
| `-=` | `x = x - value` |
| `*=` | `x = x * value` |
| `/=` | `x = x / value`|
| `//=` | `x = x // value` |
| `%=` | `x = x % value` |
| `**=` | `x = x ** value` |

### ✔ Example
```python
x = 10
x += 5   # x = 15
x *= 2   # x = 30
```

**Works with strings & lists**
```python
s = "Hi"
s += " there"   # "Hi there"

lst = [1,2]
lst += [3,4]    # [1,2,3,4]
```

### ❌ Common Mistake
- Using `+=` with incompatible types causes TypeError:
```python
x = "Hello"
x += 5   # ❌ TypeError
```

---

## ⭐ 6. Identity Operators (`is`, `is not`)
Identity operators check `memory location`, not value.

| Operator | Meaning |
|----------|---------|
| `is` | True if both refer to same object |
| `is not` | True if not same object |

### ✔ Examples
**Case 1: Same object**
```python
a = [1,2,3]
b = a
print(a is b)  # True
```

**Case 2: Different objects, same value**
```python
x = [1,2,3]
y = [1,2,3]
print(x == y)  # True
print(x is y)  # False
```

**Small integer caching**
```python
a = 10
b = 10
print(a is b)  # True (same chache object)
```

### ❌ Common Mistake
- Using `is` instead of `==`:
```python
x = 1000
y = 1000
print(x is y)  # False (different objects)
```
- For strings, Python may cache some literals, leading to confusing results.

---

## ⭐ 7. Membership Operators (`in`, `not in`)
Used to check if a value **exists** inside `sequence`, `string`, or `dictionary`.

| Operator | Meaning |
|----------|---------|
| `in` | True if present |
| `not in` | True if not present |

### ✔ Examples
**With strings**
```python
print("py" in "python")  # True
```

**With lists**
```python
lst = [10,20,30]
print(20 in lst)         # True
print(40 not in lst)     # True
```

**With dictionary keys**
```python
d = {"name": "Amit", "age": 25}
print("name" in d)     #  True (checks keys)
print("Amit" in d)     # False
```
- Important exam trap:
- `in` checks dictionary **keys**, not values.

**To Check values:**
```python
"Amit" in d.values()
```

### ❌ Common Mistakes
```python
5 in 12345  # ❌ TypeError
```
- Expecting dictionary membership to check values, NOT True by default.


---

## ⭐ 8. Summary Comparison (Quick Revision Table)
| Operator Type | Examples | Returns |
|---------------|----------|---------|
| Arithmetic | + - * / // % ** | Number |
| Relational | > < >= <= == != | Boolean |
| Logical | and, or, not | Boolean / value |
| Assignment | = | Assigns value |
| Augmented | += -= *= | Modified variable |
| Identity | is, is not | True/False |
| Membership | in, not in | True/False |

---

## ⭐ 9. Full Code Demonstration
```python
# Arithmetic
a = 10
b = 3
print(a + b, a - b, a * b, a / b, a // b, a % b, a ** b)

# Relational
print(a > b, a == b, a != b)

# Logical
x = True
y = False
print(x and y, x or y, not x)

# Assignment
num = 5
num += 2   # 7

# Identity
lst1 = [1,2]
lst2 = [1,2]
print(lst1 is lst2)    # False

# Membership
print(2 in lst1)       # True
```

---

## ⭐ 10. Typical Exception Cases
**❌ Type mismatch**
```python
10 + "5"       # TypeError
```

**❌ Membership for non-iterable**
```python
5 in 10        # TypeError
```
**❌ Using `is` for numbers/string comparisons**
```python
'abc' is 'abc' # May be True (interning)
```
**❌ Zero division**
```python
10 / 0         # ZeroDivisionError
```

---

## ⭐ 11. Very Frequent Human Mistakes (Exam Favorites)
- Confusing `==` vs `is`
- Using `/` expecting integer result

- Believing `a = b = []` creates two separate lists
(It creates SAME object!)

- Thinking `%` always gives positive result (not with negative numbers)

- Using `in` to search values inside a dictionary
(Searches keys only!)

- Writing `notin` instead of `not in`
(must be two words)

