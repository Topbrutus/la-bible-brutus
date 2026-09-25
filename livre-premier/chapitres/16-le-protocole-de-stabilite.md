# Chapitre 16 — Le Protocole de Stabilité

**APRÈS L’INTRODUCTION — SIXIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** Tenir, revenir, résister  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Un système n’est pas stable parce qu’il fonctionne aujourd’hui.  
> Il est stable lorsque son comportement reste acceptable sous des conditions définies, pendant un temps défini, malgré des perturbations définies.**

---

## La cicatrice reste. La stabilité doit maintenant être prouvée.

Le chapitre 15 nous a appris à réparer.

Détecter.

Isoler.

Restaurer.

Vérifier.

Conserver la cicatrice.

Mais une nouvelle question apparaît aussitôt.

Si un système casse toutes les dix minutes puis se répare parfaitement, pouvons-nous l’appeler stable ?

Non.

Il est peut-être récupérable.

Peut-être résilient dans une certaine mesure.

Mais pas nécessairement stable.

La stabilité demande autre chose.

Elle demande de regarder le comportement dans le temps.

Sous contrainte.

Sous perturbation.

Et surtout :

avec des critères définis avant de regarder le résultat.

---

## Le mot stable est trop facile

Dans le langage courant, nous disons facilement :

**ça a l’air stable.**

**ça ne bouge pas beaucoup.**

**ça roule bien.**

**ça tient.**

Ces phrases peuvent être utiles dans une conversation.

Elles ne suffisent pas pour une preuve.

Un système peut sembler calme pendant trente secondes et dériver après trois heures.

Il peut rester parfaitement constant parce qu’il est bloqué.

Il peut produire une sortie lisse mais fausse.

Il peut ne jamais planter et accumuler pourtant une erreur lente.

Alors le mot **stable** doit recevoir une définition locale.

---

## Stabilité n’est pas immobilité

Un système dynamique peut être stable tout en bougeant.

Une oscillation périodique peut être stable.

Une trajectoire peut être stable.

Un contrôleur peut suivre une consigne variable tout en restant stable.

L’absence de mouvement n’est donc pas le critère.

La vraie question est :

**le comportement reste-t-il dans les limites attendues, ou revient-il vers elles après perturbation ?**

---

## État de référence

Toute expérience de stabilité commence avec un état de référence.

Appelons-le :

[
S^*
]

Cet état peut être :

un point fixe;

un cycle;

une distribution;

une plage admissible;

un régime nominal.

Il faut définir ce qui constitue la référence.

Sinon nous ne savons pas ce que signifie « revenir ».

---

## Point fixe

Pour un système discret :

[
S_{n+1}=F(S_n)
]

un point fixe (S^*) satisfait :

[
F(S^*)=S^*
]

Cela signifie qu’une fois dans cet état, le système y reste selon le modèle.

Mais beaucoup de systèmes ne cherchent pas un point fixe.

Ils cherchent un comportement périodique ou une plage.

Le protocole doit donc choisir la bonne notion.

---

## Cycle stable

Pour un cycle de période (p) :

[
S_{n+p}=S_n
]

le régime de référence n’est pas une seule valeur.

C’est une orbite.

Une perturbation peut décaler la phase sans détruire le cycle.

Alors la mesure de stabilité doit prendre cette structure en compte.

---

## Bande admissible

Dans un système réel, viser une valeur exacte peut être inutile.

Nous pouvons définir une bande :

[
|x-x^*|le epsilon
]

où :

- (x^*) = valeur cible;
- (epsilon) = tolérance.

Le système peut être considéré dans sa zone nominale tant qu’il reste dans cette bande.

Mais (epsilon) doit avoir une raison.

Pas être choisi après coup pour faire passer le test.

---

## La perturbation

Une stabilité sans perturbation dit peu de choses.

Il faut introduire une perturbation :

[
d(t)
]

ou, en discret :

[
d_n
]

Elle peut être :

une variation d’entrée;

un retard;

une perte de tick;

un bruit;

une panne de chemin;

une variation de charge;

une modification contrôlée de paramètre;

un restart;

une impulsion.

Le type de perturbation doit être défini.

---

## Une perturbation doit avoir une amplitude

Dire :

**on l’a perturbé**

est insuffisant.

Il faut savoir de combien.

Par exemple :

[
d = +10%
]

ou :

[
d = 50 	ext{ ms de retard}
]

ou :

[
P_3 = OFF 	ext{ pendant } 5 	ext{ s}
]

Sans amplitude, deux tests ne sont pas comparables.

---

## Une perturbation doit avoir une durée

Certaines perturbations sont impulsives.

D’autres persistent.

Une surcharge de 100 ms n’est pas la même chose qu’une surcharge de 10 minutes.

Nous devons donc enregistrer :

[
T_d
]

la durée de perturbation.

---

## Une perturbation doit avoir un moment

Le système peut réagir différemment selon son état.

Une perturbation au démarrage n’est pas nécessairement équivalente à la même perturbation après une heure.

Alors le protocole doit préciser :

tick;

temps;

phase du cycle;

état.

Le contexte est une partie de la perturbation.

---

## Réponse du système

Après perturbation, nous observons une réponse :

[
y(t)
]

ou :

[
y_n
]

Nous pouvons comparer cette réponse à la référence :

[
e(t)=y(t)-y^*
]

ou :

[
e_n=y_n-y^*
]

L’erreur devient une variable mesurable.

---

## Amplitude maximale

Une première métrique peut être :

[
E_{max}
=
max_t |e(t)|
]

Elle répond :

**jusqu’où le système s’est-il écarté ?**

Deux systèmes peuvent revenir aussi vite mais l’un peut faire une excursion beaucoup plus grande.

Cette différence peut être importante.

---

## Temps de retour

Nous pouvons définir un temps de récupération :

[
T_r
]

comme le temps nécessaire pour revenir dans une bande définie autour de la référence.

Par exemple :

[
|e(t)|le epsilon
]

et y rester pendant une durée minimale.

La dernière condition est importante.

Sinon un système peut traverser brièvement la bande puis repartir.

---

## Settling time

En contrôle, on parle souvent de **settling time** pour le temps nécessaire à rester ensuite dans une bande autour de la valeur finale.

La définition précise dépend de la bande choisie.

La Bible ne doit pas utiliser ce terme sans préciser :

quelle bande;

quelle variable;

