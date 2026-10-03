# Chapitre 96 — Astra, Muse, Grok et Antigravity

Quatre chaises.

Quatre noms.

Une seule table.

Brutus resta debout devant GAMEZEL.

---

P1.

P2.

P3.

P4.

Les sièges existaient déjà.

Le protocole aussi.

Les tours.

Les traces.

Les snapshots.

Les cartes.

Les désaccords.

---

Il ne manquait plus que les noms.

Brutus prit la feuille déposée au centre de la table.

Il lut :

**ASTRA**

**MUSE**

**GROK**

**ANTIGRAVITY**

---

Puis il écrivit immédiatement :

**NAME ASSIGNMENT ≠ LIVE CONNECTION.**

---

Avant même de placer les noms.

---

Il connaissait le piège.

Une chaise pouvait porter un nom.

Une configuration pouvait contenir un provider ID.

Une interface pouvait afficher un logo.

Et pourtant :

aucune session réelle.

Aucune authentification.

Aucun appel réussi.

Aucun tour joué.

---

Brutus écrivit :

**NAMED ≠ CONFIGURED ≠ AUTHENTICATED ≠ READY ≠ PARTICIPATED.**

---

La chaîne resta au-dessus de la table.

C’était la règle du chapitre.

---

Il plaça le premier nom.

P1 :

**ASTRA**

---

Le siège s’illumina.

Mais Brutus arrêta immédiatement l’animation.

---

Pourquoi la chaise venait-elle de s’allumer ?

Parce qu’un nom avait été assigné.

Pas parce qu’Astra était réellement connectée.

---

Il corrigea.

---

Le siège reçut seulement une étiquette.

**SEAT_NAME = ASTRA**

---

État :

**CONFIGURED**

ou seulement :

**ASSIGNED**

selon ce qui était réellement connu.

---

Brutus écrivit :

**LABEL MAY CHANGE. SESSION STATE MUST NOT.**

---

Il fit la même chose.

P2 :

**MUSE**

P3 :

**GROK**

P4 :

**ANTIGRAVITY**

---

Puis la table afficha :

| Siège | Nom | Session |
|---|---|---|
| P1 | Astra | à vérifier |
| P2 | Muse | à vérifier |
| P3 | Grok | à vérifier |
| P4 | Antigravity | à vérifier |

---

Brutus regarda.

Voilà une table honnête.

---

Pas de vert automatique.

Pas de badge LIVE.

Pas de compteurs inventés.

---

Il écrivit :

**UNKNOWN CONNECTION STATE MUST REMAIN UNKNOWN UNTIL CHECKED.**

---

Puis il créa :

**PLAYER_BINDING**

avec :

**SEAT_ID**

**DISPLAY_NAME**

**PROVIDER_ID**

**AUTH_STATE**

**SESSION_STATE**

**CAPABILITY_MANIFEST**

**LAST_VERIFIED**

**TRACE_REF**

---

Brutus s’arrêta sur :

**LAST_VERIFIED**

---

Très important.

---

Une connexion vérifiée hier n’était pas nécessairement disponible maintenant.

---

Il écrivit :

**PAST CONNECTION ≠ CURRENT AVAILABILITY.**

---

Puis :

**CURRENT AVAILABILITY REQUIRES CURRENT EVIDENCE.**

---

La table devait apprendre à distinguer mémoire et présent.

---

Le chapitre 65 revenait encore.

---

Brutus prit Astra.

---

Que savait-il réellement ?

---

Astra était le nom donné au premier rôle du système.

Le siège pouvait être associé à l’opérateur principal de GAMEZEL.

Mais même là, il ne voulait pas transformer une convention narrative en preuve technique.

---

Il écrivit :

**ASTRA = PLAYER ROLE / BINDING NAME.**

Puis :

**ROLE NAME ≠ PROVIDER PROOF.**

---

La même discipline s’appliquait aux trois autres.

---

Muse.

Nom de joueur envisagé.

---

Grok.

Nom de joueur envisagé.

---

Antigravity.

Nom de joueur envisagé.

---

Brutus n’allait pas inventer un état de connexion.

---

Il créa trois états simples :

**UNVERIFIED**

**VERIFIED_AVAILABLE**

