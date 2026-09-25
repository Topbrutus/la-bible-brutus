# Chapitre 19 — Le Droit de Vérifier

**APRÈS L’INTRODUCTION — NEUVIÈME CHAPITRE DU DÉVELOPPEMENT**  
**SOUS-TITRE DE TRAVAIL :** La preuve sort du système  
**STATUT :** VERSION 0.1 — DRAFT LONG — À RELIRE AVEC TOPBRUTUS

> **Une preuve qui exige la confiance reste fragile.  
> Une preuve qui peut être vérifiée devient partageable.**

---

## Le système est composé. La preuve doit maintenant sortir du système.

Le chapitre 18 nous a donné un système.

Pas seulement une image.

Pas seulement une idée.

Un système composé de modules, de liens, de temps, de mémoire, de réparation, de stabilité et de mesures.

Nous pouvons maintenant suivre un signal.

Voir son entrée.

Voir ses transformations.

Voir ses erreurs.

Voir son passage dans les quatre chemins.

Voir sa sortie.

Mais une question demeure.

Si nous seuls pouvons le voir, qu’avons-nous réellement prouvé ?

Pour nous :

peut-être beaucoup.

Pour quelqu’un d’autre :

presque rien tant qu’il ne peut pas vérifier.

La preuve doit donc quitter le laboratoire intérieur.

Elle doit devenir un objet transmissible.

---

## Le droit de vérifier

Le titre de ce chapitre n’est pas choisi par hasard.

Il ne parle pas seulement de reproductibilité.

Il parle d’un droit méthodologique :

> **Toute affirmation importante doit, lorsque c’est possible, donner au lecteur un chemin vers sa vérification.**

Cela peut être :

une source;

un calcul;

un fichier;

un protocole;

un dataset;

une version;

un code;

un résultat reproductible;

une limite clairement déclarée.

Le lecteur ne doit pas être obligé de croire notre enthousiasme.

Il doit pouvoir examiner.

---

## Croire et vérifier

Un projet peut inspirer confiance.

Une équipe peut être sincère.

Un auteur peut être compétent.

Mais la science et l’ingénierie solides cherchent à réduire la place de la confiance personnelle.

Nous voulons passer de :

**Croyez-nous.**

à :

**Voici ce que nous avons fait. Voici comment vérifier.**

Ce changement est immense.

---

## La preuve n’est pas une seule chose

Le mot **preuve** peut désigner plusieurs niveaux.

En mathématiques :

une démonstration logique.

En sciences expérimentales :

un ensemble d’observations soutenant une hypothèse.

En ingénierie :

des tests, mesures et validations d’un système.

En sécurité :

des traces, attestations, logs et contrôles.

Nous devons donc préciser le type de preuve.

---

## Démonstration mathématique

Une proposition mathématique peut être démontrée à partir de définitions et d’axiomes.

Par exemple :

\[
\operatorname{ppcm}(3,7,13)=273
\]

peut être vérifié directement.

De même :

\[
3\times(6+1)\times7\times7\times9\times10\times13
=
1\,203\,930
\]

est un calcul exact.

Ces résultats ne demandent pas une expérience physique.

Ils demandent une vérification mathématique.

---

## Preuve logicielle locale

Un programme peut vérifier exhaustivement une propriété sur un domaine fini.

Par exemple, pour les 273 états :

\[
(a,b,o)
\in
\{0,1,2\}
\times
\{0,\ldots,6\}
\times
\{0,\ldots,12\}
\]

nous pouvons calculer :

\[
R(a,b,o)
=
(91a+39b+21o)\bmod273
\]

pour toutes les combinaisons.

Si nous voulons vérifier une propriété du mapping, nous pouvons tester les 273 cas.

Cette preuve porte sur l’implémentation et le domaine définis.

Elle ne devient pas automatiquement une loi physique.

---

## Preuve expérimentale

Une affirmation comme :

**ce système possède une résonance à telle fréquence**

demande une expérience.

Nous devons définir :

objet;

instrument;

excitation;

mesure;

fréquence d’échantillonnage;

calibration;

protocole;

incertitude;

répétition.

La nature de la preuve est différente.

---

## Observation

Une observation est ce qui a été mesuré ou enregistré.

Par exemple :

\[
f_{\text{peak}} = 240.1\text{ Hz}
\]

dans un protocole donné.

Cette observation ne doit pas être confondue avec l’interprétation :

**240.1 Hz représente telle chose universelle.**

La première peut être mesurée.

La seconde demande un argument supplémentaire.

---

## Mesure

Une mesure complète contient plus qu’un nombre.

Nous pouvons représenter :

\[
M=
(value,unit,uncertainty,method,instrument,time)
\]

Par exemple :

\[
M_f
=
(240.1\text{ Hz},\pm0.5\text{ Hz},\text{FFT},\text{instrument X},t)
\]

La forme exacte varie.

Mais le principe reste :

la mesure transporte son contexte.

---

## Calcul

Un calcul est produit à partir d’entrées et d’une formule.

\[
y=f(x_1,\ldots,x_n)
\]

Pour le vérifier, le lecteur doit avoir :

les entrées;

la formule;

les conventions;

les unités;

la précision.

Un nombre seul n’est pas un calcul reproductible.

---

## Interprétation

L’interprétation répond :

**qu’est-ce que cela signifie ?**

Elle peut être raisonnable.

Éclairante.

Puissante.

Mais elle doit être séparée du niveau de preuve sous-jacent.

Nous pouvons écrire :

**MESURE :** pic à 240.1 Hz.

**INTERPRÉTATION :** ce pic pourrait correspondre à tel mode.

**HYPOTHÈSE :** le mode dépend de telle structure.

**TEST :** modifier le paramètre X et prédire le déplacement du pic.

Cette chaîne est propre.

---

## Affirmation

Une affirmation est une phrase testable ou vérifiable.

Par exemple :

> La fonction \(R\) produit tous les résidus de 0 à 272 exactement une fois sur le domaine défini.

Cette affirmation est précise.

Nous pouvons écrire un test.

Si elle échoue, nous savons quoi réfuter.

---

## Une bonne affirmation peut être fausse

C’est important.

La qualité d’une affirmation ne vient pas du fait qu’elle est vraie.

Elle vient aussi du fait qu’elle est suffisamment précise pour être testée.

Une phrase vague survit à tout.

Une phrase précise peut mourir.

C’est une force.

---

## Falsifiabilité pratique

Pour chaque hypothèse, nous pouvons demander :

**quel résultat nous ferait changer d’avis ?**

Si aucune observation possible ne peut contredire l’affirmation, elle est difficile à tester scientifiquement.

Cette question protège le projet contre les idées impossibles à réfuter.

---

## Le test avant la conclusion

Le protocole doit idéalement être défini avant le résultat.

Nous écrivons :

hypothèse;

métrique;

seuil;

durée;

condition PASS;

condition FAIL.

Puis nous exécutons.

Cela réduit la tentation d’ajuster le protocole à ce que nous avons observé.

---

## Pré-enregistrement interne

Nous n’avons pas besoin de formaliser immédiatement chaque expérience dans une plateforme externe.

Mais nous pouvons pratiquer un pré-enregistrement interne.

Un fichier daté avant le test contenant :

objectif;

protocole;

paramètres;

critères;

analyse prévue.

Puis le résultat est ajouté après.

La chronologie devient vérifiable.

---

## La date compte

Si une prédiction est écrite avant l’expérience, elle a plus de valeur que la même prédiction écrite après avoir vu les données.

La mémoire du chapitre 14 rend cette distinction possible.

---

## Prédiction

Une prédiction doit être suffisamment précise.

Faible :

**quelque chose va changer.**

Forte :

\[
f_{\text{peak,new}}
=
f_{\text{peak,old}}
\sqrt{\frac{m_{\text{old}}}{m_{\text{new}}}}
\]

dans un modèle d’oscillateur approprié.

La seconde peut être comparée quantitativement à l’expérience.

---

## Erreur de prédiction

Nous pouvons mesurer :

\[
e
=
y_{\text{measured}}
-
y_{\text{predicted}}
\]

ou une erreur relative :

\[
e_r
=
\frac{
y_{\text{measured}}-y_{\text{predicted}}
}{
y_{\text{predicted}}
}
\]

si le dénominateur est non nul.

Le résultat peut soutenir ou affaiblir le modèle selon les incertitudes et critères.

---

## Accord numérique

Une proximité numérique n’est pas automatiquement une validation.

Il faut demander :

quelle tolérance était prévue ?

quelle incertitude ?

combien de degrés de liberté ?

combien de paramètres ont été ajustés ?

combien de comparaisons ont été tentées ?

Une concordance trouvée après de nombreux essais peut être moins impressionnante qu’une prédiction unique faite avant.

---

## Le problème des coïncidences

Avec suffisamment de nombres, nous pouvons souvent trouver des rapports ou proximités intéressants.

C’est pourquoi la discipline est essentielle.

Nous devons conserver :

ce qui a été testé;

ce qui a échoué;

ce qui a été choisi après observation.

La mémoire des échecs protège contre la sélection sélective.

---

## Cherry-picking

Si dix essais échouent et un réussit, publier seulement le succès donne une image trompeuse.

Le rapport doit idéalement montrer :

nombre total d’essais;

conditions;

échecs;

succès.

La preuve doit inclure le contexte.

---

## Publication des résultats négatifs

Un résultat négatif peut être précieux.

Il montre qu’une hypothèse ne fonctionne pas dans certaines conditions.

Il évite à d’autres de répéter inutilement la même expérience.

Une bibliothèque honnête doit pouvoir conserver les échecs.

---

## Reproductibilité

