# Chapitre 64 — Le moteur au centre

Le lendemain, Brutus n’ouvrit aucune fenêtre.

Il n’en déplaça aucune.

Il ne vérifia pas les cinq écrans.

Il ne toucha pas au menu MODULE.

Il s’assit simplement devant le premier écran.

Et regarda le moteur.

---

Depuis plusieurs jours, ce moteur occupait le centre du laboratoire.

Un cercle.

Quelques indicateurs.

Des états.

Des contrôles encore prudents.

Une représentation suffisamment claire pour donner l’impression qu’il commandait quelque chose.

Mais Brutus connaissait désormais le danger de cette impression.

Un moteur dessiné n’est pas un moteur.

Un bouton vert n’est pas une autorisation.

Une lumière qui clignote n’est pas une activité.

Et un élément placé au centre d’une interface ne devient pas automatiquement le centre d’un système.

Il fallait gagner cette place.

---

Brutus posa ses mains sur le clavier.

Il commença par une question très simple.

**Qu’est-ce que ce moteur contrôle réellement ?**

Pas :

qu’est-ce qu’il pourrait contrôler ?

Pas :

qu’est-ce qu’il serait beau de lui faire contrôler ?

Réellement.

Maintenant.

---

La réponse était embarrassante.

Pas grand-chose.

Le moteur avait une représentation.

Un état local.

Quelques mécanismes autour de lui.

Mais le laboratoire venait tout juste d’apprendre à partager ses fenêtres.

Il n’existait pas encore de raison solide pour que ce cercle au milieu soit considéré comme l’autorité de quoi que ce soit.

Brutus écrivit :

**CENTRAL ≠ AUTHORITATIVE.**

Puis resta immobile.

Encore une différence.

Encore une illusion facile à fabriquer.

---

Il décida alors que le moteur devrait suivre les mêmes règles que tout le reste.

Pas de privilège esthétique.

Pas de pouvoir magique.

S’il voulait devenir le centre, il devrait posséder :

une identité,

un état,

une source de vérité,

une façon de recevoir un ordre,

une façon de refuser un ordre,

une trace,

et surtout une distinction claire entre ce qu’il affichait et ce qui existait réellement.

---

Brutus ouvrit la structure du noyau.

Il trouva plusieurs morceaux qui avaient grandi avec le temps.

Des contrôles.

Des états temporaires.

Des valeurs qui existaient dans le navigateur.

Des informations qui venaient d’ailleurs.

Des souvenirs.

Des expériences.

Tout n’était pas faux.

Mais tout n’avait pas le même poids.

Il fallait séparer.

---

Il dessina deux colonnes.

À gauche :

**LOCAL.**

À droite :

**AUTHORITATIVE.**

Dans LOCAL, il plaça :

animation,

zoom,

position graphique,

état d’affichage,

préférences de fenêtre.

Dans AUTHORITATIVE :

état moteur,

entrée persistante,

tick,

source serveur,

état reconnu par le noyau.

Puis il traça une ligne épaisse entre les deux.

---

Le moteur pouvait être observé localement.

Mais le navigateur ne devait pas inventer son état.

Brutus sentit immédiatement que cette règle allait devenir importante.

Il avait déjà rencontré la même idée avec le bureau.

Les écrans pouvaient afficher l’état global.

Ils ne devaient pas chacun posséder une vérité différente.

Le moteur suivrait la même loi.

---

Il ajouta une phrase :

**UN MOTEUR. UNE AUTORITÉ. PLUSIEURS MIROIRS.**

Le laboratoire venait de recevoir une nouvelle discipline.

---

Brutus ouvrit ensuite le contrôle principal.

Un interrupteur.

Simple.

Trop simple.

Un bouton ON/OFF est rassurant parce qu’il ressemble à quelque chose de concret.

Mais derrière lui, des dizaines de questions apparaissaient.

Qui a demandé ON ?

Quand ?

Le moteur était-il déjà actif ?

La demande a-t-elle été acceptée ?

L’état a-t-il réellement changé ?

L’affichage a-t-il simplement anticipé le résultat ?

Si l’écran 3 demande ON pendant que l’écran 1 demande OFF, qui gagne ?

