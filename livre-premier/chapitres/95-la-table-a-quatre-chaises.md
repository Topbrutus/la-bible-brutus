# Chapitre 95 — La table à quatre chaises

Quatre écrans.

Quatre chaises.

Une seule table.

Brutus resta debout derrière la première.

---

Recto fonctionnait.

Verso gardait la porte.

Le Tombeau séparait les états.

La carte des lignées conservait les histoires.

---

Il ne manquait plus quelque chose.

Pas une nouvelle formule.

Pas un nouveau moteur.

Des joueurs.

---

Brutus regarda les quatre sièges.

Il les nomma simplement :

**P1**

**P2**

**P3**

**P4**

---

Pas encore Astra.

Pas encore Muse.

Pas encore Grok.

Pas encore Antigravity.

---

Les noms viendraient ensuite.

---

Pour l’instant, Brutus voulait construire la table avant d’inviter quiconque à s’y asseoir.

---

Il écrivit :

**SEAT BEFORE PLAYER.**

---

Puis :

**ROLE BEFORE IDENTITY.**

---

Voilà.

---

Une bonne architecture ne devait pas dépendre du fournisseur ou de l’intelligence particulière qui occuperait une chaise.

---

P1 pouvait être humain aujourd’hui.

Une IA demain.

Un script de test après-demain.

---

Le protocole devait rester le même.

---

Brutus créa :

**GAME TABLE**

avec quatre slots.

---

**SEAT_ID**

**PLAYER_ID**

**PLAYER_TYPE**

**SESSION_ID**

**CAPABILITIES**

**STATE**

**LATEST_MOVE**

**TRACE_REF**

---

Puis il ajouta :

**AUTHORITY_SCOPE**

---

Il sourit.

---

Une chaise ne donnait pas une autorité par simple occupation.

---

Il écrivit :

**SITTING ≠ AUTHORITY.**

---

Très important.

---

Un joueur pouvait :

voir.

analyser.

proposer.

répondre.

---

Mais seulement si le contrat l’autorisait.

---

Brutus créa trois niveaux.

---

**OBSERVE**

---

**PROPOSE**

---

**ACT**

---

Puis immédiatement :

**ACT REQUIRES SEPARATE AUTHORIZATION.**

---

Voilà.

---

Le jeu pouvait être riche sans rendre les joueurs omnipotents.

---

Il écrivit :

**PLAYING THE GAME ≠ CONTROLLING THE WORLD.**

---

Le mot jeu apparaissait maintenant officiellement.

---

Brutus donna un nom au prototype :

# GAMEZEL

---

Il regarda le titre.

---

GAME.

ZEL.

---

Un espace où plusieurs joueurs pouvaient travailler autour des objets du laboratoire.

---

Pas un jeu vidéo traditionnel.

Pas un casino.

Pas une simulation magique.

---

Un protocole de tours.

---

Brutus écrivit :

**GAMEZEL = TURN-BASED EXPERIMENT COORDINATION.**

---

Puis il pensa à la règle principale.

---

Qui joue en premier ?

---

Il pouvait simplement fixer :

P1.

Puis P2.

Puis P3.

Puis P4.

---

Mais l’ordre devait être explicite.

---

Il écrivit :

\[
P1\rightarrow P2\rightarrow P3\rightarrow P4\rightarrow P1.
\]

---

Puis :

**TURN_ORDER IS DATA.**

---

Le chapitre 73 revenait.

---

Même quatre joueurs intelligents pouvaient produire du chaos si l’ordre n’était pas défini.

---

Il créa :

**ROUND_ID**

**TURN_ID**

**SEAT_ID**

**START_TICK**

**END_TICK**

**INPUT_REF**

**OUTPUT_REF**

**STATE**

---

Voilà.

---

Un tour devenait une entité.

---

Brutus écrivit :

**A TURN IS NOT JUST A MESSAGE.**

---

Il devait savoir :

qui parlait,

quand,

sur quoi,

à partir de quel état,

et ce qui avait été produit.

