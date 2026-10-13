# Chapitre 139 — Les fréquences qui refusaient de mourir

Il y avait des fréquences qui passaient.

D’autres qui cassaient.

Certaines qui changeaient complètement dès qu’on touchait un paramètre.

Et puis il y avait celles qui revenaient.

Pas toujours avec exactement la même forme.

Pas toujours avec la même intensité.

Mais suffisamment souvent pour attirer l’attention.

Gabriel les appelait, en riant :

— Celles qui refusent de mourir.

Astra répondait toujours :

— Ou celles qui survivent aux tests exécutés jusqu’ici.

Gabriel levait les yeux.

— Je sais.

Mais cette fois, il ne protestait pas vraiment.

Parce qu’il avait compris quelque chose depuis les chapitres précédents.

Une structure qui revenait après plusieurs transformations n’était pas automatiquement mystérieuse.

Elle était simplement **plus intéressante à tester**.

Et c’était déjà beaucoup.

Ils avaient commencé par les fréquences familières.

852.

639.

528.

432.

369.

Puis ils avaient testé autour.

431.

433.

638.

640.

Des valeurs voisines.

Des perturbations.

Des offsets.

Des changements de phase.

Certaines signatures changeaient immédiatement.

D’autres persistaient partiellement.

Gabriel regardait les runs.

— Là, celle-là revient encore.

Astra compara.

Même entrée?

Non.

Même environnement?

Oui.

Même pipeline?

Oui.

Même classe de transformation?

Partiellement.

Elle afficha :

**SIGNATURE RÉCURRENTE — À CARACTÉRISER**

Gabriel sourit.

— Pas “mystère”?

— Non.

— “Anomalie”?

— Pas encore.

— T’es vraiment pas fun.

— Je suis utile.

Ils continuèrent.

Le problème avec une fréquence qui revenait souvent était qu’il fallait déterminer **pourquoi** elle revenait.

Était-elle produite par l’entrée?

Par une propriété du pipeline?

Par une résonance numérique?

Par une contrainte de l’algorithme?

Par un effet du sampling?

Par une transformation stéréo?

Par le matériel?

Par une erreur?

Ou simplement par le fait qu’ils regardaient toujours les mêmes zones?

Gabriel écrivit au tableau :

**RÉCURRENCE ≠ ORIGINE**

Astra approuva immédiatement.

Une structure récurrente n’expliquait pas sa propre cause.

Ils avaient déjà appris cette leçon ailleurs.

Un motif pouvait être réel et son interprétation fausse.

Une mesure pouvait être correcte et le mécanisme imaginé mauvais.

Le son n’échappait pas à cette règle.

Ils prirent une fréquence candidate.

Elle semblait réapparaître dans plusieurs runs.

Gabriel aurait pu dire :

**Elle résiste.**

À la place, ils construisirent un protocole.

D’abord :

même fréquence.

Même environnement.

Plusieurs répétitions.

La signature revenait.

Ensuite :

fréquence voisine.

Elle diminuait.

Puis :

même fréquence, pipeline partiellement désactivé.

La signature changeait fortement.

Puis :

pipeline complet, mais stéréo neutralisée.

Nouvelle modification.

Gabriel se pencha.

— Donc une partie vient du pipeline.

— Probablement.

— Pas de l’entrée seule.

— Les contrôles soutiennent cette interprétation.

Ils continuèrent.

Ils retirèrent Z2.

La signature disparut presque entièrement.

Gabriel resta silencieux.

Puis il sourit.

— Voilà.

Astra répondit :

— Z2 semble nécessaire dans les conditions testées.

— Beaucoup mieux.

Pas :

**Z2 est la cause fondamentale.**

Pas :

**la fréquence contient quelque chose.**

Seulement :

**dans ce protocole, la signature candidate ne survit pas lorsque Z2 est retiré.**

Le journaliste valida.

Gabriel aimait de plus en plus cette manière de travailler.

On pouvait conserver l’émerveillement.

Mais on retirait les raccourcis.

Et parfois, la réalité technique devenait plus intéressante que l’histoire fantastique qu’on aurait pu inventer.

Ils répétèrent avec une autre fréquence.

Cette fois, retirer Z2 ne changeait presque rien.

