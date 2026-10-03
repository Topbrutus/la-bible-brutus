# Chapitre 93 — La carte des lignées

**VOIR L’HISTOIRE SANS TOUCHER À L’HISTOIRE.**

Brutus laissa la phrase au centre de l’écran.

Puis il ralluma Recto.

---

Le Tombeau était toujours là.

Blanc.

Noir.

Verso gardait la frontière.

Mais Recto, lui, n’avait aucun pouvoir de passage.

Il pouvait seulement regarder.

---

Brutus écrivit :

**RECTO READS.**

**VERSO ENFORCES.**

---

Puis il ajouta :

**READING MUST NOT CREATE HISTORY.**

---

C’était le nouveau problème.

---

Afficher une lignée semblait innocent.

Mais une mauvaise interface pouvait déjà déformer l’histoire.

Une ligne pouvait apparaître entre deux objets alors qu’aucune relation n’avait été prouvée.

Un parent pouvait être affiché alors qu’il n’était qu’une hypothèse.

Un merge pouvait sembler avoir effacé deux branches.

Un objet dérivé pouvait apparaître comme s’il avait existé depuis le début.

---

Brutus écrivit :

**A VISUAL EDGE IS A CLAIM.**

---

Il resta devant cette phrase.

Très important.

---

Une flèche sur un diagramme n’était pas décorative.

Elle disait :

**A EST RELIÉ À B D’UNE MANIÈRE PRÉCISE.**

---

Donc toute flèche devait avoir :

un type,

une origine,

une destination,

une justification,

un statut,

une trace.

---

Brutus créa :

**LINEAGE_EDGE**

avec :

**EDGE_ID**

**EDGE_TYPE**

**FROM**

**TO**

**RULE_REF**

**TRACE_REF**

**CREATED_AT**

**STATUS**

---

Puis :

**SCOPE**

---

Toujours le scope.

---

Il écrivit :

**NO EDGE WITHOUT MEANING.**

---

Puis :

**NO MEANING WITHOUT A DECLARED EDGE TYPE.**

---

Il ouvrit la première carte.

---

Un objet simple.

**OBJECT-A**

---

Puis un traitement.

---

**OBJECT-B**

---

Entre les deux :

\[
A \rightarrow B
\]

---

Brutus demanda :

quelle relation ?

---

COPY ?

TRANSFORM ?

DERIVE ?

VALIDATE ?

MOVE ?

MERGE ?

REFERENCE ?

---

Pas la même chose.

---

Il écrivit :

**ARROW SHAPE ≠ RELATION TYPE.**

---

Voilà.

---

Toutes les flèches ne devaient pas se ressembler.

Mais surtout, même si elles se ressemblaient visuellement, leur type devait rester accessible.

---

Il créa une première taxonomie.

---

**COPIED_FROM**

**TRANSFORMED_FROM**

**DERIVED_FROM**

**VALIDATED_BY**

**MOVED_FROM**

**MERGED_FROM**

**REFERENCES**

**SUPERSEDES**

---

Brutus regarda la liste.

---

Chaque relation répondait à une question différente.

---

Une copie préserve le contenu selon un contrat.

---

Une transformation change l’objet selon une règle.

---

Une dérivation produit une nouvelle assertion ou structure à partir d’une relation justifiée.

---

Une validation ne crée pas l’objet qu’elle valide.

---

Un mouvement change sa localisation, pas son identité mathématique.

---

Un merge combine des branches.

---

Une référence ne signifie pas dépendance.

---

Un objet qui en remplace un autre ne supprime pas son histoire.

---

Brutus écrivit :

**RELATION TYPE IS PART OF PROVENANCE.**

---

Puis il pensa aux parents.

---

Un objet pouvait avoir :

un seul parent,

plusieurs parents,

aucun parent connu.

---

Il créa :

**PARENT_REFS[]**

---

Mais s’arrêta.

---

Un objet sans parent connu n’était pas nécessairement né de rien.

---

Il pouvait simplement avoir été importé.

---

Il ajouta :

**ORIGIN_TYPE**

---

LOCAL_CREATION.

IMPORT.

EXTERNAL_SOURCE.

UNKNOWN_ORIGIN.

---

