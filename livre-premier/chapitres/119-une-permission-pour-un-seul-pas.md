# Chapitre 119 — Une permission pour un seul pas

**AUTHORIZATION SHOULD BE AS SMALL AS THE ACTION IT ENABLES.**

Brutus relut la phrase.

Puis il regarda CRYSTAL-0001.

---

Le cristal était admis.

Il était encore à son emplacement actuel.

---

Aucune erreur.

---

Mais maintenant, Brutus voulait autoriser un déplacement.

---

Un seul.

---

Pas :

« ANT-001 peut déplacer les cristaux. »

---

Pas :

« QueenCore autorise le mouvement. »

---

Pas :

« utilisateur approuvé. »

---

Trop large.

---

Il écrivit :

**ONE ACTION. ONE OBJECT. ONE STATE. ONE DESTINATION. ONE USE.**

---

Voilà.

---

Il ouvrit un nouveau dossier.

# SINGLE-STEP AUTHORIZATION

---

Puis il créa :

**ACTION_GRANT**

avec :

**GRANT_ID**

**ACTOR_ID**

**OBJECT_ID**

**OBJECT_VERSION**

**ACTION_TYPE**

**SOURCE_LOCATION**

**SOURCE_STATE_VERSION**

**DESTINATION_LOCATION**

**DESTINATION_EXPECTATION**

**CAPABILITY_SCOPE**

**ISSUED_AT**

**EXPIRES_AT**

**MAX_USES**

**AUTHORITY_REF**

**POLICY_VERSION**

**TRACE_REF**

---

Puis il fixa :

**MAX_USES = 1**

---

Brutus sourit.

---

Très important.

---

Une permission pour un pas devait mourir après ce pas.

---

Il écrivit :

**ONE-SHOT MEANS ONE-SHOT.**

---

Puis :

**SUCCESSFUL USE CONSUMES THE GRANT.**

---

Et immédiatement :

**FAILED VALIDATION DOES NOT SILENTLY EXPAND IT.**

---

Encore.

---

Le token n’était pas une carte d’accès générale.

---

C’était une autorisation chirurgicale.

---

Puis il pensa au mot :

**capability.**

---

Une capability pouvait être beaucoup trop large si mal définie.

---

Alors il créa :

**CAPABILITY_SCOPE**

---

MOVE_OBJECT_ONCE.

---

Pas :

MOVE_OBJECT.

---

Pas :

MOVE_ANY_OBJECT.

---

Pas :

WORLD_WRITE.

---

Brutus écrivit :

**CAPABILITY MUST NAME THE VERB AND THE LIMIT.**

---

Très important.

---

Une permission devait dire :

ce qu’elle permet.

---

Et tout aussi clairement :

ce qu’elle ne permet pas.

---

Puis il créa :

**DENIED_BY_OMISSION**

---

Pas un champ runtime.

---

Une règle mentale.

---

Si la permission ne dit pas qu’une action est permise…

elle est interdite.

---

Il écrivit :

**UNLISTED ACTION != IMPLIED ACTION.**

---

Excellent.

---

Puis il pensa à ANT-001.

---

Elle voulait déplacer CRYSTAL-0001.

---

De :

WORLD:C4.

---

Vers :

WORLD:C5.

---

Un pas.

---

Brutus créa :

**MOVE_INTENT**

---

ACTOR:

ANT-001.

---

OBJECT:

CRYSTAL-0001.

---

FROM:

C4.

---

TO:

C5.

---

ACTION:

MOVE_ONE_STEP.

---

Il demanda à QueenCore :

autoriser ?

---

QueenCore ne répondit pas tout de suite.

---

Elle vérifia :

actor allowed?

object movable?

source state current?

destination valid?

world generation correct?

crystal version current?

policy allows one-step move?

---

Puis elle émit :

**GRANT-0001**

---

Brutus regarda le grant.

---

ACTOR:

ANT-001.

---

OBJECT:

CRYSTAL-0001.

---

FROM:

C4.

---

TO:

C5.

---

MAX_USES:

1.

---

EXPIRES:

tick 950.

