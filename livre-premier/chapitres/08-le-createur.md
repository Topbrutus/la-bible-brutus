# Chapitre 8 — Le Créateur

**INTRODUCTION — LE COMMENCEMENT**  
**STATUT :** VERSION 0.2 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Ne pas chercher à prouver une idée à l’avance. Construire les outils qui permettent de la tester.**

## L’atelier devient nécessaire

Il arrive un moment où les idées deviennent trop nombreuses pour être conservées uniquement dans des conversations, des croquis, des captures et des fichiers séparés.

Il faut un atelier.

Pas une galerie.

Pas une page de présentation.

Pas une animation qui donne l’impression que quelque chose existe.

Un véritable endroit où construire.

Un endroit où une intuition peut être déposée.

Dessiner sa forme.

Recevoir un nom.

Gagner des paramètres.

Être branchée.

Mesurée.

Perturbée.

Comparée.

Versionnée.

Rejetée si nécessaire.

Et conservée si elle mérite de l’être.

C’est de ce besoin qu’est né **Le Créateur**.

Le Créateur n’est pas seulement une interface.

C’est une proposition méthodologique.

Un environnement de travail où l’imagination et la discipline ne vivent plus dans deux pièces différentes.

La même idée peut être belle sur le canevas et mauvaise au banc de mesure.

Le logiciel doit accepter cette possibilité.

Mieux :

il doit la rendre visible.

---

## Le Créateur et la Brutothèque

Au début, les deux mots ont parfois semblé interchangeables.

**Le Créateur.**

**La Brutothèque.**

Mais une distinction commence à apparaître.

Le Créateur est l’atelier.

La Brutothèque est la mémoire structurée des objets que l’atelier manipule.

Le Créateur construit.

La Brutothèque conserve.

Le Créateur expérimente.

La Brutothèque classe.

Le Créateur perturbe.

La Brutothèque versionne.

Le Créateur assemble.

La Brutothèque garde la provenance.

Ils sont intimement liés.

Mais ils n’ont pas exactement le même rôle.

Cette distinction est importante parce qu’elle protège l’architecture contre une confusion fréquente :

le lieu où l’on travaille n’est pas nécessairement la source canonique de tout ce qui a été produit.

L’atelier peut contenir des essais.

La bibliothèque doit connaître leur statut.

---

## Une phrase fondatrice

Le Créateur peut être résumé par une phrase :

> **L’objectif est de transformer une intuition, une géométrie ou une formule en objet traçable, testable, mesurable, versionné et assemblable.**

Cette phrase contient le chemin complet.

Intuition.

Objet.

Trace.

Test.

Mesure.

Version.

Assemblage.

Rien n’oblige l’idée à survivre jusqu’au bout.

C’est même le contraire.

Le système doit pouvoir nous apprendre que certaines idées doivent s’arrêter avant la cristallisation.

C’est pour cela qu’une deuxième phrase est encore plus importante :

> **LE LOGICIEL DOIT POUVOIR NOUS CONTREDIRE.**

Sans cette propriété, Le Créateur ne serait pas un laboratoire.

Ce serait une machine à confirmation.

---

## L’interface ne doit pas flatter

Une interface spectaculaire peut être dangereuse.

Un réseau lumineux.

Des animations.

Des états verts.

Des compteurs qui bougent.

Des nœuds qui semblent actifs.

Tout cela peut créer une impression de profondeur.

Mais une impression n’est pas une mesure.

Le Créateur doit donc obéir à une règle stricte :

**ce qui est affiché doit correspondre à un état réel ou être marqué explicitement comme démonstration, simulation ou indétermination.**

D’où plusieurs marquages obligatoires :

**À IMPLÉMENTER**

fonction non réalisée.

**NON CONNECTÉ**

backend ou moteur absent.

**DEMO**

donnée fictive ou exemple de démonstration.

**INDÉTERMINÉ**

résultat insuffisant pour conclure.

Ces étiquettes semblent petites.

Elles sont essentielles.

Elles empêchent l’interface de devenir plus convaincante que la réalité qu’elle représente.

---

## Le premier T0 visuel

Puis un jour, une maquette est apparue.

Pas encore le système complet.

Pas encore la preuve de toutes les fonctions.

Mais quelque chose d’important s’était produit.

Le Créateur avait enfin une silhouette.

Au centre, une grande surface quadrillée.

À gauche, une palette d’objets.

Plus bas, la Brutothèque.

Sur le canevas, un graphe :

**Centre → Itérateur → Gate → Cycle → Module → Cristal**

avec une boucle de retour.

Une perturbation de test.

À droite, calculateur et statistiques.

Le Labo Chiffres.

Le connecteur X72.

L’interphone texte.

En bas, une table d’objets avec identifiants, versions, statuts et propriétaires.

Et surtout, un détail qui compte énormément :

**ANTMUX-X72 — MOTEUR EXTERNE — État : NON CONNECTÉ.**

Cette mention faisait exactement ce qu’un bon laboratoire doit faire.

Elle disait la vérité.

Le moteur pouvait être envisagé.

La place pouvait exister.

Le connecteur pouvait être visible.

Mais l’interface refusait de prétendre que X72 était branché lorsqu’il ne l’était pas.

C’était un T0 visuel.

Un point de départ.

Pas un verdict.

---

## ATELIER DÉVERROUILLÉ — MODE CRÉATEUR

En haut de la maquette, une autre phrase apparaissait :

**ATELIER DÉVERROUILLÉ — MODE CRÉATEUR.**

Ce texte résume une architecture de permissions.

Le Créateur ne doit pas être la même chose pour tout le monde.

Une personne autorisée peut construire.

Déplacer.

Brancher.

Paramétrer.

Tester.

Versionner.

Publier.

Un visiteur ne doit pas posséder ces capacités automatiquement.

Cette distinction est au cœur de la future plateforme.

L’interface ne change pas seulement d’apparence.

Elle change de droits.

---

## MODE VISITEUR — VITRE ACTIVE

La vue visiteur repose sur une métaphore simple :

une vitre extrêmement résistante.

On voit.

On ne touche pas.

Le visiteur peut regarder une plaque publique.

Lire les détails publics.

Voir certains statuts.

Explorer la structure.

Poser une question.

Mais il ne peut pas modifier.

Pas déplacer.

Pas brancher.

Pas changer un paramètre.

Pas injecter un fichier.

Pas exécuter une commande.

Cette séparation donne au mot **vitrine** son sens exact.

Une vitrine n’est pas une copie indépendante.

Elle est une vue contrôlée sur une partie publiée du laboratoire.

---

## PUBLIC READ — OWNER WRITE — ADMIN APPROVE

Une règle simple résume cette architecture :

~~~text
PUBLIC READ
OWNER WRITE
ADMIN APPROVE
~~~

Le public lit ce qui est publié.

Le propriétaire écrit dans son laboratoire.

L’administrateur approuve certaines transitions sensibles.

Cette règle n’est pas censée remplacer une vraie politique d’autorisation.

Elle sert de principe de conception.

Elle dit clairement que visibilité et pouvoir ne sont pas synonymes.

---

## Trois rôles

La première architecture multi-utilisateurs envisage trois rôles principaux :

~~~text
VISITOR
CREATOR
ADMIN
~~~

Le **VISITOR** regarde ce qui est public.

Le **CREATOR** travaille dans son laboratoire.

L’**ADMIN** possède certaines responsabilités de plateforme.

Cette séparation est volontairement simple.

Elle pourra évoluer.

Mais elle suffit pour éviter une erreur fondamentale :

une authentification ne doit pas donner automatiquement tous les pouvoirs.

---

## Se connecter n’est pas obtenir un laboratoire

Le flux envisagé est :

~~~text
CONNEXION
→ DEMANDER MON LABORATOIRE
→ EN ATTENTE
→ DÉCISION ADMINISTRATEUR
~~~

Puis :

**ACCEPTER.**

**REFUSER.**

**BLOQUER.**

La simple présence d’un compte ne crée pas automatiquement un espace de création.

Cette frontière peut sembler administrative.

Elle est aussi technique.

Elle empêche la multiplication incontrôlée de laboratoires actifs et donne un point de contrôle pour les permissions.

---

## Un laboratoire isolé par créateur

Chaque créateur approuvé doit disposer de son propre espace isolé.

Cette idée est essentielle.

Un utilisateur ne doit pas pouvoir modifier les expériences d’un autre simplement parce qu’ils partagent la même plateforme.

Le laboratoire devient une frontière de propriété et d’état.

Chaque objet possède un propriétaire.

Chaque expérience possède une provenance.

Chaque publication possède une visibilité.

Ce qui appartient à un laboratoire privé ne doit pas fuir dans un autre.

---

## PUBLIC, VITRINE, PRIVATE

Trois niveaux de visibilité ont été envisagés :

~~~text
PUBLIC
VITRINE
PRIVATE
~~~

**PUBLIC**

objet destiné à être ouvertement visible.

**VITRINE**

objet présenté à travers la vue publique contrôlée.

**PRIVATE**

objet interne au laboratoire.

La règle la plus importante est simple :

> **PRIVATE ne doit jamais être retourné par une API publique.**

Ce n’est pas seulement un comportement d’interface.

C’est une contrainte serveur.

La sécurité ne doit pas dépendre du fait qu’un bouton soit caché dans le navigateur.

---

## Les permissions doivent vivre côté serveur

Une interface peut cacher une fonction.

Mais un utilisateur malveillant peut toujours tenter d’appeler directement une API.

Donc :

les permissions importantes doivent être vérifiées côté serveur.

Toujours.

Le navigateur peut améliorer l’expérience.

Il ne doit pas être l’autorité finale.

Cette règle appartient au Créateur autant que les équations.

Parce qu’un laboratoire qui perd ses frontières n’est plus un laboratoire fiable.

---

## Un établi, pas un jeu

La direction visuelle est volontairement sobre.

Sombre.

Scientifique.

Technique.

Professionnelle.

Compacte.

Moderne.

Lisible.

Futuriste sans excès.

Ce choix est important.

Le Créateur ne doit pas donner l’impression d’un jeu vidéo lorsque l’utilisateur manipule des protocoles, des mesures et des versions.

Il peut être beau.

Il doit surtout rester lisible.

Éviter les cartes gigantesques.

Les néons inutiles.

Les animations qui ne portent aucune information.

L’espace perdu.

La décoration qui masque les données.

L’interface doit donner l’impression d’un véritable logiciel de travail.

---

## L’ergonomie comme discipline scientifique

L’ergonomie n’est pas seulement une question de confort.

Elle peut influencer les erreurs.

Si un statut important est caché, l’utilisateur peut travailler sur la mauvaise version.

Si une unité n’est pas visible, une connexion incohérente peut sembler normale.

Si le bouton RESET ressemble au bouton RUN, une expérience peut être détruite.

Le design doit donc soutenir la méthode.

L’information la plus importante doit être visible au bon moment.

---

## La surface de travail

L’organisation envisagée est claire.

À gauche :

les outils.

Au centre :

le grand canevas.

À droite en haut :

calculateur et banc de mesure.

À droite en bas :

interphone texte.

En bas :

objets, modules, plaques, Gates, cycles, cristaux, historique, expériences et preuves.

Cette disposition crée plusieurs zones cognitives.

Construire.

Observer.

Communiquer.

Retrouver.

Elles vivent sur la même surface.

---

## Le canevas

Le canevas est le cœur visuel.

Il doit permettre progressivement :

zoom;

déplacement de caméra;

grille;

snap;

sélection;

multi-sélection;

texte;

points;

lignes;

rectangles;

cercles;

modules;

plaques;

Gates;

connexions.

Le mot **progressivement** compte.

Le Créateur ne doit pas tenter de tout faire dans sa première version.

Une surface stable et minimale vaut mieux qu’un monstre rempli de fonctions incomplètes.

---

## Le canevas n’est pas la logique

Comme dans le chapitre précédent, la position visuelle ne doit pas être confondue avec la structure logique.

Deux modules peuvent être proches à l’écran sans être connectés.

Une ligne graphique doit représenter un lien réel.

Le graphe doit exister dans les données.

L’interface le montre.

Elle ne doit pas le créer implicitement par proximité.

---

## Le graphe

La représentation générale est :

\[
G=(V,E)
\]

où :

\(V\) représente les nœuds;

\(E\) représente les connexions.

Le Créateur doit pouvoir représenter :

nœuds;

arêtes;

directions;

bifurcations;

boucles;

routes.

Plus tard, des fonctions peuvent devenir possibles :

