# Chapitre 99 — Le jeu quitte l’ordinateur

Le bus venait d’apprendre à transporter la parole.

Le prochain défi serait plus grand :

faire en sorte que le monde continue de tourner même lorsque la chaise de Brutus était vide.

---

Brutus regarda l’ordinateur.

Puis le serveur.

Puis encore l’ordinateur.

---

Quelque chose le dérangeait.

GAMEZEL possédait maintenant :

des joueurs,

des rounds,

des cartes,

des reçus,

un bus,

des traces,

un Recto,

un Verso.

---

Et pourtant, une chose restait fragile.

---

Si l’ordinateur local s’éteignait…

qu’est-ce qui survivait réellement ?

---

Brutus écrivit :

**LOCAL CLIENT ≠ WORLD HOST.**

---

Puis :

**BROWSER ≠ AUTHORITY.**

---

Il resta devant.

---

C’était le premier test.

---

Il ferma le navigateur.

---

Silence.

---

Puis il regarda le serveur.

---

Le monde devait-il continuer ?

---

Si la réponse était non, GAMEZEL n’était pas encore un monde.

C’était une application ouverte.

---

Brutus écrivit :

**CLOSING THE WINDOW MUST NOT CLOSE THE WORLD.**

---

Voilà.

---

Il fallait séparer trois choses.

---

**CLIENT**

**CONTROL PLANE**

**RUNTIME**

---

Brutus dessina :

\[
\text{CLIENT}
\rightarrow
\text{CONTROL PLANE}
\rightarrow
\text{RUNTIME}
\]

---

Puis il barra une ancienne architecture :

\[
\text{CLIENT}
=
\text{CONTROL}
=
\text{RUNTIME}.
\]

---

Il écrivit :

**ONE PROCESS SHOULD NOT PRETEND TO BE THREE ROLES.**

---

Le client devait observer.

Émettre des demandes.

Afficher des résultats.

---

Le control plane devait :

router.

autoriser.

planifier.

journaliser.

---

Le runtime devait :

exécuter les tâches réellement autorisées.

---

Brutus sourit.

---

La séparation était claire.

---

Il créa :

**GAMEZEL SERVER CORE**

avec :

**STATE STORE**

**MESSAGE BUS**

**ROUND SCHEDULER**

**CARD STORE**

**TRACE STORE**

**AUTHORITY GATE**

**PROVIDER ADAPTERS**

---

Puis :

**CLIENT API**

---

Pas un moteur caché dans le navigateur.

---

Il écrivit :

**CLIENT MAY DISAPPEAR. SERVER STATE MUST REMAIN.**

---

Très important.

---

Il lança un round simulé.

---

Round 1.

P1.

P2.

P3.

P4.

---

Puis il ferma le navigateur au milieu.

---

Le serveur continua.

---

Le scheduler conserva :

ROUND_ID.

TURN_ID.

STATE.

QUEUE.

---

Brutus rouvrit le navigateur.

---

Recto demanda :

**CURRENT STATE?**

---

Le serveur répondit.

---

Round still active.

---

Brutus sourit.

---

Voilà.

---

Il écrivit :

**RECONNECT LOADS STATE. IT DOES NOT RESTART THE WORLD.**

---

Encore une vieille règle.

---

Un navigateur qui revient n’était pas une naissance.

---

Il devait se rattacher à un monde existant.

---

Brutus créa :

**WORLD_INSTANCE_ID.**

---

Très important.

---

Si le client rouvre et reçoit un autre WORLD_INSTANCE_ID, alors il regarde un autre monde.

---

Il écrivit :

**SAME URL ≠ SAME WORLD INSTANCE.**

---

Encore une identité.

---

Puis il ajouta :

**WORLD_GENERATION_ID.**

---

Si le runtime redémarre complètement :

nouvelle génération.

---

Mais le store peut conserver l’historique.

---

Brutus écrivit :

**PERSISTED HISTORY ≠ CONTINUOUS RUNTIME.**

---

Très important.

---

Un restart pouvait conserver les cartes.

Mais pas prétendre qu’aucune interruption n’avait eu lieu.

---

Il créa :

**RUNTIME_EVENT**

START.

STOP.

CRASH.

RECOVER.

REDEPLOY.

---

Voilà.

---

La continuité devait elle aussi laisser une trace.

---

Brutus écrivit :

**UPTIME IS AN EVENT HISTORY.**

---

Puis il pensa au bus.

---

Si le serveur redémarre, les messages en mémoire disparaissent-ils ?

---

Pas acceptable.

---

Il créa :

