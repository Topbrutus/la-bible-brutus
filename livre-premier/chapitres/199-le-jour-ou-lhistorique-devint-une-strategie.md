# Chapitre 199 — Le jour où l’historique devint une stratégie

Au début,

l’historique servait à se souvenir.

C’était déjà beaucoup.

Savoir ce qui avait été fait.

Retrouver un résultat.

Éviter de recalculer.

Voir où une expérience avait cassé.

Comprendre pourquoi une route avait été abandonnée.

Mais ce matin-là,

quelque chose changea.

Brutus ne regarda plus seulement l’historique pour comprendre le passé.

Il commença à l’utiliser pour choisir le futur.

Gabriel regardait une nouvelle tâche.

Pas exceptionnelle.

Pas critique.

Mais suffisamment proche de plusieurs expériences anciennes pour que Memoria s’allume presque immédiatement.

Trois routes apparaissaient.

### ROUTE A

Petit test ciblé.

### ROUTE B

Extension de domaine.

### ROUTE C

Implémentation indépendante.

Gabriel sourit.

— Ça, on connaît.

Astra répondit :

— Justement.

Le système ouvrit l’historique.

Pas un seul cas.

Une série.

Des dizaines de décisions semblables.

Pas identiques.

Mais structurées de la même façon.

Même type d’unknown.

Même classe de coût.

Même genre de claim.

Même besoin de discrimination.

Gabriel se pencha.

Pour la première fois,

le passé n’apparaissait pas comme une liste d’exemples.

Il apparaissait comme un **profil de décision**.

Il écrivit :

**QUAND L’HISTORIQUE DEVIENT ASSEZ STRUCTURÉ, IL PEUT CESSER D’ÊTRE UNE ARCHIVE ET DEVENIR UNE STRATÉGIE.**

Astra approuva fortement.

Voilà.

Mais attention.

Pas une stratégie automatique par magie.

Pas :

« ça a marché avant, donc faisons pareil. »

Il fallait démonter le mécanisme.

Pourquoi une route avait été utile?

Dans quel contexte?

Avec quel coût?

À quel moment?

Et surtout :

quand avait-elle cessé d’être utile?

Gabriel écrivit :

**UNE STRATÉGIE HISTORIQUE N’EST PAS UNE COPIE DU PASSÉ. C’EST UNE RÈGLE CONDITIONNELLE TIRÉE DE PLUSIEURS TRACES.**

Astra approuva fortement.

Très important.

Ils commencèrent à construire quelque chose.

### HISTORICAL STRATEGY CANDIDATE

Classe de problème :

unknown expérimental local avec deux hypothèses principales.

Historique observé :

- petits contrastes souvent informatifs en premier;
- gros scans souvent redondants tant que les hypothèses ne sont pas mieux séparées;
- implémentation indépendante utile plus tard, après survie initiale.

Suggestion :

**targeted contrast → if survives → broader generalization → if still relevant → independent implementation**

Gabriel regarda.

— Là, c’est quasiment un workflow.

Exact.

Mais ce workflow venait du passé réel du Royaume.

Pas seulement d’une règle écrite d’avance.

Ils l’appelèrent :

**STRAT-199-001**

Gabriel sourit.

Pas encore active.

Candidate.

Toujours.

Il écrivit :

**UNE STRATÉGIE DOIT ÊTRE TESTÉE COMME UNE HYPOTHÈSE SUR LE TRAVAIL.**

Astra approuva fortement.

Très important.

Parce qu’un workflow qui semble bon rétrospectivement peut être biaisé.

Peut-être on se souvient seulement des succès.

Peut-être les échecs n’étaient pas indexés.

Peut-être certains cas étaient différents.

Donc il fallait comparer.

Ils prirent l’historique complet disponible pour cette classe.

Pas seulement les beaux cas.

Succès.

Échecs.

Inconclusifs.

Routes interrompues.

Routes coûteuses.

Décisions humaines.

Puis ils demandèrent :

dans combien de cas le targeted contrast avait-il réellement changé la suite?

Dans combien avait-il été inutile?

Quand le broad scan avait-il été meilleur d’emblée?

Quand l’implémentation indépendante avait-elle dû venir plus tôt?

Pas de score magique.

Mais des patterns.

Gabriel regarda.

Une structure apparut.

Quand l’hypothèse était encore vague,

les gros scans apprenaient peu.

