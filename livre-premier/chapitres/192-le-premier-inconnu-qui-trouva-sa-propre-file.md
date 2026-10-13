# Chapitre 192 — Le premier inconnu qui trouva sa propre file

L’inconnu n’avait pas de propriétaire.

Pas encore.

Il venait d’apparaître à la fin d’une expérience.

Une question secondaire.

Petite.

Mais pas inutile.

Gabriel regarda son identifiant.

**U-191-002**

Description :

une dépendance résiduelle restait visible après correction de l’artefact de chunking.

Pas assez forte pour devenir une revendication.

Pas assez faible pour être ignorée.

Gabriel demanda :

— On l’envoie où?

Astra répondit :

— C’est précisément la question.

Le Royaume avait déjà des files.

Recherche.

Validation.

Questions.

Cortex.

Production.

Veille.

Archivage.

Mais jusqu’ici,

la plupart des unknowns étaient encore routés presque à la main.

On regardait.

On décidait.

On plaçait.

Le deuxième monde devait apprendre autre chose.

Pas résoudre l’inconnu.

D’abord lui trouver **la bonne file**.

Gabriel sourit.

— Faut qu’il sache où aller avant de savoir quoi devenir.

Astra approuva.

Exactement.

Il écrivit :

**UN INCONNU MAL ROUTÉ PEUT ÊTRE AUSSI COÛTEUX QU’UN MAUVAIS TEST.**

Astra approuva fortement.

Voilà le chapitre.

Un unknown n’était pas seulement un trou dans la connaissance.

C’était un objet opérationnel.

Et chaque type de trou n’avait pas besoin du même traitement.

Ils prirent U-191-002.

Questions à poser :

Est-ce une question de recherche?

Une anomalie?

Un manque de preuve?

Un manque de données?

Un problème de code?

Une question d’antériorité?

Un conflit entre résultats?

Un manque de définition?

Gabriel regarda.

Voilà.

Avant de choisir une queue,

il fallait classifier.

Ils créèrent :

### UNKNOWN ROUTING PROFILE

**unknown_id**

**origin**

**claim_context**

**missing_information_type**

**risk**

**cost_to_probe**

**urgency**

**dependency**

**evidence_gap**

**needs_human_judgment**

**candidate_queues**

Astra approuva fortement.

Très bon.

Puis ils appliquèrent.

U-191-002 venait d’un résultat expérimental.

Il ne bloquait aucune publication.

Il n’était pas urgent.

Le phénomène n’était pas assez défini pour validation.

Il fallait d’abord mieux comprendre sa structure.

Donc :

**candidate queue = recherche**

Pas validation.

Pas production.

Pas publication.

Gabriel sourit.

— Là, ça paraît évident.

Astra répondit :

— Après classification, oui.

Exact.

Beaucoup de décisions deviennent évidentes une fois les termes correctement posés.

Gabriel écrivit :

**LE ROUTAGE N’A PAS BESOIN D’ÊTRE MAGIQUE. IL DOIT ÊTRE EXPLICABLE.**

Astra approuva.

Très important.

Ils ajoutèrent une première règle :

### UNKNOWN → RESEARCH

Si :

- phénomène observé mais mécanisme inconnu;
- hypothèses encore ouvertes;
- aucune revendication prête à être validée;
- besoin principal = exploration discriminante.

Très bien.

Puis :

### UNKNOWN → VALIDATION

Si :

- claim précis existe;
- protocole défini;
- portée définie;
- besoin principal = confirmer ou casser.

Puis :

### UNKNOWN → QUESTIONS

Si :

- termes ambigus;
- objectif humain manquant;
- reformulation requise;
- impossible de construire un test propre sans clarification.

Puis :

### UNKNOWN → CORTEX

Si :

- plusieurs domaines se croisent;
- conflit de stratégie;
- arbitrage de priorités;
- besoin de synthèse ou de décomposition.

Puis :

