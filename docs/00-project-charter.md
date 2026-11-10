# Charte du projet — REA Intelligence Platform

**Statut :** cadrage proposé, à valider par le propriétaire du projet. Ce document n'autorise ni audit opérationnel ni réalisation.

## Vision

Concevoir une plateforme indépendante qui gouverne des travaux d'analyse technique, organise projets, autorisations, agents et résultats, et pourrait intégrer le moteur externe [morluto/rea](https://github.com/morluto/rea) après audit. La plateforme ne réécrit pas REA et ne transforme pas son dépôt en dépôt principal du projet.

## Objectifs proposés

- Centraliser les projets, cibles, autorisations et limites applicables.
- Orchestrer des tâches vers des environnements d'exécution explicitement autorisés.
- Relier résultats et rapports à leurs sources, versions, limites et décisions.
- Permettre une assistance IA facultative, gouvernée par des règles de données et de consentement.
- Concevoir des contrôles de sécurité, de révocation et de traçabilité avant toute réalisation.

## Hors périmètre explicite à ce stade

- Toute activité sans autorisation documentée ou qui dépasse le périmètre autorisé.
- L'exécution d'analyses REA sur une cible réelle dans le cadre du travail documentaire.
- La réécriture, le fork principal ou la modification du dépôt externe `morluto/rea`.
- L'exécution automatique de fichiers, scripts ou ressources importés ; l'exécution de commandes arbitraires proposées par une personne ou une IA.
- Le contournement de contrôles, les opérations destructrices et la promesse de compatibilité REA non démontrée.
- La définition d'un modèle commercial, d'un déploiement de production ou d'un engagement de disponibilité sans décision dédiée.

## Utilisateurs et contexte initial

L'usage personnel est une hypothèse de cadrage ; les rôles propriétaire, opérateur et lecteur sont définis dans la [spécification fonctionnelle](01-specifications/functional-specification.md). Windows est prioritaire pour un agent initial, sous réserve d'une étude de compatibilité. OpenRouter est envisagé, sans décision de transfert de données ni preuve de compatibilité.

## Principes non négociables proposés

1. Une analyse ne peut pas être exécutée sans périmètre et autorisation valides, vérifiables et non expirés.
2. Les données provenant d'une cible ou d'un import sont non fiables ; aucun contenu ne devient une instruction d'exécution.
3. L'IA ne peut ni accorder des permissions ni approuver ses propres actions.
4. Le partage externe est désactivé par défaut dans la conception tant qu'une politique explicite n'est pas définie.
5. Les données sources, synthèses, hypothèses, erreurs, résultats partiels et limites restent distincts et traçables.
6. Aucune capacité REA n'est annoncée comme disponible avant vérification sur une révision identifiée.

## Catégories de statut documentaire

- **Exigence plateforme :** comportement attendu indépendamment du contrat REA.
- **Choix accepté :** décision formellement acceptée et consignée ; sinon, l'ADR est proposé.
- **Proposition à confirmer :** option de conception, technologie ou politique non arbitrée.
- **Fait vérifié :** preuve référencée avec source, date et révision/version.
- **Hypothèse :** élément non confirmé ; elle ne doit pas servir de garantie ou de contrat.

## Portes et conditions de réalisation

La phase actuelle est documentaire. Toute réalisation reste interdite jusqu'à la clôture de l'audit REA, la validation de la conception fonctionnelle et sécurité, la revue des licences, coûts et limites du pilote, puis une demande explicite de démarrer le développement. La [roadmap](06-roadmap/roadmap.md) est la référence pour les critères de passage.

## Questions de cadrage à trancher

- Quel utilisateur, cas d'usage et type d'analyse composent le pilote minimal ?
- Quelle révision immuable de REA servira de référence d'audit ?
- Quelles cibles et opérations seront explicitement autorisées ou exclues ?
- Quelle identité, infrastructure, région, rétention et politique de sauvegarde sont acceptables ?
- Quelles catégories de données, le cas échéant, peuvent être envoyées à un fournisseur IA ?
- Quels seuils de coût, performance, disponibilité et durée de conservation sont nécessaires ?