Quand deux prédictions discriminantes existaient déjà,

les petits contrastes étaient efficaces.

Quand le risque principal était logiciel,

l’implémentation indépendante devait monter plus tôt.

Voilà.

La stratégie candidate devait donc intégrer une branche.

Pas une séquence fixe.

Ils réécrivirent.

### STRAT-199-001 v0.2

If:

hypotheses not discriminated yet

→ design targeted contrast.

If:

software implementation risk high

→ independent check may precede expansion.

If:

targeted contrast survives

→ broaden domain.

If:

generalization survives and claim strength justifies it

→ independent implementation or stronger validation.

Gabriel sourit.

— Là, oui.

Astra approuva.

Une stratégie historique n’était donc pas :

A → B → C.

C’était :

**si ceci, alors ça.**

Très important.

Il écrivit :

**LE PASSÉ DEVIENT STRATÉGIE QUAND IL PRODUIT DES CONDITIONS, PAS SEULEMENT DES HABITUDES.**

Astra approuva fortement.

Voilà.

Puis une question.

Est-ce que la stratégie devait s’exécuter automatiquement?

Pas tout de suite.

D2.

Recommandation.

Pas D4.

Gabriel écrivit :

**UNE STRATÉGIE NOUVELLEMENT EXTRAITE DE L’HISTORIQUE COMMENCE COMME CONSEIL, PAS COMME AUTORITÉ.**

Astra approuva fortement.

Très important.

Il fallait observer.

Comparer.

Calibrer.

Puis peut-être déléguer certaines branches L1 plus tard.

Exact.

Ils lancèrent le premier test prospectif.

Nouvel unknown.

Le système historique recommandait :

targeted contrast.

Gabriel aurait choisi la même chose.

Ils exécutèrent.

Le contraste cassa l’hypothèse principale en trois tests.

Très bon.

La stratégie semblait utile.

Mais un cas ne suffit pas.

Deuxième.

Recommandation identique.

Cette fois,

le contraste était inconclusif.

La stratégie proposa :

reformulate question.

Gabriel approuva.

Troisième.

Risque d’implémentation élevé.

La stratégie choisit independent implementation en premier.

Les deux codes divergeaient.

Excellent.

Pas besoin de broad scan avant de corriger.

Gabriel sourit.

La stratégie commençait à montrer une vraie valeur.

Mais encore :

petit panel.

Ils marquèrent :

**PROSPECTIVE TRIAL — ONGOING**

Pas « validated ».

Toujours.

Puis un quatrième cas.

Le système recommanda targeted contrast.

Mais le domaine était tellement petit que broad scan coûtait pratiquement la même chose.

Gabriel regarda.

La stratégie avait sur-réfléchi.

Le gros scan aurait été plus simple.

Ils enregistrèrent :

**STRATEGY MISFIT**

Cause :

strategy ignored trivial full-domain cost.

Très important.

Ils corrigèrent.

Ajout :

If full domain is below trivial-cost threshold,

prefer complete scan or run both.

Gabriel sourit.

Voilà.

Une stratégie historique devait rester modifiable par de nouveaux cas.

Il écrivit :

**UNE STRATÉGIE ISSUE DU PASSÉ DOIT RESTER VULNÉRABLE AU PRÉSENT.**

Astra approuva fortement.

Très belle phrase.

Sinon l’historique devient dogme.

Puis ils versionnèrent :

`STRAT-199-001 v0.3`

Voilà.

Le Royaume n’apprenait pas une loi.

Il apprenait un workflow adaptatif.

Puis Gabriel réalisa quelque chose.

Ils avaient maintenant trois niveaux différents.

### TRACE

Un événement.

### LESSON

Une interprétation réutilisable de plusieurs traces.

### STRATEGY

Une politique conditionnelle qui modifie l’ordre futur des actions.

Astra approuva.

Très important.

Ils écrivirent :

**TRACE → LEÇON → STRATÉGIE**

Puis Gabriel ajouta :

**PAS AUTOMATIQUEMENT.**

Astra approuva fortement.

Exact.

Il faut validation entre chaque niveau.

Une trace peut être anecdotique.

Une leçon peut être fausse.

Une stratégie peut généraliser trop loin.

Très important.

Puis ils ajoutèrent un quatrième niveau.

### POLICY

Une stratégie suffisamment éprouvée et gouvernée pour obtenir une autorité définie.

