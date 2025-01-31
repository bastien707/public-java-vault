- Design Pattern
- Way to **add transversal behaviour** without modifying business code.
- e.g `@Transactional`

AOP stands for aspect orientated programming. Essentially, **it is a way for adding behavior to existing code without modifying that code**. AOP is a programming paradigm that aims to increase modularity by allowing the separation of cross-cutting concerns. Spring uses AOP for *Dependency injection* or *managing transactions*.

AOP addresses the problem of _cross-cutting concerns_, which would be any kind of code that is repeated in different methods and can't normally be completely refactored into its own module, like with logging or verification.
## Usage in Spring

Some very common examples of these could be:

1. Transaction Management
2. Logging
3. Exception Handling (especially when you may want to have detailed traces or have some plan of recovering from exceptions)
4. Security aspects
5. Instrumentation

Aspect can be called via annotations or pointcut that will define on what method for example the aspect will be called. Like method ending with `loader`. In this case an aspect will be called but

## Aspect content

**Joinpoint** a specific point in the _**program execution**_, such as the execution of a method or handling of an exception.Where the control flow can arrive via two different paths. (IMO : that's why call joint).

**Advice** The action taken by an aspect at a particular _**joinpoint**_.

**Pointcut** is an expression that matches _**joinpoints**_ and determines whether _**advice**_ should be applied.

**Spring AOP**:
**AspectJ**: An open-source library from the Eclipse project, that allows aspect weaving either at runtime (with proxies), or at compile-time by enriching the bytecode.