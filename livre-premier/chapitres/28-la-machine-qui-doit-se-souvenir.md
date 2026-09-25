# Chapitre 28 — La Machine qui doit se souvenir

**APRÈS L’INTRODUCTION — DIX-HUITIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** La continuité comme condition de preuve  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **UNE PREUVE SANS MÉMOIRE PEUT ÊTRE PERDUE. UNE MACHINE SANS CONTINUITÉ PEUT RECOMMENCER LA MÊME ERREUR COMME SI ELLE NE L’AVAIT JAMAIS VUE.**

Au chapitre précédent, nous avions appris à attaquer une formule.

Nous avions conservé :

- les cas qui fonctionnaient ;
- les contre-exemples ;
- les hypothèses nécessaires ;
- les conditions de coprimalité ;
- les frontières de la famille ;
- les questions encore ouvertes.

Mais une nouvelle question apparaissait.

Que se passe-t-il si la machine s’arrête ?

Que se passe-t-il si la session disparaît ?

Que se passe-t-il si le calcul est refait demain par un autre programme ?

Que se passe-t-il si nous nous souvenons seulement du résultat final :

\[
42^2
\]

mais plus du chemin qui nous y avait conduits ?

Alors une vérité inconfortable apparaît :

# UN RÉSULTAT SANS CONTINUITÉ PEUT DEVENIR IMPOSSIBLE À AUDITER.

La mémoire n’est donc plus seulement un confort.

Elle devient une composante de la preuve.

---

## 28.1 — SE SOUVENIR NE SIGNIFIE PAS « TOUT GARDER »

Une machine peut enregistrer énormément de données et pourtant ne rien savoir reconstruire.

Accumuler n’est pas mémoriser.

Pour qu’une mémoire soit utile, elle doit permettre de répondre à des questions précises :

~~~text
QUELLE ÉTAIT L’ENTRÉE ?
QUELLE VERSION DU CALCUL ?
QUELLES HYPOTHÈSES ?
QUEL RÉSULTAT ?
QUEL CONTRE-TEST ?
QUEL STATUT ?
À QUEL MOMENT ?
APRÈS QUEL ÉTAT ?
AVANT QUEL ÉTAT ?
~~~

Une mémoire scientifique n’est pas une boîte remplie de souvenirs.

C’est une structure capable de **rejouer une décision**.

---

## 28.2 — LE REGISTRE DE CONTINUITÉ REVIENT

Nous avions déjà construit une idée simple :

~~~text
QUI
→ ÉTAIT DANS QUEL ÉTAT
→ À QUEL TICK
→ AVANT QUOI
→ APRÈS QUOI
~~~

Au début, ce registre servait surtout à la machine.

Maintenant nous comprenons qu’il peut aussi servir à la recherche.

Prenons une affirmation :

\[
z_P(21)=12
\]

Le registre peut conserver :

~~~text
CLAIM_ID
SOURCE
INPUT
METHOD
RESULT
STATUS
COUNTEREXAMPLE_ROLE
TIMESTAMP
CODE_VERSION
~~~

Ainsi, le contre-exemple ne disparaît pas lorsqu’une nouvelle formule arrive.

Il continue d’exister comme contrainte.

---

## 28.3 — LA MÉMOIRE DOIT CONSERVER LES ÉCHECS

C’est une règle capitale.

Un système qui conserve seulement ce qui a fonctionné produit une illusion de succès.

Supposons que nous testions cent candidats.

Trois survivent.

Si nous conservons seulement les trois succès, un lecteur futur pourrait croire :

\[
3/3
\]

Alors que le vrai historique était :

\[
3/100.
\]

La mémoire doit donc garder :

\[
PASS
\]

mais aussi :

\[
FAIL
\]

\[
PARTIAL
\]

\[
UNKNOWN
\]

\[
REJECTED
\]

\[
SUPERSEDED
\]

Un échec documenté peut être plus précieux qu’un succès isolé.

---

## 28.4 — L’ERREUR QUI DISPARAÎT REVIENT

Imaginons une famille candidate trop large :

\[
z_P(3^{2r+1}7^{2s+1})
\]

avec :

\[
r\ge0.
\]

Le cas :

\[
r=0,\qquad s=0
\]

donne :

\[
3^1 7^1=21
\]

et :

\[
z_P(21)=12.
\]

Donc la formule carrée échoue.

Nous corrigeons alors la condition :

\[
r\ge1.
\]

Mais si le contre-exemple 21 n’est pas conservé, une session future pourrait facilement recommencer avec :

