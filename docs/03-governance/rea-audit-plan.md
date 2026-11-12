# Plan documentaire d'audit de REA

**Statut :** protocole proposé ; audit documentaire partiel consigné dans le [rapport de référence](rea-audit-report.md). Aucune installation, exécution de REA ni analyse de cible n'est attestée par ce plan.

## Objectif et limites

Produire un rapport reproductible sur une révision précisément identifiée de `morluto/rea`, afin de savoir si et comment une intégration pourrait être conçue. L'audit ne modifie pas le dépôt externe et ne lance pas l'outil. Un examen de sources est distinct d'un test d'exécution et d'un audit de sécurité indépendant.

## Identité de la révision

| Champ | Valeur |
| --- | --- |
| URL du dépôt source | `https://github.com/morluto/rea` |
| Commit immuable | `0909d89c966c30955fd0906b622ff25f3700789f` |
| URL commit | `https://github.com/morluto/rea/commit/0909d89c966c30955fd0906b622ff25f3700789f` |
| Date du commit consultée | `2026-11-11T15:49:30Z` |
| Sources de haut niveau consultées | README, package.json, server.json, mcp.json, référence MCP, guides CLI/installation, SECURITY, DISCLAIMER, LICENSE, THIRD_PARTY_NOTICES et guide native-initializers ; liens épinglés dans le rapport. |
| Auditeur / limites | Revue documentaire assistée ; aucun test, installation, lancement ou validation juridique. |
| Licence | Fichier LICENSE déclare MIT pour le code REA-authored ; les composants et outils tiers gardent leurs propres licences/conditions ; voir THIRD_PARTY_NOTICES. |

Ne pas agréger les observations de versions différentes. Si la révision change, créer un rapport distinct ou documenter explicitement la comparaison.

## État des axes

| Axe | Preuve attendue | État actuel |
| --- | --- | --- |
| Interface MCP/CLI | catalogue exhaustif, source et schémas par opération | Partiel : protocole et exemples publics consultés ; catalogue complet non inventorié |
| Transport et cycle de vie | modes exacts, lancement, arrêt, annulation et timeouts, par workflow | Partiel ; stdio documenté, limites HTTP relevées ; opérations individuelles à examiner |
| Entrées/sorties | schémas et erreurs exacts, résultats partiels et compatibilité | Partiel : règles communes Evidence documentées, fiches outil manquantes |
| Capacités et providers | opérations exactes, conditions, versions, OS et limites | Partiel : familles générales au README, mapping exhaustif non fait |
| Sessions et preuves | identifiants, persistance, provenance et formats effectivement exposés | Partiel : Evidence/MCP documentés à haut niveau, tests et mapping plateforme absents |
| Dépendances et installation | inventaire de versions, provenance, licences, conditions | Partiel : manifestes et notices lus, audit juridique exhaustif non effectué |
| Compatibilité | matrice sourcée par OS, architecture, runtime et provider | Incomplète ; exigences runtime principales connues, compatibilité du pilote non démontrée |
| Sécurité | permissions, accès réseau/fichiers, frontières et contrôles observables | Revue documentaire de SECURITY/DISCLAIMER ; pas d'audit technique ni test d'efficacité |
| Maintenance | changements, politique de mise à jour et compatibilité | Partiel ; référence épinglée, politique par usage à préciser |
| Exécution et annulation | effets, refus, interruption, arrêt et résultat partiel de chaque opération | Non testé ; garanties doivent rester propres à l'opération/provider |

## Méthode de consignation

Pour chaque constat, consigner : ID, statut (`vérifié documentairement`, `hypothèse`, `inconnu`, `non applicable`, `non testé`), formulation précise, URL/path, commit source, date de consultation, effet sur le produit et vérification suivante. Une affirmation provenant d'une page générale ne doit pas être extrapolée à tous les outils.

## Livrables de sortie

1. révision et sources identifiées ;
2. matrice des opérations nécessaires au pilote, avec contrat et preuve par ligne ;
3. analyse des licences pour les seuls composants réellement retenus ;
4. écarts entre besoins et contrats observés ;
5. risques, inconnues, recommandations et décisions à faire trancher ;
6. conclusion distincte : faisabilité documentaire, validation technique, compatibilité et autorisation d'usage.

## Porte de clôture

La phase d'audit ne peut être marquée terminée que si les axes nécessaires au périmètre sont sourcés, les inconnues visibles, la licence vérifiée au niveau pertinent et la conclusion revue par le propriétaire. Un test ou une exécution doit être planifié et autorisé séparément ; aucune exécution de cible réelle n'est implicite.
