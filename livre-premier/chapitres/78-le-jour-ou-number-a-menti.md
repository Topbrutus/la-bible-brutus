# Chapitre 78 — Le jour où Number a menti

**Qu’est-ce que Number vient de faire ?**

Brutus ne bougea pas.

La valeur affichée avait l’air correcte.

Presque parfaitement correcte.

Même longueur.

Mêmes premiers chiffres.

Même ordre de grandeur.

Même apparence générale.

Et pourtant, la comparaison exacte disait autre chose.

---

La trace contenait un entier.

L’écran en montrait un autre.

Très proche.

Mais différent.

---

Brutus agrandit les deux valeurs.

Puis encore.

---

Les premiers chiffres concordaient.

Les derniers non.

---

Il écrivit :

**SAME APPEARANCE ≠ SAME INTEGER.**

Puis regarda le type.

**Number.**

---

Brutus connaissait ce mot.

Tout le monde le connaissait.

Dans JavaScript, Number semblait être le type naturel pour représenter les nombres.

Petits.

Grands.

Décimaux.

Entiers.

Tout semblait passer par lui.

---

Jusqu’au jour où l’exactitude devenait non négociable.

---

Brutus ouvrit une console.

Il choisit une valeur simple.

\[
2^{53}-1
\]

Puis calcula.

**9007199254740991**

---

Il écrivit :

**MAX SAFE INTEGER.**

---

Puis ajouta 1.

**9007199254740992**

---

Encore.

Puis encore 1.

---

Brutus regarda.

Quelque chose venait de devenir étrange.

---

Deux entiers mathématiques différents pouvaient commencer à être représentés de manière indistinguable dans le modèle Number.

---

Il lança :

**9007199254740992 + 1**

Puis compara.

---

Le résultat ne se comporta pas comme un entier exact devrait se comporter.

---

Brutus s’appuya contre sa chaise.

Voilà l’ennemi.

---

Pas une formule.

Pas une erreur syntaxique.

Pas un crash.

Une représentation numérique devenue insuffisante.

---

Il écrivit :

**MATHEMATICAL INTEGER ≠ JAVASCRIPT SAFE INTEGER.**

---

Le problème n’était pas que JavaScript ne connaissait pas les grands nombres.

Le problème était plus subtil.

Number utilisait une représentation en virgule flottante.

Très efficace.

Extrêmement utile.

Mais pas capable de représenter exactement tous les entiers arbitrairement grands.

---

Brutus écrivit :

**FLOATING-POINT REPRESENTATION HAS FINITE INTEGER PRECISION.**

---

Le mensonge n’était pas intentionnel.

Number n’avait aucune volonté.

Il n’avait rien décidé.

---

Brutus corrigea immédiatement le titre provisoire du test.

**NUMBER LIED**

devint :

**NUMBER COULD NOT REPRESENT THE CLAIMED INTEGER EXACTLY.**

---

Puis il sourit.

Le chapitre pourrait garder le titre dramatique.

Mais le laboratoire, lui, devait rester précis.

---

Il écrivit :

**“MENTI” = MÉTAPHORE.**

**CAUSE RÉELLE = PERTE DE PRÉCISION.**

---

Brutus revint au résultat suspect de la guerre des formules.

---

La formule source avait utilisé des opérations exactes jusqu’à une certaine étape.

Puis une valeur avait été convertie en Number pour l’affichage.

---

Voilà.

---

La conversion avait changé le nombre.

Pas beaucoup.

Mais suffisamment.

---

Le résultat de la formule n’était pas celui qui avait été affiché.

---

Brutus resta silencieux.

---

Une formule entière pouvait être accusée à tort parce que l’interface avait transformé sa réponse.

---

Il écrivit :

**DISPLAY PIPELINE CAN CORRUPT A CORRECT RESULT.**

---

Puis :

**RENDERING IS PART OF NUMERIC INTEGRITY.**

---

