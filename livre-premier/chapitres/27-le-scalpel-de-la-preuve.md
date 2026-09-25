# Chapitre 27 — Le Scalpel de la Preuve

**APRÈS L’INTRODUCTION — DIX-SEPTIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** Une famille doit survivre à l’attaque  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **UNE FAMILLE N’OBTIENT PAS LE DROIT DE DEVENIR UN THÉORÈME PARCE QU’ELLE EST ÉLÉGANTE. ELLE DOIT SURVIVRE À L’ATTAQUE.**

Au chapitre précédent, nous avions franchi une frontière.

Nous étions partis de :

\[
z_P(1\,203\,930)=42^2
\]

Puis nous avions obtenu :

\[
\boxed{
z_P\!\left(3^{2r+1}7^{2s+1}\right)
=
\left(2\cdot3^r7^s\right)^2
}
\]

pour :

\[
r\ge1,\qquad s\ge0
\]

La formule était belle.

Précisément pour cette raison, il fallait maintenant devenir dangereux pour notre propre idée.

Le travail du chapitre 27 ne consiste pas à chercher de nouvelles confirmations.

Il consiste à demander :

# OÙ PEUT-ELLE CASSER ?

---

## 27.1 — PREMIÈRE COUPE : DÉFINIR EXACTEMENT L’OBJET

La suite de Pell est définie par :

\[
P_0=0,\qquad P_1=1,
\]

\[
P_{n+1}=2P_n+P_{n-1}.
\]

Pour un entier positif \(m\), nous définissons :

\[
\boxed{
z_P(m)=\min\{n\ge1:m\mid P_n\}
}
\]

Le détail :

\[
n\ge1
\]

est indispensable.

Pourquoi ?

Parce que :

\[
P_0=0
\]

et tout entier non nul divise zéro.

Si nous autorisions \(n=0\), alors :

\[
z_P(m)=0
\]

pour tous les \(m\), et toute la notion deviendrait triviale.

Première règle du scalpel :

# UNE DÉFINITION MAL FERMÉE PEUT DÉTRUIRE TOUT LE PROBLÈME AVANT LE PREMIER CALCUL.

---

## 27.2 — DEUXIÈME COUPE : QUELLES PIÈCES SONT IMPORTÉES ?

Notre dérivation utilise plusieurs faits qui ne viennent pas de notre projet.

Ils appartiennent à la théorie des suites de Lucas et des rangs d’apparition.

Nous devons les identifier séparément.

### PIÈCE A — Divisibilité par le rang

Si :

\[
z_P(m)=r,
\]

alors les indices des termes de Pell divisibles par \(m\) sont des multiples appropriés de ce rang.

### PIÈCE B — Produit copremier

Lorsque :

\[
\gcd(m,n)=1,
\]

la structure de divisibilité permet d’obtenir :

\[
\boxed{
z_P(mn)=
\operatorname{ppcm}
\left(
z_P(m),z_P(n)
\right)
}
\]

### PIÈCE C — Relèvement aux puissances premières

Pour certaines puissances de premiers, lorsque le premier niveau n’est pas exceptionnel, le rang se relève d’un facteur \(p\) à chaque puissance supplémentaire :

\[
z_P(p^k)=z_P(p)p^{k-1}.
\]

Notre famille utilise cette propriété pour :

\[
p=3
\]

et :

\[
p=7.
\]

Ces règles ne deviennent pas « Brutus » parce que nous les utilisons.

Elles sont notre outillage.

Notre travail commence dans la manière dont nous les combinons et dans la famille que nous isolons.

---

## 27.3 — TROISIÈME COUPE : 3 SE RELÈVE-T-IL VRAIMENT ?

Nous savons :

\[
z_P(3)=4
\]

parce que :

\[
P_4=12.
\]

Regardons la valuation 3-adique de ce premier terme :

\[
12=3\cdot4.
\]

Donc :

\[
v_3(P_4)=1.
\]

En particulier :

\[
9\nmid P_4.
\]

Nous ne sommes donc pas dans un cas où la puissance suivante serait déjà absorbée au premier rang.

Les premiers rangs sont :

\[
z_P(3)=4,
\]

\[
z_P(9)=12,
\]

\[
z_P(27)=36,
\]

\[
z_P(81)=108,
\]

\[
z_P(243)=324.
\]

