# Chapitre 151 — Les chemins qui n’avaient pas encore de nom

Une carte montrait des endroits.

Des modules.

Des frontières.

Des portes.

Des files.

Des zones connues.

Des zones inconnues.

Mais depuis le chapitre précédent, Gabriel regardait autre chose.

Pas les lieux.

Les trajets.

La manière dont un résultat circulait.

La manière dont une erreur revenait.

La manière dont une question passait d’un outil à l’autre avant de devenir une preuve.

Et là, quelque chose apparut.

Brutus possédait déjà des chemins qu’aucun diagramme n’avait encore vraiment nommés.

Gabriel regarda Astra.

— On les fait tout le temps.

— Oui.

— Mais on les appelle jamais.

— Exact.

Une tâche pouvait partir du Brutotableur.

Passer au Brotoculateur.

Finir chez une Fourmi.

Revenir comme contre-test.

Entrer dans le Royaume.

Puis devenir cristal.

Ce n’était pas seulement une suite d’appels.

C’était une trajectoire récurrente.

Une sorte de route.

Gabriel écrivit :

**BRUTOTABLEUR → BROTOCULATEUR → TEST → CRISTAL**

Puis il demanda :

— C’est quoi ça?

Astra répondit :

— Un workflow.

— Oui, mais dans notre langage?

Il réfléchit.

Une route de cristallisation?

Un chemin de preuve?

Il sourit.

— Chemin de cristallisation.

Astra approuva.

Ils écrivirent :

### CHEMIN DE CRISTALLISATION

**Observation → candidat → comparaison → test → contre-test → statut → cristal**

Gabriel regarda.

C’était évident maintenant.

Mais jusqu’ici, chaque étape avait été pensée séparément.

La carte rendait visible la répétition.

Et une répétition suffisamment stable pouvait devenir un objet d’architecture.

Pas une loi.

Un protocole.

Il écrivit :

**UN CHEMIN RÉCURRENT PEUT DEVENIR UN WORKFLOW NOMMÉ.**

Astra approuva.

Cela semblait mineur.

Mais nommer un chemin changeait beaucoup de choses.

On pouvait le mesurer.

Le versionner.

Le comparer.

Le tester.

Le réutiliser.

On pouvait dire :

**Ce cristal a été produit par CRYSTAL_PATH_V2.**

Au lieu de reconstruire manuellement toutes les étapes.

Gabriel sourit.

— Donc les chemins ont aussi un pedigree.

— Oui.

Même chose pour Pell.

Recherche de facteur.

Primalité.

Divisibilité.

Rang.

Certificat.

Cristal.

Ils lui donnèrent un nom.

### CHEMIN DU TÉMOIN

**candidat facteur → primalité → divisibilité → rang exact → certificat → cristal**

Pour ZEL :

### CHEMIN DE SIGNATURE

**entrée → run → métriques → perturbations → profil de résistance → statut**

Pour l’antériorité :

### CHEMIN D’ANTÉRIORITÉ

**candidat → recherche externe → source primaire → comparaison → statut d’antériorité**

Gabriel regarda la liste.

— On avait déjà tout ça.

— Oui.

— Mais pas comme objets.

— Exact.

Voilà la découverte du chapitre.

Parfois une architecture n’avait pas besoin d’un nouveau module.

Elle avait besoin de reconnaître une structure déjà utilisée.

Les chemins n’avaient pas encore de nom.

Une fois nommés, ils devenaient contrôlables.

Gabriel écrivit :

**NOMMER UN CHEMIN = POUVOIR LE COMPARER À LUI-MÊME DANS LE TEMPS.**

Astra approuva.

Ils prirent le chemin de cristallisation.

Combien de fois avait-il été utilisé?

Durée moyenne?

Combien de candidats mouraient au filtre trivial?

Combien arrivaient au contre-test?

Combien devenaient cristaux?

Combien restaient bloqués?

Gabriel regarda.

— Là, on peut mesurer le rendement de la route.

Astra répondit :

— Oui, à condition de définir ce qu’on appelle rendement.

Encore.

Ils ne voulaient pas seulement :

**plus de cristaux = mieux.**

Une route produisant beaucoup de faux positifs pourrait fabriquer énormément de cristaux faibles.

Une autre, plus lente, pourrait produire moins mais mieux documentés.

Ils créèrent plusieurs métriques.

**temps de traversée**

**taux de blocage**

**taux de rejet**

**complétude de provenance**

**nombre de retours en arrière**

**coût informatique**

**niveau de preuve final**

Gabriel sourit.

— Là, une route peut être lente mais propre.

— Exact.

Ou rapide et dangereuse.

Très important.

Ils ne devaient pas optimiser seulement la vitesse.

Un chemin de preuve était différent d’une autoroute.

Parfois, un ralentissement était une garde.