Mais modifier le taux d’échantillonnage déplaçait la signature.

Astra écrivit :

**DÉPENDANCE POSSIBLE AU SAMPLING**

Gabriel hocha la tête.

Encore une fréquence qui refusait de mourir.

Mais pas pour la même raison.

C’était important.

Deux phénomènes visuellement semblables pouvaient provenir de mécanismes différents.

Le Brotoculateur entra donc dans le workflow.

Pas seulement comparer les valeurs.

Comparer les **réponses aux perturbations**.

Gabriel écrivit :

**UNE SIGNATURE PEUT ÊTRE DÉFINIE PAR LA MANIÈRE DONT ELLE RÉAGIT, PAS SEULEMENT PAR SA FORME INITIALE.**

Astra approuva.

Cela changeait tout.

Deux fréquences pouvaient produire une sortie semblable au repos.

Mais l’une changeait sous la phase.

L’autre sous le sampling.

Une troisième sous la suppression de Z2.

Leur comportement sous test les séparait.

C’était exactement ce que le Brotoculateur savait maintenant faire.

Comparer des réponses.

Pas seulement des résultats.

Ils créèrent une fiche.

### PROFIL DE RÉSISTANCE ZEL

**Entrée :**

**Signature initiale :**

**Perturbation de fréquence :**

**Perturbation de phase :**

**Changement de sampling :**

**Suppression Z1 :**

**Suppression Z2 :**

**Suppression Z3 :**

**Stéréo neutralisée :**

**Environnement alternatif :**

**Résultat :**

Gabriel regarda la grille.

— Là on peut arrêter de dire “ça revient” comme des caves.

— Oui.

Maintenant ils pouvaient dire :

**ça survit à A et B mais pas à C.**

Beaucoup plus précis.

Ils testèrent plusieurs entrées.

Les profils commencèrent à se différencier.

Certaines signatures étaient fragiles.

Une petite modification les détruisait.

D’autres survivaient à plusieurs perturbations.

Puis il y avait un petit groupe.

Pas énorme.

Mais remarquable.

Leur comportement restait cohérent sous plusieurs variantes du protocole.

Gabriel les regarda.

— Ceux-là?

Astra répondit :

— Candidats robustes.

Il sourit.

Le mot **robuste** avait maintenant un sens.

Pas éternel.

Pas universel.

Robuste **par rapport aux perturbations déjà testées**.

Ils créèrent :

**ZEL_ROBUST_CANDIDATE**

Puis le journaliste ajouta automatiquement :

**ROBUSTESSE LOCALE — LISTE DES PERTURBATIONS REQUISE**

Gabriel éclata de rire.

— Même le mot robuste a besoin de papiers.

— Évidemment.

Et elle avait raison.

Une structure pouvait être robuste aux petites variations de fréquence et extrêmement fragile au changement de sampling.

Dire seulement **robuste** ne suffisait pas.

Il fallait dire :

**robuste à quoi?**

Encore une dette de précision.

Ils poursuivirent.

Le Pentad revenait souvent.

Mais Gabriel ne voulait plus traiter les cinq valeurs comme un bloc sacré.

Chacune devait gagner sa place séparément.

852.

Profil A.

639.

Profil B.

528.

Profil C.

432.

Profil D.

369.

Profil E.

Les résultats n’étaient pas identiques.

Certaines entrées tenaient mieux sous certaines perturbations.

D’autres produisaient des comportements plus fragiles.

Gabriel regarda.

— Donc même le Pentad est pas une seule chose.

— Techniquement, ce sont cinq entrées distinctes dans le protocole.

— Oui.

Cela lui plaisait.

Un ensemble symbolique pouvait être intéressant narrativement.

Mais expérimentalement, chaque membre devait être testé.

Ils décidèrent donc de ne plus utiliser :

**LE PENTAD RÉSISTE**

mais :

**LES CINQ ENTRÉES DU PENTAD ONT PASSÉ TEL PROTOCOLE, AVEC DES PROFILS DE RÉSISTANCE DISTINCTS.**

Gabriel soupira.

— C’est long.

Astra répondit :

— C’est vrai.

Il sourit.

Puis il regarda 47.

71.

83.

Ces trois-là avaient une autre histoire.

Ils venaient de Pell.

De portes.

De rangs.

