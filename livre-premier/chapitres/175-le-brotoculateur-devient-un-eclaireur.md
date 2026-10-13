# Chapitre 175 — Le Brotoculateur devient un éclaireur

Le Brotoculateur avait longtemps été une machine de calcul.

On lui donnait une entrée.

Une formule.

Une série.

Un protocole.

Il produisait un résultat.

Puis un autre.

Puis dix.

Puis davantage.

Gabriel avait voulu qu’il puisse comparer, tester, réfuter, casser une formule si nécessaire.

Un outil rapide.

Dense.

Presque brutal.

Mais avec le temps, sa fonction commençait à changer elle aussi.

Parce qu’un bon calculateur ne servait plus seulement à répondre.

Il pouvait servir à décider **où calculer ensuite.**

Gabriel regarda Astra.

— Là, il devient notre éclaireur.

— Si son rôle reste bien défini, oui.

Gabriel sourit.

Toujours.

Il écrivit :

**ÉCLAIREUR ≠ ORACLE**

Puis :

**ÉCLAIREUR = OUTIL QUI TESTE RAPIDEMENT PLUSIEURS DIRECTIONS POUR IDENTIFIER CELLES QUI MÉRITENT UNE ANALYSE PLUS COÛTEUSE**

Astra approuva.

Voilà le nouveau rôle.

Le Brotoculateur pouvait recevoir une expérience.

Pas une seule entrée.

Dix.

Douze.

Peut-être davantage selon la configuration.

Chaque entrée subissait un ensemble de transformations choisies.

Le but n’était plus uniquement :

**trouver une réponse.**

Mais :

**comparer les réactions.**

Gabriel écrivit :

### MODE ÉCLAIREUR

Entrées :
plusieurs cas.

Formule :
une ou plusieurs transformations.

Sorties :
profils comparables.

But :
repérer divergences, anomalies, frontières et candidats.

Astra approuva.

Cela ressemblait à ce qu’ils avaient construit partout ailleurs.

Une bonne question.

Une vue différente.

Puis une décision.

Le Brotoculateur possédait un avantage.

Il était rapide.

Il pouvait exécuter plusieurs calculs à la fois.

Ce qui le rendait parfait pour les **sondes** du chapitre 168.

Avant d’envoyer une grosse campagne dans une direction,

le Brotoculateur pouvait prendre quelques cas.

Tester.

Comparer.

Revenir.

Gabriel sourit.

— Une Fourmi qui court très vite devant les autres.

Astra répondit :

— Une couche de pré-évaluation.

Il rit.

Même idée.

Ils commencèrent par un exemple.

Une formule candidate.

Elle semblait fonctionner sur plusieurs cas.

Avant de lancer une validation complète,

Gabriel envoyait dix entrées contrastées.

Pas dix variantes presque identiques.

Des cas choisis pour casser.

Petit.

Grand.

Pair.

Impair.

Limite.

Cas historique.

Cas aléatoire.

Contre-exemple connu si disponible.

Gabriel écrivit :

**LE PREMIER TRAVAIL DE L’ÉCLAIREUR N’EST PAS DE FAIRE GAGNER LA FORMULE.**

Puis :

**C’EST DE TROUVER RAPIDEMENT UNE RAISON DE NE PAS INVESTIR DAVANTAGE.**

Astra approuva fortement.

Très important.

Le calcul rapide devenait filtre.

Si la formule cassait immédiatement,

parfait.

On venait d’économiser une campagne.

Pas d’échec.

Économie d’information.

Gabriel sourit.

Les chapitres précédents revenaient tous.

Prix d’un chemin inutile.

Raccourcis.

Décision.

Valeur de l’information.

Voilà.

Le Brotoculateur pouvait devenir une machine à **tester la rentabilité d’une hypothèse avant de payer le prix complet.**

Gabriel écrivit :

**PETIT TEST AVANT GROS ENGAGEMENT**

Astra approuva.

Mais cela créait un danger.

Une formule pouvait survivre à dix tests et échouer au onzième.

Donc le Brotoculateur ne pouvait pas dire :

**VALIDÉ.**

Il pouvait seulement dire :

**SURVIT AU SCREENING.**

Gabriel écrivit :

