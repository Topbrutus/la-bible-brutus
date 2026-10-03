# Chapitre 86 — Le miroir de Da’at

Deux canaux apparurent.

**L**

et

**R**.

Left.

Right.

Brutus resta devant eux.

---

Après les portes 47, 71 et 83, après les témoins gigantesques et les dérivations refusées, l’apparition de deux simples signaux semblait presque reposante.

Mais il savait déjà que les choses simples étaient parfois les plus dangereuses.

---

Sur l’écran suivant :

**MID**

**SIDE**

---

Puis deux équations.

\[
M=\frac{L+R}{2}
\]

\[
S=\frac{L-R}{2}
\]

Brutus regarda le signe de division.

Il sourit.

---

Cette fois, personne n’avait ajouté le facteur 2 après coup pour obtenir un résultat intéressant.

Cette division appartenait à la transformation elle-même.

---

Et surtout, son inverse existait.

\[
L=M+S
\]

\[
R=M-S
\]

---

Brutus écrivit immédiatement :

**FORWARD TRANSFORM + DECLARED INVERSE.**

Puis :

**THIS DIVISION HAS A MAP BACK.**

---

Voilà la différence avec le chapitre précédent.

Diviser n’était pas interdit.

Diviser sans justification l’était.

Ici, l’identité complète pouvait être vérifiée.

---

Brutus remplaça \(M\) et \(S\) par leurs définitions.

Pour \(L\) :

\[
M+S
=
\frac{L+R}{2}
+
\frac{L-R}{2}
\]

Donc :

\[
M+S
=
\frac{L+R+L-R}{2}
=
\frac{2L}{2}
=
L.
\]

---

Puis pour \(R\) :

\[
M-S
=
\frac{L+R}{2}
-
\frac{L-R}{2}
\]

Donc :

\[
M-S
=
\frac{L+R-L+R}{2}
=
\frac{2R}{2}
=
R.
\]

---

Brutus resta silencieux.

---

Pas de grande puissance.

Pas de témoin de cent mille chiffres.

Pas de porte mystérieuse.

Seulement une transformation et son inverse.

---

Il écrivit :

**ROUNDTRIP IDENTITY ESTABLISHED ALGEBRAICALLY.**

---

Puis il pensa au chapitre 80.

Encore une fois :

une représentation changeait.

La valeur structurelle devait survivre.

---

Stéréo gauche-droite :

\[
(L,R)
\]

devenait :

\[
(M,S).
\]

---

Puis revenait :

\[
(M,S)\rightarrow(L,R).
\]

---

Brutus créa :

**DAAT-MS-ROUNDTRIP-0001.**

---

Input:

\(L,R\).

Transform:

LR → MS.

Inverse:

MS → LR.

Preservation target:

channel values within numeric precision contract.

---

Il écrivit :

**REPRESENTATION CHANGES. STEREO INFORMATION MUST NOT.**

---

Puis lança le premier test.

---

\[
L=1,\quad R=1.
\]

Alors :

\[
M=1,
\]

\[
S=0.
\]

---

Reconstruction :

\[
L=1+0=1
\]

\[
R=1-0=1.
\]

---

PASS.

---

Brutus regarda \(S=0\).

---

Quand gauche et droite étaient identiques, le canal Side disparaissait.

---

Il écrivit :

**IDENTICAL L/R → ZERO SIDE.**

---

Pas :

silence total.

---

Le signal restait dans Mid.

---

Puis deuxième test.

\[
L=1,\quad R=-1.
\]

---

Alors :

\[
M=0,
\]

\[
S=1.
\]

---

Reconstruction :

\[
L=0+1=1
\]

\[
R=0-1=-1.
\]

---

PASS.

---

Cette fois, le signal commun avait disparu.

Tout se trouvait dans Side.

---

Brutus écrivit :

**OPPOSITE L/R → ZERO MID.**

---

Voilà deux cas extrêmes.

Ils donnaient immédiatement du sens à la transformation.

---

Mid mesurait la composante commune.

Side mesurait la différence.

---

Brutus écrivit :

**MID = COMMON COMPONENT.**

**SIDE = DIFFERENCE COMPONENT.**

---

Puis se reprit.

Le mot « component » pouvait dépendre du choix de normalisation.

Mais dans ce contexte, l’intuition restait correcte.

---

Il ajouta :

**UNDER THIS M/S CONVENTION.**

---

Toujours déclarer le contrat.