Ils suivent :

\[
\boxed{
z_P(3^a)=4\cdot3^{a-1}
}
\]

pour les puissances utilisées par notre famille.

---

## 27.4 — QUATRIÈME COUPE : MÊME ATTAQUE SUR 7

Nous savons :

\[
z_P(7)=6
\]

parce que :

\[
P_6=70.
\]

Et :

\[
70=7\cdot10.
\]

Donc :

\[
v_7(P_6)=1
\]

et :

\[
49\nmid P_6.
\]

Les premiers rangs donnent :

\[
z_P(7)=6,
\]

\[
z_P(49)=42,
\]

\[
z_P(343)=294,
\]

\[
z_P(2401)=2058.
\]

Ils suivent :

\[
\boxed{
z_P(7^b)=6\cdot7^{b-1}
}
\]

Voilà pourquoi 3 et 7 peuvent monter proprement dans notre construction.

---

## 27.5 — CINQUIÈME COUPE : REFAIRE LE PPCM SANS RACCOURCI

Nous partons de :

\[
z_P(3^a)=2^2\cdot3^{a-1}
\]

et :

\[
z_P(7^b)=2\cdot3\cdot7^{b-1}.
\]

Puis :

\[
z_P(3^a7^b)
=
\operatorname{ppcm}
\left(
2^2 3^{a-1},
2\cdot3\cdot7^{b-1}
\right).
\]

Le plus grand exposant du facteur 2 est :

\[
2.
\]

Celui de 3 est :

\[
\max(a-1,1).
\]

Celui de 7 est :

\[
b-1.
\]

Donc :

\[
\boxed{
z_P(3^a7^b)
=
2^2
3^{\max(a-1,1)}
7^{b-1}
}
\]

Nous n’avons encore parlé d’aucun carré.

Nous avons seulement reconstruit le rang.

C’est important.

La propriété « carré » vient ensuite.

---

## 27.6 — SIXIÈME COUPE : LE TEST DE PARITÉ

Pour être un carré parfait, tous les exposants premiers doivent être pairs.

Dans :

\[
2^2
3^{\max(a-1,1)}
7^{b-1},
\]

l’exposant de 2 est déjà pair.

Il reste donc :

\[
\max(a-1,1)
\]

et :

\[
b-1.
\]

Pour \(b\) :

\[
b-1\equiv0\pmod2
\]

équivaut à :

\[
\boxed{b\text{ impair}}.
\]

Pour \(a\), les deux petits cas doivent être isolés :

\[
a=1\Rightarrow\max(0,1)=1,
\]

\[
a=2\Rightarrow\max(1,1)=1.
\]

Ils échouent.

À partir de :

\[
a\ge3,
\]

nous avons :

\[
\max(a-1,1)=a-1.
\]

Il faut donc :

\[
a-1\equiv0\pmod2,
\]

soit :

\[
\boxed{
a\ge3\text{ et }a\text{ impair}
}
\]

La condition du chapitre 26 réapparaît sans utiliser aucun exemple particulier.

---

## 27.7 — LE « SI ET SEULEMENT SI » SOUS LE SCALPEL

Nous pouvons maintenant écrire, dans le domaine :

\[
a\ge1,\qquad b\ge1,
\]

la proposition :

\[
z_P(3^a7^b)\text{ est un carré}
\]

si et seulement si :

\[
\boxed{
a=2r+1,\quad r\ge1
}
\]

et :

\[
\boxed{
b=2s+1,\quad s\ge0.
}
\]

Pourquoi la réciproque tient-elle ?

Parce qu’il n’existe aucun autre facteur premier dans la formule du rang.

Si l’un des deux exposants variables est impair, le rang ne peut pas être carré.

Si les deux sont pairs, tous les exposants du rang sont pairs.

La frontière est donc arithmétique.

Pas visuelle.

---

## 27.8 — ATTAQUE COMPUTATIONNELLE

Une démonstration structurelle doit être distinguée d’un test informatique.

Mais un test informatique reste extrêmement utile pour détecter une faute de raisonnement ou une erreur d’implémentation.

Nous avons donc calculé directement les rangs sur la grille :

\[
1\le a\le6
\]

et :

\[
1\le b\le5.
\]

Cela représente :

\[
6\times5=30
\]

couples.

