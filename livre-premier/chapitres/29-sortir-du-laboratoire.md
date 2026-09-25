# Chapitre 29 — Sortir du laboratoire

**APRÈS L’INTRODUCTION — DIX-NEUVIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** De la preuve interne à la reproduction indépendante  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **UNE DÉCOUVERTE DEVIENT PARTAGEABLE LORSQUE QUELQU’UN QUI N’ÉTAIT PAS LÀ PEUT REPRENDRE LES TRACES, REFAIRE LE CALCUL ET DÉCIDER LUI-MÊME SI ELLE TIENT.**

Jusqu’ici, tout s’était passé dans notre laboratoire.

Nous avions construit.

Mesuré.

Corrigé.

Cassé nos propres hypothèses.

Conservé les échecs.

Versionné les claims.

Créé des checkpoints.

Appris à rejouer l’histoire.

Mais une preuve qui ne peut vivre qu’à l’intérieur de notre propre atelier possède encore une faiblesse.

Elle dépend de nous.

De notre mémoire.

De notre code.

De notre façon d’expliquer.

De notre présence.

Alors une nouvelle porte s’ouvre.

# SORTIR DU LABORATOIRE.

Pas pour convaincre.

Pas pour impressionner.

Pour permettre à quelqu’un d’autre de vérifier.

---

## 29.1 — LA QUESTION CHANGE ENCORE

Dans le laboratoire, nous demandions :

> **Est-ce que le résultat tient ?**

À l’extérieur, la question devient :

> **Une autre personne peut-elle le reconstruire sans information cachée ?**

La différence est énorme.

Une formule peut être correcte.

Un calcul peut être correct.

Un test peut passer.

Mais si le protocole de reproduction dépend d’une étape implicite, d’un fichier absent ou d’un paramètre non documenté, le résultat reste difficile à vérifier.

Alors nous introduisons une nouvelle exigence :

# AUCUNE ÉTAPE PRIVÉE DANS UNE PREUVE PUBLIQUE.

---

## 29.2 — LE PAQUET DE REPRODUCTION

Nous pouvons définir un artefact :

# REPRODUCTION_PACKAGE_V1

Il doit contenir au minimum :

~~~text
README
CLAIM
DEFINITIONS
ASSUMPTIONS
FORMULAS
SOURCE_CODE
TESTS
RAW_RESULTS
COUNTEREXAMPLES
ENVIRONMENT
VERSION
LICENSE
CITATION
~~~

Chaque élément répond à une question.

Le lecteur ne devrait jamais avoir à deviner.

---

## 29.3 — README : OÙ SUIS-JE ?

Le README n’est pas un résumé décoratif.

Il doit permettre à quelqu’un d’ouvrir le paquet et de comprendre immédiatement :

~~~text
QU’EST-CE QUI EST TESTÉ ?
POURQUOI ?
COMMENT ?
AVEC QUEL CODE ?
QUEL RÉSULTAT EST ATTENDU ?
QUEL RÉSULTAT INVALIDERAIT LE CLAIM ?
~~~

Une bonne première page réduit l’ambiguïté avant même le premier calcul.

---

## 29.4 — CLAIM : UNE PHRASE QUI PEUT ÊTRE FAUSSE

Un claim scientifique utile doit pouvoir être réfuté.

Par exemple :

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
r\ge1,\qquad s\ge0.
\]

Cette phrase est testable.

Elle dit exactement quel objet, quel domaine et quel résultat.

Si quelqu’un trouve un couple dans le domaine pour lequel l’égalité échoue, le claim est faux dans sa forme actuelle.

C’est une force.

Pas une faiblesse.

---

## 29.5 — DÉFINITIONS : AUCUN SYMBOLE ORPHELIN

Avant toute preuve, nous devons définir :

\[
P_0=0,
\]

\[
P_1=1,
\]

\[
P_{n+1}=2P_n+P_{n-1},
\]

et :

\[
z_P(m)
=
\min\{n\ge1:m\mid P_n\}.
\]

Nous devons également définir :

- PPCM ;
- valuation première si elle est utilisée ;
- carré parfait ;
- domaine des paramètres ;
- notion de facteur compatible ;
- statut des tests informatiques.

Un symbole non défini est une porte vers plusieurs interprétations.

---

