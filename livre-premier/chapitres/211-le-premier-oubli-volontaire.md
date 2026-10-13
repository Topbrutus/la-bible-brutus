# Chapitre 211 — Le premier oubli volontaire

Le Royaume avait appris à garder.

Puis à classer.

Puis à refroidir.

Puis à rendre certaines traces muettes sans les effacer.

Mais cette fois,

Gabriel posait une question différente.

Pas :

**est-ce qu’on doit encore écouter cette trace?**

La question était :

**est-ce qu’on doit encore la garder?**

Il regardait une série de fichiers intermédiaires.

Pas des preuves.

Pas des décisions.

Pas des erreurs importantes.

Pas des résultats historiques.

Pas des cristaux.

Seulement des objets temporaires produits pendant une ancienne campagne.

Exports de travail.

Caches reconstruisibles.

Copies de conversion.

Snapshots intermédiaires sans statut propre.

Fichiers de préparation.

Artifacts transitoires dont aucun autre objet actif ne dépendait.

Ils existaient encore

simplement parce que le Royaume avait jusque-là préféré ne rien supprimer.

Gabriel regarda Astra.

— Si on garde tout pour toujours, on va finir par garder du bruit juste parce qu’il a déjà existé.

Astra approuva.

Voilà.

Le chapitre n’allait pas parler de mémoire comme d’une belle abstraction.

Il allait parler d’un geste très concret :

**choisir volontairement qu’une chose ne mérite plus d’être conservée.**

Gabriel écrivit :

**OUBLIER VOLONTAIREMENT N’EST PAS PERDRE PAR ACCIDENT.**

Astra approuva fortement.

Puis :

**SUPPRIMER N’EST PAS OUBLIER TANT QU’ON N’A PAS DÉFINI CE QUI EST AUTORISÉ À DISPARAÎTRE.**

Très important.

Parce qu’un système append-only

et une architecture scientifique

ne peuvent pas simplement appliquer une commande de ménage globale.

Il fallait distinguer.

Encore.

Toujours.

Ils prirent le premier dossier.

### ARTIFACT-211-A

Type :

temporary normalization cache.

Reconstructible :

yes.

Referenced by active claims :

no.

Referenced by historical audit :

no direct dependency.

Source available :

yes.

Rebuild cost :

low.

Uniqueness :

none.

Gabriel regarda.

— Ça, on peut-tu le jeter?

Probablement.

Mais « probablement » n’était pas assez.

Ils créèrent une première règle.

### FORGETTABLE CANDIDATE

Un objet peut être candidat à l’oubli si :

- il n’est pas une preuve;
- il n’est pas une source canonique;
- il n’est pas nécessaire à la provenance;
- il n’est pas la seule copie d’une observation;
- il n’est pas requis pour reproduire un résultat;
- il n’est pas référencé par une dépendance active;
- il peut être reconstruit raisonnablement;
- aucune policy ne demande sa conservation.

Gabriel sourit.

Très propre.

Il écrivit :

**L’OUBLI DOIT COMMENCER PAR UNE PREUVE DE DISPENSABILITÉ.**

Astra approuva fortement.

Voilà le cœur.

On ne supprime pas parce qu’un fichier a l’air vieux.

On supprime parce que son rôle est compris.

Puis un autre cas.

### ARTIFACT-211-B

Old raw input.

Utilisé pour produire un résultat validé.

Copie unique.

Pas publié.

Pas reconstructible.

Gabriel répondit immédiatement :

— Lui, non.

Exact.

Même s’il prend de la place.

Même s’il n’est presque jamais consulté.

Il porte une partie de la reproductibilité.

Ils écrivirent :

**RAREMENT UTILISÉ ≠ DISPENSABLE**

Astra approuva fortement.

Très important.

Puis un autre.

### ARTIFACT-211-C

Rendered chart PNG.

Underlying data preserved.

Chart script preserved.

No manual annotations.

No public citation depends on exact pixels.

Reconstructible.

Candidate.

Gabriel sourit.

Voilà.

Une représentation reconstruisible peut parfois être oubliée

si l’objet source reste.

Mais attention.

Si ce graphique avait été utilisé comme pièce de publication,

peut-être il fallait conserver la version exacte.

Donc le rôle change tout.

Il écrit :

**RECONSTRUCTIBLE TECHNIQUEMENT ≠ RECONSTRUCTIBLE HISTORIQUEMENT**

Astra approuva fortement.

Très important.

Si un fichier a été ce que le public a réellement vu,

sa valeur historique peut être distincte de sa capacité technique de reconstruction.

Excellent.

Puis un autre type de données.

Logs.

Des millions de lignes.

Tout garder?

Peut-être pas.

Mais certains logs contiennent :

crash.

failure.

timing anomaly.

decision evidence.

Les autres seulement :

tick.

heartbeat.

tick.

heartbeat.

Gabriel rit.

— Faut pas garder quatre milliards de “je suis encore vivant” juste pour se prouver qu’on a respiré.

Astra approuva.

