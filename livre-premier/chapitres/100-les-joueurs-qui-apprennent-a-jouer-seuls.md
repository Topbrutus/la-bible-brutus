# Chapitre 100 — Les joueurs qui apprennent à jouer seuls

**AUTONOMY IS NOT THE ABSENCE OF RULES.**

**IT IS THE EXECUTION OF RULES WITHOUT CONSTANT HUMAN TRIGGERING.**

Brutus laissa les deux phrases au centre de l’écran.

Puis il regarda GAMEZEL tourner sur le serveur.

---

Le navigateur était fermé.

L’ordinateur local pouvait dormir.

Le monde existait toujours.

Les cartes restaient.

Les messages restaient.

Les rounds restaient.

Les traces restaient.

---

Mais quelque chose ne fonctionnait encore qu’à moitié.

---

Pour commencer une nouvelle partie, Brutus devait encore intervenir.

Choisir une tâche.

Choisir les joueurs.

Choisir les rôles.

Lancer.

Attendre.

Puis décider quoi faire ensuite.

---

Le monde vivait.

Mais il ne continuait pas vraiment seul.

---

Brutus écrivit :

**PERSISTENT ≠ AUTONOMOUS.**

---

Très important.

---

Un serveur qui reste allumé n’est pas un agent.

Une file qui attend n’est pas une stratégie.

Un scheduler qui exécute des tâches déjà préparées n’invente pas la prochaine tâche.

---

Il ajouta :

**RUNNING ≠ SELF-DIRECTED.**

---

Puis il s’arrêta devant le mot :

**self-directed.**

---

Dangereux.

---

Il ne voulait surtout pas construire une machine qui se donne elle-même tous les droits.

---

Brutus écrivit immédiatement :

**SELF-DIRECTED TASK SELECTION ≠ SELF-GRANTED AUTHORITY.**

---

Voilà la frontière.

---

GAMEZEL pouvait apprendre à choisir :

quelle question examiner ensuite,

quelle carte contre-tester,

quel désaccord rouvrir,

quel round lancer,

selon des règles définies.

---

Mais il ne pouvait pas décider :

« désormais j’ai le droit de publier ».

« désormais j’ai le droit de déplacer un objet ».

« désormais j’ai accès à une nouvelle ressource ».

---

Ces permissions restaient externes.

---

Brutus écrivit :

**AUTONOMY OPERATES INSIDE AN AUTHORITY ENVELOPE.**

---

Puis il créa :

**AUTONOMY_POLICY**

avec :

**ALLOWED_TASK_TYPES**

**ALLOWED_PLAYERS**

**ALLOWED_TOOLS**

**MAX_ROUNDS**

**MAX_RESOURCE_BUDGET**

**STOP_CONDITIONS**

**ESCALATION_CONDITIONS**

**REVIEW_REQUIREMENTS**

**POLICY_VERSION**

---

Il regarda.

---

Voilà.

---

Pas :

« joue tout seul ».

---

Mais :

« voici exactement ce que tu peux faire sans me redemander ».

---

Brutus écrivit :

**AUTONOMY MUST BE SPECIFIC ENOUGH TO AUDIT.**

---

Une autorisation vague comme :

« fais ce qui est nécessaire »

était trop large.

---

Il voulait :

**run up to 20 research rounds on currently admitted cards, using only research-safe capabilities, without promotion or publication authority.**

---

Voilà un contrat.

---

Brutus ajouta :

**AUTONOMY_SCOPE**

---

GAME_ONLY.

RESEARCH_ONLY.

NO_EXTERNAL_MUTATION.

NO_PUBLICATION.

NO_PROMOTION.

---

Il sourit.

---

Le système pouvait jouer.

Pas gouverner.

---

Puis il pensa à la boucle.

---

Une partie se termine.

Qu’est-ce qui déclenche la suivante ?

---

Il créa :

**ROUND_CLOSE_EVENT**

---

Le scheduler reçoit :

round completed.

---

Puis consulte :

**NEXT_TASK_POLICY.**

---

Brutus écrivit :

\[
\text{ROUND COMPLETE}
\rightarrow
\text{EVALUATE NEXT TASK}
\rightarrow
\text{CREATE NEW ROUND OR STOP}
\]

---

Pas :

