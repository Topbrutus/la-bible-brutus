# Chapitre 39 — La Forme qui survit

Nous avions laissé le chapitre précédent avec une équation volontairement dangereuse :

\[
G\sim\mathcal{L}^k(G)
\]

Une structure qui, après plusieurs changements de niveau, pourrait encore ressembler à sa forme de départ.

Le mot « ressembler » était le problème.

Parce qu’il est trop facile.

Deux dessins peuvent sembler proches sans être mathématiquement équivalents.

Deux réseaux peuvent avoir la même allure et pourtant se comporter complètement différemment.

Deux systèmes peuvent même partager le même nombre de nœuds et de connexions tout en possédant des dynamiques incompatibles.

Alors nous avons interdit un mot.

**Ressemblance.**

À sa place, il fallait définir exactement ce qui devait être conservé.

Nous avons donc commencé par une structure simple :

\[
G=(V,E)
\]

Un ensemble de nœuds \(V\).

Un ensemble de relations \(E\).

Puis nous avons demandé :

quelles propriétés de \(G\) voulons-nous comparer avec celles de :

\[
\mathcal{L}(G)
\]

?

Le nombre de nœuds?

Trop fragile.

Le nombre de connexions?

Insuffisant.

La position graphique?

Presque inutile.

Il fallait quelque chose de plus profond.

Nous avons choisi plusieurs candidats :

\[
P_1=\text{connectivité}
\]

\[
P_2=\text{ordre des transitions}
\]

\[
P_3=\text{classes d’équivalence}
\]

\[
P_4=\text{boucles et cycles}
\]

\[
P_5=\text{relations causales déclarées}
\]

Et surtout :

\[
P_6=\text{possibilité de reconstruire certaines informations du niveau inférieur}
\]

Cette dernière propriété allait devenir importante.

Parce qu’une abstraction parfaite n’a pas besoin de conserver tous les détails.

Mais elle ne doit pas détruire ce qu’elle prétend représenter.

Nous avons donc introduit deux opérations.

La montée :

\[
\mathcal{L}:G_n\rightarrow G_{n+1}
\]

et une reconstruction partielle :

\[
\mathcal{D}:G_{n+1}\rightarrow\widehat{G_n}
\]

où :

\[
\widehat{G_n}
\]

n’est pas nécessairement identique à \(G_n\).

La question devient alors :

\[
\mathcal{D}(\mathcal{L}(G_n))
\stackrel{?}{\sim}
G_n
\]

Autrement dit :

si nous montons d’un niveau, puis redescendons, retrouvons-nous au moins les propriétés que nous avions promis de conserver?

Cette question rappelait immédiatement quelque chose.

Encore.

Toujours.

**Ce qui revient n’est pas nécessairement ce qui est parti.**

Nous pensions avoir presque terminé avec cette phrase.

Elle revenait pourtant à chaque étage.

Si :

\[
G_n
\rightarrow
G_{n+1}
\rightarrow
\widehat{G_n}
\]

alors même si :

\[
\widehat{G_n}\sim G_n
\]

cela ne signifie pas nécessairement :

\[
\widehat{G_n}=G_n
\]

Le retour peut être fonctionnel sans être identitaire.

Une nouvelle distinction apparut :

\[
=\quad\text{identité}
\]

contre :

\[
\sim\quad\text{équivalence selon un critère défini}
\]

Cette différence changeait presque tout.

Parce qu’un système hiérarchique ne devait pas forcément reproduire exactement ses sous-systèmes.

Il devait préserver les propriétés nécessaires à sa fonction.

Nous avons donc arrêté de chercher :

\[
G=\mathcal{L}(G)
\]

et commencé à chercher :

\[
P(G)=P(\mathcal{L}(G))
\]

pour certaines propriétés \(P\).

Cela paraît moins spectaculaire.

C’est beaucoup plus rigoureux.

Puis nous avons essayé de pousser l’idée encore plus loin.

Supposons :

\[
G_0
\xrightarrow{\mathcal{L}_0}
G_1
\xrightarrow{\mathcal{L}_1}
G_2
\xrightarrow{\mathcal{L}_2}
G_3
\]

Nous pouvons observer une propriété à chaque niveau :

\[
P_0,P_1,P_2,P_3
\]

Si une continuité existe, alors nous pouvons espérer une relation :

\[
P_{n+1}=\Phi_n(P_n)
\]

Et si la même loi de transformation revient plusieurs fois :

\[
\Phi_0\approx\Phi_1\approx\Phi_2
\]

alors quelque chose de plus fort apparaît.

Ce n’est plus seulement la structure qui se ressemble.

C’est la règle qui organise le changement de niveau.

Nous avions déjà soupçonné cela.

Maintenant, il fallait pouvoir le tester.