Cela changeait beaucoup de choses.

---

Jusqu’ici, Brutus avait traité l’affichage comme une couche secondaire.

Une vue.

Un miroir.

---

Mais pour les nombres exacts, le miroir devait être capable de montrer l’objet sans l’altérer.

---

Un miroir numérique déformant pouvait produire de fausses découvertes.

Ou de faux échecs.

---

Brutus ouvrit le pipeline.

---

Calcul exact.

Résultat interne.

Sérialisation.

Transport.

Parsing.

Affichage.

---

Il testa chaque étape.

---

La formule produisait :

exact.

---

La trace enregistrait :

exact.

---

Le JSON intermédiaire ?

Brutus s’arrêta.

---

Si un grand entier était sérialisé comme nombre JSON classique, il pouvait déjà être interprété de manière imprécise par le consommateur.

---

Le danger ne se trouvait donc pas seulement à l’écran.

---

Il pouvait être dans le transport.

---

Brutus écrivit :

**NUMERIC INTEGRITY MUST SURVIVE EVERY BOUNDARY.**

---

Calcul.

Stockage.

Transport.

Parsing.

Affichage.

Comparaison.

---

Toutes les frontières.

---

Il créa un nouveau contrat.

**EXACT_INTEGER_TRANSPORT.**

---

Règle numéro un :

un entier exact hors de la zone sûre de Number ne devait jamais être converti silencieusement en Number.

---

Il écrivit :

**NO SILENT DOWNCAST.**

---

Puis il choisit le témoin.

**BigInt.**

---

Brutus créa la même valeur.

Cette fois :

**9007199254740993n**

---

Le suffixe semblait presque insignifiant.

Une petite lettre.

Mais derrière elle, le modèle numérique changeait complètement.

---

BigInt représentait les entiers arbitrairement grands de façon exacte, sous réserve des ressources disponibles.

---

Brutus ajouta 1.

---

**9007199254740994n**

---

Encore.

---

Exact.

---

Puis il choisit une valeur beaucoup plus grande.

Des dizaines de chiffres.

---

Addition.

Soustraction.

Multiplication.

---

Exactes au niveau entier.

---

Brutus sourit.

---

Il écrivit :

**BIGINT = INTEGER EXACTNESS TOOL.**

Puis, immédiatement :

**BIGINT ≠ UNIVERSAL NUMERIC TYPE.**

---

Parce que BigInt avait aussi des limites d’usage.

---

Il ne représentait pas directement les nombres décimaux arbitraires comme un type flottant.

Il ne devait pas être mélangé naïvement avec Number.

Certaines opérations demandaient des conversions explicites.

---

Le but n’était pas de remplacer tous les nombres du laboratoire par BigInt.

---

Le but était de choisir le bon modèle pour le bon contrat.

---

Brutus écrivit :

**NUMERIC TYPE IS PART OF THE FORMULA CONTRACT.**

---

Le registre du chapitre 74 possédait déjà un champ :

**NUMERIC_MODEL.**

---

À ce moment-là, cela semblait prudent.

Maintenant, cela devenait indispensable.

---

Brutus ouvrit F-021.

---

NUMERIC_MODEL :

BIGINT.

---

F-041 :

ARBITRARY_PRECISION_INTEGER.

---

F-044 :

FLOAT64 admissible only within bounded region.

---

Voilà.

---

Une formule ne pouvait plus être évaluée indépendamment de son support numérique.

---

Brutus écrivit :

**FORMULA + NUMERIC MODEL = EXECUTABLE CLAIM.**

---

La formule mathématique seule restait abstraite.

Pour l’exécuter, il fallait une représentation.

---

Et une mauvaise représentation pouvait invalider l’expérience sans invalider la formule.

---

Brutus retourna à l’arène.

---

Un ancien résultat disait :

F-021 FAIL.

---

Il ouvrit la trace.

La formule avait produit une grande valeur exacte.