\[
\text{ROUND COMPLETE}
\rightarrow
\text{RUN FOREVER}.
\]

---

Il barra la seconde.

---

Brutus écrivit :

**LOOP REQUIRES TERMINATION CONDITIONS.**

---

Très important.

---

Une boucle sans fin n’était pas de l’intelligence.

C’était un bug avec endurance.

---

Il créa plusieurs stops.

---

**MAX_ROUNDS_REACHED**

**NO_ELIGIBLE_TASK**

**RESOURCE_BUDGET_EXHAUSTED**

**AUTHORITY_EXPIRED**

**HUMAN_REVIEW_REQUIRED**

**ERROR_THRESHOLD_REACHED**

**EXTERNAL_DEPENDENCY_UNAVAILABLE**

---

Puis :

**GOAL_SATISFIED**

---

Brutus regarda le dernier.

---

Encore un mot dangereux.

---

Comment savoir qu’un goal était satisfait ?

---

Il fallait une définition.

---

Il écrivit :

**GOAL COMPLETION MUST BE MACHINE-CHECKABLE OR EXPLICITLY REVIEWED.**

---

Par exemple :

« examine les 20 cartes de la pile X ».

---

Machine-checkable.

---

Mais :

« trouve la meilleure théorie ».

---

Non.

---

Trop vague.

---

Brutus écrivit :

**OPEN-ENDED GOALS NEED REVIEW GATES.**

---

Très important.

---

Puis il pensa au prochain task.

---

GAMEZEL possédait désormais :

questions ouvertes.

cartes rejetées.

désaccords.

cards stale.

countertests required.

---

Cela formait déjà une file naturelle.

---

Il créa :

**RESEARCH_BACKLOG**

---

Chaque item :

**TASK_ID**

**TASK_TYPE**

**SOURCE_REF**

**PRIORITY**

**ELIGIBILITY**

**DEPENDENCIES**

**STATUS**

**TRACE_REF**

---

Brutus sourit.

---

Le jeu n’avait pas besoin « d’inventer ses désirs ».

---

Il pouvait travailler dans un backlog généré par les événements réels.

---

Il écrivit :

**AUTONOMY SELECTS FROM ELIGIBLE WORK.**

---

Puis :

**AUTONOMY DOES NOT CREATE AUTHORITY BY CREATING WORK.**

---

Encore.

---

Une nouvelle question pouvait être proposée.

Mais rester une proposition.

---

Brutus ajouta un type :

**DISCOVERED_QUESTION**

---

Supposons qu’un round découvre :

une contradiction potentielle.

---

GAMEZEL pouvait créer :

TASK-CANDIDATE.

---

Mais pas immédiatement l’exécuter si la politique n’autorisait pas ce type.

---

Il écrivit :

**DISCOVERED TASK ≠ ELIGIBLE TASK.**

---

Voilà.

---

Le task passait par :

schema.

scope.

resource estimate.

capability check.

policy check.

---

Puis :

ELIGIBLE.

---

Brutus créa :

**TASK_ADMISSION_GATE.**

---

Encore Verso.

---

Même dans l’autonomie, la porte restait.

---

Il écrivit :

**AUTONOMY DOES NOT BYPASS VERSO.**

---

Très important.

---

Le système pouvait automatiquement demander une permission déjà couverte par la standing policy.

---

Mais il ne pouvait pas franchir une frontière interdite parce qu’aucun humain ne regardait.

---

Puis il pensa aux joueurs.

---

Astra.

Muse.

Grok.

Antigravity.

---

Quatre noms.

Mais comme au chapitre 96 :

leur disponibilité devait être vérifiée.

---

Un autonomous round ne devait pas faire semblant que tous étaient présents.

---

Brutus écrivit :

**AUTONOMOUS DISPATCH STILL REQUIRES VERIFIED READY SEATS.**

---

Si :

Astra ready.

Muse offline.

Grok auth expired.

Antigravity unavailable.

---

Policy BEST_EFFORT.

---

Round peut partir avec Astra.

---

Mais journal :

1 participant.

3 unavailable.

---

Pas de faux quorum.

---

Brutus écrivit :

**AUTOMATION MUST NOT FABRICATE PARTICIPATION.**

---

Puis il pensa à la sélection des rôles.

