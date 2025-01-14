- `volatile` is used in multithread environment
-  Forces reads and writes to avoid **CPU-level caches**
- **Ensure that updates are always visible to all threads**. They are directly written to and read from main memory, bypassing CPU caches
- Guarantees visibility but **does not ensure atomicity** for compound actions (e.g., i++)


## Visual representation

![[Volatile_keyword_java.excalidraw|700]]




