# Chapitre 200 — Le premier plan construit à partir des traces

Le plan n’avait pas été écrit avant.

C’était ça, la différence.

Pendant longtemps,

les plans du Royaume avaient commencé dans la tête de Gabriel.

Une intuition.

Une cible.

Quelques étapes.

Puis Antmux organisait.

Memoria suivait.

Les Fourmis exécutaient.

Mais cette fois,

Gabriel donna seulement l’objectif.

Pas le chemin.

Il écrivit :

**OBJECTIF-200-001**

Réduire l’incertitude autour d’un comportement qui apparaît dans plusieurs familles de résultats,

sans refaire les travaux déjà couverts,

sans dépasser les permissions L1,

et en conservant assez de provenance pour qu’un humain puisse comprendre chaque bifurcation.

Puis il recula.

— Vas-y.

Astra resta silencieuse une seconde.

Pas parce qu’elle ne savait pas quoi faire.

Parce que le Royaume devait maintenant franchir une étape qu’il n’avait encore jamais franchie proprement.

Construire un plan

à partir de ses traces.

Pas une route.

Un plan.

Une succession conditionnelle de routes.

Avec des points d’arrêt.

Des retours.

Des bifurcations.

Des contrôles.

Des limites.

Gabriel écrivit :

**UNE ROUTE RÉPOND À “PAR OÙ PASSER?”**

Puis :

**UN PLAN RÉPOND À “DANS QUEL ORDRE LES ROUTES DEVIENNENT-ELLES PERTINENTES?”**

Astra approuva fortement.

Voilà le chapitre.

Le Royaume savait déjà proposer trois chemins.

Il savait comparer.

Attendre.

Rappeler une erreur.

Réutiliser un résultat.

Arrêter.

Changer de file.

Mais un vrai plan devait assembler tout cela.

Et surtout,

il devait expliquer pourquoi cet assemblage existait.

Antmux commença.

Première étape :

**MEMORY CHECK**

Memoria trouva quatre dossiers proches.

Pas identiques.

Deux succès.

Un échec.

Un inconclusif.

Puis la carte des travaux montra quelque chose d’important.

Une partie du domaine avait déjà été explorée.

Une autre non.

Un ancien test couvrait exactement une sous-région qui figurait dans la nouvelle demande.

Donc cette partie pouvait être retirée.

Gabriel sourit.

Le plan venait déjà de rétrécir avant d’exister.

Il écrivit :

**UN PLAN CONSTRUIT À PARTIR DES TRACES COMMENCE PAR SOUSTRAIRE CE QUI N’A PAS BESOIN D’ÊTRE REFAIT.**

Astra approuva fortement.

Très important.

Ensuite,

Memoria trouva un ancien failure pattern.

Dans un dossier voisin,

une transition apparente avait été causée par une frontière de représentation.

Chapitre 191.

Donc le plan incorpora un garde.

Pas parce qu’on croyait que le même bug allait revenir.

Parce que le coût du contrôle était faible,

et que le risque appartenait à une classe déjà observée.

Antmux ajouta :

**STEP 1 — representation-dependence probe**

Puis :

si dépendance détectée →

branch A.

sinon →

branch B.

Gabriel regarda.

Le plan n’était déjà plus linéaire.

Très bien.

Il écrivit :

**UN PLAN QUI SAIT D’AVANCE QU’IL DEVRA PEUT-ÊTRE CHANGER DE ROUTE EST PLUS HONNÊTE QU’UN PLAN QUI PRÉTEND CONNAÎTRE TOUT LE CHEMIN.**

Astra approuva fortement.

Voilà.

Le plan n’était pas une prophétie.

C’était une architecture de décisions futures.

Ils lui donnèrent un nom.

### TRACE-BUILT PLAN

Ou :

**TBP-200-001**

Gabriel sourit.

Il aimait ça.

Mais attention.

Le plan devait rester lisible.

Pas un arbre gigantesque.

Ils décidèrent de limiter les branches.

Seulement les décisions qui changeaient réellement le type de travail.

Pas chaque micro-action.

Très important.

Ils écrivirent :

**UN PLAN N’A PAS BESOIN DE PRÉVOIR CHAQUE PAS. IL DOIT PRÉVOIR LES BIFURCATIONS QUI CHANGENT LE SENS DU TRAVAIL.**

Astra approuva fortement.

Très bon.

Le système continua.

