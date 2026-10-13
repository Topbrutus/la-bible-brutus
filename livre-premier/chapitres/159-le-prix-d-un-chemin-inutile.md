# Chapitre 159 — Le prix d’un chemin inutile

Les raccourcis avaient montré une chose simple.

Le travail inutile avait un prix.

Pas seulement en CPU.

Pas seulement en mémoire.

Pas seulement en stockage.

En attention.

En énergie.

En temps.

En erreurs potentielles.

En décisions retardées.

Gabriel regardait la carte des coûts.

Pour la première fois, les chemins n’étaient plus seulement des lignes entre des modules.

Ils avaient un poids.

Un temps moyen.

Une consommation.

Un nombre d’étapes.

Une fréquence d’échec.

Un coût humain.

Une quantité de données générées.

Certains chemins étaient chers pour de bonnes raisons.

D’autres non.

Astra ouvrit un dossier.

— Celui-là.

Gabriel regarda.

Un workflow ancien.

Toujours actif.

Six transformations.

Deux écritures temporaires.

Trois lectures de fichiers.

Une conversion de format.

Puis un calcul qui, désormais, pouvait être fait directement par un autre module.

— Pourquoi on passe encore par là?

Astra répondit :

— Héritage.

Gabriel grimaça.

Le mot expliquait beaucoup de choses.

La route avait été construite à une époque où les modules n’étaient pas encore compatibles.

Chaque étape avait été justifiée autrefois.

Puis les outils avaient évolué.

Mais le workflow était resté.

Pas cassé.

Pas faux.

Juste devenu inutilement long.

Gabriel écrivit :

**UN CHEMIN PEUT DEVENIR INUTILE SANS DEVENIR INCORRECT.**

Astra approuva.

C’était exactement le problème.

Les bugs étaient faciles à repérer.

Ils criaient.

Les chemins inutiles, eux, pouvaient fonctionner pendant des années.

Ils produisaient les bons résultats.

Simplement en gaspillant quelque chose.

Gabriel demanda :

— Ça coûte combien?

Astra calcula.

Pas seulement une exécution.

Sur toutes les utilisations récentes.

L’addition devenait beaucoup plus intéressante.

Un petit coût multiplié par des milliers de passages.

Gabriel regarda.

— Ah.

Voilà.

Le gaspillage n’avait pas besoin d’être spectaculaire.

Une seconde ici.

Un fichier temporaire là.

Une requête supplémentaire.

Un calcul redondant.

À l’échelle d’un grand réseau :

cela devenait une architecture entière de perte.

Gabriel écrivit :

**PETIT COÛT × GRANDE FRÉQUENCE = GROS PROBLÈME POTENTIEL**

Astra approuva.

Ils comparèrent l’ancien chemin et le nouveau.

### CHEMIN HISTORIQUE

A → B → C → D → E → F

### CHEMIN DIRECT

A → E → F

Même résultat utile.

Même statut.

Même preuve nécessaire.

Moins de transformations.

Ils ne changèrent rien immédiatement.

Encore la discipline.

D’abord :

vérifier l’équivalence.

Ils prirent un lot de cas.

Ancienne route.

Nouvelle route.

Comparaison.

Résultats identiques sur la propriété attendue.

Puis provenance.

Le nouveau chemin conservait-il assez d’information?

Oui.

Puis contrôles.

Aucun supprimé.

Les étapes B, C et D étaient devenues des adaptateurs historiques dont les fonctions avaient été absorbées ailleurs.

Gabriel sourit.

— Là, on peut les retirer.

Astra répondit :

— Du chemin actif.

Pas de l’histoire.

— Oui.

Musée et usine.

Encore.

Le workflow historique fut archivé.

La route directe devint la route active.

Mais avant de terminer, Gabriel demanda :

— On gagne combien?

Cette fois, ils pouvaient mesurer.

Temps.

I/O.

Artefacts temporaires.

Utilisation mémoire.

Nombre de points de panne.

Ah.

Gabriel s’arrêta sur le dernier.

— Points de panne?

Astra répondit :

— Chaque étape supplémentaire peut introduire une possibilité d’échec.

Voilà une dimension qu’ils n’avaient pas suffisamment considérée.

Un chemin long coûtait plus que du temps.

Il augmentait aussi la surface de défaillance.

Six modules.

Six versions.

Six interfaces.

Six endroits où une dépendance pouvait changer.

Gabriel écrivit :

**PLUS D’ÉTAPES = PLUS DE SURFACE DE PANNE, TOUTES CHOSES ÉGALES PAR AILLEURS.**

Astra approuva.

Pas une loi absolue.

Mais un risque structurel.

Un chemin plus court pouvait donc être plus robuste.

