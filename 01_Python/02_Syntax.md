# Python Syntax

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐☆☆☆ Difficulty | Very High Interview | ⏱ Living Document | 🔄 Before Every Interview

This document is a quick syntax reference for Python. It complements `01_Theory.md` by focusing on **how to write Python**, not **why Python works**.

---

# Block 01 — Fundamentals
> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐☆☆ Difficulty | Very High Interview | ⏱ 2–3h Study | 🔄 20m Revision

<details>
<summary>Contents</summary>

## Variables

### Syntax

```python
x = 10
name = "Swapnil"
is_active = True
salary = 10.5
```

### Multiple Assignment

```python
a, b = 10, 20

x = y = z = 0
```

### Variable Swap (Pythonic)

```python
a, b = b, a
```

### Delete Variable

```python
del x
```

### Best Practices

✅ Use meaningful variable names.

```python
employee_salary
customer_name
model_accuracy
```

❌ Avoid

```python
x
a
temp1
```

---

## Comments

```python
# Single line comment
```

```python
"""
Multi-line comment
or Docstring
"""
```

---

## Data Types

### Numeric

```python
x = 10          # int
y = 10.5        # float
z = 2 + 3j      # complex
```

### Boolean

```python
flag = True
```

### String

```python
name = "Python"
```

### Sequence

```python
list_obj = [1, 2]

tuple_obj = (1, 2)

range_obj = range(10)
```

### Mapping

```python
employee = {
    "id": 101,
    "name": "Swapnil"
}
```

### Set

```python
skills = {"Python", "SQL"}
```

---

## Type Checking

```python
type(x)
```

Preferred

```python
isinstance(x, int)
```

Multiple Types

```python
isinstance(value, (int, float))
```

---

## Type Conversion

```python
int("10")

float("10")

str(100)

bool(1)

list("ABC")

tuple([1,2])

set([1,2,2])

dict()
```

---

## Identity vs Equality

### Value Comparison

```python
a == b
```

### Object Identity

```python
a is b

a is not b
```

### Check None

✅

```python
if value is None:
```

❌

```python
if value == None:
```

---

## Mutable vs Immutable

Mutable

```python
list
dict
set
bytearray
```

Immutable

```python
int
float
bool
tuple
str
frozenset
```

---

## Truthy / Falsy

Falsy

```python
False
0
0.0
None
''
[]
{}
set()
```

Truthy

Everything else.

Example

```python
if items:
    print("Not Empty")
```

---

## Input / Output

```python
name = input("Name: ")

print(name)
```

Formatted Output

```python
print(f"Hello {name}")
```

---

## String Formatting

f-string (Recommended)

```python
name = "Swapnil"

print(f"Hello {name}")
```

format()

```python
print("Hello {}".format(name))
```

Old Style

```python
print("Hello %s" % name)
```

---

## Scope

Local

```python
def fun():
    x = 10
```

Global

```python
x = 10

def fun():
    global x
```

Nonlocal

```python
def outer():
    x = 10

    def inner():
        nonlocal x
```

---

## Useful Built-in Functions

```python
type()

id()

len()

print()

input()

range()

enumerate()

zip()

sorted()

reversed()

sum()

max()

min()

abs()

round()

any()

all()
```

---

## Pythonic Tips

Instead of

```python
if len(items) > 0:
```

Prefer

```python
if items:
```

---

Instead of

```python
if flag == True:
```

Prefer

```python
if flag:
```

---

## Interview Pitfalls

- `is` vs `==`
- Mutable default arguments
- Truthy vs Falsy
- Using `type()` instead of `isinstance()`
- Forgetting Python is strongly typed

---

## Production Notes

- Use `isinstance()` over `type()`.
- Prefer f-strings for formatting.
- Avoid global variables.
- Keep variable names descriptive.
- Use constants for configuration values.
</details>

---
# Block 02 — Collections
> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐☆☆ Difficulty | Very High Interview | ⏱ 2–3h Study | 🔄 20m Revision

<details>
<summary>Contents</summary>
    
Collections are one of the most frequently tested Python topics.

Interviewers expect you to know:
- Characteristics
- Time Complexity
- Common Methods
- Real-world Use Cases

---

# List

### Create

```python
numbers = [1, 2, 3]
```

### Common Methods

```python
append()

extend()

insert()

remove()

pop()

clear()

copy()

sort()

reverse()

index()

count()
```

### Access

```python
numbers[0]

numbers[-1]

numbers[1:4]
```

### Copy

```python
copy.copy()

copy.deepcopy()

numbers.copy()
```

### Pythonic

```python
squares = [x*x for x in range(10)]
```

### Interview Pitfalls

- append vs extend
- sort vs sorted
- shallow vs deep copy

---

# Tuple

### Create

```python
point = (10, 20)
```

Single Element

```python
value = (10,)
```

Packing

```python
person = 1, "Swapnil"
```

Unpacking

```python
id, name = person
```

Useful Functions

```python
count()

index()
```

Use Cases

- Configuration
- Coordinates
- Dictionary Keys

---

# Set

### Create

```python
numbers = {1,2,3}
```

Empty Set

```python
numbers = set()
```

Methods

```python
add()

update()

remove()

discard()

pop()

clear()
```

Operations

```python
a | b

a & b

a - b

a ^ b
```

Pythonic

```python
unique = set(data)
```

Interview Pitfalls

- `{}` creates Dictionary
- Sets are unordered
- No indexing

---

# Dictionary

### Create

```python
employee = {
    "id":101,
    "name":"Swapnil"
}
```

Access

```python
employee["name"]

employee.get("name")
```

Add

```python
employee["salary"] = 100
```

Update

```python
employee.update({"city":"Pune"})
```

Delete

```python
del employee["salary"]

employee.pop("salary")
```

Useful Methods

```python
keys()

values()

items()

get()

setdefault()

update()

copy()

pop()

popitem()
```

Dictionary Comprehension

```python
square = {x: x*x for x in range(5)}
```

Merge Dictionaries (Python 3.9+)

```python
c = a | b
```

Safe Lookup

```python
employee.get("salary", 0)
```

Interview Pitfalls

- `get()` vs indexing
- Mutable values
- Hashable keys only

---

# Collection Complexity (Must Remember)

| Operation | List | Tuple | Set | Dictionary |
|-----------|------|-------|-----|------------|
| Access | O(1) | O(1) | N/A | O(1) |
| Search | O(n) | O(n) | O(1)* | O(1)* |
| Insert End | O(1) | ❌ | O(1)* | O(1)* |
| Delete | O(n) | ❌ | O(1)* | O(1)* |

\* Average Case

---

# Pythonic Collection Patterns

Frequency Count

```python
from collections import Counter

Counter(words)
```

Remove Duplicates

```python
unique = list(set(data))
```

Dictionary Iteration

```python
for key, value in employee.items():
    print(key, value)
```

List Iteration

```python
for index, value in enumerate(items):
    print(index, value)
```

Parallel Iteration

```python
for a, b in zip(list1, list2):
    print(a, b)
```

Sorting

```python
sorted(data)

sorted(data, reverse=True)

sorted(data, key=len)
```

---

# Collection Interview Favorites

⭐⭐⭐⭐⭐

- Mutable vs Immutable
- List vs Tuple
- Set vs Dictionary
- append() vs extend()
- sort() vs sorted()
- get() vs []
- shallow vs deep copy
- Counter
- enumerate()
- zip()

---

# Production Notes

- Prefer `get()` over direct indexing when keys may be missing.
- Prefer `Counter` over manual frequency counting.
- Prefer comprehensions over unnecessary loops.
- Use tuples for immutable records.
- Use sets for membership testing and duplicate removal.
- Choose the collection based on access patterns, not familiarity.
</details>

---

# Block 03 — Functions

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐☆☆ Difficulty | Very High Interview | ⏱ 2–3h Study | 🔄 20m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Function Definition
- Function Call
- Parameters & Arguments
- Return Statement
- Default Parameters
- Keyword Arguments
- Positional-only & Keyword-only Arguments
- Variable-Length Arguments (`*args`, `**kwargs`)
- Scope (`global`, `nonlocal`)
- Lambda Functions
- Recursion
- Anonymous Functions
- Docstrings
- Type Hinting
- First-Class Functions
- Interview Pitfalls
- Production Notes

---

# Function Definition

## Basic Syntax

```python
def greet():
    print("Hello")
```

## Function with Parameters

