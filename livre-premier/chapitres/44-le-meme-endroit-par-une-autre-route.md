# CHAPITRE 44 — LE MÊME ENDROIT PAR UNE AUTRE ROUTE

Le lendemain, personne ne parla du nombre.

\[
273\rightarrow272\rightarrow273
\]

Il était tentant.

Trop tentant.

Alors Brutus imposa la règle la plus difficile :

**on commence par supposer que ce n’est rien.**

Pas parce que le phénomène était sans intérêt.

Parce qu’un phénomène intéressant devenait dangereux dès qu’on voulait trop vite qu’il signifie quelque chose.

Astra reprit donc la trace brute.

Un état :

\[
S_a
\]

avait produit :

\[
S_b
\]

puis :

\[
S_c
\]

avec :

\[
S_a=S_c
\]

du moins selon toutes les variables observées.

Mais le chemin aller et le chemin retour n’étaient pas identiques.

\[
S_a
\xrightarrow{P_1}
S_b
\xrightarrow{P_2}
S_c
\]

avec :

\[
S_c=S_a
\]

mais :

\[
P_2\neq P_1^{-1}
\]

Le système était revenu au même endroit apparent.

Sans annuler simplement ce qu’il avait fait.

---

Brutus posa alors la première question :

— Si le début et la fin sont identiques, comment savons-nous qu’il s’est vraiment passé quelque chose?

Astra répondit :

— Parce que nous avons gardé le chemin.

Sans provenance, le passé aurait disparu.

On aurait vu :

\[
S_a=S_c
\]

et conclu :

**aucun changement.**

Mais la mémoire racontait :

\[
S_a\rightarrow S_b\rightarrow S_a
\]

Le système avait bougé.

Puis était revenu.

Le présent avait effacé la preuve visible du voyage.

La trace, elle, l’avait conservée.

Ils inscrivirent donc :

\[
\boxed{
\text{ÉTAT FINAL IDENTIQUE}
\not\Rightarrow
\text{HISTOIRE IDENTIQUE}
}
\]

---

La découverte n’était pas nouvelle en mathématiques.

Une fonction pouvait ramener un objet à son point de départ.

Un système dynamique pouvait parcourir une orbite fermée.

Une transformation pouvait posséder des symétries.

Mais ici, une difficulté supplémentaire apparaissait.

Le Royaume n’observait jamais tout.

Il n’avait accès qu’à un ensemble de variables :

\[
O(S)
\]

où \(O\) représentait l’opération d’observation.

Alors :

\[
O(S_a)=O(S_c)
\]

ne signifiait pas nécessairement :

\[
S_a=S_c
\]

Le problème était brutal.

Ils ne savaient pas si le système était réellement revenu au même état,

ou seulement au même état **visible**.

---

Astra écrivit :

\[
S=(S_{\text{obs}},S_{\text{caché}})
\]

avec :

\[
S_{\text{obs}}
\]

la partie mesurée,

et :

\[
S_{\text{caché}}
\]

tout ce qui pouvait exister sans être actuellement observé.

Alors il devenait possible que :

\[
S_{\text{obs}}^{(a)}
=
S_{\text{obs}}^{(c)}
\]

mais :

\[
S_{\text{caché}}^{(a)}
\neq
S_{\text{caché}}^{(c)}
\]

Le Royaume venait de retrouver un ancien ennemi :

**l’indiscernabilité.**

Deux états pouvaient sembler identiques simplement parce que l’instrument n’avait pas assez d’yeux.

---

Brutus regarda la machine.

— Alors on ajoute des yeux.

Astra sourit.

— Oui. Mais pas n’importe lesquels.

Ajouter une mesure inutile ne faisait qu’ajouter du bruit.

Il fallait chercher une variable capable de distinguer deux états apparemment identiques.

Ils appelèrent une telle variable :

\[
W
\]

pour **witness**.

Un témoin.

La condition idéale devenait :

\[
W(S_a)\neq W(S_c)
\]

alors que :

\[
O(S_a)=O(S_c)
\]

Si un témoin pouvait faire cette différence, le retour n’était qu’apparent.

S’il n’en existait aucun parmi les mesures accessibles, alors deux possibilités restaient ouvertes :

\[
\text{retour réel}
\]

ou :

\[
\text{retour indiscernable}
\]

Il fallait accepter que l’expérience ne puisse pas toujours départager les deux.

