# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Tous les documents de conception sont des propositions tant qu'ils ne sont pas explicitement validés ; toute affirmation sur REA reste non vérifiée jusqu'à l'audit d'une révision précise.

## État et statut des informations

- **Phase active :** phase 2, spécifications fonctionnelles et conception logique.
- **Phase 1 — audit REA :** incomplète ; aucune révision auditée n'est enregistrée ici.
- **Réalisation :** non autorisée ; aucun code applicatif, outil, essai sur cible réelle ni déploiement n'est entrepris.
- **Validation :** les documents ci-dessous ne valent pas validation utilisateur ni clôture d'une phase.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et les règles de continuité [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Vision, périmètre et limites | [Charte du projet](00-project-charter.md) | Proposition de cadrage |
| Exigences et parcours produit | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Proposition à valider |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition ; intégration REA conditionnelle |
| Sécurité | [Conception sécurité](02-architecture/security-design.md) | Analyse initiale, à compléter en phase 3 |
| Données et IA | [Gouvernance des données et de l'IA](03-governance/data-ai-governance.md) | Politique proposée, décisions ouvertes |
| Risques | [Registre des risques](03-governance/risk-register.md) | Initial, sans cotation validée |
| Audit du moteur | [Plan d'audit REA](03-governance/rea-audit-plan.md) | Protocole à exécuter ultérieurement et hors de cette tâche |
| Traçabilité | [Traçabilité et validation](03-governance/traceability-and-validation.md) | Cadre de conception ; aucun test exécuté |
| Conception sécurité/exploitation | [Agenda phase 3](03-governance/phase-3-design-agenda.md) | Travail restant |
| Modèle conceptuel | [Modèle de données](04-data-model/data-model.md) | Proposition, sans DDL |
| Contrats de plateforme | [Contrats API](05-api-contracts/api-contracts.md) | Propositions, non implémentables en l'état |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Phase 2 active ; phases suivantes bloquées par leurs portes |
| Décisions | [Index des ADR](07-decisions/README.md) | Orientations à confirmer selon leur statut |
| Vue générale | [Cahier de conception](technical-design.md) | Synthèse conceptuelle |

## Règles de lecture

1. **Exigence** : besoin que la plateforme devra satisfaire, sous réserve de validation du périmètre.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire du projet ; une orientation documentaire ne suffit pas à l'établir.
3. **Proposition** : option de conception à discuter, non engageante.
4. **Fait vérifié** : affirmation étayée par une source et une révision identifiées. Aucun contrat REA n'est encore classé ainsi.
5. **Hypothèse** : affirmation à vérifier, notamment tout exemple de commande, capacité, format, transport ou comportement REA issu de notes antérieures.

## Prochaine séquence documentaire

1. Faire valider le périmètre et les arbitrages ouverts de phase 2.
2. Définir une révision de référence pour l'audit REA et compléter son rapport sans modifier le dépôt externe.
3. Compléter la conception sécurité et exploitation de phase 3.
4. Effectuer une revue de conception et demander une décision explicite avant toute éventuelle réalisation.