```python
def greet(name):
    print(f"Hello {name}")
```

## Function with Return Value

```python
def add(a, b):
    return a + b
```

---

# Parameters vs Arguments

| Parameter | Argument |
|------------|----------|
| Variable defined in function | Actual value passed during function call |

```python
def add(a, b):     # Parameters
    return a + b

add(10, 20)        # Arguments
```

---

# Types of Arguments

## Positional Arguments

```python
add(10, 20)
```

---

## Keyword Arguments

```python
add(a=10, b=20)
```

---

## Mixed Arguments

```python
calculate(10, rate=18)
```

**Rule**

Positional arguments must appear before keyword arguments.

---

# Default Parameters

```python
def greet(name="Guest"):
    print(name)
```

Call

```python
greet()

greet("Swapnil")
```

---

# Positional-only Parameters (Python 3.8+)

```python
def divide(a, b, /):
    return a / b
```

Valid

```python
divide(10, 2)
```

Invalid

```python
divide(a=10, b=2)
```

---

# Keyword-only Parameters

```python
def calculate(*, tax):
    print(tax)
```

Valid

```python
calculate(tax=18)
```

Invalid

```python
calculate(18)
```

---

# Variable-Length Arguments

## *args

Collects positional arguments.

```python
def add(*args):
    return sum(args)
```

```python
add(1, 2, 3, 4)
```

Type

```python
tuple
```

---

## **kwargs

Collects keyword arguments.

```python
def employee(**kwargs):
    print(kwargs)
```

```python
employee(name="Swapnil", city="Pune")
```

Type

```python
dict
```

---

# Argument Unpacking

## List

```python
numbers = [10, 20]

add(*numbers)
```

---

## Dictionary

```python
employee = {
    "name": "Swapnil",
    "age": 30
}

display(**employee)
```

---

# Return Statement

Single Value

```python
return total
```

Multiple Values

```python
return name, salary
```

Receive

```python
name, salary = get_employee()
```

---

# Scope

## Local Scope

```python
def fun():
    x = 10
```

---

## Global Scope

```python
x = 10

def fun():
    global x
```

---

## Nonlocal Scope

```python
def outer():
    count = 0

    def inner():
        nonlocal count
        count += 1
```

---

# Lambda Function

```python
square = lambda x: x * x
```

Multiple Parameters

```python
multiply = lambda a, b: a * b
```

Sorting

```python
students.sort(key=lambda x: x["marks"])
```

---

# Recursion

```python
def factorial(n):
    if n == 0:
        return 1

    return n * factorial(n - 1)
```

---

# First-Class Functions

Functions can be

- Assigned to variables
- Passed as arguments
- Returned from another function

```python
def greet():
    print("Hello")

fun = greet

fun()
```

---

# Nested Functions

```python
def outer():

    def inner():
        print("Inner")

    inner()
```

---

# Docstrings

```python
def add(a, b):
    """
    Adds two numbers.
    """
    return a + b
```

Access

```python
help(add)

add.__doc__
```

---

# Type Hinting

```python
def add(a: int, b: int) -> int:
    return a + b
```

Optional

```python
from typing import Optional

def get_name(name: Optional[str]):
    ...
```

---

# Mutable Default Argument (Interview Favorite)

❌ Avoid

```python
def add(item, items=[]):
    items.append(item)
    return items
```

✅ Preferred

```python
def add(item, items=None):

    if items is None:
        items = []

    items.append(item)

    return items
```

---

# Pythonic Tips

Instead of

```python
if value == None:
```

Prefer

```python
if value is None:
```

---

Return early instead of nested conditions.

```python
if not user:
    return

process(user)
```

---

Prefer keyword arguments when many parameters exist.

```python
train(
    learning_rate=0.01,
    epochs=100,
    batch_size=64
)
```

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- Parameter vs Argument
- *args vs **kwargs
- Mutable default arguments
- Scope
- global vs nonlocal
- Lambda limitations
- Recursion base condition
- Returning multiple values

---

# Production Notes

- Keep functions short and focused.
- Prefer pure functions whenever possible.
- Avoid global variables.
- Add type hints.
- Write meaningful docstrings for reusable functions.
- Use keyword arguments for readability.

---

# Quick Revision

- `*args` → Tuple
- `**kwargs` → Dictionary
- `return a, b` → Tuple Packing
- `global` → Module Scope
- `nonlocal` → Enclosing Function Scope
- Functions are first-class objects.
  
</details>

---
# Block 04 — Functional Programming

> ⭐⭐⭐⭐☆ Priority | ⭐⭐⭐☆☆ Difficulty | High Interview | ⏱ 2h Study | 🔄 15m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- map()
- filter()
- reduce()
- enumerate()
- zip()
- sorted()
- any()
- all()
- List Comprehension
- Dictionary Comprehension
- Set Comprehension
- Generator Expression
- functools
- operator
- Interview Pitfalls
- Production Notes

# map()

Apply a function to every element.

```python
numbers = [1, 2, 3]

result = list(map(lambda x: x * 2, numbers))
```

Equivalent

```python
[x * 2 for x in numbers]
```

---

# filter()

Filter elements based on a condition.

```python
numbers = [1, 2, 3, 4]

result = list(filter(lambda x: x % 2 == 0, numbers))
```

Equivalent

```python
[x for x in numbers if x % 2 == 0]
```

---

# reduce()

```python
from functools import reduce

result = reduce(lambda a, b: a + b, numbers)
```

---

# enumerate()

```python
for index, value in enumerate(items):
    print(index, value)
```

Start Index

```python
enumerate(items, start=1)
```

---

# zip()

```python
for a, b in zip(names, scores):
    print(a, b)
```

Dictionary

```python
dict(zip(keys, values))
```

---

# sorted()

```python
sorted(data)

sorted(data, reverse=True)

sorted(data, key=len)
```

Objects

```python
employees = sorted(
    employees,
    key=lambda x: x.salary
)
```

---

# any()

```python
any(numbers)
```

Returns True if any element is truthy.

---

# all()

```python
all(numbers)
```

Returns True only if all elements are truthy.

---

# List Comprehension

```python
[x * x for x in range(10)]
```

Condition

```python
[x for x in data if x > 10]
```

Nested

```python
[(i, j) for i in a for j in b]
```

---

# Dictionary Comprehension

```python
{x: x * x for x in range(5)}
```

---

# Set Comprehension

```python
{x for x in data}
```

---

# Generator Expression

```python
(x * x for x in range(10))
```

Memory Efficient

---

# functools

Useful Functions

```python
reduce()

partial()

lru_cache()
```

---

# operator Module

```python
from operator import itemgetter

sorted(data, key=itemgetter("salary"))
```

---

# Pythonic Tips

Prefer comprehensions over unnecessary loops.

Prefer `enumerate()` over manual index management.

Prefer `zip()` instead of indexing multiple lists.

Prefer `sorted()` instead of modifying the original collection unless needed.

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- map vs comprehension
- sorted vs sort
- enumerate
- zip
- any vs all
- reduce
- generator expression vs list comprehension

---

# Production Notes

- Prefer comprehensions for readability.
- Use generators for large datasets.
- Avoid deeply nested comprehensions.
- Use `enumerate()` when index is required.
- Use `zip()` for parallel iteration.
- Use `functools.lru_cache` for expensive recursive computations.

---

# Quick Revision

- `map()` → Transform
- `filter()` → Select
- `reduce()` → Aggregate
- `enumerate()` → Index + Value
- `zip()` → Parallel Iteration
- `sorted()` → New List
- `sort()` → In-place
- Generator Expression → Lazy Evaluation
</details>

---

# Block 05 — Object-Oriented Programming (OOP)

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐⭐☆ Difficulty | Very High Interview | ⏱ 3–4h Study | 🔄 30m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Class & Object
- Constructor (`__init__`)
- Instance Variables
- Class Variables
- Instance Methods
- Class Methods
- Static Methods
- Encapsulation
- Inheritance
- Method Overriding
- super()
- Polymorphism
- Abstraction
- Composition vs Inheritance
- Magic (Dunder) Methods
- Property Decorators
- Dataclasses
- Method Resolution Order (MRO)
- Interview Pitfalls
- Production Notes
- Quick Revision

# Class

Blueprint for creating objects.

```python
class Employee:
    pass
```

---

# Object

Instance of a class.

```python
emp = Employee()
```

Multiple objects can be created from the same class.

---

# Constructor

