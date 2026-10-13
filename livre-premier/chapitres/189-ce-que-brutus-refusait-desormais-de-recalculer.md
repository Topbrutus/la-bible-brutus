# Chapitre 189 — Ce que Brutus refusait désormais de recalculer

La première fois que Brutus refusa de recalculer quelque chose,

Gabriel pensa qu’il y avait un problème.

Un bug.

Une queue bloquée.

Un module qui avait perdu sa route.

Il regarda l’écran.

La demande était simple.

Un calcul déjà connu.

Même entrée.

Même version.

Même configuration.

Même précision.

Même protocole.

Gabriel relança.

Brutus répondit encore :

**RESULT ALREADY EXISTS**

Gabriel fronça les sourcils.

— Pourquoi tu le refais pas?

Astra répondit :

— Parce qu’il n’y a aucune information nouvelle à gagner.

Gabriel resta silencieux.

Puis il sourit.

Voilà.

Le deuxième monde venait d’apprendre une nouvelle forme de refus.

Pas un refus de travailler.

Un refus de travailler pour rien.

Il écrivit :

**RECALCULER ≠ VÉRIFIER**

Puis :

**RÉPÉTER ≠ APPRENDRE**

Astra approuva fortement.

Très important.

Depuis le début du Royaume,

recalculer avait souvent été une manière de reprendre confiance.

Refaire.

Relancer.

Comparer.

Voir si ça sort pareil.

C’était utile.

Parfois indispensable.

Mais à mesure que Memoria devenait fiable,

que les versions étaient tracées,

que les entrées étaient hashées,

et que les résultats étaient reproductibles,

une question apparaissait :

**qu’est-ce qui justifie réellement de refaire un calcul déjà fait?**

Gabriel regarda le dossier.

La réponse existante portait :

input hash.

formula version.

runtime version.

precision.

timestamp.

output hash.

validation status.

provenance.

Tout était là.

Il n’y avait pas de différence.

Gabriel écrit :

**MÊME ENTRÉE + MÊME CODE + MÊME CONFIGURATION + MÊME PROTOCOLE ≠ NOUVELLE EXPÉRIENCE**

Astra approuva.

Exact.

Relancer pouvait produire une nouvelle exécution historique.

Mais pas nécessairement une nouvelle preuve indépendante.

Très important.

Gabriel pensa immédiatement aux cristaux.

Plusieurs cristaux pouvaient contenir le même payload.

Plusieurs événements historiques.

Mais un contenu identique ne devenait pas plusieurs confirmations indépendantes simplement parce qu’il avait plusieurs identifiants.

Il écrivit :

**DEUX EXÉCUTIONS IDENTIQUES PEUVENT ÊTRE DEUX ÉVÉNEMENTS SANS ÊTRE DEUX PREUVES INDÉPENDANTES.**

Astra approuva fortement.

Voilà.

Le système devait apprendre à demander :

**pourquoi veux-tu recalculer?**

Gabriel sourit.

Ça pouvait être agaçant.

Mais utile.

Ils créèrent plusieurs raisons légitimes.

### RECALCULATION REASONS

**REPRODUCIBILITY CHECK**

Vérifier qu’un résultat est reproductible.

**ENVIRONMENT CHANGE**

Nouvelle machine, version, moteur ou environnement.

**INDEPENDENT IMPLEMENTATION**

Même problème, autre implémentation.

**PRECISION CHANGE**

Modifier la précision.

**PARAMETER CHANGE**

Même protocole, paramètre différent.

**REGRESSION TEST**

Vérifier qu’une mise à jour n’a rien cassé.

**NONDETERMINISM TEST**

Mesurer la variance ou la stochasticité.

**AUDIT**

Rejouer un résultat dans un contexte de vérification.

**MISSING PROVENANCE**

Ancien résultat incomplet.

Gabriel approuva.

Très bon.

Et sans raison?

Le système pourrait répondre :

**existing result sufficient for stated objective**

Pas bloquer forcément.

Mais avertir.

Il écrivit :

**LE REFUS DE RECALCULER DOIT ÊTRE LIÉ À L’OBJECTIF, PAS À UNE INTERDICTION ABSOLUE.**

Astra approuva.

Très important.