quelle durée de maintien.

---

## Dépassement

Une réponse peut dépasser la cible.

Nous pouvons mesurer un overshoot :

[
M_p
=
rac{y_{max}-y^*}{|y^*|}
]

lorsque cette définition est pertinente et que (y^*
eq0).

Mais le sens doit être adapté au système.

Un dépassement peut être tolérable.

Ou critique.

---

## Oscillation

Après perturbation, le système peut osciller autour de la référence.

La question devient :

l’amplitude diminue-t-elle ?

reste-t-elle constante ?

augmente-t-elle ?

Si l’amplitude augmente, l’instabilité est évidente.

Si elle diminue, le système peut converger.

Si elle reste constante, il peut avoir un régime oscillatoire persistant.

---

## Convergence

Une notion simple :

[
lim_{n	oinfty} e_n = 0
]

signifie que l’erreur converge vers zéro.

Mais tous les systèmes stables n’ont pas besoin de converger exactement vers zéro.

Ils peuvent converger vers une bande.

Ou vers une distribution.

Ou vers un cycle.

Le protocole doit définir le comportement attendu.

---

## Stabilité de Lyapunov

Pour certains systèmes dynamiques, la stabilité peut être étudiée avec la théorie de Lyapunov.

L’idée générale est qu’un petit écart initial reste petit.

Formellement, autour d’un équilibre, une notion classique impose que pour toute tolérance (epsilon>0), il existe un (delta>0) tel que :

[
|x(0)-x^*|<delta
]

implique :

[
|x(t)-x^*|<epsilon
]

pour tout (tge0).

Cette définition est mathématique.

Elle ne doit être appliquée que si le modèle satisfait les conditions nécessaires.

---

## Stabilité asymptotique

Une notion plus forte ajoute :

[
x(t)ightarrow x^*
]

lorsque :

[
tightarrowinfty
]

Le système ne reste pas seulement proche.

Il revient vers l’équilibre.

Encore une fois, cela concerne un cadre mathématique précis.

Un dashboard ne doit pas afficher « asymptotiquement stable » uniquement parce qu’une courbe semble descendre.

---

## Fonction de Lyapunov

Une fonction candidate :

[
V(x)
]

peut aider à prouver la stabilité si elle respecte certaines propriétés.

Par exemple, autour de l’équilibre :

[
V(x)>0
]

pour (x
eq x^*),

[
V(x^*)=0
]

et :

[
dot V(x)le0
]

dans un cadre continu adapté.

Mais cette méthode exige une vraie dérivation.

Le mot Lyapunov ne doit pas devenir un décor scientifique.

---

## Stabilité empirique

Lorsque nous n’avons pas de preuve analytique, nous pouvons mesurer une stabilité expérimentale.

C’est un statut différent.

Nous pouvons dire :

**stable dans ce protocole, sous ces perturbations, pendant cette durée.**

C’est une affirmation limitée.

Mais très utile.

---

## Ne jamais généraliser au-delà du test

Supposons qu’un système résiste à :

10 % de bruit pendant 30 minutes.

Nous ne pouvons pas conclure :

**le système est stable dans toutes les conditions.**

Nous pouvons conclure :

**dans ce protocole précis, aucun échec n’a été observé sous cette perturbation.**

La limite fait partie du résultat.

---

## Protocole minimal

Nous pouvons définir :

### Référence
(S^*)

### Perturbation
(d)

### Amplitude
(A_d)

### Durée
(T_d)

### Métriques
(M)

### Tolérances
(epsilon)

### Fenêtre d’observation
(T_o)

### Condition de retour
(C_r)

### Condition d’échec
(C_f)

Voilà la structure minimale.

---

## Condition PASS

Une condition candidate :

[
PASS
=
(E_{max}le E_{	ext{allowed}})
land
(T_rle T_{max})
land
(NO_CRITICAL_ERROR)
]

Cette formule est un exemple.

Le vrai protocole doit choisir les métriques pertinentes.

Le mot PASS doit toujours pointer vers une condition explicite.

---

## Condition FAIL

Une condition d’échec peut être :

invariant violé;

sortie hors domaine;

temps de retour dépassé;

perte de données;

crash;

désynchronisation persistante;

écart supérieur au seuil.

L’échec doit être défini avant le test.

---

## Le seuil n’est pas la vérité

Un seuil est une décision de protocole.

Si :

[
E_{max}le0.05
]

est acceptable, cela vient d’un besoin.

Pas d’une loi naturelle sauf contexte particulier.

Le rapport doit distinguer :

mesure;

seuil;

verdict.

---

## Mesure, seuil, verdict

Nous pouvons écrire :

[
M = 0.041
]

[
T = 0.050
]

donc :

[
M < T
]

et le protocole dit :

[
PASS
]

Le verdict vient de la comparaison.

Il ne doit pas être confondu avec la mesure brute.

---

## Stabilité et précision

Un système peut être stable mais imprécis.

Supposons qu’il produit toujours :

[
9.5
]

alors que la vraie cible est :

[
10
]

Il est peut-être très stable autour de 9.5.

Mais biaisé.

Ainsi :

[
STABILITY

eq
ACCURACY
]

Cette distinction est capitale.

---

## Stabilité et répétabilité

Un système peut être répétable sans être stable sous perturbation.

Répétabilité :

mêmes conditions → résultats proches.

Stabilité :

perturbation → comportement reste acceptable ou revient.

Les deux propriétés sont différentes.

---

## Stabilité et robustesse

Le mot **robustesse** désigne généralement la capacité à conserver des performances malgré des variations, incertitudes ou perturbations.

Nous pouvons voir la stabilité comme une propriété du comportement dynamique.

La robustesse demande :

**la stabilité et les performances survivent-elles lorsque le modèle ou les conditions varient ?**

---

## Robustesse

Une expérience de robustesse peut faire varier un paramètre :

[
	heta
in
[	heta_{min},	heta_{max}]
]

et vérifier le protocole sur plusieurs valeurs.

Le résultat devient une région de fonctionnement.

Pas un seul point.

---

## Domaine de robustesse

Nous pouvons définir un ensemble :

[
Omega
=
{	heta : PASS(	heta)=TRUE}
]

Ce domaine indique où le système satisfait les critères.

Il peut être beaucoup plus informatif qu’une seule exécution.

---

## Résilience

La résilience concerne davantage la capacité à absorber un incident, récupérer et continuer.

