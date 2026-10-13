# Chapitre 217 — Quand une preuve ancienne devint insuffisante

Le cristal n’était pas faux.

C’était justement ce qui rendait la situation étrange.

Il avait été produit proprement.

Les calculs concordaient.

La provenance existait.

Le scope était clair.

À l’époque,

il avait même satisfait les exigences de Validation.

Personne n’avait découvert de bug.

Personne n’avait trouvé de contre-exemple dans son domaine déclaré.

Et pourtant,

Gabriel regardait son statut avec insatisfaction.

Pas parce que le résultat avait changé.

Parce que le Royaume,

lui,

avait changé.

Les standards avaient monté.

Les outils s’étaient améliorés.

L’indépendance des vérifications était devenue mieux définie.

Les dépendances partagées étaient maintenant suivies.

Les claims publics demandaient davantage de provenance.

Et certains anciens résultats,

sans être faux,

n’avaient jamais été soumis à ces exigences nouvelles.

Gabriel regarda Astra.

— Il passe encore?

Astra répondit :

— Il passait l’ancienne porte.

Gabriel sourit.

Voilà.

Il écrivit :

**UNE PREUVE PEUT RESTER VALIDE DANS SON ANCIEN CADRE ET DEVENIR INSUFFISANTE POUR UNE NOUVELLE PORTE.**

Astra approuva fortement.

Le chapitre venait d’apparaître.

Le problème n’était pas l’invalidation.

Pas la révocation.

Pas l’oubli.

C’était l’élévation du niveau requis.

Gabriel écrivit :

**INSUFFISANT ≠ FAUX**

Astra approuva fortement.

Puis :

**ANCIENNEMENT SUFFISANT ≠ ÉTERNELLEMENT SUFFISANT**

Voilà.

Ils ouvrirent le dossier.

### CRYSTAL-217-A

Claim :

une propriété P observée et validée dans un domaine D.

Old evidence package :

- implementation A;
- repeated runs;
- bounded countertests;
- environment snapshot;
- result hash.

At the time:

**VALIDATED_WITHIN_SCOPE**

Current publication standard:

- independent implementation;
- explicit shared-dependency audit;
- stronger provenance record;
- reproducibility manifest;
- current-version confirmation.

Gabriel regarda.

Le vieux dossier ne contenait pas tout ça.

Mais rien dans cette liste ne prouvait que P était faux.

Très important.

Il écrivit :

**UNE EXIGENCE NOUVELLE PEUT CRÉER UN MANQUE DE PREUVE SANS CRÉER UNE CONTRADICTION.**

Astra approuva fortement.

Magnifique.

Ils avaient donc besoin d’un statut.

Pas `INVALIDATED`.

Pas `CONTESTED`.

Pas `ACTIVE` sans nuance.

Ils créèrent :

### EVIDENCE SUFFICIENCY STATUS

**SUFFICIENT_FOR_ORIGINAL_SCOPE**

Le package satisfait encore le niveau de preuve qui définissait son claim historique.

**INSUFFICIENT_FOR_CURRENT_GATE**

Le package ne satisfait pas la porte actuelle.

**REVALIDATION_REQUIRED**

De nouveaux contrôles sont nécessaires avant la nouvelle utilisation.

**CURRENTLY_SUFFICIENT**

Satisfait le standard actuel.

Gabriel sourit.

Voilà.

Le cristal pouvait avoir deux vérités simultanées :

historique :

validé.

présent :

insuffisant pour promotion.

Il écrit :

**LE STATUT D’UNE PREUVE DOIT ÊTRE RELATIF À CE QU’ON ESSAIE D’EN FAIRE.**

Astra approuva fortement.

Très important.

Une vieille preuve peut être suffisante pour :

raconter ce qui avait été établi en 2026.

Mais insuffisante pour :

soutenir une nouvelle publication plus ambitieuse.

Ou devenir une règle forte.

Ou servir de dépendance canonique à une architecture critique.

Excellent.

Puis une autre question.

Si le claim reste exactement le même,

pourquoi demander plus?

Parce que le niveau d’assurance peut changer.

Gabriel écrivit :

