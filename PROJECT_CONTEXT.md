# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Langue de travail : français
- Objectif : concevoir une plateforme indépendante autour de REA ; poursuivre la documentation et les revues de conception avant toute implémentation.

## Statut actuel

- Phase active : **phase 2 — spécifications fonctionnelles et conception logique ; revue documentaire préparatoire effectuée**.
- Phase 1 — audit technique REA : **incomplète** ; aucune révision de référence ni rapport d'audit n'est consigné.
- Phase 3 — sécurité et exploitation : **conception et revue documentaire préliminaires effectuées ; décisions et validation du propriétaire ouvertes**.
- Phase 4 — porte avant réalisation : **non franchie**.
- Code applicatif, installation d'outils, exécution de REA, analyse d'une cible réelle et déploiement : **non effectués**. Ils ne commencent pas tant que les portes du dépôt ne sont pas satisfaites.
- Les commandes, capacités, formats, transports, sessions, preuves et prérequis REA issus de notes antérieures restent des **hypothèses** jusqu'à audit d'une révision précise.
- Les avis des revues sont documentaires ; ils ne valent pas approbation du propriétaire, audit technique, recette ni preuve de sécurité.

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
| 2 | Spécifications fonctionnelles et conception logique | Revue documentaire effectuée ; validation du propriétaire et arbitrages en attente |
| 3 | Conception détaillée sécurité, agent et exploitation | Conception/revue préliminaires effectuées ; décisions et validation ouvertes |
| 4 | Revue de conception et décision de démarrer la réalisation | Bloquée ; prérequis non clos et validation explicite absente |
| 5+ | Développement, tests et déploiement | Pas commencé / bloqué par les portes du projet |

Les critères applicables sont dans [`docs/06-roadmap/roadmap.md`](docs/06-roadmap/roadmap.md). Les avis de revue sont consignés dans [`docs/03-governance/phase-review.md`](docs/03-governance/phase-review.md). La demande de démarrage du codage ne clôt pas l'audit REA ni les validations fonctionnelles et sécurité exigées par les règles du dépôt.

## Questions prioritaires ouvertes

- Quel pilote minimal, profils d'utilisateurs, cas d'usage, cibles et opérations autorisées/interdites ?
- Quelle révision immuable de `morluto/rea` sera auditée, et quelles étapes nécessitent une autorisation séparée ?
- Quels outils/interfaces, transports, schémas, capacités, états, sessions, preuves et erreurs sont réellement documentés dans cette révision ?
- Quelles capacités et conditions sont compatibles avec Windows et Linux ?
- Quel fournisseur d'identité, hébergement, région, base, file et stockage seront retenus ?
- Quel modèle d'enrôlement, de transport, d'isolation, de mise à jour et de révocation agent est acceptable ?
- Quelles données pourront être transmises à un fournisseur IA, avec quel consentement, quelle rétention et quelles conditions ?
- Quels seuils de performance, disponibilité, budget, support et durée de conservation sont souhaités ?
- Quels risques résiduels peuvent être acceptés, par qui et avec quelle justification ?

## Prochaine action

Le propriétaire examine les [revues fonctionnelle, sécurité et de phase](docs/03-governance/phase-review.md) et consigne ses décisions. Ensuite, choisir une révision immuable de REA et produire un audit sourcé ; préciser les décisions de phase 3 et les critères de vérification. La réalisation demeure bloquée jusqu'à satisfaction de la porte de phase 4 et des règles `AGENTS.md`.

## Journal de continuité

- Le dépôt contient une première spécification fonctionnelle, une architecture logique, une analyse de menace initiale, un modèle conceptuel, des contrats API proposés, une roadmap et des ADR.
- La documentation comprend une charte, un index documentaire, un plan d'audit REA, un registre initial des risques, une gouvernance données/IA, un cadre de traçabilité/validation, un agenda et une conception sécurité/exploitation préliminaire.
- Cette tâche ajoute les revues documentaires fonctionnelle et sécurité ainsi qu'un relevé explicite de l'état des portes.
- Aucun audit technique de REA, test, installation, analyse sur cible, développement ou déploiement n'a été effectué.