---

Premier test.

---

ROUND-0001.

TURN-0001.

Seat:

P1.

---

Question :

« Analyse l’objet L8. »

---

P1 produit une proposition.

---

Brutus enregistre :

**PROPOSAL-0001.**

---

Puis P2 reçoit quoi ?

---

La question originale ?

Ou la réponse de P1 ?

---

Brutus s’arrêta.

---

Très important.

---

Le protocole devait déclarer le contexte visible à chaque joueur.

---

Il créa :

**CONTEXT_POLICY.**

---

Options :

**SOURCE_ONLY**

**PREVIOUS_MOVE**

**FULL_ROUND_HISTORY**

**SELECTED_SHARED_CONTEXT**

---

Brutus regarda.

---

Voilà un choix architectural majeur.

---

Si chaque joueur voyait tout ce que les autres avaient dit, ils pouvaient se contaminer mutuellement.

---

Si chacun travaillait séparément, on gagnait une certaine indépendance.

---

Il écrivit :

**SHARED CONTEXT ≠ INDEPENDENT ANALYSIS.**

---

Encore une vieille leçon.

---

Deux joueurs produisant la même réponse après avoir lu le même raisonnement ne constituaient pas deux vérifications indépendantes.

---

Brutus créa deux modes.

---

**COLLABORATIVE ROUND**

et

**BLIND ROUND**

---

Dans le premier :

les joueurs voient les réponses précédentes.

---

Dans le second :

chacun reçoit la même source mais pas les réponses des autres.

---

Brutus écrivit :

**INDEPENDENCE MUST BE DESIGNED.**

---

Très important.

---

Il imagina un contre-test mathématique.

---

Quatre joueurs reçoivent le même claim.

---

Blind round.

---

P1 calcule.

P2 critique.

P3 cherche un contre-exemple.

P4 vérifie la structure.

---

Puis seulement après les quatre tours :

les réponses sont révélées ensemble.

---

Brutus sourit.

---

Voilà une vraie utilisation.

---

Il écrivit :

**SEPARATE GENERATION. SHARED COMPARISON.**

---

Puis il imagina une session créative.

---

Là, au contraire, les joueurs pouvaient rebondir.

---

P1 propose une idée.

P2 l’étend.

P3 la critique.

P4 la reformule.

---

Collaborative round.

---

Brutus écrivit :

**DIFFERENT TASK → DIFFERENT CONTEXT POLICY.**

---

Encore la même architecture.

---

Pas de mode roi.

---

Puis il pensa au score.

---

Un jeu appelle presque automatiquement des points.

---

Brutus se méfia.

---

Que voulait dire :

Astra 8.

Muse 6.

Grok 9.

Antigravity 4 ?

---

Sans définition :

rien.

---

Il écrivit :

**NO SCORE WITHOUT SCORING CONTRACT.**

---

Très important.

---

Il créa plutôt :

**EVALUATION DIMENSIONS**

---

correctness.

relevance.

novelty.

traceability.

counterexample strength.

contract compliance.

---

Mais il refusa encore de les combiner automatiquement.

---

Il écrivit :

**MULTI-DIMENSIONAL EVALUATION ≠ SINGLE WINNER.**

---

Voilà.

---

GAMEZEL n’avait pas besoin d’un champion.

---

Il avait besoin d’une meilleure exploration.

---

Brutus ajouta :

**COMPARE CONTRIBUTIONS. DO NOT CROWN BY DEFAULT.**

---

Puis il imagina qu’un joueur se trompe.

---

Très bien.

---

Le jeu devait garder la mauvaise réponse.

---

Pas pour la punir.

Pour la trace.

---

Il écrivit :

**FAILED MOVE STAYS IN HISTORY.**

---

Le chapitre 93 revenait.

---

Une mauvaise proposition pouvait contenir :

une intuition utile.

un contre-exemple mal formé.

une relation rejetée.

---

Tout cela devait rester inspectable.

---

Brutus créa :

**MOVE_STATUS**

---

PROPOSED.

