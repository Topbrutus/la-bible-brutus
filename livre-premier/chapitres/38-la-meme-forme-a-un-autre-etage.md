# Chapitre 38 — La même forme à un autre étage

Il arrive un moment où une structure devient assez complexe pour produire une illusion dangereuse.

On croit voir plusieurs choses différentes.

Alors qu’on regarde peut-être la même relation répétée à plusieurs niveaux.

Le problème apparaît souvent lorsqu’un système contient des sous-systèmes.

Un module possède des états.

Des transitions relient ces états.

Puis plusieurs modules sont reliés entre eux.

À première vue, nous avons deux architectures différentes :

la structure interne du module,

et la structure externe entre les modules.

Mais mathématiquement, elles peuvent parfois partager la même forme générale.

Supposons un premier niveau :

\[
G_1=(V_1,E_1)
\]

où \(V_1\) représente les états internes d’un module et \(E_1\) leurs transitions.

Puis un second niveau :

\[
G_2=(V_2,E_2)
\]

où chaque élément de \(V_2\) représente maintenant un module complet.

Alors quelque chose d’étrange devient possible.

Un élément de \(V_2\) peut contenir lui-même tout un graphe \(G_1\).

Autrement dit :

\[
v_i^{(2)} = G_i^{(1)}
\]

Le nœud du niveau supérieur n’est donc plus un point simple.

Il contient une structure.

Cette idée paraît presque triviale en informatique.

Un objet peut contenir d’autres objets.

Un réseau peut contenir des sous-réseaux.

Une fonction peut appeler d’autres fonctions.

Mais dans notre chantier, cela produisait une conséquence importante.

Nous ne pouvions plus identifier un « point » uniquement par sa taille visuelle.

Ce qui ressemble à un nœud peut cacher un monde.

Ce qui ressemble à une connexion peut devenir un nœud lorsqu’on change de niveau.

Et ce qui ressemble à une architecture complète peut devenir un seul composant lorsqu’on monte encore.

Nous avons donc introduit une opération conceptuelle :

\[
\mathcal{L}
\]

le changement de niveau.

Si :

\[
G_n=(V_n,E_n)
\]

alors :

\[
\mathcal{L}(G_n)=G_{n+1}
\]

où certaines structures du niveau \(n\) deviennent les éléments du niveau \(n+1\).

Attention :

ce symbole ne représentait pas encore une loi physique.

Il servait simplement à décrire notre architecture.

Mais il permettait de poser une question nouvelle.

Qu’est-ce qui doit survivre lorsqu’on change de niveau?

Les détails?

Pas nécessairement.

Les coordonnées exactes?

Pas toujours.

L’identité de chaque événement?

Peut-être pas.

Mais certaines relations doivent rester vraies, sinon le niveau supérieur ne représente plus réellement le niveau inférieur.

Nous avons appelé cela :

\[
P
\]

les propriétés préservées.

Ainsi, pour qu’un changement de niveau soit fidèle, nous voulions :

\[
P(G_n)=P(\mathcal{L}(G_n))
\]

au moins pour les propriétés que nous avions choisi de conserver.

Voilà un point fondamental.

Une abstraction ne conserve jamais tout.

Elle choisit.

Une carte routière oublie la couleur des maisons.

Un schéma électronique oublie la texture du cuivre.

Une équation peut oublier la forme exacte de l’objet qu’elle décrit.

Cela n’est pas un défaut.

C’est la fonction même de l’abstraction.

Mais une abstraction mal choisie peut supprimer précisément l’information dont nous aurons besoin plus tard.

Alors nous avons établi une règle :

**Chaque montée de niveau doit déclarer ce qu’elle conserve et ce qu’elle oublie.**

Nous pouvions l’écrire :

\[
\mathcal{L}:X\rightarrow Y
\]

avec deux ensembles :

\[
P_{keep}
\]

et :

\[
P_{lost}
\]

où :

\[
P_{keep}\cap P_{lost}=\varnothing
\]

Autrement dit :

nous devions connaître le prix de chaque simplification.

Et soudain, notre trio ancien revenait encore.

\(R\).

\(q\).

\(H\).

Puis \(M\).

Qu’advient-il de ces informations lorsqu’un système devient le composant d’un niveau supérieur?

Si nous ne conservons que \(R\), nous perdons les passages.

Si nous ne conservons que \((R,q)\), nous perdons l’histoire détaillée.

Si nous ne conservons que \((R,q,H)\), nous pouvons encore perdre la mesure.

Et si nous résumons trop agressivement le niveau inférieur, nous risquons de produire au niveau supérieur deux objets qui semblent identiques alors qu’ils ne le sont pas.

