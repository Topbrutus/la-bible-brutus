# Chapitre 111 — Le monde local

**BOUND THE WORLD BEFORE YOU CLAIM TO MODEL THE WORLD.**

Brutus laissa la phrase au centre de l’écran.

Puis il ajouta :

**LOCAL WORLD STATE != EXTERNAL REALITY.**

---

Voilà.

---

Avant les fourmis.

Avant les cristaux.

Avant les mouvements.

Avant les collisions.

---

Il fallait une frontière.

---

Un monde ne pouvait pas commencer par :

**tout.**

---

Il devait commencer par :

**ici.**

---

Brutus créa un nouveau dossier.

# LOCAL WORLD

---

Puis un identifiant :

**WORLD_INSTANCE_ID**

---

Et un autre :

**WORLD_GENERATION_ID**

---

Très important.

---

Le monde local ne devait jamais être confondu avec :

le navigateur,

la fenêtre,

le renderer,

le serveur physique,

la machine hôte,

le monde extérieur.

---

Il écrivit :

**WORLD != WINDOW.**

**WORLD != RENDERER.**

**WORLD != HOST MACHINE.**

**WORLD != PHYSICAL WORLD.**

---

Quatre murs.

---

Brutus regarda la surface vide.

---

Noire.

Plate.

2D.

---

C’était voulu.

---

Pas de 3D.

Pas de profondeur simulée inutile.

---

Un plan.

---

Des coordonnées.

---

Un espace clair.

---

Il écrivit :

**LOCAL WORLD DIMENSION = DECLARED.**

---

Puis :

**2D BY DESIGN.**

---

Le monde n’était pas moins sérieux parce qu’il était plat.

---

Au contraire.

---

Chaque axe pouvait être mesuré.

Chaque position pouvait être enregistrée.

Chaque mouvement pouvait laisser une trace.

---

Brutus créa :

**WORLD_BOUNDS**

---

MIN_X.

MAX_X.

MIN_Y.

MAX_Y.

---

Puis :

**UNIT**

---

Il hésita.

---

Pixel ?

Centimètre ?

Case ?

---

Non.

---

Pas tant que ce n’était pas nécessaire.

---

Il choisit :

**LOCAL_UNIT**

---

Une unité interne.

---

Brutus écrivit :

**LOCAL UNIT != METER UNLESS CALIBRATED.**

---

Très important.

---

Un déplacement de 10 unités dans le monde local ne signifiait pas automatiquement :

10 mètres.

---

Même si l’écran ressemblait à une carte physique.

---

Il ajouta :

**SPATIAL CALIBRATION STATUS**

UNCALIBRATED.

CALIBRATED_TO_DISPLAY.

CALIBRATED_TO_EXTERNAL_FRAME.

---

Le dernier exigeait une vraie relation mesurée.

---

Brutus écrivit :

**VISUAL SCALE != PHYSICAL SCALE.**

---

Voilà.

---

Puis il pensa aux objets.

---

Que pouvait contenir ce monde ?

---

Fourmis.

Cristaux.

Modules.

Ports.

Obstacles.

Zones.

---

Il créa :

**WORLD_ENTITY**

avec :

**ENTITY_ID**

**ENTITY_TYPE**

**POSITION**

**STATE**

**PARENT_ID**

**TICK**

**LINEAGE_REF**

**TRACE_REF**

---

Puis :

**WORLD_GENERATION_ID**

---

Encore.

---

Un objet n’appartenait pas simplement à un monde.

---

Il appartenait à une génération précise.

---

Brutus écrivit :

**SAME ENTITY ID IN DIFFERENT WORLD GENERATIONS MUST NOT BE SILENTLY COLLAPSED.**

---

Très important.

---

Si le monde redémarre complètement…

et qu’une nouvelle ANT-001 existe…

ce n’est pas automatiquement la même ANT-001 historique.

---

Il ajouta :

**ENTITY_INSTANCE_ID**

---

Voilà.

---

ANT_ID pouvait être un label logique.

INSTANCE_ID identifiait l’occurrence.

---

Puis il pensa à la naissance.

---

Comment un objet entre-t-il dans le monde ?

