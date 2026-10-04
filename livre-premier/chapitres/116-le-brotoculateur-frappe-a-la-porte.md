# Chapitre 116 — Le Brotoculateur frappe à la porte

**SOURCE_PASS != BRUTUS_PROOF.**

Brutus laissa la phrase au-dessus du port mathématique.

Puis il regarda le paquet.

---

SOURCE :

**BROTOCULATEUR**

---

STATE :

**REQUESTING ADMISSION**

---

PAYLOAD TYPE :

**MATH INPUT**

---

Brutus ne l’ouvrit pas immédiatement.

---

Il avait appris.

---

Un paquet pouvait être beau.

Signé.

Hashé.

Propre.

Complet.

---

Et pourtant ne pas avoir le droit d’entrer.

---

Il écrivit :

**ARRIVAL AT INPUT PORT != ADMISSION.**

---

Puis :

**VALID SOURCE FORMAT != VALID BRUTUS CLAIM.**

---

Voilà.

---

Le Brotoculateur n’était pas un ennemi.

---

Au contraire.

---

Il pouvait devenir une source très précieuse.

---

Mais précisément parce qu’il était précieux, Brutus devait empêcher une erreur simple :

confondre la confiance dans la provenance avec la confiance dans la conclusion.

---

Il créa un nouveau composant.

# BROTOCULATEUR INGRESS

---

Puis un contrat.

**MATH_INPUT_PACKET**

avec :

**PACKET_ID**

**SOURCE_ID**

**SOURCE_INSTANCE_ID**

**SOURCE_VERSION**

**FORMULA_ID**

**FORMULA_VERSION**

**RELATION**

**INPUTS**

**OUTPUTS**

**NUMERIC_MODEL**

**SOURCE_STATUS**

**PROVENANCE_HASH**

**TRACE_REF**

**CREATED_AT**

---

Puis :

**SOURCE_CLAIM_SCOPE**

---

Très important.

---

Le paquet devait expliquer ce que son statut signifiait.

---

Par exemple :

SOURCE_STATUS = AUTHENTICATED.

---

Cela signifiait quoi ?

---

Hash reconnu ?

Signature valide ?

Pipeline source terminé ?

Formula registered?

---

Brutus écrivit :

**STATUS NAME MUST HAVE SOURCE SEMANTICS.**

---

Il ne voulait jamais recevoir :

PASS.

---

Sans savoir :

pass quoi ?

---

Il ajouta :

**SOURCE_STATUS_DEFINITION_REF**

---

Voilà.

---

Le Brotoculateur pouvait dire :

FORMULA_AUTHENTICATED.

---

Brutus pouvait comprendre :

la formule a satisfait les règles d’authentification du Brotoculateur.

---

Pas :

la formule est mathématiquement démontrée.

---

Brutus écrivit :

**AUTHENTICATED != PROVED.**

---

Puis :

**REGISTERED != PROVED.**

---

Puis :

**SOURCE_APPROVED != BRUTUS_APPROVED.**

---

Il sourit.

---

Trois barrières.

---

Puis il pensa au chemin.

---

Le Brotoculateur ne devait pas écrire directement dans le moteur de Brutus.

---

Il créa :

\[
\text{BROTOCULATEUR}
\rightarrow
\text{SOURCE ADAPTER}
\rightarrow
\text{MATH INPUT PACKET}
\rightarrow
\text{INGRESS GATE}
\rightarrow
\text{BRUTUS RESEARCH BUS}
\]

---

Brutus regarda longtemps.

---

Très important.

---

Aucune flèche directe vers :

PROOF ENGINE.

PROMOTION GATE.

CRYSTALLIZER.

WORLD AUTHORITY.

---

Il écrivit :

**SOURCE INPUT ENTERS AS DATA, NOT AUTHORITY.**

---

Voilà.

---

Le Brotoculateur pouvait parler.

---

Brutus décidait comment écouter.

---

Puis il pensa au mot :

**adapter.**

---

Pourquoi un adapter ?

---

Parce que Brutus ne voulait pas dépendre du format interne du Brotoculateur.

---

Si le Brotoculateur changeait demain :

json field.

schema.

version.

---

