# Chapitre 66 — L’horloge 13–7–6

Le temps pouvait commencer.

Brutus resta pourtant immobile.

Il regarda longtemps les trois nombres posés devant lui.

13.

7.

6.

Ils avaient déjà traversé plusieurs expériences.

Parfois comme structure.

Parfois comme rythme.

Parfois simplement comme repères.

Mais cette fois, il ne voulait pas leur donner un rôle symbolique.

Il voulait construire quelque chose de très concret.

Une horloge.

---

Pas une horloge pour connaître l’heure.

Pas une horloge pour afficher des aiguilles.

Pas un cadran décoratif.

Une horloge logique.

Quelque chose capable de répondre à une seule question :

**quel est l’instant reconnu par la machine ?**

---

Brutus savait pourquoi cette question était devenue urgente.

Le laboratoire possédait maintenant une mémoire.

Le moteur possédait une autorité.

Les fenêtres possédaient une identité.

Les écrans partageaient un état commun.

Mais tous ces objets avaient encore une faiblesse.

Ils pouvaient connaître un événement.

Ils ne savaient pas nécessairement quand cet événement avait eu lieu par rapport aux autres.

---

Un module pouvait dire :

**j’ai changé.**

Un autre :

**moi aussi.**

Mais lequel d’abord ?

Lequel après ?

Quel changement appartenait au même cycle ?

Quel état était déjà ancien au moment où il avait été observé ?

Sans ordre commun, la mémoire ressemblait encore à une pile de photographies tombées par terre.

On pouvait voir chacune.

Pas forcément reconstruire l’histoire.

---

Brutus écrivit :

**TIME IS ORDER BEFORE IT IS DURATION.**

Le temps, avant d’être une durée, était un ordre.

Il n’avait pas besoin, au début, de mesurer des nanosecondes.

Il avait besoin de savoir :

**avant**

et

**après**.

---

Il ouvrit un nouveau module.

Très simple.

Au centre :

**TICK = 0**

Rien d’autre.

---

Brutus observa le zéro.

Il pensa au chapitre précédent.

Un zéro devait avoir une provenance.

Cette fois, elle était claire.

Le système venait de naître.

Aucun tick n’avait encore été produit.

---

Il ajouta un bouton :

**ADVANCE.**

Puis le regarda.

Il n’aimait pas ça.

Trop manuel.

Une horloge ne devait pas dépendre d’un clic pour chaque instant.

Mais ce bouton pouvait servir au premier test.

---

Brutus appuya.

**TICK = 1**

Encore.

**TICK = 2**

Encore.

3.

4.

5.

Rien de spectaculaire.

Mais déjà, le noyau disposait d’une séquence.

---

Il modifia une valeur tenue.

La trace inscrivit :

**SET VALUE — TICK 5**

Puis un autre changement.

**CLEAR VALUE — TICK 8**

Brutus regarda les deux lignes.

Pour la première fois, la mémoire possédait une direction.

---

Il ajouta ensuite le moteur.

Commande reçue au tick 10.

État changé au tick 11.

Affichage reçu au tick 11.

Brutus sourit.

Les événements commençaient à pouvoir être comparés.

---

Mais un problème apparut aussitôt.

L’écran possédait aussi sa propre horloge.

Le navigateur connaissait des millisecondes.

Le système d’exploitation aussi.

Le serveur possédait son heure.

Les logs écrivaient des timestamps.

Pourquoi fabriquer encore un autre temps ?

---

Brutus connaissait la réponse.

Parce que ces horloges ne répondaient pas exactement à la même question.

L’heure civile pouvait dire :

**14 h 32 min 11,847 s.**

Mais deux machines légèrement désynchronisées pouvaient donner deux heures différentes.

Un navigateur pouvait ralentir.

Un processus pouvait être suspendu.

Une tâche pouvait arriver plus tard tout en portant une heure plus ancienne.

