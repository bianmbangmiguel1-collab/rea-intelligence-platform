# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Langue de travail : français
- Objectif : concevoir une plateforme indépendante autour de REA ; commencer dès maintenant par la documentation et les décisions, pas par l'implémentation.

## Statut actuel

- Phase active : **phase 2 — spécifications fonctionnelles et conception logique**.
- Phase 1 — audit technique REA : **incomplète** ; aucune révision de référence ni rapport d'audit n'est consigné.
- Phase 3 — sécurité et exploitation : **à détailler** ; l'agenda documentaire est ouvert.
- Code applicatif, installation d'outils, exécution de REA, analyse d'une cible réelle et déploiement : **non autorisés dans la phase actuelle et non effectués**.
- Les commandes, capacités, formats, transports, sessions, preuves et prérequis REA issus de notes antérieures restent des **hypothèses** jusqu'à audit d'une révision précise.
- Les documents préparés sont des propositions de conception ; ils ne valent pas validation utilisateur ni clôture de phase.

## Cadrage en cours — à confirmer

1. Intégrer le moteur officiel REA ; ne pas le réécrire et ne pas modifier son dépôt.
2. Architecture hybride visée : web/cloud, backend central, agents locaux et runners adaptés.
3. Windows prioritaire pour l'agent initial, sous réserve de compatibilité auditée.
4. Usage initial personnel, extensible ; pas de portée commerciale multi-utilisateur présumée.
5. OpenRouter envisagé, sans décision technique ni autorisation de transfert de données ; mode sans IA requis dans la conception.
6. Orientations d'architecture enregistrées dans les ADR à confirmer selon leur statut et l'approbation explicite.

Les technologies de stockage, file, identité, transport et hébergement demeurent proposées jusqu'à décision et vérification.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage initial et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible d'une révision précise de REA | Incomplet / dépendance ouverte |
| 2 | Spécifications fonctionnelles et conception logique | Active ; documents enrichis, validation utilisateur attendue |
| 3 | Conception détaillée sécurité, agent et exploitation | À faire ; agenda établi |
| 4 | Revue de conception et décision de démarrer la réalisation | Bloquée jusqu'à clôture des prérequis et validation explicite |
| 5+ | Développement, tests et déploiement | Pas commencé / non autorisé |

Le travail de phase 2 peut avancer sans figer les détails dépendant de REA. Les critères de passage applicables sont dans [`docs/06-roadmap/roadmap.md`](docs/06-roadmap/roadmap.md).

## Questions prioritaires ouvertes

- Quelle révision immuable de `morluto/rea` sera auditée, et avec quelles autorisations pour toute étape ultérieure ?
- Quels outils/interfaces, transports, schémas, capacités, états, sessions, preuves et erreurs sont réellement documentés dans cette révision ?
- Quelles capacités et conditions sont compatibles avec Windows et Linux ?
- Quel fournisseur d'identité, hébergement, région, base, file et stockage seront retenus ?
- Quel modèle d'enrôlement, de transport, de mise à jour et de révocation agent est acceptable ?
- Quelles données pourront être transmises à un fournisseur IA, avec quel consentement, quelle rétention et quelles conditions ?
- Quel périmètre de pilote, budget, politique d'autorisation et durée de conservation sont souhaités ?

## Prochaine action

Faire relire et valider le cadrage et les questions de phase 2 ; puis choisir une révision de référence et compléter l'audit documentaire REA, sans modifier son dépôt. Poursuivre la conception sécurité/exploitation en phase 3. Aucune réalisation avant clôture de l'audit, validation fonctionnelle et sécurité, revue des licences/coûts/périmètre et demande explicite de démarrage.

## Journal de continuité

- Le dépôt contient une première spécification fonctionnelle, une architecture logique, une analyse de menace initiale, un modèle conceptuel, des contrats API proposés, une roadmap et des ADR.
- Cette tâche ajoute une charte, un index documentaire, un plan d'audit REA, un registre initial des risques, une gouvernance des données/IA, un cadre de traçabilité/validation et un agenda de phase 3.
- Aucun audit technique de REA, test, installation, exécution sur cible ou développement n'a été effectué par ce travail.
