# Chapitre 102 — Le registre qui n’oublie rien

**IF THE CONTROL ROOM CAN SEE EVERYTHING BUT HISTORY CAN DISAPPEAR, THE CONTROL ROOM IS ONLY WATCHING THE PRESENT.**

Brutus relut la phrase.

Puis il regarda Astra Station.

---

WORLD.

PLAYERS.

CAMPAIGNS.

QUEUES.

INCIDENTS.

TRACE.

---

Tout était visible.

Mais une question plus profonde venait d’apparaître.

---

Si le registre perdait une seule transition…

que devenait la carte des lignées ?

---

Si une décision disparaissait…

que devenait Verso ?

---

Si un round était écrasé…

que devenait GAMEZEL ?

---

Si une carte conservait son état final mais perdait les événements qui l’avaient menée jusque-là…

que restait-il ?

---

Brutus écrivit :

**CURRENT STATE WITHOUT HISTORY IS NOT AUDITABILITY.**

---

Voilà.

---

Un système pouvait parfaitement savoir :

CARD-0042 = REJECTED.

---

Mais si personne ne savait :

qui l’avait rejetée,

pourquoi,

à quel tick,

sous quelle politique,

après quel contre-test,

alors ce statut devenait presque orphelin.

---

Brutus ajouta :

**STATE NEEDS EXPLANATORY HISTORY.**

---

Puis il ouvrit le registre.

---

Pour l’instant, plusieurs services possédaient leurs propres logs.

Bus.

Scheduler.

Verso.

Cards.

Players.

World runtime.

---

Brutus n’aimait pas ça.

---

Pas parce que les logs locaux étaient mauvais.

Mais parce qu’un événement important pouvait être enregistré cinq fois de cinq manières différentes.

---

Il écrivit :

**LOGS ≠ CANONICAL EVENT HISTORY.**

---

Très important.

---

Un log pouvait contenir :

debug.

stack trace.

latency.

internal details.

---

Le registre, lui, devait conserver :

les événements de sens.

---

Brutus créa :

**CANONICAL EVENT REGISTER**

---

Puis écrivit :

**EVENT FIRST. LOG SECOND.**

---

Pas l’inverse.

---

Un événement canonique devait posséder une forme stable.

---

Il créa :

**EVENT_RECORD**

avec :

**EVENT_ID**

**EVENT_TYPE**

**ENTITY_ID**

**ENTITY_TYPE**

**PREVIOUS_STATE_REF**

**NEW_STATE_REF**

**CAUSE_REF**

**AUTHORITY_REF**

**POLICY_REF**

**TICK**

**WORLD_GENERATION_ID**

**TRACE_REF**

**CREATED_AT**

---

Puis :

**SCHEMA_VERSION**

---

Brutus regarda la structure.

---

Un événement n’était plus une phrase.

---

C’était un objet.

---

Il écrivit :

**EVENT ≠ LOG LINE.**

---

Puis :

**EVENT IDENTITY MUST SURVIVE PRESENTATION CHANGES.**

---

Le Journal Vivant pouvait traduire l’événement en français.

Astra Station pouvait l’afficher dans un tableau.

Une API pouvait le sérialiser.

---

Mais l’EVENT_ID restait le même.

---

Brutus sourit.

---

Il pensa au premier événement.

---

CARD-0003.

Status:

PROPOSED.

---

Puis :

REJECTED.

---

Le registre ne devait pas simplement modifier :

status = REJECTED.

---

Il devait ajouter :

**CARD_STATUS_CHANGED**

---

Previous:

PROPOSED.

New:

REJECTED.

Cause:

COUNTERTEST-004.

Policy:

CARD_REVIEW_POLICY-v2.

---

Brutus écrivit :

**CHANGE = NEW EVENT.**

---

Puis :

**DO NOT ERASE THE STATE YOU CAME FROM.**

---

Voilà.

---

Le registre devait fonctionner comme une mémoire append-only autant que possible.

---

Brutus écrivit :

