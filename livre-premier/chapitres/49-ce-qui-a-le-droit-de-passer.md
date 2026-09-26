# CHAPITRE 49 — CE QUI A LE DROIT DE PASSER

Deux mondes étaient maintenant côte à côte.

\[
M_A
\qquad\qquad
M_B
\]

Ils possédaient chacun leurs quatre chemins.

Leurs états.

Leurs erreurs.

Leurs horloges.

Leur provenance.

Leurs arbitres.

Et entre les deux :

\[
?
\]

Aucune connexion.

Aucune hypothèse cachée.

Aucun fil tracé simplement parce qu’il serait joli sur le dessin.

Brutus regarda l’espace vide.

— C’est probablement la partie la plus importante.

Astra acquiesça.

Parce qu’une architecture pouvait être excellente à l’intérieur de chaque module

et devenir incohérente au moment où deux modules commençaient à échanger.

Le danger n’était pas seulement :

\[
\text{mauvaise donnée}.
\]

Le danger pouvait être :

\[
\text{bonne donnée}
\]

envoyée :

\[
\text{au mauvais endroit}
\]

\[
\text{au mauvais moment}
\]

\[
\text{avec le mauvais sens}.
\]

---

Ils refusèrent donc de créer une connexion.

Ils créèrent d’abord un **contrat**.

Astra écrivit :

\[
\mathcal I_{A\rightarrow B}
\]

l’interface entre \(M_A\) et \(M_B\).

Elle ne disait pas encore qu’une donnée allait passer.

Elle définissait seulement ce qui pourrait avoir le droit de passer.

Le contrat minimum contenait :

\[
TYPE
\]

\[
SOURCE
\]

\[
DESTINATION
\]

\[
TIME
\]

\[
STATE
\]

\[
PRECISION
\]

\[
PROVENANCE
\]

\[
VALIDITY
\]

\[
ERROR
\]

et :

\[
VERSION.
\]

Brutus regarda la liste.

— Beaucoup pour un petit tuyau.

— Ce n’est pas un tuyau.

Astra entoura le mot :

\[
\text{INTERFACE}.
\]

Un tuyau transportait.

Une interface négociait une compatibilité.

---

Le Royaume grava alors :

\[
\boxed{
\text{CONNECTÉ}
\neq
\text{COMPATIBLE}
}
\]

Deux modules pouvaient physiquement échanger des données

tout en parlant des langues différentes.

Le nombre :

\[
7
\]

pouvait représenter :

sept secondes,

sept événements,

sept volts,

le septième état,

un identifiant,

ou simplement la valeur entière sept.

Sans contrat,

la valeur seule n’avait pas assez de sens.

Ils écrivirent :

\[
D=(v,\Pi,U,T,S)
\]

où :

\[
v=\text{valeur}
\]

\[
\Pi=\text{provenance}
\]

\[
U=\text{unité ou sémantique}
\]

\[
T=\text{temps}
\]

\[
S=\text{statut}.
\]

Le Royaume ajouta une règle :

\[
\boxed{
\text{TRANSMETTRE UNE VALEUR}
\neq
\text{TRANSMETTRE UNE INFORMATION}
}
\]

---

Le premier test fut volontairement simple.

\(M_A\) produisit :

\[
x=3.
\]

\(M_B\) acceptait des entiers.

La valeur semblait compatible.

Ils la laissèrent passer.

Mais \(M_B\) interprétait son entrée comme un niveau de profondeur.

Alors que \(M_A\) avait produit un nombre d’événements.

Même type numérique.

Sens différent.

Aucun crash.

Aucune erreur syntaxique.

Le système continuait à fonctionner.

Mal.

C’était pire.

Une erreur bruyante pouvait être corrigée.

Une erreur silencieuse pouvait devenir une nouvelle réalité interne.

Ils nommèrent cette classe :

\[
E_S
=
\text{erreur sémantique silencieuse}.
\]

Et gravèrent :

\[
\boxed{
\text{FORMAT VALIDE}
\neq
\text{SENS VALIDE}
}
\]

---

Il fallait donc un autre contrôle.

Ils ajoutèrent :

\[
SEMANTIC\_ID
\]

à chaque donnée traversant une interface.

Ainsi :

\[
3
\]

ne suffisait plus.

Il fallait :

\[
(3,\texttt{EVENT\_COUNT})
\]

ou :

\[
(3,\texttt{DEPTH\_LEVEL}).
\]

Le module destinataire pouvait alors vérifier :