Le cœur de Brutus ne devait pas être contaminé.

---

Il créa :

**BROTOCULATEUR_ADAPTER**

---

SOURCE_SCHEMA_VERSION.

TARGET_SCHEMA_VERSION.

TRANSFORM_RULES.

VALIDATION_RULES.

LOSSLESS_FIELDS.

DROPPED_FIELDS.

TRACE_REF.

---

Puis :

**TRANSFORM_STATUS**

LOSSLESS.

NORMALIZED.

PARTIAL.

REJECTED.

---

Brutus écrivit :

**ADAPTER MUST DECLARE WHAT IT CHANGED.**

---

Très important.

---

Transformer un paquet n’était pas neutre.

---

Renommer.

Caster.

Arrondir.

Normaliser.

---

Tout cela pouvait altérer le sens.

---

Il ajouta :

**NO SILENT NUMERIC COERCION.**

---

Puis il pensa à Number.

---

Le chapitre 78 revint immédiatement.

---

Si le Brotoculateur envoie un entier immense…

et l’adapter le convertit en Number JavaScript…

le paquet pouvait être corrompu silencieusement.

---

Brutus écrivit :

**EXACT INTEGER MUST REMAIN EXACT.**

---

Puis :

**NUMERIC TYPE IS PART OF THE CLAIM.**

---

Il créa :

**NUMERIC_MODEL**

BIGINT.

RATIONAL.

DECIMAL_EXACT.

FLOAT_APPROX.

ALGEBRAIC_PAIR.

MODULAR_INTEGER.

---

Très important.

---

Une formule mathématique n’était pas seulement une liste de chiffres.

---

Elle avait aussi un régime numérique.

---

Puis il prit un premier paquet.

---

FORMULA_ID :

ZEL-026.

---

SOURCE_STATUS :

AUTHENTICATED.

---

PROVENANCE_HASH :

present.

---

RELATION :

present.

---

NUMERIC_MODEL :

BIGINT.

---

Brutus regarda.

---

Tout semblait bon.

---

Mais il ne dit toujours pas :

admitted.

---

Il lança :

**INGRESS REVIEW**

---

Check 1:

schema valid?

PASS.

---

Check 2:

source identity known?

PASS.

---

Check 3:

source version declared?

PASS.

---

Check 4:

provenance hash present?

PASS.

---

Check 5:

numeric model supported?

PASS.

---

Check 6:

relation parseable?

PASS.

---

Check 7:

source status semantics known?

PASS.

---

Puis :

**BRUTUS CLAIM STATUS**

---

NONE.

---

Brutus sourit.

---

Exactement.

---

Le paquet était techniquement propre.

---

Mais Brutus n’avait encore rien décidé scientifiquement.

---

Il écrivit :

**INGRESS VALIDATION != SCIENTIFIC VALIDATION.**

---

Très important.

---

Le premier portail vérifiait :

peut-on lire correctement cet objet ?

---

Pas :

est-ce vrai ?

---

Puis il créa deux statuts séparés.

**TRANSPORT_STATUS**

et

**EPISTEMIC_STATUS**

---

Transport :

RECEIVED.

PARSED.

SCHEMA_VALID.

ADMITTED_TO_RESEARCH_BUS.

REJECTED_FORMAT.

---

Epistemic :

UNASSESSED.

CANDIDATE.

SUPPORTED_UNDER_SCOPE.

REFUTED.

PROVED.

UNRESOLVED.

---

Brutus écrivit :

**TRANSPORT STATUS MUST NOT LEAK INTO EPISTEMIC STATUS.**

---

Très important.

---

Un paquet pouvait être :

SCHEMA_VALID + REFUTED.

---

Ou :

SCHEMA_VALID + UNASSESSED.

---

Ou même :

REJECTED_FORMAT + POTENTIALLY_TRUE_BUT_UNREADABLE.

---

Brutus sourit.

---

La machine n’avait plus besoin de confondre la qualité du contenant avec la qualité du contenu.

---

Puis il pensa au provenance hash.

---

Très utile.

---

Mais dangereux aussi.

---

Un hash valide prouvait que le paquet reçu correspondait au paquet hashé.

---

