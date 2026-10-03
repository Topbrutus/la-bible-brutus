# Chapitre 106 — La porte de promotion

Au-dessus du nouveau dossier, Brutus avait écrit :

**SURVIVING TESTS DOES NOT GIVE AN IDEA THE RIGHT TO PROMOTE ITSELF.**

Il relut la phrase.

Puis il ouvrit la porte.

---

Derrière, rien de spectaculaire.

Pas de lumière blanche.

Pas de cristal.

Pas de musique.

---

Seulement une file.

---

Des cartes.

Des claims.

Des résultats.

Des expériences terminées.

Des contre-tests.

Des rapports du Judge.

---

Tous attendaient.

---

Brutus écrivit :

# PROMOTION GATE

---

Puis, juste en dessous :

**PROMOTION ≠ PROOF.**

---

Voilà.

---

La règle devait être visible avant même de regarder un seul dossier.

---

Une promotion n’était pas une transformation magique d’une hypothèse en vérité.

---

C’était un changement de statut.

---

Un objet pouvait passer :

PROPOSED

vers

ADMITTED_FOR_RESEARCH.

---

Ou :

ADMITTED_FOR_RESEARCH

vers

SUPPORTED_UNDER_SCOPE.

---

Ou :

SUPPORTED_UNDER_SCOPE

vers

READY_FOR_EXTERNAL_REVIEW.

---

Mais aucune de ces transitions ne voulait dire :

**THEOREM.**

---

Brutus écrivit :

**STATUS STRENGTH ≠ MATHEMATICAL CERTAINTY.**

---

Puis il créa le premier contrat.

**PROMOTION_REQUEST**

avec :

**REQUEST_ID**

**OBJECT_ID**

**OBJECT_VERSION**

**CURRENT_STATUS**

**REQUESTED_STATUS**

**CLAIM_SCOPE**

**EVIDENCE_REFS**

**COUNTERTEST_REFS**

**JUDGE_REFS**

**DEPENDENCY_STATUS**

**POLICY_VERSION**

**REQUESTED_BY**

**TRACE_REF**

---

Puis il ajouta :

**WHY_NOW**

---

Très important.

---

Pourquoi cette promotion est-elle demandée maintenant ?

---

Nouvelle expérience ?

Contre-test terminé ?

Reproduction indépendante ?

Dépendance résolue ?

---

Ou simplement parce que quelqu’un aime beaucoup la formule ?

---

Brutus écrivit :

**ENTHUSIASM ≠ PROMOTION EVIDENCE.**

---

Il sourit.

---

Cette porte allait devoir résister à beaucoup d’enthousiasme.

---

Il prit une carte.

---

CARD-042.

Status :

PROPOSED.

---

Evidence :

none.

---

Requested status :

SUPPORTED_UNDER_SCOPE.

---

La porte refusa.

---

Reason :

**MISSING_REQUIRED_EVIDENCE.**

---

Brutus écrivit :

**REQUEST DENIED ≠ CLAIM FALSE.**

---

Très important.

---

La promotion pouvait échouer parce que le dossier était incomplet.

---

Pas parce que la claim était réfutée.

---

Il ajouta :

**PROMOTION_FAILURE_REASON**

INSUFFICIENT_EVIDENCE.

UNRESOLVED_COUNTERTEST.

MISSING_REPLICATION.

STALE_DEPENDENCY.

SCOPE_MISMATCH.

POLICY_MISMATCH.

CLAIM_VERSION_MISMATCH.

OPEN_INCIDENT.

---

Puis :

**NOT_ELIGIBLE_YET**

---

Brutus sourit.

---

Le mot **yet** était important.

---

Un dossier incomplet aujourd’hui pouvait devenir admissible demain.

---

Il écrivit :

**NOT READY ≠ NEVER.**

---

Puis il pensa aux statuts.

---

Il ne voulait pas dix couleurs mystérieuses.

---

Il voulait une échelle claire.

---

Il créa :

**RESEARCH_STATUS**

DRAFT.

PROPOSED.

ADMITTED_FOR_TESTING.

SUPPORTED_UNDER_SCOPE.

COUNTERTESTED_UNDER_SCOPE.

REPLICATED_UNDER_SCOPE.

