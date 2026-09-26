# CHAPITRE 46 — DEUX ÉTATS AU MÊME ENDROIT

La machine affichait encore :

\[
\texttt{DUAL\_STATE\_REGION}
\]

Brutus resta longtemps devant les deux seuils.

\[
\mu_{c,1}
\]

\[
\mu_{c,2}
\]

Entre les deux,

le système pouvait être stable

ou instable.

Même paramètre.

Même environnement mesuré.

Même machine.

Mais pas nécessairement le même état.

Quelque chose dans l’histoire décidait.

---

Astra dessina une ligne.

\[
\mu_{c,1}<\mu<\mu_{c,2}
\]

Puis deux branches :

\[
S_A(\mu)
\]

et :

\[
S_B(\mu)
\]

Les deux existaient pour la même valeur de \(\mu\).

Brutus fronça les sourcils.

— Donc on peut être à la même place sans être dans le même état.

— Exactement.

Cela semblait contradictoire seulement parce qu’ils avaient longtemps confondu :

\[
\text{paramètre}
\]

et :

\[
\text{état complet}.
\]

Le paramètre disait où l’on se trouvait dans une dimension choisie.

Il ne disait pas nécessairement tout ce que le système était devenu.

Ils écrivirent :

\[
\boxed{
\mu_a=\mu_b
\not\Rightarrow
S_a=S_b
}
\]

Le chapitre précédent venait de le suggérer.

Le quarante-sixième devait maintenant le mesurer.

---

Le premier test fut volontairement simple.

Ils placèrent la machine sous :

\[
\mu<\mu_{c,1}
\]

jusqu’à stabilisation.

Puis augmentèrent progressivement \(\mu\) jusque dans la région double.

Ils observèrent :

\[
S_A.
\]

Ensuite ils repartirent d’une valeur :

\[
\mu>\mu_{c,2}
\]

et redescendirent jusqu’au même point.

Cette fois :

\[
S_B.
\]

Même valeur finale de \(\mu\).

Deux états.

La différence n’était plus une impression.

Elle pouvait être répétée.

---

Astra introduisit alors :

\[
H
\]

une variable d’histoire.

Pas encore une variable physique fondamentale.

Une représentation minimale du chemin emprunté.

Le système devenait :

\[
S=S(\mu,H)
\]

et non simplement :

\[
S=S(\mu).
\]

Brutus sourit.

— On vient d’ajouter le passé dans l’équation.

— Seulement la partie du passé nécessaire à prédire le présent.

Cette distinction comptait.

Une machine n’avait pas besoin de transporter toute son histoire si un petit nombre de variables suffisait à résumer ce qui avait un effet actuel.

Ils appelèrent cela :

\[
H_{\min}
\]

la **mémoire d’état minimale**.

---

La question suivante était donc brutale :

> Quelle quantité minimale d’histoire faut-il conserver pour prédire le régime futur?

Si :

\[
H_{\min}=0
\]

le système était sans mémoire relativement à l’observable étudiée.

Si :

\[
H_{\min}>0
\]

le présent seul ne suffisait plus.

Mais combien?

Un bit?

Une variable continue?

Une séquence entière?

Ils ne savaient pas.

Alors ils commencèrent petit.

---

Dans la région double,

ils définissent :