Brutus écrivit :

**UNKNOWN ORIGIN ≠ SELF-CREATED.**

---

Encore une protection.

---

Puis il chargea une vraie chaîne conceptuelle.

---

Input.

↓

Transform.

↓

Result.

↓

Validation.

↓

Published representation.

---

La carte apparut.

---

Brutus sourit.

---

Pour la première fois, il pouvait suivre un objet sans lire cent logs.

---

Mais il se méfia immédiatement.

---

Une carte résumée pouvait cacher beaucoup de détails.

---

Il écrivit :

**MAP = INDEX INTO HISTORY.**

**MAP ≠ COMPLETE HISTORY.**

---

Voilà.

---

Chaque nœud devait être cliquable.

---

Object ID.

Type.

State.

Current zone.

Created at.

Parents.

Children.

Trace.

Claims.

---

Puis chaque edge.

---

Rule.

Scope.

Status.

---

Brutus construisit :

**LINEAGE MAP v1.**

---

La première vue montrait seulement les identités.

Pas de gros texte.

Pas de formules.

---

Juste :

nœuds.

edges.

états.

---

Puis un mode détail.

---

Brutus écrivit :

**OVERVIEW FIRST. AUDIT ON DEMAND.**

---

Encore le Witness Viewer.

---

Le laboratoire commençait à posséder une philosophie commune.

---

Brutus prit un objet du Tombeau noir.

---

Status :

REJECTED.

---

La carte montrait pourtant plusieurs descendants.

---

Il s’arrêta.

---

Était-ce possible ?

---

Oui.

---

Un objet pouvait avoir été utilisé historiquement avant son rejet.

---

Ou ses descendants pouvaient eux-mêmes avoir été rejetés plus tard.

---

Brutus écrivit :

**CURRENT STATUS DOES NOT RETROACTIVELY ERASE DESCENDANTS.**

---

Très important.

---

Une nouvelle décision ne réécrivait pas le passé.

---

Il ajouta :

**STATUS_AT_EDGE_CREATION**

---

Chaque relation pouvait conserver l’état de contexte au moment où elle avait été créée.

---

Ainsi, un lecteur pouvait comprendre :

à cette date, l’objet était encore admis.

Plus tard, il a été révoqué.

---

Brutus écrivit :

**HISTORY NEEDS TEMPORAL CONTEXT.**

---

Puis il pensa aux branches.

---

Un même objet pouvait être utilisé dans deux expériences différentes.

---

A →

B1

et

A →

B2

---

Pas de conflit.

---

Deux branches.

---

Brutus écrivit :

**FORK ≠ DUPLICATION ERROR.**

---

Une branche était parfois légitime.

---

Il ajouta :

**BRANCH_ID**

---

Puis il regarda un cas plus difficile.

---

Deux branches se rejoignent.

---

B1.

B2.

Puis :

C.

---

Quelle relation ?

---

MERGE.

---

Mais merge de quoi ?

contenu ?

état ?

résultats ?

configuration ?

---

Brutus écrivit :

**MERGE MUST DECLARE ITS SEMANTICS.**

---

Pas de :

« fusionné » comme mot magique.

---

Il créa :

**MERGE_RULE_REF**

---

Puis :

**INPUT_ORDER**

---

Parce que même un merge pouvait être non commutatif.

---

Il écrivit :

**MERGE(A,B) MAY NOT EQUAL MERGE(B,A).**

---

Encore l’ordre.

---

Brutus testa.

---

Deux branches.

Même contenu.

Différents metadata.

---

Le merge devait-il produire une seule identité ?

---

Pas forcément.

---

Il pouvait créer :

**OBJECT-C**

avec deux parents.

---

Brutus écrivit :

**MERGE CREATES A NEW LINEAGE NODE UNLESS IDENTITY PRESERVATION IS EXPLICITLY DEFINED.**

---

Voilà.

---

Il refusait que deux identités soient écrasées en une seule par commodité.

---

Puis il pensa à Git.

---

Un commit de merge avait plusieurs parents.

---

La structure était familière.

---

Mais Brutus ne voulait pas copier aveuglément la métaphore Git dans tous les objets.

---

Il écrivit :