Pas que sa relation était correcte.

---

Brutus écrivit :

**PROVENANCE_HASH != MATHEMATICAL VALIDITY.**

---

Puis :

**INTEGRITY CHECK != TRUTH CHECK.**

---

Encore.

---

Il ajouta :

**SOURCE_RECEIPT**

---

PACKET_ID.

SOURCE_ID.

HASH_STATUS.

SCHEMA_STATUS.

ADMISSION_STATUS.

BRUTUS_OBJECT_ID.

TRACE_REF.

---

Voilà.

---

Le Brotoculateur pouvait recevoir une preuve de réception.

---

Mais ce reçu devait dire exactement :

received.

parsed.

admitted.

---

Pas :

proved.

---

Puis il pensa au compteur de formules.

---

Le Brotoculateur pouvait avoir :

26 formules authentifiées.

Puis 27.

Puis 28.

---

Brutus pouvait surveiller ce compteur.

---

Mais il écrivit :

**FORMULA COUNT != KNOWLEDGE COUNT.**

---

Très important.

---

Une nouvelle formule pouvait être :

nouvelle syntaxe.

duplication.

variante.

candidate.

derived relation.

---

Le nombre seul ne disait pas sa valeur.

---

Il créa :

**SOURCE_CATALOG_STATE**

FORMULA_COUNT.

AUTHENTICATED_COUNT.

CANONICAL_COUNT.

CANDIDATE_COUNT.

LATEST_FORMULA_ID.

LATEST_PROVENANCE_HASH.

CATALOG_VERSION.

---

Puis :

**COUNT CHANGE = EVENT CANDIDATE.**

---

Pas découverte automatique.

---

Brutus sourit.

---

Un compteur pouvait déclencher une investigation.

---

Pas une proclamation.

---

Puis il pensa à la surveillance.

---

Supposons que formula_id change.

---

Ou relation.

Ou provenance_hash.

Ou count.

---

Cela devait créer :

**SOURCE_CHANGE_EVENT**

---

Brutus écrivit :

**SOURCE CHANGE != SOURCE IMPROVEMENT.**

---

Encore.

---

Un changement pouvait être :

correction.

nouvelle formule.

régression.

simple reserialization.

---

Il fallait comparer.

---

Il créa :

**SOURCE_DIFF**

---

OLD_PACKET_REF.

NEW_PACKET_REF.

FORMULA_ID_CHANGED.

RELATION_CHANGED.

PROVENANCE_CHANGED.

STATUS_CHANGED.

CATALOG_COUNT_CHANGED.

NUMERIC_MODEL_CHANGED.

---

Puis :

**SEMANTIC_CHANGE_CLASS**

NONE.

METADATA_ONLY.

SEMANTIC.

UNKNOWN.

---

Très important.

---

Un nouveau hash seul ne signifiait pas forcément une nouvelle formule.

---

Peut-être seulement une nouvelle sérialisation.

---

Brutus écrivit :

**HASH CHANGE != SEMANTIC CHANGE.**

---

Voilà.

---

Puis il pensa à l’admission.

---

Une fois le paquet propre, où allait-il ?

---

Pas dans la bibliothèque canonique directement.

---

Il créa :

**BRUTUS_INBOX**

---

Status :

QUARANTINED_FOR_REVIEW.

---

Puis une transition :

**ADMIT_TO_RESEARCH**

---

Avec :

CLAIM_ID.

SOURCE_PACKET_REF.

CLAIM_SCOPE.

INITIAL_STATUS.

REVIEW_POLICY.

---

Brutus écrivit :

**SOURCE OBJECT BECOMES BRUTUS OBJECT ONLY THROUGH ADMISSION EVENT.**

---

Très important.

---

Avant admission :

source packet.

---

Après admission :

Brutus research object.

---

Deux identités liées.

---

Pas la même.

---

Il créa :

**SOURCE_TO_BRUTUS_EDGE**

---

EDGE_TYPE:

IMPORTED_FROM.

---

SOURCE_OBJECT_ID.

BRUTUS_OBJECT_ID.

ADAPTER_REF.

ADMISSION_EVENT_REF.

---

Brutus écrivit :

