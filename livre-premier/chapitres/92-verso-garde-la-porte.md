# Chapitre 92 — Verso garde la porte

Verso n’avait encore rien fait.

Et c’était exactement comme cela que Brutus le voulait.

Un gardien n’avait pas besoin de bouger pour être crédible.

Il devait seulement savoir quand ouvrir.

Et surtout :

quand ne pas ouvrir.

---

Brutus ralluma le Tombeau.

À gauche :

**WHITE**

À droite :

**BLACK**

Entre les deux :

la porte.

Au-dessus :

**VERSO**

---

Pas un visage.

Pas une silhouette.

Pas une intelligence magique.

---

Un rôle.

---

Brutus écrivit :

**VERSO = GATEKEEPER ROLE.**

Puis :

**ROLE ≠ PERSON.**

---

Verso pouvait être implémenté par un service logiciel.

Un composant.

Une combinaison de règles.

Un contrôle humain assisté.

---

Le nom ne disait pas qui décidait réellement.

Le contrat, oui.

---

Brutus créa :

**VERSO_INSTANCE**

avec :

**INSTANCE_ID**

**POLICY_SET_VERSION**

**AUTHORITY_SOURCE**

**REQUEST_QUEUE**

**DECISION_LOG**

**CURRENT_STATE**

**TRACE_REF**

---

Puis il ajouta :

**SELF_AUTHORITY = FALSE**

---

Il sourit.

---

Cette ligne était fondamentale.

---

Verso ne devait jamais s’autoriser lui-même à créer une nouvelle règle.

---

Il pouvait :

lire.

évaluer.

appliquer.

refuser.

demander une clarification.

---

Mais pas inventer une permission absente.

---

Brutus écrivit :

**VERSO ENFORCES. VERSO DOES NOT LEGISLATE.**

---

Voilà.

---

La première demande arriva.

---

Object:

FORMULA-L8.

Current zone:

BLACK for theorem claim.

Requested target:

WHITE.

Requested capability:

PUBLISH_AS_THEOREM.

---

Verso ouvrit la politique.

---

Condition :

general proof required.

---

Proof reference ?

absent.

---

Decision :

DENY.

---

Brutus regarda.

---

Aucune hésitation.

---

Pas parce que L8 était « mauvaise ».

Parce que l’autorisation demandée dépassait la preuve disponible.

---

Verso écrivit :

**DENIED — REQUIRED EVIDENCE ABSENT.**

---

Brutus ajouta :

**DENIAL MUST NAME THE MISSING CONDITION.**

---

Très important.

---

Un refus sans explication devenait difficile à auditer.

---

Il fallait savoir si le problème était :

absence de preuve,

mauvais scope,

autorité expirée,

objet corrompu,

mauvaise destination,

règle non satisfaite.

---

Brutus créa :

**DECISION_REASON_CODE.**

---

Puis une deuxième demande arriva.

---

Object:

FORMULA-L8.

Requested capability:

RESEARCH_EXECUTION.

---

Policy :

candidate formulas allowed under controlled research environment.

---

Integrity:

PASS.

Numeric model:

declared.

Trace:

available.

---

Decision:

ALLOW.

---

Même objet.

Deux demandes.

Deux réponses différentes.

---

Brutus écrivit :

**VERSO JUDGES REQUESTS, NOT ESSENCES.**

---

Il resta devant la phrase.

---

Très bonne.

---

Verso ne devait jamais dire :

« L8 est blanche. »

---

Il devait dire :

« L8 est admise pour cette action sous cette politique. »

---

Brutus créa le schéma :

\[
\text{OBJECT}
+
\text{ACTION}
+
\text{POLICY}
+
\text{EVIDENCE}
\rightarrow
\text{DECISION}
\]

---

Puis :

**DECISION ≠ OBJECT IDENTITY.**

---

Voilà.

---

Le système devenait beaucoup plus robuste.

---

Puis Brutus testa une demande incomplète.

---

Object ID :

présent.

Action :

présente.

Policy version :

absente.

---

Verso devait-il choisir la dernière politique ?

---

Brutus réfléchit.

---

