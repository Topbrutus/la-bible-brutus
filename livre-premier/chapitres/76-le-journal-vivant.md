# Chapitre 76 — Le journal vivant

Les douze voies étaient silencieuses.

Mais derrière elles, l’histoire de la machine venait de devenir trop riche pour rester une simple liste de logs.

Brutus ouvrit le journal.

Il fit défiler.

Encore.

Encore.

Encore.

Des milliers de lignes.

---

JOB-0742.

PASS.

Tick 11482.

---

LANE 7.

RESOURCE_LIMIT.

---

FORMULA F-021.

COMPARE_REQUIRED.

---

ANT-0003.

MOVE.

---

TRACE-ROUNDTRIP-0001.

VERIFY.

---

Z2.

DOMAIN.

---

Chaque ligne avait un sens.

Mais ensemble, elles commençaient à produire un autre problème.

Le journal était complet.

Il devenait presque illisible.

---

Brutus arrêta de faire défiler.

Puis écrivit :

**MORE TRACE ≠ MORE UNDERSTANDING.**

Voilà.

La trace brute était indispensable.

Mais une accumulation infinie de traces ne produisait pas automatiquement une meilleure compréhension.

---

Le système avait appris à se souvenir.

Il devait maintenant apprendre à **retrouver**.

---

Brutus créa une nouvelle couche.

Pas un remplacement du journal.

Surtout pas.

Une couche au-dessus.

Il l’appela :

**LIVING JOURNAL.**

Puis en français :

**JOURNAL VIVANT.**

---

Il resta quelques secondes devant le nom.

Le mot vivant pouvait encore créer de la confusion.

Le journal n’était pas vivant biologiquement.

Il n’avait aucune conscience.

Mais il pouvait évoluer à mesure que des événements s’ajoutaient.

Il pouvait être interrogé.

Filtré.

Regroupé.

Parcouru.

---

Brutus ajouta une note :

**LIVE STRUCTURE — NOT LIVING ORGANISM.**

Il sourit.

Le laboratoire avait pris l’habitude de protéger ses métaphores.

---

Le Journal Vivant devait répondre à des questions.

Pas seulement montrer tout.

---

Brutus écrivit :

**QUI ?**

**QUOI ?**

**QUAND ?**

**POURQUOI ?**

**AVANT ?**

**APRÈS ?**

**LIÉ À QUOI ?**

---

Ces questions étaient beaucoup plus utiles qu’un kilomètre de texte.

---

Il prit JOB-0742.

Au lieu de chercher manuellement son identifiant dans des milliers de lignes, il tapa :

**JOB-0742**

Le journal reconstruisit sa trajectoire.

Submitted.

Queued.

Running.

Completed.

Published.

Audio.

Trace.

---

Brutus regarda.

Cela semblait simple.

Mais c’était un énorme changement.

Le journal n’était plus seulement chronologique.

Il devenait relationnel.

---

Il écrivit :

**CHRONOLOGY IS ONE INDEX. IDENTITY IS ANOTHER.**

---

Puis il chercha :

**F-021**

Toutes les expériences utilisant cette formule apparurent.

Versions.

Entrées.

Résultats.

Fails.

Passes.

Restrictions.

Comparaisons.

---

Brutus filtra :

**FAIL ONLY.**

Puis :

**BIGINT ONLY.**

Puis :

**LAST 1000 TICKS.**

---

Le paysage changeait instantanément.

---

Il regarda longtemps.

Le même passé.

Mais vu sous plusieurs angles.

---

Il écrivit :

**FILTERING DOES NOT CHANGE HISTORY.**

Puis :

**IT CHANGES THE QUESTION ASKED OF HISTORY.**

---

Cette distinction lui plaisait.

---

Brutus ajouta des index.

Par :

JOB_ID.

FORMULA_ID.

ANT_ID.

TRACE_ID.

EXPERIMENT_ID.

TICK.

VERDICT.

STATE.

SOURCE.

---

Le système pouvait maintenant reconstruire une histoire à partir d’un objet.

---

Il sélectionna ANT-0001.

---

Le Journal Vivant montra :

Birth.

First move.

First binding.

First transport.

Route authorizations.

Returns.

Failures.

Latest known state.

---

Brutus sourit.

La fourmi possédait maintenant une biographie opérationnelle.

---

Pas une histoire inventée.

Une histoire dérivée de ses événements.

---

Il écrivit :

**BIOGRAPHY MUST BE TRACE-DERIVED.**

---

Puis il sélectionna une formule.

