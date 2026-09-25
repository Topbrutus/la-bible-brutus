# Chapitre 15 — Réparer sans effacer

**APRÈS L’INTRODUCTION — CINQUIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** La cicatrice utile  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Réparer un système ne signifie pas faire disparaître l’erreur.  
> Cela signifie retrouver un état acceptable sans perdre la preuve de ce qui s’est produit.**

---

## La mémoire garde la trace. La réparation peut commencer.

Le chapitre 14 s’est terminé devant un système qui possède enfin un passé vérifiable.

Il peut comparer.

Il peut rejouer.

Il peut retrouver un checkpoint.

Il peut montrer ce qui était vrai avant une rupture.

Cette capacité change complètement la nature de l’erreur.

Avant la mémoire, une erreur est parfois seulement un événement pénible.

Après la mémoire, elle devient un objet analysable.

Nous pouvons demander :

quand a-t-elle commencé ?

quel module l’a vue en premier ?

quelle donnée l’a précédée ?

quel état était encore valide ?

quelle action a aggravé ou réduit le problème ?

quel chemin est resté sain ?

quel checkpoint est disponible ?

À partir de là, la réparation cesse d’être une improvisation.

Elle peut devenir une procédure.

---

## Détecter n’est pas réparer

Cette distinction doit être posée immédiatement.

Un système peut savoir qu’il va mal sans savoir quoi faire.

Nous pouvons décomposer :

[
DETECTION
ightarrow
DIAGNOSTIC
ightarrow
DECISION
ightarrow
ACTION
ightarrow
VERIFICATION
]

Chaque étape possède un rôle différent.

**DETECTION** dit :

quelque chose ne respecte plus une condition attendue.

**DIAGNOSTIC** cherche :

où et pourquoi.

**DECISION** choisit :

quoi faire.

**ACTION** applique :

la correction, l’isolation, le rollback ou l’arrêt.

**VERIFICATION** répond :

est-ce réellement revenu dans un état acceptable ?

Confondre ces étapes produit des réparations dangereuses.

---

## Une alarme n’est pas un diagnostic

Supposons qu’une métrique dépasse un seuil.

[
x > x_{max}
]

Le système peut lever une alarme.

Mais cette alarme ne prouve pas la cause.

La cause peut être :

une entrée incorrecte;

un module fautif;

une unité erronée;

une donnée périmée;

une horloge désynchronisée;

un lien dupliqué;

une erreur de calcul;

une instrumentation elle-même défectueuse.

Alors :

> **symptôme ≠ cause.**

Cette règle doit survivre à toutes les couches.

---

## Le premier réflexe : ne pas empirer

Lorsqu’un système détecte un comportement anormal, la première action utile n’est pas toujours de corriger.

Parfois, il faut d’abord empêcher l’erreur de se propager.

Nous pouvons appeler cela :

**CONTAINMENT.**

Le confinement peut signifier :

isoler un module;

geler une sortie;

désactiver un chemin;

passer en lecture seule;

rejeter de nouvelles commandes;

sauvegarder l’état;

arrêter proprement.

Le but immédiat est simple :

**limiter la zone de dommage.**

---

## Le rayon d’impact

Une erreur dans B1 peut rester locale.

Ou se propager vers :

[
B1 ightarrow B2 ightarrow B3 ightarrow J
]

Si les quatre chemins partagent certaines ressources, l’erreur peut contaminer davantage.

Nous pouvons définir conceptuellement un ensemble d’impact :

[
I(e)
=
{m mid m 	ext{ peut être influencé par l’erreur } e}
]

Plus cet ensemble est petit, plus l’architecture est contenue.

Cela donne un objectif de conception :

> **une panne locale devrait rester locale autant que possible.**

---

## Les frontières de faute

Une architecture peut créer des frontières entre composants.

Une erreur dans un module ne doit pas automatiquement corrompre l’état de tous les autres.

Pour cela, nous pouvons utiliser :

validation des entrées;

copies immuables;

files séparées;

transactions;

timeouts;

processus isolés;

permissions limitées.

La frontière de faute n’est pas une garantie absolue.

C’est une stratégie de réduction de propagation.

---

## Isoler

Si un module devient suspect, nous pouvons le faire passer dans un état :

[
ISOLATED
]

Cela signifie qu’il ne participe plus aux sorties actives.

Mais il peut rester observable.

Cette nuance est importante.

Arrêter toute visibilité sur un module fautif détruit parfois les informations nécessaires au diagnostic.

L’isolation doit couper l’influence, pas forcément l’observation.

---

## Le module malade ne doit pas cacher sa maladie

Un module isolé devrait pouvoir exposer :

dernière entrée valide;

dernière sortie valide;

état actuel;

erreur;

tick de rupture;

version;

dépendances;

tentatives de récupération.

Ainsi, l’architecture peut continuer à regarder la panne sans la laisser piloter le reste du système.

---

## FAIL OPEN et FAIL CLOSED

Certains systèmes doivent choisir leur comportement lorsqu’une vérification échoue.

Deux stratégies générales existent :

**fail open** : continuer malgré l’échec;

**fail closed** : bloquer ou refuser par défaut.

Le choix dépend du risque.

Pour une fonction critique, continuer avec une donnée inconnue peut être dangereux.

Pour une fonction non critique, bloquer tout le système peut être disproportionné.

La politique doit donc être attachée au contexte.

---

## Le mode dégradé

Entre fonctionner normalement et tout arrêter, il existe parfois un troisième état :

[
DEGRADED
]

Le système continue avec moins de capacités.

Exemple :

quatre chemins deviennent trois;

une visualisation est coupée;

une fonctionnalité secondaire est désactivée;

un calcul haute résolution passe en basse résolution.

Mais ce mode doit être visible.

Un résultat produit en mode dégradé ne doit pas être présenté comme provenant du système complet.

---

## Dégradation explicite

Nous pouvons attacher un statut à la sortie :

[
O =
(value,status,active_paths)
]

Par exemple :

[
status = DEGRADED
]

et :

[
active_paths = {P_1,P_2,P_4}
]

Ainsi, la sortie peut continuer d’exister tout en conservant la preuve que (P_3) était absent.

---

## Réparer quoi ?

Le mot réparation peut désigner plusieurs choses.

Réparer une donnée.

Réparer un état.

Réparer un lien.

Réparer une configuration.

Réparer un fichier.

Réparer un processus.

Réparer un service.

Réparer une dépendance.

Réparer un protocole.

Réparer une hypothèse.

Ces réparations n’ont pas les mêmes règles.

Le système doit donc identifier la couche concernée.

---

## Réparer une donnée

Une donnée invalide ne devrait pas être modifiée silencieusement pour devenir plausible.

Si une valeur :

[
x = -5 	ext{ Hz}
]

arrive dans un contexte où la fréquence doit être non négative, plusieurs options existent.

Rejeter.

Marquer invalide.

Demander une nouvelle mesure.

Appliquer une transformation seulement si elle est définie par le protocole.

Mais remplacer automatiquement par :

[
|x| = 5
]

sans justification serait une falsification du sens.

---

## Imputation

Parfois une donnée manquante peut être estimée.

Interpolation.

Moyenne.

