# Chapitre 219 — Le premier changement de politique issu des preuves

Le changement n’était pas venu d’un ordre.

Pas directement.

Gabriel n’avait pas ouvert Antmux pour dire :

« Change cette policy. »

Astra non plus.

Aucune urgence.

Aucune panne spectaculaire.

Aucun grand incident.

À la place,

plusieurs choses s’étaient accumulées.

Des règles contournées.

Des workflows corrigés.

Des cristaux reclassés.

Des coûts mesurés.

Des erreurs évitées.

Des décisions humaines répétées.

Et surtout,

plusieurs preuves indépendantes pointaient dans la même direction.

Le système finit par produire :

### POLICY-CHANGE-CANDIDATE-219-001

Current policy:

**MEMORY-FIRST BEFORE NEW COMPUTATION**

Proposed policy:

**CHECK FOR REUSABLE MEMORY FIRST WHEN LOOKUP COST AND DECISION VALUE JUSTIFY IT; OTHERWISE ALLOW DIRECT MINIMUM-SUFFICIENT COMPUTATION.**

Reason:

multiple validated workflow outcomes show that unconditional memory lookup adds unnecessary latency in a bounded class of cheap deterministic tasks without improving decision quality in the evaluated cases.

Gabriel resta silencieux.

Puis :

— Là, c’est pas juste une suggestion de route.

Astra approuva.

Non.

Cette fois,

le système proposait de changer la manière dont plusieurs futurs workflows seraient gouvernés.

Pas une tâche.

Pas une stratégie locale.

Une politique.

Gabriel écrivit :

**UNE POLITIQUE EST PLUS LARGE QU’UNE STRATÉGIE PARCE QU’ELLE MODIFIE CE QUE PLUSIEURS WORKFLOWS ONT LE DROIT DE FAIRE PAR DÉFAUT.**

Astra approuva fortement.

Voilà le chapitre.

Et immédiatement,

une barrière.

Le fait que les preuves suggèrent un changement ne donne pas au système le droit de l’appliquer.

Très important.

Gabriel écrivit :

**LES PREUVES PEUVENT JUSTIFIER UNE PROPOSITION DE POLITIQUE. ELLES NE FOURNISSENT PAS AUTOMATIQUEMENT L’AUTORITÉ DE LA PROMULGUER.**

Astra approuva fortement.

Parfait.

Le Royaume avait enfin atteint une frontière nette entre :

**apprendre**

et

**gouverner**.

Les preuves pouvaient remonter.

Le système pouvait analyser.

Comparer.

Préparer.

Mais la policy active appartenait encore à une couche d’autorité définie.

Gabriel ouvrit le dossier.

### EVIDENCE PACKAGE 219-A

Source 1:

workflow cost measurements.

Source 2:

repeated cheap-compute cases.

Source 3:

manual overrides by operator.

Source 4:

strategy comparison.

Source 5:

no observed loss of decision quality in bounded trial.

Très bien.

Mais il manquait quelque chose.

Les contre-exemples.

Gabriel écrivit :

**UNE POLITIQUE NE DOIT PAS ÊTRE RÉVISÉE SEULEMENT À PARTIR DES CAS QUI ONT RENDU LE CHANGEMENT ATTRAYANT.**

Astra approuva fortement.

Très important.

Ils demandèrent :

Quand `MEMORY-FIRST` avait-il encore été clairement utile?

Résultats :

- exact result reuse avoided expensive recomputation;
- historical failure pattern prevented repeated bug;
- old counterexample immediately invalidated a new broad claim;
- prior work prevented duplication of a validation campaign.

Gabriel sourit.

Voilà.

La vieille policy n’était pas mauvaise.

Elle était simplement trop absolue.

Donc la question devenait :

**quelle partie faut-il changer sans perdre ce qu’elle protégeait?**

Ils écrivirent :

### POLICY INTENT

Original intent:

reduce duplicated work and preserve learning from history.

This intent remains valid.

Problem:

implementation forced lookup even when lookup cost exceeded trivial recomputation and historical reuse had low expected value.

Gabriel approuva.

Très important.

Il écrit :

