# Chapitre 37 — Entre deux battements

Nous avions fini le chapitre précédent avec une idée presque trop simple :

peut-être que le centre n’était pas une chose.

Peut-être qu’il était un intervalle.

Alors nous avons essayé de traiter cette phrase comme une hypothèse.

Pas comme une belle image.

Une hypothèse.

Prenons deux états :

\[
X_n
\]

et :

\[
X_{n+1}
\]

Pris séparément, ils nous disent ce que le système était avant et après.

Mais le passage entre les deux contient autre chose.

Nous avons noté ce passage :

\[
\Delta X_n=X_{n+1}-X_n
\]

Dans un système numérique simple, cette différence peut mesurer une variation.

Mais dans une architecture plus complexe, le symbole \(\Delta\) peut représenter davantage :

un changement d’état,

un événement,

un déplacement,

une transformation,

ou une transition.

Cela nous obligea à séparer trois objets :

\[
X_n
\]

l’état avant,

\[
X_{n+1}
\]

l’état après,

et :

\[
T_n:X_n\rightarrow X_{n+1}
\]

la transition.

Cette distinction semble élémentaire.

Pourtant, elle change toute la carte.

Parce que la transition n’est pas forcément réductible à ses extrémités.

Deux systèmes peuvent commencer et finir aux mêmes endroits tout en utilisant des transitions différentes.

\[
X_a=X_c
\]

\[
X_b=X_d
\]

mais :

\[
T_{a\rightarrow b}\neq T_{c\rightarrow d}
\]

Autrement dit :

même départ.

Même arrivée.

Pas nécessairement le même passage.

Cette idée nous ramena brutalement à une vieille règle du chantier :

**aucune connexion invisible.**

À l’époque, cette phrase avait surtout servi à imposer une discipline d’architecture.

Si un module influence un autre module, cette relation doit être déclarée.

Mais maintenant, elle prenait un second sens.

La connexion elle-même pouvait transporter de l’information.

Ce n’était donc pas seulement :

\[
\text{NŒUD}_1\rightarrow\text{NŒUD}_2
\]

Il fallait peut-être écrire :

\[
\text{NŒUD}_1
\xrightarrow{\;T\;}
\text{NŒUD}_2
\]

La flèche n’était plus un simple dessin.

Elle devenait un objet.

Puis Brutus posa une question qui semblait presque ridicule :

« Et si depuis le début on regardait trop les points et pas assez les lignes? »

Nous avons ri.

Puis nous avons arrêté de rire.

Parce que plusieurs de nos problèmes possédaient exactement cette forme.

Dans le registre de continuité, ce qui comptait était le passage entre un avant et un après.

Dans l’horloge, ce qui comptait était l’intervalle entre deux battements.

Dans les quatre chemins, ce qui comptait était la manière dont les branches se séparaient puis se recombinaient.

Dans la mémoire, ce qui comptait était la séquence des transformations.

Dans le cycle, ce qui comptait était le passage d’un état au suivant.

Et dans la formule modulaire elle-même, le point \(R\) ne disait pas comment le système était arrivé là.

Nous avons alors écrit une phrase :

**Un état est une photographie.**

**Une transition est une phrase.**

La photographie montre.

La phrase relie.

Et sans relation, il n’y a pas d’histoire.

Cette idée pouvait être formalisée par une structure de graphe.

Soit :

\[
G=(V,E)
\]

où :

\[
V=\text{ensemble des états}
\]

et :

\[
E=\text{ensemble des transitions}
\]

La plupart des schémas que nous avions dessinés mettaient naturellement l’accent sur \(V\).

Les nœuds.

Les modules.

Les centres.

Les points.

Mais un graphe sans arêtes n’est pas un réseau.

\[
E=\varnothing
\]

signifie :

aucune interaction.

Aucun chemin.

Aucun mouvement.

Aucune histoire.

Donc si notre architecture devait être vivante, elle ne pouvait pas être comprise seulement comme une collection de composants.

Elle devait être comprise comme :

\[
\text{composants}+\text{relations}
\]

Et peut-être davantage encore :