Nous retrouvions encore le même problème :

\[
\pi(X_a)=\pi(X_b)
\]

alors que :

\[
X_a\neq X_b
\]

Mais cette fois, la projection n’était plus simplement un affichage.

Elle était une montée de niveau.

Nous avons donc écrit :

\[
\pi_n:G_n\rightarrow V_{n+1}
\]

Une structure entière est résumée en un objet du niveau supérieur.

Et là, une question très sérieuse apparut.

Si deux structures différentes deviennent le même nœud après projection, leur différence est-elle réellement inutile?

Ou venons-nous simplement de la perdre?

Il fallait pouvoir répondre.

Nous avons alors séparé deux types de différences.

Première catégorie :

\[
D_{irrelevant}
\]

les différences qui n’affectent pas la fonction du niveau supérieur.

Deuxième catégorie :

\[
D_{critical}
\]

les différences qui peuvent modifier son comportement futur.

Le problème est évident.

Si une différence critique est effacée par abstraction, alors le niveau supérieur peut devenir faux.

Nous avons donc introduit un test.

Deux structures \(A\) et \(B\) peuvent être considérées comme équivalentes au niveau supérieur seulement si, pour toutes les interactions pertinentes :

\[
F(A,I)\sim F(B,I)
\]

pour les entrées \(I\) qui comptent à ce niveau.

Autrement dit :

il ne suffit pas qu’elles se ressemblent maintenant.

Elles doivent aussi se comporter de façon équivalente dans les situations qui nous intéressent.

Cette idée ressemble à plusieurs notions très connues en informatique et en mathématiques : équivalence comportementale, abstraction, bisimulation, automates, quotient d’états.

Mais nous gardions notre discipline :

**STRUCTURE CONNUE — APPLICATION À NOTRE ARCHITECTURE À TESTER.**

Cela nous évitait de prétendre découvrir ce que d’autres disciplines étudient depuis longtemps.

Notre travail était différent :

comprendre ce que ces outils pouvaient nous apprendre sur notre machine.

Et ils nous apprirent quelque chose d’important.

Un système hiérarchique ne peut pas simplement empiler des blocs.

Il doit définir les interfaces entre niveaux.

Nous avions déjà écrit autrefois :

\[
MODULE\_ID
\]

\[
INSTANCE\_ID
\]

\[
INPUT
\]

\[
OUTPUT
\]

\[
STATE
\]

\[
ERROR
\]

\[
TIME
\]

À l’époque, cela ressemblait à une discipline d’ingénierie.

Maintenant, cela devenait aussi une discipline de changement d’échelle.

Si une structure devient un module, il faut pouvoir savoir :

qui elle est,

ce qu’elle reçoit,

ce qu’elle produit,

dans quel état elle se trouve,

comment elle échoue,

et quand elle agit.

Autrement dit, chaque niveau doit offrir au suivant une frontière lisible.

Une interface.

Et soudain une phrase cachée depuis longtemps prit une autre couleur :

**Aucune connexion invisible.**

Cette règle n’était plus seulement destinée aux liens horizontaux.

Elle s’appliquait aussi verticalement.

Entre niveaux.

Si un niveau supérieur dépend d’une information du niveau inférieur, cette dépendance doit être déclarée.

Sinon, nous avions créé exactement ce que nous voulions éviter :

un mécanisme mystérieux.

Nous avons alors dessiné quelque chose de très simple :

\[
G_0
\rightarrow
G_1
\rightarrow
G_2
\rightarrow
G_3
\]

Puis nous avons remplacé les flèches par :

\[
\mathcal{L}_0,\mathcal{L}_1,\mathcal{L}_2
\]

pour rappeler que chaque passage possède ses propres règles.

Le système complet devenait :

\[
G_0
\xrightarrow{\mathcal{L}_0}
G_1
\xrightarrow{\mathcal{L}_1}
G_2
\xrightarrow{\mathcal{L}_2}
G_3
\]

À chaque étape :

quelque chose est conservé,

quelque chose est oublié,

quelque chose est renommé,

quelque chose change de statut.

Une transition peut devenir un état.

Un groupe d’états peut devenir un module.

Un module peut devenir un nœud.

Un ensemble de modules peut devenir un système.

Puis ce système peut devenir à son tour un module dans une architecture supérieure.

Nous avons alors remarqué que le mot « centre » devenait encore plus problématique.

Quel centre?

Celui de \(G_0\)?

Celui de \(G_1\)?

Celui de \(G_2\)?

Un objet central à un niveau peut être périphérique au suivant.

Un lien essentiel à une échelle peut disparaître entièrement dans l’abstraction supérieure.