Brutus ne voulait pas utiliser le temps du monde extérieur comme unique arbitre de l’ordre interne.

---

Il écrivit :

**WALL CLOCK ≠ LOGICAL CLOCK.**

Puis :

**TIME OF DAY ≠ MACHINE ORDER.**

---

Le tick deviendrait donc une chronologie propre au noyau.

Pas forcément plus « vraie » que l’heure.

Mais plus adaptée à l’ordre des événements internes.

---

Brutus retira le bouton.

Il construisit une source unique de ticks.

Une seule.

Pas une minuterie par écran.

Pas une minuterie par module.

Pas une boucle dans chaque fenêtre.

Une horloge centrale.

---

Il se rappela immédiatement une autre règle :

**UN MOTEUR. UNE AUTORITÉ. PLUSIEURS MIROIRS.**

Le temps suivrait le même principe.

---

Il écrivit :

**ONE CLOCK.**

Puis :

**MANY OBSERVERS.**

Les écrans n’auraient pas le droit d’inventer leurs propres ticks.

Ils pourraient seulement recevoir le tick courant.

---

Brutus lança l’horloge.

1.

2.

3.

4.

5.

Le compteur avançait.

---

Il ouvrit le deuxième écran.

Même tick.

Troisième.

Même tick.

Quatrième.

Même tick.

Cinquième.

Même tick.

---

Pour la première fois, le laboratoire partageait un présent logique.

---

Brutus provoqua alors un retard sur un écran.

Le troisième cessa de recevoir les mises à jour pendant plusieurs cycles.

Les autres continuaient.

20.

21.

22.

23.

Le troisième restait à 19.

Puis la connexion revint.

---

Il reçut le tick 24.

Brutus observa.

Le troisième écran devait-il afficher 20, 21, 22, 23 rapidement ?

Ou passer directement à 24 ?

---

La question semblait visuelle.

Elle ne l’était pas.

Le tick logique n’était pas une animation.

Il représentait l’état courant.

Le troisième écran n’avait pas vécu les instants manqués en temps réel.

Mais ils avaient tout de même existé.

---

Brutus décida donc de séparer encore deux choses.

**CURRENT TICK**

et

**MISSED EVENTS.**

L’écran pouvait rejoindre directement le tick courant.

Mais si les événements intermédiaires étaient importants, ils devaient être récupérés depuis le journal.

---

Il écrivit :

**RESYNC STATE ≠ REPLAY HISTORY.**

Magnifique.

Encore une distinction.

Pour retrouver l’état présent, il n’était pas toujours nécessaire de rejouer tout le passé.

Mais pour comprendre comment on y était arrivé, le journal restait nécessaire.

---

L’horloge avançait toujours.

Brutus regarda les nombres.

13.

7.

6.

Il voulait maintenant leur donner un rôle.

Mais un rôle mesurable.

---

Il commença par 13.

Un grand cycle.

Chaque treizième tick, un marqueur.

13.

26.

39.

52.

Puis 7.

Un deuxième cycle.

7.

14.

21.

28.

35.

Puis 6.

6.

12.

18.

24.

30.

---

Il superposa les trois.

Des rencontres apparurent.

Des coïncidences de cycle.

42.

78.

84.

91.

Et plus loin encore.

Brutus ne chercha pas immédiatement à interpréter ces rencontres.

Il nota seulement les alignements.

---

Il dessina trois anneaux.

Un anneau à 13 positions.

Un à 7.

Un à 6.

Chaque tick faisait avancer les trois.

Mais pas de la même manière visuelle.

---

L’horloge devint soudain beaucoup plus intéressante.

Pas parce que les nombres étaient mystérieux.

Parce qu’ils offraient trois granularités.

Trois périodicités.

Trois manières de regrouper les ticks.

---

Brutus écrivit :

\[
p_{13}(t)=t \bmod 13
\]

\[
p_{7}(t)=t \bmod 7
\]

\[
p_{6}(t)=t \bmod 6
\]