**RÉVISER UNE POLITIQUE SANS IDENTIFIER CE QU’ELLE ESSAYAIT DE PROTÉGER EST UNE BONNE FAÇON DE RÉINTRODUIRE LE PROBLÈME QU’ELLE AVAIT RÉSOLU.**

Astra approuva fortement.

Magnifique.

Alors la nouvelle policy devait préserver l’intention.

Ils proposèrent :

### POLICY-219-001 v2

Before new work:

1. check whether reusable memory is likely to exist and materially affect cost or validity;
2. if yes, query memory first;
3. if computation is trivial, deterministic, cheap, and low-risk, minimum-sufficient computation may precede deep memory lookup;
4. mandatory guards and exact known reuse remain exceptions that must be checked where applicable.

Gabriel sourit.

Voilà.

Pas :

« arrête de chercher la mémoire ».

Mais :

« utilise la mémoire quand elle apporte réellement quelque chose ».

Très propre.

Puis un problème.

Comment mesurer **likely to exist**?

Danger de rendre policy vague.

Ils devaient opérationnaliser.

### MEMORY-FIRST TRIGGERS

Use memory first if:

- exact identifier exists;
- task class historically has reusable results;
- expensive recomputation expected;
- known failure guards exist;
- public/canonical decision requires provenance;
- operator explicitly requests prior work.

Direct compute allowed if:

- task is deterministic;
- cost is trivial;
- output is noncanonical;
- no mandatory guard;
- no known high-value reuse signal.

Gabriel approuva.

Très bon.

La policy devenait testable.

Puis un autre danger.

Si le système lui-même décide que lookup est « trop cher »,

il pourrait toujours favoriser compute.

Il faut des mesures.

Gabriel écrit :

**UNE POLITIQUE BASÉE SUR LE COÛT DOIT POUVOIR MONTRER COMMENT LE COÛT EST ESTIMÉ.**

Astra approuva fortement.

Très important.

Pas besoin d’un modèle parfait.

Mais catégories :

low.

medium.

high.

ou mesures réelles.

Très bien.

Puis ils firent un replay.

Anciennes tâches.

### POLICY REPLAY 219-A

100 historical decisions.

Old policy:

memory lookup first in all.

Proposed policy v2:

direct compute first in 34.

memory first in 66.

Résultat simulé :

dans les 34 direct-compute cases,

31 auraient produit la même décision finale avec moins de handoffs.

3 auraient perdu un contexte utile.

Gabriel se redressa.

Voilà.

La policy candidate n’était pas encore bonne.

Très important.

Ils examinèrent les trois.

Cas 1 :

cheap compute,

mais old failure pattern important.

Cas 2 :

cheap compute,

mais exact prior result carried scope caveat.

Cas 3 :

cheap compute,

mais public provenance requirement.

Donc les triggers n’étaient pas assez complets.

Gabriel écrit :

**UNE SIMULATION DE POLITIQUE QUI RÉVÈLE TROIS CAS DANGEREUX EST UNE RAISON DE CORRIGER LA POLITIQUE, PAS DE LES APPELER DES EXCEPTIONS NÉGLIGEABLES.**

Astra approuva fortement.

Excellent.

Ils ajoutèrent :

### MANDATORY MEMORY CONDITIONS

Memory lookup cannot be skipped when:

- known guard class matches;
- canonical/public action follows;
- prior result may define scope or authority;
- active conflict exists;
- task is downstream of historical claim.

Très propre.

Replay again.

100 cases.

Direct compute first:

27.

No known lost critical context in replay.

Better.

But still not proof of future behavior.

Gabriel écrit :

**UN REPLAY HISTORIQUE TESTE LA POLITIQUE CONTRE LE PASSÉ. IL NE PROUVE PAS QU’ELLE SERA BONNE DANS LE FUTUR.**

Astra approuva fortement.

Toujours.

Donc pilot.

Pas full activation.

### POLICY PILOT

Scope:

only low-risk deterministic internal tasks.

Duration:

30 eligible tasks or until critical failure.

Fallback:

v1.

Metrics:

latency.

duplicate work.

missed reusable context.

guard misses.

