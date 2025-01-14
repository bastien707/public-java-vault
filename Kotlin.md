Both Kotlin and Java compile to bytecode that runs on the JVM, which means they have similar performance characteristics.
### Null safety

In Java, it's possible to have `null` values assigned to a variable, which can lead to null pointer exceptions at runtime. **Kotlin, requires you to explicitly define whether a variable can be null or not**. This makes it easier to avoid null pointer exceptions during runtime.

### More concise syntax

Kotlin has a more concise syntax so that require less code than Java to write the same thing:
create a singleton:
```kotlin
object SomeSingleton
```

```java
public class Singleton {
 
    private static Singleton instance = null;
 
    private Singleton(){
    }
 
    private synchronized static void createInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
    }
 
    public static Singleton getInstance() {
        if (instance == null) createInstance();
        return instance;
    }

}
```

It avoid a lot of boilerplate code with getter, setter for example.
### Why do people still use java ?

For its retro-compatibility.

## Some Java issues addressed in Kotlin﻿

Kotlin fixes a series of issues that Java suffers from:
- Null references are controlled by the type system.
- No raw types
- Arrays in Kotlin are invariant
- Kotlin has proper function types, as opposed to Java's SAM-conversions
- Use-site variance without wildcards
- Kotlin does not have checked exceptions
- Separate interfaces for read-only and mutable collections

