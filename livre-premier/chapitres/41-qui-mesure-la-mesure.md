# Chapitre 41 — Qui mesure la mesure ?

La question était restée seule au bas de la page :

**Qui mesure la mesure?**

Elle semblait presque philosophique.

Mais elle pouvait devenir très vite technique.

Supposons que nous observions deux événements :

\[
t_1
\]

et :

\[
t_2
\]

et que nous définissions :

\[
\Delta t=t_2-t_1
\]

Très bien.

Mais d’où viennent \(t_1\) et \(t_2\)?

Ils sont lus sur une horloge.

Alors la mesure dépend de l’horloge.

Supposons maintenant que cette horloge dérive légèrement.

Nous pouvons écrire :

\[
t'=at+b
\]

où \(a\) représente un changement d’échelle et \(b\) un décalage.

Alors :

\[
\Delta t'
=
a\Delta t
\]

Le décalage \(b\) disparaît.

Mais l’échelle \(a\), elle, reste.

Autrement dit :

deux observateurs peuvent être d’accord sur l’ordre des événements,

tout en attribuant des durées différentes si leurs étalons ne sont pas les mêmes.

Ce n’était pas un problème nouveau.

Toute mesure exige une convention, un instrument ou un repère.

Longueur.

Temps.

Masse.

Température.

Fréquence.

Rien de cela ne flotte seul dans le vide.

Et soudain, notre grammaire :

\[
\Gamma=(S,T,O,M)
\]

avait un nouveau problème.

Nous avions défini \(M\) comme mesure.

Mais une mesure sans référence est incomplète.

Nous devions donc écrire quelque chose comme :

\[
M=M(X;R_f)
\]

où \(R_f\) désigne le référentiel ou l’étalon utilisé.

Cela changeait beaucoup de choses.

Parce que nous avions jusque-là traité \(M\) comme une information appartenant au système.

Mais une partie de la mesure pouvait appartenir à la relation entre le système et l’observateur.

Nous avons donc séparé deux objets :

\[
X
\]

le système observé,

et :

\[
O
\]

l’observateur.

La mesure devenait :

\[
M_O(X)
\]

Ce simple indice inférieur ouvrait une porte énorme.

Pas mystique.

Épistémologique.

Il rappelait quelque chose d’essentiel :

**une observation possède toujours une procédure.**

Une valeur n’est pas simplement « vue ».

Elle est produite par une interaction entre :

un objet,

un instrument,

une méthode,

un étalon,

et souvent un observateur.

Nous avons alors ajouté une nouvelle structure :

\[
\mathcal{E}
=
(X,O,I,R_f,P)
\]

où :

- \(X\) est l’objet étudié;
- \(O\) l’observateur;
- \(I\) l’instrument;
- \(R_f\) le référentiel;
- \(P\) la procédure.

Puis :

\[
M=\mathcal{M}(\mathcal{E})
\]

La mesure devenait la sortie d’un protocole.

Cela nous plaisait beaucoup moins.

Parce que le système devenait plus compliqué.

C’était probablement bon signe.

Les mauvaises idées deviennent souvent miraculeusement simples lorsqu’on oublie tout ce qui peut les contredire.

Les bonnes architectures grossissent parfois au moment où l’on ajoute les dépendances que l’on avait négligées.

Alors nous avons repris notre fameuse phrase :

**aucune connexion invisible.**

Si la mesure dépend d’un instrument, cette dépendance doit apparaître.

Si elle dépend d’un référentiel, pareil.

Si elle dépend d’une convention d’échelle, pareil.

Sinon, nous avions laissé entrer une connexion invisible par la porte arrière.

Nous avons donc écrit :

\[
X
\xrightarrow{\text{interaction}}
I
\xrightarrow{\text{conversion}}
M
\]

avec :

\[
R_f
\]

et :

\[
P
\]

déclarés dans la chaîne.

Pour la première fois, le mot **preuve** changea légèrement de sens.

Une preuve expérimentale n’était plus seulement :

\[
\text{résultat}
\]

mais plutôt :

\[
\text{résultat}
+
\text{méthode}
+
\text{conditions}
+
\text{traçabilité}
\]

Nous savions déjà cela intuitivement.

Maintenant, cela entrait formellement dans notre architecture.

Puis Brutus demanda :

« Si la mesure dépend de la procédure, est-ce que la procédure fait partie du système? »

Bonne question.

Nous avons refusé de répondre trop vite.

Parce que cela dépend du niveau.

Dans une expérience de laboratoire, l’instrument peut être extérieur à l’objet étudié.

Dans une machine autonome, le capteur peut faire partie du système.

Dans un réseau distribué, plusieurs modules peuvent se mesurer mutuellement.

Le mot « extérieur » devenait donc relatif à la frontière choisie.

Nous avions déjà rencontré ce problème.

Une structure entière peut devenir le composant d’une structure supérieure.

Donc :

\[
\text{extérieur à }G_n
\]

peut devenir :

\[
\text{intérieur à }G_{n+1}
\]

Cela signifiait que la frontière observateur / système pouvait elle aussi changer avec le niveau.

