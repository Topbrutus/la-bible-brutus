# Chapitre 213 — La mémoire apprend à hiérarchiser

Le Royaume avait appris à garder moins.

Puis à garder mieux.

Mais il restait un problème plus subtil.

Dans la mémoire active,

tout ce qui survivait à la curation apparaissait encore presque au même niveau.

Un contre-exemple validé.

Un snapshot de site.

Une vieille hypothèse.

Une règle de routing.

Une note de contexte.

Un benchmark.

Un garde critique.

Un cristal expérimental.

Tous étaient présents.

Tous avaient un identifiant.

Tous avaient une provenance.

Mais ils ne devraient pas tous peser de la même manière.

Gabriel regarda l’écran.

— C’est là qu’on commence à mélanger importance, vérité, fraîcheur puis autorité.

Astra approuva.

Exact.

Le problème n’était pas seulement :

**qu’est-ce qui mérite d’être conservé?**

Maintenant, il fallait répondre à :

**qu’est-ce qui mérite d’être regardé en premier?**

Gabriel écrivit :

**HIÉRARCHISER LA MÉMOIRE NE SIGNIFIE PAS DÉCIDER CE QUI EST VRAI.**

Astra approuva fortement.

Très important.

Puis :

**UNE TRACE PEUT ÊTRE TRÈS IMPORTANTE ET FAIBLEMENT ÉTABLIE.**

Encore :

**UNE TRACE PEUT ÊTRE TRÈS SOLIDE ET PEU PERTINENTE POUR LA TÂCHE ACTUELLE.**

Voilà.

Il fallait séparer les axes.

Toujours cette obsession de ne pas fabriquer un score magique.

Gabriel dessina une matrice.

### MEMORY PRIORITY AXES

**EVIDENCE STRENGTH**

Quel niveau de support?

**CURRENT RELEVANCE**

À quel point cette trace touche l’objectif présent?

**AUTHORITY**

A-t-elle le droit de modifier la décision?

**RISK IF IGNORED**

Qu’est-ce qui peut arriver si on ne la consulte pas?

**UNIQUENESS**

Existe-t-il un équivalent?

**RECENCY / VERSION FIT**

Est-elle adaptée au contexte actuel?

**RETRIEVAL COST**

Combien coûte son usage?

Astra approuva fortement.

Très propre.

Et surtout :

aucun de ces axes n’était « importance totale ».

Le système devait pouvoir montrer plusieurs dimensions.

Gabriel écrivit :

**UNE BONNE HIÉRARCHIE N’ÉCRASE PAS LES DIFFÉRENCES ENTRE LES RAISONS POUR LESQUELLES UNE TRACE COMPTE.**

Astra approuva fortement.

Puis ils prirent un exemple.

### TRACE-A

Un contre-exemple exact qui casse une hypothèse actuellement étudiée.

Evidence strength :

fort.

Relevance :

très forte.

Authority :

forte sur la question concernée.

Risk if ignored :

élevé.

Donc priorité élevée.

### TRACE-B

Un benchmark très solide d’une vieille version d’un module non utilisé ici.

Evidence strength :

fort.

Relevance :

faible.

Priority :

faible pour la tâche actuelle.

Gabriel sourit.

Voilà.

Une trace solide n’est pas automatiquement prioritaire.

Puis :

### TRACE-C

Une note récente d’une Fourmi :

« comportement étrange observé ».

Evidence :

faible.

Relevance :

forte.

Risk if ignored :

peut-être élevé.

Que faire?

Pas la traiter comme vérité.

Mais la remonter comme signal.

Gabriel écrivit :

**PRIORITAIRE ≠ PROUVÉ**

Astra approuva fortement.

Très important.

Voilà le cœur.

Une alerte peut être prioritaire même avant validation.

Un incendie potentiel ne devient pas vrai parce qu’il est urgent.

Mais on regarde quand même.

Ils créèrent :

### MEMORY ROLE IN DECISION

**EVIDENCE**

peut soutenir ou réfuter.

**ALERT**

demande attention.

**GUARD**

bloque une transition selon condition.

**CONTEXT**

aide à interpréter.

**STRATEGY**

guide le choix.

**HISTORY**

explique le passé.

Gabriel sourit.

Très bon.