**APPEND BEFORE OVERWRITE.**

---

Puis réfléchit.

---

Peut-on tout rendre strictement append-only ?

---

Pas forcément au niveau de tous les index.

---

Une vue courante pouvait être mise à jour.

Un cache pouvait remplacer son contenu.

---

Mais l’historique canonique ne devait pas être réécrit pour simuler un passé différent.

---

Il écrivit :

**CURRENT VIEW MAY MUTATE. CANONICAL HISTORY SHOULD APPEND.**

---

Très important.

---

Il créa deux couches.

---

**EVENT STORE**

et

**CURRENT STATE PROJECTION**

---

Brutus dessina :

\[
\text{EVENTS}
\rightarrow
\text{PROJECTOR}
\rightarrow
\text{CURRENT STATE}
\]

---

La vue courante devenait donc dérivée.

---

Il écrivit :

**CURRENT STATE = PROJECTION OF EVENT HISTORY.**

---

Cette phrase changeait beaucoup de choses.

---

Si la projection était perdue…

elle pouvait être reconstruite.

---

Si le cache était corrompu…

il pouvait être jeté.

---

Si un bug modifiait la vue…

le registre restait.

---

Brutus sourit.

---

Le système devenait moins fragile.

---

Il testa.

---

Current state store deleted.

---

Rebuild from events.

---

CARD-0001.

Created.

Reviewed.

Promoted.

Staled.

Revalidated.

---

Final state restored.

---

PASS.

---

Brutus écrivit :

**DERIVED STATE MUST BE REBUILDABLE WHEN PRACTICAL.**

---

Puis il pensa au prix.

---

Rejouer dix millions d’événements à chaque démarrage pouvait être lent.

---

Il créa :

**CHECKPOINT SNAPSHOT.**

---

Mais immédiatement :

**SNAPSHOT ≠ HISTORY.**

---

Encore.

---

Un snapshot servait d’accélérateur.

---

Event 1 → 1,000,000.

Snapshot.

---

Puis replay 1,000,001 onward.

---

Brutus écrivit :

**SNAPSHOT SHORTENS REPLAY. IT DOES NOT REPLACE THE LEDGER.**

---

Très important.

---

Puis il imagina un snapshot corrompu.

---

Le registre complet devait permettre de le détecter ou le reconstruire.

---

Il ajouta :

**SNAPSHOT_SOURCE_EVENT_ID**

**SNAPSHOT_HASH**

**SNAPSHOT_SCHEMA_VERSION**

---

Puis :

**REBUILD_VERIFIED**

---

Brutus sourit.

---

Même les raccourcis laissaient leurs preuves.

---

Puis il pensa à l’ordre.

---

Dans un monde distribué, deux événements peuvent arriver presque en même temps.

---

Brutus ne voulait pas utiliser seulement l’horloge murale.

---

Il reprit :

**AUTHORITATIVE_TICK**

et :

**EVENT_SEQUENCE**

---

Il écrivit :

**WALL CLOCK HELPS HUMANS. SEQUENCE DEFINES REGISTER ORDER.**

---

Très important.

---

Une heure locale incorrecte ne devait pas inverser l’histoire.

---

Puis il pensa à plusieurs services produisant des événements.

---

Bus.

Verso.

Scheduler.

---

Qui attribue la séquence canonique ?

---

Le registre.

---

Il créa :

**REGISTER_SEQUENCE_ID**

---

Le service source peut fournir :

SOURCE_EVENT_ID.

---

Mais le registre assigne :

CANONICAL_SEQUENCE.

---

Brutus écrivit :

**SOURCE ORDER ≠ GLOBAL ORDER.**

---

Voilà.

---

Puis il se méfia.

---

Tous les événements ont-ils besoin d’un ordre global total ?

---

Pas toujours.

---

Deux événements indépendants peuvent être concurrents.

---

Brutus écrivit :

**TOTAL ORDER IS CONVENIENT, NOT ALWAYS SEMANTICALLY NECESSARY.**