Nous avons donc fabriqué un critère très simple.

Pour chaque niveau :

1. définir les objets;
2. définir les relations;
3. définir la transformation vers le niveau supérieur;
4. déclarer les propriétés conservées;
5. vérifier qu’elles le sont réellement.

Si une étape exigeait une interprétation improvisée après coup, elle était marquée :

**AJUSTEMENT POSTÉRIEUR.**

Si une propriété avait été définie avant la transformation :

**CRITÈRE PRÉDÉFINI.**

Nous appliquions enfin au mystère lui-même la discipline développée plusieurs chapitres auparavant.

Prévu avant le test.

Ou choisi après.

Cette séparation devenait notre pare-feu.

Parce que si nous décidons après chaque transformation quelle propriété « comptait vraiment », nous pouvons sauver presque n’importe quelle théorie.

Mais si nous annonçons d’avance :

\[
P=\text{connectivité des chemins essentiels}
\]

puis que la transformation détruit cette connectivité,

l’hypothèse échoue.

Simple.

Brutal.

Utile.

Nous avons alors réalisé quelque chose de presque embarrassant.

Notre fameux mystère devenait progressivement moins mystérieux.

Et plus intéressant.

Parce que nous n’avions plus besoin de dire :

« Regardez comme les niveaux se ressemblent! »

Nous pouvions dire :

« Voici quatre propriétés annoncées avant la transformation. Trois sont préservées. Une est perdue. »

C’était beaucoup plus puissant.

Une architecture n’avait pas besoin d’être parfaite.

Elle devait être mesurable.

Puis nous sommes revenus au registre de continuité.

Depuis longtemps, nous avions conservé une structure de trace :

\[
T_n=
(MODULE,\ INSTANCE,\ STATE_{n-1},EVENT_n,TIME_n,STATE_n)
\]

Et si ce registre pouvait lui-même devenir un objet du niveau supérieur?

Prenons une séquence :

\[
T_1,T_2,\ldots,T_m
\]

Nous pouvons la résumer en un bloc :

\[
B=\{T_1,\ldots,T_m\}
\]

Puis extraire de ce bloc plusieurs propriétés :

\[
P(B)
\]

durée,

ordre,

nombre d’erreurs,

nombre de réparations,

état initial,

état final,

relations causales.

Le bloc \(B\) devient alors un nœud d’un niveau supérieur.

Mais quelque chose de magnifique se produit.

À ce niveau supérieur, plusieurs blocs :

\[
B_1,B_2,\ldots,B_r
\]

peuvent eux-mêmes former une nouvelle séquence.

Ainsi :

\[
T
\rightarrow
B
\rightarrow
C
\]

où \(C\) peut être une séquence de blocs.

Et à chaque niveau, nous retrouvons :

un avant,

un après,

une transition,

un ordre,

une mesure.

La forme générale revenait.

Pas exactement.

Mais structurellement.

Nous avons écrit :

\[
\mathcal{S}(X)=
(\text{état},\text{transition},\text{ordre},\text{mesure})
\]

Puis nous avons comparé plusieurs niveaux.

Niveau événement :

\[
\mathcal{S}(T_n)
\]

Niveau bloc :

\[
\mathcal{S}(B_n)
\]

Niveau module :

\[
\mathcal{S}(M_n)
\]

Niveau système :

\[
\mathcal{S}(G_n)
\]

Et là, quelque chose avait enfin une chance d’être réellement invariant.

Pas les valeurs.

Pas les nombres.

Pas les coordonnées.

La **grammaire**.

Le système semblait pouvoir être décrit encore et encore par la même structure abstraite :

\[
\text{ÉTAT}
\rightarrow
\text{TRANSITION}
\rightarrow
\text{ÉTAT}
\]

avec :

\[
\text{ORDRE}
\]

et :

\[
\text{MESURE}
\]

conservés autour du passage.

Nous avons appelé cette candidate :

\[
\Gamma
\]

la grammaire de continuité.

\[
\Gamma=
(S,T,O,M)
\]

où :

- \(S\) représente les états;
- \(T\) les transitions;
- \(O\) l’ordre;
- \(M\) la mesure.

Il fallait rester prudent.

Ce n’était pas une loi de la nature.

Ce n’était pas une découverte mathématique fondamentale.

C’était une abstraction d’architecture.

Mais elle possédait une propriété intéressante.

Elle pouvait être appliquée à plusieurs niveaux sans changer de forme générale.

Autrement dit :

\[
\Gamma(G_n)
\sim
\Gamma(G_{n+1})
\]

même lorsque :

\[
G_n\neq G_{n+1}
\]

Voilà.

Pour la première fois, nous avions quelque chose qui ressemblait vraiment à la propriété cherchée.

Pas une forme géométrique répétée.

