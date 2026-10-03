# Chapitre 80 — Cent quarante-quatre chemins de 78 à 2

Cent quarante-quatre cases.

Brutus resta devant la grille.

Douze colonnes.

Douze lignes.

\[
12\times12=144
\]

Rien de mystérieux.

Une simple multiplication.

Mais derrière chacune des cases pouvait exister un chemin différent.

Une représentation d’entrée.

Une représentation de sortie.

Et entre les deux :

une responsabilité.

---

Brutus choisit douze bases numériques.

Il aurait pu prendre n’importe lesquelles.

Mais il voulait un ensemble assez large pour faire travailler la machine.

---

Base 2.

Base 3.

Base 4.

Base 5.

Base 6.

Base 7.

Base 8.

Base 9.

Base 10.

Base 11.

Base 12.

Base 13.

---

Douze représentations.

---

Chacune pouvait convertir vers les onze autres.

Et vers elle-même.

---

Douze sources.

Douze destinations.

---

Cent quarante-quatre routes.

---

Brutus écrivit :

**RADIX MATRIX 12×12.**

---

La première case était simple.

Base 2 vers base 2.

---

Une identité.

---

La suivante :

base 2 vers base 3.

Puis :

base 2 vers base 4.

---

Jusqu’à base 13.

---

Deuxième ligne :

base 3 vers base 2.

Base 3 vers base 3.

Et ainsi de suite.

---

Le système ne devait pas considérer les chemins symétriques comme identiques.

---

2 → 7

et

7 → 2

utilisaient peut-être des composants similaires.

Mais ce n’étaient pas le même événement.

---

Brutus écrivit :

**A→B ≠ B→A.**

---

Même lorsque les deux conversions étaient parfaitement réversibles.

---

Le sens faisait partie de l’identité du trajet.

---

Il donna donc un identifiant aux routes.

---

**RADIX-2-TO-2**

**RADIX-2-TO-3**

**RADIX-2-TO-4**

…

**RADIX-13-TO-13**

---

Chaque case possédait :

**ROUTE_ID**

**FROM_RADIX**

**TO_RADIX**

**CODEC_VERSION**

**VALUE_ID**

**TRACE_REF**

**ROUNDTRIP_POLICY**

---

Brutus sourit.

La grille ressemblait déjà beaucoup moins à un dessin.

---

Elle devenait un registre.

---

Il choisit une valeur.

Pas trop grande pour commencer.

Le nombre décimal :

\[
78
\]

---

Brutus le regarda.

Le titre du prochain test lui vint immédiatement.

**78 → 2.**

---

Pas soixante-dix-huit chemins vers deux.

Pas un symbole caché.

Simplement :

la valeur décimale 78 représentée en base 2.

---

Il écrivit :

\[
78_{10}=1001110_2
\]

---

Puis vérifia.

\[
64+8+4+2=78
\]

Exact.

---

Brutus choisit cette conversion comme premier chemin de référence.

---

**ROUTE_ID: RADIX-10-TO-2**

Input:

78

Source radix:

10.

Output:

1001110

Destination radix:

2.

---

PASS.

---

Mais il ne voulait pas seulement voir le bon texte.

Il voulait savoir si la valeur abstraite avait été conservée.

---

Il écrivit :

**REPRESENTATION CHANGES. VALUE MUST NOT.**

---

Voilà le contrat.

---

Le texte 78 n’était pas la même chaîne que 1001110.

Mais ils pouvaient représenter le même entier.

---

Brutus ajouta donc une couche.

**CANONICAL VALUE.**

---

Input representation:

78.

Decoded canonical value:

78n.

---

Output representation:

1001110.

Decoded canonical value:

78n.

---

Comparaison :

\[
78n = 78n
\]

---

PASS.

---

Brutus sourit.

C’était beaucoup plus solide.

---

Une conversion de base ne devait pas être jugée par l’apparence.

Elle devait être jugée par la valeur canonique.

---

Il écrivit :

**STRING EQUALITY IS NOT VALUE EQUALITY.**

---

Deux chaînes différentes pouvaient représenter la même valeur.

Et deux chaînes identiques pouvaient représenter des valeurs différentes si leur base différait.

---

10 en base 2.

Deux.

---

10 en base 10.

Dix.

---

10 en base 13.

Treize.

---

Brutus écrivit :

