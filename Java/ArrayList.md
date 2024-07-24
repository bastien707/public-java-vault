#### Characteristics

- **Underlying Data Structure**: Dynamic array
- **Advantages**: Fast random access, efficient traversal

#### Complexity

- **Insertion (at the end)**: O(1) amortized
- **Insertion (at a specific position)**: O(n) (due to shifting elements)
- **Access (get)**: O(1)
- **Update (set)**: O(1)
- **Deletion (from a specific position)**: O(n) (due to shifting elements)
- **Search (contains)**: O(n)

#### Use Case

- Use `ArrayList` when you need fast random access and don't often need to insert or delete elements from the middle of the list.