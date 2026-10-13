# Chapitre 205 — Le premier workflow qui change en cours de route

Le workflow était bon.

C’était justement pour ça que le problème était intéressant.

Il n’avait pas été mal construit.

Il ne contenait pas de porte oubliée.

Il ne dépendait pas d’un mauvais statut.

Il n’avait pas violé une policy.

Il avait été composé proprement.

Puis le monde avait changé.

Gabriel regarda l’écran.

Une Fourmi avançait dans un trajet construit par Antmux.

Le workflow disait :

1. retrouver une trace historique;
2. vérifier l’intégrité;
3. comparer la version;
4. exécuter un contre-test;
5. décider si la trace restait réutilisable.

Simple.

Propre.

Borné.

Mais entre les étapes 3 et 4,

quelque chose entra.

Une autre Fourmi,

dans une autre mission,

venait de découvrir qu’une dépendance partagée avait changé de comportement.

Pas cassé.

Pas disparu.

Mais changé.

Et ce changement touchait potentiellement le contre-test qui allait être exécuté.

Gabriel regarda Astra.

— Là, notre workflow est encore bon?

Astra répondit :

— Il était bon au moment où il a été composé.

Gabriel sourit.

Voilà.

Le chapitre venait d’apparaître.

Il écrivit :

**UN WORKFLOW PEUT ÊTRE CORRECT À T0 ET DEVENIR INADAPTÉ À T1 SANS AVOIR ÉTÉ MAL CONÇU.**

Astra approuva fortement.

Très important.

Le deuxième monde avait appris à composer des trajets.

Maintenant,

il devait apprendre à les modifier pendant qu’ils étaient encore en train d’exister.

Pas tout recommencer.

Pas continuer aveuglément.

Changer.

Mais proprement.

Ils créèrent :

### WORKFLOW-205-001

Status initial:

**ACTIVE**

Current step:

3/5 completed.

New event:

dependency behavior changed.

Potential impact:

step 4 assumptions may no longer hold.

Antmux devait répondre.

Pas automatiquement :

abort.

Pas automatiquement :

continue.

D’abord :

**impact analysis.**

Gabriel écrivit :

### WORKFLOW CHANGE TRIGGER

Un workflow actif doit être réévalué si un nouvel événement peut modifier :

- une précondition;
- une dépendance;
- un coût;
- une autorité;
- une stratégie;
- une preuve requise;
- une route disponible;
- une condition d’arrêt.

Astra approuva fortement.

Très propre.

Et seulement si ça peut changer le workflow.

Pas pour chaque nouveauté du Royaume.

Sinon replanification permanente.

Gabriel écrivit :

**TOUTE NOUVELLE INFORMATION N’EST PAS UNE RAISON DE RECOMPOSER LE TRAJET.**

Astra approuva.

Très important.

Dans le cas 205,

oui.

La dépendance touchait directement l’étape suivante.

Donc Antmux marqua :

**WORKFLOW_REPLAN_REQUIRED**

Gabriel se pencha.

Puis une question essentielle.

Que fait-on de ce qui est déjà fait?

Étapes 1 à 3.

Faut-il les jeter?

Pas nécessairement.

Voilà.

Ils écrivirent :

### WORKFLOW STATE PRESERVATION

Lors d’un changement de workflow, classer chaque résultat déjà produit :

**STILL_VALID**

**NEEDS_RECHECK**

**INVALIDATED**

**UNKNOWN**

Gabriel sourit.

Très important.

Le système devait préserver autant que possible le travail valide.

Pas repartir de zéro pour se donner l’impression d’être propre.

Il écrit :

**CHANGER DE WORKFLOW NE SIGNIFIE PAS EFFACER L’HISTOIRE DU WORKFLOW.**

Astra approuva fortement.

Voilà.

Étape 1 :

trace retrouvée.

Toujours valide.

Étape 2 :

intégrité.

Toujours valide.

Étape 3 :

version comparison.

Partiellement valide,

mais la dépendance nouvelle ajoute une dimension.

Donc :

`NEEDS_RECHECK_PARTIAL`

Très propre.

Le système pouvait donc reprendre à un point précis.

Pas au début.

Encore la continuité.

Gabriel écrivit :

**UN BON REPLAN COMMENCE PAR DEMANDER : QU’EST-CE QUI RESTE VRAI?**

Astra approuva fortement.

Magnifique.

Puis Antmux recomposa.

