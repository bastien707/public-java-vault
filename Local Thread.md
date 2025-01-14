- Thread local allows **attaching data to the current thread** context
- This **avoids passing certain data as parameters** through multiple method calls
- The concept *local thread* is not specific to a language and is also called **context**.
### Examples where it's used

- In [[Hibernate]] the [[EntityManager]] is attached to a local thread.

- With [[Spring Security]] the `SecurityContextHolder` is already using a `ThreadLocal` to store the `SecurityContext` and so the `Authentication` the security context is always available to methods in the same thread of execution.

https://www.jmdoudoux.fr/java/dej/chap-threadlocal.htm