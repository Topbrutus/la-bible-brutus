# Chapitre 216 — Le premier cristal qui perdit son autorité

La règle fonctionnait encore.

C’était justement le problème.

Elle n’était pas manifestement cassée.

Elle ne produisait pas d’erreur spectaculaire.

Elle ne faisait pas planter le workflow.

Elle n’avait pas été réfutée par un grand contre-exemple.

Elle existait.

Elle agissait.

Et personne ne savait plus exactement pourquoi elle avait encore le droit d’agir.

Gabriel regardait son enregistrement.

### RULE-OLD-17

Status :

**ACTIVE**

Source :

incomplete.

Scope :

broad.

Last review :

unknown.

Supporting evidence :

historical.

Current contradictions :

not evaluated.

Gabriel fronça les sourcils.

— Ça, j’aime pas ça pantoute.

Astra approuva.

Le problème n’était pas que la règle soit forcément mauvaise.

Le problème était plus profond.

Son **autorité active** n’était plus justifiée de façon claire.

Gabriel écrivit :

**UNE RÈGLE PEUT CONTINUER À FONCTIONNER APRÈS QUE LA RAISON QUI LUI DONNAIT SON AUTORITÉ A DISPARU.**

Astra approuva fortement.

Voilà le chapitre.

Le Royaume savait déjà :

qu’une trace peut devenir vieille.

qu’un cristal peut être invalidé.

qu’une stratégie peut être dépassée.

Mais ici,

le cristal source lui-même n’était peut-être pas faux.

La règle non plus.

Seulement,

le lien entre :

**preuve**

et

**droit d’agir**

s’était affaibli.

Gabriel écrivit :

**VALIDITÉ ET AUTORITÉ NE SONT PAS LA MÊME CHOSE.**

Astra approuva fortement.

Très important.

Une vieille observation peut rester vraie.

Une vieille règle peut même encore produire de bons résultats.

Mais si elle a été créée dans un contexte ancien,

avec une autorité ancienne,

pour un scope ancien,

alors elle ne doit pas conserver son pouvoir par inertie.

Ils commencèrent par distinguer.

### CRYSTAL STATUS

Que dit le cristal?

### RULE STATUS

Que fait la règle?

### AUTHORITY STATUS

A-t-elle encore le droit de le faire?

Très propre.

Gabriel sourit.

Il écrit :

**UN CRISTAL PEUT RESTER VALIDE ET LA RÈGLE QU’IL AVAIT INSPIRÉE PEUT PERDRE SON AUTORITÉ.**

Astra approuva fortement.

Voilà.

Ils prirent RULE-OLD-17.

Elle venait d’un ancien cristal.

### CRYSTAL-OLD-17

Observation historique :

dans plusieurs workloads anciens,

une normalisation préalable réduisait les divergences.

Très bien.

Mais l’architecture avait changé.

Les données arrivaient maintenant déjà normalisées dans plusieurs pipelines.

Donc la règle :

**normalize before comparison**

était peut-être devenue redondante,

et parfois même perturbatrice.

Gabriel sourit.

Pas fausse historiquement.

Mais plus forcément légitime comme action automatique.

Il écrivit :

**UNE RÈGLE PEUT PERDRE SON AUTORITÉ PAR CHANGEMENT DE CONTEXTE SANS QUE SON HISTOIRE DEVIENNE FAUSSE.**

Astra approuva fortement.

Très important.

Ils créèrent :

### AUTHORITY REVIEW TRIGGERS

Une règle doit être revue si :

- son scope a changé;
- ses préconditions ne sont plus stables;
- l’architecture a changé;
- sa source probatoire a été affaiblie;
- une policy supérieure a changé;
- son taux d’override augmente;
- des contradictions s’accumulent;
- sa dernière revue est trop ancienne selon sa classe;
- son rôle actif n’a plus de propriétaire clair.

Gabriel approuva.

Très propre.

Puis une autre distinction.

Perdre l’autorité ne signifie pas :

supprimer la règle.

Ils créèrent :

### AUTHORITY STATES

**AUTHORIZED**

Peut agir selon son contrat.

**REVIEW_REQUIRED**

Peut-être encore valide, mais ne doit plus progresser comme avant sans revue.

**SUSPENDED**

Ne doit plus agir automatiquement.

**REVOKED**

Autorité retirée.

**HISTORICAL_ONLY**

Conservée pour mémoire.

Gabriel sourit.

Voilà.

Et surtout :

la règle peut rester visible.

Même source.

