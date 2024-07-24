The HashSet class implements the `Set` interface in the Java Collections Framework and is a member of the `HashSet` class. 

The underlying data structure for HashSet is Hashtable. In *Hashtable* we specify an object that is used as a key, and the value we want to associate to that key. The key is then hashed, and the resulting hash code is used as the index at which the value is stored within the table.
![[Screenshot 2024-07-24 at 8.10.28 AM.png|300]]

Unlike duplicate values, **it stores a collection of distinct elements**. In this implementation, each element is mapped to an index in an array using a hash function, and the index is used to quickly access the element. It produces an index for the element in the array where it is stored based on the input element. Assuming the hash function distributes the elements among the buckets appropriately, the HashSet class provides constant-time performance for basic operations (add, remove, contain, and size).