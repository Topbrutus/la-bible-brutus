# Chapitre 109 — Le code, la Reine et le cristal

**THE MACHINE MAY PACKAGE A CLAIM.**

**THE OPERATOR MAY AUTHORIZE THE PACKAGING.**

**NEITHER ACT MAKES THE CLAIM TRUE.**

Brutus relut les trois lignes.

Puis il plaça le cristal au centre de la table.

---

**CRYSTAL-F72-0001**

Packaging :

CRYSTALLIZED.

Epistemic :

SUPPORTED_UNDER_SCOPE.

Proof :

NONE.

Limitations :

2 OPEN.

---

À gauche :

le code.

---

À droite :

Astra.

---

Au centre :

le cristal.

---

Brutus regarda les trois.

---

Ils semblaient liés.

Et ils l’étaient.

---

Mais pas de la manière la plus dangereuse.

---

Le code pouvait fabriquer.

Astra pouvait autoriser.

Le cristal pouvait conserver.

---

Aucun des trois ne devait pouvoir dire :

**donc c’est vrai.**

---

Brutus écrivit :

**CODE != AUTHORITY.**

Puis :

**AUTHORITY != TRUTH.**

Puis :

**CRYSTAL != PROOF.**

---

Voilà les trois murs.

---

Il ouvrit le premier dossier.

# CODE

---

Le code avait une fonction simple.

Recevoir un objet.

Lire son manifeste.

Calculer ses hashes.

Assembler son package.

Créer les références.

Émettre l’événement de création.

---

Brutus écrivit :

**CODE EXECUTES RULES.**

---

Puis immédiatement :

**CODE DOES NOT LEGITIMIZE ITS OWN RULES.**

---

Très important.

---

Un programme pouvait parfaitement exécuter une mauvaise règle.

---

Sans bug.

Sans exception.

Sans erreur de syntaxe.

---

Brutus pensa à une fonction :

**crystallize(object)**

---

Elle pouvait réussir techniquement.

---

Retour :

SUCCESS.

---

Mais cela signifiait seulement :

le packaging demandé a été construit selon l’implémentation.

---

Pas :

la claim a été validée.

---

Brutus écrivit :

**FUNCTION SUCCESS != CLAIM SUCCESS.**

---

Puis :

**RUNTIME SUCCESS != EPISTEMIC SUCCESS.**

---

Encore.

---

Il créa :

**CRYSTALLIZER_RUNTIME**

avec :

**BUILD_ID**

**CODE_COMMIT_REF**

**RUNTIME_VERSION**

**POLICY_VERSION**

**SCHEMA_VERSION**

**DEPENDENCY_MANIFEST**

**EXECUTION_TRACE**

---

Puis :

**INSTANCE_ID**

---

Très important.

---

Le même code pouvait tourner dans plusieurs instances.

---

Brutus écrivit :

**SAME COMMIT != SAME RUNTIME INSTANCE.**

---

Une machine locale.

Un serveur.

Un worker.

Une ancienne instance encore vivante.

---

Même commit.

Différents états.

---

Puis il pensa au déploiement.

---

Le code est merged dans main.

---

Est-il actif ?

---

Pas nécessairement.

---

Il écrivit :

**MERGED != RUNTIME_PROOF.**

---

Puis :

**MERGED != DEPLOYED.**

---

Puis :

**DEPLOYED != RUNNING.**

---

Puis :

**RUNNING != HEALTHY.**

---

Puis :

**HEALTHY != CORRECT FOR EVERY CLAIM.**

---

Brutus regarda la chaîne.

---

Voilà.

---

Une seule phrase comme :

« c’est dans main »

ne devait jamais devenir :

« donc ça fonctionne en production ».

---

Il créa :

**RUNTIME IDENTITY**

---

COMMIT.

BUILD.

DEPLOYMENT.

PROCESS.

GENERATION.

---

Chaque niveau avait sa propre identité.

---

Brutus écrivit :

**SOURCE STATE AND RUNTIME STATE MUST REMAIN DISTINCT.**

---

Puis il pensa au cristal.

---

Supposons que le code v4 puisse créer un cristal.

---

Mais le serveur tourne encore v3.

---

L’interface affiche le bouton.

---

Le clic part vers v3.