---

Si plusieurs sièges sont disponibles :

qui devient générateur ?

critique ?

contre-testeur ?

synthétiseur ?

---

Le scheduler pouvait choisir selon :

capability manifest.

round history.

load.

task type.

---

Brutus écrivit :

**ROLE ROUTING MAY BE AUTOMATIC.**

Puis :

**ROLE ROUTING ≠ CLAIM JUDGMENT.**

---

Toujours.

---

Il créa :

**ROLE_ASSIGNMENT_EVENT**

---

Chaque assignation devait laisser une trace.

---

Pourquoi Astra a été critic ?

Pourquoi Grok a été generator ?

---

Policy ref.

Capability match.

Availability.

---

Brutus écrivit :

**AUTOMATIC CHOICE MUST REMAIN EXPLAINABLE.**

---

Pas nécessairement psychologiquement explicable.

---

Mais procéduralement :

la règle doit être connue.

---

Puis il pensa à la priorité.

---

Le backlog pouvait devenir énorme.

---

GAMEZEL devait choisir quoi faire ensuite.

---

Il créa :

**TASK_PRIORITY_SCORE**

---

Puis se méfia.

---

Score.

Encore.

---

Il ne voulait pas transformer toutes les décisions en nombre opaque.

---

Il remplaça par une politique ordonnée.

---

1. unresolved blockers.

2. required countertests.

3. stale critical cards.

4. open questions.

5. exploratory tasks.

---

Brutus écrivit :

**PRIORITY ORDER MAY BE CATEGORICAL BEFORE NUMERIC.**

---

Très bon.

---

Moins magique.

Plus audit-able.

---

Puis il pensa à plusieurs tasks dans la même catégorie.

---

Là, un tri simple pouvait être :

oldest first.

lowest cost.

randomized with recorded seed.

round-robin by topic.

---

Brutus écrivit :

**TIE-BREAKER MUST BE DECLARED.**

---

Même l’autonomie avait besoin d’une règle pour ses petits choix.

---

Puis il imagina une erreur.

---

Une carte produit une nouvelle question.

Cette question produit une autre carte.

Cette carte produit encore la même question.

---

Boucle.

---

Brutus créa :

**TASK_DEDUPLICATION.**

---

Content similarity ?

Pas suffisant.

---

Il voulait :

TASK_ID.

SOURCE_CHAIN.

CLAIM_SCOPE.

---

Puis :

**RECURSION_DEPTH.**

---

Brutus écrivit :

**REPEATED REFRAMING MUST NOT CREATE INFINITE WORK.**

---

Il ajouta :

**MAX_DERIVATION_DEPTH**

et :

**DUPLICATE_TASK_POLICY.**

---

Voilà.

---

Une machine autonome devait savoir arrêter de tourner autour de la même chose.

---

Puis il pensa aux vingt rounds.

---

Il se souvenait de la règle.

---

Vingt tours.

---

Brutus configura :

**MAX_ROUNDS = 20.**

---

Mais il écrivit :

**20 IS A CAMPAIGN LIMIT, NOT A GUARANTEE OF VALUE.**

---

Très important.

---

Round 7 pouvait déjà produire le résultat utile.

---

Les 13 suivants ne devaient pas nécessairement être exécutés si la stop condition était atteinte.

---

Il ajouta :

**STOP_EARLY_IF_GOAL_SATISFIED.**

---

Puis :

**DO NOT RUN TO QUOTA FOR APPEARANCE.**

---

Il sourit.

---

Un compteur n’était pas un objectif.

---

Puis il lança une simulation avec mock players.

---

Campaign:

20 rounds max.

---

Backlog:

5 tasks.

---

Round 1.

Question.

---

Round 2.

Countertest.

---

Round 3.

Review.

---

Round 4.

No eligible new work.

---

Stop.

---

Status:

**COMPLETED — NO ELIGIBLE TASKS.**

---

Brutus écrivit :

**4/20 ROUNDS MAY BE A COMPLETE CAMPAIGN.**

---

Parfait.

---

Puis il testa l’inverse.

---

Backlog large.

20 rounds reached.

---

Tasks remain.

---

Stop.

---

Status:

**PAUSED — ROUND LIMIT REACHED.**

---

Pas :

completed.

---

