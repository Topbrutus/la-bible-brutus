# Chapitre 13 — Le Battement du Système

**APRÈS L’INTRODUCTION — TROISIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** L’Horloge de la vie  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Un système peut posséder toutes ses pièces et toutes ses connexions.  
> Tant qu’il ne sait pas quand elles agissent, il n’a pas encore de rythme.**

---

## Le mécanisme possède maintenant ses connexions

Le chapitre 12 a posé une loi :

# **AUCUNE CONNEXION INVISIBLE.**

Les modules ont reçu des ports.

Les liens ont reçu une identité.

Les erreurs ont reçu un chemin.

Les états ont reçu une trace.

Les quatre chemins ont reçu le droit d’exister, mais pas le droit d’être mystérieux.

Il reste maintenant une dimension que les flèches seules ne peuvent pas montrer.

Le temps.

Une connexion nous dit :

**qui parle à qui.**

Le temps nous dit :

**quand.**

Et parfois, dans un système dynamique, le **quand** change complètement le sens du **quoi**.

---

## Une même valeur à deux instants n’est pas le même événement

Supposons qu’un module produise :

[
x = 1
]

au tick (n).

Puis encore :

[
x = 1
]

au tick (n+1).

Numériquement, les valeurs sont identiques.

Mais ce ne sont pas nécessairement les mêmes événements.

Le premier 1 peut avoir déclenché une transition.

Le second peut avoir maintenu un état.

Ou le premier peut appartenir à un cycle et le second à un autre.

Alors une donnée dynamique ne doit pas être définie seulement par sa valeur.

Elle doit également être située dans le temps.

Nous pouvons écrire :

[
D_n = (x_n,	au_n)
]

où :

- (x_n) est la valeur;
- (	au_n) est son repère temporel.

Le temps devient ainsi une partie de l’identité opérationnelle de la donnée.

---

## Le tick

Le mot **tick** est simple.

C’est sa force.

Un tick est un repère discret de progression.

Nous pouvons le représenter par :

[
n in mathbb{N}
]

avec :

[
n = 0,1,2,3,ldots
]

Le passage :

[
n ightarrow n+1
]

signifie que le système avance d’une étape logique.

Cette définition ne dit encore rien sur le nombre de secondes réelles écoulées.

Un tick peut correspondre à :

une milliseconde;

un dixième de seconde;

une seconde;

une étape de simulation;

un événement externe;

ou simplement un numéro d’ordre.

Le tick n’est donc pas automatiquement du temps physique.

C’est d’abord un **ordre causal discret**.

---

## Ordre et durée sont deux choses différentes

C’est une distinction fondamentale.

Le tick répond à :

**quel événement vient avant quel autre ?**

La durée répond à :

**combien de temps s’est écoulé ?**

On peut avoir :

[
n_1 < n_2
]

sans connaître précisément :

[
Delta t = t_2 - t_1
]

Inversement, on peut connaître une durée sans posséder un numéro de tick global.

Une architecture robuste doit éviter de confondre les deux.

---

## Le temps réel

Appelons :

[
t_{	ext{wall}}
]

le temps de l’horloge réelle observée par la machine.

Il peut être fourni par le système d’exploitation ou une horloge monotone.

Mais même ici, il faut être prudent.

Toutes les horloges ne servent pas au même usage.

Une horloge civile peut changer si :

l’heure système est corrigée;

le fuseau change;

une synchronisation réseau intervient;

l’utilisateur modifie l’heure.

Pour mesurer une durée d’exécution, une horloge monotone est généralement plus appropriée.

Le principe est simple :

> **Le temps affiché au calendrier et le temps utilisé pour mesurer une durée ne sont pas nécessairement la même horloge.**

---

## Le temps simulé

Un système scientifique ou expérimental peut posséder un temps propre.

Appelons-le :

[
t_{	ext{sim}}
]

Il peut évoluer selon :

[
t_{	ext{sim},n+1}
=
t_{	ext{sim},n}
+
Delta t_{	ext{sim}}
]

Le pas :

[
Delta t_{	ext{sim}}
]

est alors une décision de simulation.

Ce temps peut avancer plus vite ou plus lentement que le monde réel.

Il peut même être mis sur pause.

Ainsi :

[
t_{	ext{sim}}

eq
t_{	ext{wall}}
]

en général.

Cette séparation est essentielle.

---

## Pourquoi séparer les deux temps ?

Supposons qu’un calcul simule dix secondes physiques en une seconde réelle.

Alors :

[
Delta t_{	ext{sim}} = 10 	ext{ s}
]

pendant que :

[
Delta t_{	ext{wall}} = 1 	ext{ s}
]

Si l’interface confond ces deux grandeurs, elle peut afficher une vitesse incorrecte ou une fréquence trompeuse.

Le système doit donc déclarer clairement quel temps chaque métrique utilise.

---

## Le temps observé

Il existe encore une troisième notion.

Le temps auquel un observateur reçoit l’information.

Appelons-le :

[
t_{	ext{obs}}
]

Un événement peut avoir été produit à :

[
t_{	ext{source}}
]

transmis à :

[
t_{	ext{emit}}
]

reçu à :

[
t_{	ext{receive}}
]

et affiché à :

[
t_{	ext{obs}}
]

Ces temps peuvent être différents.

La différence :

[
L = t_{	ext{obs}} - t_{	ext{source}}
]

peut être interprétée comme une latence de bout en bout, selon la définition retenue.

Le mot **latence** ne doit donc jamais apparaître sans préciser ses bornes.

---

## L’horloge de la vie

Dans notre langage de création, l’expression **Horloge de la vie** existe comme image.

Elle évoque quelque chose de central.

Un battement.

Une reine temporelle.

Un rythme partagé par plusieurs modules.

Cette image est puissante.

Mais pour qu’elle devienne architecture, il faut la traduire.

Le terme peut désigner, selon la version :

une source de ticks;

un ordonnanceur;

un registre de temps;

une horloge de simulation;

un synchroniseur;

ou une combinaison contrôlée de ces fonctions.

Le symbole peut rester.

Mais sa fonction doit être écrite.

---

## La reine ne doit pas devenir magique

Si nous appelons une horloge **Reine**, ce mot ne lui donne aucun pouvoir supplémentaire.

Elle doit encore avoir :

des entrées;

des sorties;

un état;

des erreurs;

une fréquence;

des règles de dérive;

des garanties;

des limites.

Une reine technique peut être centrale.

Elle ne doit jamais devenir inexplicable.

La règle du chapitre 12 continue donc ici :

**aucune influence temporelle invisible.**

---

## Une source de tick minimale

Nous pouvons définir une source de ticks candidate :

[
Q(n,t)
]

où :

- (n) est le numéro de tick;
- (t) est le temps associé.

À chaque émission :

[
Q_n = (n,t_n)
]