READY_FOR_EXTERNAL_REVIEW.

ARCHIVED.

REJECTED.

---

Puis il s’arrêta.

---

Attention.

---

**REPLICATED_UNDER_SCOPE** ne devait pas automatiquement être « plus vrai » dans tous les cas.

---

Une reproduction peut répliquer une erreur méthodologique partagée.

---

Il écrivit :

**STATUS ORDER ≠ UNIVERSAL TRUTH ORDER.**

---

Très important.

---

L’échelle était une progression procédurale.

---

Pas un thermomètre métaphysique.

---

Il ajouta :

**STATUS SEMANTICS MUST BE EXPLICIT.**

---

Par exemple :

SUPPORTED_UNDER_SCOPE signifie :

evidence consistent with claim under declared experiment scope.

---

COUNTERTESTED_UNDER_SCOPE signifie :

required countertest set completed under declared policy, with no validated refutation found in that tested scope.

---

REPLICATED_UNDER_SCOPE signifie :

specified result reproduced under declared replication class.

---

READY_FOR_EXTERNAL_REVIEW signifie :

internal evidence package meets publication/review requirements.

---

Brutus écrivit :

**STATUS NAME WITHOUT DEFINITION IS DANGEROUS.**

---

Puis il pensa au mot :

**PASS.**

---

Beaucoup trop vague.

---

Pass quoi ?

---

Une expérience ?

Un gate ?

Un review ?

Un schema check ?

---

Il écrivit :

**PASS MUST ALWAYS NAME THE TEST IT PASSED.**

---

Très important.

---

Alors la porte n’afficherait pas :

PASS.

---

Elle afficherait :

**PROMOTION ELIGIBILITY — PASS**

---

ou :

**COUNTERTEST SET — COMPLETE**

---

ou :

**REPLICATION REQUIREMENT — SATISFIED**

---

Voilà.

---

Brutus prit L8.

---

Supposons que CT-02 et CT-04 sont terminés.

CT-01 et CT-03 restent ouverts.

---

Le dossier demande :

READY_FOR_EXTERNAL_REVIEW.

---

La porte regarde :

required countertest set.

---

Incomplete.

---

Decision :

DENIED.

---

Reason :

**OPEN_REQUIRED_CONTROLS: CT-01, CT-03.**

---

Brutus écrit :

**PARTIAL COMPLETION ≠ PROMOTION ELIGIBILITY.**

---

Pas besoin de dire que L8 est mauvaise.

---

Seulement :

le dossier requis n’est pas complet.

---

Très important.

---

Puis il pensa aux gates 71 et 83.

---

Toujours unresolved.

---

Une formule dépendante de ces portes pouvait-elle être promue ?

---

Cela dépend du scope.

---

Si la claim exige ces gates :

non.

---

Si le scope exclut explicitement ces dépendances :

peut-être.

---

Brutus écrivit :

**OPEN DEPENDENCY BLOCKS ONLY THE CLAIMS THAT REQUIRE IT.**

---

Excellent.

---

Le laboratoire ne devait pas bloquer tout le monde à cause d’un seul problème local.

---

Il ajouta :

**DEPENDENCY IMPACT MUST BE CLAIM-SCOPED.**

---

Puis il pensa à q47.

---

Un witness validé sous contrat q47 pouvait soutenir une promotion concernant q47.

---

Mais pas automatiquement q71.

---

Il écrivit :

**PROMOTION EVIDENCE MUST MATCH CLAIM SCOPE.**

---

Encore.

---

Le chapitre 105 revenait.

---

Une preuve forte pour la mauvaise claim restait la mauvaise preuve.

---

Puis il pensa aux objets composés.

---

Supposons :

CLAIM-C dépend de CLAIM-A et CLAIM-B.

---

A est supported.

B est unresolved.

---

C peut-elle être promoted ?

---

Pas au-delà du niveau permis par B.

---

Brutus créa :

**PROMOTION_DEPENDENCY_GRAPH**

---

Il écrivit :

**A COMPOSITE CLAIM CANNOT OUTRUN ITS REQUIRED DEPENDENCIES.**

---

Très important.

---

Puis il ajouta :

**WEAKEST REQUIRED DEPENDENCY MAY BOUND PROMOTION.**

