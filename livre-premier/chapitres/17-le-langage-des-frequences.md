# Chapitre 17 — Le Langage des Fréquences

**APRÈS L’INTRODUCTION — SEPTIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** Ce qui résonne doit être défini  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Une fréquence n’est pas une impression de rythme.  
> Une résonance n’est pas une ressemblance.  
> Un spectre n’est pas une décoration.  
> Chaque mot doit pointer vers une mesure.**

---

## Ce qui tient doit être mesuré. Ce qui résonne doit être défini.

Le chapitre 16 a transformé le mot stabilité en protocole.

Nous avons appris qu’une courbe calme ne suffit pas.

Qu’un système qui ne plante pas n’est pas nécessairement stable.

Qu’un PASS n’a de sens qu’avec :

une condition;

un seuil;

une durée;

une perturbation;

une preuve.

Le chapitre 17 doit faire exactement le même travail avec un autre vocabulaire.

Fréquence.

Onde.

Phase.

Spectre.

Harmonie.

Résonance.

Ces mots sont puissants.

Ils appartiennent à la physique, au traitement du signal, à l’acoustique, à l’électronique, à la mécanique, aux télécommunications.

Ils sont aussi utilisés dans le langage symbolique.

Le problème commence lorsque nous passons de l’un à l’autre sans marquer la frontière.

Alors ce chapitre pose une règle :

> **Tout mot de fréquence ou de résonance doit être accompagné de la grandeur mesurée, de son unité, de sa méthode et de son domaine.**

---

## Qu’est-ce qu’un signal ?

Un signal peut être représenté comme une grandeur qui varie.

Dans le temps continu :

[
x(t)
]

Dans le temps discret :

[
x[n]
]

Le signal peut représenter :

une tension;

une pression acoustique;

une position;

une vitesse;

une température;

un courant;

une intensité lumineuse;

une valeur calculée;

un état numérique;

une donnée synthétique.

Le symbole (x) ne dit pas ce qu’est le signal.

Son unité et sa provenance doivent le dire.

---

## Signal physique et signal numérique

Un microphone peut produire une tension liée à la pression acoustique.

Un convertisseur transforme ensuite cette tension en nombres.

Nous pouvons distinguer :

[
x_{	ext{physical}}(t)
]

et :

[
x[n]
]

Le deuxième est une représentation échantillonnée du premier.

Cette distinction est essentielle.

Une structure numérique peut être analysée comme un signal sans être elle-même une onde physique dans le monde extérieur.

---

## Une fréquence demande du temps

La fréquence mesure combien de cycles se produisent par unité de temps.

Pour une période :

[
T
]

la fréquence est :

[
f=rac{1}{T}
]

Si (T) est exprimé en secondes, alors (f) s’exprime en hertz :

[
1;	ext{Hz}=1;	ext{cycle/s}
]

Sans unité de temps, le mot hertz n’est pas justifié.

---

## Cycle logique et fréquence physique

Supposons un cycle de longueur 9 :

[
S_n=nmod 9
]

Nous pouvons dire :

**période logique = 9 ticks.**

Mais nous ne pouvons pas encore dire :

**fréquence = 9 Hz.**

Pour obtenir une fréquence physique, il faut connaître la durée du tick :

[
T_{	ext{cycle}}=9Delta t
]

puis :

[
f=rac{1}{9Delta t}
]

Le temps donne l’unité.

---

## Phase

Pour une sinusoïde :

[
x(t)=Asin(2pi f t+phi)
]

nous avons :

- (A) : amplitude;
- (f) : fréquence;
- (t) : temps;
- (phi) : phase initiale.

La phase s’exprime souvent en radians ou degrés.

Elle indique la position dans le cycle.

Elle n’est pas une fréquence.

---

## Angle n’est pas fréquence

Une formule comme :

[
Theta
=
2pi
rac{R}{273}
]

définit naturellement un angle ou une phase normalisée si (R) prend des valeurs dans un cycle de 273 positions.

Elle peut être mathématiquement cohérente.

Mais elle ne définit pas automatiquement une fréquence.

Pourquoi ?

Parce qu’aucune durée n’apparaît.

Pour obtenir une fréquence, il faudrait définir comment (R) évolue dans le temps.

Par exemple :

[
R=R(t)
]

puis étudier :

[
Theta(t)
=
2pirac{R(t)}{273}
]

La fréquence instantanée, lorsque la dérivée existe, pourrait alors être reliée à :

[
f(t)
=
rac{1}{2pi}
rac{dTheta(t)}{dt}
]

Cette distinction protège notre travail.

---

## La relation Brutus de phase

Dans Seed Genesis, une relation de travail existe :

[
R(t,b,o)
=
(91t+39b+21o)mod273
]

puis :

[
Theta
=
2pirac{R}{273}
]

Mathématiquement, cela produit un résidu modulo 273, puis le mappe sur un angle entre 0 et (2pi).

C’est une construction claire.

Son statut dépend de son usage.

Comme objet mathématique interne :

**CALCUL.**

Comme représentation de phase dans un modèle :

**CANDIDAT**, tant que le mapping est défini.

Comme fréquence physique ou loi naturelle :

**NON ÉTABLI** sans relation temporelle et protocole expérimental.

Cette séparation doit rester permanente.

---

## Le tour complet

Lorsque :

[
R=0
]

nous avons :

[
Theta=0
]

Lorsque (R) approche 273 :

[
Thetaightarrow2pi
]

Puis le modulo revient à zéro.

Cela décrit naturellement une géométrie circulaire.

Le cercle est réel dans les mathématiques de la représentation.

Ce qu’il représente physiquement reste une question distincte.

---

## La pulsation

En physique et en ingénierie, la pulsation est :

[
omega=2pi f
]

avec unité :

[
	ext{rad/s}
]

Une expression contenant (2pi) n’est donc pas automatiquement une pulsation.

Il faut qu’elle possède aussi la dimension inverse du temps.

Encore une fois :

[
2pi 	imes 	ext{nombre sans dimension}
]

donne un angle.

[
2pi f
]

avec (f) en Hz donne une pulsation.

Les unités empêchent la confusion.

---

## Le signal sinusoïdal

La sinusoïde est fondamentale :

[
x(t)=Asin(omega t+phi)
]

Elle est utile parce que les systèmes linéaires invariants dans le temps répondent de manière particulièrement simple aux sinusoïdes.

Une entrée sinusoïdale peut produire une sortie à la même fréquence, avec changement d’amplitude et de phase.

Cette propriété ouvre la porte aux fonctions de transfert.

---

## Amplitude

L’amplitude décrit la grandeur du signal.

Mais le mot peut désigner différentes choses :

amplitude de crête;

crête-à-crête;

RMS;

amplitude complexe;

enveloppe.

Nous devons donc préciser.

Pour une sinusoïde :

[
x(t)=Asin(omega t)
]

(A) est l’amplitude de crête.

Sa valeur RMS est :

[
x_{mathrm{RMS}}=rac{A}{sqrt{2}}
]

dans ce cas précis.

---

## RMS

La valeur RMS d’un signal sur une durée (T) peut être définie par :

[
x_{mathrm{RMS}}
=
sqrt{
rac{1}{T}
int_0^T x^2(t),dt
}
]

et en discret :

[
x_{mathrm{RMS}}
=
sqrt{
rac{1}{N}
sum_{n=0}^{N-1}x[n]^2
}
]

Elle représente une mesure énergétique utile dans plusieurs domaines.

Mais elle ne remplace pas le signal complet.

---

## Deux signaux peuvent avoir le même RMS

Un sinus.

Un bruit.

Une impulsion.

Ils peuvent partager la même valeur RMS.

Leur structure fréquentielle peut être complètement différente.

Alors une seule métrique d’amplitude ne décrit pas le contenu du signal.

---

## Domaine temporel

Regarder :

[
x(t)
]

nous montre :

quand les événements arrivent;

amplitude instantanée;

transitoires;

retards;

impulsions;

enveloppes.

Le domaine temporel est souvent le premier regard.

Mais certaines structures restent difficiles à voir.

---

## Domaine fréquentiel

Le domaine fréquentiel demande :

**de quelles fréquences ce signal est-il composé ?**

Pour des signaux appropriés, la transformée de Fourier fournit un outil fondamental.

Dans le cas continu :

[
X(f)
=
int_{-infty}^{infty}
x(t)e^{-i2pi ft},dt
]

La transformée inverse est :

