# Réalisation et sécurisation des formulaires en PHP

## Tables of contents

1. [Rappel : Formulaire en HTML](#rappel--formulaire-en-html)
2. [Récupération des données avec PHP](#récupération-des-données-avec-php)
3. [Sécurisation côté utilisateur](#sécurisation-côté-utilisateur)
4. [Sécurisation côté serveur](#sécurisation-côté-serveur)



##### [Return to Top](#réalisation-et-sécurisation-des-formulaires-en-php)
# **Rappel : Formulaire en HTML**

``` html
<form action="thanks.php" method="post" id="survey-form">
    <fieldset class="personnal-info">
        <div class="field">
            <label for="name">Prénom</label>
            <input type="text" name="name" id="name" class="form-control" placeholder="Entrer votre prénom" required/>
        </div>
        <div class="field">
            <label for="last-name">Nom</label>
            <input type="text" name="last-name" id="last-name" class="form-control" placeholder="Entrer votre nom" required/>
        </div>
        <div class="field">
            <label for="number">Téléphone</label>
            <input type="tel" name="number" id="number" class="form-control" placeholder="06 ..."/>
        </div>
        <div class="field">
            <label for="email">Email</label>
            <input type="email" name="email" id="email" class="form-control" placeholder="Entrer votre adresse mail" required />
        </div>
        <div class="field">
            <label for="dropdown">Quel est le sujet de votre message ?</label>
            <select name="dropdown" id="dropdown" class="dropmenu" required>
                <option value="" disabled selected>Select the subject</option>
                <option value="Deamande d'information">Demande d'informations</option>
                <option value="Signaler un problème">Signaler un problème</option>
                <option value="Remerciement">Remerciement</option>
                <option value="Réclamation">Réclamation</option>
                <option value="Autre">Autre</option>
            </select>
        </div>
        <div class="field">
            <label for="message" class="label-block">Ecrivez votre message ici :</label>
            <textarea name="message" id="message" rows="5" placeholder="Enter your comment here..."></textarea>
        </div>
        <button type="submit" value="submit" id="submit">
            Envoyer
        </button>
    </fieldset>
  </form>
```

Avec le CSS, cela donne ce rendu :
![Vu Formulaire](./img/04.png)

##### [Return to Top](#réalisation-et-sécurisation-des-formulaires-en-php)
# **Récupération des données avec PHP**


Il y a deux attributs très importants à connaitre pour la balise `<form>` :
- La méthode : method
- La cible : action


Il y a deux méthodes pour envoyer les données des formulaires :
- get : les données vont transiter par l'URL. On pourra les récupérer grâce au tableau (array) : $_GET. Cette méthode est peu utilisée car on ne peut pas envoyer beaucoup d'informations dans l'URL (256 caractères maximum).
- post : les données ne transiteront pas par l'URL, l'utilisateur ne les verra donc pas dans la barre d'adresse. Cette méthode permet d'envoyer autant de données que l'on veut, ce qui fait qu'on la privilégie le plus souvent. Mais les données ne sont pas plus sécurisées qu'avec la méthode GET et il faudra toujours vérifier si tous les paramètres sont bien présents et valides comme vu précédemment. **On ne doit pas ni faire confiance aux formulaires ni aux URL**.


La bonne pratique est donc de privilégier la méthode post pour les formulaires.


Pour récupérer les données en PHP il faut :
* Indiquer une `method` au formulaire. Il vaut mieux privilégier la méthode `POST`.
* Indiquer éventuellement une `action` si on souhaite rediriger l'utilisateur et les données du formulaire vers une autre page. Ici `action=thanks.php`.

* ## Method GET

Avec la méhode GET, les données sont envoyés via l'URL.

    http://www.monsite.com/contact.php?nom=Dupont&prenom=Jean

Le "?" sépare me nom de la page des paramètres qui se trouvent sous la forme nom=valeur et sont séparés par "&".

La seule limite est que l'URL ne doit pas dépasser 256 caractères.

Pour envoyer des paramètres on peut donc le faire via :
* un lien : utile pour naviguer de page en page dans notre site internet

``` html
<a href="bonjour.php?nom=Dupont&amp;prenom=Jean">Dis-moi bonjour !</a>
```

* un formulaire avec la méthode GET

``` html
<form action="submit_contact.php" method="GET">
    <div>
        <label for="email">Email</label>
        <input type="email" name="email">
    </div>
    <div>
        <label for="message">Votre message</label>
        <textarea placeholder="Exprimez vous" name="message"></textarea>
    </div>
    <button type="submit">Envoyer</button>
</form>
```

Si l'utilisateur complète le formulaire avec utilisateur@example.com et comme message "Bonjour", le formulaire va alors être converti en lien vers :

    submit_contact.php?email=utilisateur%40exemple.com&message=Bonjour

On va récupérer les informations par PHP dans le fichier `submit_contact.php`.

Lors de la soumission, une variable superglobale appelée `$_GET` va contenir les données envoyées. Il s'agit d'un tableau associatif dont les clés et valeurs correspondent aux paramètres envoyés dans l'URL après le '?'. Les clés avant le signe '=', les valeurs après.

``` php
$_GET['email'] = utilisateur@exemple.com;
$_GET['message'] = Bonjour;
``` 
On peut donc récupérer les informations, les traiter, les afficher :

``` html
<h1>Message bien reçu !</h1>
<div class="card">
    <div class="card-body">
        <h5 class="card-title">Rappel de vos informations</h5>
        <p class="card-text"><b>Email</b> : <?php echo $_GET['email']; ?></p>
        <p class="card-text"><b>Message</b> : <?php echo $_GET['textarea']; ?></p>
    </div>
</div>
```


* ## Method POST

Avec cette méthode, les données seront alors stockées dans la varibale `$_POST`. Cette variable est un tableau associatif qui a pour clés les valeurs des attributs `name` de chaque champ du formulaire et pour valeurs, ce que l'utilisateur a saisi. Les infos ne sont pas directement visible dans l'URL mais l'utilisateur peut quand même les modifier.

On peut donc les inclures dans une page :

``` php
    <main>
        <h1>Résumé de votre demande :</h1>
        <p>
            Merci <?php echo $_POST['name'] . ' ' . $_POST['last-name']?> de nous contacter à propos de : <?php echo $_POST['dropdown'] ?>
        </p>
        <p>
            Un de nos conseiller vous contactera soit à l'adresse <?php echo $_POST['email'] ?> ou par téléphone au 
            <?php echo $_POST['number'] ?> dans les plus brefs délais pour traiter votre demande :
        </p>
        <p>
            Message : <br>
            <?php echo $_POST['message'] ?>
        </p>
    </main>
```

Avec le CSS, cela donne ce rendu :
![Vu Réponse](./img/05.png)


##### [Return to Top](#réalisation-et-sécurisation-des-formulaires-en-php)
# **Sécurisation côté utilisateur**



**Il ne faut jamais faire confiance à l'utilsateur !**

Pour cela on peut d'abord mettre quelques barrières grâce au HTML :
* L'attribut `required` pour obliger l'utilisateur à saisir les champs
* Utiliser l'attribut `type` pour obliger l'utilisateur à entrer un chiffre, une adresse mail
* Utiliser les attributs `min`, `max`, `minlength`, `maxlength`, `pattern`, `step`

Cependant tout ces moyens de contrôles sont surtout à but UX puisqu'un utilisateur mal intentionné peut modifier le code HTML avant d'envoyer le formulaire.

Il faut donc **impérativement** mettre en place des vérifications côté serveur qui reprendront les *sécurités* mises en place du côté front.


##### [Return to Top](#réalisation-et-sécurisation-des-formulaires-en-php)
# **Sécurisation côté serveur**

**Il ne faut jamais faire confiance à l'utilsateur !**


- Contrôler la présence d'un paramètre avec `isset()`

Que ce soit avec la méthode GET ou la méthode POST, l'utilisateur peut modifier la valeur des champs et des données associées. Il faut donc vérifier que les champs attendus existent bien.

- Contrôler la valeur d'un paramètre

    - Vérifier qu'une donnée est valide avec la fonction `filter_var()`
    - Vérifier que l'entrée ne soit pas vide avec la fonction `empty()`
    - La fonction `trim()` permet d'enlever les espaces de part et d'autres des données saisies par l'utilisateur.

Pour un formulaire qui demande une adresse mail et un message cela donnerait :

``` php
<?php
if (
    (!isset($_GET['email']) || !filter_var($_GET['email'], FILTER_VALIDATE_EMAIL))
    || (!isset($_GET['message']) || empty($_GET['message']))
)
{
    echo('Il faut un email et un message valides pour soumettre le formulaire.');
    return;
}
```
Cela fait beaucoup de conditions mais c'est nécessaire, on doit toujours faire attention et prévoir tous les cas, même les plus tordus.

Avec la méthode `POST`, les informations ne transitent pas dans la barre d'adresse et on remplace les `GET` par des `POST` pour récupérer les informations. Mais un utilisateur mal intentionné peut toujours envoyer les valeurs qu'il veut par cette méthode.


* ## Les champs cachés

C'est un code dans le formulaire qui n'apparaîtra pas aux yeux du visiteurs mais qui va quand même créer une variable avec une valeur. On peut s'en servir pour transmettre des informations fixes.  
Imaginions que l'on veuille "retenir" le pseudo du visiteur on peut alors rajouter le code suivant dans la page :

``` html
<input type="hidden" name="pseudo" value="Mateo21" />
```

Sur la page web, on ne verra rien mais une variable $_POST['pseudo'] sera créée et elle aura la valeur "Mateo21". C'est apparemment inutile mais on en aura parfois besoin.
Ces champs ne sont pas réellement cachés. N'importe quel visiteur peut afficher le code source de la page pour voir et modifier les champs cachés en lisant le code HTML.

* ## Les failles XSS

Tout comme les paramètres qui transitent par l'URL, il ne faut jamais faire confiance aux données reçues. Il faut faire attention au code HTML que l'on reçoit.  
La faille XSS (pour cross-site scripting) est vieille comme le web ! Et on la trouve encore sur de nombreux site web, même professionnels. C'est une technique qui consiste à injecter du code HTML contenant du JavaScript dans vos pages pour le faire exécuter à vos visiteurs.  
On reprend le formulaire précédent qui envoie un message et un email :

``` html
<h5>Rappel de vos informations</h5>
<p><b>Email</b> : <?php echo $_POST['email']; ?></p>
<p><b>Message</b> : <?php echo $_POST['message']; ?></p>
```
Si le visiteur décide d'écrire du code HTML dans la zone de message cela fonctionnera très bien. Imaginons qu'il écrive cela dans le corps de son message : `<strong>Badaboom</strong>,` le code source HTML qui sera généré par PHP sera :


``` html
<p><b>Message</b> : <strong>Badaboum</strong></p>
```

Outre le fait que l'utilisateur peut insérer n'importe quel code HTML et rendre la page invalide (ce qui n'est pas le plus grave), il peut aussi ouvrir des balises de type `<script>` pour faire exécuter du code JavaScript au visiteur qui
visualisera la page :

``` html
<p><b>Message</b> : <script>alert('Badaboum')</script></p>
```
Tous les visiteurs qui arriveront sur cette page verront une boîte de dialogue JavaScript s'afficher. Ce qui est plutôt gênant. Il faut donc sécuriser notre code en bloquant l'exécution de code JavaScript.

* Pour ignorer le code HTML, il suffit d'utiliser la fonction `htmlspecialchars()` ou `htmlentities()`. On dira dans ce cas qu'on "échappe" le code HTML, c’est-à-dire que la fonction JavaScript alert() n'en tiendra pas compte. Elle va transformer les chevrons des balises HTML < et > en $lt; et $gt; respectivement. Cela provoquera l'affichage de la balise plutôt que son exécution.


``` html
<p><b>Message</b> : <?php echo htmlspecialchars($_POST['message']); ?></p>
```
Le code HTML qui en résultera sera propre et protégé car les balises HTML insérées par le visiteur auront été échappées.

``` html
<p><b>Message</b> : &lt;strong&gt;Badaboum&lt;/strong&gt; ?></p>
```
Tout ce qui est affiché et qui vient, à la base, d'un visiteur, doit être protégé avec `htmlspecialchars()`. Si on préfère retirer les balises HTML que le visiteur a tenté d'envoyer plutôt que les afficher, on peut utiliser la fonction `strip_tags()`.

* ## Bilan

Les fonctions à connaître pour protéger les données saisies par l'utilisateur :
* `filter_var()` associé à des multiples filtres (string, email, int etc...) Exemple :
    - Pour un email : `filter_var($_POST['email'], FILTER_VALIDATE_EMAIL)`
    - Pour un int : `filter_var($int, FILTER_VALIDATE_INT, ["options" => ["min_range" => 0]])`
* `empty()` : vérifie si l'argument est vide
* `trim()` : nettoie les espaces en début et fin de chaine
* `isset()` : verifie si la variable passée en argument est définie
* `htmlspecialchars()` : nettoie les balises html
* `htmlentities()` : nettoie les balises html
* `strlen()` : compte la longueur d'une chaîne.
* `stripslashes()` : supprime les antislashes d'une chaîne de caractères
* `is_numeric()` : vérifie si la variable passée en argument est numérique


### Exemple en GET + requête PDO statique et dynamique

La variable `$_GET` doit juste être une lettre. Elle est créée par un lien sur la page web :
``` php
<?php 
require_once __DIR__.'/../connec.php';
$pdo = new \PDO(DSN, USER, PASS);

define('ALPHABET', ["a","b","c","d","e","f","g","h","i","j","k","l","m","n","o","p","q","r","s","t","u","v","w","x","y","z"]);

if ($_SERVER["REQUEST_METHOD"] === 'GET') {
    if(!isset($_GET['letter']) || trim($_GET['letter']) === '' || strlen($_GET['letter'])!=1) {
        $msg = 'Oops something went wrong !';
    } else {
        $letter = strtolower(htmlentities($_GET['letter']));
    }

    if (!isset($msg) && in_array($letter, ALPHABET)) {
        $query = "SELECT * FROM bribe WHERE name LIKE :letter ORDER BY name ASC";
        $statement = $pdo->prepare($query);
        $statement->bindValue(':letter', $letter.'%', \PDO::PARAM_STR);
        $statement->execute();
        $bribes = $statement->fetchAll(PDO::FETCH_ASSOC);
        $choice = strtoupper($letter);
    } else {
        $query = "SELECT * FROM bribe ORDER BY name ASC LIMIT 10";
        $statement = $pdo->query($query);
        $bribes = $statement->fetchAll(PDO::FETCH_ASSOC);
        $choice = 'All';
    }
} 

require_once './controlForm.php';

?>
```

### Exemple en POST + requête PDO dynamique

La variable `$_POST` vient d'un formulaire où on attend le nom d'une personne ainsi qu'une somme d'argent :

``` php
<?php 
require_once __DIR__.'/../connec.php';
$pdo = new \PDO(DSN, USER, PASS);
$errors = [];
if($_SERVER['REQUEST_METHOD'] === 'POST') {

    $bribe = array_map('trim', $_POST);
    $bribe = array_map('htmlentities', $bribe);

    $payment = filter_var($bribe['payment'], FILTER_VALIDATE_INT, ["options" => ["min_range" => 0]]);
    if (false === $payment || null === $payment) {
        $errors[] = "Payment is mandatory and must be positive";
    }

    if(!isset($bribe['name']) || strlen($bribe['name'])>100 || empty($bribe['name'])>100) 
        $errors[] = "Name is mandatory ! 100 characters max !";
    
    if ($bribe['name']==='Eliott Ness')
        $errors[] = "This man is untouchable";


    if (empty($errors)) {
        $query = 'INSERT INTO bribe (name, payment) VALUES (:name, :payment)';
        $statement = $pdo->prepare($query);
        $statement->bindValue(':name', $bribe['name'], \PDO::PARAM_STR);
        $statement->bindValue(':payment', $bribe['payment'], \PDO::PARAM_INT);
        $statement->execute();
        header('Location: /book.php');
    } 
}
?>
```
On peut aussi implémenter une fonction pour automatiser cela :
``` php
function test_input($data) {
  $data = trim($data);
  $data = stripslashes($data);
  $data = htmlspecialchars($data);
  return $data;
}
```