**DIGITS WITHOUT RADIX ARE INCOMPLETE DATA.**

---

Il ajouta donc une enveloppe.

---

**RADIX_VALUE**

**DIGITS**

**RADIX**

**SIGN**

**CANONICAL_INTEGER_REF**

**VALIDATION_STATE**

---

Pas de nombre de base sans sa base.

---

Puis Brutus choisit la première ligne entière.

Base 2 vers toutes les autres.

---

Il prit :

\[
1001110_2
\]

Canonical:

78.

---

Vers base 3.

---

\[
78=2\times27+2\times9+2\times3+0
\]

Donc :

\[
78_{10}=2220_3
\]

---

Vers base 6.

\[
78=2\times36+1\times6+0
\]

Donc :

\[
210_6
\]

---

Vers base 13.

\[
78=6\times13
\]

Donc :

\[
60_{13}
\]

---

Les représentations changeaient énormément.

La valeur restait.

---

Brutus lança la ligne complète.

---

Douze conversions.

---

Douze retours vers la valeur canonique.

---

PASS.

---

Il écrivit :

**ONE VALUE. TWELVE REPRESENTATIONS.**

---

Puis il remplit la deuxième ligne.

---

Puis la troisième.

---

Très vite, le laboratoire exécutait les 144 routes.

---

Mais un nouveau problème apparut.

---

Certains digits n’existaient pas dans certaines bases.

---

Par exemple, le symbole 8 était invalide en base 8.

Le symbole 9 invalide en base 9.

---

Brutus injecta :

78

comme texte en base 7.

---

Le parseur devait refuser.

---

Il refusa.

---

Brutus écrivit :

**INVALID DIGIT ≠ NUMERIC FAILURE.**

---

C’était un problème de représentation.

---

Il créa l’état :

**RADIX_SYNTAX_REJECTED.**

---

Ainsi, la machine ne dirait pas que « le calcul est faux ».

Elle dirait :

la chaîne donnée ne constitue pas un entier valide dans cette base.

---

Brutus ajouta :

**VALID DIGITS MUST SATISFY DIGIT < RADIX.**

---

Simple.

Fondamental.

---

Il pensa ensuite aux bases supérieures à 10.

---

Base 11.

Base 12.

Base 13.

---

Il fallait représenter les digits 10, 11 et 12.

---

A.

B.

C.

---

Brutus choisit :

A = 10.

B = 11.

C = 12.

---

Mais il écrivit immédiatement :

**DIGIT ALPHABET IS PART OF THE CODEC CONTRACT.**

---

Car un autre système pouvait choisir des symboles différents.

---

Une chaîne comme 1A n’avait de sens que si le codec savait que A représentait dix.

---

Il ajouta :

**DIGIT_ALPHABET_VERSION.**

---

La machine était prête.

---

Brutus relança 78.

---

En base 11 :

\[
78=7\times11+1
\]

Donc :

\[
71_{11}
\]

---

En base 12 :

\[
66_{12}
\]

---

En base 13 :

\[
60_{13}
\]

---

Toutes les routes convergaient vers la même valeur canonique.

---

Brutus regarda la grille.

---

La même valeur apparaissait sous douze formes.

---

1001110

2220

1032

303

210

141

116

86

78

71

66

60

---

Brutus sourit.

---

Ce n’était pas douze nombres différents.

C’étaient douze écritures du même entier.

---

Il écrivit :

**REPRESENTATION DIVERSITY ≠ VALUE DIVERSITY.**

---

Puis il fit le contraire.

---

Il choisit la même chaîne :

100

---

Dans plusieurs bases.

---

Base 2 :

4.

---

Base 3 :

9.

---

Base 10 :

100.

---

Base 13 :

169.

---

Même chaîne.

Valeurs différentes.

---

Il écrivit :

**TEXT IDENTITY ≠ NUMERIC IDENTITY.**

---

Encore une frontière.

---

Brutus comprit que la grille 12×12 pouvait devenir un excellent banc de test pour la discipline numérique.

---

Chaque route pouvait effectuer :

decode source.

canonicalize.

encode destination.

decode destination.

compare canonical values.

---

Il écrivit la chaîne :

**SOURCE STRING**

↓

**SOURCE DECODE**

↓

**CANONICAL INTEGER**

↓

**DESTINATION ENCODE**

↓

**DESTINATION DECODE**

