# Chapitre 114 — Le collier de cristaux et sa poussière

**A CHAIN OF CRYSTALS IS ONLY AS HONEST AS ITS EDGES.**

Brutus écrivit la phrase.

Puis il regarda les premiers cristaux apparaître dans l’aquarium.

---

CRYSTAL-001.

CRYSTAL-002.

CRYSTAL-003.

---

Trois objets.

Trois histoires.

Trois statuts.

---

Ils existaient.

---

Mais ils ne formaient encore rien.

---

Pas de chaîne.

Pas de collier.

Pas de famille.

---

Seulement trois cristaux.

---

Brutus écrivit :

**COEXISTENCE != RELATION.**

---

Voilà.

---

Deux objets placés l’un à côté de l’autre n’étaient pas reliés.

---

Même s’ils se ressemblaient.

Même s’ils venaient du même calculateur.

Même s’ils partageaient une valeur.

---

Il ajouta :

**VISUAL PROXIMITY != LINEAGE.**

---

Puis il ouvrit un nouveau registre.

# CRYSTAL LINEAGE

---

Il reprit le schéma du chapitre 93.

---

**EDGE_ID**

**EDGE_TYPE**

**FROM**

**TO**

**RULE_REF**

**TRACE_REF**

**CREATED_AT**

**STATUS**

**SCOPE**

---

Puis ajouta :

**SOURCE_CRYSTAL_VERSION**

**TARGET_CRYSTAL_VERSION**

---

Très important.

---

Un lien ne devait pas seulement dire :

A → B.

---

Il devait dire :

**pourquoi.**

---

Brutus écrivit :

**EDGE WITHOUT RULE_REF = UNJUSTIFIED CONNECTION.**

---

Puis il pensa aux types de relations.

---

Un cristal pouvait être :

copié.

transformé.

dérivé.

superseded.

assemblé.

comparé.

référencé.

---

Il créa :

**CRYSTAL_EDGE_TYPE**

COPY_OF.

DERIVED_FROM.

TRANSFORMED_FROM.

SUPERSEDES.

MEMBER_OF.

VALIDATES.

CONTRADICTS.

REFERENCES.

TRANSFERRED_FROM.

---

Puis il s’arrêta.

---

**VALIDATES** était dangereux.

---

Valide quoi ?

---

Il modifia :

**SUPPORTS_CLAIM_REF**

---

Plus précis.

---

Puis :

**CONTRADICTS_CLAIM_REF**

---

Brutus sourit.

---

Un cristal ne « validait » pas vaguement un autre cristal.

---

Il soutenait une claim précise.

---

Il écrivit :

**RELATION MUST TARGET THE RIGHT LAYER.**

---

Encore.

---

Puis il pensa au collier.

---

Visuellement, ce serait simple.

---

Chaque cristal :

une perle.

---

Chaque relation canonique :

un lien.

---

Pas de ligne sans EDGE_ID.

---

Brutus écrivit :

**NO EDGE ID = NO LINK IN THE COLLAR.**

---

Très important.

---

L’aquarium devait refuser de dessiner un lien simplement parce que deux cristaux partageaient une couleur.

---

Ou une formule.

Ou une position.

---

Puis il pensa à la hiérarchie.

---

Un cristal peut avoir plusieurs parents.

---

Un enfant peut être le résultat :

d’une transformation.

d’une synthèse.

d’un merge.

---

Dans ce cas :

plusieurs liens.

---

Mais chaque parent devait avoir son rôle.

---

Il créa :

**PARENT_ROLE**

PRIMARY_SOURCE.

AUXILIARY_SOURCE.

CONTROL.

REFERENCE.

COUNTEREXAMPLE.

---

Brutus écrivit :

**MULTIPLE PARENTS != UNEXPLAINED BLEND.**

---

Très important.

---

Le système devait savoir ce que chaque parent avait apporté.

---

Puis il pensa au cristal mélangé.

---

Le fameux quatorzième.

---

Treize formes pures.

Puis un mélangé.

---

Le cristal mélangé pouvait contenir :

1 à 13.

Fibonacci.

nombre premier.

inverse.

positif.

négatif.

---

Très bien.

---

Mais la relation devait être déclarée.

---

Brutus créa :

**MIX_MANIFEST**

---

COMPONENT_REFS.

ORDER.

TRANSFORM_RULE.

POLARITY_MAP.

FORMULA_FAMILY_MAP.