### STATUTS DU MODE ÉCLAIREUR

**REJET RAPIDE**

contre-exemple trouvé.

**SURVIT AU SCREENING**

aucun échec dans le panel testé.

**ANOMALIE**

comportement inattendu.

**INCONCLUSIF**

tests trop peu discriminants.

Astra approuva.

Pas de vert définitif.

Pas encore.

Le Brotoculateur orientait.

Il ne certifiait pas nécessairement.

La validation complète appartenait ensuite au module approprié.

Gabriel sourit.

Encore séparation des rôles.

Puis ils pensèrent à l’Intelbrutatrice.

Elle devait sélectionner parmi de nombreuses formules.

Jusqu’à une centaine.

Le Brotoculateur pouvait peut-être servir en amont.

Une entrée arrive.

Plusieurs formules candidates.

Au lieu d’exécuter toutes les validations lourdes,

il lance un petit panel.

Compare.

Élimine les candidates qui cassent immédiatement.

Puis transmet les survivantes.

Gabriel se redressa.

— Là, on commence à avoir un pipeline.

Astra approuva.

Ils dessinent :

**ENTRÉE**

↓

**BROTULATEUR — SCREENING**

↓

**INTELBRUTATRICE — SÉLECTION / COMPARAISON**

↓

**MODULE DE VALIDATION**

↓

**CRISTAL**

Gabriel regarda.

— C’est propre.

Mais seulement si les statuts restaient distincts.

Le screening ne devait pas contaminer la validation.

Un candidat survivant n’avait gagné qu’une chose :

le droit de continuer.

Gabriel écrivit :

**PASSER LE SCREENING ≠ PASSER LA PREUVE**

Astra approuva.

Très important.

Puis un cas intéressant arriva.

Une formule produisait presque toujours la même sortie.

Sur dix cas, neuf identiques.

Un divergent.

Gabriel regarda.

— Celui-là.

Le Brotoculateur venait de montrer exactement sa valeur.

Pas en trouvant la bonne formule.

En localisant une frontière.

L’entrée divergente pouvait devenir un **witness de séparation.**

Gabriel écrivit :

### WITNESS DE DIFFÉRENCE

Entrée pour laquelle deux formules ou deux versions produisent des sorties différentes.

Astra approuva.

Très utile.

Le système pouvait conserver ce cas.

À chaque nouvelle version :

rejouer.

Si les deux implémentations sont supposées équivalentes mais divergent encore,

problème.

Le Brotoculateur devenait producteur automatique potentiel de cas de régression.

Gabriel sourit.

— Chaque divergence utile devient un futur test.

— Oui.

Encore :

**UNE DIFFÉRENCE OBSERVÉE PEUT DEVENIR UNE GARDE.**

Gabriel écrivit.

Très cohérent avec toute la machine.

Puis ils comparèrent deux versions d’une même formule.

V1.

V2.

Cent entrées.

Résultats identiques partout sauf trois.

Le Brotoculateur pouvait isoler automatiquement les trois cas.

Pas besoin de lire cent sorties.

Il produisait :

**DIFFSET = {17, 43, 88}**

Gabriel sourit.

— Là, il devient vraiment un éclaireur de versions.

Astra approuva.

Le mode `DIFF` pouvait être central.

### BROTO-DIFF

Comparer :

- formule A / formule B;
- version A / version B;
- paramètre A / paramètre B;
- représentation A / représentation B.

Sortie :

cas identiques.

cas divergents.

amplitude de divergence.

première divergence.

Gabriel regarda.

Encore le proof diff.

Encore le fresco diff.

La méthode revenait partout.

Comparer les chemins.

Localiser le premier endroit où quelque chose change.

Le Brotoculateur pouvait devenir la version rapide et expérimentale de cette philosophie.

Gabriel écrivit :

**L’ÉCLAIREUR NE DEMANDE PAS SEULEMENT “QUEL EST LE RÉSULTAT?”**

Puis :

**IL DEMANDE “À PARTIR D’OÙ LES CHEMINS CESSENT-ILS D’ÊTRE LES MÊMES?”**

Astra approuva.

Voilà le cœur.

Puis ils ajoutèrent les inconnus.