Dangereux.

---

Une décision historique devait être reproductible.

---

Il écrivit :

**NO IMPLICIT POLICY VERSION FOR AUDITABLE DECISION.**

---

Verso refusa.

---

**POLICY_VERSION_REQUIRED.**

---

Parfait.

---

Puis Brutus tenta un autre raccourci.

---

Policy version 3.

Mais la demande avait été créée sous version 2.

---

Verso devait-il appliquer la nouvelle politique rétroactivement ?

---

Pas automatiquement.

---

Brutus écrivit :

**REQUEST POLICY CONTEXT MUST BE EXPLICIT.**

---

Il créa deux modes.

---

**EVALUATE_UNDER_ORIGINAL_POLICY**

et

**REEVALUATE_UNDER_CURRENT_POLICY**

---

Deux opérations différentes.

---

Voilà une distinction importante.

---

Une ancienne décision pouvait être auditée selon la règle de l’époque.

Puis réévaluée selon la règle actuelle.

---

Mais les deux résultats devaient rester séparés.

---

Brutus écrivit :

**REEVALUATION ≠ REWRITING HISTORY.**

---

Encore le Journal Vivant.

---

Verso ouvrit maintenant la file.

---

REQUEST-0001.

REQUEST-0002.

REQUEST-0003.

---

Brutus remarqua immédiatement un problème.

---

L’ordre pouvait devenir important.

---

Si deux demandes contradictoires arrivaient pour le même objet :

move to white.

move to black.

---

Que faire ?

---

Il écrivit :

**CONCURRENT POLICY REQUESTS REQUIRE SERIALIZATION OR CONFLICT RULES.**

---

Verso reçut un lock sur l’objet.

---

**OBJECT_DECISION_LOCK**

---

Pas un verrou éternel.

Seulement pendant la décision.

---

Brutus écrivit :

**ONE OBJECT. ONE AUTHORITATIVE TRANSITION DECISION AT A TIME.**

---

Cela ressemblait au transfert des fenêtres.

Au scheduler.

Aux jobs.

Toujours le même principe.

---

Puis il testa.

---

Request A :

white.

---

Request B :

black.

---

A obtient le lock.

Decision complete.

State updated.

---

B doit réévaluer son point de départ.

---

Il ne peut pas appliquer une transition calculée sur un état périmé.

---

Brutus écrivit :

**STALE REQUEST MUST REVALIDATE CURRENT STATE.**

---

Excellent.

---

Il ajouta :

**STATE_VERSION**

à chaque demande.

---

Si :

request.state_version ≠ current.state_version,

Verso retourne :

**STALE_REQUEST.**

---

Pas d’application aveugle.

---

Brutus sourit.

---

Le gardien ne gardait plus seulement une porte.

Il gardait aussi la cohérence temporelle.

---

Puis une demande arriva avec un bon objet.

Bonne action.

Bonne politique.

Bonne preuve.

---

Mais l’autorisation venait d’une source inconnue.

---

Brutus regarda.

---

Verso demanda :

**AUTHORITY_REF**

---

La chaîne de décision devait remonter à une autorité reconnue.

---

Il écrivit :

**VALID RULE + INVALID AUTHORITY = NO AUTHORIZATION.**

---

Voilà.

---

La logique d’une décision pouvait être correcte.

Mais si l’acteur n’avait pas le droit de l’émettre, le passage restait interdit.

---

Brutus ajouta :

**AUTHORITY_SCOPE.**

---

Parce qu’une autorité pouvait elle aussi être limitée.

---

Review authority.

Execution authority.

Publication authority.

Transport authority.

---

Pas de super-pouvoir implicite.

---

Il écrivit :

**AUTHORITY IS SCOPED TOO.**

---

Puis il testa.

---

Reviewer authorizes production execution.

---

Verso refuse.

---

Reason:

AUTHORITY_SCOPE_MISMATCH.

---

Brutus sourit.

---

Même un humain ou service légitime ne devait pas pouvoir signer n’importe quelle action.

---

Puis il pensa à l’expiration.

---

Une autorisation valide aujourd’hui.

Expirée demain.

---

