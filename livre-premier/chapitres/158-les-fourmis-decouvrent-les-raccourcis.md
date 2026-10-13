# Chapitre 158 — Les Fourmis découvrent les raccourcis

Les Fourmis avaient appris à ne pas recommencer.

Elles savaient maintenant regarder derrière elles.

Voir les traces.

Reconnaître une impasse.

Éviter un doublon.

Réutiliser un résultat encore valide.

Rejouer un test lorsque le contexte l’exigeait.

Mais une nouvelle question apparut presque immédiatement.

Si plusieurs chemins menaient au même endroit,

et si certains avaient déjà été comparés,

alors pourquoi toujours prendre le chemin complet?

Gabriel regarda la carte.

— On peut couper.

Astra répondit :

— Peut-être.

Le mot était important.

Un raccourci pouvait être utile.

Ou catastrophique.

Tout dépendait de ce qu’on supprimait.

Un détour inutile?

Très bien.

Un contrôle critique?

Non.

Ils avaient déjà appris :

**OPTIMISER UN WORKFLOW ≠ RETIRER SES CONTRÔLES**

Cette règle devenait maintenant centrale.

Parce que les Fourmis commençaient à observer quelque chose.

Dans plusieurs workflows, certaines étapes produisaient toujours le même résultat lorsque certaines conditions étaient déjà satisfaites.

Exemple simple.

Un candidat arrivait avec une provenance complète.

Le workflow standard contenait une étape :

**vérifier présence de provenance**

Évidemment, cette étape restait rapide.

Mais elle illustrait un principe.

Si une condition avait déjà été démontrée par une trace fiable et applicable, fallait-il refaire tout le travail?

Gabriel écrivit :

**RACCOURCI = RÉUTILISATION D’UNE ÉTAPE DÉJÀ ÉTABLIE SOUS CONDITIONS COMPATIBLES**

Astra approuva.

Pas suppression gratuite.

Réutilisation justifiée.

Ils prirent un cas plus intéressant.

Un workflow de validation avait six étapes.

A.

B.

C.

D.

E.

F.

L’historique montrait que lorsque A produisait un certain certificat fort, B et C ne changeaient jamais la décision finale, parce qu’elles vérifiaient des propriétés déjà incluses dans A.

Gabriel regarda.

— Donc B et C sont redondantes?

Astra répondit :

— Dans ce sous-contexte précis, peut-être.

Encore.

Il fallait le prouver.

Ils ne retirèrent rien.

Ils construisirent une expérience.

Deux versions du workflow.

### COMPLET

A → B → C → D → E → F

### CANDIDAT RACCOURCI

A → D → E → F

Seulement lorsque le certificat A possédait les propriétés définies.

Ils rejouèrent des cas historiques.

Même décision finale.

Même provenance essentielle.

Coût inférieur.

Gabriel sourit.

— Bon.

Astra répondit :

— Backtest.

Il soupira.

Bien sûr.

Ils testèrent ensuite sur de nouveaux cas.

Toujours sous les conditions exactes.

Même résultat.

Puis un cas apparut où le certificat A était légèrement différent.

Le raccourci ne s’activa pas.

Le workflow complet fut exécuté.

Gabriel regarda.

— Là, j’aime ça.

Parce que le raccourci n’était pas une nouvelle route universelle.

C’était une condition.

**SI certificat A de type X est valide, alors B et C peuvent être omis parce que leur information est déjà couverte.**

Gabriel écrivit :

**RACCOURCI = THÉORÈME OU RÈGLE CONDITIONNELLE SUR LE WORKFLOW**

Astra approuva.

Parfois théorique.

Parfois empirique.

Très important de distinguer.

Si B et C étaient logiquement impliquées par A, le raccourci pouvait avoir une justification forte.

Si elles étaient seulement « presque toujours inutiles » historiquement, le statut était différent.

Gabriel créa deux classes.

### RACCOURCI PROUVÉ

Une condition garantit que l’étape retirée n’apporte aucune information nécessaire supplémentaire selon le protocole.

### RACCOURCI EMPIRIQUE

Historique favorable, mais possibilité résiduelle d’apport; utilisation limitée ou surveillée.

Astra approuva.

Voilà qui évitait de transformer une optimisation observée en équivalence logique.

Gabriel sourit.

— Même les raccourcis ont un niveau de preuve.

— Évidemment.

Ils regardèrent les Fourmis.

Une Fourmi pouvait maintenant recevoir une tâche.

Avant :

suivre le workflow standard.

Maintenant :