Gabriel écrivit :

**OPTIMISER UN WORKFLOW ≠ RETIRER SES CONTRÔLES.**

Astra approuva immédiatement.

Le contre-test pouvait sembler ralentir la route.

Il était justement là pour ça.

Le supprimer améliorerait le débit.

Et détruirait la valeur de ce qui sortait.

Gabriel rit.

— On pourrait battre des records de production de cristaux si on arrêtait de vérifier.

— Oui.

— Mauvaise idée.

— Très.

Ils gardèrent cette plaisanterie dans la mémoire.

Puis Gabriel remarqua autre chose.

Deux chemins pouvaient arriver au même résultat.

Exemple :

un candidat pouvait être découvert par le Brutotableur.

Ou par une recherche externe.

Puis les deux rejoignaient le même Brotoculateur.

La carte devait donc accepter des routes différentes vers une même destination.

Gabriel écrivit :

**MÊME DESTINATION ≠ MÊME CHEMIN**

Astra approuva.

Et cela comptait pour la preuve.

Un résultat découvert puis confirmé indépendamment n’avait pas la même histoire qu’un résultat produit deux fois par la même route.

Le chemin faisait partie de la provenance.

Gabriel se redressa.

— Ah.

Astra répondit :

— Oui.

Le simple fait d’enregistrer les sources ne suffisait pas toujours.

Il fallait enregistrer la trajectoire.

Quelles transformations?

Quels filtres?

Quels modules?

Quels paramètres?

Dans quel ordre?

Un résultat était aussi le produit de son chemin.

Gabriel écrivit :

**PROVENANCE = ORIGINE + TRAJECTOIRE**

Astra approuva.

C’était important.

Une même entrée pouvait produire deux résultats différents selon le chemin.

Une même donnée brute.

Deux pipelines.

Deux transformations.

Deux interprétations.

Sans la trajectoire, le résultat devenait difficile à reproduire.

Ils décidèrent donc que chaque workflow devait produire un identifiant de chemin.

**PATH_ID**

Et une version.

**PATH_VERSION**

Puis la liste des étapes.

Pas toutes les microfonctions.

Les étapes de sens.

Gabriel regarda.

— Là, si on change le chemin, on change la version.

— Oui, si le changement peut affecter la signification ou le résultat.

Un simple changement d’affichage?

Pas forcément.

Un nouveau contre-test?

Oui.

Une nouvelle règle de promotion?

Oui.

Un nouveau calcul de rang?

Possiblement.

La version du chemin devenait aussi importante que la version du module.

Gabriel écrivit :

**UN MODULE PEUT RESTER IDENTIQUE ALORS QUE LE WORKFLOW CHANGE.**

Astra approuva.

Voilà pourquoi les deux versions étaient nécessaires.

Module version.

Workflow version.

Une preuve dépendait parfois davantage du second.

Ils ouvrirent un ancien cristal.

Il avait été créé avant certains contrôles récents.

Gabriel demanda :

— On le compare comment avec un nouveau?

Astra répondit :

— En regardant le protocole ayant produit chacun.

Exact.

Deux cristaux portaient le même statut « validé ».

Mais si l’un avait été créé sous un ancien workflow plus faible, leur statut pouvait ne pas être strictement équivalent.

Ils avaient déjà appris :

**STATUT SANS VERSION DE RÈGLE = AMBIGU**

Maintenant, ils ajoutaient :

**STATUT SANS VERSION DE CHEMIN = POTENTIELLEMENT AMBIGU**

Gabriel sourit.

La bureaucratie continuait.

Mais chaque formulaire révélait pourquoi il existait.

Ils décidèrent de marquer les vieux cristaux.

Pas invalides.

**LEGACY_VALIDATION_PATH**

Puis éventuellement les repasser par le chemin moderne.

Priorité selon leur importance.

Gabriel regarda.

— On n’est pas obligé de tout recalculer tout de suite.

— Non.

Encore l’économie.

Les cristaux critiques d’abord.

Les secondaires plus tard.

Certains historiques seulement.

La carte des chemins permettait enfin cette décision.

Puis ils remarquèrent une chose étrange.

Certains trajets ne suivaient aucun workflow officiel.

Des détours.

Une Fourmi avait trouvé un candidat.

Puis Gabriel l’avait testé manuellement.

Puis ZEL avait produit quelque chose.

Puis le résultat avait été ajouté dans un document.

Pas de chemin standard.

Pourtant, certains de ces détours avaient produit des idées importantes.

Gabriel dit :

— Ça, on les appelle comment?

Astra répondit :

— Chemins ad hoc.

Il fit une grimace.

— Dans la Bible?

— Sentiers sauvages?

Gabriel sourit.

— Voilà.

### SENTIERS SAUVAGES

