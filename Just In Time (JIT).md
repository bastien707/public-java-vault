**JIT** is a part of the JVM that optimizes the performance of the application. **JIT** stands for **Java-In-Time Compiler**. The JIT compiler is an optimization technique used by the JVM to improve the performance of Java applications.

A JIT compiler runs **after** the program has started and compiles the code (usually bytecode or some kind of VM instructions) on the fly (or just-in-time, as it's called) into a form that's usually faster, typically the **host CPU's native instruction set**. A JIT has access to dynamic runtime information whereas a standard compiler doesn't and can make better optimizations like inlining functions that are used frequently.
## Configuration of JIT

### default 

**By default, most JVM implementations, such as Oracle's HotSpot JVM, use the JIT compiler as part of their standard execution process**. This means that every time you run a Java application, the JVM will start by interpreting the bytecode and then use the JIT compiler to optimize hot spots during execution.
## custom

Some common JVM flags related to JIT compilation include `-Xint` (interpreted mode, no JIT), `-Xcomp` (compile all code, no interpretation), and `-Xmixed` (default mode, using both interpretation and JIT).

## Bytecode Execution in the JVM

JIT compiler only compiles the byte-code to equivalent native code at first execution. Upon every successive execution, the JVM merely uses the already compiled native code to optimize performance.

![[Pasted image 20240721151531.png]]

Without JIT compiler, the JVM interpreter translates the byte-code line-by-line to make it appear as if a native application is being executed.

![[Pasted image 20240721151546.png]]



**Initial Execution with JIT Compiler:**
- First Use When a Java program is run, the JVM starts by interpreting the bytecode. During this phase, the JIT compiler is not immediately involved.
- *Hot Spot Detection*: As the program runs, the JVM identifies frequently executed sections of the bytecode (hot spots).
- *Compilation*: The JIT compiler then compiles these hot spots into native machine code. This compilation happens "just in time" during the execution of the program.
- *Successive Use*: For subsequent executions of these hot spots, the JVM uses the already compiled native code, bypassing the need for further interpretation of these sections. This optimizes performance significantly.
**Without JIT Compiler:**
- If the JIT compiler is not used, the JVM interpreter continuously translates the bytecode into machine code line-by-line at runtime. This method is slower because each bytecode instruction must be interpreted every time it is encountered.