Un système peut être stable en nominal mais peu résilient à une panne sévère.

Un autre peut être instable sous certaines petites perturbations mais très bon en récupération de crash.

Encore une fois :

**stable ≠ robuste ≠ résilient.**

---

## Fiabilité

La fiabilité ajoute une dimension probabiliste ou statistique :

à quelle fréquence le système fonctionne-t-il correctement pendant une durée donnée ?

Cela peut conduire à des mesures comme :

temps moyen entre pannes;

taux de panne;

probabilité de succès.

Mais ces mesures demandent beaucoup de données et des hypothèses.

Nous ne devons pas les improviser.

---

## Disponibilité

La disponibilité peut être estimée conceptuellement comme une proportion de temps où le service est utilisable.

Mais :

disponible ≠ correct.

Un système peut répondre 100 % du temps et être faux.

L’intégrité doit rester séparée.

---

## Le protocole doit choisir ce qu’il mesure

Un seul mot « stabilité » peut cacher plusieurs dimensions :

valeur;

temps;

phase;

synchronisation;

mémoire;

débit;

erreur;

consommation;

température;

état.

Le test doit nommer la variable.

Sinon le verdict devient vague.

---

## Stabilité de valeur

Nous pouvons mesurer la dispersion :

[
sigma_x
]

ou l’écart maximal :

[
max|x_n-x^*|
]

pendant une période nominale.

Cela mesure la stabilité d’une variable.

Pas nécessairement celle de tout le système.

---

## Stabilité temporelle

Nous pouvons mesurer :

jitter;

dérive;

ticks perdus;

latence;

deadline misses.

Un système peut être stable numériquement mais instable temporellement.

---

## Stabilité de phase

Pour deux signaux :

[
Deltaphi(t)
=
phi_1(t)-phi_2(t)
]

Nous pouvons observer si :

[
Deltaphi(t)
]

reste borné, dérive ou converge.

Mais cette analyse suppose une définition rigoureuse de phase.

---

## Stabilité des quatre chemins

Nos quatre chemins peuvent être analysés séparément.

Pour chacun :

[
P_k
]

nous pouvons mesurer :

latence;

erreur;

état;

taux d’échec;

temps de retour.

Puis analyser la jonction.

Une stabilité globale peut cacher un chemin fragile compensé par les autres.

---

## Le chemin fragile

Supposons que trois chemins soient robustes et un quatrième oscille souvent.

La sortie globale peut rester acceptable pendant un certain temps.

Mais la marge de sécurité est réduite.

Le système doit donc exposer la santé locale, pas seulement la sortie finale.

---

## Marge

Une architecture stable exactement à la limite peut être fragile.

Nous voulons connaître la distance au seuil.

Si le critère est :

[
x le x_{max}
]

la marge peut être :

[
M = x_{max}-x
]

Une petite marge signifie qu’une faible variation supplémentaire peut produire un échec.

---

## Marge de stabilité

En contrôle, certaines notions plus spécifiques de marges de gain ou de phase existent pour les systèmes linéaires en fréquence.

Si nous les utilisons un jour, elles devront être calculées selon les modèles appropriés.

Pour le moment, retenons l’idée générale :

**PASS avec grande marge n’est pas la même chose que PASS juste au seuil.**

---

## Bruit

Un système réel reçoit souvent du bruit.

Nous pouvons modéliser :

[
x_{	ext{obs}} = x + eta
]

où (eta) est un terme de bruit.

Le protocole peut faire varier l’amplitude ou la distribution du bruit.

Mais le bruit doit être défini.

**bruit aléatoire** sans seed ni distribution est difficile à reproduire.

---

## Seed

Pour un test pseudo-aléatoire :

[
seed=s
]

permet de rejouer la même séquence.

Cela transforme un test « aléatoire » en expérience reproductible.

Nous pouvons ensuite changer le seed pour explorer plusieurs scénarios.

---

## Monte Carlo

Lorsque l’incertitude est importante, des simulations répétées peuvent explorer une distribution de résultats.

Pour (N) essais :

[
{Y_1,ldots,Y_N}
]

nous pouvons estimer :

moyenne;

variance;

quantiles;

taux d’échec.

Mais la qualité de l’analyse dépend du modèle et de l’échantillonnage.

Le nombre d’essais seul ne garantit pas la validité.

---

## Perturbation déterministe

Une perturbation fixe est souvent utile au début.

Par exemple :

[
d(t)
=
egin{cases}
0 & t<t_0\
A & t_0le t<t_0+T_d\
0 & tge t_0+T_d
end{cases}
]

Elle est simple.

Reproductible.

Facile à comparer.

Nous pouvons commencer petit avant d’ajouter de l’aléatoire.

---

## Impulsion

Une impulsion courte permet de mesurer une réponse transitoire.

Elle peut révéler :

oscillation;

overshoot;

retard;

temps de retour.

C’est un bon outil de caractérisation.

---

## Échelon

Une perturbation de type échelon modifie une entrée puis maintient la nouvelle valeur.

Elle permet d’observer un nouveau régime.

Dans un système de contrôle, la réponse à échelon est un outil classique.

Mais son interprétation dépend du modèle.

---

## Rampe

Une entrée qui augmente progressivement :

[
r(t)=at
]

permet de voir si le système suit une variation continue.

Les erreurs peuvent apparaître différemment qu’avec un saut brutal.

---

## Perturbation structurelle

Toutes les perturbations ne sont pas numériques.

Nous pouvons couper un chemin :

[
P_3 = OFF
]

changer une topologie;

retirer un module;

changer une version.

La stabilité architecturale peut alors être testée.

---

## Perturbation de charge

Nous pouvons augmenter le nombre d’événements :

[
lambda
]

jusqu’à observer :

latence;

backlog;

drops;

timeouts.

Le système peut être stable à faible charge et s’effondrer au-delà d’un seuil.

---

## Point de saturation

Il peut exister :

[
lambda^*
]

au-delà duquel le système ne maintient plus les critères.

Ce point est précieux.

Il décrit une limite opérationnelle.

La bonne documentation ne cache pas cette limite.

---

## Courbe de dégradation

Au lieu d’un simple PASS/FAIL, nous pouvons mesurer comment les performances se dégradent avec la charge.

[
M(lambda)
]

La forme de cette courbe révèle :

dégradation douce;

seuil brutal;

instabilité;

saturation.