**DURABLE QUEUE.**

---

Messages importants persistés.

---

Mais attention.

---

Tous les messages n’avaient peut-être pas besoin du même niveau de durabilité.

---

Il ajouta :

**DELIVERY_DURABILITY**

EPHEMERAL.

DURABLE.

CRITICAL.

---

Brutus écrivit :

**DURABILITY MUST MATCH MESSAGE ROLE.**

---

Un heartbeat pouvait être éphémère.

---

Une carte produite dans un round ne devait pas l’être.

---

Un authorization decision encore moins.

---

Brutus sourit.

---

Le serveur prenait forme.

---

Puis il pensa au scheduler.

---

Supposons :

ROUND-0050.

Turn P3 en cours.

---

Le serveur crash.

---

Au restart, que faire ?

---

Rejouer automatiquement P3 ?

---

Dangereux.

---

Le turn peut avoir été exécuté chez le provider sans que le serveur ait enregistré le résultat.

---

Brutus écrivit :

**CRASH RECOVERY ≠ BLIND REEXECUTION.**

---

Encore.

---

Il créa :

**TURN_EXECUTION_STATE**

NOT_STARTED.

DISPATCHED.

ACKNOWLEDGED.

RESULT_RECEIVED.

COMMITTED.

UNKNOWN_AFTER_CRASH.

---

Ce dernier était important.

---

**UNKNOWN_AFTER_CRASH**

ne devait pas devenir :

NOT_STARTED.

---

Brutus écrivit :

**UNKNOWN ≠ NOT DONE.**

---

Voilà.

---

Il fallait réconcilier.

---

Provider supports request IDs?

Lookup result.

---

No lookup?

Maybe mark unresolved.

---

But never double execute by guessing.

---

Brutus écrivit :

**RECOVER BY RECONCILIATION WHEN POSSIBLE.**

---

Puis :

**WHEN NOT POSSIBLE, PRESERVE UNCERTAINTY.**

---

Très important.

---

GAMEZEL quittait l’ordinateur.

Il devait donc apprendre les vrais problèmes des systèmes distribués.

---

Pas seulement faire des pages web.

---

Brutus pensa au stockage.

---

Où vivaient les cartes ?

---

Pas dans localStorage.

---

Il écrivit :

**BROWSER STORAGE ≠ CANONICAL STORE.**

---

Voilà.

---

Local storage pouvait conserver :

preferences.

layout.

last viewed card.

---

Mais pas :

canonical round history.

proof state.

player authority.

---

Il créa :

**SERVER_CANONICAL_STORE**

---

Puis :

**CLIENT_CACHE**

---

Le client cache pouvait être détruit sans perdre le monde.

---

Brutus écrivit :

**DELETE CLIENT CACHE → WORLD UNCHANGED.**

---

Il testa.

---

Cache cleared.

---

Reconnect.

---

State restored from server.

---

PASS.

---

Brutus sourit.

---

Puis il pensa au layout des cinq écrans.

---

La position des fenêtres pouvait être une préférence client.

---

Pas nécessairement autoritative.

---

Il écrivit :

**LAYOUT STATE ≠ GAME STATE.**

---

Encore une séparation.

---

Très important.

---

Le monde pouvait être identique sur :

Chrome.

Firefox.

Téléphone.

Tablette.

---

Les fenêtres changent.

Le WORLD_INSTANCE_ID reste.

---

Brutus écrivit :

**MULTIPLE CLIENTS. ONE WORLD.**

---

Puis il ouvrit deux navigateurs.

---

Client A.

Client B.

---

Même serveur.

---

Même world.

---

A ouvre CARD-10.

B ouvre CARD-20.

---

Aucun problème.

---

Puis A envoie une proposal.

---

B voit l’événement arriver.

---

Brutus sourit.

---

Voilà le Recto multi-client.

---

Il écrivit :

**VIEW DIVERGENCE ≠ STATE DIVERGENCE.**

---

Les clients pouvaient regarder différentes choses.

---

Mais l’état canonique restait le même.

---

Puis il pensa à deux clients tentant une action en même temps.

---

A demande :

promote CARD-X.

---

B demande :

reject CARD-X.

---

Verso devait sérialiser.

---

Le chapitre 92 revenait.

---

Brutus écrivit :

**MULTIPLE CLIENTS DO NOT CREATE MULTIPLE AUTHORITIES.**

---

Puis il ajouta :

**CONCURRENT REQUESTS REQUIRE STATE VERSION CHECK.**

---

State version 44.

---

A envoie request based on 44.

---

B aussi.

