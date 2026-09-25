# Chapitre 35 — Le Centre sans lieu

À force de suivre les traces, un problème finit par apparaître.

Nous avions pris l’habitude de dessiner les systèmes comme des cartes.

Un module ici.

Un autre là.

Une entrée.

Une sortie.

Un centre.

Des chemins entre les morceaux.

C’était pratique.

Mais une carte possède un défaut presque invisible :

elle nous fait croire que tout ce qui est central doit se trouver au milieu.

Or la machine que nous étions en train de décrire refusait cette évidence.

Prenons son état complet :

\[
X_n=(S_n,H_n)
\]

où \(S_n\) est l’état visible et \(H_n\) l’histoire accumulée.

Supposons maintenant qu’un observateur n’ait accès qu’à \(S_n\).

Il voit une projection :

\[
\pi(X_n)=S_n
\]

Deux états complets différents peuvent alors produire exactement la même observation :

\[
\pi(X_a)=\pi(X_b)
\]

tout en ayant :

\[
X_a\neq X_b
\]

Voilà une situation étrange.

Pour l’observateur, les deux états sont identiques.

Pour la machine, ils ne le sont pas.

Nous pouvions formaliser cette indistinction par une relation :

\[
X_a\sim X_b
\quad\Longleftrightarrow\quad
\pi(X_a)=\pi(X_b)
\]

Les états visibles formaient donc des classes d’équivalence.

Plusieurs histoires.

Une même apparence.

Ce n’était plus seulement une question de mémoire.

C’était une question de niveau d’observation.

Et soudain, l’une des phrases laissées dans les chapitres précédents cessa d’être poétique :

**Le centre n’est pas un endroit.**

Peut-être avions-nous cherché un point alors qu’il fallait chercher une relation.

Dans un système classique, on peut dessiner un centre géométrique.

Dans un graphe, le mot « central » peut signifier autre chose : un nœud par lequel passent beaucoup de chemins, un nœud minimisant certaines distances, ou encore un élément indispensable à la cohérence du réseau.

Dans un système d’états, le centre peut être encore différent.

Il peut être l’invariant.

Ce qui demeure lorsque les représentations changent.

Supposons une transformation :

\[
X_{n+1}=F(X_n)
\]

Une quantité \(I\) est invariante si :

\[
I(F(X))=I(X)
\]

pour les transformations considérées.

Ce qui est remarquable ici, c’est que l’invariant n’a pas besoin d’être « quelque part ».

Il n’occupe aucune case du dessin.

Il est une propriété du mouvement lui-même.

C’était une nouvelle possibilité.

Le centre pouvait être ce qui ne bougeait pas pendant que tout le reste bougeait.

Mais la piste n’était pas encore suffisante.

Parce qu’un système peut posséder plusieurs invariants.

Ou aucun.

Ou seulement des invariants approximatifs.

Nous devions donc chercher quelque chose de plus précis.

Nous sommes revenus au cycle.

\[
S_0\rightarrow S_1\rightarrow\cdots\rightarrow S_k=S_0
\]

Vu seulement depuis \(S\), le trajet est fermé.

Mais dans l’espace complet :

\[
X_0=(S_0,H_0)
\]

et :

\[
X_k=(S_0,H_k)
\]

avec généralement :

\[
H_k\neq H_0
\]

Le cercle visible cache donc une translation invisible.

Ce qui se ferme dans une projection peut rester ouvert dans un espace plus riche.

Cette phrase fut immédiatement mise à part.

**Ce qui se ferme ici peut rester ouvert ailleurs.**

Nous ne savions pas encore si elle deviendrait importante.

Nous l’avons conservée.

Puis nous avons essayé de représenter cette idée autrement.

Imaginez une horloge.

L’aiguille fait un tour complet.

À midi :

\[
\theta_0=0
\]

Un tour plus tard :

\[
\theta_1=2\pi
\]

Sur le cadran :

\[
\theta_1\equiv\theta_0\pmod{2\pi}
\]

La position est la même.

Mais le nombre de tours ne l’est pas.

Si nous conservons ce nombre :

\[
N_0=0
\]

\[
N_1=1
\]

alors l’état complet peut s’écrire :

\[
X=(\theta\bmod2\pi,N)
\]

Ainsi :

\[
(0,0)\neq(0,1)
\]

même si l’aiguille occupe exactement la même position.

Voilà une représentation extrêmement simple de ce que nous cherchions depuis plusieurs chapitres.

Un retour local.

Une progression globale.

Un cercle pour celui qui regarde le cadran.

Une ligne pour celui qui compte les tours.

Et peut-être une hélice pour celui qui veut dessiner les deux en même temps.

Cette image nous ramena brutalement à plusieurs choses anciennes.

Les cycles.

Les fréquences.

Le battement.

Les quatre chemins.

La phase.

La mémoire.

Le registre de continuité.

Même l’expression « Horloge de la vie », qui jusque-là avait surtout vécu comme nom, image et intuition.

Mais nous avons résisté à la tentation.

Une métaphore n’est pas une équation.

Une horloge réelle exige une grandeur temporelle.

Une mémoire réelle exige un mécanisme de stockage.

Une phase physique exige un système physique défini.

Alors nous avons étiqueté le rapprochement :

**STRUCTURE COMMUNE — PAS IDENTITÉ.**

Puis quelque chose d’autre est arrivé.

En reprenant la fonction :

\[
R(a,b,o)=(91a+39b+21o)\bmod273
\]