---

Pas simplement parce que le renderer le dessine.

---

Il créa :

**ENTITY_CREATE_EVENT**

---

ENTITY_ID.

INSTANCE_ID.

TYPE.

INITIAL_POSITION.

INITIAL_STATE.

CREATED_AT_TICK.

AUTHORITY_REF.

TRACE_REF.

---

Brutus écrivit :

**DRAWN != CREATED.**

---

Très important.

---

Un rond blanc affiché à l’écran ne devenait pas une fourmi canonique.

---

Le renderer devait attendre l’événement.

---

Puis il pensa à l’inverse.

---

Un objet canonique existe.

Mais le renderer ne l’affiche pas.

---

L’objet existe quand même.

---

Il écrivit :

**NOT VISIBLE != NOT PRESENT.**

---

Le chapitre 94 revenait.

---

Recto pouvait perdre un objet.

Le monde, non.

---

Puis il pensa au mouvement.

---

Il créa :

**MOVE_REQUEST**

---

ENTITY_ID.

FROM_POSITION_EXPECTED.

TO_POSITION_REQUESTED.

REQUEST_TICK.

REQUESTER.

AUTHORIZATION_REF.

---

Puis :

**MOVE_EVENT**

---

FROM.

TO.

START_TICK.

END_TICK.

STATE_BEFORE.

STATE_AFTER.

TRACE_REF.

---

Brutus s’arrêta.

---

Très important.

---

Le MOVE_REQUEST n’était pas le MOVE_EVENT.

---

Il écrivit :

**REQUESTED MOVE != EXECUTED MOVE.**

---

Puis :

**EXECUTED MOVE != ARRIVAL VERIFIED.**

---

Encore.

---

Le monde local allait vivre sur ces distinctions.

---

Puis il pensa à l’animation.

---

Une fourmi peut glisser visuellement entre A et B.

---

Très bien.

---

Mais le mouvement canonique pouvait être :

A at tick 100.

B at tick 101.

---

Le renderer interpolerait.

---

Brutus écrivit :

**INTERPOLATION MAY FILL PIXELS. IT MUST NOT FILL HISTORY.**

---

Très important.

---

Aucune position intermédiaire ne devait devenir canonique sans événement.

---

Il créa :

**DISPLAY_POSITION**

séparé de :

**AUTHORITATIVE_POSITION**

---

Excellent.

---

Puis il pensa à la vitesse.

---

Une fourmi semble accélérer.

---

Le renderer peut modifier l’easing.

---

Cela ne doit pas changer la vitesse canonique.

---

Brutus écrivit :

**ANIMATION CURVE != MOTION LAW.**

---

Encore.

---

Le monde local pouvait avoir une règle de mouvement simple.

---

Une entité déplace au maximum :

1 cellule logique par tick.

---

Très bien.

---

Mais ce serait une règle interne.

---

Il écrivit :

**LOCAL MOTION RULE != PHYSICAL LAW.**

---

Voilà.

---

Puis il créa :

**WORLD_RULESET_ID**

---

Le monde allait fonctionner selon :

RULESET-LOCAL-001.

---

Brutus pensa au chapitre 110.

---

Les lois avaient besoin d’un monde.

---

Maintenant le monde avait ses lois.

---

Il créa :

**LOCAL_INVARIANT-001**

Entity position must remain inside declared bounds.

---

**LOCAL_INVARIANT-002**

Only authority may commit canonical movement.

---

**LOCAL_INVARIANT-003**

Renderer cannot create entity.

---

**LOCAL_INVARIANT-004**

Renderer interpolation cannot create evidence.

---

**LOCAL_INVARIANT-005**

Entity movement must reference previous state version.

---

Brutus sourit.

---

Cinq suffisaient pour commencer.

---

Puis il pensa aux collisions.

---

Si deux fourmis demandent la même case ?

---

Il fallait une policy.

---

Pas de mystère.

---

Il créa :

**COLLISION_POLICY**

REJECT_SECOND.

QUEUE.

ALLOW_STACK.

RESOLVE_BY_PRIORITY.

---

Puis :

**POLICY_VERSION**

