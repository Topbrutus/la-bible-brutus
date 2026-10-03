# Chapitre 87 — Deux voix, un rayon et un angle

Dans le plan Mid-Side, un rayon attendait.

Avec un angle.

Brutus rouvrit la fenêtre qu’il avait fermée au chapitre précédent.

Deux axes apparurent.

Horizontal :

**M**

Vertical :

**S**

---

Au centre :

\[
(0,0)
\]

---

Puis un point.

\[
(M,S)
\]

---

Brutus le regarda.

Jusqu’ici, ce point avait deux coordonnées.

Mid.

Side.

Deux nombres.

---

Mais on pouvait décrire exactement le même point autrement.

Par sa distance à l’origine.

Et sa direction.

---

Brutus écrivit :

\[
r=\sqrt{M^2+S^2}
\]

Puis :

\[
\theta=\operatorname{atan2}(S,M)
\]

---

Deux nouvelles valeurs.

Un rayon.

Un angle.

---

Il écrivit immédiatement :

**SAME POINT. DIFFERENT COORDINATE SYSTEM.**

---

Le chapitre 80 revenait encore.

Valeur.

Représentation.

Transformation.

---

Seulement, cette fois, le terrain avait changé.

Avec les bases numériques, le même entier pouvait souvent voyager exactement.

Avec Mid/Side, les opérations linéaires pouvaient rester exactes sous certains modèles.

Mais avec :

\[
\sqrt{\phantom{x}}
\]

et

\[
\operatorname{atan2},
\]

on entrait généralement dans le monde des approximations numériques.

---

Brutus écrivit :

**COORDINATE TRANSFORM MAY CHANGE NUMERIC EXACTNESS CLASS.**

---

Voilà le premier contrat.

---

Il ouvrit le NUMERIC REGISTRY.

Input :

M, S.

Numeric class :

declared.

---

Output :

r.

theta.

---

Rayon :

potentiellement exact symboliquement dans certains cas.

Mais généralement calculé approximativement.

---

Angle :

généralement flottant approximatif dans l’implémentation.

---

Brutus ajouta :

**POLAR_OUTPUT_CLASS = APPROXIMATE unless symbolic representation exists.**

---

Pas de confusion.

---

Il prit le premier cas.

\[
M=1,\quad S=0.
\]

Alors :

\[
r=1
\]

et

\[
\theta=0.
\]

---

Simple.

---

Deuxième cas.

\[
M=0,\quad S=1.
\]

---

Alors :

\[
r=1
\]

et

\[
\theta=\frac{\pi}{2}.
\]

---

Brutus s’arrêta.

---

L’angle pouvait être représenté symboliquement :

\[
\frac{\pi}{2}
\]

ou numériquement :

environ 1.5708 radians.

---

Ce n’était pas la même chose.

---

Il écrivit :

**SYMBOLIC ANGLE ≠ FLOAT APPROXIMATION.**

---

Le laboratoire devait savoir lequel il possédait.

---

Il ajouta :

**ANGLE_REPRESENTATION**

SYMBOLIC.

FLOAT64.

ARBITRARY_PRECISION.

---

Puis :

**ANGLE_UNIT**

RADIAN.

DEGREE.

---

Brutus sourit.

Un angle sans unité était presque aussi dangereux qu’un nombre sans base.

---

Il écrivit :

**ANGLE WITHOUT UNIT IS INCOMPLETE DATA.**

---

Cela allait rester.

---

Puis troisième test.

\[
M=-1,\quad S=0.
\]

---

Le rayon :

\[
r=1.
\]

---

Mais l’angle ?

---

Il dépendait de la convention de branche.

Avec atan2 :

\[
\theta=\pi
\]

ou, selon la représentation choisie, \(-\pi\) à la frontière équivalente.

---

Brutus regarda.

Voilà un problème de convention.

---

Le point était le même.

Mais sa description angulaire pouvait utiliser des intervalles différents.

