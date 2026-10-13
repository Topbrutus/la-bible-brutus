# Chapitre 206 — Ce que Verso savait qu’Antmux ne savait pas

Antmux avait construit un bon trajet.

Techniquement,

tout était propre.

Les contrats étaient respectés.

Les dépendances étaient connues.

Les portes d’autorité étaient en place.

Le coût avait été estimé.

Le workflow avait même prévu un replan si quelque chose changeait.

Et pourtant,

Gabriel regardait la route proposée avec un malaise.

— Non.

Astra attendit.

Gabriel pointa Verso.

— Lui, il sait quelque chose que le routeur sait pas.

Voilà.

Le problème n’était pas que Antmux manquait d’une donnée.

Il manquait d’un **contexte**.

Quelque chose que Verso conservait précisément parce que son rôle n’était pas le même.

Gabriel écrivit :

**DEUX ORGANES PEUVENT TRAVAILLER SUR LE MÊME OBJET ET NE PAS SAVOIR LES MÊMES CHOSES.**

Astra approuva fortement.

Voilà le chapitre.

Jusqu’ici,

le Royaume avait beaucoup travaillé sur le partage.

Cartes.

Handoffs.

Questions.

Traces.

Mais partager tout,

tout le temps,

avec tout le monde,

aurait été une mauvaise solution.

Verso existait justement comme espace interne.

Un endroit où davantage de contexte pouvait vivre.

Recto montrait.

Verso savait.

Antmux routait.

Ces fonctions n’étaient pas identiques.

Gabriel écrivit :

**PARTAGER ASSEZ POUR COORDONNER NE SIGNIFIE PAS RENDRE TOUS LES ORGANES IDENTIQUES.**

Astra approuva fortement.

Très important.

Ils ouvrirent le dossier.

### OBJECTIVE-206-001

Un résultat avait passé screening,

contre-test local,

et reproduction sur deux implémentations.

Antmux proposait :

validation renforcée,

puis possible préparation publique.

Raisonnable.

Mais Verso contenait une note interne importante :

le résultat dépendait d’une série de données dont la provenance complète était encore en reconstruction.

Pas fausse.

Pas corrompue.

Mais provenance incomplète.

Antmux n’avait reçu que :

`result_status = reproduced`.

Il n’avait pas reçu :

`provenance_state = incomplete`.

Gabriel grimaca.

Voilà.

Le workflow était valide avec les informations qu’il possédait.

Mais il n’avait pas assez d’informations.

Il écrivit :

**UN BON CHOIX AVEC UN CONTEXTE INCOMPLET PEUT RESTER UN MAUVAIS CHOIX GLOBAL.**

Astra approuva fortement.

Très important.

Mais attention à « global ».

Le Royaume n’avait pas forcément une vue globale absolue.

Chaque organe détenait une partie.

Il fallait donc résoudre un problème plus précis :

**comment Antmux sait-il qu’il lui manque potentiellement un contexte détenu ailleurs?**

Gabriel sourit.

Très bonne question.

Ils créèrent :

### CONTEXT REQUIREMENT

Chaque type de décision importante devait déclarer :

**which context classes are required?**

Exemple avant publication candidate :

- validation status;
- provenance status;
- authority;
- prior-art status;
- public-safety classification;
- unresolved conflicts.

Astra approuva.

Très important.

Antmux ne devait pas nécessairement recevoir tout Verso.

Mais il devait savoir :

« pour cette décision, j’ai besoin d’un verdict de provenance. »

Voilà.

Il écrit :

**LE ROUTEUR N’A PAS BESOIN DE TOUT SAVOIR. IL DOIT SAVOIR QUEL CONTEXTE IL EST OBLIGÉ DE DEMANDER.**

Astra approuva fortement.

Magnifique.

Puis ils modifièrent le workflow.

Avant publication preparation :

### CONTEXT GATE

Request:

`PROVENANCE_CLEARANCE`

