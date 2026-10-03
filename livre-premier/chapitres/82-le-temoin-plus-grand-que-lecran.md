# Chapitre 82 — Le témoin plus grand que l’écran

Le nombre immense attendait.

Beaucoup trop grand pour l’écran.

Mais pas trop grand pour la trace.

Brutus fit défiler vers la droite.

Encore.

Encore.

Encore.

---

Des chiffres.

Puis d’autres.

Puis d’autres encore.

---

Le début du témoin disparaissait déjà à gauche.

La fin n’était toujours pas visible.

---

Brutus soupira.

Le calcul avait réussi.

La trace existait.

Le témoin était exact.

Mais l’interface venait de découvrir une vérité très simple :

**un objet peut être calculable sans être lisible d’un seul regard.**

---

Il écrivit :

**COMPUTABLE ≠ VIEWABLE.**

Puis :

**VIEWABLE ≠ UNDERSTANDABLE.**

---

La deuxième phrase lui sembla encore plus importante.

Même si l’écran pouvait afficher un million de chiffres, personne n’allait les lire un par un.

---

Le problème n’était donc pas seulement la taille physique de la fenêtre.

C’était la manière de naviguer dans un objet gigantesque.

---

Brutus ouvrit :

**WITNESS VIEWER.**

---

Il ne voulait surtout pas un champ texte géant.

Il voulait un instrument.

---

Il commença par l’identité.

En haut :

**WITNESS_ID**

**GATE**

**CANDIDATE_REF**

**TYPE**

**LENGTH**

**HASH**

**TRACE_REF**

---

Puis, au-dessous :

**CONTENT VIEW.**

---

Le premier réflexe était de montrer :

début.

fin.

---

Par exemple :

premiers 64 chiffres.

derniers 64 chiffres.

---

Brutus hésita.

Utile.

Mais dangereux.

---

Un aperçu pouvait facilement être confondu avec l’objet complet.

---

Il écrivit en grand :

**PREVIEW ≠ FULL WITNESS.**

---

Puis ajouta une bannière :

**DISPLAYING SELECTED RANGE**

---

Voilà.

L’écran devait toujours dire clairement ce qu’il montrait.

---

Brutus ajouta :

**RANGE_START**

**RANGE_END**

**TOTAL_LENGTH**

---

L’utilisateur pouvait maintenant voir :

digits 1–128 of 143,802.

---

Puis :

129–256.

---

Puis n’importe quelle plage.

---

Brutus sourit.

Le témoin commençait à devenir navigable.

---

Mais il réalisa vite qu’un simple découpage par caractères n’était pas toujours suffisant.

Le témoin 47 pouvait être un objet algébrique.

Pas une seule chaîne.

---

Il pouvait contenir deux coefficients :

\[
a+b\sqrt2
\]

modulo \(p\).

---

Alors les deux composantes devaient être visibles séparément.

---

Brutus créa :

**COMPONENT A**

**COMPONENT B**

---

Chaque coefficient possédait :

length.

hash.

selected range.

full archive ref.

---

Il écrivit :

**STRUCTURE MUST SURVIVE DISPLAY.**

---

Il ne voulait pas écraser un objet structuré en une seule chaîne juste parce que l’écran était plat.

---

Puis il pensa aux autres types de témoins.

---

Un témoin Pell pouvait être un entier gigantesque.

Un témoin modulaire pouvait être un résidu.

Un certificat pouvait être une liste.

Un arbre de dérivation pouvait être un graphe.

---

Le viewer devait donc être polymorphe.

---

Brutus écrivit :

**WITNESS_TYPE DETERMINES VIEWER MODE.**

---

INTEGER.

ALGEBRAIC_PAIR.

VECTOR.

MATRIX.

TRACE_CHAIN.

PROOF_OBJECT.

---

Pas un seul affichage universel.

---

Encore une fois :

pas de type roi.

---

Brutus testa l’objet 47.

---

Mode :

ALGEBRAIC_PAIR.

