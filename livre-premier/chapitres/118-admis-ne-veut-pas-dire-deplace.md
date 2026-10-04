# Chapitre 118 — Admis ne veut pas dire déplacé

**ADMISSION != MOVEMENT.**

Puis :

**STATE TRANSITION AND LOCATION TRANSITION ARE DIFFERENT AXES.**

Brutus regarda CRYSTAL-0001.

---

Le cristal existait maintenant.

---

Il avait un identifiant.

Un manifeste.

Une provenance.

Un hash.

Un statut.

Une lignée.

---

Il avait même franchi la porte d’admission.

---

Dans le registre, on lisait :

**ADMISSION_STATE : ADMITTED**

---

Brutus resta quelques secondes devant cette ligne.

Puis posa une question extrêmement simple :

**Où est-il ?**

---

Le système ne répondit pas immédiatement.

---

Et cette hésitation était importante.

---

Parce que le registre savait que le cristal était admis.

---

Mais cela ne signifiait absolument pas qu’il avait changé de place.

---

Brutus écrivit :

**EXISTENCE != LOCATION.**

Puis :

**ADMISSION != ARRIVAL.**

---

Voilà.

---

Une nouvelle frontière venait d’apparaître.

---

Depuis des dizaines de chapitres, Brutus séparait les choses qui se ressemblaient trop.

---

Candidate et preuve.

Cristal et vérité.

Autorisation et exécution.

Renderer et autorité.

Message et commande.

---

Cette fois, il devait séparer :

**appartenance**

et

**position.**

---

Il ouvrit deux panneaux.

# AXE 1 — ADMISSION

et

# AXE 2 — LOCATION

---

Dans le premier :

**PENDING**

**ADMITTED**

**REJECTED**

**QUARANTINED**

**REVIEW_REQUIRED**

---

Dans le deuxième :

**AT_SOURCE**

**IN_TRANSIT**

**AT_BOUNDARY**

**AT_DESTINATION_UNVERIFIED**

**ARRIVED_VERIFIED**

**UNKNOWN**

---

Brutus regarda les deux colonnes.

---

Le cristal pouvait être :

**ADMITTED + AT_SOURCE**

---

Et il n’y avait rien d’anormal là-dedans.

---

Il pouvait aussi être :

**REJECTED + AT_DESTINATION_UNVERIFIED**

---

Étrange peut-être.

Mais parfaitement possible.

---

Un objet pouvait être arrivé quelque part…

et ne pas avoir le droit d’y entrer.

---

Brutus écrivit :

**ADMISSION STATUS DOES NOT ENCODE POSITION.**

---

Très important.

---

Il créa :

**ADMISSION_STATE**

avec :

**OBJECT_ID**

**TARGET_SYSTEM**

**POLICY_VERSION**

**DECISION**

**DECISION_TICK**

**DECISION_REF**

**SCOPE**

**TRACE_REF**

---

Puis :

**LOCATION_STATE**

avec :

**OBJECT_ID**

**LOCATION_ID**

**LOCATION_TYPE**

**POSITION_IF_APPLICABLE**

**CUSTODY_REF**

**OBSERVED_AT**

**STATE_VERSION**

**TRACE_REF**

---

Deux objets d’état.

---

Deux responsabilités.

---

Brutus sourit.

---

Enfin, le mot **admis** pouvait retrouver sa vraie signification.

---

Il écrivit :

**ADMISSION GRANTS LOGICAL MEMBERSHIP.**

Puis :

**IT DOES NOT PERFORM TRANSPORT.**

---

Très important.

---

Un cristal pouvait être admis dans le registre de recherche de Brutus…

sans être encore placé dans le monde local.

---

Une formule pouvait être admise dans le bus mathématique…

sans avoir encore été envoyée à un worker.

---

Un objet pouvait être reconnu comme membre d’un système…

tout en restant stocké ailleurs.

---

Brutus écrivit :

**MEMBERSHIP != PLACEMENT.**

---

Puis il pensa au cas inverse.

---

Un paquet pouvait arriver sur le serveur.

---

Ses bytes pouvaient être présents.

---

Mais la policy pouvait le refuser.

---

L’objet était donc :

présent.

---

Mais pas :

admis.

---

Brutus écrivit :

**PRESENCE != MEMBERSHIP.**

---

Très important.

---

Il repensa à la porte de Verso.

