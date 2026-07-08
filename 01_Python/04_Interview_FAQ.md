# Python Interview FAQ

> ⭐⭐⭐⭐⭐ Priority | ⭐⭐⭐☆☆ Difficulty | Very High Interview | ⏱ Living Document | 🔄 Weekly Revision

This file contains interview questions that frequently appear in Python interviews.

---
# Legend

- 🟢 Beginner
- 🟡 Intermediate
- 🔴 Senior

---
# Block 01 — Python Fundamentals
<details>
<summary><strong>📚 Contents</strong></summary>

## 🟢 Q001. Why is Python called dynamically typed?
Keywords: Runtime binding, Variable references, Flexible types, No declaration
Follow-ups: Dynamic vs Strong typing? | Pros and cons?

## 🟢 Q002. What does "everything is an object" mean in Python?
Keywords: Object model, Identity, Type, Methods
Follow-ups: Are functions objects? | Are modules objects?

## 🟢 Q003. Difference between `is` and `==`?
Keywords: Identity, Equality, Reference, Value
Follow-ups: Why use `is` for None? | Object interning?

## 🟢 Q004. What is object identity?
Keywords: id(), Memory identity, Reference, Object
Follow-ups: Can equal objects have different identities?

## 🟢 Q005. What is variable binding?
Keywords: Name binding, References, Assignment, Objects
Follow-ups: Assignment vs Copy?

## 🟢 Q006. Explain mutable vs immutable objects.
Keywords: In-place change, New object, Side effects, Hashability
Follow-ups: Why are strings immutable? | Tuple mutable?

## 🟢 Q007. Why should `None` be compared using `is`?
Keywords: Singleton, Identity, PEP8, Correctness
Follow-ups: Why not `==`?

## 🟢 Q008. What is the LEGB rule?
Keywords: Local, Enclosing, Global, Built-in
Follow-ups: Variable shadowing? | Closures?

## 🟢 Q009. Difference between local and global variables?
Keywords: Scope, Lifetime, Visibility, Namespace
Follow-ups: When use global?

## 🟢 Q010. How are arguments passed in Python?
Keywords: Object reference, Binding, Mutable, Immutable
Follow-ups: Pass-by-value? | Pass-by-reference?

## 🟢 Q011. Why is Python strongly typed?
Keywords: No implicit conversion, Type safety, Runtime check
Follow-ups: Compared to JavaScript?

## 🟢 Q012. What are truthy and falsy values?
Keywords: Boolean context, Empty objects, None, Zero
Follow-ups: Custom truthiness?

## 🟡 Q013. Why can't lists be dictionary keys?
Keywords: Mutable, Hashability, Stable hash, Dictionary
Follow-ups: Why tuples can?

## 🟡 Q014. Explain hashability.
Keywords: __hash__, Immutable, Dictionary, Set
Follow-ups: Hash vs Equality?

## 🟡 Q015. Difference between identity and value?
Keywords: id(), ==, is, Object state
Follow-ups: When identical values differ?

## 🟡 Q016. Why are strings immutable?
Keywords: Performance, Hashing, Thread safety, Optimization
Follow-ups: Benefits?

## 🟡 Q017. Explain namespace.
Keywords: Name mapping, Scope, Lookup, Isolation
Follow-ups: Namespace collision?

## 🟡 Q018. What happens during variable assignment?
Keywords: Reference binding, No copy, Object model
Follow-ups: Deep vs Shallow copy?

## 🟡 Q019. Explain object lifetime.
Keywords: References, GC, Scope, Deallocation
Follow-ups: Reference counting?

## 🟡 Q020. Why is Python considered interpreted?
Keywords: Bytecode, PVM, Interpreter, Compilation
Follow-ups: CPython workflow?

## 🟡 Q021. Difference between compilation and interpretation?
Keywords: Bytecode, Machine code, Execution, Runtime
Follow-ups: Does Python compile?

## 🟡 Q022. Why avoid global variables?
Keywords: Coupling, Testing, Side effects, Maintainability
Follow-ups: Alternatives?

## 🟡 Q023. Explain variable shadowing.
Keywords: Scope, LEGB, Local override, Bugs
Follow-ups: How avoid?

## 🟡 Q024. What is name mangling?
Keywords: __var, Encapsulation, Convention, Access
Follow-ups: True private?

## 🔴 Q025. Explain Python's execution model.
Keywords: Source, Bytecode, PVM, Runtime
Follow-ups: .pyc files? | Optimization?

## 🔴 Q026. Why is mutability important in interviews?
Keywords: Side effects, Functions, Copies, References
Follow-ups: Production bugs?

## 🔴 Q027. How would you explain Python's object model?
Keywords: References, Objects, Identity, Mutability
Follow-ups: Java comparison?

## 🔴 Q028. What misconceptions do candidates have about assignment?
Keywords: Copy vs Reference, Shared state, Binding
Follow-ups: Nested objects?
</details>

---
# Block 02 — Collections
<details>
<summary><strong>📚 Contents</strong></summary>
  
## 🟢 Q029. List vs Tuple?
Keywords: Mutable, Immutable, Memory, Use case
Follow-ups: When prefer tuple?

## 🟢 Q030. List vs Set?
Keywords: Order, Duplicates, Lookup, Hashing
Follow-ups: Membership complexity?

## 🟢 Q031. Dictionary vs List lookup?
Keywords: O(1), O(n), Hash table, Search
Follow-ups: Internal implementation?

## 🟢 Q032. Why use a set?
Keywords: Unique values, Membership, Fast lookup, Hashing
Follow-ups: Duplicate removal?

## 🟢 Q033. Why must dictionary keys be hashable?
Keywords: Stable hash, Immutable, Lookup, Buckets
Follow-ups: Mutable keys?

## 🟢 Q034. Explain shallow copy.
Keywords: Outer copy, Shared nested objects, References
Follow-ups: Deep copy?

## 🟢 Q035. Explain deep copy.
Keywords: Recursive copy, Independent objects, copy.deepcopy
Follow-ups: Performance?

## 🟢 Q036. What is list comprehension?
Keywords: Readability, Concise, Transformation, Pythonic
Follow-ups: Generator expression?

## 🟢 Q037. When should you use tuple?
Keywords: Fixed data, Immutable, Hashable, Lightweight
Follow-ups: NamedTuple?