↓

**CANONICAL COMPARE**

---

Une conversion correcte devait satisfaire :

\[
D_b(E_b(n))=n
\]

pour la destination \(b\).

---

Et, pour un trajet complet entre bases \(a\) et \(b\) :

\[
D_b(E_b(D_a(s)))=D_a(s)
\]

lorsque la chaîne source \(s\) était valide en base \(a\).

---

Brutus contempla l’expression.

---

Voilà le vrai contrat des 144 chemins.

---

Pas la beauté de la grille.

Pas la symétrie.

La conservation de la valeur.

---

Il écrivit :

**RADIX CONVERSION IS REPRESENTATION TRANSPORT.**

---

Le mot transport revenait encore.

---

La fourmi transportait une référence.

Le pipeline Z transportait un Value Envelope.

Le codec transportait une valeur entre représentations.

---

Toujours la même idée.

---

Brutus lança une campagne.

---

Valeurs :

0.

1.

2.

7.

13.

78.

273.

637.

2401.

Puis plusieurs grands entiers.

---

Il choisit certains nombres utilisés ailleurs dans le laboratoire, mais sans leur attribuer une signification particulière ici.

---

Ils étaient simplement de bons cas de test.

---

Le système passa les premières valeurs.

---

Puis arriva un problème sur une valeur négative.

---

Le codec avait oublié le signe.

---

Input:

-78.

---

Output destination:

60.

---

Brutus arrêta.

---

La magnitude avait survécu.

Pas le nombre.

---

Il écrivit :

**MAGNITUDE PRESERVED ≠ VALUE PRESERVED.**

---

Le signe devait faire partie de l’enveloppe.

---

Il corrigea.

---

-78 en base 13 :

-60.

---

Roundtrip.

PASS.

---

Puis zéro.

---

Brutus testa -0.

---

Le système normalisait vers 0.

---

Il réfléchit.

---

Pour les entiers mathématiques exacts, -0 et 0 représentent la même valeur.

---

Mais la chaîne source pouvait néanmoins être différente.

---

Il décida de distinguer :

**LEXICAL IDENTITY**

et

**NUMERIC IDENTITY.**

---

-0 pouvait perdre son signe lors de la canonicalisation numérique sans que la valeur mathématique change.

---

Brutus écrivit :

**CANONICALIZATION MAY CHANGE SPELLING WITHOUT CHANGING VALUE.**

---

Le contrat devait dire si cela était accepté.

---

Pour la matrice de bases :

oui.

---

Le but était la valeur.

Pas la préservation bit-à-bit du texte.

---

Brutus ajouta :

**PRESERVATION_TARGET = NUMERIC_VALUE.**

---

Voilà.

---

Il testa ensuite les zéros en tête.

00078.

---

Vers base 2.

---

1001110.

---

Retour vers base 10.

---

78.

---

La chaîne n’était pas identique.

La valeur oui.

---

PASS.

---

Brutus écrivit :

**NORMALIZED ROUNDTRIP ≠ TEXT ROUNDTRIP.**

---

Encore une distinction.

---

Si un jour le laboratoire voulait préserver le texte exact, il faudrait un autre contrat.

---

Mais pas ici.

---

Il lança les 144 routes pour une grande valeur BigInt.

---

Cette fois, chaque codec devait utiliser l’entier exact.

---

Aucun passage par Number.

---

Le chapitre précédent avait laissé des traces profondes.

---

Brutus surveilla :

unsafe conversion.

Lossy cast.

Parser overflow.

Truncation.

---

Zéro.

---

Il sourit.

---

Les nombres pouvaient changer de base sans perdre un chiffre.

---

Puis il injecta volontairement Number sur une route.

---

Base 13 vers base 2.

---

Une grande valeur.

---

Le retour divergea.

---

La route passa rouge.

---

**NUMERIC_INTEGRITY_FAIL.**

---

Brutus regarda la grille.

Une seule case rouge au milieu de cent quarante-trois cases vertes.

---

Voilà une représentation utile.

---

Mais il écrivit :

**GREEN CELL = PASSED TEST SET. NOT UNIVERSAL PROOF.**

---

Toujours.

---

Une case verte signifiait seulement :

les tests définis ont passé pour cette route et cette version de codec.

---

Il ajouta un compteur de couverture.

---

RADIX-13-TO-2.

