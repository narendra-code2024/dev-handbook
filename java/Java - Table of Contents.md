
---

## Phase 1: Foundations

### 1. Introduction to Java

- What is Java?
- Java Editions
    - Java SE
    - Jakarta EE
    - Java ME
- Java Features
    - Object-Oriented
    - Platform Independent
    - Secured
    - Multithreaded
    - Compiled and Interpreted

### 2. JDK, JRE & JVM

- JDK vs JRE vs JVM
    - Compilation Flow (`.java` → `javac` → `.class` → JVM)
    - "Write Once, Run Anywhere"
- JVM Architecture (high-level)
    - ClassLoader Subsystem
    - Runtime Data Areas
    - Execution Engine
    - Metaspace (replaced PermGen in Java 8)
    - String Constant Pool (in Heap since Java 7)

### 3. Java Basics

- Program Structure
    - Hello World
    - `main` Method Signature
    - Command-Line Arguments
    - Parameters vs Arguments
- Statements, Expressions & Blocks
- Identifiers, Keywords & Naming Conventions
    - Identifier Rules
    - Reserved Keywords
    - Naming Conventions
- Comments
    - Single-line `//`
    - Multi-line `/* */`
    - Javadoc `/** */`
- Packages and Imports
    - `package` Statement
    - `import` Statement
    - Static Imports
    - Java Library Packages

### 4. Variables & Data Types