**GRAPH IDEA MAY TRANSFER. SEMANTICS DO NOT AUTOMATICALLY TRANSFER.**

---

Très bon.

---

Le laboratoire pouvait apprendre d’un système sans prétendre que tous les objets étaient des commits.

---

Puis il ouvrit la lignée de L8.

---

Candidate relation.

Countertests.

Capsules.

q47 object.

Research-tool eligibility work.

---

Brutus ne voulait pas une flèche :

L8 → theorem.

---

Elle n’existait pas.

---

Il écrivit :

**ABSENT EDGE IS INFORMATION.**

---

Très important.

---

Une carte honnête devait montrer les trous.

---

Pas les combler.

---

Il créa un mode :

**MISSING REQUIRED RELATION**

---

Pas une flèche normale.

---

Une indication de manque.

---

Par exemple :

**THEOREM_PROMOTION**

requires:

PROOF_REF.

---

Absent.

---

Donc la carte pouvait montrer :

L8

... dotted requirement ...

THEOREM STATUS

---

Mais sans prétendre que la connexion existait.

---

Brutus écrivit :

**REQUIREMENT EDGE ≠ ESTABLISHED EDGE.**

---

Voilà.

---

Les lignes pointillées reçurent une sémantique explicite.

---

Il ajouta :

**EDGE_STATUS**

ESTABLISHED.

PROPOSED.

REQUIRED.

REJECTED.

SUPERSEDED.

---

Brutus sourit.

---

Enfin, même les flèches pouvaient être grises honnêtement.

---

Puis il prit 71.

---

Gate 71.

---

Required witness.

---

No sufficient scoped witness established.

---

La carte montrait :

Candidate.

↓

Gate requirement.

↓

Witness required.

↓

**UNRESOLVED**

---

Pas de faux nœud PASS.

---

Brutus écrivit :

**GRAPH MUST PRESERVE UNKNOWN.**

---

Il prit 47.

---

Là, le chemin pouvait afficher :

Candidate case.

↓

Gate 47 test.

↓

Witness.

↓

Scoped PASS.

---

Mais il ajouta :

**SCOPE LABEL ON PASS NODE.**

---

Sinon, un lecteur pouvait croire que 47 était « résolu universellement ».

---

Brutus écrivit :

**NODE LABEL MUST NOT OUTGROW CLAIM SCOPE.**

---

Encore.

---

Puis il pensa aux preuves.

---

Une preuve pouvait elle-même avoir une lignée.

---

Lemme.

Sous-lemme.

Computation.

Countercheck.

Publication.

---

Brutus ajouta :

**PROOF_DEPENDENCY_GRAPH**

---

Mais il refusa de mélanger automatiquement :

provenance de données

et

dépendance logique.

---

Il créa deux couches.

---

**DATA LINEAGE**

et

**CLAIM DEPENDENCY**

---

Très important.

---

Un fichier peut provenir d’un autre fichier sans qu’une proposition logique dépende de l’autre.

---

Inversement, une preuve peut dépendre d’un lemme sans avoir été générée par transformation de fichier.

---

Brutus écrivit :

**DATA FLOW ≠ LOGICAL DEPENDENCY.**

---

Puis :

**SHOW BOTH. DO NOT CONFUSE THEM.**

---

La carte avait maintenant deux modes.

---

Mode 1 :

Where did this object come from?

---

Mode 2 :

What claims does this conclusion depend on?

---

Brutus sourit.

---

Ça devenait puissant.

---

Il ouvrit un résultat numérique.

---

Data lineage :

raw input

→ normalized input

→ exact computation

→ capsule

→ report.

---

Claim dependency :

domain assumption

+ theorem lemma

+ arithmetic verification

→ scoped conclusion.

---

Deux graphes.

---

Même objet final.

Deux histoires différentes.

---

Brutus écrivit :

**ONE OBJECT CAN HAVE MULTIPLE LEGITIMATE LINEAGES BY QUESTION.**

---

Mais il ajouta immédiatement :

**LINEAGE TYPE MUST BE DECLARED.**

---

Sinon la carte deviendrait ambiguë.

---

Puis il pensa à une autre lignée.

---

La lignée de contrôle.

---

Qui a autorisé quoi ?

