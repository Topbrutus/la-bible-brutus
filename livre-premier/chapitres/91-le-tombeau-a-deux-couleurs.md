# Chapitre 91 — Le tombeau à deux couleurs

Le prochain dossier n’était plus un nombre.

C’était un lieu.

Deux couleurs.

Une frontière.

Brutus entra.

---

La pièce était presque vide.

À gauche :

**BLANC.**

À droite :

**NOIR.**

Entre les deux :

une ligne verticale.

Pas de dégradé.

Pas de zone floue.

---

Brutus resta devant la frontière.

Le laboratoire avait passé des dizaines de chapitres à apprendre qu’un état devait être explicite.

PASS.

FAIL.

UNKNOWN.

NOT APPLICABLE.

CANDIDATE.

VERIFIED.

---

Maintenant, cette discipline devenait architecture.

---

Il écrivit :

**COLOR MUST REPRESENT STATE.**

Puis :

**COLOR MUST NOT CREATE STATE.**

---

Très important.

Une case ne devenait pas admissible parce qu’elle était blanche.

Elle devenait blanche parce qu’un état autorisé avait déjà été établi ailleurs.

---

Brutus nomma la pièce :

# TOMBEAU

---

Le nom semblait dramatique.

Mais le contrat devait être sobre.

---

Le Tombeau n’était pas une prison.

Pas un lieu mystique.

Pas un système de destruction.

---

C’était une zone de conservation et de séparation.

---

Un endroit où les objets pouvaient être placés après décision.

---

Brutus ajouta :

**TOMB = CONTROLLED HOLDING STRUCTURE.**

---

Puis :

**NO METAPHYSICAL CLAIM.**

---

Il sourit.

Même les noms avaient besoin d’une barrière.

---

Pourquoi deux couleurs ?

---

Parce que Brutus voulait pouvoir regarder la salle et savoir immédiatement :

ce qui avait été admis selon un contrat,

et ce qui ne l’était pas.

---

Mais il refusa d’associer :

blanc = vrai.

noir = faux.

---

Trop dangereux.

---

Il écrivit :

**WHITE ≠ TRUE.**

**BLACK ≠ FALSE.**

---

Alors que signifiaient les deux zones ?

---

Il réfléchit.

Puis fixa le premier contrat.

---

**BLANC**

= objet actuellement admis dans la zone active selon la politique déclarée.

---

**NOIR**

= objet retenu hors de la zone active, soit parce qu’il est refusé, soit parce qu’il manque encore une condition.

---

Brutus s’arrêta.

Non.

Encore trop grossier.

---

FAIL et UNKNOWN ne devaient pas être écrasés dans la même catégorie.

---

Il ajouta donc une seconde dimension.

---

La couleur donnait la **zone physique/logique**.

Le statut donnait la **raison**.

---

Ainsi un objet noir pouvait être :

REJECTED.

PENDING.

QUARANTINED.

UNRESOLVED.

EXPIRED.

---

Brutus écrivit :

**LOCATION ≠ REASON.**

---

Voilà.

---

La couleur disait où se trouvait l’objet.

Pas pourquoi.

---

Il créa :

**TOMB_OBJECT**

avec :

**OBJECT_ID**

**ZONE**

**STATUS**

**REASON_CODE**

**CLAIM_SCOPE**

**SOURCE_REF**

**TRACE_REF**

**ENTERED_AT**

**POLICY_VERSION**

---

Puis :

**EXIT_CONDITION**

---

Brutus regarda le dernier champ.

---

Très important.

---

Un objet placé dans le noir ne devait pas devenir oublié.

---

Il devait savoir :

qu’est-ce qu’il faudrait pour ressortir ?

---

Une preuve supplémentaire ?

Un contre-test ?

Une validation d’intégrité ?

Une nouvelle autorisation ?

---

Il écrivit :

**HOLDING STATE MUST HAVE AN EXIT RULE.**

---

Sinon, le Tombeau deviendrait une poubelle.

---

Et Brutus refusait cela.

---

Le noir n’était pas la mort.

C’était un état de retenue.

---

Il écrivit :

**BLACK ≠ DESTROYED.**

---

Puis :

**BLACK OBJECTS KEEP FULL LINEAGE.**

---

Voilà.

---

