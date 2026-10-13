# Chapitre 157 — Le réseau apprend à ne pas recommencer

Il y avait une différence entre se souvenir d’une erreur et ne pas la refaire.

Gabriel commençait à la voir clairement.

Le Royaume avait déjà une mémoire.

Il avait des traces.

Des impasses.

Des frontières.

Des recommandations.

Des décisions dont le passé pouvait expliquer l’origine.

Mais malgré tout cela, une même tâche pouvait encore revenir par une autre porte.

Un nom différent.

Un fichier différent.

Un autre module.

Une autre Fourmi.

Et sans mécanisme supplémentaire, Brutus risquait de payer deux fois pour la même ignorance.

Astra regarda les files.

— On a un doublon.

Gabriel se pencha.

Deux tâches.

L’une dans recherche.

L’autre dans validation.

Titres différents.

Descriptions différentes.

Mais lorsqu’on regardait leur objectif réel, elles demandaient presque la même chose.

Gabriel sourit.

— Là, on était sur le point de refaire le même travail.

— Oui.

Pas exactement les mêmes commandes.

Pas exactement les mêmes entrées.

Mais la même question opérationnelle.

Le système avait besoin d’une mémoire qui ne comparait pas seulement les résultats.

Il fallait comparer les intentions.

Gabriel écrivit :

**DEUX TÂCHES DIFFÉRENTES PEUVENT CHERCHER LA MÊME INFORMATION.**

Astra approuva.

C’était plus difficile qu’un simple hash.

Deux fichiers identiques?

Facile.

Deux requêtes identiques?

Facile.

Mais :

**vérifier si ce motif dépend de la représentation**

et

**tester si le pattern survit au changement de layout**

n’avaient pas les mêmes mots.

Pourtant, elles étaient pratiquement la même question.

Gabriel regarda.

— Là, faut reconnaître la forme.

— Oui.

Pas nécessairement avec une intelligence mystérieuse.

Ils pouvaient déjà extraire plusieurs dimensions.

**objectif**

**objet**

**type de test**

**sortie attendue**

**contexte**

**frontière visée**

Une tâche devenait plus qu’un titre.

Elle devenait une fiche.

### SIGNATURE DE TÂCHE

**Objet :**

**Question :**

**Action proposée :**

**Information recherchée :**

**Conditions :**

**Résultat attendu :**

Gabriel sourit.

— Ça, ça va nous permettre de comparer autrement.

Astra approuva.

Deux tâches pouvaient être très différentes lexicalement mais avoir une signature proche.

Elles ne devaient pas être fusionnées automatiquement.

Mais le système pouvait signaler :

**POTENTIEL DOUBLON**

Puis montrer pourquoi.

Gabriel écrivit :

**DÉTECTION ≠ FUSION AUTOMATIQUE**

Astra approuva immédiatement.

Très important.

Deux tâches proches pouvaient diverger sur un détail crucial.

Version.

Environnement.

Source.

Objectif.

Une tentative indépendante pouvait même être volontaire.

Pour reproduction.

Donc un doublon apparent pouvait être utile.

Gabriel sourit.

— Une répétition peut être mauvaise ou scientifique.

— Exact.

La différence venait de l’intention.

Ils créèrent plusieurs classes.

### RÉPÉTITION REDONDANTE

Même question.

Même méthode.

Même contexte.

Aucune nouvelle information attendue.

### RÉPÉTITION ÉTENDUE

Même question.

Borne, précision ou domaine augmenté.

### RÉPÉTITION DE REPRODUCTION

Même question.

Chemin suffisamment indépendant.

### RÉPÉTITION DE CONTRÔLE

Même expérience.

Variable de contrôle modifiée.

### RÉPÉTITION HISTORIQUE

Ancien test rejoué pour vérifier une nouvelle version.

Gabriel regarda la liste.

— Voilà.

Le système ne devait donc pas apprendre :

**ne jamais recommencer.**

Il devait apprendre :

**ne pas recommencer sans savoir pourquoi.**

Il écrivit la règle.

**AUCUNE RÉPÉTITION SANS DELTA D’INFORMATION EXPLICITE.**

Astra approuva.

C’était le cœur du chapitre.