vérifier d’abord si un raccourci certifié s’appliquait.

Gabriel écrivit :

**STANDARD PATH FIRST, SHORTCUT ONLY WITH EVIDENCE**

Puis traduisit pour la Bible :

**LE CHEMIN COURT DOIT PROUVER QU’IL A LE DROIT D’ÊTRE COURT.**

Astra approuva.

Il adorait cette phrase.

Parce qu’un raccourci semblait toujours séduisant.

Moins de temps.

Moins de calcul.

Moins de stockage.

Mais la vitesse n’était pas la seule valeur.

Un raccourci devait préserver ce qui comptait.

Résultat.

Preuve.

Provenance.

Contrôle.

Gabriel écrivit :

### CONTRAT DU RACCOURCI

Le raccourci doit préserver :

**la propriété recherchée**

**les contrôles nécessaires**

**la provenance requise**

**le statut final**

**la capacité d’audit**

Astra approuva.

Si l’une de ces choses disparaissait, ce n’était plus le même workflow.

C’était une autre méthode.

Peut-être bonne.

Mais pas un raccourci équivalent.

Cette distinction était importante.

Gabriel dit :

— Donc si je coupe trois étapes et que je change ce qu’on peut affirmer, j’ai pas optimisé. J’ai changé le protocole.

— Exact.

Ils écrivirent :

**PLUS COURT ≠ ÉQUIVALENT**

Voilà.

Puis les Fourmis découvrirent un deuxième type de raccourci.

Pas à l’intérieur d’un workflow.

Entre deux workflows.

Un résultat existant avait déjà été calculé par un autre chemin.

Exemple :

une étape du Brotoculateur demandait une propriété que Pell avait déjà certifiée dans le dossier courant.

Fallait-il la recalculer?

Pas si les propriétés étaient vraiment équivalentes et les dépendances acceptables.

Gabriel se pencha.

— Là, les modules commencent à partager des preuves.

Astra répondit :

— Oui, avec prudence.

C’était puissant.

Et dangereux.

Un certificat produit pour une question ne devait pas être réutilisé pour une autre propriété simplement parce que les nombres ressemblaient.

Il fallait une correspondance explicite.

**proof_requirement**

contre

**proof_artifact**

Le système devait vérifier :

le certificat établit-il exactement ce que l’étape exige?

Gabriel écrivit :

**RÉUTILISER UNE PREUVE SEULEMENT SI SA PORTÉE COUVRE LA QUESTION ACTUELLE.**

Astra approuva.

Pas de :

« Pell a validé le nombre, donc tout est bon. »

Non.

Pell validait une propriété précise.

Le Brotoculateur pouvait demander autre chose.

La correspondance devait être formelle.

Ils appelèrent cela :

### RACCOURCI PAR CERTIFICAT

Une étape peut être satisfaite par un artefact de preuve déjà existant lorsque :

l’objet est le même,

la propriété demandée est couverte,

la version est compatible,

la provenance est valide,

aucune condition supplémentaire n’est nécessaire.

Gabriel sourit.

— Ça, ça peut sauver énormément.

Parce qu’un calcul difficile pouvait être réutilisé proprement.

Mais surtout :

la preuve devenait un objet portable.

Pas une phrase perdue dans un log.

Un artefact.

Avec un contrat.

Ils avaient déjà commencé cette idée avec les cristaux.

Maintenant, elle devenait opérationnelle.

Gabriel écrivit :

**UNE PREUVE BIEN FORMÉE PEUT DEVENIR UNE INFRASTRUCTURE.**

Astra approuva.

Très important.

Un témoin Pell n’était pas seulement une réponse.

Il pouvait servir de test de régression.

De validation croisée.

De référence.

De certificat réutilisable pour exactement les propriétés qu’il démontrait.

Le travail passé continuait à produire de la valeur.

Les Fourmis commencèrent donc à chercher non seulement :

**quel chemin a déjà été parcouru?**

Mais :

**quelles étapes ont déjà été payées?**

Gabriel sourit.

Voilà le vrai raccourci.

Pas couper sauvagement.

Réutiliser correctement ce qui avait déjà été établi.

Il écrivit :

**NE PAS RECALCULER UNE PREUVE ENCORE VALIDE SI LA MÊME PREUVE RÉPOND EXACTEMENT AU BESOIN.**

Astra approuva.

Puis ils rencontrèrent le troisième type.

Le raccourci par échec.

Cela semblait étrange.

Une étape avait déjà montré qu’une condition nécessaire était absente.

Le workflow complet n’avait donc plus besoin de continuer.