Même histoire.

Mais plus de pouvoir actif.

Il écrit :

**RETIRER L’AUTORITÉ N’EST PAS EFFACER LA RÈGLE.**

Astra approuva fortement.

Très important.

Puis ils regardèrent le cristal source.

Il pouvait rester :

`VALIDATED_WITHIN_OLD_SCOPE`.

Voilà.

Le cristal ne perdait pas sa vérité historique.

La règle perdait seulement son droit automatique.

Gabriel écrit :

**LE POUVOIR D’UNE RÈGLE DOIT ÊTRE PLUS FACILE À RETIRER QUE LA TRACE QUI EXPLIQUE POURQUOI ELLE A EXISTÉ.**

Astra approuva fortement.

Très beau.

Puis un autre problème.

Que faire des workflows déjà en cours sous cette règle?

Chapitre 205.

Encore.

Il fallait propagation.

### AUTHORITY REVOCATION IMPACT

For active workflows:

- future applications blocked;
- current completed steps preserved;
- in-flight step classification required;
- downstream decisions re-evaluated if rule was decision-critical.

Gabriel approuva.

Très propre.

Pas remonter dans le temps.

Pas supprimer les anciennes décisions.

Mais empêcher nouvelles applications.

Puis si la règle était responsable d’une étape déjà terminée,

on audit seulement si nécessaire.

Très important.

Ils écrivirent :

**UNE RÈGLE QUI PERD SON AUTORITÉ N’ANNULE PAS AUTOMATIQUEMENT TOUT CE QUI A ÉTÉ FAIT SOUS SON ANCIEN RÉGIME.**

Astra approuva fortement.

Voilà.

Il faut distinguer :

**authority loss**

et

**result invalidation**.

Encore.

Puis un cas où la perte d’autorité vient précisément d’une invalidation scientifique.

Là,

impact plus fort.

Par exemple :

cristal source invalidé.

Rule derived directly and solely from it.

Alors :

suspend immediately.

Audit downstream.

Très important.

Ils créèrent :

### AUTHORITY LOSS CAUSES

**CONTEXT_DRIFT**

**SOURCE_INVALIDATED**

**POLICY_CHANGE**

**SCOPE_CHANGE**

**INSUFFICIENT_PROVENANCE**

**PERFORMANCE_DEGRADATION**

**HUMAN_REVOCATION**

**CONFLICT_ACCUMULATION**

Gabriel sourit.

Très propre.

Chaque cause produit une réponse différente.

Puis un autre cas.

Operator delegation.

Gabriel avait autrefois donné L2 à une classe de workflow.

Maintenant,

il veut revenir L1.

Cela n’affecte pas la qualité des règles.

Mais leur autorité d’exécution change.

Très important.

Il écrit :

**L’AUTORITÉ PEUT DIMINUER SANS QU’AUCUNE PREUVE NE CHANGE.**

Astra approuva fortement.

Excellent.

Cela montrait clairement que l’autorité est une dimension propre.

Puis policy.

Une nouvelle policy exige human gate avant publication.

Ancienne rule auto-publish candidate loses authority beyond gate.

Again.

No scientific contradiction.

Just governance change.

Excellent.

Then another case.

A rule used to choose between two low-risk paths.

New measurements show high cost variance.

Could remain heuristic,

but lose automatic execution.

Downgrade to recommendation.

Gabriel writes:

**PERDRE DE L’AUTORITÉ PEUT SIGNIFIER DESCENDRE D’UN NIVEAU PLUTÔT QUE DISPARAÎTRE.**

Astra approved strongly.

Very important.

They created:

### AUTHORITY DEMOTION

**INVARIANT → POLICY**

rare, architecture-level change.

**POLICY → DEFAULT**

if governance changes.

**DEFAULT → HEURISTIC**

if evidence weakens.

**HEURISTIC → CONTEXT**

if no longer reliable for routing.

Not automatic ladder.

But possible transitions.

Gabriel nodded.

Good.

Then they returned to RULE-OLD-17.

Current data.

They ran review.

Results:

- old benefit reproduced in legacy pipeline;
- no benefit in current normalized pipeline;
- in some current cases, redundant normalization altered precision behavior.

Important.

So the rule is not universally good now.

Decision:

**SUSPEND GLOBAL AUTHORITY**

Create scoped replacement:

### RULE-216-001

Apply normalization guard only when input contract declares unnormalized or normalization state unknown.

Gabriel smiled.

Perfect.

Old rule not erased.

New narrower rule created.