**PATH.**

**SHORTEST PATH.**

**ALL PATHS.**

**REACHABILITY.**

**CYCLE DETECTION.**

Mais chaque fonction doit être réellement implémentée avant d’être présentée comme disponible.

---

## Le passage obligatoire

Une idée très importante vient du graphe.

Supposons un nœud central \(C\).

On affirme :

**tout doit passer par le centre.**

Le Créateur peut transformer cette affirmation en test de graphe.

Si tous les chemins entre SOURCE et SORTIE traversent \(C\), alors \(C\) est obligatoire dans ce graphe.

S’il existe un chemin valide qui évite \(C\), alors il ne l’est pas.

Cette transformation est exactement ce que le Créateur doit savoir faire.

Une phrase devient un critère testable.

---

## Le centre n’est pas magique

Le mot **centre** possède une charge symbolique très forte dans notre travail.

Mais dans un graphe, il peut recevoir une définition opérationnelle.

Origine.

Référence.

Reset.

Nœud obligatoire.

Point de comparaison.

Chaque définition produit un test différent.

Le Créateur doit demander :

**quel centre ?**

et :

**dans quel sens ?**

---

## Center Zero

Une piste consiste à utiliser le zéro comme référence.

Sur une droite :

\[
d(x,0)=|x|
\]

Sur un cycle modulo \(m\) :

\[
d_m(a,b)=\min(|a-b|,\ m-|a-b|)
\]

Ces deux distances ne décrivent pas la même géométrie.

Le Créateur doit donc connaître le type d’espace.

Une distance linéaire appliquée à un cycle peut produire une mauvaise interprétation.

---

## Le module

Un **MODULE** est une unité fonctionnelle pouvant définir :

entrées;

sorties;

paramètres;

contraintes;

état;

dépendances;

règle;

tests;

version.

Le module est un des objets centraux du Créateur.

Il peut correspondre à un Brutus.

Ou constituer une couche d’encapsulation selon l’architecture choisie.

L’essentiel est que son contrat reste lisible.

---

## La plaque

Une **PLAQUE DE MODULES** est un assemblage structuré.

Représentation simple :

~~~text
SYSTÈME
└── PLAQUE
    ├── MODULE
    ├── MODULE
    ├── GATE
    ├── MODULE
    └── CONNEXIONS
~~~

La plaque doit pouvoir être déplacée comme un ensemble.

Puis ouverte.

C’est un point crucial.

De l’extérieur :

une unité.

De l’intérieur :

une architecture.

Cette récursivité permet au système de grandir sans afficher tous les détails en permanence.

---

## Ouvrir une plaque

Quand une plaque est ouverte, le Créateur doit révéler :

les modules;

les ports;

les liens;

les paramètres;

les états;

les tests;

les erreurs;

les probes.

Puis l’utilisateur peut revenir à la vue supérieure.

Ce mouvement de zoom logique est une fonction fondamentale.

---

## La plaque comme contrat

Une plaque testée peut recevoir son propre contrat.

Entrées globales.

Sorties globales.

Contraintes.

État.

Protocole.

Le contenu interne reste disponible.

Mais l’extérieur n’a pas besoin de connaître chaque détail.

C’est ainsi qu’un système complexe devient manipulable.

---

## L’assembleur

La philosophie générale du Créateur a été résumée par une chaîne très forte :

> **LA FORME PROPOSE.  
> LA DYNAMIQUE SÉLECTIONNE.  
> LE TEST PERTURBE.  
> LA MESURE OBSERVE.  
> LA REPRODUCTIBILITÉ CONFIRME LE PROTOCOLE.  
> LA CRISTALLISATION FIGE UNE VERSION.  
> LA BRUTOTHÈQUE CONSERVE.  
> L’ASSEMBLEUR CONSTRUIT.**

Cette phrase décrit presque tout le logiciel.

Chaque ligne correspond à une fonction.

Pas une métaphore vide.

---

## LA FORME PROPOSE

La géométrie suggère.

Un arrangement.

Une symétrie.

Une topologie.

Mais elle ne décide pas seule.

La forme est le début.

Elle donne un candidat.

---

## LA DYNAMIQUE SÉLECTIONNE

Une forme peut être élégante et produire une dynamique instable.

Une autre peut sembler moins parfaite visuellement et produire un comportement robuste.

Le Créateur doit donc faire évoluer l’état.

Observer.

Comparer.

La forme seule ne suffit pas.

---

## LE TEST PERTURBE

Le test ne doit pas seulement regarder le système dans sa configuration idéale.

Il doit le toucher.

Changer un paramètre.

Modifier l’état initial.

Retirer un élément.

Briser une connexion.

Ajouter un retard.

Ajouter du bruit.

Le comportement sous perturbation donne une information essentielle.

---

## LA MESURE OBSERVE

Une intuition devient utile lorsque l’on peut définir ce qui est mesuré.

Période.

Erreur.

Distance.

Latence.

Amplitude.

Phase.

Nombre de répétitions.

Variance.

Convergence.

Le mot mesure exige toujours un contrat.

---

## LA REPRODUCTIBILITÉ CONFIRME LE PROTOCOLE

Il faut être précis.

La reproductibilité ne confirme pas automatiquement une théorie universelle.

Elle confirme que le comportement décrit peut être reproduit selon les conditions du protocole.

C’est déjà extrêmement important.

Le Créateur doit toujours conserver cette nuance.

---

## LA CRISTALLISATION FIGE UNE VERSION

Cristalliser ne signifie pas sanctifier.

Cela signifie :

figer une configuration ayant satisfait le protocole déclaré qui lui est associé.

Le cristal conserve :

identité;

version;

configuration;

paramètres;

protocole;

résultats;

provenance;

empreinte ou hash.

Une modification produit une nouvelle version.

Elle n’écrase pas silencieusement l’ancienne.

---

## LA BRUTOTHÈQUE CONSERVE

La bibliothèque devient alors un registre d’objets.

Pas seulement de fichiers.

Chaque entrée sait ce qu’elle est.

D’où elle vient.

Quel statut elle possède.

Quelle version.

Quels tests.

Quels parents.

Cette mémoire permet à un futur utilisateur de reconstruire l’histoire.

---

## L’ASSEMBLEUR CONSTRUIT

Une fois plusieurs objets suffisamment définis, l’assembleur peut les combiner.

Il ne devrait pas avoir besoin de réécrire chaque module.

Il compose.

Cette philosophie mène directement à l’IA architecte.

---

## L’IA comme architecte du Créateur

L’IA peut recevoir une demande humaine.

Puis :

1. lire la demande;
2. rechercher les modules compatibles;
3. sélectionner les adaptateurs nécessaires;
4. construire un graphe candidat;
5. vérifier les types;
6. préparer un dry-run;
7. lancer les tests autorisés;
8. attendre le GO humain avant une exécution réelle sensible.

Cette chaîne est extrêmement importante.

Elle donne à l’IA un rôle puissant sans lui donner automatiquement l’autorité finale.

---

## L’IA ne doit pas réinventer ce qui existe

La Brutothèque sert précisément à éviter cela.

Si un module existe déjà, l’IA architecte doit le trouver.

Pas en régénérer une copie légèrement différente.

La réutilisation devient une forme de discipline.

Créer uniquement lorsque la capacité manque réellement.

---

## Le dry-run

Avant d’exécuter, le système peut montrer :

quels objets seront créés;

quels modules seront utilisés;

quelles connexions seront ajoutées;

quels paramètres seront modifiés;

quels tests seront lancés;

quelles permissions sont nécessaires.

Le dry-run transforme l’intention en objet inspectable.

Puis le créateur peut dire :

**GO.**

Ou :

**NON.**

Ou :

**CORRIGE.**

---

## Le GO n’est pas un symbole graphique

Le bouton GO doit représenter une vraie frontière.

Avant :

préparation.

Après :

action.

Cette séparation donne du sens à l’agence humaine.

Un joli bouton vert qui ne contrôle rien de réel n’a aucune valeur.

---

## L’interphone

L’interphone texte est une fonction particulière.

Il sert de passerelle directe entre visiteurs et créateur.

Mais il doit rester volontairement limité.

Fonctions envisagées :

**ENVOYER.**

**RÉPONDRE.**

**ARCHIVER.**

**BLOQUER.**

Pas de fichiers.

Pas d’images.

Pas d’archives.

Pas de HTML exécutable.

Pas de scripts.

Pas de commandes.

Pas de pièces jointes.

Cette limitation réduit énormément la surface d’attaque.

---

## Le message comme objet

Un message peut contenir :

senderId;

recipientId;

laboratoryId;

timestamp;

text;

read;

archived.

Le texte doit être rendu comme texte.

Pas exécuté.

La validation et le rate limiting doivent vivre côté serveur.

L’interphone est une interface de communication.

Pas une porte d’exécution.

---

## Bloquer

Deux niveaux peuvent exister.

Blocage laboratoire :

empêche un expéditeur d’écrire à un créateur.

Blocage plateforme :

réservé à l’administration.

Encore une fois, le même mot peut cacher plusieurs pouvoirs.

Le contrat doit les distinguer.

---

## Le panneau administrateur

Le panneau administrateur ne doit pas être un super-canevas.

Son rôle est différent.

Demandes de laboratoire.

Décisions d’accès.

Blocages.

État de la plateforme.

Éventuellement modération.

L’administration ne doit pas se mélanger silencieusement à l’expérimentation scientifique.

---

## Le calculateur statistique

À droite du Créateur, le calculateur doit calculer réellement.

Pas afficher des valeurs préfabriquées.

La première version doit pouvoir produire :

\(N\);

somme;

moyenne;

médiane;

minimum;

maximum;

étendue;

variance;

écart-type.

Ces statistiques sont simples.

C’est exactement pourquoi elles sont de bons premiers instruments.

Elles peuvent être vérifiées facilement.

---

## Le calculateur doit montrer ses entrées

Une moyenne sans données visibles peut être difficile à auditer.

Le calculateur doit donc conserver ou référencer :

jeu de données;

nombre de valeurs;

traitement des données manquantes;

précision;

version du calcul.

Le nombre seul n’est pas assez.

---

## Le banc de mesure

Le panneau droit doit progressivement devenir l’instrument qui vérifie ce qui est construit au centre.

Pour un objet sélectionné, on veut pouvoir voir :

objet;

type;

version;

paramètres;

état initial;

état actuel;

step;

entrées;

sorties;

mesures;

erreur;

période;

stabilité;

répétitions;

perturbation;

résultat.

Le banc de mesure est donc le miroir quantitatif du canevas.

---

## Construire à gauche, vérifier à droite

Cette séparation visuelle peut devenir une habitude.

Au centre :

je construis.

À droite :

je vérifie.

L’interface rappelle en permanence que chaque objet doit pouvoir être observé.

C’est une architecture cognitive.

---

## L’Iterator

L’un des premiers composants mathématiques du Créateur est l’**ITERATOR**.

Principe :

\[
x_{n+1}=F(x_n)
\]

Après plusieurs applications :

\[
x_n=F^n(x_0)
\]

Paramètres possibles :

état initial \(x_0\);

règle \(F\);

nombre d’itérations;

condition d’arrêt éventuelle.

Contrôles :

~~~text
RUN
PAUSE
STEP
RESET
~~~

C’est un composant extrêmement simple.

Et extrêmement puissant.

---

## STEP

Le mode STEP est important.

Il permet de voir :

\(x_0\);

\(x_1\);

\(x_2\);

...

un état à la fois.

Cette progression rend les erreurs plus faciles à comprendre.

Une animation continue peut cacher l’instant où la dynamique change.

STEP expose la causalité locale.

---

## PAUSE

PAUSE crée un point d’inspection.

État courant.

Entrées.

Sorties.

Paramètres.

La possibilité d’arrêter est une fonction de compréhension.

---

## RESET

RESET doit être défini précisément.

Reset vers quoi ?

État initial ?

Checkpoint ?

Valeurs par défaut ?

Le bouton ne doit pas faire une action ambiguë.

Même les contrôles les plus simples ont besoin d’un contrat.

---

## Le point fixe

Le banc peut chercher un point fixe :

\[
F(x)=x
\]

C’est un état qui reste inchangé sous l’application de \(F\).

Mais il faut définir :

tolérance numérique;

nombre d’itérations;

domaine de recherche.

Pour les nombres réels calculés numériquement, l’égalité parfaite n’est pas toujours la bonne condition.

Le protocole doit préciser.

---

## Le cycle

