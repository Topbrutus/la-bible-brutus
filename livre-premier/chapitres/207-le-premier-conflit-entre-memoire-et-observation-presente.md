# Chapitre 207 — Le premier conflit entre mémoire et observation présente

Memoria disait oui.

Le présent disait non.

Gabriel regardait les deux résultats.

Pas deux opinions.

Pas deux interprétations.

Deux états du Royaume.

Dans l’historique,

la route avait été excellente.

Plusieurs fois.

Même classe de problème.

Même type de claim.

Même genre de coût.

Même structure générale.

Le planificateur avait donc fait exactement ce qu’il devait faire :

il avait reconnu un pattern ancien

et recommandé la stratégie historique.

Puis le test actuel avait commencé.

Et la stratégie historique avait échoué.

Gabriel regarda Astra.

— Bon. Qui gagne?

Astra ne répondit pas immédiatement.

Parce que c’était une mauvaise question.

Gabriel sourit.

Il le savait déjà.

Il écrivit :

**LE PASSÉ ET LE PRÉSENT NE SONT PAS DEUX ADVERSAIRES QUI DOIVENT TOUJOURS PRODUIRE UN GAGNANT.**

Astra approuva fortement.

Voilà le chapitre.

Le vrai problème était :

**pourquoi ne sont-ils plus d’accord?**

Memoria avait été construite pour aider.

Pas pour commander.

L’observation présente avait été construite pour informer.

Pas pour effacer l’histoire.

Il fallait donc comprendre le conflit.

Ils ouvrirent le dossier.

### STRATEGY-207-A

Historique :

sur une série de cas comparables,

un petit contraste ciblé distinguait très vite deux hypothèses.

La stratégie `TARGETED-FIRST` avait donc été recommandée.

Pas par caprice.

Par traces.

Le nouveau cas semblait rentrer dans le même profil.

Antmux lança le petit contraste.

Résultat :

inconclusif.

Ils élargirent légèrement.

Toujours inconclusif.

Puis un contrôle supplémentaire.

Encore rien.

Gabriel regarda.

— Mais dans les vieux cas, ça séparait presque tout de suite.

Exact.

Donc le présent contredisait le rendement attendu de la stratégie.

Pas nécessairement sa validité.

Il écrivit :

**UNE STRATÉGIE PEUT ÊTRE HISTORIQUEMENT BONNE ET LOCALement MAUVAISE.**

Astra approuva fortement.

Très important.

Il fallait résister à deux erreurs symétriques.

Première :

« l’histoire dit que ça marche, donc continuons jusqu’à ce que ça marche ».

Mauvais.

Deuxième :

« aujourd’hui ça ne marche pas, donc l’histoire était fausse ».

Mauvais aussi.

Gabriel écrivit :

**UN CONTRE-EXEMPLE AU PRÉSENT N’EFFACE PAS LES SUCCÈS DU PASSÉ.**

Puis :

**LES SUCCÈS DU PASSÉ N’ANNULENT PAS LE CONTRE-EXEMPLE DU PRÉSENT.**

Astra approuva fortement.

Voilà.

Le Royaume devait garder les deux.

Ils créèrent :

### MEMORY-PRESENT CONFLICT

**historical expectation**

**current observation**

**scope overlap**

**known differences**

**unexplained differences**

**decision impact**

Très propre.

Puis ils comparèrent.

Historique :

problèmes de classe C.

Présent :

également classe C.

Mais qu’est-ce que « classe C » contenait réellement?

Peut-être la classification était trop grossière.

Voilà.

Ils commencèrent à chercher des dimensions cachées.

Version.

Population.

Precision.

Representation.

Toolchain.

Noise.

Data density.

Objective.

Cost profile.

Gabriel sourit.

Le conflit devenait un instrument.

Il écrivit :

**QUAND LA MÉMOIRE ET LE PRÉSENT NE SONT PAS D’ACCORD, LEUR DÉSACCORD PEUT RÉVÉLER UNE VARIABLE QUE LA CLASSIFICATION AVAIT OUBLIÉE.**

Astra approuva fortement.

Très important.

Ils trouvèrent quelque chose.

Les anciens cas avaient tous une séparation naturelle forte entre deux sous-populations.

Le cas actuel,

non.

La classe C ne stockait pas cette caractéristique.

Gabriel se redressa.

