### Primary key

In Hibernate, the primary key of an entity is defined using the `@Id` annotation. Hibernate provides several strategies to generate primary keys automatically, including:

`@GeneratedValue`: Specifies how the primary key value should be generated. Common strategies include AUTO, IDENTITY, SEQUENCE, and TABLE.

• **AUTO**: Hibernate selects the generation strategy based on the database dialect.
• **IDENTITY**: Uses an auto-increment column in the database.
• **SEQUENCE**: Uses a database sequence to generate unique values.
• **TABLE**: Uses a table to maintain and generate primary key values.

### Foreign key

Foreign keys are used to define relationships between entities. Hibernate uses annotations like @ManyToOne, @OneToMany, @OneToOne, and @ManyToMany to establish these relationships. The @JoinColumn annotation is used to specify the foreign key column.