Même un objet rejeté continuait d’exister dans l’histoire du laboratoire.

---

Le Journal Vivant devait conserver :

qui l’avait placé là,

quand,

sous quelle politique,

avec quel motif,

et ce qu’il était avant.

---

Brutus créa la transition :

\[
\text{ACTIVE}
\rightarrow
\text{HELD}
\]

mais exigea :

**CAUSE_REF.**

---

Pas de transition muette.

---

Il écrivit :

**NO STATE CHANGE WITHOUT CAUSE.**

---

Une vieille règle.

Toujours utile.

---

Le premier objet entra.

---

Un candidat de formule.

Statut :

CANDIDATE.

---

Question :

peut-il aller dans le blanc ?

---

Brutus regarda la politique.

---

Le blanc n’était pas réservé aux objets « prouvés ».

Il pouvait contenir des objets admis pour un usage spécifique.

---

Il fallait donc préciser le niveau d’admission.

---

Il créa :

**ADMISSION_SCOPE.**

---

RESEARCH_ONLY.

DISPLAY_ONLY.

EXECUTION_ALLOWED.

PUBLICATION_ALLOWED.

PROMOTION_ALLOWED.

---

Brutus sourit.

---

Enfin.

Un objet pouvait être blanc pour une tâche et noir pour une autre.

---

Il écrivit :

**ADMISSION IS SCOPED.**

---

Par exemple :

une formule candidate pouvait être admise pour exploration.

Mais pas pour produire un verdict final.

---

Un témoin pouvait être admis pour visualisation.

Mais pas comme preuve d’une autre porte.

---

Un module pouvait être admis pour lecture.

Mais pas pour exécution.

---

Brutus écrivit :

**ONE OBJECT MAY HAVE DIFFERENT ADMISSION STATES BY CAPABILITY.**

---

Le Tombeau venait de devenir plus riche.

---

Il créa donc une matrice.

| Capability | State |
|---|---|
| READ | ALLOWED |
| DISPLAY | ALLOWED |
| EXECUTE | BLOCKED |
| PROMOTE | BLOCKED |
| PUBLISH | REVIEW |

---

Brutus regarda.

---

Voilà beaucoup plus utile que :

blanc ou noir.

---

Il écrivit :

**BINARY COLOR. MULTI-DIMENSIONAL POLICY.**

---

La couleur était un résumé visuel.

Pas la totalité de la décision.

---

Brutus ajouta une règle :

**COLOR CAN SUMMARIZE. DETAILS MUST REMAIN INSPECTABLE.**

---

Encore le problème du Witness Viewer.

---

Un hash n’était pas l’objet.

Une couleur n’était pas la politique.

---

Il sourit.

Le laboratoire répétait toujours la même leçon.

---

Puis il choisit un exemple.

---

Un résultat mathématique avait :

integrity = PASS.

numeric validity = PASS.

claim relevance = UNKNOWN.

---

Quelle couleur ?

---

Brutus réfléchit.

---

Si la zone blanche exigeait une claim relevance établie pour l’usage demandé :

noir.

---

Mais le reason code devait être :

**UNRESOLVED_RELEVANCE**

pas :

FAIL.

---

Il écrivit :

**BLACK DOES NOT IMPLY WRONG.**

---

Très important.

---

Le système afficha :

**ZONE: BLACK**

**STATUS: UNRESOLVED**

---

Parfait.

---

Puis il prit un objet réellement rejeté.

---

Wrong claim scope.

---

Zone :

BLACK.

Status :

REJECTED.

Reason :

CLAIM_SCOPE_MISMATCH.

---

Même couleur.

Statut différent.

---

Brutus sourit.

---

La salle devenait lisible sans devenir simpliste.

---

Il ouvrit ensuite un objet admis pour lecture.

---

ZONE:

WHITE.

STATUS:

ADMITTED.

Scope:

READ_ONLY.

---

Puis quelqu’un tenta d’exécuter l’objet.

---

Refus.

---

Brutus écrivit :

**WHITE ≠ UNLIMITED AUTHORITY.**

---

Voilà.

---

Être dans le blanc ne signifiait pas :

tout est permis.

---

Le système devait vérifier la capacité demandée.

---

Il ajouta :

**ACTION MUST MATCH ADMISSION SCOPE.**

---