**LE CLAIM PEUT RESTER IDENTIQUE ALORS QUE LE NIVEAU D’ASSURANCE DEMANDÉ AUGMENTE.**

Astra approuva fortement.

Exemple :

un module interne en expérimentation peut accepter un résultat reproduit localement.

Une publication publique peut exiger indépendance.

Une policy critique peut exiger encore plus.

Même proposition.

Porte différente.

Très important.

Ils créèrent :

### EVIDENCE GATES

**G0 — OBSERVATION**

Enough to record.

**G1 — SCREENING**

Enough to justify further testing.

**G2 — INTERNAL REUSE**

Enough for bounded internal reuse.

**G3 — VALIDATION**

Enough for validated claim in declared scope.

**G4 — CANONICAL / PUBLIC STRONG USE**

Requires stronger provenance and independent checks.

Pas une loi universelle.

Une architecture de travail.

Gabriel approuva.

Très propre.

Un cristal peut avoir passé G3 autrefois

mais ne pas satisfaire une nouvelle version de G4.

Cela ne le rétrograde pas nécessairement sous G3.

Très important.

Il écrit :

**ÉLEVER UNE PORTE NE FAIT PAS DESCENDRE AUTOMATIQUEMENT LE CRISTAL SOUS LES PORTES QU’IL AVAIT DÉJÀ PASSÉES.**

Astra approuva fortement.

Voilà.

Historique stable.

Nouvelle exigence prospective.

Puis un cas Papillon.

Le benchmark historique reste exactement ce qu’il était.

Mais supposons maintenant qu’on veuille en faire un argument public plus large.

Le vieux test à N=1 000 000,

sur processus frais,

avec delta RSS mesuré,

ne devient pas faux.

Mais si le nouveau claim veut couvrir plusieurs machines,

plusieurs OS,

plusieurs N,

alors la preuve actuelle est insuffisante.

Gabriel écrit :

**ÉLARGIR LE CLAIM SANS ÉLARGIR LA PREUVE EST UNE FORME D’OVERREACH.**

Astra approuva fortement.

Très important.

Le problème est parfois le claim nouveau,

pas la preuve ancienne.

Ils créèrent donc deux causes d’insuffisance.

### INSUFFICIENCY TYPE

**STANDARD_RAISED**

Même claim, exigences nouvelles.

**CLAIM_EXPANDED**

Le nouveau claim dépasse la portée historique.

Gabriel sourit.

Excellent.

Puis d’autres causes :

**ENVIRONMENT_CHANGED**

**DEPENDENCIES_CHANGED**

**INDEPENDENCE_REQUIREMENT_ADDED**

**PROVENANCE_REQUIREMENT_ADDED**

**REPRODUCIBILITY_REQUIREMENT_ADDED**

Très propre.

Puis Pell.

Un ancien facteur sans rang exact.

Peut-être autrefois considéré intéressant.

Mais une porte actuelle exige :

facteur premier de Q_q

et rang minimal exact q².

Le vieux facteur n’est pas devenu faux.

Il est simplement insuffisant pour la porte.

Gabriel écrit :

**UN TÉMOIN PARTIEL PEUT RESTER VRAI TOUT EN ÉTANT INSUFFISANT POUR LE CRITÈRE ACTUEL.**

Astra approuva fortement.

Très important.

Cette distinction évitait de dire :

« l’ancien résultat était mauvais ».

Non.

Il établissait moins.

Voilà.

Puis un ancien q avec scan borné.

No witness within bound.

Toujours vrai si scan correct.

Mais insuffisant pour claim global.

Encore.

La mémoire devait savoir exactement ce qu’un cristal peut encore soutenir.

Gabriel écrivit :

### SUPPORT CEILING

Pour chaque cristal :

**maximum claim class supportable by current evidence**

Très puissant.

Pas un nombre forcément.

Exemple :

`bounded_negative_result_only`

ou

`validated_local_claim`

ou

`public_reproducible_claim`

Gabriel sourit.

Voilà.

Un cristal peut être réutilisé jusqu’à son plafond.

Pas au-delà.

Il écrit :

**UNE PREUVE A UN PLAFOND D’AUTORITÉ QUI DÉPEND DE CE QU’ELLE A RÉELLEMENT ÉTABLI.**