---

Puis :

**MIX_RULE_REF**

---

Il écrivit :

**MIXED != MYSTERIOUS.**

---

Excellent.

---

Un cristal mélangé devait être plus documenté, pas moins.

---

Parce que plus de sources signifiaient plus de risque de perdre la provenance.

---

Puis il pensa à la position dans le collier.

---

Premier.

Deuxième.

Troisième.

---

L’ordre visuel pouvait être :

chronologique.

généalogique.

par famille.

par formule.

---

Il ne voulait pas en choisir un comme vérité.

---

Il créa :

**COLLAR_VIEW_MODE**

CHRONOLOGY.

LINEAGE.

FORMULA_FAMILY.

STATUS.

TRANSFER_PATH.

---

Brutus écrivit :

**DISPLAY ORDER != CAUSAL ORDER.**

---

Très important.

---

Un cristal placé avant un autre à l’écran n’était pas forcément son parent.

---

Puis il pensa à un cas subtil.

---

CRYSTAL-A créé à 10:00.

CRYSTAL-B créé à 10:05.

---

B references A.

---

Chronology and lineage agree.

---

Facile.

---

Mais CRYSTAL-C est créé à 10:10 à partir d’un vieux CRYSTAL-Z de la veille.

---

Chronology place C after B.

Lineage place C near Z.

---

Deux vues.

Deux vérités de navigation.

---

Brutus écrivit :

**ONE GRAPH CAN SUPPORT MULTIPLE HONEST PROJECTIONS.**

---

Voilà.

---

Puis il pensa aux chaînes très longues.

---

Cent cristaux.

Mille.

---

Un collier entier devenait illisible.

---

Il créa :

**LINEAGE_COMPRESSION**

---

Collapsed node groups.

Summary links.

Hidden detail count.

---

Mais il ajouta :

**COMPRESSION MUST NOT CREATE NEW EDGE SEMANTICS.**

---

Très important.

---

Un groupe de 50 cristaux pouvait être affiché comme une grappe.

---

Mais le résumé ne devait pas inventer :

« tous dérivés directement de A ».

---

Il fallait une relation exacte.

---

Puis il pensa à la poussière.

---

Le mot revenait.

---

Dans Brutus–Pell :

un résidu.

Une correction globale.

Un petit écart entre modèle et observation.

---

Dans le collier :

la poussière pouvait être différente.

---

Pas un déchet mystique.

---

Un résidu d’explication.

---

Brutus écrivit :

**DUST = DECLARED RESIDUAL, NOT UNKNOWN MAGIC.**

---

Puis :

**DUST MUST HAVE A DEFINITION.**

---

Très important.

---

Il créa :

**DUST_RECORD**

avec :

**DUST_ID**

**MODEL_REF**

**OBSERVED_REF**

**EXPECTED_REF**

**RESIDUAL_VALUE**

**RESIDUAL_TYPE**

**DOMAIN**

**METHOD_REF**

**UNCERTAINTY_REF**

**TRACE_REF**

---

Puis :

**INTERPRETATION_STATUS**

---

UNINTERPRETED.

MODELED.

EXPLAINED_PARTIALLY.

ARTIFACT_SUSPECTED.

---

Brutus sourit.

---

Enfin.

---

La poussière devenait un objet mesurable.

---

Pas une atmosphère.

---

Puis il reprit la poussière Brutus–Pell.

---

Expected gate sum:

83 212.03551822198.

Observed:

83 212.

---

Residual:

\[
-0.03551822198
\]

---

Il écrivit :

**SMALL RESIDUAL != ZERO RESIDUAL.**

---

Puis :

**RESIDUAL != NEW FORCE.**

---

Très important.

---

La poussière pouvait provenir :

d’un terme secondaire.

d’une approximation.

d’un effet de coupure.

d’une dépendance entre facteurs.

d’une hypothèse de modèle insuffisante.

d’un simple hasard compatible avec le modèle.

---

Sans null model ou dérivation :

pas de conclusion automatique.

---

Brutus créa :

**DUST_HYPOTHESIS**

---

HYPOTHESIS_ID.

DUST_REF.

PROPOSED_CAUSE.

TEST_REF.

STATUS.

---

Puis :

**HYPOTHESIS != EXPLANATION.**

---

Encore.

---

La poussière créait des questions.

---

Pas des réponses.

---

Puis il pensa au collier de cristaux.