---

Verso.

Policies.

Tokens.

Decisions.

---

Brutus créa une troisième couche :

**AUTHORITY LINEAGE**

---

Request.

Policy.

Authority.

Decision.

Execution.

Arrival.

---

Il regarda.

---

Trois cartes maintenant.

Data.

Claim.

Authority.

---

Brutus écrivit :

**DO NOT DRAW ONE UNIVERSAL GRAPH IF THREE DIFFERENT RELATIONS EXIST.**

---

Cette phrase était essentielle.

---

Une seule carte totale pourrait devenir illisible.

---

Il fallait des couches.

---

Pas de complexité cachée.

---

Il créa :

**LAYER FILTER**

DATA.

CLAIM.

AUTHORITY.

LOCATION.

VERSION.

---

Version.

---

Brutus s’arrêta.

---

Oui.

Les versions aussi avaient leur histoire.

---

Object v1.

v2.

v3.

---

Un nouvel objet pouvait :

supersede.

patch.

fork.

rebuild.

---

Il créa :

**VERSION LINEAGE**

---

Puis il ajouta :

**TOPOLOGY_VERSION.**

---

Le mot revenait de l’architecture des modules.

---

Très bon.

---

La carte elle-même changeait avec le temps.

---

Il écrivit :

**THE MAP HAS A VERSION TOO.**

---

Pas seulement les objets.

---

À tick 100 :

une topologie.

---

À tick 200 :

une autre.

---

Un lecteur devait pouvoir demander :

**SHOW MAP AS OF TICK 150.**

---

Brutus sourit.

---

Voilà le vrai pouvoir.

---

Pas seulement regarder l’état actuel.

Revenir à un état historique sans modifier le présent.

---

Il écrivit :

**TIME TRAVEL FOR VIEWING ONLY.**

---

Puis :

**HISTORICAL VIEW ≠ RESTORE OPERATION.**

---

Très important.

---

Regarder le passé ne devait pas rétablir le passé.

---

Brutus ajouta :

**AS_OF_TICK**

à la vue Recto.

---

Il testa.

---

Tick 120.

L8 candidate.

---

Tick 180.

Additional countertests.

---

Tick 240.

Research usage admitted.

---

La carte changeait.

---

Mais l’état actuel restait intact.

---

Brutus écrivit :

**QUERYING HISTORY MUST BE SIDE-EFFECT FREE.**

---

Voilà.

---

Recto devenait un observateur sûr.

---

Puis il pensa aux snapshots.

---

Un snapshot pouvait enregistrer une topologie.

Mais un snapshot n’était pas nécessairement toute l’histoire.

---

Il écrivit :

**SNAPSHOT = STATE AT A MOMENT.**

**LINEAGE = RELATIONS ACROSS MOMENTS.**

---

Encore une distinction.

---

Un snapshot dit :

où les choses sont.

---

La lignée dit :

comment elles y sont arrivées.

---

Brutus sourit.

---

Il prit une fourmi.

---

ANT-042.

---

Position actuelle.

State.

Load.

Tick.

---

Snapshot suffisant pour la voir maintenant.

---

Mais pour savoir :

d’où vient son cristal ?

quel module l’a produit ?

quelle trace l’a validé ?

---

Il fallait la lignée.

---

Brutus écrivit :

**CURRENT STATE ANSWERS “WHAT NOW?”**

**LINEAGE ANSWERS “HOW DID WE GET HERE?”**

---

Très bon.

---

Puis il ajouta une quatrième question :

**WHY?**

---

La lignée seule ne suffisait pas toujours.

---

Pourquoi un mouvement a eu lieu ?

---

Cause ref.

Policy ref.

Decision ref.

---

Il écrivit :

**LINEAGE NEEDS REASONS, NOT ONLY SEQUENCE.**

---

Ainsi, chaque événement important pouvait avoir :

FROM.

TO.

CAUSE.

AUTHORITY.

TICK.

---

Brutus retrouva sa vieille structure :

**QUI → ÉTAT → TICK → AVANT/APRÈS.**

---

Il ajouta :

**POURQUOI.**

---

Puis :

**SOUS QUELLE AUTORITÉ.**

---