Dernière valeur connue.

Modèle prédictif.

Cette opération s’appelle souvent imputation ou estimation.

Elle peut être légitime.

Mais la sortie doit porter un statut différent :

[
ESTIMATED
]

et non :

[
MEASURED
]

Une réparation de continuité ne doit pas réécrire une estimation comme une observation.

---

## Réparer un état

Si l’état courant est corrompu mais qu’un checkpoint valide existe, le système peut revenir à :

[
S_k
]

avec :

[
k < n
]

Cette opération est un rollback.

Mais revenir en arrière crée une nouvelle question :

que faire des événements entre (k) et (n) ?

Les rejouer ?

Les abandonner ?

Les filtrer ?

La réparation doit définir cette politique.

---

## Rollback

Un rollback peut être représenté :

[
S_n
ightarrow
S_k
]

Mais cette flèche ne doit jamais effacer l’existence de (S_n).

Le registre doit conserver :

état fautif;

raison du rollback;

checkpoint choisi;

acteur ou mécanisme ayant autorisé l’action;

résultat.

La trajectoire devient :

[
S_k
ightarrow
cdots
ightarrow
S_n
ightarrow
ROLLBACK(S_k)
ightarrow
S'_k
]

Le passé fautif reste visible.

---

## Rollforward

Parfois revenir en arrière est impossible ou indésirable.

On peut réparer en avançant.

Appliquer une correction.

Migrer.

Réconcilier.

Recalculer.

Nous pouvons appeler cela conceptuellement :

**ROLLFORWARD.**

Le choix entre rollback et rollforward dépend du contexte.

Un fichier peut être restauré.

Une transaction externe déjà envoyée ne peut pas toujours être annulée.

---

## L’irréversible

Certaines actions changent le monde extérieur.

Envoyer un message.

Déclencher une machine.

Publier.

Supprimer.

Payer.

Commander.

Dans ces cas, le système doit reconnaître que :

[
UNDO
]

n’existe pas toujours.

La meilleure réparation devient parfois une **action compensatoire**.

---

## Compensation

Si une action (A) ne peut pas être annulée, on peut parfois appliquer :

[
A^{-1}_{comp}
]

qui ne remonte pas le temps mais réduit ou corrige l’effet.

Exemple conceptuel :

une entrée publiée incorrectement peut être suivie d’une correction.

Le premier événement reste réel.

La compensation devient un deuxième événement.

C’est plus honnête que prétendre que le premier n’a jamais existé.

---

## La réparation transactionnelle

Pour les opérations réversibles, nous pouvons utiliser une séquence :

[
PREPARE
ightarrow
VALIDATE
ightarrow
APPLY
ightarrow
VERIFY
ightarrow
COMMIT
]

Si la vérification échoue avant le commit :

[
ROLLBACK
]

Cette structure réduit le risque d’états intermédiaires incohérents.

---

## Atomicité

Une opération atomique cherche à apparaître comme :

tout appliqué

ou

rien appliqué.

Cela peut être précieux lorsque plusieurs éléments doivent changer ensemble.

Par exemple, si deux fichiers constituent un même contrat, modifier seulement l’un peut casser le système.

L’atomicité protège contre les demi-réparations.

---

## Une demi-réparation peut être pire que la panne

Supposons qu’une configuration comporte deux paramètres liés :

[
(a,b)
]

et qu’une migration exige :

[
(a_0,b_0)
ightarrow
(a_1,b_1)
]

Si seulement (a) est modifié, l’état :

[
(a_1,b_0)
]

peut être invalide.

Le système doit donc connaître les invariants qui doivent rester vrais pendant ou après la réparation.

---

## Invariant

Un invariant est une propriété attendue.

Par exemple :

[
a+b=1
]

ou :

[
STATE in {READY,RUNNING,STOPPED}
]

ou :

[
tick_{n+1}>tick_n
]

Une réparation est acceptable seulement si les invariants requis sont restaurés.

---

## Le catalogue d’invariants

Chaque module peut déclarer des invariants.

Types.

Domaines.

Relations.

Ordre.

État.

Synchronisation.

La détection d’une violation devient alors plus précise.

Au lieu de dire :

**ça semble bizarre**

nous pouvons dire :

**l’invariant I-07 est violé depuis le tick 812.**

La réparation devient plus mesurable.

---

## Détection par invariant

Pour un invariant :

[
I(S)=TRUE
]

le système peut vérifier :

[
I(S_n)
]

Si :

[
I(S_n)=FALSE
]

il lève une violation.

Mais encore une fois :

violation ≠ cause.

L’invariant dit que l’état n’est pas acceptable selon la règle.

Il ne dit pas nécessairement pourquoi.

---

## Diagnostic

Le diagnostic cherche à localiser la cause probable.

Il peut examiner :

les événements précédents;

les dépendances;

les erreurs;

les changements de configuration;

les versions;

les écarts de timing;

les entrées inhabituelles.

Le diagnostic peut produire plusieurs candidats.

Il doit accepter l’incertitude.

---

## Cause candidate

Nous pouvons représenter :

[
C =
{c_1,c_2,ldots,c_k}
]

avec éventuellement des scores ou priorités.

Mais tant qu’une cause n’est pas démontrée, elle doit rester :

**CANDIDAT.**

Cela évite qu’une hypothèse de diagnostic soit inscrite comme cause certaine.

---

## Corrélation n’est pas cause

Un paramètre changé juste avant une panne est suspect.

Mais cette proximité temporelle ne prouve pas qu’il est responsable.

Il faut tester.

Reproduire.

Comparer.

Isoler.

Le registre donne une piste.

Le protocole donne la preuve.

---

## Reproduction de la panne

Une réparation robuste commence souvent par la capacité à reproduire le défaut.

Si nous possédons :

checkpoint;

inputs;

version;

timing;

configuration;

nous pouvons tenter :

[
REPLAY
ightarrow
FAIL
]

Si la panne revient de manière déterministe, le diagnostic devient beaucoup plus fort.

---

## Le test minimal qui casse

Au lieu de rejouer tout le système, nous pouvons chercher le plus petit scénario qui reproduit le défaut.

C’est le principe du **minimal failing case**.

Réduire :

nombre de modules;

données;

durée;

dépendances.

Jusqu’à obtenir une petite expérience qui échoue encore.

Le problème devient plus facile à comprendre.

---

## Réparer petit

La philosophie Brutus revient :

**construire petit → vérifier → cloner → étendre.**

La réparation doit suivre la même règle :

**isoler petit → corriger petit → tester petit → réintégrer.**

Une grosse réparation non décomposée peut masquer de nouvelles erreurs.

---

## Patch minimal

Un patch devrait modifier le moins de choses possible pour corriger le défaut identifié.

Cela réduit le rayon de risque.

Mais minimal ne signifie pas bâclé.

Le patch doit encore :

respecter les invariants;

passer les tests;

laisser une trace;

être relisible.

---

## Le patch et la cause

Un patch peut supprimer le symptôme sans corriger la cause.

Par exemple :

augmenter un timeout peut cacher un ralentissement.

Ignorer une erreur peut faire disparaître l’alarme.

Redémarrer périodiquement peut masquer une fuite.