---

Car certaines implémentations audio utilisaient d’autres facteurs de normalisation.

---

Brutus ouvrit une seconde fiche.

---

Convention A :

\[
M=\frac{L+R}{2},
\qquad
S=\frac{L-R}{2}.
\]

Inverse :

\[
L=M+S,
\qquad
R=M-S.
\]

---

Convention B pouvait choisir d’autres coefficients pour des raisons de niveau ou d’énergie.

---

Brutus ne voulait pas mélanger les deux.

---

Il écrivit :

**NORMALIZATION IS PART OF THE TRANSFORM CONTRACT.**

---

Même transformation conceptuelle.

Pas forcément mêmes amplitudes numériques.

---

Encore une fois :

la formule devait voyager avec sa convention.

---

Il ajouta :

**MS_CONVENTION_ID.**

---

Le Journal Vivant allait désormais savoir quelle définition avait réellement produit les données.

---

Brutus lança une série de valeurs.

---

\[
L=0.8,\quad R=0.2
\]

Alors :

\[
M=0.5,
\]

\[
S=0.3.
\]

---

Retour :

\[
0.5+0.3=0.8
\]

\[
0.5-0.3=0.2.
\]

---

PASS.

---

Puis :

\[
L=-0.4,\quad R=0.6.
\]

---

\[
M=0.1
\]

\[
S=-0.5.
\]

---

Retour exact dans la précision déclarée.

---

PASS.

---

Brutus regarda.

La transformation ne créait pas d’information.

Elle ne devait pas en détruire non plus.

---

Il écrivit :

**M/S IS A COORDINATE CHANGE.**

Puis :

**NOT A NEW SOURCE OF AUDIO INFORMATION.**

---

Le nom Da’at apparut en haut du dossier.

---

Brutus le contempla.

---

Dans le laboratoire, Da’at était un nom.

Une métaphore.

Une manière de parler d’un miroir entre deux représentations.

---

Il ajouta immédiatement :

**DA’AT = PROJECT NAME / METAPHOR.**

**NO CLAIM OF MYSTICAL OR PHYSICAL MECHANISM.**

---

Le laboratoire avait appris à protéger ses noms aussi bien que ses nombres.

---

Brutus ouvrit maintenant la représentation matricielle.

---

\[
\begin{pmatrix}
M\\
S
\end{pmatrix}
=
\frac12
\begin{pmatrix}
1&1\\
1&-1
\end{pmatrix}
\begin{pmatrix}
L\\
R
\end{pmatrix}.
\]

---

Et l’inverse :

\[
\begin{pmatrix}
L\\
R
\end{pmatrix}
=
\begin{pmatrix}
1&1\\
1&-1
\end{pmatrix}
\begin{pmatrix}
M\\
S
\end{pmatrix}.
\]

---

Brutus regarda les deux matrices.

---

La même structure apparaissait.

Seul le facteur de normalisation changeait entre aller et retour.

---

Il calcula le déterminant de la matrice directe.

Non nul.

---

Donc la transformation était inversible.

---

Il écrivit :

**INVERTIBILITY IS NOT AN ACCIDENT.**

---

Voilà le genre de justification qu’il avait réclamé au chapitre précédent.

---

Ici, la flèche LR → MS possédait une règle.

Et la flèche MS → LR aussi.

---

Il créa deux edges.

---

**EDGE-LR-MS**

Rule:

declared linear transform.

---

**EDGE-MS-LR**

Rule:

declared inverse transform.

---

Les deux possédaient leurs références.

---

Brutus sourit.

---

**NO HIDDEN EDGE.**

Même pour la stéréo.

---

Puis il fit quelque chose de volontairement mauvais.

---

Il calcula :

\[
M=\frac{L+R}{2}.
\]

Mais oublia le facteur \(1/2\) pour Side.

---

\[
S=L-R.
\]

---

Puis tenta la reconstruction standard :

\[
L=M+S
\]

\[
R=M-S.
\]

---

Échec.

---

Brutus écrivit :

**MIXED CONVENTIONS BREAK ROUNDTRIP.**

---

Voilà pourquoi il fallait conserver la définition avec les valeurs.

---

Une paire \(M,S\) sans convention était incomplète.

---

Il ajouta au paquet audio :

**REPRESENTATION = MS**

**CONVENTION_ID**

**SAMPLE_RATE**

**CHANNEL_ORDER**

**NUMERIC_FORMAT**