Verso répond :

**INCOMPLETE**

Donc route publique bloquée.

Mais le travail interne peut continuer.

Très propre.

Gabriel sourit.

Voilà.

Verso n’avait pas pris la place d’Antmux.

Il avait fourni un contexte que le workflow déclarait nécessaire.

Il écrivit :

**CONSULTER UN AUTRE ORGANE ≠ LUI CÉDER LA DÉCISION.**

Astra approuva fortement.

Très important.

Le routeur garde son rôle.

Verso garde le sien.

Puis une question :

qu’est-ce que Verso sait exactement?

Le mot pouvait devenir vague.

Ils décidèrent de définir.

### VERSO CONTEXT CLASSES

Selon le dossier, Verso peut contenir :

- provenance détaillée;
- notes internes;
- résultats non publiés;
- contradictions ouvertes;
- statuts préliminaires;
- branches abandonnées;
- contraintes opérateur;
- politiques internes;
- décisions humaines non destinées à Recto.

Gabriel approuva.

Très bon.

Mais pas automatiquement toutes ces choses.

Verso n’était pas une boîte magique.

Il stockait les éléments internes réels.

Toujours trace.

Puis ils définissent Antmux.

### ANTMUX KNOWLEDGE

Antmux doit surtout connaître :

- objectifs;
- contrats d’actions;
- dependencies;
- queue states;
- authority;
- relevant context requirements;
- current workflow state;
- route options.

Très important.

Antmux n’avait pas besoin de lire toutes les notes.

Il avait besoin des bonnes assertions.

Gabriel écrit :

**UN ORCHESTRATEUR DOIT ÊTRE RICHE EN CONTRATS ET SOBRE EN CONTENU.**

Astra approuva fortement.

Très belle phrase.

Sinon Antmux devient lui-même Memoria,

Verso,

Validation,

et tout le système fusionne.

Mauvais.

Puis un autre cas.

Verso sait qu’un résultat a été obtenu pendant un mode expérimental où un garde était volontairement désactivé.

Le résultat peut être intéressant.

Mais Antmux ne le sait pas.

Si le résultat est utilisé comme entrée normale,

danger.

Donc Verso doit fournir :

`environment_mode = experimental_bypass`

Le routeur peut alors dire :

revalidate under standard mode before canonical use.

Gabriel sourit.

Voilà.

Le contexte change ce qu’on a le droit de faire du résultat.

Il écrit :

**DEUX RÉSULTATS IDENTIQUES PEUVENT AVOIR DES DROITS DE RÉUTILISATION DIFFÉRENTS SI LEUR CONTEXTE DE PRODUCTION DIFFÈRE.**

Astra approuva fortement.

Très important.

Le contenu seul ne suffit pas.

Provenance.

Toujours.

Puis un autre cas.

Antmux voit une tâche de validation.

Verso sait qu’elle a déjà été explicitement abandonnée par Gabriel pour manque de priorité.

Pas rejetée scientifiquement.

Mais parked.

Antmux pourrait la relancer parce qu’elle semble logique.

Doit-il?

Pas sans vérifier decision state.

Gabriel écrit :

**UNE TÂCHE PEUT ÊTRE TECHNIQUEMENT PERTINENTE ET OPÉRATIONNELLEMENT DIFFÉRÉE.**

Astra approuva fortement.

Voilà.

Verso doit peut-être exposer :

`operator_disposition = PARKED`

Pas le détail privé.

Juste le statut pertinent.

Très important.

Puis un autre type de connaissance.

Verso contient une préférence humaine :

ne pas publier avant un certain contrôle supplémentaire.

Cette préférence n’est pas une loi scientifique.

Mais c’est une contrainte de gouvernance.

Antmux doit la respecter si elle est active.

Gabriel écrit :

**UNE PRÉFÉRENCE OPÉRATEUR PEUT DEVENIR UNE CONTRAINTE DE WORKFLOW SANS DEVENIR UNE VÉRITÉ SCIENTIFIQUE.**

