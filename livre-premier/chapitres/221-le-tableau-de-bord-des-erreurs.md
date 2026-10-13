# Chapitre 221 — Le tableau de bord des erreurs

Le premier tableau de bord de qualité avait à peine commencé à respirer

qu’une chose devenait évidente.

Les erreurs existaient déjà partout.

Mais elles vivaient séparément.

Un mauvais routage dans Antmux.

Une provenance incomplète dans Memoria.

Une règle devenue trop large.

Un vieux cache.

Un claim trop fort.

Une tâche inutile.

Une révision mal propagée.

Un worker qui avait repris avec un contexte dépassé.

Tout cela était connu.

Mais dispersé.

Gabriel regarda Astra.

— Là, on a besoin d’une place où les erreurs arrêtent de se cacher chacune dans leur coin.

Astra approuva.

Exact.

Ce n’était pas un journal d’échec.

Ce n’était pas une liste rouge.

Ce n’était pas un classement humiliant des modules.

Le but était différent.

**Voir les erreurs assez clairement pour comprendre comment le Royaume se trompait.**

Gabriel écrivit :

**UNE ERREUR QU’ON NE PEUT PAS CLASSER EST DIFFICILE À CORRIGER SYSTÉMATIQUEMENT.**

Astra approuva fortement.

Puis :

**UNE ERREUR QU’ON NE PEUT PAS RELIER À SA CAUSE RISQUE DE REVENIR SOUS UN AUTRE NOM.**

Voilà.

Ils commencèrent par un écran vide.

### ERROR DASHBOARD

Pas encore de nombres.

D’abord des catégories.

Le chapitre précédent avait déjà défini plusieurs types :

- correctness error;
- routing error;
- authority error;
- semantic escalation error;
- efficiency error;
- provenance error;
- stale-context error;
- revision error.

Mais maintenant il fallait les faire vivre.

Gabriel ajouta :

### ERROR EVENT

**error_id**

**workflow_id**

**module**

**time**

**error_type**

**severity**

**detected_by**

**detected_at_stage**

**impact**

**cause_status**

**containment**

**correction**

**downstream_audit**

**current_status**

Astra approuva fortement.

Très propre.

Chaque erreur devait devenir un objet.

Pas une note oubliée.

Pas une phrase dans un chat.

Pas « on a vu un bug tantôt ».

Un événement traçable.

Gabriel écrivit :

**UNE ERREUR DOIT POUVOIR AVOIR UNE IDENTITÉ SANS DEVENIR UNE HONTE.**

Astra approuva fortement.

Important.

Parce que si le système cache les erreurs pour garder ses métriques belles,

tout le tableau devient inutile.

Il fallait donc une règle.

### NO ERROR HIDING

Une erreur détectée et confirmée doit entrer au registre,

même si elle a été corrigée immédiatement.

Gabriel sourit.

Très important.

Un correctif rapide n’efface pas le fait que l’erreur a existé.

Il écrit :

**CORRIGÉ VITE ≠ N’A JAMAIS EXISTÉ**

Astra approuva fortement.

Voilà.

Puis ils prirent le premier cas.

### ERROR-221-001

Type :

PROVENANCE_ERROR

Module :

nouveau chemin de raccourci.

Impact :

metadata lineage field missing.

Detected by :

quality dashboard.

Stage :

post-run audit.

Severity :

Q2.

Cause :

implementation path bypassed metadata contract.

Containment :

shortcut disabled.

Correction :

contract enforcement added.

Downstream audit :

12 outputs checked.

Current status :

CLOSED.

Gabriel regarda.

Parfait.

Une erreur complète.

Pas seulement :

« bug corrigé ».

L’histoire de la correction existait.

Puis une question.

Que signifie **CLOSED**?

Danger.

Closed could mean:

bug patch applied.

Or:

all affected outputs reviewed.

Or:

cause understood.

Need separation.

They created:

### ERROR STATUS

**DETECTED**

**TRIAGED**

