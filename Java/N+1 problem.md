The **_N+1 query problem_** is said to occur when an ORM, like hibernate, executes 1 query to retrieve the parent entity and N queries to retrieve the child entities.
This can quickly lead to a large number of queries being executed, resulting in poor application performance.

## Why Does the N+1 Problem Occur?

The N+1 problem occurs because of Hibernate’s default fetching strategy. By default, Hibernate uses lazy loading for associations, which means that associated entities are loaded only when they are accessed. This behavior helps reduce unnecessary data retrieval, but it can lead to the N+1 problem when not used strategically.

**Although this problem often is connected to lazy loading, it’s not always the case.**