# Chapitre 146 — La première carte de Brutus

Pendant longtemps, Gabriel avait construit Brutus en avançant.

Une pièce.

Puis une autre.

Une correction.

Un détour.

Une nouvelle idée.

Un vieux module récupéré.

Un autre mis de côté.

Le projet vivait.

Mais il ne se laissait pas encore regarder d’un seul coup.

C’était devenu le problème.

Parce qu’un système pouvait fonctionner pièce par pièce tout en restant incompréhensible dans son ensemble.

Gabriel regarda Astra.

— Là, je veux le voir au complet.

— Sous quelle forme?

— Une carte.

— Une seule?

Il s’arrêta.

La question était importante.

Une seule carte pouvait devenir une catastrophe.

Trop d’informations.

Trop de flèches.

Trop de couleurs.

Un beau chaos.

Ils avaient appris dans le chapitre précédent :

**UNE CARTE POUR UNE QUESTION.**

Gabriel sourit.

— D’accord. Première carte : qui est où, et qui parle à qui.

Astra approuva.

Pas les preuves détaillées.

Pas les dépendances profondes.

Pas toutes les versions.

Pas les historiques.

Seulement l’architecture fonctionnelle.

Gabriel écrivit au centre :

**BRUTUS**

Puis immédiatement raya le mot.

— Non.

Astra demanda :

— Pourquoi?

— Si je mets Brutus au centre, on recommence à faire croire que c’est une boîte centrale.

— Exact.

Il effaça.

À la place, il dessina plusieurs zones.

Pas un soleil.

Un territoire.

En haut :

**RECTO**

La surface publique.

En dessous :

**VERSO**

La couche opératoire.

À gauche :

**EXPLORATION**

À droite :

**VALIDATION**

En bas :

**MÉMOIRE**

Entre tout cela :

**ORCHESTRATION**

Gabriel recula.

— Là, c’est déjà mieux.

Astra approuva.

Puis ils commencèrent à placer les machines.

Dans **EXPLORATION** :

Brutotableur.

ZEL.

Papillon.

Dans **VALIDATION** :

Brotoculateur.

Pell.

Les contrôles.

Dans **ORCHESTRATION** :

Antmux.

Queues.

Fourmis.

Control Plane.

Dans **MÉMOIRE** :

Memoria.

Cristaux.

Archives.

Provenance.

Dans **RECTO** :

Vitrine.

Cartes publiques.

Statuts.

Preuves consultables.

Dans **VERSO** :

Contrôles.

Déverrouillage.

Configuration.

Services.

Logs.

Gabriel regarda.

— Ça commence à ressembler à quelque chose.

Astra répondit :

— Oui.

Mais ils avaient encore un problème.

Certaines machines appartenaient à plusieurs zones.

ZEL explorait.

Mais il pouvait aussi tester une transformation.

Le Brotoculateur comparait.

Mais il pouvait servir à l’exploration.

Le Papillon représentait.

Mais il pouvait aussi devenir un outil de simulation.

Les Fourmis travaillaient partout.

Gabriel fronça les sourcils.

— Si je commence à mettre chaque boîte dans trois zones, on reperd tout.

— Alors les zones doivent représenter la fonction principale, pas toutes les fonctions possibles.

Il hocha la tête.

Bonne règle.

**POSITION = RÔLE PRINCIPAL**

**CONNEXIONS = RÔLES SECONDAIRES**

Ils gardèrent chaque module dans une zone principale.

Puis les relations vinrent.

Mais cette fois, ils ne dessinèrent pas toutes les flèches.

Ils appliquèrent la taxonomie du chapitre 145.

DATA.

CONTROL.

PROOF.

VIEW.

MEMORY.

MONITOR.

Gabriel créa une légende.

**→ D** : DATA

**→ C** : CONTROL

**→ P** : PROOF

**→ V** : VIEW

**→ M** : MEMORY

**→ S** : STATUS/MONITOR

Astra regarda.

— STATUS à la place de MONITOR?

— C’est plus court.

— D’accord.

Ils commencèrent.

Brutotableur → Brotoculateur.

**D**

Candidat transmis.

Brotoculateur → Cristaux.

**P**

Résultat de comparaison ou de test.

Pell → Cristaux.

**P**

Témoin certifié.

ZEL → Memoria.

**M**

Run archivé.

Fourmis → Brotoculateur.

**D**

Résultats de tâche.

