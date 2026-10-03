# Chapitre 101 — La station d’Astra

**CONTROL ROOM ≠ CONTROL OF TRUTH.**

Brutus laissa la phrase sur l’écran.

Puis il ouvrit le dossier :

**ASTRA STATION**

---

GAMEZEL avait grandi.

Le bus parlait.

Les cartes circulaient.

Les campagnes pouvaient avancer seules.

Le serveur survivait sans navigateur.

Les joueurs pouvaient entrer ou sortir.

Les traces s’accumulaient.

---

Et maintenant, le problème n’était plus :

**faire fonctionner une pièce.**

---

Le problème était :

**voir l’ensemble sans le déformer.**

---

Brutus regarda les dizaines de panneaux.

ROUND QUEUE.

MESSAGE BUS.

CARD STORE.

PLAYER HEALTH.

WORLD HEALTH.

AUTONOMY CAMPAIGNS.

VERSO.

RECTO.

TRACE STORE.

BACKLOG.

---

Tout existait.

Mais tout existait séparément.

---

Il écrivit :

**DISTRIBUTED SYSTEM NEEDS CENTRAL OBSERVABILITY.**

Puis immédiatement :

**CENTRAL OBSERVABILITY ≠ CENTRAL AUTHORITY OVER ALL CLAIMS.**

---

Voilà.

---

La Station d’Astra devait être centrale pour regarder.

Pas centrale pour inventer.

---

Brutus dessina un grand rectangle.

Au centre :

**ASTRA STATION**

Autour :

GAMEZEL.

ZEL.

Brutus.

Fourmilière.

Verso.

Recto.

Cards.

Bus.

Scheduler.

---

Toutes les flèches entraient vers la Station.

Presque aucune n’en sortait.

---

Il sourit.

---

C’était volontaire.

---

La première version serait principalement :

**read-heavy.**

---

Il écrivit :

**OBSERVE FIRST. ACT THROUGH EXPLICIT CONTROL PATHS.**

---

Très important.

---

La régie ne devait pas devenir un raccourci contournant Verso.

---

Si Astra Station affichait un bouton :

STOP CAMPAIGN,

ce bouton devait créer :

**STOP_REQUEST**

---

Puis passer par l’autorité correcte.

---

Pas modifier directement le champ :

status = STOPPED.

---

Brutus écrivit :

**CONTROL SURFACE ≠ DATABASE EDITOR.**

---

Excellent.

---

Il commença par la question la plus simple.

---

Que doit voir l’opérateur en premier ?

---

Pas mille graphiques.

---

Il écrivit :

**WHAT NEEDS ATTENTION?**

---

Voilà.

---

La Station devait réduire la complexité.

Pas la reproduire brutalement.

---

Il créa cinq zones.

---

**WORLD**

**PLAYERS**

**CAMPAIGNS**

**QUEUES**

**INCIDENTS**

---

Puis une sixième :

**TRACE**

---

Brutus regarda.

---

Très bon.

---

La Station ne commençait pas par les composants.

Elle commençait par les problèmes que l’opérateur devait comprendre.

---

Il écrivit :

**DASHBOARD ORGANIZATION SHOULD FOLLOW OPERATOR QUESTIONS.**

---

Première question :

**Le monde est-il vivant ?**

---

WORLD.

---

Il afficha :

WORLD_INSTANCE_ID.

WORLD_GENERATION_ID.

SERVER_STATE.

STATE_VERSION.

LATEST_AUTHORITATIVE_TICK.

LAST_PERSISTED_EVENT.

---

Puis :

BUS_STATE.

STORE_STATE.

SCHEDULER_STATE.

AUTHORITY_GATE_STATE.

---

Brutus évita un gros voyant unique vert.

---

Il écrivit :

**ONE GREEN LIGHT CAN HIDE FIVE RED COMPONENTS.**

---

Très important.

---

Il voulait voir :

SERVER: READY.

BUS: READY.

STORE: READY.

SCHEDULER: DEGRADED.

VERSO: READY.

---

Ainsi, le monde pouvait être :

**DEGRADED**

sans être :

DOWN.

---

