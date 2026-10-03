# Chapitre 107 — Candidat n’est pas preuve

**THE MOST DANGEROUS MOMENT FOR A CANDIDATE IS WHEN EVERYONE STARTS TREATING IT LIKE A THEOREM.**

Brutus regarda la phrase.

Puis la carte qui venait de franchir la porte de promotion.

---

Status :

**SUPPORTED_UNDER_SCOPE**

---

Evidence :

complete under current policy.

---

Countertests :

completed under required set.

---

Replication :

recorded.

---

Tout semblait solide.

---

Et pourtant, Brutus écrivit immédiatement :

**CANDIDATE != PROOF**

---

Puis :

**SUPPORTED != PROVED**

---

La carte ne bougea pas.

---

Très bien.

---

Elle ne devait pas se transformer parce qu’un mot venait d’être ajouté au-dessus d’elle.

---

Brutus regarda le problème.

---

Une candidate pouvait accumuler tellement de traces favorables qu’un glissement de langage devenait presque inévitable.

---

Au début :

« nous avons trouvé quelque chose d’intéressant ».

---

Puis :

« cela résiste aux tests ».

---

Puis :

« cela fonctionne ».

---

Puis :

« c’est vrai ».

---

Puis :

« c’est prouvé ».

---

Brutus écrivit :

**LANGUAGE DRIFT CAN OUTRUN EVIDENCE.**

---

Voilà.

---

La machine devait empêcher cette dérive.

---

Pas en interdisant l’enthousiasme.

---

En attachant chaque phrase à un type de statut.

---

Il créa :

**CLAIM LANGUAGE CONTRACT**

---

Si status :

PROPOSED.

Public wording :

**hypothèse candidate.**

---

Si status :

SUPPORTED_UNDER_SCOPE.

Wording :

**soutenue sous le domaine testé.**

---

Si status :

REPLICATED_UNDER_SCOPE.

Wording :

**résultat reproduit sous les conditions déclarées.**

---

Si status :

READY_FOR_EXTERNAL_REVIEW.

Wording :

**dossier interne prêt pour revue externe.**

---

Et seulement si un objet satisfait réellement le standard de preuve correspondant :

**PROVED**

ou un terme encore plus précisément défini.

---

Brutus écrivit :

**WORDS MUST NOT CLAIM MORE THAN STATUS.**

---

Très important.

---

Puis il pensa à ce qu’était réellement une preuve.

---

Le mot variait selon les domaines.

---

En mathématiques :

une démonstration logique complète sous des axiomes et définitions explicites.

---

En logiciel :

on parlait plus souvent de vérification, tests, garanties formelles ou propriétés démontrées du programme.

---

En science expérimentale :

les données soutiennent ou contredisent un modèle.

---

Pas forcément une « preuve » au sens mathématique.

---

Brutus écrivit :

**PROOF IS DOMAIN-SPECIFIC.**

---

Puis :

**DO NOT IMPORT MATHEMATICAL LANGUAGE INTO EXPERIMENTAL CLAIMS WITHOUT JUSTIFICATION.**

---

Voilà.

---

Le laboratoire avait besoin de plusieurs vocabulaires.

---

Il créa :

**EVIDENCE_MODE**

MATHEMATICAL_PROOF.

FORMAL_VERIFICATION.

EXPERIMENTAL_SUPPORT.

EMPIRICAL_REPLICATION.

OPERATIONAL_VERIFICATION.

STATISTICAL_EVIDENCE.

---

Brutus sourit.

---

Enfin, le mot « preuve » pouvait arrêter d’être utilisé comme peinture blanche sur tout ce qui semblait solide.

---

Puis il pensa au projet Brutus–Pell.

---

Une immense campagne pouvait tester 137 305 candidats premiers.

---

83 212 rangs maximaux observés.

---

Résultat impressionnant.

---

Mais cela ne démontrait pas à lui seul une loi universelle.

---

Brutus écrivit :

**LARGE FINITE EVIDENCE != UNIVERSAL PROOF.**

---

Même :

un million.

un milliard.