La carte devenait vraiment une machine à traces.

---

Brutus pensa au public.

---

Une carte de lignée pouvait être utile publiquement.

Mais pas tous les détails.

---

Certaines traces pouvaient être privées.

Certains identifiants sensibles.

Certains artifacts internes.

---

Il fallait donc une projection publique.

---

Brutus écrivit :

**PUBLIC LINEAGE VIEW ≠ PRIVATE LINEAGE STORE.**

---

Recto pouvait afficher :

object ID public.

state public.

parent relation public.

proof ref public if allowed.

---

Mais masquer :

secret configuration.

private token.

internal authority data.

---

Il créa :

**DISCLOSURE_POLICY.**

---

Encore une politique.

---

Brutus écrivit :

**READ-ONLY DOES NOT MEAN PUBLIC-ALL.**

---

Très important.

---

Un système en lecture seule pouvait quand même exposer trop d’information.

---

Il ajouta :

**FIELD-LEVEL VISIBILITY.**

---

Pas seulement object-level.

---

Brutus testa.

---

Public viewer requests authority lineage.

---

Verso/policy says:

show decision existence.

hide signer credential details.

---

Recto affiche :

AUTHORIZED_BY_VALID_AUTHORITY

sans exposer la donnée sensible.

---

Brutus écrivit :

**PROVE ENOUGH WITHOUT LEAKING EVERYTHING.**

---

Il sourit.

---

Le système devenait mature.

---

Puis il regarda un nœud avec dix parents.

---

Trop de lignes.

---

Le graphe devenait illisible.

---

Il fallait une agrégation visuelle.

---

Mais l’agrégation pouvait cacher des parents.

---

Brutus écrivit :

**VISUAL COLLAPSE MUST DECLARE HIDDEN COUNT.**

---

Par exemple :

