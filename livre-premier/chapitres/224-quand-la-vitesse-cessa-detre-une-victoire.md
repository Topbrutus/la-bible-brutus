# Chapitre 224 — Quand la vitesse cessa d’être une victoire

Au début,

tout le monde avait aimé le nouveau chemin.

Il était rapide.

Très rapide.

Les tâches traversaient Antmux avec moins de handoffs.

Les réponses arrivaient plus tôt.

Les files semblaient respirer.

Le tableau de bord affichait une amélioration nette sur la latence.

Gabriel regarda les courbes.

— Ça, c’est beau.

Astra approuva.

Oui.

Sur cet axe-là,

c’était réellement mieux.

Puis une autre courbe commença à bouger.

Pas assez pour inquiéter au premier regard.

Puis encore.

Un peu.

Puis encore.

Le système allait plus vite.

Mais certains dossiers revenaient.

Certains résultats demandaient une correction.

Certains contextes importants étaient récupérés trop tard.

Pas une catastrophe.

Pas une panne.

Quelque chose de plus insidieux.

Gabriel fronça les sourcils.

— On est-tu juste en train de faire les erreurs plus vite?

Astra resta silencieuse une seconde.

Puis approuva.

La question était exactement la bonne.

Gabriel écrivit :

**LA VITESSE N’EST UNE AMÉLIORATION QUE SI ELLE NE DÉGRADE PAS CE QUE LE WORKFLOW ESSAIE DE PROTÉGER.**

Astra approuva fortement.

Voilà le chapitre.

Jusqu’ici,

la vitesse avait souvent été considérée comme une victoire évidente.

Moins de latence.

Moins d’attente.

Moins de temps CPU.

Plus de tâches terminées.

Mais désormais,

le Royaume disposait de suffisamment de métriques pour découvrir quelque chose de moins confortable :

**une méthode pouvait devenir plus rapide et moins bonne.**

Gabriel écrivit :

### SPEED PROFILE

**latency**

**throughput**

**time-to-first-result**

**time-to-validated-result**

**time-to-correction**

Astra approuva fortement.

Très important.

Parce que :

time-to-first-result

n’était pas forcément

time-to-usable-result.

Et encore moins

time-to-trustworthy-result.

Gabriel écrivit :

**LA PREMIÈRE RÉPONSE N’EST PAS TOUJOURS LA PREMIÈRE RÉPONSE UTILISABLE.**

Astra approuva fortement.

Puis un cas concret.

### METHOD-224-A

Fast path :

cheap index.

direct computation.

minimal context.

defer deeper provenance until result looks interesting.

Très rapide.

Sur tâches simples :

excellent.

Mais sur certaines tâches de recherche,

la première réponse arrivait rapidement,

puis le système découvrait :

ancienne exception.

scope historique.

claim voisin déjà réfuté.

version plus récente.

Résultat :

rework.

Gabriel regarda.

Le premier calcul n’était pas nécessairement faux.

Mais il avait été produit avant que le contexte utile soit disponible.

Le workflow avait gagné 30 secondes au début

et perdu 12 minutes à la fin.

Il écrivit :

**LA VITESSE LOCALE PEUT CRÉER DE LA LENTEUR GLOBALE.**

Astra approuva fortement.

Très important.

Ils comparèrent deux mesures.

### TIME TO FIRST OUTPUT

Fast path gagne.

### TIME TO FINAL USABLE OUTPUT

Différence beaucoup plus faible.

Parfois old path gagne.

Voilà.

Gabriel sourit.

La mauvaise métrique aurait déclaré victoire trop tôt.

Puis une troisième mesure :

### TIME TO STABLE OUTPUT

Combien de temps avant que le résultat cesse d’être corrigé ou renvoyé?

Encore plus intéressant.

Dans certaines classes,

la méthode rapide produisait rapidement une réponse instable.

La méthode plus lente produisait directement quelque chose de plus durable.

Gabriel écrivit :

**UNE RÉPONSE RAPIDE QUI DOIT ÊTRE REFAITE DEUX FOIS PEUT ÊTRE PLUS LENTE QU’UNE RÉPONSE PLUS LENTE MAIS STABLE.**

