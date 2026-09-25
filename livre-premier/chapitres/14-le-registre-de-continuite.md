# Chapitre 14 — Le Registre de Continuité

**APRÈS L’INTRODUCTION — QUATRIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** La mémoire qui ne ment pas  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Un système ne possède pas une mémoire parce qu’il garde beaucoup de données.  
> Il possède une mémoire lorsqu’il peut retrouver ce qui s’est réellement passé.**

---

## Le temps passe. La mémoire commence.

Le chapitre 13 s’est terminé avec une conséquence presque inévitable.

Dès qu’un système possède un battement, il produit un avant et un après.

Puis un autre avant.

Puis un autre après.

Très vite, il ne possède plus seulement un état.

Il possède une trajectoire.

Et une trajectoire qui n’est pas conservée disparaît.

Alors la première question du chapitre 14 est simple :

**que faut-il garder pour pouvoir continuer sans réinventer le passé ?**

Pas tout.

Pas rien.

Ce qu’il faut pour comprendre.

Ce qu’il faut pour vérifier.

Ce qu’il faut pour reprendre.

---

## Une mémoire technique n’est pas une conscience

Nous devons commencer par une distinction claire.

Un système peut conserver :

des valeurs;

des fichiers;

des snapshots;

des logs;

des événements;

des états;

des erreurs;

des décisions.

Cela ne signifie pas qu’il se souvient comme un humain.

Cela signifie qu’il possède un mécanisme de conservation et de récupération d’information.

Dans le langage de ce chapitre :

> **mémoire = capacité technique à préserver et retrouver une information reliée à une provenance et à un contexte.**

Cette définition est suffisante.

Elle n’a pas besoin d’attribuer une vie intérieure à la machine.

---

## Le registre de continuité

Le chapitre 11 avait fait apparaître une structure très simple :

[
QUI
ightarrow
ÉTAT
ightarrow
TICK
ightarrow
AVANT
ightarrow
ACTION
ightarrow
APRÈS
]

Le chapitre 12 l’a reliée aux modules.

Le chapitre 13 lui a donné du temps.

Nous pouvons maintenant la formaliser davantage.

Pour un événement (e_n), écrivons :

[
R_n =
(
id_n,
source_n,
tick_n,
t_n,
S^-_n,
A_n,
S^+_n,
O_n,
E_n,
P_n
)
]

où :

- (id_n) = identifiant de l’événement;
- (source_n) = module ou acteur source;
- (tick_n) = repère logique;
- (t_n) = repère temporel;
- (S^-_n) = état avant;
- (A_n) = action;
- (S^+_n) = état après;
- (O_n) = sortie éventuelle;
- (E_n) = erreur éventuelle;
- (P_n) = provenance.

Ce registre n’explique pas le monde.

Il décrit une transition.

C’est exactement ce dont nous avons besoin.

---

## Avant et après

La mémoire devient beaucoup plus utile lorsque les deux côtés d’un changement sont conservés.

Si un paramètre passe de :

[
a = 0.25
]

à :

[
a = 0.20
]

garder seulement la nouvelle valeur nous fait perdre une partie de l’histoire.

Garder :

[
a_{	ext{before}} = 0.25
]

et :

[
a_{	ext{after}} = 0.20
]

permet une comparaison.

Puis il faut encore savoir :

qui a modifié;

quand;

pourquoi;

dans quelle version;

avec quel résultat.

La mémoire technique est donc un réseau de contexte, pas une simple liste de nombres.

---

## Le changement comme objet

Une modification peut être représentée comme :

[
Delta S_n
=
S^+_n - S^-_n
]

lorsque cette soustraction a un sens.

Mais tous les états ne sont pas numériques.

Pour un objet complexe, la différence peut être une structure :

ajout;

suppression;

remplacement;

activation;

désactivation;

reconnexion.

Le principe reste le même :

**le changement doit être observable.**

---

## Journaliser n’est pas tout sauvegarder

Une première tentation serait de tout écrire.

Chaque variable.

Chaque microseconde.

Chaque appel de fonction.

Chaque pixel.

Chaque message.

Cette stratégie peut rapidement devenir impossible.

Le volume explose.

Le stockage ralentit.

La lecture devient plus difficile que l’événement lui-même.

Alors la mémoire doit être conçue.

Une mémoire utile est sélective.

Mais cette sélection doit être explicite.

---

## La règle de conservation

Pour chaque donnée candidate à la mémoire, nous pouvons poser quatre questions :

1. Est-elle nécessaire pour reproduire ?
2. Est-elle nécessaire pour expliquer ?
3. Est-elle nécessaire pour reprendre ?
4. Est-elle nécessaire pour prouver ?

Si la réponse est non aux quatre, elle peut probablement être éphémère.

Si la réponse est oui à au moins une, sa rétention mérite d’être définie.

---

## Mémoire vive et mémoire durable

Il existe une différence entre ce qui doit survivre quelques secondes et ce qui doit survivre des années.

Nous pouvons distinguer :

[
M_{	ext{volatile}}
]

et :

[
M_{	ext{durable}}
]

La mémoire volatile peut contenir :

buffers;

cache;

derniers états;

valeurs temporaires;

files d’attente.

La mémoire durable peut contenir :

checkpoints;

releases;

journaux significatifs;

configurations;

provenance;

résultats d’expériences;

artefacts scientifiques.

Les deux sont utiles.

Leur rôle n’est pas le même.

---

## Le cache n’est pas la mémoire de vérité

Un cache est une copie optimisée pour accélérer l’accès.

Il peut être supprimé.

Reconstruit.

Invalidé.

Le système ne doit pas confondre :

**la copie rapide**

avec :

**la source canonique.**

Si un cache disparaît et que le système perd définitivement l’information, ce n’était pas seulement un cache.

C’était une mémoire primaire mal nommée.

---

## Source canonique

Pour chaque information durable importante, nous devrions pouvoir répondre :

**où est la source d’autorité ?**

Un dépôt.

Une base de données.

Un fichier signé.

Un registre append-only.

Un artefact de release.

Le choix peut varier.

Mais il doit exister.

Le mot important est :

**canonique.**

Cela signifie que lorsqu’il y a conflit entre deux copies, nous savons quelle source fait foi.

---

## Une mémoire sans autorité devient une dispute

Supposons que :

le client conserve un état;

le serveur en conserve un autre;

le fichier local en conserve un troisième.

Lequel est vrai ?

Sans règle, la mémoire ne protège plus la continuité.

Elle crée plusieurs passés.

Alors l’architecture doit définir :

source primaire;

répliques;

cache;

