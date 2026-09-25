# Chapitre 12 — Aucune connexion invisible

**APRÈS L’INTRODUCTION — DEUXIÈME CHAPITRE DU DÉVELOPPEMENT**  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Un système devient compréhensible le jour où chaque influence possède un chemin visible.**

---

## Après le miroir, le mécanisme

Le chapitre 11 s’est terminé sur une phrase :

**Le mécanisme peut commencer.**

Alors il faut maintenant accepter une conséquence immédiate.

Un mécanisme n’est pas une collection de belles pièces.

Ce n’est pas un dessin rempli de conduits.

Ce n’est pas une interface lumineuse.

Ce n’est même pas un ensemble de modules qui fonctionnent séparément.

Un mécanisme commence lorsqu’on peut répondre à une question simple :

**qui influence quoi, comment, quand, et avec quelle trace ?**

Si B1 modifie B2, cette relation doit exister quelque part.

Si une valeur traverse trois modules avant de produire une sortie, le trajet doit pouvoir être retrouvé.

Si un état ancien modifie un calcul présent, cet état doit être identifié.

Si une erreur change le comportement du système, elle doit apparaître.

Si le temps intervient, il doit avoir un port.

Si rien de cela n’est visible, nous n’avons pas encore une architecture.

Nous avons une boîte noire.

Et Brutus ne doit pas devenir une boîte noire.

---

## La première loi d’architecture

Nous pouvons maintenant écrire une règle qui devra survivre aux futurs modules :

> **AUCUNE CONNEXION INVISIBLE.**

Cette phrase est volontairement absolue dans le cadre architectural.

Elle ne signifie pas que tout doit être affiché en permanence à l’écran.

Elle signifie que toute relation active doit être **définie, inspectable et traçable**.

Un lien peut être caché visuellement pour alléger une interface.

Mais il ne doit jamais être caché conceptuellement.

Il doit posséder une identité.

Une origine.

Une destination.

Un type.

Et idéalement une raison.

---

## Une ligne n’est pas encore une connexion

Dans un schéma, il est facile de dessiner une ligne entre deux blocs.

Cela donne immédiatement l’impression que les deux blocs communiquent.

Mais une ligne graphique ne répond pas aux questions essentielles.

Que transporte-t-elle ?

Un nombre ?

Un vecteur ?

Une structure ?

Une commande ?

Un événement ?

Un état ?

Une erreur ?

Une fréquence ?

Une phase ?

À quelle cadence ?

Dans quelle unité ?

Avec quelle précision ?

Est-elle obligatoire ?

Peut-elle être absente ?

Que se passe-t-il si elle est invalide ?

Une connexion réelle commence quand ces questions ont une réponse.

---

## Les ports avant les fonctions

Avant de décider ce qu’un module accomplit, nous pouvons décider ce qu’il a le droit de recevoir et de transmettre.

C’est une discipline extrêmement utile.

Chaque module peut commencer par cinq familles de ports :

[
	ext{INPUT}
]

[
	ext{OUTPUT}
]

[
	ext{STATE}
]

[
	ext{ERROR}
]

[
	ext{TIME}
]

Ces cinq mots ne prétendent pas décrire toutes les architectures possibles.

Ils constituent un vocabulaire minimal de travail.

Ils imposent surtout une habitude :

**séparer les rôles.**

---

## INPUT

Le port **INPUT** reçoit ce qui vient de l’extérieur du module.

Il ne faut pas écrire seulement une valeur nue.

Il faut savoir de quelle valeur il s’agit.

Une entrée robuste devrait pouvoir être décrite au minimum par :

[
I = (v,	au,u,s,p)
]

où, par convention de travail :

- (v) = valeur;
- (	au) = temps ou tick associé;
- (u) = unité ou type;
- (s) = source;
- (p) = provenance ou identifiant de trace.

Ce tuple n’est pas une loi universelle.

C’est un **CANDIDAT d’interface**.

Son intérêt est pratique : une valeur cesse d’arriver seule.

Elle arrive avec assez de contexte pour être interprétée.

---

## OUTPUT

Le port **OUTPUT** ne représente pas simplement « ce que le module donne ».

Il représente ce que le module accepte de déclarer comme résultat de son traitement.

Nous pouvons lui donner une structure analogue :

[
O = (y,	au,u,m,p)
]

où :

- (y) = résultat;
- (	au) = temps ou tick de production;
- (u) = unité ou type;
- (m) = module producteur;
- (p) = provenance.

Ainsi, si une valeur finale paraît étrange, nous pouvons remonter vers son producteur.

Le système commence à raconter sa propre histoire.

---

## STATE

Le port **STATE** est différent.

Il ne représente pas simplement ce qui entre ou sort.

Il représente ce qui **persiste**.

Un module sans état peut être purement fonctionnel :

[
y = f(x)
]

Un module avec état peut dépendre de son histoire :

[
(y_{n+1},S_{n+1}) = f(x_n,S_n)
]

Ici :

- (x_n) est l’entrée actuelle;
- (S_n) est l’état actuel;
- (y_{n+1}) est la sortie;
- (S_{n+1}) est le nouvel état.

Cette différence est immense.

Deux modules peuvent recevoir exactement la même entrée et produire des sorties différentes simplement parce que leur état précédent n’est pas le même.

Si cet état reste invisible, le système peut sembler incohérent alors qu’il suit parfaitement sa logique interne.