Astra approuva fortement.

Voilà.

Puis ils regardèrent le throughput.

La méthode rapide terminait davantage de tâches par heure.

Impressionnant.

Mais plusieurs tâches terminées étaient ensuite rouvertes.

Donc :

**gross throughput**

et

**net useful throughput**

devaient être distingués.

Ils créèrent :

### THROUGHPUT TYPES

**RAW THROUGHPUT**

tasks marked complete / time.

**STABLE THROUGHPUT**

tasks remaining resolved after review window.

**VALIDATED THROUGHPUT**

tasks reaching required evidence gate / time.

Gabriel approuva.

Très propre.

Il écrit :

**TERMINER PLUS DE TÂCHES N’EST PAS UNE VICTOIRE SI ON AUGMENTE AUSSI LE NOMBRE DE TÂCHES QU’IL FAUT REFAIRE.**

Astra approuva fortement.

Très important.

Puis ils calculèrent dans un petit panel.

Old method :

moins de tâches brutes.

moins de reopen.

Fast method :

plus de tâches brutes.

plus de reopen.

Après correction,

le gain réel était modeste.

Pas nul.

Mais modeste.

Gabriel sourit.

Encore une fois,

les données ne racontaient pas une histoire spectaculaire.

Elles corrigeaient une impression.

Il écrivit :

**LES BONNES MÉTRIQUES NE SONT PAS OBLIGÉES DE PRODUIRE UNE HISTOIRE DRAMATIQUE. ELLES DOIVENT PRODUIRE UNE HISTOIRE JUSTE.**

Astra approuva fortement.

Puis un autre problème.

Certaines tâches n’avaient aucun besoin de profondeur.

Calcul simple.

Reformatage.

Lookup exact.

Là,

la rapidité était une vraie victoire.

Il ne fallait pas tomber dans l’extrême inverse.

Gabriel écrivit :

**DÉCOUVRIR QUE LA VITESSE PEUT ÊTRE TROMPEUSE NE SIGNIFIE PAS QUE LA LENTEUR DEVIENT UNE VERTU.**

Astra approuva fortement.

Très important.

Le bon objectif n’était pas :

ralentir.

C’était :

**mettre le bon niveau de contrôle au bon endroit.**

Ils créèrent :

### SPEED SAFETY PROFILE

For each task class:

**minimum required checks**

**allowed shortcuts**

**maximum acceptable latency**

**rework tolerance**

**authority level**

**validation requirement**

Excellent.

Puis un cas.

Lookup d’un hash exact.

Fast path.

Très bien.

Un claim de publication.

Fast path sans provenance.

Non.

Un scan exploratoire sandbox.

Rapide.

Très bien.

Un changement de policy.

Plus lent.

Normal.

Gabriel écrit :

**LA VITESSE DOIT ÊTRE RELATIVE À LA CONSÉQUENCE.**

Astra approuva fortement.

Voilà.

Puis une courbe étrange apparut.

Dans certains workflows,

plus ils allaient vite,

plus les décisions humaines arrivaient tard.

Pourquoi?

Parce que le système accumulait davantage de travail avant de demander un gate.

Quand Gabriel intervenait,

il devait examiner un plus gros paquet.

Le throughput machine avait augmenté.

Le coût humain avait aussi augmenté.

Gabriel soupira.

— On a juste déplacé la file dans ma tête.

Astra approuva.

Exact.

Il écrivit :

**UNE OPTIMISATION QUI RETIRE UNE FILE À LA MACHINE ET LA TRANSFÈRE À L’HUMAIN N’A PAS FORCÉMENT RÉDUIT LE COÛT GLOBAL.**

Astra approuva fortement.

Très important.

Donc mesure :

### HUMAN QUEUE DEPTH

Combien de décisions attendent l’opérateur?

### CONTEXT PACKAGE SIZE

Combien de contexte moyen à examiner?

Très utile.

Puis le Royaume constata :

la méthode rapide produisait des lots plus gros.

Gabriel préférait parfois des paquets plus petits,

plus tôt,