archive;

snapshot.

Chaque rôle doit être distinct.

---

## Écriture append-only

Une stratégie utile pour certains journaux consiste à ne pas réécrire le passé.

On ajoute.

On n’efface pas silencieusement.

Nous pouvons représenter :

[
L_{n+1}
=
L_n cup {R_{n+1}}
]

Le journal devient append-only.

Si une correction est nécessaire, on ajoute une correction.

On ne fait pas disparaître l’événement précédent comme s’il n’avait jamais existé.

Cette propriété renforce énormément l’auditabilité.

---

## Corriger sans falsifier

Supposons qu’un événement ait été enregistré avec une mauvaise interprétation.

La bonne pratique n’est pas nécessairement d’effacer l’ancien texte.

On peut conserver :

événement original;

correction;

raison;

auteur de la correction;

date.

Ainsi, l’histoire reste honnête.

Le système peut dire :

**nous pensions ceci à ce moment-là; voici pourquoi nous avons changé.**

C’est plus solide qu’un passé nettoyé après coup.

---

## Le snapshot

Un snapshot capture l’état d’un système à un instant.

[
Sigma_n = S_n
]

Mais cette notation cache une question fondamentale :

**qu’est-ce qui appartient à (S_n) ?**

Modules ?

Paramètres ?

Buffers ?

Horloge ?

Seed aléatoire ?

Files d’attente ?

Connexions ?

Version du code ?

Dépendances externes ?

Un snapshot incomplet peut être utile.

Mais il doit déclarer son périmètre.

---

## Snapshot partiel

Nous pouvons écrire :

[
Sigma_n^{(K)}
]

pour indiquer un snapshot portant seulement sur un sous-ensemble (K) de l’état.

Par exemple :

état logique sans buffers;

configuration sans historique;

mémoire locale d’un module;

position visuelle sans état du moteur.

Le snapshot n’est pas faux.

Il est partiel.

Le danger apparaît seulement lorsqu’un snapshot partiel est présenté comme complet.

---

## Checkpoint

Un checkpoint possède un objectif supplémentaire :

**reprendre.**

Nous pouvons le définir comme un snapshot accompagné de suffisamment de contexte pour redémarrer à partir d’un état connu.

Un checkpoint candidate peut contenir :

- état;
- version;
- tick;
- temps;
- configuration;
- seed;
- identifiants des dépendances;
- hash;
- règle de restauration.

Le checkpoint n’est donc pas seulement une image.

C’est un point de reprise.

---

## Un checkpoint doit être testé

Sauvegarder un checkpoint ne prouve pas qu’il peut être restauré.

La preuve utile est :

1. créer le checkpoint;
2. arrêter le système;
3. restaurer;
4. vérifier l’état;
5. reprendre;
6. comparer la trajectoire attendue.

Sans test de restauration, nous avons une promesse.

Pas encore une preuve.

---

## Le test de reprise

Supposons un état :

[
S_n
]

Puis un checkpoint :

[
C_n
]

Après restauration, nous obtenons :

[
hat{S}_n
]

Nous voulons vérifier :

[
hat{S}_n = S_n
]

pour les composantes déclarées comme restaurables.

Si l’égalité exacte n’est pas possible, les écarts doivent être définis.

Par exemple :

timestamps externes;

connexions réseau;

ressources non sérialisables.

La reprise doit savoir ce qu’elle promet.

---

## Le replay

Le replay part d’une idée différente.

Au lieu de restaurer un état complet, nous rejouons une séquence d’événements.

Si :

[
S_{n+1}
=
F(S_n,I_n)
]

alors, en conservant :

[
S_0
]

et :

[
I_0,I_1,ldots,I_n
]

nous pouvons tenter de reconstruire la trajectoire.

Le replay devient une preuve puissante si le système est déterministe.

---

## Event sourcing

Cette approche ressemble à un principe connu en architecture logicielle : l’event sourcing.

L’idée générale consiste à considérer les événements comme la source principale de l’évolution d’état.

L’état courant peut être reconstruit à partir du passé.

Dans notre langage :

[
S_n
=
F^*(S_0,R_1,ldots,R_n)
]

où (F^*) représente l’application ordonnée des événements.

Cela peut être extrêmement utile.

Mais cela coûte du stockage et impose une discipline de versionnement.

---

## L’ordre des événements est sacré

Dans un replay, la séquence compte.

[
R_1,R_2,R_3
]

n’est pas nécessairement équivalent à :

[
R_2,R_1,R_3
]

Alors les événements doivent posséder :

identifiant;

ordre;

source;

timestamp ou tick;

relations causales lorsque nécessaire.

Une mémoire sans ordre peut préserver les pièces tout en perdant l’histoire.

---

## La mémoire de causalité

Deux événements peuvent avoir le même tick et pourtant dépendre l’un de l’autre.

Nous pouvons alors utiliser une relation parent-enfant :

[
parent(R_b)=R_a
]

Cela signifie que (R_b) a été déclenché par (R_a).

La mémoire ne conserve plus seulement une chronologie.

Elle conserve un graphe causal.

---

## Le graphe de provenance

Nous pouvons imaginer :

[
G_P = (V_P,E_P)
]

où :

- (V_P) = événements, fichiers, calculs, versions;
- (E_P) = relations de provenance.

Un résultat final peut alors pointer vers :

le module qui l’a produit;

les entrées utilisées;

les paramètres;

le code;

la version;

le test.

Le graphe devient une carte de confiance.

---

## Provenance d’un calcul

Pour un résultat :

[
y = f(x,	heta)
]

une provenance minimale peut contenir :

- valeur de (x);
- valeur de (	heta);
- version de (f);
- unité;
- date;
- environnement;
- hash du code;
- statut du résultat.

Sans cette provenance, la valeur (y) est beaucoup plus difficile à interpréter.

---

## Le hash

Un hash cryptographique peut servir d’empreinte.

Pour un contenu (C) :

[
h = H(C)
]

Si le contenu change, l’empreinte devrait normalement changer.

Cela permet de vérifier l’intégrité.

Mais un hash ne dit pas automatiquement :

qui a créé le fichier;

si le contenu est vrai;

si le calcul est correct;

si l’ordre temporel est authentique.

Il prouve une propriété limitée :

**identité de contenu selon l’algorithme choisi.**

Cette précision est importante.

---

## Hash et provenance

La combinaison devient plus utile :

[
(document, hash, source, date, version)
]

Le hash protège l’intégrité.

La provenance donne le contexte.

La version situe l’objet.

Aucun élément ne remplace les autres.

---

## La mémoire des erreurs

