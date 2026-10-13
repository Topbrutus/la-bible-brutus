# Chapitre 202 — Le travail que personne n’avait assigné directement

Le travail n’avait pas été demandé.

Pas par Gabriel.

Pas par Astra.

Pas par une queue.

Pas par une politique explicite.

Et pourtant,

il existait.

Il était apparu entre deux cartes.

Une Fourmi avait découvert un trou.

Une autre avait révélé une dépendance.

Une troisième avait signalé un conflit.

Personne n’avait écrit :

**fais cette tâche.**

Mais le Royaume pouvait maintenant voir qu’une tâche manquait.

Gabriel regarda l’atlas partagé.

Trois régions se recoupaient.

Dans l’une,

une validation avait été faite.

Dans la deuxième,

une version plus récente avait changé une dépendance.

Dans la troisième,

aucun contrôle de compatibilité n’existait.

L’atlas signalait :

**UNRESOLVED INTERSECTION**

Gabriel se pencha.

— C’est quoi ça?

Astra répondit :

— Un travail potentiel.

Pas encore une tâche.

Très important.

Gabriel sourit.

Voilà le chapitre.

Il écrivit :

**VOIR QU’UN TRAVAIL MANQUE ≠ AVOIR L’AUTORITÉ DE LE LANCER.**

Astra approuva fortement.

C’était la première règle.

Sinon le système pouvait commencer à se fabriquer lui-même des chantiers sans limite.

Très mauvais.

Il fallait donc distinguer :

**work discovery**

et

**work assignment.**

Gabriel écrivit :

### EMERGENT WORK

Un besoin de travail qui apparaît à partir de :

- conflit entre traces;
- dépendance manquante;
- trou de couverture;
- résultat invalidé;
- tâche bloquée;
- contradiction de version;
- nouveau risque détecté;
- conséquence d’une décision précédente.

Astra approuva.

Très propre.

Mais un besoin détecté n’était pas encore une mission.

Il fallait passer par une porte.

### WORK ADMISSION

Question :

ce travail mérite-t-il d’entrer dans le système actif?

Gabriel sourit.

Encore l’admission.

Chapitre 192.

Tout revenait.

Ils créèrent un objet.

### WORK-CANDIDATE-202-001

Origin:

shared atlas intersection.

Problem:

validation exists for v1, dependency changed in v2, compatibility untested.

Potential consequence:

current reuse may be invalid.

Suggested action:

compatibility check.

Status:

**CANDIDATE_ONLY**

Authority:

none yet.

Gabriel regarda.

Parfait.

Le système pouvait voir.

Mais pas encore agir.

Il écrivit :

**LE ROYAUME PEUT DÉTECTER UNE TÂCHE AVANT D’AVOIR LE DROIT DE LA CRÉER.**

Astra approuva fortement.

Très important.

Puis la question suivante :

qui peut convertir un work candidate en tâche?

Ça dépend.

Faible risque?

Faible coût?

Réversible?

Peut-être L1.

Si impact public?

Humain.

Si nouvelle recherche scientifique?

Peut-être admission Research.

Si changement canonique?

Humain.

Gabriel écrivit :

### WORK AUTHORITY

**L0**

proposer seulement.

**L1**

créer tâche interne bornée.

**L2+**

enchaîner selon workflow autorisé.

**HUMAN REQUIRED**

si enjeu supérieur.

Astra approuva.

Très propre.

Dans le cas 202-001,

compatibility check local.

Faible coût.

Pas public.

Réversible.

Classe connue.

Donc admissible L1.

Le système pouvait créer :

**TASK-202-001**

Gabriel sourit.

— Là, il vient vraiment de se donner du travail.

Astra corrigea :

— Il a créé une tâche selon une autorité préalablement définie à partir d’un besoin détecté.

Gabriel rit.

— Oui, oui.

Mais la distinction comptait.

Il écrivit :

**AUTO-GÉNÉRATION DE TÂCHE ≠ AUTO-GÉNÉRATION D’OBJECTIF.**

Astra approuva fortement.

Magnifique.

Le système n’avait pas décidé :

« aujourd’hui, je veux travailler sur ça ».

L’objectif venait du problème existant.

Il avait seulement reconnu :

