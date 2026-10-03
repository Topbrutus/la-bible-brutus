# Chapitre 72 — Trente-six voix pour une machine

**Combien de sons faudrait-il pour donner une vraie langue à la machine ?**

Brutus resta devant cette question plus longtemps qu’il ne l’aurait cru.

Quatre sons suffisaient pour dire beaucoup.

PASS.

FAIL.

DOMAIN.

ERROR.

Quatre verdicts.

Quatre états.

Quatre signatures.

Mais un laboratoire ne vivait pas seulement de verdicts.

Il démarrait.

Il arrêtait.

Il attendait.

Il connectait.

Il recevait.

Il rejetait.

Il déplaçait.

Il liait.

Il libérait.

Il créait.

Il vérifiait.

Il archivait.

Il contre-testait.

Il revenait en arrière.

Il produisait des traces.

Et parfois, il ne savait rien du tout.

---

Brutus ouvrit la banque sonore.

Il y avait assez de matière pour aller beaucoup plus loin.

Plus de trente sons.

Des impulsions.

Des cloches sèches.

Des frappes métalliques.

Des sons courts presque numériques.

Des vibrations plus longues.

Des montées.

Des chutes.

Des sons qui ressemblaient à des ouvertures.

D’autres à des fermetures.

---

Il compta.

Puis recompta.

Trente-six.

---

Le nombre lui plut immédiatement.

Pas parce qu’il cherchait une signification cachée.

Parce que trente-six était suffisamment grand pour former un vocabulaire.

Et suffisamment petit pour rester maîtrisable.

---

Il écrivit :

**SFX36.**

Puis :

**36 SONS.**

**36 FONCTIONS MAXIMUM.**

---

Brutus réfléchit.

La pire chose serait d’associer des sons arbitrairement.

Un son à une action aujourd’hui.

Le même son à autre chose demain.

Au bout de quelques semaines, personne ne saurait plus ce qu’il entendait.

Il fallait un dictionnaire.

---

Il créa un manifeste.

**SFX36 MANIFEST.**

---

Chaque entrée contiendrait :

**SOUND_ID**

**SEMANTIC_ROLE**

**CATEGORY**

**PRIORITY**

**DURATION**

**SOURCE_SCOPE**

**REPEAT_POLICY**

**DESCRIPTION**

---

Brutus regarda la structure.

C’était sérieux pour quelques fichiers audio.

Et pourtant, il savait déjà pourquoi c’était nécessaire.

Une machine qui parle sans dictionnaire devient une machine qui fait du bruit.

---

Il écrivit :

**SOUND WITHOUT CONTRACT = NOISE.**

---

Il commença par les quatre sons déjà connus.

SFX01.

PASS.

SFX02.

FAIL.

SFX03.

DOMAIN.

SFX04.

ERROR.

---

Puis il continua.

START.

STOP.

PAUSE.

RESUME.

CONNECT.

DISCONNECT.

ATTACH.

DETACH.

MOVE.

ARRIVAL.

CHECKPOINT.

TRACE.

COUNTERTEST.

REJECT.

ACCEPT.

WAIT.

UNKNOWN.

---

Le vocabulaire grandissait.

---

Brutus compta.

Il n’était encore qu’à dix-huit.

---

Il ajouta des événements liés aux futures structures.

CRYSTAL_CREATED.

CRYSTAL_REJECTED.

FORMULA_RECEIVED.

FORMULA_COMPARE.

FORMULA_PROMOTE_CANDIDATE.

ROUTE_OPEN.

ROUTE_CLOSED.

AUTH_GRANTED.

AUTH_DENIED.

---

Il s’arrêta.

AUTH_GRANTED.

Ce son devait être utilisé avec prudence.

Il ne devait pas ressembler à ARRIVAL.

---

Une autorisation n’était pas un mouvement.

---

Brutus écrivit à côté :

**AUTHORIZED ≠ EXECUTED.**

---

Encore cette vieille règle.

Le vocabulaire sonore ne devait jamais effacer les distinctions conceptuelles.

---

Il choisit donc deux signatures très différentes.

Une autorisation produirait un son bref, presque administratif.

Un mouvement confirmé aurait une signature physique plus distincte.

---

Brutus écouta.

AUTH_GRANTED.

Petit clic montant.

MOVE.

Impulsion plus large.

ARRIVAL.

Son de fermeture courte.

---

Il testa les trois dans l’ordre.

---

Autorisation.

Mouvement.