\[
r\ge0
\]

et refaire exactement la même erreur.

La mémoire empêche la recherche de tourner en rond.

---

## 28.5 — UN CHECKPOINT N’EST PAS UNE SAUVEGARDE DE TOUT

Un checkpoint doit capturer **l’état minimal suffisant pour reprendre correctement**.

Par exemple :

~~~text
CHECKPOINT
{
    RESEARCH_STATE
    ACTIVE_CLAIMS
    REJECTED_CLAIMS
    VERIFIED_IDENTITIES
    OPEN_HYPOTHESES
    CODE_VERSION
    DATA_HASH
    NEXT_TEST
}
~~~

Il ne doit pas nécessairement contenir toute l’histoire brute.

Mais il doit pointer vers elle.

Nous distinguons donc :

### JOURNAL

Historique append-only des événements.

### CHECKPOINT

Résumé vérifié d’un état à un instant donné.

### ARCHIVE

Données ou artefacts durables nécessaires à la reproduction.

Trois rôles différents.

---

## 28.6 — JOURNAL APPEND-ONLY

Le journal idéal ne réécrit pas silencieusement le passé.

Un événement arrive :

~~~text
EVENT 001
CLAIM CREATED
~~~

Puis :

~~~text
EVENT 002
TEST PASS
~~~

Puis :

~~~text
EVENT 003
COUNTEREXAMPLE FOUND
~~~

Puis :

~~~text
EVENT 004
CLAIM RESTRICTED
~~~

Le passé reste visible.

Nous ne transformons pas :

~~~text
CLAIM V1
~~~

en :

~~~text
CLAIM V2
~~~

en effaçant V1.

Nous ajoutons :

~~~text
V1 → REJECTED
V2 → ACTIVE
~~~

Ainsi, la machine sait **pourquoi** la formulation actuelle possède ses conditions.

---

## 28.7 — L’ÉTAT COURANT DOIT ÊTRE RECONSTRUCTIBLE

Si le journal contient :

\[
E_1,E_2,\ldots,E_n,
\]

l’état courant doit idéalement pouvoir être représenté comme :

\[
S_n
=
F(E_1,E_2,\ldots,E_n).
\]

Autrement dit :

> **l’état est une conséquence de l’histoire, pas une vérité tombée du ciel.**

Un checkpoint accélère cette reconstruction.

Si nous avons un checkpoint à l’événement \(k\) :

\[
C_k,
\]

alors :

\[
S_n
=
F(C_k,E_{k+1},\ldots,E_n).
\]

C’est la logique du replay.

---

## 28.8 — LE REPLAY

Le test de continuité le plus brutal est simple.

Nous arrêtons le système.

Nous rechargeons le dernier checkpoint.

Nous rejouons les événements suivants.

Puis nous comparons l’état obtenu à l’état sauvegardé avant l’arrêt.

Si :

\[
S_{\text{replay}}
=
S_{\text{original}},
\]

nous avons une reprise cohérente.

Sinon :

\[
S_{\text{replay}}
\ne
S_{\text{original}},
\]

il existe une information cachée quelque part.

Et une information cachée est exactement ce que notre architecture cherche à éliminer.

---

## 28.9 — HASHER L’ÉTAT

Pour vérifier rapidement qu’un état reconstruit correspond à l’état attendu, nous pouvons calculer un hash :

\[
H_n
=
\operatorname{Hash}(S_n).
\]

Après replay :