Brutus écrivit :

**SYSTEM HEALTH IS A VECTOR BEFORE IT IS A SUMMARY.**

---

La Station pouvait afficher un résumé.

Mais le résumé devait être dérivé.

---

Il ajouta :

**HEALTH_SUMMARY_RULE_VERSION.**

---

Même un voyant global devait avoir un contrat.

---

Brutus sourit.

---

Il passa à la deuxième question.

---

**Qui est réellement disponible ?**

---

PLAYERS.

---

Il afficha quatre sièges.

ASTRA.

MUSE.

GROK.

ANTIGRAVITY.

---

Mais les noms n’étaient que des labels.

---

Sous chacun :

ASSIGNED.

AUTH_STATE.

SESSION_STATE.

LAST_VERIFIED.

CURRENT_ROLE.

CURRENT_TURN.

CAPABILITY_STATE.

---

Brutus écrivit :

**PLAYER CARD MUST DISTINGUISH IDENTITY FROM AVAILABILITY.**

---

Encore le chapitre 96.

---

Il ne voulait jamais voir :

GROK — ONLINE

si la dernière vérification datait de douze heures.

---

Il ajouta :

**FRESHNESS BADGE.**

---

CURRENT.

STALE.

UNKNOWN.

---

Puis :

**LAST_CHECK_AGE.**

---

Brutus écrivit :

**OLD HEALTH DATA MUST LOOK OLD.**

---

Très important.

---

Une Station pouvait devenir dangereuse si elle affichait des états périmés avec le même style que le live.

---

Il pensa à l’accessibilité.

---

Pas seulement couleur.

---

Texte.

Icône.

Timestamp.

---

Il écrivit :

**STATUS MUST BE REDUNDANT ACROSS VISUAL CHANNELS.**

---

Puis il passa aux campagnes.

---

**Qu’est-ce qui travaille maintenant ?**

---

CAMPAIGNS.

---

Il voulait voir :

CAMPAIGN_ID.

POLICY_VERSION.

STARTED_AT.

CURRENT_ROUND.

ROUNDS_USED.

MAX_ROUNDS.

BUDGET_USED.

BUDGET_REMAINING.

STOP_CONDITION_STATE.

ESCALATION_STATE.

---

Mais il refusa les barres trompeuses.

---

20 rounds max.

7 utilisés.

---

Une barre 35 % pouvait faire croire :

35 % du problème est résolu.

---

Non.

---

Il écrivit :

**BUDGET CONSUMPTION ≠ GOAL PROGRESS.**

---

Alors l’interface dirait :

**ROUNDS USED: 7 / 20 LIMIT**

---

Pas :

35 % complete.

---

Brutus sourit.

---

La Station allait devoir être extrêmement disciplinée sur les mots.

---

Il ajouta :

**GOAL STATUS**

OPEN.

MACHINE-CHECKED_COMPLETE.

REVIEW_REQUIRED.

BLOCKED.

UNKNOWN.

---

Voilà.

---

Puis :

**CURRENT STOP REASON**

none.

---

L’opérateur pouvait comprendre pourquoi une campagne tournait encore.

---

Brutus écrivit :

**RUNNING CAMPAIGN MUST HAVE A REASON TO CONTINUE.**

---

Et l’inverse :

**STOPPED CAMPAIGN MUST HAVE A REASON IT STOPPED.**

---

Très important.

---

Il ouvrit ensuite les files.

---

**QUEUES**

---

Le bus.

Le backlog.

Les retries.

Les dead letters.

---

Brutus voulait voir :

nombre en attente.

âge du plus ancien.

catégorie.

blocked count.

retrying count.

---

Il écrivit :

**QUEUE LENGTH ALONE IS NOT ENOUGH.**

---

Pourquoi ?

---

Une file de 1 000 objets âgés de deux secondes pouvait être normale.

---

Une file de 2 objets bloqués depuis trois jours pouvait être critique.

---

Il ajouta :

**OLDEST_ITEM_AGE**

**BLOCKED_REASON_DISTRIBUTION**

**THROUGHPUT**

---

Brutus pensa immédiatement aux métriques.