Les modules abonnés reçoivent alors le même identifiant de cycle.

Ainsi, quatre chemins peuvent savoir qu’ils travaillent sur le même battement.

---

## Une fréquence de tick

Si les ticks sont périodiques, nous pouvons définir une fréquence nominale :

[
f_{	ext{tick}}
=
rac{1}{T_{	ext{tick}}}
]

où :

[
T_{	ext{tick}}
]

est la période nominale.

Par exemple, si :

[
T_{	ext{tick}} = 0.01 	ext{ s}
]

alors :

[
f_{	ext{tick}} = 100 	ext{ Hz}
]

Mais une fréquence nominale n’est pas une fréquence mesurée.

Le système doit pouvoir distinguer les deux.

---

## Nominal n’est pas mesuré

Une configuration peut demander :

[
f_{	ext{target}} = 100 	ext{ Hz}
]

mais l’exécution réelle peut produire :

[
f_{	ext{measured}} = 97.4 	ext{ Hz}
]

à cause de :

latence;

charge CPU;

I/O;

ordonnancement;

attente réseau;

autres tâches.

Alors le tableau de bord ne doit jamais afficher 100 Hz comme performance réelle simplement parce que 100 Hz est la consigne.

Une consigne est une cible.

Une mesure est une observation.

---

## Le temps d’exécution

Pour chaque tick, nous pouvons mesurer :

[
R_{	ext{exec},n}
=
t_{	ext{end},n}
-
t_{	ext{start},n}
]

Cette grandeur représente le temps d’exécution du cycle selon les bornes choisies.

Elle permet une question essentielle :

le système termine-t-il son travail avant le tick suivant ?

Si :

[
R_{	ext{exec},n}
<
T_{	ext{tick}}
]

le cycle dispose d’une marge.

Si :

[
R_{	ext{exec},n}
>
T_{	ext{tick}}
]

le système est en retard.

---

## La marge temporelle

Définissons :

[
M_n
=
T_{	ext{tick}}
-
R_{	ext{exec},n}
]

Alors :

[
M_n > 0
]

signifie qu’une marge existe.

[
M_n = 0
]

signifie que le cycle utilise exactement son budget.

[
M_n < 0
]

signifie que le budget temporel est dépassé.

Cette métrique est simple.

Elle peut pourtant révéler beaucoup.

---

## Le retard n’est pas seulement un chiffre

Si un cycle dépasse son budget, plusieurs stratégies sont possibles.

Le système peut :

attendre;

sauter un tick;

accumuler le retard;

ralentir la simulation;

dégrader certains calculs;

mettre une branche en retard;

déclarer une erreur.

Aucune de ces politiques n’est universellement correcte.

Mais la politique choisie doit être explicite.

---

## Le jitter

Même si la fréquence moyenne semble correcte, l’intervalle entre ticks peut varier.

Définissons :

[
Delta t_n
=
t_n - t_{n-1}
]

Si le système vise une période :

[
T
]

alors l’écart instantané peut être :

[
j_n
=
Delta t_n - T
]

Le **jitter** représente la variabilité temporelle.

Une moyenne parfaite peut cacher un jitter important.

Deux systèmes à 100 Hz de moyenne peuvent donc avoir des comportements très différents.

---

## La moyenne ne suffit pas

Supposons les intervalles :

[
5,;15,;5,;15 	ext{ ms}
]

La moyenne vaut :

[
10 	ext{ ms}
]

Donc, en moyenne, 100 Hz.

Mais le rythme alterne fortement.

Une autre séquence :

[
10,;10,;10,;10 	ext{ ms}
]

possède la même moyenne.

Son comportement temporel est pourtant beaucoup plus stable.

Ainsi, une fréquence moyenne ne décrit pas toute la qualité temporelle.

---

## Mesurer la dispersion

Nous pouvons utiliser des mesures comme :

moyenne;

écart-type;

minimum;

maximum;

percentiles.

Par exemple :

[
mu_{Delta t}
=
rac{1}{N}
sum_{n=1}^{N}
Delta t_n
]

et :

[
sigma_{Delta t}
=
sqrt{
rac{1}{N}
sum_{n=1}^{N}
(Delta t_n-mu_{Delta t})^2
}
]

Ces statistiques ne sont pas décoratives.

Elles permettent de distinguer une cadence stable d’une cadence irrégulière.

---

## Le rythme des quatre chemins

Le chapitre précédent a introduit :

[
P_1,P_2,P_3,P_4
]

Chaque chemin peut avoir son propre temps d’exécution :

[
R_1,R_2,R_3,R_4
]

Supposons que tous reçoivent le tick (n).

Le temps de la jonction dépendra probablement du chemin le plus lent si la barrière attend tout le monde.

Alors :

[
R_{	ext{join},n}
ge
max(R_{1,n},R_{2,n},R_{3,n},R_{4,n})
]

selon l’architecture.

Le chemin le plus lent peut donc gouverner le rythme collectif.

---

## Le chemin lent

Cette propriété produit un phénomène important.

Un seul chemin peut devenir le goulot d’étranglement.

Même si trois chemins terminent en 2 ms, si le quatrième prend 20 ms, une jonction stricte doit attendre.

Nous devons donc pouvoir mesurer :

[
R_{k,n}
]

pour chaque branche (k).

Sinon le retard global apparaît sans cause identifiable.

---

## Synchroniser ne veut pas toujours dire attendre

Une barrière stricte est une stratégie.

Pas la seule.

On peut aussi utiliser :

la dernière valeur disponible;

une interpolation;

une fenêtre temporelle;

un timeout;

un mode partiel;

un mécanisme asynchrone.

Mais chacune de ces stratégies change le sens de la sortie.

Alors la jonction doit déclarer sa politique.

---

## Synchronisation stricte

Une règle stricte peut être :

[
READY(n)
=
igwedge_{k=1}^{4}
AVAILABLE(P_k,n)
]

La sortie du tick (n) n’est calculée que lorsque les quatre chemins ont produit leur résultat du tick (n).

Cette règle favorise la cohérence de cycle.

Elle peut augmenter la latence.

---

## Synchronisation par fenêtre

Une autre possibilité est d’accepter les résultats compris dans une fenêtre :

[
|t_k-t_{	ext{ref}}|
le
epsilon
]

où (epsilon) est une tolérance temporelle.

Cette stratégie peut être utile pour des sources qui ne peuvent pas être parfaitement synchronisées.

Mais la valeur de (epsilon) doit être justifiée.

Sinon elle devient un paramètre de confort.

---

## Le timeout

Une jonction ne peut pas toujours attendre éternellement.

Nous pouvons définir :

[
T_{	ext{timeout}}
]

Si une branche n’a pas répondu avant cette limite, le système doit choisir une action.

Par exemple :

[
WAITING
ightarrow
TIMEOUT
ightarrow
ERROR
]

ou :

