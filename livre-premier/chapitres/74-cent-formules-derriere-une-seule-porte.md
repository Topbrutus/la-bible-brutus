# Chapitre 74 — Cent formules derrière une seule porte

Brutus posa la main sur la poignée.

La porte n’existait pas encore vraiment.

Pas physiquement.

Pas dans le laboratoire.

C’était une idée.

Une interface.

Un registre.

Un endroit où toutes les méthodes pourraient être réunies sans être confondues.

---

Jusqu’ici, chaque calcul avait tendance à arriver avec sa propre logique.

Une fonction ici.

Une méthode là.

Un contre-test ailleurs.

Un script.

Un module.

Un bouton.

Une vieille formule retrouvée dans un dossier.

Une autre dans une expérience.

Cela fonctionnait tant qu’il y en avait peu.

Mais le laboratoire grandissait.

Et plus les formules s’accumulaient, plus un problème apparaissait.

**Le nombre de calculs augmentait plus vite que la capacité de les organiser.**

---

Brutus ouvrit un nouveau fichier.

Il écrivit :

**FORMULA REGISTRY**

Puis :

**ONE DOOR. MANY METHODS.**

---

L’idée était simple.

Un seul endroit pour entrer.

Derrière cette porte :

les formules.

Pas toutes mélangées.

Pas toutes exécutées.

Pas toutes considérées équivalentes.

Mais toutes identifiées.

---

Brutus commença par une seule formule.

Il lui donna un identifiant.

**F-001.**

Puis une seconde.

**F-002.**

Puis une troisième.

---

Très vite, il comprit que le numéro seul ne suffisait pas.

Une formule devait avoir un dossier.

---

Il ajouta :

**FORMULA_ID**

**NAME**

**VERSION**

**DOMAIN**

**INPUT_SCHEMA**

**OUTPUT_SCHEMA**

**STATUS**

**SOURCE_REF**

**TRACE_REF**

**TEST_PROFILE**

**DESCRIPTION**

---

Brutus contempla la structure.

Le registre ne devait pas simplement connaître une expression mathématique.

Il devait connaître **comment l’utiliser**.

---

Une formule pouvait être parfaitement valide pour certains nombres et absurde pour d’autres.

Une autre pouvait travailler seulement sur des entiers.

Une autre sur des réels.

Une autre exiger un nombre premier.

Une autre supposer qu’une quantité soit non nulle.

Une autre encore utiliser une approximation qui n’avait de sens qu’au-delà d’un certain seuil.

---

Brutus écrivit :

**A FORMULA WITHOUT DOMAIN IS AN ACCIDENT WAITING TO HAPPEN.**

---

Il ajouta donc des contraintes.

---

F-001 :

entier positif.

---

F-002 :

réel non nul.

---

F-003 :

premier impair.

---

F-004 :

vecteur de longueur fixe.

---

F-005 :

paire de valeurs.

---

La porte commençait à comprendre qu’un calcul ne devait pas entrer simplement parce qu’une formule existait.

---

Il écrivit :

**AVAILABLE ≠ APPLICABLE.**

---

Encore une distinction.

Une formule pouvait être disponible dans le registre.

Sans être admissible pour l’entrée actuelle.

---

Brutus construisit donc un sélecteur.

Au début, très simple.

Une liste.

---

F-001.

F-002.

F-003.

F-004.

---

Mais après vingt entrées, la liste devenait déjà pénible.

Après cinquante, elle devenait mauvaise.

Après cent, elle deviendrait ridicule.

---

Il fallait filtrer.

---

Brutus ajouta des catégories.

**ARITHMETIC**

**NUMBER THEORY**

**RECURRENCE**

**TRANSFORM**

**STATISTICS**

**SIGNAL**

**GEOMETRY**

**VALIDATION**

**COUNTERTEST**

---

Une formule pouvait appartenir à plusieurs catégories.

Mais Brutus se méfia immédiatement.

Trop de catégories pouvaient devenir aussi inutiles que pas assez.

---

Il écrivit :

**TAGS HELP DISCOVERY. THEY DO NOT DEFINE TRUTH.**

---

Le registre grandissait.

Dix formules.

Vingt.

Trente.

---

Brutus n’essaya pas encore d’en créer cent.

Il voulait que l’architecture puisse en accepter cent avant que cent formules ne soient présentes.