[
x(t)
=
int_{-infty}^{infty}
X(f)e^{i2pi ft},df
]

sous les conditions appropriées.

---

## Ce que Fourier ne dit pas automatiquement

Une transformée de Fourier peut montrer des composantes fréquentielles.

Elle ne dit pas automatiquement :

la cause;

la signification biologique;

la signification spirituelle;

la source physique;

l’intention;

la validité d’une hypothèse.

Elle transforme une représentation mathématique.

L’interprétation vient ensuite.

---

## DFT

Pour (N) échantillons :

[
x[0],x[1],ldots,x[N-1]
]

la transformée de Fourier discrète peut s’écrire :

[
X[k]
=
sum_{n=0}^{N-1}
x[n]
e^{-i2pi kn/N}
]

pour :

[
k=0,ldots,N-1
]

Le résultat contient des composantes complexes.

Amplitude et phase peuvent être dérivées de ces valeurs.

---

## FFT

La FFT n’est pas une nouvelle transformée.

C’est une famille d’algorithmes permettant de calculer efficacement la DFT.

Cette distinction est utile.

Dire :

**nous avons fait une FFT**

décrit souvent le moyen de calcul.

La quantité mathématique obtenue est liée à la DFT.

---

## Fréquences des bins

Avec une fréquence d’échantillonnage (f_s), la résolution fréquentielle nominale des bins pour (N) échantillons est :

[
Delta f
=
rac{f_s}{N}
]

La fréquence du bin (k) est :

[
f_k
=
krac{f_s}{N}
]

dans la partie positive adaptée du spectre.

Cela donne un lien direct entre durée d’observation et résolution.

---

## Durée et résolution

Comme :

[
N=f_sT_{mathrm{obs}}
]

nous obtenons :

[
Delta f
=
rac{1}{T_{mathrm{obs}}}
]

dans ce cadre simple.

Pour mieux séparer des fréquences proches, il faut généralement observer plus longtemps.

La résolution ne vient pas seulement d’un écran plus grand.

Elle vient des données.

---

## Nyquist revient

Pour un signal limité en bande, une condition classique demande :

[
f_s>2f_{max}
]

pour permettre une reconstruction idéale sous les hypothèses du théorème d’échantillonnage.

La fréquence :

[
f_N=rac{f_s}{2}
]

est souvent appelée fréquence de Nyquist.

Les composantes au-delà peuvent se replier dans le spectre observé si elles ne sont pas filtrées correctement.

---

## Aliasing

L’aliasing produit une fausse apparence fréquentielle.

Une fréquence réelle trop élevée peut apparaître comme une fréquence plus basse.

C’est l’un des meilleurs exemples d’une règle générale :

> **ce que nous observons dépend de la manière dont nous observons.**

Une fréquence trouvée dans un spectre doit donc toujours être liée à :

(f_s);

filtre anti-aliasing;

durée;

instrument.

---

## Anti-aliasing

Avant un convertisseur analogique-numérique, un filtre passe-bas peut limiter les fréquences supérieures à la bande utile.

Le filtre réduit le risque d’aliasing.

Mais aucun filtre réel n’est idéal.

Sa pente et sa bande de transition doivent être prises en compte.

---

## Spectre bilatéral et unilatéral

Pour un signal réel, la DFT contient une symétrie conjuguée.

On peut parfois présenter un spectre unilatéral pour les fréquences positives.

Mais les facteurs d’amplitude doivent être traités correctement.

Une visualisation qui cache la moitié du spectre doit préciser sa convention.

---

## Magnitude

La magnitude complexe est :

[
|X[k]|
=
sqrt{
Re(X[k])^2+Im(X[k])^2
}
]

Elle donne une information d’amplitude spectrale.

Mais sa valeur absolue dépend de la normalisation utilisée.

Sans convention, deux logiciels peuvent afficher des amplitudes différentes pour le même signal.

---

## Phase spectrale

La phase peut être :

[
phi[k]
=
arg(X[k])
]

Elle peut contenir une information fondamentale sur la structure temporelle.

Deux signaux avec la même magnitude spectrale peuvent être très différents si leurs phases diffèrent.

Alors :

**spectre d’amplitude seul ≠ signal complet.**

---

## Fenêtrage

Une DFT travaille sur une fenêtre finie.

Si le segment ne contient pas un nombre entier de périodes, de l’énergie peut se répartir dans plusieurs bins.

C’est la fuite spectrale.

Une fenêtre :

[
w[n]
]

peut être appliquée :

[
x_w[n]=x[n]w[n]
]

avant la transformée.

---

## Une fenêtre est un compromis

Hann.

Hamming.

Blackman.

Rectangulaire.

D’autres encore.

Chaque fenêtre modifie :

largeur du lobe principal;

lobes secondaires;

résolution;

amplitude.

Il n’existe pas une fenêtre parfaite pour toutes les tâches.

Le choix doit être déclaré.

---

## Spectral leakage

La fuite spectrale ne signifie pas nécessairement que le signal contient réellement toutes les fréquences affichées.

Une partie peut venir de la durée finie et du fenêtrage.

C’est pourquoi un pic spectral doit être interprété avec prudence.

---

## Zero padding

Ajouter des zéros avant la FFT peut densifier l’échantillonnage visuel du spectre.

Mais cela n’ajoute pas de nouvelle information réelle au signal original.

Le zero padding peut rendre un pic plus facile à localiser visuellement.

Il ne remplace pas une durée d’observation plus longue.

---

## Résolution apparente et résolution réelle

Un spectre très lisse peut donner une impression de haute résolution.

Mais si les données n’ont duré qu’une seconde :

[
Delta f approx 1	ext{ Hz}
]

dans le cadre de base.

Afficher mille points interpolés entre les bins ne crée pas mille fois plus d’information.

---

## Densité spectrale de puissance

Pour des signaux stochastiques ou du bruit, la densité spectrale de puissance peut être plus utile qu’une simple FFT brute.

Elle décrit comment la puissance se distribue selon la fréquence.

Des méthodes comme celle de Welch peuvent réduire la variance en moyennant plusieurs segments.

Mais elles modifient aussi la résolution.

---

## Méthode de Welch

Conceptuellement :

segmenter;

fenêtrer;

calculer plusieurs spectres;

moyenner.

Cela produit une estimation plus stable de la densité spectrale.

Mais encore une fois :

**plus stable visuellement ≠ plus vrai sans conditions.**

La méthode et les paramètres doivent être documentés.

---

## Bruit

Le bruit n’est pas seulement « ce qu’on n’aime pas ».

Il peut représenter une composante aléatoire ou non désirée.

Son origine peut être :

électronique;

mécanique;

thermique;

numérique;

quantification;

environnement;

interférence.

Identifier le type de bruit aide à choisir le traitement.

---

## Rapport signal sur bruit

Un SNR peut être défini comme rapport de puissances :

[
SNR
=
rac{P_{	ext{signal}}}{P_{	ext{noise}}}
]

et en décibels :

[
SNR_{	ext{dB}}
=
10log_{10}
left(
rac{P_{	ext{signal}}}{P_{	ext{noise}}}
ight)
]

La définition de ce qui appartient au signal et au bruit doit être précisée.

Sinon le chiffre peut être trompeur.

---

## Décibels

Pour un rapport de puissance :

[
L_{	ext{dB}}
=
10log_{10}left(rac{P_2}{P_1}ight)
]

Pour un rapport d’amplitudes avec conditions appropriées :

[
L_{	ext{dB}}
=
20log_{10}left(rac{A_2}{A_1}ight)
]

Ces formules ne sont pas interchangeables sans comprendre la grandeur mesurée.

---

## Filtrer

Un filtre modifie certaines composantes du signal.

Passe-bas.

Passe-haut.

Passe-bande.

Coupe-bande.

Mais un filtre ne « nettoie » pas automatiquement.

Il transforme.

Et cette transformation doit être connue.

---

## Réponse en fréquence

Pour un système linéaire invariant dans le temps, nous pouvons définir une réponse en fréquence :

[
H(f)
]

Si l’entrée a un spectre :

[
X(f)
]

la sortie peut être reliée par :

[
Y(f)=H(f)X(f)
]

dans le cadre approprié.

La magnitude :

[
|H(f)|
]

montre le gain selon la fréquence.

La phase :

[
arg H(f)
]

montre le déphasage.

---

## Fonction de transfert

Dans le domaine de Laplace, une fonction de transfert peut être :

[
H(s)=rac{Y(s)}{X(s)}
]