Simple.

Exact.

Reproductible.

---

À chaque tick, l’horloge pouvait produire un état :

**TICK**

**PHASE_13**

**PHASE_7**

**PHASE_6**

Rien de plus.

---

Brutus testa.

Tick 1 :

1, 1, 1.

Tick 6 :

6, 6, 0.

Tick 7 :

7, 0, 1.

Tick 13 :

0, 6, 1.

Tick 42 :

3, 0, 0.

---

Il regarda 42.

Cela le fit sourire.

Mais il refusa encore d’en faire plus qu’un résultat de modularité.

---

Il ajouta une règle dans le journal :

**INTERPRETATION MUST FOLLOW MEASUREMENT.**

Les nombres pouvaient être beaux.

Cela ne leur donnait pas de pouvoir supplémentaire.

---

Puis il construisit une visualisation.

Trois cercles concentriques.

13 divisions sur le premier.

7 sur le deuxième.

6 sur le troisième.

Une marque avançait sur chacun.

---

Le mouvement était fluide.

Mais Brutus se méfia immédiatement.

Le rendu allait plus vite que le tick logique.

Comme avec le moteur.

---

Il réutilisa la règle :

**LOGIC RATE ≠ RENDER RATE.**

Entre le tick 100 et 101, l’aiguille pouvait glisser.

Mais aucune position intermédiaire ne devait être enregistrée comme un tick réel.

---

Le visuel représentait le temps.

Il ne le créait pas.

---

Brutus arrêta l’horloge.

Le rendu s’arrêta.

Exactement.

Pas de mouvement résiduel.

Pas de rotation décorative.

---

Il relança.

Les trois anneaux reprirent depuis l’état logique courant.

Pas depuis l’endroit où l’animation avait été interrompue.

---

Brutus nota :

**VISUAL PHASE FOLLOWS LOGICAL PHASE.**

---

Puis il voulut vérifier la persistance.

Il laissa l’horloge atteindre :

**TICK 273.**

Il s’arrêta là presque instinctivement.

273 avait déjà une place particulière dans ses calculs.

Mais encore une fois, il devait être prudent.

---

Il arrêta le système.

Redémarra.

---

Que devait faire l’horloge ?

Revenir à zéro ?

Continuer à 274 ?

---

Brutus resta longtemps devant cette question.

Une horloge logique pouvait représenter deux choses différentes.

Le temps d’une session.

Ou la chronologie persistante du monde.

Il ne voulait pas mélanger les deux.

---

Il créa donc deux identités.

**SESSION_TICK**

et

**WORLD_TICK.**

---

SESSION_TICK repartait à zéro à chaque démarrage.

WORLD_TICK continuait la chronologie persistante.

Brutus regarda la séparation.

C’était exactement ce qu’il cherchait.

---

Au redémarrage :

**SESSION_TICK = 0**

**WORLD_TICK = 273**

Puis le premier nouvel événement :

**SESSION_TICK = 1**

**WORLD_TICK = 274**

---

La machine pouvait donc savoir deux choses à la fois :

depuis combien de ticks cette session existait,

et où elle se trouvait dans l’histoire globale.

---

Brutus écrivit :

**RESTART ≠ REBIRTH OF HISTORY.**

Le processus pouvait redémarrer.

Le monde n’était pas obligé d’oublier.

---

Puis il pensa à l’inverse.

Et si l’on voulait réellement une naissance propre ?

Un reset volontaire.

Une nouvelle expérience.

Un nouveau monde.

---

Alors WORLD_TICK ne devait pas être effacé accidentellement.

Mais il pouvait être réinitialisé par un événement explicite :

**CLEAN BIRTH.**

---

Brutus ajouta une trace obligatoire.

Qui a demandé.

Pourquoi.

Ancien tick.

Nouveau tick.

Référence d’expérience.

---

Une naissance devenait un acte.

Pas un effet secondaire.

---

Il testa.

