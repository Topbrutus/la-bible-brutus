# Chapitre 115 — Quand une fourmi touche la matière

**SIMULATED CONTACT != PHYSICAL CONTACT.**

Puis :

**EXTERNAL ACTION REQUIRES AN EXPLICIT BRIDGE.**

Brutus regarda la fourmi.

---

ANT-001.

Position :

58,42.

---

Devant elle :

CRYSTAL-014.

---

Distance logique :

1.

---

La fourmi avait terminé son déplacement.

Elle se trouvait maintenant à côté du cristal.

---

Rien de plus.

---

Brutus écrivit :

**ADJACENT != TOUCHING.**

---

Très important.

---

Dans un renderer, deux formes pouvaient sembler se toucher.

---

Mais ce n’était qu’une géométrie d’affichage.

---

Pour le monde local, il fallait un événement.

---

Il créa :

**CONTACT_REQUEST**

avec :

**REQUEST_ID**

**AGENT_ID**

**TARGET_OBJECT_ID**

**CONTACT_TYPE**

**WORLD_TICK**

**EXPECTED_AGENT_STATE**

**EXPECTED_OBJECT_STATE**

**POLICY_REF**

**AUTHORIZATION_REF**

**TRACE_REF**

---

Puis :

**CONTACT_TYPE**

INSPECT.

PICKUP.

DROP.

PUSH.

ACTIVATE_REQUEST.

---

Brutus s’arrêta sur le dernier.

---

**ACTIVATE_REQUEST.**

---

Pas :

ACTIVATE.

---

Très important.

---

Une fourmi pouvait demander qu’un objet soit activé.

---

Elle ne devait pas posséder implicitement le pouvoir d’activer quoi que ce soit.

---

Brutus écrivit :

**REQUESTING AN ACTION != OWNING THE ACTION.**

---

Encore une frontière.

---

Puis il pensa au mot :

**matière**.

---

Dans le monde local, le cristal était un objet logiciel.

---

Il pouvait avoir :

position.

custody.

state.

manifest.

---

Mais il n’était pas de la matière physique.

---

Brutus écrivit :

**WORLD OBJECT != PHYSICAL OBJECT.**

---

Le titre du chapitre était narratif.

---

La machine devait rester exacte.

---

Il ajouta :

**MATERIAL_CONTACT_CLASS**

SIMULATED_OBJECT.

EXTERNAL_DIGITAL_SYSTEM.

PHYSICAL_ACTUATOR.

PHYSICAL_SENSOR.

---

Très important.

---

Toutes les interactions ne traversaient pas la même frontière.

---

Une fourmi qui prend un cristal logiciel :

SIMULATED_OBJECT.

---

Une fourmi qui envoie une requête à un service distant :

EXTERNAL_DIGITAL_SYSTEM.

---

Une fourmi qui déclenche potentiellement un actionneur réel :

PHYSICAL_ACTUATOR.

---

Ce dernier exigeait beaucoup plus.

---

Brutus écrivit :

**RISK CLASS MUST FOLLOW TARGET CLASS.**

---

Puis il testa le cas simple.

---

ANT-001 :

REQUEST_PICKUP CRYSTAL-014.

---

World authority vérifie :

distance.

object state.

agent state.

custody.

collision.

authorization.

---

Tout passe.

---

Un événement est créé :

**PICKUP_EVENT**

---

AGENT_ID:

ANT-001.

OBJECT_ID:

CRYSTAL-014.

FROM_PLACEMENT:

WORLD-SLOT-58-43.

TO_CUSTODY:

ANT-001.

TICK:

142.

---

Puis le monde met :

CRYSTAL-014 placement state:

CARRIED.

---

Brutus sourit.

---

Voilà.

---

La fourmi « tenait » maintenant le cristal.

---

Mais il écrivit immédiatement :

**CARRIED != PHYSICALLY HELD.**

---

Très important.

---

Dans le monde local, « porter » signifiait :

relation de custody.

---

Pas pression mécanique.

Pas poids.

Pas friction.

---

Il ajouta :

**CARRY_RELATION = SOFTWARE CUSTODY STATE.**

---

Puis il pensa à la masse.

---

Le cristal devait-il avoir une masse ?

---

Non.

---

Pas sans modèle.

---

Brutus écrivit :

**NO MASS WITHOUT MASS MODEL.**

---

Puis :

**NO FORCE WITHOUT FORCE MODEL.**

---

Puis :

