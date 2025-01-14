**Integration tests verify that different components or systems work together as expected**. They test how various units or services interact with each other, including external systems like databases, APIs, or file systems.
#### Characteristics

- **Complex Setup**: Integration tests typically require more setup and teardown, such as starting a server or setting up a database.
- **Longer Execution Time**: They are generally slower to execute compared to unit tests because they involve multiple components and possibly external systems.
- **Broader Scope**: They cover a broader scope, including the interaction between various units, external services, and user interfaces.

### Test containers

TestContainers is a library that provides lightweight, disposable containers for integration testing.