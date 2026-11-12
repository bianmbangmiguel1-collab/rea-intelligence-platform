# Documentation du projet

Point d'entrée documentaire de REA Intelligence Platform. Les décisions et statuts doivent rester soutenus par les preuves présentes dans le dépôt ; une intention ou un plan ne vaut pas exécution ni recette.

## État et statut des informations

- **Phase active :** phase 5 — préparation documentaire, réalisation non commencée et non validée.
- **Phase 1 — audit REA :** commit de référence épinglé, audit documentaire partiel ; contrats/outils précis du pilote à inventorier.
- **Phases 2 et 3 :** décrites comme validées au niveau de conception/documentation ; pas une recette technique.
- **Phase 4 :** validation consignée dans son document ; les éléments d'audit cochés doivent être rapprochés des preuves réellement présentes et des consignes actives.
- **Phase 5 :** plan, autorisation vierge et protocole de recette disponibles ; aucun livrable applicatif ou résultat de test n'est attesté.
- **Règles applicables :** `AGENTS.md` autorise actuellement la documentation seulement et interdit code applicatif, installation, exécution REA, analyse sur cible réelle et déploiement.

Lire aussi [`PROJECT_CONTEXT.md`](../PROJECT_CONTEXT.md) et [`AGENTS.md`](../AGENTS.md).

## Références principales

| Sujet | Document | Statut |
| --- | --- | --- |
| Spécification fonctionnelle | [Spécification fonctionnelle](01-specifications/functional-specification.md) | Base de conception, recette non attestée |
| Architecture logique | [Architecture détaillée](02-architecture/detailed-architecture.md) | Proposition, intégration REA conditionnelle |
| Sécurité | [Conception sécurité](02-architecture/security-design.md) | Analyse documentaire, contrôles techniques non testés |
| Porte avant réalisation | [Porte de phase 4](03-governance/phase-4-gate-review.md) | Décision documentée ; preuves et consignes à réconcilier |
| Plan d'audit REA | [Plan](03-governance/rea-audit-plan.md) · [Rapport](03-governance/rea-audit-report.md) | Sources haut niveau citées ; contrats spécifiques au pilote incomplets |
| Autorisation phase 5 | [Formulaire d'autorisation](09-phase-5/implementation-authorization.md) | Vierge, aucune portée approuvée par ce formulaire |
| Plan phase 5 | [Plan d'implémentation](09-phase-5/phase-5-implementation-plan.md) | Plan documentaire, pas une réalisation |
| Recette phase 5 | [Protocole de recette](09-phase-5/phase-5-acceptance-protocol.md) | Cas et preuves proposés, aucun test exécuté |
| Validation phase 5 | [État de validation](09-phase-5/phase-5-validation-status.md) | Bloquée / non réalisée / non validée |
| Phases et portes | [Roadmap](06-roadmap/roadmap.md) | Audit à compléter, phase 5 bloquée |

## Règles de lecture

1. **Exigence** : besoin à satisfaire, selon le périmètre approuvé.
2. **Choix accepté** : décision explicitement approuvée par le propriétaire.
3. **Proposition** : option non engageante.
4. **Fait vérifié** : affirmation étayée par source, révision et preuve.
5. **Hypothèse** : élément non confirmé, ne constituant pas un contrat.

## Prochaine séquence

1. Compléter l'inventaire des opérations REA nécessaires aux besoins retenus et leurs preuves sourcées.
2. Réconcilier l'autorisation de phase 4 avec les règles actives de `AGENTS.md`.
3. Faire approuver un périmètre précis avec exclusions dans le formulaire d'autorisation.
4. Reprendre la phase 5 après levée des blocages et consigner les résultats de recette avant toute clôture.