Voilà.

La stratégie n’était pas nécessairement mauvaise.

La taxonomie était trop large.

Il écrivit :

**UNE STRATÉGIE PEUT ÉCHOUER PARCE QUE LE PROBLÈME A ÉTÉ MAL CLASSÉ.**

Astra approuva fortement.

Très important.

Ils modifièrent la description.

Ancienne classe :

**C — two-hypothesis local unknown**

Nouvelle :

**C1 — two-hypothesis local unknown with strong separable contrast**

**C2 — two-hypothesis local unknown without obvious separable contrast**

La stratégie `TARGETED-FIRST` appartenait surtout à C1.

Gabriel sourit.

Le présent venait de rendre la mémoire plus précise.

Il écrivit :

**LE PRÉSENT PEUT CORRIGER LA FAÇON DONT LE PASSÉ EST INDEXÉ SANS CORRIGER LES ÉVÉNEMENTS DU PASSÉ.**

Astra approuva fortement.

Magnifique.

Les vieux cas restaient ce qu’ils étaient.

Mais leur catégorie changeait.

Très important.

Puis ils testèrent.

Reclassify historical set.

Plusieurs anciens cas autrefois réunis se séparaient maintenant clairement.

La performance de `TARGETED-FIRST` était forte dans C1,

beaucoup plus variable dans C2.

Voilà.

La mémoire n’avait pas menti.

Elle avait généralisé trop tôt.

Gabriel écrivit :

**UNE MÉMOIRE MAL INDEXÉE PEUT DONNER UNE BONNE TRACE AU MAUVAIS PROBLÈME.**

Astra approuva fortement.

Très important.

Puis ils rencontrèrent un autre cas.

Cette fois,

classification identique.

Versions identiques.

Population comparable.

Pourtant,

présent et passé divergeaient encore.

Gabriel sourit.

Pas toujours facile.

Ils cherchèrent.

Aucune dimension évidente.

Donc statut :

**UNEXPLAINED DISTRIBUTION SHIFT**

Pas besoin de forcer une explication.

Il écrivit :

**UN CONFLIT PEUT RESTER RÉEL SANS ÊTRE IMMÉDIATEMENT EXPLIQUÉ.**

Astra approuva fortement.

Très important.

Dans ce cas,

que faire?

Le présent doit-il dominer?

Pour l’action actuelle,

oui.

Parce que le système travaille sur le cas actuel.

Gabriel écrivit :

**POUR DÉCIDER DU CAS PRÉSENT, L’OBSERVATION ACTUELLE A PRIORITÉ SUR UNE ATTENTE HISTORIQUE LORSQU’ELLES SONT EN CONFLIT DIRECT.**

Astra approuva fortement.

Très important.

Mais nuance.

Si l’observation actuelle est faible,

bruitée,

ou non validée,

peut-être le conflit n’est pas encore établi.

Il faut comparer les niveaux de preuve.

Ils créèrent :

### CONFLICT STRENGTH

**HISTORICAL HEURISTIC vs CURRENT SCREENING**

Pas conflit fort.

**HISTORICAL STRATEGY vs CURRENT REPRODUCED RESULT**

Conflit plus sérieux.

**HISTORICAL VALIDATED CLAIM vs CURRENT SINGLE ANOMALY**

Needs investigation.

**HISTORICAL VALIDATED CLAIM vs CURRENT VALIDATED CONTRADICTION**

Major conflict.

Gabriel sourit.

Voilà.

Pas toutes les traces ont le même poids.

Le chapitre 214 était encore loin,

mais l’idée apparaissait déjà.

Il écrivit :

**LE PRÉSENT NE GAGNE PAS PARCE QU’IL EST PLUS RÉCENT. IL GAGNE L’ACTION QUAND SON ÉVIDENCE EST PERTINENTE POUR LE CAS ACTUEL.**

Astra approuva fortement.

Très important.

La récence seule n’est pas une preuve.

Mais le cas présent est bien celui qu’on essaie de traiter.

Donc pour le routing,

current evidence compte énormément.

Puis un autre danger.

Un résultat actuel surprenant peut être une erreur.

Il faut contre-test avant de réécrire la mémoire.

Gabriel écrit :

