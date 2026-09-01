# Journal de bord

Consigner les faits utiles des sessions. Omettre les essais sans impact et les détails de commandes.

## Format d'entrée

> Les entrées datées sont classées de la plus récente à la plus ancienne.

```md
## AAAA-MM-JJ - Titre court

- Objectif :
- Faits :
- Fichiers concernés :
- Validation :
- Suite ou blocage :
```

## 2026-09-01 - Préparation pour la publication sur GitHub (Binwinwinw/portfolio)

- Objectif : configurer le projet et les règles d'exclusion pour la publication sur GitHub.
- Faits :
  - Rédaction du fichier `.gitignore` avec règles d'exclusion pour OS, logs, backups (`dev/backup/`), variables d'environnement (`.env`), artefacts Node/Build et fichiers temporaires.
  - Mise à jour de `README.md` avec le lien du dépôt officiel (`https://github.com/Binwinwinw/portfolio`) et la commande de clonage Git.
- Fichiers concernés : `.gitignore`, `README.md`, `dev/docs/JOURNALDEBORD.md`.
- Validation : vérification de la syntaxe `.gitignore` et `README.md`.
- Suite ou blocage : prêt pour le push / publication sur GitHub.

## 2026-09-01 - Synthèse du travail accompli (Version v1.1.0)

- Objectif : consigner le bilan du cycle complet d'itérations UI/UX.
- Faits :
  1. **Règles & Gouvernance** : Intégration de la Règle 1 de vérification critique automatique dans `REGLES.md` et `AGENTS.md`.
  2. **Accessibilité & Sécurité (Paquet 1)** : Briques WCAG 2.1 AA intégrées, `target="_blank"` avec `rel="noopener noreferrer"`, `aria-label` explicites et bouton de contact direct `mailto:contact@binwinwinw.pe.hu`.
  3. **Qualité de code (Paquet 2)** : 0 style CSS inline, factorisation du composant `.card` (DRY) et création de la classe `.section-title`.
  4. **Polish Visuel (Paquet 3)** : Cartes projets interactives (Variante A), isolation tactile mobile, navigation au clavier (`:focus-within`) et intégration du lien vers les 8 autres projets sur GitHub.
  5. **Release Note** : `v1.1.0 - Audit UI/UX complet (accessibilité WCAG 2.1 AA, DRY, contact mailto, polish cartes)`.
- Fichiers concernés : `index.html`, `AGENTS.md`, `dev/docs/REGLES.md`, `dev/docs/JOURNALDEBORD.md`.
- Validation : checklist 100% validée.
- Suite ou blocage : cycle d'itérations UI/UX clos.

## 2026-09-01 - Execution du Paquet 3 : Polish visuel cartes projets & complément KPI 11+ projets

- Objectif : appliquer la Variante A sur `.project-card`, réserver le comportement de survol uniquement aux projets et ajouter le lien vers les autres projets sur GitHub.
- Faits :
  - Application de la Variante A (`border-color: rgba(45, 212, 191, 0.45)` + `transform: translateY(-4px)`) sur `.project-card` avec `@media (hover: hover)` et `:focus-within`.
  - Différenciation visuelle : `.expertise-card` conserve le style `.card` de base sans effet de survol pour une meilleure hiérarchie.
  - Ajout du lien `"Voir les 8 autres projets sur GitHub ↗"` sous la grille de projets avec `target="_blank"`, `rel="noopener noreferrer"` et style discret réactif.
- Fichiers concernés : `index.html`, `dev/docs/JOURNALDEBORD.md`.
- Validation : validation HTML/CSS, vérification responsive et zéro erreur.
- Suite ou blocage : checklist de validation finale 100% exécutée et validée (Version v1.1.0).

## 2026-09-01 - Execution du Paquet 2 : Qualité de code, suppression des styles inline & factorisation DRY

- Objectif : supprimer tous les styles CSS inline et factoriser les répétitions de styles des cartes/panneaux.
- Faits :
  - Suppression de tous les styles inline (`style="..."`) sur les titres `<h2>`.
  - Création de la classe réutilisable `.section-title` avec la fonction `clamp()` et la gestion des marges.
  - Audit et factorisation DRY : création du composant de base `.card` partagé par `.hero-card`, `.project-card`, `.expertise-card`, `.about-panel` et `.contact-panel`.
- Fichiers concernés : `index.html`, `dev/docs/JOURNALDEBORD.md`.
- Validation : validation CSS, zéro erreur remontée par `get_errors`.
- Suite ou blocage : validé par l'utilisateur.

## 2026-09-01 - Execution du Paquet 1 : Accessibilité WCAG + Contact direct + Sécurité des liens

- Objectif : corriger l'accessibilité des liens, ajouter un accès direct par e-mail (`mailto:`) et sécuriser l'ensemble des liens externes avec `rel="noopener noreferrer"`.
- Faits :
  - Ajout du bouton CTA `mailto:contact@binwinwinw.pe.hu` dans le header et du chip principal d'e-mail dans `#contact`.
  - Audit complet des 7 liens externes avec `target="_blank"` : ajout systématique de `rel="noopener noreferrer"`, d'intitulés accessibles `aria-label` et du signal visuel `↗`.
  - Ajout des balises Open Graph et Twitter Cards manquantes dans `<head>`.
- Fichiers concernés : `index.html`, `dev/docs/JOURNALDEBORD.md`.
- Validation : validation HTML/CSS et vérification par `grep_search` / `get_errors`.
- Suite ou blocage : validé par l'utilisateur.

## 2026-09-01 - Ajout de la Règle 1 dans le registre des règles du dépôt

- Objectif : enregistrer la première règle stricte de déroulement du travail pour les agents.
- Faits : ajout de la règle d'enchaînement automatique (review -> simplify -> verif -> correction si nécessaire -> reverif) dans `dev/docs/REGLES.md`.
- Fichiers concernés : `dev/docs/REGLES.md`, `dev/docs/JOURNALDEBORD.md`.
- Validation : relecture et validation de la mise à jour du fichier `dev/docs/REGLES.md`.
- Suite ou blocage : en attente des règles suivantes si le projet le nécessite.

## 2026-09-01 - Initialisation du registre des décisions d'architecture (ADR)

- Objectif : documenter la structure fondamentale du projet et les choix d'architecture dans `dev/docs/DECISIONS.md`.
- Faits : rédaction de la structure ADR et ajout de ADR-001 (Portfolio statique vanille), ADR-002 (Séparation donnée/interface via `projects.json`) et ADR-003 (Système de documentation autonome pour agents).
- Fichiers concernés : `dev/docs/DECISIONS.md`, `dev/docs/JOURNALDEBORD.md`.
- Validation : vérification de la cohérence avec `AGENTS.md`, `index.html` et `projects.json`.
- Suite ou blocage : registres de documentation entièrement initialisés et prêts.

## 2026-09-01 - Cadre de travail des agents

- Objectif : définir les informations communes à tout agent intervenant sur le dépôt.
- Faits : création des instructions racine et définition des rôles du journal, du registre préventif et des décisions.
- Fichiers concernés : `AGENTS.md`, `dev/docs/JOURNALDEBORD.md`, `dev/docs/SPECS.md`.
- Validation : structure de `AGENTS.md` vérifiée par script Node.js.
- Suite ou blocage : alimenter ces registres uniquement à partir de faits ou de règles réellement établis.