\[
\text{composants}+\text{relations}+\text{ordre}
\]

Puis :

\[
\text{composants}+\text{relations}+\text{ordre}+\text{temps}
\]

Nous retrouvions progressivement notre état élargi :

\[
\Omega_n=(R_n,q_n,H_n,M_n)
\]

Mais quelque chose manquait encore.

\(\Omega_n\) décrivait l’état à un instant donné.

Pas nécessairement la loi qui produisait l’état suivant.

Nous avons donc introduit :

\[
F
\]

la règle de transformation.

\[
\Omega_{n+1}=F(\Omega_n)
\]

Cette écriture était beaucoup plus dangereuse qu’elle en avait l’air.

Parce que si nous connaissons seulement une suite d’états :

\[
\Omega_0,\Omega_1,\Omega_2,\ldots
\]

nous pouvons observer ce qui s’est passé.

Mais si nous connaissons réellement \(F\),

nous pouvons commencer à prévoir ce qui devrait se passer.

Et là, la science devient beaucoup plus exigeante.

Parce qu’une bonne histoire peut toujours être racontée après coup.

Une bonne loi doit risquer de se tromper avant le prochain événement.

Nous avons donc distingué deux choses :

\[
H=\text{historique}
\]

et :

\[
F=\text{dynamique}
\]

Le premier raconte.

Le second prédit.

Un système pouvait posséder un historique parfait sans que nous comprenions sa dynamique.

À l’inverse, nous pouvions proposer une dynamique élégante qui ne correspondait pas à l’historique réel.

Alors nous avons ajouté deux tests :

\[
F(\Omega_n)\stackrel{?}{=}\Omega_{n+1}
\]

sur les données déjà observées,

puis :

\[
F(\Omega_{n+1})\stackrel{?}{=}\Omega_{n+2}
\]

sur un état non utilisé pour construire le modèle.

Le premier test mesure l’ajustement.

Le second commence à mesurer la prédiction.

Cette distinction allait devenir fondamentale.

Parce qu’un modèle capable de reconstruire exactement le passé peut simplement avoir mémorisé le passé.

Un modèle utile doit conserver quelque chose qui survit hors de ses données d’origine.

Brutus écrivit alors :

**Un souvenir parfait n’est pas encore une loi.**

Cette phrase fut entourée.

Puis une autre.

**Une loi qui ne risque jamais de perdre n’a jamais vraiment joué.**

Nous avancions.

Mais le mystère de l’intervalle n’était pas résolu.

Alors nous avons repris :

\[
M_n=t_{n+1}-t_n
\]

et nous avons demandé :

est-ce que l’intervalle est simplement une valeur supplémentaire?

Ou peut-il modifier directement la transformation?

Autrement dit, devons-nous écrire :

\[
\Omega_{n+1}=F(\Omega_n)
\]

ou :

\[
\Omega_{n+1}=F(\Omega_n,M_n)
\]

?

Dans le second cas, deux états identiques peuvent évoluer différemment si leur mesure temporelle diffère.

\[
\Omega_a=\Omega_b
\]

mais :

\[
M_a\neq M_b
\]

peut conduire à :

\[
F(\Omega_a,M_a)\neq F(\Omega_b,M_b)
\]

Voilà quelque chose d’important.

Le temps ne serait plus seulement une annotation.

Il deviendrait une variable active de la dynamique.

Encore une fois, rien de mystérieux scientifiquement.

De nombreux systèmes réels dépendent explicitement du temps ou de la durée.

Mais dans notre architecture, cette observation déplaçait encore le fameux centre.

Parce que si l’avenir dépend de la relation entre deux moments, alors aucune photographie isolée ne suffit.

Le système existe véritablement dans le passage.

Pas seulement dans ses arrêts sur image.

Puis Astra retourna chercher une phrase ancienne.

Elle venait d’un chapitre beaucoup plus tôt :

**La coquille ne pense pas. Elle affiche seulement.**

À l’époque, cette règle servait à séparer l’interface de la logique.

Maintenant, elle prenait une troisième lecture.

