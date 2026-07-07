# Python Theory

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐☆☆☆ Difficulty | Very High Interview Value | ⏱ 24–30h Study | 🔄 5–6h Revision

---

# Purpose

This handbook is designed to build a deep understanding of Python for **Data Science, Machine Learning, GenAI, Backend Engineering, and Product Company Interviews**.

The focus is not on memorizing syntax but on understanding **how Python works**, **why it behaves the way it does**, and **when to apply each language feature in production systems**.

This document serves as the conceptual foundation of the repository.

For syntax, examples, and quick reference, refer to **02_Syntax.md**.

---

# Who Should Read This

This handbook is intended for:

- Data Scientists
- Machine Learning Engineers
- GenAI Engineers
- Data Engineers
- Backend Engineers
- Software Engineers
- Experienced Python Developers preparing for interviews

---

# Prerequisites

Readers should be comfortable with:

- Basic programming concepts
- Writing simple Python programs
- Running Python locally
- Basic command-line usage

No prior knowledge of Python internals is required.

---

# Learning Philosophy

This repository follows a simple principle:

> **Understand Python. Don't memorize Python.**

The goal is to develop engineering intuition rather than remember isolated facts.

Every topic emphasizes:

- Why the concept exists
- How Python implements it
- Where it is used
- Common misconceptions
- Production implications

---

# Repository Philosophy

- Interview First Learning
- High Signal > High Volume
- One File = One Responsibility
- Documentation over Notes
- Repository grows with learning
- Every paragraph should improve interview readiness

---

# How to Use This Handbook

Study the blocks sequentially.

Each block builds on concepts introduced earlier.

Recommended workflow:

1. Read the theory.
2. Practice syntax in `02_Syntax.md`.
3. Solve coding problems.
4. Revise Key Takeaways.
5. Continue to the next block.

Avoid skipping foundational topics.

---

# Documentation Conventions

Throughout this handbook:

| Symbol | Meaning |
|---------|----------|
| 💡 | Internal Working |
| ⚠ | Common Mistake |
| ✅ | Best Practice |
| 📝 | Important Note |
| 🚀 | Production Perspective |

---

# Learning Roadmap

- [ ] Block 01 — Python Fundamentals
- [ ] Block 02 — Collections
- [ ] Block 03 — Functions
- [ ] Block 04 — Functional Programming
- [ ] Block 05 — Object-Oriented Programming
- [ ] Block 06 — Exception Handling
- [ ] Block 07 — File Handling & Context Managers
- [ ] Block 08 — Iterators & Generators
- [ ] Block 09 — Decorators
- [ ] Block 10 — Memory Management
- [ ] Block 11 — Modern Python
- [ ] Block 12 — Production Python

---

# Block 01 — Python Fundamentals

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐☆☆☆ Difficulty | Very High Interview Value | ⏱ 3–4 Hours Study

---

## Why This Matters

Python fundamentals are the building blocks of every advanced topic in the language. Whether you're working with Data Science, Machine Learning, Backend Development, Automation, or GenAI, every concept eventually relies on understanding how Python executes code, represents objects, and manages memory.

Unlike many programming languages, Python emphasizes **objects, references, readability, and developer productivity**. Understanding these principles helps you write cleaner code, debug issues faster, and confidently answer interview questions that focus on reasoning rather than syntax.

This block establishes the mental model required for the rest of this handbook.

---

## Core Concepts

Before diving into individual topics, remember these three principles:

- Python is **object-oriented by design**.
- Variables store **references**, not values.
- Everything revolves around **objects and namespaces**.

Understanding these concepts makes later topics like functions, collections, decorators, generators, and memory management much easier.

---

# Python Philosophy

Python was created with a simple goal:

> **Write code for humans first, computers second.**

The language prioritizes readability, simplicity, and explicit behavior over clever or cryptic code.

## Design Principles

Python follows the philosophy described in **The Zen of Python** (`import this`).

Some of the most important principles are:

