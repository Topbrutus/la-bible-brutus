# Chapitre 77 — La guerre des formules

Bientôt, CANDIDATE-0001 ne serait plus seul.

Brutus n’eut pas à attendre longtemps.

Le lendemain, le pool contenait déjà trois nouveaux candidats.

---

**CANDIDATE-0002**

Parent :

F-021.

Mutation :

M-007.

---

**CANDIDATE-0003**

Parent :

F-044.

Mutation :

M-002.

---

**CANDIDATE-0004**

Parents :

F-021 + F-041.

Type :

HYBRID.

---

Brutus regarda les quatre lignes.

Pour la première fois, plusieurs formules prétendaient pouvoir remplir une fonction comparable.

Pas nécessairement avec la même méthode.

Pas avec la même architecture.

Mais avec un objectif suffisamment proche pour justifier une confrontation.

---

Il écrivit :

**FORMULA WAR.**

Puis resta devant le titre.

Le mot guerre était brutal.

Mais il décrivait bien une chose.

Les méthodes allaient être placées dans les mêmes conditions.

Certaines résisteraient mieux.

D’autres moins bien.

---

Brutus ajouta immédiatement :

**WAR = CONTROLLED COMPARISON.**

Puis :

**NOT DESTRUCTION.**

Une formule qui perdait une comparaison ne devait pas disparaître.

Elle devait conserver son histoire.

---

Brutus construisit la première arène.

Il l’appela :

**ARENA-0001.**

---

L’arène n’était pas une lane.

Elle utilisait les lanes.

Elle n’était pas une formule.

Elle testait les formules.

Elle n’était pas un verdict.

Elle produisait des observations à partir desquelles plusieurs verdicts limités pouvaient être établis.

---

Brutus écrivit :

**ARENA ≠ JUDGE.**

Voilà.

---

Une arène définissait les conditions.

Pas la vérité.

---

Il lui donna un contrat.

**ARENA_ID**

**TARGET_RELATION**

**INPUT_SET_REF**

**FORMULA_SET**

**NUMERIC_MODEL**

**PRECISION_POLICY**

**RESOURCE_POLICY**

**CACHE_POLICY**

**STOP_POLICY**

**COMPARISON_METRICS**

**TRACE_REF**

---

Brutus regarda le contrat.

S’il voulait confronter plusieurs méthodes, elles devaient recevoir le même terrain.

---

Il écrivit :

**SAME QUESTION. SAME RULES. DIFFERENT METHODS.**

---

Mais là encore, « mêmes règles » demandait une définition.

Certaines formules exigeaient BigInt.

D’autres pouvaient utiliser FLOAT64.

Certaines étaient approximatives.

D’autres exactes.

Les forcer à utiliser exactement la même représentation numérique pouvait désavantager artificiellement l’une d’elles.

---

Brutus réfléchit.

---

Il décida de séparer deux types d’arène.

**EQUAL ENVIRONMENT**

et

**NATIVE ENVIRONMENT.**

---

Dans EQUAL ENVIRONMENT, les formules recevaient volontairement les mêmes contraintes techniques.

Même modèle numérique.

Même budget.

Même matériel logique.

---

Dans NATIVE ENVIRONMENT, chaque formule pouvait utiliser son environnement déclaré comme optimal ou requis.

---

Deux questions différentes.

---

Equal environment demandait :

**qui se comporte le mieux dans les mêmes conditions ?**

Native environment demandait :

**que produit chaque méthode lorsqu’elle est utilisée correctement selon son propre contrat ?**

---

Brutus écrivit :

**FAIRNESS DEPENDS ON THE QUESTION.**

---

Cela lui sembla important.

Il n’existait pas toujours une seule manière « juste » de comparer.

Il fallait déclarer le type de comparaison.

---

Pour ARENA-0001, il choisit :

**NATIVE ENVIRONMENT.**

L’objectif serait l’exactitude sur un ensemble d’entrées où chaque méthode était admissible.

---

Il sélectionna quatre formules.

F-021.

F-041.

CANDIDATE-0001.

CANDIDATE-0004.

---

Puis créa un corpus.

Cent entrées.

Pas choisies après avoir vu les résultats.

---

Brutus écrivit :

**INPUT SET MUST BE COMMITTED BEFORE THE MATCH.**

