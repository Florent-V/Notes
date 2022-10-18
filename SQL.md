# Notes SQL

## Tables of contents

1. [Installation de MySQL](#installation-de-mysql)
2. [Création d'une base de données](#création-dune-base-de-donnée)
3. [Récupérer les informations d'une BDD](#récupérer-les-informations)
4. [Manipuler les données](#manipuler-les-données)
4. [Bilan](#bilan)


##### [Return to Top](#notes-sql)
# **Installation de MySQL**

D'abord on installe :
``` sh
$sudo apt update 
$sudo apt install mysql-server
```

Ensuite on configure :

``` sh
$sudo mysql_secure_installation
```

``` sh
mysql > CREATE USER 'USERNAME_OF_YOUR_CHOICE'@'localhost' IDENTIFIED WITH caching_sha2_password BY 'PASSWORD_OF_YOUR_CHOICE_TO_NEVER_FORGET';
mysql > GRANT ALL PRIVILEGES ON * . * TO 'USERNAME_OF_YOUR_CHOICE'@'localhost';
mysql > FLUSH PRIVILEGES;
```

Pour se connecter à notre base de donnée :

``` sh
$mysql -u USERNAME_YOU_CHOOSE_JUST_BEFORE -p
```

Pour se connecter à une base de donnée précise :

``` sh
$mysql -u USERNAME_YOU_CHOOSE_JUST_BEFORE -D wizard -p
```
##### [Return to Top](#notes-sql)
# **Création d'une base de donnée**

* Importer une BDD existante

``` sh
mysql> source ~/path/to/file.sql
```

* Créer une base de données :
``` sql
CREATE DATABASE wild;
```
On peut également préciser l'encodage des caractères :

``` sql
CREATE DATABASE maBase DEFAULT CHARACTER SET utf8mb4;
```


Il existe en plus du set de caractère ce qu'on appelle l'interclassement ou collation. Elle précise au set de caractères les spécificités d'une langue. Par exemple que le "E" est semblable au "e" ou au "é".

Pour consulter les charset disponibles
``` sql
SHOW CHARACTET SET;
```
Pour consulter les collations disponibles
``` sql
SHOW COLLATION
```
Voici un exemple de définition pour l’UTF-8 avec une collation unicode multilingue insensible à la casse :
``` sql
CREATE DATABASE maBase DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

La commande générique est donc la suivante :
``` sql
CREATE DATABASE db_name [DEFAULT CHARACTER SET character_set_name [COLLATE collation_name]];
```

* Se placer dans une BDD :
``` sql
USE wild;
```

* Créer une table dans une BDD :

La syntaxe générale est la suivante :

``` sql
CREATE TABLE nom_table (
    colonne_1 type de champs [NULL | NOT NULL] [AUTO_INCREMENT] [DEFAULT 'valeur'],
    [colonne_2 type de champs [NULL | NOT NULL] [AUTO_INCREMENT] [DEFAULT 'valeur']]
    …
    [PRIMARY KEY (nom_colonne)]
    [DEFAULT CHARACTER SET character_set_name [COLLATE collation_name]]
)
[ENGINE = MYISAM | INNODB];
```

Exemple :

``` sql
CREATE TABLE `wizard` (
  `id` INT NOT NULL AUTO_INCREMENT,
  `firstname` VARCHAR(100) NOT NULL,
  `lastname` VARCHAR(100) NOT NULL,
  `birthday` DATE NOT NULL,
  `birth_place` VARCHAR(255) NULL,
  `biography` TEXT NULL
  PRIMARY KEY (`id`)
);
```

* Importer une BDD existante

``` sh
mysql> source ~/path/to/file.sql
```

* Voir les BDD de l'utilisateurs :
``` sql
SHOW DATABASES;
```
* Voir les tables d'une BDD :
``` sql
SHOW TABLES;
```
* Voir la description d'une table :

On voit les différents champs de la table.
``` sql
DESCRIBE wizard;
```
##### [Return to Top](#notes-sql)
# **Récupérer les informations**

* La commande SELECT

La syntaxe de base est la suivante :
``` sql
SELECT <champs> FROM <table>;
```
``` sql
SELECT colonne1, [colonne2, …]
FROM nom_table
[WHERE arguments [ORDER BY DESC|ASC]] [LIMIT un_nombre [OFFSET un_nombre]]
```
Pour récupérer toutes les données d'une table :
``` sql
SELECT * FROM wizard;
```
Pour ne récupérer que des champs en particulier :
``` sql
SELECT firstname, lastname FROM wizard;
```
Utiliser des alias plutôt que le nom des champs :
``` sql
SELECT lastname AS student_name FROM wizard;
```

* La clause WHERE

``` sql
SELECT firstname, birthday FROM wizard WHERE lastname='Weasley';
```
On peut également 

| utiliser les signe `!=, >, <, >!, <=`.

| choisir une valeur parmi plusieurs possible avec `IN`, une valeur numérique (ou une date) dans une fourchette avec `BETWEEN xx AND yy`.

| viser une chaîne commençant ou finissant par avec `LIKE et %`

| une valeur `IS NULL` ou `IS NOT NULL`

On peut également combiner les conditions avec `AND` et `OR`

``` sql
SELECT firstname, birthday 
FROM wizard 
WHERE 
lastname LIKE 'Weas%' AND
birthday BETWEEN '1970-01-01' AND '2000-01-01';
```
Autre exemple :
``` sql
SELECT *
FROM films
WHERE format = 'mp4' OR format = 'webm';
```

* ORDER / LIMIT

Pour limiter le nombre de résultats :
``` sql
SELECT <champs> FROM <table> LIMIT <nb_results>;
```
``` sql
SELECT * FROM wizard LIMIT 5;
```
Associée à la clause `OFFSET`, la clause `LIMIT` peut être très utilise pour une pagination. Par défaut, la LIMIT renvoie les résultats à partir du 1er trouvé (résultat 0). L'OFFSET permet d'indiquer que la LIMIT d'appliqera à oartir du Nième trouvé :

``` sql
SELECT * FROM wizard LIMIT 5 OFFSET 20;
```
Autre exemple :
``` sql
SELECT *
FROM films
WHERE format = 'mp4' OR format = 'webm'
ORDER BY titre;
```

* Le tri ascendant ou descendant

``` sql
SELECT firstname, lastname FROM wizard ORDER BY lastname ASC, birthday DESC;
```
On n'est pas obligé d'afficher les champs qui nous servent à trier. Ici la date de naissance.
``` sql
SELECT * FROM wizard WHERE lastname='Weasley' ORDER BY birthday DESC LIMIT 0,3;
```
Autre exemple :
``` sql
SELECT *
FROM films
WHERE format = 'mp4' OR format = 'webm'
ORDER BY id DESC;
```

* Eliminer les doublons : DISTINCT

Si on veut savoir tous les âges représentés par les membres de notre site :
``` sql
SELECT ages
FROM membres
ORDER BY ages;
```
Avec cette commande on affichera tous les membres, ce n'est pas très pratique pour une vue d'ensemble.
``` sql
SELECT DISTINCT ages
FROM membres
ORDER BY ages;
```
On aura donc la liste de tous les âges représentés par les membres de notre site, sans doublons, et par ordre croissant.

##### [Return to Top](#notes-sql)
# **Manipuler les données**

* Ajouter des données : INSERT

La syntaxe est la suivante :

``` sql
INSERT INTO table (col1, col2, ...) VALUES ('valeur1', 'valeur2', ...);
```
Pour ajouter une valeur dans la table school  :

``` sql
INSERT INTO school (name, country, capacity) VALUES ('Hogwarts School of Witchcraft and Wizardry', 'United Kingdom', 400);
```

On peut également en ajouter plusieurs en même temps :
``` sql
INSERT INTO school (name, country, capacity) 
VALUES ('Beauxbatons Academy of Magic', 'France', 550), 
('Castelobruxo', 'Brazil', 380), 
('Durmstrang Institute', 'Norway', 570);
```

* Modifer les données : UPDATE

La syntaxe est la suivante :

``` sql
UPDATE <table>
SET colonne1 = valeur1, colonne2 = valeur2, etc...
WHERE <conditions>;
```
Il faut faire attention à ne pas oublier la clause `WHERE` sinon toutes les données de la table seront modifiées.

Exemple : pour modifier la capacité d'une école qui a l'iD 1 :

``` sql
UPDATE school
SET capacity = 450
WHERE id = 1;
```

La plupart du temps on ne souhaite modifier qu'une valeur donc on utilise la clé primaire pour s'assumer de n'identifier que cette ligne.

* Supprimer des données : DELETE

La syntaxe est la suivante :

``` sql
DELETE FROM <table>
WHERE <conditions>;
```
Comme pour `UPDATE`, il faut faire attention à ne pas oublier la clause `WHERE` pour ne pas supprimer toutes les données de la table.

Exemple :

``` sql
DELETE FROM school
WHERE id = 3;
```
Ou encore :

``` sql
DELETE FROM school
WHERE capacity > 500;
```
* La commande TRUNCATE

Pour vider une table de toutes ses données, on utilise la commande `TRUNCATE`. Cela ne supprimer pas la structure de la table. Cette commande est plus performante qu'un `DELETE`.  
De plus `TRUNCATE` réinitialise l'auto-incrémentation, ce qui n'est pas le cas de `DELETE`.

``` sql
TRUNCATE school;
```
* Modifier une table : ALTER

Pour modifier des éléments de la base de données :
``` sql
ALTER DATABASE nom_de_la_base CHARACTER SET character_set_name COLLATE collation_name;
```

Ajouter une colonne :
``` sql
ALTER TABLE test
ADD nom_colonne desc [AFTER colonne];
```

Supprimer une colonne :
``` sql
ALTER TABLE test DROP COLUMN nom;
```

Changer et renommer une colonne :
``` sql
ALTER TABLE nom_table
CHANGE nom_colonne nouveau_nom_colonne TYPE [NULL|NOT NULL] [AUTO_INCREMENT];
```

* La commande DROP
Pour supprimer une base de données :
``` sql
DROP DATABASE nom_de_la_base;
```

* La commande RENAME
Pour renommer une table :
``` sql
RENAME TABLE ancien_nom TO nouveau_nom;
```

##### [Return to Top](#notes-sql)
# **Bilan**
## Création base, table et insertion de valeur :
``` sql
CREATE DATABASE checkpoint1;
USE checkpoint1;
CREATE TABLE bribe (
    `id` INT PRIMARY KEY AUTO_INCREMENT NOT NULL, 
    `name` VARCHAR(100) NOT NULL, 
    `payment` INT NOT NULL
    );

INSERT INTO bribe (name, payment) 
VALUES ('Alexandre D', 250),
('Jessica P', 500),
('Maxence H', 1200),
('Megane P', 850),
('Axel C', 1500),
('Marine V', 1400);
```


##### [Return to Top](#notes-sql)
# **Les bases de la modélisation**



``` sql

```
[u]Texte[/u]
<color=red>Texte</color> / [color=#FF3300]Texte[/color]

<font color=red>Texte</font>

[size=3]Texte[/size]

*TODO*

Commande   ==ALTER== 


### qfsdf
#### qfsfsfsfd
##### qfsfsfsfd
###### qfsfsfsfd
fsfsfs