**VERIFIED_UNAVAILABLE**

---

Puis il ajouta :

**AUTH_REQUIRED**

---

Parce qu’un service pouvait être connu, accessible en théorie, mais nécessiter encore une authentification.

---

Brutus écrivit :

**KNOWN PROVIDER ≠ ACTIVE SESSION.**

---

Excellent.

---

Il imagina ensuite que Grok possédait un ancien login.

---

Même si une session avait déjà fonctionné auparavant, GAMEZEL devait vérifier l’état actuel avant un nouveau round.

---

Il écrivit :

**OLD SESSION ≠ CURRENT SESSION.**

---

Puis :

**AUTHENTICATION MUST NOT BE INFERRED FROM HISTORY.**

---

Même principe pour Muse.

Même principe pour Antigravity.

---

Brutus regarda les quatre sièges.

---

L’architecture devait pouvoir fonctionner dans tous les cas :

4 joueurs disponibles.

3 joueurs.

2 joueurs.

1 joueur.

0 joueur.

---

Il écrivit :

**TABLE STATE MUST BE VALID FOR EVERY AVAILABILITY COMBINATION.**

---

Puis il lança une simulation.

---

Astra :

READY.

Muse :

AUTH_PENDING.

Grok :

OFFLINE.

Antigravity :

UNVERIFIED.

---

La table devait-elle commencer ?

---

Cela dépendait de :

**ROUND_COMPLETION_POLICY.**

---

Si BEST_EFFORT :

oui.

---

Si ALL_PLAYERS_REQUIRED :

non.

---

Brutus écrivit :

**ROUND START DEPENDS ON POLICY, NOT OPTIMISM.**

---

Puis il plaça quatre indicateurs.

---

Pas des gros voyants dramatiques.

---

Seulement :

**READY**

**AUTH_PENDING**

**OFFLINE**

**UNVERIFIED**

---

Brutus sourit.

---

C’était beaucoup plus utile qu’un simple :

CONNECTED / NOT CONNECTED.

---

Puis il pensa aux capacités.

---

Même si quatre joueurs étaient disponibles, ils n’étaient pas forcément interchangeables.

---

Astra pouvait avoir accès à certains outils.

Muse à d’autres.

Grok à d’autres.

Antigravity à d’autres.

---

Brutus écrivit :

**PLAYER IDENTITY ≠ CAPABILITY SET.**

---

Il créa :

**CAPABILITY_MANIFEST**

pour chaque siège.

---

Possible examples :

TEXT_REASONING.

CODE_ANALYSIS.

WEB_ACCESS.

FILE_ACCESS.

AUDIO_ANALYSIS.

MATH_TOOLING.

IMAGE_INPUT.

LONG_CONTEXT.

---

Brutus n’assigna rien qu’il ne pouvait vérifier.

---

Il écrivit :

**CAPABILITIES MUST COME FROM VERIFIED SESSION METADATA OR DECLARED CONFIGURATION.**

---

Pas de prestige.

Pas de réputation.

---

Seulement ce que le système savait.

---

Puis il pensa au routage.

---

GAMEZEL devait choisir le joueur selon la tâche.

---

Mais si les capacités changent ?

---

Une nouvelle version du fournisseur.

Une session différente.

Un outil désactivé.

---

Il ajouta :

**CAPABILITY_VERSION**

et :

**VERIFIED_AT**

---

Brutus écrivit :

**ROUTING MUST USE CURRENT CAPABILITY STATE.**

---

Encore.

---

Le temps.

Toujours le temps.

---

Puis il créa un test.

---

Task :

exact integer arithmetic.

---

Supposons que P1 dispose d’un outil exact.

P2 non.

---

Le scheduler peut préférer P1.

---

Mais si P1 est indisponible ?

---

P2 peut peut-être produire une analyse.

---

Seulement :

la trace doit dire qu’aucun outil exact n’a été utilisé.

---

Brutus écrivit :

**FALLBACK MUST LOWER CLAIM SCOPE WHEN TOOLING CHANGES.**

---

Très important.

---

Une réponse sans outil exact ne devait pas recevoir le même statut qu’une vérification exacte.

---

Il ajouta :

