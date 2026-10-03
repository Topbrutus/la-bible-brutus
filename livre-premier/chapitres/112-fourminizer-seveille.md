# Chapitre 112 — Fourminizer s’éveille

**AWAKE != CONSCIOUS.**

Puis, juste en dessous :

**AWAKE = RUNTIME POLICY ACTIVE.**

Brutus laissa les deux phrases visibles.

Au centre du monde local, ANT-001 attendait toujours.

---

Position :

51,50.

---

Tick :

4.

---

State :

IDLE.

---

Pas de mouvement.

Pas de son.

Pas de lumière supplémentaire.

---

Le monde fonctionnait parfaitement.

---

Et pourtant, rien ne se passait.

---

Brutus sourit.

---

C’était exactement le bon point de départ.

---

Parce qu’avant d’apprendre à une fourmi à agir…

il fallait savoir si le système était capable de respecter son immobilité.

---

Il écrivit :

**NO ACTION REQUESTED = NO ACTION EXECUTED.**

---

Puis :

**IDLE != FAILURE.**

---

Très important.

---

Une machine qui bouge toujours n’est pas nécessairement plus vivante.

---

Parfois, elle est seulement incapable de s’arrêter.

---

Brutus ouvrit un nouveau dossier.

# FOURMINIZER

---

Puis il regarda ANT-001.

---

Pour l’instant, elle possédait :

un ID.

une instance.

une position.

un tick.

un état.

une trace.

---

Mais aucun mécanisme pour choisir ce qu’elle ferait ensuite.

---

Brutus créa :

**ANT_AGENT**

avec :

**ANT_ID**

**INSTANCE_ID**

**WORLD_REF**

**POSITION**

**STATE**

**POLICY_REF**

**MEMORY_REF**

**ACTION_BUDGET**

**CURRENT_OBJECT_REF**

**LINEAGE_REF**

**LATEST_TRACE**

**TICK**

---

Puis il ajouta :

**AGENT_MODE**

---

MANUAL.

POLICY_DRIVEN.

PAUSED.

DISABLED.

---

ANT-001 passa de :

MANUAL

à :

POLICY_DRIVEN.

---

Brutus regarda l’écran.

---

Elle ne bougea pas.

---

Parfait.

---

Il écrivit :

**POLICY ASSIGNED != ACTION SELECTED.**

---

Encore une frontière.

---

Puis il pensa au mot :

**agent.**

---

Dangereux aussi.

---

Un agent logiciel pouvait sélectionner des actions.

---

Cela ne signifiait pas :

volonté.

conscience.

intention humaine.

---

Brutus écrivit :

**AGENT != PERSON.**

Puis :

**ACTION SELECTION != SUBJECTIVE INTENT.**

---

Très important.

---

Fourminizer serait un moteur de comportement.

---

Pas une usine à prétentions.

---

Il créa :

**ANT_POLICY v1**

---

Observe local state.

Determine eligible actions.

Select one action according to policy.

Submit request.

Wait for authority.

Observe result.

Update memory.

---

Brutus écrivit :

\[
\text{OBSERVE}
\rightarrow
\text{SELECT}
\rightarrow
\text{REQUEST}
\rightarrow
\text{AUTHORITY}
\rightarrow
\text{EVENT}
\rightarrow
\text{MEMORY}
\]

---

Voilà.

---

La fourmi ne mutait jamais directement le monde.

---

Elle proposait.

---

Le monde décidait si le mouvement était admissible.

---

Brutus écrivit :

**AGENT CHOOSES REQUEST. WORLD COMMITS STATE.**

---

Très important.

---

Cela empêchait la politique d’une fourmi de devenir une seconde autorité cachée.

---

Puis il pensa aux actions possibles.

---

ANT-001 pouvait :

WAIT.

MOVE_NORTH.

MOVE_SOUTH.

MOVE_EAST.

MOVE_WEST.

INSPECT_LOCAL.

REQUEST_PICKUP.

REQUEST_DROP.

---