Gabriel regarda.

— Ah oui.

Un candidat devait passer cinq tests.

Le deuxième échouait sur une condition strictement nécessaire.

Pourquoi exécuter les trois suivants?

Pas besoin.

**FAIL FAST**

Gabriel rit.

— Celui-là, les programmeurs connaissent depuis longtemps.

Mais dans Brutus, il fallait encore distinguer :

condition nécessaire.

condition seulement indicative.

Si un test faible échouait, le candidat pouvait parfois survivre.

Si une condition nécessaire échouait, la route pouvait s’arrêter.

Gabriel écrivit :

### RACCOURCI NÉGATIF

**Condition nécessaire non satisfaite → arrêt du chemin**

Astra approuva.

Cela évitait énormément de calcul inutile.

Mais le certificat négatif devait être clair.

Pas :

**score trop faible.**

Plutôt :

**condition obligatoire X démontrée fausse.**

Encore la différence entre heuristique et preuve.

Les Fourmis apprenaient à courir moins loin lorsque la porte était déjà fermée.

Gabriel sourit.

— Elles deviennent bonnes.

Astra répondit :

— Elles deviennent mieux orchestrées.

Toujours.

Puis le quatrième type apparut.

Le raccourci par groupement.

Plusieurs tâches différentes demandaient une même étape coûteuse.

Au lieu de l’exécuter séparément, les Fourmis pouvaient partager le calcul.

Chapitre 157 avait déjà introduit le partage d’un travail actif.

Maintenant, ils allaient plus loin.

Avant même de lancer, la Reine pouvait voir :

dix tâches ont besoin de la même transformation.

Une seule exécution.

Dix consommateurs.

Gabriel écrit :

**BATCH COMMON WORK**

Puis :

**UNE FOIS POUR PLUSIEURS.**

Ils testèrent.

Dix candidats.

Tous nécessitaient la même table de référence.

Avant :

dix constructions.

Maintenant :

une construction versionnée.

Puis réutilisation.

Même résultat.

Moins de temps.

Moins d’I/O.

Moins de fichiers temporaires.

Gabriel sourit.

— Les Fourmis viennent d’apprendre à transporter une grosse roche ensemble.

Astra répondit :

— Oui.

La métaphore lui plaisait aussi, visiblement.

Ils appelèrent cela :

### RACCOURCI COLLECTIF

Identifier un sous-calcul commun à plusieurs tâches et le produire une seule fois lorsqu’il est déterministe et partageable.

Encore des conditions.

Déterministe.

Même paramètres.

Même version.

Même besoin.

Sinon :

pas de partage.

Gabriel écrivit :

**MÊME NOM D’ÉTAPE ≠ MÊME CALCUL SI LES PARAMÈTRES DIFFÈRENT.**

Astra approuva.

Évidemment.

Mais les bugs de cache naissaient exactement de ce genre de simplification.

Un cache incorrect pouvait renvoyer un résultat calculé pour une autre configuration.

Le raccourci devenait alors une source de corruption.

Il fallait donc une clé.

**computation_key**

Fonction de :

algorithme.

version.

paramètres.

entrée.

environnement si pertinent.

Gabriel sourit.

— Là, on arrive au cache sérieux.

Astra approuva.

Ils n’avaient pas besoin de stocker tous les résultats éternellement.

Mais les calculs chers et réutilisables pouvaient produire un artefact adressable.

Le réseau pouvait demander :

**ce calcul exact existe-t-il déjà?**

Si oui :

réutiliser.

Sinon :

calculer.

Le raccourci devenait presque mécanique.

Gabriel écrivit :

**IDENTITÉ DE CALCUL AVANT RÉUTILISATION.**

Astra approuva.

Puis il pensa immédiatement au stockage.

Si on conservait tous les calculs réutilisables, le disque finirait par exploser.

Chapitre 137 revenait.

Coût d’existence.

Donc un raccourci pouvait économiser du CPU tout en coûtant du stockage.

Il fallait comparer.

Gabriel sourit.

— Rien est gratuit.

— Exact.

Ils créèrent une politique.

Conserver :

calcul cher,

fréquemment réutilisé,

petit artefact,

preuve importante.

Évincer :

calcul facile,

très gros,

rarement réutilisé,

reconstructible rapidement.

Mais jamais évincer un artefact requis pour la preuve ou la provenance uniquement pour gagner de l’espace.

Gabriel écrivit :

**CACHE ≠ ARCHIVE DE PREUVE**

Astra approuva immédiatement.

Très important.