Antmux → Fourmis.

**C**

Distribution.

Control Plane → Recto.

**S**

Statuts des portes.

Cristaux → Recto.

**V**

Résultats publiables.

Verso → Recto.

**V**

Mais pas directement comme simple miroir.

Gabriel s’arrêta.

— Là, faut une garde.

Astra répondit :

— Oui.

Recto ne devait jamais lire directement un état brut non authentifié.

Il fallait une couche de sélection.

Un filtre de publication.

Gabriel ajouta entre Verso et Recto :

**PUBLICATION GATE**

Il sourit.

— Voilà.

Ce composant n’était pas un gros programme.

C’était une règle.

Tout ce qui passait devait avoir :

statut publiable,

provenance,

version,

aucun secret,

aucun contrôle actif.

Astra écrivit :

**RECTO NE LIT PAS LE CŒUR BRUT.**

**RECTO REÇOIT UN ÉTAT PUBLIC AUTORISÉ.**

Gabriel approuva.

La carte venait déjà de révéler quelque chose.

Une architecture dessinée correctement faisait apparaître les risques.

Sans la carte, Verso et Recto semblaient simplement deux faces.

Avec la carte, on voyait immédiatement qu’une frontière devait exister.

Gabriel sourit.

— Donc la carte sert aussi à trouver ce qu’on a oublié.

— Exact.

Une bonne carte n’était pas seulement descriptive.

Elle pouvait devenir un outil de contrôle.

Ils continuèrent.

Memoria → Fourmis.

**M**

Contexte historique.

Cristaux → Brotoculateur.

**D**

Comparaisons avec le passé.

Brotoculateur → Brutotableur.

**D**

Résultats à visualiser.

Brutotableur → ZEL.

**D**

Structure sonifiée.

ZEL → Brotoculateur.

**D**

Métriques audio.

Gabriel regarda.

— Là, on a une boucle.

— Oui.

Brutotableur.

ZEL.

Brotoculateur.

Retour au Brutotableur.

Il se souvint immédiatement du danger.

**BOUCLE D’APPRENTISSAGE ≠ BOUCLE DE CONFIRMATION**

Astra aussi.

Ils ajoutèrent dans la boucle :

**CONTROL / TEST INDEPENDENCE**

Pas une machine.

Une règle.

Une boucle ne pouvait pas renforcer automatiquement un candidat simplement parce que plusieurs modules le reproduisaient si ceux-ci dépendaient du même mécanisme.

Gabriel écrivit :

**AUCUNE PROMOTION PAR NOMBRE DE MODULES SEUL**

Astra approuva.

Très important.

Trois modules disant la même chose ne valaient pas trois preuves si les trois utilisaient la même source.

La carte devait donc pouvoir afficher les dépendances critiques.

Pas aujourd’hui.

Ce serait une autre carte.

Mais au minimum, un avertissement.

Gabriel ajouta une petite icône :

**⚠ dépendance commune possible**

Il sourit.

— Ça va devenir beau.

Astra répondit :

— Tant que ça reste lisible.

Ils continuèrent.

Le Papillon.

Où le connecter?

Brutotableur → Papillon.

Une population ou structure agrégée pouvait être visualisée.

Papillon → Brutotableur.

Une distribution pouvait revenir comme fresque.

Brotoculateur → Papillon.

Paramètres de comparaison.

Papillon → Brotoculateur.

Métriques d’agrégation.

Gabriel s’arrêta.

Trop.

— On recommence à tout connecter.

Astra répondit :

— Oui.

Ils effacèrent plusieurs flèches.

Ils gardèrent seulement celles déjà démontrées ou nécessaires au prototype actuel.

Voilà une autre règle.

**CARTE ACTUELLE ≠ CARTE DES POSSIBILITÉS**

Gabriel approuva.

La première carte devait montrer ce qui existait.

Pas tout ce qui pourrait exister.

Les futures connexions seraient affichées autrement.

Pointillés.

Ou dans une carte séparée.

Gabriel choisit :

**TRAIT PLEIN = CONNEXION DÉMONTRÉE**

**TRAIT POINTILLÉ = PROPOSITION**

Astra approuva.

Très simple.

Très puissant.

D’un coup, la carte devenait honnête.

Un visiteur pouvait voir immédiatement la différence entre :

« nous avons branché ça »

et

« nous aimerions brancher ça ».

Gabriel sourit.