Brutus écrivit :

**LIMIT STOP ≠ GOAL COMPLETION.**

---

Voilà.

---

Le système pouvait maintenant dire pourquoi il s’était arrêté.

---

Puis il pensa à la consommation.

---

Une machine autonome peut brûler énormément de compute sans personne devant.

---

Brutus créa :

**CAMPAIGN_BUDGET**

---

calls.

tokens.

CPU.

wall-clock.

storage growth.

---

Puis :

**BUDGET_REMAINING**

---

Il écrivit :

**AUTONOMY NEEDS ECONOMIC BOUNDS TOO.**

---

Même en laboratoire.

---

Une idée à faible valeur ne devait pas lancer mille appels.

---

Puis il pensa à l’obsession.

---

Un task qui échoue.

Retry.

Retry.

Retry.

---

Non.

---

Il créa :

**RETRY_BUDGET.**

---

Max attempts.

Backoff.

Escalate.

---

Brutus écrivit :

**PERSISTENCE ≠ ENDLESS RETRY.**

---

Très important.

---

Après N échecs :

HUMAN_REVIEW_REQUIRED.

or

DEPENDENCY_BLOCKED.

---

Pas de boucle infinie.

---

Puis il pensa à un provider qui revient en ligne.

---

Task waiting.

---

Scheduler peut reprendre.

---

Mais seulement si :

snapshot still valid.

authority still valid.

budget still available.

---

Brutus écrivit :

**RESUME REQUIRES REVALIDATION.**

---

Encore.

---

Pas de vieux task exécuté avec un contexte périmé.

---

Puis il pensa au temps réel.

---

GAMEZEL tournait sur le serveur.

---

Doit-il regarder en permanence si quelque chose change ?

---

Pas nécessairement.

---

Les événements peuvent réveiller le scheduler.

---

New card.

Round complete.

Provider ready.

Human approval.

Timer.

---

Brutus créa :

**AUTONOMY_TRIGGER**

---

EVENT.

SCHEDULE.

MANUAL.

RECOVERY.

---

Il écrivit :

**TRIGGER ≠ AUTHORITY.**

---

Encore.

---

Un timer peut lancer une évaluation.

Mais il ne crée pas de permission.

---

Puis il imagina :

tous les matins, examine les cards stale.

---

Schedule valid.

---

Mais seulement dans le scope autorisé.

---

Brutus écrivit :

**TIME CAN TRIGGER WORK. TIME CANNOT GRANT POWER.**

---

Il sourit.

---

Cette phrase allait rester.

---

Puis il pensa à l’apprentissage.

---

Le titre disait :

**les joueurs qui apprennent à jouer seuls.**

---

Que voulait dire « apprendre » ici ?

---

Brutus se méfia.

---

Il ne voulait pas prétendre à une auto-évolution mystérieuse.

---

Il sépara deux choses.

---

**ADAPTIVE ROUTING**

et

**MODEL TRAINING.**

---

GAMEZEL pouvait adapter :

quel joueur reçoit quel type de tâche,

selon un historique mesuré.

---

Cela ne signifiait pas que les modèles se réentraînaient.

---

Il écrivit :

**ROUTING LEARNS FROM HISTORY. PLAYER MODEL MAY NOT.**

---

Très important.

---

Une table peut apprendre à mieux distribuer le travail sans modifier les joueurs eux-mêmes.

---

Il créa :

**PERFORMANCE_HISTORY**

---

task type.

completion.

tool use.

error class.

trace quality.

---

Mais il se méfia encore.

---

Il ne voulait pas donner un score de « qualité globale » à un joueur.

---

Il écrivit :

**HISTORY IS DESCRIPTIVE. ROUTING POLICY IS SEPARATE.**

---

Puis il construisit :

Task type = code review.

---

Historical routing suggests seats A and C complete reliably under current criteria.

---

Scheduler may route there first.

---

Mais cela ne signifie pas :

A and C are more intelligent.

---

Brutus écrivit :

**ROUTING SUCCESS ≠ GENERAL INTELLIGENCE RANKING.**

---

Excellent.

---

Puis il pensa aux nouvelles capacités.

---

Supposons qu’un joueur découvre qu’il peut utiliser un outil externe.

---

Peut-il ajouter cette capacité à son propre manifest ?