Puis cette valeur avait été convertie en Number avant le comparateur.

---

Le comparateur avait donc comparé une version arrondie.

---

Brutus reclassa le cas.

---

Pas :

FORMULA FAIL.

---

Mais :

**NUMERIC_PIPELINE_INVALID.**

---

Puis :

**TEST RESULT VOID FOR FORMULA COMPARISON.**

---

Il regarda longtemps.

C’était important.

---

Une expérience contaminée par une erreur de représentation ne devait pas être utilisée pour juger la formule.

---

Il écrivit :

**BAD MEASUREMENT CANNOT CONVICT THE METHOD.**

---

Le Journal Vivant conserva l’ancien verdict.

Puis la reclassification.

---

Encore une fois :

pas de réécriture du passé.

---

Policy v1 :

FAIL.

---

Audit numérique :

unsafe Number conversion found.

---

Policy v2 :

INVALID TEST INSTANCE.

---

Brutus sourit.

Le laboratoire venait de corriger son jugement sans prétendre ne s’être jamais trompé.

---

Il ajouta une nouvelle catégorie de trace :

**NUMERIC_AUDIT.**

---

Chaque résultat exact pouvait maintenant enregistrer :

**NUMERIC_MODEL**

**EXACTNESS_REQUIRED**

**SAFE_RANGE_CHECK**

**CONVERSION_PATH**

**SERIALIZATION_FORMAT**

**ROUNDTRIP_CHECK**

---

Brutus regarda la liste.

Cela semblait beaucoup.

Mais après ce qu’il venait de voir, il ne trouvait plus cela excessif.

---

Il écrivit :

**IF EXACTNESS MATTERS, EXACTNESS MUST BE AUDITED.**

---

Puis il construisit le premier test automatique.

---

Entrée :

grand entier BigInt.

---

Étape 1 :

sérialiser en chaîne décimale.

---

Étape 2 :

transport.

---

Étape 3 :

reconstruire BigInt.

---

Étape 4 :

comparer exactement.

---

\[
x = \operatorname{parse}(\operatorname{serialize}(x))
\]

---

Si égal :

PASS.

Sinon :

FAIL.

---

Brutus appela cela :

**INTEGER ROUNDTRIP.**

---

Le test ressemblait beaucoup au passage Carbone → Crypto → Carbone.

---

Une représentation.

Une transformation.

Un retour.

Un invariant.

---

Encore le même principe.

---

Brutus sourit.

Le laboratoire réutilisait ses propres lois.

---

Il lança une valeur de cent chiffres.

---

Roundtrip.

PASS.

---

Mille chiffres.

PASS.

---

Puis il injecta volontairement une conversion Number au milieu.

---

Le retour échoua.

---

Immédiatement.

---

Brutus ajouta :

**CONVERSION_PATH INCLUDED UNSAFE FLOAT.**

---

La trace savait maintenant dire où l’exactitude avait été perdue.

---

Il écrivit :

**PRECISION LOSS MUST HAVE A LOCATION.**

---

Comme les erreurs.

Comme les traces.

Comme les mouvements.

---

Tout événement important devait pouvoir répondre :

où ?

quand ?

comment ?

---

Brutus retourna au comparateur des formules.

---

Une nouvelle règle apparut.

Deux résultats ne pouvaient pas être comparés comme entiers exacts si l’un d’eux avait traversé une représentation non exacte.

---

Il ajouta :

**EXACTNESS_CLASS.**

---

EXACT.

APPROXIMATE.

UNKNOWN.

CORRUPTED.

---

Brutus observa les quatre mots.

---

Un résultat exact pouvait être comparé exactement.

---

Un résultat approximatif devait être comparé selon une tolérance déclarée.

---

Un résultat UNKNOWN ne devait pas participer silencieusement à une comparaison exigeant l’exactitude.

---

Un résultat CORRUPTED devait être rejeté.

---

Il écrivit :