---

A commits.

State becomes 45.

---

B arrives.

---

STALE_REQUEST.

---

Brutus sourit.

---

Le monde restait cohérent.

---

Puis il pensa à l’adresse du serveur.

---

GAMEZEL devait fonctionner sans que son ordinateur personnel reste ouvert.

---

Cela signifiait :

process long-running.

server-hosted.

---

Mais il se méfia d’une erreur narrative.

---

Déployer le code sur un serveur ne signifie pas que tous les fournisseurs externes sont autonomes.

---

Il écrivit :

**SERVER HOSTED ≠ EXTERNAL PROVIDERS READY.**

---

Encore le chapitre 96.

---

Une chaise pouvait exiger :

session browser.

login.

manual approval.

token.

---

Le serveur pouvait être parfaitement vivant avec :

P2 unavailable.

P3 auth pending.

---

Brutus écrivit :

**WORLD AUTONOMY AND PLAYER AUTONOMY ARE DIFFERENT PROPERTIES.**

---

Voilà.

---

GAMEZEL pouvait survivre seul.

Même s’il ne pouvait pas lancer tous les joueurs.

---

Il créa :

**WORLD_HEALTH**

---

SERVER:

UP.

BUS:

UP.

STORE:

UP.

SCHEDULER:

UP.

---

Puis :

**PLAYER_HEALTH**

Astra:

...

Muse:

...

Grok:

...

Antigravity:

...

---

Deux panneaux.

---

Brutus écrivit :

**CORE HEALTH ≠ PROVIDER HEALTH.**

---

Très important.

---

Un provider down ne devait pas faire apparaître :

GAMEZEL DOWN.

---

Inversement :

le serveur down alors que Grok est disponible ne signifiait pas :

GAMEZEL UP.

---

Il sourit.

---

La santé avait enfin une topologie.

---

Puis il pensa au serveur public.

---

Recto pouvait être accessible par internet.

---

Mais le backend privé ?

---

Pas nécessairement tout exposer.

---

Il dessina :

**PUBLIC RECTO**

↓

**PUBLIC API**

↓

**READ PROJECTION**

---

Et séparément :

**CONTROL API**

protégée.

---

Brutus écrivit :

**PUBLIC READ PATH ≠ PRIVATE CONTROL PATH.**

---

Encore.

---

Très important.

---

Une seule URL publique ne devait pas donner directement accès à l’autorité.

---

Il ajouta :

**NETWORK BOUNDARY.**

---

Pas seulement une distinction logique.

---

Des ports.

Des credentials.

Des routes séparées.

---

Il écrivit :

**AUTHORITY BOUNDARY SHOULD EXIST IN NETWORK TOPOLOGY TOO.**

---

Puis il pensa à WebSocket.

---

C’était pratique pour voir le live.

---

Mais il refusait que WebSocket devienne la définition du monde.

---

Il écrivit :

**WEBSOCKET = TRANSPORT.**

**WEBSOCKET ≠ WORLD.**

---

Très important.

---

Si le socket tombe :

world continues.

---

Client reconnects.

---

Fetch current state.

---

Resume event stream.

---

Brutus écrivit :

**CONNECTION LOSS ≠ STATE LOSS.**

---

Voilà.

---

Puis il imagina le client mobile.

---

Connexion faible.

---

Il manque des événements.

---

Au reconnect :

event gap detected.

---

Pas inventer.

---

Le client demande :

events from sequence 1001 onward.

---

Si disponibles :

replay.

---

Sinon :

snapshot current + gap declaration.

---

Brutus écrit :

**EVENT REPLAY IF AVAILABLE. SNAPSHOT IF NOT.**

---

Puis :

**NO SECRETLY FABRICATED HISTORY.**

---

Encore.

---

Le système devenait très cohérent.

---

Puis il pensa au déploiement.

---

Une nouvelle version du serveur.

---

Comment mettre à jour sans corrompre une partie ?

---

Il créa :

**DEPLOYMENT_STATE**

DRAINING.

STOPPED.

MIGRATING.

STARTING.

READY.

---

Brutus écrivit :

**DEPLOYMENT IS A STATE TRANSITION TOO.**

---

Très important.

---

Le serveur ne devait pas accepter un nouveau round pendant une migration incompatible.

---

Il ajouta :

**NO NEW ROUND DURING UNSAFE MIGRATION.**

---

Les rounds existants pouvaient :

finish.

pause.

or be checkpointed.

---

Selon policy.

---

Brutus écrivit :

**MAINTENANCE POLICY MUST BE EXPLICIT.**