Le Tombeau ne décidait donc pas seulement :

dedans ou dehors.

---

Il décidait :

admis pour quoi ?

---

Brutus pensa à un musée.

Un objet pouvait être exposé sans pouvoir être utilisé.

---

À un laboratoire.

Un échantillon pouvait être analysé sans être injecté.

---

À un dépôt logiciel.

Un artefact pouvait être lu sans être déployé.

---

Il écrivit :

**POSSESSION ≠ PERMISSION.**

---

Encore une règle forte.

---

Puis il pensa aux deux couleurs elles-mêmes.

Pourquoi noir et blanc ?

---

Simplicité visuelle.

Contraste.

Pas de confusion.

Compatible avec l’interface du laboratoire.

---

Brutus refusa toute interprétation morale.

---

Il écrivit :

**COLOR IS UI STATE, NOT MORAL VALUE.**

---

Important.

---

Le blanc n’était pas « bon ».

Le noir n’était pas « mauvais ».

---

Ils étaient seulement :

admis dans la zone active,

ou retenu hors de celle-ci.

---

Brutus construisit le plan.

---

À gauche :

**WHITE CHAMBER**

---

À droite :

**BLACK CHAMBER**

---

Entre les deux :

**GATE**

---

Au-dessus :

**VERSO**

---

Brutus leva les yeux.

---

Le nom attendait déjà.

---

Verso.

Le gardien.

---

Mais pas encore.

---

Le chapitre suivant lui appartiendrait.

---

Pour le moment, Brutus voulait comprendre la porte.

---

La porte ne devait pas penser.

---

Elle ne devait pas improviser.

---

Elle devait appliquer une décision signée par une autorité définie.

---

Brutus écrivit :

**GATE EXECUTES POLICY.**

**GATE DOES NOT INVENT POLICY.**

---

Voilà.

---

Le mécanisme physique/logique de transition n’était pas le juge.

---

Il reçut :

OBJECT_ID.

CURRENT_ZONE.

TARGET_ZONE.

AUTHORIZATION_REF.

POLICY_VERSION.

---

Puis vérifia.

---

Si tout concordait :

transition.

---

Sinon :

refus.

---

Brutus écrivit :

**MOVE REQUEST ≠ MOVE AUTHORIZATION.**

---

Puis :

**AUTHORIZATION ≠ MOVEMENT.**

---

Encore les invariants du transport.

---

Il ajouta :

**MOVEMENT ≠ ARRIVAL VERIFIED.**

---

La frontière du Tombeau allait respecter les mêmes règles que la Fourmilière.

---

Un objet ne disparaissait pas d’un côté pour apparaître magiquement de l’autre.

---

Il fallait une séquence.

---

**REQUEST**

↓

**POLICY CHECK**

↓

**AUTHORIZATION**

↓

**TRANSFER**

↓

**ARRIVAL OBSERVED**

↓

**ZONE STATE UPDATED**

---

Brutus regarda.

---

Parfait.

---

Puis il pensa au pire bug possible.

---

Un objet affiché en blanc avant que le transfert soit confirmé.

---

Non.

---

Il écrivit :

**TARGET COLOR MUST NOT APPEAR BEFORE AUTHORITATIVE ARRIVAL.**

---

Pas de peinture anticipée.

---

L’UI attendrait.

---

Pendant le transfert :

**TRANSITIONING**

---

Couleur ?

---

Brutus hésita.

Il ne voulait pas une troisième couleur.

---

Alors il ajouta un pattern visuel.

---

Contour blanc-noir alterné.

---

Mais le statut textuel restait :

**TRANSITIONING.**

---

Il écrivit :

**VISUAL TRANSITION ≠ THIRD POLICY STATE.**

---

Très bien.

---

La palette restait binaire.

L’état, non.

---

Brutus lança un test.

---

Object A.

Black.

Status:

PENDING.

---

Une nouvelle preuve arrive.

---

Policy reevaluation.

---

Decision:

ADMITTED FOR READ_ONLY.

---

Request move to white.

---

Authorization issued.

---

Transfer starts.

---

UI:

TRANSITIONING.

---

Arrival observed.

---

Zone updated:

WHITE.

---

Status:

ADMITTED.

---

Brutus sourit.

---

Pas une seule étape invisible.