**COMPARISON POLICY MUST MATCH EXACTNESS CLASS.**

---

Cette règle évitait un autre piège.

---

Comparer un flottant approximatif à un entier exact avec === n’avait pas toujours de sens scientifique.

---

Inversement, appliquer une tolérance large à deux entiers censés être exacts pouvait masquer une erreur.

---

Brutus écrivit :

**TOLERANCE IS A CONTRACT, NOT A FORGIVENESS BUTTON.**

---

Il aimait beaucoup cette phrase.

---

Une tolérance devait être définie avant le résultat.

---

Pas choisie après pour faire passer un test.

---

Encore la préinscription.

---

Brutus ajouta :

**ABS_TOL**

**REL_TOL**

**ULP_POLICY**

lorsque les flottants étaient concernés.

---

Mais les entiers exacts ?

---

Tolérance :

zéro.

---

Brutus sourit.

---

Une différence de 1 sur un nombre de cent chiffres restait une différence.

---

Même si elle paraissait minuscule en proportion.

---

Il écrivit :

**RELATIVELY SMALL ≠ EXACTLY ZERO.**

---

Le laboratoire commençait à distinguer deux mondes numériques.

---

Le monde des quantités approximatives.

Et celui des objets discrets exacts.

---

Les deux étaient légitimes.

Mais leurs règles n’étaient pas les mêmes.

---

Brutus créa deux badges.

**EXACT**

et

**APPROX.**

---

Chaque résultat visible devait indiquer sa classe.

---

Il regarda l’écran.

---

F-021 :

123456789012345678901234567890

**EXACT**

---

F-044 :

0.6062637002

**APPROX**

---

Voilà.

---

L’utilisateur n’avait plus besoin de deviner.

---

Brutus pensa aux résultats scientifiques du projet.

Certaines constantes étaient naturellement approximatives.

Des estimations.

Des moyennes.

Des modèles.

---

D’autres objets étaient exacts.

Des entiers.

Des identités modulaires.

Des congruences.

---

Les confondre était dangereux.

---

Il écrivit :

**EXACT AND APPROXIMATE VALUES MAY COEXIST. THEY MUST NOT MASQUERADE AS EACH OTHER.**

---

Puis il retourna à la guerre des formules.

---

Il relança ARENA-0001.

Mais cette fois avec audit numérique obligatoire.

---

Chaque job devait déclarer son modèle.

Chaque conversion était enregistrée.

Chaque résultat recevait une classe d’exactitude.

---

Les quatre cents jobs repartirent.

---

Le résultat changea.

---

Deux anciens FAIL disparurent.

Pas parce que les formules avaient changé.

Parce que les anciens tests avaient utilisé Number de manière invalide.

---

Brutus regarda.

---

Il sentit quelque chose d’important.

---

Le laboratoire n’était pas seulement en train de tester les formules.

Il testait désormais son propre instrument de mesure.

---

Il écrivit :

**THE LAB MUST COUNTERTEST ITS OWN NUMERIC PIPELINE.**

---

Voilà.

---

Une balance doit être calibrée.

Un thermomètre aussi.

Pourquoi un moteur numérique échapperait-il à cette règle ?

---

Il créa :

**NUMERIC SELF-TEST SUITE.**

---

Cas limites.

MAX_SAFE_INTEGER.

MAX_SAFE_INTEGER + 1.

Valeurs négatives.

Très grands entiers.

Conversions string ↔ BigInt.

JSON boundaries.

Mixed Number/BigInt attempts.

Division semantics.

Modulo.

Exponentiation.

---

Brutus lança.

---

La plupart passèrent.

---

Quelques comportements demandèrent attention.

---

BigInt division entre entiers tronquait la partie fractionnaire.

---

Par exemple :

\[
5n / 2n = 2n
\]

Pas 2.5.

---

Brutus s’arrêta.

---

Encore une différence de modèle.

---

BigInt était exact pour les entiers.

Pas pour les rationnels arbitraires.