---

Pas comme une loi universelle.

Comme règle de policy.

---

Il sourit.

---

Enfin les dépendances avaient un effet clair.

---

Puis il pensa à un autre cas.

---

Une claim a été testée sur :

n ≤ 10^6.

---

Requested promotion :

SUPPORTED_UNDER_ALL_N.

---

Refus.

---

Brutus écrivit :

**EVIDENCE DOMAIN MUST COVER PROMOTION SCOPE.**

---

Très important.

---

La porte pouvait proposer :

SUPPORTED_UNDER_TESTED_DOMAIN.

---

Mais jamais élargir silencieusement.

---

Il ajouta :

**SCOPE EXPANSION REQUIRES NEW EVIDENCE.**

---

Voilà.

---

Puis il pensa aux statistiques.

---

Un résultat avec une estimation et un intervalle.

---

La promotion devait conserver :

sample.

method.

uncertainty.

---

Pas seulement :

SUPPORTED.

---

Brutus écrivit :

**PROMOTION MUST NOT STRIP UNCERTAINTY METADATA.**

---

Très important.

---

Le statut plus fort ne devait pas produire une claim plus précise que les données.

---

Puis il pensa aux claims exactes.

---

Pour une identité mathématique, le chemin de promotion pouvait être différent.

---

Evidence :

formal derivation.

verified algebra.

independent proof review.

counterexample search.

---

Brutus écrivit :

**PROMOTION POLICY DEPENDS ON CLAIM TYPE.**

---

Encore le chapitre 103.

---

Une même gate ne devait pas exiger les mêmes éléments à :

une conjecture,

une mesure expérimentale,

une garantie logicielle,

un théorème.

---

Il créa :

**PROMOTION_POLICY_CLASS**

MATHEMATICAL.

STATISTICAL.

OPERATIONAL.

EXPERIMENTAL.

SOFTWARE.

---

Puis il ajouta :

**POLICY_VERSION**

à chaque décision.

---

Parce qu’un dossier évalué sous policy v1 pouvait recevoir un résultat différent sous v2.

---

Brutus écrivit :

**PROMOTION DECISION IS POLICY-RELATIVE.**

---

Très important.

---

Cela ne rendait pas la science arbitraire.

---

Cela rendait explicite la règle utilisée.

---

Puis il pensa aux changements de policy.

---

Supposons :

v1 exige deux reproductions.

v2 en exige trois.

---

Les objets déjà promus sous v1 deviennent-ils automatiquement invalides ?

---

Pas forcément.

---

Il écrivit :

**NEW POLICY ≠ AUTOMATIC RETROACTIVE DEMOTION.**

---

La policy pouvait déclarer :

grandfathered.

review-required.

automatic re-evaluation.

---

Brutus créa :

**POLICY_MIGRATION_RULE**

---

Il sourit.

---

Même les standards évoluaient proprement.

---

Puis il pensa aux promotions automatiques.

---

GAMEZEL produit un résultat.

Judge valide.

Tous les critères machine-checkable sont satisfaits.

---

La carte peut-elle être promoted automatiquement ?

---

Peut-être jusqu’à certains niveaux.

---

Il créa :

**AUTO_PROMOTION_LIMIT**

---

Par exemple :

PROPOSED → ADMITTED_FOR_TESTING.

---

Possible.

---

Mais :

READY_FOR_PUBLICATION ?

Peut-être humain requis.

---

Brutus écrivit :

**AUTOMATION MAY PROMOTE ONLY WITHIN PREAUTHORIZED BOUNDS.**

---

Encore le chapitre 100.

---

Pas de pouvoir auto-créé.

---

Il ajouta :

**MAX_AUTONOMOUS_STATUS**

---

Très important.

---

Une campagne autonome pouvait faire avancer un objet jusqu’à :

COUNTERTESTED_UNDER_SCOPE.

---

Puis s’arrêter.

---

Human review required.

---

Brutus écrit :

**AUTONOMOUS RESEARCH CAN PREPARE A DECISION WITHOUT OWNING THE FINAL DECISION.**

---

Voilà.

---

Puis il pensa au Judge.

---

Le Judge produit :

VALID_REFUTATION.

---

