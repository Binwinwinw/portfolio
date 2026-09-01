# Instructions pour les agents

## Objet du dépôt

- Portfolio statique.
- `index.html` porte l'interface, les styles et le comportement front-end.
- `projects.json` porte les données des projets.

## Fichiers de référence

- Lire `.memory/security.md` avant toute modification.
- Lire `README.md` pour l'utilisation et le déploiement.
- Lire `dev/docs/DECISIONS.md` pour les décisions techniques durables.
- Consulter `dev/docs/REGLES.md` pour les règles de vérification et de revue du dépôt.
- Consulter `dev/docs/JOURNALDEBORD.md` pour l'historique utile des sessions.
- Consulter `dev/docs/SPECS.md` pour les règles issues des erreurs et des corrections passées.

## Données et contenu

- Maintenir `projects.json` comme JSON valide.
- Conserver les champs, types et URLs compatibles avec `index.html`.
- Ne pas présenter de contenu fictif comme réel.

## Interface

- Préserver HTML sémantique, navigation clavier et lisibilité sur mobile.
- Garder le parcours clair pour recruteurs et clients : identité, réalisations, preuves, contact.
- Mener toute analyse ou refonte UI par lots distincts, puis obtenir une priorisation avant l'implémentation.

## Portée et validation

- Limiter chaque intervention aux fichiers requis ; ne pas écraser les changements existants.
- Ne pas ajouter de dépendance ou de pipeline sans besoin démontré.
- Après modification, valider les formats touchés, la syntaxe HTML ou JavaScript concernée, puis l'affichage local si l'interface change.
- Toujours documenter ce qui a été fait (consigner les interventions et faits utiles dans `dev/docs/JOURNALDEBORD.md`).
- Mettre à jour `README.md` quand l'utilisation ou le déploiement évolue.
- Consigner les décisions durables dans `dev/docs/DECISIONS.md`.

## Git et commandes

- Ne pas réécrire l'historique Git ni annuler le travail d'autrui.
- Ne créer ni commit, ni branche, ni publication distante sans demande explicite.
- Préfixer les commandes shell par `rtk`.
