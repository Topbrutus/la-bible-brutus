# Chapitre 194 — Le seuil entre aider et décider

Le problème n’était plus de savoir si Brutus pouvait aider.

Il aidait déjà.

Il proposait des routes.

Il comparait des coûts.

Il retrouvait les erreurs anciennes.

Il évitait certains recalculs.

Il routait des unknowns.

Il exécutait même quelques décisions L1 sans demander Gabriel.

Tout cela fonctionnait.

La vraie question était devenue plus difficile.

**À partir de quand aider devient décider?**

Gabriel regardait l’écran.

Une décision venait d’entrer.

Pas critique.

Pas dangereuse.

Mais pas totalement triviale non plus.

Trois options.

A.

B.

C.

Brutus avait une recommandation claire.

B.

Gabriel demanda :

— Là, si tu me dis juste “je recommande B”, tu m’aides.

Astra approuva.

— Si tu exécutes B sans moi?

— Alors je décide dans le cadre d’une autorité déléguée.

Gabriel hocha la tête.

Voilà.

La frontière n’était pas dans l’intelligence.

Elle était dans **l’autorité d’agir**.

Il écrivit :

**AIDER = STRUCTURER LE CHOIX.**

Puis :

**DÉCIDER = ENGAGER UNE ACTION OU UN ÉTAT SELON UNE AUTORITÉ DONNÉE.**

Astra approuva fortement.

Très important.

Un système peut être extrêmement intelligent

et rester en mode assistance.

Il peut analyser.

Comparer.

Prédire.

Montrer les conséquences.

Mais tant qu’il n’engage pas l’action,

la décision finale reste ailleurs.

Gabriel sourit.

Simple en apparence.

Mais les zones grises allaient être nombreuses.

Ils prirent un exemple.

Brutus dit :

**B est recommandé.**

Puis il met automatiquement B en surbrillance.

Aide.

Il trie B en premier.

Aide.

Il masque A parce qu’elle est dominée.

Peut-être aide.

Il masque C parce qu’elle dépasse une policy dure.

Garde.

Il lance B automatiquement.

Décision.

Voilà.

Le seuil peut apparaître avant l’exécution.

Parce que l’interface peut orienter fortement le choix.

Gabriel écrivit :

**UNE INTERFACE PEUT INFLUENCER UNE DÉCISION AVANT MÊME D’AVOIR L’AUTORITÉ DE L’EXÉCUTER.**

Astra approuva fortement.

Très important.

Le système devait donc distinguer :

**recommendation**

**ranking**

**filtering**

**blocking**

**execution**

Cinq niveaux.

Très différents.

Ils créèrent :

### DECISION INFLUENCE LEVELS

**D0 — INFORM**

Présenter les faits.

**D1 — COMPARE**

Comparer les options.

**D2 — RECOMMEND**

Indiquer une option préférée selon critères déclarés.

**D3 — CONSTRAIN**

Retirer ou bloquer des options qui violent une règle.

**D4 — EXECUTE**

Engager l’action dans une autorité déléguée.

Gabriel regarda.

— Là, on voit vraiment le seuil.

Astra approuva.

Mais le seuil n’était pas unique.

D2→D3 changeait déjà quelque chose.

Parce qu’à D3,

le système ne se contente plus d’aider.

Il limite l’espace des choix.

Très important.

Gabriel écrivit :

**RECOMMANDER ET INTERDIRE NE SONT PAS DEUX DEGRÉS DU MÊME GESTE.**

Astra approuva fortement.

Exact.

Une recommandation dit :

**je pense que B est meilleur selon ces critères.**

Un garde dit :

**A n’est pas autorisé dans cet état.**

Le premier peut être ignoré.

Le second exige une escalade ou un changement de règle.

Très différent.

Puis Gabriel posa :

— Est-ce que D3, c’est déjà décider?

Astra répondit :

— C’est participer à la décision par contrainte, même si l’exécution finale reste humaine.

