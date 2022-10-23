# Notes PHP

## Tables of contents

1. [Fonction intéressantes en PHP](#fonction-intéressante-en-php)



##### [Return to Top](#réalisation-et-sécurisation-des-formulaires-en-php)
# **Fonction intéressante en PHP**

* ## array_map()
Appliquer une fonction à tous les membres d'un tableau : utilisation de la fonction `array_map()`. Utilise pour appliquer le même filtre à toutes les valeurs de la varibale $_POST d'un formulaire.

``` php
array_map('htmlentities', $_POST)
```
* ## intval()
Retourner le integer d'une variable avec `intval()`
``` php
intval($var)
```
Fonctionne de la même manière : `floatval()`

* ## instanceof
Vérifier qu'un objet est une instance d'une classe : `instanceof`

``` php
$obj instanceof MyClass
// Return true or false
```
* ## Différence entre `isset()` vs `empty()` vs `is_null()`

    * `isset()` : Détermine sur une variable est définie et non nulle. La fonction retourne `true` seulement si la varibale est **définie** et **non nulle.**
    * `empty()` : Détermine si une variable est vide. Elle retourne `true` si la variable est une **string vide**, **false**, tableau vide (**array()**), **NULL**, **0** (string ou integer) et une varibale non définie (**unset**).
    * `is_null()` : La fonction retourne `true` seulement si la varibale vaut **null**. `is_null()` est l'opposé de `isset()` sauf que `isset()` peut être appliquée à des **varibales inconnue** alors que `is_null()` ne peut être appliquée qu'à des **variables déclarée**.


* ## Opérateur ternaire ?:

Exemple savoir si un nombre est pair :
``` php
if ($nb%2 === 0) {
    return "Even Number";
} else {
    reurn "Odd Number;
}
```
Peut s'écrire en une seule ligne
``` php
return ($nb%2 === 0) ? "Even Number" : "Odd Number";
```
L'opérateur ternaire `?:` est une porte qui laisse passer tout ce qui est faux y compris NULL : 0, empty string, NULL, false, !isset(), empty().

L'opérateur ?: permet donc de vérifier empty(), !isset(), is_null() et permet donc de raccourcir certaines écriture comme :

``` php
!empty($x) ? $x : $y;
// Equivaut à
$x ?: $y
```
``` php
if(!$x) { 
    echo $x; 
} else { 
    echo $y; 
}
// Equivaut à
echo $x ?: $y
```

* ## Opérateur coalescent : ??

``` php 
$defaultNumber = 25;
$userNumber;
if (isset($userNumber)) {
    echo $userNumber;
}else {
    echo $defaultNumber;
}
// Output => 25
```
Peut s'écrire plus simplement :
``` php 
$defaultNumber = 25;
 // Null Values and value is not set
$userNumber;
 echo $userNumber ?? $defaultNumber;
 // Output => 25
```
On peut également faire un chaînage :
``` php
$defaultNumber = 25;
$browserNumber;
$userNumber;
echo $userNumber ?? $browserNumber ?? $defaultNumber;
// Output => 25
```
``` php
$defaultNumber = 25;
$browserNumber = 20;
$userNumber;
echo $userNumber ?? $browserNumber ?? $defaultNumber;
// Output => 20
```
On peut en utiliser plusieurs sur une même ligne mais il faut mettre des parenthèses :
``` php
$firstName = "John";
$lastName = "Doe";
echo ($firstName ?? "Unknown") . " " . ($lastName ?? "");
```
Sans parenthèse on obtiendrait uniquement `John`.

**Exemple :**
``` php
var_export (false ?? 'value2');   // false
var_export (true  ?? 'value2');   // true
var_export (null  ?? 'value2');   // value2
var_export (''    ?? 'value2');   // ""
var_export (0     ?? 'value2');   // 0
 
var_export (false ?: 'value2');   // value2
var_export (true  ?: 'value2');   // true
var_export (null  ?: 'value2');   // value2
var_export (''    ?: 'value2');   // value2
var_export (0     ?: 'value2');   // value2
```
``` php

```

