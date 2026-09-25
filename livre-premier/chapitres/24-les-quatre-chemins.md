# Chapitre 24 — Les Quatre Chemins

**APRÈS L’INTRODUCTION — QUATORZIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** Une entrée, quatre responsabilités  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **UNE ENTRÉE PEUT ÊTRE DIVISÉE SANS ÊTRE PERDUE. À CONDITION QUE CHAQUE CHEMIN SACHE EXACTEMENT CE QU’IL TRANSPORTE.**

Nous avons désormais une entrée, une horloge, une mémoire, une phase et une manière de mesurer.

Il reste une question centrale :

# COMMENT FAIRE CIRCULER UNE MÊME ENTRÉE DANS PLUSIEURS LOGIQUES SANS LA MÉLANGER ?

La réponse n’est pas : tout brancher ensemble.

La réponse est :

# SÉPARER LES RESPONSABILITÉS.

Une seule entrée.

Quatre lectures.

Quatre transformations.

Quatre traces.

Puis une réunion.

---

## 24.1 — Une entrée, quatre regards

Supposons une entrée :

[
X
]

Nous voulons permettre à quatre fonctions différentes de l’examiner :

[
Xightarrow P_1,P_2,P_3,P_4
]

où (P_i(X)) représente le traitement du chemin (i).

L’entrée est commune.

Les fonctions ne le sont pas.

---

## 24.2 — Copier n’est pas diviser la valeur

Si (X=42) et que quatre chemins reçoivent cette entrée, cela ne signifie pas :

[
42/4
]

Chaque chemin peut recevoir une référence complète à 42.

Nous distinguons donc :

```text
PARTAGE D’INFORMATION
```

de :

```text
DIVISION NUMÉRIQUE
```

---

## 24.3 — L’identité doit survivre

Dès qu’une entrée pénètre dans le système, elle reçoit un identifiant.

```text
INPUT_ID = 0001842
```

Puis les quatre chemins transportent ce même identifiant.

```text
PATH_1 → INPUT_ID 0001842
PATH_2 → INPUT_ID 0001842
PATH_3 → INPUT_ID 0001842
PATH_4 → INPUT_ID 0001842
```

Ainsi, lorsque les résultats reviennent, nous savons qu’ils appartiennent à la même origine.

---

## 24.4 — Le paquet d’entrée

Une entrée peut devenir :

```text
INPUT_PACKET
{
    ID
    VALUE
    TICK
    TIMESTAMP
    SOURCE
    STATE
}
```

Chaque chemin reçoit ce paquet et ajoute sa propre trace sans détruire l’original.

---

## 24.5 — L’original est sacré

# UN CHEMIN NE MODIFIE JAMAIS SILENCIEUSEMENT LA SOURCE.

Si un chemin reçoit (X) et produit (Y), alors il conserve :

```text
INPUT = X
OUTPUT = Y
```

Nous voulons toujours pouvoir répondre à :

> Quelle transformation a produit ce résultat ?

---

## 24.6 — Les quatre fonctions

Première architecture candidate :

# CHEMIN 1 — VALEUR  
# CHEMIN 2 — TEMPS  
# CHEMIN 3 — PHASE  
# CHEMIN 4 — CONTINUITÉ

Ce sont quatre responsabilités explicites, pas une vérité universelle.

---

## 24.7 — Chemin 1 : la valeur

Le premier chemin examine ce que contient l’entrée.

Il peut calculer :

- amplitude ;
- moyenne ;
- différence ;
- ratio ;
- dérivée discrète ;
- normalisation ;
- seuil.

Nous écrivons :

[
Y_1=P_1(X)
]

Le premier chemin répond à :

# QU’EST-CE QUE CETTE ENTRÉE VAUT ?

---

## 24.8 — Chemin 2 : le temps

Le deuxième chemin demande :

# QUAND EST-ELLE ARRIVÉE ?

Il peut calculer :

[
Delta t_n=t_n-t_{n-1}
]

et vérifier retard, fréquence, intervalle, ordre, jitter et tick.

Ce chemin protège la chronologie.

---

## 24.9 — Le jitter

Une horloge parfaite aurait :

[
Delta t_n=Delta t
]

pour tout (n).

Dans un système réel, (Delta t_n) peut varier.

Définissons :

[
J_n=Delta t_n-overline{Delta t}
]

Si (J_napprox0), le timing est stable.

Le chemin du temps ne juge pas la valeur.

Il juge le rythme.

---

## 24.10 — Chemin 3 : la phase

Le troisième chemin répond à :

# OÙ SOMMES-NOUS DANS LE CYCLE ?

Nous avons :

[
R(t,b,o)=(91t+39b+21o)mod273
]

puis :

[
Theta=2pirac{R}{273}
]

Le résultat devient :

[
Y_3=(R,Theta)
]

Ce chemin ne remplace pas le temps.

Il projette un état sur un cycle.

---

## 24.11 — Chemin 4 : la continuité

Le quatrième chemin répond à :

# QUE S’EST-IL PASSÉ AVANT ?