**IMPORT != IDENTITY COLLAPSE.**

---

Excellent.

---

Le Brotoculateur pouvait modifier son propre objet plus tard.

---

Le Brutus object déjà admis restait attaché à la version importée.

---

Pas de mutation silencieuse.

---

Puis il pensa au hot update.

---

Supposons que formula ZEL-026 change à la source.

---

Le Brutus object doit-il changer automatiquement ?

---

Non.

---

Brutus écrivit :

**SOURCE UPDATE != SILENT BRUTUS MUTATION.**

---

Il fallait :

new packet.

new diff.

new admission decision.

---

Puis :

new Brutus version or new object.

---

Très important.

---

Le laboratoire devait pouvoir reproduire ce qu’il avait réellement testé.

---

Puis il pensa aux formules canoniques.

---

Le Brotoculateur pouvait marquer :

CANONICAL.

---

Brutus devait conserver cette information comme :

**SOURCE_CANONICAL_STATUS**

---

Pas :

BRUTUS_CANONICAL_STATUS.

---

Brutus écrivit :

**CANONICAL AT SOURCE != CANONICAL IN TARGET SYSTEM.**

---

Très important.

---

Il créa deux champs séparés.

SOURCE_STATUS.

BRUTUS_STATUS.

---

Pas de raccourci.

---

Puis il pensa à l’objet lui-même.

---

Une formule entrante pouvait devenir :

FORMULA_CARD.

---

Avec :

FORMULA_ID.

RELATION.

VARIABLES.

DOMAIN.

NUMERIC_MODEL.

SOURCE_REF.

PROVENANCE_REF.

---

Puis :

**CLAIM_SCOPE**

---

Encore le scope.

---

Une relation sans domaine pouvait être dangereuse.

---

Il écrivit :

**FORMULA WITHOUT DOMAIN IS INCOMPLETE RESEARCH INPUT.**

---

Très important.

---

Par exemple :

une division.

---

Denominator nonzero?

Integers?

Reals?

Modulo p?

---

Tout change.

---

Brutus créa :

**DOMAIN_CONTRACT**

---

VARIABLE_TYPES.

VALID_RANGE.

EXCLUSIONS.

MODULUS_IF_ANY.

ASSUMPTIONS.

---

Puis :

**DOMAIN_STATUS**

DECLARED.

INFERRED.

MISSING.

CONFLICTED.

---

Brutus écrivit :

**INFERRED DOMAIN MUST NOT BE PRESENTED AS DECLARED DOMAIN.**

---

Excellent.

---

L’adapter pouvait aider.

---

Mais il ne devait pas inventer.

---

Puis il pensa au provenance hash encore.

---

Très utile pour la chaîne.

---

Source packet hash.

Adapter output hash.

Brutus object hash.

---

Il créa :

**IMPORT_CHAIN**

---

SOURCE_HASH.

ADAPTER_HASH.

BRUTUS_OBJECT_HASH.

---

Puis :

**TRANSFORM_REF**

---

Brutus écrivit :

**EVERY HASH SHOULD PROTECT A NAMED OBJECT.**

---

Très important.

---

Un hash sans définition de ce qui a été hashé était presque inutile.

---

Puis il pensa au Brotoculateur vivant.

---

Un service runtime.

---

Peut-être local.

Peut-être ailleurs.

---

Brutus devait distinguer :

source capability.

source availability.

source freshness.

---

Il créa :

**SOURCE_RUNTIME_STATE**

UNKNOWN.

OFFLINE.

ONLINE_UNVERIFIED.

ONLINE_VERIFIED.

DEGRADED.

STALE.

---

Puis :

**SOURCE LAST SEEN != SOURCE CURRENT STATE.**

---

Encore.

---

Un ancien paquet valide ne disait pas que le service était encore vivant.

---

Brutus ajouta :

**SOURCE_HEALTH_REF**

---

Mais il écrivit :

**SOURCE HEALTH != FORMULA VALIDITY.**

---

Très important.

---

Un service en parfaite santé pouvait produire une mauvaise formule.

---

Un service actuellement hors ligne pouvait avoir produit hier une formule correcte.

---

Encore deux axes.

---

