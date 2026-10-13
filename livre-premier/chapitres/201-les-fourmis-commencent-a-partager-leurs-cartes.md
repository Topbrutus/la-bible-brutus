# Chapitre 201 — Les Fourmis commencent à partager leurs cartes

La première carte n’était pas complète.

La deuxième non plus.

Et pourtant,

ensemble,

elles voyaient déjà plus loin.

Gabriel regardait BrutoBac.

Deux Fourmis travaillaient sur des régions différentes.

La première avait exploré une famille de résultats.

La deuxième suivait une série de contre-tests.

Chacune possédait une petite carte locale.

Pas une carte du Royaume entier.

Seulement :

ce qu’elle avait vu.

ce qu’elle avait testé.

ce qu’elle avait abandonné.

ce qu’elle considérait encore ouvert.

Gabriel regarda Astra.

— Elles savent-tu que l’autre a déjà passé là?

Astra répondit :

— Pas toujours.

Gabriel grimaça.

Voilà le problème.

Le Royaume avait commencé à construire des cartes.

Chapitre 190.

Puis des stratégies.

Chapitre 199.

Puis un plan fabriqué à partir des traces.

Chapitre 200.

Mais si chaque Fourmi travaillait avec sa propre portion d’historique,

le Royaume pouvait encore reproduire le même vieux défaut :

plusieurs mémoires,

plusieurs cartes,

et aucun moyen propre de savoir quand elles décrivaient le même territoire.

Il écrivit :

**UNE CARTE LOCALE DEVIENT VRAIMENT UTILE AU ROYAUME LORSQU’ELLE PEUT ÊTRE PARTAGÉE SANS PERDRE SON CONTEXTE.**

Astra approuva fortement.

Voilà le chapitre.

Pas fabriquer une grosse mémoire centrale et forcer tout le monde à tout lire.

Ce serait trop lourd.

Pas faire croire que chaque Fourmi doit connaître tout Brutus.

Ce serait absurde.

Il fallait autre chose.

Partager juste assez.

Gabriel sourit.

Encore.

Toujours la même idée.

Minimum suffisant.

Ils commencèrent par une règle.

### LOCAL MAP

Chaque Fourmi peut posséder une vue locale contenant :

**objective**

**known territory**

**tested routes**

**open unknowns**

**failure patterns**

**validated results**

**dependencies**

**current frontier**

Très propre.

Pas tout Memoria.

Pas tous les cristaux.

Seulement ce qui sert à son travail.

Puis une Fourmi devait pouvoir dire :

**voici ma carte.**

Mais qu’est-ce qu’une carte partageable?

Pas une capture d’écran.

Pas une impression subjective.

Un objet structuré.

Gabriel écrivit :

### MAP PACKET

**map_id**

**owner_task**

**scope**

**version**

**known_nodes**

**known_edges**

**unknown_nodes**

**confidence_by_entry**

**source_refs**

**last_updated**

**reuse_rules**

Astra approuva.

Très important.

Une autre Fourmi pouvait alors recevoir la carte

et savoir :

ce qui est certain.

ce qui est seulement observé.

ce qui est hypothétique.

ce qui est vieux.

ce qui dépend d’une version.

Voilà.

Gabriel écrivit :

**PARTAGER UNE CARTE ≠ PARTAGER UNE CONCLUSION.**

Astra approuva fortement.

Très important.

Une Fourmi peut montrer :

« dans ma mission, j’ai observé ceci ».

L’autre ne doit pas transformer automatiquement cette observation en preuve pour son propre problème.

Le scope suit la carte.

Toujours.

Puis ils testèrent.

Fourmi A travaille sur une frontière F.

Fourmi B travaille sur une sous-population S.

A trouve :

la frontière semble disparaître quand une représentation change.

B trouve :

S est surreprésentée précisément dans la zone où F apparaissait.

Deux cartes.

Deux observations.

Séparées,

aucune ne répond.

Partagées,

elles produisent une nouvelle question :

**la dépendance de représentation observée par A varie-t-elle selon la sous-population décrite par B?**

Gabriel se redressa.

— Là, ça devient bon.