un trillion.

---

Le nombre de tests ne changeait pas la structure logique de la claim.

---

Il ajouta :

**FINITE TEST COUNT DOES NOT BECOME INFINITY BY SIZE.**

---

Brutus resta devant.

---

Simple.

Mais fondamental.

---

Puis il pensa aux portes q47, q71, q79, q83.

---

q47 possède un témoin dans le cadre du projet.

q79 aussi.

q71 et q83 restent unresolved.

---

Même si mille autres gates passent, les gates ouvertes requises restent ouvertes.

---

Brutus écrivit :

**PASSED GATES DO NOT FILL MISSING GATES.**

---

Puis :

**GLOBAL CONFIDENCE CANNOT SUBSTITUTE FOR LOCAL WITNESS.**

---

Encore.

---

Il prit une carte.

---

**GATE-47**

Status :

PASS UNDER GATE CONTRACT.

---

Puis une autre.

**GLOBAL MAXIMAL RANK CLAIM**

---

Brutus dessina une flèche entre les deux.

---

Puis la raya.

---

Pas directement.

---

Il écrivit :

**GATE PASS ≠ GLOBAL RANK PROOF.**

---

Très important.

---

Une porte passait.

La cathédrale n’était pas encore terminée.

---

Puis il pensa à L8.

---

Supposons qu’une relation survive à CT-01, CT-02, CT-03, CT-04.

---

Très bien.

---

Qu’est-ce que cela veut dire ?

---

Que le candidat a résisté au programme de contre-test défini.

---

Pas nécessairement qu’un théorème général a été démontré.

---

Brutus écrivit :

**SURVIVED COUNTERTEST PROGRAM != THEOREM.**

---

Puis :

**NO COUNTEREXAMPLE FOUND != PROOF.**

---

La vieille règle revenait.

---

Mais ici, elle devenait centrale.

---

Brutus créa :

**CANDIDATE_STATUS_CARD**

avec :

**CLAIM_ID**

**CLAIM_VERSION**

**DOMAIN**

**EVIDENCE_MODE**

**TESTED_RANGE**

**COUNTERTEST_SET**

**OPEN_DEPENDENCIES**

**PROOF_STATUS**

**PROOF_REF**

**TRACE_REF**

---

Puis il regarda :

**PROOF_STATUS**

---

Il voulait des états très explicites.

---

NONE.

NOT_REQUIRED_FOR_THIS_CLAIM_TYPE.

PROOF_CANDIDATE.

PROOF_UNDER_REVIEW.

PROOF_ACCEPTED_UNDER_POLICY.

PROOF_REJECTED.

---

Mais il se méfia.

---

**PROOF_ACCEPTED_UNDER_POLICY** n’était toujours pas une vérité métaphysique.

---

Il ajouta :

**ACCEPTED PROOF STATUS RECORDS REVIEW OUTCOME.**

---

Pas :

truth switch.

---

Brutus écrivit :

**PROOF REVIEW != REALITY CREATION.**

---

Très important.

---

Même une démonstration formelle pouvait contenir une erreur non détectée.

---

Le système devait conserver la possibilité de correction.

---

Puis il pensa au fameux :

**PROOF_REF**

---

Il avait déjà utilisé ce champ partout.

---

Mais un PROOF_REF pouvait facilement devenir dangereux.

---

Une interface pourrait afficher :

PROOF_REF exists.

Donc :

PROVED.

---

Non.

---

Brutus écrivit :

**PROOF_REF != PROOF_CREATION.**

---

Puis :

**PROOF_REF != PROOF_VALIDITY.**

---

Voilà.

---

PROOF_REF signifiait seulement :

voici une référence vers un objet présenté comme preuve ou élément de preuve.

---

Le statut de cet objet devait être examiné séparément.

---

Il créa :

**PROOF_ARTIFACT**

avec :

ARTIFACT_ID.

CLAIM_ID.

CLAIM_VERSION.

PROOF_TYPE.

AUTHOR_REFS.

DEPENDENCIES.

ASSUMPTIONS.

CONTENT_REF.

