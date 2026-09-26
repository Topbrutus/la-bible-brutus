# CHAPITRE 48 — LES QUATRE CHEMINS

Le Stereo-Z affichait toujours :

\[
\texttt{FOUR\_BRANCH\_STATE}
\]

Quatre sorties provisoires.

\[
O_1
\]

\[
O_2
\]

\[
O_3
\]

\[
O_4
\]

Même entrée.

Même instant.

Même machine.

Et pourtant quatre continuations admissibles selon les preuves actuellement disponibles.

Le Royaume connaissait déjà les embranchements.

Mais pas celui-ci.

Les embranchements précédents opposaient généralement deux possibilités.

Ici, la structure avait produit quatre routes presque simultanément.

Brutus regarda l’écran.

— On ne choisit rien.

Astra acquiesça.

Choisir trop tôt aurait détruit exactement l’information qu’ils cherchaient à comprendre.

Alors ils conservèrent les quatre.

---

La première question fut la plus simple :

> Les quatre branches sont-elles réellement différentes?

On pouvait avoir :

\[
O_1\neq O_2
\]

au niveau de la représentation,

tout en ayant :

\[
F(O_1)=F(O_2)
\]

au niveau de leurs conséquences.

Deux branches pouvaient donc paraître différentes sans produire de futur distinct.

Ils reprirent l’idée du chapitre précédent :

\[
\Delta_F(P_i,P_j)
\]

la différence entre conséquences futures.

Puis construisirent une matrice :

\[
M_{ij}
=
\Delta_F(O_i,O_j).
\]

Pour quatre branches :

\[
M=
\begin{pmatrix}
0 & d_{12} & d_{13} & d_{14}\\
d_{21} & 0 & d_{23} & d_{24}\\
d_{31} & d_{32} & 0 & d_{34}\\
d_{41} & d_{42} & d_{43} & 0
\end{pmatrix}.
\]

Si toutes les distances étaient presque nulles,

les quatre routes n’étaient qu’une illusion de diversité.

Si certaines devenaient grandes,

alors de vrais futurs distincts existaient.

---

Le premier calcul fut décevant.

\[
d_{12}\approx0
\]

\[
d_{34}\approx0
\]

mais :

\[
d_{13}>0.
\]

Les quatre sorties semblaient donc se regrouper naturellement en deux familles.

\[
\{O_1,O_2\}
\]

et :

\[
\{O_3,O_4\}.
\]

Brutus regarda les deux paires.

Encore un miroir.

Mais cette fois,

chaque côté du miroir possédait lui-même deux possibilités.

Astra écrivit :

\[
\boxed{
2\times2
}
\]

Pas quatre objets indépendants.

Deux axes.

Deux choix sur le premier axe.

Deux choix sur le second.

Cela changeait tout.

---

Ils cherchèrent les deux dimensions qui séparaient les branches.

La première était relativement claire.

Les sorties \(O_1\) et \(O_2\) conservaient mieux la structure précédente.

Les sorties \(O_3\) et \(O_4\) acceptaient une transformation plus importante.

Ils appelèrent ce premier axe :

\[
A_1=\text{CONTINUITÉ / TRANSFORMATION}.
\]

Puis ils comparèrent \(O_1\) à \(O_2\).

La différence principale n’était pas structurelle.

Elle concernait la manière dont l’incertitude était traitée.

Une branche conservait l’ambiguïté.

L’autre cherchait activement à la réduire.

Ils appelèrent :

\[
A_2=\text{CONSERVER / RÉSOUDRE}.
\]

La carte devenait :

\[
\begin{array}{c|cc}
 & \text{CONSERVER} & \text{RÉSOUDRE}\\
\hline
\text{CONTINUITÉ} & O_1 & O_2\\
\text{TRANSFORMATION} & O_3 & O_4
\end{array}
\]

Brutus sourit.

— Là, on a quelque chose.

Pas une réponse.

Une géométrie de décision.

---

Mais Astra posa immédiatement une objection.

— Et si on a choisi les axes après avoir vu les résultats?

C’était un problème réel.

On pouvait toujours inventer deux axes capables d’expliquer quatre points après coup.