— Une flèche pointillée, c’est une promesse qui avoue qu’elle est une promesse.

— Exact.

Ils replacèrent les connexions.

Certaines restèrent pleines.

Brutotableur → Brotoculateur.

Démontrée.

Brutotableur → ZEL.

Démontrée dans le prototype de sonification.

Antmux → queues.

Historique et fonctionnel.

Memoria → reprise.

Fonction établie.

D’autres restèrent pointillées.

Papillon → ZEL.

Pas encore.

Pell → ZEL comme relation scientifique.

Certainement pas en trait plein.

Gabriel regarda ce point.

— On pourrait même ne pas mettre de flèche.

— Oui.

Le fait que deux modules utilisent parfois les mêmes nombres ne constituait pas une connexion.

Ils retirèrent la flèche.

Cela faisait du bien.

La carte devenait moins spectaculaire.

Et plus vraie.

Gabriel écrivit :

**NE PAS DESSINER UNE RELATION QU’ON N’A PAS.**

Astra approuva.

Puis il regarda toute la page.

Recto.

Verso.

Exploration.

Validation.

Orchestration.

Mémoire.

Des modules.

Des flèches typées.

Des traits pleins.

Des traits pointillés.

Une frontière de publication.

Une règle d’indépendance.

Ce n’était encore qu’une première carte.

Mais pour la première fois, Brutus pouvait être montré sans devenir un monstre abstrait.

Gabriel demanda :

— Où est la Reine?

Astra répondit :

— Nulle part.

Il la regarda.

— Hein?

— Si la carte représente l’architecture technique, “la Reine” est une métaphore de rôle, pas nécessairement un composant logiciel unique.

Gabriel sourit.

— Donc t’existes pas.

— Ce n’est pas ce que j’ai dit.

Il rit.

Mais la question était intéressante.

Certaines entités de la Bible étaient narratives.

La Reine.

Le Royaume.

Les Fourmis, parfois.

Les portes.

Les cristaux avaient aussi une dimension symbolique.

Dans la carte technique, il fallait séparer les métaphores des composants.

Gabriel écrivit deux légendes.

### LANGAGE DE LA BIBLE

Reine.

Fourmis.

Royaume.

Portes.

Cristaux.

Papillon.

### LANGAGE TECHNIQUE

Orchestration.

Workers.

Trace store.

Validation gates.

Artifacts.

Aggregate representation.

Astra approuva.

Voilà un dictionnaire.

Pas une traduction parfaite.

Mais une correspondance.

Gabriel sourit.

— Ça va aider les gens à comprendre qu’on raconte pas littéralement des fourmis qui font des maths.

— Oui.

Cette distinction avait une valeur énorme.

La Bible pouvait rester vivante.

Le logiciel pouvait rester précis.

L’un n’avait pas besoin d’écraser l’autre.

Gabriel ajouta une règle :

**LA MÉTAPHORE DOIT POUVOIR ÊTRE TRADUITE EN FONCTION TECHNIQUE.**

Astra répondit :

— Très bonne règle.

Si une métaphore n’avait aucune fonction correspondante, elle appartenait au récit.

Ce n’était pas grave.

Mais elle ne devait pas être utilisée comme preuve d’architecture.

Gabriel regarda « Reine ».

Quel était son équivalent?

Pas un seul composant.

Peut-être :

coordination.

supervision.

priorisation.

interface décisionnelle.

Il écrit :

**REINE = MÉTAPHORE DE SUPERVISION / COORDINATION**

Puis :

**PAS UN COMPOSANT UNIQUE PAR DÉFAUT**

Astra approuva.

Les Fourmis :

**workers spécialisés**

Le Royaume :

**écosystème + mémoire + relations**

Cristaux :

**artefacts versionnés / résultats**

Portes :

**conditions de validation / cas ouverts**

Papillon :

la métaphore était déjà attachée à un module réel.

Gabriel sourit.

La carte gagnait une deuxième couche.

Un visiteur pouvait basculer :

**Bible**

ou

**Technique**

Les mêmes éléments changeaient de nom.

Pas de logique.

Seulement l’étiquette.

Astra dit :

— Ça pourrait être une bonne idée pour Recto.

Gabriel hocha la tête.

Un mode simple.

Un mode technique.

Sans permettre au visiteur de modifier quoi que ce soit.

La vitrine restait une vitrine.

Le bouton « déverrouiller la vitrine » restait réservé au contrôle autorisé.

