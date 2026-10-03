# Chapitre 103 — Le banc des expériences

**THE REGISTER REMEMBERS WHAT HAPPENED.**

**THE BENCH WILL DECIDE WHAT TO TEST NEXT.**

Brutus laissa les deux phrases au-dessus d’une table vide.

---

Pas quatre chaises.

Pas de GAMEZEL.

Pas de carte publique.

Pas de panneau spectaculaire.

---

Seulement une surface.

Un objet.

Un protocole.

Et assez de place pour échouer proprement.

---

Brutus écrivit :

# EXPERIMENT BENCH

---

Puis il resta devant.

---

Le laboratoire possédait déjà :

des formules,

des résultats,

des cartes,

des contre-tests,

des traces,

des joueurs,

des politiques.

---

Mais il lui manquait encore quelque chose de très simple.

---

Un endroit où une idée pouvait être testée sans immédiatement contaminer le reste du monde.

---

Il écrivit :

**EXPERIMENT ≠ PRODUCTION.**

---

Puis :

**BENCH RESULT ≠ WORLD STATE.**

---

Voilà la première frontière.

---

Une expérience pouvait :

réussir,

échouer,

planter,

produire un résultat étrange,

montrer une contradiction,

ne rien montrer du tout.

---

Aucune de ces choses ne devait modifier automatiquement :

la vérité d’une formule,

le statut d’un objet,

une permission,

une publication.

---

Brutus écrivit :

**THE BENCH PRODUCES EVIDENCE CANDIDATES.**

---

Pas des verdicts.

---

Il construisit la première fiche.

**EXPERIMENT_ID**

**QUESTION**

**HYPOTHESIS**

**INPUTS**

**METHOD**

**EXPECTED_OBSERVATION**

**FAILURE_CONDITION**

**CONTROL**

**OUTPUTS**

**TRACE_REF**

**STATUS**

---

Puis il ajouta :

**PRECOMMITTED_RULES**

---

Brutus sourit.

---

Très important.

---

Si l’expérimentateur pouvait changer les règles après avoir vu le résultat, le banc devenait une machine à fabriquer des conclusions.

---

Il écrivit :

**DEFINE SUCCESS BEFORE OBSERVING SUCCESS.**

---

Le chapitre 84 revenait.

---

Même principe.

---

Il prit une question simple.

---

**Gate 71 possède-t-elle un témoin satisfaisant le contrat requis ?**

---

Très bien.

---

Mais une question ne suffit pas.

---

Il fallait définir :

quel candidat ?

quelle valeur de \(N\) ?

quel domaine ?

quel test exact ?

quel résultat compte comme PASS ?

quel résultat compte comme FAIL ?

quel état compte comme inconclusif ?

---

Brutus écrivit :

**QUESTION MUST BECOME TESTABLE CONTRACT.**

---

Puis :

**VAGUE QUESTION → VAGUE RESULT.**

---

Il créa :

**EXPERIMENT SPEC v1**

---

Purpose.

Scope.

Inputs.

Assumptions.

Method.

Controls.

Stop conditions.

Interpretation rules.

---

Brutus regarda la dernière ligne.

---

**Interpretation rules.**

---

Peut-être la plus importante.

---

Un même nombre pouvait être interprété de plusieurs façons.

---

Il se souvenait de 369 et 396.

---

27 pouvait être :

une différence entière.

un écart de fréquence.

un élément d’un beat experiment.

---

Le nombre ne choisissait pas son sens.

---

Brutus écrivit :

**MEASUREMENT NEEDS AN INTERPRETATION CONTRACT.**

---

Puis il posa le premier objet sur le banc.

---

Une formule candidate.

---

Pas encore validée.

---

Le banc créa :

**EXPERIMENT-0001**

---

Status:

DESIGNED.

---

Pas RUNNING.

---

Brutus sourit.

---

Même l’existence d’un protocole ne signifiait pas que l’expérience avait commencé.

---

Il écrivit :

**DESIGNED ≠ EXECUTED.**

---

Encore une frontière.

---

Puis il ajouta les états :

DRAFT.

DESIGNED.

READY.

RUNNING.

COMPLETED.