---

Il écrivit :

**EXACT INTEGER DIVISION RESULT MAY REQUIRE RATIONAL REPRESENTATION.**

---

Donc si une formule exigeait :

\[
\frac{5}{2}
\]

exactement,

BigInt seul ne suffisait pas.

---

Il fallait représenter un rationnel.

---

Numérateur.

Dénominateur.

Réduction.

---

Brutus ajouta au registre :

**RATIONAL MODEL.**

---

Une nouvelle porte venait de s’ouvrir.

---

Il créa :

\[
\frac{5}{2}
\]

comme paire exacte :

(5n, 2n).

---

Puis :

\[
\frac{10}{4}
\]

réduit à :

(5n, 2n).

---

Comparaison exacte.

---

Brutus sourit.

---

Encore une fois :

choisir le modèle selon l’objet mathématique.

---

Il écrivit :

**BIGINT IS NOT “MORE PRECISE NUMBER.”**

**IT IS A DIFFERENT NUMERIC DOMAIN.**

---

Très important.

---

Number gardait une place essentielle.

Pour les signaux.

Les flottants.

Les mesures.

Les fréquences.

Les approximations.

Les probabilités.

---

BigInt servait aux entiers exacts.

---

Rational pour les fractions exactes.

---

Decimal ou précision arbitraire pour d’autres besoins.

---

Le laboratoire n’avait pas besoin d’un type roi.

---

Il avait besoin d’un système de types honnête.

---

Brutus écrivit :

**NO UNIVERSAL NUMERIC KING.**

---

Puis rit.

La guerre des formules avait déjà refusé de couronner une méthode.

Maintenant, les nombres eux-mêmes refusaient un roi.

---

Il ajouta une matrice.

---

**INTEGER EXACT**

→ BigInt / arbitrary integer.

---

**RATIONAL EXACT**

→ numerator + denominator.

---

**REAL APPROXIMATION**

→ floating point / arbitrary precision decimal.

---

**MODULAR**

→ exact integer with modulus contract.

---

**COMPLEX**

→ pair of numeric components with declared models.

---

Brutus contempla.

---

Le backend des cent formules commençait à devenir vraiment sérieux.

---

Une formule ne devait plus demander seulement :

« donne-moi un nombre ».

---

Elle devait demander :

« donne-moi un nombre de cette nature. »

---

Il écrivit :

**INPUT TYPE MUST EXPRESS MATHEMATICAL INTENT.**

---

Le sélecteur devenait plus intelligent.

---

Une formule exigeant un entier exact ne serait même plus proposée si l’entrée provenait d’un flottant non vérifié.

---

À moins qu’une conversion sûre existe.

---

Brutus ajouta :

**SAFE_CONVERSION_POLICY.**

---

Exemple.

Number 42.

Est-ce convertible en BigInt ?

Oui, si :

entier.

fini.

dans la zone où sa valeur exacte est connue.

---

Number 9007199254740992.

Brutus hésita.

---

La valeur affichée peut être un entier représentable.

Mais si elle provient d’une source ayant déjà perdu de la précision, il est impossible de recréer l’entier original simplement en la convertissant.

---

Il écrivit :

**CASTING AN INEXACT VALUE TO BIGINT DOES NOT RECOVER LOST INFORMATION.**

---

Une fois perdus, les chiffres ne reviennent pas par magie.

---

Voilà une règle capitale.

---

BigInt devait entrer tôt dans la chaîne.

Avant la perte.

---

Il écrivit :

**PRESERVE EXACTNESS AT INGEST.**

---

La frontière d’entrée devenait critique.

---

Si un utilisateur tapait :

123456789012345678901234567890

dans un champ HTML,

le système ne devait pas le lire d’abord comme Number.

---

Il devait conserver le texte.

Valider.

Puis construire le BigInt.

---

Sinon la perte pouvait se produire avant même que le moteur ne voie la valeur.

