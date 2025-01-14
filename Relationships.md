Relationships in JPA (Java Persistence API) are used to define associations between entities in a relational database. JPA uses annotations to describe these relationships, and specifies how the associated data is to be retrieved. **Foreign keys are used to define relationships between entities.** 

## 4 types of relation

### One-to-One (`@OneToOne`)

This relationship means that an instance of one entity is associated with a single instance of another entity.

By default it use **EAGER** fetch.

### Many-to-One (`@ManyToOne`)

This relationship means that several instances of one entity are associated with a single instance of another entity.

By default it use **EAGER** fetch.

### One-to-Many (`@OneToMany`)

This relationship means that an instance of one entity is associated with several instances of another entity.

By default it use **LAZY** fetch.

### Many-to-Many (`@ManyToMany`)

This relationship means that several instances of one entity are associated with a single instance of another entity.

By default it use **LAZY** fetch.