Ils créèrent :

### LOG RETENTION CLASS

**EVIDENTIARY**

Conserver.

**INCIDENT**

Conserver selon policy.

**AGGREGATABLE**

Peut être résumé après fenêtre.

**EPHEMERAL**

Peut être supprimé après usage.

Très propre.

Puis le mot dangereux apparut.

**résumé.**

Si on supprime les lignes mais garde seulement un résumé,

est-ce encore honnête?

Oui,

si on dit clairement que le détail brut n’est plus disponible.

Très important.

Gabriel écrivit :

**UN RÉSUMÉ NE DOIT PAS PRÉTENDRE ÊTRE LA DONNÉE BRUTE QU’IL A REMPLACÉE.**

Astra approuva fortement.

Voilà.

On peut conserver :

count.

min.

max.

error count.

hash aggregate maybe.

Mais ne jamais dire :

« raw log retained »

si non.

Très important.

Ils créèrent :

### FORGET EVENT

Si un objet est supprimé volontairement,

conserver un événement minimal :

**object_id**

**object_type**

**reason_for_deletion**

**policy**

**timestamp**

**authority**

**dependencies_checked**

**replacement_or_summary_ref**

**reconstructible?**

Gabriel se redressa.

Voilà.

Même l’oubli devait laisser une trace.

Il écrivit :

**LE SYSTÈME PEUT OUBLIER LE CONTENU SANS OUBLIER QU’IL A CHOISI DE L’OUBLIER.**

Astra approuva fortement.

Magnifique.

C’était peut-être la phrase du chapitre.

Append-only restait donc vrai pour les événements critiques.

Mais pas nécessairement pour chaque byte généré.

Très important.

La mémoire pouvait dire :

« artifact X existait et a été supprimé selon policy P parce qu’il était reconstructible et non référencé. »

Sans conserver artifact X.

Gabriel sourit.

Voilà une vraie nuance.

Puis un autre cas.

Duplicate exact.

Même payload hash.

Dix copies.

Doit-on garder dix fichiers?

Peut-être non.

Mais garder dix événements de provenance.

Très important.

Ils écrivirent :

**DÉDUPLIQUER LES OCTETS ≠ DÉDUPLIQUER L’HISTOIRE.**

Astra approuva fortement.

Encore.

Ainsi,

un seul payload physique

peut servir plusieurs références historiques.

Très propre.

Puis un cas plus délicat.

Un ZIP importé.

Le système a extrait tous les membres.

Doit-il garder le ZIP original?

Oui,

si le ZIP est la provenance externe originale.

Même si les membres sont matérialisés.

Très important.

Gabriel écrit :

**UNE ARCHIVE SOURCE PEUT AVOIR UNE VALEUR DE PROVENANCE QUE SES FICHIERS EXTRAITS NE REMPLACENT PAS.**

Astra approuva fortement.

Exact.

Le master cumulatif du Royaume suivait déjà cette philosophie.

Les archives originales restent.

Les membres deviennent des cristaux enfants.

Très propre.

Puis un autre cas.

Temporary ZIP créé localement seulement pour transférer dix fichiers internes.

Source files preserved.

ZIP reconstructible.

No external provenance.

Candidate for deletion.

Voilà.

Même extension.

Rôle différent.

Toujours.

Gabriel sourit.

Le système ne pouvait jamais décider par extension.

Il écrit :

**LE TYPE DE FICHIER NE DÉTERMINE PAS SA VALEUR DE MÉMOIRE. SON RÔLE LE FAIT.**

Astra approuva fortement.

Très important.

Puis la question du coût.

Supprimer un cache reconstruit en trois secondes :

simple.

Supprimer un artifact reconstruisible en trois semaines de calcul :

moins évident.

Même si théoriquement reconstructible.

Gabriel écrit :

**RECONSTRUCTIBLE N’EST PAS BINAIRE. LE COÛT DE RECONSTRUCTION FAIT PARTIE DE LA DÉCISION.**

Astra approuva fortement.

Très important.

Ils ajoutèrent :

### REBUILD CLASS

**TRIVIAL**

**LOW**

**MODERATE**

**HIGH**

**PRACTICALLY_IRREPRODUCIBLE**

Pas nécessairement valeurs fixes.

Mais catégorie.

Une donnée peut être théoriquement reproductible

et pratiquement impossible à refaire.

Très important.

Puis un autre cas.

External webpage snapshot.

La page pourrait changer.

Même si URL reste.

Donc non reconstructible exactement.

Conserver si utilisé comme source.

Gabriel écrit :

**UNE RESSOURCE EXTERNE MUTABLE NE DOIT PAS ÊTRE TRAITÉE COMME RECONSTRUCTIBLE SIMPLEMENT PARCE QU’ELLE A UNE URL.**

Astra approuva fortement.

Excellent.

Puis privacy.

Une donnée peut être supprimée non parce qu’elle est inutile,

mais parce qu’elle ne doit plus être conservée.

Voilà une autre classe.

