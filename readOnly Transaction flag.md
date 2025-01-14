- Read-only transactions **cannot modify data in the database**.
- Read-only will improve the **resource consumption** by letting the DBMS optimize such transactions.
	- [[Hibernate]] will skip the [[Dirty checking]] when read only is activated
- This attribute is **only a hint to the provider**, the behavior depends on, in this case, Hibernate.
- Use `@Transactional(readOnly=true)`

---

The main difference between a `read-only` transaction and a normal transaction is **resource consumption**. By default, read-only transactions cannot modify data in the database, unless a TEMPORARY keyword is added.

This makes certain optimizations possible for Hibernate:
- Hibernate doesn't need to add transaction IDs on each query line.
- Hibernate can disable [[Dirty checking|dirty checking]].
- Hibernate can disable the `loaded` lifecycle immediately.
- Hibernate can set its flush method to FlushMode.NEVER.

Other optimizations may also be applied, depending on the database used. Finally, a read-only transaction must be explicitly declared, either directly on the Hibernate session, or by annotating a service method with @Transactional(readOnly=true). It's also worth pointing out that **[[Spring Framework 🌱|Spring]] doesn't apply any optimization of its own; it simply tells the JPA implementation (usually Hibernate) that the transaction is read-only.**