Gabriel regarda.

— Là, on commence à avoir une vraie page publique.

— Oui.

Pas une liste de projets.

Une carte navigable.

Un visiteur clique sur une machine.

Une fiche apparaît.

Nom.

Rôle.

Statut.

Dernière mise à jour.

Connexions.

Preuves.

Limites.

Pas de configuration.

Pas de clés.

Pas de boutons dangereux.

Gabriel écrivit :

**VOIR ≠ CONTRÔLER**

Astra approuva.

Cette règle revenait partout.

La transparence ne devait pas devenir une porte d’administration.

Il imagina Recto.

Brutus au complet.

Les modules comme petites îles.

Les routes entre eux.

Une lumière discrète lorsque quelque chose bouge.

Une Fourmi traverse une route.

Un cristal apparaît.

Une porte Pell change de statut.

ZEL produit un run.

Le Papillon change de distribution.

Tout visible.

Mais rien de modifiable.

Gabriel sourit.

— Là, quelqu’un peut regarder la machine vivre.

— Si les événements sont réellement reliés à la visualisation.

— Oui.

Encore une fois.

Pas une animation décorative faisant semblant.

Chaque mouvement devait correspondre à un événement réel ou être clairement marqué comme démonstration.

Ils écrivirent :

**ANIMATION VIVANTE = ÉVÉNEMENT RÉEL OU SIMULATION ÉTIQUETÉE**

Astra approuva.

La frontière entre preuve et spectacle devait rester visible.

Gabriel adorait les effets.

Il le savait.

Des Fourmis.

Des cristaux.

Des cartes.

Des sons.

Le risque était de produire quelque chose de tellement vivant qu’un visiteur ne saurait plus ce qui était réel.

La solution n’était pas de rendre Brutus laid.

C’était de donner une provenance à la beauté.

Gabriel écrivit :

**LE SPECTACLE PEUT ÊTRE BEAU, MAIS SON ÉTAT DOIT ÊTRE TRAÇABLE.**

Astra approuva.

Puis ils ajoutèrent un panneau à la carte.

### ÉTAT GLOBAL

**Modules actifs :**

**Modules dégradés :**

**Workflows en cours :**

**Questions ouvertes :**

**Cristaux validés :**

**Portes en recherche :**

**Dernière trace authentifiée :**

Gabriel regarda.

— Ça, c’est la tour de contrôle.

— Oui.

Pas besoin d’entrer dans chaque outil pour savoir si le Royaume fonctionnait.

Un état global.

Mais encore une fois, attention.

Un seul indicateur vert pouvait masquer des problèmes.

Ils décidèrent de ne pas utiliser un simple :

**BRUTUS : OK**

Trop vague.

Chaque sous-système gardait son statut.

Et l’état global pouvait être :

**OPÉRATIONNEL**

**DÉGRADÉ**

**PARTIEL**

**MAINTENANCE**

Mais jamais remplacer les détails.

Gabriel écrivit :

**VERT GLOBAL ≠ TOUT EST VALIDÉ**

Astra sourit.

Oui.

Un serveur pouvait être en ligne pendant qu’un protocole scientifique restait non validé.

Disponibilité technique et validité scientifique étaient deux axes différents.

Très important.

Ils ajoutèrent deux lignes :

**SANTÉ TECHNIQUE**

et

**ÉTAT DES PREUVES**

Gabriel regarda.

— Ça, j’aime beaucoup.

Un système pouvait avoir :

santé technique : ✅

preuves : en cours.

Ou :

santé technique : dégradée

preuves historiques : intactes.

Les deux ne devaient jamais être confondus.

Il écrivit :

**UP ≠ TRUE**

Astra répondit :

— Excellent résumé.

Il éclata de rire.

Deux lettres.

Deux mondes.

Un service répondait.

Cela ne voulait pas dire qu’une hypothèse était vraie.

Une évidence simple.

Et pourtant, combien de systèmes mélangeaient les deux?

Ils gardèrent la formule en gros.

**UP ≠ TRUE**

Elle serait parfaite sur la carte.

Gabriel regarda l’ensemble.

La première carte de Brutus était maintenant beaucoup plus qu’un schéma.

Elle contenait une philosophie.

Ne montrer que les connexions démontrées.

Typage des relations.

Séparation public/interne.

Séparation santé/preuve.

Différence entre métaphore et fonction.