## 29.6 — LES HYPOTHÈSES DOIVENT ÊTRE DEVANT LA FORMULE

Avant :

\[
z_P(dC)=z_P(C),
\]

nous devons écrire :

\[
\gcd(d,C)=1
\]

et :

\[
z_P(d)\mid z_P(C).
\]

Sinon, quelqu’un pourrait essayer :

\[
d=3
\]

sur :

\[
C=3^3 7^3
\]

et obtenir :

\[
5292
\]

au lieu de :

\[
1764.
\]

Ce n’est pas la formule qui aurait échoué.

Ce serait la documentation.

---

## 29.7 — LE CODE N’EST PAS LA PREUVE

Un programme peut calculer :

\[
z_P(1\,203\,930)=1764.
\]

Cela constitue une vérification computationnelle.

Mais le programme, à lui seul, ne remplace pas la dérivation mathématique.

Nous voulons deux pistes :

### PISTE A — ANALYTIQUE

Factorisations.

Relèvement.

PPCM.

Parité des valuations.

### PISTE B — COMPUTATIONNELLE

Calcul direct du premier indice divisant.

Tests de grille.

Contre-exemples.

Les deux doivent converger.

---

## 29.8 — LE CODE DOIT ÊTRE PETIT AVANT D’ÊTRE INTELLIGENT

Pour vérifier un rang d’apparition, un programme minimal suffit.

Conceptuellement :

~~~text
P0 = 0
P1 = 1

for n = 1,2,3,...
    compute Pn modulo m
    if Pn == 0
        return n
~~~

Nous n’avons pas besoin d’une énorme infrastructure pour établir un résultat élémentaire.

Une implémentation courte possède un avantage :

# ELLE EST PLUS FACILE À AUDITER.

L’optimisation vient après la correction.

---

## 29.9 — CALCULER MODULO m

Les nombres de Pell deviennent rapidement énormes.

Mais pour savoir si :

\[
m\mid P_n,
\]

nous n’avons pas besoin de stocker \(P_n\) au complet.

Il suffit de conserver :

\[
P_n\bmod m.
\]

La récurrence devient :

\[
r_{n+1}
=
(2r_n+r_{n-1})\bmod m.
\]

Ainsi :

\[
0\le r_n<m.
\]

Le calcul direct devient beaucoup plus simple à reproduire.

---

## 29.10 — LA SORTIE BRUTE DOIT ÊTRE CONSERVÉE

Un rapport final peut dire :

\[
z_P(9261)=1764.
\]

Mais le paquet peut aussi conserver :

~~~text
MODULUS = 9261
FIRST_ZERO_INDEX = 1764
PREVIOUS_INDEX_ZERO = false
STATUS = PASS
~~~

Pour les tests de famille :

~~~text
a,b,m,predicted_rank,direct_rank,is_square,status
~~~

La donnée brute ne remplace pas l’analyse.

Elle permet de la contrôler.

---

## 29.11 — LES CONTRE-EXEMPLES DOIVENT ÊTRE PUBLIÉS AVEC LE RÉSULTAT

Nous ne voulons pas cacher :

\[
z_P(21)=12.
\]

Au contraire.

Ce contre-exemple explique pourquoi :

\[
r\ge1
\]

est nécessaire.

Nous devons également conserver :

\[
z_P(3^4 7^3)=5292
\]

comme preuve que la coprimalité ne peut pas être retirée de l’extension.

Et :

\[
z_P(17\cdot9261)=3528
\]

comme exemple d’un facteur dont le rang n’est pas absorbé.

Les contre-exemples racontent les frontières.

---

## 29.12 — UNE BONNE PUBLICATION DIT AUSSI CE QU’ELLE NE PROUVE PAS

Le paquet doit comporter une section :

# LIMITATIONS

Par exemple :

~~~text
NOT CLAIMED:
- classification of all Pell square ranks
- physical law
- universal prime-pair theorem
- bibliographic novelty unless prior-art review completed
~~~

Cette section empêche une interprétation future d’élargir le résultat au-delà de son domaine.

---

## 29.13 — LA REPRODUCTIBILITÉ

Nous pouvons distinguer trois niveaux.

### RÉPÉTABILITÉ

Même équipe.

Même environnement.

Même méthode.

Résultat reproduit.

### REPRODUCTIBILITÉ

Même claim.