Ces actions peuvent être utiles temporairement.

Mais elles doivent être étiquetées :

**MITIGATION**

et non :

**FIX**

si la cause n’est pas réellement corrigée.

---

## Mitigation

Une mitigation réduit l’impact.

Elle peut être nécessaire immédiatement.

[
MITIGATION

eq
ROOT_CAUSE_FIX
]

Cette distinction est fondamentale.

Elle permet de continuer à opérer sans fermer prématurément l’enquête.

---

## Correction racine

Une correction de cause racine cherche à supprimer le mécanisme qui produit le défaut.

Pour prétendre qu’elle fonctionne, nous voulons idéalement :

reproduction avant;

patch;

non-reproduction après;

tests de non-régression;

surveillance après déploiement.

La preuve est une séquence.

---

## Le test avant et après

Pour un cas fautif (X) :

Avant :

[
F_{old}(X)=FAIL
]

Après :

[
F_{new}(X)=PASS
]

Puis il faut vérifier que les cas normaux restent valides :

[
F_{new}(N_i)=PASS
]

Le deuxième test est aussi important que le premier.

Une réparation qui casse trois fonctions pour en sauver une n’est pas nécessairement acceptable.

---

## Régression

Une régression est un comportement anciennement correct qui devient incorrect après un changement.

Le système doit donc posséder des tests historiques.

La mémoire des anciennes erreurs devient alors une défense contre leur retour.

---

## Test de non-régression

Chaque bug important peut produire un test permanent.

Le test porte la cicatrice.

Il dit :

**ceci a déjà cassé.**

Et à chaque nouvelle version :

**ça ne doit pas recasser.**

Voilà une mémoire active.

---

## Le réparateur automatique

Nous pouvons maintenant imaginer un module de réparation automatique.

Mais il doit être conçu avec beaucoup de prudence.

Il ne doit pas posséder un pouvoir illimité.

Il doit avoir :

un périmètre;

des règles;

des actions autorisées;

des seuils;

des validations;

un rollback;

une journalisation.

---

## Le réparateur ne doit pas improviser hors contrat

Un système automatique peut choisir parmi une liste d’actions autorisées :

restart module;

reload config;

switch replica;

restore checkpoint;

clear cache;

isolate path.

Mais s’il rencontre une situation non couverte, le bon comportement peut être :

[
STOP_AND_ASK
]

plutôt que d’inventer une procédure.

La prudence est une fonction.

---

## Autorité de réparation

Qui a le droit de réparer quoi ?

Nous pouvons définir des niveaux.

**AUTO-SAFE**  
Action locale, réversible, testée.

**GO-REQUIRED**  
Action potentiellement importante nécessitant une autorisation.

**MANUAL-ONLY**  
Action irréversible ou hors périmètre.

Cette séparation transforme la sécurité en architecture.

---

## Réparation sous GO

Pour une action sensible :

[
DETECT
ightarrow
DIAGNOSE
ightarrow
PROPOSE
ightarrow
PREVIEW
ightarrow
GO
ightarrow
APPLY
ightarrow
VERIFY
]

Le système prépare.

L’opérateur décide.

La trace conserve la frontière.

---

## Le GO doit porter sur une action précise

Un GO général ne devrait pas autoriser n’importe quoi.

Il peut être lié à :

[
GO(action_id,scope,expiry)
]

où :

- action_id identifie l’action;
- scope limite son effet;
- expiry limite sa durée.

Ainsi, une autorisation ne devient pas un chèque en blanc.

---

## Réparer automatiquement un crash

Un crash de processus peut parfois être réparé par restart.

Mais il faut distinguer :

**recovery**

et :

**resolution.**

Le service peut repartir.

La cause du crash peut rester.

Alors le registre doit contenir :

crash;

restart;

succès du restart;

cause inconnue ou candidate;

fréquence de répétition.

---

## Restart loop

Une réparation automatique mal conçue peut créer :

[
CRASH
ightarrow
RESTART
ightarrow
CRASH
ightarrow
RESTART
ightarrow
cdots
]

Une boucle de redémarrage peut consommer des ressources et masquer le problème.

Il faut donc une limite.

Par exemple :

[
N_{	ext{restart}} le N_{max}
]

dans une fenêtre donnée.

Après cela :

[
ISOLATE
]

ou :

[
STOP
]

---

## Backoff

Lorsque des retries sont permis, il est souvent utile d’espacer les tentatives.

Une séquence de backoff peut suivre :

[
d_k = d_0 2^k
]

jusqu’à une limite, dans un schéma exponentiel simple.

Cela évite de marteler une ressource défaillante.

Mais le choix du backoff doit être adapté au contexte.

---

## Retry n’est pas réparation

Réessayer peut résoudre une panne transitoire.

Mais si la même erreur revient, le retry ne corrige rien.

La télémétrie doit donc distinguer :

attempt count;

success after retry;

permanent failure.

Le système ne doit pas déclarer « réparé » simplement parce qu’il a réessayé.

---

## Pannes transitoires et permanentes

Une erreur réseau peut disparaître.

Un fichier corrompu peut persister.

Une mauvaise configuration restera jusqu’à modification.

La stratégie de réparation dépend donc du type de panne.

Classifier correctement est important.

---

## Corruption

La corruption signifie qu’une donnée ou un état ne correspond plus à ce qui était attendu.

Un checksum ou un hash peut détecter certaines modifications.

Par exemple :

[
H(C_{read}) 
eq H(C_{expected})
]

indique que le contenu lu ne correspond pas à l’empreinte attendue.

Mais cela ne dit pas automatiquement pourquoi.

---

## Détection de corruption

Une stratégie peut utiliser :

checksums;

hashes;

parité;

copies redondantes;

validation de structure;

contraintes sémantiques.

Chaque méthode détecte certaines classes d’erreurs.

Aucune ne garantit tout.

---

## Réparer une corruption par copie saine

Si nous possédons deux copies :

[
C_A
]

et :

[
C_B
]

et que (C_A) échoue à la vérification tandis que (C_B) passe, nous pouvons restaurer à partir de (C_B).

Mais il faut être sûr que (C_B) est réellement une source autorisée.

Sinon nous remplaçons une corruption par une autre.

---

## Redondance

La redondance conserve plusieurs ressources capables de remplir une fonction.

Elle peut améliorer la tolérance aux pannes.

Mais elle augmente aussi :

complexité;

coût;

synchronisation;

risque de divergence.

La redondance n’est pas automatiquement de la robustesse.

Elle doit être contrôlée.

---

## Deux copies peuvent mentir ensemble

Si deux répliques dérivent de la même source corrompue, leur accord ne prouve rien.

La diversité de provenance peut parfois compter autant que le nombre de copies.

Encore une fois :

quantité ≠ indépendance.

---

## Réplication et consensus

Dans certains systèmes distribués, plusieurs nœuds doivent s’accorder sur un état.

Cela mène à des familles de protocoles de consensus.

Brutus n’a pas besoin de prétendre réinventer ces théories.

Si un jour cette fonction devient nécessaire, nous devrons étudier et utiliser des protocoles établis adaptés au problème.

La discipline reste :

**ne pas réinventer une sécurité complexe par intuition seule.**

---