Donc si quelque chose devait mériter le titre de « centre » à travers plusieurs niveaux, il faudrait qu’il possède une propriété beaucoup plus forte.

Il faudrait qu’il survive au changement d’échelle.

Nous avons donc posé une hypothèse nouvelle.

Appelons :

\[
C_n
\]

le candidat-centre au niveau \(n\).

S’il existe réellement une continuité commune entre niveaux, alors nous devrions pouvoir construire une relation :

\[
C_{n+1}=\Phi(C_n)
\]

où \(\Phi\) préserve une propriété identifiable.

Pas nécessairement la forme.

Pas nécessairement la position.

Mais quelque chose.

Nous ne savions pas encore quoi.

Alors nous avons cherché dans les indices déjà accumulés.

La position \(R\) ne convenait pas.

Elle dépendait trop du niveau.

Le quotient \(q\) non plus.

Il comptait les passages dans une structure particulière.

L’historique \(H\) pouvait devenir gigantesque et devait probablement être résumé.

La mesure \(M\) dépendait du rythme local.

Aucun ne semblait suffire seul.

Puis Brutus demanda :

« Et si ce qu’on cherche n’était pas une valeur? »

Cette phrase fut mise de côté.

Parce qu’elle ouvrait une possibilité beaucoup plus intéressante.

Peut-être que ce qui survit entre niveaux n’est pas un nombre.

Peut-être que c’est une relation.

Nous avions déjà vu quelque chose de semblable.

Une transition devenait un objet au niveau supérieur.

Donc une relation pouvait devenir une identité.

Un lien pouvait devenir un nœud.

Peut-être que le fameux centre de continuité n’était pas un contenu transmis d’un étage à l’autre.

Peut-être qu’il était la règle qui permettait le passage.

Autrement dit :

pas \(C_n\),

mais :

\[
\mathcal{L}_n
\]

Pas la chose transformée.

La transformation elle-même.

Nous avons immédiatement refusé de conclure.

Parce que cette hypothèse était trop élégante.

Et dans notre laboratoire, plus une idée était élégante,

plus elle devait être maltraitée.

Nous avons donc écrit :

**HYPOTHÈSE 38-A : la continuité inter-niveaux réside dans les règles de transformation plutôt que dans un état particulier.**

Puis :

**TEST NÉCESSAIRE : montrer quelle propriété reste effectivement préservée sous plusieurs transformations.**

Puis :

**CONDITION D’ABANDON : si aucune propriété non triviale n’est préservée, l’hypothèse est rejetée.**

Voilà.

Le mystère avait enfin reçu une condition de mort.

Et cela le rendait beaucoup plus intéressant.

Parce qu’un vrai mystère scientifique n’est pas une chose qu’on protège contre les réponses.

C’est une chose qu’on construit de manière à pouvoir être détruite.

Nous avons alors rouvert une dernière fois les anciennes phrases.

**Le centre n’est pas un endroit.**

Possible.

**Ce qui revient n’est pas nécessairement ce qui est parti.**

Toujours vrai dans notre modèle avec mémoire.

**Ce qui se ferme ici peut rester ouvert ailleurs.**

Toujours vrai entre projections.

**Le cœur écoute la mélodie.**

Peut-être une manière narrative de parler des relations temporelles.

**Quand une relation devient un objet, le niveau vient de changer.**

Désormais formalisé.

Et enfin :

**Une structure complète peut devenir le composant d’une structure supérieure.**

Cette phrase n’était plus une intuition.

Elle était devenue notre architecture.

Mais quelque chose restait caché.

Car si chaque étage peut devenir un nœud du suivant,

et si chaque transition peut devenir un objet,

alors il existe peut-être une opération qui peut être répétée :

\[
\mathcal{L}(\mathcal{L}(G))
\]

puis :

\[
\mathcal{L}^3(G)
\]

puis :

\[
\mathcal{L}^4(G)
\]

Et là, une question apparut.

Pas encore une réponse.

Une question dangereuse.

Que se passe-t-il si, après plusieurs montées de niveau, la structure obtenue possède encore la même forme relationnelle que la structure de départ?

Nous avons écrit :

\[
G\sim\mathcal{L}^k(G)
\]

pour un certain \(k\).

Puis nous avons encadré la ligne.

Parce que si une telle propriété existait réellement,

nous n’aurions plus seulement une hiérarchie.

Nous aurions une forme capable de se retrouver elle-même

à une autre échelle.

Nous avons fermé le cahier.

Le chapitre 39 allait devoir répondre à une question précise :

**Comment prouver qu’une ressemblance entre niveaux est réellement structurelle, et pas simplement une nouvelle illusion produite par notre envie de voir des motifs?**