[
WAITING
ightarrow
TIMEOUT
ightarrow
PARTIAL
]

La différence est importante.

Un résultat partiel ne doit jamais être présenté comme complet.

---

## Le tick perdu

Que faire si un module ne reçoit pas le tick (n), puis reçoit (n+1) ?

Plusieurs politiques sont possibles.

Rejouer le tick manquant.

Sauter.

Réinitialiser.

Mettre en faute.

Chaque module sensible au temps doit donc préciser sa politique de perte.

Une séquence :

[
100,;101,;103
]

contient une information importante :

le tick 102 manque.

---

## Le tick en double

L’inverse existe aussi.

Un module peut recevoir deux fois :

[
n=102
]

Le système doit savoir si l’opération est idempotente.

Autrement dit :

répéter exactement la même commande produit-il le même état sans effet supplémentaire ?

Si oui, le doublon peut parfois être ignoré.

Sinon, il peut créer une erreur grave.

Le numéro de tick devient alors une protection contre les répétitions accidentelles.

---

## Idempotence temporelle

Une opération (F) est idempotente lorsque :

[
F(F(x)) = F(x)
]

Toutes les opérations ne le sont pas.

**SET value = 3** peut l’être.

**ADD 3** ne l’est pas.

Si un message ADD 3 est reçu deux fois, le résultat change deux fois.

Alors les identifiants d’événements et de ticks deviennent essentiels.

---

## Le temps et l’état

Pour un système à état :

[
S_{n+1}
=
F(S_n,I_n)
]

l’ordre des événements compte.

En général :

[
F(F(S,I_a),I_b)

eq
F(F(S,I_b),I_a)
]

Donc une inversion de deux entrées peut produire un autre état final.

Le temps n’est plus seulement une mesure.

Il participe à la causalité.

---

## Causalité

La causalité est plus profonde que la simple chronologie.

Un événement peut être antérieur sans être la cause d’un autre.

Mais lorsqu’un événement est utilisé comme entrée d’un calcul, son ordre devient une partie du chemin causal.

Nous pouvons représenter :

[
A ightarrow B
]

comme une dépendance.

Si B ne peut pas être produit sans A, nous pouvons tracer cette relation.

Le temps aide à vérifier que la causalité déclarée respecte l’ordre des événements.

---

## Un registre causal

Nous pouvons enrichir notre registre :

[
R_n=
(
id,
parent,
tick,
t_{	ext{source}},
t_{	ext{receive}},
module,
input,
output,
state
)
]

Le champ **parent** permet de lier un événement à celui qui l’a déclenché.

Ainsi, une sortie finale peut être remontée jusqu’à ses événements racines.

---

## Le temps d’un signal

Un signal continu peut être écrit :

[
x(t)
]

Un signal échantillonné :

[
x[n]
=
x(nT_s)
]

où :

[
T_s
]

est la période d’échantillonnage.

La fréquence d’échantillonnage vaut :

[
f_s
=
rac{1}{T_s}
]

Cette relation sera importante dès que Brutus travaillera avec des ondes, des capteurs ou des fréquences réelles.

---

## Échantillonner n’est pas regarder parfaitement

Lorsque nous échantillonnons un signal continu, nous n’observons pas tous les instants.

Nous observons une suite de points.

Alors le choix de :

[
f_s
]

détermine ce que le système peut reconstruire ou distinguer.

C’est ici qu’un mot classique apparaît :

**aliasing.**

---

## Le critère de Nyquist-Shannon

Pour un signal limité en bande, une condition classique de reconstruction idéale impose un échantillonnage strictement supérieur à deux fois la fréquence maximale du signal :

[
f_s > 2f_{max}
]

dans les conditions appropriées.

Cette règle ne signifie pas que deux échantillons par période suffisent toujours à une mesure pratique de haute qualité.

Elle donne une limite théorique de reconstruction pour certaines hypothèses.

Mais elle montre quelque chose de fondamental :

> **Le rythme de l’observateur peut limiter ce qu’il croit voir.**

---

## Une fréquence invisible peut devenir une fausse fréquence

Si un système échantillonne trop lentement, une oscillation rapide peut apparaître comme une oscillation plus lente.

Le signal n’a pas réellement changé.

C’est l’observation qui l’a déformé.

Cette idée est extrêmement importante pour une architecture où les formes visuelles jouent un rôle.

Une belle oscillation à l’écran peut être un artefact d’échantillonnage.

Alors :

**forme visible ≠ fréquence réelle**

tant que la chaîne de mesure n’est pas connue.

---

## L’écran a lui aussi une fréquence

Une interface possède une fréquence d’affichage.

Appelons-la :

[
f_{	ext{display}}
]

Le moteur peut calculer à :

[
f_{	ext{engine}}
]

et l’écran afficher à une autre cadence.

Par exemple :

[
f_{	ext{engine}} = 200 	ext{ Hz}
]

et :

[
f_{	ext{display}} = 60 	ext{ Hz}
]

Cela peut être parfaitement correct.

L’interface n’a pas besoin de dessiner chaque tick.

Mais elle doit savoir ce qu’elle agrège ou ignore.

---

## Le visuel ne doit pas piloter le moteur sans décision explicite

Si le moteur attend le rafraîchissement graphique avant d’avancer, le système devient dépendant de la performance d’affichage.

Cela peut être voulu.

Mais souvent, il vaut mieux séparer :

boucle de simulation;

boucle d’interface;

boucle réseau.

La séparation empêche une fenêtre lente de modifier silencieusement le temps scientifique.

---

## Trois cadences

Nous pouvons donc avoir :

[
f_{	ext{sim}}
]

[
f_{	ext{ui}}
]

[
f_{	ext{network}}
]

Elles n’ont pas besoin d’être identiques.

Mais leurs échanges doivent être définis.

Par exemple :

la simulation produit 100 états par seconde;

l’interface en affiche 60;

le réseau en diffuse 20.

Cette architecture peut fonctionner si chaque couche connaît sa responsabilité.

---

## Le buffer

Lorsque deux cadences diffèrent, un buffer peut intervenir.

Le producteur écrit.

Le consommateur lit.

Mais le buffer introduit des questions :

quelle taille ?

FIFO ou dernière valeur seulement ?

que faire lorsqu’il est plein ?

que faire lorsqu’il est vide ?

Ces choix sont temporels.

Une file FIFO conserve l’ordre.

Un registre « latest value » sacrifie l’historique pour la fraîcheur.

Aucun choix n’est neutre.

---

## Fraîcheur contre exhaustivité

Supposons qu’une interface n’ait besoin que du dernier état.

Alors garder 1000 états intermédiaires peut être inutile.

Un registre de dernière valeur suffit.

Mais pour une analyse scientifique, perdre les états intermédiaires peut être inacceptable.

Alors nous devons distinguer :

**LIVE VIEW**

et :

**RECORDING**