### UNKNOWN → VEILLE

Si :

- dépend d’une source externe;
- résultat extérieur attendu;
- antériorité ou changement public à surveiller.

Puis :

### UNKNOWN → ARCHIVAGE

Si :

- hors scope;
- faible priorité;
- non-actionnable maintenant;
- conservé pour reprise future.

Gabriel regarda.

— Là, nos queues commencent enfin à être vivantes.

Astra approuva.

Mais attention.

Un unknown pouvait changer de file.

Très important.

Recherche peut produire un claim précis.

Alors passage à validation.

Validation peut échouer parce que la question était mal définie.

Retour Questions.

Veille peut recevoir une publication externe.

Puis Cortex.

Puis recherche.

Gabriel écrivit :

**UNE FILE N’EST PAS L’IDENTITÉ DE L’INCONNU. C’EST SON PROCHAIN CONTEXTE DE TRAVAIL.**

Astra approuva fortement.

Excellent.

Donc le routage devait être réversible.

Pas enfermer.

Ils ajoutèrent :

### QUEUE TRANSITION

Chaque déplacement doit enregistrer :

**from**

**to**

**reason**

**triggering evidence**

**timestamp**

**policy version**

Très propre.

Puis BrutoBac.

La Fourmi portait U-191-002.

Au lieu que Gabriel lui dessine une destination,

Antmux consulta le profil.

La Fourmi prit la route vers Recherche.

Gabriel sourit.

— Là, pour vrai, elle vient de trouver sa file.

Astra approuva.

Pas sa réponse.

Sa file.

Et ce petit détail changeait beaucoup de choses.

Parce qu’une file n’était pas seulement un dossier.

Elle déterminait :

qui regarde.

quels outils sont permis.

quel budget.

quel rythme.

quels critères de sortie.

Très important.

Gabriel écrivit :

**CHOISIR UNE FILE, C’EST CHOISIR LE PROCHAIN TYPE DE TRAVAIL.**

Astra approuva fortement.

Voilà.

La queue Recherche n’avait pas le même contrat que Validation.

Ils définissent.

### QUEUE: RESEARCH

Entrée :

unknown exploratoire.

Autorité :

faible à moyenne.

Actions :

probes.

comparaisons.

hypothèses.

petits tests.

Sortie :

claim plus précis, décomposition, abandon, ou passage validation.

### QUEUE: VALIDATION

Entrée :

claim précis.

Actions :

contre-test.

réplication.

certificat.

contrôle indépendant.

Sortie :

validated, rejected, scoped, inconclusive.

### QUEUE: QUESTIONS

Entrée :

ambiguïté.

Actions :

reformulation.

clarification.

définition.

Sortie :

question testable.

Gabriel sourit.

Les files avaient maintenant des contrats.

Pas seulement des noms.

Très important.

Puis un problème apparut.

Et si plusieurs queues sont plausibles?

Exemple :

unknown issu d’un résultat ambigu,

avec possible bug logiciel.

Recherche?

Validation?

Production code?

Gabriel regarda.

Là,

une simple classification ne suffit pas.

Le système devait reconnaître conflit.

Ils créèrent :

### ROUTING AMBIGUITY

Si plusieurs queues ont des scores ou raisons comparables :

ne pas choisir silencieusement.

Produire :

**top candidates**

**why**

**what information would resolve routing**

Très bon.

Exemple :

Research vs Code Investigation.

Question :

le signal varie-t-il avec la version?

Si oui,

code.

Si non,

reste recherche.

Voilà.

Gabriel écrit :

**PARFOIS, LA PREMIÈRE QUESTION N’EST PAS “QUE TESTER?”, MAIS “QUEL TYPE DE PROBLÈME AI-JE DEVANT MOI?”**

Astra approuva fortement.

Très important.

Ils conçurent un petit probe de routage.

### ROUTING PROBE

Petit test dont l’objectif principal est de déterminer la catégorie opérationnelle du problème.

