# Chapitre 137 — Le poids de ce qui n’existe pas

Gabriel avait passé des années à regarder ce qui existait.

Les nombres.

Les fichiers.

Les résultats.

Les images.

Les formules.

Les lignes de code.

Les cristaux.

Les machines.

Les Fourmis.

Les preuves.

Tout ce qui pouvait être montré.

Mesuré.

Sauvegardé.

Comparé.

Puis le Papillon lui avait laissé une drôle d’idée.

Peut-être qu’une partie de la puissance d’un système venait aussi de ce qu’il choisissait **de ne pas matérialiser**.

Cette pensée semblait presque vide.

Et pourtant, elle avait un poids.

Un poids informatique.

Un poids méthodologique.

Un poids architectural.

Gabriel regarda les cent quarante-quatre chambres.

Le Papillon représentait des populations gigantesques.

Mais la majorité des individus n’existaient jamais comme objets séparés.

Pas d’adresse personnelle.

Pas d’instance individuelle.

Pas de petite structure mémoire pour chacun.

Ils existaient seulement comme multiplicité.

Une quantité.

Une distribution.

Gabriel murmura :

— Donc la machine économise de la mémoire avec des objets qui n’existent même pas.

Astra répondit :

— Plus précisément, elle évite d’allouer les objets individuels dont elle n’a pas besoin.

— Je préfère ma version.

— Je sais.

Mais la correction importait.

Le Papillon ne faisait pas disparaître des objets existants.

Il choisissait une représentation où ces objets n’avaient jamais besoin d’être construits individuellement.

La différence était fondamentale.

Gabriel écrivit :

**NE PAS MATÉRIALISER ≠ SUPPRIMER APRÈS COUP**

Astra approuva.

La seconde stratégie coûtait déjà quelque chose.

Créer.

Stocker.

Puis compresser.

La première pouvait éviter le coût dès le départ.

Et cette idée semblait pouvoir s’appliquer bien au-delà du Papillon.

Gabriel ouvrit les journaux de Brutus.

Des milliers d’événements.

Certaines visualisations étaient générées puis jamais regardées.

Des objets temporaires.

Des copies.

Des structures intermédiaires.

Des artefacts créés simplement parce qu’un programme avait l’habitude de les produire.

Il demanda :

— Combien de choses on fabrique juste parce qu’on peut?

Astra répondit :

— Probablement beaucoup.

— Et combien sont réellement nécessaires?

— Il faut mesurer.

Évidemment.

Toujours mesurer.

Ils commencèrent petit.

Un workflow.

Un candidat passait du Brutotableur au Brotoculateur.

Pendant le trajet, le système créait plusieurs représentations.

Une structure source.

Une copie sérialisée.

Une représentation temporaire.

Un objet pour affichage.

Un log détaillé.

Un cache.

Un cristal provisoire.

Gabriel regarda.

— Tout ça pour un candidat?

— Oui.

— Pourquoi?

Astra parcourut les fonctions.

Certaines étaient nécessaires.

D’autres étaient héritées de décisions anciennes.

Une couche avait été ajoutée pour faciliter un débogage.

Une autre pour une ancienne interface.

Une copie existait uniquement parce que deux modules n’utilisaient pas le même format.

Gabriel sourit.

— Là, on vient de trouver du poids qui n’a peut-être plus besoin d’exister.

Ils prirent soin de ne pas tout supprimer.

Un objet apparemment inutile pouvait avoir une valeur de trace.

Ils savaient maintenant que le ménage aveugle était dangereux.

Alors ils classèrent.

**NÉCESSAIRE AU CALCUL**

**NÉCESSAIRE À LA PREUVE**

**NÉCESSAIRE À LA REPRISE**

**RECONSTRUCTIBLE**

**CACHE**

**HÉRITAGE OBSOLÈTE**

Gabriel regarda la dernière catégorie.

— Ça, ça me plaît.

Les systèmes accumulaient des couches.

Une correction temporaire devenait permanente.

Une conversion ajoutée pour un prototype restait pendant des mois.

Un fichier créé pour comprendre un bug continuait d’être généré une fois le bug disparu.

Petit à petit, les logiciels portaient le poids de leur propre histoire.

Astra répondit :

— Comme les chemins refusés.

— Exact.

Mais cette fois, le passé ne pesait pas seulement sur les décisions.

Il pesait physiquement sur le disque.

Sur la mémoire.

Sur le processeur.

Gabriel écrivit :

**UNE ARCHITECTURE PEUT PORTER DES COÛTS DONT LA RAISON D’ÊTRE A DISPARU.**

