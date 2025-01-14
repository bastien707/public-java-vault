`EntityManager` is a **JPA interface** that lets you interact with the **persistence context**, manage the lifecycle of your entities, it handles crud operations and transactions. An EntityManager is typically created by an `EntityManagerFactory` **Each EntityManager instance is associated with a [[Persistence context|persistence context]] and is meant to be used for a single unit of work** (e.g., a transaction).

The _EntityManager_ is the interface that lets us interact with the persistence context. Whenever we use the _EntityManager_, we are actually interacting with the persistence context.

The EntityManager is created and managed by Spring. It is automatically closed when the transaction ends.

The entitymanager role is also the L1 cache.