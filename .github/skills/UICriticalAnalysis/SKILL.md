---
name: UICriticalAnalysis
description: "Use when auditing an existing portfolio, showcase site, or project page for recruiter/client UX, hero and project-grid composition, mobile layout, generic AI-looking design patterns, and WCAG accessibility. Trigger for 'analyse UI critique', 'audit portfolio recruteur', 'analyse UX client', 'review portfolio design', or 'before redesigning this portfolio'. Run the audits in batches and only use redesign-existing-projects after a prioritized correction plan is explicitly selected. Do not use for a one-off CSS bug, a single accessibility fix, or a request to implement a redesign immediately."
---

# UICriticalAnalysis

Analyse un portfolio existant pour mesurer ce qu'un recruteur ou client voit, comprend et peut utiliser avant de proposer une refonte ciblée.

## Principe

Travaille par lots. Chaque lot produit des constats sourcés et ne modifie aucun fichier. Ne mélange pas les recommandations, ne redessine pas pendant l'analyse, et ne réutilise pas `redesign-existing-projects` avant la sélection explicite des corrections.

## Préparation

1. Définis les visiteurs prioritaires: recruteur et client potentiel, ainsi que leurs tâches principales. Pour un portfolio, ils doivent pouvoir comprendre le profil, évaluer les projets et trouver un moyen de contact.
2. Charge le site dans son état initial. Capture un rendu large, un rendu tablette et un rendu mobile. Vérifie que `document.documentElement.scrollWidth - document.documentElement.clientWidth` vaut `0` à chaque largeur.
3. Confie l'évaluation visuelle à un juge distinct de l'agent qui a construit ou modifié la page. Le juge doit examiner le rendu et le parcours, pas seulement le HTML ou le CSS.

## Lot 1: Experience recruteur et client

Utilise `design-ux`.

- Trace les tâches: identifier la spécialité, parcourir les réalisations, juger la crédibilité et engager un contact.
- Evalue les heuristiques de Nielsen, la clarté de l'information, les états, les sorties et le coût de déplacement visuel ou du curseur.
- Produit les constats au format: `Heuristique | Observation située | Impact | Correction proposée`.

## Lot 2: Composition et responsive

Utilise `design-spatial`.

- Juge le hero, le poids visuel du contenu opérable, la hiérarchie et la lisibilité de la grille de projets.
- Examine le passage desktop -> tablette -> mobile: collisions, troncatures, zones tactiles, alignements et overflow horizontal.
- Traite les signaux de balance comme des pistes à examiner, non comme des défauts automatiques.
- Produit les constats au format: `Surface | Largeur concernée | Observation située | Impact | Correction proposée`.

## Lot 3: Specificite visuelle

Utilise `styleseed-design-review`.

- Attribue un score sur 100 a partir d'elements observables dans les sources et les rendus.
- Releve les choix incoherents, generiques ou trop proches de codes d'interface produits par defaut: typographie, accents, rayons, surfaces, icones, etats et microcopie.
- Ne modifie rien dans ce lot.
- Produit le score par categorie et les corrections ordonnees par gain attendu.

## Lot 4: Accessibilite

Utilise `accesslint-audit` en mode rapport.

- Prefere un audit du DOM en direct. Sans site lance, effectue l'audit statique et indique clairement cette limite.
- Regroupe les violations par regle WCAG et par cause racine. Ne liste pas des doublons sans valeur.
- Distingue les violations mecaniquement verifiables des points a valider manuellement: parcours clavier, lecteur d'ecran et clarte des contenus alternatifs.
- Produit: severite, regle WCAG, emplacements affectes, impact et directive de correction.

## Synthese et gate de decision

1. Fusionne les quatre lots dans une matrice unique en eliminant les doublons.
2. Classe chaque correction: `bloquante`, `majeure`, `mineure`, avec un benefice pour recruteur/client, les lots qui l'ont signalee, la portee technique et le risque.
3. Propose au plus trois paquets coherents de corrections. Chaque paquet doit preciser les fichiers ou surfaces touches et les validations necessaires.
4. Arrete-toi et demande la selection d'un paquet avant toute edition de design.

## Apres selection uniquement

Apres que l'utilisateur a choisi un paquet, utilise `redesign-existing-projects` pour appliquer uniquement les corrections retenues. Preserve les comportements, le contenu fonctionnel et les semantiques accessibles. Revalide les lots touches, dont l'absence d'overflow horizontal sur desktop et mobile.

## Rapport final

Rends les sections dans cet ordre:

1. `Contexte et parcours evalues`
2. `Lot 1 - Experience`
3. `Lot 2 - Composition et responsive`
4. `Lot 3 - Specificite visuelle`
5. `Lot 4 - Accessibilite`
6. `Matrice de priorisation`
7. `Paquets de corrections a choisir`
8. `Limites de l'audit`

## When to Use

Utilise ce skill pour une analyse critique complete d'un portfolio ou d'une page de presentation existante, avant de decider d'une refonte UI.

## Limitations

- Ce skill est un audit et une phase de decision, pas une autorisation automatique de modifier le site.
- Il ne remplace pas les tests avec de vrais recruteurs, clients, lecteurs d'ecran ou appareils physiques.
- N'affirme jamais qu'un rendu est corrige sans une verification executable ou un nouveau rendu aux largeurs concernees.
