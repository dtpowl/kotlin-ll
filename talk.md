Why Kotlin?
===========

- What is Kotlin?
 -- Kotlin is an object-oriented, statically typed, garbage-collected language with excellent cross-platform support, targeting mobile, desktop, and server

- Why Kotlin?
  -- Almost entirely full-stack and broadly cross-platform
     -- Usable for both client and server code, on any client platform (mobile, desktop, browser) and any server platform (Unix/Linux, Windows)
  -- Syntax and semantics will be relatively familiar to users of Ruby, Python, Java, C/C++, Swift, and Objective-C
  -- Excellent JVM interoperability
  -- Type system allows efficient generated code and compile-time

- Compilation targets:
  -- JVM (including first-class support for native Android apps)
  -- iOS
  -- Other native: uses LLVM backend, so it can target (e.g.) native MacOS, Linux, & Windows environments with x86, x64, ARM, and other architectures
  -- even Javascript (which could be used to target either browser clients or Node servers)
     -- also allows cross-calling between Kotlin and JS

  -- Also:
     -- Offers full JVM bytecode compatibility (therefore interoperability with any/all existingJVM libraries written in Java, Scala, Groovy, J, others)
     -- A high-quality Java-to-Kotlin converter already exists

In other words: Kotlin is incredibly flexible: almost entirely full-stack, usable for both client and server code, on any client platform (mobile, desktop, browser) and any server platform (Unix/Linux, Windows)
   -- one deficiency: you can't really build UIs in Kotlin. UIs could be built with React or Elm (or with native tools)

- Kotlin in the real world
  -- Some prominent users
    -- Amazon Web Services
    -- Pinterest
    -- Coursera
    -- Netflix
    -- Uber
    -- Square
    -- Trello
    -- Basecamp (founded by DHH, developer of Rails)

    -- Corda, a sophisticated open-source fintech application (used by Goldman Sachs, JP Morgan, Deutsche Bank and others) written entirely in Kotlin
       {explain why Kotlin's language features make it useful for financial technology applications}


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


- Cool syntax bits and pieces
   -- ?. (safe navigation operator)
      {code example]

   -- ?: (coalescing operator)
      {code example}

   -- string interpolation
      {code example, make comparison with Java}

   -- destructuring
      {code example}

   -- anonymous functions (already mentioned above)