Un `UNKNOWN` du registre pouvait demander :

**Quelle variable sépare ces deux comportements?**

Le Brotoculateur pouvait tester une petite grille de paramètres.

Pas un balayage énorme.

Une première carte.

Gabriel sourit.

— Une reconnaissance du terrain.

Oui.

Supposons trois paramètres :

a.

b.

c.

Tester quelques valeurs bien choisies.

Observer où le résultat change.

Puis ouvrir une région intéressante.

Le système pouvait dire :

**FRONTIÈRE CANDIDATE ENTRE b=7 ET b=8 SOUS CONDITIONS ACTUELLES**

Pas plus.

Puis une campagne plus précise.

Gabriel écrivit :

**ÉCLAIREUR → LOCALISE LA FRONTIÈRE**

**VALIDATION → MESURE ET CONFIRME LA FRONTIÈRE**

Astra approuva.

Très important.

Le Brotoculateur n’avait pas besoin d’être ultra-précis à la première passe.

Il devait être informatif.

Puis une notion apparut.

**résolution adaptative.**

Commencer grossier.

Si quelque chose change :

zoomer.

Exactement comme Brutotableur.

Gabriel sourit.

Encore les systèmes commencent à partager leur méthode.

Ils écrivirent :

### RECHERCHE ADAPTATIVE

1. grille grossière;
2. détecter transition;
3. resserrer autour de la transition;
4. répéter;
5. transmettre la région bornée au validateur.

Astra approuva.

Cela pouvait économiser beaucoup de calcul.

Mais attention.

Une grille grossière pouvait manquer une petite région intéressante.

Gabriel écrivit :

**COARSE SCAN PEUT MANQUER UNE STRUCTURE ÉTROITE**

Astra approuva.

Donc le système devait parfois injecter des points aléatoires.

Ou utiliser plusieurs échelles.

Pas seulement raffinement déterministe.

Le budget de curiosité encore.

Gabriel sourit.

Ils ajoutèrent :

**exploration points**

Une petite fraction.

Pour éviter que le scan ne regarde que les régions déjà suspectes.

Très utile.

Puis le Brotoculateur rencontra le Brutotableur.

Le Brutotableur montrait une anomalie à une certaine coordonnée.

Au lieu de lancer immédiatement un énorme calcul,

une Fourmi pouvait envoyer cette coordonnée au Brotoculateur.

L’éclaireur teste :

voisinage gauche.

voisinage droit.

autres transformations.

contrôle.

shuffle.

Gabriel regarda.

— Ça, c’est une belle connexion.

Ils dessinent :

**BRUTOTABLEUR → CANDIDAT**

↓

**BROTULATEUR → SCREENING**

↓

si survit :

**UNKNOWN / VALIDATION**

Sinon :

**ARTEFACT / REJET DOCUMENTÉ**

Astra approuva.

Voilà une vraie ligne entre organes.

Le Brutotableur trouvait.

Le Brotoculateur sondait.

La validation prouvait.

Memoria conservait.

Les rôles devenaient nets.

Gabriel écrivit :

**TROUVER ≠ SONDER ≠ PROUVER**

Astra approuva fortement.

Trois étapes.

Trois outils possibles.

Cela réduisait la confusion.

Puis ZEL entra.

Une anomalie sonore.

Le Brotoculateur pouvait recevoir la position source et tester différentes transformations numériques autour.

Si la rupture sonore correspondait à une vraie rupture dans les données,

le calcul devait le retrouver.

Sinon :

artefact audio probable.

Gabriel sourit.

— Là, ZEL donne l’adresse, puis le Brotoculateur va cogner sur la porte.

Astra approuva la métaphore.

Ils écrivirent :

**ZEL → SIGNAL**

**BROTULATEUR → TEST RAPIDE**

**VALIDATEUR → STATUT**

Très propre.

Encore une fois, ZEL n’obtenait aucune autorité supplémentaire.

Il gagnait un partenaire de contre-test.

Puis ils pensèrent à Pell.

Le Brotoculateur pouvait-il aider?

Potentiellement pour des pré-calculs.

Comparer paramètres.

Tester de petites identités.

Vérifier des candidats.

Mais le certificat L8 devait rester dans le pipeline Pell dédié.