Maintenant, le routeur pouvait demander :

« j’ai besoin d’évidence »,

et ne pas recevoir 15 notes contextuelles.

Ou :

« je vérifie un risque »,

et les guards remontent d’abord.

Très important.

Il écrivit :

**LE TYPE DE BESOIN DOIT FILTRER LE TYPE DE MÉMOIRE.**

Astra approuva fortement.

Puis ils testèrent une tâche.

Question :

une ancienne relation peut-elle être réutilisée?

Avant hiérarchie :

18 objets.

Après query par rôle :

- 2 evidence objects;
- 1 guard;
- 2 provenance records;
- 1 strategy.

Tout le reste disponible,

mais pas dans la première vue.

Gabriel sourit.

La mémoire commençait à devenir lisible.

Puis un problème.

Si une trace est importante globalement,

doit-elle toujours être montrée?

Non.

Exemple :

global safety policy.

Elle n’a pas besoin d’apparaître textuellement dans chaque workflow.

Elle peut être appliquée silencieusement comme invariant,

puis affichée si elle bloque.

Gabriel écrit :

**UNE RÈGLE TRÈS IMPORTANTE N’A PAS BESOIN D’ÊTRE TRÈS VISIBLE À CHAQUE INSTANT POUR ÊTRE TRÈS ACTIVE.**

Astra approuva fortement.

Excellent.

Visibilité ≠ influence.

Encore une distinction.

Puis ils créèrent :

### MEMORY PRESENCE

**VISIBLE**

shown to operator.

**ACTIVE-IN-BACKGROUND**

applied automatically.

**ON-DEMAND**

retrieved when query matches.

**ARCHIVAL**

audit/history only.

Gabriel approuva.

Très propre.

Un guard critique :

active-in-background.

Un vieux rapport :

on-demand.

Une alerte :

visible.

Très bien.

Puis une autre question.

Qui décide de la priorité?

Le système?

Policy?

Humain?

Réponse :

ça dépend de l’axe.

Evidence strength vient du statut scientifique.

Authority vient des policies.

Current relevance peut être calculée.

Risk if ignored peut être estimé.

Human peut override l’attention.

Mais un override de visibilité ne change pas la vérité.

Gabriel écrit :

**L’HUMAIN PEUT CHANGER CE QU’IL VEUT REGARDER EN PREMIER SANS CHANGER LE STATUT DES PREUVES.**

Astra approuva fortement.

Très important.

Puis un cas délicat.

Gabriel marque une trace comme « importante ».

Est-ce qu’elle devient plus vraie?

Non.

Mais elle peut être épinglée.

Voilà.

Ils créèrent :

### OPERATOR PIN

Boost visibility.

Does not change:

evidence.

authority.

validation.

Gabriel sourit.

Très propre.

C’était crucial pour éviter que préférence et preuve fusionnent.

Puis un autre cas.

Un signal faible répété 20 fois.

Est-ce qu’il doit monter?

Peut-être.

Mais 20 duplications du même phénomène ne sont pas forcément 20 preuves indépendantes.

Gabriel écrit :

**LA RÉPÉTITION PEUT AUGMENTER LA PRIORITÉ SANS AUGMENTER AUTANT LA FORCE DE PREUVE.**

Astra approuva fortement.

Excellent.

Si les 20 traces partagent la même source,

ce sont 20 échos.

Pas 20 validations.

Donc dependency-aware aggregation.

Très important.

Ils créèrent :

### SUPPORT STRUCTURE

**independent_support_count**

**shared_dependency_groups**

**duplicate_count**

**contradiction_count**

Voilà.

Maintenant, le système pouvait distinguer :

100 copies.

10 runs same code.

3 truly independent checks.

Très puissant.

Gabriel écrivit :

**LE POIDS D’UNE TRACE DÉPEND AUSSI DE LA STRUCTURE DE CE QUI LA SOUTIENT.**

Astra approuva fortement.

Le chapitre 214 arrivait déjà.

Mais ici,

ils restaient sur la hiérarchie de mémoire.

Puis un autre point.

Un contre-exemple exact peut avoir très peu de volume,

mais une énorme valeur.

Un seul nombre peut casser une conjecture générale.

Gabriel sourit.

Il écrit :