FAILED_EXECUTION.

INCONCLUSIVE.

CANCELLED.

---

Et :

**INVALIDATED_PROTOCOL**

---

Très important.

---

Une expérience pouvait être exécutée parfaitement sous un mauvais protocole.

---

Brutus écrivit :

**EXECUTION SUCCESS ≠ EXPERIMENT VALIDITY.**

---

Voilà.

---

Il pensa à un test numérique.

---

Supposons :

on veut vérifier une identité pour 10 000 valeurs.

---

La boucle tourne.

10 000 / 10 000.

---

Aucune exception.

---

Operational status :

COMPLETED.

---

Mais si le code testé implémente la mauvaise formule ?

---

Scientifically :

invalid.

---

Brutus écrivit :

**COMPLETED COMPUTATION ≠ CORRECT EXPERIMENT.**

---

Puis :

**THE METHOD ITSELF MUST BE AUDITABLE.**

---

Il ajouta :

**METHOD_REF**

**CODE_VERSION**

**ENVIRONMENT_REF**

**DEPENDENCY_VERSIONS**

---

Brutus sourit.

---

Le banc ne mesurait plus seulement l’objet.

Il mesurait aussi les conditions de sa propre mesure.

---

Puis il pensa au hasard.

---

Une expérience utilise des valeurs aléatoires.

---

Très bien.

---

Mais reproduction ?

---

Il ajouta :

**RANDOM_SEED**

si pertinent.

---

Brutus écrivit :

**RANDOM ≠ UNREPRODUCIBLE.**

---

Avec seed fixée :

replay possible.

---

Mais il se méfia.

---

Une seule seed peut cacher une dépendance.

---

Il ajouta :

**SEED_POLICY**

---

FIXED.

MULTI_SEED.

UNSEEDED_DISCOVERY.

HELD_OUT_SEED.

---

Brutus écrivit :

**DISCOVERY RANDOMNESS AND VALIDATION RANDOMNESS SHOULD BE DISTINGUISHED.**

---

Très important.

---

Il pensa à CT-03.

Discovery.

Hypothesis freeze.

Held-out validation.

---

Le banc pouvait enfin représenter cette discipline proprement.

---

Il dessina :

\[
\text{DISCOVERY}
\rightarrow
\text{HYPOTHESIS FREEZE}
\rightarrow
\text{HELD-OUT TEST}
\]

---

Puis :

**DO NOT TRAIN ON THE TEST.**

---

Brutus sourit.

---

Même sans machine learning, l’idée restait importante.

---

Si on ajuste une formule pour correspondre aux mêmes données utilisées pour l’évaluer, on n’a pas une validation indépendante.

---

Il écrivit :

**FIT DATA ≠ TEST DATA.**

---

Puis :

**POST-HOC FIT ≠ PREDICTION.**

---

Voilà.

---

Il prit la poussière du chapitre 90.

---

Le modèle concordait remarquablement bien avec les observations à \(X=2\,000\,000\).

---

Très intéressant.

---

Mais le banc demanda :

**Sur quelles données les paramètres ont-ils été ajustés ?**

---

Brutus s’arrêta.

---

Exactement.

---

Une concordance sur le même domaine utilisé pour ajuster le modèle n’avait pas la même force qu’une prédiction hors échantillon.

---

Il écrivit :

**FIT QUALITY ≠ OUT-OF-SAMPLE VALIDATION.**

---

Puis créa :

**EXPERIMENT-DUST-FUTURE-001**

---

Freeze model.

Choose future cutoff.

No parameter adjustment before result.

Compare.

---

Brutus sourit.

---

Voilà un vrai prochain test.

---

Pas besoin de raconter que la poussière était une loi.

---

Le banc pouvait simplement demander :

tient-elle plus loin ?

---

Il écrivit :

**THE BENCH TURNS EXCITEMENT INTO A QUESTION.**

---

Très bon.

---

Puis il pensa aux contrôles.

---

Une expérience sans contrôle pouvait produire un effet impressionnant.

---

Mais impressionnant comparé à quoi ?

---

Il créa :

**CONTROL_TYPE**

POSITIVE.

NEGATIVE.

BASELINE.