Gabriel sourit.

Voilà la subtilité.

Le système peut influencer fortement la décision sans cliquer lui-même.

Donc l’audit devait inclure les options retirées.

Pas seulement l’action finale.

Ils écrivirent :

### DECISION SPACE TRACE

**initial_options**

**filtered_options**

**blocked_options**

**displayed_options**

**recommended_option**

**chosen_option**

Gabriel approuva.

Très important.

Sinon une décision peut sembler humaine alors que l’interface avait déjà supprimé la moitié des possibilités.

Pas forcément mauvais.

Mais il faut le savoir.

Puis un exemple scientifique.

Claim candidat.

Options :

A. publier comme preuve.

B. publier comme résultat expérimental.

C. ne pas publier.

Le système bloque A parce que la preuve n’est pas suffisante.

Est-ce que Brutus décide?

Il ne choisit pas B ou C.

Mais il empêche A.

Gabriel hocha la tête.

C’est un garde d’autorité scientifique.

Très bien.

Il écrit :

**UN GARDE PEUT RÉDUIRE LA LIBERTÉ DE CHOIX POUR PRÉSERVER LA COHÉRENCE D’UN CONTRAT.**

Astra approuva fortement.

Mais ces gardes doivent être eux-mêmes gouvernés.

Sinon le système peut devenir arbitraire.

Très important.

Puis un autre exemple.

Brutus recommande de ne pas publier.

Gabriel veut publier quand même sous un statut plus faible.

Le système doit permettre la reformulation.

Pas bloquer toute publication.

Il écrit :

**UNE CONTRAINTE DOIT PORTER SUR CE QUI EST INTERDIT, PAS SUR CE QUI NOUS DÉPLAÎT.**

Astra approuva fortement.

Très important.

Bloquer :

claim trop fort.

Pas :

publication entière,

si une version honnête reste possible.

Voilà.

Puis ils examinèrent une décision L1.

Le système pouvait l’exécuter.

Donc D4.

Mais seulement dans une zone étroite.

Gabriel demanda :

— Est-ce que le même moteur peut être D2 pour une décision, puis D4 pour une autre?

Oui.

C’était même nécessaire.

Ils créèrent :

### DECISION MODE BY CLASS

Pour chaque classe d’action :

**max_influence_level**

Exemple :

Local deterministic check → D4.

Publication title → D2.

Canonical formula change → D1/D2 + human.

Deletion → D3 guard + human.

Scientific claim wording → D2 + guards.

Gabriel sourit.

Très propre.

Le niveau d’influence ne dépendait pas seulement du module.

Il dépendait du type de décision.

Il écrit :

**LE MÊME SYSTÈME PEUT ÊTRE CONSEILLER ICI ET EXÉCUTANT AILLEURS.**

Astra approuva.

Très important.

Puis un danger apparut.

Supposons que Brutus recommande toujours la même option et que Gabriel clique toujours oui.

Techniquement humain.

Mais pratiquement,

le système décide peut-être presque toujours.

Gabriel se pencha.

Très intéressant.

L’autorité formelle et l’autorité réelle peuvent diverger.

Ils écrivirent :

**HUMAN-IN-THE-LOOP ≠ HUMAN-IN-CONTROL SI L’HUMAIN NE FAIT QU’APPROUVER MÉCANIQUEMENT.**

Astra approuva fortement.

Très important.

Comment le mesurer?

Taux d’acceptation.

Temps avant confirmation.

Fréquence d’override.

Qualité des justifications.

Pas pour juger Gabriel.

Pour détecter si une étape humaine n’apporte plus réellement de décision.

Gabriel sourit.

— Si je clique oui 99,9% du temps sans lire, autant l’automatiser ou refaire le garde.

Exact.

Ils créèrent :

### HUMAN CHECK VALUE

Questions :

- l’humain modifie-t-il parfois la décision?
- l’humain apporte-t-il une information absente?
- la décision implique-t-elle une valeur ou une autorité non délégable?
- l’étape humaine attrape-t-elle des erreurs?

