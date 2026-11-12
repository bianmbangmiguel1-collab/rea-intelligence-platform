# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Révision REA épinglée pour l'examen documentaire : `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` ; l'audit documentaire est partiel, les opérations pilotes exactes restent à confirmer.
- Langue de travail : français
- Objectif : concevoir et, après levée des blocages de gouvernance, réaliser une plateforme indépendante autour de REA ; ne déclarer des validations que sur preuve.

## Statut actuel

- Phase active : **phase 5 — réalisation locale de fondations autorisée sous périmètre restreint ; phase non terminée/non validée**.
- Phase 1 — audit REA : révision épinglée et sources de haut niveau examinées ; catalogue exhaustif/outils nécessaires au pilote, contrats détaillés et exécution restent ouverts/non testés.
- Phase 2 — conception fonctionnelle : décrite comme validée dans les documents du projet.
- Phase 3 — sécurité et exploitation : décrite comme validée au niveau documentaire.
- Phase 4 — porte avant réalisation : décision du propriétaire acceptée uniquement pour le sous-périmètre local/synthétique décrit dans `docs/09-phase-5/implementation-authorization.md`. Elle ne vaut pas clôture des prérequis d'intégration REA, d'utilisation de cibles réelles ou de déploiement.
- Phase 5 — réalisation contrôlée : autorisation limitée consignée ; plan de travail approuvé comme plan le 2026-11-12 ; aucun livrable applicatif ni résultat de test n'est encore attesté. La phase demeure non validée.
- `AGENTS.md` autorise le code et les tests locaux synthétiques dans ce périmètre, sans installation de nouvelles dépendances, lancement de REA, cible réelle, transfert externe ou déploiement.

## Périmètre autorisé à ce stade

- Travail local, mono-utilisateur, hors production et sans connexion à une cible externe.
- Modèles de domaine, contrats de plateforme, validation d'autorisation, provenance et flux simulés avec fixtures synthétiques.
- Tests unitaires et d'intégration isolés utilisant les outils déjà disponibles dans le dépôt/environnement autorisé.
- Toute technologie ou dépendance nouvelle doit faire l'objet d'une décision documentée avant ajout.
- Interdits dans ce périmètre : installer des outils/dépendances, lancer le moteur REA, exécuter des workflows dynamiques ou de provider, analyser des cibles réelles, utiliser des outils propriétaires sans licence validée, envoyer des données à une IA ou à tout service externe, déployer.

## Référence et dépendances

La révision `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f` est une référence documentaire. Le rapport d'audit précise que le catalogue exhaustif et les contrats opérationnels des outils retenus ne sont pas encore inventoriés ; aucune intégration d'exécution n'est donc autorisée par la présente portée.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage initial et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible d'une révision précise de REA | Révision épinglée ; audit documentaire partiel, contrats de pilote incomplets |
| 2 | Spécifications fonctionnelles et conception logique | Décrite comme validée |
| 3 | Conception détaillée sécurité, agent et exploitation | Décrite comme validée documentairement |
| 4 | Revue de conception et porte avant réalisation | Autorisation restreinte pour fondations locales/synthétiques ; autres usages bloqués |
| 5 | Développement, tests et recette | Active sous périmètre restreint ; plan approuvé, non terminée/non validée |

## Prochaine action

Suivre le plan de travail de phase 5, en commençant par les contrats de domaine purs. Consigner les décisions techniques et les changements, exécuter uniquement les vérifications permises et joindre leurs preuves. Toute extension de portée requiert une nouvelle autorisation.

## Journal de continuité

- L'audit documentaire REA cite des sources de haut niveau épinglées mais demeure incomplet pour les contrats exacts du pilote ; aucune exécution REA n'a été effectuée.
- Le propriétaire a explicitement autorisé le sous-périmètre local/synthétique et validé le plan de travail de phase 5 le 2026-11-12. Cette validation porte sur le plan, pas sur la réalisation ou la clôture.
- Le protocole de recette phase 5 définit des critères et preuves attendues ; aucun cas n'est déclaré exécuté.
- La phase 5 reste ouverte et non validée jusqu'à production des livrables et preuves de recette.
