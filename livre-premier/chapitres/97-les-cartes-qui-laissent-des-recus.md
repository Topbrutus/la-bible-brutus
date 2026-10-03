# Chapitre 97 — Les cartes qui laissent des reçus

Au centre de la table, la boîte était vide.

Une seule inscription :

**CARDS**

Brutus prit la première carte blanche.

---

Au recto :

rien.

---

Au verso :

rien.

---

Il sourit.

C’était exactement comme cela qu’elle devait commencer.

---

Pas de prétention.

Pas de statut.

Pas d’origine inventée.

---

Seulement un objet vide, prêt à recevoir une contribution.

---

Brutus écrivit :

**A CARD STARTS EMPTY.**

Puis :

**A CARD EARNS CONTENT THROUGH AN EVENT.**

---

Voilà.

---

Une carte ne devait jamais apparaître dans GAMEZEL comme si elle avait toujours existé.

Elle devait avoir une naissance.

---

Un événement.

---

Un joueur.

Un tour.

Un snapshot.

Une sortie.

---

Brutus créa :

**CARD_CREATION_EVENT**

---

Puis ajouta :

**CARD_ID**

**SOURCE_MOVE_ID**

**ROUND_ID**

**SEAT_ID**

**PLAYER_BINDING_REF**

**INPUT_SNAPSHOT_ID**

**CREATED_AT**

**TRACE_REF**

---

Il regarda la liste.

---

La carte avait déjà une identité avant même son contenu.

---

Il écrivit :

**CARD IDENTITY ≠ CARD CONTENT.**

---

Très important.

---

Deux cartes pouvaient contenir exactement le même texte.

Mais provenir de deux tours différents.

---

Elles n’étaient donc pas nécessairement le même objet historique.

---

Encore le chapitre 65.

---

Même valeur.

Pas le même événement.

---

Brutus prit deux cartes.

---

Carte A :

« tester q71 séparément ».

---

Carte B :

« tester q71 séparément ».

---

Même phrase.

---

Mais A venait d’Astra.

B venait d’un autre siège.

---

Brutus écrivit :

**SAME TEXT ≠ SAME CONTRIBUTION.**

---

Puis il ajouta :

**CONTENT_HASH**

et

**CARD_ID**

séparément.

---

Voilà.

---

Un hash pouvait montrer que le contenu était identique.

Mais pas fusionner les histoires.

---

Brutus créa une relation :

**CONTENT_EQUIVALENT**

---

Pas :

SAME_CARD.

---

Il sourit.

---

Le laboratoire devenait incapable d’écraser deux découvertes simplement parce qu’elles se ressemblaient.

---

Puis il pensa au recto de la carte.

---

Que devait-il afficher ?

---

Peut-être :

une formule.

une hypothèse.

un contre-test.

un résultat.

une observation.

un artefact.

---

Brutus créa :

**CARD_TYPE**

---

FORMULA.

HYPOTHESIS.

COUNTERTEST.

RESULT.

OBSERVATION.

ARTIFACT.

QUESTION.

WARNING.

---

Puis il ajouta :

**STATUS**

---

PROPOSED.

UNDER_REVIEW.

ADMITTED.

REJECTED.

SUPERSEDED.

UNRESOLVED.

---

Brutus écrivit :

**TYPE ≠ STATUS.**

---

Encore une séparation.

---

Une carte pouvait être de type FORMULA.

Mais statut PROPOSED.

---

Une carte pouvait être de type WARNING.

Et statut ADMITTED.

---

Une carte pouvait être de type RESULT.

Et statut UNRESOLVED.

---

Il écrivit :

**WHAT IT IS ≠ WHAT WE CURRENTLY THINK OF IT.**

---

Très important.

---

Puis il retourna la carte.

---

Voilà le verso.

---

Le verso devait contenir le reçu.

---

Brutus écrivit :

**RECEIPT**

---

Puis les champs.

**PLAYER**

**TURN**

**ROUND**

**INPUT**

**OUTPUT TRACE**

**TOOLS USED**

**MODEL / PROVIDER VERSION**

**CLAIM SCOPE**

**EVIDENCE REFS**

---

Il regarda.