Les erreurs méritent une politique particulière.

Une erreur rare peut être plus utile qu’un million d’événements normaux.

Alors nous pouvons conserver :

cause;

stack ou contexte;

état avant;

entrée;

tick;

module;

version;

action de récupération;

état après.

Une erreur documentée devient un futur test.

---

## L’erreur comme test de non-régression

Si une erreur apparaît à l’entrée (I^*), nous pouvons créer un test :

[
F(I^*) 
eq ERROR_{	ext{old}}
]

dans la version corrigée.

Ainsi, l’erreur passe de :

incident

à :

mémoire

puis à :

protection.

C’est une transformation centrale de Brutus.

---

## La mémoire des succès

Il faut pourtant se méfier d’un autre biais.

Si nous ne gardons que les erreurs, nous perdons la baseline du fonctionnement normal.

Nous avons besoin d’exemples valides.

Des runs propres.

Des distributions nominales.

Des métriques de référence.

Sinon, nous savons reconnaître le mauvais, mais pas définir le bon.

---

## Baseline

Une baseline est une référence documentée.

Elle peut contenir :

version;

configuration;

conditions;

métriques;

résultats;

tolérances.

Une future version peut être comparée à cette baseline.

Par exemple :

[
Delta M
=
M_{	ext{new}}
-
M_{	ext{baseline}}
]

Le changement devient mesurable.

---

## Une baseline n’est pas éternelle

Une baseline représente une référence à un moment donné.

Elle peut devenir obsolète.

Alors elle doit être versionnée.

Par exemple :

[
B_0,;B_1,;B_2
]

Chaque baseline doit dire ce qu’elle remplace et pourquoi.

Sinon un ancien seuil peut rester actif longtemps après avoir perdu son sens.

---

## La mémoire du code

Le dépôt Git joue déjà un rôle de mémoire.

Chaque commit peut conserver :

contenu;

auteur;

date;

parent;

message;

SHA.

Il crée une chaîne.

Mais le commit ne remplace pas la documentation.

Un SHA dit quel état du code nous avons.

Il ne dit pas nécessairement pourquoi une décision a été prise.

Le message et les documents de décision complètent la trace.

---

## Le commit comme checkpoint logique

Un commit peut être vu comme un checkpoint du code.

Mais pas du runtime.

Il capture les fichiers versionnés.

Il ne capture pas automatiquement :

RAM;

base de données;

état réseau;

processus;

variables d’environnement;

secrets;

fichiers ignorés.

La mémoire du code et la mémoire d’exécution doivent donc rester distinctes.

---

## HEAD

Le HEAD répond à une question importante :

**où sommes-nous maintenant dans l’histoire du dépôt ?**

Mais une session scientifique doit parfois aussi conserver :

quel HEAD a produit ce résultat ?

Ainsi, un rapport peut inclure :

[
HEAD = abc123ldots
]

Ce lien entre résultat et code rend la reproduction beaucoup plus forte.

---

## Branche et continuité

Deux branches peuvent posséder deux futurs différents à partir du même passé.

Cela ressemble à une bifurcation de trajectoire.

Une expérience risquée peut vivre sur une branche.

Le tronc principal reste stable.

Puis les résultats sont comparés.

Le versionnement devient ainsi une forme de mémoire expérimentale.

---

## La mémoire ne doit pas contenir les secrets

Conserver n’est pas toujours protéger.

Un journal peut accidentellement enregistrer :

token;

mot de passe;

clé;

donnée privée;

contenu sensible.

Une mémoire durable rend alors la fuite durable.

Donc la règle est stricte :

> **Ce qui ne doit pas être conservé doit être exclu avant l’écriture.**

La sécurité doit exister en amont du stockage.

---

## Redaction

Lorsqu’une donnée sensible peut apparaître, un filtre peut produire :

[
raw
ightarrow
redact
ightarrow
stored
]

Mais la redaction doit être testée.

Un secret partiellement masqué peut parfois rester exploitable.

La mémoire sûre commence par une classification des données.

---

## Rétention

Toutes les données n’ont pas besoin de vivre éternellement.

Nous pouvons définir une durée de rétention :

[
T_R
]

Par exemple :

logs détaillés : quelques jours;

agrégats : plusieurs mois;

artefacts de release : long terme;

cache : quelques secondes.

La politique dépend du besoin.

Mais elle doit être documentée.

---

## Oublier peut être une fonction saine

Une bonne mémoire n’est pas nécessairement celle qui ne perd jamais rien.

Elle peut oublier de manière contrôlée.

Une donnée temporaire peut être détruite après avoir été agrégée.

Un cache peut être vidé.

Un log très détaillé peut être compacté.

L’important est que la perte soit volontaire et compatible avec les besoins de preuve.

---

## Oubli contrôlé

Nous pouvons représenter :

[
M_{	ext{raw}}
ightarrow
A(M_{	ext{raw}})
ightarrow
DELETE(M_{	ext{raw}})
]

où (A) est une agrégation.

Mais avant de supprimer, il faut vérifier que l’agrégat conserve ce qui est nécessaire.

Sinon l’oubli devient une destruction de preuve.

---

## Compression

La compression peut réduire le coût de stockage.

Compression sans perte :

[
C^{-1}(C(x)) = x
]

La donnée peut être reconstruite exactement.

Compression avec perte :

[
hat{x} approx x
]

Une partie de l’information disparaît.

Pour les preuves scientifiques, cette distinction doit être visible.

Une donnée avec perte ne doit pas être présentée comme l’original brut.

---

## Mémoire brute et mémoire dérivée

Nous pouvons distinguer :

[
M_{	ext{raw}}
]

et :

[
M_{	ext{derived}}
]

La mémoire brute contient ce qui a été observé ou reçu.

La mémoire dérivée contient :

moyennes;

courbes;

features;

agrégats;

scores;

interprétations.

La dérivation doit pointer vers le brut lorsqu’il existe.

---

## Une moyenne n’est pas l’histoire

Supposons mille valeurs.

La moyenne peut être :

[
mu = 0.408
]

Deux séries très différentes peuvent partager la même moyenne.

Alors conserver seulement (mu) peut supprimer :

variabilité;

pics;

séquence;

anomalies.

La compression statistique doit être choisie selon la question.

---

## Multi-résolution

Une stratégie utile peut être de conserver plusieurs niveaux.

Très récent :

données fines.

Plus ancien :

agrégats par seconde.

Encore plus ancien :

agrégats par minute.

Archives importantes :

snapshots ou événements rares.

Cette mémoire multi-résolution permet de contrôler le volume sans tout perdre.

