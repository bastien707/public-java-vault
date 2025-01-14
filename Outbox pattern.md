- Solve dual-write problem and ensure atomic distributed transactions.
- Two-Phase Commit (2PC) is not a solution.
- Persist message in outbox table before sending.
- A job publish the events to the message broker.
## Problem
*How to atomically update the database and send messages to a message broker?*
- Update its database: Save a new order in its database
- Send a message to a message broker: Notify other services about the order via a message broker
It's a *dual-write* problem.

## Solution 

The solution is for the service that sends the message to first store the message in the database as part of the transaction that updates the business entities. A separate process then sends the messages to the message broker.

 Simply, when your API publishes event messages, it doesn’t directly send them. Instead, the messages are persisted in a database table. After that, A job publish events to message broker system in predefined time intervals.

![[Pasted image 20250109130906.png]]
## Source 

cf. https://microservices.io/patterns/data/transactional-outbox.html

