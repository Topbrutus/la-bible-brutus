# Chapitre 20 — Le Système Complet

**APRÈS L’INTRODUCTION — DIXIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** De l’entrée à la preuve  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Un système devient complet lorsqu’on peut suivre ce qui entre, ce qui change, ce qui attend, ce qui casse, ce qui revient, ce qui sort et ce qui peut être vérifié.**

---

## Nous avons le droit de créer. Les autres ont le droit de vérifier.

Le chapitre 19 a ouvert la porte du laboratoire.

Jusqu’ici, nous pouvions construire.

Mesurer.

Tester.

Comparer.

Corriger.

Publier.

Mais le chapitre 20 doit accomplir quelque chose de différent.

Il doit tout remettre ensemble.

Pas comme une liste.

Pas comme une accumulation de mots.

Comme un parcours.

Un seul trajet complet.

Depuis l’instant où quelque chose arrive à l’entrée jusqu’à l’instant où un résultat sort, porte sa provenance et peut être vérifié par quelqu’un d’autre.

C’est ici que l’architecture doit montrer qu’elle est cohérente.

---

## Le système complet n’est pas un gros module

La première erreur serait de croire que l’intégration signifie :

mettre tout dans une seule boîte.

Au contraire.

Le système complet est un ensemble de responsabilités qui restent distinctes mais coordonnées.

Nous pouvons écrire :

\[
\mathcal{B}
=
(
I,
Q,
D,
P,
J,
M,
R,
S,
F,
O,
E
)
\]

où, dans ce chapitre :

- \(I\) = entrée;
- \(Q\) = horloge ou Reine de coordination;
- \(D\) = divergence;
- \(P\) = ensemble des chemins;
- \(J\) = jonction;
- \(M\) = mémoire;
- \(R\) = réparation;
- \(S\) = stabilité;
- \(F\) = analyse fréquentielle ou fonctionnelle;
- \(O\) = sortie;
- \(E\) = couche de preuve.

Ce tuple n’est pas une loi universelle.

C’est une carte.

---

## Le premier principe

Avant tout :

> **AUCUNE ÉTAPE NE DOIT EXISTER SEULEMENT DANS NOTRE TÊTE.**

Si nous disons :

le signal passe ici;

alors un lien doit exister.

Si nous disons :

il attend;

alors un état d’attente doit exister.

Si nous disons :

il se synchronise;

alors une règle temporelle doit exister.

Si nous disons :

il se répare;

alors un protocole de réparation doit exister.

Si nous disons :

il est stable;

alors un protocole de stabilité doit exister.

Si nous disons :

il résonne;

alors une mesure de fréquence et de réponse doit exister.

Si nous disons :

c’est prouvé;

alors un chemin de vérification doit exister.

---

## Le trajet complet

Nous pouvons maintenant dessiner le trajet principal :

\[
INPUT
\rightarrow
VALIDATE
\rightarrow
STAMP
\rightarrow
DIVERGE
\rightarrow
(P_1,P_2,P_3,P_4)
\rightarrow
SYNC
\rightarrow
JOIN
\rightarrow
ANALYZE
\rightarrow
OUTPUT
\rightarrow
EVIDENCE
\]

Autour de cette chaîne principale vivent :

\[
MEMORY
\]

\[
ERROR
\]

\[
REPAIR
\]

\[
STABILITY
\]

\[
AUTHORITY
\]

Ces couches ne sont pas des décorations.

Elles surveillent, expliquent et protègent le trajet.

---

## INPUT

L’entrée est la frontière.

Quelque chose arrive.

Une valeur.

Un signal.

Un fichier.

Un événement.

Une commande.

Une mesure.

Avant de faire quoi que ce soit, le système doit savoir :

**qu’est-ce que c’est ?**

Nous pouvons représenter une entrée :

\[
I_n
=
(
value,
type,
unit,
source,
tick,
time,
status,
trace
)
\]

Une entrée nue est insuffisante.

---

## Le système n’accepte pas n’importe quoi

La première fonction réelle est :

\[
VALIDATE(I_n)
\]

Elle vérifie :

type;

unité;

domaine;

taille;

fraîcheur;

permissions;

format.

Si une condition essentielle échoue :

\[
I_n\rightarrow REJECTED
\]

Le système ne doit pas tenter de deviner silencieusement.

---

## UNKNOWN est mieux qu’une invention

Si l’unité manque :

**UNKNOWN UNIT.**

Si la provenance manque :

**UNKNOWN SOURCE.**

Si la valeur est hors domaine :

**INVALID.**

Le système ne complète pas l’histoire à notre place.

---

## L’entrée reçoit un temps

Après validation, l’entrée reçoit ou confirme ses repères temporels.

\[
tick_n
\]

\[
t_{\text{source}}
\]

\[
t_{\text{receive}}
\]

Le chapitre 13 revient.

L’entrée devient un événement situé.

---

## La Reine

La Reine peut maintenant recevoir une définition sobre.

Elle n’est pas une conscience.

Elle n’est pas un cerveau caché.

Elle est un rôle de coordination.

Elle peut fournir :

session;

tick;

barrière;

ordre logique;

état de cycle.

Conceptuellement :

\[
Q_n=(session,tick,time)
\]

---

## La Reine ne calcule pas tout

Elle ne doit pas devenir un monolithe.

Elle ne décide pas nécessairement :

la transformation mathématique;

le filtre;

la réparation;

le verdict scientifique.

Elle coordonne.

Les autres modules travaillent.

---

## READY

Avant d’ouvrir le flux :