---

Il écrivit :

**GRANT ISSUED != ACTION EXECUTED.**

---

Très important.

---

Encore une fois :

l’autorisation pouvait exister…

sans qu’aucun mouvement n’ait encore eu lieu.

---

Puis il pensa à la détention du grant.

---

ANT-001 reçoit le token.

---

Est-ce que posséder le token suffit ?

---

Non.

---

Il faut encore :

présenter.

valider.

consommer.

---

Brutus créa :

**GRANT_STATE**

ISSUED.

PRESENTED.

VALIDATED.

CONSUMED.

EXPIRED.

REVOKED.

REJECTED.

UNKNOWN.

---

Puis :

**TOKEN PRESENT != TOKEN VALID.**

---

Très important.

---

Un token pouvait être :

expiré.

révoqué.

mal adressé.

pour un autre objet.

pour un autre état.

---

Puis il pensa à la copie.

---

Si quelqu’un copie le token ?

---

Même GRANT_ID.

---

Le système doit refuser une deuxième utilisation.

---

Il écrivit :

**COPYING A ONE-SHOT TOKEN MUST NOT COPY ITS AUTHORITY.**

---

Très important.

---

L’autorité vivait dans le registre canonique.

---

Pas dans les bytes du token.

---

Le token n’était qu’un porteur de référence.

---

Il créa :

**GRANT_LEDGER_STATE**

avec :

**GRANT_ID**

**CURRENT_STATE**

**USE_COUNT**

**CONSUMED_BY_ACTION_ID**

**LAST_UPDATED_AT**

---

Brutus écrivit :

**AUTHORITY STATE LIVES SERVER-SIDE.**

---

Voilà.

---

Même si le token circule…

la vérité de son état reste canonique.

---

Puis il pensa à la signature.

---

Le grant pouvait être signé.

---

Très utile.

---

Mais :

signature valide ne voulait pas dire grant encore utilisable.

---

Brutus écrivit :

**VALID SIGNATURE != UNUSED GRANT.**

---

Encore.

---

Il ajouta :

**SIGNATURE_CHECK**

et

**LEDGER_CHECK**

---

Deux étapes.

---

Très important.

---

Puis il pensa au temps.

---

Le grant est émis au tick 940.

---

Expire au tick 950.

---

ANT-001 tente de l’utiliser au tick 951.

---

Refus.

---

Location inchangée.

---

Brutus écrivit :

**EXPIRED AUTHORIZATION MUST FAIL CLOSED.**

---

Très important.

---

Pas de grâce silencieuse.

---

Pas :

« il était presque encore valide ».

---

Le système devait choisir une règle claire.

---

Puis il pensa aux horloges.

---

WORLD_TICK.

SERVER_TIME.

---

Quelle référence utiliser ?

---

Pour une action locale :

WORLD_TICK pouvait être suffisant.

---

Pour une autorisation externe :

server time pourrait aussi compter.

---

Mais il fallait le déclarer.

---

Il créa :

**EXPIRATION_CLOCK**

WORLD_TICK.

SERVER_MONOTONIC_TIME.

EXTERNAL_AUTHORITY_TIME.

---

Puis :

**CLOCK DOMAIN MUST BE EXPLICIT.**

---

Excellent.

---

Puis il pensa au changement d’état.

---

Grant-0001 autorise :

C4 → C5.

---

Mais avant usage…

un autre événement déplace le cristal de C4 à D4.

---

Le grant devient quoi ?

---

Invalide.

---

Brutus écrivit :

**GRANT BINDS EXPECTED SOURCE STATE.**

---

Puis :

**STATE DRIFT INVALIDATES STALE AUTHORIZATION.**

---

Très important.

---

Il créa :

**PRECONDITION_HASH**

---

Hash of:

object version.

source location.

custody state.

world generation.

placement state.

---

Brutus sourit.

---

Une autorisation devenait attachée à une photographie logique de l’état.

---

Pas seulement à un objet.

---

Puis il pensa à la destination.

---

C5 était libre à émission.

---

Mais devient occupé avant exécution.

---

Que faire ?