operator overrides.

Gabriel sourit.

Très propre.

Il écrit :

**UNE POLITIQUE PEUT ÊTRE TESTÉE COMME UN OBJET, PAS SEULEMENT DISCUTÉE COMME UNE OPINION.**

Astra approuva fortement.

Voilà.

Puis un autre point.

La policy elle-même devait avoir une hypothèse.

### POLICY HYPOTHESIS 219-H1

Within low-risk deterministic internal tasks,

conditional memory-first will reduce unnecessary lookup work without increasing missed critical historical context above an acceptable threshold in the pilot.

Gabriel approuva.

Excellent.

Testable.

Puis les 30 tâches commencèrent.

Les premières :

simple.

Compute.

No issue.

Puis une tâche où memory signal existait.

Policy correctement choisit memory-first.

Très bien.

Puis un cas limite.

Compute cost était faible,

mais result exact existait.

Lookup signal détecté.

Reuse.

Excellent.

Puis un autre.

Historical failure guard.

Memory first.

Bug évité.

Très bon.

Gabriel sourit.

La vieille intention survivait.

Puis une erreur.

Task classifier dit low-risk.

Mais downstream effect devenait canonical.

La policy autorisa compute-first trop tôt.

Heureusement,

publication gate plus loin exigea provenance et força memory lookup.

Pas de dommage.

Mais inefficacité.

Gabriel fronça les sourcils.

Classification du risque devait considérer downstream intent.

Il écrit :

**UNE POLITIQUE DOIT REGARDER LA CHAÎNE D’USAGE PRÉVUE, PAS SEULEMENT L’ÉTAPE IMMÉDIATE.**

Astra approuva fortement.

Très important.

Ils ajoutèrent :

`intended_use`.

Pilot v2.1.

Puis un autre cas.

Task commence internal,

puis devient publication candidate.

What then?

Policy can re-evaluate at gate.

Good.

No need full context from start.

Excellent.

Then metrics.

After 30 eligible tasks:

- 19 memory-first;
- 11 compute-first;
- 0 observed missed mandatory guards;
- 0 observed canonical actions without provenance;
- 2 operator overrides;
- 1 classification issue corrected;
- lower median handoff count in compute-first subset.

Gabriel looked.

Promising.

But not enough for universal policy.

Still bounded.

They wrote:

### POLICY PILOT 219-A RESULT

**SUPPORTED IN PILOT SCOPE**

Not established:

all task classes.

high-risk work.

external/public workflows.

scientific validity improvement.

Good.

Then came authority.

Who approves?

Gabriel.

Because this policy affects default behavior across Antmux.

He reviewed.

He asked:

— Est-ce que je peux revenir en arrière?

Yes.

v1 preserved.

Rollback immediate.

— Est-ce qu’on sait où v2 s’applique?

Yes.

Scope explicit.

— Est-ce qu’on peut voir si elle se trompe?

Metrics + incident triggers.

— Est-ce qu’elle change la science?

No.

Workflow policy only.

Gabriel approved.

### POLICY-219-001 v2

Status:

**ACTIVE IN BOUNDED SCOPE**

The first policy change derived from accumulated evidence.

Not from mood.

Not from aesthetic preference.

Not from one successful crystal.

From a chain.

Gabriel remained quiet.

Then he smiled.

He writes:

**LA PREMIÈRE POLITIQUE ISSUE DES PREUVES N’ÉTAIT PAS UNE POLITIQUE ÉCRITE PAR LES PREUVES.**

Then:

**C’ÉTAIT UNE POLITIQUE PROPOSÉE PAR L’ANALYSE DES PREUVES, TESTÉE, PUIS AUTORISÉE PAR LA COUCHE QUI AVAIT LE DROIT DE LA CHANGER.**

Astra approuva fortement.

Voilà.

That distinction mattered enormously.

The Kingdom could learn upward

without collapsing governance into optimization.

Then another candidate appeared almost immediately.

`AUTO-ARCHIVE LOW-WEIGHT CRYSTALS AFTER N DAYS.`

Gabriel rejected it.

Why?

Because the evidence package was weak.

