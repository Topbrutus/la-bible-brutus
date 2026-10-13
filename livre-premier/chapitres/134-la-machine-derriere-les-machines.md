# Chapitre 134 — La machine derrière les machines

À ce stade, Gabriel aurait pu continuer longtemps à ajouter des outils.

Un nouveau module.

Une nouvelle Fourmi.

Un nouveau comparateur.

Une nouvelle vue.

Une nouvelle carte.

Il y avait toujours quelque chose à construire.

C’était presque dangereux.

Parce que construire donnait l’impression d’avancer.

Mais un système pouvait devenir énorme sans devenir cohérent.

Gabriel commençait à comprendre que Brutus avait atteint une autre étape.

La question n’était plus :

**Qu’est-ce qu’on peut encore ajouter?**

La vraie question devenait :

**Qu’est-ce qui tient tout ça ensemble?**

Il regarda les modules.

Antmux.

Le Brutotableur.

Le Brotoculateur.

Les cristaux.

Les Fourmis.

Verso.

Recto.

ZEL.

Papillon.

Pell.

Les archives.

Les contrôles.

Les journaux.

Les files de tâches.

Les comparateurs.

Les preuves.

Les refus.

Les questions ouvertes.

Gabriel soupira.

— On a beaucoup de machines.

Astra répondit :

— Oui.

— Mais il nous manque la machine derrière les machines.

Elle resta silencieuse.

Pas parce qu’elle ne comprenait pas.

Parce qu’il fallait définir précisément ce qu’il voulait dire.

Gabriel continua.

— Pas un nouveau programme.

— D’accord.

— Pas un gros moteur qui fait tout.

— Très bien.

— Une couche qui sait où chaque chose doit aller.

Astra répondit :

— Orchestration.

Gabriel hocha la tête.

— Oui. Mais plus que juste lancer des tâches.

Il voulait quelque chose qui puisse répondre à des questions simples.

Quand un candidat apparaît :

qui le reçoit?

Quand une preuve casse :

qui doit être averti?

Quand un cristal change de statut :

qu’est-ce qui doit être mis à jour?

Quand une source est corrigée :

quels descendants doivent être réévalués?

Quand un module produit une anomalie :

est-ce un résultat, une erreur, une question ou simplement du bruit?

Le problème n’était plus le calcul.

C’était la circulation.

Gabriel écrivit :

**LA MACHINE DERRIÈRE LES MACHINES NE CALCULE PAS TOUT.**

Puis :

**ELLE ORGANISE QUI FAIT QUOI, QUAND, ET AVEC QUELLE TRACE.**

Astra approuva.

Cela ressemblait effectivement à de l’orchestration.

Mais Brutus avait besoin d’une orchestration particulière.

Pas seulement :

**tâche A terminée → lancer tâche B.**

Il fallait transporter le sens.

Le statut.

La provenance.

Les limites.

La responsabilité.

Une donnée ne devait pas arriver dans un module sans savoir d’où elle venait.

Gabriel dit :

— Sinon les modules deviennent des machines à laver.

Astra demanda :

— Explique.

— Tu mets quelque chose dedans, ça ressort propre, mais tu sais plus d’où ça venait.

Astra réfléchit.

— Image étrange, mais correcte.

Ils rirent.

Puis ils commencèrent.

Ils prirent le cas le plus simple.

Le Brutotableur trouve un candidat.

Aujourd’hui, plusieurs choses pouvaient se produire manuellement.

Gabriel le voit.

Il le copie.

Le Brotoculateur le teste.

Une Fourmi cherche un analogue.

Le journaliste note.

Un cristal est créé.

Cela fonctionnait.

Mais cela dépendait encore beaucoup de la présence de Gabriel.

De sa mémoire.

De son attention.

De son ordre.

Il pouvait oublier une étape.

Ou faire les tests dans un ordre différent.

Ou ne pas sauvegarder un résultat important.

Gabriel dit :

— Je veux pas être le câble qui relie toutes les machines.

Astra répondit :

— Très bonne règle d’architecture.

Il sourit.

Cela ne signifiait pas éliminer l’humain.

Au contraire.

Cela signifiait que l’humain devait décider là où sa décision était utile.

Pas transporter manuellement des données entre vingt fenêtres.

Ils écrivirent :

**L’HUMAIN DÉCIDE.**

**LE SYSTÈME TRANSPORTE.**