## Vote majoritaire

Un vote simple peut sembler naturel :

trois copies;

deux gagnent.

Mais si les erreurs ne sont pas indépendantes, le vote peut confirmer une valeur fausse.

Alors une majorité ne signifie pas automatiquement vérité.

Le modèle de faute doit être défini.

---

## Réparer les quatre chemins

Dans notre architecture à quatre chemins, une panne peut toucher un seul chemin.

Nous pouvons imaginer :

[
P_1 = OK
]

[
P_2 = OK
]

[
P_3 = FAULT
]

[
P_4 = OK
]

Le système doit décider si la sortie peut continuer.

Cela dépend de la fonction de la jonction.

Si les quatre sont obligatoires :

[
OUTPUT = BLOCKED
]

Si trois suffisent selon le protocole :

[
OUTPUT = DEGRADED
]

La règle doit exister avant la panne.

---

## Pas de règle inventée pendant l’incident

Décider en plein incident que « trois sur quatre, c’est assez » uniquement parce qu’un chemin vient de casser serait dangereux.

Les critères de tolérance doivent être définis et testés à l’avance lorsque possible.

La crise n’est pas le meilleur moment pour inventer le protocole.

---

## Quorum

Lorsqu’un système utilise un quorum, le seuil doit être défini.

Par exemple :

[
q = 3
]

sur quatre participants.

Mais la valeur (q) n’a de sens qu’avec un modèle de fonctionnement précis.

Le nombre seul ne garantit rien.

---

## La réparation par substitution

Un chemin défaillant peut parfois être remplacé par une instance de secours.

[
P_3
ightarrow
P_3'
]

Mais il faut vérifier :

version;

état;

configuration;

position dans le cycle;

dépendances.

Un remplaçant qui ne partage pas le bon contexte peut produire une nouvelle incohérence.

---

## Warm standby et cold standby

Une instance de secours peut être :

déjà active et synchronisée;

ou démarrée seulement au besoin.

Ces stratégies ont des coûts différents.

Le standby chaud réduit le temps de reprise mais augmente la complexité de synchronisation.

Le standby froid est plus simple mais plus lent.

Le choix dépend de l’exigence.

---

## RTO et RPO

Dans les systèmes de continuité, deux notions sont utiles.

**RTO** : Recovery Time Objective — délai cible de reprise.

**RPO** : Recovery Point Objective — quantité de données ou de temps que l’on accepte potentiellement de perdre.

Ces objectifs ne sont pas des mesures après coup.

Ce sont des cibles de conception.

Par exemple :

un système peut viser une reprise en moins d’une minute avec moins de dix secondes de données perdues.

La valeur exacte doit venir du besoin réel.

---

## Mesure de reprise

Après un incident, nous pouvons mesurer :

[
T_{	ext{recovery}}
=
t_{	ext{restored}}
-
t_{	ext{failure}}
]

et :

[
L_{	ext{data}}
=
t_{	ext{failure}}
-
t_{	ext{last durable}}
]

Ces mesures permettent de comparer la réalité aux objectifs.

---

## Réparation et état sain connu

Pour revenir à un état correct, il faut savoir ce que signifie **sain**.

Nous pouvons définir un prédicat :

[
HEALTHY(S)=TRUE
]

qui dépend d’invariants et de tests.

Un état n’est pas sain seulement parce que le programme ne plante plus.

Il doit respecter les conditions nécessaires.

---

## Health check

Un health check peut tester :

processus actif;

ports disponibles;

dépendances accessibles;

état interne cohérent;

latence acceptable;

erreurs bloquantes absentes.

Mais un seul endpoint « OK » ne prouve pas tout.

Le health check doit documenter ce qu’il couvre.

---

## Liveness et readiness

Deux concepts peuvent être séparés.

**Liveness** : le processus fonctionne-t-il encore ?

**Readiness** : est-il prêt à recevoir du travail ?

Un module peut être vivant mais pas prêt.

Par exemple :

il démarre;

charge un checkpoint;

synchronise;

puis devient READY.

Cette distinction rend les récupérations plus sûres.

---

## Un voyant vert peut mentir

Si l’interface affiche HEALTHY parce que le processus répond, mais que ses données sont corrompues, le voyant est trompeur.

La santé doit donc être composée de conditions réelles.

Une couleur ne crée pas le statut.

Elle le reflète.

---

## Le protocole de santé

Nous pouvons imaginer :

[
HEALTH =
LIVENESS
land
STATE_VALID
land
DEPENDENCIES_VALID
land
CLOCK_VALID
land
NO_CRITICAL_ERROR
]

Cette formule est un exemple de contrat.

La vraie définition dépendra du module.

---

## Auto-réparation

Le terme **self-healing** est séduisant.

Nous devons l’utiliser avec prudence.

Un système qui redémarre un service n’est pas nécessairement « auto-guéri ».

Il a exécuté une procédure de récupération.

Le mot peut être utilisé comme raccourci d’ingénierie, mais la Bible doit décrire l’action concrète derrière.

---

## Auto-réparation bornée

Nous pouvons définir une capacité d’auto-réparation comme :

> ensemble fini et testé d’actions automatiques autorisées permettant de restaurer certaines classes connues de défaillances, avec vérification et journalisation.

Cette définition est beaucoup plus précise que :

**le système se répare tout seul.**

---

## Classe de panne

Pour chaque action automatique, il faut définir la classe qu’elle couvre.

Exemple :

**F-01 : processus non répondant mais état durable intact.**

Action :

restart contrôlé.

Vérification :

health + état + reprise du tick.

Si la panne ne correspond pas à F-01 :

ne pas appliquer automatiquement la recette F-01.

---

## Catalogue de réparations

Nous pouvons construire :

[
F_i
ightarrow
A_i
ightarrow
V_i
]

où :

- (F_i) = classe de panne;
- (A_i) = action;
- (V_i) = vérification.

Ce catalogue devient testable.

Il peut grandir avec l’expérience.

---

## Une réparation sans vérification n’est pas terminée

Après l’action, il faut mesurer.

Le système a-t-il retrouvé :

ses invariants ?

sa synchronisation ?

ses connexions ?

son rythme ?

son état ?

sa sortie ?

Si non :

la réparation a échoué.

Même si l’erreur initiale a disparu.

---

## VERIFY

Nous pouvons définir :

[
VERIFY(S_{	ext{after}})
=
igwedge_i I_i(S_{	ext{after}})
]

où les (I_i) sont les invariants requis.

Seulement si cette vérification passe, l’état peut être marqué :

[
RECOVERED
]

---

## RECOVERED n’est pas RESOLVED

Un incident peut être récupéré sans que sa cause soit résolue.

**RECOVERED** :

le service fonctionne de nouveau.

**RESOLVED** :

la cause a été identifiée et traitée selon le protocole.

Cette distinction protège contre les faux fermetures.

---

## Le temps après réparation

Une réparation peut sembler réussie immédiatement puis échouer plus tard.

Nous avons donc besoin d’une période d’observation.

[
OBSERVE(T)
]

Pendant cette fenêtre :

métriques;

erreurs;

jitter;

état;

répétition du symptôme.

La réparation gagne en confiance avec le temps, mais ne devient jamais « vraie » par magie.