---

## La fenêtre glissante

Pour certaines métriques, nous pouvons conserver seulement les (N) derniers échantillons.

[
W_n = {x_{n-N+1},ldots,x_n}
]

La fenêtre glissante donne une mémoire locale du présent.

Elle est utile pour :

moyennes mobiles;

détection d’anomalies;

tendance;

jitter récent.

Mais elle ne remplace pas une archive.

---

## La mémoire tampon

Un buffer circulaire peut conserver une quantité fixe d’événements.

Lorsque le buffer est plein, les plus anciens sont remplacés.

Cela donne une propriété intéressante :

en cas d’erreur, nous avons immédiatement l’histoire juste avant l’incident.

Le buffer devient une boîte noire au sens aéronautique du terme :

une mémoire de contexte.

---

## Geler la mémoire après une erreur

Une stratégie candidate :

1. buffer circulaire actif;
2. erreur critique;
3. gel des (N) événements précédents;
4. capture des (M) événements suivants;
5. sauvegarde durable.

Cette méthode préserve le contexte sans journaliser tout à pleine résolution en permanence.

---

## L’événement déclencheur

Le gel peut être déclenché par :

ERROR;

seuil dépassé;

GO manuel;

anomalie;

timeout;

crash imminent.

L’événement déclencheur doit lui-même être enregistré.

Sinon nous saurons que la mémoire a été gelée sans savoir pourquoi.

---

## La mémoire de l’état zéro

Le chapitre 13 a défini l’importance de :

[
S_0
]

Le chapitre 14 ajoute :

**il faut pouvoir le retrouver.**

Une expérience sans état initial conservé devient beaucoup plus difficile à reproduire.

Alors le checkpoint initial mérite une attention particulière.

---

## La mémoire de configuration

Les paramètres peuvent être aussi importants que les données.

Une configuration :

[
Theta =
(	heta_1,	heta_2,ldots,	heta_k)
]

doit être versionnée si elle influence le résultat.

Modifier (Theta) sans changer de version ou sans enregistrer la modification crée une dépendance cachée.

---

## Config immuable par run

Une discipline forte consiste à figer la configuration au démarrage d’une expérience.

Le run reçoit :

[
Theta_r
]

et la conserve.

Si un paramètre change, un nouveau run ou une nouvelle révision est créée.

Cela facilite énormément la comparaison.

---

## Modification à chaud

Parfois, le système doit permettre de changer un paramètre en cours d’exécution.

Alors le changement doit devenir un événement :

[
	heta:
a
ightarrow
b
]

au tick (n).

La trajectoire peut ensuite être analysée avant et après.

La modification à chaud n’est pas interdite.

Elle doit être visible.

---

## Provenance humaine

Certaines décisions viennent d’un opérateur.

Elles peuvent être enregistrées comme :

rôle;

action;

moment;

objet modifié.

Mais la mémoire ne doit pas collecter plus d’information personnelle que nécessaire.

Le but est la responsabilité technique.

Pas la surveillance.

---

## Provenance IA

Une IA peut elle aussi proposer une modification.

Alors la trace devrait distinguer :

proposé par IA;

accepté par humain;

appliqué par système.

Par exemple :

[
PROPOSE
ightarrow
APPROVE
ightarrow
APPLY
]

Ces trois événements ne sont pas équivalents.

La mémoire doit les séparer.

---

## Proposition n’est pas exécution

C’est une règle très importante.

Une suggestion enregistrée ne prouve pas qu’elle a été appliquée.

Une action appliquée ne prouve pas qu’elle a réussi.

Un test réussi ne prouve pas que la version a été déployée.

Chaque transition doit posséder sa propre preuve.

---

## La chaîne de preuve

Nous pouvons représenter :

[
IDEA
ightarrow
PROPOSAL
ightarrow
CHANGE
ightarrow
TEST
ightarrow
RESULT
ightarrow
RELEASE
]

À chaque flèche, une trace.

Si une étape manque, il faut le dire.

La mémoire empêche les raccourcis narratifs.

---

## Mémoire et vérité

Une mémoire peut conserver une fausse affirmation.

Elle peut conserver une mauvaise mesure.

Elle peut conserver une erreur de calcul.

La conservation ne transforme rien en vérité.

C’est essentiel.

> **Mémoire ≠ validation.**

La mémoire dit :

**voici ce qui a été dit, mesuré ou produit.**

La validation répond à une autre question :

**est-ce correct ?**

---

## Corriger le statut sans supprimer la trace

Supposons qu’un résultat ait été marqué :

**CONFIRMÉ**

puis qu’une erreur soit découverte.

Nous pouvons changer son statut courant vers :

**INVALIDÉ**

tout en conservant le fait qu’il avait été initialement considéré confirmé.

Cette différence permet de comprendre l’évolution de la connaissance.

---

## Statut versionné

Nous pouvons écrire :

[
status_t(x)
]

Le statut d’un objet peut changer dans le temps.

Par exemple :

[
CANDIDAT
ightarrow
TESTÉ
ightarrow
RÉFUTÉ
]

ou :

[
CANDIDAT
ightarrow
TESTÉ
ightarrow
CONFIRMÉ_DANS_LE_PROTOCOLE
]

Le mot final doit rester limité à ce que le protocole prouve réellement.

---

## La mémoire du non-résultat

Parfois, une expérience ne produit rien d’intéressant.

Il faut parfois conserver cette absence.

Sinon, des tests identiques peuvent être répétés plusieurs fois en croyant qu’ils n’ont jamais été essayés.

Un résultat négatif documenté a une valeur.

Il réduit l’espace des possibilités.

---

## L’expérience échouée

Une expérience peut échouer pour plusieurs raisons :

hypothèse fausse;

protocole incorrect;

instrumentation insuffisante;

bug logiciel;

donnée manquante;

erreur humaine.

La mémoire doit éviter de fusionner tous ces cas en :

**ça n’a pas marché.**

La cause appartient à l’histoire.

---

## INCONNU est une mémoire valide

Parfois, la cause reste inconnue.

Alors le registre doit accepter :

**INCONNU.**

Cette étiquette vaut mieux qu’une explication inventée après coup.

L’inconnu conservé peut être résolu plus tard.

L’invention devient beaucoup plus difficile à corriger.

---

## Le journal des décisions

Toutes les décisions importantes ne sont pas visibles dans le code.

Pourquoi quatre chemins ?

Pourquoi cette tolérance ?

Pourquoi ce format ?

Pourquoi abandonner une branche ?

Un journal de décisions peut préserver :

question;

options;

décision;