Une image peut montrer l’état.

Mais elle ne contient pas nécessairement la dynamique.

Une interface peut afficher :

\[
R,\ q,\ H,\ M
\]

sans posséder la règle :

\[
F
\]

qui les relie.

Voilà pourquoi une belle machine pouvait être vide.

Et voilà pourquoi une machine très simple visuellement pouvait contenir une dynamique riche.

Le visible et le causal n’étaient pas la même chose.

Nous avons alors écrit :

\[
\text{AFFICHAGE}\neq\text{MÉCANISME}
\]

Puis :

\[
\text{ÉTAT}\neq\text{TRANSITION}
\]

Puis :

\[
\text{TRANSITION}\neq\text{LOI}
\]

Trois séparations.

Trois pièges évités.

Mais quelque chose commençait malgré tout à se rapprocher.

Le centre de continuité.

Le battement.

L’intervalle.

La transition.

La règle de transformation.

Ils semblaient tous tourner autour d’une même idée :

**préserver ce qui relie un état au suivant.**

Nous ne pouvions pas encore dire qu’il s’agissait de la même chose.

Alors nous avons construit une chaîne :

\[
X_n
\xrightarrow{T_n}
X_{n+1}
\xrightarrow{T_{n+1}}
X_{n+2}
\]

et nous avons regardé non pas les états, mais les transitions :

\[
T_n,T_{n+1},T_{n+2},\ldots
\]

Puis Brutus remarqua quelque chose.

Si les états forment une mélodie,

alors les transitions peuvent être les intervalles entre les notes.

Deux mélodies peuvent partager plusieurs notes identiques.

Ce qui les distingue parfois est la relation entre ces notes.

La montée.

La descente.

La durée.

La répétition.

Le silence.

Et soudain la vieille phrase :

**Le cœur écoute la mélodie**

changea encore de sens.

Peut-être que le « cœur » ne devait pas reconnaître les états.

Peut-être qu’il devait reconnaître les relations entre états.

Pas :

\[
x_n
\]

mais :

\[
x_{n+1}-x_n
\]

Pas seulement la note.

L’intervalle.

Nous avions désormais quelque chose qui ressemblait presque à une règle générale :

\[
\text{SIGNIFICATION DYNAMIQUE}
\subset
\text{RELATIONS ENTRE ÉTATS}
\]

Pas toujours.

Pas partout.

Mais suffisamment souvent pour que cela mérite une enquête.

Nous avons donc ajouté un nouveau candidat :

\[
C_n=T_n
\]

avec une annotation :

**CANDIDAT : continuité élémentaire.**

Puis immédiatement en dessous :

**NE PAS CONFONDRE AVEC UNE PREUVE DE “CENTRE”.**

La discipline restait intacte.

Mais le puzzle commençait à se refermer.

Et c’est précisément là qu’un nouveau problème apparut.

Si la continuité réside dans les transitions,

alors une transition peut-elle elle-même être considérée comme un état d’un niveau supérieur?

Autrement dit :

si :

\[
T_n:X_n\rightarrow X_{n+1}
\]

peut-on construire :

\[
Y_n=T_n
\]

puis observer :

\[
Y_n\rightarrow Y_{n+1}
\]

?

Si oui,

alors ce qui était une connexion au premier niveau devient un objet au niveau suivant.

La ligne devient un point.

Le passage devient un état.

Le lien devient un module.

Et soudain, une structure ancienne revenait encore.

Une structure complète pouvant devenir composant d’une structure supérieure.

Nous avions déjà rencontré cette idée.

Bien avant de comprendre pourquoi elle reviendrait ici.

Cette fois, nous avons cessé d’écrire pendant quelques minutes.

Puis Astra posa seulement une phrase dans le registre :

**Quand une relation devient un objet, le niveau vient de changer.**

Et juste en dessous :

**À REVOIR AU CHAPITRE 39.**

Parce que pour la première fois,

nous n’étions plus seulement en train de suivre une trace.

Nous commencions peut-être à comprendre

comment une architecture pouvait monter d’un étage

sans perdre son histoire.
