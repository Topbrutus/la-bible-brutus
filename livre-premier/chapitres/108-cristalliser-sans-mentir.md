# Chapitre 108 — Cristalliser sans mentir

**CRYSTAL != PROOF**

Brutus écrivit la phrase au centre de l’écran.

Puis une seconde :

**STABILITY OF FORM DOES NOT CREATE CERTAINTY OF CONTENT.**

---

Devant lui reposaient plusieurs objets.

Une formule candidate.

Un résultat expérimental.

Un contre-test.

Une carte GAMEZEL.

Un témoin mathématique.

Un rapport.

---

Certains étaient solides.

D’autres encore discutés.

---

Mais plusieurs avaient une chose en commun.

---

Ils avaient fini de changer.

---

Pas intellectuellement.

Pas épistémiquement.

---

Structurellement.

---

Leur contenu avait atteint une version que le laboratoire voulait conserver telle quelle.

---

Brutus écrivit :

**CRYSTALLIZATION = STABLE PACKAGING EVENT.**

---

Voilà.

---

Pas illumination.

Pas vérité.

Pas consécration.

---

Packaging.

---

Un cristal devait dire :

voici exactement l’objet tel qu’il existait à cette version.

---

Brutus créa :

**CRYSTAL_OBJECT**

avec :

**CRYSTAL_ID**

**SOURCE_OBJECT_ID**

**SOURCE_VERSION**

**CONTENT_HASH**

**PROVENANCE_REF**

**CLAIM_SCOPE**

**EPISTEMIC_STATUS**

**PACKAGING_STATUS**

**CREATED_AT**

**TICK**

**TRACE_REF**

---

Puis :

**CRYSTAL_SCHEMA_VERSION**

---

Il regarda.

---

Une chose était immédiatement importante.

---

Le cristal conservait :

**EPISTEMIC_STATUS**

---

Il ne le remplaçait pas.

---

Une candidate cristallisée restait candidate.

---

Un résultat unresolved cristallisé restait unresolved.

---

Un contre-exemple validé restait contre-exemple validé.

---

Brutus écrivit :

**CRYSTALLIZATION PRESERVES STATUS. IT DOES NOT UPGRADE STATUS.**

---

Très important.

---

Il prit FORMULA-X.

Status :

SUPPORTED_UNDER_SCOPE.

---

Il la cristallisa.

---

Nouveau résultat :

**CRYSTAL-X-001**

Packaging :

CRYSTALLIZED.

Epistemic :

SUPPORTED_UNDER_SCOPE.

---

Pas :

PROVED.

---

Brutus sourit.

---

Exactement.

---

Puis il pensa à la raison de cristalliser.

---

Pourquoi ne pas simplement garder le fichier ?

---

Parce qu’un fichier peut changer.

---

Un nom peut rester identique.

Le contenu peut être remplacé.

---

Le cristal devait être lié à une empreinte.

---

Il écrivit :

**NAME != CONTENT IDENTITY.**

---

Puis :

**CRYSTAL CONTENT MUST BE HASH-BOUND.**

---

Voilà.

---

Le hash protégeait l’identité du contenu.

---

Mais encore :

**HASH != VALIDITY.**

---

Brutus ajouta la règle immédiatement.

---

Un fichier faux pouvait avoir un hash parfait.

---

Le cristal garantissait :

ce contenu n’a pas changé depuis sa cristallisation.

---

Pas :

ce contenu est correct.

---

Il écrivit :

**INTEGRITY OF OBJECT != TRUTH OF CLAIM.**

---

Le chapitre 82 revenait encore.

---

Puis il pensa aux dépendances.

---

Une formule peut dépendre :

d’un dataset,

d’un proof candidate,

d’un code,

d’une policy.

---

Si le cristal ne conserve que le fichier principal, il perd une partie de son contexte.

---

Brutus créa :

**CRYSTAL_MANIFEST**

---

SOURCE_OBJECT.

DEPENDENCIES.

DEPENDENCY_VERSIONS.

METHOD_REFS.

EVIDENCE_REFS.

POLICY_REFS.

LINEAGE_REFS.

---

Puis :

**MANIFEST_HASH**

---

Il écrivit :

**CRYSTAL = CONTENT + CONTEXT MANIFEST.**

---

Voilà.

---

Pas seulement un fichier.

---