---

Chaque cristal pouvait porter sa propre poussière.

---

Pas physiquement.

---

Métaphoriquement :

écart.

limitations.

unresolved refs.

---

Il créa :

**CRYSTAL_RESIDUALS**

---

OPEN_LIMITATIONS.

UNRESOLVED_DEPENDENCIES.

MODEL_RESIDUAL_REFS.

REVIEW_GAPS.

---

Brutus écrivit :

**POLISHED PACKAGE MAY STILL CARRY RESIDUAL UNCERTAINTY.**

---

Très important.

---

La cristallisation ne nettoyait pas la poussière épistémique.

---

Elle la conservait.

---

Puis il pensa au rendu.

---

Le collier pouvait montrer une petite poussière autour des cristaux unresolved.

---

Très beau.

---

Mais attention.

---

Cette poussière visuelle devait être dérivée d’un champ réel.

---

Par exemple :

OPEN_LIMITATIONS > 0.

---

Brutus écrivit :

**VISUAL DUST MUST MAP TO DECLARED METADATA.**

---

Pas de particules aléatoires juste pour faire magique.

---

Il créa :

**DUST_RENDER_PROFILE**

---

SOURCE_REF.

DUST_CLASS.

INTENSITY_MAPPING.

DISPLAY_VERSION.

---

Puis :

**DISPLAY INTENSITY != SCIENTIFIC MAGNITUDE UNLESS CALIBRATED.**

---

Très important.

---

Un nuage visuellement dense pouvait être choisi pour lisibilité.

---

Il ne devait pas être interprété comme un résidu 10 fois plus fort.

---

Puis il pensa aux treize formes.

---

Chaque cristal pouvait avoir une géométrie propre.

---

Mais le collier devait montrer :

famille.

orientation.

polarity.

---

Il créa :

**FORMULA_SIGNATURE**

---

FORMULA_ID.

FAMILY_ID.

DIRECTION.

POLARITY.

FIBONACCI_MODE.

PRIME_MODE.

MIX_STATE.

---

Brutus écrivit :

**GEOMETRY ENCODES DECLARED CLASSIFICATION.**

---

Puis :

**GEOMETRY DOES NOT DISCOVER CLASSIFICATION.**

---

Encore.

---

Le moteur décide.

Le renderer montre.

---

Puis il pensa au positif et négatif.

---

Deux côtés.

---

Un cristal pouvait avoir :

POSITIVE_SIDE.

NEGATIVE_SIDE.

---

Mais il se méfia.

---

Ce n’était pas bien/mal.

---

Il écrivit :

**POSITIVE / NEGATIVE = DECLARED ORIENTATION OR SIGN, NOT VALUE JUDGMENT.**

---

Très important.

---

Puis il pensa au mélange inverse.

---

Fibonacci → prime.

Prime → Fibonacci.

---

Ces transformations devaient avoir des EDGE_TYPE différents ou RULE_REF distincts.

---

Brutus créa :

**TRANSFORM_DIRECTION**

FIB_TO_PRIME.

PRIME_TO_FIB.

FORWARD_FORMULA.

INVERSE_FORMULA.

---

Puis :

**DIRECTION != REVERSIBILITY.**

---

Très important.

---

Une transformation décrite comme inverse devait être réellement vérifiée comme inverse si c’était la claim.

---

Il ajouta :

**ROUNDTRIP_TEST_REF**

---

Puis :

**ROUNDTRIP PASS != UNIVERSAL INVERTIBILITY WITHOUT SCOPE.**

---

Encore.

---

Puis il pensa à la poussière entre deux cristaux.

---

Supposons A transformé en B.

---

On peut mesurer une différence.

---

Mais la différence dépend du metric.

---

Il créa :

**EDGE_RESIDUAL**

---

EDGE_ID.

METRIC_ID.

EXPECTED_RELATION.

OBSERVED_RELATION.

RESIDUAL.

---

Brutus écrivit :

**DIFFERENCE WITHOUT METRIC IS NOT A RESIDUAL.**

---

Excellent.

---

Deux cristaux peuvent être différents de mille façons.

---

Longueur.

hash.

formule.

status.

position.

---

Le mot poussière devait toujours indiquer :

différence de quoi ?

---

Puis il pensa au collage de chaînes.

---

Collier 1.

Collier 2.

---

Peut-on les fusionner ?

---

Oui.