---

Une carte sans verso pouvait être jolie.

Mais elle serait inutilisable pour l’audit.

---

Il écrivit :

**FRONT = CONTRIBUTION.**

**BACK = PROVENANCE.**

---

Voilà le cœur.

---

Recto montre l’idée.

Verso explique d’où elle vient.

---

Brutus sourit en voyant le parallèle.

---

Encore Recto et Verso.

---

Même les cartes apprenaient la même architecture.

---

Il écrivit :

**CARD RECTO PRESENTS. CARD VERSO ACCOUNTS.**

---

Puis il se corrigea.

---

Le verso de la carte n’était pas le Verso gardien du Tombeau.

Même nom imagé.

Rôle différent.

---

Il ajouta :

**CARD BACK ≠ VERSO GATEKEEPER.**

---

Toujours éviter les collisions de métaphores.

---

Puis il créa la première vraie carte.

---

**CARD-0001**

Type :

QUESTION.

---

Recto :

**La porte 71 possède-t-elle son propre témoin valide sous le contrat exact requis ?**

---

Verso :

Source move :

P1.

Round :

GAMEZEL-0001.

Snapshot :

S-0001.

Status :

PROPOSED.

Claim scope :

Gate 71 only.

---

Brutus sourit.

---

Cette carte était parfaite.

Pourquoi ?

Parce qu’elle ne prétendait pas répondre à la question.

---

Elle conservait la question.

---

Il écrivit :

**A QUESTION CAN BE A FIRST-CLASS RESEARCH OBJECT.**

---

Très important.

---

Toutes les cartes n’avaient pas besoin d’être des réponses.

---

Une bonne question pouvait survivre plusieurs rounds.

---

Puis il créa :

**CARD-0002**

Type :

COUNTERTEST.

---

Recto :

**Refuser toute dérivation q47 → q71 sans identité explicite.**

---

Verso :

source chapter logic.

method.

reason.

status.

---

Brutus regarda les deux cartes.

---

Elles étaient maintenant reliées.

---

CARD-0002 :

**SUPPORTS_REVIEW_OF**

CARD-0001.

---

Il créa une edge.

---

Puis s’arrêta.

---

Une carte ne devait pas pouvoir relier une autre par simple texte.

---

Il fallait une relation typée.

---

Il écrivit :

**CARD EDGE = CLAIM TOO.**

---

Le chapitre 93 revenait.

---

Il ajouta :

**CARD_EDGE_ID**

**EDGE_TYPE**

**FROM_CARD**

**TO_CARD**

**RULE_REF**

**TRACE_REF**

---

Voilà.

---

Le jeu produisait maintenant un petit graphe de cartes.

---

Brutus sourit.

---

Une partie n’était plus une conversation.

Elle devenait une construction d’objets reliés.

---

Il écrivit :

**GAME TRANSCRIPT ≠ GAME KNOWLEDGE GRAPH.**

---

Très important.

---

Le transcript racontait tout ce qui avait été dit.

---

Les cartes sélectionnaient ce qui méritait de rester comme objet manipulable.

---

Mais attention.

---

Sélectionner une carte ne signifiait pas la valider.

---

Brutus écrivit :

**CARD CREATION ≠ CARD PROMOTION.**

---

Puis :

**CARD EXISTENCE ≠ CARD CORRECTNESS.**

---

Encore.

---

Une mauvaise idée pouvait devenir une carte.

Et c’était utile.

---

Il créa une carte :

**CARD-0003**

Type :

HYPOTHESIS.

Status :

REJECTED.

---

Recto :

**Peut-on dériver le témoin 71 à partir d’un objet 47 par division ?**

---

Verso :

rejected under derivation contract.

missing identity.

source chapter 85.

---

Brutus sourit.

---

Voilà une carte précieuse.

---

Pas parce qu’elle était correcte.

Parce qu’elle empêchait le laboratoire de refaire la même erreur.

---

Il écrivit :

**REJECTED CARD ≠ USELESS CARD.**

---

Puis :

**NEGATIVE KNOWLEDGE DESERVES RECEIPTS TOO.**

---

La boîte commençait à se remplir.

---

Questions.