Un paquet stable.

---

Puis il pensa à la phrase :

**portable object.**

---

Oui.

---

Un cristal devait pouvoir voyager.

---

GAMEZEL.

Brutus.

Recto.

Archive.

Publication.

---

Mais le transport ne devait pas détacher son origine.

---

Brutus écrivit :

**PORTABLE != ORPHANED.**

---

Puis :

**EVERY CRYSTAL MUST CARRY A PATH BACK TO SOURCE.**

---

Très important.

---

Il créa :

**PEDIGREE**

---

Parent refs.

Source refs.

Creation event.

Promotion history.

Experiment refs.

---

Le mot lui plut.

---

Pedigree.

---

Mais il se méfia encore de la poésie.

---

Il écrivit :

**PEDIGREE IS LINEAGE DATA, NOT PRESTIGE.**

---

Excellent.

---

Un cristal ancien n’était pas meilleur parce qu’il était ancien.

---

Un cristal créé par Astra n’était pas meilleur parce qu’il venait d’Astra.

---

Un cristal cité cent fois n’était pas meilleur à cause du nombre.

---

Brutus écrivit :

**CRYSTAL AGE != QUALITY.**

**CRYSTAL AUTHOR != VALIDITY.**

**CRYSTAL POPULARITY != PROOF.**

---

Puis il pensa au changement.

---

Supposons qu’une faute soit découverte après cristallisation.

---

Peut-on éditer CRYSTAL-X-001 ?

---

Non.

---

Brutus écrivit :

**CRYSTAL IS IMMUTABLE BY IDENTITY.**

---

Une correction crée :

**CRYSTAL-X-002**

---

Avec :

**SUPERSEDES = CRYSTAL-X-001**

---

L’ancien reste.

---

Brutus écrivit :

**EDIT != HISTORY REWRITE.**

---

Puis :

**CORRECTED CRYSTAL = NEW CRYSTAL.**

---

Voilà.

---

Le chapitre 97 revenait.

---

Même identité.

Même philosophie.

---

Puis il pensa aux petites corrections.

---

Typo.

---

Peut-être une nouvelle version de présentation.

---

Mais si le cristal représente une unité de contenu exacte, même la typo change le hash.

---

Brutus décida :

nouvel objet dérivé.

---

Cependant, pour éviter de multiplier inutilement les objets, il sépara :

**CANONICAL_CONTENT**

et

**DISPLAY_METADATA**

---

Brutus écrivit :

**PRESENTATION METADATA MAY CHANGE WITHOUT ALTERING CANONICAL CONTENT WHEN POLICY ALLOWS.**

---

Très important.

---

Titre traduit.

Description.

Thumbnail.

---

Pas nécessairement nouveau cristal.

---

Mais formule.

Données.

Proof artifact.

---

Oui.

---

Nouveau cristal.

---

Puis il pensa aux cristaux composites.

---

Un résultat peut dépendre de 49 cartes.

---

Il pouvait vouloir créer un cristal groupé.

---

Brutus créa :

**COMPOSITE_CRYSTAL**

---

avec :

**MEMBER_CRYSTAL_IDS[]**

---

Puis il écrivit :

**COMPOSITE CRYSTAL != MERGED CLAIM.**

---

Très important.

---

Mettre 49 objets dans un paquet ne fusionnait pas automatiquement leurs claims.

---

Le cristal composite disait seulement :

voici cet ensemble stable.

---

Brutus pensa au cube 7×7.

---

49 cases.

---

Très beau.

---

Il pouvait représenter :

49 cristaux.

---

Mais le visuel ne devait pas créer une relation mathématique entre eux.

---

Il écrivit :

**GRID ADJACENCY != SEMANTIC EDGE.**

---

Encore.

---

Une carte à côté d’une autre n’était pas automatiquement liée.

---

Il ajouta :

**CRYSTAL_SLOT**

---

slot id.

member crystal id.

position.

---

Puis :

**POSITION != DERIVATION.**

---

Très important.

---

L’interface pouvait organiser.

Pas inventer des dépendances.

---

Puis il pensa au cinquantième objet.

---

Les 49 remplissent le cube.

Le 50e reste sur le jeu.

---

Brutus sourit.

---

Il écrivit :

**BATCH SIZE MAY DEFINE PACKAGING, NOT MATHEMATICAL SIGNIFICANCE.**

