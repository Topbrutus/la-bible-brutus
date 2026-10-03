# Chapitre 75 — Douze voies en parallèle

Les voies attendaient.

Douze colonnes.

Douze espaces d’exécution.

Douze chemins capables de recevoir un calcul.

Brutus les regarda comme on regarde une autoroute avant l’ouverture.

Tout semblait propre.

Calme.

Presque trop calme.

---

Une seule formule entra dans LANE 1.

Puis une seconde dans LANE 2.

Une troisième dans LANE 3.

Jusqu’à douze.

---

Les colonnes commencèrent à vivre.

Chaque lane affichait :

**JOB_ID**

**FORMULA_ID**

**INPUT_REF**

**STATE**

**START_TICK**

**LATEST_EVENT**

---

Brutus observa.

Tout fonctionnait.

Mais il savait que ce test était trop gentil.

Douze calculs indépendants ne constituent pas encore un système parallèle solide.

Ils constituent simplement douze calculs simultanés.

---

Il écrivit :

**PARALLEL ≠ COORDINATED.**

---

Le mot coordination allait devenir le vrai problème.

---

Brutus choisit une seule entrée.

Un nombre.

Puis demanda au registre de sélectionner douze formules admissibles.

Une formule par lane.

---

La même entrée entra donc dans douze méthodes différentes.

---

LANE 1 :

F-003.

LANE 2 :

F-011.

LANE 3 :

F-017.

LANE 4 :

F-024.

Et ainsi de suite.

---

Douze attaques.

Une question.

---

Brutus lança.

---

Les lanes s’allumèrent presque ensemble.

---

Certaines formules terminèrent immédiatement.

D’autres prirent davantage de temps.

Certaines produisirent PASS.

Une DOMAIN.

Une FAIL.

---

Les sons de SFX36 apparurent dans la pièce.

---

Brutus regarda la vue globale.

La première tentation était évidente.

Faire un compteur.

PASS : 9.

FAIL : 1.

DOMAIN : 1.

RUNNING : 1.

---

Il ajouta le compteur.

Puis s’arrêta.

Un nombre agrégé pouvait être utile.

Mais il pouvait aussi être trompeur.

---

Neuf PASS ne signifiaient pas nécessairement neuf confirmations indépendantes.

Deux formules pouvaient partager le même algorithme sous des noms différents.

Trois pouvaient dépendre de la même approximation.

Deux pouvaient utiliser le même code.

---

Brutus écrivit :

**METHOD COUNT ≠ INDEPENDENCE COUNT.**

---

Cela compliquait immédiatement les choses.

---

Si le laboratoire voulait utiliser plusieurs méthodes comme contre-test, il devait savoir quelque chose sur leur parenté.

---

Il retourna au FORMULA REGISTRY.

Ajouta :

**METHOD_FAMILY**

**IMPLEMENTATION_FAMILY**

**DEPENDENCY_REF**

**DERIVED_FROM**

---

F-003 et F-017 pouvaient être mathématiquement différentes mais utiliser la même bibliothèque.

F-024 pouvait être une réécriture directe de F-003.

F-041 pouvait offrir une méthode réellement indépendante.

---

Brutus regarda les douze résultats.

Le nombre brut de PASS venait de perdre un peu de sa force.

---

Il créa un second résumé.

**12 RUNS**

**9 PASS**

**5 DISTINCT METHOD FAMILIES**

---

Mieux.

---

Puis il ajouta :

**3 INDEPENDENT IMPLEMENTATION FAMILIES**

Encore mieux.

---

Il écrivit :

**DIVERSITY MUST BE MEASURED, NOT ASSUMED.**

---

Le parallèle n’était pas seulement une question de vitesse.

Il pouvait devenir un instrument épistémique.

Mais seulement si les voies n’étaient pas de simples copies les unes des autres.

---

Brutus lança une autre expérience.

Cette fois, les douze lanes reçurent douze entrées différentes avec la même formule.

---

Même formule.

Douze données.

---

Le système fonctionna.

Mais maintenant, une autre distinction apparaissait.

---

Mode A :

**ONE INPUT → MANY FORMULAS**

Mode B :

**MANY INPUTS → ONE FORMULA**

Puis Brutus écrivit :

Mode C :

**MANY INPUTS → MANY FORMULAS**

---

Voilà le vrai danger.

---

Cent formules.

Douze lanes.

Des centaines d’entrées.

Le nombre de combinaisons pouvait exploser.

---

Brutus écrivit :

**DO NOT CONFUSE CAPACITY WITH REQUIREMENT.**

