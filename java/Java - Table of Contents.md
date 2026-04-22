
---

## Phase 1: Foundations

---

### 1. Introduction to Java

- What is Java?
- Java Editions (Java SE, Java EE, Java ME)
- Java Features: Simple, Object-Oriented, Platform Independent, Secured, Robust, Multithreaded, Compiled and Interpreted
- Java as a Software/Hardware Platform
- Compilation and Interpretation: How it happens in Java (`javac` and `java` commands)

### 2. JDK, JRE, JVM & Memory Model

- JDK vs JRE vs JVM
- JVM Architecture
    - ClassLoader Subsystem
        - Loading (Bootstrap, Extension, Application ClassLoader)
        - Linking (Verification, Preparation, Resolution)
        - Initialization
    - Runtime Data Areas
        - Method Area (Class metadata, static variables)
            - Metaspace (Java 8+ implementation of Method Area)
        - Heap (Instance variables and objects live here)
        - Stack (Local variables and method calls live here)
        - PC Register
        - Native Method Stack
    - Execution Engine
        - Interpreter
        - JIT Compiler
        - Garbage Collector
    - Java Native Interface (JNI)
- Object Creation & Memory in Action
    - Object Creation Flow: Class Loading → Memory Allocation in Heap → Default Initialization → Constructor Execution
    - Stack vs Heap: Example with Method Calls

> **Deep JVM internals** (ClassLoader phases, GC algorithms, JNI) are advanced topics — revisit after Phase 3 (OOP) once the rest of the language is grounded.

### 3. Java Basics

- Java Naming Conventions (Packages, Classes, Interfaces, Variables, Methods, Keywords)
- Java Library Packages (Core and Advanced Packages)
- `import` Statement
- `package` Statement
- `main` Method Signature (`public static void main(String[] args)`)
- Parameters vs Arguments
- Command-Line Arguments
    - How to pass them while executing code

### 4. Data Types & Variables

- Primitive Data Types: Type, Size, Description, Default Value, Wrapper Class
- Non-Primitive Data Types: Strings, Arrays, Classes, Interfaces, Enums
- Enums
    - Enum Constants
    - Enums with Constructors and Methods
    - Enums in `switch` Statements

### 5. Operators & Type System

- Operators: Arithmetic, Unary, Assignment, Relational, Logical, Bitwise, Shift, Ternary, `instanceof`
- Typecasting
    - Widening (Implicit)
    - Narrowing (Explicit)
- Type Promotion
- Boxing, Auto-Boxing, and Unboxing

### 6. Control Statements

- Conditional Statements (`if`, `if-else`, `else-if`, `switch`)
- Iterative Statements (`for`, `while`, `do-while`, enhanced `for-each`)
- Branching (Jumping) Statements (`break`, `continue`, `return`)

### 7. Java I/O Basics

- Reading User Input: Scanner Class
    - What is `System.in`?
    - Methods: `next()`, `nextInt()`, `nextByte()`, `nextLine()`, etc.
    - Gotcha with `nextLine()`
    - Why Parse Methods on Wrapper Classes
- Printing Output: PrintStream Class
    - `System.out.println()`, `System.out.print()`, `System.out.printf()`

---

## Phase 2: Common Types & Error Handling

---

### 8. Arrays

- Single-Dimensional Arrays
- Multi-Dimensional Arrays
- Commonly Used Array Methods
- `length` vs `length()`

### 9. Strings

- Different String Classes and Properties
- Immutability Behavior
    - `String` Immutability: Common Confusions and Gotchas
- String Constant Pool
    - Interning (`intern()` Method)
- Commonly Used String Methods
- String Comparison
- `String` vs `StringBuffer` vs `StringBuilder`

### 10. Exception Handling

- Exception Hierarchy
    - Throwable
        - Error
        - Exception
- Define Exception Handling: `try`, `catch`, `finally`
- Checked vs Unchecked Exceptions
    - Built-in Unchecked Exceptions
    - Built-in Checked Exceptions
- `getMessage()` and `printStackTrace()` Methods
- Handling Multiple Exceptions
    - Multiple `catch` Blocks
    - Single `catch` for Multiple Exceptions (Java 7+)
- User-Defined Exceptions (preview — class + inheritance syntax covered in Phase 3)
    - Custom Checked Exceptions
    - Custom Unchecked Exceptions
- Enhanced Try-With-Resources Statement
- Common Exceptions (`NullPointerException`, `ArrayIndexOutOfBoundsException`, `IOException`, `SQLException`, etc.)
- Exception Rethrowing
- Exception Propagation
- `throw` vs `throws` Keyword
- Exception Best Practices
    - Avoid Catching Generic `Exception`
    - Always Handle Resources (or use Try-With-Resources)
    - Prefer Custom Exceptions for Business Logic