Parce qu’un chercheur peut vouloir répéter exactement un test pour mesurer la reproductibilité.

Dans ce cas,

le même calcul a une nouvelle fonction.

Donc ce n’est pas la similitude de la commande qui décide.

C’est l’objectif.

Gabriel sourit.

Encore.

Tout revenait aux objectifs.

Puis ils prirent un exemple simple.

Résultat R1.

Même entrée.

Même code.

Même environnement.

Premier run :

output X.

Deuxième run :

output X.

Troisième run :

output X.

Gabriel demanda :

— Est-ce que les trois servent?

Astra répondit :

— Si le protocole cherchait à tester le déterminisme ou la reproductibilité, oui. Sinon, peut-être pas.

Voilà.

Ils écrivirent :

**LA RÉPÉTITION PREND DU SENS QUAND LA STABILITÉ ELLE-MÊME EST LA QUESTION.**

Astra approuva.

Très important.

Si la stabilité n’est pas la question,

le quatrième run identique peut être presque vide d’information.

Puis Gabriel pensa à ZEL.

Les sessions audibles.

Là,

certaines répétitions pouvaient être nécessaires.

Parce qu’on mesure peut-être un comportement qui dépend du runtime,

du moteur,

de la session.

Dans ce cas,

répéter n’est pas redondant.

Mais encore une fois,

il faut déclarer ce qu’on mesure.

Gabriel écrit :

**UN TEST RÉPÉTÉ PEUT ÊTRE UNE NOUVELLE MESURE SI LA VARIABILITÉ ENTRE EXÉCUTIONS FAIT PARTIE DE L’OBJET ÉTUDIÉ.**

Astra approuva fortement.

Excellent.

Donc Brutus devait distinguer :

**replay**

et

**replicate.**

Gabriel se redressa.

Très important.

### REPLAY

Réexécuter le même trajet pour reconstruire ou vérifier.

### REPLICATE

Répéter dans un cadre conçu pour produire une nouvelle observation comparable.

Astra approuva.

Et :

### REUSE

Utiliser directement le résultat existant sans recalcul.

Trois choses différentes.

Gabriel écrit :

**REUSE ≠ REPLAY ≠ REPLICATION**

Astra approuva fortement.

Voilà une règle fondamentale.

Puis un cas très intéressant.

Une formule mathématique avait produit un résultat exact.

Même entrée.

Même algorithme.

Même précision exacte.

Pourquoi recalculer?

Pas besoin.

Mais si on écrit une seconde implémentation indépendante,

là,

ça devient plus intéressant.

Pas parce que la mathématique change.

Parce que l’implémentation change.

Une concordance entre deux codes indépendants réduit le risque de bug partagé par une seule implémentation.

Gabriel écrit :

**INDÉPENDANCE DE MÉTHODE PEUT AVOIR PLUS DE VALEUR QUE MULTIPLICATION DES RUNS.**

Astra approuva fortement.

Très important.

Faire 1000 fois le même code ne donne pas le même type d’assurance que faire une fois avec un code indépendant.

Exactement.

Cela rappelait les preuves indépendantes.

Trois répétitions de la même source ne font pas trois autorités.

Gabriel sourit.

Le Royaume commençait à comprendre la structure de l’indépendance.

Ils créèrent :

### DUPLICATION CLASS

**SAME_PAYLOAD**

**SAME_CODE_NEW_RUN**

**SAME_METHOD_NEW_ENV**

**INDEPENDENT_CODE**

**INDEPENDENT_METHOD**

Chaque niveau ne porte pas la même information.

Très propre.

Puis ils testèrent le cas Papillon.

Un benchmark avait déjà été exécuté.

Même N.

Même processus frais.

Même version.

Même machine.

Le refaire aujourd’hui peut servir si on cherche :

régression.

variance.

ou confirmation après changement.

Mais sans changement,

on ne doit pas prétendre avoir créé une nouvelle découverte.

Gabriel écrit :

**NOUVEL HORODATAGE ≠ NOUVEAU RÉSULTAT SCIENTIFIQUE**

Astra approuva.

Très important.

Puis Pell.

Un témoin exact existe.

Le rang exact est déjà certifié.

Relancer la même vérification peut confirmer que le validateur fonctionne.