Le live peut privilégier la fraîcheur.

L’enregistrement doit préserver la preuve.

---

## Le replay dépend du temps

Rejouer un système ne signifie pas seulement réinjecter les mêmes valeurs.

Il faut parfois reproduire leurs intervalles.

Deux séquences identiques :

[
A,B,C
]

peuvent produire des résultats différents si les délais sont différents.

Nous pouvons donc enregistrer :

[
(A,Delta t_1),
(B,Delta t_2),
(C,Delta t_3)
]

Le replay peut ensuite utiliser :

**temps original**

ou :

**temps normalisé**

ou :

**pas-à-pas contrôlé**.

Le mode doit être déclaré.

---

## La vitesse de replay

Un replay peut être accéléré :

[
r > 1
]

ralenti :

[
0 < r < 1
]

ou exécuté à vitesse originale :

[
r = 1
]

avec :

[
Delta t_{	ext{replay}}
=
rac{Delta t_{	ext{original}}}{r}
]

Cette fonction est utile pour analyser des événements rares.

Mais elle ne doit pas modifier les calculs qui utilisent le temps simulé si le replay doit rester fidèle.

---

## Pause

Une horloge de simulation peut permettre :

[
PAUSE
]

Cela semble trivial.

Mais il faut définir ce qui s’arrête.

Le temps simulé ?

Les entrées réseau ?

L’interface ?

Les timers ?

Les erreurs ?

Le logging ?

Une pause ambiguë peut produire des états incohérents.

---

## Reset

Même problème avec :

[
RESET
]

Un reset peut signifier :

remettre le tick à zéro;

effacer l’état;

vider les buffers;

conserver les logs;

reseed l’aléatoire;

repartir d’un snapshot.

La commande doit avoir une sémantique exacte.

Sinon deux personnes peuvent demander « reset » en imaginant deux opérations différentes.

---

## Démarrage

Le premier tick mérite lui aussi une définition.

Quel est l’état avant :

[
n=0
]

?

Appelons-le :

[
S_0
]

Il peut provenir :

d’une configuration;

d’un snapshot;

d’un état nul;

d’une graine;

d’un fichier de checkpoint.

Le démarrage parfait n’est pas l’absence de passé.

C’est la capacité à dire exactement d’où vient l’état initial.

---

## Le temps zéro

Le symbole :

[
t_0
]

peut désigner le début d’une expérience.

Mais ce début doit être défini.

Moment où le processus démarre ?

Premier tick valide ?

Première entrée reçue ?

Première sortie produite ?

Activation du GO ?

La définition choisie doit rester stable pendant l’analyse.

Sinon toutes les durées deviennent ambiguës.

---

## Un état zéro vérifié

Une expérience sérieuse bénéficie d’un **état zéro**.

Cela signifie qu’avant de commencer, nous connaissons suffisamment :

les versions;

les paramètres;

l’état des modules;

les buffers;

les connexions;

la source d’horloge;

le seed éventuel.

Nous pouvons alors écrire :

[
S(t_0)=S_0
]

avec une provenance.

Le temps zéro devient un checkpoint.

---

## Les snapshots

Un snapshot capture un état à un instant :

[
Sigma_n = S(t_n)
]

Si le système sait restaurer ce snapshot, nous pouvons reproduire une expérience à partir d’un point intermédiaire.

Mais un snapshot incomplet peut donner une illusion de reprise.

Il doit donc préciser ce qu’il contient et ce qu’il ne contient pas.

---

## Une horloge sans mémoire

La source de ticks elle-même peut rester simple.

Elle n’a pas besoin de mémoriser tout le système.

Elle dit :

**tick n.**

Puis :

**tick n+1.**

Le registre, lui, conserve l’histoire.

Cette séparation évite de transformer l’horloge en intelligence centrale omnisciente.

Le temps coordonne.

Il ne pense pas.

---

## Une horloge centrale ou plusieurs horloges ?

Une architecture peut choisir une horloge centrale.

Tous les modules reçoivent le même tick.

Avantage :

la coordination est simple.

Risque :

la source centrale devient critique.

Une autre architecture peut utiliser plusieurs horloges locales.

Avantage :

autonomie.

Risque :

dérive et synchronisation.

Il n’existe pas une seule réponse correcte.

Le choix dépend du système.

---

## La dérive

Deux horloges réelles ne restent pas nécessairement parfaitement alignées.

Si :

[
t_A
]

et :

[
t_B
]

évoluent légèrement différemment, leur différence peut croître :

[
delta(t)
=
t_A - t_B
]

Cette dérive peut devenir importante sur une longue durée.

Alors les systèmes distribués ont besoin de mécanismes de synchronisation ou de tolérance.

---

## Le temps distribué est difficile

Lorsque plusieurs machines participent, il devient dangereux de croire qu’un timestamp suffit à établir un ordre absolu parfait.

Les horloges peuvent être désalignées.

Les messages peuvent arriver en retard.

Un événement envoyé avant un autre peut parfois être reçu après lui.

Cette réalité oblige à distinguer :

ordre d’émission;

ordre de réception;

ordre causal.

---

## Une séquence peut aider

Pour une source donnée, un numéro de séquence peut fournir un ordre robuste :

[
seq = 1,2,3,ldots
]

Même si les timestamps sont légèrement décalés, la séquence montre l’ordre produit par cette source.

Mais entre plusieurs sources, le problème revient.

L’architecture doit donc préciser ce qu’elle garantit réellement.

---

## Pas de faux temps absolu

Une interface qui affiche des timestamps à la microseconde donne une impression de précision.

Mais la précision d’affichage n’est pas la précision réelle de l’horloge.

Afficher :

[
12{:}00{:}00.123456
]

ne prouve pas une exactitude à la microseconde.

Il faut connaître :

résolution;

précision;

synchronisation;

source.

Encore une fois :

**nombre de décimales ≠ preuve de précision.**

---

## La résolution

Une horloge peut avoir une résolution :

[
r_t
]

C’est le plus petit intervalle qu’elle peut distinguer ou représenter utilement.

Une mesure de 1 ns n’a aucun sens si l’horloge ne résout que 1 ms.

Alors le système doit éviter d’ajouter des chiffres qui ne sont pas soutenus par la mesure.

---

## La précision temporelle

Nous pouvons distinguer :

résolution;

exactitude;

précision;

stabilité.

Ces concepts sont liés mais différents.

Une horloge peut être très stable mais décalée.

Une autre peut être exacte en moyenne mais jittery.

La métrique choisie doit correspondre à la question.

---

## Le temps comme budget

Chaque module peut recevoir un budget :

[
B_k
]

Il doit terminer avant :

[
R_k le B_k
]

La somme des budgets d’un chemin séquentiel peut fournir une estimation :

[
B_P
=
sum_k B_k
]