Gabriel sourit.

Voilà.

**TRACE → LEÇON → STRATÉGIE → POLITIQUE**

Mais chaque flèche demande des preuves.

Très important.

Il écrivit :

**PLUS UNE IDÉE GAGNE D’AUTORITÉ, PLUS ELLE DOIT AVOIR SURVÉCU À DES CONTRE-EXEMPLES.**

Astra approuva fortement.

Voilà.

Puis ils étudièrent comment une stratégie pouvait être mauvaise sans être fausse.

Exemple :

elle minimise le coût.

Mais Gabriel veut maximiser robustesse.

La stratégie reste valide pour un objectif,

pas pour l’autre.

Donc chaque stratégie doit porter :

**objective profile**

Très important.

Ils ajoutèrent :

### STRATEGY CONTRACT

**problem_class**

**objective**

**preconditions**

**action tree**

**stop conditions**

**escalation conditions**

**known failure modes**

**evidence base**

**version**

**authority level**

Gabriel regarda.

— Là, on peut vraiment les traiter comme des objets.

Exact.

Une stratégie n’était plus une intuition cachée dans un prompt.

Elle devenait un artefact.

Versionné.

Testable.

Comparable.

Rétractable.

Très important.

Puis un autre problème.

Deux stratégies historiques.

### STRAT-A

Minimise coût.

### STRAT-B

Maximise indépendance de preuve.

Les deux bonnes.

Chapitre 195.

Encore.

Le système ne devait pas fusionner.

Il devait demander l’objectif.

Gabriel sourit.

Tout revenait.

Il écrivit :

**L’HISTORIQUE PEUT PRODUIRE PLUSIEURS STRATÉGIES LÉGITIMES POUR LA MÊME CLASSE DE PROBLÈMES.**

Astra approuva fortement.

Voilà.

Le passé n’avait pas une voix unique.

Très important.

Puis un cas encore plus intéressant.

Une stratégie qui avait bien marché historiquement

commence à moins bien marcher après une mise à jour du Brotoculateur.

Pourquoi?

Le coût des petits tests avait changé.

Les outils avaient évolué.

Gabriel sourit.

Donc :

la stratégie dépend aussi de l’infrastructure.

Ils ajoutèrent :

**environment dependencies**

**tool version dependencies**

Très important.

Une bonne stratégie de 2026 peut devenir mauvaise en 2027 si les coûts changent.

Il écrit :

**UNE STRATÉGIE EST UNE RÉPONSE À UN MONDE. SI LE MONDE CHANGE, IL FAUT LA RETESTER.**

Astra approuva fortement.

Excellent.

Puis un cas mathématique.

Une stratégie de recherche factorielle historique.

Elle choisit certaines bornes et méthodes selon q.

Peut-elle devenir policy?

Seulement avec prudence.

Parce qu’un échec passé d’une méthode ne prouve pas qu’elle est inutile ailleurs.

Il faut contextes.

Toujours.

Gabriel écrit :

**UNE STRATÉGIE DE RECHERCHE NE DOIT PAS TRANSFORMER LES ZONES NON EXPLORÉES EN ZONES INTERDITES.**

Astra approuva fortement.

Très important.

Le budget de curiosité futur devait laisser de la place aux nouvelles routes.

Puis ils créèrent :

### EXPLORATION ESCAPE

Même si une stratégie historique est active,

un pourcentage ou budget de travail peut être réservé à :

routes nouvelles.

méthodes alternatives.

tests adversariaux.

Pas nécessairement un pourcentage fixe.

Concept seulement.

Gabriel sourit.

Voilà.

Sinon le système optimize vers son passé.

Il écrit :

**UNE STRATÉGIE QUI GAGNE TOUJOURS PARCE QU’ELLE EMPÊCHE LES AUTRES D’ÊTRE TESTÉES N’EST PAS VALIDÉE.**

Astra approuva fortement.

Très important.

Il faut permettre la compétition.

Puis un autre concept apparut.

Les stratégies pouvaient être comparées prospectivement.

Pas seulement rétrospectivement.

### STRATEGY TOURNAMENT

Même classe de problèmes.

A recommande route X.

B recommande route Y.

Comparer :

coût.

information.

temps.

erreurs.

Mais sans exécuter deux fois les actions coûteuses chaque fois.

On peut commencer sur sandbox.