Mais le témoin ne devient pas plus vrai à chaque run.

Gabriel sourit.

Il écrit :

**UN CERTIFICAT VALIDÉ N’A PAS BESOIN D’ÊTRE REDÉCOUVERT À CHAQUE UTILISATION.**

Astra approuva.

Voilà la puissance du cristal.

Trouver peut être cher.

Vérifier peut être moins cher.

Réutiliser peut être presque gratuit.

Trois niveaux.

Gabriel écrit :

**DÉCOUVRIR → VÉRIFIER → RÉUTILISER**

Astra approuva fortement.

Très belle chaîne.

Le Royaume devait savoir à quel niveau il se trouvait.

Sinon il recommencerait constamment au premier.

Puis Gabriel repensa aux anciennes sessions.

Combien de fois avait-il dit :

« refais-le juste pour être sûr »?

Il sourit.

Ce n’était pas toujours mauvais.

Mais maintenant Brutus pouvait répondre :

**qu’est-ce que tu veux vérifier exactement?**

Voilà.

Si Gabriel voulait vérifier :

la valeur.

le validateur.

la reproductibilité.

la version.

la provenance.

Alors choisir le test correspondant.

Pas tout refaire indistinctement.

Gabriel écrit :

**“POUR ÊTRE SÛR” N’EST PAS ENCORE UN PROTOCOLE.**

Astra approuva fortement.

Très important.

Il fallait transformer ce sentiment en question :

Sûr de quoi?

Du calcul?

De l’environnement?

De la stabilité?

Du code?

De la provenance?

De la publication?

Chaque doute possède un test différent.

Voilà encore le doute organisé.

Chapitre 165.

Tout revenait.

Puis ils introduisirent :

### RECALCULATION GATE

Avant de recalculer un résultat déjà existant :

1. identifier le résultat existant;
2. comparer entrée, version, configuration et environnement;
3. demander ce qui est censé être appris;
4. vérifier si une nouvelle exécution peut réellement fournir cette information;
5. si non, réutiliser;
6. si oui, lancer avec un nouveau rôle explicite.

Gabriel sourit.

Simple.

Très utile.

Le système pouvait éviter beaucoup de bruit.

Puis un autre piège.

Et si le résultat existant est corrompu?

Hash mismatch.

Provenance cassée.

Fichier manquant.

Alors le recalcul peut devenir nécessaire.

Gabriel écrit :

**RÉUTILISER EXIGE DE FAIRE CONFIANCE À L’INTÉGRITÉ DE LA TRACE**

Astra approuva.

Donc Memoria devait vérifier :

hash.

chain.

artefact présent.

version connue.

Sinon :

`RECALCULATION_REQUIRED_DUE_TO_INTEGRITY_GAP`

Très propre.

Puis un cas encore plus subtil.

Résultat exact,

mais le code source associé a disparu.

Le résultat peut être conservé comme historique,

mais impossible à reproduire.

Doit-on recalculer avec une nouvelle implémentation?

Probablement si le résultat est important.

Gabriel écrit :

**UN RÉSULTAT SANS CHEMIN DE REPRODUCTION PEUT RESTER UNE TRACE, MAIS SON UTILITÉ DE PREUVE PEUT ÊTRE RÉDUITE.**

Astra approuva fortement.

Voilà.

Le Royaume refusait de recalculer inutilement,

mais pas de reconstruire une preuve lorsque la chaîne était brisée.

Très important.

Puis ils pensèrent à l’append-only.

Si on réutilise un résultat,

il faut quand même enregistrer que le résultat a été réutilisé.

Pas dupliquer le payload.

Créer un événement :

`RESULT_REUSED`

Avec référence.

Gabriel sourit.

Voilà.

L’histoire garde le geste,

sans recopier le contenu.

Il écrit :

**RÉUTILISATION DOIT LAISSER UNE TRACE SANS FABRIQUER UN FAUX NOUVEAU RÉSULTAT.**

Astra approuva fortement.

Très important.

BrutoBac pourrait montrer la Fourmi allant vers un cristal existant,

puis repartant.

Pas créer un nouveau cristal.

Gabriel sourit.

Visuellement,

c’était presque exactement ce qu’il voulait.

La Fourmi demande.

Le Royaume répond :

