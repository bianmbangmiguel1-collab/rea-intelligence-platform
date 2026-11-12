# Feuille de route

Les phases définissent des portes de décision. La progression documentaire ne signifie pas qu'un audit ou un test a été exécuté. Les statuts doivent refléter les preuves disponibles et ne peuvent pas être avancés par une simple checklist préremplie.

## Phase 0 — Cadrage initial — terminée

Vision, objectif d'intégrer REA, règle de non-réécriture et dépôt documentaire initial.

## Phase 1 — Audit de REA — révision épinglée, audit technique incomplet

Le rapport de référence nomme `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` et cite des métadonnées de dépôt. Il précise cependant que les interfaces exactes, transports, sessions et propriétés du moteur doivent continuer à être vérifiés. Un SHA immuable fixe la version observée, mais ne prouve pas à lui seul l'audit des contrats.

Voir le [plan d'audit](../03-governance/rea-audit-plan.md) et le [rapport disponible](../03-governance/rea-audit-report.md).

## Phase 2 — Spécifications fonctionnelles et conception logique — décrite comme validée

La spécification et les documents associés sont consignés comme base de conception. Cela ne constitue pas une recette d'implémentation.

## Phase 3 — Conception sécurité et exploitation — décrite comme validée documentairement

La conception documentaire existe. L'efficacité de contrôles techniques n'a pas été démontrée par les documents consultés.

## Phase 4 — Revue et porte avant réalisation — décrite comme validée dans les documents de porte

La porte contient une décision de validation enregistrée. Les critères de réalisation restent soumis aux consignes de `AGENTS.md` et aux preuves d'audit et de sécurité applicables.

## Phase 5 — Réalisation contrôlée — non commencée / non validée

Le plan documentaire est présent, mais aucun livrable applicatif ni rapport de recette n'est attesté. En outre, `AGENTS.md` interdit actuellement la réalisation applicative, l'installation, l'exécution de REA, l'analyse sur cible réelle et le déploiement.

**Conditions de reprise :**
1. résoudre la contradiction entre la porte de phase 4 et les consignes actives de `AGENTS.md` par une décision appropriée du propriétaire ;
2. compléter l'audit REA avec preuves détaillées de la révision et des interfaces nécessaires ;
3. produire les livrables contrôlés de phase 5 après autorisation ;
4. exécuter les tests approuvés et consigner résultats, anomalies, limites et preuves ;
5. obtenir la revue et la validation du propriétaire après réalisation.

La phase 5 ne peut être déclarée terminée par la finalisation de son plan seulement.

## Critères transversaux

- faits REA cités avec révision et source ;
- exigences, décisions, propositions, hypothèses et faits vérifiés distingués ;
- autorisations et limites représentées dans les flux ;
- erreurs, limites et résultats partiels conservés ;
- transferts externes et données IA maîtrisés ;
- risques résiduels et dépendances visibles ;
- livrable relu et passage explicitement validé.
