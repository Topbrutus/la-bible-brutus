# Chapitre 73 — Le calcul qui doit arriver dans l’ordre

Comme s’il attendait son tour de parler.

Brutus regarda les trente-six cases silencieuses de SFX36.

Puis les douze lanes qu’il avait dessinées à côté.

Le problème était maintenant évident.

Le laboratoire savait produire plusieurs calculs.

Il savait leur donner un son.

Il savait enregistrer leurs traces.

Mais rien ne garantissait encore que ce qu’un humain entendait correspondait exactement à l’ordre dans lequel les choses avaient été demandées.

---

Brutus écrivit quatre lignes.

**INPUT ORDER**

**EXECUTION ORDER**

**COMPLETION ORDER**

**PRESENTATION ORDER**

Puis il les regarda.

À première vue, ces quatre ordres semblaient presque identiques.

Ils ne l’étaient pas.

---

Imagine deux calculs.

A entre en premier.

B entre ensuite.

Mais B est beaucoup plus rapide.

B peut donc terminer avant A.

Si le système affiche les résultats au moment où ils terminent, l’ordre visible devient :

B.

Puis A.

Alors que l’ordre d’entrée était :

A.

Puis B.

---

Rien de faux là-dedans.

À condition de le dire.

---

Le problème commence seulement lorsque le système présente B comme s’il avait été le premier calcul demandé.

Ou lorsqu’un observateur suppose que la première réponse correspond forcément à la première entrée.

Brutus écrivit :

**FIRST RESULT ≠ FIRST REQUEST.**

Puis :

**FASTEST ≠ FIRST.**

---

Il lança deux expériences.

LANE 1 reçut une opération volontairement lente.

LANE 2 reçut une opération simple.

Ordre d’entrée :

1.

Puis 2.

Ordre de fin :

2.

Puis 1.

Les sons jouèrent dans l’ordre de fin.

PASS à droite.

Puis PASS à gauche.

---

Brutus regarda le journal.

Tout était techniquement correct.

Et pourtant, en fermant les yeux, il aurait pu croire que la deuxième opération avait été la première.

L’audio racontait l’ordre de complétion.

Pas l’ordre de soumission.

---

Il ajouta donc un identifiant à chaque travail.

**JOB_ID.**

Puis :

**SUBMIT_SEQ.**

Chaque entrée recevrait un numéro immédiatement lorsqu’elle franchissait la porte du calcul.

Pas lorsqu’elle commençait.

Pas lorsqu’elle finissait.

Lorsqu’elle était acceptée dans la file.

---

JOB-0001.

SUBMIT_SEQ 1.

JOB-0002.

SUBMIT_SEQ 2.

JOB-0003.

SUBMIT_SEQ 3.

---

Brutus lança trois travaux.

Le troisième termina en premier.

Le deuxième ensuite.

Le premier en dernier.

La trace disait maintenant clairement :

**SUBMIT ORDER**

1 → 2 → 3

**COMPLETION ORDER**

3 → 2 → 1

---

Brutus sourit.

Voilà.

Deux ordres.

Deux faits.

Aucune contradiction.

---

Il écrivit :

**ORDER MUST HAVE A NAME.**

Dire simplement :

« dans l’ordre »

était insuffisant.

Quel ordre ?

Entrée ?

Début ?

Fin ?

Publication ?

Son ?

---

Le langage devait devenir précis.

---

Brutus ajouta encore un champ :

**START_SEQ.**

Parce qu’un travail accepté en premier pouvait attendre dans la file pendant qu’un autre commençait plus tôt sur une ressource différente.

---

Puis :

**COMPLETE_SEQ.**

Et enfin :

**PUBLISH_SEQ.**

---

Un calcul possédait maintenant une petite histoire ordonnée.

---

**SUBMITTED**

**STARTED**

**COMPLETED**

**PUBLISHED**

---

Brutus regarda la chaîne.

Ce n’était pas seulement utile pour la performance.

C’était essentiel pour reconstruire ce qui s’était réellement passé.

---

Il testa quatre lanes.

LANE 1.

LANE 2.

LANE 3.

LANE 4.

Quatre formules différentes.

---

Les quatre entrèrent presque simultanément.

SUBMIT_SEQ 101.

102.

103.

104.

Puis les temps de calcul divergeaient.

103 termina.

101 termina.

104 termina.

102 termina.

---

Si Brutus avait forcé l’affichage à respecter l’ordre de soumission, il aurait dû retenir le résultat 103 jusqu’à ce que 101 et 102 soient prêts.