Hypothèses.

Tests.

Rejets.

Résultats.

---

Brutus pensa aux prochaines parties.

---

Comment un joueur pouvait-il réutiliser une carte ?

---

Il ne devait pas copier simplement son texte.

---

Il devait référencer la carte.

---

Brutus créa :

**CARD_REF**

---

Un move futur pouvait dire :

uses CARD-0002.

---

La lignée devenait :

CARD-0002

→ TURN-0014

→ CARD-0048.

---

Brutus écrivit :

**REUSE MUST PRESERVE SOURCE IDENTITY.**

---

Pas de copier-coller sans provenance.

---

Puis il imagina une carte devenue obsolète.

---

Une formule change.

---

Toutes les cartes qui en dépendent doivent-elles disparaître ?

---

Non.

---

Le chapitre 95 avait déjà répondu.

---

Brutus écrivit :

**STALE ≠ DELETED.**

---

Il ajouta :

**DEPENDENCY_STATE**

CURRENT.

STALE.

INVALIDATED.

REVIEW_REQUIRED.

---

Puis :

**STALE_REASON**

---

Brutus sourit.

---

Une carte pouvait maintenant survivre à son propre vieillissement.

---

Il écrivit :

**A CARD MAY REMAIN HISTORICALLY VALID WHILE BECOMING OPERATIONALLY STALE.**

---

Très important.

---

Une ancienne mesure pouvait être correcte pour la version de l’époque.

Mais plus applicable à la version actuelle.

---

Brutus pensa aux snapshots.

---

La carte devait donc garder :

**INPUT_SNAPSHOT_ID**

et éventuellement :

**DEPENDENCY_VERSION_SET**

---

Voilà.

---

Impossible désormais de prétendre qu’une vieille carte s’appliquait automatiquement au présent.

---

Il écrivit :

**OLD CARD + NEW WORLD = REVALIDATION REQUIRED.**

---

Puis il imagina une partie de vingt rounds.

---

Des dizaines de cartes.

---

Comment éviter une montagne illisible ?

---

Il créa des piles.

---

FORMULAS.

QUESTIONS.

WARNINGS.

TESTS.

RESULTS.

---

Mais une carte ne devait pas changer d’identité lorsqu’elle changeait de pile.

---

Brutus écrivit :

**COLLECTION ≠ IDENTITY.**

---

Un classement n’était pas une transformation de l’objet.

---

Il ajouta :

**COLLECTION_MEMBERSHIP**

---

Une carte pouvait même apparaître dans plusieurs collections.

---

Par exemple :

CARD-0003.

HYPOTHESES.

REJECTED.

GATE-71.

---

Brutus écrivit :

**ONE CARD MAY HAVE MANY INDEXES.**

---

Mais une seule identité canonique.

---

Encore.

---

Puis il pensa aux cartes physiques.

---

Une carte a deux faces.

Mais dans le système, le reçu pourrait devenir énorme.

---

Model version.

Tools.

Sources.

Trace.

Artifacts.

---

Impossible d’imprimer tout cela au dos.

---

Il créa :

**RECEIPT_SUMMARY**

et

**FULL_RECEIPT_REF.**

---

Brutus écrivit :

**SHORT RECEIPT ≠ FULL PROVENANCE.**

---

Le dos montrait assez pour comprendre l’origine.

Le full receipt ouvrait la trace complète.

---

Comme le Witness Viewer.

---

Toujours la même structure :

résumé.

puis profondeur.

---

Brutus sourit.

---

Le système entier commençait à converger vers une architecture uniforme.

---

Il prit une carte produite par un joueur.

---

Supposons :

Astra propose une formule.

---

Recto :

\[
F(n)=...
\]

---

Verso :

Astra.

Round 7.

Turn 2.

Model version.

Input snapshot.

Tools.

No independent validation yet.

---

Brutus ajouta sur le bord :

**PROPOSED**

---

Pas de couleur de victoire.

---

Puis Muse propose la même formule indépendamment dans un blind round.

---

Deux cartes.

---

Même formule.

---

Deux origines.

---

Brutus écrivit :