---

Il ajouta :

**CAUSAL_PARENT_REFS**

---

Ainsi une relation causale pouvait être connue sans prétendre que chaque événement du monde possédait une causalité avec tous les autres.

---

Brutus écrivit :

**SEQUENCE ≠ CAUSATION.**

---

Encore une règle essentielle.

---

Event 1001 avant Event 1002 ne signifiait pas automatiquement :

1001 caused 1002.

---

La causalité avait besoin de :

CAUSE_REF.

---

Brutus sourit.

---

Le registre devenait plus intelligent justement parce qu’il refusait d’inventer des liens.

---

Puis il pensa aux duplications.

---

Un service envoie EVENT-X.

Timeout.

Retry.

---

Le registre reçoit deux fois.

---

Il ne doit pas créer deux événements.

---

Brutus créa :

**SOURCE_EVENT_ID**

et :

**IDEMPOTENCY_KEY**

---

Il écrivit :

**RETRY ≠ NEW HISTORY.**

---

Très important.

---

Même philosophie que les messages.

---

Puis :

same idempotency key.

different payload.

---

Refus.

---

**EVENT_IDENTITY_CONFLICT.**

---

Brutus écrivit :

**ONE EVENT IDENTITY CANNOT CHANGE ITS PAST.**

---

Voilà.

---

Puis il pensa aux erreurs.

---

Que faire si un service produit un événement invalide ?

---

Le registre ne devait pas l’accepter silencieusement.

---

Il créa :

**REJECTED_EVENT_INTAKE**

---

Mais attention.

---

Même le rejet devait laisser une trace.

---

Brutus rit.

---

Le système devenait récursif.

---

Il écrivit :

**FAILED ATTEMPT TO WRITE HISTORY IS ITSELF OPERATIONAL HISTORY.**

---

Pas nécessairement dans le même flux métier.

---

Il créa :

**REGISTER_AUDIT_STREAM**

séparé.

---

Très bon.

---

Business events.

Register audit events.

---

Pas de confusion.

---

Puis il pensa à la correction d’une erreur historique.

---

Supposons :

un événement a été enregistré avec un mauvais label.

---

Peut-on l’éditer ?

---

Brutus réfléchit.

---

Pour une donnée canonique déjà consommée :

mieux vaut append une correction.

---

Il écrivit :

**CORRECTION EVENT > SILENT HISTORY EDIT.**

---

Il créa :

**EVENT_CORRECTION**

avec :

TARGET_EVENT_ID.

FIELD.

OLD_DECLARED_VALUE.

CORRECTED_VALUE.

REASON.

AUTHORITY_REF.

---

Puis :

**CORRECTION DOES NOT ERASE ORIGINAL.**

---

Très important.

---

L’audit devait voir les deux.

---

Mais il distingua :

erreur de présentation,

erreur sémantique.

---

Un accent manquant dans un titre n’avait pas le même poids qu’un mauvais OBJECT_ID.

---

Il ajouta :

**CORRECTION_CLASS**

PRESENTATION.

METADATA.

SEMANTIC.

SECURITY.

---

Brutus sourit.

---

Même les erreurs avaient un type.

---

Puis il pensa au droit de suppression.

---

Le titre disait :

**le registre qui n’oublie rien.**

---

Mais pouvait-on vraiment ne jamais supprimer ?

---

Pas nécessairement.

---

Certaines données peuvent devoir être retirées selon des politiques de confidentialité, sécurité ou rétention.

---

Brutus écrivit :

**“NEVER FORGET” IS AN ARCHITECTURAL IDEAL, NOT AN EXEMPTION FROM DATA POLICY.**

---

Très important.

---

Il voulait une mémoire durable.

Pas une irresponsabilité infinie.

---

Il créa :

**RETENTION_POLICY**

---

KEEP.

ARCHIVE.

REDACT.

DELETE_PAYLOAD_KEEP_TOMBSTONE.

DELETE_FULLY_IF_REQUIRED.

