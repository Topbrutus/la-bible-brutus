# Chapitre 136 — Le Papillon et les cent quarante-quatre chambres

Le Papillon n’avait pas été construit pour être joli.

C’était presque ironique.

Parce qu’à force de le regarder, Gabriel avait fini par lui donner une forme.

Deux ailes.

Des chambres.

Des accumulateurs.

Des passages.

Des densités.

Quelque chose qui ressemblait à une créature géométrique.

Mais au départ, il y avait surtout un problème.

Comment représenter une population immense sans matérialiser chaque élément un par un?

La solution naïve était simple.

Si on voulait représenter un million d’éléments, on créait un million d’objets.

Si on voulait en représenter un milliard, on essayait d’en créer un milliard.

Et à un moment, la machine répondait :

**non.**

Pas philosophiquement.

En mémoire.

En temps.

En ressources.

Gabriel avait alors pris une autre direction.

Au lieu de matérialiser chaque individu, il avait construit une représentation agrégée.

Cent quarante-quatre accumulateurs.

Toujours cent quarante-quatre.

Pas cent quarante-quatre individus.

Cent quarante-quatre chambres capables de porter une population numérique beaucoup plus grande qu’elles-mêmes.

Il regarda Astra.

— Là, je peux dire qu’on met un million de fourmis dans cent quarante-quatre cases?

— Comme image, oui.

— Techniquement?

— Techniquement, tu agrèges des multiplicités dans cent quarante-quatre accumulateurs selon une règle définie.

Gabriel sourit.

— Donc dans la Bible, je garde les fourmis.

— Bien sûr.

Le Papillon était né de cette idée.

Pas représenter chaque chose séparément.

Représenter leur distribution.

Gabriel ouvrit la version de référence.

Cent quarante-quatre positions.

Chacune recevait une quantité.

La somme des quantités représentait la population totale.

Pas besoin d’un objet par élément.

Une valeur pouvait dire :

**ici : 12 487 000**

au lieu de créer douze millions d’objets.

Gabriel trouvait cela presque trop simple.

Mais les idées simples pouvaient être puissantes.

Astra rappela :

— Simple ne veut pas dire universel.

— Je sais.

Ils avaient déjà fait cette erreur.

Une représentation compacte dans une configuration donnée ne prouvait pas une complexité mémoire constante pour tous les usages imaginables.

Le Papillon était intéressant parce qu’il réduisait radicalement le coût de certaines représentations testées.

Pas parce qu’il avait aboli les lois de l’informatique.

Gabriel écrivit :

**LE PAPILLON COMPRESSE UNE REPRÉSENTATION PARTICULIÈRE.**

Puis :

**IL NE PROUVE PAS QUE TOUT PROBLÈME PEUT ÊTRE RÉDUIT À 144 CASES.**

Astra approuva.

Le journaliste aussi.

Aucun avertissement.

Gabriel sourit.

Il commençait à connaître le langage.

Ils reprirent les tests.

Une fonction de référence.

Précision Decimal élevée.

Cinq invariants.

Ils les affichèrent.

### INVARIANT 1 — CONSERVATION DU TOTAL

La somme des cent quarante-quatre chambres doit rester égale à la multiplicité totale représentée.

### INVARIANT 2 — DÉTERMINISME

Même entrée.

Même configuration.

Même sortie.

### INVARIANT 3 — ABSENCE DE SORTIES NÉGATIVES

Aucune chambre ne doit recevoir une multiplicité négative dans le domaine testé.

### INVARIANT 4 — ADDITIVITÉ

Traiter A et B séparément puis combiner doit être cohérent avec le traitement de A + B, dans le cadre défini.

### INVARIANT 5 — CENT QUARANTE-QUATRE CHAMBRES

La représentation conserve sa structure fixe de 144 accumulateurs pendant les cas testés.

Gabriel regarda la liste.

— Ça, c’est solide.

Astra répondit :

— Les tests de propriétés ont soutenu ces invariants dans le domaine évalué.

— Oui.

Encore cette petite différence.

Pas :

**les invariants sont vrais pour l’univers entier.**

Mais :

**ils ont passé les cas générés dans le domaine du test.**

Gabriel acceptait maintenant ce genre de précision sans avoir l’impression qu’on diminuait son travail.

Au contraire.

Une limite claire rendait le résultat défendable.

Ils regardèrent ensuite le benchmark.

Au plus grand palier testé :