Il s’arrêta.

---

Pickup et drop viendraient plus tard.

---

Pour v1 :

seulement :

WAIT.

NORTH.

SOUTH.

EAST.

WEST.

---

Brutus écrivit :

**START WITH THE SMALLEST ACTION SPACE THAT CAN TEACH THE SYSTEM SOMETHING.**

---

Excellent.

---

Pas besoin de donner vingt pouvoirs dès le premier réveil.

---

Il créa :

**ACTION_TYPE**

WAIT.

MOVE_N.

MOVE_S.

MOVE_E.

MOVE_W.

---

Puis :

**ACTION_ELIGIBILITY**

---

Inside world bounds?

Target blocked?

Action budget available?

Agent enabled?

World running?

---

Brutus sourit.

---

La fourmi pouvait choisir une action.

Mais uniquement parmi les actions admissibles.

---

Il écrivit :

**SELECTABLE != EXECUTABLE.**

---

Encore.

---

Une action pouvait être sélectionnée.

Puis refusée par l’autorité.

---

Très important.

---

Supposons :

ANT-001 sélectionne MOVE_E.

---

Target :

52,50.

---

Policy says eligible.

---

Move request emitted.

---

World checks:

bounds.

collision.

zone.

state version.

authorization.

---

Commit.

---

Tick 5.

---

ANT-001 at:

52,50.

---

Brutus sourit.

---

Premier pas autonome.

---

Mais il se corrigea immédiatement.

---

Pas autonome au sens souverain.

---

Policy-driven.

---

Il écrivit :

**AUTONOMOUS STEP = SELF-SELECTED WITHIN PREAUTHORIZED ACTION SET.**

---

Voilà.

---

Le mot autonomie avait maintenant un scope précis.

---

Puis il pensa au choix de l’action.

---

Comment Fourminizer sélectionne-t-il entre quatre directions ?

---

Pour commencer :

pseudo-aléatoire.

---

Mais traçable.

---

Il créa :

**POLICY_RANDOM_STREAM**

---

PRNG_VERSION.

SEED.

STREAM_ID.

DRAW_INDEX.

---

Puis :

**ACTION_SELECTION_EVENT**

---

ANT_ID.

TICK.

ELIGIBLE_ACTIONS.

POLICY_REF.

RANDOM_DRAW_REF.

SELECTED_ACTION.

TRACE_REF.

---

Brutus écrivit :

**RANDOM CHOICE CAN STILL HAVE PROVENANCE.**

---

Très important.

---

Un comportement non déterministe en apparence pouvait rester rejouable.

---

Puis il pensa à un détail.

---

Si on rejoue le monde…

doit-on recalculer les décisions ou rejouer celles déjà enregistrées ?

---

Deux modes.

---

Il créa :

**REPLAY_POLICY**

EVENT_REPLAY.

POLICY_RECOMPUTE.

---

Puis il écrivit :

**REPLAY OF HISTORY != RECOMPUTATION OF HISTORY.**

---

Très important.

---

EVENT_REPLAY :

rejouer les décisions enregistrées.

---

POLICY_RECOMPUTE :

utilisé seulement en sandbox pour vérifier si la policy actuelle reproduirait les mêmes choix.

---

Pas la même chose.

---

Brutus sourit.

---

Encore une séparation propre.

---

Puis il pensa à la mémoire.

---

Une fourmi devait-elle se souvenir ?

---

Oui.

Mais minimalement.

---

Pas besoin de construire un cerveau imaginaire.

---

Il créa :

**ANT_MEMORY**

---

LAST_POSITION.

LAST_ACTION.

LAST_ACTION_RESULT.

LAST_BLOCK_REASON.

RECENT_VISITS.

CURRENT_TASK_REF.

MEMORY_VERSION.

---

Puis :

**MEMORY_WINDOW**

---

Par exemple :

16 derniers états utiles.

---

Brutus écrivit :

**MEMORY != CONSCIOUSNESS.**

---

Puis :