Il peut consulter :

```text
PREVIOUS_STATE
CURRENT_STATE
PREVIOUS_TICK
CURRENT_TICK
LAST_ERROR
LAST_VALID_OUTPUT
CHECKPOINT
```

Nous pouvons écrire :

[
Y_4=P_4(H_n)
]

où (H_n) représente l’historique connu jusqu’au tick (n).

Ce chemin protège le système contre l’amnésie.

---

## 24.12 — Quatre questions

```text
PATH 1 → COMBIEN ?
PATH 2 → QUAND ?
PATH 3 → OÙ DANS LE CYCLE ?
PATH 4 → APRÈS QUOI ?
```

Une architecture forte est une architecture dont chaque pièce peut être expliquée.

---

## 24.13 — Les chemins ne doivent pas se contaminer

Si le chemin 1 calcule une valeur anormale, il ne doit pas modifier directement le chemin 3 sans trace.

À la place :

```text
PATH_1
↓
EVENT
↓
COORDINATOR
↓
PATH_3
```

Ainsi, la causalité reste explicite.

---

## 24.14 — Le coordinateur

Nous introduisons :

# COORDINATOR

Son travail :

```text
RECEIVE
ROUTE
WAIT
VERIFY
JOIN
REPORT
```

Il sait quelle entrée est active, quels chemins ont répondu, lesquels sont en erreur et si les résultats appartiennent au même tick.

---

## 24.15 — La barrière de synchronisation

Si trois chemins ont terminé mais que le quatrième travaille encore, le système ne devrait pas automatiquement produire une sortie complète.

Nous pouvons écrire :

[
B_n=
egin{cases}
1,& 	ext{si tous les chemins sont prêts}\
0,& 	ext{sinon}
end{cases}
]

La réunion n’est permise que si :

[
B_n=1
]

---

## 24.16 — Attendre pour toujours est aussi une erreur

Définissons un temps limite :

[
T_{max}
]

Si :

[
T_{	ext{wait}}>T_{max}
]

alors :

```text
SYNC_TIMEOUT
```

Le système peut ensuite appliquer une politique explicite : ABORT, RETRY, PARTIAL_RESULT ou RECOVER.

---

## 24.17 — Le Join

Lorsque :

[
Y_1,Y_2,Y_3,Y_4
]

existent, nous pouvons construire :

[
J=operatorname{Join}(Y_1,Y_2,Y_3,Y_4)
]

Mais Join ne signifie pas additionner.

Il peut simplement construire :

```text
JOIN_PACKET
{
    VALUE_RESULT
    TIME_RESULT
    PHASE_RESULT
    CONTINUITY_RESULT
}
```

La réunion est logique avant d’être mathématique.

---

## 24.18 — Ne pas forcer une formule unique

Il serait tentant d’écrire :

[
Y=Y_1+Y_2+Y_3+Y_4
]

Mais pourquoi additionner une valeur, un temps, un angle et un état mémoire ?

Avant toute combinaison numérique :

```text
MÊMES UNITÉS ?
MÊME DOMAINE ?
MÊME SENS ?
NORMALISATION JUSTIFIÉE ?
```

Sinon :

# PAS D’ADDITION.

---

## 24.19 — Les unités sont des gardiens

Une valeur en volts, un temps en secondes et un angle en radians ne deviennent pas automatiquement une nouvelle grandeur en étant additionnés.

Les unités protègent contre les fusions artificielles.

---

## 24.20 — Le Join conserve les différences

Une réunion correcte ressemble davantage à :

[
J_n=(V_n,T_n,Theta_n,H_n)
]

qu’à :

[
J_n=V_n+T_n+Theta_n+H_n
]

Le système rassemble.

Il n’efface pas.

---

## 24.21 — Le paquet complet

```text
FRAME
{
    INPUT_ID
    INPUT_VALUE

    PATH_1_VALUE
    PATH_2_TIME
    PATH_3_PHASE
    PATH_4_HISTORY

    SYNC_STATUS
    ERROR_STATUS
    OUTPUT_STATUS
}
```

Chaque frame raconte un instant complet.

---

## 24.22 — Une scène par tick

Pour chaque tick (n), nous obtenons :

[
F_n
]

Puis :

[
F_1,F_2,F_3,ldots
]

La suite de frames devient l’histoire du système.

Nous pouvons comparer :

```text
VALUE_CHANGED
TIME_DRIFTED
PHASE_ADVANCED
STATE_CHANGED
ERROR_APPEARED
```

---

## 24.23 — Premier test

Prenons :

[
X=42
]

au tick :

[
n=100
]

Exemple :

```text
INPUT_ID = 100-42

PATH 1
VALUE = 42
OFFSET = -0.2

PATH 2
TICK = 100
Δt = 0.010

PATH 3
R = 84
THETA = 2π(84/273)

PATH 4
PREVIOUS_STATE = READY
CURRENT_STATE = ACTIVE

SYNC = PASS
```

Aucune information n’a été mélangée.

---