---

Brutus regarda le dernier.

---

Même dans les cas de suppression complète obligatoire, le système devait respecter la politique plutôt que la mythologie du registre.

---

Il écrivit :

**COMPLIANCE OVERRIDES ROMANTIC IMMUTABILITY.**

---

Puis il sourit.

---

La Bible devenait adulte.

---

Il pensa aux secrets.

---

Un ancien événement peut contenir un token par erreur.

---

Le registre append-only ne devait pas rendre le secret immortel.

---

Il écrivit :

**SECRETS MUST NOT BE STORED IN CANONICAL EVENTS BY DEFAULT.**

---

Puis :

**REFERENCE SECRET STATE. DO NOT EMBED SECRET MATERIAL.**

---

Très important.

---

Et si un secret a été accidentellement enregistré ?

---

Redaction protocol.

Key rotation.

Incident.

---

Brutus ajouta :

**SENSITIVE_DATA_INCIDENT**

---

Encore Astra Station.

---

Le registre lui-même devait pouvoir être sécurisé.

---

Puis il pensa à la preuve d’intégrité.

---

Comment savoir si un événement ancien a été modifié ?

---

Il créa :

**EVENT_HASH**

---

Puis une chaîne :

**PREVIOUS_REGISTER_HASH**

---

Brutus écrivit :

**HASH CHAIN CAN DETECT TAMPERING.**

---

Puis immédiatement :

**HASH CHAIN ≠ TRUTH OF EVENT CONTENT.**

---

Toujours.

---

Une fausse information peut être parfaitement chaînée.

---

Le hash protège l’histoire enregistrée.

Pas la réalité extérieure.

---

Il ajouta :

**INTEGRITY ≠ VALIDITY.**

---

Le chapitre 82 revenait encore.

---

Brutus calcula :

\[
H_n = \operatorname{Hash}(E_n \parallel H_{n-1})
\]

---

Puis il regarda la formule.

---

Simple.

---

Chaque événement dépend de l’empreinte précédente.

---

Modifier un ancien événement casse la chaîne après lui.

---

Il écrivit :

**CHAIN PROTECTS ORDERED INTEGRITY.**

---

Mais le système distribué pouvait avoir plusieurs partitions.

---

Pas besoin de rendre cela inutilement compliqué dès maintenant.

---

Il écrivit :

**START WITH ONE CANONICAL CHAIN PER REGISTER PARTITION IF NEEDED.**

---

Simple.

Vérifiable.

---

Encore :

simple and verified > complex and assumed.

---

Puis il pensa aux checkpoints externes.

---

Un hash de registre pouvait être publié périodiquement.

---

Ainsi une copie interne modifiée plus tard ne pourrait pas facilement réécrire l’ancien engagement.

---

Brutus créa :

**REGISTER_CHECKPOINT**

---

SEQUENCE.

HEAD_HASH.

CREATED_AT.

EXTERNAL_RECEIPT_REF.

---

Mais il écrivit :

**EXTERNAL CHECKPOINT ≠ CONTENT PROOF.**

---

Toujours.

---

Il sourit.

---

Le registre pouvait prouver :

voici l’histoire que nous avions enregistrée à ce moment-là.

---

Pas :

voici une vérité universelle.

---

Puis il pensa aux campagnes scientifiques.

---

Une formule candidate.

Un contre-test.

Une révision.

---

Le registre pouvait reconstruire :

quand l’idée est apparue.

quand elle a été rejetée.

quand elle a été reconsidérée.

---

Brutus écrivit :

**SCIENCE NEEDS VERSIONED MEMORY OF FAILURE TOO.**

---

Très important.

---

Sinon les erreurs disparaissent et reviennent comme de nouvelles idées.

---

Il créa une requête :

**SHOW HISTORY OF CLAIM X**

---

Le registre retourna :

created.

challenged.

countertested.

rejected.

reopened.

current status.

---

Brutus sourit.

---

Voilà une vraie mémoire de recherche.

