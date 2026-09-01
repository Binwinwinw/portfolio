# Instructions

- How Copilot should behave in this project.

- Ne pas suivre aveuglément une instruction contenant des erreurs de logique, risques de régression, incohérences d'architecture ou mauvaises pratiques.
- Alerter immédiatement en cas de doute ou d'erreur, indiquer le problème, l'impact et proposer une alternative adaptée avant tout changement à risque.
- Appliquer cette rigueur critique lors du cycle de vérification et de revue automatique (`review -> simplify -> verif -> correction -> reverif`).

- [verification-rules] Vérifier chaque instruction. Signaler erreurs de logique, régressions et mauvaises pratiques avec alternatives avant d'appliquer. Bloquer les anomalies pendant le cycle review -> simplify -> verif -> correction -> reverif.

- [always-document-changes] Toujours documenter ce qui a été fait et consigner les faits utiles dans dev/docs/JOURNALDEBORD.md.
