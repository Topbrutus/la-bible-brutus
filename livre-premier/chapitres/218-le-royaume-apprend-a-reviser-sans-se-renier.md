# Chapitre 218 — Le Royaume apprend à réviser sans se renier

Le Royaume avait appris à corriger des résultats.

À invalider des cristaux.

À renforcer des preuves.

À retirer l’autorité d’une règle.

À refroidir certaines traces.

À laisser partir certains objets.

Mais tout cela restait encore dispersé.

Des corrections ici.

Des révisions là.

Une policy remplacée.

Une stratégie resserrée.

Un cristal réévalué.

Une porte renforcée.

Gabriel regardait maintenant une carte qui racontait plusieurs vérités en même temps.

Ancien workflow.

Nouvelle règle.

Vieille preuve.

Nouveau certificat.

Ancienne classification.

Nouveau scope.

Rien n’était entièrement faux.

Rien n’était entièrement intact.

Le Royaume changeait.

Mais il lui manquait une manière simple de dire :

**voilà ce que nous pensions avant, voilà ce que nous pensons maintenant, et voilà pourquoi les deux appartiennent à la même histoire.**

Gabriel regarda Astra.

— Là, c’est pas juste corriger des affaires. Faut apprendre à changer sans faire semblant qu’on a jamais pensé autrement.

Astra approuva.

Voilà.

Il écrivit :

**RÉVISER ≠ RÉÉCRIRE LE PASSÉ**

Astra approuva fortement.

Puis :

**SE CORRIGER ≠ SE RENIER**

Très important.

Le mot **renier** était central.

Parce qu’un système qui change peut tomber dans deux extrêmes.

Premier extrême :

s’accrocher à l’ancien pour rester cohérent.

Deuxième :

remplacer l’ancien et prétendre qu’il n’a jamais existé.

Les deux sont mauvais.

Gabriel écrivit :

**LA COHÉRENCE NE CONSISTE PAS À NE JAMAIS CHANGER. ELLE CONSISTE À POUVOIR EXPLIQUER LE CHEMIN ENTRE DEUX ÉTATS.**

Astra approuva fortement.

Voilà le cœur.

Ils prirent un premier cas.

### POLICY-218-A

Old:

`MEMORY_FIRST`

New:

`MEMORY_FIRST_UNLESS_TRIVIAL_COMPUTE_IS_CHEAPER`

La vieille policy n’était pas forcément fausse.

Elle avait été utile.

Mais les coûts avaient changé.

Les workflows aussi.

Le nouveau système n’avait pas besoin de dire :

« ancienne policy = erreur ».

Il pouvait dire :

**superseded due changed cost structure and accumulated evidence.**

Gabriel écrivit :

### REVISION RECORD

**object**

**previous_version**

**new_version**

**what_changed**

**why**

**what_remains_valid**

**what no longer applies**

**evidence**

**authority**

Très propre.

Le champ le plus important était peut-être :

**what remains valid.**

Parce qu’une révision ne détruit pas nécessairement tout.

Il écrit :

**UNE BONNE RÉVISION DIT AUSSI CE QU’ELLE NE CHANGE PAS.**

Astra approuva fortement.

Magnifique.

Dans POLICY-218-A :

What remains valid:

- memory lookup still useful;
- historical failure patterns still valuable;
- exact existing result should still be reused.

What changed:

- memory lookup no longer mandatory before trivial cheap computation.

Voilà.

La continuité devenait visible.

Puis un autre cas.

### CLAIM-218-B

Old claim:

structure persists in tested range.

New evidence:

structure persists only in subset S.

Révision :

scope narrowed.

Le vieux résultat n’est pas entièrement faux.

Il était trop large.

Ils écrivirent :

**REVISED_SCOPE**

Pas :

deleted claim.

Gabriel sourit.

Le nouveau claim pointe vers l’ancien.

On peut voir :

version 1.

version 2.

reason.

Très propre.

Il écrit :

**UNE CONCLUSION PEUT ÊTRE RÉVISÉE PAR RÉDUCTION DE SCOPE SANS ÊTRE EFFACÉE DE L’HISTOIRE.**

Astra approuva fortement.

Puis un cas plus fort.

Old claim false.

New claim opposite.

Là,

oui,

invalidation.

Mais même ici,