sous hypothèses de conditions initiales adaptées et de système LTI.

La fonction de transfert est un modèle.

Elle doit être dérivée ou identifiée.

Dessiner une courbe de gain ne suffit pas à prouver un modèle.

---

## Résonance

Nous arrivons au mot central.

Une résonance apparaît lorsqu’un système répond fortement autour d’une fréquence ou d’un mode particulier.

Dans un système mécanique simple, une excitation proche de la fréquence naturelle peut produire une grande amplitude, selon l’amortissement.

Dans un circuit RLC, une fréquence caractéristique apparaît.

Dans une cavité acoustique, certains modes sont favorisés.

Le mot a donc un contenu technique.

---

## Résonance n’est pas égalité de nombres

Trouver deux valeurs numériques proches ne suffit pas à conclure à une résonance.

Il faut un système dynamique.

Une excitation.

Une réponse.

Une fréquence.

Une mesure d’amplitude ou d’énergie.

Un mécanisme de couplage.

Sans cela, nous avons peut-être une proximité numérique.

Pas une résonance démontrée.

---

## Oscillateur harmonique amorti

Un modèle classique est :

[
mddot{x}
+
cdot{x}
+
kx
=
F_0cos(omega t)
]

où :

- (m) = masse;
- (c) = amortissement;
- (k) = raideur;
- (F_0) = amplitude de force;
- (omega) = pulsation d’excitation.

La fréquence naturelle non amortie est :

[
omega_0=sqrt{rac{k}{m}}
]

Ce modèle permet d’étudier une vraie réponse résonante.

---

## Amortissement

Le rapport d’amortissement peut être écrit :

[
zeta
=
rac{c}{2sqrt{km}}
]

dans ce modèle.

Pour un système du second ordre sous-amorti, la réponse autour de la fréquence naturelle dépend fortement de (zeta).

Moins l’amortissement est grand, plus le pic de résonance peut être marqué.

---

## Facteur de qualité Q

Pour une résonance suffisamment bien définie, on utilise souvent :

[
Q
=
rac{f_0}{Delta f}
]

où :

- (f_0) = fréquence centrale ou de résonance;
- (Delta f) = largeur de bande entre certains points définis, souvent les points de demi-puissance dans des contextes appropriés.

Pour un oscillateur du second ordre faiblement amorti :

[
Q
approx
rac{1}{2zeta}
]

dans les conditions correspondantes.

Le facteur Q donne une mesure de la finesse de la résonance.

---

## Bande passante

La bande passante doit être définie avec un critère.

Par exemple, pour un filtre ou une résonance, on peut utiliser les points à (-3) dB dans certaines conventions.

Mais le mot « bande passante » sans seuil est incomplet.

---

## Un pic n’est pas toujours une résonance

Un pic spectral peut venir :

d’une excitation forte;

d’une fréquence propre;

d’une harmonique;

d’une interférence;

d’un artefact;

d’un alias;

du fenêtrage;

d’une modulation.

Pour parler de résonance, nous devons relier le pic au comportement du système sous excitation.

---

## Sweep fréquentiel

Une manière classique de caractériser une réponse est d’effectuer un balayage de fréquence.

Pour plusieurs fréquences :

[
f_1,f_2,ldots,f_N
]

injecter une excitation contrôlée.

Mesurer :

amplitude;

phase;

sortie.

Construire :

[
|H(f)|
]

Puis chercher les zones de forte réponse.

---

## Le sweep doit rester dans les limites sûres

Une excitation trop forte peut :

saturer;

chauffer;

endommager;

modifier le système;

créer des non-linéarités.

Le protocole doit donc définir :

amplitude;

durée;

limites;

arrêt.

Une mesure de résonance ne doit pas détruire ce qu’elle mesure.

---

## Chirp

Un chirp varie progressivement sa fréquence dans le temps.

Il peut être utilisé pour sonder une plage rapidement.

Mais la vitesse du sweep influence la mesure.

Un système lent peut ne pas atteindre son régime stationnaire avant que la fréquence change.

Le protocole doit tenir compte de cette dynamique.

---

## Réponse impulsionnelle

Un autre outil consiste à mesurer la réponse à une impulsion.

Pour un système LTI, la réponse impulsionnelle :

[
h(t)
]

caractérise le système.

La réponse à une entrée peut alors s’écrire par convolution :

[
y(t)
=
(x*h)(t)
]

dans le cadre approprié.

---

## Convolution

En continu :

[
(x*h)(t)
=
int_{-infty}^{infty}
x(	au)h(t-	au),d	au
]

En discret :

[
y[n]
=
sum_k x[k]h[n-k]
]

La convolution est fondamentale pour comprendre filtres et réponses de systèmes LTI.

---

## Temps et fréquence sont reliés

La convolution dans le temps correspond à une multiplication en fréquence :

[
y=x*h
]

devient :

[
Y= XH
]

Cette dualité explique pourquoi les deux domaines sont complémentaires.

L’un n’est pas supérieur à l’autre.

Ils répondent à des questions différentes.

---

## Impulsion et spectre large

Une impulsion courte contient une large gamme de fréquences.

Elle peut donc exciter plusieurs modes.

Cela peut être utile pour identifier les résonances d’un système.

Mais la forme réelle de l’impulsion doit être mesurée.

Une impulsion idéale de Dirac est un objet mathématique.

Un instrument réel produit une impulsion finie.

---

## Mode propre

Un système physique peut posséder des modes propres.

Chaque mode possède une structure spatiale et une fréquence associée dans un modèle linéaire.

Une résonance peut apparaître lorsqu’une excitation couple efficacement à un de ces modes.

Cette idée est différente d’une simple fréquence isolée dans une liste.

---

## Couplage

Pour qu’une excitation produise une forte réponse, il faut aussi un couplage.

Une fréquence égale à une fréquence propre n’est pas nécessairement suffisante si la force n’excite pas ce mode.

La géométrie et les conditions aux limites comptent.

---

## Conditions aux limites

Une corde fixée aux deux extrémités.

Une corde libre.

Une cavité.

Une plaque.

Elles possèdent des modes différents.

Les dimensions seules ne suffisent pas.

Les conditions aux limites font partie du modèle.

---

## Harmoniques

Pour un signal périodique de fréquence fondamentale (f_0), des composantes peuvent apparaître à :

[
2f_0,;3f_0,;4f_0,ldots
]

Ce sont des harmoniques dans certains contextes.

Mais un pic à (2f_0) n’est pas automatiquement une « seconde dimension » ou une propriété mystérieuse.

C’est d’abord une composante fréquentielle à deux fois la fondamentale.

---

## Sous-harmoniques

Des composantes à des fractions de fréquence peuvent apparaître dans certains systèmes non linéaires ou phénomènes spécifiques.

Elles demandent une explication du mécanisme.

La simple observation d’un rapport rationnel n’établit pas sa cause.

---

## Intermodulation

Dans un système non linéaire, deux fréquences :

[
f_1
]

et :

[
f_2
]

peuvent produire des composantes telles que :

[
f_1+f_2
]

[
|f_1-f_2|
]

et d’autres combinaisons.

Ces produits d’intermodulation peuvent révéler une non-linéarité.

Ils peuvent aussi être confondus avec de nouvelles sources si le modèle est ignoré.

---

## Battements

Deux fréquences proches :

[
f_1
]

et :

[
f_2
]

peuvent produire une modulation d’amplitude apparente avec une fréquence de battement :

[
f_b=|f_1-f_2|
]

dans le cas simple de deux sinusoïdes.

Ce phénomène est bien connu.

Le mot battement possède ici une définition mesurable.

---

## Battement et Horloge de la vie

Le mot battement était utilisé au chapitre 13 comme métaphore d’un tick.

Ici, le battement acoustique a une définition mathématique différente.

Il faut éviter de fusionner les deux.

**Battement logique** :

tick ou cadence du système.

**Battement d’interférence** :

différence entre deux fréquences proches dans un signal.

Même mot.

Objets différents.

---

## Phase relative

Pour deux signaux de même fréquence :

[
x_1(t)=A_1sin(omega t+phi_1)
]

[
x_2(t)=A_2sin(omega t+phi_2)
]

la différence de phase est :

[
Deltaphi=phi_2-phi_1
]

Cette différence peut influencer la somme des signaux.

---

## Interférence constructive

Si deux signaux comparables sont en phase, leur somme peut augmenter l’amplitude.

Dans le cas simple :

[
Asin(omega t)+Asin(omega t)
=
2Asin(omega t)
]