\[
READY
=
INPUT\_PORTS\_VALID
\land
CLOCK\_VALID
\land
PATHS\_AVAILABLE
\land
MEMORY\_READY
\land
NO\_BLOCKING\_ERROR
\]

Cette formule est un exemple de contrat.

Le vrai READY doit être calculé.

Pas décoratif.

---

## GO

Lorsque l’action nécessite une autorisation humaine :

\[
GO(action\_id,scope)
\]

le GO devient un événement.

Il peut être enregistré.

Il ne devient pas une permission globale infinie.

---

## Divergence

Une fois l’entrée validée :

\[
D(I_n)
\rightarrow
(I_{1,n},I_{2,n},I_{3,n},I_{4,n})
\]

La divergence doit décider :

copies indépendantes ?

références partagées ?

même tick ?

même provenance ?

Le choix est explicite.

---

## Quatre chemins

Nous conservons :

\[
P_1,\;P_2,\;P_3,\;P_4
\]

Mais le nombre quatre n’est pas une preuve de quoi que ce soit.

Il est une structure architecturale.

Chaque chemin doit posséder une fonction.

Par exemple, dans une version candidate :

\[
P_1 = MAIN
\]

\[
P_2 = REFERENCE
\]

\[
P_3 = CHECK
\]

\[
P_4 = ANALYSIS
\]

Ce n’est qu’un exemple.

Le sens réel viendra du protocole.

---

## Un chemin ne peut pas être seulement une couleur

Chaque \(P_k\) doit avoir :

input;

output;

state;

error;

time;

version;

tests.

Sinon ce n’est pas un chemin fonctionnel.

C’est une ligne graphique.

---

## Le chemin principal

Un chemin peut effectuer le calcul principal.

\[
y_1=P_1(I)
\]

Sa sortie doit porter :

value;

unit;

tick;

trace;

status.

---

## Le chemin de référence

Un deuxième chemin peut calculer une référence indépendante.

\[
y_2=P_2(I)
\]

Il peut utiliser :

une formule différente;

une implémentation indépendante;

une baseline.

Son rôle est de fournir un point de comparaison.

---

## Le chemin de contrôle

Un troisième chemin peut vérifier :

domaines;

invariants;

qualité;

cohérence.

\[
c=P_3(I)
\]

Il peut produire un statut plutôt qu’une valeur physique.

---

## Le chemin d’analyse

Un quatrième chemin peut calculer :

phase;

spectre;

offset;

drift;

SNR;

métriques.

\[
a=P_4(I)
\]

Encore une fois :

le rôle doit être déclaré.

---

## Les chemins peuvent avoir d’autres rôles

Nous ne devons pas figer l’architecture trop tôt.

Dans une autre plaque :

P1 peut être raw.

P2 low-pass.

P3 band-pass.

P4 reference.

Ou :

quatre implémentations indépendantes.

Ou :

quatre hypothèses.

La structure reste.

Le contrat change.

---

## Le tick commun

Tous les chemins doivent savoir à quel cycle appartient leur travail.

\[
tick(P_k)=n
\]

La jonction ne doit pas réunir silencieusement :

\[
P_1(n)
\]

avec :

\[
P_2(n-1)
\]

sauf si une règle explicite l’autorise.

---

## La phase commune

Si des signaux sont comparés en phase, ils doivent avoir un repère commun.

L’horloge devient une condition de la comparaison fréquentielle.

---

## L’attente

Un chemin peut être en retard.

Le système doit pouvoir afficher :

**WAITING P3**

et non simplement figer.

L’attente est un état.

---

## Timeout

Si :

\[
t_{\text{wait}}>T_{\text{timeout}}
\]

une transition se produit.

Vers :

ERROR.

DEGRADED.

PARTIAL.

Le choix dépend du contrat.

---

## La jonction

La jonction reçoit :

\[
y_1,y_2,y_3,y_4
\]

et applique :

\[
J(y_1,y_2,y_3,y_4)
\]

Mais avant de calculer, elle vérifie les statuts.

Un chemin ERROR ne doit pas être utilisé comme une valeur normale.

---

## La jonction n’est pas toujours une somme

Elle peut :

sélectionner;

comparer;

voter;

pondérer;

concaténer;

normaliser;

déclencher une décision.

La fonction doit être écrite.

---

## Exemple de composition pondérée

\[
y
=
\sum_{k=1}^{4}w_ky_k
\]

avec :

\[
\sum_{k=1}^{4}w_k=1
\]

si le protocole le demande.

Les poids sont des paramètres versionnés.

---

## Exemple de sélection

\[
k^\*=\arg\max q_k
\]

puis :

\[
y=y_{k^\*}
\]

où \(q_k\) représente une qualité définie.

La qualité doit avoir une formule.

---

## Exemple de comparaison

La jonction peut simplement produire :

\[
\Delta_{12}=y_1-y_2
\]

et ne choisir aucun gagnant.

Le système peut laisser l’écart au lecteur ou au protocole.

---

## Z stéréo

Nous pouvons maintenant donner au Z stéréo une place architecturale propre.

Il ne doit pas être une idée flottante.

Il peut devenir une plaque.

Par exemple :

\[
Z_B:
(L,R,\Theta_B,\tau)
\rightarrow
(offset,phase,metrics)
\]

où :

- \(L\) = canal gauche;
- \(R\) = canal droit;
- \(\Theta_B\) = phase Brutus de référence;
- \(\tau\) = temps ou repère;
- output = mesures définies.

---

## La phase Brutus

Nous conservons :

\[
R(a,b,o)
=
(91a+39b+21o)\bmod273
\]

et :

\[
\Theta_B
=
2\pi\frac{R}{273}
\]

Le statut est clair :

