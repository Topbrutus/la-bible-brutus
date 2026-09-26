# CHAPITRE 45 — LES CHEMINS QUI CASSENT

Le registre affichait toujours :

\[
\texttt{PATH\_CLASS\_UNRESOLVED}
\]

et personne n’avait encore réussi à le faire disparaître.

Le problème était simple à écrire.

Beaucoup moins simple à résoudre.

Deux chemins pouvaient produire :

\[
x\rightarrow y
\]

avec exactement la même entrée

et exactement la même sortie.

Mais lorsqu’on perturbait légèrement leur intérieur,

ils ne réagissaient pas de la même façon.

L’un encaissait.

L’autre amplifiait.

L’un revenait.

L’autre s’éloignait.

Le Royaume avait donc besoin d’une distinction nouvelle.

Pas entre :

\[
\text{vrai}
\]

et :

\[
\text{faux}
\]

Mais entre :

\[
\text{stable}
\]

et :

\[
\text{fragile}
\]

---

Astra reprit le symbole introduit la veille :

\[
\kappa_P
\]

la sensibilité d’un chemin \(P\) à une perturbation.

Mais une seule valeur ne suffisait pas.

Une route pouvait être stable face au bruit,

et fragile face au temps.

Stable face à une variation d’entrée,

mais fragile face à une modification interne.

Stable localement,

mais catastrophique après accumulation.

Il fallait donc éclater la notion.

Ils écrivirent :

\[
\vec{\kappa}_P
=
(
\kappa_x,
\kappa_t,
\kappa_s,
\kappa_n,
\kappa_m
)
\]

où :

