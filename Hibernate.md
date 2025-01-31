- Hibernate is an ORM
- Implementation of [[Java Persistence API (JPA)|JPA]]

---
Hibernate is an ORM which stands for **Object Relational Mapping**. **It's an implementation of JPA specification.**

Object-Relational Mapping (ORM) is the **process of converting Java objects to database tables**. In other words, this allows us to interact with a relational database without any SQL.

Hibernate enables the relationship between the object and the database.

We can use Hibernate without JPA. Hibernate release before JPA in 2001.

- `EntityManager` ⇒  JPA
- `SessionFactory` ⇒  Hibernate

See [[EntityManager]] and [[Session]]

### Analogy

**Row** in the table correspond to a instance.
**Column** in the table correspond to a field of the class.

How does Hibernate works internally to link Relational model to Classes ?

Inheritance : `@Inheritance(strategy = InheritanceType.JOINED)`


`cascade = CascadeType.ALL`: Cela indique que toutes les opérations effectuées sur l'entité parent (ici Cart) seront également propagées aux entités enfants (Ici tes CartArticles). Les opérations concernés par le . ALL sont : PERSIST MERGE REMOVE REFRESH DETACH

`orphanRemoval = true`: Cela signifie que les entités enfants seront automatiquement supprimées de la base de données si elles ne sont plus référencées par l'entité parente. C'est utile pour maintenir l'intégrité référentielle et éviter les enregistrements orphelins dans la base de données. Donc ici, c'est utile si tu supprimes manuellement un Cart de ta BDD. Dans ce cas là, tes CartArticles seront retirés.