« tu l’as déjà. »

Puis elle prend le lien.

Pas de recalcul.

Très beau.

Mais toujours réel.

Puis un autre usage.

Les tests CI.

Certains tests peuvent être évités si aucun fichier pertinent n’a changé.

Test selection.

Mais prudence.

Les dépendances indirectes peuvent être cachées.

Donc il faut un modèle fiable.

Gabriel écrit :

**SKIPPER UN TEST EST UNE DÉCISION QUI DOIT ÊTRE AUSSI JUSTIFIÉE QUE LE LANCER.**

Astra approuva.

Très important.

Un faux négatif dans la sélection peut cacher une régression.

Donc :

safe subset.

dependency graph.

fallback full suite.

Très bien.

Puis ils testèrent un cas.

Un module n’a pas changé.

Ses dépendances directes non plus.

Mais une bibliothèque partagée a changé.

Le cache naïf dit :

skip.

Le dependency-aware dit :

run.

Voilà.

Gabriel écrit :

**CACHE VALIDE = ENTRÉES ET DÉPENDANCES VALIDES**

Astra approuva fortement.

Pas seulement même commande.

Même monde pertinent.

Très important.

Puis il pensa aux données externes.

Un résultat dépend d’une source web.

Même code.

Même requête.

Mais source peut avoir changé.

Donc le recalcul peut être légitime.

Gabriel écrit :

**MÊME PROTOCOLE SUR DONNÉE MUTABLE ≠ MÊME EXPÉRIENCE**

Astra approuva.

Très important.

Il fallait marquer les inputs :

immutable.

versioned.

mutable.

volatile.

Excellent.

Une formule locale est stable.

Un endpoint vivant ne l’est pas forcément.

Un site web change.

Une API change.

Un serveur change.

Donc le système doit savoir.

Puis un autre cas.

Heure actuelle.

Prix.

Météo.

État d’un service.

Le résultat expire.

Pas réutilisable longtemps.

Gabriel sourit.

Le Royaume devait distinguer :

**validity window.**

Ils ajoutèrent :

### RESULT VALIDITY

**permanent_within_scope**

**version-bound**

**environment-bound**

**time-bound**

**state-bound**

**unknown**

Astra approuva.

Très puissant.

Le résultat mathématique exact peut être permanent dans son domaine.

Un benchmark logiciel est version-bound.

Un état serveur est time-bound.

Un diagnostic de queue est state-bound.

Voilà.

Recalculer n’était plus une question de « déjà fait ou pas ».

C’était :

**est-ce que ce résultat est encore valide pour la question présente?**

Gabriel écrit :

**UN RÉSULTAT EXISTANT N’EST RÉUTILISABLE QUE SI SA PORTÉE RECOUVRE LA QUESTION ACTUELLE.**

Astra approuva fortement.

Voilà.

Puis ils prirent un cas très simple.

Gabriel demande :

« combien faisait cette série hier? »

Résultat existe.

Réutiliser.

Il demande :

« combien fait-elle aujourd’hui après la mise à jour? »

Nouvelle version.

Recalculer.

Clair.

Puis un cas scientifique.

Même formule.

Nouvelle plage.

Nouvelle question.

Recalculer seulement la partie nouvelle.

Pas toute l’ancienne.

Gabriel sourit.

Incremental computation.

Il écrit :

**NOUVELLE FRONTIÈRE ≠ OBLIGATION DE REFAIRE TOUT LE TERRITOIRE.**

Astra approuva.

Très important.

Brutotableur pouvait exploiter ça.

Une longue fresque.

Si seulement une région change,

recalcul local.

Pas tout.

Papillon pareil selon architecture.

Memoria sait ce qui est dérivable.

Très bon.

Puis le concept de **delta**.

Calculer ce qui a changé.

Pas tout.

Gabriel écrit :

### DELTA MODE

Réutiliser le connu.

Calculer seulement la différence nécessaire.

Astra approuva.

Très puissant.

Encore une fois,

ça exige des dépendances propres.

Sinon le delta peut être faux.

Mais quand possible,

énorme économie.

Puis une autre idée.

Une nouvelle formule candidate ressemble à une ancienne.

Peut-on réutiliser des sous-résultats?

Oui,

