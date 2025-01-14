Inheritance is a mechanism in Java by which **one class** (child/subclass) **can inherit the fields and methods of another class** (parent/superclass). It promotes code reusability and establishes a relationship between the parent and child classes, forming an "is-a" relationship.

Inheritance allows a class to use methods and fields of another class without rewriting the code. This promotes code reusability and reduces redundancy.

Java does not support multiple inheritance, instead, **Java allows multiple inheritance through interfaces.**
### Limitations

- **Tight Coupling**: Subclasses are tightly coupled to superclasses, making changes in the superclass affect the subclass.
-  **Fragile Base Class Problem**: Changes in the base class can inadvertently affect the subclasses ⇒ to solve this problem you can use composition.