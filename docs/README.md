# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Tous les documents de conception sont des propositions tant qu'ils ne sont pas explicitement validés ; toute affirmation sur REA reste non vérifiée jusqu'à un audit d'une révision déterminée.

## État et statut des informations

- **Phase active :** phase 5, réalisation contrôlée, après validation documentaire de la phase 4.
- **Phase 1 — audit REA :** terminé au niveau documentaire pour la révision de référence `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`.
- **Phase 2 — spécifications fonctionnelles et conception logique :** validée par le propriétaire.
- **Phase 3 — sécurité/exploitation :** validée au niveau documentaire.
- **Phase 4 — porte avant réalisation :** validée ; la revue finale est clôturée.
- **Réalisation :** autorisée sous périmètre documenté ; phase 5+ ouverte.
- **Aucune implémentation ou exécution REA** n'est positivement affirmée au-delà du périmètre autorisé par la phase 5.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et les règles de continuité [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Vision, périmètre et limites | [Charte du projet](00-project-charter.md) | Proposition de cadrage |
| Exigences et parcours produit | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Validée comme base fonctionnelle |
| Revue fonctionnelle | [Revue documentaire fonctionnelle](03-governance/functional-design-review.md) | Avis favorable sous réserves ; pas une recette |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition ; intégration REA conditionnelle |
| Sécurité | [Conception sécurité](02-architecture/security-design.md) | Analyse initiale, validée en matière de conception |
| Sécurité/exploitation détaillées | [Conception phase 3](03-governance/security-operations-design.md) | Validée au niveau documentaire |
| Brief de décision de phase 3 | [Brief de décision](03-governance/phase-3-decision-brief.md) | Validé comme support de décision |
| Revue sécurité | [Revue documentaire sécurité](03-governance/security-design-review.md) | Couverture revue ; aucun contrôle technique testé |
| Porte avant réalisation | [Porte de phase 4](03-governance/phase-4-gate-review.md) | Validée ; phase 5 ouverte |
| Revue des portes | [Revue de phase](03-governance/phase-review.md) | Phase 4 validée |
| Décisions du propriétaire | [Registre des décisions](03-governance/owner-decision-record.md) | À tenir à jour selon les évolutions de phase 5 |
| Arborescence cible | [Structure proposée](08-project-structure/README.md) | Documentation uniquement ; aucun squelette applicatif créé |
| Données et IA | [Gouvernance des données et de l'IA](03-governance/data-ai-governance.md) | Politique proposée, décisions ouvertes |
| Risques | [Registre des risques](03-governance/risk-register.md) | Initial, sans cotation validée |
| Audit du moteur | [Plan d'audit REA](03-governance/rea-audit-plan.md) | Protocole ; audit référencé sur la révision de référence |
| Rapport d'audit | [Rapport d'audit REA](03-governance/rea-audit-report.md) | Document de référence de la révision auditée |
| Traçabilité | [Traçabilité et validation](03-governance/traceability-and-validation.md) | Cadre de conception ; aucun test exécuté |
| Travail phase 3 | [Agenda phase 3](03-governance/phase-3-design-agenda.md) | Validé comme préparation de conception |
| Modèle conceptuel | [Modèle de données](04-data-model/data-model.md) | Proposition, sans DDL |
| Contrats de plateforme | [Contrats API](05-api-contracts/api-contracts.md) | Propositions, non implémentables en l'état |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Audit ouvert ; réalisation bloquée jusqu'à validation de phase 4 |
| Décisions | [Index des ADR](07-decisions/README.md) | Orientations à confirmer selon leur statut |
| Vue générale | [Cahier de conception](technical-design.md) | Synthèse conceptuelle |

## Règles de lecture

1. **Exigence** : besoin que la plateforme devra satisfaire, sous réserve de validation du périmètre.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire du projet ; une orientation documentaire ne suffit pas à l'établir.
3. **Proposition** : option de conception à discuter, non engageante.
4. **Fait vérifié** : preuve étayée par source et révision identifiées. La révision de référence REA est désormais identifiée.
5. **Hypothèse** : élément non confirmé ; elle ne doit pas servir de garantie ou de contrat.

## Prochaine séquence

1. La phase 5 démarre sous le périmètre documenté et les contrôles de conception validés.
2. Les évolutions de périmètre, de sécurité et de dépendance doivent être tracées à la révision de référence et au registre des décisions.
3. Toute exécution REA ou réalisation associée doit rester alignée sur la révision `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` et les critères de recette définis.
4. En cas de nouvelle dépendance, de risque substantiel ou de changement de périmètre, la phase 4 doit être revue à nouveau.