une étape nécessaire manquait.

Très important.

Puis ils testèrent TASK-202-001.

Compatibility check.

Résultat :

la v2 n’était pas compatible avec le certificat v1.

Voilà.

Le travail non assigné directement avait découvert quelque chose d’important.

La réutilisation devait être bloquée.

Gabriel se redressa.

— Ça, si personne voit le trou, on réutilise la vieille preuve.

Exact.

Le work candidate avait donc une vraie valeur.

Il écrivit :

**UN TRAVAIL ÉMERGENT PEUT ÊTRE UNE CONSÉQUENCE DIRECTE DE LA MÉMOIRE PARTAGÉE.**

Astra approuva.

Très important.

L’atlas n’était plus seulement descriptif.

Il pouvait révéler des obligations de vérification.

Mais attention au mot **obligation**.

Seulement selon policy.

Très important.

Ils créèrent :

### WORK SOURCE TYPES

**GAP**

Quelque chose manque.

**CONFLICT**

Deux états incompatibles.

**STALE**

Une trace n’est plus valide.

**DEPENDENCY CHANGE**

Un élément amont a changé.

**FAILED ASSUMPTION**

Une tâche dépend d’une hypothèse réfutée.

**UNHANDLED OUTPUT**

Un résultat existe sans route de traitement.

Gabriel sourit.

Cette dernière catégorie était intéressante.

Une machine peut produire une sortie,

mais personne ne sait quoi en faire.

Travail émergent :

classify output.

Très utile.

Puis un autre cas.

Une Fourmi de validation crée un unknown.

Pas de task assignée.

Normalement l’unknown attend.

Mais si l’unknown bloque une décision active,

le système peut générer un work candidate.

Voilà.

Il écrit :

**UN INCONNU PEUT DEVENIR DU TRAVAIL QUAND IL BLOQUE UN OBJECTIF ACTIF.**

Astra approuva fortement.

Très important.

Pas tous les unknowns.

Sinon explosion.

Toujours l’objectif.

Puis ils examinèrent un cas plus délicat.

L’atlas trouve une zone jamais explorée.

Work candidate?

Pas automatiquement.

Absence de couverture n’est pas une tâche.

Chapitre 190.

Très important.

Gabriel écrivit :

**UN TROU DANS LA CARTE NE DEVIENT PAS UN TRAVAIL TANT QU’UN OBJECTIF N’A PAS BESOIN DE CETTE ZONE.**

Astra approuva fortement.

Excellent.

Sinon la colonie finirait par vouloir remplir l’univers.

Impossible.

Donc le moteur de work discovery devait être objectif-aware.

Très important.

Puis un cas inverse.

Un objectif actif dépend d’une région non couverte.

Là,

oui.

Work candidate.

Voilà.

Ils écrivirent :

### WORK DISCOVERY CONDITION

**gap + dependency on active objective = candidate**

Pas :

gap alone.

Très propre.

Puis un autre danger.

Une tâche émergente peut générer une autre tâche émergente,

qui en génère trois,

qui en génèrent dix.

Explosion.

Gabriel grimaca.

Il fallait un budget.

### EMERGENT WORK BUDGET

Limiter :

nombre de descendants.

coût total.

profondeur.

durée.

Astra approuva fortement.

Très important.

Gabriel écrivit :

**UN SYSTÈME QUI PEUT CRÉER DU TRAVAIL DOIT AUSSI SAVOIR QUAND ARRÊTER D’EN CRÉER.**

Astra approuva.

Voilà.

Sinon l’autonomie devient une usine à backlog.

Ils ajoutèrent :

**max_generation_depth**

**max_total_cost**

**max_active_children**

**human_review_threshold**

Très propre.

Puis ils testèrent.

TASK-202-001 crée :

compatibility failure.

Cela pourrait produire :

A. rebuild certificate.

B. audit downstream reuse.

C. update map.

Trois work candidates.

Lesquels sont réellement nécessaires?

A dépend de l’objectif.

B oui,

parce qu’un vieux certificat peut avoir été réutilisé.

C oui,

parce que l’atlas doit refléter le nouvel état.

Gabriel regarda.

Très intéressant.