Astra approuva.

Cela ressemblait au concept de décision morte du chapitre 123.

Une règle continuant à s’appliquer après la disparition de ses conditions.

Ici, ils avaient l’équivalent technique.

**ARTEFACT MORT**

Un objet encore généré alors que la nécessité ayant justifié sa création n’existait plus.

Gabriel sourit.

— On vient de donner du travail à la Fourmi archéologue.

— Oui.

Elle pouvait rechercher :

**Pourquoi ce fichier existe-t-il?**

**Quel module le lit encore?**

**Peut-il être reconstruit?**

**Est-il cité par une preuve?**

**Sa suppression casserait-elle un workflow?**

Gabriel se pencha.

— Ça, c’est plus intéressant que juste “supprimer les gros fichiers”.

— Beaucoup plus sûr.

Ils avaient déjà appris :

**TAILLE ≠ VALEUR.**

Un fichier minuscule pouvait être une preuve unique.

Un fichier énorme pouvait être un cache reproductible.

La politique de réduction devait donc porter sur la fonction.

Pas seulement le poids.

Gabriel dit :

— On va appeler ça le poids logique.

Astra réfléchit.

— Définis-le.

Gabriel hésita.

— Pas le poids en octets. Le coût que cet objet impose au système parce qu’il existe.

Astra approuva prudemment.

Un objet pouvait avoir plusieurs coûts.

Mémoire.

Disque.

CPU.

Bande passante.

Complexité.

Temps humain.

Risque de confusion.

Maintenance.

Gabriel écrivit :

**COÛT D’EXISTENCE**

Puis il sourit.

— Voilà.

Tout élément de Brutus avait un coût d’existence.

Même petit.

Une variable.

Un fichier.

Un module.

Une API.

Une interface.

Une règle.

Une Fourmi.

Quelqu’un devait la maintenir.

La documenter.

La tester.

La comprendre.

Plus on ajoutait, plus le système payait.

Astra dit :

— Ça rejoint le chapitre 135.

— Oui.

— Ajouter un module n’est pas gratuit.

— Exact.

Une nouvelle machine pouvait être utile.

Mais elle apportait aussi :

un contrat à maintenir,

une connexion à tester,

des versions,

des erreurs possibles,

des dépendances,

une documentation,

des traces.

Gabriel regarda toute l’architecture.

— Donc avant d’ajouter, on devrait demander si la fonction n’existe pas déjà.

— Oui.

— Et si elle mérite son coût.

— Exact.

Ils ajoutèrent une règle à la douane Brutus.

### TEST DU COÛT D’EXISTENCE

**Quelle nouvelle capacité apporte le module?**

**Quelle duplication crée-t-il?**

**Quel coût de maintenance ajoute-t-il?**

**Peut-on obtenir la même capacité avec un module existant?**

**Que se passe-t-il si on ne le construit pas?**

Gabriel regarda la dernière question.

— Ça, c’est très important.

Parce que les inventeurs demandaient naturellement :

**Que se passe-t-il si je construis ça?**

Mais rarement :

**Que se passe-t-il si je ne le construis pas?**

L’absence pouvait parfois être la meilleure décision.

Il écrivit :

**TOUT CE QUI PEUT ÊTRE CONSTRUIT NE MÉRITE PAS D’EXISTER.**

Astra répondit :

— Principe d’ingénierie, pas jugement universel.

Gabriel rit.

— Évidemment.

Ils revinrent au Papillon.

Cent quarante-quatre chambres.

Imaginez une population de dix millions.

Dans une représentation naïve, dix millions d’objets.

Dans le modèle agrégé, cent quarante-quatre accumulateurs et de grandes multiplicités.

La différence n’était pas seulement :

**moins de mémoire utilisée.**

C’était :

**des millions d’objets n’ont jamais eu besoin d’exister comme objets.**

Gabriel trouvait cette idée fascinante.

Le rien avait donc une valeur mesurable.

Ce qu’on ne créait pas ne consommait pas.

Pas de mémoire pour cet objet.

Pas de descripteur.

Pas de référence.

Pas de cycle de vie.

Pas de sérialisation.

Pas de destruction.

Le poids de ce qui n’existait pas était précisément le poids que la machine n’avait pas à porter.

Astra dit :

— Attention à la formulation.

— Je sais.

— Ce n’est pas un “poids négatif”.

— Non.

— C’est un coût évité.

Gabriel écrivit :

**LE POIDS DE CE QUI N’EXISTE PAS = LE COÛT ÉVITÉ PAR NON-MATÉRIALISATION.**

