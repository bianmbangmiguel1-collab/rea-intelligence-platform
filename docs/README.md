# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Tous les documents de conception sont des propositions tant qu'ils ne sont pas explicitement validés ; toute affirmation sur REA reste non vérifiée jusqu'à un audit d'une révision déterminée.

## État et statut des informations

- **Phase active :** phase 3, conception sécurité et exploitation, après validation de la phase 2.
- **Phase 1 — audit REA :** incomplète ; aucune révision auditée n'est enregistrée ici.
- **Phase 2 — spécifications fonctionnelles et conception logique :** validée par le propriétaire.
- **Phase 3 — sécurité/exploitation :** conception initiale et revue documentaire effectuées ; validation du propriétaire et décisions ouvertes.
- **Réalisation :** bloquée ; phase 4 non franchie.
- **Aucune implémentation, recette, installation d'outils ou exécution REA** n'est affirmée par ces documents.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et les règles de continuité [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Vision, périmètre et limites | [Charte du projet](00-project-charter.md) | Proposition de cadrage |
| Exigences et parcours produit | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Validée comme base fonctionnelle |
| Revue fonctionnelle | [Revue documentaire fonctionnelle](03-governance/functional-design-review.md) | Avis favorable sous réserves ; pas une recette |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition ; intégration REA conditionnelle |
| Sécurité | [Conception sécurité](02-architecture/security-design.md) | Analyse initiale, à compléter et valider |
| Sécurité/exploitation détaillées | [Conception phase 3](03-governance/security-operations-design.md) | Proposition, décisions à valider |
| Décision de phase 3 | [Brief de décision](03-governance/phase-3-decision-brief.md) | Proposition de travail, à confirmer par le propriétaire |
| Revue sécurité | [Revue documentaire sécurité](03-governance/security-design-review.md) | Couverture revue ; aucun contrôle technique testé |
| Revue des portes | [Revue de phase](03-governance/phase-review.md) | Phase 4 non franchie |
| Décisions du propriétaire | [Registre des décisions](03-governance/owner-decision-record.md) | À compléter par le propriétaire ; aucune décision présumée acceptée |
| Arborescence cible | [Structure proposée](08-project-structure/README.md) | Documentation uniquement ; aucun squelette applicatif créé |
| Données et IA | [Gouvernance des données et de l'IA](03-governance/data-ai-governance.md) | Politique proposée, décisions ouvertes |
| Risques | [Registre des risques](03-governance/risk-register.md) | Initial, sans cotation validée |
| Audit du moteur | [Plan d'audit REA](03-governance/rea-audit-plan.md) | Protocole ; audit non exécuté |
| Traçabilité | [Traçabilité et validation](03-governance/traceability-and-validation.md) | Cadre de conception ; aucun test exécuté |
| Travail phase 3 | [Agenda phase 3](03-governance/phase-3-design-agenda.md) | Travail restant et décisions ouvertes |
| Modèle conceptuel | [Modèle de données](04-data-model/data-model.md) | Proposition, sans DDL |
| Contrats de plateforme | [Contrats API](05-api-contracts/api-contracts.md) | Propositions, non implémentables en l'état |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Audit ouvert ; réalisation bloquée |
| Décisions | [Index des ADR](07-decisions/README.md) | Orientations à confirmer selon leur statut |
| Vue générale | [Cahier de conception](technical-design.md) | Synthèse conceptuelle |

## Règles de lecture

1. **Exigence** : besoin que la plateforme devra satisfaire, sous réserve de validation du périmètre.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire du projet ; une orientation documentaire ne suffit pas à l'établir.
3. **Proposition** : option de conception à discuter, non engageante.
4. **Fait vérifié** : preuve étayée par source et révision identifiées. Aucun contrat REA n'est encore classé ainsi.
5. **Hypothèse** : élément non confirmé ; elle ne doit pas servir de garantie ou de contrat.

## Prochaine séquence

1. Le propriétaire valide les décisions de sécurité et d'exploitation dans le [brief de décision](03-governance/phase-3-decision-brief.md) et dans le [registre des décisions](03-governance/owner-decision-record.md).
2. Choisir une révision immuable de REA et compléter l'audit avec des sources datées ; distinguer examen documentaire et tests exécutés.
3. Traiter les risques, confirmer les décisions sécurité/exploitation et définir les critères de vérification.
4. Effectuer une revue de conception finale et demander une décision explicite avant toute éventuelle réalisation.