---

Refuser.

---

Pas chercher une autre case automatiquement.

---

Brutus écrivit :

**AUTHORIZED DESTINATION IS EXACT.**

Puis :

**NO SILENT REROUTE.**

---

Très important.

---

Sinon une permission C4 → C5 pourrait devenir C4 → C6.

---

Ce ne serait plus la même action.

---

Il faudrait un nouveau grant.

---

Puis il pensa à la notion de « un pas ».

---

C4 → C5.

---

Simple.

---

Mais dans un autre monde, un pas pourrait être :

distance 1.

un edge topologique.

une transition de state machine.

---

Il fallait définir.

---

Brutus créa :

**STEP_CONTRACT**

---

STEP_TYPE.

SOURCE.

DESTINATION.

MAX_DISTANCE.

TOPOLOGY_EDGE_REF.

WORLD_RULESET_REF.

---

Puis :

**ONE STEP MUST BE DEFINED BY THE WORLD, NOT BY THE STORY.**

---

Très important.

---

Dans LOCAL-001 :

un pas = une transition autorisée entre deux cases adjacentes.

---

Pas téléportation.

---

Pas saut de quatre cases.

---

Il ajouta :

**MOVE_ONE_STEP**

---

Voilà.

---

Puis il pensa aux permissions composées.

---

Supposons qu’on veut déplacer :

C4 → C5 → C6 → C7.

---

Un seul grant pour trois pas ?

---

Possible.

---

Mais pas dans cette policy.

---

Brutus écrit :

**MULTI-STEP PLAN != MULTI-STEP AUTHORITY.**

---

Très important.

---

Le plan pouvait exister.

---

Mais chaque pas recevrait son propre grant.

---

Il dessina :

\[
C4
\rightarrow
C5
\rightarrow
C6
\rightarrow
C7
\]

---

Puis en dessous :

GRANT-A.

GRANT-B.

GRANT-C.

---

Chacun émis après observation de l’état précédent.

---

Brutus écrivit :

**NEXT STEP DEPENDS ON VERIFIED CURRENT STATE.**

---

Voilà.

---

Pas de permissions futures sur un état qui n’existait pas encore.

---

Puis il pensa à performance.

---

Trois grants.

Plus lent.

---

Oui.

---

Mais le coût était acceptable pour les actions sensibles.

---

Il écrivit :

**SAFETY MAY REQUIRE MORE ROUND TRIPS THAN CONVENIENCE.**

---

Très important.

---

Puis il pensa aux actions non sensibles.

---

Peut-être une policy future pourrait autoriser :

up to 10 local steps.

---

Mais ce serait une autre capability.

---

Pas une interprétation libre du one-step.

---

Brutus écrivit :

**BROADER AUTHORITY REQUIRES A BROADER EXPLICIT CONTRACT.**

---

Encore.

---

Puis il pensa à la fourmi.

---

Fourminizer choisit C5.

---

Elle soumet :

MOVE_INTENT.

---

QueenCore émet grant.

---

Verso valide.

---

World authority reçoit :

ACTION_REQUEST + GRANT.

---

Puis le moteur vérifie :

grant actor == ANT-001?

yes.

---

grant object == CRYSTAL-0001?

yes.

---

source location == C4?

yes.

---

current version matches?

yes.

---

destination == C5?

yes.

---

not expired?

yes.

---

unused?

yes.

---

destination free?

yes.

---

world rule allows?

yes.

---

Brutus écrivit :

**VALIDATION PASS.**

---

Mais encore :

pas de mouvement.

---

Il ajouta :

**ACTION_COMMIT**

---

Seulement maintenant.

---

Un nouvel événement :

**MOVE_EVENT-0001**

---

FROM:

C4.

---

TO:

C5.

---

GRANT_REF:

GRANT-0001.

---

ACTION_ID:

MOVE-0001.

---

Puis le registre consomma le grant.

---

GRANT_STATE:

CONSUMED.

---

USE_COUNT:

1.

---

Brutus sourit.

---

Voilà.

---

Il écrivit :

