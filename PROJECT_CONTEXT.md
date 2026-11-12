# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Révision REA mentionnée comme référence : `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` ; le rapport disponible ne constitue pas un audit complet des interfaces et capacités.
- Langue de travail : français
- Objectif : concevoir une plateforme indépendante autour de REA ; respecter les consignes du dépôt, puis produire et valider les livrables selon les portes documentées.

## Statut actuel

- Phase active : **phase 5 — non réalisée et non validée**.
- Phase 1 — audit REA : révision épinglée et rapport documentaire sommaire présent ; les interfaces et propriétés du moteur restent à vérifier selon le rapport lui-même.
- Phase 2 — conception fonctionnelle : décrite comme validée dans les documents du projet.
- Phase 3 — sécurité et exploitation : décrite comme validée au niveau documentaire.
- Phase 4 — porte avant réalisation : décrite comme validée dans certains documents ; la clôture doit rester conforme aux consignes applicables du dépôt.
- Phase 5 — réalisation contrôlée : plan documentaire présent ; aucun livrable applicatif, résultat de test ou preuve de recette identifié. Ne pas déclarer la phase terminée.
- `AGENTS.md` restreint actuellement le travail à la conception documentaire et interdit le code applicatif, l'installation d'outils, l'exécution REA, l'analyse sur cible réelle et le déploiement.

## Cadrage en cours — à confirmer

1. Intégrer le moteur officiel REA ; ne pas le réécrire et ne pas modifier son dépôt.
2. Architecture hybride visée : web/cloud, backend central, agents locaux et runners adaptés.
3. Windows prioritaire pour l'agent initial, sous réserve de compatibilité démontrée.
4. Usage initial personnel, extensible ; pas de portée commerciale multi-utilisateur présumée.
5. OpenRouter envisagé, sans décision ni autorisation de transfert de données ; mode sans IA requis dans la conception.
6. Les technologies de stockage, file, identité, transport et hébergement demeurent à décider.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage initial et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible d'une révision précise de REA | Révision épinglée ; audit des contrats incomplet selon le rapport disponible |
| 2 | Spécifications fonctionnelles et conception logique | Décrite comme validée |
| 3 | Conception détaillée sécurité, agent et exploitation | Décrite comme validée documentairement |
| 4 | Revue de conception et porte avant réalisation | Décrite comme validée ; conformité aux consignes du dépôt à réconcilier |
| 5 | Développement, tests et recette | Non commencée / non validée ; bloquée par `AGENTS.md` et l'absence de preuves |

## Prochaine action

Le propriétaire doit résoudre le blocage de gouvernance dans `AGENTS.md`, compléter l'audit de la révision REA avec des sources concrètes, puis autoriser et réaliser les livrables dans un environnement contrôlé. La phase 5 ne pourra être clôturée qu'après exécution des critères de recette et enregistrement des preuves.

## Journal de continuité

- Un plan documentaire de phase 5 est présent ; il ne prouve pas une implémentation.
- Le rapport REA présent épingle un commit mais indique que plusieurs propriétés techniques restent à vérifier.
- Aucun test, installation, exécution REA sur cible, développement ou déploiement n'est attesté dans les documents examinés.
- L'état de validation de phase 5 est consigné dans `docs/09-phase-5/phase-5-validation-status.md`.