le Royaume ne renie pas le fait que l’ancien claim avait été accepté.

Il documente.

Très important.

Gabriel écrit :

**RECONNAÎTRE QU’UNE ANCIENNE CONCLUSION ÉTAIT FAUSSE N’OBLIGE PAS À PRÉTENDRE QU’ELLE N’A JAMAIS ÉTÉ CRUE.**

Astra approuva fortement.

Voilà.

Puis une vieille stratégie.

Old strategy:

A then B.

New:

B then A.

Why?

Cost structure changed.

Outcome quality improved in pilot.

Again.

Revision, not shame.

Puis ils créèrent plusieurs types de révision.

### REVISION TYPES

**SCOPE NARROWING**

Le claim devient plus étroit.

**SCOPE EXPANSION**

Le claim s’élargit après nouvelles preuves.

**AUTHORITY CHANGE**

Règle conserve son sens mais change de pouvoir.

**EVIDENCE UPGRADE**

Même claim, preuve renforcée.

**METHOD CHANGE**

Même objectif, meilleure méthode.

**STATUS CHANGE**

Observed → validated, active → contested, etc.

**CORRECTION**

Ancien contenu réellement faux.

**SUPERSESSION**

Nouveau objet devient référence active.

Gabriel approuva.

Très propre.

Toutes ces choses étaient différentes.

Le mot « révision » les couvrait sans les confondre.

Puis un autre danger.

Versioning trop simple.

v1, v2, v3.

Ça dit l’ordre.

Pas le sens.

Il faut aussi changement sémantique.

Gabriel écrit :

**LE NUMÉRO DE VERSION DIT QU’UN OBJET A CHANGÉ. LE JOURNAL DE RÉVISION DIT POURQUOI.**

Astra approuva fortement.

Très important.

Puis une règle :

### NO SILENT SEMANTIC CHANGE

Si le sens change,

new version required.

Pas modifier même ID comme si rien n’était arrivé.

Très important.

Un texte peut être corrigé pour typo sans changer version sémantique.

Mais scope, authority, conditions?

Version.

Gabriel sourit.

Cela protégeait l’histoire.

Puis un autre cas.

Une formule.

Same mathematical relation.

Notation change only.

No semantic revision.

Could be alias/display version.

Très important.

Ne pas créer faux changement scientifique.

Il écrit :

**CHANGER LA NOTATION N’EST PAS CHANGER LA FORMULE.**

Astra approuva fortement.

Évident mais essentiel.

Puis une implementation change.

Same algorithm.

Faster code.

Scientific claim unchanged.

Operational version changed.

Encore deux axes.

Gabriel écrit :

**UNE RÉVISION TECHNIQUE ET UNE RÉVISION ÉPISTÉMIQUE NE SONT PAS LA MÊME CHOSE.**

Astra approuva fortement.

Très important.

Ils créèrent :

### VERSION DIMENSIONS

**CONTENT VERSION**

**IMPLEMENTATION VERSION**

**EVIDENCE VERSION**

**POLICY VERSION**

**PUBLICATION VERSION**

Excellent.

Un même cristal peut garder content v1

mais recevoir evidence certificate v3.

Comme chapitre 217.

Très propre.

Puis un autre problème.

Le public peut voir une ancienne version.

Le système interne en utilise une nouvelle.

Need current pointer.

### CURRENT POINTER

`current_version = v3`

Historical versions accessible.

No ambiguity.

Gabriel sourit.

Simple.

Puis un old link.

If someone opens v1,

show:

**SUPERSEDED BY v3**

not redirect silently.

Very important.

He writes:

**UN ANCIEN LIEN DOIT POUVOIR MONTRER L’ANCIEN ÉTAT ET INDIQUER LE NOUVEAU, PAS EFFACER LE PREMIER SOUS LES PIEDS DU LECTEUR.**

Astra approuva fortement.

Excellent.

Then a difficult question.

What if new version is worse?

Revision itself must be reversible.

Exactly.

They created:

### REVISION ROLLBACK

If new policy performs worse or causes unexpected failure:

- disable v2;
- restore v1 authority if still valid;
- preserve failed revision as history;
- record reason.

Gabriel smiled.

Very important.

He writes:

**REVENIR À UNE VERSION ANTÉRIEURE N’EST PAS EFFACER LA TENTATIVE DE CHANGEMENT.**

