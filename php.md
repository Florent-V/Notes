# Notes PHP

## Tables of contents

1. [Les classes et les objets](#les-classes-et-les-objets)
2. [Les propriétés](#les-propriétés)
3. [Les méthodes](#les-méthodes)
4. [Constructeurs et visibilité](#constructeur-et-visibilité)
5. [Les constantes de classe](#les-constantes-de-classe)
6. [Héritage et parentalité](#héritage-et-parentalité)


##### [Return to Top](#réalisation-et-sécurisation-des-formulaires-en-php)
# **Fonction intéressante en PHP**

* Appliquer une fonction à tous les membres d'un tableau : utilisation de la fonction `array_map()`. Utilise pour appliquer le même filtre à toutes les valeurs de la varibale $_POST d'un formulaire.

``` php
array_map('htmlentities', $_POST)
```
* Retourner le integer d'une variable :
``` php
intval($var)
```


``` php

```