Cases tested:

10 000.

Failures:

0.

Coverage class:

sampled.

---

Pas :

**perfect.**

---

Brutus écrivit :

**ZERO OBSERVED FAILURES ≠ ZERO POSSIBLE FAILURES.**

---

Le laboratoire avait appris cette phrase sous plusieurs formes.

---

Puis Brutus eut une idée.

---

Au lieu de tester seulement les routes individuellement, il pouvait tester des cycles.

---

Base 2.

Vers base 7.

Vers base 13.

Vers base 3.

Retour base 2.

---

Si tous les codecs étaient corrects, la valeur canonique devait survivre.

---

Il créa :

**RADIX CYCLE.**

---

Route :

2 → 7 → 13 → 3 → 2.

---

VALUE-0007.

---

Brutus lança.

---

Chaque étape créait une nouvelle représentation.

---

Mais pas une nouvelle valeur abstraite.

---

À la fin :

canonical input = canonical output.

---

PASS.

---

Il écrivit :

**MULTI-HOP REPRESENTATION CHANGE MUST PRESERVE CANONICAL VALUE.**

---

Puis il augmenta.

---

Six hops.

Douze.

Vingt-quatre.

---

Toujours.

---

Mais quelque chose le dérangeait.

---

Une route pourrait contenir deux erreurs qui s’annulent.

---

Par exemple, un codec produit une mauvaise valeur.

Puis un autre fait une erreur inverse.

Le retour final pourrait être correct par accident.

---

Brutus écrivit :

**END-TO-END PASS CAN HIDE INTERMEDIATE FAILURE.**

---

Important.

---

Le test final seul ne suffisait pas.

---

Il fallait vérifier chaque hop.

---

Il ajouta :

**HOP_INVARIANT_CHECK.**

---

À chaque étape :

decode.

compare canonical.

Puis seulement continuer.

---

Ainsi, une corruption intermédiaire serait détectée immédiatement.

---

Il écrivit :

**VERIFY LOCALLY. VERIFY END-TO-END.**

---

Deux niveaux.

---

Le cycle fut relancé.

---

Tous les hops passèrent.

Puis le roundtrip global aussi.

---

Beaucoup mieux.

---

Brutus observa les 144 routes.

---

Une idée de tressage apparut.

---

Les douze bases étaient comme douze fils.

Chaque fil pouvait se connecter aux onze autres.

---

Un réseau dense.

---

Il nomma cette visualisation :

**RADIX BRAID.**

---

Mais il ajouta aussitôt :

**BRAID = VISUAL MODEL OF CONVERSION GRAPH.**

---

Pas une nouvelle structure mathématique fondamentale.

Pas un phénomène physique.

Simplement une manière utile de voir les chemins.

---

Brutus dessina les douze nœuds autour d’un cercle.

---

Chaque conversion possible devenait une arête dirigée.

---

Trop de lignes.

Illisible.

---

Il réduisit.

---

N’afficher que la route active.

---

Puis les routes testées.

---

Puis les routes en échec.

---

La grille 12×12 restait finalement beaucoup plus claire pour l’audit.

---

Le graphe était joli.

La matrice était utile.

---

Brutus écrivit :

**BEAUTY ≠ OPERABILITY.**

---

Il choisit encore une fois le cas 78 → 2.

---

Input:

78 radix 10.

---

Canonical:

78n.

---

Destination:

radix 2.

---

Output:

1001110.

---

Puis il fit continuer le trajet.

2 → 3.

---

2220.

---

3 → 7.

---

78 divisé par 7.

\[
78=1\times49+4\times7+1
\]

Donc :

\[
141_7
\]

---

7 → 13.

---

60.

---

13 → 10.

---

78.

---

Brutus regarda.

---

78 avait traversé cinq représentations.

---

La chaîne était revenue à son écriture initiale normalisée.

---

Il écrivit :

**78 LEFT AS TEXT.**

**78 RETURNED AS VALUE.**

---

Puis corrigea.

---

Le nombre n’avait jamais été « 78 » au sens absolu.

78 était seulement son écriture décimale.

---

Il écrivit plutôt :

**THE VALUE TRAVELED. THE DIGITS CHANGED.**

---

Voilà.

---

Le système pouvait maintenant faire comprendre quelque chose de très important visuellement.

---

Un nombre n’est pas son écriture.