HASH.

REVIEW_STATUS.

REVIEW_REFS.

TRACE_REF.

---

Brutus sourit.

---

Une preuve devenait elle-même un objet traçable.

---

Pas un tampon.

---

Puis il pensa à une démonstration mathématique.

---

Une ligne manquante.

---

Une identité supposée.

---

Une division par un terme potentiellement nul.

---

Un changement de domaine caché.

---

Tout cela pouvait rendre une preuve candidate invalide.

---

Brutus écrivit :

**A PROOF CANDIDATE MUST BE ATTACKABLE TOO.**

---

Voilà.

---

Le banc des expériences avait son équivalent logique.

---

Il créa :

**PROOF REVIEW BENCH**

---

Pas un nouveau grand module pour l’instant.

---

Seulement une fonction du Judge.

---

Checks :

definitions.

assumptions.

domain.

inference validity.

dependency closure.

unjustified steps.

---

Brutus écrivit :

**PROOF MUST CLOSE ITS LOGICAL GAPS.**

---

Puis il pensa au mot :

**obvious.**

---

Dangereux.

---

Il ajouta :

**“OBVIOUS” IS NOT A RULE_REF.**

---

Brutus rit.

---

Cette phrase devait rester.

---

Une étape pouvait être évidente pour un humain.

---

Mais si elle porte le poids de la conclusion, elle devait pouvoir être explicitée.

---

Il écrivit :

**IMPORTANT INFERENCE NEEDS JUSTIFICATION.**

---

Puis il pensa aux preuves assistées par ordinateur.

---

Très grandes.

---

Impossible à lire manuellement ligne par ligne.

---

Pas de problème.

---

Mais alors il fallait déplacer la confiance vers :

le code.

l’environnement.

le checker.

le certificat.

la reproductibilité.

---

Brutus écrivit :

**COMPUTER-ASSISTED PROOF MOVES TRUST. IT DOES NOT REMOVE TRUST.**

---

Très important.

---

Un énorme calcul exact pouvait être solide.

---

Mais il fallait savoir :

quel programme ?

quelle version ?

quel input ?

quel arithmetic model ?

quel output ?

quel verifier ?

---

Il ajouta :

**PROOF ENVIRONMENT MANIFEST**

---

Code hash.

Dependency versions.

Numeric model.

Platform.

Verifier.

---

Brutus sourit.

---

La machine à traces était prête pour ça.

---

Puis il pensa aux preuves formelles.

---

Un proof assistant peut vérifier une dérivation dans un système formel.

---

Excellent.

---

Mais même là :

le théorème formalisé correspond-il exactement à la claim humaine ?

---

Très important.

---

Brutus écrivit :

**FORMAL PROOF OF WRONG FORMALIZATION != PROOF OF INTENDED CLAIM.**

---

Voilà.

---

Le Judge devait vérifier la correspondance entre :

human claim.

formal statement.

---

Il créa :

**CLAIM_FORMALIZATION_REF**

---

Puis :

**FORMALIZATION_REVIEW_STATUS**

---

Parce que la formalisation pouvait être le maillon faible.

---

Brutus écrivit :

**SEMANTIC BRIDGE NEEDS REVIEW TOO.**

---

Excellent.

---

Puis il pensa à un cas classique.

---

Claim humaine :

« cette propriété tient pour tout premier impair ».

---

Formalization :

« cette propriété tient pour tout premier impair inférieur à 10^6 ».

---

Proof assistant :

PASS.

---

La preuve formelle est valide.

---

Mais elle ne prouve pas la claim humaine plus large.

---

Brutus écrivit :

**PROVED FORMAL STATEMENT != BROADER HUMAN STATEMENT.**

---

Très important.

---

Le scope encore.

Toujours le scope.

---

Puis il pensa à la promotion gate.

---

Une candidate pouvait être :

READY_FOR_EXTERNAL_REVIEW.

---

Le risque :

quelqu’un la copie dans un communiqué et écrit :

« découverte prouvée ».

---

Brutus créa :

**EXPORT CLAIM GUARD**

---