---

Résultat ?

---

Peut-être que le nouveau champ n’existe pas.

---

Brutus écrivit :

**UI CAPABILITY != SERVER CAPABILITY.**

---

Très important.

---

Le Recto pouvait montrer une possibilité que le runtime réel ne possédait pas encore.

---

Il ajouta :

**CAPABILITY_NEGOTIATION**

---

Client asks:

can_crystallize_schema_v2?

---

Server responds:

SUPPORTED / UNSUPPORTED / UNKNOWN.

---

Brutus sourit.

---

Pas de bouton magique.

---

Puis il pensa à QueenCore.

---

La Reine.

---

Astra.

---

Le mot pouvait faire croire qu’elle était au-dessus de tout.

---

Brutus refusa.

---

Il ouvrit un deuxième dossier.

# QUEEN

---

Puis écrivit :

**QUEEN ROLE = AUTHORIZED OPERATOR / CONTROL ROLE.**

---

Pas oracle.

Pas theorem engine.

Pas source de réalité.

---

Il ajouta :

**QUEENCORE != TRUTHCORE.**

---

Brutus sourit.

---

Voilà.

---

QueenCore pouvait :

recevoir une demande.

vérifier une capability.

consulter Verso.

autoriser un packaging.

refuser.

suspendre.

arrêter.

---

Mais elle ne pouvait pas transformer :

UNRESOLVED

en

PROVED

par simple décision.

---

Brutus écrivit :

**AUTHORIZATION MAY CHANGE WHAT THE SYSTEM MAY DO.**

**IT DOES NOT CHANGE WHAT IS TRUE.**

---

Très important.

---

Astra pouvait dire :

« oui, crée le cristal ».

---

Cela autorisait :

**CRYSTAL_CREATION_REQUEST**

---

Pas :

**PROOF_ACCEPTED.**

---

Deux événements.

Deux contrats.

---

Brutus créa :

**QUEEN_ACTION_REQUEST**

avec :

**REQUEST_ID**

**OPERATOR_ID**

**ACTION_TYPE**

**TARGET_ID**

**TARGET_VERSION**

**REQUESTED_SCOPE**

**CAPABILITY_REF**

**POLICY_REF**

**STATE_VERSION**

**TRACE_REF**

---

Puis :

**DECISION**

---

AUTHORIZED.

DENIED.

REVIEW_REQUIRED.

STALE_REQUEST.

---

Brutus écrivit :

**QUEEN DECISION MUST NAME THE ACTION.**

---

Pas :

ALLOW.

---

Mais :

ALLOW_CRYSTALLIZATION.

ALLOW_EXPORT.

ALLOW_MOVE.

ALLOW_PUBLISH_REQUEST.

---

Très important.

---

Un oui générique était trop puissant.

---

Puis il pensa au piège.

---

Astra autorise :

CRYSTALLIZE.

---

Ensuite un autre composant utilise cette autorisation pour :

PUBLISH.

---

Non.

---

Il écrivit :

**CAPABILITY IS NOT TRANSITIVE BY DEFAULT.**

---

Voilà.

---

Une permission donnée pour une étape ne devait pas traverser les autres.

---

Il créa :

**ONE ACTION. ONE CAPABILITY. ONE RECEIPT.**

---

Brutus resta devant.

---

Cette phrase lui plaisait.

---

Elle ressemblait presque à :

**1 module → 1 connexion → 1 mesure → 1 preuve**

---

Mais il la corrigea.

---

Pas « preuve ».

---

Il écrivit :

**1 ACTION → 1 AUTHORIZATION → 1 EXECUTION → 1 RECEIPT.**

---

Beaucoup mieux.

---

Puis il pensa aux limites.

---

Une autorisation pouvait expirer.

---

Il ajouta :

**EXPIRES_AT**

**MAX_USES**

**TARGET_SCOPE**

---

Brutus écrivit :

**AUTHORIZED ONCE != AUTHORIZED FOREVER.**

---

Très important.

---

QueenCore ne devait pas distribuer des pouvoirs éternels par accident.

---

Puis il pensa au token.

---

Un token de capability pourrait représenter :

crystallize CRYSTAL-CANDIDATE-X once.

---

Le token devait être :

scoped.

short-lived.