Automatically called during object creation.

```python
class Employee:

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary
```

Object Creation

```python
emp = Employee("Swapnil", 100000)
```

---

# Instance Variables

Unique for every object.

```python
class Employee:

    def __init__(self, name):
        self.name = name
```

---

# Class Variables

Shared by all objects.

```python
class Employee:

    company = "OpenAI"
```

Access

```python
Employee.company

emp.company
```

---

# Instance Method

Works on object data.

```python
class Employee:

    def display(self):
        print(self.name)
```

---

# Class Method

Works on class data.

```python
class Employee:

    company = "ABC"

    @classmethod
    def get_company(cls):
        return cls.company
```

---

# Static Method

Utility function.

Does not access instance or class state.

```python
class Math:

    @staticmethod
    def add(a, b):
        return a + b
```

---

# Difference

| Method | First Parameter | Access |
|---------|----------------|--------|
| Instance | self | Object |
| Class | cls | Class |
| Static | None | Neither |

---

# self vs cls

```python
self
```

Current Object

```python
cls
```

Current Class

---

# Encapsulation

Hide implementation details.

```python
class Bank:

    def __init__(self):
        self.__balance = 0
```

Private Variable

```python
__balance
```

Getter

```python
def get_balance(self):
    return self.__balance
```

Setter

```python
def deposit(self, amount):
    self.__balance += amount
```

---

# Name Mangling

```python
obj._ClassName__balance
```

Avoid using directly.

---

# Inheritance

Reuse existing code.

```python
class Animal:

    def sound(self):
        print("Sound")

class Dog(Animal):

    pass
```

---

# Types of Inheritance

Single

```python
A -> B
```

Multiple

```python
A
 \
  C
 /
B
```

Multilevel

```python
A -> B -> C
```

Hierarchical

```python
      A
     / \
    B   C
```

Hybrid

Combination of above.

---

# Method Overriding

```python
class Animal:

    def sound(self):
        print("Animal")

class Dog(Animal):

    def sound(self):
        print("Dog")
```

---

# super()

Call parent implementation.

```python
class Dog(Animal):

    def __init__(self):

        super().__init__()
```

---

# Polymorphism

Same interface.

Different implementations.

```python
class Dog:

    def sound(self):
        print("Bark")

class Cat:

    def sound(self):
        print("Meow")
```

```python
for animal in animals:
    animal.sound()
```

Duck Typing.

---

# Abstraction

Hide implementation.

Expose behavior.

```python
from abc import ABC

from abc import abstractmethod
```

```python
class Shape(ABC):

    @abstractmethod
    def area(self):
        pass
```

Implementation

```python
class Circle(Shape):

    def area(self):
        ...
```

---

# Composition

Object contains another object.

```python
class Engine:
    ...

class Car:

    def __init__(self):
        self.engine = Engine()
```

---

# Composition vs Inheritance

| Composition | Inheritance |
|-------------|-------------|
| HAS-A | IS-A |
| Flexible | Tightly Coupled |
| Preferred | Use Carefully |

Interview Favorite.

---

# Magic (Dunder) Methods

Constructor

```python
__init__()
```

String Representation

```python
__str__()
```

Developer Representation

```python
__repr__()
```

Length

```python
__len__()
```

Comparison

```python
__eq__()
```

Addition

```python
__add__()
```

Callable Object

```python
__call__()
```

Context Manager

```python
__enter__()

__exit__()
```

---

# Property Decorator

Getter

```python
@property
def salary(self):
    return self.__salary
```

Setter

```python
@salary.setter
def salary(self, value):
    self.__salary = value
```

---

# Dataclass

Python 3.7+

```python
from dataclasses import dataclass

@dataclass
class Employee:

    id: int

    name: str
```

Automatically creates

- __init__()
- __repr__()
- __eq__()

---

# Method Resolution Order (MRO)

Check resolution order.

```python
ClassName.mro()
```

or

```python
ClassName.__mro__
```

Interview Favorite.

---

# isinstance()

```python
isinstance(emp, Employee)
```

---

# issubclass()

```python
issubclass(Dog, Animal)
```

---

# hasattr()

```python
hasattr(emp, "salary")
```

---

# getattr()

```python
getattr(emp, "salary")
```

Default

```python
getattr(emp, "salary", 0)
```

---

# setattr()

```python
setattr(emp, "salary", 100)
```

---

# delattr()

```python
delattr(emp, "salary")
```

---

# Pythonic Tips

Prefer

Composition

over

Inheritance.

---

Use

```python
@dataclass
```

for DTOs and configuration models.

---

Prefer

```python
@property
```

instead of explicit getters/setters.

---

Keep classes focused on one responsibility.

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- self vs cls
- Class Variable vs Instance Variable
- @classmethod vs @staticmethod
- Inheritance vs Composition
- __str__ vs __repr__
- Property Decorators
- MRO
- super()
- Duck Typing
- Abstract Class vs Interface

---

# Production Notes

Use OOP when:

- Managing complex domain models
- Building reusable libraries
- Creating APIs
- Designing scalable systems

Avoid unnecessary classes for simple scripts.

Prefer composition over inheritance to reduce coupling.

Use dataclasses for immutable data containers and configuration objects.

Keep classes small and follow the Single Responsibility Principle (SRP).

Document public APIs and expose only what consumers need.

---

# Where I've Used This

FastAPI

- Pydantic models
- Dependency Injection
- Service Classes

GenAI

- Prompt Builders
- Model Wrappers
- LLM Clients

Production Systems

- Configuration Objects
- Database Managers
- API Clients
- Azure Service Wrappers

---

# Quick Revision

✅ Class → Blueprint

✅ Object → Instance

✅ self → Current Object

✅ cls → Current Class

✅ @classmethod → Class State

✅ @staticmethod → Utility Function

✅ Encapsulation → Hide Data

✅ Inheritance → IS-A

✅ Composition → HAS-A

✅ Polymorphism → Same Interface, Different Implementation

✅ Abstraction → Hide Implementation

✅ @property → Pythonic Getter/Setter

✅ @dataclass → Auto-generated Boilerplate

✅ MRO → Method Resolution Order

✅ Prefer Composition > Inheritance

</details>

---
# Block 06 — Exception Handling

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐☆☆ Difficulty | Very High Interview | ⏱ 2–3h Study | 🔄 20m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Why Exception Handling?
- Built-in Exceptions
- try / except
- else
- finally
- Raising Exceptions
- Custom Exceptions
- Exception Chaining
- Assertions
- Logging Exceptions
- Context Managers
- Best Practices
- Interview Pitfalls
- Production Notes
- Frequently Asked Follow-up Questions
- Quick Revision


# Why Exception Handling?

Exception handling prevents abrupt program termination by gracefully handling runtime errors.

A well-designed exception strategy improves:

- Reliability
- Debuggability
- User Experience
- Maintainability

**Senior Interview Perspective**

Interviewers expect you to:

- Handle expected failures.
- Avoid hiding bugs.
- Log useful information.
- Raise meaningful exceptions.

---

# Built-in Exceptions

Commonly Used

```python
Exception

ValueError

TypeError

KeyError

IndexError

AttributeError

NameError

ImportError

FileNotFoundError

ZeroDivisionError

RuntimeError

PermissionError

TimeoutError

StopIteration
```

---

# Basic try-except

```python
try:
    result = 10 / 0

except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

# Multiple Exceptions

```python
try:
    value = int(user_input)

except ValueError:
    print("Invalid number")

except TypeError:
    print("Invalid type")
```

---

# Handling Multiple Exceptions Together

```python
try:
    ...

except (TypeError, ValueError):
    print("Invalid Input")
```

---

# Generic Exception

```python
try:
    ...

except Exception as e:
    print(e)
```

Use only when required.

Avoid swallowing unexpected exceptions.

---

# else Block

Runs only if no exception occurs.

```python
try:
    number = int(input())

except ValueError:
    print("Invalid")

else:
    print("Success")
```

---

# finally Block

Always executes.

Useful for cleanup.

```python
try:
    file = open("data.txt")

finally:
    file.close()
```

---

# Complete Structure

```python
try:
    ...

except ValueError:
    ...

except Exception:
    ...

else:
    ...

finally:
    ...
```

---

# Raising Exceptions

```python
raise ValueError("Invalid Salary")
```

---

# Re-raising Exception

```python
try:
    ...

except Exception:
    raise
