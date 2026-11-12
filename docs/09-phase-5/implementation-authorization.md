# Autorisation de réalisation — phase 5

**Statut : AUTORISÉE SOUS PÉRIMÈTRE RESTREINT.** Cette autorisation ne clôt pas la phase 5 et ne vaut pas autorisation d'utiliser REA sur une cible réelle.

## Décision

À la demande explicite du propriétaire dans la conversation du 2026-11-12, démarrer uniquement les fondations locales, mono-utilisateur et hors production décrites ci-dessous. Cette décision est enregistrée comme autorisation de phase 5 limitée ; les tests et livrables restent à produire et à prouver.

- **Décideur :** propriétaire du dépôt (`bianmbangmiguel1-collab`, selon le contexte de session)
- **Date :** 2026-11-12
- **Statut :** approuvé pour le périmètre borné ci-dessous
- **Références :** `AGENTS.md`, `docs/03-governance/phase-4-gate-review.md`, `docs/09-phase-5/phase-5-acceptance-protocol.md`

## Périmètre autorisé

- Prototype local, mono-utilisateur, sans service cloud, multi-tenant ou production.
- Code de fondations, modèles métier et contrats de plateforme indépendants de l'exécution REA.
- Contrôles de périmètre, autorisation et provenance, implémentés sans appel moteur.
- Flux simulés avec fixtures synthétiques ; tests locaux unitaires et d'intégration à l'aide des outils déjà présents et autorisés.
- Toute décision de stack ou de dépendance nouvelle doit être documentée et approuvée avant son ajout. Pas d'installation ni téléchargement de dépendances au titre de cette autorisation.

## Exclusions qui demeurent bloquées

- Lancer REA, MCP REA, CLI REA ou un provider ; installer/configurer le moteur.
- Analyser un binaire, application, site, réseau, appareil ou autre cible réelle.
- Toute opération dynamique, interactive, réseau, navigateur, debug, instrumentée ou ayant un effet sur une cible.
- Installer des outils ou dépendances nouvelles, utiliser des composants propriétaires sans preuve de licence.
- Envoyer des données à une IA externe, OpenRouter ou un autre service externe.
- Déployer, exposer un endpoint distant, activer multi-utilisateur ou traiter de vraies données d'analyse.
- Modifier le dépôt source externe `morluto/rea`.

Une extension nécessite une autorisation distincte, une revue des risques et la mise à jour cohérente de `AGENTS.md`, du rapport d'audit et de la porte concernée.

## Conditions de recette et de clôture

Cette autorisation permet de commencer le travail restreint, pas de déclarer la phase réussie. La clôture demande les livrables réalisés, les résultats des tests approuvés, les anomalies/limites documentées et une validation finale après examen des preuves. Voir le [protocole de recette](phase-5-acceptance-protocol.md).