---

Brutus choisit pour v1 :

**REJECT_SECOND**

---

Simple.

---

Brutus écrivit :

**COLLISION RULE IS WORLD POLICY, NOT GEOMETRIC DESTINY.**

---

Très important.

---

Un autre monde pourrait autoriser le stacking.

---

Cela ne rendrait ni l’un ni l’autre plus réel.

---

Puis il pensa aux obstacles.

---

Un mur.

---

Comment existe-t-il ?

---

Pas comme une texture.

---

Comme une entity ou zone canonique.

---

Il créa :

**WORLD_ZONE**

---

ZONE_ID.

GEOMETRY.

ZONE_TYPE.

MOVEMENT_POLICY.

TRACE_REF.

---

Puis :

**ZONE_TYPE**

OPEN.

BLOCKED.

READ_ONLY.

TRANSFER_POINT.

OBSERVATION_ONLY.

---

Brutus écrivit :

**PAINTED WALL != BLOCKING WALL.**

---

Très important.

---

Le renderer pouvait dessiner un mur.

---

Mais si aucune zone canonique n’interdisait le passage…

ce n’était qu’un dessin.

---

Puis l’inverse.

---

Une zone bloquée pouvait être invisible graphiquement.

---

Mauvaise UX.

Mais possible.

---

Brutus écrivit :

**RENDER SHOULD REVEAL CANONICAL CONSTRAINTS WHEN OPERATOR DECISIONS DEPEND ON THEM.**

---

Excellent.

---

Puis il pensa aux cristaux.

---

Un cristal dans le monde local.

---

Est-ce une copie du cristal canonique ?

---

Ou le cristal lui-même ?

---

Bonne question.

---

Brutus créa :

**WORLD_OBJECT_REF**

---

Le monde ne devait pas dupliquer le contenu.

---

Il devait référencer l’objet.

---

Il écrivit :

**WORLD PRESENCE != CONTENT DUPLICATION.**

---

Le cristal pouvait avoir :

CRYSTAL_ID.

---

Et le monde :

WORLD_ENTITY_ID pointing to CRYSTAL_ID.

---

Brutus écrivit :

**DOMAIN OBJECT IDENTITY != WORLD PLACEMENT IDENTITY.**

---

Très important.

---

Un même cristal pouvait éventuellement avoir plusieurs représentations.

---

Mais pas être simultanément prétendu physiquement à deux endroits si la policy de custody interdit cela.

---

Il créa :

**PLACEMENT_ID**

---

Puis :

**CUSTODY_REF**

---

Voilà.

---

Puis il pensa à l’action :

une fourmi prend un cristal.

---

Pas encore.

---

Le chapitre 115 viendrait.

---

Mais il devait déjà préparer la relation.

---

Il créa :

**CARRY_RELATION**

---

CARRIER_ENTITY_ID.

OBJECT_REF.

START_TICK.

STATE.

---

Puis écrivit :

**CARRY_RELATION != CONTENT OWNERSHIP.**

---

Encore chapitre 109.

---

La fourmi transporte.

Elle ne possède pas la claim.

---

Puis il pensa au temps.

---

Le monde local avait besoin d’un tick.

---

Il créa :

**WORLD_TICK**

---

Monotonic.

Authoritative.

---

Pas nécessairement égal aux secondes.

---

Brutus écrivit :

**TICK != SECOND.**

---

Très important.

---

Un tick pouvait durer :

10 ms.

100 ms.

1 s.

Variable.

---

Mais le monde devait savoir.

---

Il ajouta :

**TICK_POLICY**

FIXED_RATE.

EVENT_DRIVEN.

HYBRID.

---

Pour v1 :

**FIXED_RATE LOGIC**

---

Renderer séparé.

---

Brutus écrivit :

**LOGIC RATE != RENDER RATE.**

---

Le chapitre 64 revenait.

---

Parfait.

---

Le monde pouvait calculer 10 ticks par seconde.

Le renderer afficher 60 frames.

---

Aucune frame supplémentaire ne créait un tick.

---

Puis il pensa aux pauses.

---

Si le monde est paused.

---

