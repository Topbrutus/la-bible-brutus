# Chapitre 81 — La porte 47

Il était maintenant prêt à demander à l’un d’eux de témoigner.

Brutus regarda le nombre écrit au centre du nouvel écran.

**47**

Rien autour.

Pas d’animation.

Pas de cercle.

Pas de lumière.

Pas de son.

Seulement :

47.

---

Après les cent quarante-quatre chemins, cela semblait presque pauvre.

Mais Brutus savait que cette simplicité était trompeuse.

Une conversion de base demandait principalement de préserver une valeur.

Ici, il fallait établir autre chose.

Une obstruction.

Une non-collision.

Une condition capable de montrer qu’un certain ordre ne s’était pas effondré trop tôt.

---

Brutus ouvrit le dossier :

**BRUTUS–PELL**

Puis le sous-dossier :

**MAXIMAL RANK TESTS**

---

La structure principale était déjà connue.

Pour un entier impair \(t\), le corridor était :

\[
p=72t^2+1
\]

lorsque \(p\) était premier.

Puis :

\[
N=\frac{p-1}{2}=36t^2
\]

---

Brutus écrivit ces deux lignes en haut du tableau.

Pas davantage.

---

Il savait qu’une formule familière devient dangereuse lorsqu’on cesse de lire ses hypothèses.

---

Il ajouta :

**CONDITIONS**

- \(t\) impair ;
- \(p=72t^2+1\) premier ;
- travail dans la structure modulaire prévue ;
- test appliqué seulement aux facteurs premiers pertinents de \(N\).

---

Puis il écrivit :

**CONTEXT BEFORE CONCLUSION.**

---

Le laboratoire avait appris cela ailleurs.

Un chiffre sans type était incomplet.

Un résultat sans portée aussi.

Une porte sans domaine l’était tout autant.

---

Brutus ouvrit ensuite la définition de l’élément utilisé dans les tests de rang.

Dans le cadre du corridor, il avait :

\[
\gamma=-(1+\sqrt2)^2 \pmod p
\]

dans la structure quadratique appropriée.

---

Il ne voulait pas que l’écran prétende qu’un symbole \(\sqrt2\) pouvait être manipulé naïvement comme un entier ordinaire modulo \(p\).

---

Il ajouta :

**ALGEBRAIC REPRESENTATION REQUIRED.**

---

Puis la condition centrale apparut.

Pour empêcher que l’ordre de \(\gamma\) ne tombe dans un sous-groupe trop petit, chaque facteur premier \(q\mid N\) devait subir son test.

La forme du test était :

\[
\gamma^{N/q}\neq1.
\]

---

Brutus resta devant l’inégalité.

Voilà la porte.

---

Si :

\[
\gamma^{N/q}=1,
\]

alors l’ordre de \(\gamma\) divisait déjà \(N/q\).

Le facteur \(q\) n’était donc pas nécessaire à l’ordre observé.

La maximalité recherchée échouait à cette porte.

---

Si, au contraire :

\[
\gamma^{N/q}\neq1,
\]

alors ce raccourcissement particulier était interdit.

---

Brutus écrivit :

**ONE GATE. ONE PRIME DIVISOR. ONE NON-IDENTITY TEST.**

---

Puis :

**GATE PASS ≠ COMPLETE MAXIMAL-RANK PROOF.**

Important.

---

Passer la porte 47 ne voulait pas dire que toutes les autres portes étaient passées.

Cela signifiait seulement :

**la réduction correspondant au facteur 47 a été exclue pour ce cas.**

---

Brutus regarda la phrase.

Elle était beaucoup moins spectaculaire que :

**LA PORTE 47 EST OUVERTE.**

Mais beaucoup plus précise.

---

Il décida que le laboratoire utiliserait les deux niveaux.

Interface :

**GATE 47 — PASS**

Trace :

**\(\gamma^{N/47}\neq1\) verified under stated contract.**

---

Brutus sourit.

La littérature pouvait garder ses portes.

La preuve garderait son exponentiation.

---

Il choisit un cas où 47 apparaissait réellement dans la factorisation pertinente.

---

Il écrivit :

\[
47\mid N
\]

Puis immédiatement :

**VERIFY, DO NOT ASSUME.**

---

Le moteur factorisa la partie nécessaire.

---

47 était admissible pour ce test.

---