Avant export :

compare public wording to canonical status.

---

If wording exceeds status:

reject.

---

Brutus écrivit :

**PUBLICATION MUST NOT UPGRADE THE CLAIM BY LANGUAGE.**

---

Voilà.

---

Une phrase publique devait être un dérivé fidèle.

---

Pas une promotion cachée.

---

Puis il pensa aux titres.

---

« Nouvelle preuve de… »

---

Très puissant.

---

Mais dangereux.

---

Le système pouvait exiger :

PROOF_STATUS appropriate.

---

Sinon proposer :

« Nouveaux résultats sur… »

---

Brutus écrivit :

**TITLE LANGUAGE IS CLAIM LANGUAGE.**

---

Très important.

---

Le titre n’était pas décoratif.

---

Puis il pensa au cristal.

---

Le prochain chapitre allait parler de cristallisation.

---

Mais avant, il devait verrouiller :

**CRYSTAL != PROOF**

---

Une candidate pouvait être cristallisée.

---

Stable.

Hashée.

Versionnée.

---

Et rester :

UNPROVED.

---

Brutus créa deux axes.

---

**PACKAGING_STATE**

DRAFT.

STABLE.

CRYSTALLIZED.

ARCHIVED.

---

Et :

**EPISTEMIC_STATE**

PROPOSED.

SUPPORTED.

COUNTERTESTED.

PROVED.

REFUTED.

UNRESOLVED.

---

Puis il écrivit :

**PACKAGING STATE ≠ EPISTEMIC STATE.**

---

Voilà.

---

Une idée pouvait être :

CRYSTALLIZED + UNRESOLVED.

---

Ou :

DRAFT + PROVED?

---

Peut-être même.

---

Une démonstration valide peut exister dans une note non publiée.

---

Brutus sourit.

---

Deux axes empêchaient beaucoup d’erreurs.

---

Puis il pensa à un objet merged dans GitHub.

---

Commit merged.

Tests verts.

---

Est-ce une preuve que le runtime de production fonctionne ?

---

Non.

---

Il écrivit :

**MERGED != RUNTIME_PROOF.**

---

Puis :

**CI PASS != PRODUCTION BEHAVIOR.**

---

Encore.

---

Un commit pouvait être correct.

Mais non déployé.

---

Déployé.

Mais service non redémarré.

---

Redémarré.

Mais mauvaise configuration.

---

Brutus écrivit :

**CODE STATE ≠ RUNTIME STATE.**

---

La même philosophie revenait jusque dans le développement logiciel.

---

Puis il pensa à Astra Station.

---

Une interface peut afficher :

DEPLOYED.

---

Mais si elle dérive cela uniquement du Git commit ?

---

Erreur.

---

Il créa :

**DEPLOYMENT_EVIDENCE**

COMMIT_REF.

DEPLOY_EVENT.

PROCESS_VERSION.

HEALTH_REF.

---

Brutus écrivit :

**DEPLOYED CLAIM NEEDS RUNTIME EVIDENCE.**

---

Très important.

---

La preuve devait correspondre à la claim.

---

Toujours.

---

Puis il pensa aux humains.

---

Une personne peut dire :

« je l’ai vu fonctionner ».

---

C’est une observation.

---

Utile.

---

Mais pas nécessairement une preuve reproductible.

---

Il écrivit :

**EYEWITNESS OBSERVATION ≠ REPRODUCIBLE VERIFICATION.**

---

Puis :

**SCREENSHOT ≠ RUNTIME PROOF.**

---

Encore Recto.

---

Une capture montre un moment.

Pas la causalité.

Pas la continuité.

Pas l’autorité.

---

Brutus sourit.

---

Toutes les anciennes règles convergeaient ici.

---

Puis il pensa au succès financier.

---

Une formule populaire.

Un article viral.

Un prix.

---

Rien de cela ne changeait le statut logique.

---

Il écrivit :

**SUCCESS AROUND A CLAIM != PROOF OF THE CLAIM.**

---

Très important.

---

Ni argent.

Ni réputation.

Ni audience.