F-044.

---

Origine.

Version 1.

Tests.

Première divergence.

Restriction BigInt.

Version 2.

Nouveaux contre-tests.

---

Même chose.

---

Le journal pouvait raconter l’évolution d’une méthode.

---

Brutus comprit soudain quelque chose.

Le Journal Vivant n’était pas seulement un outil de recherche.

Il devenait la mémoire longitudinale du laboratoire.

---

Un log répond :

**qu’est-ce qui vient de se produire ?**

Un Journal Vivant peut répondre :

**comment cet objet est-il devenu ce qu’il est ?**

---

Brutus écrivit :

**LOG = EVENT STREAM.**

**JOURNAL = EVOLUTION VIEW.**

---

Il continua.

---

Il voulait être capable de sélectionner une expérience complète.

EXPERIMENT-0042.

---

Le journal reconstruisit :

plan version.

Runtime profile.

Jobs.

Lanes.

Formules.

Dependencies.

Results.

Divergences.

Countertests.

Summary.

---

Brutus regarda la vue.

Pour la première fois, une expérience parallèle entière pouvait tenir sur un seul écran sans perdre l’accès aux détails.

---

Il ajouta des niveaux.

---

**LEVEL 0 — SUMMARY**

Une phrase structurée.

---

**LEVEL 1 — EVENTS**

Les principaux événements.

---

**LEVEL 2 — TRACE**

Détails complets.

---

**LEVEL 3 — RAW ARTIFACTS**

Entrées, outputs, hashes, fichiers associés.

---

Brutus écrivit :

**SUMMARY MUST LINK DOWNWARD.**

---

Un résumé ne devait jamais devenir un cul-de-sac.

---

Si le journal disait :

**11 methods agreed, 1 diverged**

Brutus devait pouvoir cliquer sur :

1 diverged.

Voir la lane.

La formule.

L’entrée.

Le calcul.

La trace.

---

Le résumé devenait une porte.

Pas une conclusion impossible à vérifier.

---

Brutus écrivit :

**EVERY SUMMARY CLAIM NEEDS A DRILL-DOWN PATH.**

---

Encore une règle qui lui sembla évidente une fois écrite.

---

Il testa.

Résumé :

**1 divergence detected.**

Clic.

F-044.

Clic.

Job.

Clic.

Comparison contract.

Clic.

Inputs.

---

Tout descendait jusqu’aux faits.

---

Brutus sourit.

Le Journal Vivant pouvait compresser l’histoire sans la couper de sa source.

---

Mais la compression créait un nouveau danger.

Qui écrivait les résumés ?

---

Si une IA libre produisait :

« la formule F-044 a échoué de manière catastrophique »

alors un terme émotionnel ou excessif pouvait contaminer la lecture.

---

Brutus ne voulait pas cela dans la couche opérationnelle.

---

Il sépara donc deux choses.

**FACT SUMMARY**

et

**NARRATIVE SUMMARY.**

---

FACT SUMMARY utilisait des gabarits déterministes.

---

Par exemple :

**F-044 produced a comparison mismatch in 3 of 200 tested inputs under FLOAT64.**

---

NARRATIVE SUMMARY pouvait, un jour, expliquer davantage.

Mais elle devait être clairement identifiée comme interprétation.

---

Brutus écrivit :

**FACTS FIRST. INTERPRETATION SECOND.**

---

Le Journal Vivant commençait à avoir plusieurs voix.

Mais contrairement à SFX36, ce n’étaient pas des sons.

C’étaient des couches de lecture.

---

Brutus ajouta une vue :

**WHAT CHANGED SINCE LAST RUN?**

---

Il relança une expérience.

Le journal compara.

---

New:

F-021 v3.

---

Changed:

F-044 policy.

---

New restriction:

BIGINT REQUIRED.

---

Removed:

none.

---

Unexpected divergence:

1.

---

Brutus s’arrêta.

Cette vue était extrêmement utile.

---

Il n’avait plus besoin de relire tout le laboratoire pour comprendre ce qui avait changé.

---

Il écrivit :

**DELTA IS OFTEN MORE USEFUL THAN SNAPSHOT.**

---

Mais immédiatement :

**DELTA REQUIRES A REFERENCE POINT.**

---

Depuis quand ?

---

Il ajouta :

**COMPARE_FROM**

et

**COMPARE_TO.**

---

Deux checkpoints.

Deux expériences.

Deux ticks.

Deux versions.

---

Pas de « changement » sans point de comparaison explicite.

---