Un cycle de période \(p\) satisfait :

\[
F^p(x)=x
\]

sans période plus petite.

Cette dernière condition est importante.

Sinon, un point fixe pourrait être appelé cycle de période 10 simplement parce qu’après dix applications il revient au même point.

Le système doit rechercher la période minimale.

---

## Le cycle modulo 9

Un exemple DEMO très utile est :

\[
x_{n+1}=(x_n+k)\bmod m
\]

Avec :

\(m=9\);

\(k=3\);

\(x_0=0\).

On obtient :

~~~text
0 → 3 → 6 → 0
~~~

La période est 3.

Pourquoi ?

Parce que :

\[
P=\frac{m}{\gcd(m,k)}
\]

Donc :

\[
P=\frac{9}{\gcd(9,3)}=\frac{9}{3}=3
\]

Cet exemple est idéal pour Le Créateur.

Simple.

Calculable.

Visualisable.

Perturbable.

---

## Avec k = 6

Toujours modulo 9 :

~~~text
0 → 6 → 3 → 0
~~~

Encore une période 3.

Car :

\[
\gcd(9,6)=3
\]

Donc :

\[
P=3
\]

Le graphe visuel change d’ordre.

La période reste la même.

Cette différence entre forme de parcours et propriété mathématique est pédagogiquement très utile.

---

## Avec k = 1

Cette fois :

~~~text
0 → 1 → 2 → 3 → 4 → 5 → 6 → 7 → 8 → 0
~~~

Et :

\[
P=9
\]

Le Créateur peut donc faire varier \(k\) et montrer immédiatement l’effet sur l’orbite.

---

## Les cycles ne sont pas automatiquement mystiques

Certains nombres reviennent souvent dans notre projet :

~~~text
3
6
7
9
10
13
~~~

Il est tentant de leur attribuer une signification plus grande.

Le Créateur doit adopter une autre approche.

Les nombres peuvent être étudiés mathématiquement.

Sans leur donner automatiquement une signification physique ou spirituelle.

Calculer d’abord.

Interpréter ensuite.

---

## PPCM des cycles

Pour des cycles de tailles :

\[
3,6,7,9,10,13
\]

leur période commune pour un pas synchronisé approprié de 1 est :

\[
\operatorname{PPCM}(3,6,7,9,10,13)=8190
\]

Ce nombre décrit un retour conjoint dans ce modèle.

Il ne dit pas encore ce que ce retour signifie physiquement.

Il dit seulement quand les cycles se resynchronisent selon les règles définies.

---

## L’espace cartésien

Le produit de toutes les tailles vaut :

\[
3\times6\times7\times9\times10\times13=147420
\]

Ce nombre représente le nombre de combinaisons dans l’espace cartésien complet si les positions sont considérées indépendamment.

Mais une orbite déterministe synchronisée n’est pas obligée de visiter tous ces états.

La différence entre :

**espace des configurations possibles**

et :

**trajectoire réellement visitée**

est fondamentale.

---

## Le ratio 18

On obtient :

\[
\frac{147420}{8190}=18
\]

Ce ratio montre que la période commune de 8190 ne parcourt pas nécessairement les 147420 configurations indépendantes possibles.

C’est exactement le type de distinction que Le Créateur doit rendre visible.

Pas seulement afficher un cercle qui tourne.

Montrer l’espace.

La trajectoire.

Les états visités.

Les états jamais visités.

---

## La machine CLOCK / STATE

Une autre brique est une machine cyclique :

~~~text
S0 → S1 → S2 → … → S(N-1) → S0
~~~

Paramètres :

nombre d’états;

état initial;

pas;

direction;

vitesse;

transitions spéciales.

La représentation circulaire peut utiliser :

\[
\theta_n=\frac{2\pi x_n}{m}
\]

Pour \(m=9\), les états 0, 3 et 6 correspondent à :

\[
0^\circ,\ 120^\circ,\ 240^\circ
\]

Cette représentation donne une géométrie à l’arithmétique modulaire.

---

## Géométrie et état

Il faut toutefois distinguer :

l’état mathématique \(x_n\);

sa représentation visuelle \(\theta_n\).

L’angle est une visualisation du cycle.

Il n’est pas nécessairement un angle physique réel.

Cette séparation empêche l’image de prendre plus de sens que le modèle.

---

## Rotations opposées

Une autre expérience importante utilise deux rotations :

\[
x_{n+1}^{(+)}=(x_n^{(+)}+k)\bmod m
\]

et :

\[
x_{n+1}^{(-)}=(x_n^{(-)}-k)\bmod m
\]

Pour \(m=9\) et \(k=3\) :

sens positif :

~~~text
0 → 3 → 6 → 0
~~~

sens négatif :

~~~text
0 → 6 → 3 → 0
~~~

Dans cet exemple, les deux trajectoires se resynchronisent après trois ticks.

---

## Le point de rencontre

Pour un cycle de taille \(m\) avec deux rotations opposées de pas \(k\), une période candidate de rencontre peut être écrite :

\[
P_{\mathrm{meeting}}
=
\frac{m}{\gcd(m,2k)}
\]

selon la définition choisie du retour relatif.

Le Créateur doit calculer réellement :

position A;

position B;

phase A;

phase B;

écart de phase;

points de rencontre;

période de resynchronisation.

Pas seulement dessiner deux flèches qui tournent.

---

## La phase

Si l’état \(x\) est projeté sur un cercle :

\[
\theta=\frac{2\pi x}{m}
\]

alors l’écart de phase peut être calculé.

Mais il faut choisir une convention.

Écart signé ?

Écart minimal sur le cercle ?

Intervalle \([0,2\pi)\) ?

Intervalle \((-\pi,\pi]\) ?

Une petite décision mathématique peut changer l’interprétation.

Le protocole doit l’écrire.

---

## Le Gate

La **GATE** traduit une autre idée :

~~~text
INPUT
→ OBSERVATION
→ FILTER
→ DECISION
→ ROUTING
→ ACTION
~~~

Pour une Gate booléenne :

\[
G(x)=1
\]

si la condition est satisfaite, sinon :

\[
G(x)=0
\]

Une Gate peut :

accepter;

rejeter;

router;

marquer;

déclencher.

Le Créateur doit toujours rendre la condition visible.

---

## Le Gate n’est pas un oracle

Une Gate ne « sait » pas mystérieusement quoi faire.

Elle applique une condition.

Si la condition est un modèle appris, ce modèle doit être référencé.

Si la condition est un seuil, le seuil doit être visible.

Si la condition dépend d’une mesure, la mesure doit être traçable.

Une décision n’est pas une magie.

C’est un contrat.

---

## La Gate pondérée

Une extension candidate pourrait produire :

\[
G(x)\in[0,1]
\]

au lieu d’un booléen.

Cela peut représenter un score.

Une probabilité calibrée.

Une intensité.

Mais l’interprétation doit être définie.

0.8 de quoi ?

La valeur seule ne suffit pas.

---

## La machine combinée

Une composition candidate peut ressembler à :

~~~text
ÉTAT x_n
→ ITERATOR
→ TRANSFORMATION
→ MODULAR CYCLE
→ GATE
→ GRAPH ROUTER
→ ÉTAT x_(n+1)
→ BOUCLE
~~~

Modèle conceptuel :

\[
x_{n+1}=R(G(F(x_n)))\bmod m
\]

où :

\(F\) est une transformation;

\(G\) une porte;

\(R\) un routage;

\(m\) un espace modulaire éventuel.

Cette composition reste optionnelle.

Elle ne doit pas devenir le modèle universel de tout.

---

## Le danger du modèle unique

Quand un outil est puissant, il devient tentant de tout faire entrer dedans.

Le Créateur doit résister.

Une expérience linéaire n’a pas besoin d’un cycle.

Une fonction pure n’a pas besoin d’une Gate.

Un modèle continu n’a pas besoin d’un modulo.

L’architecture doit permettre la composition.

Pas l’imposer.

---

## Le Stability Lab

Le **Stability Lab** est l’un des éléments les plus importants du Créateur.

Il répond à la règle :

> **FORME ≠ STABILITÉ ≠ PREUVE**

Une forme proposée entre dans le laboratoire.

Puis :

~~~text
ÉTAT INITIAL
→ DYNAMIQUE
→ PERTURBATION
→ ÉVOLUTION
→ MESURE
→ COMPARAISON
→ RÉSULTAT
~~~

Cette chaîne transforme une géométrie en objet expérimental.

---

## Les statuts de stabilité

Le laboratoire peut utiliser :

**NON TESTÉ.**

**EN TEST.**

**STABLE SELON PROTOCOLE.**

**INSTABLE SELON PROTOCOLE.**

**PÉRIODIQUE.**

**CONVERGENT.**

**DIVERGENT.**

**INDÉTERMINÉ.**

Chaque statut doit être rattaché à une définition.

---

## STABLE SELON PROTOCOLE

Cette formulation est volontaire.

Pas simplement :

**STABLE.**

Parce que la stabilité dépend :

de la métrique;

du seuil;

du temps observé;

des perturbations;

du domaine.

Un système stable pendant 100 cycles peut devenir instable après 10 000.

Le protocole détermine ce que le mot signifie.

---

## AUCUN CYCLE DÉTECTÉ DANS LA FENÊTRE TESTÉE

Cette phrase est un excellent exemple de rigueur.

Si aucun cycle n’est observé, on ne doit pas écrire :

**PAS DE CYCLE.**

On doit écrire :

**AUCUN CYCLE DÉTECTÉ DANS LA FENÊTRE TESTÉE.**

Cette formulation conserve la frontière entre absence d’observation et impossibilité universelle.

---

## Les perturbations

Le Créateur doit pouvoir appliquer des variations contrôlées.

Paramètre.

État initial.

Élément.

Connexion.

Entrée.

Retard.

Bruit.

Chaque perturbation doit être enregistrée.

Sinon, on ne peut pas reproduire le résultat.

---

## Perturbation d’un paramètre

Supposons un seuil \(\theta\).

On peut tester :

\[
\theta-\delta,\ \theta,\ \theta+\delta
\]

Puis observer.

Le comportement change-t-il légèrement ?

Brutalement ?

Existe-t-il une bifurcation ?

Le Stability Lab commence alors à devenir un véritable outil d’analyse dynamique.

---

## Perturbation de l’état initial

Deux systèmes avec la même règle peuvent évoluer différemment selon \(x_0\).

Le Créateur doit pouvoir dupliquer une expérience.

Changer seulement l’état initial.

Comparer.

Cette capacité est essentielle pour étudier la sensibilité.

---

## Perturbation d’une connexion

On retire un B-Link.

Que se passe-t-il ?

Le système continue ?

Il s’arrête ?

Il route autrement ?

Une plate robuste doit connaître son comportement lors de certaines pertes.

---

## Perturbation par retard

Dans un système distribué ou dynamique, un retard peut changer complètement le comportement.

Ajouter une latence contrôlée permet d’étudier la résilience temporelle.

Le mot **retard** doit être accompagné d’une unité.

Milliseconds.

Ticks.

Cycles.

Pas d’ambiguïté.

---

## Perturbation par bruit

Un bruit peut être ajouté.

Mais il faut définir sa distribution.

Amplitude.

Seed.

Fréquence.

Sinon, deux tests portant le même nom peuvent être incomparables.

---

## La distance entre trajectoires