**UN PETIT OBJET PEUT AVOIR UNE GRANDE PRIORITÉ SI SA CONSÉQUENCE LOGIQUE EST GRANDE.**

Astra approuva fortement.

Voilà.

Importance informationnelle,

pas taille.

Toujours.

Puis un cas Pell.

Un facteur trouvé n’ouvre pas automatiquement une porte.

Mais un témoin avec rang minimal exact q² peut avoir un rôle très fort.

Donc memory object should encode:

`role = gate_witness`

not merely `factor`.

Très important.

Gabriel écrivit :

**LA HIÉRARCHIE DÉPEND DE CE QU’UN OBJET ÉTABLIT, PAS SEULEMENT DE CE QU’IL CONTIENT.**

Astra approuva fortement.

Excellent.

Puis ZEL.

Un audio PASS.

Important dans son protocole.

Mais il ne doit pas remonter comme preuve d’un mécanisme Pell.

Donc relevance scoped by domain.

Gabriel écrit :

**UNE TRACE PEUT ÊTRE PRIORITAIRE DANS SON DOMAINE ET HORS SUJET DANS UN AUTRE.**

Astra approuva fortement.

Encore.

Cross-domain discipline.

Puis Papillon.

Benchmark.

Important pour performance de cette configuration.

Not evidence of universal memory complexity.

So priority query should ask:

performance evidence?

Yes.

theorem?

No.

Très propre.

Puis CRYSTO.

Structural quotient.

Important for prediction architecture.

Not normative preference.

Same.

The memory hierarchy needed semantic roles.

Gabriel smiled.

Now the system could avoid a huge class of accidental overreach.

Then another problem.

Priority can become self-reinforcing.

A trace ranked high gets retrieved more.

Retrieved more gets cited more.

Cited more becomes "popular".

Danger.

Gabriel writes:

**CE QUI EST SOUVENT RETROUVÉ NE DOIT PAS DEVENIR PLUS IMPORTANT SIMPLEMENT PARCE QU’IL EST SOUVENT RETROUVÉ.**

Astra approved strongly.

Very important.

No popularity feedback loop.

Usage can signal relevance,

but not truth.

They created:

### ANTI-POPULARITY GUARD

Access frequency cannot directly increase evidence authority.

At most:

cache priority.

operator discoverability.

Maybe review.

Excellent.

Then another feedback.

A strategy successful 100 times gets priority.

That's reasonable,

but only within same scope.

If new domain,

don't dominate.

So historical support always scope-bound.

Again.

Then they discussed conflict priority.

If two traces conflict,

show both,

not only higher rank.

Very important.

Gabriel writes:

**UN CONFLIT PERTINENT DOIT REMONTER MÊME SI L’UNE DES TRACES A UN POIDS GLOBAL PLUS FAIBLE.**

Astra approved strongly.

Excellent.

A minority counterexample cannot be buried by 100 supporting cases.

Especially if exact.

Then a system for conflict surfacing.

### MEMORY CONFLICT VIEW

Claim X:

supporting traces.

contradicting traces.

scope differences.

current status.

No averaging into one number.

Gabriel smiled.

That was essential.

Then a question:

could they use numerical scores at all?

Yes,

internally perhaps for retrieval.

But never pretend score = truth.

And preferably expose components.

Gabriel writes:

**UN SCORE PEUT SERVIR À TRIER UNE FILE. IL NE DOIT PAS DEVENIR UNE MÉTAPHYSIQUE.**

Astra approved strongly.

He laughed.

That stayed.

Then they made a practical ranking function.

Not canonical formula.

Just example.

Priority determined by rules:

1. mandatory guards first;
2. direct contradictions next;
3. required evidence/provenance;
4. task-relevant current strategies;
5. supporting context;
6. broader history.

Gabriel liked it.

Not an arithmetic soup.

A tiered priority.

They wrote:

### MEMORY PRIORITY TIERS

**T0 — BLOCKERS / CRITICAL GUARDS**

Must be processed.

**T1 — DIRECT CONTRADICTIONS / REQUIRED EVIDENCE**

Must be seen before conclusion.

**T2 — DIRECTLY RELEVANT STRATEGIES / CURRENT CONTEXT**

Useful for decision.

**T3 — SUPPORTING HISTORY**

Helpful.