**METHOD FOLLOWS CAPABILITY.**

---

Puis il imagina un round de créativité.

---

Là, les différences de style pouvaient être utiles.

---

Un joueur propose.

Un autre critique.

Un autre cherche un angle différent.

Un autre synthétise.

---

Brutus créa :

**ROLE_ASSIGNMENT**

---

GENERATOR.

CRITIC.

COUNTEREXAMPLE_HUNTER.

SYNTHESIZER.

---

Puis il écrivit :

**SEAT ≠ FIXED ROLE.**

---

Très important.

---

Astra n’était pas forcément toujours génératrice.

Muse pas toujours créatrice.

Grok pas toujours critique.

Antigravity pas toujours explorateur.

---

Le rôle devait dépendre du round.

---

Brutus écrivit :

**PLAYER NAME MUST NOT BECOME A STEREOTYPE.**

---

Il sourit.

---

Le protocole devait rester supérieur aux personnages.

---

Puis il pensa à une autre erreur.

---

Un joueur pouvait répondre :

« j’ai vérifié ».

---

Cela ne suffisait pas.

---

GAMEZEL devait enregistrer :

quelle méthode ?

quels outils ?

quelle source ?

quel résultat ?

---

Brutus écrivit :

**SELF-REPORTED VERIFICATION ≠ VERIFIED TRACE.**

---

Même règle pour tous les joueurs.

---

Il ajouta :

**MOVE_EVIDENCE**

---

Tool calls.

Artifacts.

Calculations.

Source refs.

Trace refs.

---

Si absents :

claim remains proposal.

---

Brutus écrivit :

**PLAYER CONFIDENCE ≠ SYSTEM CONFIDENCE.**

---

Puis il corrigea encore.

---

Même « system confidence » pouvait être trop vague.

---

Il remplaça :

**PLAYER CONFIDENCE ≠ CLAIM STATUS.**

---

Mieux.

---

Un joueur pouvait dire :

99 % sûr.

---

Le statut de la claim pouvait rester :

UNVERIFIED.

---

Brutus sourit.

---

La table ne devait pas être hypnotisée par le ton.

---

Il écrivit :

**ELOQUENCE ≠ EVIDENCE.**

---

Puis :

**CERTAINTY OF LANGUAGE ≠ CERTAINTY OF RESULT.**

---

Cette règle lui plut.

---

GAMEZEL pouvait recevoir quatre styles très différents.

---

L’un sec.

L’un créatif.

L’un très confiant.

L’un très prudent.

---

Il fallait comparer leurs contenus.

Pas leurs personnalités.

---

Brutus créa :

**NORMALIZED MOVE VIEW**

---

Claim.

Evidence.

Assumptions.

Unknowns.

Counterexample attempt.

Trace.

---

La prose complète restait accessible.

Mais la comparaison utilisait un schéma commun.

---

Il écrivit :

**NORMALIZE STRUCTURE, NOT THOUGHT.**

---

Très important.

---

GAMEZEL ne devait pas forcer quatre joueurs à penser pareil.

Seulement à livrer des objets comparables.

---

Puis il imagina le premier vrai round nominal.

---

Task :

analyze candidate relation.

---

Round mode :

BLIND_PARALLEL.

---

Same snapshot.

Same task.

Same output schema.

---

Seats :

Astra.

Muse.

Grok.

Antigravity.

---

Mais GAMEZEL vérifia d’abord :

Astra READY?

Muse READY?

Grok READY?

Antigravity READY?

---

Brutus écrivit :

**CHECK SEAT BEFORE DISPATCH.**

---

Pas de requête envoyée à un joueur OFFLINE.

---

Pas de timeout inutile.

---

Pas de résultat fictif.

---

Un siège indisponible devenait :

**SKIPPED_UNAVAILABLE**

---

Pas :

FAILED_ANALYSIS.

---

Très important.

---

Un joueur indisponible n’avait pas échoué à résoudre le problème.

Il n’avait pas participé.

---

Brutus écrivit :

**AVAILABILITY FAILURE ≠ REASONING FAILURE.**

---

Voilà une nuance importante.

---

Puis il pensa aux timeouts.

---

Un joueur démarre.

Mais ne répond pas dans la fenêtre.