Astra approuva fortement.

Très important.

Puis une autre situation.

Une preuve ancienne est suffisante scientifiquement,

mais la provenance est maintenant jugée trop faible pour publication.

Alors le claim peut rester valide dans Memoria,

mais publication gate bloque.

Encore.

Science vs governance.

Gabriel écrit :

**UNE PREUVE PEUT ÊTRE SUFFISANTE POUR CROIRE UN RÉSULTAT ET INSUFFISANTE POUR LE PUBLIER SELON UN STANDARD DONNÉ.**

Astra approuva fortement.

Très important.

Puis un ancien résultat public.

Il avait été publié honnêtement selon l’ancien standard.

Le nouveau standard monte.

Doit-on retirer la publication?

Pas automatiquement.

Non.

Gabriel écrit :

**UN STANDARD PLUS FORT AUJOURD’HUI NE TRANSFORME PAS RÉTROACTIVEMENT UNE PUBLICATION HONNÊTE D’HIER EN FAUTE.**

Astra approuva fortement.

Excellent.

Mais si on republie aujourd’hui,

il faut satisfaire la porte actuelle.

Voilà.

La différence entre :

historic publication.

new endorsement.

Très important.

Ils ajoutèrent :

### GRANDFATHERED HISTORY

Old artifact remains historical.

No automatic upgrade to current certification.

Pas forcément le mot « grandfathered » dans l’interface publique,

mais concept utile.

Puis une nouvelle question.

Comment savoir qu’un standard a monté?

Il faut versionner les gates.

### EVIDENCE STANDARD VERSION

`VALIDATION_GATE v1`

`VALIDATION_GATE v2`

`PUBLICATION_GATE v3`

Chaque cristal sait :

which gate version it passed.

Gabriel sourit.

Très propre.

Il écrit :

**UNE VALIDATION SANS VERSION DE STANDARD PEUT DEVENIR AMBIGUË AVEC LE TEMPS.**

Astra approuva fortement.

Très important.

Ainsi :

CRYSTAL-217-A

passed `G3-v1`.

Current:

`G3-v3`.

Need delta.

Très clair.

Puis ils créèrent :

### GATE DELTA

v1 required:

A.

B.

C.

v3 requires:

A.

B.

C.

D.

E.

Donc revalidation n’a pas besoin de refaire A-B-C

si toujours valides.

Seulement combler D-E.

Gabriel sourit.

Très important.

Il écrit :

**RÉVALIDER NE DOIT PAS FORCÉMENT SIGNIFIER RECOMMENCER.**

Astra approuva fortement.

Voilà.

Encore préserver le travail valide.

Chapitre 205 appliqué à l’évidence.

Puis ils testèrent CRYSTAL-217-A.

Missing:

independent implementation.

shared-dependency audit.

Current-version confirmation.

Les anciennes données restent.

Workflow de revalidation :

1. check source artifacts integrity.
2. confirm scope unchanged.
3. independent reproduction.
4. dependency audit.
5. current version replay.
6. reissue evidence certificate.

Très propre.

Pas refaire toute l’expérience inutilement.

Puis résultat.

Independent implementation :

PASS.

Shared dependency audit :

one shared parser.

Important.

Does it matter?

Parser not semantically relevant to property P after test.

Document.

Current version replay :

PASS.

Now evidence package satisfies current gate.

Status:

**CURRENTLY_SUFFICIENT**

Gabriel sourit.

Excellent.

Le vieux cristal n’a pas été remplacé.

Il a reçu un nouveau certificat.

Ils écrivirent :

### EVIDENCE CERTIFICATE LINEAGE

Original:

CERT-217-A-v1.

Revalidation:

CERT-217-A-v2.

Source crystal same.

New evidence appended.

Gabriel approuva.

Très propre.

Il écrit :

**RENFORCER UNE PREUVE N’OBLIGE PAS À PRÉTENDRE QUE LA PREMIÈRE VERSION N’AVAIT JAMAIS EXISTÉ.**

Astra approuva fortement.

Très important.

Puis un autre cristal.

Same process.