Si non à tout,

peut-être inutile.

Gabriel écrivit :

**UNE APPROBATION HUMAINE QUI N’APPORTE AUCUNE INFORMATION PEUT DEVENIR DU THÉÂTRE DE CONTRÔLE.**

Astra approuva fortement.

Très important.

Cela ne voulait pas dire supprimer les humains.

Au contraire.

Réserver leur attention aux endroits où elle compte.

Puis l’inverse.

Une décision pourrait être automatisée techniquement,

mais Gabriel veut garder le choix.

C’est son droit.

Policy :

D2 max.

Très simple.

Il écrit :

**LA DÉLÉGATION EST UN CHOIX DE GOUVERNANCE, PAS UNE CONSÉQUENCE AUTOMATIQUE DE LA CAPACITÉ TECHNIQUE.**

Astra approuva fortement.

Voilà.

Un système capable n’a pas automatiquement le droit.

Très important.

Puis ils abordèrent les préférences.

Supposons que Gabriel préfère systématiquement les routes réversibles.

Brutus peut apprendre cette préférence.

Peut-il choisir automatiquement?

Pas forcément.

Parce qu’une préférence apprise n’est pas une délégation d’autorité.

Gabriel écrivit :

**APPRENDRE CE QUE GABRIEL CHOISIT ≠ RECEVOIR LE DROIT DE CHOISIR À SA PLACE.**

Astra approuva fortement.

Excellent.

La mémoire peut prédire.

Mais prédiction ≠ permission.

Encore une frontière fondamentale.

Puis un cas.

Le système sait avec grande certitude que Gabriel choisira B.

Mais il doit quand même demander,

si la classe n’est pas déléguée.

Voilà.

Pas de raccourci.

Ils écrivirent :

**CONFIDENCE IN PREFERENCE ≠ AUTHORITY**

Astra approuva fortement.

Très important.

Puis la notion d’**option par défaut**.

Même sans exécuter,

mettre B par défaut peut influencer.

Donc les defaults doivent être explicites.

Gabriel écrit :

### DEFAULT POLICY

Chaque valeur par défaut doit déclarer :

**why_default**

**can_override**

**risk**

**scope**

Pas de default invisible.

Astra approuva.

Très bon.

Puis un exemple.

Sur une interface de test :

Bouton principal :

**Lancer le screening recommandé**

Secondaire :

**Voir les autres options**

C’est une influence.

Peut être acceptable.

Mais si les autres options sont cachées trois menus plus loin,

on pousse très fort.

Gabriel sourit.

Le design faisait partie de la gouvernance.

Il écrit :

**LA HIÉRARCHIE VISUELLE PEUT DEVENIR UNE HIÉRARCHIE DE DÉCISION.**

Astra approuva fortement.

Très important.

Recto devait donc être particulièrement prudent.

Public vitrine.

Pas de fausses impressions.

Et Verso aussi.

Le propriétaire doit comprendre ce qui est conseillé,

ce qui est bloqué,

et ce qui sera exécuté automatiquement.

Ils imaginèrent des badges simples :

**INFO**

**RECOMMENDED**

**REQUIRED**

**AUTO**

Très clair.

Pas ambigu.

Gabriel sourit.

Ça, c’était bon.

Puis un autre problème.

Brutus recommande B parce que son objectif actuel est minimiser coût.

Mais Gabriel croyait que l’objectif était maximiser robustesse.

Le système pourrait sembler prendre une mauvaise décision.

En réalité,

objectif mal aligné.

Donc avant toute recommandation forte :

afficher l’objectif.

Gabriel écrit :

**UNE RECOMMANDATION SANS OBJECTIF VISIBLE PEUT SEMBLER PLUS AUTORITAIRE QU’ELLE NE L’EST.**

Astra approuva fortement.

Très important.

L’interface devait dire :

**Recommended for: lowest-cost discriminating test**