---

Les chiffres sont une représentation.

---

Le même objet mathématique peut avoir plusieurs formes textuelles.

---

Brutus regarda la grille.

---

Peut-être que c’était ça, le vrai intérêt des cent quarante-quatre chemins.

---

Pas la quantité.

La discipline de séparation entre :

valeur,

représentation,

codec,

route,

et trace.

---

Il écrivit :

**VALUE ≠ REPRESENTATION ≠ TRANSPORT.**

---

Puis il ajouta :

**BUT TRANSPORT MUST PRESERVE THE VALUE CONTRACT.**

---

Il lança une campagne plus sévère.

---

10 000 valeurs aléatoires.

Petits entiers.

Grands BigInt.

Valeurs négatives.

Zéro.

Limites de longueur.

---

Chaque valeur traversait plusieurs routes sélectionnées.

---

Le Journal Vivant enregistrait seulement les détails nécessaires, avec possibilité d’ouvrir chaque trace.

---

Les douze lanes travaillaient.

---

La première lane testait 2→3.

La deuxième 3→4.

La troisième 4→5.

---

À mesure qu’une lane terminait, le scheduler lui attribuait une nouvelle route.

---

Brutus entendait SFX36.

---

PASS regroupés.

Quelques rejets de syntaxe injectés.

Un ERROR volontaire.

---

Le système tenait.

---

Puis une case échoua.

---

RADIX-11-TO-13.

---

Brutus ouvrit.

---

Valeur impliquée :

un grand entier.

---

Le codec n’était pas en cause.

---

La faute venait d’un alphabet.

---

Le parser acceptait B dans une base où le digit 11 n’était pas valide.

---

Brutus regarda.

---

Voilà un vrai bug de contrat.

---

Il écrivit :

**ALPHABET PARSER MUST BE RADIX-AWARE.**

---

Correction.

---

Retest.

---

PASS.

---

Régression sur toutes les bases.

---

PASS.

---

Le Journal Vivant conserva :

bug.

cause.

patch.

retest.

---

Brutus sourit.

La matrice avait déjà trouvé une faille.

---

Il ajouta le cas comme test permanent.

---

**REGRESSION-RADIX-ALPHABET-0001.**

---

Un échec venait encore de devenir une protection.

---

Le laboratoire apprenait bien.

---

Puis Brutus s’intéressa aux routes diagonales.

---

2→2.

3→3.

4→4.

---

Elles semblaient inutiles.

Pourquoi convertir une représentation vers la même base ?

---

Brutus allait presque les ignorer.

Puis se ravisa.

---

Elles pouvaient tester la normalisation du codec.

---

Input base 10 :

00078.

---

Output normalized base 10 :

78.

---

Input base 13 :

060.

---

Output :

60.

---

Ces routes testaient donc :

parse.

canonicalize.

re-encode.

---

Brutus écrivit :

**IDENTITY ROUTE IS STILL A TEST.**

---

Très utile.

---

Les douze cases diagonales devenaient des tests de santé pour chaque codec.

---

Si RADIX-7-TO-7 échouait, il n’était même pas utile de tester 7→13.

---

Brutus modifia l’ordre de qualification.

---

Avant qu’un codec entre dans la matrice complète :

son identity route devait passer.

---

Il écrivit :

**SELF-ROUNDTRIP BEFORE CROSS-CONVERSION.**

---

Encore une économie de tests.

---

Le système lança les douze diagonales.

---

Toutes passèrent.

---

Puis les cent trente-deux conversions croisées.

---

Brutus regarda le compteur.

---

144 routes.

144 configured.

144 qualified under current suite.

---

Il ne mit pas :

**144 proven correct.**

---

Il écrivit :

**144 ROUTES PASSED CURRENT TEST CONTRACT.**

---

Beaucoup mieux.

---

Brutus ouvrit le Journal Vivant.

---

La matrice pouvait maintenant être consultée par version.

---

Codec v1.

Codec v2.

---

Une modification dans le parser pouvait être comparée sur les 144 chemins.

---

Si une nouvelle version améliorait une route mais en cassait trois autres, le journal le montrerait immédiatement.

---

Il écrivit :

**A CODEC CHANGE MUST FACE THE WHOLE MATRIX.**

---

La grille devenait un test de régression naturel.

---

Une seule petite modification.