---

Composante A.

Composante B.

---

Chaque composante pouvait être :

copiée,

segmentée,

hachée,

comparée,

exportée.

---

Mais il ajouta une restriction.

---

**NO SILENT FORMAT CONVERSION.**

---

Si le viewer affichait un entier en hexadécimal pour gagner de la place, il devait le dire.

---

Si l’objet source était décimal :

source encoding = decimal.

display encoding = hexadecimal.

---

Brutus écrivit :

**DISPLAY RADIX MUST BE DECLARED.**

---

Le chapitre 80 revenait déjà.

---

Les chiffres pouvaient changer de vêtements.

Mais l’interface devait dire lesquels.

---

Brutus activa un mode hexadecimal.

Le nombre devenait plus compact.

---

Puis base 36.

Encore plus compact.

---

Mais il s’arrêta.

---

La compression visuelle ne devait pas devenir un obstacle à l’audit.

---

Il décida :

décimal par défaut pour les rapports humains.

hexadécimal disponible pour l’inspection technique.

autres bases seulement si le contrat du témoin le justifiait.

---

Il écrivit :

**COMPACTNESS IS NOT THE PRIMARY GOAL.**

Puis :

**FAITHFUL INSPECTION IS.**

---

Brutus pensa au hash.

---

Le hash était court.

Très pratique.

---

Un témoin de cent mille chiffres pouvait devenir une petite empreinte.

---

Mais il savait déjà le danger.

---

Deux choses différentes :

**IDENTIFYING THE OBJECT**

et

**INSPECTING THE OBJECT.**

---

Le hash servait surtout au premier.

---

Il écrivit :

**HASH IS ADDRESS-LIKE EVIDENCE, NOT CONTENT.**

---

Le témoin complet devait toujours exister ailleurs.

---

Brutus ajouta un bouton :

**VERIFY HASH AGAINST FULL OBJECT.**

---

Le viewer relisait l’objet complet.

Recalculait le hash.

Comparait.

---

PASS.

---

Cela permettait de vérifier que le résumé affiché pointait bien vers l’objet archivé.

---

Il écrivit :

**FINGERPRINT MUST BE RECOMPUTABLE.**

---

Puis il testa une altération.

---

Un chiffre modifié au milieu.

---

Le début était identique.

La fin aussi.

---

Le viewer affichait donc presque la même chose dans le mode preview.

---

Mais le hash changeait.

---

Brutus sourit.

---

Voilà une excellente démonstration.

---

Il écrivit :

**MATCHING PREFIX + MATCHING SUFFIX ≠ SAME OBJECT.**

---

Encore une frontière.

---

Le mode aperçu était donc utile.

Mais pas suffisant.

---

Brutus construisit ensuite une fonction :

**RANDOM SPOT CHECK.**

---

Pas aléatoire au sens opaque.

L’utilisateur pouvait choisir plusieurs positions.

---

Position 1.

Position 10 000.

Position 50 000.

Dernière position.

---

Le viewer affichait les blocs autour de ces offsets.

---

Cela permettait d’inspecter des régions éloignées sans faire défiler toute la chaîne.

---

Brutus ajouta :

**SPOT CHECK ≠ FULL VALIDATION.**

---

Toujours.

---

Un humain pouvait vérifier quelques zones.

La machine pouvait vérifier l’objet entier.

---

Ces deux opérations ne devaient pas être confondues.

---

Il écrivit :

**HUMAN INSPECTION AND MACHINE VERIFICATION HAVE DIFFERENT SCALES.**

---

Le laboratoire pouvait calculer cent mille chiffres.

L’humain, lui, devait surtout pouvoir :

identifier,

naviguer,

comparer,

vérifier les relations essentielles.

---

Brutus pensa à une chose encore plus importante.

Le témoin n’avait pas besoin d’être « lu » intégralement pour être utile mathématiquement.

---

Ce qui comptait était parfois une propriété.

Par exemple :