La porte de promotion reçoit ensuite une demande vers un statut plus fort.

---

Refus évident.

---

Mais pourquoi ?

---

Il ne devait pas simplement dire :

DENIED.

---

Il devait dire :

**BLOCKED_BY_VALIDATED_REFUTATION**

with REF.

---

Brutus écrivit :

**PROMOTION DENIAL MUST POINT TO BLOCKING EVIDENCE.**

---

Très important.

---

L’opérateur pouvait descendre jusqu’au contre-exemple.

---

Pas de boîte noire.

---

Puis il pensa à un contre-test unresolved.

---

Pas validé.

Pas dismissed.

---

La porte devait-elle bloquer ?

---

Selon policy.

---

Brutus créa :

**OPEN_CHALLENGE_POLICY**

BLOCK.

ALLOW_WITH_FLAG.

REQUIRE_REVIEW.

---

Puis :

**UNRESOLVED CHALLENGE MUST NEVER DISAPPEAR FROM PROMOTED OBJECT.**

---

Très important.

---

Si policy autorise la promotion malgré un point ouvert, le badge doit rester.

---

Brutus écrivit :

**PROMOTION MUST CARRY FORWARD KNOWN LIMITATIONS.**

---

Excellent.

---

Une promotion ne devait pas laver le dossier.

---

Puis il pensa à la version.

---

Claim v3 est promoted.

---

Quelqu’un édite la claim en v4.

---

Le statut peut-il suivre automatiquement ?

---

Non.

---

Brutus écrivit :

**PROMOTION BELONGS TO A SPECIFIC CLAIM VERSION.**

---

Puis :

**NEW SEMANTIC VERSION REQUIRES NEW ELIGIBILITY REVIEW.**

---

Très important.

---

Le texte peut sembler presque identique.

---

Mais un seul mot peut élargir énormément le scope.

---

Exemple :

“pour les q testés”

devient :

“pour tous les q”.

---

Pas le même objet.

---

Brutus sourit.

---

La version était une barrière contre les promotions fantômes.

---

Puis il pensa aux corrections éditoriales.

---

Accent.

Typo.

Whitespace.

---

Pas besoin de recommencer tout le processus.

---

Il reprit :

**CHANGE_CLASS**

EDITORIAL.

SEMANTIC.

---

Editorial :

promotion carries.

Semantic :

re-review.

---

Brutus écrivit :

**TEXT CHANGE ≠ CLAIM CHANGE.**

---

Et :

**CLAIM CHANGE ≠ TEXT CHANGE SIZE.**

---

Très important.

---

Une petite modification peut être sémantiquement énorme.

---

Puis il pensa au public.

---

La carte est READY_FOR_EXTERNAL_REVIEW.

---

Peut-elle apparaître sur Recto ?

---

Oui, peut-être.

---

Mais le Recto doit afficher le statut exact.

---

Pas :

PROVEN.

---

Brutus écrivit :

**PUBLIC LABEL MUST MATCH CANONICAL STATUS.**

---

Encore.

---

Il ajouta :

**PUBLIC_STATUS_TEXT**

dérivé de status.

---

Par exemple :

“Résultat interne, prêt pour revue externe.”

---

Pas :

“Découverte prouvée.”

---

Brutus sourit.

---

Les mots publics pouvaient changer la perception plus que les données.

---

Il écrivit :

**PROMOTION LANGUAGE IS PART OF SCIENTIFIC INTEGRITY.**

---

Puis il pensa au cristal.

---

Le mot revenait de loin.

---

Cristalliser.

---

Dans Brutus, un cristal pouvait devenir un objet stable.

---

Mais attention.

---

Un cristal n’était pas une preuve.

---

Il écrivit :

**CRYSTAL != PROOF.**

---

Puis :

**CRYSTALLIZATION MAY REPRESENT STABLE PACKAGING, NOT TRUTH.**

---

Très important.

---

Un objet pouvait être cristallisé parce que :

son contenu est figé,

ses hashes sont calculés,

sa provenance est complète,

sa version est stable.

---

Pas parce que la théorie est démontrée.

---

Brutus sourit.

---

Cela préparait la suite.

---

Mais il n’était pas encore au chapitre 108.

---

Il revint à la promotion.

---

