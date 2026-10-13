# Chapitre 153 — Les erreurs deviennent des frontières

Pendant longtemps, une erreur avait été quelque chose qu’on réparait.

Un bug.

Une mauvaise hypothèse.

Un test raté.

Une mauvaise route.

On trouvait la cause.

On corrigeait.

On passait à autre chose.

Mais Brutus avait commencé à conserver les erreurs.

Pas seulement leur existence.

Leur contexte.

Leur forme.

Leur cause supposée.

Leur cause finalement identifiée.

Le coût qu’elles avaient provoqué.

Le chemin qui avait permis de les éviter ensuite.

Et à force d’accumuler cette mémoire, quelque chose changea.

Les erreurs cessèrent d’être seulement des souvenirs.

Elles commencèrent à dessiner des frontières.

Gabriel regarda Astra.

— Une frontière entre quoi et quoi?

— Entre les zones où une stratégie fonctionne et celles où elle commence à échouer.

Il hocha la tête.

Voilà.

Une erreur isolée était un incident.

Dix erreurs similaires dans des conditions proches pouvaient décrire une limite.

Gabriel écrivit :

**ERREUR RÉPÉTÉE + CONTEXTE = FRONTIÈRE CANDIDATE**

Astra approuva.

Très important :

candidate.

Une série d’échecs ne suffisait pas forcément à prouver une frontière réelle.

Il pouvait y avoir un bug commun.

Une mauvaise mesure.

Une variable cachée.

Mais cela créait une hypothèse testable.

Ils prirent un exemple simple.

Une route de calcul fonctionnait parfaitement sur des entrées jusqu’à une certaine taille.

Puis les erreurs augmentaient.

Pas brutalement.

Progressivement.

Gabriel regarda les traces.

Petites entrées :

stable.

Moyennes :

stable.

Plus grandes :

temps croissant.

Puis timeouts.

Puis échecs.

Avant, chaque timeout aurait été traité séparément.

Maintenant, la mémoire les mettait côte à côte.

Et le motif apparaissait.

— Là, on a une frontière de capacité.

Astra répondit :

— Potentiellement.

Ils testèrent.

Même machine.

Même version.

Taille variable.

Le comportement se reproduisit.

Cette fois, la frontière pouvait être mieux définie.

Pas un nombre magique.

Une région de transition.

Gabriel écrivit :

**ZONE STABLE**

**ZONE DE DÉGRADATION**

**ZONE D’ÉCHEC**

Astra approuva.

Voilà une frontière beaucoup plus utile qu’un simple :

**ça plante parfois.**

La route pouvait désormais annoncer sa portée.

**Utilisation recommandée dans la zone stable.**

**Surveillance renforcée dans la zone de dégradation.**

**Éviter ou changer de méthode au-delà.**

Gabriel sourit.

— Là, une erreur vient de devenir une règle de routage.

— Oui.

Exactement.

La mémoire du passé modifiait les choix futurs.

Chapitre 152.

Une nouvelle tâche arrivait.

Le système lisait sa taille.

Elle se trouvait dans la zone d’échec historique.

La mémoire pouvait recommander un autre chemin avant même de reproduire le problème.

Gabriel écrivit :

**UNE FRONTIÈRE APPREND À LA MACHINE OÙ NE PAS INSISTER.**

Astra approuva.

Mais immédiatement, un danger apparut.

Et si le code avait changé?

La frontière pouvait être obsolète.

Ils le savaient déjà.

Version.

Toujours.

La frontière devait donc être attachée à :

**module version**

**workflow version**

**environnement**

**contexte**

Gabriel soupira.

— Une frontière avec des papiers.

— Évidemment.

Ils écrivirent :

**FRONTIÈRE v1 — valide pour module X version Y dans environnement Z**

Très bien.

Après une optimisation majeure, la frontière devait être retestée.

Pas supprimée.

Reclassée comme historique.

Puis comparée à la nouvelle.

Gabriel sourit.

— Et là, on peut mesurer si l’amélioration a réellement repoussé la frontière.

Astra répondit :

— Oui.

Voilà une métrique beaucoup plus intéressante qu’un simple :