## 🟢 Q038. Why are sets unordered?
Keywords: Hash table, Implementation, No indexing
Follow-ups: Python ordering?

## 🟢 Q039. What happens if duplicate values are added to a set?
Keywords: Unique elements, Hashing, Ignore duplicates
Follow-ups: Equality rules?

## 🟢 Q040. Difference between `remove()` and `discard()`?
Keywords: KeyError, Safe removal, Set methods
Follow-ups: pop()?

## 🟡 Q041. Why is dictionary lookup O(1)?
Keywords: Hash table, Buckets, Average case, Hash function
Follow-ups: Worst case?

## 🟡 Q042. Explain hash collisions.
Keywords: Same bucket, Collision handling, Performance
Follow-ups: Resolution strategy?

## 🟡 Q043. Why are tuples more memory efficient?
Keywords: Immutable, Compact layout, Optimization
Follow-ups: Performance gain?

## 🟡 Q044. How do shallow copies cause bugs?
Keywords: Nested objects, Shared references, Side effects
Follow-ups: Debugging?

## 🟡 Q045. Why avoid modifying a list during iteration?
Keywords: Iterator invalidation, Skipped elements, Bugs
Follow-ups: Safe alternatives?

## 🟡 Q046. List comprehension vs map()?
Keywords: Readability, Functional style, Performance
Follow-ups: When use map?

## 🟡 Q047. Why are dictionaries ordered in modern Python?
Keywords: Insertion order, Python 3.7+, Language guarantee
Follow-ups: OrderedDict?

## 🟡 Q048. Explain amortized O(1) append.
Keywords: Dynamic array, Resize, Capacity, Allocation
Follow-ups: Worst case?

## 🟡 Q049. Why prefer set for membership testing?
Keywords: O(1), Hashing, Performance, Large datasets
Follow-ups: Trade-offs?

## 🟡 Q050. Explain dictionary resizing.
Keywords: Rehashing, Capacity growth, Performance
Follow-ups: Memory overhead?

## 🟡 Q051. What makes an object hashable?
Keywords: Immutable, __hash__, __eq__, Stable value
Follow-ups: Custom classes?

## 🟡 Q052. Why shouldn't mutable objects be hashed?
Keywords: Changing hash, Dictionary corruption, Lookup failure
Follow-ups: Frozen dataclass?

## 🔴 Q053. How are dictionaries implemented internally?
Keywords: Hash table, Buckets, Collision, Probing
Follow-ups: CPython specifics?

## 🔴 Q054. Explain time complexity trade-offs among collections.
Keywords: Lookup, Insert, Delete, Memory
Follow-ups: Real-world choice?

## 🔴 Q055. When would you optimize collection choice?
Keywords: Profiling, Bottleneck, Access pattern, Scalability
Follow-ups: Premature optimization?

## 🔴 Q056. How would you choose the right collection in production?
Keywords: Access pattern, Complexity, Memory, Maintainability
Follow-ups: Real production example?

</details>

---

# Block 03 — Functions

<details>
<summary>📚 Contents</summary>

## 🟢 Q057. What are first-class functions?
Keywords: Objects, Assignable, Pass as argument, Return from function
Follow-ups: Why important for decorators? | Higher-order functions?

## 🟢 Q058. Difference between parameters and arguments?
Keywords: Definition, Invocation, Formal, Actual
Follow-ups: Positional vs Keyword?

## 🟢 Q059. Positional vs keyword arguments?
Keywords: Order, Readability, Explicit, Flexibility
Follow-ups: Mixing rules?

## 🟢 Q060. What are default arguments?
Keywords: Optional parameters, Defaults, Function signature
Follow-ups: Mutable default pitfall?

## 🟢 Q061. What is `*args`?
Keywords: Variable positional arguments, Tuple, Flexibility
Follow-ups: Difference from list?

## 🟢 Q062. What is `**kwargs`?
Keywords: Variable keyword arguments, Dictionary, Named parameters
Follow-ups: Order preservation?

## 🟢 Q063. Difference between `*args` and `**kwargs`?
Keywords: Positional, Keyword, Tuple, Dictionary
Follow-ups: Can both be used together?

## 🟢 Q064. What does a function return if no return statement exists?
Keywords: None, Implicit return, Default behavior
Follow-ups: Explicit vs implicit return?

## 🟢 Q065. Why are functions considered objects?
Keywords: First-class, References, Assignment, Callables
Follow-ups: Function attributes?

## 🟢 Q066. What are type hints?
Keywords: Readability, IDE, Static analysis, Documentation
Follow-ups: Runtime enforcement?

## 🟢 Q067. What is a docstring?
Keywords: Documentation, Help(), Maintainability, API
Follow-ups: Docstring vs comment?

## 🟢 Q068. What is recursion?
Keywords: Self-call, Base case, Recursive case
Follow-ups: Recursion limit?

## 🟡 Q069. Explain Python's argument passing mechanism.
Keywords: Object references, Binding, Mutable, Immutable
Follow-ups: Pass-by-reference myth?

## 🟡 Q070. Why are mutable default arguments dangerous?
Keywords: Shared state, Persistent object, Unexpected behavior
Follow-ups: Correct solution?

## 🟡 Q071. What are keyword-only arguments?
Keywords: *, Explicit API, Readability
Follow-ups: Production use cases?

## 🟡 Q072. What are positional-only arguments?
Keywords: /, API stability, Performance
Follow-ups: Why introduced?

## 🟡 Q073. Explain LEGB in functions.
Keywords: Scope, Namespace, Lookup, Closures
Follow-ups: Shadowing?

## 🟡 Q074. What is a closure?
Keywords: Nested function, Captured variables, State
Follow-ups: Decorators?

## 🟡 Q075. Lambda vs normal function?
Keywords: Anonymous, Single expression, Readability
Follow-ups: When avoid lambda?

## 🟡 Q076. Can Python overload functions?
Keywords: No true overloading, Redefinition, Default args
Follow-ups: Alternatives?

## 🟡 Q077. Function vs method?
Keywords: Class, Instance, Self, Invocation
Follow-ups: Static method?

## 🟡 Q078. Why keep functions small?
Keywords: Readability, Testing, Maintainability, SRP
Follow-ups: Ideal function size?

## 🟡 Q079. Pure function vs impure function?
Keywords: Side effects, Deterministic, Testability
Follow-ups: Production benefits?