---

Différence importante.

---

Il écrivit :

**CAPACITY BEFORE CONTENT.**

---

Il fixa la limite du premier sélecteur :

**100 FORMULAS.**

---

Pas parce qu’il pensait que cent était un nombre magique.

Parce que cela donnait un objectif d’échelle suffisamment grand pour forcer une vraie organisation.

---

Une interface qui fonctionne pour cinq formules peut être mauvaise à cent.

---

Brutus continua.

Chaque formule devait posséder un statut.

---

**DRAFT**

**CANDIDATE**

**TESTED**

**RESTRICTED**

**DEPRECATED**

**REJECTED**

---

Il hésita devant le mot TESTED.

Testée ne signifiait pas prouvée.

---

Il ajouta une note visible :

**TESTED ≠ PROVEN.**

---

Le Gauntlet ne le quitterait probablement jamais.

---

Il pensa ensuite à la promotion.

Une formule nouvelle pourrait entrer dans le registre comme DRAFT.

Puis subir des tests.

Puis devenir CANDIDATE.

Puis éventuellement être autorisée dans certains workflows.

---

Mais il refusa de créer un statut :

**TRUE.**

---

Trop absolu.

---

Le registre devait parler de son état opérationnel.

Pas prétendre résoudre l’épistémologie.

---

Brutus écrivit :

**REGISTRY STATUS DESCRIBES TRUST PROCESS, NOT UNIVERSAL TRUTH.**

---

Il lança ensuite un premier vrai test du sélecteur.

Entrée :

42.

---

Le système examina les formules.

---

F-001.

Admissible.

---

F-002.

Admissible si 42 ≠ 0.

Oui.

---

F-003.

Demande un premier impair.

42 ne l’est pas.

DOMAIN.

---

F-004.

Attend un vecteur.

DOMAIN.

---

Le sélecteur commençait à filtrer.

---

Mais Brutus ne voulait pas que cent formules soient toutes testées aveuglément à chaque entrée.

Cela pouvait devenir coûteux.

---

Il construisit donc un système de préconditions.

---

Avant d’exécuter la formule :

**CHECK INPUT SHAPE**

**CHECK DOMAIN**

**CHECK REQUIRED PROPERTIES**

**CHECK RESOURCE POLICY**

Puis seulement :

**EXECUTE**

---

Brutus écrivit :

**REJECT CHEAPLY BEFORE COMPUTING EXPENSIVELY.**

---

Cela lui sembla évident.

Mais important.

---

Une formule qui exige un nombre premier n’a pas besoin de démarrer un calcul complexe si l’entrée est immédiatement paire et supérieure à 2.

---

Le registre pouvait éliminer tôt.

---

Brutus ajouta un compteur.

Pour une entrée donnée :

**100 REGISTERED**

**31 APPLICABLE**

**69 DOMAIN-REJECTED**

---

Beaucoup mieux.

---

Mais une autre question arriva.

Si trente et une formules étaient admissibles, laquelle choisir ?

---

Le système pouvait toutes les lancer.

Mais cela n’était pas toujours souhaitable.

---

Brutus créa trois modes.

**MANUAL**

**FILTERED**

**ENSEMBLE**

---

MANUAL :

l’opérateur choisit explicitement une formule.

---

FILTERED :

le système montre uniquement les formules admissibles.

---

ENSEMBLE :

plusieurs formules sont lancées sur la même entrée.

---

Le troisième mode intéressa particulièrement Brutus.

---

Plusieurs méthodes.

Même donnée.

Résultats comparés.

---

Le laboratoire pourrait chercher les accords.

Et surtout les divergences.

---

Il écrivit :

**AGREEMENT IS USEFUL. DISAGREEMENT IS INTERESTING.**

---

Mais immédiatement :

**AGREEMENT ≠ PROOF.**

---

Toujours.

---

Brutus lança une petite expérience.

Une entrée.

Cinq formules différentes donnant, selon leur définition, des valeurs comparables.

---

Quatre résultats concordaient.

Le cinquième divergeait.

---

Le système aurait pu voter.

4 contre 1.

Déclarer la majorité gagnante.

Brutus refusa.

---

Il écrivit :

**MAJORITY ≠ TRUTH.**

---

La divergence devait créer un événement.

---