Voilà.

Partager ne produisait pas une conclusion.

Cela produisait un croisement testable.

Il écrivit :

**DEUX CARTES PEUVENT PRODUIRE UNE QUESTION QU’AUCUNE N’AURAIT PU FORMULER SEULE.**

Astra approuva fortement.

Très important.

Ils créèrent :

### CROSS-MAP QUESTION

Source map A.

Source map B.

Shared region.

Potential relation.

Status:

**CANDIDATE QUESTION**

Pas claim.

Pas proof.

Très propre.

Puis la question :

comment détecter que deux cartes se recouvrent?

Par mots?

Insuffisant.

Par identifiants?

Parfois.

Par scope.

Par objets.

Par ranges.

Par module.

Par formule.

Par population.

Par relation.

Gabriel sourit.

Le Royaume avait besoin d’un vocabulaire commun.

Pas nécessairement un langage universel.

Mais des clés stables.

Il écrivit :

**LE PARTAGE EXIGE DES COORDONNÉES COMMUNES.**

Astra approuva fortement.

Voilà.

Une Fourmi dit :

`FORMULA_ID X`

Une autre :

`FORMULA_ID X`

Le système sait qu’elles parlent du même objet.

Si une dit :

« le motif bleu dans le coin gauche »

et l’autre :

« la série bizarre »

impossible.

Donc :

IDs.

Scopes.

Versions.

Très important.

Ils créèrent :

### MAP COORDINATES

**object_id**

**domain**

**version**

**representation**

**protocol**

**time/state if relevant**

Gabriel approuva.

Très propre.

Puis un piège.

Même `object_id`,

mais version différente.

Les cartes ne sont pas directement fusionnables.

Elles peuvent être comparées.

Pas fusionnées sans condition.

Il écrit :

**MÊME OBJET ≠ MÊME TERRITOIRE SI LA VERSION OU LE PROTOCOLE CHANGE.**

Astra approuva fortement.

Très important.

Le système devait distinguer :

### MAP RELATIONS

**OVERLAPS**

**CONTAINS**

**DISJOINT**

**COMPARABLE**

**CONFLICTS**

**SUPERSEDES**

**UNKNOWN_RELATION**

Gabriel sourit.

Voilà.

Deux cartes pouvaient se chevaucher sans être identiques.

Une pouvait en contenir une autre.

Une plus récente pouvait supersede une partie.

Très propre.

Puis un cas.

Fourmi A :

scan 1–1000, version v1.

Fourmi B :

scan 500–1500, version v1.

Overlap :

500–1000.

Facile.

Mais si B est version v2?

Relation :

COMPARABLE,

pas mergeable by default.

Très important.

Ils écrivirent :

**UNE SUPERPOSITION GÉOMÉTRIQUE NE SUFFIT PAS POUR UNE SUPERPOSITION SÉMANTIQUE.**

Astra approuva fortement.

Gabriel sourit.

La carte devenait sérieuse.

Puis la question du transfert.

Faut-il envoyer toute la carte de A à B?

Pas forcément.

Si B n’a besoin que de la région 500–700,

envoyer local neighborhood.

Gabriel écrivit :

**PARTAGER TOUT EST PARFOIS UNE AUTRE FORME DE GASPILLAGE.**

Astra approuva.

Très important.

Ils créèrent :

### MAP QUERY

B demande :

object X.

scope Y.

need:

failure patterns + validated coverage + unresolved conflicts.

A répond :

packet minimal.

Voilà.

Pas besoin de copier l’univers.

Puis un autre avantage.

Privacy / permissions internes.

Une Fourmi peut ne pas avoir droit à toutes les données.

Donc le partage doit respecter les capacités.

Gabriel écrivit :

**UNE CARTE PARTAGÉE DOIT RESPECTER LES MÊMES LIMITES D’AUTORITÉ QUE LE TRAVAIL QU’ELLE DÉCRIT.**

Astra approuva fortement.

Très important.

Une Fourmi publique ne reçoit pas Verso complet.

Une Fourmi de validation n’a pas besoin des secrets de déploiement.

