# REA Intelligence Platform

Plateforme indépendante d'orchestration et d'analyse technique intégrant le moteur officiel [REA (morluto/rea)](https://github.com/morluto/rea).

> **Statut : conception fonctionnelle et technique en cours. Aucun code applicatif.**

## Documents de référence

- [Cahier d'architecture général](docs/technical-design.md)
- [Spécifications fonctionnelles et critères](docs/01-specifications/functional-specification.md)
- [Architecture détaillée et frontières de confiance](docs/02-architecture/detailed-architecture.md)
- [Sécurité et modèle de menace](docs/02-architecture/security-design.md)
- [Modèle de données conceptuel](docs/04-data-model/data-model.md)
- [Contrats API proposés](docs/05-api-contracts/api-contracts.md)
- [Roadmap et portes de phase](docs/06-roadmap/roadmap.md)
- [Décisions d'architecture](docs/07-decisions/README.md)
- [Contexte persistant du projet](PROJECT_CONTEXT.md)
- [Consignes de continuité](AGENTS.md)

## Principes

1. REA reste le moteur spécialisé : pas de réécriture ni de fork principal.
2. La plateforme orchestre projets, agents, preuves, IA et rapports.
3. Les analyses qui nécessitent des fichiers locaux ou des outils natifs s'exécutent sur un agent ou un runner adapté.
4. Les résultats, erreurs, limites et preuves d'origine de REA sont préservés.
5. Observations, hypothèses et conclusions validées sont distinguées.
6. Les analyses sont limitées aux cibles que l'utilisateur possède ou est autorisé à examiner.
7. Les ressources importées sont en quarantaine et ne sont jamais exécutées automatiquement.

## État de conception

La conception de la plateforme démarre sur la base des hypothèses indiquées dans le cahier d'architecture. L'audit technique du dépôt REA reste une dépendance ouverte : aucun détail de commande, transport MCP, format de sortie, capacité ou comportement de REA ne doit être considéré comme vérifié avant d'être confirmé sur une révision identifiée du dépôt officiel.
