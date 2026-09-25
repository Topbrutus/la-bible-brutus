# Chapitre 18 — Du Module au Système

**APRÈS L’INTRODUCTION — HUITIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** La loi de composition  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Des modules corrects ne garantissent pas un système correct.  
> La composition crée ses propres comportements, ses propres risques et ses propres preuves.**

---

## La fréquence est mesurée. La composition va commencer.

Le chapitre 17 s’est terminé avec un ensemble de pièces mieux définies.

Nous savons maintenant parler de :

ports;

temps;

états;

mémoire;

erreurs;

réparation;

stabilité;

signaux;

fréquences;

phase;

résonance.

Mais une architecture ne devient pas un système simplement parce que chacune de ses pièces possède une fiche technique.

Le vrai saut commence lorsqu’on branche les pièces ensemble.

À cet instant, quelque chose de nouveau apparaît.

Une sortie devient l’entrée d’un autre module.

Une latence s’ajoute à une autre.

Une phase se combine à une autre.

Une erreur traverse un lien.

Un état dépend d’un état précédent.

Un chemin converge avec trois autres.

Une petite décision locale devient une propriété globale.

Le système commence.

---

## Le piège de la confiance locale

Supposons trois modules :

\[
B_1,\;B_2,\;B_3
\]

et supposons que chacun passe parfaitement ses tests unitaires.

Nous pourrions être tentés de conclure :

\[
PASS(B_1)
\land
PASS(B_2)
\land
PASS(B_3)
\Rightarrow
PASS(B_1\circ B_2\circ B_3)
\]

Mais cette implication n’est pas garantie.

Pourquoi ?

Parce que les tests locaux ne couvrent pas nécessairement :

compatibilité des interfaces;

ordre des opérations;

latence cumulée;

synchronisation;

unités;

saturation;

effets d’état;

boucles;

gestion d’erreur;

ressources partagées.

La composition crée de nouveaux objets à tester.

---

## Composition fonctionnelle

Dans un cas simple, deux fonctions peuvent être composées :

\[
f:A\rightarrow B
\]

\[
g:B\rightarrow C
\]

Alors :

\[
g\circ f:A\rightarrow C
\]

avec :

\[
(g\circ f)(x)=g(f(x))
\]

Cette écriture paraît simple.

Mais elle contient déjà une condition :

la sortie de \(f\) doit appartenir au domaine accepté par \(g\).

La compatibilité n’est pas facultative.

---

## Les ports sont des contrats

Le chapitre 12 a donné aux modules des ports.

Nous pouvons maintenant les traiter comme des contrats.

Si :

\[
O_{B_1}
\]

alimente :

\[
I_{B_2}
\]

nous devons vérifier au minimum :

type;

unité;

domaine;

cadence;

statut;

provenance;

politique d’erreur.

Une connexion ne vaut pas seulement parce que les deux ports existent.

Ils doivent être compatibles.

---

## Compatibilité de type

Si :

\[
O_{B_1}\in\mathbb{R}
\]

et que :

\[
I_{B_2}\in\mathbb{R}
\]

la compatibilité de type numérique peut sembler assurée.

Mais elle peut encore échouer sémantiquement.

Une température en Celsius et une fréquence en hertz peuvent toutes deux être des réels.

Le type informatique ne suffit pas.

---

## Type sémantique

Nous pouvons représenter un port comme :

\[
P=(dtype,unit,domain,role)
\]

où :

- \(dtype\) = type informatique;
- \(unit\) = unité;
- \(domain\) = domaine admissible;
- \(role\) = signification.

Deux ports sont compatibles seulement si les conditions nécessaires sont satisfaites.

---

## Le lien comme preuve

Un lien peut donc produire un résultat de validation :

\[
VALIDATE(L_{i\rightarrow j})
\in
\{PASS,FAIL,UNKNOWN\}
\]

Cette validation peut se faire avant exécution.

Nous obtenons alors un avantage énorme :

certaines erreurs sont rejetées avant d’entrer dans le runtime.

---

## Composition statique

Une partie de la composition peut être vérifiée sans faire tourner le système.

Par exemple :

les types existent-ils ?

les unités sont-elles compatibles ?

les ports requis sont-ils connectés ?

les cycles interdits existent-ils ?

des dépendances manquent-elles ?

Cette phase est une vérification structurelle.

---

## Composition dynamique

D’autres propriétés n’apparaissent qu’en exécution.

Latence.

Jitter.

Deadlock.

Race.

Saturation.

Dérive.

Instabilité.

Backpressure.

La composition doit donc être testée à deux niveaux :

\[
STATIC
\]

et :

\[
DYNAMIC
\]

---

## La plaque

Nous pouvons maintenant définir une **plaque** comme un assemblage versionné de modules et de liens.

Conceptuellement :

\[
P=
(M,L,C)
\]

où :

- \(M\) = ensemble de modules;
- \(L\) = ensemble de liens;
- \(C\) = configuration de composition.

La plaque devient un nouvel objet.

Elle peut avoir :

un nom;

une version;

un hash;

des tests;

des entrées;

des sorties;

un statut.

---

## Le module devient composant

Un module seul possède son contrat.

Une plaque expose une interface plus large.

Certains ports internes peuvent disparaître de l’extérieur.

D’autres deviennent les ports publics.

Ainsi :

\[
P_{\text{public}}
\subset
P_{\text{all}}
\]

La plaque cache l’implémentation interne sans cacher les relations importantes.

C’est une différence essentielle.

---

## Cacher n’est pas rendre invisible

L’encapsulation est saine.

Elle permet de ne pas exposer tous les détails à chaque utilisateur.

Mais le système doit encore pouvoir inspecter l’interne lorsqu’il faut diagnostiquer.

Donc :

**encapsulation ≠ mystère.**

Une connexion interne peut être cachée de la vue principale tout en restant définie et traçable.

---

## Interface publique

Une plaque peut déclarer :

### INPUTS

### OUTPUTS

### STATES EXPOSED

### ERRORS EXPOSED

### TIME CONTRACT

### VERSION

Tout le reste peut rester interne.

Cela permet de composer des plaques comme nous composions des modules.

---

## Hiérarchie

Nous obtenons une hiérarchie :

\[
module
\rightarrow
plaque
\rightarrow
sous\text{-}système
\rightarrow
système
\]

Chaque niveau doit posséder un contrat.

Sinon la complexité remonte jusqu’au sommet.

---

## Composition récursive

Une plaque peut elle-même être traitée comme un module au niveau supérieur.

Si elle expose une interface propre, nous pouvons écrire :

\[
P_1\rightarrow P_2
\]

sans avoir besoin de connaître immédiatement chaque lien interne.

Cette propriété permet au système de grandir.

---

## Le contrat doit survivre à l’intérieur

Même si l’intérieur change :

\[
P_v
\rightarrow
P_{v+1}
\]

l’interface publique peut rester compatible.

C’est une forme de stabilité d’API.

Si l’interface change, la version doit le dire.

---

## Version sémantique conceptuelle

Sans imposer un standard particulier, nous pouvons distinguer :

changement compatible;

changement comportemental;

rupture d’interface.

Une version majeure peut signaler une incompatibilité.

Une version mineure peut ajouter une capacité compatible.

Une correction peut modifier un bug sans changer le contrat.

Le schéma exact pourra être choisi plus tard.

---

