# Feuille de route

Les phases définissent des portes de décision. La progression documentaire ne signifie pas qu'un audit ou un test a été exécuté. Aucun passage à la réalisation sans validation explicite.

## Phase 0 — Cadrage initial — terminée

Vision, objectif d'intégrer REA, règle de non-réécriture et dépôt documentaire initial.

## Phase 1 — Audit de REA — incomplète / dépendance ouverte

Vérifier sur une révision déterminée du dépôt officiel les interfaces réellement exposées, leurs schémas, transports, capacités, sessions, preuves, erreurs, annulation, dépendances, licences et compatibilité déclarée. Distinguer documentation consultée et comportement effectivement vérifié ; cette dernière vérification nécessite une autorisation distincte et ne doit pas viser une cible réelle sans autorisation.

**Sortie :** rapport sourcé, révision auditée, matrice des capacités et questions restantes. Les éléments REA des documents antérieurs restent des hypothèses jusqu'à cette sortie.

Voir le [plan d'audit documentaire](../03-governance/rea-audit-plan.md). L'audit n'est pas marqué terminé.

## Phase 2 — Spécifications fonctionnelles et conception logique — revue documentaire effectuée, validation propriétaire en attente

Les exigences et parcours, l'architecture logique, le modèle conceptuel, les contrats API proposés, la gouvernance données/IA et les risques ont fait l'objet d'une revue de cohérence documentaire. Voir la [revue fonctionnelle](../03-governance/functional-design-review.md) et la [revue des portes](../03-governance/phase-review.md).

**Résultat de revue :** base conceptuelle cohérente sous réserves, mais pilote, priorités, approbations, seuils non fonctionnels et dépendances REA restent à arbitrer. Aucun test/recette n'a été effectué. La phase n'est pas déclarée validée ou terminée.

**Sortie requise :** décisions consignées, critères d'acceptation par exigence, dépendances REA sourcées ou explicitement ouvertes et validation du propriétaire.

## Phase 3 — Conception sécurité et exploitation — revue documentaire effectuée, validation propriétaire en attente

Une proposition couvre l'identité et le cycle de vie des agents, le transport et l'isolation, les secrets, le cycle de vie des données, la gouvernance IA, les journaux, les incidents, l'exploitation et les vérifications futures. Voir la [conception sécurité/exploitation](../03-governance/security-operations-design.md), l'[agenda phase 3](../03-governance/phase-3-design-agenda.md) et la [revue de sécurité](../03-governance/security-design-review.md).

**Résultat de revue :** principaux domaines de risque représentés au niveau conceptuel ; mécanismes, paramètres, responsables et preuve d'efficacité restent ouverts. Aucun contrôle technique n'a été exécuté. La sécurité n'est pas déclarée validée.

**Sortie requise :** arbitrer les décisions, attribuer propriétaires et traitements aux risques, définir des vérifications mesurables et obtenir la validation explicite du propriétaire.

## Phase 4 — Revue et porte avant réalisation — non franchie

Clôturer l'audit et les conceptions, vérifier coûts/licences/périmètre pilote, définir les critères de recette, obtenir les approbations fonctionnelle et sécurité du propriétaire et une demande explicite de démarrer le développement. La demande de codage ne remplace pas ces prérequis.

## Phase 5+ — Réalisation — bloquée

Prototype contrôlé, agent, backend, interface, tests et déploiement ne sont possibles qu'après la phase 4 et son autorisation explicite. Aucun code applicatif ou test sur cible réelle avant satisfaction des conditions.

## Critères transversaux

- faits REA cités avec révision et source ;
- exigences, choix acceptés, propositions, hypothèses et faits vérifiés distingués ;
- autorisations et limites représentées dans les flux ;
- erreurs, limites et résultats partiels conservés ;
- transferts externes et données IA maîtrisés ;
- risques résiduels et dépendances visibles ;
- livrable relu et passage explicitement validé.
