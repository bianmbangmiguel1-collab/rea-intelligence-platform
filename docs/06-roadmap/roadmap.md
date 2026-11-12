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

## Phase 4 — Revue et porte avant réalisation — décision documentée, exigences à réconcilier

Le document de porte consigne une validation. Toutefois, certains critères cochés — notamment l'audit complet et sa matrice — n'étaient pas soutenus par le rapport antérieur. La portée d'implémentation doit aussi être conciliée avec les consignes actives de `AGENTS.md` avant tout code.

## Phase 5 — Réalisation contrôlée — non commencée / non validée

Un plan et un protocole de recette existent ; aucun livrable applicatif ni rapport de test n'est attesté. `AGENTS.md` interdit actuellement l'implémentation, l'installation, l'exécution de REA, l'analyse sur cible réelle et le déploiement.

**Conditions de reprise :**
1. compléter l'audit documentaire des opérations REA nécessaires au pilote ;
2. résoudre la contradiction entre la porte de phase 4 et les règles actives de `AGENTS.md` par une décision appropriée du propriétaire ;
3. remplir le formulaire d'autorisation avec un périmètre précis et ses exclusions ;
4. produire les livrables contrôlés et exécuter uniquement des tests approuvés ;
5. consigner preuves, résultats, anomalies et approbation de recette du propriétaire.

La phase 5 ne peut être déclarée terminée par la finalisation d'un plan ou d'une checklist seulement. Voir le [protocole de recette](../09-phase-5/phase-5-acceptance-protocol.md) et l'[état de validation](../09-phase-5/phase-5-validation-status.md).

## Critères transversaux

- faits REA cités avec révision et source ;
- exigences, décisions, propositions, hypothèses et faits vérifiés distingués ;
- autorisations et limites représentées dans les flux ;
- erreurs, limites et résultats partiels conservés ;
- transferts externes et données IA maîtrisés ;
- risques résiduels et dépendances visibles ;
- livrable relu et passage explicitement validé.