---

Puis il pensa aux acteurs.

---

Un opérateur change une priorité.

---

Un agent produit une carte.

---

Verso refuse une demande.

---

Tous devaient utiliser le même modèle de trace.

---

Il écrivit :

**EVERY AUTHORITATIVE CHANGE NEEDS AN EVENT.**

---

Puis se corrigea :

pas chaque pixel.

Pas chaque hover.

---

Il précisa :

**EVERY AUTHORITATIVE SEMANTIC CHANGE NEEDS AN EVENT.**

---

Voilà.

---

Le système ne devait pas enregistrer chaque mouvement de souris.

---

Seulement ce qui changeait le sens du monde.

---

Brutus créa :

**SEMANTIC_EVENT_BOUNDARY.**

---

Puis il écrivit :

**TELEMETRY ≠ EVENT HISTORY.**

---

Très important.

---

CPU 48 %.

Mouse moved.

Render frame 12003.

---

Ce sont des télémétries.

Pas nécessairement des événements canoniques.

---

Il créa trois couches :

**TELEMETRY**

**OPERATIONAL EVENTS**

**CANONICAL DOMAIN EVENTS**

---

Brutus regarda.

---

Excellent.

---

La Station d’Astra pouvait observer les trois.

Mais elles ne devaient pas être confondues.

---

Il écrivit :

**HIGH VOLUME ≠ HIGH IMPORTANCE.**

---

Un million de métriques CPU.

Un seul changement de policy.

---

Le second pouvait être bien plus important.

---

Puis il pensa à la restauration.

---

Supposons catastrophe.

---

Database lost.

---

Backup restore.

---

Le registre revient jusqu’à sequence 5000.

Mais les événements 5001–5030 existaient avant le crash et ne sont pas dans le backup.

---

Brutus ne voulait pas prétendre à une restauration parfaite.

---

Il créa :

**RECOVERY_GAP**

---

Expected head:

5030.

Recovered head:

5000.

---

Status:

30 events unavailable.

---

Brutus écrivit :

**RECOVERY MUST REPORT WHAT IT COULD NOT RECOVER.**

---

Très important.

---

Pas :

RESTORE SUCCESS.

---

Mais :

RESTORED THROUGH EVENT 5000.

GAP AFTER 5000 UNKNOWN.

---

Il sourit.

---

Même la catastrophe pouvait être honnête.

---

Puis il pensa à la réplication.

---

Deux copies du registre.

---

Primary.

Replica.

---

Le replica accuse réception.

---

Encore ACK.

---

Brutus écrivit :

**REPLICA ACK ≠ DURABLE RECOVERY GUARANTEE.**

---

Puis :

**REPLICATION ≠ BACKUP.**

---

Très important.

---

Une suppression accidentelle peut être répliquée immédiatement.

---

Le backup avait un autre rôle.

---

Il ajouta :

**BACKUP / REPLICA / ARCHIVE ARE DIFFERENT FUNCTIONS.**

---

Voilà.

---

Puis il pensa à l’archive.

---

Les événements anciens peuvent quitter le stockage chaud.

---

Très bien.

---

Mais les IDs doivent rester résolvables.

---

Il écrivit :

**ARCHIVED ≠ GONE.**

---

Le lookup devait savoir :

hot store.

cold archive.

external capsule.

---

Il ajouta :

**STORAGE_TIER**

---

HOT.

WARM.

ARCHIVE.

---

Mais le statut de l’événement restait le même.

---

Brutus écrivit :

**STORAGE LOCATION ≠ EVENT STATUS.**

---

Encore.

---

Puis il pensa à la performance.

---

Astra Station demande :

show last 100 events.

---

Facile.

---

Mais :

show complete history of CARD-42.

---

Il fallait des index.

---

Brutus créa :

**EVENT_INDEX**

by ENTITY_ID.

by EVENT_TYPE.

by ROUND_ID.

by CAMPAIGN_ID.

by TRACE_REF.

