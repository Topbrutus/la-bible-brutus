# Chapitre 105 — Le juge du contre-test

Le dossier portait un seul nom :

**COUNTERTEST JUDGE**

Brutus resta devant.

---

Le banc savait produire des expériences.

Le registre savait tout conserver.

Les idées pouvaient mourir proprement.

Mais une question restait ouverte.

---

Un contre-test apparaissait.

Était-il réellement fatal ?

---

Pas :

est-il impressionnant ?

Pas :

est-il énorme ?

Pas :

est-il produit par plusieurs joueurs ?

---

Mais :

**FRAPPE-T-IL EXACTEMENT LA CLAIM QU’IL PRÉTEND FRAPPER ?**

---

Brutus écrivit immédiatement :

**JUDGE ≠ ORACLE.**

---

Puis :

**JUDGE APPLIES A CONTRACT.**

---

Voilà.

---

Le juge ne devait pas dire :

« ceci est vrai parce que je le déclare ».

---

Il devait examiner :

la claim.

le domaine.

le contre-test.

la méthode.

la trace.

la relation logique entre eux.

---

Puis produire un verdict limité.

---

Brutus créa :

**COUNTERTEST_REVIEW**

avec :

**REVIEW_ID**

**CLAIM_ID**

**CLAIM_VERSION**

**CLAIM_SCOPE**

**COUNTERTEST_ID**

**EXPERIMENT_REF**

**METHOD_REF**

**EVIDENCE_REFS**

**REVIEW_POLICY**

**STATUS**

**TRACE_REF**

---

Puis :

**DECISION_REASON**

---

Très important.

---

Un verdict sans raison devenait seulement une nouvelle étiquette.

---

Brutus écrivit :

**VERDICT WITHOUT REASON ≠ AUDITABLE JUDGMENT.**

---

Il prit un exemple simple.

---

Claim :

\[
\forall n\in\mathbb{N},\ F(n)=0.
\]

---

Countertest :

\[
F(47)=3.
\]

---

Si :

47 appartient au domaine,

la méthode est valide,

la valeur est correctement calculée,

alors la claim universelle tombe.

---

Brutus écrivit :

**ONE VALID COUNTEREXAMPLE CAN REFUTE A UNIVERSAL CLAIM.**

---

Puis immédiatement :

**ONLY IF IT BELONGS TO THE CLAIM DOMAIN.**

---

Voilà.

---

Il changea le scope.

---

Claim :

\[
\forall n<40,\ F(n)=0.
\]

---

Même countertest :

\[
F(47)=3.
\]

---

Brutus secoua la tête.

---

Irrelevant.

---

Il écrivit :

**VALID FACT OUTSIDE SCOPE ≠ COUNTEREXAMPLE.**

---

Encore le chapitre 85.

---

Un nombre vrai pouvait être inutile.

---

Le juge devait donc commencer par :

**DOMAIN MATCH.**

---

Brutus créa la première étape.

---

### CHECK 1 — CLAIM IDENTITY

Est-ce la bonne claim ?

---

Pas une version antérieure.

Pas une reformulation différente.

Pas une phrase ressemblante.

---

Il écrivit :

**SIMILAR CLAIM ≠ SAME CLAIM.**

---

Puis :

### CHECK 2 — CLAIM SCOPE

Le contre-test appartient-il réellement au domaine ?

---

### CHECK 3 — INPUT VALIDITY

L’entrée respecte-t-elle les hypothèses ?

---

### CHECK 4 — METHOD VALIDITY

La méthode utilisée mesure-t-elle bien la propriété visée ?

---

### CHECK 5 — EXECUTION INTEGRITY

Le calcul ou l’expérience a-t-il été exécuté correctement ?

---

### CHECK 6 — LOGICAL EFFECT

Si le résultat est accepté, contredit-il réellement la claim ?

---

Brutus regarda la chaîne.

---

Voilà le juge.

---

Pas une voix.

Une série de portes.

---

Il écrivit :

**COUNTERTEST ACCEPTANCE IS MULTI-STAGE.**

---

Puis il pensa aux verdicts.

---

PASS ?

FAIL ?

Trop vague.

---

Il créa :

