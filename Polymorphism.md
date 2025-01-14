- Overriding
- Overloading
- Type compensation

**Polymorphism in Java** is a concept by which we can perform a _single action in different ways_. Polymorphism is derived from 2 Greek words: poly and morphs. The word "poly" means many and "morphs" means forms. So polymorphism means many forms.

## Types of polymorphism

### Compile time

Compile time polymorphism or **method overloading** a function called during compile time. For instance, take a class ‘area’. Based on the number of parameters it may calculate the area of a square, triangle, or circle.

In Java, Method Overloading allows different methods to have the same name, but different signatures where the signature can differ by the number of input parameters or type of input parameters, or a mixture of both.

You can achieve **polymorphism without inheritance**. You can use interface implementation and method overloading to achieve polymorphism. Interface implementation allows different classes to use the same interface but implement methods differently.
### Runtime

Runtime polymorphism or **method overriding** links during runtime. **The method inside a class overrides the method of the parent class.**

Method overriding, also known as run time polymorphism is one where the child class contains the same method as the parent class. For instance, we have a method named `eat()` in the parent class. A method `eat()` is again defined in the sub-class. Thus when `eat()` is called in the subclass, the method within the class id executed. Here, `eat() `within the class overridden the method outside.
## Advantages

1. **Code Reusability:** Polymorphism provides the reuse of code, as methods with the same name can be used in different classes.
2. **Flexibility and Dynamism:** Polymorphism allows for more flexible and dynamic code, where the behaviour of an object can change at runtime depending on the context in which it is being used.
3. **Reduced Complexity:** It can reduce the complexity of code by allowing the use of the same method name for related functionality, making the code easier to read and maintain.

## Disadvantages

1. **Complexity:** It can sometimes make code more complex, especially when multiple methods or constructors with the same name are defined in a class hierarchy.
2. **Debugging:** Debugging polymorphic code can be more challenging, as it may be difficult to trace the exact method that is being executed at runtime.

**What is the difference between polymorphism and inheritance in Java?**

Polymorphism is a concept where a function is defined in more than one form whereas in inheritance, a new class inherits the features from an already existing class. The concept of polymorphism applies to functions or methods whereas inheritance applies to classes.