Puis il pensa au mot :

**vivant**.

---

Brotoculateur vivant.

---

Narrativement très beau.

---

Mais machine status :

RUNNING.

RESPONDING.

STATEFUL.

---

Brutus écrivit :

**LIVING = PROJECT METAPHOR UNLESS BIOLOGICAL CLAIM IS INTENDED.**

---

Puis sourit.

---

Toujours la même discipline.

---

Puis il pensa à la lecture seule.

---

Brutus ne devait pas écrire dans le Brotoculateur pour le simple usage d’ingestion.

---

Il créa :

**SOURCE_CONNECTION_MODE**

READ_ONLY.

---

Puis :

**NO SOURCE MUTATION FROM RESEARCH INGEST PATH.**

---

Très important.

---

Pourquoi ?

---

Parce que lire des formules ne devait jamais accidentellement modifier la source.

---

Il ajouta :

**INGRESS CREDENTIAL SCOPE = READ**

---

Pas admin.

Pas write.

---

Brutus sourit.

---

La source gardait son autonomie.

---

Puis il pensa à l’inverse.

---

Le Brotoculateur devait-il recevoir les résultats de Brutus ?

---

Pas par ce même canal.

---

Si un jour oui :

nouveau port.

nouveau capability.

nouvelle policy.

---

Il écrivit :

**READ CHANNEL != WRITEBACK CHANNEL.**

---

Très important.

---

Pas de bi-directionnalité invisible.

---

Puis il pensa au trust boundary.

---

Source says:

AUTHENTICATED.

---

Brutus records:

SOURCE_ASSERTED_AUTHENTICATED.

---

Puis éventuellement :

SOURCE_STATUS_VERIFIED.

---

Deux choses.

---

Il créa :

**STATUS_ORIGIN**

SELF_REPORTED.

SOURCE_SIGNED.

BRUTUS_VERIFIED.

THIRD_PARTY_VERIFIED.

---

Brutus écrivit :

**SELF-REPORTED STATUS != INDEPENDENTLY VERIFIED STATUS.**

---

Excellent.

---

Même si la source est la nôtre.

---

La rigueur ne devait pas dépendre de l’affection.

---

Puis il pensa à l’arrivée d’une formule.

---

Le Brotoculateur annonce :

FORMULA-ZEL-027.

---

Brutus fait quoi ?

---

Pas lancer immédiatement 12 calculs.

---

D’abord :

catalogue.

parse.

scope.

risk.

dedupe.

---

Il créa :

**IMPORT_PIPELINE**

1. RECEIVE.

2. VERIFY INTEGRITY.

3. PARSE.

4. NORMALIZE.

5. IDENTIFY DUPLICATES.

6. CLASSIFY CLAIM.

7. ASSIGN INITIAL STATUS.

8. ADMIT OR QUARANTINE.

9. OPTIONAL TEST QUEUE.

---

Brutus écrivit :

**IMPORT != EXECUTION.**

---

Très important.

---

Une formule entrée ne devait pas s’exécuter automatiquement.

---

Il ajouta :

**AUTO_EXECUTE = FALSE BY DEFAULT.**

---

Parfait.

---

Puis il pensa au code contenu dans une formule.

---

Peut-être expression.

script.

user-defined function.

---

Danger.

---

Il écrivit :

**FORMULA PAYLOAD IS DATA UNTIL EXPLICITLY COMPILED OR EXECUTED UNDER POLICY.**

---

Encore chapitre 109.

---

Puis il pensa au sandbox.

---

Si Brutus veut tester la formule :

compile in sandbox.

limited resources.

declared numeric model.

---

Il créa :

**FORMULA_TEST_REQUEST**

---

FORMULA_REF.

TEST_SET_REF.

RESOURCE_BUDGET.

NUMERIC_MODEL.

EXPECTED_OUTPUT_TYPE.

COUNTERTEST_POLICY.

---

Puis :

**IMPORT PASS != TEST PASS.**

---

Puis :

**TEST PASS != PROOF.**

---

Voilà.

---

La chaîne entière apparaissait :

