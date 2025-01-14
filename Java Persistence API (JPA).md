**The Java Persistence API (JPA) is a specification that defines how to persist data in Java applications**.

It's a **specification** meaning it provides a **set of guidelines and rules for how to interact with databases** in Java applications.

**Java Persistence API (JPA) is a Java API for Object-Relational Mapping (ORM)**

JPA-based applications still use JDBC under the hood. Therefore, when we utilize JPA, our code is actually using the JDBC APIs for all database interactions. In other words, JPA serves as a layer of abstraction that hides the low-level JDBC calls from the developer, making database programming considerably easier.

JPA was originally intended for use with relational databases, some JPA implementations have been extended for use with NoSQL datastores such as EclipseLink.

## Popular implementations

- **[[EclipseLink]]:** The reference implementation for JPA 3. It supports both relational and some NoSQL databases.
- **[[Hibernate]]:** One of the most popular JPA implementations. Although it started as an ORM tool, it fully supports the JPA specification.

### JPA is not an ORM

JPA and ORM are related but distinct concepts.

- **JPA:** Handles the querying and management of data.
- **ORM:** Focuses on the mapping between Java objects and database tables.


One of the main interface it defines is the [[EntityManager]] or EntityManagerFactory.

[[Spring Data JPA]]