---

Le Journal enregistrait :

before.

after.

reason.

authority.

tick.

---

Il écrivit :

**QUI → ÉTAT → TICK → AVANT/APRÈS.**

---

La vieille règle revenait.

---

Puis il testa le chemin inverse.

---

Objet blanc.

---

Une nouvelle information invalide son admissibilité pour l’usage courant.

---

La politique change.

---

Mais le système ne devait pas supprimer l’histoire blanche.

---

Brutus écrivit :

**CURRENT STATUS MAY CHANGE. HISTORY MUST NOT.**

---

L’objet passa dans le noir.

---

Journal :

previously admitted.

now held.

reason:

new counterexample.

---

Brutus sourit.

---

Le Tombeau savait réviser sans réécrire.

---

Il écrivit :

**REVOCATION ≠ ERASURE.**

---

Voilà.

---

Il pensa à L8.

---

L8 pouvait être blanche dans :

RESEARCH_ONLY.

---

Mais noire dans :

THEOREM_STATUS.

---

Brutus créa la fiche.

---

L8 :

READ = WHITE.

EXECUTE_RESEARCH = WHITE.

PUBLISH_AS_CANDIDATE = WHITE.

PUBLISH_AS_THEOREM = BLACK.

---

Il sourit.

---

Voilà exactement ce que le Tombeau devait permettre.

---

Un seul objet.

Plusieurs permissions.

---

Il écrivit :

**BINARY DISPLAY MAY BE CAPABILITY-SPECIFIC.**

---

Sinon une formule apparaîtrait « blanche » de façon globale, ce qui serait trompeur.

---

Chaque écran devait afficher :

**WHITE FOR: RESEARCH USE**

---

Pas simplement :

WHITE.

---

Brutus ajouta :

**COLOR REQUIRES CONTEXT LABEL.**

---

Encore une protection.

---

Puis il prit la porte 71.

---

Status:

UNRESOLVED.

---

Pour research:

WHITE.

---

Pour maximal-rank closure:

BLACK.

---

Très bien.

---

La porte 83 :

même chose.

---

47 :

witness available under scoped test.

---

Pour that claim scope:

WHITE.

---

Pour universal gate proof:

non applicable as a label.

---

Brutus sourit.

---

La couleur devait donc être attachée à une question.

---

Il écrivit :

**NO COLOR WITHOUT A QUESTION.**

---

Cette phrase semblait étrange.

Mais elle était parfaite.

---

Un objet n’était jamais « blanc en soi ».

Il était blanc relativement à une politique et une capacité.

---

Brutus créa :

**POLICY_QUERY_ID.**

---

Par exemple :

