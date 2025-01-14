The Open Session in View (OSIV) *anti-pattern* in Hibernate ensures that the **Hibernate Session remains open for the entire duration of an HTTP request**, from the beginning of the request until the view (typically the HTML response) is fully rendered.

| PROS                                   | CONS                        |
| -------------------------------------- | --------------------------- |
| developer productivity                 | data base performance issue |
| Prevents `LazyInitializationException` | Extended session lifecycle  |

### The typical flow with OSIV

1. **Request Begins**: A web request is received.
2. **Session Opened**: A Hibernate session is opened at the start of the request.
3. **Service Layer**: The session is used for database operations in the service layer.
4. **View Rendering**: The session remains open while the view is being rendered, allowing lazy-loaded entities to be fetched if they are accessed during view rendering.
5. **Session Closed**: The session is closed at the end of the request.

### Alternatives

**Explicit Fetching**: Load all required data in the service layer before returning it to the controller. Use @Transactional, and since we implicitly also open a Hibernate Session, we can fetch our relations lazily.

### Deactivate OSIV

You can disable OSIV like this :

```yml title:application.yml
spring:
	jpa:
		open-in-view:false
```