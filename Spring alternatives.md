## Quelles alternatives de Spring ?

Pour ma part je connais deux alternatives à Spring.

La première est J2E (pour Java Entreprise Edition) qui est un framework Java. J2E avait certains défauts comme un **fort couplage** et une certaine **lourdeur** car il impose l'utilisation de beaucoup de ses composants. Toutefois, cela reste un framework robuste et viable qui permet de développer des applications d'entreprise complète.

Également, il y a Quarkus qui est un framework plus récent mais qui a été conçu spécifiquement pour les microservices et les applications cloud-natives, il apporte par exemple un style de programmation reactive natif.

### Liste de mots clés : 
JEE, Quarkus, Modularité
### Good to Know 

J2E a un **fort couplage** notamment les servlets doivent hériter de la classe `HttpServlet`, les EJB (Enterprise JavaBeans) doivent implémenter des interfaces spécifiques.

L'architecture J2E était d'une certaine lourdeur et imposait l'utilisation de nombreux composants lourds comme les Serveurs d'applications J2E complets, les Conteneurs EJB ou encore les Bases de données relationnelles.

Ce qu'il faut comprendre c'est que J2E va fournir un ensemble d'outils et de composants pour développer une application et dont on peut ne pas se servir. Alors que Spring, de par son architecture modulaire, va pouvoir proposer différentes briques au développeur pour qu'il n'utilise que ce dont il a besoin.

J2E repose sur des serveurs d'applications complets comme Wildfly ou JBoss. Ils fournissent un environnement d'exécution complet pour les applications mais sont lourds et demandent beaucoup de ressources. Avec Spring (plus précisément son module Spring MVC) quant à lui va utiliser des conteneurs de servlets comme Tomcat qui sont plus légers.

Le développement d'applications cloud-native s'articule autour d'une architecture modulaire qui utilise des services indépendants et faiblement couplés. L'intérêt va être d'avoir des applications hautement évolutives et scalables. 

Quarkus a été conçu dès le départ pour être un framework réactif, contrairement à Spring qui a dû s'adapter à ce paradigme, notamment par le biais de Spring Webflux.

Une applications réactive est conçue pour réagir rapidement aux événements, comme des entrées utilisateur ou des modifications de données. Cela signifie qu'elles peuvent répondre en temps réel sans attendre que d'autres opérations se terminent. Dans une application on va  intéragir avec des flux de données  qui vont se propager directement dans le système.