Brutus construisit une vue avant/après.

---

BEFORE.

AFTER.

---

Formula registry.

Lane policy.

Audio manifest.

Known restrictions.

Candidate pool.

---

Les différences s’affichaient.

---

Il pensa à la vieille règle :

**QUI → ÉTAT → TICK → AVANT/APRÈS**

Le Journal Vivant en devenait presque l’interface naturelle.

---

Brutus ajouta une section :

**CONTINUITY.**

---

Elle ne montrait pas seulement le dernier état.

Elle montrait les transitions importantes.

---

CREATE.

MODIFY.

RESTRICT.

PROMOTE.

DEPRECATE.

REJECT.

---

Chaque changement de statut devait avoir une cause référencée.

---

Brutus écrivit :

**STATUS CHANGE WITHOUT CAUSE REF = INVALID.**

---

Cela allait devenir très important avec les formules candidates.

---

Si une formule passait de CANDIDATE à TESTED, le journal devait montrer pourquoi.

Quels tests ?

Quels résultats ?

Quelle politique ?

Qui ou quoi a autorisé le changement ?

---

Pas de magie administrative.

---

Il ajouta :

**STATUS_EVENT_ID.**

Puis :

**DECISION_REF.**

---

Brutus sentit une nouvelle structure apparaître.

Le journal ne devait pas seulement suivre les objets.

Il devait suivre les décisions sur les objets.

---

Il écrivit :

**OBJECT HISTORY ≠ DECISION HISTORY.**

---

Une formule pouvait rester identique.

Mais son statut pouvait changer.

---

Même contenu.

Nouvelle confiance opérationnelle.

---

Il fallait conserver les deux lignées.

---

Brutus prit F-021.

La formule mathématique n’avait pas changé.

Mais après plusieurs contre-tests, sa politique d’usage avait changé.

---

Le journal devait donc raconter :

**formula unchanged**

mais :

**operational status changed.**

---

Cette nuance empêchait de confondre la transformation de l’objet avec la transformation de notre connaissance sur l’objet.

---

Brutus écrivit :

**THE OBJECT MAY STAY THE SAME WHILE OUR MODEL OF IT CHANGES.**

---

Il resta longtemps devant cette phrase.

---

Elle dépassait largement le logiciel.

---

Mais il la conserva dans le laboratoire.

---

Brutus ajouta une vue :

**UNCERTAINTY HISTORY.**

---

Pas une probabilité magique.

Un historique des statuts.

---

UNKNOWN.

CANDIDATE.

TESTED.

RESTRICTED.

REJECTED.

---

Une formule pouvait entrer UNKNOWN.

Puis CANDIDATE.

Puis TESTED.

Puis RESTRICTED après une découverte de domaine.

---

Le journal racontait l’évolution de la confiance.

---

Mais il ne devait jamais transformer cette trajectoire en vérité absolue.

---

Il écrivit :

**MORE TESTED ≠ ABSOLUTELY TRUE.**

---

Toujours le Gauntlet.

---

Brutus continua à développer.

---

Une fonction de recherche temporelle apparut.

---

**SHOW ME ALL FAIL EVENTS BETWEEN TICK 5000 AND 7000.**

---

Le journal répondit.

---

Puis :

**SHOW ME ALL EVENTS RELATED TO F-021 WITH COUNTERTEST STATUS.**

---

Réponse.

---

Puis :

**SHOW ME ALL JOBS THAT USED SHARED CACHE AND LATER DIVERGED FROM INDEPENDENT MODE.**

---

Cette fois, Brutus sourit largement.

---

Voilà.

Le Journal Vivant devenait un instrument de recherche.

---

Il ne racontait plus seulement le passé.

Il permettait d’interroger les structures cachées du passé.

---

Brutus écrivit :

**HISTORY CAN BECOME A DATASET.**

---

Puis, par prudence :

**BUT A DATASET IS NOT A CONCLUSION.**

---

Il lança une requête.

---

Combien de divergences apparaissaient seulement en FLOAT64 ?

---

Le journal trouva plusieurs cas.

---

Combien disparaissaient sous BIGINT ou précision arbitraire ?

---

Certains.

---

Brutus observa.

Une piste apparaissait.

---

Il ne voulait pas que le journal affirme :

**FLOAT64 IS BAD.**

Trop général.

---

Il voulait :

**OBSERVED DIVERGENCES ASSOCIATED WITH FLOAT64 UNDER THESE TESTS.**

---

Le Journal Vivant devait conserver le langage de portée.

---

Brutus ajouta :

