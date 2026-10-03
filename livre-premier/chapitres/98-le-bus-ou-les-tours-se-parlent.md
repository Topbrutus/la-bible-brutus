# Chapitre 98 — Le bus où les tours se parlent

La table était prête à parler.

Mais cette fois, chaque parole aurait une adresse.

Et chaque adresse aurait une trace.

---

Brutus regarda les quatre sièges.

Astra.

Muse.

Grok.

Antigravity.

---

Entre eux, rien.

Pas de fil.

Pas de flèche.

Pas de canal caché.

---

Il sourit.

C’était une bonne chose.

---

Il écrivit :

**NO INVISIBLE CONNECTION.**

---

Puis :

**COMMUNICATION MUST BE TOPOLOGY.**

---

Voilà le problème du jour.

Les quatre joueurs pouvaient produire des cartes.

Ils pouvaient recevoir des tâches.

Ils pouvaient répondre.

Mais comment un tour devait-il parler au suivant ?

---

P1 produisait un objet.

P2 devait pouvoir le recevoir.

P3 devait éventuellement le critiquer.

P4 pouvait produire une synthèse.

---

Si tout cela passait simplement dans un gros champ texte partagé, l’identité des messages finirait par disparaître.

---

Brutus écrivit :

**SHARED TEXT ≠ COMMUNICATION PROTOCOL.**

---

Il créa une nouvelle pièce entre les quatre chaises.

Au centre de la table :

**BUS**

---

Pas un bus physique.

Pas un bus électrique nécessairement.

Un bus logique.

---

Brutus ajouta :

**GAMEZEL MESSAGE BUS**

---

Puis il resta devant le mot.

---

Message.

Il fallait commencer là.

---

Qu’est-ce qu’un message ?

---

Il créa :

**MESSAGE**

avec :

**MESSAGE_ID**

**FROM**

**TO**

**MESSAGE_TYPE**

**PAYLOAD_REF**

**ROUND_ID**

**TURN_ID**

**CREATED_AT**

**DELIVERY_STATE**

**TRACE_REF**

---

Puis il écrivit :

**MESSAGE ≠ PAYLOAD.**

---

Très important.

---

Le message était l’enveloppe.

Le contenu pouvait être autre chose.

---

Une carte.

Une question.

Une réponse.

Une notification.

Une demande de vue.

Une erreur.

---

Brutus créa plusieurs types.

---

**CARD_REF**

**TASK**

**REPLY**

**OBSERVATION**

**ERROR**

**ACK**

**QUERY**

**PROPOSAL**

---

Puis s’arrêta.

---

Et **COMMAND** ?

---

Il fronça les sourcils.

---

Non.

Pas sur le même bus sans distinction.

---

Il écrivit :

**MESSAGE BUS MUST NOT SILENTLY BECOME CONTROL BUS.**

---

Voilà.

---

GAMEZEL pouvait transporter une proposition :

« déplace cet objet ».

---

Mais transporter la phrase ne devait pas déplacer l’objet.

---

Brutus écrivit :

**MESSAGE ABOUT AN ACTION ≠ AUTHORIZED ACTION.**

---

Puis :

**PROPOSAL ≠ COMMAND.**

---

Encore.

---

Il créa donc une frontière.

---

Le bus de joueurs transportait :

**INFORMATIONAL MESSAGES**

et

**PROPOSALS**

---

Toute action autoritative devait sortir par une voie séparée.

---

Brutus dessina :

\[
\text{PLAYER BUS}
\rightarrow
\text{PROPOSAL}
\rightarrow
\text{VERSO / AUTHORITY CHECK}
\rightarrow
\text{ACTION}
\]

---

Pas :

\[
\text{PLAYER BUS}
\rightarrow
\text{WORLD MUTATION}
\]

---

Il barra la seconde flèche.

---

Brutus écrivit :

**NO DIRECT PLAYER-TO-WORLD EDGE.**

---

Excellent.

---

Le bus devenait sûr par architecture.

