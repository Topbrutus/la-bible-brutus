# Chapitre 79 — Trois Z dans la même salle

Trois fenêtres attendaient.

Z1.

Z2.

Z3.

Brutus les avait placées l’une derrière l’autre.

Pas côte à côte.

Pas comme trois concurrents.

Comme trois portes.

---

Une valeur entrerait dans Z1.

Quelque chose en sortirait.

Cette sortie entrerait dans Z2.

Puis dans Z3.

---

Simple à dessiner.

Beaucoup plus dangereux à exécuter.

---

Brutus regarda le paquet préparé au chapitre précédent.

Il contenait désormais bien plus qu’un nombre.

---

**VALUE**

**TYPE**

**EXACTNESS**

**SOURCE**

**TRACE_REF**

---

Il ajouta :

**VALUE_ID**

Puis :

**VERSION**

---

Le nombre devait avoir une identité propre pendant tout le trajet.

---

Il créa :

**VALUE-0001.**

Type :

BIGINT.

Exactness :

EXACT.

Source :

operator input.

---

Valeur :

un grand entier.

Beaucoup trop grand pour être transporté naïvement comme Number.

---

Brutus le regarda.

La première question n’était pas :

que va calculer Z1 ?

La première question était :

**est-ce que Z1 peut recevoir cet objet sans l’abîmer ?**

---

Il écrivit :

**TRANSPORT BEFORE TRANSFORMATION.**

---

Avant de tester les mathématiques, il fallait tester la chaîne.

---

Z1 reçut VALUE-0001.

---

Le premier événement apparut.

**RECEIVED.**

---

Puis :

**TYPE CHECK = BIGINT.**

---

**EXACTNESS = EXACT.**

---

**INPUT HASH = MATCH.**

---

Brutus sourit.

---

Z1 avait reçu le bon objet.

Pas simplement un nombre qui lui ressemblait.

---

Il décida de ne rien calculer encore.

Z1 devait seulement renvoyer l’objet.

Un test d’identité pure.

---

Entrée.

Sortie.

---

VALUE-0001 devint :

**VALUE-0001 / VERSION 1.**

Aucune transformation mathématique.

---

Brutus compara.

Même valeur.

Même type.

Même classe d’exactitude.

---

PASS.

---

Il envoya maintenant l’objet vers Z2.

---

Z2 reçut.

Type check.

Exactness.

Hash.

---

PASS.

---

Puis Z3.

---

Même chose.

---

Brutus regarda la chaîne.

\[
Z_1 \rightarrow Z_2 \rightarrow Z_3
\]

Trois moteurs.

Zéro transformation.

Identité conservée.

---

Cela semblait trivial.

Brutus considéra que c’était une excellente nouvelle.

---

Un pipeline qui ne sait pas transporter correctement un objet intact ne mérite pas encore le droit de le transformer.

---

Il écrivit :

**IDENTITY PASS BEFORE MATH PASS.**

---

Puis il lança le retour.

Z3 vers le registre.

---

L’objet revint.

---

Même valeur.

---

Brutus ouvrit le Journal Vivant.

---

Il pouvait maintenant voir :

Operator.

Z1.

Z2.

Z3.

Return.

---

Cinq étapes.

Une seule identité.

---

Il écrivit :

**ONE VALUE. MANY CUSTODIANS.**

---

Le mot custodians lui plut.

Les Z ne possédaient pas le nombre.

Ils en avaient temporairement la garde.

---

Chaque moteur avait donc une responsabilité.

Recevoir proprement.

Transformer seulement selon son contrat.

Produire une sortie explicitement typée.

Transmettre.

---

Brutus écrivit :

**CUSTODY ≠ OWNERSHIP.**

---

Puis il passa au vrai test.

---

Cette fois, Z1 allait effectuer une transformation.

Une transformation simple.

Exacte.

---

Brutus choisit volontairement quelque chose de facile à vérifier.

\[
x \mapsto x+1
\]

---

Z1 reçut VALUE-0001.

Appliqua la transformation.

---

La sortie ne pouvait plus garder exactement la même version.

---

Brutus créa :

