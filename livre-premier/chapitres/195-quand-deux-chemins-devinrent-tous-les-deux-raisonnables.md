# Chapitre 195 — Quand deux chemins devinrent tous les deux raisonnables

Le problème n’était plus de trouver un bon chemin.

Il y en avait deux.

Et les deux tenaient debout.

Gabriel regardait l’écran.

Pas de route dominante.

Pas d’option manifestement meilleure.

Pas de bug.

Pas d’oubli.

Pas de règle cachée.

Juste deux stratégies différentes,

défendables,

cohérentes,

et orientées vers des objectifs légèrement différents.

Il sourit.

— Là, c’est là que ça devient intéressant.

Astra approuva.

Exactement.

Pendant longtemps,

le Royaume avait surtout appris à éliminer les mauvaises routes.

Celles qui coûtaient trop cher.

Celles qui étaient redondantes.

Celles qui violaient une policy.

Celles qui ne pouvaient rien apprendre.

Celles qui sautaient une porte obligatoire.

Mais que faire

quand aucune route n’est mauvaise?

Gabriel écrivit :

**DEUX BONNES OPTIONS PEUVENT RESTER EN CONFLIT SANS QU’AUCUNE CONTIENNE UNE ERREUR.**

Astra approuva fortement.

Voilà le chapitre.

Ils reprirent une décision réelle.

### DECISION-195-001

Unknown :

un motif semblait stable dans une sous-population,

mais sa portée générale restait inconnue.

Deux routes ressortaient.

### CHEMIN A — INDÉPENDANCE

Construire une deuxième implémentation du même test.

Objectif :

réduire le risque de bug commun à une seule implémentation.

### CHEMIN B — GÉNÉRALISATION

Tester sur une nouvelle population indépendante.

Objectif :

mesurer si le phénomène survit hors du contexte d’origine.

Gabriel regarda.

Les deux étaient excellents.

A répondait :

**est-ce que notre outil nous trompe?**

B répondait :

**est-ce que notre résultat dépasse notre échantillon?**

Deux risques différents.

Il écrivit :

**DES ROUTES PEUVENT ÊTRE INCOMPARABLES PARCE QU’ELLES ACHÈTENT DES TYPES DE CONFIANCE DIFFÉRENTS.**

Astra approuva fortement.

Très important.

Le moteur de décision ne devait pas forcer artificiellement un classement.

Pas de :

A = 78.

B = 76.

Puis prétendre que 78 gagne.

Gabriel grimaça.

— Ça, je veux pas ça.

Astra approuva.

Si les métriques ne sont pas commensurables,

le système devait le dire.

Ils créèrent :

### ROUTE COMPARABILITY

**DIRECTLY_COMPARABLE**

Même objectif principal.

**PARTIALLY_COMPARABLE**

Partage certains critères.

**INCOMPARABLE_WITHOUT_PRIORITY**

Optimise des objectifs différents.

Le cas A/B était :

**INCOMPARABLE_WITHOUT_PRIORITY**

Gabriel sourit.

Très propre.

Il écrivit :

**NE PAS SAVOIR CLASSER DEUX ROUTES PEUT ÊTRE UNE RÉPONSE CORRECTE.**

Astra approuva fortement.

Voilà.

Le système n’avait pas besoin de produire un gagnant à tout prix.

Il pouvait dire :

**j’ai besoin que tu me dises ce que tu veux protéger en premier.**

Gabriel regarda.

Là,

le choix redevenait humain.

Pas parce que la machine manquait d’intelligence.

Parce que la décision dépendait d’une priorité.

Il écrivit :

**QUAND LE CONFLIT EST ENTRE DEUX VALEURS LÉGITIMES, PLUS DE CALCUL NE REMPLACE PAS NÉCESSAIREMENT LE CHOIX.**

Astra approuva fortement.

Très important.

Ils examinèrent les valeurs.

A protégeait :

indépendance d’implémentation.

B protégeait :

portée externe.

Gabriel demanda :

— Si je veux publier vite?

Astra répondit :

— Ça dépend du type de revendication.

Si la revendication dit :