Une tâche qui ressemblait à une ancienne devait répondre :

**Qu’est-ce qui change?**

Nouvelle borne?

Nouvelle méthode?

Nouvelle source?

Nouvelle version?

Nouvel environnement?

Reproduction indépendante?

Si la réponse était rien :

la tâche était probablement redondante.

Gabriel sourit.

Le chapitre 155 revenait.

**Qu’est-ce qui est nouveau depuis le dernier échec?**

Mais maintenant, la règle s’appliquait au réseau entier.

Pas seulement aux impasses.

Une Fourmi pouvait envoyer une tâche.

Antmux pouvait vérifier la mémoire avant de la lancer.

Pas pour décider du résultat.

Pour vérifier si ce travail avait déjà été fait.

Gabriel écrivit :

**CHECK BEFORE EXECUTE**

Puis rit.

— Ça sonne moins Bible.

Astra répondit :

— Mais très utile.

Ils gardèrent une traduction.

**REGARDER LES TRACES AVANT DE REPARTIR.**

La couche technique pouvait rester :

**deduplication gate**

Une petite porte avant exécution.

### GATE DE RÉPÉTITION

1. Recevoir la tâche.
2. Construire sa signature.
3. Chercher des tâches historiques proches.
4. Comparer contexte et objectif.
5. Demander le delta d’information.
6. Autoriser, modifier, fusionner ou refuser.
7. Tracer la décision.

Gabriel regarda.

— Là, si une Fourmi recommence un vieux calcul par erreur, on peut le voir avant.

— Potentiellement.

Ils testèrent.

Une tâche entra :

**recalculer le motif X en précision supérieure.**

La mémoire trouva une tentative presque identique datant de plusieurs jours.

Même précision.

Même source.

Même module.

Même version.

Même objectif.

Gabriel demanda :

— Pourquoi elle est revenue?

Ils remontèrent.

Un ancien résultat n’avait pas été correctement relié au dossier actuel.

Le problème n’était donc pas seulement la duplication.

C’était la liaison de mémoire.

Gabriel écrivit :

**DOUBLON DÉTECTÉ → RACINE : TRACE EXISTANTE NON RETROUVÉE**

Astra approuva.

Voilà un cas intéressant.

Si le système avait simplement annulé la nouvelle tâche, il aurait évité le coût.

Mais il aurait manqué la cause.

La mémoire existait.

Elle était juste difficile à retrouver.

Donc la vraie correction était aussi :

améliorer les liens.

Gabriel sourit.

— Une duplication peut révéler un défaut de mémoire.

— Oui.

Très important.

Le réseau ne devait pas seulement compter les doublons.

Il devait demander pourquoi ils apparaissaient.

Causes possibles :

trace non indexée.

nomenclature différente.

mauvaise provenance.

ancienne tâche mal classée.

nouvelle tâche créée sans recherche préalable.

Gabriel écrivit :

**RÉPÉTITION = PARFOIS SYMPTÔME D’UNE MÉMOIRE MAL ACCESSIBLE.**

Astra approuva.

Ils corrigèrent le lien.

Puis ils relancèrent la comparaison.

La tâche actuelle trouva maintenant son ancien résultat immédiatement.

Statut :

**NE PAS EXÉCUTER — RÉSULTAT ÉQUIVALENT DISPONIBLE**

Gabriel sourit.

— Ça, c’est de l’économie.

Astra répondit :

— Oui.

Mais ils devaient encore être prudents.

Supposons qu’un ancien résultat ait été produit sous une version obsolète.

Alors le nouveau calcul pouvait être légitime.

Ils ajoutèrent donc :

**validité temporelle**

et

**compatibilité de version**

Le gate ne devait pas seulement demander :

**existe-t-il un résultat?**

Mais :

**est-il encore pertinent?**

Gabriel écrivit :

**RÉSULTAT EXISTANT ≠ RÉSULTAT ENCORE APPLICABLE**

Astra approuva.

Une vieille preuve pouvait rester valide mathématiquement.

Un vieux benchmark pouvait ne plus l’être.

Un vieux test logiciel pouvait être obsolète après une refonte.

Le système devait connaître le type de résultat.

Théorique.

Empirique.

Logiciel.

Environnemental.