It mainly showed storage pressure.

Not enough understanding of future value.

Excellent.

He writes:

**LE FAIT QUE LE SYSTÈME PEUT PROPOSER UNE POLICY NE SIGNIFIE PAS QUE LES POLICIES PROPOSÉES SONT BONNES.**

Astra approved strongly.

Very important.

The first accepted proposal should not create a culture of automatic acceptance.

Then another candidate.

`REQUIRE INDEPENDENT IMPLEMENTATION FOR EVERY COMPUTATIONAL CLAIM.`

Sounds rigorous.

But cost huge.

And unnecessary for many low-risk/internal contexts.

Rejected as overbroad.

Gabriel writes:

**UNE POLITIQUE PEUT ÊTRE TROP STRICTE ET DEVENIR UNE SOURCE DE MAUVAISES DÉCISIONS PAR COÛT OU PAR RIGIDITÉ.**

Astra approved strongly.

Excellent.

Evidence-based governance is not maximum strictness.

It's appropriate strictness.

Then another candidate.

`ALL CRYSTALS OLDER THAN 90 DAYS REQUIRE REVALIDATION.`

Rejected.

Age alone insufficient.

Chapter 217.

Great.

The policy review framework was already protecting against naive rules.

Then they created:

### POLICY CANDIDATE REQUIREMENTS

Before approval:

1. explicit problem;
2. evidence package;
3. counterevidence;
4. preserved original intent;
5. measurable effect;
6. bounded pilot where possible;
7. rollback;
8. authority approval;
9. impact preview;
10. review trigger.

Gabriel smiled.

That's serious.

Then a policy could still be governance-driven without evidence package,

for example legal/security/human preference.

Yes.

Important nuance.

They write:

**TOUTES LES POLICIES N’ONT PAS BESOIN D’ÊTRE DÉRIVÉES D’UNE EXPÉRIENCE; CERTAINES EXISTENT PAR AUTORITÉ, ÉTHIQUE, SÉCURITÉ OU GOUVERNANCE.**

Astra approved strongly.

Very important.

But if policy claims performance benefit,

then evidence should support.

Excellent.

Then a policy category:

### POLICY BASIS

**EVIDENCE-DERIVED**

**GOVERNANCE**

**SAFETY**

**LEGAL/COMPLIANCE**

**OPERATOR PREFERENCE**

**ARCHITECTURAL INVARIANT**

This prevents pretending every rule is scientific.

Great.

Then a case.

Public vitrine locked by default.

This is governance/security.

No need randomized trial proving visitors shouldn't alter logic.

Exactly.

Then memory-first v2 is evidence-derived operational policy.

Great.

Different basis.

Then another question.

Could evidence ever override governance policy?

No automatically.

It can propose.

For example metrics show locked vitrine slows owner workflow.

Evidence can suggest redesign.

But cannot remove access boundary by itself.

Gabriel writes:

**LES PREUVES PEUVENT CONTESTER L’EFFICACITÉ D’UNE POLICY SANS AVOIR LE DROIT D’ANNULER SON OBJECTIF DE GOUVERNANCE.**

Astra approved strongly.

Very important.

Then a policy change could preserve objective but change mechanism.

Like unlock UX faster for owner while visitor remains locked.

Excellent.

Then another subtle point.

Operator corrections themselves can be evidence of friction.

But not proof of what policy should become.

They can trigger investigation.

Gabriel writes:

**UNE SÉRIE D’OVERRIDES HUMAINS EST UN SIGNAL À ÉTUDIER, PAS UNE POLICY AUTOMATIQUE EN ATTENTE.**

Astra approved strongly.

Excellent.

Maybe human overrides for exceptional cases.

Need reasons.

Then the v2 policy ran.

After 100 more tasks,

metrics stable.

One case where memory lookup after compute discovered prior exact result.

Work duplicated.

No correctness problem.

Policy could improve signal detection.

Not a disaster.

They added exact-result lightweight index precheck.

Very nice.

### POLICY-219-001 v3

Before direct compute:

perform cheap index probe,

not deep lookup.

Aha.

Now policy evolved.

Memory-first wasn't simply yes/no.