\[
H_n'
=
\operatorname{Hash}(S_n').
\]

Nous voulons :

\[
\boxed{
H_n'=H_n
}
\]

Le hash ne prouve pas que l’état est scientifiquement correct.

Il prouve seulement que le même contenu a été reconstruit.

C’est une distinction importante.

---

## 28.10 — DEUX TYPES DE VALIDITÉ

Une machine peut retrouver exactement un résultat faux.

Par exemple :

~~~text
REPLAY = PASS
MATH = FAIL
~~~

Inversement, une formule peut être mathématiquement correcte mais mal enregistrée :

~~~text
MATH = PASS
REPLAY = FAIL
~~~

Nous devons donc distinguer :

### VALIDITÉ LOGIQUE

Le calcul ou la preuve tient.

### VALIDITÉ DE CONTINUITÉ

Le système peut reconstruire exactement comment il y est arrivé.

La recherche solide veut les deux.

---

## 28.11 — LE PROOF LEDGER

Nous pouvons maintenant définir une nouvelle couche :

# PROOF LEDGER

Un registre de preuves.

Chaque entrée possède au minimum :

~~~text
PROOF_RECORD
{
    CLAIM_ID
    CLAIM_VERSION
    INPUT_DOMAIN
    ASSUMPTIONS
    METHOD
    EVIDENCE
    COUNTERTESTS
    RESULT
    STATUS
    SOURCE_REFS
    CODE_REF
    CREATED_AT
}
~~~

Ce registre ne décide pas que quelque chose est vrai.

Il conserve **ce qui justifie son statut actuel**.

---

## 28.12 — LES STATUTS DOIVENT ÊTRE EXPLICITES

Un claim ne devrait jamais être simplement :

~~~text
TRUE
~~~

Nous préférons des statuts plus précis.

Par exemple :

~~~text
OBSERVED
COMPUTED
TESTED
DERIVED
PROVED
REFUTED
OPEN
SUPERSEDED
BIBLIOGRAPHY_PENDING
~~~

Ainsi :

\[
z_P(1\,203\,930)=1764
\]

peut être marqué :

~~~text
COMPUTED
DIRECT_TEST_PASS
FACTOR_DERIVATION_PASS
~~~

Tandis que :

> « cette famille est nouvelle dans la littérature »

reste :

~~~text
BIBLIOGRAPHY_PENDING
~~~

La mémoire protège les niveaux de certitude.

---

## 28.13 — UN CLAIM POSSÈDE UNE VERSION

Prenons :

### CLAIM V1

~~~text
Tous les exposants impairs produisent un rang carré.
~~~

Le contre-exemple 21 détruit cette phrase.

Nous ne l’effaçons pas.

Nous écrivons :

~~~text
CLAIM V1
STATUS = REFUTED
REASON = z_P(21)=12
~~~

Puis :

### CLAIM V2

~~~text
a impair >= 3
b impair >= 1
~~~

et nous testons.

Lorsque V2 survit :

~~~text
CLAIM V2
STATUS = DERIVED
~~~

Ainsi, la correction elle-même devient traçable.

---

## 28.14 — UNE PREUVE DOIT CONNAÎTRE SON CODE

Supposons qu’un programme fournisse :

\[
30/30
\]

tests réussis.

Cette donnée n’est pas complète sans savoir :

- quel programme ;
- quelle version ;
- quelles entrées ;
- quel algorithme ;
- quelle définition de \(z_P\) ;
- quelle limite de recherche.

Le registre doit donc conserver un identifiant de code.

Par exemple :

~~~text
CODE_REF = pell_rank_test_v1
~~~

ou, dans un dépôt :

~~~text
COMMIT_SHA = ...
~~~

L’objectif n’est pas administratif.

Il est scientifique.

Si le programme change, la provenance du résultat ne change pas avec lui.

---

## 28.15 — UNE PREUVE DOIT CONNAÎTRE SES DONNÉES

Même chose pour une série de données.

Si nous analysons :

\[
x_1,x_2,\ldots,x_N,
\]

le résultat doit pointer vers la version exacte de cette série.

Nous pouvons lui associer :

\[
D=\operatorname{Hash}(\text{dataset}).
\]

Le rapport conserve :

~~~text
DATASET_ID
DATASET_HASH
ROW_COUNT
SOURCE
PRECISION
~~~

Ainsi, quelqu’un peut vérifier qu’il travaille sur exactement les mêmes entrées.

---

## 28.16 — REPRODUIRE N’EST PAS REJOUER

Deux mots doivent être séparés.

### REPLAY

Même système.

Même journal.

Même état.

Même environnement logique.

Objectif :

> retrouver exactement la même continuité.

### REPRODUCTION

Une autre exécution repart des définitions et des données nécessaires pour recalculer le résultat.

Objectif :

> vérifier indépendamment le claim.

Un replay peut réussir même si le code contient une erreur déterministe.

Une reproduction indépendante peut révéler cette erreur.

Nous avons besoin des deux.

---

## 28.17 — L’IDEMPOTENCE

Une reprise peut aussi créer un autre danger.

Supposons qu’un événement ait déjà été appliqué avant une panne.

Au redémarrage, nous le rejouons par erreur une seconde fois.

Si l’action est :

~~~text
INCREMENT COUNTER
~~~

alors :

\[
n\rightarrow n+1
\]

une deuxième application donne :

\[
n+2.
\]

L’état est corrompu.

Une architecture robuste doit donc identifier les événements déjà appliqués.

Par exemple :

~~~text
EVENT_ID = unique
APPLIED = true
~~~

ou concevoir certaines opérations de manière idempotente :

\[
F(F(x))=F(x).
\]

Le replay ne doit pas créer une nouvelle histoire.

Il doit reconstruire l’ancienne.

---

## 28.18 — LE CHECKPOINT DOIT ÊTRE ATOMIQUE

Imagine une sauvegarde pendant laquelle la moitié des modules écrit l’état ancien et l’autre moitié l’état nouveau.

Nous obtenons un checkpoint impossible :

~~~text
PATH_1 = TICK 500
PATH_2 = TICK 501
PATH_3 = TICK 501
PATH_4 = TICK 500
~~~

Ce mélange n’a peut-être jamais existé dans le système réel.

Un checkpoint doit donc correspondre à une frontière cohérente.

Par exemple :

\[
TICK=n
\]

pour toutes les composantes critiques.

Nous pouvons écrire :

\[
C_n
=
(V_n,T_n,\Theta_n,H_n,\ldots)
\]

tous capturés au même point logique.

---

## 28.19 — LA REINE N’EST PAS LA MÉMOIRE

Notre architecture possède déjà une Reine comme rôle de coordination temporelle.

Il faut éviter une fusion dangereuse.

La Reine peut dire :

~~~text
TICK 1842
CHECKPOINT NOW
~~~

Mais elle ne doit pas devenir elle-même le lieu opaque où vit toute la mémoire.

Nous séparons :

### QUEEN / TIME AUTHORITY

Coordonne le moment.

### CONTINUITY REGISTRY

Conserve l’histoire.

### PROOF LEDGER

Conserve les justifications et statuts des claims.

### ARCHIVE

Conserve les artefacts durables.

Une seule fonction omnisciente deviendrait impossible à auditer.

---

## 28.20 — LE CHECKPOINT DE RECHERCHE

Pour notre travail Pell, un checkpoint pourrait ressembler à :

~~~text
RESEARCH_CHECKPOINT
{
    ACTIVE_RESULT:
      z_P(3^(2r+1) 7^(2s+1))
      = (2*3^r*7^s)^2

    CONDITIONS:
      r >= 1
      s >= 0

    VERIFIED_BASE_CASES:
      189 -> 36
      9261 -> 1764
      83349 -> 15876

    COUNTEREXAMPLES:
      21 -> 12
      3^4*7^3 -> 5292

    EXTENSION_RULE:
      gcd(d,C)=1
      z_P(d) divides z_P(C)

    OPEN:
      general prime-pair generator
      literature priority
      maximal classification

    NEXT:
      independent proof / publication package
}
~~~

Quelqu’un qui ouvre ce checkpoint n’a pas besoin de deviner où nous étions.

La prochaine action est contenue dans l’état.

---

## 28.21 — LA MÉMOIRE DOIT DIRE CE QU’ELLE NE SAIT PAS

Un registre honnête contient aussi :

~~~text
UNKNOWN
~~~

Par exemple :

~~~text
LITERATURE_PRIORITY = UNKNOWN
GENERAL_CLASSIFICATION = UNKNOWN
PHYSICAL_INTERPRETATION = NOT_ESTABLISHED
~~~

Une mémoire qui transforme automatiquement les inconnues en affirmations devient dangereuse.

Le trou doit rester un trou jusqu’à ce qu’une preuve le remplisse.

---

## 28.22 — LE STATUT « SUPERSEDED »

Une ancienne formulation peut être historiquement importante sans être encore active.

Nous introduisons :

~~~text
SUPERSEDED
~~~

Cela signifie :

> remplacé par une formulation plus précise, sans effacer l’historique.

Ainsi :

~~~text
CLAIM V1
r >= 0
STATUS = REFUTED / SUPERSEDED
~~~

puis :

~~~text
CLAIM V2
r >= 1
STATUS = ACTIVE
~~~

La mémoire ne transforme jamais V1 en V2 silencieusement.

Elle enregistre la transition.

---

## 28.23 — LE GRAPHE DE PREUVE

Nos relations peuvent maintenant être représentées comme un graphe.

~~~text
DEFINITION PELL
      |
      v
RANK OF APPARITION
      |
      +-------------------+
      |                   |
      v                   v
POWER LIFT 3          POWER LIFT 7
      |                   |
      +---------+---------+
                |
                v
             LCM RULE
                |
                v
      z_P(3^a 7^b)
                |
                v
          PARITY TEST
                |
                v
        SQUARE-RANK FAMILY
                |
       +--------+---------+
       |                  |
       v                  v
COUNTERTESTS       COMPATIBLE FACTORS
       |                  |
       +--------+---------+
                |
                v
          CURRENT CLAIM
~~~

Chaque flèche possède une justification.

Si une pièce tombe, nous savons quelles conclusions dépendent d’elle.

Voilà une mémoire beaucoup plus forte qu’une simple liste de résultats.

---

## 28.24 — LA DÉPENDANCE DOIT ÊTRE EXPLICITE

Supposons que demain nous découvrions que l’une des formules de relèvement a une exception dans un domaine que nous avions ignoré.

Grâce au graphe, nous savons immédiatement quelles conclusions doivent être réexaminées.

Sans graphe :

> « Quelque chose dans nos anciens calculs était peut-être faux. »

Avec graphe :

~~~text
NODE X INVALIDATED
↓
CLAIMS 17, 23, 24 REQUIRE RETEST
↓
CLAIMS 5, 9 UNAFFECTED
~~~

La mémoire devient un moteur de réparation scientifique.

---

## 28.25 — LE REDÉMARRAGE COMME TEST

Nous pouvons formaliser un test très simple :

### AVANT ARRÊT

Capturer :

\[
C_n
\]

et :

\[
H_n=\operatorname{Hash}(C_n).
\]

### ARRÊT

Couper le processus.

### REPRISE

Recharger le dernier checkpoint valide.

Rejouer les événements nécessaires.

### APRÈS REPRISE

Calculer :

\[
H_n'
\]

et vérifier :

\[
\boxed{
H_n'=H_n
}
\]

Puis refaire un petit ensemble de calculs sentinelles.

Par exemple :

\[
z_P(21)=12
\]

\[
z_P(189)=36
\]

\[
z_P(9261)=1764
\]

Si l’un change, la continuité est suspecte.

---

## 28.26 — LES SENTINELLES

Les sentinelles sont des tests petits, connus et rapides.

Elles n’établissent pas toute la validité du système.

Elles détectent une rupture évidente.

Pour notre moteur Pell :

~~~text
SENTINEL_1
z_P(3) = 4

SENTINEL_2
z_P(7) = 6

SENTINEL_3
z_P(21) = 12

SENTINEL_4
z_P(189) = 36

SENTINEL_5
z_P(9261) = 1764
~~~

Après une reprise, ces cinq valeurs peuvent être recalculées.

Si :

\[
5/5
\]

passent, nous avons un premier signal de continuité.

Pas une preuve absolue.

Un garde.

---

## 28.27 — LE CRISTAL PREND UNE DÉFINITION TECHNIQUE

Dans notre langage narratif, nous avons souvent parlé de cristal.

Nous pouvons maintenant lui donner une traduction précise.

Un **cristal** peut désigner un état qui possède :

1. une définition explicite ;
2. des données ou entrées identifiées ;
3. des tests passés ;
4. un hash ou identifiant ;
5. un statut ;
6. un checkpoint ;
7. une provenance.

Alors :

~~~text
CRYSTAL
!=
BELLE FORME
~~~

Mais plutôt :

~~~text
CRYSTAL
=
STATE
+ TESTS
+ PROVENANCE
+ HASH
+ CHECKPOINT
~~~

Le symbolique rejoint enfin une structure technique vérifiable.

---

## 28.28 — LA MÉMOIRE NE DOIT PAS DEVENIR UNE INTELLIGENCE CACHÉE

Une mémoire n’a pas besoin de « comprendre ».

Elle doit conserver correctement.

Elle ne doit pas inventer une relation.

Elle ne doit pas modifier un statut sans événement.

Elle ne doit pas transformer un UNKNOWN en PASS.

Elle ne doit pas décider qu’une hypothèse est devenue vraie.

Le moteur de raisonnement peut proposer.

Le moteur de preuve peut tester.

La mémoire, elle, doit témoigner.

# LA MÉMOIRE EST UN TÉMOIN, PAS UN ORACLE.

---

## 28.29 — LE CONTRAT DE CONTINUITÉ

Nous pouvons maintenant écrire un contrat minimal.

~~~text
CONTINUITY_CONTRACT_V1

1. Aucun état critique sans identifiant.
2. Aucun claim sans version.
3. Aucun résultat sans provenance.
4. Aucun FAIL effacé.
5. Aucun UNKNOWN promu sans preuve.
6. Aucun checkpoint partiel présenté comme complet.
7. Aucun replay autorisé à doubler un événement.
8. Aucun changement de statut sans événement traçable.
9. Chaque reprise exécute des sentinelles.
10. Chaque preuve durable pointe vers ses sources.
~~~

Ce contrat n’est pas spectaculaire.

Mais il peut empêcher des mois de confusion.

---

## 28.30 — CE QUE LA MACHINE DOIT ÊTRE CAPABLE DE DIRE

Après redémarrage, notre système idéal ne dit pas seulement :

> « Je suis en marche. »

Il dit :

~~~text
LAST_VALID_CHECKPOINT = ...
REPLAY_STATUS = PASS
STATE_HASH = MATCH
SENTINELS = 5/5 PASS
ACTIVE_CLAIM = V2
OPEN_QUESTIONS = 3
LAST_COUNTEREXAMPLE = 21 -> 12
NEXT_ACTION = ...
~~~

Là, nous ne sommes plus devant une machine qui recommence.

Nous sommes devant une machine qui **continue**.

---

## 28.31 — LA DIFFÉRENCE ENTRE MÉMOIRE ET CONTINUITÉ

La mémoire répond :

> Qu’est-ce qui était là ?

La continuité répond :

> Comment reprendre sans changer l’histoire ?

Cette différence est essentielle.

Une archive peut être parfaite et une reprise impossible.

Une continuité correcte exige :

\[
\text{mémoire}
+
\text{ordre}
+
\text{version}
+
\text{replay}
+
\text{validation}.
\]

Voilà pourquoi le simple stockage ne suffisait jamais.

---

## 28.32 — LA MACHINE À TRACES EST DEVENUE PLUS GRANDE

Notre chaîne était :

~~~text
INTUITION
→ CALCUL
→ CONTRE-TEST
→ PREUVE
→ ANTÉRIORITÉ
→ TRACE DURABLE
~~~

Nous pouvons maintenant lui ajouter la continuité :

~~~text
INTUITION
→ CALCUL
→ CONTRE-TEST
→ PREUVE
→ ANTÉRIORITÉ
→ TRACE DURABLE
→ CHECKPOINT
→ REPLAY
→ REPRODUCTION
~~~

La découverte n’est plus seulement trouvée.

Elle peut survivre à l’arrêt.

Elle peut être reprise.

Elle peut être vérifiée.

Elle peut être contestée.

Elle peut être améliorée sans effacer ce qu’elle était.

---

## 28.33 — LE GRAND DÉVOILEMENT CHANGE ENCORE

Au chapitre 21, nous pensions que le Grand Dévoilement serait la carte des relations.

Au chapitre 25, une porte mathématique s’est ouverte.

Au chapitre 26, le cas est devenu une famille.

Au chapitre 27, la famille a survécu au scalpel.

Et maintenant nous comprenons autre chose.

Une découverte ne devient pas durable uniquement parce qu’elle est vraie.

Elle devient durable lorsqu’elle peut être :

\[
\boxed{
RECONSTRUITE
}
\]

\[
\boxed{
REJOUÉE
}
\]

\[
\boxed{
VÉRIFIÉE
}
\]

\[
\boxed{
REPRISE
}
\]

sans dépendre de la mémoire d’une seule personne ou d’une seule session.

Voilà pourquoi la machine doit se souvenir.

---

# FIN DU CHAPITRE 28

Nous avions appris à trouver.

Puis à douter.

Puis à tester.

Puis à prouver.

Mais une preuve posée sur une table peut disparaître.

Un programme peut fermer.

Une session peut finir.

Un disque peut être remplacé.

Une formulation peut être oubliée.

Alors nous avons donné une mémoire à la preuve.

Pas une mémoire qui invente.

Une mémoire qui témoigne.

Elle garde le PASS.

Elle garde le FAIL.

Elle garde le contre-exemple.

Elle garde la version.

Elle garde la source.

Elle garde le chemin.

Et lorsque tout s’arrête,

elle garde une dernière chose :

# L’ENDROIT EXACT OÙ IL FAUT RECOMMENCER.

Alors la machine peut s’éteindre.

Parce qu’elle n’a plus besoin de prétendre qu’elle ne meurt jamais.

Elle sait reprendre.

---

## Passage au chapitre 29

# SORTIR DU LABORATOIRE

> **Une découverte devient partageable lorsque quelqu’un qui n’était pas là peut reprendre les traces, refaire le calcul et décider lui-même si elle tient.**