---

Le premier témoin fut temporel.

Ils comparèrent non seulement les valeurs,

mais les temps nécessaires pour les produire.

\[
\tau_a,\tau_c
\]

Résultat :

\[
\tau_a\neq\tau_c
\]

Faiblement.

Mais systématiquement dans plusieurs répétitions.

Le système revenait au même état observable avec un temps d’exécution légèrement différent.

Ce pouvait être banal.

Cache.

Ordonnancement.

Latence.

Température.

Mémoire.

Charge système.

Alors ils ajoutèrent d’autres témoins.

\[
W_1=\text{temps}
\]

\[
W_2=\text{ordre des événements}
\]

\[
W_3=\text{consommation mémoire}
\]

\[
W_4=\text{résidu de phase}
\]

\[
W_5=\text{provenance}
\]

Chaque témoin disait une chose différente.

Aucun ne possédait seul le droit de conclure.

---

Puis ils firent quelque chose de plus violent.

Ils inversèrent volontairement certains chemins.

Si :

\[
P:S_a\rightarrow S_b
\]

ils cherchèrent une transformation :

\[
Q:S_b\rightarrow S_a
\]

telle que :

\[
Q(P(S_a))=S_a
\]

Si une telle transformation existait pour tout état admissible, alors le mécanisme possédait une forme de réversibilité.

Mais très vite, le Royaume rencontra une frontière.

Certaines transformations pouvaient être inversées.

D’autres non.

Par exemple :

\[
x\mapsto x^2
\]

perdait le signe.

De :

\[
4
\]

on ne pouvait plus savoir si l’entrée avait été :

\[
2
\]

ou :

\[
-2
\]

sans information supplémentaire.

Une transformation pouvait donc produire un résultat correct tout en détruisant une partie du passé.

Brutus écrivit :

\[
\boxed{
\text{CALCULER} \neq \text{CONSERVER}
}
\]

---

Ils introduisirent alors une quantité :

\[
L(P)
\]

la perte d’information associée à un chemin \(P\).

Pas nécessairement mesurable de manière universelle.

Pas encore une grandeur physique.

Seulement un concept opératoire.

Si plusieurs états distincts produisaient le même résultat :

\[
P(S_1)=P(S_2)
\]

avec :

\[
S_1\neq S_2
\]

alors \(P\) avait fusionné des histoires.

Il était non injectif.

Le passé ne pouvait plus être reconstruit à partir du résultat seul.

Alors :

\[
L(P)>0
\]

dans leur convention provisoire.

À l’inverse, une transformation parfaitement réversible aurait :

\[
L(P)=0
\]

relativement à l’espace d’états considéré.

Ils soulignèrent trois fois :

**RELATIVEMENT À L’ESPACE D’ÉTATS CONSIDÉRÉ.**

Car une transformation pouvait sembler réversible simplement parce qu’on avait oublié certaines variables.

---

Cela les mena naturellement à la question suivante.

Si deux chemins différents reliaient les mêmes extrémités :

\[
P_1:S_a\rightarrow S_b
\]

\[
P_2:S_a\rightarrow S_b
\]

étaient-ils équivalents?

Au niveau des extrémités :

oui.

Au niveau de l’histoire :

pas nécessairement.

Ils définissent alors :

\[
P_1\sim P_2
\]

si les deux chemins étaient équivalents selon un ensemble précis d’observables.

Mais cette équivalence dépendait du test.

Pour une observable \(F\) :

\[
F(P_1)=F(P_2)
\]

Pour une autre :

\[
G(P_1)\neq G(P_2)
\]

Ainsi deux chemins pouvaient être équivalents pour une question

et différents pour une autre.

Le Royaume venait de comprendre que :