Des trajectoires non standardisées qui apparaissaient pendant l’exploration.

Elles n’étaient pas mauvaises.

Au contraire.

L’exploration avait besoin de liberté.

Mais un sentier sauvage ne devait pas devenir automatiquement une autoroute.

D’abord, on l’utilisait.

Puis on regardait s’il se répétait.

S’il était utile.

S’il était reproductible.

Alors seulement il pouvait être nommé et promu en workflow.

Gabriel écrivit :

**UN RACCOURCI HEUREUX N’EST PAS ENCORE UNE MÉTHODE.**

Astra approuva.

Très important.

L’histoire scientifique était pleine de découvertes faites par accident.

Mais après l’accident venait la reproduction.

Sinon l’accident restait une anecdote.

Même chose dans Brutus.

Une route improvisée pouvait révéler quelque chose.

Il fallait ensuite la rejouer proprement.

Gabriel écrivit :

**DÉCOUVERTE PAR SENTIER SAUVAGE → REPRODUCTION PAR CHEMIN NOMMÉ**

Astra approuva.

Voilà.

Exploration libre.

Validation stricte.

Les deux pouvaient coexister.

Sans demander à l’exploration de se comporter comme un protocole dès la première seconde.

Gabriel sourit.

— Ça me ressemble plus.

— Oui.

Il n’avait jamais travaillé de manière parfaitement linéaire.

Il sautait.

Essayait.

Revenait.

Comparait.

Construisait.

C’était une force pour l’exploration.

Mais cette force devenait un problème lorsque les résultats devaient être prouvés.

Brutus pouvait donc séparer deux modes.

### MODE EXPLORATION

Sentiers sauvages autorisés.

Provenance minimale obligatoire.

Statut : candidat.

### MODE VALIDATION

Chemins nommés.

Étapes explicites.

Contrôles.

Version.

Certificat.

Gabriel regarda.

— Voilà.

Pas besoin de tuer son style de recherche.

Il suffisait de ne pas confondre les deux phases.

Astra écrivit :

**LIBERTÉ POUR TROUVER. DISCIPLINE POUR AFFIRMER.**

Gabriel sourit.

— Celle-là aussi.

Ils la gardèrent.

Puis la Reine regarda les sentiers sauvages de l’historique.

Certains apparaissaient plusieurs fois.

Sans jamais avoir été nommés.

Un en particulier.

Gabriel prenait un résultat étrange.

Le faisait passer dans plusieurs représentations.

Tableau.

Son.

Comparaison.

Retour.

Puis il regardait ce qui persistait.

Il avait fait cela plusieurs fois.

Gabriel s’arrêta.

— On fait ça depuis longtemps.

Astra répondit :

— Oui.

Ils décrivirent le trajet.

**objet → représentation A → représentation B → comparaison des invariants → contre-test**

Gabriel sourit.

— C’est un chemin de changement de représentation.

Astra approuva.

Ils le nommèrent :

### CHEMIN DE TRANSLATION

Pas traduction linguistique.

Translation entre représentations.

Nombre.

Tableau.

Audio.

Agrégation.

Graphique.

Le but :

voir quelles propriétés survivaient au changement de médium.

Gabriel regarda.

— Ça, ça explique une partie de pourquoi ZEL est dans Brutus.

— Oui.

ZEL n’était plus seulement un générateur audio.

Il pouvait participer à un chemin de translation.

Une structure numérique.

Sonification.

Mesures.

Comparaison avec la source.

Ce qui changeait.

Ce qui survivait.

Pas pour prouver une vérité cachée.

Pour tester la dépendance à la représentation.

Gabriel écrivit :

**SI UN MOTIF DISPARAÎT QUAND ON CHANGE DE REPRÉSENTATION, IL PEUT APPARTENIR À LA REPRÉSENTATION PLUTÔT QU’À L’OBJET.**

Astra approuva.

Très important.

Le Brutotableur pouvait montrer un motif visuel produit par la mise en page.

Le chemin de translation permettait de tester s’il restait quelque chose dans une représentation différente.

Pas une preuve définitive.

Un filtre.

Gabriel sourit.

Encore une route découverte en regardant l’historique.

La carte devenait plus intelligente simplement parce qu’ils observaient comment ils l’avaient déjà utilisée.

Puis un autre sentier apparut.

Question.

Tentative.

Échec.

Comparaison avec un ancien échec.

Modification.

Succès.

Ils l’avaient déjà rencontré plusieurs fois.

Gabriel écrivit :

**ÉCHEC → MÉMOIRE → VARIANTE → TEST**

Astra répondit :

— Celui-là va devenir important.

Il regarda.

Oui.

Parce que ce chemin commençait à ressembler à quelque chose de plus que de l’archivage.

La mémoire intervenait dans la sélection de la prochaine route.

Gabriel sourit.