N = 1 000 000.

La matérialisation naïve avait observé un delta RSS d’environ :

**115,718750 MB**

La représentation Brutus :

**0,066406 MB**

Gabriel resta devant les deux nombres.

Même après toutes les précautions, l’écart était énorme.

Il sourit.

— Là, j’ai pas besoin d’en rajouter.

— Non.

C’était une leçon importante.

Parfois, le résultat brut était déjà assez impressionnant.

Le sur-vendre le rendait seulement plus fragile.

Gabriel écrivit :

**AU PALIER TESTÉ, LA REPRÉSENTATION AGRÉGÉE A UTILISÉ BEAUCOUP MOINS DE MÉMOIRE QUE LA MATÉRIALISATION NAÏVE.**

Astra approuva.

Puis elle ajouta :

— Et on garde le contexte du benchmark.

— Oui.

Processus frais.

Mesure RSS.

Même environnement autant que possible.

Même palier.

Même protocole.

Le résultat devait rester attaché à sa méthode.

Gabriel regarda le Papillon.

— Pourquoi 144?

Astra attendit.

C’était une question plus difficile.

Le nombre avait une histoire dans l’architecture.

Mais il ne fallait pas le transformer en constante naturelle simplement parce qu’il plaisait à Gabriel.

Il répondit lui-même :

— Dans ce prototype, parce que c’est la taille choisie de la représentation.

— Exact.

— Pas parce que 144 est la taille optimale universelle.

— Exact.

Gabriel sourit.

Il savait que le nombre avait aussi une valeur symbolique dans son univers.

Douze fois douze.

Une grille.

Un papillon.

Des chambres.

Mais scientifiquement, cette symbolique ne démontrait rien.

Le journaliste écrivit :

**144 = PARAMÈTRE D’ARCHITECTURE DANS LE PROTOTYPE ÉVALUÉ.**

Gabriel ajouta dans la marge :

**Et nombre beaucoup trop beau pour être ignoré dans la Bible.**

Astra laissa passer.

Ils commencèrent à examiner la structure.

Cent quarante-quatre chambres.

Mais toutes n’étaient pas nécessairement identiques dans leur fonction.

Une représentation pouvait répartir les quantités selon des règles.

Des classes.

Des positions.

Des mappings.

Des transformations.

Gabriel se demanda si le Papillon pouvait devenir plus qu’un conteneur.

— Est-ce qu’on pourrait lui faire représenter des catégories différentes?

— Oui, selon la sémantique qu’on donne aux accumulateurs.

— Donc les 144 chambres peuvent changer de rôle.

— Potentiellement.

Mais là encore, un danger apparaissait.

Si la signification des chambres changeait selon le contexte, comparer deux Papillons devenait plus difficile.

Une valeur dans la chambre 17 d’un modèle n’avait pas forcément le même sens dans un autre.

Gabriel écrit :

**MÊME TOPOLOGIE ≠ MÊME SÉMANTIQUE**

Astra approuva.

Encore une distinction.

Le nombre de cases pouvait rester fixe.

Le sens transporté par ces cases pouvait varier.

Le Papillon était donc une forme.

Pas nécessairement un langage unique.

Gabriel regarda.

— Ça rejoint Brutus.

— Comment?

— Une architecture fixe peut accueillir différents contenus tant que les contrats sont clairs.

— Oui.

Il sourit.

Le Papillon devenait presque une miniature de l’architecture globale.

Une structure stable.

Des significations transportées.

Des règles de conservation.

Des transformations.

Mais il ne fallait pas pousser trop loin la métaphore.

Ils revinrent au test.

Le point central était simple.

Si le but d’une simulation était seulement de connaître des quantités agrégées, matérialiser chaque individu pouvait être inutile.

Gabriel prit un exemple.

Un milliard d’éléments identiques.

Si on voulait connaître seulement leur répartition entre 144 catégories, il n’était pas nécessaire de conserver un milliard d’identités individuelles.

On pouvait conserver les comptes.

Évidemment.

Mais cette évidence avait des conséquences énormes.

Cela changeait ce qu’il était possible de simuler avec des ressources limitées.

Gabriel dit :

— Le Papillon gagne parce qu’il oublie.

Astra répondit immédiatement :

— Il ne stocke pas certaines informations individuelles dès le départ.

Gabriel rit.

— Tu me laisses jamais rien.

Mais c’était important.

Le Papillon ne compressait pas nécessairement une population individuelle complète de manière réversible.