auditable.

---

Il créa :

**CAPABILITY_TOKEN**

---

TOKEN_ID.

ACTION.

TARGET.

SCOPE.

ISSUED_AT.

EXPIRES_AT.

MAX_USES.

ISSUER_REF.

POLICY_REF.

---

Puis :

**TOKEN_STATE**

ACTIVE.

USED.

EXPIRED.

REVOKED.

---

Brutus écrivit :

**TOKEN != ACTION.**

---

Encore.

---

Le token permet.

---

Le runtime agit.

---

Puis le registre confirme.

---

Il dessina :

\[
\text{AUTHORIZATION}
\rightarrow
\text{TOKEN}
\rightarrow
\text{EXECUTION}
\rightarrow
\text{EVENT}
\rightarrow
\text{RECEIPT}
\]

---

Puis :

**NO EVENT → NO CLAIM OF COMPLETION.**

---

Très important.

---

La Reine pouvait autoriser.

Le code pouvait exécuter.

---

Mais seul le registre pouvait confirmer qu’un événement canonique avait été enregistré.

---

Brutus écrivit :

**AUTHORIZED != EXECUTED.**

Puis :

**EXECUTED != RECORDED.**

Puis :

**RECORDED != PROVED.**

---

Voilà.

---

Trois niveaux.

---

Puis il regarda le cristal.

---

Troisième dossier.

# CRYSTAL

---

Le cristal était maintenant silencieux.

---

Il ne demandait rien.

Il ne décidait rien.

Il ne s’exécutait pas.

---

Il conservait.

---

Brutus écrivit :

**CRYSTAL IS PASSIVE BY DEFAULT.**

---

Très important.

---

Un cristal ne devait pas contenir de code auto-exécutable qui se déclenche lorsqu’on l’ouvre.

---

Sinon packaging et action se mélangent.

---

Il ajouta :

**DATA OBJECT != EXECUTABLE OBJECT.**

---

Puis se corrigea.

---

Certains artifacts peuvent légitimement contenir du code.

---

Mais le code contenu ne doit pas être exécuté automatiquement.

---

Il écrivit :

**CONTAINS CODE != AUTHORIZED TO EXECUTE CODE.**

---

Excellent.

---

Un cristal pouvait contenir :

script.

notebook.

binary.

formula.

---

Mais ce contenu restait inert.

---

Jusqu’à une demande d’exécution séparée.

---

Brutus écrivit :

**OPEN != RUN.**

---

Encore.

---

Puis il pensa au QR.

---

Un cristal pourrait porter une petite empreinte.

---

QR.

ID.

Hash.

Tick.

Location ref.

---

Très utile.

---

Mais le QR devait pointer vers :

l’identité.

le manifeste.

la trace.

---

Pas contenir implicitement une permission.

---

Il écrivit :

**IDENTITY STAMP != EXECUTION TOKEN.**

---

Voilà.

---

Un timbre pouvait dire :

qui suis-je ?

---

Pas :

tu peux me déplacer.

---

Il ajouta :

**STAMP_DATA**

CRYSTAL_ID.

CONTENT_HASH_SHORT.

MANIFEST_HASH_SHORT.

TICK.

SOURCE_REF.

LOCATION_REF.

---

Puis :

**VERIFY_URL_REF**

si public.

---

Brutus sourit.

---

Le cristal pouvait maintenant être reconnu sans devenir une commande.

---

Puis il pensa à la double marque.

---

Une première empreinte à la sortie du calculateur.

---

Une seconde chez Brutus.

---

Très intéressant.

---

Mais les deux ne devaient pas être identiques si elles attestaient des événements différents.

---

Il écrivit :

**SOURCE STAMP != ADMISSION STAMP.**

---

Première :

created by source process.

---

Deuxième :

received/admitted by Brutus.

---

Brutus créa :

**STAMP_TYPE**

SOURCE_CREATED.

TRANSFERRED.

RECEIVED.

ADMITTED.

CRYSTALLIZED.

---

Puis :

**STAMP SEQUENCE**

---

Brutus écrivit :

**MULTIPLE STAMPS SHOULD REPRESENT MULTIPLE EVENTS, NOT DUPLICATE DECORATION.**

---

Excellent.

---