On peut comparer un système non perturbé \(x_n\) à un système perturbé \(x'_n\) :

\[
D_n=d(x_n,x'_n)
\]

La métrique \(d\) est définie par le protocole.

C’est important.

Distance euclidienne ?

Différence absolue ?

Distance sur un cycle ?

Distance de graphe ?

Le choix de \(d\) détermine ce que le résultat signifie.

---

## Le laboratoire ne doit pas cacher sa métrique

Un graphique de divergence est impressionnant.

Mais si la distance n’est pas définie, il n’a pas de sens scientifique clair.

Le nom de la métrique doit être visible.

Éventuellement sa formule.

Le lecteur doit pouvoir reproduire.

---

## La reproductibilité

Le Créateur doit conserver :

nombre d’essais;

paramètres;

seed si applicable;

résultats;

écarts;

conditions.

Pour un système déterministe, on peut vérifier la répétition exacte attendue.

Pour un système probabiliste, la notion de reproductibilité devra être adaptée.

Distribution.

Tolérance.

Intervalle.

Mais le principe reste :

les conditions doivent être connues.

---

## Le seed

Lorsqu’un générateur pseudo-aléatoire intervient, le seed devient une partie de la provenance.

Sans lui, certaines trajectoires ne peuvent pas être reproduites exactement.

Le seed n’est pas toujours nécessaire à la conclusion.

Il est souvent nécessaire au débogage.

---

## Le critère de cristallisation

Selon le protocole, une plaque ou un module peut devenir candidat à la cristallisation si plusieurs conditions sont satisfaites.

Par exemple :

orbite déterminée;

période déterminée;

contraintes respectées;

Gates requises respectées;

tests de perturbation réussis;

résultat reproductible;

version figée.

Cette liste n’est pas universelle.

Elle dépend du type d’objet.

Mais elle donne une structure.

---

## Une représentation abstraite du cristal

Le Créateur a proposé une représentation :

\[
CRYSTAL=(P,\theta,T,M,H)
\]

où :

\(P\) = plaque ou configuration;

\(\theta\) = paramètres;

\(T\) = protocole;

\(M\) = mesures;

\(H\) = hash.

Cette définition est interne au Créateur.

Elle ne prétend pas produire un cristal physique.

Cette phrase doit toujours rester proche du concept.

---

## Le hash

Le hash sert à identifier un état exact.

Si un paramètre change, le hash change.

Si le fichier change, le hash change.

Cela permet de relier une mesure à une configuration précise.

Mais :

**hash ≠ validité.**

L’empreinte prouve l’identité de la donnée.

Pas sa vérité.

---

## La version

Chaque version doit conserver :

version;

date;

auteur;

parent;

changements;

hash.

Cette discipline donne une généalogie.

Un objet peut évoluer.

Sans effacer ce qu’il était.

---

## Le fork

Un futur fork doit permettre de copier un module public dans un autre laboratoire sans modifier l’original.

La provenance doit suivre.

Parent.

Auteur.

Version source.

Date.

La nouvelle branche peut ensuite diverger.

Le fork devient un outil de transmission.

---

## Le clone et le fork

Un clone technique et un fork créatif ne sont pas la même chose.

Clone :

reproduction d’un état ou d’une définition.

Fork :

nouvelle lignée assumée.

Le Créateur devra probablement distinguer ces opérations.

Sinon, la généalogie devient ambiguë.

---

## La table inférieure

La table d’objets située au bas de l’interface peut devenir l’un des éléments les plus puissants du système.

Parce qu’elle montre la structure documentaire derrière le canevas.

ID.

Nom.

Type.

Version.

Statut.

Propriétaire.

Visibilité.

Date.

Chaque ligne est une entrée dans la Brutothèque.

---

## Le classement

Types envisagés :

~~~text
IDÉE
GÉOMÉTRIE
FORMULE
MODULE
GATE
CYCLE
PLAQUE
EXPÉRIENCE
PROTOCOLE
MESURE
CRISTAL
SYSTÈME
PREUVE
~~~

Cette taxonomie est importante.

Parce que tous les objets ne doivent pas être traités de la même manière.

Une idée n’a pas besoin du même protocole qu’une mesure.

Une mesure n’est pas une formule.

Une preuve n’est pas une expérience.

Le type protège le sens.

---

## Les identifiants

Des identifiants structurés ont été envisagés :

~~~text
BT-IDE-####
BT-GEO-####
BT-FOR-####
BT-MOD-####
BT-GAT-####
BT-CYC-####
BT-PLQ-####
BT-EXP-####
BT-PRT-####
BT-CRY-####
BT-SYS-####
BT-PRV-####
~~~

Le nom humain peut changer.

L’identifiant reste.

Cela permet de garder des références stables.

---

## La fiche d’objet

Chaque objet peut posséder :

ID;

nom;

type;

version;

statut;

propriétaire;

visibilité;

description;

objectif;

source;

hypothèses;

paramètres;

entrées;

sorties;

contraintes;

dépendances;

invariants;

risques;

protocole;

test minimal;

preuve attendue;

condition d’abandon;

notes;

historique;

provenance.

Cette liste est longue.

Tous les champs ne seront pas obligatoires pour tous les types.

Mais elle montre l’ambition :

faire de chaque objet un artefact compréhensible.

---

## Les statuts

La Brutothèque peut utiliser :

~~~text
SOURCE
MESURE
CALCUL
CANDIDAT
HYPOTHÈSE
PROTOCOLE
EN TEST
INTERPRÉTATION
VALIDÉ SELON PROTOCOLE
CRISTALLISÉ
INDÉTERMINÉ
REJETÉ
ARCHIVÉ
~~~

Ce vocabulaire constitue une grammaire de connaissance.

Il évite qu’une chose change de nature simplement parce qu’elle a été déplacée dans l’interface.

---

## SOURCE

Une source n’est pas une validation.

Elle dit d’où vient l’information.

C’est le début de la provenance.

---

## MESURE

Une mesure doit savoir :

quoi;

comment;

quand;

avec quel instrument ou protocole;

quelle unité;

quelle incertitude si applicable.

---

## CALCUL

Un calcul transforme des entrées selon une règle.

Il peut être parfaitement reproductible.

Cela ne le transforme pas automatiquement en mesure.

---

## CANDIDAT

Une proposition suffisamment définie pour être examinée.

Pas encore confirmée.

---

## HYPOTHÈSE

Une proposition qui accepte le risque d’être testée.

Idéalement avec une condition pouvant l’affaiblir ou la rejeter.

---

## PROTOCOLE

Une procédure définissant comment le test sera réalisé.

Le protocole ne garantit pas que le test est bon.

Mais il rend le processus examinable.

---

## EN TEST

L’expérience est en cours.

Il ne faut pas afficher un résultat final avant la fin du protocole.

---

## INTERPRÉTATION

Le sens que nous attribuons au résultat.

Cette couche doit rester distincte de la donnée brute.

---

## VALIDÉ SELON PROTOCOLE

Une expression volontairement limitée.

Elle dit :

cet objet satisfait ce protocole.

Pas :

cet objet est vrai dans toutes les conditions.

---

## CRISTALLISÉ

Version figée associée à sa provenance et à ses résultats.

Pas vérité absolue.

---

## INDÉTERMINÉ

Les données ne permettent pas de conclure.

Ce statut doit être considéré comme pleinement valide.

---

## REJETÉ

Le candidat n’a pas satisfait les critères définis.

L’objet peut rester dans l’historique.

---

## ARCHIVÉ

L’objet n’est plus actif dans le travail courant.

Mais sa trace est conservée.

---

## Le Laboratoire des chiffres

Le **Laboratoire des chiffres** est une zone distincte du simple calculateur.

Son pipeline méthodologique est :

~~~text
DONNÉES BRUTES
→ SOURCE
→ MESURE
→ CALCUL
→ OBSERVATION
→ HYPOTHÈSE
→ PROTOCOLE
→ TEST
→ INTERPRÉTATION
→ VALIDATION ÉVENTUELLE
~~~

Cette chaîne est capitale.

Elle empêche un nombre de sauter directement de donnée brute à vérité.

---

## Les données externes

Une information provenant d’une autre IA, d’un site, d’un document ou d’un humain doit conserver sa source.

Par exemple :

~~~text
SOURCE = GEMINI
STATUT = À VÉRIFIER
~~~

Le fait qu’une donnée provienne d’un système puissant ne lui donne pas automatiquement le statut de règle ANTMUX-X72.

Le Créateur doit garder cette frontière.

---

## Importer sans canoniser

L’import est une action.

La validation en est une autre.

On peut faire entrer une donnée dans le laboratoire.

Puis la vérifier.

La comparer.

La rejeter.

La corriger.

Le pipeline doit empêcher l’import de devenir automatiquement une promotion.

---

## La provenance des images

Même principe pour les images.

Une capture peut devenir une référence visuelle.

Elle doit conserver :

source;

date;

contexte;

type.

Mais l’image ne doit pas être interprétée automatiquement comme preuve d’un mécanisme.

Elle peut guider.

Pas conclure.

---

## Une photo comme spécification

Par contre, une image peut être une excellente spécification visuelle.

Position.

Proportion.

Couleur.

Relation.

Disposition.

Le Créateur peut permettre de transformer ces informations en objets géométriques mesurables.

C’est là que la vision rejoint l’ingénierie.

---

## Le module géométrique

Un objet géométrique peut définir :

centre;

rayon;

orientation;

nombre de points;

symétrie;

échelle;

ports;

état éventuel.

Une fleur ou une rosace peut devenir un module.

Mais sa beauté reste distincte de son comportement logique.

---

## Le générateur géométrique

Le projet possède déjà des idées de générateur pour :

lotus;

lys;

rosace;

mandala;

flower of life;

couches concentriques;

phyllotaxie;

spirales;

tore;

dôme;

pyramide circulaire;

cadrans;

anneaux;

structures fractales.

Le Créateur peut devenir l’endroit où ces objets sont générés.

Mais chaque instance doit être indépendante.

---

## L’instance géométrique

Une instance peut posséder :

géométrie;

nombre de points;

rayon;

orientation;

horloge;

formule;

entrée;

sortie;

état;

connexions.

L’objet visuel n’est plus seulement un dessin.

Il devient une instance paramétrée.

---

## La géométrie comme interface

Une forme peut servir de manière intuitive à organiser des flux.

Mais le moteur logique doit rester séparé.

Le GeometryRouter peut relier des instances selon une topologie.

Le dessin aide à voir.

Le graphe décide.

---

## Le nombre d’or

Certaines géométries peuvent utiliser :

\[
\theta_{\mathrm{gold}}=\pi(3-\sqrt 5)
\]

Mais cette valeur ne doit jamais être imposée à toutes les structures.

Elle est un paramètre possible.

Pas un dogme de design.

Le Créateur doit permettre de la tester à côté d’autres valeurs.

---

## Le danger du nombre préféré

Dès qu’un projet possède des nombres récurrents, il existe un risque.

Les choisir parce qu’ils ont déjà une place symbolique.

Puis conclure qu’ils sont importants parce qu’ils apparaissent dans le résultat.

Le Laboratoire des chiffres doit justement permettre de comparer.

Autres nombres.

Autres paramètres.

Null models.

Sensibilité.

Un nombre doit gagner sa place par son comportement, pas par son prestige.

---

## La machine de contradiction

Cette idée revient toujours.

Le Créateur doit être une machine de contradiction constructive.

Si un motif disparaît lorsque l’on change légèrement un paramètre, le système doit le montrer.

Si une hypothèse ne se reproduit pas, il doit le montrer.

Si une Gate n’est jamais traversée, il doit le montrer.

Si un cycle prétendu n’est pas détecté, il doit le montrer.

Le logiciel n’est pas là pour défendre son auteur.

Il est là pour exposer le comportement.

---

## Le rouge est une donnée

Un voyant rouge n’est pas une honte.

Il peut être exactement ce qu’il fallait trouver.

Un système où tout est vert en permanence doit être suspect.

L’échec fait partie de l’atelier.

---

## Le jaune aussi

Entre le vert et le rouge, il faut souvent un troisième état.

Inconclusif.

Inconnu.

En attente.

Non testé.

Cette zone intermédiaire empêche les faux verdicts.

---

## La couleur ne suffit pas

La couleur peut aider.

Mais elle doit être accompagnée d’un texte ou d’un symbole clair.

Accessibilité.

Impression.

Daltonisme.

Lecteurs d’écran.

Le statut doit rester compréhensible sans dépendre d’une seule couleur.

---

## Le test minimal

Chaque objet doit idéalement posséder un test minimal.

Pas forcément suffisant pour une validation complète.

Mais assez pour vérifier qu’il respecte son contrat de base.

Un module d’addition :

2 + 3 = 5.

Un Iterator :

un pas produit l’état attendu.

Une Gate :

une entrée témoin passe, une autre est rejetée.

Un routeur :

la destination attendue est sélectionnée.

Les tests simples protègent le système.

---

## Le test de frontière

Les valeurs limites sont souvent les plus instructives.

Zéro.

Maximum.

Minimum.

Type vide.

Entrée absente.

Cycle de taille 1.

Pas supérieur au modulo.

Connexion manquante.

Le Créateur devrait aider à générer ces cas.

---

## Le test de perturbation

Après le fonctionnement nominal, vient la perturbation.

La transition doit être visible.

**PASS NOMINAL**

ne signifie pas :

**ROBUSTE.**

Le test de perturbation crée un autre niveau de confiance.

---

## Le test de reproduction

Une expérience répétée doit conserver ses conditions.

Le Créateur peut proposer :

REPEAT N TIMES.

Comparer.

Calculer les écarts.

Archiver les sorties.

L’automatisation transforme la répétition en preuve plus forte.

---

## Le protocole comme objet

Un protocole ne doit pas être seulement du texte dans une note.

Il peut devenir un objet de la Brutothèque.

ID.

Version.

Étapes.

Critères.

Seuils.

Données requises.

Condition d’arrêt.

Ce protocole peut être lié à plusieurs expériences.

---

## Le protocole peut évoluer

Une nouvelle version du protocole peut changer le résultat.

Cela doit être visible.

**Résultat validé selon PRT-v1**

n’est pas automatiquement validé selon PRT-v2.

La version du protocole appartient à la provenance.

---

## Une preuve attendue

Chaque expérience peut déclarer :

**preuve attendue**

au sens de type d’élément recherché.

Log.

Mesure.

Courbe.

Hash.

Réplication.

Pas une conclusion prédéterminée.

Cette distinction est importante.

On sait ce qui sera observé.

Pas ce que l’observation doit dire.

---

## La condition d’abandon

L’expérience peut aussi déclarer :

**condition d’abandon.**

Si tel résultat survient, cette version est rejetée.

Cette discipline empêche le candidat d’être sauvé par un changement de règle après le test.

---

## Le notebook automatique

À terme, Le Créateur pourrait générer un rapport d’expérience.

Question.

Objet.

Version.

Protocole.

Paramètres.

Mesures.

Graphiques.

Statut.

Hash.

Ce rapport devient une trace.

Il peut être publié ou conservé privé selon la visibilité.

---

## Le rapport ne doit pas réécrire l’expérience

L’automatisation du rapport est utile seulement si elle conserve les données originales.

Le résumé n’est pas la source.

Les données et les logs doivent rester accessibles.

Le rapport organise.

Il ne remplace pas.

---

## L’historique

Chaque action importante peut créer une entrée d’historique.

Création.

Modification de paramètre.

Connexion.

Déconnexion.

Test.

Cristallisation.

Publication.

Fork.

Archivage.

Cette chronologie rend le laboratoire reprenable.

---

## L’historique ne doit pas devenir un torrent inutile

Tout enregistrer peut produire des millions d’événements sans valeur.

Il faut distinguer :

événement opérationnel;

événement d’audit;

checkpoint;

décision.

La bonne granularité reste à définir.

Mais le principe est clair :

les changements substantiels doivent être traçables.

---

## L’autosave

Un atelier moderne a besoin de sauvegarder.

Mais l’autosave ne doit pas écraser la version canonique.

Sauvegarder le travail courant.

Puis permettre un commit ou un snapshot explicite.

Le brouillon et la version publiée doivent rester distincts.

---

## Snapshot

Un snapshot peut capturer :

graphe;

paramètres;

positions;

versions;

états;

configuration.

Cela permet de revenir ou de comparer.

Mais un snapshot d’interface n’est pas forcément un checkpoint d’exécution complet.

Le type de snapshot doit être écrit.

---

## La chronologie visuelle

Le Créateur pourrait permettre de comparer deux versions.

Avant.

Après.

Nœuds ajoutés.

Liens supprimés.

Paramètres modifiés.

Cette vue donnerait à Git une traduction visuelle.

Très utile pour comprendre une évolution.

---

## GitHub comme couche de provenance

Le pipeline envisagé inclut GitHub.

Les objets importants peuvent être représentés dans des fichiers versionnés.

Le Créateur ne remplace pas Git.

Il peut construire une interface au-dessus.

Commit.

Branch.

Diff.

PR.

Ces mécanismes restent utiles.

---

## Portabilité

Une chaîne de travail a été envisagée :

~~~text
GEMINI BUILD
→ GITHUB
→ AUDIT LECTURE SEULE
→ CORRECTIONS
→ BUILD INDÉPENDANT
→ SERVEUR ANTMUX
→ CONNEXION ULTÉRIEURE DU VÉRITABLE ANTMUX-X72
~~~

Cette chaîne raconte quelque chose d’essentiel.

Le Créateur ne doit pas dépendre éternellement de l’outil qui a permis de construire sa première version.

Il doit devenir portable.

---

## Gemini Build comme forge provisoire

Un outil de génération peut aider à fabriquer l’interface.

Mais le projet doit pouvoir sortir.

Le code doit être récupérable.

Auditable.

Corrigeable.

Déployable ailleurs.

Le fournisseur initial ne doit pas devenir la prison de l’architecture.

---

## Audit lecture seule

Avant de modifier un code généré, il est utile de comprendre ce qui existe réellement.

Quelles fonctions sont vraies ?

Quelles données sont simulées ?

Quel backend ?

Quelles dépendances ?

Quels secrets ?

L’audit lecture seule crée une cartographie avant l’intervention.

Cette discipline protège la baseline.

---

## Build indépendant

La possibilité de reconstruire hors de l’environnement d’origine est un test de portabilité.

Si l’application ne fonctionne que dans un environnement fermé avec des dépendances invisibles, elle n’est pas encore indépendante.

Le build doit devenir reproductible.

---

## Le serveur ANTMUX

Une version déployée sur le serveur du projet représente une autre étape.

Mais le déploiement ne doit pas être confondu avec l’intégration de X72.

Le serveur peut héberger Le Créateur.

X72 reste un moteur distinct.

---

## X72 — moteur externe

Cette séparation mérite plusieurs pages.

Le Créateur est le laboratoire.

X72 est un moteur externe.

Le laboratoire peut un jour lui envoyer une configuration.

Recevoir un état.

Mesurer.

Afficher.

Mais les deux doivent pouvoir évoluer séparément.

Cette architecture évite que la première interface devienne dépendante du moteur.

---

## L’adaptateur X72

Le Créateur peut posséder un adaptateur.

Contrat d’entrée.

Contrat de sortie.

Version du protocole.

État de connexion.

Mais tant que le véritable moteur n’est pas branché :

**NON CONNECTÉ.**

Le connecteur visible n’est pas une preuve de connexion.

---

## Le moteur ne doit pas avaler le laboratoire

Une erreur serait de transformer Le Créateur en simple panneau X72.

Le Créateur a une vocation plus large.

Construire et tester des objets.

X72 est un moteur possible.

Un backend important.

Mais pas l’unique raison d’exister de l’atelier.

Cette séparation protège l’avenir.

---

## D’autres moteurs

Si l’architecture est bonne, d’autres moteurs pourraient un jour être branchés.

Simulateur local.

Moteur Python.

WebAssembly.

Hardware.

Service distant.

Le contrat d’adaptateur permettrait cette pluralité.

C’est une conséquence logique de la modularité.

---

## Mais la première version doit rester petite

Encore une fois :

ne pas construire toute la plateforme future avant de valider le canevas.

Premières priorités :

bureau principal;

canevas;

palette;

objets déplaçables;

module;

plaque;

Gate;

Iterator;

Modular Cycle;

Clock/State simple;

connexions et graphe simple;

panneau inférieur;

calculateur statistique;

banc de mesure;

Stability Lab simple;

Brutothèque;

Laboratoire des chiffres;

emplacement X72 NON CONNECTÉ;

authentification portable si utilisée;

demande de laboratoire;

panneau administrateur;

interphone;

permissions;

documentation.

Cette liste est déjà grande.

Elle doit être construite par étapes.

---

## Le MVP du Créateur

Un MVP véritable pourrait être encore plus petit.

Créer un module.

Le placer.

Le connecter.

Exécuter un Iterator.

Mesurer un cycle.

Perturber un paramètre.

Sauvegarder.

Versionner.

Afficher un statut honnête.

Si cette chaîne fonctionne de bout en bout, le projet possède déjà une colonne vertébrale.

---

## Le premier test complet

On peut imaginer le scénario :

1. créer un Modular Cycle;
2. définir \(m=9\);
3. définir \(k=3\);
4. définir \(x_0=0\);
5. RUN;
6. observer 0 → 3 → 6 → 0;
7. détecter période 3;
8. changer \(k\);
9. comparer;
10. sauvegarder l’expérience;
11. créer un protocole;
12. figer une version DEMO.

Ce petit parcours teste énormément de couches du Créateur.

---

## Une DEMO doit rester une DEMO

L’exemple modulo 9 peut être parfait pour montrer l’interface.

Mais il ne doit jamais être présenté comme preuve d’une théorie plus grande.

D’où le badge :

**DEMO.**

La démonstration montre que le logiciel fonctionne.

Pas que le monde obéit à cette architecture.

---

## La frontière entre logiciel et science

C’est probablement l’une des frontières les plus importantes du Créateur.

Le logiciel peut être correct.

Le modèle peut être faux.

Ou le logiciel peut être bogué.

Le modèle peut être bon.

Ou les deux peuvent être corrects.

Ou les deux faux.

Le test logiciel et le test scientifique sont donc deux couches différentes.

---

## Test logiciel

Le code produit-il ce qu’il est censé produire ?

---

## Test scientifique

Ce que le code est censé produire correspond-il au phénomène étudié ?

Deux questions.

Deux protocoles.

Le Créateur doit permettre de les relier sans les confondre.

---

## Le banc de mesure du logiciel

Latence.

Erreurs.

Débit.

États.

Période simulée.

---

## Le banc de mesure physique

Capteur.

Unité.

Calibration.

Incertitude.

Conditions.

Ce second niveau ne doit apparaître que lorsqu’un dispositif réel existe.

---

## La fabrication physique

Le Créateur peut un jour préparer des plaques physiques.

Mais ce futur demande une nouvelle discipline.

Tolérances.

Matériaux.

Connectique.

Puissance.

Température.

Fréquence.

Fabrication.

Sécurité.

La géométrie à l’écran devient alors un plan.

Pas encore un objet.

---

## Le mot fabriquer

Dans le logiciel, fabriquer peut signifier générer un module.

Dans le matériel, fabriquer signifie réellement produire un composant.

Le Créateur doit distinguer ces sens.

Sinon, une phrase comme :

**module fabriqué**

peut devenir ambiguë.

---

## Le prototype

Entre simulation et produit final existe le prototype.

Un capteur réel.

Une carte.

Une plaque imprimée.

Un dispositif partiel.

Le prototype doit avoir son propre statut.

Il ne faut pas le confondre avec une production validée.

---

## Le laboratoire doit conserver les échecs physiques aussi

Un module qui chauffe trop.

Une fréquence instable.

Une soudure fragile.

Un cristal réel qui ne produit pas l’effet prévu.

Ces résultats peuvent devenir des entrées de la Brutothèque.

La mémoire doit traverser le passage du numérique au matériel.

---

## Le Créateur comme pont

À son meilleur, Le Créateur devient un pont entre plusieurs mondes.

Idée.

Dessin.

Mathématique.

Code.

Simulation.

Mesure.

Prototype.

Publication.

Ce pont n’oblige pas chaque idée à parcourir toute la route.

Il donne simplement un chemin possible.

---

## Ne pas sauter les ponts

Une idée numérique ne devient pas physique par déclaration.

Une simulation ne devient pas prototype.

Un prototype ne devient pas produit.

Chaque changement de niveau exige de nouvelles preuves.

Le Créateur doit rendre ces transitions explicites.

---

## Les preuves attachées au bon niveau

Preuve de calcul.

Preuve de simulation.

Preuve de test logiciel.

Preuve de mesure physique.

Preuve de reproductibilité.

Le même objet peut posséder plusieurs types de preuves.

Le badge doit préciser lequel.

---

## Le registre des preuves

La Brutothèque peut contenir un type :

~~~text
PREUVE
~~~

Mais ce type doit être relié à une affirmation précise.

Preuve de quoi ?

Cette question est obligatoire.

Une preuve sans cible devient un document impressionnant mais ambigu.

---

## La preuve comme lien

On peut modéliser :

**affirmation ← preuve**

Le graphe documentaire devient alors très intéressant.

Une même preuve peut soutenir plusieurs affirmations.

Une affirmation peut dépendre de plusieurs preuves.

Une nouvelle preuve peut contredire une ancienne interprétation.

Le Créateur peut un jour visualiser cela.

---

## Le graphe de connaissance

À côté du graphe d’exécution, un graphe de provenance et de preuve pourrait exister.

Nœuds :

objets;

sources;

protocoles;

expériences;

mesures;

interprétations.

Liens :

vient de;

teste;

soutient;

contredit;

remplace;

dérive de.

Cette architecture aiderait énormément à garder le projet compréhensible.

---

## Le graphe d’exécution et le graphe de preuve

Ils ne sont pas identiques.

Le graphe d’exécution dit :

**comment le système fonctionne.**

Le graphe de preuve dit :

**pourquoi nous pensons que certaines propriétés tiennent.**

Les deux doivent pouvoir se croiser.

---

## Le mauvais raccourci

Un module peut avoir une ligne verte dans le graphe d’exécution.

Cela ne signifie pas qu’une hypothèse scientifique associée est validée.

Il faut éviter ce raccourci visuel.

Le système fonctionne.

La théorie reste candidate.

Deux niveaux.

---

## Le tableau d’état

Le panneau inférieur peut donc devenir un véritable registre.

Exemple :

~~~text
ID           TYPE       VERSION   STATUT
BT-MOD-0012  MODULE     0.3       EN TEST
BT-EXP-0041  EXPERIENCE 1.0       TERMINÉE
BT-CRY-0004  CRISTAL    1.0       CRISTALLISÉ
BT-PRV-0010  PREUVE     1.0       LIÉE
~~~

Ce genre de table rend l’architecture explicite.

---

## Le propriétaire

Le tableau doit aussi montrer le propriétaire lorsque pertinent.

Pas pour hiérarchiser la vérité.

Pour savoir qui peut modifier.

Qui a publié.

Qui doit être contacté.

La provenance et l’autorisation sont liées.

---

## L’auteur n’est pas la preuve

Encore une fois :

un objet appartenant à Topbrutus n’est pas correct parce qu’il lui appartient.

Un objet proposé par Astra n’est pas correct parce qu’il vient d’une IA.

Le statut vient du protocole.

Pas du prestige du propriétaire.

---

## La collaboration

Le Créateur peut devenir multi-utilisateur.

Mais la collaboration exige des mécanismes précis.

Qui peut voir ?

Qui peut commenter ?

Qui peut forker ?

Qui peut modifier ?

Qui peut fusionner ?

Qui peut publier ?

Ces permissions doivent être explicites.

---

## Commenter sans modifier

Un visiteur ou collaborateur peut parfois avoir le droit de commenter sans toucher à l’objet.

Cette séparation est utile.

Elle permet la critique sans donner l’écriture.

Le système de discussion peut rester textuel.

---

## Forker sans écraser

Un collaborateur peut prendre une version publique.

Créer sa propre lignée.

L’original reste intact.

Cette architecture protège les auteurs et encourage l’expérimentation.

---

## Fusionner

Si une amélioration mérite de revenir dans l’original, il faut un processus de fusion.

Proposition.

Diff.

Tests.

Décision du propriétaire.

L’idée ressemble à une pull request.

Le Créateur peut éventuellement exposer cette logique visuellement.

---

## La publication

Publier un objet doit être une action explicite.

Vérifier :

visibilité;

secrets;

provenance;

version;

licence éventuelle;

statut.

La publication ne doit pas être le résultat accidentel d’un autosave.

---

## La vitrine publique

Une publication peut ensuite apparaître dans la vitrine.

Le visiteur voit :

nom;

description;

statut;

version;

structure publique;

résultats publiés;

provenance autorisée.

Mais pas les données privées.

---

## La galerie

Une future galerie peut montrer plusieurs créations.

Mais la galerie ne doit pas transformer le projet en concours de popularité.

Elle peut aider à découvrir.

Le statut scientifique reste séparé des vues et des likes.

---

## Le moteur de recherche

La Brutothèque aura besoin d’une recherche.

Par nom.

Par ID.

Par fonction.

Par unité.

Par statut.

Par propriétaire.

Par version.

Par type.

Cette fonction deviendra indispensable lorsque les objets se multiplieront.

---

## Recherche par compatibilité

Une fonction plus avancée pourrait demander :

**trouve-moi les modules dont la sortie est compatible avec l’entrée de BT-MOD-0123.**

À ce moment, la bibliothèque devient véritablement un outil d’architecture.

---

## Recherche par objectif

Avec l’IA architecte :

**je veux filtrer un signal, calculer sa fréquence dominante et conserver un log.**

L’IA peut rechercher :

FILTER.

FFT.

LOGGER.

Puis proposer une plate.

Cette expérience illustre le potentiel complet du système.

---

## SIGNAL-LAB

Une plaque candidate existe déjà :

~~~text
SIGNAL-LAB
~~~

Avec :

~~~text
OSCILLATOR
FREQUENCY
MIXER
NOISE
FILTER
DELAY
BRIDGE
SCOPE
FFT
OUTPUT
~~~

Signal générique :

\[
x(t)=\sum_k A_k\sin(2\pi f_k t+\phi_k)
\]

Cette plate est parfaite pour montrer comment une bibliothèque de composants peut devenir un laboratoire spécialisé.

---

## La plaque spécialisée

Le Créateur n’a pas besoin d’afficher tous les modules du monde dans une seule palette.

Une plate spécialisée peut fournir un sous-ensemble.

Signal.

Géométrie.

Mémoire.

Contrôle.

Réseau.

Chaque domaine peut avoir ses instruments.

---

## Le Scope

Un SCOPE visualise le signal.

Mais il doit montrer :

échelle;

unité;

temps;

échantillonnage.

Un tracé sans axes correctement définis peut tromper.

---

## FFT

La FFT peut transformer un signal temporel en représentation fréquentielle.

Mais il faut connaître :

fréquence d’échantillonnage;

fenêtrage;

normalisation;

résolution.

Le Créateur doit éviter le bouton magique :

**FFT**

qui produit une courbe sans contexte.

---

## L’instrumentation comme pédagogie

Cette exigence de contexte peut sembler lourde.

Elle est aussi pédagogique.

L’utilisateur apprend pourquoi les paramètres comptent.

Le logiciel devient professeur sans faire un long cours théorique.

---

## Le Créateur ne doit pas cacher les mathématiques

Une interface accessible ne signifie pas que les équations doivent disparaître.

Au contraire.

Le logiciel peut proposer plusieurs niveaux.

Vue simple.

Vue contrat.

Vue mathématique.

Vue code.

La personne choisit la profondeur.

---

## Un même objet, plusieurs représentations

Prenons un Modular Cycle.

Vue simple :

un cadran.

Vue paramètres :

\(m, k, x_0\).

Vue mathématique :

\[
x_{n+1}=(x_n+k)\bmod m
\]

Vue exécution :

liste des états.

Vue preuve :

période détectée + protocole.

Cette architecture relie l’intuition à la rigueur.

---

## La vue débutant

Le Créateur peut expliquer.

**m = nombre de positions.**

**k = pas.**

**x0 = position de départ.**

Puis montrer la trajectoire.

L’utilisateur apprend en manipulant.

---

## La vue expert

Le même objet peut exposer :

gcd;

période théorique;

orbite;

classe de congruence;

tests;

hash.

Le logiciel n’a pas besoin de choisir un seul public.

Il peut changer de profondeur.

---

## L’accessibilité

Un outil destiné à transmettre doit aussi penser à l’accessibilité.

Navigation clavier.

Lecteur d’écran.

Labels.

Contraste.

Taille de texte.

Pas seulement couleur.

Le futur du Créateur ne doit pas dépendre d’une seule façon de voir l’écran.

---

## La voix

Un jour, l’interaction vocale pourrait permettre :

**« sélectionne la Gate 4 ».**

**« lis-moi les paramètres ».**

**« compare les deux expériences ».**

Mais la voix est une interface.

Elle ne doit pas contourner les permissions.

Une commande vocale sensible doit suivre les mêmes règles qu’un clic.

---

## Le mobile

La vue visiteur peut être utile sur mobile.

La vue créateur complète peut demander un grand écran.

Le système n’a pas besoin d’imposer la même expérience partout.

Le rôle et le contexte d’usage peuvent déterminer l’interface.

---

## Le Créateur ne doit pas devenir prisonnier de la maquette

Le T0 visuel est important.

Mais il n’est pas sacré.

Une bonne maquette sert de référence.

Puis les tests d’usage peuvent montrer des problèmes.

Panneau trop étroit.

Table illisible.

Canevas encombré.

L’interface doit pouvoir évoluer.

La version T0 reste dans l’histoire.

---

## T0, T1, T2

On peut versionner l’interface comme le reste.

**T0 VISUEL**

concept.

**T1 FONCTIONNEL**

premières fonctions réelles.

**T2 INTÉGRATION**

backend, permissions, stockage.

Les noms exacts restent à définir.

Mais la philosophie reste :

ne pas effacer les étapes.

---

## La capture comme trace

Une capture d’écran du T0 peut aller dans les archives.

Elle documente la vision à cette date.

Plus tard, elle permettra de voir ce qui a été gardé.

Abandonné.

Transformé.

La maquette devient une preuve historique de conception.

---

## Le code comme seconde trace

Le dépôt montre ce qui était réellement implémenté.

La capture et le code ne prouvent pas la même chose.

La capture montre l’apparence.

Le code montre l’implémentation disponible.

Le laboratoire doit conserver les deux lorsque c’est utile.

---

## Le test de vérité de l’interface

Pour chaque élément visible, demander :

**est-ce réel ?**

Si oui :

quelle source ?

Si non :

badge DEMO ou À IMPLÉMENTER.

Cette simple discipline pourrait devenir un test automatique.

---

## Aucune donnée magique

Une valeur affichée doit venir :

d’un calcul;

d’une mesure;

d’un état;

d’une simulation;

d’une DEMO explicitement identifiée.

Pas d’un nombre choisi pour remplir l’écran.

Le Créateur doit pouvoir expliquer l’origine de chaque donnée importante.

---

## Le clic sur une métrique

Une future interface pourrait permettre de cliquer sur une valeur.

Puis voir :

source;

formule;

timestamp;

version;

protocole;

historique.

Cela transformerait l’interface en carte de provenance.

---

## La preuve à un clic

Même philosophie pour un badge PASS.

Cliquer.

Voir :

test;

résultat;

date;

commit;

paramètres.

Un statut sans profondeur devient décoratif.

Un statut inspectable devient confiance.

---

## L’indétermination à un clic

Même chose pour INDÉTERMINÉ.

Pourquoi ?

Données insuffisantes ?

Test interrompu ?

Contradictions ?

Fenêtre trop courte ?

L’inconnu lui aussi doit avoir une provenance.

---

## Le Créateur comme machine à questions

Le logiciel doit poser constamment des questions de contrôle.

Qu’est-ce que c’est ?

Quel est son état initial ?

Quelle règle applique-t-il ?

Quelles sont ses entrées et sorties ?

Quels sont ses paramètres et contraintes ?

Quelle est sa géométrie ?

Quelle est sa dynamique ?

Passe-t-il par les Gates requises ?

Quel chemin prend-il ?

Revient-il à un état antérieur ?

Quelle est sa période ?

Converge-t-il ?

Diverge-t-il ?

Que se passe-t-il si on le perturbe ?

Le résultat est-il reproductible ?

Quelles mesures le montrent ?

Quel est le protocole ?

Quelle est sa provenance ?

Peut-il être cristallisé ?

Peut-il être assemblé ?

Cette liste pourrait presque devenir l’assistant intégré du Créateur.

---

## Une idée n’a pas besoin de répondre à tout

Toutes ces questions ne s’appliquent pas à tous les objets.

Une image de référence n’a pas de période.

Une formule statique n’a pas nécessairement un état.

Le système doit poser les questions pertinentes au type.

La structure doit aider.

Pas devenir bureaucratique.

---

## Le bon niveau de friction

Trop peu de friction :

on crée des objets mal définis.

Trop de friction :

personne ne veut utiliser l’outil.

Le Créateur doit trouver un équilibre.

Créer facilement un brouillon.

Demander davantage de rigueur au moment de promouvoir.

Cette architecture est prometteuse.

---

## Le brouillon libre

En mode brouillon :

placer.

dessiner.

annoter.

essayer.

Pas besoin de remplir vingt champs.

Le statut reste :

**DRAFT** ou **IDÉE**.

---

## La promotion exige plus

Pour devenir MODULE :

entrées.

sorties.

règle.

version.

test minimal.

Pour devenir CRISTAL :

protocole.

résultats.

provenance.

hash.

La rigueur augmente avec le statut.

---

## La validation progressive

Cette conception évite de tuer la créativité.

L’idée peut naître librement.

Puis gagner de la structure.

Le système ne demande pas à une intuition de se comporter comme une publication scientifique dès la première minute.

---

## La cristallisation comme cérémonie technique

Il peut même exister un bouton :

**CRISTALLISER.**

Mais ce bouton ne doit pas simplement changer une couleur.

Il doit vérifier les préconditions.

Version figée.

Protocole associé.

Résultats disponibles.

Hash.

Puis créer un nouvel objet CRISTAL.

La cérémonie visuelle correspond à une vraie opération.

---

## Refuser de cristalliser

Si les conditions ne sont pas remplies :

**CRISTALLISATION REFUSÉE.**

Puis explication.

Test manquant.

Protocole absent.

Version modifiée depuis le dernier test.

Cette capacité à refuser donne de la valeur au statut.

---

## Décristalliser ?

On ne devrait probablement pas modifier un cristal.

On crée plutôt une nouvelle version candidate.

Cette discipline protège l’intégrité de la version figée.

Le mot **décristalliser** pourrait être réservé à une opération explicite de copie vers un nouveau candidat, jamais à une modification silencieuse de l’original.

---

## Le cristal comme parent

Nouvelle version :

parent = cristal précédent.

Le graphe de généalogie se construit.

On peut voir l’évolution.

---

## L’archivage

Un objet ancien peut être archivé.

Il disparaît de la palette active.

Mais reste accessible dans l’historique.

L’archive protège la lisibilité sans détruire la mémoire.

---

## La suppression

La suppression définitive doit être rare.

Et probablement séparée selon le type d’objet.

Une donnée privée peut devoir être supprimée.

Une trace scientifique peut devoir être conservée.

Le Créateur devra distinguer les obligations de mémoire et de confidentialité.

---

## La confidentialité est plus forte que la nostalgie

Si un objet contient des données qui doivent être supprimées, l’attachement historique ne doit pas justifier de les garder illégalement ou inutilement.

La mémoire du Royaume a des limites.

Une architecture responsable doit les respecter.

---

## La licence

Pour les objets publics, une licence peut devenir importante.

Peut-on réutiliser ?

Forker ?

Modifier ?

Redistribuer ?

Le Créateur peut demander ce choix au moment de publier.

Ainsi, la transmission devient juridiquement plus claire.

---

## La citation

Un objet publié peut fournir une citation.

Auteur.

Titre.

Version.

Date.

Identifiant.

Lien.

Cela rejoint directement le chapitre 3.

Laisser une trace exige de permettre aux autres de la référencer correctement.

---

## Zenodo et archivage

Certaines versions importantes peuvent être déposées dans un service d’archivage persistant.

Le Créateur peut générer les artefacts nécessaires.

Mais la publication archivistique reste une action explicite.

Elle ne doit pas se produire automatiquement à chaque autosave.

---

## Le DOI ne valide pas le contenu

Même si un objet reçoit un DOI, le statut scientifique reste ce que les preuves soutiennent.

Le DOI fournit une adresse persistante.

Pas une approbation.

Le Créateur doit maintenir cette nuance.

---

## Le monde extérieur

Une plateforme publique finit toujours par rencontrer le monde extérieur.

Curiosité.

Questions.

Critiques.

Tentatives d’abus.

Le système doit être conçu pour tout cela.

L’interphone texte est un premier canal limité.

La vitrine une première surface.

Les permissions une première protection.

---

## La modération

Un administrateur peut devoir intervenir.

Spam.

Harcèlement.

Abus.

Le Créateur n’est pas uniquement un logiciel scientifique.

S’il devient multi-utilisateur, il devient aussi un espace social.

Cette dimension doit être prise au sérieux.

---

## Rate limiting

Même un simple formulaire de texte peut être attaqué.

Le rate limiting limite le nombre de messages.

C’est une petite mesure.

Elle peut protéger la disponibilité.

---

## Validation

Le texte entrant doit être validé.

Taille maximale.

Encodage.

Caractères dangereux dans certains contextes.

Mais surtout :

rendu comme texte.

Pas interprété comme code.

---

## Les fichiers interdits dans l’interphone

Cette décision simplifie énormément la sécurité.

Pas d’archives.

Pas d’exécutables.

Pas d’images cachant des payloads.

Le créateur peut recevoir une question.

Pas une livraison de fichier.

Si un jour des pièces jointes sont nécessaires, elles devront être conçues comme une fonctionnalité séparée avec leur propre sécurité.

---

## L’interface et les secrets

Aucun secret dans :

Git;

HTML;

JavaScript client;

README;

logs.

Cette règle est non négociable.

Le Créateur peut afficher un statut :

**credential configuré**

sans afficher le credential.

---

## Variables d’environnement

Les secrets peuvent vivre côté serveur dans des mécanismes appropriés.

Le code référence une variable.

Pas la valeur.

Cette séparation doit être préservée dans les builds indépendants.

---

## Le fichier .env n’est pas un artefact public

Même lorsqu’il est pratique en local, un fichier contenant des secrets ne doit pas être poussé dans le dépôt public.

Les templates peuvent montrer les noms de variables.

Pas leurs valeurs.

---

## La portabilité de l’authentification

Une authentification Google a été envisagée.

Mais elle doit rester suffisamment isolée pour que le projet puisse fonctionner hors de l’environnement initial.

L’identité est un service.

Pas le cœur du Créateur.

---

## Le Créateur sans compte externe

Une version locale ou de développement devrait idéalement pouvoir fonctionner sans dépendre d’un fournisseur d’authentification externe.

Cela simplifie les tests.

Puis la couche d’identité peut être branchée.

C’est une conséquence logique de la modularité.

---

## Le cœur local

Le cœur du Créateur devrait pouvoir :

ouvrir un projet;

manipuler un graphe;

exécuter une simulation locale;

mesurer;

sauvegarder;

sans nécessiter immédiatement tous les services de plateforme.

Cette indépendance rend l’architecture plus robuste.

---

## Le mode hors ligne

Un futur mode hors ligne pourrait même exister pour certaines fonctions.

Mais il ne faut pas le promettre tant que l’architecture ne le permet pas.

Le point important est de ne pas coupler inutilement le canevas à des services externes.

---

## La sauvegarde locale et distante

Le projet peut distinguer :

draft local;

version synchronisée;

version publiée.

Chaque couche possède un statut.

Cela évite d’envoyer involontairement des données privées.

---

## Le conflit de version

Si deux sessions modifient le même objet, le système doit détecter le conflit.

Pas écraser silencieusement.

Diff.

Choix.

Merge.

C’est une difficulté classique des outils collaboratifs.

La provenance doit survivre.

---

## La présence multi-utilisateur

À terme, plusieurs personnes peuvent regarder une même vitrine.

Peut-être collaborer.

Mais la première priorité reste l’isolement et la stabilité.

La présence temps réel peut venir plus tard.

---

## Le Créateur n’a pas besoin de tout faire aujourd’hui

Cette phrase est importante.

L’ambition du système est immense.

Mais l’implémentation doit rester incrémentale.

Le T0 visuel a une valeur.

Le premier cycle fonctionnel aura une valeur.

Le premier module réellement sauvegardé aura une valeur.

La première cristallisation honnête aura une valeur.

Le projet peut grandir étape par étape.

---

## Un seul chemin complet vaut mieux que cent boutons

Si une fonctionnalité traverse réellement :

création;

exécution;

mesure;

sauvegarde;

version;

preuve;

alors elle valide beaucoup plus d’architecture que cent boutons décoratifs.

Cette règle peut guider la roadmap.

---

## Le chemin vertical

Choisir une seule fonction et l’emmener de haut en bas.

Par exemple :

Modular Cycle.

Créer.

Exécuter.

Mesurer.

Perturber.

Comparer.

Cristalliser.

Publier.

Ce chemin vertical est un excellent test de plateforme.

---

## Puis élargir

Une fois la chaîne solide :

Gate.

Iterator.

Clock.

Graph Router.

Signal Lab.

La largeur vient après la profondeur.

---

## La dette de maquette

Une maquette peut cacher beaucoup de fonctions simulées.

Il faut progressivement remplacer chaque DEMO par une implémentation.

Le statut doit changer uniquement lorsqu’elle existe.

Cette migration doit être suivie.

---

## Un registre des fonctionnalités

Le Créateur peut avoir une table :

~~~text
FEATURE                  STATUS
Canvas pan/zoom          IMPLEMENTED
Module drag              IMPLEMENTED
Stability test           DEMO
X72 connector            NOT CONNECTED
Public visitor mode      PARTIAL
~~~

Une telle table peut éviter énormément de confusion.

---

## Le statut PARTIAL

Il peut être utile d’ajouter :

**PARTIEL.**

Certaines fonctions existent mais pas entièrement.

Cependant, chaque statut supplémentaire augmente le vocabulaire.

Il faut rester parcimonieux.

---

## Le test de réalité avant release

Avant une release :

cliquer chaque bouton.

Vérifier chaque badge.

Comparer l’interface au backend.

Retirer ou marquer ce qui ne fonctionne pas.

C’est un test de vérité de l’interface.

---

## La documentation intégrée

Le Créateur doit pouvoir expliquer ses objets.

Un bouton d’aide.

Une définition.

Une formule.

Un exemple.

Le logiciel devient plus facile à transmettre.

---

## Le lien vers la Bible

La Bible Brutus peut devenir la documentation longue.

Le Créateur montre un objet.

Un lien ouvre le passage pertinent.

Histoire.

Définition.

Méthode.

La plateforme et le livre se renforcent.

---

## Le livre ne doit pas être requis pour utiliser le logiciel

L’interface doit rester suffisamment claire.

La Bible donne la profondeur.

Pas les instructions essentielles cachées.

Un utilisateur doit pouvoir accomplir une tâche sans lire cent pages.

---

## Le tutoriel

Un tutoriel peut guider :

Créer un premier module.

Construire le cycle modulo 9.

Lancer.

STEP.

Perturber.

Lire la période.

Sauvegarder.

Cette expérience enseigne le langage du Créateur.

---

## Le tutoriel comme test de design

Si le tutoriel doit expliquer dix exceptions pour une action simple, l’interface a probablement un problème.

Le onboarding devient donc lui aussi un test de qualité.

---

## La Brutothèque comme mémoire de l’apprentissage

Un nouveau créateur peut consulter des exemples validés.

Pas seulement des documents.

Des objets exécutables.

Cela transforme la bibliothèque en école.

---

## Copier un exemple

L’utilisateur ne modifie pas l’original.

Il crée un fork.

Puis expérimente.

La provenance reste.

L’apprentissage ne détruit pas le modèle.

---

## Le laboratoire personnel

Chaque créateur possède son espace.

Ses brouillons.

Ses forks.

Ses expériences.

Il peut choisir ce qu’il publie.

Cette autonomie est importante.

Le Royaume offre l’infrastructure.

Le créateur garde son travail.

---

## Le public ne voit pas le brouillon

Sauf publication explicite.

Un brouillon peut être faux.

Incomplet.

Confidentiel.

La plateforme doit respecter cela.

---

## La vitrine comme publication sélective

Le créateur choisit une plaque.

Une version.

Des résultats.

Puis publie.

La vitrine montre cette version précise.

Pas automatiquement le live du laboratoire.

Cette distinction est essentielle.

---

## Le live privé peut continuer à changer

Pendant que la vitrine montre v1.0, le laboratoire peut travailler sur v1.1.

Le public continue à voir la version publiée.

Jusqu’à une nouvelle publication.

C’est le même principe qu’une release.

---

## La reproductibilité publique

Une publication peut offrir :

manifest;

protocole;

résultats;

version;

hash;

fichiers autorisés.

Le visiteur peut reproduire dans son propre laboratoire si la licence le permet.

La vitrine devient une porte vers la recherche partagée.

---

## Le fork public

Un bouton futur :

**FORKER DANS MON LABORATOIRE.**

Il copie la version publique.

Conserve le parent.

Puis l’utilisateur peut modifier sa copie.

Cette fonction serait une traduction très directe de Git pour des objets scientifiques modulaires.

---

## Le mérite

Le graphe de provenance permet de conserver le créateur original.

Même après plusieurs forks.

Cela aide l’attribution.

L’évolution ne doit pas effacer les contributions.

---

## Le Créateur comme plateforme de continuité

À ce stade, l’atelier dépasse l’interface.

Il devient un système de continuité.

Une idée entre aujourd’hui.

Une autre personne peut la reprendre plus tard.

Voir sa généalogie.

Comprendre ses tests.

Créer une nouvelle version.

C’est exactement ce que le chapitre 3 cherchait à rendre possible.

---

## Le cercle se referme

Laisser une trace.

Rencontrer Astra.

Construire le Royaume.

Apprendre la preuve.

Définir Brutus.

Puis créer l’atelier où tout cela peut fonctionner ensemble.

Chaque chapitre prépare le suivant.

Le Créateur est le premier endroit où toutes les règles précédentes doivent coexister.

---

## Une interface qui porte une philosophie

Chaque détail peut traduire une règle.

Badge NON CONNECTÉ :

ne pas inventer l’état.

Badge INDÉTERMINÉ :

ne pas forcer la conclusion.

Version :

ne pas écraser l’histoire.

Hash :

identifier exactement.

Protocole :

définir le test.

Vitre :

séparer lecture et écriture.

GO :

maintenir l’agence humaine.

Interphone texte :

limiter la surface d’entrée.

Stability Lab :

attaquer nos propres idées.

Brutothèque :

conserver la provenance.

Le design devient philosophie exécutable.

---

## Le Créateur doit pouvoir nous faire perdre

Voilà son test ultime.

Nous entrons avec une idée magnifique.

Nous espérons qu’elle fonctionne.

Le système mesure.

Perturbe.

Compare.

Puis il affiche :

**INSTABLE SELON PROTOCOLE.**

Ou :

**INDÉTERMINÉ.**

Ou :

**REJETÉ.**

Si nous acceptons ce résultat et gardons l’échec, Le Créateur remplit sa mission.

---

## Le Créateur doit aussi savoir célébrer correctement

Lorsqu’une expérience réussit, le système peut reconnaître le résultat.

Mais avec précision.

**STABLE SELON PRT-0042.**

**20/20 RÉPÉTITIONS.**

**HASH = …**

**VERSION = 1.0.**

La réussite devient plus belle parce qu’elle est traçable.

---

## La joie après la mesure

Le moment où une idée survit aux perturbations n’est pas moins excitant que la découverte initiale.

Il l’est peut-être davantage.

Parce que le wow a maintenant une structure.

---

## Le Créateur n’est pas le juge final du monde

Même un excellent laboratoire logiciel reste limité.

Il teste selon les modèles et les instruments qu’il possède.

Une validation dans Le Créateur ne remplace pas une expérience physique lorsque l’affirmation concerne la nature.

Le système doit savoir où s’arrête son autorité.

---

## L’atelier de l’inconnu

Finalement, Le Créateur est un endroit où l’inconnu peut rester visible.

On n’a pas besoin de remplir tous les trous.

Un port non défini peut être marqué.

Une mesure manquante.

Un moteur non connecté.

Une hypothèse non testée.

L’inconnu devient un objet de travail.

Pas une honte.

---

## La première grande loi du Créateur

Je veux donc fixer une première loi :

> **Une fonction non réalisée est marquée À IMPLÉMENTER.  
> Un moteur absent est marqué NON CONNECTÉ.  
> Une donnée fictive est marquée DEMO.  
> Un résultat insuffisant est marqué INDÉTERMINÉ.**

Cette loi protège la vérité de l’interface.

---

## La deuxième grande loi

> **FORME ≠ STABILITÉ ≠ PREUVE**

Le canevas propose.

Le Stability Lab teste.

Le protocole définit le statut.

---

## La troisième grande loi

> **LE LOGICIEL DOIT POUVOIR NOUS CONTREDIRE.**

Sinon le laboratoire n’est qu’un miroir flatteur.

---

## La quatrième grande loi

> **UNE MODIFICATION SUBSTANTIELLE CRÉE UNE NOUVELLE VERSION.**

Parce que le futur doit pouvoir reconstruire le passé.

---

## La cinquième grande loi

> **PUBLIC READ — OWNER WRITE — ADMIN APPROVE.**

Parce que voir n’est pas posséder.

Et posséder n’est pas approuver toute action de plateforme.

---

## La sixième grande loi

> **X72 RESTE EXTERNE JUSQU’À CONNEXION RÉELLE ET VÉRIFIÉE.**

La présence du connecteur n’est pas la présence du moteur.

---

## La septième grande loi

> **LE GO HUMAIN RESTE UNE FRONTIÈRE RÉELLE POUR LES ACTIONS SENSIBLES.**

L’IA peut préparer.

Le système peut simuler.

Le créateur décide.

---

## La huitième grande loi

> **LA PROVENANCE VOYAGE AVEC L’OBJET.**

Source.

Auteur.

Version.

Parent.

Tests.

Hash.

La trace ne doit pas être séparée de ce qu’elle décrit.

---

## La neuvième grande loi

> **UN ÉCHEC DOCUMENTÉ RESTE UN RÉSULTAT.**

La Brutothèque ne conserve pas seulement les vainqueurs.

Elle conserve les leçons.

---

## La dixième grande loi

> **LE CRISTAL EST UNE VERSION FIGÉE VALIDÉE SELON UN PROTOCOLE, PAS UNE VÉRITÉ UNIVERSELLE.**

Cette phrase protège le mot le plus symbolique de notre architecture.

---

## Le Créateur comme héritage pratique

Si je veux laisser quelque chose à l’humanité, un livre peut raconter.

Un dépôt peut montrer.

Mais un atelier peut permettre de refaire.

Le Créateur possède donc une place particulière.

Il peut devenir la partie manipulable de l’héritage.

Le lecteur ne reçoit pas seulement les conclusions.

Il reçoit les outils.

---

## Le futur utilisateur

J’imagine une personne qui ne connaît rien à notre histoire.

Elle ouvre Le Créateur.

Elle prend un module public.

Elle lit son contrat.

Elle le fork.

Change un paramètre.

Lance une expérience.

Observe.

Obtient un résultat différent.

Puis comprend pourquoi.

À ce moment-là, le projet a vraiment traversé.

---

## Le futur critique

Une autre personne ouvre la même expérience.

Elle découvre une erreur.

Elle construit un meilleur protocole.

La conclusion change.

C’est aussi une réussite.

L’héritage utile doit permettre la contradiction.

---

## Le futur constructeur

Une troisième personne assemble plusieurs Brutus.

Crée une plaque que nous n’avions jamais imaginée.

Notre architecture devient une matière première.

C’est probablement l’une des formes les plus fortes de transmission.

---

## Le Créateur ne doit pas exiger de nous connaître

Le futur utilisateur ne devrait pas avoir besoin de connaître les blagues privées.

Les anciennes conversations.

Les surnoms.

La chronologie personnelle.

Tout cela enrichit la Bible.

Mais l’atelier doit pouvoir se tenir seul.

Contrats.

Aide.

Documentation.

Exemples.

---

## Pourtant, l’histoire reste à côté

Et si l’utilisateur veut comprendre pourquoi le mot Brutus existe.

Pourquoi le GO compte.

Pourquoi X72 reste externe.

Pourquoi le cristal possède ce statut.

Alors la Bible explique.

L’outil fonctionne sans le récit.

Le récit donne la profondeur à l’outil.

---

## La Brutothèque comme pont vers les autres

Le Créateur prépare naturellement le chapitre suivant.

Parce qu’un atelier construit seulement pour son créateur serait incomplet.

Si la Brutothèque peut publier.

Si la vitre peut montrer.

Si le fork peut transmettre.

Alors une nouvelle question apparaît :

**qu’est-ce que nous construisons pour les autres ?**

Pas pour impressionner.

Pas pour prouver que nous avions raison.

Pour rendre quelque chose utilisable.

Compréhensible.

Reproductible.

Modifiable.

---

## Le passage du personnel au transmissible

Une idée personnelle peut devenir un objet.

L’objet peut devenir un protocole.

Le protocole peut devenir une expérience.

L’expérience peut produire une version cristallisée.

Cette version peut entrer dans la Brutothèque.

Puis être publiée.

Alors le travail quitte progressivement son créateur.

Il devient transmissible.

---

## Une chaîne complète

Nous pouvons maintenant écrire une chaîne beaucoup plus large :

~~~text
INTUITION
→ IDÉE
→ GÉOMÉTRIE / FORMULE
→ CONTRAT
→ MODULE / BRUTUS
→ PLAQUE
→ EXPÉRIENCE
→ PROTOCOLE
→ MESURES
→ TESTS
→ REPRODUCTIBILITÉ
→ VALIDATION SELON PROTOCOLE
→ CRISTALLISATION
→ BRUTOTHÈQUE
→ PUBLICATION / FORK
→ NOUVELLE LIGNÉE
~~~

Cette chaîne ne dit pas que tout atteindra la fin.

Elle dit seulement que le chemin existe.

---

## Une idée peut sortir à chaque étape

Rejetée après le calcul.

Rejetée après la dynamique.

Indéterminée après la mesure.

Archivée après l’expérience.

C’est très bien.

Le Créateur n’est pas une chaîne de production où chaque idée devient un produit.

C’est un filtre construit pour préserver ce qui résiste.

---

## La sélection n’est pas esthétique

Un beau module ne gagne pas parce qu’il est beau.

Un module stable ne gagne pas automatiquement parce qu’il est stable.

Une idée populaire ne gagne pas parce qu’elle est populaire.

Le critère appartient au protocole.

Cette discipline doit rester visible jusque dans l’interface.

---

## L’imagination reste libre

Tout cela pourrait donner l’impression d’un système très strict.

Mais la liberté est au début.

Créer.

Dessiner.

Imaginer.

Assembler.

Le protocole n’arrive que lorsqu’on veut donner un statut plus fort.

Cette séparation protège l’imagination au lieu de la limiter.

---

## Le Créateur comme lieu des deux vitesses

**Vitesse 1 : exploration.**

Rapide.

Visuelle.

Libre.

**Vitesse 2 : validation.**

Lente.

Versionnée.

Mesurée.

Documentée.

Le logiciel doit permettre de passer de l’une à l’autre sans confusion.

---

## Le bouton PROMOUVOIR

Un jour, l’interface pourrait avoir une action :

**PROMOUVOIR EN CANDIDAT.**

À ce moment :

snapshot;

ID;

version;

contrat minimal;

protocole à définir.

Le brouillon entre dans la chaîne de validation.

Cette opération peut devenir le vrai seuil entre création libre et recherche structurée.

---

## Le bouton RETOUR EN BROUILLON

Si le candidat est trop incomplet, il peut revenir.

Pas de honte.

Le statut n’est pas une récompense.

C’est un état.

---

## Le Créateur doit conserver la liberté de revenir

Une architecture rigide où chaque promotion est irréversible deviendrait pénible.

La seule chose qui doit rester irréversible est l’histoire.

La version ancienne reste.

Le travail actuel peut évoluer.

---

## La trace comme invariant

On peut modifier le présent.

On ne doit pas modifier silencieusement le passé.

Voilà un invariant de toute la plateforme.

---

## La fin du chapitre

Le Créateur est encore jeune.

Certaines fonctions sont des concepts.

Certaines existent déjà visuellement.

D’autres doivent être implémentées.

X72 reste une frontière externe tant qu’il n’est pas réellement connecté.

La Brutothèque doit encore devenir une vraie mémoire d’objets.

Le Stability Lab doit passer du concept au moteur de tests.

Le Laboratoire des chiffres doit gagner ses protocoles.

Les permissions doivent devenir des règles serveur réelles.

L’interphone doit rester une passerelle étroite.

Il reste énormément à construire.

Mais quelque chose a changé.

Nous ne parlons plus seulement d’idées.

Nous avons commencé à construire l’endroit où elles pourront être jugées.

Et cet endroit possède déjà une philosophie :

> **LA FORME PROPOSE.  
> LA DYNAMIQUE SÉLECTIONNE.  
> LE TEST PERTURBE.  
> LA MESURE OBSERVE.  
> LA REPRODUCTIBILITÉ CONFIRME LE PROTOCOLE.  
> LA CRISTALLISATION FIGE UNE VERSION.  
> LA BRUTOTHÈQUE CONSERVE.  
> L’ASSEMBLEUR CONSTRUIT.**

Puis une règle qui domine les autres :

> **LE LOGICIEL DOIT POUVOIR NOUS CONTREDIRE.**

Si Le Créateur réussit cela, il ne sera pas seulement une interface.

Il deviendra une manière de travailler.

Une manière de transformer l’imagination en objets que d’autres peuvent examiner.

Et lorsqu’un objet peut être examiné par quelqu’un d’autre, une nouvelle responsabilité apparaît.

Il faut penser à celui qui recevra.

À celui qui apprendra.

À celui qui reprendra.

À celui qui corrigera.

À celui qui construira après nous.

C’est là que commence le chapitre suivant.

**Chapitre 9 — Ce que nous construisons pour les autres.**