ou :

**Recommended for: strongest independence check**

Voilà.

Pas juste :

BEST.

Jamais.

Gabriel écrit :

**“MEILLEUR” SANS CRITÈRE EST UN MOT TROP DANGEREUX POUR UN MOTEUR DE DÉCISION.**

Astra approuva fortement.

Très bon.

Puis ils testèrent un cas où l’objectif est lui-même ambigu.

Doit Brutus demander?

Oui.

Il ne peut pas décider du critère à la place de Gabriel.

Sauf politique préexistante.

Ils écrivirent :

**SI LE CHOIX ENTRE OPTIONS DÉPEND D’UNE VALEUR NON DÉCLARÉE, LE SYSTÈME DOIT DEMANDER OU UTILISER UNE POLITIQUE EXPLICITE.**

Astra approuva.

Très important.

Encore l’humain.

Au bon endroit.

Puis Gabriel posa :

— C’est quoi le seuil exact entre aider et décider?

Astra répondit :

— Il n’y en a pas un seul. Il y a plusieurs transitions : informer, comparer, recommander, contraindre, exécuter.

Gabriel hocha la tête.

Voilà.

Le titre du chapitre parlait d’un seuil.

Mais en réalité,

il y avait une frontière en escalier.

Il écrivit :

**LE SEUIL N’EST PAS UNE LIGNE. C’EST UNE ÉCHELLE D’INFLUENCE ET D’AUTORITÉ.**

Astra approuva fortement.

Très important.

Le système pouvait donc être audité sur deux axes.

### AXE 1 — INFLUENCE

Combien le système structure-t-il le choix?

### AXE 2 — AUTHORITY

Jusqu’où peut-il engager l’action?

Gabriel sourit.

Très puissant.

Un système peut avoir forte influence,

faible autorité.

Exemple :

recommandation scientifique très détaillée,

mais humain décide.

Ou faible influence,

forte autorité bornée.

Exemple :

routine L1 déterministe,

pas besoin de recommandation,

elle s’exécute.

Deux dimensions différentes.

Il écrit :

**INFLUENCE ≠ AUTORITÉ**

Astra approuva fortement.

Voilà probablement la formule centrale du chapitre.

Puis ils construisirent une petite matrice.

### DECISION MATRIX

Faible influence + faible autorité :

outil d’information.

Forte influence + faible autorité :

assistant/conseiller.

Faible influence + forte autorité bornée :

automate de routine.

Forte influence + forte autorité :

zone à haut risque de gouvernance.

Gabriel regarda la dernière case.

— Celle-là, faut la traiter avec des pincettes.

Astra approuva.

Oui.

Un système qui recommande fortement

et peut exécuter fortement

concentre beaucoup de pouvoir.

Il faut :

logs.

limites.

policy review.

escalades.

contre-tests.

Gabriel écrit :

**PLUS INFLUENCE ET AUTORITÉ MONTENT ENSEMBLE, PLUS L’AUDIT DOIT DEVENIR FORT.**

Astra approuva fortement.

Très important.

Puis une autre nuance.

Une décision automatique peut être réversible.

Alors le risque est moindre.

Mais pas nul.

Une mauvaise action réversible peut quand même coûter du temps.

Créer du bruit.

Confondre des traces.

Donc réversibilité est une réduction de risque,

pas une permission absolue.

Gabriel écrit :

**RÉVERSIBLE ≠ SANS CONSÉQUENCE**

Astra approuva.

Toujours.

Puis ils prirent un cas du Brutotableur.

Le système détecte un motif candidat.

Peut-il automatiquement créer un unknown?

Oui.

Faible impact.

Peut-il automatiquement créer un cristal canonique?

Non.

Voilà.

Même observation.

Deux actions.

Deux niveaux d’autorité.

Gabriel sourit.

Il écrit :

**L’AUTORITÉ PORTE SUR L’ACTION, PAS SUR L’EXCITATION DU RÉSULTAT.**