Une promotion devait produire un nouvel événement.

---

Il créa :

**PROMOTION_EVENT**

avec :

EVENT_ID.

OBJECT_ID.

FROM_STATUS.

TO_STATUS.

CLAIM_VERSION.

SCOPE.

POLICY_VERSION.

EVIDENCE_SET_HASH.

BLOCKERS_RESOLVED_REFS.

REVIEWER_REF.

AUTHORIZED_BY.

TICK.

TRACE_REF.

---

Puis :

**PROMOTION_RECEIPT**

---

Brutus écrivit :

**PROMOTION IS AN EVENT, NOT A COLOR CHANGE.**

---

La vieille phrase du chapitre 97 revenait.

---

Encore plus forte ici.

---

Une carte ne devient pas blanche parce que l’interface la peint en blanc.

---

L’interface devient blanche parce qu’un promotion event existe.

---

Il écrivit :

**COLOR FOLLOWS EVENT. EVENT DOES NOT FOLLOW COLOR.**

---

Excellent.

---

Puis il pensa à la concurrence.

---

Deux reviewers.

---

Reviewer A demande promotion.

Reviewer B demande hold.

---

Même state version.

---

Verso doit sérialiser.

---

Après première décision :

state version change.

---

La seconde demande devient stale.

---

Brutus écrivit :

**PROMOTION GATE MUST BE CONCURRENCY-SAFE.**

---

Encore le chapitre 92.

---

Pas de double statut contradictoire.

---

Puis il pensa aux retries.

---

Promotion request envoyée.

Network timeout.

---

Retry.

---

Le système ne doit pas promouvoir deux fois.

---

Il ajouta :

**IDEMPOTENT PROMOTION REQUEST.**

---

Même REQUEST_ID.

---

Same decision.

---

Brutus écrivit :

**RETRY ≠ SECOND PROMOTION.**

---

Très important.

---

Puis il pensa au rollback.

---

Promotion faite.

Ensuite on découvre un bug majeur dans l’expérience.

---

Que faire ?

---

Pas supprimer la promotion.

---

Créer :

**DEMOTION_REQUEST**

---

Brutus n’aimait pas le mot.

---

Mais il était utile.

---

Il créa :

**STATUS_REVISION_REQUEST**

---

Possible transitions :

SUPPORTED → REVIEW_REQUIRED.

PROMOTED → SUSPENDED.

READY_FOR_EXTERNAL_REVIEW → INTERNAL_REVIEW_REQUIRED.

---

Brutus écrivit :

**NEW NEGATIVE EVIDENCE SHOULD TRIGGER REVIEW, NOT HISTORY ERASURE.**

---

Puis :

**DEMOTION IS AN EVENT TOO.**

---

Encore.

---

La promotion n’était pas irréversible.

---

Mais sa révocation devait être traçable.

---

Il ajouta :

**PROMOTION_REVOCATION_REF**

---

Puis il pensa à un objet publié.

---

Si le statut interne baisse après publication ?

---

Le système doit le signaler.

---

Il créa :

**PUBLICATION_IMPACT_EVENT**

---

Brutus écrivit :

**POST-PUBLICATION CORRECTION MUST BE POSSIBLE.**

---

Très important.

---

Pas de système scientifique sérieux sans capacité de correction.

---

Puis il pensa au prestige.

---

Supposons qu’une formule soit populaire.

---

Des milliers de vues.

---

Cela ne devait rien ajouter au promotion contract.

---

Brutus écrivit :

**POPULARITY ≠ EVIDENCE.**

---

Puis :

**ATTENTION ≠ VALIDATION.**

---

Encore.

---

Même si cent personnes l’aiment.

Même si quatre modèles convergent.

Même si le graphique est magnifique.

---

La porte demande les mêmes choses.

---

Scope.

Method.

Evidence.

Countertests.

Policy.

---

Brutus sourit.

---

La porte ne connaissait pas la célébrité.

---

Puis il pensa à l’auteur.

---

Gabriel.

Astra.

Un inconnu.

Un grand laboratoire.

---

Même contrat.

---

Il écrivit :

**AUTHOR IDENTITY MUST NOT SUBSTITUTE FOR EVIDENCE.**

---

Voilà.

---