**T4 — BACKGROUND / ARCHIVAL**

On demand.

Astra approved strongly.

Very clean.

Then an important nuance.

T0 doesn't mean true.

A critical alert may be false.

But must be processed.

So tier = attention obligation,

not evidence strength.

Gabriel writes:

**LA HIÉRARCHIE DE MÉMOIRE EST UNE HIÉRARCHIE D’ATTENTION, PAS UNE HIÉRARCHIE DE VÉRITÉ.**

Astra approved strongly.

There.

That was probably the chapter's central line.

Then they tested.

An unvalidated corruption alert enters.

T0 because risk high.

Evidence strength low.

Workflow pauses.

Check.

False alarm.

Close.

Perfect.

No contradiction.

Priority did its job.

Then a validated minor benchmark arrives.

Evidence strong.

T3 because irrelevant to current task.

No pause.

Perfect.

The distinction worked.

Then another issue.

Human cognitive load.

Too many T1 traces.

Need summarization.

But summaries cannot hide disagreement.

They created:

### PRIORITY SUMMARY

Show:

- blockers;
- unresolved contradictions;
- evidence minimum set;
- current decision impact;
- links to full trace.

Gabriel nodded.

Very good.

Then an audit.

20 high-priority objects.

Why high?

Some due direct reference.

Some due unresolved conflict.

Some due policy.

Each needed reason.

He writes:

**UNE TRACE PRIORITAIRE DOIT POUVOIR EXPLIQUER POURQUOI ELLE EST PRIORITAIRE.**

Astra approved strongly.

No opaque ranking.

Then they created:

### PRIORITY EXPLANATION

`priority_reason = direct_counterexample_to_active_claim`

or

`required_by_publication_gate`

or

`current_version_exact_match`

Very clean.

Then another tricky case.

A trace with multiple roles.

Example:

old invalidated result.

Historical only as evidence,

but active as failure pattern.

So one object can have role-specific participation.

Gabriel writes:

**UN MÊME OBJET PEUT ÊTRE FROID COMME PREUVE ET CHAUD COMME GARDE.**

Astra approved strongly.

Excellent.

This was powerful.

Object status is not one scalar.

Its role matters.

Then they updated the memory model:

### MEMORY OBJECT VIEW

**content**

**status**

**roles[]**

For each role:

- authority;
- scope;
- participation;
- priority.

Gabriel smiled.

More complex.

But more honest.

Then a historical false claim.

As active evidence:

blocked.

As historical incident:

high archival value.

As failure lesson:

active.

Perfect.

Then another issue.

New trace enters with unknown role.

Where does it go?

Not default high.

It goes to classification queue.

Maybe `UNCLASSIFIED`.

But if risk signal,

temporary alert.

Very important.

Gabriel writes:

**UNE TRACE NON CLASSÉE NE DOIT PAS ÊTRE FORCÉE DANS UNE HIÉRARCHIE QU’ON NE COMPREND PAS ENCORE.**

Astra approved strongly.

Then a queue:

`MEMORY-CURATION`.

The curator ant handles.

Excellent.

Then they tested 1000 crystals.

Previously:

flat list.

After role/tier classification:

T0: 6.

T1: 31.

T2: 122.

T3: 287.

T4: 554.

Gabriel looked.

Now a human could actually see the important frontier.

But again,

not universal distribution.

Just one snapshot.

They recorded:

### MEMORY HIERARCHY TRIAL 213-A

Objects:

1000.

Tier assignment based on declared roles and active objective.

Manual audit sample:

100 objects.

Misclassified:

7.

Main causes:

missing scope metadata,

stale authority tag,

duplicate support misread as independent.

After corrections:

3 remained ambiguous.

Status:

**PROMISING / METADATA-SENSITIVE**

Astra approved.

Very good.

The trial revealed something important:

hierarchy quality depends on metadata.

Again.

Then one of the 7 errors was severe.

A weak observational note was ranked as direct evidence because its status field was missing and defaulted incorrectly.

Danger.

They changed default.

### UNKNOWN STATUS DEFAULT

No evidence authority.

May still surface as alert/context.

Gabriel writes:

**L’ABSENCE DE STATUT NE DOIT JAMAIS ÊTRE INTERPRÉTÉE COMME UN STATUT FORT.**