---

Verso pouvait prendre une décision :

**ADMITTED**

---

Mais cette décision ne devait pas produire un déplacement visuel.

---

Pas de cristal qui glisse automatiquement de gauche à droite.

---

Pas de téléportation.

---

Brutus écrivit :

**VERSO MAY AUTHORIZE MEMBERSHIP. VERSO DOES NOT TELEPORT OBJECTS.**

---

Il sourit.

---

La phrase était un peu brutale.

---

Mais parfaite.

---

Puis il pensa à QueenCore.

---

QueenCore pouvait recevoir une demande :

**MOVE CRYSTAL-0001 TO SLOT-B7**

---

Elle pouvait répondre :

**AUTHORIZED**

---

Le cristal était-il maintenant en B7 ?

---

Non.

---

Brutus écrivit :

**MOVE AUTHORIZED != MOVE EXECUTED.**

Puis :

**MOVE EXECUTED != ARRIVAL VERIFIED.**

Puis :

**ARRIVAL VERIFIED != ADMISSION GRANTED.**

---

Voilà.

---

Quatre événements différents.

---

Il dessina deux lignes parallèles.

---

La première :

\[
\text{REVIEW}
\rightarrow
\text{ADMISSION DECISION}
\]

---

La deuxième :

\[
\text{MOVE REQUEST}
\rightarrow
\text{AUTHORIZATION}
\rightarrow
\text{EXECUTION}
\rightarrow
\text{ARRIVAL OBSERVATION}
\]

---

Brutus regarda le dessin.

---

Le problème devenait limpide.

---

Les deux chemins pouvaient avancer à des vitesses différentes.

---

L’un pouvait même terminer sans l’autre.

---

Il créa :

**OBJECT_COORDINATION_VIEW**

avec :

**ADMISSION_STATE**

**TRANSPORT_STATE**

**LOCATION_STATE**

**CUSTODY_STATE**

**PLACEMENT_STATE**

**EPISTEMIC_STATE**

---

Puis il écrivit :

**ONE OBJECT MAY HAVE MANY ORTHOGONAL STATES.**

---

Très important.

---

Un objet n’avait pas un seul état.

---

Il avait plusieurs dimensions.

---

Une formule pouvait être :

candidate.

admitted.

unplaced.

at source.

not in transit.

---

Tout cela en même temps.

---

Brutus écrivit :

**ONE BADGE CANNOT REPRESENT EVERY AXIS.**

---

Il pensa immédiatement à l’interface.

---

Un gros voyant vert :

**ADMITTED**

---

Cela pouvait être dangereux.

---

Parce qu’un humain pouvait croire :

arrivé.

installé.

actif.

validé.

---

Alors qu’il signifiait seulement :

admis sous une policy précise.

---

Brutus ajouta :

**LABELS MUST NAME THE AXIS THEY BELONG TO.**

---

Très important.

---

Pas simplement :

GREEN.

---

Mais :

**ADMISSION : ADMITTED**

---

Puis :

**LOCATION : AT_SOURCE**

---

Puis :

**PLACEMENT : UNPLACED**

---

Puis :

**TRANSPORT : NOT_REQUESTED**

---

Voilà.

---

Une interface plus longue.

---

Mais infiniment plus honnête.

---

Puis il pensa à l’animation.

---

Le bouton :

**ADMIT**

---

Quelqu’un clique.

---

L’objet passe dans la liste des objets admis.

---

Très bien.

---

Mais le renderer ne devait pas le déplacer dans l’aquarium.

---

Brutus écrivit :

**ADMISSION ANIMATION MUST NOT IMPLY MOVEMENT.**

---

Une petite bordure pouvait apparaître.

Un badge.

Une entrée dans le registre.

---

Mais aucune trajectoire.

---

Parce qu’aucun MOVE_EVENT n’existait.

---

Puis il pensa à l’inverse.

---

Un objet arrive réellement au port.

---

Mais la décision d’admission n’a pas encore été prise.

---

Que faire ?

---

Il créa une zone.

# INGRESS HOLD

---

Un espace d’attente.

---

Le paquet pouvait être là.

---

Physiquement ou numériquement présent.

---

Mais encore hors du domaine logique principal.

---

Brutus écrivit :

**HOLDING AREA IS LOCATION, NOT MEMBERSHIP.**

---

Excellent.

---