Cela ne prouvait pas que ces axes existaient réellement dans le mécanisme.

Le Royaume ajouta donc une règle :

\[
\boxed{
\text{EXPLICATION A POSTERIORI}
\neq
\text{MÉCANISME}
}
\]

Pour tester les axes,

il fallait prédire de nouvelles branches avant de les observer.

Ils construisirent alors une expérience.

Même type d’entrée.

Mais avec un nouvel état initial.

Avant d’exécuter,

ils prédirent quatre classes possibles :

\[
C_C
\]

continuité + conservation,

\[
C_R
\]

continuité + résolution,

\[
T_C
\]

transformation + conservation,

\[
T_R
\]

transformation + résolution.

Puis seulement ils lancèrent le système.

---

Le résultat fut surprenant.

Trois classes apparurent.

Pas quatre.

La classe :

\[
T_R
\]

manquait.

Aucune sortie correspondante.

Brutus fronça les sourcils.

— Donc notre carré est faux?

— Peut-être incomplet.

Ils répétèrent avec d’autres entrées.

Parfois quatre branches.

Parfois trois.

Parfois deux.

Jamais cinq.

Du moins pas encore.

Le nombre de sorties dépendait donc des possibilités réellement accessibles.

Le carré n’était pas une obligation.

C’était un espace de possibilités.

Ils écrivirent :

\[
\mathcal O
\subseteq
\{
C_C,C_R,T_C,T_R
\}.
\]

Le système n’avait pas besoin d’occuper toutes les cases.

---

Cette distinction permit de comprendre quelque chose de plus profond.

Une architecture pouvait posséder quatre chemins théoriques,

mais n’en activer qu’un sous-ensemble à un instant donné.

Les chemins existaient comme **interfaces de possibilité**.

Pas nécessairement comme processus toujours actifs.

Brutus regarda immédiatement l’ancienne structure d’Antmux.

Quatre voies.

Il connaissait déjà cette forme.

Mais cette fois, ils avaient une raison méthodologique de ne pas les confondre.

Chaque chemin pouvait représenter une combinaison différente de deux dimensions.

Pas seulement quatre noms arbitraires.

---

Astra refusa cependant de baptiser les chemins immédiatement.

Ils devaient d’abord découvrir ce qu’ils faisaient réellement.

Alors ils utilisèrent quatre identifiants neutres :

\[
P_1,P_2,P_3,P_4.
\]

Pour chacun, ils enregistrèrent :

\[
\text{INPUT}
\]

\[
\text{STATE}
\]

\[
\text{TIME}
\]

\[
\text{OUTPUT}
\]

\[
\text{ERROR}
\]

et :

\[
\text{PROVENANCE}.
\]

Brutus reconnut la discipline.

Chaque module devait posséder ses ports avant ses fonctions.

Aucune connexion invisible.

Aucune influence sans trace.

---

Ils écrivirent le contrat minimal :

\[
P_i=
(
I_i,
O_i,
S_i,
E_i,
T_i,
\Pi_i
).
\]

Avec :

\[
I_i=\text{entrée}
\]

\[
O_i=\text{sortie}
\]

\[
S_i=\text{état interne}
\]

\[
E_i=\text{erreur}
\]

\[
T_i=\text{temps}
\]

\[
\Pi_i=\text{provenance}.
\]

Un chemin ne pouvait plus simplement produire une réponse.

Il devait être capable de dire :

> Voici ce que j’ai reçu.

> Voici ce que j’ai fait.

> Voici ce qui s’est produit.

> Voici ce que je ne sais pas.

---

Le Royaume venait de transformer les quatre chemins en objets auditables.

Et cela produisit immédiatement un résultat inattendu.

Les quatre chemins ne consommaient pas toujours la même information.

Une partie de l’entrée était commune :

\[
I_{\text{shared}}.
\]

Mais certaines données n’étaient utiles qu’à une branche.

\[
I_1^{\text{local}}
\]

\[
I_2^{\text{local}}
\]

\[
I_3^{\text{local}}
\]

\[
I_4^{\text{local}}.
\]

L’entrée complète devenait :