---

## Burn-in

Pour certaines modifications, une période de fonctionnement prolongé peut servir de burn-in.

Le système reste sous observation.

Si aucune récidive n’apparaît pendant les conditions définies, la confiance augmente.

Mais l’absence d’erreur pendant une durée ne prouve pas l’impossibilité d’une future erreur.

Le langage doit rester mesuré.

---

## Réparer la mémoire elle-même

La mémoire peut aussi être endommagée.

Log incomplet.

Checkpoint corrompu.

Index cassé.

Hash manquant.

Dans ce cas, le système doit distinguer :

source primaire;

copies;

index reconstructible;

archive.

La mémoire doit avoir sa propre stratégie de récupération.

---

## Checkpoint corrompu

Un checkpoint ne doit jamais être utilisé simplement parce qu’il existe.

Il doit passer des validations :

format;

hash;

version;

schéma;

cohérence;

compatibilité.

Si la validation échoue :

[
CHECKPOINT = INVALID
]

et le système cherche une autre source.

---

## Dernier checkpoint valide

Nous pouvons maintenir une chaîne :

[
C_0,C_1,ldots,C_n
]

avec statut.

Si (C_n) est invalide, le système peut chercher :

[
C_{n-1}
]

puis rejouer les événements ultérieurs disponibles.

Cette stratégie peut réduire la perte.

---

## Ne jamais écraser la seule copie saine

Une règle opérationnelle extrêmement importante :

> **Avant une réparation destructive, préserver une copie vérifiée de l’état courant ou du dernier état sain lorsque c’est possible.**

Sinon une tentative de réparation peut détruire la seule preuve restante.

---

## Sauvegarde avant mutation

Le cycle devient :

[
READ
ightarrow
BACKUP
ightarrow
CHANGE
ightarrow
TEST
ightarrow
COMMIT
]

Cette discipline apparaît aussi dans Git.

Lire avant d’écrire.

Obtenir le SHA avant de remplacer.

Vérifier après.

La réparation logicielle et la continuité documentaire se rejoignent.

---

## L’état courant peut être précieux même s’il est cassé

Un système fautif contient parfois la seule preuve de la panne.

Le redémarrer immédiatement peut effacer :

mémoire volatile;

stack;

buffers;

états transitoires.

Alors, si le contexte le permet :

**capture avant reset.**

Cette règle doit être équilibrée avec l’urgence et la sécurité.

---

## Triage

Le triage répond :

quelle est la gravité ?

quel est le rayon d’impact ?

faut-il arrêter ?

peut-on observer ?

peut-on continuer en mode dégradé ?

Cette étape évite d’appliquer la même procédure à toutes les erreurs.

---

## Sévérité

Nous pouvons définir des niveaux internes :

INFO;

WARNING;

ERROR;

CRITICAL.

Mais les noms ne suffisent pas.

Chaque niveau doit être lié à des conséquences.

Par exemple :

WARNING : continue, surveille.

ERROR : isole le module.

CRITICAL : stop global ou GO requis.

Le sens doit être opérationnel.

---

## Priorité

La sévérité n’est pas toujours la priorité.

Une panne mineure très fréquente peut devenir prioritaire.

Une panne critique dans une fonctionnalité jamais utilisée peut avoir une urgence différente.

La gestion d’incident doit séparer ces concepts si nécessaire.

---

## L’erreur doit être reproductible avant d’être spectaculaire

Une panne impressionnante attire l’attention.

Mais pour l’ingénierie, la question centrale est :

pouvons-nous la reproduire ?

Si oui, nous pouvons construire un test.

Si non, nous devons améliorer l’instrumentation.

La reproductibilité transforme l’incident en objet scientifique.

---

## Fuzzing et stress

Nous pouvons provoquer des erreurs de manière contrôlée.

Entrées limites.

Ordres inhabituels.

Redémarrages.

Corruption simulée.

Concurrence.

Charge.

Le but n’est pas de casser pour casser.

Le but est de découvrir où la réparation échoue avant que le monde réel le fasse.

---

## Injection de faute

Une technique de test consiste à introduire volontairement une panne.

Couper un lien.

Retarder un message.

Tuer un processus.

Corrompre une copie de test.

Refuser une dépendance.

Puis observer :

détection;

confinement;

reprise;

trace.

Cela permet de tester le système de réparation lui-même.

---

## Un test de panne doit rester contrôlé

Les expériences destructives doivent être isolées.

Environnement de test.

Données de test.

Permissions limitées.

Rollback préparé.

Il serait absurde de tester la résilience en détruisant la seule copie de production.

---

## Chaos contrôlé

Les techniques dites de chaos engineering poussent cette idée plus loin : introduire des défaillances de manière planifiée pour mesurer la résilience.

Mais le mot **chaos** ne signifie pas absence de protocole.

Au contraire.

Le test doit avoir :

hypothèse;

périmètre;

arrêt d’urgence;

métriques;

critère de succès;

preuve.

---

## Hypothèse de réparation

Avant un test :

> Si P3 tombe pendant moins de 5 secondes, le système doit passer en DEGRADED, conserver les trois autres chemins, restaurer P3, puis revenir en READY sans perdre l’ordre des ticks confirmés.

Cette hypothèse est testable.

Elle peut échouer.

Voilà ce que nous voulons.

---

## Condition d’abandon

Une réparation automatique doit être désactivée ou revue si :

elle aggrave les pannes;

elle masque la cause;

elle crée des boucles;

elle perd de la preuve;

elle agit hors autorisation;

elle n’est pas reproductible;

elle restaure un état techniquement actif mais sémantiquement faux.

La réparation n’est pas sacrée.

Elle aussi doit être testée.

---

## Le système doit savoir demander de l’aide

Une architecture mature possède une sortie :

[
NEEDS_HUMAN
]

ou :

[
GO_REQUIRED
]

Admettre qu’une situation dépasse le périmètre automatique est une force.

Un réparateur qui prétend tout résoudre devient dangereux.

---

## La frontière humaine

Certaines décisions demandent du jugement.

Choisir entre deux données contradictoires.

Accepter une perte.

Publier une correction.

Modifier un protocole scientifique.

La machine peut présenter :

faits;

options;

impacts;

risques.

L’humain garde la décision lorsque le contrat l’exige.

---

## La réparation et la preuve scientifique

Une réparation peut influencer une expérience.

Si un module a redémarré au milieu d’un run, le résultat doit le signaler.

Sinon nous pourrions comparer :

run sans incident

et

run réparé

comme s’ils étaient identiques.

La provenance de réparation appartient au résultat.

---

## Run contaminé

Un incident peut rendre un run invalide.

Nous pouvons marquer :

[
RUN = INVALID
]

ou :

[
RUN = DEGRADED
]

ou :

[
RUN = RECOVERED
]

selon le protocole.

Le statut doit être défini avant l’interprétation.

---

## La réparation ne nettoie pas la science

Réparer un système permet de continuer.

Elle ne transforme pas automatiquement les données produites pendant la panne en données valides.

Il faut décider séparément quelles portions du run sont utilisables.

Cette décision doit être documentée.

---

## La cicatrice utile