**INDEPENDENT DUPLICATION IS EVIDENCE ABOUT REPRODUCIBILITY, NOT PROOF BY ITSELF.**

---

Très important.

---

Il créa :

**INDEPENDENT_MATCH**

comme relation.

---

Mais seulement si le protocole de blind round garantissait réellement l’indépendance.

---

Sinon :

**CORRELATED_MATCH.**

---

Brutus sourit.

---

Même les accords pouvaient maintenant avoir un type.

---

Il écrivit :

**MATCH QUALITY DEPENDS ON CONTEXT SHARING.**

---

Puis il pensa à une carte générée après avoir vu une autre.

---

Muse lit la carte d’Astra et l’améliore.

---

La nouvelle carte devait avoir :

**DERIVED_FROM_CARD**

---

Pas INDEPENDENT_MATCH.

---

Voilà.

---

Brutus écrivit :

**INFLUENCE MUST BE VISIBLE IN LINEAGE.**

---

Le système pouvait désormais répondre :

qui a pensé quoi en premier ?

---

Pas au sens philosophique absolu.

Mais au sens de l’historique de GAMEZEL.

---

Brutus ajouta :

**SEEN_CONTEXT_REFS**

---

Très important.

---

Si un joueur avait vu une carte avant de produire la sienne, cela devenait une donnée.

---

Il écrivit :

**VISIBLE PRIOR ART IS PART OF THE EXPERIMENT.**

---

Puis il pensa à la publication.

---

Une carte pouvait devenir assez solide pour sortir de GAMEZEL.

---

Par exemple :

un résultat validé.

---

Mais elle ne devait pas quitter la table en perdant son reçu.

---

Brutus écrivit :

**EXPORT MUST INCLUDE PROVENANCE CAPSULE.**

---

Il créa :

**CARD EXPORT PACKET**

---

CARD_ID.

CONTENT.

STATUS.

CLAIM_SCOPE.

LINEAGE.

EVIDENCE.

RECEIPT_HASH.

FULL_TRACE_REF.

---

Voilà.

---

Une carte exportée devenait portable.

---

Mais le laboratoire devait toujours pouvoir dire :

voici d’où elle vient.

---

Brutus écrivit :

**PORTABILITY WITHOUT PROVENANCE CREATES ORPHANS.**

---

Il n’aimait pas les orphelins.

---

Les objets sans origine étaient difficiles à défendre.

---

Puis il pensa à une capture d’écran d’une carte.

---

Très dangereuse.

---

Une image du recto pouvait circuler sans le verso.

---

Brutus écrivit :

**SCREENSHOT ≠ CARD.**

---

Puis :

**CARD IMAGE ≠ CARD RECEIPT.**

---

Voilà.

---

Une capture pouvait être utile pour montrer.

Mais pas pour auditer.

---

Il ajouta un petit identifiant visible sur le recto :

**CARD_ID**

et

**STATUS**

---

Ainsi, même une capture pouvait au moins pointer vers l’objet canonique.

---

Brutus écrivit :

**DISPLAY SHOULD LEAVE A PATH BACK TO SOURCE.**

---

Encore la machine à traces.

---

Puis il pensa à une carte falsifiée.

---

Quelqu’un change le texte.

Garde le même CARD_ID.

---

Le hash ne correspond plus.

---

Brutus créa :

**CARD_CONTENT_HASH.**

---

À l’ouverture :

verify.

---

Mismatch :

**TAMPERED COPY.**

---

Brutus sourit.

---

Mais il écrivit immédiatement :

**HASH MATCH ≠ CARD CORRECTNESS.**

---

Toujours.

---

L’intégrité protégeait le contenu après création.

Pas la vérité du contenu.

---

Encore le chapitre 82.

---

Il ajouta :

**RECEIPT_HASH**

séparément.

---

Ainsi :

content hash.

receipt hash.

---

Pourquoi deux ?

---

Parce qu’on pouvait éventuellement conserver le même contenu avec un nouveau statut ou une annotation de revue.

---

Brutus réfléchit.

---

Mais modifier le statut ne devait pas réécrire le reçu original.

---

Il créa :

**CARD_STATE_EVENTS**

---

CREATE.

REVIEW.

PROMOTE.