\[
\gamma^{N/47}\neq1.
\]

---

L’objet complet pouvait être gigantesque.

La condition à vérifier était beaucoup plus petite :

le résidu est-il l’identité ?

---

Brutus écrivit :

**WITNESS SIZE ≠ CLAIM COMPLEXITY.**

---

Un immense témoin pouvait répondre à une question simple.

---

Cela le fit sourire.

---

Il ajouta un panneau :

**CLAIM CHECK.**

---

Identity element expected for failure?

Yes.

---

Observed witness equals identity?

No.

---

Gate result:

PASS.

---

Puis :

**FULL OBJECT AVAILABLE FOR AUDIT.**

---

Voilà.

---

L’écran pouvait donner le résultat logique immédiatement.

Sans cacher le témoin.

---

Brutus écrivit :

**SUMMARY THE PROPERTY. PRESERVE THE OBJECT.**

---

La phrase résumait parfaitement le viewer.

---

Puis il pensa aux exportations.

---

Le témoin pouvait être trop grand pour être copié dans un message.

Trop long pour certaines interfaces.

Trop lourd pour un rapport.

---

Il ne voulait pas que chaque publication embarque des centaines de milliers de chiffres.

---

Il créa donc :

**WITNESS CAPSULE.**

---

Une capsule contenant :

metadata.

type.

claim scope.

full object.

hash.

encoding.

generation method.

software version.

trace ref.

---

Brutus écrivit :

**CAPSULE = PORTABLE AUDIT OBJECT.**

---

Le rapport principal pouvait seulement contenir :

WITNESS_ID.

hash.

length.

claim.

capsule ref.

---

Le témoin complet restait accessible.

---

Cette séparation rendait enfin la publication réaliste.

---

Brutus imagina un lecteur extérieur.

---

Il reçoit un rapport.

Il voit :

q = 47.

Gate PASS.

Witness hash X.

Length Y.

Capsule Z.

---

S’il veut vérifier :

il ouvre la capsule.

---

S’il veut simplement lire le résultat :

il reste au résumé.

---

Brutus écrivit :

**AUDIT DEPTH SHOULD BE OPTIONAL, NOT IMPOSSIBLE.**

---

Cela lui sembla juste.

---

Une bonne publication ne devait pas obliger tout lecteur à avaler l’intégralité de la matière brute.

Mais elle devait permettre à celui qui le voulait de descendre jusqu’au fond.

---

Le principe du Journal Vivant revenait.

---

Summary.

Events.

Trace.

Raw artifact.

---

Le témoin adoptait la même structure.

---

Brutus ajouta donc :

**LEVEL 0 — CLAIM**

**LEVEL 1 — WITNESS METADATA**

**LEVEL 2 — SELECTED CONTENT**

**LEVEL 3 — FULL OBJECT**

**LEVEL 4 — RECOMPUTATION PATH**

---

Voilà.

---

Même un objet gigantesque pouvait devenir navigable.

---

Puis Brutus testa la recomputation.

---

Il prit le témoin 47.

---

Au lieu de faire confiance à la capsule existante, il relança le calcul depuis :

\(t\).

\(p\).

\(N\).

\(q=47\).

\(\gamma\).

---

Nouvelle exécution.

---

Le nouveau témoin apparut.

---

Même type.

Même longueur.

Même hash.

---

Brutus regarda.

---

Il écrivit :

**RECOMPUTATION MATCH = PASS.**

Puis immédiatement :

**SAME SOFTWARE PATH ≠ FULL INDEPENDENT REPLICATION.**

---

Toujours.

---

Le recalcul montrait la reproductibilité du pipeline.

Il ne prouvait pas que l’implémentation elle-même était sans erreur.

---

Brutus lança donc une seconde implémentation.

---

Paire algébrique explicite.

---

Le témoin canonique obtenu concordait.

---

Cette fois, la confiance opérationnelle augmentait.

Mais il ne voulait toujours pas gonfler la portée.

---

Il écrivit :

