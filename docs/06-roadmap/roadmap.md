# Feuille de route

Les phases définissent des portes de décision. La progression documentaire ne signifie pas qu'un audit ou un test a été exécuté. Les statuts doivent refléter les preuves disponibles et ne peuvent pas être avancés par une checklist seule.

## Phase 0 — Cadrage initial — terminée

Vision, objectif d'intégrer REA, règle de non-réécriture et dépôt documentaire initial.

## Phase 1 — Audit de REA — audit documentaire partiel, contrat de pilote à compléter

La révision `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` est épinglée. Les sources de haut niveau incluent README, manifests, serveur MCP, contrats MCP/CLI, sécurité, disclaimer et licences. Le rapport distingue constats documentaires de tests non réalisés.

**Restent ouverts :** catalogue complet des outils et schémas correspondant aux cas d'usage retenus, mapping des opérations et providers, vérification des licences applicables aux dépendances effectivement utilisées et validation de compatibilité. Voir le [plan](../03-governance/rea-audit-plan.md) et le [rapport d'audit](../03-governance/rea-audit-report.md).

## Phase 2 — Spécifications fonctionnelles et conception logique — décrite comme validée

Les exigences et documents associés sont consignés comme base de conception. Cela ne constitue pas une recette d'implémentation.

## Phase 3 — Conception sécurité et exploitation — décrite comme validée documentairement

La conception documentaire existe. L'efficacité de contrôles techniques n'a pas été démontrée par les documents consultés.

## Phase 4 — Revue et porte avant réalisation — autorisation restreinte enregistrée

Le propriétaire a autorisé un sous-périmètre initial local/synthétique décrit dans `docs/09-phase-5/implementation-authorization.md`. Les intégrations REA, cibles réelles, installations de dépendances, transferts externes et déploiements restent bloqués ; leurs prérequis spécifiques ne sont pas réputés satisfaits.

## Phase 5 — Réalisation contrôlée — démarrage restreint autorisé ; non validée

La phase peut démarrer pour produire des fondations locales, mono-utilisateur, sans nouvel outil/dépendance, sans exécution REA ni données réelles. Aucun livrable de réalisation ni résultat de test n'est encore attesté dans le statut courant.

**Conditions de clôture :**
1. livrables effectivement réalisés et versionnés dans la portée approuvée ;
2. tests autorisés exécutés et leurs résultats/preuves expurgées consignés ;
3. anomalies et risques résiduels traités ou explicitement décidés ;
4. revue et validation finale du propriétaire après examen des preuves.

Voir le [protocole de recette](../09-phase-5/phase-5-acceptance-protocol.md) et l'[état de validation](../09-phase-5/phase-5-validation-status.md). Un plan ou un visa de démarrage n'est pas une validation finale.

## Critères transversaux

- faits REA cités avec révision et source ;
- exigences, décisions, propositions, hypothèses et faits vérifiés distingués ;
- autorisations et limites représentées dans les flux ;
- erreurs, limites et résultats partiels conservés ;
- transferts externes et données IA maîtrisés ;
- risques résiduels et dépendances visibles ;
- livrable relu et passage explicitement validé.