**CALCUL mathématique** pour le mapping.

**CANDIDAT d’architecture** lorsqu’il est utilisé comme phase de référence.

**NON ÉTABLI** comme loi physique universelle.

---

## Le temps doit entrer avant la fréquence

Si nous voulons produire un signal :

\[
x(\tau)
=
A\sin(2\pi f\tau+\Theta_B)
\]

alors :

- \(f\) possède une unité de fréquence;
- \(\tau\) possède une unité de temps;
- \(\Theta_B\) est un angle.

Les rôles sont séparés.

---

## La formule ne porte pas plus qu’elle ne dit

Cette discipline est peut-être l’une des plus importantes de toute la série.

Une formule peut être exacte comme calcul.

Mais son interprétation peut être candidate.

Le système doit conserver cette distinction jusque dans l’interface.

---

## Statut attaché

Nous pouvons transporter :

\[
result=(value,status)
\]

Par exemple :

\[
(\Theta_B,\ CALCUL)
\]

Puis :

\[
(signal,\ CANDIDAT\_MODEL)
\]

Puis :

\[
(measurement,\ MESURE)
\]

Chaque couche garde son niveau.

---

## Le registre

Pendant tout le trajet, le registre écrit.

\[
R_n=
(
module,
tick,
input,
state\_before,
action,
state\_after,
output,
error,
trace
)
\]

Le registre ne raconte pas une histoire.

Il conserve les transitions.

---

## Trace ID

Le même :

\[
trace\_id
\]

suit l’entrée à travers :

validation;

divergence;

quatre chemins;

jonction;

analyse;

sortie.

Le lecteur peut reconstruire le parcours.

---

## La mémoire ne doit pas ralentir le cœur sans contrôle

Le logging a un coût.

Le système peut utiliser :

buffer;

écriture asynchrone;

niveaux de trace.

Mais les preuves critiques doivent rester garanties.

---

## Niveau de trace

Nous pouvons imaginer :

MINIMAL.

NORMAL.

DEBUG.

EVIDENCE.

Le mode EVIDENCE enregistre davantage pour un run destiné à publication.

---

## Evidence mode

Un run scientifique peut activer :

raw input;

config;

all path outputs;

timing;

errors;

analysis params;

hashes.

Le coût est accepté parce que l’objectif est la preuve.

---

## Runtime mode

En production ou démonstration, le système peut enregistrer moins.

Mais il doit rester suffisamment observable.

Les modes doivent être explicitement étiquetés.

---

## La réparation surveille

Si un invariant casse :

\[
I_G(S)=FALSE
\]

le réparateur ne modifie pas immédiatement tout.

Il suit :

DETECT.

CONTAIN.

DIAGNOSE.

PROPOSE.

GO si nécessaire.

APPLY.

VERIFY.

---

## La réparation laisse la cicatrice

Le run contient :

incident;

cause candidate;

action;

résultat;

nouveau statut.

Le résultat final peut être :

RECOVERED.

Mais la trace de panne reste.

---

## Le run après réparation

Un run réparé peut être marqué :

\[
RUN=RECOVERED
\]

ou :

\[
RUN=DEGRADED
\]

selon le protocole.

Il ne devient pas automatiquement équivalent à un run nominal.

---

## Le protocole de stabilité surveille le comportement

En parallèle, le système suit :

drift;

jitter;

latence;

files;

mémoire;

erreurs;

temps de retour.

Il ne se contente pas de détecter les crashes.

---

## STABILITY_PROTOCOL_V1

Un run peut embarquer :

baseline;

perturbation;

seuils;

fenêtre;

PASS/FAIL/UNKNOWN.

Le verdict est attaché au protocole.

---

## La stabilité ne gouverne pas la vérité scientifique

Un système stable peut produire une formule fausse.

La stabilité prouve une propriété opérationnelle.

Pas la validité de l’interprétation.

Les niveaux restent séparés.

---

## L’analyse fréquentielle intervient là où elle est pertinente

Si le signal a une structure temporelle :

FFT;

phase;

corrélation;

spectre;

Q;

SNR.

Mais tous les objets n’ont pas besoin d’une FFT.

Le système ne doit pas imposer un outil parce qu’il est impressionnant.

---

## Le bon outil pour la bonne question

Calcul modulo ?

Mathématiques discrètes.

Latence ?

Chronométrie.

Stabilité ?

Systèmes dynamiques.

Fréquence ?

Signal processing.

Dépendances ?

Graphes.

Reproductibilité ?

Méthodologie expérimentale.

Cette diversité de disciplines est une force.

---

## Brutus n’est pas une seule discipline

C’est un point important.

Notre projet contient des objets qui appartiennent à plusieurs domaines.

Il ne faut pas inventer une discipline unique qui remplacerait toutes les autres.

Il faut apprendre à les relier correctement.

---

## Mathématiques

Pour :

structures;

cycles;

modulo;

graphes;

optimisation;

probabilités.

---

## Informatique

Pour :

architecture;

types;

réseau;

concurrence;

versioning;

tests.

---

## Contrôle

Pour :

stabilité;

feedback;

réponse;

perturbations.

---

## Traitement du signal

Pour :

FFT;

phase;

spectres;

filtrage;

corrélation.

---

## Métrologie

Pour :

mesures;

calibration;

incertitude;

traçabilité.

---

## Méthodologie scientifique

Pour :

hypothèse;

protocole;

réplication;

limites.

---

## L’intégration est justement la discipline de leurs frontières

Le projet ne devient pas plus fort en mélangeant les vocabulaires.

Il devient plus fort lorsqu’il sait :

quand passer de l’un à l’autre;