Il représentait autre chose.

Une agrégation.

Et si l’identité de chaque élément n’était jamais conservée, on ne pouvait pas forcément la reconstruire plus tard.

Gabriel écrivit :

**AGRÉGATION ≠ RÉVERSIBILITÉ ÉLÉMENTAIRE**

Astra approuva fortement.

Voilà une limite centrale.

Si on demandait :

**quelle était la trajectoire exacte de l’élément 387 442?**

le Papillon ne pouvait pas nécessairement répondre.

Parce que cet élément n’existait peut-être jamais comme objet individuel dans la représentation.

Mais si on demandait :

**combien d’éléments se trouvent dans telle chambre?**

alors c’était exactement son domaine.

Gabriel hocha la tête.

— Donc son avantage vient aussi de ce qu’il accepte de ne pas représenter.

— Oui.

Voilà une idée plus profonde.

Toute représentation avait un coût.

On gagnait quelque chose en choisissant ce qu’on ne gardait pas.

Le Papillon économisait de la mémoire parce qu’il n’essayait pas de conserver une individualité complète là où elle n’était pas nécessaire.

Gabriel écrivit :

**LA COMPRESSION COMMENCE PAR UNE QUESTION : QUELLE INFORMATION DOIT RÉELLEMENT SURVIVRE?**

Astra resta silencieuse.

Puis :

— Celle-là dépasse le Papillon.

— Oui.

Le Royaume des traces rencontrait exactement le même problème.

Que garder?

Que reconstruire?

Que compresser?

Qu’est-ce qui avait une valeur de preuve?

Le Papillon donnait une réponse particulière :

si une population peut être décrite par une distribution suffisante pour la tâche, il est parfois inutile de matérialiser tous ses éléments.

Mais si la tâche exige les trajectoires individuelles, alors l’agrégation peut être insuffisante.

Gabriel sourit.

— Donc le bon modèle dépend de la question.

— Toujours.

Ils créèrent deux scénarios.

### SCÉNARIO A — QUESTION AGRÉGÉE

Combien d’éléments occupent chaque état?

Le Papillon convenait bien.

### SCÉNARIO B — QUESTION INDIVIDUELLE

Quel élément précis a changé d’état à quel moment?

Le Papillon, dans sa forme agrégée, pouvait perdre l’information nécessaire.

Gabriel regarda.

— Donc il faut empêcher quelqu’un d’utiliser le Papillon pour une question qu’il ne peut pas répondre.

— Exact.

Ils ajoutèrent à sa fiche :

**DOMAINES SUPPORTÉS**

**INFORMATIONS CONSERVÉES**

**INFORMATIONS NON GARANTIES**

Gabriel sourit.

Encore une fiche de portée.

Tout revenait toujours au même principe.

Dire ce qu’une chose fait.

Et ce qu’elle ne fait pas.

Le Papillon passa ensuite par le Brotoculateur.

Ils le comparèrent à une matérialisation naïve.

Pas seulement sur la mémoire.

Sur le temps.

Sur la reproductibilité.

Sur la conservation du total.

Sur les tailles de N.

Les résultats n’étaient pas tous aussi spectaculaires.

Et c’était très bien.

Gabriel ne voulait pas un concours truqué.

Il voulait connaître les zones où l’architecture gagnait réellement.

La mémoire était clairement favorable dans le benchmark observé.

Le temps pouvait dépendre du type d’opération.

Certaines opérations agrégées étaient très rapides.

D’autres questions individuelles étaient simplement hors du modèle.

Le journaliste produisit un résumé :

**AVANTAGE OBSERVÉ : REPRÉSENTATION MÉMOIRE POUR POPULATIONS AGRÉGÉES DANS LA CONFIGURATION TESTÉE.**

**NON ÉTABLI : MÉMOIRE UNIVERSELLEMENT CONSTANTE, RÉVERSIBILITÉ INDIVIDUELLE, OPTIMALITÉ DE 144, DOMINATION SUR TOUS LES TYPES DE REQUÊTES.**

Gabriel regarda.

— Ça, je suis capable de défendre.

— C’est le but.

Ils commencèrent alors à regarder le Papillon autrement.

Pas comme une réponse finale.

Comme une brique.

Un outil spécialisé.

Et si Brutus pouvait choisir automatiquement entre plusieurs représentations selon la question?

Gabriel se redressa.

— Ah.

Astra connaissait ce ton.