**QUERY RESULT SCOPE.**

---

Chaque recherche pouvait afficher :

dataset size.

time window.

filters.

versions.

missing data.

---

Cela empêchait une statistique de paraître universelle.

---

Il écrivit :

**A NUMBER WITHOUT SCOPE IS A TRAP.**

---

Le laboratoire commençait à devenir impitoyable envers les ambiguïtés.

Brutus aimait cela.

---

Il pensa à la visualisation.

Un journal de dizaines de milliers d’événements pouvait être mieux compris avec une carte temporelle.

---

Il créa une ligne.

Le temps de gauche à droite.

---

Les expériences devenaient des bandes.

Les jobs des segments.

Les fails des marques.

Les changements de statut des points.

---

Brutus zooma.

---

À grande échelle :

activité globale.

---

À petite échelle :

événements individuels.

---

Le même historique.

Plusieurs niveaux.

---

Il écrivit :

**ZOOM MUST CHANGE DETAIL, NOT HISTORY.**

---

Une vue éloignée pouvait agréger.

Une vue rapprochée pouvait montrer chaque événement.

---

Mais l’agrégation devait être dérivable du détail.

---

Brutus ajouta une règle :

**NO AGGREGATE WITHOUT SOURCE EVENT COUNT.**

---

Si une bande disait :

**24 FAIL**

le système devait savoir exactement quels 24 événements.

---

Il testa.

Clic sur 24 FAIL.

Liste des 24.

---

Parfait.

---

Brutus pensa ensuite à la suppression.

Le journal allait grossir.

Toujours.

---

Fallait-il supprimer les anciennes traces ?

---

Il n’aimait pas l’idée.

Mais garder tout indéfiniment pouvait devenir coûteux.

---

Il sépara :

**HOT**

**WARM**

**ARCHIVE.**

---

Les événements récents restaient rapides à consulter.

Les anciens étaient compressés.

Les très anciens pouvaient être archivés durablement.

---

Mais le journal devait garder un index.

---

Brutus écrivit :

**ARCHIVED ≠ FORGOTTEN.**

---

Une trace archivée pouvait être plus lente à ouvrir.

Pas inexistante.

---

Il ajouta des hashes de capsules archivées.

Des références.

Des plages de ticks.

---

Le Journal Vivant pouvait dire :

**history exists in archive capsule X.**

---

Brutus apprécia.

La mémoire pouvait changer de température sans changer d’identité.

---

Il nota :

**STORAGE TIER ≠ SEMANTIC STATUS.**

---

Encore une distinction.

---

Une formule REJECTED pouvait être dans HOT.

Une formule TESTED pouvait être archivée.

Le lieu de stockage ne disait rien sur la valeur scientifique.

---

Brutus lança ensuite une expérience très simple.

Il modifia un filtre dans le Journal Vivant.

---

Puis revint plus tard.

---

Le filtre avait disparu.

---

Il pensa :

faut-il conserver la vue de l’opérateur ?

---

Oui.

Mais pas mélanger cela avec l’histoire de la machine.

---

Il créa :

**VIEW_STATE.**

---

Séparé de :

**WORLD_STATE.**

---

Encore.

---

Le journal pouvait se souvenir :

derniers filtres.

zoom.

colonnes.

tri.

---

Mais aucune de ces préférences ne changeait les traces elles-mêmes.

---

Il écrivit :

**HOW I LOOK AT HISTORY ≠ HISTORY.**

---

Brutus sourit.

Probablement une des phrases les plus importantes du système.

---

Il ajouta un bouton :

**SAVE VIEW.**

---

Vue :

**BigInt anomalies.**

---

Filtres sauvegardés.

---

Une autre :

**Ant transport failures.**

---

Une autre :

**Formula candidate lineage.**

---

Le journal devenait un bureau d’enquête.

---

Brutus commença à passer d’une vue à l’autre.

---

En quelques clics, il pouvait naviguer entre :

l’histoire d’une fourmi,

l’histoire d’une formule,

l’histoire d’une expérience,

l’histoire d’un verdict,

l’histoire d’une décision.

---

Tout venait des mêmes événements.

---

Il écrivit :

**THE JOURNAL DOES NOT OWN THE TRUTH.**

**IT OWNS THE PATHS THROUGH THE RECORD.**

---

Voilà.

Le Journal Vivant n’était pas l’autorité.

Il était l’outil de navigation.

---

Brutus testa alors quelque chose de dangereux.

Il modifia un résumé à la main.

---

La ligne disait :