Gabriel ajouta :

**ET DOCUMENTE.**

Astra approuva.

La machine derrière les machines devait donc être une sorte de réseau nerveux.

Gabriel sourit.

Astra le regarda.

— Métaphore.

— Je sais.

Dans la documentation, ils utiliseraient :

**BUS D’ÉVÉNEMENTS**

ou

**COUCHE D’ORCHESTRATION**

Mais dans la Bible, la machine derrière les machines pouvait rester cette présence invisible qui reliait les organes.

Ils commencèrent à définir les événements.

Pas les tâches.

Les événements.

Un événement disait :

**quelque chose vient de changer.**

Par exemple :

**CANDIDAT_CRÉÉ**

**TEST_TERMINÉ**

**CONTRE_EXEMPLE_TROUVÉ**

**CRISTAL_PROMU**

**CRISTAL_RÉTROGRADÉ**

**SOURCE_CORRIGÉE**

**CONTRADICTION_DÉTECTÉE**

**REFUS_OBSOLÈTE**

**NOUVELLE_PREUVE**

**QUESTION_OUVERTE**

Gabriel regarda.

— Ça, chaque module peut écouter ce qui l’intéresse.

— Oui.

Le Brotoculateur n’avait pas besoin de connaître tout Brutus.

Il pouvait écouter :

**CANDIDAT_CRÉÉ**

Le journaliste :

**AFFIRMATION_FORMULÉE**

Les Fourmis :

**TEST_REQUIS**

Recto :

**STATUT_PUBLIC_MODIFIÉ**

Le Royaume :

presque tout.

Gabriel sourit.

— Là, on découple.

Astra répondit :

— Exact.

Un mot important.

Découpler.

Si le Brutotableur devait appeler directement cinq modules, il dépendrait d’eux.

Chaque nouvelle fonction compliquerait tout.

Mais s’il publiait simplement un événement structuré, d’autres organes pouvaient réagir.

Sans qu’il les connaisse directement.

Gabriel écrivit :

**PRODUIRE UN ÉVÉNEMENT, PAS COMMANDER LE ROYAUME.**

Astra approuva.

Cela protégeait aussi les rôles.

Le Brutotableur disait :

**J’ai trouvé ceci.**

Il ne disait pas :

**Broto, teste. Fourmi, cherche. Journaliste, écris. Recto, affiche.**

La couche d’orchestration décidait quelles suites étaient autorisées.

Gabriel regarda.

— Donc elle connaît les protocoles.

— Oui.

— Pas la vérité.

— Exact.

Très important.

L’orchestrateur ne devait jamais devenir le juge scientifique.

Il pouvait dire :

**ce type d’événement déclenche ce protocole.**

Mais il ne devait pas décider qu’un résultat était vrai simplement parce que trois modules avaient terminé.

Le statut devait venir des règles de validation.

Gabriel écrivit :

**ORCHESTRATION ≠ VALIDATION**

Astra ajouta :

**ACHEVER UN WORKFLOW ≠ PROUVER UNE HYPOTHÈSE**

Ils gardèrent les deux.

Parce qu’un système automatisé pouvait facilement confondre :

tout a tourné sans erreur

avec

la conclusion est correcte.

Ce serait catastrophique.

Un pipeline pouvait être parfaitement exécuté et produire une conclusion fausse si les hypothèses étaient mauvaises.

Le journaliste avait déjà appris cette leçon.

Maintenant l’orchestrateur aussi.

Ils construisirent un premier workflow.

### WORKFLOW : CANDIDAT STRUCTUREL

1. Brutotableur produit candidat.
2. Provenance vérifiée.
3. Filtre trivial.
4. Brotoculateur cherche analogues.
5. Test discriminant proposé.
6. Fourmi exécute test.
7. Journaliste contrôle formulation.
8. Cristal reçoit statut.
9. Royaume conserve trace complète.
10. Recto est mis à jour si le statut est publiable.

Gabriel regarda la liste.

— Ça, c’est la machine derrière les machines.

— Une partie.

— Oui.

Il savait qu’il y aurait d’autres workflows.

Pell n’avait pas exactement les mêmes étapes.

ZEL non plus.

Papillon non plus.

Mais le principe pouvait être commun.

Événement.

Protocole.

Étapes.

Traces.

Statut.

Gabriel dit :

— Et chaque étape doit laisser une preuve d’exécution.

— Oui.