**AUTHORIZATION AND EXECUTION MEET AT COMMIT.**

---

Très important.

---

Le grant n’était ni le mouvement…

ni le résultat.

---

Il rendait simplement un mouvement précis admissible.

---

Puis il tenta immédiatement de réutiliser GRANT-0001.

---

Même action.

Même objet.

Même destination.

---

Refus.

---

Reason:

GRANT_CONSUMED.

---

PASS.

---

Brutus écrivit :

**REPLAYED TOKEN != REPLAYED AUTHORITY.**

---

Excellent.

---

Puis il tenta de changer l’objet.

---

Same grant.

OBJECT:

CRYSTAL-0002.

---

Refus.

---

**OBJECT_SCOPE_MISMATCH.**

---

PASS.

---

Puis acteur différent.

---

ANT-003.

---

Refus.

---

**ACTOR_SCOPE_MISMATCH.**

---

PASS.

---

Puis destination différente.

---

C6.

---

Refus.

---

**DESTINATION_SCOPE_MISMATCH.**

---

PASS.

---

Puis action différente.

---

DROP.

---

Refus.

---

**ACTION_SCOPE_MISMATCH.**

---

PASS.

---

Brutus regarda les refus.

---

C’était exactement ce qu’il voulait.

---

La permission était difficile à détourner parce qu’elle avait presque tout verrouillé.

---

Il écrivit :

**A GOOD GRANT IS BORING TO ABUSE.**

---

Puis il pensa à la révocation.

---

Supposons :

grant issued.

---

Avant usage, un incident survient.

---

QueenCore doit pouvoir révoquer.

---

Il créa :

**GRANT_REVOCATION_EVENT**

---

GRANT_ID.

REASON.

REVOKED_BY.

REVOKED_AT.

TRACE_REF.

---

Puis :

**REVOKED GRANT FAILS EVEN IF SIGNATURE REMAINS VALID.**

---

Très important.

---

Encore la distinction :

crypto integrity.

live authority state.

---

Puis il pensa au motif.

---

Pourquoi révoquer ?

---

WORLD_PAUSED.

OBJECT_CHANGED.

DESTINATION_CHANGED.

INCIDENT.

OPERATOR_CANCEL.

POLICY_CHANGE.

---

Il créa :

**REVOCATION_REASON**

---

Puis il pensa à la policy change.

---

Grant issued under policy v1.

---

Policy v2 arrives.

---

Does old grant remain valid?

---

Depends.

---

Il fallait déclarer.

---

Il créa :

**POLICY_UPDATE_EFFECT**

KEEP_EXISTING_GRANTS.

REVOKE_INCOMPATIBLE.

REVOKE_ALL.

---

Brutus écrivit :

**POLICY CHANGE MUST DECLARE EFFECT ON OUTSTANDING AUTHORITY.**

---

Excellent.

---

Puis il pensa à un crash.

---

Grant validated.

---

World process crashes before commit.

---

Le grant est-il consommé ?

---

Danger.

---

Il fallait transaction.

---

Brutus créa :

**ACTION_COMMIT_PROTOCOL**

---

1. lock grant.

2. validate preconditions.

3. commit world event.

4. mark grant consumed.

5. emit receipt.

---

Mais crash possible entre 3 et 4.

---

Il pensa.

---

Il fallait idempotency.

---

Il ajouta :

**ACTION_ID**

unique.

---

Le registre doit pouvoir dire :

action already committed for this grant.

---

Brutus écrivit :

**CRASH RECOVERY MUST NOT TURN ONE-SHOT INTO TWO-SHOT.**

---

Très important.

---

Puis :

**GRANT CONSUMPTION AND ACTION COMMIT MUST BE RECONCILABLE AS ONE LOGICAL TRANSACTION.**

---

Voilà.

---

Le système pouvait utiliser une transaction atomique…

ou une reconciliation robuste.

---

Mais jamais supposer.

---

Puis il pensa au cas inverse.

---

Grant consumed.

---

Action not committed.

---

Il fallait détecter :

**CONSUMED_WITHOUT_COMMIT**

---

Incident.

---