---

Un groupe de 49 pouvait être un choix architectural.

---

Pas une loi universelle.

---

Puis il pensa à la détection de duplicata.

---

Deux cristaux ont le même CONTENT_HASH.

---

Sont-ils le même cristal ?

---

Pas nécessairement.

---

Le chapitre 97 avait déjà répondu.

---

Même contenu.

Origines différentes.

---

Brutus écrivit :

**SAME CONTENT HASH != SAME EVENT IDENTITY.**

---

Il créa :

**CONTENT_EQUIVALENT_TO**

---

Mais conserva :

deux CRYSTAL_ID.

---

Pourquoi ?

---

Parce que provenance différente.

---

Peut-être deux équipes indépendantes ont produit exactement le même résultat.

---

Cela vaut la peine de le conserver.

---

Brutus écrivit :

**IDENTICAL RESULT CAN HAVE INDEPENDENT PROVENANCE.**

---

Très important.

---

Puis il pensa à la déduplication de stockage.

---

On pouvait stocker une seule copie physique du blob.

---

Mais garder deux identités logiques.

---

Il écrivit :

**STORAGE DEDUPLICATION != LINEAGE COLLAPSE.**

---

Excellent.

---

Puis il pensa au statut :

**CRYSTAL READY**

---

Trop vague.

---

Il créa :

**PACKAGING_STATE**

DRAFT_PACKAGE.

SEALED.

CRYSTALLIZED.

SUPERSEDED.

ARCHIVED.

CORRUPTED_COPY.

---

Brutus écrivit :

**SEALED != VALIDATED.**

---

Encore.

---

Un paquet peut être fermé.

---

Cela ne signifie pas que ses contenus sont corrects.

---

Puis il pensa à la détection de corruption.

---

Read crystal.

Hash mismatch.

---

Status :

**CORRUPTED_COPY**

---

Mais le cristal canonique n’est pas forcément corrompu.

---

Peut-être seulement cette copie.

---

Brutus écrivit :

**COPY CORRUPTION != CANONICAL OBJECT CORRUPTION.**

---

Très important.

---

Il créa :

**COPY_ID**

---

Encore l’identité.

---

Canonical crystal.

Replica copy.

Local cache.

Archive copy.

---

Brutus écrivit :

**CRYSTAL ID != COPY ID.**

---

Voilà.

---

Puis il pensa au transport.

---

Un cristal quitte le serveur A.

Arrive au serveur B.

---

Que faut-il vérifier ?

---

Crystal ID.

Manifest.

Hashes.

Schema.

Dependencies available?

---

Brutus créa :

**CRYSTAL_TRANSFER_RECEIPT**

---

FROM.

TO.

CRYSTAL_ID.

COPY_ID.

CONTENT_HASH.

MANIFEST_HASH.

SENT_AT.

RECEIVED_AT.

VERIFIED_AT.

TRACE_REF.

---

Puis :

**TRANSFER_RECEIVED != CONTENT VERIFIED.**

---

Encore ACK.

---

Il sourit.

---

Le chapitre 120 était encore loin.

Mais la philosophie était déjà là.

---

Un reçu de transport ne prouvait pas l’intégrité.

---

Il ajouta :

**HASH_VERIFIED**

séparé de :

**RECEIVED**

---

Brutus écrivit :

**ARRIVAL != VALIDATION.**

---

Très important.

---

Puis il pensa au cristal comme artifact public.

---

Quelqu’un pouvait télécharger :

CRYSTAL-X.

---

Il devait pouvoir vérifier :

hash.

manifest.

status.

---

Mais pas nécessairement accéder aux secrets internes.

---

Il créa :

**PUBLIC_CRYSTAL_CAPSULE**

---

CRYSTAL_ID.

TITLE.

CONTENT_HASH.

MANIFEST_HASH.

PUBLIC_STATUS.

SCOPE.

CREATED_AT.

PUBLIC_TRACE_REF.

---

Puis :

**PRIVATE_REFS_REDACTED**

si nécessaire.

---

Brutus écrivit :

**PUBLIC VERIFIABILITY AND PRIVATE DISCLOSURE ARE SEPARATE DESIGN PROBLEMS.**

---

Excellent.

---

Puis il pensa à la publication Zenodo.

---

Un cristal pouvait être un excellent paquet de publication.