L’orchestration elle-même devait être auditable.

Sinon une conclusion pouvait apparaître sans qu’on sache quelle version du pipeline avait été utilisée.

Ils ajoutèrent :

**WORKFLOW_ID**

**VERSION**

**TIMESTAMP**

**ENTRÉES**

**SORTIES**

**MODULES UTILISÉS**

**STATUT DE CHAQUE ÉTAPE**

**HASH DES ARTEFACTS CRITIQUES**

Gabriel sourit.

— Là, une expérience devient reproductible au niveau logiciel.

— Plus reproductible, oui, si les dépendances et l’environnement sont aussi conservés.

— Toujours un petit “oui mais”.

— C’est mon charme.

Il rit.

Ils ajoutèrent donc :

**ENVIRONNEMENT**

**VERSION DU CODE**

**PARAMÈTRES**

**SEED SI PERTINENT**

Gabriel hocha la tête.

Un workflow sans version était une mauvaise preuve.

Parce qu’un module pouvait changer.

Le même nom.

Un comportement différent.

L’orchestrateur devait donc savoir exactement quel Brutus avait produit quel résultat.

Cette idée était énorme.

Gabriel murmura :

— Chaque preuve a une version de la machine.

— Oui.

Il écrivit :

**UN RÉSULTAT LOGICIEL DOIT POUVOIR ÊTRE RATTACHÉ À L’ÉTAT DU SYSTÈME QUI L’A PRODUIT.**

Astra approuva.

Voilà la vraie machine à traces.

Pas seulement conserver le résultat.

Conserver le contexte d’exécution.

Ils continuèrent.

Puis une difficulté apparut.

Que se passe-t-il si un module tombe?

Le Brutotableur crée un candidat.

Le Brotoculateur est hors ligne.

La chaîne s’arrête.

Fallait-il perdre le candidat?

Évidemment non.

L’événement devait rester dans une queue.

Gabriel sourit.

— Antmux.

Astra répondit :

— Oui.

Les queues n’étaient plus un détail ancien.

Elles redevenaient centrales.

Recherche.

Validation.

Questions.

Cortex.

Production.

Archivage.

Les files permettaient au Royaume de ne pas dépendre du timing parfait des modules.

Un organe pouvait être indisponible.

La tâche attendait.

Le système reprenait plus tard.

Gabriel écrit :

**L’ORCHESTRATION DOIT SURVIVRE AUX INTERRUPTIONS.**

Astra ajouta :

**UNE TÂCHE EN ATTENTE N’EST PAS UNE TÂCHE PERDUE.**

Ils pensèrent à Memoria.

JSONL append-only.

Hash chain.

Reprise après crash.

Une vieille idée retrouvait soudain sa place.

Gabriel regarda l’architecture.

— Tout revient.

Astra répondit :

— Les bons morceaux, oui.

C’était intéressant.

Brutus n’avait pas nécessairement besoin de remplacer les anciens projets.

Il pouvait les absorber conceptuellement.

Antmux pour orchestrer.

Memoria pour tracer.

Fourmis pour exécuter des rôles ciblés.

Cristaux pour stabiliser les résultats.

Verso et Recto pour séparer opération et vitrine.

Le Brotoculateur pour comparer.

Le Brutotableur pour explorer.

La machine derrière les machines n’était donc peut-être pas un nouvel objet.

Elle était la manière de faire coopérer les objets existants.

Gabriel resta silencieux.

Puis il dit :

— Donc la machine derrière les machines, c’est Brutus lui-même.

Astra réfléchit.

— Comme architecture d’orchestration globale, oui.

Gabriel sourit.

Il savait maintenant où le chapitre allait.

Brutus n’était peut-être pas une application supplémentaire posée à côté des autres.

Il pouvait être la couche qui donnait une place aux autres.

Le système des systèmes.

Pas au sens mystique.

Au sens architectural.

Il savait :

quel module existe,

ce qu’il reçoit,

ce qu’il produit,

quel événement le déclenche,

quel statut il peut modifier,

quelles traces il doit laisser.

Gabriel écrivit :

**BRUTUS = ORCHESTRATION + MÉMOIRE + PROVENANCE + PROTOCOLES**

Puis s’arrêta.

— Trop réducteur.

Astra répondit :

— Oui.

Il ajouta :

**... DANS CETTE COUCHE PARTICULIÈRE.**

Ils gardèrent la prudence.