Astra approuva fortement.

Très important.

Encore séparation des rôles.

Puis ils créèrent un mécanisme.

### CONTEXT QUERY

Antmux ne demande pas :

« donne-moi Verso ».

Il demande :

- provenance clearance?
- operator disposition?
- unresolved contradiction?
- publication hold?
- current policy exception?

Verso répond par assertions bornées.

Très propre.

Gabriel sourit.

Ça protégeait aussi la surcharge.

Il écrit :

**DEMANDER UNE RÉPONSE CONTEXTUELLE EST SOUVENT MEILLEUR QUE COPIER TOUT LE CONTEXTE.**

Astra approuva fortement.

Très important.

Puis un problème.

Verso peut lui-même être incomplet.

Donc ses assertions doivent porter :

**status**

**source**

**freshness**

**confidence / completeness class**

Pas faux sentiment d’autorité.

Gabriel écrit :

### CONTEXT ASSERTION

**context_type**

**value**

**scope**

**source_refs**

**freshness**

**completeness**

**authority**

Très propre.

Exemple :

`PROVENANCE_CLEARANCE = INCOMPLETE`

source refs.

current.

authoritative for publication gate.

Excellent.

Puis un autre problème.

Antmux peut consulter Verso trop souvent.

Chaque micro-décision.

Lent.

Donc context requirements par classe de décision.

Pas chaque étape.

Très important.

Gabriel écrit :

**LE CONTEXTE DOIT ÊTRE DEMANDÉ AUX FRONTIÈRES OÙ IL PEUT CHANGER LA DÉCISION.**

Astra approuva fortement.

Encore minimum suffisant.

Puis ils testèrent.

Décision locale de routing Research.

Aucun besoin de provenance publique.

Pas de Verso query.

Validation gate.

Oui.

Publication candidate.

Oui.

Canonical promotion.

Oui.

Très propre.

Puis une autre classe de contexte.

Recto.

Recto savait quelque chose que Verso ne savait pas?

Peut-être l’état exact de ce qui était actuellement visible publiquement.

Voilà.

Si Verso pense qu’un claim n’a jamais été publié,

mais Recto montre une ancienne version,

une correction peut être nécessaire.

Gabriel sourit.

Le problème n’était donc pas simplement :

Verso sait plus.

Chaque surface sait certaines choses différentes.

Il écrit :

**LE ROYAUME N’A PAS UN SEUL CENTRE DE CONTEXTE. IL A DES SOURCES DE CONTEXTE SPÉCIALISÉES.**

Astra approuva fortement.

Très important.

Ils généralisèrent.

### CONTEXT PROVIDERS

**MEMORIA**

history / events.

**VERSO**

internal operational context.

**RECTO**

public current state.

**ANTMUX**

workflow state.

**VALIDATION**

evidence authority.

**MAP/ATLAS**

coverage/topology.

**QUEUE SYSTEM**

work state.

Gabriel regarda.

Voilà.

Aucun n’est « le cerveau total ».

Le système fonctionne parce qu’ils se consultent par contrat.

Il écrit :

**UNE ARCHITECTURE DISTRIBUÉE DEVIENT PLUS SÛRE QUAND ELLE SAIT QUI EST AUTORITATIF POUR QUEL TYPE DE QUESTION.**

Astra approuva fortement.

Très important.

Ils créèrent :

### CONTEXT AUTHORITY TABLE

Question :

« ce résultat a-t-il passé Validation? »

Provider:

Validation registry.

Question :

« a-t-il déjà été publié? »

Provider:

Recto/public registry.

Question :

« pourquoi cette tâche est-elle parked? »

Provider:

Verso / queue decision record.

Question :

« quelles routes ont déjà été testées? »

Provider:

Memoria / Work Map.

Très propre.

Pas faire répondre n’importe quel module à n’importe quoi.

Puis un cas difficile.