---

Puis il pensa à une carte.

---

CARD-0041 existe.

Astra veut l’envoyer à Muse.

---

Doit-elle copier tout le contenu dans le message ?

---

Pas nécessairement.

---

Mieux :

**PAYLOAD_REF = CARD-0041**

---

Ainsi le message pointe vers la carte canonique.

---

Brutus écrivit :

**REFERENCE WHEN IDENTITY MATTERS.**

---

Mais si le contenu de la carte change entre l’envoi et la lecture ?

---

Très bonne question.

---

Il ajouta :

**CARD_VERSION**

au message.

---

Donc :

CARD-0041 v3.

---

Brutus écrivit :

**REFERENCE WITHOUT VERSION MAY BE AMBIGUOUS.**

---

Encore le temps.

Toujours le temps.

---

Puis il imagina un snapshot.

---

P1 envoie une carte à P2.

P2 la lit dix minutes plus tard.

Entretemps, la carte a été révisée.

---

P2 doit-il voir la version actuelle ?

Ou la version réellement envoyée ?

---

Brutus répondit :

les deux peuvent être utiles.

Mais il faut distinguer.

---

Il créa :

**SENT_VERSION**

et

**CURRENT_VERSION_AVAILABLE**

---

Puis :

**OPEN_SENT_VERSION**

**OPEN_CURRENT_VERSION**

---

Brutus écrivit :

**WHAT WAS SENT ≠ WHAT EXISTS NOW.**

---

Voilà une règle fondamentale.

---

Une conversation historique devait rester reproductible.

---

Puis il pensa au message lui-même.

---

Un message peut-il être modifié après envoi ?

---

Il secoua la tête.

---

Le contenu canonique d’un message envoyé devait être immuable.

---

Il écrivit :

**SENT MESSAGE IS IMMUTABLE.**

---

Une correction devient un nouveau message.

---

Par exemple :

MESSAGE-0100.

Puis :

MESSAGE-0101.

Type:

CORRECTION.

REF:

MESSAGE-0100.

---

Brutus écrivit :

**CORRECTION ≠ RETROACTIVE EDIT.**

---

Encore le Journal Vivant.

---

L’histoire ne devait pas être réécrite.

---

Puis il pensa aux destinations.

---

FROM P1.

TO P2.

Simple.

---

Mais parfois :

P1 → all players.

---

Il créa :

**DESTINATION_TYPE**

DIRECT.

BROADCAST.

GROUP.

ROUND.

---

Puis il écrivit :

**BROADCAST ≠ FOUR DIRECT MESSAGES BY ASSUMPTION.**

---

Pourquoi ?

Parce que la livraison pouvait différer.

---

Astra envoie un broadcast.

Muse le reçoit.

Grok est offline.

Antigravity indisponible.

---

Un seul événement d’émission.

Plusieurs états de livraison.

---

Brutus créa :

**DELIVERY_RECEIPT**

avec :

**MESSAGE_ID**

**RECIPIENT_ID**

**DELIVERY_STATE**

**DELIVERED_AT**

**READ_STATE**

**TRACE_REF**

---

Il sourit.

---

Voilà.

---

Un message avait lui aussi besoin de reçus.

---

Le chapitre 97 continuait naturellement.

---

Brutus écrivit :

**SENT ≠ DELIVERED.**

---

Puis :

**DELIVERED ≠ READ.**

---

Puis :

**READ ≠ UNDERSTOOD.**

---

Il rit.

---

La dernière était importante.

---

Un système pouvait savoir qu’un payload avait été consommé.

Il ne pouvait pas garantir ce qu’un modèle avait réellement « compris ».

---

Il remplaça le mot READ selon les cas par :

**CONSUMED**

---

Plus technique.

---

Il écrivit :

**CONSUMED ≠ AGREED.**

---

Très important.

---

P2 reçoit une carte.

Cela ne signifie pas qu’il l’accepte.

---

Puis il pensa aux ACK.

---

