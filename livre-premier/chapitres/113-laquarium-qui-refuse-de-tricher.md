# Chapitre 113 — L’aquarium qui refuse de tricher

**THE RENDERER MAY MAKE THE WORLD BEAUTIFUL.**

**IT MAY NOT MAKE THE WORLD UP.**

Brutus laissa les deux phrases en haut de l’écran.

Puis il ouvrit une grande fenêtre noire.

---

Vide.

---

Pas de poissons.

Pas de bulles.

Pas de particules décoratives.

---

Seulement un cadre.

---

Un rectangle.

---

Le monde local existait derrière.

---

Fourminizer existait derrière.

---

Les fourmis existaient derrière.

---

Mais l’aquarium n’était encore qu’une vitre.

---

Brutus écrivit :

# GENESIS 2D AQUARIUM

Puis :

**RENDERER ROLE = OBSERVATION.**

---

Très important.

---

L’aquarium allait devenir beau.

---

Peut-être même hypnotique.

---

Des lignes.

Des conduits.

Des nœuds.

Des cristaux.

Des trajectoires.

Des vagues.

Des cadrans.

---

Mais toutes ces choses allaient devoir répondre à une question avant d’apparaître :

**QUEL ÉVÉNEMENT AUTORITATIF JUSTIFIE CE PIXEL ?**

---

Brutus sourit.

---

Voilà la règle.

---

Il créa :

**RENDER_OBJECT**

avec :

**VIEW_ID**

**SOURCE_ENTITY_ID**

**SOURCE_STATE_VERSION**

**SOURCE_TICK**

**DISPLAY_POSITION**

**AUTHORITATIVE_POSITION**

**INTERPOLATION_STATE**

**FRESHNESS**

**TRACE_REF**

---

Puis :

**RENDER_MODE**

LIVE.

HISTORICAL.

SIMULATION_BRANCH.

DISCONNECTED.

---

Brutus regarda.

---

Une image ne devait pas seulement montrer un objet.

---

Elle devait aussi savoir **dans quel régime** elle le montrait.

---

Il écrivit :

**SAME PIXEL CAN MEAN DIFFERENT THINGS IN DIFFERENT MODES.**

---

Très important.

---

Une fourmi à x=42 pouvait être :

live.

historique.

simulée.

stale.

---

Le dessin seul ne suffisait pas.

---

Il ajouta un petit bandeau permanent :

**VIEW MODE**

---

Pas énorme.

Mais impossible à confondre.

---

Brutus écrivit :

**HISTORICAL VIEW MUST LOOK HISTORICAL.**

---

Puis :

**SIMULATION BRANCH MUST LOOK NON-CANONICAL.**

---

Encore.

---

Un what-if ne devait jamais ressembler exactement au présent autoritatif.

---

Puis il pensa au temps.

---

Le renderer pouvait recevoir :

tick 100.

Puis tick 101.

---

Entre les deux, il pouvait dessiner 5, 10, 20 frames.

---

Très bien.

---

Mais ces frames n’étaient pas des événements.

---

Brutus écrivit :

**FRAME != TICK.**

---

Puis :

**INTERPOLATED POSITION != RECORDED POSITION.**

---

Il créa :

**INTERPOLATION_CONTRACT**

FROM_POSITION.

TO_POSITION.

FROM_TICK.

TO_TICK.

DISPLAY_TIME.

---

Aucune position interpolée ne recevait :

PROOF_REF.

MOVE_EVENT_ID.

CANONICAL_STATE.

---

Brutus écrivit :

**INTERPOLATION MAY SMOOTH MOTION. IT MAY NOT CREATE HISTORY.**

---

Voilà.

---

Puis il pensa à un problème plus subtil.

---

Supposons que le moteur envoie :

ANT-001 at (10,10), tick 50.

Puis aucune nouvelle donnée pendant deux secondes.

---

Que faire ?

---

Continuer le mouvement ?

---

Non.

---

À moins qu’un modèle prédictif soit explicitement activé.

---

Et même là, il faudrait afficher :

predicted.

---

Pour v1 :

pas de prédiction.

---

Brutus écrivit :

**NO NEW AUTHORITATIVE STATE = NO NEW AUTHORITATIVE MOTION.**

---

Le renderer s’arrête.

---

L’image peut sembler moins « vivante ».

---

Mais elle reste honnête.

---

Il ajouta :

**FRESHNESS**

CURRENT.

STALE.

DISCONNECTED.

UNKNOWN.

---