**MEMORY = PERSISTED STATE USED BY POLICY.**

---

Voilà.

---

La définition devait rester froide.

---

ANT-001 pouvait éviter de revenir immédiatement sur la même case.

---

Pas parce qu’elle « n’aime pas » cette case.

---

Parce que policy :

avoid immediate backtracking when alternatives exist.

---

Brutus écrivit :

**BEHAVIORAL DESCRIPTION SHOULD NOT INVENT MOTIVE.**

---

Très important.

---

Au lieu de :

ANT-001 préfère avancer.

---

Dire :

policy deprioritizes previous position.

---

Encore plus précis.

---

Puis il pensa au mot :

**curiosity.**

---

On pourrait être tenté de créer :

CURIOSITY_SCORE.

---

Il hésita.

---

Non.

---

Pas tant qu’on n’avait pas défini le calcul.

---

Il écrivit :

**DO NOT NAME A VARIABLE AFTER A MENTAL STATE UNLESS IT IS CLEARLY A MODEL LABEL.**

---

Puis créa plutôt :

**NOVELTY_SCORE**

---

Définition :

inverse of recent visit count inside local memory window.

---

Voilà.

---

Brutus écrivit :

**NOVELTY SCORE != CURIOSITY.**

---

Excellent.

---

La fourmi pouvait favoriser les cases moins visitées.

---

Sans prétendre ressentir quoi que ce soit.

---

Puis il pensa au choix de policy.

---

v1 :

eligible moves.

score by novelty.

random tie-break.

---

Simple.

---

Il créa :

\[
S(a)=N(a)
\]

où \(N(a)\) mesure la nouveauté locale de la destination.

---

Puis :

highest score.

random tie.

---

Brutus écrivit :

**POLICY FORMULA IS A SOFTWARE RULE, NOT A MODEL OF ANIMAL COGNITION.**

---

Très important.

---

Fourminizer n’essayait pas de reproduire une vraie fourmi biologique.

---

Il construisait une créature logicielle.

---

Puis il pensa à la visualisation.

---

ANT-001 se déplace.

---

Le renderer peut afficher :

une petite trajectoire.

---

Mais pas une pensée.

---

Pas une bulle :

« je vais à droite ».

---

À moins qu’elle ne soit explicitement un diagnostic de policy.

---

Brutus créa :

**DECISION DEBUG VIEW**

---

Eligible:

N,S,E,W.

Scores:

0.25,0.50,1.00,0.75.

Selected:

E.

---

Très utile.

---

Il écrivit :

**SHOW DECISION DATA, NOT INVENTED INNER MONOLOGUE.**

---

Brutus rit.

---

La fourmi n’avait pas besoin de raconter sa vie.

---

Les nombres suffisaient.

---

Puis il pensa à plusieurs fourmis.

---

Une seule ne testait pas les collisions.

---

Il créa :

ANT-002.

ANT-003.

ANT-004.

---

Même policy.

Différentes seeds.

---

Brutus écrivit :

**SAME POLICY != SAME TRAJECTORY.**

---

Puis :

**DIFFERENT TRAJECTORY != DIFFERENT INTELLIGENCE.**

---

Très important.

---

Les seeds suffisaient à créer des chemins différents.

---

Il lança.

---

Tick 6.

ANT-001 → east.

ANT-002 → north.

ANT-003 → west.

ANT-004 → wait.

---

Brutus regarda.

---

Le monde avait commencé à bouger.

---

Pas beaucoup.

---

Mais honnêtement.

---

Puis tick 7.

---

ANT-001 veut west.

---

Policy sees previous position.

Novelty lower.

Select north instead.

---

Brutus écrivit :

**MEMORY AFFECTED POLICY OUTPUT.**

---

Pas :

ANT-001 learned fear of west.

---

Très important.

---

Puis il pensa à l’apprentissage.

---

Le mot arriverait tôt ou tard.

---

Fourminizer pouvait modifier sa policy à partir de l’expérience.

---

Mais pas encore.

---

Pour l’instant :