Une Fourmi cartographe peut lire beaucoup,

mais pas modifier les preuves.

Toujours least privilege.

Puis ils testèrent le premier vrai échange.

### MAP-201-A

Source:

Research Ant.

Scope:

V5 boundary.

Known:

V5 associated with narrowed transition.

Unknown:

mechanism.

Failure pattern:

chunk dependence previously ruled out.

### MAP-201-B

Source:

Validation Ant.

Scope:

same V5 region.

Known:

independent implementation reproduces boundary.

Unknown:

external generalization.

Gabriel regarda.

Les deux cartes se recouvraient.

A savait :

origine de l’hypothèse.

B savait :

robustesse d’implémentation.

Ensemble :

le prochain test pouvait directement viser generalization,

sans refaire chunking

ni second implementation.

Voilà.

Le partage venait d’éviter deux répétitions.

Cette fois,

réellement.

Gabriel écrivit :

**UNE CARTE PARTAGÉE PEUT ÉVITER NON SEULEMENT UN RECALCUL, MAIS UNE RECONSTRUCTION DE CONTEXTE.**

Astra approuva fortement.

Très important.

C’était peut-être encore plus précieux.

Parce que reconstruire le contexte humain coûte beaucoup.

Lire.

Comprendre.

Retrouver.

Comparer.

Le Map Packet pouvait réduire ça.

Puis ils créèrent :

### HANDOFF MAP

Quand une tâche change de Fourmi ou de queue,

transmettre :

- état du territoire;
- travaux faits;
- échecs;
- revendications;
- inconnus;
- prochaine frontière;
- raisons des choix précédents.

Gabriel sourit.

Voilà le passage de relais parfait.

Chapitre 192.

Queues.

Maintenant,

chaque handoff pouvait transporter une carte.

Il écrit :

**UN BON PASSAGE DE RELAIS TRANSMET LA POSITION, PAS SEULEMENT LE BAGAGE.**

Astra approuva fortement.

Belle phrase.

Puis un problème.

Que faire quand les cartes se contredisent?

Fourmi A dit :

boundary stable.

Fourmi B dit :

boundary moves.

Impossible de fusionner silencieusement.

Créer :

**MAP CONFLICT**

Puis comparer :

version?

population?

precision?

protocol?

representation?

time?

Voilà.

Gabriel écrivit :

**UNE CONTRADICTION ENTRE CARTES EST UNE QUESTION DE RECHERCHE AVANT D’ÊTRE UNE ERREUR DE DONNÉES.**

Astra approuva fortement.

Très important.

Parfois,

une carte est fausse.

Mais parfois,

elles sont toutes les deux vraies dans des scopes différents.

Le conflit révèle une variable cachée.

Excellent.

Ils testèrent.

A :

boundary at B under precision P1.

B :

boundary at B+δ under P2.

Conflit apparent.

Après comparaison :

precision differs.

Donc pas contradiction.

Relation :

**CONTEXTUAL_VARIATION**

Gabriel sourit.

Voilà.

La carte partagée avait révélé que la précision était pertinente.

Une nouvelle information.

Puis un vrai conflit.

Même version.

Même precision.

Même inputs.

Outputs différents.

Là :

possible nondeterminism.

possible corruption.

possible environment difference non capturée.

Escalade.

Très important.

Gabriel écrivit :

**PLUS DE CARTES PEUT AUGMENTER LES CONFLITS VISIBLES. C’EST UNE AMÉLIORATION SI CES CONFLITS ÉTAIENT DÉJÀ RÉELS.**

Astra approuva fortement.

Magnifique.

Le système ne devenait pas plus incohérent.

Il voyait davantage son incohérence existante.

Très important.

Puis le problème de la fraîcheur.

Une Fourmi garde une carte vieille.

Pendant ce temps,

le terrain change.

Policy.

Version.

Résultat rétracté.

Donc chaque carte doit avoir :

**last_updated**

**validity dependencies**

et peut être :

**STALE**

Gabriel écrit :

**UNE CARTE OBSOLÈTE PEUT ÊTRE PLUS DANGEREUSE QU’UNE ABSENCE DE CARTE.**