## Une version n’est pas seulement un numéro

Elle doit pointer vers :

code;

configuration;

tests;

dépendances;

artefact.

Sinon deux systèmes portant le même numéro peuvent être différents.

---

## Le manifest

Une plaque exportable peut avoir un manifeste.

Par exemple :

\[
MANIFEST=
(id,version,modules,links,ports,tests,hashes)
\]

Ce manifeste devient la carte d’identité de la composition.

---

## Dépendances

Un module peut dépendre d’un autre.

Une plaque peut dépendre d’une bibliothèque.

Un sous-système peut dépendre d’un service.

Ces dépendances forment un graphe.

\[
G_D=(V_D,E_D)
\]

Analyser ce graphe peut révéler :

cycles;

points critiques;

dépendances uniques;

chaînes longues.

---

## Dépendance directe et transitive

Si :

\[
A\rightarrow B
\]

et :

\[
B\rightarrow C
\]

alors A dépend transitivement de C.

Un changement dans C peut donc affecter A même sans lien direct.

La provenance des dépendances doit être conservée.

---

## Le diamant

Une structure classique peut apparaître :

\[
A\rightarrow B
\]

\[
A\rightarrow C
\]

puis :

\[
B\rightarrow D
\]

\[
C\rightarrow D
\]

Si B et C exigent deux versions incompatibles de D, la composition peut casser.

Les conflits de dépendances sont des problèmes de système.

---

## Verrouiller les versions

Pour une expérience reproductible, les versions de dépendances peuvent être figées.

Ainsi, un run aujourd’hui et un run demain utilisent les mêmes éléments.

Sans verrouillage, une mise à jour externe peut modifier le résultat sans changement apparent de notre propre code.

---

## Composition temporelle

Deux modules corrects peuvent produire une composition incorrecte s’ils n’utilisent pas le temps de la même manière.

Par exemple :

B1 produit toutes les 10 ms.

B2 consomme toutes les 100 ms.

Que se passe-t-il entre les deux ?

Buffer ?

Dernière valeur ?

Accumulation ?

Drop ?

La politique doit être définie.

---

## Adaptateur temporel

Nous pouvons insérer un module :

\[
A_T
\]

qui adapte les cadences.

Par exemple :

agrégation;

downsampling;

upsampling;

interpolation;

hold.

Mais l’adaptation modifie l’information.

Elle doit être visible.

---

## Downsampling

Réduire la fréquence d’échantillonnage peut créer de l’aliasing si la bande n’est pas limitée auparavant.

Un adaptateur temporel sérieux peut donc exiger un filtrage anti-aliasing.

La composition rejoint directement le chapitre 17.

---

## Upsampling

Augmenter le nombre d’échantillons ne crée pas automatiquement de nouvelle information.

Une interpolation reconstruit selon un modèle.

Le statut doit rester clair.

---

## Composition des latences

Pour une chaîne séquentielle simple :

\[
B_1\rightarrow B_2\rightarrow B_3
\]

la latence de bout en bout peut être approximativement :

\[
L_{\text{total}}
=
L_1+L_{12}+L_2+L_{23}+L_3
\]

où les liens et modules contribuent.

Mais pour un pipeline parallèle, la formule change.

---

## Latence parallèle

Si quatre chemins fonctionnent en parallèle et qu’une jonction attend tous les chemins :

\[
L_{\text{join}}
\approx
\max(L_1,L_2,L_3,L_4)
+
L_J
\]

selon le modèle.

Le chemin le plus lent devient critique.

---

## Critical path

Dans un graphe de tâches, le chemin critique correspond au chemin qui détermine la durée totale selon les dépendances.

Identifier ce chemin permet de savoir où optimiser.

Optimiser un module hors chemin critique peut n’avoir presque aucun effet sur la latence globale.

---

## Optimisation locale, effet nul

Supposons :

\[
P_1=2\text{ ms}
\]

\[
P_2=3\text{ ms}
\]

\[
P_3=40\text{ ms}
\]

\[
P_4=4\text{ ms}
\]

Réduire P1 de 2 ms à 1 ms ne change presque pas une jonction qui attend P3.

L’optimisation doit suivre la structure.

---

## Backpressure composée

Un producteur rapide peut saturer un consommateur lent.

Dans une chaîne :

\[
A\rightarrow B\rightarrow C
\]

si B ralentit, A peut continuer à produire.

Le backlog augmente.

La pression doit remonter ou la perte doit être définie.

---

## Contrat de débit

Un lien peut déclarer :

\[
\lambda_{\max}
\]

et :

\[
Q_{\max}
\]

pour le débit et la taille de file.

Lorsque les limites sont atteintes :

drop;

block;

degrade;

error.

La politique doit être testée.

---

## La saturation globale

Chaque module peut être sous sa limite individuelle et le système peut quand même saturer une ressource partagée.

CPU.

Mémoire.

Disque.

Réseau.

GPU.

La composition introduit des ressources globales.

---

## Budget partagé

Nous pouvons définir :

\[
\sum_i CPU_i
\le
CPU_{\text{budget}}
\]

et des contraintes analogues pour d’autres ressources.

Mais les pics simultanés peuvent être plus importants que les moyennes.

La télémétrie doit regarder les distributions.

---

## Mémoire partagée

Deux modules peuvent fonctionner correctement seuls et provoquer ensemble une pression mémoire trop forte.

Encore une fois :

PASS local n’implique pas PASS global.

---

## Port STATE partagé

Partager un état mutable entre plusieurs modules peut créer des races et dépendances cachées.

Une architecture plus sûre peut préférer :

propriétaire unique;

messages explicites;

copies immuables;

transactions.

Le choix dépend du besoin.

---

## Single writer

Une règle utile :

> **Une donnée mutable critique possède idéalement une source d’écriture clairement identifiée.**

Plusieurs lecteurs peuvent exister.

Mais plusieurs écrivains demandent une coordination forte.

---

## Multi-writer

Si plusieurs modules peuvent modifier le même état, il faut définir :

ordre;

conflit;

merge;

priorité;

transaction;

verrouillage.

Sans cela, le résultat dépend de la course.

---

## Transactions

Une transaction peut regrouper plusieurs modifications.

Elle vise à préserver des propriétés telles que cohérence et atomicité selon le système.

Mais toutes les architectures n’utilisent pas une base transactionnelle.

Le principe général reste :

les changements liés doivent être coordonnés.

---

## État distribué

Lorsque l’état est réparti entre plusieurs processus ou machines, la composition devient plus difficile.

Nous devons traiter :

réplication;

partition;

retard;

conflit;

ordre.

Le système ne doit pas prétendre posséder un état global instantané parfait si ce n’est pas garanti.

---

## Cohérence

Le mot cohérence doit être défini.

Cohérence forte ?

Éventuelle ?

Par session ?

Par clé ?

Les systèmes distribués possèdent plusieurs modèles.

Si Brutus devient distribué, il faudra choisir explicitement.

---

## Le réseau est un composant

Un lien réseau n’est pas une flèche magique.

Il possède :

latence;

perte;

réordre;

duplication;

déconnexion;

MTU;

débit.

Une architecture distribuée doit tester ces réalités.

---

## Message

Un message peut porter :

\[
M=(id,source,destination,type,payload,tick,time,trace)
\]

Cette structure rend le transfert inspectable.

---

## Identifiant de message