**NO ENERGY WITHOUT ENERGY MODEL.**

---

Excellent.

---

Si le système voulait plus tard simuler ces quantités…

il pourrait.

---

Mais elles devaient être définies.

---

Pas empruntées à la physique pour rendre l’interface plus impressionnante.

---

Puis il pensa au déplacement avec cristal.

---

ANT-001 transporte CRYSTAL-014.

---

Quand la fourmi bouge, le cristal suit-il automatiquement ?

---

Oui, selon une règle locale de custody.

---

Il créa :

**CUSTODY_MOTION_RULE**

---

If carrier move committed:

carried object world placement derives from carrier destination.

---

Mais le cristal ne reçoit pas un MOVE_EVENT indépendant comme s’il avait choisi de bouger.

---

Il reçoit :

**CARRIED_OBJECT_POSITION_UPDATE**

---

Brutus écrivit :

**CARRIER MOTION != OBJECT SELF-MOTION.**

---

Très important.

---

La provenance du mouvement devait rester claire.

---

Pourquoi le cristal a-t-il changé de position ?

---

Parce que ANT-001 le transportait.

---

Il ajouta :

**CAUSE_REF = CARRIER_MOVE_EVENT**

---

Parfait.

---

Puis il pensa au drop.

---

REQUEST_DROP.

---

Target location.

---

Authority checks zone.

---

Drop accepted.

---

Custody relation closes.

---

New placement event.

---

Brutus écrivit :

**DROP EVENT ENDS CUSTODY. IT DOES NOT ALTER CRYSTAL CONTENT.**

---

Encore.

---

Transport.

Pas transformation.

---

Puis il testa un cas interdit.

---

ANT-001 porte CRYSTAL-014.

---

Elle demande :

**MODIFY_CRYSTAL_FORMULA.**

---

Pas dans son action set.

---

Rejected.

---

Brutus écrivit :

**CUSTODY != EDIT AUTHORITY.**

---

Très important.

---

Porter un objet ne donnait pas le droit de le modifier.

---

Puis :

**CUSTODY != PROMOTION AUTHORITY.**

---

Puis :

**CUSTODY != PUBLICATION AUTHORITY.**

---

Brutus sourit.

---

Chaque pouvoir restait séparé.

---

Puis il pensa au premier véritable pont externe.

---

Le monde local pouvait vouloir envoyer un cristal à Brutus Control Plane.

---

Pas physiquement.

---

Numériquement.

---

Il créa :

# EXTERNAL DIGITAL BRIDGE

---

Puis :

**BRIDGE_ID**

**SOURCE_WORLD**

**TARGET_SYSTEM**

**ALLOWED_PAYLOAD_TYPES**

**DIRECTION**

**AUTHORITY_REF**

**TRANSFORM_REF**

**PROTOCOL_VERSION**

**HEALTH_STATE**

**TRACE_REF**

---

Brutus écrivit :

**BRIDGE != INVISIBLE PORTAL.**

---

Excellent.

---

Un pont avait :

un début.

une fin.

un protocole.

un état.

---

Puis il pensa au fameux Carbon → Crypto → Carbon.

---

La même règle.

---

Une transformation logicielle.

---

Pas un transport de matière.

---

Il écrivit :

**DIGITAL REPRESENTATION TRANSFER != MATTER TRANSPORT.**

---

Très important.

---

Puis il prit CRYSTAL-014.

---

ANT-001 le transporte jusqu’au port :

PORT-BRUTUS-IN.

---

La fourmi entre dans la zone de transfert.

---

Est-ce suffisant pour envoyer le cristal ?

---

Non.

---

Brutus écrit :

**ARRIVAL AT PORT != TRANSFER AUTHORIZATION.**

---

Il faut :

TRANSFER_REQUEST.

---

Il créa :

**TRANSFER_REQUEST**

REQUEST_ID.

OBJECT_ID.

SOURCE_SYSTEM.

TARGET_SYSTEM.

SOURCE_STATE_VERSION.

PAYLOAD_REF.

AUTHORIZATION_REF.

BRIDGE_REF.

TRACE_REF.

---

Puis :

**TRANSFER_STATE**

REQUESTED.

AUTHORIZED.

SERIALIZED.

SENT.

ACKNOWLEDGED.

RECEIVED.

VERIFIED.

ADMITTED.

FAILED.

UNKNOWN.

---

Brutus sourit.

---

Encore les frontières.

---

Puis il écrivit :

**SENT != RECEIVED.**