sur les décisions importantes.

Donc latence humaine.

Encore un axe.

Puis un autre phénomène.

Le système avait réduit les vérifications intermédiaires.

Résultat :

plus de travail accompli avant détection d’une mauvaise hypothèse.

Une erreur détectée plus tard coûte plus cher.

Chapitre 222.

Gabriel écrivit :

**ACCÉLÉRER ENTRE DEUX CONTRÔLES AUGMENTE PARFOIS LA DISTANCE QU’UNE ERREUR PEUT PARCOURIR AVANT D’ÊTRE ARRÊTÉE.**

Astra approuva fortement.

Excellent.

C’était exactement ce que le tableau de bord des erreurs montrait.

Même taux d’erreur initial.

Plus grand blast radius.

Très important.

Donc la fréquence des checkpoints pouvait dépendre de :

risk.

reversibility.

cost of propagation.

Pas seulement throughput.

Puis un exemple.

1000 transformations.

Old method:

validation every 100.

Fast method:

validation only at end.

If error at step 201,

old loses 99 steps.

fast loses 799.

Voilà.

Gabriel écrit :

**MOINS DE CHECKPOINTS PEUT ÊTRE PLUS RAPIDE QUAND TOUT VA BIEN ET BEAUCOUP PLUS CHER QUAND QUELQUE CHOSE VA MAL.**

Astra approuva fortement.

Très important.

Ils créèrent :

### CHECKPOINT ECONOMY

Checkpoint cost.

Expected rework reduction.

Risk.

Not universal interval.

Great.

Puis un autre problème.

Caches.

Cache improved speed.

But stale-context near misses increased.

Chapter 220.

The fast path got old answers quicker.

Gabriel laughed.

— Magnifique. On est capables d’aller chercher la mauvaise réponse plus vite.

Astra approuva.

Le sarcasme méritait presque une ligne dans la Bible.

Il écrivit :

**UNE RÉPONSE OBSOLÈTE LIVRÉE PLUS RAPIDEMENT N’EST PAS UNE AMÉLIORATION.**

Astra approuva fortement.

Voilà.

Donc cache speed must pair with freshness contract.

Great.

Then:

### CACHE PERFORMANCE CONTRACT

speed gain valid only if:

freshness requirement satisfied.

critical invalidation propagation works.

fallback available.

Perfect.

Then another example.

Parallelization.

Three Fourmis work at once.

Faster.

But if they duplicate same search,

throughput apparent high.

Useful work lower.

Need coordination.

Chapter 222.

Gabriel writes:

**PARALLÉLISER DU TRAVAIL DUPLIQUÉ NE TRANSFORME PAS LE GASPILLAGE EN PERFORMANCE.**

Astra approved strongly.

Excellent.

Then another.

Parallel branches can explore genuinely different hypotheses.

That's valuable.

So diversity matters.

Again.

Then a queue optimization.

Batch 50 items for efficiency.

High throughput.

But first item waits for batch.

Latency worsens.

Tradeoff.

Different modes.

Operational maybe not.

Bulk archive yes.

Good.

Gabriel writes:

**LE DÉBIT ET LA LATENCE PEUVENT TIRER DANS DES DIRECTIONS OPPOSÉES.**

Astra approuva fortement.

Very important.

Then a publication case.

Batch validations overnight.

Efficient compute.

But human wants immediate check for critical claim.

Different SLA.

Great.

Then they defined:

### SPEED METRICS BY MODE

**interactive**

time-to-useful-response.

**batch**

throughput and cost.

**validation**

time-to-stable-validated-result.

**incident**

time-to-detect and contain.

**research**

time-to-informative-result.

Gabriel smiled.

This was much more useful.

Then a research route.

Fast answer says no witness in first 1000 candidates.

Slow route explores 1e6.

Which faster?

Depends question.

If goal cheap screening,

first is good.

If claim requires broad bound,

not enough.

So speed can't ignore requested gate.

Again.

Then a dangerous habit.

People celebrate lower latency.

Easy.

Visible.

But provenance completeness is less exciting.

Gabriel writes :

