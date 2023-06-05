# BDD-PHP-DATAVIZ.

Qu'est ce qu'un SGBD ?
-----
SGBD (système de gestion de base de données) est le logiciel qui permet a l'ordinateur de stocker, modifier, récupérer ou supprimer des données.

Qu'est ce qu'un système d'informations ?
-----
Le système d'information (SI) est un ensemble de ressources et de dispositifs permettant de collecter, stocker, traiter et diffuser les informations nécessaires au fonctionnement d'une organisation (administration, entreprise…).

Qu'est ce qu'une base de données ?
-----
Ensemble d'informations structurées accessibles au moyen d'un logiciel.
Les bases de données permettent aux utilisateurs de centraliser et partagés leurs informations à tout moment. Par conséquent, si vous avez une entreprise avec des sites différents, vous pouvez partager vos données en même temps avec les différents sites commerciaux.

Les différences SQD - SI - BASE DE DONNÉES
-----
le SGBD est le logiciel qui permet de gérer les bases de données, la base de données est l'ensemble des données structurées stockées, tandis que le système d'information est un ensemble plus large qui englobe la base de données ainsi que les ressources et les processus nécessaires pour collecter, traiter et distribuer les informations au sein d'une organisation.

Qu'est ce qu'un MCD ?
-----
Également appellé modèle conceptuel de données, il s'agit d'une répresentation claire des données du système d'information à concevoir.
Cette représentation en outre figure les relations entre ces données.

Comment représenter une entité ?
-----
La plupart du temps avec un rectangle sur un site ou un logiciel (draw.io ...)

Comment représenter une liaison entre des entités ?
-----

Pour représenter une liaison entre des entités dans un schéma conceptuel, on utilise généralement des symboles et des notations spécifiques. Les deux notations les plus couramment utilisées sont le modèle Entité-Association (E/A) et le modèle Relationnel.

Modèle Entité-Association (E/A):
Dans le modèle E/A, les entités sont représentées par des rectangles et les liaisons entre les entités sont représentées par des lignes avec des indicateurs de cardinalité.
Une liaison 1 à 1 est représentée par une ligne sans indicateurs de cardinalité.
Une liaison 1 à plusieurs (1:N) est représentée par une flèche partant de l'entité "1" vers l'entité "N" avec un indicateur "1" du côté de l'entité "1" et un indicateur "N" du côté de l'entité "N".
Une liaison plusieurs à plusieurs (N:N) est représentée par deux flèches partant de chaque entité "N" et se rejoignant avec les indicateurs "N" des deux côtés.

Modèle Relationnel:
Dans le modèle relationnel, les entités sont représentées par des tables et les liaisons entre les entités sont représentées par des clés étrangères.
Une liaison 1 à 1 est représentée en ajoutant une clé étrangère d'une table à une autre table.
Une liaison 1 à plusieurs (1:N) est représentée en ajoutant une clé étrangère de la table "1" à la table "N".
Une liaison plusieurs à plusieurs (N:N) est représentée en créant une table de liaison supplémentaire qui contient les clés étrangères des deux entités.

Où mettre les données qui composent nos entités ?
-----
Les données qui composent les entités sont généralement stockées dans une base de données. Une base de données est un système de stockage structuré qui permet de stocker, organiser et gérer efficacement les données. Elle offre une méthode centralisée pour stocker et accéder aux données de manière cohérente.

Quels sont les différents types de cardinalité possibles ? Où les placer dans notre schéma ?
-----
Cardinalité Un à Un (1:1) : Cela signifie qu'une occurrence d'une entité est associée à une seule occurrence de l'autre entité, et vice versa. Dans un schéma Entité-Association (E/A), cette cardinalité est représentée par une ligne simple sans indicateurs de cardinalité entre les entités liées.

