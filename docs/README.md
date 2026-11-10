# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Les documents de conception sont des propositions tant qu'ils ne sont pas explicitement validés ; toute affirmation sur REA reste non vérifiée jusqu'à l'audit de la révision identifiée.

## État et statut des informations

- **Phase active :** phase 3, conception sécurité/exploitation documentaire ; périmètre pilote et modèle de rôles approuvés, autres décisions ouvertes.
- **Phase 1 — audit REA :** révision approuvée (`3345019fe1341db40c26af3463e136fcb7c7d11e`) ; audit non effectué.
- **Phase 2 — conception fonctionnelle :** revue documentaire effectuée ; approbation formelle globale en attente.
- **Réalisation :** bloquée ; phase 4 non franchie.
- **Aucune implémentation, recette, installation d'outils ou exécution REA** n'est affirmée par ces documents.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et les règles de continuité [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Vision, périmètre et limites | [Charte du projet](00-project-charter.md) | Cadrage |
| Exigences et parcours produit | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Revue de conception ; approbation globale en attente |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition ; intégration REA conditionnelle |
| Sécurité/exploitation détaillées | [Conception phase 3](03-governance/security-operations-design.md) | Proposition ; décisions à valider |
| Décision de périmètre pilote | [Périmètre et rôles approuvés](03-governance/pilot-scope-decisions.md) | Approuvé le 2026-11-10 ; décision documentaire |
| Revue sécurité | [Revue documentaire sécurité](03-governance/security-design-review.md) | Couverture revue ; aucun contrôle technique testé |
| Revue des portes | [Revue de phase](03-governance/phase-review.md) | Phase 4 non franchie |
| Données et IA | [Gouvernance des données et de l'IA](03-governance/data-ai-governance.md) | Politique proposée, décisions ouvertes |
| Risques | [Registre des risques](03-governance/risk-register.md) | Initial, sans cotation validée |
| Audit du moteur | [Plan d'audit REA](03-governance/rea-audit-plan.md) | SHA approuvé ; audit non effectué |
| Traçabilité | [Traçabilité et validation](03-governance/traceability-and-validation.md) | Cadre de conception ; aucun test exécuté |
| Travail phase 3 | [Agenda phase 3](03-governance/phase-3-design-agenda.md) | Arbitrages restant à traiter |
| Modèle conceptuel | [Modèle de données](04-data-model/data-model.md) | Proposition, sans DDL |
| Contrats de plateforme | [Contrats API](05-api-contracts/api-contracts.md) | Propositions, non implémentables en l'état |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Audit ouvert ; réalisation bloquée |
| Décisions | [Index des ADR](07-decisions/README.md) | Orientations à confirmer selon leur statut |
| Vue générale | [Cahier de conception](technical-design.md) | Synthèse conceptuelle |

## Règles de lecture

1. **Exigence** : besoin que la plateforme devra satisfaire, sous réserve de validation du périmètre.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire du projet ; la décision est consignée dans le document de périmètre.
3. **Proposition** : option de conception à discuter, non engageante.
4. **Fait vérifié** : preuve étayée par source et révision identifiées. Aucun contrat REA n'est encore classé ainsi.
5. **Hypothèse** : élément non confirmé ; elle ne doit pas servir de garantie ou de contrat.

## Prochaine séquence

1. Désigner les titulaires de rôles et l'auditeur REA.
2. Réaliser l'audit documentaire sourcé du commit REA approuvé ; ne pas exécuter REA ni analyser une cible.
3. Traiter les risques, confirmer les décisions sécurité/exploitation et définir les critères de vérification.
4. Effectuer une revue de conception finale et demander une décision explicite avant toute éventuelle réalisation.