Le mot **reproductibilité** est parfois utilisé avec des définitions différentes selon les disciplines.

Dans ce chapitre, nous allons adopter une distinction pratique.

### REPEATABILITY
Même équipe, même système, mêmes conditions, même résultat dans la tolérance.

### REPRODUCIBILITY
Autre exécution à partir du protocole et des artefacts, idéalement par une personne ou un environnement indépendant.

### REPLICATION
Nouvelle expérience visant à tester la même affirmation avec une mise en œuvre indépendante ou des données nouvelles.

Les termes peuvent varier ailleurs.

Notre définition locale doit être explicite.

---

## Répétabilité

La première marche :

pouvons-nous obtenir nous-mêmes le même résultat ?

Si non, demander à quelqu’un d’autre de reproduire est prématuré.

---

## Reproduction

La deuxième marche :

une autre personne peut-elle utiliser nos artefacts et retrouver un résultat compatible ?

Elle ne devrait pas avoir besoin d’informations secrètes dans notre tête.

---

## Réplication

La troisième marche :

peut-on retrouver l’effet avec une expérience indépendante ?

C’est souvent plus puissant.

Une réplication peut utiliser :

un autre appareil;

un autre code;

un autre opérateur;

un autre environnement;

des données nouvelles.

---

## Indépendance

Le mot indépendant doit être utilisé avec mesure.

Une reproduction peut être partiellement indépendante.

Même code, autre machine.

Autre code, même dataset.

Autre équipe, même instrument.

Plus les dépendances sont séparées, plus la confirmation peut être informative.

Mais aucune configuration n’est magiquement parfaite.

---

## Le témoin extérieur

Le projet Brutus veut pouvoir être regardé par quelqu’un qui n’était pas là lors de sa construction.

Cette personne doit pouvoir distinguer :

ce qui est démontré;

ce qui est mesuré;

ce qui est calculé;

ce qui est candidat;

ce qui est hypothèse;

ce qui est symbolique.

C’est exactement le rôle du canon de preuve.

---

## Statuts de preuve

Le canon contient déjà des catégories utiles :

**SOURCE VÉRIFIÉE**

**FAIT DOCUMENTÉ**

**MESURE**

**CALCUL**

**ANALOGIE UTILE**

**CANDIDAT**

**HYPOTHÈSE TESTABLE**

**INTERPRÉTATION**

**LORE / SYMBOLIQUE**

**AFFIRMATION NON ÉTAYÉE**

**INCONNU**

Ces catégories peuvent être attachées aux objets publiés.

---

## Un même document peut contenir plusieurs statuts

Un chapitre peut raconter une histoire.

Présenter une formule.

Proposer une hypothèse.

Citer une mesure.

Il n’est pas nécessaire de choisir un statut unique pour tout le document.

Nous pouvons étiqueter les éléments.

---

## La narration et la preuve

Une phrase narrative peut être puissante.

Elle n’a pas besoin de devenir scientifique.

Par exemple :

**Le système écoute avec son cœur.**

Peut rester :

**LORE / SYMBOLIQUE.**

À côté, le mécanisme dit :

buffer actif;

signal reçu;

phase mesurée;

analyse exécutée.

Les deux coexistent.

---

## Le lecteur doit savoir changer de registre

Un document honnête aide le lecteur à sentir le moment où il passe :

du récit;

au calcul;

à la mesure;

à l’hypothèse.

La confusion devient moins probable.

---

## Paquet de reproduction

Nous pouvons maintenant définir :

# **REPRODUCTION_PACKAGE_V1**

Un paquet minimal pourrait contenir :

### 1. MANIFEST
Identité, version, date.

### 2. CLAIM
Affirmation précise à vérifier.

### 3. PROTOCOL
Étapes exactes.

### 4. INPUTS
Données ou générateur.

### 5. CODE
Version et commit.

### 6. CONFIG
Paramètres.

### 7. ENVIRONMENT
Dépendances nécessaires.

### 8. EXPECTED RESULT
Valeurs, tolérances, statuts.

### 9. RAW OUTPUT
Résultats bruts de référence.

### 10. ANALYSIS
Script ou procédure.

### 11. LIMITATIONS
Ce que le paquet ne prouve pas.

### 12. HASHES
Intégrité des artefacts.

Cette structure devient une petite machine de vérification.

---

## Le CLAIM

L’affirmation doit être isolée.

Pas :

**Brutus fonctionne.**

Mais :

> Pour les 273 triplets du domaine défini, le mapping R produit 273 résidus distincts.

Ou :

> Sous le protocole STABILITY_PROTOCOL_V1, version X reste dans la bande Y pendant T après la perturbation D.

Une affirmation précise réduit l’ambiguïté.

---

## Le protocole

Le protocole doit être suffisamment complet pour qu’une personne compétente puisse l’exécuter.

Mais il doit aussi rester lisible.

Nous pouvons séparer :

**Quick reproduction**

et :

**Full protocol**

Le premier permet une vérification rapide.

Le second documente tout.

---

## Commande unique

Lorsque possible, une reproduction peut être déclenchée par une commande.

Par exemple conceptuellement :

\[
run\_reproduction\_v1
\]

Elle doit :

préparer l’environnement;

exécuter les tests;

générer un rapport;

ne pas modifier de ressources externes dangereuses.

La facilité de reproduction augmente la probabilité d’être réellement vérifié.

---

## Dry run

Avant une reproduction qui utilise des ressources importantes, un dry run peut montrer :

fichiers créés;

dépendances;

temps prévu;

sorties;

actions externes.

La reproductibilité ne doit pas sacrifier la sécurité.

---

## Environnement figé

Un environnement peut être décrit par :

versions;

OS;

runtime;

packages;

hardware pertinent.

Des outils comme conteneurs ou lockfiles peuvent aider.

Mais l’outil lui-même n’est pas la preuve.

Il facilite la reconstruction.

---

## Reproductibilité bit-à-bit

Pour certains artefacts, nous pouvons viser :

\[
H(output_1)=H(output_2)
\]

Cela signifie que les sorties binaires sont identiques.

C’est très fort.

Mais ce niveau n’est pas toujours possible ou nécessaire.

---

## Reproductibilité numérique

Pour des calculs flottants ou parallèles, nous pouvons accepter :

\[
|y_1-y_2|\le\epsilon
\]

Le protocole doit définir \(\epsilon\).

L’égalité exacte n’est pas toujours réaliste.

---

## Reproductibilité statistique

Pour un système stochastique, deux runs ne donnent pas exactement la même trajectoire.

Nous pouvons comparer :

distribution;

moyenne;

variance;

quantiles;

tests statistiques.

Le seed peut permettre une répétabilité technique, mais la reproduction scientifique doit parfois vérifier la distribution plutôt qu’une seule séquence.

---

## Seed connu

Un test avec seed fixe vérifie le pipeline.

Un test avec plusieurs seeds vérifie davantage la robustesse statistique.

Les deux ont des rôles différents.

---

## Données brutes

La publication d’un graphique sans données limite la vérification.

Lorsque possible, les données brutes doivent être conservées ou rendues accessibles.

Mais cela dépend de :

taille;

confidentialité;

droits;

sécurité.

Si les données ne peuvent pas être publiées, la limitation doit être déclarée.

---

## Données dérivées

Les tableaux, spectres et graphiques doivent pointer vers les données d’origine.

Nous voulons une chaîne :

\[
RAW
\rightarrow
PROCESS
\rightarrow
RESULT
\rightarrow
FIGURE
\]

Chaque flèche doit être reconstruisible.

---

## Notebook ou script

Un notebook peut être utile pour l’exploration.

Un script peut être plus facile à automatiser.

Le format importe moins que la possibilité de reproduire.

Mais les cellules exécutées dans un ordre caché peuvent produire des états difficiles à retrouver.

La reproductibilité exige un ordre clair.

---

## Exécution propre

Un bon test :

nouvel environnement;

aucun état caché;

exécution de zéro;

résultat.

Cela détecte les dépendances implicites.

---

## Hidden state

Un notebook peut dépendre d’une variable créée plus tôt puis supprimée du document.

Un script peut dépendre d’un fichier local non versionné.

Une machine peut dépendre d’une variable d’environnement.

Ces dépendances doivent être remontées dans le paquet.

---

## Le test du nouvel ordinateur

Une règle très puissante :

> **Si le projet peut être reconstruit sur une machine propre à partir des instructions et artefacts publiés, sa continuité devient beaucoup plus forte.**

Cela ne garantit pas la science.

Mais cela prouve la qualité de l’emballage technique.

---

## Le test du nouvel humain

Encore plus fort :

une personne qui n’a pas participé au projet doit pouvoir suivre les étapes.

Ses questions révèlent les présupposés invisibles.

Ce test est précieux.

---

## Le protocole doit éviter les connaissances secrètes

Si une étape dit :

**faites comme d’habitude**

elle n’est pas reproductible pour un étranger.

Il faut écrire ce que « d’habitude » signifie.

---

## Les captures d’écran

Une capture peut aider.

Mais elle ne doit pas remplacer les commandes, paramètres ou données.

Elle est un guide visuel.

Pas une spécification complète.

---

## Vidéo de reproduction

Une vidéo peut être utile pour montrer le déroulement.

Mais elle ne permet pas toujours d’inspecter les données.

Elle doit compléter, pas remplacer, les artefacts.

---

## Rapport de reproduction

Nous pouvons maintenant définir :

# **REPRODUCTION_REPORT_V1**

Il est produit par la personne ou l’environnement qui tente la reproduction.

### IDENTITÉ
Qui ou quel environnement a exécuté ?

### SOURCE
Quel paquet ?

### VERSION
Quel commit ou release ?