---

Version figée.

Hashée.

Date.

Auteur.

Méthode.

---

Mais encore :

publication ne crée pas preuve.

---

Il écrivit :

**PUBLICATION CAN PRESERVE A CRYSTAL. IT CANNOT UPGRADE ITS EPISTEMIC STATUS.**

---

Le chapitre 107 revenait.

---

Puis il pensa au mot :

**cristallisation**.

---

Pourquoi ce mot ?

---

Parce qu’un matériau diffus prend une structure stable.

---

Dans Brutus :

idées dispersées.

traces.

résultats.

méthodes.

---

Puis :

un paquet.

---

Brutus écrivit :

**CRYSTALLIZATION REDUCES AMBIGUITY OF FORM.**

---

Pas :

ambiguity of truth.

---

Il ajouta :

**FORM STABILITY != CLAIM CERTAINTY.**

---

Voilà.

---

Puis il pensa aux 36 sons.

---

Le système voulait un son différent pour :

formula found.

crystal assembled.

---

Très bien.

---

Il écrivit :

**FORMULA FOUND EVENT != CRYSTAL ASSEMBLED EVENT.**

---

Donc :

deux sons.

---

Un ding simple peut annoncer :

candidate formula detected.

---

Un son différent :

crystal packaging completed.

---

Mais aucun des deux :

proof accepted.

---

Brutus écrivit :

**SONIFICATION MUST PRESERVE EVENT SEMANTICS.**

---

Très important.

---

Une oreille devait apprendre la différence.

---

Candidate.

Crystal.

Proof.

---

Trois événements.

Trois significations.

---

Pas le même son.

---

Puis il pensa au système qui fabrique automatiquement des cristaux après 49 formules.

---

Danger.

---

Le 50e événement pouvait déclencher un packaging.

---

Mais seulement parce que la règle de batch le dit.

---

Pas parce que 50 possède un sens scientifique particulier.

---

Brutus écrivit :

**AUTOMATIC CRYSTALLIZATION TRIGGER != SCIENTIFIC DISCOVERY RULE.**

---

Puis :

**BATCH THRESHOLD IS OPERATIONAL POLICY.**

---

Voilà.

---

Si policy :

when 49 eligible cards fill grid, crystallize package.

---

Très bien.

---

Mais le statut de chaque carte reste.

---

Il ajouta :

**ELIGIBILITY_FOR_PACKAGING**

séparé de :

**EPISTEMIC_ELIGIBILITY**

---

Encore deux axes.

---

Puis il pensa aux formules rejetées.

---

Peut-on cristalliser une formule rejetée ?

---

Oui.

---

Pourquoi pas ?

---

Elle peut être importante historiquement.

---

Brutus écrivit :

**REJECTED OBJECT MAY BE CRYSTALLIZED AS ARCHIVAL EVIDENCE.**

---

Très important.

---

Un cristal n’était donc pas réservé aux succès.

---

Il pouvait contenir :

une erreur importante.

un contre-exemple.

une voie fermée.

---

Le chapitre 104 rejoignait le chapitre 108.

---

Brutus sourit.

---

Il créa :

**CRYSTAL_PURPOSE**

RESEARCH_RESULT.

ARCHIVAL_RECORD.

COUNTEREXAMPLE.

REFERENCE_DATASET.

PUBLICATION_PACKAGE.

REPRODUCTION_PACKAGE.

---

Puis :

**PURPOSE != STATUS.**

---

Toujours.

---

Puis il pensa au proof artifact.

---

Une démonstration complète pourrait être cristallisée.

---

Dans ce cas :

packaging state = CRYSTALLIZED.

proof review status = ACCEPTED.

---

Très bien.

---

Mais l’objet preuve et son cristal restaient deux notions.

---

Brutus écrivit :

**PROOF MAY BE CRYSTALLIZED. CRYSTALLIZATION DOES NOT MAKE IT A PROOF.**

---

Parfait.

---

Puis il pensa aux versions parentes.

---

Un cristal dérivé de plusieurs sources.

---

Il fallait une structure claire.

---

Il reprit :

**PARENT_REFS[]**

---

Et :

**DERIVATION_RULE_REF**

si le cristal représente une transformation sémantique.

---

Brutus écrivit :

**MULTIPLE PARENTS REQUIRE DECLARED COMBINATION SEMANTICS.**