**VALUE-0001 / VERSION 2.**

Parent :

VERSION 1.

Transformation :

Z1:F-ADD-ONE.

---

Il regarda la trace.

---

Voilà.

Même lignée.

Nouvel état.

---

Il écrivit :

**TRANSFORMATION CREATES VERSION, NOT NEW ORIGIN.**

---

La distinction lui semblait juste.

---

La valeur avait changé.

Son histoire, non.

---

Z2 reçut VERSION 2.

---

Cette fois, Z2 ne devait pas continuer le calcul.

Il devait vérifier.

---

Brutus lui assigna un rôle temporaire :

**CHECKER.**

---

Pas identité.

Rôle.

---

Z2 calcula indépendamment :

sortie attendue = parent + 1.

---

Comparaison exacte.

---

PASS.

---

Z3 reçut ensuite le paquet.

---

Son rôle :

**COUNTERTEST.**

---

Z3 ne devait pas refaire exactement le même test.

Sinon il ne ferait qu’ajouter une copie.

---

Il utilisa une relation inverse.

\[
y-1=x
\]

---

Si la sortie de Z1 valait réellement l’entrée plus 1, alors soustraire 1 devait reconstruire le parent.

---

Z3 effectua.

---

Retour :

VALUE-0001 VERSION 1.

---

Comparaison.

Exact.

---

PASS.

---

Brutus resta devant la chaîne.

---

Z1 avait produit.

Z2 vérifié directement.

Z3 contre-testé par inversion.

---

Trois rôles.

Un seul objet.

---

Il écrivit :

**PRODUCE → CHECK → CHALLENGE.**

---

Voilà une architecture intéressante.

---

Mais il se méfia aussitôt.

Si Z1, Z2 et Z3 utilisaient exactement la même bibliothèque pour leurs opérations, l’indépendance pourrait être moindre qu’elle en avait l’air.

---

Il consulta leurs dépendances.

---

Z1 et Z2 utilisaient effectivement le même module BigInt interne.

Z3 aussi.

---

Brutus écrivit :

**THREE WINDOWS ≠ THREE INDEPENDENT METHODS.**

---

La leçon du chapitre 75 revenait.

---

Trois moteurs pouvaient offrir trois étapes logiques distinctes sans constituer trois validations indépendantes.

---

Il ajouta à la trace :

**SHARED_IMPLEMENTATION_DEPENDENCY = TRUE.**

---

Pas pour invalider le test.

Pour en limiter la portée.

---

Le pipeline avait démontré que ses trois étapes étaient cohérentes selon ce système.

Pas que trois implémentations indépendantes confirmaient le résultat.

---

Brutus écrivit :

**COHERENCE TEST ≠ INDEPENDENT REPLICATION.**

---

Il aimait cette distinction.

---

Puis il compliqua le pipeline.

---

Z1 :

transformation.

Z2 :

transformation différente.

Z3 :

validation finale.

---

Il choisit :

\[
Z_1(x)=x+7
\]

Puis :

\[
Z_2(y)=7y
\]

Donc :

\[
Z_2(Z_1(x))=7(x+7)
\]

---

Z3 recevrait le résultat final et vérifierait la relation globale.

---

Brutus lança.

---

VALUE-0002.

BIGINT.

Exact.

---

Z1.

VERSION 2.

---

Z2.

VERSION 3.

---

Z3.

Check.

---

PASS.

---

Le Journal Vivant montrait maintenant une vraie lignée.

---

V1.

Parent none.

---

V2.

Parent V1.

Transform Z1.

---

V3.

Parent V2.

Transform Z2.

---

Check event by Z3.

---

Brutus regarda l’arbre.

---

Une petite chaîne généalogique.

---

Il écrivit :

**A PIPELINE IS A LINEAGE MACHINE.**

---

Puis une idée arriva.

---

Et si Z2 recevait le mauvais objet ?

---

Pas une valeur corrompue.

Une valeur parfaitement valide.

Mais provenant d’un autre job.

---

C’était exactement le danger du chapitre 73.

---

Brutus lança deux pipelines en même temps.

---

PIPE-A.