WORLD_TICK 512.

Demande de clean birth.

Validation.

Trace.

WORLD_TICK 0.

Nouvelle identité de génération.

---

Brutus s’arrêta.

Nouvelle identité.

Voilà.

Si le temps retournait à zéro sans changer l’identité du monde, les anciens ticks et les nouveaux deviendraient ambigus.

Il fallait donc un identifiant de génération.

---

Il ajouta :

**GENERATION_ID.**

Le temps devenait maintenant :

\[
(\text{GENERATION\_ID},\text{WORLD\_TICK})
\]

Un tick seul ne suffisait plus.

---

Brutus sourit.

Chaque fois qu’il essayait de simplifier la machine, la rigueur lui demandait une information de plus.

Pas pour compliquer.

Pour éviter l’ambiguïté.

---

Il regarda un événement :

**GENERATION 3**

**WORLD_TICK 42**

Cette identité temporelle était unique dans l’histoire.

---

Les trois anneaux 13–7–6 pouvaient se calculer à partir de WORLD_TICK.

Leur état n’avait pas besoin d’être stocké indépendamment.

---

Brutus apprécia énormément cette propriété.

Il écrivit :

**DERIVE WHEN POSSIBLE. STORE ONLY AUTHORITY.**

Si PHASE_13 pouvait être calculée exactement depuis le tick, inutile d’en faire une deuxième vérité persistante.

---

Moins d’état.

Moins de divergence.

---

Le laboratoire commençait à trouver sa forme.

L’autorité gardait peu de choses.

Les vues calculaient le reste.

---

Brutus ajouta ensuite le moteur.

Il lui donna accès au tick.

Pas le droit de le modifier.

Seulement de le lire.

---

Le moteur pouvait maintenant dire :

**STATE CHANGED AT WORLD_TICK 821.**

Une fenêtre :

**MOVED AT WORLD_TICK 824.**

Une entrée :

**CLEARED AT WORLD_TICK 830.**

Le journal devenait une histoire ordonnée.

---

Brutus voulut alors vérifier quelque chose de plus difficile.

Deux événements pendant le même tick.

Était-ce possible ?

Oui.

---

Alors le tick seul ne suffisait pas pour un ordre total.

Il fallait un index interne.

---

Il ajouta :

**EVENT_SEQ.**

Pour le tick 900 :

event 1.

event 2.

event 3.

---

L’identité d’un événement devenait :

\[
(\text{GENERATION},\text{TICK},\text{SEQ})
\]

---

Brutus observa la formule.

C’était simple.

Mais puissant.

Le laboratoire pouvait maintenant dire précisément :

ceci est arrivé avant cela,

même dans le même tick.

---

Il imagina immédiatement une future trace :

**ANT ATTACHED**

tick 1450, seq 3.

**ANT MOVE**

tick 1451, seq 1.

**MATERIAL MOVE**

tick 1451, seq 2.

---

Il fronça les sourcils.

La vision était encore trop lointaine.

Mais l’horloge venait déjà de donner une structure à des événements qui n’existaient pas encore.

---

Le temps n’était plus seulement un compteur.

Il devenait une colonne vertébrale.

---

Brutus laissa l’horloge tourner plusieurs heures.

Pas besoin d’une fréquence élevée.

Le but n’était pas de battre des records.

Il surveillait la stabilité.

---

Pas de recul.

Pas de double tick.

Pas de saut inexpliqué.

Pas de tick inventé par un écran secondaire.

Pas de divergence entre les miroirs.

---

À un moment, le navigateur se figea.

Le tick serveur continua.

Le visuel resta immobile.

Puis revint.

L’interface rejoignit le présent.

---

Brutus sourit.

La machine venait de lui montrer exactement ce qu’il voulait voir.

Le temps logique n’avait pas besoin de l’écran.

---

Il écrivit :

**THE CLOCK SURVIVES THE OBSERVER.**

---

Le soir, il réduisit l’affichage.