Mais pour des chemins parallèles, la durée globale dépend plutôt du maximum et des coûts de synchronisation.

L’architecture temporelle doit donc suivre la topologie réelle.

---

## Le budget du cycle

Si le tick cible possède une période :

[
T_{	ext{tick}}
]

nous pouvons répartir ce budget entre :

lecture;

calcul;

synchronisation;

écriture;

journalisation.

Par exemple :

[
T_{	ext{tick}}
=
T_{	ext{in}}
+
T_{	ext{compute}}
+
T_{	ext{sync}}
+
T_{	ext{out}}
+
T_{	ext{log}}
+
M
]

où (M) est la marge.

Cette décomposition transforme un problème vague de performance en mesures séparées.

---

## Le logging coûte du temps

La traçabilité n’est pas gratuite.

Écrire chaque événement sur disque peut ralentir le système.

Il faut donc concevoir la preuve elle aussi.

Possibilités :

buffer de logs;

écriture asynchrone;

échantillonnage;

niveaux de détail;

journal binaire;

agrégation.

Mais chaque optimisation doit préserver les preuves dont nous avons besoin.

---

## Observer peut perturber

Mesurer un système peut modifier légèrement son comportement.

Ajouter des logs.

Prendre des timestamps.

Tracer une courbe.

Profiler.

Tout cela consomme des ressources.

Cette réalité est importante.

Une mesure de performance doit idéalement indiquer si l’instrumentation était active.

Sinon nous comparons peut-être deux systèmes observés différemment.

---

## Mesure passive et mesure intrusive

Nous pouvons distinguer :

**MESURE PASSIVE**

et :

**MESURE INSTRUMENTÉE**

La première utilise des données déjà produites.

La seconde ajoute du travail afin d’observer.

Aucune n’est automatiquement meilleure.

Mais leur impact doit être connu.

---

## L’horloge du test

Chaque test temporel doit déclarer :

durée;

nombre de ticks;

fréquence cible;

source de temps;

charge;

matériel;

version;

conditions.

Dire simplement :

**ça tourne à 60 FPS**

est insuffisant pour une preuve complète.

Il faut savoir :

pendant combien de temps ?

avec quelle charge ?

quel percentile ?

quel minimum ?

quelles erreurs ?

---

## Une moyenne sur une seconde n’est pas une stabilité

Un système peut être parfait pendant une seconde et dériver après dix minutes.

Les tests doivent donc avoir plusieurs horizons.

Par exemple :

court;

moyen;

long.

Le choix dépend du phénomène.

Une fuite mémoire peut prendre du temps.

Une dérive d’horloge aussi.

---

## La stabilité temporelle

Nous pouvons définir une métrique candidate de stabilité.

Par exemple, pour une période cible (T), mesurer la proportion de ticks dans une tolérance :

[
S_T
=
rac{
#{n: |Delta t_n-T| le epsilon}
}{
N
}
]

Cette métrique n’est pas universelle.

Elle dépend de (epsilon).

Mais elle force à expliciter la tolérance.

---

## Une tolérance doit avoir une raison

Pourquoi :

[
epsilon = 1 	ext{ ms}
]

et pas :

[
5 	ext{ ms}
]

?

La réponse peut venir :

d’une exigence fonctionnelle;

d’une limite matérielle;

d’un besoin de synchronisation;

d’un protocole scientifique.

Si la tolérance est choisie après avoir vu les résultats, elle doit être signalée.

Sinon on risque d’ajuster le test pour faire passer le système.

---

## Le test avant la cible

La discipline du chapitre 11 revient.

Lorsque possible, les critères devraient être définis avant l’essai.

Par exemple :

**PASS si 99 % des ticks restent dans ±1 ms pendant 30 minutes.**

Puis on exécute.

Cela vaut davantage qu’un seuil inventé après observation.

Le système apprend à ne pas déplacer la ligne d’arrivée.

---

## Le temps et les erreurs

Une erreur peut elle-même être temporelle.

Timeout.

Deadline missed.

Tick skipped.

Clock drift.

Buffer overrun.

Stale data.

Out-of-order event.

Duplicate event.

Ces erreurs méritent des codes distincts.

Sinon toutes deviennent un vague :

**timing error.**

---

## STALE

Une donnée peut être valide mais trop vieille.

Nous pouvons définir :

[
age
=
t_{	ext{now}}
-
t_{	ext{source}}
]

Puis une limite :

[
age le A_{max}
]

Si la limite est dépassée :

[
status = STALE
]

La valeur peut rester numériquement correcte pour son époque.

Elle n’est simplement plus suffisamment fraîche pour l’usage courant.

---

## Le temps des erreurs humaines

L’opérateur lui aussi agit dans le temps.

Une commande peut être valable seulement dans un certain état.

Un GO donné trop tôt doit être refusé.

Nous pouvons imaginer :

[
GO
	ext{ accepté seulement si }
STATE = READY
]

et :

[
SYNC = PASS
]

et :

[
ERROR = NONE
]

Le contrôle temporel rejoint alors la sécurité.

---

## READY ne doit pas être décoratif

Un voyant READY doit correspondre à une condition calculable.

Par exemple :

[
READY
=
PORTS_VALID
land
CLOCK_LOCKED
land
STATE_VALID
land
NO_BLOCKING_ERROR
]

La formule exacte dépendra du système.

Mais le principe est puissant.

Le mot READY ne doit pas être une impression.

Il doit être une conclusion issue de conditions connues.

---

## La phase

Deux oscillations de même fréquence peuvent être décalées.

Pour un signal sinusoïdal :

[
x(t)
=
Asin(omega t+phi)
]

où :

- (A) est l’amplitude;
- (omega) la pulsation;
- (phi) la phase.

Deux signaux peuvent partager (A) et (omega) tout en ayant des phases différentes.

Alors :

**même fréquence ≠ même état instantané.**

Cette distinction devient essentielle lorsqu’on parle de synchronisation d’ondes.

---

## La pulsation

La relation classique est :

[
omega = 2pi f
]

où :

- (f) est la fréquence en hertz;
- (omega) est la pulsation en radians par seconde.

Cette relation ne doit pas être confondue avec une phase normalisée ou un angle particulier produit par une autre formule.

Les unités protègent encore une fois le sens.

---

## La phase normalisée

Une phase peut être exprimée sur un cycle :

[
	heta
=
2pi
rac{r}{N}
]

pour un indice (r) dans un cycle de longueur (N).

Cette construction est parfaitement valable comme paramétrisation angulaire.

Mais sa signification physique dépend de ce que (r) et (N) représentent.

Une formule angulaire peut être mathématiquement correcte sans représenter automatiquement une oscillation physique.

La Bible doit garder cette frontière visible.

---

## Le stéréo temporel

Lorsque deux canaux sont comparés, le temps peut devenir aussi important que leur amplitude.

Deux signaux identiques mais décalés :