Le fait de pouvoir lancer beaucoup de calculs ne signifiait pas qu’il fallait tout calculer.

---

Il construisit donc un planificateur.

---

Le scheduler connaissait maintenant :

la formule,

le coût approximatif,

le domaine,

la lane disponible,

la priorité,

la mémoire nécessaire,

la précision demandée.

---

Brutus ajouta :

**COST_PROFILE.**

---

Une formule légère ne devait pas attendre derrière une opération énorme si une autre lane était libre.

---

Mais il ne voulait pas non plus qu’un seul calcul lourd monopolise toute la machine.

---

Il créa :

**RESOURCE_BUDGET.**

---

CPU.

Mémoire.

Temps maximal.

Taille d’entrée.

---

Chaque job recevait un budget.

---

Brutus écrivit :

**JOB AUTHORIZATION INCLUDES RESOURCE SCOPE.**

---

Encore la même idée que pour les fourmis.

Une autorisation ne devait jamais être infinie.

---

Un calcul autorisé pouvait consommer jusqu’à une certaine quantité.

Au-delà :

pause,

timeout,

ou refus.

---

Brutus testa un job volontairement énorme.

Il entra dans LANE 4.

Sa consommation grimpa.

---

Le scheduler observa.

---

Lorsque le budget fut atteint, le job passa :

**RESOURCE_LIMIT.**

Pas FAIL.

Pas ERROR.

---

Brutus sourit.

Encore une nuance.

---

Il ajouta à son vocabulaire opérationnel :

**RESOURCE_LIMIT ≠ MATHEMATICAL FAILURE.**

---

La formule pouvait être correcte.

Le laboratoire avait simplement refusé de lui donner davantage de ressources.

---

Cette distinction devait rester dans la trace.

---

Il lança ensuite deux jobs lourds en même temps.

Puis quatre.

Puis douze.

---

La machine ralentit.

Pas de catastrophe.

Mais la latence augmenta partout.

---

Brutus comprit que « douze voies » ne signifiait pas nécessairement douze calculs lourds simultanés.

---

Les lanes étaient logiques.

Les ressources physiques restaient limitées.

---

Il écrivit :

**LOGICAL PARALLELISM ≠ PHYSICAL PARALLELISM.**

---

Important.

---

Douze lanes pouvaient représenter douze travaux actifs ou en attente, même si le processeur n’exécutait réellement qu’une partie d’entre eux au même instant.

---

Brutus ajouta un état :

**READY**

en plus de :

**RUNNING.**

---

READY signifiait :

le job est admissible et attend une ressource.

---

Cela rendait le scheduler beaucoup plus honnête.

---

Brutus afficha :

LANE 1 : RUNNING.

LANE 2 : RUNNING.

LANE 3 : READY.

LANE 4 : RUNNING.

LANE 5 : READY.

---

L’interface ne prétendait plus que tout tournait réellement en parallèle.

---

Il écrivit :

**SHOW SCHEDULING STATE, NOT PERFORMANCE THEATER.**

---

Cette phrase rejoignait NO FAKE MOTION.

---

Ne pas dessiner douze roues en train de tourner simplement parce que douze jobs existaient.

---

Seulement les jobs réellement exécutés pouvaient montrer une activité.

---

Brutus testa le rendu.

Trois lanes calculaient.

Les autres attendaient.

---

Visuellement, seules trois bougeaient.

---

Parfait.

---

Puis le scheduler libéra une ressource.

LANE 3 passa de READY à RUNNING.

Son activité démarra.

---

Le visuel suivit l’état.

Pas l’inverse.

---

Brutus commençait à aimer cette machine.

Elle devenait de plus en plus difficile à faire mentir.

---

Il ajouta ensuite une fonction importante :

**CANCEL.**

---

Un job long pouvait être interrompu.

Mais l’annulation elle-même devait être propre.

---

CANCEL_REQUESTED.

Puis :

CANCEL_CONFIRMED.

---

Pas simplement disparition.

---

Brutus écrivit :

**REQUESTED CANCEL ≠ CANCELLED.**

---

Encore.

---

Il lança un calcul long.

Clique CANCEL.

---

Pendant quelques ticks, le job continuait.

---

Puis le worker confirma l’arrêt.

---

État final :

CANCELLED.

---

Trace complète.

---

Brutus apprécia.

---

La machine savait désormais dire :

« j’essaie de l’arrêter »

puis :

« il est réellement arrêté ».

---

Cette distinction serait importante plus tard pour beaucoup d’autres actions.