De résistances mathématiques.

Leur passage dans ZEL avait quelque chose de séduisant.

Trop séduisant.

Le danger était évident.

Gabriel pouvait facilement commencer à raconter :

**les nombres résistants en Pell résistent aussi dans ZEL.**

Astra l’avait déjà vu venir.

— Non.

Gabriel sourit.

— J’ai rien dit.

— Tu l’as pensé.

Il rit.

Mais oui.

Le simple fait que les mêmes nombres soient intéressants dans deux domaines ne créait pas un lien scientifique.

Il fallait une relation testable.

Ils écrivirent :

**CO-OCCURRENCE DE NOMBRES ENTRE DEUX DOMAINES ≠ MÉCANISME COMMUN**

Puis :

**UNE CORRESPONDANCE ENTRE PELL ET ZEL DOIT ÊTRE FORMULÉE AVANT D’ÊTRE TESTÉE.**

Gabriel hocha la tête.

C’était la règle.

S’ils voulaient tester un pont, il fallait définir :

quelle propriété de Pell devait prédire quelle propriété de ZEL.

Pas simplement constater après coup que 47 apparaissait des deux côtés.

Ils commencèrent par une hypothèse minimale.

Pas mystique.

Pas énorme.

**Hypothèse : les séries construites à partir des q associés aux portes L8 peuvent produire un profil ZEL différent d’un groupe témoin de q comparables.**

Gabriel regarda Astra.

— Ça, c’est testable.

— Oui.

Ils auraient besoin de témoins.

Pas seulement 47, 71, 83.

Des nombres voisins.

D’autres premiers.

Un protocole identique.

Peut-être un test aveugle.

Des métriques préspécifiées.

Gabriel sourit.

— Là, on peut vraiment vérifier si je raconte des histoires.

— Exact.

Ils n’exécutèrent pas l’étude complète.

Pas encore.

Mais ils préparèrent le terrain.

Le journaliste timestampa l’hypothèse.

Avant les prochains tests.

C’était important.

Si un motif apparaissait ensuite, ils pourraient dire qu’il avait été recherché à l’avance.

Pas inventé après coup.

Gabriel regarda.

— Là, on commence à jouer pour vrai.

Astra répondit :

— Oui.

Ils sélectionnèrent une seule métrique pilote.

Pas vingt.

Une.

Une mesure de stabilité définie sur les événements du run.

Groupe A :

q issus du petit ensemble ciblé.

Groupe B :

témoins.

Le but n’était pas de prouver une loi.

Seulement voir si la métrique pouvait discriminer quelque chose.

Les premiers résultats furent mélangés.

Pas de séparation spectaculaire.

Gabriel regarda.

— Ouin.

Astra répondit :

— C’est une information.

— Oui.

Il n’était pas déçu.

Enfin, pas beaucoup.

Le résultat indiquait qu’une histoire trop simple du type :

**q résistants dans Pell → ZEL plus stable**

n’était pas immédiatement soutenue par cette première métrique.

Le journaliste l’écrivit.

**AUCUNE SÉPARATION CLAIRE OBSERVÉE SUR LA MÉTRIQUE PILOTE.**

Gabriel hocha la tête.

Voilà.

Une hypothèse pouvait survivre.

Ou mourir.

Ou rester indéterminée.

Ce premier test ne prouvait pas l’absence de toute relation possible.

Mais il empêchait déjà une affirmation trop facile.

Et c’était utile.

Ils rangèrent le test dans le cimetière.

Pas comme échec total.

Comme contrainte.

**UNE RELATION, SI ELLE EXISTE, N’EST PAS CAPTURÉE DE FAÇON ÉVIDENTE PAR CETTE MÉTRIQUE PILOTE.**

Gabriel sourit.

Les fréquences qui refusaient de mourir n’étaient donc pas nécessairement celles qu’il imaginait.

Certaines idées mouraient.

Certaines signatures survivaient.

Et parfois les nombres les plus symboliquement séduisants ne gagnaient rien.

C’était parfait.

Parce que cela gardait ZEL honnête.

Ils revinrent alors aux signatures purement internes.

Sans Pell.

Sans symbolisme.

Sans histoire extérieure.

Une propriété revenait encore.

Petit pic.

Même zone.