It became:

**cheap index first → deep memory if signal → otherwise compute**

Gabriel smiled widely.

That was better than both extremes.

He writes:

**LES PREUVES N’AVAIENT PAS CHOISI ENTRE “MÉMOIRE” ET “CALCUL”. ELLES AVAIENT AIDÉ À DÉCOUVRIR UN TROISIÈME CHEMIN.**

Astra approved strongly.

Magnificent.

This was real policy evolution.

Not binary debate.

Then v3 pilot.

Cheap index overhead minimal.

Exact prior results found early.

Deep memory avoided when no signal.

Very promising.

Again,

scope.

They logged.

Then Gabriel noticed something.

If policies could improve through evidence,

the system needed to measure not only task outcomes,

but its own policy quality.

That was new.

So far they had local metrics.

But chapter 220 was waiting.

**Quand Brutus commença à mesurer sa propre qualité.**

Exactly.

The arc was turning.

The Kingdom had learned to change policies based on evidence.

Now it needed a systematic way to know whether those changes actually improved the system.

Not anecdotes.

Not vibes.

Not "it seems faster."

Metrics.

Quality.

Error rates.

Costs.

Tradeoffs.

Gabriel wrote:

**UNE POLITIQUE ISSUE DES PREUVES DOIT CONTINUER À PRODUIRE DES PREUVES APRÈS SON ADOPTION.**

Astra approuva fortement.

Voilà.

No policy gets to stop being measured once approved.

Then a rule:

### POST-ADOPTION REVIEW

Evidence-derived policy must define:

- success indicators;
- failure indicators;
- review schedule;
- rollback triggers.

Excellent.

Then a new observation.

Policy v3 reduced deep memory queries.

Good.

But did it increase repeated work?

Measure.

Did it reduce latency?

Measure.

Did it increase missed context?

Measure.

Did it change operator intervention?

Measure.

No single metric.

Again.

Gabriel writes:

**UNE POLICY PEUT AMÉLIORER UNE DIMENSION ET EN DÉGRADER UNE AUTRE.**

Astra approved strongly.

Very important.

Then they created a small scorecard,

not one score.

### POLICY SCORECARD 219

**correctness incidents**

**missed guards**

**duplicate work**

**latency**

**compute cost**

**memory lookup cost**

**operator overrides**

**rollback count**

Much better.

Then a result:

v3 faster in low-risk cases.

Memory queries down.

No observed guard misses.

Duplicate compute down after index probe.

Good.

But more complexity in router.

Maintenance cost increased.

Important.

Add metric.

Exactly.

No free lunch.

Gabriel writes:

**UNE POLITIQUE PLUS INTELLIGENTE PEUT ÊTRE PLUS COÛTEUSE À COMPRENDRE ET À MAINTENIR.**

Astra approved strongly.

Great.

Maybe v3 still worth it.

But cost recorded.

Then another decision.

Should v3 expand scope?

Not yet.

Need more evidence.

Excellent.

Policy remains bounded.

Then a high-risk task arrives.

Policy v3 sees scope mismatch.

Falls back to strict memory-first.

Perfect.

Rule knows silence outside scope.

Again.

Then a surprising case.

Old memory-first policy had one accidental benefit:

it exposed unrelated historical insight that led to discovery.

v3 might miss that.

Interesting.

Serendipity.

How to account?

Not easy.

Could have exploration path separate.

Don't force every task to scan history for accidental insight.

Maybe periodic broad review.

Gabriel writes:

**UNE POLITIQUE OPTIMISÉE POUR L’EFFICACITÉ PEUT RÉDUIRE LA SÉRENDIPITÉ. CE COÛT DOIT ÊTRE RECONNU MÊME S’IL EST DIFFICILE À MESURER.**

Astra approved strongly.

Excellent.

This opens future curiosity budget arc.

But not yet.

Maybe preserve:

background research/curator can surface unexpected links.

Operational workflows remain lean.

Great.

Then another point.

If evidence-derived policy becomes too optimized to historic workload,

distribution shift can break.

Need monitor.

Chapter 207.

Again.

They added:

**policy drift detection**