```

Preserves original traceback.

---

# Custom Exceptions

```python
class ValidationError(Exception):
    pass
```

Raise

```python
raise ValidationError("Invalid Email")
```

---

# Custom Exception with Constructor

```python
class EmployeeNotFound(Exception):

    def __init__(self, employee_id):
        super().__init__(
            f"Employee {employee_id} not found."
        )
```

---

# Exception Chaining

```python
try:
    ...

except ValueError as e:

    raise RuntimeError(
        "Processing Failed"
    ) from e
```

Preserves root cause.

Interview Favorite.

---

# Assertions

```python
assert age >= 18
```

With Message

```python
assert salary > 0, "Salary must be positive."
```

Do not use assertions for user input validation.

---

# Common Exception Patterns

Dictionary

```python
try:
    value = employee["salary"]

except KeyError:
    value = 0
```

---

File

```python
try:

    with open("file.txt") as file:

        data = file.read()

except FileNotFoundError:

    print("Missing File")
```

---

API

```python
try:

    response = requests.get(url)

    response.raise_for_status()

except requests.RequestException:

    ...
```

---

Database

```python
try:

    conn.commit()

except Exception:

    conn.rollback()
```

---

# Logging Exceptions

```python
import logging

logging.exception("Unexpected Error")
```

Equivalent

```python
logger.exception("Unexpected Error")
```

Automatically logs traceback.

---

# Context Manager

Preferred

```python
with open("data.txt") as file:

    data = file.read()
```

Avoid

```python
file = open("data.txt")

try:
    ...

finally:
    file.close()
```

---

# Creating Context Managers

```python
from contextlib import contextmanager

@contextmanager
def database():

    print("Connect")

    yield

    print("Close")
```

Usage

```python
with database():
    ...
```

---

# Exception Hierarchy

```
BaseException
│
├── Exception
│    ├── ValueError
│    ├── TypeError
│    ├── KeyError
│    ├── IndexError
│    ├── RuntimeError
│    └── ...
│
├── KeyboardInterrupt
└── SystemExit
```

Never catch

```python
BaseException
```

unless absolutely necessary.

---

# Best Practices

Catch specific exceptions.

```python
except ValueError:
```

instead of

```python
except Exception:
```

---

Log exceptions.

Don't ignore them.

---

Raise meaningful exceptions.

```python
raise ValueError(
    "Salary cannot be negative."
)
```

instead of

```python
raise Exception()
```

---

Keep try blocks small.

Avoid wrapping hundreds of lines.

---

Do not silently suppress exceptions.

Avoid

```python
except:
    pass
```

---

# Pythonic Tips

Prefer

```python
with
```

over

```python
try-finally
```

for resources.

---

Raise early.

Fail fast.

---

Never expose raw exception messages to end users.

---

Use custom exceptions for business rules.

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- except Exception vs specific exception
- raise vs return
- finally execution
- exception chaining
- custom exception
- logging.exception()
- assert misuse
- swallowing exceptions
- cleanup logic

---

# Production Notes

Use custom exceptions for domain logic.

Examples

- AuthenticationError
- ValidationError
- BusinessRuleViolation
- ModelNotFound

---

Separate

Business Exceptions

from

System Exceptions.

---

Always log unexpected exceptions.

---

Never lose original traceback.

Use

```python
raise ... from e
```

---

Rollback transactions when operations fail.

---

Wrap external services with proper exception handling.

Examples

- Database
- REST API
- Azure Services
- OpenAI API
- File System

---

Avoid exposing stack traces to API consumers.

Return meaningful error responses.

---

# Where I've Used This

FastAPI

- HTTPException
- Request Validation
- Global Exception Handler

GenAI

- API Failures
- Timeout Handling
- Token Validation
- Model Response Validation

Azure

- Service Bus Retry
- Blob Storage Errors
- Authentication Failures

MongoDB

- Connection Failures
- Duplicate Key Errors

Production Pipelines

- Retry Logic
- Failure Logging
- Transaction Rollback

---

# Frequently Asked Follow-up Questions

### Why shouldn't we catch `Exception` everywhere?

It hides programming errors, makes debugging difficult, and may unintentionally suppress critical failures.

---

### Why create custom exceptions?

They make code more readable, communicate business intent, and allow precise error handling.

---

### Why use `raise ... from e`?

To preserve the original traceback while adding higher-level context.

---

### Difference between `raise` and `return`?

`raise` stops execution by throwing an exception.

`return` exits normally with a value.

---

### Difference between `finally` and `with`?

`finally`

- General cleanup mechanism.
- Works everywhere.

`with`

- Resource management.
- Cleaner and Pythonic.
- Automatically handles cleanup.

---

### When should assertions be used?

Assertions verify internal assumptions during development.

They should not be used for validating user input or business rules.

---

### Should we log every exception?

No.

Expected exceptions should usually be handled.

Unexpected exceptions should be logged with sufficient context.

---

### When should we re-raise an exception?

When you need to:

- Log it.
- Add context.
- Perform cleanup.

without losing the original traceback.

---

# Quick Revision

✅ try → Protected Code

✅ except → Handle Error

✅ else → Runs on Success

✅ finally → Always Executes

✅ raise → Throw Exception

✅ raise ... from e → Preserve Traceback

✅ Custom Exception → Business Logic

✅ assert → Development Checks

✅ logging.exception() → Logs Traceback

✅ with → Automatic Resource Management

✅ Catch Specific Exceptions

✅ Log Unexpected Exceptions

✅ Prefer Custom Exceptions over Generic Exceptions

✅ Never use `except: pass`

✅ Keep try blocks small

</details>

---
# Block 07 — File Handling

> ⭐⭐⭐⭐☆ Priority | ⭐⭐☆☆☆ Difficulty | High Interview | ⏱ 2h Study | 🔄 15m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Opening Files
- File Modes
- Reading Files
- Writing Files
- Appending Files
- Context Manager (`with`)
- File Pointer
- Binary Files
- CSV Files
- JSON Files
- pathlib
- Temporary Files
- Common File Operations
- Interview Pitfalls
- Production Notes
- Frequently Asked Follow-up Questions
- Quick Revision

# Opening a File

```python
file = open("data.txt")
```

Recommended

```python
with open("data.txt") as file:
    ...
```

---

# File Modes

| Mode | Description |
|------|-------------|
| `r` | Read (Default) |
| `w` | Write (Overwrite/Create) |
| `a` | Append |
| `x` | Create New File |
| `r+` | Read + Write |
| `w+` | Read + Write (Overwrite) |
| `a+` | Read + Append |
| `rb` | Binary Read |
| `wb` | Binary Write |
| `ab` | Binary Append |

---

# Reading File

Read Entire File

```python
with open("sample.txt") as file:
    data = file.read()
```

Read One Line

```python
line = file.readline()
```

Read All Lines

```python
lines = file.readlines()
```

Iterate Line by Line (Recommended)

```python
with open("sample.txt") as file:

    for line in file:
        print(line.strip())
```

---

# Writing File

Overwrite

```python
with open("sample.txt", "w") as file:

    file.write("Hello")
```

---

# Writing Multiple Lines

```python
lines = [
    "Python\n",
    "SQL\n"
]

with open("sample.txt", "w") as file:

    file.writelines(lines)
```

---

# Append

```python
with open("sample.txt", "a") as file:

    file.write("New Line\n")
```

---

# File Pointer

Current Position

```python
file.tell()
```

Move Pointer

```python
file.seek(0)
```

Example

```python
with open("sample.txt") as file:

    print(file.tell())

    file.read(5)

    print(file.tell())

    file.seek(0)
```

---

# Closing File

Manual

```python
file.close()
```

Preferred

```python
with open(...)
```

---

# Binary Files

Read

```python
with open("image.png", "rb") as file:

    data = file.read()
```

Write

```python
with open("copy.png", "wb") as file:

    file.write(data)
```

---

# CSV Files

Read

```python
import csv

with open("employee.csv") as file:

    reader = csv.reader(file)

    for row in reader:
        print(row)
```

Dictionary Reader

```python
reader = csv.DictReader(file)
```

Write

```python
writer = csv.writer(file)

writer.writerow(["Name", "Salary"])
```

---

# JSON Files

Read

```python
import json

with open("employee.json") as file:

    data = json.load(file)
```

Write

```python
with open("employee.json", "w") as file:

    json.dump(data, file, indent=4)
```

String

```python
json.loads()