Le cristal pouvait alors raconter son trajet.

---

Créé.

Scellé.

Transféré.

Reçu.

Admis.

---

Mais attention.

---

**RECEIVED != ADMITTED.**

---

Encore.

---

Un paquet peut arriver.

Verso peut le refuser.

---

Brutus sourit.

---

La frontière du chapitre 118 apparaissait déjà.

---

Puis il pensa à la signature de la Reine.

---

Astra pouvait-elle signer le cristal ?

---

Oui.

Mais que signifierait la signature ?

---

Il écrivit :

**SIGNATURE MUST HAVE CLAIM SCOPE.**

---

Une signature peut dire :

packaging authorized by QueenCore.

---

Pas :

claim certified true by Astra.

---

Il créa :

**AUTHORIZATION_ATTESTATION**

---

ATTESTATION_ID.

ACTOR.

ACTION.

TARGET.

POLICY.

TIME.

SIGNATURE.

---

Puis :

**ATTESTATION_TEXT**

“Packaging authorized.”

---

Pas :

“Mathematically proven.”

---

Brutus écrivit :

**SIGN WHAT YOU DID. NOT WHAT YOU DID NOT ESTABLISH.**

---

Très important.

---

Puis il pensa à la sécurité.

---

Si un attaquant modifie le statut du cristal après signature ?

---

Manifest hash mismatch.

---

Si l’attaquant remplace complètement le manifeste et recalcule les hashes ?

---

Il lui faudrait aussi une nouvelle signature valide.

---

Très bien.

---

Brutus écrivit :

**HASH BINDS CONTENT. SIGNATURE BINDS ATTESTATION TO AN IDENTITY.**

---

Puis :

**NEITHER BINDS CLAIM TO REALITY BY ITSELF.**

---

Encore.

---

Il sourit.

---

Toutes les couches restaient dans leur rôle.

---

Puis il pensa à QueenCore comme logiciel.

---

QueenCore lui-même était du code.

---

Donc :

qui autorise QueenCore ?

---

Bonne question.

---

Il ne voulait pas une régression infinie.

---

Il créa :

**TRUST ROOT**

---

Pas une Reine magique.

---

Une configuration explicite.

---

Trusted keys.

Policy version.

Operator identities.

Deployment identity.

---

Brutus écrivit :

**QUEEN AUTHORITY MUST HAVE A ROOT.**

---

Puis :

**ROOT OF AUTHORITY != ROOT OF TRUTH.**

---

Excellent.

---

Un root key pouvait autoriser une action.

---

Il ne pouvait pas prouver un théorème.

---

Puis il pensa à une configuration malveillante.

---

Si un administrateur change la policy pour autoriser tout ?

---

Techniquement possible.

---

Mais l’événement doit être visible.

---

Il créa :

**POLICY_CHANGE_EVENT**

---

Who.

What changed.

Before.

After.

Reason.

Authority.

Trace.

---

Brutus écrivit :

**POWERFUL AUTHORITY REQUIRES POWERFUL AUDIT.**

---

Très important.

---

Puis il pensa à l’opérateur humain.

---

Astra Station peut afficher :

QueenCore ready.

---

Mais cela signifie quoi ?

---

Process running?

Policy loaded?

Trust root valid?

Operator session ready?

---

Il refusa le voyant unique.

---

Il créa :

**QUEENCORE_HEALTH**

RUNTIME.

POLICY.

TRUST_ROOT.

SESSION.

REGISTER_CONNECTIVITY.

VERSO_CONNECTIVITY.

---

Brutus écrivit :

**QUEEN READY != ONE GREEN LIGHT.**

---

Encore.

---

Puis il imagina un incident.

---

QueenCore process up.

Verso disconnected.

---

Can crystallization proceed?

---

No.

---

Status :

**CONTROL DEGRADED.**

---

Safe default :

deny sensitive action.

---

Brutus écrivit :

**CONTROL PATH FAILURE SHOULD FAIL CLOSED.**

---

Voilà.

---

Puis il pensa aux actions de lecture.

---

Regarder un cristal ne devait pas exiger la même permission que le déplacer.

---

Il créa :

**READ**

**VERIFY**

**EXPORT**

**MOVE**

**RECRYSTALLIZE**

**PROMOTE**