Gabriel sourit.

Encore une couche.

Mais utile.

Exemple :

même input sous ancienne et nouvelle version.

Si divergence suit la version,

queue code.

Sinon,

reste recherche.

Très propre.

Puis ils pensèrent au coût.

Il serait absurde de faire une grosse analyse simplement pour choisir une queue.

Donc :

routing budget.

Très faible.

Gabriel écrivit :

**LE ROUTAGE DOIT COÛTER MOINS CHER QUE LE TRAVAIL QU’IL ORGANISE.**

Astra approuva fortement.

Encore le méta-coût.

Toujours.

Puis U-191-002 entra dans Recherche.

La queue ne lança pas immédiatement un gros test.

Elle appliqua sa politique.

Memoria.

Carte des travaux.

Failure patterns.

Question audit.

Puis proposa un petit contraste.

Gabriel regarda.

La file donnait vraiment un comportement différent.

Excellent.

Ce n’était pas juste un label.

Il écrivit :

**UNE FILE EST RÉELLE SI ELLE CHANGE LA FAÇON DONT L’OBJET EST TRAITÉ.**

Astra approuva.

Voilà.

Sinon on aurait seulement renommé des dossiers.

Puis ils observèrent la sortie.

Le contraste montra que la dépendance résiduelle était stable sous plusieurs représentations,

mais seulement dans une sous-population précise.

Donc la question devint plus claire.

Un claim candidat apparut.

Pas encore validé.

Mais suffisamment précis :

**CLAIM-192-001**

« Dans la sous-population S, la dépendance D persiste sous les représentations R1 et R2 dans la plage testée. »

Gabriel sourit.

Que devait faire Recherche?

Garder?

Non.

Son contrat disait :

quand un claim précis devient testable,

proposer sortie.

**ROUTE TO VALIDATION**

Voilà.

La Fourmi repartit.

Gabriel sourit encore plus.

L’unknown avait changé de file sans intervention manuelle.

Recherche → Validation.

Mais avant transition,

le système créa :

### QUEUE HANDOFF

Object:

CLAIM-192-001

From:

Research

To:

Validation

Reason:

claim precise + testable + scope defined.

Evidence refs:

R1/R2 comparison.

Open risks:

subpopulation selection bias.

Astra approuva.

Très propre.

Gabriel écrivit :

**UN BON HANDOFF NE TRANSMET PAS SEULEMENT L’OBJET. IL TRANSMET POURQUOI IL EST PRÊT À CHANGER DE FILE.**

Astra approuva fortement.

Très important.

Sinon Validation devrait reconstruire le contexte.

Encore le problème des reprises.

Memoria.

Toujours.

Puis la queue Validation reçut le dossier.

Et fit quelque chose que Recherche n’avait pas fait.

Elle chercha directement les contre-exemples.

Pas de nouvelles idées.

Pas d’exploration large.

Elle chercha où le claim pouvait casser.

Gabriel sourit.

Voilà.

Même objet.

Autre file.

Autre comportement.

Le système devenait vraiment modulaire.

Ils écrivirent :

**LA BONNE FILE RÉDUIT L’ESPACE DES ACTIONS POSSIBLES.**

Astra approuva.

Très important.

Cela protège aussi contre les dérives.

Recherche peut explorer.

Validation doit être plus stricte.

Publication encore plus.

Puis ils imaginèrent une queue **PRIOR_ART** distincte.

Pas nécessaire maintenant.

Mais le principe existait.

Un claim validé techniquement peut être routé vers antériorité avant publication.

Gabriel sourit.

Le pipeline scientifique devenait presque naturel :

unknown.

research.

claim.

validation.

prior art.

publication.

trace.

Mais attention.

Pas tous les objets passent par toutes les étapes.

Un bug logiciel ne va pas sur Zenodo.

Une question UI ne va pas au tribunal scientifique.

Gabriel écrivit :