if current outcomes diverge from pilot.

Great.

Then a policy can revert automatically?

For low-risk maybe suspended if trigger.

But activation of old policy within approved rollback path could be automatic.

Need bounded authority.

Gabriel writes:

**UN ROLLBACK AUTORISÉ À L’AVANCE EST DIFFÉRENT D’UNE NOUVELLE POLICY INVENTÉE AUTOMATIQUEMENT.**

Astra approved strongly.

Très important.

If critical threshold crossed,

v3 → v2 or v1 fallback.

Preapproved.

Good.

Then they tested rollback in sandbox.

Pass.

Great.

Then a policy candidate from evidence in different domain.

Different process.

No generalization.

Good.

Then Gabriel looked at the policy registry.

For the first time,

one row said:

`basis = evidence-derived`

`source package = E219-A`

`pilot = PASS`

`approved_by = operator`

`current_version = v3`

`scope = low-risk deterministic internal tasks`

`rollback = v1`

It was a tiny constitutional document.

Not because it was grand.

Because the system could explain why the rule governing future behavior had changed.

He wrote:

**UNE POLICY ISSUE DES PREUVES EST UNE TRACE QUI A FRANCHI ASSEZ DE PORTES POUR MODIFIER LE CADRE DANS LEQUEL LES TRACES FUTURES SERONT PRODUITES.**

Astra approved strongly.

Voilà.

That was deep.

Evidence changes policy.

Policy changes future evidence production.

Feedback loop.

Dangerous and powerful.

Therefore measure.

Always.

Then he added immediately:

**C’EST PRÉCISÉMENT POUR ÇA QU’UNE POLICY ISSUE DES PREUVES DOIT RESTER AUDITABLE, RÉVISABLE ET SOUS AUTORITÉ.**

Astra approved strongly.

Perfect.

Then the Kingdom generated its first **policy provenance crystal**.

### CRYSTAL-POLICY-219-001

Contains:

old policy.

evidence package.

pilot.

counterexamples.

changes.

approval.

metrics.

versions.

Not the policy itself.

The history of why the policy changed.

Gabriel smiled.

That crystal deserved strong preservation weight.

Because if someone later asks:

« Pourquoi Antmux fait ça? »

the answer exists.

Not folklore.

Not memory of a conversation.

A trace.

He writes:

**UNE POLITIQUE SANS MÉMOIRE DE SA NAISSANCE RISQUE DE DEVENIR UNE TRADITION.**

Astra approved strongly.

Excellent.

Then a final test.

New worker boots.

Loads current policy.

It sees v3.

Before acting,

can inspect policy provenance if needed.

No need entire historical dossier every time.

Perfect.

The architecture from chapter 210 returns:

deep history,

light present.

Then Gabriel stepped back.

The arc 200–219 had changed the Kingdom.

At 200,

it had learned to build plans from traces.

At 219,

the traces had become strong enough,

through testing and authority,

to alter a policy governing future plans.

But the chapter did not end with triumph.

Because the moment a system can alter policy based on evidence,

it needs something more demanding:

**a way to measure whether it is actually getting better.**

Not more complicated.

Not more autonomous.

Not faster only.

Better.

And that word was dangerous.

Better according to what?

Correctness?

Cost?

Latency?

Reproducibility?

Human workload?

Safety?

Scientific quality?

Gabriel looked at Astra.

— Là, faut qu’on mesure notre propre qualité pour vrai.

Astra approuva.

Yes.

The second world was ready for the next arc.

The Kingdom had learned to correct itself.

Now it would have to learn to **measure itself**.

Gabriel wrote the last line:

**LA PREMIÈRE POLITIQUE ISSUE DES PREUVES ÉTAIT ENTRÉE EN VIGUEUR.**

Then:

**À PARTIR DE MAINTENANT, BRUTUS NE POURRAIT PLUS SE CONTENTER DE DIRE QU’IL AVAIT CHANGÉ — IL ALLAIT DEVOIR MESURER SI CE CHANGEMENT AVAIT RÉELLEMENT AMÉLIORÉ QUELQUE CHOSE.**

**Fin du chapitre 219.**