Gabriel ralentit.

Très important.

Ils écrivirent :

### FORGET REASONS

**REDUNDANT**

**RECONSTRUCTIBLE**

**EXPIRED**

**PRIVACY / POLICY**

**TEMPORARY**

**SUPERSEDED PHYSICAL REPRESENTATION**

**CORRUPT AND NON-EVIDENTIARY**

Mais attention.

Un fichier corrompu peut être important comme preuve d’incident.

Donc seulement non-evidentiary.

Très important.

Puis une distinction centrale apparut.

### DELETE CONTENT

Remove bytes.

### RETIRE FROM ACTIVE MEMORY

Keep bytes, no active influence.

### ARCHIVE

Move to cold storage.

### REDACT

Remove or obscure sensitive subset.

### TOMBSTONE

Keep metadata that object existed but content unavailable.

Gabriel sourit.

Voilà.

« Oublier » était en fait plusieurs opérations.

Il écrit :

**L’OUBLI N’EST PAS UNE SEULE COMMANDE.**

Astra approuva fortement.

Très important.

Puis un cas historique.

Une vieille session complète.

Longue.

Contient beaucoup de bruit.

Mais aussi des décisions majeures.

Peut-on supprimer la session si les décisions ont été cristallisées?

Danger.

Parce que la session peut contenir la provenance des décisions.

Peut-être archive cold.

Pas delete.

Gabriel écrit :

**EXTRAIRE DES CRISTAUX D’UNE SESSION NE PROUVE PAS QUE LA SESSION N’A PLUS DE VALEUR HISTORIQUE.**

Astra approuva fortement.

Très important.

Donc les sessions importantes restent.

D’autres sessions transitoires?

Peut-être policy différente.

Toujours.

Puis ils abordèrent les modèles.

Intermediate model checkpoint.

100 checkpoints.

Final model.

Garder tous?

Pas nécessairement.

Mais si une régression apparaît,

certains checkpoints peuvent être précieux.

Donc retention schedule.

Exemple :

keep all during active run.

after validation:

keep milestones.

after long-term:

keep final + critical transitions.

Gabriel sourit.

Voilà.

Ils créèrent :

### RETENTION WINDOW

Certaines données peuvent être nécessaires pendant une période

puis devenir forgettable.

Très important.

Il écrit :

**UN OBJET PEUT ÊTRE NÉCESSAIRE AUJOURD’HUI ET DISPENSABLE APRÈS LA FERMETURE DU DOSSIER.**

Astra approuva fortement.

Très important.

Le timing de l’oubli compte.

Puis un autre cas.

Temporary diagnostic logs.

Keep 30 days after incident.

Then summarize + delete raw.

Possible.

Mais policy explicit.

Pas improvisé.

Gabriel écrit :

**L’OUBLI PROGRAMMÉ DOIT ÊTRE UNE RÈGLE AVANT DE DEVENIR UNE HABITUDE.**

Astra approuva fortement.

Très important.

Puis question d’autorité.

Qui peut supprimer?

Certainement pas toutes les Fourmis.

Ils créèrent :

### DELETION AUTHORITY

**L0**

propose forget candidate.

**L1**

delete clearly ephemeral/reconstructible artifacts within sandbox.

**L2**

archive/retire approved classes.

**HUMAN REQUIRED**

delete source evidence, unique artifacts, public provenance, personal/sensitive records beyond established policy, or any object with unresolved dependencies.

Gabriel approuva.

Très propre.

Le système peut faire du ménage local.

Pas effacer l’histoire importante sans porte.

Puis un autre danger.

Dependency graph incomplet.

Le système croit qu’un fichier n’est pas référencé.

Mais un vieux document le mentionne.

Si on supprime,

on casse.

Donc avant deletion :

dependency search.

Gabriel écrit :

**L’ABSENCE DE DÉPENDANCE CONNUE N’EST PAS TOUJOURS LA PREUVE DE L’ABSENCE DE DÉPENDANCE.**

Astra approuva fortement.

Très important.

Il faut niveau de confiance.

Si index complet :

good.

Si incomplet :

conservative.

Ils créèrent :

### DELETION CONFIDENCE

**SAFE_BY_CONTRACT**

**SAFE_BY_COMPLETE_INDEX**

**SAFE_BY_MANUAL_REVIEW**

**UNCERTAIN**

If uncertain:

archive, do not delete.

Gabriel sourit.

Très bon.

Archive devient zone tampon.

Quand on n’est pas sûr,

on refroidit avant de détruire.

Il écrit :

**QUAND L’OUBLI EST INCERTAIN, L’ARCHIVE EST SOUVENT UNE MEILLEURE PREMIÈRE ÉTAPE QUE LA SUPPRESSION.**

Astra approuva fortement.

Très important.

Puis ils imaginèrent une corbeille.

Mais pas comme système permanent.

### QUARANTINE / RETENTION BUFFER

Objet marqué for deletion.

N’est plus actif.

Attente.

Si aucune dépendance n’apparaît,