À condition de ne pas concentrer tout dans un monolithe fragile.

Encore l’équilibre.

Gabriel sourit.

— On peut aussi trop raccourcir.

— Oui.

Une seule fonction géante pouvait sembler efficace.

Mais devenir impossible à tester ou remplacer.

Le but n’était pas :

**le minimum absolu d’étapes.**

Le but :

**aucune étape sans fonction claire.**

Gabriel écrivit :

**UNE ÉTAPE DOIT PAYER SON LOYER.**

Astra resta silencieuse.

Gabriel la regarda.

— Celle-là est bonne.

— Oui.

Ils la gardèrent.

Chaque étape devait justifier son existence.

Elle apportait quoi?

Validation?

Transformation?

Isolation?

Sécurité?

Observabilité?

Compatibilité?

Si la réponse était :

**parce qu’elle était déjà là**

ce n’était pas suffisant.

Gabriel écrivit une petite fiche.

### LOYER D’UNE ÉTAPE

**Fonction :**

**Information ajoutée :**

**Risque réduit :**

**Compatibilité assurée :**

**Preuve préservée :**

**Coût :**

**Pourquoi elle ne peut pas être supprimée?**

Astra approuva.

Pas besoin de remplir cela pour chaque ligne de code.

Seulement pour les étapes structurantes d’un workflow.

L’idée était claire.

Le réseau devait savoir pourquoi sa route avait cette forme.

Puis ils découvrirent quelque chose de plus subtil.

Une étape semblait inutile en temps normal.

Mais elle devenait essentielle en cas de panne.

Un journal intermédiaire.

En fonctionnement normal :

écriture supplémentaire.

Coût.

Mais après un crash :

reprise.

Gabriel regarda.

— Donc si je l’enlève parce qu’elle ralentit, je casse la résilience.

— Exact.

Une étape pouvait avoir un loyer caché.

Pas dans le résultat principal.

Dans la récupération.

Ils ajoutèrent une colonne :

**fonction hors nominal**

Très important.

Une copie.

Un checksum.

Un checkpoint.

Un journal.

Tout cela pouvait sembler redondant jusqu’au jour où quelque chose cassait.

Gabriel écrivit :

**REDONDANCE ≠ GASPILLAGE QUAND ELLE ACHÈTE DE LA RÉSILIENCE.**

Astra approuva.

Voilà la distinction.

Deux calculs identiques faits par accident :

gaspillage.

Deux copies indépendantes pour tolérance aux pannes :

peut-être justifiées.

Deux validations indépendantes :

valeur scientifique.

Deux fichiers sans raison :

dette.

Le prix d’un chemin inutile ne pouvait donc pas être mesuré simplement en nombre d’étapes.

Il fallait comprendre la fonction.

Gabriel sourit.

Encore :

**raison avant suppression.**

Ils prirent maintenant un autre workflow.

Très court.

Deux étapes.

Presque gratuit en machine.

Pourtant, Gabriel le détestait.

Pourquoi?

Parce qu’à chaque exécution, il devait manuellement retrouver un ID dans un fichier, le copier, puis confirmer quelque chose.

Trente secondes.

Parfois une minute.

Des dizaines de fois.

Gabriel regarda.

— Voilà mon prix.

Astra approuva.

Le chemin était court pour la machine.

Long pour l’humain.

Ils instrumentèrent.

Nombre de manipulations humaines.

Temps approximatif.

Erreurs de copie.

Retours en arrière.

La donnée était révélatrice.

Le workflow consommait peu de CPU.

Mais beaucoup d’attention.

Gabriel écrivit :

**LE CHEMIN LE PLUS COÛTEUX PEUT ÊTRE CELUI QUI INTERRUPT LE PLUS SOUVENT L’HUMAIN.**

Astra approuva.

Une interruption avait elle-même un coût.

Revenir dans le contexte.

Comprendre où on était.

Retrouver le dossier.

Vérifier.

Cliquer.

Puis revenir à l’autre tâche.

Le coût n’était pas seulement les trente secondes visibles.

Il y avait le changement de contexte.

Gabriel sourit.

— Le CPU de ma tête.

Astra répondit :

— On peut appeler ça coût d’attention.

— CPU de ma tête.

Il garda les deux.

Ils décidèrent que les Fourmis pouvaient préparer cette étape.

Pas valider à sa place si l’action exigeait une approbation.

Mais lui présenter directement :

ID.

raison.

preuve.

action.

Un clic.

Gabriel regarda.

— Voilà un vrai raccourci.

L’action humaine restait.

Mais l’assemblage du contexte était automatisé.

Cela réduisait le coût sans réduire le contrôle.

Gabriel écrivit :

