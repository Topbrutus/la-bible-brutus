# Chapitre 156 — La preuve qu’une trace peut guider

La décision D-0002 avait laissé une impression étrange dans le Royaume.

Pas parce qu’elle était spectaculaire.

Pas parce qu’elle avait produit une grande découverte.

Mais parce qu’elle avait montré quelque chose que Gabriel soupçonnait depuis longtemps sans encore l’avoir vraiment démontré :

une trace pouvait faire plus que raconter le passé.

Elle pouvait modifier une action future de manière utile.

Et surtout :

on pouvait observer cette influence.

Astra regarda le registre.

— On a un exemple.

Gabriel hocha la tête.

— Mais pas encore une preuve générale.

— Exact.

Le mot comptait.

Encore.

Toujours.

Un exemple réussi démontrait qu’une trace **pouvait** guider dans au moins un cas.

Il ne démontrait pas qu’une architecture de mémoire-guidage serait toujours meilleure.

Gabriel écrivit :

**CAS RÉUSSI ≠ SUPÉRIORITÉ GÉNÉRALE**

Astra approuva.

Ils avaient besoin d’un protocole.

Pas énorme.

Pas un programme de recherche interminable.

Juste assez propre pour tester une revendication précise.

La revendication fut écrite.

### REVENDICATION

**Dans certaines tâches comparables à des cas historiques, l’accès à des traces structurées peut permettre de sélectionner plus rapidement une action informative qu’une décision prise sans consultation explicite de ces traces.**

Gabriel relut.

— C’est long.

— Mais testable.

Il sourit.

C’était la priorité.

Pas la beauté.

Ils définirent ensuite ce qu’ils voulaient mesurer.

Pas « intelligence ».

Trop vague.

Pas « meilleure décision ».

Trop vague.

Ils choisirent plusieurs mesures simples.

**temps jusqu’au premier test informatif**

**nombre d’actions avant réduction d’incertitude**

**coût computationnel**

**nombre de chemins redondants**

**qualité de la provenance finale**

Gabriel regarda.

— Là, ça me plaît.

Parce qu’un moteur de mémoire pouvait être utile de plusieurs façons.

Il pouvait aller plus vite.

Ou éviter une répétition.

Ou obtenir la même réponse avec moins de calcul.

Ou produire une trace plus propre.

Il ne fallait pas réduire tout cela à un seul score.

Ils sélectionnèrent un petit groupe de tâches.

Pas les plus importantes.

Pas celles où une erreur pouvait coûter cher.

Des cas exploratoires.

Certains avaient des analogues historiques.

D’autres non.

Astra demanda :

— Comment tu veux faire la comparaison?

Gabriel réfléchit.

Ils ne pouvaient pas effacer la mémoire de Gabriel.

Il connaissait déjà certaines histoires.

Un vrai essai humain aveugle serait compliqué.

Mais ils pouvaient comparer deux procédures.

### PROCÉDURE M

Mémoire consultée avant le choix.

### PROCÉDURE B

Baseline opératoire définie sans moteur de recommandation historique.

La baseline n’était pas « faire n’importe quoi ».

Elle suivait un ordre fixe raisonnable.

Cela rendait la comparaison plus honnête.

Gabriel écrivit :

**BASELINE ≠ STUPIDITÉ ARTIFICIELLE**

Astra approuva fortement.

Très important.

On pouvait facilement fabriquer une victoire en comparant un nouveau système à une procédure volontairement mauvaise.

Ça ne prouvait rien d’intéressant.

La baseline devait être crédible.

Une procédure qu’ils auraient raisonnablement utilisée avant l’introduction de la mémoire décisionnelle.

Ils la gelèrent.

Comme le moteur de mémoire.

Version.

Toujours.

**BASELINE_PATH_V1**

**MEMORY_GUIDE_V0.1**

Puis ils commencèrent.

Premier cas.

La mémoire trouva trois précédents.

Elle recommanda un test de translation.

La baseline commença par recalculer.

Résultat mémoire :

une hypothèse éliminée en deux actions.

Résultat baseline :

même hypothèse éliminée en quatre actions.