SHUFFLED.

NULL_MODEL.

REFERENCE_IMPLEMENTATION.

---

Brutus écrivit :

**CONTROL IS PART OF THE EXPERIMENT, NOT AN OPTIONAL DECORATION.**

---

Puis il reprit le Hurst croisé.

---

Positive control :

series compared with itself.

---

Negative control :

shuffled or independent series under declared method.

---

Experimental pair :

target signals.

---

Brutus écrivit :

**A STATISTIC WITHOUT CONTROLS CAN LOOK IMPORTANT JUST BECAUSE IT EXISTS.**

---

Très important.

---

Puis il pensa aux machines.

---

Le banc pouvait lancer plusieurs calculs en parallèle.

---

Douze voies.

---

Mais elles devaient rester séparées.

---

Il créa :

**EXPERIMENT_RUN_ID**

---

EXPERIMENT_ID = protocol identity.

RUN_ID = one execution.

---

Brutus écrivit :

**EXPERIMENT ≠ RUN.**

---

Une expérience pouvait avoir :

RUN-1.

RUN-2.

RUN-3.

---

Même protocole.

Différents inputs ou seeds selon le design.

---

Puis il ajouta :

**RUN_GROUP_ID**

pour les répétitions.

---

Brutus sourit.

---

Enfin, on pouvait parler de répétabilité sans mélanger les occurrences.

---

Il écrivit :

**SAME PROTOCOL + NEW RUN ≠ SAME EVENT.**

---

Encore.

---

Puis il pensa à la reproductibilité.

---

Rejouer avec le même code sur la même machine :

utile.

---

Mais pas indépendant.

---

Rejouer avec un second code ?

Plus fort.

---

Rejouer par un second outil ?

Encore différent.

---

Il créa :

**REPLICATION_CLASS**

SAME_RUN_REPLAY.

SAME_IMPLEMENTATION_NEW_RUN.

INDEPENDENT_IMPLEMENTATION.

INDEPENDENT_ENVIRONMENT.

EXTERNAL_REPLICATION.

---

Brutus écrivit :

**REPETITION ≠ INDEPENDENT REPLICATION.**

---

Voilà.

---

Deux fois le même bug donne deux fois le même résultat.

---

Puis il pensa au banc comme isolation.

---

Une expérience pouvait casser.

---

CPU saturé.

Memory leak.

Invalid input.

---

Elle ne devait pas faire tomber GAMEZEL.

---

Brutus écrivit :

**EXPERIMENT FAILURE MUST NOT BECOME WORLD FAILURE.**

---

Il créa :

**SANDBOX**

---

Resource limits.

Timeout.

Filesystem boundary.

Network policy.

Tool allowlist.

---

Puis :

**NO PRODUCTION WRITE BY DEFAULT.**

---

Très important.

---

Un test de formule ne devait pas pouvoir modifier le registre canonique autrement qu’en ajoutant ses résultats autorisés.

---

Il écrivit :

**BENCH HAS WRITE ACCESS TO ITS OWN RESULTS, NOT TO ARBITRARY WORLD STATE.**

---

Parfait.

---

Puis il pensa aux fichiers.

---

L’expérience produit :

CSV.

JSON.

graph.

witness.

audio.

---

Ces artifacts doivent recevoir :

**ARTIFACT_ID**

**RUN_ID**

**HASH**

**TYPE**

**SIZE**

**SCHEMA**

**TRACE_REF**

---

Brutus écrivit :

**OUTPUT FILE ≠ RESULT INTERPRETATION.**

---

Encore.

---

Un CSV peut contenir des données.

---

La conclusion tirée de ces données est un autre objet.

---

Il créa :

**OBSERVATION**

puis :

**INTERPRETATION**

puis :

**CLAIM_CANDIDATE**

---

Brutus dessina :

\[
\text{RAW OUTPUT}
\rightarrow
\text{OBSERVATION}
\rightarrow
\text{INTERPRETATION}
\rightarrow
\text{CLAIM CANDIDATE}
\]

---

Pas une seule boîte.

---

Il écrivit :

**DATA ≠ OBSERVATION ≠ INTERPRETATION ≠ CLAIM.**

