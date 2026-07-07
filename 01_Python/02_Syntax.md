# Python Syntax

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐☆☆☆ Difficulty | Very High Interview | ⏱ Living Document | 🔄 Before Every Interview

This file is a quick-reference guide for syntax that is commonly forgotten during interviews.

It is **not** intended to teach Python.

---

# Variables

```python
name = "Swapnil"
age = 30
salary = 100000.0
is_active = True
```

---

# Multiple Assignment

```python
a, b = 10, 20

a, b = b, a
```

---

# List

```python
numbers = [1, 2, 3]

numbers.append(4)

numbers.pop()

numbers.remove(2)

numbers.sort()

numbers.reverse()
```

---

# Tuple

```python
point = (10, 20)
```

---

# Set

```python
numbers = {1,2,3}

numbers.add(4)

numbers.remove(3)
```

---

# Dictionary

```python
employee = {
    "id":101,
    "name":"John"
}

employee["salary"] = 100

employee.get("salary")

employee.keys()

employee.values()

employee.items()
```

---

# List Comprehension

```python
square = [x*x for x in range(10)]
```

---

# Dictionary Comprehension

```python
square = {x:x*x for x in range(5)}
```

---

# Lambda

```python
square = lambda x: x*x
```

---

# Enumerate

```python
for index, value in enumerate(items):
    print(index, value)
```

---

# Zip

```python
for a, b in zip(list1, list2):
    print(a, b)
```

---

# Counter

```python
from collections import Counter

Counter(words)
```

⭐ Interview Favorite

Useful for:

- Frequency counting
- Duplicate detection
- Top-K problems

---

# *args

```python
def add(*args):
    print(args)
```

Tuple

---

# **kwargs

```python
def display(**kwargs):
    print(kwargs)
```

Dictionary

---

# Generator

```python
def numbers():
    yield 1
    yield 2
```

---

# Decorator

```python
@decorator
def func():
    pass
```

---

# Common Interview Mistakes

- `is` vs `==`
- `loc` vs `iloc`
- `append()` vs `extend()`
- `sort()` vs `sorted()`
- Mutable default arguments
- Shallow copy vs Deep copy
- `*args` vs `**kwargs`

> **Personal Focus:** Based on your diagnostic, these are the syntax areas you should revise frequently.