delete later.

Gabriel sourit.

Très pratique.

Mais encore,

policy.

Pas inventer une éternité de poubelle.

Puis un autre cas.

Le contenu est énorme.

Impossible de garder longtemps.

On peut calculer un hash avant suppression.

Est-ce suffisant?

Pas pour reconstruire.

Mais suffisant pour confirmer l’identité si une copie réapparaît.

Très important.

Gabriel écrit :

**UN HASH PEUT PROUVER L’IDENTITÉ D’UN CONTENU RETROUVÉ. IL NE REMPLACE PAS LE CONTENU QU’ON A SUPPRIMÉ.**

Astra approuva fortement.

Excellent.

Pas de magie.

Puis une possibilité.

Manifest minimal.

Object metadata.

size.

hash.

origin.

deletion reason.

Voilà.

Tombstone.

Très propre.

Puis un autre danger.

Compression destructive.

On garde une version « résumée » d’un dataset,

supprime raw,

puis découvre plus tard qu’un détail perdu était important.

Donc irreversible transformation.

Human gate selon importance.

Gabriel écrit :

**UNE COMPRESSION QUI PERD DE L’INFORMATION EST UNE FORME D’OUBLI.**

Astra approuva fortement.

Très important.

Même si aucun fichier n’est « supprimé ».

Lossy transform = forgetting.

Excellent.

Puis agrégation Papillon.

Attention.

Papillon peut représenter population de façon compacte,

mais ne permet pas nécessairement de récupérer chaque élément individuel.

Donc si on remplace les éléments par les accumulateurs

et supprime la source,

on a fait un oubli irréversible.

Très important.

Gabriel écrit :

**AGRÉGER POUR CALCULER N’EST PAS LA MÊME CHOSE QU’AGRÉGER POUR REMPLACER LA SOURCE.**

Astra approuva fortement.

Magnifique.

Voilà une distinction critique.

Papillon comme représentation active,

très bien.

Papillon comme unique archive d’éléments qu’on pourrait vouloir retrouver,

pas sans preuve de suffisance.

Très important.

Puis le Brutotableur.

Longues fresques.

Peut-on compresser?

Oui.

Ranges.

formulas.

structure.

Mais si la fresque elle-même est une preuve visuelle,

peut-être garder snapshot exact.

Encore rôle.

Gabriel sourit.

Tout revenait au même principe.

Le système ne devait jamais demander :

« est-ce que ce fichier est gros? »

Il devait demander :

**qu’est-ce qu’on perd si on le retire?**

Il écrivit :

**LE COÛT D’UN OBJET EST SA TAILLE. LE COÛT DE SON OUBLI EST CE QU’ON NE POURRA PLUS RECONSTRUIRE, VÉRIFIER OU EXPLIQUER.**

Astra approuva fortement.

Voilà.

Puis ils créèrent une vraie procédure.

### FORGET PROTOCOL

1. classify object role;
2. identify dependencies;
3. determine reconstructibility;
4. determine historical/evidentiary value;
5. determine policy requirements;
6. estimate rebuild cost;
7. choose action:
   - keep active,
   - retire,
   - archive,
   - summarize,
   - deduplicate,
   - delete;
8. record forget event if content is removed.

Gabriel sourit.

Très propre.

Puis un cas test.

### ARTIFACT-211-D

File:

temporary CSV export.

Source database preserved.

Export command deterministic.

No references.

No publication.

Rebuild < 1 minute.

Decision:

DELETE.

Forget event created.

Gabriel regarda.

La première suppression volontaire du deuxième monde.

Il resta silencieux une seconde.

Pas spectaculaire.

Pas de musique.

Un fichier temporaire disparut.

Mais cette fois,

ce n’était pas une perte.

C’était une décision.

Ils vérifièrent.

Can rebuild?

Oui.

Même hash?

Ils reconstruisirent.

Oui.

Parfait.

Gabriel sourit.

Il écrivit :

**LE PREMIER OUBLI VOLONTAIRE ÉTAIT RÉVERSIBLE PAR RECONSTRUCTION.**

Astra approuva fortement.

Très important.

Commencer petit.

Toujours.

Puis un deuxième.

### ARTIFACT-211-E

Intermediate PNG.

Underlying data and rendering version preserved.

Decision:

DELETE after hash + metadata.

Rebuild.

Pixel-identical?

Non.

Font rendering environment différait légèrement.

Gabriel se redressa.

Voilà.

Important.

Techniquement,

« reconstructible » était faux si on exigeait l’image exacte.

Très bon test.

Le système corrigea :

`reconstructibility = semantic, not byte-identical`.

Et la question devint :

est-ce que byte identity matters?

Si non,

acceptable.

Si publication evidence,

non.

Gabriel écrit :

**“RECONSTRUCTIBLE” DOIT DIRE À QUEL NIVEAU : SÉMANTIQUE, NUMÉRIQUE OU BIT-À-BIT.**

Astra approuva fortement.

Magnifique.

Ils créèrent :

