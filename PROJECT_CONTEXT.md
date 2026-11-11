# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Révision REA de référence : `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`
- Source de référence : `https://github.com/morluto/rea/commit/0909d89c966c30955fd0906b622ff25f3700789f`
- Langue de travail : français
- Objectif : concevoir une plateforme indépendante autour de REA ; poursuivre la documentation, la validation documentaire et la mise en œuvre conforme à la révision référencée.

## Statut actuel

- Phase active : **phase 5 — réalisation contrôlée et validée à la suite de la phase 4**.
- Phase 1 — audit technique REA : **terminé au niveau documentaire** ; la révision de référence est épinglée et documentée.
- Phase 2 — spécifications fonctionnelles et conception logique : **validée**.
- Phase 3 — sécurité et exploitation : **validée**.
- Phase 4 — porte avant réalisation : **validée** ; la revue finale est clôturée et l'autorisation de mise en œuvre est enregistrée.
- Code applicatif, installation d'outils, exécution de REA, analyse d'une cible réelle et déploiement : **autorisé dans le périmètre documenté de la phase 5**.
- Les commandes, capacités, formats, transports, sessions, preuves et prérequis REA issus de notes antérieures sont désormais **traités comme hypothèses documentées** jusqu'à confirmation dans la révision auditée.
- Les avis des revues sont documentaires ; ils ne valent pas approbation du propriétaire, audit technique, recette ni preuve de sécurité, sauf mention explicite de clôture de phase et de validation du propriétaire.

## Cadrage en cours

1. Intégrer le moteur officiel REA ; ne pas le réécrire et ne pas modifier son dépôt.
2. Architecture hybride visée : web/cloud, backend central, agents locaux et runners adaptés.
3. Windows prioritaire pour l'agent initial, sous réserve de compatibilité auditée.
4. Usage initial personnel, extensible ; pas de portée commerciale multi-utilisateur présumée.
5. OpenRouter envisagé, sans décision technique ni autorisation de transfert de données ; mode sans IA requis dans la conception.
6. Orientations d'architecture enregistrées dans les ADR à confirmer selon leur statut et l'approbation explicite.

Les technologies de stockage, file, identité, transport et hébergement demeurent proposées jusqu'à décision et vérification, mais la phase 5 peut avancer dans le périmètre documenté avec la révision auditée.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage initial et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible d'une révision précise de REA | Terminé au niveau documentaire pour la révision `0909d89c966c30955fd0906b622ff25f3700789f` |
| 2 | Spécifications fonctionnelles et conception logique | Validée par le propriétaire |
| 3 | Conception détaillée sécurité, agent et exploitation | Validée à ce niveau documentaire |
| 4 | Revue de conception et décision de démarrer la réalisation | Validée ; autorisation de phase 5 enregistrée |
| 5+ | Développement, tests et déploiement | Active ; sous périmètre documenté et contrôlé |

Les critères applicables sont dans [`docs/06-roadmap/roadmap.md`](docs/06-roadmap/roadmap.md). Les avis de revue sont consignés dans [`docs/03-governance/phase-review.md`](docs/03-governance/phase-review.md).

## Questions prioritaires ouvertes

- Quels outils/interfaces, transports, schémas, capacités, états, sessions, preuves et erreurs sont réellement documentés dans la révision de référence ?
- Quelles capacités et conditions sont compatibles avec Windows et Linux ?
- Quel fournisseur d'identité, hébergement, région, base, file et stockage seront retenus ?
- Quel modèle d'enrôlement, de transport, d'isolation, de mise à jour et de révocation agent est acceptable ?
- Quelles données pourront être transmises à un fournisseur IA, avec quel consentement, quelle rétention et quelles conditions ?
- Quels seuils de performance, disponibilité, budget, support et durée de conservation sont souhaités ?
- Quels risques résiduels peuvent être acceptés, par qui et avec quelle justification ?
- Quelles vérifications de conception seront exécutées dans la phase 5 avec leur responsable et leur preuve ?

## Prochaine action

La phase 5 démarre sous le périmètre architectural et de sécurité validé. La réalisation doit rester conforme à la révision REA de référence et aux contrôles de phase 4, avec traçabilité et preuve de validation par conception.

## Journal de continuité

- Le dépôt contient une première spécification fonctionnelle, une architecture logique, une analyse de menace initiale, un modèle conceptuel, des contrats API proposés, une roadmap et des ADR de cadrage.
- La documentation comprend une charte, un index documentaire, un plan d'audit REA, un registre initial des risques, une gouvernance données/IA, un cadre de traçabilité/validation, un agenda, les revues documentaires de sécurité et la feuille de route des phases.
- Les phases 2, 3 et 4 ont été validées au niveau documentaire ; la phase 5 est ouverte sous périmètre contrôlé.
- L'audit REA de référence est désormais épinglé sur la révision officielle `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`.