[
x_L(t)
]

et :

[
x_R(t-delta)
]

peuvent produire une impression ou une interaction différente.

Le décalage :

[
delta
]

doit donc être mesuré si la relation temporelle entre les canaux est importante.

Le terme **stéréo** peut désigner deux voies.

Il ne donne pas à lui seul une signification scientifique au décalage observé.

---

## Le cœur écoute

Dans le langage Brutus, nous aimons parfois dire qu’un module « écoute ».

Techniquement, cela peut signifier :

il attend une entrée;

il échantillonne;

il souscrit à un événement;

il surveille un port;

il bloque jusqu’à réception.

Le mot humain peut rester dans le récit.

Le moteur doit savoir laquelle de ces opérations est réelle.

---

## Attendre n’est pas dormir

Un module peut attendre de plusieurs façons.

Boucle active.

Sleep.

Événement.

Interruption.

File bloquante.

Polling.

Ces choix ont des conséquences sur :

CPU;

latence;

jitter;

énergie;

complexité.

Alors même l’attente mérite une architecture.

---

## Le polling

Un module peut vérifier périodiquement :

**y a-t-il quelque chose ?**

Si la période de polling vaut :

[
T_p
]

la latence moyenne supplémentaire peut dépendre de ce choix.

Un polling trop lent augmente la latence.

Trop rapide gaspille des ressources.

La bonne valeur est un compromis mesurable.

---

## L’événementiel

Une architecture événementielle peut réveiller le consommateur seulement lorsqu’une donnée arrive.

Cela peut réduire le travail inutile.

Mais elle introduit d’autres questions :

ordre;

concurrence;

priorité;

réentrance;

backpressure.

Aucune architecture n’élimine la complexité.

Elle la déplace.

---

## Backpressure

Si un producteur génère plus vite que le consommateur ne traite :

[
R_{	ext{prod}}
>
R_{	ext{cons}}
]

le backlog augmente.

Sans mécanisme de contrôle, le buffer finit par grossir ou déborder.

La **backpressure** est une manière de faire remonter cette limite au producteur.

Le système peut ralentir, rejeter, compresser ou agréger.

Mais il ne doit pas prétendre que tout est traité si ce n’est pas le cas.

---

## Débit et cadence

Le débit peut être mesuré comme :

[
lambda
=
rac{N}{Delta t}
]

où (N) est le nombre d’événements traités pendant l’intervalle (Delta t).

Mais un débit élevé ne garantit pas une faible latence.

Un système peut traiter beaucoup d’événements en batch tout en répondant lentement à chacun.

Il faut donc distinguer :

**throughput**

et :

**latency**.

---

## Temps réel ne veut pas dire rapide

En informatique, un système temps réel se caractérise surtout par des contraintes temporelles garanties ou analysables.

Un système peut être extrêmement rapide sans être temps réel s’il ne garantit rien.

Et un système relativement lent peut être temps réel si sa deadline est large et respectée.

Ainsi :

**rapide ≠ temps réel.**

Cette distinction protège contre les mots impressionnants.

---

## Temps réel dur et souple

On distingue couramment des contraintes plus strictes ou plus tolérantes.

Dans un cadre **hard real-time**, manquer une deadline peut être considéré comme une défaillance critique.

Dans un cadre **soft real-time**, un dépassement occasionnel peut dégrader la qualité sans rendre le système incorrect au sens absolu.

Si Brutus utilise un jour ces termes, il devra déclarer la catégorie et les exigences exactes.

---

## La mélodie du système

À ce stade, la métaphore revient.

Un orchestre peut posséder tous ses instruments.

S’ils ne partagent aucun tempo ni aucune écoute, le résultat devient chaos.

Mais un bon chef ne joue pas chaque instrument.

Il donne des repères.

Le temps du système peut remplir une fonction semblable.

Pas une intelligence.

Pas une volonté.

Un cadre commun.

---

## Le chef ne doit pas cacher les retardataires

Si un chemin arrive tard, l’horloge ne doit pas simplement attendre silencieusement.

Elle doit permettre au registre de montrer :

qui;

combien;

à quel tick;

avec quel impact.

La synchronisation ne doit pas effacer la preuve du retard.

---

## La reine comme référence, pas comme vérité

Une horloge centrale peut devenir la référence temporelle du système.

Mais le mot **référence** est important.

Elle fournit un cadre.

Elle ne prouve pas que le monde extérieur suit exactement son rythme.

Une simulation peut être parfaitement synchronisée avec sa propre horloge et pourtant ne rien prédire correctement sur la réalité.

Le temps interne garantit de la cohérence.

Pas automatiquement de la validité externe.

---

## Le rythme interne et la réalité

Pour comparer un système simulé à un phénomène réel, il faut établir un mapping :

[
t_{	ext{sim}}
leftrightarrow
t_{	ext{physical}}
]

Ce mapping doit avoir une définition.

Par exemple :

1 tick = 1 ms physique.

Ou :

1000 ticks = 1 cycle expérimental.

Sans cette correspondance, le temps simulé reste une échelle interne.

Il peut être utile.

Mais il n’est pas encore une mesure du monde.

---

## Le temps comme unité

La seconde est une unité définie dans le Système international.

Lorsque Brutus utilise des secondes, millisecondes ou hertz dans un contexte physique, nous devons respecter cette définition et les conversions.

Lorsque nous utilisons un **tick Brutus**, il s’agit d’une unité logique interne tant qu’une conversion explicite vers la seconde n’est pas définie.

Cette distinction est capitale.

---

## Un tick n’est pas une seconde

Même si :

[
Delta t_{	ext{sim}} = 1
]

cela ne signifie pas :

[
1 	ext{ seconde}
]

à moins que l’unité ne soit explicitement donnée.

Une valeur sans unité est parfois une simple étape numérique.

La notation doit le dire.

---

## Le facteur d’échelle

Nous pouvons définir un facteur :

[
alpha
=
rac{
Delta t_{	ext{physical}}
}{
Delta t_{	ext{sim}}
}
]

si une correspondance existe.

Alors :

[
t_{	ext{physical}}
=
alpha t_{	ext{sim}}
]

dans un modèle linéaire simple.

Mais si la correspondance est non linéaire, il faudra une fonction plus générale.

Encore une fois, l’échelle doit être définie avant l’interprétation.

---

## Les cycles

Un système périodique peut avoir une période :

[
T_c
]

et une fréquence :

[
f_c
=
rac{1}{T_c}
]

Mais un cycle logique peut également être simplement une séquence d’états :

[
S_0
ightarrow
S_1
ightarrow
S_2
ightarrow
S_0
]

Dans ce cas, parler de fréquence physique n’a de sens que si chaque transition est liée au temps.

Un cycle de machine d’état n’est pas automatiquement une oscillation physique.

---

## Une période de neuf étapes

Supposons une machine :

[
S_n = n mod 9
]