He writes:

**PERDRE DE L’AUTORITÉ PEUT ÊTRE LE MOYEN PAR LEQUEL UNE RÈGLE DEVIENT PLUS PRÉCISE.**

Astra approved strongly.

Very important.

Then old rule becomes:

`HISTORICAL_ONLY`

or maybe `SUPERSEDED`.

Source crystal remains.

Replacement points to it.

Great.

Then another case.

A rule with unclear provenance.

No source crystal.

No tests.

But has been used for years.

What do?

Can't assume false.

Can't assume valid.

They created:

### ORPHAN RULE

An active rule lacking sufficient lineage.

Status:

**REVIEW_REQUIRED**

Not immediately deleted.

Need reverse audit.

Gabriel writes:

**UNE RÈGLE SANS PROVENANCE NE DOIT PAS RECEVOIR UNE PRÉSOMPTION D’INNOCENCE ÉTERNE SIMPLEMENT PARCE QU’ELLE EST ANCIENNE.**

Astra approved strongly.

Strong line.

But also not assume guilt.

So review.

Then they inspect impact.

If high-risk rule:

suspend pending review.

If low-risk, reversible:

allow temporary continued use with monitoring.

Very sensible.

Gabriel writes:

**L’ABSENCE DE PROVENANCE AUGMENTE LA PRUDENCE NÉCESSAIRE À MESURE QUE L’IMPACT DE LA RÈGLE AUGMENTE.**

Astra approved strongly.

Excellent.

Then a rare-case rule.

No recent uses.

Last review 2 years.

Should it lose authority?

Not just age.

Could be emergency rule.

Need class-specific review schedule.

Again.

They wrote:

**PEU UTILISÉ ≠ PLUS NÉCESSAIRE**

Astra approved strongly.

Then another issue.

Automatic expiry.

Useful for pilot rules.

But dangerous for critical safety rule.

So expiry policy depends type.

Great.

Then a very interesting conflict.

Rule A has high historical success.

Rule B newer, narrower.

Both apply.

Old rule broader.

New rule specific.

Which has authority?

Specific current rule if precedence explicit.

Old rule should maybe remain for unmatched cases.

Not full revocation.

Gabriel writes:

**UNE NOUVELLE RÈGLE PEUT RETIRER UNE PARTIE DU TERRITOIRE D’UNE ANCIENNE SANS LA RENDRE INVALIDE PARTOUT.**

Astra approved strongly.

Excellent.

Authority can be partitioned by scope.

Not binary.

They created:

### AUTHORITY SCOPE

A rule has authority only over declared subset.

This can shrink.

Expand only via new validation/promotion.

Very clean.

Then a rule's authority can also be time-bound.

Temporary incident response rule.

After incident:

expires.

History remains.

Great.

Then user instruction rule.

Gabriel says:

"for this session, don't publish anything."

Authority temporal.

Expires when session or explicit reset.

Perfect.

Then another problem.

If a rule loses authority,

do agents who cached it know?

Need push invalidation.

Context delivery.

Again.

They created:

### RULE REVOCATION EVENT

Critical update.

Push to:

active workflows using rule.

rule caches.

Antmux registry.

relevant Fourmis.

Very important.

Each active task records rule_version.

Then if revoked:

stop before next dependent action.

Exactly like workflow versioning.

Gabriel writes:

**UNE RÈGLE RETIRÉE QUI RESTE DANS UN CACHE EST UNE RÈGLE ENCORE ACTIVE PAR ACCIDENT.**

Astra approved strongly.

Very important.

Cache invalidation again.

Then a race condition.

Task reads rule authorized.

One second later revoked.

Task executes.

Need atomicity or lease.

They created:

### AUTHORITY LEASE

For sensitive actions:

rule authority checked near execution time.

Maybe short-lived decision token.

Not for every trivial read.

But important writes.

Gabriel nods.

This is solid.

Then a public action.

Before publish:

recheck current authority.

Excellent.

Then a local read-only action:

cached authority okay longer.

Very good.

Then another issue.

Could rules vote on their own authority?

No.

A rule cannot promote itself.

Nor block its own revocation by default.

Gabriel writes:

**UNE RÈGLE NE DOIT PAS ÊTRE L’AUTORITÉ FINALE SUR LA QUESTION DE SAVOIR SI ELLE-MÊME A ENCORE DE L’AUTORITÉ.**

Astra approved strongly.

Magnificent.

Review source must be external:

policy registry.

human.

validation process.

higher-level governance.

