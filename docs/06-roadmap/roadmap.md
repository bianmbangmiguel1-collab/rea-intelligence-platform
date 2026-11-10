# Feuille de route

Les phases définissent des portes de décision. La progression documentaire ne signifie pas qu'un audit ou un test a été exécuté. Aucun passage à la réalisation sans validation explicite.

## Phase 0 — Cadrage initial — terminée

Vision, objectif d'intégrer REA, règle de non-réécriture et dépôt documentaire initial.

## Phase 1 — Audit de REA — incomplète / dépendance ouverte

Vérifier sur une révision déterminée du dépôt officiel les interfaces réellement exposées, leurs schémas, transports, capacités, sessions, preuves, erreurs, annulation, dépendances, licences et compatibilité déclarée. Distinguer documentation consultée et comportement effectivement vérifié ; cette dernière vérification nécessite une autorisation distincte et ne doit pas viser une cible réelle sans autorisation.

**Sortie :** rapport sourcé, révision auditée, matrice des capacités et questions restantes. Les éléments REA des documents antérieurs restent des hypothèses jusqu'à cette sortie.

Voir le [plan d'audit documentaire](../03-governance/rea-audit-plan.md). L'audit n'est pas marqué terminé.

## Phase 2 — Spécifications fonctionnelles et conception logique — active

Travaux en cours :

- exigences, parcours utilisateur, périmètre et exclusions ;
- composants et frontières de confiance ;
- modèle de données conceptuel et contrats de plateforme proposés ;
- exigences de sécurité, gouvernance des données/IA et registre des risques ;
- traçabilité, critères d'acceptation et questions ouvertes.

**Sortie :** documents cohérents, statuts et risques explicites, questions de décision identifiées et validation de l'utilisateur. Les détails d'intégration REA restent conditionnels à la phase 1.

Références : [charte](../00-project-charter.md), [index documentaire](../README.md), [traçabilité et validation](../03-governance/traceability-and-validation.md).

## Phase 3 — Conception sécurité et exploitation — conception initiale rédigée, non validée

Une proposition de conception couvre l'identité et le cycle de vie des agents, le transport et l'isolation, les secrets, le cycle de vie des données, la gouvernance IA, les journaux, les incidents, l'exploitation et les vérifications futures. Voir la [conception sécurité/exploitation](../03-governance/security-operations-design.md) et l'[agenda phase 3](../03-governance/phase-3-design-agenda.md).

Les décisions restent ouvertes ; une liste rédigée ne vaut ni décision acceptée ni conception validée.

**Sortie :** décisions et propriétaires explicités, risques résiduels traités ou acceptés formellement, conception revue et validation utilisateur.

## Phase 4 — Revue et porte avant réalisation — non franchie

Clôturer l'audit et la conception, vérifier coûts/licences/périmètre pilote, préciser les critères de recette et obtenir la demande explicite de démarrer le développement. La demande de codage ne remplace pas l'audit ni la validation de conception.

## Phase 5+ — Réalisation — bloquée

Prototype contrôlé, agent, backend, interface, tests et déploiement ne sont planifiés qu'après la phase 4 et son autorisation explicite. Aucun code applicatif ou test sur cible réelle avant la satisfaction de ces conditions.

## Critères transversaux

- faits REA cités avec révision et source ;
- exigences, choix acceptés, propositions, hypothèses et faits vérifiés distingués ;
- autorisations et limites représentées dans les flux ;
- erreurs, limites et résultats partiels conservés ;
- transferts externes et données IA maîtrisés ;
- risques résiduels et dépendances visibles ;
- livrable relu et passage explicitement validé.