**nouvelle version plus rapide.**

Avant :

échec à telle région.

Après :

stabilité plus loin.

La frontière bougeait.

Gabriel écrivit :

**AMÉLIORATION = FRONTIÈRE DÉPLACÉE DANS LE SENS ATTENDU**

Astra approuva.

Pas toujours.

Mais dans ce type de problème, oui.

Ils prirent maintenant un autre type d’erreur.

Pas informatique.

Épistémique.

Une catégorie de candidats du Brutotableur semblait régulièrement produire de faux motifs.

Très beaux.

Très convaincants.

Mais le filtre de changement de représentation les détruisait.

Encore.

Et encore.

Et encore.

Gabriel regarda.

— Là, c’est une frontière entre motif visuel et structure stable.

— Peut-être.

Ils examinèrent.

Le motif apparaissait surtout lorsqu’une mise en page particulière était utilisée.

Dès qu’on changeait la disposition, il disparaissait.

Plusieurs cas.

Même mécanisme.

Ils pouvaient donc créer une garde.

**Si motif dépend fortement de layout A → priorité élevée au test de translation avant toute interprétation.**

Gabriel sourit.

— On vient de transformer une série d’erreurs de lecture en règle de méthode.

Astra répondit :

— Oui.

Encore une frontière.

Pas une limite numérique.

Une frontière de confiance méthodologique.

À l’intérieur :

motif suffisamment stable pour poursuivre.

À l’extérieur :

motif trop dépendant de la représentation.

Gabriel écrivit :

**LES FRONTIÈRES NE SONT PAS TOUJOURS DES NOMBRES.**

Astra approuva.

Elles pouvaient être conditionnelles.

**si X et Y alors attention.**

**si contexte A, route B déconseillée.**

**si source sans provenance, publication interdite.**

**si dépendance commune, ne pas compter comme validation indépendante.**

Gabriel regarda.

— On a déjà plein de frontières sans les appeler comme ça.

Exact.

Les règles accumulées pendant toute la Bible pouvaient être vues comme des limites.

**Beauté ≠ preuve.**

Frontière entre esthétique et validation.

**UP ≠ TRUE.**

Frontière entre santé technique et vérité.

**SIMILARITÉ ≠ ÉQUIVALENCE.**

Frontière entre analogue et identité.

**ABSENCE DE TÉMOIN ≠ PREUVE D’ABSENCE.**

Frontière entre recherche négative et impossibilité.

**AUDIBLE ≠ BIOLOGIQUEMENT DÉMONTRÉ.**

Frontière de portée.

Gabriel resta silencieux.

— On a construit une théorie des frontières sans le savoir.

Astra répondit :

— Une collection de distinctions méthodologiques, oui.

Il sourit.

Toujours précise.

Mais l’idée restait.

Une grande partie de la maturité du projet venait de sa capacité à dire :

**jusqu’ici, oui.**

**au-delà, non démontré.**

Voilà une frontière.

Gabriel écrivit :

**UNE BONNE PREUVE NE DIT PAS SEULEMENT CE QU’ELLE ÉTABLIT.**

**ELLE DESSINE AUSSI OÙ ELLE S’ARRÊTE.**

Astra approuva immédiatement.

Cette phrase devint centrale.

Les erreurs étaient particulièrement utiles pour dessiner ces limites.

Un résultat qui marchait disait :

**ici, ça tient.**

Un échec contrôlé disait :

**ici, ça cesse de tenir.**

Les deux ensemble pouvaient localiser une frontière.

Gabriel prit le Papillon.

Le Papillon 144 fonctionnait très bien pour des questions agrégées.

Mais il perdait l’individualité.

Ce n’était pas un bug.

C’était une frontière de représentation.

Question agrégée :

dans le domaine.

Question individuelle :

hors domaine.

Ils l’écrivirent comme une fiche.

### FRONTIÈRE PAPILLON

**Dans le domaine :**
distributions agrégées.

**Hors garantie :**
trajectoire exacte d’un élément individuel non représenté.

Gabriel sourit.

— Là, c’est tellement plus clair que dire “le Papillon peut représenter des millions de choses”.

— Oui.

