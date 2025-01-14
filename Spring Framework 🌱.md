The Spring Framework is a comprehensive framework for enterprise Java development. The main goal is to make JEE application development easier.

J2E apps were **tightly coupled** (should extend servlet, EJB...). It's **heavy weight**, and need a lot a **boilerplate code**. *Rod Johnson* introduced Spring Framework.

Spring Boot : 3.2.5 is based on Spring: 6.1.

## Spring in a nutshell

- It's a framework.
- It offers **DI** and **IoC**.
- It leverages **AOP** to enhance your POJOs.

- Main advantage : thanks to the ***IoC*** pattern, the developer can **focus** on the **business code**.
# Spring Modules

The Spring Framework is **divided into modules**. Applications can choose which modules they need. At the heart are the modules of the core container, including a configuration model and a dependency injection mechanism. Beyond that, the Spring Framework provides foundational support for different application architectures, including messaging, transactional data and persistence, and web. It also includes the Servlet-based Spring MVC web framework and, in parallel, the Spring WebFlux reactive web framework.

The Spring Framework consists of features organized into about **20 modules**. These modules are grouped into *Core Container*, *Data Access/Integration*, *Web*, *AOP* (Aspect Oriented Programming), *Instrumentation*, and *Test*, as shown in the following diagram.

![[Pasted image 20240722131813.png]]

## Spring core

*Spring core* is the base module for all other modules.
It is used to manage the object dependencies. Spring will create the required objects and supply to the application for us.
## Beans and Context

The `org.springframework.beans` and `org.springframework.context` packages are the basis for Spring Framework’s IoC container.


[[Spring Boot]], [[Spring Security]], [[Spring Data]], [[Inversion of Control 🔄]], [[Core Container]], [[Dependency Injection]], [[Spring Webflux]], [[Spring MVC]], [[Aspect Oriented Programming]], [[Spring AOP]]