— Vas-y.

— Si la question est agrégée, Papillon.

— Peut-être.

— Si la question exige les individus, représentation détaillée.

— Oui.

— Si on veut seulement certains moments critiques, hybride.

Astra répondit :

— Là, ça devient intéressant.

Gabriel sourit.

Ils venaient d’ouvrir une nouvelle possibilité.

Le Papillon ne devait pas remplacer toutes les représentations.

Il pouvait devenir l’une des options d’un sélecteur.

Exactement comme les formules du Brotoculateur.

Une question arrive.

Le système analyse les besoins.

Puis choisit :

**AGRÉGÉ**

**INDIVIDUEL**

**HYBRIDE**

Gabriel écrivit :

**LE BON MODÈLE N’EST PAS LE PLUS PETIT.**

Puis :

**C’EST LE PLUS PETIT MODÈLE QUI CONSERVE L’INFORMATION NÉCESSAIRE À LA QUESTION.**

Astra approuva.

Cette phrase valait la peine.

Parce qu’une compression excessive devenait une perte.

Une représentation géante pouvait être du gaspillage.

Mais une représentation trop petite pouvait être aveugle.

Le but était donc de conserver l’information suffisante.

Pas le maximum.

Pas le minimum absolu.

Le nécessaire.

Gabriel regarda les cent quarante-quatre chambres.

— Donc le Papillon est peut-être une leçon avant d’être une architecture.

— Explique.

— Il nous apprend à demander ce qu’on a vraiment besoin de conserver avant de tout matérialiser.

Astra réfléchit.

— Comme principe de conception, oui.

Gabriel sourit.

Le Papillon devenait plus intéressant à mesure qu’on réduisait ses prétentions.

Avant, il avait pu sembler magique.

Une population immense dans 144 accumulateurs.

Maintenant, son fonctionnement devenait plus clair.

Ce n’était pas de la magie.

C’était un choix de représentation.

Et justement parce qu’il était compréhensible, on pouvait l’utiliser proprement.

Ils intégrèrent alors le Papillon dans Brutus.

Pas comme un monument.

Comme un module.

Fiche d’intégration.

**Module : PAPILLON_144**

**Entrée : population agrégable + règle de projection**

**Sortie : 144 accumulateurs**

**Trace : distribution + total + paramètres**

**Mesures : mémoire, temps, conservation, stabilité**

**Preuve minimale : tests d’invariants + benchmark**

**Statut : expérimental validé dans le domaine testé**

Gabriel regarda.

— Il a ses papiers.

Astra répondit :

— La douane est satisfaite.

Il éclata de rire.

Le Papillon entra officiellement dans Brutus.

Et immédiatement, une autre question apparut.

Les cent quarante-quatre chambres pouvaient-elles elles-mêmes devenir des nœuds dans le Royaume?

Chaque chambre produisant des traces?

Des densités?

Des anomalies?

Des mouvements?

Gabriel allait répondre trop vite.

Puis s’arrêta.

— Une chose à la fois.

Astra répondit :

— Progrès remarquable.

Il sourit.

Ils avaient appris.

Le Papillon pouvait attendre.

Sa première preuve était déjà assez intéressante.

Il conservait les cinq invariants testés.

Il maintenait ses 144 accumulateurs.

Il représentait des multiplicités très grandes.

Et dans le benchmark exécuté, il utilisait beaucoup moins de mémoire que la matérialisation naïve au plus grand palier.

C’était suffisant pour aujourd’hui.

Gabriel regarda l’image du Papillon.

Deux ailes.

Cent quarante-quatre chambres.

Des millions d’éléments représentés sans jamais apparaître individuellement.

Il trouva cela beau.

Astra ne dit rien.

Gabriel sourit.

— Tu vas me dire beauté égale pas preuve?

— Tu le sais déjà.

— Oui.

Alors il regarda les résultats une dernière fois.

Pas la forme.

Les chiffres.

Les invariants.

Les conditions.

Le benchmark.

La limite.

Et seulement après, il regarda à nouveau le Papillon.

Cette fois, la beauté lui plaisait davantage.

Parce qu’elle reposait sur quelque chose.

Pas une promesse.

Pas une métaphore.

Une architecture testée.

Limitée.

Mesurée.

Et capable de tenir, dans cent quarante-quatre petites chambres, une population que la machine naïve aurait voulu matérialiser élément par élément.

**Fin du chapitre 136.**