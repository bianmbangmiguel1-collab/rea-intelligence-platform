# Revue de phase — état et décision

**Date de revue documentaire :** 2026-11-10  
**Statut :** avis préparatoire ; aucune phase n'est déclarée terminée par cette revue.

## Résumé de l'état

| Porte | État constaté | Conclusion |
| --- | --- | --- |
| Phase 1 — audit REA | Référence candidate épinglée dans la décision de cadrage ; audit non effectué | Bloquante pour intégration et réalisation |
| Phase 2 — conception fonctionnelle | Documents examinés ; revue documentaire favorable sous réserves | Validation du propriétaire et décisions de pilote en attente |
| Phase 3 — sécurité/exploitation | Conception préliminaire et revue de couverture rédigées ; proposition de périmètre pilote/rôles consignée | Approbation du propriétaire, arbitrages opérationnels et vérifications ultérieures en attente |
| Phase 4 — décision avant réalisation | Non franchie | Pas d'autorisation d'implémenter |
| Phase 5+ — réalisation | Non commencée | Aucun code produit par cette revue |

## Documents examinés

- [`docs/00-project-charter.md`](../00-project-charter.md)
- [`docs/01-specifications/functional-specification.md`](../01-specifications/functional-specification.md)
- [`docs/02-architecture/detailed-architecture.md`](../02-architecture/detailed-architecture.md)
- [`docs/02-architecture/security-design.md`](../02-architecture/security-design.md)
- [`docs/03-governance/security-operations-design.md`](security-operations-design.md)
- [`docs/03-governance/functional-design-review.md`](functional-design-review.md)
- [`docs/03-governance/security-design-review.md`](security-design-review.md)
- [`docs/03-governance/risk-register.md`](risk-register.md)
- [`docs/03-governance/data-ai-governance.md`](data-ai-governance.md)
- [`docs/03-governance/traceability-and-validation.md`](traceability-and-validation.md)
- [`docs/03-governance/rea-audit-plan.md`](rea-audit-plan.md)
- [`docs/03-governance/pilot-scope-decisions.md`](pilot-scope-decisions.md)
- [`docs/04-data-model/data-model.md`](../04-data-model/data-model.md)
- [`docs/05-api-contracts/api-contracts.md`](../05-api-contracts/api-contracts.md)
- [`docs/06-roadmap/roadmap.md`](../06-roadmap/roadmap.md)

## Points à arbitrer par le propriétaire

1. Accepter ou modifier le périmètre personnel proposé, les cas d'usage et les opérations explicitement exclues dans la [décision de cadrage pilote](pilot-scope-decisions.md).
2. Nommer les personnes tenant les rôles de propriétaire plateforme/projet, opérateur, approbateur et auditeur REA ; confirmer la séparation applicable en pilote personnel.
3. Confirmer le commit immuable de REA proposé comme référence d'audit et autoriser séparément l'examen documentaire.
4. Confirmer les cibles, opérations et preuves d'autorisation ; aucune cible réelle n'est autorisée par la proposition.
5. Arbitrer les règles d'approbation, de gestion des états et d'annulation.
6. Choisir hébergement, identité, transport, OS, isolation, stockage et région.
7. Décider classification, transferts IA, consentement, fournisseur, rétention, sauvegarde et suppression.
8. Définir objectifs mesurables, budget, support et risques résiduels acceptables.

Les réponses doivent être consignées comme décisions, propositions ou questions ouvertes. La revue documentaire par l'assistant n'est pas une validation à la place du propriétaire.

## Conditions de passage non satisfaites

- La référence candidate REA est épinglée, mais l'audit n'a pas été effectué et les constats/licences ne sont pas sourcés.
- Le propriétaire n'a pas validé formellement les conceptions fonctionnelle et sécurité, le périmètre pilote et les rôles.
- Les choix de fournisseurs, données, exploitation et risques résiduels ne sont pas tous arbitrés.
- Les critères de recette ne sont pas transformés en vérifications exécutables, et aucun test n'a été effectué.

## Décision

**Phase 2 :** revue documentaire effectuée, validation formelle en attente.  
**Phase 3 :** revue de couverture effectuée ; proposition de périmètre et de rôles consignée, décisions et validation en attente.  
**Phase 4 :** non franchie. La réalisation demeure bloquée.

| Décision / visa | État | Responsable / date |
| --- | --- | --- |
| Revue documentaire préparatoire | Consignée | Assistant / 2026-11-10 |
| Proposition de périmètre pilote et rôles | Consignée, approbation en attente | Assistant / propriétaire du projet |
| Référence candidate REA pour audit | SHA consigné, confirmation en attente | Propriétaire du projet |
| Approbation fonctionnelle | En attente | Propriétaire du projet |
| Approbation sécurité | En attente | Propriétaire du projet |
| Clôture de l'audit REA | En attente | Après examen sourcé de la révision confirmée |
| Autorisation de réalisation | Non accordée | Porte de phase 4 à franchir |