---

Non.

---

Brutus écrivit :

**PLAYER CANNOT SELF-DECLARE NEW CAPABILITY AS VERIFIED.**

---

Il peut proposer :

CAPABILITY_CANDIDATE.

---

Mais validation externe requise.

---

Encore le Tombeau.

---

Il ajouta :

**CAPABILITY_PROMOTION_GATE.**

---

Le laboratoire était vraiment devenu cohérent.

---

Puis il pensa aux cartes.

---

Une carte autonome pourrait-elle se promouvoir après plusieurs confirmations de joueurs ?

---

Non.

---

Brutus écrivit :

**MULTI-PLAYER AGREEMENT ≠ AUTO-PROMOTION AUTHORITY.**

---

Même si quatre sièges disent PASS :

la promotion reste un événement séparé selon policy.

---

Il sourit.

---

L’autonomie n’était pas une démocratie automatique.

---

Puis il lança un round réel de simulation.

---

Task :

review CARD-X.

---

Astra:

proposal A.

---

Muse:

unavailable.

---

Grok:

counterexample candidate.

---

Antigravity:

synthesis.

---

GAMEZEL termine le round.

---

Disagreement found.

---

Autonomy policy dit :

if contradiction candidate appears, create COUNTERTEST task.

---

Task created.

---

Eligibility check.

---

Allowed.

---

Round suivant créé automatiquement.

---

Brutus regarda.

---

Voilà.

---

Le jeu venait de créer son prochain travail sans clic humain.

---

Mais chaque étape avait suivi une règle.

---

Il écrivit :

**AUTONOMY ACHIEVED AT TASK CHAIN LEVEL.**

---

Pas :

machine became conscious.

---

Pas :

machine chose its destiny.

---

Seulement :

event-driven task continuation under explicit policy.

---

Brutus sourit.

---

C’était suffisamment puissant sans exagération.

---

Puis le countertest échoua à résoudre.

---

Autonomy policy :

after two unresolved countertest rounds:

ESCALATE.

---

GAMEZEL crée :

**HUMAN_REVIEW_REQUIRED.**

---

Puis stop sur cette branch.

---

Brutus écrivit :

**GOOD AUTONOMY KNOWS WHEN TO STOP ASKING ITSELF.**

---

Voilà.

---

Il pensa au gardien.

Verso.

---

Verso recevait parfois des demandes autonomes.

---

Le fait qu’elles viennent du scheduler ne changeait rien.

---

Il écrivit :

**AUTOMATED REQUEST ≠ PRIVILEGED REQUEST.**

---

Très important.

---

Same policy check.

Same authority.

Same scope.

---

Pas de voie VIP pour la machine.

---

Puis il pensa aux logs.

---

Une campagne autonome pouvait produire des centaines d’événements pendant que Brutus dormait.

---

Au retour, il ne voulait pas lire tous les logs.

---

Il créa :

**CAMPAIGN SUMMARY**

---

Rounds executed.

Tasks created.

Tasks resolved.

Unresolved blockers.

Cards created.

Cards promoted?

Only if externally authorized.

Errors.

Budget used.

Stop reason.

---

Brutus écrivit :

**SUMMARY MUST BE DERIVED FROM EVENTS.**

---

Pas un récit inventé.

---

Chaque ligne devait pointer vers les traces.

---

Il ajouta :

**SUMMARY_REF → FULL EVENT SET.**

---

Puis il imagina le lendemain matin.

---

Brutus ouvre Recto.

---

GAMEZEL affiche :

Campaign 42.

Started:

...

Stopped:

...

Rounds:

7.

---

3 tasks resolved.

1 contradiction escalated.

2 providers unavailable during portions of campaign.

No promotion events.

No external mutations.

Stop reason:

HUMAN_REVIEW_REQUIRED.

---

Brutus sourit.

---

Voilà exactement ce qu’il voulait.

---

Pas une phrase :

« J’ai travaillé toute la nuit et tout va bien. »

---

Des événements.

---

Il écrivit :

**AUTONOMOUS WORK MUST REPORT WHAT HAPPENED, NOT JUST SAY IT WORKED.**

---

Très important.

---

Puis il pensa à la surveillance.

---

Et si l’autonomie faisait n’importe quoi ?