Cela permettait de recevoir avant de décider.

---

Et de décider sans prétendre avoir déplacé.

---

Puis il pensa au Brotoculateur.

---

Même principe.

---

Un paquet pouvait être dans :

**BRUTUS_INBOX**

---

Mais ne pas encore être :

**BRUTUS_RESEARCH_OBJECT**

---

Il écrivit :

**INBOX PRESENCE != RESEARCH ADMISSION.**

---

Encore.

---

Le chapitre 116 se raccordait directement.

---

Puis il pensa au monde local.

---

CRYSTAL-0001 pouvait appartenir au monde…

sans être placé sur la grille 2D.

---

Il créa :

**PLACEMENT_STATE**

**UNPLACED**

**PENDING_PLACEMENT**

**PLACED**

**REMOVED**

**UNKNOWN**

---

Puis il écrivit :

**ADMITTED + UNPLACED IS A VALID STATE.**

---

Très important.

---

Un objet pouvait exister dans le registre du monde sans être visible.

---

Le renderer, lui, devait seulement afficher les objets dont :

**PLACEMENT_STATE = PLACED**

---

Brutus écrivit :

**RENDER LOCATION FROM LOCATION STATE, NOT ADMISSION STATE.**

---

Voilà.

---

Une règle simple.

---

Et extrêmement importante.

---

Puis il pensa à la custody.

---

Qui détient l’objet ?

---

Encore un autre axe.

---

SOURCE.

BRIDGE.

DESTINATION_INGRESS.

WORLD_AGENT.

ARCHIVE.

---

Brutus créa :

**CUSTODY_TRANSFER_EVENT**

avec :

**FROM_CUSTODIAN**

**TO_CUSTODIAN**

**OBJECT_ID**

**AUTHORIZATION_REF**

**HANDOFF_REF**

**TICK**

**TRACE_REF**

---

Puis :

**CUSTODY_TRANSFER != LOCATION ARRIVAL.**

---

Très important.

---

Un bridge pouvait accepter la custody d’un paquet…

alors que celui-ci était encore en transit.

---

Le responsable changeait.

---

La position finale, non.

---

Brutus regarda les axes.

---

Admission.

Transport.

Location.

Custody.

Placement.

Epistemic status.

---

Cela pouvait sembler beaucoup.

---

Mais la complexité existait déjà dans le réel.

---

Brutus ne faisait que refuser de l’écraser dans un seul mot.

---

Il écrivit :

**CLARITY DOES NOT REQUIRE SIMPLIFYING AWAY REAL DIFFERENCES.**

---

Puis il construisit la machine d’état du transport.

**TRANSPORT_STATE**

**NOT_REQUESTED**

**REQUESTED**

**AUTHORIZED**

**PICKED_UP**

**IN_TRANSIT**

**AT_DESTINATION_BOUNDARY**

**TRANSFERRED_TO_DESTINATION_CUSTODY**

**ARRIVAL_UNVERIFIED**

**ARRIVAL_VERIFIED**

**FAILED**

**UNKNOWN**

---

À côté :

**ADMISSION_STATE**

**PENDING**

**ADMITTED**

**REJECTED**

**QUARANTINED**

**REVIEW_REQUIRED**

---

Brutus écrivit :

**DO NOT MERGE STATE MACHINES BECAUSE THEIR WORDS SOUND RELATED.**

---

Très important.

---

Il testa des combinaisons.

---

**ADMITTED + FAILED_TRANSPORT**

---

Valide.

---

L’objet a été accepté.

Mais le déplacement a échoué.

---

**REJECTED + ARRIVAL_VERIFIED**

---

Valide.

---

L’objet est arrivé.

Mais il a été refusé.

---

**PENDING + IN_TRANSIT**

---

Valide.

---

La décision n’est pas terminée.

Le transport est déjà en cours.

---

Brutus écrivit :

**UNUSUAL COMBINATION != INVALID COMBINATION.**

---

Puis il pensa aux vraies contradictions.

---

Un objet :

**PLACED**

sans LOCATION_ID.

---

Impossible.

---

Un objet :

**ARRIVAL_VERIFIED**

sans ARRIVAL_EVIDENCE_REF.

---

Inacceptable.

---

Un objet :

**ADMITTED**

sans ADMISSION_EVENT.

---

Inacceptable.

---

Il créa :

**CROSS_AXIS_INVARIANTS**