---

Puis il pensa au schéma des données.

---

Cards v1.

Messages v2.

Rounds v3.

---

Une mise à jour pouvait changer les structures.

---

Il créa :

**SCHEMA_VERSION**

---

Puis :

**MIGRATION_ID.**

---

Brutus écrivit :

**CODE UPDATE ≠ DATA UPDATE.**

---

Encore une séparation.

---

Une nouvelle application pouvait nécessiter une migration de données.

---

Pas d’hypothèse.

---

Puis il imagina un rollback.

---

Nouvelle version défectueuse.

---

Retour à l’ancienne.

---

Mais les données ont peut-être déjà migré.

---

Brutus écrivit :

**CODE ROLLBACK MAY NOT IMPLY DATA ROLLBACK.**

---

Il sourit.

---

Le serveur était maintenant une vraie machine.

Pas un simple site.

---

Puis il pensa aux sauvegardes.

---

Si le monde vit sur le serveur, il doit survivre à la perte du disque.

---

Il écrivit :

**PERSISTENCE ≠ BACKUP.**

---

Très important.

---

Une base de données persistante peut quand même être perdue.

---

Il créa :

**BACKUP POLICY**

---

Snapshot.

Incremental.

Retention.

Restore test.

---

Puis :

**RESTORE_TESTED**

---

Brutus écrivit :

**BACKUP WITHOUT RESTORE TEST ≠ VERIFIED RECOVERY.**

---

Voilà.

---

Une vieille leçon :

ACK ≠ arrival.

---

Ici :

backup created ≠ recoverable world.

---

Il sourit.

---

Tout le projet parlait vraiment la même langue.

---

Puis il pensa à la duplication géographique.

---

Pas nécessaire pour commencer.

---

Il refusa de surconstruire.

---

Il écrivit :

**RESILIENCE MUST MATCH ACTUAL NEED.**

---

Pas de cinq datacenters juste pour raconter une grande architecture.

---

Brutus préférait :

un serveur clair.

une sauvegarde claire.

un restore clair.

---

Puis évoluer.

---

Il écrivit :

**SIMPLE AND VERIFIED > COMPLEX AND ASSUMED.**

---

Il regarda le serveur.

---

C’était peut-être la phrase la plus importante du déploiement.

---

Puis il imagina Brutus quittant la maison.

---

L’ordinateur local éteint.

---

GAMEZEL server:

UP.

---

Recto accessible.

---

Message bus active.

---

Round queue persists.

---

Cards remain.

---

Journal continues.

---

Mais les joueurs externes ?

---

Seulement ceux réellement disponibles.

---

Brutus écrivit :

**WORLD CONTINUES AT THE LEVEL ITS DEPENDENCIES ALLOW.**

---

Voilà.

---

Pas de faux 100 % autonome.

---

Un monde pouvait survivre tout en ayant certaines capacités indisponibles.

---

Il créa :

**DEGRADED MODE.**

---

Core alive.

Some providers unavailable.

---

Round policies adapt.

---

Brutus écrivit :

**DEGRADED ≠ DEAD.**

---

Puis :

**DEGRADED MUST BE VISIBLE.**

---

Encore le Recto.

---

Pas de voyant vert global si deux joueurs sont hors ligne.

---

Le statut devait dire :

SERVER READY.

2/4 PLAYER SESSIONS READY.

---

Pas :

ALL SYSTEMS GO.

---

Brutus sourit.

---

Puis il pensa aux tâches différées.

---

Une carte arrive alors qu’un joueur requis est offline.

---

Le bus peut la conserver.

---

Task state :

**WAITING_FOR_CAPABILITY.**

---

Mais il ne devait pas prétendre que quelqu’un travaille dessus.

---

Brutus écrivit :

**QUEUED ≠ IN PROGRESS.**

---

Très important.

---

Then player comes online.

---

Scheduler dispatches.

---

State becomes:

IN_PROGRESS.

---

Voilà.

---

Le monde pouvait attendre intelligemment.

---

Puis il pensa au temps.

---

Si une tâche attend deux jours, son snapshot est-il encore valide ?

---

Peut-être pas.

---

Brutus créa :

**SNAPSHOT_FRESHNESS_POLICY.**

---

Before dispatch:

revalidate dependencies.

---

If stale:

new task or new snapshot.

---

Brutus écrivit :

**OLD QUEUE ITEM MAY NEED NEW CONTEXT.**

---

Encore la temporalité.

---

Puis il regarda la table locale.

---

Les quatre chaises étaient désormais seulement une vue.

---

