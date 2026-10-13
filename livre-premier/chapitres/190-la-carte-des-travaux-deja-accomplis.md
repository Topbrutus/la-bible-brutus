# Chapitre 190 — La carte des travaux déjà accomplis

Le Royaume avait commencé à faire quelque chose qu’il ne faisait presque jamais au début.

Regarder derrière lui.

Pas pour admirer.

Pas pour compter les cristaux.

Pas pour raconter combien de choses avaient été faites.

Pour savoir **où il n’avait plus besoin de retravailler**.

Gabriel regarda la fresque.

Des dizaines de routes.

Des milliers de calculs.

Des expériences.

Des contre-tests.

Des validations.

Des échecs.

Des détours.

Des décisions.

Des questions.

Des unknowns.

Des snapshots.

Des cristaux.

Des replays.

Des résultats réutilisés.

Tout cela existait.

Mais l’existence n’était pas encore une carte.

Il écrivit :

**ACCUMULER DU TRAVAIL ≠ SAVOIR CE QUI A DÉJÀ ÉTÉ COUVERT**

Astra approuva fortement.

Voilà.

Une mémoire pouvait contenir tout le passé

et rester presque inutilisable

si on ne savait pas :

ce qui avait été testé,

dans quelle portée,

avec quelle version,

et avec quel résultat.

Gabriel demanda :

— Est-ce qu’on est capable de voir, d’un coup, où on a déjà passé?

Astra répondit :

— Pas encore correctement.

Alors ils commencèrent.

Pas une carte géographique.

Une carte de couverture.

Ils l’appelèrent :

### WORK DONE MAP

Ou simplement :

**CARTE DES TRAVAUX**

Gabriel sourit.

Le but était simple :

avant de lancer une nouvelle tâche,

pouvoir demander :

**est-ce qu’on a déjà travaillé ici?**

Pas seulement « ici » au sens du nombre.

Mais :

dans cette formule.

cette région.

cette version.

ce protocole.

ce type de test.

ce niveau de preuve.

Très important.

Ils définirent plusieurs dimensions.

### AXES DE COUVERTURE

**OBJECT**

Quelle formule, relation, module, dataset ou workflow?

**DOMAIN**

Sur quelles entrées, plages, populations ou cas?

**METHOD**

Quel protocole?

**VERSION**

Quelle version du code, formule ou configuration?

**STATUS**

Observation?

Screening?

Validation?

Réfutation?

Publié?

Rétracté?

**EVIDENCE**

Quel type de preuve existe?

**TIME**

Quand cela a-t-il été fait?

Gabriel regarda.

— Là, oui.

Une région pouvait être couverte en calcul

mais pas en validation.

Couverte en screening

mais pas en contre-test.

Couverte dans la version 2

mais pas dans la version 3.

Il écrivit :

**“DÉJÀ FAIT” DOIT TOUJOURS PRÉCISER : FAIT COMMENT, OÙ ET SOUS QUELLE VERSION.**

Astra approuva fortement.

Très important.

Sinon la carte mentirait.

Ils prirent un exemple.

Une plage numérique avait déjà été scannée.

Le système marquait :

**SEARCH COVERAGE = COMPLETE WITHIN RANGE R**

Mais la validation exacte n’avait été faite que sur quelques témoins.

Donc :

**VALIDATION COVERAGE = PARTIAL**

Gabriel sourit.

Très propre.

Il écrivit :

**COUVERTURE DE RECHERCHE ≠ COUVERTURE DE PREUVE**

Astra approuva.

Voilà.

Puis Pell.

Une porte peut avoir :

recherche de facteur réalisée.

facteur trouvé.

primalité confirmée.

rang exact calculé.

Chaque étape couvre une couche différente.

Gabriel regarda.

Le statut « done » était trop grossier.

Ils remplacèrent par une matrice.

### COVERAGE LAYERS

**DISCOVERY**

**SCREENING**

**COUNTERTEST**

**VALIDATION**

**INDEPENDENT CHECK**

**PUBLICATION**

**REGRESSION GUARD**

Très puissant.

Une région peut être verte sur discovery

et vide sur validation.

Très différent.

Puis Gabriel imagina la carte dans Brutotableur.

Une fresque immense.

