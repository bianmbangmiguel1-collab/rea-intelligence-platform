# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Langue de travail : français
- Objectif : concevoir une plateforme indépendante autour de REA ; poursuivre la documentation et les revues de conception avant toute implémentation.

## Statut actuel

- Phase active : **phase 3 — conception sécurité/exploitation documentaire ; périmètre de pilote et rôles approuvés, autres décisions et validation globale en attente**.
- Phase 1 — audit technique REA : **incomplète** ; révision immuable approuvée, audit documentaire non effectué.
- Phase 2 — conception fonctionnelle : revue documentaire préparatoire effectuée ; approbation formelle globale en attente.
- Phase 4 — porte avant réalisation : **non franchie**.
- Code applicatif, installation d'outils, exécution REA, analyse d'une cible réelle et déploiement : **non effectués** ; restent interdits avant satisfaction des portes applicables.
- Les comportements, commandes, capacités, formats, transports, sessions, preuves et prérequis REA restent non vérifiés jusqu'à audit sourcé de la révision approuvée.
- Les avis documentaires ne valent pas audit technique, recette, preuve de sécurité ou autorisation de déploiement.

## Cadrage approuvé ou restant à confirmer

1. **Approuvé le 2026-11-10 :** pilote personnel mono-propriétaire, limites, exclusions, modèle de rôles et d'approbation ; détail dans `docs/03-governance/pilot-scope-decisions.md`.
2. **Approuvé le 2026-11-10 :** révision REA à auditer : `morluto/rea` commit `3345019fe1341db40c26af3463e136fcb7c7d11e`. Audit et revue de licence non effectués.
3. Architecture hybride visée : web/cloud, backend central, agents locaux et runners adaptés — proposition.
4. Windows prioritaire pour l'agent initial, sous réserve de compatibilité auditée.
5. OpenRouter envisagé, sans décision technique ni autorisation de transfert de données ; mode sans IA requis dans la conception.
6. Technologies de stockage, file, identité, transport et hébergement demeurent à décider et vérifier.
7. Les titulaires individuels des rôles et l'auditeur REA restent à désigner.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage initial et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible d'une révision précise de REA | Référence approuvée ; audit incomplet |
| 2 | Spécifications fonctionnelles et conception logique | Revue documentaire effectuée ; validation formelle en attente |
| 3 | Conception détaillée sécurité, agent et exploitation | Périmètre pilote/rôles approuvés ; autres décisions ouvertes |
| 4 | Revue de conception et décision de démarrer la réalisation | Bloquée ; prérequis non clos et validation explicite absente |
| 5+ | Développement, tests et déploiement | Pas commencé / bloqué par les portes du projet |

Les critères applicables sont dans `docs/06-roadmap/roadmap.md`. Les avis et décisions sont consignés dans `docs/03-governance/phase-review.md`.

## Questions prioritaires ouvertes

- Qui sont les titulaires individuels des rôles d'approbateur et d'auditeur REA ?
- Quels constats, interfaces, transports, capacités, états, sessions, preuves, erreurs, dépendances et licences sont documentés dans le commit approuvé ?
- Quelles capacités et conditions sont compatibles avec Windows et Linux ?
- Quel fournisseur d'identité, hébergement, région, base, file et stockage seront retenus ?
- Quel modèle d'enrôlement, de transport, d'isolation, de mise à jour et de révocation agent est acceptable ?
- Quelles données pourront être transmises à un fournisseur IA, avec quel consentement et quelle rétention ?
- Quels seuils de performance, disponibilité, budget, support et conservation sont souhaités ?
- Quels risques résiduels peuvent être acceptés, par qui et avec quelle justification ?

## Prochaine action

Désigner l'auditeur et consigner les titulaires des rôles, puis réaliser l'audit documentaire en lecture seule du commit REA approuvé et produire les constats sourcés. Poursuivre les arbitrages sécurité/exploitation ; ne pas franchir la porte de réalisation sans clôture des prérequis et décision explicite.

## Journal de continuité

- Le dépôt contient les spécifications fonctionnelles, l'architecture logique, l'analyse de menace, le modèle conceptuel, les contrats API proposés, les ADR et la roadmap.
- La documentation comprend le plan d'audit REA, le registre de risques, la gouvernance données/IA, la traçabilité, l'agenda phase 3, la conception sécurité/exploitation et les revues préparatoires.
- Le 2026-11-10, le propriétaire a approuvé le périmètre minimal du pilote, le modèle de rôles et d'approbation ainsi que le SHA REA à auditer ; les documents de décision, d'audit et de revue ont été actualisés.
- Aucun audit technique ou test, installation, exécution REA, analyse sur cible, développement ou déploiement n'a été effectué.