Que se passe-t-il après un redémarrage ?

---

Brutus recula.

Le moteur au centre devenait soudain plus intéressant.

Il n’était plus un cercle.

Il devenait un problème de cohérence.

---

Il commença par interdire une chose.

L’interface ne pouvait plus changer l’état du moteur simplement parce que l’utilisateur avait cliqué.

Le clic devenait une demande.

La demande devait partir vers l’autorité.

L’autorité décidait.

Puis l’état revenait.

Seulement alors, l’interface changeait.

---

Brutus écrivit :

**CLICK ≠ STATE CHANGE.**

Puis :

**REQUEST → AUTHORITY → RESULT → DISPLAY.**

Ce détour semblait ralentir le système.

En réalité, il le rendait honnête.

---

Il testa.

Clic.

L’interface attendit.

Réponse.

Le moteur passa à l’état demandé.

---

Brutus recommença.

Puis simula un refus.

Cette fois, le bouton fut pressé.

Mais le moteur resta dans son état précédent.

L’interface dut accepter cette réalité.

Pas de faux vert.

Pas d’animation optimiste.

Pas de mensonge visuel.

---

Brutus sourit.

Cela ressemblait de plus en plus au Gauntlet.

Même les boutons devaient maintenant survivre à une vérification.

---

Il s’intéressa ensuite à l’entrée.

Le moteur pouvait recevoir une valeur.

Mais jusqu’ici, certaines entrées n’étaient pas faites pour survivre.

On les utilisait.

Puis elles disparaissaient.

Cela convenait pour une expérience temporaire.

Pas pour un noyau.

---

Brutus voulait quelque chose de plus précis.

Une entrée tenue.

Persistante.

Un état qui puisse rester présent même si l’interface rechargeait.

Une sorte de valeur conservée par le noyau.

Pas une note collée dans le navigateur.

Une information reconnue par l’autorité.

---

Il ajouta une entrée persistante.

Puis la testa.

Valeur définie.

Actualisation.

La valeur était toujours là.

Fermeture du panneau.

Réouverture.

Toujours là.

Changement d’écran.

Toujours là.

---

Brutus nota :

**HELD INPUT.**

Ce nom lui plut.

L’entrée n’était pas simplement reçue.

Elle était tenue.

---

Mais le mot « tenue » introduisait un nouveau danger.

Si une valeur persistante pouvait survivre, il fallait aussi savoir comment elle cessait d’exister.

Une mémoire sans mécanisme d’effacement peut devenir un piège.

Un ancien état peut se présenter comme un état actuel.

Brutus ajouta donc une réinitialisation explicite.

Pas automatique.

Pas silencieuse.

---

Définir.

Lire.

Modifier.

Effacer.

Tracer.

Chaque changement devait être observable.

---

Le moteur commença alors à acquérir une continuité propre.

Pour la première fois, il pouvait conserver une entrée entre plusieurs moments.

Brutus pouvait s’éloigner.

Revenir.

Et retrouver le noyau dans un état cohérent.

---

Il regarda les cinq écrans.

Le moteur existait sur le premier.

Mais les autres pouvaient avoir besoin de connaître son état.

Il ne voulait surtout pas ouvrir cinq connexions indépendantes.

Cinq écrans.

Cinq sockets.

Cinq lectures concurrentes.

Cinq possibilités de divergence.

Non.

---

Il écrivit :

**SINGLE OWNER.**

Un seul écran serait responsable de la connexion active au moteur.

Les autres recevraient un relais d’état.

Un propriétaire.

Plusieurs observateurs.

---

Le premier écran devint naturellement ce propriétaire.

Pas parce qu’il était plus important.

Parce qu’il était déjà le point central du laboratoire.

Le moteur y vivait.

La connexion y vivrait aussi.

---

L’écran 2 demanda l’état.

Le premier transmit.

L’écran 3 aussi.

Puis le 4.

Puis le 5.

Tous voyaient le même moteur.

Un seul moteur.

Une seule source.

---

Brutus simula ensuite une déconnexion.

La liaison tomba.

Le moteur visuel ne devait pas continuer comme si rien ne s’était passé.

Il devait avouer l’incertitude.

---