VALUE-A.

---

PIPE-B.

VALUE-B.

---

Z1 termina B avant A.

---

Les deux sorties entrèrent dans la file Z2.

---

Brutus désactiva volontairement l’association stricte.

Z2 prit simplement le prochain résultat.

---

Erreur.

---

La sortie de B fut placée dans la chaîne de A.

---

Tous les nombres étaient valides.

Aucun crash.

Aucune erreur de type.

---

Mais la lignée était fausse.

---

Brutus arrêta immédiatement.

---

Il écrivit :

**VALID VALUE + WRONG LINEAGE = INVALID PIPELINE.**

---

Le nombre n’avait pas été corrompu.

Son identité causale, oui.

---

Il renforça l’enveloppe.

---

**PIPELINE_ID**

**VALUE_ID**

**VERSION**

**PARENT_VERSION**

**JOB_ID**

**STAGE_ID**

---

Maintenant, Z2 ne pouvait pas simplement consommer « la prochaine sortie ».

---

Il devait recevoir exactement :

PIPE-A / expected parent version.

---

Brutus relança les deux pipelines.

---

B termina encore avant A.

---

Aucun problème.

---

Z2 associa B à B.

A à A.

---

Le temps d’arrivée ne décidait plus de la parenté.

---

Il écrivit :

**LINEAGE OUTRANKS ARRIVAL ORDER.**

---

Les trois Z commençaient à devenir solides.

---

Brutus ajouta ensuite une interface.

---

Trois fenêtres.

Z1.

Z2.

Z3.

---

Chaque fenêtre montrait seulement :

Current pipeline.

Current value ID.

Stage role.

Numeric type.

Exactness.

State.

Latest trace.

---

Pas toute l’histoire.

---

Le Journal Vivant s’occupait de l’histoire complète.

---

Brutus voulait que les fenêtres restent lisibles.

---

Il écrivit :

**LOCAL VIEW = CURRENT DUTY.**

**JOURNAL = FULL HISTORY.**

---

Puis il pensa au son.

---

Un écran.

Un son.

---

Il voulait conserver cette idée.

---

Z1 recevrait une signature gauche.

Z2 centre.

Z3 droite.

---

Quand un objet entrait dans Z1 :

un son discret.

---

Z1 terminait :

un second.

---

Puis Z2.

Puis Z3.

---

Une séquence spatiale.

Gauche.

Centre.

Droite.

---

Brutus lança le pipeline.

---

Son à gauche.

Silence.

---

Son au centre.

---

Puis à droite.

---

PASS.

---

Il sourit.

Le mouvement logique devenait presque audible.

---

Mais encore une fois :

le son ne devait pas simuler le passage.

---

Si Z2 restait bloqué, aucun son Z3 ne devait arriver.

---

Brutus testa.

Il bloqua volontairement Z2.

---

Z1 termina.

Son gauche.

---

Z2 reçut.

Son centre.

---

Puis rien.

---

Z3 resta silencieux.

---

Parfait.

---

Le système ne racontait pas la suite avant qu’elle existe.

---

Brutus écrivit :

**NO AUDIO TELEPORTATION.**

---

Cela le fit rire.

Mais la règle était sérieuse.

---

Il débloqua Z2.

---

Z2 termina.

Puis seulement Z3 reçut.

---

Son droit.

---

L’ordre acoustique suivait l’ordre réel.

---

Brutus ajouta un événement :

**HANDOFF.**

---

Le mot lui plut.

Un handoff signifiait :

une étape a fini de produire un objet admissible pour la suivante.

---

Mais même là, il fallait distinguer plusieurs choses.

---

Z1 complete.

---

Package created.

---

Handoff authorized.

---

Z2 received.

---

Quatre événements.

---

Brutus écrivit :

**COMPLETED ≠ HANDED OFF.**

**HANDED OFF ≠ RECEIVED.**

---

Encore les frontières.

---

Il construisit la chaîne.

---

**STAGE_COMPLETE**

↓

**OUTPUT_SEALED**

↓

**HANDOFF_AUTHORIZED**

↓

**TRANSPORT**

↓