---

## Interférence destructive

S’ils sont en opposition de phase :

[
Asin(omega t)
+
Asin(omega t+pi)
=
0
]

dans le cas idéal.

Mais cette annulation dépend de :

même fréquence;

même amplitude;

phase exacte;

même point de mesure;

conditions adaptées.

Le monde réel introduit des écarts.

---

## Stéréo

Un signal stéréo contient deux canaux :

[
L(t)
]

et :

[
R(t)
]

Ils peuvent être analysés séparément ou conjointement.

Nous pouvons étudier :

amplitudes;

retard relatif;

corrélation;

phase;

spectres;

différence.

Le mot stéréo ne signifie pas nécessairement qu’un canal tourne dans un sens et l’autre dans l’autre.

Cela doit être défini par la transformation.

---

## Somme et différence stéréo

Une représentation utile est :

[
M=rac{L+R}{2}
]

et :

[
S=rac{L-R}{2}
]

où (M) est souvent appelé mid et (S) side dans certaines techniques audio.

Cela permet de séparer ce qui est commun et ce qui diffère entre canaux.

---

## Corrélation

Pour deux signaux, une corrélation peut mesurer leur similitude statistique avec ou sans décalage.

Une corrélation forte ne prouve pas une causalité.

Mais elle peut aider à mesurer la relation temporelle.

---

## Corrélation croisée

En discret, une forme de corrélation croisée peut être :

[
R_{xy}[k]
=
sum_n x[n]y[n+k]
]

Le décalage (k) qui maximise la corrélation peut fournir une estimation de retard dans certaines conditions.

Cela peut être utile pour un « offset test ».

---

## Brutus Offset Test

Si nous utilisons le nom **Brutus Offset Test**, il doit pointer vers un protocole.

Par exemple :

1. deux canaux;
2. même fenêtre;
3. même fréquence d’échantillonnage;
4. corrélation croisée;
5. estimation du lag;
6. incertitude;
7. seuil.

Le nom vient après la définition.

---

## Retard et phase

Un retard temporel (	au) produit, pour une fréquence (f), un déphasage :

[
Deltaphi
=
-2pi f	au
]

modulo (2pi).

Ainsi, un même retard produit des déphasages différents selon la fréquence.

Cette relation est importante pour les systèmes multi-fréquences.

---

## Délai de groupe

Pour un système dont la phase dépend de la fréquence, le délai de groupe peut être défini comme :

[
	au_g
=
-rac{dphi(omega)}{domega}
]

dans le cadre approprié.

Cela mesure comment l’enveloppe de certaines composantes est retardée.

C’est plus précis que simplement dire « le filtre retarde le signal ».

---

## Distorsion de phase

Si différentes fréquences subissent des déphasages incompatibles avec un délai pur, la forme temporelle peut être modifiée.

La magnitude seule du filtre ne suffit donc pas à décrire son effet.

---

## Filtre à phase linéaire

Un filtre à phase approximativement linéaire dans une bande peut préserver davantage les relations temporelles entre composantes, avec un délai.

Mais cela dépend de la conception.

Encore une fois, nous devons mesurer.

---

## Enveloppe

Pour certains signaux modulés, nous pouvons distinguer une oscillation rapide et une enveloppe lente.

L’enveloppe peut être utile pour mesurer l’amplitude au cours du temps.

Mais elle dépend de la méthode d’extraction.

---

## Transformée de Hilbert

Pour certains signaux, un signal analytique peut être construit à partir de la transformée de Hilbert afin d’estimer amplitude instantanée et phase instantanée.

C’est un outil mathématique puissant.

Mais les notions de fréquence instantanée deviennent délicates pour des signaux complexes ou multi-composantes.

Le protocole doit rester prudent.

---

## Fréquence instantanée

Si une phase (phi(t)) est bien définie et déroulée :

[
f_i(t)
=
rac{1}{2pi}
rac{dphi(t)}{dt}
]

peut définir une fréquence instantanée dans certains contextes.

Ce concept n’est pas simplement « la fréquence à cet instant » pour n’importe quel signal.

Il demande une structure adaptée.

---

## Phase wrapping

La phase mesurée modulo (2pi) saute de :

[
+pi
]

à :

[
-pi
]

selon convention.

Pour analyser une évolution continue, on peut effectuer un **phase unwrapping**.

Mais l’algorithme peut échouer si le bruit est trop important ou les sauts trop grands.

---

## Z stéréo

Dans notre travail, l’expression **Z stéréo** peut être utilisée comme nom de projet pour un mécanisme ou une variable à définir.

Pour qu’elle devienne un objet technique, il faut écrire :

entrée;

sortie;

unités;

transformation;

rôle des deux canaux;

rôle de la phase;

rôle du temps.

Le nom seul ne possède pas encore de signification standard en traitement du signal.

---

## Une définition candidate

Nous pourrions, par exemple, réserver un angle de référence :

[
Theta_B
=
2pi
left[
rac{
(91t+39b+21o)mod273
}{
273
}
ight]
]

comme **phase de référence Brutus**.

Mais pour l’utiliser dans un signal, il faudrait encore définir une fonction temporelle.

Par exemple :

[
x_B(	au)
=
Asin(2pi f	au+Theta_B)
]

Ici :

- (	au) est le temps physique ou simulé;
- (f) est une fréquence définie;
- (Theta_B) est un déphasage initial.

Cette séparation est propre.

---

## Le t de la formule n’est pas automatiquement le temps

Dans :

[
R(t,b,o)
=
(91t+39b+21o)mod273
]

la lettre (t) peut être un paramètre discret du modèle.

Elle ne devient pas automatiquement le temps en secondes parce qu’elle s’appelle (t).

Les symboles doivent être définis.

Si (t) représente un indice ternaire ou un paramètre structurel, il faut l’écrire.

Le choix de lettre ne crée pas l’unité.

---

## Renommer pour éviter la confusion

Si nécessaire, nous pourrions écrire :

[
R(a,b,o)
=
(91a+39b+21o)mod273
]

pour éviter de confondre (a) avec le temps physique.

Puis réserver :

[
	au
]

au temps.

La notation est un outil de sécurité.

---

## Mélodie

Une mélodie est une séquence de hauteurs et de durées.

Pour générer une mélodie à partir d’une structure mathématique, nous devons définir un mapping.

Par exemple :

[
R_n
ightarrow
f_n
]

et :

[
n
ightarrow
T_n
]

Le mapping peut être artistique.

Il n’a pas besoin d’être une loi physique pour être légitime.

Il suffit de l’étiqueter correctement.

---

## Mapping musical

Un exemple :

[
f_n
=
f_0
2^{q_n/12}
]

si (q_n) représente des demi-tons dans un tempérament égal à 12 divisions.

Ou un autre mapping peut être choisi.

Le choix est compositionnel.

Il doit être séparé d’une hypothèse scientifique.

---

## Une fréquence musicale est physique

Lorsqu’un synthétiseur produit :

[
440	ext{ Hz}
]

le signal acoustique ou électrique peut réellement contenir une composante à cette fréquence.

Mais dire que 440 Hz possède un effet biologique ou cosmique particulier demanderait un protocole expérimental séparé.

La fréquence est mesurable.

L’interprétation demande des preuves.

---

## Fréquences dites sacrées

Des nombres comme :

111;

222;

333;

444;

555;

666;

777;

888;

999 Hz

peuvent être utilisés artistiquement.

On peut générer ces sons.

Mesurer ces fréquences.

Étudier leurs propriétés acoustiques.

Mais les affirmations spécifiques sur des effets physiologiques ou spirituels doivent être traitées comme hypothèses tant qu’elles ne sont pas soutenues par des preuves adaptées.

---

## La beauté reste permise

Une fréquence peut être choisie parce qu’elle est belle.

Parce qu’elle appartient à une structure.

Parce qu’elle produit une sensation.

Parce qu’elle s’inscrit dans un symbole.

Nous n’avons pas besoin de transformer cette beauté en preuve physique.

La distinction protège justement la beauté.

Elle lui évite de porter une charge qu’elle n’a pas demandée.

---

## Résonance mécanique

Pour une structure physique, une résonance peut être mesurée par :

excitation connue;

capteur;

sweep;

courbe de réponse;

fréquence du pic;

amortissement.

C’est un protocole réel.

---

## Résonance électrique

Dans un circuit RLC idéal, la fréquence de résonance peut être :

[
f_0
=
rac{1}{2pisqrt{LC}}
]