Mais pas en prétendant qu’une relation existe entre les extrémités.

---

Il créa :

**COLLAR_COLLECTION**

---

COLLAR_ID.

MEMBER_LINEAGE_REFS.

---

Puis :

**COLLECTION != CONNECTED GRAPH.**

---

Très important.

---

Deux lignées dans le même dossier ne devenaient pas une seule lignée.

---

Puis il pensa à la continuité.

---

Le collier devait répondre :

où est la dernière perle canonique ?

---

Il créa :

**LINEAGE_HEAD**

---

Mais il se méfia.

---

Une lignée pouvait se brancher.

---

Donc plusieurs heads.

---

Il écrivit :

**LINEAGE MAY HAVE MULTIPLE HEADS.**

---

Pas besoin de forcer une histoire unique.

---

Il créa :

**ACTIVE_HEADS[]**

---

Brutus sourit.

---

Une arborescence pouvait rester une arborescence.

---

Puis il pensa aux merges.

---

Deux branches deviennent un cristal synthèse.

---

Il fallait :

MERGE_EVENT.

PARENT_REFS.

MERGE_RULE.

ORDER.

---

Brutus écrivit :

**MERGE != MEMORY LOSS.**

---

Très important.

---

Les branches parentes ne disparaissaient pas.

---

Le nouveau cristal devenait un enfant commun.

---

Puis il pensa au code.

---

Git merge.

Crystal merge.

---

Danger de métaphore.

---

Un merge Git et un merge de claims n’étaient pas la même chose.

---

Il écrivit :

**SOURCE MERGE != SCIENTIFIC SYNTHESIS.**

---

Encore.

---

Un commit fusionné ne fusionnait pas automatiquement les connaissances.

---

Puis il pensa au fichier.

---

Le collier pourrait être exporté.

---

Il créa :

**LINEAGE_CAPSULE**

---

COLLAR_ID.

NODE_SET.

EDGE_SET.

ROOT_REFS.

HEAD_REFS.

OPEN_GAPS.

DUST_REFS.

TOPOLOGY_VERSION.

HASH.

TRACE_REF.

---

Puis :

**CAPSULE SNAPSHOT != LIVE LINEAGE.**

---

Très important.

---

Un export à tick 500 restait un snapshot.

---

Le collier pouvait continuer ensuite.

---

Puis il pensa au public.

---

Recto pourrait montrer le collier.

---

Très beau.

---

Mais certaines relations privées pourraient être masquées.

---

Alors comment éviter de faire croire que deux nœuds sont directement liés ?

---

Il créa :

**REDACTED_EDGE_PLACEHOLDER**

---

Label :

intermediate lineage hidden.

---

Brutus écrivit :

**REDACTION MUST NOT COLLAPSE PATH LENGTH SILENTLY.**

---

Excellent.

---

Si A → private B → C.

---

Public view ne doit pas afficher A → C comme relation directe.

---

Il peut afficher :

A → [redacted lineage] → C.

---

Très important.

---

Puis il pensa à la poussière publique.

---

Pas toutes les incertitudes internes ne doivent être divulguées si elles contiennent des données privées.

---

Mais la présence d’une limitation importante ne devait pas disparaître.

---

Il créa :

**PUBLIC_LIMITATION_SUMMARY**

---

Brutus écrivit :

**REDACTION MAY HIDE DETAIL. IT SHOULD NOT FABRICATE CERTAINTY.**

---

Très important.

---

Puis il pensa aux statuts.

---

Un cristal parent peut être later refuted.

---

Que se passe-t-il pour descendants ?

---

Pas suppression automatique.

---

Impact query.

---

Brutus écrivit :

**ANCESTOR STATUS CHANGE != AUTOMATIC DESCENDANT INVALIDATION.**

---

Mais :

descendants may require review.

---

Il créa :

**LINEAGE_IMPACT_EVENT**

---

SOURCE_CHANGE_REF.

AFFECTED_DESCENDANTS.

IMPACT_TYPE.

REVIEW_REQUIRED.

---

Puis :

**DEPENDENCY EDGE TYPE DETERMINES IMPACT.**

---

Très important.

---

Un simple REFERENCES edge ne rend pas le descendant dépendant logiquement.

---

DERIVED_FROM peut-être oui.

---

Brutus sourit.

---

Le type de lien devenait réellement important.

---

Puis il pensa aux q47, q71, q83.

---