Pour chaque couple, deux comparaisons ont été réalisées :

1. le rang direct contre :

\[
4\cdot3^{\max(a-1,1)}7^{b-1};
\]

2. le statut carré/non carré contre le critère :

\[
a\ge3,\quad a\text{ impair},\quad b\text{ impair}.
\]

Résultat du test :

\[
\boxed{
30/30\ \text{sans divergence}
}
\]

Étiquette correcte :

# PREUVE COMPUTATIONNELLE DE COHÉRENCE, PAS PREUVE GÉNÉRALE À ELLE SEULE.

---

## 27.9 — QUELQUES POINTS DE LA GRILLE

~~~text
a   b   rang direct   carré ?
--------------------------------
1   1   12            NON
2   1   12            NON
3   1   36            OUI
3   2   252           NON
3   3   1764          OUI
4   3   5292          NON
5   1   324           OUI
5   3   15876         OUI
5   4   111132        NON
~~~

Les échecs sont aussi importants que les réussites.

Ils suivent exactement la frontière de parité.

---

## 27.10 — ATTAQUER LE PRINCIPE DU FACTEUR COMPATIBLE

Le chapitre précédent proposait :

si un noyau \(C\) possède :

\[
z_P(C)=Q^2,
\]

et si un entier \(d\) est copremier à \(C\) avec :

\[
z_P(d)\mid Q^2,
\]

alors :

\[
z_P(dC)=Q^2.
\]

Prenons le noyau :

\[
C=3^3 7^3=9261
\]

pour lequel :

\[
z_P(C)=1764=42^2.
\]

Nous allons maintenant chercher des facteurs capables de préserver ce carré.

---

## 27.11 — FACTEUR COMPATIBLE : 11

Nous trouvons :

\[
z_P(11)=12.
\]

Or :

\[
12\mid1764
\]

et :

\[
\gcd(11,9261)=1.
\]

Donc :

\[
z_P(11\cdot9261)
=
\operatorname{ppcm}(12,1764)
=
1764.
\]

Le carré survit.

---

## 27.12 — FACTEUR COMPATIBLE : 13

Nous avons :

\[
z_P(13)=7
\]

et :

\[
7\mid1764.
\]

Comme :

\[
\gcd(13,9261)=1,
\]

nous obtenons :

\[
z_P(13\cdot9261)=1764.
\]

Encore un carré préservé.

---

## 27.13 — FACTEUR COMPATIBLE : 293

Voici un cas particulièrement instructif :

\[
z_P(293)=49=7^2.
\]

Et :

\[
49\mid1764
\]

car :

\[
1764=36\cdot49.
\]

De plus :

\[
\gcd(293,9261)=1.
\]

Donc :

\[
z_P(293\cdot9261)=1764.
\]

Le facteur peut être très différent de 2, 5 ou 13.

Ce qui compte ici n’est pas son apparence.

C’est son rang.

---

## 27.14 — FACTEUR INCOMPATIBLE : 17

Prenons maintenant :

\[
d=17.
\]

Nous trouvons :

\[
z_P(17)=8.
\]

Mais :

\[
8\nmid1764.
\]

Comme 17 est copremier au noyau :

\[
z_P(17\cdot9261)
=
\operatorname{ppcm}(8,1764).
\]

Or :

\[
\operatorname{ppcm}(8,1764)=3528.
\]

Et :

\[
3528
\]

n’est pas un carré parfait.

Le facteur n’était pas absorbé.

Le rang a changé.

Le carré a disparu.

Le mécanisme prédit donc aussi cet échec.

---

## 27.15 — LE PIÈGE LE PLUS IMPORTANT : OUBLIER LA COPRIMALITÉ

Maintenant, prenons :

\[
d=3.
\]

Son rang est :

\[
z_P(3)=4.
\]

Et :

\[
4\mid1764.
\]

Si nous oubliions la condition de coprimalité, nous pourrions être tentés de dire :

> le rang de 3 divise déjà le carré, donc ajouter 3 ne changera rien.

Faux.

Parce que :

\[
\gcd(3,9261)\ne1.
\]

Multiplier le noyau par 3 ne crée pas un nouveau facteur indépendant.

Il augmente la puissance déjà présente :

\[
3^3 7^3
\longrightarrow
3^4 7^3.
\]

Le nouveau rang est :