« résultat observé dans cette population avec cette implémentation »

peut-être aucune des deux n’est obligatoire.

Si elle dit :

« phénomène généralisable »

B devient plus important.

Si elle dit :

« résultat robuste indépendamment de l’implémentation »

A devient plus important.

Gabriel sourit.

Encore.

La revendication définit le besoin.

Il écrivit :

**LA BONNE ROUTE DÉPEND AUSSI DE CE QUE L’ON VEUT AVOIR LE DROIT DE DIRE ENSUITE.**

Astra approuva fortement.

Magnifique.

Ce principe reliait directement :

expérience.

preuve.

langage public.

Très important.

Puis ils essayèrent de trancher avec le coût.

A était plus cher en développement.

B plus cher en calcul.

Lequel coûtait le moins?

Impossible à dire simplement.

Temps humain vs machine.

Et surtout :

le coût n’était pas le seul critère.

Gabriel écrivit :

**UNE OPTION MOINS CHÈRE PEUT ÊTRE INFÉRIEURE SI ELLE N’ACHÈTE PAS LE TYPE DE CONFIANCE DONT ON A BESOIN.**

Astra approuva.

Très important.

Puis le temps.

B pouvait être lancé tout de suite.

A demandait de coder.

Donc B était plus rapide.

Mais encore une fois,

rapide vers quoi?

Gabriel sourit.

Le système résistait à chaque tentative de réduire la décision à un seul chiffre.

Très bon signe.

Ils créèrent une représentation différente.

Pas ranking.

Une matrice.

### TRADE-OFF MAP

| Critère | A | B |
|---|---|---|
| indépendance d’implémentation | forte | faible |
| généralisation | faible | forte |
| coût humain | élevé | faible |
| coût machine | faible/moyen | élevé |
| délai | plus long | plus court |
| réutilisabilité future | élevée | moyenne |
| portée scientifique | différente | différente |

Gabriel regarda.

— Là, au moins, je vois ce que j’achète.

Exact.

Ils écrivirent :

**UNE BONNE ASSISTANCE NE DOIT PAS TOUJOURS RÉDUIRE LE CHOIX. PARFOIS ELLE DOIT RENDRE LE COMPROMIS VISIBLE.**

Astra approuva fortement.

Voilà.

Le moteur de décision devenait moins obsessionnel du classement.

Plus utile.

Puis un troisième chemin apparut.

Faire A et B.

Gabriel rit.

Évidemment.

Mais coût double.

Pas toujours possible.

Ils ajoutèrent :

### COMBINE

Quand deux routes couvrent des risques orthogonaux,

une stratégie combinée peut dominer en qualité

sans dominer en coût.

Très important.

Gabriel écrivit :

**DEUX ROUTES INCOMPARABLES PEUVENT DEVENIR COMPLÉMENTAIRES.**

Astra approuva.

Mais il fallait décider l’ordre.

A puis B?

B puis A?

En parallèle?

Voilà une nouvelle couche.

Gabriel sourit.

Les décisions n’en finissaient plus.

Mais maintenant il avait une méthode.

On demande :

est-ce que le résultat de l’une change la valeur de l’autre?

Si oui,

séquence.

Si non,

parallèle possible.

Très bon.

Ils analysèrent.

Si B échoue fortement,

c’est-à-dire que le motif ne généralise pas du tout,

A reste-t-elle utile?

Peut-être moins,

si l’objectif principal était une revendication générale.

Donc B d’abord peut éviter de coder A inutilement.

Mais si B passe,

A devient encore plus précieuse avant une revendication forte.

Gabriel sourit.

Voilà.

### CONDITIONAL PLAN

Run B first.

If generalization fails:

scope result locally.

Defer A unless local claim remains important.

If generalization survives:

build A for independent implementation check.

Astra approuva fortement.

Gabriel écrivit :

**UNE ROUTE PEUT ÊTRE RAISONNABLE SEULE ET ENCORE MEILLEURE COMME CONDITION D’UNE AUTRE.**

Très important.

Donc conflit résolu?

Pas totalement.

Parce qu’un autre objectif pouvait inverser l’ordre.