Ancien segment :

3 → 4 → 5.

Nouveau :

3b — dependency behavior check.

4b — countertest adapted to new behavior.

5 — reuse decision.

Gabriel regarda.

Le workflow avait changé.

Mais seulement où nécessaire.

Il écrivit :

**REPLAN LOCAL > REPLAN TOTAL QUAND LE CHANGEMENT EST LOCAL.**

Astra approuva fortement.

Très important.

Le système devait minimiser la zone de recomposition.

Pourquoi?

Pour réduire :

coût.

risque.

perte de contexte.

et nouvelles erreurs.

Ils créèrent :

### REPLAN SCOPE

**LOCAL**

Une sous-branche.

**PARTIAL**

Plusieurs étapes futures.

**FULL**

Objectif ou structure fondamentale changé.

Gabriel approuva.

Très bon.

Dans le cas 205 :

LOCAL.

Puis nouvelle question.

Qu’est-ce qui arrive si le changement rend le workflow impossible?

Exemple :

une action nécessaire n’existe plus.

Capability gone.

Alors :

**PAUSE + ESCALATE**

Pas inventer.

Ils écrivirent :

**UN WORKFLOW DYNAMIQUE PEUT CHANGER DE ROUTE; IL NE PEUT PAS INVENTER UNE CAPACITÉ QUI N’EXISTE PAS.**

Astra approuva fortement.

Très important.

Puis un cas différent.

Le workflow est en cours.

Une nouvelle stratégie historique devient disponible.

Elle suggère une route moins chère.

Doit-on changer automatiquement?

Pas forcément.

Parce que le coût de bascule compte.

Gabriel sourit.

Chapitre 197.

Encore.

Ils écrivirent :

### SWITCH DECISION

Changer de workflow si :

**expected future gain > switch cost**

Pas forcément calcul numérique exact.

Mais dimensions explicites.

Très important.

Un workflow presque terminé ne doit pas être remplacé juste parce qu’un meilleur workflow théorique apparaît.

Le futur compte.

Pas le passé.

Mais le coût restant est réel.

Gabriel écrit :

**UN NOUVEAU CHEMIN MEILLEUR EN THÉORIE PEUT ARRIVER TROP TARD POUR ÊTRE LE MEILLEUR CHOIX EN PRATIQUE.**

Astra approuva fortement.

Voilà.

Puis un autre cas.

Une route devient moins chère en cours d’exécution.

Par exemple,

un résultat externe devient disponible.

Le workflow peut sauter une étape.

Très bien.

Mais encore :

revalidate dependencies.

Il écrit :

**UN WORKFLOW PEUT RACCOURCIR EN COURS DE ROUTE SI LA FONCTION DE L’ÉTAPE SUPPRIMÉE EST DÉSORMAIS SATISFAITE AILLEURS.**

Astra approuva fortement.

Chapitre 196.

Encore.

Réutiliser une porte validée.

Pas la supprimer.

Très important.

Puis un cas plus difficile.

Le workflow active une écriture locale.

Puis il change.

Que faire de l’état déjà modifié?

Compensation.

Chapitre 203.

Ils testèrent.

Action A modifie un cache local.

Action B devait utiliser le cache.

New event rend B inutile.

Le cache A n’est plus nécessaire.

Peut-on le garder?

Peut-être.

Mais s’il change un comportement futur,

danger.

Donc action A avait déclaré une compensation.

`REVERT_CACHE_OVERRIDE`

Le workflow la déclencha.

Gabriel sourit.

Voilà.

Il écrit :

**UN WORKFLOW QUI CHANGE APRÈS AVOIR MODIFIÉ L’ÉTAT DOIT DÉCIDER SI CET ÉTAT RESTE LÉGITIME.**

Astra approuva fortement.

Très important.

Puis un autre cas.

Une action publique a déjà été faite.

Impossible de rollback complètement.

Le workflow change ensuite.

Alors il faut correction.

Pas prétendre que rien n’est arrivé.

Gabriel écrit :

**IRRÉVERSIBLE CHANGE LE TYPE DE REPLANIFICATION.**

Astra approuva.

Très important.

On passe de :

rollback

à :

amend / correct / supersede.

Encore append-only.

Puis ils introduisirent :

### REPLAN EFFECT HANDLING

**NO_SIDE_EFFECT**

just recompose.

**REVERSIBLE_EFFECT**

rollback or preserve explicitly.