Encore cette idée de préengagement.

---

Il créa :

**INPUTSET-0001.**

Puis calcula son hash.

---

Les cent entrées furent gelées.

---

Brutus regarda les formules.

Le combat pouvait commencer.

---

Douze lanes.

Quatre méthodes.

Cent entrées.

Quatre cents jobs.

---

Le scheduler se mit au travail.

---

Les premiers résultats arrivèrent.

PASS.

PASS.

PASS.

FAIL.

---

Puis :

PASS.

PASS.

FAIL.

PASS.

---

Le Journal Vivant enregistrait.

---

Brutus ne regardait pas encore les totaux.

Il voulait éviter de tomber amoureux d’un résultat trop tôt.

---

Après cinquante entrées, il aperçut pourtant une tendance.

CANDIDATE-0004 semblait produire moins de divergences.

---

Il sentit immédiatement la tentation.

Voilà.

Le nouveau hybride était meilleur.

---

Il s’arrêta.

---

**PARTIAL RESULT ≠ FINAL RESULT.**

Il écrivit la phrase avant même de continuer.

---

Les quatre cents jobs devaient terminer ou recevoir un état terminal explicite.

---

Pas de conclusion au milieu.

---

L’expérience continua.

---

À l’entrée 73, CANDIDATE-0004 rencontra une région particulière.

FAIL.

Puis encore.

FAIL.

---

Deux autres erreurs apparurent.

---

Brutus sourit.

Exactement pourquoi il avait attendu.

---

À la fin, le résumé disait :

F-021 :

96 PASS.

4 FAIL.

---

F-041 :

98 PASS.

2 FAIL.

---

CANDIDATE-0001 :

97 PASS.

3 FAIL.

---

CANDIDATE-0004 :

97 PASS.

3 FAIL.

---

Brutus regarda les nombres.

Très facile maintenant de dire :

F-041 gagne.

---

Il refusa.

---

La guerre n’avait pas été construite pour produire un podium.

Elle avait été construite pour produire de l’information.

---

Il écrivit :

**SCORE IS A VIEW. NOT A VERDICT OF UNIVERSAL SUPERIORITY.**

---

Les deux échecs de F-041 pouvaient être beaucoup plus graves que les quatre de F-021.

Ou simplement concentrés dans une région particulière.

---

Brutus ouvrit la carte des erreurs.

---

F-021 échouait dans quatre cas dispersés.

F-041 échouait deux fois, mais les deux cas appartenaient au même sous-domaine.

CANDIDATE-0001 avait trois fails très proches d’une frontière numérique.

CANDIDATE-0004 avait trois fails liés à une condition héritée d’un parent.

---

Voilà.

Les nombres bruts cachaient la structure.

---

Il écrivit :

**WHERE A FORMULA FAILS MAY MATTER MORE THAN HOW OFTEN.**

---

Le Journal Vivant dessina une carte.

Entrées sur l’axe horizontal.

Méthodes sur l’axe vertical.

PASS.

FAIL.

DOMAIN.

ERROR.

---

Brutus pouvait voir des motifs.

---

Une bande de FAIL apparaissait pour plusieurs formules sur les mêmes entrées.

---

Cela l’intéressa immédiatement.

---

Si plusieurs méthodes indépendantes échouaient au même endroit, deux interprétations étaient possibles.

Soit la région était réellement difficile.

Soit l’ensemble de référence utilisé pour juger PASS/FAIL était lui-même incorrect.

---

Brutus écrivit :

**COMMON FAILURE CAN IMPLICATE THE TEST, NOT ONLY THE METHODS.**

---

Voilà pourquoi il refusait de transformer l’arène en juge absolu.

---

Il inspecta la région.

---

Une valeur de référence avait été produite par une cinquième méthode.

Cette méthode utilisait elle-même une approximation.

---

Brutus arrêta l’analyse.

---

Le juge avait un juge.

---

Et le juge pouvait se tromper.

---

Il écrivit :

**REFERENCE ≠ ORACLE.**

---

Puis construisit une catégorie :

**REFERENCE_SOURCE.**

---

Toute valeur attendue devait avoir une provenance.

---

Exact proof-derived value.

Independent implementation.

High precision numeric reference.

Historical dataset.

Human assertion.

