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

# CRUD : GET avec MySQL

## Ecrire une première requête GET

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

La méthode `getMovies` sera appelée lors de l'accès à une route de l'API : 
https://www.monapi.com/api/movies

## Requête GET avec paramètres

Si on veut trouver un film avec son id, on va devoir transmettre l'id comme paramètre à l'URL :
https://www.monapi.com/api/movies/1

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
## Paramètre d'URL et query string

Il y a deux types de paramètres dans une URL. Les paramètres de route et les paramètres de requête.

### Les paramètres d'URL
Ils font partie de la route URL appelée par le client :
- `GET` : `/movies` retourner une liste de TOUS les éléments "movies" dans la base de données.
- `GET` `/movies/<idNumber>` (ex: /movies/12) renvoie un seul objet de type "movies" avec l'id de <idNumber>.

Les paramètres d'URL sont accessibles via `req.params`

### Les paramètres de requête : query string

Ce ne sont pas des paramètres d'URL. Les paramètres de requête doivent être utilisés pour tout type de filtrage que l'on prévoit d'utiliser sur la ressource spécifiée.
- GET : `/car/make/12/model` retourne d'une liste de modèles de voitures de la marque qui a l'id 12
- GET : `/car/make/12/model?color=mintgreen&doors=4` retour d'une liste de modèles de voitures de la marque qui a l'id 12, mais filtrée afin que seuls les modèles à 4 portes et une couleur vert menthe soient renvoyés.

Cela n'a pas de sens d'ajouter ces filtres dans les paramètres URL (`/car/make/12/model/color/mintgreen`) car selon REST, cela impliquerait que nous voulions des informations sur la couleur vert menthe.

Express gère les query string d'une manière similaire aux paramètres URL. Ils sont stockés dans un objet via `req.query` :

``` json
{
  "color": "mintgreen",
  "doors": 4
}
```

## Implémenter un filtre

Voici une fonction getMovies qui sera appelée sur la route `/movies` :
``` js
const getMovies = (req, res) => {
  const initialSql = "select * from movies";
  const where = [];

  if (req.query.color != null) {
    where.push({
      column: "color",
      value: req.query.color,
      operator: "=",
    });
  }
  if (req.query.max_duration != null) {
    where.push({
      column: "duration",
      value: req.query.max_duration,
      operator: "<=",
    });
  }

  database
    .query(
      where.reduce(
        (sql, { column, operator }, index) =>
          `${sql} ${index === 0 ? "where" : "and"} ${column} ${operator} ?`,
        initialSql
      ),
      where.map(({ value }) => value)
    )
    .then(([movies]) => {
      res.json(movies);
    })
    .catch((err) => {
      console.error(err);
      res.status(500).send("Error retrieving data from database");
    });
};
```
Si avec les critères de recherche on reçoit un tableau vide c'est tout de même le code 200 qui est envoyé. Là où dans la requête `/movies/7`, si la ressource 7 n'existe pas, c'est une 404 qui est renvoyé. Une ressource au singulier est considérée comme existante (200) ou inexistante (404) alors qu'une collection, même si elle est vide, retourne un code 200.


# Enregistrement des utilisateurs

Les utilisateurs doivent être enregistrés de manière sécurisée et les mots de passe ne doivent pas être stocké en clair dans la basse de donnée. Ils doivent être hasher avant d'être stocké afin qu'ils soient inutilisables si la base de données est compromise par des pirates.
https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html

## Utilisation d'un algorithme de hash dans Node.js

Il existe de nombreuses bibliothèques qui peuvent aide rà hasher un mot de passe. Ici on utilisera Argon 2. On commence donc par l'installer :

``` sh
npm i argon2
```
https://github.com/ranisalt/node-argon2/wiki/Options

Comme on veut hasher le mot de passe avant de l'insérer en base de données, on va se baser sur l'architecture middleware d'Express.

Dans le dossier `middleware`, on peut placer un fichier `auth.js` :