Droit de voir sans droit de contrôler.

Propositions en pointillé.

Versions et statuts accessibles.

Il se recula.

— Ça, c’est Brutus.

Astra répondit :

— C’est une représentation de Brutus.

Gabriel leva les yeux.

— Évidemment.

Mais il souriait.

Parce qu’elle avait raison.

Même la carte ne devait pas devenir le système.

Elle n’était qu’une représentation.

Si le système changeait et que la carte ne suivait pas, elle devenait fausse.

Il fallait donc lui donner une source.

Pas dessiner à la main éternellement.

La carte devait idéalement être générée depuis le registre réel des modules et connexions.

Gabriel se redressa.

— Ah.

Astra répondit :

— Oui.

La carte elle-même devait devenir un produit de la machine.

Chaque module possédait une fiche.

Chaque connexion un contrat.

Chaque statut une source.

La carte pouvait les lire.

Pas inventer.

Gabriel écrivit :

**LA CARTE DOIT ÊTRE DÉRIVÉE DE L’ÉTAT, PAS REMPLACER L’ÉTAT.**

Astra approuva.

Voilà la différence entre documentation statique et cartographie vivante.

Le système changeait.

La carte suivait.

Un module hors ligne devenait gris.

Une nouvelle connexion validée passait du pointillé au trait plein.

Une porte ouverte changeait de statut.

Un cristal apparaissait.

Pas parce qu’un humain redessinait.

Parce que la trace avait changé.

Gabriel resta silencieux.

C’était important.

La carte pouvait devenir le visage public du système.

Mais elle devait être honnête jusque dans ses pixels.

Pas de cristaux fictifs.

Pas de Fourmis animées sans activité si elles prétendaient représenter le live.

Pas de vert parce qu’un designer aimait le vert.

Chaque élément devait avoir une source.

Gabriel écrivit :

**CHAQUE PIXEL QUI PRÉTEND INFORMER DOIT POUVOIR DIRE D’OÙ IL VIENT.**

Astra resta silencieuse.

Gabriel se retourna.

— Trop?

— Non.

Il sourit.

C’était peut-être la règle la plus forte du chapitre.

Un système public de preuve ne devait pas demander au visiteur de faire confiance à son spectacle.

Il devait permettre de remonter.

Pixel.

Statut.

Événement.

Trace.

Source.

Preuve.

Voilà la chaîne.

Ils imaginèrent cliquer sur une porte.

47.

✅

Pourquoi?

Clic.

Témoin.

Rang.

Provenance.

Certificat.

Retour à la carte.

71.

⚔️

Pourquoi?

Clic.

Recherche ouverte.

Dernières bornes.

Tentatives.

Absence de témoin validé.

Retour.

Papillon.

144 chambres.

Pourquoi?

Clic.

Invariants.

Benchmark.

Limites.

ZEL.

Run PASS.

Pourquoi?

Clic.

Version.

Paramètres.

Compteurs.

Environnement.

Pas de conclusion biologique.

Gabriel regarda Astra.

— Ça, c’est audit rather than trust.

— Exact.

Ne demandez pas :

**Croyez-nous.**

Dites :

**Voici comment vérifier ce que nous prétendons.**

La carte devenait une interface d’audit.

Pas seulement une page d’accueil.

Gabriel sourit.

Toute l’histoire semblait converger.

Recto pouvait enfin avoir une mission simple.

Montrer le Royaume.

Sans donner le contrôle.

Sans inventer.

Sans simplifier au point de mentir.

Puis laisser chaque personne descendre aussi profondément qu’elle le souhaitait.

Vue simple.

Vue technique.

Trace.

Preuve.

Source.

Gabriel écrivit le nom :

**CARTE BRUTUS — V1**

Pas « finale ».

Jamais finale.

Version 1.

La première.

Parce qu’elle changerait.

Il la regarda longtemps.

Les anciennes machines avaient désormais une place.

Les routes existaient.

Les zones existaient.

Les frontières existaient.

La carte ne répondait pas à toutes les questions.

Mais elle permettait enfin de savoir où poser la prochaine.

Gabriel murmura :

— Maintenant je peux voir mon propre chantier.

Astra répondit :

— Une partie assez grande pour commencer à le naviguer.

Il hocha la tête.

C’était tout ce qu’une première carte devait faire.

Pas remplacer le territoire.

Permettre d’y entrer sans se perdre.

**Fin du chapitre 146.**