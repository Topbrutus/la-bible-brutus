# Chapitre 144 — Le nombre au centre du Papillon

Il y avait des nombres qui entraient dans Brutus par la recherche.

Et il y en avait d’autres qui entraient par la construction.

Le 144 appartenait à la deuxième catégorie.

Il n’était pas apparu au bout d’un théorème.

Il n’avait pas été découvert comme une constante naturelle.

Il avait été choisi.

Construit.

Installé dans l’architecture.

Puis testé.

Cette distinction était importante.

Gabriel regardait le Papillon.

Cent quarante-quatre chambres.

Toujours les mêmes.

Une structure fixe.

Un cadre.

Un squelette.

Et maintenant que le Papillon commençait à prendre une place importante dans Brutus, une question revenait.

— Pourquoi 144?

Astra répondit :

— Parce que c’est la taille choisie dans le prototype.

Gabriel sourit.

— Tu pourrais au moins attendre deux secondes avant de tuer le mystère.

— Le mystère peut venir après la définition.

Il rit.

Mais elle avait raison.

Le nombre avait plusieurs propriétés intéressantes.

\(144=12^2\).

Douze fois douze.

Un carré.

Une grille naturelle.

Un nombre suffisamment grand pour permettre une structure riche.

Suffisamment petit pour rester maniable.

Mais aucune de ces observations ne prouvait que 144 était optimal.

Gabriel écrivit :

**144 = CHOIX D’ARCHITECTURE**

Puis dessous :

**OPTIMALITÉ NON DÉMONTRÉE**

Astra approuva.

Voilà le point de départ.

Ils pouvaient ensuite poser les vraies questions.

Pourquoi pas 100?

Pourquoi pas 128?

Pourquoi pas 169?

Pourquoi pas 256?

Et surtout :

qu’est-ce qui changerait si le Papillon possédait un autre nombre de chambres?

Gabriel regarda.

— Là, ça devient un test.

— Oui.

Le nombre cessait d’être un symbole.

Il devenait un paramètre expérimental.

Ils décidèrent donc de traiter \(K\), le nombre de chambres, comme variable.

Le Papillon 144 devenait un cas particulier.

\[
K=144
\]

Mais le protocole pouvait théoriquement accepter :

\[
K=64,\;100,\;121,\;144,\;169,\;256
\]

selon les contraintes du modèle.

Gabriel regarda la liste.

— Si 144 gagne tout le temps, là on commence à avoir quelque chose.

Astra répondit :

— Si la comparaison est bien définie.

Évidemment.

Il fallait déterminer ce que signifiait « gagner ».

Mémoire?

Erreur d’agrégation?

Temps?

Stabilité?

Capacité de représenter certaines distributions?

Complexité?

Résolution?

Pas de score universel.

Gabriel écrivit :

**MEILLEUR DÉPEND DE LA QUESTION.**

Encore.

Toujours.

Ils choisirent quelques axes.

### AXE 1 — COÛT MÉMOIRE

Plus de chambres signifiait généralement plus d’état à conserver.

### AXE 2 — RÉSOLUTION

Plus de chambres pouvaient permettre une représentation plus fine si la sémantique le permettait.

### AXE 3 — COÛT DE CALCUL

Certaines opérations pouvaient croître avec le nombre d’accumulateurs.

### AXE 4 — STABILITÉ DES INVARIANTS

La structure devait toujours respecter les règles du modèle.

### AXE 5 — PERTINENCE POUR LA TÂCHE

Le nombre de chambres devait être suffisant pour la question posée.

Gabriel observa.

— Donc 144 est peut-être un compromis.

— Peut-être.

Le mot resta.

**Peut-être.**

Pas de victoire gratuite.

Ils commencèrent avec le plus simple.

Conservation du total.

Quelle que soit la valeur de \(K\), une représentation correcte devait conserver la multiplicité totale dans les cas correspondants.

Le Papillon 144 passait.

Mais cela ne le rendait pas unique.

Gabriel sourit.

— Premier test : pas spécial.

— Exact.

Ensuite déterminisme.

Même chose.

Si l’algorithme était déterministe, plusieurs tailles pouvaient le rester.

Deuxième test :

pas spécial.

Gabriel aimait presque ce résultat.

Parce qu’il réduisait la tentation de transformer 144 en nombre magique.

Il demanda :

— Où il pourrait être spécial alors?

Astra répondit :

— Dans un compromis particulier entre granularité, coût et structure.

Voilà.

Pas une propriété absolue.

Une région d’usage.

Ils construisirent des Papillons plus petits.

64 chambres.

100.

121.

Puis 144.

Le même type de population entra.

