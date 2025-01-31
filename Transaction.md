**A transaction is a sequence of operations performed as a single logical unit of work.**

A transaction must follow ACID properties 
## ACID

#### Atomicity
Ensures that all operations within the transaction are completed successfully. If any operation fails, the entire transaction is rolled back, leaving the database in its original state.
#### Consistency
Consistency ensures that a database remains in a valid state before and after a transaction. It guarantees that any transaction will take the database from one consistent state to another, **maintaining the rules and constraints defined for the data**.
#### Isolation
Ensures that the operations within a transaction are isolated from other transactions. Intermediate states of a transaction are not visible to other transactions, preventing concurrent transactions from interfering with each other.
#### Durability
Ensures that once a transaction has been committed, its changes are permanent and persist even in the case of a system failure.