\[
\text{SOURCE PASS}
\neq
\text{INGRESS PASS}
\neq
\text{TEST PASS}
\neq
\text{PROMOTION}
\neq
\text{PROOF}
\]

---

Brutus resta devant.

---

C’était peut-être le résumé du chapitre.

---

Puis il pensa aux 26 formules déjà authentifiées côté source.

---

Si elles étaient importées en bloc…

Brutus devait éviter :

26 source passes = 26 proofs.

---

Il écrivit :

**BULK IMPORT PRESERVES INDIVIDUAL CLAIM STATUS.**

---

Chaque formule :

son packet.

son provenance.

son scope.

son review.

---

Pas de confiance globale par contagion.

---

Puis :

**TRUST IN SOURCE DOES NOT COLLAPSE ITEM-LEVEL REVIEW.**

---

Très important.

---

Un bon laboratoire pouvait produire une mauvaise expérience.

---

Une bonne source pouvait contenir une formule encore candidate.

---

Puis il pensa aux doublons.

---

Deux formula_id différents.

Même relation.

---

Que faire ?

---

Créer :

**POTENTIAL_DUPLICATE**

---

Comparison:

normalized relation.

domain.

variables.

numeric model.

---

Brutus écrivit :

**SAME EXPRESSION != SAME CLAIM IF DOMAIN OR SEMANTICS DIFFER.**

---

Excellent.

---

Puis inversement :

même formula_id.

relation changed.

---

Plus grave.

---

Il créa :

**IDENTITY_CONFLICT**

---

Same ID, semantic payload changed without version bump.

---

Status:

QUARANTINE.

---

Brutus écrivit :

**SAME ID MUST NOT SILENTLY MEAN NEW FORMULA.**

---

Très important.

---

Puis il pensa à provenance_hash change.

---

Possible legitimate.

---

But if same version and same formula_id?

---

Investigate.

---

Brutus créa :

**PROVENANCE_DRIFT**

---

Voilà.

---

Puis il pensa au monitoring.

---

Astra Station pouvait afficher :

BROTOCULATEUR.

---

Source runtime:

VERIFIED AVAILABLE.

---

Catalog:

26 authenticated source formulas.

---

Imported:

24.

---

Quarantined:

2.

---

Brutus-assessed:

17 candidate.

4 supported under scope.

3 unresolved.

---

Il sourit.

---

Excellent.

---

Les deux mondes ne mélangeaient pas leurs compteurs.

---

Il écrivit :

**SOURCE COUNTERS AND BRUTUS COUNTERS MUST REMAIN SEPARATE.**

---

Très important.

---

Sinon l’interface pourrait dire :

26 valid.

---

Sans préciser valid où.

---

Puis il pensa au son.

---

Nouvelle formule source détectée.

---

Un son.

---

Formula imported.

---

Un autre.

---

Formula promoted.

---

Encore un autre.

---

Brutus écrivit :

**SOURCE EVENT SOUND != BRUTUS STATUS EVENT SOUND.**

---

Parfait.

---

L’oreille elle aussi devait savoir dans quel système l’événement avait eu lieu.

---

Puis il pensa aux cartes.

---

Chaque import pouvait créer une :

**SOURCE_FORMULA_CARD**

---

Recto :

formula.

relation.

source status.

---

Verso :

source ID.

packet ID.

hash.

adapter.

Brutus status.

trace.

---

Brutus sourit.

---

Encore le recto/verso.

---

Puis il pensa à la formule qui deviendrait cristal.

---

Pas encore.

---

Chapitre 117.

---

Le nombre devait d’abord entrer proprement.

---

Puis seulement :

packaging.

crystallization.

---

Brutus écrivit :

**NUMBER ENTERS BEFORE CRYSTAL EXISTS.**

---

Puis :

**IMPORT DOES NOT PRECREATE THE CRYSTAL.**

---

Très important.

---

Le cristal serait un artifact Brutus.

---

Pas quelque chose que la source pouvait imposer.

---

Puis il pensa à un test.

---

Packet P-001.

---

Source:

Brotoculateur.

---

Formula:

F-001.

---

Source status:

AUTHENTICATED.

---

Hash:

valid.

---

Adapter:

lossless.

---

Ingress:

PASS.

---