Nous pouvons maintenant donner un sens technique au sous-titre.

Une cicatrice est la trace durable qu’une panne a existé et qu’une réponse a été appliquée.

Elle peut prendre la forme de :

test;

incident report;

commit;

règle;

métrique;

checkpoint;

nouvel invariant.

La cicatrice devient utile lorsqu’elle réduit la probabilité de refaire exactement la même erreur.

---

## Du défaut à la connaissance

La chaîne peut devenir :

[
FAILURE
ightarrow
TRACE
ightarrow
DIAGNOSIS
ightarrow
FIX
ightarrow
TEST
ightarrow
KNOWLEDGE
]

Le système ne « grandit » pas biologiquement.

Mais le projet humain accumule de la connaissance technique.

Cette connaissance peut ensuite être encodée dans l’architecture.

---

## Une réparation devient mémoire

Lorsque la correction est connue, elle peut entrer dans :

catalogue;

test;

documentation;

automatisation.

Ainsi, la prochaine occurrence est traitée plus vite.

La mémoire et la réparation forment une boucle.

---

## Boucle de robustesse

Nous pouvons représenter :

[
OBSERVE
ightarrow
DETECT
ightarrow
DIAGNOSE
ightarrow
REPAIR
ightarrow
VERIFY
ightarrow
LEARN
ightarrow
OBSERVE
]

Le mot **LEARN** ici signifie :

mettre à jour les règles, tests ou connaissances techniques.

Pas attribuer une conscience au système.

---

## Réparation et cristallisation

Dans le langage Brutus, la **cristallisation** peut être utilisée comme métaphore d’un état qui se stabilise.

Mais nous devons préciser la traduction.

Un état « cristallisé » pourrait signifier, dans un protocole futur :

invariants satisfaits;

configuration figée;

hash enregistré;

checkpoint valide;

tests passés.

Alors le mot symbolique peut recevoir un contrat technique.

---

## Cristal valide

Nous pouvons définir un candidat :

[
CRYSTAL(S)
=
HEALTHY(S)
land
CHECKPOINTED(S)
land
HASHED(S)
land
TESTED(S)
]

Ce n’est pas une formule physique.

C’est une règle architecturale possible.

Elle traduit une image en conditions vérifiables.

---

## Décristalliser

Si une modification intervient, l’état n’est plus identique au checkpoint.

Le système peut repasser en :

[
DIRTY
]

ou :

[
UNVERIFIED
]

jusqu’à une nouvelle validation.

Ainsi, la cristallisation n’est pas permanente.

Elle représente un état vérifié à une version précise.

---

## L’état stable n’est pas forcément le bon état

Un bug peut être parfaitement stable.

Un système peut produire toujours le même mauvais résultat.

La stabilité ne prouve donc pas la correction.

[
STABLE 
eq VALID
]

Cette distinction doit rester centrale.

---

## Réparer la stabilité

Parfois le problème n’est pas un crash mais une oscillation, une dérive ou une instabilité.

Dans ce cas, la réparation peut relever du contrôle.

Mesurer l’erreur :

[
e(t)=r(t)-y(t)
]

et appliquer une action corrective.

Mais toute boucle de contrôle doit être analysée pour éviter de créer plus d’instabilité.

---

## Le contrôleur n’est pas un guérisseur

Un contrôleur ajuste.

Il ne comprend pas nécessairement pourquoi la perturbation existe.

Il peut maintenir une variable autour d’une cible.

Cela peut être une forme de compensation continue.

La cause externe peut rester présente.

Encore une fois :

compensation ≠ suppression de cause.

---

## Saturation

Une action corrective possède des limites.

[
u_{min}
le
u(t)
le
u_{max}
]

Si le contrôleur atteint sa saturation, il ne peut plus compenser davantage.

Cette limite doit être visible.

Un système qui cache la saturation peut donner l’impression qu’il contrôle encore.

---

## Anti-windup

Dans certains contrôleurs intégrateurs, une saturation prolongée peut accumuler un terme interne et provoquer un dépassement lors du retour.

Des techniques d’anti-windup existent pour limiter ce problème.

La leçon architecturale plus générale est simple :

> **une réparation continue peut elle-même accumuler une erreur interne.**

Le réparateur doit donc être observé.

---

## Le réparateur doit avoir un health check

Nous surveillons les modules.

Mais qui surveille le mécanisme de réparation ?

Il doit lui aussi exposer :

état;

actions en cours;

actions réussies;

actions échouées;

boucles;

limites;

autorisations.

Aucun composant important ne doit devenir invisible parce qu’il est censé aider.

---

## Watchdog

Un watchdog peut surveiller qu’un composant répond dans le temps prévu.

Si le signal attendu n’arrive pas, il peut déclencher une action.

Mais un watchdog mal calibré peut produire des faux positifs.

Le timeout doit être basé sur des mesures et des besoins.

---

## Heartbeat

Un module peut émettre périodiquement un heartbeat :

[
H_n=(module,tick,time,status)
]

L’absence de heartbeat pendant une fenêtre peut signaler un problème.

Mais encore une fois :

absence de heartbeat ≠ preuve absolue de crash.

Le réseau ou le superviseur peuvent être fautifs.

Le diagnostic doit garder plusieurs possibilités.

---

## Réparer sans anthropomorphiser

Nous pouvons dire dans le récit :

**Brutus s’est blessé.**

C’est une image.

Dans le système :

un invariant a été violé;

un module a été isolé;

un checkpoint a été restauré;

un test a été exécuté.

Les deux langages peuvent coexister.

La Bible doit seulement montrer lequel est lequel.

---

## Une réparation observable

Une interface peut représenter :

FAULT;

ISOLATING;

RESTORING;

VERIFYING;

RECOVERED.

Chaque étape correspond à un événement réel.

L’animation n’invente rien.

Elle raconte le protocole.

---

## La couleur de réparation

Une lumière ou une animation peut aider l’opérateur à comprendre.

Mais le statut doit venir du moteur.

La coquille ne pense toujours pas.

Elle montre :

[
STATE_{	ext{repair}}
]

fourni par le système d’autorité.

---

## Réparation manuelle

L’humain peut intervenir.

Mais l’action manuelle doit être enregistrée avec le même sérieux que l’automatique.

Une commande tapée dans un terminal peut modifier plus de choses qu’un module logiciel.

Alors elle mérite :

heure;

commande ou action pertinente;

cible;

résultat;

preuve.

Sans enregistrer de secrets.

---

## Le mode opérateur

Une interface de réparation peut proposer :

diagnostic;

prévisualisation;

dry run;

GO;

exécution;

vérification.

Le dry run est précieux.

Il permet de voir ce qui serait changé sans changer réellement.

---

## Dry run

Nous pouvons écrire :

[
ACTION(S)
ightarrow
PREDICTED_DIFF
]

sans mutation réelle.

Le résultat montre :

fichiers touchés;

états visés;

services redémarrés;

risques connus.

Puis l’opérateur décide.

Cela réduit les surprises.

---

## Le diff de réparation

Avant :

[
S_{	ext{before}}
]

Prévision :

[
hat{S}_{	ext{after}}
]

Après application :

[
S_{	ext{after}}
]

Nous pouvons comparer :