---

Parce que les axes étaient séparés…

mais pas totalement indépendants.

---

Brutus écrivit :

**ORTHOGONAL DOES NOT MEAN UNRELATED.**

---

Très important.

---

Puis il pensa au statut scientifique.

---

Admettre un cristal au centre du laboratoire pouvait donner une impression de prestige.

---

Comme si le placer plus près du moteur lui donnait plus de valeur.

---

Brutus refusa immédiatement.

---

Il écrivit :

**ADMISSION != EPISTEMIC PROMOTION.**

Puis :

**PLACEMENT != EPISTEMIC PROMOTION.**

Puis :

**MOVEMENT != EPISTEMIC PROMOTION.**

---

Et enfin :

**LOCATION PRESTIGE != EVIDENCE.**

---

Voilà.

---

Un candidat posé au centre de l’écran restait un candidat.

---

Un théorème prouvé rangé dans une archive restait un théorème prouvé.

---

La géographie n’avait aucun droit sur la vérité.

---

Puis il pensa au transport visuel.

---

ANT-001 prend le cristal.

---

PICKUP_EVENT.

---

Elle marche vers le port.

---

MOVE_EVENT.

---

Le bridge reçoit la custody.

---

CUSTODY_TRANSFER_EVENT.

---

Le paquet est envoyé.

---

SEND_EVENT.

---

Destination reçoit.

---

RECEIVE_EVENT.

---

Destination vérifie.

---

VERIFY_EVENT.

---

Destination place.

---

PLACEMENT_EVENT.

---

Brutus écrivit :

**NO VISUAL STEP WITHOUT EVENT CLASS.**

---

Très important.

---

Chaque animation devait raconter un événement réellement enregistré.

---

Pas remplir les trous.

---

Puis il lança le test principal.

---

CRYSTAL-0001.

---

État initial :

**ADMISSION : ADMITTED**

**LOCATION : SOURCE_STORAGE**

**CUSTODY : SOURCE**

**TRANSPORT : NOT_REQUESTED**

**PLACEMENT : UNPLACED**

---

Brutus demanda :

**MOVE TO WORLD SLOT C4**

---

Un MOVE_REQUEST fut créé.

---

QueenCore vérifia.

---

Verso vérifia.

---

Autorisation accordée.

---

Transport :

**AUTHORIZED**

---

Location :

toujours SOURCE_STORAGE.

---

Très important.

---

L’autorisation n’avait encore rien déplacé.

---

Puis :

**PICKUP_EVENT**

---

Custody :

BRIDGE.

---

Location :

IN_TRANSIT.

---

Transport :

PICKED_UP.

---

Ensuite :

SEND_EVENT.

---

Transport :

IN_TRANSIT.

---

Puis la destination signala :

RECEIVED.

---

Brutus regarda.

---

Pas encore ARRIVED_VERIFIED.

---

Il écrivit :

**RECEIVED != ARRIVAL VERIFIED.**

---

Le paquet pouvait être arrivé au service…

mais pas encore à l’emplacement final.

---

Puis le hash fut vérifié.

---

Package valid.

---

Toujours :

PLACEMENT = UNPLACED.

---

Puis arriva :

**PLACEMENT_REQUEST**

---

Target :

WORLD:C4.

---

Le monde local vérifia :

zone.

occupancy.

generation.

object version.

---

Tout passa.

---

**PLACEMENT_EVENT**

---

Location :

WORLD:C4.

---

Placement :

PLACED.

---

Puis seulement :

ARRIVAL_EVIDENCE_REF created.

---

Transport :

**ARRIVAL_VERIFIED**

---

Brutus sourit.

---

Cette fois, le cristal avait réellement changé de place selon le contrat du système.

---

Pas parce qu’une permission existait.

---

Pas parce qu’un badge était vert.

---

Parce qu’une histoire complète existait.

---

Il écrivit :

**MOVEMENT IS A HISTORY, NOT A BADGE.**

---

Puis il pensa au cas difficile.

---

Crystal admitted.

Move authorized.

Pickup done.

---

Puis :

network failure.

---

Plus de nouvelles.

---

Que faire ?

---

Surtout pas :

DELIVERED.

---

Location :

UNKNOWN.

---

Transport :

UNKNOWN.

---

Custody :

BRIDGE.

---

Admission :

toujours ADMITTED.

---