Astra approuva fortement.

Très important.

Parce qu’elle donne confiance.

Ils créèrent :

### MAP FRESHNESS

**CURRENT**

**STALE_BY_VERSION**

**STALE_BY_POLICY**

**STALE_BY_DATA**

**UNKNOWN**

Très propre.

Une Fourmi recevant une carte stale peut l’utiliser comme historique,

pas comme autorité active.

Excellent.

Puis un problème plus subtil.

Supposons une carte construite sur une hypothèse ensuite réfutée.

Doit-on la jeter?

Non.

Elle conserve l’histoire.

Mais ses routes peuvent être marquées invalidées.

Gabriel écrit :

**UNE CARTE PEUT RESTER VRAIE COMME HISTOIRE MÊME SI CERTAINS CHEMINS NE SONT PLUS VALIDES COMME CONSEILS.**

Astra approuva fortement.

Toujours append-only.

Très important.

Puis ils abordèrent la fusion.

Est-ce qu’on veut une carte globale?

Oui,

mais comme index dérivé.

Pas comme objet que chaque Fourmi modifie directement.

Trop dangereux.

Gabriel sourit.

Ils créèrent :

### SHARED ATLAS

Une projection globale de cartes locales.

Rebuildable.

Read-optimized.

Not canonical history.

Source:

local map events + Memoria.

Voilà.

Il écrivit :

**L’ATLAS PEUT ÊTRE RECONSTRUIT. LES TRACES QUI LE NOURRISSENT DOIVENT RESTER LA SOURCE.**

Astra approuva fortement.

Exactement la règle du chapitre 190.

La carte globale ne devait pas devenir un point unique de vérité fragile.

Puis ils demandèrent :

comment éviter que deux Fourmis modifient le même secteur en même temps?

Pas forcément un problème.

On peut avoir plusieurs observations.

Mais si elles écrivent un statut canonique,

il faut contrôle.

Ils séparèrent :

**map observations**

appendable.

**canonical status**

guarded.

Très important.

Gabriel écrivit :

**PLUSIEURS FOURMIS PEUVENT CARTOGRAPHIER LA MÊME ZONE. ELLES NE DOIVENT PAS TOUTES POUVOIR EN CHANGER LE STATUT CANONIQUE.**

Astra approuva fortement.

Voilà.

Exploration distribuée.

Autorité centralement gouvernée.

Pas nécessairement centralisée techniquement,

mais contractuellement.

Très important.

Puis un autre cas.

Deux Fourmis travaillent en parallèle.

A découvre un contre-exemple.

B continue une campagne qui dépend de l’hypothèse maintenant cassée.

Si A partage seulement à la fin,

B gaspille.

Il faut donc certains événements de carte en temps réel ou quasi temps réel.

Gabriel écrivit :

**CERTAINES MISES À JOUR DE CARTE DOIVENT ÊTRE PUBLIÉES AVANT LA FIN DE LA MISSION.**

Astra approuva fortement.

Très important.

Mais pas chaque micro-observation.

Sinon bruit.

Donc :

### MAP UPDATE PRIORITY

Publish immediately if:

- hypothesis invalidated;
- safety/policy condition changed;
- canonical dependency changed;
- high-cost route now obsolete;
- major conflict detected.

Batch later if:

- local notes;
- minor coverage increments;
- low-impact observations.

Gabriel sourit.

Très bon.

Le partage avait besoin de priorités.

Puis ils simulèrent.

Fourmi A casse H1.

Map event :

`H1_REJECTED_WITHIN_SCOPE`.

Atlas met à jour.

Fourmi B a une route active dont `depends_on H1`.

Antmux détecte.

Pause B.

Pas kill.

Re-evaluate.

Gabriel regarda.

Voilà.

Le partage de carte venait de modifier le travail d’une autre Fourmi en cours.

Il écrit :

**PARTAGER UNE CARTE DEVIENT OPÉRATIONNEL QUAND UNE NOUVELLE TRACE PEUT CHANGER UNE ROUTE QUI N’EST PAS LA SIENNE.**

Astra approuva fortement.

