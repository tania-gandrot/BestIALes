# Experiments

## Expérience 001 - Organisme aléatoire

Objectif :
Créer un organisme capable de survivre dans un environnement contenant de la nourriture.

Description :
L'organisme se déplace aléatoirement.
Chaque déplacement consomme de l'énergie.
Lorsqu'il rencontre une ressource, il récupère de l'énergie.

Résultat :
✓ Organisme fonctionnel
✓ Consommation d'énergie
✓ Consommation de nourriture
✓ Mort lorsque l'énergie atteint zéro

Observations :
La survie dépend uniquement du hasard des déplacements.

Questions suivantes :
- Ajouter une perception ?
- Ajouter une direction ?
- Ajouter un comportement orienté ?

## Expérience 002 - Augmentation des ressources

Hypothèse :
Une plus grande densité de nourriture augmente la probabilité de survie d'un organisme se déplaçant aléatoirement.

Modification :
Passage de 50 à 200 unités de nourriture.

Code :
for(let i=0;i<200;i++)

Résultat :
À observer.

Mesures possibles :
- Temps de survie
- Énergie moyenne
- Nombre de nourritures consommées