---

Il écrivit :

**ANGLE BRANCH IS PART OF THE CONTRACT.**

---

Puis ajouta :

**POLAR_CONVENTION_ID.**

---

Par exemple :

\[
\theta\in(-\pi,\pi]
\]

ou :

\[
\theta\in[0,2\pi).
\]

---

Même géométrie.

Écriture différente.

---

Brutus écrivit :

**SAME DIRECTION CAN HAVE MULTIPLE ANGULAR REPRESENTATIONS.**

---

Encore le chapitre 80.

---

La représentation n’était pas l’objet.

---

Il construisit donc :

**DAAT-POLAR-CONTRACT-v1**

avec :

**INPUT_SPACE = MS**

**OUTPUT_SPACE = POLAR**

**ANGLE_UNIT = RADIAN**

**ANGLE_BRANCH = (-π, π]**

**NUMERIC_MODEL = FLOAT64**

**ROUNDTRIP_TOLERANCE = DECLARED**

---

Il regarda le dernier champ.

---

Tolérance.

---

Cette fois, impossible de faire semblant.

---

Avec les fonctions trigonométriques numériques, le roundtrip ne devait pas exiger une égalité bit-à-bit dans tous les cas.

---

Brutus écrivit :

**APPROXIMATE TRANSFORM REQUIRES APPROXIMATE ROUNDTRIP CONTRACT.**

---

Puis définît l’inverse :

\[
M=r\cos\theta
\]

\[
S=r\sin\theta.
\]

---

Voilà le retour.

---

Cartésien vers polaire :

\[
(M,S)\rightarrow(r,\theta)
\]

Puis :

\[
(r,\theta)\rightarrow(M',S').
\]

---

Le test devenait :

\[
M'\approx M
\]

et

\[
S'\approx S
\]

selon une tolérance préétablie.

---

Brutus écrivit :

**APPROXIMATE EQUALITY MUST BE PREDECLARED.**

---

Puis :

**TOLERANCE IS NOT A REPAIR TOOL.**

---

Le chapitre 78 revenait encore.

---

On ne devait pas élargir la tolérance après avoir vu une erreur.

---

Brutus choisit plusieurs cas simples.

---

\[
(M,S)=(3,4)
\]

Alors :

\[
r=5.
\]

---

L’angle :

\[
\theta=\operatorname{atan2}(4,3).
\]

---

Brutus calcula.

---

Puis reconstruisit :

\[
M'=5\cos\theta
\]

\[
S'=5\sin\theta.
\]

---

Les valeurs revenaient très près de :

3 et 4.

---

PASS selon le contrat de tolérance.

---

Il écrivit :

**ROUNDTRIP PASS UNDER DECLARED FLOATING-POINT TOLERANCE.**

---

Pas :

exact identity in machine representation.

---

La distinction était importante.

---

Brutus testa ensuite :

\[
(M,S)=(0,0).
\]

---

Le rayon :

\[
r=0.
\]

---

Et l’angle ?

---

Il s’arrêta.

---

Voilà un cas particulier.

À l’origine, la direction n’était pas définie géométriquement.

---

Certaines bibliothèques retournaient une valeur conventionnelle.

Mais mathématiquement, aucun angle unique n’était imposé.

---

Brutus écrivit :

**ZERO RADIUS → ANGLE UNDEFINED BY GEOMETRY.**

---

Le système ne devait pas transformer une convention logicielle en propriété mathématique.

---

Il créa :

**ANGLE_STATE = UNDEFINED_AT_ORIGIN.**

---

Très important.

---

Si une implémentation retournait 0 pour atan2(0,0), le laboratoire pouvait enregistrer :

implementation output = 0.

Mais la couche mathématique devait dire :

angle geometrically undefined.

---

Brutus écrivit :

**IMPLEMENTATION VALUE ≠ MATHEMATICAL UNIQUENESS.**

---

Encore une frontière.

---