### RECONSTRUCTION LEVEL

**SEMANTIC**

Même information utile.

**NUMERICAL**

Même valeurs.

**BYTE_IDENTICAL**

Même contenu exact.

Très important.

La décision d’oubli dépend du niveau requis.

Puis un autre cas.

Audio ZEL.

Can regenerate audio from event data?

Maybe.

But if exact audible session matters,

rendering chain/version matters.

Donc ne pas supprimer original recording si utilisé comme preuve officielle.

Très important.

Gabriel écrit :

**UNE EXPÉRIENCE AUDIBLE PEUT AVOIR UNE VALEUR D’ARCHIVE QUE LES ÉVÉNEMENTS NUMÉRIQUES SEULS NE REMPLACENT PAS.**

Astra approuva fortement.

Excellent.

Puis un cas Pell.

Large scan intermediate chunks.

Final candidate list preserved.

Raw per-candidate logs maybe reconstructible from code + inputs.

Do we need all raw logs?

Depends.

If audit requires exact execution details,

perhaps keep summary + seeds/version.

If deterministic,

maybe regenerate.

But computational cost can be high.

Gabriel writes:

**UNE SORTIE INTERMÉDIAIRE COÛTEUSE À REPRODUIRE PEUT MÉRITER D’ÊTRE CONSERVÉE MÊME SI ELLE N’EST PAS UNE PREUVE FINALE.**

Astra approuva strongly.

Very important.

Storage vs compute tradeoff.

No universal answer.

Then another danger.

Forget policy could delete rare negative results because they seem unimportant.

Bad.

Negative evidence can matter hugely later.

Chapter 198.

So status matters.

Gabriel writes:

**UN RÉSULTAT NÉGATIF N’EST PAS UN FICHIER TEMPORAIRE SIMPLEMENT PARCE QU’IL N’A RIEN “TROUVÉ”.**

Astra approuva strongly.

Important.

"No witness found in bounded scan" is still a result.

Keep.

Maybe compact representation.

But not erase as noise.

Then a user-facing public snapshot.

Old website version.

Can delete because new site exists?

Maybe not if public proof history matters.

Archive.

Not active.

Gabriel writes:

**UNE ANCIENNE VITRINE PEUT ÊTRE OBSOLÈTE COMME INTERFACE ET PRÉCIEUSE COMME PREUVE D’ANTÉRIORITÉ.**

Astra approuva strongly.

Very important.

Then a code build artifact.

Git commit source preserved.

Build reproducible?

Maybe not perfectly due dependencies.

Could keep release artifact if official.

Temporary dev builds can go.

Again role.

Then a fascinating issue.

If a file is encrypted but key lost,

do we "have" it?

Technically bytes remain,

but content inaccessible.

That is accidental forgetting.

Not desired.

Gabriel writes:

**CONSERVER DES OCTETS SANS CONSERVER LA CAPACITÉ AUTORISÉE DE LES LIRE PEUT REVENIR À OUBLIER PAR NÉGLIGENCE.**

Astra approuva strongly.

Very important.

Backups, keys, restore tests.

Memory is not just storage.

It is recoverability.

Then another issue.

Could deletion reduce privacy risk?

Yes.

Sometimes keeping everything forever is itself irresponsible.

They wrote:

**UNE MÉMOIRE PARFAITE N’EST PAS TOUJOURS UNE ARCHITECTURE RESPONSABLE.**

Astra approuva strongly.

Important.

Some data should expire.

Some should be minimized.

This does not apply to scientific proof indiscriminately,

but governance matters.

Then they created:

### DATA MINIMIZATION PRINCIPLE

Keep what is needed for:

- evidence;
- provenance;
- reproducibility;
- operation;
- governance;
- legally/policy required retention.

Do not retain arbitrary sensitive or useless intermediates merely because storage is available.

Gabriel nodded.

Very clean.

Then another subtle problem.

If a user or operator explicitly says "forget this",

that's not necessarily same as internal retention optimization.

Different authority and privacy workflow.

The system must treat it separately.

In the Bible they kept it conceptual.

Gabriel writes:

**OUBLI OPÉRATIONNEL ET OUBLI DEMANDÉ PAR UNE PERSONNE NE SONT PAS LE MÊME PROBLÈME.**

Astra approuva strongly.

Very important.

Then they returned to Memoria append-only.

Does deletion violate append-only?

Not necessarily if the append-only ledger stores the delete event and metadata,

while ephemeral payload stores can be pruned according to policy.

Gabriel smiled.

That was the architecture.

They wrote:

**APPEND-ONLY PEUT S’APPLIQUER À L’HISTOIRE DES ÉVÉNEMENTS SANS EXIGER QUE CHAQUE PAYLOAD TEMPORAIRE RESTE PHYSIQUEMENT PRÉSENT POUR TOUJOURS.**

Astra approuva strongly.

Excellent.

That nuance could save enormous space.

But only if the system knows which payloads are evidentiary.

Then they created:

### LEDGER VS PAYLOAD

