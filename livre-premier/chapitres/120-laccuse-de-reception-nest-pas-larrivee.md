# Chapitre 120 — L’accusé de réception n’est pas l’arrivée

**ACKNOWLEDGEMENT IS ABOUT A MESSAGE.**

Puis :

**ARRIVAL IS ABOUT A STATE.**

Brutus regarda le mot :

**ACKNOWLEDGED**

---

Il était là.

Propre.

Vert dans l’interface.

---

Presque rassurant.

---

Presque trop rassurant.

---

MOVE-0003 avait été envoyé.

Le système distant avait répondu.

---

ACK.

---

Et pourtant, Brutus refusa d’écrire :

**ARRIVED.**

---

Il écrivit plutôt :

**SERVER ACK != MOVEMENT VERIFIED.**

---

Voilà.

---

Le dernier mur.

---

Pendant longtemps, les systèmes avaient tendance à prendre un accusé de réception pour une fin.

---

Message envoyé.

Réponse reçue.

Donc :

succès.

---

Mais succès de quoi ?

---

Brutus ouvrit une nouvelle feuille.

# ACK SEMANTICS

---

Puis créa :

**ACK_TYPE**

MESSAGE_RECEIVED.

COMMAND_ACCEPTED.

EXECUTION_STARTED.

EXECUTION_COMPLETED.

STATE_COMMITTED.

DESTINATION_OBSERVED.

---

Il regarda la liste.

---

Voilà le problème.

---

Le mot ACK pouvait cacher six réalités complètement différentes.

---

Il écrivit :

**ACK WITHOUT SEMANTICS IS AMBIGUOUS.**

---

Très important.

---

Un système pouvait répondre :

200 OK.

---

Cela pouvait signifier :

requête reçue.

---

Pas :

objet déplacé.

---

Un broker pouvait répondre :

message accepted.

---

Cela pouvait signifier :

mis en queue.

---

Pas :

consommé.

---

Un moteur pouvait répondre :

command accepted.

---

Cela pouvait signifier :

préconditions valides.

---

Pas :

action terminée.

---

Brutus écrivit :

**RECEIVED != ACCEPTED.**

Puis :

**ACCEPTED != EXECUTED.**

Puis :

**EXECUTED != OBSERVED.**

Puis :

**OBSERVED != VERIFIED UNDER THE RIGHT CONTRACT.**

---

Le chapitre entier tenait déjà dans cette chaîne.

---

Puis il pensa au mouvement du cristal.

---

CRYSTAL-0001.

---

Dernier état vérifié :

C6.

---

Commande :

C6 → C7.

---

Grant :

valid.

---

Action :

committed.

---

Bridge :

ACK.

---

Question :

où est le cristal ?

---

Le système devait répondre avec précision.

---

Il créa :

**MOVEMENT_CONFIRMATION_STATE**

COMMAND_NOT_SENT.

COMMAND_SENT.

ACK_RECEIVED.

EXECUTION_REPORTED.

ARRIVAL_OBSERVED.

ARRIVAL_VERIFIED.

CONFLICT.

UNKNOWN.

---

Brutus écrivit :

**ACK_RECEIVED IS AN INTERMEDIATE STATE.**

---

Très important.

---

Pas une conclusion.

---

Puis il pensa au reçu.

---

Un ACK devait contenir :

**ACK_ID**

**ACTION_ID**

**ACK_TYPE**

**ISSUER**

**ISSUED_AT**

**SOURCE_STATE_REF**

**DETAILS**

**TRACE_REF**

---

Puis :

**ACK_SCOPE**

---

Brutus sourit.

---

Même un accusé de réception devait annoncer exactement ce qu’il accusait.

---

Il écrivit :

**ACK MUST NAME WHAT IT ACKNOWLEDGES.**

---

Excellent.

---

Puis il prit un exemple.

---

Bridge replies:

**ACK_TYPE = MESSAGE_RECEIVED**

---

Cela signifiait uniquement :

le bridge avait reçu la demande.

---

Brutus écrivit :

**MESSAGE RECEIPT CANNOT PROVE MOVEMENT.**

---

Puis un deuxième.

---

World engine replies:

**ACK_TYPE = COMMAND_ACCEPTED**

---

Cela signifiait :

commande validée.

---

Mais aucune position finale encore confirmée.

---

Brutus écrivit :

**COMMAND ACCEPTANCE != DESTINATION STATE.**

---