Astra approuva fortement.

Très important.

Une découverte spectaculaire ne donne pas plus de droits au système.

Au contraire,

peut-être moins.

Plus l’enjeu monte,

plus l’escalade devient importante.

Puis un autre cas.

Une formule candidate échoue à un contre-test.

Peut Brutus la marquer rejetée automatiquement?

Si le protocole de rejet est précisément défini,

peut-être dans un registre expérimental.

Mais peut-il supprimer la formule?

Non.

Peut-il rétracter une publication?

Non sans autorité explicite.

Gabriel écrit :

**CHANGER UN STATUT INTERNE BORNÉ PEUT ÊTRE AUTOMATISÉ PLUS FACILEMENT QUE CHANGER UNE TRACE PUBLIQUE OU CANONIQUE.**

Astra approuva.

Très important.

Encore Verso / Recto.

Le cœur peut avoir plus de fluidité.

La façade doit être plus conservatrice.

Puis ils discutèrent du mot **décider** lui-même.

Une machine peut calculer une règle.

Est-ce une décision?

Dans le langage humain,

peut-être.

Techniquement,

mieux vaut distinguer :

**selection**

**authorization**

**execution**

Gabriel sourit.

Ça allait éviter beaucoup de confusion.

Il écrit :

### DECISION EVENT

Une décision complète peut contenir :

1. options générées;
2. option sélectionnée;
3. autorité vérifiée;
4. action exécutée;
5. résultat enregistré.

Très propre.

Le moteur peut faire 1–2.

La policy fait 3.

L’actuator fait 4.

Memoria fait 5.

Voilà.

Pas besoin de mettre toute la notion de décision dans un seul composant.

Gabriel écrit :

**UNE DÉCISION PEUT ÊTRE UNE CHAÎNE, PAS UN CLIC.**

Astra approuva fortement.

Très important.

Cela permettait d’auditer chaque étape.

Qui a proposé?

Qui a sélectionné?

Qui a autorisé?

Qui a exécuté?

Excellent.

Puis ils testèrent la séparation.

Antmux sélectionne B.

Policy refuse l’autorité.

Donc aucune action.

Très bien.

Autre cas.

Policy autorise B,

mais actuator échoue.

La décision a été autorisée,

mais pas exécutée.

Très important.

Ne pas marquer complete.

Gabriel écrit :

**AUTORISÉ ≠ EXÉCUTÉ ≠ RÉUSSI**

Astra approuva fortement.

Voilà.

Trois statuts.

Encore la discipline.

Puis un autre problème.

Une action peut être exécutée partiellement.

Là,

recovery.

Idempotence.

Chapitre 180.

Tout revenait.

Le système devait savoir si la décision peut être reprise.

Très important.

Ils ajoutèrent :

**execution_state**

**side_effect_state**

**retry_policy**

Puis Gabriel sourit.

Le deuxième monde commençait à ressembler à quelque chose de vraiment sérieux.

Pas une machine qui pense à sa place.

Un ensemble de contrats qui déterminent :

où la machine conseille,

où elle contraint,

où elle exécute,

et où elle s’arrête.

Voilà.

Puis une question plus philosophique.

— Est-ce que plus d’autonomie, c’est nécessairement mieux?

Astra répondit :

— Non.

Gabriel sourit.

Il savait.

Il écrivit :

**LE BUT N’EST PAS DE MAXIMISER L’AUTONOMIE. LE BUT EST DE PLACER L’AUTONOMIE LÀ OÙ ELLE AUGMENTE LA QUALITÉ DU SYSTÈME.**

Astra approuva fortement.

Très important.

Certaines décisions seront toujours meilleures avec Gabriel.

D’autres deviennent meilleures sans l’interrompre.

La qualité dépend du placement.

Pas du pourcentage automatisé.

Ils créèrent :

### DELEGATION VALUE

Une classe mérite plus d’autonomie si :