[
hat{S}_{	ext{after}}
stackrel{?}{=}
S_{	ext{after}}
]

Si la réalité diffère fortement de la prévision, le système doit le signaler.

---

## Le plan n’est pas le résultat

Cette distinction est cruciale.

Un plan de réparation peut être parfait.

L’exécution peut échouer.

Alors les rapports doivent séparer :

**PROPOSED**

**EXECUTED**

**VERIFIED**

Jamais fusionner les trois.

---

## Réparer Git

Le même principe existe dans notre manière de travailler avec les dépôts.

Lire avant d’écrire.

Connaître le SHA.

Modifier précisément.

Commit atomique.

Relire.

Vérifier le HEAD.

Si quelque chose diverge, ne pas écraser aveuglément.

Cette discipline n’est pas bureaucratique.

C’est une forme de réparation préventive.

---

## Conflit

Un conflit signifie que l’état que nous voulions modifier n’est plus celui que nous avions lu.

La bonne réaction n’est pas :

forcer.

C’est :

relire;

comparer;

réconcilier.

Le conflit protège parfois le travail d’un autre acteur.

---

## Force

Certaines opérations permettent un mode force.

C’est un outil puissant.

Il doit être utilisé seulement lorsque la perte potentielle est comprise.

Un système qui répare toujours avec force transforme les protections en décor.

---

## Préserver l’inconnu

Lorsqu’un incident contient une zone non comprise, il faut la conserver.

Ne pas nettoyer tous les fichiers temporaires si l’un peut contenir la preuve.

Ne pas réinitialiser tous les logs avant capture.

Ne pas réécrire une configuration suspecte avant comparaison.

L’inconnu peut être précieux.

---

## La réparation scientifique

Lorsqu’une formule échoue à un test, la réparation n’est pas d’ajuster jusqu’à obtenir le résultat désiré.

Il faut comprendre le modèle.

Vérifier les unités.

Réexaminer les hypothèses.

Tester sur d’autres données.

Une hypothèse scientifique ne se « répare » pas pour gagner.

Elle se modifie parce qu’une raison explicite le justifie.

---

## Le surajustement comme fausse réparation

Modifier les paramètres pour correspondre parfaitement à un exemple connu peut produire une illusion de succès.

Le modèle devient excellent sur la cible utilisée.

Mais mauvais ailleurs.

La réparation scientifique doit donc chercher des tests hors échantillon ou indépendants lorsque possible.

---

## La réparation d’une formule

Une formule peut évoluer :

[
F_1
ightarrow
F_2
]

La provenance doit conserver :

différence;

raison;

test ayant échoué;

test ayant motivé la correction;

nouveaux résultats.

Ainsi, (F_1) ne disparaît pas.

Elle devient une étape de l’histoire.

---

## Versionner la réparation

Un correctif peut être :

[
PATCH_V1
]

puis :

[
PATCH_V2
]

si le premier était incomplet.

L’étiquette de version empêche la phrase vague :

**nous avons déjà corrigé ça.**

La bonne question devient :

**quelle correction, dans quelle version, avec quels tests ?**

---

## Le rapport d’incident

Un rapport minimal peut contenir :

### Détection
Que s’est-il passé ?

### Impact
Qu’est-ce qui a été affecté ?

### Timeline
Quand ?

### Preuves
Logs, métriques, états.

### Cause
Confirmée, candidate ou inconnue.

### Mitigation
Qu’a-t-on fait immédiatement ?

### Correction
Qu’est-ce qui a changé ?

### Vérification
Quels tests ont passé ?

### Suivi
Qu’est-ce qui reste à faire ?

Cette structure transforme la panne en connaissance transmissible.

---

## Postmortem sans théâtre

Le but d’un postmortem technique n’est pas de chercher un coupable.

Il est de rendre le système plus compréhensible.

Les décisions humaines peuvent être analysées.

Mais la question principale reste :

**quelles conditions ont permis à la panne d’exister et de se propager ?**

Cette approche produit de meilleures protections.

---

## La faute unique et les conditions multiples

Un incident important a souvent plusieurs conditions.

Un bug.

Un test manquant.

Une alerte trop tardive.

Une permission trop large.

Un rollback non testé.

Chercher une seule « cause » peut simplifier à l’excès.

Le graphe causal peut être plus honnête.

---

## Arbre de défaillance

Une analyse peut représenter plusieurs conditions menant à un événement.

Par exemple :

[
FAIL
=
A
land
(B lor C)
]

Cette structure aide à trouver plusieurs points de prévention.

Nous ne sommes pas obligés de corriger une seule cause si plusieurs barrières peuvent être renforcées.

---

## Défense en profondeur

Une architecture robuste ne dépend pas d’une seule protection.

Validation.

Isolation.

Permissions.

Checkpoints.

Tests.

Monitoring.

Rollback.

Chaque couche réduit un risque différent.

Si une barrière échoue, une autre peut limiter l’impact.

---

## Pas de sécurité magique

Aucune couche ne garantit l’absence totale de panne.

La robustesse est une réduction du risque.

Une capacité de détection.

Une capacité de récupération.

Une capacité d’apprentissage.

Le langage doit rester réaliste.

---

## Mesurer la réparation

Nous pouvons suivre :

taux de détection;

temps de détection;

temps de confinement;

temps de récupération;

récurrence;

perte de données;

faux positifs;

faux négatifs.

Ces métriques permettent d’améliorer le protocole.

---

## Temps de détection

[
MTTD
]

est souvent utilisé pour mean time to detect dans certains contextes opérationnels.

Mais plutôt que d’utiliser l’acronyme sans définition, la Bible doit toujours préciser ce qui est mesuré.

Une moyenne peut aussi masquer une distribution.

Les percentiles restent utiles.

---

## Temps de récupération

[
MTTR
]

peut signifier mean time to repair ou mean time to recovery selon les organisations.

Cette ambiguïté montre pourquoi les acronymes doivent être définis localement.

Le projet doit écrire sa définition.

---

## Le langage doit être aussi robuste que le système

Un mot ambigu devient une connexion invisible dans la documentation.

La règle du chapitre 12 s’applique aussi au vocabulaire.

Si deux personnes utilisent « repair » pour parler de choses différentes, le protocole peut échouer.

Définir les mots fait partie de l’ingénierie.

---

## Réparer ne veut pas dire revenir exactement

Après une panne, le système peut revenir dans un état différent mais valide.

Par exemple :

ancienne instance remplacée;

nouvelle version;

nouveau checkpoint;

nouvelle route.

La continuité n’exige pas identité absolue.

Elle exige un lien explicable entre avant et après.

---

## Continuité de service

Un service peut rester disponible pendant une réparation grâce à la redondance ou au mode dégradé.

Mais disponibilité ne signifie pas intégrité.

Nous devons mesurer les deux séparément.

Un service peut répondre tout en produisant de mauvaises données.

---

## Intégrité

L’intégrité concerne la correction et la cohérence de l’information selon le contrat.

La disponibilité concerne l’accès au service.

Un système robuste doit savoir lequel il protège dans chaque situation.

Parfois il vaut mieux devenir indisponible que produire une réponse fausse.

---

## Le choix sûr

