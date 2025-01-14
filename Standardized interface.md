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