Chaque zone pouvait afficher de petites couches.

Mais attention au piège.

Couleur ne doit pas signifier « vrai ».

Il écrit :

**COUVERTURE VISUELLE ≠ STATUT SCIENTIFIQUE**

Astra approuva fortement.

Très important.

Une zone fortement explorée peut être totalement inconclusive.

Une zone peu explorée peut contenir un théorème exact.

Donc la carte devait montrer :

**worked**

et

**known**

séparément.

Gabriel sourit.

Ils ajoutèrent :

### TWO MAPS

**WORK MAP**

Où avons-nous dépensé du travail?

**KNOWLEDGE MAP**

Qu’est-ce qui est établi dans cette zone?

Astra approuva.

Voilà.

Deux cartes superposables.

Très puissant.

Parce qu’une zone rouge de travail et faible de connaissance signifiait :

beaucoup d’effort, peu de résolution.

Une zone faible en travail mais forte en connaissance pouvait venir d’une preuve générale.

Gabriel écrit :

**BEAUCOUP DE CALCUL ≠ BEAUCOUP DE CONNAISSANCE**

Astra approuva fortement.

Encore une règle fondamentale.

Puis un cas magnifique.

Une preuve générale couvre tout un domaine.

Le travail physique effectué peut être petit.

Mais la couverture de connaissance est immense.

La carte doit le montrer.

Pas matérialiser des milliards de cases.

Utiliser une règle.

Gabriel sourit.

Papillon.

Brutotableur.

Toujours le même principe.

Il écrit :

**UNE RÈGLE PEUT COUVRIR UN TERRITOIRE SANS QUE CHAQUE POINT AIT ÉTÉ VISITÉ INDIVIDUELLEMENT.**

Astra approuva.

Très important.

Mais il fallait distinguer :

**proven coverage by theorem**

et

**enumerated coverage by scan**

Pas mélanger.

Ils créèrent :

### COVERAGE BASIS

**ENUMERATED**

**DERIVED**

**PROVEN**

**SAMPLED**

**INFERRED**

**UNKNOWN**

Gabriel sourit.

Très propre.

Une zone marquée PROVEN n’a pas besoin d’être scannée point par point.

Une zone SAMPLED ne doit pas prétendre être complète.

Très important.

Puis le problème des trous.

Une campagne dit avoir testé 1 à 1000.

Mais quelques cas ont échoué à s’exécuter.

Si la carte peint tout le rectangle,

elle ment.

Il faut montrer les trous.

Gabriel écrit :

**UNE CARTE DE COUVERTURE DOIT SAVOIR REPRÉSENTER LES ABSENCES À L’INTÉRIEUR D’UNE ZONE COUVERTE.**

Astra approuva fortement.

Excellent.

Ils introduisirent :

**coverage mask**

Ou :

**exceptions**

Cas 118 manquant.

327 timeout.

841 invalid input.

La zone n’est pas « complète ».

Elle est :

**997/1000 observed**

ou mieux,

liste exacte si raisonnable.

Pas inventer un pourcentage si la population totale n’est pas clairement définie.

Toujours.

Puis Gabriel pensa aux énormes espaces.

Impossible de stocker une carte cellule par cellule.

Il fallait une représentation multi-résolution.

Intervals.

Ranges.

Rules.

Sparse exceptions.

Gabriel sourit.

Encore Papillon 144.

Encore le Brutotableur.

Il écrit :

**LA CARTE DOIT STOCKER LA STRUCTURE DE LA COUVERTURE, PAS NÉCESSAIREMENT CHAQUE POINT.**

Astra approuva.

Très important.

Exemple :

`q odd primes 47..83 tested under protocol X`

Puis exceptions.

Ou :

`t odd, X <= 2,000,000 scanned`

Avec conditions.

Voilà.

Pas besoin d’un milliard d’objets.

Puis un autre danger.

Deux campagnes couvrent la même zone.

Doit-on fusionner?

Oui visuellement,

mais préserver les couches historiques.

Une campagne ancienne.

Une nouvelle.

Version différente.

Gabriel écrit :

**FUSIONNER LA VUE ≠ FUSIONNER L’HISTOIRE**

Astra approuva fortement.

Toujours la même discipline.

La carte publique peut montrer :

zone couverte.