- Readability counts.
- Explicit is better than implicit.
- Simple is better than complex.
- Complex is better than complicated.
- There should preferably be one obvious way to do something.
- Errors should never pass silently.
- Practicality beats purity.

These principles explain why Python code often looks different from languages like C++, Java, or JavaScript.

---

## Why This Matters

Good Python code is not judged by how short it is.

It is judged by whether another developer can understand it six months later.

Always prefer:

- Clear naming
- Readable logic
- Explicit behavior
- Maintainable code

instead of writing overly clever one-liners.

---

# Python Execution Model

Many beginners believe Python executes source code line by line.

In reality, execution happens through several stages before your program actually runs.

Understanding this process helps explain:

- Syntax Errors
- Bytecode
- `.pyc` files
- Python Virtual Machine
- Import performance

---

## Execution Pipeline

```
Python Source (.py)

        │

        ▼

Tokenizer (Lexical Analysis)

        │

        ▼

Parser

        │

        ▼

Abstract Syntax Tree (AST)

        │

        ▼

Compiler

        │

        ▼

Python Bytecode (.pyc)

        │

        ▼

Python Virtual Machine (PVM)

        │

        ▼

Operating System
```

### Stage 1 — Source Code

You write Python code inside a `.py` file.

```python
x = 10
print(x)
```

---

### Stage 2 — Tokenizer

The tokenizer converts raw text into meaningful language tokens.

Example:

```python
x = 10
```

becomes conceptually

```
NAME

ASSIGN

NUMBER
```

This is the first step toward understanding the program.

---

### Stage 3 — Parser

The parser checks whether the sequence of tokens follows Python's grammar.

If the syntax is invalid, execution stops immediately.

Example:

```python
if True
    print("Hello")
```

Result:

```
SyntaxError
```

No bytecode is generated.

---

### Stage 4 — Abstract Syntax Tree (AST)

Once syntax is validated, Python builds an internal representation of your program called the **Abstract Syntax Tree (AST)**.

Instead of storing text, Python stores the logical structure of the program.

Conceptually:

```
Assignment

├── Variable (x)

└── Constant (10)
```

This representation allows Python to analyze and optimize the program before execution.

---

### Stage 5 — Compilation

The compiler converts the AST into Python Bytecode.

Bytecode is **platform-independent intermediate code**.

It is not machine code.

---

## Bytecode

Bytecode is the instruction set understood by the Python Virtual Machine.

Characteristics:

- Generated automatically
- Platform independent
- Faster to execute than repeatedly parsing source code
- Stored as `.pyc` files inside `__pycache__`

Example:

```
project/

main.py

__pycache__/

main.cpython-312.pyc
```

Python regenerates bytecode whenever the source file changes.

---

## Python Virtual Machine (PVM)

The Python Virtual Machine executes bytecode instruction by instruction.

Conceptually:

```
Bytecode

↓

Python Virtual Machine

↓

Operating System

↓

Hardware
```

The PVM abstracts operating-system differences, allowing the same Python code to run on Windows, Linux, and macOS without recompilation.

---

## CPython

CPython is the **reference implementation** of Python and the one used by most developers.

Its responsibilities include:

- Parsing source code
- Compiling bytecode
- Executing programs
- Managing objects
- Import system
- Memory management
- Garbage collection

Unless explicitly stated otherwise, "Python" usually refers to CPython.

### Other Implementations

| Implementation | Primary Purpose |
|----------------|-----------------|
| CPython | Reference implementation |
| PyPy | JIT compilation for improved performance |
| Jython | Runs on the Java Virtual Machine |
| IronPython | Runs on the .NET runtime |

For interviews, assume **CPython** unless another implementation is mentioned.

---

# Python Object Model

One of Python's most important design principles is:

> **Everything in Python is an object.**

This includes:

- Integers
- Floating-point numbers
- Strings
- Lists
- Tuples
- Dictionaries
- Sets
- Functions
- Classes
- Modules
- Exceptions

Everything behaves as an object with associated data and behavior.