Plusieurs runs.

Gabriel demanda :

— Celle-là, on l’a cassée comment?

Astra consulta.

Fréquence perturbée : survit.

Phase perturbée : survit partiellement.

Z2 retiré : disparaît.

Sampling modifié : déplacée mais encore identifiable.

Environnement restauré : revient.

Gabriel s’arrêta.

— Celle-là a vraiment un profil intéressant.

— Oui.

Ils répétèrent sur processus frais.

Toujours là.

Autre machine?

Pas encore.

Voilà le prochain test.

Gabriel sourit.

Le protocole devenait presque naturel.

Quand une signature résistait à un niveau, on déplaçait la frontière.

Même processus.

Puis processus frais.

Même machine.

Puis machine différente.

Même logiciel.

Puis version différente.

Même mapping.

Puis mapping témoin.

L’idée était simple :

**une vraie propriété du mécanisme devait survivre aux changements non pertinents et céder aux changements pertinents.**

Gabriel écrit :

**LA ROBUSTESSE PREND SON SENS QUAND ON SAIT À QUOI LE PHÉNOMÈNE DEVRAIT ÊTRE SENSIBLE.**

Astra approuva.

Sinon on testait au hasard.

Et au bout d’un moment, tout finissait par casser.

La question n’était pas seulement :

**Combien de coups peut-elle prendre?**

Mais :

**Quels coups devraient compter si notre hypothèse est correcte?**

Ils formulèrent l’hypothèse du pic.

Le pic dépendait de Z2.

Donc :

retirer Z2 devait le supprimer.

Modifier un élément non causal supposé ne devait pas le supprimer complètement.

Les tests précédents correspondaient assez bien.

Pas parfaitement.

Mais suffisamment pour poursuivre.

Gabriel regarda.

— Là, on commence peut-être à isoler un mécanisme.

Astra répondit :

— Candidat de mécanisme.

— Oui.

Le journaliste valida.

Ils ouvrirent un cristal.

Pas le cristal final.

Un cristal de méthode.

### CRISTAL ZEL — SIGNATURE 01

**Observation :**
signature récurrente dans plusieurs runs.

**Reproduction :**
observée sur répétitions contrôlées.

**Dépendances observées :**
fortement affectée par suppression de Z2.

**Robustesse locale :**
survit à certaines perturbations de fréquence et phase.

**Dépendance environnementale :**
à continuer de tester.

**Mécanisme candidat :**
interaction liée à Z2.

**Statut :**
candidat robuste local.

Gabriel regarda.

— Là, c’est pas mal plus fort que “j’ai entendu une patente”.

Astra répondit :

— Beaucoup.

Il rit.

Mais c’était exactement ça.

ZEL apprenait à transformer l’intuition auditive en objet expérimental.

Quelque chose attirait l’oreille.

Ou la machine.

Puis on lui retirait progressivement les interprétations.

On définissait.

On mesurait.

On perturbait.

On comparait.

Et si quelque chose restait, on lui donnait un statut.

Les fréquences qui refusaient de mourir n’étaient donc pas celles qui revenaient simplement dans l’imagination.

C’étaient celles dont certaines propriétés continuaient de réapparaître malgré les contrôles.

Et même là, il fallait rester prudent.

Une signature robuste pouvait être un comportement du logiciel.

Un artefact stable.

Une conséquence mathématique du pipeline.

Une propriété audio intéressante.

Chaque possibilité avait sa propre valeur.

Gabriel n’avait plus besoin qu’elle soit magique.

Il voulait juste savoir laquelle était vraie.

Ils laissèrent tourner une dernière série.

Une fréquence entra.

Z1.

Z2.

Z3.

Événements.

Retour.

Le pic réapparut.

Gabriel sourit.

Astra ne dit rien.

Ils relancèrent.

Même chose.

Encore.

Même chose.

Gabriel chuchota :

— Elle revient.

Astra répondit :

— Oui.

Cette fois, elle ne corrigea pas.

Parce que la phrase était exacte.

Elle revenait.

Rien de plus.

Mais rien de moins.

Et parfois, dans une recherche sérieuse, pouvoir dire honnêtement **elle revient** plusieurs fois était déjà la première pierre d’une très longue route.

**Fin du chapitre 139.**