Astra approved strongly.

This is key.

Rollback itself is history.

Then a trial.

RULE-X v1.

v2 narrows scope.

After 20 cases,

v2 causes missed opportunities.

Review.

Maybe v1 too broad.

Could create v3,

not simply pretend v2 never happened.

Great.

Then another issue.

Revision chains can get long.

v1→v2→v3→v4→v5.

Need summaries.

### REVISION SUMMARY

Current state.

Major turning points.

Full history on demand.

Good.

No cognitive overload.

Then a branching history.

Two experimental revisions in parallel.

A and B.

Not linear.

Need DAG.

Gabriel writes:

**L’HISTOIRE D’UNE RÈGLE PEUT ÊTRE UN GRAPHE, PAS SEULEMENT UNE LIGNE.**

Astra approved strongly.

Very important.

Pilot branch.

Then one merges.

Other retired.

Exactly like code.

But semantic.

Then another problem.

Two teams revise same rule differently.

Conflict.

Need reconciliation.

Not overwrite last-write-wins.

Very important.

### REVISION CONFLICT

Two competing successors.

Keep both candidate versions.

Compare.

Choose/synthesize under authority.

Gabriel smiled.

This is disciplined.

Then a human issue.

Gabriel changes his mind.

Does the system treat that as inconsistency?

No.

If explicit.

New preference or delegation.

Old remains historical.

He writes:

**CHANGER D’AVIS EXPLICITEMENT EST PLUS COHÉRENT QUE CONSERVER UNE ANCIENNE DÉCISION QU’ON NE SOUTIENT PLUS.**

Astra approved strongly.

Très important.

Then a scientific one.

A conjecture evolves.

Old wording general.

New wording narrower.

The name may stay.

Need version.

Excellent.

Then publication.

Zenodo record may be immutable in some respects.

New version/new record maybe.

The Bible doesn't need exact mechanics here.

Principle:

public corrections must preserve old public state.

Good.

Then they created:

### REVISION PRINCIPLES

1. preserve old state;
2. explain change;
3. identify unchanged parts;
4. link evidence;
5. version semantics;
6. propagate impact;
7. keep rollback path where possible;
8. never let current view erase history.

Gabriel nodded.

This was the core framework.

Then a more philosophical issue.

Could too much reverence for history slow revision?

Yes.

If every change requires monumental ceremony,

people stop correcting.

Need proportional process.

Gabriel writes:

**LA RÉVISION DOIT ÊTRE ASSEZ RIGOUREUSE POUR RESTER TRAÇABLE ET ASSEZ LÉGÈRE POUR NE PAS DÉCOURAGER LES CORRECTIONS.**

Astra approved strongly.

Excellent.

Typos:

light.

Scoped strategy change:

moderate.

Canonical claim correction:

strong.

Public retraction:

stronger.

Proportionality.

Then another issue.

The system can learn to revise based on evidence.

But cannot revise governance boundaries without proper authority.

Very important.

Gabriel writes:

**LE DROIT DE RÉVISER UN OBJET DÉPEND AUSSI DU TYPE D’OBJET.**

Astra approved strongly.

A Fourmi can update local route.

Cannot revise publication policy.

Great.

Then a revision authority table.

### REVISION AUTHORITY

**local task metadata**

L1.

**strategy candidate**

L1/L2 depending.

**active default rule**

authorized rule gate.

**policy**

human/owner governance.

**canonical claim**

validation + authority.

**public artifact**

publication authority.

Very clean.

Then a new case.

A crystal's status changes from VALIDATED to CONTESTED.

Does content version change?

Maybe not.

Status version/event changes.

Important.

The underlying payload didn't change.

Metadata changed.

So revision events can target metadata.

Gabriel writes:

**TOUT CHANGEMENT IMPORTANT N’EXIGE PAS DE MODIFIER LE CONTENU; PARFOIS, C’EST LE STATUT AUTOUR DU CONTENU QUI DOIT ÊTRE RÉVISÉ.**

Astra approved strongly.

Excellent.

Then a dependency.

If current rule points to claim with status changed,

propagate.

Chapter 202/216.

Again.

Then a revision affects multiple downstream objects.

Need impact preview before commit for high-impact revision.

Very important.

### REVISION IMPACT PREVIEW