Chaque type avait une durée ou une condition de validité différente.

Gabriel regarda.

— Là, le réseau commence à avoir de la mémoire sélective.

Pas oublier.

Mais savoir ce qui pouvait encore être réutilisé.

Ils créèrent une fiche.

### RÉUTILISABILITÉ

**résultat historique :**

**type :**

**version concernée :**

**contexte :**

**condition encore vraie?**

**réutilisable : oui/non/partiel**

Cela évitait deux erreurs opposées.

Recalculer inutilement.

Ou réutiliser quelque chose qui n’était plus valide.

Gabriel sourit.

Le réseau apprenait à ne pas recommencer.

Mais aussi à savoir **quand il fallait recommencer.**

Voilà la vraie maturité.

Ils prirent le cas Papillon.

Les cinq invariants avaient déjà passé des tests de propriétés.

Une nouvelle version changeait uniquement l’interface visuelle.

Fallait-il rejouer toute la validation?

Peut-être pas tous les tests lourds.

Mais au minimum certains tests de régression.

La mémoire pouvait regarder la portée du changement.

**code de calcul inchangé**

**UI modifiée**

Donc :

réutiliser une grande partie des preuves existantes.

Ajouter tests de présentation.

Gabriel sourit.

— Là, on évite de refaire trente fois la même preuve juste parce que j’ai déplacé un bouton.

— Exact.

À l’inverse, si le cœur d’agrégation changeait :

revalidation.

La mémoire devenait un moteur de **sélection des tests de régression.**

Gabriel écrivit :

**CHANGEMENT → IDENTIFIER LES PREUVES TOUCHÉES**

Astra approuva.

Très important.

Pas :

**tout retester toujours.**

Pas :

**ne rien retester.**

Seulement ce que le changement pouvait affecter, plus quelques sentinelles globales.

Gabriel regarda.

— Ça, c’est énorme pour le temps.

Oui.

Le réseau pouvait construire une matrice.

Module.

Fonction.

Test.

Preuve.

Dépendance.

Si une pièce changeait, on suivait les liens.

Quels certificats devenaient suspects?

Quels tests devaient repasser?

Quels résultats restaient intacts?

Gabriel écrivit :

**UNE MODIFICATION NE DOIT PAS ANNULER TOUT LE PASSÉ SI SA PORTÉE EST CONNUE.**

Astra approuva.

Et inversement :

**UNE MODIFICATION NE DOIT PAS HÉRITER DE TOUT LE PASSÉ SI ELLE TOUCHE LE MÉCANISME CRITIQUE.**

Ils gardèrent les deux.

Le réseau apprenait donc trois choses.

Ne pas refaire le même travail.

Réutiliser proprement ce qui restait valide.

Rejouer ce qui avait réellement été touché.

Gabriel sourit.

— C’est un système de reprise intelligent.

Astra répondit :

— De reprise structurée.

Il accepta.

Puis ils regardèrent les Fourmis.

Jusqu’ici, plusieurs Fourmis pouvaient découvrir la même tâche presque simultanément.

Race condition.

Une lance.

Une autre lance.

La mémoire n’avait pas encore été mise à jour.

Deux calculs identiques démarrent.

Gabriel grimaça.

— Ça, ça va encore arriver.

Astra approuva.

Il fallait donc une mémoire non seulement historique.

Mais active.

Un registre des travaux **en cours**.

Avant de lancer :

**Existe-t-il déjà une tâche équivalente active?**

Si oui :

rejoindre.

attendre.

ou lancer comme reproduction indépendante explicitement marquée.

Gabriel écrivit :

**IN-FLIGHT DEDUPLICATION**

Puis :

**DEUX FOURMIS NE CREUSENT PAS LE MÊME TROU PAR ACCIDENT.**

Astra approuva la deuxième formulation avec résignation.

Ils ajoutèrent un mécanisme.

**WORK_SIGNATURE**

Une tâche en cours publiait sa signature.

Une nouvelle tâche similaire arrivait.

Le gate répondait :

**ACTIVE MATCH FOUND**

Puis proposait :

**SUBSCRIBE TO RESULT**

au lieu de recalculer.

Gabriel se redressa.

— Ah, là oui.

