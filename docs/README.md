# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Tous les documents de conception sont des propositions tant qu'ils ne sont pas explicitement validés ; toute affirmation sur REA reste non vérifiée jusqu'à un audit d'une révision déterminée.

## État et statut des informations

- **Phase active :** phase 5, plan de mise en œuvre finalisé ; exécution réelle soumise à validation de recette.
- **Phase 1 — audit REA :** terminé au niveau documentaire pour la révision de référence `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`.
- **Phase 2 — spécifications fonctionnelles et conception logique :** validée par le propriétaire.
- **Phase 3 — sécurité/exploitation :** validée au niveau documentaire.
- **Phase 4 — porte avant réalisation :** validée ; la revue finale est clôturée.
- **Phase 5 — réalisation contrôlée :** plan finalisé ; mise en œuvre réelle non déclarée terminée sans validation de recette.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et les règles de continuité [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Vision, périmètre et limites | [Charte du projet](00-project-charter.md) | Proposition de cadrage |
| Exigences et parcours produit | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Validée comme base fonctionnelle |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition ; intégration REA conditionnelle |
| Sécurité | [Conception sécurité](02-architecture/security-design.md) | Analyse initiale, validée en matière de conception |
| Sécurité/exploitation détaillées | [Conception phase 3](03-governance/security-operations-design.md) | Validée au niveau documentaire |
| Porte avant réalisation | [Porte de phase 4](03-governance/phase-4-gate-review.md) | Validée ; phase 5 ouverte |
| Rapport d'audit REA | [Rapport d'audit REA](03-governance/rea-audit-report.md) | Référence documentée |
| Plan de phase 5 | [Plan d'implémentation phase 5](09-phase-5/phase-5-implementation-plan.md) | Finalisé à titre documentaire |
| Arborescence cible | [Structure proposée](08-project-structure/README.md) | Documentation uniquement ; aucun squelette applicatif créé |
| Traçabilité | [Traçabilité et validation](03-governance/traceability-and-validation.md) | Cadre de conception ; validation de recette en attente |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Phase 5 planifiée et conditionnelle |

## Règles de lecture

1. **Exigence** : besoin que la plateforme devra satisfaire, sous réserve de validation du périmètre.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire du projet.
3. **Proposition** : option de conception à discuter, non engageante.
4. **Fait vérifié** : preuve étayée par source et révision identifiées.
5. **Hypothèse** : élément non confirmé ; elle ne doit pas servir de garantie ou de contrat.

## Prochaine séquence

1. Valider le plan de phase 5 avec le propriétaire.
2. Mettre en œuvre uniquement le périmètre de la phase 5 et les contraintes documentées.
3. Exécuter les tests de recette et les contrôles de sécurité exigés.
4. Réenregistrer la preuve de validation avant de conclure la phase 5.