**COUNTERTEST_REVIEW_STATUS**

VALID_REFUTATION.

VALID_BUT_IRRELEVANT.

METHOD_INVALID.

INPUT_OUT_OF_DOMAIN.

EXECUTION_UNVERIFIED.

CLAIM_MISMATCH.

INCONCLUSIVE.

NEEDS_REPRODUCTION.

REJECTED_AS_ARTIFACT.

---

Brutus sourit.

---

Beaucoup mieux.

---

Un contre-test pouvait être correct comme calcul mais sans effet sur la claim.

---

Il écrivit :

**COUNTERTEST VALIDITY ≠ COUNTERTEST RELEVANCE.**

---

Puis :

**RELEVANCE ≠ LOGICAL SUFFICIENCY.**

---

Encore une séparation.

---

Prenons un résultat numérique.

---

Claim :

« l’algorithme retourne toujours un entier pair ».

---

Observation :

sur 10 000 entrées, tous les résultats sont pairs.

---

Est-ce un contre-test ?

---

Non.

---

C’est du support expérimental.

---

Brutus écrivit :

**PASSING CASES ≠ COUNTEREXAMPLE.**

---

Puis :

**MANY CONFIRMATIONS DO NOT SUBSTITUTE FOR ONE REQUIRED DISPROOF CONDITION.**

---

Très important.

---

Le juge devait donc connaître le type de claim.

---

Il reprit :

**CLAIM_TYPE**

UNIVERSAL.

FINITE_DOMAIN.

STATISTICAL.

OPERATIONAL.

HEURISTIC.

---

Puis il écrivit :

**COUNTERTEST LOGIC DEPENDS ON CLAIM TYPE.**

---

Pour une claim universelle :

un cas valide contradictoire peut suffire.

---

Pour une claim statistique :

un seul cas atypique ne suffit pas forcément.

---

Pour une claim opérationnelle :

un échec peut suffire à montrer que la garantie absolue est fausse, mais pas nécessairement que le système est inutilisable.

---

Brutus écrivit :

**THE SAME OBSERVATION CAN HAVE DIFFERENT LOGICAL WEIGHT AGAINST DIFFERENT CLAIMS.**

---

Voilà.

---

Il pensa à une formulation dangereuse.

---

Claim :

« cette méthode fonctionne bien ».

---

Le juge se figea.

---

Que veut dire :

bien ?

---

Brutus écrivit :

**UNDEFINED CLAIM CANNOT RECEIVE PRECISE COUNTERTEST JUDGMENT.**

---

Très important.

---

Le juge devait parfois refuser de juger.

---

Il créa :

**CLAIM_NOT_TESTABLE_AS_WRITTEN.**

---

Pas FAIL.

---

La claim elle-même était insuffisamment définie.

---

Brutus sourit.

---

Le juge pouvait donc protéger le banc contre des questions mal posées.

---

Puis il pensa à L8.

---

Relation :

\[
Q_q=\frac{P_{q^2}}{P_q}
\]

pour \(q\) premier impair.

---

Si quelqu’un trouve un q où le quotient n’est pas entier…

quel effet ?

---

Cela dépend de la claim exacte.

---

Si la claim dit :

« le quotient est entier pour tout premier impair q »,

un seul q valide suffit à réfuter cette version universelle.

---

Mais si L8 n’est encore qu’un objet de recherche dont certaines propriétés restent en examen…

le même résultat doit frapper la propriété précise, pas « L8 entière ».

---

Brutus écrivit :

**COUNTEREXAMPLE TARGETS A CLAIM, NOT A NAME.**

---

Très important.

---

Une formule pouvait survivre après qu’une propriété particulière soit réfutée.

---

Il ajouta :

**OBJECT SURVIVAL ≠ CLAIM SURVIVAL.**

---

Puis il pensa aux portes 71 et 83.

---

Supposons qu’un calcul échoue.

---

Le juge devait demander :

est-ce une vraie obstruction mathématique ?

---

Ou :

mauvaise représentation ?

timeout ?

overflow ?

mauvais modulus ?

mauvais candidat ?

---

Brutus écrivit :

**COMPUTATION FAILURE ≠ MATHEMATICAL COUNTEREXAMPLE.**