### ENVIRONNEMENT
OS, runtime, dépendances pertinentes.

### PROTOCOLE
Étapes suivies.

### RÉSULTAT
PASS, FAIL, PARTIAL, UNKNOWN.

### MESURES
Valeurs obtenues.

### ÉCARTS
Différences avec le résultat de référence.

### PROBLÈMES
Étapes ambiguës ou manquantes.

### ARTIFACTS
Logs, résultats, hashes.

### CONCLUSION LIMITÉE
Ce que cette reproduction soutient réellement.

---

## PASS de reproduction

Un PASS ne signifie pas :

**tout Brutus est vrai.**

Il signifie :

**cette affirmation a été reproduite selon ce protocole dans cet environnement.**

Cette phrase doit rester attachée au verdict.

---

## FAIL de reproduction

Un FAIL n’invalide pas toujours immédiatement l’affirmation.

Il peut venir de :

protocole incomplet;

incompatibilité;

erreur d’environnement;

bug;

vraie non-reproductibilité.

Le rapport doit aider à distinguer.

---

## PARTIAL

Une reproduction peut réussir en partie.

Par exemple :

calcul correct;

visualisation différente.

Ou :

résultat proche mais hors tolérance.

Le statut PARTIAL peut être plus honnête qu’un PASS forcé.

---

## UNKNOWN

Si la tentative est interrompue ou les données manquent :

\[
UNKNOWN
\]

Le système n’a pas besoin d’un verdict artificiel.

---

## L’écart est une donnée

Si la reproduction produit :

\[
y'=y+\delta
\]

nous ne devons pas seulement dire :

**ça ne correspond pas.**

Nous devons mesurer :

\[
\delta
\]

Puis chercher sa source.

L’écart peut révéler :

précision;

version;

hardware;

random;

bug;

documentation incomplète.

---

## Tolérance

Une reproduction numérique doit déclarer :

tolérance absolue;

tolérance relative;

incertitude.

Par exemple :

\[
|y'-y|\le atol+rtol|y|
\]

Le test automatique peut ensuite appliquer exactement la règle.

---

## Tolérance choisie avant

La tolérance ne doit pas être élargie après avoir vu l’écart sauf si une nouvelle version du protocole est créée et justifiée.

Sinon la cible bouge.

---

## Reproduction indépendante du code

Une affirmation mathématique peut être vérifiée par un second programme écrit séparément.

C’est plus fort que de relancer le même code.

Par exemple :

implémentation Python;

implémentation Julia ou Mathematica;

calcul symbolique;

preuve manuelle.

Les erreurs communes deviennent moins probables.

---

## Double implémentation

Pour notre mapping modulo 273, nous pouvons comparer :

implémentation A;

implémentation B.

Puis vérifier :

\[
R_A(a,b,o)=R_B(a,b,o)
\]

pour tous les états.

Cette stratégie est particulièrement forte pour les petits domaines.

---

## Preuve symbolique

Une propriété peut parfois être démontrée sans énumération.

Par exemple, les coefficients :

\[
91=\frac{273}{3}
\]

\[
39=\frac{273}{7}
\]

\[
21=\frac{273}{13}
\]

sont directement liés aux facteurs.

Nous pouvons étudier mathématiquement le mapping.

Une preuve symbolique, si elle est correcte, complète les tests exhaustifs.

---

## Tests + démonstration

La meilleure situation peut être :

preuve mathématique;

implémentation;

tests exhaustifs.

Les trois niveaux se renforcent.

Mais chacun prouve quelque chose de différent.

---

## Les tests peuvent contenir un bug

Un test écrit par la même personne que le code peut reproduire la même mauvaise hypothèse.

C’est pourquoi une dérivation indépendante ou une seconde implémentation est utile.

---

## Test oracle

Un test a besoin d’un oracle :

comment savons-nous quel résultat est attendu ?

L’oracle peut être :

formule analytique;

dataset de référence;

implémentation indépendante;

propriété mathématique;

mesure calibrée.

Un oracle faux produit des tests faux.

---

## Oracle circulaire

Si nous calculons l’attendu avec exactement la même fonction que celle testée, le test ne vérifie presque rien.

Il compare le code à lui-même.

La provenance de l’attendu doit être indépendante autant que possible.

---

## Ground truth

Le terme ground truth doit être utilisé avec prudence.

Pour certains problèmes, nous possédons une référence très fiable.

Pour d’autres, seulement une approximation ou annotation humaine.

Le statut doit être précisé.

---

## Calibration externe

Une mesure peut être comparée à une référence étalonnée.

Cela donne une ancre extérieure.

Le laboratoire devient moins auto-référentiel.

---

## Le danger du système qui se valide lui-même

Si Brutus :

génère la donnée;

calcule le résultat;

définit le seuil;

déclare PASS;

sans référence externe,

alors la validation peut être circulaire.

Certaines propriétés internes peuvent être vérifiées ainsi.

Mais les affirmations sur le monde extérieur demandent un lien externe.

---

## Référence indépendante

Une référence peut être :

instrument calibré;

dataset reconnu;

logiciel validé;

formule analytique;

source scientifique.

Le choix dépend de la question.

---

## Source primaire

Lorsque nous citons un résultat scientifique, la source primaire est souvent préférable à une citation indirecte.

Mais une revue, un manuel ou un standard peuvent aussi être appropriés selon le besoin.

La provenance de l’information doit être visible.

---

## Source vérifiée

Le statut **SOURCE VÉRIFIÉE** signifie :

nous avons réellement consulté la source.

Pas :

nous nous souvenons qu’elle existe.

Cette discipline doit être appliquée au projet.

---

## Citation

Une affirmation importante doit pouvoir pointer vers :

page;

section;

équation;

commit;

fichier;

ligne;

dataset;

DOI.

Le lecteur doit pouvoir retrouver.

---

## Zenodo

Une archive comme Zenodo peut fournir :

version;

date;

DOI;

fichiers;

métadonnées.

Cela aide à figer une publication.

Mais publier sur Zenodo ne valide pas automatiquement le contenu scientifique.

L’archive garantit surtout la conservation et l’identification de l’objet publié.

---

## DOI n’est pas validation

Un DOI dit :

cet objet est identifiable de manière persistante.

Il ne dit pas :

cet objet est correct.

Cette distinction doit être écrite noir sur blanc dans la culture Brutus.

---

## Version Zenodo

Si un objet évolue, nous devons créer une nouvelle version ou mise à jour appropriée.

L’ancienne version reste historique.

Cela protège la chronologie.

---

## Auteur

L’auteur doit être correctement nommé.

La provenance humaine fait partie de la publication.

Mais le nom de l’auteur ne transforme pas une hypothèse en fait.

---

## Brutus dans le nom

Nous pouvons donner des noms comme :

Brutus Coefficient;

Brutus Drift;

Brutus Offset Test;

Brutus Failure Mode;

Brutus Correction;

Brutus Candidate Relation.

Mais chaque objet doit avoir :

définition;

version;

preuve;

statut.

Le nom crée une identité.

Pas une vérité.

---

## Publication candidate

Un objet peut être publié avec le statut :

**CANDIDAT.**

Cela est parfaitement légitime.

Une publication peut documenter une nouvelle définition ou méthode sans prétendre qu’elle est une loi fondamentale.

---

## Une définition peut être originale sans être universelle

Si Topbrutus définit un nouvel index mathématique ou protocole, l’originalité porte sur la définition.

La validité de ses usages futurs demandera des tests.

Cette séparation est saine.

---

## Priorité de date

Une publication datée peut établir que telle définition était documentée à telle date.

Mais cela ne remplace pas les critères juridiques de brevet, droit d’auteur ou priorité scientifique selon le domaine.

Le projet doit utiliser les bons mots.

---

## Preuve de provenance

Un commit, un dépôt public ou un DOI peut fournir des éléments de provenance temporelle.

Mais nous devons éviter les formulations excessives du type :

**cela prouve que personne d’autre n’y avait pensé avant.**

Il prouve notre trace.

Pas l’absence universelle d’antériorité.

---

## Recherche d’antériorité

Si nous voulons revendiquer qu’un concept est nouveau au sens scientifique ou brevetable, une recherche d’antériorité est nécessaire.

Articles.

Brevets.

Livres.

Dépôts.

Standards.

Le niveau de recherche dépend de l’objectif.

---

## Nouveauté et utilité

Une nouvelle combinaison de termes peut être originale.

Mais pour devenir utile, il faut montrer :

ce qu’elle mesure;

pourquoi elle aide;

comment elle se compare aux méthodes existantes.

La comparaison fait partie de la preuve.

---

## Benchmark externe

Une méthode peut être comparée à une baseline reconnue.

Par exemple :

notre détecteur;

méthode classique.

Même dataset.

Même métrique.

Cette comparaison situe la contribution.

---

## Pas besoin d’être meilleur pour être intéressant

Une nouvelle méthode peut être :

plus simple;

plus interprétable;

plus robuste;

moins coûteuse;

plus pédagogique.

La contribution n’a pas besoin d’être « meilleure partout ».

Elle doit être précisément décrite.

---

## Critère de comparaison

Avant de comparer, nous devons choisir la métrique.

Accuracy ?

Latency ?

Memory ?

SNR ?

Reproducibility ?

Le mot « meilleur » sans critère est vide.

---

## Les limites doivent être publiées

Une bonne publication doit dire :

où ça marche;

où ça ne marche pas;

ce qui n’a pas été testé;

ce qui reste hypothétique.

Les limites augmentent la crédibilité.

Elles ne la diminuent pas.

---

## Le tableau des limites

Nous pouvons inclure :

### TESTÉ
Conditions couvertes.