Il aimait beaucoup ce test.

---

Parce qu’il montrait qu’un ordinateur peut toujours rendre un nombre, même lorsque la question demande plus de prudence.

---

Brutus ajouta au pipeline :

**ORIGIN_CHECK BEFORE ANGLE INTERPRETATION.**

---

Maintenant, aucun graphe ne dessinerait une direction arbitraire lorsque le rayon était zéro.

---

Pas de flèche fictive.

---

**NO FAKE DIRECTION.**

---

Il sourit.

Une cousine de NO FAKE MOTION.

---

Puis il passa à l’audio.

---

Que représentait le rayon dans ce contexte ?

---

Pour un échantillon Mid-Side :

\[
r=\sqrt{M^2+S^2}.
\]

---

Il mesurait la magnitude euclidienne du couple \((M,S)\).

---

Brutus écrivit :

**r = EUCLIDEAN MAGNITUDE IN M/S COORDINATES.**

---

Il refusa de l’appeler :

énergie physique.

---

Parce que cela dépendrait des conventions, du signal, de la normalisation et de la définition d’énergie utilisée.

---

Il écrivit :

**GEOMETRIC MAGNITUDE ≠ AUTOMATIC PHYSICAL ENERGY CLAIM.**

---

Très important.

---

Le laboratoire pouvait utiliser \(r\) comme quantité géométrique.

Pas lui attribuer une signification acoustique supplémentaire sans dérivation.

---

Puis l’angle.

---

\[
\theta=\operatorname{atan2}(S,M)
\]

---

Que disait-il ?

---

Il décrivait l’orientation du point dans le plan Mid-Side.

---

Un angle proche de zéro :

Mid dominant positif.

---

Un angle proche de :

\[
\frac{\pi}{2}
\]

Side dominant positif.

---

Près de :

\[
-\frac{\pi}{2}
\]

Side dominant négatif.

---

Brutus écrivit :

**ANGLE = ORIENTATION IN M/S PLANE.**

---

Pas :

position sonore absolue.

---

Pas :

angle physique dans la pièce.

---

Pas :

azimut de la source.

---

Il ajouta immédiatement :

**M/S ANGLE ≠ PHYSICAL SOURCE ANGLE.**

---

Voilà une limite capitale.

---

Un signal stéréo est le résultat de microphones, mixage, délais, phases, traitements et gains.

Le simple angle du vecteur \((M,S)\) ne donnait pas automatiquement la position réelle d’un objet dans l’espace.

---

Brutus écrivit :

**GEOMETRIC FEATURE ≠ PHYSICAL LOCALIZATION.**

---

Le laboratoire venait encore de protéger une métaphore séduisante.

---

Il dessina un point.

Puis un rayon depuis l’origine.

---

Une petite flèche.

---

Le point bougeait au rythme du signal.

---

Cette animation était autorisée.

Pourquoi ?

Parce qu’elle provenait directement des échantillons calculés.

---

Il écrivit :

**VISUAL MOTION MUST BE DATA-DRIVEN.**

---

Pas de rotation permanente lorsqu’il n’y avait pas de données.

---

Signal zéro ?

Point au centre.

Pas de flèche de direction.

---

Signal actif ?

Point déplacé selon \(M,S\).

---

Brutus regarda.

---

Pour la première fois, la stéréo pouvait être vue comme une géométrie mouvante sans prétendre qu’il s’agissait d’un espace physique réel.

---

Il nomma la vue :

**DAAT VECTOR SCOPE.**

---

Input :

L/R.

---

Transform :

M/S.

---

Derived :

r/θ.

---

Display :

point + radius + angle.

---

Brutus écrivit :

**DISPLAY IS DERIVED FROM AUDIO STATE.**

---

Puis testa un signal mono.

L = R.

---

Alors :

\[
S=0.
\]

---

Le point restait sur l’axe Mid.

---

L’angle était :

0 lorsque Mid positif.