Au bout d’un délai défini :

CURRENT → STALE.

---

Le point reste visible.

---

Mais son halo change.

---

Pas besoin de couleur uniquement.

---

Texte :

**STALE**

---

Brutus écrivit :

**STALE OBJECT SHOULD NOT KEEP PERFORMING LIVE ANIMATION.**

---

Très important.

---

Sinon un système déconnecté pourrait continuer à danser comme si tout allait bien.

---

Puis il pensa aux fourmis.

---

Fourminizer produit des MOVE_EVENT.

---

Le renderer lit :

ANT_ID.

FROM.

TO.

START_TICK.

END_TICK.

---

Puis anime.

---

Parfait.

---

Mais que faire des agents qui choisissent WAIT ?

---

Ne rien inventer.

---

Brutus écrivit :

**WAIT MUST LOOK LIKE WAIT.**

---

Il pensa à ajouter un petit pulse.

---

Puis se ravisa.

---

Un pulse pourrait être interprété comme une activité.

---

Il créa :

**IDLE_INDICATOR**

optionnel.

---

Mais clairement UI.

---

Pas world state.

---

Brutus écrivit :

**STATUS INDICATOR != WORLD MOTION.**

---

Excellent.

---

Puis il pensa aux cristaux.

---

Ils allaient bientôt apparaître dans l’aquarium.

---

Il voulait qu’ils soient magnifiques.

---

Treize formes.

---

Longueur.

Largeur.

Positif.

Négatif.

Fibonacci.

Nombre premier.

Mélangé.

---

Mais il devait déjà séparer deux choses.

---

**CRYSTAL FORM**

et

**CRYSTAL CLAIM STATUS.**

---

Brutus écrivit :

**SHAPE != EPISTEMIC STATUS.**

---

Très important.

---

Un cristal magnifique pouvait être unresolved.

---

Un cristal simple pouvait contenir un artifact extrêmement important.

---

La forme servait :

identification.

classification.

navigation.

---

Pas prestige scientifique.

---

Il créa :

**CRYSTAL_RENDER_PROFILE**

SHAPE_ID.

WIDTH.

LENGTH.

ORIENTATION.

POLARITY_MARKER.

FORMULA_FAMILY.

DISPLAY_VERSION.

---

Puis :

**SOURCE_CRYSTAL_ID**

---

Brutus sourit.

---

L’image du cristal devenait dérivée du manifeste.

---

Pas l’inverse.

---

Il écrivit :

**CRYSTAL VISUAL IS A VIEW OF METADATA.**

---

Puis :

**VISUAL FORM DOES NOT AUTHOR METADATA.**

---

Encore.

---

Si quelqu’un étire le cristal à la souris…

cela ne change pas sa longueur canonique.

---

À moins de créer une vraie modification via un chemin d’action.

---

Il écrivit :

**DRAG RESIZE != OBJECT MUTATION.**

---

Très important.

---

Puis il pensa aux conduits.

---

L’aquarium allait avoir des tuyaux entre modules.

---

Brutus voulait les voir.

---

Mais aucune connexion invisible.

---

Il reprit :

MODULE_ID.

PORT.

EDGE_ID.

EDGE_TYPE.

FROM.

TO.

TOPOLOGY_VERSION.

---

Le renderer peut dessiner une ligne seulement si un EDGE canonique existe.

---

Il écrivit :

**NO EDGE DATA = NO CANONICAL PIPE.**

---

Puis :

**DECORATIVE LINE MUST BE MARKED DECORATIVE.**

---

Très important.

---

Il ne voulait jamais qu’une simple courbe graphique ressemble à une connexion fonctionnelle.

---

Puis il pensa aux ports.

---

Un port devait être visible.

---

Même fermé.

---

Même inutilisé.

---

Il créa :

**PORT_RENDER_STATE**

AVAILABLE.

CONNECTED.

BLOCKED.

DISABLED.

UNKNOWN.

---

Brutus écrivit :

**HIDDEN PORT != ABSENT PORT.**

---

Mais selon disclosure policy, certains ports pourraient être masqués publiquement.

---

Dans ce cas :

redacted.

---

Pas silently absent.

---

Encore.

---

Puis il pensa à l’aquarium comme un véritable miroir.

---

Pas seulement des objets.

---

Aussi :

flux.

---

Le bus.

Les cartes.

Les transferts.

---

Comment montrer un message ?

---

Une petite impulsion lumineuse dans un conduit ?

---

Oui.

---