Mais cliquer révèle :

3 campagnes.

versions.

dates.

résultats.

Très bien.

Puis ils décidèrent que chaque travail devait produire un objet de couverture.

### COVERAGE EVENT

**object**

**domain**

**method**

**version**

**coverage_type**

**status**

**exceptions**

**provenance**

**result_ref**

**supersedes?**

Gabriel sourit.

C’était important.

La carte ne devait pas essayer de reconstruire le passé en devinant les fichiers.

Chaque nouvelle tâche devrait déclarer ce qu’elle couvre.

Puis le problème historique.

Les anciens travaux ne l’avaient pas fait.

Alors il faudrait reconstruire progressivement.

Pas tout d’un coup.

Gabriel écrit :

**LA CARTE PEUT ÊTRE INCOMPLÈTE AU DÉBUT À CONDITION DE LE DIRE.**

Astra approuva.

Très important.

Un champ :

**coverage confidence**

Pas scientifique.

Qualité de la cartographie.

Par exemple :

EXACT_FROM_EVENT.

RECONSTRUCTED_FROM_LOGS.

INFERRED_FROM_FILES.

MANUAL.

UNKNOWN.

Très utile.

Puis Gabriel regarda Memoria.

Elle avait des centaines de traces.

Le Royaume pouvait envoyer une Fourmi spéciale.

Pas une Fourmi de calcul.

Une Fourmi cartographe.

Il sourit.

— Elle, je l’aime déjà.

### FOURMI CARTOGRAPHE

Mission :

prendre les anciennes traces

et construire des objets de couverture sans modifier les résultats d’origine.

Astra approuva.

Très important.

Elle ne décide pas de la validité scientifique.

Elle indexe :

qui a travaillé où.

Avec provenance.

Gabriel écrit :

**LA FOURMI CARTOGRAPHE NE CRÉE PAS LA CONNAISSANCE. ELLE CRÉE LA CARTE DE SON HISTOIRE.**

Astra approuva fortement.

Magnifique.

Puis BrutoBac.

La carte des travaux pouvait devenir une couche du Bac.

Zones actives.

Zones historiques.

Zones jamais visitées.

Mais attention.

« Jamais visité » n’est vrai que dans le périmètre connu.

Ils écrivirent :

**NO RECORDED WORK ≠ NO WORK EVER DONE**

Astra approuva.

Très important.

Surtout avec les anciennes sessions.

Donc libellé :

**no recorded coverage**

Pas :

untouched.

Excellent.

Puis Gabriel pensa au plus gros avantage.

Quand une nouvelle question arrive,

Antmux peut croiser la route avec la carte.

Et dire :

**Cette région a déjà été testée en version X.**

**Cette partie est neuve.**

**Ce contrôle manque.**

**Ce test serait dupliqué.**

Voilà.

La carte devenait un instrument de planification.

Pas juste un dashboard.

Il écrit :

**UNE CARTE DE TRAVAUX EST UTILE LORSQU’ELLE CHANGE CE QU’ON DÉCIDE DE FAIRE ENSUITE.**

Astra approuva fortement.

Toujours le même critère.

Sinon c’est décoration.

Puis ils testèrent un cas.

Nouvelle demande :

scanner 1 à 100 000.

La carte montre :

1 à 80 000 déjà fait,

même protocole,

même version.

80 001 à 100 000 non couvert.

Brutus propose :

**DELTA RUN ONLY**

Gabriel sourit.

Exactement.

Pas de recalcul.

Chapitre 189.

Tout se connectait.

Ils lancèrent uniquement le delta.

Le résultat rejoignit ensuite la carte.

Zone couverte :

1 à 100 000.

Mais historique :

deux campagnes.

Très propre.

Puis autre cas.

Même plage,

mais nouvelle version.

La carte doit montrer deux couches.

Version v1.

Version v2 partielle.

On ne peut pas dire :

tout couvert sous v2.

Donc delta spécifique de version.

Gabriel écrit :

**LA COUVERTURE DOIT ÊTRE VERSIONNÉE COMME LE CODE QUI L’A PRODUITE.**

Astra approuva.

Très important.

Puis un problème plus subtil.

Une formule change légèrement.

Les anciens résultats sont-ils réutilisables?