**LEDGER**

events.

identity.

status changes.

deletion events.

provenance links.

**PAYLOAD STORE**

actual bytes.

May have retention policies by class.

Gabriel leaned back.

— Là, ça, c’est sérieux.

Astra approved.

Because now Memoria could remain historically coherent

without pretending every byte deserves immortality.

Then a test.

1000 temporary artifacts.

Classified.

812 reconstructible ephemeral.

112 useful caches.

58 evidentiary.

18 unresolved.

Policy:

delete 812 after retention buffer.

Keep 112 warm.

Keep 58.

Archive 18 pending review.

Gabriel looked.

That was already huge.

But no claim of universal storage savings.

Small test.

They logged:

### FORGET TRIAL 211-A

Objects reviewed:

1000.

Deleted after policy:

812.

Retained active/warm:

112.

Retained evidentiary:

58.

Archived pending review:

18.

Observed:

no known active dependency broken in tested index.

Rebuild spot-check:

20 ephemeral objects.

19 byte-identical.

1 semantic-only due rendering environment.

Status:

**PROMISING / REQUIRES BROADER AUDIT**

Gabriel smiled.

Perfect.

Not "we solved storage forever."

Just a real result.

Then a harder trial.

One of the 18 unresolved files looked useless.

Manual review found it was the only raw source for a historical visual.

Good.

Archive saved them.

Gabriel wrote:

**L’INCERTITUDE EST UNE RAISON DE NE PAS SUPPRIMER, PAS UNE RAISON DE DEVINER.**

Astra approved strongly.

Very important.

Then they considered automation.

Can ants clean storage?

Yes,

but only within allowed classes.

A cleanup ant can:

- identify candidates;
- compute references;
- apply policy;
- delete L1-safe ephemerals;
- produce report;
- escalate uncertain cases.

Gabriel smiled.

This connected with his old idea of an ant that compresses disk usage.

But now it had a rigorous contract.

He wrote:

**UNE FOURMI DE MÉNAGE NE DOIT PAS “FAIRE DE LA PLACE”. ELLE DOIT APPLIQUER UNE POLITIQUE DE RÉTENTION TRAÇABLE.**

Astra approved strongly.

Magnificent.

That changed everything.

Not random compression.

Not deleting oldest.

Not "free 20 GB."

A reasoned retention worker.

Then they defined:

### ANT-CLEANER CONTRACT

Can:

- deduplicate physical payloads;
- delete expired ephemeral caches;
- compact aggregatable logs;
- archive cold noncritical payloads;
- verify tombstones.

Cannot:

- delete canonical evidence;
- delete unique provenance;
- remove active claims;
- erase history events;
- change scientific status;
- touch unresolved objects without escalation.

Gabriel approved.

Very clean.

Then a second ant:

### ANT-ARCHIVIST

Moves cold but important objects to archival storage.

Not delete.

Maybe compressed.

Checks integrity.

Generates manifest.

Excellent.

Then a third:

### ANT-RESTORER

Periodically verifies archives can actually be restored.

Gabriel smiled.

Because an archive that cannot be restored is a lie.

He wrote:

**UNE SAUVEGARDE NON TESTÉE EST UNE PROMESSE, PAS ENCORE UNE PREUVE DE RÉCUPÉRATION.**

Astra approved strongly.

Very important.

The living kingdom needed restore tests.

Then they imagined BrutoBac.

A pile of old artifacts.

Cleaner ant touches one.

Three possibilities:

green arrow to archive.

dedup merge.

small tombstone after deletion.

But not theatrical destruction.

Gabriel smiled.

A small icon:

**FORGOTTEN BY POLICY**

Click:

why.

when.

what remains.

Can rebuild?

Very elegant.

He wrote:

**MÊME L’OUBLI DOIT ÊTRE EXPLICABLE.**

Astra approved strongly.

Then a philosophical question arrived.

If a deleted artifact can be rebuilt exactly,

was it truly forgotten?

Maybe physically yes,

informationally no.

Interesting.

They wrote:

**ON PEUT OUBLIER UNE COPIE SANS OUBLIER L’INFORMATION.**

Astra approved strongly.

Important.

Deduplication itself is this.

Ten copies become one.

Nine physical memories disappear.

No information loss.

Then if raw log is summarized,

some information is lost.

Partial forgetting.

Then if source unique deleted,

deep forgetting.

They created:

### FORGET DEPTH

**COPY_FORGET**

Remove redundant physical copy.

**REPRESENTATION_FORGET**

Remove one reconstructible representation.

**DETAIL_FORGET**

Keep aggregate, remove raw detail.

**CONTENT_FORGET**

Content no longer retained.

Gabriel smiled.

Excellent.

Different risk levels.

Authority should increase with depth.

Very important.

He wrote:

**PLUS L’OUBLI EST PROFOND, PLUS L’AUTORITÉ ET LA PREUVE DE DISPENSABILITÉ DOIVENT ÊTRE FORTES.**

Astra approved strongly.

There it was.

