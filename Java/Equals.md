By default, the `equals()` method in Java checks if two references point to the same memory location which is the same behaviour of using `==`. However, it can be overridden to compare the contents of objects, allowing for more meaningful equality checks.

For example comparing only the IDs.
### Example
By default this comparison is `false` since the two objects are not the same in memory.

```java
Customer customer1= new Customer("peter");
Customer customer2= new Customer("peter");
customer1.equals(customer2); //return false by JVM i.e. we have two different peter customers
```

If we override equals to compare Customer names we can get the `true` equality.

```java
Customer customer1= new Customer("peter");
Customer customer2= new Customer("peter"); //Insteady identify the Object equality by JVM, we can do it by overring equals method.
customer1.equals(customer2);  // returns true by our own logic
```

If we use built-in hash technique, for above two customers it generates two different hashcode. **So we are storing the same identical object in two different buckets**. To avoid this kind of issues we should override the hashCode method also based on the following principles.

- un-equal instances may have same hashcode.
- equal instances should return same hashcode.


If the contract between `hashCode` and `equals` is not respected, **we may have duplicates** with objects in 2 different buckets, which is against the `HashSet` logic.
## Equals properties

Equals method must satisfy the following properties:

- **Reflexive:** For any non-null reference value `x`, `x.equals(x)` should return `true`.
- **Symmetric:** For any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- **Transitive:** For any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- **Consistent:** For any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` should consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- **Null Comparison:** For any non-null reference value `x`, `x.equals(null)` should return `false`

---

https://stackoverflow.com/questions/2265503/why-do-i-need-to-override-the-equals-and-hashcode-methods-in-java