Il regarda.

— Ça fait le titre.

— Oui.

L’idée devint immédiatement plus large.

Dans le Royaume des traces, fallait-il matérialiser toutes les relations possibles entre tous les cristaux?

Non.

Avec dix mille cristaux, le nombre de paires possibles devenait immense.

La plupart n’avaient aucun intérêt.

Il valait mieux créer les relations lorsqu’une raison existait.

Gabriel écrivit :

**NE PAS MATÉRIALISER TOUT LE GRAPHE POSSIBLE.**

**MATÉRIALISER LES RELATIONS JUSTIFIÉES.**

Astra approuva.

Sinon Brutus pourrait dépenser des ressources à calculer des connexions entre objets qui ne se rencontreraient jamais.

Même problème avec le Brotoculateur.

Cent formules.

Comparer chaque paire systématiquement?

Des milliers de comparaisons.

Et si on ajoutait encore des paramètres, les combinaisons explosaient.

Gabriel regarda.

— Donc la meilleure comparaison est parfois celle qu’on ne fait pas.

— Si elle n’a aucune valeur attendue, oui.

Il sourit.

Le principe revenait partout.

Ne pas confondre capacité et nécessité.

Brutus pouvait peut-être tester un million de combinaisons.

Cela ne signifiait pas qu’il devait le faire.

Gabriel écrivit :

**CALCUL DISPONIBLE ≠ CALCUL UTILE**

Puis :

**L’ABSENCE D’UN CALCUL PEUT ÊTRE UNE OPTIMISATION SI SA VALEUR INFORMATIONNELLE EST FAIBLE.**

Astra approuva.

Une question apparaissait alors :

comment décider ce qui mérite d’exister?

Pas seulement les objets.

Les tests.

Les comparaisons.

Les tâches.

Les traces.

Les visualisations.

Ils revenaient à la valeur informationnelle.

Un test devait être priorisé lorsqu’il pouvait distinguer des hypothèses.

Une trace devait être conservée lorsqu’elle était nécessaire à la preuve, à la reprise ou à l’histoire.

Une représentation devait être matérialisée lorsqu’une question l’exigeait.

Gabriel vit une structure générale.

**CRÉER SEULEMENT SI LA CRÉATION ACHÈTE QUELQUE CHOSE.**

Astra répondit :

— Définis “achète”.

— Information. Preuve. Fonction. Reprise. Compréhension.

— Bon.

Ils formalisaient presque une économie interne.

Chaque objet coûtait.

Chaque objet devait produire une valeur.

Pas nécessairement financière.

Valeur de preuve.

Valeur de calcul.

Valeur documentaire.

Valeur opérationnelle.

Gabriel dit :

— Brutus devrait avoir un comptable.

Astra répondit :

— Pitié.

Il éclata de rire.

Mais l’idée d’un **budget de complexité** avait du sens.

Un module pouvait être techniquement performant mais trop complexe à maintenir.

Une optimisation pouvait économiser 1 MB et ajouter cinq mille lignes de code fragiles.

Mauvais échange.

Un format compact pouvait économiser de l’espace mais rendre impossible l’audit.

Mauvais échange.

Une compression pouvait retirer exactement le détail nécessaire à une reproduction.

Catastrophe.

Ils écrivirent :

**OPTIMISER UNE RESSOURCE PEUT DÉGRADER UNE AUTRE.**

Puis :

**AUCUNE COMPRESSION N’EST GRATUITE SI ELLE MODIFIE L’INFORMATION DISPONIBLE.**

Gabriel regarda.

Le Papillon revenait encore.

Sa force venait d’accepter explicitement une perte d’individualité lorsqu’elle n’était pas nécessaire.

Cette perte était admissible seulement parce que la question ciblée n’exigeait pas cette information.

Donc toute compression devrait annoncer ce qu’elle abandonnait.

Gabriel écrivit :

**TOUTE COMPRESSION SÉMANTIQUE DOIT DIRE CE QU’ELLE NE PERMET PLUS DE RECONSTRUIRE.**

Astra approuva immédiatement.

Cela pouvait devenir une règle pour les Fourmis de ménage.

Avant de compresser :

**Qu’est-ce qui sera perdu?**

Si la réponse était :

**rien, compression sans perte vérifiée**

très bien.

Si la réponse était :

**des détails reconstruisibles depuis une source conservée**

probablement acceptable.

Si la réponse était :

**des informations uniques nécessaires à la preuve**

interdit.

Gabriel sourit.

