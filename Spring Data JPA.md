Spring Data JPA is on top of the core Spring Data project and adds additional features to simplify JPA-based data access. Spring Data JPA is a JPA data access abstraction.

It can also generate JPA queries on your behalf through method name conventions.
## Key features

### JPA Repositories
Provides interfaces such as `JpaRepository` and `CrudRepository` for defining repositories. These interfaces come with many pre-defined methods for common CRUD operations.

`JpaRepository` extends `PagingAndSortingRepository` which in turn extends `CrudRepository`. But this structure changed since `spring-data-jpa-3.x`, now it's `ListCrudRepositoy` and `ListPagingAndSortingRepository`. The difference is that it returns a `List` instead of an `Iterable`.

`JpaRepository`  provides CRUD and pagination operations, along with additional methods like `flush()`, `saveAndFlush()`, and `deleteInBatch()`, etc.

#### *Since 3.x*
![[Pasted image 20240728103036.png]]

## Derived Queries

Allows you to create queries by simply defining method names following certain naming conventions. Spring Data JPA automatically generates the necessary SQL or JPQL queries. For example: `findByFirstName(arg1)`. This is useful for simple query but it can be a mess for complex ones :`findByFirstNameStartsWithAndLastNameContainsAndAgeGreaterThan...(arg1, arg2, arg3)`We have static parameters for the query and may sometimes just find the firstName, this is where the **specification** come in.

**Custom Queries**: Supports defining custom queries using the `@Query` annotation in repository interfaces. You can use JPQL, SQL, or native queries.

## Pagination and Sorting

Provides easy-to-use methods for pagination and sorting of results.

## Criteria API and Specifications

Allows the use of JPA Criteria API and Specifications for more complex queries and dynamic query generation. You can support specification using `JpaSpecificationExecutor` interface.

--- 
## References

```cardlink
url: https://stackoverflow.com/questions/14014086/what-is-difference-between-crudrepository-and-jparepository-interfaces-in-spring
title: "What is difference between CrudRepository and JpaRepository interfaces in Spring Data JPA?"
description: "What is the difference between CrudRepository and JpaRepository interfaces in Spring Data JPA?When I see the examples on the web, I see them there used kind of interchangeably.What is the differ..."
host: stackoverflow.com
image: https://cdn.sstatic.net/Sites/stackoverflow/Img/apple-touch-icon@2.png?v=73d79a89bded
```