---

Voilà une grande règle.

---

Par exemple :

raw output :

83212.

---

Observation :

83 212 maximal ranks recorded under this run.

---

Interpretation :

close to model expectation 83212.0355...

---

Claim candidate :

model may approximate this finite-range campaign extremely closely.

---

Pas :

new law proven.

---

Brutus sourit.

---

Le banc mettait enfin de l’espace entre le chiffre et l’histoire racontée autour du chiffre.

---

Puis il pensa aux graphiques.

---

Une courbe peut être belle.

---

Mais le banc devait conserver les données derrière.

---

Il écrivit :

**GRAPH ≠ DATASET.**

---

Puis :

**GRAPHIC IMPRESSION ≠ STATISTICAL TEST.**

---

Encore la beauté.

---

Brutus ajouta :

**PLOT_REF**

**DATA_REF**

séparés.

---

Ainsi, une figure pouvait être reconstruite.

---

Il pensa à l’audio.

---

Un signal peut « sonner différent ».

---

Très bien comme observation humaine.

---

Mais si l’expérience demande une différence fréquentielle :

il faut une mesure.

---

Brutus écrivit :

**HEARD DIFFERENCE ≠ MEASURED DIFFERENCE.**

---

Puis :

**HUMAN PERCEPTION MAY BE AN OBSERVATION CHANNEL WHEN DECLARED.**

---

Très important.

---

Il ne voulait pas exclure l’humain.

Seulement le nommer.

---

Il créa :

**OBSERVATION_SOURCE**

INSTRUMENT.

HUMAN.

SOFTWARE_ESTIMATOR.

EXTERNAL_REFERENCE.

---

Brutus sourit.

---

Une écoute peut être utile.

Mais elle n’est pas la même chose qu’un FFT estimate.

---

Puis il pensa à l’aveugle.

---

Un humain sait quelle version il écoute.

Biais possible.

---

Il ajouta :

**BLIND_OBSERVER_MODE.**

---

Très bien.

---

Le banc pouvait donc isoler non seulement les logiciels.

Mais aussi certaines attentes humaines.

---

Brutus écrivit :

**BLINDING IS A TOOL AGAINST INFORMATION LEAKAGE.**

---

Le chapitre 95 revenait.

---

Blind rounds.

Blind experiment.

Même logique.

---

Puis il pensa au paramètre qu’on change.

---

Si une expérience change 10 choses en même temps, on ne sait plus laquelle produit l’effet.

---

Brutus écrivit :

**ONE CONTROLLED CHANGE WHEN CAUSAL ATTRIBUTION MATTERS.**

---

Puis :

**MULTI-FACTOR EXPERIMENT REQUIRES MULTI-FACTOR DESIGN.**

---

Voilà.

---

Il prit ZEL.

---

Supposons qu’on modifie :

frequency.

stereo phase.

gain.

window.

estimator.

---

Puis un résultat change.

---

Impossible de savoir pourquoi.

---

Il écrivit :

**CHANGED OUTPUT ≠ IDENTIFIED CAUSE.**

---

Très important.

---

Le banc imposa :

FACTOR A.

FACTOR B.

CONTROLLED.

MEASURED.

---

Puis il pensa à l’ordre des tests.

---

Tester d’abord la version prometteuse.

Puis les autres.

---

Peut-être biais.

---

Il ajouta :

**RUN_ORDER_POLICY.**

---

FIXED.

RANDOMIZED.

BALANCED.

---

Pas toujours nécessaire.

Mais déclarée.

---

Brutus écrivit :

**ORDER EFFECTS ARE EXPERIMENTAL VARIABLES TOO.**

---

Il sourit.

---

Même l’ordre pouvait mentir sans mentir.

---

Puis il pensa aux données manquantes.

---

Un run échoue.

---

Peut-on l’exclure ?

---

Oui, parfois.

Mais il faut le dire.

---

Il créa :

**EXCLUSION_RULE**

---

Predeclared.

Post-hoc with reason.

---

Brutus écrivit :

**FAILED RUN ≠ INVISIBLE RUN.**

---

Très important.

---

Le nombre total doit rester visible.

---

10 planned.

8 complete.