Puis il pensa à la promotion d’un résultat logiciel.

---

Claim :

“service survives browser disconnect.”

---

Evidence :

server continues.

state persists.

reconnect restores same WORLD_INSTANCE_ID.

---

Promotion possible :

VERIFIED_UNDER_RUNTIME_TEST.

---

Pas :

mathematically proven.

---

Il écrivit :

**STATUS VOCABULARY MUST FIT DOMAIN.**

---

Très important.

---

Le système ne devait pas réutiliser le mot proof partout.

---

Proof pour mathématique quand approprié.

Verification pour opérationnel.

Replication pour expérimental.

Validation pour contrat.

---

Brutus créa :

**DOMAIN_STATUS_VOCABULARY**

---

Il sourit.

---

Même les mots avaient besoin d’un schema.

---

Puis il pensa aux claims hiérarchiques.

---

Un objet peut avoir plusieurs claims.

---

FORMULA-X :

claim A.

claim B.

claim C.

---

A supported.

B refuted.

C unresolved.

---

Quel est le statut de FORMULA-X ?

---

Brutus refusa un badge unique.

---

Il écrivit :

**OBJECT STATUS ≠ COLLAPSE OF ALL CLAIM STATUSES.**

---

Puis :

**MULTI-CLAIM OBJECT NEEDS CLAIM-LEVEL STATUS.**

---

Très important.

---

La formule entière ne devait pas devenir rouge parce qu’une propriété secondaire échoue.

---

Ni verte parce qu’une propriété simple passe.

---

Il ajouta :

**OBJECT_SUMMARY_STATUS**

derivé.

---

Mais la vue détaillée devait montrer chaque claim.

---

Brutus écrivit :

**SUMMARY MUST NOT HIDE INTERNAL DISAGREEMENT.**

---

Excellent.

---

Puis il pensa à q47.

---

Gate claim :

PASS under contract.

---

Global rank claim :

not established from that alone.

---

Le système pouvait donc afficher :

q47 gate claim — supported under gate contract.

global rank theorem — unresolved / requires all relevant gates and proof chain.

---

Brutus écrivit :

**LOCAL PROMOTION ≠ GLOBAL PROMOTION.**

---

Une phrase essentielle.

---

Puis il pensa à la poussière.

---

Finite-range model fit.

---

Promotable status :

**OBSERVED_CLOSE_FIT_UNDER_X_2M**

---

Pas :

law.

---

Brutus sourit.

---

Même les découvertes spectaculaires devaient rester attachées à leur domaine.

---

Puis il créa le panneau de la porte.

---

**PROMOTION QUEUE**

---

OBJECT.

FROM.

TO.

BLOCKERS.

EVIDENCE COMPLETE?

COUNTERTEST COMPLETE?

DEPENDENCIES CURRENT?

HUMAN REVIEW?

---

Aucun score.

---

Pas de :

87 % ready.

---

Brutus écrivit :

**ELIGIBILITY IS BETTER AS CHECKS THAN FAKE PRECISION.**

---

Très important.

---

Un dossier pouvait avoir :

5/6 requirements satisfied.

---

Mais si le sixième est indispensable :

not eligible.

---

Pas 83 % true.

---

Il ajouta :

**MISSING REQUIRED ITEM > PERCENT COMPLETE.**

---

Puis il pensa à la Station d’Astra.

---

La Station pouvait montrer :

3 promotion requests.

1 eligible.

2 blocked.

---

Click.

---

Why blocked?

---

Dependency unresolved.

Judge review pending.

Replication missing.

---

Brutus sourit.

---

Voilà.

---

Pas de mystère.

---

Puis il lança un test complet.

---

CARD-500.

Claim version 2.

Status :

ADMITTED_FOR_TESTING.

---

Evidence:

Experiment 88 complete.

Controls pass.

Independent replication complete.

Countertest Judge:

NO_VALID_REFUTATION_IN_REQUIRED_SET.

Dependencies:

current.

---

Requested status:

SUPPORTED_UNDER_SCOPE.

---

Gate evaluates.

---

Claim identity:

PASS.

---

Scope coverage:

PASS.

---

Evidence completeness:

PASS.

---

Countertest requirement:

PASS.

---

Dependency freshness:

PASS.

