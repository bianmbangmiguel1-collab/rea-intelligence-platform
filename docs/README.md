# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Les décisions et statuts doivent rester soutenus par les preuves présentes dans le dépôt ; une intention ou un plan ne vaut pas exécution ni recette.

## État et statut des informations

- **Phase active :** phase 5 — réalisation locale/synthétique autorisée, phase non terminée et non validée.
- **Phase 1 — audit REA :** commit de référence épinglé, audit documentaire partiel ; contrats/outils précis du pilote à inventorier.
- **Phases 2 et 3 :** décrites comme validées au niveau de conception/documentation ; pas une recette technique.
- **Phase 4 :** autorisation limitée à la portée de phase 5 locale/synthétique ; intégration REA, cibles réelles et production restent bloquées.
- **Phase 5 :** autorisation de démarrage limitée et plan de travail validé par le propriétaire le 2026-11-12 ; aucun livrable applicatif ou résultat de test n'est encore attesté.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Spécification fonctionnelle | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Base de conception, recette non attestée |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition, intégration REA conditionnelle |
| Sécurité | [Conception sécurité](02-architecture/security-design.md) | Analyse documentaire, contrôles techniques non testés |
| Porte avant réalisation | [Porte de phase 4](03-governance/phase-4-gate-review.md) | Visa limité ; autres extensions bloquées |
| Audit REA | [Plan](03-governance/rea-audit-plan.md) · [Rapport](03-governance/rea-audit-report.md) | Sources haut niveau citées ; contrats spécifiques au pilote incomplets |
| Autorisation phase 5 | [Formulaire](09-phase-5/implementation-authorization.md) | Approuvée uniquement pour fondations locales/synthétiques |
| Plan de travail et backlog phase 5 | [Plan de travail](09-phase-5/phase-5-work-plan.md) | Validé comme plan par le propriétaire ; tâches ouvertes |
| Plan d'implémentation | [Plan](09-phase-5/phase-5-implementation-plan.md) | Plan documentaire, pas une réalisation |
| Recette phase 5 | [Protocole](09-phase-5/phase-5-acceptance-protocol.md) | Cas et preuves proposés, aucun test exécuté |
| Validation phase 5 | [État](09-phase-5/phase-5-validation-status.md) | Non terminée/non validée |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Démarrage restreint, clôture soumise aux preuves |

## Règles de lecture

1. **Exigence** : besoin à satisfaire, selon le périmètre approuvé.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire.
3. **Proposition** : option non engageante.
4. **Fait vérifié** : affirmation étayée par source, révision et preuve.
5. **Hypothèse** : élément non confirmé, ne constituant pas un contrat.

## Prochaine séquence

1. Suivre le [plan de travail phase 5](09-phase-5/phase-5-work-plan.md), en commençant par les contrats de domaine purs.
2. Tracer les décisions de technologie et les changements sans ajouter de dépendance non approuvée.
3. Exécuter les tests autorisés et consigner résultats, anomalies, limites et preuves.
4. Ne conclure la phase 5 qu'après revue et validation écrite des preuves par le propriétaire.