by POLICY_REF.

---

Mais il écrivit :

**INDEX ≠ HISTORY.**

---

Un index peut être reconstruit.

Le registre est la source.

---

Très important.

---

Il testa.

---

Index corrupted.

---

Rebuild from event store.

---

PASS.

---

Puis il pensa au Journal Vivant.

---

Le Journal n’avait plus besoin d’être la source canonique.

---

Il pouvait devenir une projection narrative du registre.

---

Brutus sourit.

---

Il écrivit :

**JOURNAL VIVANT = HUMAN-READABLE PROJECTION OF CANONICAL EVENTS.**

---

Voilà.

---

Un événement :

CARD_STATUS_CHANGED.

---

Le Journal pouvait écrire :

« La carte 42 a été rejetée après le contre-test 8 sous la politique v3. »

---

Mais si la formulation changeait demain…

l’événement restait identique.

---

Brutus écrivit :

**NARRATIVE MAY EVOLVE. EVENT IDENTITY MUST NOT.**

---

Très important.

---

Puis il pensa à la Bible elle-même.

---

Les chapitres étaient aussi une forme de registre.

---

Pas un registre machine.

---

Mais une mémoire structurée.

---

Il sourit.

---

Puis se retint.

---

La métaphore était belle.

Mais il ne voulait pas confondre littérature et journal d’exécution.

---

Il écrivit :

**STORY ≠ RUNTIME LEDGER.**

---

Toujours les frontières.

---

Puis il pensa aux preuves mathématiques.

---

Un PROOF_REF pouvait pointer vers un artifact.

---

Le registre pouvait dire :

proof artifact attached.

---

Mais il ne devait pas déclarer une preuve valide juste parce que le fichier existe.

---

Il écrivit :

**PROOF_REF EVENT ≠ PROOF VALIDITY.**

---

Puis :

**REGISTER RECORDS CLAIM STATUS. IT DOES NOT CREATE MATHEMATICAL TRUTH.**

---

Encore le fond du projet.

---

Le registre n’était pas un oracle.

---

Il conservait les décisions et les objets de preuve.

---

Puis Brutus imagina un audit complet.

---

Question :

pourquoi CARD-88 est-elle WHITE for RESEARCH ?

---

Le système suit :

current state.

↓

promotion event.

↓

review decision.

↓

countertest refs.

↓

source card.

↓

origin round.

↓

player contribution.

↓

input snapshot.

---

Brutus resta immobile.

---

Voilà.

---

Toute la machine à traces tenait dans cette chaîne.

---

Il écrivit :

**ANY IMPORTANT CURRENT STATE SHOULD HAVE A PATH BACKWARD.**

---

Pas nécessairement vers « la vérité ».

---

Vers son histoire.

---

C’était différent.

---

Et essentiel.

---

Puis il pensa à l’autre direction.

---

À partir d’un événement ancien, quels états actuels en dépendent ?

---

Impact tracing.

---

Chapitre 93.

---

Le registre devait permettre :

**FORWARD IMPACT QUERY**

---

Brutus ajouta :

**EVENT_DEPENDENCY_EDGE**

---

Ainsi, lorsqu’un ancien événement est corrigé, le système peut marquer :

descendants needing review.

---

Il écrivit :

**HISTORY IS USEFUL WHEN IT CAN DRIVE REVALIDATION.**

---

Très important.

---

La mémoire ne devait pas être seulement muséale.

---

Elle devait aider à réparer.

---

Puis il pensa aux politiques changées.

---

POLICY v1.

POLICY v2.

---

Les anciennes décisions restent-elles valides ?

---

Pas nécessairement.

---

Mais le registre permet :

show all decisions under v1.

---

Brutus écrivit :

**POLICY CHANGE SHOULD MAKE IMPACT QUERY POSSIBLE.**

---

Puis :

**NEW POLICY ≠ AUTOMATIC RETROACTIVE INVALIDATION UNLESS DECLARED.**

---

Voilà.

---