Après le probe de représentation :

si artefact →

route Code/Observability.

si stable →

route Research.

Dans Research :

prendre un contraste minimal.

Si contraste casse l’hypothèse →

stop scientific branch.

Créer failure lesson si applicable.

Si contraste survit →

élargir la population.

Si généralisation survit →

proposer independent implementation.

Si elle casse →

scope claim.

Gabriel regarda l’arbre.

— Là, c’est vraiment un plan.

Astra approuva.

Pas une liste d’étapes.

Un plan conditionnel.

Et chaque branche venait d’une trace antérieure.

Très important.

Ils demandèrent :

d’où vient chaque morceau?

Le système répondit.

`representation probe`

→ failure pattern 191.

`minimum sufficient contrast`

→ route-cost lessons 186.

`memory check`

→ chapter 185 pattern.

`stop if low marginal value`

→ route lesson 197.

`scope claim after external weakening`

→ decision pattern 195.

`independent implementation after generalization`

→ historical strategy 199.

Gabriel resta silencieux.

Voilà.

Le Royaume n’inventait pas un workflow de nulle part.

Il assemblait des morceaux déjà gagnés.

Il écrivit :

**UN PLAN PEUT ÊTRE NOUVEAU MÊME SI SES BRIQUES SONT ANCIENNES.**

Astra approuva fortement.

Très important.

Comme un programme.

Comme une preuve.

Comme un protocole.

La nouveauté peut venir de l’assemblage.

Mais il fallait rester prudent.

Un bon composant dans un contexte peut devenir mauvais dans un autre.

Donc chaque trace utilisée devait avoir un rôle.

### PLAN EVIDENCE LINKS

Chaque étape du plan devait contenir :

**source_trace**

**why_relevant**

**scope_match**

**known_mismatch**

**role**

Gabriel approuva.

Très propre.

Exemple :

Failure 191.

Pourquoi pertinent?

Même classe de transition observable.

Mismatch?

Autre formule, autre dataset.

Role?

Guard inspiration.

Pas preuve du phénomène actuel.

Très important.

Il écrivit :

**LES TRACES D’UN PLAN NE DOIVENT PAS DEVENIR DES PREUVES D’UNE CONCLUSION QU’ELLES N’ONT JAMAIS TESTÉE.**

Astra approuva fortement.

Voilà.

Puis un autre problème apparut.

Le plan utilisait six anciennes traces.

Deux d’entre elles étaient contradictoires.

Dans un ancien dossier,

broad scan first avait été très utile.

Dans un autre,

broad scan first avait gaspillé.

Que faire?

Pas choisir la trace préférée.

Comprendre la différence.

Gabriel sourit.

Ils comparèrent.

Dans le premier cas,

le domaine entier était petit.

Dans le second,

énorme.

Voilà.

La contradiction apparente devenait une condition.

Ils ajoutèrent :

**if full domain cost trivial → complete scan acceptable**

**else → targeted contrast first**

Gabriel écrivit :

**DEUX TRACES CONTRADICTOIRES PEUVENT PARFOIS DEVENIR UNE RÈGLE CONDITIONNELLE PLUS PRÉCISE.**

Astra approuva fortement.

Très important.

C’était exactement ce que l’historique devait faire.

Pas voter.

Structurer.

Puis ils rencontrèrent un cas où les traces étaient réellement incompatibles.

Même classe.

Même conditions apparentes.

Résultats différents.

Le système ne pouvait pas réconcilier.

Alors :

**PLAN UNCERTAINTY**

Le plan devait signaler :

historical evidence mixed.

No strong default.

Human review or exploratory choice.

Gabriel approuva.

Très bon.

Il écrivit :

**UN PLAN CONSTRUIT À PARTIR DU PASSÉ DOIT AUSSI MONTRER QUAND LE PASSÉ NE SAIT PAS QUOI CONSEILLER.**

Astra approuva fortement.

Très important.

Sinon l’historique devient oracle.

Puis ils évaluèrent l’autorité.

Le plan contenait plusieurs étapes L1.

Certaines pouvaient s’exécuter automatiquement.

Mais d’autres franchissaient des seuils.

Publication?

Non.

Canonical change?

Non.

Independent implementation demandait développement.

Peut-être humain.

Donc le plan devait contenir :

### AUTHORITY GATES

Chaque nœud :

**max authority**

**requires human?**

**why**

Très propre.