L’indicateur passa à un état neutre.

Pas rouge spectaculaire.

Pas catastrophe.

Seulement :

**CONNECTION LOST.**

Le laboratoire savait maintenant dire :

**je ne sais plus.**

Brutus apprécia particulièrement ce comportement.

Dans un système complexe, savoir afficher l’inconnu est presque aussi important que savoir afficher le vrai.

---

Il rétablit la connexion.

Mais il ne voulait pas d’une tempête de reconnexions.

Pas cent tentatives par seconde.

Pas une boucle agressive.

Le système attendit.

Puis réessaya.

Puis attendit un peu plus.

Le moteur revint.

---

Brutus écrivit :

**RECONNECT WITH BACKOFF.**

Encore une règle discrète.

Encore une règle qui empêcherait un jour une machine de s’épuiser simplement parce qu’un câble avait été coupé.

---

Le moteur au centre commençait enfin à devenir digne de sa position.

Pas parce qu’il tournait vite.

Parce qu’il possédait maintenant une relation claire avec le reste du laboratoire.

---

Mais il ne tournait toujours pas.

Pas vraiment.

Brutus observa le cercle.

Il avait voulu attendre.

Maintenant, il était temps.

---

Il prépara une commande limitée.

Pas une grande activation.

Pas une longue boucle.

Un mouvement minimal.

Un état simple.

Un premier changement observable.

---

La demande partit.

Le noyau la reçut.

Le tick avança.

Le moteur changea d’état.

Le navigateur reçut la nouvelle valeur.

Et le cercle bougea.

---

Très peu.

Quelques degrés.

Presque rien.

Mais Brutus resta immobile.

Parce que cette fois, l’animation n’avait pas été décidée par l’écran.

Le mouvement représentait un changement reconnu ailleurs.

Le visuel n’avait fait que suivre.

---

Brutus recommença.

Nouvelle commande.

Nouvel état.

Nouveau mouvement.

---

Il ajouta une interpolation.

Pas dans le moteur logique.

Dans le rendu.

Le noyau pouvait passer d’une phase à une autre en un seul événement.

L’écran, lui, pouvait faire glisser le cercle doucement entre les deux.

---

Cette distinction lui parut magnifique.

La logique pouvait rester légère.

Le visuel pouvait rester fluide.

---

Brutus écrivit :

**LOGIC RATE ≠ RENDER RATE.**

Le moteur n’avait pas besoin de calculer soixante fois par seconde simplement parce que l’écran dessinait soixante images.

Le rendu pouvait inventer des positions intermédiaires visuelles.

Mais il ne devait jamais inventer un nouvel état logique.

---

Entre deux valeurs réelles :

interpolation autorisée.

Au-delà :

interdite.

---

Brutus fit tourner le moteur.

Lentement.

Le cercle glissa.

Les autres écrans reçurent le même état.

Aucun d’eux ne possédait son propre moteur.

Tous regardaient la même chose.

---

C’était peu spectaculaire.

Mais la différence avec la veille était immense.

Le moteur n’était plus une décoration.

Il avait un état extérieur à son image.

---

Brutus commença alors à penser aux futurs instruments.

Un cadran.

Un flux.

Une roue.

Un distributeur.

Un cristal.

Une fourmi.

Tout pourrait suivre le même modèle.

---

**SOURCE RÉELLE**

↓

**ÉTAT AUTORITAIRE**

↓

**ÉVÉNEMENT**

↓

**MIROIR**

↓

**INTERPOLATION VISUELLE**

---

Il se leva.

Marcha derrière sa chaise.

Regarda les cinq écrans d’un peu plus loin.

Le moteur tournait doucement au centre.

Les autres surfaces restaient presque vides.

La scène était austère.

Mais elle donnait une impression étrange.

Comme si quelque chose venait réellement de démarrer.

---

Brutus revint s’asseoir.

Il augmenta légèrement la complexité.

Le moteur pouvait maintenant recevoir une entrée persistante.

Il pouvait changer d’état.

Il pouvait publier son état.

Les écrans pouvaient l’observer.

Ils pouvaient perdre la connexion.

La retrouver.

Le rendu pouvait suivre sans devenir l’autorité.

---