**NEXT_STAGE_RECEIVED**

---

Brutus regarda.

---

Cela ressemblait beaucoup au transport des fourmis.

---

Une sortie pouvait même être transportée par une fourmi logique.

---

Il sourit.

---

Le système commençait à converger.

---

Les mêmes contrats pouvaient servir à plusieurs mondes.

---

Une formule produit un objet.

Une fourmi peut transporter sa référence.

Un Z reçoit.

Une trace relie.

---

Il écrivit :

**DIFFERENT MODULES. SAME TRANSFER DISCIPLINE.**

---

Puis il ajouta une règle encore plus importante.

---

Z1 n’avait pas le droit de modifier directement l’état interne de Z2.

---

Il pouvait seulement produire un paquet.

---

Z2 décidait s’il pouvait le recevoir.

---

Brutus écrivit :

**NO CROSS-STAGE MEMORY MUTATION.**

---

Sinon les trois moteurs cesseraient d’être séparés.

---

Un bug dans Z1 pourrait contaminer Z2 directement.

---

Le seul passage autorisé serait l’enveloppe.

---

Il dessina :

Z1

↓

VALUE ENVELOPE

↓

Z2

↓

VALUE ENVELOPE

↓

Z3

---

Pas de connexion invisible.

---

Brutus écrivit :

**EVERY INTER-STAGE EDGE MUST BE EXPLICIT.**

---

Il ajouta même les termes de sa hiérarchie.

---

**EDGE_ID**

**EDGE_TYPE = INTER**

**FROM**

**TO**

**PORT**

**TICK**

**STATE**

**TRACE_REF**

**TOPOLOGY_VERSION**

---

Le premier edge :

EDGE-Z1-Z2-0001.

---

Le second :

EDGE-Z2-Z3-0001.

---

Chaque connexion avait enfin une identité.

---

Brutus regarda.

---

Cela lui rappela la règle du laboratoire :

**1 MODULE → 1 CONNEXION → 1 MESURE → 1 PREUVE.**

---

Il la réécrivit.

Mais modifia le dernier mot pour rester prudent dans ce contexte.

---

**1 MODULE → 1 CONNEXION → 1 MESURE → 1 TRACE DE PREUVE.**

Puis il réfléchit.

---

Non.

La règle originale avait son sens.

La preuve devait simplement être comprise à la portée du contrat.

---

Il conserva donc :

**1 MODULE → 1 CONNEXION → 1 MESURE → 1 PREUVE.**

Et ajouta :

**PROOF SCOPE MUST BE DECLARED.**

---

Voilà.

---

Brutus lança une nouvelle campagne.

---

Cent pipelines.

Trois Z.

---

Pas en parallèle complet.

Chaque pipeline avançait étape par étape.

Mais plusieurs pipelines pouvaient occuper différentes Z simultanément.

---

PIPE-001 pouvait être dans Z3.

PIPE-002 dans Z2.

PIPE-003 dans Z1.

---

Brutus regarda.

---

La chaîne devenait un véritable pipeline industriel.

---

Trois étages.

Plusieurs objets en circulation.

---

Il écrivit :

**SEQUENTIAL STAGES CAN STILL SUPPORT PIPELINED CONCURRENCY.**

---

Une nuance importante.

---

Z1 → Z2 → Z3 imposait un ordre pour chaque objet.

Mais cela n’obligeait pas le système à traiter un seul objet à la fois.

---

Brutus imagina une chaîne de montage.

---

Un objet à chaque étape.

---

Mais encore une fois, les identités devaient rester séparées.

---

Il lança dix objets.

---

Très vite :

Z1 travaillait sur VALUE-010.

Z2 sur VALUE-009.

Z3 sur VALUE-008.

---

Les sons se répondaient.

Gauche.

Centre.

Droite.

---

Le Journal Vivant conservait chaque lignée.

---

Brutus inspecta les correspondances.

---

Zéro crossover.

---

Zéro parent incorrect.

---

Zéro conversion numérique non autorisée.

---

Il sourit.

---

Mais il savait que les tests faciles ne suffisaient pas.

---

