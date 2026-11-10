# Feuille de route

Les phases décrivent les portes de décision du projet. La progression documentaire ne signifie pas que les audits ou tests ont été exécutés. Aucun passage à la réalisation sans validation explicite.

## Phase 0 — Cadrage initiale — terminée

Vision, objectif d'intégrer REA, règles de non-réécriture et dépôt documentaire initial.

## Phase 1 — Audit de REA — incomplète / dépendance ouverte

Vérifier sur une révision identifiée du dépôt officiel : interface CLI/MCP, transports, schémas, providers/capacités, sessions, preuves, erreurs, annulation, dépendances, licences et compatibilité OS.

**Sortie :** rapport sourcé, révision auditée, matrice des capacités et questions restantes. Les éléments du document d'architecture actuellement décrits comme commandes REA restent des hypothèses tant que non vérifiés.

## Phase 2 — Spécifications fonctionnelles et conception logique — active

Travaux en cours :

- exigences et parcours utilisateur ;
- composants et frontières de confiance ;
- modèle de données conceptuel ;
- propositions de contrats API de la plateforme ;
- premiers contrôles de sécurité et critères d'acceptation.

**Sortie :** documents cohérents, risques et questions ouverts visibles ; validation de l'utilisateur. Les détails d'intégration REA sont conditionnels à la phase 1.

## Phase 3 — Conception sécurité et exploitation — à faire

Compléter le modèle de menace, transport/enrôlement/révocation agent, isolation, secrets, stockage, sauvegarde, rétention, observabilité, réponse aux incidents et plan de tests.

**Sortie :** conception sécurité/exploitation révisée et validée.

## Phase 4 — Revue et porte avant réalisation

Clôturer l'audit et la conception, vérifier coût/licences/périmètre pilote, préciser les critères de recette et obtenir la demande explicite de démarrer le développement.

## Phase 5+ — Réalisation — non autorisée à ce stade

Prototype contrôlé, agent, backend, interface, tests et déploiement seront planifiés après la phase 4. Ne pas commencer avant.

## Critères transversaux

- faits REA cités avec révision/source ;
- décisions distinguées des propositions ;
- permissions et autorisations représentées dans les flux ;
- erreurs, limites et résultats partiels conservés ;
- données externes/IA maîtrisées ;
- livrable de la phase relu et passage explicite.