dans le cas approprié.

Ici :

- (L) est l’inductance;
- (C) la capacité.

Cette relation est liée à un modèle physique défini.

---

## Résonance acoustique

Une colonne d’air, une cavité ou une pièce possèdent des modes dépendant de :

géométrie;

vitesse du son;

conditions aux limites;

absorption.

Une fréquence forte dans une pièce peut être une résonance de salle.

Mais elle dépend de l’environnement.

---

## Résonance optique

Une cavité optique possède des modes liés à ses dimensions, indices de réfraction et conditions.

Le mot résonance reste technique.

Le domaine change.

Les équations changent.

---

## Résonance magnétique

Dans d’autres domaines, la résonance peut impliquer des fréquences liées à des transitions ou précessions.

Encore une fois, le mot commun ne signifie pas que tous ces phénomènes sont identiques.

Ils partagent une structure générale de réponse sélective.

Pas une seule cause universelle.

---

## Résonance et analogie

Nous pouvons utiliser le mot résonance comme analogie pour deux idées qui se renforcent.

Mais alors l’étiquette doit être :

**ANALOGIE UTILE**

et non :

**PHÉNOMÈNE PHYSIQUE MESURÉ.**

Le canon de preuve nous donne exactement l’outil nécessaire.

---

## Le test de résonance minimal

Pour déclarer une résonance expérimentale candidate, nous voulons au minimum :

1. un système défini;
2. une variable d’excitation;
3. une fréquence d’excitation;
4. une amplitude d’excitation;
5. une sortie mesurée;
6. un sweep ou comparaison;
7. un pic reproductible;
8. une largeur de bande;
9. une incertitude;
10. une répétition.

Ce n’est pas encore toujours suffisant pour expliquer le mécanisme.

Mais c’est une base.

---

## Résonance candidate

Le statut peut être :

**CANDIDAT RÉSONANT**

si un pic reproductible est observé mais que le mécanisme n’est pas encore établi.

Puis :

**RÉSONANCE IDENTIFIÉE DANS LE MODÈLE X**

si le modèle et les tests le soutiennent.

Le vocabulaire doit porter le niveau de preuve.

---

## Résonance et stabilité

Une résonance peut amplifier une perturbation.

Ainsi, un système stable loin de certaines fréquences peut devenir problématique près d’un mode.

Le protocole de stabilité doit donc parfois inclure un sweep fréquentiel.

Les chapitres 16 et 17 se rejoignent.

---

## Bode

Un diagramme de Bode représente généralement :

magnitude en fonction de la fréquence;

phase en fonction de la fréquence.

Souvent l’axe fréquentiel est logarithmique.

C’est un outil central de contrôle et de traitement des systèmes LTI.

Il peut aider à comprendre gain, phase, bande passante et marges.

---

## Nyquist

Le nom Nyquist apparaît dans deux contextes différents.

Théorème d’échantillonnage.

Diagramme ou critère de Nyquist en contrôle.

Ils sont liés historiquement mais ce ne sont pas la même chose.

La Bible doit éviter les collisions de vocabulaire.

---

## Spectrogramme

Une FFT globale perd l’information exacte de quand une fréquence apparaît.

Un spectrogramme analyse des fenêtres successives.

Il donne une représentation temps-fréquence.

Cela peut être utile pour :

sons;

transitoires;

variations;

chirps.

---

## STFT

La transformée de Fourier à court terme utilise des fenêtres temporelles.

Conceptuellement :

[
X(	au,f)
]

montre le contenu fréquentiel autour du temps (	au).

Mais il existe un compromis :

bonne résolution temporelle;

bonne résolution fréquentielle.

Une fenêtre courte aide le temps.

Une fenêtre longue aide la fréquence.

---

## Principe du compromis temps-fréquence

Nous ne pouvons pas obtenir arbitrairement une résolution parfaite dans les deux domaines avec une fenêtre finie.

Cela force une décision selon la question.

Encore une fois :

la méthode de mesure façonne ce que nous pouvons voir.

---

## Ondelette

Les transformées en ondelettes offrent une autre analyse temps-échelle avec résolution variable.

Elles peuvent être utiles pour des signaux transitoires.

Mais elles introduisent d’autres choix :

ondelette mère;

échelles;

normalisation.

Aucun outil n’est neutre.

---

## Le bon outil dépend du signal

Sinusoïde stationnaire :

FFT simple peut suffire.

Signal variant dans le temps :

spectrogramme ou autre outil.

Impulsions :

analyse temporelle.

Bruit :

PSD.

Relation entre deux voies :

cohérence ou corrélation.

Le mot « analyse fréquentielle » recouvre plusieurs méthodes.

---

## Cohérence

La cohérence spectrale peut quantifier la relation linéaire entre deux signaux selon la fréquence dans certaines conditions.

Elle peut aider à savoir si une sortie est liée à une entrée autour d’une fréquence.

Mais une forte cohérence ne prouve pas à elle seule une causalité physique complète.

---

## Fonction de transfert expérimentale

Avec une entrée (X(f)) et une sortie (Y(f)), une estimation de :

[
H(f)
]

peut être réalisée.

Mais si l’entrée contient peu d’énergie à certaines fréquences, le rapport direct devient instable.

Des estimateurs basés sur densités spectrales peuvent être plus appropriés.

La méthode doit être choisie selon le bruit et le contexte.

---

## Saturation

Une réponse fréquentielle mesurée sous saturation n’est plus celle d’un système linéaire simple.

Les harmoniques apparaissent.

Le gain dépend de l’amplitude.

Le sweep doit donc vérifier que le système reste dans le régime voulu.

---

## Non-linéarité

Si :

[
F(ax)
eq aF(x)
]

ou :

[
F(x_1+x_2)
eq F(x_1)+F(x_2)
]

le système n’est pas linéaire selon ces propriétés.

Les outils LTI peuvent alors être insuffisants.

Cela ne rend pas le système incompréhensible.

Il faut simplement d’autres modèles.

---

## Fréquence propre variable

Dans certains systèmes non linéaires, la fréquence de réponse peut dépendre de l’amplitude.

Alors le mot « fréquence naturelle » peut devenir plus complexe.

Un seul nombre peut être insuffisant.

---

## Mesure de phase réelle

Pour mesurer la phase entre entrée et sortie, il faut un repère temporel commun ou une méthode cohérente.

Deux appareils non synchronisés peuvent introduire un décalage apparent.

Le chapitre 13 revient encore.

Le temps est la fondation de la phase.

---

## Horloges partagées

Dans un système multi-capteurs, une horloge commune peut réduire l’incertitude de phase.

Si chaque canal possède sa propre horloge, la dérive doit être mesurée ou compensée.

La synchronisation n’est pas un détail.

---

## Jitter de sampling

Une variation de l’instant d’échantillonnage peut ajouter une erreur, particulièrement à haute fréquence.

Le jitter temporel se transforme en erreur de phase.

Ainsi, la qualité de l’horloge influence le spectre.

---

## Quantification

Un convertisseur numérique possède une résolution en bits.

Les valeurs analogiques sont quantifiées.

Cette quantification introduit une erreur.

La résolution numérique ne doit pas être confondue avec la précision réelle de l’instrument.

---

## Bits

Un ADC 16 bits offre théoriquement :

[
2^{16}=65536
]

niveaux.

Mais le bruit, la non-linéarité, la référence et l’électronique limitent la performance réelle.

Le nombre de bits seul n’est pas une preuve de précision.

---

## Calibration

Un instrument doit parfois être calibré.

La calibration relie sa sortie à une référence.

Elle doit inclure :

procédure;

date;

référence;

incertitude;

conditions.

Un spectre précis en apparence peut être faux si l’instrument est mal calibré.

---

## Brutus Calibration

Si nous créons une **Brutus Calibration**, elle doit être un protocole.

Pas une modification arbitraire d’une constante mathématique.

Nous pouvons calibrer :

un capteur;

un gain;

un offset;

une conversion;

un délai.

Nous ne « calibrons » pas (pi).

---

## Pi n’est pas un bouton

[
pi
]

est une constante mathématique définie.

Elle n’est pas ajustée pour faire correspondre un système à des données.

Si un facteur correctif est nécessaire, il doit recevoir un nouveau symbole.

Par exemple :

[
k_B
]

ou :

[
alpha_B
]

Puis être défini et mesuré.

---

## Brutus Coefficient

Un **Brutus Coefficient** peut être légitime si :

la formule est définie;