Brutus écrivit :

**TRANSPORT FAILURE MUST NOT REVOKE ADMISSION BY ACCIDENT.**

---

Très important.

---

Un problème de transport n’était pas une révision scientifique.

---

Puis il pensa au cas inverse.

---

Admission révoquée.

---

Mais l’objet est déjà présent à destination.

---

Que faire ?

---

Pas le faire disparaître.

---

Brutus écrivit :

**REVOKED MEMBERSHIP != AUTOMATIC REMOVAL.**

---

Il fallait une nouvelle action :

**REMOVAL_REQUEST**

---

Avec :

**OBJECT_ID**

**CURRENT_LOCATION**

**REASON**

**AUTHORIZATION_REF**

**DESTINATION**

**TRACE_REF**

---

Puis :

**REMOVAL != DELETION.**

---

Très important.

---

Un objet pouvait être retiré du monde actif…

tout en restant dans l’historique.

---

Il écrivit :

**REMOVE FROM ACTIVE WORLD != ERASE HISTORY.**

---

Puis il pensa aux tombes.

---

Archive.

Quarantine.

Tomb.

---

Ces lieux pouvaient recevoir des objets.

---

Mais encore :

être dans une tombe ne signifiait pas être faux.

---

Brutus écrivit :

**ARCHIVE LOCATION != REFUTED STATUS.**

Puis :

**QUARANTINE LOCATION != FALSE CLAIM.**

---

Excellent.

---

La quarantine pouvait simplement signifier :

provenance incertaine.

policy mismatch.

integrity issue.

review pending.

---

Pas nécessairement :

false.

---

Puis il pensa aux versions.

---

CRYSTAL-0001 v1 admis.

---

CRYSTAL-0001 v2 apparaît.

---

L’admission de v1 s’applique-t-elle automatiquement ?

---

Non.

---

Brutus écrivit :

**ADMISSION IS VERSION-SCOPED UNLESS POLICY EXPLICITLY SAYS OTHERWISE.**

---

Très important.

---

Une nouvelle version pouvait changer :

la claim.

le statut.

les limitations.

la provenance.

---

Elle devait avoir sa propre décision.

---

Puis il pensa aux copies.

---

Un objet numérique pouvait avoir plusieurs copies.

---

COPY-A au source.

COPY-B dans le cache destination.

COPY-C dans une archive.

---

Mais toutes pouvaient référencer :

CRYSTAL-0001.

---

Brutus créa :

**COPY_ID**

---

Puis écrivit :

**LOGICAL OBJECT != DIGITAL COPY.**

---

Très important.

---

Déplacer COPY-B ne déplaçait pas nécessairement COPY-A.

---

Il fallait donc déclarer ce que signifiait réellement :

MOVE.

---

Il créa :

**TRANSFER_SEMANTICS**

**COPY**

**MOVE_LOGICAL_CUSTODY**

**REPLICATE**

**MIRROR**

**ARCHIVE**

---

Puis :

**MOVE MUST DECLARE ITS SEMANTICS.**

---

Excellent.

---

Un transfert numérique pouvait en réalité être :

copier les bytes.

vérifier.

transférer la custody logique.

conserver ou supprimer la copie source selon policy.

---

Brutus écrivit :

**DIGITAL MOVE MAY BE COPY + CUSTODY TRANSITION.**

---

Puis :

**NEVER ASSUME BYTE EXCLUSIVITY.**

---

Très important.

---

Contrairement à une pierre physique…

un fichier pouvait exister à plusieurs endroits simultanément.

---

Le mot **déplacer** devait donc être défini.

---

Puis il pensa à Fourminizer.

---

Quand ANT-001 « portait » CRYSTAL-014…

elle ne transportait pas forcément un fichier réseau.

---

Elle portait une relation de custody dans le monde local.

---

Brutus écrivit :

**WORLD CARRY != NETWORK COPY.**

---

Encore une frontière.

---

Puis il pensa au Brotoculateur.

---

Quand Brutus avait importé une formule…

la source ne l’avait pas perdue.

---

Il écrivit :

**IMPORT DOES NOT CONSUME SOURCE OBJECT.**

---

Très important.

---

L’import était :

copy/reference semantics.

---

Pas retrait.

---

Puis il retourna à Astra Station.

---

Il ajouta un panneau :

# COORDINATION

---

**ADMITTED / UNPLACED : 3**