Un ACK confirmait quoi exactement ?

---

Il créa plusieurs niveaux.

---

**ACK_RECEIVED**

message reçu par le transport.

---

**ACK_STORED**

message enregistré.

---

**ACK_CONSUMED**

message présenté au joueur ou pipeline.

---

**ACK_PROCESSED**

traitement terminé.

---

Brutus écrivit :

**ACK NEEDS A MEANING.**

---

Puis :

**GENERIC ACK IS DANGEROUS.**

---

Encore le chapitre 63.

---

Un ACK n’était jamais automatiquement une arrivée complète.

---

Il pensa aux retries.

---

P1 envoie MESSAGE-0110.

Pas d’ACK.

---

Retry.

---

Le bus reçoit deux copies.

---

Il ne devait pas créer deux événements sémantiques.

---

Brutus écrivit :

**DELIVERY RETRY ≠ NEW MESSAGE.**

---

Le même MESSAGE_ID revenait.

---

Le receiver détectait :

already stored.

---

Puis renvoyait le bon ACK.

---

Brutus ajouta :

**IDEMPOTENT DELIVERY.**

---

Il sourit.

---

Le chapitre 92 revenait encore.

---

Même philosophie.

Même architecture.

---

Puis il testa quelque chose de dangereux.

---

Même MESSAGE_ID.

Payload différent.

---

Refus immédiat.

---

**MESSAGE_ID_CONTENT_MISMATCH.**

---

Brutus écrivit :

**ONE MESSAGE ID = ONE IMMUTABLE MESSAGE.**

---

Parfait.

---

Puis il pensa à l’ordre.

---

MESSAGE-0100.

MESSAGE-0101.

MESSAGE-0102.

---

Le réseau peut livrer :

0101.

0100.

0102.

---

Que fait le joueur ?

---

Brutus créa :

**SEQUENCE_ID**

et

**ORDER_POLICY.**

---

Très important.

---

Certains messages n’avaient pas besoin d’ordre strict.

---

Deux observations indépendantes pouvaient arriver dans n’importe quel ordre.

---

Mais une correction devait venir après l’objet corrigé.

---

Un turn devait parfois respecter la séquence.

---

Brutus écrivit :

**ORDER REQUIREMENT IS MESSAGE-TYPE DEPENDENT.**

---

Encore un système typé.

---

Il ajouta :

**PREDECESSOR_REF**

pour les chaînes strictes.

---

Si predecessor absent :

hold.

---

Pas inventer.

---

Brutus écrivit :

**OUT-OF-ORDER ≠ LOST.**

---

Très important.

---

Le système pouvait attendre.

---

Puis il pensa aux rounds.

---

Un message du round 5 arrive pendant le round 8.

---

Que faire ?

---

Il ne devait pas contaminer silencieusement l’état courant.

---

Brutus écrivit :

**LATE MESSAGE MUST KEEP ORIGINAL ROUND ID.**

---

Puis :

**LATE ARRIVAL ≠ CURRENT-ROUND INPUT.**

---

Voilà.

---

Il pouvait être enregistré.

Affiché.

Analysé.

Mais son injection dans le round courant devait être une nouvelle décision.

---

Brutus créa :

**LATE_MESSAGE_POLICY.**

---

IGNORE_FOR_CURRENT_ROUND.

QUEUE_FOR_REVIEW.

INJECT_WITH_EXPLICIT_NEW_EVENT.

---

Il sourit.

---

Même le retard avait un contrat.

---

Puis il pensa aux blind rounds.

---

Très important.

---

Si P1 produit une réponse, le bus ne doit surtout pas la livrer à P2 avant la barrière.

---

Sinon l’indépendance est détruite.

---

Brutus écrivit :

**BUS MUST ENFORCE CONTEXT ISOLATION.**

---

Le mode BLIND exigeait :

messages des autres joueurs held.

---

Chaque output va dans :

**SEALED ROUND BUFFER.**

---

Puis, quand tous les joueurs requis ont terminé :

