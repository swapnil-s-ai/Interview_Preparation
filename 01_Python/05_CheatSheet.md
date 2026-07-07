# Python Cheat Sheet

> ⭐⭐⭐⭐⭐ Priority | ⭐☆☆☆☆ Difficulty | Very High Interview | ⏱ 15 min | 🔄 Before Every Interview

---

# Collections

| Type | Ordered | Mutable | Duplicate |
|------|---------|----------|-----------|
| List | ✅ | ✅ | ✅ |
| Tuple | ✅ | ❌ | ✅ |
| Set | ❌ | ✅ | ❌ |
| Dictionary | ✅ | ✅ | Keys Unique |

---

# Copy

```python
y = x              # Reference
copy.copy(x)       # Shallow
copy.deepcopy(x)   # Deep
```

---

# Comparison

```python
==

Compare Value
```

```python
is

Compare Identity
```

---

# Functions

```python
*args

Tuple
```

```python
**kwargs

Dictionary
```

---

# Collections Module

```python
Counter()

defaultdict()

deque()
```

---

# Useful Built-in Functions

```python
zip()

enumerate()

sorted()

reversed()

any()

all()

sum()

max()

min()
```

---

# Comprehension

```python
[x for x in data]

{x:x*x for x in data}
```

---

# Generator

```python
yield
```

Memory Efficient

---

# Decorator

```python
@decorator
```

Wraps existing function.

---

# Common Interview Mistakes

- Mutable default argument
- `is` vs `==`
- `append` vs `extend`
- `sort` vs `sorted`
- Shallow vs Deep Copy

---

# Personal Weak Areas

- Counter
- Decorators
- `*args`
- `**kwargs`
- `loc`
- `iloc`
