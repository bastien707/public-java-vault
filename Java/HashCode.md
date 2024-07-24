The `hashCode` method returns an integer value that represents the object. This integer is used to determine the bucket (a storage location in the hash table) where the object will be stored.

Collections such as `HashMap` and `HashSet` use a _hashcode_ value of an object to determine how it should be stored inside a collection, and the _hashcode_ is used again in order to locate the object in its collection.

Hashing retrieval is a two-step process:

1. Find the right bucket (using `hashCode()`)
2. Search the bucket for the right element (using `equals()` )
![[Pasted image 20240723202804.png|350]]

---

Méthode qui renvoie un entier. Souvent utilisée pour les Collections qui utilisent un hash comme `hashSet` et `hashMap`. Ces méthodes vont regrouper en mémoire les objets en **buckets**. On peut savoir dans quel bucket il est situé grace au hashcode.

Un bucket peut être relié a un champs, par exemple "lieu de naissance". Cela permet d'être plus rapide dans la recherche.

On comprend donc pourquoi deux objets avec le même hashcode ne sont pas forcément égaux. Et deux objets égaux ont forcément le même hashcode.

On va comparer ensuite les objets d'un bucket avec le equals.

Utilisé pour les hashset etc car les objets avec le même hashcode vont être dans le même bucket et ça permet de simplifier lors de la recherche. Si tu cherches un Damien tu as un bucket avec les prénom en "D" ce qui simplifie la recherche.