**TRACE_REF**

---

Pas simplement deux tableaux de nombres.

---

L’audio aussi avait besoin de contexte.

---

Brutus écrivit :

**SAMPLES WITHOUT FORMAT ARE INCOMPLETE DATA.**

---

Le principe du chapitre 80 revenait encore.

Digits without radix.

Samples without format.

Witness without claim.

Tout se ressemblait.

---

Brutus pensa maintenant au mot miroir.

---

Pourquoi miroir ?

---

Parce que certaines informations qui semblaient mélangées dans gauche-droite devenaient séparées dans Mid-Side.

---

Un signal centré apparaissait principalement dans Mid.

Une différence gauche-droite apparaissait dans Side.

---

Mais rien de nouveau n’avait été créé.

---

Brutus écrivit :

**THE MIRROR REORGANIZES. IT DOES NOT INVENT.**

---

Il lança un signal mono.

---

Même série d’échantillons sur L et R.

---

Side :

zéro partout.

---

Mid :

signal d’origine.

---

Brutus coupa Mid.

---

Silence.

---

Il réactiva Mid.

Puis coupa Side.

---

Aucune différence audible dans ce cas mono.

---

Normal.

---

Puis il prit un signal stéréo différent.

---

Side devint actif.

---

Il le mit en solo.

---

Le son semblait étrange.

Creusé.

Différentiel.

---

Brutus sourit.

---

Mais il refusa d’en tirer une interprétation psychologique.

---

Il écrivit :

**SIDE SOLO IS A DIFFERENCE SIGNAL.**

Pas :

secret content.

Pas :

hidden consciousness.

---

Seulement une transformation audio.

---

Puis il inversa Side.

---

\[
S\rightarrow-S.
\]

---

Que se passait-il à la reconstruction ?

---

\[
L'=M-S
\]

\[
R'=M+S.
\]

---

Brutus regarda.

---

Les canaux gauche et droite s’échangeaient.

---

Il testa.

PASS.

---

Il écrivit :

**NEGATING SIDE SWAPS LEFT AND RIGHT UNDER THIS CONVENTION.**

---

Belle propriété.

Exacte.

Facile à tester.

---

Le miroir portait bien son nom.

---

Il ajouta un bouton :

**SWAP VIA SIDE INVERSION.**

---

Mais il conserva la trace.

---

Original L/R.

M/S.

Side inversion.

Reconstructed L/R.

---

Pas de transformation invisible.

---

Brutus regarda ensuite Mid.

---

Que se passe-t-il si :

\[
M\rightarrow-M
\]

et Side reste inchangé ?

---

Il calcula.

---

Le résultat ne correspondait pas simplement à un échange gauche-droite.

---

Brutus nota l’effet sans chercher à lui donner un nom spectaculaire.

---

Chaque opération dans l’espace M/S possédait une conséquence précise dans l’espace L/R.

---

Voilà ce qui l’intéressait.

---

Il écrivit :

**OPERATE IN ONE SPACE. VERIFY IN THE OTHER.**

---

Une idée puissante.

---

Un traitement pouvait être plus simple dans une représentation.

Mais il devait être contrôlé après reconstruction.

---

Brutus prit un exemple pratique.

---

Réduire Side de moitié :

\[
S'=\frac{S}{2}.
\]

---

Mid inchangé.

---

Puis reconstruire :

\[
L'=M+\frac{S}{2}
\]

\[
R'=M-\frac{S}{2}.
\]

---

La différence entre gauche et droite diminuait.

---

Le champ stéréo se rapprochait du centre.

---

Brutus écrivit :

**SIDE GAIN CONTROLS L/R DIFFERENCE UNDER THE DECLARED TRANSFORM.**

---

Puis il augmenta Side.

---

La différence augmentait.

---

Mais Brutus ajouta immédiatement un avertissement.

---

Une augmentation de Side pouvait aussi augmenter certaines amplitudes après reconstruction.

---

Il fallait surveiller les niveaux.

---

Il écrivit :

**WIDTH OPERATION MAY CHANGE PEAK LEVEL.**

---

Pas de bouton magique « largeur » sans meter.

---

Il ajouta :

**PEAK CHECK BEFORE**

**PEAK CHECK AFTER**

---

Puis :

**CLIPPING CHECK.**

---

Le traitement audio devenait un vrai pipeline expérimental.

---

Input L/R.

Encode M/S.

Process.