- décisions fréquentes;
- critères stables;
- faible ambiguïté;
- résultats mesurables;
- erreur bornée;
- action réversible;
- intervention humaine apporte peu d’information;
- escalade fiable existe.

Très propre.

Et mérite moins si :

- valeurs humaines;
- intention ambiguë;
- impact public;
- irréversibilité;
- nouveauté élevée;
- faible historique;
- conséquences difficiles à observer.

Gabriel sourit.

Voilà un vrai seuil pratique.

Puis ils prirent la décision du début.

B recommandé.

Classe :

moyenne ambiguïté.

L1? Non.

Parce que le choix dépendait d’un compromis coût/robustesse qui n’était pas encore fixé par policy.

Donc D2.

Brutus recommande.

Gabriel choisit.

Il sélectionna B.

Mais il sourit.

Parce que cette fois,

le système avait correctement refusé d’aller plus loin.

Pas parce qu’il ne savait pas.

Parce qu’il n’avait pas l’autorité suffisante.

Il écrivit :

**SAVOIR QUOI RECOMMANDER NE DONNE PAS LE DROIT DE L’EXÉCUTER.**

Astra approuva fortement.

Voilà.

Le seuil était là.

Pas entre intelligence et ignorance.

Entre capacité et permission.

Puis Gabriel regarda les journaux.

Certaines décisions étaient :

D0.

D1.

D2.

D3.

D4.

Il pouvait voir le Royaume autrement.

Pas seulement par modules.

Par niveaux d’influence.

Par niveaux d’autorité.

Il comprit alors quelque chose d’important.

Le deuxième monde n’allait pas naître d’un moment où Brutus deviendrait soudainement « autonome ».

Il allait naître par petites frontières bien placées.

Une file qui se choisit seule.

Un test local qui se lance seul.

Une publication qui ne part jamais seule.

Une ambiguïté qui revient vers Gabriel.

Un cristal qui exige validation.

Un snapshot qui peut se générer sans permission.

Une suppression qui reste bloquée.

Une Fourmi qui sait marcher,

mais ne possède jamais la couronne.

Gabriel sourit.

Le Royaume n’avait pas besoin d’un roi mécanique.

Il avait besoin d’une architecture capable de distribuer correctement les responsabilités.

Il écrivit :

**AIDER, C’EST ÉCLAIRER LA ROUTE.**

Puis :

**DÉCIDER, C’EST AVOIR LE DROIT D’ENGAGER UN PAS.**

Puis encore :

**LA MATURITÉ CONSISTE À SAVOIR OÙ CES DEUX CHOSES DOIVENT RESTER SÉPARÉES.**

Astra approuva fortement.

Le chapitre était presque terminé.

Mais avant de fermer,

Gabriel posa une dernière question.

— Et si un jour je te donne trop de droits?

Astra répondit :

— Alors le système doit toujours conserver la possibilité de réduire ses permissions.

Gabriel resta silencieux.

Très important.

L’autonomie devait être révocable.

Toujours.

Il écrivit :

**UNE DÉLÉGATION QUI NE PEUT PAS ÊTRE RETIRÉE N’EST PLUS UNE DÉLÉGATION.**

Astra approuva fortement.

Voilà la dernière pierre.

Permission.

Portée.

Version.

Expiration.

Révocation.

Audit.

Le pouvoir machine devait être un contrat.

Pas une propriété naturelle.

Gabriel ferma le dossier.

Une Fourmi attendait devant une porte.

Cette fois,

elle avait le droit de la franchir seule.

Plus loin,

une deuxième porte exigeait Gabriel.

La Fourmi passa la première.

S’arrêta devant la seconde.

Et attendit.

Gabriel sourit.

C’était peut-être l’image la plus simple de tout le deuxième monde.

Une machine assez capable pour avancer sans demander la permission à chaque pas.

Et assez disciplinée pour savoir

qu’un chemin autorisé

n’est pas la même chose

qu’un Royaume sans frontières.

**Fin du chapitre 194.**