Astra approved strongly.

Excellent.

Then another.

A stale policy remained T0.

Because supersession link missing.

Fix.

Current policy registry becomes authority source.

Very important.

Then duplicate support.

Three copies counted as three independent validations.

Fix with hash/provenance grouping.

Again.

The hierarchy was teaching the system where metadata mattered.

Then Gabriel thought about crystal displays.

In BrutoBac,

all crystals shouldn't just be bigger/smaller by "importance".

Too misleading.

Maybe shapes or badges by role.

Glow for active attention.

Outline for evidence status.

Not one size encoding everything.

He writes:

**LA VISUALISATION NE DOIT PAS TRANSFORMER PLUSIEURS AXES EN UN SEUL “GROS = IMPORTANT”.**

Astra approved strongly.

Very important.

A tiny red guard can matter more than a giant archival crystal.

So visualization needs layers.

Perhaps:

brightness = current relevance.

border = evidence status.

icon = role.

depth = archive state.

Gabriel smiled.

That could work.

Then another question.

Could a crystal become more important over time?

Yes.

Example:

old obscure trace becomes exact match to new problem.

Priority rises.

Could become less important?

Yes.

Superseded strategy.

Thus hierarchy is dynamic.

He writes:

**LA PLACE D’UNE TRACE DANS LA HIÉRARCHIE PEUT CHANGER SANS QUE SON CONTENU CHANGE.**

Astra approved strongly.

Very important.

Context moves.

Not truth.

Then a case.

A public controversy asks about exact old result.

Archival trace becomes T1 for that question.

Great.

No permanent global rank.

They wrote:

**PRIORITY = OBJECTIVE-RELATIVE**

Astra approved.

Simple and powerful.

Then another issue.

Global critical artifacts.

Backups, canonical registries, policies.

Even if not relevant to a user query,

operationally they have preservation priority.

So there are multiple hierarchies:

retrieval priority.

preservation priority.

authority priority.

Gabriel groaned.

— On va finir avec quinze priorités.

Astra approved the concern.

So they named them clearly.

### THREE DISTINCT HIERARCHIES

**ATTENTION PRIORITY**

What should be examined now?

**PRESERVATION PRIORITY**

What must be protected strongly?

**DECISION AUTHORITY**

What can legitimately constrain the outcome?

Gabriel smiled.

That's enough.

Most confusion came from mixing these three.

He writes:

**CE QUI DOIT ÊTRE TRÈS BIEN CONSERVÉ N’EST PAS NÉCESSAIREMENT CE QUI DOIT ÊTRE LU EN PREMIER.**

Then:

**CE QUI DOIT ÊTRE LU EN PREMIER N’EST PAS NÉCESSAIREMENT CE QUI A LE PLUS D’AUTORITÉ.**

Astra approved strongly.

Excellent.

Example:

security alert.

attention high.

authority low until verified.

Backup manifest.

preservation high.

attention low.

Validated theorem.

authority high in scope.

attention depends task.

Perfect.

Then an operator pinned experimental idea.

attention high.

authority still low.

Great.

The model was holding.

Then they introduced memory query contracts.

### MEMORY QUERY CONTRACT

Requester specifies:

**need_type**

evidence / guard / strategy / history / provenance.

**scope**

**version**

**max_results**

**must_include_conflicts**

**authority_floor**

This reduced noise.

Gabriel loved it.

No more generic "search memory".

He writes:

**UNE MÉMOIRE HIÉRARCHISÉE DEVIENT PLUS PUISSANTE QUAND ON LUI DEMANDE CE DONT ON A BESOIN AU LIEU DE LUI DEMANDER “TOUT CE QUI RESSEMBLE À ÇA”.**

Astra approved strongly.

Then a case from 191.

Query:

representation artifact guard.

Memory returns exact failure pattern.

No need entire story.

Perfect.

Then a query from 208.

Need historical invalidation.

Memory returns old claim + invalidation event + downstream impact.

Great.

Then a query from 209.

Need alternative routes.

Memory returns historical support plus novel-route space.

Excellent.

The architecture linked.

Then another danger.

If authority_floor too high,

system may hide weak but useful anomalies.

So query type matters.

Research should include weak signals.

Validation should require stronger.