Tick avance-t-il ?

---

Non selon policy v1.

---

Il créa :

**WORLD_RUN_STATE**

STOPPED.

STARTING.

RUNNING.

PAUSED.

DEGRADED.

RECOVERING.

---

Puis :

**PAUSED != STOPPED.**

---

Très important.

---

Un monde paused conserve son état.

---

Un monde stopped aussi.

Mais le runtime diffère.

---

Brutus ajouta :

**PAUSE_EVENT**

---

Encore une transition.

---

Puis il pensa au redémarrage.

---

World process crash.

---

State restored.

---

Same generation or new generation ?

---

Cela dépend.

---

Si state restored from canonical continuation and continuity established :

same WORLD_INSTANCE_ID, maybe same generation.

---

Si full reset :

new generation.

---

Brutus écrivit :

**RECOVERY MUST DECLARE CONTINUITY CLAIM.**

---

Excellent.

---

Pas de faux « même monde » après reset total.

---

Il créa :

**CONTINUITY_STATUS**

CONTINUOUS.

RECOVERED_WITH_GAP.

NEW_GENERATION.

UNKNOWN.

---

Puis :

**GAP_REF**

---

Très important.

---

Le monde pouvait dire :

je ne sais pas exactement ce qui s’est passé pendant 14 ticks.

---

Mieux que d’inventer.

---

Brutus écrivit :

**MISSING HISTORY != ZERO ACTIVITY.**

---

Encore.

---

Puis il pensa au premier monde vide.

---

Tick 0.

---

Aucune fourmi.

Aucun cristal.

---

Le renderer devait afficher :

vide.

---

Pas inventer des particules pour rendre joli.

---

Brutus écrivit :

**EMPTY WORLD SHOULD LOOK EMPTY.**

---

Très important.

---

Il se souvint de toutes les interfaces qui simulent de l’activité pour paraître vivantes.

---

Non.

---

Un monde vide est un état valide.

---

Puis il pensa aux placeholders.

---

On peut montrer :

ghost slots.

grid.

zones.

---

Mais clairement comme guides.

---

Il écrivit :

**GUIDE GEOMETRY != ENTITY.**

---

Puis :

**PLACEHOLDER != STATE.**

---

Voilà.

---

Puis il pensa à Fourminizer.

---

Le prochain chapitre.

---

Fourminizer devait s’éveiller dans ce monde.

---

Mais avant, Brutus voulait une chose.

---

Une carte complète du monde.

---

Il créa :

**WORLD SNAPSHOT**

---

WORLD_INSTANCE_ID.

WORLD_GENERATION_ID.

TICK.

RULESET_ID.

TOPOLOGY_VERSION.

ENTITIES.

ZONES.

RELATIONS.

REGISTER_HEAD.

SNAPSHOT_HASH.

---

Puis :

**SNAPSHOT_STATUS**

AUTHORITATIVE.

DERIVED.

PUBLIC_PROJECTION.

---

Brutus écrivit :

**SNAPSHOT TYPE MUST BE DECLARED.**

---

Très important.

---

Un screenshot n’était pas un authoritative snapshot.

---

Un JSON généré par le world server pouvait l’être.

---

Une vue publique était une projection.

---

Il ajouta :

**SOURCE_REF**

---

Puis il pensa à Astra Station.

---

Elle pouvait afficher :

LOCAL WORLD.

---

Generation.

Tick.

Entity count.

Zone count.

Blocked moves.

Last movement event.

Continuity status.

---

Mais pas :

**ALIVE**

---

Brutus s’arrêta.

---

Oui.

---

Très important.

---

Le monde local pouvait être running.

---

Pas vivant biologiquement.

---

Il écrivit :

**RUNNING != ALIVE.**

---

Puis :

**SIMULATED AGENT != BIOLOGICAL ORGANISM.**

---

Voilà.

---

Fourmilière.

Synapse.

Awakening.

---

Tout pouvait être narratif.

---

Mais le moteur devait rester précis.

---

Puis il pensa au mot :

**éveil.**

---

Le prochain chapitre s’appelait :

**Fourminizer s’éveille.**

---