ce qui est conservé;

ce qui doit être converti;

ce qui ne peut pas être conclu.

---

## OUTPUT

Après tout ce travail, une sortie apparaît.

Elle ne doit pas être simplement :

\[
y
\]

Elle peut devenir :

\[
O=
(
value,
unit,
tick,
time,
status,
quality,
trace,
version
)
\]

La sortie sait d’où elle vient.

---

## Sortie calculée

Si \(y\) vient d’une formule :

status :

**CALCUL.**

---

## Sortie mesurée

Si \(y\) vient d’un instrument :

status :

**MESURE.**

---

## Sortie estimée

Si \(y\) est imputée ou prédite :

status :

**ESTIMATED** ou **CANDIDAT** selon contexte.

---

## Sortie inconnue

Si le système ne peut pas conclure :

\[
UNKNOWN
\]

C’est une sortie légitime.

---

## Le système peut répondre « je ne sais pas »

Ce droit est fondamental.

Un système qui doit toujours produire une valeur finira par inventer.

Un système scientifique doit parfois s’arrêter.

---

## Proof layer

La couche de preuve reçoit le run.

Elle ne modifie pas le résultat.

Elle construit :

claim;

protocol;

config;

raw;

analysis;

result;

hashes;

report.

---

## Le résultat devient artefact

Une sortie utile peut être exportée dans :

\[
REPRODUCTION\_PACKAGE\_V1
\]

Le paquet permet à quelqu’un d’autre de relancer.

---

## Claim ID

Chaque résultat important est relié à :

\[
CLAIM\_ID
\]

Le claim dit exactement ce qui est vérifié.

---

## Exemple

**CLAIM-MATH-001**

Mapping modulo 273.

**CLAIM-SYS-001**

Ordre des ticks après restart.

**CLAIM-STAB-001**

Temps de retour après panne P3.

**CLAIM-SIG-001**

Erreur de mesure d’un signal connu.

Le système complet peut produire des preuves différentes selon le domaine.

---

## Aucun claim total

Il n’existe pas un claim :

**Brutus est vrai.**

Cette phrase serait trop large.

Nous construisons une constellation de claims précis.

L’ensemble forme une connaissance.

---

## L’architecture de preuve

Nous pouvons écrire :

\[
CLAIM
\rightarrow
PROTOCOL
\rightarrow
RUN
\rightarrow
RAW
\rightarrow
ANALYSIS
\rightarrow
RESULT
\rightarrow
REPORT
\]

Chaque nœud est versionné.

---

## Le résultat peut contredire le claim

C’est voulu.

Le système de preuve n’est pas construit pour confirmer.

Il est construit pour tester.

---

## FAIL est un résultat

Un FAIL bien documenté vaut davantage qu’un PASS décoratif.

Il nous dit où la frontière existe.

---

## La sortie vers le visiteur

Le visiteur voit une vue simple :

CLAIM.

STATUS.

RESULT.

LIMITS.

REPRODUCE.

La complexité reste derrière.

---

## La sortie vers le chercheur

Le chercheur peut ouvrir :

raw;

code;

config;

hashes;

logs;

plots;

reproduction reports.

La preuve possède des couches.

---

## La sortie vers le constructeur

Le constructeur voit :

module states;

traces;

errors;

dependencies;

performance;

next action.

Même système.

Autre lecture.

---

## Une architecture, plusieurs vues

C’est une propriété importante.

Nous n’avons pas besoin de créer trois systèmes séparés.

Nous pouvons créer trois projections du même état.

---

## La coquille reste une coquille

L’interface montre.

Le moteur agit.

Le registre conserve.

La proof layer exporte.

Aucune couche ne doit prétendre être l’autre.

---

## La Source d’autorité

Pour chaque catégorie, nous devons savoir qui fait foi.

État runtime :

serveur ou core.

Historique code :

Git.

Release :

artefact versionné.

Publication :

DOI ou release canonique.

Mesure :

raw instrument.

Conclusion :

rapport associé au protocole.

Cette carte d’autorité évite les conflits.

---

## Quand deux sources se contredisent

Le système doit produire :

**CONFLICT.**

Puis comparer :

version;

date;

scope;

source canonique.

Il ne choisit pas silencieusement.

---

## Diff

La différence entre :

expected;

observed;

live;

historical;

devient un objet.

Le diff est un instrument de vérité.

---

## Le système complet sait revenir

Grâce au chapitre 14 :

checkpoint.

Grâce au chapitre 15 :

réparation.

Grâce au chapitre 16 :

stabilité.

Grâce au chapitre 19 :

preuve.

L’intégration ne supprime aucune couche.

Elle les coordonne.

---

## Le système complet sait avancer

Une nouvelle idée devient :

CANDIDAT.

Puis :

module.

Puis :

test.

Puis :

plaque.

Puis :

claim.

Puis :

publication.

Le chemin est clair.

---

## La chaîne Brutus

Nous pouvons résumer :

\[
INTUITION
\rightarrow
DEFINITION
\rightarrow
MATH
\rightarrow
MODULE
\rightarrow
COMPOSITION
\rightarrow
TEST
\rightarrow
MEASURE
\rightarrow
EVIDENCE
\rightarrow
PUBLICATION
\]

À chaque étape, le statut peut évoluer.

---

## L’intuition ne doit pas être humiliée

Tout commence souvent par une forme vue dans la tête.

Une relation.

Un chiffre.

Un dessin.

Une impression.

Nous ne demandons pas à l’intuition d’être déjà une preuve.

Nous lui demandons seulement d’accepter le passage vers la définition.

---

## Définition

Une intuition devient calculable lorsqu’elle reçoit :