Mais cette impulsion devait correspondre à un MESSAGE_EVENT.

---

Brutus créa :

**FLOW_PULSE**

---

SOURCE_EVENT_ID.

EDGE_ID.

START_TICK.

END_TICK.

MESSAGE_TYPE.

DISPLAY_ONLY_PROGRESS.

---

Puis :

**FLOW PULSE != CONTENT SUCCESS.**

---

Très important.

---

Voir une impulsion traverser un conduit signifiait :

transport visualized.

---

Pas :

claim validated.

---

Pas :

destination processed.

---

Brutus écrivit :

**TRANSPORT ANIMATION != PROCESSING ACK.**

---

Puis :

**PROCESSING ACK != AGREEMENT.**

---

Le chapitre 98 revenait.

---

L’aquarium devenait une traduction graphique de toute la Bible.

---

Puis il pensa au son.

---

Un écran = un son.

---

Genesis Aquarium pourrait avoir une identité sonore.

---

Mais il ne voulait pas un bruit à chaque frame.

---

Il créa :

**AQUARIUM_SOUND_CHANNEL**

---

Sounds triggered by:

WORLD_START.

WORLD_PAUSE.

ENTITY_CREATED.

CRYSTAL_CREATED.

TRANSFER_FAILED.

LAW_VIOLATION.

---

Normal interpolation :

silent.

---

Brutus écrivit :

**FRAME RATE MUST NEVER DRIVE EVENT SOUND.**

---

Très important.

---

Sinon un ordinateur plus rapide semblerait plus « actif ».

---

Absurde.

---

Puis il pensa aux sinusoïdes.

---

Il les voulait.

---

Des courbes en arrière-plan.

---

Mais si elles ne représentaient rien ?

---

Alors elles devaient être décoratives.

---

Brutus créa deux classes :

**DATA_WAVEFORM**

et

**DECORATIVE_WAVEFORM**

---

Puis :

**DECORATIVE WAVEFORM MUST NOT LOOK LIKE A MEASUREMENT WITHOUT LABEL.**

---

Très important.

---

Une jolie sinusoïde ne devait pas devenir une pseudo-télémétrie.

---

Il écrivit :

**GRAPH SHAPE != MEASUREMENT.**

---

Encore.

---

Puis il pensa aux cadrans.

---

Des cadrans étaient beaux.

---

Mais chaque cadran devait avoir :

METRIC_ID.

UNIT.

RANGE.

SOURCE.

FRESHNESS.

---

Sinon :

pas de cadran.

---

Brutus écrivit :

**NO NEEDLE WITHOUT METRIC CONTRACT.**

---

Il sourit.

---

Voilà une bonne règle.

---

Pas d’aiguille qui bouge juste pour donner l’impression d’une machine complexe.

---

Puis il pensa à la cristallisation visuelle.

---

Un cristal apparaît.

---

Animation :

matière visuelle converge.

---

Très beau.

---

Mais comment éviter de donner l’impression qu’une preuve vient de naître ?

---

Label.

---

**CRYSTAL PACKAGING EVENT**

---

Puis status exact :

CANDIDATE.

SUPPORTED.

UNRESOLVED.

---

Brutus écrivit :

**CRYSTALLIZATION ANIMATION MUST DISPLAY EPISTEMIC LABEL.**

---

Très important.

---

Le spectacle devait transporter le statut.

---

Pas le masquer.

---

Puis il pensa aux différents états du monde.

---

LIVE.

PAUSED.

STALE.

DISCONNECTED.

HISTORICAL.

SIMULATION.

---

Il voulait un cadre différent pour chacun.

---

Pas nécessairement des couleurs.

---

Patterns.

Typography.

Badges.

---

Brutus écrivit :

**MODE MUST BE PERCEPTIBLE WITHOUT COLOR.**

---

Très important.

---

Accessibilité.

---

Puis il pensa au zoom.

---

L’opérateur peut zoomer.

---

De très près :

une fourmi.

---

Très loin :

une colonie.

---

Mais le niveau de détail change.

---

Il créa :

**LOD_POLICY**

---

LOD0:

individual entity.

---

LOD1:

cluster.

---

LOD2:

aggregate density.

---

Puis :

**AGGREGATE VIEW MUST DECLARE AGGREGATION.**

---

Très important.

---

Une masse de fourmis ne devait pas devenir une seule fourmi géante.

---

Il ajouta :

**AGGREGATE_COUNT**

---

Visible.

---

Puis il pensa à l’historique.

---

