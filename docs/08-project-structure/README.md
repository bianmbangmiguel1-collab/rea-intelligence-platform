# Arborescence cible du dépôt

**Statut :** proposition d'organisation, pas une arborescence applicative créée. Aucun répertoire de code, manifeste de dépendances, configuration d'exécution ou workflow de déploiement n'est ajouté avant la porte de réalisation. Les choix technologiques et le contrat REA restent ouverts.

## Principes

- Séparer l'interface, le backend, l'agent d'exécution, les contrats partagés et les documents.
- Isoler l'adaptateur REA derrière une frontière propre ; ne pas supposer ses interfaces avant audit.
- Séparer tests unitaires, intégration contrôlée et tests de sécurité ; aucun test sur cible réelle par défaut.
- Garder configurations d'exemple sans secret ; secrets et données d'analyse ne sont jamais committés.
- Conserver les domaines métier modulaires dans le backend initial, sans imposer des microservices.
- N'ajouter les dossiers applicatifs qu'après validation explicite de la phase 4.

## Arbre proposé pour la future réalisation

```text
rea-intelligence-platform/
├── README.md
├── AGENTS.md
├── PROJECT_CONTEXT.md
├── docs/
│   ├── README.md
│   ├── 00-project-charter.md
│   ├── 01-specifications/
│   ├── 02-architecture/
│   ├── 03-governance/
│   ├── 04-data-model/
│   ├── 05-api-contracts/
│   ├── 06-roadmap/
│   ├── 07-decisions/
│   └── 08-project-structure/
├── apps/
│   ├── web/                 # Interface utilisateur ; technologie à décider
│   └── api/                 # Backend modulaire ; technologie à décider
├── services/
│   └── analysis-agent/      # Agent local ; protocole et capacités à valider
├── packages/
│   ├── contracts/           # Types/schémas de plateforme versionnés
│   ├── domain/              # Concepts et règles indépendants des fournisseurs
│   └── ui/                  # Composants partagés si le besoin est confirmé
├── adapters/
│   ├── rea/                 # Adaptateur isolé, seulement après audit REA
│   ├── identity/            # Fournisseur d'identité à sélectionner
│   ├── storage/             # Stockage à sélectionner
│   └── ai/                  # Intégration facultative, gouvernée par politique
├── infrastructure/
│   ├── local/               # Environnement de développement contrôlé
│   └── deployment/          # À définir après choix d'hébergement et revue sécurité
├── tests/
│   ├── fixtures/            # Données synthétiques/non sensibles
│   ├── integration/          # Environnements contrôlés, aucune cible réelle par défaut
│   └── security/             # Scénarios autorisés et critères de recette
└── .github/
    ├── ISSUE_TEMPLATE/
    └── workflows/            # À créer après décision CI/CD et revue de sécurité
```

## Décisions de placement

| Élément | Emplacement proposé | Condition avant création |
| --- | --- | --- |
| Interface web | `apps/web/` | Pilote et technologie validés |
| API et modules métier | `apps/api/` | Contrats fonctionnels et politique d'identité validés |
| Agent local | `services/analysis-agent/` | Modèle de menace, transport, enrôlement et révocation validés |
| Contrats plateforme | `packages/contracts/` | Schémas d'API et de tâche stabilisés |
| Adaptateur REA | `adapters/rea/` | Audit d'une révision précise, licences et compatibilité vérifiées |
| Adaptateurs IA | `adapters/ai/` | Fournisseur, données, consentement et rétention approuvés ; option désactivable |
| Infrastructure et déploiement | `infrastructure/` | Hébergement, secrets, sauvegarde, coûts et contrôles validés |
| Tests | `tests/` | Stratégie, fixtures sûres et environnements autorisés définis |

## Ce qui n'est pas créé maintenant

Cette proposition ne crée pas les dossiers ci-dessus et ne choisit pas de langage, framework, gestionnaire de paquets, base de données, file, protocole d'agent, fournisseur IA ou cible de déploiement. Elle ne contient pas de code exécutable. Les répertoires de conception actuellement présents restent la seule arborescence à créer dans le cadre de la phase documentaire.

## Conditions pour matérialiser le squelette applicatif

1. Clôturer l'audit REA et enregistrer la révision, les sources et les licences.
2. Obtenir l'approbation propriétaire de la conception fonctionnelle et sécurité.
3. Arbitrer pilote, technologies, identité, données, transport, coûts et environnement de test.
4. Franchir la porte de phase 4 et consigner une autorisation explicite de réalisation.
5. Créer alors le squelette minimal, avec contrôles de secrets, CI et tests sûrs décidés en amont.