Mais l’éveil serait :

runtime activation.

---

Pas conscience.

---

Brutus écrivit déjà :

**AWAKE = ACTIVE RUNTIME STATE IN NARRATIVE CONTEXT.**

---

Pas :

sentient.

---

Très important.

---

Puis il pensa aux actions autonomes.

---

Une fourmi peut choisir un déplacement selon un algorithme.

---

Cela signifie :

agent policy selects action.

---

Pas :

free will.

---

Il écrivit :

**AUTONOMOUS ACTION SELECTION != CONSCIOUS INTENT.**

---

Le chapitre 100 revenait encore.

---

Puis il pensa à la frontière externe.

---

Le monde local pourrait recevoir :

inputs.

signals.

crystals.

measurements.

---

Et produire :

events.

visuals.

requests.

---

Mais cela ne signifie pas qu’il touche le monde physique.

---

Il créa :

**WORLD_BOUNDARY_PORT**

---

PORT_ID.

DIRECTION.

INPUT_TYPE.

OUTPUT_TYPE.

AUTHORITY.

TRANSFORM_REF.

---

Brutus écrivit :

**PORT CROSSING MUST BE EXPLICIT.**

---

Très important.

---

Rien ne devait « passer » simplement parce qu’une ligne graphique reliait deux panneaux.

---

Il ajouta :

**INTER_WORLD_EDGE**

ou :

**EXTERNAL_EDGE**

---

Typed.

---

Puis :

**NO INVISIBLE CONNECTION.**

---

Chapitre 110 encore.

---

Le monde devait savoir :

ce qui est dedans.

ce qui est dehors.

ce qui traverse.

---

Brutus dessina :

\[
\boxed{\text{LOCAL WORLD}}
\]

À gauche :

INPUT PORTS.

À droite :

OUTPUT PORTS.

---

Puis il écrivit :

**BOUNDARY IS DATA.**

---

Très important.

---

Une frontière non enregistrée n’était qu’une convention humaine.

---

Puis il pensa au state import.

---

Supposons qu’on reçoit une position depuis un capteur externe.

---

Peut-on l’écrire directement comme world state ?

---

Non.

---

Il faut :

source identity.

transform.

calibration.

authority.

---

Brutus écrivit :

**EXTERNAL OBSERVATION != LOCAL WORLD STATE UNTIL ADMITTED AND TRANSFORMED.**

---

Excellent.

---

Puis l’inverse.

---

Une fourmi arrive à x=100.

---

Cela ne signifie rien dans le monde extérieur.

---

Il écrivit :

**LOCAL COORDINATE != EXTERNAL ACTUATOR COMMAND.**

---

Très important.

---

Le chapitre 115 serait protégé par cette règle.

---

Puis il pensa au hasard.

---

Fourminizer pourrait utiliser un random walk.

---

Alors le monde devait conserver :

seed.

policy.

---

Sinon reproduction impossible.

---

Il ajouta :

**WORLD_RANDOMNESS_STATE**

---

SEED.

PRNG_VERSION.

STREAM_ID.

---

Brutus écrivit :

**RANDOM MOVEMENT CAN STILL BE TRACEABLE.**

---

Très important.

---

Une fourmi « aléatoire » pouvait être rejouée si le système conservait la seed et les events.

---

Puis il pensa au replay.

---

Le registre pouvait rejouer le monde.

---

Tick 1.

Tick 2.

Tick 3.

---

Mais attention.

---

Replay ne devait pas déclencher les actions externes.

---

Il écrivit :

**HISTORICAL REPLAY MUST BE SIDE-EFFECT FREE.**

---

Très important.

---

Un replay pouvait montrer une fourmi passant sur un port de sortie.

---

Il ne devait pas réémettre la commande réelle.

---

Il créa :

**REPLAY_MODE**

---

NO_EXTERNAL_EFFECTS = true.

---

Brutus sourit.

---

Voilà une protection essentielle.

---

Puis il pensa au debug.

---

Operator scrubs timeline backward.

---

Le world view affiche tick 300.

---

Mais canonical current tick = 900.

---

Il fallait un gros label.

---