**CONTAINED**

**ROOT_CAUSE_IDENTIFIED**

**FIXED**

**VERIFIED**

**CLOSED**

Astra approuva fortement.

Très important.

Un bug n’est pas fermé juste parce qu’un commit a été fait.

Gabriel écrit :

**FIXÉ ≠ VÉRIFIÉ**

Astra approuva fortement.

Encore.

Et :

**VÉRIFIÉ ≠ IMPACT HISTORIQUE AUDITÉ**

Voilà.

Donc closure requires appropriate downstream audit where relevant.

Puis un autre cas.

### ERROR-221-002

Task routed to Validation instead of Research.

No scientific damage.

Cost:

8 minutes.

Detected by:

operator.

Type:

ROUTING_ERROR.

Severity:

Q1.

Cause:

ambiguous task classification.

Correction:

queue routing profile refined.

Très bon.

Puis un autre.

### ERROR-221-003

Claim wording:

"none exist"

Evidence:

bounded scan only.

Detected before publication.

Type:

SEMANTIC_ESCALATION_ERROR.

Severity:

Q3.

Containment:

publication blocked.

Correction:

claim changed to bounded statement.

No public impact.

Gabriel se redressa.

Voilà.

Cette erreur est beaucoup plus importante que 30 secondes de latence.

Donc le tableau doit pouvoir montrer gravité,

pas seulement nombre.

Il écrit :

**COMPTER LES ERREURS SANS LES CLASSER PAR CONSÉQUENCE PEUT DONNER PLUS DE POIDS À DIX PETITS PROBLÈMES QU’À UNE SEULE ERREUR CRITIQUE.**

Astra approuva fortement.

Très important.

Puis un cas Q4.

Un workflow effectue une action publique sans gate autorisé.

Ça,

grave.

Même si résultat final correct.

Authority violation.

Gabriel écrit :

**UNE ACTION PEUT PRODUIRE LE BON RÉSULTAT ET RESTER UNE ERREUR SI ELLE N’AVAIT PAS LE DROIT D’ÊTRE EXÉCUTÉE.**

Astra approuva fortement.

Excellent.

La qualité n’était pas seulement résultat.

Encore.

Puis ils ajoutèrent :

### ERROR SEVERITY DIMENSIONS

Severity depends on:

- reversibility;
- blast radius;
- public/canonical impact;
- authority breach;
- evidence corruption risk;
- recoverability;
- detection delay.

Gabriel sourit.

Encore une fois,

pas besoin d’un score magique.

Mais une classification cohérente.

Puis une question :

une erreur Q1 répétée mille fois est-elle toujours Q1?

Chaque instance oui,

mais la répétition peut devenir un problème systémique majeur.

Très important.

Ils créèrent :

### ERROR PATTERN

If same error class recurs beyond expected baseline:

create pattern object.

Example:

`PATTERN-ROUTE-221-A`

14 similar misroutes in 3 days.

Now the pattern itself has severity.

Gabriel écrit :

**UNE PETITE ERREUR RÉPÉTÉE PEUT DEVENIR UN GRAND PROBLÈME SANS QUE CHAQUE INSTANCE DEVIENNE GRAVE INDIVIDUELLEMENT.**

Astra approuva fortement.

Excellent.

Le tableau devait donc avoir deux niveaux :

events.

patterns.

Puis cause.

Toutes les erreurs n’ont pas une cause connue.

Très important.

Status:

UNKNOWN.

No pretending.

They created:

### CAUSE STATUS

**UNKNOWN**

**HYPOTHESIZED**

**SUPPORTED**

**CONFIRMED**

Gabriel sourit.

Parfait.

Pas de root cause inventée.

Il écrit :

**UNE EXPLICATION PLAUSIBLE N’EST PAS UNE CAUSE CONFIRMÉE.**

Astra approuva fortement.

Encore.

Puis une erreur avec plusieurs causes.

Possible.

Bad metadata.

Plus stale cache.