---

Brutus continua à pousser.

Il lança douze jobs utilisant la même grosse table intermédiaire.

---

Chaque job recalculait la même chose.

Gaspillage.

---

Il pensa à utiliser un cache partagé.

Puis hésita.

Un cache pouvait accélérer.

Mais il pouvait aussi contaminer l’indépendance des méthodes.

---

Si deux contre-tests utilisaient la même valeur pré-calculée erronée, leurs résultats pourraient s’accorder artificiellement.

---

Brutus écrivit :

**SHARED CACHE CAN CREATE SHARED FAILURE.**

---

Il ne voulait pas interdire les caches.

Mais leur utilisation devait être visible.

---

Il ajouta :

**CACHE_REF**

et :

**CACHE_POLICY.**

---

Pour un mode performance :

cache autorisé.

---

Pour un mode contre-test indépendant :

cache partagé interdit.

---

Brutus nomma les deux politiques.

**FAST MODE**

et

**INDEPENDENT MODE**

---

Puis il écrivit :

**SPEED AND INDEPENDENCE ARE DIFFERENT OPTIMIZATION TARGETS.**

---

Le laboratoire devenait un véritable banc d’essai.

---

En FAST MODE, plusieurs lanes pouvaient partager des calculs intermédiaires.

En INDEPENDENT MODE, les familles de méthodes devaient reconstruire leurs propres étapes critiques.

---

Plus lent.

Mais plus utile pour chercher une erreur commune.

---

Brutus lança les douze formules dans les deux modes.

---

FAST :

beaucoup plus rapide.

---

INDEPENDENT :

plus lent.

Mais la structure de dépendance était plus propre.

---

Il regarda les résultats.

Ils concordaient.

---

Il nota seulement :

**NO DIVERGENCE OBSERVED.**

Pas :

**CONFIRMED TRUE.**

---

La discipline ne disparaissait jamais.

---

Brutus pensa ensuite aux erreurs dans une lane.

Que devait-il se passer si LANE 7 plantait ?

---

Les onze autres devaient-elles s’arrêter ?

Pas forcément.

---

Il décida que l’isolation serait la règle par défaut.

---

**ONE LANE FAILURE MUST NOT KILL OTHER INDEPENDENT LANES.**

---

Il simula une exception.

LANE 7 passa ERROR.

---

Les autres continuèrent.

---

Le scheduler récupéra la lane après nettoyage.

---

Brutus vérifia une chose importante.

L’ancien JOB_ID ne devait jamais rester attaché à la lane réutilisée.

---

Il trouva justement un petit bug.

La vue affichait brièvement le nouvel état avec l’ancien identifiant.

---

Brutus arrêta tout.

---

Une fraction de seconde.

Mais inacceptable.

---

Il écrivit :

**LANE IS NOT JOB IDENTITY.**

---

Exactement comme l’écran n’était pas l’identité de la fenêtre.

---

Une lane était une ressource.

Pas le travail lui-même.

---

Le job devait pouvoir migrer.

Une lane devait pouvoir être réutilisée.

---

Il corrigea la vue.

Avant d’afficher un nouveau job :

clear association.

bind new JOB_ID.

verify generation.

render.

---

Le fantôme disparut.

---

Brutus sourit.

Les vieux principes revenaient toujours.

---

**POSITION ≠ IDENTITY.**

---

Une fenêtre pouvait changer d’écran.

Une fourmi de position.

Un job de lane.

---

La machine devenait cohérente précisément parce que les mêmes lois s’appliquaient partout.

---

Brutus alla plus loin.

Et si un job devait changer de lane pendant son exécution ?

---

Possible en théorie.

Mais plus difficile.

---

Il décida de ne pas autoriser la migration d’un job RUNNING pour la première version.

---

Un job pouvait être déplacé tant qu’il était READY.

Une fois RUNNING :

lane verrouillée jusqu’à fin, pause ou annulation.

---

Il écrivit :

**MIGRATION POLICY MUST BE EXPLICIT.**

---

Pas besoin de résoudre tous les problèmes d’un coup.

---

Brutus lança ensuite un test de pression.

---

1 000 jobs.

---

Cent formules possibles.

Plusieurs entrées.

Douze lanes.

---

La file se remplit.

---

Il surveilla surtout :

duplications,

pertes,

jobs sans résultat,

résultats sans job,

ordre,

mémoire.

---

Le traitement prit du temps.

---

Brutus n’essayait pas d’être rapide.

Il cherchait les trous.

---