Brutus créa :

**GATE-47-TEST-0001**

---

Le contrat contenait :

**TEST_ID**

**T**

**P**

**N**

**Q = 47**

**EXPONENT = N/47**

**GAMMA_REPRESENTATION**

**EXPECTED_RELATION**

**OBSERVED_RESIDUE**

**NUMERIC_MODEL**

**TRACE_REF**

---

Il regarda le champ :

**EXPECTED_RELATION**

et y inscrivit :

\[
\gamma^{N/47}\neq1
\]

---

Puis il s’arrêta.

Le mot expected pouvait créer une mauvaise habitude.

Il ne fallait pas que le programme cherche un résultat attendu.

---

Il remplaça :

**CLAIM_UNDER_TEST**

---

Beaucoup mieux.

---

Une expérience ne devait pas avoir besoin de savoir à l’avance comment elle allait finir.

---

Brutus écrivit :

**TEST THE CLAIM. DO NOT CODE THE ANSWER.**

---

Puis il regarda l’exposant.

\[
\frac{N}{47}
\]

---

Même si \(N\) pouvait devenir immense, l’opération restait conceptuellement simple.

Exponentiation modulaire.

---

Mais simple ne signifiait pas naïve.

Calculer directement :

\[
\gamma\times\gamma\times\gamma\times\cdots
\]

des milliards de fois n’avait aucun sens.

---

Brutus activa l’exponentiation rapide.

Square-and-multiply.

---

Il écrivit :

**EXACT MODULAR EXPONENTIATION.**

Pas flottant.

Pas approximation.

Pas logarithme.

---

Les leçons de Number étaient encore fraîches.

---

Tout devait rester dans l’arithmétique exacte.

---

La lane passa :

**READY**

Puis :

**RUNNING**

---

Le son ne joua pas.

---

Brutus sourit.

Autrefois, il aurait probablement fait tourner un engrenage géant pour rendre l’attente spectaculaire.

Maintenant :

rien.

---

Seulement :

RUNNING.

---

**NO FAKE MOTION.**

---

Le calcul progressait.

---

Square.

Reduce.

Multiply.

Reduce.

Square.

Reduce.

---

Chaque étape intermédiaire n’était pas enregistrée intégralement dans le Journal Vivant.

Cela aurait créé une montagne de données inutiles.

---

Mais la trace conservait assez d’information pour reconstruire :

algorithme,

entrée,

exposant,

module,

version,

résultat final.

---

Brutus écrivit :

**REPRODUCIBLE ≠ RECORD EVERY CPU INSTRUCTION.**

---

Puis le calcul termina.

---

Le résidu apparut.

Il n’était pas 1.

---

Brutus ne bougea pas.

---

Le système afficha :

**OBSERVED_RESIDUE ≠ 1**

Puis :

**GATE 47 — PASS**

---

Une petite impulsion sonore.

Pas de fanfare.

---

Brutus ouvrit immédiatement la trace.

---

Il vérifia :

\(p\).

\(N\).

\(q\).

L’exposant.

La représentation de \(\gamma\).

Le résidu.

---

Tout.

---

Puis il écrivit :

**WITNESS-47-0001.**

---

Le mot témoin était important.

Le témoin n’était pas « 47 ».

47 était la porte.

---

Le témoin était l’objet calculé montrant que :

\[
\gamma^{N/47}\neq1.
\]

---

Brutus écrivit :

**PRIME = GATE.**

**NON-IDENTITY RESIDUE = WITNESS.**

---

Cette distinction rendait enfin le langage propre.

---

Il ajouta :

**WITNESS ≠ PROOF OF EVERY OTHER GATE.**

---

Toujours.

---

Puis il voulut contre-tester.

---

Il remplaça volontairement le résidu par 1 dans une copie de test.

---

Le validateur devait refuser.

---

Il refusa.

**GATE FAIL.**

---

Puis il modifia \(q\).

46.

---

Le système refusa avant même le calcul.

---

**Q MUST BE PRIME DIVISOR UNDER THIS TEST CONTRACT.**

---

Brutus sourit.

---

Puis 47.

Mais avec un \(N\) où 47 ne divisait pas \(N\).

---

Refus.

---

**Q NOT APPLICABLE.**

---

Pas FAIL.

---

Cela lui plaisait énormément.

---