## 🟡 Q080. What makes a good function API?
Keywords: Explicit, Predictable, Minimal, Reusable
Follow-ups: Keyword-only parameters?

## 🔴 Q081. Design a reusable function for a library.
Keywords: Generic, Validation, Documentation, Exceptions
Follow-ups: Public API?

## 🔴 Q082. How would you optimize a function?
Keywords: Profile first, Complexity, Caching, Bottlenecks
Follow-ups: Premature optimization?

## 🔴 Q083. How do decorators affect functions?
Keywords: Wrapper, Metadata, Higher-order, Closures
Follow-ups: functools.wraps?

## 🔴 Q084. What are common function design mistakes?
Keywords: Long functions, Side effects, Globals, Hidden dependencies
Follow-ups: Refactoring strategy?

</details>

---

# Block 04 — Functional Programming

<details>
<summary>📚 Contents</summary>

## 🟢 Q085. What is functional programming?
Keywords: Declarative, Pure functions, Immutability, Composition
Follow-ups: OOP vs Functional?

## 🟢 Q086. What is a pure function?
Keywords: No side effects, Same input-output, Predictable
Follow-ups: Benefits?

## 🟢 Q087. What are side effects?
Keywords: I/O, Global state, Mutation, External changes
Follow-ups: Examples?

## 🟢 Q088. What is a higher-order function?
Keywords: Accept functions, Return functions, Abstraction
Follow-ups: Examples?

## 🟢 Q089. What is `map()`?
Keywords: Transformation, Iterable, Function application
Follow-ups: List comprehension?

## 🟢 Q090. What is `filter()`?
Keywords: Selection, Predicate, Lazy evaluation
Follow-ups: Comprehension alternative?

## 🟢 Q091. What is `reduce()`?
Keywords: Aggregation, functools, Accumulator
Follow-ups: When avoid?

## 🟢 Q092. What is function composition?
Keywords: Pipeline, Chaining, Reusability
Follow-ups: ETL examples?

## 🟢 Q093. Why are functions first-class objects important?
Keywords: Flexibility, Callbacks, Decorators, Composition
Follow-ups: Framework examples?

## 🟢 Q094. Lambda vs comprehension?
Keywords: Readability, Simplicity, Functional style
Follow-ups: Which is preferred?

## 🟢 Q095. Why avoid complex lambda expressions?
Keywords: Readability, Maintainability, Debugging
Follow-ups: Refactor approach?

## 🟢 Q096. Why prefer immutable data?
Keywords: Predictability, Thread safety, Reliability
Follow-ups: Performance?

## 🟡 Q097. List comprehension vs `map()`?
Keywords: Pythonic, Readability, Performance
Follow-ups: When use map?

## 🟡 Q098. List comprehension vs generator expression?
Keywords: Lazy, Memory, Performance
Follow-ups: Large datasets?

## 🟡 Q099. What is lazy evaluation?
Keywords: On-demand, Memory efficient, Deferred execution
Follow-ups: Generators?

## 🟡 Q100. Explain closures in functional programming.
Keywords: State retention, Nested scope, Encapsulation
Follow-ups: Decorators?

## 🟡 Q101. Why avoid side effects?
Keywords: Testing, Predictability, Reusability
Follow-ups: Exceptions?

## 🟡 Q102. When should `reduce()` be avoided?
Keywords: Readability, Alternatives, Simplicity
Follow-ups: sum()?

## 🟡 Q103. What is function composition used for?
Keywords: Pipelines, ETL, ML workflows, Chaining
Follow-ups: Production examples?

## 🟡 Q104. Functional vs imperative programming?
Keywords: Declarative, Control flow, State, Readability
Follow-ups: Python preference?

## 🟡 Q105. Functional vs object-oriented programming?
Keywords: Composition, Objects, State, Behavior
Follow-ups: Hybrid design?

## 🟡 Q106. Why is immutability useful in concurrency?
Keywords: No shared state, Safety, Predictability
Follow-ups: Threading?

## 🟡 Q107. Why are comprehensions preferred in Python?
Keywords: Readability, Pythonic, Conciseness
Follow-ups: Nested comprehensions?

## 🔴 Q108. Where is functional programming useful in production?
Keywords: ETL, Data pipelines, ML preprocessing, Streaming
Follow-ups: Real examples?

## 🔴 Q109. Functional programming trade-offs?
Keywords: Learning curve, Readability, Debugging, Balance
Follow-ups: Team preference?

## 🔴 Q110. How do decorators leverage functional programming?
Keywords: Higher-order functions, Closures, Wrappers
Follow-ups: Execution flow?

## 🔴 Q111. How would you refactor imperative code into functional style?
Keywords: Composition, Pure functions, Pipelines, Immutability
Follow-ups: Maintainability?

## 🔴 Q112. Common misconceptions about functional programming?
Keywords: No loops, No OOP replacement, Pragmatic usage
Follow-ups: Python's multi-paradigm design?

</details>

---

# Block 05 — Object-Oriented Programming (OOP)

<details>
<summary>📚 Contents</summary>

## 🟢 Q113. What are the four pillars of OOP?
Keywords: Encapsulation, Inheritance, Polymorphism, Abstraction
Follow-ups: Which is most important? | Real examples?

## 🟢 Q114. Class vs Object?
Keywords: Blueprint, Instance, State, Behavior
Follow-ups: Memory allocation?

## 🟢 Q115. Instance variable vs Class variable?
Keywords: Shared state, Object state, Namespace
Follow-ups: Common mistakes?

## 🟢 Q116. Instance method vs Class method vs Static method?
Keywords: self, cls, Utility, Factory
Follow-ups: When use each?

## 🟢 Q117. What is `self`?
Keywords: Instance reference, First parameter, Object access
Follow-ups: Why explicit?

## 🟢 Q118. What is `cls`?
Keywords: Class reference, Factory methods, Alternative constructor
Follow-ups: cls vs self?

## 🟢 Q119. What is a constructor?
Keywords: __init__, Initialization, Object creation
Follow-ups: __new__?

## 🟢 Q120. What is encapsulation?
Keywords: Data hiding, Interface, Access control, Maintainability
Follow-ups: Private variables?

## 🟢 Q121. What is inheritance?
Keywords: Code reuse, IS-A, Parent-child
Follow-ups: Multiple inheritance?