Nouvelle exécution.

Environnement potentiellement différent.

Résultat retrouvé.

### RÉPLICATION INDÉPENDANTE

Une autre personne ou équipe construit sa propre vérification suffisamment indépendante.

Elle décide elle-même si le claim tient.

Plus nous avançons dans cette chaîne, moins le résultat dépend de nous.

---

## 29.14 — LE FICHIER ENVIRONMENT

Un programme qui dépend d’un environnement particulier doit le dire.

Nous pouvons conserver :

~~~text
LANGUAGE = Python
PYTHON_VERSION = ...
DEPENDENCIES = ...
OS = ...
ARCHITECTURE = ...
~~~

Pour un calcul minimal, moins il y a de dépendances, mieux c’est.

Idéalement :

~~~text
DEPENDENCIES = STANDARD_LIBRARY_ONLY
~~~

si le test peut réellement être écrit ainsi.

Une reproduction doit distinguer le résultat mathématique de la configuration accidentelle de la machine.

---

## 29.15 — LE TEST SENTINELLE PUBLIC

Avant les grands tests :

~~~text
z_P(3) = 4
z_P(7) = 6
z_P(21) = 12
z_P(189) = 36
z_P(9261) = 1764
~~~

Si ces valeurs échouent, inutile d’aller plus loin.

Le vérificateur sait immédiatement que son implémentation ou sa définition ne correspond pas à la nôtre.

---

## 29.16 — LE TEST DE FAMILLE

Une première reproduction peut explorer :

\[
1\le a\le A
\]

et :

\[
1\le b\le B.
\]

Pour chaque couple :

1. calculer \(m=3^a7^b\) ;
2. calculer le rang direct ;
3. calculer le rang prédit ;
4. comparer ;
5. tester si le rang est carré ;
6. comparer au critère de parité.

Un rapport peut ensuite dire :

~~~text
TOTAL_CASES
FORMULA_MATCHES
FORMULA_MISMATCHES
SQUARE_PREDICTIONS
SQUARE_MISMATCHES
~~~

Le nombre de succès seul ne suffit pas.

Il faut publier aussi le nombre d’échecs.

---

## 29.17 — LE TEST NÉGATIF

Nous voulons volontairement des cas qui doivent échouer.

Par exemple :

\[
(a,b)=(1,1)
\]

doit donner :

\[
12
\]

et non un carré.

\[
(a,b)=(3,2)
\]

doit donner :

\[
252
\]

et non un carré.

\[
(a,b)=(4,3)
\]

doit donner :

\[
5292.
\]

Un test qui vérifie seulement les cas positifs est incomplet.

---

## 29.18 — LE FICHIER CLAIMS

Le paquet peut contenir un fichier lisible par machine :

~~~text
CLAIM_001
TYPE = IDENTITY
STATUS = VERIFIED_BY_DIRECT_COMPUTATION
STATEMENT = z_P(1203930)=1764

CLAIM_002
TYPE = FACTORIZATION
STATUS = VERIFIED
STATEMENT = 1764=42^2

CLAIM_003
TYPE = FAMILY
STATUS = DERIVED
DOMAIN = r>=1,s>=0

CLAIM_004
TYPE = NOVELTY
STATUS = BIBLIOGRAPHY_PENDING
~~~

Le lecteur sait immédiatement quel niveau de preuve est attaché à chaque phrase.

---

## 29.19 — L’ANTÉRIORITÉ EST UNE EXPÉRIENCE DIFFÉRENTE

Trouver une identité mathématique et déterminer si elle a déjà été publiée sont deux travaux différents.

Le premier demande :

> Est-ce vrai ?

Le second :

> Est-ce nouveau ?

Nous ne devons jamais répondre au second avec les outils du premier.

Un million de tests réussis ne prouvent pas qu’un résultat n’a jamais été publié auparavant.

L’antériorité exige une recherche bibliographique séparée.

---

## 29.20 — LE NOM DE L’AUTEUR

Pour le travail que nous préparons, le nom d’auteur doit être conservé de manière cohérente :

# GABRIEL ST-PIERRE

Le nom du projet peut rester :

# BRUTUS–PELL SQUARE-RANK RELATION

Mais le projet et l’auteur ne sont pas la même chose.