``` js
const argon2 = require("argon2");

const hashingOptions = {
  type: argon2.argon2id,
  memoryCost: 2 ** 16,
  timeCost: 5,
  parallelism: 1,
};

const hashPassword = (req, res, next) => {
  argon2
    .hash(req.body.password, hashingOptions)
    .then((hashedPassword) => {
      console.log(hashedPassword);

      req.body.hashedPassword = hashedPassword;
      delete req.body.password;

      next();
    })
    .catch((err) => {
      console.error(err);
      res.sendStatus(500);
    });
};

module.exports = {
  hashPassword,
};
```

Un hashage produit toujours un hash différent pour le même mot de passe. Lors de l'authentification, en comparant les deux hash, on sait s'ils viennent du même mot de passe.

# Authentification avec JWT

## Login

Pour s'identifier, l'utilisateur va donc entre ses identifiants. Le plus souvent  :
- un email
- un mot de passe

Dans une route /api/login, la requête de connexion ressemblerait à ceci :

``` js
POST http://localhost:5000/api/login
Content-type: application/json

{
  "email": "dwight@theoffice.com",
  "password": "123456"
}
```

Il va donc falloir :
- Créer la route
- Récupérer dans la BDD le mot de passe hashé de l'utilisateur pour l'email envoyé dans la requête
- Vérifier que le mot de passe hashé correspond au mot de passe envoyé dans la requête.

Pour cela on va utiliser encore une fois les middlewares.

Pour la route :

``` js
router.post("/api/login", userController.getUserByEmailWithPassword, verifyPassword);
```
La fonction `getUserByEmailWithPassword`

``` js
const getUserByEmailWithPassword = (req, res, next) => {
  const { email } = req.body;

  database
    .query("select * from users where email = ?", [email])
    .then(([users]) => {
      if (users[0] != null) {
        req.user = users[0];

        next();
      } else {
        res.sendStatus(401);
      }
    })
    .catch((err) => {
      console.error(err);
      res.status(500).send("Error retrieving data from database");
    });
};
```

La vérification se fait avec le package argon2 qui avait déjà servi à hasher le mot de passe. On peut donc ajouter la fonction `verifyPassword` dans le fichier `auth.js`.

``` js
const verifyPassword = (req, res) => {
  argon2
    .verify(req.user.hashedPassword, req.body.password)
    .then((isVerified) => {
      if (isVerified) {
        res.send("Credentials are valid");
      } else {
        res.sendStatus(401);
      }
    })
    .catch((err) => {
      console.error(err);
      res.sendStatus(500);
    });
};
```

## Le Json Web Token : JWT

Habituellement lorsque l'on se connecte sur un site web, une fois le login passé, le serveur renvoie une **preuve d'authentification**. Cette preuve est ensuite **stockée** par le client (navigateur) et **envoyée** au serveur dans les requêtes suivants. Cela peut être un **cookie** avec un identifiant de session par exemple. 

Mais l'utilisateur d'une session signifie que le serveur stocke les données pour chaque personne connectée, or le principe des API Rest est qu'une **API doit être sans état**.. Ce qui signifie que le serveur ne doit **stocker aucune information** sur qui fait les requêtes. Au lieu de cela, il doit founir une chaîne de caractère unique (chaque personne doit avoir une chaîne différente) pour identfier ses clients. Cet identifiant unique est appelée un token (ou jeton en français).

On doit donc créer une chaîne **unique** (une par client) qui peut contenir les informations sur la personne connectée (comme son identifiant) et que **seul** notre serveur peut créer. Il existe une norme qui couvre cela : le **JWT**.

Il faut donc d'abord installer le paquet `jsonwebtoken` sur notre serveur pour créer les JWT.

https://www.npmjs.com/package/jsonwebtoken

``` js
npm install jsonwebtoken
```

Ensuite il faut l'importer dans le fichier `auth.js` et l'inclure dans la fonction `verifyPassword` :

