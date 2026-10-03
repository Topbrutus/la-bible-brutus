# Chapitre 63 — Le bureau qui traverse les écrans

Le moteur semblait déjà l’attendre.

Brutus resta quelques secondes devant l’écran principal, sans toucher à rien.

La salle aux cinq fenêtres existait maintenant.

Elle pouvait s’ouvrir.

Se refermer.

Mémoriser une disposition.

Revenir à son état précédent.

Les modules pouvaient être cachés, retrouvés, déplacés.

Sur le papier, cela ressemblait déjà à un laboratoire.

Mais Brutus savait qu’il manquait encore quelque chose.

Quelque chose de beaucoup plus difficile à obtenir que cinq écrans allumés côte à côte.

Il fallait que le laboratoire oublie qu’il y avait cinq écrans.

---

Pas complètement.

Les écrans devaient évidemment continuer d’exister.

Chacun avec ses limites physiques.

Ses coordonnées.

Sa résolution.

Son bord.

Mais pour l’opérateur, ces frontières devaient devenir secondaires.

Le bureau devait se comporter comme une seule grande surface.

Un territoire continu.

Brutus voulait pouvoir prendre une fenêtre avec la souris, traverser le bord d’un écran et la déposer sur un autre comme on déplace un instrument sur une grande table.

Pas comme on expédie un fichier.

Pas comme on fabrique une copie.

Comme on transporte un objet.

---

Il ouvrit un module presque vide.

Un rectangle noir.

Un titre.

Quelques données de test.

Rien d’important.

C’était volontaire.

Avant de transporter un moteur, une expérience ou une formule, mieux valait transporter quelque chose dont la perte ne coûtait rien.

Brutus plaça le module près du bord droit du premier écran.

Il le saisit.

Puis commença à avancer.

Le curseur atteignit la frontière.

Passa.

La fenêtre, elle, hésita.

---

Une fraction de seconde.

Pas davantage.

Mais Brutus la vit.

Le curseur était déjà ailleurs.

La fenêtre était encore ici.

Puis elle sauta.

Pas de manière catastrophique.

Elle finit bien par apparaître sur le deuxième écran.

Pour un utilisateur ordinaire, l’expérience aurait peut-être été acceptable.

Pour Brutus, elle ne l’était pas.

Parce qu’entre les deux états, il existait un instant où personne ne pouvait répondre proprement à la question :

**où est la fenêtre ?**

---

Brutus lâcha la souris.

Le panneau s’immobilisa.

Il nota :

**FRONTIÈRE NON CONTINUE.**

Puis il ajouta :

**CURSEUR ≠ OBJET.**

Encore une séparation.

Encore une chose qui pouvait sembler évidente après coup.

Le mouvement du pointeur ne prouvait pas le mouvement de la fenêtre.

---

Brutus retourna dans le code.

Chaque écran possédait sa propre structure.

Chaque fenêtre était rendue dans un contexte particulier.

Lorsqu’un déplacement quittait un contexte pour un autre, plusieurs mécanismes se mettaient à intervenir en même temps.

Le navigateur.

Le système de coordonnées.

La fenêtre physique.

Le cadre interne.

Les événements de pointeur.

Le cache.

Le stockage.

Le rendu.

Le navigateur pouvait savoir que la souris avait traversé.

Cela ne signifiait pas que l’application savait précisément quoi faire de l’objet transporté.

---

Brutus dessina une petite chaîne :

**POINTER DOWN**

↓

**OBJECT ARMED**

↓

**SOURCE SCREEN**

↓

**CROSSING**

↓

**TARGET SCREEN**

↓

**DROP**

↓

**STATE UPDATE**

↓

**RENDER**

Il observa les étapes.

Il manquait quelque chose.

Entre le début et la fin, il fallait conserver un paquet minimal de vérité.

Pas tout le module.

Pas toute l’interface.

Seulement ce qui permettait de dire :

**c’est bien cet objet-là qui est en train d’être déplacé.**

---

Il ajouta :

**WINDOW_ID**

**SOURCE_SCREEN**

**START_POSITION**

**CURRENT_POINTER**

**TARGET_SCREEN**

**DROP_POSITION**

**TRANSFER_STATE**

Voilà.

Le bureau avait besoin d’un contrat de déplacement.

---

Cette idée plut à Brutus.