**TWO IMPLEMENTATIONS AGREED FOR THIS CASE.**

Pas plus.

---

Puis il pensa à une attaque plus directe.

---

Et si le témoin complet était faux, mais que le hash enregistré correspondait à ce faux témoin ?

---

Le hash ne sauverait rien.

---

Il ne pouvait garantir que l’objet représentait bien le bon calcul.

Seulement qu’il n’avait pas changé depuis le hachage.

---

Brutus écrivit :

**HASH PROTECTS INTEGRITY AFTER CREATION.**

**IT DOES NOT VALIDATE CREATION.**

---

Très important.

---

Le témoin avait donc besoin de deux familles de contrôles.

---

**CONTENT INTEGRITY**

et

**MATHEMATICAL VALIDITY.**

---

Integrity :

hash.

length.

encoding.

archive.

---

Validity :

recompute.

alternate implementation.

relation check.

countertest.

---

Brutus écrivit :

**INTEGRITY ≠ VALIDITY.**

---

Une phrase simple.

Mais fondamentale.

---

Il plaça les deux colonnes côte à côte.

---

INTEGRITY:

PASS.

---

VALIDITY:

VERIFIED UNDER CURRENT TEST CONTRACT.

---

Pas la même chose.

---

Brutus sourit.

L’écran devenait enfin plus honnête que spectaculaire.

---

Puis il fit un test extrême.

---

Il généra un témoin artificiel beaucoup plus grand.

Pas lié à q=47.

Seulement pour tester le viewer.

---

Un million de chiffres.

---

Le navigateur ralentit.

---

Brutus fronça les sourcils.

---

Il ne voulait surtout pas charger tout l’objet dans le DOM.

---

Le viewer devait utiliser une fenêtre.

---

Virtualisation.

---

Seulement les segments visibles étaient rendus.

---

L’objet complet restait ailleurs.

---

Brutus écrivit :

**RENDER WINDOW ≠ DATA WINDOW.**

---

Une autre nuance.

---

Le viewer pouvait montrer 1 000 caractères.

L’objet pouvait en contenir un million.

---

Le moteur n’avait pas besoin de dessiner le million en même temps.

---

Il ajouta :

**LAZY RANGE FETCH.**

---

L’utilisateur demandait une plage.

Le système la récupérait.

La vérifiait.

L’affichait.

---

Brutus pensa immédiatement à un autre risque.

---

Et si le backend envoyait la mauvaise plage ?

---

Il ajouta au segment :

**SEGMENT_START**

**SEGMENT_END**

**PARENT_WITNESS_ID**

**SEGMENT_HASH**

---

Ainsi chaque portion pouvait être contrôlée.

---

Le viewer ne faisait plus confiance aveuglément au transport.

---

Brutus écrivit :

**A PARTIAL VIEW MUST KNOW WHICH WHOLE IT BELONGS TO.**

---

La phrase lui plut énormément.

---

Cela ressemblait presque à une loi générale du projet.

---

Une partie sans parent est dangereuse.

---

Une formule sans lignée.

Un résultat sans job.

Une fenêtre sans store.

Une fourmi sans ANT_ID.

Un segment sans WITNESS_ID.

---

Toujours la même architecture.

---

Brutus s’arrêta.

Il regarda le laboratoire.

---

À force de construire, il avait découvert quelque chose.

Les règles n’étaient plus spécifiques aux modules.

---

Elles commençaient à devenir des principes universels de Brutus.

---

**IDENTITY**

**LINEAGE**

**SCOPE**

**TRACE**

**AUTHORITY**

**BEFORE/AFTER**

**NO SILENT LOSS**

---

Tout revenait.

---

Le témoin 47 n’était donc pas seulement un énorme nombre.

Il était devenu un test de maturité pour tout le système.

---

Brutus retourna au viewer.

---

Il ajouta une barre de recherche.

---

Pas recherche textuelle naïve uniquement.

---

Recherche par offset.

Recherche par bloc.