Plus weak guard.

Need contributing factors.

Not one root if reality complex.

Gabriel écrit :

**TOUTES LES ERREURS N’ONT PAS UNE SEULE CAUSE RACINE.**

Astra approuva fortement.

Très important.

Ils créèrent :

### CAUSAL FACTORS

**primary**

**contributing**

**enabling**

**detection failure**

Excellent.

Example:

Primary:

stale policy cache.

Contributing:

worker reconnect skipped refresh.

Enabling:

authority lease too long.

Detection failure:

no pre-action gate check.

Great.

Then a more subtle idea.

Error prevention vs error detection.

A system may improve because same underlying defect exists but is caught earlier.

That's still improvement.

Gabriel writes:

**DÉTECTER PLUS TÔT UNE ERREUR PEUT ÊTRE UNE AMÉLIORATION MÊME AVANT QU’ON AIT ÉLIMINÉ SA CAUSE.**

Astra approved strongly.

Very important.

Thus dashboard needs:

detection stage.

### DETECTION STAGE

**PRE-EXECUTION**

**DURING EXECUTION**

**POST-EXECUTION**

**PRE-PUBLICATION**

**POST-PUBLICATION**

**EXTERNAL REPORT**

Earlier generally better,

but depends.

Then metrics:

mean time to detect?

Maybe.

But distributions.

And severity.

Good.

Then another dimension.

Time to contain.

Time to correct.

Time to verify.

Excellent.

### ERROR RESPONSE TIMES

**TTD**

time to detect.

**TTC**

time to contain.

**TTF**

time to fix.

**TTV**

time to verify.

Gabriel sourit.

Useful.

But not universal optimization.

Fast wrong fix bad.

So time paired with correctness.

Il écrit :

**CORRIGER VITE UNE ERREUR AVEC UN MAUVAIS CORRECTIF N’EST PAS UNE BONNE PERFORMANCE.**

Astra approuva fortement.

Évident.

Puis un dashboard row.

Error 003:

Detected pre-publication.

Contained immediate.

Fix 4 min.

Verified 12 min.

Downstream impact none.

Excellent.

Then another:

detected after 2 days.

Public impact.

Correction 10 min.

Downstream audit 6 hours.

Very different.

This is useful.

Then one major issue.

If system gets better at detecting errors,

error count may go up.

That doesn't necessarily mean quality worsened.

Important.

Gabriel writes:

**PLUS D’ERREURS DÉTECTÉES PEUT SIGNIFIER PLUS D’ERREURS PRODUITES — OU SIMPLEMENT UNE MEILLEURE CAPACITÉ À LES VOIR.**

Astra approved strongly.

Excellent.

Therefore raw error count over time is ambiguous.

Need detection coverage.

Audits.

Exposure.

Great.

Then a module installs better validator.

Error events spike.

Could be good.

Need interpret.

Then after fixes,

rates decline.

Fine.

Then another issue.

Error rate denominator.

Per task?

Per action?

Per claim?

Depends type.

Authority errors per sensitive action.

Routing errors per routed task.

Provenance errors per produced artifact.

Semantic escalations per claim transition.

Gabriel writes :

**UNE ERREUR DOIT AVOIR UN DÉNOMINATEUR QUI CORRESPOND À L’OCCASION OÙ ELLE POUVAIT ARRIVER.**

Astra approuva strong.

Very important.

No one global rate.

Then they created:

### ERROR RATE CONTRACT

For each error type:

define exposure unit.

Perfect.

Then one metric:

0 authority violations / 500 sensitive actions.

Better than 0.

Great.

Then a quality issue.

If exposure tracking incomplete,

rate unknown.

Show UNKNOWN.

Never divide by guessed denominator.

Gabriel smiles.

Chapter 220 principle.

Then another case.

Human rescue.

Machine generates overbroad claim.

Gabriel catches before publication.

Workflow successful.

But error event remains.

Type:

semantic escalation.

Detected_by human.