Arrivée.

---

Même sans regarder, la séquence était compréhensible.

---

Il sourit.

Voilà.

Le son commençait à raconter une causalité.

---

Mais cela créait immédiatement un danger.

La machine pouvait produire une séquence sonore cohérente même si les événements n’avaient pas réellement eu lieu.

Il suffisait qu’un mauvais composant déclenche les fichiers audio directement.

---

Brutus interdit donc l’accès direct aux sons.

---

Aucun module ne pouvait dire :

**PLAY SFX12.**

Il devait produire un événement.

Puis le Speech Bus ou l’Audio Bus décidait si cet événement avait une représentation sonore.

---

Il écrivit :

**EVENT → SEMANTIC ROLE → SOUND**

Jamais :

**MODULE → SOUND FILE.**

---

Cette séparation lui semblait essentielle.

Les sons n’étaient pas des commandes.

Ils étaient des rendus.

---

Brutus ajouta :

**SOUND_ID MUST NEVER BECOME BUSINESS LOGIC.**

---

SFX17 pouvait changer de fichier audio un jour.

Le système devait continuer de fonctionner.

---

Le sens appartenait à l’événement.

Pas au fichier WAV.

---

Brutus regarda les trente-six emplacements.

La machine avait besoin d’une grammaire.

Pas seulement d’un dictionnaire.

---

Il regroupa les sons par familles.

---

**FAMILLE 1 — VERDICTS**

PASS.

FAIL.

DOMAIN.

ERROR.

---

**FAMILLE 2 — CYCLE**

START.

STOP.

PAUSE.

RESUME.

WAIT.

---

**FAMILLE 3 — CONNEXION**

CONNECT.

DISCONNECT.

ROUTE_OPEN.

ROUTE_CLOSED.

---

**FAMILLE 4 — TRANSPORT**

ATTACH.

DETACH.

AUTH_GRANTED.

AUTH_DENIED.

MOVE.

ARRIVAL.

---

**FAMILLE 5 — TRACE**

TRACE.

CHECKPOINT.

COUNTERTEST.

ACCEPT.

REJECT.

UNKNOWN.

---

**FAMILLE 6 — CRISTAL / FORMULE**

CRYSTAL_CREATED.

CRYSTAL_REJECTED.

FORMULA_RECEIVED.

FORMULA_COMPARE.

FORMULA_CANDIDATE.

FORMULA_PROMOTE.

---

Il compta.

Il restait encore quelques positions.

---

Brutus décida de ne pas les remplir immédiatement.

---

Cela lui sembla presque contre-intuitif.

Il avait trente-six emplacements.

Pourquoi ne pas en utiliser trente-six ?

---

Parce qu’un vocabulaire trop rempli trop tôt devient rigide.

---

Il écrivit :

**EMPTY SLOT = FUTURE FREEDOM.**

---

Quelques entrées resteraient réservées.

---

SFX34.

RESERVED.

SFX35.

RESERVED.

SFX36.

RESERVED.

---

Brutus sourit.

Même le silence pouvait être planifié.

---

Il commença ensuite l’apprentissage auditif.

Pas pour la machine.

Pour lui.

---

Il lança SFX01.

PASS.

SFX02.

FAIL.

SFX03.

DOMAIN.

SFX04.

ERROR.

---

Puis plusieurs autres.

---

Au bout d’une heure, il commençait à reconnaître les familles.

Pas chaque son parfaitement.

Mais il savait si un événement concernait un verdict, une route ou un transport.

---

Brutus comprit alors quelque chose.

Le vocabulaire devait être hiérarchique.

L’auditeur ne devait pas avoir besoin de mémoriser trente-six fichiers individuellement.

---

Une famille sonore devait partager une texture.

---

Les verdicts pouvaient être courts et nets.

Les transports plus spatiaux.

Les connexions plus métalliques.

Les traces plus sèches.

Les cristaux plus harmoniques.

---

Il écrivit :

**FIRST HEAR CATEGORY. THEN HEAR EVENT.**

---

Comme dans une langue.

Avant même de comprendre chaque mot, on reconnaît parfois une intonation.

---

Brutus modifia quelques sons.

Pas leur identité.

Leur texture.

---

Puis il testa.

---

CONNECT.

AUTH_GRANTED.

MOVE.

ARRIVAL.

TRACE.

PASS.

---

Une petite histoire.

---

La machine venait de dire, sans phrase :

une route existe,

une autorisation est accordée,