\(\pi\) lorsque Mid négatif.

---

Brutus regarda la flèche basculer de droite à gauche avec le signe du signal.

---

Il sourit.

---

Même un signal purement mono oscillait entre deux directions géométriques opposées dans ce plan, simplement parce que l’amplitude changeait de signe.

---

Important.

---

Cela montrait pourquoi il ne fallait pas interpréter \(\theta\) naïvement comme « largeur stéréo ».

---

Brutus écrivit :

**INSTANTANEOUS ANGLE MAY FLIP WITH SIGNAL POLARITY.**

---

Donc :

**ANGLE ≠ SIMPLE WIDTH METER.**

---

Voilà.

---

Si l’on voulait une mesure de largeur ou de relation stéréo stable, il faudrait intégrer ou analyser dans le temps.

---

Pas regarder un seul échantillon.

---

Brutus ajouta :

**SAMPLE-LEVEL FEATURE ≠ WINDOW-LEVEL METRIC.**

---

Le mot fenêtre revenait encore.

---

Il créa une fenêtre temporelle.

Par exemple :

un bloc de plusieurs échantillons.

---

Dans ce bloc, on pouvait calculer des statistiques.

---

Moyennes de puissances.

Relations entre canaux.

Corrélation.

Distribution angulaire.

---

Mais pas encore.

---

Chaque nouvelle métrique devrait avoir son contrat.

---

Brutus écrivit :

**AGGREGATION CREATES A NEW OBJECT.**

---

Une valeur instantanée et une statistique de fenêtre n’étaient pas la même chose.

---

Il ajouta :

**WINDOW_ID**

**START_SAMPLE**

**END_SAMPLE**

**SAMPLE_COUNT**

---

Toute métrique agrégée devait connaître sa fenêtre.

---

Encore le contexte.

---

Brutus choisit un bloc stéréo.

---

Pour chaque échantillon :

\[
(M_i,S_i)
\]

puis :

\[
r_i,\theta_i.
\]

---

Il dessina la distribution des points.

---

Un nuage apparut.

---

Brutus resta devant.

---

Cette fois, le signal n’était plus un seul rayon.

Il devenait une forme.

---

Mais il s’interdit de l’appeler immédiatement :

signature.

empreinte universelle.

structure cachée.

---

Il écrivit :

**POINT CLOUD = OBSERVED SAMPLE DISTRIBUTION IN CHOSEN COORDINATES.**

---

Rien de plus.

---

Le laboratoire avait grandi.

---

Autrefois, une belle forme aurait peut-être déclenché une théorie.

Maintenant, elle déclenchait une définition.

---

Brutus sourit.

---

Il ajouta une grille.

---

Quadrant I :

M positif.

S positif.

---

Quadrant II :

M négatif.

S positif.

---

Quadrant III :

M négatif.

S négatif.

---

Quadrant IV :

M positif.

S négatif.

---

Puis se demanda si les quadrants avaient une signification audio immédiate.

---

Pas universelle.

---

Ils décrivaient simplement les signes de Mid et Side.

---

Il écrivit :

**QUADRANT LABEL ≠ AUDIO SEMANTIC LABEL.**

---

Pas de « voix », « espace », « profondeur », « intention ».

---

Seulement signes.

---

Brutus lança ensuite deux sinusoïdes.

Même fréquence.

Même amplitude.

Mais avec un déphasage entre gauche et droite.

---

Le point M/S décrivit une trajectoire.

---

Une ellipse apparut.

---

Brutus regarda.

---

Voilà quelque chose de familier dans l’analyse stéréo.

---

Un vecteurscope pouvait produire des lignes, ellipses et nuages selon les relations de phase et d’amplitude.

---

Mais encore une fois :

forme observée.

Pas verdict automatique.

---

Il écrivit :

**SHAPE MAY REFLECT CHANNEL RELATION.**

Puis :

**SHAPE NAME ≠ CAUSAL EXPLANATION.**