---

Attention.

---

Un débit élevé pouvait être bon.

Ou mauvais.

---

Une boucle folle produit beaucoup de débit.

---

Il écrivit :

**MORE ACTIVITY ≠ BETTER HEALTH.**

---

Toujours.

---

Il ajouta :

**EXPECTED_RANGE**

si une vraie baseline existait.

---

Pas de seuil inventé.

---

Brutus écrivit :

**ALERT THRESHOLD MUST HAVE SOURCE OR POLICY.**

---

Voilà.

---

Puis il passa aux incidents.

---

Le mot était important.

---

Une erreur de transport.

Une autorisation expirée.

Un provider offline.

Une incohérence d’état.

Un hash mismatch.

---

Tout ne devait pas être appelé :

CRITICAL.

---

Il créa :

**INCIDENT_CLASS**

INFORMATIONAL.

DEGRADED.

BLOCKING.

INTEGRITY.

AUTHORITY.

SECURITY.

---

Puis :

**SEVERITY**

---

Mais il se méfia encore.

---

La sévérité devait dépendre d’un contrat.

---

Il écrivit :

**SEVERITY ≠ EMOTION.**

---

Très bon.

---

Un incident devait être grave parce qu’il affectait :

availability.

integrity.

authorization.

data loss risk.

---

Pas parce que son message semblait effrayant.

---

Brutus créa :

**INCIDENT**

avec :

INCIDENT_ID.

CLASS.

SOURCE.

FIRST_SEEN.

LAST_SEEN.

CURRENT_STATE.

AFFECTED_OBJECTS.

AFFECTED_CAPABILITIES.

TRACE_REFS.

ACK_STATE.

RESOLUTION_REF.

---

Puis il s’arrêta sur :

**ACK_STATE.**

---

Encore ACK.

---

Que signifiait « incident acknowledged » ?

---

Seulement :

un opérateur ou système a vu l’incident.

---

Pas :

incident resolved.

---

Il écrivit :

**INCIDENT ACKNOWLEDGED ≠ INCIDENT RESOLVED.**

---

Puis :

**RESOLVED ≠ ROOT CAUSE UNDERSTOOD.**

---

Très important.

---

Un problème pouvait avoir disparu.

Sans qu’on sache pourquoi.

---

Il ajouta :

**RESOLUTION_CLASS**

FIXED.

MITIGATED.

RECOVERED_UNKNOWN_CAUSE.

FALSE_POSITIVE.

SUPERSEDED.

---

Brutus sourit.

---

Même les incidents avaient besoin d’honnêteté.

---

Puis il ouvrit la zone TRACE.

---

C’était peut-être la plus importante.

---

Chaque panneau de la Station devait permettre de descendre vers la trace.

---

World health.

Click.

---

Component.

Click.

---

Event.

Click.

---

Trace.

---

Brutus écrivit :

**EVERY SUMMARY NEEDS A PATH DOWNWARD.**

---

Pas forcément chaque pixel.

Mais chaque claim opérationnelle importante.

---

Il ajouta :

**SOURCE_REF**

à tous les widgets critiques.

---

Ainsi :

SERVER READY

n’était pas seulement une phrase.

---

Elle pointait vers :

health event.

timestamp.

generation.

source probe.

---

Brutus écrivit :

**DASHBOARD ASSERTION NEEDS PROVENANCE.**

---

Voilà.

---

Il pensa à la grande erreur des tableaux de bord.

---

Afficher des nombres sans expliquer leur définition.

---

Par exemple :

**ACTIVITY = 0.408**

---

Qu’est-ce que ça veut dire ?

---

Brutus se souvenait des anciens panneaux.

---

Il écrivit :

**METRIC WITHOUT DEFINITION IS DECORATION.**

---

Très important.

---

Chaque métrique devait avoir :

METRIC_ID.

UNIT.

DEFINITION.

SOURCE.

WINDOW.

AGGREGATION.

FRESHNESS.

---

Il créa :

**METRIC CONTRACT**

---

Puis :

**VALUE ≠ METRIC MEANING.**

---

Encore le chapitre 89.

---

