# Notes PHP

## Tables of contents

1. [Fonction intéressantes en PHP](#fonction-intéressante-en-php)



##### [Return to Top](#réalisation-et-sécurisation-des-formulaires-en-php)
# **Fonction intéressante en PHP**

* Appliquer une fonction à tous les membres d'un tableau : utilisation de la fonction `array_map()`. Utilise pour appliquer le même filtre à toutes les valeurs de la varibale $_POST d'un formulaire.

``` php
array_map('htmlentities', $_POST)
```
* Retourner le integer d'une variable avec `intval()`
``` php
intval($var)
```
Fonctionne de la même manière : `floatval()`

* Vérifier qu'un objet est une instance d'une classe : `instanceof`

``` php
$obj instanceof MyClass
// Return true or false
```




``` php

```