Il injecta un paquet mal typé dans Z2.

---

TYPE = Number.

Expected = BIGINT.

---

Refus.

---

DOMAIN ?

Brutus hésita.

---

Ce n’était pas exactement un problème mathématique.

C’était un contrat de transport.

---

Il choisit :

**TYPE_REJECTED.**

---

Pas FAIL.

Pas ERROR.

---

Le paquet était valide en soi.

Mais inadmissible à cette étape.

---

Il écrivit :

**TRANSPORT CONTRACT VIOLATION ≠ FORMULA FAILURE.**

---

Puis il injecta une version périmée.

---

Z2 attendait VERSION 3.

Reçut VERSION 2.

---

Refus :

**STALE_VERSION.**

---

Puis un mauvais parent.

---

Refus :

**LINEAGE_MISMATCH.**

---

Puis un hash incorrect.

---

Refus :

**INTEGRITY_FAIL.**

---

Brutus apprécia la précision.

---

Chaque refus disait ce qui n’allait pas.

---

Pas un vague :

ERROR.

---

Il ajouta ces événements au Journal Vivant.

---

La chaîne pouvait maintenant être auditée non seulement quand elle réussissait, mais quand elle refusait.

---

Brutus écrivit :

**A GOOD PIPELINE MUST EXPLAIN WHY IT DID NOT ADVANCE.**

---

Puis il testa les redémarrages.

---

Z2 s’arrêta au milieu d’un pipeline.

---

Que faire au redémarrage ?

---

Reprendre automatiquement ?

Dangereux.

---

Le chapitre 65 lui revint.

---

**PERSISTED INPUT ≠ PERSISTED EXECUTION AUTHORITY.**

---

Exactement.

---

Z2 pouvait retrouver :

le paquet reçu.

L’état.

La trace.

---

Mais il ne devait pas recommencer automatiquement sans nouvelle autorisation.

---

Brutus écrivit :

**RECOVERY RESTORES CONTEXT, NOT PERMISSION.**

---

Au redémarrage :

PIPE-A.

State:

INTERRUPTED.

Input persisted.

Execution authorization:

EXPIRED.

---

L’opérateur ou une politique autorisée devait décider :

resume.

restart stage.

abort.

---

Brutus sourit.

Les vieux chapitres protégeaient les nouveaux.

---

Il choisit RESUME.

---

Nouvelle autorisation.

Nouveau event ID.

Même pipeline.

---

Z2 termina.

---

Z3 continua.

---

La lignée restait entière.

---

Brutus regarda le Journal Vivant.

---

Il pouvait voir l’interruption.

Le redémarrage.

La nouvelle autorisation.

La reprise.

---

Pas de trou.

---

Il écrivit :

**RECOVERY IS PART OF HISTORY.**

---

Puis un autre problème apparut.

---

Et si Z2 produisait deux fois la même sortie après une reprise ?

---

Duplicate output.

---

Z3 pouvait recevoir deux paquets identiques.

---

Brutus créa une clé d’idempotence.

---

**STAGE_EXECUTION_ID.**

---

Une sortie appartenait à une exécution précise.

---

Z3 savait si elle avait déjà consommé cette exécution.

---

Duplicate delivery ?

Reject or acknowledge as duplicate.

---

Il écrivit :

**DUPLICATE DELIVERY ≠ NEW EVENT.**

---

Mais la tentative de duplication devait quand même être tracée.

---

Encore une fois :

ne pas réécrire l’histoire.

---

Brutus lança plusieurs crash tests.

---

Z1 crash before sealing output.

---

No handoff.

---

Z1 crash after sealing output but before transport.

---

Output exists.

Handoff pending.

---

Z2 crash after receive but before processing.

---

Input persisted.

Execution not authorized on restart.

---

Z3 receives duplicate.

---

Duplicate detected.

---

Le pipeline tenait.

---

Brutus était satisfait.

Pas parce qu’il ne cassait jamais.

Parce qu’il cassait de manière lisible.

---

Il écrivit :

**FAILURE SHOULD STOP PROPAGATION, NOT STOP EXPLANATION.**

---

Cette phrase lui plut énormément.