Cent quarante-quatre conséquences potentielles.

---

Le laboratoire pouvait toutes les vérifier.

---

Brutus pensa aux cent formules.

---

Même principe.

Une modification locale pouvait avoir des effets globaux.

---

Le Journal Vivant et les lanes permettaient maintenant d’explorer cette surface.

---

Il écrivit :

**LOCAL CHANGE. GLOBAL RETEST.**

---

Puis il revint au nom du chapitre.

**Cent quarante-quatre chemins de 78 à 2.**

---

C’était volontairement étrange.

---

Dans l’expérience réelle, il n’existait qu’un chemin direct particulier pour convertir 78 décimal vers base 2.

---

Mais autour de cette conversion existaient 143 autres relations de représentation dans la matrice.

---

Et d’innombrables routes multi-hop à travers le graphe.

---

Brutus écrivit une note :

**144 = COUNT OF DIRECTED SOURCE/DESTINATION CELLS IN THE 12×12 MATRIX.**

---

Pas 144 manières mathématiquement uniques d’écrire 78 en binaire.

---

Important.

---

Le titre pouvait être poétique.

Le contrat ne devait jamais l’être.

---

Brutus sourit.

---

Il lança un dernier trajet.

---

78 base 10.

↓

base 2.

↓

base 13.

↓

base 6.

↓

base 11.

↓

base 10.

---

À chaque étape :

canonical = 78n.

---

Final :

78.

---

PASS.

---

Puis il modifia volontairement une seule représentation intermédiaire.

---

Base 13 :

61 au lieu de 60.

---

Le hop check s’arrêta immédiatement.

---

Canonical:

79n.

Expected:

78n.

---

FAIL.

---

Les étapes suivantes ne furent pas exécutées.

---

Brutus écrivit :

**DO NOT PROPAGATE CORRUPTED VALUE.**

---

La route mourait à l’endroit exact où la valeur avait changé.

---

La trace montrait :

source.

destination.

before.

after.

expected canonical.

observed canonical.

---

Voilà.

---

Une corruption n’était plus seulement détectée.

Elle était localisée.

---

Brutus regarda la matrice.

---

Cent quarante-quatre chemins.

Chacun pouvait répondre :

d’où je viens.

où je vais.

quel codec m’a transformé.

quelle valeur j’ai reçue.

quelle valeur j’ai produite.

si je l’ai conservée.

---

Il écrivit :

**A PATH IS AUDITABLE WHEN EVERY TRANSFORMATION HAS A BEFORE AND AFTER.**

---

La grille ne ressemblait plus du tout à un jouet numérique.

---

Elle ressemblait à une carte de douane.

---

Chaque frontière inspectait ce qui la traversait.

---

Le nombre pouvait changer de vêtements.

Mais pas d’identité mathématique.

---

Brutus écrivit :

**CHANGE THE CLOTHES. KEEP THE VALUE.**

---

Puis il rit.

---

Peut-être que celle-là resterait dans le livre.

Pas dans le protocole.

---

Il sauvegarda :

**RADIX-BRAID-12x12 v1.**

---

Les cent quarante-quatre cellules s’éteignirent.

---

Le chapitre semblait terminé.

Mais Brutus regardait déjà ailleurs.

---

Les nombres avaient survécu à leurs représentations.

Les formules avaient survécu aux arènes.

Les Z pouvaient transporter des objets exacts.

---

Maintenant, il était temps de revenir à quelque chose de beaucoup moins général.

Une porte précise.

Un problème précis.

Une relation que Brutus connaissait déjà.

---

Il ouvrit le dossier Brutus–Pell.

---

Plusieurs nombres apparurent.

47.

71.

83.

---

Brutus regarda le premier.

---

47.

---

Pas comme un nombre mystique.

Comme une porte mathématique avec un test défini.

---

Il ferma la matrice 12×12.

Puis ouvrit un nouveau banc.

---

Les règles allaient changer.

Ici, une conversion correcte ne suffirait plus.

Une formule correcte ne suffirait plus.

Il faudrait construire un témoin.

---

Brutus écrivit :

**q = 47**

Puis :

**DO NOT CALL IT OPEN UNTIL THE WITNESS PASSES.**

---

Le laboratoire venait d’apprendre à transporter les nombres sans les abîmer.

Il était maintenant prêt à demander à l’un d’eux de témoigner.