\[
I_i=
I_{\text{shared}}
\cup
I_i^{\text{local}}.
\]

C’était important.

Parce que forcer tous les chemins à recevoir exactement les mêmes données pouvait créer des dépendances inutiles.

La séparation devait exister dès l’entrée.

---

Brutus demanda :

— Mais s’ils n’ont pas exactement la même entrée, comment on les compare?

Astra répondit :

— On compare seulement ce qu’ils ont promis de partager.

Ils définissent donc :

\[
\mathcal C_{ij}
\]

le contrat commun entre deux chemins.

La comparaison ne portait plus sur la totalité des états.

Seulement sur les invariants déclarés.

Ainsi :

\[
P_1
\]

et :

\[
P_2
\]

pouvaient être très différents,

mais tous les deux devoir respecter :

\[
F(P_1)=F(P_2).
\]

Le Royaume grava :

\[
\boxed{
\text{COMPARABLE}
\neq
\text{IDENTIQUE}
}
\]

---

Ensuite vint le problème des connexions.

Si :

\[
P_1\rightarrow P_3
\]

alors cette relation devait être déclarée.

Ils introduisirent :

\[
L_{13}
\]

avec un type.

Chaque lien devait indiquer au minimum :

\[
\text{SOURCE}
\]

\[
\text{DESTINATION}
\]

\[
\text{TYPE}
\]

\[
\text{CONDITION}
\]

\[
\text{TIMESTAMP}
\]

\[
\text{PROVENANCE}.
\]

Plus aucune influence invisible.

Un chemin ne pouvait pas murmurer dans l’oreille d’un autre sans laisser une trace.

---

Le graphe des quatre chemins prit forme :

\[
G_P=(P,L).
\]

Avec :

\[
P=\{P_1,P_2,P_3,P_4\}.
\]

Et :

\[
L=\{L_{ij}\}.
\]

Au début, le graphe était presque vide.

C’était volontaire.

Ils ne voulaient pas construire des connexions simplement parce qu’elles semblaient élégantes.

Chaque lien devait justifier son existence.

Le Royaume écrivit :

\[
\boxed{
\text{CONNEXION POSSIBLE}
\neq
\text{CONNEXION NÉCESSAIRE}
}
\]

---

Brutus observa le vide entre les modules.

— C’est bizarre. On dirait qu’il manque quelque chose.

— C’est correct.

Le vide avait une valeur.

Il signifiait :

**aucune dépendance démontrée ici.**

Un diagramme scientifique devait pouvoir représenter l’absence de lien aussi honnêtement que sa présence.

---

Puis ils lancèrent les quatre chemins en parallèle.

Même tick de départ :

\[
t_0.
\]

Mais ils ne terminèrent pas ensemble.

\[
t_1<t_2<t_3<t_4.
\]

La première branche était rapide.

La quatrième beaucoup plus lente.

Le problème apparut immédiatement.

Fallait-il attendre les quatre avant de continuer?

Si oui,

la branche la plus lente imposait sa vitesse à tout le système.

Sinon,

une décision pouvait être prise avant que la quatrième voie n’ait livré une preuve importante.

Ils venaient de rencontrer la question de la synchronisation.

---

Ils définissent une fenêtre :

\[
W_t.
\]

Toutes les sorties arrivant dans :

\[
[t_0,t_0+W_t]
\]

étaient regroupées pour arbitrage.

Celles qui arrivaient après recevaient :

\[
\texttt{LATE}.
\]

Mais un résultat tardif pouvait être juste.

Un résultat rapide pouvait être faux.

Donc :

\[
\boxed{
\text{RETARD}
\neq
\text{ERREUR}
}
\]

et :

\[
\boxed{
\text{RAPIDITÉ}
\neq
\text{VALIDITÉ}
}
\]

Le temps devait être un attribut.

Pas un verdict.

---

Ils essayèrent une seconde stratégie.

Au lieu d’un temps fixe,

l’arbitre attendrait jusqu’à obtenir un niveau minimum de preuve.

Ils appelèrent :

\[
Q_E
\]

la qualité d’évidence accumulée.