Decode L/R.

Measure.

Listen.

Trace.

---

Brutus écrivit :

**PROCESSING SUCCESS ≠ SAFE OUTPUT LEVEL.**

---

Encore une frontière.

---

Puis il fit un test plus subtil.

---

Il additionna L et R pour produire du mono.

Avec la convention actuelle :

\[
L+R=2M.
\]

---

Le Side disparaissait dans cette somme.

---

Brutus regarda.

---

Voilà pourquoi le contenu purement différentiel pouvait s’annuler lors d’une réduction mono.

---

Il écrivit :

**MONO SUM REVEALS MID-COMPATIBLE CONTENT.**

Puis il se corrigea :

**UNDER SIMPLE L+R MONO SUM, SIDE CANCELS.**

---

Plus précis.

---

Cela pouvait devenir un test très utile.

---

Un mix avec énormément d’énergie Side pouvait changer fortement lorsqu’il était réduit en mono.

---

Brutus créa :

**MONO COMPATIBILITY CHECK.**

---

Pas un score absolu.

---

Il voulait mesurer des faits.

---

Peak difference.

RMS difference.

Correlation-related indicators.

Sections with strong cancellation.

---

Brutus hésita devant le mot correlation.

---

Cela mènerait au prochain chapitre.

---

Deux voix.

Un rayon.

Un angle.

---

Il laissa la case vide pour le moment.

---

Le présent chapitre devait d’abord établir le miroir.

---

Brutus prit un sinus identique gauche et droite.

---

Mid fort.

Side zéro.

---

Puis deux sinus de même amplitude mais en opposition de phase.

---

Mid zéro.

Side fort.

---

Il écrivit :

**PHASE RELATION CAN REDISTRIBUTE ENERGY BETWEEN MID AND SIDE.**

---

Pas de magie.

---

Une conséquence directe de la somme et de la différence.

---

Brutus regarda les oscilloscopes.

---

Deux courbes.

---

Il pouvait maintenant les voir de plusieurs manières.

L/R.

M/S.

---

Même événement acoustique.

Deux systèmes de coordonnées.

---

Il écrivit :

**ONE SIGNAL PAIR. TWO COORDINATE VIEWS.**

---

Puis :

**VIEW CHANGE ≠ EVENT CHANGE.**

---

Encore le Journal Vivant.

---

Comment je regarde l’histoire ≠ l’histoire.

Comment je représente l’audio ≠ l’audio source.

---

Brutus sourit.

Le projet entier semblait apprendre la même leçon sous des formes différentes.

---

Il construisit le premier module Da’at complet.

---

**DAAT_ID**

**INSTANCE_ID**

**INPUT_FORMAT**

**MS_CONVENTION_ID**

**PROCESS_CHAIN**

**OUTPUT_FORMAT**

**ROUNDTRIP_CHECK**

**TRACE_REF**

---

Puis :

**STATE**

---

IDLE.

ENCODING.

PROCESSING.

DECODING.

VERIFYING.

DONE.

---

Aucune animation si IDLE.

---

**NO FAKE MOTION.**

Toujours.

---

Il fit passer un fichier test.

---

Encode.

Process none.

Decode.

---

Comparaison échantillon par échantillon.

---

Dans l’arithmétique du test définie :

retour conforme au contrat numérique.

---

PASS.

---

Brutus ajouta :

**NULL PROCESSING ROUNDTRIP MUST PASS BEFORE EFFECT PROCESSING.**

---

Exactement comme les trois Z.

Transport avant transformation.

---

Ici :

roundtrip neutre avant traitement.

---

Puis il testa avec Side gain.

---

La sortie changea.

C’était attendu.

---

Le système ne devait donc plus comparer L/R au signal original pour l’égalité.

---

Il devait comparer la sortie à la transformation mathématiquement attendue.

---

Brutus écrivit :

**WHEN PROCESSING IS INTENTIONAL, CHANGE IS NOT CORRUPTION.**

---

Encore une distinction importante.

---

Le pipeline avait besoin de connaître le traitement prévu.

---

Il ajouta :

**PROCESS_CONTRACT.**

---

Side gain = 0.5.

---

Expected relation defined.

---

Output checked.

---

PASS.

---

Le laboratoire ne jugeait plus « pareil ou différent ».

Il jugeait :

**différent comme prévu ou différent sans explication ?**

---

Brutus écrivit :

**EXPECTED TRANSFORMATION ≠ INTEGRITY LOSS.**