## 🟢 Q122. What is polymorphism?
Keywords: Same interface, Different behavior, Duck typing
Follow-ups: Runtime polymorphism?

## 🟢 Q123. What is abstraction?
Keywords: Interface, Hide implementation, Simplicity
Follow-ups: ABC module?

## 🟢 Q124. What is duck typing?
Keywords: Behavior, Interface, Dynamic typing
Follow-ups: Duck typing vs inheritance?

## 🟡 Q125. Composition vs Inheritance?
Keywords: HAS-A, IS-A, Flexibility, Maintainability
Follow-ups: Which is preferred?

## 🟡 Q126. Method overloading vs overriding?
Keywords: Overriding, No true overloading, Polymorphism
Follow-ups: Python alternatives?

## 🟡 Q127. How does `super()` work?
Keywords: Parent access, MRO, Cooperative inheritance
Follow-ups: Multiple inheritance?

## 🟡 Q128. Explain MRO.
Keywords: Method Resolution Order, C3 Linearization, Diamond problem
Follow-ups: mro()?

## 🟡 Q129. What are magic methods?
Keywords: Dunder methods, Operator overloading, Protocols
Follow-ups: Common methods?

## 🟡 Q130. `__str__()` vs `__repr__()`?
Keywords: User representation, Developer representation, Debugging
Follow-ups: Which is default?

## 🟡 Q131. What are dataclasses?
Keywords: Boilerplate reduction, Immutable option, Type hints
Follow-ups: dataclass vs normal class?

## 🟡 Q132. Why use Abstract Base Classes?
Keywords: Contract, Interface, abc module
Follow-ups: Protocols?

## 🟡 Q133. Public vs Protected vs Private?
Keywords: Convention, Name mangling, Encapsulation
Follow-ups: True private?

## 🟡 Q134. Explain SOLID principles.
Keywords: SRP, OCP, LSP, ISP, DIP
Follow-ups: Most violated principle?

## 🟡 Q135. Favor composition over inheritance—why?
Keywords: Loose coupling, Flexibility, Testability
Follow-ups: Examples?

## 🔴 Q136. Design a class hierarchy for a payment system.
Keywords: Extensibility, Polymorphism, Composition
Follow-ups: LSP?

## 🔴 Q137. How would you model real-world entities?
Keywords: Responsibility, Relationships, Abstraction
Follow-ups: Domain-driven design?

## 🔴 Q138. Common OOP design mistakes?
Keywords: God object, Tight coupling, Deep inheritance
Follow-ups: Refactoring?

## 🔴 Q139. When should you avoid inheritance?
Keywords: Composition, Coupling, Maintenance
Follow-ups: Strategy pattern?

## 🔴 Q140. OOP interview red flags?
Keywords: Overengineering, Wrong abstraction, SRP violations
Follow-ups: Production examples?

</details>

---

# Block 06 — Exception Handling

<details>
<summary>📚 Contents</summary>

## 🟢 Q141. What is an exception?
Keywords: Runtime error, Control flow, Recovery
Follow-ups: Exception vs Error?

## 🟢 Q142. SyntaxError vs Exception?
Keywords: Parse time, Runtime, Recoverability
Follow-ups: Can SyntaxError be caught?

## 🟢 Q143. Purpose of try-except?
Keywords: Error handling, Recovery, Stability
Follow-ups: Multiple except?

## 🟢 Q144. Why catch specific exceptions?
Keywords: Precision, Debugging, Safety
Follow-ups: Why not Exception?

## 🟢 Q145. Why avoid bare `except:`?
Keywords: KeyboardInterrupt, SystemExit, Hidden bugs
Follow-ups: Difference from Exception?

## 🟢 Q146. Purpose of else block?
Keywords: Success path, Readability, Separation
Follow-ups: Why use else?

## 🟢 Q147. Purpose of finally?
Keywords: Cleanup, Always executes, Resource release
Follow-ups: Return in finally?

## 🟢 Q148. What is traceback?
Keywords: Call stack, Debugging, Error origin
Follow-ups: Stack unwinding?

## 🟢 Q149. What does raise do?
Keywords: Explicit exception, Validation, Propagation
Follow-ups: raise vs assert?

## 🟢 Q150. What are custom exceptions?
Keywords: Business rules, Domain errors, Readability
Follow-ups: Inheritance?

## 🟢 Q151. Why log exceptions?
Keywords: Debugging, Monitoring, Context
Follow-ups: Log and rethrow?

## 🟢 Q152. Difference between Exception and BaseException?
Keywords: KeyboardInterrupt, SystemExit, Hierarchy
Follow-ups: Which to catch?

## 🟡 Q153. Explain exception chaining.
Keywords: raise from, Root cause, Traceback
Follow-ups: Benefits?

## 🟡 Q154. Raise vs re-raise?
Keywords: Preserve traceback, Error propagation
Follow-ups: raise e?

## 🟡 Q155. Assert vs raise?
Keywords: Debugging, Validation, Optimization
Follow-ups: Production use?

## 🟡 Q156. EAFP vs LBYL?
Keywords: Pythonic, Race conditions, Readability
Follow-ups: Examples?

## 🟡 Q157. Should exceptions control program flow?
Keywords: Performance, Exceptional cases, Clarity
Follow-ups: Best practice?

## 🟡 Q158. Exception hierarchy design?
Keywords: Base class, Domain exceptions, Organization
Follow-ups: Naming?

## 🟡 Q159. Why avoid `except: pass`?
Keywords: Silent failures, Hidden bugs, Debugging
Follow-ups: Any valid use?

## 🟡 Q160. When should exceptions propagate?
Keywords: Recovery boundary, API, Layers
Follow-ups: Service layer?

## 🟡 Q161. Common built-in exceptions?
Keywords: ValueError, TypeError, KeyError, IndexError
Follow-ups: AttributeError?

## 🟡 Q162. Multiple except order?
Keywords: Specific first, Generic last, Hierarchy
Follow-ups: Wrong order?

## 🔴 Q163. Exception strategy in production?
Keywords: Logging, Monitoring, Recovery, Fail fast
Follow-ups: Retry?

## 🔴 Q164. How do exceptions affect performance?
Keywords: Stack unwinding, Cost, Rare path
Follow-ups: Benchmarks?

## 🔴 Q165. Debug intermittent production exceptions?
Keywords: Logs, Metrics, Correlation ID
Follow-ups: Missing logs?