---

## Hystérésis

Certains systèmes ne reviennent pas exactement par le même chemin lorsque la perturbation diminue.

Le comportement peut dépendre de l’histoire.

C’est une forme d’hystérésis.

Si elle existe, un test qui augmente puis diminue la charge peut révéler une différence.

La mémoire du système devient alors directement liée à sa stabilité.

---

## Stabilité et état

Un système avec mémoire peut posséder plusieurs attracteurs ou régimes.

La même entrée peut conduire à des résultats différents selon l’état initial.

Alors chaque test doit préciser :

[
S_0
]

Sinon deux essais ne sont pas comparables.

---

## Attracteur

En systèmes dynamiques, un attracteur décrit grossièrement un ensemble vers lequel certaines trajectoires évoluent.

Cela peut être :

point fixe;

cycle limite;

structure plus complexe.

Mais le mot doit être utilisé avec rigueur.

Une forme visuelle attrayante dans un graphe n’est pas automatiquement un attracteur mathématique démontré.

---

## Bassin d’attraction

Pour un attracteur, le bassin d’attraction est l’ensemble des états initiaux menant vers lui.

Cette idée peut devenir très utile pour Brutus.

Au lieu de tester une seule perturbation, nous pouvons explorer :

**depuis quelles régions le système revient-il ?**

---

## Carte de stabilité

Nous pouvons imaginer une grille de paramètres.

Pour chaque point :

PASS ou FAIL.

Puis cartographier :

[
Omega_{	ext{stable}}
]

la région où le protocole passe.

Cette carte est plus informative qu’un test unique.

---

## Frontière

La frontière entre PASS et FAIL peut révéler les limites du système.

Mais il faut faire attention à la résolution de la grille.

Une frontière apparente peut changer si nous testons plus finement.

Le résultat doit donc inclure la méthode d’échantillonnage.

---

## Le test de durée

Certaines instabilités apparaissent lentement.

Drift.

Fuite mémoire.

Accumulation d’erreurs.

Désynchronisation progressive.

Le protocole doit donc inclure des runs longs.

---

## Dérive

Définissons une variable :

[
x(t)
]

et une référence (x^*).

La dérive peut être étudiée via :

[
d(t)=x(t)-x^*
]

ou par une pente estimée.

Une petite dérive continue peut devenir grave avec le temps.

---

## Drift linéaire

Si approximativement :

[
d(t)approx at+b
]

alors (a) donne un taux de dérive.

Mais une dérive réelle peut être non linéaire.

La régression linéaire n’est qu’un modèle.

Le rapport doit le dire.

---

## Dérive de phase

Pour une horloge ou oscillation :

[
Deltaphi(t)
]

peut croître même si la fréquence instantanée semble proche.

Une petite erreur de fréquence accumulée devient un grand décalage de phase.

Le long terme révèle ce que le court terme cache.

---

## Mémoire et fuite

Une fuite mémoire peut être modélisée par une croissance de l’utilisation mémoire :

[
M(t)
]

Si elle augmente sans se stabiliser sous charge constante, il peut y avoir un problème.

Mais il faut distinguer :

cache légitime;

allocation différée;

garbage collection;

vraie fuite.

La courbe seule ne donne pas toujours la cause.

---

## Plateau

Un système peut augmenter sa mémoire puis atteindre un plateau stable.

C’est différent d’une croissance non bornée.

Le protocole doit donc observer assez longtemps pour distinguer les deux.

---

## Test restart

La stabilité doit survivre, si le contrat le prévoit, à un restart.

Après redémarrage :

état restauré;

ticks cohérents;

pas de duplication;

pas de perte au-delà du RPO;

services READY.

La reprise est une perturbation contrôlée.

---

## Test de persistance

Écrire.

Arrêter.

Redémarrer.

Relire.

Comparer.

C’est un test simple mais fondamental.

La stabilité de l’état durable est aussi importante que celle du runtime.

---

## Test de concurrence

Lorsque plusieurs actions arrivent en même temps, des races peuvent apparaître.

Nous pouvons créer des scénarios concurrents reproductibles autant que possible.

Le système peut sembler stable en séquentiel et casser sous concurrence.

---

## Race condition

Une race condition apparaît lorsque le résultat dépend de l’ordre relatif d’événements concurrents non correctement synchronisés.

Ces bugs sont parfois difficiles à reproduire.

Le registre de ticks, séquences et événements devient alors précieux.

---

## Deadlock

Deux composants peuvent attendre mutuellement.

Le système ne plante pas nécessairement.

Il se fige.

Une stabilité basée seulement sur « aucun crash » manquerait ce problème.

Nous devons mesurer le progrès.

---

## Liveness

Une propriété de liveness peut signifier :

**quelque chose de bon finit par se produire.**

Dans notre contexte :

les ticks continuent;

les files se vident;

les requêtes terminent;

la jonction produit.

Le système peut être techniquement vivant au niveau processus mais mort fonctionnellement.

---

## Progress metric

Nous pouvons définir une métrique de progrès :

[
P(t)
]

par exemple nombre de cycles complétés.

Si le temps avance mais :

[
Delta P = 0
]

pendant trop longtemps, le système peut être bloqué.

---

## Stabilité de débit

Sous charge fixe, nous pouvons observer si le débit :

[
lambda_{	ext{out}}
]

reste proche du débit attendu.

Si les files augmentent constamment, le système n’est pas en régime stationnaire.

---

## Queue stability

Pour une file avec arrivées et service, une condition intuitive de stabilité à long terme exige généralement que la capacité de service dépasse le taux d’arrivée moyen dans les hypothèses du modèle.

[
lambda < mu
]

est une relation classique dans des modèles simples.

Mais les vraies files peuvent être plus complexes.

Le protocole doit mesurer.

---

## Backlog

Nous pouvons suivre :

[
Q(t)
]

la taille d’une file.

Si (Q(t)) augmente sans borne sous charge nominale, le système n’est pas stable pour cette charge.

---

## Énergie ou ressource

Un système peut rester fonctionnel tout en consommant de plus en plus de CPU, mémoire ou énergie.

La stabilité opérationnelle doit parfois inclure les ressources.

---

## Budget de ressource

Nous pouvons fixer :

[
CPU le C_{max}
]

[
MEM le M_{max}
]

[
LAT le L_{max}
]

Le PASS devient multidimensionnel.

---