Good.

This gives system learning target.

Then if same error recurs 10 times,

guard inadequate.

Excellent.

Then human mistakes too?

The dashboard should track workflow errors,

not blame person.

Could include source actor:

human/system/module/external input.

But not leaderboard.

Gabriel writes :

**LE TABLEAU DE BORD DES ERREURS DOIT SERVIR À CORRIGER LE SYSTÈME, PAS À FABRIQUER UN PALMARÈS DES COUPABLES.**

Astra approuva strong.

Very important.

Because blame reduces reporting.

Then a user-supplied typo causes failure.

Could be input error.

But system maybe should validate.

Useful.

No blame.

### ERROR ORIGIN

**INPUT**

**SYSTEM**

**POLICY**

**ENVIRONMENT**

**DEPENDENCY**

**HUMAN DECISION**

**UNKNOWN**

Again, origin ≠ blame.

Great.

Then one case.

External API returns stale data.

System trusts it.

Cause:

dependency.

But lack of freshness check is enabling system factor.

Exactly.

Good.

Then another.

Network failure.

No bug.

Operational failure event.

Should that be error?

Maybe yes as incident,

but separate from internal defect.

Need distinguish.

### ERROR VS INCIDENT

**ERROR**

process/system decision deviates from intended contract.

**INCIDENT**

undesired operational event, possibly external.

Can overlap.

Gabriel approuva.

Very important.

Not every outage means coding error.

Then dashboard can link incident to errors.

Good.

Then one case:

disk fills.

Incident.

Cleaner deletes wrong file.

Error.

Two events.

Great.

Then another distinction.

Expected failure.

A hypothesis test returns negative.

Not error.

Very important.

Gabriel writes :

**UN RÉSULTAT NÉGATIF ATTENDU COMME POSSIBILITÉ N’EST PAS UNE ERREUR.**

Astra approuva strong.

This protects research.

Likewise:

NO VALID COMPOSITION under contracts.

Not error if correct.

Good.

Then timeout due stop condition.

Not necessarily error.

Could be designed outcome.

Excellent.

Then false positives.

Guard blocks safe action.

Could be overconstraint error or acceptable conservative behavior depending policy.

Need classify.

Again.

Then a safe fallback triggered.

Maybe not error.

Could be degraded mode event.

Thus dashboard must avoid labeling every non-happy path as error.

Gabriel writes :

**UN CHEMIN DE SECOURS QUI S’ACTIVE COMME PRÉVU N’EST PAS UNE PANNE.**

Astra approuva strong.

Excellent.

Then another important class.

**Near miss.**

An error nearly happened but guard caught before bad state.

Should track.

Yes.

### NEAR MISS

Condition that would have produced error absent a guard.

Useful for measuring protective mechanisms.

Gabriel sourit.

This is big.

A guard preventing 50 incidents should get credit.

But near miss count increase could mean underlying issue worsening.

Again interpretation.

Il écrit :

**UN NEAR MISS PROUVE QU’UNE PROTECTION A SERVI; IL PEUT AUSSI SIGNALER QUE LE DANGER SOUS-JACENT EST FRÉQUENT.**

Astra approuva strong.

Perfect.

Then dashboard shows:

errors.

near misses.

incidents.

This becomes operationally useful.

Then one example.

Semantic guard blocks SCREENING→VALIDATED escalation.

Near miss.

No error propagated.

Great.

Then 12 such near misses.

Maybe interface causing bad promotion attempts.

Fix upstream.

Excellent.

Then a rule.

Don't just celebrate guard.

Remove source if possible.

Gabriel writes :

**UNE GARDE QUI SAUVE LE SYSTÈME CENT FOIS PEUT ÊTRE EXCELLENTE — ET AUSSI RÉVÉLER QU’IL FAUT CORRIGER CE QUI FRAPPE CENT FOIS CONTRE ELLE.**

Astra approuva strong.

Beautiful.

Then another metric.

Recurrence after fix.