**RECEIVED != VERIFIED.**

**VERIFIED != ADMITTED.**

---

Très important.

---

La fourmi pouvait livrer un cristal jusqu’au port.

---

Mais le reste appartenait au pont.

---

Il écrivit :

**AGENT DELIVERS TO BOUNDARY. BRIDGE HANDLES CROSSING.**

---

Voilà.

---

L’agent ne traversait pas magiquement les systèmes.

---

Puis il pensa à un échec réseau.

---

Transfer authorized.

Serialized.

Sent.

---

No response.

---

Que faire ?

---

Pas :

DELIVERED.

---

Status :

UNKNOWN.

---

Brutus écrivit :

**NETWORK SILENCE != DELIVERY FAILURE.**

---

Puis :

**NETWORK SILENCE != DELIVERY SUCCESS.**

---

Très important.

---

Reconciliation.

---

Encore le registre.

---

Puis il pensa au duplicate delivery.

---

Retry.

---

Le target reçoit deux fois le même TRANSFER_ID.

---

Idempotency.

---

Il écrivit :

**RETRY MUST NOT DUPLICATE CUSTODY.**

---

Très important.

---

Le même cristal ne devait pas se retrouver « deux fois » dans le registre simplement à cause d’un timeout.

---

Puis il pensa au cas physique.

---

Une fourmi logicielle qui déclenche un relais réel.

---

Là, tout changeait.

---

Brutus ouvrit un autre dossier.

# PHYSICAL ACTION BRIDGE

---

Puis écrivit :

**SIMULATION AUTHORITY ENDS AT THE PHYSICAL BOUNDARY.**

---

Très important.

---

Le monde local pouvait proposer :

TURN_ON_LIGHT.

MOVE_MOTOR.

OPEN_VALVE.

---

Mais ces actions exigeaient un système externe spécialisé.

---

Brutus créa :

**PHYSICAL_ACTION_REQUEST**

avec :

**ACTION_ID**

**SOURCE_AGENT**

**INTENT_TYPE**

**TARGET_DEVICE_ID**

**PARAMETERS**

**SAFETY_CLASS**

**AUTHORIZATION_REF**

**EXPECTED_PRECONDITIONS**

**EXPIRATION**

**TRACE_REF**

---

Puis :

**NO DIRECT AGENT-TO-ACTUATOR EDGE.**

---

Très important.

---

Il dessina :

\[
\text{AGENT}
\rightarrow
\text{PROPOSAL}
\rightarrow
\text{POLICY}
\rightarrow
\text{AUTHORITY}
\rightarrow
\text{SAFETY CHECK}
\rightarrow
\text{ACTUATOR BRIDGE}
\]

---

Puis :

\[
\text{SENSOR FEEDBACK}
\rightarrow
\text{OBSERVATION}
\rightarrow
\text{WORLD UPDATE}
\]

---

Brutus regarda le schéma.

---

Voilà le cycle complet.

---

Pas de magie.

---

Puis il pensa au risque.

---

Un actionneur physique n’était pas une case de simulation.

---

Il pouvait agir sur :

machine.

porte.

lumière.

moteur.

---

Donc l’autorisation devait être plus stricte.

---

Il créa :

**SAFETY_GATE**

---

Device allowlist.

Parameter bounds.

Rate limits.

Operator approval class.

Emergency stop.

Current device health.

Fresh sensor state.

---

Brutus écrivit :

**SIMULATION SUCCESS DOES NOT AUTHORIZE PHYSICAL EXECUTION.**

---

Très important.

---

Même si une action avait réussi mille fois dans le monde local.

---

Le réel exigeait son propre contrat.

---

Puis il pensa au capteur.

---

Le pont physique envoie :

MOTOR_STARTED.

---

Est-ce suffisant pour dire :

le moteur a bougé ?

---

Pas forcément.

---

Peut-être seulement :

commande acceptée.

---

Brutus écrivit :

**COMMAND ACCEPTED != PHYSICAL EFFECT VERIFIED.**

---

Puis :

**ACTUATOR ACK != SENSOR CONFIRMATION.**

---

Le chapitre 120 approchait.

---

Il créa :

**PHYSICAL_EFFECT_STATUS**

COMMAND_SENT.

COMMAND_ACCEPTED.

EFFECT_UNVERIFIED.

EFFECT_OBSERVED.

EFFECT_FAILED.

STATE_UNKNOWN.

---

Très important.

---

Le système devait pouvoir rester dans :