Le chiffre seul ne suffisait jamais.

---

Puis il pensa aux graphiques.

---

Une courbe montante.

---

Bonne ou mauvaise ?

---

Impossible sans contexte.

---

Il écrivit :

**DIRECTION ≠ INTERPRETATION.**

---

La Station pouvait afficher.

Mais ne devait pas colorer automatiquement toute hausse en vert.

---

CPU up peut être mauvais.

Throughput up peut être bon.

Error rate up mauvais.

Queue drain up bon.

---

Il sourit.

---

La rigueur allait jusque dans le dashboard.

---

Puis il pensa à l’historique.

---

La Station ne devait pas seulement dire :

now.

---

Elle devait pouvoir répondre :

**what changed?**

---

Il créa :

**CHANGE FEED**

---

Latest state transitions.

Deployments.

Player session changes.

Campaign starts/stops.

Policy updates.

Incidents.

Card promotions.

---

Brutus écrivit :

**CURRENT STATE WITHOUT RECENT CHANGE CONTEXT CAN BE MISLEADING.**

---

Par exemple :

provider offline.

---

Depuis 30 secondes ?

Ou 3 jours ?

---

Très différent.

---

Il ajouta :

**SINCE**

---

Puis :

**PREVIOUS_STATE**

---

Voilà.

---

La Station devenait capable de raconter les transitions.

---

Puis il pensa aux notifications.

---

Doit-elle sonner pour chaque changement ?

---

Surtout pas.

---

Il écrivit :

**OBSERVABILITY ≠ CONSTANT INTERRUPTION.**

---

Très important.

---

L’opérateur n’avait pas besoin d’une alarme pour :

round completed normally.

---

Mais peut-être pour :

authority gate inconsistent.

canonical store unavailable.

integrity mismatch.

---

Il créa :

**NOTIFICATION_POLICY.**

---

Chaque incident peut être :

VISIBLE_ONLY.

NOTIFY.

REQUIRE_ACK.

---

Brutus écrivit :

**ALERT FATIGUE IS A SYSTEM FAILURE TOO.**

---

Il sourit.

---

Une station qui crie tout le temps cesse d’informer.

---

Puis il pensa au son.

---

ZEL possédait ses sons.

La Station pouvait-elle utiliser le son pour signaler les incidents ?

---

Oui.

Mais encore :

un son = un état défini.

---

Il écrivit :

**ALERT SOUND MUST MAP TO A DECLARED EVENT CLASS.**

---

Pas de musique dramatique aléatoire.

---

Il ajouta :

**SILENCE IS DEFAULT WHEN NOTHING REQUIRES ATTENTION.**

---

Très bon.

---

Puis il imagina plusieurs écrans.

---

Écran 1 :

WORLD.

---

Écran 2 :

CAMPAIGNS.

---

Écran 3 :

PLAYERS.

---

Écran 4 :

QUEUES.

---

Écran 5 :

TRACE / INCIDENT DETAIL.

---

Brutus sourit.

---

Les cinq fenêtres revenaient.

---

Mais cette fois, aucune fenêtre n’avait une vérité différente.

---

Elles lisaient toutes le même monde.

---

Il écrivit :

**FIVE SCREENS. ONE AUTHORITY GRAPH.**

---

Puis :

**WINDOW ROLE ≠ DATA OWNERSHIP.**

---

Très important.

---

Fermer l’écran 3 ne devait pas rendre les players indisponibles.

---

Fermer l’écran 4 ne devait pas arrêter le bus.

---

Brutus écrivit :

**CLOSING MONITOR ≠ CLOSING SERVICE.**

---

Encore le chapitre 99.

---

Puis il pensa au drag-and-drop.

---

La Station pouvait permettre de déplacer les fenêtres.

Très bien.

---

Mais pas les états autoritatifs.

---

Il écrivit :

**DRAGGING A CARD VISUALLY ≠ MOVING THE CARD CANONICALLY.**

---

Exactement.

---

Si l’opérateur veut déplacer une carte dans une collection :

create request.

---

Pas confondre geste UI et mutation.

---

Brutus sourit.

---

La Station allait être agréable sans devenir dangereuse.