fixed policy + changing memory.

---

Il écrivit :

**STATE ADAPTATION != POLICY LEARNING.**

---

Voilà.

---

La trajectoire pouvait changer parce que l’état change.

---

Pas parce que l’algorithme s’était entraîné.

---

Puis il pensa à une vraie future adaptation.

---

Si un jour weights changent :

il faudra :

POLICY_VERSION.

UPDATE_EVENT.

TRAINING_OR_ADAPTATION_REF.

---

Brutus ajouta :

**NO SILENT POLICY MUTATION.**

---

Très important.

---

Une fourmi ne devait pas « devenir différente » sans que le système sache quand et pourquoi.

---

Puis il pensa au parentage.

---

ANT-005 pourrait être créée à partir d’une template dérivée d’ANT-001.

---

Mais pas biologiquement.

---

Il créa :

**POLICY_LINEAGE_REF**

---

Et :

**AGENT_TEMPLATE_REF**

---

Brutus écrivit :

**SOFTWARE LINEAGE != BIOLOGICAL REPRODUCTION.**

---

Encore.

---

Le mot colonie pouvait rester narratif.

---

La structure, elle, restait logicielle.

---

Puis il pensa aux tâches.

---

Une fourmi pouvait avoir :

CURRENT_TASK_REF.

---

Exemple :

explore zone A.

---

Qu’est-ce qu’une tâche ?

---

Il créa :

**ANT_TASK**

---

TASK_ID.

TASK_TYPE.

TARGET_ZONE.

START_TICK.

STOP_CONDITION.

PRIORITY.

AUTHORITY_REF.

TRACE_REF.

---

Puis :

**TASK_TYPE**

EXPLORE.

PATROL.

WAIT.

DELIVER_OBJECT.

OBSERVE.

---

Deliver viendrait plus tard.

---

Pour l’instant :

EXPLORE.

---

Brutus écrivit :

**TASK != COMMAND TO BREAK WORLD RULES.**

---

Très important.

---

Même une tâche prioritaire ne pouvait pas contourner :

bounds.

collision.

authorization.

---

Il ajouta :

**TASK GOAL CANNOT OVERRIDE WORLD INVARIANT.**

---

Voilà.

---

Puis il pensa au scheduler.

---

Qui décide quelle fourmi agit à quel tick ?

---

Il fallait éviter les races.

---

Il créa :

**AGENT_SCHEDULER**

---

Mode :

SEQUENTIAL_BY_ENTITY_ORDER.

ROUND_ROBIN.

PARALLEL_PROPOSAL_SERIAL_COMMIT.

---

Brutus choisit :

**PARALLEL_PROPOSAL_SERIAL_COMMIT**

---

Pourquoi ?

---

Chaque fourmi pouvait calculer sa proposition depuis le même snapshot.

---

Puis l’autorité sérialisait les commits.

---

Brutus écrivit :

**PARALLEL THINKING != PARALLEL STATE MUTATION.**

---

Très important.

---

Il lança un test.

---

Tick 20 snapshot.

---

ANT-001 propose 55,52.

ANT-003 propose aussi 55,52.

---

Collision.

---

World policy :

REJECT_SECOND.

---

Commit order :

ANT-001 accepted.

ANT-003 rejected.

---

ANT-003 result:

BLOCKED_COLLISION.

---

Memory updated.

---

Brutus écrivit :

**FAILED MOVE IS STILL EXPERIENCE DATA.**

---

Très important.

---

ANT-003 pouvait éviter de reproposer immédiatement le même move.

---

Pas parce qu’elle était fâchée.

---

Parce que memory stores block reason.

---

Puis il pensa à la justice.

---

Si entity order favorise toujours ANT-001, elle gagne toujours les collisions.

---

Problème.

---

Il créa :

**COMMIT_ARBITRATION_POLICY**

ROUND_ROBIN_PRIORITY.

DETERMINISTIC_ROTATING_PRIORITY.

RANDOM_WITH_SEED.

---

Pour v1 :