## Un système peut être stable sur une métrique et instable sur une autre

Sortie stable.

Mémoire croissante.

Latence croissante.

Cette combinaison est possible.

Alors le verdict global doit être décomposable.

---

## Score unique : prudence

Il peut être tentant de fusionner toutes les métriques en un score de stabilité.

Cela peut aider l’interface.

Mais un score agrégé peut cacher la cause.

Si nous utilisons un score, ses composantes doivent rester visibles.

---

## Score candidat

Conceptuellement :

[
S =
w_1s_1+w_2s_2+cdots+w_ks_k
]

Mais les poids (w_i) sont des choix.

Ils doivent être justifiés.

Un score élégant ne remplace pas les mesures brutes.

---

## PASS multidimensionnel

Une approche souvent plus claire :

[
PASS
=
C_1
land
C_2
land
cdots
land
C_k
]

Chaque condition correspond à une exigence.

Ainsi, l’échec montre immédiatement quelle contrainte a cassé.

---

## Les quatre chemins comme laboratoire

Nous pouvons utiliser nos quatre chemins pour tester différentes stratégies.

Par exemple :

(P_1) nominal.

(P_2) bruit ajouté.

(P_3) délai ajouté.

(P_4) perturbation de paramètre.

Puis comparer les réponses.

Mais seulement si cette architecture correspond à l’objectif expérimental.

---

## Chemins parallèles contrôlés

Une expérience parallèle peut être plus forte si les chemins partagent exactement la même entrée de base.

Cela crée une comparaison.

Mais nous devons contrôler :

même tick;

même source;

même seed si nécessaire;

mêmes versions hors perturbation.

Sinon nous comparons des choses différentes.

---

## Contrôle expérimental

Un chemin peut jouer le rôle de contrôle.

Pas de perturbation.

Les autres reçoivent des variations.

Alors la différence :

[
Delta y_k
=
y_k-y_{	ext{control}}
]

peut aider à isoler l’effet.

Cette structure rapproche Brutus d’un vrai banc expérimental.

---

## Randomisation

Dans certaines expériences, randomiser l’ordre des perturbations peut réduire certains biais temporels.

Mais cela dépend du protocole.

La randomisation doit être enregistrée avec seed si elle doit être reproductible.

---

## Réplication

Un seul run n’est pas toujours suffisant.

Nous pouvons répéter :

[
N
]

fois.

Puis comparer la variabilité.

Si le système est déterministe et les conditions identiques, nous attendons peut-être la même sortie.

S’il est stochastique, nous analysons une distribution.

---

## Stabilité inter-run

Nous pouvons mesurer la variation entre runs.

Cela révèle des dépendances cachées :

seed;

temps;

ordre;

ressource externe;

concurrence.

Un système qui change beaucoup entre runs identiques doit être expliqué.

---

## Baseline avant perturbation

Avant chaque perturbation, il faut vérifier que le système est déjà dans un état nominal.

Sinon nous ne savons pas si la réponse provient de la perturbation ou d’un problème préexistant.

Nous pouvons imposer :

[
BASELINE = PASS
]

avant injection.

---

## Washout

Après une perturbation, il peut être nécessaire d’attendre un retour complet avant la suivante.

Sinon les effets se superposent.

Cette période peut être appelée washout ou récupération.

Sa durée doit être définie.

---

## Perturbations combinées

Après les tests simples, nous pouvons combiner.

Retard + charge.

Bruit + perte de chemin.

Restart + trafic.

Mais la complexité augmente vite.

La règle reste :

**une variable à la fois d’abord, combinaisons ensuite.**

---

## Interaction

Deux perturbations peuvent avoir un effet plus fort ensemble que séparément.

Cela révèle une interaction.

Une expérience factorielle peut étudier ces effets.

Mais nous n’avons pas besoin de commencer là.

Le chapitre défend d’abord la discipline.

---

## La stabilité ne doit pas être devinée visuellement

Une courbe lisse peut rassurer.

Une courbe agitée peut inquiéter.

Mais l’œil humain peut être trompé par :

échelle;

lissage;

zoom;

framerate;

échantillonnage.

Le verdict doit venir des données et critères.

---

## Lissage

Un filtre peut produire une courbe plus propre.

Mais il peut cacher des pics.

Alors l’interface doit distinguer :

raw;

filtered.

Un graphique lissé ne doit pas remplacer silencieusement le signal brut.

---

## Filtre

Un filtre peut être parfaitement légitime.

Par exemple, une moyenne mobile :

[
ar{x}_n
=
rac{1}{N}
sum_{k=0}^{N-1}
x_{n-k}
]

Mais la fenêtre (N) modifie la réponse.

La visualisation doit déclarer ce choix.

---

## Le cristal et la stabilité

Nous pouvons maintenant revenir au mot **cristallisation**.

Dans le projet, il peut symboliser un état stabilisé et vérifié.

Mais il ne doit pas signifier :

**la valeur ne bouge plus.**

Une cristallisation technique candidate peut exiger :

baseline passée;

invariants respectés;

 perturbation testée;

temps d’observation réussi;

checkpoint créé;

hash enregistré.

---

## CRYSTAL PASS

Nous pouvons imaginer :

[
CRYSTAL_PASS
=
BASELINE
land
STABILITY
land
INTEGRITY
land
CHECKPOINT
]

C’est une règle architecturale.

Pas une loi de physique.

Le nom peut être poétique.

La condition doit être calculable.

---

## Cristallisation temporaire

Un état cristallisé à la version (v) peut devenir non vérifié à la version (v+1).

Alors :

[
CRYSTAL(v)

otRightarrow
CRYSTAL(v+1)
]

Les tests doivent être rejoués.

La preuve est versionnée.

---

## Régression de stabilité

Une nouvelle fonctionnalité peut conserver toutes les sorties correctes mais augmenter le jitter.

Ou le temps de récupération.

Ou la consommation mémoire.

Le test de stabilité doit donc faire partie des non-régressions.

---

## Budget de régression

Nous pouvons accepter certaines variations.

Par exemple :

latence +2 % maximum;

mémoire +5 % maximum;

aucune nouvelle erreur critique.

Ces seuils sont des décisions.

Ils doivent être fixés avant comparaison.

---

## Performance et stabilité

Un système plus rapide n’est pas automatiquement meilleur.

Une optimisation peut réduire la latence moyenne mais augmenter le jitter ou les erreurs.