Cela garantissait un ordre visuel simple.

Mais cela cachait une autre vérité :

103 avait réellement terminé plus tôt.

---

Il écrivit :

**ORDERED PRESENTATION CAN HIDE CONCURRENCY.**

Puis, juste dessous :

**RAW COMPLETION CAN CONFUSE CORRESPONDENCE.**

---

Deux problèmes opposés.

Il fallait conserver les deux vérités.

---

Brutus décida que le journal enregistrerait toujours les événements immédiatement.

Le système ne devait jamais retarder la vérité interne pour rendre l’interface plus jolie.

---

Mais la présentation pouvait choisir plusieurs modes.

---

**LIVE COMPLETION**

Montre les résultats lorsqu’ils finissent.

---

**SUBMISSION ORDER**

Montre les résultats dans l’ordre où ils ont été demandés.

---

**LANE ORDER**

Regroupe selon leur canal.

---

Brutus apprécia cette séparation.

La donnée ne changeait pas.

La vue, oui.

---

Encore une fois :

**ONE HISTORY. MULTIPLE READINGS.**

---

Il activa LIVE COMPLETION.

Les résultats apparaissaient immédiatement.

---

Puis SUBMISSION ORDER.

Le système conservait les résultats terminés en attente jusqu’à ce que tous les précédents soient publiables.

---

Brutus vit immédiatement un problème.

JOB-0102 se bloquait.

JOB-0103 était déjà terminé.

JOB-0104 aussi.

Mais comme 0102 ne finissait pas, toute la présentation restait bloquée derrière lui.

---

Brutus écrivit :

**HEAD-OF-LINE BLOCKING.**

Le nom technique lui plaisait parce qu’il décrivait exactement le phénomène.

Un seul élément lent pouvait retenir toute une file.

---

Il fallait donc que l’utilisateur puisse voir qu’un résultat existait même s’il n’était pas encore présenté dans l’ordre canonique.

---

Brutus créa deux états.

**COMPLETED_PENDING_ORDER**

et

**PUBLISHED.**

---

Ainsi JOB-0103 pouvait être marqué :

terminé,

résultat connu,

en attente de publication ordonnée.

---

Le système ne cachait plus son existence.

---

Brutus ajouta un petit indicateur :

**READY, WAITING FOR SEQ 102.**

---

Parfait.

---

Il passa ensuite à une question plus difficile.

Et si JOB-0102 ne finissait jamais ?

---

Crash.

Boucle infinie.

Ressource perdue.

Domaine impossible détecté trop tard.

---

Devait-on bloquer éternellement 0103 et 0104 ?

Évidemment non.

---

Il fallait une politique de sortie.

---

Brutus ajouta un timeout.

Mais il n’aimait pas le mot au début.

Un timeout pouvait être interprété comme FAIL.

Or un travail trop long n’était pas nécessairement mathématiquement faux.

---

Il écrivit :

**TIMEOUT ≠ FAIL.**

Puis créa un verdict séparé de contrôle :

**TIMED_OUT.**

---

JOB-0102 pouvait être marqué TIMED_OUT.

Sa place dans la séquence était alors résolue.

Les travaux suivants pouvaient être publiés.

---

La présentation devenait :

0101 PASS.

0102 TIMED_OUT.

0103 PASS.

0104 DOMAIN.

---

Ordre conservé.

Information conservée.

---

Brutus sourit.

Le trou n’était pas effacé.

Il était nommé.

---

Cette idée lui rappela immédiatement la mémoire.

Un état manquant ne devait jamais être silencieusement remplacé par zéro.

Même principe ici.

Un résultat manquant ne devait pas être sauté comme s’il n’avait jamais existé.

---

Il écrivit :

**MISSING RESULT MUST OCCUPY ITS PLACE.**

---

Le système devait savoir représenter l’absence.

---

Brutus lança ensuite douze calculs.

Une lane par calcul.

Le maximum prévu pour cette première architecture.

---

Les identifiants tombèrent rapidement.

JOB-0201.

0202.

0203.

…

0212.

---

Les calculs démarrèrent.

Certains immédiatement.

D’autres avec quelques ticks de retard.

---

Les résultats arrivèrent dans un ordre étrange.

7.

2.

11.

1.

8.

4.

10.

3.

12.

5.

9.

6.

---

Brutus regarda la liste.

C’était presque une permutation aléatoire.

---