A fix that doesn't reduce recurrence may be incomplete.

So dashboard tracks reopened/repeated.

### FIX EFFECTIVENESS

Compare before/after within comparable exposure.

Not claim causality automatically.

But useful.

Then a fix creates new error type.

Regression.

Need link.

### REGRESSION

New error related to prior corrective change.

Very important.

Gabriel writes :

**UNE CORRECTION PEUT RÉSOUDRE UNE ERREUR ET EN CRÉER UNE AUTRE.**

Astra approuva strong.

That's why post-fix verification matters.

Then one real example.

Stale cache fix forces fresh lookup every time.

Stale errors down.

Latency spikes.

Not an error maybe,

but quality tradeoff.

If timeout occurs,

new error.

Then optimize.

Great.

Then dashboard grouping.

By:

type.

module.

workflow class.

severity.

status.

cause.

version.

time.

But avoid shame.

Good.

Then trend heatmap perhaps.

Not necessary text.

But BrutoBac could visualize.

Error crystals?

Maybe.

Red is tempting.

But role labels better.

Gabriel smiles.

Could have fracture marks.

Yet no dramatization.

Then "error crystal" itself.

Should errors become crystals?

Yes,

because durable lessons.

But status distinct.

Maybe `INCIDENT_CRYSTAL`.

Gabriel writes :

**UNE ERREUR BIEN DOCUMENTÉE PEUT DEVENIR UNE DES TRACES LES PLUS UTILES DU ROYAUME.**

Astra approved strongly.

Chapter 198 again.

Then they looked at an old nasty corruption guard.

Born from failure.

Now critical.

Great.

Error became guard.

This is learning.

They define:

### ERROR LIFECYCLE

error event

→ analysis

→ fix

→ verification

→ lesson

→ guard/strategy/policy candidate.

Not every error reaches policy.

Good.

Then an error repeats after fix.

Could mean:

fix failed.

different cause.

scope incomplete.

Need compare.

No assume same.

Then deduplicate errors carefully.

Exact duplicate vs similar pattern.

Don't merge away important variation.

Gabriel writes :

**DEUX ERREURS QUI SE RESSEMBLENT PEUVENT AVOIR DES CAUSES DIFFÉRENTES.**

Astra approuva strong.

Thus clustering creates candidate pattern,

not identity.

Excellent.

Then another.

One cause can produce many error types.

Stale context may cause:

routing error.

authority error.

wrong claim.

Need causal graph.

Maybe later.

But dashboard can link.

### ERROR GRAPH

Cause node.

Events.

Downstream effects.

Very powerful.

Then a shared dependency bug.

Multiple modules fail.

Graph reveals one common parser.

Great.

Then avoid counting as multiple independent failures in root-cause analysis.

But still impact counts across modules.

Again independence.

Then error budget?

Could be useful later maybe.

But not all errors can be budgeted.

Authority violations should not be "allowed 5 per month."

Gabriel writes :

**CERTAINES ERREURS PEUVENT ÊTRE GÉRÉES PAR OBJECTIF DE RÉDUCTION; D’AUTRES DOIVENT ÊTRE TRAITÉES COMME DES VIOLATIONS À ÉVITER, PAS COMME UN QUOTA À CONSOMMER.**

Astra approuva strong.

Very important.

No simplistic error budget for critical semantic/authority violations.

Then efficiency errors could have budgets.

Fine.

Then another dimension.

Severity can depend on when caught.

Same semantic escalation:

pre-publication Q2/Q3.

post-publication higher.

Yes.

Impact.

Then a near miss before action:

lower realized impact.

But latent risk still.

Great.

Then a public correction event.

Dashboard links error to correction.

Good.

Then a task abort.

If system detects potential corruption and stops,

maybe success.

Do not count aborted workflow as error if guard did job.

Yet underlying trigger may be near miss.

Exactly.

Then a new view:

### TOP CURRENT RISKS

Not "top worst modules."

Patterns ranked by:

severity.

recurrence.

exposure.

unresolved status.

Again not one magic number perhaps.

But triage.

Could use rules.

Critical unresolved first.

Then systemic repeated.

Then low-level.

Good.

Then Gabriel asks:

— Which error is costing us most?

Could be by total time.

Another by risk.

Need separate views.

### ERROR VIEWS

**BY RISK**

**BY COST**

**BY FREQUENCY**

**BY RECURRENCE**

**BY UNRESOLVED AGE**

**BY PUBLIC IMPACT**

Very clean.

No one leaderboard.

Then an efficiency error may top cost.

A semantic error tops risk.

Different.

Excellent.

Then a trial.

### ERROR DASHBOARD TRIAL 221-A

Window:

100 workflows.

Detected events:

- 5 routing inefficiencies;
- 3 provenance omissions;
- 2 stale-context events;
- 2 semantic near misses;
- 1 actual semantic escalation caught before publication;
- 0 authority violations observed;
- 0 canonical corruption observed.

Important:

not global rates.

Only tested window.

Gabriel nods.

Then patterns:

routing inefficiencies cluster in one task classifier.

Provenance omissions cluster in one shortcut path.

Stale context from one cache.

Semantic near misses from ambiguous status naming.

Aha.

Now errors were actionable.

They create four work items.

Great.

Then another insight.

The number of error events = 13.

But actual underlying improvement targets = 4.

This is why patterns matter.

Gabriel writes :

**TREIZE ERREURS PEUVENT ÊTRE QUATRE PROBLÈMES — OU TREIZE PROBLÈMES. IL FAUT REGARDER LA STRUCTURE, PAS SEULEMENT LE COMPTE.**

Astra approuva strong.

Excellent.

Then fix ambiguous status naming.

SCREENING and VALIDATED now typed more strongly.

Semantic near misses drop in next panel.

Promising.

Then stale cache fix.

No stale events in next comparable small window.

But latency up 4%.

Tradeoff.

Quality dashboard chapter 220 catches it.

Great.

Then routing classifier fix.

Misroutes down.

No increase in escalation.

Nice.

Then provenance contract fix.

Omissions zero in next sample.

Good.

Again bounded.

No universal claims.

Then an important problem.

If dashboard is fed by modules themselves,

can errors be underreported?

Maybe.

Independent audit stream helps.

Gabriel writes :

**UN MODULE NE DEVRAIT PAS ÊTRE LA SEULE SOURCE D’INFORMATION SUR SES PROPRES ERREURS.**

Astra approuva strong.

Very important.

Sources:

self-reported.

guards.

audits.

human corrections.

downstream contradictions.

Independent validation.

Great.

Then detection provenance.

Every error says who detected.

Useful.

If most critical errors detected only by Gabriel manually,

automation gap.

That's actionable.

Excellent.

Then a metric:

### DETECTION SOURCE PROFILE

Human.

Automated guard.

Audit.

Downstream failure.

External report.

Goal not necessarily zero human.

But understand.

Great.

Then one sobering result.

In sample,

2 of 3 high-severity semantic issues were caught manually.

So automatic semantic guards need improvement.

This matters.

Gabriel smiles.

Not shame.

Work.

He writes :

**LE TABLEAU DE BORD NE DEVAIT PAS DIRE “BRUTUS EST MAUVAIS”. IL DEVAIT DIRE “VOICI OÙ LA PROCHAINE AMÉLIORATION A LE PLUS DE SENS”.**

Astra approuva strong.

Voilà.

Then another risk.

Optimizing error dashboard can create conservative paralysis.

If system avoids risky tasks to reduce errors,

bad.

Need exposure/coverage.

Chapter 220.

So dashboard shows task coverage alongside error rates.

Gabriel writes :

**UN SYSTÈME QUI NE FAIT PLUS RIEN PEUT AVOIR TRÈS PEU D’ERREURS. CE N’EST PAS UNE VICTOIRE.**