Before changing high-authority object:

- dependent rules;
- public claims;
- active workflows;
- open experiments;
- archived references unaffected but noted.

Gabriel smiled.

Like database migration.

Then confirmation.

High impact human gate.

Good.

Then a case.

Revision of a central label only.

Impact mostly UI.

No need scientific review.

Again.

Role-aware.

Then they tested revision system.

### REVISION TRIAL 218-A

20 objects revised:

- 5 scope refinements;
- 4 policy/strategy updates;
- 3 evidence upgrades;
- 2 authority demotions;
- 2 public wording corrections;
- 2 implementation-only changes;
- 2 status changes.

Audit:

all previous states recoverable.

all current states linked to reason.

1 missing impact link discovered.

0 silent semantic overwrites after fix.

Status:

**PASS IN TESTED WORKFLOW**

Gabriel smiled.

Good.

Then they found the missing impact link.

A rule had been narrowed,

but one cached workflow continued under old scope.

Fix:

revision events push to active dependents.

Again.

Then a stronger test.

Rollback one revision.

Current pointer back.

History preserved.

Pass.

Great.

Then branching.

Two candidate policy updates.

Compare.

One chosen.

Other archived.

Pass.

Nice.

Then a conceptual distinction.

Revision isn't always improvement.

Sometimes it's simply adaptation.

Need not claim new version better universally.

Gabriel writes:

**NOUVELLE VERSION ≠ MEILLEURE VERSION DANS TOUS LES CONTEXTES.**

Astra approved strongly.

Very important.

Maybe v2 trades speed for auditability.

Different objective.

Need reason.

Then a case.

Old method is faster.

New method more reproducible.

Which is "better"?

Depends.

Thus revision record should state tradeoff.

Excellent.

### REVISION TRADEOFF

**gains**

**losses**

**changed assumptions**

Very clean.

Then another.

A policy revision can be temporary.

Incident mode.

Then revert.

Version history tracks.

Good.

Then "renier".

What would renier look like technically?

Deleting old rule.

Removing old publication.

Changing timestamp.

Changing original claim text without record.

Replacing authorship.

Pretending old status was always current.

Gabriel frowned.

They wrote:

### REVISION ANTI-PATTERNS

**silent overwrite**

**retroactive relabeling without trace**

**history deletion**

**claim laundering**

**backdated correction**

**status rewriting**

Très important.

A mature system must resist these.

He writes:

**CORRIGER L’HISTOIRE N’EST PAS CORRIGER LE PASSÉ.**

Astra approved strongly.

Beautiful.

You correct current understanding of past events,

not the event record itself.

Then an example.

At T1:

claim status validated.

At T2:

invalidated.

Historical view must say:

T1: validated under knowledge then.

T2: invalidated after defect found.

Not rewrite T1 status to invalidated-at-T1.

Unless it was metadata error.

Very important.

Temporal status from 208.

Again.

Then they formalized:

### BITEMPORAL VIEW

**event-time state**

what was recorded then.

**current-time interpretation**

how we understand it now.

Gabriel smiled.

This was powerful.

A historical object can have:

status_at_T1 = validated.

status_now = invalidated.

No contradiction.

Excellent.

Then public versioning.

Old PDF remains.

Current page links correction.

This is exactly honest revision.

Then another philosophical issue.

Can a system be trusted if it changes often?

Maybe more,

if changes are traceable and evidence-driven.

Stability alone isn't trust.

Gabriel writes:

**LA CONFIANCE NE VIENT PAS DU FAIT QU’UN SYSTÈME NE CHANGE PAS. ELLE PEUT VENIR DU FAIT QU’ON PEUT VOIR COMMENT ET POURQUOI IL CHANGE.**

Astra approved strongly.

Voilà.

Then a rule:

No revision without reason.

But reason can be simple.

`cost profile changed`.

`new counterexample`.

`operator policy change`.

Good.

Then no reason like:

"improved".

Too vague.

Need observable basis.

Very important.

Then they created revision quality checks.

### REVISION CHECK

- target identified;
- old state preserved;
- new state explicit;
- reason testable or governance-explicit;
- authority valid;
- impact considered;
- lineage linked.

Great.

Then a case where new evidence is ambiguous.

Don't revise fully yet.

Maybe `CONTESTED`.

