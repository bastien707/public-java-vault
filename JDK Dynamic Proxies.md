Spring AOP primarily uses Java’s dynamic proxies **when the target object implements one or more interfaces**. Java’s Proxy class is used to create these dynamic proxies at runtime.

Java Dynamic proxies can proxy: `public class Foo implements iFoo`