Pour une fonction scientifique, il peut être préférable de répondre :

**UNKNOWN**

ou :

**BLOCKED**

plutôt que d’inventer une valeur.

Le système doit considérer l’absence honnête comme une sortie valide.

---

## Un zéro de secours peut être dangereux

Remplacer une valeur manquante par zéro peut modifier un calcul sans déclencher d’erreur.

Alors une valeur de secours doit être explicitement marquée.

Par exemple :

[
(value=0,status=FALLBACK)
]

Cela évite de confondre le secours avec la mesure réelle.

---

## La réparation et l’utilisateur

Lorsque le système se répare, l’utilisateur doit savoir si le résultat qu’il voit a été affecté.

Le silence peut détruire la confiance.

Un indicateur simple peut montrer :

NORMAL;

DEGRADED;

RECOVERING;

RECOVERED;

BLOCKED.

Cette transparence est une fonction de sécurité.

---

## Ne pas paniquer l’interface

La transparence ne signifie pas afficher mille erreurs brutes.

L’interface peut résumer.

Mais les détails doivent être accessibles.

Le visiteur voit :

**mode dégradé.**

L’architecte peut ouvrir :

module;

tick;

erreur;

action;

preuve.

Deux niveaux de lecture.

Une même vérité.

---

## Le réparateur et la Reine

Si l’Horloge de la vie fournit le battement, le réparateur ne doit pas modifier le temps sans trace.

Un restart peut créer une nouvelle session.

Un rollback peut restaurer un ancien tick logique.

Le registre doit distinguer :

temps de l’ancien run;

temps du nouveau run;

relation entre les deux.

---

## Nouvelle session

Après une récupération majeure, nous pouvons créer :

[
session_{k+1}
]

même si le système reprend un état de :

[
session_k
]

Cela évite de prétendre que la chronologie n’a jamais été interrompue.

La continuité peut contenir une rupture explicitement marquée.

---

## Une rupture visible est meilleure qu’une continuité fausse

C’est une règle puissante.

Une ligne brisée que l’on comprend vaut mieux qu’une ligne lisse fabriquée artificiellement.

La réparation doit accepter la cicatrice.

---

## La mémoire tampon avant crash

Le buffer circulaire du chapitre 14 devient ici un outil de diagnostic.

Il conserve les dernières secondes ou derniers ticks.

À la panne :

gel.

Puis capture après si possible.

Nous obtenons :

[
PRE_FAIL
]

et :

[
POST_FAIL
]

Cette fenêtre est souvent plus informative qu’un log immense.

---

## Le moment exact de bascule

Une panne peut être définie par le premier tick où un invariant devient faux.

[
n^* =
min {n : I(S_n)=FALSE}
]

Ce tick devient un point d’enquête.

Nous pouvons remonter juste avant :

[
S_{n^*-1}
]

et comparer.

La réparation commence par une frontière précise.

---

## Bisect

Lorsqu’un bug apparaît entre deux versions, nous pouvons chercher le premier commit fautif par dichotomie.

Cette méthode réduit rapidement l’espace de recherche.

Elle repose sur une mémoire versionnée propre.

Encore une fois, la continuité rend la réparation possible.

---

## Le premier mauvais commit

Si une version :

[
V_a
]

passe le test et :

[
V_b
]

échoue, le bisect cherche la transition.

Le résultat ne prouve pas toujours la cause exacte, mais il localise fortement la modification suspecte.

Le diff peut ensuite être analysé.

---

## La réparation comme science expérimentale

Une panne est une observation.

Une hypothèse de cause est une hypothèse.

Un patch est une intervention.

Le test après patch est une expérience.

La régression est une réplication.

Cette structure ressemble profondément à une démarche scientifique.

Elle impose :

mesure;

hypothèse;

test;

preuve;

révision.

---

## Ne pas tomber amoureux du diagnostic

Une cause élégante peut être fausse.

Si le test la réfute, il faut l’abandonner.

La beauté d’une explication n’a pas plus de poids ici qu’ailleurs.

Le chapitre 6 reste vivant :

**forme ≠ stabilité ≠ preuve.**

---

## Réparation et apprentissage humain

Chaque incident peut améliorer le projet.

Pas automatiquement.

Seulement si nous faisons le travail :

documenter;

comprendre;

tester;

modifier;

vérifier.

La souffrance d’un système ne produit pas la robustesse.

La transformation produit la robustesse.

C’est le même principe que dans le chapitre 2.

---

## Ce qui ne tue pas ne rend pas automatiquement plus fort

Une panne répétée peut simplement abîmer le système.

Pour qu’elle devienne force, elle doit devenir :

information;

test;

protection.

La phrase de l’Introduction revient sous forme mécanique :

> **La cicatrice devient information. L’erreur devient mémoire.**

---

## La réparation parfaite n’existe pas

Toute réparation peut introduire un nouveau risque.

Tout rollback peut perdre une donnée récente.

Toute redondance peut diverger.

Tout automatisme peut se tromper.

La robustesse vient donc d’un cycle continu de vérification.

Pas d’une solution finale.

---

## La prochaine porte

Nous savons maintenant :

détecter;

contenir;

diagnostiquer;

réparer;

revenir;

avancer;

isoler;

vérifier;

apprendre.

Mais un autre phénomène apparaît.

Quand un système est réparé plusieurs fois, quand il reçoit des perturbations, quand ses chemins se synchronisent et se désynchronisent, nous devons pouvoir répondre :

**est-il réellement stable ?**

Un système peut toujours finir par revenir.

Mais à quel coût ?

Avec quelle amplitude ?

En combien de temps ?

Après quelles perturbations ?

Le prochain chapitre devra transformer le mot **stabilité** en mesure.

---

## Réparer n’est pas stabiliser

Une réparation est un événement ou une procédure.

La stabilité est une propriété du comportement sur le temps et sous perturbation.

Un système peut être facilement réparable mais intrinsèquement instable.

Un autre peut être stable et rarement nécessiter une réparation.

Les deux notions doivent être séparées.

---

## Vers le protocole de stabilité

Nous aurons besoin de :

état de référence;

perturbation définie;

métrique;

seuil;

temps d’observation;

condition de retour;

condition d’échec.

Alors seulement nous pourrons dire quelque chose de sérieux sur la stabilité.

---

## Dernière image

Une erreur apparaît.

Le voyant change.

P3 est isolé.

Le registre gèle la fenêtre.

Un checkpoint est sélectionné.

Le système propose une action.

Le GO arrive.

La restauration commence.

Les invariants repassent au vert.

Les quatre chemins reviennent.

Mais l’ancien incident n’a pas disparu.

Il existe maintenant sous une autre forme.

Un test.

Un rapport.

Une règle.

Une cicatrice.

C’est là que la réparation devient utile.

Pas lorsqu’elle cache que quelque chose s’est cassé.

Lorsqu’elle transforme la rupture en une protection supplémentaire.

Le système n’est pas invincible.

Il devient plus compréhensible.

Et ce que nous pouvons comprendre, nous pouvons enfin commencer à mesurer sous contrainte.

# **LA CICATRICE RESTE. LA STABILITÉ DOIT MAINTENANT ÊTRE PROUVÉE.**
