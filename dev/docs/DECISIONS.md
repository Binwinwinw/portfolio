# Registre des décisions d'architecture (ADR)

Consigner les choix d'architecture durables et leurs justifications. Utiliser ce registre pour expliquer la structure du projet et éviter les remises en cause injustifiées.

## Format d'entrée

```md
## ADR-000 - Titre de la décision

- Statut : [Proposé | Accepté | Remplacé]
- Date : AAAA-MM-JJ
- Contexte :
- Décision :
- Conséquences :
- Fichiers concernés :
```

## Décisions

## ADR-001 - Portfolio statique sans framework front-end lourd

- Statut : Accepté
- Date : 2026-09-01
- Contexte : Le portfolio doit être rapide à charger, facile à héberger sur tout serveur web (ex: Hostinger public_html) et d'une maintenance minimale sans étape de build complexe.
- Décision : Utiliser uniquement HTML, CSS natif et JavaScript vanille dans `index.html` sans framework JS (React, Vue, etc.) ni outil de bundling.
- Conséquences : Performance maximale, zéro dépendance npm de runtime, chargement immédiat. Requis d'écrire le code UI et les interactions directement en JS natif.
- Fichiers concernés : `index.html`

## ADR-002 - Séparation du contenu et de la structure via `projects.json`

- Statut : Accepté
- Date : 2026-09-01
- Contexte : La liste des projets et leurs métadonnées doivent pouvoir être mises à jour sans modifier la structure HTML ou la logique de rendu.
- Décision : Isoler toutes les données des réalisations dans un fichier JSON externe (`projects.json`) chargé dynamiquement par `index.html`.
- Conséquences : Le contenu est structuré et maintenable. Les modifications de données ne risquent pas de casser la mise en page HTML. Nécessite une validation systématique de la validité du fichier JSON.
- Fichiers concernés : `projects.json`, `index.html`

## ADR-003 - Système de documentation autonome pour agents IA

- Statut : Accepté
- Date : 2026-09-01
- Contexte : Plusieurs agents IA ou contributeurs peuvent intervenir sur le dépôt. Sans cadre clair, le projet risque la dérive de structure et les réécritures inutiles.
- Décision : Établir une charte minimale dans `AGENTS.md` appuyée par un triptyque dans `dev/docs/` (`JOURNALDEBORD.md` pour l'historique, `SPECS.md` pour les règles préventives, `DECISIONS.md` pour l'architecture).
- Conséquences : Garantie de continuité entre les sessions d'agents, traçabilité des choix techniques, prévention de la dégradation du code.
- Fichiers concernés : `AGENTS.md`, `dev/docs/JOURNALDEBORD.md`, `dev/docs/SPECS.md`, `dev/docs/DECISIONS.md`
