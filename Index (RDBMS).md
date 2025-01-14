- It's a data structure like a binary tree, often.
- It's used because the sequential search in database can be not efficient enough on huge amount of data.
- We have a default on the id (PK).
# Index anatomy

- An index is pure redundant data, but is **an ordered copy of data**.
- It's updated by the SGBD.

## Index B-tree

- B-Tree is a kind of index and is the most common one
- B stands for *Balanced*. This mean in every leaf has the same depth. Same depth ⇒ constant time for lookup.

### Leaf node (noeud feuille)

- Data structure of ordred double linked list.
- Every node points to the previous and next node.
- Linked list allow simple insertion anywhere

### Branch node

- Composed of only one column that is the one we want to index.
- Point to a node with a value lower than or equal.


### Complexity

- with index $O(log(n))$ ⇒ log curve mean with a lot of data it won't add much complexity
- without index $O(n)$ ⇒ go through whole data, which is linear.
## Example

for example create an index on column `customer_id`. The leaf node is composed of ordered customer_id and the row_id points to the row of the data on the table.

Create an index : `CREATE INDEX index_customer_id ON "order" (customer_id);`

![[Screenshot 2024-09-07 at 9.40.08 AM.png]]


## Query Plan

- **How the database plan the query execution.**
- Use keyword `EXPLAIN [ANALYZE]`. Optionally you can add `ANALYZE` that will explain the query and **execute it**, so do not try it in production.

Contains some important key words when reading EXPLAIN:
- Sequential Scan ⇒ seq scan. Means DB does not use index and scan the whole table.
- Index Scan : mean index has been used.