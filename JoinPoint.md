A joinpoint is a _candidate_ point in the **Program Execution** of the application where an aspect can be plugged in. This point could be a method being called, an exception being thrown, or even a field being modified. These are the points where your aspect’s code can be inserted into the normal flow of your application to add new behavior.

**A Joinpoint is an opportunity within code for you to apply an aspect**. Just an opportunity. Once you take that opportunity and select one or more Joinpoints and apply an aspect to them, you've got a Pointcut.
