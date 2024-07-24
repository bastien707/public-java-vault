LAZY fetching means that the associated **entities are loaded on demand**. The data is fetched only when it's actually accessed for the first time. **It delays the fetching of associated entities or collections until they are actually accessed.**

When Hibernate loads a `Customer` entity with lazy-loaded `orders`, it doesn't immediately load the `Order` entities. Instead, it creates a proxy for the `orders` collection.
A proxy is a placeholder object that acts as a stand-in for the actual collection of `Order` entities.

### `LazyInitalizationException`

`LazyInitializationException` would occur if a proxy tries to load data after the session is closed. If you try to access a lazy-loaded property after the session is closed, the proxy cannot load the data. This triggers a `LazyInitializationException` because the proxy doesn't have access to the session needed to fetch the data.