---

Toutes n’avaient pas le même poids.

---

Brutus modifia ARENA-0001.

Les cas où la référence n’était pas suffisamment solide ne produiraient plus FAIL automatiquement.

Ils produiraient :

**DISAGREEMENT.**

---

Cette distinction lui sembla essentielle.

---

FAIL signifiait :

le résultat violait un critère suffisamment défini.

---

DISAGREEMENT signifiait :

deux sources comparables ne concordaient pas encore.

---

Brutus écrivit :

**DISAGREEMENT ≠ FAILURE.**

---

Puis relança le résumé.

---

Les anciens chiffres changèrent.

Pas parce que les résultats avaient été modifiés.

Parce que la politique de qualification avait été corrigée.

---

F-021 :

94 PASS.

2 FAIL.

4 DISAGREEMENT.

---

F-041 :

96 PASS.

0 FAIL.

4 DISAGREEMENT.

---

CANDIDATE-0001 :

95 PASS.

1 FAIL.

4 DISAGREEMENT.

---

CANDIDATE-0004 :

94 PASS.

2 FAIL.

4 DISAGREEMENT.

---

Brutus regarda.

Le Journal Vivant conservait l’ancienne évaluation et la nouvelle.

---

C’était important.

---

Il écrivit :

**RECLASSIFICATION MUST NOT ERASE PRIOR CLASSIFICATION.**

---

L’histoire devait montrer :

version de politique 1.

Puis version 2.

Pourquoi la règle avait changé.

---

Le passé ne devait pas être réécrit pour donner l’impression que le laboratoire avait toujours eu raison.

---

Brutus ajouta :

**POLICY_VERSION.**

---

ARENA-0001 revint au registre.

---

Le premier combat avait déjà appris quelque chose au système.

Pas laquelle des formules était « meilleure ».

Mais comment mieux comparer.

---

Brutus sourit.

C’était presque plus intéressant.

---

Il construisit ARENA-0002.

Cette fois :

performance.

---

Même input set.

Même hardware profile.

Même precision model.

---

Question :

temps et ressources.

---

Brutus voulait savoir quelles méthodes étaient les plus coûteuses sous les mêmes contraintes.

---

Cette métrique n’avait rien à voir avec l’exactitude.

---

Il écrivit :

**FAST ≠ CORRECT.**

Puis :

**CORRECT ≠ FAST.**

---

Deux axes.

---

ARENA-0002 démarra.

---

F-021 était rapide.

F-041 plus lente.

CANDIDATE-0001 très rapide.

CANDIDATE-0004 variable.

---

Brutus ajouta la consommation mémoire.

---

Encore un autre classement possible.

---

Une formule pouvait être rapide mais gourmande.

Une autre lente mais presque sans mémoire.

---

Brutus écrivit :

**NO SINGLE METRIC DEFINES BEST.**

---

Puis s’arrêta.

Le mot best ne lui plaisait pas.

---

Il corrigea :

**NO SINGLE METRIC DEFINES SUITABILITY FOR ALL USES.**

---

Beaucoup mieux.

---

Le laboratoire ne devait pas créer un championnat simpliste.

Il devait construire un profil.

---

Exactitude observée.

Domaine.

Temps.

Mémoire.

Stabilité numérique.

Robustesse.

Indépendance.

---

Une formule devenait un objet multidimensionnel.

---

Brutus ajouta :

**FORMULA PROFILE.**

---

F-021 pouvait être excellente pour certaines entrées.

F-041 pour d’autres.

CANDIDATE-0001 dans les cas où la vitesse comptait.

CANDIDATE-0004 dans un sous-domaine précis.

---

La guerre commençait déjà à ressembler moins à une guerre qu’à une cartographie.

---

Brutus sourit.

Peut-être était-ce la bonne conclusion.

---

Mais il voulait encore confronter les candidats plus agressivement.

---

Il construisit :

**COUNTEREXAMPLE ARENA.**

---

Cette arène n’essayait pas de confirmer une formule.

Elle cherchait à la casser.

---

Brutus écrivit :

**SEARCH FOR FAILURE, NOT COMFORT.**

---

Il sélectionna CANDIDATE-0001.

---

Le système analysa son domaine déclaré.

Puis généra des classes d’entrées.