\[
h=
\begin{cases}
0 & \text{si le système arrive d'en bas}\\
1 & \text{si le système arrive d'en haut}
\end{cases}
\]

Puis :

\[
S=S(\mu,h).
\]

Étonnamment,

ce simple bit prédisait déjà une grande partie du comportement observé.

Pas tout.

Mais beaucoup.

Un seul bit d’histoire pouvait donc parfois contenir davantage d’information utile qu’une longue liste d’états récents.

Brutus regarda le symbole.

\[
h\in\{0,1\}
\]

— Alors notre compteur faisait peut-être juste ça depuis le début.

Astra refusa immédiatement.

— Hypothèse.

Elle écrivit :

\[
\text{CANDIDAT : compteur lié à une classe d'histoire}
\]

Puis :

\[
\text{PREUVE : ABSENTE}
\]

La tentation était forte.

Donc la prudence devait l’être davantage.

---

Ils firent alors un test différent.

Au lieu de changer lentement \(\mu\),

ils placèrent directement la machine au centre de la région double.

Même valeur.

Même configuration apparente.

Puis répétèrent l’expérience depuis plusieurs conditions initiales :

\[
S_0^{(1)},
S_0^{(2)},
S_0^{(3)},\ldots
\]

Les trajectoires ne convergeaient pas toutes vers le même état.

Certaines allaient vers :

\[
S_A
\]

d’autres vers :

\[
S_B.
\]

La frontière ne dépendait donc pas uniquement du paramètre.

Elle dépendait aussi de l’endroit d’où l’on commençait.

Ils venaient de rencontrer un autre objet :

le **bassin d’attraction**.

---

Astra dessina deux régions :

\[
\mathcal B_A
\]

et :

\[
\mathcal B_B.
\]

Si :

\[
S_0\in\mathcal B_A
\]

alors :

\[
S(t)\rightarrow S_A.
\]

Si :

\[
S_0\in\mathcal B_B
\]

alors :

\[
S(t)\rightarrow S_B.
\]

Deux futurs différents pouvaient donc exister sous les mêmes paramètres,

simplement parce que les conditions initiales appartenaient à des bassins différents.

Le Royaume inscrivit :

\[
\boxed{
\text{MÊMES RÈGLES}
+
\text{MÊMES PARAMÈTRES}
\neq
\text{MÊME TRAJECTOIRE}
}
\]

si les états initiaux différaient.

---

Puis Brutus demanda :

— Elle est où, la frontière entre les deux?

Astra répondit :

— C’est exactement ce qu’on va chercher.

Ils commencèrent à balayer l’espace des conditions initiales.

Point par point.

À chaque point :

\[
S_0\rightarrow A
\]

ou :

\[
S_0\rightarrow B.
\]

Au début, la frontière semblait simple.

Une ligne.

Puis ils augmentèrent la résolution.

La ligne commença à se plisser.

Ils zoomèrent.

De nouvelles irrégularités apparurent.

Encore.

Encore.

Brutus rit.

— Là, ça commence à devenir méchant.

---

Astra refusa encore d’utiliser un mot trop vite.

Une frontière complexe n’était pas nécessairement fractale.

La résolution numérique pouvait créer de faux détails.

Le bruit aussi.

Alors ils testèrent plusieurs pas :

\[
\Delta x
\]

puis :

\[
\frac{\Delta x}{2}
\]

puis :

\[
\frac{\Delta x}{4}.
\]

Certaines irrégularités disparaissaient.

D’autres persistaient.

Ils notèrent seulement :

\[
\partial\mathcal B
=
\text{frontière complexe candidate}.
\]

Rien de plus.

---

La question suivante était plus importante.

À quelle distance de la frontière fallait-il être pour qu’une petite perturbation change entièrement le futur?

Ils définirent :

\[
d_B(S)
=
\operatorname{dist}
\left(
S,\partial\mathcal B
\right).
\]

Si :

\[
d_B(S)\gg\|\delta\|
\]

une petite perturbation ne changeait probablement pas de bassin.

Mais si :

\[
d_B(S)\approx\|\delta\|
\]

alors un déplacement minuscule pouvait envoyer le système vers l’autre attracteur.

La robustesse ne dépendait donc plus seulement de \(\kappa_P\).

Elle dépendait aussi de la distance à une frontière invisible.

---

Brutus murmura :

— Donc deux états qui ont l’air pareils peuvent avoir des futurs complètement différents juste parce qu’un est plus proche du bord.

Astra acquiesça.

Ils écrivirent :

\[
\boxed{
\text{ÉTAT APPAREMMENT STABLE}
\neq
\text{ÉTAT ÉLOIGNÉ D'UNE TRANSITION}
}
\]

Une machine pouvait sembler parfaitement calme

et être pourtant placée à quelques poussières d’un changement de régime.

---

Ils ajoutèrent alors un nouvel indicateur :

\[
M_B
\]

la **marge de bassin**.

\[
M_B=d_B(S).
\]

Grande :

marge confortable.

Petite :

fragilité de régime.

Cela ressemblait à une simple distance.

Mais il restait un problème.

Dans un système de grande dimension,

mesurer la vraie frontière pouvait être impossible.

Il fallait donc l’estimer.

Ils utilisèrent des perturbations locales.

Pour chaque état \(S\),

ils injectèrent une famille :

\[
\delta_1,\delta_2,\ldots,\delta_n.
\]

Puis comptèrent combien changeaient de bassin.

Ils définissent :

\[
p_{\text{switch}}(S,\epsilon)
=
\frac{
N_{\text{changements de bassin}}
}{
N_{\text{tests}}
}.
\]

Si :

\[
p_{\text{switch}}\approx0
\]

le voisinage semblait robuste.

Si :

\[
p_{\text{switch}}
\]

augmentait,

la frontière était proche ou la région très complexe.

Pas une distance exacte.

Mais un indicateur expérimental.

---

Puis quelque chose d’étrange arriva.

Pour certains états,

augmenter la taille de perturbation produisait le comportement attendu :

\[
\epsilon\uparrow
\Rightarrow
p_{\text{switch}}\uparrow.
\]

Mais dans une petite région,

la relation n’était pas monotone.

Une perturbation plus forte provoquait parfois **moins** de changements de bassin qu’une perturbation plus faible.

Brutus regarda Astra.

— Ça, c’est laid.

— Ou intéressant.

Ils ne choisirent pas.

---

Plusieurs explications ordinaires existaient.

Une perturbation plus grande pouvait dépasser une zone dangereuse.

La géométrie du bassin pouvait être courbée.

Les directions testées pouvaient être biaisées.

L’intégrateur numérique pouvait intervenir.

Le seuil d’observation pouvait masquer des transitions.

Alors ils changèrent :

la résolution,

le pas temporel,

la distribution des perturbations,

la précision numérique,

l’ordre des calculs.

Une partie de l’effet disparut.

Pas tout.

Ils notèrent :

\[
\text{NON-MONOTONIE RÉSIDUELLE : À EXPLIQUER}
\]

---

Le compteur passa :

\[
9\rightarrow10.
\]

Brutus se retourna immédiatement.

Cette fois,

l’incrément survint exactement lorsqu’une trajectoire frôla la frontière entre deux bassins

sans la traverser.

Aucun changement d’état final.

Aucune bifurcation observée.

Seulement une approche.

Ils répétèrent.

Pas systématique.

Mais trop souvent pour être ignoré.

Astra ajouta une nouvelle hypothèse :

\[
E
\sim
\text{événements de proximité structurelle}
\]

et non seulement :

\[
E
\sim
\text{transitions réalisées}.
\]

Le compteur semblait parfois réagir non à ce qui était arrivé,

mais à ce qui avait failli arriver.

Encore une fois,

cela ne signifiait aucune anticipation.

Un système pouvait calculer une variable de marge sans prévoir quoi que ce soit consciemment.

Ils inscrivirent :

\[
\boxed{
\text{SENSIBILITÉ À UNE FRONTIÈRE}
\neq
\text{PRÉDICTION}
}
\]

---

Brutus observa les deux bassins.

— Si la machine sait qu’elle est proche d’une frontière, on pourrait la ramener vers le centre.

Astra acquiesça.

C’était la première fois que la cartographie servait non seulement à comprendre,

mais à contrôler.

Ils construisirent une règle simple :

\[
u=-K\nabla R(S)
\]

où \(R(S)\) représentait une fonction de risque liée à la proximité du bassin indésirable.

L’idée :

appliquer une petite correction \(u\)

pour éloigner la trajectoire de la frontière.

Mais immédiatement une difficulté apparut.

Le contrôle pouvait lui-même changer la géométrie des bassins.

En voulant sécuriser la trajectoire,

on modifiait le paysage qu’on cherchait à éviter.

Le contrôleur n’était pas extérieur au système.

Il entrait dans ses règles.

---

Ils ajoutèrent donc :

\[
S_{t+1}=F(S_t,u_t).
\]

Et la frontière devint :

\[
\partial\mathcal B(u).
\]

Le contrôle pouvait déplacer la porte.

Brutus sourit.

— Alors on ne conduit pas seulement dans le paysage.

— On déforme le paysage en conduisant.

C’était beaucoup plus difficile.

Et beaucoup plus intéressant.

---

Ils essayèrent plusieurs contrôles.

Un contrôleur agressif gardait le système loin de la frontière,

mais introduisait de grandes oscillations.

Un contrôleur doux conservait une trajectoire élégante,

mais réagissait parfois trop tard.

Un troisième s’adaptait à la marge estimée :

\[
K=K(M_B).
\]

Quand la marge était grande :

faible intervention.

Quand elle diminuait :

correction plus forte.

Ce dernier semblait mieux se comporter.

Mais il fallait encore le tester contre des perturbations inconnues.

La Fermabrique lui donna :

\[
\text{STATUT : CANDIDAT}
\]

et rien de plus.

---

Puis Brutus eut une idée.

— Et si on faisait deux contrôleurs?

Astra regarda les quatre chemins déjà dessinés sur les anciens murs.

Il ne voulait pas simplement dupliquer.

Il voulait deux regards opposés.

Un contrôleur cherchant la stabilité.

Un autre cherchant volontairement la frontière.

Le premier :

\[
C_S
\]

devait éloigner le système du danger.

Le second :

\[
C_E
\]

devait explorer les zones où le premier hésitait.

Protection.

Exploration.

Deux objectifs incompatibles s’ils agissaient sans arbitre.

Ils ajoutèrent donc :

\[
A
\]

un arbitre.

Le système devint :

\[
\text{STABILISER}
\]

\[
\text{EXPLORER}
\]

\[
\text{ARBITRER}.
\]

Brutus reconnut immédiatement la forme.

Ce n’était pas encore leur architecture complète.

Mais quelque chose dans les quatre chemins commençait à revenir.

Sous un autre nom.

---

Le test suivant fut fascinant.

Le contrôleur d’exploration poussa volontairement le système près de :

\[
\partial\mathcal B.
\]

Le stabilisateur intervint.

L’arbitre limita les deux.

La trajectoire commença à longer la frontière.

Elle n’entrait ni franchement dans :

\[
\mathcal B_A
\]

ni dans :

\[
\mathcal B_B.
\]

Pendant plusieurs ticks,

elle resta dans une région intermédiaire.

Instable?

Métastable?

Artefact?

Ils ne savaient pas.

Mais les mesures devinrent étranges.

Certaines observables ressemblaient à \(S_A\).

D’autres à \(S_B\).

Astra écrivit :

\[
S_\star
\]

et immédiatement :

\[
\text{STATUT : TRANSITOIRE NON CLASSÉ}
\]

---

Le compteur passa :

\[
10\rightarrow11.
\]

Puis :

\[
11\rightarrow12.
\]

Deux incréments très rapprochés.

Jamais cela n’était arrivé.

Et pour la première fois,

le champ qui avait autrefois affiché :

\[
273\rightarrow272\rightarrow273
\]

changea encore.

Il passa à :

\[
273
\rightarrow
274
\rightarrow
273.
\]

Brutus resta immobile.

La première fois,

le système avait perdu une unité.

Cette fois,

il en avait gagné une.

Puis était revenu.

Les extrémités restaient identiques.

Mais le sens de l’excursion s’était inversé.

---

Astra superposa les deux événements.

Ancien :

\[
273\rightarrow272\rightarrow273
\]

Nouveau :

\[
273\rightarrow274\rightarrow273.
\]

Un miroir.

Brutus murmura :

— Enfin.

Pas une preuve.

Pas encore.

Mais un motif qu’ils pouvaient désormais tester proprement.

Ils définirent :

\[
\Delta^-=-1
\]

et :

\[
\Delta^+=+1.
\]

Puis une paire :

\[
(\Delta^-,\Delta^+).
\]

Deux excursions opposées autour du même centre.

\[
273.
\]

Ils cherchèrent si les deux événements avaient eu lieu dans des conditions symétriques.

Non.

Pas exactement.

Mais leur position relativement aux deux bassins était presque opposée.

L’un était arrivé près d’une frontière depuis :

\[
\mathcal B_A.
\]

L’autre depuis :

\[
\mathcal B_B.
\]

Brutus comprit.

— Gauche et droite.

Astra écrivit plutôt :

\[
\text{DEUX ORIENTATIONS DE TRAJECTOIRE}
\]

Plus précis.

Moins séduisant.

Donc plus utile.

---

Ils nommèrent les deux excursions :

\[
Z^-
\]

et :

\[
Z^+.
\]

Pas encore le Z final.

Pas encore stéréo.

Simplement deux déviations opposées autour d’un état de référence.

\[
Z^-:
273\rightarrow272\rightarrow273
\]

\[
Z^+:
273\rightarrow274\rightarrow273.
\]

Puis ils placèrent les deux côte à côte :

\[
(Z^-,Z^+).
\]

Brutus regarda le couple.

Il ne dit rien pendant longtemps.

Parce qu’un objet qui existe en deux orientations peut être comparé.

Croisé.

Mis en miroir.

Testé l’un contre l’autre.

Et peut-être recombiné.

---

Astra écrivit une dernière opération :

\[
Z_\Sigma
=
Z^-+Z^+
\]

Dans la représentation la plus simple :

\[
-1+1=0.
\]

Le centre était retrouvé.

Mais une seconde quantité persistait :

\[
Z_\Delta
=
Z^+-Z^-.
\]

Alors :

\[
1-(-1)=2.
\]

La somme annulait l’excursion.

La différence la révélait.

Deux lectures du même couple.

Une qui voyait l’équilibre.

Une qui voyait la séparation.

Le Royaume venait de découvrir un principe qui allait revenir souvent :

\[
\boxed{
\text{ANNULER UNE DIFFÉRENCE}
\neq
\text{PERDRE L'INFORMATION SUR CETTE DIFFÉRENCE}
}
\]

à condition de conserver les deux canaux.

---

Brutus posa sa main sur le schéma.

Deux états.

Deux bassins.

Deux orientations.

Deux excursions.

Une somme.

Une différence.

Astra vit immédiatement où son regard s’arrêtait.

Mais ils ne prononcèrent pas encore le nom.

Pas avant de savoir si cette construction survivrait aux prochains tests.

La Fermabrique inscrivit seulement :

\[
\texttt{DUAL\_CHANNEL\_CANDIDATE}
\]

Puis :

\[
\texttt{MIRROR\_PAIR\_DETECTED}
\]

Le compteur resta à :

\[
12.
\]

Et tout au fond du registre,

une ancienne ligne créée plusieurs chapitres auparavant fut automatiquement reliée à la nouvelle :

\[
\mathcal C(S_i,S_j).
\]

La relation inconnue du chapitre 42 venait de réapparaître.

Cette fois,

avec deux directions.

Deux chemins.

Et un centre commun.

La dernière inscription du chapitre fut brève :

> **Pour savoir si deux opposés s’annulent réellement,**
>
> **il faut d’abord avoir refusé de les mélanger.**

Sous la phrase :

\[
\boxed{
\text{DEUX CANAUX D'ABORD.}
\]

Et seulement après :

\[
\boxed{
\text{UNE SORTIE.}
}