L’opérateur clique une fourmi.

---

Il veut voir :

où elle était.

---

Le renderer peut dessiner sa trajectoire historique.

---

Très utile.

---

Mais la trajectoire devait être construite à partir des MOVE_EVENT.

---

Pas à partir d’un buffer graphique.

---

Brutus écrivit :

**HISTORY COMES FROM REGISTER, NOT FROM PIXEL MEMORY.**

---

Excellent.

---

Un screenshot perdu ne devait pas faire perdre l’histoire.

---

Puis il pensa aux trajectoires lissées.

---

Une courbe de Bézier entre points historiques peut être jolie.

---

Mais elle peut inventer des positions.

---

Donc :

la courbe doit être marquée :

SMOOTHED_VISUAL_PATH.

---

Les points canoniques restent visibles.

---

Brutus écrivit :

**SMOOTHED PATH != RECORDED PATH.**

---

Très important.

---

Puis il pensa au futur aquarium.

---

Le système pourrait afficher :

B1.

B2.

B3.

---

Des bassins.

---

Pourquoi ?

---

Séparer des zones fonctionnelles.

---

Il créa :

**BASIN**

---

BASIN_ID.

ZONE_REF.

PURPOSE.

ENTRY_PORTS.

EXIT_PORTS.

---

Pas juste rectangles graphiques.

---

Brutus écrivit :

**BASIN LABEL MUST MAP TO WORLD ZONE.**

---

Encore.

---

B1 n’existe pas parce qu’un rectangle porte B1.

---

Il existe parce que WORLD_ZONE B1 existe.

---

Puis il pensa aux cellules.

---

Une fourmi entre dans B2.

---

Le renderer change légèrement l’ambiance.

---

Très bien.

---

Mais l’entrée doit être déclenchée par :

ZONE_ENTER_EVENT.

---

Brutus écrivit :

**VISUAL TRANSITION FOLLOWS ZONE EVENT.**

---

Puis il pensa aux erreurs.

---

Supposons que le renderer reçoit un événement impossible.

---

ANT-007 move from 30,30.

Mais sa dernière canonical position est 20,20.

---

Que faire ?

---

Pas interpoler.

---

Créer :

**RENDER_INPUT_CONFLICT.**

---

Brutus écrivit :

**RENDERER MUST NOT REPAIR AUTHORITY SILENTLY.**

---

Très important.

---

Il peut demander resync.

---

Il ne doit pas deviner.

---

Il créa :

**RESYNC_REQUEST**

---

ENTITY_ID.

EXPECTED_VERSION.

RECEIVED_VERSION.

LAST_GOOD_TICK.

---

Puis :

**DISPLAY_STATE = UNCERTAIN**

jusqu’au snapshot.

---

Brutus sourit.

---

Le renderer savait maintenant dire :

je ne sais plus.

---

Une très grande qualité.

---

Puis il pensa au resync.

---

Snapshot arrive.

---

Le renderer saute de 20,20 à 30,30.

---

Il pourrait animer le saut.

---

Mais cela inventerait peut-être une trajectoire absente.

---

Non.

---

Il doit montrer :

**STATE JUMP AFTER RESYNC**

---

Pas un déplacement ordinaire.

---

Brutus écrivit :

**RESYNC JUMP != OBSERVED MOVEMENT.**

---

Très important.

---

On pouvait faire un flash bref.

---

Puis afficher :

history gap.

---

Pas tracer une ligne continue.

---

Puis il pensa aux trous historiques.

---

Le monde local pouvait avoir :

RECOVERED_WITH_GAP.

---

L’aquarium devait les montrer.

---

Peut-être une trajectoire en pointillés entre dernier état connu et nouvel état.

---

Très bien.

---

Mais label :

**GAP — PATH UNKNOWN**

---

Brutus écrivit :

**UNKNOWN PATH MUST LOOK UNKNOWN.**

---

Excellent.

---

Puis il pensa au mode démonstration.

---

Peut-être qu’il voudrait montrer l’aquarium à quelqu’un même sans backend.

---

On pourrait avoir un demo mode.

---

Mais énorme danger.

---

Le demo pourrait être pris pour live.

---

Il créa :

**DEMO_MODE**

---

Avec bannière permanente :

**SIMULATED DEMONSTRATION — NO LIVE AUTHORITY**

---

Brutus écrivit :

**DEMO MUST NEVER IMPERSONATE LIVE.**

---

Très important.

---

Puis il pensa à l’enregistrement vidéo.