---

Il testa plusieurs cas.

---

L = R.

---

La trajectoire s’alignait sur Mid.

---

L = -R.

---

Elle s’alignait sur Side.

---

Décalage de phase intermédiaire.

---

Une ellipse.

---

Différence d’amplitude.

---

Ellipse inclinée ou déformée selon le cas.

---

Brutus aimait cette géométrie.

---

Pas parce qu’elle cachait un secret.

Parce qu’elle rendait certaines relations visibles.

---

Il écrivit :

**VISUALIZATION CAN REVEAL RELATIONSHIP WITHOUT EXPLAINING CAUSE.**

---

Voilà une phrase utile.

---

Le scope pouvait montrer.

Le test devait expliquer.

---

Puis Brutus ouvrit un second panneau.

---

Il voulait comparer L/R et M/S côte à côte.

---

Pas deux machines.

Deux vues du même signal.

---

Brutus écrivit :

**ONE SOURCE. MULTIPLE VIEWS.**

---

Le même AUDIO_FRAME_ID alimentait les deux.

---

Aucune duplication d’autorité.

---

Le renderer LR.

Le renderer MS.

Le renderer polar.

---

Trois projections.

---

Il écrivit :

**RENDERER ≠ SOURCE.**

---

Encore une vieille règle.

---

Le système était cohérent.

---

Brutus pensa maintenant à la possibilité d’envoyer ces trois vues sur trois écrans différents.

---

Écran 1 :

L/R waveform.

---

Écran 2 :

M/S scope.

---

Écran 3 :

polar vector.

---

Mais il ne voulait surtout pas créer trois flux audio différents.

---

Un seul signal.

Trois observateurs.

---

Il écrivit :

**ONE AUDIO AUTHORITY. MULTIPLE VISUAL OBSERVERS.**

---

Le principe du chapitre 64 revenait jusque dans l’audio.

---

Brutus sourit.

---

Il activa les trois fenêtres.

---

Même tick audio.

Même frame ID.

Même source.

---

Les affichages évoluaient ensemble.

---

Pas parfaitement au pixel près.

Ce n’était pas nécessaire.

---

Mais ils devaient tous référencer la même fenêtre de données.

---

Il ajouta :

**AUDIO_FRAME_ID**

**WINDOW_START**

**WINDOW_END**

---

Maintenant, quand Brutus voyait une ellipse étrange dans le scope, il pouvait cliquer.

---

Le Journal Vivant ouvrait exactement le segment audio correspondant.

---

L/R.

M/S.

Polar.

Même intervalle.

---

Brutus écrivit :

**VISUAL ANOMALY MUST LINK BACK TO SOURCE DATA.**

---

Très important.

---

Une jolie forme n’était plus une fin.

Elle devenait une porte d’inspection.

---

Il vit soudain un rayon très grand.

---

Le graphique fit un saut.

---

Brutus cliqua.

---

Un transitoire audio.

Rien d’étrange.

---

La magnitude géométrique avait simplement augmenté.

---

Il écrivit :

**LARGE RADIUS ≠ ANOMALY BY ITSELF.**

---

Le contexte temporel comptait.

---

Puis il remarqua une série d’angles qui semblaient sauter de \(\pi\) à \(-\pi\).

---

Au premier regard :

discontinuité.

---

Mais c’était simplement la frontière de branche.

---

Même direction voisine.

Deux représentations numériques autour du wrap.

---

Brutus écrivit :

**ANGLE WRAP ≠ PHYSICAL JUMP.**

---

Excellent.

---

Il créa une option :

**UNWRAPPED ANGLE VIEW**

pour certaines analyses temporelles.

---

Mais avec un avertissement.

---

L’unwrapping était une transformation interprétative.

---

Il ajouta :

**RAW_ANGLE**

et

**UNWRAPPED_ANGLE**

séparément.

---

Brutus écrivit :

**POSTPROCESSING MUST NOT OVERWRITE RAW MEASUREMENT.**