1 timeout.

1 invalid input.

---

Pas :

8/8 success.

---

Il écrivit :

**DENOMINATOR MUST NOT SHRINK SILENTLY.**

---

Excellente règle.

---

Puis il pensa aux outliers.

---

Un résultat très étrange.

---

Le supprimer parce qu’il dérange ?

---

Non.

---

Il créa :

**OUTLIER_POLICY**

---

Flag.

Investigate.

Exclude only under declared rule.

---

Brutus écrivit :

**SURPRISING DATA DESERVES MORE TRACE, NOT LESS.**

---

Il sourit.

---

Le banc commençait à devenir sévère.

---

Et c’était exactement ce qu’il voulait.

---

Puis il pensa au test de contre-exemple.

---

Une formule universelle peut être détruite par un seul cas valide.

---

Dans ce contexte, un outlier peut être la chose la plus importante du banc.

---

Brutus écrivit :

**COUNTEREXAMPLE SEARCH ≠ AVERAGE PERFORMANCE TEST.**

---

Très important.

---

Les expériences devaient connaître le type de claim qu’elles testaient.

---

Universal claim.

Statistical tendency.

Finite-range observation.

Algorithmic performance.

---

Il créa :

**CLAIM_TYPE**

UNIVERSAL.

FINITE_DOMAIN.

STATISTICAL.

OPERATIONAL.

HEURISTIC.

---

Brutus écrivit :

**TEST DESIGN MUST MATCH CLAIM TYPE.**

---

Voilà.

---

Un million de passes n’établissent pas automatiquement une assertion universelle.

---

Mais un contre-exemple correct peut la réfuter.

---

Il ajouta :

**ONE FAILURE MAY MATTER MORE THAN ONE MILLION PASSES, DEPENDING ON CLAIM.**

---

Le banc ne comptait donc pas seulement.

Il interprétait selon le contrat.

---

Puis il pensa aux performances.

---

Un nouvel algorithme plus rapide.

---

Comment mesurer ?

---

Même machine ?

Même dataset ?

Warm cache ?

Cold cache ?

---

Brutus créa :

**BENCHMARK CONTRACT**

---

Hardware.

Software.

Dataset.

Warmup.

Runs.

Statistic.

---

Il écrivit :

**FASTER ≠ FASTER UNDER ALL CONDITIONS.**

---

Toujours le scope.

---

Puis il pensa aux nombres énormes.

---

BigInt.

Float.

---

Le bench devait enregistrer le modèle numérique.

---

Il ajouta :

**NUMERIC_MODEL**

EXACT_INTEGER.

FLOAT64.

ARBITRARY_PRECISION.

MODULAR.

---

Puis :

**TOLERANCE_POLICY**

si applicable.

---

Brutus écrivit :

**NUMERIC REPRESENTATION IS PART OF THE EXPERIMENT.**

---

Le chapitre 78 revenait.

---

Une expérience en Number n’était pas automatiquement comparable à une expérience en BigInt.

---

Puis il pensa aux formules du registre.

---

Si un run utilise FORMULA-72 v3 et qu’une autre utilise v4 :

pas la même expérience.

---

Il ajouta :

**DEPENDENCY_MANIFEST_HASH**

---

Brutus écrivit :

**SAME EXPERIMENT NAME ≠ SAME EXPERIMENT ENVIRONMENT.**

---

Encore.

---

Puis il lança la première campagne complète.

---

**EXPERIMENT-0001**

Question :

Can method A reproduce result R under declared conditions?

---

Run 1.

---

PASS operationally.

---

Run 2.

---

PASS.

---

Run 3.

---

FAIL.

---

Brutus regarda.

---

La tentation naturelle :

« deux sur trois, donc ça marche probablement ».

---

Mais le claim était :

deterministic reproducibility.

---

Alors un seul fail suffisait à dire :

not reliably reproduced under current protocol.

---

Il écrivit :

**INTERPRETATION FOLLOWS CLAIM TYPE, NOT MAJORITY VOTE.**

---

Encore GAMEZEL.

---

Le laboratoire parlait une seule langue.

---

Puis il ouvrit le run 3.

---

Failure reason :