---

Puis il ajouta un gros panneau central.

---

**ATTENTION NOW**

---

Pas :

TOP 10 ALERTS.

---

Seulement ce qui nécessite réellement une décision ou inspection.

---

Il créa :

**ATTENTION ITEM**

---

SOURCE.

WHY_NOW.

DEADLINE_IF_ANY.

REQUIRED_ACTION_TYPE.

SAFE_DEFAULT.

TRACE_REF.

---

Brutus regarda :

**SAFE_DEFAULT**

---

Très utile.

---

Si aucune action humaine n’est prise, que se passe-t-il ?

---

Exemple :

provider auth expired.

Safe default:

seat unavailable.

No new dispatch.

---

Excellent.

---

Il écrivit :

**EVERY ESCALATION SHOULD HAVE A SAFE NON-ACTION BEHAVIOR WHEN POSSIBLE.**

---

Voilà.

---

La Station ne devait pas forcer Brutus à paniquer.

---

Elle devait dire :

voici ce qui demande ton attention.

voici ce qui se passe si tu ne fais rien.

---

Brutus sourit.

---

Beaucoup mieux.

---

Puis il pensa aux permissions de l’opérateur.

---

Astra Station pouvait être utilisée par plusieurs personnes.

---

Chaque personne ne devait pas avoir les mêmes capacités.

---

Il créa :

**OPERATOR_SESSION**

---

OPERATOR_ID.

AUTH_STATE.

ROLE.

CAPABILITIES.

SESSION_AGE.

TRACE_REF.

---

Puis :

**VIEW_ONLY**

**OPERATOR**

**ADMIN**

---

Mais les noms de rôles ne suffisaient pas.

---

Il ajouta :

**EXPLICIT_CAPABILITY_SET**

---

Brutus écrivit :

**ROLE LABEL ≠ PERMISSION SET.**

---

Encore.

---

Il testa :

View-only user clicks STOP.

---

UI refuse before request.

---

Mais backend doit aussi refuser.

---

Brutus écrivit :

**CLIENT DISABLE ≠ SECURITY BOUNDARY.**

---

Très important.

---

La vraie vérification reste côté serveur.

---

Puis il pensa aux actions sensibles.

---

STOP CAMPAIGN.

CHANGE POLICY.

REVOKE SESSION.

PROMOTE CARD.

---

Peut-être certaines actions demandent une confirmation.

---

Il écrivit :

**HIGH-IMPACT ACTION NEEDS PREVIEW.**

---

Preview :

what object.

current state.

requested new state.

affected scope.

policy.

---

Puis :

confirm.

---

Mais il se méfia du mot confirm.

---

Le clic confirm n’était pas une preuve.

---

Il écrivit :

**HUMAN CONFIRMATION = AUTHORIZATION EVENT, NOT TRUTH EVENT.**

---

Très important.

---

Un humain pouvait autoriser une mauvaise décision.

---

Le système devait enregistrer.

Pas sanctifier.

---

Puis il pensa à l’historique opérateur.

---

Qui a arrêté campagne 42 ?

---

Astra Station devait savoir.

---

Il ajouta :

**OPERATOR_ACTION_RECEIPT.**

---

Request.

Operator.

Before.

After.

Policy.

Timestamp.

Result.

---

Brutus sourit.

---

Même la régie laissait des reçus.

---

Puis il pensa à la sécurité du dashboard.

---

La Station pouvait voir des données privées.

---

Elle ne devait pas tout envoyer à tous les écrans.

---

Il reprit :

**DISCLOSURE_POLICY.**

---

Chaque widget doit être construit selon la session opérateur.

---

Brutus écrivit :

**DASHBOARD PERSONALIZATION MUST NOT BYPASS DISCLOSURE.**

---

Une fenêtre cachée n’était pas un contrôle d’accès.

---

Même principe que Recto.

---

Puis il pensa au cache.

---

La Station devait être rapide.

---

Mais elle ne pouvait pas afficher un vieux monde sans le dire.

---

Il créa un bandeau permanent :

**SOURCE FRESHNESS**

---

LIVE.