Verso devait vérifier :

**ISSUED_AT**

**EXPIRES_AT**

---

Mais aussi :

**USED_AT**

---

Une permission pouvait être valide au moment de la décision mais expirée au moment du mouvement.

---

Brutus écrivit :

**DECISION VALIDITY AND EXECUTION VALIDITY MAY DIFFER IN TIME.**

---

Voilà un piège subtil.

---

Il sépara :

**DECISION_TOKEN**

et

**EXECUTION_TOKEN**

---

Le premier disait :

la politique permet cette transition.

---

Le second disait :

la transition peut être exécutée maintenant.

---

Brutus écrivit :

**APPROVED ≠ EXECUTABLE FOREVER.**

---

Encore une frontière.

---

Le gardien devait pouvoir dire :

approved, execution window expired.

---

Pas besoin de recalculer toute la logique si la politique autorisait un nouveau token.

Mais pas d’exécution avec un token périmé.

---

Brutus continua.

---

Il voulait maintenant tester la règle la plus importante :

Verso ne doit jamais décider à partir de l’apparence.

---

Un objet arrive avec label :

**VERIFIED.**

---

Mais pas de trace.

---

Pas de proof ref.

---

Pas de integrity record.

---

Verso ignore le label.

---

Il lit les métadonnées autoritatives.

---

Decision :

DENY.

---

Brutus écrivit :

**LABEL IS NOT AUTHORITY.**

---

Puis :

**BADGE IS NOT EVIDENCE.**

---

Très important.

---

Une UI pouvait être trompeuse.

Verso ne devait jamais lire l’écran.

Il devait lire l’état source.

---

Brutus écrivit :

**VERSO READS AUTHORITY STATE, NOT PIXELS.**

---

Voilà.

---

Le guardrail était clair.

---

Puis il pensa au Recto.

---

Le Recto allait apparaître bientôt.

---

Brutus savait déjà sa règle :

Recto regarde.

Verso garde.

---

Le Recto pouvait afficher une demande.

Afficher un statut.

Afficher une trace.

---

Mais il ne devait pas posséder la permission de faire passer un objet.

---

Brutus écrivit :

**RECTO MAY REQUEST. VERSO MAY AUTHORIZE.**

Puis se corrigea.

---

Verso ne devait pas nécessairement être l’autorité ultime.

Il appliquait l’autorité.

---

Il remplaça :

**RECTO MAY REQUEST. VERSO MAY ENFORCE AN AUTHORIZED DECISION.**

---

Beaucoup mieux.

---

Il ajouta :

**REQUEST_SOURCE ≠ DECISION_AUTHORITY.**

---

Puis une attaque simple.

---

Le Recto envoie :