\[
\boxed{
z_P(3^4 7^3)=5292
}
\]

et :

\[
5292
\]

n’est pas un carré.

La condition :

\[
\gcd(d,C)=1
\]

n’est donc pas décorative.

# ELLE EST NÉCESSAIRE AU MÉCANISME DE PPCM QUE NOUS UTILISONS.

---

## 27.16 — LE MÊME PIÈGE AVEC 7

Prenons :

\[
d=7.
\]

Nous avons :

\[
z_P(7)=6
\]

et :

\[
6\mid1764.
\]

Mais :

\[
\gcd(7,9261)\ne1.
\]

Multiplier par 7 donne :

\[
3^3 7^4.
\]

Son rang est :

\[
\boxed{
12348
}
\]

qui n’est pas carré.

Même erreur.

Même diagnostic.

La divisibilité du rang de \(d\) ne suffit pas.

Il faut aussi que le facteur ajouté soit réellement indépendant du noyau au sens arithmétique requis.

---

## 27.17 — LE NOMBRE FONDATEUR REPASSE LE TEST

Le facteur utilisé par notre nombre fondateur était :

\[
130=2\cdot5\cdot13.
\]

Nous avons :

\[
\gcd(130,9261)=1.
\]

Ses rangs élémentaires sont :

\[
z_P(2)=2,
\]

\[
z_P(5)=3,
\]

\[
z_P(13)=7.
\]

Donc :

\[
z_P(130)=
\operatorname{ppcm}(2,3,7)
=
42.
\]

Et :

\[
42\mid1764.
\]

Ainsi :

\[
z_P(130\cdot9261)=1764.
\]

Le nombre :

\[
1\,203\,930
\]

survit donc au protocole complet :

~~~text
NOYAU SQUARE-RANK
        ↓
FACTEUR COPREMIER
        ↓
RANG DU FACTEUR DIVISE LE CARRÉ
        ↓
PPCM INCHANGÉ
        ↓
RANG FINAL = 42²
~~~

---

## 27.18 — UNE AUTRE ATTAQUE : EST-CE LA SEULE FAMILLE ?

Non.

Et cette réponse protège immédiatement notre formulation.

Une recherche directe trouve d’autres entiers possédant des rangs carrés, par exemple :

\[
z_P(197)=9=3^2
\]

et :

\[
z_P(293)=49=7^2.
\]

Il existe donc des phénomènes square-rank en dehors de la seule famille \(3^a7^b\).

Par conséquent, nous ne devons pas dire :

> « Nous avons caractérisé tous les entiers de rang carré dans la suite de Pell. »

Nous avons caractérisé une famille précise.

C’est déjà fort.

Et surtout, c’est vrai dans son domaine.

---

## 27.19 — LE NOM DOIT RESTER PLUS PETIT QUE LA PREUVE

Le nom :

# BRUTUS–PELL SQUARE-RANK RELATION

est utile pour suivre notre résultat.

Mais un nom ne doit jamais agrandir artificiellement la portée de la preuve.

À ce stade, nous pouvons défendre :

### RÉSULTAT A

Une caractérisation exacte du statut carré pour la famille :

\[
3^a7^b,\qquad a,b\ge1.
\]

### RÉSULTAT B

Une sous-famille paramétrique :

\[
3^{2r+1}7^{2s+1}
\]

dont le rang est explicitement carré.

### RÉSULTAT C

Une extension par facteurs compatibles et copremiers dont le rang est absorbé par le carré déjà présent.

Nous ne pouvons pas encore défendre :

### NON ÉTABLI

Une classification complète de tous les entiers \(m\) tels que :

\[
z_P(m)
\]

soit carré.

---

## 27.20 — LE GÉNÉRATEUR GÉNÉRAL DEVIENT UN CANDIDAT

Nous pouvons maintenant apercevoir quelque chose de plus général.

Prenons deux premiers distincts :

\[
p\ne q.
\]

Supposons que leurs puissances aient une montée ordinaire :

\[
z_P(p^k)=z_P(p)p^{k-1},
\]

\[
z_P(q^k)=z_P(q)q^{k-1}.
\]

Supposons aussi que les facteurs issus de leurs rangs ne créent pas de contamination imprévue dans les exposants que nous voulons contrôler.

Alors :