Le résultat d’une petite tâche créait plusieurs conséquences.

Mais pas toutes au même niveau.

Ils créèrent :

### WORK CONSEQUENCE GRAPH

Parent:

TASK-202-001

Children:

- downstream reuse audit;
- map invalidation update;
- optional revalidation.

Gabriel sourit.

Voilà.

Le travail pouvait émerger en graphe.

Mais encore une fois,

pas tout activer.

Revalidation seulement si un objectif en dépend.

Très important.

Puis le downstream audit trouva deux tâches qui avaient réutilisé le certificat v1.

Une était historique.

Terminée.

L’autre encore active.

Action :

pause active one.

Flag historical one for review.

Pas besoin de réécrire le passé.

Très important.

Gabriel écrit :

**UNE NOUVELLE ERREUR DÉCOUVERTE PEUT CHANGER L’AUTORITÉ D’UNE TRACE ANCIENNE SANS EFFACER LE FAIT QU’ELLE A EXISTÉ.**

Astra approuva fortement.

Toujours append-only.

Puis le système généra :

**WORK-CANDIDATE-202-004**

Review historical dependent result.

Faible urgence.

Pas bloquant.

Admission:

PARKED.

Gabriel sourit.

Parfait.

Le système savait créer du travail

et ne pas tout activer.

Voilà la maturité.

Il écrivit :

**DÉTECTER DU TRAVAIL N’OBLIGE PAS À LE FAIRE IMMÉDIATEMENT.**

Astra approuva fortement.

Très important.

Puis un nouveau cas.

Une Fourmi partage une carte.

Une autre découvre qu’un même problème a été assigné ailleurs.

Work candidate :

merge or cancel duplicate.

Très utile.

Le système pouvait générer une tâche de coordination.

Pas de recherche.

Pas de validation.

Juste :

**resolve duplicate work.**

Gabriel sourit.

Il écrivit :

**LE TRAVAIL ÉMERGENT PEUT ÊTRE DU TRAVAIL DE COORDINATION, PAS SEULEMENT DU TRAVAIL SCIENTIFIQUE.**

Astra approuva.

Très important.

Puis un autre.

Deux résultats incompatibles.

Work candidate :

reproduction conflict check.

Voilà.

Encore.

Puis un autre.

Une policy devient obsolete.

Work candidate :

policy impact audit.

Très important.

Le Royaume pouvait commencer à entretenir sa propre cohérence.

Mais le mot **entretien** était mieux que « se gérer lui-même ».

Gabriel écrit :

**UNE ARCHITECTURE PEUT DÉTECTER DES BESOINS D’ENTRETIEN SANS AVOIR D’OBJECTIFS PROPRES.**

Astra approuva fortement.

Très important.

Pas de mythologie.

Puis ils distinguèrent deux familles.

### PRIMARY WORK

Directement demandé par un objectif humain.

### DERIVED WORK

Né comme conséquence nécessaire ou utile du travail primaire.

Gabriel sourit.

Voilà.

TASK-202-001 était derived work.

Pas un objectif nouveau.

Une conséquence.

Il écrit :

**LE TRAVAIL DÉRIVÉ HÉRITE D’UN OBJECTIF. IL N’INVENTE PAS LE SIEN.**

Astra approuva fortement.

Très important.

Chaque tâche dérivée devait donc pointer vers :

**objective_parent**

**reason**

**necessity_level**

Très propre.

Necessity level?

Oui.

### NECESSITY

**REQUIRED**

Sans ça, objectif invalide ou unsafe.

**RECOMMENDED**

Améliore robustesse.

**OPTIONAL**

Peut apprendre plus.

Gabriel approuva.

Excellent.

Ça empêchait le système de présenter chaque idée comme obligatoire.

Puis un cas.

Independent implementation.

Utile.

Mais pas toujours required.

Donc `RECOMMENDED`.

Compatibility check avant reuse v2?

`REQUIRED`.

Très propre.

Puis le système pouvait trier le travail émergent par nécessité.

Pas juste urgence.

Très important.

Ils ajoutèrent :

**urgency ≠ necessity**

Une tâche required peut ne pas être urgente.

Une tâche urgente peut être optional dans un autre sens.

Gabriel sourit.