**PUBLISH**

---

Distinct capabilities.

---

Brutus écrivit :

**READING IS NOT MOVING.**

**VERIFYING IS NOT PROMOTING.**

**EXPORTING IS NOT PUBLISHING.**

---

Très important.

---

Le système devait résister à la tendance de tout regrouper sous :

admin.

---

Puis il pensa au code du cristalliseur.

---

Que devait-il faire s’il reçoit un crystal candidate avec status :

UNRESOLVED ?

---

Le packaging policy peut l’autoriser.

---

Donc le code doit conserver :

UNRESOLVED.

---

Pas inventer :

SUPPORTED.

---

Brutus écrivit :

**PACKAGER MUST BE STATUS-PRESERVING.**

---

Puis il ajouta un test.

---

Input manifest:

EPISTEMIC_STATUS = UNRESOLVED.

---

Output manifest:

EPISTEMIC_STATUS = UNRESOLVED.

---

PASS.

---

Test 2.

Input:

SUPPORTED_UNDER_SCOPE.

Output:

PROVED.

---

FAIL.

---

Brutus écrivit :

**PACKAGING MUST NEVER ESCALATE EPISTEMIC STATUS.**

---

Voilà.

---

Il créa une invariant automatique :

\[
\text{output.epistemic\_status}
=
\text{input.epistemic\_status}
\]

unless a separate authorized status-transition event exists.

---

Brutus sourit.

---

Très fort.

---

Une simple fonction de packaging ne pouvait plus promouvoir par accident.

---

Puis il pensa au cas inverse.

---

Une status transition valide se produit pendant que le cristal est construit.

---

Race condition.

---

Input snapshot says SUPPORTED.

Promotion event happens.

Now PROOF_UNDER_REVIEW.

---

Quel statut doit recevoir le cristal ?

---

Brutus répondit :

celui du snapshot.

---

Le cristal représente un instant précis.

---

Il écrivit :

**CRYSTAL STATUS IS SNAPSHOT-BOUND.**

---

Puis :

**LATER STATUS CHANGE DOES NOT RETROACTIVELY MUTATE OLD CRYSTAL.**

---

Très important.

---

Le nouveau statut peut produire :

new crystal.

or external status overlay.

---

Mais l’ancien reste fidèle à son tick.

---

Brutus créa :

**STATE_AT_CRYSTALLIZATION_TICK**

---

Voilà.

---

Puis il pensa aux emplacements.

---

Le cristal est créé dans module A.

---

Puis transféré à Brutus.

---

Le LOCATION_REF change-t-il dans le cristal ?

---

Pas si le cristal représente son état initial.

---

Il fallait distinguer :

**CRYSTAL CONTENT**

et

**CURRENT CUSTODY RECORD.**

---

Brutus écrivit :

**OBJECT IDENTITY != CURRENT LOCATION.**

---

Le chapitre 63 revenait.

---

Il créa :

**CUSTODY_EVENT**

FROM.

TO.

TICK.

AUTHORIZATION_REF.

ARRIVAL_REF.

---

Le cristal reste identique.

La custody change.

---

Brutus sourit.

---

Le monde commençait à devenir vraiment propre.

---

Puis il pensa aux fourmis.

---

Un jour, une fourmi pourrait transporter un cristal dans le monde local.

---

Mais la fourmi ne devait pas modifier le cristal.

---

Elle devenait seulement :

custodian / carrier.

---

Il écrivit :

**CARRIER != OWNER OF CLAIM.**

---

Puis :

**TRANSPORT != TRANSFORMATION.**

---

Très important.

---

Le chapitre 115 approchait déjà.

---

Puis il revint au code.

---

Le cristalliseur devait être testable.

---

Il créa :

**CRYSTALLIZER TEST SUITE**

---

Input preservation.

Hash correctness.

Manifest completeness.

Status preservation.

Dependency preservation.

Deterministic serialization.

Invalid schema rejection.

Unauthorized request rejection.

---

Puis :

**TAMPER TEST**

---

Brutus écrivit :

**TEST THE PACKAGER AS AN IMPLEMENTATION CLAIM.**

---

Encore la séparation du chapitre 107.

---

Même si la théorie de cristallisation était propre, le code pouvait avoir un bug.