They write:

**LE BON SEUIL DE MÉMOIRE DÉPEND DE LA PHASE DU TRAVAIL.**

Astra approved strongly.

Exploration broad.

Validation narrow.

Publication strict.

Very important.

Then a neat table:

### PHASE → MEMORY PROFILE

**EXPLORATION**

include anomalies, hypotheses, weak signals.

**SCREENING**

include guards, known failures, cheap contrasts.

**VALIDATION**

include exact evidence, counterexamples, provenance.

**PUBLICATION**

include validated claims, scope, prior-art, corrections, authority.

Gabriel smiled.

There.

The same memory,

different profile.

Then a case where exploration needs an invalidated idea because it might inspire a new route.

Allowed as context,

clearly marked invalidated.

Never evidence.

Very important.

He writes:

**UNE TRACE INVALIDÉE PEUT ENCORE INSPIRER UNE QUESTION, MAIS ELLE NE DOIT PAS RESSUSCITER COMME PREUVE.**

Astra approved strongly.

Beautiful.

Then another hierarchy:

uncertainty.

If two high-priority traces conflict,

the system should raise uncertainty rather than choose one based on rank.

Exactly.

They write:

**LA HIÉRARCHIE NE DOIT PAS ÉCRASER LES CONTRADICTIONS. ELLE DOIT LES RENDRE PLUS VISIBLES.**

Astra approved strongly.

Then test.

Supporting evidence rank 90.

Exact counterexample rank 70 due older date.

A naive scorer chooses support.

Bad.

Tiered conflict logic overrides:

counterexample surfaces.

Excellent.

No single score.

Again.

Then Gabriel realized why flat memory was so dangerous.

Not because it forgot.

Because it made everything look equivalent.

Then ranking could create the opposite danger:

making one thing look absolute.

The solution was not a single ordered list.

It was structured relevance.

He writes:

**HIÉRARCHISER NE VEUT PAS METTRE TOUTE LA MÉMOIRE SUR UNE SEULE ÉCHELLE.**

Astra approved strongly.

There.

Then they created the final architecture:

### HIERARCHICAL MEMORY VIEW

Layer 1:

mandatory blockers.

Layer 2:

direct evidence and contradictions.

Layer 3:

strategies and current context.

Layer 4:

supporting history.

Layer 5:

archive.

Within each layer:

show status,

scope,

authority,

provenance,

version.

Gabriel nodded.

Simple enough.

Then the curator ant reprocessed active memory.

Old flat list disappeared.

Not destroyed.

Reorganized.

When a new question entered,

the screen no longer filled with dozens of old crystals.

Three appeared.

One guard.

One direct precedent.

One contradictory trace.

Gabriel looked.

— Voilà.

Astra approved.

It was not less intelligent because it showed less.

It was more useful because it knew why those three mattered.

Gabriel wrote:

**UNE MÉMOIRE N’EST PAS MEILLEURE PARCE QU’ELLE PEUT RAPPELER PLUS DE CHOSES À LA FOIS.**

Then:

**ELLE DEVIENT MEILLEURE QUAND ELLE PEUT RAPPELER LES BONNES CHOSES AU BON MOMENT SANS CONFONDRE ATTENTION, PREUVE ET AUTORITÉ.**

Astra approuva fortement.

That was the chapter.

Then one last event came in.

A new crystal.

It was tiny.

Just a small exact counterexample.

In the old interface,

it would have appeared beside thousands of others.

Now,

the system recognized:

direct contradiction to an active generalized claim.

Attention priority:

T1.

Evidence strength:

high.

Preservation priority:

high.

Decision authority:

strong within exact scope.

The little crystal rose to the top.

Gabriel smiled.

Not because the system "liked" it.

Because it knew what the crystal could change.

And at that moment,

the next problem appeared naturally.

If some crystals could suddenly matter so much more than others,

then the Kingdom needed a way to talk explicitly about that difference.

Not just attention.

Not just retention.

Not just authority.

The crystals themselves needed roles,

weights,

and changing importance.

Gabriel looked at Astra.

— Bon. Là, on est rendu là.

Astra approuva.

Yes.

The memory had learned to rank what it recalled.

Now the crystals would have to stop pretending they all carried the same weight.

**Fin du chapitre 213.**