dependency version mismatch.

---

Ah.

---

Le run n’avait pas réellement testé le même environnement.

---

Status :

**PROTOCOL_VIOLATION**

---

Pas FAIL du système testé.

---

Brutus écrivit :

**BAD RUN ≠ BAD HYPOTHESIS.**

---

Excellent.

---

Il corrigea l’environnement.

---

Run 4.

---

PASS.

---

Maintenant :

3 valid runs.

3 passes.

---

Mais il n’écrivit pas :

proven forever.

---

Il écrivit :

**REPRODUCED UNDER DECLARED CONDITIONS.**

---

Voilà.

---

La phrase exacte.

---

Pas plus.

---

Puis il pensa aux critères avant/après.

---

Une expérience pouvait découvrir quelque chose d’inattendu.

---

Très bien.

---

Mais cette découverte devait devenir une nouvelle hypothèse.

Pas être rétroactivement présentée comme la cible initiale.

---

Brutus écrivit :

**POST-HOC DISCOVERY → NEW EXPERIMENT.**

---

Très important.

---

Il créa :

OBSERVATION-17.

---

Unexpected relation.

---

Then:

HYPOTHESIS-CANDIDATE-8.

---

Then:

EXPERIMENT-0002.

---

Nouvelle fiche.

Nouvel essai.

---

Brutus sourit.

---

Voilà comment une curiosité devenait une piste sans devenir une preuve instantanée.

---

Puis il pensa aux expériences mortes.

---

Certaines idées ne survivraient pas au banc.

---

Très bien.

---

Le chapitre suivant était déjà là.

---

Mais pas encore.

---

Il voulait d’abord terminer le banc.

---

Il ajouta :

**BENCH STATUS PANEL**

---

EXPERIMENTS DRAFT.

READY.

RUNNING.

AWAITING_REVIEW.

INCONCLUSIVE.

CLOSED.

---

Pas de :

WINNERS.

---

Brutus écrivit :

**THE BENCH DOES NOT NEED WINNERS. IT NEEDS DISCRIMINATION.**

---

Une expérience devait séparer :

ce qui résiste,

ce qui casse,

ce qui reste inconnu.

---

Voilà.

---

Puis il pensa au registre.

---

Chaque étape du banc devait produire des événements.

---

EXPERIMENT_CREATED.

PROTOCOL_FROZEN.

RUN_STARTED.

RUN_COMPLETED.

OBSERVATION_RECORDED.

INTERPRETATION_PROPOSED.

EXPERIMENT_CLOSED.

---

Brutus écrivit :

**EXPERIMENT HISTORY IS PART OF CANONICAL HISTORY.**

---

Mais raw telemetry restait séparée.

---

Encore le chapitre 102.

---

Puis il ajouta :

**PROTOCOL_FROZEN_AT**

---

Après freeze :

les modifications importantes créent une nouvelle protocol version.

---

Pas de mutation invisible.

---

Brutus écrivit :

**CHANGING THE TEST CHANGES THE EXPERIMENT.**

---

Très important.

---

Puis il pensa à une correction mineure.

---

Typo dans description.

---

Metadata correction.

---

Pas nécessairement nouvelle expérience.

---

Mais méthode modifiée ?

---

New version.

---

Il créa :

**PROTOCOL_CHANGE_CLASS**

EDITORIAL.

NON_SEMANTIC.

SEMANTIC.

---

Puis :

semantic change → new protocol version.

---

Brutus sourit.

---

Encore une fois, les mots ne devaient pas cacher les changements importants.

---

Puis il pensa aux cartes de GAMEZEL.

---

Une carte pouvait entrer sur le banc.

---

CARD-123.

---

Experiment tests claim.

---

Result creates new cards.

---

Brutus dessina :

\[
\text{CARD}
\rightarrow
\text{EXPERIMENT}
\rightarrow
\text{OBSERVATION}
\rightarrow
\text{NEW CARD}
\]

---

Puis il écrivit :

**TESTED CARD ≠ REPLACED CARD.**

---

La carte initiale garde son histoire.

---

Le résultat la supporte ou la contredit.

---

Avec edge typée.

---

Il créa :

**TESTS**