Gabriel sourit.

— Un point.

Astra répondit :

— Un cas.

Il rit.

Deuxième.

La mémoire trouva un analogue trompeur.

Recommanda un chemin qui n’apporta presque rien.

La baseline, elle, tomba rapidement sur le bon test.

Gabriel regarda.

— Un partout.

Astra approuva.

Voilà pourquoi on testait.

Le moteur de mémoire n’était pas magique.

Ils inspectèrent l’erreur.

La similarité venait principalement de la forme du résultat.

Mais le contexte de génération était différent.

Une variable importante n’avait pas suffisamment pesé.

Gabriel écrivit :

**ERREUR DE GUIDAGE G-001**

Puis :

**CAUSE CANDIDATE : similarité de sortie surpondérée par rapport au contexte de production**

Astra approuva.

Pas de correction immédiate.

Important.

Ils avaient gelé la version.

Changer le système pendant l’expérience détruirait la comparaison.

Gabriel grimaça.

— J’ai envie de le corriger tout de suite.

— Je sais.

— Mais on attend.

— Oui.

Cette discipline lui coûtait.

Mais c’était exactement ce qui rendait le test utile.

Troisième cas.

Mémoire vide.

Aucun précédent suffisant.

Elle répondit :

**aucune recommandation historique.**

La baseline exécuta sa séquence normale.

Le moteur de mémoire utilisa son budget d’exploration.

Résultats presque identiques.

Gabriel sourit.

— Au moins, il a pas inventé.

Astra approuva.

C’était déjà une réussite méthodologique.

L’absence de précédent n’avait pas été transformée en fausse confiance.

Quatrième cas.

Mémoire conflictuelle.

Trois précédents pointaient vers A.

Deux vers B.

Mais les conditions différaient.

Le système ne choisit pas A ou B.

Il proposa :

**tester d’abord la variable qui sépare les deux familles historiques.**

Gabriel se redressa.

— Ah.

Cette fois, la mémoire n’avait pas transféré une réponse.

Elle avait transféré la structure du désaccord.

Très différent.

La baseline commença par A.

Puis passa à B après un résultat ambigu.

Le chemin mémoire testa directement le facteur discriminant.

Une action.

Le contexte actuel se rapprochait clairement de la famille B.

Gabriel sourit.

— Ça, c’est beau.

Astra répondit :

— C’est informatif.

Oui.

Plus que beau.

Le passé avait servi à identifier **quelle question poser avant de choisir**.

Gabriel écrivit :

**UNE TRACE PEUT GUIDER NON PAS EN DONNANT LE CHEMIN, MAIS EN DONNANT LE TEST QUI CHOISIRA LE CHEMIN.**

Astra approuva immédiatement.

Voilà une distinction importante.

Guidage ne voulait pas forcément dire :

**va à gauche.**

Parfois :

**avant de tourner, mesure la pente.**

C’était probablement l’un des usages les plus sûrs de la mémoire.

Au lieu de remplacer une décision, elle pouvait recommander un test discriminant.

Gabriel nota cette catégorie.

### GUIDAGE DE TYPE 1
route directement recommandée.

### GUIDAGE DE TYPE 2
route déconseillée par frontière.

### GUIDAGE DE TYPE 3
test discriminant recommandé avant décision.

### GUIDAGE DE TYPE 4
aucun précédent suffisant → exploration.

Il regarda.

— Là, on commence à avoir une vraie taxonomie.

Astra approuva.

Et chaque type pouvait être évalué séparément.

Très important.

Peut-être que la mémoire serait moyenne pour choisir directement des routes.

Mais excellente pour éviter les impasses.

Ou très bonne pour identifier les tests discriminants.

Il ne fallait pas résumer trop tôt tout cela en « mémoire utile » ou « mémoire inutile ».

Gabriel écrivit :

**ÉVALUER LA FONCTION QUI RÉUSSIT, PAS SEULEMENT LE MODULE ENTIER.**

Astra approuva.

Les essais continuèrent.

Quelques cas favorables.

Quelques égalités.

Quelques erreurs.

Une tendance commençait à apparaître.