Très important.

Mais attention.

Une observation locale ne doit pas stopper une autre mission si scope différent.

Donc dependency match.

Très important.

Ils créèrent :

### CROSS-TASK INVALIDATION

Trigger only if:

source result scope covers target dependency.

Gabriel approuva.

Très propre.

Sinon avertissement seulement.

Puis un cas extraordinaire.

Fourmi A trouve une anomalie.

Fourmi B possède déjà un vieux failure pattern qui l’explique potentiellement.

Grâce au partage,

A reçoit immédiatement :

**relevant prior map fragment found**

Elle ne sait pas encore si c’est la cause.

Mais elle peut tester.

Voilà.

L’historique n’était plus seulement central.

Les Fourmis pouvaient se nourrir mutuellement de cartes.

Gabriel sourit.

— Là, on commence vraiment à avoir une colonie.

Astra approuva.

Mais techniquement,

il fallait rester précis.

Pas « elles pensent ensemble ».

Pas nécessaire.

Elles échangeaient des objets structurés,

et le routeur réévaluait les tâches.

Cela suffisait.

Gabriel écrivit :

**COORDINATION ≠ CONSCIENCE COLLECTIVE.**

Astra approuva fortement.

Très important.

Le Royaume pouvait être fascinant sans inventer ce qui n’était pas démontré.

Puis ils définissent les types d’échanges.

### MAP SHARE TYPES

**PULL**

Une Fourmi demande un fragment.

**PUSH**

Une mise à jour importante est envoyée.

**HANDOFF**

Carte transmise avec une tâche.

**BROADCAST**

Événement global exceptionnel.

Gabriel approuva.

Très propre.

Broadcast devait être rare.

Exemple :

policy change.

critical failure pattern.

canonical status retraction.

Pas :

chaque nouveau résultat.

Sinon tempête.

Il écrit :

**TOUT CE QUI EST PARTAGEABLE NE MÉRITE PAS D’ÊTRE DIFFUSÉ À TOUT LE MONDE.**

Astra approuva fortement.

Toujours minimum suffisant.

Puis un autre problème.

Spam cartographique.

Une Fourmi produit 10 000 petits updates.

Atlas étouffe.

Donc aggregation.

Chunking.

Mais attention à ne pas réintroduire les artefacts du chapitre 191.

Gabriel rit.

Encore.

Ils créèrent :

**MAP BATCH**

avec interval.

summary.

exception list.

Mais les événements critiques sortent immédiatement.

Très bon.

Puis compression.

Les régions couvertes peuvent être représentées comme ranges.

Pas cellule par cellule.

Chapitre 190.

Encore.

Tout se raccordait.

Gabriel écrivit :

**LES FOURMIS PARTAGENT DES FORMES DE TERRITOIRE, PAS NÉCESSAIREMENT TOUTES LEURS EMPREINTES.**

Astra approuva fortement.

Belle phrase.

Puis un autre risque.

La carte globale peut devenir tellement dense qu’elle est impossible à lire.

Donc progressive disclosure.

Par défaut :

territoire local.

Puis voisins.

Puis global sur demande.

Gabriel sourit.

BrutoBac.

Exactement.

Il écrit :

**UNE BONNE CARTE COMMUNE DOIT POUVOIR ÊTRE GRANDE SANS ÊTRE OBLIGÉE D’ÊTRE TOUTE VISIBLE EN MÊME TEMPS.**

Astra approuva fortement.

Très important.

BrutoBac afficherait :

Fourmi active.

route locale.

overlap relevant.

Pas toutes les traces du Royaume.

Clique pour ouvrir l’atlas.

Très propre.

Puis un test pratique.

Trois Fourmis.

### ANT-A

cherche une frontière.

### ANT-B

valide une sous-population.

### ANT-C

audite un ancien bug.

Sans partage :

A propose 8 tests.

B propose 5.

C propose 4.

Total 17 actions candidates.

Avec partage :

A voit que C a déjà invalidé deux représentations.

B voit que A a déjà couvert une plage.

C voit que B a un résultat indépendant qui rend un vieux test inutile.

Nouvelle planification :

