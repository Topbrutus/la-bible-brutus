# Chapitre 25 — La Porte Pell

**APRÈS L’INTRODUCTION — QUINZIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** Du nombre fondateur au rang carré  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **CETTE FOIS, NOUS NE SUIVRONS PLUS UNE DONNÉE DANS UNE MACHINE. NOUS SUIVRONS UN ENTIER JUSQU’AU PREMIER ENDROIT OÙ UNE SUITE ACCEPTE DE LE CONTENIR.**

Il existe des moments où une recherche change de direction sans changer de question.

Nous cherchions déjà : où ? quand ? après combien d’étapes ?

Puis nous avons rencontré une suite mathématique capable de poser presque la même question à un entier.

# LA SUITE DE PELL

Et derrière elle se cachait une porte que nous n’avions pas construite.

Nous l’avons seulement ouverte.

---

## 25.1 — La suite

Définissons :

[
P_0=0,qquad P_1=1
]

et :

[
oxed{P_{n+1}=2P_n+P_{n-1}}
]

Nous obtenons :

[
0, 1, 2, 5, 12, 29, 70, 169, 408, 985,ldots
]

Chaque terme dépend des deux précédents.

Une récurrence simple, avec des propriétés de divisibilité riches.

---

## 25.2 — Le rang d’apparition

Pour un entier positif (m), nous cherchons le premier terme de Pell divisible par (m).

Définissons :

[
oxed{
z_P(m)=min{nge1:mmid P_n}
}
]

Autrement dit :

# À QUEL PREMIER INDICE (n) LE NOMBRE (m) DIVISE-T-IL (P_n) ?

Ce nombre (n) est son rang d’apparition dans la suite de Pell.

---

## 25.3 — Exemple simple

Prenons :

[
m=13
]

La suite donne :

[
P_7=169=13^2
]

et aucun terme précédent n’est divisible par 13.

Ainsi :

[
oxed{z_P(13)=7}
]

Le nombre 13 possède maintenant une adresse dans la suite.

---

## 25.4 — Une autre adresse

Prenons :

[
637=7^2	imes13
]

Le calcul donne :

[
oxed{z_P(637)=42}
]

Nous rencontrons déjà :

[
13ightarrow7
]

et :

[
637ightarrow42
]

Mais la porte va s’ouvrir avec un nombre que nous connaissions avant d’arriver chez Pell.

---

## 25.5 — Le nombre fondateur

Dans notre construction existait déjà :

[
3	imes(6+1)	imes7	imes7	imes9	imes10	imes13
]

soit :

[
oxed{1,203,930}
]

Appelons-le ici :

[
B_{mathrm{fond}}=1,203,930
]

Sa factorisation première est :

[
oxed{
1,203,930
=
2	imes3^3	imes5	imes7^3	imes13
}
]

Puis nous avons posé une question nouvelle :

# QUEL EST SON RANG D’APPARITION DANS LA SUITE DE PELL ?

---

## 25.6 — Le test

Nous calculons la suite de Pell modulo :

[
1,203,930
]

et cherchons le premier indice (n) tel que :

[
P_nequiv0pmod{1,203,930}
]

Le premier zéro apparaît à :

[
oxed{n=1764}
]

Ainsi :

[
oxed{z_P(1,203,930)=1764}
]

---

## 25.7 — Et 1764 est un carré parfait

Factorisons :

[
1764=2^2	imes3^2	imes7^2
]

Donc :

[
1764=(2	imes3	imes7)^2
]

et :

[
2	imes3	imes7=42
]

Ainsi :

[
oxed{1764=42^2}
]

Par conséquent :

[
oxed{z_P(1,203,930)=42^2}
]

Voilà le cœur exact de la découverte.

---

## 25.8 — Brutus–Pell Square-Rank Relation

Nous pouvons nommer l’identité observée :

# BRUTUS–PELL SQUARE-RANK RELATION

avec :

[
oxed{z_P(B_{mathrm{fond}})=42^2}
]

où :

[
oxed{
B_{mathrm{fond}}
=
3(6+1)(7)(7)(9)(10)(13)
=
1,203,930
}
]

Donc :

