# Notes AJAX

## Tables of contents

- [Notes AJAX](#notes-ajax)
  - [Tables of contents](#tables-of-contents)
- [1. **Introduction**](#1-introduction)
- [2. **Exemple simplifié : Mise en pratique**](#2-exemple-simplifié--mise-en-pratique)
- [3. **Récupérer du JSON avec Fetch**](#3-récupérer-du-json-avec-fetch)
- [4. **Récupérer du JSON avec AXIOS**](#4-récupérer-du-json-avec-axios)
- [5. **Main Title**](#5-main-title)


[Return to Top](#notes-ajax)
# 1. **Introduction**

L'AJAX (Asynchronous JavaScript and XML) est un moyen d’échanger des données avec le serveur, sans recharger la page, en utilisant le JavaScript.

Cette technique utilise soit : 
- L’objet **XMLHttpRequest** du navigateur (technique historique) ,
- Des bibliothèques dédiée comme **Axios** (basé sur XMLHttpRequest )
- L’API native **Fetch**.

Dans tous les  cas le principe est le même :
1. Une **requête HTTP** (GET, POST,...) est envoyée à un serveur;
2. Le **serveur** traite les données;
3. Il renvoie une **réponse** en fonction (au format HTML, JSON, XML...), 
issue d'une API REST par exemple !
4. La réponse est récupérée par le **client en javascript**, 
puis affichée dans la page initiale, sans rechargement visible (manipulation du DOM).

Exemple :
https://wildcodeschool.github.io/ajax-quest/html/

La page HTML à cette adresse utilise **JavaScript** pour charger **après coup** un bloc de contenu **HTML**, et insérer ce bloc dans la page **existante**.

Voici à quoi ressemble le code :
``` js
function fetchAdditionalHTML() {
  fetch('additional-content.html')
    .then(function(response) {
      return response.text();
    })
    .then(function(htmlContent) {
      console.log('received data:', htmlContent);
      document.querySelector('#additional-content').innerHTML = htmlContent;
    });
}
setTimeout(fetchAdditionalHTML, 3000);
```

`fetch` est une fonction fournie nativement par JavaScript dans les navigateurs modernes. Un ancien système, *XMLHttpRequest*, existait et est toujours disponible, mais son utilisation est sensiblement plus complexe.

On donne à fetch un paramètre : l'adresse de la donnée à aller chercher (fetch = chercher). Celle-ci peut être une URL "**absolue**" (https://github.com/WildCodeSchool/ajax-quests/html/additional-content.html) ou "**relative**" : ici le fichier `additional-content.html` se trouve au même endroit que l'index de la page, donc on n'a pas besoin de préciser tout le chemin pour aller le chercher.

La fonction `fetch` est asynchrone. La programmation asynhchrone est un vaste sujet. Ici on se limitera à ce qui nous intéresse. Elle ne récupère pas les données immédiatement. Un **certain temps** est nécessaire pour que la requête **parvienne** au serveur, et que celui-ci **réponde** avec les données demandées. Il existe donc un mécanisme permettant d'indiquer qu'on veut exécuter du code **seulement après qu'on ait obtenu la réponse à la requête**. 

C'est le sens du `.then` : indiquer ce qui doit être fait quand on a reçu les données. Dans les parenthèses du `.then`, on indique une fonction qui sera appelée quand on aura reçu les données. Dans le code, on trouve deux `.then` qui s'enchaînent.

La fonction donnée au premier `.then` reçoit un objet response (souvent noté res) : il contient des informations sur la **réponse** envoyée par le serveur, et des données **brutes**. À partir de ces données brutes, on extrait le texte de la réponse : `response.text()` renvoie le code HTML que nous a transmis le serveur.

Le retour du premier `.then` va servir de paramètre au second `.then`, ici : `htmlContent`.

La ligne suivante va sélectionner un élément du DOM pour y afficher la réponse obtenue précédemment :

``` js
document.querySelector('#additional-content').innerHTML = htmlContent;
```
Le document HTML possède donc 
``` html
<div class="content" id="additional-content">
  <!-- This is empty on initial page load -->
</div>
```
Le `setTimeout`, à la dernière ligne, prend deux paramètres : une fonction, et un délai après lequel elle sera appelée. Ce délai est spécifié en millisecondes : on attend donc 3 secondes avant d'appeler fetchAdditionalHTML.

Une fonction appelée de cette façon est ce que l’on appelle un callback. Leur utilisation est monnaie courante en JavaScript. Mais sache que c’est aussi possible dans d’autres langages comme en PHP par exemple.

Ajax = requêtes et réponses asynchrones avec le serveur .
La page doit être mise à jour sans se rafraîchir.  
Manipulation du DOM pour écouter / modifier le contenu de la page.

https://developer.mozilla.org/fr/docs/Learn/JavaScript/Client-side_web_APIs/Fetching_data
https://developer.mozilla.org/fr/docs/Web/API/Fetch_API/Using_Fetch


[Return to Top](#notes-ajax)
# 2. **Exemple simplifié : Mise en pratique**

* ## Ajout d'un article dans un panier

![panier_01](/img/45.png)

Côté client :
1. Un utilisateur clique sur l’icone **panier**
2. Un eventListener **détecte** le clic sur le bouton et lance une fonction
3. Celle-ci envoie une **requête** au serveur (via *fetch*) vers une route permettant l'ajout du produit au panier (produit identifié par un *data-attribute* par exemple)

![panier_02](/img/46.png)

Côté serveur : 

4. Le **serveur** reçoit la requête, effectue les vérifications, modifie la base de données.
5. Le serveur renvoie une **réponse** (en JSON) et signale que tout s’est bien passé (code 2XX)

![panier_03](/img/47.png)

Côté client :

6. Le client récupère la réponse et modifie le DOM
7. Un nouvel élément HTML est ajouté dans le panier qui s’affiche sur la droite de l’écran

![panier_04](/img/48.png)

[Return to Top](#notes-ajax)
# 3. **Récupérer du JSON avec Fetch**

* ## Pourquoi du JSON ?

L'exemple précédent a montré une requête Ajax qui consiste à récupérer du HTML "prêt à l'emploi" via des requêtes Ajax. Cette pratique est plutôt désuète à l'heure actuelle.

Dans la pratique, et avec les mêmes mécanismes, on va plutôt vouloir récupérer des données telles que des **objets** ou des **tableaux d'objet**s. Ces données proviendront d'**API** : des services Internet qui ne fournissent pas de pages HTML, mais des **données**. Dans tous les langages - que ce soit `TypeScript`, `JavaScript`, `PHP` ou `Java` - on dispose de structures telles que les **tableaux** et les **objets**. Quand on les manipule, il faut garder à l'esprit que celles-ci sont stockées dans la mémoire de travail de l'ordinateur.

Chaque langage a sa propre façon de stocker ces données. Il est donc nécessaire de disposer d'un moyen permettant de transformer ces données dans un format "universel". Il existe plusieurs formats de communication "universels" ou "interopérables" : notamment `XML` et `JSON`. C'est ce dernier que nous allons utiliser.

Pour voir à quoi ressemblent des données JSON réelles, ouvre cette page sur l'API de GitHub : https://api.github.com/users/defunkt. Ce sont les données publiques du compte d'un des cofondateurs de GitHub. On peux remplacer le pseudo `defunkt` par le sien.

Cela ressemble au `JavaScript`, mais n'en est pas tout à fait. `JSON` est juste un format de données. Ce sont des données texte, écrites de telle manière qu'elles soient lisibles pour un humain comme pour un ordinateur. Les données sont écrites sous la forme de paires clé-valeur. C'est l'équivalent en texte des objets littéraux en JavaScript, des tableaux associatifs en PHP, des HashMap en Java.

https://www.youtube.com/watch?v=7mj-p1Os6QA  
https://www.youtube.com/watch?v=_I9KgdRvyQA


* ## La requête

Interface récente pour manipuler des requêtes/réponses HTTP simplement en Javascript vanilla (aucune bibliothèque requise).

``` js
fetch('https://jsonplaceholder.typicode.com/todos/1')
   .then(response => response.json())
   .then(json => console.log(json))
   .catch(() => alert('error'));
```

fetch() attend deux paramètres :
- 1er paramètre : Obligatoire, le chemin vers une ressource (URL). 
- 2nd paramètre : Optionnel, un objet comportant des réglages pour le fetch.

Exemple :

``` js
let myInit = { method: 'GET',
               mode: 'same-origin',
               cache: 'default' };
fetch('https://jsonplaceholder.typicode.com/todos/1', myInit)
   .then(response => response.json())
   .then(json => console.log(json))
   .catch(() => alert('error'));
```

`fetch()` a renvoyé une promesse. 
Si elle a été accomplie, elle passe par le 1er then. 
La réponse HTTP est traitée : ici, on souhaite en “extraire” le body d'une réponse au format json, ce qui retourne une nouvelle promesse.

Si la promesse est résolue avec succès, on traite le json reçu (affichage, manipulation…).

Remarque : c’est une bonne pratique UX d’afficher un loader lors des appels asynchrones.
Dans ce cas, son affichage se fait juste avant le fetch, et l'arrêt de son affichage se fera dans ce second `.then`.

S’il y a une erreur durant l'exécution, elle est attrapée par le `catch()`.


Le code de l'exemple suivant : https://wildcodeschool.github.io/ajax-quest/json-fetch/

``` js
function fetchGitHubProfileJSON() {
  const username = 'defunkt';
  const url = `https://api.github.com/users/${username}`;
  fetch(url)
    .then(function(response) {
      return response.json();
    })
    .then(function(profile) {
      const profileHtml = `
        <p><strong>${profile.name}</strong></p>
        <img src="${profile.avatar_url}" />
      `;
      document.querySelector('#github-profile').innerHTML = profileHtml;
    });
}
fetchGitHubProfileJSON();
```

Dans cette fonction, on génère la variable `url`, à partir de `username`. On appelle ensuite `fetch` avec cette URL comme argument pour lancer la requête. Même principe : `.then` permet d'attendre qu'on ait reçu la réponse du serveur, pour faire quelque chose des données obtenues.

Une différence notable avec l'exemple HTML : l'utilisation de `response.json()` au lieu de `response.text()`. `response.json()` est ce qui permet de transformer des données `JSON`, qui sont du texte, en objets exploitables par `JavaScript`.

La fonction exécutée dans le deuxième `.then` reçoit en paramètre un objet JSON retourné par le `.then` précédent et représentant un profil. Cet objet est constitué de paires clé-valeur ou attributs : en `JavaScript`, on accède à ces derniers via la syntaxe object.key (équivalent de $object['key'] en PHP). name et avatar_url sont deux attributs de l'objet profile.

Avec cet objet, on construit une chaîne `profileHtml`, par concaténation de ces attributs avec des balises HTML. Enfin, on insère le bloc `HTML` ainsi construit dans une `div`, possédant l’id `github-profile`, prévue à cet effet.

https://devhints.io/js-fetch

* ## Côté serveur : PHP (simple-MVC)

Requête via `fetch()` vers la route /products. Côté serveur, le routeur renvoie pour cette route vers la méthode `index()` du ProductController.

``` php
<?php
 public function index()
{
    $productManager = new ProductManager();
    $products = $productManager->selectAll();
    return json_encode($products);
}
```
Le serveur récupère les données en base. Le tableau est encodé en `json` avant d'être retourné. `Fetch()` récupère la réponse et la traite (par ex en modifiant le DOM).

* ## Exemple : site de réservation de logement

L'utilisateur accède à la page http://wildbnb.com sans avoir encore sélectionné sa position.

**Objectif :**
- Sélectionner la position
- Récupérer la liste des logements proches
- Afficher cette liste, sans rechargement sur la droite.

**Côté client :**

![wildbnb_01](/img/49.png)

L'utilisateur clique sur la carte. Cela déclenche un event JS et récupère latitudes et longitudes.  
En JS, requête HTTP (via fetch) vers une route /hotels configurée dans le routeur.
Coordonnées en paramètres   

``` js
fetch('/hotels?latitude=<lat>&longitude=<long>')
   .then(response => response.json())
   .then(json => console.log(json))
   .catch(() => alert('error'));
```

**Côté serveur :**
Le contrôleur récupère en base de données, la liste des hôtels les plus proches en fonction des coordonnées. On retrouve alors cette fonction dans le fichier `HotelController.php`

``` php
<?php
public function index()
{
    $latitude = $_GET['latitude'];
    $longitude = $_GET['longitude'];
    // TODO : clean and validate $_GET data

    // Custom query to get the nearest hotels
    $hotelManager = new HotelManager();
    $hotels = $hotelManager->findNeareast($latitude, $longitude);

    // return hotels data in json format
    return json_encode($hotels);
}
```

**Côté client :**
Le contrôleur retourne la liste des hôtels au format `JSON`.  
Coté JS, fetch() récupère cette réponse `JSON` puis transforme le `JSON` pour le mettre en forme et l'intégrer dans le cadre de résultats sur la page.

``` js
fetch('/hotels?latitude=<lat>&longitude=<long>')
   .then(response => response.json())
   .then(json => {
       // Transform JSON to HTML 
 //...
   })
   .catch(() => alert('error')
);

```

``` json
[{
   "id": 1,
   "name": "Le Grand Hôtel",
   "address": "12, avenue de paris",
   "latitude": 26.826999,
   "longitude": 16.21999,
}, {
   "id": 2,
   "name": "Hôtel de Paris",
   "address": "13, rue de rivoli",
   "latitude": 25.826999,
   "longitude": 17.21999,
}, {
   "id": 3,
   ...
}]
```


``` js
const results = document.getElementById('results');

// Transform JSON to HTML
for (hotel of hotels) {
   let card = document.createElement('div');
   card.innerHTML = `
           <h2>${hotel.name}<h2>
           <p>${hotel.address}</p>   
   `;
   // add data to #results
   results.appendChild(card);
}
```
![wildbnb_02](/img/50.png)



[Return to Top](#notes-ajax)
# 4. **Récupérer du JSON avec AXIOS**

https://github.com/axios/axios

`axios` est une bibliothèque pour l'envoi de requêtes Ajax, plus avancée que ne l'est `Fetch`.

`Fetch` présente l'avantage d'être disponible nativement sur tous les navigateurs modernes, mais `axios` simplifie la tâche du développeur, en fournissant :
- La transformation automatique d'objets JavaScript en JSON et vice-versa,
- De meilleurs mécanismes de gestion d'erreurs.

Pour ces raisons, il est en général conseillé d'utiliser `axios`. Le mécanisme reste cependant très similaire à `Fetch`. Le 3ème exemple se trouve ici et fait exactement la même chose que le précédent, à ceci près qu'il va chercher des données sur l'API Pokémon au lieu de celle de GitHub. C'est l'occasion de montrer que les objets JSON reçus d'une API peuvent être plus complexes, comme le montre la page d'accueil de l'API.

Voici le code :

``` js
// This function loads pokemon data from the Pokemon API
function fetchPokemonJSON() {
  // Feel free to download this HTML and edit it, to use another Pokemon ID
  const pokemonId = 1;
  const url = `https://pokeapi.co/api/v2/pokemon/${pokemonId}`;
  axios.get(url)
    .then(function(response) {
      return response.data; // response.data instead of response.json() with fetch
    })
    .then(function(pokemon) {
      console.log('data decoded from JSON:', pokemon);

      // Build a block of HTML
      const pokemonHtml = `
        <p><strong>${pokemon.name}</strong></p>
        <img src="${pokemon.sprites.front_shiny}" />
      `;
      document.querySelector('#pokemon').innerHTML = pokemonHtml;
    });
}
fetchPokemonJSON();
```

À part les noms des variables, et le contenu HTML généré, il y a très peu de différences :
- On a ajouté une balise `<script>` au-dessus de notre code pour charger axios, en précisant l’url où est hébergé la librairie https://cdnjs.cloudflare.com/ajax/libs/axios/0.19.0/axios.min.js dans l’attribut src.

- Dans le premier `.then()`, on indique non pas return `response.json()` pour décoder le JSON, mais return `response.data`. Note qu'il n'y a pas de parenthèses après response.data.

- Dans pokemonHtml, on va chercher une donnée "imbriquée" : comme l'API fournit plusieurs images, elles sont regroupées dans l'attribut `sprites` de l'objet pokemon. `sprites` est lui-même un objet, dans lequel on va chercher l'attribut string `front_shiny`.

[Return to Top](#notes-ajax)
# 5. **Main Title**
* ## Subtitle

``` php
<?php

```