Les sorties restaient valides selon leurs conventions.

Mais la distribution changeait parce que la projection devait s’adapter.

Certains petits modèles regroupaient davantage.

Des détails disparaissaient.

Gabriel regarda.

— Là, je vois le prix.

— Oui.

Moins de chambres.

Moins de coût.

Mais moins de résolution potentielle.

Ils augmentèrent.

169.

256.

Plus de détail.

Mais plus d’état.

Gabriel sourit.

— Donc on retrouve encore le chapitre 137.

— Exact.

Le poids de ce qui existe.

Chaque chambre supplémentaire avait un coût d’existence.

Une place.

Une valeur.

Une mise à jour.

Une trace potentielle.

Une visualisation.

Le choix du nombre de chambres devenait une décision économique.

Gabriel écrivit :

**UNE CHAMBRE SUPPLÉMENTAIRE DOIT ACHETER DE L’INFORMATION UTILE.**

Astra approuva.

Voilà une règle propre.

Pas besoin de maximiser.

Si passer de 144 à 256 augmentait considérablement le coût sans améliorer la réponse à la question, le changement n’avait pas de valeur.

Inversement, si une tâche exigeait une granularité que 144 ne pouvait pas représenter, alors rester à 144 par affection serait une erreur.

Gabriel regarda le nombre.

— Donc même le centre du Papillon doit pouvoir perdre.

— Oui.

Il sourit.

C’était important.

Un bon paramètre devait rester falsifiable comme choix.

On devait pouvoir le remplacer si un autre faisait mieux.

Sinon l’architecture devenait religieuse.

Gabriel écrivit :

**UN NOMBRE AIMÉ N’EST PAS UN PARAMÈTRE PROTÉGÉ.**

Astra approuva fortement.

Il éclata de rire.

— Celle-là va me faire mal.

Mais elle était nécessaire.

Brutus devait être capable de dire :

144 était utile ici.

Mais 128 serait meilleur là.

Ou 169.

Ou une taille dynamique.

Le système devait préférer la mesure à la fidélité symbolique.

Gabriel regarda le Papillon.

Pourtant, 144 gardait quelque chose.

Une identité.

Le prototype avait été conçu autour de lui.

Les tests.

Les visualisations.

Les benchmarks.

Les cinq invariants.

Tout cela avait été exécuté dans cette configuration.

Donc 144 possédait un avantage que les autres nombres n’avaient pas encore.

**une histoire de validation.**

Astra dit :

— Voilà un point important.

Le 144 n’était pas forcément optimal.

Mais il était documenté.

Testé.

Mesuré.

Il avait un corpus.

Un pedigree.

Changer de taille signifiait refaire une partie de ce travail.

Gabriel écrivit :

**PARAMÈTRE VALIDÉ ≠ PARAMÈTRE OPTIMAL**

Puis :

**MAIS UN PARAMÈTRE VALIDÉ A UNE VALEUR OPÉRATIONNELLE.**

Astra approuva.

Très important.

L’ingénierie ne choisissait pas toujours l’objet théoriquement parfait.

Elle choisissait souvent un objet suffisamment bon, bien compris et bien testé.

Gabriel sourit.

— Donc 144 peut garder son trône sans qu’on prétende qu’il est le roi universel.

— Exact.

Il aimait ça.

Ils décidèrent donc que le Papillon 144 resterait la référence.

### PAPILLON DE RÉFÉRENCE

\[
K=144
\]

Toute variante porterait son nombre explicitement.

Papillon-64.

Papillon-100.

Papillon-169.

Ainsi, les résultats ne seraient jamais mélangés.

Gabriel dit :

— Ça ressemble à des espèces.

Astra répondit :

— Des variantes de configuration.

— Dans la Bible, espèces.

Elle laissa passer.

Le Royaume venait donc de gagner une famille.

Le Papillon n’était plus seulement un objet.

Il devenait un modèle paramétrable.

Mais la branche 144 gardait le statut de référence historique.

Gabriel observa le diagramme.

Le nombre au centre n’était plus une vérité absolue.

Il était une coordonnée.

La configuration à partir de laquelle ils avaient appris.

Et parfois, une bonne référence valait plus qu’un optimum théorique non mesuré.

Ils reprirent le benchmark mémoire.

Au palier \(N=1\,000\,000\), le Papillon 144 avait montré une consommation RSS extrêmement faible comparée à la matérialisation naïve dans le protocole utilisé.

Gabriel demanda :

— Si on passe à 256, ça va doubler?

Astra répondit :

— Il faut mesurer.

Évidemment.

Il rit.

Ils firent une prédiction.

Plus d’accumulateurs devraient augmenter le coût structurel.