quelque chose bouge,

quelque chose arrive,

une trace est enregistrée,

le test associé passe.

---

Brutus regarda l’écran.

La même séquence existait dans les logs.

---

Il ferma les yeux.

---

Il pouvait l’entendre.

---

Cela le fascina.

---

Puis il fit quelque chose de plus intéressant.

Il injecta un échec.

---

CONNECT.

AUTH_GRANTED.

MOVE.

ERROR.

---

Pas ARRIVAL.

---

Brutus ouvrit immédiatement les yeux.

---

L’absence du son d’arrivée comptait autant que la présence de ERROR.

---

Il nota :

**MISSING EXPECTED SOUND CAN BE A SIGNAL.**

Puis s’arrêta.

Danger.

---

L’absence d’un son pouvait aussi venir d’un problème audio.

Un haut-parleur coupé.

Une file bloquée.

Un fichier manquant.

---

Donc l’opérateur ne devait jamais conclure qu’un événement n’existait pas simplement parce qu’il ne l’avait pas entendu.

---

Il corrigea :

**MISSING SOUND MAY TRIGGER INSPECTION.**

Pas :

**MISSING SOUND PROVES MISSING EVENT.**

---

Brutus sourit.

Le son devait rester un outil d’attention.

Jamais une source unique de vérité.

---

Il testa ensuite plusieurs événements simultanés.

---

Z1 lança un test.

Z2 aussi.

Z3 aussi.

Une fourmi se déplaça.

Une route s’ouvrit.

Un checkpoint fut écrit.

---

Le laboratoire explosa presque acoustiquement.

---

Brutus coupa immédiatement.

---

Trente-six sons existaient.

Cela ne voulait pas dire qu’ils devaient parler tous en même temps.

---

Il écrivit :

**VOCABULARY CAPACITY ≠ PLAYBACK CAPACITY.**

---

Il construisit alors une vraie politique audio.

---

Trois niveaux.

**IMMEDIATE**

**QUEUE**

**SILENT-LOG**

---

Certaines erreurs critiques pouvaient parler immédiatement.

Les événements ordinaires entraient dans la file.

Les événements trop fréquents restaient silencieux mais enregistrés.

---

Brutus hésita sur l’ordre.

Une urgence pouvait-elle interrompre un événement en cours ?

---

Il décida que oui, mais seulement pour une catégorie très restreinte.

---

ERROR critique.

Perte de source autoritaire.

Échec de sécurité.

---

Ces événements pouvaient interrompre un son de faible priorité.

---

Mais l’interruption elle-même devait être tracée.

---

Il écrivit :

**AUDIO INTERRUPT IS ALSO AN EVENT.**

---

Encore un niveau.

---

Le laboratoire devenait presque absurdement rigoureux.

Brutus aimait ça.

---

Il testa.

PASS commence.

Une ERROR critique arrive.

PASS est interrompu.

ERROR joue.

Le journal note :

audio PASS interrupted at offset X.

reason CRITICAL_ERROR.

---

Parfait.

---

Puis il pensa à l’opérateur.

Travailler plusieurs heures avec un laboratoire sonore pouvait devenir fatigant.

Même si les sons étaient utiles.

---

Il ajouta des modes.

---

**SILENT**

Aucun son.

---

**CRITICAL**

Seulement ERROR et événements critiques.

---

**LAB**

FAIL, DOMAIN, ERROR, transports importants.

---

**FULL**

Tout le vocabulaire autorisé.

---

**TRAINING**

Les sons + le nom du rôle affiché à l’écran.

---

Brutus apprécia particulièrement TRAINING.

Il pouvait servir à apprendre la langue SFX36.

---

Son.

Texte.

Événement.

Trace.

---

Après suffisamment de temps, l’opérateur pourrait passer à LAB.

---

Il écrivit :

**A LANGUAGE SHOULD BE LEARNABLE.**

---

Puis une idée lui vint.

Et si chaque écran avait son propre son ?

Il avait déjà exploré le principe :

un écran = un son.

---

Mais il ne voulait pas revenir à cinq autorités audio.

---

Il sépara encore.

La source sonore pouvait rester unique.

La spatialisation pouvait indiquer l’écran concerné.

---

Écran 1 :

position centrale avant.

Écran 2 :

gauche.

Écran 3 :

droite.

Écran 4 :

gauche arrière.

Écran 5 :

droite arrière.

---

Pas besoin de cinq moteurs audio.

Un seul moteur.