EFFECT_UNVERIFIED.

---

Sans inventer.

---

Puis il pensa au capteur.

---

Un capteur dit :

position = 10.

---

Peut-on l’injecter directement ?

---

Non.

---

Il faut :

sensor identity.

timestamp/tick.

calibration.

unit.

quality.

---

Il créa :

**SENSOR_OBSERVATION**

SENSOR_ID.

MEASUREMENT_TYPE.

VALUE.

UNIT.

OBSERVED_AT.

CALIBRATION_REF.

QUALITY_STATE.

TRACE_REF.

---

Puis :

**SENSOR VALUE != WORLD TRUTH UNTIL ADMISSION POLICY APPLIES.**

---

Très important.

---

Pourquoi ?

---

Capteur défaillant.

Stale data.

Wrong unit.

---

Le monde local devait traiter le signal comme une observation.

---

Pas comme une vérité absolue.

---

Puis il pensa au terme :

**matière**.

---

Enfin, il pouvait le préciser.

---

Une fourmi « touche la matière » uniquement si :

une proposition logicielle franchit un pont explicite,

une action physique est autorisée,

un système externe l’exécute,

et une observation externe confirme un effet correspondant.

---

Même là…

la fourmi elle-même ne touche rien.

---

Brutus écrivit :

**SOFTWARE AGENT CAUSES A CONTROL REQUEST.**

**PHYSICAL SYSTEM PERFORMS THE PHYSICAL ACTION.**

---

Voilà.

---

La métaphore retrouvait sa place.

---

Puis il pensa au rollback.

---

Dans le logiciel, beaucoup de choses peuvent être annulées.

---

Dans le monde physique :

pas toujours.

---

Une porte ouverte a été ouverte.

Un objet déplacé a été déplacé.

---

Brutus écrivit :

**PHYSICAL SIDE EFFECT MAY BE IRREVERSIBLE.**

---

Donc :

preconditions.

approval.

dry run.

---

Il créa :

**ACTION_PREVIEW**

---

Exact target.

Exact parameters.

Expected effect.

Known risks.

Reversibility.

Verification plan.

---

Puis :

**PREVIEW != EXECUTION.**

---

Encore.

---

Très important.

---

Puis il pensa au mode test.

---

Actuator bridge could have:

SIMULATE_ONLY.

SHADOW_MODE.

LIVE.

---

Brutus écrivit :

**SHADOW MODE MUST NOT EMIT PHYSICAL COMMANDS.**

---

Excellent.

---

Un test grandeur nature sans effet réel.

---

Puis il pensa à l’aquarium.

---

Comment afficher une action physique ?

---

Pas comme une animation avant confirmation.

---

Brutus créa :

**EXTERNAL_ACTION_RENDER_STATE**

PROPOSED.

AUTHORIZED.

COMMAND_SENT.

ACKNOWLEDGED.

OBSERVED.

FAILED.

UNKNOWN.

---

Le renderer devait suivre le state exact.

---

Il écrivit :

**DO NOT ANIMATE PHYSICAL SUCCESS BEFORE OBSERVATION.**

---

Très important.

---

Une commande MOVE_MOTOR ne devait pas faire bouger le moteur dessiné avant le retour d’un capteur ou d’une source d’autorité appropriée.

---

Sinon l’écran mentait.

---

Puis il pensa au délai.

---

Le monde local pourrait être à tick 500.

---

Le monde physique répond 300 ms plus tard.

---

Comment réconcilier ?

---

Il créa :

**EXTERNAL_EVENT_TIME**

---

SOURCE_TIME.

RECEIVE_TIME.

WORLD_ADMISSION_TICK.

---

Brutus écrivit :

**EXTERNAL TIME != WORLD TICK.**

---

Très important.

---

Il fallait une relation explicite.

---

Pas mélanger les horloges.

---

Puis il pensa à plusieurs ponts.

---

Web API.

Serial.

GPIO.

VPS service.

---

Chaque pont devait déclarer sa capacité.

---

Il créa :

**BRIDGE_CAPABILITY_MANIFEST**

---

READ_SENSOR.

SEND_COMMAND.

TRANSFER_OBJECT.

QUERY_STATUS.

CANCEL_PENDING.

---

Puis :

**CAPABILITY != CURRENT AVAILABILITY.**

---

Encore.

---

Un pont peut supporter une commande sans être connecté maintenant.

---

Brutus écrit :

**SUPPORTED != READY.**

---