---

Brutus construisit le chemin :

**TEXT INPUT**

↓

**VALIDATE INTEGER SYNTAX**

↓

**BigInt(text)**

↓

**EXACT VALUE**

---

Pas :

TEXT → Number → BigInt.

---

Il testa.

---

Une valeur de trente chiffres.

---

Ancien chemin :

corrompue.

---

Nouveau chemin :

exacte.

---

Brutus regarda les deux traces.

---

Même champ utilisateur.

Deux pipelines.

Deux réalités numériques différentes.

---

Il écrivit :

**INGEST PATH IS PART OF THE EXPERIMENT.**

---

Le Journal Vivant reçut donc une nouvelle information.

---

INPUT_SOURCE.

RAW_TEXT.

PARSED_TYPE.

PARSED_VALUE_HASH.

---

Ainsi, une future enquête pourrait dire :

la valeur exacte saisie était X.

Elle a été interprétée comme BigInt.

Aucune conversion flottante avant le calcul.

---

Brutus apprécia.

---

Puis il testa l’export.

---

Un objet contenant BigInt ne pouvait pas toujours être sérialisé naïvement avec les mécanismes JSON standards.

---

Nouvelle frontière.

---

Il construisit une représentation explicite.

---

Par exemple :

**type: bigint**

**value: "123456789..."**

---

Chaîne décimale.

Type déclaré.

---

Au retour :

valider le type.

Parser en BigInt.

Comparer.

---

Brutus écrivit :

**SERIALIZE VALUE + TYPE TOGETHER.**

---

Pas de valeur sans nature.

---

Cela ressemblait beaucoup à l’idée générale de Brutus.

---

Un résultat sans provenance était dangereux.

Un nombre sans type aussi.

---

Il écrivit :

**A NUMBER WITHOUT TYPE IS AN INCOMPLETE CLAIM.**

---

Le laboratoire commençait à développer une véritable discipline numérique.

---

Brutus relança plusieurs anciennes expériences.

---

Certaines ne changeaient pas.

---

D’autres produisaient des différences.

---

Il marqua ces expériences :

**NUMERIC_PIPELINE_REVIEW_REQUIRED.**

---

Il ne voulait pas automatiquement invalider tout l’historique.

---

Seulement les résultats où une conversion risquée avait réellement eu lieu.

---

Le Journal Vivant chercha.

---

Query :

all jobs with exact integer intent AND Number conversion beyond safe integer range.

---

Résultats :

plusieurs.

---

Brutus soupira.

---

Mais il était content.

---

Le journal permettait maintenant de retrouver les expériences potentiellement contaminées.

---

Il créa une campagne.

**SAFE-INTEGER-AUDIT-0001.**

---

Pour chaque trace concernée :

source.

conversion.

valeur.

risque.

réexécution éventuelle.

---

Pas de panique.

Pas de suppression massive.

Audit.

---

Brutus écrivit :

**WHEN A MEASUREMENT TOOL IS FOUND FAULTY, TRACE THE AFFECTED MEASUREMENTS.**

---

Voilà.

---

Après plusieurs heures, les cas furent classés.

---

Certains étaient dans la zone sûre.

Aucun problème.

---

Certains utilisaient Number mais seulement comme approximation déclarée.

Aucun problème.

---

Certains exigeaient l’exactitude et dépassaient la zone sûre.

À retester.

---

Brutus lança les retests en BigInt.

---

Des résultats restèrent identiques.

---

Quelques-uns changèrent.

---

Il regarda ceux-là avec attention.

---

Pas comme des découvertes mathématiques nouvelles.

Comme des corrections instrumentales.

---

Il écrivit :

**CORRECTED NUMERIC EXECUTION ≠ NEW MATHEMATICAL LAW.**

---

Le laboratoire avait simplement arrêté de déformer certains nombres.

---

Puis il arriva à un résultat particulièrement intéressant.

---