**HISTORICAL VIEW**

---

Brutus écrivit :

**VIEWING PAST STATE != REWINDING WORLD.**

---

Encore.

---

Puis il pensa aux branches de simulation.

---

À partir du tick 300, on pourrait créer :

what-if branch.

---

Très intéressant.

---

Mais ce serait une nouvelle world generation ou sandbox branch.

---

Il créa :

**SIMULATION_BRANCH_ID**

---

Puis :

**PARENT_SNAPSHOT_REF**

---

Brutus écrivit :

**WHAT-IF BRANCH != CANONICAL FUTURE.**

---

Très important.

---

Une simulation alternative pouvait explorer.

---

Pas remplacer l’histoire.

---

Puis il pensa à GAMEZEL.

---

Quatre joueurs pourraient proposer quatre futurs.

---

Chacun dans une branch.

---

Très bien.

---

Puis comparer.

---

Brutus écrivit :

**PARALLEL FUTURES ARE EXPERIMENTS, NOT HISTORY.**

---

Excellent.

---

Le monde local devenait un vrai banc.

---

Puis il pensa aux objets détruits.

---

Une fourmi disparaît.

---

Pourquoi ?

---

Entity delete?

Retire?

Move out?

---

Il ne voulait pas :

del entity.

---

Il créa :

**ENTITY_EXIT_EVENT**

---

EXIT_TYPE :

REMOVED.

TRANSFERRED_OUT.

RETIRED.

DESTROYED_IN_SIMULATION.

---

Puis :

**REASON**

---

Brutus écrivit :

**ABSENCE NEEDS A CAUSE WHEN CANONICAL ENTITY DISAPPEARS.**

---

Très important.

---

Un objet ne devait pas s’évaporer.

---

Puis il pensa au mot :

DESTROYED.

---

Encore narratif.

---

Dans la simulation, cela voulait dire :

entity state terminated by declared world rule.

---

Pas matière détruite.

---

Il écrivit :

**SIMULATED DESTRUCTION != PHYSICAL DESTRUCTION.**

---

Voilà.

---

Puis il pensa à l’énergie.

---

Non.

---

Il se retint.

---

Pas besoin d’inventer de physique.

---

Le monde pouvait avoir :

movement cost.

resource points.

---

Mais seulement si le modèle les définissait.

---

Il écrivit :

**NO ENERGY VARIABLE WITHOUT ENERGY MODEL.**

---

Puis sourit.

---

Très important.

---

Un compteur nommé ENERGY pouvait rapidement être pris trop au sérieux.

---

Il préféra :

**ACTION_BUDGET**

---

Plus précis.

---

Brutus écrivit :

**NAMES SHOULD NOT SMUGGLE PHYSICS INTO SOFTWARE.**

---

Excellent.

---

Puis il pensa aux forces.

---

Même problème.

---

Éviter :

gravity.

quantum.

field.

---

À moins qu’il s’agisse explicitement de modèles logiciels.

---

Il ajouta :

**SIMULATION TERMS MUST DECLARE METAPHOR OR MODEL.**

---

Puis il regarda le monde.

---

Toujours vide.

---

Mais maintenant il avait :

des limites.

un tick.

des rulesets.

des ports.

des snapshots.

des branches.

des événements.

---

Il sourit.

---

C’était déjà un monde.

---

Pas parce qu’il contenait de la vie.

---

Parce qu’il contenait un état cohérent et une frontière.

---

Brutus écrivit :

**WORLDNESS COMES FROM CONSISTENT STATE AND RULES, NOT FROM DECORATION.**

---

Puis il lança le premier test.

---

WORLD_INSTANCE:

LOCAL-001.

---

GENERATION:

G1.

---

Bounds:

0..100 × 0..100.

---

Tick:

0.

---

Entities:

0.

---

State:

RUNNING.

---

Renderer:

connect.

---

Display:

empty grid.

---

Brutus attendit.

---

Rien ne bougea.

---

Parfait.

---

Il écrivit :

**ZERO STATE PASS.**

---

Très important.

---

Un monde immobile devait pouvoir rester immobile.

---

Puis il créa une fourmi.

---