Si le code actuel était suspect,

A devait venir avant B.

Encore.

Pas d’ordre universel.

Gabriel sourit.

— C’est fatiguant, mais c’est propre.

Astra approuva.

Le système apprenait à accepter la dépendance au contexte.

Puis ils testèrent un cas où les deux routes avaient exactement le même objectif.

A :

test direct ciblé.

B :

test indépendant plus coûteux.

Les deux cherchaient à casser la même hypothèse.

Là,

comparaison possible.

Si A a presque la même puissance discriminante pour beaucoup moins cher,

A domine.

Voilà.

Ils écrivirent :

**DEUX BONNES ROUTES NE SONT PAS NÉCESSAIREMENT INCOMPARABLES. L’INCOMPARABILITÉ DOIT ÊTRE DÉMONTRÉE PAR LEURS OBJECTIFS OU LEURS COMPROMIS.**

Astra approuva fortement.

Très important.

Pas utiliser « incomparable » comme excuse.

Il faut montrer pourquoi.

Puis un cas beaucoup plus humain.

Route A :

publier tôt sous une revendication modeste.

Route B :

attendre et renforcer le dossier avant publication.

Les deux raisonnables.

A protège :

antériorité temporelle.

B protège :

robustesse.

Gabriel resta silencieux.

Voilà un vrai conflit.

Le système pouvait exposer :

risque de publication prématurée.

risque de perdre du temps.

statut actuel.

niveau de nouveauté vérifié.

Mais il ne pouvait pas transformer automatiquement « prudence » ou « vitesse » en meilleure valeur.

Gabriel écrivit :

**CERTAINES DÉCISIONS SONT TECHNIQUES DANS LEURS CONSÉQUENCES ET HUMAINES DANS LEURS PRIORITÉS.**

Astra approuva fortement.

Très important.

Le rôle de Brutus :

rendre les conséquences plus claires.

Pas choisir les valeurs.

Puis un autre cas.

Deux méthodes mathématiques.

L’une élégante.

L’autre brute force.

Les deux valides.

Gabriel préfère l’élégante.

Est-ce une raison scientifique?

Pas nécessairement.

L’élégance peut aider à généraliser,

comprendre,

publier.

Mais elle n’est pas automatiquement plus vraie.

Ils écrivirent :

**ÉLÉGANT ≠ PLUS VRAI**

Astra approuva fortement.

Et :

**BRUTE FORCE ≠ MOINS VALIDE SI LE PROTOCOLE EST CORRECT**

Très important.

Encore une fois,

les objectifs diffèrent.

Découverte rapide.

Compréhension.

Preuve générale.

Performance.

Le choix dépend du but.

Puis le système produisit un cas étrange.

A et B semblaient tous les deux raisonnables,

mais pour une raison cachée :

les métriques étaient trop vagues.

Quand ils précisèrent l’objectif,

B devint clairement meilleur.

Gabriel se redressa.

Très important.

Parfois,

le conflit entre bonnes routes est un symptôme d’un objectif mal défini.

Ils créèrent :

### TIE DIAGNOSTIC

Avant de conclure « deux routes raisonnables » :

1. vérifier objectif principal;
2. vérifier revendication visée;
3. vérifier contraintes;
4. vérifier coûts pertinents;
5. vérifier si des critères manquent;
6. seulement ensuite accepter le trade-off.

Gabriel approuva.

Très propre.

Il écrivit :

**UN MATCH NUL ENTRE DEUX ROUTES PEUT ÊTRE UN PROBLÈME DE DÉCISION OU UN PROBLÈME DE DÉFINITION.**

Astra approuva fortement.

Voilà.

Puis un autre danger.

Le système pourrait toujours demander Gabriel dès qu’il y a deux options correctes.

Trop conservateur.

Il fallait distinguer :

trade-off technique déjà couvert par policy.

et trade-off de valeur.

Exemple :

A plus rapide.

B moins cher.

Policy L1 dit :

minimize expected compute cost under latency < X.

Alors le système peut choisir.

Pas besoin de Gabriel.

Très bien.