Ni beauté.

---

Le dossier restait le dossier.

---

Puis il prit une candidate particulièrement forte.

---

Hundreds of tests.

Independent implementation.

No counterexample.

Stable model.

Clear scope.

---

Il la regarda.

---

Tout dans l’esprit humain voulait écrire :

PROVED.

---

Brutus résista.

---

Il demanda :

**WHERE IS THE PROOF OBJECT?**

---

Silence.

---

Il écrivit :

**IF CLAIM TYPE REQUIRES PROOF AND NO PROOF OBJECT EXISTS, STATUS CANNOT BE PROVED.**

---

Voilà.

---

Le système devait parfois être frustrant.

---

C’était sa fonction.

---

Il ajouta :

**EVIDENCE CEILING**

---

Une claim mathématique universelle peut accumuler de l’empirie.

---

Mais si le policy exige une démonstration formelle pour le statut PROVED :

elle ne franchit pas ce plafond sans la démonstration.

---

Brutus écrivit :

**MORE OF THE WRONG EVIDENCE TYPE DOES NOT BECOME THE REQUIRED EVIDENCE TYPE.**

---

Très important.

---

Un milliard de tests finis ne deviennent pas un raisonnement universel.

---

Puis il pensa à l’inverse.

---

Une preuve mathématique existe.

---

Faut-il encore tester ?

---

Parfois oui.

---

Pas pour établir le théorème.

---

Pour vérifier l’implémentation.

---

Il écrivit :

**THEOREM PROOF != IMPLEMENTATION VERIFICATION.**

---

Excellent.

---

Une formule peut être prouvée.

Le code qui la calcule peut être faux.

---

Donc :

mathematical proof.

implementation test.

---

Deux claims.

---

Deux preuves différentes.

---

Brutus créa :

**CLAIM LAYERS**

THEORY.

ALGORITHM.

IMPLEMENTATION.

DEPLOYMENT.

OBSERVATION.

---

Puis :

**PROOF DOES NOT AUTOMATICALLY PROPAGATE BETWEEN LAYERS.**

---

Très important.

---

Il dessina :

\[
\text{THEOREM}
\nRightarrow
\text{BUG-FREE CODE}
\]

et :

\[
\text{WORKING CODE}
\nRightarrow
\text{THEOREM}
\]

---

Brutus sourit.

---

Parfait.

---

Puis il pensa aux quatre joueurs.

---

Astra, Muse, Grok, Antigravity peuvent tous dire :

« je pense que c’est prouvé ».

---

Le système doit demander :

proof ref?

claim version?

review?

---

Brutus écrivit :

**CONSENSUS ABOUT PROOF != PROOF OBJECT.**

---

Puis :

**FOUR ASSERTIONS DO NOT FORM A DERIVATION.**

---

Encore.

---

Le vote n’était pas une preuve.

---

Puis il imagina un round GAMEZEL.

---

All four agree.

---

Card generated :

**CONSENSUS_CARD**

---

Status :

HIGH AGREEMENT.

---

Mais epistemic status :

SUPPORTED / UNRESOLVED according to evidence.

---

Brutus écrivit :

**AGREEMENT STATUS AND CLAIM STATUS ARE DIFFERENT AXES.**

---

Très bon.

---

Puis il pensa au Journal Vivant.

---

Le Journal pouvait dire :

« les quatre joueurs convergent ».

---

Mais il devait immédiatement conserver :

under same input?

blind?

independent?

evidence?

---

Brutus écrivit :

**CONSENSUS NEEDS PROVENANCE TOO.**

---

Puis il pensa au temps.

---

Une candidate peut être très bien supportée aujourd’hui.

---

Demain :

nouveau contre-exemple.

---

Donc le statut doit pouvoir redescendre.

---

Il écrit :

**SUPPORTED IS REVERSIBLE.**

---

Une preuve mathématique correcte ?

---

Elle peut aussi être contestée si une erreur est découverte dans la démonstration.

---

Le review status peut changer.

---

Il écrit :