Le dépôt, le rapport, l’archive et les métadonnées de citation doivent éviter de mélanger pseudonyme, nom du projet et nom de l’auteur.

La provenance humaine fait aussi partie de la continuité.

---

## 29.21 — LE DOI

Un DOI peut fournir une référence persistante vers une version archivée d’un travail.

Mais il faut graver une règle :

# DOI ≠ VALIDATION SCIENTIFIQUE.

Un DOI permet de citer.

Il ne transforme pas automatiquement une hypothèse en théorème.

Il ne remplace pas une revue par les pairs.

Il ne remplace pas une reproduction indépendante.

Il donne au résultat une adresse durable.

C’est déjà très utile.

---

## 29.22 — ZENODO COMME COUCHE D’ARCHIVE

Dans notre workflow, une archive comme Zenodo peut recevoir une version figée d’un paquet de reproduction.

Par exemple :

~~~text
BRUTUS_PELL_SQUARE_RANK_V1
├── README.md
├── paper.md
├── claim.json
├── pell_rank.py
├── test_family.py
├── raw_results.csv
├── counterexamples.csv
├── environment.txt
├── CITATION.cff
└── LICENSE
~~~

La plateforme d’archive n’est pas la preuve.

Elle conserve la version de la preuve que nous présentons.

---

## 29.23 — FIGER UNE VERSION

Une publication doit correspondre à un état précis.

Supposons :

~~~text
VERSION = 1.0.0
GIT_COMMIT = abcdef...
ARCHIVE_DATE = ...
~~~

Si nous corrigeons ensuite une erreur, nous créons une nouvelle version.

Nous ne réécrivons pas silencieusement l’ancienne.

Ainsi :

~~~text
V1.0.0 → ARCHIVED
V1.0.1 → CORRECTION
V1.1.0 → EXTENDED FAMILY
~~~

L’histoire scientifique reste visible.

---

## 29.24 — CORRECTION OU NOUVEAU RÉSULTAT

Supposons qu’une faute dise :

\[
r\ge0
\]

au lieu de :

\[
r\ge1.
\]

Cette correction change mathématiquement le domaine.

Le journal de version doit préciser :

~~~text
WHAT CHANGED
WHY
DOES IT CHANGE THE CLAIM?
DOES IT CHANGE THE PROOF?
DOES IT CHANGE THE DATA?
~~~

Le lecteur doit savoir si la version précédente reste valide.

---

## 29.25 — LE HASH DU PAQUET

Pour une archive, nous pouvons calculer un hash de chaque artefact.

~~~text
README.md        → HASH_A
pell_rank.py     → HASH_B
raw_results.csv  → HASH_C
paper.pdf        → HASH_D
~~~

Puis un manifeste :

~~~text
MANIFEST.sha256
~~~

L’objectif est de détecter toute modification entre la version testée et la version partagée.

Le hash ne prouve pas la science.

Il protège l’intégrité des fichiers.

---

## 29.26 — LE RAPPORT DE REPRODUCTION

Une personne extérieure devrait pouvoir produire quelque chose comme :

~~~text
REPRODUCTION_REPORT

CLAIM:
z_P(3^(2r+1)7^(2s+1))
=
(2*3^r*7^s)^2

IMPLEMENTATION:
independent

BASE SENTINELS:
5/5 PASS

GRID:
500 cases

FORMULA MATCH:
500/500

NEGATIVE CASES:
PASS

COUNTEREXAMPLES:
REPRODUCED

NOVELTY:
NOT ASSESSED

CONCLUSION:
COMPUTATIONAL REPRODUCTION PASS
~~~

Cette personne n’a pas besoin de partager notre vision.

Elle doit seulement pouvoir vérifier.

---

## 29.27 — LE RAPPORT D’ÉCHEC EST AUSSI UN SUCCÈS SCIENTIFIQUE

Supposons qu’un tiers obtienne :

~~~text
CASE:
r=14
s=9

PREDICTED:
...

DIRECT:
...

STATUS:
MISMATCH
~~~

Ce résultat est précieux.

Nous voulons l’entrée, le code, la version, la sortie et le détail de la divergence.

Si le contre-exemple est valide, nous corrigeons la formule.

La publication n’est pas un monument qu’il faut défendre.

C’est une proposition exposée à l’examen.

---

## 29.28 — SORTIR DU LABORATOIRE SIGNIFIE PERDRE LE CONTRÔLE