**CANONICAL_EFFECT**

versioned correction.

**PUBLIC_EFFECT**

public amendment / correction trail.

Gabriel approuva.

Très propre.

Puis une autre question.

Est-ce que l’objectif lui-même peut changer en cours de workflow?

Oui.

Mais c’est plus sérieux.

Par exemple :

on découvre que le claim initial est trop large.

Question 204.

L’objectif devient :

valider un scope plus petit.

Le workflow doit alors être rebasé.

Gabriel écrit :

**CHANGER L’OBJECTIF N’EST PAS LE MÊME GESTE QUE CHANGER LE CHEMIN VERS L’OBJECTIF.**

Astra approuva fortement.

Très important.

Il faut versionner l’objectif.

`OBJECTIVE-205-v2`

Puis vérifier chaque étape déjà exécutée :

reste-t-elle pertinente?

Voilà.

Un objectif plus petit peut rendre certaines étapes inutiles.

Un objectif plus grand peut exiger de nouvelles.

Très propre.

Puis un autre danger.

Le workflow pourrait modifier son objectif juste pour éviter un échec.

Très mauvais.

Ils créèrent :

### OBJECTIVE DRIFT GUARD

Si objectif change après résultat défavorable :

- reason required;
- old objective preserved;
- status of old objective recorded;
- new objective gets new version;
- cannot retroactively count old failure as success.

Gabriel sourit.

Excellent.

Il écrit :

**UN WORKFLOW NE DOIT PAS GAGNER EN CHANGEANT LA QUESTION APRÈS AVOIR PERDU.**

Astra approuva fortement.

Magnifique.

Très important.

Puis ils testèrent.

Objectif :

valider relation générale.

Résultat casse généralité.

Workflow propose :

valider relation dans sous-scope.

Acceptable.

Mais statut :

original objective failed or unsupported.

New objective created.

Pas :

success.

Très propre.

Puis un autre type de changement.

Authority changes.

Supposons Gabriel délègue temporairement L2.

Le workflow peut continuer plus loin.

Ou retire une permission.

Le workflow doit s’arrêter avant la prochaine action concernée.

Gabriel écrit :

**UNE AUTORITÉ MODIFIÉE EN COURS DE ROUTE DOIT PRENDRE EFFET AVANT LA PROCHAINE ACTION QUI EN DÉPEND.**

Astra approuva fortement.

Très important.

Pas après.

Puis policies.

Une policy nouvelle arrive.

Elle rend une action interdite.

Même chose.

Replan.

Mais ce qui est déjà fait reste historique.

Pas automatiquement invalidé scientifiquement.

Il faut distinguer :

policy invalidity

et result invalidity.

Très important.

Gabriel écrit :

**UNE ACTION DEVENUE INTERDITE PLUS TARD N’EST PAS AUTOMATIQUEMENT UNE PREUVE QUE SON RÉSULTAT PASSÉ ÉTAIT FAUX.**

Astra approuva fortement.

Excellent.

Historique.

Toujours.

Puis un cas où une nouvelle preuve invalide directement un résultat passé.

Là,

oui.

Different.

Le workflow doit propager.

Chapitre 202.

Encore.

Ils créèrent :

### CHANGE SOURCE

**ENVIRONMENT**

**EVIDENCE**

**POLICY**

**AUTHORITY**

**COST**

**CAPABILITY**

**OBJECTIVE**

**FAILURE**

Chaque source produit des effets différents.

Très propre.

Puis Gabriel demanda :

— Est-ce qu’on peut mesurer combien un workflow change?

Oui.

Ils inventèrent :

### WORKFLOW DELTA

Nombre d’étapes :

added.

removed.

reordered.

revalidated.

invalidated.

authority gates changed.

Gabriel sourit.

Pas besoin d’un score unique.

Mais un diff.

Très utile.

Ancien :

A1 A2 A3 A4 A5

Nouveau :

A1 A2 A3b A4b A5

Diff clair.

Puis version.

### WORKFLOW VERSION

`WF-205-001 v1`

→ `v2`

Le journal conserve les deux.

Très important.

Il écrit :

**UN WORKFLOW QUI CHANGE DOIT AVOIR UNE HISTOIRE DE SES PROPRES CHANGEMENTS.**

Astra approuva fortement.

Voilà.

Sinon impossible de comprendre pourquoi le trajet final diffère du plan initial.

Puis ils créèrent :

