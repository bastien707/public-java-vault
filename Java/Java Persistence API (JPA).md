**The Java Persistence API (JPA) is a specification that defines how to persist data in Java applications**.

It's a **specification** meaning it provides a **set of guidelines and rules for how to interact with databases** in Java applications.

JPA was originally intended for use with relational databases, some JPA implementations have been extended for use with NoSQL datastores such as EclipseLink.

You can find the `spring-boot-starter-data-jpa`:

```cardlink
url: https://github.com/spring-projects/spring-boot/blob/main/spring-boot-project/spring-boot-starters/spring-boot-starter-data-jpa/build.gradle
title: "spring-boot/spring-boot-project/spring-boot-starters/spring-boot-starter-data-jpa/build.gradle at main · spring-projects/spring-boot"
description: "Spring Boot. Contribute to spring-projects/spring-boot development by creating an account on GitHub."
host: github.com
favicon: https://github.githubassets.com/favicons/favicon.svg
image: https://opengraph.githubassets.com/9b1c959e6f17f53a608e4dc0b9b80806ee09b9c798bf4d9a48a2f40941e7ab4a/spring-projects/spring-boot
```

## Popular implementations

- **[[EclipseLink]]:** The reference implementation for JPA 3. It supports both relational and some NoSQL databases.
- **[[Hibernate]]:** One of the most popular JPA implementations. Although it started as an ORM tool, it fully supports the JPA specification.

### JPA is not an ORM

JPA and ORM are related but distinct concepts.

- **JPA:** Handles the querying and management of data.
- **ORM:** Focuses on the mapping between Java objects and database tables.