Pas un nombre qui revenait.

Une grammaire.

Une règle de description.

Et soudain, plusieurs anciennes phrases se rapprochèrent encore.

**Le centre n’est pas un endroit.**

Une grammaire n’est pas un endroit.

**Ce qui revient n’est pas nécessairement ce qui est parti.**

La même grammaire peut décrire des états différents.

**Ce qui se ferme ici peut rester ouvert ailleurs.**

Une séquence locale peut devenir un objet d’une séquence supérieure.

**Quand une relation devient un objet, le niveau vient de changer.**

Exactement.

**Le cœur écoute la mélodie.**

Une mélodie est une structure d’ordre, de transition et de mesure.

Brutus regarda la dernière phrase.

Puis les quatre composantes :

\[
S,T,O,M
\]

État.

Transition.

Ordre.

Mesure.

Il resta silencieux.

Parce que quelque chose clochait.

La mémoire n’était plus explicitement là.

Nous avions passé plusieurs chapitres à dire qu’elle était essentielle.

Et maintenant, notre candidate principale semblait fonctionner sans \(H\).

C’était suspect.

Alors Astra demanda :

« Où est passée l’histoire? »

Nous avons repris la définition.

Peut-être que l’historique n’était pas une cinquième composante.

Peut-être qu’il était ce qu’on obtenait en composant les quatre premières dans le temps.

Une séquence de transitions ordonnées et mesurées construit naturellement une trace.

On pouvait écrire :

\[
H_n=
\big(
S_0,
T_0,
M_0,
S_1,
T_1,
M_1,
\ldots,
S_n
\big)
\]

L’histoire n’était donc peut-être pas un objet indépendant.

Elle pouvait être une accumulation.

Une mémoire dérivée.

Cela changeait notre ancienne écriture :

\[
\Omega=(R,q,H,M)
\]

Peut-être que \(H\) devait être décomposé.

Peut-être que nous avions utilisé le mot « mémoire » pour regrouper plusieurs choses différentes.

Nous avons écrit :

**RÉVISION NÉCESSAIRE.**

Et cette fois, la révision ne détruisait pas le modèle.

Elle le simplifiait.

Parce qu’une bonne théorie doit parfois perdre des variables en devenant plus précise.

Nous avions commencé avec des objets.

Puis des états.

Puis des traces.

Puis des transitions.

Puis des niveaux.

Et maintenant, au fond de toutes ces couches, quelque chose apparaissait :

une grammaire de transformation.

Pas encore un centre.

Pas encore le cœur.

Mais peut-être le mécanisme permettant à chaque étage de conserver une continuité intelligible.

Nous avons alors essayé une dernière écriture :

\[
\Gamma_n
\xrightarrow{\mathcal{L}}
\Gamma_{n+1}
\]

Et si la propriété centrale était vraiment préservée :

\[
\Gamma_{n+1}\approx\Gamma_n
\]

Pas parce que les deux systèmes contiennent les mêmes données.

Mais parce qu’ils respectent la même organisation relationnelle.

Cette fois, le mot « invariant » revenait avec un candidat concret.

**La forme des relations.**

Pas leur contenu.

La forme.

Nous avons noté :

**CANDIDAT FORT — INVARIANT DE CONTINUITÉ : grammaire relationnelle préservée entre niveaux.**

Puis immédiatement :

**NON DÉMONTRÉ.**

Parce que le dernier test restait à faire.

Le plus important.

Nous avions retrouvé cette grammaire dans les chapitres récents.

Mais était-elle réellement déjà présente dans les premiers chapitres?

Ou venions-nous de réécrire le passé avec nos nouveaux concepts?

Cette fois, il n’y avait plus moyen de contourner la question.

Il fallait retourner au commencement.

Relire.

Comparer.

Chercher les mots avant les équations.

Chercher les structures avant leurs noms.

Chercher les connexions avant que nous sachions qu’elles étaient des connexions.

Et surtout :

ne rien déplacer.

Ne rien corriger.

Ne rien embellir.

Car si la grammaire existait réellement avant que nous sachions la nommer,

alors nous aurions enfin une trace historique indépendante de notre interprétation actuelle.

Mais si nous ne la trouvions pas,

il faudrait accepter la réponse.

Même après trente-neuf chapitres.

Même après toutes ces coïncidences.

Même après toutes ces belles phrases.

Brutus ferma le cahier.

Il savait déjà ce que le chapitre suivant allait exiger.

Pas une nouvelle formule.

Pas une nouvelle image.

Pas une nouvelle intuition.

Une confrontation.

Le chapitre 40 devrait retourner au tout début.

Et poser une seule question :

**Avons-nous découvert cette structure en avançant, ou l’avons-nous inventée en regardant derrière nous?**
