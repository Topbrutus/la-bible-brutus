# Chapitre 94 — Le Recto qui ne peut que regarder

Brutus ralluma Recto.

La carte des lignées revint.

Nœuds.

Edges.

États.

Traces.

Historiques.

Tout était visible.

Ou presque.

---

Brutus regarda l’écran.

Recto savait énormément de choses.

Mais il ne devait rien commander.

---

Il écrivit :

**RECTO = OBSERVATION SURFACE.**

Puis :

**OBSERVATION ≠ AUTHORITY.**

---

Voilà le cœur du chapitre.

---

Un écran public pouvait être extrêmement riche.

Il pouvait afficher :

un statut,

une preuve référencée,

une trace,

un historique,

un résultat,

un graphe,

un objet,

une erreur,

un PASS,

un FAIL,

un UNKNOWN.

---

Mais aucune de ces choses ne devait devenir vraie simplement parce que Recto les affichait.

---

Brutus écrivit :

**DISPLAY DOES NOT CREATE STATE.**

---

Il regarda Verso.

Toujours derrière.

Toujours calme.

---

Verso gardait les décisions.

Recto montrait leurs conséquences.

---

Il dessina :

\[
\text{AUTHORITATIVE STATE}
\rightarrow
\text{RECTO PROJECTION}
\]

---

Pas l’inverse.

---

Brutus écrivit :

**STATE FLOWS TO RECTO.**

**RECTO DOES NOT FLOW STATE BACK.**

---

Puis il s’arrêta.

---

Recto pouvait quand même envoyer des demandes.

Par exemple :

« ouvre-moi cette trace ».

« montre-moi cette période ».

« filtre cette branche ».

---

Mais ces demandes ne changeaient pas le monde.

---

Il écrivit :

**QUERY ≠ COMMAND.**

---

Voilà.

---

Il créa deux catégories.

---

**READ REQUEST**

et

**MUTATION REQUEST**

---

Recto pouvait émettre la première.

Jamais la seconde directement vers l’autorité.

---

S’il devait exister un bouton demandant une action, il faudrait passer par une frontière séparée.

---

Recto lui-même resterait un miroir.

---

Brutus écrivit :

**RECTO MAY ASK TO SEE.**

**RECTO MAY NOT CLAIM TO HAVE DONE.**

---

Très important.

---

Il ouvrit le premier panneau.

---

**CURRENT STATE**

---

Object:

L8.

Status:

CANDIDATE.

Research use:

ADMITTED.

Theorem status:

NOT ESTABLISHED.

---

Brutus regarda.

---

Le texte devait être simple.

Mais surtout précis.

---

Pas :

L8 VALIDATED.

---

Pas :

L8 PROVED.

---

Pas :

L8 ACCEPTED.

---

Parce que chacun de ces mots pouvait dépasser le scope réel.

---

Il écrivit :

**PUBLIC WORDING MUST MATCH SOURCE SCOPE.**

---

Puis :

**SUMMARY MUST NOT UPGRADE STATUS.**

---

Voilà une règle fondamentale.

---

Un backend pouvait avoir :