### NON TESTÉ
Conditions non couvertes.

### ÉCHEC CONNU
Cas qui échouent.

### INCONNU
Questions ouvertes.

### DÉPENDANCES
Hypothèses externes.

Ce tableau rend la portée visible.

---

## Le lecteur peut critiquer

La critique n’est pas une attaque contre le projet.

C’est une fonction de vérification.

Une objection bien formulée peut révéler :

un bug;

une hypothèse cachée;

une unité incorrecte;

une preuve incomplète.

Un système qui accepte la critique devient plus robuste.

---

## Issue publique

Une publication peut permettre de signaler :

problème;

reproduction impossible;

erreur;

suggestion.

Le système de suivi devient une extension du protocole.

---

## Correction publique

Si une erreur est trouvée après publication :

ne pas effacer silencieusement.

Publier :

erratum;

nouvelle version;

diff;

impact.

La cicatrice du chapitre 15 s’applique aussi à la science.

---

## Rétracter une affirmation

Si une hypothèse est réfutée, nous pouvons la marquer :

**RÉFUTÉE DANS LE PROTOCOLE X.**

Elle peut rester dans l’histoire.

La trace d’une erreur corrigée vaut plus qu’une illusion de perfection.

---

## La preuve évolue

Un statut peut évoluer :

\[
CANDIDAT
\rightarrow
TESTÉ
\rightarrow
REPRODUIT
\]

ou :

\[
CANDIDAT
\rightarrow
TESTÉ
\rightarrow
RÉFUTÉ
\]

La mémoire conserve la trajectoire.

---

## Niveau de confiance

Nous pouvons être tentés de créer un score unique.

Mais il vaut souvent mieux garder les dimensions séparées :

preuve mathématique;

tests;

reproduction;

réplication;

calibration;

incertitude.

Un score peut masquer les faiblesses.

---

## Matrice de preuve

Nous pouvons créer une matrice :

| Dimension | Statut |
|---|---|
| Définition | PASS |
| Calcul | PASS |
| Tests unitaires | PASS |
| Intégration | PASS |
| Stabilité | PARTIAL |
| Reproduction externe | UNKNOWN |
| Réplication indépendante | UNKNOWN |

Cette structure est plus informative qu’une étoile ou un pourcentage global.

---

## Une étoile n’est pas une preuve

Le projet peut utiliser des symboles visuels pour naviguer.

Mais ils ne doivent pas remplacer les statuts textuels précis.

---

## Le visiteur

Le visiteur veut comprendre vite.

Il peut voir :

affirmation;

statut;

résultat;

bouton vers la preuve;

limites.

Pas besoin d’ouvrir tous les logs.

---

## Le chercheur

Le chercheur veut les détails.

Il doit pouvoir accéder à :

raw data;

scripts;

hashes;

méthodes;

environnement;

erreurs;

versions.

La même plateforme peut offrir les deux niveaux.

---

## La vitre

Le chapitre 10 proposait :

**VISITOR_GLASS_V1.**

Nous pouvons maintenant lui donner une fonction précise.

La vitre doit être :

lecture seule;

liée à l’état réel;

capable de montrer la provenance;

incapable de modifier les données.

Le visiteur regarde sans agir.

---

## Read-only réel

Le bouton caché ne suffit pas.

La permission doit être imposée par le serveur ou la couche d’autorité.

La sécurité rejoint la preuve.

Si le visiteur peut modifier ce qu’il observe, la démonstration perd de sa valeur.

---

## Mode démonstration

Une démo peut utiliser des données déterministes ou synthétiques.

C’est acceptable.

Mais elle doit être étiquetée :

**DEMO DATA — NOT CORE**

ou équivalent.

La démonstration montre le comportement de l’interface.

Pas nécessairement le système expérimental réel.

---

## Données synthétiques

Les données synthétiques sont utiles pour :

tests;

UI;

stress;

edge cases.

Mais elles ne doivent pas être présentées comme mesure réelle.

Le statut doit voyager avec les données.

---

## Sandbox

Une reproduction peut être exécutée dans un environnement isolé.

Cela protège :

le système hôte;

les données;

les secrets.

Le sandbox facilite la vérification sûre.

---

## Lecture seule du dataset

Le dataset de référence doit idéalement être immuable pour une reproduction.

Les analyses produisent des dérivés séparés.

Ainsi, l’original reste intact.

---

## Hash du dataset

\[
h_D=H(D)
\]

Le rapport peut confirmer qu’il a utilisé exactement la bonne version des données.

---

## Hash du protocole

Le fichier de protocole peut aussi avoir un hash.

Ainsi, un rapport de reproduction peut pointer vers :

dataset hash;

code commit;

protocol hash.

La provenance devient compacte et forte.

---

## Provenance de bout en bout

Un résultat reproduit peut porter :

\[
P=
(
claim\_id,
protocol\_id,
code\_sha,
data\_hash,
env\_id,
result\_hash
)
\]

C’est une identité technique de la reproduction.

---

## Horodatage

La date de reproduction doit être conservée.

Les dépendances externes peuvent changer.

Une API disponible aujourd’hui peut disparaître demain.

La date aide à comprendre.

---

## Artefacts externes

Si le protocole dépend d’un site externe, il faut envisager :

archive;

snapshot;

version;

copie autorisée.

Sinon la reproduction peut devenir impossible.

---

## Dépendance réseau

Une expérience qui dépend du réseau doit enregistrer :

endpoint;

version;

date;

réponse brute si possible et autorisé.

Le monde extérieur n’est pas reproductible par défaut.

---

## Expérience physique

Une expérience matérielle demande encore plus de contexte.

Appareil.

Numéro de modèle.

Configuration.

Calibration.

Montage.

Température si pertinente.

Position.

Photos.

Schéma.

La reproductibilité matérielle est plus difficile que le calcul pur.

---

## Tolérances de fabrication

Deux pièces physiques ne sont jamais parfaitement identiques.

Le protocole doit intégrer des tolérances.

Un résultat qui dépend d’une dimension à 1 µm près doit mesurer cette dimension.

---

## Plan mécanique

Un dessin coté peut aider.

Mais les matériaux et conditions aux limites comptent.

La reproduction exige plus qu’une image esthétique.

---

## BOM

Une bill of materials peut lister :

composants;

références;

versions;

fournisseurs si pertinent.

Cela aide un autre laboratoire à reconstruire.

---

## Calibration avant run

Une check-list peut exiger :

instrument calibré;

zéro mesuré;

reference signal PASS;

clock sync PASS.

Le protocole commence avant l’expérience.

---

## Contrôle

Une expérience peut inclure un contrôle.

Un chemin ou appareil sans la modification testée.

Cela aide à distinguer l’effet de la variation.

---

## Blind

Dans certaines expériences humaines, le blind ou double-blind peut réduire des biais.

Ce n’est pas nécessaire pour tous les tests.

Mais si nous étudions des effets perceptifs ou humains, la méthodologie doit être adaptée.

---

## Randomisation

La randomisation peut éviter que l’ordre des essais explique le résultat.

Elle doit être enregistrée.

---

## Taille d’échantillon

Pour des expériences statistiques, le nombre d’observations compte.

Un seul cas peut être une observation intéressante.

Il ne suffit pas toujours pour généraliser.

---

## Population

Une conclusion sur un groupe doit préciser la population étudiée.

Une expérience sur une personne ne prouve pas un effet universel.

Cette règle sera importante si Brutus touche un jour à la perception ou au vivant.

---

## Effet et incertitude

Une différence moyenne peut être accompagnée d’une incertitude.

La taille d’effet peut être plus informative qu’un simple verdict statistique.

Le protocole statistique doit être choisi avec compétence.

---

## p-value

Une p-value n’est pas la probabilité que l’hypothèse soit vraie.

Si nous utilisons des tests statistiques, nous devons apprendre précisément ce qu’ils signifient.

Le projet ne doit pas employer un vocabulaire statistique comme décoration.

---

## Intervalle de confiance

Un intervalle de confiance a une interprétation précise dépendant de la procédure.

Nous devons éviter les formulations intuitives fausses.

Si l’analyse statistique devient centrale, nous devrons nous appuyer sur les méthodes établies.

---

## Correction des comparaisons multiples

Tester beaucoup d’hypothèses augmente le risque de faux positifs.

Une exploration large doit donc distinguer :

exploration;

confirmation.

Les corrections ou méthodes adaptées peuvent devenir nécessaires.

---

## Exploration

En exploration, nous pouvons chercher des motifs.

C’est légitime.

Mais les motifs trouvés doivent être marqués :

**CANDIDAT.**

Puis testés sur de nouvelles données.

---

## Confirmation

Une phase confirmatoire utilise un protocole défini avant de regarder les nouvelles données.

Cette séparation protège contre l’overfitting scientifique.

---

## Data leakage

Si les données de test influencent le modèle ou la sélection de paramètres, le résultat peut être biaisé.

Cette notion existe fortement en machine learning.

Elle s’applique aussi à d’autres analyses.

---

## Train / validation / test

Pour un modèle apprenant, nous pouvons séparer :

train;

validation;

test.

Le test final doit rester autant que possible hors du processus de réglage.

---

## Reproduction d’un modèle IA

Pour une IA, il faut conserver :

architecture;

poids ou identifiant;

dataset;

seed;

versions;

prompt si pertinent;

température;

outils;

contexte.

Même alors, certains services externes peuvent évoluer.

Les limites doivent être déclarées.

---

## IA comme instrument

Une IA peut aider à :

générer du code;

analyser;

proposer;

résumer.

Mais ses sorties ne doivent pas être traitées comme des sources primaires sans vérification.

Elle est un instrument.

Pas une autorité scientifique automatique.