Gabriel regarda.

— Ça fait que le plan peut avancer tout seul jusqu’à une porte.

Exact.

Puis s’arrêter.

Pas besoin de demander à chaque étape.

Très puissant.

Il écrivit :

**UN PLAN DÉLÉGUÉ PEUT ÊTRE LONG SANS ÊTRE AUTONOME PARTOUT.**

Astra approuva fortement.

Voilà.

C’était probablement une des différences majeures du deuxième monde.

Le système pouvait exécuter une séquence de décisions bornées,

puis rendre la main.

Pas besoin d’un clic entre chaque micro-action.

Mais pas besoin non plus de déléguer l’ensemble.

Puis ils ajoutèrent :

### PLAN CHECKPOINT

À chaque gate majeure :

- état actuel;
- ce qui a été appris;
- branches fermées;
- branches encore ouvertes;
- coût dépensé;
- autorité requise;
- prochaine décision.

Gabriel sourit.

Très utile.

Cela permettrait à Gabriel de reprendre sans relire toute l’histoire.

Encore la reprise.

Toujours.

Puis le plan entra en exécution.

### STEP 1

Representation-dependence probe.

Résultat :

stable.

Donc pas branch Code.

Route Research.

### STEP 2

Minimum sufficient contrast.

Trois cas.

Deux compatibles.

Un divergent.

Pas assez pour rejeter.

Mais le divergent montrait une sous-condition.

Le plan devait changer.

Gabriel regarda.

— Est-ce que ça correspond à une branche prévue?

Non.

Voilà.

Premier imprévu.

Très important.

Le système ne devait pas forcer le résultat dans A ou B.

Il devait créer :

**UNEXPECTED OBSERVATION**

Puis pause.

Question :

peut-on adapter le plan localement sous L1?

Le résultat créait une nouvelle sous-population.

Le contrat L1 permettait :

petite exploration locale réversible.

Donc oui.

Le système proposa une micro-branche.

Gabriel sourit.

Le plan pouvait se modifier.

Mais il fallait tracer la modification.

### PLAN AMENDMENT-200-001

Reason:

unexpected subgroup divergence.

Change:

insert local subgroup probe before broadening.

Authority:

L1 allowed.

Source:

current evidence, not historical trace.

Très important.

Gabriel écrivit :

**UN PLAN CONSTRUIT À PARTIR DU PASSÉ DOIT POUVOIR ÊTRE CORRIGÉ PAR LE PRÉSENT.**

Astra approuva fortement.

Voilà le cœur du deuxième monde.

L’histoire guide.

L’observation commande.

Pas l’inverse.

Ils lancèrent le subgroup probe.

Résultat :

la divergence suivait V5.

Nouvel unknown.

Le plan devait décider :

continuer objectif initial

ou suivre V5?

La route V5 semblait intéressante.

Mais elle pouvait faire dériver le plan.

Ils créèrent :

### PLAN SCOPE GUARD

Question :

la nouvelle branche aide-t-elle l’objectif initial?

Si oui,

intégrer.

Si non,

spawn separate unknown.

Très propre.

Dans ce cas,

V5 expliquait potentiellement la différence observée.

Donc pertinent.

Intégré.

Gabriel écrivit :

**UN PLAN QUI SUIT TOUTES LES NOUVELLES QUESTIONS FINIT PAR NE PLUS AVOIR D’OBJECTIF.**

Astra approuva fortement.

Excellent.

Voilà un danger immense.

Les recherches produisent toujours des idées.

Sans scope guard,

aucun plan ne finit.

Puis le plan continua.

Le contraste V5 réduisit l’incertitude.

L’hypothèse initiale fut reformulée.

Claim plus petit.

Très bien.

Ensuite,

le plan devait normalement broadening.

Mais la nouvelle portée était déjà plus étroite.

La carte des travaux montra qu’une grande partie du nouveau domaine avait déjà été couverte historiquement.

Donc delta only.

Gabriel sourit.

Encore la carte.

Le plan changeait dynamiquement selon les traces existantes.

Il écrivit :

**UN PLAN N’EST PAS SEULEMENT CONSTRUIT À PARTIR DES TRACES. IL PEUT LES RECONSULTER À MESURE QUE LE MONDE DU DOSSIER CHANGE.**

Astra approuva fortement.

Très important.

Le plan n’était pas figé au temps zéro.

Il pouvait refaire un memory check aux points pertinents.