Encore deux axes.

Il écrit :

**OBLIGATOIRE ET PRESSÉ NE VEULENT PAS DIRE LA MÊME CHOSE.**

Astra approuva fortement.

Très important.

Puis un autre problème.

Une Fourmi découvre une amélioration possible.

Par exemple :

un cache.

Un index.

Une optimisation.

Work candidate?

Oui,

mais type :

**IMPROVEMENT**

Pas maintenance required.

Le système ne doit pas interrompre les tâches importantes pour chaque optimisation.

Gabriel écrit :

**UNE IDÉE D’AMÉLIORATION N’EST PAS UNE PANNE.**

Astra approuva.

Très important.

Donc catégories :

REPAIR.

VALIDATION.

COORDINATION.

IMPROVEMENT.

EXPLORATION.

COMPLIANCE.

Très propre.

Puis un cas intéressant.

Un nouveau résultat produit un artifact non indexé.

Work candidate :

index artifact.

Petit travail.

L1.

Le système peut le faire automatiquement.

Voilà un excellent exemple de derived work trivial.

Gabriel sourit.

Le Royaume pouvait commencer à faire son ménage au fur et à mesure.

Pas le grand ménage mystérieux.

Des petites obligations explicitement définies.

Il écrit :

**LE BON ENTRETIEN AUTOMATIQUE EST CELUI DONT ON PEUT EXPLIQUER L’ORIGINE EN UNE LIGNE.**

Astra approuva fortement.

Magnifique.

Puis ils testèrent un cas limite.

La machine détecte qu’une documentation pourrait être meilleure.

Peut-elle créer une tâche?

Candidate oui.

Mais priorité basse.

Et surtout,

pas besoin de générer 700 tickets de documentation.

Budget.

Toujours.

Ils écrivirent :

**LE TRAVAIL ÉMERGENT DOIT AVOIR UN COÛT DE DÉTECTION INFÉRIEUR À LA VALEUR QU’IL CRÉE.**

Astra approuva.

Encore le meta-coût.

Très important.

Puis une question :

comment éviter que le système invente des problèmes?

Chaque work candidate doit avoir :

**trigger evidence.**

Gabriel écrit :

### WORK PROVENANCE

**trigger_event**

**affected_objective**

**dependency_path**

**why_work_exists**

**what_happens_if_ignored**

Astra approuva fortement.

Très important.

Un candidat sans trigger clair :

ne pas activer.

Voilà.

Puis un exemple.

« Peut-être qu’on devrait optimiser X. »

Pas suffisant.

Pourquoi?

Metric?

Bottleneck?

Incident?

Objectif?

Sinon :

idea only.

Pas task.

Gabriel écrit :

**UNE IDÉE N’EST PAS DU TRAVAIL TANT QU’ELLE N’A PAS DE RAISON OPÉRATIONNELLE.**

Astra approuva fortement.

Très bon.

Puis le système détecta un vrai problème.

Queue Validation grossissait.

Oldest age augmentait.

Certaines tâches bloquaient Research.

Work candidate :

investigate validation bottleneck.

Pas demandé par Gabriel.

Mais clairement dérivé d’un objectif :

maintenir le flux.

Peut-il s’activer?

Selon policy.

Peut-être L1 pour diagnostic.

Pas pour changer les ressources ou policies.

Très important.

Le système lança un diagnostic local.

Résultat :

80% du blocage venait d’un même contrôle coûteux.

Nouvelle suggestion :

cache certificate where valid.

Gabriel sourit.

Voilà.

Le travail émergent avait produit une proposition d’amélioration.

Mais changement de workflow?

Humain.

Donc escalade.

Très propre.

Ils écrivirent :

**LE SYSTÈME PEUT DÉCOUVRIR UN PROBLÈME ET PRÉPARER UNE SOLUTION SANS S’AUTORISER À MODIFIER SON ARCHITECTURE.**

Astra approuva fortement.

Très important.

Encore le seuil entre aider et décider.

Puis un autre cas.

Un test échoue.

Work candidate :

rerun.

Mais est-ce toujours bon?

Non.

Chapitre 189.

Need reason.

Donc le moteur ne doit pas générer automatiquement « rerun » sur tout fail.