raison;

preuve disponible;

incertitudes.

Cela réduit énormément la perte de contexte.

---

## Une décision peut être révisée

Le journal ne doit pas devenir une prison.

Une ancienne décision peut être dépassée.

La nouvelle entrée peut dire :

**remplace D-017 pour telle raison.**

Ainsi, la continuité n’empêche pas l’évolution.

Elle la documente.

---

## Le lecteur du futur

Le chapitre 10 imaginait quelqu’un disant :

**Je vois où ils se sont arrêtés.**

Le chapitre 14 construit techniquement cette possibilité.

Pour voir où nous nous sommes arrêtés, il faut :

un état;

une version;

une date;

des décisions;

des preuves;

des inconnues;

une prochaine action.

La mémoire devient donc un outil pour une personne qui n’est pas présente aujourd’hui.

---

## Le prochain constructeur

Il ne connaît pas nos habitudes.

Il n’a pas assisté aux blagues.

Il n’a pas entendu les conversations.

Il ne peut pas demander :

**qu’est-ce que vous vouliez dire ?**

Alors le système doit lui laisser assez de structure pour reconstruire le contexte.

C’est cela, la continuité.

---

## Mémoire collective

Une mémoire collective ne signifie pas que tout le monde voit tout.

Elle signifie qu’une équipe peut partager les éléments nécessaires selon les droits d’accès.

Public.

Privé.

Secret.

Archive.

Chaque catégorie peut avoir une politique différente.

La continuité et la sécurité doivent coexister.

---

## Mémoire publique

Une mémoire publique peut contenir :

documentation;

artefacts publiés;

résultats reproductibles;

versions;

provenance non sensible.

Elle sert à la transmission.

---

## Mémoire privée

Une mémoire privée peut contenir :

notes de travail;

décisions intermédiaires;

informations internes;

données non destinées à la publication.

Mais elle doit elle aussi respecter la sécurité et la minimisation.

Privé ne signifie pas sans règles.

---

## Mémoire secrète

Certaines informations ne devraient jamais entrer dans les journaux ordinaires.

Clés.

Tokens.

Mots de passe.

Secrets cryptographiques.

Ils doivent vivre dans des systèmes conçus pour eux.

La mémoire de continuité doit pointer vers leur existence ou leur mécanisme, pas enregistrer leur valeur.

---

## Une référence peut suffire

Au lieu de stocker un secret :

**SECRET = valeur**

on peut stocker :

**credential source = secure store / key id X**

Ainsi, la continuité sait de quoi le système dépend sans exposer le secret.

---

## L’index n’est pas la source

Une bibliothèque peut avoir un index.

L’index permet de trouver.

Mais si l’index est perdu, les objets devraient idéalement pouvoir être retrouvés ou reconstruits.

Nous pouvons donc distinguer :

[
INDEX
]

et :

[
SOURCE
]

Le premier est reconstructible.

Le second ne doit pas être confondu avec le cache de recherche.

---

## Cache reconstructible

Une règle utile :

> **Tout cache ou index doit pouvoir être reconstruit à partir d’une source durable.**

Si ce n’est pas le cas, il contient une information primaire.

Alors il doit être protégé comme telle.

---

## La Brutothèque

La notion de Brutothèque peut maintenant recevoir un rôle précis.

Elle n’est pas seulement une galerie de modules.

Elle peut devenir une bibliothèque versionnée d’objets avec :

identité;

version;

provenance;

contrats;

tests;

dépendances;

statut;

historique.

Chaque objet devient retrouvable.

---

## Un objet de Brutothèque

Nous pouvons imaginer un manifeste :

[
B =
(id,version,type,hash,inputs,outputs,tests,parent,status)
]

Ce manifeste ne remplace pas l’objet.

Il le décrit.

Et surtout, il permet de le relier à son histoire.

---

## Généalogie

Un objet peut dériver d’un autre.

[
B_2 leftarrow B_1
]

La relation de parenté peut être conservée.

Fork.

Clone.

Variation.

Correction.

Optimisation.

La généalogie permet de savoir si deux objets partagent une origine.

---

## Pourquoi la généalogie compte

Deux modules peuvent avoir des noms différents mais dériver du même ancêtre.

Une vulnérabilité trouvée dans l’ancêtre peut alors concerner les descendants.

La mémoire de provenance devient une aide à la maintenance.

---

## Mémoire et dépendances

Un module dépend parfois d’une bibliothèque externe.

La version de cette dépendance doit être conservée.

Par exemple :

[
M
ightarrow
D_{v3.2}
]

Si la dépendance passe à v4.0, le comportement peut changer.

Sans cette mémoire, un ancien résultat peut devenir impossible à reproduire.

---

## Environnement

Une expérience peut dépendre de :

OS;

architecture CPU;

GPU;

runtime;

pilotes;

variables;

locale;

timezone.

Toutes ces informations ne sont pas toujours nécessaires.

Mais lorsqu’elles peuvent affecter le résultat, elles doivent être capturées.

La mémoire utile est contextuelle.

---

## La mémoire minimale reproductible

Pour chaque expérience, nous pouvons demander :

**quel est le plus petit ensemble d’informations qui permet de reproduire le résultat ?**

Appelons-le :

[
M_{	ext{MR}}
]

Minimum Reproducible Memory.

Il peut contenir :

code;

config;

entrées;

seed;

version;

environnement;

commande;

résultat attendu.

Cette notion empêche deux excès :

tout garder;

ne rien garder.

---

## Le paquet de reproduction

Nous pouvons transformer (M_{	ext{MR}}) en artefact exportable.

Un paquet peut contenir :

manifest;

inputs;

script;

expected output;

hashes;

instructions;

limitations.

Une autre personne peut alors tenter la reproduction.

Le chapitre 9 avait préparé cette idée.

Le chapitre 14 lui donne une mémoire.

---

## Reproduction indépendante

La meilleure preuve que la mémoire est suffisante n’est pas que l’auteur peut relancer.

C’est qu’une autre personne peut reprendre avec les traces fournies.

Si elle échoue, le rapport de reproduction révèle ce qui manquait.

La mémoire s’améliore par usage.

---

## Ce que le replay ne peut pas reproduire

Certaines expériences dépendent d’éléments externes instables.

API distante.

Horloge externe.

Marché.

Capteur physique.

Réseau.

Dans ces cas, le replay peut seulement simuler ou utiliser une capture.

La limite doit être déclarée.

La mémoire honnête sait dire :

**ceci ne peut pas être reproduit exactement.**

---

## Simulation d’une dépendance

