Initiation au SQL :
-----

Comment créer une base de données ?
-----

En ligne de commande. En écrivant des requêtes SQL à la main.
En interface graphique (avec PhpMyAdmin). Il faut simplement cliquer sur des boutons et remplir les champs nécessaires.

Comment faire un commentaire ?
-----

En précédant les commentaires de -- pour les commentaires mono-ligne.
En encadrant les commentaires entre /* et */ pour les commentaires multi-lignes.

Comment créer une table et des colonnes ?
-----

Utiliser la syntaxe SQL standard de la commande CREATE TABLE : CREATE TABLE nom_table ( column1 data_type, column2 data_type, … ) 

Listez les types de données que vous utiliserez le plus souvent.
-----

Les principaux types de données en SQL sont :

CHARACTER (ou CHAR) : valeur alpha de longueur fixe.

CHARACTER VARYING (ou VARCHAR) : valeur alpha de longueur maximale fixée.

TEXT : suite longue de caractères (sans limite de taille).

NUMERIC (ou DECIMAL ou DEC) : décimal

INTEGER (ou INT) : entier long

REAL : réel à virgule flottante dont la représentation est binaire.

BOOLEAN (ou LOGICAL) : vrai/faux

DATE : date du calendrier grégorien.