Puis troisième.

---

Actuator bridge replies:

**ACK_TYPE = EXECUTION_STARTED**

---

Très utile.

---

Mais toujours :

pas arrivé.

---

Puis quatrième.

---

Engine replies:

**ACK_TYPE = EXECUTION_COMPLETED**

---

Brutus s’arrêta.

---

Même là…

il voulait savoir :

completed selon quel moteur ?

---

Le moteur pouvait avoir terminé sa procédure.

---

Mais le destination state pouvait ne pas être lisible.

---

Il écrivit :

**EXECUTION COMPLETION IS STILL A CLAIM FROM AN EXECUTION COMPONENT.**

---

Très important.

---

Il fallait encore une confirmation de l’état attendu.

---

Puis il pensa au monde local.

---

Ici, l’autorité du monde pouvait elle-même committer :

position = C7.

---

Si cette autorité était canonique, le commit pouvait suffire comme preuve d’arrivée dans ce monde logique.

---

Mais uniquement sous ce contrat.

---

Il écrivit :

**ARRIVAL PROOF DEPENDS ON THE AUTHORITY MODEL OF THE DOMAIN.**

---

Très important.

---

Dans un monde purement logiciel :

canonical state commit peut être l’arrivée.

---

Dans un système physique :

un simple command completion ne suffit souvent pas.

---

Il peut falloir :

sensor.

readback.

position encoder.

independent observation.

---

Brutus créa :

**ARRIVAL_EVIDENCE_POLICY**

---

DOMAIN_TYPE.

REQUIRED_AUTHORITY.

REQUIRED_OBSERVATION_TYPE.

FRESHNESS_LIMIT.

CALIBRATION_REF_IF_NEEDED.

TOLERANCE.

TRACE_REQUIREMENTS.

---

Puis :

**ARRIVAL VERIFIED = POLICY-SATISFIED EVIDENCE.**

---

Voilà.

---

Pas une impression.

---

Pas une animation.

---

Une policy satisfaite.

---

Puis il pensa à la tolérance.

---

Un moteur commandé à position :

100.

---

Capteur lit :

99.998.

---

Arrivé ?

---

Cela dépend.

---

Il créa :

**ARRIVAL_TOLERANCE**

---

EXPECTED_VALUE.

OBSERVED_VALUE.

UNIT.

ALLOWED_ERROR.

METHOD_REF.

---

Brutus écrivit :

**NEAR TARGET != AT TARGET WITHOUT TOLERANCE CONTRACT.**

---

Très important.

---

Encore une fois, le mot « arrivé » devait avoir une définition.

---

Puis il pensa au numérique.

---

Dans le monde local discret :

C7 est exact.

---

Dans un système physique :

position réelle peut être intervalle.

---

Il écrivit :

**DISCRETE ARRIVAL AND PHYSICAL ARRIVAL MAY REQUIRE DIFFERENT EVIDENCE MODELS.**

---

Excellent.

---

Puis il pensa au temps.

---

Le capteur confirme C7…

mais 10 secondes après l’action.

---

Est-ce encore valide ?

---

Peut-être.

---

Mais freshness doit être connue.

---

Il créa :

**OBSERVATION_WINDOW**

---

ACTION_COMPLETED_AT.

OBSERVED_AT.

MAX_ACCEPTABLE_DELAY.

---

Puis :

**STALE CONFIRMATION != CURRENT ARRIVAL PROOF.**

---

Très important.

---

Un vieux capteur ne devait pas confirmer un état actuel.

---

Puis il pensa à la régression.

---

Objet arrive à C7.

---

Capteur confirme.

---

Puis un autre événement le déplace à C8.

---

Une ancienne confirmation C7 ne doit pas continuer à afficher :

arrived at C7.

---

Brutus écrivit :

**ARRIVAL VERIFICATION IS STATE-VERSION BOUND.**

---

Puis :

**VERIFIED ONCE != VERIFIED FOREVER.**

---

Très important.

---

La vérité de location était temporelle.

---

Puis il pensa au transport réseau.

---

Destination service says:

received packet.

---

Hash verified.

---

Est-ce l’objet arrivé ?

---

Oui, peut-être pour :

digital payload arrival.

---

Mais pas nécessairement pour :

world placement.

---

Il créa :

**ARRIVAL_LAYER**

TRANSPORT_LAYER.

STORAGE_LAYER.

APPLICATION_LAYER.