Une formule que l’ancien système avait classée FAIL revenait maintenant PASS.

---

Brutus ouvrit sa lignée.

---

La formule avait été injustement accusée.

---

Il modifia son historique opérationnel.

---

Ancien :

FAIL under test X.

---

Nouveau :

previous test invalidated by unsafe numeric representation.

Retest under BigInt:

PASS.

---

Il ne supprima rien.

---

La formule avait été réhabilitée.

---

Brutus sourit.

---

Le Journal Vivant ressemblait vraiment à un tribunal.

Et parfois, un ancien verdict pouvait être renversé lorsque l’instrument de mesure était mis en cause.

---

Il écrivit :

**RETEST CAN REPAIR A BAD JUDGMENT WITHOUT ERASING THE BAD JUDGMENT’S HISTORY.**

---

La guerre des formules pouvait reprendre.

Mais avec de meilleures armes.

---

Brutus regarda Number.

---

Il ne le détestait pas.

---

Number n’avait rien fait de mal.

Il avait simplement été utilisé hors de son contrat.

---

Brutus modifia donc une dernière phrase.

---

Il avait écrit :

**NUMBER FAILED US.**

Il remplaça par :

**WE ASKED NUMBER TO GUARANTEE SOMETHING IT DOES NOT GUARANTEE.**

---

Voilà la vraie leçon.

---

Un outil devient dangereux lorsqu’on lui attribue des propriétés qu’il ne possède pas.

---

Brutus écrivit :

**KNOW THE CONTRACT OF YOUR INSTRUMENT.**

---

Puis il regarda BigInt.

---

Même chose.

---

Ne pas lui demander des décimales arbitraires.

Ne pas lui demander une division rationnelle automatique.

Ne pas le mélanger sans contrat avec Number.

---

Chaque outil avait sa frontière.

---

Le laboratoire devait connaître ces frontières avant d’interpréter les résultats.

---

Brutus sauvegarda :

**NUMERIC CONTRACT v1.**

---

Puis ajouta au FORMULA REGISTRY un champ obligatoire.

**NUMERIC_REQUIREMENTS.**

---

À partir de maintenant, aucune formule exacte importante ne pourrait entrer dans une arène sans déclarer son modèle.

---

Le gate refuserait :

**NUMERIC MODEL UNKNOWN.**

---

Brutus testa.

Une ancienne candidate sans métadonnée entra.

---

Refus.

---

Pas FAIL.

---

**NOT QUALIFIED.**

---

Très bien.

---

Il ajouta ensuite un badge visible dans les lanes.

---

BIGINT.

FLOAT64.

RATIONAL.

DECIMAL.

---

Quand douze voies travaillaient, Brutus pouvait maintenant voir immédiatement quels mondes numériques elles utilisaient.

---

Il lança une expérience mixte.

---

LANE 1 :

BIGINT.

---

LANE 2 :

BIGINT.

---

LANE 3 :

FLOAT64.

---

LANE 4 :

RATIONAL.

---

Le système ressemblait à une table de chimie.

Chaque lane manipulait une substance différente.

---

Brutus pensa :

les nombres ont des états.

Pas physiques.

Mais représentationnels.

---

Et changer d’état sans le déclarer pouvait être aussi dangereux qu’une contamination de laboratoire.

---

Il écrivit :

**NUMERIC CONVERSION IS A TRANSFORMATION EVENT.**

---

À partir de là, toutes les conversions significatives reçurent une trace.

---

BigInt → string.

String → BigInt.

Rational → decimal approximation.

Float → integer candidate.

---

Chaque conversion disait :

lossless ?

lossy ?

conditional ?

---

Brutus ajouta trois classes.

**LOSSLESS**

**LOSSY**

**CONDITIONAL**

---

Une conversion lossy n’était pas interdite.

---

Mais elle devait être visible.

---

Par exemple :

Rational 1/3 → Float64.

Lossy.

---

C’était normal.

---