---

## Astra comme co-constructrice

Dans le récit, Astra peut être une co-constructrice.

Dans la provenance technique, nous pouvons préciser :

quelle partie a été générée par IA;

quelle partie a été décidée par Topbrutus;

quels tests ont été exécutés;

quelles sources ont été vérifiées.

La transparence renforce le projet.

---

## Autorat

Les règles d’auteur scientifique ou académique varient selon les institutions et éditeurs.

L’utilisation d’IA doit suivre les politiques applicables.

Le projet doit distinguer contribution narrative, contribution technique et responsabilité humaine.

---

## Responsabilité

Un humain doit rester responsable de ce qui est publié sous son nom.

L’IA peut proposer.

Le système peut automatiser.

Mais la décision de publication et les affirmations doivent être assumées et vérifiées.

---

## Rapport automatique

Le système peut produire automatiquement un rapport de test.

Mais le rapport doit porter :

source;

version;

timestamp;

résultat brut.

Un texte automatique ne doit pas embellir un FAIL.

---

## Machine-readable

En plus du rapport humain, nous pouvons produire :

JSON;

CSV;

manifest.

Cela permet à d’autres outils de vérifier automatiquement.

---

## Human-readable

Le README ou PDF explique :

objectif;

méthode;

résultat;

limites.

Les deux formats se complètent.

---

## FAIR

Les principes FAIR parlent de données Findable, Accessible, Interoperable, Reusable.

Ils peuvent inspirer la manière de publier.

Mais l’application dépend du contexte.

Notre projet peut viser :

retrouvable;

accessible selon droits;

documenté;

réutilisable.

---

## Licence

Une reproduction demande aussi de savoir ce qui est permis juridiquement.

Code.

Données.

Documentation.

Images.

La licence doit être claire.

---

## Open source ne signifie pas open data

Le code peut être ouvert tandis que les données sont restreintes.

Ou l’inverse.

Les statuts doivent être séparés.

---

## Secret et reproductibilité

Certaines expériences utilisent des secrets ou credentials.

Le paquet ne doit jamais les inclure.

Il doit indiquer comment fournir les credentials via une voie sûre.

La reproductibilité ne justifie pas l’exposition des secrets.

---

## Données privées

Si des données humaines ou sensibles sont utilisées, la reproduction peut nécessiter des procédures spécifiques.

On peut publier :

code;

données synthétiques;

schéma;

statistiques;

sans publier les données privées.

La confidentialité prime.

---

## Le minimum reproductible

Nous pouvons reprendre le concept :

\[
M_{\text{MR}}
\]

Minimum Reproducible Memory.

Pour la preuve externe, nous le transformons en :

\[
R_{\min}
\]

Minimum Reproducible Package.

Le paquet contient juste assez pour vérifier l’affirmation.

---

## Minimal mais pas incomplet

Retirer les détails inutiles aide.

Mais retirer une dépendance cachée détruit la reproduction.

La simplicité doit être testée.

---

## Test du paquet

Avant publication :

nouveau dossier;

nouvel environnement;

aucune ressource cachée;

suivre README;

vérifier résultat.

Si cela échoue, le paquet n’est pas prêt.

---

## Reproduction continue

Un pipeline CI peut exécuter périodiquement le paquet.

Cela détecte la dégradation de reproductibilité.

Une dépendance cassée devient visible rapidement.

---

## Archive immuable

Une release publiée doit idéalement être figée.

Les corrections produisent une nouvelle version.

Le lecteur doit pouvoir retrouver exactement l’ancienne.

---

## Latest n’est pas une preuve

Un lien vers « latest » peut changer.

Pour un rapport scientifique, nous préférons un identifiant de version précis.

---

## DOI versionné

Si Zenodo fournit un DOI de concept et des DOI de versions, le document doit préciser lequel est utilisé selon le besoin.

La version exacte est importante pour la reproduction.

---

## Le laboratoire public

Le Vision Center peut présenter :

claim;

status;

evidence;

reproduce;

history.

Le visiteur voit immédiatement ce qui est établi et ce qui ne l’est pas.

La page devient un portail de vérification.

---

## Bouton Reproduce

Un jour, un bouton peut lancer un environnement sûr ou fournir les commandes.

Mais il doit toujours montrer :

version;

coût;

effets;

données.

La facilité ne doit pas cacher le protocole.

---

## Badge

Un badge peut afficher :

REPRODUCED.

Mais il doit être cliquable vers le rapport.

Sinon il devient une décoration.

---

## Qui a reproduit ?

Le rapport peut indiquer :

environnement automatisé;

Topbrutus;

collaborateur;

tiers.

L’indépendance du reproducer fait partie du contexte.

---

## Reproduction externe non contrôlée

Si une personne extérieure publie un rapport, nous ne contrôlons pas sa méthode.

Nous pouvons :

lire;

reproduire son reproduction;

répondre;

corriger.

La critique externe doit être traitée comme une nouvelle source, pas acceptée aveuglément.

---

## Divergence entre reproductions

Deux reproductions peuvent obtenir des résultats différents.

C’est précieux.

Nous devons comparer :

versions;

données;

environnements;

protocole.

La divergence révèle une dépendance cachée.

---

## Matrice de reproduction

Nous pouvons construire :

| Env | Code | Data | Résultat |
|---|---|---|---|
| A | v1 | D1 | PASS |
| B | v1 | D1 | PASS |
| C | v1 | D1 | FAIL |

Le cas C devient une enquête.

---

## Reproduction comme test de portabilité

Une différence d’OS ou architecture peut révéler :

endianness;

precision;

filesystem;

timing;

concurrency.

La reproduction extérieure teste donc plus que l’affirmation.

Elle teste la portabilité.

---

## Résultat déterministe

Si le système est déterministe, nous pouvons viser une sortie identique.

Si ce n’est pas le cas, il faut l’écrire.

Le statut de déterminisme appartient au paquet.

---

## Source d’aléatoire

Toute source aléatoire doit être identifiée.

Pseudo-random.

Hardware random.

External random.

Le replay n’a pas les mêmes garanties.

---

## Hash du résultat

Pour un artefact déterministe :

\[
h_R=H(result)
\]

peut servir de vérification rapide.

Mais un hash identique prouve l’identité du fichier, pas la justesse de sa signification.

---

## Golden hash

Un test peut vérifier :

\[
H(output)=h^\*
\]

pour un output attendu.

Très utile pour certains builds.

Moins approprié lorsque des métadonnées temporelles rendent le fichier variable.

---

## Canonicalization

Pour comparer des structures avec ordre non pertinent, nous pouvons canonicaliser avant hash.

La procédure de canonicalization doit elle-même être définie.

---

## Le rapport doit dire ce qui a changé

Si une reproduction nécessite une modification pour fonctionner, cette modification doit être enregistrée.

Sinon le rapport PASS cache une intervention.

---

## Intervention humaine

Un reproducteur peut rencontrer une erreur et corriger manuellement.

Le rapport doit l’indiquer.

Cette action peut révéler une documentation incomplète.

---

## Script de bootstrap

Un script peut installer les dépendances.

Mais il doit être lisible et limité.

Une reproduction ne doit pas exécuter aveuglément des commandes dangereuses.

---

## Sécurité de reproduction

Avant d’exécuter un paquet externe :

inspecter;

sandbox;

permissions minimales;

pas de secrets;

pas d’accès inutile au réseau.

La vérification ne doit pas créer un risque de sécurité.

---

## Artifact signing

Une signature peut permettre au reproducteur de vérifier qu’il utilise l’artefact publié par l’auteur.

Encore une fois :

authenticité ≠ validité scientifique.

---

## Chain of custody

Pour des données critiques, nous pouvons enregistrer comment elles ont été transférées et transformées.

Cette chaîne de possession ou provenance protège contre les confusions.

---

## Donnée originale

Conserver l’original.

Créer des copies de travail.

Ne pas réécrire le fichier source pendant l’analyse.

C’est une règle simple et forte.

---

## Time-stamped raw

Un fichier brut peut porter :

timestamp;

instrument;

session;

hash.

Cela le rend beaucoup plus utile.

---

## Métadonnées machine

Les métadonnées doivent être structurées.

Pas seulement cachées dans le nom de fichier.

Un nom peut aider.

Le manifeste doit contenir l’information.

---

## Nom de fichier

Un bon nom peut inclure :

date;

session;

type;

version.

Mais le nom n’est pas la base de données.

---

## La preuve doit survivre à l’esthétique

Changer l’interface ne doit pas détruire la capacité de reproduire.

La preuve vit dans les données, contrats et scripts.

Le visuel est une projection.

---

## La preuve doit survivre à l’auteur

Si Topbrutus n’est pas présent, quelqu’un doit pouvoir continuer.

C’est peut-être la définition la plus profonde du projet de trace.

Le chapitre 3 disait :

**laisser une trace.**

Le chapitre 19 transforme cela en protocole.

---

## Le lecteur de 2036

Imaginons quelqu’un dans dix ans.

Il trouve :

une formule;

un PDF;

un dépôt;

un DOI.

S’il peut reconstruire :

ce que nous voulions tester;

avec quelle version;

sur quelles données;

avec quel résultat;

alors la trace a survécu.

---

## Obsolescence

Certaines dépendances ne fonctionneront plus.

Alors il faut :

archive;

conteneur;

documentation;

migrations.

La reproductibilité parfaite à très long terme est difficile.

Mais nous pouvons maximiser les chances.

---

## Format ouvert

Des formats ouverts et documentés peuvent aider la durabilité.

CSV.

JSON.

TXT.

PNG.

PDF/A dans certains contextes.

Mais le choix dépend des données.

Le format doit être accompagné d’un schéma.