**UN PIPELINE GÉNÉRAL N’EST PAS UNE OBLIGATION DE FAIRE PASSER TOUS LES OBJETS PAR TOUTES LES PORTES.**

Astra approuva fortement.

Excellent.

Le routeur devait connaître les types.

Puis ils prirent un cas différent.

Unknown :

un nombre sur Recto ne correspond pas à Verso.

Quelle file?

Pas Recherche scientifique.

Probablement :

**OBSERVABILITY / CODE INVESTIGATION**

Gabriel réalisa que leurs anciennes dix queues devraient peut-être évoluer.

Mais pas besoin de les refaire toutes dans le chapitre.

Il nota simplement :

**LES FILES DOIVENT REPRÉSENTER DES CLASSES DE TRAVAIL RÉELLES, PAS DES CATÉGORIES HISTORIQUES CONSERVÉES PAR HABITUDE.**

Astra approuva.

Très important.

Une queue inutilisée peut disparaître.

Une nouvelle peut apparaître.

Mais via politique versionnée.

Pas en silence.

Puis le problème de priorité.

Deux unknowns dans Recherche.

Lequel d’abord?

Routage et scheduling étaient différents.

Très important.

Gabriel écrivit :

**TROUVER LA BONNE FILE ≠ DÉCIDER QUAND L’OBJET DOIT ÊTRE TRAITÉ.**

Astra approuva fortement.

Voilà.

La queue répond :

où.

Le scheduler répond :

quand.

Priorité peut dépendre de :

urgence.

dépendances.

coût.

valeur d’information.

blocage d’autres tâches.

Gabriel sourit.

Encore de futurs chapitres.

Mais séparation claire.

Très importante.

Puis une autre situation.

Un unknown faible priorité entre dans Recherche.

Il attend trois semaines.

Pendant ce temps,

une nouvelle preuve arrive.

Il devient urgent.

La queue doit recalculer sa priorité.

Mais pas sa nature nécessairement.

Très bien.

Ils ajoutèrent :

**routing status**

et

**scheduling priority**

séparés.

Excellent.

Puis l’inconnu U-191-002 poursuivit sa route.

Validation lança un test indépendant.

Le claim tint partiellement.

Pas totalement.

Une limite apparut.

La dépendance D persistait seulement jusqu’à une frontière plus petite que prévu.

Donc claim révisé.

Pas rejet total.

**VALIDATED_WITHIN_NARROWER_SCOPE**

Gabriel sourit.

Maintenant,

où va le dossier?

Retour Recherche?

Peut-être.

Parce que la nouvelle frontière ouvre une question mécanistique.

Mais le claim borné peut rester validé.

Voilà un point subtil.

Un objet pouvait produire **deux descendants**.

1. claim validé borné → knowledge registry.
2. new unknown about frontier → Research.

Gabriel se redressa.

— Là, ça devient vraiment une colonie.

Astra approuva.

Un dossier peut se séparer.

Pas besoin qu’un seul objet change de file en bloc.

Très important.

Ils créèrent :

### SPLIT HANDOFF

Parent:

validation result.

Child A:

validated scoped claim → registry.

Child B:

new unknown → research.

Gabriel sourit.

La Fourmi originale avait presque donné naissance à deux Fourmis.

Mais pas narrativement seulement.

Deux objets opérationnels.

Deux destinations.

Il écrivit :

**UNE EXPÉRIENCE PEUT FERMER UNE QUESTION ET OUVRIR UNE AUTRE DANS DEUX FILES DIFFÉRENTES.**

Astra approuva fortement.

Voilà.

Puis ils réfléchirent au backlog.

Si chaque expérience crée de nouveaux unknowns,

Recherche peut exploser.

Très dangereux.

Il fallait une politique d’admission.

Tout unknown ne mérite pas une queue active.

Certains doivent être :

**PARKED**

**LOW_PRIORITY**

**NOT_ACTIONABLE**