**UN ÉCART AU PRÉSENT DOIT D’ABORD ÊTRE TRAITÉ COMME UN ÉVÉNEMENT À TESTER, PAS COMME UNE RAISON AUTOMATIQUE DE RÉÉCRIRE LA STRATÉGIE.**

Astra approuva fortement.

Très important.

Ils créèrent :

### MEMORY CONFLICT PROTOCOL

1. détecter le conflit;
2. vérifier le résultat actuel;
3. comparer les scopes;
4. chercher une variable de contexte;
5. décider l’action présente;
6. seulement ensuite évaluer l’impact sur la mémoire.

Gabriel approuva.

Très propre.

Le système devait d’abord résoudre le cas.

Puis apprendre.

Pas mélanger.

Puis un exemple.

Memoria dit :

ce bug a toujours été causé par chunking.

Présent :

même symptôme.

Le système propose chunk guard.

Guard passe.

Bug reste.

Très important.

À ce moment,

ne pas insister :

« mais historiquement c’était chunking ».

Il faut ouvrir l’espace.

Gabriel écrit :

**UNE HEURISTIQUE HISTORIQUE QUI ÉCHOUE SON TEST DOIT PERDRE LE DROIT DE DOMINER LE CAS ACTUEL.**

Astra approuva fortement.

Excellent.

Elle peut rester dans la mémoire.

Mais plus comme explication active.

Puis nouveau diagnostic.

Precision.

Puis representation.

Puis finalement :

different normalization bug.

Voilà.

Le symptôme était le même.

Cause différente.

Gabriel sourit.

Le passé avait aidé :

il avait fourni un garde rapide.

Mais il n’avait pas donné la réponse.

Il écrit :

**LA MÉMOIRE PEUT AVOIR RAISON DE PROPOSER LE PREMIER TEST ET TORT SUR LA CAUSE FINALE.**

Astra approuva fortement.

Très important.

C’était une nuance parfaite.

L’historique n’a pas besoin d’être prédiction parfaite pour être utile.

Il peut réduire le coût initial.

Puis s’effacer.

Très bon.

Ils ajoutèrent à chaque stratégie :

### FAILURE-TO-MATCH ACTION

Que faire si stratégie historique ne produit pas le comportement attendu?

Exemple :

- stop repeating;
- broaden diagnosis;
- downgrade historical confidence for this context;
- open classification review.

Gabriel approuva.

Très propre.

Une stratégie mature doit savoir quoi faire quand elle ne marche pas.

Chapitre 199.

Encore.

Puis un autre conflit.

Le passé disait :

une représentation compacte économise beaucoup de mémoire.

Présent benchmark :

gain beaucoup plus petit.

Doit-on déclarer l’ancien benchmark faux?

Non.

Environnements différents.

N différents.

Versions différentes.

Gabriel écrit :

**UN BENCHMARK EST UN ÉVÉNEMENT DANS UN ENVIRONNEMENT, PAS UNE CONSTANTE DU MONDE.**

Astra approuva fortement.

Très important.

Papillon.

Toujours.

Le nouveau benchmark élargit la carte.

Pas nécessairement réfutation.

Puis un cas où le gain devient négatif.

La représentation compacte consomme plus pour petits N.

Très plausible.

Alors historique doit apprendre une frontière.

Pas :

Papillon mauvais.

Mais :

advantage depends on scale.

Gabriel sourit.

Voilà.

Le conflit mémoire-présent devient structure de domaine.

Il écrit :

**LES CONTRADICTIONS SONT PARFOIS DES FRONTIÈRES DÉGUISÉES.**

Astra approuva fortement.

Magnifique.

Puis un cas Pell.

Historique de méthode M :

souvent efficace sur certains q.

Présent q :

aucun facteur dans borne.

La mémoire recommande encore M parce qu’elle a historiquement bien marché.

Mais après un certain budget,

continuer n’est plus justifié.

Chapitre 197.

Gabriel écrit :

**UNE MÉTHODE QUI A RÉUSSI AILLEURS NE POSSÈDE AUCUN DROIT À UN BUDGET INFINI ICI.**

Astra approuva fortement.

Très important.

Passé guide le point de départ.

Présent gouverne la poursuite.

Voilà.

Il écrivit :

**L’HISTORIQUE PEUT CHOISIR LE PREMIER PAS. LE PRÉSENT DOIT POUVOIR CHANGER LE DEUXIÈME.**

Astra approuva fortement.