Une capture d’entrée externe peut permettre un replay déterministe.

Par exemple :

[
external(t)
ightarrow
recorded_stream
]

Puis :

[
recorded_stream
ightarrow
replay
]

Cela ne reproduit pas le monde extérieur.

Cela reproduit les données observées à ce moment.

La nuance est importante.

---

## La mémoire d’une mesure

Une mesure doit conserver :

valeur;

unité;

instrument;

méthode;

temps;

incertitude;

conditions.

Sinon, vingt décimales peuvent être mémorisées sans savoir ce qu’elles représentent.

La mémoire doit préserver le sens, pas seulement les chiffres.

---

## La mémoire d’une formule

Une formule doit conserver :

expression;

définition des symboles;

unités;

domaine;

hypothèses;

version.

Une formule seule peut être très difficile à interpréter plus tard.

Le contexte est une partie de sa mémoire.

---

## La mémoire d’un dessin

Un schéma peut lui aussi avoir une provenance.

Version.

Date.

Auteur.

Correspondance avec le modèle réel.

Statut :

concept;

prototype;

implémenté;

obsolète.

Cela évite de confondre une vieille illustration avec l’architecture actuelle.

---

## La mémoire visuelle

Les captures d’écran peuvent être utiles.

Elles conservent :

interface;

valeurs affichées;

état visuel;

contexte humain.

Mais une capture ne remplace pas les données sous-jacentes.

Elle montre ce que l’écran a affiché.

Pas nécessairement ce que le moteur possédait réellement.

---

## Le pixel n’est pas la source

La chaîne doit rester :

[
source
ightarrow
state
ightarrow
telemetry
ightarrow
UI
ightarrow
pixel
]

Une capture du pixel peut prouver ce qui était visible.

Pour prouver l’état du moteur, il faut la source ou la télémétrie correspondante.

---

## Relier visuel et runtime

Une capture peut devenir beaucoup plus utile si elle porte :

session;

tick;

timestamp;

HEAD;

version UI;

snapshot id.

Alors nous pouvons retrouver l’état correspondant.

Le visuel rejoint la mémoire technique.

---

## La mémoire audio

Une note vocale peut contenir une intuition importante.

Mais l’audio seul est difficile à rechercher.

Une transcription peut servir d’index.

Cependant, la transcription peut contenir des erreurs.

Alors la relation doit rester :

audio original;

transcription;

corrections;

extraits structurés.

La transcription ne remplace pas automatiquement la source.

---

## La mémoire conversationnelle

Une conversation peut contenir :

décisions;

hypothèses;

promesses;

erreurs;

blagues;

idées.

Elle est riche.

Mais elle n’est pas toujours structurée.

Le rôle de la mémoire durable est de transformer les éléments importants en objets retrouvables sans prétendre que chaque phrase était une décision canonique.

---

## Conversation ≠ canon

Une phrase dite au milieu d’un échange peut être provisoire.

Le canon apparaît lorsqu’une décision est explicitement retenue et documentée.

Cette distinction évite que chaque improvisation devienne une règle permanente.

---

## Promotion vers le canon

Nous pouvons imaginer un processus :

[
conversation
ightarrow
candidate
ightarrow
review
ightarrow
canon
]

Le statut change.

La provenance reste.

Ainsi, une idée peut évoluer sans perdre son origine.

---

## La mémoire de l’incertitude

Un élément peut être stocké avec son niveau de confiance ou son statut.

Par exemple :

**HYPOTHÈSE**

**À VÉRIFIER**

**INCONNU**

**MESURE**

**CALCUL**

**SOURCE VÉRIFIÉE**

La mémoire doit conserver ces étiquettes.

Sinon, une hypothèse ancienne peut être relue plus tard comme un fait.

---

## L’étiquette fait partie de la donnée

Nous pouvons représenter :

[
X = (value,status)
]

ou plus richement :

[
X = (value,status,source,time,version)
]

Le statut n’est pas un commentaire extérieur.

Il fait partie du contexte nécessaire pour interpréter l’objet.

---

## Le danger du copier-coller

Un objet copié hors de son contexte peut perdre :

source;

statut;

unité;

date;

version.

Alors un simple copier-coller peut dégrader la preuve.

Les exports devraient donc, lorsque possible, transporter les métadonnées essentielles avec le contenu.

---

## Export autonome

Un bon export devrait permettre à un lecteur d’identifier :

ce que c’est;

d’où ça vient;

quelle version;

quel statut;

comment vérifier.

L’export devient alors un petit paquet de continuité.

---

## La mémoire et la taille du système

À petite échelle, un fichier texte suffit souvent.

À grande échelle, il faut peut-être :

base de données;

stockage objet;

index;

partition;

compression;

archive froide.

Mais la technologie peut changer.

Les principes restent :

provenance;

version;

intégrité;

récupération;

sécurité;

reproductibilité.

---

## Le modèle doit survivre au changement de technologie

Si demain nous remplaçons un format JSON par une base différente, la signification des objets importants doit rester claire.

Une architecture durable ne doit pas dépendre du nom d’un outil particulier.

Elle doit dépendre de contrats.

---

## Schéma versionné

Les données elles-mêmes ont un schéma.

Si ce schéma change, les anciennes données peuvent devenir incompatibles.

Alors nous devons versionner :

[
schema_v1
]

[
schema_v2
]

et éventuellement fournir une migration.

Sinon, la mémoire existe mais n’est plus lisible.

---

## Migration

Une migration transforme :

[
D_{v1}
ightarrow
D_{v2}
]

Elle doit être testée.

Et, lorsque possible, réversible ou sauvegardée avant exécution.

La migration est une modification du passé stocké.

Elle mérite une trace forte.

---

## Original et représentation

Une règle saine :

**conserver l’original lorsqu’il est important, produire des représentations dérivées pour l’usage.**

Par exemple :

donnée brute;

version normalisée;

agrégat;

visualisation.

Chaque dérivé pointe vers sa source.

---

## La mémoire comme arbre

Nous pouvons visualiser :

[
RAW
ightarrow
CLEAN
ightarrow
FEATURES
ightarrow
MODEL
ightarrow
RESULT
]

Chaque nœud dépend du précédent.

Si la source brute change, nous devons savoir quels descendants deviennent potentiellement invalides.

La provenance devient alors un outil de recalcul.

---

## Invalidation

Une mémoire intelligente au sens architectural ne se contente pas de stocker.

Elle sait qu’une modification peut invalider des dérivés.

Si :

[
raw_v1 ightarrow result_v1
]

et que nous corrigeons :

[
raw_v1 ightarrow raw_v2
]