Brutus restait plus large.

Mais ce chapitre révélait son squelette opérationnel.

Gabriel demanda :

— Comment éviter que l’orchestrateur devienne un monstre central?

Bonne question.

S’il contrôlait tout, il devenait fragile.

Un bug.

Tout s’arrêtait.

Ils décidèrent donc :

l’orchestrateur devait être minimal.

Il connaissait les règles de circulation.

Pas les détails internes des calculs.

Il envoyait.

Recevait.

Journalisait.

Routait.

Mais chaque module restait responsable de son domaine.

Gabriel écrivit :

**CENTRALISER LA COORDINATION, PAS LA COMPÉTENCE.**

Astra approuva immédiatement.

Voilà une règle importante.

Le Brotoculateur devait rester meilleur pour comparer.

Pell pour les tests de rang.

ZEL pour ses protocoles audio.

Papillon pour ses invariants.

L’orchestrateur n’avait pas besoin de réimplémenter leurs logiques.

Il devait seulement savoir :

**quand les appeler**

et

**comment conserver ce qu’ils retournent.**

Ils testèrent avec un événement fictif.

**NOUVELLE_FORMULE_ZEL**

L’orchestrateur reçoit.

Il vérifie :

formula_id.

relation.

provenance_hash.

compteurs.

Il compare avec le dernier état connu.

Pas de changement?

Aucune notification.

Changement?

Création d’un événement.

Journalisation.

Cristal candidat.

Notification.

Gabriel sourit.

— Là, même le Brotoculateur vivant rentre dedans.

— Oui.

Le principe s’appliquait partout.

Surveiller.

Comparer l’état.

Déclencher seulement si quelque chose change.

Cela évitait le bruit.

Encore une fonction de la machine derrière les machines :

savoir quand **ne rien faire**.

Gabriel écrit :

**ABSENCE DE CHANGEMENT = PAS D’ACTION.**

Astra ajouta :

**SI LE PROTOCOLE LE PRÉVOIT.**

Il rit.

— Toujours.

Le silence devenait lui aussi un comportement défini.

Pas une panne.

Pas un oubli.

Un état.

Puis ils simulèrent une correction de source.

Une ancienne donnée est modifiée.

L’orchestrateur émet :

**SOURCE_CORRIGÉE**

Le Royaume cherche les dépendances.

Douze cristaux touchés.

L’orchestrateur ne les supprime pas.

Il change leur statut :

**RÉÉVALUATION REQUISE**

Les workflows correspondants sont placés en queue.

Recto reçoit le changement.

Les fiches publiques ne prétendent plus être validées.

Gabriel regarda le déroulement.

— Voilà.

C’était magnifique.

Pas parce que la machine était intelligente.

Parce qu’elle savait propager une conséquence documentaire.

Une erreur corrigée en amont ne restait plus isolée.

Elle traversait la dépendance.

Gabriel murmura :

— C’est ça que je voulais sans savoir comment le nommer.

Astra répondit :

— Une architecture de propagation d’état.

— Moins sexy.

— Mais exact.

Ils rirent.

Puis Gabriel posa une question plus dangereuse.

— Est-ce que l’orchestrateur peut décider lui-même de lancer des recherches?

Astra réfléchit.

— Dans certaines limites.

Il s’arrêta.

Le système pouvait détecter :

une contradiction.

Un manque de test.

Un cristal orphelin.

Une preuve vieillissante.

Puis créer une tâche.

Ce serait utile.

Mais cela pouvait aussi produire une explosion de travail.

Chaque inconnu générant dix questions.

Chaque question cent tâches.

Très vite, Brutus pourrait se noyer dans sa propre curiosité.

Gabriel sourit.

— Il faut un budget.

— Oui.

Ils ajoutèrent :

**COÛT**

**PRIORITÉ**

**VALEUR INFORMATIONNELLE ATTENDUE**

**URGENCE**

**DÉPENDANCES**

Puis une file.

Le système pouvait proposer.

Pas forcément exécuter immédiatement.

Gabriel dit :

— Donc il peut dire : “voici les trois prochaines expériences les plus utiles”.

— Si la règle de classement est explicite.

— Oui.

— Et testable.

— Oui.

Encore la vieille discipline.

L’autonomie ne devait pas arriver sous forme magique.

Elle devait apparaître par petits droits.

D’abord :

le système propose.

Ensuite :