json.dumps()
```

---

# pathlib (Recommended)

```python
from pathlib import Path

path = Path("sample.txt")
```

Exists

```python
path.exists()
```

Create Folder

```python
path.mkdir()
```

Create Multiple Folders

```python
path.mkdir(parents=True)
```

Extension

```python
path.suffix
```

Filename

```python
path.name
```

Absolute Path

```python
path.resolve()
```

---

# Temporary Files

```python
import tempfile

with tempfile.NamedTemporaryFile() as file:

    print(file.name)
```

---

# Useful File Operations

Copy

```python
import shutil

shutil.copy(src, dst)
```

Move

```python
shutil.move(src, dst)
```

Delete

```python
import os

os.remove(path)
```

Rename

```python
os.rename(old, new)
```

---

# Pythonic Tips

Prefer

```python
Path()
```

instead of

```python
os.path
```

---

Always use

```python
with
```

---

Read large files line by line.

---

Use UTF-8 encoding.

```python
open(file, encoding="utf-8")
```

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- Forgetting to close files
- read() vs readline() vs readlines()
- File Modes
- tell()
- seek()
- JSON load vs loads
- JSON dump vs dumps
- CSV Reader vs DictReader
- pathlib

---

# Production Notes

- Always use Context Managers.
- Handle FileNotFoundError.
- Avoid loading huge files into memory.
- Use pathlib for portability.
- Validate file existence before processing.
- Log file processing failures.

---

# Where I've Used This

Data Science

- CSV Dataset Loading
- Model Serialization
- Feature Export

GenAI

- Prompt Templates
- Configuration Files
- JSON Responses

FastAPI

- File Upload
- File Download

Azure

- Blob Upload
- Blob Download

ETL

- CSV Processing
- JSON Transformation

---

# Frequently Asked Follow-up Questions

### Why use `with` instead of `open()`?

Automatic cleanup.

Less error-prone.

---

### Why prefer pathlib?

Readable

Object-Oriented

Cross-platform

---

### Difference between `json.load()` and `json.loads()`?

load()

Reads from file.

loads()

Reads from string.

---

### Difference between `json.dump()` and `json.dumps()`?

dump()

Writes to file.

dumps()

Returns JSON string.

---

### Why avoid `read()` on large files?

Consumes large memory.

Prefer iteration.

---

# Quick Revision

✅ with

✅ open()

✅ read()

✅ readline()

✅ readlines()

✅ write()

✅ writelines()

✅ tell()

✅ seek()

✅ pathlib

✅ csv

✅ json

✅ Binary Mode
</details>

---
# Block 08 — Iterators & Generators

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐⭐☆ Difficulty | Very High Interview | ⏱ 3h Study | 🔄 30m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Iterable
- Iterator
- iter()
- next()
- Custom Iterator
- Generator
- yield
- Generator Expression
- Generator vs Function
- Generator vs List
- itertools
- Infinite Iterators
- Lazy Evaluation
- Interview Pitfalls
- Production Notes
- Frequently Asked Follow-up Questions
- Quick Revision

# Iterable

Object capable of returning an iterator.

Examples

```python
list

tuple

set

dict

str
```

Check

```python
from collections.abc import Iterable

isinstance(obj, Iterable)
```

---

# Iterator

Object that returns one item at a time.

Methods

```python
__iter__()

__next__()
```

---

# iter()

```python
numbers = [1,2,3]

iterator = iter(numbers)
```

---

# next()

```python
next(iterator)
```

Default

```python
next(iterator, None)
```

---

# Iterator Example

```python
numbers = [10,20,30]

it = iter(numbers)

print(next(it))
print(next(it))
```

---

# StopIteration

Raised automatically.

```python
try:

    next(it)

except StopIteration:

    ...
```

---

# Custom Iterator

```python
class Counter:

    def __init__(self):

        self.value = 0

    def __iter__(self):

        return self

    def __next__(self):

        if self.value >= 5:

            raise StopIteration

        self.value += 1

        return self.value
```

---

# Generator

Uses

```python
yield
```

instead of

```python
return
```

---

# Generator Example

```python
def numbers():

    yield 1
    yield 2
    yield 3
```

---

Consume

```python
for n in numbers():

    print(n)
```

---

# Generator vs Return

Return

```python
return
```

Ends execution.

Yield

```python
yield
```

Pauses execution.

---

# Generator Expression

```python
(x*x for x in range(10))
```

Equivalent

```python
def square():

    for x in range(10):

        yield x*x
```

---

# Generator vs List

Generator

```python
(x*x for x in data)
```

List

```python
[x*x for x in data]
```

---

# Why Generators?

Memory Efficient

Lazy Evaluation

Useful for

- Large Files
- Streaming Data
- APIs
- ETL
- ML Pipelines

---

# itertools

Import

```python
import itertools
```

Count

```python
itertools.count()
```

Cycle

```python
itertools.cycle()
```

Repeat

```python
itertools.repeat()
```

Chain

```python
itertools.chain()
```

Accumulate

```python
itertools.accumulate()
```

Combinations

```python
itertools.combinations()
```

Permutations

```python
itertools.permutations()
```

Product

```python
itertools.product()
```

Groupby

```python
itertools.groupby()
```

---

# Lazy Evaluation

Nothing executes until requested.

```python
gen = (x*x for x in range(100))
```

Execution starts during iteration.

---

# Pythonic Tips

Prefer generators for

- Large datasets
- Infinite streams
- Pipelines

---

Use

```python
yield from
```

to delegate generators.

```python
def generator():

    yield from range(5)
```

---

Prefer generator expressions when data is consumed once.

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- Iterable vs Iterator
- iter()
- next()
- yield
- Generator Expression
- StopIteration
- Lazy Evaluation
- Generator vs List
- yield vs return

---

# Production Notes

Use generators for

- Reading GB-sized files
- Streaming APIs
- Kafka Consumers
- ETL Pipelines
- Batch Processing
- ML Data Loaders

Avoid converting generators into lists unless necessary.

Chain generators to build efficient pipelines.

---

# Where I've Used This

Data Science

- Dataset Loading
- Feature Engineering

GenAI

- Streaming LLM Responses
- Prompt Pipelines

FastAPI

- StreamingResponse

Azure

- Blob Processing

Production

- Log Processing
- CSV Readers
- Batch Jobs

---

# Frequently Asked Follow-up Questions

### Difference between Iterable and Iterator?

Iterable

Can create an iterator.

Iterator

Produces next element.

---

### Difference between Generator and Iterator?

Generator is a special iterator automatically created using `yield`.

---

### Why use generators?

Memory efficiency.

Lazy evaluation.

Streaming.

---

### Difference between `yield` and `return`?

return

Terminates function.

yield

Pauses and resumes execution.

---

### When should generators not be used?

When

- Random access is required.
- Multiple passes are needed.
- Dataset is small.

---

### What is lazy evaluation?

Compute values only when requested.

---

### Why are generators useful in Data Science?

Datasets may not fit into memory.

Generators process records incrementally.

---

# Quick Revision

✅ Iterable

✅ Iterator

✅ iter()

✅ next()

✅ StopIteration

✅ yield

✅ Generator

✅ Generator Expression

✅ itertools

✅ Lazy Evaluation

✅ yield from

✅ Generator > List for large datasets
</details>

---
# Block 09 — Decorators

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐⭐☆ Difficulty | Very High Interview | ⏱ 3h Study | 🔄 30m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- What is a Decorator?
- First-Class Functions
- Higher-Order Functions
- Basic Decorator
- Nested Functions
- Wrapper Function
- functools.wraps
- Decorators with Arguments
- Parameterized Decorators
- Multiple Decorators
- Class Decorators
- Built-in Decorators
- Property Decorators
- Timing & Logging Decorators
- Authentication Decorators
- Interview Pitfalls
- Production Notes
- Frequently Asked Follow-up Questions
- Quick Revision

# What is a Decorator?

A decorator extends or modifies the behavior of a function **without changing its original implementation**.

```python
@decorator
def greet():
    pass
```

Equivalent

```python
greet = decorator(greet)
```

---

# First-Class Functions

Functions can be:

- Assigned to variables
- Passed as arguments
- Returned from another function

```python
def greet():
    print("Hello")

func = greet

func()
```

---

# Higher-Order Functions

Accept functions as arguments or return functions.

```python
def execute(func):
    func()
```

---

# Nested Functions

```python
def outer():

    def inner():
        print("Inside")

    inner()
