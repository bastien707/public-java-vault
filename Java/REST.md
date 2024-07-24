REST stands for **Re**presentational **S**tate **T**ransfer
**It's an architecture style in which resources are manipulated.**
It's a way of creating APIs
## 5 key points

> [!note] 5 key points
>
> 1. identifiable resources
> 2. normalized interface
> 3. stateless conversation
> 4. representation
> 5. hypermedia
### Identifiable resource

Everything is represented by a resource this can be a Car, a Cart, a Customer.
In REST, resources are any kind of object, data, or service that can be accessed. Each resource **must be uniquely identifiable**.

Resources are identified using Uniform Resource Identifiers (**URIs**). For example, a resource representing a user might be accessed via the URI `/users/{userId}`
### Standardized interface

Ensures a uniform way to interact with resources.

We interact with resources according to a list of operation, nouns, verbs **through HTTP** methods:

**POST** = create resources.
**PUT**, **PATCH** = modify, update. PUT needs the whole object. PATCH only needs one field.
**DELETE** = delete a resource.
**OPTION** = view supported verbs.
**HEAD** = retrieve a resource's header (used for the cache system).
#### Codes de retour HTTP
**100-199**: opération de streaming. Information, un peu comme des logs
**200-299**: Succès
**300-399**: Redirection. Important pour faire des API propres, et des API publiques.
	301: MOVED. Déplacement de manière permanent de la resource. permet d'éviter la perte de référencement.
	302: FOUND. Déplacement temporaire.
	304: NOT MODIFIED.
**400-499**: Erreur imputable au client. Le client a mal formulé sa demande.
	400: Bad Request
	401: Unauthorized (pas connecté)
	403: Forbidden (connecté mais interdit en terme de droit)
	404: Not found
**500-599**: Server 
	500: Internal server error (exception)
	502: Bad Gateaway (le serveur n'arrive pas à se connecter au service, surchage serveur)
	503: Service unavailable

### Stateless conversation

Each request contains all the information needed for the server to process it, with no client state stored on the server.

**Make the app scalable**. Requires only a front-end load balancer.
**Favors low coupling**: Session concept cannot be shared.

The advantage of stateles is that it makes it easier to replicate servers, since no data is saved in RAM. **Allows easy horizontal scaling (server replication)**.

### Resource representation

Resources are represented in different formats, such as JSON or XML, specified by the client.

The client specifies the desired format via the `Accept` header in the HTTP request, and the server responds with the resource representation in that format.
For example: `Accept: application/json`.
### Hypermedia

**The responses include hyperlinks to other resources or actions, allowing clients to navigate the API.**