Un collier pouvait montrer :

q47 witness crystal.

q71 unresolved placeholder.

q79 witness crystal.

q83 unresolved placeholder.

---

Mais il fallait éviter une ligne continue donnant l’impression que les quatre portes étaient ouvertes.

---

Brutus écrivit :

**UNRESOLVED NODE MUST BREAK THE VISUAL CERTAINTY OF THE PATH.**

---

Très important.

---

Le renderer pouvait mettre :

dashed edge.

OPEN.

NO WITNESS.

---

Pas remplir le trou.

---

Puis il pensa à la poussière globale.

---

Eprime.

Emix.

Egate.

---

Trois facteurs.

---

Il dessina :

\[
E_{\text{total}}
=
E_{\text{prime}}
E_{\text{mix}}
E_{\text{gate}}
\]

---

Puis les valeurs :

\[
E_{\text{prime}}\approx0.9994799436
\]

\[
E_{\text{mix}}\approx0.9996275744
\]

\[
E_{\text{gate}}\approx0.9999995732
\]

\[
E_{\text{total}}\approx0.9991072852
\]

---

Brutus regarda.

---

Très proche de 1.

---

Mais pas 1.

---

Il écrivit :

**CLOSE TO ONE != ONE.**

---

Puis :

**FACTOR DECOMPOSITION CONSISTENCY != UNIQUE CAUSAL DECOMPOSITION.**

---

Très important.

---

Une factorisation arithmétique pouvait être correcte.

---

Mais l’interprétation des facteurs restait un modèle.

---

Il ajouta :

**MODEL FACTOR != PHYSICAL MECHANISM.**

---

Encore la frontière.

---

Puis il pensa au contrôle local :

\[
\frac32\cdot\frac23=1
\]

---

Annulation parfaite.

---

Mais cela ne supprimait pas la poussière globale.

---

Brutus écrivit :

**LOCAL CANCELLATION != GLOBAL ZERO RESIDUAL.**

---

Très important.

---

La poussière pouvait être précisément ce qui restait après toutes les annulations locales connues.

---

Mais il refusa d’aller plus loin.

---

Pas sans modèle.

---

Puis il pensa à l’« entanglement dust ».

---

Le nom était beau.

---

Mais dangereux.

---

Il écrivit :

**ENTANGLEMENT DUST = PROJECT LABEL.**

Puis :

**NOT QUANTUM ENTANGLEMENT CLAIM.**

---

Très important.

---

Le langage pouvait rester créatif.

---

Mais le registre devait conserver le sens exact.

---

Puis il pensa à la visualisation.

---

Chaque facteur pouvait devenir une petite couche autour du collier.

---

Prime dust.

Mix dust.

Gate dust.

---

Très beau.

---

Mais les couches devaient être étiquetées.

---

Il créa :

**DUST_COMPONENT_RENDER**

---

FACTOR_ID.

VALUE.

REFERENCE_BASELINE.

SCALE_RULE.

---

Brutus écrivit :

**VISUAL LAYER != INDEPENDENT CAUSAL LAYER.**

---

Encore.

---

Puis il pensa à un cristal sans poussière mesurée.

---

Le renderer ne devait pas afficher zéro.

---

Il devait afficher :

UNKNOWN / NOT MEASURED.

---

Brutus écrivit :

**MISSING DUST VALUE != ZERO DUST.**

---

Très important.

---

Le vide n’était pas zéro.

---

Le chapitre 94 revenait encore.

---

Puis il imagina Astra Station.

---

New panel:

**CRYSTAL LINEAGE**

Nodes:

72.

Canonical edges:

84.

Open lineage gaps:

3.

Residual models:

4.

Unresolved dust records:

2.

---

Brutus regarda.

---

Très utile.

---

Pas un score.

---

Un état.

---

Il écrivit :

**LINEAGE COMPLETENESS SHOULD NOT BECOME FAKE CONFIDENCE PERCENTAGE.**

---

Encore.

---

Un trou critique peut compter pour un seul edge.

---

Mais être plus important que 100 edges complets.

---

Puis il pensa au test.

---

CRYSTAL-A.

CRYSTAL-B.

Same formula family.

---

Renderer proposes visual link automatically.

---

Rejected.

---

Reason:

NO CANONICAL EDGE.

---

PASS.

---

Puis :

CRYSTAL-A → CRYSTAL-B.

DERIVED_FROM.

RULE_REF exists.