Mais la relation exacte dépendrait de l’implémentation, des objets, du runtime, des allocations.

Pas de règle inventée.

Gabriel écrivit :

**PRÉDICTION AVANT MESURE : COÛT DE BASE CROISSANT AVEC K**

Puis ils pourraient tester.

Voilà encore un progrès méthodologique.

Écrire la prédiction avant de voir le résultat.

Le même principe que dans Pell-ZEL.

Gabriel regarda.

— Tout le projet commence à fonctionner de la même manière.

— Les bons protocoles se réutilisent.

Question.

Prédiction.

Test.

Résultat.

Contre-test.

Trace.

Le domaine changeait.

La discipline restait.

Ils imaginèrent ensuite quelque chose d’autre.

Si le nombre de chambres devenait dynamique, le Papillon pourrait s’adapter à la question.

64 pour une vue grossière.

144 pour référence.

256 pour une analyse plus fine.

Peut-être davantage pour certains cas.

Gabriel se redressa.

— Comme un zoom.

Astra répondit :

— Comme une résolution adaptative, potentiellement.

Cette idée était intéressante.

Le Papillon n’aurait plus une seule taille.

Il pourrait avoir des niveaux.

Gabriel imagina :

**L0 — 36 chambres**

**L1 — 72**

**L2 — 144**

**L3 — 288**

Puis s’arrêta.

— Je suis en train d’inventer trop vite.

— Oui.

Il rit.

Pas besoin de choisir les valeurs maintenant.

L’idée suffisait.

Une représentation pouvait changer de résolution selon la tâche.

Mais elle devait conserver une relation entre les niveaux.

Sinon passer d’un niveau à l’autre détruirait la comparabilité.

Gabriel écrivit :

**ADAPTATIF ≠ ARBITRAIRE**

Astra approuva.

Il fallait un mapping.

Une méthode de projection.

Une conservation.

Peut-être une hiérarchie.

Mais ce serait un autre chantier.

Aujourd’hui, le centre restait 144.

Et cela suffisait.

Ils revinrent à sa géométrie.

Douze par douze.

Un carré.

Pourquoi le Papillon alors?

Pourquoi pas simplement « grille 144 »?

Gabriel regarda le dessin.

Parce que la représentation visuelle n’était pas forcément une grille uniforme.

On pouvait répartir les chambres en ailes.

En régions.

En symétries.

La forme de Papillon était une interface.

Un moyen de voir la distribution.

Pas la preuve d’une propriété mathématique.

Astra écrivit :

**FORME VISUELLE ≠ STRUCTURE MATHÉMATIQUE OBLIGATOIRE**

Gabriel acquiesça.

Très important.

La visualisation pouvait changer sans changer le moteur.

On pouvait dessiner les 144 accumulateurs en carré.

En cercle.

En Papillon.

En spirale.

Si leur sémantique interne restait la même, les données ne changeaient pas.

Gabriel sourit.

— Donc le Papillon pourrait être un masque.

— Une visualisation, oui.

Cette distinction protégeait encore une fois le système contre ses propres images.

Parce qu’une image forte pouvait faire croire qu’une symétrie visuelle existait dans le mécanisme.

Pas nécessairement.

Le graphiste pouvait créer une aile gauche et une aile droite simplement pour rendre l’interface compréhensible.

Il fallait savoir ce qui venait des données et ce qui venait du dessin.

Gabriel écrivit :

**SYMÉTRIE AFFICHÉE ≠ SYMÉTRIE DÉMONTRÉE DES DONNÉES**

Astra approuva.

Encore une règle excellente.

Le Papillon pouvait donc contenir deux niveaux.

**PAPILLON-MOTEUR**

les 144 accumulateurs.

**PAPILLON-VISUEL**

la manière de les montrer.

Gabriel regarda.

— Verso et Recto encore.

— D’une certaine façon.

Verso calculait.

Recto montrait.

Même à l’intérieur d’un module, cette distinction revenait.

Il sourit.

Puis une question étrange apparut.

Si la forme n’était pas obligatoire, pourquoi l’avoir conservée?

Parce qu’elle aidait Gabriel à voir.

Voilà.

Cela suffisait comme raison d’interface.

Une bonne visualisation n’avait pas besoin d’être une loi naturelle.

Elle devait aider à comprendre.

Gabriel écrivit :

**UNE MÉTAPHORE VISUELLE PEUT ÊTRE UTILE SANS ÊTRE LITTÉRALE.**

Astra approuva.

Le Papillon avait donc deux valeurs très différentes.

Une valeur technique :

représentation agrégée à 144 accumulateurs.