```

---

# Basic Decorator

```python
def logger(func):

    def wrapper():

        print("Before")

        func()

        print("After")

    return wrapper
```

Usage

```python
@logger
def greet():
    print("Hello")
```

---

# Decorator with Parameters

```python
def logger(func):

    def wrapper(*args, **kwargs):

        print("Calling Function")

        return func(*args, **kwargs)

    return wrapper
```

---

# Returning Values

```python
def logger(func):

    def wrapper(*args, **kwargs):

        result = func(*args, **kwargs)

        return result

    return wrapper
```

---

# functools.wraps

Preserve metadata.

```python
from functools import wraps
```

```python
def logger(func):

    @wraps(func)

    def wrapper(*args, **kwargs):

        return func(*args, **kwargs)

    return wrapper
```

Without wraps

```python
func.__name__
```

becomes

```
wrapper
```

---

# Parameterized Decorator

```python
def repeat(times):

    def decorator(func):

        def wrapper(*args, **kwargs):

            for _ in range(times):
                func(*args, **kwargs)

        return wrapper

    return decorator
```

Usage

```python
@repeat(3)
def hello():
    print("Hello")
```

---

# Multiple Decorators

```python
@timer

@logger

def process():
    pass
```

Execution

```
timer
↓

logger
↓

process
```

---

# Built-in Decorators

Class Method

```python
@classmethod
```

Static Method

```python
@staticmethod
```

Property

```python
@property
```

Setter

```python
@salary.setter
```

Abstract Method

```python
@abstractmethod
```

Dataclass

```python
@dataclass
```

---

# Class Decorator

```python
def add_method(cls):

    cls.version = "1.0"

    return cls
```

Usage

```python
@add_method
class Employee:
    pass
```

---

# Timing Decorator

```python
import time

from functools import wraps

def timer(func):

    @wraps(func)

    def wrapper(*args, **kwargs):

        start = time.perf_counter()

        result = func(*args, **kwargs)

        end = time.perf_counter()

        print(end - start)

        return result

    return wrapper
```

---

# Logging Decorator

```python
import logging

def log(func):

    def wrapper(*args, **kwargs):

        logging.info(func.__name__)

        return func(*args, **kwargs)

    return wrapper
```

---

# Authentication Decorator

```python
def authenticated(func):

    def wrapper(user):

        if not user:

            raise PermissionError()

        return func(user)

    return wrapper
```

---

# Retry Decorator

```python
def retry(func):

    def wrapper(*args, **kwargs):

        for _ in range(3):

            try:
                return func(*args, **kwargs)

            except Exception:
                pass

        raise Exception("Failed")

    return wrapper
```

---

# Caching Decorator

```python
from functools import lru_cache

@lru_cache
def fibonacci(n):
    ...
```

---

# Pythonic Tips

Decorators should have **one responsibility**.

---

Always use

```python
@wraps
```

---

Keep wrapper functions lightweight.

---

Prefer decorators for

- Logging
- Authentication
- Validation
- Retry
- Timing
- Metrics

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- Decorator vs Higher-Order Function
- @wraps
- Nested Functions
- Closures
- Decorator Order
- Decorator with Parameters
- Returning Values
- Built-in Decorators

---

# Production Notes

Common Production Decorators

- Authentication
- Authorization
- Logging
- Rate Limiting
- Retry
- Caching
- Validation
- Performance Monitoring

FastAPI heavily relies on decorators.

Examples

```python
@app.get()

@app.post()

@app.put()
```

Pytest

```python
@pytest.fixture
```

Dataclass

```python
@dataclass
```

---

# Where I've Used This

FastAPI

- Route Registration
- Dependency Injection

GenAI

- Retry Logic
- Logging
- Token Tracking

Production APIs

- Authentication
- Timing
- Metrics

Pytest

- Fixtures

---

# Frequently Asked Follow-up Questions

### Why use decorators?

To add reusable behavior without modifying the original function.

---

### Difference between decorator and inheritance?

Decorator extends function behavior.

Inheritance extends class behavior.

---

### Why use @wraps?

Preserves metadata.

---

### What is a closure?

A nested function that remembers variables from the enclosing scope.

---

### Can decorators accept arguments?

Yes.

Parameterized decorators.

---

### Why are decorators popular in FastAPI?

Routes, dependency injection, validation, middleware, caching.

---

# Quick Revision

✅ Decorator

✅ Higher-Order Function

✅ Nested Function

✅ Closure

✅ Wrapper

✅ @wraps

✅ Parameterized Decorator

✅ Built-in Decorators

✅ Authentication

✅ Retry

✅ Logging
</details>

---
# Block 10 — Memory Management

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐⭐☆ Difficulty | Very High Interview | ⏱ 3h Study | 🔄 30m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Python Memory Model
- Stack vs Heap
- Object References
- Reference Counting
- Garbage Collection
- Circular References
- del Statement
- Copy vs Deep Copy
- Memory Optimization
- Slots
- Weak References
- Object Interning
- GC Module
- Memory Profiling
- Interview Pitfalls
- Production Notes
- Frequently Asked Follow-up Questions
- Quick Revision

# Python Memory Model

Variables do **not store values**.

Variables store **references** to objects.

```python
a = 10

b = a
```

```
a ─┐
   ▼
 10
   ▲
b ─┘
```

---

# Stack vs Heap

Stack

- Function Calls
- Local References

Heap

- Objects
- Lists
- Dictionaries
- Instances

---

# Object Identity

```python
id(obj)
```

Type

```python
type(obj)
```

Reference Count

```python
import sys

sys.getrefcount(obj)
```

---

# Reference Counting

Primary memory management mechanism.

```python
a = []

b = a
```

Reference Count

```
2
```

When count becomes

```
0
```

Object becomes eligible for cleanup.

---

# Garbage Collection

Import

```python
import gc
```

Collect

```python
gc.collect()
```

Enable

```python
gc.enable()
```

Disable

```python
gc.disable()
```

---

# Circular References

```python
class A:
    pass

class B:
    pass

a = A()

b = B()

a.b = b

b.a = a
```

Reference counting cannot remove this.

Garbage Collector handles it.

---

# del Statement

```python
del obj
```

Deletes reference.

Not necessarily object.

---

# Copy

Reference Copy

```python
b = a
```

Shallow Copy

```python
import copy

copy.copy(obj)
```

Deep Copy

```python
copy.deepcopy(obj)
```

---

# Shallow vs Deep Copy

Shallow

Copies outer object.

Nested objects shared.

Deep

Copies everything recursively.

---

# __slots__

Reduce memory usage.

```python
class Employee:

    __slots__ = ("id", "name")
```

Benefits

- Lower Memory
- Faster Attribute Access

Limitations

- No dynamic attributes

---

# Weak References

```python
import weakref

ref = weakref.ref(obj)
```

Useful for

- Cache
- Observer Pattern

---

# Object Interning

Integers

```python
a = 10

b = 10

a is b
```

Usually

```
True
```

Strings

```python
a = "Python"

b = "Python"
```

Often interned.

Never rely on this behavior.

---

# Memory Profiling

Object Size

```python
import sys