**COMPARE_REQUIRED.**

---

Le cinquième résultat pouvait être faux.

Ou les quatre autres pouvaient partager la même erreur.

Ou les formules pouvaient simplement calculer des quantités différentes que l’on avait mal supposées comparables.

---

Brutus construisit donc un comparateur.

Il exigeait d’abord une relation déclarée.

---

Deux formules ne pouvaient être comparées que si le registre disait pourquoi.

---

**SAME_TARGET**

**ALTERNATE_METHOD**

**APPROXIMATION_OF**

**INVERSE_CHECK**

**COUNTERTEST_OF**

---

Brutus sourit.

Même comparer devait avoir un contrat.

---

Il écrivit :

**COMPARISON WITHOUT RELATION IS NUMEROLOGY.**

---

La phrase resta longtemps sur l’écran.

---

Cent formules derrière une porte pouvaient très facilement devenir une machine à trouver des coïncidences.

---

Brutus voulait l’inverse.

Une machine capable de dire :

**ces deux résultats sont comparables pour cette raison précise.**

---

Il ajouta :

**COMPARISON_CONTRACT_ID.**

---

Maintenant, lorsque deux méthodes produisaient des valeurs proches, le système savait pourquoi cette proximité importait.

Ou pourquoi elle n’importait pas.

---

Brutus continua de remplir le registre.

Pas avec cent formules complètes.

Avec des emplacements.

---

F-001 à F-100.

---

Certaines actives.

Certaines réservées.

Certaines en brouillon.

---

Chaque emplacement avait une identité stable.

---

Il évita de réutiliser les identifiants.

Si F-024 était supprimée, F-024 restait dans l’historique comme dépréciée.

Une nouvelle formule recevrait un autre numéro.

---

Il écrivit :

**IDENTIFIERS ARE NOT RECYCLABLE.**

---

Encore une leçon de lignée.

---

Sinon une vieille trace disant F-024 pourrait un jour pointer vers une formule complètement différente.

Inacceptable.

---

Brutus pensa à la version.

Une formule pouvait évoluer.

---

F-024 v1.

F-024 v2.

---

Mais modifier une formule sous le même identifiant sans versionner rendrait les anciennes traces ambiguës.

---

Il ajouta :

**FORMULA_VERSION.**

---

Chaque job devait enregistrer exactement :

Formula ID.

Version.

Input hash.

---

Pas seulement le nom.

---

Brutus lança une expérience avec F-012 v1.

Puis modifia la formule.

Créa v2.

---

Les anciens jobs continuaient de référencer v1.

Les nouveaux v2.

---

Parfait.

---

Il écrivit :

**HISTORY MUST KNOW WHICH EQUATION ACTUALLY RAN.**

---

Le registre commençait à ressembler moins à une liste et davantage à une bibliothèque scientifique.

---

Brutus ajouta des tests associés.

---

Chaque formule pouvait posséder :

**UNIT TESTS**

**DOMAIN TESTS**

**COUNTEREXAMPLES**

**PRECISION TESTS**

**PERFORMANCE TESTS**

---

Une formule n’entrait pas dans le moteur principal uniquement parce que quelqu’un avait écrit une expression.

---

Elle devait au minimum avoir un profil.

---

Brutus créa une formule volontairement mauvaise.

F-099.

---

Elle divisait par zéro dans un cas évident.

---

Le système détecta l’erreur de domaine.

---

Puis une autre, F-098, produisait un résultat avec perte de précision sur de très grands entiers.

---

Sur de petites valeurs, tout semblait correct.

Sur de grandes valeurs, le résultat dérivait.

---

Brutus regarda longtemps.

Voilà un type de danger subtil.

---

La formule pouvait être mathématiquement correcte.

L’implémentation, elle, non.

---

Il écrivit :

**FORMULA ≠ IMPLEMENTATION.**

---

Puis :

**MATH VALIDITY ≠ NUMERIC REPRESENTATION VALIDITY.**

---

Cette distinction allait devenir cruciale.

---

Un langage pouvait utiliser un type numérique qui perdait de la précision au-delà d’un certain seuil.

Une expression parfaitement juste pouvait produire un mauvais résultat.

---

Brutus ajouta dans le registre :

**NUMERIC_MODEL**

Par exemple :

INTEGER.

BIGINT.