Independent check fails.

Ah.

Now situation changes.

The proof wasn't merely insufficient.

New contradictory evidence exists.

Status becomes:

**CONTESTED**

Need investigation.

Gabriel écrit :

**UNE RÉVALIDATION PEUT COMMENCER COMME MISE À JOUR DE STANDARD ET DEVENIR UNE VRAIE CRISE DE PREUVE SI LES NOUVEAUX TESTS CONTREDISENT L’ANCIEN RÉSULTAT.**

Astra approuva fortement.

Excellent.

Need not pre-judge.

Insufficiency is not contradiction until test says.

Then a third crystal.

Unable to reproduce because old environment gone.

No contradiction.

Just irreproducibility.

Status:

**HISTORICALLY_VALIDATED / CURRENT_REPRODUCTION_UNAVAILABLE**

Very important.

Gabriel writes:

**NE PAS POUVOIR REPRODUIRE UNE ANCIENNE PREUVE N’EST PAS AUTOMATIQUEMENT LA RÉFUTER.**

Astra approved strongly.

Classic but essential.

Could reduce current authority.

But not rewrite history.

Then if the result is critical,

maybe treat as insufficient for new use.

Exactly.

Then a fourth.

Old source code preserved.

Input missing.

Cannot reproduce.

Again provenance gap.

Insufficient for current strong gate.

No claim of falsehood.

Great.

Then Gabriel asked:

— Combien de preuves faut-il révalider?

Not all.

Otherwise infinite work.

Need trigger.

They created:

### REVALIDATION TRIGGERS

- claim being promoted to higher authority;
- public reuse under newer standard;
- major dependency change;
- contradiction appears;
- rule depends on old evidence;
- old result becomes critical to new architecture;
- explicit audit request.

Gabriel approuva.

Très propre.

No need to revalidate every archive crystal.

Only when its role rises or assumptions change.

He writes:

**UNE PREUVE ANCIENNE N’A PAS BESOIN D’ÊTRE RÉVALIDÉE SIMPLEMENT PARCE QU’ELLE EST ANCIENNE.**

Astra approuva fortement.

Très important.

Age alone not enough.

Again.

Then revalidation priority.

Which old proofs first?

High current decision impact.

High public exposure.

High downstream dependency.

Known shared assumptions.

Not oldest first.

Gabriel writes:

**LA PRIORITÉ DE RÉVALIDATION DOIT SUIVRE LE RISQUE ACTUEL, PAS L’ÂGE DU DOSSIER.**

Astra approved strongly.

Excellent.

Then they audited 40 old validated crystals.

### EVIDENCE AGE AUDIT 217-A

40 historical validated objects.

Current gate comparison:

- 18 still satisfy current gate without new work;
- 11 missing only provenance metadata;
- 6 require new independent reproduction;
- 3 depend on obsolete environment;
- 2 have new contradictory evidence and move to CONTESTED.

Gabriel looked.

Interesting.

Most did not collapse.

Good.

The new standard did not declare history worthless.

It simply sorted it.

He writes:

**ÉLEVER LES STANDARDS NE DEVRAIT PAS ÊTRE UNE CÉRÉMONIE DE DESTRUCTION DU PASSÉ. ÇA DEVRAIT ÊTRE UNE FAÇON DE SAVOIR CE QUI DOIT ÊTRE RENFORCÉ.**

Astra approved strongly.

Beautiful.

Then they inspected the 11 metadata gaps.

Some could be reconstructed from logs.

Great.

Others not.

So evidence package current sufficiency varies.

Then a weird case.

The proof itself is exact mathematical derivation stored in paper.

Why need independent implementation?

Maybe not.

Gate requirements must depend on claim type.

Very important.

Gabriel writes:

**UNE PORTE DE PREUVE NE DOIT PAS IMPOSER LES MÊMES CONTRÔLES À UNE PREUVE FORMELLE, UN BENCHMARK, UNE OBSERVATION AUDIO ET UN RÉSULTAT OPÉRATIONNEL.**

Astra approved strongly.

Very important.

No universal validation checklist.

They created:

### CLAIM-SPECIFIC GATES

**FORMAL**