Un simple geste de souris devenait une transaction.

L’objet devait être armé.

Transporté.

Reçu.

Puis confirmé.

La destination ne devait pas inventer un nouveau module.

Elle devait accepter celui qui était déjà en mouvement.

---

Il recommença.

Cette fois, lorsqu’il appuya sur la fenêtre, l’événement ne signifiait pas seulement :

**la souris est enfoncée.**

Il signifiait :

**WINDOW-TEST-01 entre en état de transport.**

Les autres écrans furent avertis.

Pas de manière bruyante.

Juste suffisamment pour savoir qu’un objet pouvait arriver.

Les surfaces de destination activèrent leurs zones de dépôt.

---

Brutus glissa la fenêtre.

Premier écran.

Frontière.

Deuxième écran.

La fenêtre passa.

Plus proprement.

Mais un autre problème apparut.

La position n’était pas exactement celle attendue.

Le module sautait de quelques pixels.

Brutus regarda les coordonnées.

Il sourit presque immédiatement.

Le piège classique.

Chaque écran croyait que son coin supérieur gauche était le début du monde.

---

Pour le premier écran :

\[
(0,0)
\]

Pour le deuxième :

\[
(0,0)
\]

Pour le troisième :

\[
(0,0)
\]

Cinq petits univers ayant chacun leur origine.

Impossible de créer un territoire continu ainsi.

Il fallait un espace global.

---

Brutus prit une feuille.

Il dessina les cinq écrans.

Puis plaça une origine unique.

Le premier écran commencerait à une certaine coordonnée globale.

Le deuxième ailleurs.

Le troisième ailleurs encore.

Chaque position locale pourrait être transformée en position globale.

Puis reconvertie dans le système local de la destination.

---

Il écrivit :

\[
P_{\text{global}}
=
P_{\text{screen}}
+
P_{\text{local}}
\]

Puis :

\[
P_{\text{local,target}}
=
P_{\text{global}}
-
P_{\text{target}}
\]

Simple.

Presque banal.

Mais cette transformation changeait le laboratoire.

Les cinq écrans obtenaient enfin une géographie commune.

---

Brutus recommença.

Fenêtre saisie.

Passage.

Dépôt.

Cette fois, aucun saut visible.

Il la ramena.

Puis recommença dans l’autre sens.

Puis du premier au troisième.

Du troisième au cinquième.

Du cinquième au deuxième.

Encore.

Encore.

Encore.

La fenêtre voyageait.

---

Brutus aurait pu s’arrêter là.

Il ne le fit pas.

Parce qu’il connaissait maintenant le danger des démonstrations trop faciles.

Un objet qui traverse une fois ne prouve pas qu’un système de transport existe.

Cela prouve seulement qu’un objet a traversé une fois.

---

Il en ouvrit dix.

Les plaça sur plusieurs écrans.

Les déplaça rapidement.

En ferma deux.

En replia une.

Déplaça une fenêtre pendant qu’une autre changeait d’état.

Puis rechargea le laboratoire.

Certaines choses revinrent correctement.

D’autres non.

Une fenêtre se retrouva sur le mauvais écran.

Une autre conserva la bonne position mais pas le bon état d’ouverture.

Une troisième revint deux fois.

Brutus fronça les sourcils.

---

Deux fois.

Voilà un problème sérieux.

Pas pour une fenêtre.

Pour ce que cela représentait.

Si le même objet pouvait apparaître simultanément à deux endroits, le laboratoire n’avait plus une identité.

Il avait une duplication.

---

Brutus écrivit en gros :

**ONE ID = ONE CANONICAL INSTANCE.**

Puis en dessous :

**VISIBLE COPIES ARE NOT ALLOWED TO BECOME AUTHORITIES.**

Une vue pouvait être dupliquée un jour.

Peut-être.

Mais jamais l’identité de contrôle.

---

Il chercha la source.

Lorsqu’un transfert se produisait au moment où un état ancien était restauré, deux chemins différents pouvaient tenter de rendre le même module.

Le problème n’était pas dans le déplacement.

Il était dans la concurrence entre deux sources d’état.

Le nouveau monde.

Et le souvenir de l’ancien.

---

Brutus coupa l’une des autorités.

Il choisit un état canonique.

Un seul.

Les écrans ne posséderaient plus chacun leur vérité.

