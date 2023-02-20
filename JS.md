# Notes JS

## Tables of contents

- [Notes JS](#notes-js)
  - [Tables of contents](#tables-of-contents)
- [1. **Introduction au format JSON**](#1-introduction-au-format-json)
  - [1.1. En Python](#11-en-python)
  - [1.2. En PHP](#12-en-php)


[Return to Top](#notes)
# 1. **Introduction au format JSON**

* ## Structure d'un objet JSON

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

* ## Travailler avec les objets JSON

Cela dépend du langage avec lequel on travaille :

## 1.1. En Python

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

## 1.2. En PHP

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


``` json

```


``` json

```


``` json

```


``` json

```