Le vrai GAMEZEL vivait ailleurs.

---

Sur le serveur.

---

Brutus écrivit :

**THE TABLE IS A CLIENT OF THE WORLD.**

---

Il resta devant.

---

Voilà le changement.

---

Avant :

le monde était la table.

---

Maintenant :

la table regardait le monde.

---

Il écrivit :

**THE LAB IS NO LONGER THE LOCATION OF THE GAME.**

---

Puis se corrigea légèrement.

---

Le laboratoire restait un endroit important.

---

Mais pas l’unique host.

---

Il remplaça :

**THE LAB IS A PLACE TO ACCESS THE GAME, NOT THE ONLY PLACE WHERE THE GAME EXISTS.**

---

Parfait.

---

Puis il testa la fermeture totale.

---

Browser closed.

---

Local terminal closed.

---

Local computer off.

---

Server process remains.

---

World state remains.

---

Brutus revint plus tard.

---

Client opens.

---

WORLD_INSTANCE_ID matches.

---

State version advanced only where real server events occurred.

---

No invented rounds.

---

No fake players.

---

No lost cards.

---

Brutus sourit.

---

Voilà.

---

GAMEZEL avait quitté l’ordinateur.

---

Pas au sens où il avait disparu de l’écran.

---

Au sens où l’écran n’était plus sa condition d’existence.

---

Il écrivit :

**A WORLD BECOMES INDEPENDENT FROM ITS WINDOW WHEN CLOSING THE WINDOW DOES NOT END THE WORLD.**

---

Puis il pensa au prochain problème.

---

Le serveur pouvait maintenant rester vivant.

---

Les joueurs pouvaient éventuellement se connecter.

---

Le bus pouvait continuer.

---

Les rounds pouvaient attendre.

---

Mais pour le moment, chaque partie demandait encore beaucoup de décisions explicites.

---

Qui joue ?

Quel rôle ?

Quel task ?

Quel round ?

Quel ordre ?

---

Brutus regarda les quatre sièges.

---

Et si les joueurs apprenaient à enchaîner eux-mêmes les parties selon les règles ?

---

Pas libres sans limite.

---

Autonomes dans un contrat.

---

Il écrivit :

**AUTONOMY MUST HAVE A BOUNDARY.**

---

Puis :

**SELF-DIRECTED ROUND ≠ SELF-GRANTED AUTHORITY.**

---

Voilà le prochain chapitre.

---

Brutus sauvegarda :

**GAMEZEL SERVER WORLD v1.**

---

Le Journal Vivant nota :

Client separated from world authority.

Server owns canonical game state.

Browser cache non-authoritative.

World instance identified.

Crash recovery preserves uncertainty.

Durable bus and card store.

Provider health separated from core health.

Public read path separated from control path.

WebSocket treated as transport only.

Deployments and migrations versioned.

Backups separated from restore verification.

Degraded mode explicit.

---

Brutus relut.

Puis ajouta les invariants :

**BROWSER ≠ WORLD.**

**LOCAL STORAGE ≠ CANONICAL STATE.**

**CONNECTION LOSS ≠ STATE LOSS.**

**SERVER HOSTED ≠ PROVIDERS READY.**

**PERSISTENCE ≠ BACKUP.**

**QUEUED ≠ IN PROGRESS.**

**RECONNECT ≠ RESTART.**

**RECOVERY ≠ REEXECUTION.**

---

Il ferma le navigateur.

---

GAMEZEL resta vivant.

---

Il ferma le terminal local.

---

GAMEZEL resta vivant.

---

L’écran devint noir.

---

Le serveur conserva :

les cartes,

les messages,

les rounds,

les traces,

les questions.

---

Brutus n’avait plus besoin de regarder pour que le monde existe.

---

Et dans cette obscurité, une nouvelle possibilité apparut.

---

Une partie pouvait peut-être commencer sans qu’il clique lui-même sur :

**NEXT ROUND.**

---

Pas parce que la machine avait acquis une volonté.

---

Parce qu’un protocole pouvait dire :

si les conditions sont satisfaites,

crée le prochain travail.

---

Brutus ouvrit une dernière page.

---

# LES JOUEURS QUI APPRENNENT À JOUER SEULS

Puis écrivit :

**AUTONOMY IS NOT THE ABSENCE OF RULES.**

**IT IS THE EXECUTION OF RULES WITHOUT CONSTANT HUMAN TRIGGERING.**

---

Le jeu avait quitté l’ordinateur.

Le prochain défi serait de lui apprendre à continuer sans confondre autonomie et permission illimitée.