Deux providers se contredisent.

Verso :

not published.

Recto :

published.

Qui gagne?

Pour état public actuel :

Recto.

Mais le conflit indique que Verso est stale.

Créer maintenance work.

Chapitre 202.

Gabriel sourit.

Encore.

Il écrit :

**UN CONFLIT DE CONTEXTE DOIT ÊTRE RÉSOLU SELON L’AUTORITÉ DU CHAMP, PAS SELON LE MODULE QU’ON PRÉFÈRE.**

Astra approuva fortement.

Excellent.

Puis un autre conflit.

Validation says claim scoped.

Recto says general.

Ça, c’est grave.

Public semantic mismatch.

Immediate work candidate.

Possible correction.

Très important.

Gabriel écrit :

**QUAND RECTO ET VALIDATION NE RACONTENT PAS LE MÊME NIVEAU D’AUTORITÉ, LE PROBLÈME N’EST PAS UNE DIFFÉRENCE D’OPINION. C’EST UNE INCOHÉRENCE À TRAITER.**

Astra approuva fortement.

Voilà.

Puis ils ont pensé à la propagation.

Si Verso met `publication_hold = true`,

Antmux doit le savoir avant prochaine publication.

Comment?

Push event?

Pull gate?

Les deux.

Critical holds push.

Normal context pull.

Gabriel écrit :

### CONTEXT DELIVERY

**PULL**

workflow asks when needed.

**PUSH**

critical state change that can invalidate active workflows.

Très propre.

Exemple :

publication hold added.

Push to relevant active workflows.

Pas broadcast à tout.

Scope match.

Toujours.

Puis un cas humain.

Gabriel écrit dans Verso :

« ne touche pas à ce dossier aujourd’hui ».

C’est une instruction opérationnelle.

Doit-elle stopper?

Oui,

si bien structurée.

Mais une note libre ne devrait pas automatiquement devenir policy.

Il faut explicitement convertir en control.

Gabriel sourit.

Très important.

Il écrit :

**UNE NOTE HUMAINE N’EST PAS UNE POLICY TANT QU’ELLE N’A PAS ÉTÉ DÉCLARÉE COMME TELLE.**

Astra approuva fortement.

Excellent.

Sinon le système interprète du texte.

Dangereux.

Donc Verso peut contenir :

notes.

controls.

Deux choses.

Très important.

Puis un autre cas.

Verso sait qu’une formule a un nom provisoire.

Recto utilise un autre nom.

Antmux n’a pas besoin de savoir sauf s’il génère publication.

Alors context query :

canonical public label?

Voilà.

Le système peut maintenir cohérence sans charger tout le lexique partout.

Gabriel écrit :

**LE CONTEXTE EST UNE RESSOURCE À DEMANDER, PAS UNE SUBSTANCE À VERSER PARTOUT.**

Astra approuva fortement.

Belle phrase.

Puis ils ont mesuré.

### CONTEXT-GATE TRIAL 206-A

10 workflow decisions.

Without context gates simulation:

3 would have proceeded with insufficient contextual state.

With context gates:

- 2 paused for incomplete provenance;
- 1 blocked by operator disposition;
- 7 unchanged.

Important.

Simulation.

Pas claim général.

Gabriel sourit.

Très utile.

Ils regardèrent les 7 unchanged.

Context gate n’avait pas changé le choix.

Est-ce gaspillage?

Peut-être coût faible.

Mais il faut mesurer.

Encore.

Ils notèrent latency.

Pas de conclusion universelle.

Puis optimisation.

Cache context assertions.

Mais freshness.

Si `publication_hold` change,

cache invalidation.

Très important.

Gabriel écrit :

**CACHER DU CONTEXTE EXIGE DE SAVOIR QUAND CE CONTEXTE N’EST PLUS VRAI.**

Astra approuva fortement.

Encore les dépendances.

Puis un cas de cache stale.

Antmux croit no hold.

