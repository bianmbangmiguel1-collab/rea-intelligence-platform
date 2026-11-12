# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Révision REA épinglée pour l'examen documentaire : `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` ; l'audit de haut niveau est documenté, mais les outils et contrats propres au pilote restent à inventorier.
- Langue de travail : français
- Objectif : concevoir et, après levée des blocages de gouvernance, réaliser une plateforme indépendante autour de REA ; ne déclarer des validations que sur preuve.

## Statut actuel

- Phase active : **phase 5 — non réalisée et non validée ; préparation documentaire en cours**.
- Phase 1 — audit REA : révision épinglée et sources de haut niveau examinées ; catalogue exhaustif/outils nécessaires au pilote, contrats détaillés et exécution restent ouverts/non testés.
- Phase 2 — conception fonctionnelle : décrite comme validée dans les documents du projet.
- Phase 3 — sécurité et exploitation : décrite comme validée au niveau documentaire.
- Phase 4 — porte avant réalisation : porte documentée comme validée, mais sa checklist d'audit complet contient des assertions non étayées par le rapport initial ; le dépôt a besoin d'une réconciliation formelle.
- Phase 5 — réalisation contrôlée : plan, formulaire d'autorisation et protocole de recette documentés ; aucun livrable applicatif ou résultat de test attesté.
- `AGENTS.md` restreint actuellement le travail à la conception documentaire et interdit le code applicatif, l'installation d'outils, l'exécution REA, l'analyse sur cible réelle et le déploiement.

## Cadrage en cours — à confirmer

1. Intégrer le moteur officiel REA ; ne pas le réécrire et ne pas modifier son dépôt.
2. Architecture hybride visée : web/cloud, backend central, agents locaux et runners adaptés, encore à décider/valider.
3. Windows prioritaire pour l'agent initial, sous réserve de compatibilité démontrée.
4. Usage initial personnel, extensible ; pas de portée commerciale multi-utilisateur présumée.
5. OpenRouter envisagé, sans décision ni autorisation de transfert de données ; mode sans IA requis dans la conception.
6. Les technologies de stockage, file, identité, transport et hébergement demeurent à décider.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage initial et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible d'une révision précise de REA | Révision épinglée, audit documentaire partiel, contrats de pilote incomplets |
| 2 | Spécifications fonctionnelles et conception logique | Décrite comme validée |
| 3 | Conception détaillée sécurité, agent et exploitation | Décrite comme validée documentairement |
| 4 | Revue de conception et porte avant réalisation | Décrite comme validée ; prérequis d'audit et consignes à réconcilier |
| 5 | Développement, tests et recette | Non commencée / non validée ; bloquée par `AGENTS.md` et l'absence de preuves |

## Prochaine action

Le propriétaire complète l'inventaire REA nécessaire au pilote, réconcilie `AGENTS.md` et le registre de porte, puis remplit le formulaire d'autorisation avec portée et limites. Après autorisation, les livrables et tests pourront être produits en environnement contrôlé ; ne clore la phase 5 qu'après revue de preuves.

## Journal de continuité

- L'audit documentaire REA cite maintenant README, package, métadonnées MCP, contrats MCP/CLI, sécurité, disclaimer et licences, tous épinglés sur la même révision.
- L'audit reste partiel : aucun appel d'outil, installation, test d'exécution, examen exhaustif de catalogue ni analyse cible n'a été effectué.
- Le protocole de recette phase 5 définit des critères et preuves attendues ; aucun cas n'a été exécuté.
- L'état de phase 5 reste bloqué/non validé conformément aux consignes présentes et aux preuves disponibles.