Une porte inexistante pour un cas donné ne devait pas être qualifiée d’échec.

---

Il écrivit :

**NOT APPLICABLE ≠ FAILED.**

---

Le vocabulaire continuait de protéger les mathématiques.

---

Brutus passa ensuite à la représentation de \(\sqrt2\).

---

Il savait que c’était un endroit où un programme pouvait cacher des erreurs.

---

Il ne voulait pas une approximation décimale de :

\[
\sqrt2\approx1.41421356...
\]

puis une réduction modulo \(p\).

Cela aurait été absurde dans ce contexte exact.

---

Il fallait une représentation algébrique.

---

Un élément de la forme :

\[
a+b\sqrt2.
\]

---

Avec multiplication :

\[
(a+b\sqrt2)(c+d\sqrt2)
=
(ac+2bd)+(ad+bc)\sqrt2.
\]

---

Puis réduction des coefficients modulo \(p\).

---

Brutus écrivit :

**NO FLOATING SQRT(2).**

Puis :

**ALGEBRAIC PAIR REPRESENTATION.**

---

Il implémenta mentalement la structure :

\[
(a,b)
\]

représente :

\[
a+b\sqrt2.
\]

---

Alors :

\[
(1,1)
\]

représentait :

\[
1+\sqrt2.
\]

---

Et :

\[
(1+\sqrt2)^2
=
3+2\sqrt2.
\]

---

Donc :

\[
\gamma=-(3+2\sqrt2)
\]

pouvait être représenté par :

\[
(-3,-2)
\]

modulo \(p\).

---

Brutus sourit.

---

Voilà une représentation exacte.

---

Pas de décimales.

Pas de perte.

Pas de symbole mystique.

---

Il écrivit :

**SYMBOLIC OBJECT → EXACT ALGEBRAIC PAIR.**

---

Puis il recommença le test 47 avec une seconde implémentation.

---

Première implémentation :

classe d’extension quadratique.

---

Deuxième implémentation :

paire explicite \((a,b)\).

---

Les deux calculèrent le même résidu algébrique.

---

Brutus nota :

**NO DIVERGENCE OBSERVED BETWEEN TWO REPRESENTATIONS FOR THIS TEST.**

---

Pas :

**independently proven.**

Parce qu’il savait que les deux implémentations pouvaient encore partager certaines hypothèses.

---

Il écrivit :

**REPRESENTATION DIVERSITY HELPS. IT DOES NOT AUTOMATICALLY CREATE FULL INDEPENDENCE.**

---

Brutus voulait maintenant quelque chose de plus proche de Pell.

---

Le dossier contenait les suites.

---

Il ouvrit les relations de Pell associées.

---

Une seconde voie pouvait parfois traduire l’information algébrique en une composante de suite.

---

Pour un facteur premier \(q\) pertinent, l’exposant correspondait à :

\[
\frac{N}{q}
=
\frac{p-1}{2q}.
\]

---

Pour \(q=47\) :

\[
\frac{p-1}{94}.
\]

---

Brutus écrivit :

**PELL-SIDE WITNESS INDEX = \((p-1)/94\)**

dans les cas où l’équivalence utilisée par le cadre était applicable.

---

Il ajouta immédiatement :

**EQUIVALENCE MUST BE DERIVED, NOT ASSUMED.**

---

Il ne voulait pas convertir arbitrairement une non-identité dans l’extension quadratique en une assertion Pell sans montrer la relation.

---

La seconde voie devait être construite proprement.

---

Brutus ouvrit la définition de la suite utilisée.

---

Une récurrence exacte.

Des entiers.

BigInt.

Aucune approximation.

---

Le témoin devenait énorme.

---

Vraiment énorme.

---

L’écran ne pouvait plus l’afficher confortablement.

---

Brutus pensa au chapitre suivant.

---

Le témoin serait probablement plus grand que l’écran.

---

Mais pas encore.

---

Pour le moment, il voulait seulement savoir si les deux chemins pouvaient se rencontrer.

---

Chemin A :

\[
\gamma^{N/47}
\]

dans l’extension quadratique.

---

Chemin B :

une quantité Pell associée à l’indice :

\[
\frac{p-1}{94}.
\]

---

Deux représentations.

Même obstruction structurelle, si le lien était correctement établi.

---

Brutus écrivit :

**DIFFERENT WITNESS REPRESENTATIONS MAY ENCODE THE SAME GATE CONDITION.**