Sur historiques replayables.

Puis cas nouveaux.

Gabriel sourit.

Les chapitres 233–235 apparaissaient déjà à l’horizon.

Mais pas encore.

Ici,

il s’agissait simplement du moment où l’historique devint assez structuré pour proposer des stratégies.

Puis ils firent un replay historique.

Ils prirent dix anciens dossiers.

Masquèrent leurs décisions.

Appliquèrent STRAT-199-001 v0.3.

Résultat :

sur plusieurs cas,

elle reproduisait ou améliorait le premier choix.

Sur d’autres,

elle divergeait.

Important.

Pourquoi divergeait-elle?

Parfois l’ancien choix était humain et meilleur.

Parfois la nouvelle stratégie semblait meilleure.

Mais attention.

On connaît le futur dans un replay.

Risque de hindsight bias.

Gabriel écrivit :

**REPLAY HISTORIQUE ≠ TEST PROSPECTIF**

Astra approuva fortement.

Très important.

Le replay sert à éliminer les stratégies absurdes.

Pas à prouver performance future.

Excellent.

Puis ils créèrent deux phases.

### STRATEGY EVALUATION

**PHASE 1 — REPLAY**

Tester cohérence sur passé.

**PHASE 2 — PROSPECTIVE**

Évaluer sur nouveaux cas.

Gabriel approuva.

Très bon.

Puis une troisième.

**PHASE 3 — LIMITED AUTHORITY**

Seulement après résultats suffisants,

certaines branches peuvent passer en L1.

Voilà.

Pas de saut.

Très propre.

Puis Gabriel demanda :

— Qu’est-ce que ça change vraiment dans Antmux?

Beaucoup.

Avant,

le routeur choisissait selon règles locales.

Maintenant,

il pouvait consulter une bibliothèque de stratégies.

Pas seulement :

quelle queue?

Mais :

quel enchaînement de travail a historiquement produit de bonnes décisions dans ce type de problème?

Voilà.

Ils imaginèrent :

### STRATEGY REGISTRY

- research-small-contrast-first
- validation-independent-check-first
- low-cost-regression-ladder
- memory-first-for-known-pattern
- public-output-high-guard
- exploratory-novel-route

Gabriel sourit.

Mais pas cent stratégies dès demain.

Commencer petit.

Une.

Tester.

Puis deux.

Toujours la règle.

**1 module → 1 connexion → 1 mesure → 1 preuve**

Il l’écrivit encore.

Astra approuva.

Très important.

Le deuxième monde n’avait pas besoin de devenir complexe immédiatement.

Une stratégie propre vaut mieux que cinquante heuristiques cachées.

Puis un problème de conflit.

Deux stratégies s’appliquent au même dossier.

Quelle priorité?

Pas hardcoder silencieusement.

Il faut un meta-router.

Gabriel rit.

— Là, on va pas construire une machine pour choisir la machine pour choisir le chemin tout de suite.

Astra approuva.

Très raisonnable.

Ils gardèrent simple :

if multiple strategies match,

show candidates.

Human or explicit policy chooses.

Pas de récursion infinie.

Gabriel écrivit :

**UN SYSTÈME PEUT DEVENIR ABSURDE S’IL CRÉE UNE NOUVELLE COUCHE DE DÉCISION POUR CHAQUE CONFLIT DE DÉCISION.**

Astra approuva fortement.

Excellent.

Parfois,

demander reste moins cher.

Toujours le meta-coût.

Puis une stratégie particulièrement utile apparut.

Elle venait des chapitres 185 à 198 eux-mêmes.

Avant un test non trivial :

1. consulter Memoria;
2. vérifier travaux déjà faits;
3. vérifier failure patterns;
4. définir question;
5. comparer routes;
6. lancer minimum sufficient test;
7. review;
8. stop/switch/escalate selon résultat.

Gabriel regarda.

— C’est presque notre méthode du deuxième monde.

Astra approuva.

Oui.

Ils l’appelèrent provisoirement :

### SECOND-WORLD BASIC STRATEGY

Mais pas canonique encore.

Gabriel sourit.

Très important.

Même la Bible pouvait suggérer une stratégie,

mais le logiciel devait la tester.

Narration ≠ preuve.

Toujours.

Ils écrivirent :

**UNE BONNE HISTOIRE PEUT INSPIRER UNE ARCHITECTURE. ELLE NE VALIDE PAS CETTE ARCHITECTURE.**