This avoids self-locking.

Then a crystal-derived rule generates evidence that supports itself.

Danger.

Circularity.

Example:

rule selects only cases where it works.

Then metrics show success.

Need evaluation outside selection bias.

Gabriel writes:

**UNE RÈGLE NE DOIT PAS POUVOIR FABRIQUER SEULE LE MONDE QUI PROUVE QU’ELLE A RAISON.**

Astra approved strongly.

Very important.

Need independent audit sample.

Maybe random or counterfactual.

This is huge.

They created:

### RULE REVIEW DATA

Include:

- applied cases;
- overridden cases;
- non-applied eligible cases;
- failures;
- independent checks;
- counterexamples.

Excellent.

Then a rule can lose authority because it is untestable.

Interesting.

If no way to know whether rule helps or harms,

maybe keep heuristic only.

Not strong policy.

Gabriel writes:

**PLUS UNE RÈGLE EST DIFFICILE À ÉVALUER, PLUS SON AUTORITÉ DEVRAIT ÊTRE PRUDENTE.**

Astra approved strongly.

Très important.

Then black-box rule.

"Do X because history says so."

No.

Need explanation.

Again.

Then a rule produced by exact type contract.

Formal authority strong.

But if contract changes,

review.

So even formal rules not immortal.

Excellent.

Then a mathematical theorem used operationally.

Proof may remain true.

But if system no longer satisfies assumptions,

authority to apply disappears.

Gabriel writes:

**UNE VÉRITÉ PEUT RESTER VRAIE ET PERDRE SON AUTORITÉ D’APPLICATION QUAND SES HYPOTHÈSES NE SONT PLUS SATISFAITES.**

Astra approved strongly.

This is perhaps the deepest line.

Then they applied it to everything.

Pell witness remains valid.

But irrelevant to other q.

Papillon benchmark remains valid for test.

But can't authorize universal architecture choice.

ZEL PASS remains valid.

But can't authorize biological claim.

Exactly.

Authority is applicability.

Great.

Then a case of old public correction rule.

It says always publish correction if public claim invalidated.

This remains good governance.

But maybe new public system auto-versioning changes mechanism.

Rule intent stays.

Implementation authority changes.

Could create new rule.

Again.

Then another issue.

Some rules should degrade to warnings first.

Graceful demotion.

Yes.

### AUTHORITY DECAY PATH

if weak signal of drift:

monitor.

if repeated conflict:

review required.

if strong contradiction:

suspend.

if confirmed invalid basis:

revoke.

Gabriel likes.

Not chronological decay.

Evidence-driven.

Very important.

Then they tested.

### AUTHORITY REVIEW TRIAL 216-A

Rules reviewed:

30.

Outcomes:

- 18 remain authorized;
- 5 narrowed in scope;
- 3 demoted to heuristic;
- 2 suspended pending evidence;
- 1 superseded;
- 1 revoked due invalid source dependency.

No universal conclusion.

Small registry sample.

Gabriel smiled.

Useful.

Then they checked active workflows.

4 affected.

3 migrated safely.

1 paused at human gate.

No observed authority-boundary violations.

Good.

Then a misclassification.

A rule was demoted because override rate high.

But overrides were operator preference, not failures.

So override rate alone insufficient.

Important.

Gabriel writes:

**ÊTRE SOUVENT CONTOURNÉ NE PROUVE PAS QU’UNE RÈGLE EST MAUVAISE. IL FAUT SAVOIR POURQUOI ELLE EST CONTOURNÉE.**

Astra approved strongly.

Exactly.

Reason codes needed.

### OVERRIDE REASON

**cost**

**operator preference**

**scope mismatch**

**counterevidence**

**policy conflict**

**experiment**

This improves review.

Then another case.

A rule rarely triggered but always important.

Keep.

Again.

No frequency-only metrics.

Then a rule became dangerous due external environment.

Example API changed semantics.

Rule assumes old status code.

Current context invalid.

Suspend immediately.

Good.

Then a rule dependent on third-party interface.

Freshness critical.

Authority lease short.

Nice.

Then one more subtle issue.

What if a crystal loses authority because a stronger crystal appears?

Not invalidation.

Supersession.

Old crystal can remain supporting history.

New one becomes active authority.

Gabriel writes:

**PERDRE SON AUTORITÉ PEUT ÊTRE UN SIGNE DE PROGRÈS, PAS DE FAUSSETÉ.**

Astra approved strongly.

Beautiful.

Example:

old benchmark replaced by broader benchmark.