11 actions candidates.

Gabriel regarda.

— On en a six de moins.

Cette fois,

comptage exact des actions planifiées supprimées.

Pas garantie de temps économisé.

Mais réduction réelle de travail proposé.

Très bon.

Ils enregistrèrent :

### MAP SHARING TRIAL 201-A

Without shared map:

17 candidate actions.

With shared map:

11 candidate actions after overlap/reuse filtering.

Difference:

6 candidate actions removed or replaced.

Not established:

exact runtime savings.

Not established:

universal efficiency gain.

Gabriel sourit.

Parfait.

Toujours précis.

Puis question qualité.

Les six actions supprimées étaient-elles vraiment inutiles?

Ils vérifièrent.

Quatre duplicats exacts ou équivalents.

Un contrôle déjà satisfait.

Une action devenue hors scope.

Très bon.

Aucune suppression injustifiée dans ce petit panel.

Status :

**PROMISING**

Pas davantage.

Gabriel écrivit :

**LE PARTAGE DOIT ÊTRE ÉVALUÉ SUR CE QU’IL ÉVITE ET SUR CE QU’IL RISQUE D’EMPÊCHER À TORT.**

Astra approuva fortement.

Très important.

Un système de coordination peut devenir trop agressif.

Une Fourmi dit :

« déjà fait ».

Mais le contexte diffère.

Et empêche un test nécessaire.

Danger.

Donc every reuse check must inspect scope.

Encore.

Puis ils testèrent un faux duplicate.

Même formule.

Même input.

Mais nouvelle version.

Atlas propose reuse?

Il ne devait pas.

Résultat :

**COMPARABLE_ONLY**

Pass.

Très bon.

Puis autre :

même version.

même input.

même protocol.

exact output exists.

`REUSE`.

Pass.

Excellent.

Le partage devenait fiable.

Puis Gabriel posa une question.

— Est-ce que les Fourmis devraient apprendre directement des cartes des autres?

Astra répondit :

— Elles peuvent utiliser les traces des autres comme contexte, heuristique ou preuve selon le statut, mais le changement de policy doit rester séparé.

Très important.

Donc une Fourmi peut modifier sa route.

Pas réécrire la stratégie globale immédiatement.

Il écrit :

**PARTAGER UNE EXPÉRIENCE N’EST PAS MODIFIER AUTOMATIQUEMENT LA POLITIQUE DE TOUT LE ROYAUME.**

Astra approuva fortement.

Exact.

Sinon une seule mauvaise observation pourrait contaminer tout.

Très dangereux.

Policy updates passent par evaluation.

Toujours.

Puis un autre cas.

Une Fourmi travaille sur Pell.

Une autre sur ZEL.

Elles voient toutes les deux q=47.

Faut-il partager automatiquement?

Non.

Même nombre ne signifie pas même mécanisme.

Gabriel sourit.

Évidemment.

Il écrit :

**UNE COORDONNÉE COMMUNE NE SUFFIT PAS À CRÉER UNE RELATION SCIENTIFIQUE COMMUNE.**

Astra approuva fortement.

Très important.

Le partage peut dire :

same literal value appears.

Pas :

related phenomenon.

Si exploration cross-domain souhaitée,

créer question candidate.

Pas claim.

Excellent.

Puis une Fourmi Papillon trouve un comportement d’agrégation.

Une Fourmi Pell travaille sur un rang exact.

Peut partager telemetry structure?

Oui,

si rôle explicitement :

representation / monitoring.

Pas proof.

Gabriel approuva.

Le rôle de la carte importait autant que son contenu.

Toujours.

Puis ils ajoutèrent à chaque entry :

**usable_as**

evidence.

counterexample.

test template.

routing heuristic.

context.

representation only.

Voilà.

Chapitre 185 revenait.

Gabriel sourit.

Tout le système commençait à parler le même langage.

Puis un incident.

Une Fourmi B utilisait une carte de A comme preuve,

alors que A l’avait marquée `routing heuristic`.

Erreur.

Le système devait bloquer.

Ils ajoutèrent :

### MAP ROLE GUARD