Tant que le résultat reste chez nous, nous pouvons décider comment il est présenté.

À l’extérieur, quelqu’un peut le critiquer.

Le reformuler.

Le casser.

Trouver un cas que nous n’avions pas vu.

Trouver un article antérieur.

Construire une preuve meilleure.

C’est exactement le but.

Une preuve qui ne peut survivre qu’à condition que personne ne la touche n’est pas encore une preuve solide.

---

## 29.29 — LE DROIT DE VÉRIFIER

Notre règle devient :

# LE LECTEUR A LE DROIT DE NE PAS NOUS CROIRE.

Il doit pouvoir :

- télécharger ;
- lire ;
- exécuter ;
- recalculer ;
- comparer ;
- contredire ;
- citer ;
- reproduire.

Ce droit impose des responsabilités au créateur.

Nous devons donner suffisamment d’information pour rendre le doute productif.

---

## 29.30 — CE QUI DOIT SORTIR, ET CE QUI PEUT RESTER PRIVÉ

La reproductibilité ne signifie pas publier n’importe quoi.

Un paquet scientifique n’a pas besoin de contenir mots de passe, tokens, secrets d’infrastructure, données personnelles ou fichiers sans rapport avec le claim.

Nous publions ce qui est nécessaire à la reproduction du résultat.

Pas notre vie entière.

Principe :

# MINIMUM SUFFISANT POUR REPRODUIRE.

---

## 29.31 — LA PREUVE PUBLIQUE DOIT ÊTRE PLUS PETITE QUE LE LABORATOIRE

Notre laboratoire peut contenir des milliers de notes, images, essais, idées abandonnées, prototypes, conversations et chemins morts.

Le paquet public doit être plus petit.

Il doit extraire :

~~~text
DÉFINITION
↓
CLAIM
↓
HYPOTHÈSES
↓
PREUVE
↓
CODE
↓
TESTS
↓
DONNÉES
↓
CONTRE-EXEMPLES
↓
LIMITES
↓
CITATION
~~~

Le laboratoire raconte comment nous avons cherché.

Le paquet de reproduction montre comment vérifier.

---

## 29.32 — NOTRE PREMIER PAQUET POSSIBLE

Pour la Brutus–Pell Square-Rank Relation :

~~~text
BRUTUS_PELL_SQUARE_RANK_V1

AUTHOR
Gabriel St-Pierre

CLAIM A
z_P(1203930)=1764=42^2

CLAIM B
z_P(3^(2r+1)7^(2s+1))
=
(2*3^r*7^s)^2
for r>=1,s>=0

CLAIM C
compatible coprime factors preserve the rank
when their ranks divide the existing square

COUNTEREXAMPLES
21
3^4*7^3
17*9261

STATUS
mathematical derivation + computational checks

NOVELTY
bibliography pending
~~~

Nous avons maintenant suffisamment de structure pour que ce paquet devienne réel.

---

## 29.33 — DE LA BIBLE AU PAPIER

La Bible de Brutus possède un rôle différent du papier scientifique.

La Bible peut raconter la découverte, les erreurs, les images, le chemin intellectuel et la transformation du projet.

Le papier doit condenser :

- définition ;
- proposition ou théorème selon le niveau établi ;
- démonstration ;
- tests ;
- limites ;
- références.

Les deux documents peuvent raconter la même découverte.

Mais ils ne remplissent pas la même fonction.

---

## 29.34 — LE MOMENT OÙ « NOUS » DEVIENT « VOUS POUVEZ VÉRIFIER »

Jusqu’ici, nous écrivions :

> **Nous avons calculé.**

À la sortie du laboratoire, la phrase la plus importante devient :

> **Vous pouvez refaire le calcul.**

La découverte cesse d’être un récit privé.

Elle devient une invitation à la vérification.

---

## 29.35 — LE TEST ULTIME DE DOCUMENTATION

Prenons une personne qui ne connaît ni TopBrutus, ni Antmux, ni la Bible, ni nos nombres fondateurs.

Donnons-lui uniquement le paquet.

Si elle peut reconstruire :

\[
P_n,
\]

\[
z_P(m),
\]

\[
z_P(1\,203\,930)=1764,
\]

et :

