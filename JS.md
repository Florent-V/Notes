# Notes JS
- [Notes JS](#notes-js)
- [1. **Introduction au format JSON**](#1-introduction-au-format-json)
  - [1.1. Structure d'un objet JSON](#11-structure-dun-objet-json)
  - [1.2. Travailler avec les objets JSON](#12-travailler-avec-les-objets-json)
    - [1.2.1. En Python](#121-en-python)
    - [1.2.2. En PHP](#122-en-php)
- [**Jason Web Token (JWT) : Authentification sur une API**](#jason-web-token-jwt--authentification-sur-une-api)
  - [Explications rapides du JWT](#explications-rapides-du-jwt)
  - [Préparatifs](#préparatifs)
  - [Obtention du token](#obtention-du-token)
  - [Middleware d'authentification](#middleware-dauthentification)
  - [Page protégée](#page-protégée)
  - [Page d'enregistrement](#page-denregistrement)


[Return to Top](#notes)
# 1. **Introduction au format JSON**

## 1.1. Structure d'un objet JSON

Les données sont classées en objets et sous la forme d'une struture arborescente :
- une racine a une clé : le nom de l'objet
- ses branches ont des clés et des valeurs : les attributs de l'objet

Des tableaux (array) peuvent aussi être imbriqués dans des objets JSON :

``` json
{ 
    "first_name" : "Sammy",
    "last_name" : "Shark",
    "location" : "Ocean",
    "age": 10,
    "psychopath": true,
    "emergencyCall": {
            "firstname": "Liane",
            "lastname": "Cartman",
            "number": 5556754
    },
    "hobbies": [
            "World of Warcraft",
            "Tacos",
            "Drink tears"
    ],
    "friends": null,
    "websites" : [
        {
            "description" : "work",
            "URL" : "https://www.digitalocean.com/"
        },
        {
            "desciption" : "tutorials",
            "URL" : "https://www.digitalocean.com/community/tutorials"
        }
    ],
    "social_media" : [
        {
            "description" : "twitter",
            "link" : "https://twitter.com/digitalocean"
        },
        {
            "description" : "facebook",
            "link" : "https://www.facebook.com/DigitalOceanCloudHosting"
        },
        {
            "description" : "github",
            "link" : "https://github.com/digitalocean"
        }
    ]
}
```
Le format JSON est de plus en plus utilisé par les développeurs. Il est beaucoup plus léger que le format XML :

**XML**
``` xml
<users>
    <user>
        <username>SammyShark</username> <location>Indian Ocean</location>
    </user>
    <user>
        <username>JesseOctopus</username> <location>Pacific Ocean</location>
    </user>
    <user>
        <username>DrewSquir</username> <location>Atlantic Ocean</location>
    </user>
    <user>
        <username>JamieMantisShrimp</username> <location>Pacific Ocean</location>
    </user>
</users>
```
**JSON**

``` json
{"users": [
  {"username" : "SammyShark", "location" : "Indian Ocean"},
  {"username" : "JesseOctopus", "location" : "Pacific Ocean"},
  {"username" : "DrewSquid", "location" : "Atlantic Ocean"},
  {"username" : "JamieMantisShrimp", "location" : "Pacific Ocean"}
] }
```

## 1.2. Travailler avec les objets JSON

Cela dépend du langage avec lequel on travaille :

###  1.2.1. En Python

**Parse JSON - Convert from JSON to Python**

On utilise la méthode `json.loads()` sur un string d'un objet JSON pour le transformer en dictionnaire python.

``` python
import json

# some JSON (type string):
x =  '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x)

# the result is a Python dictionary:
print(y["age"]) # Output : 30
```

**Convert from Python to JSON**

Si on a un objet python (dictionnaire), on utilise la méthode `json.dumps()` pour le convertir en un string `JSON`.

``` python
import json

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)  #{"name": "John", "age": 30, "city": "New York"}
```

Le string `JSON` produit n'est pas facile à lire, sans indentations ni sauts de ligne. Pour faciliter la lecture, la méthode `json.dumps()` a des paramètres :


``` python
# formate l'affichage avec l'indentation
json.dumps(x, indent=4)
# remplace les , par des . et les : par des =
json.dumps(x, indent=4, separators=(". ", " = "))
# trie les clés par ordre alphabétique
json.dumps(x, indent=4, sort_keys=True)
```

### 1.2.2. En PHP

**Lire un JSON depuis un fichier ou un string**

D'abord on récupère la data d'un fichier dans une variable en utilisant `file_get_contents()`. Une fois que l'on a la data dans un string, on appelle la fonction `json_decode()` pour extraire l'information depuis un string.

La fonction `json_decode()` accepte 4 paramètres mais on va en utiliser deux la majeure partie du temps. Le second paramètre détermine comment la data décodée est retournée. Si c'est `true` cela va retouner un tableau associatif, si c'est `false`, cela va retouner un objet.

Si le fichier people.json contient :
``` json
{
    "name": "Monty",
    "email": "monty@something.com",
    "age": 77
}
```
ON peut lire le fichier JSON avec le code suivant :
Avec false comme deuxième paramètre :

``` php
<?php
 
$people_json = file_get_contents('people.json');
 
$decoded_json = json_decode($people_json, false);
 
echo $decoded_json->name;
// Monty
 
echo $decoded_json->email;
// monty@something.com
 
echo $decoded_json->age;
// 77
?>
```
Avec true comme deuxième paramètre :

``` php
<?php
 
$people_json = file_get_contents('people.json');
 
$decoded_json = json_decode($people_json, true);
 
echo $decoded_json['name'];
// Monty
 
echo $decoded_json['email'];
// monty@something.com
 
echo $decoded_json['age'];
// 77
?>
```
Pour un fichier JSON avec des objets imbriqués :

``` json
{
    "name": "Monty",
    "email": "monty@something.com",
    "age": 77,
    "countries": [
        {"name": "Spain", "year": 1982},
        {"name": "Australia", "year": 1996},
        {"name": "Germany", "year": 1987}
    ]
}
```
`$decoded_json['countries']` sera donc en réalité un tableau sur lequel on va pouvoir boucler.

``` php
<?php
 
$people_json = file_get_contents('people.json');
 
$decoded_json = json_decode($people_json, true);
 
$name = $decoded_json['name'];
$countries = $decoded_json['countries'];
 
foreach($countries as $country) {
    echo $name.' visited '.$country['name'].' in '.$country['year'].'.';
}
/*
Monty visited Spain in 1982.
Monty visited Australia in 1996.
Monty visited Germany in 1987.
*/
 
?>
```
Un peu plus compliqué encore :

``` json
{
    "customers": [
      {
        "name": "Andrew",
        "email": "andrew@something.com",
        "age": 62,
        "countries": [
          {
            "name": "Italy",
            "year": 1983
          },
          {
            "name": "Canada",
            "year": 1998
          },
          {
            "name": "Germany",
            "year": 2003
          }
        ]
      },
      {
        "name": "Sajal",
        "email": "sajal@something.com",
        "age": 65,
        "countries": [
          {
            "name": "Belgium",
            "year": 1994
          },
          {
            "name": "Hungary",
            "year": 2001
          },
          {
            "name": "Chile",
            "year": 2013
          }
        ]
      },
      {
        "name": "Adam",
        "email": "adam@something.com",
        "age": 72,
        "countries": [
          {
            "name": "France",
            "year": 1988
          },
          {
            "name": "Brazil",
            "year": 1998
          },
          {
            "name": "Poland",
            "year": 2002
          }
        ]
      },
      {
        "name": "Monty",
        "email": "monty@something.com",
        "age": 77,
        "countries": [
          {
            "name": "Spain",
            "year": 1982
          },
          {
            "name": "Australia",
            "year": 1996
          },
          {
            "name": "Germany",
            "year": 1987
          }
        ]
      }
    ]
}
```


``` php
<?php
 
$people_json = file_get_contents('people.json');
 
$decoded_json = json_decode($people_json, true);
 
$customers = $decoded_json['customers'];
 
foreach($customers as $customer) {
    $name = $customer['name'];
    $countries = $customer['countries'];
 
    foreach($countries as $country) {
        echo $name.' visited '.$country['name'].' in '.$country['year'].'.';
    }
}
/*
Andrew visited Italy in 1983.
Andrew visited Canada in 1998.
Andrew visited Germany in 2003.
 
Sajal visited Belgium in 1994.
Sajal visited Hungary in 2001.
Sajal visited Chile in 2013.
 
Adam visited France in 1988.
Adam visited Brazil in 1998.
Adam visited Poland in 2002.
 
Monty visited Spain in 1982.
Monty visited Australia in 1996.
Monty visited Germany in 1987.
*/
?>
```
Pour un fichier JSON dont on ne connait pas les clés avant :

``` json
{
    "kdsvhe": {
        "name": "Andrew",
        "age": 62
    },
    "lvnwfd": {
        "name": "Adam",
        "age": 65
    },
    "ewrhbw": {
        "name": "Sajal",
        "age": 72
    },
    "klkwcn": {
        "name": "Monty",
        "age": 77
    }
}
```


``` php
<?php
$people_json = file_get_contents('people.json');
 
$decoded_json = json_decode($people_json, true);
 
foreach($decoded_json as $key => $value) {
    $name = $decoded_json[$key]["name"];
    $age = $decoded_json[$key]["age"];
     
    echo $name.' is '.$age.' years old.';
}
/*
Andrew is 62 years old.
Adam is 65 years old.
Sajal is 72 years old.
Monty is 77 years old.
*/
?>
```
**Créer un fichier JSON en PHP**

On peut transformer notre propre data bien formatée en string JSON avec la fonction json_encore(). Elle accepte 3 paramètres mais on utilise majoritairement que le premier :

``` php
<?php
 
$people_info = [
    "customers" => [
        ["name" => "Andrew", "score" => 62.5],
        ["name" => "Adam", "score" => 65.0],
        ["name" => "Sajal", "score" => 72.2],
        ["name" => "Monty", "score" => 57.8]
    ]
];
echo json_encode($people_info);
/*
{"customers":[{"name":"Andrew","score":62.5},{"name":"Adam","score":65},{"name":"Sajal","score":72.2},{"name":"Monty","score":57.8}]}
*/
?>
```
On peut utiliser d'autres paramètres pour obtenir un JSON bien formaté. Par exemple JSON_PRETTY_PRINT pour formatter le JSON et également JSON_PRESERVE_ZERO_FRACTION pour être sur que les float seront enregistrés comme des float :

``` php
<?php
$people_info = [
    "customers" => [
        ["name" => "Andrew", "score" => 62.5],
        ["name" => "Adam", "score" => 65.0],
        ["name" => "Sajal", "score" => 72.2],
        ["name" => "Monty", "score" => 57.8]
    ]
];
echo json_encode($people_info, JSON_PRETTY_PRINT|JSON_PRESERVE_ZERO_FRACTION);
/*
{
    "customers": [
        {
            "name": "Andrew",
            "score": 62.5
        },
        {
            "name": "Adam",
            "score": 65.0
        },
        {
            "name": "Sajal",
            "score": 72.2
        },
        {
            "name": "Monty",
            "score": 57.8
        }
    ]
}
*/
?>
```
# **Jason Web Token (JWT) : Authentification sur une API**

## Explications rapides du JWT

Le JWT est un token composé de 3 parties séparées par un point :
- Le **Header**
Le header détermine le type de token : JWT et l'algorithme de chiffrement HS256 (HMAC avec du SHA-256) ou RS256 (signature RSA avec du SHA-256).
``` json
{
  "alg": "HS256",
  "typ": "JWT"
}
```
- Le **Payload**
La partie qui contient les informations de l'utilisateur comme son id, son nom d'utilisateur, etc...

- La **Signature**
c'est la partie la plus complexe car elle prend en compte un mot secret.

## Préparatifs

Dans un nouveau dossier que vous nommez "api", initialisez votre projet avec la commande
- `npm init -y`
Puis installez les modules 
- `npm i express jsonwebtoken cors`
- `npm i -D morgan`

- express (version XX) : le framework HTTP
- jsonwebtoken (version XX) : générer un JWT
- cors (version XX) : activer le CORS
- morgan (version XX) : avoir des logs dans le terminal.

``` js
const express = require('express')
const morgan = require('morgan')
const jwt = require('jsonwebtoken')
const cors = require('cors')

const PORT = 1234
const SECRET = 'mykey'

// Initialisation de Express
const app = express()

app.use(cors())                                 // Activation de CORS
app.use(morgan('tiny'))                         // Activation de Morgan
app.use(express.json())                         // Activation du raw (json)
app.use(express.urlencoded({ extended: true })) // Activation de x-wwww-form-urlencoded

// Liste des utilisateurs
const users = [
    { id: 1, username: 'admin', password: 'password123' }
]

/* Ici les futures routes */

app.get('*', (req, res) => {
    return res.status(404).json({ message: 'Page not found' })
})

app.listen(PORT, () => {
    console.log(`Server is running on port ${PORT}.`)
})
```

Le serveur est prêt sauf qu'il manque les routes...
**Remarque :** dans l'idéal, c'est mieux de stocker la valeur `SECRET` dans un fichier de configuration.

## Obtention du token

Dans la route `/login`, on invite l'utilisateur à se connecter avec son login et son mot de passe.

``` js
/* Formulaire de connexion */
app.post('/login', (req, res) => {
    // Pas d'information à traiter
    if (!req.body.username || !req.body.password) {
        return res.status(400).json({ message: 'Error. Please enter the correct username and password' })
    }

    // Checking
    const user = users.find(u => u.username === req.body.username && u.password === req.body.password)

    // Pas bon
    if (!user) {
        return res.status(400).json({ message: 'Error. Wrong login or password' })
    }

    const token = jwt.sign({
        id: user.id,
        username: user.username
    }, SECRET, { expiresIn: '3 hours' })

    return res.json({ access_token: token })
})
```
On lance le serveur avec la commande `node index.js` (pensez à redémarrer votre serveur lors de la modification de ce dernier).

- On vérifie d'abord que l'utilisateur a bien saisi les 2 champs obligatoires. Si ce n'est pas le cas, on retourne une erreur 400 l'invitant à les saisir.
- On vérifie ensuite dans le tableau des utilisateurs que le nom et le mot de passe correspondent via la fonction `find`. Si ce n'est pas le cas, alors une erreur 400 informe l'utilisateur sur l'échec de son authenfication.
- Si c'est le cas, alors le token est donné à l'utilisateur final qui pourra l'utiliser pour se connecter sur les routes nécésitant d'une authentification.

Les requêtes peuvent être testées avec postman ou avec curl

## Middleware d'authentification

On va mettre en place un middleware pour chaque page protégée. Pour ce faire, on vérifie la présence du token dans le header de la requête ainsi que sa véracité.


``` js
/* Récupération du header bearer */
const extractBearerToken = headerValue => {
    if (typeof headerValue !== 'string') {
        return false
    }

    const matches = headerValue.match(/(bearer)\s+(\S+)/i)
    return matches && matches[2]
}

/* Vérification du token */
const checkTokenMiddleware = (req, res, next) => {
    // Récupération du token
    const token = req.headers.authorization && extractBearerToken(req.headers.authorization)

    // Présence d'un token
    if (!token) {
        return res.status(401).json({ message: 'Error. Need a token' })
    }

    // Véracité du token
    jwt.verify(token, SECRET, (err, decodedToken) => {
        if (err) {
            res.status(401).json({ message: 'Error. Bad token' })
        } else {
            return next()
        }
    })
}
```

## Page protégée

Ainsi, on peut insérer facilement ce middleware pour gérér l'authentification des pages protégées par ce dernier.


``` js
app.get('/me', checkTokenMiddleware, (req, res) => {
    // Récupération du token
    const token = req.headers.authorization && extractBearerToken(req.headers.authorization)
    // Décodage du token
    const decoded = jwt.decode(token, { complete: false })

    return res.json({ content: decoded })
})
```

On peut essayer les requêtes avec et sans token pour vérifier. Dans postman on peut utiliser le volet Authorization et choisir Bearer token. Ou en curl :

``` sh
curl -X GET \
  http://localhost:1234/me \
  -H 'Authorization: Bearer ici_le_token_valide_obtenu_lors_du_login'
```

``` json

```


``` json

```


``` json

```


@TODO
## Page d'enregistrement