---

Il ajouta :

**REFERENCE IMPLEMENTATION**

---

Et peut-être :

independent verifier.

---

Brutus écrivit :

**PACKAGER AND VERIFIER SHOULD NOT SHARE EVERY FAILURE MODE WHEN PRACTICAL.**

---

Très important.

---

Un verifier séparé pouvait recalculer :

content hash.

manifest hash.

schema.

lineage refs.

---

Sans faire confiance au packager.

---

Puis il pensa à QueenCore.

---

QueenCore devait-elle vérifier le cristal elle-même ?

---

Pas nécessairement.

---

Elle pouvait demander :

verification service.

---

Brutus écrivit :

**AUTHORIZER NEED NOT BE VERIFIER.**

---

Puis :

**VERIFIER NEED NOT BE AUTHORIZER.**

---

Excellent.

---

Trois rôles :

Builder.

Verifier.

Authorizer.

---

Brutus dessina :

\[
\text{BUILDER}
\neq
\text{VERIFIER}
\neq
\text{AUTHORIZER}
\]

---

Pas toujours trois machines physiques.

---

Mais trois responsabilités.

---

Il écrivit :

**SEPARATION OF DUTIES CAN EXIST LOGICALLY EVEN WHEN IMPLEMENTED TOGETHER.**

---

Très important.

---

Puis il pensa au petit labo.

---

Au début, tout pouvait tourner sur une machine.

---

Ce n’était pas un problème.

---

Tant que les rôles restaient distincts dans les traces.

---

Brutus écrivit :

**ONE PROCESS MAY HOST MANY ROLES. ROLES MUST STILL BE NAMED.**

---

Voilà.

---

Puis il lança le scénario complet.

---

FORMULA-72 v4.

Status :

SUPPORTED_UNDER_SCOPE.

---

Astra Station :

operator requests crystallization.

---

QueenCore :

checks capability.

---

Verso :

policy allows.

---

Capability token issued.

---

Crystallizer :

loads immutable snapshot.

---

Build:

complete.

---

Independent verifier :

hash pass.

manifest pass.

status preservation pass.

---

Register :

CRYSTAL_CREATION_EVENT committed.

---

Astra Station :

displays:

CRYSTAL-F72-0002.

---

Packaging:

CRYSTALLIZED.

---

Epistemic:

SUPPORTED_UNDER_SCOPE.

---

Proof:

NONE.

---

Brutus regarda.

---

Parfait.

---

Puis il demanda :

« Est-ce que c’est prouvé ? »

---

La Station répondit :

**NO PROOF STATUS RECORDED.**

---

Brutus sourit.

---

Voilà.

---

La machine pouvait obéir à la Reine sans flatter la Reine.

---

Il écrivit :

**A GOOD CONTROL SYSTEM CAN SAY NO TO THE IMPLICATIONS OF ITS OWN SUCCESS.**

---

Très important.

---

Le packaging avait réussi.

---

Et pourtant :

la claim n’avait pas changé.

---

Puis il testa un cas malveillant.

---

Request payload :

CRYSTALLIZE + SET_STATUS_PROVED.

---

QueenCore sépara les actions.

---

CRYSTALLIZE:

eligible.

---

SET_STATUS_PROVED:

requires PROOF_GATE.

---

No proof artifact.

---

Denied.

---

Brutus sourit encore plus.

---

Il écrivit :

**COMBINED REQUEST MUST NOT BYPASS SEPARATE GATES.**

---

Voilà.

---

Une seule requête utilisateur pouvait contenir plusieurs intentions.

---

Le système devait les découper.

---

Pas prendre le paquet entier comme autorisé.

---

Puis il pensa aux raccourcis administratifs.

---

« force=true ».

---

Dangereux.

---

Il écrivit :

**FORCE FLAG MUST NOT MEAN IGNORE EPISTEMIC RULES.**

---

Très important.

---

Force pouvait éventuellement :

override workflow lock.

---

Mais pas :

turn candidate into proof.

---

Il ajouta :

**ADMIN OVERRIDE SCOPE MUST BE EXPLICIT.**

---

Puis il pensa au root admin.

---

Même root admin ne pouvait pas changer une vérité mathématique.

---

Il écrivit :