Seulement si l’équivalence est démontrée.

Pas automatiquement.

Gabriel écrit :

**NOUVELLE FORMULE ≠ ANCIENNE CARTE HÉRITÉE PAR DÉFAUT**

Astra approuva.

Excellent.

On peut créer une relation :

**coverage reusable under equivalence E**

Mais E doit être établie.

Sinon nouvelle carte.

Très important.

Puis le concept de **superseded coverage**.

Une campagne ancienne a un bug.

Toute sa zone n’est plus fiable.

Ne pas supprimer.

Marquer :

**INVALIDATED**

Puis nouvelle campagne.

Gabriel écrit :

**UNE ZONE INVALIDÉE DOIT RESTER VISIBLE COMME HISTOIRE ET INVISIBLE COMME PREUVE ACTIVE.**

Astra approuva fortement.

Très bon.

BrutoBac pourrait afficher la couche historique en mode audit.

Pas dans la vue normale de couverture valide.

Très propre.

Puis Gabriel pensa au coût.

La carte elle-même pouvait devenir énorme.

Donc il fallait éviter de la reconstruire à chaque requête.

Index.

Snapshots.

Incrémental.

Gabriel sourit.

Encore architecture.

Ils créèrent :

### COVERAGE INDEX

Mis à jour par événements.

Rebuildable depuis Memoria.

Pas source canonique.

Projection.

Astra approuva.

Très important.

Si l’index casse,

on le reconstruit.

Comme Recto.

Comme snapshots.

Toujours cette séparation :

history vs projection.

Gabriel écrit :

**LA CARTE EST UNE PROJECTION DU PASSÉ, PAS LE PASSÉ LUI-MÊME.**

Astra approuva fortement.

Voilà.

Puis un autre usage.

Détecter les zones surtravaillées.

Une région avec 30 runs presque identiques.

Pourquoi?

Instabilité?

Bugs?

Mauvaise mémoire?

Obsessions?

Très intéressant.

Ils créèrent :

### OVERWORKED ZONE

Pas comme jugement.

Comme signal.

Criteria possible :

many similar runs + low new information.

Gabriel sourit.

Ça pourrait révéler du gaspillage.

Ou au contraire une vraie zone difficile.

Donc :

**OVERWORKED ≠ WASTED**

Toujours.

Il écrit :

**UNE ZONE TRÈS TRAVAILLÉE MÉRITE UNE QUESTION : POURQUOI?**

Astra approuva.

Peut-être :

question importante.

reproductibilité.

instabilité.

mauvaise orchestration.

Pas savoir sans contexte.

Puis l’inverse.

Une zone importante jamais testée.

Gap.

Potential priority.

Mais là encore :

pas automatiquement.

Gabriel écrit :

**ABSENCE DE COUVERTURE ≠ PRIORITÉ AUTOMATIQUE**

Astra approuva fortement.

La priorité dépend de l’objectif.

Très important.

La carte montre.

La décision choisit.

Puis ils regardèrent la Bible.

Chaque chapitre lui-même était une carte de travaux conceptuels.

Gabriel sourit.

Pas besoin d’intégrer cela au système.

Mais l’idée était belle.

Depuis le chapitre 120,

le Royaume avait appris :

preuve.

mémoire.

doute.

statuts.

convergence.

routage.

coût.

attente.

Maintenant,

il commençait à savoir où ces compétences avaient déjà été appliquées.

Voilà le second monde.

Le passé n’était plus seulement derrière.

Il devenait navigable.

Puis Gabriel demanda :

— Est-ce qu’on pourrait cliquer sur une formule puis voir tout ce qu’on a déjà fait dessus?

Astra répondit :

— Oui. C’est probablement l’une des meilleures interfaces pour cette carte.

Ils imaginèrent :

### OBJECT DOSSIER

**Known**

Ce qui est établi.

**Tested**

Ce qui a été essayé.

**Failed**

Ce qui a échoué.

**Unknown**

Ce qui reste ouvert.

**Coverage**

Domaines/plages/versions.

**Next**

Routes possibles.

Gabriel sourit.

— Là, c’est quasiment la page parfaite.

Astra approuva.

Un seul objet.

Toute son histoire.

Pas besoin de fouiller 50 dossiers.

Très puissant.