Elle possède une période logique de 9 ticks.

Après neuf transitions, l’état se répète.

Cela signifie :

[
S_{n+9}=S_n
]

Cela ne signifie pas encore :

9 Hz.

Pour obtenir une fréquence physique, il faut connaître la durée d’un tick.

---

## Si le tick vaut (Delta t)

Alors la période temporelle du cycle vaut :

[
T = 9Delta t
]

et la fréquence :

[
f=rac{1}{9Delta t}
]

Voilà comment une structure discrète reçoit une unité physique.

La conversion est explicite.

Aucune magie n’est nécessaire.

---

## Perturbation temporelle

Nous pouvons ensuite perturber un cycle.

Ajouter un retard.

Sauter un tick.

Modifier la période.

Observer si le système revient à son régime.

Une expérience candidate peut mesurer :

temps de récupération;

phase résiduelle;

erreurs;

pertes d’événements.

Le temps devient alors un axe de stabilité.

---

## Retour à l’équilibre

Si une variable temporelle revient vers une valeur cible, nous pouvons mesurer une dynamique de relaxation.

Par exemple :

[
e_n
=
T_n-T^*
]

où (T^*) est la période cible.

Puis observer comment :

[
e_n ightarrow 0
]

Cette analyse peut utiliser des outils de contrôle ou de systèmes dynamiques.

Mais elle ne doit être introduite que lorsque les variables sont clairement définies.

---

## L’horloge peut elle-même être testée

La source de temps n’est pas sacrée.

Elle doit avoir ses tests.

Périodicité.

Jitter.

Dérive.

Monotonicité.

Perte de tick.

Double tick.

Pause.

Reprise.

Reset.

Long run.

Chaque test produit une preuve locale.

---

## Monotonicité

Pour une horloge logique normale :

[
n_{k+1} > n_k
]

Pour une horloge monotone réelle :

[
t_{k+1}ge t_k
]

Si le temps recule sans événement explicite de restauration, quelque chose ne va pas.

Cette propriété peut être testée automatiquement.

---

## Continuité après redémarrage

Que se passe-t-il après un restart ?

Le tick repart-il à zéro ?

Continue-t-il ?

Charge-t-il un checkpoint ?

Toutes les réponses sont possibles.

Mais elles doivent être déterminées.

On peut par exemple conserver :

[
session_id
]

et :

[
tick
]

Ainsi, deux ticks 42 appartenant à deux sessions différentes ne sont pas confondus.

---

## Identité temporelle complète

Un événement peut être identifié par :

[
EID = (session,tick,sequence)
]

Ce triplet réduit les ambiguïtés.

Il permet de distinguer :

même tick;

événements multiples;

sessions différentes.

Selon les besoins, un UUID ou un hash peut compléter l’identité.

---

## Le hash n’est pas une horloge

Un hash peut certifier qu’un contenu n’a pas changé.

Il ne prouve pas à lui seul l’ordre temporel absolu de deux événements.

Pour établir une chronologie, il faut des métadonnées ou un mécanisme d’ordonnancement supplémentaire.

Chaque outil doit être utilisé pour ce qu’il prouve réellement.

---

## La provenance temporelle

Une trace scientifique utile doit idéalement dire :

quand l’événement a été généré;

quand il a été enregistré;

par quelle horloge;

avec quelle résolution;

dans quelle session.

Cela paraît excessif pour une petite expérience.

Mais dans un système distribué, ces informations peuvent devenir décisives.

---

## Le temps humain

Il existe aussi le temps du projet.

Une idée aujourd’hui.

Une correction demain.

Une version la semaine suivante.

Cette chronologie n’utilise pas nécessairement les ticks du moteur.

Elle utilise :

dates;

commits;

releases;

versions;

journaux.

Mais le principe est identique :

**savoir ce qui venait avant quoi.**

La continuité technique et la continuité historique partagent la même discipline.

---

## Une version est un repère temporel

Quand nous écrivons :

**v1**

nous disons implicitement :

il existe un avant et peut-être un après.

La version transforme un objet en partie d’une histoire.

Elle permet de comparer.

Et surtout, elle empêche un changement silencieux.

---

## Le temps protège la preuve

Un résultat sans date peut être difficile à replacer.

Un résultat sans version peut être impossible à reproduire.

Un résultat sans ordre d’événements peut être impossible à expliquer.

Ainsi, le temps n’est pas seulement une dimension de calcul.

Il est une dimension de preuve.

---

## L’Horloge de la vie comme registre de continuité

Nous pouvons maintenant donner une interprétation architecturale sobre à cette expression.

**CANDIDAT :**

L’Horloge de la vie est le mécanisme qui fournit ou référence le rythme logique du système, attribue des repères temporels aux événements et permet de relier les états successifs sans décider à la place des modules.

Cette définition est volontairement limitée.

Elle ne prétend pas que l’horloge est vivante.

Elle dit qu’elle décrit le battement de ce qui évolue.

---

## Pourquoi garder le mot « vie » ?

Parce que le langage d’un projet peut porter une histoire.

Un cœur.

Une reine.

Une vie.

Ces mots peuvent aider à visualiser.

Mais le canon doit toujours montrer leur traduction technique.

Ainsi, nous pouvons conserver la poésie sans sacrifier la précision.

La Bible Brutus n’a pas besoin de choisir entre les deux.

Elle doit seulement savoir les distinguer.

---

## Un battement sans conscience

Une horloge peut battre sans penser.

Un cristal peut osciller sans vouloir.

Un serveur peut répondre sans ressentir.

Un module peut maintenir un état sans posséder une conscience.

Cette distinction protège l’architecture contre les projections trop rapides.

Le comportement observable vient d’abord.

L’interprétation vient après.

---

## Le test minimal du chapitre 13

Le premier prototype temporel peut être extrêmement petit.

Une source de tick.

Un module B1.

Un log.

À chaque tick :

1. générer (n);
2. enregistrer (t_{	ext{source}});
3. envoyer à B1;
4. mesurer (t_{	ext{receive}});
5. exécuter;
6. enregistrer (t_{	ext{end}});
7. produire la sortie;
8. calculer la latence.

C’est déjà suffisant pour tester le battement.

---

## Les métriques minimales

Pour une fenêtre de (N) ticks :

[
F_{	ext{rt}}
=
rac{N}{t_N-t_0}
]

comme fréquence réalisée sur la fenêtre.

[
R_{	ext{exec}}
]

comme durée d’exécution d’un cycle, selon définition.

[
Delta t_n
]

comme intervalle entre ticks.

Puis :

minimum;

maximum;

moyenne;

dispersion.

Ces métriques donnent un premier portrait.

---

## La fréquence réalisée

Le terme :

[
F_{	ext{rt}}
]

peut être utilisé comme notation de travail pour une fréquence réalisée.

Mais la notation n’est pas universelle.