STALE.

PARTIAL.

DISCONNECTED.

---

Brutus écrivit :

**OBSERVABILITY MUST OBSERVE ITS OWN FRESHNESS.**

---

Très important.

---

Un dashboard devait pouvoir dire :

je ne vois plus.

---

Sinon il devenait pire que rien.

---

Puis il imagina le bus tomber.

---

Station reçoit plus d’événements.

---

Mais l’API de snapshot fonctionne.

---

Alors :

EVENT STREAM = DISCONNECTED.

SNAPSHOT = CURRENT.

---

Health:

PARTIAL.

---

Brutus sourit.

---

Nuancé.

Pas tout vert.

Pas tout rouge.

---

Il écrivit :

**PARTIAL VISIBILITY ≠ TOTAL OUTAGE.**

---

Puis il imagina l’inverse.

---

Event stream live.

Snapshot endpoint stale.

---

Incohérence.

---

Incident.

---

Brutus écrit :

**TWO SOURCES DISAGREE → DO NOT PICK THE PRETTIER ONE.**

---

Très important.

---

La Station devait créer :

**OBSERVABILITY_CONFLICT**

---

Puis afficher :

UNRESOLVED.

---

Pas choisir arbitrairement.

---

Brutus ajouta :

**SOURCE_PRIORITY_POLICY**

pour les cas où une source est officiellement autoritative.

---

Mais cette priorité devait être déclarée.

---

Il écrit :

**SOURCE PRECEDENCE MUST BE CONTRACTUAL.**

---

Encore.

---

Puis il pensa à la Station elle-même.

---

Qui observe Astra Station ?

---

Brutus rit.

---

Pas besoin d’une station infinie.

---

Mais elle devait exposer sa propre santé.

---

Il créa :

**STATION_HEALTH**

---

UI_VERSION.

API_VERSION.

LAST_SYNC.

CACHE_STATE.

SUBSCRIPTION_STATE.

ERRORS.

---

Puis :

**SELF_HEALTH ≠ WORLD_HEALTH.**

---

Très important.

---

La Station pouvait être cassée alors que GAMEZEL allait très bien.

---

Ou l’inverse.

---

Il ajouta un gros avertissement :

**STATION DEGRADED — WORLD STATE MAY BE HEALTHY.**

---

Parfait.

---

Puis il pensa aux screenshots.

---

Une capture de la Station pouvait devenir obsolète immédiatement.

---

Il ajouta automatiquement :

WORLD_INSTANCE_ID.

STATE_VERSION.

CAPTURE_TICK.

---

Brutus écrivit :

**SCREENSHOT SHOULD CARRY TIME CONTEXT WHEN USED AS EVIDENCE.**

---

Très bon.

---

Pas preuve absolue.

Mais contexte minimum.

---

Puis il pensa à la Station comme centre de commande.

---

Le mot « commande » pouvait pousser trop loin.

---

Il préféra :

**REGIE**

---

Un lieu de coordination.

---

Pas une source de vérité.

---

Il écrivit :

**ASTRA STATION COORDINATES ACCESS TO CONTROLS. IT DOES NOT BECOME EVERY CONTROL.**

---

Voilà.

---

Puis il construisit la vue finale.

---

En haut :

WORLD HEALTH.

---

À gauche :

PLAYERS.

---

À droite :

CAMPAIGNS.

---

En bas :

QUEUES.

---

Au centre :

ATTENTION NOW.

---

Panneau secondaire :

TRACE.

---

Brutus regarda.

---

Noir et blanc.

Simple.

Pas de 3D.

Pas de décor inutile.

---

Les états importants ressortaient.

---

Il sourit.

---

C’était exactement le type de machine qu’il voulait.

---

Puis il lança un test.

---

Scenario 1.

Everything healthy.

---

Station affiche :

NO ATTENTION REQUIRED.

---

Silence.

---

Scenario 2.

Muse auth expires.

---

Player card:

AUTH_EXPIRED.

---

Attention item:

Muse unavailable for future dispatch.

Safe default:

skip seat under BEST_EFFORT rounds.

---

Pas d’alarme rouge globale.