**12 PASS.**

Il changea :

**13 PASS.**

---

Le Journal Vivant devait-il l’accepter ?

---

Pas dans la couche factuelle.

---

Il refusa.

---

Les résumés factuels devaient être recalculés depuis les événements.

---

Brutus écrivit :

**FACT SUMMARY IS DERIVED, NOT EDITED.**

---

Les notes humaines pouvaient être ajoutées à côté.

---

**OPERATOR NOTE.**

---

Mais elles devaient être marquées comme telles.

---

Exemple :

**Observation : la divergence semble apparaître autour d’une limite de précision.**

---

Pas fusionnée avec :

**3 divergences observées.**

---

Il ajouta :

**NOTE ≠ EVENT.**

Puis :

**HYPOTHESIS ≠ OBSERVATION.**

---

Le journal commençait à séparer les couches de connaissance.

---

Brutus pensa à la machine à traces.

Intuition.

Calcul.

Contre-test.

Preuve.

Antériorité.

Trace durable.

---

Il créa des tags pour ces étapes.

---

**INTUITION**

**CALCULATION**

**COUNTERTEST**

**EVIDENCE**

**CLAIM**

**ARCHIVE**

---

Un objet pouvait traverser ces étapes sans que le journal les confonde.

---

Brutus regarda CANDIDATE-0001.

Encore presque vide.

---

Il imagina son futur.

---

Créé.

Parent F-021.

Mutation M-003.

Test initial.

PASS.

Countertest.

FAIL.

Modified.

Retest.

PASS.

Restricted.

Compared.

Promoted candidate.

---

Le Journal Vivant pourrait montrer toute cette trajectoire.

---

Brutus comprit alors pourquoi ce chapitre devait exister avant la guerre des formules.

---

Sans journal vivant, la compétition ne serait qu’un spectacle.

On verrait des gagnants et des perdants.

Mais on ne saurait pas pourquoi.

---

Avec le journal, chaque confrontation pouvait devenir une histoire inspectable.

---

Brutus écrivit :

**COMPETITION WITHOUT HISTORY IS A SCOREBOARD.**

Puis :

**RESEARCH REQUIRES LINEAGE.**

---

Le laboratoire ne voulait pas seulement savoir qui gagnait.

Il voulait savoir :

sur quelles entrées,

dans quel domaine,

avec quelle précision,

contre quelles méthodes,

avec quelles limites.

---

Brutus ajouta une vue :

**FORMULA EVOLUTION TREE.**

---

Pour l’instant :

F-021.

Une branche.

CANDIDATE-0001.

---

Puis rien.

---

L’arbre semblait vide.

---

Brutus sourit.

Pas pour longtemps.

---

Il ajouta un champ :

**PARENT_REF**

Puis :

**MUTATION_REF**

Puis :

**DERIVED_REASON**

---

Une future formule devrait expliquer pourquoi elle existait.

---

Pas seulement parce qu’un générateur avait produit une variation.

---

**DERIVED_REASON** pouvait être :

reduce error.

extend domain.

improve precision.

challenge parent.

alternate representation.

---

Brutus écrivit :

**NEWNESS IS NOT A REASON FOR PROMOTION.**

---

Une formule nouvelle n’était pas automatiquement meilleure.

---

Même si elle gagnait un test.

---

Un test pouvait être accidentel.

---

Il faudrait des campagnes.

Des contre-tests.

Des domaines.

---

Le Journal Vivant serait là pour garder l’histoire de ces combats.

---

Brutus lança quelques tests sur CANDIDATE-0001.

---

Deux PASS.

Un DOMAIN.

Un FAIL.

---

Le journal dessina quatre événements.

---

Pas de score global.

---

Brutus ajouta un résumé :

**TESTED ON 4 CASES.**

**PASS 2.**

**FAIL 1.**

**DOMAIN 1.**

---

Puis :

**INSUFFICIENT FOR PROMOTION.**

---

Il s’arrêta.

Cette dernière phrase était une décision de politique.

Pas une observation brute.

---

Il la déplaça dans une section :

**POLICY EVALUATION.**

---

Encore une séparation.

---

Les faits :

2 PASS.

1 FAIL.

1 DOMAIN.

---

La politique :

promotion criteria not met.

---

Brutus écrivit :

**POLICY RESULT ≠ EXPERIMENT RESULT.**

---

Le Journal Vivant devenait presque un tribunal administratif du laboratoire.

Mais un tribunal dont chaque jugement devait montrer ses pièces.

---