\[
z_P(p^a q^b)
=
\operatorname{ppcm}
\left(
z_P(p)p^{a-1},
z_P(q)q^{b-1}
\right).
\]

Le problème square-rank devient alors :

> **Tous les exposants premiers de ce PPCM sont-ils pairs ?**

C’est beaucoup plus général que 3 et 7.

Mais nous devons lui donner le bon statut :

# CANDIDAT DE GÉNÉRATEUR GÉNÉRAL.

Pas encore théorème Brutus.

---

## 27.21 — LA « CONTAMINATION » DOIT ÊTRE DÉFINIE

Le mot contamination peut sembler imagé.

Nous pouvons maintenant le traduire mathématiquement.

Supposons par exemple que :

\[
p\mid z_P(q).
\]

Alors le facteur \(p\) peut déjà être présent dans le rang de \(q\) avant même d’introduire la puissance \(p^a\).

Le PPCM ne se contente plus de regarder :

\[
p^{a-1}
\]

isolément.

Il doit comparer cet exposant à celui déjà contenu dans :

\[
z_P(q).
\]

Le bon langage est donc :

# INTERACTION DES VALUATIONS PREMIÈRES DANS LE PPCM.

Notre mot « contamination » peut rester comme raccourci de chantier.

Mais la preuve doit parler de valuations.

---

## 27.22 — LE VRAI MIROIR

Nous pouvons représenter un candidat général par son vecteur d’exposants premiers.

Si :

\[
L=
\operatorname{ppcm}
\left(
z_P(p)p^{a-1},
z_P(q)q^{b-1}
\right),
\]

écrivons sa factorisation :

\[
L=\prod_{\ell}\ell^{e_\ell}.
\]

Alors :

\[
L\text{ est un carré}
\]

si et seulement si :

\[
\boxed{
e_\ell\equiv0\pmod2
\quad
\text{pour tout premier }\ell.
}
\]

Voilà notre **combinaison miroir** la plus propre.

Chaque exposant regarde sa parité.

Pair : fermé.

Impair : ouvert.

Le carré parfait est obtenu lorsque toutes les portes se referment simultanément.

---

## 27.23 — LE TEST MINIMAL D’UN NOUVEAU COUPLE \((p,q)\)

Avant d’annoncer une nouvelle famille, nous devrons exiger :

~~~text
1. calculer z_P(p)
2. calculer z_P(q)

3. vérifier le relèvement de p
4. vérifier le relèvement de q

5. factoriser z_P(p)
6. factoriser z_P(q)

7. construire le PPCM symbolique

8. suivre chaque valuation première

9. dériver les conditions de parité

10. tester les plus petits cas

11. chercher volontairement un contre-exemple

12. séparer preuve et antériorité
~~~

Cette procédure transforme notre intuition en moteur de recherche contrôlé.

---

## 27.24 — CONDITIONS D’ABANDON

Une idée doit aussi savoir quand mourir.

Nous abandonnerons une famille candidate si :

- la formule de relèvement supposée échoue ;
- un contre-exemple satisfait toutes les hypothèses annoncées ;
- une simplification du PPCM ignore une valuation ;
- le critère de carré prédit incorrectement un cas ;
- une hypothèse nécessaire n’a pas été déclarée ;
- une preuve dépend d’un dessin plutôt que de l’arithmétique ;
- l’antériorité montre que nous attribuons incorrectement un résultat standard à notre travail.

Abandonner une mauvaise formulation n’est pas perdre la découverte.

C’est la nettoyer.

---

## 27.25 — TABLEAU DE STATUT

À cet instant :

### VÉRIFIÉ PAR CALCUL DIRECT

\[
z_P(1\,203\,930)=1764=42^2.
\]

### DÉRIVÉ SOUS PROPRIÉTÉS STANDARD DE RANG

\[
z_P(3^a7^b)
=
4\cdot3^{\max(a-1,1)}7^{b-1}.
\]

### CARACTÉRISÉ

Le rang précédent est carré si et seulement si :

\[
a\ge3,\quad a\text{ impair},\quad b\text{ impair}.
\]

### TEST COMPUTATIONNEL

30 couples \((a,b)\) testés sur la grille \(1\le a\le6\), \(1\le b\le5\), sans divergence.

### VALIDÉ COMME MÉCANISME

Extension par facteur \(d\) lorsque :