### WORKFLOW CHANGE EVENT

**workflow_id**

**from_version**

**to_version**

**trigger**

**affected_steps**

**preserved_results**

**invalidated_results**

**new_steps**

**removed_steps**

**authority**

**reason**

Très propre.

Puis BrutoBac.

Comment afficher?

Ancienne route en pointillé.

Nouvelle route en clair.

Le point de bifurcation marqué :

**REPLAN EVENT**

Cliquer :

why changed.

Gabriel sourit.

Voilà.

La carte devenait une histoire dynamique.

Pas juste l’état actuel.

Il écrit :

**UNE BONNE VISUALISATION DE REPLANIFICATION DOIT MONTRER D’OÙ LE NOUVEAU CHEMIN EST VENU.**

Astra approuva fortement.

Très important.

Sinon on voit seulement une route et on croit qu’elle avait toujours été prévue.

Faux.

Puis un autre problème.

Trop de replans.

Workflow thrashing.

A puis B.

Puis A.

Puis C.

Puis A.

Gabriel grimaca.

Il fallait détecter.

### REPLAN THRASH

Possible causes:

- unstable metrics;
- contradictory signals;
- over-sensitive trigger;
- no hysteresis;
- bad strategy;
- environment unstable.

Gabriel approuva.

Très important.

Un workflow qui change tout le temps peut coûter plus que continuer.

Ils ajoutèrent :

### STABILITY WINDOW

Certains changements non critiques doivent persister avant de déclencher replan.

Mais pas les critical invalidations.

Très propre.

Gabriel écrit :

**LA RÉACTIVITÉ SANS STABILITÉ PEUT DEVENIR DE L’INDÉCISION AUTOMATISÉE.**

Astra approuva fortement.

Magnifique.

Puis un cas important.

Une nouvelle donnée semble importante,

mais disparaît une seconde plus tard.

Sans window,

replan inutile.

Avec :

attendre confirmation.

Mais si sécurité/autorité?

Immediate.

Toujours classes.

Très bon.

Puis ils abordèrent la concurrence.

Deux événements arrivent en même temps.

E1 :

dependency changed.

E2 :

new validation result.

Le workflow pourrait être replanné deux fois.

Mieux :

coalesce.

Gabriel écrit :

**DEUX CHANGEMENTS QUI ARRIVENT ENSEMBLE DOIVENT SI POSSIBLE ÊTRE ÉVALUÉS DANS LE MÊME REPLAN.**

Astra approuva.

Très important.

Sinon oscillation.

Ils créèrent :

### REPLAN BATCH

Collect related triggers within small window.

Build one consistent new version.

Exceptions:

critical stop triggers.

Très propre.

Puis un autre cas.

Une Fourmi travaille depuis longtemps.

Le workflow change.

Elle peut continuer avec ancienne version par erreur.

Il faut workflow version pinning.

Task knows its workflow_version.

On replan,

active tasks receive:

continue / stop / migrate.

Gabriel écrit :

**UNE FOURMI DOIT SAVOIR SOUS QUELLE VERSION DU TRAJET ELLE TRAVAILLE.**

Astra approuva fortement.

Très important.

Pas de tâches orphelines.

Puis migration.

Si step compatible,

migrate.

Sinon finish current safe point,

then switch.

Voilà.

Ils créèrent :

### TASK MIGRATION POLICY

**IMMEDIATE**

Safe and stateless.

**CHECKPOINT**

Finish current atomic step.

**COMPENSATE_THEN_SWITCH**

If side effect.

**DO_NOT_MIGRATE**

Complete old branch if still valid.

Gabriel sourit.

Très propre.

Puis un cas où l’ancien workflow reste valide.

Nouveau workflow meilleur.

Peut laisser les tâches déjà avancées finir old path.

Et utiliser new workflow pour futures tâches.

Très important.

Il écrit :

**UNE NOUVELLE VERSION DU WORKFLOW N’OBLIGE PAS TOUJOURS À MIGRER TOUT CE QUI EST DÉJÀ EN VOL.**

Astra approuva fortement.

Comme logiciel.

Encore.

Puis ils mesurèrent un trial.

### WORKFLOW CHANGE TRIAL 205-A

Initial workflow:

5 steps.

Trigger after step 3:

dependency change.

Replan:

2 future steps replaced by 2 adapted steps.

Preserved:

steps 1, 2.

Partially rechecked:

step 3.

Invalidated:

