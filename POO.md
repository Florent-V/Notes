# Notes POO

## Tables of contents

1. [Les classes et les objets](#les-classes-et-les-objets)
2. [Les propriétés](#les-propriétés)
3. [Les méthodes](#les-méthodes)
4. [Constructeurs et visibilité](#constructeur-et-visibilité)

# **Les classes et les objets**


* ## Les classes

La classe permet de définir/modéliser le concept à manipuler. Cette modélisation est la plus importante, il faut donc décider ce dont on aura besoin pour définir correctement le concept :

``` php
<?php
// src/Animal.php
class Animal
{
    public string $name;
    
// size expressed in whatever unit    
    
    public int $pawNumber;
    
    public bool $isCarnivorous;
}
```
La classe doit être définie dans son propre fichier, et le fihcier doit avoir exactement le même nom que la classe.  
Une classe doit être nommé en PascalCase.

* ## Les objets

A partir de cette classe animal, que l'on peut comparer à un moule, il est possible de créer des animaux différents. C'est ce qu'on appelle les **objets** ou **instance d'une classe.**

``` php
<?php
// public/index.php

require __DIR__ . '/../src/Animal.php';

$animal1 = new Animal();
$animal2 = new Animal();
```
On doit d'abord *require* la classe que l'on veut utiliser.  
Puis on utilise le mot clé `new` pour instancier l'objet. On peut créer autant d'objet à partir d'une même classe, ils auront chacun les mêmes propriétés mais avec des valeurs différentes. Ces **objets** issus de la même classe s'appellent des **instances**. 

``` sh
object(Animal)[1]
  public string 'name' => *uninitialized*
  public float 'size' => *uninitialized*
  public int 'pawNumber' => *uninitialized*
  public int 'isCarnivorous' => *uninitialized*

object(Animal)[2]
  public string 'name' => *uninitialized*
  public float 'size' => *uninitialized*
  public int 'pawNumber' => *uninitialized*
  public int 'isCarnivorous' => *uninitialized*
```

# **Les propriétés**

Reprenons la classe `Animal` :
``` php
<?php
class Animal
{
    public string $name;
    public float $size;
    public bool $carnivorous;
    public int $pawNumber;
}
```
Dans cette classe, le nom, la taille, le régime alimentaire, le nombre de pattes sont les **propriétés** auxquelles il va être possible d'affecter des **valeurs**.

Il ne faut pas oublier de typer ces propriétés.

Le mot `public` indique que l'on peut accéder aux variables depuis l'extérieur. Ce concept sera vu en détail plus tard.

* ## Affecter une valeur par défaut
Pour affecter une valeur par défaut, il faut le faire dès sa définition. Cela peut être intéressant mais pas toujours. Donner un `$name` par défaut n'a pas grand intérêt.
``` php
<?php
class Animal
{
    public string $name;
    public float $size = 100;
    public bool $carnivorous = false;
    public int $pawNumber;
}
```
* ## Affecter une valeur dépuis l'extérieur de la classe

Pour modifier les propriétés depuis l'extérieur de la classe, on utilise la syntaxe suivante :
``` php
<?php
$lion->name = 'lion';
$lion->pawNumber = 4;
$lion->carnivorous = true;
```
Pour récupérer la valeur d'une propriété, on utilise la même syntaxe :
``` php
echo 'Bonjour je suis un ' . $lion->name . ' et j\'ai ' . $lion->pawNumber . ' patte(s)';
```

# **Les méthodes**

* ## Définir une méthode

En plus de propriétés, une classe est dotée de fonction que l'on appelle des méthodes dans le contexte objet.  
Les méthodes s'écrivent exactement comme des fonctions, avec un nom, des paramètres obligatoires et optionnels, des accolades contenant le corps de la fonction. Les paramètres etla valeur de sortie seront typés.

Premier exemple :
``` php
<?php
class Animal
{
    public string $name;
    public float $size = 100;
    public bool $carnivorous = false;
    public int $pawNumber;
    public string $threatenedLevel = 'NE';

    public function speak(): string
    {
        return 'Welcome to the zoo';
    }
}
```

* ## Utiliser une méthode
Syntaxe de base :

``` php
<?php
echo $lion->speak();
```
Elle est similaire à celle des propriétés. Les () en plus car c'est une fonction.


* ## Accéder aux propriétés avec `$this`

Une méthode permet de manipuler les propriétés d'un objet. Les portées sont limitées. On a déjà vu qu'une variable définie à l'extérieur d'une fonction n'était pas accessible à l'intérieur de celle-ci.

Dans une classe, les méthodes ont la possibilités d'accéder aux propriétés de la classe à l'aide du mot clé `$this`.

``` php
<?php
public function speak(): string
{
    return 'Welcome to the zoo, I\'am a ' . $this->name;
}
```
`$this` représente l'instance de la classe en cours d'utilisation. Si on appelle la méthode sur l'objet `$lion`, `$this` correspond donc à `$lion` et donc $name vaut 'lion' pour cet objet. De même si on fait `$parrot->speak()`, le `$this` correspondra à l'instance `$parrot` et le `$name` sera alors 'Parrot'.

* ## Les méthodes avec paramètres

Une méthode est une fonction de classe. Elle a donc le même fonctionnement et peut prendre donc des paramètres. Ceux-ci ont la même portée que pour des fonctions classiques. Il ne faut donc pas confondre ces variables "paramètres" avec les propriétés accessibles via `$this`.

``` php
public function speak(string $lang = 'fr'): string
{
    if($lang === 'fr') {
        $message = 'Bienvenue au zoo, je suis un ';
    } else {
        $message = 'Welcome to the zoo, I\'am a ';
    }
    return $message . $this->name;
}
```
Dans cette méthode, on mélange un paramètre externe `$lang` (qui n'est pas une propriété de l'aimal et n'est accessible que dans cette méthode) avec `$name` qui est une propriété et s'appelle donc via la syntaxe `$this->name`.

``` php
<?php
echo $lion->speak('fr');
echo $lion->speak('en');
echo $lion->speak();
```
Sur le 1er appel, on demande au lion de parler français
Sur le second, on demande de parler anglais
Sur le 3e on n'indique pas d'argument, la valeur par défaut "fr" va donc s'appliquer et le texte sera de nouveau en français.

Une autre méthode :
``` php
<?php
public function isDangerous(): bool
{
    return ($this->size > 50 && $this->carnivorous);
}
```
# **Constructeur et visibilité**

* ## Constructeur
Avec les syntaxes précédentes, toutes les propriétés ne sont pas définies à la création de l'objet et donc si on fait cela :
``` php
<?php
// $lion->name = 'lion';
var_dump($lion);
echo $lion->name;
```
On aura donc ici une Fatal Error car le `$name` du lion n'est pas définie.

Si on regarde le résultat du `var_dump()`, on voit que la propriété `$name` est `uninitialized`. Or il est impossible d'afficher une propriété non initialisée.

Il faudra donc s'assurer que le développeur utilisant la classe soit forcée de définir un nom au moment de l'intanciation.

La solution c'est le constructeur ! C'est une méthode particulière qui, si elle est définie, impose d'utiliser un certain nombre de paramètre au moment de l'instanciation de l'objet, c'est à dire au moment d'utiliser le mot clé `new`.

En PHP, le constructeur s'écrit `__construct()` avec DEUX underscores. C'est une "méthode magique", il y en a d'autres en PHP mais celle-ci est la plus utilisée. Voici le code correspondant :

``` php
<?php
public string $name;
public function __construct(string $name)
{
    $this->name = $name;
}
```
Un constructeur ne renvoie rien, on ne doit donc pas y mettre de return.

Maintenant à l'instanciation on doit mettre le paramètre `$name`.
``` php
<?php
$lion = new Animal('lion');
```
* ## Visibilité : public ou private ?

Depuis le début, on utilise le mot clé `public` devant toutes les propriétés et les méthodes. C'est ce qu'on appelle la visibilité. Il en existe 3 niveaux :

        - public
        - protected
        - private

Ils permettent de définir si une propriété ou une méthode est accessible depuis l'extérieur de la classe ou non. Si le mot clé `public` est utilisé, la propritété/méthode sera utilisable partout, si elle est définie sur `private`, la propriété/méthode ne sera accessible que depuis la classe elle-même.

Exemple si on change la visibilité de la propriété `$size`
``` php
<?php
private float $size;
```
On obtient :
``` sh
php Fatal error: Uncaught Error: Cannot access private property Animal::$size in ...`.
```

* ## Les Getters & Setters









``` php
<?php

```