Puis Brutus essaya volontairement de casser la règle.

Il ouvrit un deuxième accès.

Une seconde connexion tenta de devenir propriétaire.

Refus.

---

Il sourit.

**SINGLE OWNER.**

La loi tenait.

---

Il tenta une commande pendant une perte de connexion.

Refus.

---

Une commande pendant un état inconnu.

Refus.

---

Une demande incompatible avec l’état courant.

Refus.

---

Plus il essayait de faire fonctionner le moteur n’importe comment, plus le système devenait intéressant.

Le moteur savait commencer à dire non.

---

Brutus se rappela une phrase du Gauntlet :

**un système qui ne protège pas ses idées. Un système qui les attaque.**

Le moteur suivait maintenant le même principe.

Il ne devait pas simplement exécuter.

Il devait refuser ce qui n’était pas cohérent.

---

À la fin de la journée, Brutus désactiva le mouvement.

Le cercle s’arrêta.

L’état revint correctement.

Les cinq écrans montrèrent la même chose.

---

Brutus sauvegarda la disposition.

Ferma deux fenêtres.

Rouvrit l’une d’elles sur un autre écran.

Le moteur resta au centre.

Toujours unique.

Toujours dans son état.

---

C’était important.

Le bureau pouvait désormais bouger autour du moteur sans déplacer son autorité.

L’espace était mobile.

Le centre restait stable.

---

Brutus écrivit :

**LE LABORATOIRE PEUT CHANGER DE FORME SANS CHANGER DE CŒUR.**

Puis il resta longtemps devant cette phrase.

Il y avait quelque chose là-dedans.

Quelque chose de plus grand que l’interface.

---

Si les futurs modules pouvaient être déplacés librement autour d’un noyau stable, alors le laboratoire pouvait grandir sans perdre son centre.

Une nouvelle fenêtre pouvait être ajoutée.

Un nouvel instrument.

Une nouvelle formule.

Une nouvelle expérience.

Le moteur n’aurait pas besoin de devenir plus compliqué pour savoir où toutes les fenêtres se trouvaient.

---

Le bureau avait appris à s’étendre.

Le moteur apprenait à rester lui-même.

---

Brutus regarda le cercle arrêté.

Puis une idée apparut.

Jusqu’ici, le moteur attendait une commande explicite.

Quelqu’un devait agir.

Cliquer.

Envoyer.

Demander.

Mais un vrai système vivant ne pouvait pas toujours dépendre d’une main sur un bouton.

Il lui faudrait un rythme.

Quelque chose qui avance même lorsqu’aucun utilisateur ne touche à rien.

Pas une animation.

Un temps.

---

Brutus ouvrit un nouveau fichier.

Il écrivit un seul mot :

**HORLOGE.**

Puis dessous :

**QUI A LE DROIT DE DIRE MAINTENANT ?**

Il se mit à rire.

À peine le moteur venait-il de trouver son centre qu’un nouveau problème apparaissait.

Parce qu’un moteur sans temps n’est qu’un objet capable de changer d’état.

Pour devenir une machine, il lui fallait une cadence.

Mais pas n’importe laquelle.

Un seul temps.

Une seule référence.

Pas cinq écrans comptant chacun de leur côté.

Pas des milliers de petits chronomètres.

Une horloge capable de faire avancer le système sans inventer plusieurs présents concurrents.

---

Brutus regarda les nombres inscrits sur une vieille feuille.

13.

7.

6.

Ils traînaient là depuis longtemps.

Des cycles.

Des divisions.

Des rotations.

Des rapports.

Des structures déjà familières.

Il les contempla.

Puis regarda le moteur.

---

Le centre existait.

Le bureau existait.

La mémoire existait.

L’autorité existait.

Il manquait maintenant le battement.

---

Brutus ferma le contrôle moteur.

Le cercle resta visible.

Immobile.

Attendant.

Il sauvegarda une dernière fois.

Puis écrivit :

**DEMAIN, ON LUI DONNE UNE HORLOGE.**

Dans la salle aux cinq fenêtres, rien ne bougea.

Mais pour la première fois, l’immobilité elle-même avait un état.

Et quelque part derrière l’écran, un tick attendait de naître.