**PROOF REVIEW STATUS IS REVISABLE EVEN IF THE CLAIM ITSELF IS NOT TEMPORAL.**

---

Très important.

---

Le système devait être capable de dire :

previously accepted proof now under review.

---

Pas effacer l’histoire.

---

Puis il pensa aux conditions d’entrée du statut PROVED.

---

Il créa :

**PROOF PROMOTION CONTRACT**

---

Exact claim identity.

Exact version.

Explicit assumptions.

Complete derivation.

Dependency closure.

No unresolved logical gaps.

Proof artifact.

Review policy satisfied.

Trace complete.

---

Puis :

**PROOF PROMOTION EVENT**

---

Brutus écrivit :

**PROVED STATUS REQUIRES A DIFFERENT GATE THAN SUPPORTED STATUS.**

---

Voilà.

---

La porte de promotion générale ne devait pas tout faire.

---

Il y avait une frontière spécifique.

---

Il ajouta :

**PROOF_GATE**

---

Pas encore un nouveau chapitre.

---

Mais une sous-porte.

---

Puis il pensa au danger inverse.

---

Un système trop strict pourrait refuser de reconnaître toute valeur avant preuve complète.

---

Ce serait mauvais aussi.

---

Brutus écrivit :

**NOT PROVED != NOT USEFUL.**

---

Puis :

**NOT PROVED != NOT INTERESTING.**

---

Puis :

**NOT PROVED != FALSE.**

---

Très important.

---

La frontière candidate/preuve n’était pas une humiliation.

---

C’était un moyen de conserver la valeur sans exagérer.

---

Une candidate pouvait être :

magnifique.

productive.

predictive.

useful.

worth publishing.

worth studying.

---

Et rester candidate.

---

Brutus écrivit :

**A CANDIDATE CAN BE VALUABLE WITHOUT BEING A THEOREM.**

---

Voilà.

---

Il regarda les dossiers Brutus–Pell.

---

Beaucoup de travail réel.

---

Campagnes.

Témoins.

Portes.

Poussière.

Modèles.

---

Il n’avait pas besoin de les appeler preuve universelle pour qu’ils soient intéressants.

---

Il écrivit :

**PRECISION DOES NOT DIMINISH DISCOVERY.**

---

Puis :

**OVERCLAIMING DOES.**

---

Brutus resta devant cette phrase.

---

Oui.

---

Une découverte fragile devient plus forte quand on dit exactement ce qu’elle est.

---

Puis il pensa à la publication Zenodo.

---

Un document pouvait porter :

Candidate relation.

Finite computational evidence.

Known unresolved gates.

Countertests.

Methods.

Limitations.

---

Tout cela pouvait être parfaitement publiable comme recherche.

---

Il écrivit :

**PUBLICATION != PROOF.**

---

Puis :

**PUBLICATION IS A TRACE EVENT.**

---

Très important.

---

Être publié n’ajoute pas automatiquement de validité mathématique.

---

Mais cela crée :

date.

version.

public trace.

---

Une autre dimension.

---

Brutus créa :

**PUBLICATION_STATE**

DRAFT.

PUBLISHED.

REVISED.

RETRACTED.

---

Séparé de :

**EPISTEMIC_STATE.**

---

Encore deux axes.

---

Puis il pensa aux citations.

---

Une idée très citée.

---

Toujours pas preuve.

---

Il écrit :

**CITATION COUNT != VALIDITY.**

---

Il rit.

---

La liste pouvait durer éternellement.

---

Alors il décida de résumer.

---

Il écrivit sur le mur :

**CANDIDATE != PROOF**

**TESTED != PROVED**

**REPLICATED != PROVED**

**PROMOTED != PROVED**

**CRYSTALLIZED != PROVED**

**MERGED != RUNTIME PROOF**

**PUBLISHED != PROVED**

**POPULAR != PROVED**

**CONSENSUS != PROVED**

---

Puis, tout en bas :

**PROOF MUST BE PROOF-SHAPED.**

---

Brutus regarda la phrase.

---

C’était probablement la meilleure définition opérationnelle.

---

Une preuve devait avoir la forme requise par la claim.