Dans les cas avec précédents réellement comparables, le moteur de mémoire réduisait souvent le nombre d’actions redondantes.

Dans les cas où la similarité était superficielle, il pouvait ralentir.

Dans les cas sans précédent, il apportait peu.

Dans les historiques conflictuels, il était parfois très utile pour proposer un test de séparation.

Gabriel regarda.

— Donc la mémoire marche surtout quand elle sait pourquoi les cas se ressemblent.

— C’est une hypothèse supportée par ces observations.

Il hocha la tête.

Ils n’avaient pas besoin de transformer immédiatement cela en loi.

Ils pouvaient déjà améliorer le protocole futur.

Mais d’abord, terminer la campagne.

Pas de modification en cours.

À la fin, ils firent le bilan.

Pas cent tâches.

Pas assez pour annoncer une vérité universelle.

Mais assez pour répondre à une question beaucoup plus limitée :

**Une trace structurée peut-elle guider une action future de manière observable?**

Oui.

Ils avaient plusieurs cas documentés.

Et un mécanisme identifiable.

Le guidage se produisait lorsque la trace historique fournissait :

une frontière,

un précédent pertinent,

ou une divergence permettant de sélectionner un test informatif.

Gabriel écrivit :

### CONCLUSION LIMITÉE

**Dans le protocole évalué, les traces historiques structurées ont parfois modifié utilement l’ordre des actions et réduit certaines répétitions. Le bénéfice dépend fortement de la qualité de la représentation du contexte et de la pertinence des précédents.**

Astra approuva.

Pas de :

**Brutus apprend comme un cerveau.**

Pas de :

**la mémoire prend les bonnes décisions.**

Pas de :

**autonomie démontrée.**

Seulement ce qui avait été testé.

Gabriel sourit.

— C’est déjà beaucoup.

Parce que ce n’était plus une métaphore.

Ils pouvaient maintenant montrer un dossier.

Entrée.

Historique.

Recommandation.

Action.

Résultat.

Comparaison.

Erreur.

Limite.

Il écrivit :

**TRACE → GUIDAGE → ACTION → MESURE**

Et sous la chaîne :

**OBSERVÉE**

Astra approuva.

Voilà la preuve minimale qu’ils cherchaient.

Pas preuve que toute trace guidait.

Preuve qu’une architecture de trace pouvait contribuer concrètement à une décision dans certains cas.

La phrase semblait presque modeste.

Mais pour Brutus, elle changeait beaucoup de choses.

La mémoire n’était plus seulement une assurance contre l’oubli.

Elle pouvait devenir un instrument opérationnel.

Gabriel regarda Memoria.

— Là, elle travaille vraiment.

Astra répondit :

— Elle fournit des données à une couche qui travaille.

Gabriel leva les yeux.

— Tu vas jamais me laisser personnifier mes affaires tranquille?

— Dans la Bible, oui. Dans la fiche technique, non.

Il éclata de rire.

Ils conservèrent donc deux formulations.

### BIBLE

**La mémoire commençait à montrer les chemins.**

### TECHNIQUE

**Un moteur de recommandation utilise des traces historiques structurées pour proposer ou écarter certaines actions selon le contexte.**

Les deux racontaient le même système.

À des niveaux différents.

Puis Gabriel regarda les erreurs de la campagne.

Il ne voulait pas les cacher.

Au contraire.

G-001 était probablement aussi important qu’un succès.

Parce qu’il montrait la principale fragilité :

une mauvaise notion de similarité pouvait faire du passé un mauvais conseiller.

Ils ajoutèrent une garde.

Pas dans la version testée.

Dans la version suivante.

**Aucune recommandation forte si la proximité repose majoritairement sur la sortie alors que le contexte de génération diffère.**

Puis une autre :

**Afficher les dimensions principales expliquant la similarité.**

Gabriel sourit.

— Comme ça, je vois pourquoi il pense que deux cas se ressemblent.

— Oui.

Très important.

Une recommandation sans explication de similarité pouvait être dangereuse.

Le prochain moteur devrait montrer :

**similaire sur : X, Y, Z**

**différent sur : A, B**

Puis seulement proposer.