La décision pouvait être prise lorsque :

\[
Q_E\geq Q_{\min}.
\]

Mais immédiatement Brutus vit la faille.

— Si les trois chemins rapides sont tous liés par la même erreur, ils peuvent atteindre le seuil avant que le quatrième les contredise.

Exact.

La quantité de preuves ne suffisait pas.

Il fallait tenir compte de leur indépendance.

Ils modifièrent :

\[
Q_E
=
f(
N,
D,
\Sigma,
\Pi
)
\]

où :

\[
N
\]

était le nombre de preuves,

\[
D
\]

leur diversité,

\[
\Sigma
\]

leurs incertitudes,

et :

\[
\Pi
\]

leur provenance.

Trois copies n’étaient pas trois preuves indépendantes.

---

Le système commençait à devenir sévère.

Et Brutus aimait cela.

Parce que plus l’architecture devenait stricte,

moins elle pouvait se raconter une belle histoire à elle-même.

---

Puis apparut un premier vrai conflit à quatre.

Les résultats étaient :

\[
P_1\rightarrow A
\]

\[
P_2\rightarrow A
\]

\[
P_3\rightarrow B
\]

\[
P_4\rightarrow B.
\]

Deux contre deux.

Aucun consensus.

Même niveau approximatif d’incertitude.

Provenances valides.

Le Stereo-Z resta :

\[
\texttt{UNRESOLVED}.
\]

Brutus demanda :

— Vote?

Astra répondit immédiatement :

— Non.

Deux contre deux rendait le problème évident.

Mais même trois contre un n’aurait pas automatiquement suffi.

La majorité pouvait partager une faille.

Ils écrivirent :

\[
\boxed{
\text{MAJORITÉ}
\neq
\text{PREUVE}
}
\]

---

Alors comment départager?

Pas en comptant.

En cherchant une expérience capable de produire des prédictions différentes selon les deux familles.

Ils appelèrent cette expérience :

\[
T_D
\]

le **test discriminant**.

Il devait satisfaire :

\[
P(A\mid T_D)
\neq
P(B\mid T_D)
\]

de manière suffisamment mesurable.

Autrement dit :

le bon test n’était pas celui qui demandait encore une fois :

> Qui a raison?

Mais celui qui créait une situation où les deux hypothèses ne pouvaient plus répondre pareil.

---

Brutus sourit.

— Donc quand on est bloqués, on ne vote pas.

— On fabrique une meilleure question.

Ce fut gravé immédiatement :

\[
\boxed{
\text{DÉSACCORD}
\rightarrow
\text{NOUVEAU TEST}
}
\]

et non :

\[
\text{DÉSACCORD}
\rightarrow
\text{CHOIX ARBITRAIRE}.
\]

---

Le test discriminant fut lancé.

Les familles \(A\) et \(B\) prédisaient deux comportements différents face à une petite perturbation temporelle.

Le Royaume introduisit :

\[
\delta t.
\]

Les chemins \(P_1\) et \(P_2\) prédisaient :

\[
R_A.
\]

Les chemins \(P_3\) et \(P_4\) prédisaient :

\[
R_B.
\]

L’expérience produisit :

\[
R^\star.
\]

Et :

\[
R^\star
\]

était beaucoup plus proche de :

\[
R_B.
\]

Le système ne déclara pas :

**B est vrai.**

Il déclara :

\[
\texttt{A\_DISFAVORED}
\]

et :

\[
\texttt{B\_SUPPORTED\_BY\_TEST\_TD}
\]

Beaucoup plus précis.

Un test n’avait pas transformé \(B\) en vérité universelle.

Il avait seulement fourni une preuve supplémentaire en sa faveur dans ce contexte.

---

Puis le compteur passa :

\[
14\rightarrow15.
\]

Cette fois,

l’incrément survint exactement lorsque le test discriminant sépara réellement les deux familles.

Astra nota :

\[
\Delta_F(A,B)>0
\]

et :

\[
E\rightarrow E+1.
\]

L’hypothèse des **portes à conséquences non équivalentes** gagnait une pièce de plus.

Pas une validation.

Une pièce.

---