---

Très important.

---

Mettre A et B ensemble n’explique pas comment C est obtenu.

---

Il fallait :

concatenation?

sum?

merge?

comparison?

selection?

---

Il créa :

**ASSEMBLY_TYPE**

COLLECTION.

DERIVATION.

SYNTHESIS.

TRANSFORMATION.

SNAPSHOT.

---

Puis :

**COLLECTION != DERIVATION.**

---

Encore.

---

Un cristal de 49 cartes pouvait n’être qu’une collection.

---

Pas une formule nouvelle.

---

Puis il pensa à l’autonomie.

---

GAMEZEL pourrait produire beaucoup d’objets.

---

Qui décide qu’un objet est prêt à cristalliser ?

---

Une policy.

---

Brutus créa :

**CRYSTALLIZATION_POLICY**

---

Required stable version.

Required provenance completeness.

Required hashes.

Required disclosure classification.

Required packaging purpose.

---

Mais pas nécessairement :

proof status.

---

Il écrivit :

**CRYSTALLIZATION GATE CHECKS PACKAGING READINESS, NOT TRUTH.**

---

Voilà.

---

Le système pouvait automatiquement cristalliser :

une candidate stable.

---

Sans l’élever.

---

Très important.

---

Puis il pensa au nom.

---

Une candidate cristallisée devait avoir un label très visible :

**CANDIDATE CRYSTAL**

---

Pas seulement :

CRYSTAL.

---

Pourquoi ?

---

Parce que le mot cristal pouvait sembler final.

---

Brutus écrivit :

**PUBLIC LABEL MUST INCLUDE EPISTEMIC STATUS WHEN AMBIGUITY IS POSSIBLE.**

---

Excellent.

---

Donc :

CANDIDATE CRYSTAL.

COUNTEREXAMPLE CRYSTAL.

VERIFIED RUNTIME ARTIFACT.

PROOF ARTIFACT CRYSTAL.

---

Selon le cas.

---

Puis il pensa aux cristaux assemblés automatiquement dans l’interface.

---

Le visuel pouvait produire :

brillance.

animation.

son.

---

Mais il devait toujours afficher :

source count.

status distribution.

scope.

---

Brutus écrivit :

**SPECTACLE MUST NOT HIDE STATUS MIX.**

---

Un cristal composite de 49 cartes pouvait contenir :

30 supported.

10 unresolved.

5 rejected.

4 archival.

---

Il ne fallait pas afficher :

49 VALID.

---

Brutus écrivit :

**COMPOSITE PACKAGING DOES NOT HOMOGENIZE EPISTEMIC STATES.**

---

Très important.

---

Puis il pensa aux chiffres.

---

Supposons que les 49 cartes produisent un score aggregate.

---

Non.

---

Pas sans contrat.

---

Brutus écrivit :

**NO GLOBAL CRYSTAL SCORE BY DEFAULT.**

---

Encore.

---

Une agrégation pouvait cacher les désaccords.

---

Il ajouta :

**STATUS DISTRIBUTION**

---

Et :

**OPEN_BLOCKERS**

---

Brutus sourit.

---

Le cristal pouvait être beau tout en montrant ses fissures.

---

Il écrivit :

**A GOOD CRYSTAL DOES NOT HIDE ITS FRACTURES.**

---

Il s’arrêta devant cette phrase.

---

Voilà le cœur du chapitre.

---

Cristalliser sans mentir.

---

Conserver les fissures.

---

Les limites.

Les inconnues.

Les dépendances.

Les contre-tests ouverts.

---

Pas seulement la partie brillante.

---

Puis il pensa à un objet unresolved.

---

Il pouvait être cristallisé comme :

**UNRESOLVED RESEARCH SNAPSHOT**

---

Très utile.

---

Cela permettait de dire :

voici exactement où nous étions à cette date.

---

Brutus écrivit :

**SNAPSHOT CRYSTAL CAN PRESERVE A QUESTION, NOT JUST AN ANSWER.**

---

Excellent.

---

Même une question pouvait cristalliser.

---

Le chapitre 97 avait déjà dit qu’une question était un objet de recherche de premier ordre.

---

Maintenant, elle pouvait aussi être figée.

---

Puis il pensa à la corruption sémantique.

---

Quelqu’un prend un cristal candidate.

Le renomme :