Pas des nombres arbitraires uniquement.

---

Limites.

Valeurs extrêmes.

Zéro voisin.

Petites valeurs.

Grandes valeurs.

Transitions de précision.

Cas proches des conditions de domaine.

---

Brutus regarda.

Voilà une guerre beaucoup plus intéressante.

---

Pas :

combien de PASS peux-tu accumuler ?

Mais :

où peux-tu casser ?

---

Il écrivit :

**A THOUSAND EASY PASSES MAY TEACH LESS THAN ONE GOOD COUNTEREXAMPLE.**

---

Le moteur lança les recherches.

---

Cent tests.

Puis mille.

---

CANDIDATE-0001 survivait.

---

Brutus ne déclara rien.

---

Deux mille.

---

Toujours aucune rupture nouvelle.

---

Puis un test près d’une frontière.

FAIL.

---

Brutus se redressa.

---

Il ouvrit la trace.

---

Entrée.

Parent.

Version.

Numeric model.

Reference.

Résultat.

---

Le problème était réel sous le contrat actuel.

---

Le candidat possédait une faille.

---

Brutus sourit.

Pas parce que la formule avait perdu.

Parce que le laboratoire venait d’apprendre quelque chose de précis.

---

Il ajouta :

**COUNTEREXAMPLE-0001.**

---

Le contre-exemple devint un objet.

---

**COUNTEREXAMPLE_ID**

**FORMULA_REF**

**INPUT**

**EXPECTED_RELATION**

**OBSERVED_RESULT**

**ENVIRONMENT**

**TRACE_REF**

**STATUS**

---

Brutus avait compris depuis longtemps qu’un bon échec valait la peine d’être conservé.

---

Ce contre-exemple ne devait jamais être perdu lors d’une nouvelle version.

---

Il ajouta au profil de CANDIDATE-0001 :

**KNOWN COUNTEREXAMPLES: 1**

---

Puis créa CANDIDATE-0005.

Une modification de CANDIDATE-0001 destinée explicitement à corriger ce cas.

---

Parent :

CANDIDATE-0001.

Reason :

COUNTEREXAMPLE-0001.

---

Brutus regarda la lignée.

---

Voilà.

La guerre produisait maintenant une évolution.

---

Pas une mutation aléatoire.

Une réponse à une faiblesse observée.

---

Il écrivit :

**FAILURE CAN BECOME PARENT OF IMPROVEMENT.**

---

Mais encore une fois, il se méfia.

CANDIDATE-0005 pouvait corriger un contre-exemple et casser dix autres cas.

---

Il fallait régression.

---

Brutus ajouta :

**REGRESSION ARENA.**

---

Tout candidat modifié devait rejouer :

les anciens tests,

les contre-exemples,

les limites connues,

et de nouvelles entrées.

---

Il écrivit :

**FIX ONE CASE. RETEST THE WORLD YOU ALREADY KNEW.**

---

CANDIDATE-0005 entra.

---

COUNTEREXAMPLE-0001 :

PASS.

---

Brutus ne célébra pas.

---

Le reste de la campagne continua.

---

Puis deux anciennes entrées échouèrent.

---

Voilà.

La correction avait créé une régression.

---

Brutus classa CANDIDATE-0005 :

**REJECTED FOR CURRENT PURPOSE.**

---

Pas supprimé.

Pas détruit.

---

Le Journal Vivant conserva :

parent.

intention.

correction réussie.

régressions introduites.

raison du rejet.

---

Brutus regarda l’arbre.

CANDIDATE-0001.

Puis branche vers CANDIDATE-0005.

Puis statut REJECTED.

---

Une branche morte.

Mais utile.

---

Il écrivit :

**DEAD BRANCHES ARE PART OF THE MAP.**

---

Une formule rejetée pouvait empêcher le laboratoire de refaire exactement la même mauvaise tentative six mois plus tard.

---

Voilà une autre fonction de la mémoire.

Se souvenir non seulement de ce qui fonctionne.

Mais de ce qui a déjà échoué.

---

Brutus ajouta :

**DO NOT REDISCOVER KNOWN FAILURE AS NEW IDEA.**

---

Le Journal Vivant gagnait soudain beaucoup de valeur.

---

Puis Brutus construisit un système de matchs.

---