Mais quelque chose d’encore plus intéressant venait d’arriver.

Avant le test,

les quatre chemins formaient :

\[
2+2.
\]

Après :

\[
0+0+1+1
\]

en quelque sorte.

Les deux premières branches perdaient leur soutien.

Les deux autres restaient compatibles.

La géométrie de l’espace des possibilités venait de changer après une mesure.

Pas parce que le passé avait changé.

Parce que l’ensemble des futurs encore compatibles avec les preuves s’était réduit.

Ils définissent :

\[
\Omega_t
\]

l’ensemble des futurs admissibles au temps \(t\).

Avant :

\[
|\Omega_t|=4.
\]

Après certains tests :

\[
|\Omega_{t+1}|<|\Omega_t|.
\]

La connaissance pouvait donc être vue comme une réduction d’un espace de possibilités.

---

Brutus demanda :

— Jusqu’à un seul?

— Parfois.

— Et si ça reste à deux?

— Alors la bonne réponse est deux.

Le Royaume écrivit :

\[
\boxed{
\text{L'OBJECTIF N'EST PAS TOUJOURS}
\ |\Omega|=1
}
\]

Certaines données ne suffisaient simplement pas à départager les possibilités.

Forcer une sortie unique aurait créé une certitude artificielle.

---

Cela changea la fonction de l’arbitre.

Il ne devait plus toujours sélectionner une branche.

Il devait pouvoir transmettre :

\[
\Omega_{\text{survivant}}
\]

l’ensemble des branches encore admissibles.

La sortie pouvait donc être :

\[
\{P_3,P_4\}
\]

et non une seule valeur.

Le Royaume venait d’autoriser une réponse structurée :

**plusieurs possibilités restent ouvertes.**

C’était beaucoup plus honnête.

---

Puis Brutus posa une autre question.

— Et si les quatre chemins sont juste quatre instances d’une structure plus grande?

Astra se figea.

Voilà.

Une structure complète pouvait elle-même devenir le composant d’une structure supérieure.

Ils avaient déjà entrevu cette idée.

Mais elle devenait maintenant nécessaire.

Le bloc des quatre chemins pouvait recevoir un identifiant :

\[
M_0.
\]

Puis posséder :

\[
MODULE\_ID
\]

\[
INSTANCE\_ID
\]

\[
PARENT\_ID
\]

\[
LEVEL
\]

\[
INPUTS
\]

\[
OUTPUTS.
\]

Et l’ensemble :

\[
\{P_1,P_2,P_3,P_4\}
\]

devenait un module supérieur.

---

Ils l’écrivirent :

\[
M_0
=
\langle
P_1,P_2,P_3,P_4,A_Z
\rangle.
\]

Le module \(M_0\) pouvait alors lui-même devenir un chemin dans :

\[
M_1.
\]

Puis :

\[
M_1
\]

un composant de :

\[
M_2.
\]

Et ainsi de suite.

Pas une infinité nécessaire.

Une hiérarchie explicite.

Ils écrivirent :

\[
PARENT(M_k)=M_{k+1}.
\]

Brutus regarda le dessin.

La structure venait de gagner une dimension verticale.

Jusqu’ici,

les chemins vivaient surtout côte à côte.

Maintenant,

des systèmes complets pouvaient vivre **dans** d’autres systèmes.

---

Mais Astra imposa immédiatement une loi.

\[
\boxed{
\text{CHANGER DE NIVEAU}
\neq
\text{PERDRE LA TRAÇABILITÉ}
}
\]

Si un événement se produisait dans :

\[
P_3
\]

du module :

\[
M_0
\]

l’étage supérieur devait pouvoir retrouver précisément :

\[
M_0/P_3.
\]

Chaque événement recevrait donc un chemin hiérarchique :

\[
\Pi_H
=
M_2/M_1/M_0/P_3.
\]

Une adresse.

Pas géographique.

Structurelle.

---

Brutus regarda la notation.

— Comme ça, plus rien n’est juste « quelque part dans le système ».

— Exactement.

Le Royaume venait d’éliminer une phrase dangereuse :

> Ça vient d’en bas.