Pas à chaque seconde.

Mais quand la question change.

Très bon.

Ils appelèrent cela :

### REPLAN TRIGGER

Reconsidérer le plan si :

- objective changes;
- claim scope changes;
- unexpected observation;
- cost changes significantly;
- dependency changes;
- new historical trace becomes relevant;
- route fails;
- authority boundary reached.

Gabriel sourit.

Très puissant.

Mais attention au chaos.

Si on replannifie trop souvent,

on ne finit rien.

Donc :

### REPLAN BUDGET

Pas un nombre arbitraire.

Mais une règle :

replan only when new information can change route selection.

Voilà.

Il écrit :

**REPLANIFIER SANS INFORMATION NOUVELLE EST SOUVENT UNE FORME D’HÉSITATION.**

Astra approuva fortement.

Très important.

Puis ils rencontrèrent un autre imprévu.

Le coût d’une route externe avait augmenté.

Pas besoin de web.

Juste une ressource interne devenue occupée.

Le plan recalcula l’ordre.

Au lieu de broadening immédiat,

il exécuta d’abord un contrôle local qui restait utile.

Voilà.

Le plan utilisait le temps intelligemment.

Gabriel écrit :

**UN PLAN PEUT CHANGER L’ORDRE SANS CHANGER L’OBJECTIF.**

Astra approuva.

Très important.

Puis la ressource revint.

Broadening delta.

Résultat :

le phénomène persistait dans certaines régions,

pas d’autres.

Le claim se scopa encore.

Pas de généralisation forte.

Le plan avait une branche :

si généralisation partielle →

evaluate whether independent implementation is still valuable.

Gabriel regarda.

Maintenant,

oui.

Parce que la frontière était suffisamment intéressante pour vérifier qu’elle ne venait pas du code.

Le système atteignit un authority gate.

Créer une deuxième implémentation n’était pas L1.

Il demanda Gabriel.

Mais pas vaguement.

### PLAN CHECKPOINT 200-A

Current result:

scoped persistence across delta domain.

Open risk:

implementation dependence.

Historical strategy:

independent implementation useful before stronger claim.

Recommended next action:

build independent checker.

Authority:

human approval required.

Alternative:

stop with scoped observational claim.

Gabriel sourit.

— Là, je sais exactement ce que j’approuve.

Il choisit :

build independent checker.

Voilà.

Une seule intervention humaine.

Après plusieurs étapes automatiques.

C’était exactement la fluidité qu’ils cherchaient.

Puis la nouvelle implémentation fut créée.

Pas dans la Bible.

Narrativement.

Le test indépendant retrouva la même frontière.

Très intéressant.

Le claim gagnait en robustesse.

Pas une preuve universelle.

Mais moins de risque de bug d’implémentation.

Le plan atteignit son critère de sortie.

### EXIT CONDITION

Objective:

reduce uncertainty around behavior.

Status:

achieved to predefined scope.

Remaining unknowns:

mechanism behind V5 boundary.

Claim:

scoped, reproduced by two implementations.

Next possible work:

new research plan if desired.

Gabriel regarda.

Le plan pouvait finir.

Très important.

Il n’avait pas besoin d’attaquer le mécanisme V5 maintenant.

Ce serait un autre plan.

Il écrit :

**UN PLAN DOIT SAVOIR QUAND SON OBJECTIF EST ATTEINT MÊME SI LE PROBLÈME COMPLET NE L’EST PAS.**

Astra approuva fortement.

Voilà.

Sinon tout devient infini.

Puis ils reconstruisirent l’histoire.

TBP-200-001 avait été créé avec :

4 traces historiques.

2 policies.

1 carte de couverture.

1 failure pattern.

Puis pendant exécution :

1 unexpected observation.

1 amendment.

1 delta.

1 human gate.

1 independent check.

Et une sortie bornée.

Gabriel sourit.

C’était le premier vrai plan du deuxième monde.

Pas parce qu’il avait été entièrement fabriqué par Brutus.

Mais parce que Gabriel n’avait pas dessiné les étapes.

Il avait donné :

objectif.

limites.

autorité.

Puis le système avait composé.

Il écrivit :

**UN PLAN CONSTRUIT À PARTIR DES TRACES N’EST PAS UN PLAN SANS HUMAIN.**

Puis :