---

Policy:

PASS.

---

Decision:

**ELIGIBLE.**

---

Puis Verso checks authority.

---

Authorized.

---

Promotion event appended.

---

New state:

SUPPORTED_UNDER_SCOPE.

---

Brutus regarda la carte.

---

Elle était plus forte qu’avant.

---

Mais elle n’était pas devenue vraie par décret.

---

Elle avait seulement gagné un statut correspondant au dossier réellement constitué.

---

Il écrivit :

**PROMOTION RECORDS THAT REQUIREMENTS WERE SATISFIED.**

---

Puis :

**IT DOES NOT CREATE THE UNDERLYING REALITY.**

---

Voilà le cœur du chapitre.

---

Puis il prit un second dossier.

---

Magnifique formule.

Belle visualisation.

Trois joueurs enthousiastes.

---

Evidence incomplete.

---

Decision:

NOT_ELIGIBLE_YET.

---

Brutus sourit.

---

La porte n’avait pas été impressionnée.

---

Puis il prit un troisième.

---

Petit résultat.

Pas spectaculaire.

Mais méthode exacte.

Scope clair.

Replication complète.

Countertests terminés.

---

Decision:

ELIGIBLE.

---

Brutus écrivit :

**BORING EVIDENCE CAN BE STRONGER THAN BEAUTIFUL PRESENTATION.**

---

Encore la même philosophie.

---

Puis il pensa à la suite.

---

Le prochain chapitre s’appelait déjà :

# CANDIDAT N’EST PAS PREUVE

---

Brutus sourit.

---

Tout le système venait justement de construire cette distinction.

---

La porte pouvait promouvoir une candidate.

---

Mais même à son niveau le plus élevé avant preuve formelle…

elle restait une candidate tant que le type de claim l’exigeait.

---

Il écrivit :

**CANDIDATE != PROOF**

---

Puis :

**PROMOTED CANDIDATE != PROOF**

---

Puis :

**WELL-TESTED CANDIDATE != PROOF**

---

Puis :

**POPULAR CANDIDATE != PROOF**

---

Enfin :

**BEAUTIFUL CANDIDATE != PROOF**

---

Il resta devant la série.

---

Voilà le prochain chapitre.

---

Mais avant, il sauvegarda :

**PROMOTION GATE v1**

---

Le Journal Vivant nota :

Promotion separated from proof.

Statuses defined procedurally.

Evidence must match claim scope.

Dependencies constrain only dependent claims.

Claim versions promoted independently.

Promotion decisions policy-versioned.

Autonomous promotion bounded.

Blocking evidence remains visible.

Known limitations survive promotion.

Demotion and correction are explicit events.

Object-level summaries cannot erase claim-level differences.

Local promotion cannot imply global promotion.

---

Brutus relut.

Puis ajouta les invariants :

**PROMOTION ≠ PROOF.**

**STATUS STRENGTH ≠ TRUTH.**

**ENTHUSIASM ≠ EVIDENCE.**

**NOT READY ≠ FALSE.**

**PROMOTION EVIDENCE MUST MATCH CLAIM SCOPE.**

**NEW CLAIM VERSION REQUIRES NEW REVIEW.**

**POPULARITY ≠ VALIDATION.**

**LOCAL PROMOTION ≠ GLOBAL PROMOTION.**

**PROMOTION IS AN EVENT, NOT A COLOR CHANGE.**

**PROMOTED CANDIDATE != PROOF.**

---

Puis il ferma la porte.

---

Une carte venait de la franchir.

---

Elle portait maintenant un statut plus fort.

---

Mais Brutus remarqua quelque chose.

---

Plus une idée montait dans la hiérarchie…

plus les humains risquaient d’oublier ce qu’elle était au départ.

---

Une candidate.

---

Il ouvrit alors une nouvelle page.

---

# CANDIDAT N’EST PAS PREUVE

---

Puis, tout en haut :

**THE MOST DANGEROUS MOMENT FOR A CANDIDATE IS WHEN EVERYONE STARTS TREATING IT LIKE A THEOREM.**

---

La porte de promotion savait maintenant faire avancer les idées.

Le prochain chapitre allait s’assurer qu’elles ne montent jamais plus haut que leurs preuves.