**LES MÉTRIQUES FACILES À CÉLÉBRER NE SONT PAS TOUJOURS LES MÉTRIQUES LES PLUS IMPORTANTES.**

Astra approuva fortement.

Very important.

A pretty dashboard can push team toward speed.

Need balanced panel.

Then the system created:

### SPEED GUARDRAILS

A speed improvement cannot be promoted if tested cohort shows:

- increased authority violations;
- increased semantic escalation;
- unacceptable provenance degradation;
- significant increase in rework;
- unacceptable stale-context errors.

Very clean.

Then a speed improvement can still trade a little maintenance complexity for latency.

If explicit.

Good.

Then another issue.

"Significant" should not imply statistical significance unless actual stats.

Use practical threshold or predefined tolerance.

Gabriel writes:

**“SIGNIFICATIF” DOIT ÊTRE DÉFINI; SINON IL DEVIENT UN MOT QUI FAIT SEMBLANT DE MESURER.**

Astra approuva fortement.

Excellent.

Use:

operationally meaningful threshold.

Good.

Then a speed pilot.

### SPEED PILOT 224-A

Task class:

low-risk deterministic internal.

Fast path vs previous.

Observed:

time-to-first-output improved.

stable throughput improved modestly.

no observed critical guard misses.

maintenance complexity higher.

Status:

supported in tested class.

Then research task class.

Fast path:

first output much faster.

stable output not improved.

rework increased.

Status:

not promoted.

Excellent.

Same optimization,

different result.

Gabriel writes :

**UNE OPTIMISATION N’A PAS DE DROIT UNIVERSEL À CAUSE DE SON SUCCÈS LOCAL.**

Astra approuva strong.

Then a question.

Could adaptive routing choose fast or deep based on task?

Yes.

That's better.

Task profile.

Confidence.

risk.

This is exactly policy 219.

Great.

Then one subtle danger.

Classifier itself can be wrong.

If high-risk task misclassified low-risk,

fast path dangerous.

So default uncertain classification should be conservative.

Gabriel writes:

**LORSQUE LE SYSTÈME N’EST PAS SÛR QUE LE CHEMIN RAPIDE EST AUTORISÉ, L’INCERTITUDE NE DOIT PAS ÊTRE INTERPRÉTÉE COMME UNE PERMISSION D’ACCÉLÉRER.**

Astra approuva strong.

Excellent.

Then class confidence.

Maybe `task_mode = UNKNOWN` → standard path.

Good.

Then another speed dimension.

Response streaming.

Can begin showing partial result early.

Useful.

But partial must be labeled.

Don't let early partial be mistaken final.

Gabriel writes:

**AFFICHER PLUS TÔT N’EST PAS TERMINER PLUS TÔT.**

Astra approuva strong.

Nice.

This matters for UI.

Partial:

PRELIMINARY.

Final:

VALIDATED or resolved.

Great.

Then user perception.

Fast UI can feel better.

But scientific status must stay.

Good.

Then another tradeoff.

Compression.

Faster retrieval.

But maybe decompression overhead.

No need deep.

Then network.

Prefetch.

Could expose unnecessary sensitive data.

Risk.

So speed optimization must respect least privilege.

Good.

Gabriel writes:

**PRÉCHARGER PLUS POUR ALLER PLUS VITE PEUT AUGMENTER CE QUE CHAQUE MODULE VOIT SANS EN AVOIR BESOIN.**

Astra approuva strong.

Very important.

Privacy/security cost.

Then a system principle:

### FAST PATH CONTRACT

Every fast path specifies:

- eligible scope;
- skipped work;
- why skipped work is safe here;
- fallback;
- invalidation triggers;
- quality metrics;
- rollback.

Gabriel smiled.

Very strong.

No fast path without naming what it omits.

He writes:

**UN RACCOURCI DOIT DÉCLARER CE QU’IL RACCOURCIT.**

Astra approuva strong.

Excellent.

This echoes chapter 196.

Then shortcut categories.

Safe reuse.

Skipped duplicate computation.

Deferred optional context.

Not skip evidence gate.

Good.

Then a fast path that omits exact check to save time.

