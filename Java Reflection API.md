- Mechanism for **examining and manipulating a program**'s classes, methods, fields and other elements **during execution**.
- Reflection ignores Java encapsulation.
- Reflection has significant **performance differences**, and is more expensive. 

As the documentation says : *"Reflection is commonly **used by programs which require the ability to examine or modify the runtime behavior of applications running in the Java virtual machine**. This is a relatively advanced feature and should be used only by developers who have a strong grasp of the fundamentals of the language. With that caveat in mind, reflection is a powerful technique and can enable applications to perform operations which would otherwise be impossible."*

***Exemple:***
```java
// Obtenir des informations sur une classe pendant l'exécution
Class<?> clazz = UserService.class;
// ou dynamiquement
Class<?> dynamicClass = Class.forName("com.example.UserService");

// Inspecter les champs
Field[] fields = clazz.getDeclaredFields();
// Inspecter les méthodes
Method[] methods = clazz.getDeclaredMethods();
```


### Sources
https://docs.oracle.com/javase/tutorial/reflect/index.html
https://stackoverflow.com/questions/435553/java-reflection-performance

[[Java ☕️]]
[[Proxy]]
[[Spring Framework 🌱]]