Ils liraient la vérité commune.

---

**GLOBAL WINDOW STORE.**

Le mot réapparut.

Mais maintenant, il prenait tout son sens.

Ce n’était pas seulement un endroit où mémoriser les positions.

C’était l’autorité du bureau.

Chaque écran devenait une projection du même état.

---

Le module possédait un identifiant.

Le store possédait sa position.

Son écran courant.

Sa taille.

Son état ouvert ou fermé.

Son niveau de zoom.

Son état réduit.

Et chaque fenêtre physique devait simplement refléter cette information.

---

Brutus exécuta un nouveau test.

Il déplaça une fenêtre.

Le store changea.

Les écrans reçurent le nouvel état.

La source cessa de rendre l’objet.

La destination le rendit.

Une seule instance.

---

Il rechargea.

L’objet revint au bon endroit.

Il ferma.

Rechargea.

Il resta fermé.

Il rouvrit depuis MODULE.

L’objet réapparut sur le dernier écran connu.

---

Brutus hocha lentement la tête.

Cette fois, le laboratoire ne se contentait plus de bouger.

Il se souvenait de ce que le mouvement voulait dire.

---

Puis vint une nouvelle complication.

Les iframes.

Certaines zones du laboratoire vivaient dans des cadres séparés.

Des mondes à l’intérieur du monde.

Le pointeur pouvait entrer dans un cadre, mais certains événements ne traversaient pas naturellement la frontière.

Le transport se coupait.

---

Brutus fixa longtemps ce problème.

Encore une frontière.

Encore un endroit où le monde extérieur et le monde intérieur n’utilisaient pas le même langage.

Il fallait un pont.

---

Pas un hack.

Pas une simulation.

Un protocole.

Le cadre devait pouvoir annoncer :

**un objet arrive.**

Ou :

**un objet repart.**

Le parent devait pouvoir transmettre l’identité.

Le cadre devait confirmer qu’il pouvait devenir destination.

---

Brutus construisit un petit relais de messages.

Un objet de transport minimal.

L’identifiant.

La position.

Le type de mouvement.

La source.

La destination.

Rien d’autre.

Pas de contenu arbitraire.

Pas de code.

Pas de contrôle caché.

---

Lorsqu’un déplacement commençait, les cibles étaient armées.

Lorsqu’il entrait dans un cadre, le cadre recevait l’information.

Lorsqu’il sortait, l’état repassait au parent.

Puis au nouvel écran.

---

Le système fonctionna.

Pas parfaitement.

Mais suffisamment pour que Brutus sente quelque chose changer.

Il ne manipulait plus cinq écrans.

Il manipulait réellement un espace.

---

Il prit le module et le lança presque volontairement à travers plusieurs frontières.

Premier écran.

Deuxième.

Troisième.

Quatrième.

Cinquième.

Puis retour.

Il observa non pas la fenêtre, mais les traces.

À chaque déplacement :

**WINDOW_ID**

**FROM**

**TO**

**POSITION BEFORE**

**POSITION AFTER**

**TIMESTAMP**

**STATE**

C’était peut-être excessif.

Mais Brutus aimait cela.

Parce que le bureau commençait à devenir vérifiable.

---

Puis il eut envie de pousser davantage.

Il ouvrit deux fenêtres simultanément.

Déplaça la première.

Puis rapidement la seconde.

Le système accepta.

Troisième.

Quatrième.

Le bureau resta stable.

---

Brutus ajouta une autre contrainte.

Une fenêtre en cours de transfert ne pouvait pas commencer un deuxième transfert.

Encore une règle d’identité.

Encore une protection contre la duplication.

---

Il écrivit :

**MOVING = LOCKED FOR SECOND TRANSFER.**

Cette phrase lui rappela immédiatement quelque chose.

Un objet en mouvement ne devrait probablement jamais recevoir deux autorisations incompatibles.

Il pensa aux routes.

Aux fourmis.

Aux futurs transports.

Puis chassa encore l’idée.

Pas encore.

---

Mais cette fois, elle revint.

Le laboratoire lui montrait peut-être un principe général.

Pour déplacer n’importe quoi proprement, il fallait connaître :

ce qui partait,

d’où,

vers où,

avec quelle identité,

sous quelle autorité,

et quand le déplacement était réellement terminé.

---