Plusieurs positions.

---

Il testa.

---

Un événement sur l’écran 4.

Le son semblait venir de la gauche.

Un autre sur le 5.

Droite.

---

Brutus tourna la tête instinctivement.

---

Excellent.

---

L’espace visuel et l’espace sonore commençaient à correspondre.

---

Il écrivit :

**SCREEN LOCATION MAY INFORM PAN.**

Puis immédiatement :

**PAN ≠ SOURCE AUTHORITY.**

Toujours.

---

Le son pouvait aider à localiser.

Pas décider.

---

Brutus poursuivit avec les trois Z.

---

Z1.

Gauche.

Z2.

Centre.

Z3.

Droite.

---

Mais les Z pouvaient eux-mêmes se déplacer entre les écrans.

Alors quel emplacement utiliser ?

L’identité de la tour ?

Ou la position actuelle de sa fenêtre ?

---

Brutus réfléchit longtemps.

---

Il choisit une règle.

Les verdicts mathématiques seraient spatialisés par **source logique**.

Les événements d’interface par **position visuelle**.

---

Ainsi Z1 garderait sa signature spatiale même si sa fenêtre changeait d’écran.

---

Il écrivit :

**LOGICAL LOCATION ≠ SCREEN LOCATION.**

---

Encore une séparation utile.

---

La machine se construisait presque uniquement avec des différences soigneusement protégées.

---

Brutus commença alors à enregistrer de véritables séquences.

---

Un calcul réussit.

PASS.

---

Une formule rencontre un domaine impossible.

DOMAIN.

---

Une fourmi reçoit un binding.

ATTACH.

---

Une route autorise le mouvement.

AUTH_GRANTED.

---

Mouvement.

MOVE.

---

Arrivée observée.

ARRIVAL.

---

Trace écrite.

TRACE.

---

Brutus écouta.

---

Cela ressemblait déjà à une phrase.

---

Pas à une phrase humaine.

Une phrase machine.

---

Il nota :

**ATTACH — AUTH — MOVE — ARRIVAL — TRACE**

---

Puis :

**FORMULA — COUNTERTEST — PASS**

---

Puis :

**CONNECT — WAIT — ERROR**

---

Les séquences devenaient des motifs grammaticaux.

---

Brutus décida de leur donner un nom.

**AUDIO PHRASES.**

---

Pas des sons préenregistrés.

Des combinaisons d’événements.

---

Il écrivit :

**PHRASE MUST EMERGE FROM EVENTS. NEVER BE FAKED AS A CLIP.**

---

Très important.

Il ne voulait pas enregistrer une jolie séquence « succès de transport » et la jouer en une seule fois.

Parce qu’alors le son pourrait annoncer une histoire qui n’avait jamais réellement eu lieu.

---

Chaque élément de la phrase devait venir d’un événement réel.

---

Brutus testa cette règle.

---

ATTACH arrive.

Le son joue.

---

AUTH_GRANTED.

Son.

---

MOVE.

Son.

---

Mais l’arrivée échoue.

---

Donc aucune ARRIVAL.

---

À la place :

FAIL.

---

La phrase se termine différemment.

---

Parfait.

---

La musique du système devait être une conséquence.

Pas un scénario.

---

Il écrivit :

**THE MACHINE MUST COMPOSE ITSELF FROM REAL EVENTS.**

---

Cette phrase lui plut énormément.

---

Pas parce que la machine devenait artiste.

Parce que la séquence acoustique était construite directement par l’histoire réelle du système.

---

Brutus laissa le laboratoire fonctionner pendant plusieurs minutes.

---

Des sons apparurent.

Puis des silences.

Puis un PASS.

Un mouvement.

Deux traces.

Un DOMAIN.

---

Rien de très musical.

Et pourtant, quelque chose ressemblait déjà à une composition.

---

Le rythme venait de l’activité réelle.

---

Brutus imagina maintenant une grande session.

Dix calculs simultanés.

Douze peut-être.

---

Il entendit mentalement le chaos.

---

Il fallait une stratégie supplémentaire.

---

Les calculs parallèles devaient avoir des canaux.

---

Il créa des **lanes audio**.

Pas trente-six.

Douze au maximum pour le premier système.

---

LANE 1.

LANE 2.

…

LANE 12.

---

Chaque calcul pouvait être associé à une lane.

---

Mais il ne voulait pas douze sons simultanés.

La lane servait surtout au contexte.

---

Les événements de la même expérience partageaient une signature secondaire.