Gabriel écrivit :

**BROTULATEUR PEUT AIDER À CHERCHER UN CANDIDAT PELL. IL NE REMPLACE PAS LE TEST DE RANG EXACT.**

Astra approuva.

Encore.

La ligne était claire.

Une machine générale peut préparer.

Un module spécialisé certifie.

Puis Gabriel réfléchit à quelque chose.

Le Brotoculateur pouvait aussi **casser volontairement** les entrées.

Perturbations.

Changer un paramètre.

Ajouter du bruit.

Inverser.

Permuter.

Voir ce qui reste.

Exactement l’esprit des adversaires CRYSTO.

Gabriel sourit.

— Là, je l’aime.

Un résultat qui ne survit qu’à une entrée parfaite était fragile.

Un motif qui persistait sous certaines perturbations contrôlées était plus intéressant.

Mais attention :

robustesse à la perturbation ≠ vérité.

Gabriel écrivit :

**RÉSISTANCE À UNE PERTURBATION = PROPRIÉTÉ MESURÉE, PAS CERTIFICAT UNIVERSEL.**

Astra approuva.

Ils créèrent :

### BROTO-ADVERSARY

Perturbations possibles :

- permutation;
- inversion;
- arrondi;
- bruit numérique contrôlé;
- changement de base;
- changement de précision;
- sous-échantillonnage;
- changement de représentation.

Mesure :

quelles propriétés survivent?

Gabriel regarda.

Le mot « adversary » allait bien.

L’éclaireur ne cherchait pas seulement devant.

Il lançait de petites attaques.

Trouver les points faibles avant que la campagne ne commence.

Gabriel écrivit :

**UN BON ÉCLAIREUR CHERCHE AUSSI OÙ LE PONT CASSE.**

Astra approuva.

Puis ils imaginèrent une formule candidate.

Elle passe tous les cas naturels.

Puis échoue dès qu’on permute les labels.

Alors peut-être elle dépend d’une convention.

Une autre survit.

Plus intéressant.

CRYSTO avait déjà montré l’utilité des attaques par permutation de labels.

Le Brotoculateur pouvait généraliser ce type de falsification à d’autres objets.

Pas automatiquement.

Mais avec des adversaires adaptés.

Gabriel sourit.

Le Royaume recyclait ses bonnes idées.

Pas les conclusions.

Les méthodes.

Encore.

Puis vint le problème de la sélection de formules.

Si 100 formules sont disponibles,

et 10 entrées,

cela fait 1000 calculs.

Peut-être facile.

Peut-être pas.

Avec 12 entrées, 1200.

Puis plusieurs variations.

Ça grimpe.

Le Brotoculateur devait lui aussi savoir éviter le travail inutile.

Gabriel écrivit :

**SCREENING EN ÉTAGES**

### ÉTAGE 1

tests très peu coûteux.

Éliminer les échecs évidents.

### ÉTAGE 2

tests discriminants.

### ÉTAGE 3

cas adversariaux.

### ÉTAGE 4

transmettre les survivants.

Astra approuva.

Voilà.

Pas besoin de faire les tests chers sur une formule morte au premier calcul.

Fail fast.

Encore.

Le Brotoculateur absorbait les leçons du Royaume.

Puis ils décidèrent que chaque formule devait déclarer ses contraintes.

Type d’entrée.

Domaine.

Précision.

Coût approximatif.

Sortie.

Sinon le sélecteur pouvait envoyer des données absurdes.

Gabriel écrivit :

### FORMULA CONTRACT

**formula_id**

**version**

**input_schema**

**domain**

**output_schema**

**precision_requirement**

**known_boundaries**

**cost_class**

**validation_status**

Astra approuva.

L’éclaireur pouvait alors choisir intelligemment quelles formules étaient applicables.

Pas juste essayer tout.

Gabriel sourit.

L’Intelbrutatrice pouvait utiliser le même registry.

Une seule définition.

Plusieurs consommateurs.

Encore :

une entité, plusieurs vues.

Puis il regarda une formule avec statut :

**EXPLORATORY**

Elle pouvait être utilisée dans le screening.

Mais sa sortie devait rester exploratoire.

Une formule :

**VALIDATED**