---

Encore le chapitre 104.

---

Il créa :

**FAILURE_CLASSIFICATION**

TOOL_FAILURE.

RESOURCE_FAILURE.

PROTOCOL_FAILURE.

NUMERIC_FAILURE.

DOMAIN_FAILURE.

LOGICAL_COUNTEREXAMPLE.

---

Voilà.

---

Un écran rouge ne devait pas tuer une conjecture.

---

Il pensa à Number.

---

JavaScript Number retourne un résultat faux pour un énorme entier.

---

Cela ne réfute pas la formule mathématique.

---

Cela réfute éventuellement :

**l’implémentation Number est suffisamment exacte pour ce domaine.**

---

Brutus écrivit :

**IMPLEMENTATION COUNTEREXAMPLE ≠ MATHEMATICAL COUNTEREXAMPLE.**

---

Très important.

---

Un bug pouvait frapper :

le code,

pas la théorie.

---

Ou l’inverse.

---

Le juge devait savoir lequel.

---

Il ajouta :

**TARGET_LAYER**

MATHEMATICAL_CLAIM.

ALGORITHM.

IMPLEMENTATION.

PROTOCOL.

RUNTIME.

UI.

---

Brutus sourit.

---

Enfin.

---

Une panne d’interface ne pourrait plus se déguiser en panne mathématique.

---

Il écrivit :

**COUNTERTEST MUST NAME THE LAYER IT ATTACKS.**

---

Puis il pensa au Recto.

---

Une animation montre une fourmi au mauvais endroit.

---

Counterexample contre quoi ?

---

Peut-être :

renderer fidelity.

---

Pas :

runtime state.

---

Si la source autoritative indique la bonne position.

---

Brutus écrit :

**DISPLAY ERROR ≠ WORLD-STATE ERROR.**

---

Encore une frontière.

---

Puis il pensa aux tests indépendants.

---

Un contre-test produit par le même code que le résultat initial.

---

Acceptable comme premier signal.

---

Mais parfois insuffisant pour conclure à un bug réel.

---

Il créa :

**COUNTERTEST_CONFIDENCE_PATH**

CANDIDATE.

REPRODUCED.

INDEPENDENTLY_REPRODUCED.

VALIDATED_FOR_CLAIM.

---

Puis il se méfia du mot confidence.

---

Il remplaça :

**COUNTERTEST_VALIDATION_STAGE.**

---

Mieux.

---

Il écrivit :

**STAGE ≠ PROBABILITY.**

---

Toujours éviter les faux pourcentages.

---

Puis il prit un contre-exemple candidat.

---

Run 1.

Failure.

---

Run 2.

Same implementation.

Failure.

---

Run 3.

Independent implementation.

Pass.

---

Que faire ?

---

Brutus écrivit :

**DISAGREEMENT BETWEEN METHODS ≠ REFUTATION.**

---

Status :

INCONCLUSIVE.

---

Need investigate method discrepancy.

---

Il créa :

**METHOD_CONFLICT.**

---

Très important.

---

Le juge ne devait pas choisir la méthode préférée par goût.

---

Il devait vérifier :

spec.

inputs.

numeric model.

assumptions.

---

Brutus écrivit :

**WHEN METHODS DISAGREE, AUDIT THE CONTRACT BEFORE CROWNING ONE.**

---

Voilà.

---

Puis il pensa aux témoins.

---

Un énorme objet calculé.

---

Hash correct.

---

Mais mauvaise formule source.

---

Le juge devait distinguer :

integrity pass.

semantic relevance fail.

---

Il écrivit :

**VALID OBJECT ≠ VALID COUNTERTEST FOR THIS CLAIM.**

---

Encore.

---

Le chapitre 82 revenait.

---

Puis il pensa au q47 witness.

---

Un witness valide pour q47.

---

Peut-il servir comme countertest sur q71 ?

---

Seulement si une relation logique explicite le permet.

---

Sinon :

VALID_BUT_IRRELEVANT.

---

Brutus écrivit :

**A STRONG WITNESS FOR THE WRONG CLAIM IS STILL THE WRONG EVIDENCE.**

---

Il sourit.

---

Voilà une phrase à garder.