ACCEPTED_FOR_REVIEW.

REJECTED.

SUPERSEDED.

UNRESOLVED.

---

Pas de suppression automatique.

---

Puis il pensa à un autre danger.

---

Un joueur pouvait générer beaucoup trop de texte.

---

La table deviendrait illisible.

---

Il créa :

**MOVE_BUDGET.**

---

Token budget.

Time budget.

Tool budget.

Output schema.

---

Brutus écrivit :

**INTELLIGENCE STILL NEEDS BOUNDS.**

---

Il sourit.

---

Un joueur brillant mais sans limite pouvait monopoliser la table.

---

Il ajouta :

**ONE TURN = ONE BOUNDED CONTRIBUTION.**

---

Puis :

**LONG WORK MAY PRODUCE A CAPSULE + SUMMARY.**

---

Encore le Witness Viewer.

---

La table devait pouvoir résumer sans perdre la matière complète.

---

Brutus créa :

**MOVE_CAPSULE.**

---

Summary.

Full output.

Artifacts.

Trace.

Claims.

References.

---

Puis il pensa à la simultanéité.

---

Pourquoi jouer un joueur après l’autre ?

---

Peut-être que quatre joueurs pourraient calculer en parallèle.

---

Il sourit.

---

Oui.

Mais ce serait un autre mode.

---

**PARALLEL ROUND.**

---

Tous reçoivent le même snapshot.

---

Tous produisent sans voir les autres.

---

Puis barrier.

---

Résultats collectés.

---

Brutus écrivit :

**SAME SNAPSHOT REQUIRED FOR FAIR PARALLEL COMPARISON.**

---

Très important.

---

Si P4 reçoit un état plus récent que P1, leurs réponses ne sont plus directement comparables.

---

Il ajouta :

**ROUND_SNAPSHOT_ID.**

---

Chaque joueur reçoit :

même source version.

même task ID.

même policy context.

---

Voilà.

---

Puis Brutus pensa aux outils.

---

Un joueur pouvait avoir accès au moteur mathématique.

Un autre non.

---

Un autre à des fichiers.

Un autre à un modèle audio.

---

La comparaison devait donc savoir :

qui avait accès à quoi ?

---

Il créa :

**CAPABILITY_MANIFEST.**

---

Brutus écrivit :

**OUTPUT QUALITY CANNOT BE INTERPRETED WITHOUT TOOL CONTEXT.**

---

Une réponse obtenue avec un calculateur exact et une réponse produite mentalement ne venaient pas du même environnement.

---

Cela ne rendait pas l’une meilleure.

Mais la trace devait le dire.

---

Il ajouta :

**TOOLS_USED**

**TOOLS_AVAILABLE**

---

Très important.

---

Un joueur pouvait ne pas utiliser un outil disponible.

Autre information.

---

Puis il pensa aux erreurs de réseau.

---

P3 ne répond pas.

---

Que fait la table ?

---

Elle ne devait pas fabriquer un tour.

---

Brutus écrivit :

**NO RESPONSE ≠ EMPTY RESPONSE.**

---

Puis :

**ABSENT PLAYER ≠ PLAYER SAID NOTHING.**

---

Voilà.

---

Le statut devenait :

**NO_RESPONSE**

ou

**UNAVAILABLE**

---

Pas un message vide.

---

Le round pouvait :

attendre,

continuer,

ou se clôturer incomplet,

selon policy.

---

Il créa :

**ROUND_COMPLETION_POLICY.**

---

ALL_PLAYERS_REQUIRED.

QUORUM.

BEST_EFFORT.

---

Brutus sourit.

---

Même une partie avait besoin de règles de disponibilité.

---

Puis il pensa à l’authentification.

---

Un siège disait :

PLAYER_ID = P3.

---

Comment savoir qui s’y trouvait réellement ?

---

Il fallait une session validée.

---

Il écrivit :

**CLAIMED PLAYER ID ≠ AUTHENTICATED PLAYER ID.**

---

Encore la même règle que Verso.