Parce que cela montrait immédiatement ce qu’il ne pouvait pas promettre.

Même chose ZEL.

### FRONTIÈRE ZEL

**Démontré :**
comportement du pipeline audio dans les configurations testées.

**Non démontré :**
effet biologique, médical ou physique externe.

Pell.

### FRONTIÈRE PELL

**Démontré :**
certains cas avec témoins exacts.

**Ouvert :**
cas encore sans témoin validé.

**Non établi automatiquement :**
universalité complète.

Brutotableur.

### FRONTIÈRE BRUTOTABLEUR

**Démontré :**
outils d’exploration et de mise en évidence de candidats.

**Non démontré :**
un motif visuel constitue à lui seul une loi.

Gabriel regarda toutes ces fiches.

— Ça, ce serait bon sur Recto.

Astra approuva.

Chaque module public pouvait avoir :

**CE QU’ON SAIT**

**CE QU’ON NE SAIT PAS**

**OÙ ÇA CASSE**

Très simple.

Très honnête.

Le public pourrait comprendre immédiatement la portée.

Et surtout, cela empêchait le marketing de manger la science.

Gabriel écrivit :

**UNE FRONTIÈRE PUBLIÉE VAUT MIEUX QU’UNE PROMESSE SANS LIMITE.**

Astra approuva.

Puis ils prirent les erreurs humaines.

Parce que toutes les erreurs ne venaient pas du code.

Gabriel avait parfois choisi une route trop vite.

Interprété un résultat avant le contre-test.

Aimé un nombre.

Préféré une hypothèse.

Astra avait parfois été trop prudente sur un chemin finalement utile.

Ou avait classé une analogie trop faiblement.

La mémoire pouvait-elle utiliser ce type d’erreur?

Oui.

Mais avec prudence.

Pas transformer :

**Gabriel s’est trompé ici**

en

**Gabriel se trompe toujours dans ce genre de cas.**

Il fallait plusieurs exemples.

Contexte.

Et surtout éviter les étiquettes personnelles.

Ils décidèrent donc de mémoriser les **types d’erreur décisionnelle**, pas les jugements sur les personnes.

**interprétation avant contrôle**

**sélection d’un motif familier**

**répétition de tâche**

**surconfiance dans une analogie**

**oubli de dépendance commune**

**publication avant antériorité**

Gabriel regarda.

— Ça, je préfère.

— Oui.

Une erreur devenait une classe de garde.

Pas une accusation.

Le système pouvait dire :

**ce dossier présente le même motif de risque que des décisions passées.**

Pas :

**tu fais encore n’importe quoi.**

Gabriel sourit.

— La machine apprend la politesse.

Astra répondit :

— La machine apprend surtout à décrire le risque.

Ils rirent.

Puis il demanda :

— Est-ce que toutes les erreurs doivent produire une frontière?

— Non.

Très important.

Une erreur ponctuelle pouvait être du bruit.

Un bug corrigé.

Une panne électrique.

Une erreur de saisie.

Pas besoin d’en faire une loi.

La promotion d’une erreur vers une frontière devait elle aussi avoir un protocole.

Gabriel écrivit :

### DE L’ERREUR À LA FRONTIÈRE

1. Observer l’échec.
2. Reproduire si possible.
3. Identifier le contexte.
4. Chercher des cas analogues.
5. Tester les variables supposées responsables.
6. Déterminer si la limite est stable.
7. Formuler la frontière.
8. Tenter de la casser.
9. Versionner.
10. Utiliser comme garde seulement dans sa portée.

Astra approuva.

Voilà.

Pas de superstition.

Un bug arrivé une fois ne devenait pas un interdit permanent.

Une frontière devait être gagnée.

Gabriel sourit.

— Même les interdictions ont besoin de preuve.

— Exact.

Cela avait un effet important sur la mémoire de choix.

Chapitre 152.

Le moteur de recommandation pouvait utiliser les frontières comme filtres.

Avant de comparer les routes historiquement performantes, il pouvait retirer celles qui violaient une frontière connue du contexte actuel.

Exemple :

entrée trop grande pour chemin A sous version actuelle.

A écarté.