Puis :

manual or automated reconciliation.

---

Brutus écrivit :

**CONSUMED != EXECUTED UNLESS ACTION_REF EXISTS.**

---

Encore.

---

La même obsession.

---

Et c’était bien.

---

Puis il pensa à l’aquarium.

---

Comment afficher le grant ?

---

Pas comme un halo permanent.

---

Peut-être :

une petite ligne pointillée C4 → C5.

---

Label :

AUTHORIZED.

---

Mais elle devait disparaître si :

consumed.

expired.

revoked.

---

Brutus écrivit :

**AUTHORIZED PATH != EXECUTED PATH.**

---

Puis :

**PLANNED LINE MUST LOOK DIFFERENT FROM HISTORY LINE.**

---

Très important.

---

Une ligne autorisée ne devait jamais ressembler à une trajectoire déjà parcourue.

---

Puis il pensa au son.

---

Grant issued.

---

Faut-il un son ?

---

Peut-être seulement pour action sensible.

---

Il créa :

**AUTHORIZATION_SOUND_EVENT**

---

Mais :

grant consumed should not be confused with arrival.

---

Il écrivit :

**AUTHORIZATION SOUND != MOVEMENT SOUND.**

---

Encore.

---

Puis il pensa à l’opérateur.

---

La Queen pouvait avoir un bouton :

**AUTHORIZE ONE STEP**

---

Très bien.

---

Mais le bouton devait montrer :

actor.

object.

from.

to.

expiry.

---

Avant l’approbation.

---

Pas seulement :

Authorize?

---

Brutus écrivit :

**HUMAN APPROVAL MUST PREVIEW EXACT ACTION SCOPE.**

---

Très important.

---

Si l’humain autorisait :

CRYSTAL-0001 C4 → C5

---

le système ne devait pas transformer silencieusement ça en :

move crystal somewhere.

---

Il créa :

**APPROVAL_PREVIEW**

---

ACTOR.

OBJECT.

CURRENT_STATE.

DESTINATION.

ACTION.

EXPIRATION.

REVERSIBILITY.

EXPECTED_EFFECT.

---

Puis :

**APPROVAL_RECEIPT**

---

Ce qui avait été approuvé.

---

Pas juste qui avait cliqué.

---

Brutus sourit.

---

Un humain devait pouvoir revenir plus tard et comprendre ce qu’il avait réellement autorisé.

---

Puis il pensa au consentement.

---

Même logique.

---

Une autorisation devait être compréhensible avant l’action.

---

Pas formulée trop largement.

---

Il écrivit :

**CONSENT TO ONE STEP != CONSENT TO A JOURNEY.**

---

Très important.

---

Puis il pensa aux Fourmis autonomes.

---

Peuvent-elles demander automatiquement le prochain grant ?

---

Oui.

---

Mais recevoir automatiquement ?

---

Seulement si une policy de standing authority le permet.

---

Pour v1 :

pas de standing authority sur les objets sensibles.

---

Brutus écrivit :

**AUTONOMOUS REQUEST != AUTOMATIC AUTHORIZATION.**

---

Excellent.

---

Fourminizer pouvait demander.

---

QueenCore ou policy gate décidait.

---

Toujours la frontière.

---

Puis il pensa aux objets ordinaires.

---

Peut-être plus tard :

LOW_RISK_AUTO_GRANT.

---

Mais même là :

scope limité.

---

Un pas.

Un objet.

Une policy.

---

Pas de pouvoir général.

---

Puis il pensa au « roi ».

---

L’opérateur principal pouvait avoir de grands pouvoirs.

---

Mais même un superuser ne devait pas transformer la vérité.

---

Chapitre 109.

---

Brutus écrivit :

**SUPERUSER MAY AUTHORIZE MORE ACTIONS. SUPERUSER DOES NOT CREATE MORE TRUTH.**

---

Très important.

---

Puis il lança une campagne.

---

Object:

CRYSTAL-0001.

---

Route planned:

C4 → C5 → C6 → C7.

---

Step 1.

Grant-001.

---

Commit.

Arrival locally observed.