---

## Every Object Has Three Core Properties

Every Python object has:

| Property | Description |
|----------|-------------|
| Identity | Unique identity of the object during its lifetime |
| Type | Defines what operations the object supports |
| Value | The actual data stored inside the object |

Understanding these three properties explains much of Python's runtime behavior.

---

## Identity

Identity uniquely distinguishes one object from every other object.

It remains constant for the lifetime of that object.

```python
x = [1, 2, 3]

id(x)
```

Think of identity as the object's internal identifier.

Identity answers:

> **"Is this the exact same object?"**

Identity comparison uses:

```python
is
```

---

## Type

Every object has exactly one type.

The type determines:

- Available methods
- Supported operators
- Behavior
- Memory representation

Example:

```python
type(10)

type("Python")

type([1, 2])
```

Important:

> Variables do **not** have types.

Objects have types.

---

## Value

The value represents the actual information stored inside an object.

Examples:

| Object | Value |
|---------|-------|
| Integer | 10 |
| String | "Python" |
| List | [1,2,3] |

Some values can change after creation.

Others cannot.

This distinction leads directly to mutability.

---

# Variables vs Objects

One of the biggest misconceptions in Python is believing that variables store values.

They do not.

Variables store **references to objects**.

Consider:

```python
x = 10
```

Many developers imagine:

```
Variable

↓

10
```

Python actually behaves conceptually like this:

```
x

↓

Integer Object

↓

10
```

Now consider:

```python
y = x
```

The integer is **not copied**.

Instead:

```
x ─────┐
       │
       ▼
   Integer(10)
       ▲
       │
y ─────┘
```

Both names reference the same object.

This idea is fundamental to understanding assignment, function arguments, copying, and mutability.

---

# Name Binding & Assignment

Assignment does not create a copy of an object.

Assignment creates a **binding between a name and an object**.

```python
numbers = [1, 2]

backup = numbers
```

Conceptually:

```
numbers ───┐
            │
            ▼
      List Object
            ▲
            │
backup ─────┘
```

No second list is created.

Only a new reference exists.

If one name modifies the list:

```python
numbers.append(3)
```

Both names observe the same change because both refer to the same object.

Understanding name binding prevents many common bugs involving mutable objects.

---

# Identity vs Equality

Identity and equality answer two different questions.

| Operator | Purpose |
|----------|---------|
| `==` | Do these objects have the same value? |
| `is` | Are these references pointing to the same object? |

Example:

```python
a = [1, 2]

b = [1, 2]
```

```
a == b

True
```

because their contents are equal.

```
a is b

False
```

because they are different objects.

Now consider:

```python
c = a
```

```
c == a

True

c is a

True
```

Both names reference the exact same object.

---

## Best Practice

Use:

```python
==
```

for comparing values.

Use:

```python
is
```

only when checking identity.

The most common production example is:

```python
if result is None:
```

Avoid using `is` for comparing numbers, strings, or other values.

---

# Mutable vs Immutable

Objects in Python are classified as either **mutable** or **immutable**.

## Mutable Objects

A mutable object can change after it is created.

Common mutable types:

- list
- dictionary
- set
- bytearray

Example:

```python
numbers = [1, 2]

numbers.append(3)
```

The original list is modified.

No new list is created.

---

## Immutable Objects

An immutable object cannot be modified after creation.

Common immutable types:

- int
- float
- bool
- str
- tuple
- bytes
- frozenset

Example:

```python
text = "Python"

text += " 3"
```

The original string is not modified.

A new string object is created and the variable is rebound to it.

Conceptually:

```
text

↓

"Python"

↓

Create New Object

↓

"Python 3"

↓

text now points here
```

---

## Why Mutability Matters

Mutability affects:

- Assignment
- Function arguments
- Copying
- Memory usage
- Shared references

Many interview questions about Python are ultimately questions about object mutability.

Always ask yourself:

> **"Am I modifying the existing object or creating a new one?"**

That single question explains much of Python's behavior.