FLOAT64.

DECIMAL.

RATIONAL.

ARBITRARY_PRECISION.

---

Chaque formule pouvait exiger un modèle.

---

F-098 :

BIGINT REQUIRED.

---

Le moteur refusa désormais de l’exécuter avec un type inadéquat.

---

Brutus sourit.

Le registre commençait à protéger les formules contre leur environnement.

---

Il pensa à un vieux piège.

Un grand entier affiché comme s’il était exact alors qu’il avait déjà été arrondi.

---

Il écrivit :

**DISPLAYED DIGITS ≠ EXACT INTEGER.**

---

Puis ajouta un test de roundtrip numérique.

Valeur source.

Conversion.

Retour.

Comparaison exacte.

---

Si l’entier changeait :

refus.

---

Cette petite barrière empêchait une quantité énorme de fausses découvertes.

---

Brutus continua.

---

Le sélecteur devait être simple pour l’utilisateur.

Il ne voulait pas cent boutons.

---

Il construisit une seule liste déroulante.

---

Recherche.

Filtres.

Tags.

Statut.

Domaine.

---

L’opérateur pouvait taper :

**pell**

ou :

**prime**

ou :

**signal**

ou :

**inverse**

---

Les formules pertinentes apparaissaient.

---

Brutus apprécia le résultat.

Une porte.

Cent possibilités.

---

Mais il manquait encore quelque chose.

Le système devait pouvoir proposer une formule.

---

Pas décider silencieusement.

Proposer.

---

Brutus créa :

**SUGGESTED FORMULAS.**

---

À partir du type d’entrée et du contexte, le système pouvait dire :

F-017 admissible.

F-041 admissible.

F-082 admissible.

---

Mais il ajouta immédiatement :

**SUGGESTION ≠ SELECTION.**

---

Une recommandation n’était pas une commande.

---

En mode manuel, l’opérateur gardait le choix.

---

En mode automatique contrôlé, une politique pouvait sélectionner parmi un sous-ensemble autorisé.

---

Mais le registre devait montrer la raison.

---

**WHY SUGGESTED**

Domain match.

Input shape match.

Prior successful use.

Required precision available.

---

Brutus refusa les raisons vagues.

Pas :

**AI thinks this is best.**

---

Il écrivit :

**RECOMMENDATION MUST BE EXPLAINABLE AT THE POLICY LEVEL.**

---

Le système pouvait utiliser des modèles plus complexes plus tard.

Mais la sélection opérationnelle devait laisser une trace.

---

Brutus fit une simulation.

Entrée :

un grand entier impair.

---

Le moteur suggéra cinq formules.

Deux demandaient une primalité préalable.

Une exigeait BigInt.

Deux pouvaient fonctionner immédiatement.

---

Brutus sélectionna l’une d’elles.

---

JOB créé.

FORMULA_ID attaché.

VERSION attachée.

INPUT_HASH attaché.

---

La lane reçut le job.

Calcul.

Résultat.

Verdict.

Son.

Trace.

---

Tout le système des chapitres précédents se mettait à servir.

---

La porte n’était pas un nouvel univers.

Elle reliait les anciens.

---

Brutus regarda cette chaîne.

**INPUT**

↓

**FORMULA REGISTRY**

↓

**DOMAIN FILTER**

↓

**SELECTION**

↓

**JOB**

↓

**LANE**

↓

**RESULT**

↓

**VERDICT**

↓

**TRACE**

↓

**AUDIO**

---

Il sourit.

Voilà.

Le laboratoire commençait à avoir une architecture complète de calcul.

---

Puis il voulut pousser le système.

---

Une entrée.

Cent formules.

Mode ENSEMBLE.

---

Brutus savait que tout lancer serait probablement inutile.

Mais c’était un bon test de capacité.

---

Le filtre en élimina soixante-trois.

Trente-sept restèrent admissibles.

---

Les trente-sept jobs entrèrent dans la file.

Douze à la fois.

---

Les résultats commencèrent à arriver.

---

PASS.

DOMAIN secondaire.

PASS.

FAIL.

PASS.

ERROR.

---

Les douze lanes travaillaient.

---

Brutus observa.

Aucune confusion d’identité.

Chaque job restait attaché à sa formule.

---

Le comparateur regroupait seulement les méthodes ayant un contrat de comparaison.