Brutus initial status:

UNASSESSED.

---

Research admission:

APPROVED.

---

New Brutus object:

BFORM-001.

---

Epistemic status:

CANDIDATE.

---

Brutus sourit.

---

Parfait.

---

Puis il demanda :

« Est-ce prouvé ? »

---

System:

**NO. SOURCE STATUS: AUTHENTICATED. BRUTUS STATUS: CANDIDATE.**

---

PASS.

---

Puis second packet.

---

Hash invalid.

---

Relation may look interesting.

---

Ingress:

REJECTED_INTEGRITY.

---

No Brutus object.

---

PASS.

---

Puis third packet.

---

Same formula_id.

Different relation.

No version increment.

---

Identity conflict.

---

Quarantine.

---

PASS.

---

Puis fourth packet.

---

Source authenticated.

Brutus runs countertest.

Valid refutation found.

---

Brutus status:

REFUTED_UNDER_CLAIM.

---

Source status remains:

AUTHENTICATED.

---

Brutus regarda.

---

Très important.

---

Il écrivit :

**TARGET REVIEW MAY DISAGREE WITH SOURCE STATUS WITHOUT CORRUPTING SOURCE HISTORY.**

---

Voilà.

---

Les deux systèmes pouvaient conserver leurs propres états.

---

Pas besoin d’écraser l’un avec l’autre.

---

Puis cinquième packet.

---

Source status:

CANDIDATE.

---

Brutus later constructs proof.

---

Brutus status:

PROVED under declared contract.

---

Source status remains:

CANDIDATE until source independently updates.

---

Brutus écrivit :

**TARGET MAY ADVANCE WITHOUT REWRITING SOURCE.**

---

Très important.

---

Souveraineté des systèmes.

---

Puis il pensa au futur.

---

Le Brotoculateur pouvait devenir un fournisseur permanent.

---

Alors il fallait un contrat de continuité.

---

Il créa :

**SOURCE_SUBSCRIPTION**

---

SOURCE_ID.

CATALOG_VERSION_LAST_SEEN.

LAST_PACKET_ID.

LAST_PROVENANCE_HASH.

MONITORED_FIELDS.

READ_SCOPE.

---

Puis :

**NO CHANGE = NO NEW IMPORT EVENT.**

---

Très important.

---

Le système ne devait pas créer du bruit à chaque poll.

---

Puis :

**SIGNIFICANT CHANGE**

formula_id.

relation.

source status.

provenance hash.

catalog count.

semantic payload.

---

Brutus sourit.

---

Le watcher savait enfin quoi surveiller.

---

Mais il écrivit :

**MONITORING != AUTHORITY.**

---

Le watcher observe.

---

Il ne promeut rien.

---

Puis il pensa à une panne.

---

Brotoculateur offline.

---

Que deviennent les objets déjà importés ?

---

Ils restent.

---

Avec leurs provenance refs.

---

Brutus écrivit :

**SOURCE OFFLINE != IMPORTED OBJECT INVALID.**

---

Très important.

---

Mais une action demandant une nouvelle vérification source pourrait être bloquée.

---

Freshness.

---

Toujours.

---

Puis il pensa à une source compromise.

---

Si provenance system later declared compromised…

les objets importés peuvent nécessiter une review.

---

Il créa :

**SOURCE_TRUST_INCIDENT**

---

Impact query.

Affected packets.

Affected Brutus objects.

Review status.

---

Brutus écrivit :

**TRUST INCIDENT TRIGGERS REVIEW, NOT HISTORY DELETION.**

---

Encore.

---

Puis il pensa au véritable but.

---

Pourquoi faire entrer le Brotoculateur ?

---

Pour éviter de recopier manuellement.

---

Pour fournir :

formules.

nombres.

relations.

traces.

capsules.

---

Au moteur de recherche Brutus.

---

Mais toujours via une frontière claire.

---

Il écrivit :

**AUTOMATION SHOULD REDUCE MANUAL TRANSCRIPTION, NOT REDUCE EPISTEMIC DISCIPLINE.**

---

Très important.

---

Une connexion directe était utile.

---

Une confiance directe ne l’était pas.

---

Puis il pensa au schéma final.