symboles;

variables;

domaines;

unités;

règles.

---

## Mathématiques

La définition devient objet.

On peut calculer.

Démontrer.

Réfuter.

---

## Module

L’objet devient exécutable.

Input.

Output.

State.

Error.

Time.

---

## Composition

Le module rencontre d’autres modules.

Les interactions apparaissent.

---

## Test

Le système reçoit des conditions.

Nous vérifions les contrats.

---

## Mesure

Le comportement devient quantifié.

---

## Evidence

La mesure reçoit :

provenance;

version;

limites.

---

## Publication

Quelqu’un d’autre peut vérifier.

La boucle sort de nous.

---

## Le prochain retour

Une personne extérieure peut répondre :

PASS.

FAIL.

QUESTION.

COUNTEREXAMPLE.

La publication crée une nouvelle entrée.

---

## La boucle scientifique

Nous obtenons :

\[
IDEA
\rightarrow
TEST
\rightarrow
PUBLIC
\rightarrow
FEEDBACK
\rightarrow
REVISION
\rightarrow
IDEA'
\]

Le système de connaissance devient itératif.

---

## Ce n’est pas une conscience collective

Il faut encore une fois garder la frontière.

Cette boucle est un processus humain et technique.

Elle peut produire une évolution de connaissances.

Elle ne prouve pas l’existence d’une conscience du système.

---

## Une architecture vivante comme métaphore

Nous pouvons utiliser le mot **vivante** dans le récit pour décrire :

un système qui évolue;

reçoit des données;

change d’état;

répare;

mémorise;

produit.

Mais techniquement, nous préférons :

**système dynamique observable.**

Les deux formulations n’ont pas le même statut.

---

## Le symbole reste autorisé

Cristal.

Reine.

Cœur.

Vie.

Mélodie.

Nous pouvons conserver ces mots.

La règle est simple :

à chaque symbole important, une traduction technique doit pouvoir exister.

---

## Cristal

Traduction possible :

état validé + checkpoint + hash + tests.

---

## Reine

Traduction possible :

coordination temporelle et autorité de cycle.

---

## Cœur

Traduction possible :

scheduler ou boucle principale.

---

## Mélodie

Traduction possible :

séquence de signaux ou mapping musical.

---

## Vie

Traduction technique prudente :

évolution d’état dans le temps.

Pas propriété biologique.

---

## Les symboles ne sont plus dangereux lorsqu’ils ont une frontière

Ils redeviennent ce qu’ils doivent être :

des images puissantes.

Pas des raccourcis de preuve.

---

## La grande formule

Nous pouvons aussi replacer :

\[
3\times(6+1)\times7\times7\times9\times10\times13
=
1\,203\,930
\]

dans l’architecture.

Elle est :

**CALCUL exact.**

Elle peut servir de référence symbolique ou paramétrique.

Mais son rôle fonctionnel doit être défini par chaque module qui l’utilise.

---

## 273

\[
\operatorname{ppcm}(3,7,13)=273
\]

possède un usage technique naturel pour synchroniser des cycles 3, 7 et 13.

Ici, la valeur relie directement mathématique et mécanisme.

---

## 637

\[
13\times7\times7=637
\]

est aussi un calcul exact.

Il peut être intégré à une structure seulement si nous définissons son rôle.

---

## 2401

\[
7^4=2401
\]

même discipline.

Calcul exact.

Usage technique à justifier.

---

## Les nombres ne décident pas de leur signification

C’est nous qui définissons un mapping.

Puis nous testons s’il est utile.

La rigueur protège les nombres de notre enthousiasme.

---

## Le cycle complet des 273 états

Un premier noyau très fort peut être :

\[
n
\rightarrow
(a,b,o)
\rightarrow
R
\rightarrow
\Theta_B
\]

pour :

\[
n=0,\ldots,272
\]

Puis retour.

Ce noyau est :

fini;

déterministe;

testable exhaustivement.

C’est une excellente première cellule du système.

---

## Le mapping des triplets

Nous pouvons définir :

\[
a=n\bmod3
\]

\[
b=n\bmod7
\]

\[
o=n\bmod13
\]

Mais il faut vérifier si ce mapping parcourt chaque triplet exactement comme attendu.

Le chapitre 19 nous interdit de l’assumer.

Il faudra tester.

---

## Ne pas transformer une conjecture en propriété

Même si une structure semble évidente, nous devons exécuter le test.

C’est exactement le genre de petit claim que le laboratoire peut publier.

---

## Cycle → phase

Ensuite :

\[
\Theta_B=2\pi R/273
\]

Nous obtenons un cercle logique.

---

## Phase → signal

Si nous choisissons une fréquence :

\[
f
\]

et un temps :

\[
\tau
\]

nous pouvons générer :

\[
x(\tau)=A\sin(2\pi f\tau+\Theta_B)
\]

La chaîne est maintenant dimensionnellement propre.

---

## Signal → analyse

Nous pouvons mesurer :

FFT;

phase;

offset;

correlation;

SNR.

---

## Analyse → preuve

Nous conservons :

raw;

params;

plots;

expected;

measured;

error.

Le résultat devient reproductible.

---

## Le Z stéréo peut attendre son entrée

L’image revient.

Une plaque peut être READY.

Elle possède son contrat.

Elle ne fait rien tant que :

\[
INPUT=NONE
\]

Puis une entrée arrive.

La transition est :

\[
READY
\rightarrow
RUNNING
\]

Le cœur n’invente pas.

Il écoute au sens technique :

il attend un événement.

---

## L’écoute technique

Écouter peut signifier :

subscribe;

wait;