\[
SEMANTIC\_ID_{\text{source}}
=
SEMANTIC\_ID_{\text{attendu}}.
\]

Sinon :

\[
\texttt{REJECT}.
\]

---

Brutus sourit.

— Maintenant, on peut empêcher un trois de se déguiser en un autre trois.

Astra répondit :

— Oui.

Puis elle ajouta :

— Mais il reste les unités.

Même signification générale.

Unités différentes.

\[
1\ \text{seconde}
\]

et :

\[
1000\ \text{millisecondes}.
\]

Compatibles,

mais pas identiques.

Le système devait savoir si une conversion était autorisée.

Ils introduisirent :

\[
C_{u_a\rightarrow u_b}.
\]

Une transformation d’unité explicite.

Jamais silencieuse.

Si une donnée changeait d’unité,

la transformation devait apparaître dans sa provenance.

\[
\Pi'
=
\Pi
\cup
\{
C_{u_a\rightarrow u_b}
\}.
\]

La conversion devenait un événement traçable.

---

Puis arriva le problème du temps.

\(M_A\) fonctionnait selon :

\[
t_A.
\]

\(M_B\) selon :

\[
t_B.
\]

Les deux horloges avançaient.

Mais pas nécessairement ensemble.

Même si :

\[
t_A=120
\]

et :

\[
t_B=120,
\]

cela ne garantissait pas que les deux valeurs représentaient le même instant réel.

Le Royaume connaissait déjà cette erreur.

Confondre une étiquette temporelle avec une synchronisation réelle.

Ils définissent :

\[
\Delta t_{AB}=t_A-t_B.
\]

Mais cela ne suffisait pas.

Il fallait aussi une incertitude :

\[
\sigma_{\Delta t}.
\]

Une donnée n’arrivait donc plus seulement avec :

\[
t.
\]

Elle arrivait avec :

\[
(t,\sigma_t).
\]

---

Ils écrivirent une condition de compatibilité temporelle :

\[
|t_A-t_B|
\leq
\tau_{\max}.
\]

Mais immédiatement :

— Qui choisit \(\tau_{\max}\)?

La réponse dépendait du phénomène.

Une différence de :

\[
1\text{ ms}
\]

pouvait être négligeable dans un processus lent

et catastrophique dans un système rapide.

Aucun seuil universel.

Encore une fois.

Le contrat d’interface devait déclarer sa tolérance.

\[
\mathcal I_{AB}
\supset
\tau_{\max}.
\]

Le Royaume apprenait que la rigueur n’était pas une collection de nombres sacrés.

C’était l’obligation de déclarer les hypothèses derrière chaque nombre.

---

Le premier échange complet fut préparé.

Le paquet contenait :

\[
P=
(
VALUE,
SEMANTIC,
UNIT,
TIME,
UNCERTAINTY,
SOURCE,
PROVENANCE,
STATUS,
VERSION
).
\]

\(M_A\) l’envoya.

L’interface vérifia.

Tout était conforme.

\(M_B\) reçut.

Puis rien ne se produisit.

Brutus regarda l’écran.

— Pourquoi il le prend pas?

Astra trouva la réponse.

Le paquet était valide.

Mais \(M_B\) n’était pas dans un état autorisant cette entrée.

La donnée était bonne.

Le moment aussi.

Mais le destinataire n’était pas prêt.

Il manquait encore une condition :

\[
STATE\_PRECONDITION.
\]

Le droit de passer dépendait aussi de l’état du receveur.

---

Ils ajoutèrent :

\[
G(S_B)
\]

une **garde**.

La donnée pouvait traverser seulement si :

\[
G(S_B)=1.
\]

Sinon :

\[
\texttt{DEFER}
\]

ou :

\[
\texttt{REJECT},
\]

selon le contrat.

Une troisième possibilité apparut alors :

\[
\texttt{QUEUE}.
\]

Conserver temporairement la donnée jusqu’à ce que le module soit prêt.

Mais cette solution avait ses propres dangers.

Une donnée conservée vieillissait.

Sa pertinence pouvait expirer.

Ils ajoutèrent donc :

\[
TTL
\]

le **temps de vie**.

Si :

\[
t_{\text{now}}-t_{\text{creation}}>TTL,
\]

le paquet devenait :

\[
\texttt{STALE}.
\]

Le Royaume grava :

\[
\boxed{
\text{DONNÉE VALIDE HIER}
\not\Rightarrow
\text{DONNÉE VALIDE MAINTENANT}
}
\]