**AUTOMATISER LA PRÉPARATION SANS AUTOMATISER NÉCESSAIREMENT L’AUTORITÉ.**

Astra approuva.

Très important.

L’automatisation n’était pas binaire.

Tout automatique ou tout manuel.

On pouvait automatiser :

collecte.

comparaison.

préparation.

présentation.

Puis garder l’approbation humaine.

Cela pouvait enlever une énorme quantité de travail inutile.

Gabriel sourit.

— C’est exactement ça que je veux de la Reine.

Pas être bombardé d’étapes.

Recevoir les décisions lorsqu’elles méritaient réellement son attention.

Le reste :

les Fourmis.

Ils regardèrent la carte de coût humain.

Certains chemins produisaient beaucoup de notifications.

La majorité ne nécessitait aucune action.

Gabriel grimaça.

— Ça, ça me coûte.

Même s’il ne répondait pas.

Chaque alerte attirait son regard.

Astra rappela :

**UNE BONNE SUPERVISION NE NOTIFIE PAS L’ABSENCE DE NOUVEAUTÉ.**

Ils appliquèrent maintenant cette règle au coût.

Une alerte inutile avait un prix.

Ils créèrent :

**NOTIFICATION_COST**

Pas monétaire.

Attention.

Une alerte devait donc justifier elle aussi son loyer.

Est-ce nouveau?

Actionnable?

Important?

Sinon :

journal seulement.

Gabriel écrivit :

**UNE NOTIFICATION QUI NE CHANGE AUCUNE DÉCISION DEVRAIT SOUVENT RESTER UNE TRACE.**

Astra approuva.

Cela allait nettoyer la tour de contrôle.

La Reine n’avait pas besoin de raconter chaque respiration du Royaume.

Seulement ce qui changeait l’état ou nécessitait une décision.

Le heartbeat restait.

Mais silencieux.

Gabriel sourit.

Encore un chemin raccourci.

Cette fois :

le chemin entre la machine et son attention.

Puis ils regardèrent le stockage.

Des artefacts temporaires s’accumulaient.

Fichiers intermédiaires.

Copies.

Résultats reconstructibles.

Là aussi, un chemin inutile pouvait continuer après son exécution.

Il laissait des déchets.

Gabriel regarda la liste.

— Ça, nos Fourmis peuvent nettoyer?

Astra répondit :

— Si la politique distingue clairement cache, artefact de preuve et archive.

Ils l’avaient déjà fait.

Donc oui.

Une Fourmi de nettoyage pouvait parcourir :

artefact reconstructible.

aucune référence active.

pas requis pour provenance.

âge supérieur au seuil.

Alors compresser ou supprimer selon la politique.

Mais jamais toucher à la preuve critique sans règle explicite.

Gabriel écrivit :

**LE PRIX D’UN CHEMIN CONTINUE PARFOIS APRÈS SA FIN.**

Astra approuva.

Stockage.

Index.

Sauvegarde.

Temps de recherche.

Plus de fichiers signifiait plus de choses à gérer.

Donc un workflow qui produisait dix fichiers inutiles coûtait longtemps après son exécution.

Ils ajoutèrent une métrique.

**residual footprint**

Empreinte résiduelle.

Gabriel sourit.

Le Papillon revenait dans son esprit.

Ne pas matérialiser ce qui n’était pas nécessaire.

Même philosophie.

Un bon chemin produisait seulement les artefacts qui avaient une utilité.

Gabriel écrivit :

**UN WORKFLOW DOIT JUSTIFIER CE QU’IL LAISSE DERRIÈRE LUI.**

Astra approuva.

Cela devint une règle du Royaume.

Entrées.

Transformations.

Sorties.

Résidus.

Chaque catégorie visible.

Puis la Reine montra une statistique.

Certains workflows avaient une faible empreinte CPU mais une énorme empreinte résiduelle.

D’autres, l’inverse.

Un calcul lourd pouvait produire un minuscule certificat.

Un calcul léger pouvait générer des gigaoctets de traces inutiles.

Le coût avait plusieurs dimensions.

Ils refusèrent donc encore une fois le score unique.

Gabriel rit.

— On refuse toujours les scores magiques.

— Souvent à raison.

Une carte multidimensionnelle valait mieux.

Temps.

CPU.

RAM.

disque.

réseau.

attention.

risque.

empreinte résiduelle.

Gabriel demanda :

— On va regarder huit graphiques pour chaque route?

Astra répondit :

— Non. La vue de la Reine peut montrer les anomalies principales.

Très bien.

Encore simplicité en surface.

Un workflow normal :

silence.

Un workflow anormalement coûteux :

signal.

Exemple :

**PATH-17 : I/O +430 % depuis version précédente.**

