The `org.springframework.context` package adds the `ApplicationContext` interface, which extends the `BeanFactory` interface, in addition to extending other interfaces to provide additional functionality in a more _application framework-oriented style_.
 
 `ApplicationContext` is a sub-interface of `BeanFactory`. It adds:

- Easier integration with Spring’s AOP features
- Message resource handling (for use in internationalization)
- Event publication
- Application-layer specific contexts such as the `WebApplicationContext` for use in web applications.

In short, the `BeanFactory` provides the configuration framework and basic functionality, and the `ApplicationContext` adds more enterprise-specific functionality.

## Spring IoC container

The interface `org.springframework.context.ApplicationContext` **represents the Spring IoC container** and is responsible for instantiating, configuring, and assembling the aforementioned beans.

The container gets its instructions on what objects to instantiate, configure, and assemble by reading configuration metadata. 

The configuration metadata is represented in XML, Java annotations, or Java code. It allows you to express the objects that compose your application and the rich interdependencies between such objects.