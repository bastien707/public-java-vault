The hibernate lifecycles contains four different stages: *Transient*, *Persistent*, *Detached*, *Removed*. The persistence context manages different states of an entity:
### Transient
The object is not related to any database.
The object exists in Heap memory and not associated to a Session, thus is independant of Hibernate.
Once we create an instance of POJO class, then the object entered in the *transient* state.

### Persistent
The object is associated to a Session. The object is in the persistence state when we save or persist it. Hence each object represents the row of the database table. Modifications in the data make changes in the database.

Methods:
```java
session.save(e);  
session.persist(e);  
session.update(e);  
session.saveOrUpdate(e);  
session.lock(e);  
session.merge(e);
```
### Detached
An entity instance that was once managed by the persistence context but is no longer managed because the `EntityManager` has been closed or the entity has been explicitly detached.

We could continue working with the data in the detached state and later call the `merge()` method to save our modifications in a new unit of work

We use detached method when you're limited to the number of connections managed by Hikari (by default around 200). So when you don't want transactions to last too long for large calculations, you can use detached.

```java
session.close();  
session.clear();  
session.detach(e);  
session.evict(e);
```

### Removed
An entity instance that has been marked for deletion but is still managed by the persistence context until the transaction is committed.

![[Screenshot 2024-04-29 at 11.15.57 AM.png]]