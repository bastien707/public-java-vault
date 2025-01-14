**When the target object does not implement any interfaces**, Spring uses CGLIB (Code Generation Library) to create a subclass of the target object. This allows Spring to intercept method calls on that subclass.

CGLIB can proxy: `public class Foo` but not `public class Foo implements iFoo`