---

## Phase 3: OOP

---

### 11. Classes, Objects & OOP Foundations

- Core of OOP
    - Classes
    - Methods
    - Attributes
- Four Pillars of OOP
    - Encapsulation
    - Inheritance
    - Polymorphism
    - Abstraction
- Class and Object
- `new` Keyword (Object Creation)
- Methods (Static and Instance)
- Blocks (Static and Instance)
    - Difference Between Methods and Blocks
- `static` Basics (Static Variables, Methods, Blocks)
- Variable Types by Scope and Lifetime (Local, Instance, Static)
- Constructors
    - Constructor Basics
    - Default Constructor
    - Advantages of Constructors
    - Constructor vs Instance Methods
    - Constructor vs Instance Blocks
    - Constructor vs Static Blocks
    - No Concept of Static Constructor
- `this` Keyword
- Coupling and Cohesion

### 12. Encapsulation & Access Control

- Access Modifiers (Private, Default, Protected, Public)
- Private Variables, Methods, Constructors, Classes
- Getter and Setter Methods
- Mutable and Immutable Objects
- Immutable Class
- Singleton Class

### 13. Inheritance & Relationships

- IS-A Relationship
- `extends` Keyword
- `super` Keyword (Parent Constructor Calls, Parent Method/Variable Access)
- Types: Single, Multilevel, Hierarchical, Hybrid
- Why Java Doesn't Support Multiple Inheritance (with classes)
- Generalization and Specialization
- HAS-A Relationship
    - Association
        - Aggregation (Weak Association)
        - Composition (Strong Association)

### 14. Polymorphism

- Compile-Time Polymorphism (Static/Early Binding)
    - Method Overloading: Instance, Static, and Constructor Overloading
        - Can Overload `main` Method
- Runtime Polymorphism (Dynamic/Late Binding)
    - Method Overriding: Only Instance Methods Can Be Overridden
    - Static Method Hiding (Not Overriding)

### 15. Abstraction & Interfaces

- Abstract Classes
    - Rules and Roles
    - Abstract Methods: Instance or Static?
    - Difference Between Class and Abstract Class
- Interfaces
    - Rules, `implements` Keyword
    - Methods are Public by Default (can also be default, static, or private in Java 8+)
    - Interface Variables: Static or Instance?
    - Can an Interface Have a Constructor?
    - Concrete Methods in Interfaces (Java 8+)
        - Default Methods
        - Static Methods
        - Private Methods (Java 9+)
- Marker Interfaces (`Serializable`, `Cloneable`, `Remote`)
- Comparison: Class vs Abstract Class vs Interface
- Multiple Inheritance with Interfaces

### 16. Inner Classes, Interfaces & Abstract Classes

- Inner Classes
    - Member Inner Classes
        - Static Member Inner Class
        - Non-Static Member Inner Class
    - Local Inner Classes
    - Anonymous Inner Classes
- Inner Interfaces
- Inner Abstract Classes

### 17. Important Keywords (Deep Dive)

- `final`: Usage with Variables, Methods, Classes and Its Impact
    - `final` vs Immutability
- `this` (Advanced Usage: chaining, returning current instance)
- `super` (Advanced Usage: constructor chaining, method access in inheritance hierarchy)
- `static` (Deep Dive: Static Nested Classes, Static Imports, etc.)

### 18. Annotations

- What are Annotations?
- Built-in Annotations
    - `@Override`
    - `@Deprecated`
    - `@SuppressWarnings`
    - `@FunctionalInterface`
- Meta-Annotations (`@Target`, `@Retention`, `@Inherited`, `@Documented`)
- Custom Annotations

### 19. Object Class & Core Methods

- `toString()`
    - `System.out.println()` internally uses `toString()`
- `equals()` Method
    - `==` vs `.equals()`
- `hashCode()` Method
- Contract Between `equals()` and `hashCode()`
    - Why `HashSet`/`HashMap` Depend on It
    - What Breaks if Not Overridden

---

## Phase 4: Collections & Generics

---

### 20. Generics

- What are Generics?
- How Generics Work
- Generic Classes and Generic Methods
- Bounded Type Parameters (`extends`, `super`)
- Wildcards (`?`, `? extends T`, `? super T`)
- Type Erasure
- Power of Generics and When They're Useful

### 21. Java Collection Framework

- Collection Framework Hierarchy
    - List, Queue, Set, Map Interfaces and Implementations
- `Collection` vs `Collections`
- `Iterable` and `Iterator`
- Commonly Used Methods with Syntax
- Internal Workings
    - `ArrayList` Resizing
    - `HashMap`: Buckets, Hashing, Collisions, Load Factor
        - `HashMap` Null Key Behavior
        - Java 8: LinkedList → Red-Black Tree Conversion (Treeification)
