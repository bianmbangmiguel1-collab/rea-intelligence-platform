# REA Intelligence Platform

Plateforme indépendante en conception pour organiser des projets d'analyse technique autour du moteur officiel [REA (`morluto/rea`)](https://github.com/morluto/rea), sans le réécrire ni modifier son dépôt.

> **Statut : phase 5 non réalisée et non validée.** Le dépôt ne contient qu'un plan de mise en œuvre documentaire. Les consignes actuelles interdisent le code applicatif, l'installation d'outils, l'exécution de REA, l'analyse sur cible réelle et le déploiement. Aucun résultat de recette n'est consigné.

## Commencer par la documentation

- [Index documentaire](docs/README.md) — statuts et navigation.
- [Contexte persistant](PROJECT_CONTEXT.md) · [Règles de continuité](AGENTS.md)
- [Spécification fonctionnelle](docs/01-specifications/functional-specification.md)
- [Architecture détaillée](docs/02-architecture/detailed-architecture.md)
- [Conception sécurité](docs/02-architecture/security-design.md)
- [Plan d'audit REA](docs/03-governance/rea-audit-plan.md) · [Rapport disponible](docs/03-governance/rea-audit-report.md)
- [Porte de phase 4](docs/03-governance/phase-4-gate-review.md)
- [Plan d'implémentation phase 5](docs/09-phase-5/phase-5-implementation-plan.md) · [État de validation](docs/09-phase-5/phase-5-validation-status.md)
- [Roadmap](docs/06-roadmap/roadmap.md)

## Principes de conception

1. REA reste un moteur externe ; ses interfaces et capacités ne sont pas considérées vérifiées avant un audit détaillé d'une révision identifiée.
2. La plateforme gouverne projets, autorisations, tâches, preuves et rapports.
3. Toute exécution dépend d'une autorisation explicite, d'un périmètre contrôlé et des règles du dépôt.
4. Les ressources importées sont non fiables et ne s'exécutent pas automatiquement.
5. Les preuves sources, résultats partiels, erreurs, hypothèses et conclusions validées restent distincts.
6. L'IA est facultative ; aucune donnée n'est transférée sans politique et approbation explicites.