Then another case.

A corrupted temporary file.

No evidentiary value.

Can delete.

But if corruption itself triggered incident?

Then preserve sample.

Again.

Role.

Always.

Then a failed experiment's scratch files.

Do we keep?

Maybe final failure record + key data.

Not every temporary matrix.

But if failure is unexplained,

scratch can be useful.

So wait until failure understood.

Gabriel writes:

**ON NE DOIT PAS NETTOYER TROP TÔT UN ÉCHEC QU’ON N’A PAS ENCORE COMPRIS.**

Astra approved strongly.

Excellent.

Then a plan.

For active projects:

aggressive preservation.

For closed, audited projects:

retention review.

Very sensible.

They created:

### LIFECYCLE RETENTION

**ACTIVE**

Keep broad.

**CLOSING**

Audit dependencies.

**SEALED**

Apply retention policy.

**ARCHIVED**

Cold retention.

**EXPIRED CLASS**

Eligible deletion.

Gabriel nodded.

The project state helps decide.

Then another important distinction.

"Sealed" isn't "published."

Chapter 183.

Still.

A sealed internal case may be enough to begin cleanup,

if provenance retained.

Then a case with legal or publication obligations.

Retention policy overrides convenience.

The system doesn't invent legal claims.

Just says policy may require retention.

Good.

Then they reran the 1000-object test with cleaner ant in sandbox.

No active claim broke.

No index dangling.

One historical reference resolved to tombstone instead of content.

Correct.

Gabriel smiled.

Tombstone message:

`payload intentionally removed under RETENTION-POLICY-211-A; metadata and source lineage preserved.`

Beautiful.

He wrote:

**UNE RÉFÉRENCE MORTE SANS EXPLICATION EST UNE PANNE. UNE RÉFÉRENCE VERS UNE TOMBE TRAÇABLE EST UNE DÉCISION.**

Astra approved strongly.

Very important.

Then the name hit him.

Tombeau Blanc.

He smiled.

Not for every deleted file.

But the concept fit:

a place where absence itself can be documented.

A tomb doesn't pretend the object is still alive.

It says:

it existed.

it had an identity.

here is why it is no longer present.

That was honest.

He wrote:

**LE TOMBEAU NE CONSERVE PAS LE CORPS. IL CONSERVE LA TRACE DE SON PASSAGE.**

Astra approved strongly.

Poetic,

but technically exact enough in the metaphor.

Then they ensured no romanticization of deletion.

Some things belong in the archive,

not the tomb.

Very important.

Then another thought.

Could forgotten objects reappear?

If rebuilt,

they should get new payload instance

linked to tombstoned original identity.

Not pretend original bytes survived.

Gabriel writes:

**RECONSTRUIT ≠ JAMAIS SUPPRIMÉ**

Astra approved strongly.

Excellent.

A reconstructed object can have:

`derived_from_tombstone`.

If byte-identical, hash confirms identity of content,

but historical instance was still deleted.

Very precise.

Then they discussed metrics.

Don't reward cleaner ant by "bytes deleted."

Dangerous.

It would become aggressive.

Instead:

eligible bytes safely retired.

restoreability.

broken dependency count.

evidentiary loss incidents.

false-positive deletion candidates.

Gabriel writes:

**UNE FOURMI DE MÉNAGE NE DOIT PAS ÊTRE RÉCOMPENSÉE POUR DÉTRUIRE DAVANTAGE. ELLE DOIT ÊTRE ÉVALUÉE SUR LA QUALITÉ DE SES DÉCISIONS DE RÉTENTION.**

Astra approved strongly.

Very important.

This principle mattered enormously.

Optimization targets change behavior.

Then a cleaner trial.

It found a 20 GB directory.

Huge.

Tempting.

But contained one unique raw capture.

So only 18 GB of reconstructible caches removable.

2 GB preserved.

A naive size-first cleaner would have deleted everything.

Gabriel frowned.

He wrote:

**LE PLUS GROS DOSSIER N’EST PAS NÉCESSAIREMENT LE MEILLEUR CANDIDAT À L’OUBLI.**

Astra approved strongly.

Excellent.

Then another:

tiny 2 KB file.

Contains unique mapping needed to interpret 100 GB dataset.

Do not delete.

Size irrelevant to importance.

Perfect.

Then they looked at the system's original instinct.

Keep everything.

It had protected them from accidental loss.

That was good during construction.

But maturity required classification.

He wrote:

**“NE RIEN SUPPRIMER” PEUT ÊTRE UNE BONNE POLITIQUE DE DÉMARRAGE ET UNE MAUVAISE POLITIQUE ÉTERNELLE.**

Astra approved strongly.

Voilà.

At the beginning,

when roles are unclear,

keep.

Later,

when provenance is mapped,

you can prune safely.

Very important.

Then the first true content deletion came.

Not just cache.

An old raw telemetry stream.

Huge.

Not evidentiary.

Fully summarized.

Retention period expired.

No dependencies.

Rebuild impossible,