Pas un tournoi.

Il refusa ce mot après quelques secondes.

Un tournoi implique généralement un gagnant.

Brutus voulait seulement organiser des confrontations.

---

Il appela cela :

**MATCH SET.**

---

MATCH-001.

F-021 vs F-041.

Target :

exact relation.

---

MATCH-002.

F-021 vs CANDIDATE-0001.

Target :

performance under BigInt.

---

MATCH-003.

CANDIDATE-0001 vs CANDIDATE-0004.

Target :

boundary robustness.

---

Chaque match avait sa métrique.

---

Brutus écrivit :

**A MATCH WITHOUT A QUESTION IS MEANINGLESS.**

---

Cela empêchait le système de produire des classements globaux absurdes.

---

Une méthode pouvait « gagner » en vitesse et « perdre » en mémoire.

Mais aucun de ces résultats ne permettait de dire qu’elle était globalement supérieure.

---

Le Journal Vivant présentait donc les matchs comme des relations.

---

F-021 faster than F-041 under ARENA-0002.

---

F-041 fewer observed exactness failures under INPUTSET-0001 / policy v2.

---

CANDIDATE-0004 lower memory use than CANDIDATE-0001 under profile X.

---

Des faits locaux.

Pas de couronne.

---

Brutus apprécia beaucoup cette architecture.

---

La guerre des formules cessait d’être une guerre de domination.

Elle devenait un système de différenciation.

---

Il écrivit :

**COMPARISON SHOULD PRODUCE A MAP, NOT A KING.**

---

Puis il regarda le mot KING.

Il sourit.

Et conserva la phrase.

---

Brutus lança plusieurs matchs.

Le Journal Vivant s’enrichissait.

---

Pour chaque formule, une carte apparaissait.

---

Strong observed region.

Known failure region.

Unknown region.

Resource profile.

Counterexamples.

Relations to other methods.

---

Les inconnues étaient visibles.

---

Brutus insista là-dessus.

Une zone jamais testée devait être affichée :

**UNKNOWN.**

Pas vide.

Pas supposée bonne.

---

Il écrivit :

**UNTESTED MUST NOT LOOK LIKE PASSED.**

---

Cette règle allait devenir essentielle.

---

Une formule pouvait avoir 99 % de vert sur les zones testées.

Mais si 90 % du domaine n’avait jamais été exploré, l’interface devait le montrer.

---

Brutus ajouta une couche grise.

UNKNOWN.

---

La carte devenait honnête.

---

Puis un cas intéressant apparut.

F-021 avait un domaine plus petit mais mieux testé.

CANDIDATE-0004 avait un domaine déclaré beaucoup plus large mais peu exploré.

---

Une simple proportion de PASS aurait favorisé artificiellement le second.

---

Brutus écrivit :

**COVERAGE AND SUCCESS RATE MUST BE SEPARATE.**

---

Il ajouta deux métriques.

**TEST COVERAGE**

et

**OBSERVED PASS RATE WITHIN TESTED SET**

---

Pas de mélange.

---

La guerre devenait de plus en plus précise.

---

Brutus pensa alors aux variantes générées automatiquement.

Si la machine pouvait en créer des centaines, les arènes pourraient devenir extrêmement coûteuses.

---

Il fallait un filtre avant le combat complet.

---

Il construisit :

**QUALIFICATION GATE.**

---

Avant d’entrer dans les grandes arènes, une formule candidate devait passer des tests minimaux.

---

Syntaxe valide.

Domain metadata present.

Numeric model declared.

No known trivial contradiction.

Basic unit tests.

Parent lineage present.

---

Brutus écrivit :

**NOT EVERY CANDIDATE EARNS AN EXPENSIVE TEST.**

---

Il lança cent variantes artificielles.

---

Soixante-deux furent éliminées au gate.

---

Pas REJECTED scientifiquement.

---

**NOT QUALIFIED FOR ARENA.**

---

Encore une distinction.

---

Certaines étaient peut-être intéressantes.

Mais mal spécifiées.

---

Le système ne devait pas confondre manque de métadonnées et fausseté mathématique.

---

Il écrivit :

**PROCESS FAILURE ≠ FORMULA FALSEHOOD.**

---

Trente-huit candidates entrèrent dans les tests rapides.

---