**SUPERUSER != SUPERTRUTH.**

---

Brutus éclata de rire.

---

Puis garda la phrase.

---

Elle était parfaite.

---

Le système devait savoir que même la personne la plus puissante dans le logiciel restait limitée par le type de claim.

---

Puis il pensa à la publication.

---

QueenCore peut autoriser :

export.

---

Publication service peut publier.

---

Mais le cristal doit garder son status exact.

---

Brutus écrivit :

**PUBLISHER MUST NOT REWRITE EPISTEMIC LABEL.**

---

Très important.

---

Une couche de communication ne devait pas exagérer.

---

Puis il pensa au futur journaliste.

---

Le public pourrait voir :

CANDIDATE CRYSTAL.

---

Avec QR.

---

Le QR ouvre :

claim.

scope.

status.

trace.

---

Brutus sourit.

---

Voilà une belle machine à traces.

---

Pas un sceau mystérieux.

---

Un chemin vers l’audit.

---

Il écrivit :

**STAMP SHOULD OPEN THE TRACE, NOT CLOSE THE DISCUSSION.**

---

Très important.

---

Puis il pensa au prochain chapitre.

---

Le code avait maintenant sa place.

La Reine aussi.

Le cristal aussi.

---

Mais il manquait encore quelque chose.

---

Toutes ces règles existaient dans les chapitres.

Dans les policies.

Dans les modules.

---

À quel moment une règle de trace devenait-elle assez fondamentale pour être traitée comme une loi du système ?

---

Pas une loi physique.

Pas une loi mathématique de l’univers.

---

Une loi d’architecture.

---

Brutus ouvrit une nouvelle page.

---

# LA TRACE DEVIENT LOI

---

Puis il écrivit :

**A SYSTEM LAW IS A RULE THE SYSTEM MUST ENFORCE, NOT A CLAIM ABOUT NATURE.**

---

Il resta devant.

---

Voilà.

---

La machine avait besoin de constitutions.

Pas de mythologie.

---

Avant de fermer le chapitre, Brutus sauvegarda :

**QUEEN / CODE / CRYSTAL CONTRACT v1**

---

Le Journal Vivant nota :

Builder separated from authorizer.

Authorizer separated from verifier.

Runtime success separated from claim status.

Merged code separated from deployed runtime.

QueenCore authority rooted in explicit trust configuration.

Capabilities scoped by action and target.

Crystallizer preserves epistemic status.

Crystal snapshots bound to a tick.

Custody separated from object identity.

Stamps represent events, not permissions.

Combined requests cannot bypass separate gates.

Administrative power cannot create proof.

---

Brutus relut.

Puis ajouta les invariants :

**CODE != AUTHORITY.**

**AUTHORITY != TRUTH.**

**CRYSTAL != PROOF.**

**MERGED != RUNTIME_PROOF.**

**AUTHORIZED != EXECUTED.**

**EXECUTED != RECORDED.**

**RECORDED != PROVED.**

**VALID SIGNATURE != VALID CLAIM.**

**PACKAGING MUST NOT ESCALATE EPISTEMIC STATUS.**

**SUPERUSER != SUPERTRUTH.**

---

Puis il regarda Astra.

---

La Reine pouvait autoriser.

---

Le code pouvait fabriquer.

---

Le verifier pouvait vérifier l’intégrité.

---

Le registre pouvait enregistrer.

---

Et le cristal pouvait traverser tout le système sans perdre son identité.

---

Mais aucun ne pouvait voler au monde scientifique le droit de répondre lui-même à la question :

**est-ce vrai ?**

---

Brutus posa le cristal devant Astra Station.

---

Le QR apparut.

---

CRYSTAL-F72-0002.

SUPPORTED_UNDER_SCOPE.

PROOF: NONE.

---

Parfait.

---

Le code avait fait son travail.

La Reine avait fait le sien.

Le cristal aussi.

---

Aucun n’avait dépassé sa frontière.

---

Brutus ouvrit la page suivante.

---

# LA TRACE DEVIENT LOI

---

Car maintenant que chaque rôle savait ce qu’il avait le droit de faire…

il fallait inscrire ces frontières si profondément dans Brutus qu’aucune interface, aucun worker et aucune Reine ne puisse les oublier par accident.