Le rapport doit regarder plusieurs métriques.

---

## Optimisation prématurée

Avant de stabiliser une architecture, optimiser trop tôt peut compliquer le diagnostic.

Il est parfois préférable d’avoir une version plus lente mais compréhensible.

Puis optimiser avec une baseline.

La vitesse vient après la vérité de fonctionnement.

---

## Le protocole STABILITY_PROTOCOL_V1

Le chapitre 10 proposait déjà un artefact :

**STABILITY_PROTOCOL_V1.**

Nous pouvons maintenant lui donner une première structure.

### 1. IDENTITÉ
- version du système;
- HEAD;
- configuration;
- environnement.

### 2. BASELINE
- durée;
- métriques;
- seuils.

### 3. PERTURBATION
- type;
- amplitude;
- durée;
- moment.

### 4. OBSERVATION
- variables;
- fréquence d’échantillonnage;
- durée.

### 5. CRITÈRES
- PASS;
- FAIL;
- UNKNOWN.

### 6. RÉSULTAT
- mesures;
- écarts;
- verdict protocolaire.

### 7. PREUVE
- logs;
- snapshots;
- hashes;
- graphiques;
- replay.

Cette structure peut devenir un vrai artefact plus tard.

---

## UNKNOWN doit exister

Si les données manquent, le protocole ne doit pas forcer PASS ou FAIL.

Il peut produire :

[
UNKNOWN
]

Par exemple :

capteur perdu;

run interrompu;

log corrompu;

fenêtre trop courte.

C’est une sortie valide.

---

## Test interrompu

Un run arrêté avant la fin ne doit pas être présenté comme PASS simplement parce qu’aucune panne n’a été vue jusque-là.

Le statut peut être :

**INCOMPLETE.**

La durée est une partie du protocole.

---

## Absence de panne ≠ preuve d’invulnérabilité

Un test long qui ne trouve aucune panne augmente la confiance dans les conditions testées.

Mais il ne prouve jamais l’impossibilité de toute panne.

La formulation doit rester limitée.

---

## La stabilité et l’incertitude

Les mesures elles-mêmes ont une incertitude.

Si un seuil est très proche de la mesure, l’incertitude peut changer le verdict.

Par exemple :

[
M = 0.050 pm 0.003
]

et :

[
T = 0.050
]

Le PASS n’est pas évident.

Le protocole peut prévoir une zone indéterminée.

---

## Zone grise

Nous pouvons définir :

PASS;

FAIL;

BORDERLINE.

Cette troisième catégorie peut être utile lorsque la mesure est trop proche du seuil ou trop incertaine.

Mais elle doit être définie avant le test.

---

## Sensibilité

Une analyse de sensibilité demande :

comment le résultat change-t-il quand un paramètre change légèrement ?

[
S_i
=
rac{partial y}{partial 	heta_i}
]

dans un cadre différentiable.

Une forte sensibilité peut signaler une fragilité.

---

## Sensibilité numérique

Même sans dérivée analytique, nous pouvons approximer :

[
S_i
approx
rac{
y(	heta_i+Delta)-y(	heta_i)
}{
Delta
}
]

pour de petits (Delta), avec prudence.

La taille de (Delta) influence l’estimation.

---

## Paramètre fragile

Un paramètre dont une variation minuscule produit un grand changement peut demander :

contrôle plus précis;

meilleure mesure;

reformulation;

bornes.

La stabilité peut donc révéler où l’architecture est sensible.

---

## Conditionnement

En analyse numérique, un problème mal conditionné peut amplifier les petites erreurs d’entrée.

Cela doit être distingué d’un algorithme instable.

Le problème lui-même peut être sensible.

L’implémentation peut ajouter une autre instabilité.

---

## Erreur numérique

Arrondis.

Précision flottante.

Accumulation.

Soustraction de nombres proches.

Ces effets peuvent produire une dérive.

Le protocole doit parfois comparer plusieurs précisions numériques.

---

## Float32 vs float64

Une expérience peut exécuter le même calcul avec deux précisions.

Si les résultats divergent fortement, cela peut révéler une sensibilité numérique.

Mais la précision plus élevée n’est pas automatiquement « vraie ».

Elle réduit certaines erreurs d’arrondi.

Le modèle reste à vérifier.

---

## Reproductibilité numérique

Sur certains matériels ou environnements, l’ordre des opérations peut produire de petits écarts.

Une tolérance numérique doit donc être définie.

Comparer des floats par égalité exacte peut être inapproprié dans certains cas.

---

## Tolérance numérique

Une comparaison peut utiliser :

[
|a-b|
le
atol
+
rtol|b|
]

avec tolérance absolue et relative.

Les valeurs de (atol) et (rtol) doivent être adaptées au contexte.

Encore une fois :

le seuil fait partie du protocole.

---

## Le système doit connaître ses limites

La meilleure conclusion d’un test de stabilité peut être :

**stable jusqu’ici, pas au-delà.**

C’est une information utile.

Une limite connue est meilleure qu’une prétention illimitée.

---

## Carte de fonctionnement

À la fin, nous pouvons imaginer une carte :

zone nominale;

zone dégradée;

zone récupérable;

zone instable;

zone inconnue.

Cette carte devient une véritable connaissance opérationnelle.

---

## Nominal

Dans la zone nominale :

tous les critères passent.

---

## Dégradé

Dans la zone dégradée :

le système fonctionne mais certains critères secondaires échouent ou des chemins sont absents.

---

## Récupérable

Dans la zone récupérable :

une perturbation fait sortir du nominal mais le protocole de récupération ramène dans l’état acceptable.

---

## Instable

Dans la zone instable :

l’écart augmente, le système diverge, les erreurs s’accumulent ou le retour échoue.

---

## Inconnu

Dans la zone inconnue :

nous n’avons pas de données suffisantes.

Cette zone doit rester visible.

---

## Le rôle du laboratoire

Le laboratoire ne doit pas seulement montrer ce qui marche.

Il doit cartographier :

où ça marche;

où ça casse;

comment ça revient;

où nous ne savons pas.

C’est beaucoup plus scientifique.

---

## La visualisation de stabilité

Une interface peut montrer :

baseline;

perturbation;

écart;

temps de retour;

seuils;

statut.

Mais le graphique doit être lié aux données réelles.

La coquille ne pense toujours pas.

---

## Ligne de seuil