``` js
const jwt = require("jsonwebtoken"); // don't forget to import

const verifyPassword = (req, res) => {
  argon2
    .verify(req.user.hashedPassword, req.body.password)
    .then((isVerified) => {
      if (isVerified) {
        const payload = { sub: req.user.id };

        const token = jwt.sign(payload, process.env.JWT_SECRET, {
          expiresIn: "1h",
        });

        delete req.user.hashedPassword;
        res.send({ token, user: req.user });
      } else {
        res.sendStatus(401);
      }
    })
    .catch((err) => {
      console.error(err);
      res.sendStatus(500);
    });
};
```

Il ne faut pas oublier d'ajouter le JWT_SECRET aux variables d'environnement. C'est une chaîne de caractère secrète, propre au serveur, qui lui permet de signer le JWT.

Cette fonction retournera donc le JWT dont l'utilisateur se servira pour accéder à des ressources protégés.

**N'importe qui peut lire le contenu des jetons**, mais **SEUL** ton serveur peut les créer. Pour vérifier cela, on peut se rendre toi sur `jwt.io` et copier/coller un de tes tokens reçu. La payload peut être entièrement décodée mais pas la signature.

## Protection des routes

Maintenant que l'on peut obtenir une preuve d'authentification, on peut désormais protéger nos routes.
Si on peut protéger les routes d'ajout de films ou de livres, on peut rejeter les demandes sauf si elle contient une en-tête `Authorization` avec le schéma d'authentification `Bearer` suivi par un jeton valide.

https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization

Exemple :
``` js
POST http://localhost:5000/api/movies
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOjcsImlhdCI6MTY2MDIwMjczMywiZXhwIjoxNjYwMjA2MzMzfQ._5PYuoPoBfDtzq6fMsUn_8YGhfqtt_OaBVMHhe-FHlU
Content-type: application/json

{
  "title": "Citizen Kane",
  "director": "Orson Wells",
  "year": "1941",
  "color": "0",
  "duration": 120
}
```
On va donc créer un nouveau middleware `verifyToken` dans `auth.js` qui va faire ce travail

``` js
const verifyToken = (req, res, next) => {
  try {
    const authorizationHeader = req.get("Authorization");

    if (authorizationHeader == null) {
      throw new Error("Authorization header is missing");
    }

    const [type, token] = authorizationHeader.split(" ");

    if (type !== "Bearer") {
      throw new Error("Authorization header has not the 'Bearer' type");
    }

    req.payload = jwt.verify(token, process.env.JWT_SECRET);

    next();
  } catch (err) {
    console.error(err);
    res.sendStatus(401);
  }
}
```

Il suffit alors de placer cette fonction dans la définition de la route :

``` js
router.post("/", verifyToken, validator.validateMovieExpress, movieController.create);
router.put("/:id", verifyToken, validator.validateMovieExpress, movieController.updateById);
```
 ## Mur d'authentification

 Ajouter le middleware `verifyToken` sur chaque route que l'on souhaite protéger peut être fastidieux. Un moyen pratique consiste à d'abord répartir les routes entre celles qui sont publiques et celles qui doivent être protégées.

 Ensuite on va construire un "mur d'authentification" entre les deux parties. Chaqye route avant le mur restera inchangée, mais chaque route après le mur va nécessiter un jeton pour fonctionner.

 On peut construire un tel mur en activant le middleware verifyToken avec app.use sans aucun path. Le middleware sera exécuté pour toutes les requêtes à l'application déclarées après l'appel à app.use :

``` js
// the public routes

app.get("/api/movies", movieHandlers.getMovies);
app.get("/api/movies/:id", movieHandlers.getMovieById);

app.post(
  "/api/login",
  userHandlers.getUserByEmailWithPasswordAndPassToNext,
  verifyPassword
); // /!\ login should be a public route

// then the routes to protect

app.use(verifyToken); // authentication wall : verifyToken is activated for each route after this line

app.post("/api/movies", movieHandlers.postMovie);
app.put("/api/movies/:id", movieHandlers.updateMovie);
app.delete("/api/movies/:id", movieHandlers.deleteMovie);

// ...
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