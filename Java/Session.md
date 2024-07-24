The `Session` is a Hibernate-specific interface that extends the JPA `EntityManager` interface. It provides additional methods and functionality specific to Hibernate, such as more control over the session lifecycle, custom queries, and batch processing.

JPA is a standard, whereas session is not.

So if you're using entityManager and want to change your JPA implementation, you can easily do so. But with SessionFactory it's more difficult. Session manager is less portable.