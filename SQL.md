# Notes SQL

- [Notes SQL](#notes-sql)
- [1. **Installation de MySQL**](#1-installation-de-mysql)
- [2. **Création d'une base de donnée**](#2-création-dune-base-de-donnée)
  - [2.1. Importer une BDD existante](#21-importer-une-bdd-existante)
  - [2.2. Voir les BDD de l'utilisateurs :](#22-voir-les-bdd-de-lutilisateurs-)
  - [2.3. Voir les tables d'une BDD :](#23-voir-les-tables-dune-bdd-)
  - [2.4. Voir la description d'une table :](#24-voir-la-description-dune-table-)
  - [2.5. Créer une base de données :](#25-créer-une-base-de-données-)
  - [2.6. Créer une table dans une BDD :](#26-créer-une-table-dans-une-bdd-)
    - [2.6.1. Se placer dans une BDD :](#261-se-placer-dans-une-bdd-)
    - [2.6.2. Utiliser la syntaxe générale suivante :](#262-utiliser-la-syntaxe-générale-suivante-)
    - [2.6.3. Exemples](#263-exemples)
- [3. **Récupérer les informations**](#3-récupérer-les-informations)
  - [3.1. La commande SELECT](#31-la-commande-select)
    - [3.1.1. Syntaxe de base](#311-syntaxe-de-base)
    - [3.1.2. Récupérer toutes les données d'une table](#312-récupérer-toutes-les-données-dune-table)
    - [3.1.3. Ne récupérer que des champs en particulier](#313-ne-récupérer-que-des-champs-en-particulier)
    - [3.1.4. Utiliser des alias plutôt que le nom des champs](#314-utiliser-des-alias-plutôt-que-le-nom-des-champs)
  - [3.2. La clause WHERE](#32-la-clause-where)
    - [3.2.1. Syntaxe de base](#321-syntaxe-de-base)
    - [3.2.2. Exemples](#322-exemples)
  - [3.3. ORDER / LIMIT](#33-order--limit)
    - [3.3.1. Syntaxe de base](#331-syntaxe-de-base)
    - [3.3.2. Autre exemple :](#332-autre-exemple-)
  - [3.4. Eliminer les doublons : DISTINCT](#34-eliminer-les-doublons--distinct)
- [4. **Manipuler/Modifier les données**](#4-manipulermodifier-les-données)
  - [4.1. Modifier une table : ALTER](#41-modifier-une-table--alter)
  - [4.2. Ajouter un champ : ALTER TABLE + ADD](#42-ajouter-un-champ--alter-table--add)
  - [4.3. Modifier un champ : ALTER TABLE + MODIFY](#43-modifier-un-champ--alter-table--modify)
  - [4.4. Supprimer un champ : ALTER TABLE + DROP](#44-supprimer-un-champ--alter-table--drop)
  - [4.5. Ajouter des données : INSERT](#45-ajouter-des-données--insert)
  - [4.6. Modifer les données : UPDATE](#46-modifer-les-données--update)
  - [4.7. Supprimer les données : DELETE](#47-supprimer-les-données--delete)
  - [4.8. Renommer une table : RENAME](#48-renommer-une-table--rename)
  - [4.9. Supprimer un champ](#49-supprimer-un-champ)
  - [4.10. Vider une table : TRUNCATE](#410-vider-une-table--truncate)
  - [4.11. Supprimer une table](#411-supprimer-une-table)
  - [4.12. Supprimer la BDD](#412-supprimer-la-bdd)
  - [4.13. Exporter la BDD](#413-exporter-la-bdd)
- [5. **Bilan**](#5-bilan)
  - [5.1. Création base, table et insertion de valeur](#51-création-base-table-et-insertion-de-valeur)
- [6. **Les bases de la modélisation**](#6-les-bases-de-la-modélisation)
  - [6.1. MODELISATION CONCEPTUELLEE DE DONNEES (MCD)](#61-modelisation-conceptuellee-de-donnees-mcd)
    - [6.1.1. **Les entités :**](#611-les-entités-)
    - [6.1.2. **Les relations :**](#612-les-relations-)
    - [6.1.3. **Les cardinalités :**](#613-les-cardinalités-)
  - [6.2. Passage de la MCD à la MLD (Modèle Logique de Données)](#62-passage-de-la-mcd-à-la-mld-modèle-logique-de-données)
    - [6.2.1. **1. Many To One (1-N)**](#621-1-many-to-one-1-n)
    - [6.2.2. **2. One To One (1-1)**](#622-2-one-to-one-1-1)
    - [6.2.3. **3. Many To Many (N-M)**](#623-3-many-to-many-n-m)
  - [6.3. Modèle Physique de Données (MPD)](#63-modèle-physique-de-données-mpd)
    - [6.3.1. Les clés étrangères](#631-les-clés-étrangères)
    - [6.3.2. **1. Many To One (1-N)**](#632-1-many-to-one-1-n)
      - [6.3.2.1. Exemples :](#6321-exemples-)
      - [6.3.2.2. New Table With 2 Foreign Keys](#6322-new-table-with-2-foreign-keys)
      - [6.3.2.3. Add Data in Table](#6323-add-data-in-table)
    - [6.3.3. **2. One To One (1-1)**](#633-2-one-to-one-1-1)
    - [6.3.4. **3. Many To Many (N-M)**](#634-3-many-to-many-n-m)
    - [6.3.5. Les contraintes d'intégrité](#635-les-contraintes-dintégrité)
- [7. **Les Jointures**](#7-les-jointures)
  - [7.1. INNER JOIN](#71-inner-join)
    - [7.1.1. Syntaxe](#711-syntaxe)
    - [7.1.2. Exemple](#712-exemple)
    - [7.1.3. Utilisation des Alias](#713-utilisation-des-alias)
    - [7.1.4. Autres Exemples](#714-autres-exemples)
  - [7.2. Jointures Avancées](#72-jointures-avancées)
  - [7.3. Join Multiple Tables](#73-join-multiple-tables)
  - [7.4. LEFT JOIN \& RIGTH JOIN](#74-left-join--rigth-join)
  - [7.5. UNION](#75-union)
- [8. **SQL Avancé**](#8-sql-avancé)
  - [8.1. WHERE Avancée](#81-where-avancée)
    - [8.1.1. **AND/OR**](#811-andor)
    - [8.1.2. **LIKE**](#812-like)
    - [8.1.3. **BETWEEN**](#813-between)
    - [8.1.4. **IS NULL/IS NOT NULL**](#814-is-nullis-not-null)
    - [8.1.5. **IN** :](#815-in-)
  - [8.2. Fonctions SQL](#82-fonctions-sql)
    - [8.2.1. **DISTINCT**](#821-distinct)
    - [8.2.2. **CONCAT**](#822-concat)
    - [8.2.3. **LENGTH**](#823-length)
  - [8.3. Fonctions Mathématiques](#83-fonctions-mathématiques)
    - [8.3.1. **RAND**](#831-rand)
    - [8.3.2. **ROUND**](#832-round)
    - [8.3.3. **Autres fonctions mathématiques**](#833-autres-fonctions-mathématiques)
  - [8.4. Fonctions Date](#84-fonctions-date)
    - [8.4.1. **NOW()**](#841-now)
    - [8.4.2. **MONTH()**](#842-month)
    - [8.4.3. **DATEDIFF()**](#843-datediff)
  - [8.5. Fonctions D'agrégation](#85-fonctions-dagrégation)
    - [8.5.1. **COUNT()**](#851-count)
    - [8.5.2. **SUM()**](#852-sum)
    - [8.5.3. **MAX()**](#853-max)
    - [8.5.4. **MIN()**](#854-min)
    - [8.5.5. **AVG()**](#855-avg)
    - [8.5.6. Exemples](#856-exemples)
  - [8.6. GROUP BY / HAVING](#86-group-by--having)
  - [8.7. Administration avancée](#87-administration-avancée)
  - [8.8. Administration avancée](#88-administration-avancée)
- [9. **Main Title**](#9-main-title)
  - [9.1. Subtitle](#91-subtitle)
    - [9.1.1. qfsdf](#911-qfsdf)
      - [9.1.1.1. qfsfsfsfd](#9111-qfsfsfsfd)



[Return to Top](#notes-sql)
# 1. **Installation de MySQL**

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

Depuis root :
``` sh
$mysql -u root -p
```

Pour se connecter à une base de donnée précise :

``` sh
$mysql -u USERNAME_YOU_CHOOSE_JUST_BEFORE -D wizard -p
```

show Grants
```sql
SHOW GRANTS FOR 'someuser'@'localhost';
```

Remove Grants
```sql
REVOKE ALL PRIVILEGES, GRANT OPTION FROM 'someuser'@'localhost';
```

Delete User
```sql
DROP USER 'someuser'@'localhost';
```

Exit
```sql
exit;
```

[Return to Top](#notes-sql)
# 2. **Création d'une base de donnée**

## 2.1. Importer une BDD existante

``` sh
mysql> source ~/path/to/file.sql
```

## 2.2. Voir les BDD de l'utilisateurs :
``` sql
SHOW DATABASES;
```

## 2.3. Voir les tables d'une BDD :
``` sql
SHOW TABLES;
```

## 2.4. Voir la description d'une table :
On voit les différents champs de la table.
``` sql
DESCRIBE wizard;
```

## 2.5. Créer une base de données :
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

## 2.6. Créer une table dans une BDD :

### 2.6.1. Se placer dans une BDD :
``` sql
USE wild;
```

### 2.6.2. Utiliser la syntaxe générale suivante :

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

### 2.6.3. Exemples

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

``` sql
CREATE TABLE users(
id INT AUTO_INCREMENT,
   first_name VARCHAR(100),
   last_name VARCHAR(100),
   email VARCHAR(50),
   password VARCHAR(20),
   location VARCHAR(100),
   dept VARCHAR(100),
   is_admin TINYINT(1),
   register_date DATETIME,
   PRIMARY KEY(id)
);
```

* Create & Remove Index

```sql
CREATE INDEX LIndex On users(location);
DROP INDEX LIndex ON users;
```

[Return to Top](#notes-sql)
# 3. **Récupérer les informations**

## 3.1. La commande SELECT

### 3.1.1. Syntaxe de base

``` sql
SELECT <champs> FROM <table>;
```
``` sql
SELECT colonne1, [colonne2, …]
FROM nom_table
[WHERE arguments [ORDER BY DESC|ASC]] [LIMIT un_nombre [OFFSET un_nombre]]
```

### 3.1.2. Récupérer toutes les données d'une table

``` sql
SELECT * FROM wizard;
SELECT * FROM users;
```

### 3.1.3. Ne récupérer que des champs en particulier

``` sql
SELECT firstname, lastname FROM wizard;
SELECT first_name, last_name FROM users;
```

### 3.1.4. Utiliser des alias plutôt que le nom des champs

``` sql
SELECT lastname AS student_name FROM wizard;
```

## 3.2. La clause WHERE

### 3.2.1. Syntaxe de base

``` sql
SELECT firstname, birthday FROM wizard WHERE lastname='Weasley';
```
> On peut également :
> - Utiliser les signe `!=, >, <, >!, <=`.
> - Choisir une valeur parmi plusieurs possible avec `IN`, une valeur numérique (ou une date) dans une fourchette avec `BETWEEN xx AND yy`.
> - Viser une chaîne commençant ou finissant par avec `LIKE et %`
une valeur `IS NULL` ou `IS NOT NULL`
> - Combiner les conditions avec `AND` et `OR`


### 3.2.2. Exemples

``` sql
SELECT firstname, birthday 
FROM wizard 
WHERE 
lastname LIKE 'Weas%' AND
birthday BETWEEN '1970-01-01' AND '2000-01-01';
```

```sql
SELECT * FROM users WHERE age BETWEEN 20 AND 25;
```

``` sql
SELECT *
FROM films
WHERE format = 'mp4' OR format = 'webm';
```

```sql
SELECT * FROM users WHERE location='Massachusetts';
SELECT * FROM users WHERE location='Massachusetts' AND dept='sales';
SELECT * FROM users WHERE is_admin = 1;
SELECT * FROM users WHERE is_admin > 0;
```

```sql
SELECT * FROM users WHERE dept LIKE 'd%';
SELECT * FROM users WHERE dept LIKE 'dev%';
SELECT * FROM users WHERE dept LIKE '%t';
SELECT * FROM users WHERE dept LIKE '%e%';
```

```sql
SELECT * FROM users WHERE dept NOT LIKE 'd%';
```

```sql
SELECT * FROM users WHERE dept IN ('design', 'sales');
```

## 3.3. ORDER / LIMIT

### 3.3.1. Syntaxe de base

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

### 3.3.2. Autre exemple :
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

## 3.4. Eliminer les doublons : DISTINCT

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

[Return to Top](#notes-sql)

# 4. **Manipuler/Modifier les données**

## 4.1. Modifier une table : ALTER

Pour modifier des éléments de la base de données :
``` sql
ALTER DATABASE nom_de_la_base CHARACTER SET character_set_name COLLATE collation_name;
```

## 4.2. Ajouter un champ : ALTER TABLE + ADD

``` sql
ALTER TABLE Nom_de_la_table 
ADD Nom_de_la_colonne Type_de_donnees desc [AFTER colonne];
```

```sql
ALTER TABLE users ADD age VARCHAR(3);
```

## 4.3. Modifier un champ : ALTER TABLE + MODIFY

Ici on préciser le nom du champ à modifier.
``` sql
ALTER TABLE Nom_de_la_table
MODIFY Nom_de_la_colonne Type_de_donnees
```
Changer et renommer une colonne :
``` sql
ALTER TABLE nom_table
CHANGE nom_colonne nouveau_nom_colonne TYPE [NULL|NOT NULL] [AUTO_INCREMENT];
```

```sql
ALTER TABLE users MODIFY COLUMN age INT(3);
```
## 4.4. Supprimer un champ : ALTER TABLE + DROP

Ici on préciser le nom du champ à modifier.
``` sql
ALTER TABLE Nom_de_la_table
DROP COLUMN Nom_de_la_colonnE
```
## 4.5. Ajouter des données : INSERT

La syntaxe est la suivante :

``` sql
INSERT INTO table (col1, col2, ...) VALUES ('valeur1', 'valeur2', ...);
```
Pour ajouter une valeur dans la table school  :

``` sql
INSERT INTO school (name, country, capacity) VALUES ('Hogwarts School of Witchcraft and Wizardry', 'United Kingdom', 400);
```

```sql
INSERT INTO users (first_name, last_name, email, password, location, dept, is_admin, register_date) values ('Brad', 'Traversy', 'brad@gmail.com', '123456','Massachusetts', 'development', 1, now());
```

On peut également en ajouter plusieurs en même temps :
``` sql
INSERT INTO school (name, country, capacity) 
VALUES ('Beauxbatons Academy of Magic', 'France', 550), 
('Castelobruxo', 'Brazil', 380), 
('Durmstrang Institute', 'Norway', 570);
```

```sql
INSERT INTO users (first_name, last_name, email, password, location, dept,  is_admin, register_date) values ('Fred', 'Smith', 'fred@gmail.com', '123456', 'New York', 'design', 0, now()), ('Sara', 'Watson', 'sara@gmail.com', '123456', 'New York', 'design', 0, now()),('Will', 'Jackson', 'will@yahoo.com', '123456', 'Rhode Island', 'development', 1, now()),('Paula', 'Johnson', 'paula@yahoo.com', '123456', 'Massachusetts', 'sales', 0, now()),('Tom', 'Spears', 'tom@yahoo.com', '123456', 'Massachusetts', 'sales', 0, now());
```

## 4.6. Modifer les données : UPDATE

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

```sql
UPDATE users SET email = 'freddy@gmail.com' WHERE id = 2;
```

La plupart du temps on ne souhaite modifier qu'une valeur donc on utilise la clé primaire pour s'assumer de n'identifier que cette ligne.

## 4.7. Supprimer les données : DELETE

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
```sql
DELETE FROM users WHERE id = 6;
```

## 4.8. Renommer une table : RENAME

``` sql
RENAME TABLE ancien_nom TO nouveau_nom;
```

## 4.9. Supprimer un champ

``` sql
ALTER TABLE table1
DROP COLUMN colonne2,
DROP COLUMN colonne3;
```
Exemple :
``` sql
ALTER TABLE wizard
DROP COLUMN birthday,
DROP COLUMN biography;
```
## 4.10. Vider une table : TRUNCATE

Pour vider une table de toutes ses données, on utilise la commande `TRUNCATE`. Cela ne supprimer pas la structure de la table. Cette commande est plus performante qu'un `DELETE`.  
De plus `TRUNCATE` réinitialise l'auto-incrémentation, ce qui n'est pas le cas de `DELETE`.

``` sql
TRUNCATE school;
```

## 4.11. Supprimer une table

``` sql
DROP TABLE table1, table2 ;
```
## 4.12. Supprimer la BDD

``` sql
DROP DATABASE test ;
```

## 4.13. Exporter la BDD

``` sql
mysqldump -u [username] -p [database-you-want-to-dump] > [path-to-place-data-dump];
```
Exemple :
``` sql
mysqldump -u florent -p mydatabase > /home/myuser/database-dump.sql
```


[Return to Top](#notes-sql)
# 5. **Bilan**

## 5.1. Création base, table et insertion de valeur

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


[Return to Top](#notes-sql)
# 6. **Les bases de la modélisation**

## 6.1. MODELISATION CONCEPTUELLEE DE DONNEES (MCD)

### 6.1.1. **Les entités :**
Une entité est un regroupement d’éléments ayant les mêmes caractéristiques. Une entité possède des propriétés permettant de caractériser celle-ci :un nom et un prénom pour un élève ; un nom et une capacité pour une école ; un titre et un nombre de pages pour un livre, etc.).   
Il faut également un identifiant unique qui permettra de caractériser sans ambiguïté possible un représentant de cette entité.
![Entités](./img/10.png)

### 6.1.2. **Les relations :**
Ce sont les liens entre deux entités ou plus. Une relation peut parfois posséder elle-même des attributs. En effet, pour l’emprunt, une date peut être associée (pour calculer une date de retour limite).  
Par exemple, pour la bibliothèque de Poudlard, si tu as une entité Wizard et une entité Book, un sorcier va pouvoir interagir avec un livre en empruntant celui-ci.
![Relation](./img/11.png)

### 6.1.3. **Les cardinalités :**
On parle de cardinalités pour décrire le nombre d'interactions possibles entre un élément d’une entité et une autre entité.  
Par exemple, un sorcier ne pourra être inscrit que dans une seule école à la fois (ou ne pas être inscrit du tout) et une école peut accueillir de 0 à N sorciers.   
Pour une association de 2 entités, il y a donc 4 cardinalités à indiquer :
- La cardinalité de la relation Wizard -> School est donc 0-1.
- La cardinalité de la relation School -> Wizard est donc 0-N (N représente un nombre potentiellement infini).

Le sens de la cardinalité est donc important.
![Cardinalités](./img/12.png)

![Exemple](./img/19.png)

![Exemple](./img/20.png)


## 6.2. Passage de la MCD à la MLD (Modèle Logique de Données)

On ne garde que les entités On prend les bornes maximales des cardinalités des deux côtés pour déterminer le type de relation, 3 possibles :

### 6.2.1. **1. Many To One (1-N)**

C’est le cas juste d'un élève inscrit dans 0 ou 1 seule Ecole  alors qu'une école peut inscrire de 0 à N élèves.

Ajout d’une clé étrangère côté “1”. Ce champ prend la valeur d’un champ unique (généralement l’id) de la table côté “n”
![Schéma](./img/21.png)
![Foreign key](./img/25.png)

### 6.2.2. **2. One To One (1-1)**

Une relation unique entre deux entités. Par exemple, un Sorcier ne pourra posséder qu’une et une seule Baguette, et une Baguette n’a qu’un seul Sorcier.

### 6.2.3. **3. Many To Many (N-M)**

Une entité peut interagir avec plusieurs éléments d’une autre entité, et vice versa. Par exemple, un Sorcier peut connaître plusieurs Sortilèges, et un sortilège peut être connu par plusieurs Sorciers en même temps.
Pour cette dernière relation, les cardinalités maximales sont bien N-N mais on écrit plutôt N-M.

Exemple : Plusieurs écoles ET plusieurs langages. On prend les plus grandes cardinalités des deux côtés. L’une des deux “n” devient “m” pour plus de lisibilité.  
Création d’une table de jointure contenant les deux clés étrangères (ce couple de clés peut suffire comme clé primaire de la table de jointure).  
![Schéma](./img/23.png)

Bilan :
![Schéma](./img/24.png)

## 6.3. Modèle Physique de Données (MPD)

Le niveau physique tient compte des particularités de chaque SGBDR :
- Types des données (INT, VARCHAR, CHAR, BOOL…) 
- Contraintes (unique, nullable, auto-incrémentation…)
- ....

Schéma final de base de donées : le nom de l’entité devient un nom de table, les propriétés de l’entité deviennent les champs de la table. Il faut également penser à leur attribuer les bons types (int, varchar, boolean, etc.). Les identifiants deviennent des clés primaires  
![Schéma](./img/26.png)

![Schéma](./img/13.png)


### 6.3.1. Les clés étrangères

Les clés étrangères servent à indiquer à une table qu’elle est reliée à une autre table.  
En règle générale, une clé étrangère fait référence à une clé primaire d’une autre table (puisque la clé primaire permet d’identifier formellement un tuple) mais tu pourrais très bien faire référence à un autre champ “unique” de la table si celle-ci en possède.


Les règles de création des clés étrangères dépendent du type de relation entre les entités.

### 6.3.2. **1. Many To One (1-N)**

C’est le type de relation la plus fréquente et la plus simple à gérer. Un sorcier est dans une seule école (côté 1 de la relation 1-N), mais une école peut recevoir plusieurs sorciers (côté N de la relation 1-N). Dans ce cas, tu ajoutes toujours dans la table ayant la plus faible cardinalité (0 ou 1), ici wizard, la clé étrangère référençant la table de plus haute cardinalité (le N), ici school, qu'on appellera par exemple `school_id`.   

![Foreign key](./img/25.png)

Ainsi, si chaque sorcier aura un champ `school_id` qui aura pour valeur l'id de l'école dans laquelle il est inscrit. Les tables sont donc reliées par les champs `school_id` de la table wizard et `id`de la table school.

Cependant on peut toujours à ce stade affecter un `school_id` à un sorcier d'une école qui n'existerait pas. On peut également supprimer une école et dans ce cas un sorcier se retrouverait avec une école qui n'existerait plus. On se retrouverait alors avec une incohérence dans l’intégrité de tes données, ce qui entraînera à coup sûr divers bugs dans ton application !

Pour pallier ce problème, il existe un type de contrainte appelée clé étrangère ou foreign key. Elle permet d’empêcher une insertion dans la table `wizard` si la valeur du `school_id` associée n’existe pas dans la table school (idem, elle empêche la suppression d’un tuple qui serait relié à des données dans une autre table). Ainsi, cela te protège de nombreuses erreurs. C’est donc indispensable pour conserver des données saines et cohérentes.

Pour définir une contrainte de clé étrangère, une fois le champ `school_id` créé, il faut taper la commande SQL suivante :

#### 6.3.2.1. Exemples :

``` sql
ALTER TABLE wizard
ADD CONSTRAINT fk_wizard_school 
FOREIGN KEY (school_id) 
REFERENCES school(id);
```

``` sql
CREATE TABLE wizard (
    id INT PRIMARY KEY AUTO_INCREMENT,
    firstname VARCHAR(100) NOT NULL,
    lastname VARCHAR(100) NOT NULL,
    school_id INT NOT NULL,
    CONSTRAINT fk_wizard_school      
        FOREIGN KEY (school_id)             
        REFERENCES school(id)    
);
```

```sql
CREATE TABLE posts(
id INT AUTO_INCREMENT,
   user_id INT,
   title VARCHAR(100),
   body TEXT,
   publish_date DATETIME DEFAULT CURRENT_TIMESTAMP,
   PRIMARY KEY(id),
   FOREIGN KEY (user_id) REFERENCES users(id)
);
```
* Add Data to Posts Table

```sql
INSERT INTO posts(user_id, title, body) VALUES (1, 'Post One', 'This is post one'),(3, 'Post Two', 'This is post two'),(1, 'Post Three', 'This is post three'),(2, 'Post Four', 'This is post four'),(5, 'Post Five', 'This is post five'),(4, 'Post Six', 'This is post six'),(2, 'Post Seven', 'This is post seven'),(1, 'Post Eight', 'This is post eight'),(3, 'Post Nine', 'This is post none'),(4, 'Post Ten', 'This is post ten');
```

#### 6.3.2.2. New Table With 2 Foreign Keys

```sql
CREATE TABLE comments(
	id INT AUTO_INCREMENT,
    post_id INT,
    user_id INT,
    body TEXT,
    publish_date DATETIME DEFAULT CURRENT_TIMESTAMP,
    PRIMARY KEY(id),
    FOREIGN KEY(user_id) references users(id),
    FOREIGN KEY(post_id) references posts(id)
);
```
#### 6.3.2.3. Add Data in Table

```sql
INSERT INTO comments(post_id, user_id, body) VALUES (1, 3, 'This is comment one'),(2, 1, 'This is comment two'),(5, 3, 'This is comment three'),(2, 4, 'This is comment four'),(1, 2, 'This is comment five'),(3, 1, 'This is comment six'),(3, 2, 'This is comment six'),(5, 4, 'This is comment seven'),(2, 3, 'This is comment seven');
```

Dans les deux cas, les mots-clés à retenir sont :

    CONSTRAINT : tu indiques ici le nom que tu souhaites, qui te permet d’identifier ta contrainte.
    FOREIGN KEY() : indique que tu souhaites créer une contrainte de type “clé étrangère” sur le champ indiqué entre les parenthèses, ici school_id, de la table wizard.
    REFERENCES () : et ce dernier mot-clé indique que la clé étrangère fait référence ici au champ id de la table school.


### 6.3.3. **2. One To One (1-1)**

One To One : reprend l’exemple donné plus haut d’un Sorcier (table `wizard`) qui possède une et une seule Baguette (table `wand`). Dans ce cas, il y a deux solutions possibles. Soit la table `wizard` prend une clé étrangère `wand_id`, soit la table `wand` prend une clé étrangère `wizard_id`. C’est donc à nous de choisir la solution qui te semble la plus pratique, en fonction des requêtes que tu seras amené à faire.

La relation reste donc de type 1-1. Ici, on choisit de mettre une clé wizard_id dans la table pet, mais le contraire est tout à fait possible.

![one-to-one](./img/15.png)

### 6.3.4. **3. Many To Many (N-M)**

Ce derniercas, et le plus compliqué est la relation N-M. Ici un élève peut emprunter plusieurs livres, et un livre peut être emprunté par plusieurs élèves. 
Dans ce cas, on ne peut ni mettre une clé `book_id` dans `wizard`, ni mettre une clé `wizard_id` dans `book`.
Il va donc falloir créer une nouvelle table intermédiaire qui va contenir les deux clés étrangères. Cette table pourra s’appeler par exemple `borrowing` (emprunt). Selon les cas, la clé primaire pourra être composite, c’est-à-dire que l’unicité sera définie par le couple de clés étrangères `wizard_id` ET `book_id`. Dans cet exemple, un même sorcier peut emprunter un même livre à différentes dates. Dans ce cas, il faudrait plutôt créer une clé primaire auto-incrémentée pour s’assurer de l’unicité de la clé. Si besoin, cette table intermédiaire peut également accueillir des champs supplémentaires (par exemple date de réservation) qui ne seraient à leur place ni dans la table wizard, ni dans la table book.

Dans ce cas, la relation est de type N-M. Il faut donc créer une table intermédiaire, appelée ici wizard_pet. La clé primaire est composite, car l’unicité est vérifiée par le couple des deux clés étrangères wizard_id et pet_id.
![many to many](./img/16.png)

Remarque : ces différentes règles te permettent de passer d’un MCD à un MLD (Modèle Logique de Données). La partie MPD (Modèle Physique de données) est moins utile de nos jours. Elle est censée prendre en compte les spécificités du SGBDR utilisé, mais celles-ci étant beaucoup plus proches aujourd’hui qu’à l’époque où Merise à été créé, cette étape est aujourd’hui bien moins pertinente. Tes MLD/MPD peuvent être “fusionnés”. Il faut que ton MLD soit le reflet de ta base finale (telle qu’elle sera écrite en SQL), avec toutes les informations sur les tables, leurs champs et les types utilisés pour ces champs.

### 6.3.5. Les contraintes d'intégrité

Règles à suivre quand des enregistrements de tables reliées sont mis à jour ou supprimés. Exemple : 

J’efface une école de la table school, reliée à des élèves de la table student
- Si aucune contrainte n’est définie, l’école est effacée et les élèves reliés à cette école se retrouvent alors “orphelins”
- Si une contrainte est définie sans option, la suppression est refusée car des élèves sont associés à cette école (par contre, on pourra effacer un élève qui lui n’est relié qu’à une et une seule école !)
- Si une option CASCADE est définie, les élèves associés à école seront automatiquement supprimés

``` sql
CREATE TABLE student
  	…
  PRIMARY_KEY(id)
  FOREIGN KEY (school_id)
	REFERENCES school(id)
  	ON DELETE CASCADE
  	ON UPDATE NO ACTION;

```
Options après `ON DELETE`  et `ON UPDATE` :
- `CASCADE` : si je tente de supprimer la clé primaire, alors supprime tous les enregistrements avec l'id associé
- `SET NULL` : si je tente de supprimer la clé primaire, alors met NULL dans les enregistrements avec l'id associé
- `NO ACTION` : si je tente de supprimer la clé primaire, laisse les enregistrements dépendants avec l'id associé (perte d'intégrité)
- `RESTRICT` : si je tente de supprimer la clé primaire, empêche la suppression si id référencée ailleurs


[Return to Top](#notes-sql)
# 7. **Les Jointures**

## 7.1. INNER JOIN

### 7.1.1. Syntaxe

Une fois que tes tables sont reliées avec les **foreign key**, cela va permettre de récupérer les informations de plusieurs tables en une seule requête SQL. Pour cela, on va utiliser les jointures :


``` sql
SELECT <column1>, <column2>… 
FROM <table1>
INNER JOIN <table2> ON <condition>
```
![illus](./img/17.png)

![illus](./img/18.png)

### 7.1.2. Exemple

``` sql
SELECT firstname, lastname, name
FROM wizard
INNER JOIN school ON school.id=wizard.school_id;
```

```sql
SELECT
  users.first_name,
  users.last_name,
  posts.title,
  posts.publish_date
FROM users
INNER JOIN posts
ON users.id = posts.user_id
ORDER BY posts.title;
```

### 7.1.3. Utilisation des Alias

``` sql
SELECT name AS school_name FROM school AS s;
```

Ou plus simplement :
``` sql
SELECT name school_name FROM school s;
```

``` sql
SELECT w.firstname, w.lastname, s.name as school_name
FROM wizard as w
JOIN school as s ON s.id=w.school_id;
```

### 7.1.4. Autres Exemples
Récupération de tous les élèves de l’école de Bordeaux. Les lignes renvoyées sont celles vérifiant la condition. Elles contiennent les champs des deux tables

``` sql
SELECT st.firstname, st.lastname, sc.city
       FROM student AS st
       JOIN school AS sc ON sc.id=st.school_id
       WHERE sc.city = 'Bordeaux';
```
Retourne :
``` sql
firstname |  lastname  |  city
----------+------------+----------
Arthur    | Pendragon  | Bordeaux 
Lancelot  | Du Lac     | Bordeaux
```

## 7.2. Jointures Avancées

**Jointures Imbriquées**

Récupération de tous les élèves dans une école proposant le langage PHP
``` sql
SELECT firstname, name
       FROM student AS st
       JOIN school AS sc ON sc.id=st.school_id
         JOIN teaching AS t ON t.school_id = sc.id
           JOIN language AS la ON t.language_id=la.id
       WHERE la.language='PHP';
```
![illus](./img/27.png)

https://sql.sh/cours/jointures#google_vignette

## 7.3. Join Multiple Tables

```sql
SELECT
comments.body,
posts.title,
users.first_name,
users.last_name
FROM comments
INNER JOIN posts on posts.id = comments.post_id
INNER JOIN users on users.id = comments.user_id
ORDER BY posts.title;
```


## 7.4. LEFT JOIN & RIGTH JOIN

Par exemple la table wizard possède deux tuples non reliés à une école. Cependant, comment faire si tu souhaites ressortir les informations sur tous les élèves, même ceux non inscrits dans une école ?

Dans ce cas, c’est la requête `LEFT JOIN` qui va t’être utile. Elle permet, comme son nom l’indique, de ressortir toutes les informations de la table de gauche (à gauche du JOIN), même si celles-ci ne sont reliées à aucune information de la table de droite (en plus des données renvoyées par un JOIN classique). 

On supprime l'école de certains élèves :
``` sql
UPDATE wizard SET school_id=NULL WHERE lastname='weasley';
```
On fait la requête
``` sql
SELECT w.firstname, w.lastname, s.name  
FROM wizard AS w 
LEFT JOIN school AS s ON s.id=w.school_id;
```
On obtient :
``` sh
+-----------+-------------+--------------------------------------------+
| firstname | lastname    | name                                       |
+-----------+-------------+--------------------------------------------+
| harry     | potter      | Hogwarts School of Witchcraft and Wizardry |
| hermione  | granger     | Hogwarts School of Witchcraft and Wizardry |
| lily      | potter      | Hogwarts School of Witchcraft and Wizardry |
| ron       | weasley     | NULL                                       |
| ginny     | weasley     | NULL                                       |
| fred      | weasley     | NULL                                       |
| george    | weasley     | NULL                                       |
| arthur    | weasley     | NULL                                       |
| molly     | weasley     | NULL                                       |
| drago     | malefoy     | Hogwarts School of Witchcraft and Wizardry |
| albus     | dumbledore  | Hogwarts School of Witchcraft and Wizardry |
| severus   | rogue       | Hogwarts School of Witchcraft and Wizardry |
| tom       | jédusor     | Hogwarts School of Witchcraft and Wizardry |
| dudley    | dursley     | Hogwarts School of Witchcraft and Wizardry |
| fleur     | delacour    | Beauxbatons Academy of Magic               |
| gabrielle | delacour    | Beauxbatons Academy of Magic               |
| viktor    | krum        | Durmstrang Institute                       |
| gellert   | grindelwald | Durmstrang Institute                       |
| babajide  | akingbade   | Uagadou School of Magic                    |
+-----------+-------------+--------------------------------------------+
```
On fait un INNER JOIN classique, on n'aurait pas obtenu les élèves qui ne seraient inscrits dans aucune école.


De la même manière, si tu veux récupérer toutes les écoles, même celles sans étudiants, tu peux utiliser `RIGHT JOIN` et cette fois, pour les écoles sans étudiant, les champs firstname et lastname seront NULL.

``` sql
SELECT w.firstname, w.lastname, s.name  
FROM wizard AS w
RIGHT JOIN school AS s ON s.id=w.school_id;
```
On obtiendrait :
``` sql
+-----------+-------------+----------------------------------------------+
| firstname | lastname    | name                                         |
+-----------+-------------+----------------------------------------------+
| fleur     | delacour    | Beauxbatons Academy of Magic                 |
| gabrielle | delacour    | Beauxbatons Academy of Magic                 |
| NULL      | NULL        | Castelobruxo                                 |
| viktor    | krum        | Durmstrang Institute                         |
| gellert   | grindelwald | Durmstrang Institute                         |
| harry     | potter      | Hogwarts School of Witchcraft and Wizardry   |
| hermione  | granger     | Hogwarts School of Witchcraft and Wizardry   |
| lily      | potter      | Hogwarts School of Witchcraft and Wizardry   |
| drago     | malefoy     | Hogwarts School of Witchcraft and Wizardry   |
| albus     | dumbledore  | Hogwarts School of Witchcraft and Wizardry   |
| severus   | rogue       | Hogwarts School of Witchcraft and Wizardry   |
| tom       | jédusor     | Hogwarts School of Witchcraft and Wizardry   |
| dudley    | dursley     | Hogwarts School of Witchcraft and Wizardry   |
| NULL      | NULL        | Ilvermorny School of Witchcraft and Wizardry |
| NULL      | NULL        | Koldovstoretz                                |
| NULL      | NULL        | Mahoutokoro School of Magic                  |
| babajide  | akingbade   | Uagadou School of Magic                      |
+-----------+-------------+----------------------------------------------+
```

LEFT JOIN renvoie TOUS les enregistrements de la table de gauche (dans le FROM) même quand il n’y a pas de correspondance avec la table de droite (dans ce cas on renvoie NULL)
(INNER) JOIN La plus utilisée. 

Renvoie les enregistrements quand la condition (après le ON) est remplie. Seuls les enregistrements communs des tables A et B sont retournés 

RIGHT JOIN renvoie TOUS les enregistrement de la table de droite (après le JOIN) même quand il n’y a pas de correspondance avec la table de gauche (dans ce cas il renvoie NULL)


```sql
SELECT
comments.body,
posts.title
FROM comments
LEFT JOIN posts ON posts.id = comments.post_id
ORDER BY posts.title;
```

https://sql.sh/cours/jointures

## 7.5. UNION
UNION permet de cumuler les résultats de deux requêtes
``` sql
SELECT firstname FROM student WHERE firstname LIKE 'A%'
UNION
SELECT firstname FROM student WHERE firstname LIKE 'L%'

```
Retourne :
``` sh
firstname
----------
Arthur
Lancelot
Léodagan
```
S’il y a des doublons dans les résultats des deux requêtes, ils ne sont pas affichés. Si on veut les afficher, il faut utiliser UNION ALL

[Return to Top](#notes-sql)
# 8. **SQL Avancé**

## 8.1. WHERE Avancée

### 8.1.1. **AND/OR**
``` sql
SELECT firstname, lastname FROM student WHERE firstname='Arthur' AND lastname='Pendragon';
```
Les AND/OR peuvent se suivre et se cumuler.

### 8.1.2. **LIKE**
``` sql
SELECT firstname FROM student WHERE firstname LIKE 'L%';
```
Le symbole % sert de Joker. L’exemple renvoie “Lancelot”, “Léodagan”...  
Remarque : MySQL est insensible à la casse, donc "L%" équivaut à "l%", ce qui n’est pas le cas de tous les SGBDR.

``` sql
SELECT * FROM student WHERE firstname LIKE '%l%';
```
Renvoie Lancelot, Leodagan, Perceval, Merlin

### 8.1.3. **BETWEEN**
``` sql
SELECT city, capacity FROM school WHERE capacity BETWEEN 20 AND 40;
```

### 8.1.4. **IS NULL/IS NOT NULL**
``` sql
SELECT * FROM school WHERE capacity IS NOT NULL;
```

### 8.1.5. **IN** : 
``` sql
SELECT * FROM school WHERE city IN ('Reims', 'Lille', 'Biarritz');
```
On peut faire des requêtes imbriquées mais il faut mieux préférer les jointures :
``` sql
SELECT * FROM student
	   WHERE school_id IN (
           SELECT id FROM school WHERE capacity>10);
```

## 8.2. Fonctions SQL

### 8.2.1. **DISTINCT**
``` sql
SELECT DISTINCT(firstname) FROM student;
```
Si un prénom est présent plusieurs fois, le distinct permet de ne l’afficher qu’une seule fois. Les doublons sont ainsi éliminés.


```sql
SELECT DISTINCT location FROM users;
```

### 8.2.2. **CONCAT**
``` sql
SELECT CONCAT(firstname,' ',lastname) AS fullname FROM student;
```
Retourne
``` sh
fullname
-----------------
Arthur Pendragon
Lancelot Du Lac
```

```sql
SELECT CONCAT(first_name, ' ', last_name) AS 'Name', dept FROM users;
```

### 8.2.3. **LENGTH**
``` sql
SELECT firstname, LENGTH(firstname) AS len
    FROM student
    WHERE LENGTH(firstname) > 7;
```
Retourne :
``` sh
firstname   |  len
------------+----------
Lancelot    |  8
Perceval    |  8
Guenièvre   |  9
```

Il existe également de nombreuses autres fonctions qui ont pour but de manipuler des chaînes (LOWER(), UPPER(), LENGTH(), REPLACE(), SUBSTRING(), TRIM() ...).

## 8.3. Fonctions Mathématiques

### 8.3.1. **RAND**
Permet de générer un nombre aléatoire

### 8.3.2. **ROUND**
Permet d'arrondir un décimal

``` sql
SELECT price, ROUND(price,1) AS rounded_price FROM product;
```
Retourne
``` sh
price | rounded_price
------+---------------
20.54 | 20.5
20.99 | 21
```

### 8.3.3. **Autres fonctions mathématiques**

Ou encore ABS(), SIN(), COS(), EXP(), LOG(), PI()...

## 8.4. Fonctions Date

### 8.4.1. **NOW()**
Renvoie la date du jour
### 8.4.2. **MONTH()**
Extrait le numéro de mois d'une date
### 8.4.3. **DATEDIFF()**

## 8.5. Fonctions D'agrégation

Fonctions permettant de réaliser des calculs sur un ensemble de résultats.

### 8.5.1. **COUNT()**
Compte le nombre de résultats
### 8.5.2. **SUM()**
Calcule la somme pour un champ donné
### 8.5.3. **MAX()**
Renvoie la valeur max pour un champ donné
### 8.5.4. **MIN()**
Renvoie la valeur min pour un champ donné
### 8.5.5. **AVG()**
Calcule la moyenne pour un champ donné

### 8.5.6. Exemples

``` sql
SELECT AVG(note) as average FROM note;
SELECT MIN(note), MAX(note) FROM note;
SELECT SUM(payment) AS total, AVG(payment) AS avg FROM bribe;
SELECT count(*) as nb_school FROM school;
```
Attention on ne peut pas mélanger ce type de reqiête dite d'agrégation avec des requêtes classiques ligne par ligne.

```sql
SELECT COUNT(id) FROM users;
SELECT MAX(age) FROM users;
SELECT MIN(age) FROM users;
SELECT SUM(age) FROM users;
SELECT UCASE(first_name), LCASE(last_name) FROM users;
```


https://sql.sh/fonctions
https://fr.wikibooks.org/wiki/MySQL/Fonctions


## 8.6. GROUP BY / HAVING

La jointure ici ne sert à rien pour “grouper”, puisque c’est le school_id de la table wizard qui est utilisé. Mais elle est cependant utile pour récupérer le name de l’école.

La syntaxe du GROUP BY est très simple. Elle attend une liste de champs sur lesquels grouper (tu peux indiquer plusieurs champs, elle fera alors les groupes dans l’ordre de ces champs).

Par exemple, voici comment récupérer le nombre d'étudiants par école :

``` sql
SELECT s.name, COUNT(*) as nb_student 
    FROM wizard w 
    INNER JOIN school s ON s.id=school_id 
    GROUP BY s.id;
```

``` sql
SELECT region, count(*) AS nb FROM student
       GROUP BY region
       ORDER BY nb DESC
```
Retourne
``` sh
 region              | nb
---------------------+----------
Ile de France        | 12
Auvergne-Rhône Alpes | 10
Centre               | 6
Occitanie            | 3
```
Il est possible d'avoir plusieurs champs dans une clause GROUP BY :
``` sql
SELECT region, city, count(*) AS nb
       FROM student
       GROUP BY region, city
       ORDER BY nb DESC
```
``` sh
region      	    |  city 	    | nb
---------------------+------------+--------
Ile de France        | Paris  	    | 12
Auvergne-Rhône Alpes | Lyon       | 10
Centre               | Orléans    | 3
Centre               | La Loupe   | 2
Occitanie            | Toulouse   | 1
```


Il est possible d’aller encore plus loin dans les regroupements, en y ajoutant des critères de filtre sur ces groupes. Par exemple, si tu souhaites ne ressortir que les groupes ayant plus de trois élèves, tu peux écrire :

``` sql
SELECT s.name, COUNT(*) AS nb_student
  FROM wizard w
  INNER JOIN school s ON s.id=w.school_id
  GROUP BY school_id
  HAVING nb_student > 3;
```
Donne :
``` sh
+----------------------------------------------+------------+
| name                                         | nb_student |
+----------------------------------------------+------------+
| Castelobruxo                                 |          8 |
| Hogwarts School of Witchcraft and Wizardry   |         29 |
| Ilvermorny School of Witchcraft and Wizardry |          4 |
| Koldovstoretz                                |          9 |
| Ugadou School of Magic                       |          9 |
| Beauxbatons Academy of Magic                 |          7 |
| Mahoutokoro School of Magic                  |          6 |
+----------------------------------------------+------------+
```
Le HAVING a donc un fonctionnement très similaire à une clause WHERE, puisqu’il a également besoin d’une condition. Cependant, ces deux clauses sont différentes et ne sont pas interchangeables.

En effet, lorsque tu fais un SELECT, tu ressors un certain nombre de tuples. Un WHERE va imposer un filtre qui va potentiellement diminuer ce nombre de résultats. Si tu ajoutes ensuite un GROUP BY, le regroupement ne se fera QUE sur les tuples préalablement filtrés par le WHERE. Une fois le regroupement fait, si tu ajoutes un HAVING, ce dernier s’appliquera sur les résultats du regroupement. C’est pour cela qu’un WHERE s’écrit toujours avant un bloc GROUP BY/HAVING.


Exemple :
``` sql
SELECT city, count(*) as nb FROM student
       GROUP BY city
       HAVING nb>2
       ORDER BY nb DESC
```
``` sh
 city     |  nb
----------+---------
Paris     | 12
Lyon      | 10
Orléans   | 3
```

```sql
SELECT age, COUNT(age) FROM users GROUP BY age;
SELECT age, COUNT(age) FROM users WHERE age > 20 GROUP BY age;
SELECT age, COUNT(age) FROM users GROUP BY age HAVING count(age) >=2;
```

## 8.7. Administration avancée
Il est possible de créer/supprimer des utilisateurs 

``` sql
CREATE USER 'myuser'@'localhost' IDENTIFIED BY 'mypassword';
DROP USER 'myuser'@'localhost';
```
Et de gérer très finement leurs droits
- Limiter le type de requête (par exemple pas de DELETE ou d’INSERT, mais SELECT autorisé)
- Limiter les tables accessibles 

``` sql
GRANT ALL ON mydb TO 'perceval'@'localhost';
// Perceval a tous les droits sur la bdd mydb
GRANT SELECT, UPDATE ON mydb.Eleve TO 'caradoc'@'localhost';
// Caradoc n’a que les droits de SELECT et UPDATE et uniquement sur la table Eleve de la bdd mydb
```
## 8.8. Administration avancée

**Procédure stockée** : Suite d’instructions SQL définies par un nom 
et enregistrées dans la base de données elle-même. Il est possible 
d’appeler la procédure par son nom et d’exécuter ces instructions. 
Elles peuvent être comparées à des fonctions.

**Transaction** : Suite de requêtes dont l'exécution se fait par bloc. Si tout le bloc d’instruction n’est pas exécuté (erreur), il est possible de revenir en arrière (ROLLBACK). Très utile pour s’assurer de l'intégrité des données (notamment des données sensibles).

**Trigger** : Instructions associées à une table qui se déclenchent lorsqu’un événement prédéterminé survient (INSERT, UPDATE…)

**Table temporaire** : Permet de stocker des résultats dans une table à durée de vie limitée (supprimées si on se déconnecte du SGBDR) : gain de performance pour des grosses requêtes répétitives.

https://openclassrooms.com/fr/courses/6971126-implementez-vos-bases-de-donnees-relationnelles-avec-sql?archived-source=1959476



[Return to Top](#notes-sql)
# 9. **Main Title**
## 9.1. Subtitle

``` sql


```

[u]Texte[/u]
<color=red>Texte</color> / [color=#FF3300]Texte[/color]

<font color=red>Texte</font>

[size=3]Texte[/size]

*TODO*

Commande   ==ALTER== 


### 9.1.1. qfsdf
#### 9.1.1.1. qfsfsfsfd
qfsfsfsfd
#qfsfsfsfd
fsfsfs