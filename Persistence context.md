A persistence context **handles a set of entities which hold data to be persisted in some persistence store** (e.g. a database). In particular, the context is **aware of the different states** an entity can have (e.g. managed, detached) in relation to both the context and the underlying persistence store.[^1] It is associated with an `EntityManager` in JPA or a `Session` in Hibernate.

It is essentially a cache of entity instances that are managed by the `EntityManager`.

- A Cache is a copy of data, copy meaning pulled from but living outside the database.
- Flushing a Cache is the act of putting modified data back into the database.
- A PersistenceContext is essentially a Cache. It also tends to have it's own non-shared database connection.
- An EntityManager represents a PersistenceContext (and therefore a Cache)
- An EntityManagerFactory creates an EntityManager (and therefore a PersistenceContext/Cache)[^2]

**First-Level Cache**: The persistence context serves as the first-level cache. It caches the entities so that multiple retrievals of the same entity within the same transaction do not require repeated database access.

The persistence context is tightly coupled with **transactions**. When a transaction is started, a persistence context is bound to that transaction. Changes made to entities within the persistence context are not immediately pushed to the database. Instead, they are synchronized with the database when the transaction is committed.

We can think of the persistence context as a service that remembers all the modifications and state changes we made to the data within a particular _unit of work_.

[^1]: https://stackoverflow.com/questions/19930152/what-is-persistence-context
[^2]: https://tomee.apache.org/jpa-concepts.html