Une légère hauteur.

Une petite position stéréo.

---

Brutus testa trois lanes.

---

Il pouvait déjà distinguer les expériences.

---

Pas parfaitement.

Mais suffisamment.

---

Il écrivit :

**IDENTITY CAN HAVE AN ACOUSTIC SHADOW.**

---

Une ombre acoustique.

Pas une preuve.

Une aide à l’orientation.

---

Brutus passa ensuite à une question plus délicate.

La voix.

---

Les quatre verdicts parlés fonctionnaient.

Mais fallait-il que les trente-six rôles puissent être prononcés ?

---

Il testa.

« Attach. »

« Move. »

« Arrival. »

« Trace. »

---

Très vite, il trouva cela fatigant.

---

Les mots étaient trop lents.

Le son était meilleur pour les événements fréquents.

---

Il construisit donc une séparation.

---

**SFX = FAST SIGNAL**

**VOICE = SELECTED SEMANTIC SUMMARY**

---

La machine ne parlerait pas chaque événement.

---

Elle utiliserait la voix pour quelques moments importants.

---

Checkpoint.

Error.

Decision.

Long-running result.

---

Et peut-être certains verdicts.

---

Brutus écrivit :

**VOICE MUST BE RARER THAN SOUND.**

---

Il testa.

Une série de douze PASS produisit quelques signaux regroupés.

Puis à la fin, la voix annonça :

**« Série terminée. Douze tests. Douze pass. »**

---

Brutus s’arrêta.

C’était utile.

Mais cette phrase introduisait un nouveau problème.

D’où venait le nombre douze ?

---

Il devait venir du registre.

---

Pas du module vocal.

---

Il ajouta :

**SPEECH TEMPLATE + VERIFIED FIELDS.**

---

Le Speech Bus pouvait utiliser des gabarits.

Mais seulement avec des valeurs tirées des événements enregistrés.

---

Pas de génération libre pour les rapports critiques.

---

Brutus écrivit :

**FREE SPEECH FOR STORY.**

**TEMPLATED SPEECH FOR MACHINE FACTS.**

---

Il aimait beaucoup cette séparation.

Un jour, une intelligence pourrait commenter.

Interpréter.

Résumer.

Mais le système de base devait conserver une couche de parole déterministe pour les faits opérationnels.

---

La voix pouvait dire :

**« FAIL, lane 3, tick 8402. »**

Et l’opérateur pouvait retrouver exactement cet événement.

---

Brutus testa.

---

FAIL.

Lane 3.

Tick 8402.

---

Clic.

Trace.

---

Parfait.

---

La voix elle-même commençait à devenir inspectable.

---

Brutus ajouta un champ :

**SPEECH_TEMPLATE_ID.**

Puis :

**SOURCE_EVENT_IDS.**

---

Chaque phrase prononcée pouvait montrer quels événements l’avaient produite.

---

Il sourit.

Même la parole devait avoir une lignée.

---

**THE LINEAGE IS PART OF THE OBJECT.**

La vieille règle revenait.

---

Brutus regarda les trente-six sons.

Ils n’étaient plus simplement une collection audio.

---

Ils formaient une couche du système.

Une interface parallèle.

---

L’écran montrait.

Le son signalait.

La voix résumait.

La trace justifiait.

---

Il écrivit :

**VISUAL → ORIENTATION**

**SFX → ATTENTION**

**VOICE → SUMMARY**

**TRACE → VERIFICATION**

---

Quatre fonctions.

---

Aucune ne devait remplacer l’autre.

---

Brutus se leva.

Il alla un peu plus loin dans la pièce.

Les écrans étaient toujours visibles.

Mais il ne les regardait plus directement.

---

Il lança une expérience.

---

Quelques secondes de silence.

---

CONNECT.

---

Un petit son.

---

Puis un autre.

AUTH_GRANTED.

---

MOVE.

---

ARRIVAL.

---

TRACE.

---

PASS.

---

Brutus n’avait pas vu la fourmi.

Il n’avait pas regardé la route.

Il n’avait pas lu le journal.

Mais il savait à peu près ce qui s’était produit.

---

Il revint à l’écran.

---

La trace confirmait exactement la séquence.

---

Il sourit.

---

La langue fonctionnait.

---

Pas parfaitement.

Pas complètement.

Mais elle fonctionnait.

---

Il imagina le laboratoire plus tard.

Trente-six sons.

Douze lanes.

Trois Z.