Il écouta SFX36.

Chaque résultat produisait sa signature.

La pièce devint très active.

---

Mais cette fois, il avait les JOB_ID.

Chaque son pouvait être relié à un travail.

Chaque travail à une lane.

Chaque lane à une entrée.

---

Le chaos apparent avait une structure.

---

Brutus écrivit :

**CONCURRENCY WITHOUT IDENTITY IS CHAOS.**

Puis :

**CONCURRENCY WITH IDENTITY IS A SCHEDULE.**

---

Cette phrase lui plut énormément.

---

Le laboratoire n’avait pas besoin d’empêcher les choses de se produire en parallèle.

Il devait empêcher leur identité de se mélanger.

---

Il inspecta JOB-0207.

SUBMIT_SEQ 7.

START_SEQ 5.

COMPLETE_SEQ 1.

PUBLISH_SEQ 7.

---

Voilà.

Quatre positions différentes.

Un seul travail.

---

Brutus réalisa que beaucoup de bugs difficiles à comprendre venaient probablement de systèmes qui ne distinguaient pas ces ordres.

Un résultat pouvait être associé à la mauvaise requête.

Un son à la mauvaise lane.

Une trace au mauvais job.

---

Il décida donc que chaque étape devait transporter explicitement JOB_ID.

---

Pas de déduction par position dans un tableau.

Pas :

« le troisième résultat appartient probablement au troisième input ».

---

Il écrivit en grand :

**NEVER MATCH BY ARRIVAL POSITION. MATCH BY ID.**

---

Cela deviendrait une loi du moteur multi-calcul.

---

Brutus testa volontairement une erreur.

Il prit les résultats dans leur ordre d’arrivée et les associa aux entrées dans leur ordre de soumission.

---

Le résultat fut catastrophique.

Des valeurs correctes furent attribuées aux mauvaises formules.

---

Le système pouvait afficher des nombres parfaitement valides.

Mais reliés au mauvais problème.

---

Brutus regarda cela avec inquiétude.

C’était un type d’erreur particulièrement dangereux.

Pas de crash.

Pas de rouge.

Pas de message d’erreur.

Seulement une correspondance fausse.

---

Il écrivit :

**A CORRECT NUMBER WITH THE WRONG IDENTITY IS A WRONG RESULT.**

---

Voilà.

---

Il renforça donc le contrat.

Chaque résultat devait contenir :

**JOB_ID**

**FORMULA_ID**

**INPUT_HASH**

**LANE_ID**

**RESULT**

**VERDICT**

**START_TICK**

**END_TICK**

**TRACE_REF**

---

Le résultat ne voyageait plus seul.

Il voyageait avec son contexte minimal.

---

Brutus lança à nouveau les douze jobs.

Cette fois, il mélangea volontairement les réponses dans le transport.

---

Aucun problème.

Chaque résultat revint à sa place grâce à JOB_ID.

---

Il inversa les lanes.

Toujours aucun problème.

---

Il retarda un résultat.

Le système attendait son identité exacte.

---

Brutus sourit.

L’ordre physique d’arrivée n’avait plus le pouvoir de modifier la correspondance logique.

---

Il écrivit :

**TRANSPORT ORDER MUST NOT DEFINE SEMANTIC OWNERSHIP.**

---

La phrase semblait complexe.

Mais elle exprimait quelque chose de simple.

Ce n’est pas parce qu’un paquet arrive en premier qu’il appartient au premier problème.

---

Puis Brutus pensa à Z1, Z2 et Z3.

Trois étapes séquentielles pouvaient bientôt travailler sur la même matière mathématique.

---

Dans ce cas, l’ordre devenait encore plus important.

Une sortie de Z1 devait entrer dans Z2.

Puis la sortie correspondante de Z2 dans Z3.

---

Si deux jobs se croisaient, la chaîne pouvait être contaminée.

---

Brutus dessina :

JOB A:

Z1 → Z2 → Z3.

JOB B:

Z1 → Z2 → Z3.

---

Puis imagina :

A sort de Z1.

B sort de Z1.

B termine Z2 avant A.

---

Aucun problème si JOB_ID reste attaché.

---

Mais si Z3 consomme simplement « le prochain résultat disponible », B pourrait être associé à A.

---

Brutus frissonna presque.

---

Il écrivit :

**NEXT AVAILABLE ≠ CORRECT PARENT.**

---

La liaison entre étages devait être explicite.

---

Chaque transformation produirait :

