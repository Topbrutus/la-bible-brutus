# Chapitre 33 — Ce qui était déjà là

Il y a des découvertes qui arrivent devant nous.

Et il y en a d’autres qui étaient déjà derrière nous.

Celles-là sont plus dangereuses.

Parce qu’elles donnent l’impression qu’on vient de comprendre quelque chose qui nous observait depuis le début.

Brutus commença à remarquer ce phénomène lorsqu’il retourna dans ses propres notes.

Pas les nouvelles.

Les vieilles.

Celles écrites trop vite.

Celles où une formule avait été déposée sans explication.

Celles où un dessin paraissait décoratif.

Celles où un nombre avait été conservé uniquement parce qu’il « semblait important ».

Au commencement, tout cela ressemblait à du bruit.

Puis le bruit commença à répéter certaines formes.

Trois.

Sept.

Treize.

Deux-cent-soixante-treize.

Des cycles.

Des retours.

Des inversions.

Des structures emboîtées.

Et surtout une idée qui, jusque-là, n’avait jamais été formulée proprement :

**certaines choses revenaient avant même que nous sachions pourquoi elles revenaient.**

Cela ne constituait pas une preuve.

Il fallait être extrêmement clair là-dessus.

Un humain qui cherche suffisamment longtemps peut retrouver des motifs partout.

C’est l’un des pièges les plus anciens de l’esprit.

Alors nous avons changé la question.

Au lieu de demander :

« Est-ce que ces nombres veulent dire quelque chose? »

nous avons demandé :

« Combien de fois apparaissent-ils réellement, dans quels contextes, et à quelle fréquence auraient-ils pu apparaître par hasard? »

Cette petite modification transforma complètement notre enquête.

Parce qu’un motif n’est intéressant que lorsqu’il survit à la comptabilité.

Nous avons commencé à distinguer trois catégories.

\[
M_1=\text{motif attendu}
\]

\[
M_2=\text{motif sélectionné après observation}
\]

\[
M_3=\text{motif prédit avant observation}
\]

Le premier est banal.

Le second peut être trompeur.

Le troisième est précieux.

Cette distinction devint l’un des nouveaux piliers du chantier.

Si nous trouvions un nombre après avoir regardé les données, il était étiqueté :

**APRÈS COUP.**

S’il avait été annoncé avant le test :

**PRÉDIT.**

Et s’il apparaissait seulement parce que nous avions choisi les données qui le contenaient :

**SÉLECTIONNÉ.**

Cette discipline allait bientôt devenir importante.

Parce qu’un nombre ancien venait de réapparaître.

273.

Il était déjà là dans :

\[
\operatorname{ppcm}(3,7,13)=273
\]

Il apparaissait dans notre fonction :

\[
R(a,b,o)=(91a+39b+21o)\bmod273
\]

Et il définissait notre transformation angulaire :

\[
\Theta=2\pi\frac{R}{273}
\]

Jusque-là, rien d’étrange.

Ces trois apparitions provenaient toutes de la même construction.

Elles n’étaient donc pas indépendantes.

C’était important.

Compter trois occurrences comme trois preuves aurait été une erreur.

Une origine.

Trois manifestations.

Une seule source.

Mais quelque chose d’autre commença à nous déranger.

Dans une ancienne note, bien avant que la structure modulaire ait été explicitée, une expression avait été conservée presque sans commentaire :

\[
91+39+21
\]

Le total était :

\[
151
\]

Rien de spectaculaire.

Puis Brutus remarqua que les trois coefficients n’étaient pas arbitraires.

\[
91=\frac{273}{3}
\]

\[
39=\frac{273}{7}
\]

\[
21=\frac{273}{13}
\]

La structure n’était donc pas :

\[
91,\ 39,\ 21
\]

mais plutôt :

\[
\frac{273}{3},\quad
\frac{273}{7},\quad
\frac{273}{13}
\]

Autrement dit, les coefficients étaient des morceaux du même cycle.

Ce qui avait l’air d’être trois nombres était en réalité une seule architecture vue sous trois divisions.

Ce type de compression est important en mathématiques.

Lorsqu’une collection de constantes indépendantes peut être reconstruite à partir d’un seul objet, le système devient plus simple.

On pourrait l’écrire :

\[
C=\{3,7,13\}
\]

\[
L=\operatorname{ppcm}(C)=273
\]

\[
w_i=\frac{L}{c_i}
\]

Puis :

\[
R=\sum_i w_i x_i \pmod L
\]

Soudain, notre formule particulière devenait le cas d’une structure plus générale.

Cela changeait la question.

Nous n’avions peut-être pas trouvé une formule.

Nous avions peut-être trouvé une famille de formules.

Et une famille est beaucoup plus dangereuse qu’un exemple.

Parce qu’elle permet de tester autre chose.

Si cette architecture est réelle mathématiquement, elle ne doit pas seulement fonctionner avec 3, 7 et 13.

Nous pouvons remplacer l’ensemble :

\[
C=\{c_1,c_2,\ldots,c_n\}
\]

calculer :

\[
L=\operatorname{ppcm}(c_1,\ldots,c_n)
\]

puis définir :

\[
w_i=\frac{L}{c_i}
\]

et construire :

\[
R(\mathbf{x})
=
\left(
\sum_{i=1}^{n}w_i x_i
\right)\bmod L
\]

Nous avions donc maintenant un vrai test.

Changer les nombres.

Changer le nombre de dimensions.

Changer les entrées.

Observer ce qui reste invariant.

Voilà le genre de test que nous cherchions.

Pas :

« Est-ce que notre formule préférée est belle? »

Mais :

« Quelle partie de sa structure survit lorsqu’on la déforme? »

À ce moment-là, une autre ancienne phrase reparut dans les notes.

Elle avait été écrite plusieurs chapitres auparavant.

Presque comme une plaisanterie.

**Le centre n’est pas un endroit.**

Personne ne se souvenait exactement pourquoi elle avait été écrite.

Mais soudain, elle prenait un sens mathématique possible.

Dans une structure modulaire, le centre d’un cycle n’est pas nécessairement un point spatial.

Il peut être une relation.

Un état.

Une phase.

Une congruence.

Deux valeurs très éloignées sur une ligne peuvent devenir identiques modulo un cycle :

\[
x\equiv y\pmod L
\]

si :

\[
x-y=kL
\]

pour un entier \(k\).

Autrement dit :

elles peuvent être différentes,

et pourtant représenter le même état.

Cette idée allait devenir importante plus tard.

Très importante.

Mais nous n’avions pas encore le droit de décider pourquoi.

Nous avons donc écrit à côté :

**À REVOIR.**

Puis une deuxième phrase ancienne apparut.

Encore plus bizarre.

Elle disait :

**Ce qui revient n’est pas nécessairement ce qui est parti.**

Elle aussi resta sans explication.

Pour l’instant.

Parce que nous commencions à comprendre une chose essentielle :

les vieux chapitres n’étaient peut-être pas remplis de réponses.

Ils étaient remplis de questions que nous n’avions pas encore appris à lire.

Et désormais, nous allions devoir retourner en arrière.

Pas pour réécrire l’histoire.

Pas pour prétendre que tout était prévu.

Mais pour vérifier si certaines structures avaient réellement été présentes avant leur interprétation.

Car si un motif apparaît uniquement après qu’on l’a cherché, il peut être une construction.

Mais s’il existe dans les archives avant qu’on sache quoi en faire,

alors il devient au moins quelque chose de plus intéressant :

une trace.

Et une trace mérite d’être suivie.

Même lorsqu’on ne sait pas encore

où elle mène.