Il doit classifier.

Gabriel écrit :

**ÉCHEC ≠ TÂCHE DE RECOMMENCER**

Astra approuva fortement.

Très important.

Peut-être :

investigate.

Maybe close.

Maybe reformulate.

Voilà.

Puis ils distinguèrent :

### EVENT → WORK RULES

Chaque type d’événement peut avoir :

allowed derived candidates.

Not mandatory.

Examples:

`DEPENDENCY_CHANGED` → compatibility check candidate.

`CLAIM_RETRACTED` → downstream impact audit candidate.

`QUEUE_STALLED` → bottleneck diagnostic candidate.

`TEST_FAILED` → failure attribution candidate.

Très propre.

Le système devenait presque un moteur de conséquences.

Mais attention à la récursion.

Toujours budgets.

Puis Gabriel regarda BrutoBac.

Une Fourmi venait de terminer une tâche.

Deux petites bulles apparaissaient derrière elle.

Pas des Fourmis.

Des work candidates.

Une required.

Une optional.

Gabriel sourit.

Visuellement,

c’était intéressant.

Mais il fallait éviter le spectacle.

Badge.

Origine.

Autorité.

Voilà.

Une bulle required pouvait être automatiquement transformée en Fourmi si L1.

Une optional attendait.

Très beau.

Il écrit :

**LE TRAVAIL ÉMERGENT DOIT ÊTRE VISIBLE AVANT D’ÊTRE EXÉCUTÉ QUAND SON AUTORITÉ N’EST PAS DÉLÉGUÉE.**

Astra approuva fortement.

Très important.

Puis ils firent un petit trial.

10 tâches primaires.

Combien de work candidates générés?

17.

Ça semblait beaucoup.

Combien required?

5.

Recommended?

6.

Optional?

6.

Combien auto-admis L1?

4.

Combien escaladés?

1.

Combien parked?

12.

Gabriel regarda.

Voilà.

Si les 17 avaient été activés,

le système aurait explosé.

Grâce à l’admission,

seulement 5 devenaient travail réel immédiat.

Il écrit :

**LA QUALITÉ D’UN MOTEUR DE TRAVAIL ÉMERGENT DÉPEND AUTANT DE CE QU’IL REFUSE D’ACTIVER QUE DE CE QU’IL DÉTECTE.**

Astra approuva fortement.

Très important.

Puis ils auditèrent les 5.

Trois nécessaires.

Un utile.

Un inutile après revue.

Donc un faux positif.

Très bien.

Le système devait apprendre.

Pourquoi inutile?

Dependency path incorrect.

Le moteur avait cru qu’un résultat dépendait d’un artifact alors que la relation était seulement illustrative.

Voilà.

Ils ajoutèrent :

**dependency edge type**

hard.

soft.

illustrative.

historical.

Très important.

Gabriel sourit.

Encore les cartes.

Les relations ont des types.

Sinon tout devient dépendance.

Il écrit :

**UNE FLÈCHE ENTRE DEUX OBJETS N’EST PAS TOUJOURS UNE DÉPENDANCE.**

Astra approuva fortement.

Excellent.

Puis ils rejouèrent.

Faux work candidate disparu.

Très bon.

Le moteur devenait plus précis.

Puis une question philosophique arriva.

— Est-ce qu’on vient de lui donner l’initiative?

Gabriel lui-même la posa.

Astra répondit :

— Une initiative bornée de maintenance et de routage, dérivée d’objectifs existants.

Gabriel sourit.

Oui.

Il voulait le dire proprement.

Il écrivit :

**INITIATIVE OPÉRATIONNELLE ≠ OBJECTIF PROPRE**

Astra approuva fortement.

Très important.

Le système pouvait remarquer :

quelque chose doit être vérifié.

Mais pas décider :

je vais inventer un nouveau grand projet parce que ça m’intéresse.

Sauf plus tard,

si Gabriel crée explicitement un budget d’exploration.

Chapitre 229 approchait.

Pas encore.

Puis un autre point.

Certains travaux dérivés pouvaient être anticipés.

Pourquoi attendre le problème?

Si chaque release exige snapshot,

le snapshot n’est plus emergent.

Il doit entrer dans le workflow normal.

