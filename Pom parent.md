Un **POM parent** dans Maven est un fichier de configuration qui utilise la notion d'héritage pour partager des configurations communes entre les projets ou modules.  L’objectif est d’**éviter les redondances** et de **standardiser** les configurations (dépendances, versions de plugins, propriétés) afin que les POM enfants n’aient pas à les redéfinir. C'est donc une manière de factoriser notre configuration.

Un exemple concret va être d'utiliser `spring-boot-starter-parent` qui hérite lui-même de `spring-boot-dependencies` et va definir notamment les versions des starters spring. Ainsi dans les pom qui vont hériter, on n'a pas a spécifier dans les *pom* enfants les versions pour les starters notamment.

---

## Good to know

#### Le Super POM 🦸‍♂️

Il y a le super pom qui est  le POM de base dont tous les projets Maven héritent implicitement. Il contient des configurations par défaut utilisées par Maven et est intégré au cœur de Maven.
#### Localiser le pom parent 🔍
Si le pom parent ne se situe pas dans le dossier parent, il faut le préciser en utilisant  le tag `<relativePath>`  qui sert à indiquer l'emplacement du POM parent par rapport au POM actuel.

- Si la balise est omise, Maven cherchera par défaut dans le répertoire parent du projet actuel.
- Une valeur vide (`<relativePath/>`) force Maven à chercher le parent dans les repositories (local puis distants) sans chercher dans le système de fichiers local.
- Un chemin spécifique peut être fourni pour indiquer l'emplacement exact du POM parent.

#### Project Aggregation et Héritage 👵

##### Héritage de projets

L'héritage est défini dans le POM enfant, qui spécifie son parent. Il permet aux projets enfants d'hériter des configurations, dépendances et propriétés du POM parent. Donc l'approche est de bas en haut : l'enfant fait référence au parent. L'héritage est utilisé pour partager des configurations communes entre plusieurs projets.

Dans le pom xml on va utiliser la balise `<parent>` pour spécifier de quels pom parents il hérite.
##### Agrégation de projets 

L'agrégation est définie dans le POM parent, qui spécifie ses modules enfants et permet de regrouper plusieurs projets (modules) sous un projet parent. Ici, l'approche est de haut en bas : le parent liste ses modules. L'aggrégation va davantage être utilisée pour construire ou traiter un groupe de projets ensemble.

Dans le pom xml on va utiliser la balise `<module>` pour lister les modules enfants.

### Ressources 📚
**An example of parent pom and child pom:**
https://howtodoinjava.com/maven/maven-parent-child-pom-example/#:~:text=Maven%20parent%20POM%20

**Inheritance and aggregation:**
https://medium.com/@lavishj77/maven-project-inheritence-and-project-aggregation-571975b7f807#:~:text=Also%20it%20is%20possible%20to,in%20the%20child%20module's%20pom

**Le contenu de spring boot dependencies:** 
https://central.sonatype.com/artifact/org.springframework.boot/spring-boot-dependencies

![[Pasted image 20240906164007.png]]