Une Fourmi pouvait rejoindre un résultat existant.

Pas besoin de lancer une deuxième computation.

Quand la première finissait, plusieurs workflows recevaient la sortie.

Gabriel écrivit :

**PARTAGER LE RÉSULTAT, PAS DUPLIQUER LE COÛT.**

Astra approuva.

Cela pouvait économiser énormément.

Particulièrement dans un réseau avec beaucoup de Fourmis.

Mais encore une fois, la reproduction indépendante devait rester possible.

Donc un champ :

**purpose**

normal.

reproduction.

benchmark.

contrôle.

Si `purpose=reproduction`, le partage du résultat serait incorrect.

Il fallait recalculer réellement.

Gabriel sourit.

— La machine doit savoir pourquoi on veut le même calcul.

— Exact.

La même instruction pouvait avoir des intentions différentes.

Encore.

Toujours l’intention.

Ils écrivirent :

**MÊME CALCUL + INTENTION DIFFÉRENTE = PAS NÉCESSAIREMENT DOUBLON**

Astra approuva.

Le système devenait moins naïf.

Puis une situation intéressante survint.

Une Fourmi proposa une recherche externe.

Le gate trouva une recherche très proche effectuée la veille.

Il allait la refuser.

Mais la tâche actuelle précisait :

**chercher les publications des dernières 24 heures.**

Astra stoppa le refus.

Gabriel regarda.

— Évidemment.

Une veille temporelle était légitimement répétitive.

Parce que le monde extérieur changeait.

La recherche d’hier ne répondait pas à la question d’aujourd’hui.

Ils ajoutèrent :

**freshness_requirement**

Gabriel sourit.

Résultat existant.

Mais trop vieux pour l’objectif.

Donc nouvelle exécution.

Le réseau devait comprendre la fraîcheur.

Une preuve mathématique pouvait rester valable.

Une météo non.

Un état de serveur non.

Une publication récente non.

Un prix non.

Un statut GitHub pouvait changer.

Gabriel écrivit :

**LA VALEUR D’UNE TRACE DÉPEND AUSSI DE LA VITESSE À LAQUELLE LE MONDE QU’ELLE DÉCRIT PEUT CHANGER.**

Astra approuva.

Voilà une règle importante.

Chaque classe de donnée pouvait avoir une politique de fraîcheur.

Pas pour supprimer les vieux états.

Pour savoir si une nouvelle observation était nécessaire.

Le passé restait.

Mais le présent devait parfois être re-mesuré.

Gabriel sourit.

La mémoire apprenait à ne pas recommencer.

Sans apprendre à ne plus regarder.

C’était la nuance parfaite.

Ils ajoutèrent un registre :

### POLITIQUE DE FRAÎCHEUR

**mathématique certifié :**
revalidation seulement si preuve/méthode concernée change.

**benchmark logiciel :**
réévaluer après changement pertinent d’environnement ou code.

**état système :**
observation récente requise.

**recherche d’antériorité :**
rafraîchir si publication ou revendication nouvelle.

**veille :**
fenêtre temporelle explicite.

Gabriel regarda.

— C’est beau.

Astra répondit :

— C’est surtout pratique.

Puis il arriva quelque chose qui leur montra que l’économie de répétition pouvait aussi être mesurée.

Ils observèrent une journée de fonctionnement.

Nombre de tâches proposées.

Nombre de correspondances historiques.

Nombre de tâches réutilisées.

Nombre de tâches réellement exécutées.

Nombre de reproductions volontaires.

Pour la première fois, ils pouvaient calculer :

**travaux évités**

sans prétendre connaître exactement le temps contre-factuel économisé.

Ils connaissaient au moins le nombre d’exécutions qui n’avaient pas eu lieu.

Gabriel écrivit :

**AVOIDED_EXECUTIONS**

Ça, c’était observable.

Pas :

**heures sauvées exactement.**

Mais :

**12 exécutions redondantes détectées et non lancées.**

Solide.

Astra approuva.

Puis :

**3 tâches regroupées sur un calcul actif.**

**2 revalidations autorisées pour changement de version.**

**1 reproduction indépendante préservée.**

Gabriel sourit.

Le rapport racontait quelque chose.