Un identifiant unique permet de détecter :

duplication;

replay;

corrélation;

trace.

Il ne garantit pas tout.

Mais il donne une identité à l’événement réseau.

---

## Delivery semantics

Une architecture peut offrir différentes garanties.

At-most-once.

At-least-once.

Exactly-once dans certains contextes et sous certaines définitions.

Ces termes doivent être utilisés avec précision.

Un système qui peut livrer deux fois doit rendre ses consommateurs capables de gérer les doublons si nécessaire.

---

## Idempotence revient

Une commande :

SET X=5

peut être répétée avec moins de risque qu’une commande :

ADD 5

La sémantique de l’opération influence la robustesse de la composition.

---

## Correlation ID

Une requête peut traverser plusieurs modules.

Un identifiant de corrélation permet de suivre :

\[
A\rightarrow B\rightarrow C\rightarrow D
\]

comme une seule transaction logique.

Le registre de continuité devient distribué.

---

## Trace ID

Nous pouvons utiliser un identifiant de trace pour relier :

entrée;

sous-appels;

sorties;

erreurs.

Ainsi, une sortie finale peut être remontée à sa cause.

---

## Span

Dans les systèmes d’observabilité, une trace peut être composée de spans.

Chaque span représente une opération avec :

début;

fin;

parent;

statut.

Cette structure est très compatible avec notre registre.

Nous n’avons pas besoin de la réinventer.

---

## Observabilité de composition

Une plaque devrait exposer :

latence;

débit;

erreurs;

files;

états;

dépendances;

traces.

Mais l’observabilité elle-même a un coût.

Le niveau de détail doit être réglable.

---

## Le système ne doit pas devenir opaque en grandissant

C’est l’un des plus grands risques de la composition.

Un seul module est compréhensible.

Cent modules deviennent une forêt.

Alors nous devons conserver :

hiérarchie;

noms;

groupes;

interfaces;

traces;

vues filtrées.

La complexité visuelle doit être gérée sans supprimer la vérité.

---

## Vue macro et vue micro

La vue macro montre :

plaques;

flux principaux;

statuts.

La vue micro montre :

ports;

messages;

ticks;

erreurs;

transformations.

Les deux doivent pointer vers le même modèle.

---

## Une seule source de topologie

L’interface ne devrait pas avoir sa propre carte indépendante.

La topologie affichée doit venir du graphe réel ou d’un manifeste canonique.

Sinon le dessin peut dériver du système.

---

## Graphe de composition

Nous pouvons définir :

\[
G_C=(V,E)
\]

où :

- \(V\) = modules ou plaques;
- \(E\) = contrats de connexion.

Chaque nœud et chaque arête possède :

version;

statut;

type;

provenance.

Le graphe devient un objet versionné.

---

## Hash du graphe

Une configuration de composition peut être canonisée puis hachée.

\[
h_G=H(G_C)
\]

Cela permet de savoir si deux runs utilisaient exactement la même topologie, selon la représentation choisie.

Le hash ne prouve pas la validité.

Il prouve l’identité du contenu encodé.

---

## Topologie et comportement

Deux systèmes avec les mêmes modules mais des liens différents peuvent se comporter différemment.

Donc :

\[
M_{\text{same}}
\not\Rightarrow
System_{\text{same}}
\]

La topologie fait partie de la version.

---

## Configuration comme code

Une composition peut être décrite dans un fichier versionné.

Cela permet :

diff;

review;

rollback;

reproduction.

La topologie devient alors inspectable comme le code.

---

## Validation avant activation

Une nouvelle topologie peut passer par :

parse;

schema;

type check;

cycle check;

dependency check;

dry run;

simulation;

activation.

Le système ne doit pas brancher une architecture invalide simplement parce qu’un fichier se charge.

---

## Dry run de composition

Avant d’activer :

quels liens seront créés ?

quels seront supprimés ?

quels modules redémarreront ?

quels états seront perdus ?

quelles incompatibilités existent ?

Le dry run produit un diff.

Puis le GO peut autoriser l’application.

---

## Hot swap

Certains modules peuvent être remplacés sans arrêter tout le système.

Mais un hot swap demande :

compatibilité d’interface;

transfert ou abandon d’état;

version;

synchronisation;

rollback.

C’est une opération complexe.

---

## State transfer

Si B1 est remplacé par B1', son état peut devoir être migré.