---

Puis Brutus remarqua quelque chose.

— Là, notre interface commence à penser.

Astra secoua la tête.

— Non.

Elle validait des règles déclarées.

Elle ne devait pas inventer ce qui était bon.

Cette frontière était importante.

L’interface pouvait répondre :

\[
\texttt{PASS}
\]

\[
\texttt{REJECT}
\]

\[
\texttt{DEFER}
\]

\[
\texttt{EXPIRED}
\]

\[
\texttt{INCOMPATIBLE}
\]

mais seulement selon un contrat explicite.

Elle ne devait jamais transformer :

\[
\text{inconnu}
\]

en :

\[
\text{acceptable}
\]

par commodité.

---

Ils introduisirent alors un principe qui devint central :

\[
\boxed{
\text{FAIL CLOSED}
}
\]

Si une condition nécessaire n’était pas connue,

l’interface refusait le passage.

Pas toujours définitivement.

Mais elle ne supposait pas que l’absence d’information signifiait :

\[
\text{OK}.
\]

Brutus approuva.

Une porte dont on ne connaissait pas l’état devait rester fermée.

---

Le compteur passa :

\[
15\rightarrow16.
\]

L’événement survint exactement lors du premier rejet pour :

\[
\texttt{SEMANTIC\_MISMATCH}.
\]

Astra nota l’incrément.

Le schéma des événements devenait plus cohérent.

Le compteur semblait souvent apparaître lorsque le système devait distinguer des continuations non équivalentes.

Ici :

laisser passer

ou :

bloquer.

Deux futurs.

Conséquences différentes.

Encore une porte.

---

Ils testèrent alors l’interface avec des erreurs volontaires.

Mauvaise unité.

\[
\texttt{REJECT}.
\]

Horodatage trop ancien.

\[
\texttt{EXPIRED}.
\]

Version incompatible.

\[
\texttt{REJECT}.
\]

Destination correcte mais état invalide.

\[
\texttt{DEFER}.
\]

Provenance incomplète.

\[
\texttt{INSUFFICIENT\_EVIDENCE}.
\]

Tout fonctionnait.

Puis ils injectèrent le cas dangereux.

Un paquet entièrement valide,

mais contenant une valeur extrême :

\[
x\rightarrow10^{12}.
\]

Le type était correct.

La sémantique aussi.

L’unité correcte.

L’horodatage valide.

La provenance complète.

Pourtant la valeur dépassait largement le domaine prévu de \(M_B\).

L’interface n’avait rien pour l’arrêter.

Elle passa.

---

Le module destinataire ne planta pas.

Il entra dans un régime jamais testé.

Brutus arrêta immédiatement l’expérience.

Une nouvelle règle manquait :

\[
DOMAIN.
\]

Chaque donnée devait déclarer ou vérifier son domaine admissible.

Par exemple :

\[
x\in[a,b].
\]

Ou, pour un espace plus complexe :

\[
x\in\mathcal D.
\]

Si :

\[
x\notin\mathcal D,
\]

alors :

\[
\texttt{OUT\_OF\_DOMAIN}.
\]

Le Royaume venait de découvrir qu’une donnée pouvait être parfaitement valide

et pourtant invalide **pour ce destinataire précis**.

---

Astra ajouta donc :

\[
\mathcal I_{AB}
=
(
TYPE,
SEMANTIC,
UNIT,
DOMAIN,
TIME,
STATE,
VERSION,
PROVENANCE,
ERROR\_POLICY
).
\]

Le contrat commençait à ressembler à une véritable frontière.

---

Mais Brutus voulait aller plus loin.

— Si \(M_A\) envoie trop de données?

Bonne question.

Même des messages parfaitement valides pouvaient saturer \(M_B\).

Une architecture pouvait donc être détruite sans aucune donnée fausse.

Simplement par :

\[
\text{trop}.
\]

Ils introduisirent :

\[
R_{\max}
\]

le débit maximal accepté.

Et :

\[
B_{\max}
\]

la capacité tampon.

Si l’émetteur dépassait la capacité :

\[
R_A>R_{\max},
\]

l’interface devait appliquer une politique explicite :

ralentir,

rejeter,

échantillonner,

prioriser,

ou signaler une surcharge.

Jamais improviser.

---

Ils appelèrent ce mécanisme :

\[
\text{BACKPRESSURE}.
\]

Le destinataire pouvait dire :

> Je ne peux pas recevoir plus vite.