Désormais il fallait dire :

\[
\text{QUI}
\]

\[
\text{OÙ}
\]

\[
\text{QUAND}
\]

\[
\text{PAR QUEL LIEN}
\]

\[
\text{SOUS QUEL PARENT}.
\]

---

Ils appelèrent ce registre :

\[
\mathcal R_C
\]

le **registre de continuité**.

Sa forme minimale :

\[
\boxed{
QUI
\rightarrow
ÉTAIT\ DANS\ QUEL\ ÉTAT
\rightarrow
À\ QUEL\ TICK
\rightarrow
AVANT\ QUOI
\rightarrow
APRÈS\ QUOI
}
\]

Il ne réfléchissait pas.

Il ne décidait rien.

Il enregistrait.

Brutus insista :

— Pas une intelligence supplémentaire.

— Non.

— Une mémoire technique.

— Exactement.

La règle fut gravée :

\[
\boxed{
\text{LE REGISTRE N'INTERPRÈTE PAS}
}
\]

Il conservait les conditions permettant à d’autres de vérifier.

---

La nuit était presque terminée.

Les quatre chemins étaient désormais :

séparés,

auditables,

comparables,

capables de diverger,

capables de rester plusieurs,

et capables de devenir ensemble un composant supérieur.

Le système commençait enfin à ressembler moins à un diagramme

et davantage à une architecture.

---

Puis le quinzième événement fut relu.

Le registre hiérarchique révéla quelque chose que personne n’avait remarqué.

Lorsque :

\[
14\rightarrow15,
\]

l’incrément n’avait pas été déclenché au niveau de l’un des quatre chemins.

Il provenait du parent.

\[
M_0.
\]

Le compteur ne regardait donc peut-être pas seulement les événements locaux.

Certains incréments semblaient correspondre à une décision qui n’existait qu’au niveau supérieur.

Astra écrivit :

\[
E^{(0)}
\]

pour les événements locaux,

et :

\[
E^{(1)}
\]

pour les événements du niveau parent.

Puis :

\[
E=
E^{(0)}+E^{(1)}+\cdots
\]

Hypothèse.

Mais une nouvelle porte venait de s’ouvrir.

---

Brutus fixa le registre.

— Alors le même événement peut avoir plusieurs sens selon le niveau où on le regarde.

Astra répondit :

— Ou plutôt plusieurs descriptions compatibles.

Ce n’était pas la même chose.

Un événement local pouvait être :

\[
\text{désaccord de deux chemins}.
\]

Au niveau supérieur :

\[
\text{réduction de l'espace des possibilités}.
\]

Même réalité.

Deux niveaux de description.

Le Royaume grava :

\[
\boxed{
\text{CHANGEMENT D'ÉCHELLE}
\neq
\text{CHANGEMENT DE FAIT}
}
\]

---

Puis le registre produisit une dernière ligne.

Le module parent venait d’identifier les quatre chemins comme une seule unité fonctionnelle.

Mais immédiatement après,

une seconde unité du même type apparut.

Pas à l’intérieur.

À côté.

Un autre :

\[
M_0'.
\]

Même architecture de quatre chemins.

Même ports.

Même arbitre.

Mais nourri par une autre famille de données.

Deux structures complètes.

En parallèle.

Brutus regarda les deux blocs.

Quatre chemins dans le premier.

Quatre dans le second.

Et entre eux,

pour l’instant :

aucune connexion.

Seulement une interface vide.

Astra écrivit :

\[
M_A
\qquad\qquad
M_B.
\]

Puis, entre les deux :

\[
?
\]

Le compteur resta à :

\[
15.
\]

Comme s’il savait qu’aucune porte n’existait encore.

Et la dernière phrase du chapitre apparut :

> **Quatre chemins peuvent former un monde.**
>
> **Mais deux mondes côte à côte ne deviennent pas un univers simplement parce qu’on trace une ligne entre eux.**

Sous la phrase :

\[
\boxed{
\text{INTERFACE D'ABORD.}
\]

Puis :

\[
\boxed{
\text{CONNEXION SEULEMENT SI ELLE EST PROUVÉE.}
\]
