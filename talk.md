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

- Corda, a sophisticated open-source fintech application (used by Goldman Sachs, JP Morgan, Deutsche Bank and others) written entirely in Kotlin



What is Kotlin Like?
====================

- Semantics
   - Object-oriented
   - Garbage-collected (Swift and Objective C use automatic reference counting)
   - Strong, static typing disclipline
   - Immutable values
   - Parametric types (generics)
   - Nullable types
      - combined with parametric types, provides very strong compile-time safety checks

   - Has support for some functional programming patterns too
      - Anonymous functions (lambdas)
      - Higher-order functions
      - Standard library includes many useful higher-order functions that will be familiar to Ruby developers
         - map
         - reduce
         - filter
         - etc etc

   - Function types
      - Since Kotlin is statically typed, in order for higher-order functions to be definable, functions must have types
      - Function types are parameterized by the types of their input and output


```kotlin
open class Person constructor(val firstName: String, val lastName: String) {
  init {
    println("Person constructed with name ${firstName} ${lastName}")
  }

  constructor(name: String) : this(name.split(" ")[0], name.split(" ")[1]) { }

  fun fullName(): String {
    return "${firstName} ${lastName}"
  }
}

val person1 = Person("Robert", "Fogarty")
val person2 = Person("Jason Bishop")
```

```kotlin
class Employee constructor(firstName: String, lastName: String, var employer: Person) : Person(firstName, lastName) {
  constructor(name: String, employer: Person) : this(name.split(" ")[0], name.split(" ")[1], employer) { }
}

val jane = Person("Jane Doe");
val john = Employee("John", "Deer", jane);
```

```kotlin
var a: String = "abc"
a = null // compilation error

var b: String? = "abc"
b = null // ok

val l = a.length // ok
val l = b.length // error: variable 'b' might be null

val l: Int  = if (b != null) b.length else -1 // explicit null checks
val l: Int? = b?.length // "safe call" operator
val l: Int = b?.length ?: -1 // retains semantics of first case
```

```kotlin
class MySet<T>(vararg initial: T) {
  val list: MutableList<T> = mutableListOf<T>(*initial)
  var size = 0

  init {
    size = list.size
  }

  fun includes(e: T) : Boolean {
    for (x in list) {
      if (x == e) {
        return true
      }
    }

    return false
  }

  fun add(e: T) : Boolean {
    if (!this.includes(e)) {
      list.add(e)
      size += 1
      return true

    } else {
      return false
    }
  }

  fun remove(e: T) : Boolean {
    if (this.includes(e)) {
      list.remove(e)
      size -= 1
      return true

    } else {
      return false
    }
  }
}
```

```kotlin
fun makeHyperoperation(order: Int) : (Int, Int) -> Int {
  if (order == 1) {
    return { a: Int, b: Int -> a + b }
  } else {
    return fun (a: Int, b: Int) : Int {
      var r = a;
      repeat(b - 1, {
        r = makeHyperoperation(order - 1)(r, a)
      })
      return r
    }
  }
}

val add = makeHyperoperation(1);
val mult = makeHyperoperation(2);
val pow = makeHyperoperation(3);
val tetrate = makeHyperoperation(4);

add(3, 4);       // 7
mult(3, 4);      // 12
pow(3, 4);       // 81
tetrate(3, 4);   // ??
```
