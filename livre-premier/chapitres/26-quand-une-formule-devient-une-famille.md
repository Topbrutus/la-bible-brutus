# Chapitre 26 — Quand une formule devient une famille

**APRÈS L’INTRODUCTION — SEIZIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** Du cas remarquable à la structure paramétrique  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **UN RÉSULTAT PEUT ÊTRE EXTRAORDINAIRE. UNE FAMILLE EXPLIQUE POURQUOI IL N’ÉTAIT PAS SEUL.**

Au chapitre précédent, nous avions une porte.

\[
z_P(1,203,930)=1764=42^2
\]

Le résultat tenait.

Nous l’avions démonté.

Nous avions retrouvé ses facteurs.

Nous avions même trouvé un contre-exemple suffisamment proche pour nous empêcher de généraliser trop vite :

\[
z_P(21)=12
\]

Alors la question changea.

Nous ne voulions plus seulement savoir pourquoi **un nombre** produisait un rang carré.

Nous voulions savoir :

# QUELLE STRUCTURE FORCE LE CARRÉ ?

Cette fois, le travail n’allait plus consister à collectionner des exemples.

Il fallait trouver la frontière exacte.

---

## 26.1 — Revenir aux deux briques principales

Dans la factorisation du nombre fondateur :

\[
1,203,930
=
2\times3^3\times5\times7^3\times13
\]

deux puissances attirent immédiatement notre attention :

\[
3^3
\]

et :

\[
7^3
\]

Commençons donc par enlever tout le reste.

Nous définissons un noyau :

\[
N_{a,b}=3^a7^b
\]

avec :

\[
a\ge1,\qquad b\ge1
\]

La question devient :

> **Pour quels exposants (a) et (b), le rang (z_P(3^a7^b)) est-il un carré parfait ?**

Cette formulation est beaucoup plus forte qu’une liste d’exemples.

Elle nous donne un domaine.

Elle nous donne des paramètres.

Elle nous donne une condition à découvrir.

---

## 26.2 — Première brique : les puissances de 3

Nous savons :

\[
z_P(3)=4
\]

car :

\[
P_4=12
\]

est le premier nombre de Pell divisible par 3.

Et :

\[
9\nmid12
\]

Le comportement de montée des puissances de 3 est alors :

\[
\boxed{
z_P(3^a)=4\cdot3^{a-1}
}
\]

pour :

\[
a\ge1
\]

Regardons :

\[
z_P(3)=4
\]

\[
z_P(9)=12
\]

\[
z_P(27)=36
\]

\[
z_P(81)=108
\]

\[
z_P(243)=324
\]

Chaque puissance supplémentaire de 3 multiplie le rang par 3.

Nous avons donc une première échelle.

---

## 26.3 — Deuxième brique : les puissances de 7

De la même manière :

\[
z_P(7)=6
\]

car :

\[
P_6=70
\]

est le premier terme divisible par 7.

Et :

\[
49\nmid70
\]

La montée est :

\[
\boxed{
z_P(7^b)=6\cdot7^{b-1}
}
\]

pour :

\[
b\ge1
\]

Ainsi :

\[
z_P(7)=6
\]

\[
z_P(49)=42
\]

\[
z_P(343)=294
\]

\[
z_P(2401)=2058
\]

Chaque puissance supplémentaire de 7 multiplie le rang par 7.

Deux échelles sont maintenant devant nous.

---

## 26.4 — La règle qui permet de les réunir

Les nombres :

\[
3^a
\]

et :

\[
7^b
\]

sont premiers entre eux.

Pour la suite de Pell, le rang d’apparition d’un produit de deux modules premiers entre eux se réunit par le PPCM :

\[
\boxed{
z_P(mn)
=
\operatorname{ppcm}\left(z_P(m),z_P(n)\right)
}
\]

lorsque :

\[
\gcd(m,n)=1
\]

Nous pouvons donc écrire :

\[
z_P(3^a7^b)
=
\operatorname{ppcm}
\left(
4\cdot3^{a-1},
6\cdot7^{b-1}
\right)
\]

Voilà le moment important.

Notre problème n’est plus caché dans des nombres de Pell gigantesques.