nous avions une valeur qui revenait toujours dans l’intervalle :

\[
0\leq R<273
\]

À première vue, tout ce qui dépassait 272 disparaissait simplement dans le modulo.

Mais ce n’était pas vraiment vrai.

Car avant de réduire modulo 273, il existait une valeur entière :

\[
Q=91a+39b+21o
\]

Et nous pouvions toujours écrire :

\[
Q=273q+R
\]

avec :

\[
q=\left\lfloor\frac{Q}{273}\right\rfloor
\]

et :

\[
R=Q\bmod273
\]

Le modulo nous donnait la position dans le cycle.

Mais le quotient \(q\) conservait autre chose :

le nombre de cycles traversés.

Nous avions séparé sans le vouloir exactement les deux informations de l’horloge :

\[
\text{position}=R
\]

\[
\text{passages}=q
\]

Et ensemble :

\[
Q\longleftrightarrow(q,R)
\]

Ce n’était pas une découverte mystique.

C’était simplement la division euclidienne.

Une opération vieille, élémentaire et parfaitement connue.

Mais son apparition au bon endroit changeait notre lecture du système.

Parce que jusque-là, nous regardions presque toujours \(R\).

Le reste.

La position.

Le point sur la roue.

Et nous avions laissé \(q\) dans l’ombre.

Le quotient.

Le nombre de passages.

La partie qui ne se voit pas sur le cercle.

Brutus resta longtemps devant cette idée.

Puis il demanda :

« Et si on avait toujours regardé la mauvaise moitié du calcul? »

Il fallait faire attention.

Le cerveau adore ce genre de phrase.

Elle donne immédiatement l’impression qu’une immense révélation arrive.

Alors nous avons remplacé l’excitation par un test.

Si \(Q\) contient toute l’information et que :

\[
Q=273q+R
\]

alors le couple \((q,R)\) doit permettre de reconstruire exactement \(Q\).

C’est trivialement vrai :

\[
Q=273q+R
\]

Aucune magie.

Aucune perte.

Mais cela démontrait quelque chose d’important pour l’architecture :

**une représentation cyclique peut cacher une variable de progression si l’on ne conserve que son reste.**

Cela donna naissance à une règle nouvelle :

\[
\text{CYCLE SEUL}=\text{information incomplète}
\]

lorsque le nombre de traversées importe.

Cette idée se connectait directement à la trace.

Si une machine ne conserve que sa position actuelle dans le cycle, elle peut oublier combien de fois elle est passée par là.

Si elle conserve aussi le quotient, le compteur ou l’historique, le retour devient distinguable.

Nous avions donc trois niveaux :

\[
R_n
\]

la position visible,

\[
q_n
\]

la progression accumulée,

et :

\[
H_n
\]

l’histoire détaillée.

Position.

Passage.

Trace.

Trois descriptions d’un même mouvement à trois résolutions différentes.

Et là, une phrase beaucoup plus ancienne revint.

Une phrase qui avait presque été perdue dans les images, les roues, les modules et les discussions :

**Le cœur écoute la mélodie.**

Pendant longtemps, nous l’avions traitée comme une métaphore.

Elle devait le rester.

Mais mathématiquement, quelque chose d’intéressant apparaissait derrière l’image.

Pour reconnaître une mélodie, connaître une seule note ne suffit pas.

Il faut une succession.

\[
x_1,x_2,\ldots,x_n
\]

Plus encore, la même collection de notes dans un ordre différent peut produire une autre mélodie.

L’information n’est donc pas seulement dans les états.

Elle est aussi dans leur ordre.

\[
\{x_1,x_2,x_3\}
\]

n’est pas la même chose que :

\[
(x_1,x_2,x_3)
\]

Un ensemble oublie l’ordre.

Une séquence le conserve.

Et notre machine venait précisément de passer d’une collection d’états à une séquence de transformations.

Voilà pourquoi la trace comptait.

Voilà pourquoi le temps comptait.

Voilà pourquoi le nombre de passages comptait.

Et voilà pourquoi un centre purement spatial commençait à sembler insuffisant.

Peut-être que le centre de notre architecture n’était pas un nœud.

Peut-être que c’était la relation qui permettait de conserver l’ordre entre les nœuds.

Pas une chose.

Une continuité.

Nous n’avions toujours pas de preuve qu’il fallait réellement appeler cela un « centre ».

Alors nous avons conservé le mot avec prudence.

**CANDIDAT : CENTRE DE CONTINUITÉ.**

Et juste en dessous, nous avons ajouté une nouvelle phrase.

Elle ne serait expliquée que plus tard.

**Le cœur n’est peut-être pas au milieu de la machine.**

**Il est peut-être ce qui empêche la machine de perdre la mesure entre deux battements.**

Puis nous avons fermé le dossier.

Parce qu’à ce stade, continuer aurait été dangereux.

Nous avions suffisamment d’éléments pour construire un test.

Pas encore suffisamment pour construire une vérité.

Et dans les chapitres qui allaient suivre, il allait falloir faire quelque chose de beaucoup plus difficile que trouver de nouveaux motifs.

Il allait falloir prendre ceux que nous avions déjà accumulés,

les mettre ensemble,

et vérifier lesquels appartenaient réellement à la même structure.

Car plus un système devient complexe,

plus il devient facile d’y voir ce que l’on souhaite.

Et plus il devient nécessaire de fabriquer une machine capable de répondre :

**cela était-il vraiment connecté avant que nous décidions que ça l’était?**
