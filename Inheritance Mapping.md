
Relational databases don’t have a straightforward way to map class hierarchies onto database tables.

Inheritance Mapping is a fundamental aspect of object-oriented programming, and Hibernate provides several strategies to map inheritance hierarchies to database tables efficiently.
### Single Table Inheritance
In this strategy, all classes in the inheritance hierarchy are mapped to a single database table. A discriminator column is used to differentiate between different types of entities.
`@Inheritance(strategy = InheritanceType.SINGLE_TABLE)`
 
### Joined Table Inheritance
This strategy involves mapping each class in the hierarchy to its own database table. Common attributes are mapped to a shared table, and subclass-specific attributes are stored in separate tables.

### Table per Class Hierarchy
Here, a single table is used to represent the entire class hierarchy. All attributes of all classes are stored in the same table, and a discriminator column is used to identify the type of each entity.

### Table per Concrete Class
In this strategy, each concrete class in the hierarchy is mapped to its own database table. No inheritance-related columns are present, and tables are fully denormalized.