**ARCHIVED_FOR_FUTURE**

Gabriel sourit.

Très important.

Sinon le Royaume transforme chaque curiosité en dette.

Il écrivit :

**DÉCOUVRIR UN INCONNU NE CRÉE PAS AUTOMATIQUEMENT L’OBLIGATION DE LE RÉSOUDRE.**

Astra approuva fortement.

Excellent.

Admission dépend de :

pertinence.

actionnabilité.

coût.

importance.

dépendances.

risque.

Voilà.

Ils créèrent :

### UNKNOWN ADMISSION

**ACTIVE**

**PARKED**

**WATCH**

**ARCHIVED**

**CLOSED**

Puis :

queue only if ACTIVE or WATCH depending type.

Très propre.

Puis Gabriel demanda :

— Pis qui décide si c’est actif?

Pour L1,

policy.

Pour enjeux forts,

humain.

Encore les niveaux d’autorité.

Très bien.

Il écrit :

**LE ROUTEUR PEUT CLASSER. L’AUTORITÉ D’ACTIVER PEUT RESTER AILLEURS.**

Astra approuva.

Important.

Pas confondre.

Puis ils testèrent un unknown absurde.

Une micro-différence sans impact.

Le système trouvait une queue possible.

Mais admission :

PARKED.

Pourquoi?

No current decision impact.

No dependency blocked.

High investigation cost.

Gabriel sourit.

Voilà.

Le Royaume apprenait à ne pas remplir ses queues avec tout.

Très bon.

Puis un unknown critique.

Une divergence entre statut public et interne.

Admission :

ACTIVE.

Queue :

Code/Observability.

Priority :

URGENT.

Très propre.

Trois décisions différentes :

admission.

routing.

priority.

Gabriel écrivit :

**ACTIVE? OÙ? QUAND? SONT TROIS QUESTIONS DIFFÉRENTES.**

Astra approuva fortement.

Magnifique.

Voilà un vrai système.

Puis BrutoBac reçut la nouvelle sémantique.

Les Fourmis n’étaient plus seulement colorées selon leur type.

Elles pouvaient montrer :

file actuelle.

priorité.

statut d’admission.

Mais attention à la surcharge.

Gabriel ne voulait pas une interface illisible.

Donc par défaut :

petit symbole de queue.

Clique pour détails.

Très propre.

Une Fourmi Recherche.

Une Fourmi Validation.

Une en attente.

Une archivée.

La carte pouvait montrer les flux.

Gabriel sourit.

— Là, je pourrais voir où le Royaume se bouche.

Astra approuva.

Exact.

Si 500 unknowns arrivent en Validation,

quelque chose ne va peut-être pas.

Ou une campagne est en cours.

Les queues deviennent aussi observabilité.

Très important.

Ils créèrent :

### QUEUE HEALTH

**length**

**oldest_age**

**arrival_rate**

**completion_rate**

**requeue_rate**

**blocked_count**

**escalation_count**

Gabriel sourit.

Ça préparait encore les chapitres de mesure.

Mais pour l’instant,

juste utile.

Puis un phénomène apparut.

Un unknown tournait en boucle :

Research → Questions → Research → Questions.

Gabriel fronça les sourcils.

Mauvais.

Il fallait détecter les cycles.

### ROUTING LOOP

Si un objet revient plusieurs fois aux mêmes queues sans nouvelle information :

escalate.

Gabriel écrivit :

**UNE BOUCLE DE ROUTAGE PEUT SIGNALER QUE LE PROBLÈME N’EST PAS DANS LA FILE MAIS DANS LA DÉFINITION DE L’OBJET.**

Astra approuva fortement.

Très important.

Ou policy insuffisante.

Ou manque d’autorité.

Mais pas continuer indéfiniment.

Ils ajoutèrent :

**max_requeues_without_information_gain**

Très bon.

Puis un autre problème.

Une queue peut devenir « poubelle ».