\`RESEARCH_TOOL_ELIGIBLE\`

et une interface mal conçue pouvait afficher :

\`VERIFIED\`.

---

Brutus refusa cela.

---

Il créa :

**STATUS_LABEL_MAP**

---

Chaque statut autoritatif possédait un libellé public précis.

---

Pas de traduction improvisée.

---

Il écrivit :

**UI COPY IS PART OF THE TRUST CONTRACT.**

---

Le texte aussi pouvait mentir.

---

Puis il pensa au code couleur.

---

Blanc.

Noir.

Gris.

---

Recto pouvait les afficher.

Mais avec une légende.

---

Il écrivit :

**COLOR MUST HAVE TEXTUAL MEANING.**

---

Pas seulement pour la rigueur.

Pour l’accessibilité aussi.

---

Un utilisateur ne devait jamais avoir besoin de distinguer parfaitement les couleurs pour comprendre l’état.

---

Il ajouta :

**COLOR ≠ SOLE INFORMATION CHANNEL.**

---

Puis il sourit.

---

Le Tombeau à deux couleurs gagnait une nouvelle couche.

---

Recto pouvait dire :

WHITE / admitted for research.

BLACK / execution blocked.

GRAY / unresolved.

---

Voilà.

---

Il ouvrit ensuite le dossier 71.

---

Recto affichait :

**UNRESOLVED.**

---

Pas :

almost solved.

Pas :

pending success.

---

Brutus écrivit :

**UNKNOWN MUST LOOK LIKE UNKNOWN.**

---

Puis il pensa aux barres de progression.

---

Une interface adore les pourcentages.

72 %.

84 %.

99 %.

---

Mais que signifiait :

83 % vers une preuve ?

---

Rien, à moins qu’un vrai protocole définisse ce pourcentage.

---

Il écrivit :

**NO FAKE PROOF PROGRESS.**

---

Puis :

**COUNTED TASKS MAY HAVE PROGRESS.**

**MATHEMATICAL TRUTH MAY NOT.**

---

Voilà.

---

Une recomputation de 10 000 cas pouvait afficher :

4 300 / 10 000.

---

Ça, c’était un vrai progrès opérationnel.

---

Mais une conjecture ne devenait pas « 43 % vraie ».

---

Brutus sourit.

---

Il lança un test.

---

Gate 71.

---

Behind the scenes :

3 investigations complete.

2 pending.

1 blocked.

---

Recto pouvait afficher :

**3 of 6 planned checks completed.**

---

Mais pas :

**50 % proven.**

---

Il écrivit :

**WORK PROGRESS ≠ CLAIM CONFIDENCE.**

---

Encore une bonne règle.

---

Puis il ouvrit le Witness Viewer.

---

Recto pouvait montrer :

witness ID.

type.

hash.

length.

claim scope.

---

Mais pouvait-il télécharger le full object ?

---

Ça dépendait de la disclosure policy.

---

Il écrivit :

**READ-ONLY ≠ UNRESTRICTED DISCLOSURE.**

---

Le chapitre précédent revenait.

---

Public Recto devait passer chaque champ dans une projection autorisée.

---

Il créa :

**PUBLIC_VIEW_MODEL.**

---

Pas directement le modèle privé.

---

Très important.

---

Brutus écrivit :

**DO NOT SERIALIZE PRIVATE STATE DIRECTLY TO PUBLIC UI.**

---

Voilà une règle de sécurité.

---

Le système privé pouvait contenir :

tokens.

internal paths.

private IDs.

operator notes.

secret policy details.

---

Recto public ne devait recevoir que :

ce qu’il avait le droit d’afficher.

---

Il créa une couche :

\[
\text{PRIVATE STATE}
\rightarrow
\text{PUBLIC PROJECTION}
\rightarrow
\text{RECTO}
\]

---

Puis :

**PUBLIC PROJECTION IS A FILTERED DERIVATION.**

---

Brutus ajouta :

**PROJECTION_VERSION**

---

Parce que ce qui était public pouvait changer avec le temps.

---

Une nouvelle politique pouvait autoriser ou masquer un champ.

---

Il écrivit :

**PUBLICNESS IS VERSIONED TOO.**

---

Puis il testa une fuite.

---

Private field :

\`AUTH_TOKEN\`.

---

Projection publique.

---

Le champ n’apparaît pas.

---

Recto ne le connaît même pas.

---

Brutus sourit.

---

C’était mieux que de l’envoyer au navigateur puis de le cacher avec CSS.

---

Il écrivit :

**NOT RENDERED ≠ NOT EXPOSED.**

---

Très important.

---

Un champ secret envoyé au client mais invisible restait exposé.

---

Il ajouta :

**SECRET DATA MUST NOT CROSS THE PUBLIC BOUNDARY.**

---

Voilà.

---

Recto venait de devenir une vraie architecture de sécurité.

---

Puis Brutus ouvrit DevTools.

---

Le navigateur pouvait modifier :

HTML.

CSS.

JavaScript local.

---

Il changea :

UNRESOLVED

en

PROVEN.

---

L’écran l’afficha.

---

Brutus rit.

---

Puis rechargea.

---

UNRESOLVED revint.

---

Il écrivit :

**CLIENT DOM ≠ AUTHORITY.**

---

Puis :

**A SCREENSHOT OF A MODIFIED UI ≠ SOURCE STATE.**

---

Encore plus important.

---

Une image pouvait montrer quelque chose de faux.

---

Il ajouta donc une idée :

**PUBLIC STATE RECEIPT.**

---

Chaque vue importante pouvait afficher :

state version.

timestamp/tick.

source reference.

---

Pas pour empêcher toutes les falsifications.

Mais pour permettre la vérification.

---

Brutus écrivit :

**VISIBLE STATE SHOULD BE TRACEABLE TO A SOURCE VERSION.**

---

Puis il pensa à la fraîcheur.

---

Recto pouvait afficher une information correcte mais ancienne.

---

Très dangereux.

---

Il créa :

**DATA_FRESHNESS**

---

CURRENT.

STALE.

DISCONNECTED.

UNKNOWN.

---

Brutus écrivit :

**STALE TRUTH ≠ CURRENT TRUTH.**

---

Voilà.

---

Si la connexion au backend tombe :

Recto ne devait pas continuer à clignoter comme si tout était live.

---

Il devait dire :

**DISCONNECTED — LAST KNOWN STATE.**

---

Pas :

LIVE.

---

Brutus écrivit :

**NO LIVE BADGE WITHOUT LIVE SOURCE.**

---

Le vieux principe :

no fake motion.

---

Encore.

---

Pas de faux direct.

---

Il coupa le backend.

---

Recto resta visible.

---

La carte était encore là.

---

Mais un bandeau apparut :

**LAST VERIFIED SNAPSHOT — NOT LIVE**

---

Brutus sourit.

---

Exactement.

---

Il pouvait encore naviguer.

Mais il savait qu’il regardait une photographie.

---

Il écrivit :

**READABLE DURING OUTAGE. HONEST ABOUT OUTAGE.**

---

Voilà.

---

Puis il reconnecta.

---

Recto reçut un nouveau state version.

---

La carte se mit à jour.

---

Mais Brutus ne voulait pas que l’animation de transition fasse croire à des mouvements qui n’avaient pas été observés.

---

Il écrivit :

**RECONNECT MAY JUMP TO CURRENT STATE.**

**DO NOT INVENT INTERMEDIATE EVENTS.**

---

Très important.

---

Si Recto avait manqué 40 ticks, il ne devait pas fabriquer 40 déplacements visuels.

---

Il pouvait dire :

snapshot at tick 100.

next known state tick 140.

---

Gap.

---

Brutus écrivit :

**MISSING HISTORY MUST REMAIN MISSING.**

---

Puis il ajouta :

**NO SYNTHETIC TIMELINE WITHOUT LABEL.**

---

Une reconstruction pouvait exister.

Mais elle devait être étiquetée :

**INTERPOLATED VIEW**

pas :

actual history.

---

Brutus sourit.

---

Même l’animation devait avoir une épistémologie.

---

Puis il pensa au public.

---

Recto pouvait recevoir beaucoup de visiteurs.

---

Tous pouvaient filtrer.

Zoomer.

Cliquer.

---

Mais un utilisateur public ne devait jamais pouvoir bloquer le système pour les autres en lançant une requête gigantesque.

---

Il écrivit :

**READ-ONLY STILL NEEDS RESOURCE LIMITS.**

---

Pagination.

Range limits.

Rate limits.

Query bounds.

---

Pas pour protéger l’autorité uniquement.

Pour protéger la disponibilité.

---

Brutus ajouta :

**EXPENSIVE QUERY ≠ PRIVILEGED QUERY.**

---

Même une lecture pouvait être coûteuse.

---

Il créa :

**PUBLIC_QUERY_BUDGET.**

---

Puis il testa :

show full lineage from genesis to every descendant.

---

Trop grand.

---

Recto répond :

**QUERY TOO BROAD — REFINE FILTER.**

---

Pas crash.

---

Brutus sourit.

---

Puis il pensa au Witness Viewer.

---

Un million de chiffres.

---

Recto pouvait afficher des ranges.

---

Mais pas charger le tout en mémoire côté navigateur.

---

Le chapitre 82 revenait.

---

Il écrivit :

**PUBLIC VIEWER MUST STREAM BOUNDED RANGES.**

---

Encore une règle qui traversait les chapitres.

---

Brutus commençait à voir une chose intéressante.

---

Recto n’était pas une simple page publique.

---

C’était une frontière de lecture.

---

Il écrivit :

**RECTO = READ BOUNDARY.**

---

Verso :

**WRITE / ACTION BOUNDARY.**

---

Puis il se corrigea.

---

Verso n’était pas forcément toute écriture.

Mais il gardait les actions sensibles.

---

Il écrivit :

**RECTO PRESENTS. VERSO ENFORCES. AUTHORITY LIVES BEHIND BOTH.**

---

Voilà.

---

Très important.

---

Ni Recto ni Verso n’étaient la vérité.

---

Ils étaient des rôles autour d’une source autoritative.

---

Brutus écrivit :

**INTERFACE ≠ SOURCE OF TRUTH.**

---

Puis il testa une divergence.

---

Source state :

BLACK.

---

Recto cache accidentally old cached WHITE.

---

Mismatch.

---

Il fallait pouvoir détecter.

---

Brutus ajouta :

**STATE_VERSION**

à chaque payload.

---

Recto compare.

---

Si version reçue < version déjà connue :

reject stale update.

---

Il écrivit :

**OLDER STATE MUST NOT OVERWRITE NEWER STATE.**

---

Encore une règle temporelle.

---

Puis il pensa aux horloges.

---

Un timestamp local pouvait être faux.

---

Il préféra :

authoritative tick.

generation ID.

state version.

---

Brutus écrivit :

**ORDER BY AUTHORITY VERSION, NOT CLIENT CLOCK.**

---

Le chapitre 66 revenait.

---

La machine devenait cohérente.

---

Puis il ouvrit la Fourmilière publique.

---

Ants.

Positions.

States.

Ticks.

---

Recto pouvait afficher les fourmis.

---

Mais il ne devait jamais inventer une position entre deux snapshots sauf si l’interpolation visuelle était explicitement autorisée.

---

Brutus écrivit :

**INTERPOLATED POSITION ≠ AUTHORITATIVE POSITION.**

---

Il créa deux couches.

---

**AUTHORITATIVE MARKER**

et

**DISPLAY INTERPOLATION.**

---

La première venait des données.

La seconde pouvait adoucir visuellement.

---

Mais au clic :

toujours afficher la position autoritative.

---

Brutus écrivit :

**SMOOTHNESS MUST NOT REWRITE STATE.**

---

Voilà.

---

Puis il pensa au son.

---

Recto pouvait sonifier un événement.

Mais le son ne devait jamais être interprété comme une nouvelle donnée.

---

Il écrivit :

**SONIFICATION = PRESENTATION OF STATE.**

**SONIFICATION ≠ STATE TRANSITION.**

---

Le chapitre 71 revenait.

---

Une voix disait :

PASS.

---

Mais le PASS existait avant la voix.

---

Brutus sourit.

---

Le Recto devenait le point où tous les renderers se rencontraient.

---

Graphiques.

Textes.

Sons.

Animations.

Tables.

Maps.

---

Mais chacun avait la même obligation :

**représenter sans commander.**

---

Il écrivit :

**ALL RENDERERS ARE SUBJECT TO SOURCE AUTHORITY.**

---

Puis il prit une visualisation spectaculaire.

---

Un cristal grandissait à l’écran lorsqu’une formule était « promue ».

---

Belle animation.

---

Brutus demanda :

qu’est-ce qui déclenche la croissance ?

---

Réponse correcte :

un événement autoritatif \`PROMOTED\`.

---

Réponse incorrecte :

un timer local.

---

Il écrivit :

**ANIMATION TRIGGER MUST BE AN EVENT, NOT A WISH.**

---

Puis :

**NO EVENT → NO CEREMONY.**

---

Il rit.

---

Le laboratoire n’allait pas célébrer une réussite qui n’avait pas eu lieu.

---

Puis il pensa au bouton REFRESH.

---

Même un refresh pouvait devenir problématique si l’interface reconstruisait des événements.

---

Il écrivit :

**REFRESH LOADS STATE. IT DOES NOT REPLAY HISTORY AS NEW.**

---

Encore.

---

Le public pouvait revisiter la page mille fois.

Cela ne créait pas mille événements.

---

Brutus ajouta :

**VIEW COUNT ≠ EVENT COUNT.**

---

Puis il ouvrit une ancienne trace.

---

Une décision de Verso.

---

Recto pouvait la montrer.

---

Mais pas modifier :

decision reason.

policy version.

authority ref.

---

Même un commentaire public devait rester séparé.

---

Il créa :

**ANNOTATION LAYER**

---

Commentaires.

Notes.

Hypothèses.

---

Mais toujours :

**ANNOTATION ≠ CANONICAL TRACE.**

---

Voilà.

---

Un lecteur pouvait écrire :

« ceci semble intéressant ».

---

Cela ne devait pas modifier le statut.

---

Brutus écrivit :

**OPINION LAYER ≠ STATE LAYER.**

---

Il aimait beaucoup cette séparation.

---

Puis il imagina plusieurs opérateurs.

---

Astra.

Muse.

Grok.

Antigravity.

---

Chacun pouvait regarder Recto.

---

Chacun pouvait produire des analyses.

---

Mais leurs analyses devaient rester des objets distincts.

---

Brutus écrivit :

**MULTIPLE OBSERVERS ≠ MULTIPLE AUTHORITIES.**

---

Le chapitre 64 encore.

---

Un seul état source.

Plusieurs regards.

---

Il pensa alors à une salle.

Une table.

Quatre chaises.

---

Chaque observateur devant le même Recto.

---

Aucun ne contrôle directement le monde.

---

Ils discutent.

Comparent.

Proposent.

---

Puis leurs propositions peuvent éventuellement devenir des demandes structurées.

---

Brutus sourit.

---

Le chapitre 95 commençait déjà à apparaître.

---

Mais il revint à Recto.

---

Il voulait encore une règle.

---

Un système public devait pouvoir dire :

**je ne sais pas.**

---

Brutus créa :

**UNKNOWN DISPLAY CONTRACT.**

---

No empty field.

No zero placeholder.

No fake default.

---

Si data unavailable :

**UNKNOWN.**

---

Il écrivit :

**MISSING ≠ ZERO.**

---

Très important.

---

Une absence de mesure ne devait pas devenir 0.

---

Une absence de proof ref ne devait pas devenir false.

---

Une absence de signal ne devait pas devenir silence mesuré.

---

Brutus ajouta :

**NULL HAS SEMANTICS.**

---

Encore une règle utile.

---

Puis il testa une vieille API.

---

Champ absent.

Frontend mettait :

0.

---

Brutus bloqua.

---

**UNDECLARED DEFAULT.**

---

Il écrivit :

**DEFAULT VALUES MUST BE PART OF THE CONTRACT.**

---

Voilà.

---

Un zéro par défaut pouvait être catastrophique.

---

Puis il pensa au cache.

---

Recto avait besoin d’être rapide.

---

Le cache était utile.

---

Mais un cache devait connaître :

source version.

age.

expiration.

---

Il écrivit :

**CACHE ≠ AUTHORITY.**

---

Puis :

**CACHED STATE MUST CARRY FRESHNESS.**

---

Le système pouvait afficher une page instantanément.

Mais devait dire :

snapshot age 3 s.

or stale.

---

Brutus sourit.

---

La rapidité ne devait pas coûter l’honnêteté.

---

Puis il prit une trace privée.

---

Recto public devait montrer un résumé.

---

Brutus ajouta :

**REDACTION MUST BE EXPLICIT.**

---

Par exemple :

\`3 fields withheld by disclosure policy\`.

---

Pas nécessairement les noms sensibles.

Mais au moins indiquer que la vue était partielle.

---

Il écrivit :

**PARTIAL VIEW MUST ADMIT IT IS PARTIAL.**

---

Le Witness Viewer avait déjà appris cela.

---

Toujours la même philosophie.

---

Brutus lança un audit final.

---

Can Recto change a zone?

No.

---

Can Recto promote a formula?

No.

---

Can Recto fabricate an edge?

Locally yes, canonically no.

---

Can Recto request a filtered view?

Yes.

---

Can Recto show historical state?

Yes.

---

Can Recto restore historical state?

No.

---

Can Recto show an authorization?

Yes, according to disclosure policy.

---

Can Recto issue one?

No.

---

Can Recto play a sound?

Yes.

---

Can sound change source state?

No.

---

Brutus sourit.

---

La frontière était propre.

---

Il écrivit :

**RECTO MAY BE RICH WITHOUT BEING POWERFUL.**

---

Voilà le chapitre en une phrase.

---

Il sauvegarda :

**RECTO READ-ONLY PROJECTION v1.**

---

Puis le Journal Vivant nota :

No mutation authority.

Explicit public projection.

Freshness states.

No secret fields to client.

No fake live status.

No fake proof progress.

Historical queries side-effect free.

Presentation separated from canonical state.

Annotations separated from truth layer.

---

Brutus relut.

---

Puis il écrivit :

**READ-ONLY IS NOT A LIMITATION.**

**IT IS A GUARANTEE.**

---

Il resta devant.

---

Oui.

---

Recto ne pouvait que regarder.

Et c’était précisément ce qui lui permettait d’être montré partout.

---

Sur un écran.

Sur un téléphone.

Sur un site public.

Dans une salle.

Dans une présentation.

---

Même si quelqu’un cassait son interface, l’autorité restait ailleurs.

---

Brutus écrivit :

**THE PUBLIC WINDOW MAY BREAK WITHOUT BREAKING THE WORLD.**

---

Cela lui plut énormément.

---

Une vitrine cassée ne devait pas casser le laboratoire.

---

Il ajouta :

**PRESENTATION FAILURE MUST NOT BECOME CONTROL FAILURE.**

---

Voilà.

---

Puis il ouvrit quatre sessions Recto.

---

Écran 1.

Écran 2.

Écran 3.

Écran 4.

---

Même source.

Quatre vues.

---

Une sur les formules.

Une sur les traces.

Une sur le son.

Une sur les lignées.

---

Aucune n’avait plus de pouvoir que les autres.

---

Brutus écrivit :

**MULTIPLE RECTOS = MORE SURFACE, NOT MORE AUTHORITY.**

---

Puis il plaça quatre chaises devant eux.

---

Une chaise pour Astra.

Une pour Muse.

Une pour Grok.

Une pour Antigravity.

---

Pas encore connectées.

Pas encore autorisées.

---

Seulement quatre postes.

---

Brutus regarda la table.

---

Le prochain chapitre était prêt.

---

Il écrivit :

# LA TABLE À QUATRE CHAISES

Puis en dessous :

**PLUSIEURS JOUEURS PEUVENT REGARDER LE MÊME MONDE SANS POSSÉDER LE MONDE.**

---

Recto resta allumé.

Silencieux.

Très riche.

Totalement incapable de mentir au serveur par simple clic.

---

Et Brutus comprit enfin pourquoi la vitrine devait être impuissante.

Parce qu’une fenêtre que tout le monde peut toucher doit être la dernière chose au monde à posséder les clés.