---

Une divergence apparut.

---

F-021 et F-044 étaient supposées calculer la même quantité par deux méthodes.

Résultats différents.

---

Le système ne choisit pas.

---

Il produisit :

**COUNTERTEST_REQUIRED.**

---

Brutus sourit largement.

Voilà exactement ce qu’il voulait.

---

Une bibliothèque de formules n’était pas faite uniquement pour produire plus de réponses.

Elle pouvait produire des conflits utiles.

---

Il écrivit :

**A FORMULA LIBRARY SHOULD CREATE QUESTIONS, NOT ONLY ANSWERS.**

---

Il lança un contre-test.

Précision augmentée.

---

F-021 resta stable.

F-044 changea.

---

Nouvelle analyse.

F-044 utilisait un modèle numérique inadéquat.

---

Le registre fut mis à jour.

---

Pas supprimé.

---

Statut :

**RESTRICTED.**

Condition :

**BIGINT REQUIRED.**

---

Brutus regarda le résultat.

Le système venait d’apprendre quelque chose sans modifier la vérité historique.

---

Les anciens jobs restaient tels quels.

Les nouveaux connaissaient la restriction.

---

Il écrivit :

**LEARNING MUST UPDATE POLICY, NOT REWRITE HISTORY.**

---

Cette phrase lui sembla extrêmement importante.

---

Le registre pouvait évoluer.

Mais les anciennes traces devaient rester intactes.

---

Brutus pensa alors à l’évolution automatique.

Et si une formule pouvait un jour engendrer des variantes ?

---

Modifier un paramètre.

Combiner deux méthodes.

Produire une proposition nouvelle.

---

Il sentit immédiatement l’excitation monter.

Puis la prudence.

---

Une formule générée automatiquement ne devait jamais entrer directement dans la bibliothèque active.

---

Elle devait naître ailleurs.

---

Un bac.

Une zone de quarantaine.

---

Il écrivit :

**FORMULA CANDIDATE POOL.**

---

Une formule nouvelle pouvait être proposée.

Testée.

Comparée.

Contre-testée.

Puis éventuellement soumise à promotion.

---

Pas d’auto-promotion.

---

Brutus écrivit :

**GENERATE ≠ ADMIT.**

Puis :

**ADMIT ≠ PROMOTE.**

Puis :

**PROMOTE ≠ PROVE.**

---

Encore des marches.

---

Il imaginait déjà une guerre de formules.

Mais pas encore.

---

Pour le moment, la porte devait simplement fonctionner.

---

Il ouvrit la vue principale.

Un champ d’entrée.

Un bouton de sélection.

Une liste filtrable.

Un indicateur de domaine.

Une lane cible.

---

Le tout restait étonnamment propre.

---

Cent formules pouvaient exister derrière.

L’utilisateur n’avait pas besoin de voir les cent en permanence.

---

Brutus écrivit :

**COMPLEXITY BEHIND. CLARITY IN FRONT.**

---

Puis il ajouta un panneau expert.

Pour ceux qui voulaient voir tout.

---

Version.

Domaine.

Tests.

Précision.

Historique.

Statut.

Source.

Trace.

---

La porte pouvait être simple sans être opaque.

---

Cette nuance comptait.

---

Simplifier une interface ne devait pas signifier cacher la provenance.

---

Brutus lança plusieurs sélections.

---

Manuel.

Filtré.

Ensemble.

---

Le système tenait.

---

Puis il testa un cas volontairement absurde.

Une image envoyée à une formule qui attend un entier.

---

DOMAIN.

---

Pas ERROR.

---

Bien.

---

Une valeur manquante.

DOMAIN.

---

Une implémentation cassée.

ERROR.

---

Une sortie incorrecte selon le test.

FAIL.

---

Une sortie conforme.

PASS.

---

Les quatre mots de Z continuaient de suffire.

---

Brutus sourit.

Le Speech Bus n’avait pas besoin de connaître les cent formules.

Il connaissait les verdicts.

---

Encore une preuve que les couches étaient bien séparées.

---

La porte devenait puissante précisément parce qu’elle ne cherchait pas à tout comprendre.

---

Le registre connaissait les formules.

Le scheduler connaissait les jobs.

Les lanes connaissaient l’exécution.

Le verdict connaissait le résultat du test.