DETERMINISTIC_ROTATING_PRIORITY.

---

Brutus écrivit :

**DETERMINISM DOES NOT REQUIRE PERMANENT FAVORITISM.**

---

Excellent.

---

Chaque tick, priority rotates.

---

Traçable.

---

Puis il pensa au nombre de fourmis.

---

10.

100.

1000.

---

Le renderer pouvait saturer.

---

Mais le monde ne devait pas perdre l’identité.

---

Il écrivit :

**RENDER CAPACITY != WORLD ENTITY CAPACITY.**

---

Si le renderer ne peut afficher que 200 agents :

public projection can aggregate.

---

Mais canonical world knows all.

---

Il créa :

**RENDER_LEVEL_OF_DETAIL**

INDIVIDUAL.

CLUSTERED.

SUMMARY.

---

Puis :

**CLUSTER DISPLAY != MERGED ENTITIES.**

---

Très important.

---

Un groupe visuel de 50 points ne devenait pas une entité unique.

---

Puis il pensa au son.

---

Un écran = un son.

---

Fourminizer pouvait produire des événements sonores.

---

Mais pas un son par fourmi à chaque tick.

---

Ce serait du bruit.

---

Il créa :

**SONIFICATION_POLICY**

---

Event classes :

AGENT_CREATED.

TASK_STARTED.

COLLISION_BLOCK.

OBJECT_PICKUP.

OBJECT_DELIVERY.

SYSTEM_ANOMALY.

---

Normal movement :

silent by default.

---

Brutus écrivit :

**MOVEMENT VOLUME != SOUND VOLUME.**

---

Puis :

**SONIFICATION SHOULD REPRESENT EVENTS, NOT FRAME RATE.**

---

Très important.

---

Le son ne devait pas devenir une deuxième animation mensongère.

---

Puis il pensa au panneau Astra Station.

---

FOURMINIZER.

---

Agents:

4 active.

---

Policy:

ANT_POLICY v1.

---

World tick:

27.

---

Moves accepted:

63.

Moves blocked:

4.

Waiting:

8.

---

Brutus s’arrêta.

---

Ces nombres étaient descriptifs.

---

Pas un score d’intelligence.

---

Il écrivit :

**MOVE COUNT != INTELLIGENCE.**

---

Puis :

**EXPLORATION RATE != COGNITION SCORE.**

---

Très important.

---

Une fourmi qui bouge beaucoup n’était pas « plus intelligente ».

---

Peut-être seulement plus agitée.

---

Il ajouta :

**NO GENERAL INTELLIGENCE METRIC.**

---

Parfait.

---

Puis il pensa aux anomalies.

---

Une fourmi tente soudain de sortir des bounds.

---

Cela peut venir :

policy bug.

bad state.

corrupted request.

---

World rejects.

---

Incident.

---

Brutus écrivit :

**WORLD RULES MUST CONTAIN AGENT ERRORS.**

---

Très important.

---

L’agent n’était pas trusted authority.

---

Même s’il appartenait au système.

---

Il créa :

**AGENT_REQUEST_VALIDATION**

---

schema.

entity identity.

state version.

action type.

bounds.

capability.

---

Then commit.

---

Brutus écrivit :

**INTERNAL AGENT != TRUSTED BY DEFAULT.**

---

Excellent.

---

Puis il pensa à un agent compromis.

---

Il envoie 1000 requests par tick.

---

Rate limit.

---

Il créa :

**MAX_REQUESTS_PER_AGENT_PER_TICK**

---

Pour v1 :

1.

---

Brutus écrivit :

**ONE AGENT. ONE ACTION REQUEST PER LOGIC TICK.**

---

Très propre.

---

Pas nécessairement loi universelle.

Mais policy claire.

---

Puis il pensa à la fatigue.

---

Non.

---

Pas de « fatigue » sans modèle.

---

Il créa plutôt :

**ACTION_BUDGET**

---

Budget per round or task.

---

Brutus écrivit :