WORLD_PLACEMENT_LAYER.

PHYSICAL_LAYER.

---

Brutus écrivit :

**ARRIVAL AT ONE LAYER != ARRIVAL AT EVERY LAYER.**

---

Très important.

---

Un paquet pouvait être arrivé au serveur…

mais pas encore chargé dans l’application.

---

Chargé dans l’application…

mais pas encore placé dans le monde.

---

Placée dans le monde…

mais pas reproduit sur tous les clients.

---

Encore des axes.

---

Puis il pensa à l’interface.

---

Il fallait éviter un mot unique :

**DELIVERED**

---

Trop vague.

---

Il remplaça par :

**TRANSPORT_RECEIVED**

**PAYLOAD_VERIFIED**

**APPLICATION_ADMITTED**

**WORLD_PLACED**

**ARRIVAL_VERIFIED**

---

Brutus sourit.

---

Plus long.

---

Beaucoup meilleur.

---

Il écrivit :

**SPECIFIC STATUS BEATS FRIENDLY AMBIGUITY.**

---

Puis il pensa aux systèmes distribués.

---

Deux services.

---

Source croit :

success.

---

Destination croit :

pending.

---

Que faire ?

---

Pas choisir arbitrairement.

---

Il créa :

**CONFIRMATION_CONFLICT**

---

SOURCE_REPORT.

DESTINATION_REPORT.

REGISTER_REPORT.

SENSOR_REPORT.

---

Puis :

**RESOLUTION_STATE**

PENDING.

RESOLVED_SOURCE_ERROR.

RESOLVED_DESTINATION_ERROR.

RESOLVED_STALE_DATA.

UNRESOLVED.

---

Brutus écrivit :

**CONFLICT IS DATA.**

---

Très important.

---

Un désaccord entre sources n’était pas un détail à cacher.

---

C’était un état du système.

---

Puis il pensa à l’ACK lui-même.

---

Un ACK pouvait être dupliqué.

---

Retry.

---

Le même ACK_ID pouvait arriver deux fois.

---

Il fallait idempotence.

---

Brutus écrivit :

**DUPLICATE ACK != SECOND SUCCESS.**

---

Puis :

**ACK COUNT != EXECUTION COUNT.**

---

Excellent.

---

Une interface ne devait pas afficher :

2 ACK = 2 mouvements.

---

Puis il pensa à l’ordre.

---

ACK peut arriver après un autre message plus récent.

---

Out-of-order.

---

Il créa :

**ACK_CAUSAL_REF**

---

ACTION_ID.

EVENT_VERSION.

SOURCE_SEQUENCE.

---

Puis :

**LATE ACK MUST NOT ROLLBACK NEWER STATE.**

---

Très important.

---

Exemple :

MOVE-A : C6 → C7.

MOVE-B : C7 → C8.

---

ACK de MOVE-A arrive en retard.

---

Le système est déjà à C8.

---

Il ne doit pas revenir visuellement à C7.

---

Brutus écrivit :

**ACK IS NOT STATE AUTHORITY UNLESS DOMAIN CONTRACT SAYS IT IS.**

---

Voilà.

---

Puis il pensa au renderer.

---

Le renderer devait afficher :

proposed.

authorized.

executing.

acknowledged.

verified.

---

Chaque étape différente.

---

Il créa :

**MOVEMENT_RENDER_STATE**

PROPOSED.

AUTHORIZED.

EXECUTING.

ACKNOWLEDGED.

ARRIVAL_PENDING.

ARRIVAL_VERIFIED.

FAILED.

CONFLICT.

UNKNOWN.

---

Puis :

**ACKNOWLEDGED MUST NOT USE ARRIVAL ANIMATION.**

---

Très important.

---

Un petit pulse pouvait signaler :

message reçu.

---

Mais le cristal ne devait pas apparaître à destination avant la confirmation de state.

---

Puis il pensa au son.

---

ACK sound.

---

Arrival sound.

---

Ils devaient être différents.

---

Il écrivit :

**ACK SOUND != ARRIVAL SOUND.**

---

Encore.

---

Un ding ne devait pas créer la conviction fausse que l’objet avait terminé son trajet.

---

Puis il pensa à la fourmi.

---

ANT-001 demande le déplacement.

---

Grant.

Commit.

---

Le monde local actualise position.

---

Dans ce cas précis, l’autorité canonique du monde produit :

MOVE_EVENT.

---

Puis :