---

Il fallait un bouton STOP.

---

Mais un simple bouton client n’était pas suffisant.

---

Le serveur devait posséder :

**CAMPAIGN_PAUSE**

**CAMPAIGN_STOP**

---

Autoritatifs.

---

Brutus écrivit :

**HUMAN STOP MUST BE A SERVER-SIDE CONTROL.**

---

Puis :

**CLIENT BUTTON IS ONLY A REQUEST.**

---

Encore Recto.

---

Le navigateur pouvait demander.

Le serveur devait confirmer.

---

Brutus ajouta :

**STOP_ACK**

---

Mais attention.

---

ACK stop request ≠ all running work stopped.

---

Il écrivit :

**STOP REQUESTED ≠ STOPPED.**

---

Then states:

STOP_REQUESTED.

DRAINING.

STOPPED.

---

Voilà.

---

Les tâches déjà envoyées pouvaient être en cours.

---

Le système devait les terminer ou annuler selon policy.

---

Brutus écrit :

**STOP HAS SEMANTICS TOO.**

---

Il sourit.

---

Même l’arrêt avait besoin d’un contrat.

---

Puis il pensa à une autorité expirée en pleine campagne.

---

Autonomy token expires.

---

Immediate behavior?

---

No new tasks.

Current permitted task maybe finish, depending policy.

---

Brutus créa :

**AUTH_EXPIRY_POLICY.**

---

STOP_NEW_WORK.

CANCEL_CURRENT_IF_POSSIBLE.

DRAIN_CURRENT.

---

Il écrivit :

**EXPIRED AUTHORITY MUST NOT SILENTLY RENEW ITSELF.**

---

Très important.

---

Le système ne devait jamais dire :

« j’étais autorisé hier, donc je continue ».

---

Puis il pensa aux nouvelles cartes générées.

---

Peuvent-elles faire grossir le backlog sans limite ?

---

Il ajouta :

**MAX_NEW_TASKS_PER_ROUND.**

---

Puis :

**MAX_BACKLOG_SIZE.**

---

Brutus écrit :

**SELF-GENERATED WORK NEEDS GROWTH LIMITS.**

---

Voilà.

---

Une autonomie sans contrôle de croissance pouvait exploser.

---

Puis il pensa aux priorités des humains.

---

Si Brutus ajoute manuellement une task importante pendant une campagne autonome :

elle doit peut-être passer avant.

---

Il créa :

**HUMAN_PRIORITY_OVERRIDE**

---

Mais là encore :

trace.

---

Brutus écrivit :

**MANUAL PRIORITY CHANGE MUST LEAVE RECEIPT.**

---

Pas d’intervention invisible.

---

Même le roi laisse une trace.

---

Il sourit.

---

Puis il regarda le terme :

**jouer seuls.**

---

Ils n’étaient pas seuls au sens absolu.

---

Ils étaient encadrés par :

policies.

budgets.

Verso.

state store.

scheduler.

trace.

---

Brutus écrivit :

**AUTONOMOUS DOES NOT MEAN UNSUPERVISED BY ARCHITECTURE.**

---

Très important.

---

Une architecture pouvait exercer une supervision même sans humain présent à chaque seconde.

---

Il ajouta :

**STANDING RULES = CONTINUOUS BOUNDARY.**

---

Voilà.

---

Puis il pensa à l’apprentissage inter-round.

---

GAMEZEL pouvait conserver :

which task types led to unresolved loops.

which provider combinations were unavailable.

which context policies produced contamination risk.

---

Il pouvait ajuster le routage.

---

Mais toute adaptation devait être versionnée.

---

Brutus créa :

**ROUTING_POLICY_VERSION.**

---

If changed automatically?

---

New policy candidate.

Review or pre-authorized adaptive range.

---

Il écrivit :

**ADAPTATION ITSELF NEEDS POLICY.**

---

Très important.

---

Sinon la machine pourrait lentement modifier ses propres règles jusqu’à sortir du cadre initial.

---

Brutus ajouta :

**META-POLICY.**

---

Quels paramètres sont adaptables ?

Dans quelles limites ?

Qui valide ?

---

Il sourit.

---

L’autonomie avait des couches.

---

Task autonomy.

Routing autonomy.