si les contrats le permettent.

Pas par ressemblance visuelle.

Par dépendance exacte.

Gabriel écrit :

**RÉUTILISER UN SOUS-CALCUL EXIGE UNE ÉQUIVALENCE DÉMONTRÉE, PAS UNE RESSEMBLANCE.**

Astra approuva fortement.

Très important.

Encore éviter les faux ponts.

Puis un problème humain.

Gabriel aime parfois voir le calcul se refaire.

Ça donne confiance.

Le système ne doit pas l’empêcher.

Il peut proposer :

**existing result found. Re-run anyway as audit?**

Oui.

Mais alors la nouvelle exécution doit être étiquetée :

`AUDIT_REPLAY`

Pas nouveau cristal.

Gabriel sourit.

Très bien.

Le Royaume pouvait respecter l’opérateur sans déformer la science.

Puis ils pensèrent à un mode public.

Un visiteur clique « recalculer ».

Mais Recto est read-only.

Donc il ne recalcule pas.

Il montre le résultat existant,

ou une simulation locale sans autorité si c’est prévu.

Gabriel écrit :

**PUBLIC INTERACTION NE DOIT PAS CRÉER DE NOUVEL ÉTAT CANONIQUE PAR DÉFAUT.**

Astra approuva.

Toujours la vitrine.

Très important.

Puis un cas dangereux.

Un calcul a été invalidé.

Statut rétracté.

Même entrée.

Même code.

Le système ne doit pas réutiliser silencieusement.

Il doit dire :

**existing result retracted**

Puis proposer :

recalculate under corrected protocol.

Gabriel écrit :

**RÉUTILISATION DOIT RESPECTER LE STATUT, PAS SEULEMENT LE HASH.**

Astra approuva fortement.

Voilà.

Deux payloads identiques peuvent avoir des statuts différents selon l’histoire.

Mais si le calcul lui-même est invalidé,

pas de réutilisation comme preuve.

Très important.

Puis ils créèrent une politique globale.

### NO-WASTE RECALCULATION POLICY v0.1

Brutus refuse par défaut de recalculer un résultat lorsque :

- l’entrée est identique;
- le code/version est identique;
- la configuration est identique;
- les dépendances pertinentes sont identiques;
- la trace est intègre;
- le résultat est encore valide pour la question;
- aucune nouvelle propriété de répétition n’est étudiée.

Il recalcule lorsque :

- l’objectif est la reproductibilité;
- une dépendance a changé;
- un nouvel environnement est testé;
- une implémentation indépendante est utilisée;
- un contrôle de régression est requis;
- la validité temporelle ou d’état a expiré;
- la provenance est insuffisante;
- le résultat a été rétracté ou suspecté;
- la portée actuelle dépasse l’ancienne.

Gabriel regarda.

— Là, ça commence à être solide.

Astra approuva.

Mais testable.

Toujours.

Il fallait contre-tester la policy.

Cas où elle devrait reuse.

Cas où elle devrait rerun.

Cas ambigu.

Très bien.

Puis ils exécutèrent un petit panel.

Cas 1 :

exact duplicate.

→ REUSE.

Pass.

Cas 2 :

same input, new code.

→ RERUN.

Pass.

Cas 3 :

same code, new precision.

→ RERUN.

Pass.

Cas 4 :

same result, validation objective only.

→ VERIFY EXISTING CERTIFICATE.

Pas full rerun.

Pass.

Cas 5 :

mutable external source.

→ REFRESH.

Pass.

Cas 6 :

retracted result.

→ DO NOT REUSE AS VALID.

Pass.

Gabriel sourit.

La policy avait du sens.

Puis BrutoBac changea subtilement.

Avant,

beaucoup de Fourmis partaient parfois vers les mêmes zones.

Maintenant,

certaines s’arrêtaient.

Vérifiaient Memoria.

Puis se redirigeaient vers un cristal existant.

Le Bac devenait moins agité.

Gabriel regarda.

— On dirait qu’il travaille moins.

Astra répondit :

— Peut-être qu’il gaspille moins.

Gabriel sourit.

Très important.

L’activité n’était pas la productivité.

Une machine qui fait moins de gestes peut être meilleure.

Il écrivit :