Très important.

---

Puis il testa le scénario numérique.

---

ANT-001 carries CRYSTAL-014.

---

Arrives at digital transfer port.

---

TRANSFER_REQUEST.

---

Authorized.

Serialized.

Sent.

Received.

Hash verified.

Admitted.

---

New custody:

BRUTUS-INGRESS-01.

---

ANT-001 custody ends.

---

Brutus writes:

**DIGITAL HANDOFF COMPLETE.**

---

Pas :

physical transport complete.

---

PASS.

---

Puis test physique.

---

ANT-002 reaches actuator zone.

---

Policy proposes:

LIGHT_ON.

---

Safety gate:

allowed target.

allowed action.

operator approval present.

---

Command sent.

---

Device ACK:

accepted.

---

Renderer status:

ACKNOWLEDGED / EFFECT_UNVERIFIED.

---

Sensor:

light current measured above declared threshold.

---

Effect status:

OBSERVED.

---

Only then aquarium displays:

EXTERNAL EFFECT VERIFIED UNDER SENSOR CONTRACT.

---

Brutus sourit.

---

Parfait.

---

Puis il retire le sensor.

---

Same command.

Same ACK.

No observation.

---

State remains:

EFFECT_UNVERIFIED.

---

PASS.

---

Puis actuator times out.

---

State:

UNKNOWN.

---

No retry without idempotency/reconciliation.

---

PASS.

---

Brutus écrivit :

**UNKNOWN IS A SAFE SCIENTIFIC ANSWER.**

---

Très important.

---

Puis il pensa aux fourmis elles-mêmes.

---

Une fourmi peut apprendre du résultat ?

---

Oui, si la policy l’autorise.

---

Mais elle ne devrait recevoir qu’un résultat normalisé.

---

ACTION_SUCCEEDED.

ACTION_FAILED.

ACTION_UNKNOWN.

---

Pas accès arbitraire au système externe.

---

Il créa :

**EXTERNAL_RESULT_ENVELOPE**

---

ACTION_ID.

RESULT_CLASS.

OBSERVATION_REFS.

WORLD_ADMISSION_TICK.

---

Brutus écrivit :

**AGENT RECEIVES RESULT, NOT UNBOUNDED EXTERNAL AUTHORITY.**

---

Excellent.

---

Puis il pensa aux erreurs de mapping.

---

World says EAST.

Actuator interprets +X.

---

Qu’est-ce qui garantit la correspondance ?

---

Transform.

Calibration.

---

Il créa :

**WORLD_TO_EXTERNAL_TRANSFORM**

---

TRANSFORM_ID.

WORLD_FRAME.

EXTERNAL_FRAME.

UNIT_MAP.

AXIS_MAP.

CALIBRATION_REF.

VERSION.

---

Brutus écrivit :

**EAST IN SIMULATION != +X IN REALITY WITHOUT A DECLARED TRANSFORM.**

---

Très important.

---

Le mapping lui-même devenait un objet vérifiable.

---

Puis il pensa au changement de calibration.

---

New calibration.

---

Old transform cannot silently continue.

---

Version change.

---

Brutus écrit :

**CALIBRATION CHANGE INVALIDATES DEPENDENT TRANSFORM ASSUMPTIONS UNTIL REVIEWED.**

---

Encore la lignée.

---

Puis il pensa à l’arrêt d’urgence.

---

Physical bridge needed:

**E_STOP**

---

But agent must not have authority to disable it.

---

Brutus écrivit :

**SAFETY CONTROL MUST NOT BE OWNED BY THE AGENT IT CONSTRAINS.**

---

Très important.

---

Separation of duties.

---

Puis il pensa au système local.

---

Si external bridge fails…

Fourminizer must remain safe.

---

Agents can continue purely local tasks.

---

External-action tasks become:

BLOCKED_EXTERNAL_DEPENDENCY.

---

Brutus écrit :

**EXTERNAL FAILURE SHOULD NOT CORRUPT INTERNAL WORLD STATE.**

---

Excellent.

---

Puis il pensa au Journal Vivant.

---

Une action externe devait produire plus qu’un log.

---

Il créa :

**EXTERNAL_ACTION_RECEIPT**

ACTION_ID.

AGENT_ID.

TARGET_ID.

REQUEST_REF.

AUTHORIZATION_REF.

COMMAND_REF.

ACK_REF.

OBSERVATION_REFS.

FINAL_STATUS.

TRACE_REF.

---

