
- Pour éliminer les redondances
- pour mieux comprendre les relations sémantiques entre les données
- pour éviter les incohérences de mise à jour
- pour éviter, autant que possible, les valeurs nulles
- Insertion d’une personne sans voiture => introduction de valeurs nulles
- Pour éviter la perte d’information
- Suppression de la dernière voiture possédée par une personne => perte d’information
## 1FN
***Une relation est en 1ère Forme Normale (1FN) si et seulement si tous ses attributs sont atomiques (non composés et mono-valués).***

**Exemples** :
`PERSONNE (NOM, PRENOMS)`
⇒  Mise en 1FN : `PERSONNE1 (NOM, PRENOM1, PRENOM2)`

`PERSONNE (NOM, PRENOM, ADRESSE)`
⇒  Mise en 1FN : `PERSONNE2 (NOM, PRENOM, N°RUE, RUE, CODEPOSTAL, VILLE)`

## 2FN
Une relation est en deuxième forme normale (2FN) si :
1. elle est en 1 FN
2. tout attribut n'appartenant pas à la clé dépend uniquement de la totalité de la clé

**Exemple:**
Avec `NumPropriétaire` et `NumVehicule` les clés primaires, 
`R(*NumPropriétaire, *NumVehicule, Nom, Ville, Marque, Date)` **n'est pas en 2FN**

`Nom` dépend que de `NumPropriétaire`
`Ville` dépend que de `NumPropriétaire`
`Marque` ne dépend que de `NumVéhicule` 
`Date` dépend de la totalité de la clé