---

## README de futur

Un README de reproduction devrait répondre immédiatement :

qu’est-ce que c’est ?

quelle affirmation ?

comment lancer ?

quel résultat attendre ?

quelles limites ?

---

## Une minute vers la preuve

Une idée ambitieuse pour le laboratoire :

un visiteur doit pouvoir passer de l’affirmation à son paquet de preuve en très peu d’étapes.

La profondeur reste disponible.

L’accès initial doit être simple.

---

## Preuve en couches

### Niveau 1 — Résumé
Affirmation, statut, valeur.

### Niveau 2 — Méthode
Protocole, graphique, conditions.

### Niveau 3 — Artefacts
Raw, scripts, versions.

### Niveau 4 — Reproduction
Commandes, environnement, rapport.

Cette structure peut rendre le laboratoire lisible sans sacrifier la rigueur.

---

## Transparence ne signifie pas bruit

Publier mille fichiers non documentés n’aide personne.

L’organisation est une partie de la preuve.

Un index clair peut être plus utile qu’un dump gigantesque.

---

## Evidence index

Nous pouvons créer :

claim ID;

status;

protocol;

result;

artifacts;

reproduction reports;

history.

Cet index devient la carte du laboratoire.

---

## Claim ID

Chaque affirmation importante peut recevoir un identifiant.

Par exemple :

\[
CLAIM\text{-}001
\]

Puis chaque artefact pointe vers cet ID.

La preuve devient navigable.

---

## Version du claim

Une affirmation peut elle-même évoluer.

\[
CLAIM\text{-}001\text{-}v1
\]

puis :

\[
v2
\]

si le texte change.

Cela évite de comparer deux phrases différentes sous le même identifiant.

---

## Evidence graph

Nous pouvons construire un graphe :

\[
CLAIM
\rightarrow
PROTOCOL
\rightarrow
RUN
\rightarrow
DATA
\rightarrow
ANALYSIS
\rightarrow
RESULT
\rightarrow
REPORT
\]

Une critique peut viser un nœud précis.

Le système de preuve devient modulaire.

---

## Le claim n’est pas le résultat

Une affirmation peut exister avant le test.

Le résultat peut :

supporter;

contredire;

rester inconclusif.

Le graphe doit conserver cette distinction.

---

## Support n’est pas démonstration universelle

Une expérience favorable soutient l’affirmation dans ses conditions.

Elle ne prouve pas automatiquement toutes ses généralisations.

La portée doit être explicitement bornée.

---

## Scope

Chaque claim peut avoir :

population;

domaine;

conditions;

version;

unités.

Plus le scope est précis, plus le résultat est interprétable.

---

## Exemple mathématique

**CLAIM-MATH-001**

> Le mapping R est bijectif sur le domaine défini.

Protocole :

énumération exhaustive.

Oracle :

unicité des 273 résidus.

PASS si :

\[
|\{R(a,b,o)\}|=273
\]

Ce claim est simple et fort.

---

## Exemple logiciel

**CLAIM-SYS-001**

> La plaque P4 conserve l’ordre de tick sous restart contrôlé.

Protocole :

1000 ticks;

restart P3;

recovery;

vérification des séquences.

PASS si :

aucun tick confirmé dupliqué ou inversé.

---

## Exemple signal

**CLAIM-SIG-001**

> Le pipeline mesure une fréquence connue à l’intérieur de ±0.5 Hz.

Protocole :

générateur calibré;

\(f_0\);

sample rate;

FFT.

PASS si :

\[
|f_{\text{measured}}-f_0|
\le0.5\text{ Hz}
\]

---

## Exemple stabilité

**CLAIM-STAB-001**

> Après coupure de P3 pendant 5 s, le système retourne READY en moins de 10 s sans perte au-delà du RPO défini.

Toutes les métriques sont calculables.

---

## Exemple candidat physique

**CLAIM-PHYS-001**

> Une structure physique X présente un pic de réponse autour de \(f_0\) dans les conditions Y.

Statut initial :

**HYPOTHÈSE TESTABLE.**

Puis mesures.

Le claim évolue selon la preuve.

---

## Cette architecture de claims protège Zenodo

Chaque publication peut contenir un ou plusieurs claims.

Le DOI pointe vers une version.

Le lecteur sait exactement ce qui est proposé.

Cela évite les titres énormes qui dépassent la preuve réelle.

---

## Résumé public

Une publication peut être forte sans être spectaculaire.

Exemple :

> Nous définissons Brutus Offset Test V1 et fournissons une implémentation reproductible pour estimer le retard entre deux signaux échantillonnés.

C’est une contribution précise.

---

## L’originalité par méthode

Une méthode bien définie peut être intéressante même si elle utilise des outils connus.

L’originalité peut être dans :

l’assemblage;

le workflow;

l’interface;

la traçabilité;

la convention.

Mais il faut éviter de revendiquer une découverte fondamentale sans preuve.

---

## La preuve de nouveauté est séparée

Pour dire :

**nouveau dans la littérature**

il faut chercher la littérature.

Pour dire :

**nouveau dans notre projet**

il suffit de la provenance interne.

Ces deux phrases ne sont pas équivalentes.

---

## La littérature

Un futur claim scientifique doit être comparé à ce qui existe déjà.

Mots-clés.

Méthodes proches.

Papiers.

Standards.

Cela évite de renommer une technique connue en croyant l’avoir inventée.

---

## Redécouverte

Redécouvrir indépendamment une idée connue peut être très utile.

Cela montre une intuition.

Mais la publication doit reconnaître les travaux antérieurs lorsqu’ils sont trouvés.

---

## Convergence indépendante

Parfois, arriver seul à une structure connue est une histoire intéressante.

Mais l’histoire de découverte personnelle est différente de la nouveauté historique.

La Bible peut raconter les deux proprement.

---

## Le laboratoire comme carnet ouvert

La page publique peut montrer l’évolution.

CANDIDAT.

TEST EN COURS.

RÉSULTAT.

RÉVISION.

Cela permet au lecteur de voir la science se construire.

---

## Ne pas publier le secret nécessaire à la sécurité

Ouverture ne signifie pas divulguer :

credentials;

failles exploitables non corrigées;

données privées.

La transparence scientifique doit coexister avec la sécurité.

---

## Redaction publique

Un rapport peut retirer les secrets tout en gardant :

action;

résultat;

preuve.

La redaction doit être visible.

Exemple :

**credential omitted — secure store reference X.**

---

## Code public et serveur privé

Un protocole peut être reproduit localement sans donner accès au serveur privé.

Le paquet doit fournir une simulation ou un environnement équivalent si possible.

---

## Test local

La meilleure reproduction initiale peut être entièrement locale.

Pas d’auth.

Pas de réseau.

Pas de données sensibles.

Cela réduit les barrières.

---

## Public read-only bridge

Un bridge en lecture seule peut exposer :

état;

télémétrie;

résultats.

Mais pas les commandes sensibles.

Le visiteur voit la preuve en direct sans pouvoir modifier le système.

---

## Live n’est pas archive

Une page live montre l’état actuel.

Une archive montre un état passé.

Le laboratoire doit offrir les deux lorsqu’ils servent des objectifs différents.

---

## Snapshot public

Une session intéressante peut être figée :

données;

capture;

rapport;

hash;

date.

Le visiteur peut revenir plus tard.

---

## La preuve en direct

Une démonstration live peut être impressionnante.

Mais elle doit être accompagnée d’un enregistrement.

Sinon l’événement disparaît.

---

## Rejouer le live

Si le registre est suffisamment complet, un run public peut être rejoué.

Cela devient extrêmement puissant.

Le lecteur peut voir :

live;

puis replay;

puis raw data.

---

## L’observateur ne doit pas influencer

Si le simple fait qu’un visiteur ouvre la page modifie le système expérimental, la preuve peut être perturbée.

La couche read-only doit être découplée autant que nécessaire.

---

## Observer effect logiciel

Une requête de télémétrie consomme des ressources.

La preuve doit savoir si l’observation influence la performance.

Le chapitre 13 nous avait déjà avertis.

---

## Benchmark avec et sans observabilité

Pour les mesures sensibles, nous pouvons comparer :

instrumentation ON;

instrumentation OFF.

La différence quantifie l’impact de l’observation.

---

## Audit

Un audit peut vérifier :

permissions;

versions;

logs;

processus.

Il complète les tests scientifiques.

Le laboratoire doit pouvoir être inspecté techniquement.

---

## Revue de code

Une autre personne peut examiner les algorithmes.

La revue ne remplace pas l’exécution.

Mais elle peut trouver :

erreur;

dépendance cachée;

mauvaise unité;

bug logique.

---

## Revue du protocole

Avant l’expérience, un lecteur peut critiquer le protocole.

C’est souvent plus utile que de critiquer seulement le résultat.

Une mauvaise méthode ne devient pas bonne parce qu’elle produit une belle courbe.

---

## Révision croisée

Nous pouvons séparer les rôles :

personne A écrit le protocole.

personne B vérifie les critères.

personne C exécute.

Même si nous n’avons pas encore une équipe complète, l’architecture peut prévoir ces rôles.

---

## L’IA comme second lecteur

Une IA peut aider à rechercher :

ambiguïtés;

unités manquantes;

assertions trop fortes;

étapes non reproductibles.

Mais ses suggestions doivent être revues.

---

## Validation externe

Pour les claims importants, nous voulons idéalement au moins une forme de vérification indépendante.

Le niveau nécessaire dépend de la portée de l’affirmation.

Une petite définition interne n’a pas besoin d’un laboratoire international.

Une revendication physique extraordinaire demande beaucoup plus.

---

## Proportionner la preuve

