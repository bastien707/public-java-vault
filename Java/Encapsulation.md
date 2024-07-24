The main advantage of Encapsulation in Java is its ability to **protect the internal state of an object from external modification or access**. It is the is a way of hiding the implementation details of a class from outside access and only exposing a public interface that can be used to interact with the class. The main benefit is of providing a way to control and manage the state and the behavior of an object and also protecting it from modification and unauthorized access at the same time.
### How is it achieved ?

This is achieved using access modifiers like `private`, `protected`, and `public`.

We should:
- Declaring the fields (data) of a class as `private`.
- Providing public getter and setter methods to access and update the value of the private fields.

Fields should be private to prevent direct access and modification from outside the class. This ensures control over how the fields are accessed and modified, allowing validation and consistent state management.
## Advantages

1. **Data Hiding**: it is a way of restricting the access of our data members by hiding the implementation details. Encapsulation also provides a way for data hiding. The user will have no idea about the inner implementation of the class. 
2. **Increased Flexibility**: We can make the variables of the class **read-only or write-only** depending on our requirements. 
3. **Reusability**: Encapsulation also improves the re-usability and is easy to change with new requirements.
4. **Testing code is easy**: Code is made easy to test for unit testing.