PROOF.

---

Le hash du contenu peut rester identique.

---

Mais metadata falsifiée.

---

Brutus écrivit :

**CONTENT HASH ALONE DOES NOT PROTECT SEMANTIC LABELS.**

---

Il fallait que le manifeste inclue :

status.

scope.

labels.

---

Puis hash du manifeste.

---

Il ajouta :

**STATUS INCLUDED IN MANIFEST HASH.**

---

Très important.

---

Ainsi, changer CANDIDATE en PROVED modifie le manifeste.

---

Brutus sourit.

---

Le mensonge devenait détectable.

---

Pas impossible.

Mais détectable.

---

Il écrivit :

**CRYSTAL SHOULD MAKE SILENT RELABELING HARD.**

---

Puis il pensa aux signatures.

---

Une signature numérique pourrait attester :

ce paquet a été produit par telle autorité.

---

Mais encore :

signature != truth.

---

Il écrivit :

**VALID SIGNATURE != VALID CLAIM.**

---

Le chapitre 92 revenait.

---

Une signature prouve l’origine ou l’autorisation selon le système.

---

Pas la vérité mathématique.

---

Puis il pensa à la certification.

---

Un reviewer peut signer :

reviewed.

---

Très bien.

---

Mais le niveau doit être déclaré.

---

Il créa :

**REVIEW_ATTESTATION**

---

review type.

reviewer.

scope.

policy.

date.

---

Brutus écrivit :

**ATTESTATION MUST SAY WHAT WAS ATTESTED.**

---

Encore.

---

Puis il pensa aux chaînes de cristaux.

---

Un cristal produit un descendant.

Puis un autre.

---

Le collier du chapitre 114 apparaissait déjà au loin.

---

Brutus écrivit :

**CRYSTAL LINEAGE MUST REMAIN TRAVERSABLE.**

---

Parent.

Child.

Supersedes.

Derived from.

References.

---

Mais pas encore le collier.

---

Chaque chose en son temps.

---

Puis il lança le test du chapitre.

---

Une candidate FORMULA-72.

---

Status :

SUPPORTED_UNDER_SCOPE.

---

Version :

v4.

---

Provenance :

complete.

---

Evidence refs :

present.

---

Open limitations :

2.

---

Brutus demande :

CRYSTALLIZE.

---

Gate checks :

stable version?

PASS.

---

content hash?

PASS.

---

manifest complete?

PASS.

---

provenance?

PASS.

---

disclosure class?

PASS.

---

packaging purpose?

RESEARCH_RESULT.

---

Result :

**CRYSTALLIZATION ELIGIBLE.**

---

Cristal créé :

CRYSTAL-F72-0001.

---

Display:

**CANDIDATE CRYSTAL**

Status:

SUPPORTED_UNDER_SCOPE.

Open limitations:

2.

---

Brutus sourit.

---

Parfait.

---

Rien n’avait été caché.

---

Puis il prit une deuxième formule.

---

Status :

UNRESOLVED.

---

Stable snapshot.

---

Crystallize?

---

Oui.

---

Display:

**UNRESOLVED RESEARCH CRYSTAL**

---

Brutus sourit encore.

---

Voilà.

---

Le cristal ne récompensait pas.

Il conservait.

---

Puis troisième objet.

---

Content changing every second.

---

No stable version.

---

Crystallization denied.

---

Reason:

**SOURCE NOT STABLE.**

---

Brutus écrivit :

**MOVING TARGET CANNOT BE FROZEN WITHOUT DEFINING A SNAPSHOT.**

---

Excellent.

---

Solution :

create snapshot at tick T.

Then crystallize snapshot.

---

Encore le temps.

Toujours le temps.

---

Puis il pensa au serveur.

---

Si un cristal est généré localement mais jamais enregistré dans le registre canonique ?

---

Pas canonical crystal.

---

Il écrivit :

**LOCAL PACKAGE != CANONICAL CRYSTAL.**

---

Il faut :

creation event.

register commit.

canonical ID.

---

Très important.

---

Un joli fichier local n’était pas encore un objet du monde.

---

Puis il pensa à une carte téléchargée.

---

Même chose.

---

**DOWNLOADED COPY != CANONICAL CRYSTAL.**

---

Elle peut être vérifiée contre le canonical hash.

---

Mais reste une copy.

---