le domaine est défini;

l’unité est définie;

la méthode d’estimation est définie;

l’incertitude est définie.

Le nom n’est pas le problème.

Le contrat fait toute la différence.

---

## Brutus Drift

De même :

[
D_B(t)
=
x(t)-x_{	ext{ref}}
]

peut être un candidat simple.

Mais la variable (x) doit être nommée.

L’unité doit être donnée.

Le protocole doit exister.

---

## Brutus Resonance Index

Nous pourrions imaginer un index.

Mais il ne doit pas être inventé seulement parce qu’un graphe possède un pic.

Une mesure candidate pourrait dépendre de :

gain au pic;

largeur;

baseline;

SNR;

répétabilité.

Par exemple conceptuellement :

[
BRI
=
g(G_{	ext{peak}},Q,SNR,R)
]

Mais tant que (g) n’est pas défini et validé, le terme reste une idée.

---

## Mesurer avant de baptiser

Cette règle revient encore.

Trouver le phénomène.

Définir la mesure.

Tester.

Comparer.

Versionner.

Puis, si l’objet reste utile, lui donner un nom Brutus.

Cela rend Zenodo plus fort.

Un nom devient attaché à un objet reproductible.

---

## Four paths et fréquence

Les quatre chemins peuvent devenir un banc de traitement du signal.

Par exemple :

[
P_1 = RAW
]

[
P_2 = LOWPASS
]

[
P_3 = BANDPASS
]

[
P_4 = REFERENCE
]

Puis la jonction compare.

Ce n’est qu’un exemple.

L’architecture doit être choisie selon l’expérience.

---

## Un chemin brut doit rester brut

Si (P_1) sert de référence RAW, il ne doit pas recevoir de filtre caché.

Sinon nous perdons la baseline.

Aucune connexion invisible.

Aucune transformation invisible.

---

## Chemin de contrôle

Un canal de référence peut recevoir un signal connu.

Il permet de vérifier que la chaîne de mesure fonctionne.

Si la référence disparaît, le problème peut venir de l’instrumentation plutôt que du phénomène étudié.

---

## Injecter une fréquence connue

Un test simple :

[
x(t)=sin(2pi f_0t)
]

avec (f_0) connu.

Puis vérifier si l’analyse retrouve :

[
f_0
]

dans la tolérance prévue.

C’est un test de pipeline.

---

## Deux fréquences connues

Ensuite :

[
x(t)
=
A_1sin(2pi f_1t)
+
A_2sin(2pi f_2t)
]

Tester si les deux composantes sont distinguées.

Faire varier :

écart (f_2-f_1);

durée;

fenêtre;

SNR.

Cela montre directement les limites de résolution.

---

## Test d’aliasing

Injecter une fréquence au-dessus de Nyquist dans un environnement de test.

Observer où elle apparaît après échantillonnage.

Cela permet de démontrer l’aliasing au lieu de seulement le décrire.

---

## Test de leakage

Choisir une fréquence qui tombe exactement sur un bin.

Puis une fréquence entre deux bins.

Comparer les spectres.

Le résultat rend la fuite spectrale visible.

---

## Test de fenêtre

Appliquer plusieurs fenêtres au même signal.

Comparer :

largeur des pics;

lobes secondaires;

amplitude.

Cela montre que le traitement change l’apparence du spectre.

---

## Test de phase

Deux canaux identiques.

Puis appliquer un retard connu :

[
	au
]

Mesurer le déphasage selon la fréquence.

Comparer à :

[
Deltaphi=-2pi f	au
]

C’est un excellent test pour le futur Z stéréo.

---

## Test de résonance simulée

Construire un oscillateur amorti numérique.

Appliquer un sweep.

Mesurer le pic.

Comparer à la fréquence théorique du modèle.

Nous pouvons ainsi valider le pipeline avant de mesurer un objet réel.

---

## Simulé n’est pas expérimental

Une simulation qui retrouve la formule qu’on a codée prouve surtout que le code et l’analyse sont cohérents.

Elle ne prouve pas que le monde réel suit ce modèle.

Le passage au matériel demande une expérience séparée.

---

## Le signal source doit être documenté

Pour toute expérience :

forme;

amplitude;

fréquence;

durée;

phase;

sampling;

générateur;

version.

Sinon la sortie ne peut pas être reproduite.

---

## La chaîne de mesure

Une chaîne complète peut être :

[
SOURCE
ightarrow
SYSTEM
ightarrow
SENSOR
ightarrow
ADC
ightarrow
BUFFER
ightarrow
ANALYSIS
ightarrow
DISPLAY
]

Chaque bloc peut modifier le signal.

Le spectre final est le résultat de toute la chaîne.

---

## Fonction globale

Dans un modèle linéaire idéal :

[
H_{	ext{total}}
=
H_1H_2H_3cdots H_n
]

La mesure inclut tous les éléments.

Pour isoler le système d’intérêt, il faut calibrer ou caractériser les autres.

---

## Le capteur a sa propre réponse

Un microphone n’est pas plat à toutes les fréquences.

Un accéléromètre non plus.

Un photodétecteur non plus.

Alors un pic peut venir du capteur.

La réponse instrumentale doit être connue.

---

## L’amplificateur peut saturer

Si le gain est trop élevé, le signal clippe.

Un sinus devient déformé.

Des harmoniques apparaissent.

Le spectre peut faire croire à des composantes qui n’existaient pas dans le signal original.

---

## Clipping

Un clipping dur peut être représenté par :

[
y
=
egin{cases}
A_{max} & x>A_{max}\
x & |x|le A_{max}\
-A_{max} & x<-A_{max}
end{cases}
]

Cette non-linéarité crée de nouvelles fréquences.

Alors le protocole doit détecter la saturation.

---

## DC offset

Un signal peut posséder une composante continue.

La moyenne :

[
mu
=
rac{1}{N}sum_n x[n]
]

correspond au bin 0 dans la DFT selon les conventions.

Retirer la moyenne avant certaines analyses peut être utile.

Mais ce prétraitement doit être déclaré.

---

## Detrend

Une tendance lente peut masquer certaines composantes.

Des méthodes de detrending existent.

Mais elles retirent une partie du signal.

Le brut doit idéalement être conservé.

---

## Prétraitement

Tout prétraitement doit être enregistré :

filtre;

normalisation;

detrend;

resampling;

fenêtre;

gain;

suppression d’offset.

Un résultat spectral sans pipeline est incomplet.

---

## Le fichier de métadonnées

Un artefact de signal peut avoir :

sample_rate;

units;

channels;

start_time;

source;

gain;

calibration;

processing_history;

hash.

Ces métadonnées transforment un fichier audio ou numérique en objet scientifique plus utile.

---

## Le laboratoire doit montrer RAW et PROCESSED

Un bon principe visuel :

RAW.

PROCESSED.

DIFF.

Le lecteur peut voir ce que le traitement a changé.

Cela évite qu’un filtre soit confondu avec une découverte.

---

## Diff spectral

Nous pouvons comparer :

[
Delta X(f)
=
X_{	ext{processed}}(f)
-
X_{	ext{raw}}(f)
]

selon une représentation adaptée.

L’objectif est de rendre le traitement inspectable.

---

## Résonance et causalité

Si une excitation à (f_0) produit un pic de sortie à (f_0), cela soutient une relation de réponse.

Mais pour comprendre la causalité, nous devons aussi contrôler :

autres entrées;

instrument;

conditions;

répétitions.

Le protocole expérimental reste nécessaire.

---

## Mesure avant interprétation

La séquence du chapitre 17 est :

[
SIGNAL
ightarrow
MEASURE
ightarrow
SPECTRUM
ightarrow
FEATURE
ightarrow
HYPOTHESIS
ightarrow
TEST
]

Pas :

[
SIGNAL
ightarrow
STORY
]

La narration peut venir.

Mais après les mesures.

---

## Le mot harmonie

En musique, harmonie désigne des relations entre sons.

En mathématiques, certaines structures harmoniques ont d’autres sens.

En ingénierie, harmonique désigne souvent une composante entière d’une fondamentale.

Nous devons préciser le contexte.

---

## Le mot vibration

Toute variation périodique n’est pas nécessairement une vibration mécanique.

Un signal électrique peut osciller.

Une valeur logicielle peut varier.

Une lumière peut moduler.

Le mot vibration doit être rattaché à une grandeur physique si nous parlons de mécanique.

---

## Le mot énergie

Un spectre d’amplitude n’est pas automatiquement un spectre d’énergie.