REJECT.

SUPERSEDE.

STALE.

REVALIDATE.

---

Chaque changement ajoutait un événement.

---

La carte ne perdait jamais son historique.

---

Brutus écrivit :

**CURRENT CARD STATUS = FOLD OF STATE EVENTS.**

---

Il sourit.

---

Très propre.

---

Pas de champ mutable sans histoire.

---

Puis il pensa à la promotion.

---

Qu’est-ce qui transforme :

PROPOSED

en

ADMITTED ?

---

Une décision externe.

---

Jamais la carte elle-même.

---

Il écrivit :

**CARD CANNOT PROMOTE ITSELF.**

---

Encore le Tombeau.

---

Une politique de promotion devait vérifier :

type.

scope.

evidence.

review.

dependencies.

---

Puis créer :

**CARD_PROMOTION_EVENT**

---

Brutus écrivit :

**PROMOTION IS AN EVENT, NOT A COLOR CHANGE.**

---

Excellent.

---

Le vert, blanc ou badge venait ensuite.

---

Pas l’inverse.

---

Puis il prit une carte de type RESULT.

---

Supposons qu’elle contienne :

137 305 candidats premiers.

---

Le chiffre était correct dans une campagne donnée.

---

Mais sans scope :

dangereux.

---

Brutus ajouta :

**SCOPE**

\[
X=2\,000\,000
\]

odd \(t\).

corridor.

model version.

---

Il écrivit :

**RESULT CARD MUST CARRY ITS DOMAIN.**

---

Pas seulement la réponse.

---

Puis il pensa aux nombres 369 et 396.

---

Une carte pouvait dire :

**difference = 27.**

---

Mais le verso devait préciser :

integer comparison ?

frequency experiment ?

synthetic pair ?

---

Brutus écrivit :

**SAME FORMULA MAY SUPPORT DIFFERENT CARDS UNDER DIFFERENT SEMANTICS.**

---

Voilà.

---

\[
396-369=27
\]

était exact arithmétiquement.

---

Mais une carte audio devait aussi porter :

UNIT = Hz.

SOURCE = synthetic test.

---

Encore le contexte.

---

Brutus sourit.

---

Les cartes forçaient désormais le laboratoire à mettre le contexte là où il était impossible de l’oublier.

---

Puis il imagina une partie avec quatre joueurs.

---

Astra produit 3 cartes.

Muse 2.

Grok 5.

Antigravity 1.

---

Devait-on dire que Grok avait mieux joué ?

---

Non.

---

Brutus écrivit :

**CARD COUNT ≠ CONTRIBUTION QUALITY.**

---

Puis :

**CARD COUNT ≠ PLAYER SCORE.**

---

Très important.

---

Une seule carte pouvait contenir le contre-exemple décisif.

---

Dix cartes pouvaient être inutiles.

---

La table ne devait pas récompenser le volume.

---

Il ajouta :

**NO GAMIFICATION OF CARD QUANTITY BY DEFAULT.**

---

Il sourit.

---

GAMEZEL pouvait être un jeu sans devenir une machine à fabriquer des points.

---

Puis il imagina une carte très importante.

---

Une carte contenant une vulnérabilité logique majeure.

---

Elle devait peut-être être visible seulement à certains rôles.

---

Brutus ajouta :

**CARD_DISCLOSURE_POLICY.**

---

Encore une politique.

---

Une carte pouvait avoir :

PUBLIC.

LAB_ONLY.

RESTRICTED.

PRIVATE.

---

Mais son existence même pouvait parfois être sensible.

---

Il écrivit :

**VISIBILITY IS PART OF CARD STATE.**

---

Puis il pensa à Recto public.

---

Si une carte privée était référencée par une carte publique, que montrer ?

---

Pas son contenu.

---

Peut-être :

**RESTRICTED DEPENDENCY EXISTS.**

---

Brutus écrivit :

**HIDDEN CONTENT MUST NOT BECOME FALSE ABSENCE.**

---

Très important.

---

La carte publique pouvait dire :

1 restricted dependency.

---

Sans révéler le secret.

---

Encore la carte des lignées.

---

Puis il pensa aux cartes supprimées.