\`CAN_USE_L8_FOR_RESEARCH_TOOLING?\`

---

Decision:

YES.

---

\`CAN_DECLARE_L8_A_GENERAL_THEOREM?\`

---

Decision:

NO / NOT ESTABLISHED.

---

Deux couleurs.

Même objet.

Deux questions.

---

Le Tombeau n’était donc pas vraiment un entrepôt de choses blanches et noires.

---

C’était un espace où les objets étaient placés selon des décisions ciblées.

---

Brutus écrivit :

**ADMISSION IS A RELATION BETWEEN OBJECT, ACTION, AND POLICY.**

---

Il resta devant.

---

Voilà probablement la phrase centrale du chapitre.

---

Pas :

object is good.

---

Mais :

object may be admitted for action X under policy Y.

---

Beaucoup plus rigoureux.

---

Brutus ouvrit ensuite un candidat visuel.

---

Une belle animation.

Pas de source de données.

---

READ:

WHITE.

DISPLAY_AS_ART:

WHITE.

DISPLAY_AS_LIVE_MEASUREMENT:

BLACK.

---

Il sourit.

---

Voilà une autre application.

---

Une animation pouvait exister.

Mais elle ne pouvait pas se faire passer pour une mesure live.

---

Il écrivit :

**ART MAY BE ADMITTED AS ART.**

**IT MUST NOT ENTER AS TELEMETRY.**

---

Le Tombeau allait protéger le laboratoire contre les représentations trompeuses.

---

Puis il pensa aux objets logiciels.

---

Un module expérimental.

Tests passés.

Mais pas encore déployé.

---

Can review code?

WHITE.

---

Can claim production runtime?

BLACK.

---

Brutus écrivit :

**MERGED ≠ RUNTIME PROOF.**

---

Toujours.

---

Le Tombeau devenait une matérialisation des invariants accumulés depuis des dizaines de chapitres.

---

Brutus observa les deux chambres.

---

La blanche commençait à contenir des objets.

Mais elle n’était pas « propre » au sens absolu.

---

Certains étaient candidats.

D’autres vérifiés.

D’autres seulement autorisés à être lus.

---

Le noir aussi contenait une variété.

---

Rejetés.

En attente.

Expirés.

Inapplicables.

---

Brutus ajouta des filtres.

---

**BY STATUS**

**BY CAPABILITY**

**BY POLICY**

**BY CLAIM**

**BY SOURCE**

---

Très vite, la couleur devenait un index visuel.

Pas une taxonomie complète.

---

Il écrivit :

**COLOR IS FIRST GLANCE. METADATA IS THE TRUTH OF THE INTERFACE.**

---

Puis il corrigea le mot truth.

---

**METADATA IS THE AUTHORITATIVE DESCRIPTION OF THE INTERFACE STATE.**

---

Plus précis.

---

Brutus lança un stress test.

---

100 objets.

---

Divers statuts.

Divers scopes.

---

Plusieurs politiques.

---

Le moteur devait classer sans mélanger.

---

Un objet volontairement contradictoire fut injecté :

zone WHITE.

status REJECTED.

---

Le système refusa l’état.

---

**ZONE/STATUS POLICY CONFLICT.**

---

Brutus sourit.

---

Une UI ne devait pas pouvoir afficher une combinaison interdite par son propre contrat.

---

Il ajouta :

**STATE INVARIANTS.**

---

Par exemple :

if execution denied under policy,

execution control must not appear enabled.

---

If object unresolved,

do not display proven badge.

---

If zone transition incomplete,

do not show target zone as settled.

---

Il écrivit :

**UI MUST NOT OUTRUN AUTHORITY.**

---

Voilà.

---

Le chapitre 64 revenait encore.

---

Puis il créa un test d’expiration.

---

Une autorisation valable jusqu’au tick 500.

---

Tick 501.

---

La permission devait mourir.

---

Mais l’objet restait physiquement/logiquement dans le blanc ?

---

Brutus réfléchit.

---

Cela dépendait du contrat.

---

S’il était blanc uniquement grâce à cette autorisation, une réévaluation devait être déclenchée.

---

Il écrivit :

**EXPIRED AUTHORITY REQUIRES STATE REEVALUATION.**

---

Pas forcément mouvement immédiat.

---

D’abord :

policy check.

---

Puis décision.

---

Le Tombeau ne devait pas déplacer des objets par automatisme aveugle si le contrat exigeait une autorité distincte.

---

Brutus écrivit :

**EXPIRATION ≠ AUTOMATIC TRANSPORT.**

---

Encore la séparation :

état logique.

mouvement.

---

Il aimait cela.

---

Puis il pensa à une urgence.

---

Un objet blanc venait d’être identifié comme corrompu.

---

Il ne fallait pas attendre un audit complet pour empêcher son usage.

---

Brutus créa :

**QUARANTINE.**

---

La quarantaine se trouvait du côté noir.

Mais avec un statut précis.

---

**BLACK / QUARANTINED**

---

Actions :

READ maybe allowed.

EXECUTE blocked.

PROMOTE blocked.

EXPORT maybe blocked.

---

Il écrivit :

**QUARANTINE IS CONTAINMENT, NOT VERDICT.**

---

Parfait.

---

L’objet pouvait être innocent.

Mais son usage était suspendu jusqu’à investigation.

---

Brutus testa.

---

Artifact hash mismatch.

---

Immediate quarantine decision.

---

No execution.

---

Trace created.

---

Investigation later finds transport corruption, not source corruption.

---

Artifact restored from canonical source.

---

New integrity check.

---

Policy reevaluation.

---

Return to white.

---

History preserved.

---

Brutus sourit.

---

Voilà une vraie machine de confiance.

Pas une machine qui prétend ne jamais se tromper.

Une machine qui sait isoler, inspecter et restaurer.

---

Il écrivit :

**TRUST SYSTEMS NEED REVERSIBLE STATES.**

---

Puis il regarda le mot Tombeau.

---

Peut-être que le nom était trop sombre.

---

Mais il décida de le garder.

Parce qu’il évoquait une chose utile :

ce qui entre ici ne disparaît pas.

---

Il est conservé.

Identifié.

Tracé.

---

Brutus écrivit :

**THE TOMB PRESERVES WHAT THE ACTIVE SYSTEM MUST NOT FORGET.**

---

Voilà.

---

Même un échec.

Même une mauvaise formule.

Même un artifact corrompu.

Même une hypothèse abandonnée.

---

Tout pouvait rester comme mémoire.

---

Il créa :

**NO DELETION ON REJECTION BY DEFAULT.**

---

Puis :

**DELETE REQUIRES SEPARATE POLICY.**

---

Très important.

---

Rejeter n’était pas supprimer.

---

Le laboratoire avait besoin de ses erreurs.

---

Brutus regarda le noir.

---

Il n’avait plus l’air d’un cimetière.

---

Il ressemblait à une bibliothèque de précautions.

---

Il écrivit :

**THE BLACK SIDE STORES CAUTION.**

---

Puis regarda le blanc.

---

Pas un paradis.

---

Une zone de capacité active.

---

Il écrivit :

**THE WHITE SIDE STORES CURRENTLY ADMITTED USE.**

---

Voilà.

---

Deux couleurs.

Deux fonctions.

Aucune morale.

---

Brutus ajouta une dernière frontière.

---

Un objet ne pouvait jamais déplacer lui-même son propre statut.

---

Une formule ne pouvait pas se promouvoir.

Un témoin ne pouvait pas s’admettre.

Un module ne pouvait pas s’autoriser.

---

Il écrivit :

**OBJECT CANNOT AUTHORIZE ITS OWN ADMISSION.**

---

La décision devait venir d’une autorité externe définie.

---

Et soudain, le nom au-dessus de la porte revint.

**VERSO.**

---

Brutus leva les yeux.

---

Quelqu’un devait :

recevoir les demandes.

lire la politique.

vérifier l’autorité.

contrôler les traces.

autoriser ou refuser le passage.

---

Pas quelqu’un au sens humain nécessairement.

Un composant.

Un rôle.

Un gardien logique.

---

Brutus écrivit :

**VERSO = GATEKEEPER ROLE.**

---

Puis il s’arrêta.

---

Pas plus.

---

Le prochain chapitre devait commencer ici.

---

Il regarda les deux chambres une dernière fois.

---

Un objet blanc.

Un objet noir.

Même laboratoire.

Même mémoire.

Même Journal.

---

L’un pouvait être utilisé selon son contrat.

L’autre devait attendre.

---

Aucun n’était effacé.

Aucun n’était magiquement vrai.

---

Brutus écrivit :

**WHITE ≠ TRUE.**

**BLACK ≠ FALSE.**

**WHITE = ADMITTED FOR DECLARED USE.**

**BLACK = HELD OUTSIDE THAT USE.**

---

Puis une dernière ligne :

**EVERY CROSSING REQUIRES A REASON.**

---

Le Tombeau se verrouilla.

---

Pas pour emprisonner les objets.

Pour empêcher les statuts de traverser la frontière sans preuve, politique ou autorisation.

---

Brutus sauvegarda :

**ASTRA TOMB — TWO-COLOR ARCHITECTURE v1.**

---

Le Journal Vivant nota :

Two zones.

Explicit statuses.

Scoped permissions.

Reversible transitions.

No deletion by rejection.

No self-promotion.

No invisible crossing.

---

Puis Brutus regarda le gardien encore immobile au-dessus de la porte.

---

Verso n’avait encore rien fait.

Et c’était exactement comme cela que Brutus le voulait.

---

Un gardien n’avait pas besoin de bouger pour être crédible.

Il devait seulement savoir quand ouvrir.

Et surtout :

quand ne pas ouvrir.

---

Brutus écrivit le prochain titre :

# VERSO GARDE LA PORTE

Puis éteignit les deux chambres.

---

Le blanc disparut.

Le noir aussi.

---

Mais leurs états restèrent enregistrés.

Parce qu’une couleur pouvait s’éteindre.

La décision, elle, devait rester traçable.