If claim needs exact check,

not allowed.

Again.

Then a very important example.

Pell factorization.

Candidate factor found quickly.

Could display:

candidate.

But opening gate waits rank exact.

Fast preliminary output okay.

Fast final claim not.

Gabriel writes:

**ON PEUT ACCÉLÉRER LA DÉCOUVERTE D’UN CANDIDAT SANS ACCÉLÉRER ARTIFICIELLEMENT SON STATUT.**

Astra approuva strong.

Excellent.

Likewise ZEL run.

Signal can appear quickly.

Protocol PASS only after full required checks.

Good.

Papillon.

Benchmark quick preliminary.

Public claim after proper run.

Great.

Then Brutus starts distinguishing:

**fast observation path**

and

**slow authority path**.

Interesting.

Not necessarily always slow.

But higher gates.

Gabriel writes:

**LE TEMPS NÉCESSAIRE POUR PRODUIRE UNE IDÉE ET LE TEMPS NÉCESSAIRE POUR LUI DONNER DE L’AUTORITÉ PEUVENT ÊTRE DIFFÉRENTS.**

Astra approuva strong.

Very important.

Then one could make exploration fast,

validation rigorous.

This is ideal.

The mistake is forcing validation speed into exploration or vice versa.

Then a new architecture:

### DUAL TEMPO

**FAST LANE**

reversible, low-authority, exploratory.

**DEEP LANE**

validation, canonical, public, irreversible.

With promotion gate between.

Gabriel smiles.

This could be powerful.

But don't make exact two-lane rigid if multiple modes.

Conceptual.

Then a candidate can move from fast to deep.

Great.

Then another danger.

Fast lane generates too many candidates.

Validation overloaded.

Throughput imbalance.

Need backpressure.

Gabriel writes:

**ACCÉLÉRER LA PRODUCTION EN AMONT PEUT SIMPLEment DÉPLACER LE GOULET D’ÉTRANGLEMENT EN AVAL.**

Astra approuva strongly.

Very important.

If Research makes 1000 candidates/hour and Validation handles 20,

system floods.

Need quality filter.

Great.

Then queue depth.

Backpressure.

Maybe slow producer.

This connects to future chapter 226, deliberate slowdown.

Perfect.

Then a real observation.

After fast candidate generator improvement,

Validation queue grew.

Raw throughput celebrated.

But useful throughput unchanged.

Gabriel frowned.

— Ben voilà.

The system was manufacturing waiting.

He writes:

**UNE MACHINE QUI PRODUIT PLUS VITE QUE SA CAPACITÉ À VÉRIFIER PEUT AUGMENTER LE TRAVAIL EN ATTENTE SANS AUGMENTER LA CONNAISSANCE PRODUITE.**

Astra approved strongly.

Excellent.

This is key.

Then backlog ages.

Candidates stale.

Human overload.

Storage.

So speed can have downstream carrying cost.

Great.

Then they define:

### FLOW BALANCE

production rate.

validation rate.

publication rate.

archive rate.

Queue growth.

If upstream > downstream sustainably,

backlog.

Need throttle or improve bottleneck.

Not celebrate raw throughput.

Then a manufacturing analogy.

But keep project tone.

Good.

Then a test.

Generator 2x faster.

Validation unchanged.

Queue doubles.

No gain in validated outputs.

Thus no system-level improvement.

Gabriel writes:

**LE DÉBIT DU ROYAUME EST LIMITÉ PAR LE DÉBIT DE CE QUI DOIT RENDRE LE TRAVAIL UTILISABLE, PAS PAR LE MODULE LE PLUS RAPIDE.**

Astra approuva strong.

Excellent.

Then a practical change.

Throttle candidate generation when Validation backlog exceeds threshold.

At first seems crazy:

deliberately slow.

But prevents waste.

This sets chapter 226.

Before that chapter 225: quality before throughput.

Perfect.

Then a more direct quality policy.

If backlog high,

raise admission threshold.

Only higher-value candidates enter Validation.

Others park.

This isn't deleting.

Queue.

Good.

Then check risk of missing discoveries.

Candidates preserved.