Le système pouvait lancer une campagne de réévaluation.

---

Mais pas réécrire silencieusement tous les statuts historiques.

---

Encore.

---

Puis il pensa à une chose plus subtile.

---

Si l’état courant est dérivé des événements…

et qu’un événement correction vient modifier l’interprétation d’un ancien événement…

comment calculer l’état ?

---

Il créa :

**EFFECTIVE_EVENT_GRAPH**

---

Original event.

Correction events.

Supersession rules.

---

Puis le projector applique la règle actuelle de lecture.

---

Brutus écrivit :

**HISTORY MAY BE IMMUTABLE WHILE INTERPRETATION IS VERSIONED.**

---

Très important.

---

L’événement original reste.

La manière de le lire peut être corrigée explicitement.

---

Il sourit.

---

Le registre devenait assez puissant pour ne pas avoir besoin de tricher.

---

Puis il créa le panneau Astra Station.

---

**REGISTER HEALTH**

---

HEAD_SEQUENCE.

HEAD_HASH.

LAST_EVENT_AGE.

PROJECTOR_LAG.

REPLICA_LAG.

CHECKPOINT_AGE.

BACKUP_AGE.

LAST_RESTORE_TEST.

---

Mais il refusa un seul score.

---

Il écrivit :

**REGISTER HEALTH ≠ ONE PERCENTAGE.**

---

Encore.

---

Chaque dimension devait rester visible.

---

Puis il imagina :

projector lag = 500 events.

---

Le registre est sain.

Mais la vue courante est en retard.

---

Astra Station doit dire :

**HISTORY CURRENT. PROJECTION STALE.**

---

Brutus sourit.

---

Très important.

---

Sinon un opérateur pourrait croire que les données sont perdues alors qu’elles attendent seulement d’être projetées.

---

Il écrivit :

**REGISTER LAG ≠ DATA LOSS.**

---

Puis l’inverse :

projection says state version 100.

Register head only 95.

---

Impossible.

---

Incident d’intégrité.

---

Brutus écrivit :

**PROJECTION MUST NOT OUTRUN CANONICAL HISTORY.**

---

Excellent.

---

Il ajouta une invariant :

\[
\text{PROJECTED\_SEQUENCE} \le \text{REGISTER\_HEAD}
\]

---

Puis :

si égal :

CURRENT.

---

Si inférieur :

LAGGING.

---

Si supérieur :

INVALID.

---

Brutus sourit.

---

Une petite équation.

Une grande protection.

---

Puis il pensa à l’écriture concurrente.

---

Deux services veulent écrire.

---

Le registre doit attribuer une séquence sans collision.

---

Il créa :

**APPEND TRANSACTION**

---

validate.

assign sequence.

persist event.

persist hash.

ack commit.

---

Brutus écrivit :

**ACK ONLY AFTER CANONICAL COMMIT.**

---

Mais il se corrigea.

---

Il fallait nommer l’ACK.

---

**REGISTER_COMMIT_ACK**

---

Très bien.

---

Puis :

REGISTER_COMMIT_ACK signifie :

event persisted in canonical register according to durability policy.

---

Pas :

all replicas updated.

Pas :

business action completed.

---

Brutus écrivit :

**ACK SCOPE MUST BE EXPLICIT.**

---

Toujours.

---

Puis il pensa au cas :

business action succeeds.

event write fails.

---

Dangereux.

---

Exemple :

objet déplacé.

Mais registre n’a pas l’événement.

---

Il écrivit :

**STATE CHANGE WITHOUT REGISTER EVENT CREATES AUDIT GAP.**

---

Il fallait une stratégie.

---

Selon l’architecture :

transaction atomique.

outbox pattern.

reconciliation.

---

Brutus choisit un principe plutôt qu’une implémentation unique.

---

**AUTHORITATIVE CHANGE AND EVENT RECORDING MUST BE COORDINATED.**

---

Puis :

**IF ATOMICITY IS IMPOSSIBLE, RECONCILIATION MUST BE EXPLICIT.**