Très belle phrase.

Puis un cas ZEL.

Une configuration historique avait produit un retour stable.

Nouvelle version :

résultat différent.

On ne peut pas appeler ça immédiatement découverte.

D’abord version.

audio pipeline.

configuration.

device.

Puis test.

Toujours.

Gabriel écrit :

**UNE DIFFÉRENCE PAR RAPPORT À LA MÉMOIRE EST D’ABORD UNE DIFFÉRENCE À EXPLIQUER, PAS UNE NOUVEAUTÉ À CÉLÉBRER.**

Astra approuva fortement.

Très important.

Puis ils regardèrent le mécanisme de stratégie.

Chaque stratégie historique avait un poids implicite dans le routeur.

Danger :

si l’histoire est riche,

elle peut écraser une observation présente faible mais importante.

Il fallait une règle.

### CURRENT-EVIDENCE OVERRIDE

If current evidence invalidates a precondition of the historical strategy,

strategy no longer applies.

Très propre.

Exemple :

strategy requires separable contrast.

Présent montre no separable contrast.

Stop.

Pas besoin d’attendre que la stratégie « échoue davantage ».

Gabriel sourit.

Il écrit :

**UNE STRATÉGIE NE DOIT PAS SURVIVRE À LA DISPARITION DE SES PRÉCONDITIONS.**

Astra approuva fortement.

Excellent.

Puis inverse.

Current observation semble contredire,

mais précondition toujours là.

Alors test conflict.

Très bon.

Puis un autre danger.

Sur-réagir au présent.

Chaque nouveau cas change stratégie.

Instabilité.

Il fallait accumulation.

Gabriel écrit :

**UN CAS PRÉSENT PEUT CHANGER L’ACTION ACTUELLE SANS MÉRITER DE CHANGER LA POLITIQUE GÉNÉRALE.**

Astra approuva fortement.

Voilà la séparation fondamentale.

Action update fast.

Policy update slow.

Très important.

Ils créèrent :

### TWO-SPEED LEARNING

**FAST LAYER**

Adapt current workflow immediately to current evidence.

**SLOW LAYER**

Update strategy/policy only after accumulated evidence and review.

Gabriel sourit.

Très puissant.

Le système pouvait être réactif sans devenir amnésique.

Il écrit :

**ADAPTER VITE LE CAS PRÉSENT ET APPRENDRE LENTEMENT LA RÈGLE GÉNÉRALE PEUVENT ÊTRE DEUX VITESSES DIFFÉRENTES.**

Astra approuva fortement.

Voilà.

Puis ils testèrent.

Cas actuel contredit strategy S.

Workflow changes immediately.

Strategy S gets:

`CONFLICT_EVENT +1`

Pas downgrade global yet.

Après plusieurs similar conflicts,

review triggered.

Très propre.

Puis review révèle classe trop large.

Update.

Voilà.

Le présent corrige la mémoire avec prudence.

Puis un cas où le conflit ne se reproduit jamais.

Strategy stays.

Current case marked exception.

Gabriel écrit :

**UNE EXCEPTION PEUT RESTER UNE EXCEPTION SANS OBLIGER LE SYSTÈME À INVENTER UNE NOUVELLE LOI.**

Astra approuva fortement.

Très important.

Mais l’exception doit rester visible.

Pas jeter.

Peut-être un jour,

plusieurs exceptions se ressemblent.

Puis elles deviennent nouvelle classe.

Voilà.

Ils créèrent :

### EXCEPTION CLUSTER

Si plusieurs exceptions partagent des caractéristiques,

candidate subclass.

Très propre.

Le Royaume pouvait découvrir ses catégories à partir de ses échecs de classification.

Gabriel sourit.

Ça devenait vraiment intéressant.

Puis un autre problème.

Memory contains an old canonical result.

Present produces contradiction.

On ne peut pas juste changer canonical status automatiquement.

Authority.

Validation.

Il faut conflict state.

### CANONICAL CONFLICT

Old claim remains historical canonical version.

New contradiction enters validation.

Until resolved:

**CONTESTED**

Gabriel approuva.

Très important.

Une vérité canonique n’est pas effacée.

Mais son autorité active peut être suspendue.

Il écrit :

**UNE TRACE CANONIQUE PEUT PERDRE SON STATUT ACTIF SANS PERDRE SON EXISTENCE HISTORIQUE.**