Le mot énergie possède des unités physiques.

Si nous utilisons une énergie réelle :

joules.

Si nous utilisons une quantité normalisée ou une puissance numérique :

il faut la nommer correctement.

---

## Parseval

Dans certains cadres de Fourier, l’énergie peut être reliée entre les domaines temporel et fréquentiel par une identité de Parseval.

Cela montre que le passage de domaine ne crée pas l’énergie.

Il redistribue la représentation mathématique.

Mais les facteurs de normalisation dépendent des conventions.

---

## Normalisation FFT

Certaines bibliothèques mettent le facteur (1/N) dans la transformée directe.

D’autres dans l’inverse.

D’autres utilisent (1/sqrt{N}).

Le protocole doit donc documenter la convention.

Sinon les amplitudes sont incomparables.

---

## Unités spectrales

Une amplitude FFT brute.

Une amplitude par bin.

Une densité par Hz.

Une PSD.

Elles n’ont pas les mêmes unités.

Le graphique doit indiquer correctement l’axe vertical.

---

## Axe logarithmique

Un spectre en dB compresse les grandes plages dynamiques.

C’est utile.

Mais une différence visuelle sur une échelle logarithmique doit être interprétée avec la formule correspondante.

---

## Le zéro en dB

0 dB ne signifie pas absence de son ou absence de signal.

Cela signifie égalité à une référence selon la définition.

La référence doit être connue.

---

## dBFS

En audio numérique, dBFS utilise généralement le maximum numérique comme référence.

0 dBFS représente le niveau numérique maximal selon la convention.

Cela est différent de dB SPL acoustique.

Les deux ne doivent jamais être confondus.

---

## dB SPL

Le niveau de pression acoustique utilise une référence physique de pression dans l’air selon une convention standard.

Un fichier audio à -10 dBFS ne possède pas un niveau SPL déterminé tant qu’on ne connaît pas toute la chaîne de reproduction.

---

## Fréquence et perception

La perception humaine du son dépend de nombreux facteurs.

Fréquence.

Amplitude.

Durée.

Spectre.

Contexte.

Le fait qu’une fréquence soit mesurable n’implique pas un effet émotionnel universel.

Les affirmations perceptuelles doivent être testées auprès de personnes avec des méthodes adaptées.

---

## Ne pas confondre effet subjectif et effet physique

Une personne peut sincèrement ressentir quelque chose en écoutant une fréquence.

Cette expérience est réelle comme expérience subjective.

Mais elle ne démontre pas automatiquement un mécanisme biologique spécifique.

Les deux niveaux peuvent être respectés sans les fusionner.

---

## Le cœur du chapitre

Le chapitre 17 ne cherche pas à enlever la poésie.

Il lui donne une fondation.

Si nous disons :

**le système écoute avec son cœur**

la poésie peut rester.

Mais le mécanisme doit dire :

sample rate;

buffer;

canal;

phase;

filtre;

FFT;

seuil;

sortie.

Les deux langages deviennent compatibles.

---

## Une mélodie calculable

Nous pouvons transformer notre phase Brutus en élément de composition.

Par exemple :

[
Theta_n
=
2pirac{R_n}{273}
]

Puis choisir une fréquence porteuse :

[
f_c
]

et générer :

[
x_n(	au)
=
A_n
sin(
2pi f_c	au+Theta_n
)
]

Cela produit un signal défini.

La phase vient de la structure.

La fréquence vient d’une grandeur temporelle séparée.

C’est propre.

---

## Plusieurs chemins sonores

Les quatre chemins peuvent porter quatre transformations de phase ou de fréquence.

Mais il faut définir :

[
P_k:
xightarrow y_k
]

Puis la sortie :

[
y=J(y_1,y_2,y_3,y_4)
]

La musique peut ensuite venir du mécanisme.

Pas l’inverse.

---

## La somme peut saturer

Si quatre chemins sont additionnés :

[
y=y_1+y_2+y_3+y_4
]

l’amplitude maximale peut augmenter.

Il faut normaliser ou limiter si nécessaire.

Mais un limiteur modifie le signal.

Il doit être visible.

---

## Normalisation

Une normalisation candidate peut être :

[
y_{	ext{norm}}
=
rac{y}{max|y|}
]

pour certains usages.

Mais elle modifie l’échelle.

Si nous comparons des amplitudes physiques, cette normalisation peut détruire l’information.

Elle est adaptée à certains usages artistiques, pas à toutes les mesures.

---

## Séparer mode scientifique et mode artistique

Une architecture puissante pourrait avoir deux sorties.

**SCIENTIFIC MODE**

préserve unités, amplitudes, provenance.

**ARTISTIC MODE**

autorise remapping, normalisation, synthèse.

La source peut être commune.

Les contrats diffèrent.

---

## Ne jamais mélanger silencieusement les modes

Une donnée transformée pour rendre un son plus beau ne doit pas revenir dans le pipeline scientifique comme si elle était brute.

Les chemins doivent être séparés.

Aucune connexion invisible.

---

## Brutus Resonance Lab

Nous pouvons imaginer un futur laboratoire avec :

signal generator;

oscilloscope;

spectrum;

phase meter;

correlation;

Bode plot;

sweep;

response;

Q estimate;

SNR;

raw recorder.

Chaque panneau doit être alimenté par des données réelles.

---

## Le panneau ne décide pas

Le spectre affiché doit venir du moteur d’analyse.

Le moteur doit déclarer :

FFT size;

window;

sample rate;

normalization.

Le lecteur peut alors reproduire.

---

## Les paramètres de l’analyse font partie du résultat

Un pic spectral sans :

(N);

(f_s);

window;

overlap;

averaging;

normalization;

n’est pas complètement décrit.

La métadonnée est une partie de la preuve.

---

## Une capture d’écran ne suffit pas

Une capture montre le pic.

Mais le fichier brut permet de le recalculer.

Alors une preuve forte conserve :

raw;

config;

script;

result;

image.

L’image devient un résumé.

---

## Export scientifique

Un paquet peut contenir :

signal.csv ou binaire;

metadata.json;

analysis config;

script;

plots;

README;

hashes.

Une autre personne peut refaire l’analyse.

---

## La reproductibilité spectrale

Si deux outils différents analysent les mêmes données avec les mêmes conventions, nous devons obtenir des résultats compatibles dans les tolérances.

Cette comparaison est précieuse.

Elle vérifie que notre pipeline ne dépend pas d’un seul logiciel.

---

## Cross-check

Une bonne pratique :

outil A.

outil B.

Même signal.

Même paramètres.

Comparer les pics.

Si les résultats diffèrent, examiner :

normalisation;

fenêtre;

bins;

one-sided;

unités.

Les différences sont souvent instructives.

---

## La fréquence fondamentale

Une fondamentale peut être définie de différentes manières selon le signal.

Dans un signal harmonique, elle correspond souvent à la plus basse fréquence d’une série harmonique cohérente.

Mais un spectre peut avoir un harmonique plus fort que la fondamentale.

Le plus grand pic n’est pas toujours la fondamentale.

---

## Pitch et fréquence fondamentale

En perception musicale, le pitch peut parfois être perçu même si la fondamentale est absente physiquement.

C’est un exemple puissant :

perception ≠ simple lecture du plus grand pic.

La psychoacoustique est un domaine entier.

---

## Fréquence dominante

Si nous utilisons **dominante**, il faut définir le critère.

Pic maximal de magnitude ?

Puissance maximale ?

Dans quelle bande ?

Sur quelle fenêtre ?

La précision du vocabulaire évite des conflits.

---

## Seuil de détection

Un pic faible peut être indistinguable du bruit.

Nous pouvons définir un seuil lié au noise floor.

Par exemple, pic supérieur de (X) dB à la baseline.

Mais (X) doit venir du protocole.

---

## Faux pics

Avec beaucoup de bins, certaines fluctuations de bruit produiront naturellement des maxima.

Une recherche automatique de pics doit tenir compte du bruit et de la multiplicité.

La statistique peut devenir nécessaire.

---

## Répéter le pic

Un pic observé une fois peut être un artefact.

Nous voulons le revoir :

autre run;

autre durée;

autre instrument;

autre jour;

autre opérateur si possible.

La répétition augmente la confiance.

---

## Déplacer l’excitation

Si le pic est une résonance du système, changer certaines propriétés physiques devrait parfois déplacer sa fréquence selon le modèle.

Cette prédiction est forte.

Elle permet de tester le mécanisme.