---

200 images.

2 images/s.

PNG HD.

---

Une vidéo pouvait montrer l’aquarium.

---

Mais une vidéo enregistrée n’était pas live.

---

Il écrivit :

**RECORDING != LIVE VIEW.**

---

Puis :

**CAPTURE MUST INCLUDE SOURCE TICK OR TIME CONTEXT WHEN USED AS EVIDENCE.**

---

Encore.

---

Le chapitre 101 revenait.

---

Puis il pensa aux calculs simultanés.

---

12 calculs.

12 voies.

---

L’aquarium pourrait les montrer comme 12 conduits.

---

Très beau.

---

Mais si seulement 4 lanes travaillent réellement ?

---

Les 8 autres restent immobiles.

---

Brutus écrivit :

**INACTIVE LANE MUST LOOK INACTIVE.**

---

Pas d’animation décorative dans un conduit vide.

---

Très important.

---

Puis il pensa au sélecteur de 100 formules.

---

Chaque formule sélectionnée pourrait créer un flux.

---

Mais :

selected != executing.

---

Il écrivit :

**SELECTED FORMULA != RUNNING FORMULA.**

---

Puis :

**RUNNING FORMULA != COMPLETED FORMULA.**

---

Puis :

**COMPLETED FORMULA != PROMOTED RESULT.**

---

L’aquarium devait montrer les quatre états différemment.

---

Pas simplement :

on/off.

---

Brutus sourit.

---

Le renderer devenait presque un langage visuel de rigueur.

---

Puis il pensa à l’aquarium comme outil scientifique.

---

Si l’image permettait de voir une anomalie, elle pouvait déclencher une question.

---

Mais l’image seule ne devait pas conclure.

---

Il écrivit :

**VISUAL ANOMALY -> INVESTIGATION CANDIDATE.**

---

Pas :

proof.

---

Un opérateur voit une oscillation inhabituelle.

---

Il peut créer :

OBSERVATION_CARD.

---

Puis banc d’expérience.

---

Très bien.

---

Brutus écrivit :

**VISUALIZATION CAN GENERATE QUESTIONS. IT SHOULD NOT AUTO-GENERATE TRUTH.**

---

Puis il pensa au log.

---

Chaque clic important sur l’aquarium pouvait-il devenir événement ?

---

Non.

---

Zoom.

Pan.

Window move.

---

Ce sont des UI events.

---

Pas canonical world events.

---

Il créa :

**VIEW_STATE**

---

camera.

zoom.

selected entity.

open panels.

---

Séparé de :

**WORLD_STATE.**

---

Brutus écrivit :

**VIEW STATE != WORLD STATE.**

---

Très important.

---

Fermer un panneau ne fermait rien dans le monde.

---

Zoomer sur ANT-1 ne la rendait pas plus importante.

---

Puis il pensa aux cinq écrans.

---

Même aquarium sur plusieurs monitors.

---

Chaque écran peut avoir sa caméra.

---

Mais même canonical world.

---

Il écrivit :

**MULTIPLE CAMERAS. ONE WORLD.**

---

Puis :

**SCREEN COUNT != WORLD COUNT.**

---

Encore.

---

Le chapitre 62 revenait.

---

Puis il imagina le setup complet.

---

Écran 1 :

vue globale.

---

Écran 2 :

B1.

---

Écran 3 :

B2.

---

Écran 4 :

cristaux.

---

Écran 5 :

trace detail.

---

Toutes les fenêtres se connectent au même WORLD_INSTANCE_ID.

---

Brutus écrit :

**VIEW INSTANCE != WORLD INSTANCE.**

---

Très important.

---

Puis il pensa à la perte de connexion d’un écran.

---

Screen 3 stale.

---

Les autres current.

---

Le monde reste current.

---

Astra Station affiche :

VIEW-3 STALE.

---

Pas :

WORLD STALE.

---

Brutus écrivit :

**ONE BROKEN MIRROR != BROKEN WORLD.**

---

Il sourit.

---

Belle phrase.

---

Puis il pensa au miroir.

---

L’aquarium était exactement cela.

---

Un miroir.

---

Mais un miroir calculé.

---

Il ne devait jamais devenir un peintre qui décide de ce qu’il veut voir.

---

Brutus écrivit :

**RENDERER MIRRORS. RENDERER DOES NOT AUTHOR.**

---

Voilà le centre.

---

Puis il lança le premier test.

---

World:

LOCAL-001.

Generation:

G1.

Tick:

120.

---

