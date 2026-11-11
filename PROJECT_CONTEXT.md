# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante, non modifiée par ce projet
- Révision REA de référence : `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`
- Source de référence : `https://github.com/morluto/rea/commit/0909d89c966c30955fd0906b622ff25f3700789f`
- Langue de travail : français
- Objectif : concevoir et mettre en œuvre une plateforme indépendante autour de REA, dans le périmètre documenté et avec validation de sécurité et de recette.

## Statut actuel

- Phase active : **phase 5 — plan de mise en œuvre finalisé ; exécution réelle soumise aux validations de recette**.
- Phase 1 — audit technique REA : **terminé au niveau documentaire** ; la révision de référence est épinglée et documentée.
- Phase 2 — spécifications fonctionnelles et conception logique : **validée**.
- Phase 3 — sécurité et exploitation : **validée**.
- Phase 4 — porte avant réalisation : **validée** ; la revue finale est clôturée et l'autorisation de mise en œuvre est enregistrée.
- Phase 5 — réalisation contrôlée : **plan finalisé**, mais **aucune implémentation applicative ni exécution REA n'est déclarée validée** sans preuve de recette.
- Les commandes, capacités, formats, transports, sessions, preuves et prérequis REA issus de notes antérieures restent des **hypothèses documentées** tant qu'ils ne sont pas vérifiés dans la révision auditée.

## Cadrage en cours

1. Intégrer le moteur officiel REA ; ne pas le réécrire et ne pas modifier son dépôt.
2. Architecture hybride visée : web/cloud, backend central, agents locaux et runners adaptés.
3. Windows prioritaire pour l'agent initial, sous réserve de compatibilité auditée.
4. Usage initial personnel, extensible ; pas de portée commerciale multi-utilisateur présumée.
5. OpenRouter envisagé, sans décision technique ni autorisation de transfert de données ; mode sans IA requis dans la conception.
6. Orientations d'architecture enregistrées dans les ADR à confirmer selon leur statut et l'approbation explicite.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage initial et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible d'une révision précise de REA | Terminé au niveau documentaire |
| 2 | Spécifications fonctionnelles et conception logique | Validée par le propriétaire |
| 3 | Conception détaillée sécurité, agent et exploitation | Validée à ce niveau documentaire |
| 4 | Revue de conception et décision de démarrer la réalisation | Validée ; autorisation enregistrée |
| 5 | Réalisation contrôlée | Plan finalisé ; mise en œuvre soumise à validation de recette |

## Prochaine action

La phase 5 passe au niveau de mise en œuvre réelle uniquement après validation explicite du périmètre fonctionnel et de sécurité, le plan documentaire étant désormais fermé. Les changements appliqués doivent rester alignés sur la révision REA de référence et sur les critères de recette définis dans le projet.

## Journal de continuité

- Les phases 2, 3 et 4 sont documentées et validées selon le cadre du dépôt.
- La révision REA de référence est épinglée et utilisée comme base de conception.
- Le plan de mise en œuvre de la phase 5 est finalisé, mais aucune exécution sur cible réelle n'est validée sans preuve de recette.