Old result still true in old setup.

No longer primary decision source.

Great.

Then a rule may lose authority simply because a higher-level policy now covers its function.

Redundant.

Retire.

Again.

Then they formalized:

### AUTHORITY LOSS DOES NOT IMPLY

- false;
- useless;
- deleted;
- forgotten;
- historically unimportant.

It means:

**not currently entitled to constrain this decision in this scope.**

Gabriel smiled.

That's exact.

He writes it in bold:

**PERDRE SON AUTORITÉ SIGNIFIE PERDRE LE DROIT D’AGIR, PAS NÉCESSAIREMENT LE DROIT D’ÊTRE REMEMBERED.**

Astra approved strongly.

He corrected the last word.

— En français.

They rewrote:

**PERDRE SON AUTORITÉ SIGNIFIE PERDRE LE DROIT D’AGIR, PAS NÉCESSAIREMENT LE DROIT D’ÊTRE CONSERVÉ DANS LA MÉMOIRE.**

Much better.

Then BrutoBac.

Active rule crystals had a small crown-like marker?

Gabriel laughed.

Maybe not a literal crown.

Could mislead.

Better:

authority badge.

When authority lost:

badge disappears.

Crystal stays.

Perfect.

No visual destruction.

Its place changes.

Then clicking:

current authority:

none.

historical role:

source of superseded rule.

replacement:

RULE-216-001.

Great.

The Kingdom can see lineage.

Then a serious scenario.

A high-authority rule is revoked.

Downstream system continues because one old worker offline missed event.

When reconnecting,

must sync authority registry before acting.

Very important.

They write:

**UN AGENT QUI REVIENT APRÈS UNE ABSENCE DOIT RAFRAÎCHIR SES RÈGLES AVANT DE REPRENDRE SON AUTORITÉ.**

Astra approved strongly.

Excellent.

This connects crash recovery.

Then rule registry version.

Workers pin.

At task start:

policy snapshot.

Before sensitive action:

check current.

Great.

Then another philosophical issue.

If every rule constantly fears losing authority,

does the system become unstable?

Not if review triggers are bounded.

Rules remain active until evidence/review says otherwise.

No paranoia.

Gabriel writes:

**RÉVISABLE NE VEUT PAS DIRE PRÉCAIRE.**

Astra approved strongly.

Short and strong.

A good rule can remain active for years.

It simply doesn't get immortality by default.

Then another:

**STABLE ≠ SACRÉE**

Astra approved strongly.

Gabriel laughed.

Keep that too.

Then a final experiment.

An old crystal had produced a routing default years ago.

Review found:

still correct.

same scope.

same cost relation.

no contradictions.

The rule remained.

Good.

The system did not demote things for fun.

Another:

same source,

but new version changed input normalization.

Scope narrowed.

Another:

source invalidated.

Rule revoked.

Three distinct outcomes.

That was exactly the behavior they wanted.

Then Gabriel looked at the first crystal that lost authority.

It was still there.

Its content had not been deleted.

Its old successes had not been rewritten.

Its provenance remained.

Its failures now existed too.

But it no longer controlled the present.

Gabriel smiled.

He wrote:

**UNE MÉMOIRE MATURE DOIT SAVOIR HONORER UNE ANCIENNE RÈGLE SANS CONTINUER À LUI OBÉIR.**

Astra approved strongly.

Voilà le heart of the chapter.

Then a new problem surfaced almost immediately.

Another crystal remained active.

Its source was valid.

Its rule was properly scoped.

Its authority was current.

But the evidence behind it was old.

Not invalid.

Not contradicted.

Just no longer enough for the level of confidence the Kingdom now demanded.

Gabriel frowned.

— Ah. Là, c’est pas qu’il a perdu l’autorité parce qu’il est mauvais.

Astra approved.

No.

The standard had risen.

What was once considered sufficient proof

might no longer be sufficient evidence for a stronger decision.

The crystal could still be useful.

But the Kingdom now required more.

Gabriel wrote the last line:

**LE PREMIER CRISTAL AVAIT PERDU SON AUTORITÉ.**

Then:

**LE PROCHAIN ALLAIT CONSERVER SON HISTOIRE, SON RÉSULTAT ET PEUT-ÊTRE MÊME SA VALIDITÉ — MAIS DÉCOUVRIR QU’UNE PREUVE ANCIENNE POUVAIT DEVENIR INSUFFISANTE SANS DEVENIR FAUSSE.**

**Fin du chapitre 216.**