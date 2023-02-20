# Algo Condingame && Codewars

## Tables of contents

1. [Main Title](#main-title)



##### [Return to Top](#notes)
# **Températures**

Écrivez un programme qui affiche la température la plus proche de 0 parmi les données d'entrée. Si deux nombres sont aussi proches de zéro, alors l'entier positif sera considéré comme étant le plus proche de zéro (par exemple, si les températures sont -5 et 5, alors afficher 5).

Affichez 0 (zéro) si aucune température n'est fournie. Sinon, affichez la température la plus proche de 0.

`inputs` est une tableau de température.

``` js
let rep;
if (inputs.lenght === 0 || inputs[0] === "") {
    rep = 0 ;
} else {
    rep = inputs.reduce((a,b) => {
        if (Math.abs(b) < Math.abs(a)) {
            return b;
        } else if (Math.abs(b) === Math.abs(a) && b > a) {
            return b;
        } else {
            return a;
        }
    })
} 
console.log(rep);
```
# **Lettres et mots**

Etant donné une liste de mot et une string de lettre, retourner le tableau de mots qui contiennent les lettres de la string

``` js
const words = ['chevre', 'mais', 'a', 'rondin', 'ecran'];
const letters = 'and';

function exercice(words, letters) {
  let rep = [];
  for (let letter of letters) {
    for (let word of words) {
      if (word.includes(letter) && !rep.includes(word)) {
        rep.push(word);
      }
    }
  }
  return rep
}

console.log(exercice(words, letters))

```


* ## Subtitle

``` php
<?php

```