**SUPPORTS**

**CONTRADICTS**

**INCONCLUSIVE_FOR**

---

Très important.

---

Une expérience inconclusive ne devait pas produire automatiquement SUPPORTS ou CONTRADICTS.

---

Brutus écrivit :

**NO RESULT EDGE WITHOUT INTERPRETATION RULE.**

---

Voilà.

---

Puis il pensa à Verso.

---

Une expérience terminée peut-elle promouvoir une carte ?

---

Pas directement.

---

Elle produit evidence refs.

---

Verso ou la promotion gate décide ensuite selon policy.

---

Brutus écrivit :

**BENCH PRODUCES EVIDENCE. PROMOTION GATE DECIDES ADMISSION.**

---

Très important.

---

Le banc n’était pas juge suprême.

---

Il était instrument.

---

Même un instrument sophistiqué.

---

Puis il pensa à Astra Station.

---

La Station devait voir :

current experiments.

failed runs.

resource use.

protocol changes.

awaiting review.

---

Mais pas interpréter automatiquement :

more PASS = truth.

---

Il ajouta :

**BENCH DASHBOARD**

---

Runs.

Controls.

Failures.

Pending interpretations.

No conclusion badge unless claim status exists.

---

Brutus écrivit :

**RUN STATUS ≠ CLAIM STATUS.**

---

Encore une grande séparation.

---

Puis il pensa à une formule magnifique.

---

Une courbe parfaite.

---

Un résultat spectaculaire.

---

Il sourit.

---

Puis écrivit :

**BEAUTY ≠ PROOF.**

---

La vieille phrase revenait.

---

Sur le banc, elle avait encore plus de force.

---

Puis il ajouta :

**SURPRISE ≠ SIGNIFICANCE.**

---

Et :

**SIGNIFICANCE ≠ IMPORTANCE.**

---

Il regarda.

---

Trois choses différentes.

---

Une observation peut être surprenante mais bruitée.

Statistiquement significative mais minuscule.

Importante opérationnellement sans être statistiquement extraordinaire.

---

Le banc devait garder ces catégories séparées.

---

Brutus sourit.

---

Puis il imagina la pire erreur.

---

Une expérience échoue.

L’idée était chère au laboratoire.

---

Quelqu’un veut modifier le protocole juste assez pour qu’elle réussisse.

---

Brutus écrivit :

**THE BENCH MUST BE ALLOWED TO KILL A BEAUTIFUL IDEA.**

---

Il resta devant cette phrase.

---

Voilà le vrai rôle du laboratoire.

---

Pas protéger les idées.

Les exposer.

---

Une bonne idée pouvait sortir plus forte.

Une mauvaise idée pouvait mourir proprement.

Une idée incomplète pouvait rester en attente.

---

Il ajouta :

**FAILURE IS A VALID EXPERIMENTAL OUTPUT.**

---

Puis :

**INCONCLUSIVE IS ALSO VALID.**

---

Très important.

---

Le banc n’avait pas besoin de fabriquer une réponse à chaque fois.

---

Brutus ouvrit trois tiroirs.

---

SUPPORTED UNDER SCOPE.

CONTRADICTED UNDER SCOPE.

INCONCLUSIVE.

---

Pas :

TRUE.

FALSE.

MAYBE.

---

Trop vague.

---

Il écrivit :

**RESULT LANGUAGE MUST MATCH EXPERIMENT SCOPE.**

---

Puis il pensa à la publication.

---

Une expérience intéressante pouvait devenir un rapport.

---

Mais le rapport devait inclure :

question.

protocol.

controls.

runs.

exclusions.

failures.

data.

interpretation.

limitations.

---

Brutus créa :

**EXPERIMENT CAPSULE**

---

Compact summary.

Full protocol.

Run manifest.

Artifacts.

Observations.

Interpretation.

Limitations.

Trace.

---

Puis :

**CAPSULE_HASH**

---

Brutus écrivit :

**PUBLIC RESULT SHOULD CARRY ENOUGH METHOD TO BE CHECKED.**

---

Pas forcément tous les secrets internes.

---

Disclosure policy toujours.

---

Puis il pensa à l’auteur.