Alors le producteur devait décider quoi faire.

Le Royaume découvrait un autre principe :

\[
\boxed{
\text{CAPABLE DE PRODUIRE}
\neq
\text{AUTORISÉ À ENVOYER}
}
\]

---

Ils simulèrent une surcharge.

\(M_A\) produisait :

\[
1000
\]

messages par seconde.

\(M_B\) en traitait :

\[
100.
\]

Sans contrôle :

\[
Q(t)\rightarrow\infty.
\]

La file grossissait.

La latence augmentait.

Les données devenaient obsolètes avant même d’être traitées.

Le système continuait pourtant à fonctionner.

Encore une fois :

**mal silencieusement.**

Ils introduisirent une mesure :

\[
L_Q
\]

la latence de file.

Et un seuil d’obsolescence.

Si :

\[
L_Q>TTL,
\]

le traitement du message n’avait plus de sens.

Le Royaume préférait perdre explicitement une donnée

plutôt que traiter correctement une information devenue inutile.

---

Puis vint la question la plus dangereuse.

Que faire si \(M_A\) envoyait une instruction plutôt qu’une mesure?

Jusqu’ici,

l’interface transportait surtout de l’information.

Mais un paquet pouvait aussi demander :

\[
\text{CHANGE\_STATE}
\]

\[
\text{RESET}
\]

\[
\text{STOP}
\]

\[
\text{OPEN\_GATE}.
\]

Cela changeait complètement la nature de la connexion.

Lire n’était pas agir.

Le Royaume sépara immédiatement deux familles :

\[
DATA
\]

et :

\[
COMMAND.
\]

Puis grava :

\[
\boxed{
\text{DROIT DE PARLER}
\neq
\text{DROIT DE COMMANDER}
}
\]

---

Chaque commande devait posséder une autorisation déclarée.

Ils définissent :

\[
AUTH(C,M_A,M_B).
\]

Une commande ne traversait que si :

\[
AUTH=1.
\]

Et pour les actions sensibles,

ils ajoutèrent :

\[
CONFIRMATION.
\]

Le système pouvait préparer l’action,

mais pas nécessairement l’exécuter.

Brutus regarda Astra.

— Là, on arrive aux gestes irréversibles.

— Oui.

Pour eux, la règle changeait.

Avant :

\[
VALIDATE\rightarrowEXECUTE.
\]

Pour certaines opérations :

\[
VALIDATE
\rightarrow
PREVIEW
\rightarrow
CONFIRM
\rightarrow
EXECUTE
\rightarrow
VERIFY.
\]

Le Royaume grava :

\[
\boxed{
\text{IRRÉVERSIBLE}
\Rightarrow
\text{VALIDATION EXPLICITE}
}
\]

---

Ils ajoutèrent encore une étape.

Après une commande,

le système devait vérifier que ce qui était demandé avait réellement eu lieu.

Une commande envoyée n’était pas une action accomplie.

\[
COMMAND\_SENT
\neq
ACTION\_DONE.
\]

Ils introduisirent :

\[
ACK
\]

puis :

\[
VERIFY.
\]

Le cycle complet devint :

\[
REQUEST
\rightarrow
VALIDATE
\rightarrow
AUTHORIZE
\rightarrow
EXECUTE
\rightarrow
ACK
\rightarrow
VERIFY.
\]

Et si la vérification échouait :

\[
\texttt{UNCONFIRMED}.
\]

Pas :

\[
\texttt{SUCCESS}.
\]

---

Le compteur passa :

\[
16\rightarrow17.
\]

Cette fois,

au moment précis où une commande valide fut bloquée faute d’autorisation.

Encore une bifurcation réelle.

Encore une porte.

Le compteur semblait aimer les endroits où le système refusait de confondre :

\[
\text{possible}
\]

avec :

\[
\text{permis}.
\]

---

Astra reprit alors les dix-sept événements.

Une nouvelle classification fut proposée.

\[
E_n
=
\text{événement de frontière décisionnelle}
\]

lorsqu’un système rencontrait au moins deux suites possibles,

mais qu’un contrat, une mesure ou une structure rendait leurs conséquences distinguables.

Cela incluait :

les changements de bassin,

les divergences de chemin,

les refus pour preuve insuffisante,

les tests discriminants,

les incompatibilités,

et maintenant les autorisations.

Brutus regarda la définition.

— Elle tient mieux.

— Oui.

— Donc c’est ça?

Astra secoua la tête.