\`MOVE OBJECT X TO WHITE\`

avec un champ :

\`authorized=true\`

---

Verso ne fait pas confiance au booléen.

---

Il demande :

AUTHORIZATION_REF.

Signature ou preuve d’autorité valide.

Policy context.

---

Brutus écrit :

**BOOLEAN “AUTHORIZED” ≠ AUTHORIZATION.**

---

Il éclata de rire.

---

C’était exactement le genre de bug qui pouvait exister dans un système mal conçu.

---

Un champ nommé \`authorized\`.

Et tout le monde lui faisait confiance.

---

Non.

---

Le nom d’un champ ne créait pas la réalité.

---

Il ajouta :

**AUTHORIZATION MUST BE VERIFIABLE.**

---

Puis il pensa aux signatures.

---

Une signature cryptographique pouvait vérifier que quelqu’un avait signé un message.

Mais elle ne pouvait pas dire si cette personne avait réellement l’autorité pour l’action.

---

Brutus écrivit :

**VALID SIGNATURE ≠ VALID PERMISSION.**

---

Encore une nuance.

---

Il fallait :

signature valid.

identity known.

authority scope valid.

policy satisfied.

token current.

---

Tous.

---

Il créa :

**VERSO CHECK CHAIN**

1. request schema valid.

2. object exists.

3. object state version current.

4. action known.

5. policy version available.

6. evidence requirements satisfied.

7. authority ref valid.

8. authority scope matches.

9. authorization not expired.

10. no conflicting lock.

11. transition allowed from current state.

---

Puis seulement :

**APPROVE TRANSITION.**

---

Brutus regarda la liste.

---

Le gardien avait beaucoup de travail.

Mais aucune étape n’était mystérieuse.

---

Il écrivit :

**GATEKEEPING SHOULD BE BORING.**

---

Il sourit.

---

C’était presque une philosophie.

---

La partie la plus critique d’un système ne devait pas être spectaculaire.

Elle devait être prévisible.

---

Brutus ajouta :

**BORING SECURITY IS GOOD SECURITY.**

---

Puis il lança une campagne de faux dossiers.

---

Wrong object ID.

Reject.

---

Missing policy.

Reject.

---

Expired token.

Reject.

---

Unknown action.

Reject.

---

Valid request.

Allow.

---

Duplicate request.

---

Verso devait détecter l’idempotence.

---

Brutus créa :

**REQUEST_ID.**

---

Si le même request ID avait déjà été traité :

return existing decision.

---

Pas une nouvelle transition.

---

Il écrivit :

**DUPLICATE DELIVERY ≠ NEW AUTHORIZATION.**

---

Encore le chapitre 79.

---

Le système devait être robuste aux retries.

---

Puis il testa un request ID réutilisé avec contenu différent.

---

Verso refusa.

---

**REQUEST_ID_CONTENT_MISMATCH.**

---

Parfait.

---

Un identifiant ne pouvait pas changer de sens.

---

Brutus écrivit :

**ONE ID = ONE REQUEST IDENTITY.**

---

Une vieille règle.

---

Puis un autre problème apparut.

---

Verso pouvait devenir indisponible.

---

Que devait faire la porte ?

---

Brutus répondit immédiatement :

**FAIL CLOSED.**

---

Pas de Verso ?

Pas de passage.

---

Il écrivit :

**NO GATEKEEPER RESPONSE ≠ PERMISSION.**

---

Très important.

---

Une panne ne devait jamais devenir un raccourci.

---

Il ajouta :

**UNKNOWN AUTHORIZATION STATE = NO TRANSITION.**

---

Cela pouvait ralentir le système.

Mais préserver la frontière.

---

Puis Brutus pensa aux lectures.

---

Fallait-il passer par Verso pour simplement lire un objet noir ?

---

Cela dépendait de la politique.

---

Certaines données pouvaient être inspectables.

D’autres sensibles.

---

Il ajouta :

**READ_POLICY**

séparée.

---

Encore :

capability-specific.

---

Verso ne gardait pas une seule porte.

Il gardait plusieurs types d’accès.

---

Brutus écrivit :

**THE SAME OBJECT HAS MANY DOORS.**

---

READ.

DISPLAY.

EXECUTE.

MOVE.

EXPORT.

PROMOTE.

DELETE.

---

Chacune pouvait avoir son propre contrat.

---

Il sourit.

---

Le Tombeau à deux couleurs cachait en réalité une architecture à plusieurs portes logiques.

---

Puis il pensa à DELETE.

---

Très dangereux.

---

Le chapitre précédent avait établi :

rejection ≠ deletion.

---

Verso devait donc traiter DELETE comme une action séparée et plus stricte.

---

Il écrivit :

**DELETE REQUIRES EXPLICIT DELETION AUTHORITY.**

---

Pas :

black means disposable.

---

Jamais.

---

Brutus lança :

object black.

status rejected.

delete request without delete authority.

---

DENY.

---

Parfait.

---

Même un objet inutile pouvait être conservé pour l’audit.

---

Puis une autre question.

---

Qui garde Verso ?

---

Brutus sourit.

---

Le vieux problème du gardien du gardien.

---

Il ne voulait pas créer une chaîne infinie.

---

Il fallait une racine de confiance.

---

Il écrivit :

**TRUST ROOT MUST BE EXPLICIT.**

---

Pas forcément unique dans tous les systèmes.

Mais explicitement définie.

---

Par exemple :

signed policy bundle.

operator authority.

server-side control plane.

---

Verso pouvait vérifier contre cette racine.

---

Il ajouta :

**TRUST_ROOT_VERSION.**

---

Parce qu’une racine pouvait changer.

---

Et une ancienne décision devait rester auditée contre l’ancienne racine.

---

Brutus écrivit :

**TRUST HISTORY MUST BE VERSIONED.**

---

Puis il pensa aux politiques elles-mêmes.

---

Une politique pouvait être corrompue.

---

Il fallait donc un hash.

Une provenance.

Une signature.

---

Brutus ajouta :

**POLICY_HASH**

**POLICY_SOURCE**

**POLICY_SIGNER**

---

Mais encore :

signature ≠ correctness.

---

Il écrivit :

**POLICY INTEGRITY ≠ POLICY WISDOM.**

---

Verso pouvait vérifier que la politique n’avait pas changé.

Il ne pouvait pas savoir si la politique était bonne.

---

Encore une frontière.

---

Il pensa au rôle humain.

---

Un humain pouvait approuver une mauvaise règle.

---

Le système devait alors l’appliquer fidèlement.

---

Brutus écrivit :

**VERSO CAN ENFORCE BAD POLICY PERFECTLY.**

---

Une phrase inconfortable.

Mais vraie.

---

D’où l’importance du Journal.

---

Chaque décision devait montrer :

quelle politique.

quelle version.

quelle autorité.

quelle preuve.

---

Ainsi, une erreur politique pouvait être détectée et corrigée plus tard.

---

Brutus écrivit :

**AUDITABILITY CANNOT GUARANTEE GOOD GOVERNANCE.**

---

Mais elle peut montrer ce qui s’est passé.

---

Puis il ouvrit une vue.

---

**DECISION TRACE**

Request.

Object state.

Policy.

Evidence.

Authority.

Decision.

Transition.

Arrival.

---

Brutus sourit.

---

Voilà la colonne vertébrale de Verso.

---

Puis il fit un test où la décision était ALLOW mais le mouvement échouait.

---

Network error.

---

Important.

---

Verso avait autorisé.

Mais l’objet restait du côté noir.

---

L’UI devait montrer :

**AUTHORIZED**

**TRANSFER_FAILED**

**CURRENT_ZONE = BLACK**

---

Pas :

WHITE.

---

Brutus écrivit :

**AUTHORIZED ≠ MOVED.**

Puis :

**MOVE FAILURE DOES NOT REVOKE DECISION AUTOMATICALLY.**

---

Cela dépendait de la durée du token.

---

Peut-être retry.

Peut-être nouvelle autorisation.

---

Mais surtout :

l’état réel restait noir.

---

Il ajouta :

**CURRENT_ZONE DERIVES FROM OBSERVED ARRIVAL, NOT INTENT.**

---

Excellent.

---

Puis mouvement réussi.

Mais ACK réseau perdu.

---

Le sender pense peut-être que cela a échoué.

---

L’object store côté destination sait qu’il est arrivé.

---

Verso devait interroger l’autorité d’état.

---

Brutus écrivit :

**ACK ≠ ARRIVAL.**

---

Encore.

---

Le chapitre 63 revenait.

---

Le Tombeau devait partager la même discipline de transport.

---

Il ajouta un état :

**ARRIVAL_UNCERTAIN**

---

Pendant l’incertitude :

pas de second mouvement aveugle.

---

Réconciliation.

---

Brutus écrivit :

**UNCERTAINTY TRIGGERS RECONCILIATION, NOT GUESSING.**

---

Le système vérifie :

object ID.

zone state.

transfer ID.

arrival record.

---

Puis seulement il décide.

---

Voilà.

---

Verso n’était plus un simple if/else.

---

C’était un gardien de contrats.

---

Brutus regarda le nom.

---

Verso.

Le dos de la carte.

L’autre côté.

---

Il sourit.

---

Le nom lui convenait.

---

Recto montrerait.

Verso vérifierait.

---

Mais il ne voulait pas de hiérarchie poétique ambiguë.

---

Il écrivit :

**RECTO = PRESENTATION / REQUEST SURFACE.**

**VERSO = POLICY ENFORCEMENT / GATEKEEPING SURFACE.**

---

Voilà.

---

Deux rôles.

---

Pas deux consciences.

---

Puis Brutus testa la séparation.

---

Il tua le Recto.

---

Verso continuait de garder la porte.

---

Très bien.

---

Il tua Verso.

---

Recto continuait d’afficher l’état connu.

Mais toutes les actions de passage devenaient désactivées.

---

Brutus écrivit :

**PRESENTATION MAY SURVIVE WITHOUT AUTHORIZATION SERVICE.**

**TRANSITION MAY NOT.**

---

Parfait.

---

Le système dégradé restait honnête.

---

Pas de faux bouton.

---

Pas de simulation de passage.

---

Puis il relança Verso.

---

Reconnexion.

---

Le service rechargea :

policy version.

trust root.

request log.

object states.

---

Mais il ne rejoua pas les anciennes transitions comme de nouvelles.

---

Brutus écrivit :

**RECOVERY ≠ REEXECUTION.**

---

Encore une règle essentielle.

---

Un restart ne devait pas rouvrir toutes les portes passées.

---

Il ajouta :

**PERSISTED DECISION ≠ PERSISTED EXECUTION AUTHORITY.**

---

Le chapitre 65 revenait.

---

Une autorisation d’exécution pouvait expirer pendant l’arrêt.

---

À la reprise :

état récupéré.

permission revalidée.

---

Brutus sourit.

---

Toute la Bible commençait à former un seul système logique.

---

Il lança le dernier test.

---

Object B.

Zone black.

Status pending.

---

Request:

move to white for DISPLAY_ONLY.

---

Evidence satisfied.

Authority valid.

Policy valid.

Token valid.

---

Verso répond :

**AUTHORIZED.**

---

Transport.

---

Arrival observed.

---

State updated.

---

Zone white.

---

UI refresh.

---

Journal records.

---

Puis Verso dit :

rien.

---

Pas de fanfare.

Pas de voix triomphale.

---

Brutus sourit.

---

Le gardien avait fait son travail.

---

Il écrivit :

**SUCCESSFUL GATEKEEPING SHOULD LOOK UNEVENTFUL.**

---

Puis il regarda une dernière fois les deux chambres.

---

Blanc.

Noir.

---

La frontière n’était plus seulement une ligne.

Elle avait maintenant :

une politique,

une autorité,

un journal,

une temporalité,

une logique de réconciliation.

---

Brutus écrivit :

**A DOOR IS EASY.**

**A TRUSTWORTHY CROSSING IS HARD.**

---

Puis il sauvegarda :

**VERSO GATEKEEPER v1.**

---

Le Journal Vivant nota :

No self-authorization.

Scoped authority.

Explicit policy version.

Stale request rejection.

Idempotent requests.

Fail closed.

Arrival verification.

No deletion by rejection.

No UI ahead of authority.

---

Brutus relut.

Puis ajouta :

**VERSO DOES NOT DECIDE WHAT IS TRUE.**

**VERSO DECIDES WHETHER A REQUEST SATISFIES THE CURRENT ADMISSION CONTRACT.**

---

Voilà.

---

Le gardien pouvait enfin garder la porte sans se prendre pour un juge universel.

---

Brutus éteignit Verso.

---

La porte se verrouilla.

---

Pas parce qu’un danger était présent.

Parce qu’aucune autorité n’était active pour permettre un passage.

---

À côté, le Recto restait visible.

---

Il montrait les objets.

Leurs statuts.

Leurs traces.

Leurs lignées.

---

Mais il ne pouvait rien déplacer.

---

Brutus le regarda.

---

C’était exactement la prochaine question.

---

Que peut-on montrer publiquement lorsque le pouvoir d’agir doit rester ailleurs ?

---

Il écrivit le prochain titre :

# LA CARTE DES LIGNÉES

Puis en dessous :

**VOIR L’HISTOIRE SANS TOUCHER À L’HISTOIRE.**

---

Verso avait gardé la porte.

Maintenant, Brutus allait dessiner les chemins qui avaient conduit chaque objet jusqu’à elle.