Cardinalité Un à Plusieurs (1:N) : Cela signifie qu'une occurrence d'une entité est associée à plusieurs occurrences de l'autre entité, mais qu'une occurrence de l'autre entité est associée à une seule occurrence de la première entité. Dans un schéma E/A, cette cardinalité est représentée par une flèche partant de l'entité "1" vers l'entité "N", avec l'indicateur "1" du côté de l'entité "1" et l'indicateur "N" du côté de l'entité "N".

Cardinalité Plusieurs à Plusieurs (N:N) : Cela signifie que plusieurs occurrences d'une entité peuvent être associées à plusieurs occurrences de l'autre entité, et vice versa. Dans un schéma E/A, cette cardinalité est représentée par deux flèches partant de chaque entité "N" et se rejoignant, avec l'indicateur "N" des deux côtés.

Les indicateurs de cardinalité sont généralement placés près des lignes qui représentent les relations entre les entités dans un schéma E/A. Ils indiquent le nombre minimum et maximum d'occurrences permises dans chaque direction de la relation.

Citer quelques bonnes pratiques de normalisation : 
-----
Première forme normale (1NF) : Chaque table doit avoir une clé primaire unique, et chaque colonne d'une table doit contenir une seule valeur atomique. Éliminez les valeurs répétées et les groupes de valeurs similaires en créant des tables distinctes.

Deuxième forme normale (2NF) : Assurez-vous que chaque colonne non clé d'une table dépend entièrement de la clé primaire de cette table. Si une colonne dépend partiellement de la clé primaire, déplacez-la vers une autre table où elle dépend entièrement de la clé.

Troisième forme normale (3NF) : Éliminez les dépendances transitives, c'est-à-dire les dépendances où une colonne dépend d'une autre colonne qui dépend elle-même de la clé primaire. Déplacez les dépendances transitives vers des tables distinctes pour atteindre la 3NF.

Forme normale de Boyce-Codd (BCNF) : Si une table contient des dépendances fonctionnelles non triviales où une colonne détermine une autre colonne qui n'est pas sa clé, décomposez la table en plusieurs tables pour atteindre la BCNF.

Cinquième forme normale (5NF) : Si une table présente des dépendances de jointure multivaluées, décomposez-la en plusieurs tables pour éliminer ces dépendances.

Éviter les redondances : Éliminez les redondances de données en normalisant correctement les tables. Stocker les données une seule fois et référencer les informations à l'aide de clés étrangères.

Utilisation de clés étrangères : Établissez des relations entre les tables à l'aide de clés étrangères pour garantir l'intégrité référentielle et maintenir la cohérence des données.

Éviter les attributs calculés : Évitez de stocker des attributs calculés dans les tables, car cela peut entraîner des incohérences lorsque les données sous-jacentes sont mises à jour. Calculez les valeurs au moment de la requête si nécessaire.

Performance et optimisation : Considérez les exigences de performance et d'accessibilité des données lors de la conception du schéma de base de données. Indexez les colonnes fréquemment utilisées et optimisez les requêtes pour améliorer les performances.

Maintenance et évolutivité : Concevez le schéma de base de données de manière à faciliter la maintenance future et l'ajout de nouvelles fonctionnalités. Anticipez les changements futurs et réfléchissez à l'évolutivité du schéma.

A quoi servent les clés primaires ?
-----

Les clés primaires sont essentielles pour l'identification unique des enregistrements, l'établissement de relations entre les tables, l'indexation des données, l'application de contraintes et la création de références externes. Elles sont au cœur de la structure et de la cohérence d'une base de données relationnelle.

Comment passer d'un MCD au MLD ? Que deviennent les associations ?
-----

Pour passer d'un Modèle Conceptuel des Données (MCD) à un Modèle Logique des Données (MLD), vous devez transformer les entités, les associations et les attributs du MCD en tables, relations et colonnes respectivement dans le MLD.

Les propriétés propres de l'association deviennent des attributs de cette relation.
L'association devient une relation ayant comme clé la concaténation des clés des relations associées à chaque individuassociation devient une relation ayant comme clé la concaténation des clés des relations associées à chaque individu.


 
 