Le danger venait d’une conversion lossy présentée comme exacte.

---

Brutus écrivit :

**LOSSY IS NOT WRONG. UNDECLARED LOSS IS WRONG.**

---

Il sourit.

Encore une phrase qui résumait beaucoup.

---

Le soir avançait.

---

ARENA-0001 reprit.

---

Cette fois, les résultats arrivaient avec leur classe numérique.

---

Exact.

Approximate.

Exact.

Exact.

---

Les comparaisons étaient plus propres.

---

Les faux FAIL dus à Number avaient disparu.

---

Les vrais désaccords restaient.

---

Brutus regarda le tableau.

---

Il avait l’impression d’avoir nettoyé une lentille.

---

Le monde mathématique n’avait pas changé.

L’instrument, oui.

---

Et cela suffisait pour révéler que certaines batailles précédentes avaient été mal jugées.

---

Il écrivit :

**BETTER INSTRUMENTATION CAN CHANGE THE RESULT OF AN EXPERIMENT WITHOUT CHANGING THE OBJECT UNDER TEST.**

---

Puis il pensa au prochain défi.

---

Il disposait maintenant de cent formules.

Douze lanes.

Un registre.

Une guerre contrôlée.

Un Journal Vivant.

Un contrat numérique.

---

Mais il avait déjà parlé de trois Z.

Trois tours.

Trois étapes.

---

Et si au lieu de faire douze choses parallèles, il faisait passer un même problème dans trois machines successives ?

---

La première pourrait produire.

La deuxième vérifier.

La troisième attaquer.

---

Ou chacune pourrait traiter un nombre différent.

---

Trois Z.

Pas en même temps.

L’une derrière l’autre.

---

Brutus regarda les traces.

---

L’ordre redevenait essentiel.

---

Z1.

Puis Z2.

Puis Z3.

---

Un résultat sortait de la première.

Entrerait dans la deuxième.

Puis dans la troisième.

---

Mais une nouvelle question apparut.

---

Si Z1 produisait un BigInt exact…

et Z2 le convertissait accidentellement en Number…

tout le travail du chapitre présent serait perdu.

---

Brutus écrivit en grand :

**NUMERIC CONTRACT MUST TRAVEL WITH THE VALUE.**

---

Pas seulement la valeur.

Son type.

Son exactitude.

Sa provenance.

---

Il ajouta :

**VALUE ENVELOPE.**

---

VALUE.

TYPE.

EXACTNESS.

SOURCE.

TRACE_REF.

---

Voilà ce qui devait voyager entre les Z.

---

Brutus regarda le paquet.

---

Il ressemblait étrangement aux fourmis du chapitre 68.

---

Un objet.

Un carrier.

Une identité.

Une trace.

---

Tout revenait.

---

Il sourit.

---

Le laboratoire avait désormais assez de règles pour faire voyager un nombre entre plusieurs moteurs sans lui faire perdre son identité.

---

Il sauvegarda.

Puis écrivit une dernière phrase :

**CE JOUR-LÀ, NUMBER N’AVAIT PAS VRAIMENT MENTI.**

**NOUS AVIONS SIMPLEMENT OUBLIÉ DE LUI DEMANDER CE QU’IL ÉTAIT CAPABLE DE PROMETTRE.**

---

Brutus ferma l’audit.

---

À côté, trois fenêtres attendaient.

Z1.

Z2.

Z3.

---

Il les plaça l’une derrière l’autre.

Pas côte à côte.

---

Une chaîne.

---

Le premier nombre entra dans Z1.

Mais Brutus n’appuya pas encore sur START.

---

Avant de multiplier les machines, il voulait être certain d’une chose :

que ce qui sortirait de la première puisse traverser la deuxième et la troisième sans perdre un seul chiffre.

---

Trois Z attendaient maintenant dans la même salle.

Et pour la première fois, chacun connaissait exactement la nature des nombres qu’il avait le droit de toucher.