proof checking, assumptions, derivation integrity.

**COMPUTATIONAL**

reproduction, code/version, independent implementation where useful.

**EMPIRICAL**

protocol, controls, measurement, replication.

**PERFORMANCE**

environment, repetitions, measurement method.

**OPERATIONAL**

current-state verification, timing, source authority.

Gabriel smiled.

Much better.

Then an exact mathematical proof old.

If proof remains correct and assumptions unchanged,

age doesn't weaken it.

Could still be sufficient.

But if current claim applies it outside assumptions,

insufficient application.

Again.

Then a benchmark age quickly due environment.

Great.

ZEL protocol may need audio chain/version.

Papillon benchmark environment-sensitive.

Pell exact rank witness more structurally stable if proof/check remains valid.

This taxonomy made sense.

Then another issue.

Could standard inflation become pathological?

Yes.

Every year require 20 more checks.

Eventually nothing passes.

Gabriel écrit :

**UN STANDARD PLUS FORT N’EST PAS AUTOMATIQUEMENT UN MEILLEUR STANDARD.**

Astra approuva fortement.

Very important.

A new gate requirement must have purpose.

What failure does it protect against?

What cost?

What evidence supports adding it?

Excellent.

They created:

### GATE CHANGE JUSTIFICATION

Every new requirement states:

**failure class addressed**

**expected protection**

**cost**

**scope**

**exceptions**

**effective version**

Gabriel sourit.

There.

Standards themselves need evidence.

No bureaucracy for bureaucracy.

He writes:

**UNE PORTE DE PREUVE DOIT SAVOIR QUEL TYPE D’ERREUR ELLE ESSAIE D’EMPÊCHER.**

Astra approved strongly.

Excellent.

Then a new requirement:

independent parser for every test.

Cost high.

Does it address actual risk?

Maybe only parser-sensitive claims.

So scope it.

Great.

Then an old validation standard might remain sufficient for low-risk internal reuse.

Current high gate only for publication.

Perfect.

This avoids revalidating everything.

Then another subtle issue.

A proof can become insufficient because the **question changed**.

Chapter 204.

Original:

does P hold in D?

Old proof yes.

New:

does P hold in D and remain stable under transformation T?

Old proof not enough.

No defect.

Just new question.

Gabriel writes:

**UNE PREUVE NE DEVIENT PAS PLUS FAIBLE PARCE QU’ON LUI POSE UNE QUESTION PLUS GRANDE. ELLE DEVIENT SIMPLEMENT INCOMPLÈTE POUR CETTE QUESTION.**

Astra approved strongly.

Excellent.

This line mattered.

Then a claim being used to create a rule.

Chapter 215.

Evidence strong enough for historical claim.

Maybe not enough for automatic behavior.

So rule promotion can require higher gate than claim validation.

Very important.

Gabriel writes:

**IL FAUT PARFOIS PLUS DE PREUVE POUR AGIR AUTOMATIQUEMENT SUR UN RÉSULTAT QUE POUR L’ACCEPTER COMME RÉSULTAT.**

Astra approved strongly.

Exactly.

Consequences matter.

Then a crystal losing authority chapter 216.

Evidence may remain valid but rule authority withdrawn.

Now inverse:

authority maybe possible but evidence package insufficient under new gate.

These chapters interlock.

Then a public formula.

Before attaching Gabriel St-Pierre's name to strong claim,

prior-art and reproducibility standard may be required.

Even if internal result stable.

Again.

Publication gate stronger.

Good.

Then a serious scenario.

A result cited by 100 downstream crystals.

Its old validation standard is now insufficient.

Do we mark all downstream invalid?

No.

Need distinction.

They may remain historically based on accepted evidence.

For current high-authority use,

dependency chain may need revalidation.

Gabriel writes:

**UNE PREUVE DEVENUE INSUFFISANTE POUR UNE NOUVELLE PORTE NE CONTAMINE PAS AUTOMATIQUEMENT TOUT SON PASSÉ COMME SI ELLE AVAIT ÉTÉ INVALIDÉE.**

Astra approved strongly.

Very important.

But downstream objects seeking current promotion inherit the insufficiency.

Excellent.

