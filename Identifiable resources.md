- Un des 5 concepts de REST ⇒ resource identifiable.
- Signifie qu'une entité va être identifiée par une URI (Unified Resource Locator).
- Une ressource peut désigner une donnée, un objet.

**Exemple**
- Un livre peut être identifié par : `bibliothèque.fr/livres/{id}`.

**Les avantages**
- Simplicité et clarté, et standardisation dans la manière de développer

Everything is represented by a resource this can be a Car, a Cart, a Customer.
In REST, resources are any kind of object, data, or service that can be accessed. Each resource **must be uniquely identifiable**.

Resources are identified using Uniform Resource Identifiers (**URIs**). For example, a resource representing a user might be accessed via the URI `/users/{userId}`