sys.getsizeof(obj)
```

Memory Profiler

```python
memory_profiler
```

Tracemalloc

```python
import tracemalloc
```

Start

```python
tracemalloc.start()
```

Snapshot

```python
tracemalloc.take_snapshot()
```

---

# Pythonic Tips

Prefer generators over large lists.

---

Reuse objects when appropriate.

---

Delete unnecessary references.

---

Avoid unnecessary deep copies.

---

Prefer immutable objects where possible.

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- Reference vs Object
- del
- Garbage Collection
- Reference Counting
- Circular References
- id()
- copy vs deepcopy
- __slots__
- Weak References

---

# Production Notes

Large ML datasets

↓

Use generators.

---

Large DataFrames

↓

Avoid unnecessary copies.

---

Caches

↓

Use weak references where appropriate.

---

Monitor memory in long-running services.

---

Profile before optimizing.

---

Use tracemalloc for memory leak investigation.

---

# Where I've Used This

Data Science

- Large Dataset Processing
- Generator Pipelines

GenAI

- Streaming Responses
- Prompt Processing

FastAPI

- Long-running APIs

Azure

- Background Workers

Production

- Memory Leak Investigation
- Performance Optimization

---

# Frequently Asked Follow-up Questions

### Does del delete an object?

No.

It deletes a reference.

---

### What removes circular references?

Garbage Collector.

---

### Why use generators?

Lower memory usage.

---

### Difference between copy and deepcopy?

Shallow copies references.

Deep recursively copies objects.

---

### Why use __slots__?

Reduce memory.

Improve performance.

---

### Why avoid deepcopy?

Expensive.

Higher memory consumption.

---

### Does Python have manual memory management?

No.

Reference Counting + Garbage Collection.

---

### How do you investigate memory leaks?

- tracemalloc
- gc
- memory_profiler
- objgraph

---

# Quick Revision

✅ Reference

✅ Heap

✅ Stack

✅ id()

✅ getrefcount()

✅ Garbage Collection

✅ gc.collect()

✅ del

✅ copy

✅ deepcopy

✅ __slots__

✅ weakref

✅ tracemalloc

✅ Reference Counting

✅ Circular References
</details>

---
# Block 11 — Modern Python

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐⭐☆ Difficulty | Very High Interview | ⏱ 3–4h Study | 🔄 30m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Type Hinting
- Advanced Typing
- Union & Optional
- Generic Types
- Dataclasses
- Enums
- NamedTuple
- TypedDict
- Protocol
- ABC vs Protocol
- Pattern Matching
- Walrus Operator
- Contextlib
- pathlib
- tomllib
- Modern String Formatting
- Common Standard Libraries
- Pythonic Coding Practices
- Interview Pitfalls
- Production Notes
- Frequently Asked Follow-up Questions
- Quick Revision

# Type Hinting

Python supports optional static type annotations.

```python
name: str = "Swapnil"

age: int = 30

salary: float = 100000.0
```

---

## Function Type Hint

```python
def add(a: int, b: int) -> int:
    return a + b
```

---

## Variable Type Hint

```python
numbers: list[int]

employee: dict[str, str]

scores: tuple[int, int]

skills: set[str]
```

---

## Any

```python
from typing import Any

value: Any
```

Avoid unless absolutely necessary.

---

# Optional

```python
from typing import Optional

name: Optional[str]
```

Equivalent

```python
str | None
```

(Python 3.10+)

---

# Union

Old Syntax

```python
from typing import Union

value: Union[int, float]
```

Modern Python

```python
value: int | float
```

Preferred.

---

# Literal

```python
from typing import Literal

status: Literal[
    "Pending",
    "Running",
    "Completed"
]
```

Useful for APIs.

---

# Final

```python
from typing import Final

PI: Final = 3.14
```

---

# Generic Collections

```python
list[int]

tuple[str, int]

dict[str, float]

set[int]
```

---

# Generic Type Variable

```python
from typing import TypeVar

T = TypeVar("T")
```

Example

```python
def first(items: list[T]) -> T:
    return items[0]
```

---

# Callable

```python
from typing import Callable

func: Callable[[int], int]
```

---

# Type Alias

```python
UserId = int
```

Modern

```python
type UserId = int
```

(Python 3.12+)

---

# TypedDict

```python
from typing import TypedDict

class Employee(TypedDict):

    id: int

    name: str
```

---

# NamedTuple

```python
from typing import NamedTuple

class Employee(NamedTuple):

    id: int

    name: str
```

Immutable.

---

# Enum

```python
from enum import Enum

class Status(Enum):

    PENDING = "Pending"

    SUCCESS = "Success"
```

Access

```python
Status.SUCCESS
```

---

# Dataclass

```python
from dataclasses import dataclass

@dataclass
class Employee:

    id: int

    name: str

    salary: float
```

Automatically creates

- __init__()
- __repr__()
- __eq__()

---

# Frozen Dataclass

Immutable

```python
@dataclass(frozen=True)

class Config:

    host: str
```

---

# Field

```python
from dataclasses import field

roles: list[str] = field(default_factory=list)
```

---

# Protocol

Structural Typing.

```python
from typing import Protocol

class Animal(Protocol):

    def sound(self) -> str:
        ...
```

---

# ABC vs Protocol

| ABC | Protocol |
|------|----------|
| Explicit Inheritance | Duck Typing |
| Runtime | Static Type Checking |
| Strong Contract | Flexible |

---

# Pattern Matching (Python 3.10+)

```python
match status:

    case "Pending":
        ...

    case "Running":
        ...

    case _:
        ...
```

---

# Walrus Operator

```python
if (n := len(data)) > 10:
    print(n)
```

---

# Contextlib

Suppress

```python
from contextlib import suppress

with suppress(FileNotFoundError):

    ...
```

Closing

```python
from contextlib import closing
```

---

# pathlib

```python
from pathlib import Path

path = Path("config.json")
```

Exists

```python
path.exists()
```

Read

```python
path.read_text()
```

Write

```python
path.write_text("Hello")
```

---

# tomllib (Python 3.11+)

Read TOML

```python
import tomllib

with open("pyproject.toml", "rb") as file:

    data = tomllib.load(file)
```

---

# Modern String Formatting

f-string

```python
name = "Swapnil"

print(f"Hello {name}")
```

Formatting

```python
price = 100.456

print(f"{price:.2f}")
```

---

# Common Standard Libraries

Collections

```python
collections
```

Itertools

```python
itertools
```

Functools

```python
functools
```

Datetime

```python
datetime
```

UUID

```python
uuid
```

Pathlib

```python
pathlib
```

JSON

```python
json
```

Logging

```python
logging
```

Typing

```python
typing
```

Dataclasses

```python
dataclasses
```

Enum

```python
enum
```

Contextlib

```python
contextlib
```

Tomllib

```python
tomllib
```

---

# Pythonic Practices

Prefer

```python
list[int]
```

Instead of

```python
List[int]
```

(Python 3.9+)

---

Prefer

```python
int | None
```

Instead of

```python
Optional[int]
```

(Python 3.10+)

---

Prefer dataclass over manual DTO classes.

---

Prefer pathlib over os.path.

---

Prefer Enum over hardcoded strings.

---

Prefer Pattern Matching over long if-elif chains when appropriate.

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- Optional vs Union
- TypedDict
- NamedTuple
- Dataclass
- Protocol
- Pattern Matching
- Walrus Operator
- Enum
- pathlib
- tomllib

---

# Production Notes

Use

- Type Hints
- Dataclasses
- Pydantic
- pathlib
- Enum

for production-ready code.

---

Static Type Checkers

- mypy
- pyright

---

Formatters

- black
- ruff format

---

Linters

- ruff
- pylint

---

Import Sorting

```python
isort
```

---

Package Management

```python
uv
```

or

```python
pip
```

---

Virtual Environment

```python
venv
```

---

Configuration

Prefer

```
pyproject.toml
```

instead of scattered configuration files.

---

# Where I've Used This

FastAPI

- Type Hints
- Pydantic
- Enums
- Dependency Injection

GenAI

- Dataclasses
- Typed Models
- Configuration

Azure

- pathlib
- TOML Configuration

Production APIs

- Enum
- Type Checking
- Static Analysis

CI/CD

- Ruff
- Black
- mypy

---

# Frequently Asked Follow-up Questions

### Why use Type Hints?

Improves

- Readability
- IDE Support
- Static Analysis
- Documentation

---

### Does Python enforce Type Hints?

No.

They are optional.

Type checkers enforce them.

---

### Why use Dataclass?

Reduces boilerplate.

Automatically generates common methods.

---

### Why use Enum?

Avoid magic strings.

Improve readability.

Prevent invalid values.

---

### Difference between TypedDict and Dataclass?

TypedDict

- Dictionary
- Type Checking

Dataclass

- Object
- Methods
- Better OOP

---

### Why use Protocol?

Supports structural typing.

Reduces unnecessary inheritance.

---

### Why prefer pathlib?

Readable.

Cross-platform.

Object-Oriented.

---

### Why use pyproject.toml?

Single source for

- Dependencies
- Tool Configuration
- Build Metadata

---

### Why use Ruff?

Very fast.

Combines linting and formatting capabilities.

Preferred in modern Python projects.

---

# Quick Revision

✅ Type Hint

✅ Optional

✅ Union (`|`)

✅ Literal

✅ Final

✅ TypedDict

✅ NamedTuple

✅ Dataclass

✅ Frozen Dataclass

✅ Enum

✅ Protocol

✅ Pattern Matching

✅ Walrus Operator

✅ pathlib

✅ tomllib

✅ pyproject.toml

✅ Ruff

✅ Black

✅ mypy

✅ Modern Python = Readable + Typed + Maintainable
</details>

---
# Block 12 — Production Python

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐⭐☆ Difficulty | Very High Interview | ⏱ 4–5h Study | 🔄 45m Revision

<details>
<summary><strong>📚 Contents</strong></summary>

- Project Structure
- Virtual Environments
- Dependency Management
- Configuration Management
- Environment Variables
- Logging
- Exception Strategy
- Type Hinting Standards
- Code Quality
- Formatting & Linting
- Testing
- Documentation
- Packaging
- Performance
- Concurrency
- Security Best Practices
- API Development
- CI/CD Readiness
- Pythonic Best Practices
- Interview Pitfalls
- Production Notes
- Frequently Asked Follow-up Questions
- Quick Revision

# Project Structure

Recommended

```text
project/