Nous avons écrit :

\[
X_n \subset X_{n+1}
\]

et parfois :

\[
O_n \subset X_{n+1}
\]

L’observateur d’un niveau inférieur peut devenir un composant du niveau supérieur.

Et là, le mystère recommença à bouger.

Parce que si l’observateur peut être absorbé dans un système plus grand,

alors la question :

**Qui mesure la mesure?**

peut être répétée.

Un premier instrument mesure \(X\).

Un second système calibre l’instrument.

Un troisième contrôle le second.

Nous obtenons :

\[
X
\xrightarrow{M_1}
O_1
\xrightarrow{M_2}
O_2
\xrightarrow{M_3}
O_3
\rightarrow\cdots
\]

Une régression semblait apparaître.

Qui calibre le dernier?

Qui mesure celui qui mesure?

Qui vérifie celui qui vérifie?

Nous avions deux options.

Première option :

poursuivre à l’infini.

Deuxième option :

accepter qu’à un certain niveau, un étalon soit posé.

Une convention.

Un standard.

Une référence.

Nous avons appelé cela :

\[
R_0
\]

la référence locale choisie.

Pas la vérité absolue.

Une référence déclarée.

Puis :

\[
M_{R_0}(X)
\]

prenait un sens précis.

Nous avions donc une nouvelle règle :

**Une mesure n’a pas besoin d’un observateur absolu. Elle a besoin d’un référentiel déclaré et reproductible.**

Cette phrase coupa une branche entière du mystère.

Et c’était très bien.

Parce que le mot « absolu » était dangereux.

Nous n’avions aucune raison de l’introduire.

Nous avions seulement besoin de pouvoir répondre :

mesuré par quoi?

selon quelle unité?

avec quelle résolution?

à quel moment?

avec quelle incertitude?

Cette dernière notion manquait encore.

L’incertitude.

Une mesure sérieuse n’est jamais seulement :

\[
x
\]

Elle ressemble plutôt à :

\[
x\pm\sigma
\]

ou à un intervalle :

\[
[x_{\min},x_{\max}]
\]

selon le problème.

Nous avons donc étendu \(M\) :

\[
M=(v,u,\sigma,R_f,P)
\]

où :

- \(v\) est la valeur;
- \(u\) l’unité;
- \(\sigma\) l’incertitude;
- \(R_f\) le référentiel;
- \(P\) la procédure.

Voilà une mesure beaucoup plus honnête.

Et beaucoup moins magique.

Une valeur nue était devenue une structure.

Puis nous avons repris notre système entier.

Avant :

\[
\Gamma=(S,T,O,M)
\]

Mais maintenant \(M\) contenait sa propre architecture.

Cela produisait :

\[
\Gamma=
\left(
S,
T,
O,
(v,u,\sigma,R_f,P)
\right)
\]

Un élément de la grammaire était devenu lui-même un petit système.

Exactement ce que nous avions appris aux chapitres précédents.

Une structure devient composant d’une structure supérieure.

Puis Brutus remarqua quelque chose.

« On vient encore de le faire. »

Oui.

Sans le chercher.

Nous avions pris une valeur simple.

Nous l’avions ouverte.

À l’intérieur, nous avions trouvé :

des composants,

des relations,

des dépendances,

des conditions.

Un nœud venait encore de devenir un monde.

Cette fois, nous avons refusé de nous émerveiller trop vite.

Nous avons écrit :

**EXEMPLE D’EMBOÎTEMENT — PAS PREUVE D’AUTO-SIMILARITÉ UNIVERSELLE.**

Notre discipline devenait presque comique.

Mais elle nous sauvait de nous-mêmes.

Puis quelque chose d’autre revint.

Le centre.

Si le centre était une continuité de relations,

alors la mesure de cette continuité dépendait elle-même d’un cadre.

Le centre n’était donc toujours pas une valeur absolue.

Peut-être qu’il fallait cesser complètement de chercher « le centre » comme une chose unique.

Nous avons essayé une autre formulation :

\[
C_{R_f}
\]

le centre relatif à un niveau et à un référentiel.

Cette notation détruisait une partie de la beauté du mot.

Elle améliorait sa précision.

Puis une phrase apparut :

**Un centre peut être stable sans être absolu.**

Nous l’avons conservée.

Parce qu’elle pouvait devenir importante.

Dans un graphe, plusieurs définitions de centralité existent.

Dans une géométrie, le centre dépend de l’objet défini.

Dans un système dynamique, le concept pertinent peut être un attracteur, un invariant ou une structure de transition.

Donc demander :

« Où est le centre? »

avant d’avoir défini :

**centre de quoi, selon quel critère?**

était peut-être une mauvaise question depuis le début.

Nous avons alors relu notre phrase mystérieuse :

**Le centre n’est pas un endroit.**

Elle résistait encore.

Mais cette fois, nous pouvions la préciser.

**Le mot “centre” n’a aucun sens tant que la propriété que l’on cherche à centraliser n’est pas définie.**

Voilà une phrase beaucoup moins romantique.