À la fin :

SUBMITTED : 1000.

TERMINAL STATES : 1000.

UNMATCHED : 0.

DUPLICATE JOB_ID : 0.

LOST TRACE : 0.

---

Il regarda longtemps.

---

C’était plus important qu’un benchmark.

---

Le système avait conservé les identités sous pression.

---

Il écrivit :

**LOAD TEST PASSED FOR IDENTITY CONSERVATION UNDER THIS RUN.**

---

Pas simplement :

**SYSTEM STABLE.**

Encore trop général.

---

Il voulait toujours dire exactement ce que le test avait observé.

---

Puis il choisit un job au hasard parmi les mille.

---

JOB-0742.

---

Trace.

Formule.

Version.

Input.

Lane initiale.

Scheduler events.

Start tick.

End tick.

Result.

Verdict.

Audio event.

---

Tout était là.

---

Une aiguille dans une botte de foin.

Retrouvée sans ambiguïté.

---

Brutus sourit largement.

---

Voilà la puissance des identifiants.

---

Il retourna à l’interface.

Les douze lanes étaient désormais de véritables instruments.

---

Pas simplement des rectangles.

Chacune pouvait afficher :

job courant,

file associée,

coût,

progression lorsqu’elle était mesurable,

dernier événement,

état source.

---

Brutus fit attention au mot progression.

Tous les calculs ne savaient pas dire combien de travail restait.

---

Une barre arbitraire serait mensongère.

---

Il écrivit :

**UNKNOWN PROGRESS MUST LOOK UNKNOWN.**

---

Pour certaines formules :

43 %.

Mesurable.

---

Pour d’autres :

RUNNING.

Sans pourcentage.

---

Parfait.

---

Une roue pouvait tourner pour indiquer qu’un processus était actif.

Mais elle ne devait pas prétendre connaître la fraction accomplie.

---

Brutus ajouta :

**ACTIVITY ≠ PROGRESS.**

---

Encore une distinction.

---

Il réfléchit ensuite à la manière d’utiliser les douze voies scientifiquement.

---

Elles pouvaient servir à accélérer.

Mais aussi à organiser un protocole.

---

Par exemple :

LANE 1 :

méthode principale.

LANE 2 :

calcul haute précision.

LANE 3 :

méthode alternative.

LANE 4 :

test de domaine.

LANE 5 :

contre-exemple.

LANE 6 :

test aléatoire.

LANE 7 :

version BigInt.

LANE 8 :

version rationnelle.

LANE 9 :

approximation.

LANE 10 :

inverse check.

LANE 11 :

historical comparison.

LANE 12 :

reserved challenger.

---

Brutus regarda cette organisation.

Intéressante.

Mais il se rappela le piège des écrans spécialisés.

---

Il ne voulait pas que LANE 1 devienne éternellement « principale ».

---

Les rôles devaient être assignés par expérience.

---

Il écrivit :

**LANE ROLE IS SESSION STATE, NOT LANE IDENTITY.**

---

Encore une fois.

---

Une expérience pouvait décider :

LANE 4 = countertest.

La suivante :

LANE 4 = high precision.

---

La lane restait une lane.

---

Brutus commença à voir le système comme une table de laboratoire réellement adaptable.

---

Douze emplacements.

Chaque expérience choisissait comment les utiliser.

---

Il créa un objet :

**EXPERIMENT_PLAN.**

---

Ce plan contenait :

les jobs,

les formules,

les lanes préférées,

les dépendances,

la politique de cache,

la précision,

les critères d’arrêt.

---

Brutus sourit.

Voilà.

L’expérience elle-même devenait un objet.

---

Pas seulement une série de clics.

---

Il ajouta :

**EXPERIMENT_ID.**

Puis :

**PLAN_VERSION.**

---

Le plan pouvait être sauvegardé.

Relancé.

Comparé.

---

Mais il ajouta immédiatement :

**REPLAY ≠ SAME ENVIRONMENT.**

---

Relancer un plan plus tard pouvait produire des conditions différentes.

Version de code.

Matériel.

Données externes.

---

La trace devait donc enregistrer l’environnement pertinent.

---

Brutus ajouta :

**RUNTIME_PROFILE_REF.**

---

Cela devenait sérieux.

---

Une expérience ne serait plus seulement :

« j’ai lancé douze calculs ».

---

Elle deviendrait :

voici le plan,

voici les versions,

voici les entrées,

voici les ressources,

voici l’ordre,

voici les résultats.

---

Une véritable capsule reproductible.

---