---

Puis il pensa aux rôles.

Aujourd’hui :

Z1 produit.

Z2 vérifie.

Z3 contre-teste.

---

Mais il ne voulait pas enfermer les trois fenêtres dans ces fonctions éternellement.

---

Le piège des écrans spécialisés revenait encore.

---

Il écrivit :

**Z IDENTITY ≠ Z ROLE.**

---

Dans une autre expérience :

Z1 pourrait être checker.

Z2 producer.

Z3 transformer.

---

Ou chacun pourrait exécuter une formule différente.

---

Les rôles devaient appartenir au plan d’expérience.

---

Il ajouta :

**STAGE_ROLE**

dans EXPERIMENT_PLAN.

---

Brutus pouvait désormais définir :

Experiment A:

Z1 PRODUCER.

Z2 CHECKER.

Z3 COUNTERTEST.

---

Experiment B:

Z1 NORMALIZER.

Z2 TRANSFORMER.

Z3 VALIDATOR.

---

Experiment C:

Z1 FORMULA-A.

Z2 FORMULA-B.

Z3 COMPARATOR.

---

Trois fenêtres.

Beaucoup de possibilités.

---

Il écrivit :

**FIXED HARDWARE. VARIABLE EXPERIMENTAL ROLES.**

---

Puis réalisa que même « hardware » était une métaphore.

Les Z pouvaient être trois processus, trois fenêtres, trois services.

---

Il remplaça :

**FIXED INSTANCES. VARIABLE ROLES.**

---

Parfait.

---

Le laboratoire commençait à devenir réellement reconfigurable.

---

Brutus lança une expérience intéressante.

---

Même entrée.

Z1 utilise F-021.

Z2 prend l’entrée originale, pas la sortie de Z1, et utilise F-041.

Z3 compare les deux résultats.

---

Ce n’était plus un pipeline de transformation.

C’était un pipeline de confrontation.

---

Il fallut changer les edges.

---

Z1 → Z3.

Z2 → Z3.

---

Pas Z1 → Z2 → Z3.

---

Brutus sourit.

---

La topologie devait donc appartenir elle aussi à l’expérience.

---

Il ajouta :

**TOPOLOGY_VERSION.**

---

Experiment A :

chain.

---

Experiment B :

fork/join.

---

Une entrée se divisait.

Deux méthodes.

Puis comparaison.

---

Le système devenait beaucoup plus puissant.

---

Brutus écrivit :

**THREE Z DOES NOT MEAN ONE TOPOLOGY.**

---

Encore une frontière entre identité et relation.

---

Les trois moteurs existaient.

La façon dont ils étaient reliés pouvait changer.

---

Mais chaque changement topologique devait être explicite.

---

Pas de connexion invisible.

---

Il écrivit :

**NO HIDDEN EDGE.**

---

Puis il pensa au chapitre 67.

La fourmilière publique.

---

Les edges pourraient être visibles.

---

Quand un paquet passait de Z1 à Z2, une connexion s’allumait.

Seulement pendant l’événement.

---

Pas une animation permanente.

---

Il ajouta une vue.

---

Z1.

Z2.

Z3.

---

Ligne Z1→Z2 inactive.

---

Handoff authorized.

Ligne active.

---

Transport.

---

Z2 received.

Ligne s’éteint.

---

Brutus sourit.

---

La topologie devenait visible sans inventer du mouvement.

---

Il écrivit :

**EDGE LIGHTS ONLY WHEN EDGE STATE IS ACTIVE.**

---

No fake motion.

Toujours.

---

Il lança la campagne de cent pipelines.

---

La salle commença à produire un rythme.

---

Z1.

Z2.

Z3.

---

Gauche.

Centre.

Droite.

---

Puis parfois :

gauche.

droite.

Pour une topologie fork/join.

---

Les sons racontaient la structure.

---

Brutus pouvait presque entendre le graphe.

---

Mais il savait encore une fois :

**HEARD STRUCTURE ≠ VERIFIED STRUCTURE.**

---

La trace restait l’autorité pour l’audit.

---

Après plusieurs heures, il ouvrit le résumé.