Il est devenu un problème d’exposants dans un PPCM.

---

## 26.5 — Démonter le PPCM

Écrivons :

\[
4\cdot3^{a-1}
=
2^2\cdot3^{a-1}
\]

et :

\[
6\cdot7^{b-1}
=
2\cdot3\cdot7^{b-1}
\]

Le PPCM conserve le plus grand exposant de chaque facteur premier.

Donc :

\[
\boxed{
z_P(3^a7^b)
=
2^2
\cdot
3^{\max(a-1,1)}
\cdot
7^{b-1}
}
\]

ou, sous une autre forme :

\[
\boxed{
z_P(3^a7^b)
=
4\cdot3^{\max(a-1,1)}\cdot7^{b-1}
}
\]

Nous avons maintenant la formule générale de cette sous-famille.

Et avec elle, la question du carré devient presque mécanique.

---

## 26.6 — Quand un entier est-il un carré ?

Un entier positif est un carré parfait si, dans sa factorisation première, **tous ses exposants sont pairs**.

Notre rang possède les exposants :

\[
2
\]

pour le facteur 2 ;

\[
\max(a-1,1)
\]

pour le facteur 3 ;

et :

\[
b-1
\]

pour le facteur 7.

L’exposant de 2 est déjà pair.

Il reste donc deux conditions :

\[
\max(a-1,1)\equiv0\pmod2
\]

et :

\[
b-1\equiv0\pmod2
\]

Voilà la serrure.

---

## 26.7 — La condition sur (b)

Pour que :

\[
b-1
\]

soit pair, il faut :

\[
\boxed{b \text{impair}}
\]

Donc :

\[
b=1,3,5,7,\ldots
\]

Nous pouvons écrire :

\[
\boxed{b=2s+1}
\]

avec :

\[
s\ge0
\]

Première condition obtenue.

---

## 26.8 — La condition sur (a)

Nous devons avoir :

\[
\max(a-1,1)
\]

pair.

Regardons les deux petits cas.

### Si (a=1)

\[
\max(0,1)=1
\]

impair.

Échec.

### Si (a=2)

\[
\max(1,1)=1
\]

impair.

Échec.

### Si (a\ge3)

alors :

\[
\max(a-1,1)=a-1
\]

Nous voulons donc :

\[
a-1
\]

pair.

Ce qui exige :

\[
\boxed{a \text{impair et }a\ge3}
\]

Nous pouvons écrire :

\[
\boxed{a=2r+1}
\]

avec :

\[
r\ge1
\]

Deuxième condition obtenue.

---

## 26.9 — La famille apparaît

Substituons :

\[
a=2r+1
\]

et :

\[
b=2s+1
\]

avec :

\[
r\ge1,\qquad s\ge0
\]

dans notre formule.

Nous obtenons :

\[
z_P
\left(
3^{2r+1}7^{2s+1}
\right)
=
4\cdot3^{2r}\cdot7^{2s}
\]

Mais :

\[
4=2^2
\]

Donc :

\[
4\cdot3^{2r}\cdot7^{2s}
=
\left(
2\cdot3^r7^s
\right)^2
\]

Ainsi :