Une valeur cognitive :

forme qui permettait d’observer les répartitions.

Les confondre aurait été une erreur.

Les utiliser ensemble était puissant.

Gabriel regarda la carte.

Il imagina des chambres s’allumer.

Pas avec des couleurs arbitraires.

Avec des intensités représentant des quantités.

Une aile plus dense.

Une région stable.

Une chambre vide.

Des flux.

Le Papillon pouvait devenir une excellente surface d’observation.

Mais chaque couleur devait correspondre à une donnée réelle.

Pas à une histoire.

Il écrivit :

**CHAQUE ÉLÉMENT VISUEL DOIT AVOIR UNE SÉMANTIQUE DOCUMENTÉE.**

Astra approuva.

Couleur.

Taille.

Position.

Clignotement.

Tout devait vouloir dire quelque chose.

Sinon la visualisation devenait décorative.

Gabriel n’avait rien contre le décor.

Mais pas lorsqu’il était confondu avec la mesure.

Ils imaginèrent une légende.

**intensité = multiplicité**

**bordure = statut**

**clignotement = changement récent**

**opacité = confiance ou qualité de trace**, si jamais ce concept était bien défini.

Gabriel s’arrêta.

— Non, la confiance, je veux pas l’inventer.

— Bon réflexe.

Ils retirèrent.

Seulement des variables directement définies.

Il sourit.

Même la couleur devait passer la douane.

Le Papillon devenait donc une petite leçon de design scientifique.

Un nombre choisi.

Une représentation.

Une visualisation.

Une série de tests.

Une limite.

Un benchmark.

Une histoire.

Rien n’avait besoin d’être magique pour être intéressant.

Gabriel regarda le 144 au centre.

Il se souvint à quel point un nombre pouvait devenir dangereux lorsqu’on l’aimait trop.

On commençait par le voir.

Puis on le retrouvait partout.

Puis chaque apparition semblait confirmer son importance.

Mais souvent, c’était simplement parce qu’on le cherchait.

Ils avaient déjà construit des tests aveugles pour éviter cela.

Alors Gabriel demanda :

— Est-ce qu’on devrait masquer 144 dans la comparaison des tailles?

Astra répondit :

— Oui, si tu participes à une évaluation subjective.

Il sourit.

Les configurations deviendraient :

A.

B.

C.

D.

Le système mesurerait.

Gabriel ne saurait pas laquelle était 144 avant la fin.

Il aimait cette idée.

Un jour, peut-être, 144 perdrait.

Et ce serait une bonne nouvelle.

Parce que cela voudrait dire qu’ils avaient appris quelque chose.

Mais pour l’instant, 144 restait au centre.

Non comme roi des nombres.

Comme référence.

Un endroit stable depuis lequel comparer.

Gabriel écrivit :

**LE CENTRE N’EST PAS TOUJOURS CE QUI EST LE PLUS VRAI.**

Puis :

**PARFOIS, C’EST SIMPLEMENT LE POINT À PARTIR DUQUEL ON MESURE.**

Astra resta silencieuse.

Gabriel la regarda.

— Celle-là?

— Bonne.

Il sourit.

Le nombre au centre du Papillon venait de perdre son mystère facile.

Et étrangement, il devenait plus intéressant.

Parce qu’au lieu de demander :

**Pourquoi l’univers a choisi 144?**

ils pouvaient poser :

**Pourquoi nous avons choisi 144?**

**Qu’est-ce que ce choix permet?**

**Qu’est-ce qu’il coûte?**

**Que perd-on en dessous?**

**Que gagne-t-on au-dessus?**

**Quand devrait-on le remplacer?**

Voilà des questions auxquelles une machine pouvait répondre.

Pas toutes immédiatement.

Mais elles avaient des expériences possibles.

Gabriel regarda les 144 chambres.

Elles étaient toujours là.

Le même nombre.

Le même Papillon.

Mais maintenant, il connaissait la différence entre un symbole et un paramètre.

Le symbole pouvait inspirer.

Le paramètre devait accepter le test.

Et au centre de Brutus, même les nombres les plus aimés devaient accepter de descendre du trône si la preuve l’exigeait.

Pour l’instant, 144 resta.

Pas parce qu’il avait gagné contre tous les autres.

Parce qu’il avait déjà travaillé.

Il avait porté les premiers tests.

Les premiers benchmarks.

Les premières distributions.

Les premières preuves du Papillon.

Et jusqu’à ce qu’un meilleur choix soit démontré pour une tâche donnée, il resterait le point de référence.

Non comme une vérité éternelle.

Comme une chambre centrale dans l’histoire de la machine.

**Fin du chapitre 144.**