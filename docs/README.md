# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Les décisions et statuts doivent rester soutenus par les preuves présentes dans le dépôt ; une intention ou un plan ne vaut pas exécution ni recette.

## État et statut des informations

- **Phase active :** phase 5 — non réalisée et non validée.
- **Phase 1 — audit REA :** un SHA de référence et un rapport documentaire sont présents ; le rapport identifie encore des propriétés techniques à vérifier.
- **Phases 2 et 3 :** décrites comme validées au niveau de conception/documentation.
- **Phase 4 :** décrite comme validée dans le document de porte ; les règles actives de `AGENTS.md` restreignent néanmoins le travail à la documentation.
- **Phase 5 :** plan documentaire seulement ; aucun livrable applicatif ni résultat de test ou de recette n'est attesté.
- **Règles applicables :** `AGENTS.md` interdit actuellement le code applicatif, l'installation d'outils, l'exécution de REA, l'analyse sur cible réelle et le déploiement.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Spécification fonctionnelle | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Base de conception, recette non attestée |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition, intégration REA conditionnelle |
| Sécurité | [Conception sécurité](02-architecture/security-design.md) | Analyse documentaire, contrôles techniques non testés |
| Sécurité/exploitation | [Conception phase 3](03-governance/security-operations-design.md) | Document de conception |
| Porte avant réalisation | [Porte de phase 4](03-governance/phase-4-gate-review.md) | Décision documentée ; prérequis à réconcilier avec les consignes actives |
| Audit REA | [Plan d'audit](03-governance/rea-audit-plan.md) · [Rapport disponible](03-governance/rea-audit-report.md) | SHA épinglé, audit des contrats incomplet selon le rapport |
| Plan phase 5 | [Plan d'implémentation](09-phase-5/phase-5-implementation-plan.md) | Plan documentaire, pas une réalisation |
| État de validation phase 5 | [Constat de validation](09-phase-5/phase-5-validation-status.md) | Non réalisée / non validée, blocages consignés |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Phase 5 bloquée, preuves nécessaires |

## Règles de lecture

1. **Exigence** : besoin à satisfaire, selon le périmètre approuvé.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire.
3. **Proposition** : option non engageante.
4. **Fait vérifié** : affirmation étayée par source, révision et preuve.
5. **Hypothèse** : élément non confirmé, ne constituant pas un contrat.

## Prochaine séquence

1. Réconcilier l'autorisation de phase 4 avec les règles de `AGENTS.md`.
2. Compléter l'audit REA et ses sources détaillées.
3. Reprendre la phase 5 uniquement après levée des blocages applicables.
4. Ne conclure la phase 5 qu'après réalisation et recette prouvées.