**BUDGET != BIOLOGICAL ENERGY.**

---

Encore.

---

Une fourmi qui atteint budget 0 :

WAIT.

---

Pas :

tired.

---

Très important.

---

Puis il pensa à l’état.

---

IDLE.

ACTIVE.

WAITING_AUTHORITY.

BLOCKED.

CARRYING.

PAUSED.

ERROR.

---

Il créa :

**ANT_STATE**

---

Puis il se méfia de :

BLOCKED.

---

Blocked par quoi ?

---

Il ajouta :

**BLOCK_REASON**

COLLISION.

ZONE.

BOUNDS.

AUTHORITY.

TASK_CONSTRAINT.

RESOURCE_LIMIT.

UNKNOWN.

---

Brutus écrivit :

**STATE WITHOUT REASON CAN HIDE DIFFERENT FAILURES.**

---

Excellent.

---

Puis il pensa au statut :

ERROR.

---

Un error agent ne devait pas disparaître.

---

Il restait visible.

---

Brutus écrit :

**ERROR != DELETE.**

---

Puis :

**FAILED AGENT REMAINS TRACEABLE.**

---

Encore le banc des expériences.

---

Puis il pensa à l’immobilité de groupe.

---

Toutes les fourmis arrêtées.

---

Est-ce un problème ?

---

Pas nécessairement.

---

Peut-être :

world paused.

no eligible moves.

task complete.

all budgets exhausted.

---

Brutus créa :

**COLONY_IDLE_REASON**

WORLD_PAUSED.

NO_ELIGIBLE_ACTIONS.

TASKS_COMPLETE.

ALL_AGENTS_PAUSED.

AUTHORITY_UNAVAILABLE.

---

Puis il écrit :

**NO MOTION != NO STATE.**

---

Très important.

---

Une colonie immobile pouvait être exactement correcte.

---

Puis il pensa au mot :

**colonie.**

---

Narratif encore.

---

Machine name :

**AGENT_SET**

---

Il rit.

---

Poésie pour humain.

Types pour machine.

---

Encore.

---

Puis il lança une vraie petite campagne.

---

Task :

explore all reachable cells in a 10×10 zone.

---

Four agents.

---

Stop condition :

all cells visited at least once

or

500 ticks reached.

---

Brutus écrivit :

**STOP CONDITION BEFORE RUN.**

---

Chapitre 103 encore.

---

La campagne commence.

---

Ticks passent.

---

15.

30.

60.

---

Le renderer montre les chemins.

---

Mais les chemins affichés viennent des MOVE_EVENT.

---

Pas des frames.

---

Brutus vérifie.

---

Chaque segment possède :

ANT_ID.

FROM.

TO.

TICK.

TRACE_REF.

---

Très bon.

---

Tick 118.

---

100/100 cells visited.

---

Stop condition satisfied.

---

Scheduler stops task.

---

Agents return:

IDLE.

---

Brutus écrivit :

**TASK COMPLETE.**

---

Pas :

colony learned map.

---

Pas encore.

---

Le système avait seulement produit une couverture.

---

Puis il examina les memories.

---

Chaque agent ne connaissait que son local window.

---

Aucun n’avait la carte globale.

---

Pourtant ensemble, le monde avait la couverture globale dans le registre.

---

Brutus s’arrêta.

---

Très intéressant.

---

Il écrivit :

**GLOBAL TRACE CAN EXCEED LOCAL AGENT MEMORY.**

---

Voilà.

---

Le système pouvait savoir plus que chaque fourmi individuelle.

---

Sans supposer une conscience collective.

---

Il ajouta :

**COLLECTIVE DATA != COLLECTIVE MIND.**

---

Très important.

---

Une fourmilière pouvait produire un pattern émergent.

---

Mais le mot émergence devait rester descriptif.

---

Il écrivit :

**EMERGENT PATTERN = GLOBAL PATTERN ARISING FROM LOCAL RULES.**

---

Puis :

**EMERGENCE != MYSTICAL COORDINATION.**