---

Puis il pensa aux statistiques.

---

Un modèle prévoit une moyenne.

Une observation diffère légèrement.

---

Est-ce un contre-test ?

---

Pas automatiquement.

---

Il faut :

null model.

expected variance.

sample size.

predeclared criterion.

---

Brutus écrivit :

**DEVIATION ≠ REFUTATION WITHOUT A TOLERANCE OR ERROR MODEL.**

---

Très important.

---

Le chapitre 90 revenait.

---

La poussière :

\[
-0.035518...
\]

---

Petit écart.

---

Pas contre-exemple en soi.

---

Il faut savoir ce que le modèle prédit exactement.

---

Brutus écrivit :

**RESIDUAL NEEDS A MODEL OF EXPECTED RESIDUALS.**

---

Puis il pensa aux seuils.

---

Si le critère est choisi après voir la donnée…

dangereux.

---

Il ajouta :

**COUNTERTEST THRESHOLD SHOULD BE PREDECLARED WHEN POSSIBLE.**

---

Encore le banc.

---

Le juge devait vérifier :

criterion before result?

or post-hoc?

---

Il créa :

**THRESHOLD_ORIGIN**

PRECOMMITTED.

DERIVED_FROM_STANDARD.

POST_HOC.

UNKNOWN.

---

Brutus écrit :

**POST-HOC THRESHOLD WEAKENS INTERPRETATION.**

---

Pas nécessairement invalide.

Mais doit être visible.

---

Puis il pensa aux preuves exactes.

---

Dans certains domaines mathématiques, le contre-exemple peut être exact.

---

Pas de p-value.

Pas de tolerance.

---

Exemple :

une identité prétend \(A=B\).

Calcul exact donne \(A\neq B\).

---

Alors le juge peut produire :

**VALID_REFUTATION**

si le domaine et la méthode sont exacts.

---

Brutus écrivit :

**EXACT CLAIMS MAY ADMIT EXACT COUNTEREXAMPLES.**

---

Puis :

**APPROXIMATE CLAIMS NEED APPROXIMATE CONTRACTS.**

---

Très bon.

---

Il pensa aux flottants.

---

A = 1.0000000001.

B = 1.

---

Différents mathématiquement.

Mais peut-être équivalents sous tolerance du protocole.

---

Brutus écrit :

**FLOAT DIFFERENCE ≠ PROTOCOL FAILURE UNTIL TOLERANCE IS APPLIED.**

---

Le chapitre 78 encore.

---

Puis il pensa aux contre-tests adversariaux.

---

Le juge pouvait demander :

le contre-test a-t-il été construit spécialement après avoir vu une faiblesse ?

---

Ce n’était pas mauvais.

---

Au contraire.

---

Mais l’interprétation change.

---

Il créa :

**COUNTERTEST_ORIGIN**

RANDOM.

SYSTEMATIC.

ADVERSARIAL.

DISCOVERED_INCIDENTALLY.

DERIVED_FROM_FAILURE.

---

Brutus écrivit :

**ADVERSARIAL DOES NOT MEAN INVALID.**

---

Très important.

---

Chercher activement à casser une claim est une bonne pratique.

---

Mais un test adversarial doit respecter le domaine.

---

Il ajouta :

**ADVERSARIAL INPUT OUTSIDE DOMAIN ≠ REFUTATION.**

---

Puis il pensa à CT-04.

---

Adversarial failure search.

---

Le juge pouvait enregistrer :

CT-04 completed.

No valid counterexample found in tested domain.

---

Mais pas :

theorem proven.

---

Brutus écrivit :

**COUNTERTEST CAMPAIGN PASS ≠ UNIVERSAL PROOF.**

---

Voilà.

---

Puis il pensa à CT-01 et CT-03.

---

Un juge ne devait pas déclarer le dossier complet si certains contrôles requis restaient ouverts.

---

Il créa :

**REVIEW_DEPENDENCY_SET**

---

CT-01.

CT-02.

CT-03.

CT-04.

---

Puis :

status per dependency.

---

Brutus écrivit :

**PARTIAL COUNTERTEST COVERAGE ≠ COMPLETE VALIDATION.**

---

Très important.

---