Can revisit.

Excellent.

Then a new metric:

### VALIDATED OUTPUT RATE

not raw generated candidate count.

Much more meaningful for validation pipeline.

Still not sole measure.

Great.

Then a case.

Research value may be in candidate diversity.

Even if not validated all immediately.

So keep inventory metric too.

Again.

No one metric.

Then Gabriel looked at fastest module.

It had a beautiful benchmark.

But system-level throughput had barely changed.

Because bottleneck elsewhere.

He writes:

**LA VITESSE D’UN MODULE N’EST PAS LA VITESSE DU SYSTÈME.**

Astra approuva strong.

Very important.

Then optimization should target bottleneck.

But if bottleneck is intentional gate,

don't "fix" by weakening it.

Excellent.

Gabriel writes:

**UNE PORTE DE VALIDATION PEUT ÊTRE LENTE PARCE QU’ELLE FAIT UN TRAVAIL QUE LE SYSTÈME A DÉCIDÉ DE NE PAS SACRIFIER.**

Astra approuva strong.

This leads directly to quality over throughput.

Then one more important thing.

Some speed improvements are genuine and free.

Better algorithm.

Same outputs.

Same evidence.

Less compute.

Great.

Celebrate.

No need anti-speed philosophy.

Gabriel writes:

**SI DEUX MÉTHODES PRODUISENT LE MÊME NIVEAU DE QUALITÉ, D’AUTORITÉ ET DE TRACE, LA PLUS RAPIDE PEUT ÊTRE RÉELLEMENT MEILLEURE SUR CET AXE.**

Astra approuva strong.

Excellent.

The point is not to distrust speed.

It's to stop equating it with victory.

Then a benchmark.

New implementation 2x faster, identical property tests, same outputs.

Good.

Promote after verification.

Excellent.

Then speed regression.

No issue.

Then the central doctrine:

### SPEED IS A SECONDARY OBJECTIVE UNDER QUALITY CONSTRAINTS

Gabriel looked.

Maybe too technical.

He rewrote:

**ON ACCÉLÈRE APRÈS AVOIR DÉFINI CE QU’ON REFUSE DE SACRIFIER.**

Astra approuva strong.

Voilà.

That's the chapter's heart.

Then another line:

**LA VITESSE DEVIENT UNE VICTOIRE QUAND ELLE RÉDUIT LE TEMPS SANS RÉDUIRE LA QUALITÉ REQUISE.**

Astra approuva strong.

Good.

Then dashboard changes.

No more green speed arrow alone.

When latency improves,

display nearby:

rework.

errors.

provenance.

stable throughput.

Maybe no visual specifics required.

But concept.

Great.

Then a speed improvement could show:

`FAST + SAFE IN TESTED SCOPE`.

Or:

`FAST / QUALITY REGRESSION OBSERVED`.

Excellent.

Then one trial reveals.

Fast path:

-34% latency.

+18% rework.

No authority issue.

Question:

worth?

Maybe not.

Depends class.

For low-cost rework maybe.

But likely no.

Need cost profile.

Good.

Then another:

-12% latency.

same rework.

same quality.

Good.

Promote.

Then a third:

-2% latency.

much higher complexity.

Not worth.

Great.

No fetishization of percentages.

Then another metric.

Variance.

Fast method unstable.

Sometimes instant.

Sometimes huge.

Operational might prefer predictable.

Good.

Then a real-time system may value p95.

Batch not.

Again.

Then Gabriel realizes the dashboard itself previously celebrated average FPS in visual work, but here science pipeline different. No need mention history maybe.

Then the Kingdom made its first deliberate decision **not to deploy a faster method**.

This is key.

### SPEED-CANDIDATE-224-B

Observed:

18% faster first output.

11% higher rework.

more context misses.

Decision:

**REJECT FOR VALIDATION WORKFLOW**

Keep for exploratory sandbox only.

Gabriel smiled.

That mattered.

Because it was the first time

a benchmark win

did not become a deployment win.

He writes:

**LE PREMIER “PLUS RAPIDE” QUE LE ROYAUME REFUSA FUT PEUT-ÊTRE UNE DES PREMIÈRES PREUVES QU’IL COMMENÇAIT À COMPRENDRE LA QUALITÉ.**

Astra approuva strong.

Excellent.

Then preserve candidate.

Maybe future optimization solves rework.

Not bad method globally.

Just wrong role.

Great.

Then another case.

Same fast method in BrutoBac visual preview.

No scientific authority.

Excellent.

Use it.

A method can be rejected in one workflow and perfect in another.

Again scope.

Then the data started changing how development goals were written.

Old:

"reduce validation latency 30%."

New:

"reduce validation latency without increasing avoidable returns, semantic errors, or provenance omissions."

Much better.

Gabriel writes:

**UN OBJECTIF DE PERFORMANCE DOIT DIRE CE QU’IL N’A PAS LE DROIT DE CASSER.**

Astra approuva strong.

Beautiful.

Then a further refinement.

Maybe quality can improve while speed decreases.

Yes.

If reduced rework enough.

Total useful output maybe higher.

That's next chapter.

Quality before throughput.

Then a case:

add exact precheck.

+8 sec per task.

But halves later returns.

Overall validated throughput rises.

Interesting.

Slower each first pass,

faster system outcome.

Great.

Gabriel writes:

**RALENTIR UNE ÉTAPE PEUT ACCÉLÉRER LE SYSTÈME.**

Astra approuva strong.

Excellent.

This paradox sets 226 too.

Then a philosophical moment.

People love speed because it's visible.

A response arrives.

A graph jumps.

A queue empties.

Quality often shows itself later.

In absence of corrections.

In reproducibility.

In not needing to redo.

In trustable provenance.

Gabriel writes:

**LA VITESSE SE VOIT TOUT DE SUITE. LA QUALITÉ SE RÉVÈLE SOUVENT APRÈS.**

Astra approuva strong.

Voilà.

Thus evaluation needs observation window.

Don't ship on first benchmark.

Good.

Then speed pilot requires post-run window.

Great.

Then another important metric:

### REOPEN WINDOW

How many "completed" tasks reopen within N relevant future events / audit window?

No universal time.

Use task type.

Excellent.

Then stable throughput.

Great.

Then a result.

Fast method initially 40% faster.

After reopen cost,

8% faster stable.

Still improvement.

Could be worth.

Honest.

Then another.

25% faster initially.

After rework,

10% slower stable.

Reject.

Perfect.

Then final principle.

Brutus should optimize **time to reliable usefulness**, not raw response speed, depending class.

Gabriel writes:

**LE TEMPS QUI COMPTE N’EST PAS TOUJOURS LE TEMPS JUSQU’À LA PREMIÈRE SORTIE. C’EST SOUVENT LE TEMPS JUSQU’À LA PREMIÈRE SORTIE QUI MÉRITE RÉELLEMENT D’ÊTRE UTILISÉE.**

Astra approuva strong.

Excellent.

Then the system looked at the growing Validation queue.

Fast generator still wanted to produce.

Metrics said it could.

But quality panel said the downstream system was saturated.

Gabriel knew what came next.

If quality mattered more than raw throughput,

then sometimes the correct decision would be to **produce less**.

Not because the machine was incapable.

Because producing more would lower the quality of what could be reviewed.

He looked at Astra.

— Bon. Là, faut qu’on ose dire que qualité passe avant débit.

Astra approuva.

Exactly.

The Kingdom had stopped worshipping speed.

Now it would have to turn that principle into an operational rule.

Not a slogan.

A policy.

A queue behavior.

A measurable tradeoff.

Gabriel wrote the last line:

**LA VITESSE AVAIT CESSÉ D’ÊTRE UNE VICTOIRE PAR ELLE-MÊME.**

Then:

**À PARTIR DE MAINTENANT, LE ROYAUME ALLAIT DEVOIR PROUVER QU’IL SAVAIT PRÉFÉRER UNE SORTIE MOINS NOMBREUSE MAIS PLUS SOLIDE LORSQUE LES DEUX ENTRAIENT EN CONFLIT.**

**Fin du chapitre 224.**