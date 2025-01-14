Spring beans are just **instance objects that are managed by the Spring container**, namely, they are created and wired by the framework and put into a "bag of objects" (the container) from where you can get them later.

The "wiring" part there is what dependency injection is all about, what it means is that you can just say "I will need this thing" and the framework will follow some rules to get you the proper instance.

[[Bean Life Cycle]], [[Singleton]], [[Prototype]]