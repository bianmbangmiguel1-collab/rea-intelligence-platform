# REA Intelligence Platform

Plateforme indépendante en conception pour organiser des projets d'analyse technique autour du moteur officiel [REA (`morluto/rea`)](https://github.com/morluto/rea), sans le réécrire ni modifier son dépôt.

> **Statut : phase 2 — conception documentaire active.** L'audit REA reste incomplet. Aucun code applicatif, outil installé, essai sur cible réelle ou déploiement n'est réalisé ou autorisé par le travail actuel.

## Commencer par la documentation

- **[Index documentaire](docs/README.md)** — état, statuts et navigation complète.
- [Charte du projet](docs/00-project-charter.md) — objectifs, limites et questions à confirmer.
- [Spécification fonctionnelle](docs/01-specifications/functional-specification.md)
- [Architecture détaillée](docs/02-architecture/detailed-architecture.md)
- [Sécurité et modèle de menace](docs/02-architecture/security-design.md)
- [Gouvernance données et IA](docs/03-governance/data-ai-governance.md)
- [Registre des risques](docs/03-governance/risk-register.md)
- [Plan d'audit REA](docs/03-governance/rea-audit-plan.md)
- [Traçabilité et validation](docs/03-governance/traceability-and-validation.md)
- [Agenda de conception phase 3](docs/03-governance/phase-3-design-agenda.md)
- [Modèle de données conceptuel](docs/04-data-model/data-model.md)
- [Contrats API proposés](docs/05-api-contracts/api-contracts.md)
- [Roadmap et portes de phase](docs/06-roadmap/roadmap.md)
- [Décisions d'architecture](docs/07-decisions/README.md)
- [Cahier de conception](docs/technical-design.md)
- [Contexte persistant](PROJECT_CONTEXT.md) · [Règles de continuité](AGENTS.md)

## Principes de conception

1. REA reste un moteur externe ; ses interfaces et capacités ne sont pas considérées vérifiées avant audit d'une révision identifiée.
2. La plateforme gouverne projets, autorisations, tâches, preuves et rapports.
3. Toute exécution future dépendra d'une autorisation explicite, d'un périmètre contrôlé et d'une décision de passage.
4. Les ressources importées sont non fiables et ne s'exécutent pas automatiquement.
5. Les preuves sources, résultats partiels, erreurs, hypothèses et conclusions validées restent distincts.
6. L'IA est facultative ; aucune donnée n'est transférée sans politique et approbation explicites.

## Prochaine porte

Valider le périmètre documentaire de phase 2, épingler une révision de REA pour l'audit et poursuivre la conception sécurité/exploitation. La réalisation ne commence qu'après clôture de l'audit, validation de la conception fonctionnelle et sécurité, revue des licences/coûts/périmètre et demande explicite de l'utilisateur.