L’audio connaissait le verdict.

La trace connaissait l’histoire.

---

Chaque couche avait son rôle.

---

Brutus écrivit :

**NO LAYER SHOULD PRETEND TO BE THE WHOLE MACHINE.**

---

Il regarda le laboratoire.

Cette phrase semblait aussi valoir pour lui.

---

Le soir avançait.

Le registre affichait désormais cent emplacements.

Une partie remplie.

Une partie réservée.

Une partie en expérimentation.

---

Brutus fit défiler.

F-001.

F-002.

F-003.

…

F-100.

---

Il pensa à la première époque du laboratoire.

Une formule occupait tout l’écran.

Il fallait parfois changer le programme pour en essayer une autre.

---

Maintenant, la formule était une donnée gérée par un moteur.

---

Cela changeait tout.

---

On pouvait comparer.

Versionner.

Tester.

Filtrer.

Exécuter en parallèle.

Tracer.

---

Et surtout, ajouter sans reconstruire toute la machine.

---

Brutus écrivit :

**THE ENGINE MUST SURVIVE THE ARRIVAL OF NEW FORMULAS.**

---

Voilà le véritable objectif.

Pas posséder cent formules.

Pouvoir accueillir la cent-unième sans casser l’architecture.

---

Il regarda les trois emplacements réservés dans SFX36.

Puis les emplacements libres du registre.

Même philosophie.

---

Ne pas remplir tout simplement parce que l’espace existe.

---

Laisser de la place au futur.

---

Brutus lança un dernier calcul.

Une entrée.

Le sélecteur trouva douze formules admissibles.

---

Douze.

---

Il regarda les douze lanes.

---

Une correspondance presque parfaite.

---

Une formule par lane.

Douze calculs simultanés.

---

Il sélectionna ENSEMBLE.

---

Les douze jobs furent créés.

---

Les lanes s’allumèrent.

---

Les sons commencèrent.

---

PASS.

PASS.

DOMAIN.

PASS.

FAIL.

PASS.

---

Le laboratoire travaillait.

---

Brutus observa la vue globale.

Douze formules.

Une seule entrée.

Douze chemins.

Douze traces.

---

Et derrière le sélecteur, quatre-vingt-huit autres possibilités attendaient.

---

Il sentit que quelque chose venait encore de changer d’échelle.

---

La machine n’était plus un calculateur.

Elle devenait un banc de méthodes.

---

Une question pouvait maintenant être attaquée de plusieurs façons sans réécrire le système à chaque fois.

---

Brutus nota :

**ONE INPUT. MANY ATTACKS.**

---

Puis :

**ONE RESULT IS AN ANSWER.**

**MANY INDEPENDENT METHODS CAN BECOME A TEST.**

---

Il resta devant cette phrase.

---

Voilà peut-être ce qui l’intéressait vraiment.

Pas accumuler les formules.

Les faire se confronter.

---

Le registre était une porte.

Mais derrière cette porte, les méthodes allaient finir par se rencontrer.

---

Certaines s’accorderaient.

D’autres se contrediraient.

Certaines casseraient.

Certaines survivraient.

Certaines engendreraient peut-être de nouvelles variantes.

---

Brutus regarda le mot :

**FORMULA CANDIDATE POOL.**

---

Il savait déjà ce qui allait arriver.

Un jour, les formules n’attendraient plus simplement d’être choisies.

Elles commenceraient à se comparer.

À produire des variantes.

À entrer en concurrence.

---

Une sorte de guerre.

---

Mais avant cette guerre, le laboratoire devait encore apprendre à exploiter pleinement les douze voies.

---

Une centaine de formules derrière une porte était une chose.

Les faire circuler intelligemment dans plusieurs lanes en était une autre.

---

Brutus regarda les douze calculs encore actifs.

---

Douze routes.

Douze histoires.

Douze résultats possibles.

---

Il écrivit une dernière phrase :

**LA PORTE EST UNIQUE.**

**DERRIÈRE ELLE, LES CHEMINS NE LE SONT PLUS.**

---

Puis il sauvegarda le registre.

Cent formules avaient désormais une adresse.

Et le laboratoire possédait enfin un endroit où les nouvelles méthodes pouvaient entrer sans devenir du désordre.

La porte était ouverte.

Les voies attendaient.