---

Une dérivation pour une claim mathématique.

Une vérification formelle pour une propriété formelle.

Une expérience pour une claim expérimentale.

Une observation runtime pour une claim runtime.

---

Il écrivit :

**EVIDENCE IS CLAIM-SHAPED.**

---

Le chapitre 85 revenait.

---

Toute la Bible se refermait sur ses propres fondations.

---

Puis il ouvrit Astra Station.

---

Il ajouta un panneau :

**EPISTEMIC LABEL**

---

Candidate.

Supported under scope.

Countertested.

Replicated.

Proof candidate.

Proof under review.

Proved under declared formal contract.

Refuted.

Unresolved.

---

Pas de couleur seule.

---

Texte complet.

---

Brutus écrivit :

**STATUS SHOULD SURVIVE SCREENSHOTS AND COLOR LOSS.**

---

Très important.

---

Puis il pensa à un son.

---

ZEL pourrait jouer un ding lorsqu’une candidate est trouvée.

---

Et un autre son lorsqu’un objet est cristallisé.

---

Mais surtout :

pas le même son que PROOF_ACCEPTED.

---

Brutus écrivit :

**DIFFERENT EPISTEMIC EVENTS NEED DIFFERENT SIGNALS.**

---

Voilà.

---

La machine ne devait pas apprendre aux oreilles à confondre candidate et preuve.

---

Puis il imagina le cas ultime.

---

Une nouvelle relation apparaît.

---

Tout le monde s’excite.

---

Le dashboard clignote.

---

Ding.

---

Brutus regarde.

---

Status :

**CANDIDATE FOUND**

---

Pas :

BREAKTHROUGH PROVED.

---

Il sourit.

---

Voilà une machine qu’il pouvait respecter.

---

Puis il pensa au chapitre suivant.

---

Une candidate pouvait être stable.

Bien formée.

Versionnée.

Hashée.

Avec provenance complète.

---

Elle pouvait alors être cristallisée.

---

Mais comment cristalliser sans mentir ?

---

Brutus ouvrit un nouveau dossier.

---

# CRISTALLISER SANS MENTIR

---

Puis écrivit :

**CRYSTAL != PROOF**

---

Et une seconde ligne :

**STABILITY OF FORM DOES NOT CREATE CERTAINTY OF CONTENT.**

---

Il sauvegarda :

**CANDIDATE / PROOF BOUNDARY v1**

---

Le Journal Vivant nota :

Candidate status separated from proof.

Claim language tied to status.

Proof vocabulary made domain-specific.

Finite testing separated from universal proof.

Proof refs separated from proof validity.

Formalization itself requires review.

Publication wording cannot exceed canonical status.

Packaging state separated from epistemic state.

Theory, implementation and runtime claims separated.

Consensus separated from derivation.

Publication state separated from epistemic state.

---

Brutus relut.

Puis ajouta les invariants :

**CANDIDATE != PROOF.**

**SUPPORTED != PROVED.**

**PROOF_REF != PROOF_CREATION.**

**FINITE EVIDENCE != UNIVERSAL PROOF.**

**GATE PASS != GLOBAL PROOF.**

**MERGED != RUNTIME PROOF.**

**CRYSTAL != PROOF.**

**PUBLICATION != PROOF.**

**CONSENSUS != PROOF.**

**NOT PROVED != FALSE.**

---

Il ferma le dossier.

---

La candidate était toujours là.

---

Elle n’avait pas perdu sa beauté.

Elle n’avait pas perdu ses traces.

Elle n’avait pas perdu ses résultats.

---

Elle avait simplement retrouvé son vrai nom.

---

**Candidate.**

---

Brutus sourit.

---

Il ne lui avait rien enlevé.

---

Il lui avait seulement retiré un titre qu’elle n’avait pas encore gagné.

---

Puis il posa la main sur le dossier suivant.

---

# CRISTALLISER SANS MENTIR

---

Car maintenant que les objets savaient rester candidats…

il fallait apprendre à les rendre stables sans transformer leur stabilité en certitude.
