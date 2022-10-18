# Notes Name space

## Tables of contents

1. [Les Namespace](#les-namespaces)


En programmation orientée objet, il arrive que différentes classes, fonctions ou constantes portent le même nom (d'une bibliothèque à une autre par exemple). Afin d'éviter tout conflit, PHP met à disposition des espaces de noms: les namespaces.


##### [Return to Top](#notes-name-space)
# **Les namespaces** 

L'intérêt des namespaces est de permettre à une application de pouvoir utiliser des classes aux noms identiques dans un même projet.

Une arborescence de fichiers definit une structure **physique** de répertoires.

Un namespace définie plutôt une structure **logique** de répertoires.


Prenons l'exemple d'un projet d'application Web : Une plateforme dans l'événementiel.
Cette application comporterait deux classes aux noms identiques !
1. Une classe Event (qui comporterait toutes les données métier d'un événement). Cette classe pourrait se trouver dans ce chemin physique : `src/Entity/Event`

2. Une autre classe Event (qui gèrerait les événements techniques d'un utilisateur, comme par exemple, l'insertion d'une donnée en base). Cette classe pourrait se trouver dans ce chemin physique : `src/Events/Event`

Maintenant, imaginons que l'on ait besoin d'utiliser ces deux classes dans un même fichier.

``` php
<?php
require 'src/Entity/Event.php';
require 'src/Events/Event.php';

$event = new Event();
```

On obtiendrait donc une erreur :

    PHP Fatal error: Cannot declare class Event, because the name is already in use

Les espaces de noms vont pouvoir régler ce problème. On va donc ajouter des namespaces dans nos deux classes :

``` php
<?php
namespace Entity;

class Event
{
    // (...) Code métier pour un événement
}
```

``` php
<?php
namespace Events;

class Event
{
    // (...) Code pour un événement technique de l'utilisteur
}
```

L'effet de l'ajout de namespace sera de créer pour chacune de ces classes un FQCN (Fully Qualified Class Name) construit comme ceci :

* `Entity\Even`t Pour la classe `src/Entity/Event.php`
* `Events\Event` Pour la classe `src/Events/Event.php`

Maintenant, il sera ainsi possible d'instancier ces deux classes dans un même fichier, de cette façon :

``` php
<?php
//index.php
require 'src/Entity/Event.php';
require 'src/Events/Event.php';

$event = new Entity\Event();
$event = new Events\Event();
```

    Cette fois, aucune erreur et nous avons bien deux instances différentes

Dans l'usage, nous utiliserons plutôt le mot clé `use` en début de fichier plutôt que d'appeler les classes par leur FQCN à chaque instanciation.  
Dans le cas de cet exemple, comme nous avons deux classes ayant le même nom, nous devrons donner un alias à l'une d'entre elles afin de les distinguer :

``` php
<?php
//index.php
require 'src/Entity/Event.php';
require 'src/Events/Event.php';
use Entity\Event;
use Events\Event as TechnicalEvent;
$event = new Event();
$technicalEvent = new TechnicalEvent();
```

Ceci te permettra d'aborder sereinement le principe d'autoload (chargement automatique des classes) !

##### [Return to Top](#notes-name-space)