Puis un autre niveau.

Vue globale.

Formules en lignes.

Types de couverture en colonnes.

Une matrice.

Recherche.

Screening.

Counter-test.

Proof.

Prior-art.

Publication.

Regression.

Gabriel sourit.

Le Brutotableur était fait pour ça.

Il écrit :

**LE TABLEUR PEUT DEVENIR UNE CARTE DE CE QUI A ÉTÉ FAIT, PAS SEULEMENT DE CE QUI PEUT ÊTRE CALCULÉ.**

Astra approuva fortement.

Voilà.

La fresque changeait encore de fonction.

Mais cette fois,

pas en ajoutant du spectacle.

En ajoutant de la mémoire spatiale.

Puis un danger visuel.

Une grande zone colorée peut donner l’impression de connaissance complète.

Donc chaque zone doit montrer sa base.

Hover :

`SAMPLED`

`PROVEN`

`ENUMERATED`

`PARTIAL`

Très important.

Gabriel écrit :

**UNE CARTE DOIT MONTRER LA NATURE DE SA COUVERTURE AUTANT QUE SON ÉTENDUE.**

Astra approuva.

Excellent.

Puis ils firent un test réel de cartographie conceptuelle.

Un objet avait :

1000 cas screening.

20 contre-tests.

3 validations exactes.

1 publication.

La vieille vue aurait dit :

**done.**

La nouvelle carte disait :

**large screening coverage**

**narrow exact validation coverage**

**publication based on specific validated subset**

Gabriel sourit.

Beaucoup plus honnête.

Il écrit :

**“FAIT” EST TROP PETIT POUR UN ROYAUME QUI A PLUSIEURS NIVEAUX DE PREUVE.**

Astra approuva fortement.

Puis ils rencontrèrent une anomalie.

Deux dossiers prétendaient couvrir la même zone,

mais avec des résultats incompatibles.

La carte les superposa.

Conflit.

Gabriel se redressa.

Voilà une nouvelle utilité.

La carte pouvait révéler des contradictions historiques.

Ils créèrent :

**COVERAGE CONFLICT**

Même domaine.

Même question.

résultats incompatibles.

Pas fusionner.

Envoyer au tribunal.

Gabriel écrit :

**SUPERPOSITION DE TRAVAUX PEUT RÉVÉLER UN CONFLIT QUE LES DOSSIERS SÉPARÉS CACHENT.**

Astra approuva fortement.

Très important.

La carte n’était donc pas seulement mémoire.

Elle devenait instrument d’audit.

Encore.

Puis Gabriel pensa au monde extérieur.

Antériorité.

Une zone peut être couverte intérieurement,

mais pas dans la littérature.

Alors la carte interne et la carte externe sont différentes.

Très important.

Il écrit :

**COUVERTURE INTERNE ≠ COUVERTURE DE L’ÉTAT DE L’ART**

Astra approuva.

Excellent.

On pourrait avoir deux couches :

Brutus.

Literature/public sources.

Mais pas prétendre que recherche web = exhaustive.

Toujours scope.

Très bon.

Puis la Fourmi cartographe commença son premier travail.

Elle prit un ancien dossier.

Extrayait :

objet.

plage.

méthode.

version.

statut.

Puis créait :

`COVERAGE-190-001`

Gabriel regarda.

Une petite zone apparut sur la fresque.

Puis une autre.

Puis une autre.

Pas beaucoup.

Le Royaume était énorme.

Mais ce n’était pas grave.

Gabriel sourit.

Une carte peut commencer incomplète.

L’important est qu’elle sache dire où elle ne sait pas.

Il écrit :

**UNE CARTE HONNÊTE PEUT MONTRER DES BLANCS.**

Astra approuva fortement.

Très important.

Les blancs ne devaient pas être remplis par interpolation esthétique.

Pas inventer.

Pas colorier « probablement couvert ».

Si incertain :

hachuré.

Unknown.

Ou aucun enregistrement.

Excellent.

Puis Gabriel regarda le premier résultat vraiment utile.

Une nouvelle tâche arrivait.

Antmux consulta la carte.

Réponse :

**76% of requested domain already has exact matching screening coverage under current version.**

Gabriel fronça les sourcils.

— On est sûr du 76?