- `Comparable` vs `Comparator` Interfaces
    - `Comparable`: Natural Ordering (inside the class)
    - `Comparator`: Custom Sorting (external)
    - `compareTo()` Method
- `equals()` and `hashCode()` in Collections (see Section 19 for contract details)

---

## Phase 5: Modern Java (Java 8+)

---

### 22. Functional Programming (Java 8+)

- Functional Interfaces
- Lambda Expressions
- Method References
    - Reference to Constructor
    - Reference to Instance Method
    - Reference to Static Method
- Consumer, Predicate, Function, Supplier Interfaces

### 23. Streams API (Java 8+)

- What are Streams? (Stream vs Collection)
- Lazy Evaluation: Intermediate Operations are Lazy, Terminal Triggers Execution
- Creating Streams (`stream()`, `of()`, `generate()`, `iterate()`)
- Intermediate Operations: `map()`, `filter()`, `sorted()`, `distinct()`, `limit()`, `flatMap()`
- Terminal Operations: `collect()`, `reduce()`, `forEach()`, `count()`, `findFirst()`, `anyMatch()`
- Collectors (`toList()`, `toSet()`, `toMap()`, `groupingBy()`, `joining()`)
- Parallel Streams
    - When to Use and When to Avoid

---

## Phase 6: Concurrency, I/O & Networking

---

### 24. Multithreading & Concurrency

- What is Multithreading? (Process vs Thread)
- Creating Threads
    - Extending `Thread` Class
    - Implementing `Runnable` Interface
    - `Thread` vs `Runnable`: When to Use Which
- Thread Lifecycle (New → Runnable → Running → Blocked/Waiting → Terminated)
- Thread Methods: `start()`, `run()`, `sleep()`, `join()`, `yield()`, `interrupt()`
- Thread Priority
- `synchronized` Keyword
    - Method-Level vs Block-Level Synchronization
    - Object-Level Locking vs Class-Level Locking
- `volatile` Keyword
- Common Problems
    - Race Condition
    - Deadlock
    - Starvation
- Inter-Thread Communication: `wait()`, `notify()`, `notifyAll()`
- Concurrency vs Parallelism
- Synchronous vs Asynchronous Execution
- ExecutorService and Thread Pools
- Callable and Future
- `CompletableFuture` (Asynchronous Programming)

### 25. File Handling

- File Class and Common Methods
- Byte Streams: `FileInputStream`, `FileOutputStream`
- Character Streams: `FileReader`, `FileWriter`
- Buffered Streams: `BufferedReader`, `BufferedWriter`
- Reading and Writing Files (line by line, entire file)
- Try-With-Resources for File Handling
- NIO (New I/O)
    - `Path` and `Paths`
    - `Files` Utility Class (`readAllLines()`, `write()`, `copy()`, `move()`, `delete()`)

### 26. Serialization

- What is Serialization and Deserialization?
- `Serializable` Interface
- `ObjectOutputStream` and `ObjectInputStream`
- `serialVersionUID`: What and Why
- `transient` Keyword (Excluding Fields from Serialization)
- Custom Serialization (`writeObject()`, `readObject()`)

### 27. Java Networking

- `java.net` Package Overview
- `InetAddress` Class
- Sockets: `Socket` and `ServerSocket` (TCP)
- `DatagramSocket` and `DatagramPacket` (UDP)
- `URL` and `HttpURLConnection`
- Client-Server Communication (Basic Example)

---

## Phase 7: Reference / Version Cheat Sheet

---

### 28. Java Modern Features (Version-wise)

- **Java 5 – Type Safety & Convenience**
    - Autoboxing/Unboxing (covered in Section 5)
    - Enhanced `for-each` Loop (covered in Section 6)
    - Generics (covered in Section 20)
- **Java 8 – Cleaner & Expressive Code**
    - Functional Interfaces (covered in Section 22)
    - Lambda Expressions (covered in Section 22)
    - Streams API (covered in Section 23)
    - `Optional` Class
- **Java 10**
    - `var` Keyword (Local Variable Type Inference)
- **Java 11 – Production Stability**
    - LTS Release: What It Means
    - HTTP Client (`java.net.http`)
    - Garbage Collection Improvements (G1 GC as Default)
- **Java 14**
    - Switch Expressions
- **Java 15**
    - Text Blocks
- **Java 16**
    - Records
    - Pattern Matching (`instanceof`)
- **Java 17 – Less Boilerplate**
    - Sealed Classes
- **Java 21 / Java 25 – Scaling Better**
    - Virtual Threads (Project Loom)
    - Structured Concurrency
    - Performance Improvements