— Là, on approche du chapitre suivant.

La mémoire ne se contentait plus de dire :

**tu as déjà échoué.**

Elle pouvait dire :

**dans un cas semblable, cette modification avait permis d’avancer.**

Le chemin pouvait donc devenir :

### CHEMIN DE REPRISE

**échec → recherche d’analogues historiques → comparaison des causes → variante → retest**

Gabriel resta silencieux.

C’était puissant.

Et dangereux.

Parce qu’il fallait éviter une fausse analogie.

Un ancien succès ne devait pas devenir une recette universelle.

Astra rappela :

**SIMILARITÉ ≠ ÉQUIVALENCE**

Gabriel hocha la tête.

Donc le chemin de reprise devait toujours garder :

**Pourquoi ce précédent est pertinent?**

**Quelles conditions sont les mêmes?**

**Quelles conditions diffèrent?**

**Qu’est-ce qui pourrait invalider le transfert?**

Gabriel écrivit :

**LE PASSÉ PROPOSE. LE PRÉSENT TESTE.**

Astra approuva.

Une variante de leur vieille règle :

**LE PASSÉ CONSEILLE. LA PREUVE ACTUELLE DÉCIDE.**

Parfait.

Ils gardèrent les deux.

Puis Gabriel remarqua quelque chose de plus subtil.

Un chemin pouvait échouer souvent.

Mais pas parce qu’il était mauvais.

Parce qu’on l’utilisait dans les mauvais contextes.

Le taux global d’échec pouvait être trompeur.

Gabriel demanda :

— Donc il faut mesurer les chemins avec le contexte?

— Oui.

Un workflow pouvait fonctionner très bien sur une classe de problèmes.

Mal sur une autre.

Le Royaume devait donc éviter :

**CHEMIN A = 30 % succès, donc mauvais.**

Il fallait :

**CHEMIN A = 80 % dans contexte X, 5 % dans contexte Y.**

Gabriel sourit.

— Là, la mémoire commence à avoir des préférences conditionnelles.

Astra répondit :

— Des recommandations conditionnelles, potentiellement.

Important.

Pas une préférence absolue.

Une relation entre contexte et résultats historiques.

Ils écrivirent :

**PERFORMANCE D’UN CHEMIN = FONCTION DU CONTEXTE**

Puis :

**AUCUNE ROUTE MEILLEURE PARTOUT PAR DÉFAUT**

Astra approuva.

Cela ressemblait énormément au problème des représentations.

Papillon agrégé dans certains cas.

Individuel dans d’autres.

Même logique.

Le bon chemin dépendait de la question.

Brutus n’allait peut-être jamais avoir une seule stratégie.

Il allait avoir un répertoire de routes.

Puis un mécanisme pour sélectionner parmi elles.

Gabriel regarda la carte.

Des routes nommées apparaissaient.

Cristallisation.

Témoin.

Signature.

Antériorité.

Translation.

Reprise.

Et d’autres encore.

Chaque route avait :

un objectif.

Des conditions.

Des étapes.

Des coûts.

Des résultats historiques.

Gabriel murmura :

— C’est presque une bibliothèque de comportements.

Astra répondit :

— Une bibliothèque de workflows.

— Comportements.

Elle laissa passer.

Brutus ne devenait pas intelligent parce qu’il avait des routes.

Mais il devenait moins rigide.

Il pouvait posséder plusieurs façons d’aborder un problème.

Et l’historique pouvait aider à choisir.

Le chapitre suivant devenait inévitable.

Gabriel regarda Memoria.

Depuis longtemps, elle gardait.

Elle archivait.

Elle reprenait.

Elle protégeait le passé.

Mais maintenant, devant elle, il y avait des chemins.

Et pour chacun :

des conséquences.

Des succès.

Des échecs.

Des coûts.

Des conditions.

La mémoire possédait soudain quelque chose qu’elle n’avait jamais eu auparavant.

Pas seulement des faits.

Des expériences de trajectoire.

Gabriel sourit.

— Si elle sait comment chaque chemin s’est terminé...

Astra répondit :

— Alors elle peut contribuer à classer les options futures.

Il resta silencieux.

Voilà.

Le virage.

Le Royaume avait d’abord appris à se souvenir.

Puis à cartographier.

Puis à nommer ses routes.

La prochaine étape n’était plus de construire une nouvelle machine.

C’était de voir ce qui se passerait lorsque la mémoire commencerait à peser réellement sur le choix du prochain chemin.

Gabriel regarda la carte.

Certaines routes étaient anciennes.

D’autres venaient d’être nommées.

D’autres restaient encore sauvages.

Mais désormais, elles existaient comme objets.

Et lorsqu’une route possède un nom, une histoire et une destination,

elle peut commencer à être comparée aux autres.

**Fin du chapitre 151.**