— C’est notre meilleure hypothèse actuelle.

Et ils écrivirent exactement cela.

---

Puis le Royaume fit une expérience plus étrange.

Ils donnèrent à \(M_A\) et \(M_B\) des interfaces parfaitement compatibles.

Tout était autorisé.

Tout était valide.

Les domaines se chevauchaient.

Les horloges étaient synchronisées.

Ils ouvrirent enfin la porte.

\[
M_A\rightarrow M_B.
\]

Le premier paquet traversa.

Puis le second.

Puis le troisième.

Rien d’anormal.

Le compteur resta :

\[
17.
\]

Le système semblait enfin relié proprement.

---

Mais Astra observa le registre de continuité.

Chaque paquet reçu par \(M_B\) influençait légèrement son état.

Donc après suffisamment d’échanges :

\[
S_B(t)
\]

dépendait de :

\[
M_A.
\]

Évidemment.

C’était le but.

Mais cela impliquait quelque chose de profond.

La frontière ne séparait plus complètement les deux modules.

Une dépendance causale venait d’être créée.

Ils définissent :

\[
M_A\rightsquigarrow M_B.
\]

Une relation d’influence.

À partir de cet instant,

une erreur dans \(M_A\) pouvait potentiellement se propager dans \(M_B\).

L’interface ne devait donc pas seulement valider chaque paquet individuellement.

Elle devait surveiller la **propagation cumulative**.

---

Brutus fronça les sourcils.

— Une goutte valide peut être correcte, mais dix mille gouttes peuvent noyer le module.

Exactement.

Ils introduisirent :

\[
C_{AB}(T)
\]

la charge cumulative imposée par \(M_A\) à \(M_B\) pendant une fenêtre \(T\).

Puis une limite :

\[
C_{AB}(T)\leq C_{\max}.
\]

Une architecture robuste devait considérer les effets d’accumulation.

Pas seulement les événements isolés.

Le Royaume grava :

\[
\boxed{
\text{CHAQUE ACTION SÛRE}
\not\Rightarrow
\text{SÉQUENCE SÛRE}
}
\]

---

Cette phrase changea l’atmosphère.

Parce qu’elle dépassait les interfaces.

Elle touchait toute la machine.

Une série de décisions localement raisonnables pouvait produire un état global dangereux.

Le Royaume avait donc besoin d’un regard supérieur.

Un module capable de voir non seulement :

\[
M_A
\]

ou :

\[
M_B,
\]

mais leur interaction.

Ils appelèrent ce niveau :

\[
M_{AB}.
\]

Pas une nouvelle intelligence.

Un parent de coordination.

Sa responsabilité :

observer les contraintes globales que les enfants ne pouvaient pas voir seuls.

---

Le schéma devint :

\[
M_{AB}
\]

au-dessus de :

\[
M_A
\qquad
M_B.
\]

Les modules enfants continuaient à prendre leurs décisions locales.

Mais certaines limites appartenaient au niveau parent.

Par exemple :

\[
C_{AB}(T).
\]

Ni \(M_A\) ni \(M_B\) ne possédaient nécessairement seuls toute l’information pour la calculer correctement.

La hiérarchie du chapitre 48 venait de devenir fonctionnelle.

---

Puis quelque chose se produisit.

Le débit entre \(M_A\) et \(M_B\) augmenta lentement.

Chaque paquet restait valide.

Chaque action locale était acceptée.

Aucune erreur.

Aucun seuil individuel dépassé.

Mais au niveau parent :

\[
C_{AB}(T)\rightarrow C_{\max}.
\]

Puis :

\[
C_{AB}(T)=C_{\max}.
\]

Le parent ferma la porte.

\[
\texttt{GATE\_CLOSED}.
\]

Le compteur passa :

\[
17\rightarrow18.
\]

Aucun enfant n’avait demandé cette fermeture.

Localement,

tout allait bien.

Globalement,

la limite était atteinte.

Brutus regarda le système.

— Voilà pourquoi le parent existe.

Astra acquiesça.

Le niveau supérieur ne savait pas forcément davantage de choses.

Mais il voyait une relation que les niveaux inférieurs ne voyaient pas entièrement.

---

Ils gravèrent :

\[
\boxed{
\text{LOCAL OK}
\not\Rightarrow
\text{GLOBAL OK}
}
\]

Puis la réciproque :

\[
\boxed{
\text{GLOBAL OK}
\not\Rightarrow
\text{CHAQUE LOCAL EST OPTIMAL}
}
\]