Cinq écrans.

Des centaines de formules.

Des agents.

Des cristaux.

Des routes.

---

La pièce pourrait devenir très bruyante.

---

Brutus ajouta une dernière règle.

Peut-être la plus importante de SFX36.

---

**SILENCE IS THE DEFAULT.**

---

Pas de son sans événement.

Pas de musique de fond destinée à donner l’impression d’activité.

Pas de bip régulier pour simuler un cœur.

Pas de faux bruit de calcul.

---

Si rien n’arrivait :

silence.

---

Il coupa toutes les expériences.

---

La pièce se tut.

---

Brutus attendit.

---

Cinq secondes.

Dix.

Vingt.

---

Rien.

---

Il aimait ce silence.

Parce qu’il signifiait quelque chose.

---

Puis un événement réel arriva.

Une formule termina.

---

PASS.

---

Une seule impulsion claire traversa la pièce.

---

Puis le silence revint.

---

Brutus écrivit :

**SILENCE DOES NOT MEAN DEAD.**

**IT MEANS NOTHING WORTH ANNOUNCING HAS JUST HAPPENED.**

---

Il hésita.

Puis corrigea encore.

Une absence de son pouvait aussi résulter d’un filtre ou d’un mode muet.

---

Il ajouta :

**AUDIO STATE MUST BE VISIBLE.**

---

En haut du système :

AUDIO MODE: LAB.

QUEUE: 0.

MUTED: NO.

SOURCE: ONLINE.

---

Parfait.

Même le silence avait maintenant un contexte.

---

Brutus regarda le manifeste.

Trente-trois rôles définis.

Trois emplacements réservés.

---

Il aurait pu remplir les trois derniers avant de finir.

Il résista.

---

Les espaces vides restèrent.

---

Une langue digne de ce nom devait pouvoir grandir.

---

Il sauvegarda :

**SFX36 MANIFEST v1.**

---

Puis il écrivit une phrase à côté.

**36 VOIX.**

Il la relut.

Ce n’était pas tout à fait exact.

Les sons n’étaient pas des voix.

Pas tous.

---

Il pensa au titre.

Puis décida de conserver le mot.

Parce que dans le monde de Brutus, une voix ne serait pas forcément une bouche.

Une voix serait une manière particulière pour la machine de rendre un événement perceptible.

---

Il ajouta :

**UNE VOIX N’EST PAS NÉCESSAIREMENT UNE PAROLE.**

---

Un clic pouvait être une voix.

Une impulsion.

Une vibration.

Un mot.

Un silence contrôlé.

---

La machine disposait maintenant de trente-six emplacements pour s’exprimer.

---

Mais un autre problème approchait déjà.

---

Les sons étaient ordonnés.

Les événements aussi.

Pourtant, lorsque plusieurs calculs arrivaient en même temps, il fallait garantir quelque chose de plus profond.

Pas seulement que les sons arrivent dans l’ordre.

Que **les calculs eux-mêmes** arrivent dans le bon ordre.

---

Brutus regarda l’AUDIO QUEUE.

Puis le journal.

Puis les lanes.

---

Il écrivit :

**INPUT ORDER.**

**EXECUTION ORDER.**

**VERDICT ORDER.**

**AUDIO ORDER.**

---

Quatre ordres.

---

Ils ne seraient pas toujours identiques.

Et s’ils étaient confondus, des erreurs très difficiles à voir pourraient apparaître.

---

Une formule lancée en premier pouvait terminer en dernier.

Un calcul plus rapide pouvait dépasser un autre.

Un verdict pouvait arriver avant celui d’une expérience commencée plus tôt.

---

Le laboratoire savait écouter.

Maintenant, il allait devoir apprendre à **ne pas mélanger les voix**.

---

Brutus sauvegarda le manifeste.

Puis coupa le Speech Bus.

La pièce redevint silencieuse.

---

Sur l’écran, trente-six cases étaient alignées.

Trente-trois portaient un sens.

Trois attendaient encore leur avenir.

---

Brutus regarda la grille.

Puis écrivit :

**UNE MACHINE QUI A TROP DE VOIX PEUT DEVENIR INCOMPRÉHENSIBLE.**

**LA PROCHAINE ÉTAPE SERA DONC DE LUI APPRENDRE À PARLER DANS L’ORDRE.**

Il ferma la banque audio.

Et pendant quelques secondes, le laboratoire entier resta parfaitement silencieux.

Comme s’il attendait son tour de parler.