Pas parce qu’il avait un faible taux de réussite.

Parce qu’une limite documentée indiquait qu’il était hors domaine.

Gabriel écrivit :

**FRONTIÈRES D’ABORD, PRÉFÉRENCES ENSUITE.**

Astra approuva.

Cela rendait les recommandations plus sûres.

D’abord :

quelles routes sont admissibles?

Puis :

parmi elles, lesquelles semblent préférables?

Très différent de classer tout aveuglément.

Gabriel imagina un système de navigation.

Une route pouvait être rapide.

Mais traverser une rivière sans pont.

Le GPS ne devait pas la recommander.

Les frontières définissaient le terrain.

L’historique choisissait ensuite les routes.

Il sourit.

— Là, ça devient vraiment une carte.

Astra répondit :

— Oui.

Pas seulement un graphe.

Un territoire avec des zones praticables.

Des limites.

Des routes.

Des coûts.

Une mémoire.

Brutus commençait à posséder les éléments d’un navigateur.

Mais encore une fois :

proposition.

Pas autorité absolue.

Les frontières pouvaient elles-mêmes être fausses ou obsolètes.

Il fallait donc permettre leur révision.

Gabriel écrivit :

**AUCUNE FRONTIÈRE N’EST SACRÉE SI ELLE EST EMPIRIQUE.**

Astra approuva.

Une frontière mathématiquement démontrée était différente.

Mais une frontière observée en benchmark devait rester ouverte au retest.

Ils ajoutèrent :

**type = théorique / empirique / opérationnel / politique**

Très utile.

Une frontière de sécurité pouvait être imposée même sans échec historique.

Une frontière théorique pouvait venir d’une preuve.

Une frontière empirique d’un test.

Une frontière opérationnelle d’une capacité machine.

Les confondre serait dangereux.

Gabriel regarda.

— La raison de la frontière doit être affichée.

— Oui.

Pourquoi cette route est-elle bloquée?

**THÉORÈME**

ou

**BENCHMARK**

ou

**RISQUE**

ou

**POLITIQUE**

Très différent.

Ils décidèrent que chaque garde produirait une explication.

Pas simplement :

**DENIED**

Mais :

**Route A non recommandée : entrée hors de la zone stable observée pour module v3; voir frontière F-017.**

Gabriel sourit.

— Ça, c’est une machine qui se justifie.

Astra répondit :

— Au moins sur cette décision.

Voilà.

L’explicabilité revenait.

Pas besoin d’expliquer l’univers.

Seulement pouvoir retracer pourquoi une route avait été écartée.

La mémoire ne devenait pas une boîte noire.

Elle devenait une carte annotée.

Puis Gabriel regarda le registre des erreurs.

Il avait longtemps trouvé ces fichiers déprimants.

Des choses cassées.

Des tentatives ratées.

Du travail perdu.

Maintenant, il voyait autre chose.

Chaque erreur bien étudiée pouvait devenir une ligne de côte.

Un bord de montagne.

Une rivière.

Une zone fragile.

Pas toujours.

Mais parfois.

Et ces frontières permettaient à la prochaine Fourmi de se déplacer plus intelligemment.

Gabriel murmura :

— Une erreur comprise devient du terrain.

Astra répondit :

— Oui.

Il écrivit la phrase.

Parce qu’elle résumait le chapitre.

Pas une erreur cachée.

Pas une erreur oubliée.

Une erreur comprise.

Documentée.

Testée.

Bornée.

Alors elle cessait d’être uniquement un événement négatif.

Elle devenait une information sur la forme du problème.

Et plus Brutus accumulait ce type de connaissance, moins sa carte ressemblait à un dessin abstrait.

Elle commençait à avoir du relief.

Des endroits sûrs.

Des zones fragiles.

Des routes efficaces.

Des routes coûteuses.

Des limites.

Des passages.

Et lorsqu’une Fourmi s’approchait d’un endroit où d’autres étaient tombées,

la mémoire ne criait plus simplement :

**danger.**

Elle pouvait dire :

**voici exactement où elles sont tombées, dans quelles conditions, et quel chemin avait permis à l’une d’elles de passer.**

**Fin du chapitre 153.**