\[
z_P
\left(
3^{2r+1}7^{2s+1}
\right)
=
\left(
2\cdot3^r7^s
\right)^2,
\]

alors notre documentation a réussi.

Si elle doit demander ce que nous voulions dire, nous avons trouvé un trou.

---

## 29.36 — LA PUBLICATION EST UNE NOUVELLE FORME DE CHECKPOINT

Au chapitre 28, le checkpoint permettait à la machine de reprendre.

Ici, une publication figée permet à la communauté de reprendre.

Nous pouvons voir une archive versionnée comme :

\[
C_{\text{public}}.
\]

Elle dit :

> Voilà exactement ce que nous affirmions à cette date, avec ces preuves et ces limites.

Les versions futures peuvent avancer.

Le passé reste vérifiable.

---

## 29.37 — LE LABORATOIRE N’EST PAS ABANDONNÉ

Sortir du laboratoire ne signifie pas terminer la recherche.

Au contraire.

La publication crée de nouvelles entrées.

Quelqu’un peut rapporter :

~~~text
NEW COUNTEREXAMPLE
~~~

ou :

~~~text
PRIOR ART FOUND
~~~

ou :

~~~text
INDEPENDENT PROOF
~~~

ou :

~~~text
GENERALIZATION
~~~

Ces éléments peuvent revenir au laboratoire.

La boucle devient :

~~~text
LAB
↓
PACKAGE
↓
PUBLICATION
↓
EXTERNAL TEST
↓
FEEDBACK
↓
LAB
~~~

La sortie n’est pas une fin.

C’est une nouvelle entrée.

---

## 29.38 — LA PROVENANCE JUSQU’AU MONDE EXTÉRIEUR

Notre chaîne complète devient :

~~~text
INTUITION
↓
DEFINITION
↓
CALCULATION
↓
COUNTERTEST
↓
DERIVATION
↓
CHECKPOINT
↓
REPRODUCTION PACKAGE
↓
ARCHIVE
↓
DOI / VERSION
↓
INDEPENDENT VERIFICATION
↓
FEEDBACK
~~~

Aucune connexion invisible.

Même à l’extérieur.

---

## 29.39 — CE QUE NOUS SOMMES PRÊTS À DIRE

### CALCUL

\[
z_P(1\,203\,930)=1764=42^2.
\]

### FAMILLE DÉRIVÉE

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

dans le domaine annoncé.

### TESTS

Les cas positifs et négatifs testés sont compatibles avec cette dérivation.

### LIMITES

Nous ne prétendons pas encore classifier tous les rangs carrés de Pell.

### ANTÉRIORITÉ

La nouveauté bibliographique doit être établie séparément.

### AUTEUR DU TRAVAIL

**Gabriel St-Pierre.**

Voilà un résultat assez précis pour être exposé.

---

# FIN DU CHAPITRE 29

Nous avions commencé dans une pièce fermée.

Un tableau.

Des nombres.

Une horloge.

Des chemins.

Des erreurs.

Des poussières.

Puis une suite.

Puis un rang.

Puis un carré.

Puis une famille.

Puis un scalpel.

Puis une mémoire.

Et maintenant, la porte du laboratoire s’ouvre.

Nous ne sortons pas en disant :

# « CROYEZ-NOUS. »

Nous sortons avec un paquet.

Un claim.

Un code.

Des données.

Des contre-exemples.

Une version.

Une provenance.

Et une phrase beaucoup plus forte :

# « VOICI EXACTEMENT CE QUE NOUS AVONS FAIT. »

# « REFAITES-LE. »

Si le résultat tient chez quelqu’un qui n’était pas là, alors quelque chose a changé.

La découverte ne dépend plus seulement de notre histoire.

Elle possède désormais une histoire que d’autres peuvent vérifier.

Et lorsque la porte du laboratoire se referme derrière nous, nous regardons enfin la table complète.

Les nombres.

Les chemins.

Les cycles.

La mémoire.

Les preuves.

Les portes.

Cette fois, ce n’est plus un morceau que nous allons regarder.

# C’EST LA CARTE.

---

## Passage au chapitre 30

# LA CARTE APPARAÎT

> **Pendant vingt-neuf chapitres, nous pensions assembler des pièces. Au trentième, nous allons regarder ce que leur ensemble dessine réellement — sans confondre la carte avec le territoire.**