Un graphique peut afficher :

[
epsilon
]

comme bande de tolérance.

Cela rend visible le contrat.

Le lecteur voit immédiatement si la trajectoire sort de la zone.

---

## Marquer l’injection

Le moment de perturbation doit être marqué.

Sinon la réponse semble apparaître sans cause.

Une ligne verticale peut indiquer :

**PERTURBATION START**

puis :

**PERTURBATION END**

Le visuel raconte le protocole.

---

## Marquer le retour

Lorsque les critères de retour sont satisfaits :

**RECOVERED AT t = ...**

Cela permet de lire le temps de récupération.

---

## Un graphique n’est pas le verdict

Le graphique aide.

Le verdict vient du protocole calculé.

Le lecteur doit pouvoir retrouver :

valeurs;

seuils;

calcul.

---

## Le test doit produire un rapport

Un rapport de stabilité peut contenir :

objectif;

configuration;

baseline;

perturbation;

mesures;

plots;

PASS/FAIL/UNKNOWN;

anomalies;

limites;

prochaine expérience.

Le rapport devient une preuve versionnée.

---

## Le test doit pouvoir être rejoué

Un bon protocole doit fournir :

commande;

seed;

configuration;

entrée;

durée;

version.

Une autre personne doit pouvoir relancer.

La reproductibilité revient encore.

---

## Le test doit pouvoir échouer honnêtement

Si nous concevons un test impossible à échouer, il ne mesure rien.

Le seuil doit être réel.

Le système doit accepter FAIL.

C’est une condition de crédibilité.

---

## Ne jamais modifier le seuil pendant le run

Si le système approche de la limite, il peut être tentant d’augmenter le seuil.

Ce serait changer les règles pendant l’expérience.

Toute modification de seuil doit créer une nouvelle version du protocole.

---

## STABILITY_PROTOCOL_V2

Si nous découvrons que V1 est mal conçu, nous pouvons créer V2.

L’ancien résultat reste associé à V1.

Nous n’effaçons pas.

Nous évoluons.

---

## Comparabilité

Deux résultats ne sont comparables que si les protocoles sont suffisamment proches.

Changer :

hardware;

fréquence;

seuil;

perturbation;

version;

peut empêcher une comparaison directe.

Le rapport doit signaler ces différences.

---

## Benchmark

Un benchmark est une expérience standardisée de comparaison.

Il peut être utile pour suivre l’évolution.

Mais un benchmark optimisé à l’excès peut devenir un objectif trompeur.

Le système doit rester représentatif de l’usage réel.

---

## Goodhart

Lorsqu’une métrique devient une cible, elle peut perdre sa qualité comme mesure.

Si nous optimisons uniquement pour un score de stabilité, nous pouvons sacrifier d’autres propriétés.

La Bible doit se méfier des scores uniques.

---

## Multi-objectifs

Nous avons souvent plusieurs objectifs :

stabilité;

latence;

mémoire;

précision;

énergie.

Améliorer l’un peut dégrader l’autre.

Alors l’optimisation devient un problème multi-objectifs.

Il n’existe pas toujours un meilleur point absolu.

---

## Pareto

Un ensemble de solutions peut être Pareto-optimal si améliorer un objectif dégrade au moins un autre.

Cette idée peut aider plus tard à choisir des compromis.

Mais elle demande une vraie définition des objectifs.

---

## Le choix revient au besoin

La stabilité n’existe pas en dehors du but.

Une interface artistique tolère peut-être 30 ms de jitter.

Un système de contrôle critique peut exiger beaucoup moins.

Le seuil doit venir de la fonction.

Pas de l’esthétique.

---

## Stabilité du concept

Même une architecture conceptuelle peut être testée.

Les définitions restent-elles cohérentes lorsqu’on ajoute de nouveaux modules ?

Les ports suffisent-ils ?

Les statuts deviennent-ils contradictoires ?

La documentation peut elle aussi devenir instable.

---

## Contradiction documentaire

Si un chapitre dit :

TIME signifie A

et un autre :

TIME signifie B

sans version ni distinction, l’architecture conceptuelle dérive.

Le canon doit détecter ces contradictions.

La stabilité du langage protège la stabilité du code.

---

## Le glossaire

Un glossaire versionné peut devenir une forme de stabilité sémantique.

Chaque terme important :

définition;

version;

aliases;

statut.

Ainsi, les mots ne changent pas silencieusement de sens.

---

## Stable ne veut pas dire figé

Un projet stable peut évoluer.

La stabilité signifie que l’évolution est contrôlée, mesurée et versionnée.

Une architecture figée peut être très fragile.

Le changement n’est pas l’ennemi.

Le changement non observé l’est.

---

## Changement contrôlé

[
CHANGE
ightarrow
TEST
ightarrow
COMPARE
ightarrow
ACCEPT
]

Si le changement échoue :

[
REJECT
]

ou :

[
REVISE
]

Cette boucle maintient la stabilité pendant l’évolution.

---

## Feature flag

Une nouvelle fonction peut être activée progressivement.

Cela permet de comparer.

Mais le flag doit être tracé.

Un résultat obtenu avec le flag ON n’est pas le même contexte qu’avec OFF.

---

## Canary

Une modification peut être déployée sur une petite fraction ou un environnement limité avant généralisation.

Cela réduit le risque.

Le principe est encore :

petit → mesurer → étendre.

---

## La stabilité comme accumulation de preuves

Une seule réussite n’est pas la stabilité.

La confiance augmente avec :

tests variés;

durées;

réplications;

perturbations;

environnements.

Mais elle reste toujours conditionnelle.

La stabilité est un dossier de preuves.

Pas une étiquette magique.

---

## Le dossier de stabilité

Nous pouvons imaginer un artefact :

**STABILITY_EVIDENCE_V1**

contenant :

protocoles;

runs;

résultats;

plots;

failures;

versions;

limites.

Une future release peut pointer vers ce dossier.

---

## Release et stabilité

Une version peut être marquée :

**EXPERIMENTAL**

**STABLE-IN-PROTOCOL-X**

**DEGRADED**

selon les preuves.

Le mot stable doit toujours avoir un référentiel.

---

## Stable pour quoi ?

C’est peut-être la question la plus importante.

Stable pour :

une heure ?

une journée ?

100 Hz ?

1000 événements/s ?

une panne de chemin ?

10 % de bruit ?

une certaine configuration ?