## 🔴 Q166. Design exception hierarchy for an API.
Keywords: Validation, Authentication, Business rules
Follow-ups: HTTP mapping?

## 🔴 Q167. Library vs application exception handling?
Keywords: Propagation, Responsibility, Contracts
Follow-ups: Logging?

## 🔴 Q168. Common exception-handling mistakes?
Keywords: Generic catch, Swallowing, Wrong abstraction
Follow-ups: Refactoring?

</details>

---

# Block 07 — File Handling & Context Managers

<details>
<summary>📚 Contents</summary>

## 🟢 Q169. Why use `with open()`?
Keywords: Context manager, Cleanup, Safety
Follow-ups: Internal working?

## 🟢 Q170. File modes?
Keywords: r, w, a, x, Binary
Follow-ups: r+?

## 🟢 Q171. read() vs readline() vs readlines()?
Keywords: Memory, Line-by-line, Entire file
Follow-ups: Large files?

## 🟢 Q172. Why specify encoding?
Keywords: UTF-8, Portability, Unicode
Follow-ups: Default encoding?

## 🟢 Q173. What is a context manager?
Keywords: Resource management, Cleanup, with
Follow-ups: __enter__?

## 🟢 Q174. Purpose of `__enter__()`?
Keywords: Resource acquisition, Setup
Follow-ups: Return value?

## 🟢 Q175. Purpose of `__exit__()`?
Keywords: Cleanup, Exception handling, Release
Follow-ups: Exception suppression?

## 🟢 Q176. Text vs Binary mode?
Keywords: Encoding, Bytes, Files
Follow-ups: Images?

## 🟢 Q177. What is buffering?
Keywords: Performance, I/O, Flush
Follow-ups: flush()?

## 🟢 Q178. What is file pointer?
Keywords: tell(), seek(), Position
Follow-ups: Random access?

## 🟢 Q179. Why use pathlib?
Keywords: Cross-platform, Readability, OO API
Follow-ups: os.path?

## 🟢 Q180. Why iterate over a file?
Keywords: Streaming, Memory efficiency
Follow-ups: Huge files?

## 🟡 Q181. How do context managers work?
Keywords: enter, exit, Deterministic cleanup
Follow-ups: Implementation?

## 🟡 Q182. Custom context managers?
Keywords: __enter__, __exit__, Resource lifecycle
Follow-ups: Use cases?

## 🟡 Q183. `contextlib` purpose?
Keywords: @contextmanager, Simplicity, Utilities
Follow-ups: Class vs decorator?

## 🟡 Q184. Why stream large files?
Keywords: Memory, Performance, Scalability
Follow-ups: Generators?

## 🟡 Q185. Common file handling mistakes?
Keywords: Missing close, Wrong encoding, Memory
Follow-ups: Production issues?

## 🟡 Q186. What resources use context managers?
Keywords: DB, Locks, Sockets, Files
Follow-ups: Transactions?

## 🟡 Q187. Why is deterministic cleanup important?
Keywords: Reliability, Resources, Stability
Follow-ups: finally?

## 🟡 Q188. What happens if file isn't closed?
Keywords: Leaks, Locks, Buffers
Follow-ups: OS behavior?

## 🔴 Q189. Design a custom context manager.
Keywords: Resource lifecycle, Cleanup, API
Follow-ups: Real examples?

## 🔴 Q190. Process a 100GB file efficiently.
Keywords: Streaming, Iteration, Chunking
Follow-ups: Parallel processing?

## 🔴 Q191. File handling in distributed systems?
Keywords: Cloud storage, Streams, Retries
Follow-ups: S3?

## 🔴 Q192. Production file processing strategy?
Keywords: Validation, Logging, Retry
Follow-ups: Corrupt files?

## 🔴 Q193. Context manager interview pitfalls?
Keywords: Exception suppression, Cleanup
Follow-ups: __exit__ return?

## 🔴 Q194. Large CSV processing best practices?
Keywords: Chunking, Generators, Memory
Follow-ups: Pandas chunks?

## 🔴 Q195. Why avoid read() on huge files?
Keywords: Memory exhaustion, Streaming
Follow-ups: Alternatives?

## 🔴 Q196. File I/O optimization?
Keywords: Buffering, Batch writes, Profiling
Follow-ups: SSD vs HDD?

</details>

---

# Block 08 — Iterators & Generators

<details>
<summary>📚 Contents</summary>

## 🟢 Q197. Iterable vs Iterator?
Keywords: __iter__, __next__, Protocol
Follow-ups: Examples?

## 🟢 Q198. What is iterator protocol?
Keywords: iter(), next(), StopIteration
Follow-ups: for loop?

## 🟢 Q199. What is a generator?
Keywords: yield, Lazy evaluation, Iterator
Follow-ups: Benefits?

## 🟢 Q200. yield vs return?
Keywords: Pause, Resume, Terminate
Follow-ups: Multiple yields?

## 🟢 Q201. Generator expression vs List comprehension?
Keywords: Lazy, Memory, Performance
Follow-ups: Use cases?

## 🟢 Q202. Why are generators memory efficient?
Keywords: Lazy evaluation, Streaming, On demand
Follow-ups: Large datasets?

## 🟢 Q203. What causes StopIteration?
Keywords: End of iteration, Iterator protocol
Follow-ups: Manual iteration?

## 🟢 Q204. How does `for` loop work internally?
Keywords: iter(), next(), StopIteration
Follow-ups: Desugaring?

## 🟢 Q205. What is lazy evaluation?
Keywords: Deferred execution, Efficiency, Memory
Follow-ups: Examples?

## 🟢 Q206. Can generators be reused?
Keywords: Exhausted, Single pass, Recreation
Follow-ups: Reset?

## 🟢 Q207. Common iterator examples?
Keywords: range, zip, enumerate, map
Follow-ups: Lazy?

## 🟢 Q208. Why use enumerate()?
Keywords: Index, Cleaner code, Readability
Follow-ups: start parameter?

## 🟡 Q209. Iterator vs Generator?
Keywords: Manual implementation, yield, Simplicity
Follow-ups: Performance?

## 🟡 Q210. Custom iterator?
Keywords: __iter__, __next__, State
Follow-ups: Examples?

## 🟡 Q211. Generator lifecycle?
Keywords: Pause, Resume, State preservation
Follow-ups: Internal frame?

