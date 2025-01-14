The container is responsible for creating instances, configuring them and managing the objects required by the application. As these objects interact, they generally have dependencies which are also managed by the container.
## BeanFactory

The `BeanFactory` interface defines the container's basic functionality. 

It's the **root interface for accessing a Spring bean container**.

Depending on the bean definition, the factory will return either an independent instance of a contained object (the Prototype design pattern), or a single shared instance (a superior alternative to the Singleton design pattern, in which the instance is a singleton in the scope of the factory).

[[Beans]], [[Context]]