# Contexte persistant du projet

> Lire ce fichier avant toute tâche. Le mettre à jour quand la phase, les décisions, les risques ou la prochaine action changent.

## Identité

- Nom : REA Intelligence Platform
- Dépôt : `bianmbangmiguel1-collab/rea-intelligence-platform`
- Moteur prévu : `morluto/rea`, dépendance externe indépendante
- Langue : français
- Objectif utilisateur : placer la conception sur GitHub avant de commencer le développement.

## Statut maintenant

- Phase de travail : **conception fonctionnelle et technique (phase 2) — démarrée**.
- Phase 1 (audit technique REA) : **incomplète**. Son rapport, la révision auditée et les contrats REA ne sont pas établis dans ce dépôt.
- Code applicatif : **aucun et non autorisé dans cette phase**.
- Analyse d'une cible réelle : non prévue dans le travail de conception.
- Dépôt `morluto/rea` : aucune modification.
- Les détails REA non confirmés sont des hypothèses et doivent être marqués comme tels.

## Choix de cadrage actuellement retenus

1. Option A : intégrer le moteur officiel REA, ne pas le réécrire et ne pas transformer le dépôt de plateforme en fork principal.
2. Architecture hybride visée : web/cloud, backend central, agents locaux et runners adaptés.
3. Windows prioritaire pour l'agent initial, sous réserve de compatibilité REA et providers à vérifier.
4. Usage initial personnel, extensible ; pas de portée commerciale multi-utilisateur à supposer.
5. OpenRouter envisagé comme premier fournisseur IA ; le système doit pouvoir fonctionner sans IA distante.
6. Aucun démarrage de réalisation avant validation explicite de la conception.

Ces choix ne constituent pas une preuve de compatibilité technique du dépôt REA. Les technologies de stockage, file et hébergement restent proposées jusqu'à leur validation.

## Phases et portes

| Phase | Objet | État |
| --- | --- | --- |
| 0 | Cadrage et dépôt documentaire | Terminé au niveau initial |
| 1 | Audit reproductible de REA | Incomplet / dépendance à fermer |
| 2 | Spécifications fonctionnelles et conception de la plateforme | Active, conception préliminaire |
| 3 | Conception détaillée sécurité, agent et exploitation | À détailler ensuite |
| 4 | Revue de conception et décision de démarrer la réalisation | Bloquée jusqu'à validation explicite |
| 5+ | Développement, tests, déploiement | Pas commencé / non autorisé |

Le travail conceptuel de phase 2 peut avancer sur les besoins indépendants de REA. Les contrats d'intégration exacts et les décisions qui dépendent du moteur demeurent provisoires jusqu'à clôture de la phase 1.

## Questions ouvertes prioritaires

- Quelle révision/tag/commit de `morluto/rea` sera la référence d'audit ?
- Quels sont les outils MCP/CLI, transports, schémas, états, sessions et preuves effectivement disponibles dans cette révision ?
- Quelles capacités et prérequis fonctionnent sur Windows et Linux ?
- Quel fournisseur d'identité, hébergement, base, file et stockage sera retenu ?
- Quel sera le modèle de transport, d'enrôlement, de mise à jour et de révocation de l'agent ?
- Quelles données pourront être transmises à un modèle externe, pour quelle rétention et avec quel consentement ?
- Quelle politique d'autorisation et de conservation s'appliquera au pilote ?

## Prochaine action

Développer les spécifications fonctionnelles et la conception logique sans coder, en marquant les dépendances REA « à confirmer ». En parallèle ou ensuite, fermer l'audit REA en enregistrant une révision précise et des sources vérifiables. Puis revoir les contrats d'intégration et faire valider les phases 2 à 4 avant toute réalisation.

## Journal de continuité

- Le README initial a été remplacé par une présentation du projet et des principes de conception.
- La conception de phase 2 est démarrée : spécifications fonctionnelles, architecture détaillée, sécurité, modèle de données et contrats de plateforme proposés.
- Rappel : l'audit REA n'est pas déclaré terminé. Aucun code ni test sur cible réelle n'a été exécuté.