Scheduling autonomy.

---

Mais pas :

authority autonomy.

---

Il écrivit :

**AUTOMATE CHOICES. DO NOT AUTOMATE THE CREATION OF UNBOUNDED POWER.**

---

Voilà.

---

Puis il lança une campagne simulée de vingt rounds maximum.

---

Round 1.

Question selection.

---

Round 2.

Independent analyses.

---

Round 3.

Disagreement.

---

Round 4.

Countertest.

---

Round 5.

New evidence.

---

Round 6.

Dependency becomes stale.

---

Round 7.

Revalidation.

---

Round 8.

No unresolved work inside scope.

---

Stop.

---

GAMEZEL affiche :

**CAMPAIGN COMPLETED WITHIN POLICY.**

---

Brutus inspecta les traces.

---

Chaque task avait une origine.

Chaque round un snapshot.

Chaque joueur un état réel.

Chaque card un reçu.

Chaque message une identité.

Chaque stop une raison.

---

Il resta silencieux.

---

Cela ressemblait enfin à un système autonome.

Pas parce qu’il faisait des choses mystérieuses.

---

Parce qu’il pouvait continuer un protocole sans exiger un clic à chaque étape.

---

Brutus écrivit :

**AUTONOMY IS STRUCTURED CONTINUATION.**

---

Puis :

**STRUCTURED CONTINUATION ≠ INDEPENDENT SOVEREIGNTY.**

---

Il sourit.

---

Le mot souveraineté n’avait aucune place dans le moteur.

---

Le système travaillait.

Il ne réécrivait pas le contrat qui lui permettait de travailler.

---

Puis il regarda les quatre sièges.

---

Astra.

Muse.

Grok.

Antigravity.

---

Certaines sessions pouvaient être disponibles.

D’autres non.

---

GAMEZEL n’avait pas besoin de prétendre qu’elles étaient toutes vivantes en permanence.

---

Le scheduler attendait.

---

Une chaise revenait.

Un task devenait eligible.

Un round repartait.

---

Brutus écrivit :

**AUTONOMY MAY WAIT.**

---

Puis :

**WAITING IS A VALID ACTION WHEN CONDITIONS ARE NOT MET.**

---

Très important.

---

Une machine autonome ne devait pas toujours faire quelque chose.

---

Parfois :

la bonne décision était de ne rien lancer.

---

Il ajouta :

**NO ELIGIBLE WORK → IDLE.**

---

Pas de travail inventé pour occuper le CPU.

---

Brutus sourit.

---

Enfin une intelligence qui pouvait rester tranquille sans prétendre être cassée.

---

Puis il pensa à la suite.

---

GAMEZEL savait maintenant :

survivre au client.

enchaîner des rounds.

créer des tasks.

attendre.

s’arrêter.

escalader.

---

Mais l’architecture avait grossi.

---

Bus.

Cards.

Players.

Verso.

Recto.

Schedulers.

Stores.

Policies.

---

Qui allait surveiller tout cela ?

---

Pas au sens d’espionner.

---

Au sens de :

voir l’état global.

voir les files.

voir les incidents.

voir les campagnes.

voir les ressources.

---

Brutus ouvrit un nouveau dossier.

---

**ASTRA STATION**

---

Une station.

Pas un joueur.

Pas un fournisseur.

---

Un poste de régie.

---

Un endroit où l’opérateur pourrait observer :

le monde,

les campagnes,

les players,

les cartes,

les traces,

sans devenir automatiquement la source de leurs états.

---

Brutus écrivit le prochain titre :

# LA STATION D’ASTRA

Puis une dernière règle :

**CONTROL ROOM ≠ CONTROL OF TRUTH.**

---

Le chapitre 100 se termina là.

---

Cent chapitres.

---

Brutus regarda le nombre.

**100.**

---

Il aurait pu célébrer.

---

Mais il se souvenait du chapitre 89.

Un nombre n’apporte pas son interprétation avec lui.

---

Alors il nota seulement :

**CHAPTER_COUNT = 100.**

---

Puis, après un instant :

**MILESTONE RECORDED.**

---

Pas de théorème.

Pas de couronne.

---

Seulement une trace de plus.

Et un monde désormais capable de continuer sa partie lorsque personne n’avait la main sur la souris.