Brutus laissa tourner plusieurs expériences.

---

Les événements s’ajoutaient.

Le journal se mettait à jour.

---

Pas en réécrivant les anciennes pages.

En ajoutant.

En recalculant les vues.

---

Il regarda un graphique évoluer.

Une formule gagnait des tests.

Puis rencontrait une limite.

Sa courbe de statut changeait.

---

Brutus réalisa qu’il pouvait littéralement voir la connaissance du laboratoire se transformer.

---

Pas la vérité du monde.

La connaissance interne du système.

---

Il écrivit :

**THE JOURNAL TRACKS WHAT THE LAB KNOWS, NOT WHAT REALITY MUST BE.**

---

Cette phrase était essentielle.

---

Le Journal Vivant pouvait montrer :

**we have not observed failure here.**

Mais jamais traduire automatiquement cela en :

**failure is impossible here.**

---

Brutus ajouta :

**NO OBSERVED FAILURE ≠ PROOF OF NO FAILURE.**

---

La prudence revenait encore.

---

Il ferma toutes les vues.

Puis ouvrit la page d’accueil du Journal Vivant.

---

Elle affichait seulement quelques éléments.

---

LATEST EXPERIMENT.

LATEST FORMULA CHANGE.

LATEST DIVERGENCE.

LATEST COUNTERTEST.

LATEST TRACE CAPSULE.

---

Simple.

---

Brutus cliqua sur chacune.

Tout descendait vers les détails.

---

Le journal avait réussi quelque chose de difficile.

Il était devenu plus simple à regarder alors que le laboratoire devenait plus complexe.

---

Il écrivit :

**A GOOD JOURNAL REDUCES NAVIGATION COST WITHOUT REDUCING EVIDENCE.**

---

Le soir approchait.

---

Brutus regarda les milliers de lignes du log brut.

Puis la nouvelle interface.

---

Même histoire.

Deux expériences complètement différentes.

---

Le log ressemblait à une chute de données.

Le Journal Vivant ressemblait à une carte.

---

Il ne remplaçait pas le terrain.

Il permettait de le parcourir.

---

Brutus sauvegarda la première version.

**LIVING JOURNAL v1.**

---

Puis il ouvrit la vue Formula Evolution.

---

F-001.

F-002.

F-003.

Des branches.

Des statuts.

Des tests.

---

Et au milieu :

CANDIDATE-0001.

---

Le premier candidat semblait minuscule.

Presque insignifiant.

---

Brutus cliqua dessus.

---

Parent :

F-021.

Mutation :

M-003.

Tests :

4.

Pass :

2.

Fail :

1.

Domain :

1.

Status :

CANDIDATE.

---

Brutus regarda.

---

Le Journal Vivant venait de rendre cette formule beaucoup plus réelle.

Pas parce qu’il l’avait rendue meilleure.

Parce qu’il lui avait donné une histoire.

---

D’autres candidats pourraient maintenant apparaître.

---

CANDIDATE-0002.

0003.

0010.

0100.

---

Ils pourraient partager des parents.

Diverger.

Se recroiser.

Se battre sur des bancs de tests.

---

Le journal pourrait raconter chaque branche.

---

Brutus sentit le prochain chapitre approcher.

---

Une bibliothèque de formules était calme.

Un arbre évolutif ne le serait pas.

---

Dès que plusieurs candidats chercheraient à occuper la même fonction, il faudrait les confronter.

---

Pas avec un vote.

Pas avec une préférence esthétique.

Avec des arènes de tests.

---

Brutus écrivit :

**FORMULA WAR.**

Puis resta devant ces deux mots.

---

La guerre n’aurait rien de violent.

Elle serait méthodique.

---

Même entrée.

Mêmes règles.

Méthodes différentes.

---

Temps.

Exactitude.

Domaine.

Robustesse.

Contre-exemples.

---

Le Journal Vivant enregistrerait tout.

---

Brutus écrivit une dernière phrase :

**LE JOURNAL N’EST PLUS L’ENDROIT OÙ LE PASSÉ EST ENTERRÉ.**

**IL EST DEVENU L’ENDROIT OÙ LE PASSÉ RESTE INTERROGEABLE.**

---

Puis il ajouta :

**ET UNE HISTOIRE QU’ON PEUT INTERROGER PEUT COMMENCER À ÉVOLUER SANS SE PERDRE.**

Il sauvegarda.

Le Journal Vivant resta ouvert.

À l’intérieur, CANDIDATE-0001 attendait.

Bientôt, il ne serait plus seul.