Vingt-trois rencontrèrent des contre-exemples immédiats.

---

Quinze survécurent.

---

Brutus les regarda.

La tentation de dire « quinze gagnantes » apparut.

Il la repoussa.

---

**15 SURVIVED CURRENT FILTERS.**

C’était tout.

---

Il ajouta cette phrase au résumé.

---

Le vocabulaire devenait aussi important que les calculs.

---

Brutus choisit les quinze candidates.

Puis lança un second niveau de campagne.

---

Plus d’entrées.

Plus de précision.

Plusieurs environnements.

Contre-exemples historiques.

---

Le nombre descendit.

---

Neuf.

Puis six.

Puis quatre.

---

Brutus regardait.

---

Ce processus ressemblait réellement à une sélection.

---

Mais il refusait encore de parler d’évolution biologique.

---

Il écrivit :

**SELECTION PROCESS = ENGINEERING FILTER, NOT BIOLOGICAL CLAIM.**

---

Toujours protéger la métaphore.

---

Les quatre candidates restantes furent placées dans une arène de comparaison avec leurs parents.

---

Une nouvelle surprise apparut.

L’une était meilleure dans presque toutes les mesures opérationnelles testées.

Mais beaucoup plus difficile à comprendre.

---

Sa structure était complexe.

---

Brutus ajouta une nouvelle dimension.

**INTERPRETABILITY.**

Puis s’arrêta.

---

Comment mesurer cela ?

---

Il ne voulait pas inventer un score pseudo-scientifique.

---

Il transforma la métrique en données concrètes.

Expression size.

Number of operators.

Dependency depth.

External dependencies.

Number of domain branches.

---

Pas :

**interpretability = 7.4/10.**

---

Il écrivit :

**MEASURE PROXIES. DO NOT PRETEND TO MEASURE THE ABSTRACT DIRECTLY.**

---

Cela lui plut.

---

Une formule complexe pouvait rester excellente.

Mais sa complexité devenait visible.

---

Le laboratoire pouvait ensuite décider selon l’usage.

---

Brutus vit quelque chose de très important.

Les arènes ne pouvaient pas décider seules des promotions.

---

Elles produisaient des mesures.

La politique de promotion utilisait ensuite ces mesures.

---

Il écrivit :

**ARENA PRODUCES EVIDENCE.**

**POLICY PRODUCES ELIGIBILITY.**

**AUTHORITY PRODUCES STATUS CHANGE.**

---

Trois niveaux.

---

Pas d’auto-couronnement.

---

Même une formule qui survivait à toutes les arènes ne devait pas se promouvoir elle-même.

---

Brutus ajouta :

**NO SELF-PROMOTION.**

---

Il imagina une candidate générée par la machine qui modifie également ses propres critères de victoire.

Absurde.

---

Il verrouilla les politiques.

---

Une formule ne pouvait pas modifier :

son propre score contract.

son input set.

ses critères de promotion.

ses références attendues.

---

Il écrivit :

**THE CONTESTANT MUST NOT WRITE THE RULES OF ITS OWN MATCH.**

---

Voilà une règle qui allait probablement survivre longtemps.

---

La soirée passa.

Les arènes continuèrent.

---

Des formules entraient.

Certaines s’effondraient rapidement.

Certaines révélaient des limites.

Certaines semblaient prometteuses.

Certaines ne faisaient que reproduire leurs parents.

---

Brutus ajouta un détecteur de duplication.

---

Deux expressions différentes pouvaient être équivalentes après simplification.

---

Il ne voulait pas gaspiller des heures à faire combattre une formule contre elle-même déguisée.

---

Il créa :

**EQUIVALENCE CANDIDATE.**

---

Pas d’affirmation automatique.

---

Le système pouvait détecter une possible équivalence symbolique ou empirique.

Puis demander vérification.

---

Brutus écrivit :

**SAME OUTPUT ON TEST SET ≠ SAME FORMULA.**

---

Encore.

---

Deux méthodes pouvaient coïncider sur mille valeurs et diverger à la mille et unième.

---

Le laboratoire ne devait jamais appeler cela une identité prouvée sans argument supplémentaire.

---

Il conserva donc les deux.

---

Le Journal Vivant montrait seulement :

**NO DIVERGENCE OBSERVED ON SET X.**