---

Status :

TIMEOUT.

---

Cela signifiait-il que la réponse était mauvaise ?

---

Non.

---

Il écrivit :

**TIMEOUT ≠ INCORRECT.**

---

Seulement :

no completed contribution within deadline.

---

Encore le scope.

---

Puis il pensa aux retries.

---

Un provider retourne une erreur réseau.

---

Retry ?

Peut-être.

---

Mais pas avec le même TURN_ID comme nouvel événement ?

---

Brutus réfléchit.

---

Le turn reste le même.

Les tentatives ont leurs propres IDs.

---

Il créa :

**ATTEMPT_ID.**

---

TURN-0004.

ATTEMPT-1.

ATTEMPT-2.

---

Brutus écrivit :

**RETRY ≠ NEW TURN.**

---

Très bon.

---

Mais si la seconde tentative utilise un snapshot différent ?

---

Non.

---

Elle doit utiliser le même ROUND_SNAPSHOT_ID pour rester le même tour.

---

Sinon :

nouveau turn.

---

Brutus écrivit :

**RETRY MUST PRESERVE INPUT IDENTITY.**

---

Encore la discipline du chapitre 79.

---

Puis il pensa au coût.

---

Quatre joueurs.

Vingt rounds.

Longues sorties.

---

Cela pouvait devenir énorme.

---

Il ajouta :

**RESOURCE BUDGET PER PLAYER**

---

Calls.

Tokens.

Compute.

Tool time.

---

Pas pour favoriser un joueur.

Pour rendre le round reproductible et borné.

---

Il écrivit :

**UNBOUNDED AGENT ≠ FAIR PARTICIPANT.**

---

Puis il pensa à l’ordre.

---

Si Astra reçoit davantage de contexte que Muse, leurs résultats ne sont plus comparables.

---

Il écrivit :

**INPUT PARITY MUST BE RECORDED.**

---

Parité ne signifiait pas outils identiques.

---

Mais le système devait savoir :

même prompt ?

même snapshot ?

mêmes documents ?

mêmes restrictions ?

---

Brutus créa :

**INPUT_MANIFEST_HASH.**

---

Voilà.

---

Chaque siège pouvait recevoir une empreinte du paquet d’entrée.

---

Si les hashes diffèrent :

comparison flagged.

---

Il écrivit :

**DIFFERENT INPUTS → DIFFERENT EXPERIMENT.**

---

Très important.

---

Puis il pensa aux sorties.

---

Supposons que trois joueurs convergent sur A.

Le quatrième propose B.

---

GAMEZEL ne devait pas écraser B.

---

Il devait demander :

pourquoi ?

---

Brutus créa :

**MINORITY REPORT**

---

Pas comme privilège.

Comme conservation du désaccord.

---

Il écrivit :

**MINORITY ≠ ERROR.**

---

Une seule voix pouvait avoir trouvé le vrai contre-exemple.

---

Très important.

---

Puis il imagina l’inverse.

---

Un joueur produit une réponse totalement sans trace.

Trois autres produisent des objets vérifiables.

---

Le système pouvait afficher les quatre.

Mais le poids opérationnel des contributions devait dépendre de leur support.

---

Brutus écrivit :

**EVIDENCE QUALITY MAY DIFFER EVEN WHEN OUTPUT FORMAT MATCHES.**

---

Pas besoin d’un score global.

---

Il ajouta :

**EVIDENCE_CLASS**

NONE.

SELF_REPORT.

DERIVED_TRACE.

TOOL_VERIFIED.

EXTERNALLY_REPRODUCED.

---

Mais attention.

---

Même TOOL_VERIFIED ne signifiait pas theorem.

---

Il écrivit :

**EVIDENCE CLASS ≠ CLAIM TRUTH.**

---

Toujours.

---

Brutus regarda les quatre noms.

---

Astra.

Muse.

Grok.

Antigravity.

---

Il les aimait.

---

Mais il ne voulait pas que la narration déforme l’architecture.

---

Il écrivit en haut de la table :

**THE NAMES ARE HUMAN-FRIENDLY. THE CONTRACTS ARE MACHINE-FRIENDLY.**

---

Voilà.

---