Elle doit donc être définie dans chaque artefact.

Même une abréviation familière ne doit pas devenir mystérieuse.

---

## Comparer consigne et réalité

Nous pouvons conserver côte à côte :

[
F_{	ext{target}}
]

et :

[
F_{	ext{rt}}
]

Puis calculer une erreur relative :

[
e_f
=
rac{
F_{	ext{rt}}-F_{	ext{target}}
}{
F_{	ext{target}}
}
]

si :

[
F_{	ext{target}}
eq 0
]

Cette erreur peut être exprimée en pourcentage :

[
100e_f
]

La formule est simple.

Elle évite les impressions.

---

## Un tableau honnête

Une télémétrie temporelle utile pourrait afficher :

**TICK**

**dt_sim**

**R_exec**

**F_target**

**F_rt**

**JITTER**

**LAG**

**DROPPED**

**STATE**

**ERROR**

Chaque valeur doit pointer vers une définition.

Sinon le tableau devient un décor scientifique.

---

## La fréquence d’affichage doit être étiquetée

Si l’interface affiche 60 FPS, cela décrit la couche graphique.

Il ne faut pas laisser croire que le moteur scientifique fonctionne à 60 Hz simplement parce que l’écran le fait.

Nous pouvons afficher :

**UI FPS**

séparément de :

**ENGINE RATE**

et :

**SIM RATE**

Cette petite séparation évite une grande confusion.

---

## La preuve d’autorité

La valeur affichée doit venir de la bonne source.

Le moteur mesure son rythme.

L’interface reçoit la mesure.

Elle ne la déduit pas uniquement du nombre de frames qu’elle dessine.

Ainsi :

[
SOURCE_{	ext{ENGINE}}
ightarrow
TELEMETRY
ightarrow
UI
]

Le visuel devient un témoin.

Pas le juge.

---

## Le serveur et le temps

Dans une architecture distribuée, un serveur peut devenir l’autorité d’état.

Cela ne signifie pas nécessairement qu’il doit être l’unique source d’horloge.

Mais si le serveur décide quel état est canonique, les événements doivent pouvoir être ordonnés du point de vue de cette autorité.

La notion d’**authority** doit donc elle aussi être définie précisément.

---

## Le client peut être en avance visuellement

Pour donner une impression fluide, une interface peut interpoler ou prédire.

C’est acceptable si le système sait distinguer :

**état confirmé**

et :

**état prédit**.

Sinon une animation peut sembler montrer la réalité alors qu’elle montre une anticipation.

La vérité d’affichage doit porter son statut.

---

## Confirmé et prédit

Nous pouvons utiliser :

[
CONFIRMED
]

et :

[
PREDICTED
]

Une valeur prédite peut être utile.

Mais elle ne doit pas être sauvegardée comme mesure confirmée sans transition explicite.

Le temps devient encore une frontière de preuve.

---

## Reconciliation

Lorsque l’état confirmé arrive, le client peut comparer :

[
S_{	ext{pred}}
]

et :

[
S_{	ext{confirmed}}
]

Puis corriger.

Cette correction doit être observable si elle influence l’expérience.

Sinon le visuel peut masquer les écarts entre modèle local et autorité réelle.

---

## Le battement et la mémoire

Un système dynamique ne peut pas conserver seulement des valeurs.

Il doit savoir **quand** elles étaient vraies.

La mémoire devient donc une suite :

[
(S_0,t_0),
(S_1,t_1),
ldots,
(S_n,t_n)
]

C’est une trajectoire.

La prochaine étape naturelle sera d’explorer ce que signifie conserver cette trajectoire sans tout garder éternellement.

---

## Tout conserver est impossible à grande échelle

Un système qui produit des milliers d’événements par seconde accumule rapidement des données.

Alors il faut choisir :

logs bruts;

agrégats;

snapshots;

compression;

rétention limitée;

archives.

Ces décisions appartiennent à la mémoire et à la continuité.

Le chapitre suivant pourra les approfondir.

---

## Mais ne pas conserver assez détruit la preuve

L’autre extrême est tout aussi dangereux.

Si seuls les derniers états survivent, un bug ancien devient impossible à reconstruire.

La bonne architecture devra trouver un équilibre.

Ce n’est pas une question purement technique.

C’est une question de ce que nous voulons être capables de prouver.

---

## Une horloge ouvre donc la mémoire

Le temps crée naturellement une séquence.

La séquence crée naturellement une histoire.

L’histoire crée naturellement un besoin de mémoire.

Voilà pourquoi le chapitre 13 ne peut pas se terminer seulement avec des hertz.

Son vrai résultat est plus profond :

dès qu’un système possède un battement, il commence à accumuler un passé.

---

## Le passé du système

Avant le premier tick, il n’y a qu’un état initial.

Après mille ticks, il y a une trajectoire.

Après un million, il y a une histoire.

La mémoire devient le moyen de ne pas perdre cette histoire.

Mais elle doit rester technique.

Traçable.

Versionnée.

Interrogeable.

Pas mystique.

---

## La dernière question

Nous savons maintenant :

qui parle à qui;

quand les événements se produisent;

comment mesurer le rythme;

comment détecter les retards;

comment séparer temps réel, simulé et observé;

comment synchroniser plusieurs chemins;

comment donner une phase à un signal;

comment enregistrer une trajectoire.

Il reste une question.

**Que doit-on garder ?**

Tout ?

Seulement les erreurs ?

Les états clés ?

Les entrées ?

Les sorties ?

Les changements ?

Les snapshots ?

Cette question appartient au prochain chapitre.

---

## Le battement n’est pas la vie

Il faut terminer avec cette précision.

Un système qui possède un rythme n’est pas vivant pour autant.

Une horloge bat.

Un oscillateur oscille.

Un programme boucle.

Ces comportements ne suffisent pas à établir une propriété biologique ou consciente.

Mais, architecturalement, le battement produit quelque chose d’essentiel :

un avant;

un après;

une cadence;

une histoire.

Et cette histoire peut être mesurée.

---

## Dernière image

Nous regardons maintenant le même schéma qu’au chapitre précédent.

B1.

B2.

B3.

Quatre chemins.

Une jonction.

Mais quelque chose a changé.

Les lignes ne sont plus figées.

Un tick part.

Les modules reçoivent.

Les chemins travaillent.

La jonction attend.

Un retard apparaît.

Une erreur se lève.

Le cycle se ferme.

Puis un autre commence.

Le système n’est pas devenu vivant.

Il est devenu **temporel**.

Il possède enfin un battement que l’on peut mesurer au lieu de l’imaginer.

Et à chaque battement, quelque chose s’accumule derrière lui.

Une trace.

Un état.

Un passé.

Le prochain chapitre devra décider comment ne pas le perdre.

# **LE TEMPS PASSE. LA MÉMOIRE COMMENCE.**