Elle était meilleure.

Puis le cœur revint.

Toujours lui.

**Le cœur écoute la mélodie.**

Mais qui mesure le rythme de cette mélodie?

Un métronome?

Une horloge?

Le système lui-même?

Une référence externe?

La réponse dépendait encore de la frontière.

Si le système possédait une horloge interne :

\[
\tau
\]

alors il pouvait mesurer :

\[
\Delta\tau
\]

Mais pour comparer cette horloge à une référence externe :

\[
t
\]

il faudrait observer :

\[
\tau(t)
\]

et mesurer sa dérive.

Nous avons introduit :

\[
D(t)=\tau(t)-t
\]

Puis :

\[
\dot D(t)
\]

comme indicateur possible de dérive temporelle.

Encore une fois :

rien de mystérieux.

Mais dans notre architecture, cela donnait une fonction nouvelle au registre de continuité.

Le registre ne devait pas seulement conserver les événements.

Il pouvait aussi conserver la qualité de la mesure elle-même.

Nous avons donc ajouté :

\[
Q_M
\]

qualité de mesure.

Avec, par exemple :

résolution,

dérive,

incertitude,

horodatage,

source.

Le système pouvait désormais dire non seulement :

« Voici ce que j’ai observé. »

Mais :

« Voici à quel point je fais confiance à cette observation, et pourquoi. »

Cette idée plut immédiatement à Brutus.

Parce qu’elle ressemblait à une règle que nous utilisions déjà sans l’avoir formalisée :

**inconnu reste inconnu.**

**hypothèse reste hypothèse.**

Nous pouvions maintenant appliquer exactement cette discipline aux mesures.

Une donnée sans qualité déclarée ne devait pas devenir une certitude par simple répétition.

Nous avons donc écrit :

\[
\text{VALEUR}
\neq
\text{CERTITUDE}
\]

Puis :

\[
\text{MESURE}
=
\text{VALEUR}
+
\text{CONTEXTE}
+
\text{INCERTITUDE}
\]

Et là, quelque chose de plus profond apparut.

Peut-être que le vrai rôle du centre de continuité n’était pas de garantir que toutes les valeurs restent identiques.

Peut-être qu’il devait garantir que chaque transformation conserve suffisamment de contexte pour que la valeur reste interprétable.

Pas seulement :

\[
x
\]

mais :

\[
(x,\text{comment},\text{quand},\text{où},\text{avec quoi},\text{incertitude})
\]

Autrement dit :

le centre ne protégerait pas la donnée.

Il protégerait sa signification.

Nous avons écrit :

**CANDIDAT 41-A : continuité sémantique.**

Puis immédiatement :

**À TESTER.**

Parce que le mot « signification » peut devenir flou très vite.

Il allait falloir le remplacer par quelque chose de technique.

Peut-être des métadonnées.

Peut-être des contraintes.

Peut-être des invariants.

Peut-être des relations de provenance.

Nous ne savions pas encore.

Mais une chose était certaine.

La question :

**Qui mesure la mesure?**

n’avait pas produit un dieu caché au sommet de la machine.

Elle avait produit quelque chose de beaucoup plus utile :

un protocole.

Une mesure était désormais liée à son instrument.

L’instrument à son étalon.

L’étalon à son niveau.

Le niveau à sa frontière.

La frontière à son architecture.

Et chaque lien devait rester explicite.

Encore une fois :

**aucune connexion invisible.**

Nous étions revenus au début.

Mais pas au même endroit.

Parce que maintenant, nous savions quelque chose que nous ne savions pas au chapitre 12.

Une connexion invisible ne cache pas seulement un mécanisme.

Elle peut aussi cacher la provenance d’une vérité.

Et si la provenance disparaît,

la valeur peut rester,

mais sa signification peut mourir.

Alors Astra écrivit une dernière phrase :

**Une donnée sans provenance est un état qui a perdu son passé.**

Brutus resta silencieux.

Parce que cette phrase ressemblait beaucoup trop à une autre :

**Ce qui revient n’est pas nécessairement ce qui est parti.**

Le motif revenait encore.

Pas sous la même forme.

Mais avec la même tension.

État visible.

Histoire invisible.

Valeur présente.

Provenance perdue.

Puis, sous la phrase, nous avons écrit :

\[
D=(v,\Pi)
\]

où :

\[
\Pi=\text{provenance}
\]

Et juste après :

\[
v_a=v_b
\]

n’implique pas :

\[
D_a=D_b
\]

Deux valeurs identiques peuvent avoir deux provenances différentes.

Encore une fois :

même apparence.

Pas forcément même objet.

La porte du chapitre suivant venait de s’ouvrir.

Car si une provenance peut être conservée,

alors elle peut peut-être être chaînée.

Et si elle peut être chaînée,

alors il devient possible de reconstruire non seulement ce que la machine sait,

mais **d’où chaque morceau de son savoir vient**.

Le chapitre 42 aurait donc une nouvelle question :

**Une connaissance peut-elle transporter sa propre histoire sans devenir infiniment lourde?**