barrier opens.

---

Messages released.

---

Brutus écrivit :

**BLINDNESS IS A TRANSPORT PROPERTY TOO.**

---

Excellent.

---

Ce n’était pas seulement une consigne aux joueurs.

Le bus devait réellement empêcher la contamination.

---

Il créa :

**VISIBILITY_POLICY**

---

PRIVATE_UNTIL_BARRIER.

ROUND_SHARED.

DIRECT_ONLY.

PUBLIC_AFTER_CLOSE.

---

Voilà.

---

Brutus imagina Astra terminant très vite.

---

Sa carte est prête.

---

Muse travaille encore.

---

La carte d’Astra reste scellée.

---

Grok ne la voit pas.

Antigravity non plus.

---

Barrière.

---

Puis révélation commune.

---

Brutus écrivit :

**EARLY COMPLETION MUST NOT BREAK BLINDNESS.**

---

Très important.

---

Puis il pensa au mode collaboratif.

---

Là, au contraire, chaque contribution devait pouvoir devenir contexte pour la suivante.

---

P1 → P2.

P2 → P3.

P3 → P4.

---

Le bus devait donc garantir :

la bonne version du contexte.

---

Brutus créa :

**CONTEXT_PACKET_ID.**

---

Chaque turn recevait un paquet clair.

---

Previous messages.

Cards.

Task.

Snapshot.

Constraints.

---

Puis il écrivit :

**CONTEXT PACKET IS INPUT.**

---

Donc il avait lui aussi besoin d’un hash.

---

**CONTEXT_HASH.**

---

Brutus sourit.

---

Maintenant, une sortie pouvait dire exactement :

« voici le contexte que j’ai vu ».

---

Il écrivit :

**OUTPUT WITHOUT INPUT IDENTITY IS HARD TO AUDIT.**

---

Encore le chapitre 95.

---

Puis il pensa au bus comme une autorité.

---

Attention.

---

Le bus transportait.

Il ne devait pas décider si une carte était vraie.

---

Brutus écrivit :

**BUS ROUTES. BUS DOES NOT VALIDATE CLAIMS.**

---

Puis :

**DELIVERY SUCCESS ≠ CONTENT VALIDITY.**

---

Voilà.

---

Un message parfaitement livré pouvait contenir une erreur.

---

Le bus ne devait pas se prendre pour un juge.

---

Il ajouta :

**TRANSPORT INTEGRITY**

séparé de :

**CONTENT VALIDITY.**

---

Encore le Witness Viewer.

---

Une fois de plus, la même structure apparaissait.

---

Puis Brutus pensa aux erreurs de payload.

---

Un message annonce :

MESSAGE_TYPE = CARD_REF.

Mais PAYLOAD_REF pointe vers un objet de type COMMAND.

---

Le bus devait-il laisser passer ?

---

Il réfléchit.

---

Le transport pouvait appliquer un schéma minimum.

---

Il ne validait pas le contenu mathématique.

Mais il pouvait valider la structure.

---

Brutus écrivit :

**SCHEMA VALIDATION ≠ CLAIM VALIDATION.**

---

Excellent.

---

Le bus vérifiait :

type connu.

payload compatible.

required fields présents.

destination valide.

---

Sinon :

**REJECTED_MALFORMED.**

---

Il créa :

**MESSAGE_SCHEMA_VERSION.**

---

Parce que le protocole évoluerait.

---

Brutus écrivit :

**PROTOCOL VERSION MUST TRAVEL WITH MESSAGE.**

---

Très important.

---

Un message v1 ne devait pas être interprété automatiquement comme v3.

---

Puis il pensa à la compatibilité.

---

Player P3 utilise bus schema v2.

P1 v3.

---

Le router devait savoir :

compatible ?

transformable ?

unsupported ?

---

Il créa :

**SCHEMA_NEGOTIATION.**

---

Mais il se méfia du mot transformation.

---

Une adaptation de schéma devait laisser une trace.