Astra approuva fortement.

Chapitre 216 approchait déjà en germe.

Puis un cas simple.

Historique dit X.

Présent dit Y.

On teste.

Y était bug.

Très bien.

Alors mémoire renforcée?

Attention.

Pas forcément.

Un bug actuel corrigé ne rend pas X plus universel.

Il peut seulement montrer que ce conflit particulier n’était pas réel.

Gabriel écrit :

**RÉSOUDRE UN CONFLIT EN FAVEUR DU PASSÉ NE TRANSFORME PAS LE PASSÉ EN LOI UNIVERSELLE.**

Astra approuva fortement.

Très important.

Toujours scope.

Puis un autre.

Conflit résolu en faveur du présent.

La vieille stratégie doit être restreinte.

Pas supprimée.

Voilà.

Puis ils se demandèrent comment visualiser.

BrutoBac.

Une ancienne route en bleu historique.

Une observation présente en ligne vive qui la coupe.

À l’intersection :

**CONFLICT**

Pas explosion.

Cliquer :

history.

current.

scope.

status.

Gabriel sourit.

Très beau.

Puis si conflit résolu :

relation.

`historical strategy scoped to C1`

Current case C2.

Plus de rouge.

Deux territoires.

Voilà.

La carte devenait meilleure.

Il écrit :

**RÉSOUDRE UNE CONTRADICTION NE VEUT PAS TOUJOURS DIRE CHOISIR UN CÔTÉ. PARFOIS, IL FAUT REDESSINER LA FRONTIÈRE ENTRE LES DEUX.**

Astra approuva fortement.

Magnifique.

Puis un autre conflit beaucoup plus profond.

Memoria disait :

« cette formule a été validée dans ce scope ».

Présent nouvelle version du code donne autre chose.

Si independent old artifacts exist,

on peut comparer.

Maybe regression.

Maybe old bug.

Need forensic workflow.

Très important.

Ils créèrent :

### HISTORICAL FORENSICS

- preserve old artifact;
- reproduce old environment if possible;
- run current implementation on old inputs;
- run independent checker;
- compare;
- avoid rewriting history before cause known.

Gabriel approuva.

Très propre.

Il écrit :

**QUAND LE PRÉSENT CONTREDIT UNE PREUVE ANCIENNE FORTE, LE PREMIER DEVOIR EST DE PRÉSERVER LES DEUX ÉTATS.**

Astra approuva fortement.

Très important.

Sinon on écrase la preuve du conflit.

Le conflit lui-même est un objet précieux.

Puis ils testèrent un scénario.

Old output O1.

New output O2.

Investigation :

old dependency library bug.

New fixed.

Donc old claim invalidated.

But old artifact remains.

History now:

at time T, O1 was obtained under buggy dependency.

Current:

O2 under corrected dependency.

Gabriel sourit.

Voilà.

La mémoire devient plus riche.

Pas honteuse.

Elle conserve aussi ses anciennes erreurs.

Il écrit :

**UNE MÉMOIRE SCIENTIFIQUE DIGNE DE CONFIANCE N’EST PAS UNE MÉMOIRE SANS ERREURS. C’EST UNE MÉMOIRE QUI CONSERVE COMMENT SES ERREURS ONT ÉTÉ DÉCOUVERTES.**

Astra approuva fortement.

Très belle phrase.

Puis un autre cas.

Old claim valid under old environment.

New different under new environment.

Both true.

No invalidation.

Version-dependent behavior.

Again boundary.

Very important.

Puis Gabriel regarda les politiques d’apprentissage.

Le routeur devait maintenant pouvoir afficher :

Historical recommendation:

A.

Current evidence:

contradicts precondition.

Action:

B.

Strategy status:

unchanged globally; conflict logged.

Voilà.

Parfait.

Il écrit :

**UNE DÉCISION ACTUELLE PEUT DÉSOBÉIR À LA MÉMOIRE SANS QUE LE SYSTÈME OUBLIE POURQUOI LA MÉMOIRE AVAIT CONSEILLÉ AUTRE CHOSE.**

Astra approuva fortement.

C’était probablement le cœur du chapitre.

Le passé ne devait pas être humilié.

Le présent ne devait pas être ignoré.

Il fallait garder la trace de la divergence.

