Garbage collector is an algorithm that aims to free the heap memory of a java application during runtime.
## Mark and sweep

Basically, _GC_ works in two simple steps, known as Mark and Sweep:

- **Mark –** this is where the garbage collector identifies which pieces of memory are in use and which aren’t.
- **Sweep –** this step removes objects identified during the “mark” phase.

But mark and sweep is outdated. We use the G1 today.

An in **use object**, or a referenced object, means that some part of your program still maintains a pointer to that object.

An **unused object**, or unreferenced object, is no longer referenced by any part of your program. So the memory used by an unreferenced object can be reclaimed.
## Implementations

GC depends of the JVM type.
- Concurrent ⇒ 
- Stop the world ⇒ 

JVM has four types of _GC_ implementations:

- Serial Garbage Collector
- Parallel Garbage Collector
- G1 Garbage Collector
- Z Garbage Collector

### Benefits of Garbage Collection

- **Simplifies Development**: Developers do not need to manually manage memory, reducing the risk of memory leaks and pointer errors.
- **Improves Application Stability**:
- **Enhances Performance**: Modern garbage collectors are highly optimized to balance between throughput and latency, improving overall application performance.


---

https://www.oracle.com/webfolder/technetwork/tutorials/obe/java/gc01/index.html