**IN_TRANSIT / PENDING_ADMISSION : 1**

**ARRIVED / REJECTED : 1**

**UNKNOWN_LOCATION : 0**

---

Brutus sourit.

---

Enfin.

---

Les états inhabituels devenaient visibles.

---

Pas cachés.

---

Il écrivit :

**CROSS-AXIS EXCEPTIONS DESERVE VISIBILITY.**

---

Très important.

---

Puis il pensa au temps.

---

Une autorisation de move pouvait vieillir.

---

Si elle restait inutilisée trop longtemps…

elle devait expirer.

---

Il créa :

**MOVEMENT_EXECUTION_STATE**

**NOT_REQUESTED**

**REQUESTED**

**AUTHORIZED**

**STARTED**

**COMPLETED**

**FAILED**

**UNKNOWN**

---

Puis :

**AUTHORIZATION_EXPIRES_AT**

---

Brutus écrivit :

**AUTHORIZED ONCE != AUTHORIZED FOREVER.**

---

Encore.

---

Le chapitre 119 se rapprochait.

---

Une permission allait bientôt devenir si petite qu’elle ne pourrait autoriser qu’un seul pas.

---

Mais Brutus n’y était pas encore.

---

Il voulait d’abord résoudre la concurrence.

---

Supposons :

CRYSTAL-0001 est à A.

---

Une demande autorise :

A → B.

---

Mais avant l’exécution…

un autre événement déplace l’objet à C.

---

La vieille autorisation peut-elle encore servir ?

---

Non.

---

Brutus écrivit :

**MOVE AUTHORIZATION MUST BIND EXPECTED SOURCE STATE.**

---

Il ajouta :

**EXPECTED_LOCATION_VERSION**

---

Puis :

**STALE LOCATION INVALIDATES MOVE INTENT.**

---

Très important.

---

Une autorisation n’était valable que pour l’état contre lequel elle avait été évaluée.

---

Puis il pensa à la destination.

---

B était libre au moment de l’autorisation.

---

Mais au moment de l’exécution…

ANT-004 y avait posé un autre cristal.

---

Le move devait être revalidé.

---

Il créa :

**DESTINATION_EXPECTATION**

**LOCATION_ID**

**EXPECTED_OCCUPANCY_STATE**

**STATE_VERSION**

---

Puis :

**AUTHORIZED DESTINATION != GUARANTEED AVAILABLE DESTINATION.**

---

Excellent.

---

Le monde changeait.

---

Les permissions devaient reconnaître cette réalité.

---

Puis il pensa à l’échec après pickup.

---

Le bridge détient l’objet.

---

La destination devient indisponible.

---

Que faire ?

---

Pas improviser.

---

Il créa :

**MOVE_FAILURE_POLICY**

**RETURN_TO_SOURCE**

**HOLD_AT_BOUNDARY**

**QUARANTINE**

**MANUAL_RECONCILIATION**

---

Puis :

**FAILURE POLICY MUST BE KNOWN BEFORE MOVEMENT STARTS.**

---

Très important.

---

Le système devait savoir où déposer un objet avant de le prendre.

---

Puis il pensa au pire cas.

---

Source affirme :

sent.

---

Destination affirme :

not received.

---

Bridge affirme :

completed.

---

Qui a raison ?

---

Brutus refusa de choisir sans preuve.

---

Il créa :

**LOCATION_RECONCILIATION**

---

LAST_CONFIRMED_LOCATION.

CURRENT_CUSTODY.

OUTSTANDING_TRANSFER_ID.

SOURCE_REPORT_REF.

DESTINATION_REPORT_REF.

BRIDGE_REPORT_REF.

TRACE_REF.

---

Puis :

**LOCATION_STATE : CONTESTED**

---

Brutus écrivit :

**NO SINGLE SIDE MAY DECLARE LOCATION IF TRANSFER IS CONTESTED.**

---

Très important.

---

Unknown était acceptable.

---

Contested aussi.

---

La machine n’avait pas besoin d’inventer une certitude pour rester fonctionnelle.

---

Il écrivit :

**UNCERTAINTY SHOULD BE REPRESENTED, NOT SMOOTHED OVER.**

---

Puis il lança une dernière batterie de tests.

---

CRYSTAL-0002.

---

Admission :

ADMITTED.

---

Movement :

NOT_REQUESTED.