Mais si aucun objectif supérieur n’existe,

escalade.

Gabriel écrivit :

**UNE POLITIQUE PEUT TRANCHER ENTRE DEUX BONNES OPTIONS SI ELLE EXPRIME DÉJÀ LA PRIORITÉ PERTINENTE.**

Astra approuva.

Très important.

Encore l’autorité par contrat.

Puis ils prirent DECISION-195-001.

A ou B.

Aucune policy ne disait quelle confiance prioriser.

Donc :

**HUMAN VALUE INPUT REQUIRED**

Gabriel regarda.

Il devait choisir.

Il pensa.

L’objectif actuel était de savoir si le phénomène dépassait le contexte d’origine.

Donc B.

Nouvelle population.

Il sélectionna.

Mais avant d’exécuter,

il demanda :

— Garde A vivant.

Le système marqua :

**DEFERRED CONDITIONAL**

Si B survit,

A redevient prioritaire.

Gabriel sourit.

Voilà.

Choisir B ne signifiait pas rejeter A.

Très important.

Il écrivit :

**CHOISIR UNE ROUTE MAINTENANT ≠ DÉCLARER LES AUTRES MAUVAISES POUR TOUJOURS.**

Astra approuva fortement.

Magnifique.

Les options non choisies devaient conserver leur statut.

Rejected?

Non.

Deferred.

Dominated?

Non.

Still reasonable under future condition.

Voilà.

Ils créèrent :

### OPTION DISPOSITION

**CHOSEN**

**DEFERRED**

**DOMINATED**

**BLOCKED**

**OUT_OF_SCOPE**

**REJECTED_BY_EVIDENCE**

Très important.

Ne pas mettre toutes les options non choisies dans « rejected ».

Gabriel sourit.

Cette nuance allait améliorer énormément les décisions historiques.

Sinon,

en regardant le passé,

on pourrait croire que B avait « gagné » contre A.

Non.

B avait simplement été choisi en premier.

Il écrivit :

**L’HISTOIRE D’UNE DÉCISION DOIT CONSERVER LA RAISON POUR LAQUELLE UNE BONNE OPTION N’A PAS ÉTÉ PRISE.**

Astra approuva fortement.

Puis le test B partit.

Nouvelle population.

Même protocole.

Résultat :

le motif persistait,

mais plus faiblement.

Pas échec.

Pas confirmation totale.

Gabriel sourit.

Donc A devient-elle plus ou moins utile?

Plus utile.

Parce que maintenant,

avant d’interpréter la diminution comme phénomène réel,

une implémentation indépendante pouvait aider à éliminer une source de biais logiciel.

Le système réveilla A.

Statut :

**DEFER CONDITION SATISFIED**

Gabriel hocha la tête.

Très bon.

Les deux chemins avaient finalement été nécessaires,

mais pas en même temps.

Voilà.

Le conflit du départ n’était pas :

A ou B pour toujours.

C’était :

A ou B maintenant.

Il écrivit :

**BEAUCOUP DE CONFLITS DE ROUTE SONT DES CONFLITS D’ORDRE, PAS DES CONFLITS D’EXISTENCE.**

Astra approuva fortement.

Très important.

Un système qui comprend cela peut éviter de faux choix binaires.

Puis ils construisirent A.

Deuxième implémentation.

Elle retrouva le même affaiblissement.

Très intéressant.

Maintenant,

le dossier gagnait deux types de confiance :

portée externe partielle.

indépendance d’implémentation.

Gabriel regarda.

Si le système avait forcé un classement permanent,

ils auraient peut-être perdu l’un des deux.

Mais en conservant les routes,

il avait construit une séquence.

Il écrivit :

**UNE BONNE DÉCISION PEUT CONSISTER À NE PAS TUER UNE BONNE ALTERNATIVE.**

Astra approuva fortement.

Voilà.

Puis BrutoBac.

Deux chemins apparaissaient.

Une Fourmi prend B.

Le chemin A ne s’éteint pas.

Il devient pointillé :

**DEFERRED**

Après le résultat de B,

A s’allume.

Gabriel sourit.