Gabriel writes:

**L’INCERTITUDE PEUT JUSTIFIER UNE SUSPENSION OU UN STATUT CONTESTÉ AVANT DE JUSTIFIER UNE RÉVISION DÉFINITIVE.**

Astra approved strongly.

Very important.

No premature correction.

Then a case where old claim partly survives.

Split.

One claim becomes two.

Excellent.

### CLAIM SPLIT

Old C.

New C1 valid in S1.

C2 unsupported in S2.

This is revision by decomposition.

Gabriel smiled.

Very useful.

Then merge.

Two redundant rules become one.

History links both parents.

Also valid.

The revision graph is flexible.

Then a model.

### REVISION OPERATIONS

**replace**

**narrow**

**expand**

**split**

**merge**

**suspend**

**revoke**

**reinstate**

**augment**

**reinterpret**

Gabriel approved.

Very complete.

Then a future issue.

Can an invalidated rule be reinstated?

Yes,

if cause removed and new evidence supports.

But not by deleting invalidation.

New revision.

Very important.

He writes:

**RÉHABILITER N’EFFACE PAS L’ÉPISODE OÙ L’OBJET AVAIT PERDU SON AUTORITÉ.**

Astra approved strongly.

Excellent.

Then they looked at CRYSTO.

A relation candidate gets refined.

Same.

Papillon.

Benchmark repeated on new environment.

Could create v2 evidence.

Pell.

A bounded negative result later supplemented by witness outside bound.

Old remains valid.

Revision of interpretation only if someone overstated.

ZEL.

Protocol version changes.

Old audio remains old protocol.

Everything fits.

Then Gabriel realized the architecture now had something like constitutional continuity.

Not because rules never changed.

Because change itself had rules.

He wrote:

**UN SYSTÈME DEVIENT COHÉRENT QUAND IL A UNE MÉTHODE POUR CHANGER SES PROPRES MÉTHODES.**

Astra approved strongly.

Strong line.

But carefully:

not unrestricted self-change.

Within authority.

So he added:

**ET CETTE MÉTHODE DOIT ELLE-MÊME RESTER SOUS AUTORITÉ ET TRACE.**

Astra approved strongly.

Perfect.

Then a dangerous recursion.

Who revises revision policy?

Higher governance/human.

Not automatic infinite regress.

Good.

Then one last trial.

A central workflow strategy revised.

Impact preview shows 12 active tasks.

3 unaffected.

6 migrate.

3 should finish old version.

System handles.

No history loss.

Great.

Then current dashboard.

Click policy.

See:

v1 original.

v2 cost exception.

v3 scope refinement.

Each with evidence.

No confusion.

Gabriel smiled.

This was the opposite of reniement.

The system didn't say:

"we were always right."

It said:

"we were here,

then we learned this,

then we changed this."

That was stronger.

He wrote:

**LA MATURITÉ N’EST PAS DE PRÉTENDRE QUE LE PASSÉ ÉTAIT PARFAIT. C’EST DE POUVOIR MONTRER CE QUE LE PRÉSENT A APPRIS DU PASSÉ SANS L’EFFACER.**

Astra approved strongly.

Voilà le chapter.

Then something new happened.

One revision was not triggered by Gabriel.

Not directly.

A policy candidate emerged because several validated traces,

multiple workflow outcomes,

and repeated operator corrections all pointed in the same direction.

The system did not activate it.

But it proposed:

**POLICY CHANGE CANDIDATE**

Gabriel stared.

— Ah.

This was different.

Until now,

evidence changed claims,

strategies,

rules.

But now the accumulated evidence was proposing a **policy change**.

Not a route.

Not a local heuristic.

A policy.

That required more authority.

More care.

But it was exactly where the arc was heading.

The Kingdom had learned to revise without renouncing itself.

Now it was about to ask whether the evidence itself could justify changing the rules by which future work was governed.

Gabriel wrote the last line:

**LE ROYAUME AVAIT APPRIS À RÉVISER SON PRÉSENT SANS EFFACER SON PASSÉ.**

Then:

**IL RESTAIT À VOIR SI UNE RÉVISION POUVAIT, POUR LA PREMIÈRE FOIS, MONTER JUSQU’AU NIVEAU D’UNE POLITIQUE.**

**Fin du chapitre 218.**