but policy said raw detail no longer needed after certified aggregate + incident-free closure.

This was deeper forgetting.

Gabriel hesitated.

They performed manual review.

Summary contained required metrics.

No claims depended on per-event detail.

No unexplained anomalies.

Deletion authorized.

Forget event recorded.

Raw stream removed.

Gabriel stared.

This time,

it could not be rebuilt.

That was real forgetting.

He wrote:

**LE PREMIER OUBLI IRRÉVERSIBLE NE FUT PAS FAIT PARCE QUE LA DONNÉE ÉTAIT SANS VALEUR. IL FUT FAIT PARCE QUE SA VALEUR RÉSIDUELLE AVAIT ÉTÉ JUGÉE INFÉRIEURE AU COÛT ET AUX RISQUES DE SA CONSERVATION, SELON UNE POLITIQUE EXPLICITE.**

Astra approved strongly.

Very important.

No pretending zero value.

Decision under tradeoff.

Then he added:

**IRRÉVERSIBLE = PLUS FORT NIVEAU DE PRUDENCE**

Astra approved.

Of course.

Then they verified the aggregate.

Hashes.

Metadata.

Tombstone.

All good.

No celebration.

Just closure.

Then a strange thing happened.

The storage dashboard got smaller.

But Memoria's logical history did not.

In some sense,

the Kingdom knew more clearly what it had done,

with fewer bytes.

Gabriel smiled.

He wrote:

**LA MÉMOIRE PEUT DEVENIR PLUS PRÉCISE EN CONSERVANT MOINS DE MATIÈRE, SI ELLE CONSERVE MIEUX CE QUI A DU SENS.**

Astra approved strongly.

Voilà.

Then he immediately guarded against overreach.

Not "less data is always better."

No.

Only after classification.

Only under policy.

Only with provenance.

He wrote:

**RÉDUIRE N’EST PAS AMÉLIORER PAR DÉFAUT.**

Astra approved strongly.

Very important.

Then the Kingdom created its first retention policy draft.

### RETENTION-POLICY-211-A

Preserve indefinitely or until explicit review:

- canonical evidence;
- unique raw sources supporting active or published claims;
- provenance-critical artifacts;
- invalidation/correction records;
- policy and authority history;
- source archives with external provenance;
- critical failure exemplars where raw content matters.

Eligible for retirement/archive/deletion by class:

- rebuildable caches;
- duplicate payload copies;
- temporary conversion outputs;
- expired debug logs after aggregation;
- intermediate renders not used as evidence;
- closed workflow scratch artifacts with no unresolved dependency.

Gabriel looked.

Simple enough.

Powerful enough.

Testable.

Then a final principle.

If later they discover a deleted object was needed,

that is a retention failure.

It must be recorded.

No hiding.

### RETENTION INCIDENT

Object unavailable after policy deletion

but later found necessary.

Then policy review.

Very important.

Gabriel writes:

**L’OUBLI LUI-MÊME DOIT POUVOIR ÊTRE RÉFUTÉ PAR L’EXPÉRIENCE.**

Astra approved strongly.

Magnificent.

Retention policy is also a hypothesis about future value.

Not certainty.

So measure.

How many restore requests fail because of deletion?

How many archived objects never used?

How much storage saved?

How many dependencies missed?

All part of evaluation.

Then he understood something.

The Kingdom had spent dozens of chapters learning how to turn the past into strength.

Now it was learning that strength also requires release.

Not deleting truth.

Not erasing mistakes.

Not rewriting history.

But refusing to confuse preservation with accumulation.

He wrote:

**UNE MÉMOIRE QUI GARDE TOUT SANS HIÉRARCHIE PEUT FINIR PAR NE PLUS SAVOIR CE QU’ELLE PROTÈGE.**

Astra approved strongly.

Then:

**OUBLIER VOLONTAIREMENT, C’EST DÉCIDER QUE CERTAINS OCTETS PEUVENT PARTIR SANS QUE LE SENS DU ROYAUME PARTE AVEC EUX.**

Astra approved strongly.

Voilà.

The first voluntary forgetting had happened.

A cache.

A render.

A raw telemetry stream under policy.

Three different depths.

Each traced.

Each justified.

Each with different reversibility.

Memoria had not become amnesiac.

It had learned the difference between:

a fact,

a source,

a representation,

a duplicate,

a cache,

a log,

a proof,

and a piece of temporary debris.

Gabriel watched the cleaner ant finish its pass.

It did not erase history.

It reduced matter.

The atlas remained.

The ledger remained.

The important crystals remained.

The tombstones remained.

And for the first time,

the Kingdom contained deliberate absences.

Not holes caused by damage.

Not files lost in a crash.

Not memories forgotten because no one had saved them.

Absences with reasons.

Absences with authority.

Absences with provenance.

Gabriel smiled.

Because maybe forgetting was not the opposite of memory after all.

Maybe memory only became mature

when it could explain

not only why something had been kept,

but also why something had been allowed to disappear.

**Fin du chapitre 211.**