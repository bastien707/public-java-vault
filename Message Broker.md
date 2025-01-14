- Message Broker **facilitates asynchronous communication**. Does not require immediate response. Whereas Web APIs use synchronous communication this is suitable for direct, point-to-point interactions.
- **Low coupling**
- **Common Distributions Patterns** : point to point or Publish/Subscribe
- **Capacity to Manage Large Data Volumes**. Message brokers are designed to handle large quantities of messages, which is crucial in systems with high data throughput.
- Kafka or RabbitMQ are message brokers.

---
## Definition

A message broker is an intermediary software that facilitates communication between different applications by translating messages from the sender’s protocol to the receiver’s protocol in an **asynchronous manner**. It helps **decouple services**, allowing them to communicate without direct dependencies on each other’s details like IP addresses or ports.

**Difference with REST API**: 
- Works asynchronously. High-consuming tasks can be distributed to separate processes. That will fasten up your application and increase user experience.
- The message broker guarantees that message will not be lost in case of failure of the consumer. It’s stored safely in the message broker queue.

Netflix sends about 5 hundred billion events and 1.3 petabytes of data per day into Kafka.

## The problem it solves

A typical business collects data through a variety of applications, e.g., accounting, billing, CRM, websites, etc. Each of these applications have their own processes for data input and update. In order to get a unified view of their business, engineers have to develop bespoke integrations between these different applications.

![[Pasted image 20241109222929.png]]

Each integration comes with difficulties around
- **Protocol** – how the data is transported (TCP, HTTP, REST, FTP, JDBC…)
- **Data format** – how the data is parsed (Binary, CSV, JSON, Avro…)
- **Data schema & evolution** – how the data is shaped and may change

With Apache Kafka as a data integration layer, data sources will publish their data to Apache Kafka and the target systems will source their data from Apache Kafka. This decouples source data streams and target systems allowing for a simplified data integration solution, as you can see in the diagram below.

![[Pasted image 20241109223108.png]]

## *Asynchronous Processing*

Message brokers enable asynchronous communication, allowing services to operate independently. A service can send a message and continue its operations without waiting for a response, which is especially useful for long-running tasks.

## *Components*

- **Producer –** the *application responsible for sending messages*. It’s connected with the message broker. In publish/subscribe pattern they are called `publishers`. 
- **Consumer –** the *endpoint that consumes messages* waiting in the message broker. In publish/subscribe pattern they are called `subscribers`. 
- **Topic –** A message distribution channel. Each message published in a topic can be **consumed several times**. Several consumers can subscribe to the same topic, and each will receive the entire message.
- **Queue —** a queue a single message processing channel. Each message published in a queue is generally **consumed only once**. A consumer takes a message from the queue, and it is no longer available to other consumers.
- **Partitions** - Part of a topic

## *Distribution Patterns*

### Point-to-point messaging

There is **one-to-one relation set between the sender and the receiver of the message**. Each message is sent and consumed only once.

![[Pasted image 20241109202000.png]]


### Publish/subscribe

**The sender of the message doesn’t know anything about receivers**. The message is being sent to the topic. After that, it’s distributed among all endpoints subscribed to that topic. It can be useful for notification mechanism. In this pattern, **the components are loosely coupled** and transmit events to one another.

![[Pasted image 20241109201947.png]]
### When use a message broker ?

- Long-running tasks and crucial API
- Microservices
## Some message broker
- Kafka
- RabbitMQ
- ActiveMQ
- Redis

#### Kafka vs RabbitMQ
Kafka is made of topics, not queues (unlike RabbitMQ, ActiveMQ, SQS). Queues are meant to scale to millions of consumers and to delete messages once processed. In Kafka data is not deleted once processed and consumers cannot scale beyond the number of partitions in a topic.

## Go further
- Protocol AMQP
- [[Outbox pattern]]