## 🟡 Q212. Why are generators good for ETL?
Keywords: Streaming, Pipelines, Memory
Follow-ups: Production use?

## 🟡 Q213. When not to use generators?
Keywords: Multiple passes, Random access
Follow-ups: Materialization?

## 🟡 Q214. map() returns what?
Keywords: Iterator, Lazy evaluation
Follow-ups: Python 2 difference?

## 🟡 Q215. zip() behavior?
Keywords: Iterator, Parallel iteration
Follow-ups: Unequal lengths?

## 🟡 Q216. enumerate() vs range(len())?
Keywords: Pythonic, Readability, Efficiency
Follow-ups: Best practice?

## 🔴 Q217. Explain generator state preservation.
Keywords: Frame object, Local variables, Resume
Follow-ups: yield from?

## 🔴 Q218. Build scalable data pipeline.
Keywords: Streaming, Generators, Composition
Follow-ups: Backpressure?

## 🔴 Q219. Generator performance trade-offs?
Keywords: CPU, Memory, Reusability
Follow-ups: Profiling?

## 🔴 Q220. Iterator protocol interview traps?
Keywords: StopIteration, Exhaustion, State
Follow-ups: Bugs?

## 🔴 Q221. Generator vs coroutine?
Keywords: yield, async, await
Follow-ups: Evolution?

## 🔴 Q222. Infinite generators?
Keywords: Lazy, Infinite sequence, next()
Follow-ups: Safe usage?

## 🔴 Q223. Production use of generators?
Keywords: Logs, APIs, ETL, ML
Follow-ups: Streaming frameworks?

## 🔴 Q224. Common iterator/generator mistakes?
Keywords: Exhausted iterators, Hidden state, Memory assumptions
Follow-ups: Debugging?

</details>

---
# Block 09 — Decorators

<details>
<summary>📚 Contents</summary>

## 🟢 Q225. What is a decorator?
Keywords: Wrapper, Higher-order function, Reusable behavior, Function enhancement
Follow-ups: Why are decorators useful? | Real-world examples?

## 🟢 Q226. Why are decorators possible in Python?
Keywords: First-class functions, Closures, Higher-order functions
Follow-ups: Functions as objects?

## 🟢 Q227. What does `@decorator` syntax do?
Keywords: Syntactic sugar, Function reassignment, Wrapper
Follow-ups: Equivalent code?

## 🟢 Q228. What problem do decorators solve?
Keywords: Separation of concerns, Reusability, DRY
Follow-ups: Cross-cutting concerns?

## 🟢 Q229. Why do decorators use wrappers?
Keywords: Pre-processing, Post-processing, Function interception
Follow-ups: Wrapper arguments?

## 🟢 Q230. What is `functools.wraps`?
Keywords: Metadata preservation, __name__, __doc__, Introspection
Follow-ups: Why important?

## 🟢 Q231. What are common built-in decorators?
Keywords: property, staticmethod, classmethod, dataclass
Follow-ups: lru_cache?

## 🟢 Q232. What is a parameterized decorator?
Keywords: Decorator factory, Arguments, Nested functions
Follow-ups: Additional nesting?

## 🟢 Q233. Multiple decorators execution order?
Keywords: Bottom-up, Wrapper chain, Nesting
Follow-ups: Execution flow?

## 🟢 Q234. Decorator vs normal function?
Keywords: Function enhancement, Wrapper, Reusability
Follow-ups: When avoid decorators?

## 🟢 Q235. Where are decorators commonly used?
Keywords: Logging, Authentication, Caching, Validation
Follow-ups: Framework examples?

## 🟢 Q236. What is a class decorator?
Keywords: Class enhancement, Metadata, Registration
Follow-ups: Function vs class decorators?

## 🟡 Q237. Decorators vs inheritance?
Keywords: Composition, Behavior extension, Flexibility
Follow-ups: Which is preferable?

## 🟡 Q238. Decorators vs middleware?
Keywords: Cross-cutting concerns, Request pipeline
Follow-ups: Web frameworks?

## 🟡 Q239. Why do decorators rely on closures?
Keywords: State preservation, Captured variables, Wrapper
Follow-ups: Closure recap?

## 🟡 Q240. Why preserve metadata?
Keywords: Debugging, Reflection, Documentation
Follow-ups: wraps vs no wraps?

## 🟡 Q241. How do decorators affect debugging?
Keywords: Stack traces, Wrappers, Metadata
Follow-ups: Debugging tips?

## 🟡 Q242. When should decorators be avoided?
Keywords: Readability, Complexity, Hidden behavior
Follow-ups: Alternatives?

## 🟡 Q243. Decorators vs monkey patching?
Keywords: Explicit, Safe, Maintainable
Follow-ups: Production usage?

## 🟡 Q244. How do decorators improve maintainability?
Keywords: Reusability, DRY, Separation
Follow-ups: Logging example?

## 🔴 Q245. Design a retry decorator.
Keywords: Retry, Backoff, Exceptions, Resilience
Follow-ups: Max retries?

## 🔴 Q246. Design a caching decorator.
Keywords: Memoization, Cache key, Performance
Follow-ups: Cache invalidation?

## 🔴 Q247. Authentication decorator design?
Keywords: Authorization, Tokens, Validation
Follow-ups: Role-based access?

## 🔴 Q248. Timing decorator implementation?
Keywords: Profiling, Performance, Metrics
Follow-ups: Production logging?

## 🔴 Q249. Decorators interview pitfalls?
Keywords: Metadata loss, Hidden flow, Complexity
Follow-ups: wraps?

## 🔴 Q250. Decorators in production?
Keywords: Observability, Logging, Validation, Security
Follow-ups: FastAPI?

## 🔴 Q251. Common decorator mistakes?
Keywords: Missing wraps, State bugs, Side effects
Follow-ups: Thread safety?

## 🔴 Q252. Decorators vs AOP?
Keywords: Cross-cutting concerns, Aspect-oriented design
Follow-ups: Spring comparison?

</details>

---

# Block 10 — Memory Management

<details>
<summary>📚 Contents</summary>

## 🟢 Q253. How does Python manage memory?
Keywords: Heap, Reference counting, Garbage collection
Follow-ups: CPython?

## 🟢 Q254. What is reference counting?
Keywords: Object lifetime, References, Deallocation
Follow-ups: Limitations?