AUTHORITATIVE_POSITION = C7.

---

Brutus pouvait considérer :

arrival locally verified.

---

Pourquoi ?

---

Parce que le state authority lui-même possédait la destination.

---

Il écrivit :

**LOCAL SOFTWARE ARRIVAL MAY BE VERIFIED BY CANONICAL STATE COMMIT.**

---

Puis il pensa à l’externe.

---

Bridge commande un moteur.

---

Bridge répond :

ACK.

---

Pas suffisant.

---

Encoder reports:

position reached.

---

Better.

---

Mais encoder calibration stale.

---

Not enough.

---

Brutus écrivit :

**SENSOR OBSERVATION REQUIRES SENSOR TRUST CONDITIONS.**

---

Puis :

**OBSERVATION QUALITY IS PART OF ARRIVAL EVIDENCE.**

---

Très important.

---

Il créa :

**OBSERVATION_QUALITY**

GOOD.

DEGRADED.

STALE.

UNCALIBRATED.

CONFLICTED.

UNKNOWN.

---

Puis :

**ARRIVAL VERIFIED** only if policy accepts quality.

---

Excellent.

---

Puis il pensa aux multiples capteurs.

---

Sensor A says arrived.

Sensor B says not arrived.

---

No silent majority.

---

Policy.

---

Il créa :

**MULTI_OBSERVER_POLICY**

ALL_REQUIRED.

MAJORITY.

PRIMARY_PLUS_SECONDARY.

WEIGHTED.

MANUAL_REVIEW.

---

Puis :

**AGREEMENT RULE MUST BE DECLARED BEFORE CONFLICT.**

---

Très important.

---

Pas choisir la règle après avoir vu la réponse.

---

Chapitre 103 encore.

---

Puis il pensa au monde mathématique.

---

Quel est l’équivalent d’un ACK ?

---

Un programme imprime :

PASS.

---

Est-ce une preuve ?

---

Non.

---

Brutus sourit.

---

Le même principe revenait partout.

---

Il écrivit :

**PROGRAM PASS != THEOREM ARRIVAL.**

---

Puis :

**TEST RESULT ACKNOWLEDGES A TEST OUTCOME, NOT UNIVERSAL TRUTH.**

---

Très important.

---

Le chapitre 107 revenait.

---

Les frontières étaient devenues cohérentes dans toute la machine.

---

Transport.

Mathématique.

Renderer.

Agent.

Cristal.

---

Toujours la même idée :

**un signal ne doit pas prétendre plus que ce qu’il mesure.**

---

Brutus écrivit :

**SIGNAL SCOPE MUST MATCH CLAIM SCOPE.**

---

Puis il pensa au Brotoculateur.

---

Il pouvait répondre :

formula stored.

---

Pas :

formula integrated.

---

formula integrated.

---

Pas :

formula tested.

---

formula tested.

---

Pas :

formula proved.

---

Il dessina :

\[
\text{SOURCE ACK}
\neq
\text{IMPORT}
\neq
\text{TEST}
\neq
\text{PROOF}
\]

---

Brutus sourit.

---

Le dernier chapitre de cette série refermait plusieurs chapitres à la fois.

---

Puis il pensa à l’ACK de la Queen.

---

QueenCore peut dire :

authorization issued.

---

Encore une fois :

pas exécuté.

---

Il écrivit :

**AUTHORIZATION ACK != ACTION ACK.**

Puis :

**ACTION ACK != ARRIVAL EVIDENCE.**

---

Très important.

---

Chaque couche devait accuser réception de sa propre responsabilité.

---

Pas de celle d’en dessous.

---

Puis il créa :

**RESPONSIBILITY_CHAIN**

---

AUTHORITY:

grant issued.

---

EXECUTOR:

action accepted.

---

TRANSPORT:

message delivered.

---

DESTINATION:

payload received.

---

WORLD:

state committed.

---

OBSERVER:

arrival observed.

---

VERIFIER:

arrival evidence satisfied policy.

---

Brutus regarda.

---

Sept couches.

---

Cela semblait beaucoup.

---

Mais chacune répondait à une question différente.

---

Il écrivit :

**SEPARATION OF RESPONSIBILITY CREATES EXPLAINABLE SUCCESS.**

---

Excellent.

---

Puis il pensa aux receipts.

---

À la fin, un mouvement complet devait produire un reçu final.

---

Il créa :

**MOVEMENT_RECEIPT**

