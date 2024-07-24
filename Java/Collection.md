A _collection_ is an object that represents a group of objects.

The Java Collections Framework is a set of classes in `java.util` for storing collections.
## Collection Interface

`Collection` is the root of the collection hierarchy. A collection represents a group of objects known as its _elements_. The `Collection` interface is the least common denominator that all collections implement and is used to pass collections around and to manipulate them when maximum generality is desired. Some types of collections allow duplicate elements, and others do not. Some are ordered and others are unordered. The Java platform doesn't provide any direct implementations of this interface.
### Arrays vs Collections

- Arrays can **store primitives** where collections cannot.
- **Arrays are fixed in size** that is once we create an array we can not increased or decreased based on our requirement. **Collection are growable in nature** that is based on our requirement.