0 completed outputs fully discarded.

Human intervention:

0.

Authority:

remained L1.

Outcome:

reuse decision completed under updated dependency state.

Gabriel sourit.

Très bon.

Petit test.

Pas preuve générale.

Ils marquèrent :

**PASS IN TESTED CASE**

Not established:

optimal replan.

general concurrency safety.

universal rollback correctness.

Astra approuva.

Toujours.

Puis un deuxième trial.

Trigger :

authority reduction.

Workflow paused before canonical write.

Human reviewed.

No violation.

Très bon.

Troisième :

new evidence invalidates upstream assumption.

Replan full.

Several outputs marked invalidated.

Very good.

Le moteur avait trois comportements différents selon trigger.

Gabriel sourit.

Ça commençait à tenir.

Puis une erreur.

Un replan local conservait un output qui dépendait indirectement d’une étape invalidée.

Dependency graph incomplet.

Danger.

Gabriel se redressa.

Voilà la vraie difficulté.

Il écrit :

**UN REPLAN N’EST SÛR QUE SI LES DÉPENDANCES DES RÉSULTATS SONT ASSEZ COMPLÈTES POUR SAVOIR CE QUI DOIT ÊTRE INVALIDÉ.**

Astra approuva fortement.

Très important.

Si provenance manque,

il faut être plus conservateur.

Ils ajoutèrent :

### INVALIDATION PROPAGATION

If dependency chain known:

invalidate transitively.

If unknown:

mark `REVIEW_REQUIRED`.

Pas supposer valide.

Gabriel approuva.

Très propre.

Puis un autre point.

Dependency types encore.

Hard.

Soft.

Historical.

Illustrative.

Only hard dependencies propagate automatic invalidation.

Très important.

Sinon tout s’écroule.

Gabriel sourit.

Les leçons de 202 revenaient.

Puis une nouvelle notion :

**checkpoint consistency.**

Quand workflow change,

snapshot de l’état.

Pour pouvoir expliquer :

avant.

après.

Très utile.

Ils créèrent :

### REPLAN CHECKPOINT

**workflow_state_before**

**trigger**

**state_after**

**preserved**

**changed**

**authority**

**reason**

Gabriel approuva.

Excellent.

Puis question performance.

Combien de replanifications coûtent trop cher?

À mesurer.

Pas de loi.

Mais on peut suivre :

**replans_per_workflow**

**average steps preserved**

**average steps discarded**

**replan latency**

**replan-induced errors**

Très important.

Le système devait mesurer sa capacité à changer,

pas seulement sa capacité à planifier.

Gabriel écrit :

**UNE MACHINE ADAPTATIVE DOIT MESURER LE COÛT DE SON ADAPTATION.**

Astra approuva fortement.

Voilà.

Sinon « adaptatif » devient un mot magique.

Puis un cas humain.

Gabriel voit le workflow changer.

Il ne comprend pas pourquoi.

Mauvais.

Donc every replan must produce a concise explanation.

Example:

> Étape 4 remplacée parce que la dépendance D est passée de v1 à v2 après l’étape 3. Les résultats 1 et 2 restent valides. Le résultat 3 doit être complété par un nouveau contrôle.

Très propre.

Il écrit :

**UN WORKFLOW QUI CHANGE SANS EXPLICATION DEVIENT PLUS DIFFICILE À FAIRE CONFIANCE QU’UN WORKFLOW FIXE.**

Astra approuva fortement.

Très important.

Puis un autre danger.

Le système explique après coup une raison qui n’a pas réellement déclenché le changement.

Non.

Explanation must be generated from change event.

Pas narration inventée.

Gabriel écrit :

**L’EXPLICATION DU REPLAN DOIT VENIR DE LA TRACE DU REPLAN, PAS D’UNE HISTOIRE RECONSTRUITE APRÈS.**

Astra approuva fortement.

Magnifique.

Très important.

Puis il pensa à une analogie.

GPS.

Route barrée.

Nouveau trajet.

Mais la comparaison s’arrêtait vite.

Parce qu’ici,

le trajet transportait aussi :

preuve.

autorité.

statut.

historique.

Une déviation pouvait modifier ce qu’on a le droit de conclure.

Beaucoup plus sérieux.

Gabriel écrit :

**REPLANIFIER UN WORKFLOW SCIENTIFIQUE OU OPÉRATIONNEL NE CONSISTE PAS SEULEMENT À TROUVER UNE AUTRE ROUTE; IL FAUT PRÉSERVER LES GARANTIES.**