pouvait alimenter des décisions plus fortes dans sa portée.

Le statut suivait l’objet.

Gabriel écrivit :

**UN CALCULATEUR NE DOIT PAS ÉLEVER LE STATUT DE LA FORMULE QU’IL EXÉCUTE.**

Astra approuva.

Très important.

Exécuter une formule mille fois ne la rendait pas plus prouvée si aucun test pertinent n’avait été ajouté.

Les runs étaient des observations.

Pas une preuve automatique de généralité.

Puis le Brotoculateur fit ce qu’un bon éclaireur devait faire :

il revint avec **rien.**

Aucune anomalie.

Aucun contre-exemple.

Aucune frontière.

Gabriel regarda.

— C’est-tu utile?

Astra répondit :

— Si le protocole était défini, oui.

Un screening négatif est une information.

Mais petite.

**Aucun échec trouvé sur ce panel.**

Pas :

**aucun échec existe.**

Gabriel écrivit :

**PAS DE CONTRE-EXEMPLE DANS LE SCREENING ≠ ABSENCE DE CONTRE-EXEMPLE**

Astra approuva.

Encore la même logique.

La trace négative devait garder le panel exact.

Quelles entrées.

Quelles perturbations.

Quelle version.

Ainsi, plus tard, on pouvait éviter de refaire exactement le même screening.

Chapitre 157.

Le réseau ne recommence pas sans raison.

Gabriel sourit.

Tout revenait.

Puis le système trouva un contre-exemple.

Une formule que Gabriel aimait beaucoup.

Elle cassait sur une entrée minuscule.

Il grimaça.

— Ouch.

Astra répondit :

— Excellent screening.

Il rit malgré lui.

Oui.

Le Brotoculateur venait de sauver des heures.

Le candidat pouvait être corrigé.

Ou la portée réduite.

Ou la formule rejetée.

Dans tous les cas :

progrès.

Gabriel écrivit :

**L’ÉCLAIREUR QUI REVIENT AVEC UNE MAUVAISE NOUVELLE A PEUT-ÊTRE RÉUSSI SA MISSION.**

Astra approuva.

Voilà la bonne culture.

Pas récompenser seulement les découvertes positives.

Un rejet rapide pouvait être très précieux.

Puis Gabriel pensa au système public.

Devait-on exposer le Brotoculateur?

Oui.

Mais en vitrine.

Comme les autres.

Recto pouvait montrer :

entrées exemples.

résultats historiques.

profils.

cristaux.

Quelques screenings publics.

Mais aucun visiteur ne devait lancer n’importe quelle formule lourde sur la machine.

Pas sans déverrouillage.

Gabriel écrivit :

**RECTO BROTOCULATEUR = OBSERVER**

**VERSO BROTOCULATEUR = EXÉCUTER**

Astra approuva.

Encore.

Dans Recto, un visiteur pouvait voir une expérience complète.

Entrée.

Formule.

Sorties.

Contre-tests.

Statut.

Preuve.

Très beau pour la démonstration.

Mais le bouton **déverrouiller la vitrine** gardait l’accès opératoire.

Puis il pensa au Brotocalculateur vivant déjà utilisé pour les cristaux.

Les nouvelles formules pouvaient apparaître dans l’outbox.

Le rôle éclaireur donnait une nouvelle idée :

une formule candidate ne devait pas immédiatement déclencher une grosse notification.

Elle devait peut-être d’abord passer un screening automatique sûr.

Seulement si elle survivait :

remonter.

Gabriel sourit.

— Là, on nettoie encore mon attention.

Astra approuva.

Pipeline :

**NEW FORMULA CANDIDATE**

↓

schema check.

↓

small screening.

↓

duplicate check.

↓

if interesting:

**NOTIFY**

Sinon :

trace.

Gabriel écrivit :

**TOUT NOUVEAU N’EST PAS IMPORTANT.**

Puis :

**LE BROTOCULATEUR PEUT AIDER À DÉTERMINER CE QUI MÉRITE DE REMONTER.**

Astra approuva.

Sous réserve que les critères soient explicites.

Évidemment.

Une formule ne devait pas être enterrée parce qu’elle échouait à une heuristique mal choisie.