Brutus regarda la fenêtre qui venait de traverser l’écran.

Elle semblait banale.

Un rectangle.

Mais elle venait de lui apprendre un langage.

---

Il écrivit dans un coin :

**SOURCE**

**OBJECT**

**ROUTE**

**DESTINATION**

**ACK**

Puis hésita.

Il raya **ACK**.

À la place :

**OBSERVED ARRIVAL.**

Il sourit.

Cela semblait peut-être trop strict pour une fenêtre.

Mais la distinction lui plaisait.

La destination pouvait dire :

**j’ai accepté le dépôt.**

Ce n’était pas exactement la même chose que :

**l’objet est maintenant correctement présent ici.**

---

Le Gauntlet vivait toujours en lui.

Il transformait les petits détails en frontières de confiance.

---

Le soir approchait.

Le bureau avait maintenant traversé des dizaines de fois les cinq écrans.

Brutus décida de faire un test final.

Il ferma toutes les fenêtres.

Sauvegarda l’état.

Puis quitta complètement le laboratoire.

Silence.

Écrans noirs.

---

Quelques secondes plus tard, il relança.

Le moteur revint au centre.

MODULE revint.

La disposition générale fut restaurée.

Brutus ouvrit une première fenêtre.

Elle apparut là où elle avait été laissée.

Deuxième.

Même chose.

Troisième.

Encore.

---

Il prit la troisième.

La déplaça vers le cinquième écran.

Ferma le laboratoire.

Relança.

La troisième revint sur le cinquième.

---

Brutus ne dit rien.

Mais il savait qu’une petite victoire venait d’avoir lieu.

La salle possédait désormais une mémoire qui survivait à son propre arrêt.

---

Cela changeait beaucoup de choses.

Car jusque-là, les écrans n’étaient qu’une extension de l’instant présent.

Maintenant, ils pouvaient conserver une organisation entre deux sessions.

Le territoire devenait persistant.

---

Brutus ouvrit un document vide.

Il écrivit :

**LE BUREAU A UNE MÉMOIRE.**

Puis :

**LES OBJETS ONT UNE IDENTITÉ.**

Puis :

**LES FRONTIÈRES SONT TRAVERSABLES.**

Puis :

**LA SOURCE DE VÉRITÉ EST UNIQUE.**

Il regarda les quatre phrases.

Ce n’était plus simplement une interface graphique.

C’était déjà une architecture.

---

Le cinquième écran attira son regard.

Un module y reposait seul.

Brutus pensa à toutes les choses qu’il pourrait bientôt y envoyer.

Des données.

Des fréquences.

Des formules.

Des traces.

Des événements.

Peut-être un jour des décisions.

---

Puis il pensa à quelque chose d’encore plus étrange.

Si une fenêtre pouvait voyager sans perdre son identité…

Pourquoi pas autre chose ?

---

La question resta suspendue.

Il ne voulait pas encore y répondre.

Mais le laboratoire venait de lui montrer qu’une frontière visuelle pouvait être franchie proprement lorsqu’on séparait l’identité, l’état, la position et l’autorité.

Cela ressemblait terriblement à un problème qu’il allait rencontrer ailleurs.

---

Brutus retourna au premier écran.

Au centre, le moteur attendait toujours.

Il avait été là pendant tout le test.

Stable.

Immobile.

Comme s’il observait les autres objets apprendre à se déplacer autour de lui.

---

Brutus approcha la souris.

Cette fois, il ne toucha pas au moteur.

Il le regarda simplement.

Le laboratoire savait maintenant transporter ses fenêtres.

Mais son centre, lui, ne faisait encore rien.

Il avait une position.

Une présence.

Peut-être une autorité future.

Mais pas encore de vie.

---

Brutus écrivit une dernière phrase avant de quitter la salle :

**LE BUREAU SAIT SE DÉPLACER.**

Puis, juste en dessous :

**MAINTENANT, IL FAUT FAIRE TOURNER LE CENTRE.**

Il sauvegarda.

Ferma le fichier.

Les cinq écrans restèrent allumés.

Et au milieu du premier, le moteur attendait toujours.

Cette fois, Brutus savait exactement ce qu’il allait faire avec lui.

Le lendemain, le laboratoire n’apprendrait plus seulement à déplacer ses outils.

**Il apprendrait à tourner.**