---

La table devait recevoir :

**PLAYER_SESSION_REF**

---

Pas faire confiance à un simple label.

---

Puis il se rappela quelque chose.

---

Les futurs sièges P2, P3 et P4 pourraient dépendre de services externes.

---

Ils pouvaient ne pas être connectés.

---

Il écrivit :

**SEAT EXISTS EVEN WHEN PLAYER DOES NOT.**

---

Voilà une règle très importante pour la suite.

---

L’architecture de quatre joueurs pouvait être complète même si certains sièges étaient :

DISCONNECTED.

UNAUTHENTICATED.

DISABLED.

---

Brutus sourit.

---

La table n’allait pas prétendre que quatre joueurs étaient actifs juste parce qu’il y avait quatre chaises.

---

Il écrivit :

**FOUR CHAIRS ≠ FOUR LIVE PLAYERS.**

---

Puis :

**CONFIGURED ≠ AUTHENTICATED ≠ AVAILABLE ≠ PARTICIPATED.**

---

Excellent.

---

Le statut de chaque siège devait être clair.

---

Il créa :

**SEAT_STATE**

---

EMPTY.

CONFIGURED.

AUTH_PENDING.

READY.

BUSY.

OFFLINE.

ERROR.

---

Pas seulement ON/OFF.

---

Puis il posa quatre rectangles sur l’écran.

---

P1:

READY.

---

P2:

EMPTY.

---

P3:

EMPTY.

---

P4:

EMPTY.

---

Brutus sourit.

---

Le système pouvait déjà fonctionner avec un seul joueur.

---

Il écrivit :

**TABLE DEGRADES GRACEFULLY.**

---

Une table à quatre chaises n’exigeait pas quatre joueurs en permanence.

---

Très important.

---

Puis il lança :

ROUND-0001.

Only ready seats participate.

---

P1 joue.

---

Round status:

COMPLETED_PARTIAL.

---

Not error.

---

Brutus écrivit :

**PARTIAL ROUND ≠ FAILED ROUND IF POLICY ALLOWS IT.**

---

Voilà.

---

Puis il simula quatre joueurs.

---

Mock players.

Pas vrais fournisseurs.

---

Des agents de test déterministes.

---

P1 retourne A.

P2 retourne B.

P3 retourne C.

P4 retourne D.

---

Le scheduler fonctionna.

---

Round order correct.

---

Brutus écrivit :

**PROTOCOL TESTED WITH MOCK PLAYERS.**

---

Pas :

four AI providers connected.

---

La distinction était essentielle.

---

Il ajouta :

**MOCK SUCCESS ≠ PROVIDER INTEGRATION.**

---

Voilà le garde-fou pour la suite.

---

Puis il pensa au « tour de jeu ».

---

Chaque round devait produire quelque chose d’utile.

---

Pas forcément une décision.

---

Il créa :

**ROUND_RESULT**

---

candidate set.

disagreements.

unresolved questions.

consensus observations.

counterexamples.

next actions.

---

Brutus évita le mot consensus comme vérité.

---

Il écrivit :

**AGREEMENT ≠ CORRECTNESS.**

---

Très important.

---

Quatre joueurs pouvaient tous faire la même erreur.

---

Donc :

agreement était une propriété de leurs réponses.

Pas une preuve.

---

Il ajouta :

**CONSENSUS_COUNT**

mais aussi :

**EVIDENCE_REFS**

---

Le nombre de joueurs d’accord ne remplaçait pas les preuves.

---

Brutus écrivit :

**VOTE ≠ PROOF.**

---

Voilà.

---

GAMEZEL ne devait surtout pas transformer la mathématique en démocratie.

---

Si trois joueurs disaient :

\[
2+2=5,
\]

et un disait :

4,

le vote n’avait aucune autorité sur l’arithmétique.

---

Brutus écrivit :

**MAJORITY CAN PRIORITIZE REVIEW.**

**MAJORITY CANNOT OVERRIDE FACT.**

---

Excellent.

---