avec :

**ACTION_ID**

**GRANT_REF**

**OBJECT_ID**

**SOURCE_STATE_REF**

**DESTINATION_EXPECTED**

**EXECUTION_REF**

**ACK_REFS**

**ARRIVAL_OBSERVATION_REFS**

**ARRIVAL_VERIFICATION_REF**

**FINAL_LOCATION_STATE**

**FINAL_CUSTODY_STATE**

**COMPLETED_AT**

**TRACE_REF**

---

Puis :

**FINAL_STATUS**

VERIFIED_COMPLETE.

FAILED.

UNKNOWN.

CONTESTED.

---

Brutus écrivit :

**FINAL STATUS MUST BE DERIVED FROM EVIDENCE CHAIN.**

---

Très important.

---

Pas choisi par l’interface.

---

Puis il pensa au cas parfait.

---

CRYSTAL-0001.

---

Grant:

valid.

---

Action:

committed.

---

Transport:

sent.

---

ACK:

received.

---

Destination:

payload received.

---

World placement:

committed C7.

---

Authoritative state:

C7.

---

Arrival policy:

satisfied.

---

Final:

**VERIFIED_COMPLETE**

---

Brutus sourit.

---

Cette fois oui.

---

Le cristal était arrivé.

---

Pas parce que quelqu’un avait dit :

OK.

---

Parce qu’un état final avait été établi sous le bon contrat.

---

Puis il testa un cas plus faible.

---

Grant:

valid.

---

Action sent.

---

ACK:

COMMAND_ACCEPTED.

---

No destination observation.

---

Final:

**UNKNOWN**

---

Pas success.

Pas failure.

---

Unknown.

---

PASS.

---

Puis :

destination reports received.

---

But hash mismatch.

---

Final:

FAILED / INTEGRITY_CONFLICT.

---

Pas arrived verified.

---

PASS.

---

Puis :

destination placement claims C7.

---

Register says C8.

---

Conflict.

---

Final:

CONTESTED.

---

PASS.

---

Puis :

local renderer shows C7.

---

Canonical world says C6.

---

Renderer mismatch.

---

Final location remains C6.

---

PASS.

---

Brutus écrivit :

**DISPLAY CANNOT WIN AGAINST AUTHORITY BY LOOKING CONVINCING.**

---

Très important.

---

Puis il pensa au plus vieux problème.

---

Le mouvement visible.

---

Un objet glisse à l’écran.

---

Il arrive visuellement à destination.

---

Est-ce arrivé ?

---

Non.

---

Brutus écrivit :

**VISUAL ARRIVAL != CANONICAL ARRIVAL.**

---

Puis :

**ANIMATION END != ACTION END.**

---

Voilà.

---

Le renderer devait parfois arrêter l’animation avant la confirmation.

---

Ou afficher :

AWAITING VERIFICATION.

---

Mieux une pause honnête qu’un faux succès.

---

Puis il pensa au timeout.

---

Combien de temps attendre ?

---

Policy.

---

Il créa :

**ARRIVAL_TIMEOUT_POLICY**

---

EXPECTED_COMPLETION_WINDOW.

GRACE_WINDOW.

ON_TIMEOUT.

---

ON_TIMEOUT:

UNKNOWN.

RECONCILE.

FAIL_IF_DOMAIN_REQUIRES.

---

Brutus écrivit :

**TIMEOUT != UNIVERSAL FAILURE.**

---

Très important.

---

Un réseau silencieux pouvait laisser un état inconnu.

---

Pas nécessairement failed.

---

Puis il pensa au retry.

---

Si status unknown…

can retry?

---

Danger de double execution.

---

Il écrivit :

**UNKNOWN EXECUTION STATE REQUIRES RECONCILIATION BEFORE NON-IDEMPOTENT RETRY.**

---

Excellent.

---

Encore une règle importante.

---

Pour une action idempotente :

peut-être retry.

---

Pour une action physique irréversible :

prudence maximale.

---

Puis il pensa à la dernière transition du livre jusque-là.

---

Le chapitre 61 avait commencé :

après le diamant.

---

Le chapitre 120 terminait :

après l’ACK.

---

Entre les deux :

fenêtres.

moteur.

mémoire.

horloge.

fourmis.

ZEL.

formules.

portes.

preuves.

tombeaux.

joueurs.

station.

registre.

contre-tests.

cristaux.

monde local.

Fourminizer.