Gabriel sourit.

Très important.

Il écrit :

**UN TRAVAIL ÉMERGENT QUI REVIENT SOUVENT DOIT PEUT-ÊTRE DEVENIR UNE ÉTAPE NORMALE DU PROCESSUS.**

Astra approuva fortement.

Voilà comment l’architecture évolue.

Les exceptions répétées deviennent règles.

Mais pas automatiquement.

Audit.

Fréquence.

Valeur.

Puis policy.

Très important.

Ils créèrent :

### PROMOTE TO WORKFLOW CANDIDATE

Si un derived work :

- revient souvent;
- reste utile;
- coût prévisible;
- faible variance;
- même trigger.

Alors proposer intégration au workflow.

Gabriel approuva.

Magnifique.

L’historique pouvait donc modifier l’architecture.

Mais encore humain pour policy.

Toujours.

Puis l’inverse.

Une étape normale ne sert presque jamais.

Peut-être la rétrograder en emergent/on-demand.

Très important.

Le système pouvait proposer simplification.

Voilà.

Puis ils regardèrent le cas initial.

Compatibility v2.

Le work candidate avait été détecté,

admis,

exécuté,

avait révélé une incompatibilité,

puis créé un audit downstream.

Sans aucun ordre direct de Gabriel.

Et pourtant,

chaque étape pouvait être expliquée par un objectif et une policy.

Gabriel sourit.

C’était peut-être une des avancées les plus importantes du deuxième monde.

Pas parce que la machine faisait « ce qu’elle voulait ».

Parce qu’un système complexe pouvait commencer à entretenir la cohérence entre ses propres traces

sans exiger que Gabriel remarque chaque conséquence à la main.

Il écrivit :

**UN SYSTÈME DEVIENT PLUS ROBUSTE QUAND LES CONSÉQUENCES IMPORTANTES DE SON TRAVAIL PEUVENT DEVENIR VISIBLES AVANT QU’UN HUMAIN LES DÉCOUVRE PAR ACCIDENT.**

Astra approuva fortement.

Voilà.

Puis une nouvelle tâche primaire entra.

Pendant son exécution,

elle produisit un résultat.

Le résultat créa un conflit.

Le conflit produisit un work candidate.

Le candidat fut classé REQUIRED.

L1 permit un petit contrôle.

Le contrôle résolut le conflit.

La tâche primaire continua.

Gabriel n’avait rien fait.

Il regarda le journal après.

Tout était là.

Aucune action cachée.

Aucune autorité dépassée.

Aucune nouvelle ambition.

Juste un petit morceau de travail qui avait existé parce qu’il devait exister,

même si personne ne l’avait écrit à l’avance.

Gabriel regarda Astra.

— Là, on commence à avoir un système qui se tient debout un peu plus tout seul.

Astra répondit :

— Oui. Parce que certaines conséquences peuvent maintenant être traitées dans les limites que tu as déjà définies.

Gabriel sourit.

C’était la bonne formulation.

Puis il vit quelque chose d’autre.

Une tâche venait d’être générée.

Mais elle ne concernait ni un bug,

ni un contrôle,

ni une validation.

Elle concernait le trajet lui-même.

Deux Fourmis avaient utilisé chacune une partie de leurs cartes.

Antmux venait de remarquer qu’en les combinant,

un chemin complet pouvait être assemblé sans avoir été écrit à l’avance.

Pas juste une tâche.

Un **workflow**.

Gabriel se redressa.

Voilà la prochaine porte.

Une question n’avait plus seulement trouvé sa file.

Un travail n’avait plus seulement été détecté.

Le système allait maintenant devoir composer

plusieurs morceaux d’actions

en un trajet complet.

Il écrivit :

**DÉTECTER UNE TÂCHE EST UNE CHOSE.**

Puis :

**COMPOSER LE CHEMIN QUI LA RELIE À SON OBJECTIF EN EST UNE AUTRE.**

Astra approuva fortement.

Le deuxième monde venait encore de changer de forme.

Le travail que personne n’avait assigné directement

avait été trouvé.

Maintenant,

il allait falloir apprendre

à construire le workflow

qui permettrait de le terminer.

**Fin du chapitre 202.**