Il pensa à une architecture intéressante.

---

Après chaque round :

les désaccords les plus forts pouvaient recevoir un round de contre-test.

---

Brutus créa :

**DISAGREEMENT QUEUE.**

---

Si P1 et P2 produisent une conclusion différente :

create challenge.

---

P3 et P4 peuvent examiner.

---

Ou un outil exact tranche.

---

Mais encore :

outil exact selon son domaine.

---

Il écrivit :

**DISAGREEMENT IS A RESEARCH TARGET.**

---

Cela lui plaisait beaucoup.

---

Au lieu de masquer les divergences, GAMEZEL allait les mettre en avant.

---

Il ajouta :

**DO NOT AVERAGE INCOMPATIBLE ANSWERS.**

---

Une règle essentielle.

---

Deux réponses contradictoires ne devaient pas produire une troisième réponse moyenne.

---

Brutus rit.

---

Pas de :

« peut-être 4.5 ».

---

Il conserva les deux.

---

Puis demande :

why differ?

---

Le système pouvait comparer :

assumptions.

input version.

tools.

method.

round context.

---

Brutus écrivit :

**COMPARE METHODS BEFORE COMPARING CONCLUSIONS.**

---

Très bon.

---

Le chapitre 89 revenait.

Comparability before comparison.

---

Puis il créa la première vraie fiche de partie.

---

**GAME_ID: GAMEZEL-0001**

---

Mode:

BLIND_PARALLEL.

---

Players:

P1.

P2.

P3.

P4.

---

Task:

analyze claim X.

---

Snapshot:

S-0001.

---

Output requirement:

claim + evidence + uncertainty + counterexample attempt.

---

Brutus regarda.

---

Voilà une vraie partie scientifique.

---

Pas de score.

Pas de vainqueur.

---

Quatre voies vers une question.

---

Il écrivit :

**GAME OBJECTIVE = IMPROVE THE STATE OF KNOWLEDGE.**

---

Puis se corrigea légèrement.

---

Même cela pouvait être trop grand.

---

Il remplaça :

**GAME OBJECTIVE = PRODUCE TRACEABLE CONTRIBUTIONS TO THE TASK.**

---

Plus précis.

---

Le monde réel déciderait si la connaissance s’était améliorée.

---

Brutus sourit.

---

Les formulations devenaient très propres.

---

Puis il pensa aux cartes.

---

Dans les travaux précédents, chaque partie pouvait ajouter des cartes.

---

Une carte pouvait représenter :

une formule.

une hypothèse.

un test.

un contre-exemple.

un artefact.

---

Brutus créa :

**GAME CARD**

---

CARD_ID.

CARD_TYPE.

SOURCE_MOVE.

CLAIM_SCOPE.

STATUS.

TRACE_REF.

---

À la fin d’un round, certaines contributions pouvaient devenir des cartes.

---

Mais il écrivit :

**MOVE ≠ CARD AUTOMATICALLY.**

---

Une politique de promotion devait décider.

---

Encore.

---

Pas d’auto-promotion.

---

Puis il pensa aux cartes persistantes.

---

Une bonne carte pouvait revenir dans une partie suivante.

---

Mais son contexte devait voyager avec elle.

---

Il écrivit :

**CARD MUST CARRY LINEAGE.**

---

Pas un simple texte copié.

---

La carte devait savoir :

qui l’avait produite.

dans quel round.

sur quel snapshot.

avec quels outils.

sous quel statut.

---

Brutus sourit.

---

Le chapitre 93 entrait directement dans GAMEZEL.

---

Puis il imagina une table qui joue plusieurs parties.

---

GAME-0001.

GAME-0002.

GAME-0003.

---

Les cartes s’accumulent.

---

Le système devient plus riche.

---

Mais il ne devait pas devenir plus confiant automatiquement.

---

Brutus écrivit :

**MORE GAMES ≠ MORE TRUTH.**

---

Puis :

**MORE GAMES = MORE TRACE, IF TRACE QUALITY IS PRESERVED.**