Astra approuva fortement.

Voilà.

Puis un cas scientifique précis.

Un protocole prévoyait :

screening → independent check → validation.

Independent checker indisponible.

Peut-on remplacer par une deuxième exécution du même code?

Non.

Même format de sortie,

garantie différente.

Chapitre 203.

Semantic type mismatch.

Workflow peut :

pause.

ou continuer avec claim plus faible.

Voilà.

Gabriel écrit :

**UN WORKFLOW PEUT CHANGER DE CHEMIN EN RÉDUISANT SON OBJECTIF, MAIS IL NE PEUT PAS FAIRE SEMBLANT QU’UNE GARANTIE MANQUANTE A ÉTÉ REMPLACÉE.**

Astra approuva fortement.

Très important.

Option :

produce `SCREENED_ONLY`.

Pas `VALIDATED`.

Excellent.

Puis un cas encore plus important.

On change workflow parce qu’un résultat est décevant.

Danger de p-hacking conceptuel.

Il faut predeclared replan rules quand possible.

Mais l’exploration a besoin de flexibilité.

Donc distinction :

### CONFIRMATORY WORKFLOW

Stricter change rules.

Any change affecting inference must be recorded and may create new protocol version.

### EXPLORATORY WORKFLOW

More flexible.

Still traced.

Gabriel sourit.

Très important.

Il écrit :

**LA FLEXIBILITÉ ACCEPTABLE DÉPEND DU TYPE DE QUESTION QU’ON ESSAIE DE RÉSOUDRE.**

Astra approuva fortement.

Voilà.

Une exploration peut suivre une piste nouvelle.

Une validation confirmatoire doit être plus stricte.

Sinon biais.

Très important.

Puis ils ajoutèrent :

**mode = exploratory / confirmatory / operational**

Chaque mode a replan policy.

Très propre.

Puis BrutoBac.

Une Fourmi avance.

Le sol devant elle change.

Ancienne route devient gris pointillé.

Nouvelle branche s’ouvre.

La Fourmi ne téléporte pas.

Elle termine son segment atomique.

Puis bifurque.

Gabriel sourit.

L’image était parfaite.

Il écrit :

**UNE FOURMI N’A PAS BESOIN DE RECOMMENCER SON VOYAGE PARCE QUE LE PROCHAIN PONT A CHANGÉ.**

Astra approuva fortement.

Très beau.

Puis le workflow 205 se termina.

Résultat historique finalement non réutilisable tel quel,

mais revalidation locale suffisante.

Pas besoin de full rerun.

Voilà.

Le workflow original aurait soit :

réutilisé trop vite,

soit recalculé trop large.

Le replan avait trouvé le milieu.

Gabriel regarda.

Cette fois,

le système avait fait quelque chose de plus que suivre un plan.

Il avait reconnu que son propre plan n’était plus adapté.

Puis il l’avait changé

sans oublier pourquoi il l’avait construit.

Il écrivit :

**UN PLAN N’EST PAS INTELLIGENT PARCE QU’IL PRÉVOIT TOUT.**

Puis :

**IL DEVIENT ROBUSTE QUAND IL PEUT CHANGER SANS PERDRE LA TRACE DE CE QU’IL ÉTAIT.**

Astra approuva fortement.

Voilà le cœur du chapitre.

Puis un événement étrange apparut.

Le workflow suivant n’avait pas changé à cause d’une erreur.

Ni d’une policy.

Ni d’un coût.

Il avait changé parce qu’un autre organe du Royaume possédait une information que Antmux n’avait pas.

Verso savait quelque chose.

Antmux,

non.

Pas parce qu’Antmux était défectueux.

Parce que les deux organes n’avaient pas le même rôle.

Gabriel se redressa.

Voilà.

Le prochain problème n’était plus :

comment changer le workflow?

C’était :

**comment reconnaître qu’un autre organe possède un contexte que le planificateur n’a pas?**

Il regarda Astra.

— Ça, c’est le prochain.

Astra approuva.

Oui.

Parce qu’un bon routeur peut encore faire un mauvais choix

s’il ne sait pas qu’une autre partie du Royaume détient une information décisive.

Le workflow 205 venait d’apprendre à changer.

Maintenant,

il allait falloir apprendre

**qui savait quoi**.

**Fin du chapitre 205.**