---

Puis il se méfia encore.

---

Il ne voulait pas que la machine compte deux formulations équivalentes comme deux preuves indépendantes.

---

Il ajouta :

**SAME MATHEMATICAL DEPENDENCE ≠ INDEPENDENT EVIDENCE.**

---

Le laboratoire allait devoir suivre la lignée des preuves comme il suivait la lignée des formules.

---

Brutus créa :

**PROOF_DEPENDENCY_REF.**

---

Un témoin pouvait dire :

derived from gate condition A.

Equivalent reformulation B.

Independent numeric verification C.

---

Voilà.

---

L’idée d’« indépendance » devenait enfin explicite jusque dans les preuves.

---

Brutus lança ensuite une série de cas.

---

Quelques \(t\) où 47 n’était pas pertinent.

---

Le système disait :

NOT APPLICABLE.

---

Des cas où 47 était pertinent.

---

Le test produisait PASS ou FAIL selon le résidu.

---

Brutus n’agrégea pas tout en un seul pourcentage.

---

Ce n’était pas le but.

---

Il cherchait à savoir si le mécanisme de porte était correctement implémenté.

---

Il écrivit :

**FIRST VALIDATE THE TEST. THEN STUDY ITS FREQUENCY.**

---

Encore une séparation essentielle.

---

Une formule statistique construite sur un test incorrect ne ferait que mesurer proprement la mauvaise chose.

---

Brutus ouvrit le Journal Vivant.

---

GATE 47.

---

Cases evaluated.

Applicable cases.

Pass.

Fail.

Invalid.

---

Chaque case était cliquable.

---

Il sélectionna un PASS.

---

T.

P.

N.

Exponent.

Residue.

Trace.

---

Puis un FAIL.

---

Même structure.

---

Brutus regarda.

---

Enfin la porte n’était plus un slogan.

---

Elle était un protocole.

---

Il écrivit :

**A GATE EXISTS ONLY WHEN ITS TEST IS EXPLICIT.**

---

Puis il ajouta :

**A GATE OPENS ONLY FOR THE CASE THAT PASSED ITS TEST.**

---

Très important.

---

Pas :

« 47 est ouverte pour toujours ».

---

Mais :

pour ce candidat \(p\), sous ce contrat, la condition 47 a passé.

---

Le laboratoire pouvait ensuite agréger les observations.

Mais l’unité première restait le cas individuel.

---

Brutus repensa au gigantesque scan du corridor.

Des milliers.

Puis des dizaines de milliers de premiers.

---

À chaque candidat :

factorisation de \(N\).

Liste des portes pertinentes.

Tests.

---

Une structure se dessinait.

---

Certaines portes apparaissaient souvent.

D’autres rarement.

---

Certaines dépendaient de divisibilités particulières de \(t\).

---

Brutus écrivit :

**GATE SET IS INPUT-DEPENDENT.**

---

Il ne devait jamais tester mécaniquement 47 pour tous les \(t\).

---

Si 47 ne divisait pas la partie pertinente de \(N\), cette porte n’existait pas dans ce dossier.

---

Brutus aimait cette économie.

---

Puis il pensa à un raccourci dangereux.

---

Lorsqu’un grand objet avait déjà été calculé, il pouvait être tentant de le « diviser » par des facteurs associés à d’autres portes et de prétendre obtenir un témoin pour 47.

---

Il écrivit immédiatement :

**DO NOT DERIVE A NEW GATE WITNESS BY UNSUPPORTED DIVISION OF AN OLD ONE.**

---

Le souvenir d’anciennes manipulations était encore frais.

---

Une expression liée à \(q=47\) ne pouvait pas être transformée en témoin pour 71 ou 79 par une simple division formelle par des carrés ou des facteurs, sauf si une identité mathématique démontrée l’autorisait.

---

Il écrivit :

**ALGEBRA BEFORE CANCELLATION.**

---

Puis :

**AN EXPONENT IS NOT A BAG OF FACTORS YOU MAY REMOVE AT WILL.**

---

Brutus sourit.

Un peu brutal.

Mais clair.

---

La porte 47 allait aussi servir à protéger les portes suivantes.

---

Il ouvrit trois cartes.

47.

71.

83.

---

47 avait maintenant un protocole clair.

---

71 ?