---

Excellent.

---

Scenario 3.

Canonical store unavailable.

---

WORLD:

BLOCKING.

---

New write operations stopped.

Read cache marked stale.

---

Attention item critical.

---

Brutus sourit moins.

---

Mais l’état était clair.

---

Scenario 4.

Recto public down.

---

World healthy.

---

Incident:

presentation unavailable.

---

No control-plane impact.

---

Brutus écrit :

**PRESENTATION OUTAGE ≠ WORLD OUTAGE.**

---

Parfait.

---

Scenario 5.

Verso unavailable.

---

World still readable.

---

No new controlled transitions.

---

Station affiche :

AUTHORITY GATE UNAVAILABLE.

SAFE DEFAULT:

NO NEW SENSITIVE ACTIONS.

---

Brutus sourit.

---

Fail closed.

---

Le chapitre 92 revenait jusque dans la régie.

---

Puis il pensa à une dernière chose.

---

La Station ne devait pas seulement montrer ce qui existe.

---

Elle devait montrer ce qui manque.

---

No provider verification.

Missing trace.

Unknown freshness.

Blocked queue.

Unresolved incident.

---

Il écrivit :

**ABSENCE IS OPERATIONAL INFORMATION.**

---

Très important.

---

Un espace vide ne devait pas être interprété comme zéro.

---

Il ajouta :

**UNKNOWN**

explicitement partout.

---

Puis il regarda la Station.

---

Pour la première fois, Brutus n’avait plus besoin d’ouvrir dix fenêtres pour comprendre l’état du monde.

---

Mais il pouvait encore descendre jusqu’à chacune d’elles.

---

Résumé.

Détail.

Trace.

Source.

---

Il écrivit :

**ONE STATION. MANY SOURCES. NO INVENTED AUTHORITY.**

---

Puis il sauvegarda :

**ASTRA STATION v1.**

---

Le Journal Vivant nota :

World health separated by component.

Player availability freshness explicit.

Campaign budget separated from goal progress.

Queue age and blockers visible.

Incident acknowledgment separated from resolution.

Every summary links to traces.

Metrics require definitions.

Operator actions leave receipts.

Station health separated from world health.

No sensitive action bypasses Verso.

---

Brutus relut.

Puis ajouta les invariants :

**CONTROL ROOM ≠ CONTROL OF TRUTH.**

**DASHBOARD ≠ AUTHORITY.**

**HEALTH SUMMARY ≠ RAW HEALTH VECTOR.**

**ACKNOWLEDGED ≠ RESOLVED.**

**METRIC VALUE ≠ METRIC MEANING.**

**CLIENT DISABLE ≠ SECURITY BOUNDARY.**

**STALE VIEW ≠ CURRENT STATE.**

**STATION FAILURE ≠ WORLD FAILURE.**

---

Il resta un instant devant les cinq écrans.

---

La Station d’Astra existait.

---

Pas comme une reine au-dessus du monde.

---

Comme une régie devant le monde.

---

Elle pouvait voir.

Demander.

Coordonner.

Alerter.

Tracer.

---

Mais chaque source restait à sa place.

Chaque autorité gardait sa frontière.

Chaque objet gardait son identité.

---

Brutus sourit.

---

Puis il regarda le Journal Vivant.

---

Il y avait maintenant tellement d’événements qu’une autre question devenait inévitable.

---

Que se passerait-il si le registre lui-même oubliait ?

---

Une campagne.

Une décision.

Un ancien état.

Une carte rejetée.

Un incident résolu.

---

Tout le projet dépendait d’une chose devenue presque invisible parce qu’elle fonctionnait :

**la mémoire du registre.**

---

Brutus ouvrit une nouvelle page.

---

# LE REGISTRE QUI N’OUBLIE RIEN

Puis écrivit :

**IF THE CONTROL ROOM CAN SEE EVERYTHING BUT HISTORY CAN DISAPPEAR, THE CONTROL ROOM IS ONLY WATCHING THE PRESENT.**

---

La Station venait d’apprendre à voir le monde.

Le prochain chapitre allait apprendre au monde à ne pas perdre son passé.