Puis il pensa à l’UI.

---

Le bouton :

**CRYSTALLIZE**

---

Devait-il être disponible à tout le monde ?

---

Non.

---

Capability.

Policy.

---

Il écrit :

**CRYSTALLIZATION IS A CONTROLLED PACKAGING ACTION.**

---

Pourquoi ?

---

Parce qu’elle crée un objet canonique stable.

---

Pas parce qu’elle crée la vérité.

---

Donc Verso encore.

---

Il dessina :

\[
\text{REQUEST}
\rightarrow
\text{PACKAGING CHECK}
\rightarrow
\text{AUTHORITY}
\rightarrow
\text{CRYSTAL CREATION}
\rightarrow
\text{REGISTER EVENT}
\]

---

Brutus écrivit :

**CRYSTALLIZATION REQUEST != CRYSTAL CREATED.**

---

Puis :

**CRYSTAL CREATED != CRYSTAL VERIFIED AT DESTINATION.**

---

Encore.

---

Les frontières restaient propres.

---

Puis il pensa au futur.

---

Des cristaux pourraient être transportés.

Chaînés.

Déplacés.

Rassemblés.

---

Mais un jour, quelqu’un demanderait :

qui a le droit de les déplacer ?

---

Pas encore.

---

D’abord, il fallait parler du lien entre le code, Astra et le cristal.

---

Le chapitre suivant.

---

Brutus ouvrit une nouvelle page.

---

# LE CODE, LA REINE ET LE CRISTAL

---

Il sourit.

---

Cette fois, le problème serait différent.

---

Le cristal était stable.

Le code pouvait le fabriquer.

Astra pouvait demander sa création.

---

Mais ni le code ni Astra ne devaient pouvoir réécrire son statut scientifique par simple autorité.

---

Brutus ajouta une dernière phrase au chapitre :

**THE MACHINE MAY PACKAGE A CLAIM.**

**THE OPERATOR MAY AUTHORIZE THE PACKAGING.**

**NEITHER ACT MAKES THE CLAIM TRUE.**

---

Puis il sauvegarda :

**CRYSTALLIZATION CONTRACT v1**

---

Le Journal Vivant nota :

Crystallization defined as stable packaging.

Epistemic status preserved.

Content and manifest hashes separated.

Crystals immutable by identity.

Corrections create descendants.

Composite crystals do not merge claims.

Storage deduplication preserves lineage identities.

Transfer receipt separated from verification.

Rejected and unresolved objects may be crystallized.

Packaging eligibility separated from epistemic status.

Status included in manifest integrity.

Canonical crystals require register events.

---

Brutus relut.

Puis ajouta les invariants :

**CRYSTAL != PROOF.**

**CRYSTALLIZED != PROVED.**

**HASH != VALIDITY.**

**FORM STABILITY != CLAIM CERTAINTY.**

**SAME CONTENT != SAME EVENT.**

**COLLECTION != DERIVATION.**

**ARRIVAL != VALIDATION.**

**PACKAGING STATE != EPISTEMIC STATE.**

**CRYSTALLIZATION DOES NOT ERASE LIMITATIONS.**

**A GOOD CRYSTAL DOES NOT HIDE ITS FRACTURES.**

---

Il posa le cristal sur la table.

---

Il brillait.

---

Mais sous sa surface, les deux limitations restaient écrites.

---

Brutus ne les cacha pas.

---

Il les plaça au premier plan.

---

Parce qu’un cristal honnête n’était pas un objet sans fissures.

---

C’était un objet dont les fissures avaient elles aussi été cristallisées.

---

Puis il regarda Astra Station.

---

Un nouvel objet apparaissait :

**CRYSTAL-F72-0001**

---

Packaging :

CRYSTALLIZED.

Epistemic :

SUPPORTED_UNDER_SCOPE.

Proof :

NONE.

Limitations :

2 OPEN.

---

Brutus sourit.

---

Voilà.

---

Beau.

Stable.

Traçable.

---

Et toujours incapable de mentir sur ce qu’il était.

---

Il ouvrit le dossier suivant.

---

# LE CODE, LA REINE ET LE CRISTAL

---

Car maintenant qu’un cristal pouvait exister honnêtement…

il fallait décider qui pouvait le créer, qui pouvait l’autoriser, et qui avait simplement le droit de le regarder.