— Là on peut enfin laisser une Fourmi faire du ménage sans lui donner une tronçonneuse.

— Exact.

Ils imaginèrent le protocole.

### FOURMI DE COMPRESSION

1. Identifier l’artefact.
2. Trouver ses dépendances.
3. Vérifier s’il est la seule copie.
4. Vérifier s’il est reconstructible.
5. Identifier la valeur de preuve.
6. Calculer le gain attendu.
7. Produire une proposition.
8. Ne supprimer que selon la politique autorisée.
9. Laisser une trace de l’opération.

Gabriel regarda le point neuf.

Même la suppression devait laisser une trace.

Bien sûr.

Si un fichier disparaissait, le système devait savoir :

qui l’avait supprimé,

pourquoi,

quand,

selon quelle règle,

et comment le reconstruire si c’était possible.

Ils écrivirent :

**L’ABSENCE ELLE-MÊME PEUT AVOIR UNE PROVENANCE.**

Gabriel s’arrêta.

— Ça, c’est bizarrement beau.

Astra répondit :

— Et techniquement utile.

Un fichier absent sans explication était un problème.

Un fichier absent parce qu’il avait été remplacé par un hash + une recette de reconstruction était une décision.

Même le vide pouvait être documenté.

Gabriel pensa aux chemins refusés.

Ils n’existaient pas comme trajectoires exécutées.

Pourtant, leur absence avait une raison.

Les décisions non prises aussi avaient une trace.

Encore une fois, le projet rejoignait le même motif.

Ce qui n’existait pas pouvait avoir de la valeur.

Un chemin non suivi.

Un objet non matérialisé.

Un calcul non exécuté.

Un fichier non conservé.

Mais seulement si le système savait **pourquoi**.

Gabriel écrit :

**UN VIDE NON EXPLIQUÉ EST UNE LACUNE.**

**UN VIDE JUSTIFIÉ EST UNE DÉCISION.**

Astra approuva.

Cette phrase devint l’une de ses préférées.

Ils testèrent la Fourmi de compression sur un petit répertoire.

Pas sur les preuves importantes.

Un bac temporaire.

Cent fichiers.

Plusieurs duplicatas exacts.

Des visualisations régénérables.

Des caches.

Quelques logs uniques.

La Fourmi analysa.

Elle proposa :

**18 duplicatas exacts → déduplication**

**23 images reconstructibles → conservation optionnelle**

**41 caches → expiration possible**

**18 fichiers à conserver**

Gabriel regarda.

— Pourquoi les dix-huit derniers?

Astra ouvrit la liste.

Certains contenaient des données originales.

D’autres étaient référencés par des cristaux.

Deux semblaient inutiles mais leur provenance n’était pas claire.

Gabriel sourit.

— Donc elle refuse de supprimer ce qu’elle ne comprend pas.

— Oui.

C’était exactement ce qu’il voulait.

Le système devait être conservateur face à l’inconnu.

Pas conserver tout éternellement.

Mais ne pas prendre une absence d’information pour une permission.

Ils ajoutèrent :

**SI LA VALEUR DE PREUVE EST INCONNUE, NE PAS SUPPRIMER AUTOMATIQUEMENT.**

Très simple.

Très important.

Ils appliquèrent la déduplication.

Le stockage diminua.

Pas énormément.

Ce n’était qu’un petit test.

Mais chaque fichier supprimé était remplacé par une référence claire.

Hash.

Origine.

Localisation canonique.

La trace demeurait.

Gabriel observa.

— On vient d’enlever des choses sans perdre leur histoire.

— Oui.

Et cette formulation résumait parfaitement l’objectif.

Le but n’était pas de tout garder physiquement.

Le but était de garder ce qui était nécessaire pour reconstruire, vérifier ou comprendre.

Parfois l’histoire pouvait survivre sans toutes ses copies.

Gabriel regarda le Royaume.

Il imagina des années de croissance.

Des millions de cristaux.

Des milliards d’événements.

À cette échelle, aucune architecture ne pouvait simplement dire :

**on garde tout de la même manière.**

Il faudrait des couches.

Des niveaux de température.

Données actives.

Archives.

Sources primaires.

Caches.

Résumés.

Indices.

Copies froides.

La mémoire elle-même aurait besoin d’une architecture.

Gabriel dit :

— On va finir par construire un Brutus pour gérer Brutus.

Astra répondit :

— C’est déjà un peu ce qu’on fait.

Il rit.

Puis il se tut.

Parce qu’elle avait raison.