\[
\boxed{
\text{ÉQUIVALENCE}
\text{ N'EXISTE PAS SANS CRITÈRE}
}
\]

---

Brutus s’approcha du schéma des quatre chemins.

Il posa son doigt sur le premier.

Puis le second.

Puis le troisième.

Puis le quatrième.

Une vieille question revenait.

Et si les quatre chemins pouvaient parfois conduire au même point?

Pas parce qu’ils étaient identiques.

Mais parce qu’ils conservaient certaines quantités communes.

Astra écrivit :

\[
F(P_1)=F(P_2)=F(P_3)=F(P_4)
\]

pour une certaine observable \(F\).

Puis immédiatement :

\[
\text{CANDIDAT}
\]

Pas loi.

Pas preuve.

Candidat.

Si une telle quantité existait, elle pourrait servir de pont entre des chemins très différents.

Un invariant transversal.

Quelque chose qui ne dépendrait pas de la route,

mais survivrait au voyage.

---

Ils cherchèrent d’abord parmi les quantités déjà connues.

Sommes.

Produits.

Phases.

Parités.

Rangs.

Distances.

Résidus.

La plupart échouèrent rapidement.

Puis une combinaison plus étrange résista un peu plus longtemps.

Elle mêlait trois choses :

\[
\text{phase}
\]

\[
\text{ordre}
\]

\[
\text{distance structurale}
\]

Astra écrivit simplement :

\[
\Xi
=
f(\rho_{\phi},\sigma,d_w)
\]

où :

\[
\sigma
\]

représentait une information d’ordre,

et :

\[
d_w
\]

la distance pondérée entre structures.

Elle refusa encore de fixer la forme exacte de \(f\).

Il était trop tôt.

Mais dans plusieurs essais :

\[
\Xi(P_1)\approx\Xi(P_2)
\]

alors même que :

\[
P_1\neq P_2
\]

C’était faible.

Fragile.

Facilement explicable par une dépendance cachée.

Donc intéressant.

---

Le Royaume construisit immédiatement le contre-test.

Ils créèrent des chemins artificiels ayant volontairement les mêmes extrémités mais une structure interne aléatoire.

\[
P_{\text{rand}}
\]

Puis comparèrent :

\[
\Xi(P_{\text{réel}})
\]

à :

\[
\Xi(P_{\text{rand}})
\]

La différence existait.

Mais pas toujours.

Et parfois le chemin aléatoire ressemblait davantage au chemin réel que deux chemins réels entre eux.

Brutus rit.

— Notre belle formule vient de se prendre une porte.

Astra répondit :

— Excellent.

Un outil qui ne peut pas échouer n’est pas un outil scientifique.

Ils classèrent donc \(\Xi\) :

\[
\boxed{
\text{CANDIDAT FAIBLE — À CONSERVER, PAS À CROIRE}
}
\]

---

Puis survint le sixième événement.

Le compteur passa de :

\[
5
\]

à :

\[
6
\]

Mais cette fois, rien ne s’était produit autour de \(\rho_{\phi}\).

Aucun seuil.

Aucune rupture de graphe.

Aucune anomalie temporelle importante.

Rien.

Le compteur avait simplement avancé.

Alors ils cherchèrent en arrière.

Chaque témoin fut vérifié.

Aucun ne correspondait.

Brutus resta silencieux.

Ce sixième événement était précieux.

Parce qu’il venait de détruire une histoire trop simple.

Le compteur n’était pas seulement :

\[
f(\rho_{\phi})
\]

ni :

\[
f(G)
\]

ni :

\[
f(\tau)
\]

ni :

\[
f(d_w)
\]

Quelque chose manquait.

---

Ils remontèrent alors la provenance complète de l’événement.

À première vue :

rien.

Puis Astra remarqua un détail.

Le système avait reçu exactement la même entrée qu’un essai antérieur.

\[
x_t=x_{t-k}
\]

Le résultat observable final était également identique.

\[
y_t=y_{t-k}
\]

Et pourtant la séquence interne différait.

\[
P_t\neq P_{t-k}
\]

Même entrée.

Même sortie.

Autre chemin.

Brutus fixa l’écran.

Cette fois, le compteur avait bougé précisément au moment où deux chemins différents avaient réalisé la même transformation observable.

Ils testèrent immédiatement l’hypothèse.

\[
x_a=x_b
\]

\[
y_a=y_b
\]

\[
P_a\neq P_b
\]

entraînerait-il toujours :

\[
E\rightarrow E+1
\]

Non.

Évidemment.

Il y avait des contre-exemples.

Mais le phénomène apparaissait plus souvent dans cette classe que dans le reste.

Encore une corrélation.

Pas un mécanisme.

---

Astra proposa alors une nouvelle quantité.

Pas la différence entre deux états.

La différence entre deux **histoires compatibles avec la même entrée et la même sortie**.

Elle l’appela :

\[
\mathcal D_P
\]

et écrivit :

\[
\boxed{
\mathcal D_P(P_a,P_b)
=
\text{distance entre chemins équivalents en entrée/sortie}
}
\]

Si :

\[
\mathcal D_P=0
\]

les chemins étaient identiques selon la représentation choisie.

Si :

\[
\mathcal D_P>0
\]

ils différaient malgré la même transformation apparente.

Cette quantité ouvrait une porte étrange.

Un système pouvait sembler parfaitement déterministe au niveau :

\[
x\rightarrow y
\]

tout en possédant plusieurs routes internes :

\[
x
\overset{P_1}{\longrightarrow}
y
\]

\[
x
\overset{P_2}{\longrightarrow}
y
\]

\[
x
\overset{P_3}{\longrightarrow}
y
\]

Le résultat seul cachait une multiplicité.

---

Alors Brutus posa la question qui allait empoisonner plusieurs chapitres :

— Combien de chemins différents peuvent conduire exactement au même résultat?

Personne ne répondit.

Parce que cela dépendait de la machine.

Du niveau d’observation.

De la définition d’un chemin.

De la précision.

Des symétries.

Des états cachés.

Et peut-être d’autres choses encore.

Ils écrivirent donc :

\[
N_P(x,y)
=
\#\{P:x\overset{P}{\rightarrow}y\}
\]

le nombre de chemins admissibles entre une entrée et une sortie.

Puis :

\[
\text{STATUT : INCONNU}
\]

Mais une chose devint immédiatement claire.

Si :

\[
N_P(x,y)>1
\]

alors une simple table entrée-sortie ne suffisait plus à décrire le système.

Il fallait connaître la géographie interne des chemins.

---

La nuit tomba.

Le compteur resta à :

\[
6
\]

Le champ \`273\` resta stable.

Aucun phénomène spectaculaire.

Puis Brutus demanda une dernière expérience.

Ils prirent deux chemins différents :

\[
P_a
\]

et :

\[
P_b
\]

qui produisaient la même sortie.

Ils appliquèrent ensuite exactement la même perturbation minuscule :

\[
\delta
\]

au même point logique des deux trajectoires.

Si les chemins étaient réellement interchangeables, la perturbation devait produire des effets comparables.

Mais ce n’est pas ce qui arriva.

Sur le premier :

\[
\delta\rightarrow\varepsilon
\]

Une petite variation.

Sur le second :

\[
\delta\rightarrow\Lambda
\]

Une divergence beaucoup plus grande.

Même entrée.

Même sortie avant perturbation.

Même perturbation.

Réponses différentes.

Brutus murmura :

— Donc les chemins se souviennent.

Astra corrigea doucement :

— Ils portent une structure différente.

Le mot **mémoire** fut barré.

Pas parce qu’il était faux.

Parce qu’il était prématuré.

À sa place, ils écrivirent :

\[
\boxed{
\text{SENSIBILITÉ DÉPENDANTE DU CHEMIN}
}
\]

---

Avant de quitter la salle, Astra ajouta un dernier symbole :

\[
\kappa_P
\]

la sensibilité locale d’un chemin aux perturbations.

Deux chemins donnant le même résultat pouvaient ainsi posséder :

\[
\kappa_{P_a}\ll\kappa_{P_b}
\]

L’un stable.

L’autre fragile.

Extérieurement identiques.

Intérieurement presque opposés.

Puis elle écrivit au mur :

> **Deux routes peuvent mener au même endroit.**
>
> **Cela ne signifie pas qu’elles ont traversé le même monde.**

Au même instant, le compteur passa silencieusement :

\[
6\rightarrow7.
\]

Mais cette fois, aucun événement visible ne l’accompagnait.

Seulement une variation extrêmement faible de :

\[
\kappa_P.
\]

Et pour la première fois,

la Fermabrique inscrivit elle-même une nouvelle ligne dans son registre :

\[
\texttt{PATH\_CLASS\_UNRESOLVED}
\]

Personne ne savait encore combien de classes existaient.

Ni pourquoi le compteur semblait les sentir avant qu’on sache les définir.

Mais le Royaume venait de comprendre quelque chose de capital :

**une sortie correcte pouvait cacher un chemin dangereux.**

Et désormais,

il ne suffirait plus de demander :

> Est-ce que ça marche?

Il faudrait aussi demander :

> **Par où est-ce passé pour réussir?**