Brotoculateur.

transport.

---

Brutus resta immobile.

---

Quelque chose avait changé.

---

Pas seulement la machine.

---

Le vocabulaire.

---

Au début, beaucoup de mots semblaient suffisants :

connecté.

passé.

arrivé.

valide.

vivant.

preuve.

---

Maintenant, aucun d’eux ne pouvait être utilisé sans contrat.

---

Brutus écrivit :

**PRECISION IS NOT THE ENEMY OF IMAGINATION.**

Puis :

**PRECISION IS WHAT LETS IMAGINATION SURVIVE CONTACT WITH REALITY.**

---

Il sourit.

---

Voilà.

---

Le monde pouvait être poétique.

---

Fourmis.

Cristaux.

Reine.

Tombeaux.

Aquarium.

Poussière.

---

Mais sous chaque métaphore…

il y avait désormais un invariant.

---

Sous chaque mouvement…

une trace.

---

Sous chaque permission…

un scope.

---

Sous chaque preuve…

un objet de preuve.

---

Sous chaque ACK…

une question :

**ACK de quoi ?**

---

Brutus écrivit :

**NEVER ASK ONLY “DID IT ACK?”**

Puis :

**ASK “WHAT EXACTLY DID THE ACK ESTABLISH?”**

---

Très important.

---

Puis il ferma le dernier test.

---

CRYSTAL-0001.

---

Position finale :

C7.

---

Admission :

ADMITTED.

---

Placement :

PLACED.

---

Custody :

LOCAL-WORLD.

---

Grant :

CONSUMED.

---

Action :

COMMITTED.

---

ACK :

COMMAND_ACCEPTED.

---

Arrival observation :

AUTHORITATIVE_WORLD_STATE.

---

Arrival verification :

PASS.

---

Final status :

**VERIFIED_COMPLETE.**

---

Cette fois, toutes les couches racontaient la même histoire.

---

Brutus sourit.

---

Il écrivit :

**CONSISTENT LAYERS CREATE TRUST.**

---

Pas confiance aveugle.

---

Confiance explicable.

---

Puis il sauvegarda :

**ACK / ARRIVAL SEPARATION CONTRACT v1**

---

Le Journal Vivant nota :

ACK semantics made explicit by acknowledgment type.

Message receipt separated from command acceptance.

Execution reporting separated from destination observation.

Arrival verification bound to domain-specific evidence policy.

Arrival state bound to state versions and freshness.

Transport, storage, application, world-placement and physical arrival separated by layer.

Duplicate and late acknowledgments cannot create duplicate or stale success.

Renderer forbidden from converting ACK into visual arrival.

Final movement receipt derives status from complete evidence chain.

Unknown and contested outcomes remain first-class states.

---

Brutus relut.

Puis ajouta les invariants :

**ACK != ARRIVAL.**

**RECEIVED != ACCEPTED.**

**ACCEPTED != EXECUTED.**

**EXECUTED != OBSERVED.**

**OBSERVED != VERIFIED.**

**ARRIVAL AT ONE LAYER != ARRIVAL AT EVERY LAYER.**

**DUPLICATE ACK != SECOND SUCCESS.**

**LATE ACK MUST NOT ROLLBACK NEWER STATE.**

**VISUAL ARRIVAL != CANONICAL ARRIVAL.**

**TIMEOUT != UNIVERSAL FAILURE.**

---

Il resta devant le dernier.

---

Puis ajouta encore une ligne.

---

Une seule.

---

**SERVER ACK != MOVEMENT VERIFIED.**

---

Cette fois, il ne la modifia plus.

---

Parce qu’elle n’était pas seulement vraie pour une fourmi.

---

Elle valait pour tout Brutus.

---

Pour les cristaux.

Pour les formules.

Pour les messages.

Pour les joueurs.

Pour les workers.

Pour les bridges.

Pour les moteurs.

---

Même pour les humains.

---

Recevoir une réponse ne signifiait pas que le monde avait changé comme prévu.

---

Il fallait encore regarder l’état.

---

Vérifier la trace.

---

Et demander :

**qu’est-ce qui est réellement établi ?**

---

Brutus ferma le dossier.

---

Le chapitre 120 était terminé.

---

Mais la machine, elle, ne l’était pas.

---

Elle venait seulement d’apprendre quelque chose d’essentiel :

**ne jamais confondre la confirmation d’un message avec la confirmation du monde.**