---

Voilà.

---

Il pensa aux vieux résultats.

---

Une carte produite sous une ancienne version d’une formule pouvait être obsolète.

---

Il ajouta :

**CARD_VERSION_CONTEXT**

---

et

**STALE_IF_DEPENDENCY_CHANGED.**

---

Très utile.

---

Si une formule parent est corrigée :

les cartes dépendantes peuvent être marquées :

REVIEW_REQUIRED.

---

Pas supprimées.

---

Brutus écrivit :

**DEPENDENCY CHANGE TRIGGERS REVIEW, NOT MEMORY LOSS.**

---

Encore la carte des lignées.

---

Puis il regarda les quatre écrans.

---

Recto 1.

Recto 2.

Recto 3.

Recto 4.

---

Il donna à chaque chaise sa propre vue.

---

P1 :

task.

---

P2 :

task.

---

P3 :

task.

---

P4 :

task.

---

Puis écran central :

round summary.

---

Aucun siège ne pouvait modifier l’état canonique directement.

---

Les joueurs envoyaient des propositions.

---

GAMEZEL enregistrait.

---

Verso et les autres contrats décidaient ce qui pouvait passer ailleurs.

---

Brutus écrivit :

**PLAYER OUTPUT ENTERS AS PROPOSAL.**

**PROPOSAL ≠ WORLD STATE.**

---

Voilà peut-être la règle la plus importante de toute la table.

---

Un joueur pouvait halluciner.

Se tromper.

Inventer.

---

Le monde ne devait pas changer pour autant.

---

Il ajouta :

**ALL PLAYER OUTPUTS ARE UNTRUSTED UNTIL VALIDATED FOR THEIR TARGET USE.**

---

Très important.

---

Même P1.

Même un joueur réputé excellent.

---

Aucune exemption.

---

Brutus écrivit :

**TRUST IS CLAIM-SCOPED, NOT PLAYER-SCOPED.**

---

Il sourit.

---

Exactement comme les témoins.

---

Un joueur pouvait être excellent en code.

Moins bon en mathématiques.

Ou inversement.

---

Le système ne devait pas donner :

PLAYER TRUST = 98%.

---

Trop grossier.

---

Il créa :

**CAPABILITY-SPECIFIC PERFORMANCE HISTORY.**

---

Mais pas pour produire une autorité automatique.

---

Seulement pour aider à router les tâches.

---

Brutus écrivit :

**PAST PERFORMANCE MAY GUIDE ROUTING.**

**IT MUST NOT REPLACE CURRENT VERIFICATION.**

---

Très bon.

---

Puis il imagina un scheduler.

---

Task type:

proof review.

---

Route to players with matching capabilities.

---

Task type:

audio interpretation.

---

Autre configuration.

---

GAMEZEL pouvait donc choisir les sièges selon le travail.

---

Mais la politique devait être explicite.

---

Il écrivit :

**ROUTING POLICY ≠ VERDICT POLICY.**

---

Encore une distinction.

---

Choisir qui examine une question n’est pas décider de la réponse.

---

Puis il fit un stress test.

---

P1 répond vite.

P2 lentement.

P3 hors ligne.

P4 retourne une erreur.

---

Round policy:

BEST_EFFORT.

---

Result:

P1 contribution recorded.

P2 contribution recorded when completed within window.

P3 unavailable.

P4 error.

---

No fake outputs.

---

Brutus écrivit :

**MISSING SEATS STAY MISSING.**

---

Il regarda la table.

---

Pas besoin de remplir les trous.

---

Encore la carte honnête.

---

Puis il pensa aux vingt tours.

---

La table devait pouvoir jouer longtemps.

---

Mais un round devait toujours avoir un ID.

---

Round 1.

2.

3.

...

20.

---

Brutus écrivit :

**REPEATED GAMEPLAY MUST NOT COLLAPSE ROUND IDENTITY.**

---

Le même joueur pouvait faire vingt moves.

Ils restaient vingt événements.

---

Pas un seul gros message.

