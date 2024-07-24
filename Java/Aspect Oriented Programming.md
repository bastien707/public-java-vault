AOP stands for aspect orientated programming. Essentially, **it is a way for adding behavior to existing code without modifying that code**. AOP is a programming paradigm that aims to increase modularity by allowing the separation of cross-cutting concerns. Spring uses AOP for *Dependency injection* or *managing transactions*.

AOP addresses the problem of _cross-cutting concerns_, which would be any kind of code that is repeated in different methods and can't normally be completely refactored into its own module, like with logging or verification.
## Usage in Spring

Some very common examples of these could be:

1. Transaction Management
2. Logging
3. Exception Handling (especially when you may want to have detailed traces or have some plan of recovering from exceptions)
4. Security aspects
5. Instrumentation

## Aspect

An aspect is a modularization of a concern that cuts across multiple classes.
## Join Points

**A _Joinpoint_ is a point during the execution of a program, such as the execution of a method or the handling of an exception.**

In Spring AOP, a _JoinPoint_ always represents a method execution.
## Pointcut

You can think of a pointcut as matching the execution of methods on Spring beans.

**Spring AOP**: A Spring based solution that leverages dynamic **proxies** to create the aspects.
**AspectJ**: An open-source library from the Eclipse project, that allows aspect weaving either at runtime (with proxies), or at compile-time by enriching the bytecode.