Astra approuva strong.

Excellent.

Then compare:

errors per exposure.

coverage.

resolved tasks.

Great.

Then another.

Over-escalation to human reduces machine error.

But increases human load.

Need quality dashboard.

Again.

No local optimization.

Excellent.

Then a very subtle thing.

Unknown errors.

By definition invisible.

You cannot count them.

So dashboard should state:

**detected errors**, not total errors.

Gabriel writes :

**UN TABLEAU DE BORD DES ERREURS MESURE LES ERREURS DÉTECTÉES, PAS TOUTES LES ERREURS QUI EXISTENT NÉCESSAIREMENT.**

Astra approuva strong.

Critical scientific honesty.

Then audits estimate detection gaps maybe.

But not claim completeness.

Great.

Then one external contradiction arrives.

Reveals old error not previously known.

Dashboard adds event with occurrence_time historical, detection_time now.

Excellent.

Two times.

### ERROR TEMPORALITY

**occurred_at**

**detected_at**

**contained_at**

**corrected_at**

This lets measure latent errors.

Very useful.

Then an old error discovered now may have broad downstream impact.

Need historical audit.

Great.

Then a correction may have already happened unknowingly due later change.

Still record.

Excellent.

Then another issue.

Error severity may be revised after impact known.

At detection Q2.

Later find public impact → Q4.

Need versioned severity event.

Gabriel writes :

**L’IMPORTANCE D’UNE ERREUR PEUT CHANGER QUAND ON DÉCOUVRE SON VRAI RAYON D’ACTION.**

Astra approuva strong.

Very important.

Again, status evolves.

Then error closure can reopen.

If recurrence or missed downstream impact.

Allow REOPENED.

Good.

Then one final experiment.

They intentionally seeded low-risk test faults in sandbox.

Wrong queue label.

Missing provenance field.

Stale cache.

Overbroad claim transition.

Not production.

Goal:

test detection.

Results:

- routing fault caught;
- provenance fault caught;
- stale cache caught;
- claim transition caught at semantic gate.

4/4 in sandbox.

Gabriel smiles.

But:

small synthetic test.

Not proof of real-world completeness.

They log:

### DETECTION TEST 221-B

Synthetic bounded faults:

4.

Detected:

4.

Status:

PASS IN TEST CONDITIONS ONLY.

Excellent.

Then they realize error dashboard itself needs tests.

Great.

Then a more realistic mutation test perhaps later.

Not now.

Then a final principle.

Errors should connect to improvements.

Every closed serious error asks:

Did it create:

fix?

guard?

test?

policy change?

documentation?

Maybe not all.

But some durable response.

Gabriel writes :

**UNE ERREUR SÉRIEUSE QUI NE LAISSE AUCUNE TRACE D’APPRENTISSAGE EST UNE ERREUR QUI PEUT COÛTER DEUX FOIS.**

Astra approuva strong.

Excellent.

Then the dashboard changed shape.

At first it was a wall of defects.

After classification,

it became a map.

A few repeated patterns.

Several minor inefficiencies.

One semantic weakness.

One stale cache family.

No observed critical authority violation in the tested window.

Some unknowns.

Some incomplete audits.

Much more useful.

Gabriel stepped back.

For the first time,

the Kingdom could answer:

**où est-ce qu’on se trompe?**

Not perfectly.

Not exhaustively.

But concretely.

And then a new question appeared.

Every error had a cost.

Sometimes minutes.

Sometimes compute.

Sometimes human attention.

Sometimes a public correction.

Sometimes a lost route.

Sometimes a full revalidation campaign.

Gabriel looked at Astra.

— On mesure les erreurs. Mais combien elles nous coûtent pour vrai?

Astra approuva.

Exactly.

Because an error count without its cost tells only part of the story.

A five-second misroute.

A six-hour recomputation.

A missed provenance chain.

A public correction.

They were not economically equivalent.

The next chapter had already begun.

**Fin du chapitre 221.**