---

Encore le Journal Vivant.

---

Le passé brut.

Puis la vue dérivée.

---

Il regarda les courbes.

---

L’angle brut sautait.

L’angle déroulé semblait continu.

---

Même données.

Deux vues.

---

Le système devait conserver les deux.

---

Brutus pensa aux fréquences.

---

Si l’angle variait dans le temps, on pourrait étudier sa dynamique.

---

Mais là encore :

une nouvelle métrique.

Un nouveau contrat.

---

Il n’allait pas tout faire dans le même chapitre.

---

Il nota simplement :

**ANGULAR DYNAMICS — FUTURE TEST.**

---

Puis il pensa au mot deux voix.

---

Pourquoi deux voix ?

---

Parce que gauche et droite pouvaient être vus comme deux signaux.

Mais Mid et Side aussi formaient une paire.

---

Et désormais rayon-angle formaient encore une autre paire.

---

Trois couples de coordonnées.

---

\[
(L,R)
\]

\[
(M,S)
\]

\[
(r,\theta)
\]

---

Brutus les plaça en colonne.

---

Il écrivit :

**THREE REPRESENTATIONS. ONE UNDERLYING SAMPLE PAIR.**

---

Puis se corrigea légèrement.

---

\(r,\theta\) au point zéro avait une ambiguïté angulaire.

Et les représentations flottantes introduisaient une tolérance.

---

Il ajouta :

**EQUIVALENT UNDER DECLARED DOMAIN AND NUMERIC CONTRACT.**

---

Voilà.

---

Les nuances étaient devenues automatiques.

---

Brutus construisit le pipeline complet.

---

**L/R INPUT**

↓

**M/S TRANSFORM**

↓

**POLAR DERIVATION**

↓

**VISUALIZATION**

↓

**INVERSE POLAR CHECK**

↓

**M/S**

↓

**INVERSE M/S**

↓

**L/R CHECK**

---

Une chaîne complète.

---

Il écrivit :

**TWO ROUNDTRIPS.**

---

Polar roundtrip.

Puis Mid/Side roundtrip.

---

L’objectif :

localiser une éventuelle erreur.

---

Si polar → MS échouait :

problème dans la conversion polaire ou la précision.

---

Si MS → LR échouait :

problème dans la transformation stéréo.

---

Brutus écrivit :

**COMPOSED ROUNDTRIP MUST RETAIN LOCAL CHECKPOINTS.**

---

Sinon une erreur à une étape pouvait être attribuée à la mauvaise couche.

---

Le système lança.

---

L/R input.

---

M/S.

PASS.

---

Polar.

PASS.

---

Inverse polar.

Within tolerance.

---

Inverse M/S.

Within expected contract.

---

Final L/R.

PASS.

---

Brutus sourit.

---

Le trajet entier fonctionnait sur ce cas.

---

Mais il refusa d’afficher :

**SYSTEM PROVEN.**

---

Il écrivit :

**COMPOSED ROUNDTRIP PASSED CURRENT TEST CASE.**

---

Encore la portée.

---

Puis il lança des valeurs extrêmes.

---

Très petites amplitudes.

---

Près de zéro.

---

L’angle devenait numériquement sensible lorsque le rayon était minuscule.

---

Brutus observa.

---

Une très petite variation de M ou S pouvait produire une grande variation angulaire.

---

Pas nécessairement parce que le signal avait « tourné brutalement ».

Parce qu’à proximité de l’origine, la direction devient mal conditionnée.

---

Il écrivit :

**ANGLE BECOMES UNSTABLE AS RADIUS APPROACHES ZERO.**

---

Voilà une propriété importante pour l’interface.

---

Un angle affiché avec grande confiance lorsque \(r\) était presque zéro serait trompeur.

---

Brutus ajouta :

**ANGLE_CONFIDENCE_STATE**

---

Pas une probabilité statistique inventée.