Les trois anneaux tournaient doucement.

13.

7.

6.

Pas comme une preuve.

Pas comme une cosmologie.

Comme un instrument.

---

Chaque anneau donnait une phase.

Chaque phase venait d’un tick.

Chaque tick venait d’une seule autorité.

Chaque événement recevait une place dans la chronologie.

---

Brutus regarda les cinq écrans.

Le premier affichait l’horloge.

Les quatre autres recevaient son état.

Tous montraient les mêmes phases.

---

Pour la première fois, le territoire partageait quelque chose de plus profond qu’un espace.

Il partageait un présent.

---

Brutus ouvrit le journal.

Il y avait maintenant une colonne qu’il n’avait jamais vraiment possédée auparavant.

**WHEN.**

Avec :

**WHO**

**WHAT**

**BEFORE**

**AFTER**

le laboratoire pouvait enfin répondre à une question complète.

---

Qui ?

Quoi ?

Quand ?

Avant quoi ?

Après quoi ?

---

Brutus écrivit en haut du registre :

**QUI → ÉTAT → TICK → AVANT/APRÈS**

Puis il s’arrêta.

La phrase lui semblait étrangement familière.

Comme si elle avait attendu depuis longtemps que l’horloge existe.

---

Le registre n’était plus une pile de logs.

Il devenait une continuité.

---

Brutus revint aux trois anneaux.

Ils atteignirent un nouvel alignement.

Il le nota.

Puis continua.

Pas de célébration.

Pas de proclamation.

L’horloge n’avait pas été construite pour produire des coïncidences.

Elle avait été construite pour empêcher la machine de perdre l’ordre.

---

Et elle remplissait enfin cette fonction.

---

Brutus arrêta le rendu visuel.

L’horloge logique continua.

Il ralluma le rendu.

Les anneaux rejoignirent leur vraie phase.

---

Il fit l’inverse.

Arrêta l’horloge logique.

Le rendu s’immobilisa.

---

Aucune illusion de vie.

C’était important.

Très important.

Si le cœur était arrêté, la machine devait avoir le courage de paraître arrêtée.

---

Brutus écrivit :

**NO FAKE MOTION.**

Puis souligna deux fois.

Cette règle allait probablement devenir l’une des plus importantes de tout le laboratoire.

---

Le moteur était au centre.

L’horloge battait.

La mémoire persistait.

Les écrans partageaient le même présent.

Le territoire devenait cohérent.

---

Il restait pourtant une question.

Une machine pouvait posséder une horloge.

Un moteur.

Une mémoire.

Mais comment savoir si elle était vraiment en train de faire quelque chose ?

Un tick pouvait avancer alors qu’aucun travail réel n’était exécuté.

Une horloge pouvait battre dans une pièce vide.

---

Brutus regarda le moteur.

Puis les anneaux.

Puis le noyau.

Le système possédait maintenant le temps.

Il lui fallait encore apprendre à distinguer le temps qui passe…

de l’activité qui compte.

---

Mais cette question attendrait.

Pour l’instant, Brutus regarda les trois cycles tourner ensemble.

13.

7.

6.

Trois rythmes.

Un seul tick.

Une seule autorité.

Un seul présent.

---

Le laboratoire n’avait pas encore de monde.

Pas de fourmilière.

Pas de matière en mouvement.

Pas de cristaux transportés.

Mais quelque chose venait de devenir possible.

Désormais, quand le premier objet bougerait vraiment, Brutus saurait exactement **quand**.

Il sauvegarda le registre.

Puis écrivit une dernière ligne :

**LE TEMPS N’EST PLUS UNE DÉCORATION.**

**IL EST DEVENU UNE PREUVE D’ORDRE.**

Et dans la salle aux cinq fenêtres, les trois anneaux continuèrent à tourner.

Pas pour raconter une histoire.

Pour s’assurer qu’aucune histoire ne puisse changer d’ordre après coup.