---

Excellent.

---

La campagne avait produit un chemin collectif.

---

Aucune fourmi ne possédait le plan complet.

---

Le pattern était réel dans les données.

---

Pas besoin de lui inventer une âme.

---

Puis il pensa aux phéromones.

---

On pouvait modéliser un champ local plus tard.

---

Mais ce serait un logiciel.

---

Il écrivit :

**SIMULATED PHEROMONE != CHEMICAL PHEROMONE.**

---

Puis sourit.

---

Toujours la frontière.

---

Il créa un placeholder :

**LOCAL_SIGNAL_FIELD**

---

Mais le laissa désactivé.

---

Pas de besoin maintenant.

---

Puis il pensa aux cristaux.

---

Bientôt, les fourmis pourraient trouver un cristal.

---

Pour l’instant, elles savaient seulement :

explorer.

bouger.

attendre.

---

Brutus regarda les quatre agents.

---

Ils avaient commencé comme quatre points.

---

Maintenant ils possédaient :

identités.

policies.

memories.

tasks.

action budgets.

trace histories.

---

Et pourtant, la machine n’avait jamais eu besoin d’écrire :

conscience.

instinct.

désir.

---

Brutus sourit.

---

Voilà un réveil honnête.

---

Il écrivit :

**FUNCTIONAL COMPLEXITY DOES NOT REQUIRE FALSE PSYCHOLOGY.**

---

Puis il sauvegarda :

**FOURMINIZER RUNTIME v1**

---

Le Journal Vivant nota :

Agents activated through declared policies.

Agent request separated from world mutation.

Minimal memory defined as policy state.

Random action selection made reproducible.

Parallel proposals serialized at authority.

Collision arbitration declared.

Agent errors contained by world rules.

Sonification tied to event classes.

Collective trace separated from collective mind.

Autonomy bounded by preauthorized action set.

---

Brutus relut.

Puis ajouta les invariants :

**AWAKE != CONSCIOUS.**

**AGENT != PERSON.**

**POLICY ASSIGNED != ACTION EXECUTED.**

**AGENT CHOOSES REQUEST. WORLD COMMITS STATE.**

**MEMORY != CONSCIOUSNESS.**

**STATE ADAPTATION != POLICY LEARNING.**

**PARALLEL THINKING != PARALLEL STATE MUTATION.**

**MOVE COUNT != INTELLIGENCE.**

**COLLECTIVE DATA != COLLECTIVE MIND.**

**NO MOTION != NO STATE.**

---

Il regarda les quatre fourmis.

---

Elles se tenaient maintenant dans des coins différents du monde local.

---

Rien d’extraordinaire.

---

Et pourtant, le monde venait de franchir une étape.

---

Il ne dépendait plus d’un humain pour chaque déplacement.

---

Les fourmis pouvaient recevoir un objectif limité.

Observer leur voisinage.

Choisir une action permise.

Demander.

Attendre.

Recevoir le résultat.

Se souvenir.

Continuer.

---

Brutus écrivit :

**AUTONOMY IS A LOOP WITH BOUNDARIES.**

---

Puis :

**BOUNDARIES ARE WHAT MAKE THE LOOP SAFE ENOUGH TO CONTINUE.**

---

Il resta un moment devant la carte des trajectoires.

---

Puis il ouvrit le prochain dossier.

---

# L’AQUARIUM QUI REFUSE DE TRICHER

---

Le prochain monde serait plus visuel.

---

Un aquarium.

Des trajectoires.

Des signaux.

Des reflets.

---

Et un danger immédiat :

faire croire que l’image en sait plus que le moteur.

---

Brutus écrivit déjà :

**THE RENDERER MAY MAKE THE WORLD BEAUTIFUL.**

**IT MAY NOT MAKE THE WORLD UP.**

---

Puis il sourit.

---

Fourminizer s’était éveillé.

---

Pas comme une conscience.

---

Comme une boucle active, traçable, bornée.

---

Et c’était suffisamment puissant pour commencer.