Brutus pensa au chapitre 70.

La trace qui revient entière.

Maintenant, la trace pouvait englober une expérience parallèle entière.

---

Douze lignées.

Un plan commun.

---

Il écrivit :

**PARALLEL TRACE = MANY LINEAGES + ONE EXPERIMENT CONTEXT.**

---

La formule lui plut.

---

Il lança une dernière expérience.

---

Douze lanes.

Douze méthodes.

Une entrée.

Mode indépendant.

Pas de cache critique partagé.

Précision élevée.

---

Le système démarra.

---

Les résultats arrivèrent.

---

Onze méthodes concordaient dans leur relation attendue.

Une divergea.

---

Brutus entendit FAIL.

---

LANE 9.

---

Il ouvrit la trace.

---

Pas de panique.

Pas de verdict global.

---

Il inspecta.

---

La formule de LANE 9 utilisait une approximation.

La valeur se trouvait près d’une zone où cette approximation devenait mauvaise.

---

DOMAIN ?

Non.

La formule restait définie.

---

ERROR ?

Non.

L’exécution avait réussi.

---

FAIL ?

Oui, pour le contrat de comparaison actuel.

---

Brutus sourit.

Parfait.

---

La divergence n’était pas une panne.

Elle révélait la limite d’une méthode.

---

Le registre fut mis à jour avec une note.

---

**KNOWN ACCURACY LIMIT IN REGION X.**

---

Pas de suppression.

Pas de honte.

Une information.

---

Brutus écrivit :

**A FORMULA THAT FAILS IN A KNOWN REGION MAY STILL BE USEFUL ELSEWHERE.**

---

Le laboratoire apprenait à ne pas jeter une méthode simplement parce qu’elle avait des limites.

---

Les limites faisaient partie de l’identité opérationnelle.

---

Le soir était bien avancé.

---

Brutus arrêta le plan.

Les lanes s’éteignirent une à une.

---

LANE 12.

Idle.

LANE 11.

Idle.

LANE 10.

Idle.

---

Jusqu’à LANE 1.

---

Silence.

---

Il regarda les douze colonnes vides.

---

Elles semblaient désormais beaucoup plus puissantes qu’au début.

Pas parce qu’elles pouvaient tourner en même temps.

Parce qu’elles pouvaient tourner **sans perdre qui faisait quoi**.

---

Brutus écrivit :

**LE PARALLÈLE NE VAUT RIEN SANS IDENTITÉ.**

Puis :

**L’IDENTITÉ NE VAUT RIEN SANS TRACE.**

Puis :

**LA TRACE NE VAUT RIEN SI LES MÉTHODES NE PEUVENT PAS ÊTRE COMPARÉES PROPREMENT.**

---

Il resta devant les trois phrases.

---

Le prochain problème était déjà là.

---

Les formules étaient maintenant nombreuses.

Les lanes pouvaient les exécuter.

Les comparateurs pouvaient repérer des divergences.

---

Mais qu’allait-il se passer lorsqu’une formule commencerait à produire une variante d’elle-même ?

---

Une méthode pourrait générer un candidat.

Une autre le tester.

Une autre le battre.

Une autre le modifier.

---

Le registre pourrait cesser d’être une bibliothèque passive.

---

Il pourrait devenir un écosystème.

---

Brutus ouvrit :

**FORMULA CANDIDATE POOL.**

---

La zone était encore presque vide.

---

Il ajouta un premier emplacement.

---

**CANDIDATE-0001.**

---

Puis écrivit :

**PARENT_FORMULA_REF**

**MUTATION_REF**

**TEST_STATUS**

**COUNTERTEST_STATUS**

---

Il s’arrêta.

---

La guerre n’avait pas commencé.

Mais les armes étaient désormais sur la table.

---

Cent formules.

Douze voies.

Un registre.

Un scheduler.

Un comparateur.

Une trace.

---

Il ne manquait plus qu’une chose pour que les méthodes commencent réellement à se confronter :

un journal capable de raconter leurs transformations au fil du temps.

---

Brutus regarda les traces accumulées.

Des milliers de lignes.

Des jobs.

Des verdicts.

Des comparaisons.

---

Le laboratoire savait enregistrer.

Mais il ne savait pas encore vraiment **raconter sa propre évolution**.

---

Il écrivit un nouveau titre :

**JOURNAL VIVANT.**

Puis sauvegarda.

Les douze voies étaient silencieuses.

Mais derrière elles, l’histoire de la machine venait de devenir trop riche pour rester une simple liste de logs.