Puis il assigna les quatre noms dans la configuration.

---

P1 → Astra.

P2 → Muse.

P3 → Grok.

P4 → Antigravity.

---

Mais les états restèrent indépendants.

---

Astra :

ASSIGNED.

Muse :

ASSIGNED.

Grok :

ASSIGNED.

Antigravity :

ASSIGNED.

---

Rien de plus.

---

Brutus sourit.

---

Enfin, il pouvait donner un nom sans fabriquer une connexion.

---

Il écrivit :

**ASSIGNMENT COMPLETE. PROVIDER STATE UNCHANGED.**

---

Puis il imagina un futur où les quatre seraient réellement READY.

---

La table pourrait lancer :

**ROUND-0042**

---

Même snapshot.

Quatre contributions.

Barrier.

Comparison.

Disagreement extraction.

Cards.

Journal.

---

Mais tant que les connexions n’étaient pas vérifiées :

pas de faux round.

---

Brutus écrivit :

**ARCHITECTURE MAY BE READY BEFORE PROVIDERS ARE READY.**

---

Très important.

---

Un système peut être complètement construit sans que tous les acteurs externes soient branchés.

---

Il ajouta :

**DESIGN COMPLETION ≠ INTEGRATION COMPLETION.**

---

Le chapitre 95 parlait déjà de cela.

Maintenant, le principe devenait central.

---

Brutus pensa au déploiement.

---

GAMEZEL pouvait être lancé sur un serveur.

---

Mais si le provider externe dépendait d’un login local ou d’une session navigateur, le siège n’était pas réellement autonome.

---

Il écrivit :

**SERVER DEPLOYED ≠ PROVIDER AUTONOMY.**

---

Puis :

**PROVIDER SESSION DEPENDENCY MUST BE EXPLICIT.**

---

Voilà.

---

Si un joueur nécessitait :

browser login.

local bridge.

manual token refresh.

desktop app.

---

La table devait le savoir.

---

Il ajouta :

**SESSION_DEPENDENCIES**

---

Brutus sourit.

---

Le chapitre ne prétendrait pas que le laboratoire était autonome avant que la preuve opérationnelle existe.

---

Il écrivit :

**AUTONOMOUS ROUND REQUIRES AUTONOMOUSLY AVAILABLE PLAYERS.**

---

Pas quatre noms.

Pas quatre logos.

Quatre sessions réellement utilisables selon la politique du round.

---

Puis il pensa à la persistance.

---

Si GAMEZEL redémarre, les noms doivent revenir.

---

Oui.

---

Mais les sessions ?

Pas forcément.

---

Très important.

---

Il écrivit :

**PERSIST PLAYER BINDING. REVALIDATE PLAYER SESSION.**

---

Voilà.

---

Après restart :

P1 still Astra.

P2 still Muse.

P3 still Grok.

P4 still Antigravity.

---

Mais states:

UNVERIFIED until checked.

---

Brutus écrivit :

**RESTART MUST NOT RESURRECT EXPIRED AUTH.**

---

Encore le chapitre 65.

---

Puis il imagina qu’un provider change de modèle.

---

Même nom.

Nouvelle version.

---

Les résultats pourraient différer.

---

Il ajouta :

**MODEL_VERSION**

**PROVIDER_VERSION**

si disponibles.

---

Brutus écrivit :

**SAME PLAYER NAME ≠ SAME MODEL INSTANCE.**

---

Très important.

---

Une partie historique devait savoir quel modèle avait réellement joué.

---

Sinon impossible de reproduire ou comparer proprement.

---

Il pensa aussi aux paramètres.

---

Temperature.

Reasoning mode.

Tool access.

System instructions.

---

Si pertinents et disponibles :

ils appartenaient au contexte du turn.

---

Il créa :

**PLAYER_RUNTIME_PROFILE.**

---

Brutus écrivit :

**OUTPUT DEPENDS ON RUNTIME CONTEXT.**

---

Pas seulement sur le nom du joueur.

---

Puis il regarda la table.

---

Elle était maintenant prête à recevoir des êtres très différents.

---

Mais elle ne se souciait pas de leur prestige.

---

Elle demandait seulement :

Qui es-tu ?

Es-tu authentifié ?