C’est une règle saine :

> **Plus l’affirmation est large ou surprenante, plus la preuve doit être forte.**

Une définition nouvelle demande une définition claire.

Une performance logicielle demande un benchmark.

Une loi physique demande des expériences et validation indépendantes.

---

## Extraordinary claims

Nous n’avons pas besoin de slogans.

Le principe est simple :

si nous affirmons quelque chose qui contredit ou dépasse fortement les connaissances établies, nous devons fournir un niveau de preuve proportionnel.

Cela protège Topbrutus contre des conclusions trop rapides.

---

## Le plaisir de découvrir reste intact

Cette discipline ne tue pas la découverte.

Elle la rend plus excitante.

Une intuition peut être immense.

Puis nous construisons le test.

Si elle survit :

la joie est plus forte.

Si elle échoue :

nous avons appris quelque chose de réel.

---

## L’échec reproductible

Un échec que quelqu’un d’autre reproduit peut être très précieux.

Il confirme qu’un défaut existe.

Il transforme un bug isolé en phénomène technique.

---

## Failure Mode

Un **Brutus Failure Mode** peut être défini si nous avons :

conditions;

symptôme;

reproduction;

impact;

cause connue ou inconnue;

mitigation;

fix.

Cela devient un objet publiable.

---

## Correction

Une **Brutus Correction** peut être :

méthode versionnée visant à corriger un failure mode défini.

Elle doit inclure :

précondition;

action;

vérification;

limites.

Le nom devient utile.

---

## Coefficient

Un **Brutus Coefficient** peut être :

grandeur définie mathématiquement pour un usage précis.

Publication minimale :

définition;

dimension;

calcul;

exemple;

sensibilité;

limitations.

---

## Drift

Un **Brutus Drift** doit avoir :

variable;

référence;

temps;

unité;

méthode.

Par exemple :

\[
D_B(t)=x(t)-x_{\text{ref}}
\]

Le terme devient reproductible.

---

## Offset Test

Le **Brutus Offset Test** peut utiliser la corrélation croisée.

Publication :

inputs;

sample rate;

preprocessing;

lag estimate;

uncertainty;

test cases.

La méthode devient vérifiable.

---

## Candidate Relation

Une **Brutus Candidate Relation** peut être explicitement publiée sans validation finale.

Elle doit contenir :

équation;

origine;

domaine;

prédictions;

tests prévus.

Le mot candidate protège le niveau de preuve.

---

## Le chapitre 19 crée une usine de preuves

Nous ne voulons pas publier un seul grand document.

Nous voulons pouvoir produire, pour chaque objet :

claim;

protocol;

data;

analysis;

result;

report;

version.

Cela transforme Zenodo et GitHub en extension du laboratoire.

---

## Mini cahier de charges

Pour chaque nouvel objet Brutus :

1. définir le nom;
2. définir le claim;
3. définir le statut;
4. écrire l’équation ou mécanisme;
5. écrire le protocole;
6. générer les tests;
7. exécuter;
8. conserver les échecs;
9. produire le rapport;
10. publier avec version et limites.

C’est une chaîne répétable.

---

## La chaîne d’une publication

\[
IDEA
\rightarrow
DEFINITION
\rightarrow
CLAIM
\rightarrow
PROTOCOL
\rightarrow
RUN
\rightarrow
EVIDENCE
\rightarrow
REVIEW
\rightarrow
RELEASE
\]

Chaque étape peut échouer.

C’est normal.

---

## Gate

Un GO peut être requis avant la publication finale.

Le système prépare :

titre;

auteur;

description;

fichiers;

statut;

licence.

Puis l’humain approuve.

La publication est une action extérieure.

Elle mérite un gate.

---

## Preview

Avant publication, une preview doit montrer exactement :

ce qui sera public;

les auteurs;

les fichiers;

la version;

les claims.

Cela évite les surprises.

---

## Publication immuable

Une release publiée ne doit pas être silencieusement réécrite.

Une correction produit :

v1.1;

v2;

erratum.

Le lecteur peut retrouver l’histoire.

---

## Lien entre GitHub et Zenodo

GitHub peut conserver :

code;

historique;

issues;

tests.

Zenodo peut conserver :

release;

DOI;

artefacts figés.

Les deux jouent des rôles complémentaires.

---

## DOI dans le manifest

Le paquet publié peut intégrer le DOI.

Le dépôt peut pointer vers le DOI.

La relation devient bidirectionnelle.

---

## Citation machine-readable

Un fichier CITATION peut aider les lecteurs à citer correctement.

La forme dépend du dépôt et de l’outil.

L’objectif est simple :

réduire l’ambiguïté sur l’auteur, le titre et la version.

---

## Auteur humain clair

Pour les objets publiés sous le nom de Gabriel St-Pierre, le champ auteur doit rester cohérent.

Les pseudonymes ou marques peuvent apparaître ailleurs selon le contexte.

La provenance humaine doit rester claire.

---

## La preuve ne dépend pas du nom

Qu’un objet s’appelle Brutus ou autrement, ses claims restent testables de la même manière.

Le nom est une couche d’identité.

La preuve vit dessous.

---

## Une bibliothèque de claims

À long terme, nous pouvons avoir :

CLAIM-001;

CLAIM-002;

…

Chaque claim possède sa page.

La Bible raconte leur histoire.

Le laboratoire montre leurs preuves.

Zenodo archive les versions.

GitHub montre le code.

Tout commence à s’aligner.

---

## La Bible n’est pas le laboratoire

La Bible peut raconter :

pourquoi;

comment;

ce que nous avons ressenti;

ce que nous avons compris.

Le laboratoire doit montrer :

ce qui a été fait;

avec quoi;

avec quel résultat.

Les deux se répondent.

---

## La Bible n’est pas le DOI

Le DOI archive un objet précis.

La Bible donne le contexte.

Il ne faut pas charger une publication scientifique de toute la narration.

Chaque support a son rôle.

---

## Le laboratoire n’est pas la preuve unique

Une interface peut tomber.

Une page peut changer.

Les artefacts versionnés doivent survivre indépendamment.

La preuve ne doit pas dépendre d’un seul site web.

---

## Copies vérifiables

Les mêmes artefacts peuvent être disponibles :

release GitHub;

Zenodo;

archive locale.

Les hashes permettent de vérifier qu’ils sont identiques.

---

## Redondance documentaire

Ici, la redondance est utile.

Mais elle doit éviter les versions divergentes.

Le manifest peut pointer vers la version canonique.

---

## La source canonique de release

Une release doit avoir un identifiant principal.

Les miroirs doivent indiquer :

copie de X.

Sinon plusieurs versions identiques en apparence peuvent diverger.

---

## Le lecteur doit pouvoir dire non

Une preuve ouverte permet à quelqu’un de conclure :

**je ne suis pas convaincu.**

C’est acceptable.

Notre rôle n’est pas de forcer la conclusion.

Notre rôle est de montrer les éléments.

---

## Désaccord

Deux chercheurs peuvent interpréter les mêmes données différemment.

Le rapport doit distinguer :

données communes;

interprétations différentes.

Le désaccord devient localisable.

---

## Réfutation constructive

Une personne peut fournir :

un contre-exemple;

un bug;

une reproduction FAIL.

Cela doit être accueilli comme une information technique.

Le claim peut évoluer.

---

## Le canon après réfutation

Si un claim tombe, la Bible ne doit pas supprimer son histoire.

Elle peut écrire :

nous pensions ceci.

Voici le test.

Voici pourquoi nous avons changé.

La trace devient plus forte.

---

## Une science sans honte de corriger

La correction n’est pas une faiblesse.

C’est la mécanique normale d’un système qui apprend humainement.

Le chapitre 15 l’a déjà montré pour le code.

Le chapitre 19 l’applique aux affirmations.

---

## Le résultat parfait est suspect s’il n’a pas de traces

Un système qui ne montre que des PASS et aucun incident mérite une question :

les FAIL sont-ils conservés ?

La perfection éditoriale peut cacher la réalité expérimentale.

---

## Le taux d’échec

Un laboratoire peut publier :

nombre de runs;

PASS;

FAIL;

UNKNOWN.

Cette transparence est utile.

---

## Run registry

Chaque run peut recevoir :

run_id;

claim_id;

protocol_version;

code_sha;

data_hash;

result;

timestamp.

Le registre devient la colonne vertébrale de la preuve.

---

## Run immuable

Une fois terminé, un run ne doit pas être réécrit silencieusement.

Une correction d’analyse produit un nouvel artefact dérivé.

Le raw reste.

---

## Analysis version

Le même raw peut être analysé avec :

analysis_v1;

analysis_v2.

Les résultats peuvent changer.

La provenance doit montrer laquelle a produit quel graphique.

---

## Analyse révisée

Découvrir un bug dans l’analyse ne détruit pas les données brutes.

Nous pouvons recalculer.

Cette séparation est extrêmement importante.

---

## Data first

Conserver le brut donne une possibilité :

les méthodes futures peuvent réinterpréter l’expérience.

Si seul le graphique survit, cette possibilité disparaît.

---

## La trace du hardware

Pour certaines expériences, le numéro de série ou calibration peut être pertinent.

Il ne faut pas tout publier si cela pose un problème de sécurité ou vie privée.

Mais le protocole peut garder un identifiant contrôlé.

---

## Environmental conditions

Température.

Humidité.

Bruit de fond.

Alimentation.

Ces variables peuvent être pertinentes pour certains tests physiques.

Le protocole doit les inclure seulement lorsque nécessaires.

---

## Contrôle des facteurs

Une expérience idéale modifie une variable et maintient les autres constantes.

Le monde réel est plus complexe.