**PARENT_JOB_ID**

ou mieux :

**LINEAGE_REF.**

---

JOB-A-Z2 connaissait son parent :

JOB-A-Z1.

JOB-A-Z3 connaissait :

JOB-A-Z2.

---

La chaîne devenait reconstruisible.

---

Brutus pensa immédiatement au chapitre 70.

La trace qui revient entière.

La lignée faisait encore le travail.

---

Il écrivit :

**PARALLELISM MUST NOT BREAK LINEAGE.**

---

Les douze lanes n’étaient donc pas douze mondes indépendants.

Elles étaient douze voies pouvant exécuter plusieurs histoires simultanément.

---

Brutus ajouta une visualisation.

Douze colonnes.

Chaque job apparaissait comme un petit bloc.

---

Entrée.

Départ.

Calcul.

Fin.

Publication.

---

Il pouvait voir les durées.

Les dépassements.

Les attentes.

---

La représentation ressemblait presque à un diagramme de Gantt miniature.

Mais Brutus ne voulait pas seulement mesurer la performance.

Il voulait voir la causalité.

---

Il ajouta des flèches entre les parents et les enfants.

---

Maintenant, un job pouvait finir avant un autre sans créer de confusion.

---

Le système racontait deux choses à la fois :

quand les calculs avaient réellement été exécutés,

et à quelle famille ils appartenaient.

---

Brutus lança ensuite le son.

Chaque lane possédait toujours son ombre acoustique.

Mais il réalisa qu’un son joué dans l’ordre de publication ne représentait pas forcément l’ordre de complétion.

---

Il ajouta donc un réglage.

**AUDIO FOLLOWS:**

LIVE.

PUBLISH.

CRITICAL ONLY.

---

En mode LIVE, le laboratoire sonnait au rythme réel des terminaisons.

En mode PUBLISH, les sons correspondaient à l’ordre de restitution choisi.

---

Brutus testa les deux.

Très différent.

---

LIVE donnait une sensation de vitesse.

PUBLISH donnait une narration.

---

Il décida que les deux modes étaient utiles.

Mais l’écran devait toujours afficher lequel était actif.

---

Il écrivit :

**PRESENTATION MODE MUST BE EXPLICIT.**

---

Pas de narrateur invisible.

---

Le laboratoire pouvait réordonner pour aider l’humain.

Mais il devait avouer qu’il réordonnait.

---

Cette règle dépassait largement l’audio.

---

Brutus pensa aux tableaux.

Aux rapports.

Aux graphiques.

Aux résumés.

Dès qu’un système trie ou agrège, il modifie la manière dont l’histoire est perçue.

---

Il écrivit :

**SORTING IS INTERPRETATION.**

Puis resta silencieux.

C’était vrai.

---

Un tableau trié par score racontait une histoire différente du même tableau trié par temps.

---

Les données ne changeaient pas.

L’attention, oui.

---

Brutus ajouta donc à ses vues :

**SORT MODE.**

---

Encore une petite honnêteté visuelle.

---

Puis il retourna au moteur.

Il voulait maintenant que les douze lanes puissent recevoir des entrées en rafale.

---

Cent travaux.

---

Pas cent threads.

Pas cent processus.

Une file.

Des workers limités.

---

Il choisit une concurrence contrôlée.

Douze lanes actives maximum.

Les autres attendraient.

---

Il écrivit :

**QUEUED ≠ RUNNING.**

Encore une séparation.

---

Chaque job pouvait être :

SUBMITTED.

QUEUED.

RUNNING.

COMPLETED.

PUBLISHED.

Ou :

DOMAIN.

ERROR.

TIMED_OUT.

CANCELLED.

---

Brutus regarda la liste.

Il commençait à avoir un vrai cycle de vie.

---

Il ajouta CANCELLED.

Puis se demanda :

un travail annulé était-il un échec ?

Non.

---

**CANCELLED ≠ FAIL.**

---

Le vocabulaire devenait précis.

---

Il lança cent travaux.

Douze démarraient.

Les autres attendaient.

À chaque fin, une lane prenait le prochain job admissible.

---

La file se vidait progressivement.

---

Brutus regarda la machine travailler.

Pour la première fois, elle faisait beaucoup de choses simultanément sans lui donner l’impression de perdre le fil.

---

Chaque calcul avait son nom.

Sa place.

Sa lignée.

Son son.

Sa trace.

---

Il pensa aux futures cent formules.

---