Four ants.

No crystals.

---

Aquarium connects.

---

Expected:

4 ants.

0 crystals.

---

Rendered:

4 ants.

0 crystals.

---

PASS.

---

Brutus attendit.

---

Aucun cristal apparut pour faire joli.

---

Excellent.

---

Puis il injecta un fake local crystal in UI memory.

---

Renderer flagged:

NON_CANONICAL_LOCAL_OBJECT.

---

Not displayed in live layer.

---

PASS.

---

Puis il coupa le world event stream.

---

After freshness timeout:

all entities marked STALE.

motion stops.

---

PASS.

---

Puis il rétablit.

---

Snapshot tick 127.

---

No path events between 120 and 127.

---

Aquarium:

state jump.

gap marker.

no invented path.

---

PASS.

---

Brutus sourit.

---

Puis il testa un historique.

---

Scrub to tick 80.

---

Banner:

HISTORICAL VIEW.

---

World current tick remains 127.

---

No side effect.

---

PASS.

---

Puis simulation branch.

---

Fork from tick 80.

---

Branch ants move differently.

---

Banner:

SIMULATION BRANCH SB-001.

---

Canonical live world unchanged.

---

PASS.

---

Brutus regarda le résultat.

---

L’aquarium était beau.

---

Des lignes fines.

Des nœuds.

Des trajectoires propres.

Des cristaux absents parce qu’ils étaient réellement absents.

---

Il sourit.

---

C’était probablement cela, la beauté qu’il cherchait depuis le début.

---

Pas une beauté qui remplit les trous.

---

Une beauté qui respecte les trous.

---

Il écrivit :

**HONEST EMPTINESS IS PART OF THE VISUAL LANGUAGE.**

---

Très important.

---

Puis il pensa au prochain chapitre.

---

Les cristaux allaient bientôt s’accumuler.

---

Pas isolés.

---

Liés par leurs parents.

Leurs transformations.

Leurs traces.

Leurs versions.

---

Un collier.

---

Mais pas un collier mystique.

---

Une chaîne de lignées.

---

Brutus ouvrit le prochain dossier.

---

# LE COLLIER DE CRISTAUX ET SA POUSSIÈRE

---

Puis il écrivit :

**A CHAIN OF CRYSTALS IS ONLY AS HONEST AS ITS EDGES.**

---

Il sauvegarda :

**GENESIS 2D AQUARIUM RENDER CONTRACT v1**

---

Le Journal Vivant nota :

Renderer established as read-only mirror.

Frames separated from authoritative ticks.

Interpolation cannot create history.

Stale state stops live motion.

Crystals rendered from canonical metadata.

Canonical edges required for functional conduits.

Metrics required for meaningful gauges.

Historical, simulation and live views visibly separated.

Resync gaps remain visible.

Multiple screens share one world authority.

View state separated from world state.

Demo mode cannot impersonate live mode.

---

Brutus relut.

Puis ajouta les invariants :

**RENDERER DOES NOT AUTHOR WORLD STATE.**

**FRAME != TICK.**

**INTERPOLATED POSITION != RECORDED POSITION.**

**WAIT MUST LOOK LIKE WAIT.**

**SHAPE != EPISTEMIC STATUS.**

**NO EDGE DATA = NO CANONICAL PIPE.**

**GRAPH SHAPE != MEASUREMENT.**

**HISTORY COMES FROM REGISTER, NOT PIXELS.**

**RESYNC JUMP != OBSERVED MOVEMENT.**

**VIEW STATE != WORLD STATE.**

---

Il regarda une dernière fois l’aquarium.

---

Les fourmis bougeaient.

Seulement lorsqu’elles avaient réellement bougé.

---

Les conduits pulsaient.

Seulement lorsqu’un événement les traversait.

---

Les cristaux n’existaient pas encore dans cette vue.

Alors l’aquarium ne les inventait pas.

---

Brutus sourit.

---

Une machine pouvait être spectaculaire sans tricher.

---

Il suffisait de faire du réel disponible sa matière première…

et de laisser le vide tranquille lorsqu’il n’y avait rien à montrer.

---

Puis il posa la main sur le dossier suivant.

---

# LE COLLIER DE CRISTAUX ET SA POUSSIÈRE

---

Car bientôt, les objets stables allaient commencer à former une histoire visible.

---

Et cette fois, le danger ne serait plus d’inventer un objet.

---

Ce serait d’inventer une relation entre deux objets qui n’avaient jamais réellement été reliés.