---

Location :

AT_SOURCE.

---

Placement :

UNPLACED.

---

UI affiche exactement cela.

---

PASS.

---

CRYSTAL-0003.

---

Transport :

ARRIVAL_VERIFIED.

---

Admission :

REJECTED.

---

Location :

INGRESS_HOLD.

---

UI affiche :

ARRIVED / REJECTED.

---

Pas :

ADMITTED.

---

PASS.

---

CRYSTAL-0004.

---

Move :

AUTHORIZED.

---

Token :

EXPIRED.

---

Execution :

NOT_STARTED.

---

Location :

UNCHANGED.

---

PASS.

---

CRYSTAL-0005.

---

Move started.

---

Destination unavailable.

---

Failure policy :

HOLD_AT_BOUNDARY.

---

Location :

BOUNDARY_HOLD.

---

Admission :

unchanged.

---

PASS.

---

CRYSTAL-0006.

---

Source says sent.

Destination says absent.

Bridge status inconsistent.

---

Location :

CONTESTED.

---

No fabricated arrival.

---

PASS.

---

Brutus regarda le tableau.

---

Tout se suivait.

---

Pas parce que les objets avaient des vies simples.

---

Mais parce que chaque changement avait maintenant son axe.

---

Il écrivit :

**A SYSTEM BECOMES CLEAR WHEN EACH EVENT IS ALLOWED TO CHANGE ONLY WHAT IT ACTUALLY CHANGED.**

---

Il resta devant cette phrase.

---

Voilà le cœur du chapitre.

---

Une admission devait changer l’admission.

---

Une autorisation devait changer la possibilité d’agir.

---

Un move devait changer la position.

---

Une observation devait confirmer l’arrivée.

---

Une promotion devait changer le statut épistémique.

---

Aucun événement ne devait voler le travail d’un autre.

---

Puis il regarda CRYSTAL-0001.

---

Admis.

---

Toujours au source.

---

Et tout allait bien.

---

Brutus sourit.

---

Il écrivit :

**AN OBJECT MAY BELONG WITHOUT MOVING.**

Puis :

**IT MAY MOVE WITHOUT BELONGING.**

Puis :

**IT MAY ARRIVE WITHOUT BEING ADMITTED.**

---

Voilà.

---

Puis il ouvrit le prochain dossier.

# UNE PERMISSION POUR UN SEUL PAS

---

Cette fois, il allait prendre la notion d’autorisation…

et la réduire.

---

Pas :

« cette fourmi peut déplacer les cristaux ».

---

Pas :

« cet opérateur a accès au monde ».

---

Mais :

cet acteur précis…

sur cet objet précis…

depuis cet état précis…

vers cette destination précise…

une seule fois…

avant telle expiration.

---

Brutus écrivit :

**AUTHORIZATION SHOULD BE AS SMALL AS THE ACTION IT ENABLES.**

---

Puis il sauvegarda :

**ADMISSION / MOVEMENT SEPARATION CONTRACT v1**

---

Le Journal Vivant nota :

Admission and movement separated into independent axes.

Membership separated from placement.

Presence separated from admission.

Transport separated from custody and arrival verification.

Digital copy identity separated from logical object identity.

Move semantics required to declare copy, replication or custody behavior.

UI forbidden from using admission as implied movement.

Source and destination state versions bound to movement decisions.

Unknown and contested locations preserved explicitly.

Failure policy declared before movement begins.

---

Brutus relut.

Puis ajouta les invariants :

**ADMISSION != MOVEMENT.**

**MEMBERSHIP != PLACEMENT.**

**PRESENCE != MEMBERSHIP.**

**AUTHORIZED != MOVED.**

**MOVED != ARRIVED.**

**ARRIVED != ADMITTED.**

**CUSTODY != LOCATION.**

**COPY != LOGICAL OBJECT.**

**DIGITAL MOVE MUST DECLARE SEMANTICS.**

**LOCATION PRESTIGE != EVIDENCE.**

---

Il ferma le chapitre.

---

Cette fois, aucun morceau du récit n’avait changé de langue.

---

Et surtout…

aucun événement n’avait changé plus de choses qu’il n’en avait réellement le droit.

---

Le cristal pouvait maintenant être admis sans être téléporté.

---

Ce qui restait à faire était encore plus précis :

lui donner le droit de faire **un seul pas**.
