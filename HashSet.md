The HashSet class implements the `Set` interface in the Java Collections Framework and is a member of the `HashSet` class. 

A `HashSet` is a collection implemented using a `HashMap` as its underlying data structure. When an object is added to the `HashSet`, its `hashCode` is computed to determine the appropriate bucket (array index) for storage. The `HashMap` stores the object’s reference as the key and assigns a dummy value to this key. This design allows the `HashSet` to manage element uniqueness efficiently, as it relies on the `HashMap`'s hashing mechanism to handle both storage and retrieval operations.
## Internal Storage in HashSet

**Objects as Keys**:

- When you add an object to a HashSet, it is stored as a key in an internal HashMap.
- The value associated with each key is a constant dummy object (often referred to as PRESENT).

**Hash Code Calculation**:

- The hash code of the object is calculated using its hashCode() method.
- This hash code is used to determine the bucket index in the internal array (bucket array) of the HashMap.

**Bucket Placement**:

- The hash code is used to determine the bucket index where the key (object) will be placed.
- If there are collisions (multiple objects with the same hash code), a linked list (or tree if many collisions occur) is used to store multiple entries in the same bucket.
## Visual representation of HashSet backed by HashMap


![[Pasted image 20240725165343.png]]



**Short version of adding an Element**:
• When an element is added, its hash code is calculated using the hash function.
• The hash code determines the index in the hash table where the element should be placed.
• If the index is empty, the element is inserted.
• If there are already elements we compare them with `equals()` to know if they are the same, if not we add it, if it is already inside, the add method return false.