[
oxed{
z_P!left(3(6+1)(7)(7)(9)(10)(13)ight)=42^2
}
]

Auteur du travail : **Gabriel St-Pierre**.

---

## 25.9 — Ce qui est remarquable

Le point intéressant est la chaîne complète :

[
oxed{
1,203,930
longrightarrow
z_P
longrightarrow
1764
longrightarrow
42^2
}
]

Le nombre d’entrée venait d’une construction antérieure.

Nous ne l’avons pas choisi après avoir regardé Pell afin d’obtenir un carré.

Puis une opération mathématique définie indépendamment — le rang d’apparition — l’a envoyé vers un carré parfait.

Ce caractère préexistant de l’entrée rend le résultat particulièrement intéressant à étudier.

---

## 25.10 — Intéressant ne veut pas dire unique

Deux questions doivent rester séparées.

### Question mathématique

[
z_P(1,203,930)=42^2 ?
]

Réponse calculatoire :

# OUI.

### Question d’antériorité

> Cette identité particulière ou la famille dont elle découle a-t-elle déjà été explicitement publiée ?

Statut :

# À VÉRIFIER BIBLIOGRAPHIQUEMENT.

---

## 25.11 — Démonter 1 203 930

La factorisation permet d’étudier séparément :

[
2,quad27,quad5,quad343,quad13
]

Les rangs calculés sont :

[
z_P(2)=2
]

[
z_P(27)=36
]

[
z_P(5)=3
]

[
z_P(343)=294
]

[
z_P(13)=7
]

Donc :

```text
2    → 2
27   → 36
5    → 3
343  → 294
13   → 7
```

---

## 25.12 — Le rendez-vous des rangs

Pour qu’un même indice satisfasse toutes ces divisibilités, il doit être compatible avec :

[
2, 36, 3, 294, 7
]

Leur PPCM est :

[
operatorname{ppcm}(2,36,3,294,7)
]

avec :

[
36=2^2	imes3^2
]

et :

[
294=2	imes3	imes7^2
]

Donc :

[
operatorname{ppcm}(2,36,3,294,7)
=
2^2	imes3^2	imes7^2
=
1764
]

et :

[
oxed{1764=42^2}
]

Le carré n’est plus seulement observé : nous voyons comment sa factorisation émerge.

---

## 25.13 — Regarde les exposants

Le résultat est :

[
1764=2^2 3^2 7^2
]

Chaque exposant est pair.

C’est exactement la condition pour être un carré parfait.

La question devient :

# POURQUOI LES EXPOSANTS MAXIMAUX SE RETROUVENT-ILS TOUS PAIRS DANS CE CAS ?

Cette question attaque le mécanisme.

---

## 25.14 — Le 42 ne doit pas être idolâtré

Nous connaissons ici l’origine arithmétique du 42 :

[
42=2	imes3	imes7
]

et :

[
42^2=2^2	imes3^2	imes7^2
]

Le 42 n’a pas besoin d’une explication mystique.

Il possède ici une construction arithmétique précise.

---

## 25.15 — Le test direct

Nous pouvons vérifier directement que :

[
P_{1764}equiv0pmod{1,203,930}
]

et qu’aucun indice plus petit ne satisfait la condition.

Deux voies conduisent alors au même résultat :

```text
VOIE A
factorisation → rangs → PPCM → 1764

VOIE B
récurrence modulo B → premier zéro → 1764
```

Puis :

[
1764=42^2
]

La convergence des méthodes renforce la confiance dans le calcul.

---

## 25.16 — Source, calcul, interprétation

### SOURCE

[
3(6+1)(7)(7)(9)(10)(13)=1,203,930
]

### DÉFINITION

[
z_P(m)=min{nge1:mmid P_n}
]

### CALCUL

[
z_P(1,203,930)=1764
]

### CALCUL

[
1764=42^2
]

### INTERPRÉTATION

La structure de factorisation de l’entrée produit ici un rang dont tous les exposants premiers sont pairs.

### QUESTION OUVERTE

Existe-t-il une famille générale permettant de prédire systématiquement ce phénomène ?

---

## 25.17 — Un cas n’est pas encore une famille

Une seule identité exacte ne constitue pas automatiquement une loi générale.