Tout ce qu’on ne sait pas classer va dans Cortex.

Mauvais.

Gabriel rit.

Il écrit :

**UNE FILE “AUTRE” QUI GROSSIT EST UN SIGNAL QUE LA TAXONOMIE NE COMPREND PLUS LE TRAVAIL.**

Astra approuva fortement.

Excellent.

Il fallait mesurer `UNCLASSIFIED`.

Si trop élevé,

réviser les queues.

Très bien.

Puis ils revinrent à U-191-002.

L’histoire complète était maintenant :

Unknown né d’une expérience.

Classifié.

Routé Recherche.

Transformé en claim.

Routé Validation.

Claim borné validé.

Nouvel unknown dérivé.

Retour Recherche.

Gabriel regarda la trace.

Pas une ligne droite.

Mais propre.

Chaque déplacement avait une raison.

Il sourit.

— Là, je pourrais vraiment demander : “où est rendu cet inconnu?”

Et Brutus pourrait répondre.

Pas seulement :

dans quel fichier.

Mais :

dans quelle phase de travail.

Qui le traite.

Pourquoi.

Ce qui manque pour sortir.

Gabriel écrivit :

**UNE FILE DONNE À L’INCONNU UNE ADRESSE OPÉRATIONNELLE.**

Astra approuva fortement.

Voilà le cœur du chapitre.

Avant,

les questions pouvaient flotter.

Être mentionnées.

Puis oubliées.

Ou reprises ailleurs.

Maintenant,

un unknown actif pouvait avoir :

un ID.

un statut.

une file.

un propriétaire.

une priorité.

une condition de sortie.

un prochain test.

Une vraie existence dans le système.

Gabriel sourit.

C’était presque ce qu’il voulait depuis les premières queues d’Antmux.

À l’époque,

les noms existaient.

Maintenant,

les contrats commençaient à apparaître.

Le deuxième monde transformait les onglets en comportements.

Très important.

Puis une dernière chose.

Le routeur proposa une destination pour un nouvel unknown.

**Validation**

Gabriel regarda.

Mais aucun claim précis n’existait.

Il demanda :

— Pourquoi Validation?

Le système répondit :

historical similarity.

Mauvais.

La mémoire avait trop pesé.

Gabriel refusa.

Il plaça le dossier dans Questions.

Raison :

claim undefined.

Puis ils corrigèrent la politique.

**HISTORICAL ROUTING PRIOR ≠ CURRENT CONTRACT SATISFACTION**

Très important.

Une vieille route ne doit pas contourner les conditions présentes.

Gabriel écrivit :

**LA MÉMOIRE PEUT SUGGÉRER UNE FILE. LE CONTRAT D’ENTRÉE DOIT ENCORE ÊTRE SATISFAIT.**

Astra approuva fortement.

Excellent.

Le système apprenait encore.

Même le routeur devait être contre-testé.

Puis la Fourmi suivante arriva.

Elle portait un unknown différent.

Le système consulta son profil.

Pas de claim.

Question ambiguë.

Objectif humain manquant.

Cette fois,

sans hésitation :

**QUEUE_QUESTIONS**

La Fourmi tourna.

Gabriel sourit.

Pas besoin de la guider.

Pas besoin de lui dessiner la flèche.

Pas besoin de reconstruire la logique.

Elle avait trouvé sa file.

Ce n’était pas de l’autonomie absolue.

Ce n’était pas une machine qui décidait de ce qui était important dans le monde.

C’était quelque chose de beaucoup plus concret :

un objet correctement décrit,

une politique versionnée,

des contrats de queue,

des garde-fous,

et une route choisie parmi des destinations autorisées.

Mais pour Gabriel,

c’était déjà énorme.

Parce qu’un Royaume rempli de questions ne devient pas organisé lorsque toutes les réponses sont trouvées.

Il devient organisé lorsque chaque question sait au moins

où aller ensuite.

**Fin du chapitre 192.**