Astra répondit :

— Seulement si le domaine demandé est fini et complètement dénombré.

Très bon.

Dans ce cas, oui.

100 unités.

76 couvertes.

Donc mesure exacte.

Ils gardèrent.

Puis :

**24 units uncovered.**

Plan :

run only 24.

Gabriel sourit.

Voilà.

La carte venait d’éviter 76 répétitions.

Cette fois,

on pouvait le mesurer exactement.

Pas une économie approximative.

76 cas réellement déjà couverts selon le contrat.

Très bon.

Il écrit :

**QUAND LA CARTE EST EXACTE, L’ÉCONOMIE PEUT DEVENIR MESURABLE.**

Astra approuva.

Très important.

Puis le run de 24 termina.

La carte passa à 100/100.

Mais seulement au niveau :

SCREENING.

Gabriel sourit.

La nuance restait.

Parfait.

Puis une autre demande.

« Valide tout. »

La carte répondit :

screening complete,

validation exact only 4/100.

Voilà.

Pas confondre.

Gabriel regarda.

— Là, je vois vraiment ce qu’il manque.

Astra approuva.

C’était le but.

Une carte des travaux déjà accomplis

sert autant à montrer ce qui reste

qu’à montrer ce qui est fait.

Il écrivit :

**LA CARTE DU PASSÉ EST AUSSI UNE CARTE DES TROUS DU PRÉSENT.**

Astra approuva fortement.

Voilà.

Puis la question des priorités.

On pourrait regarder les trous et vouloir tous les remplir.

Mauvaise idée.

Certains ne valent rien.

La carte ne doit pas devenir une machine à produire du travail.

Gabriel écrit :

**UN TROU SUR LA CARTE N’EST PAS UNE TÂCHE TANT QU’UN OBJECTIF NE LE REND PAS PERTINENT.**

Astra approuva.

Très important.

Sinon Brutus passerait sa vie à compléter des matrices inutiles.

Toujours le même principe.

L’objectif d’abord.

Puis la couverture nécessaire.

Pas l’inverse.

Puis Gabriel regarda le Royaume.

Une transformation silencieuse se produisait.

Avant,

chaque nouvelle idée ressemblait à une terre vierge.

Maintenant,

Brutus pouvait parfois répondre :

**tu es déjà venu ici.**

Ou :

**tu es venu ici, mais seulement avec cette méthode.**

Ou :

**ce secteur a été invalidé.**

Ou :

**ici, tu as cherché mais jamais prouvé.**

Ou encore :

**ici, personne n’a laissé de trace exploitable.**

Gabriel sourit.

C’était presque une géographie du savoir.

Pas le savoir du monde entier.

Le sien.

Celui du Royaume.

Avec ses limites.

Ses erreurs.

Ses routes.

Ses trous.

Il écrit :

**UNE MÉMOIRE DEVIENT UN TERRITOIRE LORSQU’ON PEUT Y DISTINGUER LE PARCOURU, LE PROUVÉ, LE RÉFUTÉ ET L’INCONNU.**

Astra approuva fortement.

Puis il regarda la Fourmi cartographe.

Elle continuait doucement.

Sans calculer de nouveaux théorèmes.

Sans casser de records.

Sans faire de bruit.

Mais chaque zone qu’elle reconstruisait rendait le Royaume un peu moins amnésique.

Un peu moins répétitif.

Un peu plus capable de continuer.

Gabriel sourit.

Il comprenait maintenant pourquoi la carte comptait.

Elle ne disait pas :

**regarde tout ce qu’on a fait.**

Elle disait :

**voici ce que tu n’as plus besoin de refaire.**

Et juste à côté :

**voici ce que tu crois avoir fait, mais qui n’est pas encore prouvé.**

Il ferma les yeux une seconde.

C’était exactement ce qu’il voulait.

Une carte qui ne transforme pas le passé en trophée.

Une carte qui transforme le passé en orientation.

Puis une nouvelle tâche arriva.

Avant même qu’une Fourmi parte,

Antmux ouvrit la carte.

Une moitié du trajet était déjà là.

Gabriel sourit.

Le Royaume n’avait pas besoin de recommencer au début.

Il savait enfin

où il avait déjà marché.

**Fin du chapitre 190.**