Le dossier pouvait être :

strongly explored.

Mais toujours incomplete.

---

Il refusa les adjectifs vagues.

---

Il écrivit :

**REPORT WHICH TESTS ARE COMPLETE.**

---

Pas :

“very solid”.

---

Le juge devait décrire.

---

Puis il pensa au nom :

JUDGE.

---

Le mot pouvait encourager une illusion d’autorité.

---

Il créa une règle.

---

**JUDGE OUTPUT = REVIEW DECISION**

---

Pas :

truth verdict.

---

Il écrivit :

**JUDGE DOES NOT DECIDE REALITY.**

**JUDGE DECIDES WHETHER EVIDENCE SATISFIES REVIEW CONTRACT.**

---

Voilà.

---

Exactement comme Verso.

---

Verso :

permission contract.

Judge :

countertest contract.

---

Deux gardiens.

Deux scopes.

---

Brutus écrivit :

**GUARD ≠ JUDGE.**

Puis :

**JUDGE ≠ AUTHORITY GATE.**

---

Très important.

---

Le Judge pouvait conclure :

VALID_REFUTATION.

---

Mais c’était encore à la promotion / status machinery de mettre à jour la claim officielle.

---

Il dessina :

\[
\text{COUNTERTEST}
\rightarrow
\text{JUDGE REVIEW}
\rightarrow
\text{REVIEW DECISION}
\rightarrow
\text{STATUS CHANGE REQUEST}
\rightarrow
\text{AUTHORITY}
\]

---

Pas :

\[
\text{JUDGE}
\rightarrow
\text{DIRECT WORLD MUTATION}.
\]

---

Il barra encore.

---

Brutus écrivit :

**JUDGE OUTPUT IS EVIDENCE FOR STATE TRANSITION, NOT THE TRANSITION ITSELF.**

---

Excellent.

---

Puis il pensa aux appels.

---

Et si le Judge se trompe ?

---

Il devait être révisable.

---

Brutus créa :

**REVIEW_APPEAL**

---

Pas comme drame juridique.

---

Comme nouveau review.

---

Different method.

New evidence.

Corrected scope.

---

Il écrit :

**REVIEW DECISION MUST BE CHALLENGEABLE.**

---

Très important.

---

Une mauvaise décision du Judge pouvait être corrigée sans effacer l’ancienne.

---

Le registre conserverait :

Review v1.

Appeal.

Review v2.

---

Brutus écrit :

**JUDGMENT HISTORY ≠ FINALITY.**

---

Puis il pensa aux conflits.

---

Judge A :

VALID_REFUTATION.

Judge B :

METHOD_INVALID.

---

Que faire ?

---

Pas voter.

---

Il écrit :

**REVIEW CONFLICT ≠ MAJORITY PROBLEM.**

---

Le système doit chercher :

why different?

---

Different claim version?

Different evidence?

Different method?

Different review policy?

---

Il créa :

**REVIEW_DIFF**

---

CLAIM_DIFF.

EVIDENCE_DIFF.

POLICY_DIFF.

METHOD_DIFF.

INTERPRETATION_DIFF.

---

Brutus sourit.

---

Un désaccord pouvait maintenant être disséqué.

---

Puis il pensa à plusieurs joueurs jouant le Judge.

---

Astra.

Muse.

Grok.

Antigravity.

---

Quatre reviews.

---

Même principe.

---

Le nombre d’accords n’établit pas la vérité.

---

Il écrit :

**FOUR JUDGES CAN SHARE ONE MISTAKE.**

---

Puis :

**CONSENSUS MAY TRIGGER CONFIDENCE IN REVIEW PROCESS, NOT REPLACE EVIDENCE.**

---

Il se corrigea encore.

---

Le mot confidence.

---

Il remplaça :

**CONSENSUS MAY PRIORITIZE OR CLOSE REVIEW UNDER POLICY, BUT DOES NOT CREATE MATHEMATICAL PROOF.**

---

Mieux.

---

Puis il pensa aux erreurs de typage.

---

Un counterexample attaché à mauvais CLAIM_ID.

---

Même si le texte semble correspondre.

---

Reject.

---

Brutus écrit :