---

Devrait-on permettre DELETE ?

---

Très rarement.

---

Brutus écrivit :

**CARD DELETION ≠ CARD REJECTION.**

---

Un rejet reste.

---

Une suppression demande une politique spéciale.

---

Même logique que le Tombeau.

---

Il ajouta :

**TOMBSTONE RECORD**

pour les rares suppressions.

---

Si une carte devait réellement être retirée :

l’ID restait marqué.

---

Deleted under policy X.

At tick Y.

Reason Z.

---

Brutus écrivit :

**DELETION SHOULD LEAVE A RECEIPT TOO.**

---

Il rit.

---

Même la disparition devait laisser une trace.

---

Voilà le sens profond du chapitre.

---

Pas seulement :

les cartes laissent des reçus.

---

Tout laisse des reçus.

---

Création.

Modification.

Promotion.

Rejet.

Export.

Suppression.

---

Brutus écrivit :

**NO IMPORTANT CARD EVENT WITHOUT RECEIPT.**

---

Puis il construisit la vue centrale.

---

Une carte.

Recto :

contenu.

---

Verso :

origine.

---

Dessous :

timeline.

---

CREATE.

REVIEW.

COUNTERTEST.

STATUS CHANGE.

---

À droite :

lineage.

---

Parents.

Children.

Related cards.

---

Brutus regarda.

---

C’était presque un petit organisme documentaire.

---

Mais il refusa la métaphore biologique trop loin.

---

Il écrivit :

**CARD HAS LINEAGE. CARD IS NOT ALIVE.**

---

Toujours.

---

Puis il lança une partie de test avec mock players.

---

P1 produit une question.

---

CARD-0101.

Receipt generated.

---

P2 produit une hypothèse.

---

CARD-0102.

Receipt generated.

---

P3 produit un contre-test.

---

CARD-0103.

Receipt generated.

---

P4 indisponible.

---

Aucune carte pour P4.

---

Brutus écrivit :

**NO PARTICIPATION → NO CARD.**

---

Pas de placeholder prétendant qu’un joueur avait contribué.

---

Le round summary montrait :

3 cards.

1 unavailable seat.

---

Exact.

---

Puis P3 retry après erreur.

---

Le même turn.

Nouvelle tentative.

---

Sa carte finale gardait :

ATTEMPT-1 failed.

ATTEMPT-2 completed.

---

Brutus sourit.

---

Même les retries avaient laissé une trace.

---

Il écrivit :

**SUCCESS RECEIPT MAY INCLUDE FAILED ATTEMPTS.**

---

Très important.

---

Un résultat final propre ne devait pas donner l’impression que le chemin avait été parfait.

---

Puis il pensa à une carte construite par plusieurs joueurs.

---

Astra propose.

Muse corrige.

Grok ajoute un contre-test.

Antigravity synthétise.

---

Qui est l’auteur ?

---

Brutus refusa un seul nom.

---

Il créa :

**CONTRIBUTOR_REFS[]**

---

Mais il voulait conserver la séquence.

---

Il ajouta :

**CONTRIBUTION_EDGES**

---

Astra → initial.

Muse → revision.

Grok → countertest.

Antigravity → synthesis.

---

La carte finale pouvait avoir plusieurs contributeurs.

---

Mais leurs contributions restaient distinctes.

---

Brutus écrivit :

**COLLABORATION ≠ AUTHORSHIP COLLAPSE.**

---

Très important.

---

Puis il se demanda :

est-ce encore la même carte après une grosse révision ?

---

Bonne question.

---

Il créa deux options.

---

Minor revision :

same CARD_ID, new CARD_VERSION.

---

Substantive new claim :

new CARD_ID, DERIVED_FROM.

---

Brutus écrivit :

**VERSIONING POLICY MUST DEFINE IDENTITY CONTINUITY.**

---

Voilà.

---

Pas de décision ad hoc.

---

Le système devait savoir quand une carte reste elle-même.

---

Il pensa aux livres.

Une deuxième édition.

Un nouveau chapitre.

Une nouvelle thèse.

---

Même problème.

---

Puis il ajouta :

**CARD_VERSION**