C’est pourquoi l’état doit laisser une trace.

---

## ERROR

Une erreur n’est pas seulement un message rouge.

C’est une sortie technique.

Elle possède une cause.

Un contexte.

Un moment.

Une gravité.

Une conséquence.

Nous pouvons écrire un événement d’erreur sous une forme minimale :

[
E = (c,	au,m,x,a)
]

où :

- (c) = code ou catégorie;
- (	au) = tick;
- (m) = module;
- (x) = contexte pertinent;
- (a) = action prise.

Par exemple, deux erreurs identiques n’ont pas nécessairement le même effet.

L’une peut produire **RETRY**.

Une autre **HOLD**.

Une autre **RESET**.

Une autre **STOP**.

Si l’action n’est pas tracée, l’erreur reste incomplète.

---

## TIME

Le port **TIME** paraît banal jusqu’au jour où deux modules ne travaillent plus au même rythme.

À ce moment, tout change.

Une valeur peut être correcte mais trop vieille.

Deux sorties peuvent être exactes séparément mais incohérentes lorsqu’elles sont combinées parce qu’elles ne correspondent pas au même instant.

Un état peut être valable à (t_n) et faux à (t_{n+1}).

Alors le temps doit devenir une donnée architecturale.

Nous pouvons distinguer au moins :

[
t_{	ext{source}}
]

[
t_{	ext{receive}}
]

[
t_{	ext{process}}
]

[
t_{	ext{emit}}
]

Cette distinction permet de mesurer la latence au lieu de la deviner.

---

## Le module minimal

Avec ces éléments, un module minimal peut être représenté comme :