│── app/
│   ├── api/
│   ├── core/
│   ├── services/
│   ├── models/
│   ├── schemas/
│   ├── database/
│   ├── utils/
│   └── main.py

│── tests/

│── docs/

│── scripts/

│── pyproject.toml

│── README.md

│── .env

│── .gitignore
```

Keep folders focused.

One responsibility per module.

---

# Virtual Environment

Create

```bash
python -m venv .venv
```

Activate (Windows)

```bash
.venv\Scripts\activate
```

Activate (Linux/Mac)

```bash
source .venv/bin/activate
```

---

# Dependency Management

Modern Recommendation

```bash
uv
```

Traditional

```bash
pip
```

Install

```bash
uv add pandas
```

or

```bash
pip install pandas
```

Sync

```bash
uv sync
```

---

# Configuration Management

Never hardcode

- API Keys
- Passwords
- URLs
- Secrets

Bad

```python
API_KEY = "abc123"
```

Good

```python
import os

API_KEY = os.getenv("API_KEY")
```

---

# Environment Variables

Read

```python
import os

DATABASE_URL = os.getenv("DATABASE_URL")
```

Load

```python
from dotenv import load_dotenv

load_dotenv()
```

---

# Logging

Import

```python
import logging
```

Basic

```python
logging.info("Started")
```

Logger

```python
logger = logging.getLogger(__name__)
```

Levels

```python
logging.debug()

logging.info()

logging.warning()

logging.error()

logging.critical()
```

Exception

```python
logger.exception("Unexpected Error")
```

---

# Exception Strategy

Catch

Specific Exceptions

```python
except ValueError:
```

Avoid

```python
except:
```

Raise meaningful exceptions.

---

# Type Hinting

Always

```python
def predict(
    features: list[float]
) -> float:
```

Avoid

```python
def predict(features):
```

---

# Code Formatting

Formatter

```text
Black
```

Run

```bash
black .
```

---

# Linting

Recommended

```text
Ruff
```

Run

```bash
ruff check .
```

Auto Fix

```bash
ruff check . --fix
```

---

# Import Sorting

```bash
isort .
```

---

# Static Type Checking

```bash
mypy .
```

or

```bash
pyright
```

---

# Testing

Framework

```text
pytest
```

Run

```bash
pytest
```

Single File

```bash
pytest tests/test_api.py
```

Assertion

```python
assert result == expected
```

Fixture

```python
@pytest.fixture
```

Mock

```python
from unittest.mock import Mock
```

---

# Documentation

Module

```python
"""
Utility Functions
"""
```

Function

```python
def predict():
    """
    Predict customer churn.
    """
```

---

# Packaging

Project Metadata

```
pyproject.toml
```

---

# Performance

Measure

```python
time.perf_counter()
```

Profile

```python
cProfile
```

Memory

```python
tracemalloc
```

---

# Concurrency

Thread

```python
threading
```

Process

```python
multiprocessing
```

Async

```python
asyncio
```

FastAPI

```python
async def endpoint():
```

---

# Security Best Practices

Never

- Hardcode Secrets
- Print Tokens
- Log Passwords

Validate

- User Input
- File Upload
- JSON Payload

Sanitize

- SQL
- HTML
- API Inputs

---

# API Development

Use

- FastAPI
- Pydantic
- Dependency Injection
- Validation
- Proper Status Codes

Example

```python
raise HTTPException(
    status_code=404,
    detail="Employee not found."
)
```

---

# CI/CD Readiness

Before Every Commit

Run

```bash
ruff check .

black .

pytest
```

Optional

```bash
mypy .
```

---

# Pythonic Best Practices

Prefer

```python
if items:
```

Instead of

```python
if len(items) > 0:
```

---

Prefer

```python
with open()
```

Instead of

```python
open()
```

---

Prefer

```python
pathlib
```

Instead of

```python
os.path
```

---

Prefer

```python
enumerate()
```

Instead of

Manual Index

---

Prefer

```python
zip()
```

Instead of

Index Based Iteration

---

Prefer

Comprehensions

Instead of

Verbose Loops

---

Prefer

Generators

Instead of

Large Lists

---

Keep

Functions

Small.

---

Follow

Single Responsibility Principle.

---

Avoid

Deep Nesting.

Use

Early Return.

---

# Common Development Tools

Formatter

```text
Black
```

Linter

```text
Ruff
```

Type Checker

```text
mypy
```

Testing

```text
pytest
```

Coverage

```text
coverage.py
```

Package Manager

```text
uv
```

Virtual Environment

```text
venv
```

Dependency File

```text
pyproject.toml
```

---

# Interview Pitfalls

⭐⭐⭐⭐⭐

- Global Variables
- Hardcoded Secrets
- Missing Type Hints
- Broad Exception Handling
- Logging vs print()
- Mutable Default Arguments
- Missing Tests
- Circular Imports
- Relative Imports
- Large Functions
- God Classes

---

# Production Notes

Write code for

Humans

First.

Computers

Second.

---

Keep modules

Small.

---

Avoid

Duplicate Logic.

---

Use

Dependency Injection.

---

Separate

Configuration

from

Business Logic.

---

Log

Everything important.

---

Never

Ignore Exceptions.

---

Write

Deterministic Tests.

---

Optimize

After Profiling.

---

Follow

PEP 8.

---

Review

Code before merging.

---

# Where I've Used This

FastAPI

- Dependency Injection
- Pydantic Validation
- Logging
- Middleware
- Exception Handlers

GenAI

- Prompt Pipelines
- Token Tracking
- Azure OpenAI Clients
- Retry Logic
- Configuration Management

Azure

- DevOps Pipelines
- Blob Storage
- Service Bus
- Key Vault
- Container Apps

Data Science

- ETL Pipelines
- Model Training
- Batch Jobs
- Feature Engineering

Production Systems

- Docker
- CI/CD
- Monitoring
- Health Checks
- Configuration
- Secrets

---

# Frequently Asked Follow-up Questions

### What makes Python code production-ready?

- Readable
- Tested
- Typed
- Logged
- Configurable
- Maintainable

---

### Why prefer logging over print()?

Logging supports

- Levels
- Files
- Rotation
- Monitoring
- Structured Logs

---

### Why use Dependency Injection?

Reduces coupling.

Improves testing.

Improves maintainability.

---

### Why use environment variables?

Security.

Environment-specific configuration.

---

### Why use Ruff instead of multiple tools?

Fast.

Modern.

Combines linting and many code quality checks.

---

### Why use uv?

Fast dependency resolution.

Modern Python package management.

Excellent developer experience.

---

### When should async be used?

I/O Bound Tasks

Examples

- APIs
- Database Calls
- HTTP Requests
- File Operations

Not CPU-intensive work.

---

### How do you improve Python performance?

- Profile first.
- Choose correct data structures.
- Use generators.
- Avoid unnecessary copies.
- Cache expensive computations.
- Optimize algorithms before micro-optimizations.

---

### What are the biggest production mistakes?

- Hardcoded secrets
- Poor logging
- Catching every exception
- Missing tests
- Ignoring type hints
- Tight coupling
- Lack of monitoring

---

# Quick Revision

✅ Virtual Environment

✅ uv

✅ pyproject.toml

✅ dotenv

✅ Logging

✅ Ruff

✅ Black

✅ mypy

✅ pytest

✅ Dependency Injection

✅ Environment Variables

✅ Type Hints

✅ Configuration Management

✅ Async IO

✅ PEP 8

✅ Generators

✅ pathlib

✅ Early Return

✅ Small Functions

✅ Single Responsibility

✅ Production Python = Readable + Testable + Typed + Logged + Secure + Maintainable
</details>

---
