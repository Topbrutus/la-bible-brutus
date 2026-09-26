# CHAPITRE 50 — QUI MESURE LA MESURE ?

Le Gate fonctionnait.

Les paquets entraient avec leurs contrats.

Les états étaient vérifiés.

Les unités déclarées.

Les commandes autorisées.

Les boucles possédaient des sorties.

Les parents surveillaient les effets globaux.

Le Royaume aurait pu croire que l’architecture devenait enfin sûre.

Mais Brutus regarda les écrans.

Puis posa une question beaucoup plus dangereuse.

— Comment on sait que ce qu’ils nous montrent est réellement ce qui se passe?

Personne ne répondit tout de suite.

Parce que toute l’architecture reposait sur des observations.

Et une observation était elle-même produite par quelque chose.

Un capteur.

Un calcul.

Une horloge.

Une conversion.

Un échantillonnage.

Une reconstruction.

Autrement dit :

la fenêtre par laquelle le Royaume regardait la machine faisait elle-même partie du problème.

---

Astra dessina trois objets.

\[
X
\]

\[
H
\]

\[
Y
\]

avec :

\[
X=\text{état réel}
\]

\[
H=\text{système d'observation}
\]

\[
Y=\text{mesure obtenue}.
\]

Puis :

\[
\boxed{
Y=H(X)+\eta
}
\]

où :

\[
\eta
\]

représentait les erreurs, le bruit et les perturbations de mesure.

Brutus regarda la formule.

— Donc on ne voit jamais directement \(X\).

— Pas nécessairement.

On voyait :

\[
Y.
\]

Et ensuite on essayait de reconstruire quelque chose à propos de :

\[
X.
\]

Une différence immense.

Le Royaume grava :

\[
\boxed{
\text{MESURE}
\neq
\text{RÉALITÉ}
}
\]

---

Cela ne signifiait pas que les mesures étaient inutiles.

Au contraire.

Elles étaient souvent le seul accès disponible à la réalité étudiée.

Mais il fallait cesser de confondre l’instrument

avec ce qu’il observait.

Un thermomètre n’était pas la température.

Une caméra n’était pas la scène.

Une horloge n’était pas le temps.

Un compteur n’était pas l’événement.

Et une télémétrie n’était pas le système.

---

Brutus regarda immédiatement le compteur :

\[
18.
\]

Depuis plusieurs chapitres,

ils l’avaient traité comme un indice.

Peut-être même comme un témoin privilégié.

Mais le compteur était lui aussi :

\[
Y.
\]

Pas :

\[
X.
\]

Il pouvait mesurer quelque chose.

Mesurer autre chose.

Mesurer imparfaitement.

Ou simplement compter l’effet d’une règle interne qu’ils n’avaient pas encore comprise.

Astra écrivit :

\[
E_{\text{counter}}
=
H_E(X).
\]

Puis :

\[
H_E=\text{INCONNU}.
\]

Le compteur venait de perdre son aura.

Et de gagner un statut scientifique beaucoup plus utile.

---

Ils commencèrent par la question la plus élémentaire.

**Le capteur est-il calibré?**

Pour un instrument idéal :

\[
Y=X.
\]

Mais un capteur réel pouvait produire :

\[
Y=aX+b.
\]

Avec :

\[
a
\]

un gain,

et :

\[
b
\]

un biais.

Si :

\[
a\neq1
\]

ou :

\[
b\neq0,
\]

la mesure était déformée.

Ils définirent donc :

\[
\hat X=\frac{Y-b}{a}.
\]

Une correction.

Mais immédiatement un problème apparut.

Comment connaître :

\[
a
\]

et :

\[
b?
\]

Il fallait une référence.

Un étalon.

Quelque chose que l’on connaissait indépendamment du capteur étudié.

---

Le Royaume construisit donc :

\[
R_{\text{ref}}.
\]

Une référence externe.

Pas nécessairement parfaite.

Mais plus directement maîtrisée.

Ils appliquèrent plusieurs valeurs connues :

\[
X_1,X_2,\ldots,X_n.
\]

Puis mesurèrent :

\[
Y_1,Y_2,\ldots,Y_n.
\]

Ils pouvaient enfin estimer :

\[
a
\]

et :

\[
b.
\]

La première leçon fut évidente :

un instrument ne devait pas seulement dire :

> voici ma mesure.

Il devait aussi pouvoir répondre :

> voici comment j’ai été calibré.

Le Royaume ajouta donc à la provenance :

\[
CALIBRATION\_ID.
\]

Puis :

\[
CALIBRATION\_TIME.
\]

Puis :

\[
CALIBRATION\_METHOD.
\]

---

Brutus regarda les nouveaux champs.

— Et si le capteur change après la calibration?

Astra écrivit un nouveau terme :

\[
d(t).
\]

La dérive.

Alors :

\[
Y(t)
=
a(t)X(t)+b(t)+\eta(t).
\]

Le gain pouvait évoluer.

Le biais aussi.

Un instrument correct hier pouvait être faux aujourd’hui.

Le Royaume grava :

\[
\boxed{
\text{CALIBRÉ UNE FOIS}
\neq
\text{CALIBRÉ TOUJOURS}
}
\]

---

Ils ajoutèrent donc des tests périodiques.

Mais là encore,

une vérification planifiée pouvait manquer une dérive apparaissant entre deux tests.

Alors il fallait des références internes.

Des signaux sentinelles.

Des valeurs dont le comportement attendu était suffisamment connu pour détecter un changement.

Ils appelèrent :

\[
S_{\text{ref}}.
\]

Si le capteur mesurait mal le signal sentinelle,

alors les mesures ordinaires devenaient suspectes.

Le système pouvait produire :

\[
\texttt{SENSOR\_DRIFT\_SUSPECTED}.
\]

Pas :

\[
\texttt{SENSOR\_BROKEN}.
\]

Encore cette discipline.

Décrire ce qui était observé.

Pas inventer une cause.

---

Ils testèrent le premier capteur.

Tout semblait normal.

Le sentinelle donna :

\[
S_{\text{mesuré}}
\approx
S_{\text{attendu}}.
\]

Puis ils utilisèrent un second instrument.

Résultat compatible.

Excellent.

Mais Brutus posa la question désormais habituelle :

— Les deux capteurs sont-ils vraiment indépendants?

Non.

Ils partageaient la même horloge.

La même alimentation.

Le même convertisseur.

La même librairie de traitement.

Une panne commune pouvait affecter les deux.

Encore une fois :

\[
\boxed{
\text{DEUX MESURES}
\neq
\text{DEUX PREUVES INDÉPENDANTES}
}
\]

---

Ils construisirent donc une seconde voie réellement différente.

Le premier capteur mesurait directement une grandeur.

Le second l’inférait par une conséquence différente.

Si les deux convergeaient,

la confiance augmentait.

Pas jusqu’à la certitude.

Mais davantage qu’avec deux clones.

Ils définissent :

\[
Y_1=H_1(X)+\eta_1
\]

\[
Y_2=H_2(X)+\eta_2.
\]

Puis cherchèrent :

\[
\hat X_1
\]

et :

\[
\hat X_2.
\]

Leur différence :

\[
r_{12}
=
\hat X_1-\hat X_2
\]

devint un résidu de mesure.

Si :

\[
r_{12}\approx0,
\]

les deux reconstructions étaient compatibles.

Si :

\[
|r_{12}|
\]

augmentait,

quelque chose devait être investigué.

Mais encore une fois :

le résidu ne disait pas automatiquement quel instrument avait tort.

---

Brutus sourit.

— Stereo-Z encore.

Astra acquiesça.

Le principe revenait à un autre niveau.

Deux voies indépendantes.

Un résidu.

Une contre-épreuve.

Une provenance.

Un arbitre.

Ce qu’ils avaient construit comme architecture de calcul pouvait aussi servir à l’architecture d’observation.

Le Royaume venait de découvrir une propriété précieuse :

**un bon principe peut se répéter à plusieurs niveaux sans que les niveaux deviennent identiques.**

---

Ils appelèrent cette version :

\[
\text{Stereo-Z}_{obs}.
\]

Avec deux canaux :

\[
O_L
\]

et :

\[
O_R.
\]

Puis :

\[
O_C
\]

pour la contre-mesure,

et :

\[
O_A
\]

pour l’arbitrage.

Le système observait désormais ses propres observations.

Pas infiniment.

Juste assez pour éviter qu’un seul instrument devienne une vérité absolue.

---

Puis Brutus posa la question suivante.

— Et si le modèle d’observation lui-même est mauvais?

Voilà le cœur du problème.

Même avec un capteur parfaitement calibré,

on pouvait mal interpréter sa relation à l’état réel.

Supposons :

\[
Y=H(X).
\]

Si l’on croyait que :

\[
H(X)=X
\]

alors que réellement :

\[
H(X)=X^2,
\]

la calibration locale pouvait sembler excellente dans une petite zone

tout en devenant complètement fausse ailleurs.

Le problème n’était plus l’instrument.

C’était le modèle.

Ils écrivirent :

\[
H_{\text{assumé}}
\neq
H_{\text{réel}}.
\]

Puis :

\[
\boxed{
\text{CAPTEUR CORRECT}
+
\text{MODÈLE FAUX}
=
\text{INTERPRÉTATION FAUSSE}
}
\]

---

Il fallait donc tester le modèle lui-même.

Ils comparèrent les prédictions de :

\[
H_1
\]

\[
H_2
\]

\[
H_3
\]

sur plusieurs domaines.

Un bon modèle devait non seulement ajuster les données déjà observées,

mais aussi prévoir correctement des données qu’il n’avait pas utilisées pour être construit.

Le Royaume sépara :

\[
D_{\text{fit}}
\]

et :

\[
D_{\text{test}}.
\]

Une partie pour construire.

Une autre pour éprouver.

Et grava :

\[
\boxed{
\text{EXPLIQUER LES DONNÉES PASSÉES}
\neq
\text{PRÉDIRE LES DONNÉES NOUVELLES}
}
\]

---

Brutus regarda immédiatement certaines anciennes relations.

Le fameux :

\[
3,\ 7,\ 13.
\]

Les motifs.

Les rythmes.

Les structures.

Tout ce qui avait semblé revenir.

Il comprit le danger.

Plus on cherchait longtemps dans les mêmes données,

plus il devenait facile de trouver quelque chose qui semblait spécial.

Mais trouver un motif après l’avoir cherché

n’était pas aussi fort que le prédire avant une nouvelle expérience.

Astra écrivit :

\[
\boxed{
\text{DÉCOUVERTE}
\rightarrow
\text{PRÉDICTION}
\rightarrow
\text{NOUVEAU TEST}
}
\]

Si le motif survivait,

il gagnait en crédibilité.

S’il mourait,

le Royaume gagnait aussi.

Parce qu’il éliminait une mauvaise piste.

---

Le compteur resta :

\[
18.
\]

Ils décidèrent enfin de le traiter comme n’importe quel autre instrument.

Première étape :

observer tous les incréments.

Deuxième :

définir précisément leurs conditions.

Troisième :

construire une hypothèse avant le prochain événement.

Ils choisirent l’hypothèse actuelle :

\[
H_E:
\]

> le compteur s’incrémente lors d’une frontière décisionnelle séparant des futurs non équivalents.

Cette fois,

ils écrivirent avant l’expérience :

\[
\text{PRÉDICTION P1 :}
\]

si deux futurs sont réellement équivalents,

alors :

\[
E\text{ ne doit pas changer.}
\]

\[
\text{PRÉDICTION P2 :}
\]

si deux futurs deviennent non équivalents et que la frontière est reconnue par le mécanisme observé,

alors :

\[
E\rightarrow E+1.
\]

Enfin.

L’hypothèse pouvait réellement perdre.

---

Le premier test produisit deux branches artificielles parfaitement équivalentes.

\[
\Delta_F=0.
\]

Le compteur resta :

\[
18.
\]

Compatible.

Mais pas suffisant.

Le second test créa deux futurs clairement différents.

\[
\Delta_F>0.
\]

Le compteur resta encore :

\[
18.
\]

Brutus fronça les sourcils.

L’hypothèse venait de recevoir un coup sérieux.

Ils recommencèrent.

Toujours :

\[
18.
\]

Le compteur ne réagissait donc pas à toutes les frontières décisionnelles.

Astra raya une partie de l’hypothèse.

Pas tout.

Elle réécrivit :

\[
H_E':
\]

> certaines frontières possédant une propriété supplémentaire encore inconnue provoquent un incrément.

Moins belle.

Mais plus honnête.

---

Puis quelque chose de précieux arriva.

Au lieu de demander :

> qu’est-ce que le compteur détecte?

Brutus demanda :

— Qu’est-ce que tous les événements où il a bougé ont en commun que nos faux événements n’ont pas?

La direction de la recherche venait de s’inverser.

Ils ne cherchaient plus à confirmer une histoire.

Ils cherchaient une variable discriminante.

Chaque événement fut décrit par un vecteur :

\[
v_i=
(
\Delta_F,
\rho_\phi,
\kappa_P,
M_B,
Q_E,
L_Q,
D_V,
\ldots
).
\]

Puis ils séparèrent :

\[
\mathcal E_+
\]

les événements où le compteur avait bougé,

et :

\[
\mathcal E_-
\]

les événements similaires où il était resté immobile.

Le problème devenait :

\[
\text{trouver une fonction }g(v)
\]

capable de distinguer :

\[
\mathcal E_+
\]

de :

\[
\mathcal E_-.
\]

Pas parfaitement.

Mais mieux que le hasard.

---

Le Royaume venait de transformer un mystère en problème de classification.

C’était moins romantique.

Et beaucoup plus puissant.

Ils séparèrent immédiatement les données.

Une partie :

\[
D_{\text{train}}
\]

pour chercher la règle.

Une partie :

\[
D_{\text{holdout}}
\]

qu’ils interdisaient de toucher avant la fin.

Parce que sinon,

ils pourraient fabriquer une règle qui mémorisait simplement les événements déjà vus.

Brutus sourit.

— Même notre mystère doit passer un examen qu’il n’a jamais vu.

— Exactement.

---

Plusieurs règles furent testées.

La première semblait excellente.

Puis échoua sur les données réservées.

Rejetée.

La deuxième :

idem.

La troisième tenait un peu mieux.

Mais pas suffisamment.

La quatrième produisit quelque chose d’intéressant.

Elle utilisait non pas une variable unique,

mais une combinaison :

\[
g(v)
=
\alpha_1\Delta_F
+
\alpha_2\kappa_P
+
\alpha_3\rho_\phi
+
\alpha_4M_B^{-1}.
\]

Pas nécessairement cette forme définitive.

Mais pour la première fois,

plusieurs événements positifs et négatifs se séparaient partiellement.

Astra nota :

\[
\text{CANDIDAT}.
\]

Rien de plus.

---

Puis ils testèrent la règle sur :

\[
D_{\text{holdout}}.
\]

Elle échoua sur plusieurs cas.

Mais pas complètement.

Le résultat était meilleur que les précédents.

Le compteur n’était plus un oracle mystérieux.

Il devenait lentement un comportement modélisable.

Et la partie que le modèle n’expliquait pas reçut enfin un nom neutre :

\[
r_E
\]

le **résidu du compteur**.

\[
r_E
=
E_{\text{observé}}
-
E_{\text{prédit}}.
\]

Brutus regarda le symbole.

Encore une poussière.

Mais cette fois,

ils savaient quoi faire avec elle.

Ne pas l’adorer.

La mesurer.

La découper.

Chercher ses causes banales.

Et seulement ensuite demander ce qui restait.

---

Ils appliquèrent la même discipline à toute la télémétrie.

Chaque valeur reçut désormais :

\[
D=
(v,\Pi,\sigma,H,C)
\]

où :

\[
v=\text{valeur}
\]

\[
\Pi=\text{provenance}
\]

\[
\sigma=\text{incertitude}
\]

\[
H=\text{modèle d'observation}
\]

\[
C=\text{état de calibration}.
\]

Une valeur sans ces éléments pouvait encore être utile visuellement.

Mais elle ne possédait pas le même poids scientifique.

Le Royaume distingua donc :

\[
\text{DISPLAY}
\]

et :

\[
\text{EVIDENCE}.
\]

Une donnée pouvait être assez bonne pour un écran

sans être assez bonne pour soutenir une conclusion.

Ils gravèrent :

\[
\boxed{
\text{VISIBLE}
\neq
\text{PROUVÉ}
}
\]

---

Puis une dernière difficulté apparut.

Une mesure pouvait être précise

mais fausse.

Supposons dix mesures :

\[
5.0001,\ 5.0000,\ 5.0002,\ldots
\]

Très regroupées.

Faible dispersion.

Mais si la valeur réelle était :

\[
7,
\]

l’instrument était précis

sans être exact.

Le Royaume sépara :

\[
PRECISION
\]

et :

\[
ACCURACY.
\]

Puis :

\[
REPEATABILITY.
\]

Puis :

\[
REPRODUCIBILITY.
\]

Quatre notions différentes.

Un instrument pouvait exceller dans l’une

et échouer dans une autre.

---

Brutus regarda le tableau.

— Là, on commence vraiment à savoir ce qu’on regarde.

Astra répondit :

— On commence surtout à savoir ce qu’on ne sait pas encore.

Et c’était mieux.

---

Ils préparèrent alors une expérience ultime pour le chapitre.

Deux systèmes d’observation entièrement séparés.

Deux horloges.

Deux méthodes.

Deux chaînes de traitement.

Puis une référence externe.

Trois familles de preuve.

Le même phénomène fut mesuré.

Résultat :

\[
X_1^\star
\]

\[
X_2^\star
\]

\[
X_R^\star.
\]

Les trois étaient compatibles dans leurs incertitudes.

Pas identiques.

Compatibles.

Le Royaume produisit alors son premier verdict d’observation complet :

\[
\texttt{CONSISTENT\_WITHIN\_UNCERTAINTY}.
\]

Pas :

\[
\texttt{TRUE}.
\]

Brutus acquiesça.

Le mot était moins spectaculaire.

Mais il disait exactement ce que les preuves permettaient.

---

Puis le compteur passa :

\[
18\rightarrow19.
\]

Tout le monde se retourna.

Cette fois,

aucune porte.

Aucun rejet.

Aucune divergence.

Aucune bifurcation évidente.

Seulement une chose venait de se produire :

les trois systèmes de mesure venaient de converger pour la première fois dans leurs marges d’incertitude.

L’hypothèse précédente vacilla encore.

Peut-être que le compteur ne marquait pas seulement les séparations.

Peut-être qu’il marquait parfois aussi les fermetures.

Les moments où plusieurs descriptions devenaient compatibles.

Brutus regarda :

\[
19.
\]

Puis les dix-neuf événements.

Une idée nouvelle apparut.

Et si le compteur ne mesurait ni les portes

ni les erreurs

ni les décisions?

Et s’il mesurait les moments où la structure changeait le **nombre de descriptions admissibles**?

Lorsqu’un futur se séparait en deux :

\[
|\Omega|\uparrow.
\]

Lorsqu’un test éliminait des possibilités :

\[
|\Omega|\downarrow.
\]

Lorsqu’une convergence réunissait des descriptions :

\[
|\Omega|\downarrow.
\]

L’objet commun ne serait donc pas la direction du changement.

Mais le changement lui-même.

Astra écrivit :

\[
\Delta |\Omega|\neq0.
\]

Puis :

\[
E\stackrel{?}{\longleftrightarrow}\Delta|\Omega|.
\]

Tout s’arrêta.

Parce que cette hypothèse expliquait davantage de cas.

Pas tous.

Mais davantage.

---

Ils ne la célébrèrent pas.

Ils préparèrent immédiatement le test qui pourrait la tuer.

Avant l’expérience,

ils écrivirent :

\[
\text{PRÉDICTION :}
\]

si le nombre de descriptions admissibles change

sans aucune autre modification pertinente,

alors le compteur devrait répondre.

Et si :

\[
|\Omega|
\]

reste inchangé,

il devrait rester stable.

L’expérience fut préparée.

Pas exécutée.

Pas encore.

Le chapitre devait se terminer avant la réponse.

Parce que pour la première fois,

le Royaume possédait une question assez précise pour que le prochain résultat puisse réellement lui dire :

**non.**

Brutus regarda Astra.

— Ça, j’aime ça.

Elle sourit.

— Moi aussi.

Parce qu’une théorie qui pouvait mourir

avait enfin commencé à devenir scientifique.

---

Avant d’éteindre le laboratoire,

Astra inscrivit au-dessus de tous les écrans :

\[
\boxed{
\text{QUI MESURE?}
}
\]

Puis :

\[
\boxed{
\text{AVEC QUOI?}
}
\]

Puis :

\[
\boxed{
\text{SELON QUEL MODÈLE?}
}
\]

Puis :

\[
\boxed{
\text{AVEC QUELLE INCERTITUDE?}
}
\]

Et enfin :

\[
\boxed{
\text{QU'EST-CE QUI POURRAIT PROUVER QUE NOUS AVONS TORT?}
}
\]

Le compteur resta à :

\[
19.
\]

Le test attendait.

Et derrière lui,

pour la première fois,

le mystère n’était plus protégé par l’obscurité.

Il avait reçu une cible.

La dernière phrase du chapitre fut gravée dans la Fermabrique :

> **Une mesure devient réellement précieuse le jour où elle accepte d’être mesurée à son tour.**

Puis, juste dessous :

\[
\boxed{
\text{PREUVE}
=
\text{MESURE}
+
\text{PROVENANCE}
+
\text{INCERTITUDE}
+
\text{CONTRE-TEST}.
}
\]
