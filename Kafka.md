- *Apache Kafka* is a message broker
- Confluent Platform includes Apache Kafka than simply use for example provide clients in Python, C++, Golang....
 ---
Kafka ***topics*** organize related events. For example a topics can be "*logs*" which contains logs from an application. Unlike SQL tables topics are not queryable. Instead we must create Kafka *producers* and *consumers* to utilize data.

Once the topics is created we can send data to it. Applications that send data into a topic are known as Kafka ***producers***.  Kafka producers are deployed outside Kafka and only interact with Apache Kafka by sending data directly into the Kafka topics.

Once a topic has been created and data produced into the topic, we can have applications that make use of the data stream. Applications that pull event data from one or more Kafka topics are known as Kafka ***consumers***. Kafka consumers as Kafka producers are deployed outside Kafka. They read data directly from Kafka topics.