## 🟢 Q255. Why is garbage collection needed?
Keywords: Cyclic references, Memory cleanup
Follow-ups: Reference counting alone?

## 🟢 Q256. What is object lifetime?
Keywords: Creation, References, Destruction
Follow-ups: del keyword?

## 🟢 Q257. Assignment vs copy?
Keywords: References, Shared objects, Identity
Follow-ups: Mutable objects?

## 🟢 Q258. Shallow vs deep copy?
Keywords: Nested objects, copy module, References
Follow-ups: deepcopy cost?

## 🟢 Q259. What is object interning?
Keywords: Small integers, Strings, Optimization
Follow-ups: Can rely on it?

## 🟢 Q260. Why shouldn't `is` compare values?
Keywords: Identity, Optimization, Undefined behavior
Follow-ups: Exceptions?

## 🟢 Q261. What is a memory leak in Python?
Keywords: Retained references, Long-lived objects
Follow-ups: Examples?

## 🟢 Q262. What does `del` do?
Keywords: Remove binding, Reference count
Follow-ups: Free memory?

## 🟢 Q263. What is `weakref`?
Keywords: Weak references, Caching, GC
Follow-ups: Use cases?

## 🟢 Q264. Where are Python objects stored?
Keywords: Heap, References, Memory model
Follow-ups: Stack?

## 🟡 Q265. Why can't reference counting handle cycles?
Keywords: Circular references, GC
Follow-ups: Example?

## 🟡 Q266. Explain cyclic garbage collection.
Keywords: Cycle detection, Unreachable objects
Follow-ups: GC generations?

## 🟡 Q267. Why are immutable objects memory efficient?
Keywords: Interning, Reuse, Optimization
Follow-ups: Strings?

## 🟡 Q268. Why avoid unnecessary copies?
Keywords: Performance, Memory, Scalability
Follow-ups: Profiling?

## 🟡 Q269. How do memory leaks occur?
Keywords: Global references, Caches, Closures
Follow-ups: Detection?

## 🟡 Q270. Reference counting vs garbage collection?
Keywords: Immediate cleanup, Cycles, Cooperation
Follow-ups: CPython?

## 🟡 Q271. Common memory optimization techniques?
Keywords: Generators, Streaming, Profiling
Follow-ups: Large datasets?

## 🟡 Q272. What affects object lifetime?
Keywords: Scope, References, Containers
Follow-ups: Closures?

## 🔴 Q273. How would you debug memory leaks?
Keywords: tracemalloc, gc, Profiling
Follow-ups: Production tools?

## 🔴 Q274. Explain pymalloc.
Keywords: Small object allocator, Performance
Follow-ups: Implementation?

## 🔴 Q275. Memory optimization strategy?
Keywords: Measure, Profile, Optimize
Follow-ups: Premature optimization?

## 🔴 Q276. Large ML dataset memory handling?
Keywords: Streaming, Chunking, Generators
Follow-ups: NumPy?

## 🔴 Q277. Weak references in production?
Keywords: Cache, Observer pattern
Follow-ups: Limitations?

## 🔴 Q278. Memory interview pitfalls?
Keywords: is vs ==, Copies, References
Follow-ups: Common mistakes?

## 🔴 Q279. CPython memory model?
Keywords: Heap, Allocator, GC
Follow-ups: PyPy differences?

## 🔴 Q280. Production memory best practices?
Keywords: Profiling, Streaming, Efficient structures
Follow-ups: Monitoring?

</details>

---

# Block 11 — Modern Python

<details>
<summary>📚 Contents</summary>

## 🟢 Q281. Why use type hints?
Keywords: Readability, IDE, Static analysis
Follow-ups: Runtime enforcement?

## 🟢 Q282. Are type hints mandatory?
Keywords: Optional, Tooling, Documentation
Follow-ups: mypy?

## 🟢 Q283. What are dataclasses?
Keywords: Boilerplate reduction, Auto-generated methods
Follow-ups: attrs?

## 🟢 Q284. Why prefer `pathlib`?
Keywords: Cross-platform, Object-oriented paths
Follow-ups: os.path?

## 🟢 Q285. Why use f-strings?
Keywords: Readability, Performance, Formatting
Follow-ups: format()?

## 🟢 Q286. What are Enums?
Keywords: Constants, Readability, Domain modeling
Follow-ups: IntEnum?

## 🟢 Q287. What is structural pattern matching?
Keywords: match-case, Branching, Pattern matching
Follow-ups: switch comparison?

## 🟢 Q288. What is the walrus operator?
Keywords: :=, Assignment expression, Readability
Follow-ups: When avoid?

## 🟢 Q289. Why use modern typing?
Keywords: Union, Generic, Protocol, TypedDict
Follow-ups: Benefits?

## 🟢 Q290. Why prefer standard library first?
Keywords: Reliability, Dependencies, Maintenance
Follow-ups: Third-party packages?

## 🟢 Q291. What is `tomllib`?
Keywords: TOML, Configuration, Standard library
Follow-ups: pyproject?

## 🟢 Q292. Modern Python improvements?
Keywords: Type hints, Pattern matching, Dataclasses
Follow-ups: Favorite feature?

## 🟡 Q293. Dataclass vs normal class?
Keywords: Boilerplate, Performance, Simplicity
Follow-ups: Frozen dataclass?

## 🟡 Q294. Dataclass vs NamedTuple?
Keywords: Mutability, Memory, Features
Follow-ups: Use cases?

## 🟡 Q295. Why use Protocols?
Keywords: Structural typing, Interfaces
Follow-ups: Duck typing?

## 🟡 Q296. TypedDict purpose?
Keywords: Typed dictionaries, API models
Follow-ups: Dataclass comparison?

## 🟡 Q297. When use match-case?
Keywords: State machines, Dispatch
Follow-ups: if-elif?

## 🟡 Q298. Why avoid overusing walrus operator?
Keywords: Readability, Simplicity
Follow-ups: Good examples?

## 🟡 Q299. Modern Python interview expectations?
Keywords: Current syntax, Best practices
Follow-ups: Python versions?

## 🔴 Q300. Modernize legacy Python code.
Keywords: Refactoring, Type hints, pathlib
Follow-ups: Migration strategy?

## 🔴 Q301. Type hints in large projects?
Keywords: Maintainability, Tooling
Follow-ups: Adoption strategy?