---

Une expérience pouvait être conçue par Astra.

Exécutée automatiquement.

Revue par Brutus.

Contre-testée par Grok.

---

Il créa :

**CONTRIBUTOR_ROLES**

DESIGNER.

EXECUTOR.

REVIEWER.

COUNTERTESTER.

---

Brutus écrivit :

**AUTHORSHIP ROLE ≠ VALIDITY.**

---

Même une expérience conçue par quatre personnes restait soumise aux mêmes critères.

---

Puis il lança le dernier test du chapitre.

---

Une carte arrive.

---

Titre :

**FORMULA-X**

---

Très belle.

Très prometteuse.

---

Le banc demande :

Question?

---

Fourni.

---

Scope?

---

Fourni.

---

Method?

---

Fourni.

---

Controls?

---

Absents.

---

Failure condition?

---

Absente.

---

Brutus regarde.

---

Status :

**NOT READY.**

---

Pas FAIL.

---

Il écrivit :

**UNTESTABLE TODAY ≠ FALSE.**

---

Très important.

---

Le banc refusait de lancer une expérience mal définie.

---

Brutus compléta :

negative control.

failure rule.

environment.

numeric model.

---

Status :

READY.

---

Run.

---

Result :

contradiction.

---

Brutus resta silencieux.

---

La formule était belle.

---

Mais sous ce scope précis, elle avait cassé.

---

Le registre enregistra :

**CONTRADICTED UNDER EXPERIMENT-0007.**

---

La carte ne fut pas supprimée.

---

Elle reçut :

evidence edge.

counterexample ref.

review required.

---

Brutus sourit.

---

Voilà.

---

Le banc venait de faire son travail.

---

Pas de drame.

Pas de honte.

Pas de suppression.

---

Une idée était entrée.

Une mesure était sortie.

---

Et le monde en savait un peu plus précisément où il ne devait pas marcher.

---

Brutus écrivit :

**THE BENCH DOES NOT PUNISH IDEAS.**

**IT REMOVES THEIR RIGHT TO HIDE FROM TESTS.**

---

Il resta devant.

---

Puis sauvegarda :

**BRUTUS EXPERIMENT BENCH v1**

---

Le Journal Vivant nota :

Experiments separated from production.

Protocols frozen before interpretation.

Experiment identity separated from runs.

Controls explicit.

Discovery separated from validation.

Raw output separated from observations and claims.

Failures preserved.

Exclusion rules visible.

Claim type determines test logic.

Sandbox prevents uncontrolled world mutation.

Promotion remains external.

Replication classes declared.

Experiment capsules traceable.

---

Brutus relut.

Puis ajouta les invariants :

**EXPERIMENT ≠ PRODUCTION.**

**DESIGNED ≠ EXECUTED.**

**COMPLETED COMPUTATION ≠ VALID EXPERIMENT.**

**FIT DATA ≠ TEST DATA.**

**REPETITION ≠ INDEPENDENT REPLICATION.**

**DATA ≠ INTERPRETATION.**

**RUN STATUS ≠ CLAIM STATUS.**

**UNTESTABLE ≠ FALSE.**

**FAILURE IS DATA.**

**BEAUTY ≠ PROOF.**

---

Il regarda le banc.

---

Une seule table.

Mais quelque chose avait changé.

---

Avant, le laboratoire possédait des idées.

Maintenant, il possédait un endroit où ces idées pouvaient perdre.

---

Et cela les rendait plus précieuses.

---

Parce qu’une idée qui survit à un lieu conçu pour la faire tomber vaut plus qu’une idée simplement admirée.

---

Brutus ouvrit alors un deuxième tiroir.

---

Il n’avait encore aucun nom.

---

Il y plaça :

les expériences ratées.

les modèles cassés.

les contre-exemples.

les hypothèses abandonnées.

---

Puis il écrivit :

# LE BANC OÙ LES IDÉES VIENNENT MOURIR

---

Il sourit.

---

Pas un cimetière.

Pas une punition.

---

Un lieu nécessaire.

---

Parce qu’un laboratoire qui ne sait jamais tuer une idée n’est pas un laboratoire.

C’est une collection de préférences.