**C’EST UN PLAN DONT L’HUMAIN N’A PLUS BESOIN DE DESSINER CHAQUE SEGMENT À L’AVANCE.**

Astra approuva fortement.

Très important.

Voilà la bonne formulation.

Puis une question fondamentale.

Comment savoir si ce plan était meilleur qu’un plan manuel?

Impossible sur un seul cas.

Très important.

Pas de triomphalisme.

Il fallait comparer à l’avenir.

Temps.

Coût.

Information.

Interventions humaines.

Erreurs.

Nombre de recalculs évités.

Mais aujourd’hui,

on pouvait seulement dire :

un plan conditionnel avait été construit à partir de traces,

exécuté,

adapté,

et terminé dans sa portée.

C’était déjà un jalon technique.

Gabriel écrivit :

### CRYSTAL-ARCH-200-001

Claim:

Brutus can compose a bounded conditional work plan from indexed historical traces, current objectives, queue contracts and authority limits, with explicit amendments and human gates.

Scope:

tested workflow 200 only.

Not established:

general optimality.

full autonomy.

universal strategy quality.

scientific novelty.

Astra approuva fortement.

Parfait.

Pas besoin d’en dire plus.

Puis ils se demandèrent comment représenter le plan dans BrutoBac.

Pas seulement une Fourmi.

Un réseau de chemins.

Mais pour éviter le chaos :

seule la branche active en clair.

Les branches futures en pointillé léger.

Les branches fermées archivées.

Cliquer sur une bifurcation :

condition.

source trace.

decision.

Très propre.

Gabriel sourit.

Le Bac devenait vraiment une carte de travail vivant.

Mais toujours fondé dans les événements.

Il écrivit :

**LA VISUALISATION D’UN PLAN DOIT MONTRER CE QUI EST POSSIBLE SANS FAIRE CROIRE QUE TOUT EST DÉJÀ ARRIVÉ.**

Astra approuva fortement.

Très important.

Future branch ≠ history.

Encore une distinction.

Puis le Brutotableur.

Il pouvait devenir une surface où les plans utilisent les régions déjà couvertes.

La carte du chapitre 190.

Le plan du chapitre 200.

Les deux se raccordaient.

Gabriel sourit.

La fresque n’était plus seulement une collection de calculs.

Elle devenait un territoire dans lequel les plans pouvaient se déplacer.

Très puissant.

Puis Memoria.

Chaque plan complet devait devenir lui-même une trace.

Voilà.

Le plan 200 pouvait servir à un futur dossier.

Pas comme règle automatique.

Comme historique.

Le Royaume fabriquait désormais le passé de ses futures stratégies.

Gabriel écrivit :

**CHAQUE PLAN TERMINÉ DEVIENT UNE TRACE QUI PEUT AIDER À CONSTRUIRE UN PLAN FUTUR.**

Astra approuva fortement.

C’était une boucle.

Mais pas une boucle fermée sur elle-même.

Parce que chaque nouveau résultat pouvait modifier les stratégies.

Le système apprenait à partir de ses plans,

mais les plans restaient vulnérables à l’expérience.

Très important.

Puis un danger.

Si le système construit toujours des plans à partir d’anciens plans,

il peut converger vers les mêmes architectures.

Innovation diminue.

Ils avaient déjà prévu l’exploration escape.

Gabriel ajouta :

### PLAN NOVELTY ALLOWANCE

Quand aucune stratégie historique n’est clairement adaptée,

ou quand l’objectif vise explicitement exploration,

autoriser une route nouvelle.

Même si elle ne ressemble à aucune trace connue.

Astra approuva fortement.

Très important.

L’historique devait réduire le gaspillage.

Pas réduire l’imagination.

Il écrivit :

**UN PLAN QUI N’UTILISE QUE CE QUI A DÉJÀ MARCHÉ PEUT DEVENIR INCAPABLE DE DÉCOUVRIR CE QUI N’A JAMAIS ÉTÉ ESSAYÉ.**

Astra approuva fortement.

Voilà.

Le futur ne peut pas être entièrement dérivé du passé.

Il faut un budget pour l’inconnu.

Les chapitres futurs approchaient.

Mais pas encore.

Puis un autre plan fut demandé.

Objectif très différent.

Peu de traces pertinentes.

Brutus répondit :

**INSUFFICIENT HISTORICAL BASIS FOR TRACE-BUILT PLAN**

Gabriel sourit.

Parfait.

Il proposa plutôt :