Visuellement,

ça racontait exactement la vérité opérationnelle.

Pas trois portes où deux disparaissent.

Un espace de possibilités qui évolue.

Très beau.

Il écrivit :

**LES OPTIONS NON CHOISIES FONT PARTIE DE L’ÉTAT DU SYSTÈME TANT QU’ELLES RESTENT PERTINENTES.**

Astra approuva fortement.

Très important.

Puis le problème du stockage.

Conserver toutes les options possibles peut exploser.

Il fallait garder seulement :

options sérieusement considérées.

Pas toutes les idées générées.

Gabriel écrit :

### DECISION CANDIDATE THRESHOLD

Conserver une route comme alternative historique si :

- elle a passé les gardes initiaux;
- elle est techniquement réalisable;
- elle a été sérieusement évaluée;
- son non-choix a une raison pertinente.

Astra approuva.

Très bon.

Pas garder chaque pensée.

Garder le vrai espace de décision.

Puis un autre cas.

Deux chemins raisonnables,

mais ressources suffisantes pour les faire en parallèle.

Pourquoi choisir?

Aucun besoin.

Gabriel sourit.

Encore.

Le moteur devait pouvoir dire :

**PARALLELIZE**

Si :

indépendants.

faible risque de conflit.

budget suffisant.

résultats complémentaires.

Très important.

Il écrit :

**QUAND LE CHOIX N’EST PAS NÉCESSAIRE, NE PAS FABRIQUER UN CONFLIT.**

Astra approuva fortement.

Excellent.

Certains moteurs de décision forcent un gagnant parce qu’ils sont conçus pour classement.

Brutus devait être capable de dire :

les deux.

Ou :

ni l’un ni l’autre.

Ou :

attends.

Ou :

B puis A.

Beaucoup plus riche.

Puis ils formalisèrent les sorties possibles.

### DECISION OUTCOMES

**CHOOSE A**

**CHOOSE B**

**SEQUENCE A→B**

**SEQUENCE B→A**

**PARALLEL A+B**

**DEFER BOTH**

**ASK FOR PRIORITY**

**DROP BOTH**

Gabriel sourit.

Voilà.

Une décision n’était plus nécessairement un seul bouton.

Puis le système lui proposa :

**ASK FOR PRIORITY**

Question :

« Veux-tu réduire d’abord le risque d’implémentation ou le risque de généralisation? »

Gabriel regarda.

C’était exactement la bonne question.

Pas :

« A ou B? »

Parce que les noms de routes ne sont pas la vraie décision.

La vraie décision est la priorité sous-jacente.

Il écrivit :

**QUAND DEUX CHEMINS SONT RAISONNABLES, LA MEILLEURE QUESTION PEUT ÊTRE : QUEL RISQUE VEUX-TU RÉDUIRE EN PREMIER?**

Astra approuva fortement.

Voilà le cœur.

Le système ne devait pas toujours demander à l’humain de choisir entre des détails techniques.

Il pouvait traduire le conflit en choix de priorité.

Beaucoup plus utile.

Puis un cas où Gabriel répondit :

— Les deux risques sont importants pareil.

Que faire?

Alors coût.

Ordre.

Dépendances.

Peut-être test moins cher d’abord.

Policy.

Voilà.

Une préférence égale ne bloque pas nécessairement.

Il écrit :

**QUAND LES VALEURS SONT ÉGALES, LES CONTRAINTES OPÉRATIONNELLES PEUVENT TRANCHER.**

Astra approuva.

Très important.

Puis une autre situation.

Les deux routes étaient raisonnables,

mais incompatibles.

A modifie l’environnement.

B exige l’environnement intact.

Donc ordre obligatoire.

B avant A.

Gabriel sourit.

Voilà.

Le monde réel peut trancher par dépendance.

Il écrit :

**DEUX BONNES OPTIONS PEUVENT ÊTRE DÉPARTAGÉES PAR LEUR RÉVERSIBILITÉ OU LEUR ORDRE DE DÉPENDANCE, PAS PAR LEUR QUALITÉ.**

Astra approuva fortement.