## 🔴 Q302. Production benefits of modern Python?
Keywords: Readability, Tooling, Refactoring
Follow-ups: Team adoption?

## 🔴 Q303. Modern Python interview pitfalls?
Keywords: Outdated syntax, Legacy habits
Follow-ups: Examples?

## 🔴 Q304. Python 3.10+ important features?
Keywords: Match-case, Better typing
Follow-ups: 3.11 improvements?

## 🔴 Q305. Static analysis workflow?
Keywords: mypy, Ruff, IDE
Follow-ups: CI integration?

## 🔴 Q306. Language evolution strategy?
Keywords: Backward compatibility, Incremental adoption
Follow-ups: Version support?

## 🔴 Q307. Common modernization mistakes?
Keywords: Overengineering, Compatibility
Follow-ups: Migration planning?

## 🔴 Q308. Senior Python coding style?
Keywords: Explicit, Typed, Readable, Maintainable
Follow-ups: Team standards?

</details>

---

# Block 12 — Production Python

<details>
<summary>📚 Contents</summary>

## 🟢 Q309. How should a Python project be structured?
Keywords: Separation of concerns, Modules, Packages
Follow-ups: Example layout?

## 🟢 Q310. Why use virtual environments?
Keywords: Isolation, Dependencies, Reproducibility
Follow-ups: venv vs uv?

## 🟢 Q311. Dependency management tools?
Keywords: pip, uv, Poetry, pip-tools
Follow-ups: Preferred tool?

## 🟢 Q312. Why externalize configuration?
Keywords: Environment variables, Secrets, Config
Follow-ups: Hardcoded values?

## 🟢 Q313. Why use logging instead of print?
Keywords: Levels, Observability, Debugging
Follow-ups: Logging levels?

## 🟢 Q314. Unit test vs Integration test?
Keywords: Scope, Isolation, Reliability
Follow-ups: E2E tests?

## 🟢 Q315. Why automate formatting?
Keywords: Black, Ruff, Consistency
Follow-ups: CI integration?

## 🟢 Q316. How should APIs handle errors?
Keywords: Validation, Status codes, Contracts
Follow-ups: Custom exceptions?

## 🟢 Q317. Why profile before optimizing?
Keywords: Bottlenecks, Measurement, Evidence
Follow-ups: Profiling tools?

## 🟢 Q318. AsyncIO vs Threading?
Keywords: I/O bound, Concurrency
Follow-ups: Multiprocessing?

## 🟢 Q319. Threading vs Multiprocessing?
Keywords: CPU bound, GIL, Parallelism
Follow-ups: Async comparison?

## 🟢 Q320. What is observability?
Keywords: Logs, Metrics, Traces
Follow-ups: Monitoring?

## 🟡 Q321. Logging best practices?
Keywords: Structured logs, Correlation IDs
Follow-ups: Sensitive data?

## 🟡 Q322. Exception strategy in production?
Keywords: Recovery, Logging, Propagation
Follow-ups: Retry?

## 🟡 Q323. Configuration management?
Keywords: Env vars, Secrets, Feature flags
Follow-ups: Vault?

## 🟡 Q324. Testing pyramid?
Keywords: Unit, Integration, E2E
Follow-ups: Trade-offs?

## 🟡 Q325. Dependency pinning?
Keywords: Reproducibility, Lock files
Follow-ups: Security?

## 🟡 Q326. API versioning?
Keywords: Backward compatibility, Evolution
Follow-ups: Deprecation?

## 🟡 Q327. Production debugging strategy?
Keywords: Logs, Metrics, Traces
Follow-ups: Incident response?

## 🟡 Q328. Performance optimization workflow?
Keywords: Measure, Analyze, Optimize
Follow-ups: Premature optimization?

## 🔴 Q329. Design a scalable Python backend.
Keywords: Architecture, Modularity, Testing
Follow-ups: Microservices?

## 🔴 Q330. Production deployment checklist?
Keywords: CI/CD, Testing, Monitoring
Follow-ups: Rollback?

## 🔴 Q331. Python code review checklist?
Keywords: Readability, Security, Performance
Follow-ups: Common review comments?

## 🔴 Q332. Production incident handling?
Keywords: RCA, Monitoring, Alerts
Follow-ups: Postmortem?

## 🔴 Q333. Concurrency decision making?
Keywords: AsyncIO, Threads, Processes
Follow-ups: Real scenarios?

## 🔴 Q334. Production security best practices?
Keywords: Secrets, Validation, Least privilege
Follow-ups: Dependency scanning?

## 🔴 Q335. Common production mistakes?
Keywords: Hardcoded configs, Logging gaps, Missing tests
Follow-ups: Prevention?

## 🔴 Q336. Senior engineering mindset?
Keywords: Simplicity, Maintainability, Reliability, Scalability
Follow-ups: Trade-off discussions?

</details>

---
### Difference between List and Tuple?

Expected Answer

- List → Mutable
- Tuple → Immutable
- Both preserve order
- Both allow duplicate values

Follow-up

When would you prefer Tuple?

---

### Difference between Set and Dictionary?

Expected Answer

Set stores unique values.

Dictionary stores key-value pairs.

---

### Difference between `==` and `is`?

Expected Answer

`==`

Compares values.

`is`

Compares object identity.

---

### Mutable vs Immutable

Examples

Mutable

- List
- Dictionary
- Set

Immutable

- String
- Tuple
- Integer

---

# Intermediate

### Explain shallow copy vs deep copy.

---

### What are generators?

---

### Why use `yield`?

---

### Explain decorators.

---

### Difference between `*args` and `**kwargs`.

---

### What is list comprehension?

---

### Explain lambda functions.

---

### What is GIL?

---

### Explain memory management in Python.

---

# Advanced

### How does Python handle garbage collection?

---

### Explain context managers.

---

### Explain iterators.

---

### Difference between iterable and iterator.

---

### Explain method resolution order (MRO).

---

### Explain monkey patching.

---

### Explain multithreading vs multiprocessing.

---

# Production Questions

These are common for experienced candidates.

- How do you structure large Python projects?
- How do you manage configuration?
- How do you log errors?
- How do you validate API requests?
- How do you write production-quality code?
- How do you improve readability?

---

# Personal Revision List

Priority topics based on diagnostic:

⭐⭐⭐⭐⭐

- Decorators
- Counter
- `is` vs `==`
- `*args`
- `**kwargs`
- Generator