\[
\gcd(d,C)=1
\]

et :

\[
z_P(d)\mid z_P(C).
\]

### CONTRE-EXEMPLES CONSERVÉS

\[
z_P(21)=12
\]

contre une généralisation trop large ;

ajout de 3 ou 7 au noyau contre une extension sans coprimalité ;

ajout de 17 contre une extension où le rang du facteur n’est pas absorbé.

### OUVERT

Générateur général pour couples de premiers.

### OUVERT

Classification de tous les square-ranks Pell.

### OUVERT

Antériorité exacte de notre formulation et de ses sous-familles.

---

## 27.26 — LA PREUVE N’EST PAS UN MOMENT

Nous pensions autrefois qu’une preuve ressemblait à une porte :

~~~text
AVANT = INCONNU
APRÈS = PROUVÉ
~~~

Mais la réalité est plus fine.

Une recherche possède plusieurs couches :

~~~text
IDENTITÉ NUMÉRIQUE
↓
RÉPÉTITION
↓
FORMULE CANDIDATE
↓
CONTRE-TEST
↓
DÉRIVATION
↓
HYPOTHÈSES EXPLICITES
↓
THÉORÈME
↓
ANTÉRIORITÉ
↓
PUBLICATION
↓
RÉPLICATION INDÉPENDANTE
~~~

Un résultat peut être très solide à une couche sans avoir encore franchi la suivante.

Cette distinction ne diminue pas le résultat.

Elle nous dit simplement où nous sommes.

---

## 27.27 — LA MACHINE À TRACES DEVIENT UNE MACHINE À PREUVES

Notre méthode :

~~~text
INTUITION
→ CALCUL
→ CONTRE-TEST
→ PREUVE
→ ANTÉRIORITÉ
→ TRACE DURABLE
~~~

vient de montrer pourquoi chaque étape existe.

Sans calcul, l’intuition flotte.

Sans contre-test, le calcul peut sélectionner uniquement les bons exemples.

Sans preuve, la régularité reste locale.

Sans antériorité, nous ne savons pas ce qui est nouveau.

Sans trace durable, nous ne savons plus exactement ce qui avait été établi.

Le Grand Dévoilement commence donc à changer de nature.

Il ne révèle plus seulement des relations.

# IL RÉVÈLE COMMENT LES RELATIONS DOIVENT ÊTRE JUGÉES.

---

## 27.28 — CE QUE LE SCALPEL A LAISSÉ DEBOUT

Après l’attaque, voici ce qui reste :

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

avec :

\[
r\ge1,\qquad s\ge0.
\]

Et pour le nombre fondateur :

\[
\boxed{
z_P
\left(
130\cdot3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2
}
\]

dans la région où le rang de 130 demeure absorbé, notamment :

\[
r\ge1,\qquad s\ge1.
\]

La formule n’est pas sortie du scalpel plus grande.

Elle en est sortie **plus précise**.

C’est mieux.

---

# FIN DU CHAPITRE 27

Nous avions apporté une belle formule sur la table.

Nous avons essayé de la couper.

Nous avons attaqué sa définition.

Ses puissances premières.

Son PPCM.

Ses parités.

Ses cas limites.

Ses facteurs supplémentaires.

Sa coprimalité.

Ses ambitions.

Et plusieurs choses sont tombées.

L’idée que tout exposant impair suffisait.

L’idée que n’importe quel facteur dont le rang divisait le carré pouvait être ajouté.

L’idée que notre famille décrivait tous les rangs carrés de Pell.

Ces idées étaient trop grandes.

Nous les avons laissées tomber.

Et ce qui resta était plus petit.

Mais beaucoup plus dur.

Une famille exacte.

Des conditions visibles.

Des contre-exemples conservés.

Un mécanisme extensible.

Et une nouvelle machine en train d’apparaître derrière les mathématiques :

# UNE MACHINE QUI NE CHERCHE PAS SEULEMENT DES FORMULES.

# UNE MACHINE QUI CHERCHE LES CONDITIONS SOUS LESQUELLES ELLES SURVIVENT.

---

## Passage au chapitre 28

# LA MACHINE QUI DOIT SE SOUVENIR

> **Une preuve sans mémoire peut être perdue. Une machine sans continuité peut recommencer la même erreur comme si elle ne l’avait jamais vue.**