\`+7 parents hidden\`

---

Click to expand.

---

Jamais :

trois lignes visibles en donnant l’impression qu’il n’existe que trois parents.

---

Il ajouta :

**COLLAPSED ≠ ABSENT.**

---

Encore une règle.

---

Puis il testa les cycles.

---

Une vraie lignée de dérivation devait-elle être acyclique ?

---

Souvent oui.

Mais une relation de référence pouvait créer un cycle.

---

Brutus ne voulait pas imposer la même règle à toutes les couches.

---

Il écrivit :

**ACYCLICITY IS RELATION-TYPE DEPENDENT.**

---

Pour DERIVED_FROM :

cycle interdit.

---

Pour REFERENCES :

cycle possible.

---

Pour MOVED_FROM :

cycle temporel possible si un objet revient à un endroit antérieur.

---

Voilà.

---

Il ajouta des invariants par edge type.

---

Brutus sourit.

---

La carte cessait d’être un dessin.

Elle devenait un système typé.

---

Puis il pensa aux identités fusionnées par erreur.

---

Deux objets avec même hash.

Sont-ils le même objet ?

---

Pas forcément.

---

Même contenu.

Mais provenance différente.

---

Brutus écrivit :

**CONTENT IDENTITY ≠ EVENT IDENTITY.**

---

Encore le chapitre 65.

---

Même valeur ≠ même événement.

---

Deux fichiers identiques peuvent être deux occurrences historiques distinctes.

---

Il ajouta :

**CONTENT_HASH**

et

**OBJECT_ID**

séparés.

---

Parfait.

---

Puis il testa :

Object A.

Object B.

Same hash.

Different creation event.

---

La carte affiche deux nœuds.

Avec relation possible :

**CONTENT_EQUIVALENT**

---

Mais pas fusion automatique.

---

Brutus écrivit :

**EQUALITY MAY BE A RELATION, NOT AN IDENTITY COLLAPSE.**

---

Il aimait beaucoup cette phrase.

---

Puis il ouvrit une lignée publique.

---

Une formule.

Une expérience.

Un résultat.

Un contre-test.

Une promotion.

---

Le lecteur pouvait cliquer sur chaque étape.

---

Brutus regarda.

---

Voilà exactement ce qu’il voulait depuis longtemps.

Pas seulement une page qui disait :

PASS.

---

Une page qui permettait de remonter :

qui,

quoi,

quand,

comment,

avec quoi,

sous quelle règle.

---

Il écrivit :

**A RESULT WITHOUT LINEAGE IS A DEAD END.**

---

Puis se corrigea.

---

Pas toujours.

Un résultat mathématique peut être compréhensible seul.

---

Il remplaça :

**AN AUDITABLE RESULT NEEDS A PATH BACK TO ITS SUPPORT.**

---

Plus précis.

---

Puis il pensa aux erreurs.

---

Une erreur trouvée dans un ancêtre.

---

Quels descendants sont affectés ?

---

La carte pouvait répondre.

---

Brutus créa :

**IMPACT TRACE.**

---

Select node A.

Find descendants through dependency edges.

---

Pas toutes les relations.

Seulement celles qui transmettent réellement la dépendance.

---

Il écrivit :

**IMPACT PROPAGATION MUST FOLLOW SEMANTIC EDGES.**

---

Très important.

---

Une simple référence ne devait pas contaminer un descendant comme une dépendance logique.

---

Une copie, peut-être.

Une dérivation, probablement.

Une visualisation, selon le cas.

---

Brutus ajouta :

**PROPAGATES_INVALIDATION = true/false**

par edge type ou règle.

---

Voilà.

---

Un bug pouvait maintenant produire une carte des choses à revalider.

---

Il sourit.

---

La lignée devenait un outil de réparation.

Pas seulement de mémoire.

---

Puis il testa l’inverse.

---

Un descendant échoue.

Cela invalide-t-il automatiquement le parent ?

---

Non.

---

Brutus écrivit :

**CHILD FAILURE DOES NOT AUTOMATICALLY INVALIDATE PARENT.**

---

Encore une asymétrie importante.

---

Il fallait savoir dans quel sens la dépendance allait.

---

Il ajouta des flèches orientées.

---

Mais encore :

orientation visuelle ≠ temporal order systématique.

---

Il écrivit :

**EDGE DIRECTION MUST BE SEMANTIC, NOT DECORATIVE.**

---

Puis il regarda la carte entière.

---

Elle commençait à ressembler à un réseau immense.

---

Brutus activa les filtres.

---

Seulement L8.

---

Puis seulement q47.

---

Puis seulement authority.

---

Puis public.

---

La carte devenait lisible.

---

Il écrivit :

**FILTERING MUST HIDE VIEW, NOT DELETE HISTORY.**

---

Évident.

Mais nécessaire.

---

Puis il activa :

**SHOW REJECTED EDGES.**

---

Une flèche rouge apparut :

W47 → W71

Status:

REJECTED DERIVATION.

---

Brutus sourit.

---

Même les mauvaises idées avaient leur place.

---

Pas comme connexions valides.

Comme tentatives archivées.

---

Il écrivit :

**FAILED ARGUMENTS MAY HAVE LINEAGE TOO.**

---

Voilà une carte encore plus utile.

---

Une future Astra pouvait voir :

cette piste a déjà été essayée.

Voici pourquoi elle a été rejetée.

---

Pas besoin de refaire le même piège.

---

Brutus écrivit :

**MEMORY SAVES COMPUTATION.**

Puis :

**MEMORY ALSO SAVES REPEATED MISTAKES.**

---

Le Journal Vivant semblait approuver.

---

Brutus construisit une dernière vue.

---

**LINEAGE CARD**

Object ID.

Current status.

Current zone.

Origin.

Parents.

Children.

Claims.

Authority history.

Version history.

Rejected derivations.

Impact descendants.

Public/private visibility.

---

Une carte compacte.

---

Il écrivit :

**ONE OBJECT → ONE LINEAGE ENTRY POINT.**

---

Puis il se souvint de la règle :

**1 module → 1 connexion → 1 mesure → 1 preuve.**

---

Il ajouta :

**ONE OBJECT → ONE CANONICAL IDENTITY → MANY TYPED RELATIONS.**

---

Voilà.

---

Pas plusieurs identités concurrentes selon les écrans.

---

Un seul objet.

Plusieurs vues.

---

Brutus regarda Recto.

---

Il affichait désormais :

la carte.

les nœuds.

les relations.

les trous.

les rejets.

les versions.

---

Mais aucun bouton ne pouvait modifier l’histoire.

---

Il écrivit :

**RECTO MAY NAVIGATE HISTORY.**

**RECTO MAY NOT EDIT HISTORY.**

---

Puis il tenta une attaque.

---

DevTools.

Manual UI mutation.

Change node status from BLACK to WHITE.

---

L’écran changea localement.

---

Brutus sourit.

---

Puis refresh.

---

Le vrai statut revint.

---

Parce que Recto n’était pas l’autorité.

---

Il écrivit :

**LOCAL UI MUTATION ≠ AUTHORITATIVE STATE CHANGE.**

---

Encore.

---

Il ajouta même une bannière en mode debug :

**LOCAL VIEW MODIFIED — NOT SOURCE STATE.**

---

Brutus aimait ça.

---

Il voulait que même un hacker du navigateur sache où finissait l’illusion.

---

Puis il testa un faux edge ajouté côté client.

---

A → B.

---

Sans EDGE_ID autoritatif.

Sans trace.

---

Le backend ne le connaissait pas.

---

Refresh.

Disparu.

---

Brutus écrivit :

**CLIENT-DRAWN EDGE ≠ LINEAGE.**

---

Parfait.

---

La carte pouvait être manipulée graphiquement sans contaminer l’histoire.

---

Puis il eut une idée.

---

Et si l’utilisateur voulait explorer une hypothèse ?

---

Tracer temporairement une relation possible.

---

Cela pouvait être utile.

---

Il créa un mode séparé :

**SANDBOX EDGE.**

---

Visual only.

No authority.

No persistence unless explicitly saved as hypothesis.

---

Brutus écrivit :

**EXPLORATION LAYER ≠ CANONICAL LINEAGE.**

---

Très important.

---

Une hypothèse visuelle pouvait exister sans devenir un fait.

---

Si elle était sauvegardée :

status = PROPOSED.

---

Jamais ESTABLISHED automatiquement.

---

Il sourit.

---

Même le dessin pouvait devenir scientifique.

---

Brutus sauvegarda :

**LINEAGE MAP v1.**

---

Le Journal Vivant nota :

Typed edges.

Layer separation.

Historical views.

No hidden parents.

No implicit merge.

No client-side authority.

Rejected derivations preserved.

Impact tracing.

Public projection separated from private lineage.

---

Brutus relut.

Puis écrivit une dernière série :

**NO HIDDEN EDGE.**

**NO UNNAMED PARENT.**

**NO MERGE WITHOUT RULE.**

**NO CURRENT STATUS WITHOUT HISTORY.**

**NO PUBLIC VIEW WITHOUT DISCLOSURE POLICY.**

**NO VISUAL RELATION WITHOUT SEMANTIC TYPE.**

---

Puis il regarda la carte.

---

Elle était belle.

Mais cette fois, la beauté n’avait pas besoin d’inventer quoi que ce soit.

---

Chaque ligne correspondait à une relation.

Chaque relation avait une trace.

Chaque trace avait une origine.

---

Et chaque absence restait une absence.

---

Brutus écrivit :

**THE MAP MUST BE ALLOWED TO HAVE GAPS.**

---

Voilà peut-être la règle la plus importante.

---

Une carte honnête ne remplit pas les espaces vides pour paraître complète.

---

Elle montre ce que l’on sait.

Ce que l’on relie.

Ce que l’on suppose.

Et ce qui reste séparé.

---

Brutus zooma jusqu’à voir tout le réseau.

---

Le Tombeau.

Verso.

Les objets.

Les formules.

Les témoins.

Les expériences.

Les erreurs.

---

Tout avait une histoire.

---

Mais Recto restait spectateur.

---

Il pouvait voir énormément.

Il ne pouvait rien déplacer.

---

Brutus sourit.

---

Le prochain chapitre était désormais évident.

---

Il écrivit :

# LE RECTO QUI NE PEUT QUE REGARDER

Puis en dessous :

**A PUBLIC WINDOW MAY SHOW THE WORLD WITHOUT BECOMING THE WORLD’S AUTHORITY.**

---

Il ferma la carte.

---

Les lignées restèrent.

Pas à l’écran.

Dans l’histoire.