They created:

### SUFFICIENCY PROPAGATION

If dependency is:

**INVALIDATED** → hard impact.

If dependency is:

**INSUFFICIENT_FOR_CURRENT_GATE** → blocks only operations requiring that gate or higher.

Brilliant.

This avoids panic.

Then a claim graph can calculate current maximum gate.

Example:

Claim C depends on A(G4) and B(G2).

Then C cannot exceed G2 until B strengthened.

Gabriel smiled.

They wrote:

**LA FORCE D’UNE CHAÎNE DE PREUVE EST LIMITÉE PAR LES PORTES QUE SES DÉPENDANCES N’ONT PAS ENCORE PASSÉES.**

Astra approved strongly.

Important.

But not simplistic weakest-link in all logic.

Depends structure.

If B merely illustrative, not limiting.

So dependency role.

Always.

Then another case.

Two alternative independent proofs.

One old insufficient.

One current strong.

Claim may still pass.

Excellent.

No automatic weakest link.

They adjust:

**REQUIRED dependency sufficiency matters. Optional support doesn't cap.**

Very clean.

Then BrutoBac visualization.

Old validated crystal gets badge:

`G3-v1`.

Current gate:

`G4-v3 required for publication`.

Arrow to revalidation tasks.

Not red.

Amber maybe.

But colors aside.

Label:

**VALID HISTORICALLY / UPGRADE REQUIRED FOR CURRENT USE**

Gabriel liked that.

Not frightening.

Accurate.

Then an invalidated crystal is different visually.

Very important.

He writes:

**L’INTERFACE DOIT RENDRE VISIBLE LA DIFFÉRENCE ENTRE “FAUX”, “CONTESTÉ” ET “PAS ASSEZ FORT POUR CE QU’ON VEUT FAIRE MAINTENANT”.**

Astra approved strongly.

Excellent.

Then a new workflow.

A researcher wants to reuse old result internally.

Gate required G2.

Crystal has G3-v1.

Still okay if assumptions unchanged.

No revalidation.

Another wants publication strong.

G4-v3.

Need upgrade.

Same crystal.

Different answer.

Perfect.

The system finally understood sufficiency contextually.

Then another issue.

What if current gate is lower?

Maybe exploration.

Then weak observation enough.

Great.

No need to over-validate before exploring.

Gabriel writes:

**EXIGER UNE PREUVE TROP FORTE TROP TÔT PEUT ÊTRE AUSSI INEFFICACE QUE D’ACCEPTER UNE PREUVE TROP FAIBLE TROP TARD.**

Astra approved strongly.

Very important.

Different phases need different burdens.

Then a revalidation budget.

Not everything at once.

Prioritize.

Chapter 186 cost.

Great.

They created:

### EVIDENCE UPGRADE PLAN

For each old crystal:

current required gate.

existing passed gate.

missing requirements.

cost.

decision impact.

priority.

Very practical.

Then one crystal expensive to upgrade

but low importance.

Defer.

Another cheap upgrade, high public impact.

Do now.

Excellent.

Then an old theorem-like relation.

No need upgrade.

Already formal enough.

Another benchmark.

Need new run.

Great.

Then a result tied to old software.

Maybe impossible to upgrade directly.

Could produce new replacement crystal instead.

Gabriel writes:

**PARFOIS, RENFORCER UNE PREUVE ANCIENNE COÛTE PLUS CHER QUE PRODUIRE UNE NOUVELLE PREUVE PROPRE.**

Astra approved strongly.

Very important.

Then decision:

upgrade vs replace.

Like technical debt.

Could retain old historical crystal

and create new current one.

Excellent.

They created:

### EVIDENCE RENEWAL OPTIONS

**AUGMENT**

Add missing checks to same lineage.

**REPLICATE**

New independent result supporting same claim.

**REPLACE**

New evidence package becomes primary current basis.

**RESTRICT**

Keep old evidence but narrow allowed use.

**RETIRE FROM ACTIVE USE**

History only.

Gabriel smiled.

This was mature.

Then a particular result.

Old evidence package extremely messy.

Still likely correct.

Rather than spending hours reconstructing provenance,