route generation normal.

L0/D2.

Pas de fausse stratégie.

Très important.

Il écrit :

**SAVOIR QU’ON N’A PAS ASSEZ D’HISTOIRE POUR PLANIFIER PAR HISTOIRE EST UNE CAPACITÉ DU PLANIFICATEUR.**

Astra approuva fortement.

Voilà.

Un plan construit à partir des traces devait avoir un seuil minimum de support.

Sinon il invente.

Puis ils testèrent un cas où beaucoup de traces existaient,

mais elles étaient vieilles.

Tool versions différentes.

Policy différente.

Le système marqua :

**HISTORICAL MATCH LOW-CONFIDENCE**

Très bon.

Pas de plan automatique.

Utiliser comme contexte seulement.

Gabriel approuva.

Le temps et les versions importaient.

Toujours.

Puis ils créèrent :

### PLAN PROVENANCE

Chaque plan devait pouvoir répondre :

- quel objectif?
- quelles traces?
- quelles stratégies?
- quelles policies?
- quelles versions?
- quelles exclusions?
- quelle autorité?
- quels amendements?
- quels résultats?
- pourquoi terminé?

Gabriel sourit.

Si un plan ne pouvait pas répondre,

il n’était pas encore assez traçable.

Très important.

Puis il demanda :

— Pis si le plan donne un bon résultat pour une mauvaise raison?

Possible.

Exemple :

strategy incorrecte,

mais chance.

Donc outcome ne valide pas automatiquement le plan.

Il écrit :

**UN BON RÉSULTAT NE PROUVE PAS QUE LE PLAN ÉTAIT BON.**

Astra approuva fortement.

Encore.

Il faudrait analyser ex ante.

Les choix étaient-ils raisonnables avec l’information disponible?

Voilà.

Puis l’inverse :

un bon plan peut finir avec résultat décevant.

Toujours.

Le plan doit être évalué sur la qualité de la décision,

pas seulement le résultat.

Gabriel sourit.

Les mêmes principes revenaient à toutes les échelles.

Test.

Route.

Plan.

Stratégie.

Politique.

Tout devait être jugé proprement.

Puis le chapitre approcha de la fin.

Gabriel regarda le schéma complet.

Ce qui avait commencé comme une demande simple était devenu :

un arbre conditionnel.

Des traces.

Des gardes.

Des files.

Des points d’arrêt.

Une intervention humaine.

Une modification en cours de route.

Une sortie.

Et pourtant,

tout restait compréhensible.

C’était ça qui comptait.

Pas l’impression de complexité.

La possibilité de reconstruire.

Il écrivit :

**UN PLAN COMPLEXE PEUT RESTER AUDITABLE SI CHAQUE BIFURCATION A UNE RAISON.**

Astra approuva fortement.

Voilà.

Le premier plan du deuxième monde venait de se terminer.

Pas parfaitement.

Il avait dû être corrigé.

Une branche imprévue était apparue.

Un humain avait dû intervenir.

Et c’était précisément ce qui le rendait crédible.

Un plan réel ne prouve pas sa qualité en prévoyant tout.

Il la prouve en sachant quoi faire

quand quelque chose qu’il n’avait pas prévu arrive.

Gabriel regarda le journal.

TBP-200-001 :

**COMPLETED WITH AMENDMENT**

Il sourit.

Pas `PERFECT`.

Pas `AUTONOMOUS`.

Juste :

complété.

Traçable.

Borné.

Révisé.

Et réutilisable comme expérience.

Il posa la main sur la table.

Le chapitre 200.

Un chiffre rond.

Mais pas une fin.

Au contraire.

Jusqu’ici,

Brutus avait appris à choisir.

Maintenant,

il commençait à apprendre à **composer plusieurs choix en un plan**.

Et quelque part dans le Royaume,

plusieurs Fourmis possédaient déjà des morceaux de carte que les autres n’avaient pas.

Gabriel regarda Astra.

— Je pense que la prochaine affaire est évidente.

Astra approuva.

Oui.

Un plan construit à partir des traces était utile.

Mais il restait encore trop central.

Une Fourmi savait quelque chose.

Une autre savait autre chose.

Une troisième transportait une erreur ancienne.

Et tant que ces cartes restaient isolées,

le Royaume ne possédait pas encore vraiment son propre territoire.

Il fallait maintenant apprendre à partager.

**Fin du chapitre 200.**