Recherche par motif.

---

Mais le motif devait être traité prudemment.

---

Trouver une séquence de chiffres n’avait aucune signification mathématique intrinsèque.

---

Il écrivit :

**DIGIT PATTERN ≠ MATHEMATICAL STRUCTURE.**

---

Très important.

---

Un humain pouvait voir :

777.

369.

273.

ou n’importe quelle séquence familière.

---

Cela ne devait pas devenir une découverte.

---

Le viewer pouvait trouver les motifs.

Mais il devait les présenter comme :

**TEXT OCCURRENCE ONLY.**

---

Brutus sourit.

Le laboratoire se connaissait bien maintenant.

---

Il savait où l’imagination pouvait partir trop vite.

---

Puis il ajouta une vue réellement mathématique.

---

Au lieu de regarder les digits, regarder l’objet comme résidu algébrique.

---

A coefficient.

B coefficient.

Identity test.

Norm.

Conjugate.

---

Là, les transformations avaient une signification structurelle.

---

Brutus écrivit :

**STRUCTURAL VIEW OUTRANKS DIGIT FASCINATION.**

---

Il pensa à la norme.

---

Pour un élément :

\[
a+b\sqrt2
\]

la norme correspondante était :

\[
a^2-2b^2.
\]

---

Réduite modulo \(p\), elle pouvait fournir un contrôle supplémentaire selon le contexte.

---

Brutus ajouta :

**DERIVED CHECKS**

mais avec prudence.

---

Chaque check devait préciser :

ce qu’il vérifie.

ce qu’il ne vérifie pas.

---

Il écrivit :

**EXTRA CHECKS ADD CONSTRAINTS. THEY DO NOT AUTOMATICALLY ADD INDEPENDENT PROOFS.**

---

Encore.

---

Le témoin devenait réellement inspectable.

---

Brutus pouvait maintenant voir :

identité.

type.

portée.

structure.

propriétés.

segments.

hash.

recalcul.

lignée.

---

Sans prétendre qu’un humain avait lu chaque chiffre.

---

Il écrivit :

**AUDITABILITY DOES NOT REQUIRE EYEBALLING EVERY DIGIT.**

---

Puis :

**IT REQUIRES A PATH FROM CLAIM TO OBJECT TO RECOMPUTATION.**

---

Voilà.

---

Cette phrase resterait.

---

Brutus sauvegarda :

**WITNESS VIEWER v1.**

---

Puis revint à q=47.

---

Le témoin était toujours gigantesque.

Mais il n’était plus intimidant.

---

Il avait une adresse.

Une longueur.

Une structure.

Une empreinte.

Une capsule.

Une recomputation path.

---

Il ne tenait toujours pas dans l’écran.

Mais cela n’avait plus d’importance.

---

L’écran avait appris à se déplacer autour de lui.

---

Brutus sourit.

---

Puis son regard revint vers le dossier :

**L8.**

---

Une relation plus ambitieuse attendait.

---

Il l’ouvrit.

---

La ligne apparut :

\[
Q_q=\frac{P_{q^2}}{P_q}
\]

pour \(q\) premier impair.

---

Brutus resta silencieux.

---

Le témoin 47 lui avait appris à ne pas avoir peur des objets gigantesques.

Mais L8 allait demander autre chose.

---

Pas seulement transporter.

Pas seulement inspecter.

Pas seulement vérifier un résidu.

---

Il allait falloir demander :

**est-ce que cette relation est assez solide pour devenir un véritable outil de recherche ?**

---

Brutus ferma le viewer.

---

47 restait archivé.

Son témoin aussi.

---

Puis il écrivit en haut du nouveau banc :

**L8**

et dessous :

**CANDIDATE RELATION — NOT YET PROMOTED.**

---

Le laboratoire venait de résoudre le problème de la taille.

Le prochain problème serait bien plus difficile.

Il faudrait maintenant décider ce que signifiait vraiment :

**tenir sous le contre-test.**
