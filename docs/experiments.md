# Carnet d'expériences — BestIAle

Ce document retrace les expériences menées dans BestIAle.

Son objectif est de conserver une trace des hypothèses, des observations et des enseignements issus de chaque expérimentation.

Le code appartient au dépôt GitHub.

Ce carnet documente la démarche d'exploration.

---

# Campagne 1 — Acquisition des ressources

## Question de recherche

**Comment un agent autonome acquiert-il les ressources nécessaires à sa survie dans un environnement plus ou moins contraint ?**

---

## Expérience 1.1 — Déplacement aléatoire

### Objectif

Créer un organisme capable de survivre dans un environnement contenant de la nourriture.

### Hypothèse

Même sans perception, un agent peut survivre grâce à des déplacements aléatoires si les ressources sont suffisamment nombreuses.

### Modification

Création d'un agent :

* déplacement aléatoire ;
* consommation d'énergie à chaque déplacement ;
* récupération d'énergie lorsqu'une ressource est rencontrée ;
* mort lorsque l'énergie atteint zéro.

### Observations

* L'agent fonctionne correctement.
* La survie dépend uniquement du hasard.
* Les performances sont très variables selon les rencontres avec les ressources.

### Enseignement

Le hasard peut suffire dans un environnement favorable, mais il ne constitue pas une stratégie robuste lorsque les ressources deviennent plus rares.

### Décision

➡️ Explorer l'influence de la quantité de nourriture disponible.

---

## Expérience 1.2 — Densité des ressources

### Hypothèse

Une plus grande densité de nourriture augmente les chances de survie d'un agent se déplaçant au hasard.

### Modification

Augmentation du nombre de ressources disponibles.

### État

⏳ À observer.

### Mesures envisagées

* temps de survie ;
* énergie moyenne ;
* nombre de ressources consommées.

### Décision

En attente des observations.

---

## Expérience 1.3 — Mobilité

### Hypothèse

Une plus grande mobilité augmente les chances de rencontrer une ressource.

### Modification

Augmentation de l'amplitude des déplacements aléatoires.

### État

⏳ À observer.

### Mesures envisagées

* distance parcourue ;
* consommation énergétique ;
* temps de survie.

### Décision

En attente des observations.

---

## Expérience 1.4 — Perception

### Objectif

Permettre à l'agent de détecter les ressources situées dans son environnement.

### Hypothèse

La perception constitue une information utile, mais ne modifie pas le comportement tant qu'elle n'est pas exploitée.

### Modification

Ajout d'une perception des ressources proches.

### Observations

* L'agent dispose désormais d'informations sur son environnement.
* Son comportement reste inchangé.

### Enseignement

Percevoir n'est pas agir.

Une information n'a de valeur que si elle influence la prise de décision.

### Décision

➡️ Utiliser cette information pour orienter les déplacements.

---

## Expérience 1.5 — Perception locale

### Hypothèse

Une perception limitée produit des comportements plus réalistes qu'une connaissance parfaite de l'environnement.

### Modification

Restriction de la portée de perception.

### État

⏳ À observer.

### Mesures envisagées

* taux de survie ;
* distance parcourue ;
* fréquence de détection des ressources.

### Décision

En attente des observations.

---

## Expérience 1.6 — Exploration

### Problème observé

Lorsque l'agent ne détectait aucune ressource, il cessait de se déplacer.

### Hypothèse

L'alternance entre exploration et poursuite constitue une stratégie plus efficace que l'immobilité.

### Modification

Ajout d'un comportement d'exploration lorsqu'aucune ressource n'est détectée.

### Observations

* L'agent alterne entre exploration et poursuite.
* Le comportement paraît plus naturel.
* La durée de survie augmente.

### Enseignement

Un agent autonome doit disposer d'une stratégie en absence d'information.

L'exploration constitue un comportement à part entière.

### Décision

✅ Hypothèse confirmée.

---

## Expérience 1.7 — Rareté des ressources

### Hypothèse

L'agent devrait conserver un avantage grâce à sa perception malgré une diminution des ressources disponibles.

### Modification

Réduction de la quantité de nourriture.

### État

⏳ À observer.

### Questions ouvertes

* Existe-t-il un seuil critique de ressources ?
* À partir de quelle densité l'agent ne peut-il plus compenser son coût énergétique ?
* Les bénéfices de la perception diminuent-ils lorsque les ressources deviennent très rares ?

### Décision

En attente des observations.

---

# Connaissances acquises

À ce stade, plusieurs enseignements commencent à émerger :

* Un comportement aléatoire peut suffire dans un environnement favorable.
* La perception seule n'améliore pas le comportement.
* Une information doit être exploitée pour devenir utile.
* L'exploration est un comportement essentiel lorsque l'environnement est incertain.
* Les contraintes de l'environnement jouent un rôle aussi important que les capacités de l'agent.

Ces résultats guideront les expériences suivantes de la campagne **Acquisition des ressources**.