Consumer cannot elevate source role without independent validation.

Gabriel écrivit :

**UNE TRACE NE DOIT PAS GAGNER DE L’AUTORITÉ SIMPLEMENT PARCE QU’ELLE A VOYAGÉ.**

Astra approuva fortement.

Magnifique.

Très important.

Le partage augmente la portée.

Il ne doit pas augmenter automatiquement l’autorité.

Voilà.

Puis un autre danger.

Telephone game.

A produit observation.

B résume.

C utilise le résumé.

D résume encore.

Au bout de quatre transferts,

la nuance disparaît.

Donc Map Packet doit pointer vers source originale.

Gabriel écrit :

**UNE CARTE PARTAGÉE DOIT RACCOURCIR L’ACCÈS À LA SOURCE, PAS LA REMPLACER.**

Astra approuva fortement.

Très important.

Chaque entry :

source_ref.

provenance_hash.

Voilà.

Pas de chaîne de paraphrases sans origine.

Puis ils firent un test.

A → B → C.

C clique source.

Retour à event original.

Pass.

Très bon.

Puis la question de fusion.

Quand plusieurs cartes disent la même chose,

l’atlas peut consolider.

Mais ne pas perdre les sources.

Il écrit :

**CONSOLIDER LA VUE ≠ CONSOLIDER LES PREUVES EN UNE SEULE ORIGINE.**

Astra approuva fortement.

Encore.

Très important.

Deux observations indépendantes peuvent rester deux.

Deux copies du même payload ne deviennent pas indépendantes.

L’atlas doit savoir.

Ils ajoutèrent :

**independence_class**

Excellent.

Puis Gabriel pensa aux 144 accumulateurs du Papillon.

Un réseau fixe pouvait agréger sans matérialiser chaque entité.

Peut-être l’atlas pouvait aussi avoir des résumés structurels.

Mais attention à ne pas prétendre que Papillon est nécessaire.

C’était seulement une inspiration.

Il écrit :

**L’AGRÉGATION PEUT AIDER À VOIR UNE GRANDE CARTE SANS MATÉRIALISER CHAQUE TRACE DANS LA VUE ACTIVE.**

Astra approuva.

Très propre.

Pas de claim universel.

Puis ils observèrent BrutoBac.

Trois Fourmis.

Avant :

trois mondes.

Maintenant :

leurs cartes se chevauchaient.

Une route déjà couverte s’éclairait.

Une erreur ancienne apparaissait comme avertissement.

Une frontière commune produisait une question.

Le Bac semblait soudain plus cohérent.

Pas parce que les Fourmis « parlaient » comme des personnes.

Parce que leurs traces devenaient interopérables.

Gabriel sourit.

Il écrit :

**UNE COLONIE COMMENCE À EXISTER TECHNIQUEMENT QUAND LE TRAVAIL D’UNE FOURMI PEUT MODIFIER UTILEMENT LE PROCHAIN TRAVAIL D’UNE AUTRE.**

Astra approuva fortement.

Voilà.

Pas besoin de mystique.

C’était déjà immense.

Puis un autre détail.

Que faire si la Fourmi qui a produit la carte disparaît?

Rien.

La carte appartient à Memoria.

Pas à la session.

Très important.

Il écrit :

**LA CARTE DOIT SURVIVRE À CELLE QUI L’A DESSINÉE.**

Astra approuva fortement.

Cela rendait le système robuste aux crashes.

Sessions.

Agents.

Reconnect.

Excellent.

Puis ils testèrent reprise.

Ant-A termine brutalement.

Nouvelle Ant-A2 reçoit Map Packet.

Elle reprend à frontier.

Pas au début.

Très bon.

Gabriel sourit.

Voilà encore la vraie mémoire.

Pas se souvenir du texte.

Se souvenir de la position.

Il écrit :

**REPRENDRE UNE MISSION, C’EST RETROUVER LA FRONTIÈRE, PAS REJOUER TOUT LE CHEMIN.**

Astra approuva fortement.

Magnifique.

Puis un autre cas.

Deux Fourmis reprennent simultanément la même carte après crash.

Double travail.