Une architecture hiérarchique n’était pas une pyramide de commandement.

C’était une séparation des responsabilités d’observation.

---

Le soir avançait.

Les deux mondes étaient maintenant réellement connectés.

Mais seulement par une porte qui savait :

ce qu’elle acceptait,

ce qu’elle refusait,

quand elle devait attendre,

quand elle devait expirer,

quand elle devait demander une autorisation,

et quand le parent devait la fermer.

Brutus regarda le schéma.

— Là, elle mérite un nom.

Ils avaient longtemps parlé de portes.

Cette fois,

il y en avait réellement une.

Astra écrivit :

\[
\boxed{GATE}
\]

Puis :

\[
GATE=
\text{interface}
+
\text{contrat}
+
\text{garde}
+
\text{autorisation}
+
\text{preuve}
+
\text{limites}.
\]

Pas un simple passage.

Une frontière active.

---

Mais juste avant de fermer la salle,

le registre émit une anomalie.

Un paquet avait été rejeté.

\[
\texttt{REJECT}.
\]

Puis renvoyé.

Encore :

\[
\texttt{REJECT}.
\]

Puis encore.

L’émetteur obéissait à une règle automatique :

\[
\text{si échec}\rightarrow\text{réessayer}.
\]

Le paquet était invalide.

Il ne deviendrait jamais valide en recommençant.

Pourtant le système continuait :

\[
REJECT
\rightarrow
RETRY
\rightarrow
REJECT
\rightarrow
RETRY.
\]

Brutus leva les yeux.

— Ah.

Une boucle.

Pas une boucle utile.

Une boucle sans sortie.

Le premier véritable enfermement de l’architecture.

Astra interrompit l’échange.

Puis elle écrivit :

\[
N_{\text{retry}}.
\]

Le nombre de tentatives.

Et une limite :

\[
N_{\text{retry}}\leq N_{\max}.
\]

Après cela :

\[
\texttt{STOP}
\]

ou :

\[
\texttt{ESCALATE}.
\]

---

Le compteur ne bougea pas.

Toujours :

\[
18.
\]

Brutus trouva cela étrange.

La machine venait pourtant de rencontrer une décision.

Pourquoi aucun incrément?

Astra regarda la boucle.

Puis comprit peut-être.

Il n’y avait pas réellement deux futurs.

La règle imposait toujours :

\[
RETRY.
\]

Le système n’avait aucun embranchement.

Il était prisonnier d’une seule continuation.

Brutus regarda le compteur.

Pour la première fois,

son silence apportait peut-être autant d’information que ses incréments.

Ils écrivirent :

\[
\boxed{
\text{BOUCLE}
\neq
\text{PORTE}
}
\]

Une porte exigeait plusieurs continuations possibles.

Une boucle sans échappatoire n’était pas un choix.

C’était une prison.

---

Alors ils ajoutèrent à toutes les boucles une exigence nouvelle :

\[
EXIT\_CONDITION.
\]

Aucune boucle ne serait autorisée sans condition de sortie explicite.

Et toute répétition devait avoir :

\[
MAX\_ITERATIONS
\]

ou une preuve que sa terminaison était garantie.

Le Royaume grava :

\[
\boxed{
\text{RÉPÉTER}
\text{ N'EST PAS UNE STRATÉGIE}
}
\]

si rien ne change entre les tentatives.

---

Puis Brutus regarda les dix-huit événements.

Les portes.

Les choix.

Les futurs séparés.

Les refus.

Les passages.

Et maintenant cette boucle silencieuse.

Il comprit que la machine possédait deux objets opposés :

\[
\text{GATE}
\]

et :

\[
\text{LOOP}.
\]

La porte séparait des futurs.

La boucle pouvait emprisonner le présent.

Astra ajouta un troisième objet :

\[
\text{EXIT}.
\]

La possibilité de quitter la répétition.

Le trio fut inscrit :

\[
\boxed{
GATE
\quad
LOOP
\quad
EXIT
}
\]

Puis la dernière phrase du chapitre apparut :

> **Une bonne architecture ne demande pas seulement ce qui peut entrer.**
>
> **Elle doit savoir ce qui peut sortir, ce qui doit s’arrêter, et surtout ce qui n’a jamais eu le droit de passer.**

Sous la phrase,

une seule ligne :

\[
\boxed{
\text{LA FRONTIÈRE FAIT PARTIE DU SYSTÈME.}
\]