---

Cette phrase devenait presque une signature du laboratoire.

---

Brutus regarda la carte générale.

---

Des branches.

Des arènes.

Des contre-exemples.

Des restrictions.

Des candidats.

Des relations.

---

Le FORMULA REGISTRY n’était plus une liste.

---

Il devenait réellement un écosystème de méthodes.

---

Pas vivant biologiquement.

Mais dynamique.

Historique.

Sélectif.

---

Brutus ouvrit CANDIDATE-0004.

---

Son histoire était maintenant longue.

Parentage.

Generation.

Tests.

Three disagreement regions.

Two resource profiles.

One known restriction.

No current counterexample under a specific domain subset.

---

Il pouvait être tenté de le promouvoir.

---

Mais il regarda le champ :

**COVERAGE: 41 %.**

---

Pas assez selon la politique actuelle.

---

Brutus laissa son statut :

CANDIDATE.

---

La formule attendrait.

---

Il écrivit :

**PROMISING ≠ READY.**

---

Puis sourit.

Encore une frontière.

---

Le laboratoire devenait un grand catalogue de frontières.

Peut-être était-ce cela, la rigueur.

---

Savoir exactement où une affirmation s’arrête.

---

Brutus ferma les arènes.

---

Le Journal Vivant continua d’indexer.

---

Il regarda la liste des candidats.

---

Certains REJECTED.

Certains RESTRICTED.

Certains CANDIDATE.

Quelques-uns encore UNKNOWN.

---

Aucun champion.

---

Cela lui plut.

---

La guerre n’avait produit aucun roi.

Elle avait produit une carte beaucoup plus précise de ce que chaque formule savait faire.

---

Brutus écrivit :

**LA GUERRE DES FORMULES N’A PAS POUR BUT DE TROUVER LA PLUS BELLE.**

Puis :

**NI LA PLUS RAPIDE.**

Puis :

**NI CELLE QUI GAGNE LE PLUS SOUVENT.**

---

Il continua :

**ELLE SERT À DÉCOUVRIR OÙ CHAQUE MÉTHODE TIENT, OÙ ELLE CASSE, ET CE QU’ELLE COÛTE.**

---

Voilà.

---

Il sauvegarda ARENA-0001.

ARENA-0002.

Les contre-exemples.

Les profils.

Les politiques.

---

Puis il remarqua un petit événement étrange dans le Journal Vivant.

---

Une formule venait de produire un résultat inattendu.

Pas FAIL.

Pas DOMAIN.

Pas ERROR.

---

Le calcul était terminé correctement.

Mais le nombre affiché ne correspondait pas à ce que la trace exacte semblait contenir.

---

Brutus regarda l’écran.

Puis la trace.

Puis l’écran.

---

Encore.

---

La formule n’avait peut-être pas menti.

Peut-être que le nombre, lui, avait changé en chemin.

---

Brutus ouvrit les détails.

Type numérique :

**Number.**

---

Valeur attendue :

un grand entier.

---

Valeur affichée :

presque identique.

---

Presque.

---

Brutus se redressa.

Il connaissait déjà ce danger.

Mais cette fois, il venait d’apparaître en pleine guerre des formules.

---

Une méthode pouvait perdre un combat non parce que sa mathématique était mauvaise…

mais parce que le nombre qui la transportait avait perdu des chiffres.

---

Brutus écrivit :

**PAUSE ALL COMPARISONS INVOLVING THIS VALUE.**

---

Les lanes concernées s’arrêtèrent.

---

Il regarda le grand entier.

---

Une différence minuscule relativement à sa taille.

Mais une différence exacte.

---

Dans une guerre de formules, cela suffisait pour accuser une méthode à tort.

---

Brutus écrivit une dernière ligne :

**AVANT D’ACCUSER LA FORMULE, IL FAUT INTERROGER LE NOMBRE QUI PORTE SA RÉPONSE.**

Puis il sauvegarda.

La guerre des formules venait de rencontrer un ennemi qu’aucune méthode n’avait créé.

Un ennemi discret.

Invisible sur les petits nombres.

Et terriblement dangereux lorsqu’on exigeait l’exactitude.

Le prochain interrogatoire allait commencer avec une seule question :

**qu’est-ce que Number vient de faire ?**