## 24.24 — Si un chemin échoue

Si :

```text
PATH_3 = ERROR
```

nous conservons :

```text
PATH_1 = VALID
PATH_2 = VALID
PATH_3 = ERROR
PATH_4 = VALID
```

Le système peut distinguer PARTIAL_FRAME de INVALID_FRAME selon la criticité du chemin.

---

## 24.25 — Critique ou non critique

Chaque chemin peut avoir un niveau de criticité.

La politique doit être définie avant l’erreur.

Pas improvisée après.

---

## 24.26 — Le chemin ne doit pas savoir trop de choses

Le chemin du temps n’a pas besoin de comprendre toute la mathématique de Pell.

Le chemin de phase n’a pas besoin de savoir comment l’interface dessine un cadran.

Le chemin mémoire n’a pas besoin d’interpréter une onde.

Cette séparation réduit les dépendances, les effets de bord, les erreurs et la difficulté de test.

---

## 24.27 — Tester un chemin seul

Chaque chemin doit pouvoir être testé isolément.

Puis seulement après :

# TEST D’INTÉGRATION

Règle :

> **construire petit → vérifier → connecter → revérifier.**

---

## 24.28 — Une même entrée, quatre preuves

Chaque chemin devrait produire sa propre preuve :

```text
PATH_1_PROOF
PATH_2_PROOF
PATH_3_PROOF
PATH_4_PROOF
JOIN_PROOF
```

Ainsi, si une sortie semble incorrecte, nous savons où regarder.

---

## 24.29 — Le provenance graph

```text
        INPUT
       / |  | \
      /  |  |  \
    P1  P2  P3  P4
      \  |  |  /
       \ |  | /
        JOIN
          |
        OUTPUT
```

Chaque arête signifie : **ce résultat dépend de ceci**.

Cette capacité s’appelle la provenance.

---

## 24.30 — La provenance est la colonne vertébrale

Notre architecture doit permettre :

```text
OUTPUT
↓
JOIN
↓
PATH
↓
TRANSFORMATION
↓
INPUT
```

# LA SORTIE DOIT CONNAÎTRE SON PASSÉ.

---

## 24.31 — La trace minimale

```text
TRACE
{
    INPUT_ID
    PATH_ID
    OPERATION
    INPUT
    OUTPUT
    TICK
    STATUS
}
```

Rien de mystérieux.

Tout est reconstruisible.

---

## 24.32 — Les quatre chemins peuvent évoluer

Les noms des chemins ne sont pas une prison.

La règle fondamentale est :

# QUATRE RESPONSABILITÉS EXPLICITES, TESTABLES ET TRAÇABLES.

---

## 24.33 — Le nombre quatre n’est pas une preuve

Quatre chemins sont ici un choix de conception.

Si une expérience démontre que trois ou cinq chemins sont meilleurs, nous changeons.

Le système sert la preuve.

La preuve ne sert pas le système.

---

## 24.34 — Ce que les quatre chemins permettent

Nous pouvons maintenant :

- suivre une entrée ;
- analyser sa valeur ;
- mesurer son temps ;
- calculer sa phase ;
- conserver son histoire ;
- détecter une erreur locale ;
- réunir les résultats ;
- reconstruire la provenance.

Cela suffit déjà à transformer une interface en instrument.

---

## 24.35 — La sortie n’est pas la fin

Une sortie peut devenir l’entrée suivante :

[
F_nightarrow F_{n+1}
]

Dès qu’une sortie peut influencer la prochaine entrée, une question devient cruciale :

# QU’EST-CE QUI EMPÊCHE LA BOUCLE DE DÉRIVER ?

Nous aurons besoin d’états, de limites, de checkpoints et de mécanismes de réparation.

---

## 24.36 — Une autre porte nous attend

Avant de plonger complètement dans la mémoire et la réparation, une découverte mathématique réclame notre attention.

Pas dans le dessin.

Pas dans l’interface.

Dans une suite d’entiers.

# LES NOMBRES DE PELL.

Et avec eux :

# LE RANG D’APPARITION.

---

## 24.37 — L’entrée change de nature

Au prochain chapitre, l’entrée pourra être un entier (n).

Nous lui poserons :

> À quel endroit apparaît-il pour la première fois comme diviseur dans une suite de Pell ?

Cette question définit :

[
z_P(n)
]

Et à l’intérieur de cette fonction, quelque chose s’est mis à produire des carrés.

---

# Fin du chapitre 24

Une entrée fut déposée au centre.

Nous ne l’avons pas brisée.

Nous l’avons copiée avec son identité.

Quatre chemins l’ont observée.

L’un a regardé sa valeur.

L’un son temps.

L’un sa phase.

L’un son histoire.

Puis les quatre sont revenus.

Ils ne racontaient pas la même chose.

Et c’était précisément le but.

---

## Passage au chapitre 25

# LA PORTE PELL

> **Cette fois, nous ne suivrons plus une donnée dans une machine. Nous suivrons un entier jusqu’au premier endroit où une suite accepte de le contenir.**