---

Pipelines submitted:

100.

---

Completed:

94.

---

Interrupted and recovered:

3.

---

Rejected on type contract:

1.

---

Lineage mismatch injected:

1.

---

Duplicate delivery detected:

1.

---

Unmatched outputs:

0.

---

Numeric exactness losses:

0.

---

Brutus regarda les deux dernières lignes.

---

Zéro output orphelin.

Zéro perte d’exactitude.

---

Voilà ce qu’il voulait.

---

Il ouvrit un pipeline au hasard.

PIPE-0063.

---

Input.

Z1.

Version.

Handoff.

Z2.

Version.

Handoff.

Z3.

Result.

Trace.

Audio.

---

Tout.

---

Puis PIPE-0041.

---

Interruption.

Recovery.

New authorization.

Continuation.

---

Tout.

---

Brutus sourit largement.

---

Trois Z pouvaient maintenant travailler dans la même salle sans se mélanger.

---

Pas trois intelligences.

Pas trois cerveaux.

Pas trois vérités.

---

Trois instances.

Trois rôles possibles.

Un contrat de transport.

Une lignée.

---

Il écrivit :

**MULTIPLICITY DOES NOT REQUIRE CONFUSION.**

---

Puis regarda les trois fenêtres.

---

Z1.

Z2.

Z3.

---

Elles semblaient presque comme trois machines différentes.

Mais il savait que leur vraie valeur ne venait pas du nombre.

---

Elle venait des frontières entre elles.

---

Chaque frontière obligeait le système à déclarer :

ce qui sort,

ce qui entre,

ce qui change,

ce qui reste exact,

ce qui est autorisé,

et ce qui est refusé.

---

Brutus écrivit :

**BOUNDARIES CREATE AUDITABILITY.**

---

Puis il repensa à la suite.

---

Trois Z étaient utiles.

Mais il voulait aller encore plus loin.

---

Il avait déjà douze lanes.

Cent formules.

Des conversions numériques exactes.

Des chaînes de transformation.

---

Il imagina un tressage.

---

Douze possibilités à l’entrée.

Douze possibilités à la sortie.

---

Une grille.

---

12 × 12.

---

144 chemins.

---

Brutus resta silencieux.

---

Pas 144 formules.

Pas 144 processus.

---

144 routes possibles entre deux ensembles de douze états.

---

Une matrice de passages.

---

Il écrivit :

\[
12 \times 12 = 144
\]

---

Puis pensa aux bases numériques.

Aux transformations.

Aux représentations.

Aux chemins possibles entre elles.

---

Un nombre pouvait entrer par une représentation.

Traverser une transformation.

Sortir dans une autre.

---

Le pipeline des trois Z venait de lui donner la discipline nécessaire pour tracer chaque route.

---

Il écrivit :

**ROUTE IDENTITY.**

---

Puis :

**FROM RADIX.**

**TO RADIX.**

---

Il s’arrêta.

---

La prochaine expérience serait beaucoup plus grande.

---

Mais maintenant il savait comment la construire.

---

Une route ne serait jamais seulement une flèche.

Elle aurait :

une source,

une destination,

un codec,

une valeur,

un type,

une trace,

un test de retour.

---

Brutus sauvegarda la configuration des trois Z.

Puis écrivit une dernière phrase :

**TROIS MACHINES DANS UNE SALLE NE FONT PAS UNE INTELLIGENCE.**

**MAIS TROIS ÉTAPES BIEN SÉPARÉES PEUVENT FAIRE UNE EXPÉRIENCE BEAUCOUP PLUS DIFFICILE À TROMPER.**

---

Les trois fenêtres restèrent ouvertes.

Z1.

Z2.

Z3.

---

Un dernier paquet traversa.

Gauche.

Centre.

Droite.

---

PASS.

---

Puis silence.

---

Brutus ouvrit une grille vide de douze colonnes par douze lignes.

Cent quarante-quatre cases.

---

Il posa le curseur sur la première.

---

Le prochain voyage n’aurait plus seulement trois étapes.

Il aurait **cent quarante-quatre chemins possibles**.