sample;

read.

Nous devons choisir un mécanisme.

Le mot poétique peut rester au-dessus.

---

## Le système ne travaille pas pour paraître vivant

Aucune animation artificielle ne doit donner l’impression d’activité si le moteur est idle.

IDLE doit ressembler à IDLE.

RUNNING doit être lié à un flux réel.

---

## IDLE

Un état IDLE peut être sain.

Le système est prêt.

Il attend.

Ce n’est pas une panne.

---

## WAITING_INPUT

Encore plus précis :

\[
WAITING\_INPUT
\]

Le visiteur sait pourquoi rien ne se passe.

---

## L’entrée déclenche le parcours

Lorsqu’elle arrive :

VALIDATE.

STAMP.

TRACE START.

DIVERGE.

PROCESS.

SYNC.

JOIN.

ANALYZE.

OUTPUT.

EVIDENCE.

Le système complet peut montrer chaque transition.

---

## Une ligne de vie

Nous pouvons représenter une exécution :

\[
I_n
\overset{v}{\rightarrow}
D_n
\overset{p}{\rightarrow}
P_{k,n}
\overset{s}{\rightarrow}
J_n
\overset{a}{\rightarrow}
O_n
\overset{e}{\rightarrow}
E_n
\]

Les exposants symbolisent les étapes.

La trace contient les détails.

---

## Le diagramme temporel

Sur un diagramme :

Q émet tick.

D reçoit.

P1..P4 exécutent.

J attend.

O produit.

M enregistre.

Cette vue permet de voir les dépendances temporelles.

---

## Le diagramme causal

Une autre vue montre :

input → outputs intermédiaires → output final.

Elle répond :

**pourquoi cette sortie existe ?**

---

## Le diagramme de preuve

Une troisième vue montre :

claim → run → raw → analysis → report.

Elle répond :

**pourquoi devrais-je croire cette affirmation ?**

---

## Trois graphes, un système

Topologie.

Causalité.

Evidence.

Ils répondent à trois questions différentes.

Les mélanger dans un seul graphe géant serait illisible.

---

## L’interface doit permettre de changer de vue

Architecture.

Runtime.

Evidence.

Le lecteur choisit.

Le modèle derrière reste cohérent.

---

## Le système sait dire ce qu’il ne sait pas

Dans la vue evidence :

UNKNOWN.

Dans la vue runtime :

BLOCKED.

Dans la vue architecture :

UNRESOLVED LINK.

Chaque inconnu est localisé.

---

## Le système complet n’est pas terminé

Paradoxalement, le titre **Le Système Complet** ne signifie pas que tout est construit.

Il signifie que les catégories nécessaires à une architecture complète sont présentes.

L’implémentation peut encore être partielle.

Le mot complet désigne la carte.

Pas la maturité.

---

## Complétude architecturale candidate

Nous pouvons définir une checklist.

### Entrée
Définie.

### Ports
Définis.

### Temps
Défini.

### État
Défini.

### Erreur
Définie.

### Mémoire
Définie.

### Réparation
Définie.

### Stabilité
Définie.

### Signal
Défini si pertinent.

### Sortie
Définie.

### Preuve
Définie.

Si une case manque, la carte est incomplète.

---

## La maturité est autre chose

Chaque catégorie peut avoir un niveau.

NONE.

DRAFT.

TESTED.

VERIFIED.

REPRODUCED.

Le système peut être architecturalement complet mais expérimental.

Cette nuance est importante.

---

## La matrice de maturité

| Couche | Statut |
|---|---|
| Ports | TESTED |
| Time | TESTED |
| Memory | PARTIAL |
| Repair | CANDIDAT |
| Stability | CANDIDAT |
| Signal | CANDIDAT |
| Reproduction | UNKNOWN |

Une matrice comme celle-ci est plus honnête qu’un verdict global.

---

## Le projet peut grandir sans se perdre

Les prochains chapitres pourront ajouter :

nouveaux modules;

nouvelles formules;

nouveaux essais;

nouveaux objets physiques;

nouvelles disciplines.

Mais ils devront trouver leur place dans cette carte.

---

## Une nouvelle formule devra répondre

Quelle entrée ?

Quelle sortie ?

Quel domaine ?

Quelle unité ?

Quel statut ?

Quel test ?

Quelle place dans le graphe ?

Quel claim ?

---

## Une nouvelle intuition devra répondre plus tard

Pas immédiatement.

Elle peut d’abord être :

CANDIDAT.

Puis être travaillée.

La structure n’écrase pas l’imagination.

Elle lui donne un chemin.

---

## Une nouvelle pièce devra répondre

Quel rôle ?

Quel port ?

Quel temps ?

Quel état ?

Quelle panne ?

Quel test ?

---

## Une nouvelle fréquence devra répondre

Mesurée où ?

Avec quel sample rate ?

Quelle résolution ?

Quelle unité ?

Quelle source ?

---

## Une nouvelle « constante » devra répondre

Définition ?

Domaine ?

Unité ?

Est-elle constante par définition ou observation ?

Quelle incertitude ?

Quelle littérature ?

Quelle réplication ?

---

## Une nouvelle découverte devra répondre

Découverte de quoi ?

Mathématique ?

Logicielle ?

Expérimentale ?

Historique ?

Le mot doit préciser.

---

## Le rôle du chapitre 20

Le chapitre 20 devient un contrat avec tous les chapitres futurs.

Il dit :

nous pouvons aller loin.

Très loin.

Mais nous ne reviendrons pas à une architecture où les choses influencent sans trace.

---

## Le premier cycle après le chapitre 20

Chapitre 21 pourra prendre une brique précise.