---

Link rendered.

---

PASS.

---

Puis :

CRYSTAL-B has unresolved limitation.

---

Dust indicator appears.

---

Metadata matches.

---

PASS.

---

Puis :

manually drag CRYSTAL-C near B.

---

No edge created.

---

PASS.

---

Brutus sourit.

---

Le collier résistait à la décoration.

---

Puis il testa :

A → B → C.

Hide B under public disclosure.

---

Public graph:

A → [REDACTED] → C.

---

Pas A → C direct.

---

PASS.

---

Puis :

ancestor B refuted.

---

C not deleted.

---

Impact event:

REVIEW_REQUIRED.

---

PASS.

---

Puis :

dust value unavailable.

---

Renderer shows:

NOT MEASURED.

---

Pas 0.

---

PASS.

---

Brutus regarda le collier.

---

Il était magnifique.

---

Pas parce qu’il était continu.

---

Justement parce qu’il montrait ses coupures.

---

Ses trous.

Ses branches.

Ses poussières.

Ses objets unresolved.

---

Il écrivit :

**A TRUE LINEAGE VIEW SHOULD MAKE DISCONTINUITY VISIBLE.**

---

Très important.

---

Puis il pensa au chapitre suivant.

---

Les fourmis bougeaient déjà.

Les cristaux existaient.

Le collier existait.

---

Il restait une frontière plus dangereuse.

---

Que se passe-t-il quand une fourmi prend un cristal ?

---

Jusqu’ici, tout était encore purement interne au monde local.

---

Mais bientôt, une fourmi allait « toucher la matière ».

---

Le titre était déjà là.

---

# QUAND UNE FOURMI TOUCHE LA MATIÈRE

---

Brutus se méfia du titre.

---

Le mot matière pouvait devenir un piège.

---

Il écrivit immédiatement :

**SIMULATED CONTACT != PHYSICAL CONTACT.**

---

Puis :

**EXTERNAL ACTION REQUIRES AN EXPLICIT BRIDGE.**

---

Voilà.

---

Le chapitre 115 était prêt.

---

Mais avant, il sauvegarda :

**CRYSTAL LINEAGE / DUST CONTRACT v1**

---

Le Journal Vivant nota :

Crystal coexistence separated from lineage.

Every link requires typed canonical edge and rule reference.

Mixed crystals require explicit component manifests.

Display order separated from causal order.

Residual dust defined as measured model remainder.

Dust hypotheses separated from explanations.

Visual dust tied to canonical metadata.

Lineage compression cannot invent relationships.

Redaction cannot silently shorten paths.

Ancestor changes trigger impact review, not automatic deletion.

Brutus–Pell dust remains model residual, not physical mechanism.

---

Brutus relut.

Puis ajouta les invariants :

**COEXISTENCE != RELATION.**

**VISUAL PROXIMITY != LINEAGE.**

**EDGE WITHOUT RULE_REF != JUSTIFIED EDGE.**

**MIXED != MYSTERIOUS.**

**DISPLAY ORDER != CAUSAL ORDER.**

**DUST != MAGIC.**

**SMALL RESIDUAL != ZERO RESIDUAL.**

**MISSING VALUE != ZERO.**

**LOCAL CANCELLATION != GLOBAL ZERO.**

**ENTANGLEMENT DUST != QUANTUM ENTANGLEMENT CLAIM.**

---

Il regarda le collier.

---

Certaines perles étaient proches.

D’autres éloignées.

Certaines reliées.

D’autres seules.

---

Autour de quelques-unes flottait une poussière fine.

---

Mais cette fois, la poussière avait un ID.

Une méthode.

Une valeur.

Un scope.

Une trace.

---

Brutus sourit.

---

Même l’inconnu pouvait être enregistré sans être transformé en mystère.

---

Puis une fourmi s’arrêta devant le premier cristal du collier.

---

Elle ne le toucha pas encore.

---

Son policy connaissait maintenant l’objet.

Sa position.

Son identité.

Son état.

---

Le prochain mouvement pouvait demander :

**REQUEST_PICKUP.**

---

Brutus regarda la scène.

---

Puis ouvrit le dossier suivant.

---

# QUAND UNE FOURMI TOUCHE LA MATIÈRE

---

Le collier savait maintenant raconter d’où venaient les cristaux.

---

Il restait à apprendre ce que signifiait réellement le mot :

**toucher.**