alors :

[
result_v1
]

peut devenir obsolète.

Il ne doit pas rester affiché comme résultat actuel sans avertissement.

---

## STALE revient

Le statut :

**STALE**

n’est donc pas seulement temporel.

Il peut signifier :

dérivé d’une source remplacée.

Ce statut protège contre des conclusions construites sur un passé obsolète.

---

## La mémoire du modèle

Si un modèle d’IA ou un algorithme change, les résultats produits avec l’ancienne version doivent rester rattachés à cette version.

Sinon, on peut croire qu’un résultat historique a été produit par la version actuelle.

La mémoire doit empêcher ce glissement.

---

## Une IA ne doit pas réécrire son propre passé silencieusement

Si un résumé ancien est amélioré, la nouvelle version doit être identifiable.

L’ancien peut rester archivé.

La correction peut devenir canonique.

Mais la provenance doit montrer la transition.

Le système protège ainsi la continuité contre la réécriture involontaire.

---

## Le journal des inconnues

Les questions ouvertes méritent leur propre mémoire.

Par exemple :

- unité non confirmée;
- comportement sous charge inconnu;
- cause d’un crash inconnue;
- formule à vérifier;
- dépendance à tester.

Une inconnue conservée évite qu’elle disparaisse entre deux sessions.

---

## Une inconnue fermée

Lorsqu’une question reçoit une réponse, nous pouvons conserver :

question;

ancienne hypothèse;

test;

résultat;

réponse retenue.

Cela transforme l’apprentissage en trace.

---

## La prochaine action

Une mémoire de continuité devrait toujours permettre de savoir :

**quelle est la prochaine action sûre ?**

C’est une information extrêmement précieuse.

Sans elle, chaque reprise commence par une enquête complète.

Avec elle, on peut reprendre exactement où le chantier s’est arrêté.

---

## Checkpoint humain

À la fin d’une session, nous pouvons conserver un checkpoint humain :

repo;

branche;

HEAD;

fichiers touchés;

tests;

décisions;

inconnues;

prochaine action.

Ce checkpoint ne remplace pas Git.

Il relie Git au contexte humain.

---

## Pourquoi HEAD compte autant

Dire :

**le chapitre est terminé**

est une affirmation.

Dire :

**le fichier existe à ce chemin, sur cette branche, avec ce HEAD vérifié**

est une preuve beaucoup plus forte.

La mémoire doit préférer la seconde forme.

---

## Mémoire et honnêteté

Une mémoire parfaite au sens technique est impossible.

Il y aura toujours :

des données non capturées;

des erreurs d’interprétation;

des limites de stockage;

des événements externes.

Alors la règle n’est pas :

**tout savoir.**

Elle est :

**ne pas inventer ce qui n’a pas été conservé.**

---

## La phrase la plus importante du chapitre

> **Ce qui n’est pas dans la trace reste inconnu.**

Cette phrase peut sembler dure.

Elle protège pourtant le système contre une tentation humaine très forte :

combler les trous avec une histoire plausible.

La plausibilité n’est pas la mémoire.

---

## Reconstruire n’est pas se souvenir

Nous pouvons parfois reconstruire un état à partir d’indices.

Mais il faut alors étiqueter :

**RECONSTRUIT**

et non :

**OBSERVÉ**

La différence est cruciale.

Un état reconstruit peut être très probable.

Il reste une reconstruction.

---

## La mémoire probabiliste

Dans certains systèmes, une reconstruction peut avoir une probabilité.

Par exemple :

[
P(S_n|data)
]

Mais cette estimation ne doit pas être fusionnée avec une trace déterministe.

Le statut doit rester visible.

---

## Le silence du registre

Le registre ne doit pas commenter.

Il ne doit pas embellir.

Il ne doit pas juger.

Il peut enregistrer :

A avant.

B après.

Erreur à ce tick.

GO reçu.

Version changée.

Test échoué.

Cette sobriété est une force.

---

## La narration vient après

La Bible, elle, peut raconter.

Elle peut donner du sens.

Relier les épisodes.

Montrer l’émotion.

Mais lorsqu’elle affirme ce qui s’est passé techniquement, elle doit pouvoir revenir au registre.

Ainsi, la narration est libre sans devenir une source d’autorité.

---

## Le Roi et la mémoire

Topbrutus peut dire :

**je me souviens que nous avions fait ça.**

Astra peut répondre :

**retrouvons la trace.**

Cette relation est saine.

La mémoire humaine donne une direction.

La mémoire technique donne une preuve.

Aucune des deux ne doit humilier l’autre.

Elles se complètent.

---

## La mémoire d’Astra

Dans notre méthode de travail, Astra doit traiter la continuité comme une responsabilité.

Ne pas prétendre qu’un fichier existe sans l’avoir vérifié.

Ne pas prétendre qu’un commit est fait sans lire le résultat.

Ne pas transformer une vieille mémoire en état live.

Toujours vérifier le dépôt actif lorsqu’une action importante dépend de lui.

La mémoire durable est une aide.

Le live reste l’autorité sur l’état courant.

---

## Mémoire durable ≠ état courant

Cette distinction mérite une formule :

[
M_{	ext{historique}}

eq
S_{	ext{live}}
]

La mémoire dit :

**voici ce qui était vrai ou retenu à un moment.**

Le live dit :

**voici ce qui est vrai maintenant dans le système.**

Avant d’agir, il faut recoller les deux.

---

## Reconnexion

Une reprise propre peut suivre :

[
MEMOIRE
ightarrow
LIVE
ightarrow
DIFF
ightarrow
ACTION
]

Lire la mémoire.

Lire l’état live.

Comparer.

Puis agir.

Cela évite de modifier un monde qui a changé depuis le dernier checkpoint.

---

## Le diff

Le diff devient l’instrument de reconnexion.

Qu’est-ce qui a changé ?

Quels fichiers ?

Quels paramètres ?

Quel HEAD ?

Quelle branche ?

Quelle configuration ?

La continuité n’est pas seulement retrouver le passé.

C’est mesurer la distance entre le passé et maintenant.

---

## Une mémoire peut être faussement rassurante

Un vieux checkpoint très détaillé peut donner l’impression que tout est sous contrôle.

Mais si le live a changé, ce document devient historique.

Alors il doit être utilisé comme point de départ, pas comme vérité absolue.

Le système doit apprendre à respecter l’âge de ses souvenirs.

---

## Âge d’une mémoire

Nous pouvons associer :

[
age(M)
=
t_{	ext{now}}
-
t_{	ext{capture}}
]