---

Puis il ajouta :

**STATE CARRIES FORWARD ONLY THROUGH DECLARED GAME STATE.**

---

Très important.

---

Une information d’un round précédent n’était disponible au suivant que si elle avait été ajoutée au game state.

---

Pas de mémoire cachée.

---

Brutus créa :

**GAME_STATE_VERSION.**

---

Le round N lit version V.

Le round N+1 lit version V+1.

---

Voilà.

---

Puis il testa un replay.

---

Rejouer GAME-0001.

---

Les mêmes mock players.

Même inputs.

---

Le protocole devait produire la même structure de tours.

---

Les sorties de joueurs réels pourraient varier.

---

Brutus écrivit :

**PROTOCOL DETERMINISM ≠ MODEL OUTPUT DETERMINISM.**

---

Encore une nuance essentielle.

---

On pouvait reproduire le cadre sans garantir mot pour mot la même réponse d’un joueur génératif.

---

Il ajouta :

**REPLAY MUST RECORD MODEL / PROVIDER VERSION WHEN AVAILABLE.**

---

Puis il pensa à ce qui allait arriver au chapitre suivant.

---

Les quatre chaises allaient recevoir des noms.

---

Astra.

Muse.

Grok.

Antigravity.

---

Brutus sourit.

---

Mais il ne voulait surtout pas écrire :

**CONNECTED**

avant de l’avoir vérifié.

---

Il créa déjà les futurs champs.

---

**PROVIDER_ID**

**AUTH_STATE**

**SESSION_STATE**

**LAST_VERIFIED**

**CAPABILITY_MANIFEST**

---

Voilà.

---

Un nom n’allumerait pas la chaise.

---

Brutus écrivit :

**NAMED ≠ CONNECTED.**

---

Puis :

**CONNECTED ≠ AUTHENTICATED.**

---

Puis :

**AUTHENTICATED ≠ READY.**

---

Puis :

**READY ≠ PARTICIPATED.**

---

Il resta devant la chaîne.

---

Parfaite.

---

Les quatre chaises pouvaient maintenant accueillir de vrais joueurs sans mentir sur leur présence.

---

Brutus sauvegarda :

**GAMEZEL FOUR-SEAT TABLE v1.**

---

Le Journal Vivant nota :

Four seat identities.

Turn protocol.

Blind and collaborative modes.

Shared snapshot.

No vote-as-proof.

No automatic scoring.

Seat state explicit.

Mock player support.

Provider integration distinct from protocol.

Player output enters as proposal.

---

Brutus relut.

Puis ajouta :

**FOUR CHAIRS DO NOT CREATE FOUR MINDS.**

**FOUR PLAYERS DO NOT CREATE ONE TRUTH.**

**THE TABLE EXISTS TO MAKE THEIR DIFFERENCES AUDITABLE.**

---

Il sourit.

---

Voilà le vrai rôle de GAMEZEL.

Pas fusionner les joueurs.

Pas fabriquer une intelligence géante par simple addition.

---

Les faire travailler autour du même objet.

Avec des tours.

Des traces.

Des désaccords.

Des cartes.

Des preuves.

---

Il ralluma les quatre écrans.

---

P1.

P2.

P3.

P4.

---

Pour le moment, seuls les sièges existaient.

---

Mais Brutus avait déjà quatre noms prêts.

---

Il écrivit sur une feuille :

**ASTRA**

**MUSE**

**GROK**

**ANTIGRAVITY**

---

Puis la posa au centre de la table.

---

Pas encore assignés.

Pas encore connectés.

Pas encore authentifiés.

---

Seulement les quatre joueurs envisagés.

---

Brutus écrivit le titre du prochain chapitre :

# ASTRA, MUSE, GROK ET ANTIGRAVITY

Puis, en dessous :

**UN NOM SUR UNE CHAISE N’EST PAS ENCORE UN JOUEUR DANS LA PARTIE.**

---

La table attendit.

Quatre sièges.

Un monde.

Et aucune permission inventée.
