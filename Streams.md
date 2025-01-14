Data flow on which operations are applied in a particular order.

JVM optimize better streams over using loops.

Operations can be:
**intermediate**: `map()`, `filter()` or
**terminal**: `forEach()`, `reduce()`, `collect()`, `min`, `max`.

They can be used only **once**.

![[Screenshot 2024-05-30 at 1.48.52 PM.png]]

### Stream advantages
- We can run **parallel stream** which improve the execution on huge amount of data over Collection API.
- **Lazy Evaluation**. Intermediate operations are lazy and do not perform any computation until a terminal operation is invoked.
- **Memory efficient** : stream does not store intermediate result.