---

Step 2.

New current state:

C5.

---

New grant:

C5 → C6.

---

Commit.

---

Step 3.

C6 → C7.

---

Commit.

---

Brutus regarda la trace.

---

Trois permissions.

Trois actions.

Trois commits.

Trois receipts.

---

Pas un seul grand passeport.

---

Il écrivit :

**A JOURNEY IS A SERIES OF VERIFIED STEPS.**

---

Puis :

**THE NEXT AUTHORIZATION BEGINS FROM THE LAST VERIFIED STATE.**

---

Voilà.

---

Le chapitre 120 apparaissait déjà.

---

Car maintenant une question restait.

---

Après chaque pas…

comment savoir que l’objet était réellement arrivé ?

---

Un moteur pouvait répondre :

ACK.

---

Mais un ACK était quoi ?

---

Commande reçue ?

Commande acceptée ?

Action enregistrée ?

Destination confirmée ?

---

Brutus regarda le dernier mouvement.

---

MOVE-0003.

---

Le transport layer affichait :

**ACKNOWLEDGED**

---

Brutus fronça les sourcils.

---

Pas assez.

---

Il écrivit :

**ACK != ARRIVAL.**

---

Puis il ouvrit le prochain dossier.

# L’ACCUSÉ DE RÉCEPTION N’EST PAS L’ARRIVÉE

---

Voilà le dernier mur.

---

Le grant avait permis un seul pas.

---

Le moteur avait exécuté.

---

Mais Brutus refusait encore d’annoncer l’arrivée tant qu’une observation ou un état autoritatif distinct ne l’avait pas confirmée.

---

Avant de fermer, il sauvegarda :

**SINGLE-STEP AUTHORIZATION CONTRACT v1**

---

Le Journal Vivant nota :

Authorization reduced to one actor, one object, one source state, one destination and one use.

Grant authority stored canonically rather than inside copyable token bytes.

One-shot grants become unusable after consumption.

Source-state drift invalidates stale authorization.

Destination changes require new validation.

Multi-step routes require distinct step grants under current policy.

Grant use tied to action IDs for crash-safe reconciliation.

Revocation separated from signature validity.

Approval preview exposes exact action scope before human consent.

Autonomous agents may request authority without automatically receiving it.

---

Brutus relut.

Puis ajouta les invariants :

**ONE ACTION != GENERAL AUTHORITY.**

**TOKEN PRESENT != TOKEN VALID.**

**VALID SIGNATURE != UNUSED GRANT.**

**GRANT ISSUED != ACTION EXECUTED.**

**STATE DRIFT INVALIDATES STALE AUTHORIZATION.**

**NO SILENT REROUTE.**

**MULTI-STEP PLAN != MULTI-STEP AUTHORITY.**

**REPLAYED TOKEN != REPLAYED AUTHORITY.**

**CONSUMED != EXECUTED WITHOUT ACTION_REF.**

**CONSENT TO ONE STEP != CONSENT TO A JOURNEY.**

---

Il regarda CRYSTAL-0001.

---

Trois pas avaient été demandés.

---

Trois permissions avaient été délivrées.

---

Trois mouvements avaient été commis.

---

Aucune permission ne pouvait servir une quatrième fois.

---

Brutus sourit.

---

Le pouvoir venait enfin d’être réduit à une taille raisonnable.

---

Pas un droit permanent.

---

Pas un accès sans frontière.

---

Un seul pas.

---

Puis il regarda le mot :

**ACKNOWLEDGED**

---

Et son sourire disparut.

---

Parce qu’il savait déjà que le dernier chapitre de cette série serait peut-être le plus important.

---

Une machine pouvait très bien dire :

« reçu ».

---

Sans pouvoir dire :

« arrivé ».

---

Brutus posa donc la dernière règle avant de fermer le dossier :

**ACKNOWLEDGEMENT IS ABOUT A MESSAGE.**

**ARRIVAL IS ABOUT A STATE.**

---

Puis il ouvrit :

# L’ACCUSÉ DE RÉCEPTION N’EST PAS L’ARRIVÉE
