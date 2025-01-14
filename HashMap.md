
A HashMap uses an array of buckets (or slots) to store entries. This array is sometimes called a “hash table.” Each index in this array corresponds to a bucket that can hold a linked list (or a balanced tree in certain cases).

Each key in the HashMap is hashed using its hashCode() method. This hash code determines which bucket (index in the array) the key-value pair will be placed into.
The hash code is used to calculate the bucket index using a formula that ensures the index is within the bounds of the array size.

When two keys hash to the same index (bucket), a collision occurs. **Linked List**: Initially, the HashMap handles collisions by using a linked list to store multiple key-value pairs in the same bucket. Each node in the linked list contains a key-value pair and a reference to the next node.
**Tree Structure**: If a bucket grows too large (more than a certain threshold), the HashMap may convert the linked list to a balanced tree to improve performance. This transformation helps in maintaining faster lookup times in buckets with many entries.

**Insertion**: 
When adding a new key-value pair, the HashMap calculates the bucket index using the hash code of the key. If the bucket is empty, a new node with the key-value pair is created and placed in the bucket. If the bucket already has nodes (due to collisions), the HashMap checks for existing keys and either updates the value if the key exists or appends the new node to the end of the list (or tree).

**Updating Values**: 
If a key already exists in the bucket, its associated value is updated with the new value. This involves traversing the linked list (or tree) to find the node with the matching key and updating its value.

**Lookup**: To retrieve a value for a given key, the HashMap computes the bucket index using the hash code of the key. It then traverses the linked list (or tree) at that bucket index to find the node with the matching key and return its value.