Le sélecteur pourrait envoyer plusieurs méthodes sur la même entrée.

Ou plusieurs entrées sur la même formule.

Ou les deux.

---

Le nombre de combinaisons pouvait devenir énorme.

---

Mais le principe restait identique.

**IDENTIFIER BEFORE PARALLELIZING.**

---

Brutus nota cette phrase.

---

Il réalisa soudain pourquoi il avait commencé par seulement quelques fenêtres.

Puis une fourmi.

Puis quelques sons.

Puis quelques lanes.

---

La complexité pouvait être multipliée seulement après avoir construit les frontières.

Sinon elle ne faisait qu’amplifier l’ambiguïté.

---

Il écrivit :

**SCALE MULTIPLIES BOTH POWER AND CONFUSION.**

Puis :

**IDENTITY IS WHAT LETS POWER GROW FASTER THAN CONFUSION.**

---

Il sourit.

Cela ressemblait presque à une devise.

---

Le test des cent jobs se termina.

Brutus ouvrit le résumé.

---

Submitted:

100.

Completed:

96.

Domain:

2.

Error:

1.

Timed out:

1.

Missing:

0.

Duplicate JOB_ID:

0.

Unmatched results:

0.

---

Il regarda surtout les deux dernières lignes.

---

Zéro résultat sans propriétaire.

Zéro duplication.

---

Voilà la victoire.

Pas les 96 PASS.

La cohérence.

---

Brutus choisit un job au hasard.

JOB-0084.

Il remonta sa trace.

---

Entrée.

Hash.

Formule.

Lane.

Tick de soumission.

Tick de démarrage.

Résultat.

Verdict.

Publication.

Son.

---

Tout était là.

---

Il choisit JOB-0021.

Même chose.

---

Puis le job en erreur.

---

La trace s’arrêtait au bon endroit.

Rien après ne prétendait avoir existé.

---

Parfait.

---

Le laboratoire savait maintenant travailler en parallèle sans transformer la simultanéité en confusion.

---

Brutus coupa les calculs.

Les lanes se vidèrent.

Le son s’arrêta.

---

Il regarda la grille.

Douze colonnes vides.

---

Il pensa à ce qu’elles pourraient bientôt contenir.

Des dizaines de formules.

Peut-être une centaine.

---

La prochaine question arrivait naturellement.

Si le moteur pouvait gérer les travaux dans le bon ordre…

**comment choisir quelle formule doit recevoir chaque travail ?**

---

Brutus ouvrit un ancien dossier.

Des équations.

Des tests.

Des méthodes.

Des transformations.

Des contre-tests.

Des fonctions accumulées au fil des expériences.

---

Il y en avait déjà beaucoup.

Et chacune avait son domaine.

Ses entrées.

Ses limites.

Ses conditions.

---

Il écrivit :

**FORMULA_ID.**

Puis :

**FORMULA_REGISTRY.**

---

Le prochain problème n’était plus l’ordre du calcul.

C’était le choix du calcul.

---

Il imagina une seule porte.

Derrière elle :

cent formules.

---

Pas cent boutons.

Pas cent applications.

Un registre.

Un sélecteur.

Une entrée.

Et un moteur capable de dire :

**celle-ci est admissible.**

**celle-ci ne l’est pas.**

**celle-ci mérite un contre-test.**

---

Brutus regarda les douze lanes une dernière fois.

---

Avant, la machine devait apprendre à parler dans l’ordre.

Maintenant, elle savait que l’ordre n’était pas unique.

Elle savait distinguer demande, exécution, fin et publication.

Elle savait garder les jobs attachés à leur histoire.

---

Il écrivit dans le registre :

**UN CALCUL PEUT FINIR HORS ORDRE.**

**IL NE DOIT JAMAIS PERDRE SA PLACE.**

---

Puis il ajouta :

**LE BON RÉSULTAT N’EST PAS SEULEMENT UN NOMBRE JUSTE.**

**C’EST UN NOMBRE JUSTE RENDU AU BON PROBLÈME.**

---

Brutus sauvegarda.

Les douze lanes restèrent vides.

Prêtes.

---

Et derrière elles, une nouvelle porte venait déjà d’apparaître.

Une porte assez grande pour contenir cent méthodes.

Cent manières de poser une question.

Cent manières de chercher une réponse.

---

Brutus posa la main sur la poignée.

Le laboratoire savait maintenant faire arriver les calculs dans l’ordre.

Il était temps de décider **lesquels laisser entrer**.
