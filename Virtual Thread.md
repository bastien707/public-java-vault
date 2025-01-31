- From Java 21
- a.k.a *Project Loom*
- Unlike a platform thread, a virtual thread **fully belongs and is managed by the JVM**
- Platform thread is mapped 1:1 with physical thread : the number of available platform threads is limited to the number of OS threads.
- Many virtual threads can be carry by one carrier thread (platform) and the carrier is mapped 1:1 with physical thread.
- Context switching is less expensive on carrier thread than physical.
- Very cheap and fast to create in large quantities.
- Just **like any Java object allocated on the heap** and can be reclaimed by the JVM's garbage collection when it is no longer needed.
 
***

A **platform thread** is implemented as a thin wrapper around an operating system (OS) thread. A platform thread runs Java code on its underlying OS thread, and the platform thread captures its OS thread for the platform thread's entire lifetime.

**Virtual thread** is also an instance of java.lang.Thread. However, a virtual thread isn't tied to a specific OS thread. A virtual thread still runs code on an OS thread.

Virtual threads are not faster threads; they do not run code any faster than platform threads. **They exist to provide scale (higher throughput), not speed (lower latency).**
### Use cases
- Perfect **for managing thousands of simultaneous HTTP connections**
- Each request can have its own thread at no extra cost
- Example: API REST servers with many clients
- Microservices with many external calls
- Ideal when your service needs to call several other services

- Necessite des années de R&D car on utilisait que des thread physique
- L'api Virtual Thread permet de faire du java a haute concurrence sans passer par des thread OS et mieux utilsier le CPU.
- On peut wrapper des appels bloquants dans des pool de thread.


As soon as we create at least one virtual thread, under the hood, the **JVM creates a relatively small internal pool of platform threads**. Whenever the JVM wants to run a particular virtual thread, for example, thread A, **it mounts it on one of the platform threads within its pool.**

In certain situations, if thread A has not finished but is unable to make any progress at that time, the JVM will unmount it but save its current state on the heap.

![[Pasted image 20250114103747.png]]

### Source 
***

```cardlink
url: https://dev.to/elayachiabdelmajid/java-21-virtual-threads-1h5b
title: "Java 21: The Magic Behind Virtual Threads"
description: "To understand virtual threads very well, we need to know how Java threads work.   Quick Introduction..."
host: dev.to
favicon: https://media2.dev.to/dynamic/image/width=32,height=,fit=scale-down,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F8j7kvp660rqzt99zui8e.png
image: https://media2.dev.to/dynamic/image/width=1000,height=500,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2F87zw0r66zjrqoh7okn3m.png
```


```cardlink
url: https://docs.oracle.com/en/java/javase/21/core/virtual-threads.html#GUID-2BCFC2DD-7D84-4B0C-9222-97F9C7C6C521
title: "Core Libraries"
description: "Virtual threads are lightweight threads that reduce the effort of writing, maintaining, and debugging high-throughput concurrent applications."
host: docs.oracle.com
```



[[Thread]]
[[Local Thread]]
[[Multi Threading]]
[[Java Versions and features]]