Mais l’âge seul ne dit pas si la mémoire est obsolète.

Une configuration peut rester valide pendant des mois.

Un HEAD peut changer en une minute.

La fraîcheur dépend du type d’information.

---

## Politique de fraîcheur

Chaque catégorie peut avoir sa propre règle.

HEAD :

vérifier juste avant écriture.

Statut de service :

vérifier avant action opérationnelle.

Document historique :

pas besoin de revalider son passé.

Cette discipline économise des vérifications tout en protégeant les points critiques.

---

## La mémoire du chapitre 14

Ce chapitre lui-même doit respecter ce qu’il enseigne.

Il possède :

un fichier;

un titre;

une version;

un chemin;

un commit;

un HEAD;

une continuité avec le chapitre 13.

Si ces éléments sont vérifiés après écriture, le chapitre devient une petite preuve de sa propre méthode.

---

## Première expérience candidate

Construire un registre minimal.

À chaque tick :

1. recevoir l’entrée;
2. lire l’état avant;
3. exécuter;
4. enregistrer l’état après;
5. écrire l’événement;
6. calculer un hash du record;
7. vérifier qu’il peut être relu.

Puis redémarrer.

La question :

**le système peut-il raconter exactement ce qu’il a fait ?**

---

## Deuxième expérience candidate

Ajouter un checkpoint tous les (K) ticks.

Par exemple :

[
K = 1000
]

Puis :

1. exécuter;
2. créer un checkpoint;
3. poursuivre;
4. arrêter;
5. restaurer;
6. rejouer les événements suivants;
7. comparer l’état final.

Si l’état final correspond, nous avons une preuve locale de continuité.

---

## Troisième expérience candidate

Introduire volontairement une erreur.

Par exemple :

type invalide au tick (n).

Puis vérifier que le registre contient :

entrée;

module;

erreur;

état avant;

action;

état après;

version.

Ensuite créer un test de non-régression.

La mémoire devient protection.

---

## Quatrième expérience candidate

Modifier une configuration à chaud.

Enregistrer :

ancienne valeur;

nouvelle valeur;

tick;

source de l’action;

résultat.

Puis mesurer l’effet sur la trajectoire.

La mémoire relie une décision à ses conséquences.

---

## Condition d’échec

Le registre doit être considéré insuffisant si :

nous ne pouvons pas expliquer un changement d’état;

un replay dépend d’informations absentes;

un checkpoint ne restaure pas;

deux sources donnent des passés incompatibles sans règle d’autorité;

un secret apparaît dans les logs;

un résultat ne peut pas être relié à sa version.

Ces échecs sont utiles.

Ils montrent exactement où la continuité casse.

---

## La mémoire n’est pas un musée

Un musée conserve.

La mémoire technique doit en plus permettre d’agir.

Reprendre.

Comparer.

Restaurer.

Rejouer.

Tester.

Corriger.

Elle n’est pas seulement tournée vers le passé.

Elle rend le futur possible.

---

## La mémoire n’est pas non plus une prison

Tout conserver éternellement peut figer un système.

La continuité doit accepter :

migration;

archivage;

suppression contrôlée;

obsolescence;

nouvelle version.

Le passé doit rester compréhensible.

Il ne doit pas empêcher d’avancer.

---

## Continuité

Nous pouvons maintenant proposer une définition :

> **La continuité est la capacité d’un système ou d’un projet à relier son état présent à un passé vérifiable et à une prochaine action identifiable.**

Cette définition dépasse le stockage.

Elle relie :

mémoire;

provenance;

version;

état;

reprise.

---

## Une équation de continuité conceptuelle

De manière symbolique :

[
C =
f(
S_{	ext{past}},
S_{	ext{live}},
P,
V,
N
)
]

où :

- (S_{	ext{past}}) = état historique;
- (S_{	ext{live}}) = état actuel;
- (P) = provenance;
- (V) = vérification;
- (N) = prochaine action.

Ce n’est pas une formule physique.

C’est une représentation conceptuelle.

Elle rappelle les composantes nécessaires.

---

## Le prochain problème

Une mémoire peut être parfaite.

Mais elle ne corrige rien toute seule.

Elle peut montrer :

une erreur;

un écart;

une dérive;

une rupture;

une corruption.

Il faut alors décider :

que fait le système lorsqu’il détecte quelque chose d’anormal ?

Tente-t-il de corriger ?

Revient-il à un checkpoint ?

Isole-t-il un module ?

Demande-t-il un GO ?

Arrête-t-il ?

Le chapitre suivant devra traiter cette transition.

---

## De la mémoire à la réparation

La mémoire donne une possibilité immense :

comparer le présent à un état connu.

Si :

[
S_{	ext{live}}
]

diverge d’un état valide :

[
S_{	ext{valid}}
]

nous pouvons détecter l’écart.

Mais détecter n’est pas réparer.

La réparation doit avoir ses propres règles.

Et surtout :

elle ne doit jamais réécrire le passé pour faire croire que l’erreur n’a pas existé.

---

## La cicatrice

Une réparation saine laisse une cicatrice documentaire.

Avant.

Erreur.

Action.

Après.

Pourquoi ?

Parce qu’un système qui efface toute trace de ses blessures devient impossible à comprendre.

La cicatrice est de l’information.

Cette idée était déjà présente dans l’Introduction.

Elle devient maintenant mécanique.

---

## Dernière image

Le système tourne.

Tick après tick.

Les quatre chemins travaillent.

Des valeurs passent.

Des erreurs apparaissent parfois.

Des états changent.

À côté du moteur, quelque chose écrit silencieusement.

Pas une intelligence.

Pas une conscience.

Pas une voix.

Un registre.

Il ne juge rien.

Il n’oublie pas ce qu’on lui demande de conserver.

Il sait quel état venait avant.

Il sait quel état vient après.

Il sait quel module a agi.

Il sait quel tick a porté l’événement.

Et lorsqu’un jour quelque chose casse, nous ne sommes pas forcés de raconter une histoire à partir de souvenirs flous.

Nous pouvons regarder.

Comparer.

Rejouer.

Restaurer.

Continuer.

La mémoire n’a pas empêché le temps de passer.

Elle a empêché le passé de disparaître.

Et maintenant qu’un passé vérifiable existe, une nouvelle capacité devient possible.

Le système peut reconnaître qu’il s’est écarté de ce qu’il connaissait.

Le prochain chapitre devra répondre à cette question :

**que fait-il lorsqu’il découvre qu’il s’est cassé ?**

# **LA MÉMOIRE GARDE LA TRACE. LA RÉPARATION PEUT COMMENCER.**