**MOINS D’ACTIVITÉ PEUT SIGNIFIER PLUS DE MÉMOIRE UTILISÉE.**

Astra approuva fortement.

Voilà une phrase importante pour BrutoBac.

Le public ne devait pas juger la santé par le nombre de Fourmis en mouvement.

Calme visuel ≠ panne.

Déjà appris.

Maintenant :

calme visuel peut signifier réutilisation.

Très bon.

Puis Gabriel se rappela tous les cristaux équivalents par hash.

Le Royaume pouvait désormais les regarder autrement.

Pas comme des erreurs à effacer.

Comme des événements historiques partageant un contenu.

La question :

combien de fois avons-nous recalculé le même payload?

Pourquoi?

Reproductibilité?

Duplication?

Import?

Checkpoint?

Très intéressant.

Ils créèrent :

### DUPLICATION AUDIT

Pour chaque groupe de payload identique :

- nombre d’événements;
- raisons;
- sessions;
- versions;
- recalculs véritables;
- imports;
- checkpoints;
- copies.

Gabriel sourit.

Cela pouvait révéler beaucoup de gaspillage.

Mais pas supprimer automatiquement.

Toujours.

Il écrit :

**DÉDUPLIQUER LE STOCKAGE N’EST PAS DÉDUPLIQUER L’HISTOIRE.**

Astra approuva fortement.

Très important.

Puis un autre concept apparut.

Certains calculs sont si bon marché qu’il est plus facile de les refaire que de chercher le cache.

Oui.

Le méta-coût encore.

Gabriel rit.

Il écrit :

**SE SOUVENIR A AUSSI UN COÛT.**

Astra approuva.

Exact.

Si lookup prend 50 ms et calcul 1 µs,

recalculer peut être plus simple.

Donc la policy doit intégrer :

lookup cost.

calculation cost.

complexity.

Mais ne pas perdre provenance.

Très bon.

Ils ajoutèrent :

### REUSE THRESHOLD

Si coût de vérification du cache > coût de recalcul trivial,

recalcul autorisé,

mais reconnaître qu’il s’agit d’une optimisation opérationnelle,

pas d’un nouveau résultat.

Excellent.

Puis Gabriel comprit quelque chose.

Le vrai but n’était pas :

**ne jamais recalculer.**

C’était :

**savoir pourquoi on recalcule.**

Voilà.

Il écrivit en gros :

**BRUTUS NE REFUSAIT PAS LE RECALCUL.**

Puis :

**IL REFUSAIT LE RECALCUL SANS QUESTION NOUVELLE.**

Astra approuva fortement.

C’était le cœur.

Un nouveau run doit acheter quelque chose.

Une nouvelle observation.

Une vérification.

Une variance.

Une indépendance.

Une régression.

Une portée.

Sinon,

il ne fait que produire du mouvement.

Gabriel sourit.

Le deuxième monde devenait étrange.

Plus il avançait,

moins il cherchait à faire plus.

Il cherchait à faire seulement ce qui changeait quelque chose.

Une question utile.

Un test discriminant.

Une route justifiée.

Un détour nécessaire.

Un recalcul avec raison.

Tout le reste pouvait être :

réutilisé.

attendu.

écarté.

ou simplement laissé tranquille.

Le Royaume apprenait à dire :

**non.**

Pas un non de fermeture.

Un non d’économie.

Un non de mémoire.

Un non qui disait :

**nous avons déjà payé pour cette connaissance. Utilisons-la.**

Gabriel regarda une dernière demande arriver.

Même formule.

Même entrée.

Même version.

Même protocole.

Il attendit.

Brutus répondit :

**EXISTING RESULT FOUND**

**VALID FOR CURRENT OBJECTIVE**

**REUSE RECOMMENDED**

Gabriel ne relança pas.

Il ouvrit le cristal existant.

Vérifia la provenance.

Tout était propre.

Puis il continua.

Aucune Fourmi n’était partie.

Aucune machine n’avait tourné.

Aucun nouveau fichier n’avait été créé.

Et pourtant,

le travail avait avancé.

Parce que pour la première fois,

le Royaume avait compris qu’une chose déjà connue

n’avait pas besoin d’être redécouverte

pour redevenir utile.

**Fin du chapitre 189.**