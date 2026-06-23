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

## Expérience 003 - Augmentation de la mobilité

Modification :
Amplitude du déplacement aléatoire :
(Math.random()-0.5)*4
→
(Math.random()-0.5)*8

Hypothèse :
Une mobilité accrue augmente les chances de rencontrer de la nourriture.

Résultat :
À observer.

## Expérience 004 - Perception de la nourriture

Objectif :
Permettre à l'organisme d'identifier la ressource la plus proche car il échoue trop rapidement.

Modification :
Ajout de la fonction findClosestFood().

Résultat :
L'organisme dispose désormais d'une information sur son environnement.

Observation :
La perception existe mais n'influence pas encore le comportement.

Prochaine étape :
Utiliser cette information pour orienter le déplacement.

## Expérience 005 - Vision limitée

Modification :
La nourriture n'est détectée que dans un rayon de 100 pixels.

Code :
if(d > 100){
    continue;
}

Hypothèse :
Une perception locale produit un comportement plus réaliste qu'une connaissance globale de l'environnement.

Résultat :
À observer.

## Expérience 006 - Exploration hors perception

Problème observé :
L'organisme restait immobile lorsqu'aucune nourriture n'était détectée.

Correction :
Ajout d'un comportement d'exploration aléatoire lorsque la perception ne détecte aucune cible.

Résultat :
L'organisme alterne désormais entre :
- exploration ;
- poursuite d'une cible détectée.

Observation :
Le comportement paraît plus naturel et la survie augmente.