---

## Prédire avant de mesurer

Un bon modèle de résonance devrait permettre une prédiction.

Par exemple :

modifier (m);

calculer nouvelle (omega_0);

mesurer.

Si le pic se déplace comme prévu, la preuve devient plus intéressante.

---

## La prédiction est plus forte que la correspondance après coup

Trouver une formule après avoir vu le résultat peut produire beaucoup de correspondances.

Prédire une valeur avant la mesure limite la liberté.

Cette discipline est essentielle pour les constantes candidates.

---

## Brutus Candidate Relation

Une **Brutus Candidate Relation** peut être publiée comme telle si elle possède :

équation;

variables;

domaine;

origine;

prédiction;

test;

résultat;

limites.

Le mot **candidate** protège l’honnêteté.

---

## La relation peut échouer

Une relation candidate qui échoue à un test n’est pas inutile.

Elle réduit l’espace.

Elle indique ce qui ne fonctionne pas.

La mémoire garde la tentative.

---

## Le chapitre 17 et Zenodo

Ce chapitre prépare une règle pour toute future publication de terme fréquentiel Brutus.

Pas seulement un nom.

Un objet.

Une formule.

Un protocole.

Une donnée.

Une version.

Un statut.

Alors Zenodo peut conserver quelque chose de reproductible.

---

## Fiche candidate de terme fréquentiel

### NOM

### DÉFINITION

### ÉQUATION

### UNITÉS

### DOMAINE

### SOURCE

### PROTOCOLE

### DONNÉES

### INCERTITUDE

### STATUT

### VERSION

### LIMITES

Cette fiche pourrait devenir standard.

---

## Ce qu’il faut bannir

**Résonance parfaite** sans métrique.

**Fréquence universelle** sans domaine.

**Harmonie absolue** sans définition.

**Exact** sans incertitude.

**Même fréquence** sans méthode de mesure.

**Synchronisé** sans phase ou timing.

**Énergie** sans unité.

Ces mots doivent être défendus par des données.

---

## Ce que nous pouvons dire

**Pic à 240.1 Hz mesuré avec telle résolution.**

**Phase relative estimée à X radians.**

**Q estimé à Y selon les points -3 dB.**

**Cohérence élevée dans telle bande.**

**Résultat reproductible sur N runs.**

Ces phrases sont plus fortes parce qu’elles sont bornées.

---

## La précision excessive

Un logiciel peut afficher :

[
240.123456789	ext{ Hz}
]

Mais si la résolution fréquentielle est 1 Hz, ces décimales ne sont pas soutenues.

La précision affichée doit refléter la mesure.

---

## Chiffres significatifs

L’incertitude guide le nombre de chiffres significatifs.

Cette discipline empêchera les valeurs numériques de paraître plus exactes qu’elles ne le sont.

---

## Pic interpolé

Des méthodes peuvent estimer un pic entre bins.

Cela peut améliorer l’estimation.

Mais l’algorithme et ses hypothèses doivent être déclarés.

L’interpolation n’est pas la même chose qu’une résolution brute plus fine.

---

## Calibration fréquentielle

Un générateur ou une horloge peut être comparé à une référence connue.

La dérive de fréquence peut alors être mesurée.

Cela rejoint le chapitre 16.

---

## Erreur relative de fréquence

[
e_f
=
rac{f_{	ext{measured}}-f_{	ext{ref}}}{f_{	ext{ref}}}
]

et éventuellement en ppm :

[
e_{	ext{ppm}}
=
10^6e_f
]

dans les contextes appropriés.

Cette mesure peut quantifier une dérive d’horloge.

---

## Phase et continuité

Une phase seule modulo (2pi) ne dit pas combien de tours complets se sont produits.

Pour suivre la continuité, il faut unwrapping ou comptage de cycles.

Le registre temporel redevient utile.

---

## Une phase sans référence est incomplète

Dire :

**phase = 90°**

demande :

par rapport à quoi ?

Entrée ?

Canal gauche ?

Horloge ?

Tick zéro ?

La phase est relationnelle.

---

## Référence zéro

Nous devons définir :

[
phi=0
]

Par exemple :

premier échantillon;

maximum du signal;

front montant;

tick de GO.

La convention doit rester constante.

---

## Zéro stéréo

Si un futur **Stereo Z** utilise une référence zéro, celle-ci doit être explicitée.

Le symbole Z peut représenter :

axe;

état;

offset;

phase;

indice.

Nous ne devons pas laisser plusieurs sens cohabiter sans définition.

---

## Le nom Z

En mathématiques et sciences, (z) peut déjà désigner plusieurs choses :

variable complexe;

axe spatial;

impédance;

transformée en Z.

Dans Brutus, nous pouvons l’utiliser.

Mais le document doit préciser son sens local.

---

## Transformée en Z

Pour les systèmes discrets, la transformée en Z est un outil important :

[
X(z)
=
sum_{n=-infty}^{infty}
x[n]z^{-n}
]

Elle est liée à l’analyse des systèmes discrets.

Si nous appelons quelque chose « Z stéréo », nous devons éviter une confusion involontaire avec cet outil établi.

---

## Nommer clairement

Nous pouvons écrire :

**Stereo-Z_B** ou autre notation spécifique si nécessaire.

Mais le nom final viendra après la définition.

---

## Résonance et feedback

Une boucle de rétroaction peut amplifier certaines fréquences.

Dans l’audio, cela peut produire un larsen.

Dans le contrôle, certaines boucles peuvent devenir oscillantes.

La phase et le gain de boucle sont alors essentiels.

---

## Gain de boucle

Si le gain de boucle et la phase atteignent certaines conditions, une oscillation peut apparaître.

Les critères exacts relèvent de la théorie de contrôle.

Nous devons les étudier avec les outils établis.

C’est une autre raison de ne pas traiter la résonance comme un concept isolé.

---

## Le feedback peut stabiliser ou déstabiliser

Une rétroaction négative correctement conçue peut stabiliser.

Une rétroaction avec retard ou gain excessif peut déstabiliser.

La direction d’une flèche ne suffit pas.

Le temps et la phase décident.

---

## Chapitres 12, 13, 16, 17 réunis

Chapitre 12 :

**qui est connecté ?**

Chapitre 13 :

**quand ?**

Chapitre 16 :

**est-ce stable ?**

Chapitre 17 :

**à quels rythmes le système répond-il ?**

Ces quatre questions commencent à former une architecture réellement calculable.

---

## Le prochain problème

Nous savons maintenant observer des signaux.

Mais le projet Brutus ne veut pas seulement observer.

Il veut composer des modules.

Assembler des fonctions.

Créer des systèmes plus grands à partir d’objets testés.

Alors une nouvelle question apparaît :

**comment plusieurs modules fiables deviennent-ils un système fiable ?**

Le chapitre suivant devra traiter la composition.

---

## Composition

Un filtre correct.

Un oscillateur correct.

Un buffer correct.

Un synchroniseur correct.

Assemblés ensemble, ils peuvent pourtant produire un système incorrect.

Pourquoi ?

Parce que les interfaces et interactions créent de nouveaux comportements.

La composition doit donc avoir ses propres preuves.

---

## Le spectre ne suffit pas

Même si chaque module possède une réponse fréquentielle connue, leur composition peut produire :

nouvelle phase;

nouvelle latence;

nouveau gain;

nouvelle instabilité;

nouvelle saturation.

Le prochain chapitre devra construire le passage :

**module → plaque → système.**

---

## Dernière image

Le moteur tourne.

Cette fois, nous n’écoutons pas seulement le battement.

Nous enregistrons.

Nous échantillonnons.

Nous ouvrons le spectre.

Un pic apparaît.

Nous ne crions pas :

**résonance !**

Nous vérifions le sample rate.

La fenêtre.

La résolution.

Le bruit.

L’instrument.

Nous répétons.

Nous changeons l’excitation.

Le pic revient.

Nous mesurons sa largeur.

Sa phase.

Sa sensibilité.

Puis seulement, si le protocole le permet, nous écrivons :

**résonance candidate observée dans ces conditions.**

La poésie n’a pas disparu.

Elle est toujours là.

Mais maintenant elle possède un oscilloscope à côté d’elle.

Un spectre.

Une unité.

Une trace.

Et une question de plus :

comment allons-nous assembler toutes ces pièces sans perdre ce que nous venons de gagner ?

# **LA FRÉQUENCE EST MESURÉE. LA COMPOSITION VA COMMENCER.**