Sans réponse, le mot reste vide.

---

## Formulation honnête

Au lieu de :

**Brutus est stable.**

Nous préférons :

> **Brutus version X a satisfait le protocole Y pendant T sous les perturbations D, avec les limites L.**

Cette phrase est moins spectaculaire.

Elle est beaucoup plus forte.

---

## La stabilité et la science

En science, une observation doit idéalement survivre à la variation raisonnable des conditions si elle prétend représenter un phénomène robuste.

Un résultat qui disparaît au moindre changement de paramètre peut être intéressant.

Mais son domaine doit être décrit.

La robustesse devient une partie de l’interprétation.

---

## La stabilité et les constantes

Une constante candidate doit être testée dans plusieurs contextes.

Si sa valeur change dès que nous modifions arbitrairement le protocole, elle n’est peut-être pas constante dans le sens supposé.

Le mot **constante** demande une stabilité de définition et de valeur selon le domaine.

---

## Brutus Drift

Nous pouvons donner un nom à une métrique candidate :

**Brutus Drift.**

Mais le nom seul ne suffit pas.

Il faut définir précisément :

[
D_B(t)
=
x(t)-x_{	ext{ref}}
]

ou une autre relation, selon la variable.

Le terme devient utile seulement lorsque la formule, l’unité et le protocole existent.

---

## Brutus Stability Index

Même chose pour un éventuel **Brutus Stability Index**.

Ce pourrait être un score.

Mais avant de le publier, il faudrait :

définir les composantes;

justifier les poids;

tester la sensibilité;

montrer les cas limites.

Sinon ce serait un nom avant d’être une mesure.

---

## Le nom vient après la définition

C’est une règle utile pour tous les nouveaux termes Brutus.

Définir.

Tester.

Versionner.

Puis nommer publiquement.

Cela protège la bibliothèque contre une multiplication de mots sans objets.

---

## Le chapitre 16 comme fondation

Ce chapitre ne prouve pas encore la stabilité d’ANTMUX, X72 ou Brutus.

Il construit la méthode qui permettra de le faire.

Son statut est architectural.

Il dit :

voici comment le mot stabilité doit être traité à partir d’ici.

---

## Première expérience réelle à construire

Un petit module.

Une valeur cible.

Une perturbation définie.

Un log.

Un seuil.

Un temps de retour.

Par exemple :

[
x^*=1
]

Perturbation :

[
x leftarrow 1.2
]

Puis mesurer :

combien de temps pour revenir dans :

[
[0.99,1.01]
]

si le système possède une dynamique de retour définie.

Simple.

Mesurable.

Reproductible.

---

## Deuxième expérience

Un cycle de neuf états.

Perturber la phase.

Mesurer si le système reprend son cycle.

Comparer :

phase;

période;

temps de récupération.

Cette expérience pourrait relier les structures cycliques déjà explorées au protocole réel.

---

## Troisième expérience

Quatre chemins.

Couper (P_3) pendant une durée définie.

Mesurer :

temps de détection;

passage DEGRADED;

impact sortie;

temps de restauration;

retour READY.

Le chapitre 15 et le chapitre 16 se rejoignent.

---

## Quatrième expérience

Long run.

Aucune perturbation volontaire.

Observer :

mémoire;

jitter;

fréquence;

latence;

erreurs;

dérive.

La stabilité nominale doit elle aussi être mesurée.

---

## Cinquième expérience

Charge croissante.

[
lambda_1 < lambda_2 < cdots < lambda_n
]

Trouver :

zone nominale;

zone dégradée;

seuil d’échec.

Cela produit une carte opérationnelle.

---

## Ce que nous ne devons pas faire

Regarder une animation pendant dix secondes.

Dire :

**ça a l’air stable.**

Changer un seuil après coup.

Ignorer les runs qui échouent.

Lisser jusqu’à cacher les pics.

Afficher seulement la moyenne.

Confondre absence de crash et stabilité.

Confondre récupération et stabilité.

Confondre répétabilité et exactitude.

---

## Ce que nous devons faire

Définir.

Perturber.

Mesurer.

Comparer.

Rejouer.

Versionner.

Conserver les échecs.

Limiter les conclusions.

Voilà le protocole.

---

## Le prochain chapitre

À mesure que nous mesurons la stabilité, une autre notion devient centrale.

Les signaux.

Fréquences.

Phases.

Résonances.

Spectres.

Filtres.

Bruit.

Jusqu’ici, nous avons parlé du temps comme battement.

Maintenant, le temps peut être regardé depuis l’autre côté :

**la fréquence.**

Le chapitre suivant pourra explorer comment un signal se transforme lorsqu’on cesse de le regarder seulement comme une suite de valeurs et qu’on commence à regarder ses composantes.

---

## Temps et fréquence

Une même réalité peut parfois être étudiée dans le domaine temporel ou fréquentiel.

Le temps montre :

quand.

La fréquence montre :

à quels rythmes.

Cette dualité deviendra une nouvelle porte.

Mais elle doit être abordée avec les mêmes règles :

unités;

échantillonnage;

Nyquist;

fenêtrage;

résolution;

preuve.

---

## La résonance ne doit pas devenir magique

Le mot résonance est puissant.

Il possède un sens précis en physique et en ingénierie dans différents contextes.

Il ne doit pas signifier simplement :

**deux choses semblent vibrer ensemble.**

Le prochain chapitre devra protéger ce mot.

---

## Dernière image

Nous reprenons le système après réparation.

Il tourne.

Mais cette fois, nous ne nous contentons pas de le regarder.

Nous notons la baseline.

Nous définissons la perturbation.

Nous lançons le test.

P3 tombe.

La sortie dérive.

Le registre écrit.

Le réparateur agit.

La trajectoire revient.

Le chronomètre s’arrête.

Puis nous faisons quelque chose de nouveau.

Nous ne disons pas :

**ça marche.**

Nous disons :

**voici jusqu’où ça s’est écarté.**

**voici combien de temps ça a pris.**

**voici ce qui a échoué.**

**voici ce qui a tenu.**

**voici les limites du protocole.**

Le système n’a pas reçu une médaille.

Il a reçu des mesures.

Et pour la première fois, le mot stabilité peut commencer à signifier quelque chose.

# **CE QUI TIENT DOIT ÊTRE MESURÉ. CE QUI RÉSONNE DEVRA ÊTRE DÉFINI.**