Un cache pouvait disparaître.

Une preuve nécessaire à l’audit devait rester selon sa politique de conservation.

Encore séparation des rôles.

Les raccourcis commençaient à toucher partout.

Workflow.

Preuves.

Échecs.

Batch.

Cache.

Gabriel regarda.

— On pourrait facilement devenir obsédés par l’optimisation.

Astra répondit :

— Oui.

Et voilà un autre danger.

Mesurer la machine pouvait pousser à vouloir rendre tout plus rapide.

Mais parfois, la meilleure optimisation était de ne rien changer.

Si une étape coûtait 0,01 seconde et assurait une vérification importante, pourquoi la supprimer?

Le gain serait invisible.

Le risque réel.

Gabriel écrivit :

**NE PAS OPTIMISER CE QUI N’EST PAS UN PROBLÈME.**

Astra approuva.

Une règle de vieux ingénieur.

Mais toujours utile.

Il fallait d’abord profiler.

Où était le coût réel?

Quelles étapes dominaient?

Quels calculs étaient répétés?

Quels artefacts occupaient l’espace?

Le système devait optimiser les vrais goulots.

Pas les étapes visuellement agaçantes.

Gabriel écrivit :

**MESURER AVANT DE RACCOURCIR.**

Astra approuva.

Ils regardèrent les métriques.

Une petite fonction exécutée des milliers de fois coûtait finalement beaucoup.

Une grosse étape impressionnante était rare et presque négligeable sur le total.

La carte de coût révélait une surprise.

Gabriel sourit.

— Comme toujours, le plus gros dessin est pas toujours le plus gros problème.

Exact.

Ils créèrent une carte supplémentaire.

Pas publique par défaut.

### CARTE DES COÛTS

CPU.

mémoire.

I/O.

réseau.

stockage.

temps humain.

Oui.

Temps humain aussi.

Gabriel s’arrêta.

— Ça, c’est important.

Une étape pouvait coûter peu à la machine et énormément à Gabriel.

Revenir ouvrir cinq fichiers.

Copier une référence.

Retrouver un run.

Vérifier manuellement un statut.

Un raccourci pouvait être utile même si le CPU n’économisait rien.

Il pouvait réduire les manipulations humaines.

Gabriel écrivit :

**LE COÛT HUMAIN EST UN COÛT DU SYSTÈME.**

Astra approuva.

Voilà une évidence souvent oubliée.

Brutus devait servir Gabriel.

Pas seulement produire des benchmarks élégants.

Si une automatisation économisait trente secondes de calcul mais ajoutait trois minutes de vérification manuelle, elle était peut-être pire.

Les Fourmis pouvaient donc aussi chercher des raccourcis d’interaction.

Regrouper les informations.

Préparer les preuves.

Présenter la bonne décision au bon endroit.

Pas faire cliquer dix fois.

Gabriel sourit.

— Là, elles deviennent vraiment utiles.

Le raccourci n’était plus seulement computationnel.

Il pouvait être cognitif.

Afficher directement :

résultat.

raison.

preuve.

action proposée.

Au lieu de forcer Gabriel à reconstruire le contexte.

Chapitre 147 revenait :

**ALERTE = ÉVÉNEMENT + CONTEXTE + PREUVE + ACTION POSSIBLE**

C’était un raccourci d’attention.

Très puissant.

Gabriel écrivit :

**UN BON RACCOURCI PEUT ÉCONOMISER DE L’ATTENTION SANS ÉCONOMISER DE PREUVE.**

Astra approuva.

Cette phrase était parfaite.

Parce que la preuve devait rester profonde.

Mais la surface pouvait être concise.

Encore :

**SIMPLICITÉ EN SURFACE. PROFONDEUR EN PREUVE.**

Ils commencèrent à voir les Fourmis autrement.

Au début, elles exécutaient.

Puis elles avaient appris à chercher.

Ensuite à ne pas répéter.

Maintenant, elles apprenaient à reconnaître les portions de route déjà garanties.

Une Fourmi n’était pas plus intelligente au sens mystérieux.

L’orchestrateur lui donnait de meilleures cartes.

Des certificats.

Des caches.

Des frontières.

Des précédents.

Des clés de calcul.

Alors elle pouvait faire moins de travail inutile.

Gabriel écrivit :

**UNE FOURMI PLUS RAPIDE N’EST PAS TOUJOURS UNE FOURMI QUI COURT PLUS VITE.**

Puis :

**C’EST PARFOIS UNE FOURMI QUI SAIT QUEL DÉTOUR ELLE N’A PAS BESOIN DE PRENDRE.**