Un état basé sur un seuil ou une politique déclarée.

---

VALID.

LOW_MAGNITUDE.

UNDEFINED.

---

Si :

\[
r<\varepsilon
\]

selon un seuil préengagé,

l’interface pouvait dire :

**LOW MAGNITUDE — ANGLE INTERPRETATION UNSTABLE.**

---

Brutus écrivit :

**DO NOT OVERINTERPRET DIRECTION WHEN MAGNITUDE VANISHES.**

---

Cette phrase allait sûrement revenir ailleurs.

---

Le laboratoire n’avait plus seulement des nombres.

Il avait une notion de qualité de représentation.

---

Brutus conserva le rayon.

Même quand l’angle devenait instable.

---

Il ne cachait pas le point.

Il signalait seulement la limite.

---

Puis il observa quelque chose.

---

Lorsque les deux voix se ressemblaient fortement, Side devenait faible.

Le vecteur se rapprochait de l’axe Mid.

---

Lorsqu’elles divergeaient davantage, Side prenait de l’importance.

---

Cela suggérait un lien avec une mesure plus générale de similarité entre les canaux.

---

Brutus pensa au mot :

**corrélation.**

---

Il ne l’écrivit pas encore comme verdict.

---

Seulement comme prochaine question.

---

Un rayon et un angle décrivaient un instant.

Mais pour savoir si deux signaux avaient tendance à évoluer ensemble dans une fenêtre temporelle, il fallait quelque chose d’autre.

---

Une statistique.

---

Et cette statistique devait distinguer :

niveau,

phase,

relation temporelle,

durée de fenêtre.

---

Brutus écrivit :

**INSTANT GEOMETRY ≠ TEMPORAL DEPENDENCE.**

---

Voilà la frontière du chapitre.

---

Le rayon et l’angle étaient prêts.

Mais ils ne pouvaient pas répondre seuls à la question :

**est-ce que les deux voix évoluent ensemble ?**

---

Brutus ferma le scope.

---

Il sauvegarda :

**DAAT POLAR VIEW v1.**

---

Puis ajouta les invariants :

**ANGLE UNIT MUST BE DECLARED.**

**ANGLE BRANCH MUST BE DECLARED.**

**ORIGIN HAS NO UNIQUE DIRECTION.**

**ANGLE WRAP ≠ PHYSICAL JUMP.**

**M/S ANGLE ≠ PHYSICAL SOURCE ANGLE.**

**LOW RADIUS → DIRECTION BECOMES NUMERICALLY FRAGILE.**

**VISUALIZATION ≠ CAUSAL EXPLANATION.**

---

Il relut.

---

Puis ajouta une dernière ligne :

**TWO VOICES CAN BE DRAWN AS ONE VECTOR WITHOUT BECOMING ONE VOICE.**

---

Brutus sourit.

---

Voilà le titre entier résumé.

---

Deux voix.

Un rayon.

Un angle.

---

Pas une fusion.

Une représentation.

---

Puis il regarda les deux signaux sur la durée.

Ils semblaient parfois avancer ensemble.

Parfois se séparer.

Parfois revenir.

---

Un point instantané ne suffisait plus.

---

Il allait falloir mesurer leur relation à travers le temps.

---

Brutus ouvrit une nouvelle page.

Il écrivit :

**HURST**

Puis :

**CROSS**

---

Il s’arrêta.

---

Une autre transformation l’attendait.

Pas une simple géométrie.

Cette fois, il faudrait être extrêmement prudent avec ce que signifiait réellement une dépendance mesurée.

---

Il inscrivit le titre :

**LE HURST CROISÉ.**

Puis sauvegarda.

---

Le miroir de Da’at avait donné deux coordonnées.

La géométrie en avait fait un rayon et un angle.

Mais le temps allait poser une question plus difficile :

quand deux voix semblent avancer ensemble, **quelle partie de cette ressemblance survit réellement à la mesure ?**