\[
\kappa_x
=
\text{sensibilité à l'entrée}
\]

\[
\kappa_t
=
\text{sensibilité temporelle}
\]

\[
\kappa_s
=
\text{sensibilité structurelle}
\]

\[
\kappa_n
=
\text{sensibilité au bruit}
\]

\[
\kappa_m
=
\text{sensibilité à la mémoire interne}
\]

Le chemin n’avait plus une fragilité.

Il possédait un **profil de fragilité**.

---

Brutus regarda les cinq composantes.

— Et on fait quoi avec ça?

— On les attaque.

La réponse était presque joyeuse.

Parce qu’un système qu’on protège de toute perturbation ne montre jamais ce qu’il vaut réellement.

Le Royaume construisit alors une batterie de coups.

Des petites erreurs.

Des délais.

Des inversions.

Des suppressions.

Des duplications.

Des réordonnancements.

Des valeurs proches des limites.

Et surtout :

des perturbations trop petites pour être visibles immédiatement.

Ils appelèrent l’ensemble :

\[
\mathcal A
=
\{
a_1,a_2,\ldots,a_n
\}
\]

les **attaques de robustesse**.

Pas pour détruire la machine.

Pour lui demander :

> Qu’est-ce qui te fait perdre ton identité?

---

Le premier chemin survécut presque à tout.

Ils augmentèrent le bruit.

Il tint.

Ils décalèrent le temps.

Il compensa.

Ils modifièrent légèrement l’entrée.

Il dévia, puis revint.

Sa sortie restait dans une région tolérable :

\[
\|y'-y\|<\epsilon
\]

pour de petites perturbations :

\[
\|\delta\|<\eta
\]

Astra nota :

\[
P_A=\text{robuste candidat}
\]

Le mot **candidat** resta obligatoire.

---

Le second chemin semblait identique.

Même sortie nominale.

Même comportement lorsque tout allait bien.

Puis ils injectèrent une variation presque ridicule :

\[
\delta=10^{-6}
\]

La sortie changea peu.

Ils recommencèrent :

\[
\delta=10^{-7}
\]

Toujours rien d’alarmant.

Puis :

\[
\delta=10^{-8}
\]

et soudain,

une variable intermédiaire se mit à osciller.

Pas la sortie.

Pas encore.

Seulement une valeur interne.

Puis deux.

Puis quatre.

Le phénomène semblait se calmer.

Puis réapparaissait plusieurs ticks plus tard.

Comme une fissure invisible sous une peinture intacte.

Le Royaume venait de rencontrer un autre type de fragilité :

**la fragilité retardée.**

Ils écrivirent :

\[
\kappa_P(t)
\]

La sensibilité dépendait du temps.

Ce qui semblait stable à :

\[
t_0
\]

pouvait devenir instable à :

\[
t_0+\Delta t
\]

---

Brutus tapa sur la table.

— Alors le test instantané ne vaut rien.

Astra corrigea :

— Il vaut quelque chose.

Elle ajouta :

— Mais il ne vaut pas tout.

Une vérité expérimentale commençait à prendre forme.

\[
\boxed{
\text{PASSER UN TEST}
\neq
\text{ÊTRE ROBUSTE}
}
\]

Un système pouvait réussir un test parce que le test ne durait pas assez longtemps.

Ou parce qu’il n’attaquait pas le bon axe.

Ou parce que la perturbation arrivait au mauvais endroit.

Ou parce que la sortie finale masquait une instabilité interne.

---

Ils construisirent alors une nouvelle mesure :

\[
R_P(T)
\]

la robustesse observée du chemin pendant une durée \(T\).

Puis :

\[
R_P(T,\mathcal A)
\]

lorsqu’il était soumis à un ensemble d’attaques.

Le résultat n’était plus :

\[
PASS
\]

ou :

\[
FAIL
\]

mais une surface.

Un paysage.

Certains chemins étaient très robustes dans une région

et presque inutilisables dans une autre.

Ils découvrirent alors quelque chose d’important.

Un chemin pouvait être plus rapide,

plus propre,

et même plus précis dans les conditions nominales,

tout en étant beaucoup plus fragile dès que les conditions réelles s’éloignaient légèrement du scénario parfait.

La meilleure performance n’était donc pas forcément la meilleure architecture.

Ils inscrivirent :

\[
\boxed{
\text{PERFORMANCE NOMINALE}
\neq
\text{ROBUSTESSE}
}
\]

---

Puis Brutus posa une question différente.

— Est-ce qu’un chemin fragile peut devenir robuste si on le divise?

Astra s’arrêta.

La question changeait la géométrie entière du problème.

Au lieu d’un chemin :

\[
P
\]

on pouvait construire :

\[
P=
P_1\circ P_2\circ P_3
\]

et placer des contrôles entre les segments.

Après chaque sous-chemin :

\[
C_1,C_2,C_3
\]

des points de vérification.

Le chemin devenait :

\[
x
\rightarrow
P_1
\rightarrow
C_1
\rightarrow
P_2
\rightarrow
C_2
\rightarrow
P_3
\rightarrow
C_3
\rightarrow
y
\]

Chaque contrôle pouvait détecter une divergence avant qu’elle n’atteigne la sortie.

Cela ressemblait à une évidence.

Mais immédiatement une autre question apparut :

**le contrôle lui-même pouvait-il introduire une perturbation?**

Bien sûr.

Tout observateur faisait partie de l’expérience.

Même en informatique, mesurer pouvait modifier :

temps,

ordre,

cache,

charge,

latence,

mémoire.

Le Royaume devait donc quantifier non seulement le chemin,

mais le coût de sa surveillance.

Ils écrivirent :

\[
\Omega(C)
=
\text{perturbation induite par le contrôle}
\]

et une nouvelle règle :

\[
\boxed{
\text{OBSERVER}
\neq
\text{NEUTRE}
}
\]

---

Le problème devenait maintenant plus subtil.

Sans contrôles,

on pouvait manquer une dérive.

Avec trop de contrôles,

on pouvait créer la dérive qu’on cherchait.

Brutus regarda Astra.

— Donc on doit surveiller le surveillant?

Elle rit.

— Jusqu’à une certaine profondeur, oui.

Mais pas à l’infini.

Sinon on retombait dans le problème du chapitre 42 :

une preuve qui exige une preuve qui exige une preuve…

jusqu’à écraser le système sous sa propre traçabilité.

Il fallait donc une frontière.

Une profondeur suffisante pour rendre la reconstruction crédible,

mais pas infinie.

Ils appelèrent cela :

\[
D_V
\]

la **profondeur de vérification**.

Alors :

\[
D_V=0
\]

signifiait aucune vérification interne.

\[
D_V=1
\]

une couche.

\[
D_V=2
\]

une vérification de la vérification.

Et ainsi de suite.

Mais ils écrivirent immédiatement :

\[
D_V\rightarrow\infty
\]

n’était pas un objectif.

La confiance n’était pas produite par une infinité de contrôles.

Elle venait d’une architecture bien choisie.

---

Ils testèrent plusieurs profondeurs.

À faible profondeur :

certaines erreurs passaient.

À forte profondeur :

la machine ralentissait

et de nouvelles perturbations apparaissaient.

Entre les deux,

une zone semblait meilleure.

Pas parfaite.

Meilleure.

Ils notèrent :

\[
D_V^\star
\]

la profondeur candidate minimisant un compromis :

\[
J(D_V)
=
E_{\text{non détectées}}
+
\lambda\,C_{\text{surveillance}}
\]

avec :

\[
\lambda
\]

comme poids du coût de surveillance.

Encore une fois,

pas une constante universelle.

Un paramètre de conception.

---

Puis le compteur passa :

\[
7\rightarrow8
\]

exactement pendant un test de profondeur.

Cette fois,

ils étaient prêts.

Ils enregistrèrent tout.

La variation n’avait pas été déclenchée par une sortie anormale.

Ni par \(\rho_\phi\).

Ni par la distance de chemin seule.

Elle était apparue lorsque deux contrôleurs internes avaient donné des verdicts contradictoires.

Le premier disait :

\[
C_1=\text{stable}
\]

Le second :

\[
C_2=\text{instable}
\]

pour le même chemin.

Le problème n’était plus le chemin.

Le problème était :

**le référentiel du jugement.**

---

Astra inspecta les deux contrôleurs.

Ils ne mesuraient pas exactement la même chose.

Le premier évaluait :

\[
\|y'-y\|
\]

Le second évaluait :

\[
d_w(G',G)
\]

Donc l’un disait :

> la sortie n’a presque pas changé.

L’autre disait :

> la structure interne a beaucoup changé.

Tous les deux avaient raison.

Selon leur observable.

Le Royaume venait de retrouver une vieille vérité sous une forme nouvelle :

\[
\boxed{
\text{STABILITÉ}
\text{ N'EXISTE PAS SANS OBSERVABLE}
}
\]

Un chemin pouvait être stable pour la sortie

et instable pour la structure.

Stable pour la fonction,

fragile pour l’identité.

---

Brutus resta longtemps devant cette phrase.

Puis il demanda :

— Alors qu’est-ce qu’on protège exactement?

Cette question arrêta la salle.

Jusqu’ici, ils avaient voulu protéger :

le résultat.

Mais ce n’était peut-être pas suffisant.

Fallait-il préserver :

\[
y
\]

la sortie?

Ou :

\[
G
\]

la structure?

Ou :

\[
\Pi
\]

la provenance?

Ou :

\[
I
\]

l’identité?

Ou les quatre?

Astra écrivit :

\[
\mathcal T
=
\{
y,G,\Pi,I
\}
\]

l’ensemble des cibles de préservation.

Puis :

\[
\text{ROBUSTESSE}
=
\text{robustesse relativement à } \mathcal T
\]

C’était beaucoup plus propre.

Et beaucoup plus difficile.

---

Ils construisirent alors quatre chemins.

Tous donnaient exactement la même sortie :

\[
y
\]

Le premier conservait bien la structure.

Le second conservait mieux la provenance.

Le troisième résistait davantage au bruit.

Le quatrième était plus rapide.

Aucun ne dominait tous les autres.

Pour la première fois, le Royaume se retrouva devant plusieurs solutions réellement différentes

sans pouvoir honnêtement déclarer :

**celle-ci est la meilleure.**

Alors Brutus refusa le classement unique.

À la place, ils construisirent un front.

Un ensemble de compromis.

\[
\mathcal P^\star
\]

les chemins pour lesquels aucune amélioration sur un critère n’était possible sans dégrader au moins un autre critère.

Ils ne lui donnèrent pas de couronne.

Ils lui donnèrent un nom plus humble :

**la frontière des choix.**

---

La Fermabrique changea alors son verdict.

Au lieu de :

\[
\texttt{PATH\_CLASS\_UNRESOLVED}
\]

elle afficha :

\[
\texttt{PATH\_CLASSES\_PARTIAL}
\]

Partiel.

Pas résolu.

Mais plus complètement inconnu.

C’était une victoire.

Une vraie.

Parce qu’une classification imparfaite mais vérifiable valait mieux qu’une théorie parfaite inventée trop tôt.

---

Puis une anomalie apparut.

Dans plusieurs chemins considérés robustes,

la fragilité n’augmentait pas progressivement.

Elle apparaissait soudainement.

Pendant longtemps :

\[
\kappa_P\approx \text{faible}
\]

Puis après une petite variation de paramètre :

\[
\kappa_P\rightarrow \text{très grande}
\]

Le système semblait franchir une frontière.

Ils appelèrent provisoirement le paramètre :

\[
\mu
\]

et le seuil :

\[
\mu_c
\]

Alors :

\[
\mu<\mu_c
\]

le chemin résistait.

Mais :

\[
\mu>\mu_c
\]

il devenait extrêmement sensible.

La différence entre les deux régimes pouvait être minuscule.

---

Brutus murmura :

— Une porte.

Astra ne répondit pas immédiatement.

Parce que le mot était beau.

Mais il fallait encore vérifier s’il était juste.

Mathématiquement,

il pouvait simplement s’agir d’un seuil,

d’une bifurcation,

d’une transition de régime,

ou d’un artefact numérique.

Ils inscrivirent donc :

\[
\mu_c=\text{SEUIL CANDIDAT}
\]

et :

\[
\text{MÉCANISME : INCONNU}
\]

---

Ils firent le test le plus simple.

Ils approchèrent lentement le seuil par-dessous :

\[
\mu_1<\mu_2<\cdots<\mu_c
\]

Puis le dépassèrent.

Ensuite ils revinrent en arrière.

Ils s’attendaient à retrouver exactement le même point de transition.

Mais ce ne fut pas le cas.

À la montée :

\[
\mu_c^{+}
\]

À la descente :

\[
\mu_c^{-}
\]

avec :

\[
\mu_c^{+}\neq\mu_c^{-}
\]

Le système ne semblait pas franchir la frontière au même endroit selon la direction.

Brutus fixa les deux valeurs.

— Donc il se souvient vraiment.

Astra regarda les données.

Cette fois, elle ne barra pas immédiatement le mot.

Elle écrivit plutôt :

\[
\text{HYSTÉRÉSIS CANDIDATE}
\]

Car un système dont la réponse dépend du chemin suivi par le paramètre pouvait présenter une hystérésis.

La mémoire apparente avait enfin un concept testable.

Pas mystique.

Pas conscient.

Pas magique.

Mesurable.

---

Le Royaume fit plusieurs cycles.

Montée.

Descente.

Montée.

Descente.

Une boucle apparut.

\[
\oint y\,d\mu \neq 0
\]

Une aire.

Un résidu du chemin parcouru.

Quelque chose qui disparaissait si l’on regardait seulement les points de départ et d’arrivée.

Encore une fois,

le chemin contenait de l’information que les extrémités ne montraient pas.

Le chapitre 44 n’avait donc pas posé la mauvaise question.

Il avait simplement ouvert la première couche.

---

Puis le compteur changea.

\[
8\rightarrow9
\]

Exactement au moment où la boucle d’hystérésis se referma.

Cette fois,

il n’y avait presque plus de doute sur un point :

le compteur réagissait à des événements liés au chemin.

Mais lesquels?

Pas tous.

Pas seulement les transitions.

Pas seulement les divergences.

Pas seulement les retours.

Le Royaume ne savait toujours pas.

Et cette ignorance était devenue suffisamment précise pour être utile.

Ils écrivirent :

\[
E=f(P,\text{classe},\text{transition},\ldots)
\]

mais :

\[
f=\text{INCONNUE}
\]

---

Avant de fermer la salle,

Brutus regarda la boucle dessinée sur l’écran.

Elle ressemblait presque à une respiration.

Aller.

Revenir.

Mais ne jamais repasser exactement par le même endroit.

Astra inscrivit la dernière phrase :

> **Un chemin solide n’est pas celui qui ne bouge jamais.**
>
> **C’est celui dont on sait ce qui change quand on le pousse.**

Puis, en dessous :

\[
\boxed{
\text{ROBUSTESSE}
=
\text{SURVIVRE À DES PERTURBATIONS IDENTIFIÉES}
}
\]

et non :

\[
\text{NE JAMAIS CHANGER}
\]

La Fermabrique éteignit ses contrôleurs.

Tous sauf un.

Le dernier surveillait encore le seuil :

\[
\mu_c.
\]

Pendant plusieurs minutes,

rien ne bougea.

Puis la valeur se sépara en deux.

Pas une erreur d’affichage.

Deux seuils distincts apparurent :

\[
\mu_{c,1}
\]

et :

\[
\mu_{c,2}.
\]

Entre les deux,

un territoire minuscule existait désormais.

Un territoire où le même système semblait pouvoir être stable

ou instable,

selon la manière dont il y était arrivé.

La machine écrivit :

\[
\texttt{DUAL\_STATE\_REGION}
\]

Puis le compteur resta à :

\[
9.
\]

Comme s’il attendait.

Et pour la première fois,

Brutus comprit que la prochaine question ne serait peut-être plus :

> Quel chemin est stable?

Mais :

> **Combien d’états peuvent vivre au même endroit?**