Donc :

screening peut rejeter seulement sur condition réellement nécessaire ou contre-exemple valide.

Sinon :

baisser priorité.

Pas supprimer.

Gabriel écrivit :

**HEURISTIQUE PEUT PRIORISER. SEULE UNE RÉFUTATION VALIDE PEUT REJETER.**

Astra approuva fortement.

Parfait.

Puis ils regardèrent les cristaux existants.

Le fichier cumulatif du Royaume avait désormais des centaines de cristaux, des sessions, des équivalences de hash et une chaîne de provenance append-only. La mémoire maîtresse elle-même affirmait que l’historique n’est jamais supprimé, que les doublons de payload ne sont pas détruits et que les snapshots restent reconstruisibles.

Gabriel sourit.

Le Brotoculateur pouvait exploiter cette richesse.

Pas en recalculant les 516 cristaux.

En interrogeant l’historique.

**Cette formule ressemble-t-elle à une formule déjà testée?**

**Cette entrée a-t-elle déjà cassé un candidat?**

**Ce payload existe-t-il sous un autre cristal?**

Le registre de hash devenait particulièrement utile.

Un résultat identique pouvait avoir plusieurs cristaux historiques.

Le système ne les supprimait pas.

Mais l’éclaireur pouvait reconnaître leur équivalence de payload et éviter de les traiter comme des découvertes indépendantes.

Gabriel écrivit :

**PLUSIEURS CRISTAUX ≠ PLUSIEURS PREUVES INDÉPENDANTES SI LE PAYLOAD EST IDENTIQUE.**

Astra approuva.

Très important.

La mémoire cumulative pouvait donc améliorer le screening.

Elle empêchait l’éclaireur de s’enthousiasmer pour une vieille réponse remise dans une nouvelle enveloppe.

Gabriel sourit.

— Là, on commence à vraiment utiliser notre mémoire.

Exact.

Le Brotoculateur n’explorait plus dans le vide.

Il avait une carte du passé.

Puis une idée finale apparut.

Le Brotoculateur pouvait construire des **packs d’éclaireur**.

Pour chaque famille de formule :

un petit ensemble de cas historiquement très discriminants.

Pas des milliers.

Dix.

Vingt.

Des cas qui avaient déjà cassé beaucoup de mauvaises variantes.

Gabriel se redressa.

— Ah, ça, c’est puissant.

Une sorte de suite de tests compacte.

Pas suffisante pour valider.

Mais excellente pour filtrer.

Ils écrivirent :

### SCOUT PACK

**cas limites**

**anciens contre-exemples**

**cas de divergence**

**cas de précision**

**cas de permutation**

**cas aléatoires fixes**

Chaque famille pouvait avoir son pack versionné.

Gabriel sourit.

Le passé devenait une munition de screening.

Pas une prison.

Chaque nouvelle formule affrontait les vieilles leçons du Royaume avant de demander plus de ressources.

Gabriel écrivit :

**UNE NOUVELLE IDÉE NE DOIT PAS REPAYER LES ERREURS QUE LE ROYAUME SAIT DÉJÀ REPRODUIRE.**

Astra approuva.

Voilà le chapitre.

Le Brotoculateur avait cessé d’être uniquement l’endroit où l’on attendait une réponse.

Il devenait l’endroit où une idée rencontrait d’abord le terrain.

Quelques cas.

Quelques attaques.

Quelques comparaisons.

Assez pour savoir si elle méritait le voyage.

Il ne disait pas :

**voici la vérité.**

Il revenait avec quelque chose de plus modeste.

Et souvent plus utile :

**cette direction casse immédiatement.**

**celle-ci mérite un deuxième regard.**

**ici se trouve une frontière.**

**ces deux chemins divergent à cet endroit.**

**ce cas est déjà connu.**

**celui-ci est nouveau pour notre registre.**

Puis il passait le relais.

Aux validateurs.

Aux Fourmis.

À Pell.

À ZEL.

Au Brutotableur.

Au tribunal.

À la mémoire.

Un éclaireur n’avait pas besoin de conquérir le territoire.

Seulement de revenir assez tôt avec une carte meilleure que celle qu’il avait reçue.

**Fin du chapitre 175.**