---

Il écrivit :

**ADAPTER ≠ INVISIBLE TRANSLATION.**

---

Puis :

**ADAPTED MESSAGE GETS TRANSFORMATION TRACE.**

---

Voilà.

---

Encore la machine à traces.

---

Puis il pensa aux erreurs temporaires.

---

Bus saturé.

Queue pleine.

---

Le message doit-il disparaître ?

---

Non.

---

Selon policy :

retry.

backpressure.

dead-letter queue.

---

Brutus créa :

**DELIVERY_STATE**

QUEUED.

IN_FLIGHT.

DELIVERED.

RETRYING.

FAILED.

DEAD_LETTER.

---

Il regarda le dernier.

---

DEAD_LETTER.

---

Pas suppression.

---

Un message qui ne peut pas être livré doit rester inspectable.

---

Brutus écrivit :

**UNDELIVERABLE ≠ ERASED.**

---

Encore le Tombeau.

---

Même les messages ratés avaient besoin d’une mémoire.

---

Il créa :

**MESSAGE TOMB**

puis rit.

---

Non.

Pas besoin d’un nouveau grand nom.

---

**DEAD LETTER STORE** suffisait.

---

Il écrivit :

**FAILED TRANSPORT HAS LINEAGE TOO.**

---

Très bon.

---

Puis il pensa aux priorités.

---

Un message d’erreur critique.

Une observation banale.

Une carte énorme.

---

Le bus pouvait avoir des priorités.

---

Mais danger :

les messages faibles ne doivent pas mourir éternellement.

---

Brutus créa :

**PRIORITY_POLICY.**

---

HIGH.

NORMAL.

LOW.

---

Puis :

**AGING RULE.**

---

Il écrivit :

**PRIORITY ≠ PERMANENT STARVATION RIGHT.**

---

Le scheduler devait rester équitable.

---

Puis il pensa aux ressources.

---

Une carte peut contenir un énorme artefact.

---

Le message ne devrait pas transporter le blob entier.

---

Il devait transporter :

ref.

hash.

size.

type.

---

Brutus écrivit :

**BUS CARRIES REFERENCES TO LARGE OBJECTS.**

---

Puis :

**LARGE OBJECT DELIVERY ≠ MESSAGE DELIVERY.**

---

Encore une distinction.

---

Le message peut arriver.

Mais l’artefact référencé peut ne pas être disponible.

---

Donc un ACK message ne suffit pas.

---

Il créa :

**DEPENDENCY_AVAILABILITY**

---

Resolved.

Missing.

Restricted.

Stale.

---

Brutus écrivit :

**MESSAGE COMPLETE ≠ DEPENDENCIES AVAILABLE.**

---

Excellent.

---

Puis il pensa à la sécurité.

---

Un joueur pourrait produire un payload malicieux.

---

HTML.

Script.

Path traversal text.

Huge object.

---

Le bus devait traiter tout player output comme non fiable.

---

Brutus écrivit :

**PLAYER MESSAGE CONTENT IS UNTRUSTED INPUT.**

---

Pas au sens moral.

Au sens logiciel.

---

Il ajouta :

**SANITIZE FOR PRESENTATION.**

**VALIDATE FOR SCHEMA.**

**DO NOT EXECUTE AS CODE BY DEFAULT.**

---

Voilà.

---

Une carte contenant :