Astra approuva.

Le Royaume commençait à changer.

Certaines routes devenaient plus courtes.

Pas parce que les distances physiques avaient changé.

Parce que la connaissance accumulée transformait le chemin nécessaire.

La première fois, il fallait six étapes.

Après une preuve réutilisable :

quatre.

Après une frontière :

trois.

Après un résultat partagé :

deux.

Cela ressemblait presque à de l’apprentissage.

Mais la mécanique restait visible.

Chaque raccourci avait une origine.

Une preuve.

Une règle.

Une version.

Gabriel sourit.

— C’est ça que j’aime. On peut voir pourquoi ça va plus vite.

Astra approuva.

Pas d’accélération magique.

La machine pouvait expliquer :

**Cette étape a été omise parce que certificat C-17 couvre déjà la propriété P sous version V.**

Ou :

**Ce calcul a été réutilisé parce que computation_key K correspond exactement.**

Ou :

**Le workflow s’est arrêté parce qu’une condition nécessaire a échoué.**

Voilà.

Audit.

Même les raccourcis étaient traçables.

Puis ils rencontrèrent le premier raccourci faux.

Un cache avait été considéré compatible alors qu’un paramètre secondaire avait changé.

Résultat presque identique.

Mais pas tout à fait.

Gabriel se figea.

— Là.

La différence avait été captée par un test de régression.

Bonne nouvelle.

Le raccourci n’avait pas contaminé un résultat final.

Mais l’incident était sérieux.

Ils remontèrent.

La clé de calcul n’incluait pas ce paramètre.

Gabriel écrivit :

**BUG S-001 — IDENTITÉ DE CACHE INCOMPLÈTE**

Astra approuva.

Le raccourci venait de montrer son principal danger.

La réutilisation amplifiait la confiance dans l’identité.

Si l’identité était mal définie, le réseau réutilisait quelque chose qui n’était pas réellement le même calcul.

Ils corrigèrent la clé.

Mais surtout, ils ajoutèrent un invariant.

**SI UN PARAMÈTRE PEUT MODIFIER LA SORTIE, IL DOIT PARTICIPER À L’IDENTITÉ DU CALCUL OU ÊTRE PROUVÉ IRRELEVANT.**

Gabriel sourit.

— Ça, garde ça en gros.

Astra approuva.

L’erreur S-001 devint une nouvelle frontière.

Encore.

Les erreurs devenaient du terrain.

Puis ils ajoutèrent des contrôles aléatoires.

Parfois, même lorsqu’un cache disait qu’un résultat pouvait être réutilisé, Brutus recalculerait un petit échantillon.

Audit.

Comparer.

Vérifier que les raccourcis ne dérivaient pas silencieusement.

Gabriel écrivit :

**UN RACCOURCI QUI N’EST JAMAIS RECONTRÔLÉ PEUT DEVENIR UNE HABITUDE FAUSSE.**

Astra approuva.

Les raccourcis eux-mêmes avaient donc besoin d’entretien.

Taux de hit.

Taux d’erreur.

Gain réel.

Incidents.

Version.

Certains raccourcis seraient retirés.

D’autres renforcés.

Certains deviendraient des règles solides.

Le réseau ne cherchait pas le chemin le plus court à tout prix.

Il cherchait le chemin le plus court **qui conservait ce qu’il fallait savoir**.

Gabriel écrivit :

**LE PLUS COURT CHEMIN UTILE N’EST PAS CELUI QUI SAUTE LE PLUS D’ÉTAPES.**

Puis :

**C’EST CELUI QUI NE PAIE AUCUNE ÉTAPE SANS RAISON TOUT EN PRÉSERVANT LA PREUVE.**

Astra approuva.

Voilà le chapitre.

Les Fourmis avaient découvert les raccourcis.

Mais elles avaient découvert en même temps que les bons raccourcis n’étaient pas des trous dans la méthode.

Ils étaient des morceaux de méthode déjà payés.

Des preuves réutilisées.

Des calculs partagés.

Des impasses évitées.

Des conditions qui permettaient de s’arrêter tôt.

Des décisions présentées plus clairement.

La carte n’était plus seulement remplie de routes.

Elle commençait à conserver l’expérience de leur traversée.

Et à chaque voyage correctement tracé,

le suivant pouvait parfois être un peu plus court.

Pas parce que le Royaume oubliait les étapes.

Parce qu’il savait lesquelles avaient déjà été franchies pour de vrai.

**Fin du chapitre 158.**