- Variables
    - Declaration and Initialization
    - Scope and Lifetime (Local, Instance, Static; instance vars auto-init, locals don't) → [12. Classes, Objects & OOP Foundations](<12. Classes, Objects & OOP Foundations.md>)
    - `final` Keyword (basics) → [18. Important Keywords (Deep Dive)](<18. Important Keywords (Deep Dive).md>)
    - `var` Keyword — Local Variable Type Inference (Java 10+)
- Primitive Data Types (Type, Size, Range, Default Value)
    - The 8 primitives: `byte`, `short`, `int`, `long`, `float`, `double`, `char`, `boolean`
- Literals
    - Types: Integer, Character, String, Boolean
    - Integer formats — decimal, hex (`0x`), binary (`0b`), octal (`0`)
    - Type suffixes — `L` (long), `f` (float), `d` (double)
    - Underscore separators (`1_000_000`)
    - Character literals — `'a'`, unicode escapes (`\uXXXX`)
    - Escape sequences — `\n`, `\t`, `\\`, `\'`, `\"`
- Wrapper Classes (one-to-one with primitives; for Collections, nullability, `Number` API) → [Operators — Autoboxing](<05. Operators & Type System.md#Boxing, Unboxing, and Auto-Boxing>), [Numbers — java.lang.Number](<10. Numbers, Math & Random.md#`java.lang.Number` — the numeric root>)
- Non-Primitive Data Types
    - Strings → [9. Strings](<09. Strings.md>)
    - Arrays → [8. Arrays](<08. Arrays.md>)
    - Classes → [12. Classes, Objects & OOP Foundations](<12. Classes, Objects & OOP Foundations.md>)
    - Interfaces → [16. Abstraction & Interfaces](<16. Abstraction & Interfaces.md>)
    - Enums → [21. Enums](<21. Enums.md>)

### 5. Operators & Type System

- Operators: Arithmetic, Unary, Assignment, Relational, Logical, Bitwise, Shift, Ternary, `instanceof`
- Operator Precedence
- Typecasting
    - Widening (Implicit)
    - Narrowing (Explicit)
    - `char` ↔ `int`
    - Compound assignment (implicit narrowing cast)
- Type Promotion
- Boxing, Unboxing, and Auto-Boxing
- Appendix
    - Two's Complement

### 6. Control Statements

- Conditional Statements
    - `if` / `if-else` / `else-if`
    - `switch` Statement
    - `switch` Expressions (Java 14+) — arrow syntax, `yield`, exhaustiveness
    - Pattern Matching in `switch` (Java 21+) — type patterns, guards
- Iterative Statements
    - `for`
    - `while`
    - `do-while`
    - Enhanced `for-each`
- Branching Statements
    - `break`, `continue`, `return`
    - Labeled `break` / `continue`

### 7. Java I/O Basics

- Reading User Input
    - `Scanner` Class
        - `System.in`
        - `next()`, `nextInt()`, `nextLine()`, etc.
        - `nextLine()` Gotcha
        - Parsing Input with Wrapper Classes
    - `Console` Class (`readPassword()` for hidden input)
- Printing Output
    - `PrintStream` Class
    - `System.out.println()`, `print()`, `printf()`
    - Format specifiers → [Numbers — Parsing and Formatting](<10. Numbers, Math & Random.md#Parsing and formatting>)

---

## Phase 2: Common Types & Error Handling

### 8. Arrays

- Declaration & Initialization (Single-Dimensional)
- Multi-Dimensional Arrays
- `Arrays` Utility Class (`java.util.Arrays`)
- `length` vs `length()` vs `size()`
- Array Copying
- Arrays and Generics
- Varargs (Variable Arguments)
- Common Array Patterns

### 9. Strings

- String Basics
- String Immutability
- String Constant Pool
- `String` vs `StringBuilder` vs `StringBuffer`
    - StringBuilder Key Methods
- String Comparison
- Commonly Used String Methods
- String Conversion
- String Concatenation Internals
- Text Blocks (Java 15+)
- Common String Patterns

### 10. Numbers, Math & Random

- `java.lang.Number` — abstract parent + summary of numeric classes
- `java.lang.Math` — abs, min, max, pow, sqrt, log, trig, rounding (`round`/`floor`/`ceil`), `floorDiv`/`floorMod`, overflow-checked arithmetic (`addExact`, `toIntExact`)
- `BigInteger` — arbitrary-precision integers (brief — rarely needed outside crypto/number theory)
- `BigDecimal` — arbitrary-precision decimals, `RoundingMode`, scale
- Parsing and Formatting (`parseInt`, `NumberFormat`, `DecimalFormat`)
- Unsigned Operations (`Integer.toUnsignedLong`, `divideUnsigned`) — brief, for low-level protocols
- Random Number Generation (`Random`, `ThreadLocalRandom`, `SplittableRandom`, `SecureRandom`)

### 11. Exception Handling

- Exception Hierarchy
- Checked vs Unchecked Exceptions
- try-catch-finally
- try-with-resources (Java 7+)
    - AutoCloseable vs Closeable
- throw vs throws
- Custom Exceptions
- Exception Chaining (Wrapping)
- Exception Methods
- Exception Handling with Inheritance
- Best Practices

---

## Phase 3: OOP

### 12. Classes, Objects & OOP Foundations

- Class and Object
- `new` Keyword
- Attributes (Instance Fields)
- Methods (Static and Instance)
- Blocks (Static and Instance)
    - Methods vs Blocks
- `static` Basics
- Variables Scope and Lifetime (Local, Instance, Static)
- Constructors
    - Constructor Basics
    - Default Constructor
    - Advantages of Constructors
    - Constructor vs Instance Methods
    - Constructor vs Instance Blocks
    - Constructor vs Static Blocks
    - No Static Constructor
- `this` Keyword
- Coupling and Cohesion
- Four Pillars of OOP (preview — full coverage in later chapters)
    - Encapsulation → [13. Encapsulation & Access Control](<13. Encapsulation & Access Control.md>)
    - Inheritance → [14. Inheritance & Relationships](<14. Inheritance & Relationships.md>)
    - Polymorphism → [15. Polymorphism](<15. Polymorphism.md>)
    - Abstraction → [16. Abstraction & Interfaces](<16. Abstraction & Interfaces.md>)

### 13. Encapsulation & Access Control

- Access Modifiers (private, default, protected, public)
- Getter and Setter Methods
- Mutable vs Immutable Objects
- Creating an Immutable Class (final class + private final fields + defensive copies)
- Singleton Class (Eager, Bill Pugh, Double-Checked, Enum)

### 14. Inheritance & Relationships

- `extends` Keyword
- `super` Keyword
- Object Creation in Inheritance
- Types of Inheritance
    - Why Java Doesn't Support Multiple Inheritance
- Generalization and Specialization
- IS-A vs HAS-A Relationships
    - Association, Aggregation, Composition

### 15. Polymorphism

- Compile-Time Polymorphism — Method Overloading
    - Overloading Resolution Priority
    - Autoboxing + Widening Interaction
- Runtime Polymorphism — Method Overriding
    - `@Override` Annotation
- Static Method Hiding (Not Overriding)
- Polymorphism in Action
- Overloading vs Overriding

### 16. Abstraction & Interfaces

- Abstract Classes
    - Abstract Methods
    - Class vs Abstract Class
- Interfaces
    - Interface Variables
    - Can an Interface Have a Constructor?
- Concrete Methods in Interfaces (Java 8+)
    - Default Methods
    - Static Methods
    - Private Methods (Java 9+)
- Default Method Conflict (Diamond Problem)
- Multiple Inheritance with Interfaces
- Marker Interfaces (`Serializable`, `Cloneable`, `Remote`)
- Class vs Abstract Class vs Interface
- Abstract Class vs Interface — When to Use

### 17. Inner Classes, Interfaces & Abstract Classes

- Member Inner Classes
    - Non-Static Member Inner Class
    - Static Member Inner Class
- Local Inner Class
- Anonymous Inner Class
    - Anonymous Class vs Lambda
- Inner Interfaces
- Inner Abstract Classes
- When to Use Which Inner Class

### 18. Important Keywords (Deep Dive)

- `final`
    - `final` Variable
    - `final` Method
    - `final` Class
    - `final` Parameter
    - `final` vs Immutability
    - Blank Final Variable
    - `static final` (Constants)
- `this`
    - Method Chaining (Fluent API)
    - Passing Current Object
    - `this` in Inner Class
- `super`
    - Constructor Chaining Up the Hierarchy
    - Accessing Hidden Parent Method
    - Accessing Hidden Parent Field
    - `super` Cannot Be Used
- `static`
    - Static Nested Class
    - Static Import
    - Static Context Rules
    - Static Initialization Order
    - When to Use Static

### 19. Annotations

- What are Annotations
- Built-in Annotations
    - `@Override`
    - `@Deprecated`
    - `@SuppressWarnings`
    - `@FunctionalInterface`
- Meta-Annotations
    - `@Target`
    - `@Retention`
    - `@Inherited`
    - `@Documented`
    - `@Repeatable`
- Custom Annotations
    - Reading Annotations at Runtime

### 20. Object Class

- `toString()`
- `equals()`
    - `==` vs `.equals()`
- `hashCode()`
- Contract Between `equals()` and `hashCode()`
    - Why `HashSet`/`HashMap` Depend on It
    - What Breaks if Not Overridden

### 21. Enums

- Declaration & Basics
- Built-in methods (`values()`, `valueOf()`, `name()`, `ordinal()`)
- Enums with Fields, Constructors, and Methods
- Abstract Methods per Constant (Strategy Pattern)
- Implementing Interfaces
- Enums in `switch` (including pattern matching in Java 21+)
- `EnumSet` and `EnumMap` (high-performance collections)
- Enum as Singleton (Effective Java pattern)
- Real-World Patterns (state, roles/permissions, feature flags, log levels)

---

## Phase 4: Collections & Generics

### 22. Generics

- Generic Class
- Generic Method
- Bounded Type Parameters (upper bound `extends`, multiple bounds with `&`)
- Wildcards (`?`, `? extends T`, `? super T`)
    - PECS — Producer Extends, Consumer Super
- Wildcards vs Bounded Type Parameters
- Type Erasure
- Generic Interface
- Generic Constructor

### 23. Java Collection Framework

- Hierarchy Overview
- List (`ArrayList`, `LinkedList`, `Vector`, `Stack`)
- Set (`HashSet`, `LinkedHashSet`, `TreeSet`)
- Queue & Deque (`PriorityQueue`, `ArrayDeque`)
- Map (`HashMap`, `LinkedHashMap`, `TreeMap`, `Hashtable`, `ConcurrentHashMap`)
    - `HashMap` Internal Working
- Iteration Techniques (`Iterator`, for-each, `forEach()`, `ListIterator`)
- `Collections` Utility Class (sort, reverse, shuffle, fill, binarySearch)
- `Comparable` vs `Comparator`
- Arrays ↔ Collections Conversions
- Bulk Operations (`addAll`, `removeAll`, `retainAll`, `removeIf`)
- Fail-Fast vs Fail-Safe Iterators
- Thread-Safe Collections (`ConcurrentHashMap`, `CopyOnWriteArrayList`, `BlockingQueue`)
- Big-O Cheat Sheet
- Quick Decision Guide

---

## Phase 5: Modern Java (Java 8+)

### 24. Functional Programming (Java 8+)

- Functional Interfaces
    - Built-in (`Predicate`, `Function`, `Consumer`, `Supplier`, Bi/Unary/Binary variants)
    - Chaining Functional Interfaces
    - Primitive Specialized Functional Interfaces (`IntPredicate`, `LongFunction`, etc.)
- Lambda Expressions
- Method References (static, instance-specific, instance-any, constructor)
- Effectively Final Variables

### 25. Streams API (Java 8+)

- Creating Streams (`stream()`, `of()`, `generate()`, `iterate()`)
- Intermediate Operations (`filter`, `map`, `flatMap`, `sorted`, `distinct`, `limit`, `skip`)
- Terminal Operations (`collect`, `forEach`, `reduce`, `count`, `findFirst`, `anyMatch`)
- Optional (Companion to Streams)
- Primitive Streams (`IntStream`, `LongStream`, `DoubleStream`)
- Parallel Streams
- Common Stream Patterns
- Stream Pipeline Order Matters
- Short-Circuiting Operations
- Stateless vs Stateful Operations
- Stream Best Practices

---

## Phase 6: Concurrency, I/O & Networking

### 26. Multithreading & Concurrency

- Creating Threads (`Thread`, `Runnable`, `Callable`)
- Thread Lifecycle (NEW, RUNNABLE, BLOCKED, WAITING, TIMED_WAITING, TERMINATED)
- Essential Thread Methods (`start`, `sleep`, `join`, `interrupt`, `yield`)
    - Daemon vs User Threads
- Synchronization — `synchronized` Keyword
- `volatile` Keyword
- `wait()`, `notify()`, `notifyAll()`
- Locks (`ReentrantLock`, `ReadWriteLock`)
- Atomic Classes (`AtomicInteger`, `LongAdder`, `LongAccumulator`)
- Synchronizers (`CountDownLatch`, `CyclicBarrier`, `Semaphore`)
- ExecutorService (Thread Pools)
    - `ThreadPoolExecutor` (production-grade)
- `CompletableFuture` (Java 8+)
- Virtual Threads (Java 21+)
- Concurrent Collections
- Common Concurrency Problems (Deadlock, Livelock, Starvation, Race Condition)

### 27. File Handling

- I/O Streams (byte vs character)
- Reading & Writing Files
    - Character Streams (`FileReader`, `FileWriter`, `PrintWriter`)
    - Byte Streams (`FileInputStream`, `FileOutputStream`)
- Buffered Streams (`BufferedReader`, `BufferedWriter`)
- `java.nio.file` (Modern File API — Java 7+)
    - `Path` and `Paths`
    - `Files` Utility Class (`readString`, `readAllLines`, `write`, `copy`, `move`, `delete`)
    - Stream-based File Reading (`Files.lines`, `Files.walk`)
    - Modern Buffered Reading/Writing (`Files.newBufferedReader`, `Files.newBufferedWriter`)
- `File` class (Legacy — `java.io`)
- `try-with-resources` for I/O
- `InputStreamReader` / `OutputStreamWriter` (Bridge)
- Common I/O Patterns
- `java.io.File` vs `java.nio.file`

### 28. Serialization

- How to Serialize (`Serializable`, `ObjectOutputStream`, `ObjectInputStream`)
- `serialVersionUID`
- `transient` Keyword (excluding fields from serialization)
- `static` Fields and Serialization
- Inheritance and Serialization
- Custom Serialization (`writeObject()`, `readObject()`)
- `Externalizable` Interface
- Serialization and Singleton (`readResolve`, enum singleton)
- Modern Alternatives (JSON, Protobuf, Avro, Kryo)

### 29. Java Networking

- `java.net` Package Overview
- `InetAddress`
- TCP Sockets (`Socket`, `ServerSocket`)
- UDP Sockets (`DatagramSocket`, `DatagramPacket`)
- `URL` and `HttpURLConnection` (legacy)
- Modern HTTP Client (Java 11+) — `java.net.http.HttpClient`

---

## Phase 7: Reference & Deep Dives

### 30. Java Modern Features (10–21+)

> Features covered elsewhere are linked, not duplicated here.

- **Java 5** (type safety)
    - Autoboxing/Unboxing → [05. Operators & Type System](<05. Operators & Type System.md>)
    - Enhanced `for-each` Loop → [06. Control Statements](<06. Control Statements.md>)
    - Generics → [22. Generics](<22. Generics.md>)
- **Java 8** (functional programming)
    - Functional Interfaces, Lambda Expressions → [24. Functional Programming (Java 8+)](<24. Functional Programming (Java 8+).md>)
    - Streams API, `Optional` → [25. Streams API (Java 8+)](<25. Streams API (Java 8+).md>)
- **Java 10** — `var` Keyword
- **Java 14** — Switch Expressions
- **Java 15** — Text Blocks
- **Java 16** — Records, Pattern Matching for `instanceof`
- **Java 17** — Sealed Classes
- **Java 21** — Virtual Threads, Structured Concurrency (preview)

### 31. JVM Architecture & Memory Model (Deep Dive)

> Advanced reference — revisit after Phase 3 (OOP). Basics → [02. JDK, JRE & JVM](<02. JDK, JRE & JVM.md>).

- ClassLoader Subsystem
    - Loading (Bootstrap, Extension/Platform, Application/System)
    - Linking (Verification, Preparation, Resolution)
    - Initialization
    - Parent-first delegation model
- Runtime Data Areas (Memory)
    - Method Area / Metaspace (class metadata, static vars)
    - Heap
        - Young Generation (Eden, Survivor S0/S1)
        - Old Generation
        - String Constant Pool (in Heap since Java 7)
    - Stack (per thread — local vars, frames)
    - PC Register (per thread)
    - Native Method Stack (per thread)
- Execution Engine
    - Interpreter vs JIT
    - Tiered Compilation (C1 + C2)
    - Garbage Collector
        - Reachability analysis from GC Roots
        - GC types: Serial, Parallel, G1 (default Java 9+), ZGC (Java 15+)
        - Minor GC vs Major/Full GC
        - Stop-The-World pauses
        - `System.gc()` is a hint, `finalize()` deprecated
- Object Creation Flow (class load → heap alloc → default init → constructor → stack reference)
- String Memory (literal pool vs `new String(...)`)
- JVM Flags (`-Xms`, `-Xmx`, `-Xss`, GC selection, heap dump on OOM)
- Gotchas
    - Stack vs Heap confusion
    - PermGen vs Metaspace
    - `OutOfMemoryError` variants (heap, metaspace, native thread, GC overhead)
    - JIT warmup
    - Memory leak causes