\[
\boxed{
z_P
\left(
3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2
}
\]

pour :

\[
\boxed{
r\ge1,\qquad s\ge0
}
\]

La formule n’est plus seule.

# NOUS AVONS UNE FAMILLE.

---

## 26.10 — Et cette fois, nous avons aussi la réciproque

Dans le domaine :

\[
a\ge1,\qquad b\ge1
\]

la condition n’est pas seulement suffisante.

Elle est nécessaire.

Autrement dit :

\[
z_P(3^a7^b)
\]

est un carré parfait **si et seulement si** :

\[
\boxed{
a\in\{3,5,7,\ldots\}
}
\]

et :

\[
\boxed{
b\in\{1,3,5,\ldots\}
}
\]

C’est une caractérisation complète de cette famille à deux primes.

À l’intérieur du domaine (3^a7^b), la frontière est maintenant visible.

---

## 26.11 — Le contre-exemple 21 trouve enfin sa place

Reprenons :

\[
21=3^1\times7^1
\]

Ici :

\[
a=1
\]

et :

\[
b=1
\]

Le second exposant convient.

Le premier non.

Notre formule donne :

\[
z_P(21)
=
4\cdot3^1\cdot7^0
=
12
\]

Donc :

\[
\boxed{z_P(21)=12}
\]

Le contre-exemple n’était pas une anomalie.

Il indiquait exactement la frontière :

> **la puissance de 3 était trop basse.**

Ce que nous avions d’abord rencontré comme un échec devient maintenant une information structurelle.

---

## 26.12 — Les premiers membres

Prenons :

\[
r=1,\qquad s=0
\]

Alors :

\[
3^{2(1)+1}7^{2(0)+1}
=
3^3\times7
=
189
\]

et :

\[
z_P(189)
=
(2\times3)^2
=
6^2
=
36
\]

Prenons :

\[
r=1,\qquad s=1
\]

Alors :

\[
3^3\times7^3
=
9261
\]

et :

\[
z_P(9261)
=
(2\times3\times7)^2
=
42^2
=
1764
\]

Prenons :

\[
r=2,\qquad s=1
\]

Alors :

\[
3^5\times7^3
=
83349
\]

et :

\[
z_P(83349)
=
(2\times3^2\times7)^2
=
126^2
=
15876
\]

Prenons :

\[
r=1,\qquad s=2
\]

Alors :

\[
3^3\times7^5
\]

possède le rang :

\[
(2\times3\times7^2)^2
=
294^2
=
86436
\]

La grille n’est plus une impression.

La formule la génère.

---

## 26.13 — Les cases qui doivent échouer

Une famille sérieuse doit prédire ses échecs.

Si (b) est pair, alors :

\[
b-1
\]

est impair.

Donc le facteur 7 apparaît avec un exposant impair dans le rang.

Pas de carré.

Si (a) est pair, alors (a-1) est impair.

Pas de carré.

Si :

\[
a=1
\]

ou :

\[
a=2
\]

le PPCM impose encore un facteur (3^1).

Pas de carré.

Ainsi, notre formule ne se contente pas de dire où regarder.

Elle dit aussi où **ne pas** attendre un carré.

---

## 26.14 — Une table devient une carte

Quelques positions :

```text
a   b   z_P(3^a 7^b)   carré ?
---------------------------------
1   1   12              NON
2   1   12              NON
3   1   36              OUI
3   2   252             NON
3   3   1764            OUI
4   3   5292            NON
5   1   324             OUI
5   3   15876           OUI
5   4   111132          NON
```

Le motif est exactement celui prédit par les parités.

Ce n’est plus :

> « Regarde, plusieurs résultats sont carrés. »

C’est :

> **« Voici la condition qui décide lesquels le sont. »**

---

## 26.15 — Retour vers 1 203 930

Mais notre nombre fondateur n’était pas seulement :

\[
3^3\times7^3
\]

Il contenait aussi :

\[
2\times5\times13
\]

Écrivons :

\[
1,203,930
=
(2\times5\times13)
(3^3\times7^3)
\]

Définissons :

\[
D=2\times5\times13=130
\]

Nous avons :

\[
z_P(2)=2
\]

\[
z_P(5)=3
\]

\[
z_P(13)=7
\]

Donc :

\[
z_P(130)
=
\operatorname{ppcm}(2,3,7)
=
42
\]

Or le noyau :

\[
3^3\times7^3
\]

possède le rang :

\[
42^2=1764
\]

Et :

\[
42\mid42^2
\]

Ainsi, ajouter le facteur 130 ne change pas le PPCM final :

\[
\operatorname{ppcm}(42,1764)=1764
\]

Voilà pourquoi :

\[
z_P(1,203,930)=1764
\]

Le facteur extérieur n’a pas créé le carré.

# IL ÉTAIT COMPATIBLE AVEC LUI.

---

## 26.16 — La famille qui contient le nombre fondateur

Nous pouvons maintenant étendre le noyau.

Définissons :

\[
M_{r,s}
=
130\cdot3^{2r+1}7^{2s+1}
\]

avec :

\[
r\ge1,\qquad s\ge1
\]

Le noyau possède :

\[
z_P
\left(
3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2
\]

Lorsque :

\[
r\ge1,\qquad s\ge1
\]

ce carré contient déjà les facteurs nécessaires à :

\[
z_P(130)=42=2\cdot3\cdot7
\]

Donc :

\[
\boxed{
z_P(M_{r,s})
=
\left(
2\cdot3^r7^s
\right)^2
}
\]

Le nombre fondateur correspond exactement à :

\[
r=1,\qquad s=1
\]

car :

\[
M_{1,1}
=
130\cdot3^3\cdot7^3
=
1,203,930
\]

et :

\[
z_P(M_{1,1})=42^2
\]

Notre cas initial est donc un membre d’une famille explicite.

---

## 26.17 — Le principe du facteur compatible

Ce que nous venons de voir peut être écrit de façon plus générale.

Supposons que :

\[
C_{r,s}
=
3^{2r+1}7^{2s+1}
\]

et :

\[
Q_{r,s}
=
2\cdot3^r7^s
\]

Alors :

\[
z_P(C_{r,s})=Q_{r,s}^2
\]

Prenons maintenant un entier (d) premier avec 21.

Si :

\[
z_P(d)\mid Q_{r,s}^2
\]

alors :

\[
z_P(dC_{r,s})
=
\operatorname{ppcm}
\left(
z_P(d),Q_{r,s}^2
\right)
\]

et puisque le premier terme divise le second :

\[
\boxed{
z_P(dC_{r,s})=Q_{r,s}^2
}
\]

Autrement dit :

# UN FACTEUR PEUT ÊTRE AJOUTÉ SANS DÉTRUIRE LE RANG CARRÉ SI SON PROPRE RANG EST DÉJÀ ABSORBÉ PAR LE CARRÉ.

C’est une porte beaucoup plus générale.

---

## 26.18 — Un générateur commence à apparaître

Nous pouvons maintenant penser autrement.

Au lieu de demander :

> Quels nombres donnent par hasard un rang carré ?

nous pouvons construire :

```text
1. choisir un noyau square-rank
2. calculer son rang carré Q²
3. chercher des facteurs d dont z_P(d) divise Q²
4. imposer la coprimalité nécessaire
5. ajouter ces facteurs
6. vérifier que le PPCM reste Q²
```

Nous obtenons un début de :

# GÉNÉRATEUR DE SQUARE-RANK

Mais ce mot doit rester correctement classé.

Le mécanisme mathématique de construction est réel.

La portée générale, les classes maximales et la nouveauté bibliographique demandent encore du travail.

---

## 26.19 — Le changement de niveau

Au chapitre 25, nous avions :

\[
1,203,930\rightarrow42^2
\]

Maintenant nous avons :

\[
3^{2r+1}7^{2s+1}
\rightarrow
\left(2\cdot3^r7^s\right)^2
\]

avec :

\[
r\ge1,\qquad s\ge0
\]

Puis une extension contenant notre nombre fondateur :

\[
130\cdot3^{2r+1}7^{2s+1}
\rightarrow
\left(2\cdot3^r7^s\right)^2
\]

pour :

\[
r\ge1,\qquad s\ge1
\]

Nous sommes passés :

```text
UN NOMBRE
↓
PLUSIEURS EXEMPLES
↓
FORMULE PARAMÉTRIQUE
↓
CONDITION NÉCESSAIRE ET SUFFISANTE
↓
EXTENSION PAR FACTEURS COMPATIBLES
```

C’est exactement le moment où une formule commence à devenir une famille.

---

## 26.20 — Ce qui est prouvé ici et ce qui ne l’est pas

Nous devons arrêter le récit quelques secondes.

### CALCUL / DÉRIVATION

Dans la sous-famille (3^a7^b), en utilisant les identités standard de rang pour les puissances de 3 et 7 et la règle du PPCM pour les modules premiers entre eux :

\[
z_P(3^a7^b)
=
4\cdot3^{\max(a-1,1)}7^{b-1}
\]

### CONSÉQUENCE

Ce rang est carré si et seulement si :

\[
a=2r+1,\quad r\ge1
\]

et :

\[
b=2s+1,\quad s\ge0
\]

### CONSÉQUENCE

\[
z_P
\left(
3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2
\]

### EXTENSION

Tout facteur copremier dont le rang divise déjà le carré peut être absorbé sans modifier le rang final.

### NON PROUVÉ PAR CE CHAPITRE

Que cette famille est inconnue de la littérature.

### NON PROUVÉ PAR CE CHAPITRE

Qu’elle est maximale parmi toutes les familles square-rank de Pell.

### NON PROUVÉ PAR CE CHAPITRE

Qu’un phénomène physique quelconque est lié à cette arithmétique.

Voilà notre frontière actuelle.

---

## 26.21 — Repère externe de rigueur

La notion utilisée ici n’est pas inventée par notre projet.

Le rang d’apparition — ou *entry point* — de la suite de Pell est étudié dans la littérature des suites de Lucas.

Les identités structurelles employées ici correspondent aux propriétés standard suivantes :

- les nombres de Pell forment une suite de divisibilité forte ;
- pour des modules premiers entre eux, les rangs se réunissent par PPCM ;
- sous la condition de non-exception au premier niveau, le rang d’une puissance première se relève par multiplication successive par le premier.

Notre contribution de travail n’est donc pas d’inventer ces règles.

Notre travail consiste à voir ce qu’elles produisent lorsqu’elles sont appliquées à **notre entrée**, puis à caractériser les familles qui en émergent.

La question d’antériorité de la formulation **Brutus–Pell Square-Rank Relation** reste séparée et doit être documentée avant toute revendication de nouveauté.

---

## 26.22 — La formule seule

Le cœur du chapitre tient maintenant en une ligne :

\[
\boxed{
z_P
\left(
3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2,
\qquad
r\ge1, s\ge0
}
\]

Et la famille contenant exactement notre nombre fondateur :

\[
\boxed{
z_P
\left(
130\cdot3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2,
\qquad
r\ge1, s\ge1
}
\]

avec :

\[
130=2\cdot5\cdot13
\]

Pour :

\[
r=s=1
\]

nous retrouvons :

\[
1,203,930
\]

et :

\[
42^2
\]

La porte referme parfaitement la boucle.

---

## 26.23 — Mais maintenant il faut essayer de la détruire

Une belle dérivation peut encore cacher une mauvaise hypothèse.

Nous devons donc attaquer :

- la formule de montée des puissances premières ;
- les cas limites ;
- les exposants zéro ;
- les facteurs supplémentaires ;
- les primes exceptionnels ;
- les contaminations entre rangs ;
- les généralisations à d’autres couples de nombres premiers ;
- l’antériorité bibliographique.

Nous avons construit une famille.

Le prochain travail n’est pas de l’admirer.

# IL FAUT LA METTRE SOUS LE SCALPEL.

---

# Fin du chapitre 26

Au commencement, il y avait :

\[
1,203,930
\]

Puis :

\[
1764
\]

Puis :

\[
42^2
\]

Nous pensions avoir trouvé un résultat.

Alors nous avons retiré les décorations.

Nous avons gardé :

\[
3^a7^b
\]

Nous avons regardé les rangs des puissances.

Nous avons ouvert le PPCM.

Nous avons suivi les exposants.

Et la frontière est apparue :

\[
a=3,5,7,\ldots
\]

\[
b=1,3,5,\ldots
\]

Alors le cas unique est devenu :

\[
\boxed{
z_P
\left(
3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2
}
\]

Puis le nombre fondateur est revenu prendre sa place dans une famille plus grande.

Cette fois, le dévoilement n’était plus une ressemblance.

Il avait des paramètres.

Des conditions.

Des échecs prédits.

Une réciproque.

Et une porte vers un générateur.

Mais le Royaume connaissait maintenant sa propre règle.

Plus une idée devient belle,

plus il faut essayer fort de la casser.

---

## Passage au chapitre 27

# LE SCALPEL DE LA PREUVE

> **Une famille n’obtient pas le droit de devenir un théorème parce qu’elle est élégante. Elle doit survivre à l’attaque.**