Verso added hold.

Danger.

Donc critical context classes require push invalidation.

Très propre.

Ils créèrent :

### CONTEXT CLASS POLICY

**STATIC-LIKE**

Can cache longer.

**VERSION-BOUND**

Invalidate on version.

**STATEFUL**

Short TTL or event invalidation.

**CRITICAL**

Push update mandatory.

Gabriel approuva.

Très bon.

Puis un autre problème.

Information sensible.

Verso peut contenir des secrets.

Antmux ne doit pas les recevoir si un simple verdict suffit.

Très important.

Il écrit :

**UNE DÉCISION PEUT AVOIR BESOIN DU VERDICT SANS AVOIR BESOIN DU SECRET QUI A PRODUIT LE VERDICT.**

Astra approuva fortement.

Excellent.

Least privilege encore.

`secret_valid = true`

sans secret.

Très important.

Puis un cas où Antmux a besoin de plus de détails pour déboguer.

Alors request elevated context.

Authority gate.

Pas automatique.

Très propre.

Puis Gabriel a regardé la philosophie de tout ça.

Au début,

il aurait peut-être voulu que chaque agent sache tout.

Plus simple à imaginer.

Mais moins propre.

Un Royaume où chaque organe connaît tout :

duplication.

staleness.

contradictions.

permissions difficiles.

coût.

Au contraire,

un Royaume où chaque organe sait son rôle

et sait **qui consulter**

peut être plus solide.

Il écrit :

**L’INTELLIGENCE D’UN SYSTÈME DISTRIBUÉ NE VIENT PAS SEULEMENT DE CE QUE CHAQUE PARTIE SAIT. ELLE VIENT AUSSI DE SA CAPACITÉ À SAVOIR OÙ DEMANDER CE QUI LUI MANQUE.**

Astra approuva fortement.

Voilà le cœur du chapitre.

Puis un nouveau dossier arriva.

Antmux composa.

Memory check.

cheap test.

validation.

Avant de continuer,

il demanda :

`VERSO: unresolved operator constraints?`

Réponse :

none.

`VALIDATION: current evidence level?`

scoped.

`RECTO: existing public claim?`

none.

Route continue.

Gabriel sourit.

Il n’avait pas fallu donner tout le Royaume à Antmux.

Seulement trois réponses.

C’était assez.

Puis un autre dossier.

Même processus.

Verso répondit :

**HOLD — AUTHOR REVIEW REQUIRED**

Workflow s’arrêta.

Pas d’erreur.

Pas de conflit.

Une contrainte légitime.

Voilà.

Puis Gabriel réalisa que cela préparait un problème encore plus intéressant.

Que se passe-t-il si Memoria dit :

« dans le passé, cette route était excellente »,

mais l’observation présente dit :

« aujourd’hui, elle échoue »?

L’historique et le présent allaient entrer en conflit.

Pas deux modules seulement.

Deux sources d’autorité temporelle.

Le passé,

qui conseille.

Le présent,

qui observe.

Gabriel regarda Astra.

— Ah, ça, j’aime ça.

Astra approuva.

Oui.

Parce que le système avait appris à utiliser sa mémoire.

Maintenant,

il allait devoir apprendre à ne pas lui obéir quand le monde présent la contredit.

Gabriel écrivit la dernière ligne :

**SAVOIR OÙ SE TROUVE LE CONTEXTE MANQUANT ÉTAIT UNE ÉTAPE.**

Puis :

**SAVOIR QUOI FAIRE QUAND LE CONTEXTE ANCIEN ET L’OBSERVATION PRÉSENTE NE SONT PLUS D’ACCORD EN SERAIT UNE AUTRE.**

Astra approuva fortement.

Le workflow attendait.

Memoria avait son histoire.

Le présent avait ses faits.

Le Royaume allait devoir décider

lequel devait avoir le dernier mot,

et dans quelles conditions.

**Fin du chapitre 206.**