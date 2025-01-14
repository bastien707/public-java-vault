- Belongs to Spring
- Ensure a transaction is [[Atomicity|ACID]]
- Transaction is *read-write* by default

Spring creates a proxy, or manipulates the class byte-code, to manage the creation, commit, and rollback of the transaction. In the case of a proxy, Spring ignores _@Transactional_ in private methods or final class.

> [!tip] Annotation on Interface or Implementation 🤔 ?
> The Spring team recommends that you **annotate methods of concrete classes** with the `@Transactional` annotation, rather than relying on annotated methods in interfaces, even if the latter does work for interface-based and target-class proxies as of 5.0. Since Java annotations are not inherited from interfaces, interface-declared annotations are still not recognized by the weaving infrastructure when using AspectJ mode, so the aspect does not get applied. As a consequence, your transaction annotations may be silently ignored: **Your code might appear to "work" until you test a rollback scenario.**
> 


[[Spring Framework 🌱]]

---
## Resources

https://www.marcobehler.com/guides/spring-transaction-management-transactional-in-depth