Il faut claim/lease.

Gabriel sourit.

Nouvelle complexité.

Ils créèrent :

### TASK LEASE

Map says work frontier F.

One worker claims next segment.

Lease expires.

Another can recover.

Très propre.

Mais la carte elle-même reste partagée.

Le lease concerne l’action.

Pas la connaissance.

Il écrit :

**PARTAGER LA CARTE NE SIGNIFIE PAS PARTAGER LE MÊME MARTEAU EN MÊME TEMPS.**

Astra approuva fortement.

Gabriel rit.

Ça resta.

Puis ils abordèrent la concurrence.

A et B écrivent deux observations simultanées.

Append-only.

Pas de problème.

Mais index atlas doit gérer ordre.

Timestamp.

Lamport-like ordering peut-être.

Pas besoin de trop de théorie ici.

Ils décidèrent :

event IDs.

parent refs.

merge deterministic.

Très important.

Gabriel écrivit :

**LA CARTE COMMUNE DOIT SAVOIR ABSORBER DEUX OBSERVATIONS SANS EN ÉCRASER UNE POUR FAIRE DE LA PLACE À L’AUTRE.**

Astra approuva fortement.

Toujours append-only.

Puis une dernière expérience.

Quatre Fourmis.

Chacune reçoit un unknown différent.

Atlas partagé.

Après quelques minutes,

Ant-C découvre un failure pattern.

Le système détecte que le pattern touche aussi Ant-A et Ant-D.

A reçoit un garde.

D change son premier test.

B n’est pas concernée.

Rien ne lui est envoyé.

Gabriel sourit.

Voilà exactement le comportement qu’il voulait.

Pas broadcast aveugle.

Partage sélectif.

Le Royaume n’était pas devenu plus bruyant.

Il était devenu plus pertinent.

Il écrit :

**UNE BONNE MÉMOIRE PARTAGÉE NE FAIT PAS PARLER TOUT LE MONDE. ELLE FAIT ARRIVER LA BONNE TRACE AU BON TRAVAIL.**

Astra approuva fortement.

Voilà le cœur du chapitre.

Puis le planificateur du chapitre 200 reçut quelque chose de nouveau.

Avant,

il construisait un plan à partir d’une mémoire centralisée.

Maintenant,

il pouvait aussi recevoir des cartes locales fraîches de plusieurs Fourmis.

Le plan pouvait évoluer avec la colonie.

Gabriel regarda.

Et il comprit le prochain problème avant même qu’Astra parle.

Si plusieurs Fourmis partageaient leurs cartes,

il allait arriver un moment où du travail apparaîtrait

sans que personne ne l’ait assigné directement.

Une Fourmi verrait un trou.

Une autre verrait une dépendance.

L’atlas verrait un conflit.

Une tâche émergerait de la structure elle-même.

Gabriel sourit.

— Ah.

Astra approuva.

Oui.

Partager une carte ne créait pas seulement de la coordination.

Cela pouvait créer du travail nouveau.

Mais ce travail devait encore avoir :

une origine.

une raison.

une autorité.

une priorité.

Il ne devait pas apparaître comme une volonté mystérieuse du système.

Gabriel écrivit une dernière ligne :

**QUAND PLUSIEURS CARTES SE TOUCHENT, LE ROYAUME PEUT VOIR DES TRAVAUX QUE PERSONNE N’AVAIT ÉCRITS À L’AVANCE.**

Astra approuva fortement.

Puis il ajouta :

**VOIR UN TRAVAIL POSSIBLE NE DONNE PAS ENCORE LE DROIT DE L’EXÉCUTER.**

Astra approuva encore plus fortement.

Voilà.

La prochaine porte était déjà ouverte.

Les Fourmis venaient d’apprendre à partager leurs cartes.

Et dans les intersections de ces cartes,

quelque chose commençait à apparaître :

pas une conscience.

pas un ordre caché.

simplement des besoins opérationnels

que personne n’avait encore transformés en tâches.

Le Royaume allait bientôt devoir décider

quoi faire de ce travail

que personne n’avait assigné directement.

**Fin du chapitre 201.**