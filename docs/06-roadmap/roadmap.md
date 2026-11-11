# Feuille de route

Les phases définissent des portes de décision. La progression documentaire ne signifie pas qu'un audit ou un test a été exécuté. Aucun passage à la réalisation sans validation explicite.

## Phase 0 — Cadrage initial — terminée

Vision, objectif d'intégrer REA, règle de non-réécriture et dépôt documentaire initial.

## Phase 1 — Audit de REA — terminé au niveau documentaire pour la révision de référence

Vérifier sur une révision déterminée du dépôt officiel les interfaces réellement exposées, leurs schémas, transports, capacités, sessions, preuves, erreurs, annulation, dépendances, licences et conditions d'usage.

**Révision de référence :** `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`  
**Source :** https://github.com/morluto/rea/commit/0909d89c966c30955fd0906b622ff25f3700789f

**Sortie :** rapport sourcé, révision auditée, matrice des capacités et questions restantes. Cette révision devient la base documentaire de référence pour la conception et la mise en œuvre.

## Phase 2 — Spécifications fonctionnelles et conception logique — validée par le propriétaire

Les exigences et parcours, l'architecture logique, le modèle conceptuel, les contrats API proposés, la gouvernance données/IA et les risques ont fait l'objet d'une revue de cohérence documentaire et d'une validation explicite du propriétaire.

**Résultat de revue :** base conceptuelle cohérente et validée comme point de départ. Les arbitrages de pilote, approbations, seuils non fonctionnels et dépendances REA restent à maîtriser selon les décisions de phase 3 et l'audit REA.

**Sortie requise :** décisions consignées, critères d'acceptation par exigence, dépendances REA sourcées ou explicitement ouvertes et validation du propriétaire. Cette étape est désormais satisfaite pour la phase 2.

## Phase 3 — Conception sécurité et exploitation — validée au niveau documentaire

Une proposition couvre l'identité et le cycle de vie des agents, le transport et l'isolation, les secrets, le cycle de vie des données, la gouvernance IA, les journaux, les incidents, l'exploitation et les responsabilités.

**Résultat de revue :** principaux domaines de risque représentés au niveau conceptuel ; mécanismes, paramètres, responsables et preuve d'efficacité ont été traités dans le cadre de la conception documentaire, et la validation du propriétaire est enregistrée au niveau des documents de phase 3.

**Sortie requise :** décisions attribuées, risques identifiés, vérifications mesurables définies et validation explicite du propriétaire. Cette étape est désormais satisfaite pour la phase 3.

## Phase 4 — Revue et porte avant réalisation — validée

Clôturer l'audit REA, vérifier les coûts/licences/périmètre pilote, définir les critères de recette de conception, obtenir les approbations fonctionnelle et sécurité du propriétaire et une autorisation explicite avant toute mise en œuvre.

**Révision de référence :** `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`  
**Validation de porte :** la revue documentaire a été clôturée et la décision de démarrer la réalisation est enregistrée.

## Phase 5+ — Réalisation — active sous périmètre documenté

Prototype contrôlé, agent, backend, interface, tests et déploiement sont autorisés dans le périmètre documenté après validation explicite de la phase 4. Aucun code applicatif ou test sur cible réelle ne doit être ajouté sans correspondre aux critères de cette phase et à la révision auditée.

## Critères transversaux

- faits REA cités avec révision et source ;
- exigences, choix acceptés, propositions, hypothèses et faits vérifiés distingués ;
- autorisations et limites représentées dans les flux ;
- erreurs, limites et résultats partiels conservés ;
- transferts externes et données IA maîtrisés ;
- risques résiduels et dépendances visibles ;
- livrable relu et passage explicitement validé.