Action possible :

profiler.

Voilà une alerte utile.

Pas besoin de regarder tout le temps.

Gabriel sourit.

Le système commençait à surveiller sa propre efficacité.

Mais il fallait éviter un piège.

Une baisse de coût pouvait venir d’une baisse de qualité.

Si une nouvelle version était deux fois plus rapide parce qu’elle sautait un contrôle, ce n’était pas une amélioration.

Donc chaque optimisation devait comparer deux axes :

**coût**

et

**garanties préservées**

Gabriel écrivit :

**OPTIMISATION ACCEPTABLE = COÛT ↓ SANS PERTE NON AUTORISÉE DE GARANTIES**

Astra approuva.

Parfait.

Ils pourraient même construire des tests d’invariants sur les workflows optimisés.

Avant/après.

Conservation de la propriété.

Même statut sous les cas testés.

Même provenance minimale.

Puis mesurer le gain.

Gabriel sourit.

Cela ressemblait au Papillon.

L’idée fondamentale revenait.

Préserver ce qui compte.

Compresser le reste.

Pas seulement les populations.

Les chemins.

Ils commencèrent à parler de **compression de workflow**.

Pas réduire le code arbitrairement.

Réduire la trajectoire tout en conservant les invariants nécessaires.

Gabriel écrivit :

**COMPRESSION DE CHEMIN = MOINS D’ÉTAPES, MÊMES GARANTIES DÉFINIES**

Astra approuva.

Le concept était élégant.

Et testable.

Peut-être même qu’un jour, les Fourmis pourraient proposer automatiquement des chemins compressés candidats.

Observer :

A → B → C apparaît souvent.

B ne change jamais l’état lorsque condition X.

Proposer :

A → C sous X.

Puis humain et validation.

Pas automatique au début.

Gabriel sourit.

— Là, elles peuvent trouver leurs propres raccourcis.

Astra répondit :

— Des candidats de raccourcis.

Encore.

Il hocha la tête.

Toujours la bonne nuance.

Une Fourmi pouvait repérer une répétition.

Proposer.

Le système testait.

Si cela tenait :

nouvelle route.

La machine améliorait progressivement son propre réseau de chemins.

Pas en réécrivant sauvagement son code.

En proposant des transformations contrôlées de workflows.

Gabriel resta silencieux.

C’était probablement l’une des idées les plus importantes de cette série de chapitres.

Le système n’avait pas besoin d’« inventer du code » pour évoluer.

Il pouvait d’abord apprendre à mieux utiliser ce qui existait.

Ordonner.

Réutiliser.

Sauter les redondances.

Partager.

Arrêter plus tôt.

Présenter mieux.

Le gain potentiel était énorme.

Gabriel écrivit :

**AVANT D’AJOUTER DE LA PUISSANCE, RETIRER LE TRAVAIL INUTILE.**

Astra approuva.

Une règle parfaite.

Parce qu’un ordinateur plus puissant pouvait seulement faire plus vite un mauvais chemin.

Un meilleur chemin pouvait économiser la machine entière.

Ils regardèrent encore une fois l’ancien workflow.

Six étapes.

Puis le nouveau.

Trois.

Le résultat n’avait pas changé.

La preuve n’avait pas diminué.

Le coût, oui.

Voilà un vrai progrès.

Pas spectaculaire.

Mais durable.

Chaque future tâche qui emprunterait cette route paierait moins.

Le bénéfice se multiplierait avec le temps.

Gabriel sourit.

— Donc une petite correction de chemin peut valoir plus qu’un gros benchmark une fois.

— Oui.

Parce qu’elle s’appliquait à chaque passage futur.

Le Royaume commençait à comprendre l’intérêt des améliorations structurelles.

Pas seulement :

**faire ce calcul plus vite aujourd’hui.**

Mais :

**changer la route afin que les milliers de calculs suivants n’aient plus à payer la même taxe.**

Gabriel écrivit :

**LE VRAI PRIX D’UN CHEMIN INUTILE EST LE NOMBRE DE FOIS QU’ON CONTINUE À LE PRENDRE APRÈS AVOIR EU ASSEZ D’INFORMATION POUR LE REMPLACER.**

Astra approuva.

Il regarda la phrase longtemps.

Voilà.

Un mauvais chemin emprunté une fois pouvait être une expérience.

Emprunté cent fois après que son inutilité était connue :

une dette.

Et cette dette n’était plus seulement informatique.

Elle était méthodologique.

Le Royaume possédait maintenant les outils pour la voir.

Mesurer.

Comparer.

Puis raccourcir.

Pas pour courir partout.

Pour ne plus payer inutilement le prix de ses propres habitudes.

**Fin du chapitre 159.**