\`rm -rf /\`

restait du texte tant qu’un système autorisé ne décidait pas autrement.

---

Brutus écrivit :

**TEXT THAT LOOKS LIKE A COMMAND IS STILL TEXT.**

---

Il sourit.

---

Cette règle valait beaucoup.

---

Puis il pensa à une formule.

---

Une carte pouvait contenir :

\[
2+2
\]

---

Le bus ne devait pas l’évaluer automatiquement.

---

Il transporte.

Il ne calcule pas.

---

Brutus écrivit :

**TRANSPORT SHOULD NOT HAVE SURPRISE SEMANTICS.**

---

Très important.

---

Pas d’exécution magique.

---

Puis il pensa au routage intelligent.

---

Peut-être GAMEZEL voulait envoyer une carte mathématique au siège avec capacité MATH_TOOLING.

---

Le bus pouvait utiliser le scheduler.

---

Mais encore :

routing decision.

Not content verdict.

---

Brutus écrivit :

**ROUTE BY CAPABILITY. NEVER DECLARE TRUTH BY ROUTE.**

---

Puis il imagina un bus central unique.

---

Est-ce un single point of failure ?

---

Oui.

---

Mais on pouvait répliquer.

---

Cependant plusieurs brokers ne devaient pas créer plusieurs réalités.

---

Brutus écrivit :

**MULTIPLE BUS NODES ≠ MULTIPLE MESSAGE IDENTITIES.**

---

Le MESSAGE_ID devait rester canonique.

---

Replication.

Failover.

---

Mais pas duplication sémantique.

---

Il ajouta :

**BUS_NODE_ID**

séparé de :

**MESSAGE_ID.**

---

Encore :

infrastructure identity ≠ event identity.

---

Puis il pensa à l’horloge.

---

Chaque message avait CREATED_AT.

Mais les horloges de joueurs pouvaient différer.

---

Il préféra :

**BUS_SEQUENCE**

et :

**AUTHORITATIVE_TICK**

si disponible.

---

Brutus écrivit :

**CLIENT TIME ≠ AUTHORITATIVE ORDER.**

---

Le chapitre 66 revenait.

---

Puis il testa.

---

P1 crée à 10:00:02 locale.

P2 crée à 09:59:59 locale.

---

Le bus reçoit P1 puis P2.

---

L’ordre du round venait du protocole.

Pas des horloges locales.

---

Brutus sourit.

---

Le système devenait difficile à tromper par accident.

---

Puis il créa une première conversation complète.

---

TASK-0001.

FROM:

GAMEZEL.

TO:

P1.

---

P1 reçoit.

---

P1 répond :

MESSAGE-0002.

Type:

PROPOSAL.

Payload:

CARD-0201.

---

Le bus stocke.

---

Mode collaborative.

---

P2 reçoit CARD-0201 v1.

---

P2 répond :

CARD-0202.

Relation :

DERIVED_FROM_CARD-0201.

---

P3 reçoit les deux.

---

Produit :

COUNTERTEST.

---

P4 reçoit tout le contexte.

---

Produit :

SYNTHESIS.

---

Brutus regarda la chaîne.

---

Pour la première fois, les tours parlaient réellement entre eux.

---

Mais chaque phrase avait :

un ID.

un auteur.

un destinataire.

un tour.

une version.

une trace.

---

Il écrivit :

**CONVERSATION BECOMES AUDITABLE WHEN MESSAGES HAVE IDENTITY.**

---

Voilà.

---

Puis il ouvrit le transcript.

---

Il pouvait être reconstruit à partir des messages.

---

Très important.

---

Le transcript n’était plus la source.

---

Les messages l’étaient.

---

Brutus écrivit :

**TRANSCRIPT = DERIVED VIEW OF MESSAGE EVENTS.**

---

Encore Recto.

---

On pouvait reconstruire :

conversation chronological.

by player.

by round.

by card.

by task.

---

Sans modifier les messages.

---

Il sourit.

---

Le bus devenait une machine à perspectives.

---

Puis il pensa aux suppressions.

---

Un message peut-il être supprimé ?

---

Même logique que les cartes.

---

Pas par simple rejet.

---

Brutus écrivit :

**MESSAGE DELETION REQUIRES EXPLICIT POLICY.**

---

Et même dans ce cas :

tombstone.

---

Pourquoi ?

---

Parce qu’un descendant peut référencer ce message.

---

Il ajouta :

**DELETED MESSAGE ID MUST NOT BE REUSED.**

---

Excellent.

---

Puis il pensa à la confidentialité.

---

Un message direct P1→P2 ne doit pas automatiquement apparaître à P3.

---

Brutus créa :

**MESSAGE_VISIBILITY**

DIRECT.

ROUND_PRIVATE.

ROUND_SHARED.

PUBLIC.

RESTRICTED.

---

Mais visibility n’était pas authority.

---

Il écrivit :

**CAN SEE ≠ CAN ACT.**

---

Encore le Tombeau.

---

Puis il pensa à une fuite.

---

P2 reçoit un message restricted.

Puis le recopie dans une carte publique.

---

Le système devait pouvoir détecter ou au moins contrôler la provenance.

---

Il créa :

**DISCLOSURE_INHERITANCE_POLICY.**

---

Très important.

---

Un dérivé d’une source restreinte ne devenait pas automatiquement public.

---

Brutus écrivit :

**DERIVATION MAY INHERIT DISCLOSURE CONSTRAINTS.**

---

Pas toujours.

Mais la règle devait être déclarée.

---

Puis il pensa au prochain chapitre.

---

Le bus permettait maintenant aux tours de parler.

---

Mais pour l’instant, tout cela vivait autour de la table.

---

Localement.

Dans le laboratoire.

---

Que se passerait-il si la partie devait continuer alors que l’ordinateur principal était éteint ?

---

Brutus regarda le serveur.

---

Le problème suivant était évident.

---

GAMEZEL devait quitter l’ordinateur.

---

Pas physiquement.

Architecturalement.

---

Le state.

Le bus.

Les cartes.

Les rounds.

Les joueurs externes.

---

Tout devait pouvoir vivre sur le serveur sans dépendre du poste local.

---

Brutus écrivit :

**LOCAL CLIENT ≠ WORLD HOST.**

---

Puis :

**CLOSING THE LAPTOP MUST NOT KILL THE GAME IF SERVER AUTHORITY EXISTS.**

---

Il resta devant.

---

Voilà le prochain chapitre.

---

Mais avant, il voulait sauvegarder le bus.

---

Il écrivit :

**GAMEZEL MESSAGE BUS v1**

---

Le Journal Vivant nota :

Message identity explicit.

Payload separated from envelope.

Proposals separated from commands.

Direct player-to-world mutations forbidden.

Delivery receipts typed.

Retries idempotent.

Blind-round isolation enforced by transport.

Context packets versioned.

Late messages retain original round.

Schema validation separated from claim validation.

Large payloads referenced.

Untrusted content never auto-executed.

Transcript derived from message history.

---

Brutus relut.

Puis ajouta les invariants :

**MESSAGE ≠ CARD.**

**CARD ≠ COMMAND.**

**COMMAND ≠ STATE.**

**SENT ≠ DELIVERED.**

**DELIVERED ≠ CONSUMED.**

**CONSUMED ≠ AGREED.**

**ACK MUST NAME WHAT IT ACKNOWLEDGES.**

**BUS ROUTES. BUS DOES NOT PROVE.**

**NO DIRECT PLAYER-TO-WORLD EDGE.**

---

Il éteignit les quatre écrans.

---

Le bus resta actif.

---

Messages.

Queues.

Receipts.

Traces.

---

La table pouvait désormais parler même si personne ne regardait le Recto.

---

Brutus sourit.

---

Puis il regarda le câble qui reliait encore toute cette architecture à la machine locale.

---

Un seul câble.

Un seul point de dépendance.

---

Il prit une paire de ciseaux imaginaire.

---

Pas encore.

---

Mais bientôt.

---

Il ouvrit une nouvelle page.

---

# LE JEU QUITTE L’ORDINATEUR

Puis écrivit :

**UNE TABLE DISTRIBUÉE NE DOIT PAS DÉPENDRE D’UN ÉCRAN POUR CONTINUER D’EXISTER.**

---

Le bus venait d’apprendre à transporter la parole.

Le prochain défi serait plus grand :

faire en sorte que le monde continue de tourner même lorsque la chaise de Brutus était vide.