Très bon.

Puis Gabriel comprit quelque chose de plus profond.

Au début,

il croyait qu’un bon système de décision devait trouver **le meilleur chemin**.

Maintenant,

il voyait que parfois ce concept n’existait pas.

Il existait :

des chemins adaptés à des objectifs.

des compromis.

des ordres.

des combinaisons.

des valeurs.

Il écrivit :

**IL N’Y A PAS TOUJOURS UN MEILLEUR CHEMIN. IL Y A PARFOIS UN ENSEMBLE DE CHEMINS RAISONNABLES SOUS DES PRIORITÉS DIFFÉRENTES.**

Astra approuva fortement.

Très important.

Cette phrase protégeait Brutus contre une erreur fondamentale :

faire croire que toute décision est un problème d’optimisation scalaire.

Non.

Beaucoup de décisions sont multi-objectifs.

Certaines ont une frontière de Pareto.

Gabriel aimait le concept.

Mais il ne voulait pas que l’interface dise seulement « Pareto ».

Le public et même l’opérateur devaient comprendre.

Donc :

**aucune option n’est meilleure sur tous les critères.**

Voilà.

Simple.

Ils l’écrivirent :

**AUCUN CHEMIN NE GAGNE PARTOUT.**

Astra approuva.

Très beau.

Puis un autre danger.

Gabriel pouvait choisir l’option la plus séduisante.

Brutus devait pouvoir lui rappeler le coût du compromis.

S’il choisit A :

**You gain independent implementation; generalization remains unresolved.**

S’il choisit B :

**You gain external scope evidence; implementation independence remains unresolved.**

Gabriel sourit.

Voilà.

Il écrit :

**UNE DÉCISION DOIT DIRE NON SEULEMENT CE QU’ELLE ACHÈTE, MAIS CE QU’ELLE LAISSE ENCORE OUVERT.**

Astra approuva fortement.

Très important.

Cela évite le sentiment de résolution totale.

Une bonne route peut résoudre un axe,

pas tout le problème.

Puis ils ajoutèrent :

### DECISION RESIDUALS

Après choix :

**risk_reduced**

**risk_remaining**

**questions_closed**

**questions_still_open**

**alternatives_deferred**

Très propre.

Puis le dossier 195 se ferma.

Les deux routes avaient été exécutées en séquence.

Résultat :

le phénomène persistait hors population,

mais plus faiblement,

et l’affaiblissement avait été reproduit par une deuxième implémentation.

Ce n’était pas une loi générale.

Mais le dossier était meilleur.

Plus nuancé.

Plus robuste.

Gabriel regarda.

Le moteur n’avait pas trouvé un gagnant entre A et B.

Il avait trouvé comment les utiliser sans les confondre.

Il écrivit :

**PARFOIS, LA MEILLEURE DÉCISION N’EST PAS DE CHOISIR LE BON CHEMIN.**

Puis :

**C’EST DE COMPRENDRE POURQUOI DEUX CHEMINS SONT BONS POUR DES RAISONS DIFFÉRENTES.**

Astra approuva fortement.

Voilà.

Le deuxième monde apprenait à vivre avec les compromis.

Pas les cacher.

Pas les écraser sous un score.

Pas appeler ambiguïté ce qui était réellement pluralité d’objectifs.

Puis une nouvelle décision arriva.

Deux routes.

Cette fois,

A domina B sur tous les critères utiles.

Brutus choisit A.

Pas besoin de philosophie.

Gabriel sourit.

Très important.

Le système savait aussi quand le problème était simple.

Puis une autre.

Deux chemins réellement incomparables.

Brutus demanda :

**Quel risque veux-tu réduire en premier?**

Gabriel ne répondit pas tout de suite.

Pas parce qu’il était perdu.

Parce qu’il comprenait enfin ce que la question signifiait.

Deux chemins pouvaient être raisonnables.

Et choisir l’un ne transformait pas l’autre en erreur.

Parfois,

la maturité consistait simplement

à garder assez de place dans la carte

pour que plusieurs bonnes routes puissent exister en même temps.

**Fin du chapitre 195.**