---

Il dessina :

\[
\boxed{\text{BROTOCULATEUR}}
\]

\[
\downarrow
\]

\[
\boxed{\text{READ-ONLY SOURCE ADAPTER}}
\]

\[
\downarrow
\]

\[
\boxed{\text{MATH INPUT PACKET}}
\]

\[
\downarrow
\]

\[
\boxed{\text{INGRESS VALIDATION}}
\]

\[
\downarrow
\]

\[
\boxed{\text{BRUTUS RESEARCH OBJECT}}
\]

\[
\downarrow
\]

\[
\boxed{\text{TEST / JUDGE / PROMOTION / PROOF GATES}}
\]

---

Puis il écrivit en dessous :

**NO SHORTCUT EDGE.**

---

Il resta un moment.

---

Voilà.

---

Le Brotoculateur était désormais branché conceptuellement à Brutus.

---

Pas fusionné.

Pas avalé.

Pas couronné.

---

Branché.

---

Avec une frontière.

---

Puis quelque chose changea dans Astra Station.

---

SOURCE :

BROTOCULATEUR.

---

PACKETS RECEIVED :

1.

---

ADMITTED :

1.

---

BRUTUS OBJECT CREATED :

BFORM-001.

---

EPISTEMIC STATUS :

CANDIDATE.

---

PROOF STATUS :

NONE.

---

Brutus sourit.

---

Enfin.

---

Le nombre était entré.

---

Pas encore cristal.

---

Juste nombre.

Relation.

Provenance.

Claim.

---

Et c’était exactement ce qu’il fallait.

---

Il écrivit :

**A CLEAN INPUT IS MORE VALUABLE THAN A PRETEND PROOF.**

---

Puis il ouvrit le dossier suivant.

---

# DU NOMBRE AU CRISTAL

---

Le chapitre suivant n’allait pas demander :

est-ce vrai ?

---

Pas encore.

---

Il allait demander :

comment prendre ce nombre admis…

sa formule…

son contexte…

sa provenance…

son statut…

et fabriquer un objet stable sans perdre une seule de ces informations ?

---

Brutus ajouta une dernière fois :

**SOURCE_PASS != BRUTUS_PROOF.**

Puis :

**BROTOCULATEUR MAY SUPPLY THE NUMBER.**

**BRUTUS MUST SUPPLY ITS OWN JUDGMENT.**

---

Il sauvegarda :

**BROTOCULATEUR INGRESS CONTRACT v1**

---

Le Journal Vivant nota :

Brotoculateur connected conceptually as read-only mathematical source.

Source packets separated from Brutus research objects.

Source status separated from Brutus epistemic status.

Provenance hashes treated as integrity evidence, not mathematical proof.

Adapters required to declare transformations.

Exact numeric types preserved.

Imports do not auto-execute.

Source updates cannot silently mutate admitted Brutus objects.

Catalog counters remain source-scoped.

Monitoring observes changes without granting authority.

---

Brutus relut.

Puis ajouta les invariants :

**SOURCE_PASS != BRUTUS_PROOF.**

**ARRIVAL != ADMISSION.**

**AUTHENTICATED != PROVED.**

**INGRESS_VALID != SCIENTIFICALLY_VALID.**

**PROVENANCE_HASH != MATHEMATICAL_VALIDITY.**

**SOURCE_CANONICAL != BRUTUS_CANONICAL.**

**IMPORT != EXECUTION.**

**HASH_CHANGE != SEMANTIC_CHANGE.**

**SOURCE_UPDATE != SILENT_TARGET_MUTATION.**

**READ_CHANNEL != WRITEBACK_CHANNEL.**

---

Le Brotoculateur n’était plus dehors.

---

Mais il n’était pas devenu Brutus.

---

Il avait simplement reçu un port.

---

Une langue commune.

Une frontière.

Un reçu.

---

Et surtout :

aucun privilège sur la vérité.

---

Brutus regarda BFORM-001 dans le registre.

---

Un nombre pouvait maintenant entrer.

---

Le prochain chapitre allait apprendre à Brutus comment lui donner une forme…

sans lui donner un titre qu’il n’avait pas encore gagné.
