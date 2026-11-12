# Autorisation de réalisation — phase 5

**Statut : À COMPLÉTER — aucune portée d'implémentation n'est approuvée par ce formulaire vierge.** Une validation conversationnelle générale ne remplace pas l'autorisation écrite et la réconciliation des règles du dépôt.

## Blocage actuel à résoudre

`AGENTS.md` autorise actuellement uniquement la conception documentaire et interdit de produire du code applicatif, d'installer des outils, d'exécuter REA, d'analyser une cible réelle ou de déployer. Tant que ce texte n'est pas modifié par le propriétaire autorisé ou qu'une dérogation conforme et non ambiguë n'est pas consignée, ces restrictions s'appliquent.

L'audit documentaire disponible identifie `morluto/rea@0909d89c966c30955fd0906b622ff25f3700789f`, mais laisse le catalogue complet et les contrats opérationnels des outils retenus à examiner. La référence de commit n'est pas une autorisation d'usage ni une preuve de compatibilité.

## Proposition de périmètre initial — à approuver

À considérer comme option de réduction du risque, non comme décision acceptée :
- prototype local mono-utilisateur, sans service cloud ni multi-tenant ;
- mode sans IA, sans transfert externe ;
- pas de cible réelle ; fixtures synthétiques ou artefacts explicitement fournis comme appartenant au projet ;
- pas de workflows REA dynamiques, runtime, navigateur, réseau, appareil ou actions modifiant une cible ;
- pas d'outils propriétaires sans droits d'utilisation vérifiés ;
- adaptateur derrière interface déclarative à allowlist, sans commande arbitraire ni exécution déclenchée par un fichier importé.

## Décisions requises avant code

| Décision | Valeur à renseigner par le propriétaire |
| --- | --- |
| Pilote et utilisateurs | À compléter |
| Composants autorisés à être codés | À compléter |
| OS et environnement contrôlé | À compléter |
| Révision REA et opérations précises | Commit `0909d89c966c30955fd0906b622ff25f3700789f` mentionné ; opérations exactes à inventorier et approuver |
| Installation/dépendances permises | À compléter ; sources et versions épinglées |
| Données et transferts autorisés | À compléter ; valeur sûre par défaut : aucun transfert IA |
| Cibles / fixtures autorisées | À compléter ; aucune cible réelle sans autorisation séparée |
| Tests autorisés | À compléter, par environnement et catégorie |
| Budget, échéance, responsable | À compléter |
| Risques résiduels | À compléter avec propriétaire, traitement et date de réexamen |

## Visa de démarrage

À renseigner par le propriétaire après revue de `AGENTS.md`, du rapport REA, du périmètre et du protocole de recette :

- Décision : `à décider / approuvé / refusé`
- Nom du propriétaire habilité : à compléter
- Périmètre et exclusions acceptés : à compléter
- Référence des documents approuvés : à compléter
- Date : à compléter
- Conditions / révocation de l'autorisation : à compléter

## Non-autorisation implicite

Ce formulaire ne déclenche pas d'exécution de REA ou de cible. Chaque activité impliquant une installation, un provider externe, un transfert de données, une cible réelle ou un déploiement nécessite la permission spécifique et le cadre de vérification approprié.