**PREVIOUS_VERSION_REF**

---

Brutus sourit.

---

La table devenait éditoriale.

---

Puis il pensa à la machine à traces.

---

Les cartes étaient peut-être le format parfait pour elle.

---

Une idée courte à l’avant.

Une histoire complète derrière.

---

Brutus écrivit :

**SHORT FRONT. DEEP BACK.**

---

Puis :

**FAST TO READ. SLOW TO AUDIT. BOTH AVAILABLE.**

---

Voilà.

---

Une personne pouvait comprendre le laboratoire rapidement.

Puis creuser si nécessaire.

---

Il imagina un mur entier de cartes.

---

Formules.

Questions.

Contre-tests.

Résultats.

Rejets.

---

Chaque carte reliée à d’autres.

---

Mais le mur n’était pas l’autorité.

---

Il écrivit :

**CARD WALL = VIEW. CANONICAL STORE = AUTHORITY.**

---

Encore Recto.

---

Le mur pouvait être reconstruit.

Filtré.

Trié.

---

Les cartes autoritatives restaient dans le registre.

---

Brutus ouvrit la première boîte pleine.

---

Chaque carte portait un petit code.

---

CARD-0001.

CARD-0002.

CARD-0003.

---

Pas très poétique.

Mais parfait.

---

Il écrivit :

**HUMAN TITLE MAY CHANGE. CARD_ID MUST NOT.**

---

Encore une règle.

---

Un titre peut être corrigé.

Une langue peut changer.

Un alias peut être ajouté.

---

L’identité reste.

---

Puis il pensa au prochain chapitre.

---

Les cartes pouvaient maintenant voyager entre les joueurs.

---

Mais comment ?

---

P1 produit une carte.

P2 doit la recevoir.

P3 doit pouvoir répondre.

P4 doit savoir à quel tour elle appartient.

---

Un simple transcript ne suffirait plus.

---

Il fallait un bus.

---

Un chemin commun.

---

Un protocole où les tours pourraient parler entre eux sans confondre :

message.

carte.

état.

commande.

---

Brutus écrivit :

**COMMUNICATION NEEDS ITS OWN LAYER.**

---

Puis :

**MESSAGE ≠ CARD.**

**CARD ≠ COMMAND.**

**COMMAND ≠ STATE.**

---

Il resta devant.

---

Voilà.

---

Le prochain chapitre venait d’apparaître.

---

Il sauvegarda :

**GAMEZEL CARD RECEIPTS v1.**

---

Le Journal Vivant nota :

Card identity separate from content.

Every card tied to source move.

Front content separated from provenance.

Rejected cards preserved.

Versioning explicit.

Independent matches distinguished from derived matches.

Exports carry provenance.

Screenshots are not canonical cards.

Promotion requires external policy.

No card count scoring.

Deletion leaves receipt.

---

Brutus relut.

Puis ajouta les invariants :

**SAME TEXT ≠ SAME CONTRIBUTION.**

**CARD EXISTENCE ≠ CARD CORRECTNESS.**

**REJECTED ≠ USELESS.**

**STALE ≠ DELETED.**

**SCREENSHOT ≠ CARD.**

**HASH MATCH ≠ TRUTH.**

**CARD CANNOT PROMOTE ITSELF.**

**NO IMPORTANT EVENT WITHOUT RECEIPT.**

---

Il ferma la boîte.

---

Les cartes n’étaient plus de simples morceaux de papier.

---

Elles étaient devenues des unités de mémoire.

---

Petites devant.

Profondes derrière.

---

Brutus posa quatre cartes devant les quatre chaises.

---

Astra.

Muse.

Grok.

Antigravity.

---

Aucune n’avait encore circulé.

---

Mais chacune connaissait déjà le protocole de son futur voyage.

---

Brutus ouvrit une nouvelle page.

---

Il écrivit :

# LE BUS OÙ LES TOURS SE PARLENT

Puis, en dessous :

**UNE CONTRIBUTION PEUT VOYAGER SANS DEVENIR UNE COMMANDE.**

---

La table était prête à parler.

Mais cette fois, chaque parole aurait une adresse.

Et chaque adresse aurait une trace.