\[
S_{B1}
\rightarrow
S_{B1'}
\]

Cette transformation doit être définie.

Un état ancien peut être incompatible avec la nouvelle version.

---

## Stateless

Un module sans état est plus facile à remplacer.

Il reçoit une entrée et produit une sortie.

Mais même un module stateless peut dépendre de :

configuration;

version;

ressources externes.

Le mot ne signifie pas absence de dépendances.

---

## Stateful

Un module stateful exige une politique pour :

checkpoint;

migration;

recovery;

concurrence;

replay.

La composition doit savoir où vit l’état.

---

## Ownership

Chaque état important doit avoir un propriétaire logique.

Qui écrit ?

Qui restaure ?

Qui versionne ?

Qui valide ?

L’ownership réduit l’ambiguïté.

---

## Le système de types de Brutus

À mesure que la composition grandit, un système de types devient précieux.

Par exemple :

Signal[Hz]

Duration[s]

Phase[rad]

Amplitude[V]

State[ModuleX]

Error[Code]

Cette notation peut prévenir des branchements absurdes.

---

## Dimensions

Pour les grandeurs physiques, une vérification dimensionnelle peut être intégrée.

Si un module attend :

\[
[T^{-1}]
\]

et reçoit :

\[
[T]
\]

la connexion doit échouer sauf adaptateur explicite.

---

## Adaptateurs

Un adaptateur est un module.

Il doit donc lui aussi avoir :

version;

tests;

contrat;

trace.

Nous ne devons pas cacher une conversion dans le lien.

---

## Conversion d’unité

Par exemple :

\[
T=2\text{ ms}
\]

devient :

\[
T=0.002\text{ s}
\]

La conversion est déterministe.

Elle peut être testée.

---

## Conversion de sens

D’autres adaptateurs modifient davantage.

Une période vers une fréquence :

\[
f=\frac{1}{T}
\]

demande :

\[
T>0
\]

L’adaptateur doit gérer le domaine invalide.

---

## Composition fréquentielle

Deux filtres en cascade, dans un cadre LTI, donnent :

\[
H_{\text{total}}(f)
=
H_1(f)H_2(f)
\]

La magnitude se multiplie.

Les phases s’additionnent :

\[
\phi_{\text{total}}
=
\phi_1+\phi_2
\]

Cela montre directement comment une composition correcte localement peut produire un effet global inattendu.

---

## Gain cumulé

Si chaque module ajoute un gain modéré :

\[
G_1=2
\]

\[
G_2=2
\]

\[
G_3=2
\]

alors :

\[
G_{\text{total}}=8
\]

Une chaîne peut saturer même si chaque étage paraît raisonnable seul.

---

## Phase cumulée

Des déphasages peuvent s’accumuler.

Dans une boucle de feedback, cette accumulation peut devenir critique.

La composition doit donc analyser la réponse globale, pas seulement les modules.

---

## Boucle

Une topologie avec feedback :

\[
A\rightarrow B\rightarrow C\rightarrow A
\]

n’est pas équivalente à une chaîne.

Elle introduit une dynamique récursive.

Il faut analyser la stabilité de boucle.

---

## Boucle algébrique

Si des modules dépendent instantanément les uns des autres sans délai ou ordre défini, une boucle algébrique peut apparaître.

Il faut parfois résoudre un système d’équations plutôt que d’exécuter séquentiellement.

Le moteur doit détecter ce cas.

---

## Délai explicite

Ajouter un état ou un délai :

\[
z^{-1}
\]

dans un système discret peut rompre une boucle instantanée.

Mais cela modifie la dynamique.

Le délai doit être un choix explicite.

---

## Transformée en Z et composition

Pour certains systèmes discrets LTI, la transformée en Z permet d’analyser les blocs et leur composition.

Mais nous ne devons utiliser cet outil que lorsque le modèle convient.

Le nom Z stéréo reste distinct.

---

## Les quatre chemins comme plaque

Nous pouvons maintenant définir une plaque candidate :

\[
P_4 =
D
\rightarrow
(P_1,P_2,P_3,P_4)
\rightarrow
J
\]

où :

- \(D\) = divergence;
- \(P_k\) = chemins;
- \(J\) = jonction.

Cette plaque expose une entrée et une sortie.

Elle devient testable comme un seul objet.

---

## Contrat de P4

### INPUT

type, unité, cadence.

### OUTPUT

type, unité, statut.

### TIME

règle de tick.

### ERROR

politique de branche.

### STATE

états de chaque chemin + jonction.

### TRACE

trace ID commun.

Ce contrat transforme quatre chemins en un composant architectural.

---

## Chaque chemin doit être identifiable

Nous voulons :

\[
path\_id\in\{1,2,3,4\}
\]

Chaque sortie porte son origine.

La jonction sait exactement qui manque.

---

## La jonction ne doit pas mélanger sans contrat

Une jonction peut :

additionner;

moyenner;

voter;

concaténer;

sélectionner;

comparer.

Le choix doit être une fonction :

\[
J(y_1,y_2,y_3,y_4)
\]

et non une intuition visuelle.

---

## Pondération

Une somme pondérée peut être :

\[
y
=
\sum_{k=1}^{4}w_ky_k
\]

avec :

\[
\sum_{k=1}^{4}w_k=1
\]

si cette normalisation est voulue.

Les poids deviennent des paramètres.

Ils doivent être versionnés.

---

## Poids fixes ou adaptatifs

Des poids fixes sont simples.

Des poids adaptatifs peuvent évoluer selon la qualité des chemins.

Mais l’adaptation introduit :

état;

règles;

risque;

provenance.

Elle doit laisser une trace.

---

## Qualité d’un chemin

Nous pouvons définir une qualité :

\[
q_k
\]

à partir de :

latence;

SNR;

erreur;

fraîcheur;

health.

Mais un score unique doit rester explicable.

---

## Sélecteur

Une jonction peut choisir :

\[
y=y_{k^\*}
\]

où :

\[
k^\*
=
\arg\max_k q_k
\]

Cela paraît élégant.

Mais si \(q_k\) est mal défini, le système choisit mal.

La logique de sélection devient critique.

---

## Vote

Une jonction peut comparer plusieurs réponses.

Mais le vote n’est valide que si les chemins sont suffisamment indépendants et si le problème se prête à une règle de vote.

Quatre copies du même bug peuvent voter faux ensemble.

---

## Diversité

Une vraie redondance peut utiliser des implémentations différentes.

Mais cette diversité coûte cher.

Elle peut réduire certains risques de faute commune.

Le choix doit venir du niveau de criticité.

---

## Composition des erreurs

Chaque module possède ses erreurs.

La plaque doit décider comment les exposer.

Une erreur interne mineure peut rester locale.

Une erreur critique doit remonter.

Nous pouvons définir une fonction :

\[
E_P
=
Aggregate(E_1,\ldots,E_n)
\]

La règle d’agrégation doit être claire.

---

## Erreur masquée

Un module peut échouer pendant que la sortie globale reste valide.

C’est acceptable si le protocole le permet.

Mais l’erreur ne doit pas disparaître du registre.

Le système peut être :

\[
OUTPUT=VALID
\]

et :

\[
HEALTH=DEGRADED
\]

en même temps.

---

## Plusieurs vérités de statut

Cela montre qu’un statut unique est souvent insuffisant.

Nous pouvons avoir :

fonctionnel;

sain;

complet;

synchronisé;

stable.

Chaque dimension répond à une question différente.

---

## Machine à états de la plaque

Une plaque peut avoir :

INIT.

READY.

RUNNING.

DEGRADED.

RECOVERING.

BLOCKED.

STOPPED.

ERROR.

Les transitions doivent être définies.

---

## Transition valide

Par exemple :

\[
INIT\rightarrow READY
\]

seulement si :

ports validés;

dépendances disponibles;

clock sync;

config chargée;

health pass.

READY n’est plus un voyant arbitraire.

---

## Transition interdite

\[
ERROR\rightarrow RUNNING
\]

peut être interdite sans passage par :

\[
RECOVERING
\]

et :

\[
VERIFY
\]

selon le protocole.

Les états protègent le système.

---

## Composition des permissions

Un sous-système peut aussi posséder des capacités.

Lecture.

Écriture.

Restart.

Configure.

Publish.

Ces permissions doivent suivre la hiérarchie.

Un module interne ne devrait pas obtenir automatiquement toutes les permissions du système parent.

---

## Principe de moindre privilège

Chaque composant reçoit les permissions nécessaires à son rôle, pas davantage.

Cela réduit le rayon d’impact d’une erreur ou compromission.

---

## Un lien est aussi une permission

Autoriser B1 à envoyer vers B2 signifie que B1 peut influencer B2.

La topologie est donc aussi une carte de pouvoir.

Cette idée renforce notre première loi :

aucune connexion invisible.

---

## Capability

Une capacité peut être représentée comme une autorisation explicite d’action.

Le système peut vérifier :

qui peut faire quoi sur quelle cible.

Cela évite les appels globaux implicites.

---

## Composition et sécurité

Un système peut être sûr module par module mais vulnérable à cause de la manière dont les modules sont reliés.

Par exemple :

un parseur public alimente directement une fonction privilégiée.

La sécurité doit analyser les chemins complets.

---

## Trust boundary

Une frontière de confiance indique où des données passent d’un domaine moins fiable vers un domaine plus privilégié.

À cette frontière :

validation;

authentification;

autorisation;

sanitization;

logging.

Le lien devient critique.

---

## Entrée externe

Toute entrée externe doit être considérée non fiable jusqu’à validation selon le contexte.

Cela ne signifie pas hostile.

Cela signifie :

non vérifiée.

---

## Composition et validation

Une validation peut être locale.

Mais si un module transforme les données, le module suivant doit savoir ce qu’il peut supposer.

Les invariants doivent être transmis ou revalidés.

---

## Post-condition

Un module peut garantir une post-condition :

\[
Q(y)=TRUE
\]

si ses préconditions ont été respectées.

Le module suivant peut utiliser cette garantie.

Cela rapproche la composition du design by contract.

---

## Précondition

\[
P(x)=TRUE
\]

est nécessaire avant l’exécution.

Si elle échoue :

le module ne doit pas prétendre produire une sortie normale.

---

## Contrat complet

Conceptuellement :

\[
\{P\}\;F\;\{Q\}
\]

Cela signifie :

si P est vrai avant F, Q doit être vrai après, selon le contrat.

Cette logique peut inspirer nos modules.

---

## Le système entier a lui aussi des invariants

Même si tous les modules respectent les leurs, le système peut avoir des invariants supplémentaires.

Par exemple :

les quatre chemins doivent partager le même tick;

la somme des poids vaut 1;

une seule Reine est active;

aucun output critique ne vient d’un chemin STALE.

Ces règles n’appartiennent à aucun module seul.

Elles appartiennent à la composition.

---

## Invariant global

Nous pouvons écrire :

\[
I_G(S)=TRUE
\]

Le test du système doit vérifier ces invariants globaux.

Ils sont la preuve que le tout respecte ses propres règles.

---

## Emergence technique

Le mot émergence peut être utilisé sobrement.

Une propriété globale peut apparaître à partir des interactions sans être une propriété individuelle d’un module.

Par exemple :

throughput global;

latence de bout en bout;

oscillation de boucle;

deadlock;

synchronisation.

Cela ne signifie pas magie.

Cela signifie :

propriété de la composition.

---

## Comportement émergent indésirable

Deux modules peuvent chacun avoir une logique correcte et créer ensemble une oscillation.

Le problème ne vit ni entièrement dans A ni entièrement dans B.

Il vit dans la boucle A↔B.

Le diagnostic doit donc pouvoir pointer vers une relation.

---

## Les liens doivent pouvoir être coupables

Notre registre ne doit pas seulement attribuer les erreurs aux modules.

Un lien peut être la cause :

mauvais type;

retard;

duplication;

perte;

conversion;

buffer overflow.

Les relations sont des objets de première classe.

---

## Test d’intégration

Le test unitaire vérifie un module.

Le test d’intégration vérifie plusieurs composants ensemble.

C’est ici que nous testons :

interfaces;

flux;

ordre;

erreurs;

time;

state.

Chaque nouvelle plaque devrait posséder ses tests d’intégration.

---

## Test end-to-end

Un test end-to-end traverse le système depuis une entrée réelle ou représentative jusqu’à la sortie finale.

Il vérifie la chaîne complète.

Il est plus coûteux et parfois plus fragile que les tests unitaires.

Mais il détecte des problèmes invisibles localement.

---

## Pyramide de tests

Nous pouvons imaginer :

beaucoup de tests unitaires;

moins de tests d’intégration;

quelques tests end-to-end;

plus des tests de stabilité, charge et panne.

Ce n’est pas une loi absolue.

C’est une stratégie fréquente pour équilibrer vitesse et couverture.

---

## Test contractuel

Deux modules peuvent tester leur contrat sans démarrer tout le système.

Le producteur garantit un format.

Le consommateur vérifie qu’il l’accepte.

Cela peut réduire les surprises d’intégration.

---

## Golden test

Pour certaines transformations déterministes, nous pouvons conserver une entrée et une sortie attendue.

\[
F(x^\*)=y^\*
\]

Cela permet de détecter une modification inattendue.

Mais les golden files doivent être révisés avec prudence.

Changer l’attendu pour faire passer un test peut cacher une régression.

---

## Snapshot test

Une interface ou structure complexe peut être comparée à un snapshot.

Mais le snapshot doit être lisible ou accompagné de tests sémantiques.

Sinon on peut accepter un gros diff sans comprendre.

---

## Property-based testing

Au lieu de tester seulement quelques exemples, on peut tester des propriétés sur de nombreux cas générés.

Par exemple :

pour tout input valide, l’output respecte le domaine.

Ou :

encode puis decode redonne l’entrée.

Cette méthode peut découvrir des cas limites inattendus.

---

## Fuzzing de composition

Nous pouvons varier :

ordre des messages;

timing;

valeurs limites;

pertes;

doublons.

Le but est de découvrir les zones où les contrats se brisent.

---

## Test de redémarrage composé

Arrêter B2.

Observer B1 et B3.

Redémarrer B2.

Vérifier :

reconnexion;

état;

duplication;

replay;

synchronisation.

C’est un vrai test de système.

---

## Test de panne réseau

Couper le lien entre deux plaques.

Mesurer :

détection;

backpressure;

timeout;

mode dégradé;

récupération.

Le réseau ne doit pas être supposé parfait.

---

## Test de version mixte

Dans un déploiement progressif, deux versions peuvent coexister.

\[
v1\leftrightarrow v2
\]

L’interface doit rester compatible pendant la transition si le protocole l’exige.

Sinon la mise à jour doit être atomique.

---

## Backward compatibility

Une nouvelle version peut continuer à accepter l’ancien format.

Cela facilite la migration.

Mais cette compatibilité a un coût.

Elle doit avoir une durée ou politique.

---

## Forward compatibility

Un ancien composant peut parfois ignorer des champs inconnus d’un nouveau format.

Cela peut aider.

Mais seulement si les champs ignorés ne sont pas critiques.

---

## Schéma évolutif

Les messages doivent être versionnés.

Une transformation de schéma doit être explicite.

Le système doit éviter les formats où un changement silencieux casse les consommateurs.

---

## Le numéro 1 203 930

Notre formule fondatrice :

\[
3\times(6+1)\times7\times7\times9\times10\times13
=
1\,203\,930
\]

est un objet mathématique défini.

Dans une architecture de composition, elle peut servir comme :

identifiant symbolique;

paramètre;

seed;

taille candidate;

structure combinatoire;

référence documentaire.

Mais son rôle doit être explicitement choisi.

Le fait qu’elle soit importante dans notre histoire ne lui donne pas automatiquement une fonction technique.

---

## Du symbole au paramètre

Si nous choisissons :

\[
N=1\,203\,930
\]

comme paramètre réel d’un algorithme, nous devons expliquer pourquoi ce nombre est adapté à cette fonction.

Sinon il reste symbolique.

Les deux usages peuvent coexister.

Ils doivent être étiquetés.

---

## 7⁴ = 2401

De même :

\[
7^4=2401
\]

est un calcul exact.

Il peut devenir une taille de grille, un nombre d’états ou un paramètre si une architecture le demande.

Mais la relation mathématique ne prouve pas que 2401 est optimal pour cette architecture.

L’optimisation demande un test.

---

## 273

Le PPCM :

\[
\operatorname{ppcm}(3,7,13)=273
\]

est une propriété arithmétique exacte.

Cette valeur peut servir naturellement à aligner des cycles de longueurs 3, 7 et 13.

C’est un exemple de composition mathématique réelle.

---

## Alignement de cycles

Si trois compteurs ont des périodes :

\[
3,\;7,\;13
\]

ils reviennent simultanément à leur origine après :

\[
273
\]

étapes.

Cette propriété peut devenir utile dans un scheduler discret ou un modèle cyclique.

Ici, le lien entre mathématique et mécanisme est explicite.

---

## Le cycle global

Nous pouvons définir un tick global :

\[
n\in\{0,\ldots,272\}
\]

et des sous-phases :

\[
a=n\bmod3
\]

\[
b=n\bmod7
\]

\[
o=n\bmod13
\]

Après 273 ticks :

\[
(a,b,o)
\]

revient au même triplet.

C’est un mécanisme parfaitement testable.

---

## Relation avec R

Une relation comme :

\[
R(a,b,o)
=
(91a+39b+21o)\bmod273
\]

peut être étudiée comme un mapping sur ces états.

Nous pouvons tester :

collision;

couverture;

bijection éventuelle selon le domaine défini;

distribution.

Ce sont des questions mathématiques précises.

---

## Tester le mapping

Si le domaine contient :

\[
3\times7\times13=273
\]

triplets possibles, nous pouvons énumérer les 273 états.

Puis mesurer :

nombre de résidus distincts;

collisions;

ordre;

période.

Ce test pourrait devenir un artefact très fort du projet.

---

## Composition arithmétique avant interprétation

Avant de parler de fréquence, conscience, onde ou physique, nous pouvons prouver les propriétés du mapping.

C’est exactement notre méthode :

mathématique d’abord.

Interprétation ensuite.

---

## Une plaque Seed Cycle candidate

Nous pourrions imaginer :

\[
TICK
\rightarrow
(a,b,o)
\rightarrow
R
\rightarrow
\Theta
\]

avec :

\[
\Theta=2\pi R/273
\]

Cette plaque possède une entrée logique et une sortie angulaire.

Elle est déterministe.

Elle peut être testée exhaustivement sur 273 états.

---

## Preuve exhaustive

Lorsque le domaine est petit, il n’est pas nécessaire d’échantillonner.

Nous pouvons tester tous les cas.

Cela donne une preuve logicielle beaucoup plus forte pour la propriété vérifiée.

---

## Exhaustif ne signifie pas universel

Tester les 273 entrées prouve le comportement de cette implémentation sur ce domaine.

Cela ne prouve pas une loi du monde physique.

La frontière reste claire.

---

## Module mathématique pur

Cette plaque pourrait être pure :

pas d’I/O externe;

pas de temps réel;

pas de random;

pas d’état caché.

Alors :

\[
output=F(input)
\]

Elle serait extrêmement reproductible.

C’est un excellent noyau de composition.

---

## Ajouter le temps plus tard

Ensuite, nous pouvons définir comment le tick réel fait avancer \(n\).

Puis seulement introduire :

cadence;

signal;

son;

visualisation.

Cette séparation empêche le temps réel de contaminer les preuves arithmétiques.

---

## Architecture en couches

Nous pouvons définir quatre couches :

### L0 — MATH
Calcul pur.

### L1 — STATE/TIME
Tick, état, scheduler.

### L2 — SIGNAL
Génération ou analyse de signaux.

### L3 — VIEW
Interface et visualisation.

Chaque couche dépend de la précédente selon un contrat.

---

## La couche visuelle ne remonte pas

Une règle possible :

\[
L3\nrightarrow L0
\]

La vue ne modifie pas le noyau mathématique sans un canal de commande explicite.

Cela protège la source d’autorité.

---

## Canal de commande

Si l’utilisateur change un paramètre via l’interface :

\[
UI
\rightarrow
COMMAND
\rightarrow
VALIDATE
\rightarrow
CORE
\]

Le chemin est explicite.

L’UI ne modifie pas directement une variable interne.

---

## Read model

L’interface peut lire une projection :

\[
STATE
\rightarrow
READ\_MODEL
\rightarrow
UI
\]

Cette projection peut être optimisée pour l’affichage.

Elle n’est pas nécessairement la source canonique.

---

## Command model

Les commandes suivent une autre voie.

Cette séparation réduit les couplages invisibles.

---

## Composition des quatre chemins par couches

Chaque \(P_k\) peut lui-même suivre :

\[
INPUT
\rightarrow
MATH
\rightarrow
STATE
\rightarrow
SIGNAL
\rightarrow
OUTPUT
\]

ou une structure adaptée.

L’important est que le pipeline soit explicite.

---

## Le Z stéréo comme plaque

Le futur Z stéréo peut devenir une plaque indépendante.

Entrées :

deux canaux ou deux phases.

Paramètres :

mapping Brutus.

Sorties :

phase relative;

offset;

signal transformé;

métriques.

Le nom devient concret.

---

## Prêt à attendre son entrée

Une plaque peut être dans l’état :

\[
READY
\]

avec aucune donnée active.

Elle attend.

Lorsqu’une entrée valide arrive :

\[
READY\rightarrow RUNNING
\]

Cette mécanique traduit proprement notre image :

**prêt à attendre son entrée et écouter.**

---

## Le cœur comme scheduler

Si le mot cœur désigne le composant qui cadence ou orchestre, nous pouvons le formaliser.

Il ne doit pas calculer toutes les fonctions.

Il peut émettre :

tick;

barrière;

état global minimal.

Le reste appartient aux modules.

---

## Orchestrateur vs chorégraphie

Une architecture peut utiliser un orchestrateur central qui dit aux composants quoi faire.

Ou une chorégraphie où les composants réagissent aux événements.

Les deux styles ont des avantages et risques.

Le choix doit être conscient.

---

## Orchestration

Avantage :

flux central visible.

Risque :

point central complexe.

---

## Chorégraphie

Avantage :

composants plus autonomes.

Risque :

flux global difficile à comprendre.

Dans Brutus, notre règle de traçabilité impose que même une chorégraphie conserve une vue globale reconstruisible.

---

## Le graphe d’exécution

À chaque run, la topologie statique produit un graphe d’exécution réel.

Certaines branches peuvent être bypass.

Certaines erreurs peuvent modifier le chemin.

Nous devons donc distinguer :

\[
G_{\text{configured}}
\]

et :

\[
G_{\text{executed}}
\]

Le deuxième est la preuve de ce qui s’est réellement passé.

---

## Configuré n’est pas exécuté

Une connexion présente dans la configuration peut n’avoir jamais transporté de donnée.

Une branche peut être disponible mais inactive.

Le registre doit pouvoir montrer la différence.

---

## Coverage de chemin

Nous pouvons mesurer quels chemins ont réellement été exercés pendant les tests.

Un système peut avoir 100 branches mais n’en tester que 20.

La couverture ne prouve pas la correction.

Mais elle montre ce qui n’a pas été exercé.

---

## Couverture de composition

Au niveau système, nous pouvons suivre :

liens traversés;

états visités;

transitions;

erreurs déclenchées;

modes dégradés.

Cela aide à construire une matrice de tests.

---

## Matrice de compatibilité

Pour plusieurs versions :

\[
B1_{v1},B1_{v2}
\]

\[
B2_{v1},B2_{v2}
\]

nous pouvons tester les combinaisons supportées.

La matrice devient une preuve de compatibilité.

---

## Explosion combinatoire

Plus nous avons de modules et paramètres, plus les combinaisons explosent.

Nous ne pouvons pas tout tester exhaustivement à grande échelle.

Alors nous devons choisir :

classes d’équivalence;

limites;

risques;

property tests;

fuzzing;

scénarios critiques.

---

## Priorisation par risque

Les chemins qui peuvent provoquer :

perte de données;

action irréversible;

corruption;

erreur scientifique;

doivent recevoir plus de tests.

La couverture uniforme n’est pas toujours optimale.

---

## Le chemin critique scientifique

Une chaîne qui produit une conclusion scientifique mérite une provenance plus forte qu’une animation secondaire.

Nous pouvons classer les chemins par importance.

---

## Data lineage

Pour chaque résultat scientifique :

quelles entrées ?

quelles transformations ?

quelles versions ?

quels filtres ?

quelles corrections ?

La data lineage est la généalogie de la donnée.

Elle doit traverser toute la composition.

---

## Un résultat sans lignée est orphelin

Il peut être beau.

Précis.

Plausible.

Mais nous ne savons pas comment il est né.

Alors la composition doit préserver la lignée.

---

## La lignée comme hash chain

Conceptuellement, chaque étape peut inclure un hash de l’entrée et de la sortie.

Cela peut aider à vérifier l’intégrité du pipeline.

Mais la chaîne de hashes ne prouve pas la validité scientifique.

Elle protège la continuité du contenu.

---

## Recalcul

Si une transformation change, nous devons savoir quels résultats dérivés recalculer.

Le graphe de dépendance permet de trouver les descendants.

---

## Build graph

Cette idée ressemble à un système de build.

Une source change.

Les artefacts dépendants deviennent stale.

Puis ils sont reconstruits.

Brutus peut utiliser cette logique pour les données et calculs.

---

## Reproductible build

Un build reproductible vise à produire le même artefact à partir des mêmes sources et environnement.

Cette propriété serait extrêmement utile pour les paquets Brutus.

---

## Brutus Package Export V1

Le chapitre 10 proposait :

**BRUTUS_PACKAGE_EXPORT_V1.**

Nous pouvons maintenant lui donner une forme.

### MANIFEST

identité, version, parent.

### MODULES

liste et versions.

### LINKS

topologie.

### CONFIG

paramètres.

### TESTS

unitaires, intégration, stabilité.

### PROVENANCE

source, commits, hashes.

### ARTIFACTS

fichiers produits.

### IMPORT CONTRACT

comment reconstruire.

---

## Import

Importer un paquet ne doit pas signifier exécuter immédiatement.

Le cycle sûr :

\[
IMPORT
\rightarrow
VERIFY
\rightarrow
INSPECT
\rightarrow
DRY\_RUN
\rightarrow
GO
\rightarrow
ACTIVATE
\]

Cela protège contre un paquet invalide ou incompatible.

---

## Signature

Un artefact peut être signé cryptographiquement pour prouver une origine contrôlée, selon l’infrastructure utilisée.

Mais signature ne signifie pas vérité.

Elle répond :

qui a signé ce contenu ?

Pas :

ce contenu est-il scientifiquement correct ?

---

## Provenance complète

La confiance vient d’un ensemble :

source;

hash;

signature;

tests;

reproduction;

documentation.

Aucune pièce ne suffit seule.

---

## Public Fork V1

Le chapitre 10 proposait aussi :

**PUBLIC_FORK_V1.**

Une composition versionnée rend le fork naturel.

Nous pouvons copier une plaque.

Conserver :

parent;

version;

hash du parent;

modifications.

Puis expérimenter.

---

## Conserver l’original, libérer le fork

Cette règle devient architecturale.

Le canon reste intact.

Le fork explore.

Si le fork devient meilleur, il peut être proposé.

La provenance montre l’histoire.

---

## Merge

Réintégrer un fork demande :

diff;

tests;

compatibilité;

review;

GO;

merge;

verification.

L’histoire n’est pas écrasée.

---

## Le système complet

À ce stade, nous pouvons écrire une abstraction générale :

\[
\mathcal{S}
=
(G,C,T,M,E,V)
\]

où :

- \(G\) = graphe de modules et liens;
- \(C\) = configuration;
- \(T\) = modèle temporel;
- \(M\) = mémoire et provenance;
- \(E\) = modèle d’erreur et réparation;
- \(V\) = vérification.

Ce n’est pas une loi universelle.

C’est un candidat de représentation pour Brutus.

---

## Entrée du système

\[
I_{\mathcal{S}}
\]

doit être définie.

Elle peut être :

signal;

commande;

fichier;

mesure;

événement.

Le système ne doit pas avoir d’entrée invisible.

---

## Sortie du système

\[
O_{\mathcal{S}}
\]

doit porter :

valeur;

statut;

temps;

provenance;

version;

qualité si nécessaire.

Une sortie nue perd trop d’information.

---

## État global

\[
S_{\mathcal{S}}
\]

peut être une projection des états locaux.

Il n’est pas toujours nécessaire de stocker tous les détails dans un seul objet.

Mais il faut pouvoir reconstruire une vue cohérente.

---

## La Reine comme composant de coordination

Dans cette architecture, la Reine peut être définie sobrement comme un rôle de coordination.

Pas une intelligence cachée.

Elle peut fournir :

tick;

barrière;

état de session;

autorité de cycle.

Son contrat doit rester minimal.

---

## Une seule responsabilité par module

Plus un module possède de responsabilités, plus il devient difficile à tester.

Nous pouvons préférer :

un scheduler;

un logger;

un calculateur;

un routeur;

un analyseur;

plutôt qu’un seul module qui fait tout.

---

## Single Responsibility

Cette idée ne doit pas devenir un dogme.

Parfois regrouper réduit la complexité.

Mais chaque regroupement doit avoir une raison.

Le bon niveau est celui qui rend le système compréhensible et testable.

---

## Couplage

Un module fortement couplé connaît beaucoup de détails d’un autre.

Cela rend les modifications difficiles.

Nous voulons généralement réduire le couplage inutile.

---

## Cohésion

Un module cohésif regroupe des responsabilités qui appartiennent réellement ensemble.

Une bonne architecture cherche souvent :

forte cohésion interne;

couplage externe maîtrisé.

---

## Mesurer le couplage

Nous pouvons compter :

dépendances;

ports;

appels;

état partagé.

Mais aucune métrique unique ne définit une bonne architecture.

Elle peut seulement signaler des zones à examiner.

---

## Composition et simplicité

Un système modulaire peut devenir plus complexe qu’un monolithe si les frontières sont artificielles.

Découper n’est pas automatiquement simplifier.

Chaque frontière ajoute :

contrat;

latence;

erreur;

version;

observabilité.

Nous devons justifier les modules.

---

## Le plus petit nombre de pièces compréhensibles

Voilà peut-être la bonne cible.

Pas le maximum de modules.

Pas le minimum absolu.

Le plus petit ensemble de responsabilités clairement séparées qui rendent le système vérifiable.

---

## Architecture avant décoration

Nous devons résister à l’envie d’ajouter immédiatement :

72 modules;

13 anneaux;

7 niveaux;

cristaux;

lumières;

si les relations fonctionnelles ne sont pas définies.

Les symboles pourront venir.

Le système doit d’abord exister.

---

## 72 comme architecture candidate

Si nous voulons réellement 72 modules, nous devons demander :

pourquoi 72 ?

quelles responsabilités ?

quelle topologie ?

quelle charge ?

quels tests ?

Si 72 vient d’une structure symbolique, c’est acceptable comme contrainte artistique.

Si nous prétendons qu’il est optimal techniquement, il faut le démontrer.

---

## Trois modules d’abord

B1.

B2.

B3.

C’est suffisant pour apprendre :

enchaînement;

état;

latence;

erreur;

composition.

Puis quatre chemins.

Puis plaques.

Puis croissance.

---

## Petite preuve avant grand système

Une plaque B1→B2 avec tests complets vaut davantage qu’un diagramme de 72 modules non exécutés.

La progression doit rester :

\[
small
\rightarrow
verified
\rightarrow
composed
\rightarrow
scaled
\]

---

## Scaling

Lorsque la petite architecture est correcte, nous pouvons augmenter :

nombre de modules;

débit;

durée;

utilisateurs;

nœuds.

Chaque axe mérite un test séparé.

---

## Scale up vs scale out

Augmenter la puissance d’une machine.

Ou distribuer sur plusieurs machines.

Ces stratégies créent des problèmes différents.

Brutus n’a pas besoin de choisir tant que les besoins ne l’exigent pas.

---

## Le serveur comme autorité

Si le système utilise un serveur central pour l’état canonique, cette autorité doit être explicite.

Les clients reçoivent.

Proposent.

Affichent.

Le serveur décide selon le contrat.

---

## Server authority

Une architecture candidate :

\[
CLIENT
\rightarrow
COMMAND
\rightarrow
SERVER
\rightarrow
STATE
\rightarrow
EVENT
\rightarrow
CLIENT
\]

Le client ne déclare pas lui-même le nouvel état comme canonique.

Il attend la confirmation.

---

## Optimistic UI

Une interface peut afficher une prédiction avant confirmation.

Mais le statut doit être :

PREDICTED.

Puis :

CONFIRMED.

Ou :

REJECTED.

La composition des couches doit préserver cette distinction.

---

## Shared Queen

Si plusieurs clients regardent la même Reine ou même état central, ils doivent voir une version cohérente selon le modèle choisi.

Le système doit définir :

qui écrit;

qui lit;

comment synchroniser;

comment résoudre une reconnexion.

---

## Reconnect

Un client qui revient après interruption doit pouvoir demander :

état courant;

version;

événements manqués si nécessaire.

Il ne doit pas reprendre en supposant que son ancien état est encore vrai.

---

## Snapshot + delta

Une stratégie :

snapshot récent;

puis événements depuis ce snapshot.

Cela réduit la quantité de replay.

Le chapitre 14 revient dans la composition.

---

## Composition de la mémoire

Chaque sous-système peut avoir son journal.

Mais le système global a besoin d’une corrélation commune.

Le trace ID relie les histoires locales.

---

## Horloge et composition

Chaque événement doit avoir un repère temporel.

Mais dans un système distribué, le tick logique peut être plus utile qu’un timestamp absolu pour certaines relations.

Nous devons conserver les deux si nécessaire.

---

## Une seule chronologie parfaite n’est pas toujours disponible

Il faut accepter cette limite.

L’ordre causal peut être plus important qu’une heure identique à la microseconde.

L’architecture doit dire ce qu’elle garantit.

---

## Composition et preuve

À la fin, une composition doit pouvoir répondre :

quels modules ?

quelles versions ?

quels liens ?

quelle config ?

quel tick ?

quelle entrée ?

quelle sortie ?

quelles erreurs ?

quels tests ?

quel HEAD ?

Si elle répond, le système possède une mémoire exploitable.

---

## Le test minimal de composition

Nous pouvons construire :

\[
INPUT
\rightarrow
B1
\rightarrow
B2
\rightarrow
OUTPUT
\]

B1 :

\[
y=2x
\]

B2 :

\[
z=y+1
\]

Donc :

\[
z=2x+1
\]

Tester :

types;

valeurs;

ticks;

trace;

erreur;

replay.

C’est une petite preuve complète.

---

## Ajouter B3

Puis :

\[
B3:z\mapsto z^2
\]

La composition devient :

\[
w=(2x+1)^2
\]

Nous pouvons comparer la sortie du pipeline à la formule composée.

Le système teste alors sa propre composition.

---

## Ajouter quatre chemins

Diverger après B1.

Chaque chemin applique une transformation différente.

Puis J réunit.

Nous obtenons un vrai banc d’intégration.

---

## Test analytique

Lorsque les fonctions sont simples, nous pouvons calculer la sortie attendue à la main.

C’est précieux.

Le runtime doit retrouver exactement ou numériquement cette sortie.

---

## Test de perturbation

Retarder P3.

Supprimer un message.

Corrompre une entrée de test.

Vérifier la politique.

La composition entre dans le protocole de stabilité.

---

## Test de fréquence

Faire passer un sinus connu dans une plaque de filtres.

Comparer la réponse mesurée à la réponse attendue.

La composition entre dans le langage du chapitre 17.

---

## Test de restart

Arrêter une plaque stateful.

Restaurer checkpoint.

Rejouer.

Comparer.

La composition rejoint la mémoire et la réparation.

---

## Une architecture unifiée commence à apparaître

Ce n’est plus une collection de chapitres séparés.

Les règles commencent à se croiser.

Connexion.

Temps.

Mémoire.

Réparation.

Stabilité.

Fréquence.

Composition.

Chaque couche vérifie les autres.

---

## Le prochain défi

Lorsque nous avons un système composé, une nouvelle question devient incontournable.

Comment savons-nous que quelqu’un d’autre peut observer la même chose ?

Comment montrer les preuves ?

Comment permettre une reproduction indépendante ?

Comment distinguer démonstration, mesure et interprétation ?

Le prochain chapitre devra traiter l’observation scientifique et la reproductibilité.

---

## Composition n’est pas preuve publique

Un système peut être parfaitement conçu en privé.

Tant que ses résultats ne sont pas exportables et vérifiables, le lecteur extérieur doit nous croire.

Le projet veut mieux que cela.

Il veut permettre de vérifier.

---

## Rapport de reproduction

Le chapitre 10 proposait :

**REPRODUCTION_REPORT_V1.**

Nous sommes maintenant presque prêts à le construire.

Il devra relier :

artefact;

version;

protocole;

environnement;

résultat;

écarts.

Le prochain chapitre pourra lui donner sa vraie forme.

---

## Le visiteur

Un visiteur ne doit pas avoir besoin de connaître tout le code pour voir :

ce qui a été exécuté;

ce qui a été mesuré;

ce qui est candidat;

ce qui a échoué;

comment reproduire.

La transparence doit avoir plusieurs niveaux.

---

## Le chercheur

Le chercheur doit pouvoir aller plus loin.

Télécharger ou retrouver l’artefact.

Lire le protocole.

Relancer.

Comparer.

Critiquer.

Une preuve qui accepte la critique est plus forte qu’une preuve qui exige la confiance.

---

## Dernière image

Sur la table, les pièces sont enfin prêtes.

B1.

B2.

B3.

La Reine.

Les quatre chemins.

Le registre.

Le réparateur.

Le protocole de stabilité.

L’analyse fréquentielle.

Une à une, nous les avons sorties de la métaphore.

Puis nous les relions.

Pas avec des fils invisibles.

Avec des contrats.

Pas avec des suppositions.

Avec des tests.

Pas avec un seul grand cerveau.

Avec des responsabilités.

Le premier signal entre.

B1 travaille.

B2 reçoit.

Les chemins se séparent.

Le temps les marque.

La mémoire les suit.

La jonction rassemble.

La sortie apparaît.

Et, pour la première fois, nous pouvons regarder tout le trajet et répondre :

**voilà exactement comment elle est arrivée ici.**

Le système existe maintenant comme composition.

La prochaine étape ne sera pas de lui ajouter des pièces.

Elle sera de laisser quelqu’un d’autre vérifier que nous ne nous racontons pas une histoire.

# **LE SYSTÈME EST COMPOSÉ. LA PREUVE DOIT MAINTENANT SORTIR DU SYSTÈME.**