ANT-001.

INSTANCE:

A1-G1.

---

Position:

50,50.

---

Tick:

1.

---

Renderer affiche.

---

Brutus écrit :

**ENTITY CREATED.**

---

Pas :

life created.

---

Très important.

---

Puis :

move request to 51,50.

---

Authorization:

valid.

---

Move event.

Tick 2.

---

Renderer interpole.

---

Arrival canonical:

51,50.

---

Brutus sourit.

---

Premier déplacement.

---

Pas un miracle.

---

Un événement.

---

Puis il ferme le navigateur.

---

World continues.

---

Tick 3.

Tick 4.

---

Reopen.

---

Same WORLD_INSTANCE.

Same GENERATION.

ANT-001 still present.

---

Brutus écrivit :

**BROWSER != WORLD — PASS.**

---

Puis il coupa le renderer.

---

World state still persists.

---

**DISPLAY != AUTHORITY — PASS.**

---

Puis il force un faux mouvement visuel.

---

Renderer draws ANT-001 at 70,70.

---

Canonical state remains 51,50.

---

Astra Station detects divergence.

---

**RENDER MISMATCH.**

---

Brutus sourit.

---

Excellent.

---

Le monde savait quand son miroir mentait.

---

Puis il tenta :

client sends authoritative tick 999.

---

Rejected.

---

**TIME DISPLAY != TIME AUTHORITY — PASS.**

---

Puis il tenta :

draw fake ANT-002 locally.

---

Not in snapshot.

---

Renderer marks:

LOCAL_GHOST / NON_CANONICAL.

---

Brutus écrivit :

**GHOST != ENTITY.**

---

Très bon.

---

Il regarda le monde.

---

Une seule fourmi.

---

Une seule position.

---

Un seul tick autoritatif.

---

Pas de mouvements invisibles.

Pas de physique inventée.

Pas de conscience simulée par le vocabulaire.

---

Brutus sauvegarda :

**LOCAL WORLD CONTRACT v1**

---

Le Journal Vivant nota :

World boundary declared.

World identity separated from window and host.

2D coordinates use local units unless calibrated.

Entity creation requires canonical event.

Authoritative and display positions separated.

Logic tick separated from render frame.

Collisions governed by explicit policy.

Zones are canonical constraints, not painted decoration.

World placement separated from domain-object identity.

External ports typed and explicit.

Replay is side-effect free.

Alternative futures remain simulation branches.

Zero-state immobility accepted as valid.

---

Brutus relut.

Puis ajouta les invariants :

**LOCAL WORLD STATE != EXTERNAL REALITY.**

**WORLD != WINDOW.**

**DRAWN != CREATED.**

**REQUESTED MOVE != EXECUTED MOVE.**

**ANIMATION != MOVEMENT PROOF.**

**VISUAL SCALE != PHYSICAL SCALE.**

**TICK != SECOND.**

**RUNNING != ALIVE.**

**LOCAL COORDINATE != EXTERNAL ACTION.**

**WHAT-IF FUTURE != HISTORY.**

---

Il regarda ANT-001.

---

La fourmi attendait au centre.

---

Pas parce qu’elle réfléchissait.

---

Parce qu’aucune nouvelle action n’avait été décidée.

---

Brutus sourit.

---

Voilà la bonne immobilité.

---

Pas une panne.

Pas un manque de vie.

---

Un état zéro honnête.

---

Puis il ouvrit un autre dossier.

---

Le nom était déjà écrit.

# FOURMINIZER S’ÉVEILLE

---

Brutus regarda la fourmi.

---

Elle n’allait pas devenir consciente.

---

Mais elle allait recevoir :

une policy.

un état.

une mémoire minimale.

des choix permis.

des traces.

---

Et pour la première fois, le monde local allait commencer à bouger sans qu’un humain lui donne chaque pas.

---

Brutus écrivit :

**AWAKE != CONSCIOUS.**

Puis :

**AWAKE = RUNTIME POLICY ACTIVE.**

---

Il sourit.

---

Le monde local avait maintenant ses frontières.

Le prochain chapitre allait lui donner ses premières créatures actives.