**CLAIM IDENTITY MUST BE MACHINE-CHECKED BEFORE SEMANTIC REVIEW.**

---

Puis :

**HUMAN-READABLE TITLE IS NOT ENOUGH.**

---

Encore les identités.

---

Puis il pensa aux versions.

---

Claim v1 :

all q.

Claim v2 :

all q except 47.

---

Counterexample q47.

---

Refutes v1.

Not v2.

---

Brutus écrit :

**COUNTEREXAMPLE EFFECT IS VERSIONED.**

---

Très important.

---

Une ancienne réfutation ne frappe pas automatiquement une claim révisée.

---

Mais elle peut expliquer pourquoi la révision existe.

---

Il ajoute :

**REVISION_REASON_REF.**

---

Voilà.

---

Puis il pensa au danger inverse.

---

Réviser constamment la claim pour éviter tous les contre-exemples.

---

Une formule universelle devient :

tous sauf 47.

Puis tous sauf 47 et 71.

Puis tous sauf 47,71,83…

---

À un moment, on doit reconnaître le pattern.

---

Brutus écrit :

**PATCHING CLAIM AFTER EACH FAILURE MAY CHANGE THE RESEARCH QUESTION.**

---

Puis :

**REVISION HISTORY MUST REMAIN VISIBLE.**

---

Très important.

---

Le système pouvait détecter :

scope shrinking repeatedly.

---

Pas pour interdire.

Pour signaler.

---

Il créa :

**CLAIM_DRIFT_FLAG.**

---

Brutus sourit.

---

Un juge devait parfois dire :

le problème n’est plus le contre-test.

La claim a changé cinq fois.

---

Il écrit :

**MOVING TARGET ≠ SURVIVING TEST.**

---

Très bon.

---

Puis il pensa au Hurst.

---

Une analyse montre une pente sur log-log.

---

Countertest :

shuffle destroys relation.

---

Le juge demande :

était-ce attendu sous la méthode ?

---

Positive control?

Negative control?

Scale selection?

---

Il écrit :

**CONTROL FAILURE CAN INVALIDATE INTERPRETATION WITHOUT REFUTING RAW DATA.**

---

Encore la séparation.

---

Data exists.

Interpretation dies.

---

Puis le 369/396.

---

Quelqu’un observe un beat de 27 Hz.

---

Countertest :

change pair to 300/327.

Beat still 27.

---

Effet ?

---

Cela réfute peut-être l’idée que 27 identifie spécifiquement le couple 369/396.

---

Mais pas la formule de différence.

---

Brutus écrit :

**SAME FEATURE IN ANOTHER PAIR COUNTERTESTS UNIQUENESS, NOT ARITHMETIC.**

---

Voilà.

---

Le Judge devait reconnaître la propriété réellement visée.

---

Puis il pensa aux contre-tests de sécurité.

---

Supposons :

API denies unauthorized action.

Good.

---

One malformed request gets through.

---

If claim is :

“all unauthorized requests are denied under policy X”,

one valid bypass refutes the claim.

---

Mais il se retint.

---

Le chapitre restait général.

---

Il écrit simplement :

**SECURITY GUARANTEES ARE CLAIMS TOO.**

---

Et :

**A VALID BYPASS COUNTERTESTS THE GUARANTEE, NOT NECESSARILY THE ENTIRE SYSTEM.**

---

Très important.

---

Puis il construisit la première fiche complète.

---

**REVIEW-0001**

Claim:

C-71-001.

Claim version:

3.

Type:

UNIVERSAL_WITHIN_DECLARED_DOMAIN.

Countertest:

CT-71-004.

---

Check 1:

Claim identity.

PASS.

---

Check 2:

Scope.

PASS.

---

Check 3:

Input assumptions.

PASS.

---

Check 4:

Method.

PASS.

---

Check 5:

Execution integrity.

PASS.

---

Check 6:

Logical contradiction.

FAIL.

---

Pourquoi ?

---

Le résultat n’était pas réellement contraire à la claim.

---

Brutus sourit.

---

Voilà un cas parfait.

---

Un contre-test peut passer cinq checks et pourtant ne pas réfuter.

---

Status :

**VALID_BUT_NON_REFUTING.**