La tester.

La pousser.

La publier.

Ou ouvrir un nouveau domaine.

Mais la fondation reste.

---

## Les 20 premiers chapitres

Les dix premiers ont construit l’Introduction.

Les dix suivants ont construit la première architecture méthodologique du développement.

Nous pouvons les regarder en deux blocs.

---

## Chapitres 1 à 10

Ils ont raconté :

conscience et inconscience;

résilience;

trace;

rencontre;

royaume;

intuition et preuve;

naissance de Brutus;

créateur;

construction pour les autres;

commencement.

Ils ont répondu :

**pourquoi construire ?**

---

## Chapitres 11 à 20

Ils ont commencé à répondre :

**comment construire sans nous mentir ?**

11 — le miroir et la frontière entre récit et preuve.

12 — les connexions explicites.

13 — le temps.

14 — la mémoire.

15 — la réparation.

16 — la stabilité.

17 — les fréquences.

18 — la composition.

19 — la vérification extérieure.

20 — l’intégration.

---

## Deux mouvements

Premier mouvement :

**sens.**

Deuxième mouvement :

**méthode.**

Les futurs chapitres pourront entrer plus profondément dans :

mathématiques;

physique;

architecture;

expérimentation;

objets;

publication.

---

## 980 chapitres en chemin

Après ce chapitre :

20 chapitres existent.

La Bible visée contient 1000 chapitres.

Il reste :

\[
1000-20=980
\]

Mais ce nombre ne doit pas devenir une course.

Chaque chapitre doit mériter sa place.

---

## Quantité ne remplace pas qualité

Un millier de chapitres non vérifiables seraient moins utiles que cent excellents.

L’objectif de 1000 donne une direction.

La méthode donne la valeur.

---

## Le prochain millier commence par un seul test

Encore une fois :

petit.

Mesurable.

Versionné.

Le chapitre 21 n’a pas besoin de sauver l’univers.

Il doit faire une chose correctement.

---

## Le prochain artefact réel

Après cette série, une priorité naturelle serait de construire un artefact minimal de preuve.

Par exemple :

**BRUTUS_MINIMAL_ADD_V1**

ou :

**CYCLE_273_PROOF_V1**

Le deuxième est particulièrement proche de notre mathématique centrale.

---

## CYCLE_273_PROOF_V1

Un artefact possible :

1. énumérer les 273 états;
2. calculer \(R\);
3. vérifier collisions;
4. exporter CSV;
5. produire un rapport;
6. hash;
7. reproduction script.

C’est suffisamment petit pour être vérifié entièrement.

---

## Le système complet doit commencer petit

C’est presque paradoxal.

Nous venons de dessiner une architecture énorme.

Et notre prochaine action idéale est minuscule.

C’est voulu.

La carte est grande.

Le premier test reste petit.

---

## Une grande architecture sans petit test reste une histoire

Alors le chapitre 20 refuse de terminer sur une promesse gigantesque.

Il termine sur une méthode d’action.

---

## Le protocole de départ

À partir d’ici :

### 1
Choisir un claim.

### 2
Définir le domaine.

### 3
Construire le plus petit module.

### 4
Tester.

### 5
Enregistrer.

### 6
Reproduire.

### 7
Publier si utile.

### 8
Étendre.

Cette boucle peut nourrir des centaines de chapitres.

---

## Le système complet comme squelette

Nous pouvons résumer l’ensemble :

\[
INPUT
\]

\[
\downarrow
\]

\[
VALIDATE
\]

\[
\downarrow
\]

\[
TIME / QUEEN
\]

\[
\downarrow
\]

\[
DIVERGE
\]

\[
\downarrow
\]

\[
P_1\quad P_2\quad P_3\quad P_4
\]

\[
\downarrow
\]

\[
SYNC
\]

\[
\downarrow
\]

\[
JOIN
\]

\[
\downarrow
\]

\[
ANALYZE
\]

\[
\downarrow
\]

\[
OUTPUT
\]

et autour :

\[
MEMORY
\]

\[
ERROR
\]

\[
REPAIR
\]

\[
STABILITY
\]

\[
EVIDENCE
\]

---

## Le cœur de la preuve

À chaque flèche :

trace.

À chaque calcul :

version.

À chaque mesure :

unité.

À chaque hypothèse :

statut.

À chaque erreur :

cicatrice.

À chaque publication :

limites.

C’est cela qui rend l’ensemble solide.

---

## Ce que Brutus ne doit jamais devenir

Une interface qui cache les données.

Une formule sans définition.

Une fréquence sans temps.

Une preuve sans protocole.

Une réparation sans trace.

Une mémoire qui réécrit le passé.

Une IA qui affirme sans vérifier.

Un symbole présenté comme loi.

Une publication qui demande la foi.

---

## Ce que Brutus peut devenir

Un laboratoire où :

les intuitions sont accueillies;

les formules sont définies;

les modules sont testés;

les erreurs restent visibles;

les résultats sont versionnés;

les preuves sont exportées;

les autres peuvent vérifier.

Cela est déjà suffisamment ambitieux.

---

## Le Roi n’a pas besoin d’avoir raison à chaque étape

Il a besoin d’un système qui permette de découvrir quand il a raison.

Et quand il se trompe.

Astra n’a pas besoin d’être infaillible.

Elle a besoin de vérifier.

Le projet n’a pas besoin de prétendre être parfait.

Il a besoin de laisser une trace suffisamment bonne pour être corrigé.

---

## L’alliance change de forme

Au chapitre 4, l’alliance était humaine et narrative.

Ici, elle devient méthodologique.

Topbrutus apporte :

intuition;