Astra approuva fortement.

Voilà.

Puis ils appliquèrent la stratégie à un nouvel unknown.

Memoria trouva un duplicate partiel.

La carte montra 60% du domaine déjà couvert.

Failure pattern signala une dépendance de version.

Question audit précisa le claim.

Minimum sufficient test fut réduit à quatre cas.

Résultat :

un contre-exemple.

Stop.

Gabriel sourit.

Toute la chaîne avait évité un gros run.

Cette fois,

l’historique n’avait pas simplement fourni une pièce.

Il avait structuré le trajet entier.

Il écrivit :

**LE PASSÉ N’ÉTAIT PLUS CONSULTÉ À UNE ÉTAPE. IL ÉTAIT DEVENU UNE PARTIE DE L’ORDRE DES ÉTAPES.**

Astra approuva fortement.

Voilà le cœur.

Un historique devient stratégie quand il commence à organiser **l’ordre du travail**.

Pas seulement ses contenus.

Très important.

Puis une autre tâche.

La stratégie recommandait memory-first.

Mais lookup historique était plus cher que le calcul trivial.

Fast path.

Le système sauta Memoria.

Très bien.

Donc la stratégie elle-même devait contenir des exceptions de coût.

Gabriel sourit.

Pas de dogme.

Toujours.

Il écrit :

**UNE STRATÉGIE QUI NE SAIT PAS QUAND NE PAS S’APPLIQUER N’EST PAS ENCORE MATURE.**

Astra approuva fortement.

Très important.

Puis ils pensèrent aux humains.

Gabriel avait lui aussi une stratégie historique.

Il reconnaissait des patterns.

« Ça, je l’ai déjà vu. »

« Ça, ça sent le bug de représentation. »

« Ça, on devrait le casser avant d’agrandir. »

Brutus pouvait commencer à rendre certaines de ces intuitions explicites.

Pas toutes.

Pas les inventer.

Mais quand elles étaient répétées et traçables,

les formaliser.

Gabriel écrivit :

**FORMALISER UNE INTUITION NE LA REND PAS VRAIE. ÇA LA REND TESTABLE.**

Astra approuva fortement.

Magnifique.

C’était exactement l’intérêt.

Une intuition dans la tête de Gabriel ne peut pas être auditée facilement.

Une stratégie candidate peut.

Voilà.

Puis un autre danger.

Si la stratégie est construite à partir des décisions de Gabriel,

elle peut reproduire ses biais.

Très important.

Il écrit :

**APPRENDRE L’HISTORIQUE HUMAIN PEUT AUSSI APPRENDRE LES ERREURS HUMAINES.**

Astra approuva fortement.

Donc les stratégies doivent être évaluées par résultats,

pas par imitation.

Pas :

Gabriel a choisi A 80% du temps.

Donc A.

Mais :

quand A a été choisi dans ces conditions,

qu’est-ce qui est arrivé?

Très important.

Ils ajoutèrent :

**decision imitation is not strategy validation.**

Excellent.

Puis une autre nuance.

Gabriel peut avoir changé de méthode avec le temps.

L’historique ancien et récent peuvent diverger.

Quelle version de Gabriel apprendre?

Mauvaise question.

Il ne fallait pas apprendre « Gabriel ».

Il fallait apprendre les conséquences des stratégies.

Gabriel rit.

— Merci.

Astra approuva.

Ils écrivirent :

**LE BUT N’EST PAS DE CLONER LES HABITUDES DE L’OPÉRATEUR. LE BUT EST DE TESTER QUELLES RÈGLES DE TRAVAIL PRODUISENT LES MEILLEURS RÉSULTATS SELON L’OBJECTIF.**

Très important.

Puis le système trouva une vieille route qui avait souvent marché.

Mais depuis une nouvelle architecture,

elle n’était plus nécessaire.

Gabriel sourit.

Encore.

L’historique peut enseigner ce qu’il faut arrêter de faire.

Pas seulement ce qu’il faut répéter.

Ils écrivirent :

**UNE STRATÉGIE HISTORIQUE PEUT ÊTRE : “NE FAIS PLUS CECI PAR DÉFAUT.”**

Astra approuva fortement.

Exemple :

ne pas recalculer full domain si coverage map montre delta.

Chapitre 190.

Très concret.