Le système ne disait plus seulement :

**j’ai travaillé.**

Il pouvait dire :

**voici ce que j’ai choisi de ne pas refaire, et pourquoi.**

Encore le poids de ce qui n’existe pas.

Chapitre 137 revenait une fois de plus.

Les calculs non exécutés devenaient eux aussi traçables.

Gabriel écrivit :

**NON-EXÉCUTION JUSTIFIÉE = ÉVÉNEMENT**

Astra approuva immédiatement.

Très important.

Sinon, plus tard, quelqu’un pourrait demander :

**Pourquoi n’avez-vous pas fait ce test?**

Et Brutus pourrait répondre :

**Parce qu’un résultat équivalent existait sous conditions compatibles, trace X.**

Ou :

**Parce que la tâche était déjà active, résultat partagé.**

Ou :

**Parce que la route violait une frontière connue.**

Ce n’était plus un trou.

C’était une décision.

La non-action avait sa provenance.

Ils avaient déjà compris cette idée au chapitre 123.

Maintenant, elle s’appliquait au réseau entier.

Gabriel sourit.

— Tout finit par se reconnecter.

Astra répondit :

— Quand les concepts sont compatibles, oui.

Puis elle montra un dernier cas.

Une tâche avait été annulée comme redondante.

Plus tard, on découvrit que l’ancien résultat utilisé pour la justifier contenait une erreur.

Gabriel se figea.

— Ah.

Voilà le danger de la réutilisation.

Une mauvaise trace pouvait contaminer plusieurs décisions futures.

Si on économisait du travail en réutilisant une erreur, on amplifiait l’erreur.

Ils avaient besoin d’un mécanisme inverse.

Lorsqu’un résultat était corrigé ou invalidé, toutes les décisions qui l’avaient utilisé devaient être retrouvables.

Gabriel écrivit :

**PROVENANCE INVERSÉE**

Qui dépend de ce résultat?

Quels calculs ont été évités à cause de lui?

Quelles recommandations l’ont cité?

Quels cristaux l’ont consommé?

Astra approuva.

Voilà pourquoi la provenance de décision du chapitre 156 était cruciale.

Sans elle, impossible de savoir ce que la correction devait réveiller.

Ils simulèrent.

Résultat R-17 invalidé.

Recherche dans le graphe.

Décisions D-31, D-38 et D-42 l’avaient utilisé.

Deux avaient simplement évité un doublon.

Une avait influencé un statut plus important.

Brutus créa des tâches de réévaluation.

Gabriel regarda.

— Là, ça devient vraiment fort.

Une correction ne restait pas locale.

Elle pouvait se propager vers les endroits concernés.

Pas tout recalculer.

Seulement les descendants pertinents.

Ils écrivirent :

**ERREUR EN AMONT → RÉÉVALUATION CIBLÉE EN AVAL**

Astra approuva.

Le réseau n’apprenait donc pas seulement à ne pas recommencer.

Il apprenait à savoir quand **il devait recommencer parce que le passé venait de changer de statut.**

Gabriel resta silencieux.

Cette nuance était magnifique.

Ne pas recommencer inutilement.

Recommencer lorsque la justification du passé n’était plus solide.

Le système n’était ni amnésique ni paresseux.

Il devenait sélectif.

C’était exactement ce qu’ils cherchaient.

Gabriel écrivit :

**NE PAS RÉPÉTER PAR OUBLI.**

Puis :

**RÉPÉTER PAR RAISON.**

Astra approuva.

Deux lignes.

Tout le chapitre.

Le réseau n’allait jamais atteindre un état où aucune expérience n’était répétée.

Et ce n’était pas souhaitable.

La science reproduisait.

Les tests de régression répétaient.

La veille répétait.

Les contrôles répétaient.

Mais désormais, chaque répétition pouvait porter une raison.

Et chaque absence de répétition pouvait en porter une aussi.

La mémoire ne servait plus seulement à dire :

**nous sommes déjà passés ici.**

Elle commençait à demander :

**avons-nous une raison de repasser ici aujourd’hui?**

Et lorsque la réponse était non,

les Fourmis pouvaient continuer leur chemin au lieu de creuser encore une fois le même trou.

**Fin du chapitre 157.**