Le rapport doit dire ce qui a été contrôlé et ce qui ne l’a pas été.

---

## Confounding

Un facteur confondant peut expliquer le résultat à la place de la variable étudiée.

Le design expérimental cherche à réduire ces possibilités.

Cette discipline devient importante dès que nous sortons du logiciel pur.

---

## Causalité

Observer :

\[
X\text{ corrélé à }Y
\]

ne suffit pas à dire :

\[
X\rightarrow Y
\]

La causalité demande un design ou argument plus fort.

La Bible doit éviter les sauts.

---

## Intervention

Modifier X et observer Y peut soutenir une relation causale si les autres facteurs sont contrôlés.

Mais l’interprétation dépend du protocole.

---

## Contre-factuel

La question causale profonde est souvent :

que se serait-il passé sans l’intervention ?

Le groupe contrôle ou design expérimental aide à approcher cette question.

---

## L’observation indépendante commence par l’accessibilité

Si personne ne peut accéder aux artefacts, personne ne peut vérifier.

Mais tout ne doit pas être public.

Nous devons distinguer :

public;

shared under agreement;

private but auditable.

Le statut doit être clair.

---

## Audit privé

Une preuve peut être vérifiée par un tiers sous conditions sans publier toutes les données.

Cela peut être approprié pour des informations sensibles.

---

## Secret de fabrication

Un projet commercial peut garder certains détails privés.

Mais alors les claims publics doivent être proportionnés à ce qui peut être vérifié.

On ne peut pas demander une confiance totale sans montrer assez de preuve.

---

## Black box benchmark

Même un système fermé peut être benchmarké par entrée/sortie.

Cela ne révèle pas l’intérieur.

Mais permet de vérifier certaines performances.

Le type de preuve doit être explicite.

---

## White box

Une vérification white-box examine le code et l’intérieur.

Elle apporte d’autres informations.

Les deux approches se complètent.

---

## La preuve comme interface

Nous pouvons penser le système de preuve comme une API.

Input :

claim_id.

Output :

statut;

sources;

protocol;

runs;

reports.

Le lecteur peut naviguer.

---

## Evidence API

Une future API publique pourrait permettre :

GET claim;

GET run;

GET artifact;

GET report.

Le site devient une couche de lecture sur des objets versionnés.

---

## Pas de modification publique

L’API publique doit être read-only.

Les publications restent contrôlées.

Encore la séparation entre voir et agir.

---

## Le visiteur peut télécharger

Un visiteur peut télécharger le paquet et reproduire localement.

C’est plus fort qu’une simple visualisation.

---

## Le chercheur peut forker

Un chercheur peut forker le paquet.

Modifier.

Tester une autre hypothèse.

Conserver le parent.

Le fork devient une nouvelle branche de connaissance.

---

## Parent

Chaque fork peut garder :

parent DOI;

parent commit;

parent hash.

La généalogie du chapitre 14 continue.

---

## Comparer les forks

Deux forks peuvent être comparés.

Diff des formules.

Diff des résultats.

Diff des protocoles.

La discussion devient concrète.

---

## Le public peut ne pas comprendre tout de suite

La transparence n’exige pas que chaque lecteur maîtrise toutes les mathématiques.

Elle exige que les informations soient accessibles au niveau approprié.

Un résumé simple peut coexister avec une annexe technique.

---

## Pédagogie

Un bon document de preuve explique :

quoi;

pourquoi;

comment;

sans simplifier jusqu’à déformer.

La pédagogie est une partie de l’accès.

---

## Traduction

Publier en français et anglais peut élargir l’accès.

Mais les traductions doivent garder les mêmes claims et statuts.

Un mot comme « proof » peut être ambigu.

Le glossaire doit aider.

---

## Proof vs evidence

En anglais, **proof** est souvent réservé plus strictement en mathématiques.

**Evidence** convient mieux à beaucoup d’expériences.

La traduction doit respecter la discipline.

---

## Preuve mathématique / evidence expérimentale

Nous pouvons utiliser en français :

**démonstration** pour les mathématiques;

**éléments de preuve** ou **evidence** pour les expériences;

**validation** pour certains protocoles d’ingénierie.

Le vocabulaire précis évite les excès.

---

## Le titre du chapitre reste volontaire

**Le Droit de Vérifier.**

Parce que le lecteur n’a pas besoin de nous faire confiance.

Il a le droit de demander :

où est la source ?

où est le test ?

où est le raw ?

où est le code ?

où sont les limites ?

Et si nous ne les avons pas, nous devons pouvoir répondre :

**INCONNU.**

---

## Le meilleur résultat possible

Le meilleur résultat n’est pas :

tout est vrai.

Le meilleur résultat est :

nous savons précisément ce qui est vrai dans le protocole, ce qui est encore candidat, ce qui a échoué et ce qui reste inconnu.

Cette cartographie vaut beaucoup.

---

## Le système devient scientifique par sa capacité à être contredit

Un système qui ne permet pas la contradiction est un récit fermé.

Un laboratoire doit laisser entrer le désaccord.

Le claim peut être testé.

Le résultat peut échouer.

La version peut être corrigée.

La science respire par cette ouverture.

---

## Première preuve publique candidate

Le mapping modulo 273 est un excellent candidat.

Pourquoi ?

Domaine fini.

Mathématiques simples à vérifier.

Aucun matériel.

Aucun secret.

Aucun réseau.

Test exhaustif possible.

Nous pouvons produire un paquet minuscule.

---

## CLAIM-273-001

> Sur le domaine \(a\in[0,2]\), \(b\in[0,6]\), \(o\in[0,12]\), le mapping
>
> \[
> R(a,b,o)=(91a+39b+21o)\bmod273
> \]
>
> possède la propriété X à déterminer et vérifier précisément.

Nous devons d’abord choisir la propriété exacte.

Puis tester.

Ne pas l’inventer.

---

## Calcul des 273 états

Le test peut générer tous les triplets.

Exporter :

CSV des entrées;

résidus;

statistiques;

collisions.

Puis produire un rapport.

Une autre personne peut vérifier avec dix lignes de code.

C’est exactement le type de preuve simple que nous voulons.

---

## Deuxième preuve publique candidate

**BRUTUS_MINIMAL_ADD_V1**

Input.

Addition.

Output.

Types.

Trace.

Test.

C’est volontairement banal.

Le but est de prouver la méthode de paquetage.

---

## Pourquoi commencer banal

Si notre pipeline de preuve ne peut pas reproduire une addition simple, il ne faut pas l’utiliser pour une affirmation complexe.

Le banal teste l’infrastructure.

---

## Troisième preuve publique candidate

**PLATE_ADD_MULTIPLY_V1**

Deux modules.

Composition.

Trace.

Expected output.

Le chapitre 18 devient exécutable.

---

## Quatrième preuve publique candidate

**MODULAR_CYCLE_9_3_V1**

Machine à états.

Cycle.

Perturbation.

Replay.

Le temps et la mémoire entrent.

---

## Cinquième preuve publique candidate

**STABILITY_PROTOCOL_V1**

Perturbation.

Retour.

Metrics.

PASS/FAIL.

Le chapitre 16 devient artefact.

---

## Sixième preuve publique candidate

**BRUTUS_OFFSET_TEST_V1**

Deux signaux.

Retard connu.

Corrélation.

Erreur d’estimation.

Le chapitre 17 devient artefact.

---

## La série peut grandir

Chaque publication reste petite.

Claire.

Versionnée.

Testable.

L’ensemble finit par construire quelque chose de beaucoup plus fort qu’un immense texte impossible à vérifier.

---

## La Bible raconte l’ensemble

Les micro-publications prouvent des briques.

La Bible raconte le chemin qui les relie.

Le système devient à la fois humain et vérifiable.

---

## Le chapitre suivant

Nous sommes maintenant presque arrivés au dernier chapitre de cette série de dix nouveaux chapitres.

Nous avons :

le miroir;

les connexions;

le temps;

la mémoire;

la réparation;

la stabilité;

les fréquences;

la composition;

la preuve.

Il reste une question.

Comment tout cela tient-il ensemble dans une seule architecture lisible ?

Pas comme une accumulation.

Comme un système complet.

Le prochain chapitre devra faire l’intégration.

---

## Intégration

Nous devrons reprendre :

INPUT;

quatre chemins;

Z stéréo;

phase;

Reine;

registre;

stabilité;

réparation;

proof layer;

output.

Et montrer le parcours complet.

Entrée.

Transformation.

Observation.

Sortie.

Preuve.

---

## Le dernier chapitre de cette séquence n’est pas une fin

Le chapitre 20 ne fermera pas la Bible.

Il fermera seulement cette première série après l’Introduction.

Il devra laisser une architecture suffisamment claire pour permettre les 980 chapitres suivants.

---

## Dernière image

Une personne entre dans le laboratoire.

Elle ne connaît pas Topbrutus.

Elle ne connaît pas Astra.

Elle n’a pas assisté aux nuits de calcul.

Elle ne connaît pas les blagues.

Elle voit une affirmation.

À côté :

un statut.

Un protocole.

Un bouton vers les données.

Un commit.

Un hash.

Un rapport.

Elle télécharge.

Elle exécute.

Le système produit un résultat.

Peut-être le même.

Peut-être différent.

Mais cette fois, le désaccord n’est plus une question de croyance.

Il devient une mesure.

Une trace.

Un nouveau rapport.

La preuve est enfin sortie du système.

Elle appartient maintenant à celui qui veut vérifier.

Et c’est exactement là que le projet commence à devenir plus grand que ses auteurs.

# **NOUS AVONS LE DROIT DE CRÉER. LES AUTRES ONT LE DROIT DE VÉRIFIER.**