---

Il ajouta ce statut.

---

Très important.

---

Le système avait évité une fausse mort.

---

Puis deuxième fiche.

---

Same claim.

New countertest.

---

All checks pass.

Logical contradiction pass.

---

Status:

**VALID_REFUTATION.**

---

Brutus resta silencieux.

---

Le Judge n’avait pas crié.

---

Pas de musique.

---

Seulement :

claim contradicted under current version and scope.

---

Brutus écrit :

**REFUTATION SHOULD BE BORING WHEN IT IS CLEAN.**

---

La même philosophie que Verso.

---

Les parties critiques n’avaient pas besoin de théâtre.

---

Puis il pensa au chapitre 104.

---

Une fois VALID_REFUTATION obtenue :

l’idée peut entrer dans CLOSED RESEARCH OBJECTS.

---

Mais encore :

via explicit transition.

---

Brutus écrit :

**JUDGE REVIEW → DISPOSITION REQUEST.**

---

Le système reste modulaire.

---

Puis il pensa au prochain chapitre.

---

Si le Judge sait examiner un contre-test…

alors il faut aussi un endroit où les idées qui survivent peuvent être promues.

---

Pas directement vers la vérité.

---

Mais vers un statut plus fort.

---

Brutus regarda Verso.

Puis le Judge.

Puis les cartes.

---

Il ouvrit un nouveau dossier.

---

**PROMOTION GATE**

---

Puis écrivit :

# LA PORTE DE PROMOTION

---

Mais avant de quitter le Judge, il voulait fixer ses règles.

---

Il sauvegarda :

**COUNTERTEST JUDGE v1**

---

Le Journal Vivant nota :

Review targets claim identity and version.

Scope checked before logic.

Method failure separated from claim refutation.

Implementation failures separated from mathematical counterexamples.

Claim type determines countertest effect.

Exact and approximate claims use different review contracts.

Judge outputs review decisions, not world mutations.

Appeals preserve previous judgments.

Review conflicts are decomposed, not voted away.

Claim drift tracked.

---

Brutus ajouta les invariants :

**JUDGE ≠ ORACLE.**

**COUNTERTEST TARGETS A CLAIM, NOT A NAME.**

**VALID FACT OUTSIDE SCOPE ≠ COUNTEREXAMPLE.**

**COMPUTATION FAILURE ≠ MATHEMATICAL COUNTEREXAMPLE.**

**IMPLEMENTATION COUNTEREXAMPLE ≠ MATHEMATICAL COUNTEREXAMPLE.**

**COUNTERTEST VALIDITY ≠ COUNTERTEST RELEVANCE.**

**COUNTERTEST CAMPAIGN PASS ≠ UNIVERSAL PROOF.**

**JUDGE OUTPUT ≠ STATE TRANSITION.**

**MOVING TARGET ≠ SURVIVING TEST.**

---

Puis il regarda les trois objets devant lui.

---

La claim.

Le contre-test.

Le jugement.

---

Trois choses différentes.

---

Aucune ne devait absorber les deux autres.

---

Le Judge avait appris à dire :

oui, ce coup touche.

non, ce coup manque.

ce coup frappe le mauvais objet.

ce coup est peut-être réel mais la méthode n’est pas encore fiable.

---

Et parfois :

je ne peux pas trancher.

---

Brutus sourit.

---

C’était probablement la phrase la plus importante qu’un juge puisse savoir prononcer.

---

**INCONCLUSIVE.**

---

Pas une faiblesse.

Un état.

---

Puis il regarda la porte suivante.

---

Une idée venait parfois de survivre au banc.

Au contre-test.

À la revue.

---

Elle ne devenait pas encore une preuve.

---

Mais peut-être qu’elle méritait de changer de statut.

---

Brutus posa la main sur le nouveau dossier.

---

# LA PORTE DE PROMOTION

---

Au-dessus, il écrivit :

**SURVIVING TESTS DOES NOT GIVE AN IDEA THE RIGHT TO PROMOTE ITSELF.**

---

Puis il ferma le Judge.

---

Le prochain chapitre allait décider non pas ce qui est vrai…

mais ce qui a gagné le droit d’être considéré plus sérieusement.