Puis ils assemblèrent quelques stratégies candidates.

### STRAT-MEMORY-FIRST

Pour tâches non triviales avec historique riche.

### STRAT-DELTA-FIRST

Si coverage exacte existe.

### STRAT-GUARD-FIRST

Si failure pattern connu et blast radius élevé.

### STRAT-TARGETED-FIRST

Si hypothèses discriminables à faible coût.

### STRAT-INDEPENDENCE-FIRST

Si implementation risk domine.

Gabriel regarda.

Le Royaume commençait à avoir un véritable répertoire de manières de travailler.

Mais chacune avait :

scope.

evidence.

known limits.

Pas de règle universelle.

Très important.

Puis BrutoBac.

Avant,

on voyait une Fourmi choisir une route.

Maintenant,

on pouvait voir un petit tag :

**STRATEGY: TARGETED-FIRST v0.3**

Gabriel sourit.

Cliquer :

pourquoi cette stratégie s’applique?

quelles traces la soutiennent?

quels cas la contredisent?

quelle policy?

Magnifique.

L’activité devenait explicable.

Le public n’avait pas besoin de tout voir.

Mais Verso,

oui.

Très important.

Puis un cas où aucune stratégie ne s’applique.

Le système dit :

**NO MATCHING STRATEGY — GENERATE ROUTES NORMALLY**

Gabriel sourit.

Parfait.

Ne pas forcer.

L’historique n’avait pas réponse à tout.

Il écrit :

**L’ABSENCE DE STRATÉGIE CONNUE EST UNE INFORMATION, PAS UNE PANNE.**

Astra approuva fortement.

Voilà.

Et parfois,

c’est précisément là que le nouveau travail commence.

Puis une stratégie échoua.

Un nouveau type de problème.

Mauvais routage.

Gabriel ne la supprima pas.

Il réduisit son scope.

Avant :

all local experimental unknowns.

Après :

local experimental unknowns with defined pairwise discriminants.

Voilà.

Une stratégie peut apprendre ses frontières.

Il écrit :

**UNE STRATÉGIE DEVIENT PLUS FORTE QUAND ELLE SAIT SUR QUELS PROBLÈMES ELLE NE DOIT PAS PARLER.**

Astra approuva fortement.

Très important.

Le système devenait meilleur par restriction.

Pas toujours par expansion.

Puis Gabriel regarda le chemin parcouru depuis le début de l’arc 180.

Le deuxième monde avait commencé avec un premier trajet.

Puis :

mémoire.

routes.

attente.

décisions assistées.

coûts.

détours.

questions.

recalcul.

cartographie.

erreurs.

files.

autorité.

compromis.

raccourcis.

abandons.

échecs.

Tout cela convergeait maintenant.

Le passé pouvait être transformé en règles de travail.

Pas directement.

Mais par étapes.

Gabriel écrivit une dernière fois :

**LE JOUR OÙ L’HISTORIQUE DEVINT UNE STRATÉGIE, BRUTUS CESSA DE SE SOUVENIR SEULEMENT DE CE QU’IL AVAIT FAIT.**

Puis :

**IL COMMENÇA À SE SERVIR DE CE PASSÉ POUR CHOISIR COMMENT IL ALLAIT TRAVAILLER ENSUITE.**

Astra approuva fortement.

Mais Gabriel ajouta immédiatement :

**ET CHAQUE STRATÉGIE RESTAIT RÉVISABLE.**

Astra approuva encore plus fortement.

Parce que sans cette dernière ligne,

tout le chapitre aurait été dangereux.

Le passé devait guider.

Jamais gouverner sans limite.

Le Royaume n’avait pas besoin d’être prisonnier de ce qui avait marché.

Il avait besoin d’un passé assez précis

pour éviter de recommencer aveuglément,

assez humble

pour reconnaître quand le monde avait changé,

et assez structuré

pour transformer des milliers de traces

en quelques bonnes façons de commencer.

Gabriel regarda la prochaine tâche entrer.

Brutus consulta son historique.

Reconnaît une classe connue.

Proposa :

**STRAT-TARGETED-FIRST v0.3**

Gabriel lut la justification.

Puis il répondit simplement :

— Go.

La Fourmi partit.

Pas parce qu’elle suivait le passé.

Parce que le passé avait enfin appris

à lui montrer une route

sans prétendre qu’elle était la seule.

**Fin du chapitre 199.**