La machine derrière les machines devait aussi gérer les coûts des machines.

Orchestration.

Stockage.

Compression.

Priorité.

Reprise.

Le système devait apprendre à ne pas s’effondrer sous son propre succès.

Plus Brutus produirait de résultats, plus ce problème deviendrait important.

Gabriel écrivit :

**UN SYSTÈME QUI SAIT PRODUIRE DOIT AUSSI SAVOIR NE PAS S’ENSEVELIR SOUS SA PRODUCTION.**

Astra approuva.

Le Brutotableur pouvait générer énormément de candidats.

Les Fourmis énormément de tests.

Le Brotoculateur énormément de comparaisons.

Le Royaume énormément de traces.

Sans politiques, la réussite devenait elle-même un problème.

Gabriel comprit quelque chose.

L’optimisation n’était donc pas un chantier secondaire à faire après que tout fonctionne.

Elle faisait partie de l’architecture.

Mais pas l’optimisation obsessionnelle de chaque microseconde.

L’optimisation de ce qui méritait d’exister.

Quel objet?

Quelle trace?

Quelle comparaison?

Quelle copie?

Quelle représentation?

Quel niveau de détail?

Il regarda le Papillon.

Cent quarante-quatre chambres.

Pas dix millions d’objets.

Cette architecture donnait une réponse radicale à une question spécifique.

**Nous n’avons pas besoin que chaque individu existe séparément pour répondre à cette question.**

Et alors, ils n’existaient pas.

Gabriel murmura :

— C’est presque de la sculpture.

Astra demanda :

— Comment?

— Tu enlèves ce qui n’est pas nécessaire.

— En informatique, tu peux aussi éviter de le créer.

Gabriel sourit.

— Encore mieux.

Ils reprirent la carte de Brutus.

Cette fois, ils ne demandèrent pas :

**Qu’est-ce qu’on peut ajouter?**

Ils demandèrent :

**Qu’est-ce qui peut ne pas exister?**

Certaines réponses furent immédiates.

Copies inutiles.

Caches morts.

Anciennes conversions.

Comparaisons sans valeur.

Visualisations jamais utilisées.

D’autres restèrent difficiles.

Certaines informations semblaient inutiles aujourd’hui mais pourraient devenir importantes demain.

Il fallait donc éviter l’excès inverse.

Tout minimaliser pouvait rendre le système incapable d’apprendre du passé.

Gabriel écrivit :

**MINIMALISME ≠ AMNÉSIE**

Astra approuva.

Voilà l’équilibre.

Le Papillon lui-même ne conservait pas l’individualité parce que son usage ne l’exigeait pas.

Mais les cristaux, eux, avaient besoin de l’histoire.

On ne pouvait pas appliquer la même compression partout.

Il fallait préserver l’information nécessaire à la fonction.

Gabriel regarda le tableau.

**Question → information nécessaire → représentation minimale suffisante**

Il resta silencieux.

— Là, on a peut-être une règle générale de conception.

Astra répondit :

— Comme principe, oui.

Pas une formule universelle.

Pas une loi.

Mais une excellente discipline.

Avant de construire une grosse représentation, demander :

**Quelle question doit-elle répondre?**

Puis :

**Quelle est l’information minimale suffisante pour répondre sans perdre ce qui compte?**

Le Papillon devenait l’exemple parfait.

Pas parce qu’il était toujours la réponse.

Parce qu’il incarnait la question.

Gabriel regarda les 144 chambres une dernière fois.

Et cette fois, ce qui l’impressionna le plus n’était pas ce qu’elles contenaient.

C’était tout ce qu’elles n’avaient jamais eu besoin de contenir.

Des millions d’objets qui n’avaient jamais été créés.

Des allocations jamais faites.

Des structures jamais sérialisées.

Des identités jamais suivies.

Pas parce qu’elles avaient été perdues par accident.

Parce que la question n’en avait jamais eu besoin.

Le poids de ce qui n’existait pas n’apparaissait dans aucun fichier.

On ne pouvait pas le poser sur une balance.

Mais on pouvait le mesurer indirectement.

Dans la mémoire économisée.

Dans les objets évités.

Dans les calculs non exécutés.

Dans les chemins ignorés.

Dans les copies supprimées.

Dans la complexité qu’on avait refusé d’ajouter.

Gabriel sourit.

Pendant longtemps, il avait cru qu’un grand système devait contenir énormément de choses.

Maintenant, il commençait à comprendre qu’un grand système devait surtout savoir **quelles choses méritaient réellement d’exister**.

**Fin du chapitre 137.**