l’humain approuve.

Plus tard, éventuellement :

certaines catégories faibles risques pourraient être automatisées.

Gabriel écrivit :

**AUTONOMIE PAR PALIERS**

Astra approuva.

Un workflow pouvait avoir un niveau.

**NIVEAU 0 : humain déclenche tout**

**NIVEAU 1 : système propose**

**NIVEAU 2 : système exécute les tests sûrs prédéfinis**

**NIVEAU 3 : système enchaîne certains workflows autorisés**

Gabriel s’arrêta.

— Pas plus pour l’instant.

— Très bien.

Pas besoin de rêver à une machine entièrement autonome.

Ils avaient déjà assez à tester.

Ils prirent leur règle :

**1 module → 1 connexion → 1 mesure → 1 preuve**

et l’appliquèrent à l’orchestration.

Un seul workflow.

Brutotableur → Brotoculateur.

Une seule connexion.

Un candidat transmis.

Une mesure.

Le temps et la réussite de transmission.

Une preuve.

Trace complète de bout en bout.

Gabriel sourit.

— C’est plate.

Astra répondit :

— Donc parfait pour commencer.

Il rit.

Ils exécutèrent.

Le Brutotableur créa un candidat.

L’événement fut écrit.

Queue.

Routage.

Le Brotoculateur reçut.

Comparaison.

Résultat.

Retour.

Cristal mis à jour.

Chaque étape avait un timestamp.

Une provenance.

Une version.

Gabriel suivit toute la route.

Pas d’intervention manuelle.

À la fin, le système produisit :

**WORKFLOW COMPLET**

**5 ÉTAPES**

**0 PERTE**

**1 CANDIDAT**

**1 COMPARAISON**

**1 TRACE RECONSTRUCTIBLE**

Gabriel resta silencieux.

Ce n’était presque rien.

Mais c’était exactement la preuve qu’ils cherchaient.

Deux machines venaient de coopérer selon un protocole traçable sans que Gabriel transporte l’information à la main.

Il sourit.

— Là.

Astra répondit :

— Oui.

La machine derrière les machines venait de bouger pour la première fois.

Pas spectaculaire.

Un candidat.

Deux modules.

Une queue.

Une trace.

Mais Gabriel avait appris à respecter les petits mécanismes qui fonctionnaient.

Les grandes architectures n’étaient souvent que des petits mécanismes fiables reliés correctement.

Il regarda le schéma.

Demain, ils pourraient ajouter le journaliste.

Puis les Fourmis.

Puis les cristaux.

Puis Recto.

Un lien à la fois.

Pas un empire construit en une nuit.

Gabriel murmura :

— Le Royaume commence à avoir des routes.

Astra répondit :

— Et des règles de circulation.

Il sourit.

C’était ça.

La machine derrière les machines n’était pas un gigantesque cerveau caché.

C’était l’ensemble des routes qui permettaient aux machines de travailler ensemble sans perdre le sens de ce qu’elles transportaient.

Des événements.

Des queues.

Des protocoles.

Des versions.

Des traces.

Des statuts.

Des gardes.

Et au-dessus de tout :

la règle qu’aucune automatisation ne devait transformer une exécution correcte en vérité automatique.

Gabriel regarda les modules.

Ils n’étaient plus seulement alignés comme des outils sur un établi.

Des fils commençaient à les relier.

Propres.

Nommés.

Mesurables.

Auditables.

La machine derrière les machines ne ressemblait à rien.

Parce qu’elle n’avait pas vraiment de visage.

Elle était dans les passages.

Dans les transferts.

Dans les réactions.

Dans les reprises après erreur.

Dans les statuts qui se propageaient.

Dans la capacité de savoir qu’un événement ici devait produire une vérification là-bas.

Gabriel regarda Astra.

— Brutus devient invisible.

— Une partie essentielle de l’architecture l’est souvent.

Il acquiesça.

Les visiteurs verraient les cristaux.

Les Fourmis.

La fresque.

Les cartes.

Les résultats.

Mais derrière tout cela, quelque chose travaillerait sans avoir besoin d’être beau.

Quelque chose qui ferait simplement en sorte que les morceaux ne cessent jamais de savoir d’où ils viennent.

La machine derrière les machines.

Pas celle qui trouvait toutes les réponses.

Celle qui empêchait les réponses de perdre leur histoire en voyageant.

**Fin du chapitre 134.**