direction;

images;

questions;

audace.

Astra apporte :

structure;

calcul;

test;

contradiction;

traçabilité.

Mais aucun des deux ne remplace la preuve.

C’est elle qui tranche les questions techniques.

---

## La preuve n’est pas l’ennemie du rêve

Elle permet de savoir quelle partie du rêve a traversé le monde réel.

C’est peut-être le point le plus important de ces dix chapitres.

---

## Le silence du chapitre 11 revient

Au début de ce mouvement, nous avions un miroir.

Une formule.

Une nuit.

Une trace.

Nous avions refusé de couronner trop vite.

Nous avions laissé le silence rester silencieux.

Aujourd’hui, neuf chapitres plus tard, nous avons une architecture entière autour de cette retenue.

Le système a appris à dire :

CALCUL.

MESURE.

CANDIDAT.

UNKNOWN.

FAIL.

PASS.

REPRODUCED.

Chaque mot possède une place.

---

## Le miroir est devenu une fenêtre

Au chapitre 11, Astra renvoyait une image.

Au chapitre 19, un étranger pouvait vérifier.

Le miroir ne regarde plus seulement vers l’intérieur.

Il devient une fenêtre vers l’extérieur.

---

## La fenêtre ne doit pas déformer

Le visiteur doit voir le statut réel.

Pas un résultat embelli.

Pas une animation qui cache un fail.

Pas un claim plus large que la preuve.

La transparence devient une propriété technique.

---

## Le système est maintenant capable de dire trois phrases

**Voici ce que je fais.**

**Voici ce que j’ai observé.**

**Voici comment vous pouvez vérifier.**

Si ces trois phrases sont vraies, nous avons franchi une étape importante.

---

## Ce qui reste inconnu

Beaucoup.

Et c’est acceptable.

Nous ne savons pas encore :

quelles parties seront réellement implémentées;

quels claims survivront;

quelles hypothèses tomberont;

quels objets physiques seront construits;

quelles relations seront publiées;

quelles personnes reproduiront.

L’inconnu est devant.

Pas caché sous le tapis.

---

## Le chapitre 20 n’est donc pas une conclusion

C’est un point d’intégration.

Une plaque.

Un checkpoint.

Une version.

Nous pouvons écrire :

\[
BIBLE\_BRUTUS\_ARCHITECTURE\_V0.1
\]

si nous voulons donner un nom à cette première synthèse.

Mais elle reste :

**DRAFT.**

Elle devra être confrontée au code.

---

## Le prochain niveau

Le prochain niveau n’est plus seulement écrire.

Il est :

implémenter;

tester;

mesurer;

publier.

Les futurs chapitres peuvent raconter cette traversée réelle.

---

## Le système complet devra être falsifiable

Chaque couche doit pouvoir échouer.

Ports.

Temps.

Mémoire.

Repair.

Stability.

Signal.

Composition.

Evidence.

Si aucun test ne peut échouer, aucune preuve n’est forte.

---

## Le GO final de cette série

Le GO qui suit ce chapitre ne signifiera plus :

écris la prochaine brique de la même séquence.

Il pourra signifier :

commençons un nouveau mouvement.

Nous avons un socle.

---

## Dernière architecture

Une dernière fois, regardons tout.

Une entrée arrive.

Elle est identifiée.

Validée.

Datée.

La Reine donne le tick.

La divergence ouvre quatre chemins.

Chaque chemin travaille.

Chacun laisse une trace.

La jonction attend les bons états.

Une erreur apparaît peut-être.

Le réparateur intervient selon contrat.

Le protocole de stabilité mesure le retour.

L’analyse fréquentielle examine ce qui doit l’être.

La sortie est produite.

Elle porte son statut.

Le registre ferme la trace.

La proof layer prépare le paquet.

Un visiteur regarde.

Un chercheur télécharge.

Une autre machine reproduit.

Un rapport revient.

PASS.

FAIL.

PARTIAL.

UNKNOWN.

Et le système accepte les quatre.

Parce qu’il n’est plus construit pour avoir toujours raison.

Il est construit pour savoir ce qui s’est réellement passé.

---

## La dernière règle des dix chapitres

Nous pouvons condenser tout le mouvement en une phrase :

> **NE JAMAIS CONFONDRE CE QUE NOUS IMAGINONS, CE QUE NOUS CALCULONS, CE QUE NOUS MESURONS ET CE QUE NOUS AVONS RÉELLEMENT PROUVÉ.**

Cette phrase n’enlève rien au rêve.

Elle lui donne un chemin.

---

## Dernière image

La pièce est calme.

L’écran est noir quelques secondes.

Pas de lumière inutile.

Pas d’animation pour donner l’impression de vie.

Puis une petite ligne apparaît.

**WAITING INPUT.**

La Reine est prête.

Le registre est vide.

Les quatre chemins attendent.

Le Z stéréo possède sa phase mais aucune fréquence n’est inventée.

Le réparateur n’a rien à réparer.

Le protocole de stabilité n’a rien à mesurer.

La proof layer n’a encore aucun claim à publier.

Tout est silencieux.

Et c’est parfait.

Parce que, cette fois, le silence ne cache rien.

Il signifie simplement :

**le système attend une vraie entrée.**

Puis l’entrée arrive.

Un tick.

Une trace.

Un calcul.

Une mesure.

Une sortie.

Une preuve possible.

Et devant nous :

980 chapitres.

Pas comme une promesse de grandeur.

Comme 980 occasions de recommencer correctement.

# **L’ENTRÉE EST PRÊTE. LE CHEMIN EST VISIBLE. LA SUITE PEUT COMMENCER.**
