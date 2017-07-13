What is Kotlin?
===============
 - Object-oriented
 - Statically typed
 - Garbage-collected
 - Excellent cross-platform support
 - Targets mobile, desktop, and server


Kotlin's Advantages
------------------
- Almost entirely full-stack and broadly cross-platform
  - Usable for both client and server code
  - Any client platform (mobile, desktop, browser)
  - Any server platform (Unix/Linux, Windows)
  - Syntax and semantics will be relatively familiar to users of Java, Ruby, C/C++, Swift, and Objective-C
  - Excellent JVM interoperability
  - Type system allows efficient generated code and compile-time safety checks

- Compilation targets:
  - First-class support for native Android applications
  - Other JVM targets
  - iOS
  - Other native: uses LLVM backend, so it can target (e.g.) native MacOS, Linux, & Windows environments with x86, x64, ARM, and other architectures
  - even Javascript (which could be used to target either browser clients or Node servers)
  - also allows cross-calling between Kotlin and JS

- Also good:
  - Offers full JVM bytecode compatibility (therefore interoperability with any/all existingJVM libraries written in Java, Scala, Groovy, J, others)
  - A high-quality Java-to-Kotlin converter already exists

*In other words*:
    Kotlin is incredibly flexible: almost entirely full-stack, usable for both client and server code, on any client platform (mobile, desktop, browser) and any server platform (Unix/Linux, Windows).

*Note*: Kotlin does not specify UIs; an appropriate tool should be used for that. For instance, when compiling Kotlin to Javascript for a web application, the front-end would still be written in HTML and CSS. A cross-platform UI toolkit like React Native is also an option

Kotlin in the real world
------------------------
- Some prominent users:
  - Amazon Web Services
  - Pinterest
  - Coursera
  - Netflix
  - Uber
  - Square
  - Trello
  - Basecamp (founded by DHH, developer of Rails)

-- Corda, a sophisticated open-source fintech application (used by Goldman Sachs, JP Morgan, Deutsche Bank and others) written entirely in Kotlin



What is Kotlin Like?
====================

- Semantics
   -- Object-oriented
      {code examples}

   -- Garbage-collected (Swift and Objective C use automatic reference counting)
      {explain what GC and ARC are for noobs + lamers}

   -- Strong, static typing disclipline
      {code examples}

   -- Immutable values (val vs var)

   -- Parametric types (generics)
      {code examples}

   -- Nullable types
      {give examples}
      -- combined with parametric types, provides very strong compile-time safety checks

   -- Has support for some functional programming patterns too
      -- Anonymous functions (lambdas)
         {code examples}

      -- Higher-order functions
         {code examples}

      -- Standard library includes many useful higher-order functions that will be familiar to Ruby developers
         -- map
         -- reduce
         -- filter
         -- etc etc

   -- Annotations
      {code examples}

   -- mixins (like Ruby)
      {code examples}

   -- Function types
      -- Since Kotlin is statically typed, in order for higher-order functions to be definable, functions must have types
      -- Function types are parameterized by the types of their input and output
      {code example: show a definition of a higher-order function, pointing out function type parameterization}





   -- Type inference
      {explain Hindley-Milner algorithm}
      {code example}

   -- Coroutines
      {define and give examples}

   -- Reflection
      -- class references
      -- function references
      -- property references
