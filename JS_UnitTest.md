# Notes Test JS

# Test & Cycle de vie du produit

## Les types de test

Voici les tests les plus courants :

- Les **tests unitaires** – ce sont souvent les premiers à être implémentés dans une base de code. On les ajoute à partir du moment où le produit a trouvé sa cible. Ils sont généralement “assez faciles” à réaliser.

- Les **tests fonctionnels** ou **d’intégration** – on les ajoute souvent soit en même temps que les tests unitaires, soit après. Ils vont être un peu plus complexes à réaliser.

- Les **tests E2E ou End 2 End** – ce sont des tests assez complexes, qui seront souvent réservés à la phase de maturité du projet.

## Stratégie de test

C’est un document “statique” ; autrement dit, il ne va pas changer durant le cycle de vie du projet. C’est un document qui va guider l’équipe, notamment dans la rédaction des plans de test.

Il est important d’y parler des éléments suivants :

- **La portée des tests** : l’idée ici est de savoir ce qu’il faut tester, et pourquoi il faut le tester.

- **L’approche des tests** : vous allez parler des types de test (unitaire, intégration, etc.), des responsabilités des différents membres de l’équipe, etc.

- **Les outils de test** : par exemple Jest pour les tests unitaires JavaScript, et NightWatch pour les tests end to end.

## Plan de test

À la différence d’une stratégie de test, un plan de test est un document dynamique ; autrement dit, c’est un document qui va être régulièrement mis à jour. L’objectif est de décrire ce qu’il faut et ce qu’il ne faut pas tester, comment et quand tester, et enfin qui fera le test. C’est généralement un document qui est écrit par un QA Engineer.


## Résumé

Si la stratégie de test est le document qui donne les grandes lignes (vision globale), le cas de test est le document que vous allez réaliser pour vérifier qu’une fonctionnalité répond bien aux attentes (vision spécifique). Grâce à ce document, l’ingénieur de test va pouvoir comparer les résultats attendus aux résultats réels.

- Un produit passe par différentes phases au cours de sa vie : l’idée, le développement, le lancement, la croissance, la maturité et le déclin.

- Les tests à intégrer dépendent du cycle de vie du projet. Plus celui-ci est avancé, autrement dit plus il approche de la maturité, plus il va y avoir de tests automatisés dessus.

- On peut intégrer un grand nombre de tests à un produit : tests unitaires, fonctionnels ou d’intégration, E2E, SmokeTest, etc.

- Le plan de test est une vision de ce que vous voulez réaliser comme tests, alors que la stratégie de test correspond à un plan d’action conçu pour réaliser cette vision.

# Les test unitaires en JavaScript

## La méthodologie des tests unitaires

- Le test unitaire permet de tester une partie spécifique de votre application (généralement une fonction). Il permet d’éviter les effets de bord : pour un paramètre donné, le résultat sera toujours le même.

- Les tests permettent à la fois de fiabiliser les applications et de décomplexifier la base de code. Une fonction difficilement testable est souvent une fonction qui doit être refactorisée pour pouvoir être mieux testée.

- Essayez toujours de commencer par réaliser des tests sur les parties les plus complexes et les plus critiques de votre application. Ce sont ces dernières qui auront souvent le plus de chance de casser.

- Attention au “Et si” lors de la phase de rédaction de votre test. Il est important que vous sachiez à quoi vous intéresser lors de la rédaction de votre test.

