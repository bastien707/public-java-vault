*Functional programming* represents a programming *paradigm* that aims to bind all things in **pure mathematical functions** based on lambda calculus. In other words, FP is an approach to software construction based on creating pure functions. FP helps in solving problems where many different operations need to be performed on the same data set.
### Core principles

- **Pure Functions:** Functions that always produce the same output for the same input and have no side effects (do not alter any state or data outside their scope). 

- **Immutability:** Data is immutable; once created, it cannot be changed. New data structures are created instead of modifying existing ones.

- **First-Class and Higher-Order Functions:** Functions are treated as *first-class citizens*[^1], meaning they can be passed as arguments to other functions, returned as values, and assigned to variables. Higher-order functions are functions that can take other functions as arguments or return them as results.

- **Function Composition:** Building complex functions by combining simpler ones.

- **Declarative Programming:** Focus on what to solve rather than how to solve it, often resulting in more concise and readable code.

### FP in Java

Java introduces functional programming with some keys features such as: *Lambdas, Functional interfaces, Streams, Method references.*
###  Advantages of FP

- **Conciseness and Readability:** Lambda expressions and the Stream API reduce boilerplate code, making the code more concise and easier to read.
- **Parallel Processing:** Streams can be **easily parallelized**, this is the main advantage over Collection API, enabling efficient multi-core processing.
- **Immutability and Thread-Safety:** Emphasizing immutability makes code safer and easier to reason about, particularly in concurrent applications.
- **Easier to test** ⇒ no side effects, consistent state

[^1]: In a given programming language design, a first-class citizen is an entity which supports all the operations generally available to other entities. These operations typically include being passed as an argument, returned from a function, and assigned to a variable. For Example a programming language is said to have first-class functions when functions in that language are treated like any other variable.

[[First class citizen]]