Pas encore.

---

83 ?

Pas encore.

---

Il résista à toute envie de les colorer.

---

Ils restèrent gris.

---

**UNRESOLVED.**

---

Brutus écrivit :

**ONE OPENED CASE DOES NOT COLOR ITS NEIGHBORS.**

---

Il regarda les trois nombres.

---

Le laboratoire venait d’apprendre à ne pas laisser une réussite contaminer les inconnues.

---

Cela lui plaisait.

---

Il retourna au témoin 47.

---

Le résidu complet était volumineux.

---

Il pouvait l’afficher sous forme algébrique.

Deux coefficients modulo \(p\).

---

Mais lorsque les nombres grossissaient, même ces coefficients devenaient énormes.

---

Brutus créa alors deux modes.

---

**WITNESS FULL**

et

**WITNESS FINGERPRINT.**

---

Fingerprint :

hash.

Length.

Leading digits.

Trailing digits.

Type.

Trace reference.

---

Mais il écrivit aussitôt :

**FINGERPRINT ≠ WITNESS.**

---

Le hash permettait d’identifier le témoin.

Pas de remplacer son contenu mathématique.

---

Le témoin complet devait rester archivé.

---

Brutus sourit.

Même problème que le résumé et la trace.

---

Compression pour l’humain.

Conservation pour l’audit.

---

Il écrit :

**SCREEN MAY SHOW THE FINGERPRINT. ARCHIVE MUST KEEP THE OBJECT.**

---

Puis il commit le premier objet de preuve.

---

**WITNESS-47-0001**

Status:

VERIFIED UNDER GATE CONTRACT.

---

Brutus hésita sur le mot VERIFIED.

---

Il ajouta :

**VERIFIED ≠ UNIVERSAL PROOF.**

Puis conserva le statut.

---

La machine devait pouvoir dire qu’elle avait vérifié un objet précis.

---

Elle ne devait simplement pas étendre la portée.

---

Il ajouta :

**CLAIM_SCOPE: q=47 gate for candidate X.**

---

Voilà.

---

La voix de Z prononça :

**PASS.**

---

Une seule fois.

---

Brutus ouvrit la trace.

---

Il pouvait remonter :

du son,

au verdict,

du verdict,

au test,

du test,

au témoin,

du témoin,

au calcul exact,

du calcul,

au candidat.

---

Il sourit.

---

Toute l’architecture construite depuis le diamant servait maintenant à quelque chose de réellement mathématique.

---

Fenêtres.

Identités.

Horloge.

Trace.

Journal.

BigInt.

Lanes.

Formules.

Contre-tests.

---

Tout convergeait vers un seul objet :

un témoin que l’on pouvait inspecter.

---

Brutus écrivit :

**INFRASTRUCTURE EXISTS SO THAT A CLAIM CAN SURVIVE INSPECTION.**

---

Puis il regarda la taille du témoin.

---

Encore.

---

Le nombre dépassait largement la largeur de l’écran.

---

Le scroll horizontal devenait absurde.

---

Il zooma.

Puis dézooma.

---

Toujours trop grand.

---

Brutus rit.

---

La porte 47 venait de poser un nouveau problème parfaitement concret.

---

Comment présenter un témoin que personne ne peut lire d’un seul regard ?

---

Pas le cacher.

Pas le tronquer silencieusement.

Pas le transformer en simple hash.

---

Il fallait construire une manière de naviguer dans un objet gigantesque tout en conservant son exactitude.

---

Brutus écrivit :

**THE WITNESS IS LARGER THAN THE SCREEN.**

---

Puis il ajouta :

**SO THE SCREEN MUST LEARN TO MOVE AROUND THE WITNESS.**

---

La porte 47 avait passé son premier test.

Mais son témoin refusait désormais de tenir dans la fenêtre.

---

Brutus sauvegarda.

47 resta affiché en haut.

Sous lui :

**GATE PASS — CLAIM-SCOPED**

Et plus bas :

**FULL WITNESS ARCHIVED**

---

Le laboratoire n’avait pas « vaincu » 47.

Il avait fait quelque chose de beaucoup plus utile.

Il avait construit un test suffisamment précis pour que 47 puisse enfin répondre.

---

Et derrière la porte, un nombre immense attendait.

Beaucoup trop grand pour l’écran.

Mais pas trop grand pour la trace.