[
M:
(I,S,E,T)
longrightarrow
(O,S',E',T')
]

Cette écriture ne signifie pas que chaque module doit modifier chaque composante.

Elle montre seulement les catégories qui peuvent participer à son comportement.

Nous pouvons alors poser une première définition opérationnelle :

> **Un module Brutus est une unité identifiable qui reçoit des données par des ports définis, applique une transformation déclarée, conserve ou non un état, produit une sortie et laisse une trace de son comportement.**

Ce n’est pas encore une norme finale.

C’est une base de construction.

---

## B1 n’est pas B2

Un piège apparaît rapidement lorsqu’on clone des modules.

Ils peuvent avoir la même forme.

Le même code.

Les mêmes ports.

Et pourtant être deux objets différents.

Alors chaque instance doit posséder une identité.

Par exemple :

[
M_i = (	ext{type},	ext{id},	ext{version})
]

Un module peut donc être décrit comme ADD / B1 / v1 et un autre comme ADD / B2 / v1.

Même transformation.

Identité distincte.

Cette séparation devient essentielle pour les logs, les états et les erreurs.

---

## Une relation doit elle aussi avoir une identité

Si B1 communique avec B2, la relation ne devrait pas exister seulement comme une flèche.

Nous pouvons lui donner une forme :

[
L_{1ightarrow2}
=
(	ext{source},	ext{port}_s,	ext{destination},	ext{port}_d,	ext{type},	ext{règle})
]

Par exemple :

[
L_{B1ightarrow B2}
=
(B1,	ext{OUTPUT},B2,	ext{INPUT},mathbb{R},	ext{direct})
]

Cette notation signifie :

la sortie numérique réelle de B1 alimente directement l’entrée de B2.

Si demain la connexion change, le changement est visible.

---

## Le lien devient un objet

Cette idée est fondamentale.

Dans beaucoup de systèmes, les modules sont traités comme des objets importants et les connexions comme de simples détails.

Nous faisons l’inverse.

La connexion est elle aussi un objet.

Parce qu’une architecture ne réside pas uniquement dans ses pièces.

Elle réside dans les relations entre ses pièces.

Deux collections contenant exactement les mêmes modules peuvent produire des systèmes radicalement différents si leurs liens sont différents.

L’architecture est donc au moins :

[
A = (M,L)
]

où :

- (M) est l’ensemble des modules;
- (L) est l’ensemble des liens.

---

## Le graphe apparaît

À partir de cette définition, nous retrouvons naturellement la théorie des graphes.

Un système peut être représenté par :

[
G=(V,E)
]

où :

- (V) représente les nœuds;
- (E) représente les arêtes.

Dans notre langage :

[
V leftrightarrow M
]

[
E leftrightarrow L
]

Cette correspondance est utile.

Elle permet d’emprunter des outils mathématiques déjà existants au lieu de réinventer tout le vocabulaire.

Chemins.

Cycles.

Connexité.

Degré.

Dépendances.

Composantes.

Graphes dirigés.

Poids.

Toutes ces notions peuvent devenir des instruments d’analyse de l’architecture Brutus.

---

## Le sens de la flèche compte

Si B1 envoie vers B2, cela ne signifie pas que B2 envoie vers B1.

Alors notre graphe est généralement **dirigé**.

Nous pouvons écrire :

[
B1 ightarrow B2
]

sans supposer :

[
B2 ightarrow B1
]

Cette distinction devient encore plus importante lorsqu’un retour existe.

Par exemple :

[
B1 ightarrow B2 ightarrow B3 ightarrow B1
]

Nous avons maintenant un cycle.

Et un cycle introduit potentiellement de la mémoire, de la rétroaction, de l’oscillation ou de l’instabilité.

Une petite flèche supplémentaire peut donc changer complètement la nature du système.

Voilà pourquoi aucune connexion ne doit être invisible.

---

## Une influence indirecte reste une influence

Supposons :

[
B1 ightarrow B2
]

et :

[
B2 ightarrow B3
]

Alors B1 peut influencer B3 sans connexion directe.

Cette influence est indirecte mais traçable.

Le chemin est :

[
P = (B1,B2,B3)
]

Si un comportement étrange apparaît dans B3, le système doit permettre d’explorer ce chemin en amont.

La traçabilité ne doit donc pas s’arrêter au voisin immédiat.

---

## Les quatre chemins

À mesure que le système grandit, une seule route devient insuffisante.

Une architecture peut avoir plusieurs chemins entre une entrée et une sortie.

Nous pouvons écrire, de manière abstraite :

[
P_1,;P_2,;P_3,;P_4
]

Chaque chemin est une suite ordonnée de modules et de liens :

[
P_k=(M_0,L_1,M_1,ldots,L_n,M_n)
]

À ce stade, **les quatre chemins sont une structure architecturale**, pas une affirmation physique.

Ils peuvent servir à représenter quatre traitements distincts, quatre branches de mesure, quatre transformations ou quatre routes de calcul.

Leur signification exacte doit être attachée à leur définition.

Le nombre quatre ne possède aucun pouvoir explicatif à lui seul.

Ce sont les transformations portées par les chemins qui comptent.

---

## Pourquoi plusieurs chemins ?

Plusieurs chemins peuvent être utiles pour différentes raisons.

Un chemin peut produire la valeur principale.

Un autre peut calculer une référence.

Un troisième peut vérifier une contrainte.

Un quatrième peut conserver un signal de comparaison ou d’erreur.

Mais cette interprétation n’est qu’un exemple.

Le principe plus général est :

> **Deux chemins ne doivent pas être considérés différents seulement parce qu’ils sont dessinés séparément. Ils doivent effectuer des opérations définies différemment.**

Sinon nous avons quatre dessins d’un même calcul.

Pas quatre chemins fonctionnels.

---

## Le fan-out

Une entrée peut être copiée vers plusieurs chemins.

Nous appelons cela une divergence ou un fan-out.

[
x
longrightarrow
egin{cases}
P_1(x)\
P_2(x)\
P_3(x)\
P_4(x)
end{cases}
]

Une question apparaît immédiatement :

chaque chemin reçoit-il exactement la même valeur ?

Au même tick ?

Avec la même unité ?

Avec la même précision ?

Si la réponse est oui, il faut pouvoir le prouver par la trace.

Sinon les résultats des chemins ne sont pas directement comparables.

---

## Copier n’est pas partager

Cette distinction est subtile.

Si quatre chemins lisent le même objet mutable, une modification dans un chemin peut contaminer les autres.

Si chacun reçoit une copie immuable de l’entrée, ils restent indépendants.

Ce choix architectural doit être explicite.

Nous pouvons distinguer deux modes :

**COPY**

et :

**SHARED REFERENCE**

Ce simple détail peut décider si un résultat est reproductible.

---

## Le fan-in

À l’autre extrémité, plusieurs chemins peuvent se rejoindre.

[
P_1,P_2,P_3,P_4
longrightarrow
J
]

où (J) représente une jonction.

Mais une jonction n’est pas automatiquement une addition.

Elle peut :

additionner;

moyenner;

sélectionner;

comparer;

voter;

concaténer;

normaliser;

attendre une synchronisation;

rejeter une branche invalide.

Alors la jonction doit posséder une fonction définie :

[
y = J(y_1,y_2,y_3,y_4)
]

Sans cette définition, quatre chemins qui se rejoignent ne forment qu’un dessin.

---

## Attendre tout le monde

Supposons que (P_1) produise son résultat avant (P_4).

La jonction doit décider quoi faire.

Attendre ?

Utiliser la dernière valeur connue ?

Abandonner le cycle ?

Marquer la donnée comme partielle ?

La synchronisation devient donc une règle explicite.

Par exemple :

[
	ext{READY}(n)
=
igwedge_{k=1}^{4}
left(	au_k=night)
]

Cette règle candidate signifie :

la jonction du tick (n) ne s’ouvre que lorsque les quatre résultats associés à ce tick sont présents.

C’est une barrière de synchronisation.

Elle n’est pas toujours nécessaire.

Mais si elle existe, elle doit être visible.

---

## Le temps rejoint l’architecture

Nous découvrons ici pourquoi le port TIME était nécessaire.

Sans lui, deux résultats peuvent porter la même forme et pourtant appartenir à deux instants différents.

Alors le système doit savoir si :

[
y_1(n)
]

et :

[
y_2(n)
]

correspondent au même cycle.

Le prochain chapitre approfondira cette question.

Pour l’instant, il suffit d’établir ceci :

> **Toute architecture multi-chemins possède un problème potentiel de synchronisation.**

---

## Le chemin d’erreur

Une erreur n’a pas besoin de voyager dans le même conduit que les données.

Nous pouvons définir un chemin séparé :

[
P_E
]

Il peut transporter :

codes;

exceptions;

timeouts;

valeurs hors domaine;

ruptures de synchronisation;

erreurs d’unité;

erreurs de type.

Cela permet de ne pas confondre :

**la donnée vaut zéro**

avec :

**aucune donnée valide n’a été produite.**

Cette différence est vitale.

---

## Zéro n’est pas l’absence

Un système mal conçu peut encoder plusieurs états avec la même valeur.

Zéro peut vouloir dire :

résultat réellement nul;

pas encore calculé;

capteur absent;

erreur;

reset;

valeur inconnue.

C’est dangereux.

Il faut séparer la valeur de son statut.

Nous pouvons écrire :

[
D=(v,q)
]

où (q) indique la qualité ou le statut.

Par exemple :

[
q in
{
VALID,
MISSING,
ERROR,
STALE,
UNKNOWN
}
]

Ainsi :

[
(0,VALID)

eq
(0,MISSING)
]

Cette distinction seule peut éviter des heures de fausse analyse.

---

## Le chemin de contrôle

Un module peut recevoir autre chose qu’une donnée.

Il peut recevoir une instruction.

**START.**

**STOP.**

**RESET.**

**HOLD.**

**COMMIT.**

**GO.**

Ces commandes ne devraient pas être mélangées silencieusement aux valeurs scientifiques.

Nous pouvons donc distinguer un canal de contrôle :

[
P_C
]

Cette séparation protège l’analyse.

Une donnée décrit quelque chose.

Une commande demande une action.

Confondre les deux rend le système difficile à raisonner.

---

## Le GO comme événement technique

Dans l’Introduction, GO était un mot.

Dans une architecture, GO peut devenir un événement formel.

[
GO(	au,p,a)
]

où :

- (	au) = moment;
- (p) = provenance de l’autorisation;
- (a) = action autorisée.

Le système peut alors prouver qu’une opération sensible n’a pas été exécutée avant son autorisation.

Le mot devient une barrière de sécurité.

---

## Les connexions interdites

Une architecture solide ne définit pas seulement ce qui peut se connecter.

Elle définit aussi ce qui **ne peut pas** se connecter.

Par exemple :

une sortie ERROR ne doit pas alimenter directement une entrée numérique sans convertisseur explicite.

Une fréquence en hertz ne doit pas être envoyée dans un port qui attend une durée en secondes simplement parce que les deux sont des nombres.

Une structure STATE ne doit pas devenir INPUT par accident.

Nous pouvons représenter les compatibilités par une relation :

[
C(T_s,T_d)
in
{0,1}
]

où (T_s) est le type source et (T_d) le type destination.

Une connexion n’est autorisée que si :

[
C(T_s,T_d)=1
]

---

## Le type n’est pas une décoration

Le typage protège contre une erreur très courante :

des valeurs numériquement plausibles mais sémantiquement incompatibles.

Par exemple :

[
5;	ext{s}
]

et :

[
5;	ext{Hz}
]

contiennent le même nombre.

Ils ne représentent pas la même grandeur.

Un système qui transporte seulement 5 perd une information essentielle.

Alors la donnée doit voyager avec son type ou son unité.

---

## Les unités comme garde-fou

La cohérence dimensionnelle est un filtre extrêmement puissant.

Si une équation additionne deux grandeurs, leurs dimensions doivent être compatibles.

Par exemple :

[
3;	ext{m} + 4;	ext{s}
]

n’est pas une addition physique valide.

Un module qui reçoit des grandeurs physiques devrait donc pouvoir vérifier les dimensions avant le calcul.

Cela ne prouve pas qu’une équation est vraie.

Mais cela élimine une classe entière d’erreurs.

---

## L’adaptateur explicite

Parfois deux ports incompatibles peuvent être reliés après transformation.

Alors il faut insérer un module d’adaptation.

[
B1
ightarrow
A
ightarrow
B2
]

où (A) effectue la conversion.

Par exemple :

[
f = rac{1}{T}
]

peut convertir une période (T) en fréquence (f), si les conditions sont correctement définies.

Le convertisseur devient visible.

Personne ne peut croire que la période était déjà une fréquence.

---

## Une connexion peut avoir un contrat

Nous pouvons aller plus loin.

Chaque lien peut posséder un contrat :

[
K_L=
(	ext{type},	ext{unité},	ext{domaine},	ext{latence},	ext{qualité})
]

Exemple :

- type : float64;
- unité : Hz;
- domaine : (fge0);
- latence maximale : 20 ms;
- statut requis : VALID.

La connexion devient alors testable.

Elle peut réussir ou échouer.

---

## Le module ne doit pas deviner

Supposons qu’un module attend une fréquence.

Il reçoit 240.1.

Sans unité, il pourrait deviner qu’il s’agit de hertz.

Mais cette devinette ne doit pas entrer dans le noyau technique.

La bonne réponse est :

**type ou unité manquante.**

Le système peut afficher une suggestion à l’utilisateur.

Mais le cœur ne doit pas transformer une supposition en fait.

---

## L’architecture et l’intuition

Cette exigence peut sembler froide comparée à la manière dont certaines idées apparaissent.

Dans l’esprit, une relation peut être évidente avant d’être nommée.

C’est normal.

Le rôle de l’architecture n’est pas d’empêcher cette intuition.

Il est de lui demander une traduction lorsqu’elle devient exécutable.

Avant le code :

**je vois un lien.**

Dans le code :

**voici le lien.**

Cette traduction est le passage de la vision vers le mécanisme.

---

## Le dessin doit suivre le système

Une erreur fréquente consiste à fabriquer d’abord un beau schéma, puis à forcer le programme à ressembler au dessin.

Nous voulons le contraire.

Le schéma doit être une projection de l’état réel de l’architecture.

Si B1 n’est pas connecté à B2 dans le modèle, l’interface ne doit pas dessiner une connexion active.

Si le lien tombe, la visualisation doit pouvoir le montrer.

Si le type change, l’inspecteur doit le révéler.

Ainsi, la beauté devient une lecture.

Pas un masque.

---

## La coquille ne pense pas

Cette règle mérite d’être répétée.

La coquille visuelle affiche.

Elle ne doit pas inventer une logique que le système n’a pas.

Un cadran peut montrer une fréquence.

Mais il ne doit pas la fabriquer.

Une lumière peut montrer un état READY.

Mais elle ne doit pas décider que le module est READY.

Une animation peut montrer un flux.

Mais elle ne doit pas simuler un flux absent simplement pour rendre l’écran vivant.

La source d’autorité doit rester identifiable.

---

## Source d’autorité

Pour toute valeur affichée, nous devrions pouvoir répondre :

**qui est autorisé à dire que cette valeur est vraie dans le système ?**

Cela peut être :

un capteur;

un calculateur;

un serveur;

un module d’état;

un test;

une donnée enregistrée.

Cette source doit être nommée.

Sinon l’interface risque de devenir une seconde réalité indépendante du moteur.

---

## La provenance jusqu’au pixel

Dans l’idéal, une valeur affichée peut être retracée jusqu’à sa source.

Le chemin peut être :

[
	ext{pixel}
leftarrow
	ext{widget}
leftarrow
	ext{state UI}
leftarrow
	ext{message}
leftarrow
	ext{output module}
leftarrow
	ext{inputs}
]

Nous n’avons pas besoin d’afficher cette chaîne en permanence.

Mais elle doit pouvoir être obtenue.

C’est une propriété extrêmement forte pour un laboratoire.

---

## Le registre de continuité revient

Le chapitre précédent a proposé :

[
	ext{QUI}
ightarrow
	ext{ÉTAT}
ightarrow
	ext{TICK}
ightarrow
	ext{AVANT}
ightarrow
	ext{ACTION}
ightarrow
	ext{APRÈS}
]

Nous pouvons maintenant l’attacher aux connexions.

Pour chaque événement :

[
R_n=
(m,	au,S_{	ext{before}},I,A,S_{	ext{after}},O,E)
]

où :

- (m) = module;
- (	au) = tick;
- (S_{	ext{before}}) = état avant;
- (I) = entrée;
- (A) = action;
- (S_{	ext{after}}) = état après;
- (O) = sortie;
- (E) = erreur éventuelle.

Cette structure peut devenir la base d’un journal reproductible.

---

## Rejouer un événement

Si les entrées, les versions et les états sont conservés, nous pouvons tenter un **replay**.

Autrement dit :

reprendre le même état;

injecter la même entrée;

utiliser la même version;

et vérifier si la même sortie réapparaît.

Pour un système déterministe :

[
(M_v,S_n,I_n)
Rightarrow
(O_n,S_{n+1})
]

devrait produire le même résultat à chaque répétition, dans les mêmes conditions.

Si ce n’est pas le cas, une variable architecturale non déclarée existe peut-être.

Et une dépendance non déclarée est exactement ce que notre règle cherche à éliminer.

---

## Les dépendances cachées

Une dépendance peut être :

l’heure système;

un seed aléatoire;

un fichier externe;

un état global;

un cache;

l’ordre d’exécution;

une variable d’environnement.

Ces éléments peuvent rendre un calcul impossible à reproduire.

Alors ils doivent être remontés dans l’architecture.

---

## Déterministe ne signifie pas simple

Un système peut être extrêmement complexe et rester déterministe.

À l’inverse, un système très simple peut être non déterministe s’il utilise une source aléatoire non contrôlée.

Le statut doit être déclaré.

Par exemple :

**DETERMINISTIC**

ou :

**STOCHASTIC avec seed déclaré**

ou :

**EXTERNAL DEPENDENCY**

Le but n’est pas de préférer systématiquement l’un.

Le but est de savoir lequel nous exécutons.

---

## Un chemin peut être désactivé

Dans une architecture à plusieurs chemins, toutes les branches ne sont pas forcément actives en permanence.

Alors il faut distinguer :

[
ACTIVE
]

[
INACTIVE
]

[
BYPASSED
]

[
FAULT
]

Si une branche est désactivée, la jonction doit savoir comment réagir.

L’absence de résultat n’est pas automatiquement une erreur.

Mais elle ne doit jamais être silencieuse.

---

## Le bypass doit laisser une cicatrice

Un bypass est utile.

Il permet de continuer à tester une architecture même lorsqu’un module est incomplet.

Mais il présente un danger :

on peut oublier qu’il existe.

Alors toute exécution en bypass doit produire une trace.

Si B3 a été contourné au tick 481, cette information doit rester visible.

Ainsi, si la sortie semble excellente, nous savons qu’elle a été obtenue sans B3.

Impossible de lui attribuer un rôle qu’il n’a pas joué.

---

## Le système doit pouvoir dire « je ne sais pas »

Une architecture robuste doit avoir une représentation de l’inconnu.

Pas seulement de l’erreur.

L’erreur signifie souvent :

une opération attendue a échoué.

L’inconnu peut signifier :

nous n’avons pas assez d’information pour décider.

C’est différent.

Nous pouvons donc conserver :

[
UNKNOWN
]

comme état légitime.

Un système qui ne possède pas cette valeur finit souvent par remplir le vide avec zéro, faux, ou une estimation silencieuse.

---

## L’incertitude doit voyager

Si une mesure possède une incertitude, la transformation ne devrait pas automatiquement la perdre.

On peut représenter une mesure comme :

[
x pm sigma_x
]

ou plus généralement par une distribution.

Lorsqu’elle traverse un calcul, l’incertitude peut elle aussi être propagée.

Même si Brutus n’implémente pas immédiatement toute la théorie nécessaire, l’architecture doit éviter de rendre impossible cette évolution.

C’est une autre raison de définir les types proprement.

---

## Le contrat minimal d’un module

Nous pouvons maintenant proposer une fiche candidate.

### IDENTITÉ

- nom;
- id;
- version.

### PORTS

- INPUT;
- OUTPUT;
- STATE;
- ERROR;
- TIME.

### CONTRATS

- types;
- unités;
- domaines;
- valeurs manquantes;
- règles de synchronisation.

### COMPORTEMENT

- transformation;
- déterministe ou non;
- dépendances.

### TRACE

- événements;
- état avant;
- état après;
- provenance.

### TESTS

- cas nominal;
- limites;
- erreur;
- redémarrage;
- replay.

Ce n’est pas encore un standard officiel.

Mais c’est déjà assez pour empêcher beaucoup de mystère.

---

## Le contrat minimal d’un lien

Une connexion peut posséder sa propre fiche.

### SOURCE

Module et port source.

### DESTINATION

Module et port destination.

### TYPE

Structure de donnée.

### UNITÉ

Lorsque pertinente.

### MODE

Direct, bufferisé, streaming, événementiel, autre.

### SYNCHRONISATION

Règle de tick ou de temps.

### QUALITÉ

Conditions d’acceptation.

### ÉCHEC

Que faire lorsque le transfert ne peut pas être effectué.

Ainsi, le lien cesse d’être une ligne anonyme.

---

## Les tests de connexion

Nous pouvons tester un lien indépendamment de l’ensemble du système.

1. envoyer une valeur valide;
2. vérifier la réception;
3. envoyer un type invalide;
4. vérifier le refus;
5. retarder le message;
6. vérifier la règle de timeout;
7. couper la destination;
8. vérifier la réaction;
9. rétablir la destination;
10. vérifier la reprise.

Cette approche réduit énormément la difficulté de débogage.

---

## Tester petit avant d’assembler grand

Cette règle rejoint une philosophie déjà présente dans Brutus :

**construire petit → vérifier → cloner → étendre.**

Si B1 fonctionne seul, nous testons B1.

Puis :

[
B1 ightarrow B2
]

Puis :

[
B1 ightarrow B2 ightarrow B3
]

Puis les branches.

Puis la jonction.

Puis les boucles.

Chaque étape ajoute une complexité identifiable.

Si tout est assemblé d’un coup, les erreurs deviennent difficiles à localiser.

---

## La première plaque

Imaginons une plaque minimale :

[
INPUT
ightarrow
B1
ightarrow
OUTPUT
]

Elle paraît presque ridicule.

C’est une qualité.

Nous pouvons mesurer exactement :

ce qui entre;

ce que B1 fait;

ce qui sort.

Puis ajouter B2 :

[
INPUT
ightarrow
B1
ightarrow
B2
ightarrow
OUTPUT
]

Et comparer.

Le système grandit par preuves locales.

---

## Le premier embranchement

Ensuite :

[
INPUT
ightarrow
B1
ightarrow
egin{cases}
B2\
B3
end{cases}
]

Puis :

[
(B2,B3)ightarrow J
]

À ce moment, nous avons créé un véritable problème architectural.

Deux chemins.

Une synchronisation.

Une jonction.

C’est petit.

Mais déjà riche.

Nous pouvons le tester complètement avant de passer à quatre chemins.

---

## Quatre chemins sans magie

Lorsque quatre chemins arrivent, il peut être tentant de leur attribuer immédiatement une signification profonde.

Nous devons résister à cette tentation.

D’abord, ils doivent fonctionner comme quatre routes définies.

[
INPUT
ightarrow
D
ightarrow
(P_1,P_2,P_3,P_4)
ightarrow
J
ightarrow
OUTPUT
]

où (D) est la divergence et (J) la jonction.

Ensuite seulement, chaque (P_k) reçoit sa fonction.

La symbolique peut venir après.

Le mécanisme doit venir avant.

---

## Une architecture peut accueillir la symbolique sans lui obéir

La Bible Brutus contient des nombres, des formes et des motifs qui possèdent une importance narrative ou exploratoire.

Nous n’avons pas besoin de les supprimer.

Nous devons seulement éviter une confusion.

Un nombre peut être :

un choix d’architecture;

un paramètre;

un résultat;

un symbole;

une contrainte;

une observation.

Ces statuts ne sont pas interchangeables.

Quatre chemins peuvent être choisis parce qu’une structure à quatre branches est utile.

Cela ne prouve aucune loi naturelle liée au nombre quatre.

La distinction protège la liberté créative.

---

## Le mécanisme doit pouvoir survivre au changement de symbole

Voilà un bon test.

Si nous renommons les quatre chemins A, B, C, D au lieu de leur donner des noms symboliques, le calcul doit continuer à fonctionner.

Si le système casse parce que le symbole a changé, le symbole était probablement devenu une dépendance cachée.

Une bonne architecture sépare :

**ce que la machine fait**

de :

**ce que nous racontons à propos de ce qu’elle fait.**

---

## La visualisation peut ensuite réunir les deux

Une fois le mécanisme stable, l’interface peut réintroduire la richesse visuelle.

Couleurs.

Cristaux.

Ondes.

Conduits.

Battements.

Lumières.

Mais chaque élément peut alors pointer vers une variable réelle.

Une lumière n’est plus seulement belle.

Elle signifie un état réel.

Un conduit animé signifie qu’un débit mesuré est non nul.

Une pulsation signifie qu’un tick a été reçu.

Une fissure signifie qu’une erreur existe.

L’esthétique devient instrumentale.

---

## L’inspecteur

Une interface Brutus devrait pouvoir permettre à l’opérateur de cliquer sur un module et de voir :

identité;

version;

ports;

état actuel;

dernière entrée;

dernière sortie;

dernier tick;

erreurs;

liens entrants;

liens sortants.

Puis cliquer sur un lien et voir :

source;

destination;

type;

unité;

dernière transmission;

latence;

statut.

Le dessin devient alors un microscope.

---

## Le visiteur et l’architecte

Tous les utilisateurs n’ont pas besoin du même accès.

Le visiteur peut regarder.

L’architecte peut inspecter.

L’opérateur autorisé peut modifier.

Ces rôles doivent être séparés techniquement.

Une vitre visuelle n’est pas une permission.

Un bouton caché n’est pas une sécurité.

Le serveur ou le noyau d’autorité doit décider ce qui est permis.

Encore une fois :

aucune relation invisible.

Même la relation entre utilisateur et pouvoir d’action doit être explicite.

---

## La connexion humaine fait aussi partie du système

Un système interactif possède un acteur supplémentaire :

l’opérateur.

Il envoie des commandes.

Il change des paramètres.

Il donne GO.

Ces actions doivent recevoir elles aussi une provenance.

Non pas pour surveiller inutilement la personne.

Pour pouvoir comprendre plus tard pourquoi le système a changé.

Dire qu’un paramètre a changé de A vers B n’est pas complet.

Il faut aussi savoir :

quand;

par quel rôle;

dans quelle session;

avec quel résultat.

---

## Le droit à l’annulation

Une architecture contrôlable doit penser au retour.

Une modification de configuration peut être :

proposée;

prévisualisée;

appliquée;

vérifiée;

annulée.

Ce cycle limite les actions irréversibles.

Nous pouvons l’écrire :

[
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

et, lorsque possible :

[
VERIFY_FAIL
ightarrow
ROLLBACK
]

Le GO n’est donc pas seulement un enthousiasme.

Il peut devenir une frontière transactionnelle.

---

## Une architecture honnête montre aussi ses blocages

Si une connexion attend une permission, l’interface doit dire **BLOCKED**.

Si elle attend une donnée : **WAITING INPUT**.

Si elle attend un autre chemin : **WAITING SYNC**.

Si elle est cassée : **ERROR**.

Si son statut est inconnu : **UNKNOWN**.

Le silence opérationnel est dangereux.

Un système qui ne fait rien doit pouvoir expliquer pourquoi il ne fait rien.

---

## Le cœur n’est pas un raccourci

Dans notre langage, nous parlons parfois du cœur d’un système.

Cela peut désigner le centre.

La boucle principale.

La source de synchronisation.

La reine.

Le module central.

Mais le mot ne doit jamais permettre d’éviter une définition.

Si quelque chose est appelé **cœur**, nous devons encore pouvoir répondre :

quelles entrées ?

quelles sorties ?

quel état ?

quel temps ?

quelles erreurs ?

quelles responsabilités ?

Le symbole peut rester.

Le contrat doit exister.

---

## Une architecture devient belle lorsqu’elle peut être interrogée

La beauté ne vient plus seulement de sa symétrie.

Elle vient d’une propriété plus rare :

on peut lui poser des questions.

Pourquoi cette sortie vaut-elle 0.408 ?

Quel chemin a contribué ?

Quel module a changé l’état ?

À quel tick ?

Quelle entrée a déclenché l’événement ?

Quelle version tournait ?

Quel lien a transporté la donnée ?

Quelle unité a été utilisée ?

Si le système peut répondre, nous avons construit quelque chose de puissant.

---

## Le graphe vivant

À ce stade, nous pouvons imaginer Brutus non comme une image fixe, mais comme un graphe vivant :

[
G_t=(V_t,E_t,S_t)
]

où :

- (V_t) = modules actifs au temps (t);
- (E_t) = connexions actives au temps (t);
- (S_t) = état du système au temps (t).

Une modification devient alors :

[
G_t ightarrow G_{t+1}
]

Et cette transition peut être enregistrée.

Nous ne voyons plus seulement le système.

Nous voyons son histoire.

---

## Une histoire calculable

Lorsque chaque transition est tracée, l’histoire cesse d’être uniquement narrative.

Elle peut être interrogée.

Combien de fois B3 est-il passé en erreur ?

Quel lien possède la plus grande latence ?

Quel chemin est le plus souvent désynchronisé ?

À quel tick la divergence a commencé ?

Quelle version a introduit le changement ?

Le journal devient donnée.

La mémoire devient instrument.

---

## Le système peut apprendre de ses erreurs sans devenir mystérieux

Un jour, certains modules pourront peut-être adapter leurs paramètres à partir de l’expérience.

Mais même alors, la règle demeure.

Si un paramètre change :

avant;

après;

raison;

données utilisées;

version de l’algorithme.

Tout doit être conservable.

Un système adaptatif n’a pas le droit d’utiliser « il a appris » comme explication finale.

L’apprentissage doit laisser des traces lui aussi.

---

## Pas d’intelligence supplémentaire cachée

Le registre de continuité n’a pas besoin d’être une nouvelle intelligence.

Le routeur n’a pas besoin d’avoir des intentions.

Le logger n’a pas besoin de comprendre.

Chaque fonction peut rester simple.

Cela protège l’architecture contre l’inflation conceptuelle.

Nous n’avons pas besoin d’ajouter une conscience chaque fois qu’une fonction devient utile.

Nous avons besoin de rôles définis.

---

## Le petit gagne encore

Il est tentant de vouloir immédiatement construire le grand Brutus à quatre chemins, avec cristallisation, mémoire, fréquence, contrôle et visualisation.

Mais le chapitre 12 nous donne une méthode différente.

Un port.

Puis deux.

Un module.

Puis deux.

Un lien.

Puis un embranchement.

Une jonction.

Un cycle.

Un état.

Un test.

Petit à petit, le mécanisme devient assez clair pour accueillir la complexité sans l’avaler.

---

## Première preuve attendue

Pour ce chapitre, la preuve la plus utile ne serait pas un grand discours.

Ce serait un prototype minimal où :

1. un INPUT reçoit une valeur typée;
2. B1 la transforme;
3. la sortie est enregistrée;
4. chaque étape porte un tick;
5. une erreur de type est rejetée;
6. le chemin complet est visible dans un log.

Si cela fonctionne, nous avons une petite architecture réelle.

Pas encore Brutus complet.

Mais une cellule de Brutus.

---

## Deuxième preuve attendue

Ensuite, créer deux chemins :

[
P_1
]

et :

[
P_2
]

à partir de la même entrée.

Le système doit prouver :

qu’ils reçoivent la même entrée;

qu’ils possèdent des identités différentes;

qu’ils produisent des sorties séparées;

qu’une jonction peut les réunir;

qu’une panne dans un chemin est visible.

C’est une étape beaucoup plus importante qu’ajouter cinquante modules d’un coup.

---

## Troisième preuve attendue

Passer à quatre chemins.

Mais sans ajouter de symbolique nouvelle.

Seulement l’architecture.

Si quatre chemins peuvent être créés, identifiés, synchronisés, testés et rejoués, alors nous disposons d’un squelette robuste.

Après cela, les fonctions complexes pourront être introduites une par une.

---

## Condition d’abandon

Une idée sérieuse doit aussi savoir quand elle échoue.

Nous devrions abandonner ou réviser cette architecture si elle crée plus de confusion qu’elle n’en enlève.

Par exemple si :

les ports deviennent trop génériques;

les logs explosent sans utilité;

la latence de traçage devient excessive;

les contrats empêchent l’expérimentation au lieu de la sécuriser;

les quatre chemins n’apportent aucune distinction fonctionnelle.

Le but n’est pas de défendre la structure.

Le but est de construire un système compréhensible.

---

## La règle qui survivra même si tout change

Les noms peuvent changer.

Les cinq ports peuvent devenir sept.

Les quatre chemins peuvent devenir trois ou huit.

Le format de log peut être remplacé.

Les modules B1, B2 et B3 peuvent disparaître.

Mais une règle devrait rester :

> **Si quelque chose influence le résultat, cette influence doit pouvoir être retrouvée.**

C’est le cœur du chapitre.

---

## Le mécanisme apparaît

Nous étions partis du silence.

D’une formule.

D’une trace.

Maintenant apparaissent :

les ports;

les modules;

les liens;

les chemins;

les états;

les erreurs;

le temps;

les contrats;

les logs.

Le dessin commence à devenir système.

Et quelque chose d’important se produit.

Plus l’architecture devient explicite, moins nous avons besoin de croire qu’elle fonctionne.

Nous pouvons regarder.

---

## La prochaine porte

Une question reste pourtant ouverte.

Nous avons donné au temps un port.

Nous avons utilisé des ticks.

Nous avons parlé de synchronisation.

Mais nous n’avons pas encore défini le temps du système.

Qui produit le tick ?

À quelle fréquence ?

Que se passe-t-il lorsqu’un module arrive en retard ?

Comment deux cycles se rencontrent-ils ?

Comment distinguer temps réel, temps simulé et temps observé ?

Le chapitre 12 ne doit pas répondre trop vite.

Il doit seulement laisser la porte ouverte.

Le mécanisme possède maintenant ses connexions.

Le prochain chapitre devra lui donner son rythme.

---

## Dernière règle

Avant de quitter ce chapitre, nous pouvons regarder une dernière fois le schéma.

B1.

B2.

B3.

Les quatre chemins.

Les ports.

Les flèches.

Le registre.

Puis poser une question simple à chaque ligne :

**Pourquoi es-tu là ?**

Si nous pouvons répondre, la ligne reste.

Si nous ne pouvons pas répondre, elle devient :

**CANDIDAT.**

Et si personne ne sait qu’elle existe :

elle doit disparaître ou être révélée.

Parce qu’à partir d’ici, notre architecture possède une loi.

# **AUCUNE CONNEXION INVISIBLE.**