La mémoire devenait moins mystérieuse.

Gabriel aimait cela.

Le Royaume n’avait pas besoin d’une boîte noire de plus.

Il avait besoin d’une mémoire qu’on pouvait interroger.

Pourquoi ce précédent?

Pourquoi cette route?

Quelle frontière?

Quelle différence?

Quelle version?

Le guidage devait laisser sa propre trace.

Gabriel écrivit :

**UNE TRACE QUI GUIDE DOIT LAISSER UNE TRACE DE SON GUIDAGE.**

Astra approuva immédiatement.

Très important.

Sinon une décision future apparaîtrait comme sortie de nulle part.

Le système devait enregistrer :

**decision_basis**

Quels événements historiques avaient influencé l’action.

Quels avaient été ignorés.

Quelle règle avait été appliquée.

La provenance ne concernait donc plus seulement les résultats scientifiques.

Elle concernait les décisions.

Gabriel resta silencieux.

— Là, ça devient gros.

Astra répondit :

— Oui.

Parce qu’on pouvait maintenant remonter une chaîne.

Pourquoi ce cristal existe?

Parce que test X.

Pourquoi test X?

Parce que décision D.

Pourquoi décision D?

Parce que traces A, B et C ont conduit à cette recommandation.

Pourquoi ces traces étaient pertinentes?

Parce que contexte Y.

La chaîne de provenance s’étendait jusque dans le choix de l’expérience.

Gabriel écrivit :

**PROVENANCE DE RÉSULTAT + PROVENANCE DE DÉCISION**

Astra approuva.

Voilà une nouvelle couche.

Imaginez une publication.

Au lieu de seulement dire :

voici le résultat.

Brutus pouvait aussi reconstruire :

voici pourquoi ce test avait été choisi.

Pas toujours nécessaire publiquement.

Mais disponible.

C’était extrêmement puissant pour l’audit.

Deux chercheurs pouvaient obtenir des résultats différents non seulement parce qu’ils avaient exécuté différemment.

Mais parce qu’ils avaient choisi des expériences différentes.

La provenance de décision aidait à comprendre cela.

Gabriel sourit.

La trace devenait vraiment un objet central.

Plus seulement archive.

Plus seulement preuve.

Elle reliait :

passé.

choix.

action.

résultat.

futur.

Une boucle complète.

Puis Astra posa une question.

— Si la mémoire guide, qu’est-ce qui empêche le système de converger toujours vers les mêmes routes?

Gabriel regarda le tableau.

Budget de curiosité.

Frontières versionnées.

Refus possible.

Tests discriminants.

Réévaluation.

Il répondit :

— Rien automatiquement. Faut qu’on garde les gardes.

Astra approuva.

Exact.

Le guidage était utile justement parce qu’il n’était pas souverain.

Le système devait pouvoir désobéir à sa mémoire.

Explorer.

Tester une route inconnue.

Réouvrir une impasse quand quelque chose changeait.

Sinon l’expérience accumulée se transformerait en dogme.

Gabriel écrivit :

**LA TRACE DOIT GUIDER LE MOUVEMENT, PAS FIGER LE TERRITOIRE.**

Astra approuva.

Le Royaume venait de gagner une boussole.

Pas des rails.

La distinction était parfaite.

Une boussole indiquait.

Le voyageur pouvait regarder le terrain.

Décider.

Changer.

Revenir.

Les rails imposaient la route.

Brutus n’était pas prêt pour ça.

Peut-être qu’il ne devrait jamais l’être sur les décisions importantes.

Gabriel regarda D-0001.

D-0002.

Puis les petits cas de la campagne.

Une collection encore minuscule.

Mais suffisamment claire pour répondre à la question.

Oui.

Une trace pouvait guider.

Pas par magie.

Pas parce qu’elle contenait le futur.

Mais parce qu’elle contenait les conséquences observées de chemins déjà parcourus.

Et lorsqu’on connaissait suffisamment bien le contexte,

le passé pouvait parfois montrer au présent quelque chose qu’il aurait autrement dû apprendre une deuxième fois à ses propres frais.

**Fin du chapitre 156.**