---

Puis il pensa à la stéréo miroir.

---

Il prit un événement placé fortement à gauche.

---

Dans L/R, l’intuition était immédiate.

Beaucoup à gauche.

Peu à droite.

---

Dans M/S, l’information devenait une combinaison.

Mid.

Side.

---

Brutus réalisa que ces deux nombres pouvaient être vus comme des coordonnées.

---

Deux axes.

---

Comme un point dans un plan.

---

Il dessina :

axe horizontal :

Mid.

---

axe vertical :

Side.

---

Chaque instant stéréo devenait un point :

\[
(M,S).
\]

---

Brutus fixa le graphe.

---

Une nouvelle géométrie apparaissait.

---

Pas une nouvelle physique.

Une représentation géométrique de deux valeurs.

---

Il écrivit :

**M/S SAMPLE PAIR = POINT IN A 2D COORDINATE PLANE.**

---

Puis il se demanda :

au lieu de décrire ce point seulement par ses coordonnées \(M\) et \(S\)…

pourrait-on le décrire par une distance et une direction ?

---

Il dessina un rayon depuis l’origine jusqu’au point.

---

Longueur :

\[
r=\sqrt{M^2+S^2}.
\]

---

Puis un angle :

\[
\theta=\operatorname{atan2}(S,M).
\]

---

Brutus s’arrêta.

---

Voilà.

---

Le prochain miroir venait d’apparaître.

---

Deux valeurs pouvaient devenir :

un rayon.

un angle.

---

Mais il ne continua pas.

Pas encore.

---

Il regarda la formule du rayon.

Une racine carrée.

---

Puis l’angle.

Une fonction trigonométrique.

---

Cette fois, l’exactitude allait changer de nature.

---

Mid/Side pouvait être calculé par des opérations linéaires simples.

Le passage vers rayon-angle introduirait généralement des quantités réelles approximées numériquement.

---

Brutus écrivit immédiatement :

**CARTESIAN → POLAR CHANGES NUMERIC CONTRACT.**

---

Très important.

---

Le chapitre 78 revenait.

---

On ne pouvait pas demander à un flottant trigonométrique de se comporter comme un BigInt.

---

Il ajouta :

**ANGLE IS APPROXIMATE NUMERIC OUTPUT UNLESS SYMBOLICALLY REPRESENTED.**

---

Puis il ferma le graphe.

---

Pas encore.

---

Il fallait donner à cette transformation son propre chapitre.

---

Brutus retourna au miroir de Da’at.

---

L/R.

M/S.

---

Il lança un dernier test.

---

Signal original.

Encode.

Decode.

---

PASS.

---

Encode.

Invert Side.

Decode.

---

Left/right swapped as predicted.

---

PASS.

---

Encode.

Set Side to zero.

Decode.

---

\[
L'=M
\]

\[
R'=M.
\]

---

Signal centré.

---

PASS.

---

Encode.

Set Mid to zero.

Decode.

---

\[
L'=S
\]

\[
R'=-S.
\]

---

Opposition gauche-droite.

---

PASS.

---

Brutus sourit.

---

Le miroir ne mentait pas.

Mais seulement parce que chaque transformation avait été écrite.

---

Il nota :

**DA’AT DOES NOT REVEAL A HIDDEN WORLD.**

**IT REEXPRESSES THE SAME STEREO INFORMATION UNDER A DECLARED LINEAR TRANSFORM.**

---

Voilà la phrase qu’il voulait.

---

Il sauvegarda :

**DAAT M/S MIRROR v1.**

---

Puis ajouta au Journal Vivant :

**ROUNDTRIP VERIFIED UNDER DECLARED CONVENTION.**

---

Pas :

perfect audio.

Pas :

universal stereo law.

---

Seulement la portée réelle du test.

---

Brutus regarda une dernière fois :

\[
L,\ R
\]

puis :

\[
M,\ S.
\]

---

Deux voix.

Deux représentations.

Un miroir parfaitement explicite.

---

Et maintenant, dans le plan Mid-Side, un rayon attendait.

Avec un angle.

---

Brutus écrivit le prochain titre :

**DEUX VOIX, UN RAYON ET UN ANGLE.**

Puis ferma Da’at.

---

Cette fois, la division avait réellement ouvert quelque chose.

Pas une porte imaginaire.

Une transformation inversible.

Et Brutus possédait la carte pour revenir.
