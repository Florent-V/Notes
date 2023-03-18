# Notes JS API Express Node

[Return to Top](#notes-js-api-express-node)
# 1. **Création d'un server Express**

## Installation d'express

On commencer par créer le dossier de l'application puis on lancer un terminal à l'intérieur pour taper la commande suivante :

``` js
npm init
```
On répond aux questions ou on peut lancer cette commande ave -y pour que les réponses par défaut soient mises. Elles seront modifiables dans le fichier `package.json`

``` js
npm init -y
```

On peut maintenant installer express
``` js
npm install express
```

## Création de l'application

Dans le fichier `app.js` :

``` js
const express = require('express');
const app = express();

const port = 5000;

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(port, (err) => {
  if (err) {
    console.error('Something bad happened');
  } else {
    console.log(`Server is listening on ${port}`);
  }
});
```

Pour lancer le serveur :
``` sh
node app.js
```
Le serveur est lancé en allant sur le navigateur à l'adresse : `http://localhost:5000` ou en faisant une requête GET à cette adresse avec `postman`.

Ne pas oublier pour un dépôt github de mettre le dossier `nodemodule` dans le `.gitignore`

## Nodemon

Avec la solution précédente à chaque modification il faut couper et relancer le serveur. Pour éviter cela on peut utiliser le paquet `Nodemon`.

1. On installe le paquet 
``` sh
npm install nodemon --save-dev
```
On ne veut installer nodemon que dans les dépendances de développement, car nous n'utiliserons nodemon que lorsque nous développerons notre projet. On ne veut pas que ce paquet soit installé et utilisé en production.

2. On adapte le fichier `package.json`

``` sh
"main": "app.js",
"scripts": {
  "start": "node app.js",
  "dev": "nodemon app.js",
  "test": "echo \"Error: no test specified\" && exit 1"
},
```

## **Paramétrer une application avec dotenv**

Pour stocker certaines données on va  utiliser les variables d'environnement :
- Une application côté serveur nécessite un ensemble de paramètres spécifiques : port utilisé, nom de la base de données, nom d'utilisateur et mot de passe pour le compte autorisé à y accéder. Ces paramètres peuvent varier entre les différentes machines des développeurs, et le serveur de production où l'application sera déployée.
- Egalement si l'application nécessite une clé API pour fonctionner, ou un token. Il ne faut pas les partager et l'utilisateur de l'application doit pouvoir utiliser ses informations.

Cela va permettre d'améliorer le processur de déploiement et de portabilité et également la sécurité.

Le paquet npm `dotenv` fournit une solution efficace pour stocker et accéder à ces variables d'environnement, tout en évitant de les partager via un dépôt GitHub ! Ces données seront stockées dans des variables d'environnement.


On installe le package
``` sh
npm install dotenv
```

Il n'y a plus qu'à créer un fichier `.env` dans lequel on va mettre le port de connexion que l'on choisit :

``` js
SERVER_PORT=5000
```
Pour accéder aux variables d'environnement on procède ainsi :
``` js
require('dotenv').config() // this line is mandatory when you want to read variables from the '.env' file 
console.log(`The server will run on port ${process.env.SERVER_PORT}`);
```

Dans le fichier app.js cela donne :

``` js
require('dotenv').config();
const express = require('express');
const app = express();

const port = process.env.SERVER_PORT;
#...
```

Il ne faut pas oublier d'ajouter le fichier `.env` au `.gitignore`

Il est néanmoins conseillé de créer un fichier `.env.sample` qui sera similaire au fichier `.env` mais avec des valeurs fictives afin d'indiquer aux contributeurs ou aux utilisateurs de l'application les paramètres nécessaires pour que l'application fonctionne.

``` js
SERVER_PORT=PORT_YOU_CHOOSE
```

# Créer des routes

Les routes se définissent de cette manière :

## HANDLER

``` js
app.METHOD(PATH, HANDLER)
```
- **app** est une instance d'Express.
- **METHOD** est une méthode de requête HTTP. (GET, POST, PUT, DELETE)
- **PATH** est un chemin sur le serveur.
- **HANDLER** est la fonction exécutée lorsque le chemin est reconnu

Un exemple de requête get :

``` js
app.get("/", (req, res) => {
  res.send("Welcome to Express");
});
```
Le `HANDLER` est une fonction exécutée lorsque la route est déclenchée par une requête. Elle est peut être écrite directement dans la déclaration de route mais également déportée ailleurs dans le code :

``` js
const handler = (req, res) => {
  res.send("Welcome to Express");
};

app.get("/search", handler);
```
Le `HANDLER` prend 2 paramètres correspondant à deux objets HTTP définis dans Express :
- Un objet de type **Request** (par convention le paramètre est appelé `request` ou plus souvent `req`)
- Un objet de type **Response** (par convention, le paramètre est appelé `response` ou plus souvent `res`)

Chacun de ces objets a de nombreuses méthodes et propriétés.

## Request

http://expressjs.com/fr/4x/api.html#req

L'objet de requête représente la requête HTTP. Il contient des informations telles que :
- l'en-tête HTTP,
- Le corps de la requête (ce qui est envoyé avec la requête),
- Données de formulaire,
- Paramètres de l'URL et query string, ...


### req.params

Cette méthode permet de récupérer les paramètres de l'url :

``` js
const welcomeName = (req, res) => {
  res.send(`Welcome ${req.params.name}`);
};

app.get("/users/:name", welcomeName);
```

## Response

http://expressjs.com/fr/4x/api.html#res

L'objet response représente la réponse HTTP que le serveur envoie au client. Il peut contenir des données, des messages (validation, erreur), ou simplement un état correspond à l'état de la requête traitée par le serveur.

### res.send

Permet d'envyer des données : string, object, array, buffer

``` js
(req, res) => {
  res.send(‘Validated’);
};
```

### res.status

Pour joindre un message de statut dans la réponse. Généralement combiné avec le send.

``` js
(req, res) => {
  res.status(404).send(‘Cannot find /foo’);
};
```
### res.sendStatus

Pour n'envoyer que le statut de la requête

``` js
(req, res) => {
  res.sendStatus(200);
};
```

### res.json

Pour onvoyer u objet au format json

``` js
(req, res) => {
  res.json({ result: ‘10 items found’ });
};
```

### res.end

permet de terminer la requête sans envoyer de données particulières

``` js
(req, res) => {
  res.end(); // or res.status(404).end();
};
```

https://www.youtube.com/watch?v=pKd0Rpw7O48

# Utilisation d'une base de données MySQL

On suppose que la base de données est déjà crée avec ses tables et ses doonées.

## Le module MySQL 2

Pour communiquer avec la base de données, on peut installer le module `mysql2`
https://www.npmjs.com/package/mysql2

``` js
npm install mysql2
```

## Configuration de l'accès à la base de données

On peut créer un fichier `.env.sample` comme cela :
``` 
DB_HOST=localhost
DB_PORT=3306
DB_USER=REPLACE_WITH_YOUR_USERNAME
DB_PASSWORD=REPLACE_WITH_YOUR_PASSWORD
DB_NAME=REPLACE_BY_DB_NAME
```

Ensuite créer un fichier `.env` pour remplacer avec nos valeurs.

>Il ne faut pas oublier de complèter avec ses données. Le port MySQL par défaut est 3306, mais selon la façon dont tu l'as installé et configuré, cela pourrait être autre chose ! (3309 avec une installation Docker)

On peut ensuite créer un fichier `database.js` :
``` js
require("dotenv").config();
const mysql = require("mysql2/promise");

require("dotenv").config();

const mysql = require("mysql2/promise");

const database = mysql.createPool({
  host: process.env.DB_HOST, // address of the server
  port: process.env.DB_PORT, // port of the DB server (mysql), not to be confused with the APP_PORT !
  user: process.env.DB_USER,
  password: process.env.DB_PASSWORD,
  database: process.env.DB_NAME,
});

database
  .getConnection()
  .then(() => {
    console.log("Can reach database");
  })
  .catch((err) => {
    console.error(err);
  });
```

Ce fichier permettra de créer un pool de connexion à l'aide des variables d'environnement puis essaiera d'obtenir une première connexion depuis le pool pour vérfier que tout se passe bien.

## Ecrire une première requête

En utilisant l'objet `database`, on peut envoyer des requêtes en utilisant la méthode `query()`. - Cette méthode prend comme premier paramètre une chaîne de caractère qui sera le code SQL de la requête.
- Ici on utilise la version avec les promesses on va chaîner l'appel à `query()` avec les méthodes `.then()` et `.catch()` pour intercepter les erreurs.

``` js
database
  .query("select * from movies")
  .then((result) => {
    console.log(result);
  })
  .catch((err) => {
    console.error(err);
  });
```
> Il n'est pas obligatoire d'utiliser la méthode `getConnection()` : faire une requête créera aussi automatiquement une connexion. Cependant, il est recommandé de l'utiliser pour déboguer ton serveur en cas d'échec de la connexion.

`result` est un tableau contenant le contenu de la requête comme premier élément. Le reste contient des informations supplémentaires concernant la requête. On va pouvoir utiliser la déstructuration des tableaux pour ne sélectionner que le 1er élément.

On peut donc déplacer ce code dans un fichier dédié. On rajoute la ligne `module.exports = database;` à la fin du fichier `database.js` puis dans le nouveau fichier :

``` js
const database = require("./database");

const getMovies = (req, res) => {
  database
    .query("select * from movies")
    .then(([movies]) => {
      res.json(movies);
    })
    .catch((err) => {
      console.error(err);
      res.status(500).send("Error retrieving data from database");
    });
};
```

La méthode `getMovies` sera appelée lors de l'accès à une route de l'API.

## Ecrire une première requête avec un paramètre

Si on veut trouver un film avec son id, on va devoir transmettre l'id comme paramètre :

``` js
const getMovieById = (req, res) => {
  const id = parseInt(req.params.id);

  database
    .query(`select * from movies where id = ${id}`)
    .then(...)
    .catch(...);
}
```

Cette façon de procéder n'est pas très sure car elle rend vulnérable aux injections SQL. Il va falloir utiliser les requêtes préparées à la place :

``` js
const getMovieById = (req, res) => {
  const id = parseInt(req.params.id);

  database
    .query("select * from movies where id = ?", [id])
    .then(([movies]) => {
      if (movies[0] != null) {
        res.json(movies[0]);
      } else {
        res.status(404).send("Not Found");
      }
    })
    .catch((err) => {
      console.error(err);
      res.status(500).send("Error retrieving data from database");
    });
};
```

``` js

```

``` js

```

``` js

```

``` js

```

``` js

```
``` js

```

``` js

```

``` js

```

``` js

```

``` js

```

``` js

```
``` js

```

``` js

```

``` js

```

``` js

```

``` js

```

``` js

```
``` js

```

``` js

```

``` js

```

``` js

```

``` js

```

``` js

```
``` js

```

``` js

```

``` js

```

``` js

```

``` js

```

``` js

```
``` js

```

``` js

```

``` js

```

``` js

```

``` js

```

``` js

```

//

``` js

```

``` js

```

``` js

```
``` js

```

``` js

```

``` js

```

``` js

```

``` js

```

``` js

```