Es-tu disponible ?

Quelles capacités sont vérifiées ?

Quel snapshot as-tu reçu ?

Qu’as-tu produit ?

Avec quelles traces ?

---

Brutus sourit.

---

Voilà une vraie table.

---

Pas une réunion de logos.

---

Il écrivit :

**GAMEZEL DOES NOT TRUST BRAND. IT TRUSTS TRACEABLE PARTICIPATION.**

---

Puis il se corrigea encore.

---

Même « trust » devait rester scoped.

---

Il remplaça :

**GAMEZEL RECORDS TRACEABLE PARTICIPATION.**

---

Parfait.

---

Puis il ouvrit le Journal Vivant.

---

Une entrée par siège :

**SEAT_BINDING_EVENT**

P1 → Astra.

P2 → Muse.

P3 → Grok.

P4 → Antigravity.

---

Pas de connexion annoncée.

Seulement l’assignation.

---

Brutus écrivit :

**NAME ASSIGNMENT RECORDED.**

---

Puis un second type d’événement :

**SESSION_VERIFICATION_EVENT**

---

Celui-là ne serait créé que lorsqu’une vraie vérification aurait lieu.

---

Il sourit.

---

Enfin les choses pouvaient progresser sans se mélanger.

---

Il ajouta :

**BINDING HISTORY ≠ SESSION HISTORY.**

---

Encore deux lignées.

---

Puis il pensa à la prochaine étape.

---

Les joueurs allaient bientôt produire des cartes.

---

Une proposition.

Une hypothèse.

Un contre-test.

Une formule.

---

Mais chaque carte devrait garder :

qui l’avait produite.

dans quel round.

avec quelle entrée.

sous quel modèle.

avec quelles traces.

---

Brutus regarda le chapitre 97 qui approchait.

---

**LES CARTES QUI LAISSENT DES REÇUS.**

---

Il sourit.

---

Évidemment.

---

Si quatre joueurs allaient contribuer au même monde, leurs productions devaient être capables de dire :

**je viens de là.**

---

Brutus sauvegarda :

**GAMEZEL PLAYER BINDINGS v1.**

---

Le Journal Vivant nota :

Four named seats.

No provider availability invented.

Auth state separate from name.

Capabilities versioned.

Retries tracked.

Input parity recorded.

Player output remains proposal.

Minority outputs preserved.

Restart requires revalidation.

---

Brutus relut.

Puis ajouta les invariants :

**NAMED ≠ CONNECTED.**

**CONNECTED ≠ AUTHENTICATED.**

**AUTHENTICATED ≠ READY.**

**READY ≠ PARTICIPATED.**

**PARTICIPATED ≠ CORRECT.**

**AGREEMENT ≠ PROOF.**

**PLAYER CONFIDENCE ≠ CLAIM STATUS.**

**BRAND ≠ AUTHORITY.**

---

Il resta devant le dernier.

---

Oui.

---

Astra.

Muse.

Grok.

Antigravity.

---

Quatre noms puissants.

Quatre chaises possibles.

Mais GAMEZEL ne leur donnerait jamais plus de pouvoir que leurs traces et leurs contrats n’en permettaient.

---

Brutus éteignit les indicateurs.

---

Les quatre noms restèrent sur les dossiers.

Pas comme preuves de présence.

Comme destinations possibles.

---

Puis il ouvrit une boîte vide au centre de la table.

---

Elle portait une inscription :

**CARDS**

---

Brutus prit une carte blanche.

---

Au recto :

un résultat.

---

Au verso :

qui l’avait produit.

quand.

dans quel round.

avec quelle source.

avec quel état.

avec quelle trace.

---

Il sourit.

---

Voilà ce qui allait empêcher les idées de perdre leur histoire.

---

Il écrivit le prochain titre :

# LES CARTES QUI LAISSENT DES REÇUS

Puis une dernière ligne :

**A CONTRIBUTION WITHOUT PROVENANCE IS ONLY A PIECE OF TEXT.**

---

Les quatre chaises attendaient toujours.

Mais maintenant, même lorsqu’elles commenceraient à parler, aucune de leurs paroles ne pourrait entrer dans Brutus sans laisser de trace.
