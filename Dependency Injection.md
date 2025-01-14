**Dependency injection is basically providing the objects that an object needs (its dependencies)**. This is done by injecting objects from the outside, i.e. from the constructor or setter when the class is instantiated, rather than directly into the code. It can also be done using 

It promotes the external injection of dependencies into an object, enhancing modularity and testability. In Spring, the IoC container manages object creation and injection, fostering loose coupling and easy maintenance.

When using dependency injection, objects are given their dependencies _at run time rather than compile time_.

***What are the advantages of dependency injection?***

- **Decoupling the creation of object** (in other word, separate usage from the creation of object);
- ability to **replace dependencies** (eg: Wheel, Battery) without changing the class that uses it(Car);
- promotes "**Code to interface not to implementation**" principle;
- ability to **create and use mock dependency** during test (if we want to use a Mock of Wheel during test instead of a real instance we can create Mock Wheel object and let DI framework inject to Car)

The advantage of dependency injection is that you can change dependencies to suit your needs. In other words, you can inject a postgres database instead of mysql. 

This means that there's little coupling between classes, as we separate the creation of the object from its use.

It also simplifies test creation, as mocks can be injected in place of a real instance.

**Without DI**
```java
public class Service {
    private Repository repository = new Repository();
    // tightly coupled to Repository class
}
```

**With DI**
```java
public class Service {
    private final Repository repository;

    @Autowired // not necessary
    public Service(Repository repository) {
        this.repository = repository;
    }
    // loosely coupled, Repository can be easily replaced
}
```

---

More details here:
https://stackoverflow.com/questions/130794/what-is-dependency-injection
Demistifying DI:
https://www.jamesshore.com/v2/blog/2006/dependency-injection-demystified