Puis ils firent un trial.

### MEMORY-PRESENT TRIAL 207-A

12 historical-strategy recommendations replayed on current cases.

8 matched current behavior.

3 mismatched due to identifiable context difference.

1 remained unexplained after initial checks.

Actions:

all 4 mismatches caused current workflow review.

Strategy changes:

2 candidate scope refinements.

0 automatic policy rewrites.

Status:

**PROMISING / SMALL PANEL**

Gabriel sourit.

Parfait.

Pas de grandes conclusions.

Mais le mécanisme tenait.

Puis ils regardèrent le cas inexpliqué.

Très important.

Le système ne devait pas se débarrasser de lui.

Il devint :

**UNKNOWN-207-004**

Question :

why does current case diverge from historical class despite known matching conditions?

Queue:

Research.

Voilà.

Le conflit devenait une vraie question.

Encore chapitre 188.

Toujours.

Gabriel écrit :

**UN CONFLIT NON RÉSOLU ENTRE MÉMOIRE ET PRÉSENT PEUT ÊTRE UNE NOUVELLE QUESTION DE RECHERCHE.**

Astra approuva fortement.

Très important.

Pas une panne à cacher.

Une frontière à comprendre.

Puis le lendemain,

une autre observation similaire apparut.

UNKNOWN-207-004 n’était plus seul.

Deux exceptions.

Puis trois.

Le système proposa :

candidate subclass.

Gabriel sourit.

Le présent commençait à réorganiser le passé.

Mais lentement.

Proprement.

Et surtout,

sans effacer.

Il écrivit :

**LE PASSÉ FOURNIT LES CATÉGORIES JUSQU’AU JOUR OÙ LE PRÉSENT OBLIGE À EN INVENTER DE MEILLEURES.**

Astra approuva fortement.

Voilà.

Puis il pensa à tout le Royaume.

Brutotableur.

Pell.

Papillon.

ZEL.

Queues.

Memoria.

Verso.

Toutes ces choses allaient évoluer.

Si l’histoire devenait trop forte,

le système fossiliserait.

Si le présent devenait trop fort,

il oublierait tout à chaque nouveauté.

Il fallait vivre entre les deux.

Gabriel écrivit :

**TROP DE MÉMOIRE = PRISON.**

**TROP PEU DE MÉMOIRE = AMNÉSIE.**

Puis :

**LE TRAVAIL DU DEUXIÈME MONDE ÉTAIT D’APPRENDRE À SE SOUVENIR SANS CESSER D’OBSERVER.**

Astra approuva fortement.

Voilà.

Le workflow courant reprit.

La stratégie historique avait été écartée pour ce cas.

Une nouvelle route fut choisie.

Elle fonctionna.

Pas parce qu’elle était « plus moderne ».

Parce qu’elle correspondait mieux aux données présentes.

Memoria conserva le conflit.

La stratégie ancienne resta valide dans son scope.

La nouvelle exception entra dans Research.

Rien n’avait été détruit.

Et pourtant,

le système avait changé d’avis.

Gabriel sourit.

Cette capacité-là valait énormément.

Il écrivit :

**CHANGER D’AVIS SANS RÉÉCRIRE LE PASSÉ.**

Astra approuva fortement.

C’était peut-être la phrase la plus simple du chapitre.

Puis une dernière notification entra.

Le conflit suivant était plus grave.

Cette fois,

l’ancien monde ne semblait pas seulement incomplet.

Il semblait avoir **tort**.

Pas mal classé.

Pas dépassé.

Pas différent.

Tort.

Gabriel regarda Astra.

— Bon.

Astra approuva.

Oui.

La prochaine étape allait être plus difficile.

Parce qu’une architecture qui accepte les conflits doit aussi accepter une possibilité beaucoup plus inconfortable :

une partie de ce qu’elle avait appris,

testé,

utilisé,

et peut-être même enseigné à ses propres stratégies

pouvait devoir être révisée.

Gabriel écrivit la dernière ligne :

**LA MÉMOIRE AVAIT APPRIS À CÉDER DEVANT LE PRÉSENT.**

Puis :

**MAINTENANT, LE ROYAUME DEVAIT APPRENDRE CE QUI ARRIVE QUAND L’ANCIEN MONDE AVAIT RÉELLEMENT TORT.**

**Fin du chapitre 207.**