- [1. **Introduction**](#1-introduction)
- [2. **Installation et Initialisation d'un projet Symfony**](#2-installation-et-initialisation-dun-projet-symfony)
  - [2.1. Installation](#21-installation)
  - [2.2. Structure d'un projet Symfony](#22-structure-dun-projet-symfony)
  - [2.3. Préconfigurer l'accès à la base de données](#23-préconfigurer-laccès-à-la-base-de-données)
  - [2.4. Versionner son projet avec Git](#24-versionner-son-projet-avec-git)
  - [2.5. Installer un projet Symfony existant](#25-installer-un-projet-symfony-existant)
- [3. **Installation du module Webpack Encore**](#3-installation-du-module-webpack-encore)
  - [3.1. Installation du module Symfony Encore](#31-installation-du-module-symfony-encore)
  - [3.2. Installation des outils Javascript](#32-installation-des-outils-javascript)
  - [3.3. Installation des dépendances du projet](#33-installation-des-dépendances-du-projet)
  - [3.4. Utilisation de Webpack Encore](#34-utilisation-de-webpack-encore)
  - [3.5. Lancer Webpack](#35-lancer-webpack)
  - [3.6. Gestion des images](#36-gestion-des-images)
  - [3.7. Installation de librairies tierces avec Webpack Encore](#37-installation-de-librairies-tierces-avec-webpack-encore)
  - [3.8. Installation de bootstrap](#38-installation-de-bootstrap)
- [4. **Création de la page d’accueil**](#4-création-de-la-page-daccueil)
  - [4.1. Créer le premier contrôleur](#41-créer-le-premier-contrôleur)
  - [4.2. Implémenter la route](#42-implémenter-la-route)
  - [4.3. Appeler un template Twig : la vue](#43-appeler-un-template-twig--la-vue)
  - [4.4. Et le modèle ?](#44-et-le-modèle-)
- [5. **Routing Avancé**](#5-routing-avancé)
  - [5.1. Rappel](#51-rappel)
  - [5.2. Les paramètres de route](#52-les-paramètres-de-route)
  - [5.3. Les contraintes de route](#53-les-contraintes-de-route)
  - [5.4. Les méthodes HTTP](#54-les-méthodes-http)
  - [5.5. Les préfixes de route](#55-les-préfixes-de-route)
  - [5.6. Utiliser et générer les routes](#56-utiliser-et-générer-les-routes)
- [6. **Doctrine**](#6-doctrine)
  - [6.1. Créer une entité avec Doctrine](#61-créer-une-entité-avec-doctrine)
    - [6.1.1. Mise à jour d'une entité avec Doctrine](#611-mise-à-jour-dune-entité-avec-doctrine)
    - [6.1.2. Détection des entités](#612-détection-des-entités)
    - [6.1.3. Validation des entités](#613-validation-des-entités)
    - [6.1.4. Pour contrôler les migrations](#614-pour-contrôler-les-migrations)
    - [6.1.5. Après chaque mise à jour de la BDD](#615-après-chaque-mise-à-jour-de-la-bdd)
  - [6.2. Récupérer des données stockées avec Doctrine](#62-récupérer-des-données-stockées-avec-doctrine)
    - [6.2.1. Récupération simple](#621-récupération-simple)
    - [6.2.2. findAll()](#622-findall)
    - [6.2.3. findOneBy() : récupérer un objet unique selon différents paramètres](#623-findoneby--récupérer-un-objet-unique-selon-différents-paramètres)
    - [6.2.4. findBy() : récupérer plusieurs objets selon différents paramètres](#624-findby--récupérer-plusieurs-objets-selon-différents-paramètres)
    - [6.2.5. find(mixec $id)](#625-findmixec-id)
  - [6.3. Manipulation des données avec Doctrine](#63-manipulation-des-données-avec-doctrine)
    - [6.3.1. Ajouter une nouvelle donnée](#631-ajouter-une-nouvelle-donnée)
    - [6.3.2. Modifier une donnée](#632-modifier-une-donnée)
    - [6.3.3. Supprimer une donnée](#633-supprimer-une-donnée)
    - [6.3.4. Utilisation directe de doctrine](#634-utilisation-directe-de-doctrine)
  - [6.4. Utiliser le QueryBuilder](#64-utiliser-le-querybuilder)
  - [6.5. Relation avec Doctrine : Exemple avec la Many-To-One](#65-relation-avec-doctrine--exemple-avec-la-many-to-one)
    - [6.5.1. Créer la relation dans Symfony](#651-créer-la-relation-dans-symfony)
  - [6.6. Relation avec Doctrine : Exemple avec la One-To-One](#66-relation-avec-doctrine--exemple-avec-la-one-to-one)
  - [6.7. Les relations bidirectionnelles avec Doctrine](#67-les-relations-bidirectionnelles-avec-doctrine)
    - [6.7.1. Créer la relation avec Symfony : Many-To-One](#671-créer-la-relation-avec-symfony--many-to-one)
    - [6.7.2. Retour sur l'exemple One-To-One](#672-retour-sur-lexemple-one-to-one)
  - [6.8. Relation avec Doctrine : Exemple avec la Many-To-Many](#68-relation-avec-doctrine--exemple-avec-la-many-to-many)
- [7. **Les fixtures**](#7-les-fixtures)
  - [7.1. Utilisation simple des fixtures](#71-utilisation-simple-des-fixtures)
  - [7.2. Utilisation avancée des fixtures](#72-utilisation-avancée-des-fixtures)
    - [7.2.1. Ajouter des références aux fixtures](#721-ajouter-des-références-aux-fixtures)
    - [7.2.2. Utilisation des références](#722-utilisation-des-références)
- [8. **FakerPHP**](#8-fakerphp)
  - [8.1. Installation](#81-installation)
  - [8.2. Utilisation](#82-utilisation)
- [9. **Les Formulaires**](#9-les-formulaires)
  - [9.1. Créer un formulaire](#91-créer-un-formulaire)
    - [La classe formulaire](#la-classe-formulaire)
    - [9.1.1. Le contrôleur](#911-le-contrôleur)
    - [9.1.2. La vue](#912-la-vue)
  - [9.2. FormType](#92-formtype)
    - [9.2.1. Les éléments FieldType](#921-les-éléments-fieldtype)
    - [9.2.2. Les options](#922-les-options)
    - [9.2.3. Le cas EntityType](#923-le-cas-entitytype)
    - [9.2.4. Imbrication de formulaires](#924-imbrication-de-formulaires)
- [10. **Validation des formulaires**](#10-validation-des-formulaires)
  - [10.1. Fonctionnement](#101-fonctionnement)
  - [10.2. Les différentes contraintes](#102-les-différentes-contraintes)
  - [10.3. Lancer la validation](#103-lancer-la-validation)
  - [10.4. Sécurisation des failles CSRF](#104-sécurisation-des-failles-csrf)
- [11. **ParamConverter**](#11-paramconverter)
  - [11.1. Le principe du ParamConverter](#111-le-principe-du-paramconverter)
  - [11.2. Utilisation avancée du Param Converter](#112-utilisation-avancée-du-param-converter)
  - [11.3. Date Converter](#113-date-converter)
- [12. Sessions et Messages flash](#12-sessions-et-messages-flash)
  - [12.1. Les sessions sous Symfony](#121-les-sessions-sous-symfony)
  - [12.2. Les messages flash](#122-les-messages-flash)
    - [12.2.1. Utilisation des messages flash avec Symfony](#1221-utilisation-des-messages-flash-avec-symfony)
- [13. **Les Services**](#13-les-services)
  - [13.1. Qu'est ce qu'un service ?](#131-quest-ce-quun-service-)
  - [13.2. Pourquoi un service ?](#132-pourquoi-un-service-)
  - [13.3. Créer un service : une histoire de réduction](#133-créer-un-service--une-histoire-de-réduction)
    - [13.3.1. Présentation](#1331-présentation)
    - [13.3.2. Première approche : tout dans le controller](#1332-première-approche--tout-dans-le-controller)
    - [13.3.3. Réorganisation du code : création d'une classe dédie = le service](#1333-réorganisation-du-code--création-dune-classe-dédie--le-service)
    - [13.3.4. Retour au controller](#1334-retour-au-controller)
    - [13.3.5. Injection de dépendance](#1335-injection-de-dépendance)
    - [13.3.6. Utilisation du service dans un contrôleur](#1336-utilisation-du-service-dans-un-contrôleur)
    - [13.3.7. Alléger le contrôleur](#1337-alléger-le-contrôleur)
    - [13.3.8. Principe d'inversion des dépendances](#1338-principe-dinversion-des-dépendances)
  - [13.4. Service Container et paramétrage](#134-service-container-et-paramétrage)
  - [13.5. Exemple : Utilisation du service Slug](#135-exemple--utilisation-du-service-slug)
  - [13.6. Appeler un service en dehors d'un contrôleur](#136-appeler-un-service-en-dehors-dun-contrôleur)
  - [13.7. Autre exemple : créer un service pour calculer une durée](#137-autre-exemple--créer-un-service-pour-calculer-une-durée)
  - [13.8. Autre exemple : utiliser httpClient pour une requête API](#138-autre-exemple--utiliser-httpclient-pour-une-requête-api)
- [14. **Envoi d'email**](#14-envoi-demail)
  - [14.1. Configurer l'envoie des mails](#141-configurer-lenvoie-des-mails)
    - [14.1.1. Choix du service](#1411-choix-du-service)
    - [14.1.2. Configurer le serveur SMTP dans Symfony](#1412-configurer-le-serveur-smtp-dans-symfony)
  - [14.2. Appeler Mailer depuis le contrôleur](#142-appeler-mailer-depuis-le-contrôleur)
  - [14.3. Mise en forme des emails](#143-mise-en-forme-des-emails)
- [15. **Upload de médias avec Vich Upload**](#15-upload-de-médias-avec-vich-upload)
  - [15.1. Installer et configurer le bundle VichUploader dans un projet Symfony](#151-installer-et-configurer-le-bundle-vichuploader-dans-un-projet-symfony)
  - [15.2. Permettre à un utilisateur d’uploader un fichier sur un serveur depuis une application.](#152-permettre-à-un-utilisateur-duploader-un-fichier-sur-un-serveur-depuis-une-application)
- [16. **Gestion des utilisateurs**](#16-gestion-des-utilisateurs)
  - [16.1. Creation des USERS](#161-creation-des-users)
  - [16.2. Un peu de sécurité](#162-un-peu-de-sécurité)
  - [16.3. Configurer le firewall](#163-configurer-le-firewall)
  - [16.4. Création de users à l'aide des fixtures](#164-création-de-users-à-laide-des-fixtures)
  - [16.5. Gestion du Login](#165-gestion-du-login)
  - [16.6. Gestion du Logout](#166-gestion-du-logout)
  - [Récupération de l'utilisateur connecté](#récupération-de-lutilisateur-connecté)
  - [16.7. Côté UI/UX : `app.user` de Twig](#167-côté-uiux--appuser-de-twig)
- [17. **Sécuriser les routes**](#17-sécuriser-les-routes)
  - [17.1. Gestion des rôles et fichier `security.yaml`](#171-gestion-des-rôles-et-fichier-securityyaml)
  - [17.2. Contrôle de l'authentification et des rôles](#172-contrôle-de-lauthentification-et-des-rôles)
    - [17.2.1. Vérifier si un utilisateur est loggué](#1721-vérifier-si-un-utilisateur-est-loggué)
    - [17.2.2. Vérifier le rôle d'un utilisateur](#1722-vérifier-le-rôle-dun-utilisateur)
  - [17.3. Protéger une route grâce au fichier yaml](#173-protéger-une-route-grâce-au-fichier-yaml)
  - [17.4. Protéger une route côté contrôleur](#174-protéger-une-route-côté-contrôleur)
  - [17.5. Filtrer côté vue](#175-filtrer-côté-vue)
- [18. **Inscription d'un nouvel utilisateur**](#18-inscription-dun-nouvel-utilisateur)
  - [18.1. Créer un compte utilisateur : implémenter un formulaire d'enregistrement](#181-créer-un-compte-utilisateur--implémenter-un-formulaire-denregistrement)
  - [18.2. Connexion automatique de l'utilisateur inscrit](#182-connexion-automatique-de-lutilisateur-inscrit)
- [19. **Test Unitaires**](#19-test-unitaires)
  - [19.1. Introduction](#191-introduction)
  - [19.2. Tester en PHP](#192-tester-en-php)
    - [19.2.1. PHPUnit](#1921-phpunit)
    - [19.2.2. Exemples](#1922-exemples)
- [**Les requêtes personnalisées**](#les-requêtes-personnalisées)
  - [Le QueryBuilder](#le-querybuilder)
  - [L'alternative DQL](#lalternative-dql)
- [20. **JS en Symfony**](#20-js-en-symfony)
  - [20.1. Subtitle](#201-subtitle)
- [20. **Main Title**](#20-main-title)
  - [20.1. Subtitle](#201-subtitle-1)
- [21. **CLI Symfony**](#21-cli-symfony)
  - [21.1. Doctrine](#211-doctrine)



[Return to Top](#notes-symfony)
# 1. **Introduction**

Symfony est un **framework** HTTP open source français, écrit en PHP objet. C'est le plus utilisé en France et l'un des plus utilisés dans le monde. A ne pas confondre avec un CMS !  
https://symfony.com/what-is-symfony

Pour démarrer un projet symfony :  
https://symfony.com/doc/current/setup.html

https://symfony.com/doc/current/quick_tour/flex_recipes.html

Historiquement, Symfony utilise le pattern MVC comme architecture. Il est possible avec Symfony d'utiliser d'autres types d'architecture (CQRS, middlewares...) mais la plus populaire reste encore MVC. Ces ressources vont te permettre de bien comprendre l'architecture standard de Symfony : MVC.

https://symfony.com/doc/current/introduction/from_flat_php_to_symfony.html

https://fr.slideshare.net/KristenLeLiboux/application-mvc


La société à l'origine de `Symfony` est `Sensiolabs`. Qui a également développé `Twig`. Par Fabien Potencier, 2004, Symfoony SAS. Un concurrent de `Symfony` est `Laravel`.
L'option `--webapp` doit être utiliser pour ajouter des librairies comme `Twig`.
Pour créer un projet web symfony on doit utiliser la commande `symfony new <project-name> --webapp`.
Les méthodes (actions) d'un controlleur doivent renvoyer un Un objet `Symfony\Component\HttpFoundation\Response`.

https://symfony.com/releases



[Return to Top](#notes-symfony)
# 2. **Installation et Initialisation d'un projet Symfony**

## 2.1. Installation

Pour l'installer sur Linux :

``` sh
curl -1sLf 'https://dl.cloudsmith.io/public/symfony/stable/setup.deb.sh' | sudo -E bash
sudo apt install symfony-cli
```
Pour créer un nouveau projet  :

``` sh
symfony new [--webapp] [--version=lts] my_project

```
Ici :
``` sh
symfony new --webapp wild-series
```
A taper dans le dossier du projet.
https://symfony.com/doc/current/setup.html


L’option `--webapp` est optimisée pour les projets web traditionnels. Pour la création d’applications web plus spécifiques (microservices,API…), omettre l’option permet d’installer le minimum de dépendances possibles.  

L’option `--version=lts` installe la version Long Time Support (5.4 actuellement)L’
Lancer le projet fraîchement créé, avec le serveur préconfiguré de Symfony (uniquement sur un environnement contrôlé : dev, test, preprod… et non en production) :


Pour gérer ses dépendances Symfony utilise un plugin pour Composer appelé **Symfony Flex**, préconisé depuis symfony 4. Ce plugin, en amont de `Composer`, permet entre autres d'exécuter des "Recipes". Une Recipe est un script qui va permettre, par exemple, de générer automatiquement les fichiers de configuration de la dépendance fraîchement ajoutée ...etc. La procédure d'installation se trouve dans le `symfony.lock` qui doit être versionné.


Une fois le projet initialisé, il faut lancer un serveur HTTP pour lire les fichiers PHP/Symfony. On peut donc lancer un serveur local depuis le répertoire du projet symfony :

``` sh
php -S 127.0.0.1:8000 -t public/
ou
symfony server:start 
```
En production, tu devras utiliser Apache ou Nginx et non plus lancer un serveur "à la main", comme ci-dessus.

Par défaut, on risque d'avoir un message d'erreur du type `[WARNING] run "symfony.exe server:ca:install" first if you want to run the web server with TLS support, or use "--no- tls" to avoid this warning`. On peut spécifier l'option --no-tls qui permet de désactiver le mode HTTPS ou installer un certificat comme recommandé dans ton terminal.

Il existe une option qui lance ton serveur en tâche de fond: -d. Cela te permet de réutiliser ton terminal directement après avoir lancé ton serveur:
``` sh
symfony server:start -d
```

Pour ouvrir l'URL du serveur en cours dans ton navigateur (par ex localhost:8000), tu peux utiliser la commande
``` sh
symfony open:local
```

Afin de pouvoir stopper ton serveur fonctionnant en mode détaché, une autre commande est à ta disposition:
``` sh
symfony server:stop
```

https://symfony.com/doc/current/setup/symfony_server.html#getting-started

## 2.2. Structure d'un projet Symfony

Organisation de l'arborescence :

![arborescence](./img/52.png)

Sans que l'on s'en rende compte, Symfony a fait pas mal de choses. Dans le dossier wild-series, tu trouveras un ensemble de fichiers et de dossiers qui constituent l'architecture de ton projet Symfony.
On y trouve tous les outils nécessaires pour construire une plateforme sur des bases saines et solides. 

![architecture](./img/52.png)

https://symfony.com/doc/current/page_creation.html#checking-out-the-project-structure

## 2.3. Préconfigurer l'accès à la base de données

La version actuelle de **Symfony** nécessite que la base de données soit configurée dans ton projet dès le **début**, même si on n'a pour le moment pas besoin de base de données.

Il va falloir paramétrer la connexion à ta base de données : Symfony gère ce genre de paramètres sensibles dans des variables d'environnement globales au système pour un projet en production.

En local sur ta machine de développement, cela va se passer dans le fichier .env.local à la racine de ton projet. Actuellement, il n’existe pas. On peut dupliquer le fichier déjà existant .env pour t’en servir de modèle de base et le configurer correctement sous le nom de .env.local.

``` php
# .env.local
DATABASE_URL="mysql://your_username:your_pwd@127.0.0.1:3306/wild-series?serverVersion=8.0"
```

Attention, par défaut Symfony propose une ligne préconfigurée pour le SGBD PostgreSQL et non pour MySQL.
`#DATABASE_URL="postgresql://db_user:db_password@127.0.0.1:5432/db_name?serverVersion=13&charset=utf8" `.
Si on veut utiliser MySQL, on doit remplacer la ligne ci-dessus par celle commençant bien par mysql, et bien penser à commenter la ligne pour PostgreSQL.


Remarque : `127.0.0.1` ou `localhost` indique que la base de données est installée sur le poste qui exécute le script PHP, mais cela n'est pas forcément le cas. La base de données peut être sur un serveur dédié. Dans ce cas, il faut bien entendu saisir l'IP du serveur et s'assurer que le serveur autorise les connexions dites "externes" ou "distantes"...

Une fois cela fait, il ne te reste plus qu'à vérifier si tout est bien "câblé" en créant la base de données, via la commande :

``` sh
symfony console doctrine:database:create
# ou symfony console d:d:c
```

## 2.4. Versionner son projet avec Git

Lorqu'on installe `symfony`, le projet est déjà pensé pour Git.
En effet, il y a dans la plupart des dossiers des fichiers `.gitignore` qui excluront les fichiers à ne pas versionner.

`Symfony` a déjà effectué un git init et le projet contient un fichier de configuration .git/config par défaut. Il te faut alors simplement configurer ton dépôt distant (remote origin).

``` sh
git remote add origin git@github.com:User/YourRepoName.git
```
https://docs.github.com/en/free-pro-team@latest/github/using-git/adding-a-remote

Ensuite, on peut faire le 1er commit 
``` sh
git status
git branch -M main
git push -u origin main
```
Attention à ne pas versionner les fichiers de configuration de l'IDE. Il faut par exemple ajouter `.idea` au fichier `.gitignore` à la racine du projet.


## 2.5. Installer un projet Symfony existant

Si on récupère un projet où `Symfony` a déjà été **intialisé** (notemment en faisant un git clone), le dossier récupéré contient déjà toutes l'**infrastructure** de dossiers de Symfony. Mais il va manquer des dossiers notemment ceux ignorés par le `.gitignore`. Comme le dossier `vendor/` (généré par **Composer**). Or c'est lui qui contient les bibliothèques utilisées par l'application. Pour récupérer ce dossier il faudra lancer la commande suivante à la racine du projet :

``` sh
composer install
```

Il faudra ensuite reprendre les étapes précédentes notemment pour personnaliser le fichier.env puisqu'il contient des données sensibles qui sont propres (comme les identifiants de la BDD).

[Return to Top](#notes-symfony)
# 3. **Installation du module Webpack Encore**


## 3.1. Installation du module Symfony Encore

``` sh
composer require symfony/webpack-encore-bundle
```
Un fichier webpack.config.js a été créé, ainsi qu'un répertoire assets/ à la racine du projet (où tu placeras maintenant tous tes assets (CSS, JS, fonts, images statiques…). Mais avant d'aller plus loin, il faut équiper ta machine.

## 3.2. Installation des outils Javascript

**Remarque** : dans cette quête, tu utiliseras Yarn, qui est un gestionnaire de paquet pour les librairies Javascript (le pendant de Composer dans le monde JS !). Il se base sur le fichier package.json dans lequel seront listées les dépendances JS et CSS du projet tel qu'on le trouve dans le fichier composer.json avec les dépendances PHP. Cependant en JS, il existe plusieurs gestionnaires de paquets, dont NPM (le plus connu) et Yarn. Ce dernier, Yarn, est l’outil recommandé par Symfony dans la documentation officielle. Les deux sont équivalents (et compatibles avec Symfony) mais si tu commences un projet avec l’un, il ne faut plus que tu changes en cours de route, au risque d’avoir des conflits. De même, si tu travailles sur un projet à plusieurs, il faut que tout le monde utilise bien le même gestionnaire. C'est pour cela que tu vas utiliser exclusivement Yarn pour la suite.

1. NVM (Node Version Manager)

``` sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
```
Lorsque l'installation de nvm est terminée, pense à ⚠️ ouvrir un nouveau terminal, puis lance la commande nvm -v pour vérifier que tout s'est bien passé. La version de nvm s'affiche, tu peux passer à l'étape suivante.

2. nstallation de Node et NPM

Il fortement recommandé d'utiliser la version Active LTS de Node. Vérifie quelle est la version actuellement en cours à la page https://nodejs.org/en/about/releases/

``` sh
nvm install <version></version>
// Exemple
nvm install 18
```

À la fin de l'installation, nvm t'indique quelles versions majeures et mineures de Node et NPM ont été téléchargées. Tu peux vérifier que tout est ok avec node -v et npm -v.

3. Installation de Yarn

``` sh
npm install --global yarn
```

Vérifie avec yarn -v.

## 3.3. Installation des dépendances du projet

Avec un terminal, déplace-toi à la racine de ton projet Wild Series et lance la commande :

``` sh
yarn install
```

Cette commande (équivalente d'un composer install) va télécharger Encore et ses propres dépendances dans le dossier node_modules/ à la racine de ton projet. Ce répertoire est l'équivalent de vendor/ pour Composer. Par conséquent, il ne faudra **jamais** versionner node_modules ni le modifier. A l’installation via composer (et donc via flex), le .gitignore de ton projet a déjà été mis à jour en conséquence.
Le fichier webpack.config.js généré à la racine du projet contient toute la configuration de Webpack.

https://symfony.com/doc/current/frontend/encore/installation.html
https://webpack.js.org/

## 3.4. Utilisation de Webpack Encore

Dans le dossier `assets/`, il y déjà des dossiers et fichiers, dont un fichier `app.js`, et un sous dossier `styles/` avec un `app.css`.
Si on modifie le fichier `app.css`, la modification ne sera effective que quand tu auras lancé webpack ;-)
Regarde également le fichier `app.js`, il charge ton fichier `app.css` (c’est nécessaire au bon fonctionnement de webpack). Si on cré d’autres fichiers `CSS`, il faudra aussi les charger ici.

**Attention**  
Tu verras aussi un fichier `bootstrap.js` dans ce dossier assets (également importer dans app.js). Attention celui-ci n'a rien à voir avec le framework CSS Bootstrap que tu connais déjà. En effet "bootstrap" qui signifie "amorçage" en français, est un terme fréquemment utilisé pour des fichiers d'initialisation. Ici il sert à initialiser Stimulus qui est une dépendance JS utile aux composants optionnels de Symfony (Symfony UX). Tu peux l'ignorer pour le moment.


## 3.5. Lancer Webpack

Pour lancer Webpack, utilise une de ces lignes de commandes selon tes besoins (à lancer à la racine du projet) :

``` sh
yarn watch
```
Webpack surveille en continu le dossier `assets/` et recompile à la volée les assets dès qu'il y détecte la moindre modification sur les fichiers css, scss et js.

``` sh
yarn dev-server
```
Fais la même chose que la commande précédente mais en plus, active un **HMR** (Hot Module Reload), ce qui recharge automatiquement ton navigateur quand tu modifies tes assets (fichier CSS ou JS). Pratique lors du développement !

Pour que le HMR s'exécute également quand tu modifies un fichier Twig, ajoute les quelques lignes ci-dessous à ton fichier webpack.config.js en prenant soin de retirer au préalable la toute dernière ligne module.exports = Encore.getWebpackConfig();

``` js
//supprime la dernière ligne
// module.exports = Encore.getWebpackConfig();

// et remplace par ceci
const fullConfig = Encore.getWebpackConfig();
fullConfig.devServer = {
    watchFiles: {
        paths: ['templates/**/*.html.twig'],
    },
};
module.exports = fullConfig;
```

``` sh
yarn build
```
Compile les assets pour un environnement de production (les fichiers sont notamment minifiés pour en limiter la taille).

Quelle que soit la commande choisie, cela a pour effet de compiler les fichiers contenus dans `assets/` et générer les fichiers finaux, utilisés par ton projet. Le dossier `assets/` n’étant pas directement accessible par le navigateur, les fichiers sont générés par Webpack dans le dossier `public/build/`.
Par exemple, tu travailleras sur un fichier `app.scss` dans `assets/` et celui-ci sera compilé en un fichier `app.css` dans le répertoire `/public/build`.
Il ne faut donc jamais modifier celui qu'il y a dans `/public/build`, cela sera écrasé lors du prochain chargement de WebPack.

Pour intégrer les fichiers style.css et script.js, on ne va donc pas utiliser les adresses suivantes : `href="/build/app.css"` ou `src="/build/app.js"`. Car si on modifie le `setOutputPath` de ton fichier `webpack.config.js`, il faudra modifier à la fin tous les chemins vers les assets. Pour pallier ce problème (et gérer également d’autres cas plus complexes, automatiquement), un helper Twig est disponible pour charger tes CSS et JS, respectivement `{{ encore_entry_link_tags('app') }}` et `{{ encore_entry_script_tags('app') }}` ou le app est le nom donné à ton fichier, sans l’extension .css ou .js.

``` twig
{% block stylesheets %}
    {{ encore_entry_link_tags('app') }}
{% endblock %}
```

``` twig
{% block javascripts %}
    {{ encore_entry_script_tags('app') }}
{% endblock %}
```

## 3.6. Gestion des images

Les images font également partie des assets (images "décoratives" de ton site et non les fichiers uploadés par l'utilisateur).On peut créer un sous-dossier `images/` dans `assets/`. Pour que ces images soient buildées par webpack, il faut rajouter quelques lignes de configuration :

``` js
// webpack.config.js

Encore
    // ...
    .setOutputPath('public/build/')

    .copyFiles({
        from: './assets/images',

        // optional target path, relative to the output dir
        to: 'images/[path][name].[ext]',

        // if versioning is enabled, add the file hash too
        //to: 'images/[path][name].[hash:8].[ext]',

        // only copy files matching this pattern
        //pattern: /\.(png|jpg|jpeg)$/
    })
```

Il peut être nécessaire de lancer cette commande :
``` sh
yarn add file-loader@^6.0.0 --dev
```

Pour faire référence à ces images depuis Twig, utilise le helper :
``` twig
<img src="{{ asset('build/path_to_image.png') }}" alt=""/>
```

## 3.7. Installation de librairies tierces avec Webpack Encore


On pourra avoir besoin de charger un certain nombre de librairies dans tes projets, par exemple `Bootstrap` (cette fois-ci, on parle bien du framework CSS) et pourquoi pas un compilateur `SCSS`. Cela tombe bien, Encore possède des documentations ou des options par défaut pour ces différentes librairies.

Par exemple, pour utiliser `SCSS` dans ton projet, il te suffit de décommenter l’option .`enableSassLoader()` dans le fichier `webpack.config.js`. Si tu lances Webpack juste après, tu vas avoir un message d’erreur t’invitant à installer les dépendances requises. Il faudra donc taper dans ton terminal :

``` sh
yarn add sass-loader@latest sass --dev
```

Pour tester, renomme le fichier `assets/styles/app.css` en `assets/styles/app.scss`, puis modifie le fichier `assets/app.js` pour qu’il charge le fichier `app.scss` et non plus `app.css:`

Relance le build de Webpack, par exemple avec la commande :
``` sh
yarn watch
```
afin de voir si cela fonctionne. Normalement, un fichier `app.css` a dû se créer dans le dossier `build/`. Oui, rappelle-toi, la compilation du `SCSS` donne un fichier `CSS` qui, lui, va être interprétable par ton navigateur.

https://symfony.com/doc/current/frontend/encore/css-preprocessors.html

## 3.8. Installation de bootstrap

``` sh
yarn add bootstrap --dev
```
https://symfony.com/doc/current/frontend/encore/bootstrap.html



[Return to Top](#notes-symfony)
# 4. **Création de la page d’accueil**

## 4.1. Créer le premier contrôleur

Un **contrôleur** en Symfony n'est pas différent d'un **contrôleur** en MVC : c'est tout simplement une **classe**.
Elle doit étendre `Symfony\Bundle\FrameworkBundle\Controller\AbstractController`. Cette classe va également contenir des **méthodes** (appelées *actions*), qui seront appelées via le mécanisme de **routing**.

Par convention, le nom de ces classes est suffixé par `Controller`, par exemple, `ForumController`. Tu en déduiras facilement le nom du fichier : `ForumController.php`.

On va placer ce controller dans le dossier `src/Controller/`. Dans l'absolu, un contrôleur peut vivre n'importe où. Certaines librairies fournissent même leurs propres contrôleurs, se trouvant donc dans le dossier vendor/nom_de_librairie/.

Exemple :

``` php
<?php
// src/Controller/ProgramController.php
namespace App\Controller;

use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Response;

class ProgramController extends AbstractController
{
    public function index(): Response
    {
        return new Response(
            '<html><body>Wild Series Index</body></html>'
        );
    }
}
```

Il ne faut pas oublier le nom du **namespace**. Tous les controller doivent se trouver dans le namespace `App\Controller`.

**L'objet Response**

On observe que le controlle retourne un objet `Response` qui est retourné avec du HTML à l'intérieur.

C'est un objet qui représente une réponse `HTTP` **complète**. Dans une réponse HTTP, on peut trouver des **headers**, un **code de réponse** (2xx, 3xx, ...) et éventuellement un **contenu** (HTML, JSON, ...). C'est pareil pour l'objet  `Symfony\Component\HttpFoundation\Response de Symfony`.

Le **travail** d'un contrôleur de `Symfony` est de **retourner** un objet de la classe `Response`. **Tout le temps. Quoi qu'il arrive**. C'est une notion fondamentale à assimiler si on veux comprendre le fonctionnement du `framework`. Son objectif est de mettre à jour le modèle et/ou d'instancier la vue.

Ici notre réponse HTML est "écrite en dure", mais ça changera par la suite.

https://symfony.com/doc/current/introduction/http_fundamentals.html#symfony-response-object

https://symfony.com/doc/current/page_creation.html#creating-a-page-route-and-controller


## 4.2. Implémenter la route

Maintenant que le **controller** est créé, il va falloir le lier à une **route** pour le tester !  
Une **route**, finalement, ce n'est que de la *configuration*. Tu peux généralement la configurer de plusieurs manières, au format annotation, YAML, XML, PHP... ou via les **attributs** (recommandé).

Les **attributs** (attributes en anglais) sont une nouvelle syntaxe apportée par `PHP8` et disponible depuis `Symfony 6`. Avant cela, la configuration utilisait les *annotations*. Tu risques encore de trouver **beaucoup** de documentation avec cette **ancienne syntaxe**.
Il existe donc **plusieurs manières** de configurer les routes, tu trouveras toutes ces informations dans la documentation, mais nous allons nous focaliser sur la nouvelle manière de faire avec les attributs.

**Le routing via les attributs**

Les **attributs** sont des morceaux de codes utiles pour définir des configurations. Ils s'écrivent sous la forme `#[attributeName(key: value)]`. Même si l'**attribut** commence par un '#' dans ce cas particulier il n'est pas considéré comme un commentaire. Ils viennent remplacer les **annotations** qui n'étaient pas natives de PHP mais reposaient sur des librairies tierces, mais l'idée est la même. Quelque part dans le code de `Symfony`, des **classes** sont écrites pour venir interpréter ces attributs et exécuter des actions en conséquence, mais c'est toutes la "magie" du **framework**, il effectue du travail pour te simplifier la vie sans que tu aies besoin de savoir ce qu'il fait en détail ;-) .


``` php
use Symfony\Component\Routing\Annotation\Route;

Class ProgramController extends AbstractController
{
    #[Route('/program/', name: 'program_index')]
    public function index(): Response
    {
        return new Response(
            '<!doctype html><html lang="en"><title>Wild Series</title><body>Wild Series Index</body></html>'
        );
    }
}
```

**Le routing via les annotations**

``` php
use Symfony\Component\Routing\Annotation\Route;

Class ProgramController extends AbstractController
{
    /**
     * @Route("/program/", name="program_index")
     */
    public function index(): Response
    {
        return new Response(
            '<!doctype html><html lang="en"><title>Wild Series</title><body>Wild Series Index</body></html>'
        );
    }
}
```

Que ce soit pour les attributs ou les annotations, le même `use Symfony\Component\Routing\Annotation\Route;` est utilisé.

Il faut maintenant lancer un serveur symfony (`symfony server:start`) et ouvre la route `http://localhost:8000/program/` qui devrait renvoyer une page blanche avec écrit "Wild Series index".

Note: le paramètre *name* de la route est facultatif mais **extrêmement utile**. Il sera détaillé plus tard mais il sert notamment pour générer une URL dynamiquement à partir d'un nom de route. Le premier paramètre, quant à lui, définit l'URL et est obligatoire.

https://symfony.com/doc/current/routing.html#creating-routes-in-yaml-xml-or-php-files
https://symfony.com/doc/current/routing.html


## 4.3. Appeler un template Twig : la vue 

Il est plus judicieux d'appeler un template **Twig** plutôt que de mettre du HTML à la main dans l'objet Response car cela ne respecte pas les principes de séparation **MVC** entre la vue et le contrôleur. **Twig** est présent dans l'installation de Symfony.

Il n'y a qu'à mettre à jour la méthode `index()` dans le contrôlleur `ProgramController` :

``` php
<?php
#[Route('/program/', name: 'program_index')]
public function index(): Response
{
    return $this->render('program/index.html.twig', [
       'website' => 'Wild Series',
    ]);
}
```
Puis à créer la vue dans `templates/program/index.html` associée. Dans Symfony, les vues se placent dans un dossier `templates/` en dehors de `src/` et Twig est préconfiguré pour y aller chercher les fichiers.

``` twig
<!doctype html>
<html lang="en">
<head>
   <meta charset="UTF-8">
   <title>Wild Series</title>
</head>
<body>
   <h1>{{ website }} index</h1>
</body>
</html>
```

Même si on ne voit pas explicitement la création d'un objet `Response`, `$this->render()` renvoie bien un objet de type `Response`.

Ici `{{ website }}` est passé en contexte depuis le contrôleur à ta vue. Pour l'exemple sa valeur est égale à “Wild Series”. Par conséquent si tu actualises ta page, ta vue à la route /program/ affiche "Wild Series index".

https://symfony.com/doc/current/best_practices.html

## 4.4. Et le modèle ?

Le modèle gère l’accès aux données (le plus souvent dans une database). Chaque **entité** correspondra à une classe, dans le dossier `src/Entity` .  
Par défaut, Symfony utilise **l'ORM Doctrine** pour accéder à la **base de données**, effectuer des **requêtes**, et faire le lien avec les entités.



[Return to Top](#notes-symfony)
# 5. **Routing Avancé**
## 5.1. Rappel

Les routes se configurent directement dans les contrôleurs à l'aide des attributs. Avant cela, la configuration utilisait les annotations. On risque encore de trouver beaucoup de documentation avec cette ancienne syntaxe.
Il existe par ailleurs d'autres manières de configurer les routes (XML, Yaml, PHP), accessible dans la documentation.

``` php
<?php
// src/Controller/ProgramController.php
namespace App\Controller;

use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;

class ProgramController extends AbstractController
{
   #[Route('/program/', name: 'program_index')]
   public function index(): Response
   {
       // return render twig
   }
}
```

Lorsque le router de symfony reçoit une requête vers la route `/program/`, il va regarder toutes les routes configurées dans l'application. S'il ne trouve pas la route, il renverra un code 404. Pour configurer les routes on utilise des **expressions régulières**. Si plusieurs définitions de route correspondent au même chemin c'est la première route rencontrée dans le fichier qui est prioritaire. Le routeur s'arrête dès qu'il a trouvé une correspondance.

- Pour lister les routes
``` sh
symfony console debug:router
```

https://symfony.com/doc/current/routing.html#debugging-routes


## 5.2. Les paramètres de route

On spécifie via les attributes, qu'une route attend un paramètre en incluant dans la route un {joker} (wildcard en anglais).

Pour afficher le programme ayant un id en particulier :

``` php
     [...]
     #[Route('/program/{id}', name:'program_show')]
     public function show(int $id): Response
     {
         return $this->render('program/list.html.twig', ['id' => $id]);
     }
```
On peut ajouter autant de paramètre que nécessaire de cette manière. Attention à la lisibilité.  
On peut ensuite récupérer le paramètre dans twig ou utiliser ce paramètre dans le contrôleur.

https://symfony.com/doc/current/routing.html#route-parameters

On peut rajouter une valeur par défaut de cette manière :

``` php
public function list(int $page = 1): Response
```

Dans ce cas, si l'on se rend sur la route `/program/` le paramètre page prendra la valeur de 1.

**Attention** : Suivant la même logique qu'en PHP, si un paramètre est déclaré optionnel, tous les autres paramètres lui succédant devront, eux aussi, être optionnels. Autrement dit, les **paramètres optionnels se situent toujours en fin de route** (et donc de méthode).

https://symfony.com/doc/current/routing.html#optional-parameters


## 5.3. Les contraintes de route

La route que l'on vient de faire nécessite un paramètre {page}. Logiquement, un numéro de page doit être un entier. Cependant, si tu ne fais aucun contrôle, il est tout à fait possible de saisir autre chose en paramètre, par ex /program/cinq/, ce qui pourrait poser problème. Il faut donc interdire cela :


``` php
 #[Route('/program/list/{page}', requirements: ['page'=>'\d+'], name: 'program_show')]
  public function show(int $page = 1): Response
  {
      // ...
  }
```

En ajoutant l'option `requirements`, on peut ajouter des prérequis aux différents paramètres. Ici le prérequis est `\d+`. C'est une **expression régulière** qui correspond à un chiffre répété de 1 à n fois, autrement dit un entier. Les requirements sont toujours définis par une regex, qui est un moyen simple et puissant de décrire des motifs variables.

https://symfony.com/doc/current/routing.html#parameters-validation

## 5.4. Les méthodes HTTP

Certaines routes ne devraient être accessibles qu'en GET, d'autres qu'en POST (et pareillement avec d'autres verbes HTTP). Quelques exemples :

``` php
#[Route('/program/new', methods: ['GET', 'POST'], name: 'program_new')]
#[Route('/program/{id}', methods: ['GET'], name: 'program_show')]
#[Route('/program/{id}', methods: ['DELETE'], name: 'program_delete')]
```

Les routes `program_show` et `program_delete` ont la même définition `/program/{id}`, mais la méthode HTTP définie n'étant pas la même, il n'y a pas de conflits entre elles.
Le router les considère bien comme deux routes différentes et saura quelle méthode appeler en fonction de la méthode HTTP utilisée.

Note : Les routes d'API se reposent beaucoup sur ces contraintes de méthodes HTTP.
https://symfony.com/doc/current/routing.html#special-parameters
https://fr.wikipedia.org/wiki/Hypertext_Transfer_Protocol#M%C3%A9thodes

## 5.5. Les préfixes de route

Le préfixe s'applique à la classe d'un contrôleur afin - comme son nom l'indique - de préfixer les routes contenues dans ce contrôleur. La syntaxe est exactement la même que pour les méthodes.
Il est également possible de spécifier un name afin de préfixer tous les noms de routes des méthodes d'un contrôleur.


``` php
use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;

#[Route('/program', name: 'program_')]
class ProgramController extends AbstractController
{

     // Correspond à la route /program/ et au name "program_index"
     #[Route('/', name: 'index')]
     public function index(): Response
     {
         // ...
     }

     // Correspond à la route /program/new et au name "program_new"
     #[Route('/new', name: 'new')]
     public function new(): Response
     {
         // ...
     }
}
```

https://symfony.com/doc/current/routing.html#route-groups-and-prefixes


## 5.6. Utiliser et générer les routes

**Dans un controlleur**

L'utilisation la plus fréquente des routes au sein d'un contrôleur est la redirection (en `GET`), suite à la validation d'un formulaire par exemple.

``` php
public function new(): Response
{
    // traitement d'un formulaire par exemple
    // redirection vers la page 'program_show',
    // correspondant à l'url /program/4
    return $this->redirectToRoute('program_show', ['id' => 4]);
}
```

La redirection revient au même que de taper l'url dans le navigateur, et donc le code de la méthode `show()` correspondant à la route `/program/4` va bien s'exécuter et l'éventuelle vue associée s'affichera donc. Pour rappel, après une redirection, les données disponibles (en POST par exemple, ici celles de la page new), sont perdues.

https://symfony.com/doc/current/controller.html#redirecting

**Dans un template twig**

Si on veut mettre un lien dans un template twig on peut procéder ainsi :

``` twig
<a href="/program/list/5">Afficher la page 5</a>
```

Mais si on modifie la définition de la route, le lien ne fonctionnera plus. Pour faire un lien de manière plus robuste, on utilise la fonction `{{path()}}` de twig qui sert à appeler la route prédéfinie. Il faut lui donner le **nom**, d'où l'intérêt de bien définir le name de chacune des routes, et une **liste optionnelle de paramètres**.

``` twig
<a href="{{ path('program_show', {page: 5}) }}">Afficher la page 5</a>
```

https://symfony.com/doc/current/templates.html#linking-to-pages

[Return to Top](#notes-symfony)
# 6. **Doctrine**

https://symfony.com/doc/current/doctrine.html

C'est ici que l'on va parler du **modèle**. Le modèle manipule les **données**. Le plus souvent ces **données** sont stockées dans une base de données (mais pas systématiquement : fichiers, XML, API...). Dans le cas d'une **BDD**, le modèle va exécuter les **requêtes** SQL.

Un **DBAL** (DataBase Abstraction & Access Layer) est une **interface** entre une application et sa **BDD**.

Un **ORM** (object relational mapping) est une couche d'**abstraction** entre le monde objet et le monde relationnel. Il permet de faire le **lien** (mapping) entre les **objets** de l'application et les éléments de la **BDD**. Il existe de nombreux outils d'ORM selon les langages (JAVA : hibernate ; JS : Mongoose, Sequelize ; PHP : Eloquent, **Doctrine**, POMM). **Doctrine** permet donc de manipuler directement des objets PHP au lieu de manipuler la base de données avec des requêtes SQL.

**Doctrine** est ce que l’on appelle un **ORM** et une **DBAL**.

![doctrine](./img/54.png)

https://www.quora.com/What-are-the-pros-and-cons-of-using-raw-SQL-versus-ORM-for-database-development

Si on utilisel'option `--webapp` quand on installe un projet symfony, Doctrine est déjà installé, sinon il faut utiliser la commande :

``` sh
composer require symfony/orm-pack
composer require symfony/maker-bundle --dev
```

Configuration du fichier env.local pour MySQL :

``` sh
DATABASE_URL="mysql://your_username:your_pwd@127.0.0.1:3306/wild-series?serverVersion=8&charset=utf8mb4"
```

En production, il faut configurer le serveur via la commande :
``` sh
SetEnv DATABASE_URL mysql:/wilder:wcs@localhost/my_db
```
ou via l'interface d'adminsitration du serveur.

https://symfony.com/doc/current/doctrine.html

L'utilisation de doctrine est **facilitée** par la console de **Symfony**. Beaucoup moins de tâches réalisées “à la main” ! C’est Doctrine qui s’en charge à partir de maintenant. La **création**, **modification** de la structure de la DB, se fait en ligne de commande.

Pour créer la base de donnée :
``` sh
symfony console doctrine:database:create
# ou symfony console d:d:c
```
Cette commande s'appuie sur les **variables d'environement** renseignées précédemment.

## 6.1. Créer une entité avec Doctrine

Une **entité** est une simple **classe**. La plupart du temps, une **entité** représente une **table** de la base de données, et chaque **propriété** de l'entité, un **champ** de la table. Mais ça n'est pas obligatoirement le cas. Les **clés étrangères** sont représentées par d'autres entités. On les trouve dans le dossier `src/Entity`. La classe doit avoir les getters et les setters correspondant et peut également contenir d'autres méthodes supplémentaires.


``` sh
symfony console make:entity
```

Symfony t'indique tout ce que tu dois remplir :
- **Nom** de l'entité
- **Propriétés** de l'entité : on peut en ajouter autant que tu le souhaites.
- **Type** des propriétés. Ainsi que les spécificités du type. Exemple : int, string, longueur de chaîne...
- Les propriétés sont elles **nullables** ou non ? Est ce que ce champ dans la table a le droit d’être vide ?

Exemple de classe générée :

``` php
<?php
namespace App\Entity;

use App\Repository\CategoryRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: CategoryRepository::class)]
class Category
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(length: 255)]
    private ?string $name = null;

   /* getters / setters */
}
```
A chaque fois que l'on génère une entité en ligne de commande, il crée spontanément une propriété clé primaire nommée `id` (Generated Value). On n'a donc pas à spécifier le champ "id".  
Un fichier Repository/****Repository.php est également généré. Il contiendra les méthodes effectuant les requêtes BDD.  
Les getters et les setters sont aussi générés.


Une fois toutes ces informations renseignées, Symfony t'indique que la classe est créée avec succès, mais la base de données n'est pas encore à jour.

https://symfony.com/doc/current/doctrine.html#creating-an-entity-class

Il faut maintenir mettre à jour la BDD :

``` sh
symfony console make:migration
```

**Doctrine Migration** génère une classe avec un numéro de version qui correspond à un état de la base de données. On y trouvera  deux méthodes :
- Une contenant un script pour monter de version ta base de données
- Une autre contenant un script pour revenir sur la version précédente. Très important, si jamais il y avait un problème lors du déploiement.  

En gros, pour chaque ordre SQL, Doctrine Migration va générer son ordre SQL inverse.

``` php
namespace DoctrineMigrations;

use Doctrine\DBAL\Schema\Schema;
use Doctrine\Migrations\AbstractMigration;

/**
 * Auto-generated Migration: Please modify to your needs!
 */
final class Version20210805173740 extends AbstractMigration
{
    public function getDescription(): string
    {
        return '';
    }

    public function up(Schema $schema): void
    {
        // this up() migration is auto-generated, please modify it to your needs
        $this->addSql('CREATE TABLE category (id INT AUTO_INCREMENT NOT NULL, name VARCHAR(255) NOT NULL, PRIMARY KEY(id)) DEFAULT CHARACTER SET utf8mb4 COLLATE `utf8mb4_unicode_ci` ENGINE = InnoDB');
    }

    public function down(Schema $schema): void
    {
        // this down() migration is auto-generated, please modify it to your needs
        $this->addSql('DROP TABLE category');
    }
}
```

Pour exécuter cette migration (et réellement impacter le schéma de la base de données), il suffit de lancer la commande :
``` sh
symfony console doctrine:migrations:migrate
# ou symfony console d:m:m
```
https://www.doctrine-project.org/projects/doctrine-migrations/en/current/reference/introduction.html#introduction


### 6.1.1. Mise à jour d'une entité avec Doctrine

``` sh
symfony console make:entity --regenerate
```

Cette commande permet, à partir d'une entité comportant uniquement des propriétés, de générer les getters / setters ainsi que certaines autres méthodes utiles pour les mappings plus complexes.
Attention à garder ta classe "propre". En effet, si tu supprimes des propriétés, la commande ne va pas supprimer les getters / setters automatiquement. Elle ne fait que de l'ajout.

### 6.1.2. Détection des entités 

``` sh
symfony console doctrine:mapping:info
```

### 6.1.3. Validation des entités
``` sh
symfony console doctrine:schema:validate
```

### 6.1.4. Pour contrôler les migrations
``` sh
symfony console doctrine:migrations:status
```

Cette commande indique toutes les informations concernant le paramétrage de Doctrine Migration, ainsi que l'état de la base de données.

On peut aussi exécuter des migrations de manière unitaire, c’est-à-dire en lancer une seule à la fois avec la commande
``` sh
symfony console doctrine:migrations:execute. 
```

En exécutant tes migrations de manière unitaire tu peux choisir la méthode que tu vas lancer de la migration de ton choix: `up` ou `down` . C’est très utile si tu exécutes une migration et que tu te rends compte qu’elle est fausse, dans ce cas il te faudra exécuter la méthode `down` pour revenir à l’état antérieur :

``` sh
symfony console doctrine:migrations:execute 'DoctrineMigrations\<nom_de_classe_de_ta_migration>' --down
```

Pour exécuter une migration dans le sens inverse

``` sh
symfony console doctrine:migrations:execute 'DoctrineMigrations\<nom_de_classe_de_ta_migration>' --up
```
https://symfony.com/doc/current/doctrine.html#migrations-adding-more-fields

### 6.1.5. Après chaque mise à jour de la BDD

Après chaque mise à jour de l'entité il faut synchroniser avec la BDD. Il n'est plus nécessaire de faire des requêtes SQL, cette synchronisation se fait à l'aide des **migrations** :
``` sh
//Génération d une classe de migration
symfony console make:migration
//Application des modifications de la BDD
symfony console doctrine:migrations:migrate
//Vérifie si la BDD est synchronosée avec l application
symfony console doctrine:schema:validate
```

## 6.2. Récupérer des données stockées avec Doctrine


Pour cela, il y a les méthodes de récupération d'objets par entité, à savoir :
- findAll()
- findOneBy(...)
- findBy(...)

À chaque fois que l'on va requêter sur une entité pour créer des objets, on vas utiliser une classe de repository qui lui est associée. Par exemple, pour l'entité `Program`, c'est la classe `ProgramRepository` du fichier `src/Repository/ProgramRepository.php` qui va être utilisée. Doctrine a directement généré ce fichier lors de la création de `Program`.

``` php
class ProgramRepository extends ServiceEntityRepository
{
    public function __construct(ManagerRegistry $registry)
    {
        parent::__construct($registry, Program::class);
    }

    public function save(Program $entity, bool $flush = false): void
    {
        $this->getEntityManager()->persist($entity);

        if ($flush) {
            $this->getEntityManager()->flush();
        }
    }

    public function remove(Program $entity, bool $flush = false): void
    {
        $this->getEntityManager()->remove($entity);

        if ($flush) {
            $this->getEntityManager()->flush();
        }
    }
}
```
- possèdent des méthodes génériques pour récupérées les données héritéés de `ServiceEntityRepository`.
- propose de base les méthodes save() et remove()
- destinés à contenir nos propres requêtes personnalisées lorsque les requêtes génériques ne sont plus suffisantes.

### 6.2.1. Récupération simple

Dans un contrôleur, récupération de l'objet de type Family, relié au `Character`
``` php
// return a Family object
$family = $character->getFamily(); 
```
Via Twig :
Attention Twig ne peut pas afficher les objets, il faut préciser les clés :
``` twig
{{ character.family.name }}
{{ character.family.banner }}
```

### 6.2.2. findAll()


``` php
 #[Route('/', name: 'index')]
    public function index(ProgramRepository $programRepository): Response
    {
         $programs = $programRepository->findAll();

         return $this->render(
             'program/index.html.twig',
             ['programs' => $programs]
         );
    }
```


Pour récupérer un objet `$programRepository` dans Symfony, tu ne vas pas faire un `new` directement, mais plutôt `ProgramRepository $programRepository` en paramètre de méthode d'un contrôleur. Symfony instancie alors "**tout seul**" l'objet nécessaire, ce mécanisme appelé "**injection de dépendance**" et très utilisé dans Symfony, te sera expliqué plus en détail dans une prochaine quête.

Ici, la variable `$programs` se voit affecter le retour de la **méthode** `findAll()` de ProgramRepository. `findAll()` retourne tous les éléments présents dans la table sous forme d'un **tableau d'objets**. Ce tableau sera envoyé à la vue program/index.html.twig.(il fait un SELECT * FROM program en base de données). 

Contrairement aux autres méthodes find(), celle-ci ne prend aucun argument.

### 6.2.3. findOneBy() : récupérer un objet unique selon différents paramètres


``` php
#[Route('/show/{id<^[0-9]+$>}', name: 'show')]
public function show(int $id, ProgramRepository $programRepository):Response
{
    $program = $programRepository->findOneBy(['id' => $id]);
    // same as $program = $programRepository->find($id);

    if (!$program) {
        throw $this->createNotFoundException(
            'No program with id : '.$id.' found in program\'s table.'
        );
    }
    return $this->render('program/show.html.twig', [
        'program' => $program,
    ]);
}
```

On récupère ici le repository de la classe `Program`, afin d'utiliser cette fois-ci la méthode de classe `findOneBy(...)` qui a pour but de sélectionner strictement une seule ligne en base de données (un équivalent de SELECT * FROM program WHERE id=`$id`), en fonction de son `id` (qui est unique). Attention, ici on récupère donc `$program` (directent un objet `Program` correspondant à l'id) et non pas un tableau d'objets `Program` comme avec le `findAll()`.


Les méthodes `findOneBy()` et `findBy()` peuvent être utilisées de différentes manières. On peut sélectionner directement la propriété sur laquelle rechercher l’information, notamment grâce à la méthode magique `__call()` émulant un appel de méthode. On a pour exemples : `findOneByNomDuChamp()`, `findOneById()`, `findOneByName()`.
Par conséquent, `findOneBy(['id' => $id])` aurait pu s'écrire `findOneById($id)`.
À ce tableau associatif, on peux ajouter d’autres filtres ou champs comme un ordre de tri ou encore une limite. N’hésite pas à regarder les ressources !
De plus, il existe une méthode `find($id)` qui est un raccourci pour `findOneById($id`).

https://symfony.com/doc/current/doctrine.html#fetching-objects-from-the-database

Autre exemple :
``` php
$characters = $characterRepository->findByLastName('Snow');  
// SELECT * FROM `character` WHERE last_name = 'Snow';

$character = $characterRepository->findOneByFirstName('Jon');  
// SELECT * FROM `character` WHERE first_name = 'Jon' LIMIT 1;
```


### 6.2.4. findBy() : récupérer plusieurs objets selon différents paramètres

``` php
#[Route('/{categoryName}', name: 'show')]
    public function show(string $categoryName, ProgramRepository $programRepository, CategoryRepository $categoryRepository)
    {
        $category = $categoryRepository->findOneBy(['name' => $categoryName]);

        if (!$category) {
            throw $this->createNotFoundException(
                '404 - No category with name : '.$categoryName.' found in category\'s table.'
            );
        }

        $programs = $programRepository->findBy(
            ['category' => $category],
            ['id' => 'DESC'],
            3
        );

        return $this->render('category/show.html.twig', [
            'programs' => $programs,
            'category' => $category,
        ]);
    }
```
Autre exemple :
``` php
$characters = $characterRepository->findBy(
   ['firstName' => 'Jon', 'lastName' => 'Snow'],
   ['age' => 'DESC'],
   5,
   0
);
// SELECT * FROM `character`
// WHERE first_name = 'Jon' AND last_name = 'Snow'
// ORDER BY age DESC
// LIMIT 0, 5;
```

### 6.2.5. find(mixec $id)

Récupère un seul résultat en fonction d'un id. Équivaut à findOneById($id)
``` php
$character = $characterRepository->find(5);  
// SELECT * FROM `character` WHERE id=5;
```
## 6.3. Manipulation des données avec Doctrine

### 6.3.1. Ajouter une nouvelle donnée

``` php
#[Route('/new', name: 'character_new')]
public function add(CharacterRepository $characterRepository) :Response
{
  // declare a new Character
  $character = new Character();

  // set character properties
  $character->setFirstName('Ned');
  $character->setLastName('Stark');

  // insert in database
  $characterRepository->save($character, true);

  return $this->redirectToRoute('character_index');      
}
```
La classe `CharacterRepository` propose une méthode `save()`. 
Un second paramètre (optionnel) true est nécessaire pour exécuter la requête SQL.

### 6.3.2. Modifier une donnée

``` php
#[Route('/edit/{id}', name: 'character_edit')]
public function edit(Character $character, CharacterRepository $characterRepository) :Response
{
  // change or set character properties
  $character->setFirstName('Ned');
  $character->setLastName('Stark');
  $characterRepository->save($character, true);

  return $this->redirectToRoute('character_index');
}
```
Cette méthode `save()` sert aussi bien à l'**ajout** qu'à l'**édition**

### 6.3.3. Supprimer une donnée


``` php
#[Route('/{id}', name: 'app_category_delete', methods: ['DELETE'])]
public function delete(Character $character, CharacterRepository $characterRepository): Response
{
  $characterRepository->remove($character, true);

   return $this->redirectToRoute('character_index');
}
```
La classe `CharacterRepository` propose également une méthode `remove()`
Un second paramètre true est là encore nécessaire pour exécuter la requête SQL (delete)

Remarque : Si plusieurs `save()` / `remove()`  on peut mettre le true que sur le dernier appel. Toutes les requêtes SQL "en **attente**" seront alors **exécutées**.

### 6.3.4. Utilisation directe de doctrine

``` php
#[Route('/new', name: 'character_new')]
public function add(ManagerRegistry $doctrine) :Response
{
 $entityManager = $doctrine->getManager();
 // declare a new Character
 $character = new Character();

 // set character properties
 $character->setFirstName('Ned');
 $character->setLastName('Stark');
 $entityManager->persist($character);
 // declare object to doctrine (no SQL query is done)
 $entityManager->flush();

 return $this->redirectToRoute('character_index');     
}
```
- **Injection** d'un objet `ManagerRegistry` (doctrine)
- **Recupération** d'un Manager
- `persist()` permet de prendre en compte l'objet Character par doctrine
- `flush()` exécute la requête SQL


## 6.4. Utiliser le QueryBuilder

On utilise le **Query Builder** quand les méthodes génériques (findAll(), findBy(), getters etc.) **ne permettent pas** de récupérer les éléments souhaités. Ces requêtes sont à **créer** dans les classes **Repository**.

Exemple :
``` php
class CharacterRepository extends ServiceEntityRepository
{
   public function findCharactersByName(string $name): array
   {
       $query = $this->createQueryBuilder('c')
           ->where('lastName LIKE :name')
           ->setParameter('name', $name . '%')
           ->getQuery();

       return $query->getResult();
   }
}
```
Les **requêtes** SQL sont construites avec une approche "**objet**", ce qui rend la construction de requêtes complexes plus **facile**. Dans ces requêtes, il faut utiliser les noms de propriétés/classe d'entité (et nom les champs/tables de la base de données), (par ex : lastName et non last_name !)

Exemple :
``` php
class CharacterRepository extends ServiceEntityRepository
{
   public function findCharacterByName(string $lastname, string $firstname): array
   {
       $query = $this->createQueryBuilder('c')
           ->andWhere('lastName = :lastname')
           ->andWhere('firstName = :firstname')
           ->setParameters(['lastname' => $lastname, 'firstname' => $firstname]);

       return $query->getOneOrNullResult();
   }
}
```
- Plusieurs `where` et plusieurs paramètres
- La méthode retournera un objet Character ou null et non un tableau d’objet comme retourné par getResult()


Exemple plus complexe :
Si besoin d'une **jointure**, il est nécessaire de créer une requête personnalisée dans la classe **Repository**
Utilisation de la méthode `join()` dans le **query builder**. La table est référencée par le nom de la **propriété** définie dans l'**entité** et non par le nom de la table dans la base de données
``` php
class CharacterRepository extends ServiceEntityRepository
{
   public function findCharactersByFamily(string $familyName): array
   {
       $query = $this->createQueryBuilder('c')
  		->join('c.family', 'f')
  		->where('f.name LIKE :familyname')
  		->setParameter('familyname', $familyName. '%')
  		->getQuery();
       return $query->getResult();
   }
}

```
- Plusieurs `where` et plusieurs paramètres
- La méthode retournera un objet Character ou null et non un tableau d’objet comme retourné par getResult()

Méthode DQL :
``` php
class CharacterRepository extends ServiceEntityRepository
{
   public function findCharactersByName(string $name): array
   {
       $query = $this->getEntityManager()->createQuery(
           'SELECT c
           FROM App\Entity\Character c
           WHERE c.name LIKE :name'
       )->setParameter('name', $name . '%');

      return $query->getResult();
   }
}
```
Il faut privilégier l'approche avec  `createQueryBuilder()` qui génère au final du DQL.


À des fins de tests, on peut taper directement une requête SQL en ligne de commande :
``` sh
symfony console doctrine:query:sql 'SELECT * FROM product'
```
Cela permet d’écrire une requête SQL,  sans changer d’interface.

https://stackoverflow.com/questions/24340729/query-builder-where-in-arraycollection
https://stackoverflow.com/questions/40502052/doctrine-querybuilder-where-in-collection
https://symfonycasts.com/screencast/doctrine-relations/collection-criteria
https://stackoverflow.com/questions/43073982/doctrine-how-to-check-if-a-collection-contains-an-entity
https://stackoverflow.com/questions/59287955/symfony-querybuilder-filter-collection-in-query
https://www.doctrine-project.org/projects/doctrine-orm/en/current/reference/query-builder.html
https://www.developpez.net/forums/d2103709/php/bibliotheques-frameworks/symfony/symfony-5-query-builder-plusieurs-innerjoin-clauses-where/

## 6.5. Relation avec Doctrine : Exemple avec la Many-To-One

**Doctrine** prend en charge les **relations** entre les différentes tables de la BDD en s'occupant de **créer** les **clés étrangères** et de **générer** les tables intermédiaires.

https://symfony.com/doc/4.4/doctrine/associations.html

Dans l'exemple d'une table `Program` et d'une table `Category`. Il semble évident qu'une `Category` peut contenir plusieurs `Program`. C'est donc une relation de type `ManyToOne`.

Doctrine est un ORM et le **“O”** veut dire **Object**. Et comme son nom l’indique, il ne fonctionne qu'avec des objets. Cela va donc se traduire par une nouvelle propriété `category` dans l'entité `Program`. Cette propriété n'aura pas un type "**basique**" (string, integer...) mais un type "**Relationships”** (Associations).

Du côté logiciel, il faudra donc penser dorénavant en terme d’interactions entre différents objets.

Cependant, rien ne change pour ton SGBD ! Il fonctionne de la même manière ! Ainsi au niveau base de données, cette relation "objet" sera traduite par une clé étrangère (category_id) dans la table program. Et comme d’habitude au niveau de la base de données, ça sera bien un integer qui sera stocké.

Il ne faut pas qu'il y ait de confusion à ce sujet : l'ORM gère des objets, la base de données gère des données "basiques" (integer, char, varchar, float...). Les entités que tu manipules et les tables sont très proches, mais il subsiste quand même certaines différences, qui font qu’on ne peut pas dire que “une entité = une table”.

https://www.doctrine-project.org/projects/doctrine-orm/en/2.9/reference/association-mapping.html

### 6.5.1. Créer la relation dans Symfony

Dans la relation Many-To-One ici Many `Program` To One `Category`, c'est la table `Program` qui va être propriétaire de la relation qui va posséder la clé étrangère pointant vers la table `Category`. On pourra donc avoir plusieurs `Program` associés à la même `Category`.

``` sh
symfony console make:entity
```
Lorsque l'on indique en `Class name` le nom d’une entité déjà existante, Doctrine va comprendre que l'on souhaite y ajouter une propriété.

Les relations sont à indiquer dans le `field type`.

Si dans la classe Program on ajoute une relation de type `ManyToOne`, on obtient cela dans le fichier `Program.php`

``` php
#[ORM\ManyToOne()]
#[ORM\JoinColumn(nullable: false)
private ?Category $category;
```
https://symfony.com/doc/current/doctrine/associations.html#the-manytoone-onetomany-association


On a rajouter la relation entre ces deux entités au sein de ton application. Mais il faut garder en tête que l'entité n’est pas directement reliée à ta base de données.

Ensuite il faut passer à l'étape de la migration en exécutant les deux commandes suivantes :

``` sh
symfony console make:migration
symfony console doctrine:migrations:migrate
```

## 6.6. Relation avec Doctrine : Exemple avec la One-To-One

Exemple d'un personnage qui possèderait un seul animal qui ne pourrait être posséder que par une seule personne. On obtiendrait :

``` php
#[ORM\Entity(repositoryClass: PetRepository::class)]
class Pet
{
// other properties and their getters and setters…
#[ORM\OneToOne()]
  private ?Character $owner = null;

  public function getOwner(): ?Character
  {
      return $this->owner;
  }

  public function setOwner(?Character $owner): self
  {
      $this->owner = $owner;

      return $this;
  }
}
```

La relation est définie en attribut avec #[ORM\OneToOne()]. La méthode `getOwner()` renvoie un objet `Character` (même si en DB, la relation est faite par une clé étrangère de type INT.)

La classe `Pet` a une propriété `$owner` (et le getter associé `getOwner()`). Par conséquent, on peut récupérer un personnage depuis un animal :
``` php
$pet->getOwner(); // return a Character object
```
Le retour sera un objet `Character`, correspondant au personnage possédant le familier. 

Par contre, le `Character` ne dispose pas de base de l’information Pet. Donc à partir d’un personnage, comment récupérer l’animal de compagnie ?
``` php
$character->getPet(); // not working
```
Pour que ça fonctionne, Il faut spécifier que la relation est **bidirectionnelle** ! Ce n’est pas obligatoire, mais ça peut être très pratique si on veut récupérer de l’information dans les deux sens ! Attention à ne faire que si c’est utile.

La **bidirectionnelle** n’a aucun effet sur la BDD, c’est une **fonction supplémentaire** apportée par **Doctrine**.


## 6.7. Les relations bidirectionnelles avec Doctrine

On a créé la relation `Many-To-One` afin d’associer un objet de type `Category` à un objet de type `Program`. On a alors dans ta classe `Program` un attribut `$category` qui fait "**référence**" à la catégorie de ta série en question.
Ainsi, tu es capable, depuis l’instance d’un objet `Program`, de faire : `$category = $program->getCategory()`, ce qui te renvoie une instance de la classe `Category` avec comme valeurs d’attributs, les informations contenues en base de données.

Par contre, cette relation ne va que dans un seul sens, et tu ne peux pas effectuer la demande inverse, à savoir : `$category->getPrograms()`. C'est cela que l’on appelle relation **unidirectionnelle**.

Pour que ta relation soit **”bidirectionnelle”**, il faut que ta classe `Category` ait aussi une "référence" vers ses `programs`. Pour cela, il faut lui ajouter une propriété `$programs.` Ainsi, tu auras une relation à "**double sens**" et tu seras capable de récupérer la **catégorie d'une série, mais aussi les séries d'une catégorie**.

### 6.7.1. Créer la relation avec Symfony : Many-To-One

Lorsque l'on crée une entité avec Doctrine, cette question est posée :

```sh
Do you want to add a new property to Category so that you can access/update Program objects from it - e.g. $category->getPrograms()? (yes/no) [yes]:
```

Il faut répondre oui ! Et c'est tout !


Ainsi dans la classe Program on va avoir :
```php
#[ORM\ManyToOne(inversedBy: 'programs')]
private ?Category $category = null;
```
La mention `inversedBy="programs"` dans l’annotation a été rajoutée.
Cela fait référence à l'attribut `$programs` dans la classe Category que l'on va rajouter.

Et dans la classe `Category` on va avoir :
1. L'ajout d'un attribut $programs (au pluriel) et son annotation :
```php
#[ORM\OneToMany(mappedBy: 'category', targetEntity: Program::class)]
private $programs;
```
Dans l'annotation de l'attribut `$programs`, il y a une mention `mappedBy="category"` qui fait référence à l'attribut $category de la classe Program.


2. L'ajout du constructeur avec à l'interieur l'initialisation de l'attribut `$programs` qui est une nouvelle instance de ArrayCollection :
```php
public function __construct()
{
    $this->programs = new ArrayCollection();
}
```

3. L'ajout du getter de cet attribut :
```php
public function getPrograms(): Collection
{
    return $this->programs;
}
```
4. L'ajout d’une méthode pour ajouter une série à une catégorie et une autre pour la supprimer.

```php
public function addProgram(Program $program): self
{
    if (!$this->programs->contains($program)) {
        $this->programs->add($program);
        $program->setCategory($this);
    }

    return $this;
}

public function removeProgram(Program $program): self
{
    if ($this->programs->removeElement($program)) {
        // set the owning side to null (unless already changed)
        if ($program->getCategory() === $this) {
            $program->setCategory(null);
        }
    }

    return $this;
}
```
https://www.doctrine-project.org/projects/doctrine-orm/en/2.9/reference/association-mapping.html

https://symfony.com/doc/5.3/doctrine/associations.html#mapping-the-manytoone-relationship

https://www.doctrine-project.org/


### 6.7.2. Retour sur l'exemple One-To-One

```php
#[ORM\Entity(repositoryClass: CharacterRepository::class)]
class Character
{ 
   #[ORM\OneToOne(mappedBy: 'owner', targetEntity: Pet::class)]
   private $pet;

   public function getPet(): ?Pet
   {
       return $this->pet;
   }

   public function setPet(?Pet $pet): self
   {
       if ($pet === null && $this->pet !== null) {
           $this->pet->setOwner(null);
       }

       if ($pet !== null && $pet->getOwner() !== $this) {
           $pet->setOwner($this);
       }
       $this->pet = $pet;
       return $this;
   }
}
```

La relation bidirectionnelle est définie en annotation :
- #[ORM\OneToOne()] qui demande la targetEntity, ici `Pet`
- La propriété de `Pet` qui fait le lien avec le `Character`, ici owner. Ceci est spécifié via le paramètre mappedBy: 'owner'

Le setter `setPet()` possède le code permettant de mettre à jour la relation depuis un Character directement, en faisant appel au `setOwner()` de Pet.


Pour terminer la configuration de la **bidirectionnelle**, il faut également modifier **l’annotation** du côté de l’entity `Pet`, en ajoutant le paramètre `inversedBy` et en lui spécifiant la propriété de l’entité `Character` qui lui est reliée, ici pet

``` sh
#[ORM\OneToOne(inversedBy: 'pet', targetEntity: Character::class, cascade: ['persist', 'remove'])]
private $owner;
```
Optionnellement, il est également possible de déterminer le comportement des cascades.
Dans notre exemple, si le Character est supprimé, le Pet associé le sera également.

Toute cette génération peut se faire directement via la console.
Si la bidirectionnelle est modifiée manuellement, il est possible de re-générer les getters/setters


## 6.8. Relation avec Doctrine : Exemple avec la Many-To-Many

Exemple : Many Characters To Many Episodes.
Des épisodes peuvent contenir plusieurs personnages et des personnages peuvent apparaître dans plusieurs épisodes dans la table intermédiaire Apperance.

``` php
//Character.php
#[ORM\ManyToMany(inversedBy: 'characters', targetEntity: Episode::class)]
#[ORM\JoinTable(name: 'appearance')]
private $episodes;

public function __construct()
{
    $this->episodes = new ArrayCollection();
}

public function getEpisodes(): Collection
{
    return $this->episodes;
}

public function addEpisode(Episode $episode): self
{   // ...   }

public function removeEpisode(Episode $episode): self
{   // ...   }
```

La relation est définie en annotation avec `#[ORM\ManyToMany()]` qui demande en paramètre
l’entité ciblée par la relation (targetEntity), ici l’entité Episode.

Si la bidirectionnelle est configurée (il faut choisir un sens **“prioritaire”** à la relation), il faut ajouter `inversedBy` et le nom de la propriété associée dans l’entité Episode, ici characters (au pluriel car il y a plusieurs personnages par épisode)

Par défaut, une table character_episode sera créée, mais pas l'entity correspondante. Étant donné que la nouvelle table n'est là que pour stocker des identifiants, et qu'avec l'ORM, on manipule directement des objets plutôt que des entiers représentant d'autres entités, on n'a donc pas besoin de l'entité correspondante. Si le nom doit-être différent, il faut le spécifier via l'attribute `JoinTable`

``` php
//Episode.php
#[ORM\ManyToMany(mappedBy: 'episodes', targetEntity: Character::class)]
private $characters;

public function __construct()
{
  $this->characters = new ArrayCollection();
}

public function getCharacters(): Collection
{
  return $this->characters;
}

public function addCharacter(Character $character): self
{ // ... }

public function removeCharacter(Character $character): self
{ // ... }
```
La **bidirectionnelle** se définit sur la propriété `$characters` et nécessite `#[ORM\ManyToMany()]` avec une `targetEntity`, ici `Character` ET un `mappedBy`, ici la propriété `episodes` de `Character`

Toute ces configurations (méthodes get, add, remove, ArrayCollection dans le __construct()...)  sont réalisées automatiquement par la commande make:entity.

Toujours vérifier que la configuration est bonne avec :

``` sh
symfony console doctrine:schema:validate
```

**Remarque** : Symfony **gère** tout seul la **table intermédiaire**, du moment que celle-ci ne nécessite pas de champ supplémentaire. Dans le cas **contraire**, il faudra créer une **classe pour la table intermédiaire** et gérer alors **deux relations ManyToOne** entre celle-ci et les deux autres tables à relier. 

https://symfonycasts.com/screencast/collections/many-to-many-extra-fields

https://symfonycasts.com/screencast/collections/saving-inverse-side-collection
https://symfonycasts.com/screencast/collections/by-reference-adder-remover#play

https://symfonycasts.com/screencast/collections/synchronizing-mapping-inverse#play



https://www.doctrine-project.org/projects/doctrine-orm/en/2.13/tutorials/pagination.html#pagination





[Return to Top](#notes-symfony)
# 7. **Les fixtures**

Les fixtures, ou l'art de créer des jeu de données de test pour nos applications web !
Lors du développement d'une application, il est souvent nécessaire d'avoir du contenu. Les fixtures vont permettrent de générer des jeux de données cohérents.

Il faut installer le composant DoctrineFixturesBundle à la main :

``` sh
composer require --dev orm-fixtures
```
Grâce à Symfony flex, il n'y a rien d'autre à faire pour l'installer.

C'est un composant qui n'est utilisable qu'en développement.

## 7.1. Utilisation simple des fixtures

``` sh
symfony console make:fixtures //+ en entityFixtures
```
Qui va créer un fichier CategoryFixtures :
``` php
<?php

namespace App\DataFixtures;

use App\Entity\Category;
use Doctrine\Bundle\FixturesBundle\Fixture;
use Doctrine\Persistence\ObjectManager;

class CategoryFixtures extends Fixture
{
    public function load(ObjectManager $manager)
    {
        $category = new Category();
        $category->setName('Horreur');
        $manager->persist($category);
        $manager->flush();
    }
}
```
Si on analyse le code ci-dessus, on peut voir :
1. Ligne 5, la référence à l'entité que tu vas manipuler,
2. Ligne 11, la méthode load qui est appelée lors du chargement des fixtures,
3. Ligne 13, l'instanciation d'un nouvel objet Category,
4. Ligne 14, la définition du nom de cette nouvelle catégorie,
5. Lignes 15 et 16, la persistance en base de données.

Ce qu'il faut retenir ici, c'est qu'il faut instancier un nouvel objet, lui attribuer les propriétés nécessaires via ses setters et enfin le persister en base de données.

On peut réaliser des boucles dans les fixtures pour avoir d'avantage de données :
``` php
    for ($i = 1; $i <= 50; $i++) {  
        $category = new Category();  
        $category->setName('Nom de catégorie ' . $i);  
        $manager->persist($category);  
    }  
    $manager->flush();
```

`flush` est sorti de la boucle. Il est impératif de persister chaque objet, l'appel à la méthode `flush` n’est nécessaire qu'une seule fois. On doit limiter au maximum le nombre de `flush` et faire appel à la méthode une fois tous les éléments persistés. Le risque est de **saturer** ta mémoire et de **provoquer** une erreur.

**Limites** : les données sont peu réalises et se ressemblent toutes.

Si on veut du contenu plus concret on peut tout à fait créer un tableau dans la fixture et boucler sur le tableau :

``` php
public const CATEGORIES = [
        'Action',
        'Aventure',
        'Animation',
        'Fantastique',
        'Horreur',
    ];

public function load(ObjectManager $manager)
{
    
    foreach (self::CATEGORIES as $categoryName) {  
        $category = new Category();  
        $category->setName($categoryName);  
        $manager->persist($category);
    }  
    $manager->flush();
}
```

**Limites** : plus compliqué de charger un grand nombre de données.

https://symfony.com/bundles/DoctrineFixturesBundle/current/index.html#writing-fixtures

Une fois la classe créée, il faut l’exécuter.

``` sh
symfony console doctrine:fixtures:load
```
A chaque chargement de fixtures, toute la base de données est **entièrement vidée**. Ceci afin d'avoir un contenu cohérent, et éviter d'avoir des données orphelines ou des incohérences dans les relations entre les clés primaires et étrangères.

Si on veut rajouter des données sans écraser :
``` sh
php bin/console doctrine:fixtures:load --append
```

Il faut **générer/mettre à jour** les fixtures à chaque **création/modifitation** d'une entité.

A chaque nouveau pull de dev :
- Application des migrations pour que la BDD soit à jour
``` sh
symfony console doctrine:migrations:migrate
```
- Générer les fixtures :
``` sh
symfony console doctrine:fixtures:load
```


## 7.2. Utilisation avancée des fixtures

Dans le cas de tables **relationnelles**, il faut s'assurer du bon **ordre** du remplissage des tables. Avant de remplir la table **program**, il faut remplir la table **category** car la table **program** dépend de la table **category**.

### 7.2.1. Ajouter des références aux fixtures

On va voir comment créer des fixtures avec des entités comportant des dépendances.
On se rappelle qu'un `Program` peut avoir une seule `Category` et qu'une `Category` peut être utilisée dans plusieurs `Program`.

Pour l'entité `Category`, au niveau des fixtures, on va ajouter des références qui vont pouvoir être utilisée dans les fixtures de l'entité `Program`.

``` php
class CategoryFixtures extends Fixture
{
    public const CATEGORIES = [
        'Action',
        'Aventure',
        'Animation',
        'Fantastique',
        'Horreur',

    ];
    public function load(ObjectManager $manager)
    {
        foreach (self::CATEGORIES as $categoryName) {
            $category = new Category();
            $category->setName($categoryName);
            $manager->persist($category);
            $this->addReference('category_' . $categoryName, $category);
        }
        $manager->flush();
    }
}
```

La nouvelle ligne :

``` php
$this->addReference('category_' . $categoryName, $category);
```

Le **premier paramètre** est le nom que l'on décide de donner à la référence (on utilise la clé du tableau pour avoir une référence différente pour chaque catégorie créée).
Le **second paramètre** est l'objet fraichement créé.

Ceci permet de mettre de côté cet objet `$category` afin de pouvoir l'utiliser quand par exemple nous écrirons les fixtures d'un `Program` (qui a besoin d'un objet `Category` pour être créé). Chaque référence doit avoir un nom unique qui sera récupéré ensuite.

Pour charger les fixtures :
``` sh
# symfony console doctrine:fixtures:load
# Ou pour aller plus vite :
symfony console d:f:l
```

### 7.2.2. Utilisation des références

Pour pouvoir créer des fixtures de `Program`, il a fallu au préalable des catégories car l'objet `Program` est dépendant d'une catégorie.

On va créer `ProgramFixtures` à l'aide de la commande :

``` sh
symfony console make:fixtures
```

Pour indiquer à l'ORM que `Program` est dépendant de fixtures existantes et donc qu'il doit les insérer en base après on va devoir implémenter l'interface `DependentFixtureInterface` dans `ProgramFixtures`. Cette interface nous imposera d'implémenter la méthode `getDependencies()`.
Cette méthode devra retourner un tableau comportant le FQCN de chaque classe de fixtures dont Program dépend.

``` php
namespace App\DataFixtures;

use App\Entity\Program;
use Doctrine\Bundle\FixturesBundle\Fixture;
use Doctrine\Common\DataFixtures\DependentFixtureInterface;
use Doctrine\Persistence\ObjectManager;

class ProgramFixtures extends Fixture implements DependentFixtureInterface
{
    public function load(ObjectManager $manager)
    {
        $program = new Program();
        $program->setTitle('Walking dead');
        $program->setSynopsis('Des zombies envahissent la terre');
        $program->setCategory($this->getReference('category_Action'));
        $manager->persist($program);
        $manager->flush();
    }

    public function getDependencies()
    {
        return [
          CategoryFixtures::class,
        ];
    }
}
```
https://symfony.com/bundles/DoctrineFixturesBundle/current/index.html#sharing-objects-between-fixtures

Il faut maintenant jouer les fixtures :
``` sh
# symfony console doctrine:fixtures:load
# Ou pour aller plus vite :
symfony console d:f:l
```
https://symfonycasts.com/screencast/symfony4-doctrine-relations/awesome-random-fixtures#dependentfixtureinterface

https://symfony.com/bundles/DoctrineFixturesBundle/current/index.html#loading-the-fixture-files-in-order


[Return to Top](#notes-symfony)
# 8. **FakerPHP**

https://fakerphp.github.io/
**FakerPHP** est une bibliothèque PHP qui nous permet de génerer des données aléatoirement en fonction de certains critères.

**Attention** ce ne sont pas de **vraies** données. En effet, l'**objectif** n'est pas d'avoir un jeu de données réel, mais plutôt de **remplir** sa base de données avec des objets **vraisemblable** et **aléatoirement** générées.

A chaque rechargement des fixtures, les données générées par FakerPhp seront remplacées par des nouvelles. C'est exactement ce que l'on cherche à faire ! Rien n'est plus mauvais que de constamment travailler avec les mêmes données, cela empêche de voir certains problèmes. FakerPhp nous assure des données toujours renouvelées, imprévisibles et donc parfaites pour nos tests !

## 8.1. Installation

``` sh
composer require fakerphp/faker
```

## 8.2. Utilisation

**FakerPhp** prend tout son sens lors de l'élaboration de fixtures, car il vient nous fournir des données générées là où il nous faudrait mettre une valeur pertinente (prénom, date, prix, email, téléphone, description, etc).

``` php
<?php

namespace App\DataFixtures;

use App\Entity\Season;
use Doctrine\Bundle\FixturesBundle\Fixture;
use Doctrine\Persistence\ObjectManager;
use Doctrine\Common\DataFixtures\DependentFixtureInterface;
//Tout d'abord nous ajoutons la classe Factory de FakerPhp
use Faker\Factory;

class SeasonFixtures extends Fixture implements DependentFixtureInterface
{
    public function load(ObjectManager $manager): void
    {
        //Puis ici nous demandons à la Factory de nous fournir un Faker
        $faker = Factory::create();
        /**
        * L'objet $faker que tu récupère est l'outil qui va te permettre 
        * de te générer toutes les données que tu souhaites
        */
        for($i = 0; $i < 50; $i++) {
            $season = new Season();
            //Ce Faker va nous permettre d'alimenter l'instance de Season que l'on souhaite ajouter en base
            $season->setNumber($faker->numberBetween(1, 10));
            $season->setYear($faker->year());
            $season->setDescription($faker->paragraphs(3, true));
            $season->setProgram($this->getReference('program_' . $faker->numberBetween(0, 5)));
            $manager->persist($season);
        }
        $manager->flush();
    }
    public function getDependencies(): array
    {
        return [
           ProgramFixtures::class,
        ];
    }
}
```

FakerPHP permet de générer toute sorte de données :
- `numberBetween()` : nombre aléatoire
- `paragraphs()` => permet de générer plusieurs paragraphes de texte.
- `firstName()` => permet de générer un prénom
- `lastName()` => permet de générer un nom de famille
- `city()` => permet de générer une ville
- `email()` => permet de générer une adresse email
- `password()` => permet de générer un mot de passe
- et encore beaucoup d'autres que tu pourras découvrir en parcourant la doc 😎. Tu peux aussi ajouter un paramètres pour gérer la **langue**, et ainsi générer des fixtures adaptées à chaque pays.


[Return to Top](#notes-symfony)
# 9. **Les Formulaires**

https://symfony.com/doc/current/forms.html#processing-forms

## 9.1. Créer un formulaire 

Dans Symfony, le composant `form` est installé par défaut avec l’option --webapp de la commande symfony. Mais il peut être utilisé en **standalone**, c’est-à-dire hors d’un projet Symfony.

``` sh
composer require symfony/form
```

Formulaire pour créer un nouveau personnage (partie de **C**RUD)

Objectif du form :  **hydrater** l'entité `Program`
=> le form doit contenir correspondre aux propriétés de l'entité


``` sh
symfony console make:form

The name of the form class (e.g. TinyChefType):
> ProgramType

The name of Entity or fully qualified model class name that the new form will be bound to (empty for none):
> Program
```

https://symfony.com/legacy/doc/forms/1_1/fr/01-form-creation

### La classe formulaire

La classe `ProgramType` est alors automatiquement générée dans le dossier `src/Form`, avec des champs correspondants à l’entité `Program` reliée.


``` php
class ProgramType extends AbstractType
{
    public function buildForm(FormBuilderInterface $builder, array $options): void
    {
        $builder
            ->add('title', TextType::class)
            ->add('synopsis', TextareaType::class)
            ->add('poster', FileType::class)
            ->add('category', null, ['choice_label' => 'name'])
        ;
    }

    public function configureOptions(OptionsResolver $resolver): void
    {
        $resolver->setDefaults([
            'data_class' => Program::class,
        ]);
    }
}
```

- Classe `ProgramType` (suffixe Type)
- Dans la méthode `buildForm()`, on retrouve les champs du formulaire (pré-générés par la console). De nombreuses options sont disponibles pour personnaliser les champs (types, label, attributs…)
- La méthode `configureOptions()` permet d’envoyer des informations (options) au formulaire.
- `'data_class' => Program::class`
Le plus souvent, un formulaire va travailler avec une entité (Doctrine). Une des ses responsabilités sera d’hydrater l’objet lors de sa soumission. 


### 9.1.1. Le contrôleur

Dans la méthode new() de `ProgramController`, 2 objets requis en paramètre : 
- un `Request` (requête HTTP)
- un `ProgramRepository` (traitement en DB).

``` php
#[Route('/new', methods: ['GET', 'POST'], name: 'new')]
public function new(Request $request, ProgramRepository $programRepository): Response
{
    $program = new Program();
    // Create the form, linked with $category
    $form = $this->createForm(ProgramType::class, $program);

    // Get data from HTTP request
    $form->handleRequest($request);

    // Was the form submitted ?
    if ($form->isSubmitted() && $form->isValid()) {
        // Deal with the submitted data
        // For example : persiste & flush the entity
        // And redirect to a route that display the result
        $programRepository->save($program, true);
        $program->getId(); //récupère l'id
        //Redirect to categories list
        // redirectToRoute(program_show, [ 'id' => $program->getId()]
        // pour rediriger vers la page du nouveau program
        return $this->redirectToRoute('program_index');
        }
    // Render the form (best practice)
    return $this->renderForm('category/new.html.twig', [
        'program' => $program,
        'form' => $form,
    ]);
}
```

Explication :
- **Nouvel** object `Program` instancié, il sera hydraté par les données du formulaire.

- La **méthode** `createForm()` va instancier un form du type demandé (**ProgramType::class**). Le **second paramètre** (optionnel) est l'objet à hydrater. S'il est omis, les données sont **récupérables** directement via `$form->getData()`.

- La **méthode** `handleRequest()` va reconnaître si le formulaire a été soumis et hydrater l'objet associé (ici `$program`). Attention, à ce stade les données n'ont pas encore été validées 

- La méthode `isSubmitted()` nous informe si le form a été soumis.

- La méthode `isValid()` va lancer les validations paramétrées pour ce form / cette entité.

- Si pas d'erreur (données "valides"), traitement des données du form. Ici, insertion en base de données.

- redirection HTTP en fin de requête via la méthode `$this->redirectToRoute('nom_de_la_route')` équivalent d'un `header('Location: ')`.

- La méthode `renderForm()` est utilisée (et non simplement render() dans le cas d'un form. Il faut également passer à la vue Twig l'objet `$form`.

### 9.1.2. La vue

Symfony embarque des extensions Twig avec le composant form de type `{{ form_xxx() }}`.  
Ajoute des fonctions dans Twig pour aider à l'affichage du formulaire envoyé à la vue.  
Dans le cas du **add**, le **form** peut être inclus pour être partagé avec la vue d'**update**

``` twig
//program/new.html.twig
{% extends 'base.html.twig' %}
{% block title %}New Program{% endblock %}

{% block body %}
   <h1>Create new Program</h1>
   {{ include('program/_form.html.twig') }}
   <a href="{{ path('program_index') }}">back</a>
{% endblock %}
```

``` twig
{{ form_start(form) }}
   {{ form_widget(form) }}
   <button class="btn">{{ button_label|default('Save') }}</button>
{{ form_end(form) }}
```
Un form commence par `form_start(form)` et fini par `form_end(form)` avec form en paramètre qui est le nom de la variable envoyé depuis le contrôleur.

Il est possible d'afficher le form de manière très rapide via `{{ form_widget(form) }}`. Fonctionne pour des formulaires très simples mais est très peu personnalisable.

``` twig
{{ form_start(form) }}
   {{ form_row(form.lastname) }}
   {{ form_row(form.firstname) }}
   <div>some HTML code between 2 form field</div>
   {{ form_row(form.family) }}
   <button class="btn">{{ button_label|default('Save') }}</button>
{{ form_end(form) }}
```

`form_row()` permet de gérer les champs un à un, utile pour
- changer l'ordre d'affichage des champs
- ajouter du code HTML entre chaque champ

un bloc `form_row` est constitué d'un <div> contenant 
- un label
- le champ 
- le message d'erreur associé au champ
- optionnellement un message d'aide

``` twig
{{ form_start(form) }}
<fieldset>
   {{ form_errors(form.lastname) }}
   {{ form_label(form.lastname) }}
   {{ form_widget(form.lastname) }}
   {{ form_help(form.lastname) }}

   {{ form_row(form.firstname) }}
</fieldset>
   <div>some HTML code between 2 form field</div>
   {{ form_row(form.family) }}
   <button class="btn">{{ button_label|default('Save') }}</button>
{{ form_end(form) }}
```
Il est possible d'aller encore plus dans le détail en appelant chaque partie séparemment

`form_errors(form.xxx)`
`form_label(form.xxx)`
`form_widget(form.xxx)`
`form_help(form.xxx) `(si défini dans la classe)

Il est possible de mixer les niveaux.

**Remarque** : si un élément du formulaire n'est pas explicitement appelé, il le sera automatiquement par form_end() et s'affichera donc tout en bas.

Il est possible de gérer la mise en forme automatique pour les formulaires (par formulaire ou de manière globale) comme appliquer les classes de base de Bootstrap aux formulaires.

- Pour tous les forms de l’application : dans le fichier config/packages/twig.yaml

``` yaml
twig:
   form_themes:
       - 'bootstrap_5_layout.html.twig'
```
POur un seul formulaire : dans la vue twig :

``` twig
{% form_theme form 'bootstrap_5_layout.html.twig' %}
```
Il faut avoir au préalable charger bootstrap dans le projet.

![formulaire](./img/51.png)

## 9.2. FormType

https://symfony.com/doc/current/reference/forms/types.html

### 9.2.1. Les éléments FieldType

Un formulaire est composé de champs. Dans la classe formulaire, chaque champ est ajouté via la méthode `add()` du `$builde`r. Le nom du champ vient en 1er paramètre :


``` php
public function buildForm(FormBuilderInterface $builder, array $options): void
{
     $builder
         ->add('firstName')
         ->add('lastName')
         ->add('family');
}
```

Mais il existe de nombreux types de champs 
- champs simples (text, date, number, email…)
- champs de choix (radio, checkbox, select)
- textarea, etc.

Le formulaire essaie de deviner le type approprié par rapport au type de base de données spécifié dans l'entité (s'il y en a une), par ex :

|             Type Doctrine                | Centré                        | 
| :--------------------------------------: |:-----------------------------:| 
| string (varchar)                         |   input type="text"           | 
| text                                     | textarea                      | 
| relation manyToOne                       | select                        | 
 
Cependant il n'y arrive pas toujours, et certains champs (email, url…) n'ont pas d'équivalent en db.

On a donc la possibilité de **spécifier** le type de champ souhaité, en second paramètre. Pour cela il faut indiquer une **classe** de type `FormTypes`.

Il en existe + de 40 différents, des plus basiques (`TextType`, `EmailType`, `TextareaType…`), aux plus spécialisés (`BirthdayType`, `CountryType…`) 

Remarque : attention à utiliser le bon `use`, certaines classe Doctrine ayant le même nom.

``` php
use Symfony\Component\Form\Extension\Core\Type\TextType;

public function buildForm(FormBuilderInterface $builder, array $options): void
{
     $builder
         ->add('firstName') // nothing, guess TextType
         ->add('lastName', TextType::class)
         ->add('family');
}
```
https://symfony.com/doc/current/reference/forms/types/choice.html

### 9.2.2. Les options

Un champ de formulaire peut prendre différentes **options** en fonction de son **type**, et des attributs **HTML** complémentaires (placeholder, class…)

La méthode `add()` **accepte** un 3ème paramètre, **tableau d'options** permettant de configurer finement chaque champ, mais également le label, une phrase d'aide, etc.

La documentation des `FormTypes` reprend en détail les options permises pour chaque type

https://symfony.com/doc/current/reference/forms/types.html

``` php
public function buildForm(FormBuilderInterface $builder, array $options): void
{
   $builder
       ->add('firstName')
       ->add('lastName', TextType::class, [
           'required' => false, // default is true
           'attr' => [
               'placeholder' => 'Doe',
               'class' => 'form-control',
           ],
           'label' => 'Family name',
           'label_attr' => [
               'class' => 'form-label'
           ],
           'help' => 'Please enter your name'
       ])
       ->add('family')
       ;
}
```

### 9.2.3. Le cas EntityType

https://symfony.com/doc/current/reference/forms/types/entity.html#basic-usage
https://symfony.com/doc/current/reference/forms/types/entity.html?fbclid=IwAR1yXXYEEe3E04bM1GzPpIhfXcYHaxznnopyHK0PKtZgyfVTKfHLT6zeXYQ#using-a-custom-query-for-the-entities

Lorsque le type associé à la propriété est une relation (`ManyToOne` par exemple), le champ de formulaire associé doit permettre le **choix** parmi les **enregistrements** déjà dans la base de données. 

Pour cela, il faut utiliser un type spécial, `EntityType`, qui étend `ChoiceType` et qui est rempli automatiquement avec les données d'une entité choisie, via doctrine.

Concrètement, cela se traduit par un champ **select**, **radio** ou **checkbox**.

``` php
class Character
{
    // ...

   #[ORM\ManyToOne(inversedBy: 'characters')]
   private ?Family $family = null;

}
```

``` php
$builder
       ->add('firstName')
       ->add('lastName', TextType::class, [
       ])
       ->add('family')
   ;
```

Le champ '`family`' est détecté comme **ManyToOne** relié à l'entité `Family`. Mais, le formulaire ne sait pas quel getter de Family il doit utiliser pour afficher dans le champ. On obtient alors l'erreur : *Objet of class App\Entity\Family could not be converted to string*.

``` php
$builder
       ->add('firstName')
       ->add('lastName', TextType::class, [
       ])
       ->add('family', EntityType::class, [
           'class' => Family::class,
           'choice_label' => 'name'
       ])
   ;
```
L'utilisation d'un `EntityType` impose la présence de deux options obligatoires
- `class` : l’entité liée
- `choice_label` : la propriété de l’entité liée à afficher

Le rôle de l'`EntityType` est d'aller récupérer en base de données toutes les données reliées à l'entité indiquée via Doctrine et ensuite d'afficher ces données dans un *select* (par défaut). Il faut biensur préciser le champ qui sera afficher dans le *select*. Symfony se base sur le `choice_label` qui doit correspondre au nom des propriétés de l'entité.

Remarque : (c'est `getName()` qui est en réalité utilisé, et non la propriété `$name` directement).

Pour afficher quelque chose de plus complexe dans le **select** (par exemple concaténer les valeurs de plusieurs champs de la BDD), tu peux créer un **getter** personnalisé, qui se chargera d’effectuer la mise en forme plus complexe, puis l’appeler dans le `choice_label`. Comme par exemple, mettre `'choice_label' => 'selector'` qui renverrait vers la méthode :

``` php
public function getSelector(): string
{
  return $this->getId() . ' - ' . $this->getName();
}
```
https://symfony.com/doc/current/reference/forms/types/entity.html#choice-label

On peut également rajouter des options supplémentaires. Si on prend le cas d'une entité `Program` dans lequel on a une propriété `$actors` (relation **ManyToOne**). Pour ajouter le champ correspondant dans le formulaire et ainsi rajouter des acteurs à un program on procède ainsi :

``` php
$builder
// add the 2 use
use App\Entity\Actor;
use Symfony\Bridge\Doctrine\Form\Type\EntityType;
// here, your form (title, summary…)
$builder->add('actors', EntityType::class, [
    'class' => Actor::class,
    'choice_label' => 'name',
    'multiple' => true,
    'expanded' => false,
]);
```
L'utilisation d'un `EntityType` propose d'autres paramètres optionnels comme :
- `expanded` et `multiple` qui peuvent prendre true ou false comme valeur. Par défaut ils sont à false. Le passage à true permet d'afficher la sélection sous forme de bouton radio ou de checkbox.
- `query_builder` : c'est la requête pour récupérer les informations en BDD. Par défaut il s'agit d'un simple `SELECT * FROM table`. Or parfois on peut vouloir trier les résultats (**ORDER BY**), en afficher qu'une partie (**LIMIT**) ou mettre une condition (**WHERE**).

Pour que l'enregistrement se fasse dans les deux sens (relation bilatérale)

``` php
$builder
// add the 2 use
use App\Entity\Actor;
use Symfony\Bridge\Doctrine\Form\Type\EntityType;
// here, your form (title, summary…)
$builder->add('actors', EntityType::class, [
    'class' => Actor::class,
    'choice_label' => 'name',
    'multiple' => true,
    'expanded' => false,
    'by_reference' => false,
]);
```


### 9.2.4. Imbrication de formulaires 

Il est également possible d’imbriquer un form dans un form (documentation).

Les éléments de formulaire étendent `Symfony\Component\Form\AbstractType`.
Les formulaires étendent `Symfony\Component\Form\AbstractType`.

La méthode `add()`du FormBuilder attend un **AbstractType** en second paramètre, on peut donc sans soucis intégrer une classe de form dans un form !

Ex : une entité `Pet` possède une relation `OneToOne` vers `Character` (pour laquelle il y a déjà un form `PetType` de créé) et tu souhaites avoir un seul formulaire pour éviter de faire deux écrans :

``` php
#src/Form/CharacterType
$builder
    ->add('pet', PetType::class);
```
Remarque : dans le cas de relation `OneToMany` ou `ManyToMany`, il te faudra utiliser des CollectionType (permettant d'imbriquer de multiples sous-formulaires)


Méthode magique __tostring() transfomer un objet en string pour en faire un select

ou

->add('categoriesé, null, 'choicelabel => 'id')

[Return to Top](#notes-symfony)
# 10. **Validation des formulaires**


## 10.1. Fonctionnement

Dans Symfony, les vérifications des données côté serveur se font via un composant dédié : le composant `Validator`, installé par défaut par le website-skeleton (option --webapp de l’installateur Symfony). 

Ce composant permet:
- d’écrire des validations rapidement
- de gérer des messages d’erreur adaptés et est facilement extensible pour des cas plus complexes
- permet également d’afficher sans effort les éventuelles erreurs dans la vue du formulaire.

On va se servir à nouveau des attributes pour configurer les validations.


Ces attributes vont être écrits dans tes fichiers **d’Entity** car les entités caractérisent les données. Il faut tout d’abord faire un `use Symfony\Component\Validator\Constraints as Assert`.

Cette dernière est sous la forme `#[Assert\TypeDeContrainte()]` et se place au-dessus d’une propriété dans la classe. Il existe un grand nombre de contraintes pré-disponibles dans Symfony, pour tester si la donnée n’est pas vide, sa longueur, son type, etc. Exemple :


``` php
use Symfony\Component\Validator\Constraints as Assert;

class Category
{
    #[Assert\NotBlank]
    public $name;

    //...
}
```
Ici, la contrainte `NotBlank` permet de vérifier qu’une valeur associée à la propriété name d’un objet de type `Category` n’est pas "vide". En ajoutant cette contrainte, si l’utilisateur outrepasse les validations côté client, il ne passera pas la méthode `->isValid()` utilisée dans le controller. Rq : black signifie une chaîne vide une fois le trim effectué dessus.

Il est bien entendu possible (et souvent nécessaire) de cumuler plusieurs `#[Assert]`. En effet, il est également intéressant ici de tester la longueur maximale du champ. Voici un exemple plus complet :

``` php
use Symfony\Component\Validator\Constraints as Assert;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: CategoryRepository::class)]
class Category
{
    #[ORM\Column(type: 'string', length: 255)]
    #[Assert\NotBlank]
    #[Assert\Length(max: 255)]
    private $name;
}
```
Depuis Symfony 4.4 si aucune validation n'est définie sur une entité mais qu'elle possède une attributes `#[ORM]`, alors le composant `Validator` s’appuie par défaut sur ce qui est défini pour **Doctrine** et applique les **validations** correspondantes, ce qui évite un certain nombre de "**répétitions**" entre ce qui est défini en `#[Assert]` et en `#[ORM]`.

Il faut activer spécifiquement cette fonctionnalité en ajoutant au dessus du nom de la classe, l'attribute * `#[Assert\EnableAutoMapping]`. Une fois cela fait, pour reprendre l’exemple ci-dessus, puisqu’on définit une longueur de **255 caractères** pour le champ (via le `#[ORM\Column]` et que ce dernier n’est pas défini comme **nullable**, le `Validator` ajoute tout seul la contrainte sur la longueur de la chaîne correspond et le non nullable. 

**Attention**, seul un **petit** nombre de contraintes qui peuvent ainsi être **automatiquement** validées. Pour tout le reste, il faudra toujours le définir **manuellement**.

Les contraintes possèdent également des paramètres (optionnels ou non, en fonction des cas).
- `NotBlank` peut rester sans paramètre
- `Length` demandera au moins de lui indiquer une taille minimum ou maximum.

Chaque contrainte affiche un message d’erreur par défaut (en anglais). Il est parfois utile de le personnaliser. Pour ce faire, il faut utiliser le paramètre correspondant. Il est possible d’y afficher la valeur actuelle erronée, via le placeholder `{{ value }}` ; ainsi que la valeur ou contrainte attendue (si cela est pertinent), via `{{ limit }}` :

``` php
#[ORM\Column(type: 'string', length: 255)]
#[Assert\NotBlank(message: 'Ne me laisse pas tout vide')]
#[Assert\Length(
    max: 255,
    maxMessage: 'La catégorie saisie {{ value }} est trop longue, elle ne devrait pas dépasser {{ limit }} caractères',
)]
private $name;
```

Si tu veux que tous les messages d'erreur soient automatiquement en français (et non plus en anglais), tu peux modifier la langue "par défaut" de Symfony dans le fichier `config/packages/translation.yaml` en modifiant la ligne `default_locale: en` en `default_locale: fr`.

https://symfony.com/doc/current/validation.html
https://symfony.com/doc/current/reference/constraints/Length.html
https://symfony.com/doc/current/doctrine.html#validating-objects


## 10.2. Les différentes contraintes

Il en existe actuellement une **cinquantaine** que l'on peut configurer comme vu précédemment, et Symfony en ajoute régulièrement de nouvelles. Elles permettent de répondre à la grande **majorité** des besoins en termes de **vérification** de données. Il est également possible de configurer des contraintes personnalisées plus complexes si besoin. Ces contraintes sont toutes listées sur la documentation officielle. Elles sont organisées en plusieurs catégories dont voici quelques exemples :

- **basiques** : vérification d’existence d’une valeur (null ou vide), vérification du type d’une valeur (string, int…)
- **chaînes de caractères** : tests sur les longueurs, vérification sur les formats (email, url, adresse IP) ou personnalisée via la contrainte Regex permettant de définir une expression régulière.
- **comparaison** : vérification si la valeur saisie est égale, différente, plus grande ou plus petite qu’une valeur attendue.
- **Date** : test si la valeur est bien de format date (ou datetime ou time).
- **Choix** : test si la valeur fait partie d’une liste préétablie par le développeur, ou de listes préconfigurées dans Symfony (liste des pays, des langues, des devises, etc.) correspondant à certains standards ISO.
- **fichiers** : utile pour l’upload notamment. Sert à vérifier si un fichier a la bonne extension, ne dépasse pas la taille requise. Il existe même des contraintes propres aux fichiers images, sur la taille de l’image en pixels, son ratio, etc.
- **financières** : vérifie si la valeur correspond bien à un format de code BIC, de carte bleue, IBAN, etc. Utile pour du paiement en ligne, par exemple.

Autres contraintes : vérifier l’unicité d’une valeur, créer des contraintes personnalisées, etc.

https://symfony.com/doc/current/validation.html#constraints
https://symfony.com/doc/current/validation/custom_constraint.html



## 10.3. Lancer la validation

Le composant formulaire de Symfony est lié au composant validator. Pour le valider, il suffit d’utiliser la méthode isValid() du formulaire :
``` php
   // $form initialization

   if ($form->isSubmitted() && $form->isValid()) {
    // handle data, in example, an insert into database
    // redirection
   }

// form rendering
```

La méthode `isValid()` retourne un booléen. Elle doit être appelée au moment de la soumission du formulaire et juste après `$form->isSubmitted()`. En effet, il est logique de ne valider les données d’un formulaire qu’une fois celles-ci soumises.

Sur l’exemple de code ci-dessus, si le formulaire n’est **pas valide**, ni l’insertion en base de données, ni la redirection ne sont effectuées et le formulaire est donc **ré-affiché**. Dans ce cas les **erreurs** vont être récupérées automatiquement dans le formulaire et apparaître à l’écran (l’helper Twig `{{ form_errors() }}` permet d’en personnaliser l’affichage).

**Remarque** : l’ajout de certaines contraintes va directement affecter l’affichage d’un formulaire relié à cette entité. Par exemple, si tu ajoutes une contrainte **Length** avec un maximum de 10 caractères sur une propriété donnée, un attribut `maxlength=10` est ajouté automatiquement à l’input correspondant dans le formulaire. Cela permet d’avoir **automatiquement** une **cohérence** entre les vérifications d’erreur côté **client** et côté **serveur**.

https://symfony.com/doc/current/validation/groups.html


## 10.4. Sécurisation des failles CSRF

Symfony embarque également un composant de **sécurité** au niveau du form, qui évite les **failles** de type **CSRF** (Cross-Site Request Forgery).

Symfony ajoute un **champ caché** de sécurité (`token CSRF`) automatiquement dans tous les forms. Ce **token** est **vérifié** à chaque requête et s'**assure** ainsi que les données postées **proviennent bien** du site en cours d’utilisation et qu’elles ne sont pas trop **datées** (durée de vie du token limitée). 
Cela **évite** par exemple une attaque **bruteforce** sur un form de login depuis un client HTTP

Cette protection est **activée par défaut**. Ajout ce champ caché en fin de formulaire lors de l’appel du form_end (la balise <form></form> ne doit donc jamais être écrit à la main dans les vues).

https://symfony.com/doc/current/forms.html
https://symfony.com/doc/current/components/form.html




[Return to Top](#notes-symfony)
# 11. **ParamConverter**

## 11.1. Le principe du ParamConverter

**Avant :**
``` php
#[Route('/program/{id}/', name: 'program_show')]
public function show(int $id, ProgramRepository $programRepository): Response
{
  $program = $programRepository->find($id);
  return $this->render('program/show.html.twig', ['program' => $program]);
}
```
1. On **récupère** l'identifiant unique d'un program : l'`id`. 
2. On **passe** ce paramètre issu de ta route en paramètre à ta méthode du **controller**.
3. La variable `$id` est utilisée pour **récupérer** le Program avec l'id correspondant, via la méthode `find()` de ProgramRepository.

**Rappel** : la méthode find() est l'équivalent de findOneById().


**Maintenant :**  
Pour passer un paramètre de route à un objet comme on vient de le faire, le param converter peut nous faire gagner du temps et des lignes de code. C'est un mécanisme activé par défaut dans symfony :

``` php
#[Route('/program/{id}/', name: 'program_show')]
public function show(Program $program): Response
{
  return $this->render('program.html.twig', ['program'=>$program]);
}
```
On obtient directement l'objet `Program` qui correspond à l'`id` saisi dans ta route. Comment cela fonctionne ?

Le paramètre de la méthode est directement `$program`. Ce qui est important ici, c'est son type : `Program`.

On a typé le paramètre pour lui dire que l'on voulait un objet `Program`, mais on a entré un **integer** correspondant à l'`id`. Il y a donc eu une **conversion automatique** de ton paramètre ! Le param converter n'est donc rien de plus !

Si on indiques que l'on souhaite un objet de type `Program`, il va automatiquement effectuer la requête `find()` du premier exemple.

**Attention :** pour que cela fonctionne, il faut que le paramètre (ici `{id}`) corresponde à une **propriété** de ton entité et qu'il s'agisse d'un champ **unique** (c’est le cas ici, puisque le champ id est une primary key) ! Il s'agit bien du **nom** de la **propriété** de l'**entité** et non pas du nom du champ en base de données (bien que parfois identique).

Autre exemple :

``` php
#[Route('/character/{id}', name: character_details)]
public function showCharacter(Character $character)
{
  // ...
}
```
Symfony va automatiquement aller chercher un objet Character ayant un ID de la même valeur que passée dans l’url.

Ce tour de “magie” est rendu possible par l’utilisation implicite du ParamConverter.

https://symfony.com/doc/current/SensioFrameworkExtraBundle/annotations/converters.html
https://symfonycasts.com/screencast/symfony3-doctrine-relations/param-conversion


## 11.2. Utilisation avancée du Param Converter

Dans certains cas, depuis une **route**, tu as besoin de récupérer des informations de plusieurs **entités**, mais on ne peut pas avoir deux fois le même paramètre.
Imaginons que l'on souhaite afficher la critique d'une série par exemple.
Dans ce cas, la route `@Route("/program/{id}/comment/{id}")` ne serait pas valide. Il faut utiliser des noms de paramètre différents.

**Solution 1 :** Utiliser un nom de paramètre identique au nom de l'entité
``` php
/**
 * @Route("/program/{program}/comment/{comment}", name="program_show_comment")
 */
public function showProgramComment(Program $program, Comment $comment): Response
{
  return $this->render('comment.html.twig', [
    'program' => $program,
    'comment' => $comment,
  ]);
}
```

Lorsque le **param converter** rencontre un **paramètre** portant le **même nom** que l'**entité**, il cherchera alors à **utiliser l'id** pour faire la **conversion**. Cela permet alors de lever l'ambiguïté.

**Solution 2 :** Mapper manuellement le paramètre à la propriété de l'entité

``` php
#[Route('/program/{program_id}/comment/{comment_id}', name: 'program_show_comment')]
#[Entity('program', options: ['mapping' => ['program_id' => 'id']])]
#[Entity('comment', options: ['mapping' => ['comment_id' => 'id']])]
public function showProgramComment(Program $program, Comment $comment): Response
{
  return $this->render('comment.html.twig', [
    'program' => $program,
    'comment' => $comment,
  ]);
}
```
Ici les **paramètres** ont un nom **différent** de l'**entité**. Ça ne peut pas fonctionner, puisque l'entité Program ne contient pas de propriété `$program_id` et Comment de propriété `$comment_id`. Il faut alors ajouter un attribute supplémentaire `#[Entity()]` qui va permettre d'indiquer correctement le lien entre paramètres et propriétés d'entité (attention à bien ajouter le `use Sensio\Bundle\FrameworkExtraBundle\Configuration\Entity;` en début de fichier.

Dans l'exemple ci-dessus on indique que le paramètre `program_id` doit être considéré comme correspondant à la propriété `$id` de l'entité `Program` et que le paramètre `comment_id` doit être considéré comme correspondant à la propriété `$id` de l'entité `Comment`.

## 11.3. Date Converter

Le terme de **param converter** est souvent utilisé pour les **Doctrine** **converters**, c'est-à-dire transformer un paramètre de **route en entité** Doctrine. Cependant, ils peuvent servir à d'**autres conversions paramètre > objet**. Un exemple concret est le **Date Converter** qui transforme un paramètre au format "**date**" automatiquement en un objet **Datetime**.

``` php
#[Route('/wild/historic/{start}')]
public function historic (\DateTime $start): Response
{
  // si {start} est au format 'YYYY-mm-dd', $start est converti en un objet \DateTime
  // par exemple : /wild/historic/2025-09-18
}
```
Ici, si `{start}` est au format date par défaut (`YYYY-mm-dd`, mais des options supplémentaires permettent d'ajuster ce comportement), alors le **Date Converter** fait son travail et la chaîne de caractères est convertie automatiquement en objet `\Datetime`, car le paramètre `$start` de la fonction `historic()` est typé en ce sens.

https://symfony.com/bundles/SensioFrameworkExtraBundle/current/annotations/converters.html#datetime-converter

https://symfony.com/doc/current/best_practices.html#use-paramconverters-if-they-are-convenient

https://symfony.com/bundles/SensioFrameworkExtraBundle/current/annotations/converters.html#built-in-converters




[Return to Top](#notes-symfony)
# 12. Sessions et Messages flash


## 12.1. Les sessions sous Symfony

Sous **symfony** on n’utilisera **JAMAIS** directement la variable superglobale `$_SESSION`. On utilisera à la place une **surcouche objet**.

Pour utiliser les **sessions**, il faut récupérer un **objet** de type `Session`, depuis un objet `RequestStack`. Grâce au **type hinting**, tu vas injecter l’objet `RequestStack` dans ton contrôleur (ou dans un Service) puis utiliser sas méthode `getSession()` :

``` php
use Symfony\Component\HttpFoundation\Session\SessionInterface;

#[Route('/program')]
class ProgramController extends AbstractController
{
    #[Route('/', name:'program_index')]
    public function index(RequestStack $requestStack) : Response
    {
        $session = $requestStack->getSession();
        // some code using $session
    }
}
```

Dans Symfony, il n’est pas nécessaire de démarrer la session via `session_start()`, cela est **géré automatiquement** dès qu’une session est requise.

Ensuite, plutôt que d’ajouter ou supprimer une **clé/valeur** au tableau `$_SESSION`, on utilisera différentes méthodes de l’objet `$session`, dont les trois principales :
- `has()` qui permet de **tester l’existence** d’une clé en session,
- `set()` qui permet **d’ajouter** une paire clé/valeur à la session
- `get()` qui permet de **récupérer** la valeur associée à une clé en session,

Exemple : si l'on souhaite récupérer un total antérieurement stocké en session :
``` php
public function index(RequestStack $requestStack) : Response
{
    $session = $requestStack->getSession();
    if (!$session->has('total')) {
        $session->set('total', 0); // if total doesn’t exist in session, it is initialized.
    }

    $total = $session->get('total'): // get actual value in session with ‘total' key.
    // ...
}
```

Pour afficher les données en session, on pourrait **envoyer** ici `$total`, que l'on vient de récupérer dans le controller, à la vue Twig. Mais Twig peut **accéder directement** aux données de session, sans passer par une récupération dans le contrôleur. C’est utile si tu n’as pas à modifier les informations en session, mais seulement à les afficher :

``` php
{{ app.session.get('total') }}
```

https://symfony.com/doc/current/templates.html
https://symfony.com/doc/current/session.html


## 12.2. Les messages flash

Les **messages flash** se basent sur les **sessions**. Chaque message est placé en attente (dans un tableau, le flashbag) jusqu’au moment où on demande de l’afficher. Ensuite, dès qu’il s’affiche, le message est “supprimé” du flashbag. Il ne s'affiche donc **qu’une et une seule fois**, d’où le nom de message flash.

On peut conditionner l'affichage des messages à un seul type de message. Dans ce cas, les messages qui n'ont pas été affichés sont conservés dans le flashbag (voir illustration ci-dessous).

![msg_flash](./img/55.png)

### 12.2.1. Utilisation des messages flash avec Symfony

On pourrait utiliser directement les sessions pour ajouter et supprimer tes messages flash de ton flashbag. Cependant, Symfony apporte différentes méthodes et helper twig pour te faciliter la vie. De ce fait, quand on utilise les messages flash, on ne fera pas directement appel à un objet `Session`, mais à des méthodes spécifiques qui, indirectement, utilisent `Session`.

**Ecrire un message Flash :**

Le **but** d’un message flash est généralement de **faire suite à une action** d’un utilisateur, le plus souvent la soumission d’un formulaire. Dans ce cas, le message doit **s’inscrire dans le contrôleur** une fois que tu t’es assuré que la soumission a été correctement effectuée, mais tout de même avant d’être redirigé vers une autre page :-)

Voici un exemple basique de l’ajout d’un article, pour illustrer où tu dois placer le message :

``` php
#[Route('/new', name: 'program_new', methods: ['GET', 'POST'])]
public function new(Request $request, ProgramRepository $programRepository): Response
{
   $program = new Program();
   $form = $this->createForm(ProgramType::class, $program);
   $form->handleRequest($request);

   if ($form->isSubmitted() && $form->isValid()) {
       $programRepository->save($program, true);

       // Once the form is submitted, valid and the data inserted in database, you can define the success flash message
       $this->addFlash('success', 'The new program has been created');

       return $this->redirectToRoute('program_index');
   }

   return $this->renderForm('program/new.html.twig', [
       'program' => $program,
       'form' => $form,
   ]);
}
```

On utilise donc la méthode `$this->addFlash()` qui prend **deux paramètres** :
- la catégorie du message
- le message lui-même.
  
La catégorie est libre, on peut mettre ce que l'on veut. Le but est de pouvoir regrouper ensemble les messages d’un même type, de décider lesquels afficher et de les styliser différemment en fonction. Par convention, un message de succès s’affiche généralement en vert, un message d’erreur en rouge, etc. Tout cela est libre, mais par simplification, il est commode d’utiliser des classes CSS (celles de Bootstrap si tu utilises ce framework CSS) comme noms de catégorie pour tes messages.

**Affichage d'un message Flash :**

Pour **afficher** les messages flash, il faut l’indiquer spécifiquement dans un fichier **Twig** : Twig peut accéder directement aux sessions, grâce à `app.flashes` (qui correspond au flashbag, le tableau contenant tous les messages flash)

``` php
{% for category, messages in app.flashes %}
    {% for message in messages %}
        <div class="alert alert-{{ category }}">
            {{ message }}
        </div>
    {% endfor %}
{% endfor %}
```

Dans la première boucle, tu récupères la clé “category” ("success", "warning"...) et les messages associés à cette catégorie, puis on effectue une seconde boucle qui va afficher dans un div tous les messages d’une catégorie donnée (tu pourrais ici ajouter une condition pour n’afficher que les messages d’une catégorie précise, si cela t’était nécessaire). On remarque que le div possède un attribut `class="alert alert-{{category}}"`. 

Toute l’astuce se trouve ici, car si on a bien utilisé les mêmes noms que ceux de Bootstrap (success, danger, info, warning…), on affiche pour chacun d’entre eux une alert stylisée de la bonne couleur, très simplement.

Ensuite, dès que les messages vont être affichés dans Twig, ils seront également supprimés du flashbag et ne s’afficheront plus.

**Attention** :
Si on souhaite afficher les messages flash sur une page mais que l'on oublie de configurer leur affichage dans le Twig, ceux-ci restent dans le flashbag et apparaîtront sur la prochaine page rencontrée qui, elle, affichera les messages flash. Le risque est donc d'afficher une notification qui n’a plus rien à voir avec la page sur laquelle tu te trouves. Pour éviter ce type de problème, il est très fortement conseillé d’afficher les messages flash sur toutes tes pages Twig. Pour ce faire simplement, il suffit d’appeler le code qui affiche les messages directement dans le fichier base.html.twig, dont tous tes autres fichiers Twig doivent normalement hériter. Problème résolu !

https://symfony.com/doc/current/controller.html#flash-messages
https://getbootstrap.com/docs/5.2/components/alerts/

[Return to Top](#notes-symfony)
# 13. **Les Services**


## 13.1. Qu'est ce qu'un service ?

Le **service** en lui-même est simplement l'instance d'une classe remplissant une fonction bien précise utile à ton code métier. Son intérêt est de rendre le code le plus **factorisé** possible, afin qu'il soit facilement réutilisable partout dans ton application.
(principe DRY).
Certains services sont **déjà présents** dans l'application **Symfony**. Tu peux retrouver la liste de ces services à l'aide de la commande suivante :

``` sh
php bin/console debug:container
```
https://putaindecode.io/articles/injection-de-dependances-en-php/
https://blog.eleven-labs.com/fr/injection-des-dependances/
https://symfony.com/doc/current/service_container.html

## 13.2. Pourquoi un service ?

Dès lors que :
- le code se répète
- un controleur est surchargé par sa logique métier
- l'on souhaite mettre en place des tests efficacement

Il est temps de **déplacer** le code ailleurs.

On appelle cela factoriser son code. C'est le **S** de **S.O.L.I.D**

On le déplace dans d'autres classes dans le dossier service dont la responsabilité sera de gérer ces problématiques (une responsabilité par classe).

Un **service** est donc une **simple classe**  gérant la logique métier qui n'a pas vocation à être dans le contrôleur ! 
- avec ses propriétés, constantes, méthodes
- utilisant toute la puissance de l'orienté objet (héritage, abstraction…)

Afin de rester bien organisé, on regroupe généralement ces classes dans le dossier `src/Service`.

Les services regroupent la logique métier, souvent critique pour l'application. Une bonne pratique est de créer un test unitaire pour chaque service.

Pour mettre en place les test :
- Installer PHPUnit
- Créer une structure identique dans le dossier tests/

![service](./img/56.png)

## 13.3. Créer un service : une histoire de réduction

### 13.3.1. Présentation

Un site de e-commerce propose 2 mécanismes de réductions
- **Une carte de fidélité** : Chaque client dispose d'un pourcentage de réduction applicable à tout moment dépendant de l'historique de ses achats
- **Un système de soldes** : Une réduction journalière est proposée à l'ensemble des clients

Les 2 mécanismes ne sont pas cumulables et seul le plus avantageux pour le client s'applique.

**En tant** qu'acheteur
**Je veux** appliquer la meilleure réduction
**Afin** d'obtenir le prix le plus bas

### 13.3.2. Première approche : tout dans le controller

Mise en place d'un **contrôleur** pour **afficher un produit** avec son **prix final** (prenant en compte la meilleure réduction) pour l'utilisateur connecté
Première approche : tout dans le `ProductController`


``` php
#[Route('/product/{id}', name: 'product', requirements: [id => '\d+'])]
public function show(Product $product, SpecialOfferRepository $specialOfferRepository): Response
{
   $currentUser = $this->getUser(); // Recover the connected user
   // Get the amount of today's discount offer
   $offer = $specialOfferRepository->findSpecialOfferForToday();
   if ($offer === null) {
       $todaysDiscount = 1;
   } else {
       $todaysDiscount = $offer->getDiscount();
   }
   // Get the amount of the personal loyalty discount for the connected user
   $currentUserDiscount = $currentUser->getLoyaltyDiscount();
   // The user's will have the best of the 2 non cumulative discounts
   $price = $product->getPrice() * min($currentUserDiscount, $todaysDiscount);
   return $this->render('product/show.html.twig', ['product' => $product, 'price' => $price]);
}
```

### 13.3.3. Réorganisation du code : création d'une classe dédie = le service

Notre contrôleur a maintenant **2 rôles**.
- **Gérer** la requête et produire la réponse
- **Calculer** le prix personnalisé d'un produit

Principe SOLID : une seule responsabilité par classe / méthode. **SOLID** n'est donc pas respecté !

**Solution** ? déporter le calcul de prix dans une classe dédiée (par ex `PriceCalculator`)

**On crée une classe dédiée :**
``` php
//Service/PriceCalculator.php
class PriceCalculator
{
  public function personalPrice(User $user, Product $product, ?SpecialOffer $specialOffer): float
  {
      $currentUserDiscount = $user->getLoyaltyDiscount();
      if ($specialOffer !== null) {
          $todaysDiscount = $specialOffer->getDiscount();
      } else {
          $todaysDiscount = 1;
      }
$price = $product->getPrice() * min($currentUserDiscount, $todaysDiscount);

      return $price;
  }
}
```
Cette simple classe dédiée **est un service**.

**On teste le service :**

Cumulons les bonnes pratiques et ajoutons des tests unitaires pour notre Service `PriceCalculator`

``` php
//tests/Service/PriceCalculatorTest.php
class PriceCalculatorTest extends TestCase
{
  public function testPersonalPrice(): void
  {
      $product = new Product();
      $user = new User();
      $offer = new SpecialOffer();
      $priceCalculator = new PriceCalculator();
      $product->setPrice(10);
      $user->setLoyaltyDiscount(1);
      $offer->setDiscount(1);
      $this->assertEquals(10, $priceCalculator->personalPrice($user, $product, $offer));
      $user->setLoyaltyDiscount(0.8);
      $this->assertEquals(8, $priceCalculator->personalPrice($user, $product, null));
      $this->assertEquals(8, $priceCalculator->personalPrice($user, $product, $offer));
      $offer->setDiscount(0.5);
      $this->assertEquals(5, $priceCalculator->personalPrice($user, $product, $offer));
  }
}
```

### 13.3.4. Retour au controller

Nous avons maintenant besoin du service dans le contrôleur. On crée un objet `PriceCalculator` dans le contrôleur !

``` php
public function show(Product $product, SpecialOfferRepository $specialOfferRepository): Response
{
   $currentUser = $this->getUser(); // Recover the connected user
   $todayOffer = $specialOfferRepository->findSpecialOfferForToday(); // Get the daily offer

   // Instance of our new service
   $priceCalculator = new PriceCalculator();
   $price = $priceCalculator->personalPrice($currentUser, $product, $todayOffer);

   return $this->render('product/show.html.twig', ['product' => $product, 'price' => $price]);
}
```
Maintenant le contrôleur dépend de notre service pour fonctionner : `PriceCalculator` est donc une **dépendance** de ProductController

![service](./img/57.png)

**Inconvénients** : mais si j'ai besoin du service ailleurs ? on devrait créer un **deuxième** objet => **inutile** un seul suffirait.

**Solution** ? Laissons Symfony **instancier le service** et nous envoyer l'**unique instance** partout ou nous en avons besoin (design pattern singleton) 

### 13.3.5. Injection de dépendance

Pour faire cela, le framework utilise un composant appelé le **Service Container**. Ce dernier est configuré pour savoir quelle classe il a le droit d'instancier et comment (paramètres éventuels du constructeur).

![service_container](./img/58.png)

Ce mécanisme s'appelle l'**injection de dépendance**. C'est une façon d'implémenter un **patron d'architecture logicielle** : l'inversion de contrôle. 

Ce patron est mis en place dans les *frameworks* et consiste à laisser au *framework* le contrôle de l'exécution globale.

Symfony met  en place un mécanisme d'**autowiring** : dans un **contrôleur**, pour accéder à un service gérer par le **service container**, il faut :
- Ajouter un paramètre au contrôleur
- Utiliser le **type-hinting** pour indiquer sa nature

Comment indiquer que mon service est géré par le **service container** ?  
C'est **automatique** : toutes les classes sont implicitement des services sauf quelques classes spécifiques (`src/Entity`, `src/Tests`, ...)

### 13.3.6. Utilisation du service dans un contrôleur

``` php
//ProductController.php
#[Route('/product/{id}', name: 'product', requirements: [id => '\d+'])]
public function show(
   Product $product,
   SpecialOfferRepository $specialOfferRepository,
   PriceCalculator $priceCalculator
): Response {
   $price = $priceCalculator->personalPrice(
       $this->getUser(),
       $product,
       $specialOfferRepository->findSpecialOfferForToday()
   );
   return $this->render('product/show.html.twig', [
       'product' => $product,
       'price' => $price,
   ]);
}
```

- Un paramètre de type `PriceCalculator` est demandé. Le service container est appelé automatiquement.
- L'`autowiring` permet de signifier au service container que l'on veut une instance de cette classe
- Le `service container` vérifie que cette classe est autorisée (c'est le cas par défaut)

Il renvoie une instance existante (ou en instancie une nouvelle). L'objet `$priceCalculator` est utilisable dans la méthode `show()`.

Pour lister les services disponibles pour l'autowiring et le type-hint :

``` sh
php bin/console debug:container --types
php bin/console debug:autowiring
```
Exemples de Services :
- Le gestionnaire d'entité Doctrine **EntityManager**
- Les **repository**
- **Mailer**, **HttpClient…**

### 13.3.7. Alléger le contrôleur

Notre contrôleur dépend maintenant du `PriceCalculator`, mais aussi du `SpecialOfferRepository` alors qu'en pratique il n'en a pas besoin.

On parle de couplage pour caractériser la quantité de dépendance des classes les unes envers les autres.
- Couplage fort : beaucoup d'interdépendance
- Couplage faible : peu d'interdépendance

Un couplage faible (Indépendance fonctionnelle) permet :
- plus de réutilisabilité
- des tests plus faciles

Objectif : éviter le code spaghetti.

Souvent, un service dépend lui-même d'autres services.

L'**autowiring** peut être utilisé au sein d'un **service** 
- Ajouter une **propriété** au service pour référencer sa dépendance
- Ajouter un paramètre au **constructeur** du service
- Utiliser le **type-hinting** pour indiquer sa nature
- **Récupérer** le service injecté dans la propriété

``` php
//Service/PriceCalculator.php
class PriceCalculator
{
   private SpecialOfferRepository $specialOfferRepository;

   public function __construct(SpecialOfferRepository $specialOfferRepository)
   {
       $this->specialOfferRepository = $specialOfferRepository;
   }

   public function personalPrice(User $user, Product $product): float
   {
       $currentUserDiscount = $user->getLoyaltyDiscount();
       $specialOffer = $this->specialOfferRepository->findSpecialOfferForToday();
       // [...]
   }
}
```
`SpecialOfferRepository` est demandé dans le `__construct`. Le *service container* est appelé et comprend qu'il doit retourner une instance de cette classe.

L'objet `$specialOfferRepository` est affecté à la propriété du même nom et peut donc être utilisée dans les méthodes du service.

Et pour le contrôleur :

``` php
//ProductController.php
#[Route('/product/{id}', name: 'product', requirements: [id => '\d+'])]
public function show(Product $product, PriceCalculator $priceCalculator): Response
{
   $price = $priceCalculator->personalPrice($this->getUser(), $product);
   return $this->render('product/index.html.twig', [
       'product' => $product,
       'price' => $price,
   ]);
}
```
Le couplage avec `SpecialOfferRepository` est retiré


![resume_service](./img/59.png)


### 13.3.8. Principe d'inversion des dépendances

Principe d'inversion des dépendances (SOLI**D**) :
- Dépendre des abstractions (interface) et non des implémentations

Le **Service Container** de Symfony utilise ce principe => `Type-hint` avec l'**interface** plutôt qu'avec la (une des) classe(s) qui implémente cette interface 

Exemple :
``` php
//ProductController.php
#[Route('/product/add', name: 'add_product')]
public function add(EntityManagerInterface $manager): Response
{
    // Creating a new product
    $product = new Product();
    // Initialiazing the product, for example using a form
    // ...
    // Save the product
    $manager->persist($product);
    $manager->flush();
    // Generate a response, for example a redirection
}
```
Pour récupérer un objet de type `$entityManager`, la configuration du service container impose de typer par l'interface `EntityManagerInterface` et non directement par `EntityManager`.
(Rappel: Depuis **Symfony 6** on privilégie l’utilisation d’un **repository** pour persister des objets)


## 13.4. Service Container et paramétrage

Symfony déclare **automatiquement** les services.

Pour passer des paramètres spécifiques à un service, il suffit de déclarer manuellement le service dans `services.yaml` (overriding).

On n’est pas obligé de re-déclarer tous les paramètres du service. Il est possible de se limiter à l’argument spécifique. Les autres resteront gérés grâce à **l’autowiring**.

Il est possible de passer en paramètres : 
- Des valeurs (booléens, strings, nombres, etc.),
- Des paramètres d’application, encadrés de signes « % »,
- Des services, précédés d'une arobase.

``` yaml
#Service.yaml
parameters:
   locale: 'fr'
   vat: 20

services:
   # default configuration for services in *this* file
   # ...
   App\Service\PriceCalculator:
       arguments :
           $shippingFee : '@App\Service\ShippingFeeCalculator'
           $currency: '€'
           $vat: '%vat%'
```

``` php
//PriceCalculator
class PriceCalculator()
{
    public function __construct(
        $shippingFee,
        float $vat, 
        string $currency
    )
    {
        $this->vat = $vat;
        $this->currency = $currency;
    }
}
```

## 13.5. Exemple : Utilisation du service Slug

Pour accéder à la fiche d'une série, on passe par l'URL`/program/{id}`. Cela fonctionne très bien, mais on peut rendre cette URL plus jolie en incluant le **titre de la série** en question dans l'URL plutôt que son identifiant.

**Pourquoi** faire cela si ça fonctionne en l'état ? Eh bien, pour une question d'**esthétique** et de **référencement** surtout. Du point de vue des moteurs de recherche, l'URL `/program/walking-dead` aura plus d'importance que `/program/1` par exemple. Pour ce faire, il va te falloir générer ce que l'on appelle un **slug**.

``` sh
php bin/console debug:autowiring slug
```

Cette commande recherche parmi les services symfony qui contiennent le mot clé *slug*. Voici le retour :

``` sh
Autowirable Types
=================

 The following classes & interfaces can be used as type-hints when autowiring:
 (only showing classes/interfaces matching slug)
 
 Creates a URL-friendly slug from a given string.
 Symfony\Component\String\Slugger\SluggerInterface (slugger)
```

On apprend ici qu'un objet du type `SluggerInterface` peut être **injecté en dépendance** dans une application partout où tu en as besoin :

``` php
// src/Controller/ProgramController.php
public function new(..., SluggerInterface $slugger)
```

Grâce aux **injections de dépendances**, on n'a pas besoin d'instancier toi-même l'objet dans le corps de ta méthode.

https://symfony.com/doc/current/components/string.html#slugger

La documentation de ce service nous indique qu'une méthode `slug()` est disponible et accepte en paramètre la chaîne de caractère à sluggifier. On lui passe donc en argument le titre de la série avant la persistence de ton nouvel objet `Program` :

``` php
$slug = $slugger->slug($program->getTitle());
$program->setSlug($slug);
```

**BILAN :**

Deux mots clés sont à retenir :
- le `TypeHinting` : préciser dans les paramètres de la méthode que `$slugger` doit être un objet de la classe `SluggerInterface`,
- l'`Autowiring` (câblage automatique) : **instanciation automatique** de la part du framework de cet objet `SluggerInterface`.

https://symfony.com/doc/current/service_container/autowiring.html

Ainsi, le service sera sollicité à chaque ajout d'une nouvelle série.

**Attention :**
On appelle une méthode `setSlug()` sur un objet qui ne dispose pas de cette fonctionnalité, ni de la propriété `slug`. On va devoir ajouter cet attribut à ton entité `Program` :

``` sh
symfony console make:entity
```
afin de rajouter la propriété `slug`, qui doit contenir un string ne pouvant pas être null.

``` sh
symfony console make:migration
//suivi de 
symfony console doctrine:migration:migrate
```
pour **créer** la classe migration et pour **impacter** la DB avec ce nouveau champ.


## 13.6. Appeler un service en dehors d'un contrôleur

Il arrive fréquemment que l'on ait besoin d'**utiliser un service** depuis une **autre classe** (autre service, fixtures, etc.)

La syntaxe est un peu différente car on devra utiliser le mécanisme d'**injection de dépendance** dans le `__construct()` (et non directement dans les méthodes comme pour les contrôleurs).

Dans tes **fixtures** par exemple, on va vouloir ajouter le slug et donc générer automatiquement ce dernier en fonction du title de la série. On peut s'inspirer de la documentation suivante et adapter notre code pour y appeler ce service SluggerInterface.

https://symfony.com/bundles/DoctrineFixturesBundle/current/index.html#accessing-services-from-the-fixtures


``` php
private SluggerInterface $slugger;

public function __construct(SluggerInterface $slugger)
{
    $this->slugger = $slugger;
}
// dans méthode load :
$program->setSlug($this->slugger->slug($program->getTitle()));
```

## 13.7. Autre exemple : créer un service pour calculer une durée

Imaginons que l'on crée un service pour calculer la durée d'une program entier qui serait afficher sur la fiche de chaque série.

- On commence donc par créer une propriété `duration` sur l'entité `Episode`, qui sera du type **integer**.
- On modifie les **fixtures** en ajoutant des valeurs pour cette nouvelle propriété.
- On crée le service dans le répertoire `src/Service`. On nomme le fichier `ProgramDuration.php`. On crée la classe avec le bon **namespace**.
- On déclare la méthode qui va permettre de calculer la durée totale d'une série `calculate(Program $program): string`


``` php
namespace App\Service;

use App\Entity\Program;

class ProgramDuration
{
    public function calculate(Program $program): string
    {
        $length = 0;
        foreach ($program->getSeasons() as $season) {
            foreach ($season->getEpisodes() as $episode) {
                $length += $episode->getDuration();
            }
        }
        return strval($length);
    }
}
```

On va pouvoir maintenant appeler le service dans notre contrôleur :

``` php
// src/Controller/ProgramController.php
public function show(Program $program, ..., ProgramDuration $programDuration)
{
    return $this->render('program/show.html.twig', [
        ...,
        'programDuration' => $programDuration->calculate($program)
    ]);
}
```
Il ne faut pas oublier le `use` !

On peut également configurer et envoyer des paramètres à un service :
https://symfony.com/doc/current/service_container.html


## 13.8. Autre exemple : utiliser httpClient pour une requête API

Contexte : afficher un prix en divers devises.

Le controleur :

``` php
#[Route('/product/{id}', name: 'app_product_details')]
public function show(Product $product, MoneyConverter $converter): Response
{
    $dollarPrice = $converter->convertEurToDollar($product->getPrice());
    $yenPrice = $converter->convertEurToYen($product->getPrice());

    return $this->render('product/details.html.twig', [
        'product' => $product,
        'dollar_price' => $dollarPrice,
        'yen_price' => $yenPrice,
    ]);
}
```

On crée donc un service `MoneyConverter` :
``` php
namespace App\Service;

use Symfony\Contracts\HttpClient\HttpClientInterface;

class MoneyConverter
{
    public function __construct(private readonly HttpClientInterface $client){}

    public function convertEurToDollar(float $euroPrice): ?string
    {
        return $this->makeRequest($euroPrice, 'USD');
    }

    public function convertEurToYen(float $euroPrice): ?string
    {
        return $this->makeRequest($euroPrice, 'JPY');
    }

    public function makeRequest(float $euroPrice, string $moneyCode): ?string
    {
        $url = 'https://v6.exchangerate-api.com/v6/e54138c2f8df9a2e71e48ff0/pair/EUR/'. $moneyCode .'/' . $euroPrice;

        $response = $this->client->request('GET', $url);

        $statusCode = $response->getStatusCode(); // $statusCode = 200
        $contentType = $response->getHeaders()['content-type'][0]; // $contentType = 'application/json'

        if ($statusCode === 200 && $contentType === 'application/json') {
            $content = $response->getContent(); // get the response in JSON format
            $content = $response->toArray(); // convert the response (here in JSON) to an PHP array

            return number_format($content['conversion_result'], 2, ","," ");
        }
        return null;
    }
}
```

`HttpClientInterface` est injecté dans le `__construct` et affecté à `$client` pour s'en resservir ensuite dans la classe.

Ici la clé API est codée en dur dans le service. Il serait intéressant de la mettre ailleurs :

``` yaml
#services.yaml
parameters:
    exchangerate_key: 'e54138c2f8df9a2e71e48ff0'
```
Le service devient :

``` php
//Le constructeur
public function __construct(
    private readonly HttpClientInterface $client,
    private readonly ParameterBagInterface $parameterBag
) {
}

//La méthode
$url = 'https://v6.exchangerate-api.com/v6/' .
    $this->parameterBag->get('exchangerate_key') .
    '/pair/EUR/' . $moneyCode . '/' . $euroPrice;
```
Cependant si on met la clé dans le fichier `service.yaml`, elle est versionnée. Si on veut la rendre en privée, il faut la mettre dans le fichier `.env.local`

``` .env.local
EXCHANGERATE_KEY=e54138c2f8df9a2e71e48ff0
```

``` yaml
#services.yaml
parameters:
    exchangerate_key: '%env(EXCHANGERATE_KEY)%'
```

Autre méthode :

``` yaml
services:
    #...
    App\Service\MoneyConverter:
        arguments:
            $exchangeKey: '%env(EXCHANGERATE_KEY)%'
```
Le service

``` php
//constructeur
public function __construct(
    private readonly HttpClientInterface   $client,
    private string $exchangeKey
) {
}
//La méthode
$url = 'https://v6.exchangerate-api.com/v6/' .
    $this->exchangeKey .
    '/pair/EUR/' . $moneyCode . '/' . $euroPrice;
```


On ne peut procéder à l'injection de dépendance directement dans une méthode uniquement dans le controller. Partout ailleurs pour injecter un service, il faut passer par le construct de la class en question.

Si pas injection de dépendance, pas besoin de faire un service, plutôt créer une méthode à l'intérieur de l'entité.
Ici Handler ou helper si pas d'injection de dépendance à faire
c'est quoi un helper ?
pourquoi dans les entités pas d'injection de dépendance possible ? : blocage symfony.

[Return to Top](#notes-symfony)
# 14. **Envoi d'email**

Pour commencer, installe le composant Mailer recommandé par Symfony, (ce dernier n'est pas installé par défaut), via la commande :

``` sh
composer require symfony/mailer
```

## 14.1. Configurer l'envoie des mails

Il faut tout d'abord permettre à ton application de communiquer avec le serveur qui fera transiter tes mails : le **serveur SMTP**.

Pour commencer, il te faut choisir l'**adresse mail** (et donc le **serveur SMTP**) qui va envoyer les messages. Utiliser une adresse **personnelle** type Gmail est **fortement déconseillé** (car peu adapté à l'envoi d'un grand nombre d'email, risque de passer pour un spammeur). Il faut plutôt se tourner vers des **fournisseurs spécialisés** qui fournissent généralement des offres gratuites pour de faibles volumes d'envois.

>**À propos de Gmail**
De base, les adresses Gmail n’autorisent pas l'envoi des courriels en dehors de l’interface web de gmail.com. Il faut donc manuellement configurer les options de son compte Google et cocher le paramètre "Autoriser les applications moins sécurisées", puis générer un mot de passe spécifique à l'application, bref évite de l'utiliser..

### 14.1.1. Choix du service

Pour la **phase de développement**, il est recommandé d'utiliser un **fake mailer** tel que `mailtrap`. Cet outil va agir comme un **smtp** mais au lieu de distribuer réellement les mails aux destinataires, il va les garder et les déposer dans une boîte de réception à laquelle tu auras accès !

Avantages :
- configuration est très simple pour Symfony
- outils d’analyse des mails envoyés 
- pas possible d'envoyer par erreur (en phase de développement) des mails à des personnes réelles !

>Pour la phase de production, voici quelques fournisseurs intéressants (liste non exhaustive) : MailChimp, Mailgun, Mailjet, SendGrid, Sendinblue. Ils possèdent généralement des offres gratuites pour les petits projets, et sont adaptés pour envoyer et suivre des campagnes de mailing massifs. Symfony possède des configurations pour ces différents services :
https://symfony.com/doc/current/mailer.html#using-a-3rd-party-transport


On se connecte à `mailtrap.io` et on crée un compte. On arrive sur une boîte de réception avec un premier projet. On clique sur la roulette “Settings” puis dans le menu déroulant **“Integrations”**, sélectionne `Symfony`.

**Mailtrap** fourni la ligne à copier directement dans ton fichier `.env.local.`qui
ressemble à MAILER_DSN=smtp://caaed6cc1d54d:86287f9d6ra7bb@smtp.mailtrap.io:2525?encryption=tls&auth_mode=login

Un autre fakemailer :
https://www.mailslurper.com/

### 14.1.2. Configurer le serveur SMTP dans Symfony

Dans le fichier `/.env.local` il y a les paramètres relatifs à la configuration de la base de données notamment. Il y a aussi des lignes (commentées) pour `symfony/mailer` qu'il faut modifier avec la ligne indiquée dans Mailtrap.

``` sh
###> symfony/mailer ###
MAILER_DSN=smtp://caaed6cc1d54d:86287f9d6ra7bb@smtp.mailtrap.io:2525?encryption=tls&auth_mode=login
###< symfony/mailer ###
```
La ligne est de la forme :
MAILER_DSN=smtp://user:pass@smtp.example.com

Cette manipulation est lié à l'envoi de mail en général depuis ton application Symfony, ce n'est pas directement lié au composant Mailer. Si on souhaite utiliser un autre service, comme `PHPMailer` par exemple, on pourras se baser sur ce fichier .env.local pour le configurer à son tour.

La configuration propre à **Mailer**, comme la majeure partie des autres librairies, se trouve dans `config/packages/mailer.yaml`.
On retrouve juste une référence à la variable configurée dans le fichier précédent `dsn: '%env(MAILER_DSN)%'`, c'est normal. En effet, `mailer.yaml` s'appuie sur les données renseignées dans `env.local`. 

Comme pour les identifiants de base de données, les identifiants de serveur de messagerie sont des données sensibles, qui ne doivent pas être partagées et donc versionnées. De plus, cela te permet de configurer différemment ton environnement de développement et de production, en leur attribuant des identifiants différents.

Une fois ton `MAILER_DSN` Mailtrap ajouté dans le fichier `.env.local`, il te reste une **dernière étape** de configuration. Par **défaut**, Symfony envoi les emails de manière **asynchrone**. Les messages sont mis dans une file d'attente, et il faut que tu gères toi même le moment où tu souhaites les envoyer. C'est très pratique quand tu as de gros flux de messages, mais nous allons partir sur un système plus simple, en **synchrone**. Dans le fichier config/packages/mailer.yaml et dans la partie "mailer", on ajoute message_bus: false. Ton fichier dois ressembler à ça maintenant :

``` yaml
framework:
    mailer:
        dsn: '%env(MAILER_DSN)%'
        message_bus: false
```

## 14.2. Appeler Mailer depuis le contrôleur

Si on souhaite envoyer un mail après l'ajout d'une nouvelle série, il faut lancer l'envoie du mail après l'enregistrement de la série en BDD :

``` php
public function new(Request $request, MailerInterface $mailer, ProgramRepository $programRepository): Response
{
    // [...]
    if ($form->isSubmitted() && $form->isValid()) {
        // [...]
        $programRepository->save($program, true); 

        $email = (new Email())
                ->from('your_email@example.com')
                ->to('your_email@example.com')
                ->subject('Une nouvelle série vient d\'être publiée !')
                ->html('<p>Une nouvelle série vient d\'être publiée sur Wild Séries !</p>');

        $mailer->send($email);
        // [...]
    }
}
```
**Explications :**
- On passe en paramètre de la méthode un `MailerInterface $mailer` et via l'**injection de dépendances** pour récupérer un objet `$mailer` utilisable.
- Tu crées un email via l'**instanciation** d'un object `Email`
- Cet objet `Email` possède des méthodes pour configurer le message, comme `from()` pour l'adresse de l'expéditeur, `to()` pour l'adresse du destinataire, `subject()` pour le sujet du mail, `html()` pour le corps du mail au format HTML, etc... 
https://symfony.com/doc/current/mailer.html#creating-sending-messages

>Les adresses email renseignées ici dans from() et to() sont fictives et saisies "en dur". Ce n'est pas une bonne pratique de saisir des adresses emails "en dur", car cela les rend difficilement modifiables. Ces adresses pourraient soit provenir d'un enregistrement en base de données, soit d'un paramètre défini dans tes variables d’environnement. Voyons comment améliorer cela.

Dans le fichier `.env.local` on rajoute :
`MAILER_FROM_ADDRESS=wilder@wildcodeschool.fr`
Dans le fichier `services.yaml`, sous la clé `parameters`, récupérer ta variable d’environnement ainsi :
``` yaml
parameters:
    mailer_from: '%env(resolve:MAILER_FROM_ADDRESS)%'
```
Puis dans le contrôleur :
``` php
$this->getParameter('mailer_from');
```

Lors de la création d'une nouvelle série, un email est normalement expédié vers ton utilisateur destinataire.  
**Attention**, avec Mailtrap, l'email n'est pas réellement envoyé à l'adresse configurée dans le `to()`, mais sera disponible sur ton interface **mailtrap** ! Si on ne reçois rien, c'est peut-être qu'il y a un problème de configuration ou que l'adresse du destinataire n'est pas bonne.


## 14.3. Mise en forme des emails

Le contenu du mail est une simple chaîne de caractères au format HTML. Dans l'exemple précédent, le HTML était directement saisi dans la méthode `html()`. **Ce n'est pas une bonne pratique** car cela va à l'encontre du **MVC** qui veut que la **Vue** soit **indépendante** du **Contrôleur**. 

Pour résoudre ce problème, on va utiliser `Twig`. Dans les contrôleurs on a utilisé `$this->render('file.thml.twig')` dans tes contrôleurs. Cette méthode renvoie un objet **Response** dans lequel tu trouveras le rendu du fichier `Twig`. Mais tes contrôleurs ont également accès à une méthode `$this->renderView('file.thml.twig')` qui permet de ne faire que le rendu du template `Twig` (et donc de **renvoyer** l'HTML sous forme d'**une chaîne de caractères**).


Dans un premier temps, créé un fichier Twig `layoutEmail.html.twig` qui sera un template d'une page HTML pour générer le mail.

On pourra ensuite créer un fichier Twig `Program/newProgramEmail.html.twig` qui étendra de ce layout commun pour les divers envois de mail. Ce qui donne dans le contrôlleur :

``` php
$email = (new Email())
    ->from($this->getParameter('mailer_from'))
    ->to('your_email@example.com')
    ->subject('Une nouvelle série vient d\'être publiée !')
    ->html($this->renderView('Program/newProgramEmail.html.twig', ['program' => $program]));
```

Il est possible de faire du templating avancé de mail avec divers outils :

https://get.foundation/emails/docs/inky.html  
https://symfony.com/doc/current/mailer.html#inky-email-templating-language  
https://symfony.com/doc/current/mailer.html#twig-html-css



[Return to Top](#notes-symfony)
# 15. **Upload de médias avec Vich Upload**


## 15.1. Installer et configurer le bundle VichUploader dans un projet Symfony

Le bundle le plus utilisé pour uploader des fichiers se nomme `VichUploaderBundle`.

``` sh
composer require vich/uploader-bundle
```
Un fichier a été créé ici `config/packages/vich_uploader.yaml` :

``` yaml
# config/packages/vich_uploader.yaml
vich_uploader:
    db_driver: orm

    metadata:
        type: attribute

    mappings:
        poster_file:
            # alias qui nous permet d'accéder à nos images depuis le navigateur
            uri_prefix: /uploads/images/posters
            upload_destination: '%kernel.project_dir%/public/uploads/images/posters/'
            namer: Vich\UploaderBundle\Naming\SmartUniqueNamer
```

Une bonne pratique est de stocker ces fichiers dans le dossier `public/` de notre application. C'est le seul dossier qui est exposé sur ton serveur. On crée ensuite un sous-dossier `uploads/` dans ton dossier `public/` qui contiendra les fichiers chargés.


`poster_file` :
- détermine simplement le nom de notre **mapping**. Il sera utile plus tard lors de la configuration des entités.


`upload_destination` :
- Pour simplifier la configuration, ajoute un paramètre `upload_directory` dans ton fichier `config/services.yaml`. En spécifiant `upload_directory` entre %, **symfony** va récupérer la valeur du paramètre du même nom défini plus haut.

``` yaml
# config/services.yaml
parameters:
    upload_directory: '%kernel.project_dir%/public/uploads/images/posters/'
```
- Il fait référence au dossier `/images/posters` dans public et te sera utile pour la configuration de Vich.

`uri_prefix`:
- va permettre d'accèder aux fichiers depuis le navigateur.

`namer` :
- spécifie la stratégie qu'utilise Vich pour renommer les fichiers uploadés (on ne peux pas conserver le nom d'origine du fichier au risque d'avoir des collisions de nom). La stratégie **SmartUniqueNamer** est un **mélange** entre le **nom d'origine** et une v**aleur aléatoire**, mais on peut utiliser d'autres stratégies de nommage.
https://github.com/dustin10/VichUploaderBundle/blob/master/docs/namers.md

`metadata` :
- Pour spécifier que la configuration se fera via les attributs PHP.

**Attention** : le répertoire va contenir des images des utilisateurs. Celles-ci ne doivent **pas** être versionnées (au risque de se retrouver publiquement sur GitHub). Pense à mettre à jour ton .gitignore en conséquences.


## 15.2. Permettre à un utilisateur d’uploader un fichier sur un serveur depuis une application.


**Modification de l'entité :**

``` php
namespace App\Entity;

use ...;

#[ORM\Entity(repositoryClass: ProgramRepository::class)]
#[Vich\Uploadable] 
class Program
{
    //...
    #[ORM\Column(type:'string', length: 255, nullable: true)]
    private ?string $poster = null;
    // ici on crée un nouvel attribut à notre entité, qui ne sera pas lié à une colonne
    // l’attribut ORM column n’est pas spécifiée, car on ne rajoute pas de données de type file en bdd
    #[Vich\UploadableField(mapping: 'poster_file', fileNameProperty: 'poster')]
    #[Assert\File(
        maxSize: '1024k',
        mimeTypes: ['image/*'],
        mimeTypesMessage: 'Please upload a valid image',
    )]
    private ?File $posterFile = null;
}
```

La propriété `$poster` était déjà présente. Elle stocke le nom du fichier (en chaîne : string).
La propriété `$posterFile` stocke le contenu du fichier.Dans ce cas, la donnée obtenue dans la variable $posterFile ne sera jamais stockée en base de données. L'idée est de récupérer **uniquement** le nom du fichier uploadé (cf upload php) et le transmettre à l’attribut `$poster`.

On peut constater que `$posterFile` a un attribut de type `Vich`, avec le **mapping** correspondant au fichier `config/packages/vich_uploader.yaml`, et un **fileNameProperty** qui réfère à ta propriété `$poster`.

Ensuite on ajoute les **getters** et **setters** de cette propriété :

``` php
public function getPosterFile(): ?File
{
    return $this->posterFile;
}

public function setPosterFile(File $image = null): Program
{
    $this->posterFile = $image;
    if ($image) {
        $this->updatedAt = new \DateTime('now');
    }
    return $this;
}
```
**Modification du formulaire :**

``` php
    $builder
        ->add('title')
        // ...
        ->add('posterFile', VichFileType::class, [
                    'required'      => false,
                    'allow_delete'  => true, // not mandatory, default is true
                    'download_uri' => true, // not mandatory, default is true
        ])
    ;
```
**Attention** : Ne pas oublier de préciser l'**import** de **namespace** en haut de ta classe, via : `use Vich\UploaderBundle\Form\Type\VichFileType`

Si on essait maintenant d'accéder au formulaire via le navigateur, on constate que :
- Visuellement, qu'un champ a été ajouté (avec un bouton "parcourir" pour sélectionner le fichier) ;
- Dans le code source on peut voir un `input type="file"` ainsi d'un attribut `enctype="multipart/form-data"` dans la balise form. Ce qui est indispensable pour uploader des fichiers.


**Attention :**

La propriété `$posterType` n’est **volontairement** pas liée à une colonne de ta table, et n’est donc pas liée à **Doctrine**. Par conséquent si on essai de **modifier** ton programme juste en changeant l’image, on sera confronté au problème de **non persistance des objets**. Lorsqu'on modifie un attribut **non lié à Doctrine**, ce dernier ne voit **aucune nouvelle** donnée apportée à son schéma (dans le `persist()`) et **ne modifie donc pas** tes changements en base de données.

C'est pour cela que l'on ajoute un attribut à ton entité `Program` :

``` php
#[ORM\Column(type: Types::DATETIME_MUTABLE, nullable: true)]
private ?DatetimeInterface $updatedAt = null;
```

Le but de la manoeuvre est de **modifier** au même moment que l’on change ou charge une image, la **date** de modification qui, elle, sera **persistée** en **base de données** et qui, par conséquent, **sauvegardera tous tes changements**.

On génère les **getters** et **setters** de ta propriété `$updatedAt` pour l'utiliser dans le **setter** de ton `$posterFile` le code suivant.


**Validation des fichiers** 

Si on souhaite contraindre l'utilisateur à certains **types** de fichiers, ou à un **poids** maximal (rappel : la configuration de base de PHP n'autorise pas d'uploads de fichiers de plus de 2M). 
Pour faire ces vérifications, tu vas utiliser les attributs `#[Assert]` :

``` php
#[Vich\UploadableField(mapping: 'poster_file', fileNameProperty: 'poster')]
#[Assert\File(
    maxSize: '1M',
    mimeTypes: ['image/jpeg', 'image/png', 'image/webp'],
)]
private ?File $posterFile = null;
```

https://symfony.com/doc/current/reference/constraints/File.html

**Affichage des images** 

On utilise Twig. On pourrait retrouver le chemin vers l'image et l'appeler mais Vich apporte une fonction dédiée pour simplifier les choses :

``` twig
<img src="{{ vich_uploader_asset(program) }}" alt="{{ program.title }}">
```

On passe l'objet `program` en paramètre de `vich_uploader_asset`. `Vich` retrouve le mapping configuré dans `Program` et peut donc en déduire le chemin vers le répertoire où est stockée la ressource. 

Des options avancées existent pour le cas où l'entité aurait plusieurs mapping (ce n'est pas le cas ici). La doc :
https://github.com/dustin10/VichUploaderBundle/blob/master/docs/generating_urls.md


[Return to Top](#notes-symfony)
# 16. **Gestion des utilisateurs**


## 16.1. Creation des USERS

On peut avoir besoin d'implémenter la notion d'utilisateur, "User" en anglais, pour plusieurs raisons :
- D'une part, toutes les parties d'un site ne doivent pas être accessibles à tout le monde. 
- D'autre part, on va devoir définir "qui a écrit quoi" et le sauvegarder en base de données : notion d'auteur.

La gestion des utilisateurs se fait par le composant `SecurityBundle`, il est déjà installé si on a crée le projet avec l'option `--webapp`. 

https://symfony.com/doc/current/security.html#security-installation

La manière la plus simple de générer des Users est :

``` psh
symfony console make:user
```

Lors de la création de l'entité, on génère une simple entité `User`, qui permettra de stocker les informations des utilisateurs avec au **minimum** leur **identifiant** et leur **mot de passe**. Si tu as besoin d'autres informations sur les `Users` (nom, date de naissance, pays, etc.) on peut simplement éditer la classe (make:entity) et y ajouter les propriétés voulues.

## 16.2. Un peu de sécurité

Pour se connecter, ton User a généralement besoin d'un identifiant (par exemple un email ou nom d'utilisateur) et d'un mot de passe. Il existe d'autres stratégies d'identification (double authentification, biométrie, etc.) plus complexes à mettre en place et non traitées ici.

Un mot de passe en base de données ne doit **JAMAIS** être stocké "en clair". Celui-ci doit systématiquement être encodé. Il existe de nombreuses **fonctions de hachage**, plus ou moins **performantes** et **sécurisées**, de nouvelles sont régulièrement créées, apportant toujours plus de sécurité et de performance.

Lors de la **tentative de connexion** au site, le mot de passe saisi par l'utilisateur est **haché** par la fonction, et la chaîne ainsi obtenue est **comparée** à celle qui se trouve en **base de données**.

A aucun moment en tant que développeur, on n'aura accès au mot de passe "**en clair**" de l'utilisateur. Si c'est le cas, c'est une **grave faille de sécurité**.

La sécurisation de l'authentification est un sujet complexe et critique. Heureusement, Symfony le gère ! Le **framework** est même **réglé** par défaut pour utiliser la **fonction de hachage la plus à jour**. C'est le but du `auto` dans la partie `password_hashers` du fichier `security.yaml` Registering the User: Hashing Passwords. À l'heure actuelle, en fonction de la version de PHP utilisée, ce sont les fonctions bcrypt ou argon2 qui sont utilisées par Symfony.

Dans le fichier `securité.yaml` :

``` yaml
# config/packages/security.yaml
security:
    # ...
    password_hashers:
        # Use native password hasher, which auto-selects and migrates the best
        # possible hashing algorithm (which currently is "bcrypt")
        Symfony\Component\Security\Core\User\PasswordAuthenticatedUserInterface: 'auto'

    providers:
        app_user_provider:
            entity:
                class: App\Entity\User
                property: email
```

https://symfony.com/doc/current/security.html#registering-the-user-hashing-passwords
https://symfony.com/doc/current/security/passwords.html

## 16.3. Configurer le firewall

Firewall : 
- permet de configurer un ensemble d'urls potentiellement sécurisées de la même manière
- Le plus souvent, un seul firewall est suffisant pour gérer l’accès à toutes les URLs

À chaque requête : vérification si l'utilisateur est déjà identifié (identifiant en **session**) et récupération de ses infos (via le provider, ici base de données).


``` yaml
# config/packages/security.yaml
security:
    # ...
    firewalls:
        main:
            lazy: true
            provider: app_user_provider
```
Si utilisateur non identifié, redirection vers un mécanisme d'authentification, généralement un formulaire de login mais il existe différentes manières de s’authentifier (JSON API, HTTP Basic header, social auth via Google, Facebook, Github, oAuth, etc.)


## 16.4. Création de users à l'aide des fixtures

On dispose désormais d'une entité `User` et de son `UserRepository` associé, et que la base de données est mise à jour avec ces changements :
``` sh
symfony console make:migration
symfone console d:m:m
```
On va créer quelques utilisateurs dans ta table `User`. Pour cela, tu vas utiliser des **fixtures**. On crée un fichier `UserFixtures` via la commande `make:fixtures`. Ici deux faux utilisateurs (un contributeur et un admin) quiauront un mot de passe. Ce mot de   est haché comme tout mot de passe, c'est le rôle du service `$passwordHasher` injecté dans le `__construct` en utilisant bien le type `UserPasswordHasherInterface` :

``` php
namespace App\DataFixtures;

use App\Entity\User;
use Doctrine\Bundle\FixturesBundle\Fixture;
use Doctrine\Persistence\ObjectManager;
use Faker\Factory;
use Symfony\Component\PasswordHasher\Hasher\UserPasswordHasherInterface;

class UserFixtures extends Fixture
{
    public function __construct(private readonly UserPasswordHasherInterface $passwordHasher)
    {
    }

    public function load(ObjectManager $manager): void
    {
        $faker = Factory::create('fr_FR');

        public function load(ObjectManager $manager): void
    {
        // Création d’un utilisateur de type “contributeur” (= auteur)
        $contributor = new User();
        $contributor->setEmail('contributor@monsite.com');
        $contributor->setRoles(['ROLE_CONTRIBUTOR']);
        $hashedPassword = $this->passwordHasher->hashPassword(
            $contributor,
            'contributorpassword'
        );

        $contributor->setPassword($hashedPassword);
        $manager->persist($contributor);

        // Création d’un utilisateur de type “administrateur”
        $admin = new User();
        $admin->setEmail('admin@monsite.com');
        $admin->setRoles(['ROLE_ADMIN']);
        $hashedPassword = $this->passwordHasher->hashPassword(
            $admin,
            'adminpassword'
        );
        $admin->setPassword($hashedPassword);
        $manager->persist($admin);

        // Sauvegarde des 2 nouveaux utilisateurs :
        $manager->flush();
    }
}
```
Puis on lance les fixtures :
``` php
symfony console d:f:l
```

## 16.5. Gestion du Login

On a besoin d'une interface de connexion, sous forme d'un formulaire d'authentification avec un login et un mot de passe.

https://symfony.com/doc/current/security.html#form-login


``` sh
symfony console make:controller Login
```

Cela va créer deux fichiers :
- `src/Controller/LoginController.php`
- `templates/login/index.html.twig`

On modifie le controller pour obtenir :
``` php
// src/Controller/LoginController.php
namespace App\Controller;

use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\HttpFoundation\Response;
use Symfony\Component\Routing\Annotation\Route;
use Symfony\Component\Security\Http\Authentication\AuthenticationUtils;

class LoginController extends AbstractController
{
    #[Route('/login', name: 'app_login')]
    public function index(AuthenticationUtils $authenticationUtils): Response
    {
        // get the login error if there is one
        $error = $authenticationUtils->getLastAuthenticationError();

        // last username entered by the user
        $lastUsername = $authenticationUtils->getLastUsername();
        return $this->render('login/index.html.twig', [
            'controller_name' => 'LoginController',
            'last_username' => $lastUsername,
            'error'         => $error,
        ]);
    }
}
```
Il faut également modifier le fichier `security.yaml`
``` yaml
# config/packages/security.yaml
security:
    # ...

    firewalls:
        main:
            # ...
            form_login:
                # "app_login" is the name of the route created previously
                login_path: app_login
                check_path: app_login
```
Et modifie
``` twig
{# templates/login/index.html.twig #}
{% extends 'base.html.twig' %}

{# ... #}

{% block body %}
    {% if error %}
        <div>{{ error.messageKey|trans(error.messageData, 'security') }}</div>
    {% endif %}

    <form action="{{ path('app_login') }}" method="post">
        <label for="username">Email:</label>
        <input type="text" id="username" name="_username" value="{{ last_username }}">

        <label for="password">Password:</label>
        <input type="password" id="password" name="_password">

        {# If you want to control the URL the user is redirected to on success
        <input type="hidden" name="_target_path" value="/account"> #}

        <button type="submit">login</button>
    </form>
{% endblock %}
```

**Protection CSRF**

``` yaml
# config/packages/security.yaml
security:
    # ...

    firewalls:
        secured_area:
            # ...
            form_login:
                # ...
                enable_csrf: true
```

``` twig
{# templates/login/index.html.twig #}

{# ... #}
<form action="{{ path('app_login') }}" method="post">
    {# ... the login fields #}

    <input type="hidden" name="_csrf_token" value="{{ csrf_token('authenticate') }}">

    <button type="submit">login</button>
</form>
```
Pour tester, on ouvre la route `/login` dans ton navigateur et on essaie de se connecter avec les différents comptes utilisateurs créés précédemment.

Si tout s'est bien passé, après identification, on se retrouve à l'accueil du site, avec, en bas de ta page, dans la barre de debug de Symfony, l'adresse email visible :

![login](./img/61.png)

https://symfony.com/blog/new-in-symfony-2-7-security-improvements#added-a-command-to-encode-a-password

## 16.6. Gestion du Logout

Ce serait une faille de sécurité importante s'il n'était pas possible à un utilisateur de fermer sa session.
https://symfony.com/doc/current/security.html#logging-out

``` yaml
# config/packages/security.yaml
security:
    # ...

    firewalls:
        main:
            # ...
            logout:
                path: app_logout

                # where to redirect after logout
                # target: app_any_route
```

``` php
// src/Controller/LoginController.php
namespace App\Controller;

use Symfony\Bundle\FrameworkBundle\Controller\AbstractController;
use Symfony\Component\Routing\Annotation\Route;

class LoginController extends AbstractController
{
    #[Route('/logout', name: 'app_logout', methods: ['GET'])]
    public function logout()
    {
        // controller can be blank: it will never be called!
        throw new \Exception('Don\'t forget to activate logout in security.yaml');
    }
}
```
## Récupération de l'utilisateur connecté

![user](./img/62.png)

## 16.7. Côté UI/UX : `app.user` de Twig

On a accès depuis Twig aux informations de l'utilisateur connecté grâce à `app.user` qui est une variable dite globale, qui contient toutes les informations de l'utilisateur actuellement auhentifié.

``` twig
{% if app.user %}
    {{ app.user.email }}
    <a href="{{ path('app_logout') }}"> Se déconnecter</a>
{% else %}
    <a href="{{ path('login') }}"> Se connecter</a>
{% endif %}
```
https://symfony.com/doc/current/templates.html#the-app-global-variable


En php on utilise :
``` php
$user = $this->getUser();
```
https://symfony.com/doc/current/security.html#fetching-the-user-object


[Return to Top](#notes-symfony)
# 17. **Sécuriser les routes**

Le but ici est de gérer les droits d'accès en fonction du type d'utilisateur et de leur **rôle**. 

## 17.1. Gestion des rôles et fichier `security.yaml`

https://symfony.com/doc/current/reference/configuration/security.html


On peut définir autant de rôles que le nécessite notre application. La seule chose à respecter est la nomenclature. Il faut systématiquement les écrire en **UPPER_SNAKE_CASE**, préfixés avec **ROLE_**. Exemple : “ROLE_COMPANY”, “ROLE_STUDENT”, “ROLE_TEACHER”, etc...
Il y a un rôle prédéfini dans symfony pour tous les utilisateurs : c’est le rôle “`ROLE_USER`”.

Si on souhaite récupérer les rôles que possède un utilisateur, on utilise l’objet `User`, à l’aide de `$user->getRoles()`. La propriété `$roles` est un tableau. Un utilisateur peut cumuler plusieurs rôles et pour redéfinir ses rôles, on doit passer par la méthode `$user->setRoles($roles)`; où `$roles` serait un tableau comportant tous les rôles souhaités.

Exemple du fichier `security.yaml` :
``` yaml
# config/packages/security.yaml
security:
    # ...
    role_hierarchy:
        ROLE_CONTRIBUTOR: ROLE_USER
        ROLE_ADMIN: ROLE_CONTRIBUTOR
```

Cela sous-entend que tous les utilisateurs ayant un rôle `ROLE_CONTRIBUTOR` ont par défaut droit aux mêmes choses que les utilisateurs ayant le `ROLE_USER`. Et que les utilisateurs ayant le ROLE_ADMIN héritent des mêmes droits que tous les `ROLE_CONTRIBUTOR` et indirectement des mêmes droits que ceux ayant le `ROLE_USER`.

Ce `ROLE_USER` est le rôle par défaut de tous les utilisateurs connectés, ajouté automatiquement par **Symfony**. La méthode `getRoles()` de l’entité `App\Entity\User`. Celle-ci renverra systématiquement au moins ce rôle.

Il existe également des rôles particuliers prédéfinis par Symfony :



https://symfony.com/doc/current/security.html#hierarchical-roles


## 17.2. Contrôle de l'authentification et des rôles

### 17.2.1. Vérifier si un utilisateur est loggué

``` php
// ...
public function adminDashboard(): Response
{
    $this->denyAccessUnlessGranted('IS_AUTHENTICATED');

    // ...
}
```
On peut également utiliser :
- `IS_AUTHENTICATED_REMEMBERED` : loggué avec un cookie remember me ou non.
- `IS_AUTHENTICATED_FULLY` : force à se logguer à nouveau, le cookie remember me ne fonctionne pas.
- `IS_REMEMBERED` : seulement les utilisateurs loggué avec un cookie remember me.
- `IS_IMPERSONATOR`


https://symfony.com/doc/current/security.html#checking-to-see-if-a-user-is-logged-in-is-authenticated-fully


### 17.2.2. Vérifier le rôle d'un utilisateur

Pour contrôler un rôle dans un contrôleur :
``` php
// BAD - $user->getRoles() will not know about the role hierarchy
$hasAccess = in_array('ROLE_ADMIN', $user->getRoles());

// GOOD - use of the normal security methods
$hasAccess = $this->isGranted('ROLE_ADMIN');
$this->denyAccessUnlessGranted('ROLE_ADMIN');
```

Pour contrôler un rôle ailleurs : dans un service par exemple :
``` php
#injecter le service Symfony\Component\Security\Core\Security
$this->security->isGranted('ROLE_ADMIN')
```

Pour contrôler un rôle dans `Twig` :
``` twig
{% if is_granted('ROLE_ADMIN') %}
  ...
{% endif  %}
```

## 17.3. Protéger une route grâce au fichier yaml

**Fichier `security.yaml`**
``` yaml
# config/packages/security.yaml
security:
    access_control:
        - { path: ^/admin, roles: ROLE_ADMIN }
        - { path: ^/program/new, roles: ROLE_CONTRIBUTOR }
        - { path: ^/program/[a-zA-Z_0-9-]+/edit, roles: ROLE_CONTRIBUTOR }
```

Cela va protéger l'accès à la page de création d'une série `/program/new` et celle d'édition `/program/{slug}/edit` qui permet l'édition d'une série.

Si on n'est pas connecté (ou en navigation privée par exemple), et que l'on tente d'accéder à la route `/program/new`, si tout est bien configuré, on est redirigé vers la page de login. Car on vient d'autoriser l'url `/program/new` uniquement aux utilisateurs ayant comme rôle le rôle "**ROLE_CONTRIBUTOR**" (au minimum). Le **ROLE_ADMIN** pourra également car il hérite du **ROLE_CONTRIBUTOR**.


Si on se log, on est autorisé à y accéder.Si tu regardes dans la barre de debug du profiler, on peut constater que l'on dispose bien du rôle **ROLE_CONTRIBUTOR** qui a été défini pour cet utilisateur dans les fixtures : `$user->setRoles(["ROLE_CONTRIBUTOR"])`.

Dans le fichier yaml le **path** comprend un `^`. C'est parce qu'il s'agit d'une expression régulière. Ainsi le path `^/program/[a-zA-Z_0-9-]+/edit` dans notre exemple, matchera l'url `/program/walking-dead/edit` par exemple.
**NB :** Si le path avait été `^/program/`, il aurait matché TOUTES les URLs commençant par `/program/`.

**Sécuriser la partie admin :**

On crée le fichier yaml suivant :
``` yaml
# config/routes/annotations.yaml
controllers:
    resource: ../../src/Controller/**/*
    exclude: ../../src/Controller/Admin
    type: attribute

admin:
    resource: ../../src/Controller/Admin
    type: attribute
    prefix: '/admin'
    #name_prefix: 'admin_
```
et on modifie le fichier :
``` yaml
# config/routes.yaml
kernel:
    resource: ../src/Kernel.php
    type: annotation
```

Cela va permettre de prefixer automatiquement toutes les routes du dossier Controller/Admin et les réserver aux rôles admin. La distinction des rôles est ainsi plus claire.


## 17.4. Protéger une route côté contrôleur

Seuls un **contributeur** ou un **administrateur** peut désormais créer une nouvelle série ou en éditer une existante. Si on veut qu'un **contributeur** ne peut modifier qu'une série qu'il a lui même créée on doit :
- Ajouter une propriété `owner` dans ta classe `Program`. (avec make:entity par exemple). Cette propriété `owner` sera une relation de type `ManyToOne` vers l'entité `User`. Penser à générer tes getter/setter.
- Modifier les fixtures pour associer un utilisateur en tant que propriétaire de la série dans ta classe `ProgramFixtures` en faisant appel à `$program->setOwner(...)`. Il faudra utiliser les méthodes `addReference()` et `getReference()`.
- Dans la méthode `new()` du `ProgramController` , Il faudra définit l'utilisateur connecté comme étant le propriétaire de la série nouvellement créée.

``` php
// src/Controller/ProgramController.php
#[Route('/program/new', name: 'program_new')]
public function new(Request $request, ProgramRepository $programRepository) : Response
{
    // ...
    if ($form->isSubmitted() && $form->isValid()) {
        // Deal with the submitted data
        // ...
        // Set the program's owner
        $program->setOwner($this->getUser());
        $programRepository->save($program, true);

        return $this->redirectToRoute('program_index');
    }
    // Render the form
    return $this->renderForm('program/new.html.twig', [
        "form" => $form,
    ]);
}
```

- Bloquer l'édition pour les contributeurs qui ne seraient pas propriétaires de la série concernée dans la méthode `edit()` du `ProgramController`.

``` php
// src/Controller/ProgramController.php
use Symfony\Component\Security\Core\Exception\AccessDeniedException;

#[Route('/{slug}/edit', name: 'program_edit', methods: ['GET', 'POST'])]
public function edit(Request $request, Program $program, ProgramRepository $programRepository): Response
{
    // Check wether the logged in user is the owner of the program
    if ($this->getUser() !== $program->getOwner()) {
        // If not the owner, throws a 403 Access Denied exception
        throw $this->createAccessDeniedException('Only the owner can edit the program!');
    }
        // ...
}
```
Ne pas oublier le `use`.


Il est également possible de verrouiller l'accès d'une URL via le controller directement via les attributs. Il faut mettre cette ligne au dessus de la méthode :
``` php
#[IsGranted('ROLE_ADMIN')]
```
Sans oublier le use :
``` php
use Sensio\Bundle\FrameworkExtraBundle\Configuration\IsGranted;
```
On peut ainsi gérer les droits finement, méthode par méthode. Mais on peut également mettre l'attribut précédent directement sur la classe pour verrouiller toutes les méthodes.

https://symfony.com/doc/current/security/voters.html
https://symfony.com/doc/current/SensioFrameworkExtraBundle/annotations/security.html


## 17.5. Filtrer côté vue

Pour ajouter des fonctionnalités comme des boutons d'édition qui ne serait présent que pour les utilisateurs ayant le **ROLE_ADMIN**, on peut ajouter cela dans `Twig` :

``` php
{% if is_granted("ROLE_ADMIN") %}
    <a href="{{ path('program_edit', { 'slug': program.slug} ) }}">Éditer</a>
{%endif%}
```

[Return to Top](#notes-symfony)
# 18. **Inscription d'un nouvel utilisateur**


## 18.1. Créer un compte utilisateur : implémenter un formulaire d'enregistrement

Il faut au préalable avoir une classe qui représente les utilisateurs : l'entité `User`. (cf chapitre précédent).

Pour créer le formulaire d'inscription, on utilise la commande :
``` sh
symfony console make:registration-form
```

Cette commande va générer :
- Un **controller** : `App\Controller\RegistrationController`
- Une classe de **formulaire** : `App\Form\RegistrationFormType`
- Une **vue** : `templates/registration/register.html.twig`

Il faudra bien évidemment modifier ces fichiers pour rendre le formulaire complet et fonctionnel. Notemment rajouter des champs pour toutes les propriétés de notre classe `User`.

https://symfony.com/doc/current/doctrine/registration_form.html

## 18.2. Connexion automatique de l'utilisateur inscrit

- Dans le RegistrationController :
``` php
<?php

class RegistrationController extends AbstractController
{
    public function __construct(
        private readonly FormLoginAuthenticator $authenticator
    ) {
    }

    #[Route('/register', name: 'app_register')]
    public function register(
        Request $request,
        UserPasswordHasherInterface $userPasswordHasher,
        EntityManagerInterface $entityManager,
        UserAuthenticatorInterface $authenticator
    ): Response {
            #...
            $authenticator->authenticateUser($user, $this->authenticator, $request);

            return $this->redirectToRoute('home');
        }

        return $this->render('registration/register.html.twig', [
            'registrationForm' => $form->createView(),
        ]);
    }

}
```

- Dans le fichier service.yaml

``` yaml
services:
    #...
    App\Controller\RegistrationController:
        arguments:
            $authenticator: '@security.authenticator.form_login.main'
```

## 18.3. Mot de passe oublié

Il est très souvent nécessaire d'avoir un lien **"mot de passe oublié"** disponible sous le formulaire de login, afin de permettre aux utilisateurs un peu tête en l'air de **réinitialiser** leur mot de passe. Attention, on parle bien ici de **réinitialisation**, il est **impossible de renvoyer** le mot de passe à un client puisque l'information est **hachée** en base de données.
- L'utilisateur clique sur le lien "mot de passe oublié".
- Un formulaire lui demande son adresse email (celle utilisée lors de la première inscription au site)
- un email est envoyé à cette adresse, contenant un lien (avec une durée de vie limitée).
le lien renvoie vers un formulaire demandant de saisir le nouveau mot de passe.


Une réinitialisation peut demander pas mal de travail. Exemple d’implémentation :
- créer un champ unique "reset_token" nullable dans l'entity User 
- créer un formulaire de demande de reset de password (champ email) 
- form soumis : si l'email existe, remplir le champ en bdd reset_token du user 
- envoyer un mail avec un lien vers une url, ex : "/reset-password/{reset_token}"
- créer le controller pour la page /reset-password. Le reset_token permet d'identifier de manière sûre que l'user est bien celui qui a fait la demande 
- la page affiche un formulaire demandant le nouveau password
- hash du password, mise à jour de la BD pour ce user


Heureusement, Symfony propose là encore d'automatiser grandement cette tâche (qui est assez répétitive puisque présente sur la plupart des sites). :

https://symfony.com/doc/current/security/passwords.html#reset-password
https://github.com/symfonycasts/reset-password-bundle



``` sh
composer require symfonycasts/verify-email-bundle
composer require symfonycasts/reset-password-bundle
symfony console make:reset-password
```

Si besoin d'insérer un user en DB sans passer par un form de registration, possibilité d'encoder le password via la commande

``` sh
symfony console security:hash-password
```

## 18.4 Bloquer connexion en attendant mail vérification

Préalable : lors du maker:bundle choisir la vérification du compte par email

https://symfony.com/doc/current/security/user_checkers.html

- Créer un custom checker dans `src/security`

``` php
namespace App\Security;

use App\Entity\User as AppUser;
use Symfony\Component\Security\Core\Exception\AccountExpiredException;
use Symfony\Component\Security\Core\Exception\CustomUserMessageAccountStatusException;
use Symfony\Component\Security\Core\User\UserCheckerInterface;
use Symfony\Component\Security\Core\User\UserInterface;

class UserChecker implements UserCheckerInterface
{
    public function checkPreAuth(UserInterface $user): void
    {
        if (!$user instanceof AppUser) {
            return;
        }

        if ($user->isDeleted()) {
            // the message passed to this exception is meant to be displayed to the user
            throw new CustomUserMessageAccountStatusException('Your user account no longer exists.');
        }
    }

    public function checkPostAuth(UserInterface $user): void
    {
        if (!$user instanceof AppUser) {
            return;
        }

        // user account is expired, the user may be notified
        if ($user->isExpired()) {
            throw new AccountExpiredException('...');
        }
    }
}
```

- Activer le custom checker dans `config/packages/security.yaml`

``` yaml
# ...
security:
    firewalls:
        main:
            pattern: ^/
            user_checker: App\Security\UserChecker
            # ...
```

``` sh
symfony console security:hash-password
```

- Dans la route `app_verify_email`

[Return to Top](#notes-symfony)
# 19. **Test Unitaires**


## 19.1. Introduction

Il est possible d’écrire des classes particulières dont le but est de tester si le code de son programme donne bien les résultats escomptés.

Un code source couvert par des tests est :
- Plus robuste (moins d’erreurs, moins de régressions)
- Mieux pensé (réfléchir à toutes les erreurs possibles pendant les tests permet de limiter en amont les problèmes)

Le code doit être testable **unitairement**
- On teste de petites choses, simples.
- Le code doit être découpé en conséquence

**Exemple de test :**

``` php
//src/Operation.php
Class Operation
{
   public function isEven(int $nb): bool
   {
       return ($nb % 2) === 0;
   }
}
```

``` php
//test/Operation.php
Class OperationTest extends…
{
   public function testEven()
   {
       $op = new Operation();
// méthode vérifiant si le résultat de la méthode isEven() avec le  mètre 4 vaut true
       $this->assertTrue($op->isEven(4));
   }
}
```
## 19.2. Tester en PHP

![TDD](./img/60.png)

1. **Ajouter** un test. **Avant** d’écrire le code de l’application. **Oblige** à penser à son code avant de l’écrire !

2. **Vérifier** que le test ne passe pas. **Normal** puisque le code n’est pas écrit

3. **Implémenter** la fonctionnalité. A minima, juste pour qu’elle renvoie un test correct

4. **Exécuter** les tests unitaires. **Vérifier** que les tests passent, sinon débug

5. **Refactoriser** le code source et exécuter à nouveau les tests unitaires. Si toujours ok, passer à l'objectif suivant et recommencer le processus à l’étape 1.

### 19.2.1. PHPUnit

Framework PHP pour faire des tests unitaires. Une syntaxe simple, facile à comprendre et à retenir.
- Un grand nombre de méthodes de tests.
- Organisation et exécution des test flexibles.
- Un utilitaire en ligne de commande complet.

Installation via composer :
``` sh
composer require phpunit/phpunit
```

Placer les tests dans un répertoire `tests/`, le code dans un répertoire `src/`, et configurer phpunit pour lui indiquer ces emplacements.

Lancer phpunit en ligne de commande (ou via l’IDE).

``` sh
php vendor/bin/phpunit --colors=auto tests
```

Tous les tests sont réalisés.
- Si un test échoue, PHPUnit indique pourquoi en rouge
- Si tout est bon, il l’indique avec un message en vert.


https://phpunit.readthedocs.io/fr/latest/writing-tests-for-phpunit.html#writing-tests-for-phpunit-data-providers

### 19.2.2. Exemples

``` php

```


``` php

```

https://symfony.com/doc/current/testing.html#integration-tests


[Return to Top](#notes-symfony)
# **Les requêtes personnalisées**


## Le QueryBuilder
Exemple de requêtes personnalisées dans le cadre d'un formulaire de recherche de séries. 

Si on utilise cette méthode :
``` php
$programs = $programRepository->findBy(['title' => $search]);
```
Il faut que l'on tape le nom exact de la série pour la retrouver. Ce qui n'est pas très pratique. 


Il serait plutôt intéressant de faire une recherche partielle à l'aide de mot clés qui seraient contenus dans le titre de la série. Pour effectuer cette requête partielle en **SQL**, tu dois utiliser le mot clé `LIKE` qui s'accompagne de % (jokers). Or, La méthode `findBy()` utilisée actuellement dans le contrôleur ne permet pas d'utiliser un `LIKE`. Tu vas devoir créer une **requête personnalisée.**

Pour cela, On va dans le fichier `App\Repository\ProgramRepository` (il y a un fichier Repository généré automatiquement pour chaque entité si on utilise la commande `make:entity`). 

C'est là que l'on va utiliser le `QueryBuilder`, objet proposé par `Doctrine`, qui va permettre de construire une **requête** via un ensemble de **méthodes**, sans avoir à taper directement du `SQL`, et tout en faisant le lien avec nos entités.


``` php
public function findLikeName(string $name)
{
    $queryBuilder = $this->createQueryBuilder('p')
        ->where('p.title LIKE :name')
        ->setParameter('name', '%' . $name . '%')
        ->orderBy('p.title', 'ASC')
        ->getQuery();

    return $queryBuilder->getResult();
}
```

- Quelques explications :

1. `createQueryBuilder('p')`. C'est ici que l'on crée le "**QueryBuilder**". En paramètre, on doit obligatoirement mettre un **alias** (par convention, c'est souvent la première lettre de l'entité concernée, ici 'p' pour 'Program', mais on peut mettre ce que l'onveut.


>**Il est où le SELECT ?**
Il n'est pas nécessaire d'ajouter une méthode `select()` car par défaut, étant dans le `ProgramRepository`, la requête **SQL** construite fera automatiquement un `SELECT` sur la table des programmes. Il est cependant possible d'utiliser cette méthode `select()` pour des utilisations plus avancées.

2. `where('p.title LIKE :name')`. La méthode `where()` permet d'exécuter une clause `WHERE` de **SQL**, c'est donc ici que le `LIKE` se place. ON est **obligé** de préfixer ton nom de champ par l'alias choisi précédemment (donc `p.title`)


>Très important
Note qu'ici, on construit une requête pour `Doctrine` (et non une requête **SQL**). Cela signifie que lorsque l'on écrit `p.title`, cela réfère à la propriété `$title` de `Program` et non directement au champ **title** de la table **program**. C'est crucial de comprendre cela (une erreur est vite arrivée) car le champ en base de données peut s'écrire différement de la propriété (par exemple une propriété `$createdAt` fera référence à une champ `created_at`, mais c'est `Doctrine` qui se chargera de faire le lien).

3. L'information provenant de l'utilisateur, on utilisera un **placeholder** pour effectuer une requête préparée et éviter les injections **SQL**. Pour spécifier la valeur de ce **placeholder**, c'est la méthode `setParameter()` qui est utilisée (c'est l'équivalent de `bindValue()` que l'on utilisait avec PDO).


>Rappel sécurité
Le **queryBuilder** te donne la possibilité de faire une requête préparée mais ce n'est ni obligatoire, ni automatique. Il en est de NOTRE responsabilité de développeur de penser à effectuer cette **requête préparée** et donc **protéger** ton application des **injections SQL**.

4. On peut ajouter d'autres méthodes (il en existe beaucoup) pour construire cette requête, comme `orderBy()`, `setMaxResults()`, `groupBy()`, `join()`, etc. On peut se référer à la **documentation** de Doctrine pour avoir une liste exhaustive des méthodes disponibles et de leur utilisation.

5. `getQuery()` Cette méthode **construit la requête SQL** en fonction des méthodes utilisées juste avant.

6. `getResult()` Cette méthode **exécute la requête SQL** et **retourne** les résultats. Par défaut, puisque l'on se trouve dans le `ProgramRepository`, cette méthode va renvoyer un tableau d'objets `Program`.

>Cependant, il est possible de renvoyer les résultats sous d'autres formats via des variantes de cette méthode, comme `getArrayResult()`, `getOneOrNullResult()`, etc. Là encore, il faut se référer à la documentation si on veut en savoir plus.

Il ne te reste plus qu'à modifier la méthode `findBy()` dans le `ProgramController` par `findLikeName($search)`;

``` php
// ProgramController
if ($form->isSubmitted() && $form->isValid()) {
    $search = $form->getData()['search'];
    $programs = $programRepository->findLikeName($search);
} else {
    $programs = $programRepository->findAll();
}
```
https://www.doctrine-project.org/projects/doctrine-orm/en/2.11/reference/query-builder.html

https://www.doctrine-project.org/projects/doctrine-dbal/en/current/reference/query-builder.html

https://symfonycasts.com/screencast/doctrine-queries/joins#play

https://symfonycasts.com/screencast/doctrine-queries/and-where-or-where#play


## L'alternative DQL

Le **QueryBuilder**, c’est bien, mais c’est assez éloigné de ce que nous avons l’habitude de faire en **SQL**. Et pour tirer le meilleur du **SQL** et de nos entités, **Doctrine** met à notre disposition le **DQL** pour Doctrine Query Language. Ce dernier permet d’écrire des requêtes très proches du SQL, tout en faisant le lien avec nos entités et leurs paramètres.

Par exemple : avoir la liste des séries avec une première saison sortie après 2010 :
``` php
public function findRecentPrograms()
{
    $em = $this->getEntityManager();
    $query = $em->createQuery('SELECT p, s FROM App\Entity\Program p
                              INNER JOIN p.seasons s
                              WHERE s.year>2010');

    return $query->execute();
}
```
Ici également, il faut continuer de penser **objet**. Ainsi, pour le cas d'une **jointure**, on ne va pas utiliser le nom d'une table, mais le nom pleinement qualifié d'une autre classe entité ainsi que le nom des propriétés, sans se soucier des noms réels dans le schéma en base de données.

Le **DQL** et le **QueryBuilder** offrent exactement les mêmes possibilités. Généralement, on préférera utiliser le **QueryBuilder**, car il permet de construire de façon plus dynamique une requête (grâce à son approche objet), sans avoir à manipuler une chaîne de caractères. Cela facilite les choses lorsque la requête doit être construite avec des conditions par exemples. De plus, ces requêtes sont plus faciles à tester via des librairies dédiées. Le **DQL** offre une syntaxe plus proche du SQL natif ce qui peut faciliter les choses pour écrire des requêtes longues et complexes.

Dans tous les cas, note que les requêtes écrites via le **QueryBuilder** seront au final transformées en **DQL** avant d'être exécutées !

https://www.doctrine-project.org/projects/doctrine-orm/en/2.11/reference/dql-doctrine-query-language.html

Pour que la recherche se fasse dans plusieurs propriétés différentes :
``` php
    public function findLikeName(string $name)
    {
        $queryBuilder = $this->createQueryBuilder('p')
            ->andWhere('p.title LIKE :name OR a.firstname LIKE :name')
            ->leftJoin('p.actors', 'a')
            ->setParameter('name', '%' . $name . '%')
            ->orderBy('p.title', 'ASC')
            ->getQuery();

        return $queryBuilder->getResult();
    }
```

Certains fonctionnalités MySQL ne sont pas disponibles via le querybuilder comme RAND(), dans ce cas :
https://forum.alsacreations.com/topic-20-85106-1-Resolu-Faire-un-rand-en-symfony.html
https://github.com/beberlei/DoctrineExtensions


[Return to Top](#notes-symfony)
# 20. **JS en Symfony**


## 20.1. Subtitle



[Return to Top](#notes-symfony)
# 20. **Main Title**


## 20.1. Subtitle













``` php

```

``` php

```


``` php

```

``` php

```


``` php

```

``` php

```


``` php
<?php

```

``` php
<?php

```


``` php
<?php

```


``` php
<?php

```


``` php
<?php

```


[Return to Top](#notes-symfony)
# 21. **CLI Symfony**

`php bin/console` et un alias de `symfony console`


- Pour avoir la liste des commandes :
``` sh
symfony console
```

``` sh
symfony console help 	 
symfony console list
symfony console about
```

- Pour créer un nouveau projet 
``` sh
symfony new --webapp wild-series
```

- Pour démarrer un serveur
``` sh
symfony server:start 
```
ou avec "-d" pour pouvoir réutiliser le terminal
``` sh
symfony server:start -d
```

-Pour ouvrir l'URL du serveur en cours dans ton navigateur
``` sh
symfony open:local
```

- Pour stopper le serveur
``` sh
symfony server:stop
```

- Pour lancer WebPAck. A faire à la racine du projet
``` sh
yarn watch
```

- Pour lancer WebPack et recharger navigateur à chaque modification
``` sh
yarn dev-server
```
- Compile les assets pour un environnement de production
``` sh
yarn build
```

Les commandes commençant par `symfony console` peut s'écrire aussi de la façon suivante  ou `php bin/console`.

- Pour lister toutes les commandes de ce type :
``` sh
symfony console list
// ou
php bin/console list
```


- Pour lister les routes
``` sh
symfony console debug:router
```


- Pour créer un nouveau controller 
``` sh
symfony console make:controller
```
On donne le nom du controller exemple : HomeController. Symfony crée la route et la view associée

## 21.1. Doctrine

- Pour créer une database

``` sh
symfony console doctrine:database:create
# ou symfony console d:d:c
```
- Pour créer une entité ou mettre à jour
``` sh
symfony console make:entity
```

- Pour mettre à jour la BDD :
``` sh
symfony console make:migration
```

Pour exécuter cette migration :
``` sh
symfony console doctrine:migrations:migrate
# ou symfony console d:m:m
```

Autre commande doctrine

``` sh
doctrine:database:create
doctrine:database:drop
make:entity --regenerate
doctrine:mapping:info
doctrine:schema:create
doctrine:schema:drop
doctrine:schema:update
doctrine:schema:validate
doctrine:migrations:migrate
doctrine:migrations:status
```
- Pour regénérer les setter et getter d'une entité
``` sh
symfony console make:entity --regenerate
```
- Pour détecter des entités 

``` sh
symfony console doctrine:mapping:info
```

- Pour valider des entités 
``` sh
symfony console doctrine:schema:validate
```

- Pour contrôler les migrations
``` sh
symfony console doctrine:migrations:status
```

- Pour créer une fixture :
``` sh
symfony console make:fixtures
```

- Pour exécutéer une fixture :
``` sh
symfony console doctrine:fixtures:load
```
- Pour rajouter des données sans écraser :
``` sh
php bin/console doctrine:fixtures:load --append
```

``` sh

```

``` sh

```

``` sh

```

Il est également possible de créer ses propres commandes :  
https://symfony.com/doc/current/console.html