La bonne progression est :

```text
UN CAS
↓
FACTORISATION
↓
MÉCANISME
↓
VARIATION DES EXPOSANTS
↓
NOUVEAUX CAS
↓
CONTRE-EXEMPLES
↓
FAMILLE CANDIDATE
```

---

## 25.18 — Premières variations

Des cas testés montrent des rangs carrés, par exemple :

[
z_P(189)=36=6^2
]

avec :

[
189=3^3	imes7
]

Puis :

[
z_P(9261)=1764=42^2
]

avec :

[
9261=3^3	imes7^3
]

Et :

[
z_P(83349)=15876=126^2
]

avec :

[
83349=3^5	imes7^3
]

Une grille commence à apparaître.

---

## 25.19 — Mais une exception apparaît immédiatement

Essayons :

[
3	imes7=21
]

Nous trouvons :

[
z_P(21)=12
]

Or 12 n’est pas un carré parfait.

Excellent.

Parce que cette exception détruit immédiatement une généralisation trop facile.

# LE CONTRE-EXEMPLE NOUS PROTÈGE.

---

## 25.20 — La frontière commence à apparaître

Les cas testés montrent que le comportement carré demande des conditions.

La bonne question n’est plus :

> Est-ce toujours un carré ?

Elle devient :

# QUELLES CONDITIONS SUR LES EXPOSANTS FORCENT LE RANG À DEVENIR UN CARRÉ ?

Nous sommes passés d’une curiosité à un problème mathématique défini.

---

## 25.21 — Le nom prend son sens

Square-Rank signifie ici :

> **une famille d’entrées dont le rang d’apparition dans la suite de Pell est un carré parfait.**

Nous recherchons donc les (m) tels que :

[
z_P(m)=q^2
]

pour un entier (q).

C’est une question claire.

Calculable.

Réfutable.

---

## 25.22 — La machine à traces

Notre méthode de recherche devient :

```text
INTUITION
↓
CALCUL
↓
CONTRE-TEST
↓
PREUVE
↓
ANTÉRIORITÉ
↓
TRACE DURABLE
```

Le résultat a besoin de chacune de ces étapes.

---

## 25.23 — Ne pas confondre trois découvertes

### Niveau 1

[
z_P(1,203,930)=1764=42^2
]

Identité numérique vérifiée.

### Niveau 2

Une ou plusieurs familles paramétriques produisent également des rangs carrés.

À caractériser et démontrer.

### Niveau 3

La famille ou sa formulation serait nouvelle dans la littérature.

À établir par recherche d’antériorité.

Le niveau 1 n’accorde pas automatiquement les niveaux 2 et 3.

Mais il justifie leur exploration.

---

## 25.24 — La porte est donc réelle

Nous avions commencé avec :

[
1,203,930
]

Puis Pell nous a répondu :

[
1764
]

et :

[
1764=42^2
]

Nous avons regardé des voisins.

Certains produisent également des carrés.

Nous avons testé une généralisation trop large.

Elle a cassé à 21.

Parfait.

Nous connaissons maintenant une partie de la frontière.

---

# Fin du chapitre 25

Nous avions apporté un nombre à une suite vieille de bien avant notre machine.

Nous lui avons demandé :

> **« Où apparais-tu pour la première fois ? »**

La suite a répondu :

[
1764
]

Nous l’avons factorisé :

[
2^2	imes3^2	imes7^2
]

Puis :

[
(2	imes3	imes7)^2
]

Puis :

[
42^2
]

Mais au moment même où nous pensions avoir trouvé une réponse, le contre-exemple 21 nous rappela la règle du Royaume :

# UNE BELLE FORMULE N’EST PAS ENCORE UNE FAMILLE.

Alors nous avons changé de question :

# QUELS NOMBRES SONT FORCÉS D’EN DONNER UN ?

Et soudain, derrière la Porte Pell, il n’y avait pas une formule.

Il y avait tout un territoire.

---

## Passage au chapitre 26

# QUAND UNE FORMULE DEVIENT UNE FAMILLE

> **Un résultat peut être extraordinaire. Une famille explique pourquoi il n’était pas seul.**