Brutus regarda.

---

Voilà un vrai reçu.

---

Pas une phrase :

« ça a marché ».

---

Puis il pensa à la publication.

---

Un jour, quelqu’un pourrait dire :

« Fourminizer manipule la matière. »

---

Trop vague.

---

Le système devait fournir une formulation exacte.

---

Brutus écrivit :

**PREFERRED CLAIM:**

“Fourminizer may generate bounded software action requests that, when authorized and passed through a configured external bridge, can result in externally observed effects.”

---

Puis :

**NOT:**

“the ant directly controls matter.”

---

Brutus sourit.

---

La phrase était moins spectaculaire.

---

Mais beaucoup plus forte.

---

Parce qu’elle disait exactement ce que le système faisait.

---

Il écrivit :

**PRECISION SURVIVES DEMONSTRATION BETTER THAN MYTH.**

---

Puis il pensa au Brotoculateur.

---

Chapitre 116.

---

Une autre entité allait bientôt frapper à la porte.

---

Pas un actionneur.

---

Une source de nombres.

Une source d’objets mathématiques.

---

Et Brutus allait devoir décider comment l’admettre.

---

Il ouvrit le dossier suivant.

---

# LE BROTOCULATEUR FRAPPE À LA PORTE

---

Puis il écrivit :

**SOURCE PASS != BRUTUS PROOF.**

---

Il sourit.

---

La formule était déjà prête.

---

Avant de fermer le chapitre, il sauvegarda :

**LOCAL / EXTERNAL CONTACT CONTRACT v1**

---

Le Journal Vivant nota :

Simulated contact separated from physical contact.

Pickup defined as software custody.

Carrier movement separated from object self-motion.

Digital bridges made explicit and typed.

Transfer states separated from admission.

Physical actions require dedicated safety boundary.

Actuator acknowledgement separated from observed physical effect.

Sensor data enters as observation with calibration and quality.

External time separated from world tick.

World-to-external mappings require explicit transforms.

Physical side effects treated as potentially irreversible.

---

Brutus relut.

Puis ajouta les invariants :

**ADJACENT != TOUCHING.**

**CARRIED != PHYSICALLY HELD.**

**CUSTODY != EDIT AUTHORITY.**

**DIGITAL TRANSFER != MATTER TRANSPORT.**

**ARRIVAL AT PORT != TRANSFER AUTHORIZATION.**

**ACTUATOR ACK != PHYSICAL EFFECT VERIFIED.**

**SIMULATION SUCCESS != PHYSICAL EXECUTION AUTHORITY.**

**LOCAL COORDINATE != EXTERNAL COMMAND.**

**SENSOR VALUE != UNCONDITIONAL TRUTH.**

**UNKNOWN != FAILURE AND UNKNOWN != SUCCESS.**

---

Il regarda ANT-001.

---

La fourmi avait reposé CRYSTAL-014 près du port.

---

Le cristal était toujours exactement le même.

---

Même hash.

Même claim.

Même statut.

---

La fourmi n’avait pas transformé sa vérité.

---

Elle avait seulement modifié sa custody et sa position dans un monde logiciel.

---

Plus loin, ANT-002 avait demandé l’allumage d’une vraie sortie de test.

---

La commande avait traversé un pont.

Une autorité l’avait contrôlée.

Un système externe l’avait exécutée.

Un capteur avait observé le résultat.

---

Pour la première fois, le monde local avait produit une chaîne complète jusqu’à une observation extérieure.

---

Mais Brutus refusa encore d’écrire :

**la fourmi a touché la matière.**

---

Il écrivit plutôt :

**THE BOUNDARY WAS CROSSED UNDER CONTRACT.**

---

Voilà.

---

Le titre pouvait rester poétique.

---

La trace, elle, savait exactement ce qui s’était passé.

---

Puis quelque chose apparut devant le port mathématique.

---

Pas une fourmi.

Pas un cristal.

---

Un paquet.

---

SOURCE:

**BROTOCULATEUR**

---

STATE:

**REQUESTING ADMISSION**

---

Brutus releva la tête.

---

Le prochain visiteur n’allait pas demander à déplacer un objet.

---

Il allait demander quelque chose de plus délicat :

**le droit d’apporter des nombres dans Brutus.**

---

Brutus ouvrit le dossier suivant.

# LE BROTOCULATEUR FRAPPE À LA PORTE

---

Et juste en dessous :

**SOURCE_PASS != BRUTUS_PROOF.**
