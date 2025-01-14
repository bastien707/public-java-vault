**A transaction is a sequence of operations performed as a single logical unit of work.**

A transaction must follow ACID properties 
## ACID

#### Atomicity
Ensures that all operations within the transaction are completed successfully. If any operation fails, the entire transaction is rolled back, leaving the database in its original state.
#### Consistency
Ensures that a transaction takes the database from one valid state to another. For example, when making a bank transfer of €100, the money must be added from one account and debited from the other account. It cannot be just added to one account.
#### Isolation
Ensures that the operations within a transaction are isolated from other transactions. Intermediate states of a transaction are not visible to other transactions, preventing concurrent transactions from interfering with each other.
#### Durability
Ensures that once a transaction has been committed, its changes are permanent and persist even in the case of a system failure.