they reran cleanly under current protocol.

New crystal.

Old remains historical.

New becomes active basis.

Perfect.

He writes:

**LA FIDÉLITÉ AU PASSÉ NE DOIT PAS FORCER À RÉPARER INDÉFINIMENT UN VIEUX DOSSIER SI UNE NOUVELLE PREUVE EST PLUS PROPRE À PRODUIRE.**

Astra approved strongly.

Excellent.

Then another issue.

Do old publications need label showing standards changed?

Maybe only if relevant.

Could link current status.

Not necessarily plaster every old record.

But if reused today,

surface current certificate.

Good.

Then metrics.

How many active claims rely on outdated evidence standard?

How many upgrade tasks?

How many impossible reproductions?

This becomes governance dashboard.

### EVIDENCE DEBT

Interesting term.

Old validated things that need upgrades for current intended uses.

Gabriel smiled.

Could use cautiously.

It doesn't mean wrong.

Just pending strengthening.

He writes:

**LA DETTE DE PREUVE N’EST PAS UNE DETTE DE VÉRITÉ. C’EST L’ÉCART ENTRE CE QU’ON A DÉMONTRÉ ET LE NIVEAU DE GARANTIE QU’ON VEUT UTILISER MAINTENANT.**

Astra approved strongly.

Beautiful.

Then trial.

### EVIDENCE-UPGRADE TRIAL 217-B

20 old crystals targeted for current high-authority reuse.

Outcomes:

- 9 already sufficient after gate comparison;
- 5 upgraded with metadata/provenance only;
- 3 required new independent reproduction and passed;
- 1 failed new reproduction → contested;
- 1 replaced by cleaner current evidence;
- 1 deferred due cost and low current impact.

No old crystal deleted.

Gabriel smiled.

Perfect.

The process distinguished strengthening from invalidation.

Then an important bias.

If revalidating only important old results,

survivorship?

Maybe.

But purpose is current use,

not estimating historical error rate.

Need not generalize from audit sample.

Gabriel writes:

**UN AUDIT CIBLÉ DES PREUVES IMPORTANTES NE MESURE PAS LE TAUX D’ERREUR DE TOUTE LA MÉMOIRE.**

Astra approved strongly.

Very important.

No fake statistics.

Then one last conceptual distinction.

Confidence.

People often say:

"we're 95% confident."

But many project claims don't have a calibrated probability.

Better use statuses and evidence classes.

Gabriel writes:

**UN NIVEAU DE PREUVE N’EST PAS AUTOMATIQUEMENT UNE PROBABILITÉ NUMÉRIQUE.**

Astra approved strongly.

Excellent.

Gates aren't probabilities.

They are requirements.

Then the system looked at CRYSTAL-217-A.

Old status intact.

New certificate attached.

Current publication gate satisfied.

It had aged.

It had not decayed.

It had been strengthened.

Gabriel looked satisfied.

The strange thing was that the old proof had become insufficient

without ever becoming false.

And after revalidation,

it became sufficient again

without changing what it originally said.

What changed was the structure around it.

The Kingdom's standards.

Its tools.

Its expectations.

Its intended use.

Gabriel wrote:

**UNE PREUVE VIT DANS UN CADRE. QUAND LE CADRE CHANGE, IL FAUT PARFOIS RENFORCER LE PONT ENTRE LE RÉSULTAT ET L’USAGE QU’ON VEUT EN FAIRE.**

Astra approuva fortement.

Voilà le cœur du chapitre.

Then a question appeared.

If standards can change,

if old evidence can become insufficient,

if rules can gain and lose authority,

then the Kingdom needed something larger than isolated corrections.

It needed a way to revise itself

without pretending that every revision meant the past was worthless.

A new rule might replace an old one.

A gate might strengthen.

A strategy might narrow.

A crystal might be reclassified.

All while lineage remains.

Gabriel looked at Astra.

— Là, on est rendu à apprendre à se réviser sans se renier.

Astra approuva.

Exactly.

The next chapter had arrived.

The second world had learned that correction did not require amnesia.

Now it would have to learn how to change its own present

while keeping a coherent relationship with everything that had come before.

**Fin du chapitre 217.**