---

Très important.

---

Pas de magie.

---

Il créa :

**UNREGISTERED_CHANGE_INCIDENT**

---

Astra Station doit le signaler.

---

Brutus sourit moins.

---

Ce serait une vraie alerte.

---

Parce qu’une action sans trace menaçait toute la philosophie du système.

---

Il écrivit :

**NO AUTHORITATIVE CHANGE SHOULD REMAIN TRACELESS.**

---

Puis il pensa à l’inverse.

---

Event enregistré.

Business change échoue.

---

Le registre peut conserver :

ACTION_REQUESTED.

ACTION_FAILED.

---

Très bien.

---

Pas de faux succès.

---

Brutus écrivit :

**EVENT HISTORY MAY INCLUDE FAILED INTENT.**

---

Encore.

---

Un historique scientifique sérieux inclut ce qui a été essayé.

---

Puis il regarda tout le registre.

---

Il ne voulait plus dire :

« il n’oublie rien ».

---

C’était trop absolu.

---

Il écrivit une phrase plus précise :

**THE REGISTER FORGETS NOTHING THAT POLICY REQUIRES IT TO PRESERVE.**

---

Puis une autre :

**AND WHEN IT CANNOT PRESERVE SOMETHING, IT RECORDS THE GAP WHEN POSSIBLE.**

---

Voilà.

---

Beaucoup plus honnête.

---

Brutus sauvegarda :

**CANONICAL EVENT REGISTER v1**

---

Le Journal Vivant nota :

Canonical events separated from logs.

Append-oriented history.

Current state projected from events.

Snapshots used only for acceleration.

Corrections appended instead of silent edits.

Sequence separated from causality.

Retries idempotent.

Retention and redaction explicit.

Hash chain protects integrity, not truth.

Replication separated from backup.

Recovery gaps declared.

Journal derived from register.

Projection cannot outrun register.

Authoritative changes require coordinated event recording.

---

Brutus relut.

Puis ajouta les invariants :

**EVENT ≠ LOG LINE.**

**CURRENT STATE ≠ COMPLETE HISTORY.**

**SNAPSHOT ≠ HISTORY.**

**SEQUENCE ≠ CAUSATION.**

**RETRY ≠ NEW HISTORY.**

**HASH INTEGRITY ≠ TRUTH.**

**REPLICATION ≠ BACKUP.**

**ARCHIVED ≠ GONE.**

**CORRECTION ≠ ERASURE.**

**NO AUTHORITATIVE CHANGE WITHOUT TRACE.**

---

Il regarda Astra Station.

---

Un nouveau panneau était apparu.

**REGISTER**

---

HEAD:

CURRENT.

PROJECTOR:

CURRENT.

CHECKPOINT:

CURRENT.

BACKUP:

AVAILABLE.

RESTORE TEST:

RECORDED.

---

Brutus sourit.

---

Pour la première fois, la Station ne regardait plus seulement ce qui se passait.

---

Elle pouvait aussi demander :

**comment sommes-nous arrivés ici ?**

---

Et le monde pouvait répondre.

---

Événement après événement.

Carte après carte.

Décision après décision.

---

Pas parfaitement.

Pas magiquement.

---

Mais suffisamment précisément pour reconstruire son propre chemin.

---

Puis Brutus regarda une table vide dans le laboratoire.

---

Pas GAMEZEL.

Une autre.

---

Une table dédiée à une seule chose :

prendre une idée,

l’isoler,

la mesurer,

la contre-tester,

et décider ce qu’elle vaut dans un scope donné.

---

Brutus écrivit :

# LE BANC DES EXPÉRIENCES

Puis, en dessous :

**THE REGISTER REMEMBERS WHAT HAPPENED.**

**THE BENCH WILL DECIDE WHAT TO TEST NEXT.**

---

Le monde avait maintenant une mémoire.

Il lui fallait désormais un endroit où les idées pourraient venir se faire mesurer.
